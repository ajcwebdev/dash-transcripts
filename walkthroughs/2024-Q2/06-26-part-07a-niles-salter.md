---
showLink: "https://www.youtube.com/watch?v=mnCTUt7CBr4"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Platform Walkthroughs Part 7 with Niles Salter"
publishDate: "2024-06-26"
coverImage: "https://i.ytimg.com/vi/mnCTUt7CBr4/sddefault.jpg?v=667a32fa"
---

## Episode Description

Dash Platform Walkthrough with developer Niles Salter, exploring the JavaScript SDK, wallet creation, and blockchain concepts.

## Episode Summary

In this episode, Ryan and Anthony introduce Niles Salter, a developer with expertise in low-level programming languages like Zig. They provide an overview of Dash cryptocurrency and its Platform, discussing the JavaScript SDK, wallet creation, and basic blockchain concepts. Despite some technical difficulties with the testnet being down, they manage to create a wallet and receive test funds. The conversation covers various aspects of Dash's architecture, including its dual blockchain system, consensus mechanisms, and the ongoing development of Platform features. The episode concludes with plans for future exploration of the Dash ecosystem and potential contributions from Niles.

## Chapters

00:00 - Introduction and Technical Background

This chapter introduces Niles Salter, a developer with expertise in low-level programming languages like Zig. The hosts discuss Niles' background, including his work on compiler front-ends and data structures. They explore the potential relevance of Niles' skills to Dash's projects, particularly in optimizing low-level data structures and code. The conversation touches on GroveDB, the database underlying Dash Platform, and its use of Merkle data trees.

05:35 - Overview of Dash and Dash Platform

In this section, Ryan provides a high-level overview of Dash cryptocurrency and Dash Platform. He explains that Dash Platform is a second-layer blockchain built on top of the original Dash blockchain. The key features of Dash Platform are discussed, including Dash Drive for decentralized storage, a decentralized API, and the Dash Platform Naming Service. The hosts also touch upon the different programming languages used in various Dash components, such as C++ for the core blockchain and Rust for Platform.

17:53 - Wallet Creation and Blockchain Basics

This chapter focuses on the practical aspects of interacting with the Dash network. The hosts guide Niles through the process of creating a wallet using the JavaScript SDK. They explain fundamental concepts such as public-private key pairs, blockchain structure, and how transactions work. The discussion includes an explanation of how the blockchain acts as a ledger, tracking ownership of funds across the network.

33:28 - Exploring Dash Repositories and SDKs

The conversation shifts to an exploration of Dash's GitHub repositories. They discuss various components of the Dash ecosystem, including the core blockchain, Platform, GroveDB, and different SDKs. The hosts highlight the importance of the JavaScript SDK and the potential need for improvements or a complete overhaul. They also touch upon the possibility of using WebAssembly to wrap the Rust SDK for JavaScript environments.

55:40 - Hands-on Wallet Creation and Funding

In this practical segment, Niles follows the tutorial to create a wallet using the JavaScript SDK. Despite some initial concerns about the testnet being down, they successfully create a wallet and receive test funds from a faucet. The process demonstrates the basic steps of interacting with the Dash network, including wallet creation, obtaining an address, and receiving funds.

64:56 - Attempting Identity Creation and Troubleshooting

The final chapter involves an attempt to create an identity on the Dash network using the newly created wallet. However, this step encounters an error, likely due to the testnet being down. The hosts discuss the nature of the error and its implications. They conclude by planning a follow-up session to continue exploring the Dash Platform when the network is fully operational.

## Transcript

[00:00] >> All right. Welcome back to Dash Walkthroughs,

[00:05] Technical Issues Edition.

[00:08] >> Yeah.

[00:10] >> No chess set and some difficulties getting us going,

[00:14] but we are here now.

[00:16] >> Yeah. Welcome everybody.

[00:19] For another walkthrough we've got today,

[00:21] our guest is Niles.

[00:24] His last name isn't phone as far as I know,

[00:27] but we have Niles phone here.

[00:30] >> Okay.

[00:31] >> Yeah. Anthony, Niles and I met through our local meetup.

[00:40] AJ knows Niles pretty well and introduced me to him.

[00:46] Then I went to one of the Zig meetups here in Utah,

[00:52] and saw a presentation from Niles

[00:54] and just talked with him for a little bit,

[00:57] and yeah, good to meet you, Niles.

[01:01] Let us know a little bit about you and what you do in terms of

[01:06] software and maybe a little bit

[01:11] about what you know about cryptocurrency as well.

[01:15] >> Sure. Well, what I've been working on a lot recently,

[01:19] as you know, is I've been working on some Zig stuff.

[01:22] Specifically, I've been working on

[01:24] the front end to the Zig compiler.

[01:27] I've been working on ways of applying SIMD and vector techniques,

[01:33] exploiting data-level parallelism to increase

[01:35] the efficiency of the front end of compilers.

[01:39] Yeah, I gave a talk that Ryan was present for.

[01:43] If you look up hyper-optimizing

[01:45] the Zig compiler on YouTube, you'll find it.

[01:48] That talk specifically introduced basically a lot of

[01:55] different ways of how we can apply

[01:58] data-level parallelism techniques on

[02:01] various architectures and how we can get

[02:06] more than one byte at once in the front end of a compiler,

[02:11] which is not typically what you

[02:13] see when it comes to tokenizers and parsers and stuff.

[02:17] I've been doing that thing for a while.

[02:19] I actually have experience working

[02:22] on a TypeScript to Lua transpiler as well.

[02:25] I also made a data structure and maybe I'll show.

[02:29] That's fun.

[02:31] >> You made a data structure.

[02:34] Do you have a CS degree or are you just a hyper-nerd?

[02:37] >> The latter.

[02:39] >> Do you have a CS degree?

[02:42] >> No, I don't. If you pull up my screen share though,

[02:46] I have a little demo

[02:48] that I could probably go through real quick.

[02:50] This is at validarch.github.io@dynastytea,

[02:57] and I just opened up the wrong thing.

[03:01] So yeah, this solves the autocomplete problem.

[03:06] The idea is that every single completion inside of

[03:12] your string corpus is assigned a numeric score

[03:15] saying the relative importance of it.

[03:18] The idea is we're going to have some structure and we want to

[03:22] return the top 10 or so

[03:25] most relevant completions to a prefix string.

[03:28] We don't want a random one,

[03:29] we want the highest scored one.

[03:31] I made this demo that shows how we can start from

[03:35] the idea of a basic try and build on top of that.

[03:39] I'll just step through real quickly here.

[03:42] Let me minimize this so it's just me talking.

[03:47] The thing that I show with the try is that a try is actually

[03:53] not that great when it comes to scored autocomplete.

[03:56] The reason is because you can

[03:58] imagine if we want to autocomplete LI,

[04:00] we have to go down the L branch and go down the I,

[04:04] and then basically everything

[04:06] inside of this subtree we're going to have to search,

[04:08] and this could be an arbitrarily large subtree.

[04:13] The first improvement on a try that we can make,

[04:17] this is actually research that was done by Su and

[04:20] Ottaviano in 2013.

[04:23] They added scores to each node.

[04:27] The leaf nodes already have scores,

[04:29] that's telling us the relevance relative to everything else.

[04:34] But now the internal nodes have a score,

[04:36] and the internal node score is going to be equal to

[04:39] the maximum score of the subtree.

[04:42] What this allows us to do is we can actually follow

[04:47] the maximum score down to a leaf at

[04:49] any given point and thereby prune large amounts of the try.

[04:54] In this demo, I'm just going to show how you do

[04:58] autocomplete for the top five completions to the empty string.

[05:02] The reason for that is because it's the worst case.

[05:05] Let's just go through it really quickly.

[05:07] We start at the root node,

[05:08] we see the highest score,

[05:11] we can follow it down to the leaf,

[05:13] and it happens to be Wikipedia.

[05:15] I pulled this data set off Wikipedia.

[05:17] Then I show the next step,

[05:19] we're just going to grab,

