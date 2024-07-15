---
showLink: "https://www.youtube.com/watch?v=Dpn0GK-74BQ"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Platform Terminal User Interface | Incubator WEEKLY"
publishDate: "2024-07-08"
coverImage: "https://i.ytimg.com/vi/Dpn0GK-74BQ/sddefault.jpg?v=668be532"
---

## Episode Description

The episode explores the Platform Terminal User Interface (TUI), a tool for interacting with Dash Platform, covering its setup, features, and future development plans.

## Episode Summary

In this episode, Paul from Dash Core Group's Research and Development team demonstrates the Platform Terminal User Interface (TUI), a powerful tool for interacting with Dash Platform. The discussion covers the setup process, including cloning the repository, installing dependencies, and configuring the environment. Paul showcases various features of the TUI, such as managing wallets, registering identities, creating and running strategy tests, and querying contracts. The conversation also touches on the DashPay.io contract creator, fee structures for Platform operations, and future development plans for the TUI, including improved documentation and additional features like contract registration without strategy tests.

## Chapters

00:00 - Introduction and Overview of Platform TUI

This chapter introduces Paul from Dash Core Group's Research and Development team and sets the stage for exploring the Platform Terminal User Interface (TUI). Paul explains the motivation behind the TUI and its potential for helping users interact with Dash Platform. The discussion highlights the recent renaming of the tool from "Platform Explorer" to "Platform TUI" to avoid confusion with other similarly named tools. This introduction provides context for the detailed exploration of the TUI's features and setup process that follows.

06:35 - Setting Up the Platform TUI Environment

In this chapter, Paul walks through the process of setting up the Platform TUI environment. He explains how to clone the repository, install dependencies like Rust, and configure the necessary environment files. The discussion covers the use of Docker for running a local network, highlighting the differences between using DashMate and the yarn setup process. Paul demonstrates how to obtain the required credentials and private keys for connecting to the local network. This section provides valuable insights for developers looking to set up their own Platform TUI environment for testing and development purposes.

27:21 - Exploring Platform TUI Features and Navigation

This chapter delves into the various features and navigation options within the Platform TUI. Paul demonstrates how to use keyboard shortcuts to navigate through different screens, including wallet management, identity registration, and contract interactions. He explains the process of refreshing wallet balances, registering identities, and interacting with contracts. The discussion also covers some of the challenges encountered during the demonstration, such as issues with identity registration, highlighting the ongoing development nature of the tool. This section gives viewers a comprehensive overview of the TUI's capabilities and user interface.

43:40 - Using DashPay.io for Contract Creation

In this segment, Paul showcases the DashPay.io website, a tool he developed for creating Dash Platform contracts using AI. He demonstrates how to use GPT-4 to generate a contract based on a simple description, and then walks through the process of validating and refining the generated contract. Paul explains how to copy the resulting contract and import it into the Platform TUI for use in strategy tests. This chapter highlights the integration between different tools in the Dash ecosystem and demonstrates how AI can be leveraged to simplify contract creation for developers.

54:13 - Advanced Features and Future Development Plans

The final chapter covers some of the more advanced features of the Platform TUI and discusses future development plans. Paul demonstrates how to fetch system contracts, perform document queries, and interact with NFT features. He also touches on upcoming features like masternode voting. The discussion then shifts to the roadmap for the TUI, including plans for improved documentation, the addition of direct contract and document registration without strategy tests, and ongoing work on fee structures for Platform operations. This segment provides insight into the future direction of the Platform TUI and its role in the broader Dash ecosystem.

## Transcript

