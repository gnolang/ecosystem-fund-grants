# Gno Grant#2 GnoSocial

# Berty X Gno Grant #2 Application

- **Name:** Berty Technologies
- **Project name**: GnoSocial

Berty Technologies is a French NGO with a mission to bring unstoppable and uncensorable communication tools to web3 application builders and the world. Our flagship product is Wesh Network, an open-source decentralized communication protocol designed to enable resilient communication even in off-the grid environments. Berty Messenger is a decentralized communication tool and the first mobile application that uses Wesh Network.

Thanks to a first successful grant received from New Tendermint we were able to build the GnoMobile framework that enables developers to create mobile applications using Gno. The code repository is found here: [https://github.com/gnolang/gnomobile](https://github.com/gnolang/gnomobile).

- **Team member GitHub handles**: jefft0, d4ryl00, iuricmp, costinberty
- **Links to Twitter, website..etc**.
    - [https://berty.tech/](https://berty.tech/)
    - [https://wesh.network/](https://wesh.network/)
- **The title of your grant submission** (how do you want us to remember you 😊)
    - *GnoSocial, a test bed for experimenting with web3 Social App features integrations*
- **Grant type** (from examples in Readme)- tinker, builder, researcher
    - Builder
- **A short description of what you are proposing** (applies to all submissions)
    - The objective of this grant proposal is to bootstrap GnoSocial, a social media application that will be used as a bed for builders to experiment with integrating social media features with web3 technologies and innovations (i.e. integration with DAO collaboration features).
- **What is the goal or the purpose of the proposed grant?** (applies to all submissions)

The goal is to create a test-bed for building decentralized social media type of applications and experimenting with smart contract integrations around social media features.

- The first version of GnoSocial will include the basic Twitter-like features like: post, react, notification, mentions, etc. GnoSocial will be built for mobile using the GnoMobile framework, but we will also include a read-only web version of the application.
- Additionally and perhaps the most interesting part of this grant proposal are the R&D parts for which we will also collaborate with other players of the Gno ecosystem. Specifically we will try to:
    - integrate a **DAO moderation feature** inspired from the work of **Teritori**.
    - We will also build a **notification system** using the “notifs core” code that is under development by the Gno core team. For this one we might collaborate with **Onbloc**.
    - Finally, we plan to study the **scalability of smart contracts** and the potential solutions involving **Merkel trees.**
- **Contributions, issues and pull requests made to Gno and Game of Realms** (links please)
    - **Blogpost** “[GnoMobile, a Framework for Building Gno Mobile Apps](https://test3.gno.land/r/gnoland/blog:p/gnomobile)”
    - [PR1034](https://github.com/gnolang/gno/pull/1034) Fix demo/boards/README, fix typos and change to a local node - MERGED
    - [Issue 1031](https://github.com/gnolang/gno/issues/1031)Some READMEs refer to an old version of the quickstart guide - RESOLVED
    - [PR1213](https://github.com/gnolang/gno/pull/1213) In Amino, use ToLowerSnakeCase for Protobuf field names - 1 APPROVAL
    - [PR1235](https://github.com/gnolang/gno/pull/1235) In amino.pkg, add optional WithComments, use them in GenerateProto3MessagePartial - REVIEWING
    - [PR1289](https://github.com/gnolang/gno/pull/1289) fix: Error string in decryptPrivKey. Use errors.As in IsErrWrongPassword - MERGED
    - [PR1031](https://github.com/gnolang/gno/pull/1301) fix: In TestGnoDoc, fix expected output for "doc", "avl". (Mentioned by [https://github.com/gnolang/gno/pull/1306](https://github.com/gnolang/gno/pull/1306) ) - MERGED
    - [PR1313](https://github.com/gnolang/gno/pull/1313) Add Keybase HasByNameOrAddress, HasByName and HasByAddress - MERGED
    - [PR1316](https://github.com/gnolang/gno/pull/1316) fix: In Keybase GetByAddress, change generic error to NewErrKeyNotFound - MERGED
    - [Issue 1070](https://github.com/gnolang/gno/issues/1070) "Gas used" is different than number of coins subtracted. (Mentioned by [https://github.com/gnolang/gno/issues/1067](https://github.com/gnolang/gno/issues/1067) and [https://github.com/gnolang/gno/issues/1106](https://github.com/gnolang/gno/issues/1106) ) - DISCUSSING
- **Why are you best suited/what is your background** (or team’s if applicable) (applies to all submissions)?
    - Berty has already completed a successful first grant with Gno and has delivered the first version of the GnoMobile framework.
    - Berty is the only team (to our knowledge) that has experience with building apps with React native, Golang and Gomobile on top of P2P
    - Berty has knowledge in building GRPC protocols
    - Berty has written Wesh Network - a protocol that enables devices to communicate/talk to each other, using P2P technologies, including our contributed Bluetooth drivers.
- **Milestones* and overall time frame of your proposal**
    - Our roadmap is divided into 3 main sub-projects:
        - P1, months 1-5: build the GnoSocial v1 with basic features of add/delete account, post, react, mention, notifications.
        - P2, months 2-6: R&D study - Scalability of smart contract, including the potential use of a Merkel tree as a solution
        - P3, months 2-6: R&D study - Integrate a DAO moderation feature into the GnoSocial app
    - Deliverables:
        - Beyond the actual code of GnoSocial, at the end of each of the 3 sub-projects we will organize a demo or another appropriate means of disseminating the results of our work.
        - We will also make intermediary demos when it makes sense and we also plan to write at least one blogpost related to this grant.
        - If it will make sense and if we will have the resources, we will organize workshops to familiarize the interested partners with the results that will emerge from this grant.

[https://lh7-us.googleusercontent.com/2nk9i42MBN9UFZLq3eGE4vTWUaaQcDp_ylvirrR936WAvg-529z35Mv5RDXo2Ypa5ugzcMzouzGIg9QviIxQx2rnpqq--OAT9OUZtIAjC8ti32zrOumfAHdnkQjICXAExCCit7lWs8U_ZvmOvwNV_Q](https://lh7-us.googleusercontent.com/2nk9i42MBN9UFZLq3eGE4vTWUaaQcDp_ylvirrR936WAvg-529z35Mv5RDXo2Ypa5ugzcMzouzGIg9QviIxQx2rnpqq--OAT9OUZtIAjC8ti32zrOumfAHdnkQjICXAExCCit7lWs8U_ZvmOvwNV_Q)

- **Your idea for fair funding of the proposal**
    - 6 months of continuous funding, from the beginning of December 2023 until the end of May 2024.
- **What do you and the submission bring to the Gno.land platform and community?**
    - GnoSocial will be the first step in building web3 alternatives to popular web2 social media applications.
    - The R&D parts of our grant will bring new insight into highly relevant topics like DAO collaboration features, smart contract infrastructure scalability and notifications functionality.
    - For developers of decentralized apps we will bring proof of the ease and effectiveness of using Gno.land's Gno smart contract language to solve practical problems that are typically encountered in deploying web3 implementations.
- **Share any referrals or other projects you work with**
    - Berty is an active contributing member of the open source community for over 5 years:
        - [GnoMobile](https://github.com/gnolang/gnomobile), the 1st framework dedicated to building Gno mobile apps
        - [Paris P2P Festival](https://p2p.paris/en/) and monthly events - Berty is a co-organiser and contributor
        - Workshops and presentations at IPFS Camp and Paris P2P festival
            - Berty presentation at IPFS Camp 2019 about Bluetooth Low Energy, libp2p on mobile [https://www.youtube.com/watch?v=p2ZAm2fAvUo](https://www.youtube.com/watch?v=p2ZAm2fAvUo)
            - Berty presentations at IPFS Camp 2022
                - Wesh Network enables builders to create more powerful dApps [https://www.youtube.com/watch?v=PWUnvz9eiF8](https://www.youtube.com/watch?v=PWUnvz9eiF8)
                - Gomobile toolkit support
                    
                    [https://www.youtube.com/watch?v=wZ7DrWXBHUI](https://www.youtube.com/watch?v=wZ7DrWXBHUI)
                    
            - Berty presentation at Paris P2P Festival 2022
                - “*Berty and Offline Communications*”: [https://www.youtube.com/watch?v=2fHHfaeT42M](https://www.youtube.com/watch?v=2fHHfaeT42M)
                - “*Optimize libp2p on Mobile*”: [https://www.youtube.com/watch?v=1-lF8fJ9GgM](https://www.youtube.com/watch?v=1-lF8fJ9GgM)
        - We maintain multiple open-source projects besides the Berty Messenger app: go-orbit-db, go-ipfs-log, gomobile-ipfs
    - We regularly contribute with enhancements to the other open source projects that we rely on like: go-libp2p, go-libp2p-pubsub, gomobile.

—

Milestones Proposal - Details

**P1: GnoSocial v1 - building the foundations of a web3 implementation of a social app**

- **Duration** ~ 5 months (partially overlapping with the other sub-projects)
- **Build GnoSocial v1** with the basic social app features inspired from Twitter:
    - Mandatory *“Needed”* features: create/delete account, post, support external URL (including smart contract link), react, mention, notification, subscribe
        - For the Notification feature we will use the “notification core” service developed by the Gno core team and improve it to fit our needs. We might collaborate with Onbloc to develop this service, as it may be relevant for their product as well.
    - Optional *“Wanted”*: feature: Direct Message
- **End results and deliverables:**
    - GnoSocial v1 app delivered as a mobile app and also as a read-only web app
    - GnoSocial v1 demo to the community, either a video, workshop or other format that makes sense
    - GnoSocial blog-post (at least one) that might include findings from the 2 R&D topics below, if relevant
    - Share our ideas periodically in the Gno Dev Calls and recover feedback from the community
    - Optional: intermediary demos when it makes sense

**P2: R&D - Scalability of Smart Contracts in web3 Social App implementation**

- **Duration** ~ 5 months (partially overlapping with the other sub-projects)
- One of the most interesting aspects of developing decentralized applications using smart contracts is testing the limits and scalability of smart contracts implementations. As we develop the features for GnoSocial, we will perform stress tests on each of them, document the results and try to find scalable solutions if possible.
    - Of particular interest is to explore potential optimisation solutions with data stored as a **Merkele tree**
- Deliverables: being an R&D topic, we cannot guarantee the exact nature and depth of our deliverables. However, we will produce at least one technical document describing our R&D findings. Provided we will have the time and resources PoCs, workshops, blog posts, conference talks are other potential venues we will explore for disseminating the results of our findings.

**P3 R&D - DAO Moderation feature integration with a web 3 Social App**

- **Duration** ~ 5 months (partially overlapping with the other sub-projects)
- Integration of DAO collaboration features in a social app is a legitimate direction of exploration and an obvious opportunity to bring web3 technology innovations in real life use-cases. From a practical point of view, once we will finish adding the “subscribe” feature to GnoSocial we will begin technical exploration with Teritori, who are already working on a similar feature in their [product](https://app.teritori.com/feed).
    - Spoiler: we already started talking with them on this topic.
- Deliverables: being an R&D topic, we cannot guarantee the exact nature and depth of our deliverables. However, we will produce at least one technical document describing our R&D findings. Provided we will have the time and resources PoCs, workshops, blog posts, conference talks are other potential venues we will explore for disseminating the results of our findings.