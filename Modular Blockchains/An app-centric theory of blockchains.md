In all honesty, I'm mostly a frontend dev—not a blockchain theorist. I like making apps. And I believe that blockchains can help make apps far better than they are today.

Blockchain theorists should be obsessing over app developers in the same way that Amazon obsesses over customers. Customers want low prices, and app developers want... well... hmmm...

What do they want? Let's dive in.

# Methodology
Since I am not a blockchain theorist, I will be forced to work from first-principles. I will ask myself, what do I believe to be fundamentally true about the world? Then, I will tie this to observations about blockchain technology. 

Next, I will use these observations as a basis for a plausible narrative. This narrative ought to be judged over time, based on whether or not people who believe it are able to take actionable insight from it that gives them a competitive advantage over those who do not.

# First principles

## Metaphors are dangerous
This isn't so much a principle, as it is a word of caution. Don't hold on to your metaphors.

Is Bitcoin "electronic cash"? Is Ethereum a "world computer"? Is blockchain technology "web 3"? Maybe this is a useful way of framing these systems. But, each one is defined by very specific sets of code. And this code is contextualized by the physical world that surrounds us all. *That* truly defines how these systems will behave, not the mental models we use to reason about them.

It is entirely possible that there are better, more adaptive, was of thinking about these things.

## Coordination does not scale
Coordinating between two people is hard enough. As the number of participants in any system grows, coordination costs increase exponentially. This is often referred to as Brooks' Law.
![[Pasted image 20230620150145.png]]

*At risk of venturing out of my depth, I like to think of adding people as increasing entropy to the system. The number of microstate configurations leading to "bad" macrostates increases as a percentage of total possible microstates.*

# Observations

## Consensus is not a good metaphor for blockchains
There is a common narrative that blockchains allow global consensus on data and state. There is a good reason to believe this. After all, a lot of the ideas behind blockchain technology come from [research into consensus](https://en.wikipedia.org/wiki/Byzantine_fault). And isn't that what Proof-of-Work and Proof-of-Stake do? Not exactly.

Consensus is a form of coordination—and coordination cannot not scale globally. 