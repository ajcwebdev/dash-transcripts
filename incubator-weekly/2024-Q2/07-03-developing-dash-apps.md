---
showLink: "https://www.youtube.com/watch?v=f_j9n2TK5lc"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Developing Dash Apps | Incubator WEEKLY"
publishDate: "2024-07-03"
coverImage: "https://i.ytimg.com/vi/f_j9n2TK5lc/sddefault.jpg?v=6683f062"
---

## Episode Description

This episode demonstrates how to set up a local Dash network and develop applications using the Dash Platform SDK.

## Episode Summary

In this developer-oriented episode, Mikhail guides viewers through setting up a local Dash network using DashMate and developing applications with the Dash Platform SDK. The process includes creating a local network of nodes, minting coins, creating identities, registering data contracts, and submitting documents. Despite some technical challenges, the tutorial provides a comprehensive overview of local Dash development, emphasizing the importance of version compatibility and proper configuration for a smooth development experience.

## Chapters

00:00 - Introduction and Context

This chapter introduces the episode's focus on developer-oriented content, specifically how to start developing dApps on Dash Platform. The hosts discuss the upcoming launch of Dash Platform on mainnet and emphasize the importance of having a local development environment for faster, more streamlined, and reliable development. They also mention that the documentation being presented is not yet public and is being tested for user-friendliness.

05:58 - Setting Up the Local Dash Network

In this chapter, Mikhail begins the process of setting up a local Dash network using DashMate. He explains the steps to create a group of nodes (one seed node and three masternodes) that simulate a small Dash network on the local machine. The chapter covers the installation of DashMate, the setup process, and troubleshooting various issues related to version compatibility. It highlights the importance of matching versions across different components of the Dash ecosystem for smooth operation.

26:36 - Creating a Dash Client and Minting Coins

This section focuses on creating a Dash client using the SDK and minting coins in the local network. Mikhail demonstrates how to connect to the local DAPI (Decentralized API) instance, generate an address, and mint coins to that address. The process involves stopping and starting the network, which leads to a discussion about potential optimizations for the minting process. The chapter also covers checking the balance of the newly minted coins and preparing for transactions.

54:55 - Working with Identities and Data Contracts

In this chapter, Mikhail explains the concept of identities in the Dash Platform and demonstrates how to create one. He then shows how to create and register a data contract, which is necessary for storing data on the Dash Platform. The process involves creating a simple "Hello World" application that allows storing messages on the blockchain. This section also covers troubleshooting various errors related to schema validation and balance issues.

73:55 - Submitting and Querying Documents

The final chapter demonstrates how to submit documents to the Dash Platform and query them back. Mikhail shows how to create a document, insert it into a batch, and broadcast it to the network. He then explains how to query the submitted documents, touching on the capabilities of the GrubDB query language. The chapter concludes with a brief discussion on SQL support in Dash Platform and the importance of proper indexing for complex queries.

81:31 - Conclusion and Future Plans

This final chapter concludes the tutorial and outlines future documentation plans. Mikhail highlights the importance of local network setup for developers, noting potential issues with laptop sleep mode and advising service checks upon wake. The hosts discuss refining the tutorial for inclusion in the main Dash documentation, with Mikhail planning a Medium post for wider accessibility. They thank viewers, mention the next show's likely return to Monday, and end with farewells.

## Transcript

