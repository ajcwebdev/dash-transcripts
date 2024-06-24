---
showLink: "https://www.youtube.com/watch?v=jmqeVaNemGI"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Platform Explorer | Incubator WEEKLY"
publishDate: "2024-06-17"
coverImage: "https://i.ytimg.com/vi/jmqeVaNemGI/sddefault.jpg?v=666fbf38"
---

## Episode Description

Mikhail Savorov from Dash Platform Explorer discusses the inner workings and setup of the explorer tool.

## Episode Summary

Mikhail, developer of Dash Platform Explorer, provides an in-depth look at the inner workings and setup process of the explorer tool. He explains the various components, such as the indexer, API, and frontend, and how they interact with a Dash Evo full node to index and display platform data. Mikhail also walks through the steps required to set up a local instance of the Platform Explorer, highlighting the necessary dependencies and configuration. The episode concludes with a brief discussion on the upcoming Dash Core Group proposal for accelerating the launch of Dash Platform.

## Chapters

00:00 - Introduction and overview of Dash Platform Explorer

Mikhail introduces the Dash Platform Explorer and its purpose in providing insights into the inner workings of the Dash Platform. The explorer is critical for developers to get feedback on their interactions with the platform.

05:19 - Explanation of the Dash Platform Explorer's architecture

Mikhail explains the architecture of the Dash Platform Explorer, which consists of an indexer, API, and frontend. The indexer connects to a local TenderDash node, indexes the blockchain data, and stores it in a PostgreSQL database. The API provides access to this data, which is then displayed by the frontend.

25:15 - Setting up a local instance of the Dash Platform Explorer

Mikhail walks through the process of setting up a local instance of the Dash Platform Explorer. This involves running a full Dash Evolution node, setting up a PostgreSQL database, and configuring the indexer, API, and frontend components. He also demonstrates how to inspect the indexed data and debug the application.

44:58 - Discussion on the Platform Explorer's features and future improvements

Mikhail discusses some of the recently added features to the Platform Explorer, such as custom data contract names. He also touches upon potential future improvements, like the addition of a GraphQL API wrapper. The conversation then shifts to the documentation and the steps required for developers to set up their own instance of the explorer.

1:10:45 - Thoughts on the upcoming Dash Core Group proposal for platform launch

The episode concludes with a brief discussion on the upcoming Dash Core Group proposal to accelerate the launch of Dash Platform. Mikhail, Anthony, and Rion share their thoughts on the potential benefits and risks associated with the proposal.

## Transcript