[05:21] we do all the steps at once,

[05:23] is what I'm showing you, and we can do this until we get five.

[05:29] You can see that we're not looking at the whole tree,

[05:31] so this is an improvement.

[05:33] We can do better though.

[05:35] We can sort the tree horizontally.

[05:38] When we do this and when we depict it as an LCRS tree,

[05:43] this actually looks more like a merge case-sorted arrays problem.

[05:47] If we do the same query on this sorted structure,

[05:53] you can see when we add all of these into

[05:57] a priority queue and take the top one at each step,

[06:01] there's a lot less of the tree that we're looking at,

[06:04] and a lot less of the tree

[06:06] that's actually going into the priority queue,

[06:08] which we can actually bound to

[06:10] just the size of how many completions we want.

[06:13] This was the previous state-of-the-art,

[06:14] and my improvement on top of it was to decompose the tree.

[06:21] That looks like this. We fold

[06:24] the vertical linked list chains into the root node,

[06:28] and then we store the longest common prefix

[06:32] between each node and the nodes inside of it.

[06:35] That enables us to sort vertically.

[06:38] We had already sorted horizontally,

[06:39] now we're sorting vertically.

[06:41] When we draw this in LCRS fashion,

[06:45] now doing the same algorithm is

[06:48] equivalent to extracting the top k elements from a max heap.

[06:53] Doing the same query now looks like this.

[06:56] You can see we look at a lot less of the tree.

[06:59] In fact, now the worst-case query that we had

[07:02] before is actually the best case.

[07:06] It's the easiest to do now,

[07:08] but this is applicable in general at any point in the tree.

[07:11] I do show what it would look like to complete LI,

[07:16] because you'll note

[07:20] that we might have to skip

[07:21] a number of nodes equal to the prefix string length.

[07:24] But aside from that, it's pretty straightforward,

[07:26] and that enables us to do queries in almost optimal time.

[07:30] We can do it in k log k plus length of the prefix string.

[07:33] Kind of fun. I wrote a paper on it,

[07:36] if anyone is interested in that.

[07:39] If you just take away demo here,

[07:42] then there you go.

[07:45] >> Okay.

[07:46] >> Very fun.

[07:50] >> Obviously, you are proficient with the low-level things here.

[07:57] >> So impressive.

[07:59] >> When I saw your presentation, I was like, okay,

[08:04] 90 plus percent of this is over my head.

[08:08] But what interests me is we're not at

[08:13] the optimizing phase right now

[08:16] for the products that we have in Dash,

[08:18] but it may very well be that sometime down the road,

[08:24] we may need some of

[08:26] these specific skills that you have in terms

[08:29] of optimizing low-level data structures

[08:32] and code and things like this.

[08:34] I think it may be relevant at some point,

[08:39] and regardless, I think that the skill set

[08:45] that I've seen that you have could be

[08:47] very good for us in

[08:50] Dash with some of the products that we have.

[08:52] I know that GroveDB is one example

[08:58] of the Dash platform which we'll talk about today.

[09:04] As we get into this,

[09:06] Dash platform is built on

[09:07] a new database called GroveDB written in Rust.

[09:11] One of the features is that it has a proof system

[09:17] and I'm not part of the coders on this.

[09:24] I'm not even really a coder myself.

[09:26] But there are lots of

[09:29] different things like Merkle data trees

[09:32] and the term GroveDB comes from

[09:35] the fact that it's built on a technology that

[09:39] uses trees of trees and that's why it's called GroveDB.

[09:46] You would understand that a lot more than I would

[09:48] understand that even though I have

[09:50] a lot of history with Dash,

[09:54] you'd probably be able to take a look at that code and see

[09:57] what's going on and how that's unique in the field.

[10:01] Without getting into those details right now,

[10:03] I would like to actually start by giving

[10:05] you a little bit of an overview of Dash and

[10:09] just welcome you to ask any questions that you

[10:12] have about it along the way.

[10:15] Because you've expressed an interest in contributing

[10:18] to Dash and contributing to

[10:22] either anywhere from part-time to

[10:24] full-time with your work structure right now.

[10:28] I think you're working four days a week,

[10:30] but you've got a day of

[10:33] the week and off time that you can contribute.

[10:36] I wanted to give you a broad overview

[10:38] of what we're working on here

[10:41] and we'll see what you're interested in.

[10:45] Dash Platform, this is

[10:46] a platform walkthrough series and unfortunately,

[10:49] right now, Testnet is down,

[10:51] so we'll go through more of a conceptual walkthrough.

[10:56] I think that we can still bring up

[10:59] the tutorial that we've been working with as

[11:04] more of a concept and discussions starting point for all.

[11:10] >> I've got the link in the private chat for you, Niles.

[11:13] >> Niles, just go ahead and bring that tutorial up.

[11:18] It's in the private chat section of StreamYard here.

[11:24] >> Got you.

[11:26] >> Then we'll share your screen

[11:28] again and we'll jump right into it.

[11:31] >> I'll be curious, do you have any experience

[11:33] with cryptocurrency at all?

[11:36] >> Not really actually, but I'm excited to take a look.

[11:43] What's going on? I almost got a crypto job one time.

[11:48] I'm just moving my monitor over now.

[11:50] >> Did you just get a job fresh out of high school?

[11:54] >> I actually did go to university for three semesters,

[11:59] and then I ended up getting a job after that.

[12:03] Actually not technical to start,

[12:06] but yeah, actually my first technical position,

[12:13] I did a little trial with Bun with Oven.

[12:19] Yeah, so that was fun.

[12:22] >> Bun, for anybody who doesn't know is,

[12:25] Bun is a JavaScript compiler of

[12:28] sorts that's written in the Zig programming language.

[12:32] >> Yeah, I'd never even heard of Zig until Bun came out,

[12:35] and then started looking into it,

[12:37] and AJ actually used to do some Zig streaming as well.

[12:42] You're going to want to bump up your font five or six times.

[12:48] >> Okay.

[12:49] >> Keep it going.

[12:50] >> One more.

[12:51] >> There you go.

[12:53] >> Yeah.

[12:53] >> Better.

[12:55] >> All right, coding anyway,

[12:58] we can actually read the first section for the first time.

[13:01] >> Yeah, let's read this first section,

[13:03] that'll give us a good high-level overview.

[13:06] >> Sure. Yeah, should we take turns reading it aloud or?

[13:12] >> You can go ahead and read it,

[13:14] and then we'll go from there.

[13:18] >> Okay. Dash Platform Overview.

[13:21] Dash is a digital cryptocurrency that was launched in 2014,

[13:25] originally called Xcoin.

[13:27] It was renamed Darkcoin and then finally rebranded as Dash in 2015.

[13:30] Dash is a portmanteau of digital cash,

[13:33] and was created as a fork of Bitcoin.

[13:35] Despite its origins today,

[13:37] Dash differs significantly from Bitcoin by aiming to be a convenient,

[13:40] fast, and private digital cash platform

[13:43] that is suitable for everyday transactions.

[13:45] This goal is reflected in its design features,

[13:47] which include Private Send.

[13:48] This feature ensures user privacy by mixing transactions together,

[13:52] making them untraceable to individual users.

[13:54] Instant Send, Dash's Instant Send feature

[13:57] enables near-instant transaction confirmations

[14:00] that are faster than Bitcoins.

[14:02] Masternodes, Dash's network includes masternodes or full nodes,

[14:05] which power its unique features like Instant Send and Private Send,

[14:09] as well as its governance system.

[14:11] Decentralized Autonomous Organization,

[14:13] Dash operates as a DAO,

[14:16] meaning it is a transparent member-controlled organization

[14:19] free from central government influence.

[14:22] Block reward allocation.

[14:24] Dash's block reward is split between miners, 45%,

[14:28] masternodes, 45%, and a development fund, 10%,

[14:32] ensuring ongoing platform maintenance and development.

[14:36] In 2019... Okay.

[14:38] Yeah, we'll skip there.

[14:40] So that's basically just the overview of Dash,

[14:43] the cryptocurrency and whatnot.

