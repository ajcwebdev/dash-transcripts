---
showLink: "https://www.youtube.com/watch?v=VaRvEWdLyyg"
slug: "dapi-on-evonodes"
title: "Get DAPI Working on EvoNodes w/o Delay"
publishDate: "2023-08-21"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/VaRvEWdLyyg/maxresdefault.webp"
---

Mikhail from Dash Incubator discusses proposals for improving Dash development tools and applications as a potential strategist.

## Episode Summary

tl;dr: Mikhail, a former Dash Incubator contributor, presents his ideas for projects he would work on if funded as a Dash Incubator strategist. His proposals include enabling Dash API (DAPI) features for building browser extensions and light applications, creating a mobile app for remotely managing Dash nodes, developing a branded UI kit for easier Dash application development, and continuing work on the Dash Platform Explorer. Mikhail demonstrates the Dash Platform data contract creator tool and discusses the process of deploying data contracts using the Dash SDK JavaScript library.

## Chapters

00:00 - Introduction and Overview of Episode
Rion introduces Mikhail, a former Dash Incubator contributor, who presents his proposals for projects he would work on if funded as a Dash Incubator strategist.

04:56 - Mikhail's Background and Reason for Joining Dash Incubator
Mikhail discusses his experience with Dash, his desire to contribute to the project long-term, and why he chose to join Dash Incubator as a strategist rather than submit proposals independently.

11:52 - Proposal 1: Enabling Dash API (DAPI) Features
Mikhail proposes enabling DAPI features, such as the Dash SPV wallet, without waiting for the completion of Dash Platform, to allow for the development of browser extensions and light applications.

19:20 - Proposal 2: DashMate Remote Control Mobile App
Mikhail presents his idea for a mobile application that allows masternode owners to manage their nodes remotely using the DashMate tool's RPC interface.

24:25 - Proposal 3: Branded UI Kit for Front-End Developers
Mikhail suggests creating a branded UI kit for popular front-end frameworks like React, Angular, and Vue to make it easier for developers to create Dash applications with a consistent design.

29:23 - Dash Platform Explorer Demo
Mikhail showcases the Dash Platform Explorer, a project he has been working on that allows users to explore platform transactions and blocks on the Dash testnet.

31:37 - Dash Platform Data Contract Creator Demo
Mikhail demonstrates the Dash Platform data contract creator tool, which enables developers to compose data contracts using a user-friendly interface, and discusses the process of deploying these contracts using the Dash SDK.

37:26 - Timeline for Mikhail's Proposal Submission
Mikhail and Rion discuss the potential timeline for submitting a proposal for funding as a Dash Incubator strategist, considering the incubator's quarterly funding schedule and Mikhail's ongoing projects within the current structure.

## Transcript

