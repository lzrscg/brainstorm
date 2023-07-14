Going to talk about how Bitcoin is not about reaching consensus, it's actually the opposite. It's about not reaching consensus.

Bitcoin is a miracle
- Starting at the beginning of it all
- Most people thought it would fail (including economists)
- It was a crazy idea
- Many people thought it died the second it had problems
- The use case struck a nerve, it could have faded off into obscurity like many other cool trends online

Bitcoin is an application
- The use case was digital money
- Although it can be thought of as a platform, it best thought of as an app.
- For example, you could use Instagram a form of cloud photo storage, but it's best to think of it as a social network.

How Bitcoin works
- Users run bitcoin nodes
- Users create transactions by writing a script that determines how UTXOs can be spent
- Miners conduct proof of work, taking signed transactions and building blocks. To do this they expend energy and incur cost and are therefore compensated through transaction fees and block rewards.
- Users then get the new blocks in the chain and check to see if it's valid and the canonical fork (this is called the fork choice rule)
- Miners build valid blocks not because they have to, but because they would have no reward if they did not (while still incurring costs)

How Bitcoin works part 2
- There are other interesting components in this system. First and foremost is light client verification.
- Instead of downloading all the transactions for all of time (what a full node must do), Bitcoin enabled light clients to only download block header, then they can just download the block headers, which is much smaller. Then through merkle proofs they are able to demonstrate their a UTXO was included in a block.
- Therefore, you can accept a payment even if you are not running a full Bitcoin node.

The problem with Bitcoin
- Bitcoin is an amazing application, but is not optimal. The biggest issue is that it is hard to engage in commerce with Bitcoins.
- Yes, sending BTC between addresses is relatively easy, but to have everyone set up to do this properly is hard.
- Connecting on-chain and off-chain events is a hard problem, so by increasing the number of things you can do on-chain, it increases the utility of the digital money.
- Unfortunately, it is really hard to add functionality to Bitcoin because you have to convince the entire community to adopt a hardfork with new op_codes.
- Most efforts to do this have failed.
- Problem 2: It doesn't scale.

Ethereum: Starting to modularize the blockchain stack
- Ethereum is not only an application (sending ETH), but also a platform.
- Ethereum unbundled the functionality (the application logic), from the security model.
- This enabled any developer to extend the functionality of what Ethereum could do, without coordinating to change the security model.
- But to be clear, this is not how people were thinking about things at the time.

How Ethereum differs from Bitcoin:
- Ethereum started as PoW but moved to PoS. Although there are important differences between these, they are not fundamentally different.
- Ethereum added turing completeness to transactions, enabling programmers to do anything just like they would when using a turing complete programming language to develop the core protocol by adding an op code.
- Hence the creation of a fully-fledged "Ethereum virtual machine"
- Enabled light client verification of state

The problem with Ethereum:
- Ethereum solved the first problem that Bitcoin faced, but not the second
- It doesn't scale
- As you increase the cost of running a node, the cost of verifying the chain goes up. Then light client verification becomes less effective.