[14:46] We'll skip the paragraph here, I guess,

[14:49] but I'll just talk about these features a little bit.

[14:53] So Dash Platform is the second-layer blockchain

[15:00] that connects with the first-layer blockchain,

[15:04] but does different things.

[15:07] So storing data is essentially the main feature

[15:11] of the Dash Platform blockchain.

[15:15] And the features are Dash Drive,

[15:20] a decentralized API, usernames for Dash Platform Naming Service,

[15:26] the platform chain, and the Dash libraries.

[15:28] So you and I talked yesterday about some of the things

[15:32] that we needed help with.

[15:35] One of those is the SDK, the JavaScript SDK

[15:38] that we're working with.

[15:41] So that's that last thing is the Dash libraries.

[15:44] So Dash Platform is essentially a bunch of nodes

[15:49] that are operating these services,

[15:51] such as a storage service built on GroveDB,

[15:54] which we introduced a little bit before.

[15:57] And then obviously, if you want to access that data,

[16:00] you need an API.

[16:01] And there's also like this naming service

[16:06] that you can register usernames on

[16:11] to interact with Dash Platform.

[16:13] And you're using the currency Dash to do all this stuff.

[16:16] So it's an open access network that relies on,

[16:22] if you want to write to this global data store,

[16:25] then you pay with the Dash cryptocurrency.

[16:29] So that's the basics of it.

[16:33] And then the client libraries,

[16:35] the main one that we're working on is the Rust client library.

[16:41] And that's a Dash core group is doing that.

[16:44] But we also want to have the JavaScript library

[16:50] working very well as well.

[16:52] So just a brief overview of the timeline here,

[16:56] Dash Platform is going to main net in about a month.

[17:00] And so right now we're working with a test network

[17:03] that's basically orchestrated by Dash core group.

[17:06] But between now and main net,

[17:09] my personal wish is that we can clean up

[17:13] the JavaScript library.

[17:15] So that may be one of the things

[17:16] that we ask you to dig a little deeper into.

[17:19] But yeah, any questions so far, high level questions,

[17:24] just getting oriented in the Dash ecosystem

[17:28] and what we're working on so far?

[17:29] I know we've gone through a lot of stuff

[17:32] just even in that past five minutes,

[17:34] but any questions so far, Niles?

[17:38] - Yeah, I didn't have a question as you were talking,

[17:41] but there's a lot of stuff that I obviously don't know.

[17:45] So as we get into more specifics,

[17:48] I can ask more specific questions.

[17:50] - Yeah, and we've gone about 17 minutes now.

[17:53] So we'll probably plan on about 60 minutes.

[17:57] And so let's continue going through this.

[18:01] Just--

[18:02] - We can probably skip the roadmap section.

[18:04] - Scan through, yeah.

[18:07] So we'll scroll down a little bit and we'll scan through.

[18:13] Yeah.

[18:14] - What's your JavaScript experience like?

[18:18] - Well, like I said, I worked on a TypeScript

[18:21] or Tolua transpiler for a number of years.

[18:23] So I've actually read quite a bit

[18:25] of the JavaScript specification and worked on it

[18:30] in kind of a rigorous manner a little bit.

[18:34] - Great, yeah, this is like entry-level Node stuff,

[18:37] so you should be just fine then.

[18:39] - Yeah, I mean, they're two different skill sets.

[18:41] So when you say you've worked on,

[18:43] you've looked at the specification,

[18:45] you're talking about like the language itself.

[18:48] That's a little bit of a different skill set

[18:50] than working in the JavaScript ecosystem

[18:53] and working with NPM and all that stuff.

[18:55] And you and I talked about that yesterday.

[18:58] You've got experience with that as well.

[19:01] So I don't know how much you're consuming

[19:04] as you're scanning through this,

[19:05] but basically this is a tutorial

[19:08] to kind of get started with interacting

[19:11] with Dash platform and the Dash network in general.

[19:14] So first of all, here we fund a wallet,

[19:20] we create a wallet and we fund a wallet.

[19:23] So if you know nothing,

[19:24] if you know very little about Dash, about cryptocurrency,

[19:27] then this part is kind of foundational understanding.

[19:31] So if you wanted to scroll back up a little bit

[19:35] and if you have any questions about some of this stuff,

[19:39] like what is a wallet and what does it mean to,

[19:44] yeah, to create a wallet,

[19:50] I would guess that you would have some questions about that.

[19:53] 'Cause that's fundamental to the platform

[19:55] is that you have to pay with cryptocurrency.

[19:59] And in this tutorial,

[20:02] you're getting the cryptocurrency from a faucet,

[20:05] which is basically just saying,

[20:07] hey, here's a website.

[20:08] And if you ask for some funds,

[20:10] you give it your address, your cryptocurrency address,

[20:14] and then it sends some funds to that address.

[20:17] And then you can then use that cryptocurrency.

[20:19] So that's what this main part is.

[20:22] But do you know what,

[20:26] what do you know about private-public key pairs in general,

[20:31] like asymmetric key pairs?

[20:34] - Yeah, asymmetric cryptography.

[20:36] I haven't written those kinds of algorithms before,

[20:41] but I think I generally understand the basic idea

[20:46] of there being a public versus private key

[20:51] or being able to escalate into a secure link.

[20:56] So yeah, I guess I couldn't speak at length about it, but.

[21:01] - Yeah, it's very similar to,

[21:07] you know, SSH-ing and things like that.

[21:10] When you SSH and put an SSH key onto a server

[21:15] and you have a private key on your own computer,

[21:19] that's essentially the same technology.

[21:21] It's public-private key pairs, asymmetric keys.

[21:25] And that's the basis of cryptocurrency,

[21:29] is a wallet is just a bunch of public-private key pairs.

[21:34] And then you can,

[21:38] sending money just means that a network is,

[21:42] has a, a network has a ledger of who owns,

[21:49] who's able to make transactions.

[21:52] And yeah, like we won't get into the details

[21:58] of all of that, but.

[22:00] - So does the network,

[22:03] the network keeps track of how much like money

[22:06] or credits everyone has, or is that, okay.

[22:10] - So that's the basis of the blockchain.

[22:12] - Yeah, it's the first and most important job

[22:14] of every blockchain, yes.

[22:16] - Gotcha.

[22:19] Yeah, Anthony, do you,

[22:21] do you want to take a stab at explaining that or?

[22:25] - Like what a blockchain is?

[22:30] - Yeah, like what a blockchain is.

[22:31] - It's easy, it's a linked list, done.

[22:34] - There you go.

[22:36] - Yeah, it's a linked list

[22:37] of cryptographically verified transactions

[22:39] that represent a balance that then attains value

[22:43] through the social contract of continuing to function

[22:47] and not allowing anyone to make up their balance.

[22:50] - So, so you can think of a, of a blockchain as,

[22:57] it is a data structure,

[23:03] like, like Anthony was saying, a linked list,

[23:07] but what the data is in that is the ownership of coins,

[23:12] the ownership of certain funds, I guess you could say.

[23:14] So this kind of gets at the heart

[23:17] of what money is and everything,

[23:19] but in the end, money is just a ledger

[23:22] where you have certain identities owning certain amounts

[23:27] of, of units on the ledger.

[23:31] And when you make a transaction,

[23:33] you're just transferring ownership or transferring,

[23:38] yeah, units from one address,

[23:41] one key pair to another key pair

[23:43] that can control sending that further on.

[23:47] And so blockchain, literally just a chain of blocks.

[23:52] What are the blocks?

[23:53] A block, it's a block of transactions

[23:56] and each of those transactions is modifying this ledger

[24:01] of global state of units of money.

[24:05] So that's kind of the high level description of it.

[24:10] It's just a, it's just a database that has a,

[24:14] a network of, of computers

[24:23] that are coming to decentralized consensus

[24:25] on the state of that blockchain.

[24:28] And so you have another core concept is how,

[24:32] who is able to participate in updating that,

[24:36] that, that blockchain, that ledger,