[00:00] The BIS just released their plan for a global central bank digital currency.
[00:12] The BIS is the bank for international settlements. If you missed our previous video on that outfit, check the link in the description titled "BIS Overview."
[00:19] Okay, back to George as he unpacks the BIS scheme. In their words, it's a tokenized, programmable platform.
[00:28] So what they do first and foremost is tokenize all of the assets in private property in the real world. Then it goes on to this global unified ledger.
[00:43] So what they're calling private tokenized money providers, let's just use banks as an example, and tokenized asset providers, those are the companies that manage the ledgers of who owns what.
[00:56] And in the execution environment, this is where the smart contracts would exist. And this is also where the transactions would take place.
[01:04] But let's not forget this purple bar on the left-hand side that says "Rules, Standards, Governance." Who do you think sets up the rules as to how you can use your asset?
[01:16] And they point out that this is managed by the local central bank. And then the BIS would be the central bank of the central banks.
[01:24] So the central bank would manage the domestic ledger that would be connected and integrated into the global unified ledger. And let's remember they have an infinite balance sheet so they could extend credit.
[01:35] They could create currency units for whomever they want. In other words, whoever is in political favor at any given time.
[01:44] And as you know, all of the external information is going into their database in real time. It gives the central bank a lot of fine grained control of how you should be spending your money.
[01:57] Which to me, you know, your money is your business. You should be free to spend your money as how you like it.
[02:04] If we want to defeat this CBDC global elite opponent of ours, we have to be realistic about its strengths and weaknesses. This tokenized programmable platform will be very fast, extremely cheap, and incredibly convenient for transactions.
[02:28] And let's not forget this would be using the exact same currencies that people are accustomed to using. Most of the people will look at this and say, "This is fantastic. Why would I want any other form of money?"
[02:40] They're going to get people hooked on the system. They're going to get them dependent on the network, and then they're going to roll it out.
[02:47] One thing George noted repeatedly during his 40 minute long commentary was that the BIS plan would be rolled out in phases. This strategy, not to force the entirety all at once, which would likely garner pushback, but to implement in steps over time, is advanced by the Fabian Society and their ilk.
[03:02] The group got their name from the Roman general Quintus Fabius Maximus Veracosus, who, when facing a more numerous opponent, opted not for the traditional direct assault and battle, but a delayed tactic,
[03:12] one in which his forces struck against the supply lines and in smaller, terrain-advantageous battles. Initially, Romans were unimpressed with this seeming lack of aggressiveness and dubbed the general "The Delayer" as an insult,
[03:23] but eventually this strategy was seen as effective and "The Delayer" became an honorific title. The logo for the group, a wolf covered with sheep's hide, meaning the underlying malevolent intent is disguised so that it can enter under the radar.
[03:36] That's what the BIS and their comrades are attempting. George then outlines what he perceives as the most difficult problem, what he calls "decentralized tyranny" and "decentralized authoritarianism."
[03:46] Because your opponent, in this case the global elite that are actually managing this entire system, are spread out across the globe in multiple jurisdictions. The world is going into digital money. As I see it, there are really two choices here, you know, or maybe you use both,
[04:04] but there's the central bank digital currencies, you know, the Treasury, the Fed, the governments with their currencies, which are not decentralized, they're not private, they're centrally controlled and they can be programmed so that they can,
[04:17] of course, limit your usage or reward you if your behavior matches the behavior that they wish to see, right? In other words, you're programmable also, not just the money, but socially programmable.
[04:29] Or you can choose decentralized private digital money that's peer-to-peer. So what will you do? Which system will you help to make more robust, not just for yourself, but for the next generation?
[04:40] One that empowers a few technocrats, or one that champions choice, voluntary interactions, and empowers us all? [MUSIC]
[04:56] Hello and welcome to Incubator Weekly. Very happy to be with these two gentlemen today. My co-host, Rion, of course, you know. Hello, Rion.
[05:04] Hello. And if you've seen very many of our shows, you may have seen a former guest and Incubator contributor, Mikhail.
[05:12] How are you today, Mikhail? I'm feeling very fine. Very, very excited.
[05:18] Good. Well, we're excited to have you. And we're a bit -- things are a bit different today than they usually are on episodes in that what we're going to talk about today is Mikhail has the intention to put in a proposal to the Dash, DAO, and future for -- to be an Incubator strategist.
[05:43] And so in relation to that, we're going to go over some of his initial proposals today. That is the things that he would like to work on should he get funded.
[05:53] Does that sound about right, Mikhail? Yeah, yeah, totally.
[05:57] So, yeah, I got dozens of ideas how to improve the Dash and Dash development tools. And, you know, platform really is in the -- I would say in the finishing phase because, you know, it's getting much, much more mature, like, last month.
[06:22] And there are a lot of things to do. There are a lot of possible decentralized applications to build.
[06:30] There are a lot of development tools that should be there to enable quicker development of platform and other Dash applications for the easier integration of different projects on the -- with the Dash network. So, yeah, I had a lot of ideas.
[06:55] And I still have a lot more. And I was starting putting them up on the forum.
[07:03] And at the same time, I was chatting with Rion. And he just proposed me, why not?
[07:09] Why not just go for the Dash Incubator strategist role? And since there are a lot of stuff to do, I think I can, like, you know, manage those projects and hopefully we can make this happen.
[07:29] >> Yeah. I just wanted to jump in and say why I suggested this, because like Mikhail was saying, he's got a lot of ideas. He's got a lot of awareness of what platform is and what it can be used for and how it can be used.
[07:53] Because he has experience both in Dash core group building platform as well as Dash Incubator building on Dash platform and the infrastructure. And more so than I do.
[08:11] And I think that -- so this is exactly why we restructured a little bit and we had our new rules V3 in the Incubator so that people could more easily join as strategists and direct capital essentially. That's the whole idea is not only do you know -- well, you have ideas and you want to throw some money at those ideas.
[08:41] And the more people we have doing this, the more competition we'll have for creating value. And the more choice masternode owners will have in who to fund and to what degree.
[08:58] And so why not just submit your own proposals and just be funded as a solo developer, Mikhail? I'll have an answer to that myself, but what -- just real quick, because I think we do want to jump into what you have in mind.
[09:15] But real quick, why did you want to do this route versus just going solo? I'm still exploring Dash and the people who are involved in Dash.
[09:30] And, yeah, there was plans for making it straight in the Dash DAO, but I don't know how to -- I don't have experience yet of doing that. And you proposed me -- suggested me to just go for a strategist role, and it's just, you know, I just picked it up.
[09:57] And I'll tell you, the reason that I suggested this versus going on your own, I don't really -- I would hope that you would pass going on your own. And I hope that Incubator doesn't hold you down from that, because that's the ideal, is that we have more people proposing as kind of independent groups.
[10:22] But I also want to make -- like, part of being the Incubator is showing that you have an intention to be a long-term -- this isn't just a project that you want to fund. You want to work for Dash on a long-term basis and are committed to working for Dash.
[10:44] And I think that that's a different idea than just, "Hey, I think that we should put this project in and fund this project." Masternode owners still have the same level of flexibility in funding that, but it shows that intention that you want to be part of the organization on the long term.
[11:07] So let's jump right into what you have prepared as far as projects, not just one project, but many projects that will require kind of like full-ish time attention. Oh, I think you're muted, Mikhail, dear.
[11:26] So my first proposal was -- it is a proposal to the network which allows us to leverage those DAPI features that we were long waiting for. And this includes the Dash SPV wallet that we will be able to use.
[11:52] And it's currently -- it's not yet there in the main net. Like, the DAPI is the brand new feature of the Dash platform, and it was planned to be rolled out together with platform.
[12:07] But in fact, like, we don't have to actually wait for the platform for all of the components to be finished in order to run the DAPI. DAPI is like -- it's like a gateway between the Dash network and the applications, you know.
[12:31] And it contains, like, you know, API for all queries, for L1 queries, for the Dash core queries, and on platform queries. So my proposal is to just disable platform queries in the DAPI and move it straight to the production.
[12:50] This way we will enable a way for building browser extensions that will use Dash SPV, Dash SDK as the engine. And it will allow us to build light applications. It will allow other developers to faster integrate it in their products and a lot more.
[13:17] And, yeah, we have -- I think we have all the infrastructure for all the things. We just need to go for it, and all HPMN masternode owners just -- ideally, they just run DAPIs on their hosts, and it will be accessible by anyone in the Internet.
[13:44] We already have, like, 60, maybe, HPMNs or stuff like that. - Evo nodes by the name, if you want to do that. Just so everybody knows. Evo nodes, HPMNs.
[13:59] - Yes, we will have, like, 50 Evo nodes, and that means that we will have already 50 DAPI endpoints, and that's a pretty -- I think that's pretty tough, you know? - Yeah.
[14:18] - This is exciting. I mean, the tech is far and away over my head, but just hearing, like, hey, let's do it with anything to do with Evo, that's exciting. - Yeah, I have -- my main question here is, what has Dash Core Group -- how have they responded to this proposal, if at all, and are they -- would they be on board?
[14:46] Because we all know that, you know, they'll follow the proposal, obviously. They would follow the direction from masternode owners if it were technically possible, but what feedback have you gotten from them?
[15:01] - Honestly, I didn't have any feedback from them yet. I haven't -- like, I wasn't asking them directly yet, because I was focusing on the other proposals as well. I shared my link in the Discord. I also tagged some people to check it, but I didn't have any clear response on this yet.
[15:31] - Well, and this has been up for, what, a week now, something like that? - Yeah, I think we can have an answer from --
[15:39] - And if I could just summarize, and correct me if I'm wrong, the summary of this to me is, hey, we've got a lot of stuff done and ready on using the JavaScript SDK that's being developed. Let's just enable it now, but disable the "evolution features" and just keep the Layer 1 features so that we don't have to use Insight. Is that the main idea?
[16:06] - Yes, yes, exactly, exactly. - Okay.
[16:11] - Is there any more to be said about this? Or does anyone have any questions in the chat about it, or shall we move on to the next proposal? - Yeah. Let's take the questions in the chat, and I will just move to the next proposal, and I will answer all the questions, like, after.
[16:30] - Okay, yeah. - I just have one question to get us started on that last one. Does the SDK provide everything that Insight is currently providing, or are there some missing features?
[16:45] - That's a good question. I haven't counted yet, but I think it does. - And if it doesn't, then we can always just add them, right?
[16:55] - Yeah, yeah. It's very easy to add in case, but I think, yeah, the most, like, all the cases, all the possible, like, cases that would be needed, I think that, yeah. Like, it has HDWallet, it has SPVWallet that will allow you to not store blocks on your client. It has all the utilities to do all the conversions, so, you know, all this stuff.
[17:24] - Can you tell what the current UTXO set is with this? - What do you mean?
[17:32] - So, if I'm a merchant and I want to know, for example, if a payment has come through, can I get notifications through the SDK for notifications? - Yes, yes.
[17:45] - And then can I also, if I'm a wallet provider, so that's good, that's the one, and then if I'm a wallet provider and I don't want to have an instance of Insight running, can I know for a given address what's the current balance on the network for that address? - Yes, yes.
[18:05] - I'm thinking of all the UTXOs. - I need to check, but yes, you can always check your personal transactions. Not sure about everyone's transactions, like, your own wallet, it's always, you can subscribe on events, you can check all your transactions, all your UTXOs, they all be there.
[18:27] Not sure about others, I need to check this carefully. But in any case, it would be a step in the right direction, because there's a lot that it does provide, so reducing that step of having your own Insight server is a big deal, so I think that's a good proposal.
[18:44] - Yeah, that would be great. - Okay, right on. And just for a heads up, for anybody who has questions after this show, Mikhail has said he will make himself available on the, tell me how, again, do you get there, Mikhail, after the show?
[19:01] - Yeah, I will be on the Discord voice chat, and I will be happy to hear all your questions, so I can ask them directly to me. - Great, okay. So then the second proposal here, DashMate Remote Control, what is this?
[19:20] - Yeah, so I have been a long time contributing into the DashMate. DashMate is a tool for running your own master nodes, to deploy them on the servers. It has all the features, like it's very powerful. It has auto-update features, it has start/stop setup, different setup modes, you can set up full node, you can set up master nodes, you can set up local nodes for your dev network.
[19:49] And recently, like maybe six months ago, I have added a very good feature into that, it's called RPC, just on the RPC interface, and it allows you to send comments to your nodes, and check status via just HTTP calls. So I proposed the project of mobile application, that it will allow you to check your node from anywhere, like just via the internet, where you have the internet, you have to check what's going on with your node.
[20:27] - Not just check your node, but it sounds like what you were saying earlier was, you're not just able to check your node, but you're also able to command your node. - Yeah, you have, yes, you can manage your node.
[20:40] - For example-- - via HTTP, which is different than what we have now, right? - What do you mean?
[20:51] - I'm saying, so this is able to send a command to your node via like a normal, like a web browser could do this as well. This is a mobile application that I see in the mock-up, right?
[21:05] - Yes, yes. It's not really available in the web browsers. - Okay.
[21:12] - It will be available on the mobile applications, because in order to securely connect to your node, you have to establish an SSH connection. And in order to make an SSH connection and make a proper tunnel, you have to have like, you know, lower levels of, you know, the system.
[21:34] - Okay. - And yeah, you can manage your node with a mobile application.
[21:40] And for example, if something is happening, or maybe a new update, you can just update it via your mobile, or you can change any settings, or you can just change any settings, or redeploy, or reset it in case there is some re-indexing, re-index issues.
[22:02] Maybe your blockchain is corrupted, you can easily start the process of re-indexing just straight from your mobile phone. So yeah.
[22:13] - So this would work for any node? Like this would work for a regular full node, master node, Evo node, just any Dash node? - Yes, it works for all nodes that are deployed via DashMate.
[22:24] That includes master nodes, Evo nodes, full nodes, dev nodes, what else? I don't know what else.
[22:32] So yeah, and it's possible to manage different master nodes in one application. This one is my mock-up.
[22:46] I have already scratched a simple application, this one is using Flutter for both cross-platform development framework. It is available for iOS and Android.
[23:05] So I did just a quick scratch on this application just to prove that this scheme is working. And yeah, my proposal is to fund the development of this application,
[23:19] because it will allow for master node owners to easily check its nodes from the phone. - Okay, and what kind of checks would they want to do?
[23:32] So the customer for this application is master node owners primarily then? - Yeah, I think they would want to check the status of the node, that it's not failing.
[23:45] I think they would want to check the payment key, like when the next payment will occur. The rewards, I don't know.
[23:59] We could easily add some like rewards history or I don't know. Anything, basically what is available from the dashboard,
[24:10] what is available from the platform, if we are talking about the testnet. So basically, yeah.
[24:20] - Okay. - Let's move on to your third proposal then, Mikhail.
[24:25] - Yeah, this one I submitted just yesterday. And this one is dedicated to the frontend engineers.
[24:35] And the proposal is to make a branded unique UI kit for frontend developers that will ease the development of applications in the Dash network.
[24:53] Like I know that's always a pain for full stack or frontend engineers to start everything over from scratch.
[25:03] And I propose to make a UI kit for each development framework, like the major development framework, like React, Angular, what else, Vue.
[25:15] I don't know what else. And make a documentation for them.
[25:20] And so the people who are onboarding into Dash development, they will be able to easily develop UI applications without needing
[25:29] to rewrite all UI stuff, you know, CSS, HTML. All you need is just to install the library and use components, you know,
[25:41] without knowing the implementation. So you just compose your web UI by composing just little blocks
[25:50] of UI components. - So this is like a dev onboarding proposal?
[25:58] - Yeah, I plan to use this UI kit in my projects that I will bring in the future into Dash.
[26:06] For example, I could reuse this UI kit for the platform explorer. We can encourage people for making applications, like it's just makes easier
[26:22] to jump into Dash development because you already have all the, you know, all the bricks.
[26:28] You just place them one by one. This one is just an example.
[26:34] - Can you zoom in a little bit on this? Can you command plus on that just to zoom in?
[26:40] - Like make the screen bigger if you can? - Yeah.
[26:46] - So, for example, this one is for React. This is just an example.
[26:50] I don't have the code yet, but this is just the real example. If you're a React developer and you want a checkbox, you just place a checkbox tag
[27:01] and put some attributes in, and you can see how they render, basically. And it's possible to document every component that you have and how they
[27:19] will look like. So this stuff is called Storybook, and it will show developers how to reuse
[27:29] the components, how to use them. - So what does this have to do with platform?
[27:35] I'm a little confused on this one. Is this storing the state of these components on a platform in a resume way?
[27:44] - No. No, no, no.
[27:47] It's not strictly for the platform. It's more for the development.
[27:52] Like it will ease the building of UI applications. Like the developers don't need to think about styling their applications.
[28:05] - Oh, you're saying this is like what your first sentence is now kind of making more sense to me.
[28:12] You're saying this is a branded UI kit. If you're building like a Dash application, it's UI components that have Dash
[28:23] branding already built in? Am I totally off base, or am I getting it closer now?
[28:28] - Yes, yes. This is exactly.
[28:31] And this is more for the front-end engineers that would like to jump into their development, make some UIs, and they will have already everything on set.
[28:46] - Okay. So if you want to build a Dash application and you don't want to be a…you're not a
[28:51] designer, you go to this site and it helps you just not have to think about the design.
[28:57] It's just got the functionality. - Yes, yes.
[29:00] - The design already built for you. So it doesn't have anything to do with platform.
[29:04] - Yes, yes, yes. It's more generally for the Dash.
[29:09] - Okay. And when you were speaking about this, Mikhail, you mentioned the Platform Explorer
[29:15] as an example. So could we tie into that at this time?
[29:20] - Yeah. Let me show you.
[29:23] This is one. This one is the website.
[29:27] So the Platform Explorer is the project that we started, like, I believe, like a month ago.
[29:36] And it's exploring… - And this is your site, or whose is this?
[29:40] Whose site is this? - What do you mean, site?
[29:45] It's like who made it? - Yeah, who made it, yeah.
[29:48] - Yeah, yeah. - Who owns the website?
[29:51] - Yeah. I made all the stuff.
[29:53] I'm at the front-end, and I'm at the back-end. That's why it looks kind of dark, you know.
[30:01] And, yeah, so the Platform Explorer is the project that allows you to explore platform transactions, platform network.
[30:11] You can page for blocks. That is happening with the testnet.
[30:17] You can see that testnet already have 40K blocks. You can open blocks and see the information on it.
[30:26] You can check any transactions and decode it. For example, this one particular transaction is about creating an identity.
[30:38] If we look at another one, it's decoding. This one is document batch.
[30:47] I think that's something about inserting documents into the data contracts. So, yeah.
[30:56] - This is pulling live data from the testnet right now already. - Yes, yes.
[31:01] This one is testnet, and it's live. It's working pretty well, and I haven't seen any major outages yet.
[31:13] So, everyone, come and see. Come and check it out.
[31:18] You can see what is happening in the platform. - Okay.
[31:22] - Okay. And then, finally, Mikhail, you were going to show those of us who have not seen it
[31:28] used, or even those of us who have, a demo of how to create a data contract. - Yeah, yeah.
[31:37] This is the dashpay.io website, the data contract creator that was made by the DCG in order to quicker composing of the data contracts.
[31:50] Data contracts in the platform, it states the rules for your applications. You define the rules, how your data will be stored, what fields your data contract has.
[32:03] Like, if you are in Pizzeria, you might want to have street properties, or, you know, address, phone numbers.
[32:12] So, data contract creator allows you to compose it in the UI interface. And, for example, we have, I don't know what, okay, we have Pizzeria.
[32:30] And we can add properties and fill to it. For example, I don't know, address.
[32:38] You can fill in some rules, like, you know, minimum length. You can enter the regex patterning.
[32:46] And, let's say, make some flags. - And just so everyone's clear, this is a tool and website that was created by Dash Core Group.
[33:04] And are you working on this? Or do you want to help build this from the incubator side?
[33:14] Or what's your connection with this? - Honestly, I don't have much connection with it.
[33:24] I just reviewed it. - You have a connection as a user.
[33:30] - Yes, yes, I have a connection as a user. - Gotcha.
[33:33] - Basically, just a generator for your data contracts. So we just composed a little demo with the Pizzeria and the address.
[33:43] And you can see how it actually looks like in the blockchain. I mean, like, how will you submit it as a developer?
[33:53] So we have the Pizzeria data contract. It has address property, which is type of string, and allows you to send from 1 to 10 strings length.
[34:07] - This is the schema, to use the developer language. This is the schema against which you would be able to submit documents that conform to this schema.
[34:18] - And how exactly would one deploy one of these, or as you say, submit them? Like, what would the next step be after this code gets generated?
[34:29] - That's a good question. We should have appropriate deploy tools for that.
[34:37] We don't have yet. We have dash SDK, which is used currently in almost every operation.
[34:46] So as a developer, for now, you just copy this data contract. Then you copy it in your project, and then deploy it with the dash SDK.
[34:56] Like, you register a data contract, and then you will be able to insert documents in it as well with the dash SDK. - And the dash SDK is like a standalone program that a dev would have on --
[35:11] - Not yet, but it is the next proposal. - It's not a program.
[35:16] It's a library. It's a bunch of code that's already written for you that you import into your project.
[35:23] - Yes, yes. If you are a JavaScript developer, yes, you just install this library and just start using it straight away.
[35:32] There is an idea to make it a standalone application. And this will allow to use dash SDK in other languages, like in Python or Rust.
[35:45] I don't know, in any languages, by making it a standalone and enabling HTTP API. So you will talk with the dash SDK standalone application via HTTP requests.
[36:02] And, you know, that will allow to leverage the dash SDK features to other platforms. Like, I don't know, any languages, you know, Java.
[36:16] - Now, isn't this front-end application built in Rust? I heard that this is built in Rust and uses --
[36:26] - Which one? - The one that we're using right now.
[36:30] - Data Control Creator? - Yeah.
[36:33] Well, I don't know. I might be wrong about that.
[36:36] But does it have a link to the source code? - I don't know.
[36:45] Yeah, possibly this is Rust. I can see some WASM.
[36:49] - Yeah, that's what I thought. I was using --
[36:52] - That's cool. That's cool.
[36:54] That's cool. - Yeah.
[36:56] This is not how -- you know, most front-end developers would not do that, obviously. But we have back-end developers at DCG that are in love with Rust.
[37:07] So they're using it as front-end. - That's cool.
[37:10] I haven't seen this yet. - The Rust to HTML or whatever it is.
[37:18] - Okay. Well, that was quite unique, as we had said.
[37:26] Mikhail, do you have a sort of timeline that you could give us as to when you may put in a proposal to get funding for one or more of the projects you've outlined here?
[37:38] I think I will focus it on this week. And, yeah, and we will sort it out.
[37:45] I don't know. - Yeah.
[37:47] I'll actually say something about that as well. So the way that we -- in the incubator, the way that we run is we ask that the strategists follow --
[37:57] we all follow the same cadence, which is quarterly. So the beginning -- it's, like, January, April, June, July.
[38:11] I forget the -- July. Anyway, there's one more month until this quarter ends.
[38:17] - Right. September.
[38:19] - Yes. - Yeah.
[38:21] - So funding for incubator strategists would be next month. But I would guess Mikhail might want to put in some -- what's the term?
[38:34] Like governance proposals, just like a yes or no, you think that this application is good. But we can -- we'll discuss that offline.
[38:43] But in terms of funding, yeah, it would probably be next month. - Got it.
[38:47] - Cool. - Cool.
[38:49] Okay. - And also just one other thing.
[38:52] Mikhail is -- you know, obviously he's got projects that he's working on within the current structure as well. So there's some projects that he's working on in my -- from my budget.
[39:04] And I think he's working on some projects from Tim's and Ash's budget as well. So he's going to continue to do that until he gets funding for his own -- as his own standalone strategist.
[39:18] So that's how it will work. - Makes sense.
[39:21] - At least that's how it would work if he continues to go down this route. And I think that that would be -- that would be great.
[39:28] But anything is available to him, so. - Well, I hope you keep us as foreign clients, Mikhail.
[39:34] I think that's what you called us once on a show or two ago, foreign clients. And I really liked that, so.
[39:43] Okay. So as Mikhail mentioned earlier, if anybody wants to ask him questions directly, interact with him directly,
[39:49] he's going to be on the voice function. Don't ask me what that is.
[39:54] But on Discord, like basically when we close out the show right now. So anyone who wants to talk to him, just hop on over there.
[40:02] And other than that, that closes us up for us today. So --
[40:07] - Great. - Thanks.
[40:09] - Thanks, everyone. Bye.
[40:11] - Bye.