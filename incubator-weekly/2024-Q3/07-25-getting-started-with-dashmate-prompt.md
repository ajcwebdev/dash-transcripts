---
showLink: "https://www.youtube.com/watch?v=s8c9Wqx1Su0"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Getting Started with Dashmate"
description: ""
publishDate: "2024-07-25"
coverImage: "https://i.ytimg.com/vi/s8c9Wqx1Su0/sddefault.jpg?v=669fe12b"
---

## Song

### ChatGPT o1

1. Dashmate Distinctions
2. Docker's Dominion
3. Minting Momentum

Verse

Progressive synergy fueling our vantage for local advantage, I manage Docker's labyrinth with fervor, never vanish
We brandish Node dependencies, brand new remedies, scrutinize seeds, minted capital freed from harsh penalties
Construct a matrix of scripts, stacking symmetrical flips, each line commits, cryptographic grit in ephemeral shifts
Status calls confirm the cluster stands firm in code, Dashmate ascends as the epicenter forging this abode

Chorus

Breathe in the synergy, revolve the local ground, launch the config, watch minted coins abound
Identity emerges, unstoppable lines converge, in this dimension, we let development surge

Verse

Commands flourish, set up local, revolve in pattern, no public net friction, minted sums never flatten
We harness unstoppable impetus, forging fluid genesis, register credentials swiftly, fueling synergy's emphasis
No illusions hamper progress, Docker keeps it cohesive, reset or force, no fiasco remains elusive
We read results from data, validated in code, when query syntax hits, the chain seamlessly bestowed

Chorus

Breathe in the synergy, revolve the local ground, launch the config, watch minted coins abound
Identity emerges, unstoppable lines converge, in this dimension, we let development surge

Verse

Multiple nodes in motion, orchestrated through synergy, group start or group stop, a sequence of wizardry
We revolve around structure, forging each contract plain, yet weave intricate schemas in every partial domain
Never cornered by chaos, top up logic in place, binding scripts with mnemonic, escaping precarious chase
Local lanes for experiments, boundaries dissolve minimal, pushing code to the forefront, pivoting toward the pinnacle

Bridge

Symphonic expansions rise from minted seeds to final frames, ensuring advanced adoption through unstoppable aims
Comprehensive synergy framed by stable pillars bright, preparing for complexities while fortifying might

Chorus

Breathe in the synergy, revolve the local ground, launch the config, watch minted coins abound
Identity emerges, unstoppable lines converge, in this dimension, we let development surge

## Episode Description

A step-by-step conversation on setting up and managing a local Dash development environment with Dashmate.

## Episode Summary

This discussion walks through configuring and running Dashmate locally to develop applications on the Dash platform. It begins with a quick overview of installation prerequisites, including Docker and Node.js, then explains how to confirm that Dashmate is correctly installed. The speakers demonstrate starting and stopping a local network, minting Dash without relying on external faucets, and creating reusable scripts that streamline wallet creation, identity registration, contract deployment, and document submission. They also talk about environment settings and potential issues that can arise, offering guidance on how to troubleshoot or reset configurations. Finally, they showcase how to retrieve stored data using basic queries. Throughout, they emphasize efficiency and clarity, allowing developers to quickly move from a blank setup to a functioning local Dash environment.

## Chapters

### 00:00 - Introduction and Overview

In the opening minutes, the hosts set the stage by confirming their streaming setup and considering options for multi-platform broadcasting. They greet viewers and outline the purpose of this session: to walk through using Dashmate to create a local development environment for the Dash platform. The conversation briefly touches on the utility of a local network, highlighting how it accelerates testing and shortens feedback loops by avoiding reliance on external test networks.

They note that this tutorial provides a straightforward path for developers looking to experiment with Dash without worrying about public faucets or more complex configurations. By focusing on client-side development tasks and essential Dashmate commands, the hosts promise a clear, step-by-step overview. This introduction underscores the benefit of local testing and frames the rest of the conversation.

### 03:00 - Setting Up Dashmate

Moving into the core steps, the presenters start by confirming the required dependencies: Node.js, Docker, and Dashmate itself. They walk through installing Dashmate globally, then verify the installation by running basic help commands. The environment checks also involve ensuring the correct system requirements are met so no surprises appear later in the setup process.