[00:00] - All right, we are live, Mikhail, how are you doing?
[00:05] - Hey guys, I'm doing well, I'm doing very fine.
[00:12] - Good, good, good.
[00:13] As you'll notice, we don't have Anthony with us today.
[00:16] He has some prior obligations
[00:20] and we're also doing the show on Tuesday.
[00:23] Yesterday, I wanted to be able to join the stream,
[00:28] the AMA with the Desert Lynx and Quantum Explorer,
[00:33] Joelle and Sam, which was nice.
[00:37] And so, yeah, we're doing the show today
[00:40] and we are going to have a developer-oriented show today
[00:44] where we're going to go through some steps
[00:47] that you, Mikhail, have painstakingly put together
[00:52] on how to start developing
[00:55] on developing dApps on Dash Platform.
[01:00] So I think we have quite a bit of content,
[01:03] so let's jump right in.
[01:04] Let's get your screen share going.
[01:07] And while you're doing that,
[01:09] I'll just give a little bit more context.
[01:12] We are going live with Dash Platform.
[01:16] I don't see your screen share coming up.
[01:18] - Wait, one second.
[01:20] - Okay, we are going live with Dash Platform
[01:24] on July 29th, and that means that's this month.
[01:29] So in 27 days, we will activate,
[01:33] we'll have binaries to activate the network
[01:37] and then the network can adopt those.
[01:40] And it will probably take a few weeks, maybe up to a month,
[01:43] I'm guessing, to get everything working out.
[01:45] So in August, we will have Dash Platform
[01:49] running live on mainnet.
[01:52] So that's pretty exciting stuff.
[01:54] But before that, I think it's,
[01:57] before that and even after that,
[01:59] it's important to have the ability
[02:01] to run a local development environment
[02:06] so that you're not relying on either testnet or mainnet
[02:10] to do your local development.
[02:12] It's faster that way.
[02:13] It's more streamlined that way.
[02:16] It's more reliable that way.
[02:18] So regardless of mainnet, testnet status,
[02:22] you can start developing your applications
[02:24] and testing it against what looks like the real network.
[02:29] So Mikhail, I see you got your screen sharing.
[02:34] So why don't you take it away from here?
[02:36] - Yeah, guys, so what I wanna show you
[02:41] is how to run your local separate Dash network
[02:46] from the scratch, like a local group of a few nodes
[02:51] that are running and creating a small Dash network
[02:54] that you can run and--
[02:57] - One thing real quick, sorry to interrupt.
[02:58] Can you bump up the font and just kind of always
[03:01] keep the font as big as you can
[03:04] so that the old people like me can see the text?
[03:07] - Yeah, so the first step that you want to do
[03:15] to start this development is you need to connect
[03:20] to the network with your SDK.
[03:23] So you basically might want to just create
[03:29] a local Dash network that consists of a few nodes
[03:34] that are connected together.
[03:37] And it will create a separate environment
[03:40] from the testnet, from the mainnet,
[03:42] so you can develop your stuff just separately
[03:46] from the network.
[03:48] So what you need is Node.js on your workstation.
[03:54] You will need a Docker and DashMate tool installed.
[04:03] So the network I created via DashMate,
[04:08] so this is another mode of the DashMate
[04:12] that allows you to create a group of nodes.
[04:14] So yeah, let's try to do it.
[04:21] - While you're doing some things,
[04:22] I'll say a couple things as well.
[04:25] We talked about before the show,
[04:29] you are going to, right now,
[04:30] this documentation isn't anywhere public,
[04:34] but we're testing it right now.
[04:37] You've written up the steps.
[04:38] We're gonna test this documentation
[04:40] to see if it's kind of foolproof from start to finish
[04:44] so that anybody who can follow a recipe,
[04:47] make chocolate chip cookies,
[04:49] can also spin up a local development environment
[04:53] and start testing, yeah, working with Dash platform.
[04:57] So specifically, we are creating the nodes
[05:01] that would simulate the backend, the blockchain network.
[05:06] We're gonna create those on our own local computer.
[05:10] And specifically, you said four nodes.
[05:14] What are those four nodes?
[05:16] - Yeah, one seed node and three master nodes
[05:21] will create a small network
[05:23] that you can use to develop your things.
[05:26] - Okay, and then I didn't mean to do this if I did it,
[05:30] but I'm gonna add your,
[05:32] did you remove your screen share purposely?
[05:37] - Yeah, I just created a separate directory
[05:41] where I will run everything from scratch.
[05:43] - How about the font? - Okay.
[05:46] I have something running.
[05:48] I will stop it right now.
[05:49] Everything that I have.
[05:53] - And then, if you would, the font, if you would, please.
[05:58] - Like, make it louder?
[06:02] - Make it bigger.
[06:03] So, like, control plus or something should usually do it.
[06:06] - Ah, ah, like this?
[06:09] - Yes.
[06:10] Keep going.
[06:11] Yep.
[06:15] I think that's good.
[06:17] - Okay.
[06:19] So, yeah, so first step that you need to do
[06:24] is to download the Dash Mate.
[06:26] Don't remember if it's installed globally on my computer.
[06:30] I usually do it from development mode.
[06:33] We need to specify the version
[06:36] that we would like to install.
[06:38] So, right now it's dev.12,
[06:44] but, yeah, it's frequently changed,
[06:49] so we need to know exactly the version.
[06:53] You can get it from the platform explorer, by the way.
[06:56] - Yeah, and just so,
[06:59] I'm just looking at your documentation on the side
[07:03] while you're doing this.
[07:05] So, the instructions aren't 100% explicit
[07:09] for non-developers, but these three prerequisites,
[07:13] you install however you want to,
[07:16] but those steps aren't going to be explicit.
[07:18] Dash Mate, for example, you just installed,
[07:21] you installed it globally,
[07:23] so that would be different than installing it.
[07:26] So, is that necessary, or can you install it?
[07:30] - You can install the Dash Mate, whatever way you like.
[07:35] Like, it can be downloaded with the dev package.
[07:39] You can install it via npm.
[07:42] But on my local computer, I usually just run it
[07:46] with the Yarn, like, in development mode.
[07:48] So, I don't really install it globally, locally.
[07:53] So, let's see if we got this, we ain't got this.
[07:58] Wait a second.
[08:06] (keyboard clicking)
[08:09] Okay, let me check.
[08:26] - So, Dash Mate, for anybody who doesn't know,
[08:28] is a command line tool that helps you
[08:32] spin up Dash instances,
[08:35] instances of the Dash daemon running on your local network,
[08:40] or it also does, sets up nodes on testnet as well,
[08:45] as far as I know.
[08:47] - So, I don't know, something I haven't tested
[08:54] with my local command line, like the Dash Mate.
[08:58] So, I will show you from a development version,
[09:01] like, I will do it with the Yarn prefix,
[09:03] but the commands are the same, basically.
[09:06] You will just need to omit Yarn.
[09:08] So, the first step that we need to do
[09:13] is to ensure that we don't have any previous group setups.
[09:19] - Now, your screen share dropped again.
[09:24] Did you mean for that to happen?
[09:26] - Yeah.
[09:28] - Add it back.
[09:32] - I'll just screen share the...
[09:34] - Yarn Dash Mate setup.
[09:55] You can bump the font up again.
[09:57] - Yeah.
[10:00] - Okay.
[10:01] - You should be able to do it with a keyboard shortcut.
[10:11] It's usually Command +, if you wanna try that.
[10:14] - No, no, no, Control +.
[10:16] - Yeah, I guess you're using WebStorm,
[10:19] so I'm not sure where it is there.
[10:20] (keyboard clicking)
[10:23] - So, do you see, like, the font is good?
[10:39] Do you see it on the screen?
[10:40] - We see what you see.
[10:43] So, it's a little small for the viewers, I think,
[10:46] but if you can, yeah, if you can bump it up a little bit.
[10:49] If not, that's fine.
[10:50] It works.
[10:51] - Let's get it like this.
[10:52] - That's good.
[10:53] - So, yeah.
[10:59] So, the first, what we need to do
[11:02] is to set up our local network.
[11:05] We run Dash Mate setup local.
[11:07] And then, basically, hit Enter for each step
[11:12] that you ask, and then the defaults are good.
[11:15] - So, I saw that it's setting up miners
[11:19] and all sorts of things.
[11:20] - Yeah, right now, it creates a configuration,
[11:26] the Dash Mate configuration,
[11:28] creating configuration for the nodes,
[11:31] and creating the basic blockchain, like Genesys and stuff.
[11:36] - Mm-hmm.
[11:37] So, the last step that I see on the screen
[11:54] is configure SSL certificates.
[11:56] Is it still working on that, or?
[11:58] - Well, yeah, it will create the self-signed certificates,
[12:03] so no interaction is needed.
[12:06] - I guess it's working on configure tender-nodes.
[12:14] - Something with the core, I think.
[12:17] - Oh, I see.
[12:18] It's a little, I see the swirling fish there.
[12:21] Configure core nodes.
[12:23] - Oh, yeah, this step, I'm sure it's creating
[12:30] like some quorums and now registering master nodes.
[12:33] We can check it, by the way, what does it do.
[12:37] If we go through the logs.
[12:45] - Mm-hmm, you ran Docker, Docker PS, okay.
[12:49] - So, it's like we can see, yeah, some blocks are going,
[12:58] just right now, just right now.
[12:59] So, it should be good very, very soon.
[13:03] - And I'll also say, this is going to,
[13:11] so we've been doing our walkthroughs, right,
[13:14] with third-party developers just to get an idea
[13:19] of how it is working with Dash platform.
[13:24] And I think that we will probably incorporate
[13:29] setting up a local node because that's both educational
[13:33] and more reliable.
[13:35] So, that's why I kind of asked you to do this setup.
[13:39] - Here it is, here it is, it's done.
[13:43] So, after the setup is successful, we just start the node
[13:48] where dash my group starts.
[13:51] So, basically--
[13:53] - Can you press hide on that little bar at the bottom?
[13:57] Yeah.
[13:58] - So, basically, so, after setup is finished,
[14:04] you would probably want to start your group of nodes.
[14:11] So, instead of regular dash my start commands,
[14:15] which we use for full nodes, for our Evo nodes,
[14:20] here we use dash my group.
[14:21] So, it's a group is added in the comment,
[14:25] which tells dash my that you are manipulating
[14:28] with the group of nodes.
[14:30] So, we do dash my group start and see
[14:33] that services are starting.
[14:38] - Okay.
[14:40] - So, it will download all the images.
[14:44] The first start probably would take several minutes.
[14:48] So, depending on your connection,
[14:50] but the images of core services and platform services
[14:55] will be downloaded and cached locally.
[14:59] So, it's pretty fast to start and stop.
[15:02] - So, just to be clear, we've spun up three Evo nodes,
[15:07] not just master nodes, correct?
[15:09] - Yes, yes, yes, three HPA mints, three Evo nodes.
[15:15] - Okay.
[15:16] (mouse clicking)
[15:19] - So, yeah.
[15:28] - Now, you've got the platform explorer as well, I know.
[15:33] And are you able to configure running
[15:36] a platform explorer node and the indexing services
[15:40] that we went over in our last show,
[15:42] all of those services that you've built individually?
[15:46] Are you able to set it up so that these nodes can,
[15:50] so that that can run on this network?
[15:52] - I think this can be done.
[15:55] Like, if you want to set up a dash mate full node,
[16:00] then set up a platform explorer.
[16:02] I will think how we can make this together.
[16:05] - Yeah, even an inside server, that kind of stuff,
[16:08] all the infrastructure locally.
[16:10] - Yeah, yeah, yeah, good idea, good idea.
[16:13] So, as we can see, everything went fine.
[16:16] And, yeah, so right now the network has started.
[16:21] We can check it by doing docker ps.
[16:26] While docker ps, we can see that all containers is up
[16:30] and that status is up, they are running.
[16:33] So if anything is, went wrong with your configuration,
[16:38] you would probably see some errors,
[16:40] some restarting containers.
[16:42] You can go and check logs of this container
[16:45] if you want to resolve your errors.
[16:47] So you can just dig this up.
[16:49] Also, another way to check that your network is good
[16:56] is to make dash mate group status common.
[17:00] It will query each of the node
[17:04] and show the status of each of it.
[17:07] - Mm-hmm.
[17:07] - Yeah, we can see that everything is up.
[17:16] We have, we don't have platform blocks yet.
[17:20] I don't know why.
[17:23] Probably the version should be dev seven, I don't know.
[17:27] Because, so, but we will see, we will see later.
[17:33] We can also, can check the status of individual node,
[17:38] of individual local node.
[17:40] Like if you want to query just like a regular node,
[17:44] we can pass a config.
[17:46] For example, we want to check local one node.
[17:50] We can do German dash mate status
[17:52] and pass the config, it will pick up everything,
[17:55] pick up the configuration and show the status.
[17:59] So we can even check platform status of this node.
[18:03] We're passing the config flag.
[18:04] - Mm-hmm.
[18:06] - Okay.
[18:10] Okay.
[18:14] I wonder if chain is progressing.
[18:19] The platform chain, because the height is one.
[18:24] So let's check it live.
[18:31] - Yep.
[18:33] - So let's first check the logs
[18:36] of the tender dash container,
[18:38] because tender dash is the main component
[18:42] of the platform chain, like.
[18:44] Oh, I can see, I can see that the chain is progressing.
[19:02] We can see that some blocks are just finally coming in.
[19:06] So it seems that network is fine.
[19:11] It seems that the network is doing good.
[19:13] And as we can see, because we deployed three even nodes,
[19:18] it also spins up a free DAPI instance for you as well.
[19:22] We can see a DAPI here.
[19:29] And we can see that it deploys a DAPI at port 3,004.
[19:33] For example, 3,005.
[19:39] Or it should be different for each of them.
[19:42] Interesting.
[19:53] DAPI, IP.
[19:55] - Are these port numbers or what's the 3,000?
[19:59] 3,004?
[20:00] - Yeah, these port numbers are what you want to put
[20:04] in your dash SDK to make your client connect to.
[20:08] So as our network is ready,
[20:11] let's create a sample project, sample application.
[20:15] - Okay, right now you're just creating
[20:20] a new WebStorm code IDE project.
[20:24] So that's straightforward.
[20:26] - So what we want to do is first initialize
[20:30] our Node.js project.
[20:32] Just put everything as default.
[20:34] - So now we're working on the client side,
[20:36] but that's for people.
[20:38] We're building the client side application.
[20:41] Now we've got the backend spun up.
[20:43] We've got three, four nodes running.
[20:45] So that's acting as our backend.
[20:46] Now we're making a client side application.
[20:49] - Yeah, as we did npm init command,
[20:53] we can see that package.json file was created.
[20:57] Then we want to install our dash SDK dependency.
[21:03] We do it by npm install.
[21:05] Save and specify a dash SDK dependency
[21:13] with the version of the network.
[21:18] - Okay, and I see you're doing version 12,
[21:21] even though the latest release is not 12 yet.
[21:24] Any reason for that?
[21:26] The latest version of the SDK,
[21:29] or of the platform is dev.16.
[21:32] - Yeah, there is a reason for that.
[21:37] Wait.
[21:38] - Okay.
[21:40] - I think I'm, ah, it's one.
[21:43] Okay, it should be like that, I think.
[21:45] Yes?
[21:46] Wait.
[21:50] We can see this through the npm website, by the way.
[21:53] So we can just get to it
[21:56] and check what we have the versions.
[21:57] Yes.
[21:58] So basically, you need to specify a correct version
[22:02] of your dash SDK of your nodes, you know,
[22:04] and it has to be correct.
[22:07] From what I know right now,
[22:09] network is running on top of dev.12 version, not dev.16.
[22:14] Like dev.16 is the development version,
[22:15] but the network is running on the dev.12.
[22:18] And all testnet nodes are running dev.12.
[22:21] So we're picking dev.12.
[22:24] - Okay.
[22:25] - Ah, ah, I remember.
[22:26] It's 4.00 for some reason.
[22:30] I don't remember for what reason.
[22:31] - Yes.
[22:33] - Yeah, I forgot about that.
[22:35] - The SDK went to semantic versioning a while ago.
[22:40] And so we've been working with,
[22:42] actually, if you saw there,
[22:44] the latest, the quote-unquote latest version
[22:46] is still the three-point-something
[22:49] because four-point-something
[22:51] is considered the development branch still.
[22:54] - Yeah, so right now Node.js is downloading the dash package.
[23:04] Once it's installed,
[23:06] you will see the node models that it downloaded.
[23:09] And right now we can start creating our Node.js application.
[23:14] Let's start it by creating an index.js.
[23:17] - Okay, so you're going to create a Node.js application
[23:22] rather than a front-end browser-based application.
[23:27] Is that right?
[23:29] - Yeah.
[23:31] So where did I have this one?
[23:33] Yeah.
[23:40] - Okay.
[23:40] That seems--
[23:43] - I have, this read me, yeah,
[23:45] I have some code samples right here.
[23:47] So let's just copy that.
[23:50] This is just the basic application,
[23:54] basic frame of our application.
[23:56] So what it does,
[23:58] it creates a client,
[24:01] then syncs up to the network
[24:05] and gets you address to receive your dash on it.
[24:11] - And the important part here
[24:13] is that you're including in the configuration object,
[24:18] the DAPI addresses array that shows 1.27.0.1
[24:23] and then port 3001.
[24:27] That's the 1.27.0 is a local node.
[24:31] - Yeah, this should point to your local DAPI node.
[24:35] And right now I think it's incorrect.
[24:37] Let's check what do we have.
[24:39] I think, yeah, yeah.
[24:41] I think we want the port of the Envoy.
[24:43] So it should be 2,443, for example.
[24:48] So that's the port of the first DAPI node.
[24:52] - And is that, so you're choosing the Envoy port.
[24:57] Is that because Envoy does port forwarding?
[25:00] - Yeah, yeah.
[25:00] It's kind of gateway.
[25:02] So DAPI Envoy is the gateway of the DAPI.
[25:07] Yeah, so as I can see everything,
[25:11] except I haven't tested the DAPI addresses
[25:14] field of the options.
[25:15] So let's check how it's working.
[25:18] - Okay.
[25:20] - We type node index.js.
[25:23] Let's see.
[25:27] Yeah, I think the server does not implement the method
[25:35] get blockchain status.
[25:38] Yeah, I think, what versions do we have?
[25:41] So, yeah, I think the problem is because drive,
[25:49] because the versions does not really match.
[25:53] - So right now in the application code, you have client.
[26:01] - Okay, in that case, let's check.
[26:04] Let's try to match the versions.
[26:08] - Okay.
[26:10] Now, do you need to blow away your NPM lock file
[26:15] or should that?
[26:17] - No, no, it's fine.
[26:18] It's fine.
[26:20] - All right.
[26:20] Now I noticed in the application code
[26:23] that you weren't doing anything network related.
[26:25] It was all wallet creation.
[26:28] - Yeah, I will make it more clear
[26:30] why I changed the version
[26:31] because the versions of my node of local vault
[26:34] is zero one development
[26:36] and the latest version for it is dev 16.
[26:39] So I will set my version to dev 16 in my local application.
[26:44] - Okay.
[26:46] - In case of testnet network, it's dev 12 for right now.
[26:50] Okay, it's still failing.
[26:55] Let's check if it's picked up.
[27:01] We can see that by checking.
[27:04] Hmm.
[27:06] The version is weird.
[27:09] Let it develop.
[27:10] Ah, yeah, yeah, yeah.
[27:12] I think we should remove that.
[27:13] I think we should remove that.
[27:16] Okay.
[27:30] Hmm.
[27:31] Now it's dev 16.
[27:36] Hmm.
[27:42] Hmm.
[27:45] So it was recently rewritten,
[27:51] but I'm remembering which version.
[27:53] Hmm.
[27:57] Hmm.
[27:58] Which version should I pick?
[28:01] - For git blockchain status,
[28:05] where in your client code is it doing that call?
[28:09] Git blockchain status.
[28:11] Could you flip over to your index?
[28:14] - Yeah, yeah, you're right.
[28:16] I think I might need to check out different version.
[28:21] I think that's the reason.
[28:24] I think I should pick up dev 16
[28:26] because I'm running DashMate from this project.
[28:31] Since I was doing that from this one,
[28:43] maybe restart.
[28:45] Oh, we should supply a group in the middle of it.
[28:50] Okay.
[28:53] (laughs)
[28:56] Okay.
[28:56] Hmm.
[29:03] Okay, let's get back to it.
[29:19] Hmm.
[29:20] What do we do here?
[29:28] Okay, let's try to leave it like this,
[29:31] but let's try to reset the network.
[29:35] Maybe it will pick everything up.
[29:36] Let's get back to the version of the dev 12 here.
[29:44] (keyboard clicking)
[29:47] To reset, so you can always reset your network.
[30:05] There are two types of resets of your Dash local network.
[30:10] So you can do a soft reset and hard reset.
[30:13] Soft reset will just drop your blockchain
[30:16] and start it from the one, from the hate one.
[30:20] So it will just clean your data during restart the services.
[30:24] But hard reset, it will drop everything.
[30:29] It will drop all the conflicts,
[30:30] all the volumes, all the chains, you know?
[30:33] So we want to drop everything.
[30:35] So we put hard reset in it.
[30:40] - Okay.
[30:41] (keyboard clicking)
[30:44] - We can also put a force,
[30:46] so it will omit the check for running services.
[30:49] Okay.
[30:57] It cleaned everything.
[30:59] Okay, get me back.
[31:02] Let me get back to the recent 16 version.
[31:07] (keyboard clicking)
[31:10] - So you just checked out a different branch.
[31:18] What are you checking out?
[31:21] Is it for the DashMate code
[31:23] that you checked out a new branch?
[31:24] - Yeah, yeah, I'm just, I'm just,
[31:27] I just need to match the version of the DashMate
[31:29] version of SDK and the version of the platform services.
[31:33] They should all match.
[31:35] I had the DashMate dev 12 while had everything dev 16.
[31:40] So I need to match the DashMate as well.
[31:44] So we dropped the local network.
[31:49] Let's create it again.
[31:53] We do set up local as we did it in the first one.
[31:58] Okay, let's drop also.
[32:05] (keyboard clicking)
[32:08] - So the hard reset doesn't delete your configuration files?
[32:22] - Yeah, it seems so.
[32:23] Let's create the network again.
[32:29] I hope it doesn't fall.
[32:30] - Okay.
[32:32] (keyboard clicking)
[32:35] - Do you want to say anything
[32:37] about that withdrawals private key?
[32:39] I'm sure some people might be wondering about that.
[32:42] - I don't know.
[32:47] I think, yeah, well, I don't know.
[32:54] I haven't used that feature.
[32:55] Like I think withdrawals was turned off for quite a while.
[33:02] In the network.
[33:03] So in the test network.
[33:04] So I wasn't using, I wasn't testing this feature yet.
[33:08] - Okay.
[33:09] Let's go back to your documentation
[33:16] while we're waiting for that
[33:18] and see where we are in that process.
[33:22] - Yeah, so what I wanna show you next is we run our code.
[33:29] We get the address to receive funds.
[33:32] Then we can mint some coins,
[33:38] get some testnet coins in our local network
[33:42] on our generated address.
[33:45] And then we will make some transactions.
[33:48] We will send some dash.
[33:50] We will register an identity.
[33:52] We will create a data contract
[33:55] that will allow us to push documents, submit a document.
[33:59] And then query it back from the system.
[34:02] - Okay, now I didn't see any code for the minting part.
[34:06] Is that?
[34:07] - Yeah, there is just a comment,
[34:10] which is dashmate wallet mint, I believe.
[34:15] Stuff like that.
[34:24] - Okay.
[34:25] And if we typed in dashmate help,
[34:29] we would probably find--
[34:30] - Yeah, yeah, yeah, yeah.
[34:32] - Wallet commands.
[34:33] Okay.
[34:35] Do you wanna do that real quick
[34:42] just while we're waiting for that,
[34:45] showing what in a new tab, what dashmate help gives us?
[34:50] - Yeah.
[34:52] (keyboard clicking)
[34:55] So you need to pass a config.
[35:03] You need to pass a config pointing to the seed node
[35:08] because the master node doesn't really hold any dash.
[35:14] And we should supply an address through an address type.
[35:20] - Okay, but one step before that,
[35:23] so if you could bump up your font,
[35:25] you typed in yarn dashmate wallet mint.
[35:30] - Yeah, actually, I meant the yarn part
[35:35] because I used the development version of the dashmate.
[35:39] - Right, but if you just type dashmate dash dash help,
[35:43] will it tell you the different options?
[35:45] 'Cause I wouldn't know
[35:46] that there's a wallet mint command, for example,
[35:50] if I was just running this for the first time.
[35:52] So does it have a list of the main commands
[35:54] if you just type dashmate dash dash help?
[35:56] - I think so, I think so.
[35:58] Yeah, there is a wallet option.
[36:02] - Okay.
[36:03] - Wallet group of commands.
[36:04] - Now you put wallet in there
[36:05] and it gives you the subcommands for that.
[36:07] - Yeah, yeah, in each command we have subcommands, so.
[36:11] - Okay, so wallet only has mint as a command.
[36:14] - Yeah. - Interesting.
[36:15] - Yeah, yeah.
[36:18] So there's no wallet mint or anything like that yet.
[36:22] - Sorry?
[36:27] - Like I would have expected a lot more wallet command.
[36:31] - Yes, probably, probably, yeah.
[36:33] Maybe it's not the best place for this command, I don't know.
[36:38] - Let's check.
[36:39] - Yeah, let's check.
[36:40] It went good.
[36:43] bev16, yeah, the latest version.
[36:48] - Yes, I'm gonna throw up a question here.
[37:10] Question about Rust SDK later on.
[37:13] And Shenmik's opinion, are the steps needed
[37:17] to call Rust SDK with JavaScript
[37:19] using wasm-bindgen a difficult task?
[37:22] If not, how long does he think a dev would need to do it?
[37:25] - Sorry, could you repeat the question?
[37:28] - Yeah, it's on the screen also.
[37:30] But the question is, in your opinion,
[37:33] are the steps needed to call the Rust SDK
[37:38] with JavaScript using wasm-bindgen a difficult task?
[37:42] So in other words, is it gonna be difficult
[37:44] to use the Rust SDK in a JavaScript setting?
[37:49] - No, no, it will be the same.
[37:51] It will be mostly the same, all the code
[37:54] that we have right now, it will be all the same.
[37:58] It will just, under the hood, it will be calling the Rust,
[38:03] the wasm bindings.
[38:05] So, from developer's perspective,
[38:08] it will be the same SDK, with the same functions,
[38:10] with the same methods, but it will,
[38:14] underlying it, it will call the Rust bindings.
[38:17] So, from developer's perspective,
[38:19] there is nothing he should worry about.
[38:22] - There may be an added prerequisite, though.
[38:26] I'm not sure.
[38:28] That's something beyond my territory.
[38:30] But I'll also just show, (laughs)
[38:35] Michael Klestrick says, "Docker plus Node
[38:37] "equals hell on Earth."
[38:38] So, I'll take that.
[38:40] - Okay, okay, we got our network started.
[38:45] Let's just make a quick check that it is working.
[38:48] Don't forget growth.
[39:02] So, let's try to run our snippet.
[39:06] - Did that stage show the version that they're running now?
[39:11] - What?
[39:15] - Did the Docker group just press up
[39:19] and to run that same command again?
[39:21] Yeah, here we go.
[39:23] - We have some errors, though.
[39:26] (keyboard clacking)
[39:29] - Chain lock quorum size.
[39:38] Okay, what does it mean?
[39:42] I don't really know.
[39:46] Okay, let's try to reset it.
[39:51] Let's try a soft reset.
[39:52] Maybe it will pick everything.
[39:54] Ah, I think I know.
[39:56] Maybe we should update everything,
[39:59] every images that we have.
[40:01] Since we have a zero, like a tag in our images,
[40:06] it will probably have outdated packages in my Docker.
[40:11] So, I will run a dash mate update command.
[40:14] - And what's that updating?
[40:18] - Sorry?
[40:25] - What is it updating, dash mate update command?
[40:30] - It's updating the images of the services
[40:32] to the latest images.
[40:35] So, all the images, for example,
[40:38] if we have updates of the components,
[40:41] of the drive components, and we have a tag,
[40:45] it will always pick up the latest version.
[40:47] So, when you, yeah, as we can see,
[40:50] we have drive outdated in Appia.
[40:53] So, probably that was the reason why it was failing.
[40:56] Let's try to reset it now.
[40:59] - So, is that contacting Docker's hosted images?
[41:04] - Yeah, yeah, yeah, exactly.
[41:05] - That UPG uploads periodically new versions
[41:09] of the Docker images, and it's contacting Docker Hub?
[41:14] - No, it's calling the local Docker.
[41:18] So, it's updating the images of the local Docker,
[41:21] in your local Docker storage.
[41:25] - Okay.
[41:25] - So, let's see if it works.
[41:32] It should work.
[41:39] We did a lot to make this work.
[41:45] - So, what is your summary
[41:48] of what went wrong the first time?
[41:51] Was it because we were on a different--
[41:53] - Everything is about the semantic versions.
[41:58] So, it's not good.
[42:02] The semantic version that is used,
[42:05] like there are different versions
[42:06] in the different development versions,
[42:08] and you have to know which version should you use,
[42:11] and you should combine this version in proper order,
[42:15] you know?
[42:16] - Yeah.
[42:17] - All of your tools have to be correct version.
[42:21] - But specifically, in order to get the version of DashMate,
[42:26] was that you switched the DashMate branch in the repo?
[42:33] - Yeah, I switched it to the version tag.
[42:39] So, every time a platform version is out,
[42:41] it also tags a git commit.
[42:44] So, I just check out this git commit,
[42:47] and I run comments on top of it.
[42:50] - Okay, so that's just one of those things
[42:53] that we should make note of,
[42:54] and make sure that the documentation has--
[42:56] - Yeah, probably, most likely you don't need this step,
[43:03] because when you install DashMate separately,
[43:07] not like me, I'm using it like a dev version,
[43:09] like through the platform code,
[43:13] from the platform monorepo,
[43:14] but usually, you use it from the command line,
[43:18] so you install DashMate via npm,
[43:20] or by downloading it with the dev package.
[43:24] So, you probably don't need this step.
[43:29] You just need to make sure your DashMate
[43:31] is correct version.
[43:33] - Okay.
[43:35] - Okay, let's start our group of nodes.
[43:42] And let's hope this time it will work.
[43:47] - Starting a minor.
[43:54] - Uh-huh.
[43:57] - Okay.
[43:57] - Okay, let's wait until it start fully.
[44:09] What command status?
[44:14] Let's wait until we see that the chain is progressing.
[44:22] Still error.
[44:29] I don't see any errors.
[44:34] Probably need some time to get up.
[44:38] (mouse clicking)
[44:41] Yep.
[44:51] Ah, no.
[44:52] Not yet, not yet.
[44:53] - You're looking at the platform status
[44:57] that's showing an error.
[44:58] The platform container is fine.
[45:01] What was the thing above it?
[45:03] - Okay, let's...
[45:05] - Yeah, actually--
[45:05] - The core is running fine, it looks like.
[45:08] It's just platform that's not.
[45:09] - Yeah, but let's check if DAPI is actually working.
[45:15] We need to check DAPI.
[45:20] Okay, cannot connect to something.
[45:32] The TenderDash is not there.
[45:36] TenderDash, TenderDash, why do you?
[45:39] - So I've noticed just recently in the past two
[45:45] or three days that a new release for TenderDash dropped
[45:50] and it's the actual 1.0.0 version of TenderDash
[45:56] and the Rust ABCI, TenderDash ABCI.
[46:01] Those both got promoted to version 1.0.0 just one day ago.
[46:06] So I'm not sure if that might be anything related to--
[46:14] - Right now, there is no chain locks yet in the system.
[46:18] So we need to wait for chain locks.
[46:21] I don't know why chain locks,
[46:22] why there is no chain locks.
[46:26] - Which would be a core.
[46:30] - That's a core function.
[46:31] So that's interesting.
[46:33] - Let's check if the master node is actually working.
[46:45] It's working.
[46:47] Oh, okay.
[46:52] I think this is just hold up.
[46:57] Yeah, yeah, yeah.
[46:59] We just need to wait a little bit more.
[47:01] Okay, okay.
[47:04] Okay, I think this one is working.
[47:05] Okay, right now we should see that the DAPI is working.
[47:12] Yeah, it got up.
[47:16] So right now we should see that the network is up
[47:22] and we can fire some requests in the DAPI.
[47:29] Yeah, yeah, all good.
[47:32] Okay, let's hope that this will work.
[47:37] Oh, it's working, it's working.
[47:41] So yeah, we got every version matching
[47:46] and that made our services working.
[47:53] I supplied a local DAPI instance of our local network
[47:58] in the DAPI addresses field.
[48:00] It also worked and got us an address.
[48:03] Okay.
[48:05] - Can you tell us again real quick before you leave that,
[48:08] tell us again what the address is
[48:11] that you're connecting to and why that's important.
[48:15] 'Cause you said before,
[48:16] you're not connecting directly to a node,
[48:17] you're connecting to a gateway.
[48:21] - Yeah, so right now we have a small network
[48:25] consisting of four nodes, which creates a small network,
[48:30] a separate network from the testing, a local network.
[48:33] So you can connect to it with your dash SDK, for example.
[48:39] And to do that, you connect to the DAPI address and port,
[48:48] which is of your local node.
[48:53] So you just put it in your configuration of the dash SDK.
[48:56] - Okay.
[48:58] - So you can connect to it.
[49:00] So basically it connects your SDK to your network,
[49:06] to your local network and you can do stuff there.
[49:11] You can send transactions, make documents
[49:14] and stuff like that.
[49:16] So right now we have an address.
[49:19] We'll put a seed phrase in it.
[49:21] And this address is the first address
[49:23] of our seed phrase in our network.
[49:26] So there are no transactions in the network yet.
[49:32] - So you would need some funds minted to that address.
[49:36] - Yeah, exactly.
[49:37] To do that, we first need to stop our network
[49:43] because while it mint comment requires you to do that
[49:46] on the stop network.
[49:47] I don't know why.
[49:48] - Okay.
[49:49] In theory, the miners are getting paid
[49:55] for mining the dash, right?
[49:57] So you could in theory have send from a miner
[50:02] to your node, right?
[50:06] To your wallet rather, but instead you were deciding
[50:10] to just mint it to yourself.
[50:12] - Mm-hmm, mm-hmm.
[50:13] - Okay.
[50:14] - The network itself, by the way,
[50:18] a rack test if anyone wonders.
[50:20] So it means that the blocks are getting created
[50:25] on the transactions that is there constantly.
[50:30] So it's not like anything is mining here.
[50:33] There is no miners in this network.
[50:35] It's just programmatically just create blocks.
[50:38] - Right, meaning that the C++ dash node,
[50:43] the core blockchain is running in reg test mode,
[50:49] the core chain.
[50:50] - Yeah, so we stopped our network.
[50:55] Let's try to mint some coins.
[51:00] We need to pass a seed node as a config value here
[51:04] and also pass an address where we want our funds to receive.
[51:09] Let's get it from our,
[51:14] this was our address.
[51:20] I think it broke because I stopped the network.
[51:24] Then we pass it here and check if missing.
[51:32] Ah, and you also need to specify amount
[51:34] of this that you want.
[51:36] For example, 100.
[51:37] That should be fine.
[51:38] Oh, what an animation, I really like that.
[51:45] Oh, this looks good.
[51:50] (laughing)
[51:52] Okay, now we can stop the network back.
[51:58] - What exactly did you stop?
[52:00] When you said group stop,
[52:02] you stopped all the nodes from running.
[52:04] - Yes, yes, yes.
[52:05] - So how do you mint, how does a network mint coins?
[52:10] - I don't know how this comment is working.
[52:13] I think it could be optimized,
[52:15] but basically it starts the network,
[52:19] minting and stopping it again.
[52:22] I don't know why you need to stop
[52:24] and start your network every time,
[52:27] but maybe this comment could get optimized.
[52:29] I don't know, just it was made like that.
[52:32] Yeah, so let's hope everything will start flawlessly.
[52:41] Okay, we also need to wait until everything's picked up.
[52:59] Let's check by the drive again,
[53:01] by the DAPI, the logs of DAPI we need.
[53:28] 30 seconds.
[53:29] Well, I don't know, probably it's good.
[53:33] Okay, let's check for the code.
[53:35] Let's check it for the code.
[53:38] So it should change the address
[53:42] if the funds was received with our previous address.
[53:46] So it should show us the next address.
[53:48] So let's just run this over again.
[53:51] - Okay, and you're doing that.
[53:56] - We can see that the address has changed.
[53:58] That means that some transactions
[54:03] went through our seed phrase.
[54:05] - Okay, and the other way to do that,
[54:07] to check that would be if you were to spin up an insight
[54:11] or a block, let's see, what's your node?
[54:16] - Sorry, what do you mean?
[54:22] - Oh, I was just saying most people wouldn't think
[54:25] to check to see if the HD wallet generation
[54:28] had moved from one to two to see if the address had.
[54:33] - Yeah, let's check the balance.
[54:36] Let's actually check the balance of the wallet
[54:38] so we can ensure that we received.
[54:41] Let's add the balance in the log.
[54:44] And also we need to request address.
[54:54] Checking the balance.
[54:55] So we get the total balance, balance is the number.
[55:01] So I think it should show us.
[55:03] Yeah, here it is.
[55:11] We have more than 100 Dash in our pocket.
[55:18] Okay, then we can start making some transactions.
[55:24] Let's try to send a basic, regular core transaction.
[55:29] - Okay.
[55:31] - Just to see if it's working.
[55:34] So as a recipient, we can use our address.
[55:39] So let's fire some Dash.
[55:45] I haven't tested this snippet,
[55:52] but I think it should work.
[55:54] We will fix the errors if we don't.
[55:57] Main relay fee, not map.
[56:07] What options can we supply?
[56:20] - Deduct fee.
[56:21] - Yeah, you'd think that would be a default option, right?
[56:28] - Yeah, something is not good with the fees.
[56:31] I don't know.
[56:32] That's probably an SDK problem.
[56:35] - Yeah.
[56:36] - So let's try if we can just please deduct fee.
[56:40] That will work.
[56:45] Oh, there is a typo.
[56:49] (keyboard clicking)
[56:52] - I don't think that this one is,
[57:01] we could probably move on to the next one.
[57:03] - Okay.
[57:04] - Just to see if the platform is running,
[57:05] 'cause that doesn't require.
[57:07] - Okay, okay, yeah.
[57:09] Yeah, you're right.
[57:10] So once we want to play some platform stuff,
[57:14] first of all, what we need to do is to create an identity.
[57:18] So identity is like an account in the Dash platform
[57:23] where you have all transactions,
[57:27] all the documents, data contracts,
[57:28] and all the stuff associated with it to register.
[57:33] - Can I ask some follow-up questions on that?
[57:36] 'Cause I get the question a lot in our walkthroughs.
[57:38] What is an identity?
[57:40] What is it?
[57:42] What is an identity?
[57:45] Not using an analogy, what is it actually?
[57:48] - Um, well, identity is a resource,
[57:53] like the same, like we have data containers,
[57:57] we have documents, and we have a lot of stuff in RhoDB.
[58:00] So technically, it's just the same as everything
[58:05] in the Dash platform.
[58:06] But you can think of it like an account in Ethereum
[58:14] where we have account and we have transactions linked to it.
[58:18] So it's basically like the similar,
[58:23] like you can have an identity,
[58:28] and you have everything in the network associated with it.
[58:32] Like you can have names, you can have data contracts,
[58:35] you can have documents that you put
[58:38] in the data contracts, they will be also linked to it.
[58:41] For example, if you have an NFT,
[58:44] you will be also an owner of NFT.
[58:49] So a specific identity will be an owner of NFT,
[58:54] of a document, of a data contract, whatever.
[59:00] - The answer that I've been giving people,
[59:02] which I'm not sure if it's correct,
[59:04] but the answer that I've been giving people
[59:06] when they ask that is that it's a public-private key pair.
[59:11] Is that true?
[59:12] Because when you get the identity back--
[59:16] - Not exactly, I think not exactly
[59:19] because the system allows you to add or remove,
[59:22] so there is a, so you can associate different public keys
[59:27] with the same identity identifier.
[59:30] So that means that you can have different public keys
[59:35] associated with identity.
[59:39] And different keys could be removed,
[59:42] could be added to you, you know?
[59:44] So it's not like exactly that way, but--
[59:49] - Okay, that's something I guess I'll dig into myself
[59:53] later on to satisfy my own curiosity.
[59:56] - Okay, yeah, let's try it to create an identity,
[60:01] an actual identity in our network.
[60:07] (mouse clicks)
[60:09] So to do that, we call client-platform-identities.register.
[60:16] It return you identity instance object.
[60:22] There are some methods to get an ID.
[60:24] You call get_id and then make a toString on it.
[60:28] So right now we have an identity.
[60:32] Okay, the next step that you probably would like to do
[60:37] is to create a data contract, right?
[60:39] Let's create it.
[60:45] So what we are going to do is we get our identity
[60:51] via identifier, this is different common than the register,
[60:56] but similar.
[60:57] So this line will get the identity
[61:02] that we received in our previous step.
[61:06] Instead of register, we just retrieve it.
[61:08] Then we can create an example data contract.
[61:14] This is just a Hello World application
[61:16] that will allow us to put messages in the Dash blockchain.
[61:23] Yeah, we created the contracts,
[61:28] I created client-side and then you can publish it.
[61:32] So it's a separate steps.
[61:33] First, you create a contract and then use it
[61:37] and publish it through the SDK.
[61:40] - I noticed the contract creation line,
[61:45] that's a client, that's not an asynchronous function.
[61:48] So that means to me, it's just creating this client-side
[61:51] and then it's- - Yeah.
[61:54] But probably, might be also a bit is missing in this,
[61:59] I don't know.
[62:00] I don't remember exactly, but we will see now.
[62:03] - Yeah.
[62:04] - Yeah, so I used previous identifier.
[62:11] Oh, yeah, probably I need to add an await right here.
[62:16] It just throws me a schema error
[62:21] because I don't have position in the property.
[62:35] There is a, it was taken from the documentation,
[62:38] but it's not quite right.
[62:39] The position should be right.
[62:41] - We've run into that issue before.
[62:42] - Yeah, yeah.
[62:44] - And then maybe the await didn't need to be there
[62:49] after all, but I don't know.
[62:54] - Now, what should we?
[62:57] - You added an await on the contract creation part.
[63:03] - Let's compare it with the dash pay.
[63:05] I think it should give us the exactly what we need.
[63:10] What we need.
[63:11] Index, document type, what we have.
[63:24] We have node, we have properties message.
[63:31] I think we can just import it.
[63:35] Let's try to do that.
[63:39] (mouse clicking)
[63:42] Interesting.
[63:50] Okay, let's make it from scratch.
[64:07] We had node, I remember, then message field.
[64:12] So, maybe type object is missing.
[64:19] I don't see it here, yeah.
[64:24] - You had type string, but yeah, I don't know.
[64:31] - I had type string on this one,
[64:34] but also type object is missing.
[64:37] Okay, let's check once again.
[64:40] Seems something is working.
[64:47] Yeah.
[65:05] - It's not that fast though.
[65:06] Everything is up.
[65:31] I'm gonna go to the tutorial
[65:35] that we've been doing with Anthony
[65:37] to see if that platform identities create
[65:41] is actually asynchronous.
[65:43] - I don't know why it's stuck.
[66:00] - Let's try once again.
[66:02] Oh, here we have.
[66:10] So, we registered the contract
[66:12] and here we can see the ID of our contract.
[66:17] - Let's see.
[66:22] - So, it worked, it worked.
[66:25] - So, it worked.
[66:26] - Yeah, so it worked.
[66:27] Great, yeah.
[66:30] So, next step, what we want to do
[66:32] is we want to push some documents in our data contract.
[66:37] - Yeah.
[66:40] - So, what we need to do
[66:45] is we need to add one more option in our client.
[66:50] So, in the options, there should be an applications field
[66:57] which will list the contract ID of our application.
[67:01] So, we can push data in.
[67:03] So, this is a required step.
[67:06] So, here where we construct the dash client,
[67:11] we need to insert our created data contract.
[67:14] Then we can insert an info unit,
[67:22] some data in it.
[67:26] Let me copy that, this one in our application.
[67:31] Let's replace data contract creation
[67:38] with a document creation.
[67:39] So, what we do is we create a document
[67:44] through the create function.
[67:46] We specify the type of the document
[67:49] that we want to create in our case,
[67:52] it's Hello World application
[67:54] that we specified in our dash client.
[67:56] And also the note, the type of document that we created.
[68:03] Let me show you.
[68:08] Like this one.
[68:11] It should be, this is our document type.
[68:16] So, we put it together.
[68:18] We put hello world dot note.
[68:21] Hello world is our data contract,
[68:23] note is our document type.
[68:25] We also pass an identity
[68:28] from which we want to push the documents from.
[68:33] And we supply document data.
[68:36] In our case, it's Hello World message.
[68:38] Yeah, we also, then we create a batch
[68:45] and insert a document inside of it, like this.
[68:51] So, only one document per one transactions
[68:56] is currently unloaded in the network,
[68:59] but theoretically it can be increased,
[69:02] the number of documents that can be supplied in the batch.
[69:05] Yeah, so let's check how it's working for us.
[69:10] So, we have a document.
[69:14] I think we also want to see a document ID
[69:16] in case everything went fine.
[69:19] So, we get hello world document, we have ID,
[69:22] and toString, I think that should work.
[69:25] - Can you scroll up a bit on your code?
[69:27] - Yeah.
[69:28] - No, the other way, yeah, just scroll up.
[69:32] - So, first we get the identity
[69:36] that we created in the first step.
[69:39] Then we supply a command for creating a document
[69:44] for which you need your Hello World application,
[69:48] which we set here.
[69:51] And also the type of your document.
[69:55] Then you supply identity
[69:57] and the actual data that you want to put.
[70:00] Then you create a batch object,
[70:03] which supplies what you want to do
[70:06] with your document created.
[70:07] Maybe you want to replace your document or even delete it.
[70:11] And then you broadcast in the network.
[70:13] Then we get the ID for broadcasting with good.
[70:16] - Okay.
[70:18] (mouse clicking)
[70:21] - Oh, we don't have enough balance on our identity.
[70:30] Good, then we might want to...
[70:35] (indistinct)
[70:38] Yeah, we need to do some top-up.
[70:39] I haven't expected that.
[70:42] (laughing)
[70:47] So, what we need to do probably is just
[70:49] to make client platform identities.topup,
[70:54] which accept, I don't know, what it accept.
[70:59] Let's check in the documentation.
[71:03] Identities, topup.
[71:07] Topup receives a document ID, identifier, and the amount.
[71:15] (mouse clicking)
[71:18] So, it should be something like,
[71:24] I don't know how much credits should I top up,
[71:27] but let's just...
[71:29] So, we have commented out, I think.
[71:32] Okay, I think we're fine.
[71:35] I think it should be good.
[71:37] I was just...
[71:42] (mouse clicking)
[71:45] There you go.
[71:49] I pasted some code in the private chat.
[71:53] - In the Discord?
[71:56] - Yeah, in StreamYard.
[71:57] This is...
[72:02] Yeah, that's from Anthony's tutorial.
[72:06] This part has been working for us regularly.
[72:10] (mouse clicking)
[72:12] Identities, IDs.
[72:17] So, basically...
[72:19] (mouse clicking)
[72:24] Ah-ha!
[72:25] (mouse clicking)
[72:38] - So, we need to make it a sled, I think.
[72:41] - That should be better, but...
[72:44] (mouse clicking)
[72:50] - Mm-hmm.
[73:07] (mouse clicking)
[73:10] - I like it.
[73:13] I need this more.
[73:14] Just to keep it clean.
[73:17] Okay, let's check.
[73:20] I don't know if there was something with the asset locks.
[73:23] I don't know.
[73:24] Oh, it actually worked.
[73:30] Cool, cool.
[73:31] Thank you, Ryan.
[73:32] Okay.
[73:37] So, let's get back to our document.
[73:42] Let's check if we can post it right now.
[73:48] Yeah, yeah.
[73:55] So, it successfully broadcasted our document,
[73:59] and we can see its ID in the log.
[74:06] Yeah, so, the last step that I wanted to show you
[74:11] is how to query back from the system.
[74:14] So, at this point, we submitted a document
[74:17] in the Dash Platform Network.
[74:19] Now, we can query it back in our SDK.
[74:23] To do that, we have a code sample.
[74:27] We have a code sample.
[74:35] So, yeah.
[74:38] Dash Platform allow you not just simply post your data
[74:45] in the blockchain.
[74:46] It allows you to make some complex queries.
[74:49] So, in this one, I will show you how to get
[74:53] all the documents that matches the specific message.
[74:58] Okay, let's see what we have.
[75:03] (keyboard clacking)
[75:06] To do that, we specify our application,
[75:16] our Hello World and Node document type,
[75:20] and supply a query options,
[75:22] where you specify query language.
[75:27] And this is GrubDB query language, I believe.
[75:32] Yeah, let's run it.
[75:34] - Once upon a time, I thought that I heard something
[75:44] about SQL query language being supported,
[75:48] rather than, you know, this right in the SDK.
[75:54] Do you know anything about that?
[75:56] - Sorry?
[75:57] - Is SQL supported for GrubDB?
[76:02] Do you know?
[76:05] - No, no, no.
[76:07] There is a specific GrubDB query language
[76:09] that you should use.
[76:10] I didn't work much with it, but what does it say?
[76:19] Query must be for valid indices.
[76:22] We have no index on the message.
[76:26] So probably we can't use this feature
[76:29] to retrieve the document.
[76:31] So let's check how we can get it another way.
[76:35] Just simply, where...
[76:40] I guess we can just omit where,
[76:50] and get all of the documents.
[76:55] - I'm looking for how we did this part.
[76:58] - Oh, it's actually returning this stuff.
[77:07] With the empty query, it's returning all of the documents
[77:12] that system has.
[77:23] What, we can do something for this?
[77:25] All right, what do I type?
[77:34] Oh, shit.
[77:46] I see.
[77:52] - I can drop another code block for you if it helps,
[77:56] but I think you're on the right track.
[77:58] - Yeah, yeah.
[77:59] It's the same document that we processed previously.
[78:04] BYK1.
[78:05] Yeah, so this is how we work with it.
[78:11] And yeah, there was a query,
[78:15] which allows you to make some queries.
[78:21] But in order for this functionality to work,
[78:24] we had to insert an index of the message
[78:29] inside the data contract.
[78:32] So the system will prepare an index,
[78:35] and then we could use this complex queries.
[78:39] - Yeah.
[78:44] - Yeah, so.
[78:47] Now, we got quite a ways here.
[78:52] The main thing that I wanted to show here in this show
[78:55] was how to set up the local network.
[79:00] So we went beyond that.
[79:03] So this is great.
[79:04] This is going to help developers, I think a lot,
[79:07] to be able to just test against their own local network.
[79:10] So, and by the way, Michael Cluster says,
[79:13] "Yes, some of the SQL standard is implemented in platform,"
[79:16] which is great to hear because there's nothing worse
[79:19] than things, query languages that are not standardized.
[79:24] So I'm glad to see that we're working towards that.
[79:29] - Yeah, so basically, that's it.
[79:32] We have a local network that is running on our local machine
[79:38] and we can work with it separately from the network.
[79:43] One thing I wanna note is that if you have a laptop,
[79:46] so when you close your laptop,
[79:51] it doesn't work really stable.
[79:52] So every time you go from the sleeping,
[79:56] if your computer went to sleep,
[79:58] so you should check all of your services, restart them,
[80:02] and ensure that all of the services are working correctly
[80:05] before you start doing your code.
[80:07] - Great.
[80:09] All right, so like we said at the beginning,
[80:12] we're going to refine this,
[80:14] the steps in the tutorial, the documentation.
[80:17] I would love to see it in the main documentation
[80:21] at some point in the actual docs.dash.org site.
[80:26] But before that, you mentioned
[80:29] that you might be putting up a medium post
[80:32] so that it can be found and indexed.
[80:37] - Yeah, I will turn this quick start
[80:39] that I just composed into an article
[80:43] so the people on the internet will be able to read it
[80:47] and follow all of the steps if they want to.
[80:52] - Is this your owl guy?
[80:53] I think you've been working with him, right?
[80:57] - Ah, yeah, yeah, yeah.
[81:00] - He says hello.
[81:01] So yeah, thank you for everybody for tuning in.
[81:04] Thank you, Mikhail, for preparing this tutorial.
[81:08] This will help a lot, like I said.
[81:10] And we will see you next week, I guess.
[81:15] I was trying to remember what we have planned for next week,
[81:20] but I don't think it's finalized yet.
[81:22] So we'll see you next week.
[81:24] We'll probably be on Monday next week as normal.
[81:27] So thanks again, Mikhail, and everybody else.
[81:30] - See you around.
[81:31] Bye.