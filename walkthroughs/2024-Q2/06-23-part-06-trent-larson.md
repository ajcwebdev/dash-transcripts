---
showLink: "https://www.youtube.com/watch?v=kH7X1w5g7_E"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Platform Walkthroughs Part 6 with Trent Larson"
publishDate: "2024-06-23"
coverImage: "https://i.ytimg.com/vi/kH7X1w5g7_E/sddefault.jpg?v=66785aa4"
---

## Episode Description

Trent Larson, an experienced developer, explores Dash Platform's features and potential applications in land governance, encountering network issues during the walkthrough.

## Episode Summary

In this episode, Trent Larson, a long-time cryptocurrency enthusiast and developer, joins Ryan to explore Dash Platform's features. They discuss Trent's background in crypto and his current work in land governance. The walkthrough encounters technical issues due to network maintenance, preventing full completion of the tutorial. Despite this, they cover key concepts such as identity creation, name registration, and data contracts. The episode concludes with a discussion on blockchain data availability and Dash Platform's approach to providing easy access to blockchain data with proofs.

## Chapters

00:00 - Introduction and Guest Background

Trent Larson is introduced as an experienced developer and long-time cryptocurrency enthusiast. He shares his journey in the crypto space, starting from discovering Bitcoin in 2011 to his current work with Medici Land Governance. Trent discusses his involvement in various crypto projects and his interest in applying blockchain technology to real-world use cases, particularly in land title management.

05:47 - Setting Up the Development Environment

The hosts begin the walkthrough of the Dash Platform tutorial. They discuss Node.js versions and set up the development environment. This chapter covers the initial steps of creating a new project, installing dependencies, and configuring the necessary files for interacting with the Dash Platform.

16:59 - Creating Identity and Registering Names

This section focuses on creating an identity on the Dash Platform and attempting to register a name. Due to network maintenance issues, they encounter difficulties in completing this step. The hosts explain the concept of identities on the platform and how they relate to usernames and document management.

30:04 - Data Contracts and Document Management

Although unable to practically demonstrate due to network issues, the hosts provide a conceptual overview of data contracts and document management on Dash Platform. They discuss how data contracts work as schemas for documents, and how this could be applied to real-world scenarios like land title management.

46:11 - Grove DB and Blockchain Data Availability

The discussion shifts to Grove DB, the database used by Dash Platform. They explore its features, including proof systems and indexing capabilities. This leads to a broader conversation about blockchain data availability and how Dash Platform aims to provide direct access to blockchain data with proofs, potentially eliminating the need for intermediary indexing services.

54:49 - Concluding Thoughts and Future Prospects

The episode wraps up with reflections on the current state of the Dash Platform SDK and the potential for improvement. They discuss the upcoming mainnet launch of Dash Platform and express interest in future collaborations to explore real-world applications, particularly in land governance.

## Transcript

[00:00] All right, welcome back. We got part 6 - walkthroughs with Trent Larson. What's up Trent?

[00:08] Hey, good to be here

[00:10] Good to have you Trent

[00:12] As opposed to most episodes. I I do know the guest pretty well today because this is one of my good friends and colleagues

[00:21] Trent we've known each other for I

[00:24] Don't know seems like 10 years on and off

[00:27] we don't do a ton together, but we've rubbed shoulders in the

[00:31] crypto context as well as

[00:33] Tech, you know in general

[00:36] Trent I I know

[00:39] About you, but you know about you more than I know about you. So I know that you are basically an og

[00:47] Bitcoin er and crypto person I was

[00:53] Surprised but not surprised to see I scrolled through your Twitter account your ex account and I think you were talking about

[01:00] Bitcoin way back in 2010 or 2011 or something like that

[01:05] I would love to know how you discovered it back then how you got into it

[01:08] Yes, so introduce us to to Trent a little bit. Tell everybody who you are. Yeah. All right, so

[01:14] Yeah, I love computer science

[01:17] you know been programming for a while I so I went and got my PhD in computer science in 2002 and

[01:25] After that decided hey academia, you know, it's cool, but I feel like I don't really know industry

[01:30] So, you know started working in industry then

[01:33] As for finding Bitcoin, I don't know. It's just another one of those random things that

[01:39] like you stumble upon nowadays in github from somebody else's projects and

[01:45] So I bought I've never been able to mine. I do remember buying just hey, okay

[01:51] I got to buy some of this and so I bought some in 2011 and

[01:55] I tell people that you know, I've lost more than I'll ever own

[01:59] It's just it was hard to get you know, people would fall through and so anyway, you know

[02:05] wish I'd of course bought more just like everybody else, but

[02:08] 2014 is when luckily I was able to join

[02:13] Overstock with Medici ventures and they created the first

[02:16] crypto based exchange in 2016 and you know with Ryan we were going to you know meetups back at the

[02:24] in the day, and I remember - ones at the beginning and

[02:28] so anyway since after

[02:31] You know t0 is still something that's out there and running but I was lucky enough to join this side project

[02:38] Medici land governance and

[02:40] It's been focused on writing land records to chain. And so that's

[02:46] Where I still am employed

[02:49] I'm doing other side things with identity and cryptography and that's fun. But that's that's so you so you work on crypto full-time. I

[02:57] Don't work on crypto full-time because it's really hard to

[03:05] Get you know that this title story

[03:09] Into government

[03:13] So most of my time and actually I think this is pretty common