[24:38] and that's where you get into things like proof of work

[24:41] and proof of stake, where in proof of work,

[24:44] you have to do a bunch of work.

[24:46] Your computer has to do a bunch of work

[24:48] to, to be the next person to update that chain.

[24:53] And in proof of stake, it's, it's a little bit different,

[24:57] but instead of showing that you've done a bunch of work,

[25:00] you show that you own a bunch of the coins already.

[25:03] And so there's, that gives you then the,

[25:07] the right to update the ledger based on what consensus

[25:12] algorithm you're choosing to use.

[25:15] So in Dash, we have actually both consensus mechanisms

[25:19] and two different blockchains.

[25:21] One is a proof of work chain

[25:22] and one is a proof of stake chain.

[25:25] And Dash platform is the proof of stake chain

[25:28] and the traditional Dash network blockchain

[25:32] is a proof of work chain.

[25:33] It's like over 10 years old now.

[25:35] It was one of the first forks of Bitcoin.

[25:39] So we don't expect you to obviously know all of this

[25:44] right off the bat and even the high level.

[25:47] - I do have one question.

[25:49] - Yeah.

[25:50] - Do you have to globally lock the whole chain

[25:54] in order to like do a transaction

[25:57] or can you like do smaller locks on like certain parts of it?

[26:04] - You don't.

[26:05] - I don't know if that makes sense.

[26:07] - No, you don't globally lock anything.

[26:10] It's, it's a, it's an append only thing.

[26:14] And so there are different, there are tons of different,

[26:17] you can have all sorts of different transactions happening

[26:20] at any time on the network.

[26:23] And those are broadcast through peer to peer messaging.

[26:26] So these transactions are basically requests

[26:29] to update the chain, update the ledger.

[26:32] - Let's talk about consensus.

[26:33] I think that kind of answers the question.

[26:36] - Yeah, this is a question of consensus.

[26:38] So in a network where anybody's able to participate,

[26:43] you have to have, there's no concept of global authority.

[26:46] So you can't really, if there was one single authority

[26:51] that said it's operating all of these nodes,

[26:55] then yeah, you could do that.

[26:56] But the whole idea is that anybody can participate

[27:00] that is participating in the, in the consensus algorithm.

[27:05] And so you have a bunch of transactions happening

[27:09] and then there are certain types of nodes

[27:12] that are assembling these transactions

[27:15] into a block of transactions, hence the name block.

[27:18] And then those blocks get up,

[27:23] like a block is considered valid

[27:28] if it shows that it has the valid proof of work.

[27:32] So I don't think that we'll go into the details of that,

[27:35] but there's no global locking or anything like that.

[27:38] It's a consensus mechanism that's based on

[27:42] showing that you are doing a bunch of work.

[27:47] And the whole idea behind the doing the whole bunch of work

[27:51] is a Sybil proof mechanism

[27:54] that eventually comes to consensus,

[27:56] but isn't immediately in consensus.

[28:00] But there again, and Dash has made improvements on that

[28:04] so that the eventual nature is very, very quick.

[28:09] But yeah, a globally distributed database

[28:13] coming to consensus,

[28:15] there is that concept outside of blockchains

[28:19] and blockchains basically just add

[28:22] the authoritative mechanism on top of that

[28:27] and saying that what we find as authority

[28:31] is based on this idea of proving work

[28:34] or proving stake in the network.

[28:39] But I think it's a little beyond the scope.

[28:43] We're not gonna actually go through.

[28:46] So like, I don't know if we said it explicitly or not,

[28:48] but we're not gonna go through this tutorial

[28:50] and actually code it out

[28:52] 'cause the network's not up right now.

[28:54] - Okay.

[28:55] - But yeah, I just wanted to use this power as--

[28:57] - We should talk about what the functions themselves

[29:01] are doing.

[29:02] So like create wallet, create identity.

[29:04] - Sure. - Yeah.

[29:06] - Wanna go to the first one?

[29:09] So yeah, we got create wallet.

[29:10] - Do you wanna go ahead and take a stab at it, Anthony?

[29:13] - Yeah, so you have your client,

[29:17] which is connecting you to the Dash SDK,

[29:20] and it gives you some of these helper functions

[29:23] to do a lot of the common functionality

[29:26] you would want to do with a blockchain.

[29:29] So as we were saying, the kind of most important thing

[29:32] is that you have some amount of coins.

[29:35] So you have this idea of a wallet,

[29:37] and the wallet has something called a mnemonic,

[29:39] which is a 12-word C phrase that is like your password.

[29:44] And then there's the wallet address,

[29:46] which is a string of alphanumeric text.

[29:51] And basically, you just run this command,

[29:53] create your wallet, it gives you that information back.

[29:56] - Yeah, so the--

[30:00] - Scroll down, you'll see what the output would be.

[30:03] A little-- - Oh, can I go to the front?

[30:05] - Yeah.

[30:06] Yep, so that's exactly what you would see

[30:08] if you were to run that command.

[30:10] - So the mnemonic is, you can see it's just 12 words,

[30:15] and basically, you can, that's just a word-encoded version

[30:20] of a very long random number.

[30:22] So it uses an encoding standard

[30:26] that has, I think, 2,048 words or something like that.

[30:30] So if you take 12 of those,

[30:32] you know the concept well enough to know that,

[30:35] you know, it's like, instead of binary,

[30:37] if you wanted to encode it as hexadecimal,

[30:39] it gets smaller, and if you encode it in base-58,

[30:43] that's even smaller.

[30:44] Well, if you encode it in this very large library,

[30:46] a very large word list,

[30:48] then 12 words gives you a lot of random entropy.

[30:53] So that's the basis.

[30:56] That mnemonic forms the basis

[30:57] of all the other public-private key pair generation.

[31:02] So you can generate a bunch of different

[31:05] public-private key pairs based on this one seed phrase.

[31:10] That's where your wallet address comes from.

[31:14] It's derived from those 12 words,

[31:16] with different encoding, obviously.

[31:19] - Yeah.

[31:22] Is this base-64 or?

[31:24] - It's base-58.

[31:27] - Base-58.

[31:28] - I think it's just a name developed

[31:30] by the cryptocurrency community.

[31:32] So it eliminates some of the characters

[31:37] to avoid similar-looking things,

[31:41] like instead of eyes or something.

[31:42] - Eyes and O's, yeah.

[31:44] - Yeah.

[31:45] - Oh, yeah.

[31:46] - Yeah, 'cause originally, I think the idea was,

[31:49] "Hey, people are gonna be writing this down,

[31:51] "and they don't wanna write down the wrong thing

[31:53] "and not be able to see."

[31:54] But nobody writes it when you practice it.

[31:56] - You have attack vectors also,

[31:58] 'cause people can have a slightly different one

[32:00] saying, "Send it here,"

[32:01] but it's actually being sent here,

[32:03] 'cause that's the thing you gotta know

[32:04] about the cryptocurrency world.

[32:06] Everyone's trying to steal everyone's crap.

[32:08] - Yeah.

[32:11] Okay, so and then this next step,

[32:13] add funds to the wallet with Testnet Faucet.

[32:16] We talked about that a little bit.

[32:18] This network is basically just operated by Dash Core Group,

[32:24] and they will perform the different functions

[32:30] on the network, like miners and masternodes

[32:35] and things like that.

[32:36] And eventually, they spin up a new blockchain

[32:40] when they reset this thing,

[32:42] which they're resetting it right now as we speak.

[32:44] And so when we do this again,

[32:47] and actually, if we go through this on step two,

[32:50] for example, of this series with you, Niles,

[32:54] then we'll actually maybe go through these,

[32:57] and it will make a little bit more sense what we're doing.

[33:00] But the network, yeah, DCG then runs this explorer

[33:08] that shows the state of the chain.

[33:10] And so you can see that, okay,

[33:12] I requested some funds from this faucet

[33:15] because these funds have no value, no market values.

[33:18] So it's just numbers in a database anyway.

[33:21] So you request some funds, they give you some funds,

[33:26] and then you can play around with the Testnetwork.

