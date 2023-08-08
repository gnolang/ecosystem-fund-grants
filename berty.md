# Berty X Gno Grant Application



* **Name:** Berty Technologies
* **Project name**: Gno on Mobile

Berty: Berty specializes in mobile app development using Go code, cryptography, and peer-to-peer technology. We can help bootstrap a social networking app for NewTendermint, where our mobile client interacts with the Gno blockchain and collaborates on jointly developed contracts. This collaboration would turn Berty into Gno contract developers, making us full-stack contributors in the partnership.

Berty plans to integrate "Wesh Network" into the app architecture, resulting in a mobile app with three layers:

1. Consensus-based single source of truth over the internet.

2. Eventually consistent private group pubsub for direct messaging and real-time interactions.

3. Local (device-specific) network representation enabling pathfinding to the Gno blockchain via relays on other devices.

Our goal is to create a user-friendly and decentralized mobile app that offers a seamless experience. It would be resistant to censorship, ensuring freedom of content through Gno's consensus mechanism and a censorship-resistant network powered by Wesh Network. We strive to develop the most usable and unstoppable social networking app available.



* **Team member GitHub handles (if applicable)**: jefft0, d4ryl00, iuricmp
* **Links to Twitter, website..etc**.
    * [https://berty.tech/](https://berty.tech/) 
    * [https://wesh.network/](https://wesh.network/) 
* **The title of your grant submission** (how do you want us to remember you 😊)
    * Gno.land mobile functionality - Gno Mobile
* **Grant type** (from examples in Readme)- tinker, builder, researcher
    * Builder
* **A short description of what you are proposing **(applies to all submissions)
    * Our goal is to support Gno in creating a user-friendly and decentralized mobile app by providing a software toolkit which offers a seamless experience on mobile. We share the goal to create an app resistant to censorship, ensuring freedom of content through Gno's consensus mechanism and a censorship-resistant network powered by Wesh Network. We strive to develop the most usable and unstoppable social networking app available.
* **What is the goal or the purpose of the proposed grant?** (applies to all submissions)
    * To provide a toolkit which enables developers to deploy their Gno apps on mobile. Berty will contribute by providing the building block that Gno misses to connect React Native with Golang code (like Gno).
    * To enable Gno mobile apps to function offgrid using Wesh Network, a protocol that enables 2 main functionalities:
        * A new transport layer: transport the data - Wesh Network adds transport layer - off-grid  
        * A standalone protocol not depending on a chain to exchange live data in trusted subgroups
    * To bring mobile app capabilities to Gno and create the next killer app
* **Contributions, issues and pull requests made to Gno and Game of Realms** (links please)
    * None so far, but we can’t wait to do it :)
* **Why are you best suited/what is your background** (or team’s if applicable) (applies to all submissions)?
    * Berty is the only team (to our knowledge) that has experience with building apps with React native, Golang and Gomobile on top of P2P
    * Berty has knowledge in building GRPC protocols
    * Berty has written Wesh Network - a protocol that enables devices to communicate/talk to each other, using P2P technologies, including our contributed Bluetooth drivers.
        * This can be done in on-grid or off-grid mode
* **Milestones* and overall time frame of your proposal**
    * M0 ~ 1 month: Proof of Concept & Plan to bring Gno on Mobile
    * M1 ~ 3 months: Gno Mobile demo and foundations 
    * M2 ~ 3 to 6 months: General-Purpose Framework for Gno on Mobile  

        _*Each milestone is detailed further at the end of this document._

* **Your idea for fair funding of the proposal**
    * Start with a 3 month trial period with € 60k a month, for X developers
* **What do you and the submission bring to the Gno.land platform and community?**
    * Berty’s proposal would allow for a mobile package to be used by other Gno.land based projects to include mobile functionality in their apps. 
    * Berty would showcase the mobile functionality with a killer mobile gaming app
    * Berty has written Wesh Network - a protocol that enables devices to communicate/talk to each other, using P2P technologies, including our contributed Bluetooth drivers.
        * This can be done in on-grid or off-grid mode
    * Berty has years of experience developing, debugging and deploying Berty Messenger, an end-user P2P-enabled message app.
* **Share any referrals or other projects you work with**
    * Berty is an active contributing member of the open source community for over 5 years:
        * [Paris P2P Festival](https://p2p.paris/en/) and monthly events - Berty is a co-organiser and contributor
        * Workshops and presentations at IPFS Camp and Paris P2P festival
            * Berty presentation at IPFS Camp 2019 about Bluetooth Low Energy, libp2p on mobile [https://www.youtube.com/watch?v=p2ZAm2fAvUo](https://www.youtube.com/watch?v=p2ZAm2fAvUo) 
            * Berty presentations at IPFS Camp 2022
                * Wesh Network enables builders to create more powerful dApps [https://www.youtube.com/watch?v=PWUnvz9eiF8](https://www.youtube.com/watch?v=PWUnvz9eiF8) 
                * Gomobile toolkit support \
[https://www.youtube.com/watch?v=wZ7DrWXBHUI](https://www.youtube.com/watch?v=wZ7DrWXBHUI) 
            * Berty presentation at Paris P2P Festival 2022
                * “_Berty and Offline Communications_”: [https://www.youtube.com/watch?v=2fHHfaeT42M](https://www.youtube.com/watch?v=2fHHfaeT42M) 
                * “_Optimize libp2p on Mobile_”: [https://www.youtube.com/watch?v=1-lF8fJ9GgM](https://www.youtube.com/watch?v=1-lF8fJ9GgM) 
        * We maintain multiple open-source projects besides the Berty Messenger app: go-orbit-db, go-ipfs-log, gomobile-ipfs
    * We regularly contribute with enhancements to the other open source projects that we rely on like: go-libp2p, go-libp2p-pubsub, gomobile.

—


## Milestones Proposal - Details

**M0: Pay to Explore:  \
**One month



* Write simple contracts (e.g. escrow or other existing examples from the Gno basic contracts), designed to test upcoming mobile apps and get the Berty team knowing Gno (Gnowing)
* Join weekly meetings to understand the technical challenges for building with Gno on mobile
* Gain enough experience to make an educated evaluation on the M1 and M2 requirements including Gno apps using _[gomobile](https://github.com/golang/go/wiki/Mobile)_ with minimal impact to Gno devs
* End results and deliverables at the end of M0: 
    1. POC: adapting an existing Gno example app that proves we can run Gno code on mobile, and/or identify challenges to fix in M1
    2. a detailed technical plan to bring Gno apps to mobile during M1 and M2.

**M1: Pay to build: Gno Mobile demo and foundations**

	-> 3 months+ (reevaluate on 3rd month)



* Write a mobile app demo connecting to Gno testnets and allowing to interact with contracts
* Implement simple CI/CD to make the development and reviews of the app smoother 
* Participate in meetings with NT product teams to continuously deepen understanding on the Gno direction and strategy
* Organize a workshop/meetup/demo to encourage people to explore Gno on mobile
* Participate in a few meetings required by NT product team to plan the upcoming social app
* Write the technical specs for the Gno on mobile general-purpose, ready to use version + a blogpost
* End result: an open-source mobile app with basic CI/CD, interacting with a Gno testnet + a blogpost

**M2: General-Purpose Framework for Gno on Mobile (gno.mobile)**

	-> ~3-6m - delivering the entire scope may require additional hiring 



* Explore with existing partners (Teritori, Onbloc) to see how much they can run mobile apps and how the demo enhances their projects
* Example of standalone app running Gno & Berty’s Wesh Network, that showcase how Gno can function offgrid (peer2peer) 
* Documentation on how to use the framework and API 
* Mini demos / examples to help devs getting started with the framework (HelloWorld app).
* Participate in meetings as required by NT product team to plan the upcoming Social App V0
* End result: Deliver a package/lib/skeleton framework that makes it easier for developers to empower their Gno apps by deploying on mobile with Wesh Network resilient, off-grid communication features.
    * Example idea: Gnoland Space Explorer mobile - Specialized App

**M3: Help NT on Social App V0**

	-> estimation: N/A



* Depending on product definition w/ NT
* Plan is to help the NT team to build and run the app