[03:18] Even though you work in crypto most of your time is spent in traditional engineering. Yeah, sure

[03:23] Yeah, that's kind of why I'm here is I'm a web dev who is into crypto also. Yeah. Yeah

[03:28] So we're trying to apply it everywhere. We can we have a really exciting project right now in Baltimore that may spread out

[03:34] So I would say that I I do crypto as much as possible, but my day job, you know, it's it's trying to engineer

[03:42] Around it and and with it so that people can actually use it

[03:46] Yeah, and we've we've spoken pretty extensively about some of the opportunities that you're one of the unique

[03:54] guests on the show in that

[03:57] You have a real use case in your actual job that could actually leverage - platform

[04:05] depending on

[04:07] How things work out?

[04:09] In the real world and so I'm excited to have to introduce you to - platform

[04:14] You don't need an introduction to - itself because you've been you know around for a while

[04:19] But let's go ahead and get your screen share

[04:23] going

[04:25] Just so that we can jump into that topic

[04:27] but yeah, thanks for thanks for being on and

[04:30] I also wanted to just mention briefly before we get started that - platform is

[04:36] Officially going to launch I believe June

[04:42] 29th

[04:44] On mainnet, so it passed it. Yes. We did have a proposal that was talking about

[04:52] Talking about whether we should launch it, even though all the features and all the thing all the buttons aren't necessarily snapped up

[05:00] But it's a good enough

[05:03] Minimum viable product and we and getting it on mainnet is a good idea

[05:07] So we had a time for the the two of us will go through this tutorial and we'll just change network to mainnet and see

[05:14] What happens?

[05:15] Yeah. Yeah, so I don't know if I happen to accidentally say June

[05:19] But I meant July and I'm pretty sure it's 29th and Anthony you and I I don't we haven't decided this yet

[05:26] but I'm pretty sure that's what we're gonna be talking about tomorrow and our

[05:30] later weekly because we have a blog post from

[05:33] Dashcore group that I want to go over and just read the whole thing and discuss it. So that would be awesome tomorrow

[05:41] But yeah, very exciting stuff. We're actually going to mainnet. So

[05:47] Right now unfortunately, we're still dealing with the finicky test nets to some degree finicky

[05:53] and we're gonna hope that it works out for us today, but we'll

[05:56] let's get started and we'll try to go as quickly as we can through this today, so

[06:02] Trent go ahead and

[06:06] Take the reins

[06:08] And looking through the the post here. You can see the table of contents just

[06:14] Give you give you us a rough idea of or give yourself a rough idea of what we're gonna go through

[06:19] But let's just scroll down and and get started on the first step. Okay. Yeah, I have been scrolling and it's not showing on the screen

[06:27] so, let me see if

[06:29] I'm going to

[06:32] Let's see, I've opened up Chrome Chrome's not showing on my screen either. Oh, no

[06:37] We thought we thought we had to fix this

[06:40] Yeah, we did actually go through this Creek show. Can you get your editor up?

[06:44] it is up and

[06:46] showing it right now and

[06:48] so

[06:50] And you you'd had the extra monitor. So maybe if you just like disconnect that that might help disconnected now

[06:57] So why don't I leave and come back in? Is that sure? Sure

[07:01] Not so we get to vamp for a while I guess yeah totally

[07:07] Yeah, no, that's um, super interesting the the land title stuff. I remember this is the thing that came up in the there was like a

[07:15] Smart contract on aetherium that had like the first home deed that was like maybe like four or five years ago

[07:22] So I'm very interesting use case

[07:24] Yeah

[07:27] Yeah, and the biggest challenge with that is obviously getting

[07:32] Governance governments to recognize it. So let's let's hope that trans able to make some inroads there

[07:38] So we see you back now Trent and we see the screen. It's currently showing the three of us

[07:46] With

[07:49] No

[07:52] I'm scrolling through the blog post

[07:55] You're not able to see it. So I could continue and talk through but

[08:02] well, Anthony you you could keep going and Anthony could do a screen share and just

[08:07] Show what steps that we're on I suppose. I don't know if that's that's maybe not a great idea

[08:13] best presentation

[08:16] Why don't I try doing this in Chrome I'm in Firefox right now, okay

[08:21] Actually hang out here

[08:28] We can try when you do join with Chrome like instead of sharing your whole screen try just sharing a tab

[08:34] Let's just play around and try a couple different setups. See what happens. There's three options

[08:39] There's whole screen window and tab and I would say try it try a window first

[08:44] instead of your whole screen

[08:57] Yeah, this is a weird one this has never happened before all right present your screen

[09:04] Oh

[09:07] Oh

[09:09] Oh

[09:11] Okay, so this is interesting

[09:39] on my

[09:41] Mac I

[09:43] was

[09:45] It looks like the settings

[09:50] Did not have permissions to share screen either on Chrome or Firefox

[09:56] Even though it did show the screen

[09:59] Are you able to see mice? Oh wait, we're not seeing anything right now. Your screen is not sharing at all on our end. Yeah

[10:08] And so are you able to update those permissions I was oh

[10:13] Here we go. And then do you see yeah, we're good. Oh, man. Thank God

[10:18] So that was the deal. I'm used to it not allowing a share for you know a screen share

[10:26] But usually it tells you this time like it shared my whole screen

[10:30] But then would never move and you I didn't know why and it's weird. Yeah