[33:28] And that's what is shown here.

[33:30] - Right.

[33:33] - Okay, so--

[33:36] - You can get infinite money on the Testnet.

[33:38] - Transaction looks like right there.

[33:39] So a transaction is inputs and outputs.

[33:42] So for example, on that left-hand side,

[33:45] that's your inputs to the transaction.

[33:47] And on the right-hand side is the outputs

[33:49] of the transaction.

[33:51] So you had 6.68 dash as your input

[33:56] that itself was an output from a previous transaction.

[34:00] And now you're requesting that the network

[34:02] does another transaction and says,

[34:04] hey, send a part of that 6.68 to these two addresses.

[34:09] So this total would add up to something close to 6.68

[34:15] minus a small fee that you're giving to the miner

[34:18] for actually doing this on the network.

[34:21] So that's an example of a transaction

[34:23] with one input and two outputs.

[34:26] And the idea there was you're requesting

[34:29] for one of those outputs to be your own address.

[34:33] - Oh yeah, it says the fee right here.

[34:35] - Yeah. - There you go.

[34:36] - Yeah.

[34:38] - Okay.

[34:39] - So the registering and retrieving an identity.

[34:43] The registering an identity is kind of this

[34:46] magic first step.

[34:48] We're dealing now on the proof of stake

[34:51] dash platform blockchain.

[34:53] And we're asking to register an identity.

[34:57] And this question has come up before several times

[35:00] and I unfortunately don't have a great answer to it.

[35:04] But what is registering an identity?

[35:06] Essentially it's creating a public private key pair

[35:08] but I don't know which type it is.

[35:10] And this is actually the point in the tutorial

[35:13] where I wanted to break off a little bit from the tutorial

[35:17] and actually just go into the GitHub source code

[35:20] to give you an idea of what kinds of code bases

[35:24] we're working with and what you might want to contribute

[35:30] to as we work together in the future.

[35:34] So go ahead and open up a new tab

[35:36] and go to github.com/dashpay.

[35:41] - Okay.

[35:46] - Let's see, github.com/dashpay.

[35:53] Did we go there?

[35:54] There we go.

[35:58] Okay, so you can see they've got,

[36:03] they meaning Dash Core Group,

[36:04] they're the primary development organization

[36:07] that is in Dash and they develop and maintain

[36:11] the core blockchain and the platform blockchain.

[36:15] You can see just, yeah, scroll up a little bit further.

[36:20] Yeah, right there.

[36:21] You can see that the Dash blockchain,

[36:24] that just the DASH right there on the top left,

[36:27] that's a C++ code base.

[36:30] Platform itself is a Rust code base for the most part.

[36:35] And then GroveDB is the actual database

[36:40] that platform is built on top of.

[36:44] TenderDash is the consensus mechanism that's built in Go.

[36:48] It's a fork of the tender mint.

[36:53] You see the SBFT consensus, SBFT is, what's the S?

[36:58] I don't remember what the S is,

[37:05] but BFT is a very common,

[37:08] even outside of cryptocurrency contexts,

[37:13] it's a Byzantine fault tolerant consensus mechanism.

[37:18] So this kind of gets back to your question

[37:21] about locking the whole chain.

[37:24] It doesn't do that.

[37:25] It uses these state transition, state machines.

[37:30] And so this is just, I'm giving you a high level overview.

[37:34] You'll be interested in doing some of this research

[37:37] 'cause that seems like, yeah,

[37:41] like the low level stuff is probably interesting to you.

[37:45] But yeah, continuing the high level,

[37:48] the Dash wallet and the Dash wallet iOS repos,

[37:52] those are the Android and iOS respective mobile wallets.

[37:57] And then, so this is client kind of,

[38:03] this is what you would make transactions from, for example.

[38:07] So if you wanted to make a transaction using a mobile app,

[38:12] you could use this wallet software.

[38:14] If you wanted to use iOS, you'd use the other software.

[38:17] And then what they don't have tagged

[38:21] is that we also have a bunch of JavaScript libraries.

[38:25] But if you scroll down or search for JavaScript,

[38:30] yeah, view all repositories.

[38:32] And then you can just kind of see all the different pieces.

[38:40] And there's a lot of pieces that go into this.

[38:43] So pretty much any language that you are,

[38:47] we don't have much, we don't have anything going on with Zig,

[38:51] but we do have a lot of Rust.

[38:53] And you tell me how similar are those.

[38:57] - So Rust, the main feature I think is its type system

[39:03] and how it stops you from having

[39:07] more than one mutable reference

[39:08] and those types of things.

[39:10] I haven't used Rust that much.

[39:13] Zig is more like C, but a little bit safer.

[39:17] So yeah, that's basically the distinction.

[39:22] I've heard people say that Rust is to C++

[39:25] what Zig is to C.

[39:27] So that's kind of a comparison there.

[39:29] - Zig is to Rust as C++ is to C.

[39:34] - No, no, no.

[39:35] Rust is to C++ what Zig is to C.

[39:39] - Rust is to C++ as Zig is to C.

[39:42] So Zig is lower level and Rust has more extra features.

[39:47] - Yeah, with Rust, you have to solve things

[39:53] in the Rust blessed way.

[39:56] There's a Rust specific way of doing things.

[39:59] And that gives you nice guarantees sometimes

[40:03] because you know that you're not gonna make

[40:05] certain classes of mistakes,

[40:06] but it can also be restricting.

[40:10] And if you don't want that,

[40:12] then you have to use something else.

[40:14] Or you could use unsafe.

[40:17] - Yeah, I've never really used a low level language.

[40:19] I've written a Rust hello world.

[40:22] So this is all above my pay grade.

[40:25] - Can you zoom in a little bit?

[40:27] And I want you to find the dash SDK.

[40:34] It might not be literal.

[40:40] So yeah, SDK.

[40:42] Let's see.

[40:45] Hmm, go back to the first page

[40:55] and just do a page find for SDK.

[40:59] Yeah.

[41:02] Nothing there.

[41:05] Okay, page two.

[41:08] Hmm.

[41:09] - Not on my control F.

[41:11] I could also do this in org search.

[41:17] That should be the same.

[41:18] Okay, here we go.

[41:20] - I'll be right back.

[41:21] - Got some SDK stuff.

[41:23] Yeah, this is RS SDK, okay.

[41:29] - Yeah, so that's the Rust one.

[41:31] And that's what dash core group is.

[41:35] Is there we go.

[41:37] There's the JavaScript one.

[41:40] So this is the one that we've been having some trouble with

[41:43] because it's not the priority right now for dash core group.

[41:48] And this is one of the two things

[41:49] that I discussed with you yesterday on our phone call.

[41:54] This is again, what the tutorial is using.

[41:58] So some of this will look similar

[42:00] or look familiar from what we've already gone over today.

[42:03] - Hmm.

[42:04] - And yeah, this is something that we could take a look at

[42:10] and see if we can.

[42:13] I'd also, we won't necessarily go through all this

[42:17] on the call today, on the stream today,

[42:20] but AJ has done a bunch of work in the dash hive repo

[42:25] building some of the core level primitives

[42:32] for building wallets.

[42:35] So the dash SDK is like a combination

[42:40] of a bunch of other libraries.

[42:44] If you go to the package.json file in here, let's see.

[42:49] Are we in the, yeah, we're in the JS dash SDK still.

[42:56] Yep, so you can see that this is built

[42:59] on a bunch of different dependencies, right?

[43:04] So a lot of this is older stuff.

[43:09] Like you see a lot of, like this code basis

[43:14] is pretty old, right?

[43:17] And I'm not sure if it would be easier

[43:25] to try to fix, make updates to this SDK

[43:30] or to start fresh with some of the stuff

[43:39] that we've built in the incubator

[43:41] that already has the wallet stuff taken care of.

[43:44] But then, yeah, looking at dappy client, for example.

[43:52] So you can see like the dash Evo, let's look over these.

[43:57] The main one is the dash Evo dappy client.

[44:02] That's essentially what the SDK is.