The discussion emphasizes that once Dashmate is properly installed, users can rely on a small range of commands to spin up and manage their local Dash network. Each command is briefly explained, illustrating how Dashmate orchestrates Docker containers and verifies whether everything is running smoothly. At this stage, viewers gain a firm understanding of how to move from zero to a fully operational local environment.

### 06:00 - Managing Local Environment

In this segment, the conversation shifts to handling various start, stop, and status operations with Dashmate. The hosts show how to watch for prompts that confirm a local network is ready, as well as the different flags and parameters useful for maintenance. They mention how powerful the Dashmate group commands can be, letting you manage multiple network nodes at once for testing or more advanced scenarios.

They also touch on resetting configurations when something goes wrong or if developers need a clean slate. There are multiple levels of resets, each with its own implications. By breaking down the differences between soft and hard resets, the speakers illustrate common real-life situations: leaving a project idle, encountering container issues, or needing to wipe configurations entirely. This segment gives developers a survival toolkit for smooth local testing.

### 10:00 - Understanding the Configuration

Here, the hosts briefly examine the auto-generated configuration files that Dashmate uses to run local nodes. They demonstrate how these files can become complex, containing thousands of lines with references to ports, container names, and service endpoints. While they note that casual users rarely need to dig deep into these files, they stress that it is helpful to know they exist.

They also discuss potential expansions, such as enabling additional monitoring or user interface services. Though these topics are more advanced, the speakers make clear that Dashmate’s underlying Docker infrastructure can handle many specialized tools, from explorers to metrics dashboards. This part underlines the breadth of Dashmate’s capabilities while keeping the focus on essential configurations for local development.

### 15:00 - Generating Dash Locally

Next, the presenters highlight the process of minting Dash within the local environment. Instead of depending on external faucets, developers can generate funds using a simple command after temporarily stopping the network. They explain that this approach guarantees consistency and significantly streamlines development, since local coin issuance is instant and under the developer’s control.

This part of the conversation clarifies why using a local environment is both practical and efficient. The hosts emphasize that minting eliminates unpredictable delays and grants total freedom to experiment with on-chain features. It saves time and helps keep projects self-contained. This moment is often the turning point for developers who find the local approach more convenient than connecting to public test networks.

### 20:00 - Registering an Identity

Once Dash is minted, attention shifts to creating and registering identities. The hosts walk through the command that sets up a unique identity on the local network, which is essential for writing data. They demonstrate how a single line of code can produce an identity and store it in an environment variable for later use, ensuring that scripts can reference it reliably.

They highlight how test net issues—like temporary network hiccups—are avoided entirely when working locally. The tone is optimistic as they show how easy it is to keep building forward at this stage. By removing external friction, developers can quickly iterate on their code, focusing on the core logic of their Dash-based application rather than battling transient network problems.

### 25:00 - Creating and Submitting Documents

With an identity in place, the presenters demonstrate contract creation and document submission. They discuss how a contract schema is defined in JSON, covering properties like message fields. Then, using a small snippet of code, they upload a document with a custom message to the Dash platform on their local network. This approach mirrors real production logic but keeps everything contained.

The speakers show the immediate return values and explain how the contract ID and document ID can be reused. They also note that topping up an identity helps guarantee enough funds for each submission, saving time otherwise spent diagnosing insufficient balance errors. This segment demystifies how to create, store, and confirm data within Dash’s decentralized architecture.

### 30:00 - Querying Data

After successfully writing documents, the hosts shift to reading them back. They demonstrate a simple script for retrieving data from the Dash platform using query commands. Although the example is minimal, it highlights how developers can store and retrieve messages or more complex structures. They talk about how data can be filtered or limited by query parameters, even if they opt for simpler universal retrieval in this tutorial.

They also mention potential complexities in advanced usage, like adapting MongoDB-style queries or dealing with restricted operators for different indexing scenarios. Nonetheless, the general takeaway is that reading data from the local network is quick, easy, and replicable. By combining these read and write steps, the entire lifecycle of a basic decentralized application is on display.

### 35:00 - Wrapping Up

As the session nears its end, the presenters briefly explore what else can be achieved with Dashmate and a local Dash network. They consider the possibility of integrating block explorers or specialized dashboards, recognizing that these are additional services that might require special configurations or external documentation. This open-ended conclusion encourages viewers to experiment further.