[10:34] Yeah, we're weird little ghosts in the machine, but um stream yards never let me down before so I figured we would eventually figure it out

[10:42] But exactly we're totally good

[10:44] So yeah, the code starts just past this the M set up and configured node project

[10:51] So actually just real quick before we start obviously, it sounds like you're a very experienced dev

[10:54] You got a frickin PhD in this stuff. What is your JavaScript experience though? I

[11:00] Prefer JavaScript. Oh great. Awesome. Can you just check your node version real quick?

[11:05] Yeah, and I could get whatever version we need

[11:08] Let's see. Let's just

[11:12] if you ever used

[11:14] package X

[11:15] No, I use Volta for my version management. Oh, I haven't heard of Volta

[11:20] Like this one. It's

[11:23] Affiliated with T and the guy who created homebrew and oh, yeah. He's a he's a crypto guy now

[11:30] Yeah, it's currently 21 5. So if that works, well

[11:32] That's why you're on an odd version, but that should be good. I

[11:37] Can switch to whatever version yeah, we need it's that we we it needs at least version 20, so you should be fine

[11:45] I've just never seen anyone run odd versions before

[11:47] Let's bump up your font also, okay

[11:58] Then if you could drag the window the other window the tutorial window

[12:03] past the

[12:06] our faces because

[12:08] Right now we see both. Yeah, there you go to distracting. Yeah, I know it's just

[12:14] Some you are is just like throwing me for a loop. Okay, so

[12:19] I'll just copy this whole chunk

[12:22] You

[12:24] Okay, let the timer start now it's a 427 so let's let's see how fast we can do this one

[12:39] I'm just kidding. We don't have to speed run through it, but I know that

[12:42] You're on a bit of a schedule today and it is pretty lengthy tutorial. So, okay fair enough. No, I

[12:52] Will let you know if I have to go so

[12:55] It's funny I'm reading this after I paste it in which is probably not the best practice so, all right

[13:02] Most of the people as we run this haven't read any of it

[13:07] All right, so create new script file individually

[13:19] Package JSON. So let's go and open this now with

[13:23] Hello

[13:28] Wait

[13:33] Let's try this

[13:37] You

[13:39] So I'm just gonna replace that

[14:00] All right

[14:05] I

[14:07] Import

[14:17] -

[14:19] Pass the projects network. And okay, so we're starting the app here

[14:24] This is called a API slash client dot JS

[14:29] All right

[14:33] all right, so starting a

[14:36] - client suite

[14:38] Get in your address. All right

[14:45] Create wallet - yes

[14:49] We'll let you get to a point where after you run a command

[15:00] We'll we'll talk a little bit about what we're we're doing, but we're almost there anyway, so yeah

[15:05] Sweet create wallet stuff is all

[15:07] pretty straightforward that's this is just you know, this stuff is creating a

[15:13] Reading a 12 word seed phrase and whatnot. Yep

[15:17] Right on just a heads up that

[15:22] the faucet is a

[15:25] little finicky, but hopefully we can get

[15:29] Get that going

[15:32] Okay

[15:33] All right, I'm putting these in my environment. Oh, so I'm copying this whole thing, right?

[15:38] Okay, add ones to faucet

[15:49] So now I'm gonna go to

[15:53] Yeah, right the the faucet broke for me in a new way this time so I'm having issues getting funds

[16:00] So we'll see what happens with Trent

[16:03] Okay

[16:05] Okay, they didn't give you the capture I had to click through the bicycles

[16:11] That's the wrong field. Oh, oh, yeah, the - address goes up top

[16:17] Is it masternode or masternodes for the promo code

[16:21] It's just masternode, but we don't necessarily need a promo code because we honestly don't

[16:27] Need that many coins anyway

[16:30] Let's see

[16:32] Yeah, just no, no, that's fine that that showed up the first time we did it's it's running up top

[16:39] So just just let that do its thing. Yeah, if the website crashes, that means it worked

[16:44] Sweet

[16:49] So you can you can open up a new tab and start checking out the

[16:55] Okay, I think you got the funds

[16:59] I don't know if I clicked on something. So if I search for that address now

[17:03] Hello, you might need to refresh that one as well sometimes it needs a refresh even after you go there

[17:14] Let's see, so that's also it might be telling you it's insecure

[17:20] So your browser might be blocking it if you just click over to the left

[17:24] It's it's not nation. It's not HTTPS. It's just HTTP

[17:29] Yeah

[17:31] There you go, so how can I force it to let me

[17:37] Good question, I've never actually

[17:43] We've never been this much on the this is probably firebox thing. Yeah, I didn't grow you were looking you were looking at

[17:51] You're doing the faucet still but let's let's check the insight

[17:56] The second tab in copy link

[18:00] Okay

[18:06] Seen this view before all right

[18:09] Yeah, cuz this is the same kind of Explorer

[18:13] We have watching the flow which is a another blockchain client. So we wanted to search for my address

[18:20] All right

[18:25] We're doing well today

[18:27] Great so the next one is the moment of truth. This is where we really find out whether the network's working or not. All right

[18:36] API client.js. So modify to include the wallets mnemonic

[18:42] Okay, I got that somewhere

[18:53] I

[18:55] Might as well just copy the whole thing. All right

[19:00] Yeah, okay

[19:05] Create identity

[19:09] Enough and

[19:12] Okay

[19:14] So, oh cuz my mnemonic is in the env file, okay enough