[44:06] I think that's like the touch point where

[44:14] then if we went to that,

[44:22] we would probably see a bunch of dependencies

[44:25] on other things as well.

[44:27] But that's where you actually are making requests

[44:34] to the dash network.

[44:50] So anyway, I'm just giving you a little bit

[44:55] of an overview here.

[44:59] - Gotcha.

[45:00] - Of the tech stack that we're using.

[45:05] So let's see.

[45:10] Yeah, so dappy client.

[45:17] - Dappy is the--

[45:19] - You cut out for a second.

[45:25] - He's gone entirely.

[45:28] We lost him, it's just you and me, bud.

[45:31] - Wow, that sentence will never be finished.

[45:34] - Ryan's dead now.

[45:38] - I wasn't sure if it was just my internet or what.

[45:41] But yeah, he started slowing down a little bit

[45:43] and then it caught up and I was like,

[45:47] oh, maybe it's okay.

[45:48] And then he just cut off, so.

[45:52] - So is Zig your favorite programming language?

[45:56] Would you say?

[45:57] - For sure, for sure.

[45:59] I love Zig so much.

[46:01] I love that it's very simple.

[46:04] It's one of those languages where I felt like

[46:07] when I first started using it, I mostly knew it.

[46:10] Like, I had to get used to things, of course,

[46:13] like you do with any other language.

[46:15] You need to get muscle memory.

[46:17] But I felt like the basic concepts,

[46:20] like if you know the delineation

[46:23] between the stack and heap memory,

[46:26] which is pretty standard for a low-level language,

[46:28] then it's just a matter of like,

[46:32] oh yeah, the specification says here's the operators,

[46:36] here's what this thing does, here are the types.

[46:39] And the type system is very straightforward and simple.

[46:45] In my opinion, it's what C should have been.

[46:48] Obviously, we have the benefit of hindsight,

[46:49] so I'm not judging her for not being able to do it

[46:53] back in the day, but.

[46:54] - Yeah, it's like years later.

[46:55] - Right, exactly.

[46:56] - A lot of hindsight buys.

[46:56] What was your first programming language?

[46:58] What was the first line of code you ever wrote?

[47:00] What language was it in?

[47:01] - No, it was actually in Lua.

[47:03] And Lua is also another very simple language.

[47:06] - Were you a gamer?

[47:07] - It's a scripting language, yeah.

[47:09] Yeah, big time.

[47:10] - I know a lot of gamers get into Lua.

[47:13] - Yeah, yeah, definitely a lot of time

[47:16] was wasted in my teenage years.

[47:18] - Seeing where you are now,

[47:21] I would not consider that time wasted.

[47:23] - Yeah, I mean, yeah, it's one of those things

[47:29] where you could tell someone like,

[47:32] oh yeah, I've been, the first time I wrote a script

[47:34] was like nine years ago.

[47:36] So I've been at this for a long time, you could say.

[47:39] But then at the same time, it's like,

[47:41] well, all the stuff that I learned with Lua,

[47:44] I mean, you could probably pick it up

[47:45] in a couple of weekends nowadays.

[47:48] And like--

[47:50] - This is the problem with all you savant people

[47:53] who started at a young age.

[47:54] You have no idea how long this stuff takes to learn

[47:57] when you start as an adult.

[47:58] Like, it took me like a year

[48:00] just to understand like basic JavaScript.

[48:03] And I'm serious.

[48:03] Like, it's really hard when you start as an adult,

[48:06] you don't know where to start.

[48:07] There's all these videos, there's all these tutorials,

[48:10] and they're all different.

[48:11] They'll tell you to do different things, and it's, yeah.

[48:15] - Well, we got Ryan back, right?

[48:19] - Yeah, sorry about that.

[48:21] - Chat about languages.

[48:22] - So yeah, overall thoughts so far, questions?

[48:29] You guys, I saw just kind of vamping while I was gone,

[48:34] but anything that you had questions about so far?

[48:40] - Yeah, I mean, I guess,

[48:41] so for the JavaScript SDK,

[48:48] you were mentioning a lot of its legacy,

[48:50] and that there's a possibility

[48:52] that just throwing away parts of it

[48:54] might be beneficial in starting fresh.

[48:56] Do you have other SDKs

[49:00] where it already does the right thing,

[49:02] it's already mature,

[49:03] and more or less what you need is a port?

[49:06] - Yeah, I'm glad that you asked that,

[49:08] because that's something I should have brought up.

[49:10] So the best example right now of an SDK,

[49:15] of our SDK is the Rust SDK.

[49:17] So that's one of the reasons why I'm kind of interested

[49:20] in you helping us out here,

[49:22] because you're the type of guy that,

[49:25] once you know programming in one language,

[49:28] you can generally pick up programming in other languages.

[49:32] And so with you knowing those low-level,

[49:38] being a good solid brain, essentially,

[49:41] you can take a look at the Rust SDK,

[49:44] which is the gold standard,

[49:46] and understand what's going on from there,

[49:50] and then try to port that over to the JavaScript library,

[49:54] the JavaScript SDK.

[49:56] Now, I've said that the JavaScript SDK is like,

[49:59] I've said some bad things about it,

[50:01] but in the end, it's actually not that bad.

[50:04] So it has been bad for us,

[50:09] but I think that it's just because we,

[50:13] I haven't looked into the details.

[50:15] - I think also, it's drawbacks are in a couple

[50:19] very specific places that are highly consequential.

[50:23] So if it just knew how to retry and hit different nodes,

[50:27] so it wouldn't completely fail when it hits a bad node,

[50:30] that would fix 90% of the problems.

[50:33] The library itself is solid.

[50:34] Like, the abstractions are good.

[50:36] Like, it's easy to use.

[50:38] The docs are actually pretty good.

[50:40] The problem is just that it breaks in a couple key ways

[50:43] that just completely nukes the entire experience.

[50:46] - And yeah, I guess I do have to ask,

[50:52] in terms of how deep the pool is for the JavaScript SDK,

[50:57] was there ever a consideration of like,

[51:02] trying to use the Rust, like, reuse the Rust code

[51:05] as like WebAssembly or something,

[51:07] or what was the thought process on that?

[51:10] I guess I don't know what environment

[51:12] you're trying to run this in, even.

[51:14] - Yeah, I think that is actually the plan.

[51:16] That is, that seems to be what DCG's plans are

[51:22] for even the JavaScript, is to wrap the Rust library

[51:27] and do it in Wasm and have that as--

[51:30] - The issue is bundle size, I think.

[51:32] - So, I'm actually not sure what the issues are.

[51:36] That's something that we would want you to help us with,

[51:41] or, yeah.

[51:44] - So, I mean, I guess I should ask first,

[51:46] is this, this is primarily meant to be run, like,

[51:51] on a website?

[51:52] Someone's gonna visit a website, or?

[51:54] - Well, that's the overall, that's the overall goal

[51:56] is for web developers like AJ, Anthony, I said AJ,

[52:01] but I was thinking of your username, AJCWebDev.

[52:05] For just normal, traditional web developers

[52:10] who may not want to or need to know

[52:13] all the low-level stuff going on under the hood,

[52:16] they just wanna be able to spin up a web app

[52:19] and use, import something from NPM,

[52:26] like they always do, and like we do with the Dash library,

[52:30] and use in a JavaScript environment,

[52:33] like a browser environment.

[52:34] And, yeah, so I'd, I'd have to talk with DCG

[52:39] about, like, what's their intention, what's their plans,

[52:44] but I know for sure that they are super busy

[52:47] this month and next month getting platform up to mainnet,

[52:53] and they probably won't have JavaScript support

[52:58] for several months, but if we can help with that--

[53:01] - They said it would be alpha, is what the blog post said,

[53:03] it'd be considered alpha, Rust would be considered beta.

[53:07] - Well, and they say that because the SDK

[53:09] that we have right now, they acknowledge that it's,

[53:13] it's behind in development, it's behind the Rust SDK.

[53:17] So whether we bring the Rust SDK

