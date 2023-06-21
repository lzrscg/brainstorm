If I want to send you some ETH, first I will ask for your address. In order to provide this to me, you must download a wallet, set it up, and copy the address.

This works well when it is a one-time thing. Unfortunately, it can be a huge pain in a multi-chain, modular world.

One token is on one rollup. An NFT is on another one. Do you really need to create a new wallet every time you interact with a new protocol? There ought to be a better way.

# The ideal UX
1. The user registers a name, like ENS. This name should ideally be an NFT itself, and therefore transferrable and collectable.
2. Instead of asking for a wallet address on the destination chain, senders can transfer assets *to the name*. Here is how this would work technically.
	1. Check if an address already exists for this name on this chain. If so, the name resolves to the existing address and the process is complete. If not, continue.
	2. A new address is created on the destination chain and associated with the recipients name. Then, the name is resolved to this new address and the process is complete.
	   - Since there is no guaranteed protection against replay attacks across all rollups, it is best to have a unique address for each rollup.
	   - The technical details will be discussed below, but securely creating a new address on-demand is non-trivial. The short explanation is that it would utilize MPC.
3. Users can also claim vanity QR codes for their addresses via generative AI. Perhaps there is an opportunity to make these NFTs as well (although we wouldn't want to overdo the NFT thing).
# How to generate new addresses