[19:29] Output oh dear. Okay. Here we go

[19:42] Mmm

[19:44] That's a new one

[19:49] You want to hit it McCale and ask him which IP address we should be using or we can try the one we used last time

[19:55] Let's try the one that we used last time for now

[19:59] I'm gonna also open up

[20:02] the Grafana

[20:04] See if oh, yeah

[20:06] Gotta find the link to that because I'm on a different computer now

[20:10] I

[20:12] Gonna have to look in our conversation because it's not a book the Grafana dashboard

[20:35] Do you have the IP address Anthony from last time I'm literally going through the YouTube video right now to find it

[20:41] Oh, I think I found it actually

[20:43] Okay, cool

[20:45] I'll paste it in our

[20:47] discord chat

[20:50] And let's see, I'm just gonna go ahead and click on that. Yeah

[20:54] So if you click on that it says method not allowed which means that the actual server is up. So that's actually good

[21:00] Okay. So now we just also have to find the the Doc's page that shows how to get it in. All right

[21:07] Let's go to a doc's dot - dot org

[21:12] And then go to open your hamburger menu

[21:26] Other one top left. Yeah, and then go to

[21:30] Scroll down or go to platform docs actually

[21:34] And then hamburger menu again this one. Yeah, and then under tutorials connect to a network

[21:43] and

[21:45] then scroll down to

[21:47] connect via address

[21:50] and

[21:52] Then we're gonna get that part the DAPI address into our client

[21:56] You can just put it along with the the rest of the info you have in your client

[22:00] So it'll be just the DAPI address part don't don't grab the whole thing

[22:07] Just this even even less just just that exactly yeah because there's a - dot client right there, okay

[22:16] Yeah, and then we just have to include the the IP that

[22:22] Brian gave us in the discord

[22:24] I'm guessing no slashes or HTTPS. Yeah

[22:28] Yeah, write it just like they got in the docs and then delete the other one and then rerun that man

[22:33] Yeah, I wish I had this kind of help on all my project setups

[22:45] We're pros at this by now. Like I said, this is part six

[22:49] So imagine how part one through four went

[22:52] What happened here and we'll know if

[22:59] What I'm saying is and it is useful at all in a minute here when this runs through but the previous node

[23:05] It could have been that what the DAPI client

[23:08] DAPI

[23:10] Decentralized API or - API. It looks like it worked. This is good

[23:13] It connects with a random

[23:18] Node

[23:19] Evo node is what we call them. That's running platform services. It connect it finds the list of them

[23:25] Connects with a random one and sometimes that random one is not

[23:29] healthy

[23:32] The SDK is not

[23:35] Very up to snuff. So it needs some work the SDK, but the network itself should be

[23:45] Pretty reliable because because it's it's pretty reliable using

[23:49] The rust SDK and other tools that DCG is more actively building

[23:54] but the JavaScript SDK

[23:56] For better for worse

[23:59] Yeah

[24:00] I would say I think it's been four out of the four out of the six we've hit this issue and two out of the

[24:05] four worked first time so

[24:07] Not a great record

[24:12] Okay, so anyway updating the the JavaScript SDK is something that we could tackle if we wanted to so just

[24:19] throw that out there in case

[24:21] somebody or you and trend are interested in doing some JavaScript SDK work, but

[24:26] that that probably needs to be given some love, but anyway, let's move forth with the

[24:32] with the tutorial so you got

[24:35] The command that we just ran was create identity and

[24:42] Essentially what create identity is doing is is creating a public-private key pair that is the basis for your interactions on

[24:50] - platform and how is that different from you know, just my

[24:55] Basic wallet that has my key pair in it. Good question

[24:59] Yeah, and I unfortunately I I don't know the details of this. So nor do we really need to

[25:07] know any of it for now, but I'm

[25:10] It's something that I want to look into because I kind of like creating it allows you to create a namespace on

[25:16] platform instead of the main the layer

[25:21] I don't know if layer 2 is the right term probably not but that's kind of how I think about it

[25:25] Platforms like this actual layer that runs on top that includes additional functionality including like your own namespace

[25:32] So we're ready to go to create your like a you know, Trent - kind of account, you know

[25:38] Separate things though. So the identity just to be clear is is

[25:41] A long string, you know of random characters and it's from what I understand. It is that public-private key pair

[25:50] I don't know exactly what curve it's using. I don't I don't think it's standard elliptic curve stuff

[25:57] public private key pairs

[26:00] ECDSA kind of stuff. I think it's different but

[26:04] Regardless that is the basis and then on top of that identity you can create

[26:10] You can create contracts you can submit documents to other contacts contracts that have been created and the - pay

[26:19] Contract is one of the flagship contracts that allows people to register a username on

[26:26] top of their identity

[26:29] so the identity you can have multiple identities and then each identity can have multiple usernames and

[26:36] Each username would have then a series of public-private key pairs used for actual funds. So that makes a lot of sense actually

[26:44] Is it the case that my original wallet seed?

[26:49] As long as I back that up and then if I reinstalled on another computer, I'll restore not only my address

[26:57] But also I can get these identities from that. Is that true? Yes. Okay

[27:02] Yep. Everything is derived from from the the seed phrase the 12-word seed phrase and the whole idea with this

[27:10] Naming thing is that you can have one username that's across different

[27:16] platform different

[27:18] devices your different devices and as long as you know that you have the

[27:21] Username Trent then you know that and you can access that then