[53:19] into a JavaScript setting using Wasm,

[53:22] or whether we try to rehabilitate

[53:24] the existing JavaScript SDK,

[53:28] or whether we try to see what the essentials are

[53:32] from both the Rust and the JavaScript,

[53:34] existing Rust and JavaScript SDKs are,

[53:37] and try to eliminate the dead code

[53:42] by starting from a clean, fresh base

[53:46] that we have with the JavaScript libraries that Ajay,

[53:51] this time really Ajay O'Neill,

[53:53] has developed through the incubator.

[53:55] Those are the three different approaches.

[53:58] And so this is kind of like, which one is,

[54:01] which one is the best, right?

[54:03] And it's a discussion that we would have to have,

[54:05] and I just wanted to use this hour

[54:09] as a way for you to get some familiar,

[54:13] high-level familiarity with different things.

[54:15] - I mean, I feel like if we throw this guy at the code,

[54:18] give him like two months and all issues will be solved.

[54:21] I'm feeling pretty confident about his abilities, so.

[54:25] - I appreciate that.

[54:26] It's definitely, yeah, it's definitely something

[54:28] where I'm gonna wanna look through all of this

[54:31] and see how it connects.

[54:32] And then I'm gonna wanna go through starting up a wallet

[54:36] and just playing with that,

[54:37] which probably we should do another hour.

[54:40] - Yeah, it's a bummer we couldn't get testnet ranks.

[54:42] I would really love to actually have you running code,

[54:46] but I'm gonna need to schedule another one.

[54:48] - With that said, we can go ahead

[54:51] and we can do the first step of that tutorial.

[54:54] We're already in an hour, so we won't do it right now.

[54:56] - You can create a wallet, you can fund it.

[54:58] - Yeah, creating a wallet is client-side stuff.

[55:01] You don't need a network for that.

[55:02] That's the beauty of that. - Oh, okay.

[55:05] - Yes, if you wanna go back to the first tutorial

[55:07] where we're looking at and just run the first couple steps.

[55:10] So scroll up to where you actually create

[55:12] your project directory and stuff.

[55:15] It'll be set up and configure node project.

[55:18] - Okay.

[55:21] Well.

[55:23] Well, not that.

[55:30] I was trying to grab it and I actually hit the wrong key.

[55:32] Okay.

[55:33] Still hear me?

[55:39] - I'll be right back.

[55:40] Yes, we can still hear you.

[55:42] - All right, cool. - Yeah, you're good.

[55:44] - What's your editor of choice?

[55:47] - I'm a scrub, to be honest.

[55:50] I'm using VS Code.

[55:53] I wanna switch--

[55:54] - I just figured since you're running Linux,

[55:56] you seem like someone who'd be using,

[55:57] I don't know, like WebStorm or something.

[56:00] - I wanna switch to Zed.dev at some point,

[56:04] but it's macOS only for now.

[56:05] - I just tried Zed, actually.

[56:07] Yeah, a couple weeks ago.

[56:08] It was pretty nice,

[56:09] but they don't have the plugin ecosystem.

[56:12] So you use all the plugins you get through VS Code,

[56:16] which is just like, there's so much stuff you get from that.

[56:19] - Yeah, I love VS Code.

[56:23] I wish it was faster.

[56:25] It is what it is.

[56:27] Anyways, should I try running this?

[56:29] Let's go to my documents.

[56:32] - Can you bump up the font on your code side?

[56:39] - Yeah.

[56:41] (mouse clicking)

[56:44] - Oh.

[56:45] - Yeah, keep going.

[56:47] There you go.

[56:48] Thanks.

[56:49] - That's good.

[56:50] - All right.

[56:51] Okay.

[56:57] We're making a blank one?

[57:00] - Yep, and then after this step,

[57:04] you'll create some scripts.

[57:06] - Cool.

[57:08] All right, install -1.0 dev.

[57:12] - Yep, so when we move to main net,

[57:20] this will move from dev to alpha.

[57:23] - Do we need security fixes?

[57:30] I don't think so.

[57:32] We live on the edge.

[57:33] All right, what do we got?

[57:35] - Right now, anyway.

[57:36] We should get them all addressed for sure.

[57:38] - Yeah.

[57:40] It's opening in my other thing.

[57:49] - Podium, that's one of those AI developers, right?

[57:52] - Oh, yeah.

[57:54] Actually, it's just the open source of VS Code.

[57:58] - Oh.

[57:59] - I was on my--

[58:03] - Also a project called Codium

[58:04] that is a AI-enabled IDE, so.

[58:08] - Yeah.

[58:09] - It's not a name probably.

[58:10] - Yeah, it is.

[58:12] Yeah, I was on my E-Ink monitor,

[58:14] so I can switch here to a different color.

[58:18] - You can increase the font a lot on this, too.

[58:21] - I could.

[58:24] Could go more.

[58:27] - One more.

[58:31] - Yeah.

[58:34] - There we go.

[58:35] - So, let's just close this

[58:41] so we can do a terminal right here.

[58:43] Okay.

[58:46] Make a package.json.

[58:56] There we go.

[58:58] (keyboard clattering)

[59:01] There's extra curly braces in there.

[59:17] Yeah, and then delete the top extra curly brace.

[59:21] This is one of the things,

[59:24] I have a separate version of this that's updated,

[59:27] but I didn't think we were gonna go through the code,

[59:29] so I just gave you the canonical one.

[59:31] - Okay.

[59:33] Create a scripts directory for our node.

[59:35] Scripts.

[59:40] And an API directory.

[59:43] Oh, we have a thing here.

[59:47] And we could do this.

[59:56] Sorry if it bothers you, I'm doing one by one,

[59:59] but I like to read it, so.

[60:01] - No, you're totally fine.

[60:02] You can.

[60:03] - Network will be set to testnet via the network variable.

[60:08] And do I have env yet?

[60:11] Yes, I do.

[60:12] Right, I just made it.

[60:15] Okay, import dash from dash.

[60:17] Pass the project's network and wallet configuration

[60:20] through the constructor and export.

[60:22] (sighs)

[60:24] Okay.

[60:26] Do I have my Intel sense?

[60:32] Yes, I do.

[60:33] It's beautiful.

[60:34] Okay, so mnemonic is set to null to indicate

[60:38] we want a new wallet to be generated.

[60:41] Oh, it could be null or undefined, just as God intended.

[60:45] All right.

[60:47] (laughs)

[60:48] Let's get a new address.

[60:49] Replace null with an existing wallet mnemonic.

[60:53] I don't have an existing one.

[60:54] Offline mode is set to true,

[60:56] indicating we don't wanna sync the chain.

[61:00] Okay.

[61:02] Cool.

[61:05] Create a new file.

[61:11] Get wallet, export wallet.

[61:15] (sighs)

[61:17] Okay.

[61:21] And we can just run that.

[61:42] (keyboard clicking)

[61:45] There you go.

[61:50] There's your wallet.

[61:51] Now you can see our--

[61:53] - Made Airship is awesome.

[61:55] Awesome.

[62:02] (keyboard clicking)

[62:05] - Oh, it says we want this in our environment?

[62:16] - That's not really as important

[62:19] 'cause we're not gonna go to the create identity step.

[62:22] Let's just do the test net

[62:23] and then see if we can see your funds on the Explorer

[62:26] 'cause this is where the next function is when that breaks.

[62:30] - Okay.

[62:31] - The test net faucet might not even be working right now.

[62:38] We'll see.

[62:39] - Oh, it worked for me.

[62:41] - Okay.

[62:42] - Oh, which squares are motorcycles?

[62:46] Oh, I missed the mirror.

[62:49] - I hate these kind of captions 'cause they're very ambiguous.

[62:56] It's not always clear what they actually mean.

[62:58] And this is, I think, why the faucet broke for me yesterday

[63:01] is 'cause I did the capture wrong.

[63:03] - You guys consider this a bicycle?

[63:05] - I don't know.

[63:07] - These ones are less ambiguous.

[63:09] - That's a truck.

[63:10] Does that count?

