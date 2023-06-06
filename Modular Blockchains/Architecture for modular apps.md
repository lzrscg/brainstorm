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
Given 2 chains, we cannot assume that they will have the same data retrieval APIs. However, it is possible that they do. For example, many chains utilize the EVM. The chains all share common characteristics, such as the endpoint `eth_getTransactionByHash`.