[27:27] then that's all you need for all of your platform interactions and

[27:33] Payments, okay. So let's keep going. The next step is

[27:40] Identities

[27:48] It's most mostly just a sanity check to see that you can retrieve that identity that you just created right

[27:55] And

[27:57] Here we go

[28:04] In some ways I'm glad this is being recorded because

[28:17] You know if you've inserted any malicious code anywhere then you know, I have proof that it was you

[28:24] Through it and I want a copy of this record. Yeah, luckily there's been no changes to this code

[28:30] He has been few had five other people run through and their computers have not been owned unless I'm really playing the long game, right?

[28:37] So retrieved identities it got this one which looks the same as before, okay

[28:50] All right, one - is equal to 100 million duffs

[28:55] That way that's actually a typo I think that we need to fix that one

[29:01] no, that's true one - one - equals 100 million duffs as

[29:05] and

[29:07] Yeah, I wrote this with you telling me what to write. So that should be correct

[29:11] I thought we might have had a typo there, but I was wrong. Yeah

[29:17] One time I will never remember that conversion offhand. So

[29:21] Just think 100 cents 1 $1 is 100 cents. But instead of 100 it's a hundred million

[29:29] So obviously, yeah

[29:32] This is that one time Ryan thought that he was wrong, but he actually wasn't so

[29:37] Okay

[29:39] Dude knows you will apparently

[29:46] I've been wrong plenty times

[29:48] And

[29:53] again this this this waiting is mostly

[29:57] The SDKs issue. I don't think things are this slow on the actual network on the network side

[30:04] It has to do with settings. There's a configuration that you can add. I believe that will speed that up, but

[30:14] Yeah, maybe I'm good here update the the client to sync even less blocks than it currently is at right now that might help

[30:21] Well, it has to do with the storage adapter warning that you keep seeing running a node.js without any specific specified adapter

[30:28] We don't we're not storing any data locally. And so it has to

[30:32] Continually sync from what that's one thing that I've heard, but I haven't verified that

[30:38] but I think that's what that the purpose of that storage adapter is is so that you can

[30:43] you don't have to rescan all the blocks from the one that we

[30:49] Said was our beginning block in the configuration file

[30:53] Okay. Yeah now we've done this done this tutorial with a bunch of people. It seems like the things that if we could

[31:00] Upstream some stuff to the actual SDK. It would be better retries for the correct nodes

[31:07] So we don't hit those errors and then the the sync issue or that the general speed issue

[31:14] Yeah

[31:16] It's just very I mean

[31:17] It's an old it's pretty old code

[31:19] Because this has been got this project has been going on for a while and DCG has decided to to make rust

[31:25] The primary SDK so that's been their focus and incubator can take on

[31:33] Updating and improving the JavaScript SDK if we want down the road

[31:38] But right now it's good enough to get the core concepts like using this SDK is good enough to get the core concepts for now

[31:45] So it's probably okay

[31:47] Let's see if spaces are

[31:53] Should I yeah be brave or not? Sure. You put us no spaces are definitely not be allowed

[32:01] but I was just I was just

[32:03] Trying to yeah, let's let's let's skip the air. Yeah, I can tell you right now spaces are not gonna be allowed

[32:09] All right, here we go to register a name

[32:14] And then fire express buffer

[32:18] But it looks like it's still working on something that's weird

[32:27] Hmm

[32:29] Hmm

[32:33] Go go to your dot EOV again real quick for me

[32:36] Do you know if the the - the - is allowed in the the - should be allowed

[32:45] But um, we could try without the - to see

[32:52] Just say Trent man, like you you're the man. You're the Trent of - right? There's only one Trent in this world

[32:58] All right, so we should kill this then

[33:00] Yeah, all right

[33:03] All right. I will be the Trent on testnet. Oh, it's ran the same thing

[33:07] Okay, what's um, let's just let it let it finish

[33:12] Or at least let it run long enough so that we could see whether it's going to finish or not

[33:17] Give it like 20 or 30 seconds. Okay?

[33:20] Did run register name, right? Yep. Okay

[33:23] Go to your your register name file real quick. Just make sure we didn't like mess up mess something up in the in the copy/paste

[33:31] So

[33:36] We're added in it looks like your your thing is adding in some types

[33:40] Are those actually being written into the code or no? No, this is just a hint

[33:48] Just like this. It's not in the code. It's not a line. Okay, so that shouldn't be an issue then

[33:53] and

[33:55] Labels good labels good

[33:57] Yeah, you don't have any spaces in your dot EMV

[34:01] Interesting, all right, well, let's see see what happens, but the next thing we can try is just um

[34:11] Hard-coding your label right into the register name

[34:14] All right, you tell me when label in your process and don't you oh, yes you do and you you saves that that's not just hanging

[34:23] Right, it does automatically. Okay, and it does have a

[34:29] Marker on it over here when it's not

[34:32] Okay, everything

[34:35] Should be fine. Yeah, I think it should be fine. I think it should be fine

[34:40] when it's not. Okay. Everything should be good. Unless Trent was already taken maybe.

[34:52] The error came so fast that it makes me think that it was something in the SDK once again.

[34:57] And yeah, that's what I'm thinking too. We could try bumping it back to 12. I guess.

[35:08] Oh, what version are we running right now? We're running the most recent, which should

[35:15] be 15. But we've run this version with other people, and it hasn't been an issue.