[63:11] I think it counts.

[63:12] Counts as a car.

[63:15] - Compared to a fire hydrant?

[63:18] I would say, yeah.

[63:19] (laughing)

[63:21] - This is the real test of intelligence right here.

[63:26] Oh, see, I messed it up.

[63:27] - No.

[63:28] - Bicycles.

[63:29] I'm including motorcycles in this.

[63:30] Zoom in.

[63:39] These look like bicycles right there.

[63:40] Let's send it.

[63:42] Does that look like a bicycle?

[63:49] So small.

[63:50] I don't think so.

[63:55] I don't think so.

[63:56] - As you can see, the faucet experience, beautiful.

[64:03] - All right, let's get some coins.

[64:06] - Yeah, put your address in the top.

[64:09] - Put your, yeah, it's above the capture, yep.

[64:12] - Yeah.

[64:13] Address in there.

[64:16] - Get coins.

[64:18] - Get them coins, son.

[64:19] - I love getting coins.

[64:23] Do everything I need to?

[64:24] - Yeah, this, the faucet's easier.

[64:29] Is your thing spinning in your tab?

[64:32] - Yeah.

[64:35] - Yes, that's the, yeah, just let it ride.

[64:37] The site's gonna crash, and that means you got your coins.

[64:40] - I love that.

[64:42] Great DX.

[64:43] - Yep.

[64:44] - I know, right?

[64:45] - Only the best.

[64:46] Oh my gosh, it didn't even crash.

[64:49] - Whoa. - Wow.

[64:50] - Look at that.

[64:52] - It must be the synthwave stuff.

[64:54] - I love that.

[64:56] Okay, we got coins.

[64:57] - All right, can I donate fake money to your--

[65:00] - I'm not sure how that was possible,

[65:02] because as far as I know, the network wasn't up.

[65:05] Let me just see if there's any updates on that.

[65:08] - I mean, it might be the faucet itself

[65:10] is just like a node running somewhere

[65:12] that's separate from testnet itself

[65:14] that's just loaded up with funds.

[65:16] I have no idea, so.

[65:18] - Could be.

[65:19] But, oh well.

[65:21] - Okay, what do you want to do now?

[65:23] Go back to the tutorial?

[65:25] - Yeah, see if we can see it in the block explorer.

[65:27] So scroll up to where you got that first link

[65:30] and go to the dash block explorer link.

[65:32] - I'm sorry, block explorer?

[65:39] - Yeah, right there, yeah.

[65:41] And then put your address at the very top.

[65:45] The same one you used.

[65:47] - Okay.

[65:47] - And then put your address at the very top.

[65:50] The same one you put into the faucet.

[65:52] - Okay.

[65:55] Zero.

[66:00] - But you see the transaction though.

[66:04] So that just means it hasn't been confirmed yet, I think.

[66:07] This one's always kind of squirrely.

[66:08] - Oh yeah, that's a good sign.

[66:12] We got it.

[66:15] - There you go.

[66:16] - Yep.

[66:17] - Boom.

[66:19] See, JavaScript works.

[66:21] I don't know what you guys--

[66:21] - We can try the next step.

[66:23] It looks like maybe the net works up so far.

[66:25] - All right.

[66:26] - So let's try the next step.

[66:28] We won't go through the whole thing regardless,

[66:29] even if it is up.

[66:30] But we'll see if our first create identity.

[66:34] - You want to bet on it whether it works or not?

[66:37] - Oh yeah, you want me to click on this or?

[66:40] - No, go back to the tutorial.

[66:42] Scroll past the screenshots

[66:43] and go to the create identity function.

[66:46] Or actually, before that, first update your client.

[66:50] This is important.

[66:51] 'Cause since you ran the create wallet function,

[66:53] it was originally null.

[66:54] Now you need to update so that your mnemonic

[66:56] is in your client.

[66:57] - Gotcha.

[67:00] I lost where I was.

[67:02] So I'm doing the Control + F.

[67:03] - You're right where you need to be.

[67:06] - You're right.

[67:07] - Yeah, yeah.

[67:08] - Right where I need to be.

[67:08] All right.

[67:09] - Yeah, just pop that guy in

[67:12] and then you can do the create identity function.

[67:15] - Cool.

[67:16] - That exited fast.

[67:26] - What?

[67:29] - Oh, you were just echoing.

[67:31] - That was just writing a file, yeah.

[67:34] Yeah, now that you got that,

[67:37] you can run the function

[67:38] and then this will hang for a bit.

[67:41] And we'll see what happens.

[67:44] (mouse clicking)

[67:46] Yep, there you go.

[67:50] That errored pretty fast though.

[67:51] So open it up all the way.

[67:52] And then scroll to error you got.

[67:57] So this is the same error I originally got.

[68:00] It's a socket hangup.

[68:02] This is a new error that I've never gotten before,

[68:05] which makes me believe that Ryan is correct,

[68:08] that the whole network is down.

[68:09] 'Cause sometimes you get an error like this

[68:12] and it just means that you hit a bad node.

[68:14] But this is an error that is different.

[68:17] So, and I'm not really able to parse the errors

[68:20] that it throws when you get a bad node.

[68:22] - Yeah, okay.

[68:25] So this was expected failure.

[68:27] But I'm glad that we were able

[68:28] to at least create the wallet.

[68:30] You got the idea of using the JavaScript SDK.

[68:34] And if the network were up,

[68:36] then we would be more worried about this error.

[68:39] But I think that we should maybe continue this on a part two.

[68:44] And, yeah, you can-- - You mean part B?

[68:47] - Yeah, part B, part.

[68:50] What are we on?

[68:50] Part seven now? - Part seven B.

[68:52] - So seven B, yeah.

[68:54] But yeah, any other high-level questions

[68:58] that you had for us, Niles, or?

[69:00] I know there's a lot to cryptocurrency

[69:06] and blockchains and stuff like that.

[69:08] And we didn't really give you the greatest answers

[69:11] on some of the-- - Yeah.

[69:14] - High-level questions. - Yeah, it's fine.

[69:15] I mean, I'm gonna have to dig into this myself, as well,

[69:20] and come back with more questions.

[69:22] But yeah, it was fun that we got something

[69:27] to work today, though.

[69:28] That was good.

[69:28] - Yeah, so the main repository is dashpay,

[69:31] github.com/dashpay.

[69:33] And then we went through the,

[69:35] there's platform is kind of like what we're,

[69:40] that's the main thing that's new in Dash right now,

[69:45] the Dash repo itself, dashpay/dash.

[69:50] That's like the one that's been around for 10-plus years,

[69:54] and that's very stable and everything.

[69:57] But yeah, it's the platform stuff

[70:00] and all the SDKs and libraries that go along with that

[70:04] that we should look into a little bit more

[70:09] for you helping us.

[70:11] - Sure, and I'll see if I understand anything

[70:16] in this paper, as well.

[70:17] - Yeah, great.

[70:19] All right, well, thanks for everybody for tuning in.

[70:24] I see we got 20 viewers,

[70:26] but most of those are probably Twitter people

[70:28] who just happened to scroll by.

[70:33] Anyway, Anthony, do we have anybody scheduled

[70:37] to come on and do this?

[70:40] - Not yet.

[70:41] I'm gonna be, I'm at a wedding for the next couple of days,

[70:44] so I'm trying not to schedule too many people.

[70:48] But next week, first week of July,

[70:52] we're gonna have two of my friends, Jim and Claire,

[70:55] I'm working on nailing down some times with them.

[70:58] - Perfect.

[71:00] All right, yeah, so we'll look forward to that.

[71:03] And I don't think we have Incubator Weekly

[71:08] scheduled yet for Monday,

[71:11] but it will probably happen,

[71:14] unless you're not able to, Anthony, for whatever reason.

[71:17] But we will see everybody.

[71:18] - I think I'll still be available for that.

[71:21] - Yeah, okay.

[71:22] All right, we'll see you Monday, then, everybody.

[71:25] Thanks. - Yep.

[71:26] All right, later, everybody.