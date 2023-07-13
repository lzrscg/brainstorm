Bitcoin is a miracle.
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