[35:20] But let's try the 12 if this doesn't work, because that has given us better luck than

[35:28] 15. Are you talking this version?

[35:33] Oh, it is 12. Oh, because I fixed that in the instructions. That's right. That's why

[35:38] I wanted to give them the Netlify version, because I fixed that in the instruction. So

[35:43] yeah, so we're on the correct version, according to Ryan.

[35:48] Okay.

[35:49] Yeah, this has been hanging for a while. So I guess we try and just hard code it.

[35:58] Well, I don't think that's going to fix anything, honestly. But Trent, can you bring up the

[36:04] link? So go to the StreamYard, and there's a link for metrics.testnet. It's a Grafana

[36:14] link at the very end. Yeah. In the public chat, wherever that is, you don't... Yeah,

[36:23] comments. There you go.

[36:24] Yeah, bring that up. And let's see, let's do a sanity check on the network itself.

[36:33] He's going to have to log in though, right?

[36:37] Yes. The username is dash, and the password is platform.

[36:45] Blowing the secrets, Ryan. Now everyone can know when our network is down.

[36:56] Yeah, this is not responding for some reason. I've got networking.

[37:12] And I do know that they... Let's see. Yeah, it's not loading for some reason. Let me try

[37:29] it.

[37:30] This is the new one. Never got stuck on this step before.

[37:38] They might be... I know that they're getting ready to upgrade the network, and we may have

[37:43] run into the exact time that they're doing that, because I'm not getting it to load for

[37:48] me either. So it's not on your end, for sure.

[38:06] Interesting.

[38:09] Yep, definitely not working. Let me check the... Is there another step? What step did

[38:17] we get hung up on here?

[38:19] Register name. We got the identity. We topped up the identity, and then we're trying to

[38:24] create the label, which would be the trend dot dash. That's the register name function.

[38:33] Okay. And this... So we may not get too much further with this, but that's okay. We can

[38:43] always pick up from where we're at now on a later stream and do it again, because I

[38:49] am noticing that they... They, meaning Dash Core Group, they are changing testnet right

[38:58] now to run...

[38:59] Right now? The first time to live stream.

[39:03] As of two o'clock. That's what... Two o'clock. So two hours ago, or three hours now ago,

[39:11] it was the last message that I saw about this. So it might be likely that something along

[39:18] those lines is happening.

[39:20] I'm just going to send a message real quick to see if anybody's around. Let's see if...

[39:37] How is testnet right now? Should it be running?

[39:50] Gravana seems down. Yeah. So in theory... Yeah, in theory, testnet... Originally, early

[40:13] on in the days of Dash, it seems like testnet was more of a pretty stable place, like pretty

[40:19] stable network, but as we're approaching the Dash platform release, it seems like there's

[40:27] a lot more testing going on in testnet. So I guess the name is... It's living up to its

[40:34] name as a testing ground. Less people than I'd like, but...

[40:42] So on this step, if it were to work, should this label correspond to my name, in my case?

[40:53] Yes.

[40:54] Trent?

[40:55] Yeah.

[40:56] And then this view on Block Explorer, would this document be Trent?

[40:59] Yep. Let's just check out Anthony's and see if we're able to get that link to show us...

[41:07] So it looks like the test... The platform explorer is working fine, so that's one thing.

[41:12] But...

[41:13] Oh.

[41:14] We're loading the...

[41:15] It's not going to be just Trent. Like, you saw my document link doesn't look like that.

[41:21] Okay.

[41:22] So it's going to be your... Some sort of identifier.

[41:25] Well, this is yours, AJCWebDev.

[41:27] Yeah. And the URL corresponds to the identifier for the document, not the identity.

[41:40] Gotcha.

[41:41] So it's using... I think there's a contract that is used to create the name, I believe.

[41:46] Gotcha.

[41:47] Yeah.

[41:48] Okay. And where did you get that identifier? I don't see this in...

[41:54] So that's what's going to be output. So if you go up to the... Scroll up into the code,

[41:59] it'll give you your label and then view on Block Explorer. So scroll to the right a little

[42:05] bit. So it does the name, registration, dot, and then dollar sign ID. So that has to do

[42:15] with the... This is all JSON schema stuff. So basically, when you register the name,

[42:21] you get a JSON blob back with all this information, and that's what allows you to find it on the

[42:26] platform explorer.

[42:27] Yeah. So in the document here in the blog, you might put this inside here because that

[42:35] is part of the output.

[42:36] That's right. Yeah. Correct. Yeah. But then you can't click it as a link in a blog. So

[42:44] trade-offs.

[42:45] Good point.

[42:46] Yeah. This has been hanging up like five minutes now, so this is clearly not going to work.

[42:51] Let's go back to the tutorial and just kind of do a conceptual overview of what's doing

[42:58] it, what it's doing here. Because Anthony gives all the outputs that we would see anyway.

[43:04] So just kind of scroll through here and then see the idea.

[43:07] Yeah. This is the JSON blob I'm talking about with the ID and all that, you know.

[43:13] ID, yeah. Okay.

[43:19] So the next step would be creating a data contract and then doing basically CRUD on

[43:28] a data contract, create, create, update, delete. And then after a data contract is created,

[43:36] you can think of it as making a schema that all other documents would adhere to, just

[43:45] like a database schema, using an SDK or rather-

[43:50] Can you hear anything in my background, by the way?

