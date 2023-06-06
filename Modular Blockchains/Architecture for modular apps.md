Building apps for modular blockchains can be challenging due the variation in each individual chain. Forgetting about the modular architecture (i.e. splitting execution, DA, and settlement) for a second, the new multi-chain era comes with its own problems.

For example:
- Not all chains are EVM
- Not all EVMs are equivalent
- Even equivalent VMs may be configured differently (such as having different TPS)

All of these things can break the assumptions that we make when we build apps. And, therefore, we want to build apps that abstract all of them away. I will walk through several patterns that we can use to do this.

# The easy way
Step 1. Build AGI.
Step 2. Have AGI create an integration for each chain.

Unfortunately, we are unable to do this with current technology. So we must go with the other solution.

# The hard way
The reality is that each chain must be integrated individually, because of our first tenet:

> **Tenet 1:** We cannot make common assumptions about all protocols.

Therefore, our strategies revolve around reducing the impact of needing to build these integrations. How can we make this process as easy as possible?

## Optimizing reusability
Given any 2 chainz, we cannot assume that they will have the same data retrieval APIs. However, it is *possible* that they do. For example, many chains utilize the EVM. These chains all share common characteristics, such as the endpoint `eth_getTransactionByHash`.

So it is therefore reasonable to to create a general **EVM integration**. However, it is important re-emphasize that there is no one-size fits all EVM integration. Even the aforementioned `eth_getTransactionByHash` endpoint may or may not support [EIP-1559](https://eips.ethereum.org/EIPS/eip-1559) fields such as `maxPriorityFeePerGas`.

### 80/20 Integrations
How can you get 80% of the benefits of a multichain app by doing only 20% of the work? **Prioritize the EVM and Cosmos.** 

A large majority of projects with adoption are in those two respective ecosystem. I expect this share to decrease over time, however, this is certainly true for the time being.

Here are some difference to look out for between Cosmos and EVM chains.

**Differences between Cosmos chains:**
- The biggest challenge we have faced is each chain can having different message schemas. So someone indexing a Cosmos chain will likely need to load unique protobufs for each chain.

**Differences between EVM chains:**
- 