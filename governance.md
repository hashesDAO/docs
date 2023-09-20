---
order: 9
icon: people
---

# Governance

The Hashes DAO is a decentralized autonomous organization (DAO) governed by the global community of Hashes DAO NFT holders. The DAO has employed a paradigm of iterating through focused projects called "Permutations" to successively realise its vision of supporting generative art. At a high level, the governance process for a Permutation entails three phases: discussion, votes, and execution.

### Discussion

To begin with, any member of the Hashes DAO (i.e. a Hashes DAO NFT holder) can propose a Permutation to the community in the Hashes Discord, wherein a constructive discussion ensues regarding the appropriateness, goals, budget, and feasability of the project. During this ideation phase a rough plan for the Permutation is devised, a sponsor is elected (typically the original advoate of the Permuation), and often several community members commit to contribute given their expertise and skillsets.

### Votes

Following the formation of a plan, budget, and delegation of core contributors that will work on the Permuatation, two governance votes must be passed. The first is a [Snapshot](https://snapshot.org/#/thehashes.eth) vote that acts to gauge the overal community sentiment and support for the Permutation. It is important to note that the results of the Snapshot vote are non-binding. A successful Snapshot vote does not imply that the subsequent on-chain governance vote will be similarly successful; however, an unsuccessful Snapshot vote strongly implies that the on-chain governance vote will fail, and as such the Permutation might need to be either reconsidered or abandoned. 

In the event that the Snapshot vote is successful an on-chain governance proposal may then be initiated. Technically, the governance vote is made by calling the `propose` function on Hashes DAO [smart contract](https://etherscan.io/address/0xbd3af18e0b7ebb30d49b253ab00788b92604552c), which is modelled after the Compound governance smart contract. The `propose` function allows for up to ten transactions to be queued and ultimately executed if the proposal is successful. For instance, a proposal may request moving treasury funds from the DAO to a multi-signature wallet for an artist grant, such as what occured under [Permutation six](https://etherscan.io/tx/0x791b67cb01cb99c1033c6fb664572bb2d4cdb9bca27430332dfba88cfb423f50). 

In order to make an on-chain governance proposal the proposing wallet must possess at least ten DAO Hashes NFTs. DAO members may then vote on the proposal by calling the `cast vote` function either in support of or against the proposal. Once a proposal has been initiated there exists a voting window of 17280 blocks (approximately 2.4 days) within which the proposal may be voted on. It should also be noted that a quorum of 40 votes must be attained in order for the proposal to succeed. 

Finally, after a successful on-chain vote has occured, two additional transactions must be made to first `queue` the proposed transactions, and to then subsequently `execute` them. Similarly to during the voting period, the proposed transactions will remain queued and be unable to be executed for 72 hours. This series of delays and voter thresholds exists so as to mitigate any risks of attack or exploitation. After the queued delay has passed anyone may execute the proposed transaction, and the on-chain governance process has been completed!

##### To summarise, the on-chain governance process is as follows:
- An individual with 10 or more DAO NFTs calls the `propose` function on the Hashes DAO smart contract, proposing a series of on-chain transactions.
- Hashes DAO NFT holders vote by calling the `cast vote` function either in support or against the proposal.
- On-chain voting lasts for 17280 blocks (approximately 2.4 days), and a quorum of 40 votes is required to have the proposal be successful.
- Anyone may then `queue` the succesfully proposed transactions, and wait another 72 hours for the delay period to elapse.
- Finally, anyone may then `execute` the succesfully proposed transactions with a final on-chain transaction.

### Execution

After the on-chain governance process has been completed the Permutation begins in earnest, with DAO members beginning to work on the newly funded project. Leading the Permutation is the Sponsor, who has executive control over the day-to-day operations of the Permutation. More detail regarding current and former permutations can be found in the Permutations section. Finally, a more thorough treatment of the Permutation governance process is discussed at length in this excellent [article](https://medium.com/@sydneyjason/how-to-run-a-hashes-dao-permutation-2ecdb6def2a9) by Sydney Jason.