[43:53] Yeah. We hear a little bit of opera. Yeah. No, that's fine. Which is awesome.

[44:01] As much as you appreciate the entertainment.

[44:03] It's over here. That's why I keep waving to make it easier to hear me. Okay. So the

[44:08] scheme is defined. Yeah. In the, okay. In the contract. That's kind of cool. We can

[44:19] retrieve the contract. Okay. And you can update the contract. Okay. So that's updating

[44:37] the contract. So is this submit note document going to be utilizing that same contract?

[44:44] Yes. So this will be a document against that schema or contract. And now I changed it.

[44:52] So now it gives you your, your own name instead of AJC web dev. That was one of the other

[44:56] changes in this. Oh, good. Good. It's too bad we can't actually test that, but that's

[45:02] updated. Okay. And then you'll actually execute that

[45:08] contract I assume. And here we go. I'll put, okay. Yep. So this is able, were you able

[45:17] to get in touch with anyone Ryan in terms of like actually confirming that nobody, nobody's

[45:22] responded on that. So we'll just continue with the conceptual overview. And then I'd

[45:28] like to ask Trent, if he has any specific questions about like what the good thing about

[45:36] having an experienced dev is he can just be like read through the code.

[45:40] You know, you could even look through the code of the SDK to see what you're doing if

[45:44] you wanted to, but we only have about 10 minutes left for the timeframe that I was shooting

[45:50] for anyway. So yeah. Yeah. And this last part, you hook up an express

[45:56] server to then expose an endpoint that gives you back your, your name, and then you create

[46:02] a react front end that then reads from your express server to display it in like a little

[46:07] front end. Oh yeah. Nice. Okay. That's a nice touch.

[46:11] Yeah. And actually I'll ask you to open up a new tab and go to grovdb.org I believe.

[46:27] You mentioned this before. If you don't mind, pause this for just a second. I wanted to

[46:34] go back on here and make a note that, you know, this is a particularly apropos example

[46:42] for me because it shows, you know, I can not only you know, it's pretty easy to create

[46:49] my own schema on chain and add arbitrary data. And that's right. As Ryan, you know, we've

[46:55] talked about for MLG, our Medici land governance and then governance. Yeah. We you'll see a

[47:04] lot of land watching companies talking about tokens and we may go there at some point,

[47:12] but right now all we're doing is copying what the registrar in the government, you know,

[47:18] the County government has accepted and putting that on chain. So it's basically a copy of

[47:25] it. It's not the source of truth. We want to get there someday, but that's useful because

[47:29] that's a public record. And this particular example you've got shows how we could do exactly

[47:37] that with some data that we're going to put on soon for Baltimore.

[47:41] That's cool, man. We should get you back sometime and try and do like a proof of concept of

[47:46] that. That'd be really interesting actually. Yeah, totally.

[47:49] Yep. Yeah. And we, yeah, we don't have to continue the tutorial. We can actually just

[47:53] try to make a very bare bones version of what you would, you would want as your land governance.

[48:01] That's what we could do. We try skipping the name registration step entirely. See if we

[48:04] can just write documents. Yeah, we could try that. Yeah.

[48:08] Yeah. They're both useful in that blog. I would have been the identity stuff is, is

[48:14] interesting to me as well, just on other projects. Yep. So this is, this is the, the database

[48:20] that it's built on. And if you go to the comparison table, it shows you some of the features of,

[48:30] that you get with this database, which in theory can be used outside of a blockchain,

[48:37] outside of a blockchain context. But we use this grove DB, which dash core group built

[48:44] a special purpose for this, for dash platform. But you get like, like it shows you get the,

[48:52] the proof system and you can do secondary indexes on nested data, for example, straight

[49:00] from the blockchain and, and identify that you want certain fields indexed so that they're

[49:07] more performant and whatnot. So you don't necessarily need a lot of performance for

[49:10] your application. It seems like, cause it would be like a one-time lookup thing, but,

[49:16] but you, you have that at your, at your disposal if you want that kind of thing.

[49:23] Interesting. Okay. Thank you. So the, when you say inclusion proofs, non-inclusion proofs,

[49:32] theory proofs, I mean, what, what does that mean?

[49:40] When you're contacting a node on the network, in theory, somebody could, if they had 4,000,

[49:48] it requires 4,000 dash to run an Evo node, right? You need 4,000 cheaper and cheaper

[49:55] every day. So like, you know, master nodes, they require 1000 dash nodes, which is running

[50:03] dash platform requires 4,000 dash. And then you can be part of today. It's like a hundred

[50:09] K. Okay. Yeah. So let's say an attacker wanted to, you know, mess, mess around and he's got

[50:17] the 4,000 dash. He runs, he spins up a node cause this is a permissionless system. He

[50:22] spins up a node. Now he's one of the Evo nodes and the, the clients that are connecting to

[50:27] him want to query some data, right? Like they, they want to query Trent's Medici land governance

[50:36] contract to see what's registered. Well, in theory he could just send back bogus data

[50:43] cause we're just contacting him through HTTP S and, but there's no, you know, you know

[50:52] how computers work and you can run any service that you want on any port and you could just

[50:58] fake some data if you wanted to. But these proofs tell you that, okay, if you wanted

[51:05] to try to fake data, like you wanted to say, no, this land title actually isn't in the

[51:10] registry. You wouldn't be able to do that because not only do you need, not only does