[00:00] And we're live.
[00:03] Welcome.
[00:05] >> Yo.
[00:07] >> Hello.
[00:09] >> Okay.
[00:11] Welcome, everyone.
[00:13] Today we have Paul with us from research and development at Dash Core Group.
[00:21] Welcome, Paul.
[00:23] >> Thanks for having me.
[00:25] >> Yep.
[00:27] I -- as we've been going through the Dash platform walk-throughs, I've wanted another tool to be able to help us cross-check our work.
[00:39] And I think -- I've been very impressed with the presentations that you've given on the Dash Core Group calls.
[00:49] And with the tool that you have, the platform, the terminal user interface.
[00:53] And I've wanted to use it for a while, but I've been staring at an empty README file for a while.
[00:59] So I didn't know how to get started.
[01:01] So I wanted to bring you on to show us how you use this tool.
[01:07] >> Okay.
[01:09] Sure.
[01:11] Yeah.
[01:13] That's all I've been working with for -- I mean, mainly all I've been working on and working with for the past few months.
[01:19] It's an awesome tool.
[01:21] And it allows you to do anything that you can do pretty much on platform.
[01:27] So, yeah.
[01:29] I think it's definitely something that we should showcase here.
[01:33] >> Yeah.
[01:35] So I think we should just jump right in.
[01:37] Anthony, did you have anything to say before we get started?
[01:39] Or should we go ahead and jump right in with Paul's demo?
[01:43] Do you have your screen share available, Paul?
[01:45] >> We tested that, yeah.
[01:47] So the one thing I was going to say is Paul also made something that I thought was cool, which was the data contract creator site,
[01:54] where you can use chat GBT to create, like, a dash contract.
[01:58] >> Dash pay.io.
[02:00] Yeah, I haven't used it yet.
[02:02] So if we want to -- I don't know if we're going to use that today.
[02:05] But we've shown it before.
[02:07] But I don't think we've used it.
[02:09] And I just wanted to also note that it looks like you're coming at us from Sam's house.
[02:15] Is that right, Paul?
[02:16] >> Yeah, yeah.
[02:18] I'm sleeping on the couch here.
[02:21] >> Nice.
[02:23] And he's jamming on the piano, I'm sure.
[02:26] Now, I've seen the background somewhere else.
[02:29] It must be one of those stock ones or something.
[02:32] >> Yeah.
[02:34] >> Anyway, yeah, let's jump in.
[02:36] >> Yeah, okay.
[02:38] Should I share my screen then?
[02:40] >> Yep.
[02:42] >> Okay.
[02:44] So you are kind of interested in how to set it up, right?
[02:49] >> Yeah, yeah.
[02:51] I'd love to be able to set it up and run it using either a local network or test net.
[02:58] And then even main net when that comes.
[03:02] And I'd also like to -- did I notice this morning that the repo has been renamed?
[03:09] Or am I crazy?
[03:11] >> Yeah, we just renamed it.
[03:14] We've been talking about it for months and finally poked Sam and Yvonne enough today to rename it for this podcast.
[03:25] >> Okay.
[03:26] Excellent.
[03:28] So because before we had a little bit of a namespace issue, as they say in the software world,
[03:35] where we had two tools that were completely different called Platform Explorer.
[03:41] One was a web app, is a web app, that Mikhail Chen has made that gives us the ability to look into platform through a web user interface.
[03:52] And then now we have -- what are we calling it now?
[03:57] >> Now we have Platform TUI.
[04:01] >> Okay.
[04:02] And TUI stands for?
[04:05] >> Terminal User Interface.
[04:08] So we got the name correct, Platform Terminal User Interface, the name of the episode.
[04:13] >> Yeah.
[04:14] >> Great.
[04:16] >> Yeah, so just for anybody who's not really into this stuff, the terminal is just -- do you want to explain that, either one of you?
[04:26] >> Oh, that's all you?
[04:27] >> I think everybody knows what a user interface is, but terminal user interface --
[04:31] >> It's how you speak to the machine.
[04:33] It's the way you speak to the machine.
[04:35] You speak directly to it, not box representation of it.
[04:41] >> Yeah, so there's this subtle distinction between a shell and a terminal.
[04:46] And, you know, I'd probably not do it justice to describe the difference there.
[04:51] But the main difference is that you're just opening an application on your computer that's not a web application.
[04:58] It's a terminal.
[05:00] Command line interfaces, sometimes people call it as well.
[05:05] But it's also graphical.
[05:08] So that's a little bit different than just typical command line interfaces.
[05:19] >> Yeah, that's cool.
[05:21] >> Okay.
[05:22] >> I just had -- you know, I came from a background in math and physics and then research here.
[05:30] So now I'm -- I am a developer at Dash.
[05:34] But so, yeah, I wasn't going to try to give a definition for a terminal.
[05:40] >> Yeah, no worries.
[05:41] And I think that's awesome, the transition that you've navigated from just doing research at DCG to actually doing development.
[05:51] And not just development, but development in Rust.
[05:53] So that's impressive.
[05:57] >> Straight into Rust.
[05:58] But, yeah, I love it.
[05:59] It's really fun.
[06:01] >> Cool.
[06:03] So, yeah, I already have everything downloaded, like all of the prereqs and stuff.
[06:11] So I'm actually going to share some -- let me share something else.
[06:19] And then let's also at some point bring up the GitHub repo, if you have any, and then the documentation that you have, wherever that is.
[06:32] I'm not sure if that's on GitHub.
[06:34] >> Yeah, sure.
[06:35] Okay.
[06:36] Yeah, we don't have any documentation on GitHub yet.
[06:39] I started on it today, but wasn't able to push it to the GitHub yet.
[06:47] But what we do have is this strategy test usage guide.
[06:52] Strategy tests are, like, performance tests for dash platform.
[07:00] I helped build out the library for that, and then we basically, like, created a pretty in-depth section in the TUI for building strategy tests and executing them.
[07:14] So that's what this is.
[07:17] It's a usage guide.
[07:19] >> Oh, we lost your screen share, I think.
[07:22] >> Oh.
[07:24] Did you?
[07:26] >> Let me add it to the stage, because I don't see it.
[07:30] >> It's up there.
[07:31] You don't?
[07:32] >> It's back up now.
[07:33] That was happening to us last week for some reason as well, and I don't think it was any of us that did it.
[07:39] It just drops out sometimes.
[07:41] >> Okay.
[07:42] >> So we see it now, though.
[07:45] >> All right.
[07:46] >> People can see where we're at.
[07:49] This is dash.org/blog, I assume.
[07:53] We don't see the URL.
[07:55] >> Oh, yeah, dash.org/blog/strategy-testsusageguide.
[08:02] >> Okay.
[08:05] So this goes into details on how to construct and execute a strategy test, but the first section gives, like, info on how to set up the TUI and connect to testnet or a local network.
[08:24] So I need to get this into the readme on GitHub as well as some more information on just general how to use all of the features in the TUI.
[08:38] But if you want to get set up, I recommend to go to this strategy test usage guide, and you can just go through the steps here.
[08:49] If you want to connect to a testnet node, you need to run a dash core node, which involves syncing, you know, syncing a node, which will take a few hours.
[09:06] So it's not really a quick start.
[09:10] I think probably a quicker start would be to run a local network.
[09:15] >> Mm-hmm, which we went over last week.
[09:19] Was that last week?
[09:20] I don't know.
[09:21] We went over that process of setting up a local network using DashMate with Mikhail Shenmig.
[09:28] I think that was last week.
[09:30] So that's what I'm trying to hope -- that's what I'm hoping to put together, not necessarily on this stream, but just that's my direction is so that when people are testing platform, they don't have to necessarily rely on testnet or mainnet.
[09:44] They can just spin up their own local network and then get all the tooling along with that.
[09:52] So the terminal user interface, setting up an insights server to have that insight interface, and the platform explorer that Mikhail's made, all the different tools that you would have at your disposal on mainnet to have those on a local network as well.
[10:14] So that's kind of my aim at some point and hoping that we can get the documentation there so that people that can make chocolate chip cookies can also do this with the right kind of groundwork.
[10:29] >> Yeah, I'm going to have it -- have some documentation this week on the GitHub.
[10:36] >> Excellent.
[10:38] >> Yeah, so I can walk through -- I think this only talks about how to connect to testnet, but I can quickly explain how to do a local network because it's easy.
[10:51] >> And what do you do when you're doing platform -- when you're doing development on this?
[10:55] Do you do the local or do you always develop on testnet?
[10:59] >> Normally local because I need to use, like, experimental versions of platform, like, when we did -- I just added master node voting to the TUI, and we don't have master node voting in the main branch of platform yet.
[11:20] So, yeah, I'm using experimental versions.
[11:25] But then when I do, like, performance tests, I do -- then I do testnet.
[11:31] >> Okay.
[11:33] >> Yeah, so -- yeah, so you need to decide, do you want to connect to testnet or local?
[11:42] >> Can you bump up the font just, like, one or two more?
[11:45] >> Sure, yeah.
[11:46] >> Since there's nothing else going on on the side.
[11:50] So command plus should do it.
[11:53] >> Okay, thank you, I didn't want to do --
[11:55] >> There you go.
[11:56] >> All right.
[11:57] >> One more, maybe.
[11:58] >> One more.
[11:59] >> Okay.
[12:00] >> Is it better?
[12:01] >> Yep.
[12:02] >> Okay.
[12:04] Yeah, so then you need to clone the repo, I think.
[12:09] >> And that's the thing that is renamed, right?
[12:12] So that --
[12:13] >> That's right, yeah.
[12:15] >> Maybe this needs to be updated as well.
[12:18] >> Yeah, it will redirect, but, yeah, eventually you're going to want the actual one in there.
[12:23] >> Right, it would automatically redirect.
[12:25] >> Yep.
[12:27] >> Okay, yeah.
[12:29] Do that, and then you need to install rust.
[12:35] Which is this command right here, does that for you.
[12:40] I believe it's -- this is a Mac command.
[12:44] I'm not sure.
[12:45] I created this using a Mac, so, yeah.
[12:49] >> Okay.
[12:52] >> Some other steps, add WebAssembly target, install essential build --
[12:57] >> Yeah, this is the WebAssembly target thing, I think, is -- or there's one step in here I think that has to do with being on an M1 or two or three, I think.
[13:07] >> Okay.
[13:08] I forget.
[13:11] Install WASM bind gen, protocol buffers, compiler, and CMake.
[13:22] And then -- well, okay.
[13:26] So, yeah.
[13:28] Then you have to create an environment file.
[13:34] So, yeah.
[13:36] I'll show you that in a second.
[13:38] Create an environment file, set the user name and password, and then cargo run, which is the command to start a Rust program.
[13:48] Okay.
[13:49] So now I'll switch over to the terminal.
[13:52] >> Okay.
[14:01] >> I -- excuse my -- my voice is a little raspy.
[14:04] I have strep throat.
[14:07] >> It's not fine.
[14:08] >> Okay.
[14:14] Where is it?
[14:15] >> Thanks for coming on, even through being sick.
[14:19] That's dedication.
[14:21] >> Yeah, I mean, I'm, like, awake and stuff.
[14:24] Just my throat hurts a little.
[14:27] All right.
[14:29] I'm sharing my screen, but I don't see it.
[14:33] >> Okay.
[14:34] I just -- I added it to stage again.
[14:37] >> Okay, cool.
[14:38] >> I don't know if the bumping up of font works on this, but if you could try that, that would be great.
[14:44] >> Sure.
[14:45] Same thing, command plus.
[14:47] >> Let's try it.
[14:48] Yep.
[14:49] >> How's that?
[14:51] >> I think that worked, yeah.
[14:53] >> Okay.
[14:55] >> Yeah, so the environment -- the .env file that was mentioned is -- it looks like this.
[15:05] So if you're running a local network, you're going to just use these explorer DAPI addresses.
[15:12] You're connecting to a local network.
[15:17] You basically copy and paste this whole thing, and you need to -- you just need to set the username and password.
[15:29] Should I be going into these details?
[15:31] Like, will you look back at this video, you think?
[15:35] >> Probably some people will, because we're going to -- we'll probably task some people to -- once you get the documentation up to what you think is sufficient,
[15:45] then we'll probably task somebody to go through it and actually try to set it up using that documentation.
[15:52] And we'll drop them a link to this video in case they want to look at that as well.
[15:57] But, I mean, in theory, the documentation should be good.
[16:01] Are these passwords and usernames something that --
[16:05] >> It's fine.
[16:06] This is just for local network.
[16:08] >> Okay.
[16:09] No, yeah, that's fine, as long as -- can you scroll up just a little bit?
[16:14] I'm looking at the port numbers for the DAPI addresses.
[16:19] Is this something -- I'm wondering if those -- like, what services those are.
[16:26] I'm assuming it's DAPI.
[16:28] And if those are the default ports that DAPI sets up and --
[16:34] >> They are, yeah.
[16:35] It'll be the same every time for a local network.
[16:40] >> Yeah, I'm seeing -- yeah, I'm seeing the three different ports.
[16:44] Do you know what that's about?
[16:45] Is that --
[16:47] >> Yeah, it's three different nodes.
[16:51] When you run a local network, the default is to have three nodes.
[16:56] >> Okay.
[16:57] >> So, yeah, each one is a different EVO node.
[17:01] >> Is that like when you are collecting a specific config, it'll be like local_1, local_2?
[17:06] Is that what that's referring to?
[17:08] >> Yes, yeah.
[17:10] >> Great.
[17:11] >> Yeah, I still have a little bit of confusion there, but I think we'll get it figured out when we go through it.
[17:19] Because I'm wondering if it's three different services on what looks to be the same node, because they're all 127 0.0.1,
[17:30] or if they're the three same services -- like when -- the way that Mikhail Shenmik sets up his local node,
[17:37] I think that they're actually three different nodes running under different port IP addresses.
[17:44] But we'll look into that.
[17:46] >> Yeah, sure.
[17:47] I'm not totally sure.
[17:50] Like, I'm running three containers in Docker, and that's all I know.
[17:56] I should share my whole screen, actually.
[17:58] I'm just sharing this window.
[18:00] Let me switch that.
[18:02] >> Okay.
[18:12] >> Can you see?
[18:14] >> Yep.
[18:15] >> Yeah, okay.
[18:16] So, yeah, I have three different -- running three different nodes, and then this is something to do with core.
[18:23] >> And this is Docker Desktop that we're looking at.
[18:26] >> Yeah, that's not something that may -- that may or may not be something that people have installed,
[18:33] and I don't know if it was in the list, but just so people are aware,
[18:38] this looks to be a graphical user interface for Docker itself.
[18:43] >> That's correct, yeah.
[18:45] This is just for a local network.
[18:47] >> Yeah.
[18:51] >> Yeah, okay.
[18:54] >> So when you -- let me quickly just say how to start a local network,
[19:01] and then I'll explain how to get the user name and password and this private key.
[19:09] >> Okay.
[19:11] >> Which are the only things you need to change in most cases.
[19:16] You can just copy/paste this whole file from GitHub, or actually from here.
[19:23] So you -- this is like a template, this .env.local.
[19:30] >> And that's what would probably be in the Git repo.
[19:33] >> Right.
[19:34] So you'll need to create a new file and just name it .env and copy local or testnet into it,
[19:45] and then just change the user name, password, and this private key.
[19:53] >> Got it.
[19:54] >> Okay.
[19:55] >> Now I'm curious to see if you're setting this up the same way that we set it up last week using DashMate.
[20:01] So let's see it.
[20:03] >> Okay.
[20:04] I don't use DashMate.
[20:05] >> Okay.
[20:06] That is the first -- let's see how you set it up.
[20:09] >> What do you use if not DashMate?
[20:12] >> Yarn.
[20:14] >> Yeah.
[20:15] Okay.
[20:16] Well, let's just see what -- let's just see.
[20:18] Can you hide the -- there's a little button that says "hide" down at the bottom.
[20:21] >> Yeah.
[20:22] >> Can you hide that?
[20:23] It's just -- yeah.
[20:27] >> Yeah, okay.
[20:28] So once you have Platform, like, cloned locally, you can just navigate to Platform in your terminal and type "yarn setup."
[20:41] >> And having Platform set up locally means that you've also, in addition to going and cloning the TUI platform, the TUI repo,
[20:54] you're saying you also needed to add the Platform Monorepo cloned.
[21:01] Is that right?
[21:03] >> If you're going to run a local network, yeah.
[21:06] >> Okay.
[21:08] >> What does "yarn setup" do?
[21:10] Because that's not a Yarn command.
[21:14] >> I'm pretty sure it does -- so there's two commands, "yarn setup," and you wait for it to finish, and then "yarn start."
[21:22] >> Could you go to your package.json?
[21:25] Because is "yarn setup" something that's defined in your package.json?
[21:29] >> I don't know.
[21:30] >> I'm guessing it must be.
[21:32] >> Yeah, if you go to package.json and wherever you're running the command.
[21:35] >> Yeah.
[21:39] >> There it is, down at the bottom.
[21:42] >> Package.json, yeah.
[21:44] And then scrolls to the setup command.
[21:46] Yeah, so "yarn install," "yarn run build."
[21:49] >> So it is running Dash Main.
[21:51] >> Hold on.
[21:52] Yeah, I was going to say, like, "yarn" doesn't just run Docker containers.
[21:55] It wouldn't make any sense.
[21:57] >> And it is running the group start, which is -- that's how we did it with Mikhail last week.
[22:03] So good.
[22:04] We're good.
[22:05] >> Cool.
[22:07] >> Yeah, I used to try to use Dash Main, like, maybe a year -- over a year ago.
[22:14] And I just gave up on it.
[22:16] There were so many bugs with it before.
[22:18] So now I just use -- it's just "yarn setup," "yarn start."
[22:23] And it's much simpler, I find.
[22:26] >> Well, it's because --
[22:27] >> You're still using it.
[22:28] >> -- there's some little Dash commands for you and made it foolproof.
[22:30] >> Yeah, you're still using it.
[22:32] I'm doing alias commands to the start and setup commands that run those -- that do run the install and Dash Main group start.
[22:41] So you're using it.
[22:43] You're just using it with these aliases, yep.
[22:47] >> Okay.
[22:48] Cool.
[22:50] Is it easier to -- is the Dash Main easier?
[22:54] >> If you're using it directly --
[22:56] >> Once you know how to use it, it's not too bad.
[22:59] It's really confusing at first.
[23:01] >> Yeah.
[23:02] >> What is it?
[23:03] It allows you to configure it more?
[23:06] >> Well, that's what's running the Docker.
[23:08] The Dash Main commands are what's starting your Docker containers.
[23:11] The Docker containers, I can tear them down and recreate them and then do all that stuff.
[23:16] It's also affecting whether you are syncing with the chain or whether you want to blow away all the transactions and just stuff like that.
[23:25] >> It's just using Dash Main directly gives you more control because you can do exactly the commands that you want to do rather than just these prescribed commands that are the start and the setup.
[23:38] >> Yeah, this is like -- it gives you a golden path.
[23:40] So if you just run this command, it's going to work.
[23:42] But if you wanted to actually, like, get into the guts of it, then it would be complicated.
[23:47] But really you don't actually want to do that.
[23:49] So this is the way to go for most people, just having a couple of commands.
[23:52] This is kind of like why people love Docker Compose.
[23:55] You just run Compose up and it spins up, like, a million different services all running at the same time.
[24:01] >> Cool.
[24:02] So let's go for it then.
[24:04] Yarn setup is going to run yarn install.
[24:07] It's going to install the dependencies and then afterwards run yarn run build and then yarn run configure, which are their -- so then it's doing the Dash Main stuff.
[24:18] So let's go ahead and do it.
[24:21] I already have -- I'm already running a network.
[24:23] It might take a few minutes of just waiting around.
[24:27] So I'm not going to do it right now.
[24:31] >> Sure.
[24:32] That's fine.
[24:33] >> Yarn setup.
[24:34] Wait for it to finish.
[24:35] Yarn start.
[24:37] And then if you're looking at this Docker desktop, you should see everything running here.
[24:45] So then to get the user name and password to plug into the .env file back in Explorer, you need to run this command here.
[24:59] Right here.
[25:00] Which you can see I ran here.
[25:03] Yarn dash main config get core RPC local seed.
[25:09] User and password right here.
[25:11] >> Got it.
[25:12] So it spits it out for you.
[25:14] >> Yep.
[25:15] And then the wallet private keys, there's two that you can use, are here in platform packages, platform test suite .env.
[25:32] And you want to use the faucet private keys.
[25:35] Faucet one, faucet two.
[25:38] >> Is this the faucet that we know and love?
[25:41] >> This is the thing that -- this is what I want, a way to just directly access the faucet from the terminal.
[25:48] >> Yeah, when you're setting up local node, it's a different faucet process because at least from last week, you're actually just minting coins to an address instead of going through a crummy old faucet website.
[26:02] >> Way better.
[26:04] Way to go.
[26:06] >> And it's different also because they only have 50 dash each, and they don't get more like the test net faucet does.
[26:16] >> Okay.
[26:19] >> Yeah, so just -- I don't -- just copy.
[26:23] I think I already have it pasted in here.
[26:26] Copy and paste here.
[26:29] And then you're ready to run the terminal thing.
[26:34] So you can do back in RS platform explorer, do cargo run.
[26:43] >> And this is the moment we've all been waiting for.
[26:46] So you've got a -- so, yeah, you're running right in the terminal.
[26:50] You've got this little graphical user interface or terminal user interface, technically.
[26:55] And it's all keyboard navigation, it looks like.
[26:59] >> Yeah.
[27:01] The mouse doesn't do anything.
[27:04] >> Okay.
[27:06] >> So all keyboard navigation.
[27:10] Yeah, so normally the first thing you do is go to the wallet by pressing W because normally you won't have an identity.
[27:21] You'll just have a wallet.
[27:23] Let me clear my identity.
[27:25] So normally when you load it, it will just look like this.
[27:28] You'll have a wallet.
[27:30] It will say no balance.
[27:32] So you want to press B to refresh wallet balance.
[27:37] >> So it does actually give you a wallet without you having to do anything.
[27:42] It does that for you.
[27:44] >> Yeah, right.
[27:47] If you paste it in here.
[27:49] You can leave this blank and still open without a wallet.
[27:56] And then you can just go to the wallet screen and press add wallet by private key and paste it in there.
[28:04] >> Okay.
[28:08] So, yeah, you have a wallet, but if you want to query the network, you don't need an identity.
[28:20] But if you want to broadcast any transactions, you need an identity.
[28:26] So people normally are going to want to press I to register an identity.
[28:33] And you will get this form where you select an amount of Dash you want to fund the identity with.
[28:43] Normally I just do one unless I'm doing something weird with a performance test.
[28:53] And you can see down here it's executing a task.
[28:59] Sometimes it takes a little bit.
[29:04] >> Yeah.
[29:06] When we do this in Node using JavaScript, it seems to take a while all the time.
[29:15] >> This is taking too long, though.
[29:17] >> It's taking too long.
[29:18] Okay.
[29:19] So this is -- something's not quite right then.
[29:22] >> Yeah.
[29:23] So I'm going to exit this terminal and try again.
[29:28] But what I often do is if I'm experiencing something weird, we have this file, explore.log.
[29:39] And we do a lot of logging in here.
[29:43] Right now it doesn't say anything relevant.
[29:47] But just FYI, this is a good place to check if you're ever interested in more information.
[29:55] >> Okay.
[29:57] >> Yeah.
[29:58] But let me try this.
[30:00] Try restarting.
[30:11] >> And then can you just kind of like say what you're typing so that people know what you're doing as you're doing it?
[30:18] >> Yeah, yeah.
[30:22] Actually, I'm so zoomed in that you can't see the whole thing here.
[30:27] But normally -- here, I'll zoom out just for a second.
[30:30] >> Sure.
[30:31] >> Zoom out.
[30:33] Oh, that's too much.
[30:36] When you have a loaded identity, you can see the -- at least one key, public key.
[30:45] We should make this screen scrollable so that you can scroll down, but, yeah.
[30:53] Okay.
[30:54] Let me clear -- I'm going to -- so there's a lot of options of things to do here.
[31:03] Copy the receive address of the wallet.
[31:06] Refresh UTXOs and balance.
[31:09] Register an identity.
[31:11] I'm going to press E to clear loaded identity.
[31:16] And then press I to register again.
[31:20] And one dash.
[31:22] Enter.
[31:27] Why is it not working?
[31:35] Oh.
[31:40] Might be some bug.
[31:41] But here, let me -- I'm going to delete -- this file here stores the state of the app.
[31:51] So anything that you might have saved in the app, if you close it and reopen it, like at a later date,
[32:00] it will reload the previous state.
[32:05] So like your wallet, if you created strategy tests and saved them, it will be here.
[32:11] I'm going to delete this and maybe that will help for some reason.
[32:17] >> This is why we have a new one.
[32:19] Because it's these little secrets that make all the difference.
[32:24] >> Yeah.
[32:33] Oh, great.
[32:38] This is a bug about when it tried to register the identity, the asset lock proof that it's trying to use has already been used.
[32:48] So I'm just going to try again.
[32:54] All right.
[32:56] So this -- I'm going to clear the loaded wallet by pressing M.
[33:01] And I'm going to try the other wallet that was in the platform here.
[33:09] This one.
[33:10] The other faucet wallet.
[33:15] So add wallet by private key, paste.
[33:23] Now register identity.
[33:29] Damn, that's annoying.
[33:35] >> If we can't get this to work, can we just try some of the other things?
[33:38] >> Yeah.
[33:39] >> Do you need an identity to do anything else?
[33:41] >> Yeah, I can just walk through.
[33:43] Let me try this one thing.
[33:49] I wonder why -- yeah, I haven't used -- I wonder -- I don't know why this is happening exactly.
[33:56] But maybe I've been using this local network.
[34:00] I haven't restarted it in a while.
[34:04] Yeah, I think I'll just walk through.
[34:06] I don't need to actually execute stuff.
[34:08] I'll just walk through other stuff you can do.
[34:12] >> Yeah, that's the main thing.
[34:14] If it's network related or something, then --
[34:17] >> Yeah, yeah.
[34:18] It's -- I'm not sure.
[34:20] It could be -- I think it could be a platform bug.
[34:25] Could be TUI bug.
[34:28] Could be -- I'm not sure.
[34:30] All right.
[34:31] So you're in the wallet screen.
[34:33] And just -- you press Q to go back.
[34:36] Q always goes back.
[34:39] And if you go back too far and press Q, then you'll quit out of the application.
[34:45] So --
[34:46] >> So this is the main, main, main menu.
[34:48] >> Yeah, right.
[34:52] So the one that I have been working on the most is the strategies screen here.
[34:59] So I'll press S.
[35:05] And so from here, you can press N to create a new strategy or press I to import a strategy.
[35:14] And to import a strategy, we have this repository on the -- in the dash pay org on GitHub with some strategy tests saved.
[35:27] And you can copy the raw GitHub URL and paste it in.
[35:34] I can try it.
[35:36] I haven't tried it in a while.
[35:38] But here.
[35:39] So import strategy.
[35:42] >> Anthony, can you find that and just post the link to the GitHub link to both those -- I can probably do it too, actually.
[35:52] I pasted the links in our Discord message.
[35:56] >> Yeah.
[35:57] Yeah.
[35:58] It's right here.
[35:59] Dash pay/platform strategy tests.
[36:02] Just wanted to show that at least.
[36:04] And then there is some read me on this one as well.
[36:08] >> Yeah.
[36:10] So I can go to documents and say 50.
[36:16] I'll just choose this one.
[36:20] And then right click on this raw button and copy link address.
[36:26] And then paste it in here.
[36:31] >> Oh, cool.
[36:32] It still works.
[36:34] >> Is there -- can we go back to the GitHub and view the file?
[36:39] I just kind of wanted to get an idea of what this actually is.
[36:42] Is it just a series of commands that the platform 2e runs?
[36:47] Or what actually is a strategy?
[36:50] >> It's a binary file.
[36:52] >> It's a binary file.
[36:53] Okay.
[36:54] >> So if you click view raw, it will just download a binary file.
[36:57] >> Okay.
[36:59] >> It's a -- so in Rust, it's a Rust structure.
[37:06] Like a struct.
[37:09] A strategy struct that is just encoded or whatever in binary.
[37:15] That's all it is.
[37:17] >> Okay.
[37:18] But conceptually, do you know conceptually is it just like creating a bunch of
[37:24] transactions or what actually is a strategy?
[37:29] >> It's essentially this right here.
[37:33] It's -- so there's identity inserts, which you can define how many times per
[37:42] block and the chance per block to insert an identity.
[37:47] And then star contracts is how many contracts to -- not how many, but star
[37:54] contracts defines data contracts to register at the very start of the strategy.
[37:59] Same with star identities.
[38:01] How many identities, how many keys each one has, what their balance is to
[38:06] register at the start of the strategy.
[38:09] >> Okay.
[38:10] Yeah.
[38:11] So conceptually, it is just running, making requests to platform, create all
[38:15] these identities, register all these identities, create all these balances,
[38:21] things like that.
[38:23] >> Yeah.
[38:24] It's not literally holding transactions, but it defines -- yeah, it holds
[38:29] instructions for platform.
[38:31] Yeah.
[38:32] To create transactions.
[38:34] >> Okay.
[38:35] So it's making 50 contracts.
[38:39] In this particular --
[38:41] >> In this particular one, it's making 50 contracts.
[38:44] It's making 50 star identities.
[38:46] And then in operations, it just says 50 here, but -- here.
[38:52] So I can -- I'll press O to navigate into operations.
[38:57] And you can see it's insert a document with random data to this contract once
[39:03] per block.
[39:05] And it's doing that for each -- it's doing that for each of the 50 contracts.
[39:10] >> Mm-hmm.
[39:12] Okay.
[39:13] So this high level is just a recipe of different commands that the platform
[39:19] TUI client runs.
[39:22] But you can also, like, use -- you can also use this platform explorer just to
[39:27] do those things manually, I assume.
[39:30] So --
[39:31] >> Yeah.
[39:32] Yeah.
[39:33] >> -- you want manually.
[39:35] So can we back up and instead of doing identities -- or whenever you're done
[39:39] with the strategy stuff, I'd kind of like to see how to use the platform TUI
[39:47] just as a user who wants to register a contract manually or whatever.
[39:55] >> Yeah.
[39:58] So back at the main screen, you can't register a contract -- I think actually
[40:08] the only -- you could do it through a strategy test.
[40:11] You could just register one contract.
[40:13] But that's the only way to do it right now.
[40:17] >> Okay.
[40:19] >> If we went to the contract screen, you can query your contracts and you can
[40:26] submit random data documents to them.
[40:31] But you can't, like, define -- well, you can't register a contract and you
[40:40] also can't, like, define a document.
[40:43] It's only random data documents at this point.
[40:47] >> Okay.
[40:49] >> You can do it through strategy tests, though.
[40:51] >> So then how would we make our own strategy test?
[40:54] I guess that's the logical question.
[40:58] >> Yeah, so going back to strategies, now that we've imported a strategy, we
[41:05] have some new options.
[41:07] You can export a strategy, select a strategy, delete one, or create a new one.
[41:14] So I'll hit N for new, and I'll name this one test.
[41:25] So from here, let's say we want to define some start contracts.
[41:35] You press C, and, man, there's a lot of options -- there's a lot of -- too much
[41:43] stuff to cover today, I think, for what you can do with strategy tests.
[41:48] But if you want to add a specific contract, this is how you would add a contract.
[41:54] You would press S, add specific.
[41:57] And these -- this list is here in supporting files, contracts.
[42:06] These are JSON files.
[42:09] So if you want to define a data contract, you can put it -- why can't I -- you can
[42:16] put it as a new file in this directory, and then you can select it from here and
[42:25] put it in a strategy test and register it that way.
[42:28] >> Okay.
[42:29] And that was actually the actual Dash Pay contract that we were looking at as an
[42:33] example, right?
[42:35] >> It's modified.
[42:36] It's slightly modified, but, yeah.
[42:38] >> Yeah.
[42:41] >> So, yeah.
[42:44] So this is what we've been familiar with doing these raw in code in our walkthroughs.
[42:55] >> These data contracts like this?
[42:58] >> Yeah.
[42:59] >> They're all in the JSON schema.
[43:01] >> JSON schema.
[43:02] And this is also what you might have as an output from the Dash Pay.io page.
[43:09] So can we -- should we look at that for a little bit?
[43:12] >> Sure, yeah.
[43:13] The Dash Pay.io will -- basically you want to paste it from here into this field,
[43:22] document schemas.
[43:23] This is what the Dash Pay.io creates.
[43:26] >> Yeah.
[43:27] >> Yeah.
[43:28] Sure.
[43:29] We can go to Dash Pay.io.
[43:40] >> Yeah, so this was the first thing I worked on as a Rust developer.
[43:46] It's front and back end Rust.
[43:51] Our graphics guy made it look nice.
[43:54] Shout out Rostislav.
[43:57] And also Tanya did an amazing job.
[44:00] >> Yeah, it's very cool.
[44:03] I've never seen a front end written in Rust.
[44:06] So it's pretty cool.
[44:08] >> Yeah.
[44:09] There's some limitations.
[44:10] Like, you can't -- there's no copy to clipboard button.
[44:15] There's no, like, library for that in Rust yet.
[44:18] But, yeah.
[44:21] Basically what you can do is describe -- this is a open AI API.
[44:30] So you can describe a data contract that you want to create.
[44:35] Or just an app that you want to create, even.
[44:38] And it already is, like, aware of what platform is and what data contracts look like.
[44:44] So you can just say something like "food delivery app."
[44:52] And it takes as long as it takes chat GPT to write something.
[45:01] >> Yep.
[45:05] >> And it will populate here.
[45:08] But you can also manually fill out, like, if you want to create document types, properties, all this stuff you can do here as well.
[45:23] >> And this is using GPT 4.0?
[45:28] >> Yeah.
[45:29] >> Did it break?
[45:31] >> It did break, but I've never seen -- with the GPT 3.5, it was -- this is the stupidest response I've ever seen.
[45:43] So we'll have to --
[45:47] >> So wait, did you recently -- you recently upgraded from 3.5 to 4.0?
[45:53] Is that why it's different or what?
[45:57] >> Yeah.
[45:58] >> I saw you had a tweet about it that was a month ago.
[46:01] >> Yeah.
[46:02] Not -- yeah.
[46:03] I just upgraded it from 3.5, like, two or three weeks ago to 4.0, like, the new one, 4.0 turbo or whatever.
[46:12] So that's funny.
[46:14] Kind of.
[46:16] I have been noticing that it's -- it's been giving me --
[46:20] >> Try a different one.
[46:22] Try a simpler one.
[46:24] >> Yeah.
[46:25] So I have to refresh.
[46:27] You may have noticed it gave, like, an error message up here.
[46:30] That is -- so it also validates the contract against platform protocol.
[46:39] So if it isn't --
[46:41] >> So it wasn't even a valid contract, even though it was the worst contract ever.
[46:45] >> Yeah.
[46:46] >> Double fail.
[46:47] >> Yeah.
[46:49] Let's see.
[46:54] So the way I would do this, if someone was just, like, how would you use chat GBT to write this kind of thing, I would speak to chat GBT directly.
[47:02] I would give it some few-shot examples of contracts, examples, docs explaining what they are, and then I'd tell it what to do.
[47:10] So it would be able to kind of have some in-context learning to understand what to write.
[47:15] So I'm not sure what's going on under the hood here in terms of how you got it to understand a platform or not.
[47:21] >> That is what's happening under the hood.
[47:24] >> There you go.
[47:26] >> Let me see if I -- yeah, I have -- I can show you exactly what's happening.
[47:33] >> There's the prompt.
[47:34] >> Yeah, yeah.
[47:35] >> You have that big string of text randomly in your code somewhere.
[47:38] >> Yeah.
[47:39] >> Anthony wants the power all to himself.
[47:41] He wants to be able to give this at the user interface level.
[47:45] >> Yeah, well, you can.
[47:47] Also, then you give this to Claude, you wouldn't have to worry about chat GBT at all.
[47:52] >> I haven't tried that yet, but I've heard that it's great.
[47:56] >> Yeah, it's pretty amazing.
[47:59] >> So --
[48:00] >> There we go.
[48:02] >> This is better, much better.
[48:06] So max length is a required property for timestamp.
[48:14] So in that case, I would just find this timestamp here, max length 63, and then submit.
[48:37] Oh, there must be multiple.
[48:39] But, yeah, basically, I'll do it.
[48:46] >> Yeah, we got some time.
[48:48] >> Yeah.
[48:49] Do you have a cutoff?
[48:52] >> Not specifically.
[48:54] We tend to go about an hour.
[48:56] So we're 48 minutes in.
[48:58] >> Okay, okay.
[49:01] Yeah, so I find that it always misses this.
[49:04] Like, certain properties need certain validations, and it doesn't catch everything.
[49:12] But this is kind of how I fix this stuff.
[49:19] Just fix everything.
[49:23] Submit, and then see.
[49:27] There, okay.
[49:29] Passing, so, yeah, you could take this, copy it.
[49:36] I can just -- I can try just putting it right into here.
[49:46] I think it goes all the way.
[49:57] Paste.
[49:59] Save.
[50:01] All right.
[50:03] I'm going to exit out and then restart so that it can become aware of this contract.
[50:12] Strategies.
[50:16] Select the strategy.
[50:18] Test.
[50:21] Contracts.
[50:23] Add specific.
[50:26] And which one?
[50:27] This one.
[50:31] After you select one, it will ask, do you want to add another contract?
[50:35] And that means, like, it has to be a contract update.
[50:43] I need to make this more clear.
[50:45] But that's what it means.
[50:48] If you want to, like -- what it will do is in, like, I think it's hard coded right now to, like, after three blocks, it will update this contract.
[51:00] We will make that number configurable later.
[51:02] But that's what this is asking.
[51:04] So I'll just hit no for now.
[51:09] And I'm going to go back.
[51:11] And so now we've added a start contract to this strategy.
[51:17] And we can add a bunch of other things.
[51:20] If you go to operations, add, you can do documents, identity top ups.
[51:28] Almost everything.
[51:30] I think Sam added master node voting transitions to this.
[51:48] So we have this strategy.
[51:50] It's going to create one start contract.
[51:52] I'm going to press R to run the strategy.
[51:57] Do you want to run on a per block or per second basis?
[52:01] Per block basically just -- it's -- originally we did per block.
[52:10] And now it kind of doesn't make sense.
[52:13] I always just do per second.
[52:15] I think I'll probably get rid of per block.
[52:19] Number of seconds to run the strategy, I'm just going to do ten.
[52:24] Verify proofs.
[52:27] Only applies to block mode is not true anymore.
[52:30] So I'll hit yes.
[52:33] And verify proofs mean, like, when you submit a state transition,
[52:40] you'll get a response from platform with a proof showing that it was,
[52:45] in fact, included, added to the platform state.
[52:49] And it will verify that proof as well if you select yes.
[52:54] It just takes a little bit more time.
[52:56] So if you're trying to do, like, you know,
[53:00] 50 transactions per second or something, you might not want to do it.
[53:05] You might not want to verify the proofs.
[53:09] And then confirm.
[53:11] Oh, no identity loaded, right.
[53:13] So, well, that's how you would do it.
[53:18] >> Cool.
[53:20] >> Yeah, so that's the strategies.
[53:25] >> What does platform information show, just so we can see that?
[53:28] >> Yeah.
[53:30] Sam did this, and I have almost never used it.
[53:35] So let's see.
[53:37] I guess we want to fetch current platform epoch info.
[53:45] So current heights is, I'm guessing, block height.
[53:52] These are block heights, block time, epoch zero.
[53:59] >> Yeah, this is good information.
[54:01] Just basically is what you would see in a block explorer.
[54:07] So let's go back out of here again and see the main menu one more time.
[54:13] Platform information, identities, wallet, this all makes sense, contracts, version upgrade.
[54:18] Is the version upgrade, would that be just a version of the TUI itself?
[54:25] >> I think it's for referring to platform, and it also doesn't do anything.
[54:30] >> Okay.
[54:33] >> Yeah, I don't know what -- I think Evgeny put that in when he created it.
[54:38] I'm not sure exactly what it's supposed to do.
[54:41] >> All right, what options do we have for wallet?
[54:43] I don't know if we've looked into that yet.
[54:50] >> You can --
[54:52] >> Oh, I think we have, actually.
[54:54] >> Yeah.
[54:57] You -- if you register an identity, and you want to register another one, you can -- it will save --
[55:05] it will save all your previously registered identities, and you can switch through them.
[55:11] And in the -- I have a branch for master node voting.
[55:16] You can register an Evo node identity also, which you can use to do master node voting.
[55:26] But I don't have that merged into master yet, and master node voting isn't merged into main platform branch yet either.
[55:37] >> Okay.
[55:38] >> Yeah.
[55:40] I'll just do identities.
[55:42] I can show you quickly identities.
[55:45] Basically, you can fetch an identity by ID from platform, and it will show you all of its keys, its balance and stuff.
[56:00] If you have a loaded identity, you can press R to register a DPNS name, and T to transfer credits.
[56:09] It will just ask you for who you want to transfer to and how much.
[56:15] Contracts.
[56:18] There's -- there's a lot -- I think there's quite a bit more stuff you can do in contracts.
[56:27] If you press Fetch System Contract, S, you can fetch Dash Pay or DPNS.
[56:34] I'll do DPNS.
[56:37] And then if you go back, you'll have it here.
[56:42] And you can press Enter to select it.
[56:46] Select the type of document type you want to examine.
[56:51] Domain is the one with all of the names in DPNS.
[56:56] And then you can broadcast a random document query.
[57:02] You can do, like, a SQL query.
[57:07] So select all from domain, Enter.
[57:09] Right now, it's -- this is just the -- I think this is, like, when platform is created, DPNS is automatically created, and this document is automatically created as well.
[57:26] So when this is on main net, we'd be able to run that command and see all the Dash usernames.
[57:31] That's -- that's right, yeah.
[57:34] And also -- oh, yeah, we have, like, the NFT feature now.
[57:40] So you can scroll through the documents here, and you -- if, like, a document is for sale, you can -- you can buy it.
[57:53] And if you're the owner of a certain document, you can put it up for sale.
[57:58] And then also for masternode voting, if a certain document is, like, being voted on at that time, if it's a contested document, you can vote on it if you're a masternode.
[58:13] So, yeah, that's -- all that stuff takes place in this screen.
[58:17] Yeah.
[58:19] Okay.
[58:21] Very cool.
[58:23] Maybe let's fly back out high level again.
[58:26] What's on the roadmap?
[58:29] I know there's not really a specific roadmap, but give us your general -- your general idea of what you're working on with this specifically in the future, what features, what documentation.
[58:47] Yeah, anything that you wanted to say high level.
[58:50] Sure, yeah.
[58:52] Well, I had, like, five PRs open, which I finally got them all reviewed today.
[59:00] Thank you, Evgeny.
[59:02] So -- but he left a bunch of comments because he's a much cleaner and better developer than me, so I'm going to address his comments and merge masternode voting in, DPNS registrations, and NFTs.
[59:22] And that will be done tomorrow, and then I'm also going to get this documentation, like the readme, done this week.
[59:34] And then I might be -- I'm not sure if -- I think maybe the next thing for the TUI is to allow people to register contracts and documents without having to use a strategy test.
[59:56] That makes the most sense to add next.
[60:00] Yeah.
[60:01] Yeah.
[60:03] For me, personally, this week, I'm running a bunch of tests to determine fees for certain operations before we launch in a few weeks.
[60:17] Yeah, that's a good point.
[60:20] Is there a file somewhere that defines the fees for each operation?
[60:27] Yeah, we have -- yeah, there is.
[60:30] There's, like, a file, like, in the code, you mean?
[60:34] Mm-hmm.
[60:35] Yeah.
[60:36] Is it right -- it's right here.
[60:43] It's one of these.
[60:45] Odysseus just made a PR to fix it, and I -- there's a file, yes.
[60:55] Do you want me to find it?
[60:56] No, it's okay.
[60:57] I was just -- if you had it, if you knew where it was specifically.
[61:01] This is -- looks like, you know, you're -- the git diff, so I'm not sure this is the best place to look for it anyway, but --
[61:11] I think -- yeah.
[61:15] That is one of the main -- that is going to be one of the main issues when we go to main net is, like, how much stuff will cost.
[61:23] I know people have been asking questions about that, and so if they could just go straight to the source, that would probably be the best place to find out how much data storage is going to cost, for example.
[61:37] Well, for data storage, that's already determined.
[61:40] It's just going to be two -- so we have -- have you heard about the fee multiplier?
[61:50] Yeah.
[61:51] Yeah, so I think we are hard coding it right now to just being two times -- the storage fee will be two times the cost that it is to store on AWS.
[62:06] So, like, masternode owners will get the cost back plus, you know, plus the same amount that it costs for storage.
[62:18] Right?
[62:19] Does that make sense?
[62:20] Sorry, I'm very tired.
[62:22] Yeah, no, it makes enough sense for now, I think.
[62:26] We'll probably -- that feature is not quite done yet, so I think we'll dig into those details later.
[62:32] The fee multiplier?
[62:36] The fact that there is a multiplier, I know that's done and everything, but, yeah, like, just the pricing around specific operations and storage, I guess that's a little bit foggy to me, but I don't need an answer on that right away.
[62:54] Oh, okay. Well, my first task at Dash as a research engineer was to make the fee system, so I have this internal document, pretty big document, which we're going to turn into a dip.
[63:11] Okay.
[63:12] But right now -- basically, the last thing that we have to do is, like, we were waiting for just a few weeks before release to actually run a bunch of tests to get costs for, like, processing costs, like I/O operations and hashing and stuff.
[63:31] So that's what I'm determining right now.
[63:34] Yeah.
[63:38] But the storage cost is fixed already.
[63:43] And that's based on AWS, you said, for lifetime storage or something?
[63:48] I didn't know AWS offered a lifetime storage.
[63:53] Yeah, yeah.
[63:57] Yeah, so I don't know -- I guess I could -- basically, we charge for -- we consider 50 years of storage to be permanent storage, because the cost of storage decreases so much every year that what you pay now -- if you pay for 50 years of storage, basically, that covers 99% of --
[64:26] Anything beyond 50 years as well.
[64:31] And AWS does have a tier for storing something for 50 years, and then you're basing -- or I guess maybe they just price it per year and you multiply by 50, something like that?
[64:43] Yeah, it's -- there's a few factors that go into it.
[64:48] Virgil helps me.
[64:50] Virgil is the other researcher who is much better at math than me.
[64:55] He has a master's in cryptography, but there's some factors that go into it.
[65:01] It's kind of like doing whatever the cost is now times 12 is about what it comes out to.
[65:08] Okay.
[65:09] Yeah.
[65:11] All right.
[65:12] Well, that was a good run-through of the terminal user interface.
[65:16] I have a much better idea of how it's used and what it can do and how to install it.
[65:23] So looking forward to those docs when they come, and then we'll -- yeah, we'll try them out.
[65:29] Cool.
[65:30] Yeah, I hope that was helpful and checked off all of your boxes.
[65:36] Yeah, I mean, it was a good introduction.
[65:38] I know that everything's not done by any means, so I just wanted to get a good overview and, yeah, a little bit of an impetus to get some documentation that external developers can use on just setting it up.
[65:55] Because if people can get to the point where they can get it installed, then people can play around.
[66:02] It's not like they need an instruction manual to know all the features, but if they can just get it installed, I think that's a good first step.
[66:09] So, yeah.
[66:10] Yeah.
[66:12] Anthony, any other questions from you?
[66:17] I guess the only one thing is just on the setup kind of theme is, like, would there be a possibility of this being just, like, a homebrew thing you could install?
[66:27] Or would there -- you'd still have to, like, configure your project, obviously, but I feel like that could potentially cut down on some of the challenge for -- at least for the people who use brew, you know?
[66:36] Oh, yeah, totally.
[66:39] Yeah, I've never used homebrew.
[66:42] Like, I've never made something like that, but, yeah, we could definitely use that.
[66:48] Or just, like, some sort of curl setup command that automates a lot of it, you know?
[66:52] Yeah.
[66:55] Okay.
[66:56] Yeah, that's a good point.
[66:57] I'll bring that up in our stand-up call tomorrow.
[67:01] And we can also hit up AJ to see if there's, you know, some --
[67:07] Web install?
[67:09] Either web install or just a shell script that kind of does it cross-platform.
[67:14] So the easier, the better, obviously.
[67:18] Yeah.
[67:19] I'll just ask Claude.
[67:22] There you go.
[67:23] All right.
[67:24] All right.
[67:25] Thanks, everyone.
[67:26] Next week.
[67:27] Next week.
[67:28] Bye.