[00:00] >> All right. We are live.
[00:03] Welcome back to Incubator Weekly.
[00:06] >> Hey, guys.
[00:07] >> Hello.
[00:09] >> Good to have you, Mikhail, here.
[00:14] Just as a brief introduction,
[00:16] I wanted to give an episode where we could refer people
[00:22] to know the inner workings,
[00:24] the inner plumbing under the hood operations
[00:27] of Dash Platform Explorer,
[00:30] which you developed and maintain and host right now.
[00:35] But as part of the show,
[00:37] I wanted to let developers know how it works,
[00:40] but also how they can spin up
[00:43] their own copy and what dependencies are required and so forth.
[00:50] Just so they have everything that they need to know,
[00:52] to know how it works and how to run their own.
[00:58] >> Yeah, sure. What I can do is to show how the Platform Explorer works,
[01:08] how it basically work under the hood,
[01:12] how it inspects all the blocks and transactions.
[01:15] Let me share my screen.
[01:17] >> Yeah. Just as we're doing that,
[01:20] I'll just mention that Anthony and I
[01:23] are doing Dash Platform walkthroughs with several developers,
[01:26] new developers, new to Dash.
[01:28] Not new developers, but new to Dash,
[01:30] new to Dash Platform,
[01:32] and we've found the Platform Explorer to be critical in doing that,
[01:38] so that people can get feedback from an independent source
[01:41] that what they just did actually occurred on
[01:45] a network instead of just locally or something like that.
[01:49] Thank you for the tool, obviously,
[01:52] and looking forward to knowing a little bit more under the hood how it works.
[01:56] >> Yeah. The Platform Explorer
[02:06] works by indexing the whole blockchain of the Dash Platform.
[02:13] On the network level, there is a TenderDash blockchain,
[02:19] and there are blocks,
[02:23] and in the blocks, we have the transactions.
[02:26] >> TenderDash, just for anybody who doesn't know,
[02:30] that's a fork of a modification of
[02:32] the TenderMint consensus algorithm from the Cosmos ecosystem.
[02:41] It just gets all the blocks that exist in the network from the first block to the latest,
[02:51] and it continuously parses all the information.
[02:55] We get to the blocks page,
[02:59] we can see there are 25,000 blocks right now,
[03:03] and if we get to the first of it,
[03:07] we can see there is a first block,
[03:09] and TenderDash exists as a separate process.
[03:22] When you're running the platform node,
[03:25] there is a few services that runs on a master node that provides,
[03:34] for example, just like Dapi,
[03:37] there is a TenderDash, there is a Drive,
[03:39] and TenderDash also has an RPC which allows you to query some data.
[03:47] What indexers do is it queries the RPC of TenderDash,
[03:53] which gives you all the data.
[03:59] There is a set of methods,
[04:03] but what we like to see is the first one is the status,
[04:09] which gives you an information about the network,
[04:14] about the synchronization process.
[04:17] >> Sorry, these are routes that are created by TenderDash,
[04:27] or these are routes that are created by the Platform Explorer?
[04:31] >> These are RPCs that exist in TenderDash,
[04:37] so it's output of the TenderDash process.
[04:40] >> Can you back up one page?
[04:42] I just hit "Back" on that one, so out of status.
[04:49] The index page is what I was looking for that shows all the RPCs.
[04:56] >> Yeah, right there. We have endpoints with no arguments,
[05:02] endpoints that require arguments,
[05:04] and you're running this on port 36657,
[05:11] and that is what exactly what service is running,
[05:14] just so we're explicitly clear what service is running on that port?
[05:19] >> First, what you need to do is to start your own full node,
[05:24] which provide you with some services like the TenderDash,
[05:30] then you will be able to access it.
[05:32] >> Okay. You do need a full Evo node,
[05:38] which is a subset of
[05:40] the Dash master nodes that are collateralized with 4,000 Dash.
[05:45] You're running that yourself,
[05:47] you're not just contacting any old Evo node,
[05:54] you're running your own Evo node.
[05:56] Is that required for this setup,
[05:58] or can you just put in an endpoint for any of the existing Evo nodes?
[06:05] >> No, it requires your self-hosted full node to access RPC.
[06:11] It doesn't connect to the IP,
[06:13] and it connects to the TenderDash RPC,
[06:15] which is available if you spin up everything locally.
[06:21] Let me get to the basics of the Dash Platform Explorer.
[06:27] I think it's worth to show how
[06:35] exactly what is needed to spin up the full node and stuff.
[06:41] Dash Platform Explorer consists of at least three models.
[06:47] There are three packages.
[06:49] It is API, which provides API to the data.
[06:56] There is a front-end, which is the website and the indexer.
[06:59] There are at least three processes
[07:02] which are needed to run the Platform Explorer.
[07:04] The indexer, it connects to the local TenderDash,
[07:10] your full node, and it inserts everything into the Postgres SQL.
[07:19] Then when you visit the page from the front-end,
[07:23] it make a call to the API,
[07:26] which fetches all the data from the Postgres SQL database.
[07:34] In order for you to start your own copy of Platform Explorer,
[07:42] you need to set up a database, Postgres SQL.
[07:47] You need to start Platform Full Node.
[07:53] Basically, that's it.
[08:00] >> Just a question on the full node again.
[08:03] On Dash's Layer 1 blockchain,
[08:05] we have at least three tiers of different types of nodes.
[08:10] You have maybe four different types.
[08:17] You have a light client that just contacts a full node.
[08:22] Then you have a full node itself that hosts
[08:25] a whole copy of the L1 blockchain.
[08:28] Then you have master nodes,
[08:30] and then we will soon have Evo nodes that are like master nodes,
[08:34] but run additional platform services.
[08:37] There's this concept of a full node that is not a master node or an Evo node,
[08:43] but is doing everything that master nodes and
[08:45] Evo nodes are doing except for the master node parts.
[08:49] Is there that same concept on the L2 blockchain where you can have
[08:55] a non-collateralized full node for the Layer 2 blockchain?
[09:00] >> Yeah, of course. The idea of the platform and all the services,
[09:07] that you can host your own,
[09:09] copy your own, so it is decentralized and there is no single point.
[09:16] >> I'm looking specifically to the day when we have platform on mainnet.
[09:24] >> Yeah, ideally.
[09:26] >> They might not have enough dash to run a "Evo node",
[09:30] but they still can run a non-collateralized,
[09:33] meaning they don't have any dash to run,
[09:36] but they want to run a full node.
[09:38] >> Yeah. It's basically the same like we have in Cora blockchain.
[09:45] You can just run the full node copy of the blockchain and access
[09:50] the data locally without connecting to external services.
[09:55] >> The difference there is you're no longer part of consensus.
[09:58] You don't create blocks or validate.
[10:00] You do validate blocks,
[10:01] but you don't create blocks,
[10:03] but you still have the full blockchain,
[10:05] the full proof-of-stake dash blockchain. Got it.
[10:09] >> Yeah. Ideally, everybody would host their own local copy,
[10:19] and when they access the application,
[10:22] they connect to the local instance and stuff.
[10:25] It's the most ideal scenario
[10:28] because you're not connecting to any external server.
[10:34] >> Got it.
[10:36] >> Yeah. Postgres SQL and full node of the evolution.
[10:48] Yeah. When you start the evolution node, full node,
[10:54] you will be able to get to the RPC endpoints of the tender dash.
[11:00] >> The full node is what exposes that service on
[11:10] that port that gives you those back-end routes.
[11:14] >> Okay.
[11:16] >> The transactions in the network,
[11:23] they are existed in two places.
[11:29] There are transactions that are in
[11:33] tender dash network and there are
[11:35] state transitions that belongs to the platform level.
[11:38] Those are pretty, well,
[11:42] it's the same, but the difference is the context.
[11:49] Tender dash transactions is just the data,
[11:55] just base 64 data,
[11:58] which doesn't know anything about the platform stuff,
[12:01] like Apex, for example, identities and stuff.
[12:05] In platform strength state transitions,
[12:07] it is decoded this base 64 data,
[12:11] which have all the platform stuff and platform data.
[12:17] Let's see the first transaction,
[12:21] whichever existed in the network,
[12:24] exists in the network.
[12:26] It's the block with height five.
[12:29] Let's see how it looks on the tender dash level.
[12:39] Nothing much difference between height one,
[12:44] but we have a data field in the block,
[12:49] which lists all of the transactions.
[12:52] All of the transactions are just base 64 encoded string,
[12:59] which you can decode with a JSDPP, for example.
[13:06] Also, the hash SH-256 of this data
[13:14] will be equal to the transaction hash,
[13:17] which is on the network,
[13:19] for example, 965.
[13:23] Hashing this data will result in this transaction hash.
[13:29] >> Those transactions,
[13:32] it's not an array of transaction IDs,
[13:35] that's actually an array of transaction.
[13:37] >> Yes.
[13:40] >> Got it. It looks like there's only one transaction.
[13:45] Am I right with that in this one?
[13:48] >> Yes.
[13:50] >> Do we have a CLI or anything like that,
[13:55] that decodes that transaction?
[13:58] Can you show us what the decoded transaction
[14:01] looks like in either case,
[14:03] maybe just on the front end?
[14:05] >> There is no such library yet,
[14:09] I think, but I have a test where I
[14:14] decode these transactions in my back end, in my API.
[14:19] I can show you how it looks from the JS side.
[14:22] I will connect with debugger and it'll show you.
[14:25] >> Okay.
[14:25] >> How it looks like. Yeah.
[14:30] What indexer do is just,
[14:33] it gets blocks one by one and decode each transaction,
[14:37] extracts all the data,
[14:39] and just moves and copies the data to the Postgres SQL.
[14:46] The Postgres SQL database,
[14:54] so basically there are a bunch of
[15:01] tables which holds all the data that we get from the transactions.
[15:08] There are table for blocks,
[15:10] there are tables for data contracts, documents, identities,
[15:14] state transitions, transfers, which has for identity credit transfers.
[15:21] Might be worth to rename this table, by the way.
[15:25] If we look into definitions of the tables,
[15:30] we can see that all the fields,
[15:32] all the data, for example, in the blocks.
[15:35] All the transactions, caches, and block caches,
[15:39] they are cross-referenced, which is each others.
[15:45] That way we can aggregate data and query and stuff.
[15:51] For example, we have block cache,
[15:55] but if you looked into state transitions,
[16:00] there is also a block cache,
[16:02] which references the block cache,
[16:05] and that way we left join tables and such.
[16:10] The same happens for the different identifiers in the identities,
[16:15] in the documents, there are identifiers,
[16:18] and identities, and documents,
[16:20] they are all linked with each others by the identifiers.
[16:24] >> Do you have a list of the varying types of transactions,
[16:30] either somewhere documented or just mentally?
[16:34] Can you give us an example of
[16:36] what the different types of transactions are?
[16:40] >> Is that what we may have also heard the term transitions?
[16:46] My understanding is transitions are basically
[16:48] just the same term as transaction,
[16:50] but for the proof-of-stake chain,
[16:52] but as a term of convention.
[17:08] Yeah, so here's an example of the output,
[17:13] what we have in database,
[17:15] and the type is integer.
[17:21] I will show you from the code.
[17:24] There are a couple of state transitions right now.
[17:33] Actually, there are, I think, even more right now.
[17:36] This is what we implemented so far in the Platform Explorer.
[17:41] This is like the basic ones.
[17:45] The first one is the most,
[17:48] the first one state transition that is
[17:52] happening in the platform is identity creation.
[17:57] First, before you make any transactions in the network,
[18:01] you need to create an identity.
[18:04] Once you get an identity,
[18:06] you are able to do a data contract,
[18:09] create transactions, which creates data contracts.
[18:12] Then you are able to push documents through documents,
[18:18] batch transactions, state transitions.
[18:21] Then you're also able to top up your identity,
[18:26] also update your data contract,
[18:28] update your documents through documents batch,
[18:32] and rest of the stuff like identity credit withdrawal,
[18:36] transfer, and update the identity.
[18:39] >> Yeah. I have a question while I'm
[18:44] thinking about it because I'll probably forget if I don't.
[18:47] Last time we did our platform walkthrough,
[18:50] we were doing the very last step,
[18:54] which is to delete a document, I believe.
[19:00] Anthony, can you correct me if I'm wrong?
[19:02] The tutorial, were we deleting
[19:04] a document on a contract or were we deleting a contract itself?
[19:10] >> I think it's deleting a document or maybe not a document.
[19:16] >> Okay. Whatever it was,
[19:20] if we delete a document,
[19:25] in theory, my understanding was that that's supposed
[19:28] to refund you the money that you paid initially to store the document.
[19:36] Now, if you delete it from platform,
[19:38] you should get reimbursed a portion of those funds back.
[19:44] Is that true? If so,
[19:47] would that trigger an identity credit withdrawal,
[19:53] withdrawal transfer, or transaction as well, or how does that work?
[19:59] >> That's a good question,
[20:01] but I don't have clear answer on it.
[20:03] I don't know the mechanics of this.
[20:09] That might be a small question to the team, to the platform team.
[20:16] But I can tell you how deletion works on the platform explorer
[20:22] and how the revisions of the documents managed to work.
[20:27] Basically, what we have is we have revisions.
[20:31] On the platform, we have revisions in the data of
[20:34] the data contracts and the documents and identities as well.
[20:41] It starts from zero or one,
[20:45] I don't remember exactly.
[20:47] In the, for example, data contracts,
[20:53] there is a field called version.
[20:58] On the first transaction, when you create a data contract,
[21:02] it will equal to zero, for example.
[21:05] But when you update your data contract, it will increment.
[21:12] Platform Explorer holds every data of every transaction,
[21:18] so it stores the state of the data contract in each version.
[21:26] But when you took virus on the platform explorer,
[21:32] it gets only the last revision.
[21:35] It slices up the data,
[21:38] retrieving only the most up-to-date version.
[21:43] Yeah, it is done by the ID that is in it.
[21:51] - Okay, so I will, I'll give an example and you can tell me.
[22:00] - Yeah, so example, I create a document on the dash pay data contract.
[22:12] So I register my name.
[22:14] Registering my name is creating a document on that contract, right?
[22:18] - Mm-hmm.
[22:19] - And let's say that costs me 1,000 credits,
[22:24] something like that, whatever it is.
[22:26] - Mm-hmm.
[22:26] - And I decide I no longer want to have a DPNS name, dash pay name.
[22:34] I want to get that 1,000 credits back or some portion of it.
[22:40] I delete the document.
[22:42] Is there any record of my, of the existence of, let's say the name is Ryan,
[22:50] is there any record of the existence of that name on the chain
[22:56] beyond that point that I delete it?
[22:58] Or does it, what gets deleted?
[23:00] - It will exist.
[23:02] It will exist in the blockchain, for example, on the tender dash level,
[23:06] but it will not exist in the state.
[23:09] So when users will query the data from the data, for example, it will not exist.
[23:17] So it does not exist in, like, in the drive database,
[23:20] but on the blockchain level, it will exist.
[23:24] - Okay, so there's two concepts.
[23:26] There's data on the platform chain and then there is state on the platform chain.
[23:31] - Yeah, yeah.
[23:32] So basically, tender dash, it just stores the transactions.
[23:37] And what drives do, it just reads the transactions, decodes it,
[23:42] and changes the local state.
[23:45] So there is a global state which has all the info.
[23:49] So each transaction partially mutates the state.
[23:54] And it just states over and over and over with each transaction.
[23:59] And, yeah.
[24:02] - Okay, yeah.
[24:02] So you might have the state, for an example, the state of the DPNS contract
[24:11] might be something like the current existing names, the whole population of names,
[24:20] there are currently 123 of those.
[24:24] Whereas if you indexed all of the transitions and put them in a local database,
[24:34] for example, what you do on Platform Explorer, there might have existed maybe
[24:38] 1,000 or so, or 200, and then some portion of those have been deleted.
[24:45] But the existing state is 123.
[24:48] But that doesn't mean that that's all that have ever existed.
[24:51] That's just how many exist right now.
[24:53] - Yes, yes, yes, yes.
[24:54] Exactly, exactly how it works.
[24:57] - Okay.
[24:58] All right.
[24:59] So what else can we see here?
[25:02] I would, at some point, like to just go through the repo code again and go through the structure.
[25:10] You feel free to do that whenever you think it's best.
[25:14] - Yeah.
[25:15] So what I want to show right now is how to spin up your own local version.
[25:24] I will show you from my IDE, there are two of them.
[25:28] This one is Rust.
[25:29] And, yeah, but this can be done just locally through, you know, just running in your terminal.
[25:39] What the first step will be, we will drop all the data that I have.
[25:45] I already see all the data from the testnet.
[25:48] I want to drop all the data that I have.
[25:52] So to do that, there is a script.
[25:59] Let's go to the packages.
[26:12] Yeah.
[26:18] So there is a script called dbdrop.
[26:22] You just pass the connection, the environments to connection to your Postgres SQL database.
[26:35] Once we do that...
[26:36] - Is that script anywhere in the README?
[26:39] - Yeah, there is, there is.
[26:45] There are default ends which you should change before running all this stuff.
[26:50] So basically, this is how it's done for the terminal.
[26:55] Yeah.
[26:57] So right now we have a clean environment.
[27:00] The first step that we need to do is to run migrations to create the basic, the schema
[27:10] of your database.
[27:13] This could be done also via script.
[27:18] - Okay.
[27:20] So we're starting from a brand new SQL database and we're creating all the schemas.
[27:27] - Yeah.
[27:30] - Once we do that, we have, let me show you, once again, as we drop, there are no more
[27:43] tables in the database.
[27:45] Once we do all the migrations, it will pop out.
[27:52] Yeah.
[27:54] So we have an empty database.
[27:56] Now we need to index some blocks into it.
[28:04] To do that, we'll get to the end.
[28:12] And this is the environments that we need to set for the indexer.
[28:16] We need to pass the Postgres connection environment.
[28:21] We have to pass the URL to your tender-interface.
[28:27] We also need to pass the connection to the core.
[28:31] There is one place where it's required.
[28:36] So it parses, well, it requests some chain logs for some procession.
[28:43] And also, this one is optional, which is the link to the platform data contract identifier.
[28:51] But I will talk about this later.
[28:55] Yeah.
[28:56] Once we have all of this, we either run everything from the terminal, like a cargo run, or we
[29:11] can fill all the environments that are missing, for example, or we can list all of the required
[29:21] environments just in here.
[29:26] Once we start our process, we can see that it couldn't connect to the TenderDash.
[29:43] Is TenderDash running right now?
[29:47] Yeah, it's running, but it's probably failed.
[29:50] I mean, fell.
[29:56] Let's see what's happening.
[29:59] Since you're already using Docker for DashMate, would it be possible to have the Postgres
[30:08] running in a Docker container, so you wouldn't need to have to figure out the local Postgres
[30:16] setup?
[30:17] Sorry, could you repeat?
[30:20] So we're using Docker for DashMate right now, and we're running Postgres locally.
[30:25] Would it be possible to also have Postgres running in a Docker container for this setup?
[30:32] Yeah.
[30:33] I'm actually doing it through the Docker.
[30:37] So I have a Postgres container, which you just map the births that you need and just
[30:44] use it.
[30:45] Gotcha.
[30:46] Yeah, the problem is, yeah, it fell, it crashed.
[30:55] We need to reset the chain, so it syncs from the block
[31:08] number one.
[31:19] So there are flags, which allows you to stop only platform services.
[31:25] So in this particular command, I'm stopping platform services on my full node.
[31:32] Then I drop the platform L2 chain, and then I'm starting again the platform services.
[31:40] So when it starts, it starts from the scratch with the empty data here, and it will start
[31:47] syncing from the block number first.
[31:50] As we can see, yeah, syncing started, and it starts, and it's going.
[31:58] Okay.
[31:59] So we're starting from a fresh platform chain and a fresh SQL database and a fresh indexer.
[32:10] So the indexer is basically just going to say, by the way, can you start the indexing
[32:16] before the chain has synced?
[32:20] Yes, you can.
[32:23] But yes, it's possible.
[32:28] It's just faster.
[32:30] Well, the TenderDash syncs faster because it does not check all the blocks, however
[32:41] drives do.
[32:43] But yeah, TenderDash syncs faster than the Platform Explorer.
[32:50] So TenderDash is syncing the blocks with the other nodes on the chain, and it will be climbing
[32:58] 1, 2, 3, 4, 5, 6, 7, 10, whatnot.
[33:01] And those number of blocks that it's syncing to your local node does that at a faster rate
[33:10] than the indexer is indexing the data on those blocks.
[33:15] Yeah.
[33:16] Yeah.
[33:17] Actually, there are a couple of optimizations that can be made to make it faster.
[33:21] I just didn't do that yet.
[33:24] Okay.
[33:25] Yeah.
[33:26] Yeah.
[33:27] Yeah, it should work faster, just...
[33:29] Are those in process right now, then, the indexing and the syncing?
[33:37] Not really, but it just takes time on the production, but I will change the way I deploy
[33:48] and it will be okay and rolling out smoothly.
[33:55] Yeah.
[33:57] So let's try once again.
[34:01] Ah, here we can see it caught up the chain.
[34:14] So it caught up the RPC role, which became available.
[34:21] So the first step what indexers do is processing the unit chain.
[34:27] So there is a little phase before the actual blocks are started.
[34:32] So there are creation of system data contracts, system documents, like DPNS and stuff.
[34:39] And there are a couple of prefilled data contracts, identities, and documents, which do not exist
[34:48] on the TenderDash level.
[34:49] So it just prefilled with some data.
[34:54] Is there a list of system fields or do you know them off the top of your head, contracts?
[34:59] No, there is no list, but it should be done by the team in the documentation because...
[35:06] I can see them right here, actually.
[35:07] I think you've got DPNS, you've got Featured Flags.
[35:12] Yeah.
[35:13] Yeah.
[35:14] Yeah.
[35:15] That's what I inserted there.
[35:17] That's what I've ever...
[35:20] That's what I know of.
[35:22] Okay.
[35:23] Possibly more, but that's what I know.
[35:26] Yeah.
[35:27] Yep.
[35:28] Okay.
[35:29] So I was curious to see if Dash Pay was a system contract and it looks like it is.
[35:34] Or is it?
[35:35] Like you tell me, is Dash Pay, which is the thing that you register...
[35:40] Like if I want to register the name Ryan, I'm a document on the Dash Pay contract.
[35:48] Is that a system contract of the chain itself or is that a contract from DCG?
[35:54] System.
[35:55] There are five system data contracts, Dash Pay, DPNS, Masternode Rewards, which allow
[36:03] you to delegate some percent of your Masternode Rewards.
[36:10] Also the Withdrawals and one more I don't remember, maybe Featured Flags, which is not
[36:18] used right now.
[36:20] Okay.
[36:21] Yeah.
[36:22] So yeah, and that's it.
[36:27] So what we have now, we just started the indexer process, which indexes all the data.
[36:36] I've done that via debugger that allows me to use breakpoints in the code.
[36:44] So for example, I don't know, somewhere.
[36:51] Should be popping, I don't know.
[37:01] Anyway.
[37:03] Do you have a rough estimate of how long the syncing and the indexing takes?
[37:09] Well, tens of minutes, I think.
[37:14] It's like from 10 to 30 minutes or so, as I remember.
[37:23] And then can you see, there were console logs for the syncing process.
[37:31] Do you have that somewhere still?
[37:33] Well, I don't.
[37:36] Actually the better way to check the syncing process is just to run the frontend and check
[37:41] it just live.
[37:44] So what we want to do is to get to the Platform Explorer, get into the frontend package.
[37:51] Then once we get here, we need to change the environment from production to your local
[37:58] Platform Explorer API.
[37:59] By the way, we should first run the API.
[38:04] Sorry about that.
[38:05] I was going to just ask that.
[38:06] So the frontend needs an API on top of the indexer.
[38:12] Yeah.
[38:13] So what we do is to fill the API.env with basically almost the same data, the Postgres
[38:22] connection, and the base URL, which is the tether-rpc, and this one is optional.
[38:31] Yeah.
[38:36] So the same I have here.
[38:41] I have everything filled in here.
[38:47] So to start the process, just run npm start on all the index.
[38:55] In our case, I will run it from the WebStorm.
[39:02] It starts instantly.
[39:06] It doesn't sync or anything like that.
[39:10] So it just starts on the port just right away and start providing you with the data.
[39:14] Can you open the package.json file on the API?
[39:19] I just wanted to see what...
[39:23] Which one?
[39:24] Yeah.
[39:25] That one.
[39:26] Package.json on that one.
[39:27] Yeah.
[39:28] npm start.
[39:29] It's good.
[39:30] No.
[39:31] So you're on the tendencies.
[39:35] You're on the Docker file.
[39:36] So the package.json file right there that you're hovering over.
[39:40] Click that.
[39:41] Yeah.
[39:42] Oh, that's what you are on.
[39:43] Okay.
[39:44] Yeah.
[39:45] Fastify.
[39:46] Fastify.
[39:47] That's what I was looking for.
[39:48] So you're running Fastify.
[39:49] Yeah.
[39:50] Yeah.
[39:51] Gotcha.
[39:52] Okay.
[39:53] So once we have the API, which is connected to the Postgres SQL where indexer pushes the
[39:59] data, we can start the front end.
[40:07] As I said, you should change the default environment to the local instance of the Platform Explorer
[40:17] API, which is this one by default.
[40:30] Once we have it, we get to the front end package and run npm run dev.
[40:45] So the next application is starting and is available on port 3000.
[40:53] It's compiling.
[40:55] Okay.
[40:58] So now we're looking at localhost 3000.
[41:00] This is not the hosted version.
[41:02] This is-
[41:03] Yes.
[41:04] ... it's contacting the API we just found out.
[41:07] Yeah.
[41:08] Yep.
[41:09] So as the local node is currently syncing, the both layers, the TenderDash and the API
[41:16] is syncing, it will be shown as yellow.
[41:20] But once the TenderDash will finish syncing, it will be the zero or the, sorry, it will
[41:26] be the green.
[41:28] And this one will be yellow until API will reach the latest block.
[41:33] Right now we have like 6000 in the API.
[41:39] When you show, scroll up a little bit, it says platform version 1.0.0-dev.12.
[41:48] What exactly is platform version for anybody that's curious about that?
[41:54] Because my understanding is platform is just a collection of services.
[41:58] So what exactly does that mean?
[42:03] Yeah.
[42:05] So basically each platform version has its own version of SDK that you need to use.
[42:17] And on the Platform Explorer site, there are transactions that you can decode and see the
[42:25] data.
[42:26] So since the transactions itself is Base64 string, it's not that easy to just show the
[42:38] data from the transactions.
[42:40] So how it's implemented on the Platform Explorer when you get to the transactions, for example.
[42:48] Oh, sorry.
[42:56] Once we get the transaction from the database, it gets returned, but it's returned as Base64
[43:02] string and it gets decoded on the client side.
[43:07] So to do that, we need a fixed version of the API, of the SDK.
[43:16] But it's also useful for the desk and for the users to know which one version exactly,
[43:22] which one, which SDK Platform Explorer is using right now.
[43:27] So this is done by, this is basically the value of, this is the value of the package
[43:39] inside the dependencies.
[43:41] So it's basically the same one.
[43:47] The TenderDash version gets returned from the TenderDash RPC status query.
[43:54] Yeah, so this is it.
[44:00] All the queries that are being sent from the front end, for example, trending data contracts,
[44:07] those queries to the database.
[44:14] For example, let's see data contracts.
[44:21] There is a pretty complex queries, but this is because of this complex versioning inside
[44:32] the database where we have different revisions.
[44:34] So we have to filter data, filter, first we get all the rows, then we filter versions,
[44:41] then we filter what we want, you know.
[44:47] So for example, if we get here, if we go to data contracts, we will get a breakpoint.
[44:59] We can get to each line and see how it's working, which variables equals what.
[45:09] And so this is useful for developers who, I don't know, who debug or want to know how
[45:17] it's working or maybe want to contribute.
[45:19] It looks like you're using the Kinect JavaScript query builder, which is pretty popular.
[45:31] Yeah.
[45:33] Quick question on the versioning again, do you know why TenderDash has not been bumped
[45:40] to a version 1.0.0 dev?
[45:44] It looked like it was 0.14 or something.
[45:46] I think there are two versions, there are platform version which will reach v1 and there
[45:52] is a TenderDash version.
[45:54] I think it will stay the 0.14, I think that's the semantic version just used in the TenderDash.
[46:00] So there is a, it's just separate projects.
[46:08] That's why the versioning is different.
[46:12] Yeah.
[46:14] So I also wanted to show you how the transactions are looked through the JavaScript, for example,
[46:22] how it's decoding into Word.
[46:27] So I have a couple of tests here, I believe.
[46:38] So the hex is stored in the database, the SQL database, and it's sent all the way to
[46:43] the front end before it gets decoded.
[46:48] Sorry?
[46:50] The state transition hex is stored in your SQL database and isn't decoded until it's
[47:00] on the front end?
[47:02] Is that correct?
[47:05] Not yet, yeah.
[47:06] It's currently stored the string, yeah.
[47:10] It gets some information, it doesn't have information of the data itself, but it can
[47:16] be done.
[47:17] Okay.
[47:18] And currently, by the way, I don't remember, I think I'm storing it as JSON-B, so the contents
[47:27] of, ah, no, I store documents as JSON-B, so it allows me to make some filtering on some
[47:38] document properties.
[47:41] But transactions themselves are stored as Base64 string, yeah.
[47:51] But transactions are always linked with other entities, like identities and stuff like that,
[47:56] so when identity gets created, it gets created from the transaction.
[48:00] So first, the transactions are inserted in the database, then if the state transition
[48:07] is, for example, identity create, then Indexer creates an identity and links it to the given
[48:17] state transition.
[48:19] Okay.
[48:20] So right now we're looking at the, we're still in the API folder in the tests of the unit
[48:26] integration, the unit tests.
[48:28] Yes, yes.
[48:29] But you would see similar code in the front end as well.
[48:32] Yeah.
[48:33] So there are a couple of mocks that are just sample from the, from the network.
[48:39] For example, we will see createIdentity.
[48:43] So it's the same Base64 transactions that, that is on TetherDash.
[48:50] Yeah.
[48:52] So let's check this, for example, createIdentity transaction.
[49:00] Let's run this test.
[49:07] What we want to do is check how it actually gets created.
[49:16] So first we get a buffer from our Base64 string, and then via Dash SDK client, we get a DPP
[49:27] instance, which is first needs to be initialized.
[49:32] I think we do that in the test.
[49:35] Yeah, we do client platform initialize to initialize Dash platform was in DPP.
[49:44] And then, and then we construct the state transition instance from this buffer.
[49:55] Once we get the state transition, it returns as a JavaScript.
[50:03] I think it's Wasm instance.
[50:06] So it's not just plain JSON object, like where you can just access field via dot notation.
[50:15] But there is a methods which allows you to return the instances of the instance, no like,
[50:24] so if we see the first, what we need to check is the state transition type.
[50:33] So we get it through the getType method, and we can see the state transition type is two,
[50:42] which is equals to identity create in our state transition enum.
[50:53] So this one just is named constants for me.
[51:02] Yeah, so to get the identity inside this state transition, we get it through, well, the structure
[51:15] of the state transitions are different, like each state transition has its own methods,
[51:22] like for data contracts, you need to get your state data contract, then get owner ID, and
[51:28] get owner ID will be a buffer, then you need to make a string from it.
[51:38] So let's check what the identity ID was created during this state transition.
[51:46] After that, we do get identity ID, and then the string.
[51:54] Quick tip for how to get like all these methods, how to check like what method you should call.
[52:02] So you get to the prototype object, in each prototype in the JavaScript, in your instance,
[52:10] which like has a prototype, then you can see a list of methods available at this instance,
[52:19] this one, which will be, oh, sorry, prototype.
[52:26] So for example, if you want to see an asset log proof from the core chain of the state
[52:32] transition, we can see that this is available through the getAssetLogProof method, we get
[52:37] state transition.getAssetLogProof, then you get instant asset log proof, then if you need
[52:47] to get down one more level, you get to the prototype and see what you can get from this
[52:56] asset log proof, and then you get down and one, and down, and down, and down, you know.
[53:01] So how you can inspect the actual structure.
[53:06] Yep, okay, great.
[53:10] Yeah.
[53:13] So in case you're like messed up, you can just check the code that I have, check this
[53:22] test and check which methods you should need to use.
[53:26] You just look and look into platform explorer unit test.
[53:30] Yep.
[53:31] Yeah, that's a great reference, and a lot of times people don't get around to writing
[53:36] tests for many, many years, so you're ahead of the game on that, so thank you for that.
[53:43] That's good documentation.
[53:47] Let's check the status of our blockchain sync and indexing, see if we are close.
[53:55] Well, it's close, I must say that up to 13,000, it gets slow, but then there are no spam transactions
[54:10] from the testers, and it will go much, much faster, like maybe a couple of minutes, maybe
[54:20] five minutes or so.
[54:22] Do you think it will be done in five minutes, or?
[54:27] Yeah, if TenderDash is still working, yeah, it's still working.
[54:33] Ah.
[54:34] Okay.
[54:35] Okay, TenderDash has 12,000, and this is one, API is 11,000, so it's 1,000 block away in
[54:44] the server from the TenderDash.
[54:47] Okay.
[54:48] What's the total block height right now on the hosted version?
[54:53] 25,000?
[54:54] Yeah, but it gets faster after, like, 15,000, so.
[55:03] Because there's, like, stress tests or whatnot, like somebody doing it faster.
[55:08] Yeah, because, yeah, I think it should get to the June 10, and then it will be much,
[55:14] much, much faster, because there are almost no transactions.
[55:19] Yeah.
[55:20] Yeah, also, I wanted to show you this new feature that Platform Explorer just received.
[55:30] Actually, there are at least two.
[55:32] The first one, the Platform Explorer received its own data contract.
[55:40] So how it works.
[55:42] The first feature that we made is custom data contract names.
[55:50] So I have prefilled some custom data contract names for system data contracts, but any developer
[55:58] on the Dash Platform Network can set their own by just pushing the document to the Platform
[56:06] Explorer data contract.
[56:09] So basically, there is this storage of linked data contract identifier and your desired
[56:20] name.
[56:22] So OnSyndexer receives your document from the network.
[56:29] It checks that data contract owner equals the owner of the document who is pushing the
[56:41] document.
[56:42] So it basically verifies the data contract matches this document, and then it sets the
[56:51] custom name for your data contract on the Platform Explorer.
[56:55] So it's basically the Platform Explorer side feature.
[56:59] So it's just a more easy way to make a label for a data contract without registration.
[57:11] So it's made just straight from the network.
[57:13] Okay.
[57:14] Now, hold up, hold up, hold up.
[57:18] Is there not a field in data contracts themselves when you're registering a data contract to
[57:23] give a string name of your data contract?
[57:28] Not yet.
[57:29] It's wiped.
[57:32] So it gets trimmed when you're basically creating it.
[57:38] So if we check the data contract schema, and if we check the data contract itself, it actually
[57:54] doesn't have a name at all.
[57:57] It has a data contracts document type.
[58:02] These are called document types.
[58:04] So one data contracts can have multiple document types, which serves for different purposes.
[58:10] So you can have a storage of data contracts with the names.
[58:14] I can similarly make documents, for example, storage, which will hold the aliases for the
[58:25] custom names for documents, or I can have some other functionality in Platform Explorer,
[58:31] which requires separate storage.
[58:35] Where are the names coming from for the system data?
[58:39] From, well...
[58:43] Like Dash Pay?
[58:44] It's just, yeah, it's just pre-filled.
[58:49] So we're doing initialization of the chain.
[58:53] So they are just, I named it just like...
[59:00] So it's just my name, you know?
[59:04] So it's basically the same how data contracts are named, for example, in the platform.
[59:11] So if we get to the original source of system data contracts, for example...
[59:18] That's just literally the file, you chose the file name, that...
[59:23] Yeah, it's like the system.
[59:24] So in the code, it's like, if I remember correctly, one second.
[59:39] So yeah, in the code, it's like system data contract with Rauls.
[59:44] So I just made a string from it, so basically, that's it.
[59:50] Okay.
[59:51] So that's kind of surprising to me that there's not a native name field for a data contract
[59:58] when you're registering.
[59:59] I think that's exactly the same thing that Paul has just asked of the platform team just
[60:09] recently.
[60:10] So I think they didn't put that in the v1.
[60:13] So I think they thought about it, but it is not a feature for v1.
[60:19] So I made them like a separate thing to make it recognizable.
[60:27] Understandable.
[60:28] And I'm sure that there are reasons for that, because if you have a blessed name field in
[60:35] a data contract, then you have to deal with, okay, are these names going to be globally
[60:41] unique?
[60:43] And if they're not, then you might have people imitating different names, things like that.
[60:49] So it's probably not a very easy problem to solve, I'm guessing.
[60:56] But until that gets sorted out, you have created a platform explorer data contract that essentially
[61:06] registers names of other contracts, and it makes sure that the owner of that data contract
[61:15] is the only person that can register a document on your contract.
[61:20] Is that correct?
[61:24] Almost.
[61:26] So anybody can push a document, but the document names will be set only for those people who
[61:34] have access to their data contract, who are submitting documents from the same identity.
[61:43] So the same owner.
[61:44] So the owner of the label should equal the owner of the data contract.
[61:49] So is that something that clients or that you would have to verify for business logic
[61:56] on your own?
[61:57] Yeah.
[61:58] Yeah.
[61:59] So of course, this is all done.
[62:01] So this is a platform explorer feature.
[62:03] This has nothing to do with the platform.
[62:08] So it's just a feature of the platform explorer website.
[62:13] Yeah.
[62:14] I understand.
[62:15] Okay.
[62:16] So I don't know what else.
[62:26] I see a GraphQL folder.
[62:29] Is that being used or is that a placeholder?
[62:33] Actually, I was thinking about, I was trying some GraphQL stuff and just forgot to remove
[62:39] this folder.
[62:40] Okay.
[62:41] So it's not a feature.
[62:42] If you clone the repo down, I don't think that's in there.
[62:46] Okay.
[62:47] Yeah.
[62:48] So yeah, I had that idea.
[62:52] So yeah, I still have, like, maybe it's a good idea to make a GraphQL wrapper around
[63:01] platform explorer API, or maybe just the platform API.
[63:05] So this will be more convenient for upcoming developer to use all of this, you know, messy
[63:11] API, messy SDKs and stuff.
[63:14] Right.
[63:15] GraphQL is not in vogue right now.
[63:17] So we don't need to do that.
[63:20] We're back to rest, right?
[63:21] That the hot new API is back to rest.
[63:25] I'm just kidding.
[63:26] People don't like building GraphQL APIs.
[63:29] They still like having them handed to them.
[63:31] It's just to explore.
[63:33] Yeah.
[63:34] The good thing about GraphQL is GraphQL can solve, I think.
[63:38] So people really like, can easily make requests, compose requests through GraphQL console.
[63:47] And then you could just give it explore right here on the website and then they could throw
[63:51] some queries in.
[63:54] That would be a cool feature.
[63:55] It's nice for clients, but it's not nice for developers of servers, I think.
[64:00] Yeah, probably.
[64:01] Probably.
[64:02] That's very pale to worry about.
[64:05] Yeah, exactly.
[64:08] Sync progress.
[64:09] Did we, did we end up making it?
[64:10] Did we stall long enough?
[64:12] Unfortunately.
[64:13] Oh, still at 12,000, it needs to get to 25,000, but it goes quicker after what number did
[64:21] you say?
[64:22] Well, I think like 35,000 or so, if we check at the timestamp of this blog.
[64:33] So it's like still in May.
[64:35] So it's going to get to the June 10 or June 5, June 5, I believe.
[64:42] Okay.
[64:43] Well, anything else to, anything else to discuss?
[64:46] The main thing that I wanted to get away from this is how's the, how's the documentation
[64:53] from what we discussed today?
[64:55] I wasn't looking specifically at the documentation yet or through this conversation, but is it
[65:00] adequate for somebody that is a developer, but doesn't know anything about Dash to start
[65:08] their own instance of Platform Explorer?
[65:12] Well, to be honest, I think it will be, well, the documentation doesn't describe this, all
[65:19] the stuff, and there are a lot of tricky parts, I think, when you're running it, but it should
[65:27] be possible, but, but I, but I'm sure I will provide all the support, whoever wants to
[65:36] do it, and yeah, there is a documentation, there is a documentation, just the basic how,
[65:46] how you run.
[65:47] Yeah, I was, I tried to do it while we were going through this, and the, the hardest part
[65:54] is just getting the, the Docker database running and making sure that that's correct in your
[65:57] doc.
[65:58] Yeah, yeah.
[65:59] The most, yeah, the most complex part, I think, is starting the Dash mate, because it requires.
[66:04] The Dash mate part was, was, was fine for, for me.
[66:07] I got that part running.
[66:09] It was, the, the Docker part is where I got, or not the Docker part, the, the Postgres
[66:14] part.
[66:15] Ah, the, the migrations possibly is not described here.
[66:20] Yeah.
[66:21] Migrations.
[66:22] However.
[66:23] Migration, like the initial migration, you're saying.
[66:25] Yeah.
[66:26] Yeah, yeah.
[66:27] The database migration.
[66:28] Yeah.
[66:29] But, but there is a readme for the API document, which, which lists all the HTTP API, and it's
[66:38] always up-to-date whenever I add new requests, new routes, so I had everything in there.
[66:47] So this API should, should be useful for incoming developers.
[66:54] Ah, yeah, but, anything other people can do with it.
[67:03] Ah, yeah, so it's pretty much simple, and it's just plain, plain stuff, you know.
[67:13] So if I had to summarize, I would say, to get a Platform Explorer instance up, you first
[67:20] need to, this is just conceptually, it might not be the right order, there's obviously
[67:25] the prerequisites, but in terms of the concept, you first need a full Dash node, doesn't have
[67:35] to be collateralized, but it has to be a full node with both the core and the platform chains.
[67:47] So you need to, and that's done through DashMate, that DashMate helps you spin up a Dash node
[67:52] and gets both chain, both the core and the platform chains going.
[67:58] That is your, your lowest level prerequisite.
[68:04] Then on top of that, you build, you build a database, an SQL database, we, the documentation
[68:14] needs to be updated so that you know how to do the schema migrations to get the database
[68:21] running.
[68:22] Then after the database is running and syncing, you can then start running the indexer, which
[68:28] queries the database and, yeah, I lost my train of thought.
[68:38] So the indexer, the indexer is actually what seeds the database.
[68:42] Yes, yes, yes.
[68:44] But you need, but you need the database tables, so you need that migration.
[68:48] Then you run the indexer, that then takes data from the blockchain, seeds it into your
[68:53] local database.
[68:55] Then after that, you can run the API, which then contacts your database and creates backend
[69:03] routes for that, that contact your database, your local database, not the chain.
[69:10] At that point, you're contacting the local database and then the front end contacts through
[69:14] the API.
[69:16] So that's the order of operations there.
[69:19] Yeah, exactly.
[69:21] Okay.
[69:23] Any other questions, Anthony, do you feel like this would answer, this episode would
[69:29] answer any questions that developers that we bring into the platform walkthroughs, would
[69:36] this be a sufficient episode for them to get up to speed with, with things?
[69:40] Yeah, no, I thought this was pretty, pretty comprehensive.
[69:45] And I think we identified a couple of places in the readme that we could, might be missing
[69:50] some steps, but I think if they watch through this, they could probably figure it out with
[69:55] a little bit of trial and error.
[69:58] Sure.
[69:59] And, and, you know, maybe, I don't know if Mikhail, that's on your list of priorities
[70:03] to update the documentation, but we could probably also find a developer that could
[70:08] struggle their way through it and make a pull request to that documentation.
[70:12] Yeah, I think I would like to have somebody outside of you test it, whether they can get
[70:21] this whole process going or not.
[70:25] So I think that that schema migration step would be, would be nice to have in the documentation.
[70:29] Okay.
[70:30] Okay.
[70:31] And then we can, we can task somebody to try to spin up their own stack and see, see how
[70:37] far they got and see if they could get all the way through.
[70:40] Okay.
[70:41] Okay.
[70:42] All right.
[70:45] One last question for you, Mikhail, do you have any opinions on the, the upcoming proposal?
[70:53] I don't know if either of you can share your screen and just talk briefly about that.
[70:57] We're already over an hour, so I figured we might as well just talk about that real quick
[71:03] because it's, I think, four days away from the voting deadlines.
[71:08] We won't have another opportunity to talk about this on Incubator Weekly.
[71:13] Do you have an opinion on the Accelerator getting Dash Platform launched?
[71:18] DCG has a proposal out to launch Dash Platform sooner than later.
[71:23] Do you have any opinions on that?
[71:28] Well, well, I think that as I know, as I, as I read, if I read correctly, there is just
[71:41] a month, month delay of withdrawals activated on the platform.
[71:47] So it's just four weeks and I think that's pretty, pretty short period.
[71:55] So that doesn't really, really makes any difference because if, if the team wants to, like, it
[72:02] won't be a one month for like, it may be one month, it may be two months, maybe six months.
[72:11] So on the one hand, on the other hand, like, even if it's a one month, that doesn't make
[72:19] like big difference because we waited so long and I know, but, but, but, but, but the other
[72:28] thing, but the other thing is that we need to push the platform out like it's getting
[72:35] long and long and once we get to the point, like, as we trying to finish it, we just create
[72:44] more task and more tasks to do.
[72:46] Like we found out this one, we found this one, but it's not the best strategy, I think.
[72:53] Happy belated birthday.
[72:55] Thank you, I had recently.
[72:59] So yeah, it's like we got to get it out because it's more, it's more like, like it's a strategy.
[73:13] I think it's, it's more, will be more better for the project to make, make updates as frequently
[73:23] as it can.
[73:24] Like right now we're just holding the position, like we will get it out soon.
[73:28] We will get it out soon, but I think like we should, we should do it and just iterate
[73:35] all the features and, but we couldn't finish and let them marketing guys do all the job.
[73:42] Like it can be as a feature where you can always make a news on it, like, and stuff
[73:47] like that.
[73:48] So yeah.
[73:49] Yeah.
[73:50] So my, my opinion is, is the same pretty much.
[73:55] I think DCG is, is like, that's, it's, it's, it's great that they submitted this proposal
[74:01] that we have, we can have the opportunity to basically say, yes, go ahead and push it
[74:08] out with the added risks, because it's the first time that I know of that we've actually
[74:14] had an explicit proposal based release date.
[74:18] And if that doesn't pass, then yes, they stay in the, it's stated in the proposal that it
[74:25] might be as early as a month later that we could actually get it released.
[74:29] But that's not, I mean, it might be the end of the year again, and then the end of it.
[74:35] So I would say just from a consumer of Dash platform standpoint, as we're walking, taking
[74:41] people through these walkthroughs, just the fact that you have to deal with test net faucets
[74:47] and things like that, that's enough of a hurdle that I think it would be an improvement if
[74:52] we were just on main net.
[74:54] So, so that we could have, you could use real Dash.
[74:59] People could start seeing, okay, this costs this much to add these data contracts and,
[75:06] and we don't have to deal with those test net faucets running dry all the time, things
[75:10] like that.
[75:11] Just logistically, it makes a lot of sense to get it out.
[75:14] My main concern, my only concern really is if we, if we push it to main net right away,
[75:22] is there a chance from what I can, from what I've seen in the past, there have been a lot
[75:27] of times where we they need to upgrade platform and then the data gets wiped.
[75:36] So we wouldn't be able to do that with main net because on main net, the assumption is
[75:40] that your data is there for good until you remove it explicitly.
[75:46] So what can you say about that?
[75:47] Like, why, why do we always wipe the data on Dash platform and how is that going, how
[75:52] is that going to stop so that we don't have to wipe data if we need to make platform updates?
[75:57] Yeah, this is very interesting part.
[76:00] So basically platform team just doesn't want to mess up with the merchant during the development.
[76:09] But there is already a feature, like there is already a mechanism for making upgrades
[76:18] of the network.
[76:19] So as platform team says, it wasn't tested in the testing yet, and I'm waiting for this
[76:28] phase.
[76:29] I hope that guys like we'll do, we'll start doing this soon because this is the most interesting
[76:37] part, part where, where possibly chain halts can occur, stuff like that, how the network
[76:45] will, will perform an upgrade process or, you know, recover from these situations.
[76:52] Yes.
[76:53] Yeah.
[76:54] Chain halt, I think that's, that's, that's almost expected in the industry at this point
[76:59] that proof of stake chains halt every now and then.
[77:03] So I'm not as concerned about that as I am, like, I just want the data to persist and
[77:08] have that be a nice easy upgrade process so that when the chain does halt, which I expect
[77:12] it to, gracefully recover from that.
[77:16] So generally speaking, there is already a mechanism for upgrading the network, but it
[77:22] hasn't been tested yet in the testnet, but team says that there is.
[77:31] So I'm waiting for, for this too, in the testnet.
[77:36] Yeah.
[77:38] So on the main net, we shouldn't have any wipes at all.
[77:42] All right.
[77:43] Well, with that, I think we will go ahead and close it out.
[77:47] Did you want to check your status one last time?
[77:49] If we, if, if it's done, let's show it.
[77:52] If it's not, we'll close it out on your sync progress.
[77:56] Do you have it up, Mikhail?
[78:01] Let me check.
[78:07] He has dark mode on, obviously.
[78:13] Actually it's, maybe it's, okay, let me share my screen just real quick.
[78:25] Joe says, Evo launched by the end of the year.
[78:37] That's what I'm hoping that we can get done before the end of the year.
[78:40] I'm hoping.
[78:41] I don't know.
[78:42] So it was seeing, but, but the full node on my local instance, for some reason is just
[78:50] failing at some point at the block 25,000.
[78:54] I think I had this before, but I don't remember.
[78:57] Let's check if the platform is actually working.
[79:01] Yeah.
[79:02] Platform is working, but, but, but something with the dash mate, tender dash gets, it's
[79:08] crashing at the 25,000, but at least 25,000, we have it.
[79:12] When you, if you, this is a good question though.
[79:15] If you restart, if, if a sync progress process stops for whatever reason, if you restart
[79:22] it, you have to restart at the beginning.
[79:25] It will, it will, it will be in the restarting state, so it will restart over and over and
[79:31] over again.
[79:32] Okay.
[79:33] All right.
[79:34] Well, I think, I think we'll just, we'll let that, we'll let that do its thing and we'll,
[79:39] we'll close out the show.
[79:41] Anthony when's the next platform walkthrough that you have scheduled?
[79:44] Wednesday.
[79:45] Okay.
[79:46] We'll see everybody Wednesday.
[79:49] If not, I might try to sneak in a Tuesday one as well.
[79:52] But we'll see you Wednesday.
[79:53] If not.
[79:54] Bye everyone.
[79:55] Thanks.
[79:56] See you around.