[51:18] the data have to come from, so what I'm trying to say is you have to, you have to spoof the

[51:24] whole network though because the proof says that the network has said that this data existed,

[51:32] say like a week ago and the network say that when you uploaded that data, you got the proof

[51:38] that it was uploaded and everything. And the network came to consensus around that state.

[51:43] And then later, if you're querying that state, you could have that rogue actor that could

[51:49] send you bad data in the absence of proofs and they could get away with it. I mean, it's

[51:55] very unlikely that somebody would do that because you know, the SDK is contacting a

[52:02] random one and what are the odds and all that sort of stuff. But if you, if you don't have

[52:07] the proof, then you're just contacting somebody that's you're in, you're asking for data from

[52:14] an individual operator on a network and that's not good enough. So, so yeah, this, this,

[52:22] this database has that consensus, that network consensus built in with the proof system as

[52:28] well. So I don't know if you've heard too much about this concept of data availability,

[52:36] but that seems to be, this is a buzzword around the crypto and blockchain scene as data availability.

[52:44] So it seems like a lot of networks are moving from this, this model of all of the nodes

[52:51] are running execution and they're, they're moving away from that like Ethereum and they're

[52:56] moving toward a world where it's now more about data availability on a blockchain and

[53:03] not necessarily the, the execution or the what's the other word that I'm looking for.

[53:10] It's not, it's not compute, it's storage. And so networks are, so if you wanted to Google

[53:16] that term, like this is basically, we were trying to do that before it was cool.

[53:20] I was talking about layer one versus layer two. This is what a lot of the Ethereum layer

[53:26] two stuff is about. Yeah. But even Ethereum layer one is, is I think moving into this

[53:31] network, this data availability paradigm where the, the layer twos are contacting that layer

[53:41] one and just saying, I don't know, it's a little beyond my, beyond my understanding,

[53:48] but I do know that this idea of just having data available from the chain for other clients

[53:55] to contact and, and, and get whether that's like a solo client or an L2 client that is

[54:06] where the industry seems to be moving. And I think without looking into the term and

[54:12] exactly like the nuances of what that means, this data availability thing, I'm pretty sure

[54:18] that this is exactly what Dash platform has already been working on and is basically has

[54:26] released and will soon be on main net. But isn't it, wouldn't it be, isn't it just easier

[54:32] to say, I want some data on a blockchain and I want to be able to give it a schema and,

[54:40] and be able to query that like a database. But you haven't historically, like there,

[54:46] there's not many chains that have given you that option.

[54:49] This is, this is actually, this is one of the problems that the company I worked for

[54:53] Quicknode was meant to solve. They would have, you could buy like a regular node or a full

[54:59] or they had terms, I forget what the terms were, but you could buy a node that would

[55:03] give you like the last, you know, however many months of data, you could buy one that

[55:06] would give you all of the data and they would basically index it for you. Which is one of

[55:11] the things we were looking at with Mikhail. And it's just like, this is just a, it's just

[55:14] a hard problem to solve with blockchain is, is kind of what I, what I gathered from working

[55:19] at that company.

[55:20] Yeah, because those companies spring up because people don't want to run their own nodes and

[55:26] trust their own. They don't want to do all that work to get, to get blockchain data.

[55:33] They want to just outsource that to a company and they trust the company and that's fine

[55:36] for a lot of people. But if you can provide data with proofs and SDKs that can just talk

[55:45] straight with the blockchain instead of talking with a company that has indexed the data,

[55:52] let's just bake that right into the, to the blockchain itself and provide that as a service

[55:59] so that the nodes running the blockchain, you can contact them. And it's as easy of

[56:04] a developer experience as working with one of these indexing companies. Now we don't

[56:11] know, I think it's, we're still going to need a lot of work. It's still a lot of work to

[56:16] get to that point where the UX, the DX is just as good as working with a company that's

[56:22] specializing in this. But the idea is that's what we're trying to do is we're trying to

[56:26] give users the ability to directly connect with and contact and communicate with the

[56:34] nodes on a blockchain network from clients instead of having that middleman of corporations

[56:40] doing that, that work. So anyway I think let's wrap it up there. I think that was a good

[56:48] introduction and maybe if we do have you on next time, another time we'll try to, we'll

[56:53] try to jump in and do a little bit more playing and maybe that will be a month from now when,

[56:59] or a little bit more than a month from now when it's on mainnet. So yeah. And I think

[57:06] we have a lot of work to do with the SDK because I am getting a little tired of these issues.

[57:11] Well, it's, this has been good because we've kind of, we've narrowed in on what the main

[57:17] issues are that we can kind of tackle. So I think this is, this has been very, very

[57:22] useful. It was super great to have you on Trent. We'd definitely love to have you again.

[57:25] Good. No, it's been great to see the progress here and yeah, looking forward to mainnet.

[57:30] That's awesome. Yep. All right. Well we'll talk later. Thanks

[57:34] Trent once again and thanks for everybody for tuning in and we will see you tomorrow

[57:39] where we will be talking about the mainnet launch of Dash platform, the roadmap. Again,

[57:48] it's slated for the end of July, so we'll go through the blog post and we'll see what

[57:55] we can pick out of that and I'll probably have details. I haven't read it yet, but we'll

[58:00] see you then. Is it live or can we see it? It's live. Yeah,

[58:05] we can see it. Awesome. We'll go through that tomorrow. Awesome, man. Good stuff. Bye everyone.
