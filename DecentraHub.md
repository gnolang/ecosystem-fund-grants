## Name
- DecentraHub

## Project name (if applicable)
- DecentraHub

## Team member GitHub handles (if applicable)
- 0xtekgrinder - https://github.com/0xtekgrinder

## Email
- 0xtekgrinder@protonmail.com

## Links to Twitter, website..etc.
- N/A

## The title of your grant submission (how do you want us to remember you 😊)
- Gnoland Grants Program Application by 0xtekgrinder

## Grant type (from examples in Readme)- tinker, builder, researcher
- Builder

## A short description of what you are proposing (applies to all submissions)

DecentraHub is decentralized application which enable users to manage and participate into the life of DAOs.

There are two types of users in DecentraHub:

- DAO managers: they can create DAOs and manage them. Meaning they can add or remove members, set the rules to be a part of the DAO (can be the holders of an ERC20), set the rules of who can create a proposal (a set list of addresses or a minimum of ERC20 hold) and manage other possible such as on chain voting or off chain voting, execution, quorum, minimum proposal duration ...etc.
- DAO members: they can participate in the DAO by creating proposals and voting on proposals.

It will works with multiple parts:
- A frontend to view the difference DAOs and participate / manage them
- An indexer to index all the tokens transfer to be able to know the votes of each addressess
- A smart contract to let users delegate their voting power to another address
- A smart contract to store core data of DAOs
- A backend to enable offchain interactions

The idea is to create an accessible application with the best user experience possible. It means that all the steps that can be done offchain will be done offchain to avoid friction of gas fees. The user will only have to pay for gas fees when he will create DAOs or delegate his voting power which are some sensitive interactions that needs to be public and provable.

Another big part will be the fact that every DAOs creator will be able to create his own strategy to compute the voting power of the participants based on his needs.

## What is the goal or the purpose of the proposed grant? (applies to all submissions)

The grant should support the complete porting of the game to the Gno platform, including backend and frontend.

## Contributions, issues and pull requests made to Gno and Game of Realms (links please)

- [feat: ability to ignore lint diagnostics in realms (ONGOING)](https://github.com/gnolang/gno/pull/1450)

## Why are you best suited/what is your background (or team’s if applicable) (applies to all submissions)?

As a seasoned smart contract engineer with a primary background in Solidity, I've amassed valuable experience within the realm of DeFi and have actively contributed to various DAOs. My involvement helps me understand the needs that comes to this new type of organisation. Additionally, I bring extensive expertise in backend development, particularly in the more recent domain of blockchain development, where I've adeptly handled aspects such as RPC load balancing. Drawing on my comprehensive skill set, I am confident in my ability to propel this project to technical excellence.

## Milestones and overall time frame of your proposal
Milestones are per the project's roadmap and will be updated as the project progresses.

### Milestone 1: Indexer and Smart Contracts **22 days**

1. Indexer **12 days**
    - [ ] Store blocks in a SQL database
    - [ ] Retrieve the token transfers of each transaction ans store them in a SQL database
    - [ ] Handle the case a block is reorged (soft fork / hard fork)
    - [ ] Handle the case a block is wrong (revalidate the block data and hashs)
    - [ ] Retrieve the creation of DAOs and store them in a SQL database
    - [ ] Ability to catch up with the current block
    - [ ] Create a Dockerfile to deploy the indexer on a server
    - [ ] Create a documentation on how to use the indexer and how it works

2. Smart Contracts **10 days**
    - [ ] Create a DAO smart contract with a few functions mainly to set core DAO settings
    - [ ] Create a Proxy Minimal Factory to create a new DAO smart contract
    - [ ] Create the Delegation smart contract which has the ability for a user to delegate his voting power to another address in a DAO
    - [ ] Test everything on a testnet

### Milestone 2: Frontend and Backend **35 days**

1. Frontend **20 days**
    - [ ] Create a landing page for the whole application
    - [ ] Create a page to view a DAO and its proposals
    - [ ] Create a page to access settings of a DAO
    - [ ] Create a page to create a DAO in a multi step process selecting the strategy to compute the voting power ...
    - [ ] Create a page to delegate voting power
    - [ ] Create a page to create a proposal
    - [ ] Create a page to browse the DAOs
    - [ ] Create a page to view a proposal with the ability to vote on it and see the votes
    - [ ] Create a Dockerfile to deploy the frontend on a server
    - [ ] Create a documentation on how to use the frontend and how it works with tutorials

2. Backend **15 days**
    - [ ] Create a REST API to interact with the frontend
       - [ ] Create a vote based on the signature route
       - [ ] Create a proposal based on the signature route
       - [ ] Create a route to get the proposals of a DAO
       - [ ] Create a route to get the votes of a proposal
       - [ ] Create a route to get the DAOs
    - [ ] Create a open api documentation of each endpoints
    - [ ] Create a Dockerfile to deploy the backend on a server

### Milestone 3: Multisig integration **5 days**

- [ ] Add as signing option the possibility to sign with a multisig wallet
- [ ] The multisig wallet should be able to create a proposal and vote on a proposal

## Your idea for fair funding of the proposal

The total grant request based on a daily rate of 450 is 27900 USD.

On top of it, I will request 200$ per month for the required cloud infrastructure which needs a persistent server to run the indexer and the backend.

The payment can be split 75/25 fiat and ATOM and done monthly regarding on the milestones achieved.

## What do you and the submission bring to the Gno.land platform and community?

All the code will be open source so first a pretty complete indexer will be available to anyone who wants to index events in GNO land.
On top of that, the DecentraHub application will be a great showcase of the Gno platform capabilities and will be a great tool for the community to manage and participate in DAOs.

## Share any referrals or other projects you work with

[Starton](https://www.starton.com/)
[InterPlanetaryCloud](https://github.com/PoCInnovation/InterPlanetaryCloud)
[Tholgar](https://github.com/astrodevs-labs/tholgar)
[Osmium](https://github.com/astrodevs-labs/osmium)

