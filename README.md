# daochem
**DAOchem** is a solution in which on- and off-chain governance data sources react to produce a holistic view of DAO governance. We integrate data on **smart contract parameters**, **voting activity**, **Twitter activity**, and **contributor sentiment** to help DAO creators and contributors understand the governance landscape.

## Where are we getting the data?
### New datasets
#### Governance-related smart contract parameters
DAOs that have an on-chain component to their governance process often deploy their smart contracts through a platform like Arargon or DAOHaus. In these cases, the contract is created by the platform's factory contract. We are accessing the entire transaction history of these factory contracts using [TrueBlocks](https://trueblocks.io/) and an archive node (generously provided by [ArchiveNode.io](https://archivenode.io/), to pull out the parameters set at the time of deployment for each set of DAO governance smart contracts.
#### Twitter engagement with governance-related tweets
Twitter is a common way for a DAO to engage with its membership. We are using the Twitter API to acquire the follower counts and the contents and engagement of up to the 200 most recent tweets for DAOs with Twitter accounts. From these, we select those related to governance (based on keyword searchs) to guage how frequently the DAO communicates about its governance process and how engaged the DAO's followers are with these.
#### Contributor sentiment survey
Quantitative data on DAO governance is useful, but ignores an important component of a DAO's operations: its contributors. Similar to how GlassDoor provides some context about what it's like to actually work at a company, we are deploying a short survey to understand how DAO contributors feel about, for example, whether the governance process is legitimate, or whether their contribution is valued.
### Sourced datasets
#### DeepDAO
[DeepDAO](https://archivenode.io/) generously provided us with a mapping of DAOs to their governance-related addresses, which we are using for data linking.
#### Boardroom
Through the [Boardroom](https://www.boardroom.info/) API, we obtained the proposal creation and voting activity of DAOs that used an on-chain voting mechanism or Snapshot. We also used this to assign categories to DAOs.
#### DAOHQ
We referenced [DAOHQ](https://www.daohq.co/) to assign categories to DAOs.