Finally, they summarize the strengths of local development: predictable funding, reduced friction, and a controlled environment for testing. By walking through wallet creation, identity registration, contract submission, and document retrieval, they have provided a solid foundation for newcomers. The hosts leave listeners with the confidence to expand their projects, build more sophisticated contracts, or connect other tools as they refine their decentralized applications.

## Transcript

[00:00] All righty. We are live. We should probably figure out whether we want to get
[00:09] a premium Twitch account so we can go back to our Twitter account so we
[00:13] can go back to streaming on Twitter. Yeah, we'll look into it. How have you
[00:22] been? Good. Welcome, everyone. Today we are going through a second tutorial that Anthony wrote
[00:33] on how to use Dashmate to set up a local development environment for Dashplatform. So
[00:41] Anthony, do you want to bring up that blog post and give it an introduction
[00:44] and then we'll dive right in. Yes. Whoops. Give me one second. Anthony has abandoned
[01:09] me here all alone with you folks. So one of the reasons that we're doing this is it makes it easier to develop applications if you have just a local
[01:17] network because 90% of what you're doing when you're building a Dash app is client
[01:25] side stuff and you don't really need a test network to test most of the
[01:35] functionality that you're going to be building with your application. But you do need some
[01:44] kind of backend service and so a local network will help with that. Okay, here
[01:58] we go. Yeah, so with Dashmate, I found that the thing that was most confusing
[02:09] for me is just kind of the process of like starting, stopping, resetting, restarting. There's like this whole set of different things you can kind of do, but that you
[02:14] can kind of ignore all of that if you just set it up and like
[02:23] set it and forget it. So over here, I already ran these commands because you
[02:29] see here the setup local commands. The first one you run, it takes about two minutes to run. At least it did when I did when I last ran it.
[02:36] And it goes, it kicks open Docker and starts a whole bunch of Docker containers. If we look in Docker just real quick, we see that we have like four running containers. We have a whole bunch of images and a crap ton of volumes. So ideally, you won't need to mess with any of this stuff. And if you
[03:02] do, you're probably gone pretty wrong. But once you set up local, that sets you up for the local group, and then you do everything through this group command. So dash group start, then that takes about a minute to run does all of that. And that's pretty much all you need to do to get it going. Now we
[03:31] will stop and restart. start. To do the minting. But the way I set up the tutorial is I first have you start it so that you can create your wallet. And you also have this group status command, which will give you the status
[03:56] of your local network. So you see here we got our local network, and it is up and then we have local one local to local three, and then this
[04:15] local seed thing. I know the local seed you use when you're minting. you're minting. So you're minting. So you're minting. And then I have some little explanations here for
[04:24] kind of the different ways of stopping, starting, restarting. and the dash mate group colon stop, dash dash force, that will be the one you'll use to stop and restart if you don't want to reset anything if you don't want to basically have to
[04:43] run the setup local command again. And then you can restart it, which is basically
[04:52] just like stopping it and starting it again. And then resetting is when you kind of like wipe the whole thing and start again, but there's reset with dash dash force or reset with dash dash force and dash dash hard, which does higher complete
[05:10] reset. And then reset. So this is kind of like the hail Mary if your
[05:15] thing is totally borked. And then well, so we'll do if it's really borked is I'll go into the dot dash mate folder and I'll blow this away as well because ideally you shouldn't have to if you the reset hard force should blow away
[05:33] your configuration. But I just, I just, I just found that sometimes if like I want to do a full full reset, you can delete that dot dash mate folder as well because this is what's holding your config here, which is like this huge
[05:50] giant file with all this config in it. Yep. And the dash mate group reset dash dash hard dash dash force does not blow that folder away is what you're
[06:01] saying. Exactly. Yeah. And it should get further. You can just, yeah, do that. Yeah. It should like reset your config dot JSON file, I believe is, is what it's
[06:13] supposed to do. So, um, for the most part, like I said, you're, you're not going to run into a lot of these issues unless you're having to stop and
[06:24] start and restart a lot. Or if like you kind of, you know, leave a project for a week and then like come back and your dark containers may or
[06:33] may not still be running. So that's where just some of this kind of like
[06:39] maintenance stuff comes in. But if you're kind of just going through the happy path,
[06:47] then you're, you're usually going to be in, in pretty good shape. Um, so let,
[06:50] okay. So you have, you have installed all the prerequisites, which would include Docker, which
[06:57] would include node. Uh, you'd have, you, you went through the system, system requirements checks
[07:06] to make sure that you meet all of those system requirements. And I installed dash
[07:09] mate globally. Yeah. Scroll all the way up to the top. Just, I'm not sure that we actually showed the very top just so that people can get an idea.
[07:16] We're at your website. First look at dash mate, first look dash mate. Um, and
[07:27] we have an outline. We've been overview. Um, we have prerequisites. Like I just said,
[07:34] no Docker dash mate. You've installed all of those. Uh, and then globally installed dash
[07:39] mate as well. Yep. Yeah. So that was, so that was all we did to,
[07:45] to get started. And then you'll know you've got it working where you can run
[07:50] this dash mate help command. So there's your, your dash mate command. So the, the surface area of dash mate is actually pretty small if you're not needing to get
[08:02] into the guts of it. And if you like, if you don't need to deal
[08:07] with SSL or, or things like that. So really it's mostly just set up, start,
[08:15] and then all the group commands that you need to deal with. Yep. Okay. Okay.
[08:18] Okay. Okay. So you've already also run the groups. Uh, yeah, maybe just go a little bit slower on the tutorial side, just so that people see which commands you
[08:32] run. We don't have to read the paragraphs, but. Yeah. So we had dash mate
[08:38] set up local. So that ran this thing right here. Yep. And then dash mate
[08:47] group start. Just this command here. You'll know it works if you get all checks,
[08:53] basically. And then dash mate group status. Okay. Gives you the status of your network.
[08:59] Okay. Uh, now I'm not, I don't expect you to know this, but just in
[09:08] case you do, I actually don't know this, um, in terms of how the local
[09:13] setup works. But I believe, um, based on what I know from using the SDK
[09:21] and whatnot, uh, on test net that. You, you need this seed node. And then the seed node essentially does the work of giving you a URL to contact and
[09:32] get a list of master nodes. And in this case, it would be one of
[09:36] those three nodes that you've set up. That's all you have to choose from because
[09:39] it's a local network. And then you do your further communication with one of those
[09:42] nodes. Do you know if that's how it works on this local setup as well
[09:49] as how it's done that with test net? So if by URL, are you talking
[09:53] about this? Uh, potentially, um, we would have to look at what the seed node, uh, port is when we set it up, but we don't have to go through
[10:05] that today. It's just in case you happen to know what it was. Um, so if you go into our config, I think I might, we might see what you're,
[10:16] what you're talking about. Um, so let's, uh, let's, uh, whoa, this is thousands of
[10:28] lines long. Okay. So yeah, the config is, the config is gnarly. I tried to
[10:37] go in here and understand what was, what was happening. And if you kind of
[10:44] go to the top level, you can get some sense of what's happening here. Um, we won't go too far into this, but just in case people do need to
[10:52] mess around here, you have a whole bunch of configs. And this is basically when
[10:55] you're running those first couple of commands. These will tell you like whether you're setting
[11:00] up for main net test net local. So the ones we need to worry about
[11:07] is basically local and then local one, two, three, and local seed. So I'm not
[11:13] sure what you mean when you say URL, what URL you're referring to. But, um,
[11:15] looking up that local seed. Yeah. Yeah. Uh, okay. So Docker network, subnet, uh, insight,
[11:34] keep going down p2p, RPC, minor dev net log, platform. Um, okay. It's even got
[11:49] the metrics drive. Yeah. I'm pretty sure it was the, the Dappy thing. Um, yeah.
[11:54] If you see that, that that's showing up a lot in here. Yeah. Okay. Yeah.
[12:01] I think, I think that's the case. So we can, let's see, you don't have
[12:06] too much further to scroll. So you might as well just scroll to the end.
[12:09] Yeah. Setting up DPNS. These are the dash, the contracts, uh, contracts, a whole bunch
[12:19] of withdrawals. And then dash mate itself. And then you got this. I don't know
[12:27] what this is. Yeah, I don't, I don't either. Uh, so, but we have 3,300
[12:34] lines of, of config file. Okay. So, um, fun stuff. Yeah. Let's go back to
[12:42] the tutorial then and, and just kind of work our way through it. Yep. Okay.
[12:44] So I've got a project here. I also learned this handy dandy new command here,
[12:54] which is, um, we were using this before to set our type to modules for,
[13:01] um, ECMAScript modules. And I learned that you can do the same thing for your
[13:04] scripts. So there's one point in the other tutorial where people would go in and
[13:08] copy paste a whole bunch of scripts. Mm. You just run this command. Hey, yo,
[13:13] look at that. Brand new scripts. Very nice. NPM hints. Yeah. And we got, so what I did is I like used, um, the Kale's tutorial a little bit and
[13:26] then kind of molded it with some of my own, basically how I set up
[13:33] some of these files and commands from the last one and created just like a
[13:39] super duper streamlined getting started. So the, the last one we did, it's like runs
[13:44] through all the commands, get you like a whole crud set up. You have like,
[13:48] you know, 15 scripts, script files by the end. Whereas this is just going to
[13:54] get you a wallet, get you an identity, get you a contract, submit documents to
[13:56] that contract. That's all. That's all we're doing here. So this can get you from
[14:05] like, you know, 0 to 50 and hopefully like five minutes or so. We're, we're taking our time in this, in this video, but you could run through this whole
[14:09] tutorial in like five minutes, probably. Yeah. So, so the scripts that you've set up
[14:16] in contrast to the other one where we did a lot of reading, uh, you
[14:19] know, scripts just to read the, the, the blockchain. This is mostly writing or we're
[14:25] creating, registering, creating, submitting. And then only the last one is actually just getting a
[14:28] document. So that's probably, I think a good call. Um, let's open up. Do you have, do you have a reference to Mikael's, um, blog posts in your blog posts?
[14:40] Or, um, so when I was writing this, he just had that gist. Um, I
[14:47] don't, I couldn't find his medium. So I'm not sure what medium he's referring to
[14:50] that he's publishing on. He may not have published it yet. So I'll, I'll check
[14:54] with him. But either way we can keep. Yeah, I will definitely once, if there
[14:59] is a link for that, I will definitely reference it right up at the top.
[15:01] Cool. All right, let's get going then. Yeah. So for this, um, I, I set
[15:12] this up so you could run this create wallet command as many times you want.
[15:13] And it'll always create you a new wallet. because it has the client in here
[15:22] with mnemonic set to null and offline mode set to true. But you do need
[15:27] your, your local network to be running for this to work. If your local network
[15:31] is not running, then this command will fail. Okay. So you should be able to
[15:38] run this and have it work. So this is the only part of the tutorial
[15:44] where you might get a little bit of weirdness happening because there is going to
[15:49] be a second we're going to have to stop and start this thing. But basically,
[15:54] for some reason, the mint command doesn't work when the network is running. I'm not
[15:57] really sure why that is. It's kind of obnoxious, but I'm assuming there's a good
[16:01] reason for it. You know? Yeah. We'll look into it. Um, Mikael was saying the
[16:06] same thing. He didn't know either. Yeah. Okay. And then we're going to set up
[16:18] our client and this is now going to have our mnemonic set from what we
[16:20] just created. And also, um, wait, I need this too. So this is really important.
[16:27] This is what we're just looking at in the config. This is what the local
[16:37] Docker network is kind of exposing the local network to you through this HTTP 127.0.0.1:3001
[16:43] port. Yep. Now we're going to do these guys. So dashmate group stop force. This
[16:56] will stop your network. And then this mint command, this is the best part of
[17:04] the whole tutorial. No more test net faucet. So happy about it. Yeah. Yeah. That's
[17:12] great. Very predictable. Yeah. Yeah. Once, once I finally got this whole thing set up,
[17:19] I'm like, oh man, I'm never going back. This is now I'm just kind of
[17:25] messing around and, you know, want to create contracts and stuff. I can just go
[17:29] from zero, zero to 50, super fast. So what I did is I grabbed that
[17:33] address from here. And the command has a address flag that you could feed it
[17:40] an address. And then you need to set config to local seed. So now for
[17:49] your run, this is going to generate your dash. And now this is while the
[17:51] network is stopped. And that's, that was that thing that you noted before. So you
[17:54] did the stop. Now you're doing the mint. And then after this, presumably you'll start
[17:59] the network back up. Yeah, exactly. So I've got that very clear here in the
[18:03] tutorial. The mint command is surrounded by stop and start commands. So hopefully that will
[18:09] not throw people off. Yep. Okay. And now we're back. We're back up. So pretty
[18:18] smooth process. If you do the command in the right order and you know what
[18:25] commands to do when. So now I know that you, you have, you have this
[18:30] plan here. You got your, you got your tutorial. I do want to go off
[18:37] script a little bit, since this is kind of how we're, we're doing it. We're not, we're not going to try to make a very streamlined 15 minute video here.
[18:43] I think right now we could potentially do that with some editing and whatnot. But
[18:52] I do actually, I'm just curious if you can open up an insight server. Um, if it should be running right now, based on what I saw in the configs,
[18:59] just, just need to find out what port and URL it's running at. Um, because I, I just like to see on a insight server, those 50 dash that you
[19:12] minted. If the, if it's picked up on the insight server. Okay. I don't know
[19:19] what you mean by insight server. So insight is the block explorer. Ah, you know
[19:25] how we usually open up a block explorer. Yeah. There should be some service running
[19:32] the block explorer on this. Interesting. Yeah. Cause so there's the dr ps command, which
[19:42] will show you everything. I, I don't know what to do with this. I wouldn't, um, I know when you did, uh, like 80 minute long stream with McHale, he,
[19:49] he was doing this a lot and he was going into like, he was picking
[19:54] certain ones and he was running like, like, like you could do, you know, Docker
[19:58] logs with one of these. Yeah. Um, I had the only way that I would
[20:05] know how to find it is to go to, go to the config file again.
[20:06] Okay. And then do a, do a page find for insight and see if we
[20:16] can find a URL that it's running at, that that service is running on. Alrighty.
[20:19] And if we don't find it there, then, uh, you know, I I'm kind of
[20:26] out of my league, uh, just on a live stream here. Yeah. We could just
[20:34] real quick, check the dash mate docs. And there's this nice dash mate.org website, nice
[20:43] little landing page. And also I like, I like this. I've never seen this diagram
[20:48] before, but this is pretty cool. This is actually just useful for understanding dash platform
[20:52] at all. Absolutely. Yeah. Um, let's see. So this takes us to docs.dash.org. The user.
[21:03] Yeah. I want them. I want them repo though. Cause this, this page is a
[21:09] whole bunch of screenshots and stuff. It's, it's not super great. Yeah. Let's see. This
[21:17] will hopefully take us to. The actual thing. Okay. And this is actually, this is
[21:22] the first time I tried to use dash mate. I went here. Um, the, the
[21:27] commands are just not in order. That kind of makes sense. sense. So it's one
[21:34] of the things that, you know, I wanted my tutorial to, to do. do, but
[21:37] if we check here. Um, yeah. So there's this Docker compose inside API file. Um,
[21:49] we're not running Docker compose right now. So I'm not sure if this is actually,
[21:54] I think dash mate might run it for you though. So if we could just
[22:02] check, um, one 27.0.0.1 and then figure out what that port number is. Um, I
[22:18] don't know why there's, why there are two colons though. Colon core insight port and
[22:25] then core insight port again. Oh, error. Something. Uh, yeah, I don't, I don't, don't
[22:34] know Docker compose enough to, to figure out why there's. two port numbers tacked onto
[22:41] that, but, but that's, um, that's, I think the, the number, the port number we'd
[22:46] have to find in the back in the Jason, uh, config file again. And I
[22:47] think it was there. I was looking for a URL last time we looked there,
[22:57] but it's just a .001. So we know that. So if you open up a
[23:06] web browser. And do what? Um, and either go to local host or 1, 2,
[23:19] 7.0.0.1. And then colon something, just go to the, just drop the colon for now.
[23:24] Okay. Can't be reached. Okay. So maybe this is, maybe this is, um, barking up
[23:34] the wrong tree here. We can keep going. I just wanted to check and see
[23:37] if that was easy. Yeah. Yeah. You should ask Mikhail. He'll probably have a better,
[23:44] better idea of that. Yeah. I would, I would be curious if you could get
[23:50] into some sort of like locally running explorer. That would be pretty sweet. Yeah. Okay.
[23:56] So we are about to register our identity. Okay. So now these are commands from
[24:09] my last tutorial. This is really simple one. You're just running dot register on identities
[24:19] and then console logging out your identity. And this is the command where, this is
[24:25] where test net would usually fail on us if test net were to fail. So now that we got everything local, this is no longer a scary commands to run.
[24:32] So that's cool. Yeah. We've got our identity. Putting it in the environment file. So
[24:49] that now subsequent scripts will refer to that identity file. Okay. And now we've got
[24:53] our create contract. This is basically the same contract from the tutorial, which is from
[24:59] the dash docs themselves. It has you create a note, which is type object and
[25:07] it's just a little JSON object with a message. And that message has a string
[25:14] type, which will contain whatever message you want to write. And then we have also, so I used to have this console log here and that would throw people off.
[25:22] So it would give you the contract ID before it finishes running. I forgot how
[25:26] to, how to fix that. You just put the console log below the last step.
[25:29] Yep. Yep. Yeah. People would be thinking that it's done because it returned something, but
[25:36] it hadn't actually finished. Yep. Exactly. Yeah. So now we got here, we have our
[25:45] contract ID and our contract. Can you go back to the script again real quick?
[25:48] Yeah. Contract ID, contract to dot to Jason. So before, did you also change this?
[26:00] Because I think before you were just referencing the name, like from the environment file
[26:05] instead of from the variable, but maybe I was wrong on that. So I was
[26:10] just double checking to see. We can find out. It may not have been the
[26:23] contract one either. It was just one of them. There was one where it was
[26:30] grabbing the data from the environment file instead of from the network. And it was
[26:37] like a false positive kind of thing, but we can look into that later. It
[26:38] looks like here. It looks like he's doing the same thing. Yeah. Okay. Yeah. All
[26:45] right. Moving on. All right. So our contract is created. Now we can. So now
[26:56] you need to update your client. Very, very important. Okay. This is what lets you
[27:13] use this nice little query syntax with hello world dot note. And then this will
[27:19] be our submit documents man. Oh, this is doing is this is now going to.
[27:26] Oh, and so here I put the top up command right in there so that
[27:33] every time you submit a document, it tops you up a little bit. This is obviously not going to be a good practice once you're, you're dealing with real funds,
[27:40] but just here on test that since dash is free. Anyway, this just ensures that
[27:48] you're never going to run this command and not have the appropriate credits or duffs
[27:54] in your, in your wallet or in your identity, I should say. Okay. And then
[27:59] it's going to give you a little message. Hello from dash local network. Oh, wait.
[28:04] Um, I probably didn't save my identity. Oh, no, I did. Let's see. Interesting. Hello
[28:20] world. I didn't expect buffer. Let's try hard coding it. Oops. Okay, I must have
[28:58] messed something up somewhere. I wonder if you. It may be an API change as
[29:06] well, because we're now running. Let's go to the pack and package to Jason file.
[29:11] We're running the most recent one 16. But when I wrote this tutorial, I was
[29:16] using this version. I'm pretty sure. Okay. Okay. So it shouldn't be an issue. Actually.
[29:24] Oh, wait. Oh, wait. Oh, I did it wrong. I didn't say the contract ID.
[29:28] Do. Do. Okay. Yeah. This happened a couple times in the streams when people didn't.
[29:33] Just not following your own instructions. Yeah, exactly. Yeah. Yeah. Okay. Yeah. Okay. Great. So
[29:38] now we see here. we'll make sure to save this one this time. document ID.
[29:40] document ID. Boom. Boom. Boom. Boom. Boom. Boom. Boom. Boom. Boom. Boom. Boom. Boom. Boom.
[29:50] Boom. Boom. Boom. Okay. Yeah. This happened a couple times in the streams when people
[29:57] didn't. People didn't. Just not following your own instructions. Yeah, exactly. Yeah. Okay. Great. So
[30:06] now we see here. We'll make sure to save this one this time. Document ID.
[30:10] Boom. Boom. Okay. So now we see here. This is our document and there is
[30:19] our message. So just so we can get the full experience. I did have one read command in here just to make sure your full end to end thing is
[30:28] working. So now we have our get documents command. This is going to run get
[30:38] on hello world dot note and it will give you all the messages. If you put this to like five and you have 10 messages, it will only show you
[30:42] the first five. Here we'll see. Nice little message there. Hello from national network. So
[30:50] there you go. That's the whole end tutorial. Yeah. Cool. Can you go back to
[31:03] the get document script again just one more time? Mm-hmm. So I'm not using the
[31:16] where command here. So we have this dash query syntax, which I found a little
[31:29] bit confusing and a lot of weird stuff kept happening. Let's see. Where is, I
[31:37] want to go to platform docs. There's a query syntax. So I also, I never
[31:45] was a Mongo person. I always did, you know, Postgres relational kind of databases. And
[31:52] so I think this is kind of like a Mongo thing. So I know Grove
[31:55] DB is a bit like Mongo DB. So this where syntax is kind of ways
[32:01] to like grab specific fields. So you see here, you have field name operator and
[32:09] value, and there's like really specific things you have to do in terms of like,
[32:16] you know, so we see here, there's like only one range operators allowed the query.
[32:19] The in operator is only allowed for the last two index properties, like all these
[32:25] weird, super specific esoteric rules. So I, I found this extremely hard to, to work
[32:30] with and deal with. So maybe that's just because my background didn't prepare me for
[32:34] it. But, um, this is one of the ways you can, you can query. So my script is not, is not doing that is just grabbing everything and then spitting
[32:45] it all out for you. Yeah. So in theory, you could, you could have better
[32:53] performance by including the, the where and the different queries, uh, query limitations filters on
[33:00] your query itself, because then you'd be returning less data from the network. But in
[33:07] practice, that's not going to make that much difference. And if it's easier to you,
[33:14] if it's easier to do filtering in your, uh, JavaScript syntax instead, then that's fine.
[33:16] You just, you're, you're putting more data over the network though. And, uh, we don't
[33:26] really have a way to prevent people from doing that because the queries are free.
[33:27] So, um, yeah. Yeah. Yeah. Reads are always cheap with blockchain. Yep. All right. Um,
[33:35] cool. That's, yeah, we, we got through that relatively quick. I wonder if we want
[33:46] to play around with anything else. Like what I would like to see as, as
[33:53] a users, I'd like to, to be able to, to see the different, um, the different UI services as well, and, and be able to have those at my disposal.
[34:01] So not only the, the insight UI, uh, the block explorer inside block explorer, but
[34:09] also Grafana and metrics, other metrics. I know that it's, I saw some things about
[34:18] that in the configuration file. So I'm assuming that it spins up those services. It's
[34:26] just how to access those, uh, from, from the browser. That's the only question. I
[34:39] don't know if we looked thoroughly on the GitHub documentation, but let's just, yeah. Do
[34:42] a fine for insight. Yeah. So we, we've done that. That's what got us this,
[34:50] that Docker compose, but it's not in the actual documentation is what I was looking
[34:51] for. Like, yeah, it does, doesn't seem like it now. Okay. Well, we'll, we'll look
[35:03] at that off stream, I suppose. Um, yeah, yeah, there are. Yeah. I see things
[35:21] like metrics in here. Let's see. So. Yep. 90, 90, 90, let's try that one.
[35:34] Yeah. Yeah. Cause I don't think these, none of these, like, it's an issue with
[35:40] Docker. Like, I don't know if Docker is actually exposing them to the outside world.
[35:43] Yeah. That's, that's not, that's what I'm saying. It's like, you can't just kind of
[35:50] like go to these, you know, some port numbers and run them in your, like
[35:54] you would, if you're just running, like, try, try localhost. I don't think it's going
[35:57] to work, but just try localhost port 99. Same thing. Yeah. Same issue. Okay. We'll,
[36:04] we'll look into that later. Anything else you want to go through over the stream?
[36:07] Let's look, let's look again at your, um, at the tutorial. Did we, did we
[36:14] make it down to the bottom in terms of, yeah. Yeah. Yeah. Um, I, I still just kind of like write a little, you know, conclusion and, you know, call
[36:19] to action or, or whatever, but, but that's pretty much, pretty much it in terms
[36:25] of the, the tutorial. I'll, I'll probably have a link actually at the end back
[36:30] to the first one set, you know, if people want to kind of go deeper,
[36:34] but, um, yeah, I like this. I like this setup. Cause, um, whenever I did
[36:40] want to kind of do anything with the dash network, I would kind of run
[36:43] through my other tutorial. And now this is like an even more kind of streamlined
[36:47] way of doing that. I might even make like, make like a little cheat sheet.
[36:49] That is just the command and codes and throw that in a gist. So if it wants to get up and running in like 30 seconds, they could, they could
[36:57] do that. So it was kind of like this slow, like whittling process of me
[37:03] kind of understanding how to, how to work with the network and then how to
[37:08] kind of get it down to its base functionality and, and really simple reusable ways.
[37:11] So, so yeah, I'm feeling, feeling pretty good about like my current knowledge of dash
[37:16] platform and, and how to work with it. So that's good. Yeah. It's a great
[37:22] tutorial as well. So thank you for putting that together and for everybody else. Thanks
[37:30] for joining in and we will see you later. Yep. Bye everyone.