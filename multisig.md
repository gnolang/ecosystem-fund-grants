# GnoLand Proposal - Multisig 


## TL;DR/Short Description:

**What We'll Build:** Multisig infrastructure on GnoLand

**Cool Features:** Easy account creation, asset management, custom message handling, and more.

**Grant:** We're asking for $40,000. No upfront cash needed.

**When Will It Be Done?:** Roughly 2 months.

## Multisig

Multisig, short for multi-signature, is more than just a vital tool in the blockchain world; it’s a requirement. 

Used by virtually everyone, from individual users to large organizations, multisig adds an essential layer of security by requiring multiple approvals to execute a transaction. Its universal application and undeniable importance make it a standard feature across various platforms and tokens.



## Our proposal

We, at blockdudes, propose to build a multisig infrastructure on GnoLand. 

Our vision is simple: make it easy for anyone to create and manage their multisig account without needing magical powers to write complex smart contracts.


Our solution takes inspiration from Safe, an esteemed product built on Ethereum. But we aim to go a step further by crafting an even better and more user-friendly experience.

Features of the solution:
- **User-Friendly Multisig Account Creation**:
	- Anyone can easily create multisig accounts using our frontend interface.
	- No need for in-depth knowledge of smart contracts.
	- A guided step-by-step process ensures accessibility for all users.
- **Token Management**:
	- Send and receive both Fungible and Non-Fungible Tokens effortlessly.
	- Full support for various token types, enhancing the platform’s versatility.
- **Custom Message Handling**:
	- Users can propose and execute custom messages.
	- Facilitates complex, multi-step transactions.
- **Dynamic Ownership Agreement Management**:
	- Directly update ownership agreements using the frontend.
	- Flexibility to adapt to changing needs and requirements.
- **DAPPs Support**:
	- Functionality to easy integrate Gnoland Ecosystem DAPPs easily into the frontend


### Main components of the solution:

#### 1.  Smart Contracts
The Smart Contracts form the backbone of our multisig solution, acting as the brain that governs every aspect of the system. 

The architecture of our smart contracts is designed with thoughtful consideration of existing successful models. It’s influenced by the cw3-flexible-multisig solution of Cosmwasm, Here’s a closer look at how they’ll be constructed:
- **Multisig Contract**:
	- **Purpose**: It’s the core of the entire multisig system, responsible for holding all the assets and managing ownership logic.
	- **Security**: Implements rigorous security protocols to ensure that transactions are processed and authorized correctly.
	- **Flexibility**: Designed to allow diverse multisig structures, making it adaptable to different use cases and needs.
- **Group Contract**:
	- **Purpose**: Acts as a dedicated storage hub for multisig owners and their corresponding weights, separate from the core logic.
	- **Interoperability**: Designed to interact seamlessly with the Multisig Contract
	- **Why Separate?**: Separating the Group Contract from the Multisig Contract adds a layer of flexibility in access control. This design allows us to use different access controls for owner storage than for multisig functions, enhancing customization and security. Although rare, there may be scenarios where this modularity is beneficial. Furthermore, this separation aligns with the cw3 architecture influence, maintaining a coherent design approach.
- **Factory Contract**:
	- **Purpose**: Simplifies the initialization process by deploying all the required starting contracts - Multisig and Group Contract and initializing any variables.
	- **User Experience**: Tailored to enhance the overall user journey by batching multisig launch transactions into one, saving time and resources.

 #### 2. Frontend Interface
The Frontend Interface is where the magic happens for the everyday user, without them ever needing to see the complex machinery behind the scenes. Here’s how we plan to design it:
- **Ease of Use**:
	- Intuitive layout and design for simple navigation.
	- Step-by-step guidance for creating, managing, and updating multisig accounts.
	- Responsive design across various devices.
- **Multisig Account Management**:
	- Tools to create and manage multisig accounts, including adding/removing signatories.
	- Visual overviews of accounts, transactions, and pending approvals.
- **Asset and Custom Message Handling**:
	- Integrated interface for sending/receiving Fungible and Non-Fungible Assets
	- User-friendly tools for proposing and executing custom messages.
	- Pre-designed templates and customization options for messages.
	- Support to integrate the favorite 
