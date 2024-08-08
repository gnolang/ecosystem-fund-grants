
![image](https://github.com/gnolang/ecosystem-fund-grants/assets/117160070/47c75689-705e-46f7-89c0-8adf8cbe6bd0)


# Gno.land Grants Program

The mission of the gno.land Grants Program is to encourage and support the growth of the Gnolang contributor community, and build out the usability of the platform and smart contract library. The program will award grants and financial contributions to individuals building projects, dApps, tooling, infrastructure, products, and smart contract libraries in Gno.land.

As gno.land is built using a new consensus mechanism, Proof of Contribution, and is still in the initial stages, this program is a way to incentivize and fund individuals and teams to use the new mechanism. The allocated amount of each grant will reflect the scope and ambition of the proposal and its priority within the Gno.land platform.


## How to get involved

We're on the lookout for passionate contributors who are interested in building new projects, dApps, tooling, infrastructure, or smart contract libraries in Gno.land. If you're participating in our ongoing incentivized Game of Realms competition or contributing to PRs and issues on the Gno.land repos and you have an idea for a new project, be sure to apply!

## What kind of contributors are we looking for?

Individual contributors and teams interested in building and developing on gno.land

## What kind of proposals are we looking for?

**Applications (Gno dApps)**

We want to support interesting smart contracts written in Gno that will either be useful as libraries, or be viral in adoption. Games, Defi applications don’t already exist, but more interestingly social communication and coordination applications. The initial expected deliverables: First an English written draft spec, before any implementation. 

* Improvements to the demo/board application to make it actually useful.
* General applications that can be used for proof-of-person.
* Name registration contracts, etc. 
* Surprise us with the next killer app
* Build, test, and launch a suite of Gno.land apps for the community, focusing on diverse use cases and industries such as DeFi, gaming, supply chain management, and social communication and coordination applications. 
* These apps should integrate seamlessly with existing Gno.land infrastructure, encourage user interaction, and promote the adoption of Gno.land services


**Products** 

* Develop advanced project management software tailored to the needs of Gno.land developers and teams, with features such as task tracking, collaboration tools, and integrated Gno.land services.
* Create comprehensive documentation, including guides, tutorials, and API references, to help users understand and utilize Gno.land's features and services more effectively.
* Design and implement an event system for Gno.land contracts, allowing for real-time monitoring, analysis, and auditing of contract-related events.

**GnoVM**
##### Expected Deliverables (one of)
* Bug fixes to the GnoVM
* Specification for persistent state garbage collection. The Gno smart contracting platform can create cycles in persistent state that cannot be garbage collected by the Go runtime (which Gno piggy backs on for in-transaction garbage collection). We want to consider both in-realm incremental garbage collection as well as inter-realm global garbage collection as two separate modules to explore in parallel. See the upcoming gno.land whitepaper for more details.
* Specification for bonded persistent state garbage collection. In addition to the above, we want to consider a specification for bonded garbage collection of persistent state that may cross realm boundaries. The general idea is that anyone can put up a bond and specify any object ID, from which point this garbage collector will begin iterating over the reachable objects to determine whether the object ID is indeed part of a cycle that should be garbage collected. If during this computation it turns out that it should *not* be garbage collected, then the bond should be burned, and have no effect. This garbage collector must also be incremental and deterministic, so that all the validators can run it in sync, and incrementally per block. 
* Gno code fuzzing tool that can generate fuzzed Gno code, for comparing behavior against the Go compiler. This is expected to be difficult, because it should be able to generate arbitrary code that also happens to terminate. Another thing to consider is that map iteration in Go is non-deterministic, so the fuzzer should have two modes; one that can generate Gno code that also is also deterministic in Go, and another mode that can generate Gno code that includes things like map iteration which is not compared against the Go result, but is only used for running in GNO to check for consistency and panics.
* Specifications for improvements to the Gno language to help with garbage collection, reference counting, merkle hash computation, and general safety of smart contracts written in Gno. 

**Interoperability and Integration**

* Implement cross-chain compatibility and interoperability, allowing Gno.land to connect and interact with other blockchain networks, thus expanding its potential user base and increasing its overall reach.
* Develop a powerful integrated development environment (IDE) specifically for Gno.land developers, with features like code completion, debugging tools, and seamless integration with Gno.land services.
* Create a framework to make it easy and powerful to build dApps with a standalone frontend that uses Gno contracts as the backend
* Add Gno support on existing tools (editors, scripts, CI/CD, frameworks, etc).

**Infrastructure, DevX, and Quality**
* Develop comprehensive GitHub and AWS integration for gno.land, including streamlined deployment processes, continuous integration and delivery pipelines, and monitoring tools.
* Create Helm charts for easy deployment and management of Gno clusters, enabling users to quickly set up and scale their Gno infrastructure.
* Improve overall quality by working on the testing pipeline and improve CI/CD.
* Improve validator and developer experience, especially when developing locally.
* You can select an idea from there too: https://github.com/gnolang/hackerspace/issues

## How to apply

To start the process, you'll need to:
1. Fork this repo
2. Create a new `.md` file with your project’s name under the `grants` folder
3. Outline your proposal in that file as outlined in the grant application template
4. Create a Pull Request

After applying with a complete application, the grant team will review it. If the submission meets the initial criteria, a grant team member will be in touch to set up a review call to ask questions, assess the deliverables, and discuss it in more detail. Keep in mind Gno.land’s mission is to launch and support Proof of Contribution, so contributing to open pull requests, challenges and topics is important until we are completely on-chain.

Following the submission and informational session, the grant team will review the submission and follow up with more questions, status updates, and general due diligence to move to the final round. The goal is to collect as much information and feedback for the review committee to make the process as streamlined, transparent and thorough as possible for everyone.

If the grant team finds it meets the requirements and brings added value to the gno.land ecosystem, the submission will be passed along to the review committee. The review committee will meet quarterly to review submission, and in exceptional cases, maybe sooner.


## Follow the journey

You can check out our grant recipients journey's on their projects and work progress on the Hackerspace repo: https://github.com/gnolang/hackerspace/issues

## Conclusion

We want the grant process to be as transparent and easy as possible, which is why we will conduct the majority of interaction, feedback loops, and updates on GitHub.

## Application template

* Name
* GitHub handle
* Email 
* Links to Twitter, website..etc.
* The title of your grant submission (how do you want us to remember you 😊)
* Potential focus for the grant based on your expertise  
* A short description of what you are proposing (applies to all submissions)
* What is the goal or the purpose of the proposed grant? (applies to all submissions)
* Contributions, issues and pull requests made to Gno and Game of Realms (links please)
* Why are you best suited/what is your background for the team to review your profile
* Your idea for fair funding of the proposal
* What do you and the submission bring to the Gno.land platform and community?
* Share any referrals or other projects you work with, and examples where you've already started contributing to the project!


You can also email us at hello@tendermint.com with questions or if you've submitted and want to let us know!