- **Ownership Agreement Adjustment**:
	- In-app tools to update ownership agreements.
	- Transparent display of current and proposed ownership structures.
- **Integration and Compatibility**:
	- Seamless workability with popular wallet solutions and existing GnoLand services.
	- Regular updates to ensure alignment with evolving blockchain technologies.
 
 
 
## Basic functioning of the contracts


### Create Multisig
![create multisig](https://github.com/blockdudes/ecosystem-fund-grants/assets/72156537/49482250-6ecf-4887-9afb-87668911faf1)


### Use Multisig
![multisig working](https://github.com/blockdudes/ecosystem-fund-grants/assets/72156537/2d795588-e65b-4237-868e-c6277ec9d4a9)


## Grant Request

We request a total grant of $40,000.

This grant will amount will be used to fund the development of the Multi-sig wallet - Smart Contracts, Frontend and other tooling required.



### Milestones and timeline

**As this is the first project we are developing with Gnoland to build the trust we won’t be asking for any upfront money or even no money until the product is fully complete! No risk for you**

1. Milestone 1 - After the project is complete and launched on testnet


### Project Deliverables
| No. | Scope                                 | Deliverables                             | Time     |
|-----|--------------------------------------|------------------------------------------|----------|
| 1   | Frontend Designs and Wireframes       | Design for the Frontend Interface        | 5 Days   |
| 2   | Smart Contract Development           | Complete Smart Contracts with tests      | 25 Days  |
| 3   | Frontend Development                 | Frontend with Smart Contracts Integrated | 20 Days  |
| 4   | Final touches, internal auditing and Testnet Launch     | Testnet Launch                           | 10 Days  |


Expected ETA = ~2 Months

## Security

The project involves developing smart contracts even if they are not very big and complex and they must be properly secured.

We will run a proper internal audit to ensure the security.

But for ensuring proper security we might require external audit from GnoLand Team or support for audits from external team - will need to discuss this

### Version 1

There are many more features that could be included in a multi-sig app like offchain signatures, recovery mechanism, gas abstraction, fraud monitoring, etc.

But these extra features won’t be included in the first version of the DAPP, the main motive of the first version will be to fulfil all the main requirements for a multi-sig account and later add more features to it as we progress and get input from the customers 

In this version all the signatures will be onchain, and will add offchain signatures in a later version


## Business Model and Maintenance: Our Commitment to Sustainability

Maintenance is very important for every product, especially for products like multi-sig which will be used by almost every project and where constant updates, security improvements and new features are important

And we recognize that maintenance is not a one-off task but a continuous responsibility.

**We’re not building a product to take the grant and vanish. We’re in this for the long haul.**

We also don’t want to continually ask for support grants, adding financial stress to GnoLand. We believe that a successful product needs to sustain itself without becoming a burden. That’s why we’ve crafted business models to support the ongoing development and maintenance of our multisig solution:

1. **Frontend Utilization**: Our frontend isn’t just a user interface; it’s a hub where the eyes of large fund owners meet. It’s valuable real estate where featured DAPPs can immediately reach a broad and influential audience. By efficiently utilizing our frontend, we can generate funds to support ongoing maintenance and development.
   
2. **Customized Services**: With big funds comes big responsibility, and we can offer tailored services to those managing substantial assets. From customized analytics to specialized fund management, our services can cater to a variety of unique needs.

These business models are just the beginning. As we evolve and grow, more opportunities will emerge to make this project not only viable but fully sustainable.

**In essence, you don’t have to worry about this project’s future. We’re committed to building, nurturing, and sustaining it. We’re here to BUIDL!**


## Value Add for the GnoLand Ecosystem

We have already seen how important this is in other blockchains and used by almost every project.

It is far from being a mere option; it’s an essential component in the modern blockchain space. Here’s why developing multisig on GnoLand is so vital:
- **Indispensable for DAOs**:
	- **Security**: Without multisig, the security of entire projects can rest in a single person’s hands. Multisig disperses this risk among multiple owners, ensuring no single point of failure.
	- **Democratic Control**: DAOs operate on collective decision-making. Multisig mirrors this philosophy by requiring consensus among multiple parties for transactions. It’s not just a security feature; it’s a governance tool.
- **Enhanced Collaboration**:
	- **Team Management**: Multisig facilitates collaboration within projects, allowing shared control over resources. It’s like a digital boardroom table, where decisions are made together.
- **Alignment with Best Practices**:
	- **Global Adoption**: Most successful blockchain projects and platforms recognize multisig as a standard practice for safeguarding assets. It’s not just a trend; it’s a well-established industry norm.
- **Multiple Safeguards**:
	- **Layered Security**: Multisig offers layers of security. If one key is compromised, the others act as safeguards, keeping assets and control intact.
	- **Flexibility**: It’s adaptable to different needs, providing varying levels of control and security based on the unique requirements of each project or organization.
### Broad Impact:
- **Projects and Developers**: Multisig is almost synonymous with secure and democratic control, essential for any serious blockchain project.
- **Enterprises and Organizations**: Beyond individual projects, businesses can leverage multisig for more transparent and secure corporate governance.
- **Individual Users**: Even personal users can benefit from the added security and collaboration opportunities that multisig offers.

By building multisig infrastructure on GnoLand, we’re laying down a foundational building block for a secure, collaborative, and compliant ecosystem.

It’s not just about following a successful path paved by others; it’s about recognizing what’s essential for growth and innovation in the blockchain space.

In a world where digital assets are becoming increasingly valuable and targeted, multisig isn’t a luxury; it’s a necessity. 



## **Team:**

Our team at [Blockdudes](https://blockdudes.com/) has a proven track record in the blockchain space. We have developed and contributed to a multitude of projects, enhancing the infrastructure and applications of various chains and platforms.

**Amrit Kumar Jain - CEO and Founder, Project Lead**

GitHub: [amritkumarj](https://github.com/amritkumarj)

LinkedIn: [Amrit Kumar Jain](https://www.linkedin.com/in/amritj/)

Amrit Kumar Jain, the founder of [Blockdudes](https://blockdudes.com/) and the lead for this project, brings a wealth of experience and a wide network to the project. I have been working in the blockchain industry for quite a while now and had established strong connections within the industry, including notable figures such as Vitalik Buterin, the founder of Ethereum.

Team Members

Four other members of the [Blockdudes](https://blockdudes.com/) team will contribute to this project, bringing their diverse skills and experience. Their roles include frontend developers, designers, and blockchain developers who will collaboratively ensure the project’s success.

As a collective, the [Blockdudes](https://blockdudes.com/) team has successfully executed a range of significant projects, a few of which are:

1. **Decentralized Bridge:** Worked with Vitalik Buterin to develop a decentralized layer 2 bridge.
2. **Mask Network:** Integrated new features into the Mask Network browser extension.
3. **Unstoppable Domains:** Assisted in integrating their service into various DeFi projects like Balancer, Enkrypt,zksync wallets, etc.
4. **Messari:** We have worked with Messari on multiple projects, including developing several DeFi subgraphs that can be viewed at [subgraphs.messari.io](http://subgraphs.messari.io/), this website is also built by us. We are currently working with them on building a large data project like Dune tables for multiple chains from scratch, which includes all Cosmos Chains, Filecoin, etc.
5. **Reserve:** Developed DeFi collateral plugins.
6. **Verge:** Developed ISO 20022 Application for Verge. Helping them integrate Smart Contracts in their chain
7. **Vetoken Finance:** Constructed the project’s website, built smart contracts and data graphs.
8. **Osmosis:** Collaborating to build DeFi Vaults and strategies.

These examples represent a fraction of our work. We’ve completed several other projects, and our collective experience and success will be instrumental in the development and success of our proposed project

## **Team Long-Term Vision**

Our long-term vision goes beyond this single project.

We aim to build far more products and help in building the Gnoland ecosystem.

Our goal will be attract to more TVL to GnoLand, enhance its ecosystem, and, importantly, to improve the user experience!



## Info

Name - [Blockdudes](https://blockdudes.com)

Project Name - TBD

Email - amrit@blockdudes.com

Grant type - Builder
