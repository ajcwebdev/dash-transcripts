---
showLink: "https://www.youtube.com/watch?v=zLg2Au2Xovo"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Proposal Web App | Incubator WEEKLY"
publishDate: "2024-07-22"
coverImage: "https://i.ytimg.com/vi/zLg2Au2Xovo/sddefault.jpg?v=669e76fd"
---

## Episode Description

Dash developers discuss enhancing proposal submission process, exploring JavaScript SDK improvements, and introducing new contributor Niles to the ecosystem.

## Episode Summary

This episode of Incubator Weekly features a discussion on improving Dash's proposal submission process and JavaScript SDK. The hosts introduce new contributor Niles, who is working on simplifying the proposal creation process. They review the recent proposal cycle results and discuss the importance of Dash's decentralized funding mechanism. The conversation then shifts to the complexity of Dash's JavaScript SDK and the need for improvement. The team explores potential solutions, including wrapping the Rust SDK or refactoring the existing JavaScript implementation. The episode concludes with a brief preview of upcoming work on DashMate, a tool for setting up local Dash nodes for development purposes.

## Chapters

00:00 - Introduction and Recent Proposal Cycle

This chapter introduces the episode's main topics and participants. The hosts discuss the recent Dash proposal cycle, reviewing which proposals passed and which didn't. They emphasize the importance of Dash's decentralized funding mechanism and how it sets Dash apart in the cryptocurrency space. The conversation touches on the challenges of submitting proposals on time and the need to make the process more accessible to a wider range of contributors.

02:56 - Introducing Niles and Current Project

Niles, a new contributor to the Dash ecosystem, is introduced. He shares his background in open-source development, compiler work, and low-level optimization. The hosts discuss the current project Niles is working on: improving the proposal submission process by creating a JavaScript library that simplifies the creation and submission of proposals to the Dash network. They explain the technical challenges involved, including serialization and hashing issues that need to be resolved to match the C++ implementation.

15:47 - Proposal Submission Process and Future Vision

This chapter delves into the current proposal submission process and the team's vision for improving it. They discuss the existing web interfaces for creating proposals and the limitations of the current system, which requires users to interact with the Dash Core wallet. The hosts outline their goal of creating a streamlined, web-based solution that would allow users to submit proposals directly from a website without needing to install additional software. They explore the potential impact of making the proposal process more accessible, including the possibility of micro-grants and increased participation from individual developers and small programming communities.

30:03 - Technical Deep Dive into Proposal Creation

Niles provides a detailed explanation of the technical challenges in recreating the proposal creation process in JavaScript. He discusses the serialization and hashing steps required to match the C++ implementation, highlighting the discrepancies they're currently facing. The team examines relevant parts of the Dash Core codebase, discussing their approach to debugging and resolving the issues. This section gives insight into the complexity of cross-implementing cryptocurrency protocols and the attention to detail required in blockchain development.

42:56 - JavaScript SDK Complexity and Future Plans

The final chapter shifts focus to the Dash JavaScript SDK and its complexity. The hosts use a dependency visualization tool to compare the Dash SDK with other popular JavaScript libraries, revealing the Dash SDK's extensive dependency tree. They discuss the challenges this presents and explore potential solutions, including wrapping the Rust SDK or refactoring the existing JavaScript implementation. The conversation concludes with a brief mention of upcoming work on DashMate, a tool for setting up local Dash nodes for development purposes, setting the stage for future improvements in the Dash development ecosystem.

## Transcript

[00:00] >> All right. We're live.

[00:03] >> Okay. Welcome everyone to a beautiful day in the Dash ecosystem.

[00:08] We have with us today, Niles.

[00:12] Hello, Niles.

[00:13] >> Hello.

[00:15] >> Anthony, how's it going, Anthony?

[00:18] >> Going good. How about you?

[00:19] >> Good. So we just had a proposal cycle that ended yesterday,

[00:27] which was eventful to some degree.

[00:31] So I wanted to start out by talking a little bit about that.

[00:34] But the topic today is one of

[00:39] our newer projects making Dash proposals more accessible in the web.

[00:47] So we'll go over that in a minute.

[00:53] So Niles, basically, we've had you on the show.

[00:56] We've had you on the channel,

[00:59] I should say, several times doing,

[01:03] two times doing the Dash platform walkthroughs.

[01:05] So you got an idea of what we're working on with Dash platform.

[01:09] Then we also had you on doing the first few live streams

[01:14] of doing this proposal work,

[01:17] which we'll talk about in the show.

[01:18] But we haven't actually had you on for Incubator Weekly.

[01:22] So we do have a little bit of a bigger audience for Incubator Weekly.

[01:26] So I wanted the folks to get to know you as a programmer,

[01:30] as a person briefly,

[01:33] and then we'll talk about the proposal stuff.

[01:36] We'll also, at the very end,

[01:39] we'll just briefly touch on some future work that I'd like you to get going on,

[01:45] and that we've talked about as well,

[01:47] which is taking a look at our Dash platform SDK

[01:52] that's currently written in JavaScript,

[01:55] and we have a Rust SDK as well,

[01:57] and there are some issues that we want to clean up there,

[02:03] and that may be a lot of work,

[02:05] it may be a little work,

[02:07] but I wanted to get you on that project as well.

[02:11] But that's not what we'll talk about today.

[02:13] I just wanted to briefly touch on it.

[02:15] So first of all,

[02:17] let's bring up my screen share,

[02:19] Anthony, if you would,

[02:21] and we'll go over the recently closed proposal cycle,

[02:28] and I just wanted to say a few things about that.

[02:31] So this is dashcentral.org/budget.

[02:36] The proposal cycle past the voting period ended yesterday,

[02:43] and this site is showing that Ash's proposal actually passed by one,

[02:50] or it's currently passing by one is what it really means,

[02:54] but it actually didn't pass in time.

[02:58] It was passing right before the end of the voting,

[03:03] and then it just dipped under passing criteria within a minute or so.

[03:10] So unfortunately, Ash's proposal didn't get funded,

[03:15] but I'm hopeful that next month MNOs will see that there's value there,

[03:21] and get that into funding territory.

[03:26] We did get our proposals in a little bit late,

[03:29] so I think that had something to do with it.

[03:32] As you can see, there's quite a bit of support,

[03:35] 406 yes votes, 56 no votes for Ash's proposal, for example.

[03:44] But I think we'll try to get them in a little earlier,

[03:48] because I think if that momentum could have kept going a little bit for longer,

[03:53] it would have been safer.

[03:55] Mikhail's obviously passed with a pretty good margin,

[04:00] and then my proposal just barely passed as well,

[04:05] and is still just barely passing.

[04:09] Jojo Bight's proposal did not pass.

[04:12] I don't know if you can see this hover when I hover over there,

[04:15] but it says proposal needs additional 25 yes votes to become funded.

[04:19] So I'm also hoping that that gets into funding territory.

[04:23] I think that it is important work that they're doing.

[04:26] But again, I think that we got our proposals in a little late.

[04:32] There is significant support here as well,

[04:35] but just wasn't enough to get us across the line on that.

[04:42] Then I'll just scroll through the rest of these just for the sake

[04:46] of looking at all of them and what happened the past cycle.

[04:52] I find that the proposal system is one of Dash's best features in the crypto space in general.

[05:01] This is what makes being able to work for this economy,

[05:09] the Dash economy or a crypto economy in general,

[05:12] being able to submit proposals and work in that primary market,

[05:17] is how I like to consider it as the primary market where Dash is created.

[05:22] That gets submitted, divvied out to masternodes,

[05:28] miners, and anybody who can add value to Dash.

[05:33] I think that's what sets Dash apart in probably the biggest way.

[05:38] That is actually related to the topic today,

[05:42] which we'll be covering,

[05:44] which is the proposal process and how we submit these proposals to the network.

[05:52] It's something that I do quite a bit.

[05:56] I have done for many years.

[05:58] But in the broad spectrum,

[06:02] very, very few people know about how to do this,

[06:07] and I'd like that to change.

[06:09] I'd like this to be a more accessible process so

[06:13] that anybody that may not even really be familiar with Dash too much,

[06:20] but they can submit proposals directly to the network.

[06:25] We fund a lot of work in the incubator from random one-off things,

[06:31] for example, like the XD5 project that Mikhail is doing.

[06:36] But why can't we have a very streamlined process

[06:42] where we could just have the XD5 guys submit their own proposal?

[06:46] I think that if we do this,

[06:50] the easier we make this process,

[06:53] the better it will be for Dash in general because there will be more competition,

[06:59] and just more people able to easily get 50-dashed for this,

[07:05] or 20-dashed for that,

[07:07] or 100-dashed for something bigger,

[07:08] or hundreds of Dash if they end up wanting to do more work for Dash.

[07:16] I'm just scrolling through here just to get this on screen for people who might have never read this.

[07:23] I think it's interesting stuff.

[07:25] I'm a big proponent of reading the documentation on sites,

[07:30] and not only reading it,

[07:33] but it first has to be written.

[07:35] Written documentation and reading documentation, very important in projects.

[07:40] It's the first touch point that a lot of people have with any project.

[07:47] If you look around the Web 2 space,

[07:50] documentation, good documentation is one of the best ways.

[07:55] Anthony, I think you'd probably agree with me here.

[07:57] It's the best way to get people interested in your project is to just have good documentation

[08:01] so that people can get from zero to one easily.

[08:05] It is that step from zero to one that is most difficult, I think.

[08:11] A lot of times, that first step is just assumed that people know that,

[08:17] but we can't assume that.

[08:19] Anyway, this is the process.

[08:22] I didn't read this.

[08:23] I have read this in other streams,

[08:25] but I'd like people to at least know about that.

[08:29] More specifically, if you do want to create a proposal,

[08:34] this is probably the most widely known way to do that,

[08:39] is you go to proposal.dash.org,

[08:42] and you go through this sequence of steps where you write your proposal name,

[08:51] your description, payment date,

[08:54] the number of payments,

[08:55] payment address, and then the payment amount.

[08:58] That's basically what the network requires as mandatory fields for submitting a proposal.

[09:04] Then, if you first go to this site,

[09:08] you would then have a button that said like next step or something like that.

[09:12] Right now, it says edit proposal or a new proposal to start over.

[09:16] But when you click that,

[09:17] then it will bring you to this screen,

[09:20] and it will then say,

[09:23] these are the wallet commands.

[09:25] Prepare proposal command, paste the following into

[09:28] your wallet console to generate the proposal at the cost of one Dash.

[09:32] You get this string to copy and paste,

[09:37] and it's not even super clear.

[09:43] If somebody had no idea about Dash,

[09:46] and maybe there's an argument to

[09:48] be made that they shouldn't be submitting proposals,

[09:49] if they don't know enough about Dash to know that this is,

[09:52] you have to actually download the Dash Core Wallet.

[09:55] Sync all the blocks,

[09:58] and I'm actually not 100 percent sure if you have to sync all the blocks,

[10:02] but you do have to download software onto your computer.

[10:06] It takes quite a bit of space and time,

[10:09] and then you have to find the console and then paste this in there,

[10:13] and you have to actually have some Dash to do that.

[10:15] It is a little bit of a cumbersome process,

[10:18] where it would be easier if we could just do this whole process within a web app.

[10:24] Creating this string is fairly trivial to do,

[10:32] but submitting that over the RPC and then generating the whole process,

[10:45] it needs to be done within the web app itself,

[10:48] even the payment itself.

[10:49] We just need a QR code that says,

[10:51] "Okay, you want to submit this proposal,

[10:53] pay the one Dash," and then that payment needs to be submitted by the web app as well.

[10:58] We have all these pieces in place except for the proposal part.

[11:04] We have the RPC library,

[11:06] we have a Dash Wallet library to use,

[11:12] but we haven't put it all together.

[11:15] Anyway, Niles, I've introduced the topic,

[11:21] but I actually went a little further than I wanted to go in the proposal topic.

[11:28] I want to back up now and let's change this back to just us three.

[11:35] You're actually working on this now.

[11:37] You've put maybe, I don't know,

[11:39] seven or eight hours into it.

[11:42] A lot of that has been just getting an idea of the Dash landscape,

[11:48] what Dash is all about,

[11:51] the different software packages and all that.

[11:54] What's your experience been so far doing that?

[11:57] Can you give us an introduction to you?

[12:00] Who are you? What programming do you do?

[12:04] >> Sure. My experience of coming into Dash,

[12:09] there were a couple of bumps with just finding how to get

[12:13] started that I think maybe we could put on the homepage of Dash D.

[12:18] But once I actually got set up with this is how you get started,

[12:24] I was able to compile it,

[12:26] I was able to get going,

[12:29] and yeah, I was working with AJ a little bit on that problem that you were just

[12:36] showing and getting a feel for what's going on in

[12:39] the code base or what's the process of these things.

[12:45] Who I am as a programmer,

[12:49] I've been doing open-source stuff for a long time just on my own.

[12:56] A long time ago, I was really working on some compilers and transpilers.

[13:05] I worked on a TypeScript to Lua transpiler,

[13:08] so I have a lot of TypeScript experience in some respect from that.

[13:16] That was a Node project.

[13:18] Then I've also done a lot of independent computer science-y stuff.

[13:25] I showed last in one of our other streams that I made

[13:30] a data structure to do prefix autocomplete over a scored dataset,

[13:38] that actually improved the previous state-of-the-art data structure

[13:41] and algorithm for how you can do such a thing.

[13:46] Actually, I learned about Dash and I met some of

[13:50] the people that have been involved with it from these meetups,

[13:54] and Ryan saw me give a talk at a Zig meetup.

[13:59] That we've been going to locally here in Utah,

[14:02] because Ryan and I don't live too far from each other,

[14:07] and also Jojo and AJ are in the vicinity.

[14:12] Yeah, so for that project,

[14:18] I've really been getting interested in CPU architectures,

[14:24] and learning all the different instructions,

[14:26] and coming up with optimized routines for

[14:30] accomplishing specific tasks that can be used to accelerate.

[14:34] The project I've been working on for a little bit now is

[14:38] like the tokenizer and parser front-end to a compiler,

[14:42] and trying to push on the best we can do for that category.

[14:49] Yeah, I actually have another talk planned for

[14:52] October coming up for that,

[14:54] and so that'll be really fun.

[14:56] If you want, I could just show an animation that I have for it.

[14:59] But otherwise, I think, yeah,

[15:03] if anyone wants to look up SIMD and vector stuff,

[15:07] I've been doing a lot of that.

[15:09] A lot of it has been inspired by the work of Daniel Meyer,

[15:14] the stuff that he's done with SIMD JSON.

[15:17] I know a number of languages as a result that I've picked up

[15:25] across time, JavaScript, TypeScript, Lua,

[15:28] Zig, and I also did some C++ in college.

[15:33] Not terribly much, so I do get confused

[15:36] by some of the more esoteric syntax sometimes,

[15:40] but I'm learning it, and yeah,

[15:44] I'm working on that stuff for Dash.

[15:47] >> Yeah, I think that's actually when we first met,

[15:50] AJ talked with us,

[15:53] we were at lunch and he was introducing me to you,

[15:57] and you described some of the stuff that you were working on,

[16:00] and then I saw your meetup,

[16:02] and I thought, this guy's too low level for what we need.

[16:06] Maybe if we need some micro-optimizations at

[16:10] some point in platform or something in Dash,

[16:15] we could tap you.

[16:17] But then the more I thought about it,

[16:19] the more I thought, one of our biggest problems right now

[16:22] or challenges in Dash, as I see it,

[16:26] is we need a good JavaScript SDK for

[16:31] platform that also works well with our libraries,

[16:35] and just in Dash in general,

[16:39] there's a lot that you have to know to be able to

[16:43] even get started and useful.

[16:46] You have to be able to look into

[16:48] the C++ code base for our main implementation.

[16:52] You need to, if you want to work on platform,

[16:54] you really need to know Rust,

[16:57] which is what most of platform is written in,

[17:00] and Go, which is where

[17:03] the Tendermint consensus algorithm is part of platform.

[17:07] Then there's SDKs.

[17:10] If we need you to work on

[17:12] the JavaScript SDK to make it perform better, for example,

[17:16] you might have to look into the Rust SDK,

[17:18] or you might have to look into

[17:20] the Java implementation of some library that we're working on.

[17:27] We have a lot of languages,

[17:29] and this is actually what I was thinking

[17:30] about when you were coming on,

[17:32] is we need somebody like you that just can be able to pick up,

[17:35] and read, and interpret

[17:38] lots of different code bases in lots of different languages.

[17:41] It's a very good fit, I think.

[17:45] >> Let's see, where were we?

[17:47] Anything else that you wanted to say about your background,

[17:50] or should we jump into the topic a little bit more?

[17:55] >> I'm ready to jump into the topic.

[17:59] But yeah, if you do want a little teaser of something from my next talk,

[18:04] I have a cool animation or a routine I did.

[18:07] But I think people probably get the feeling anyway,

[18:09] so we can just move on.

[18:11] >> Sure. Let's see.

[18:15] Just moving on with,

[18:16] Anthony, can you do my screen share again?

[18:19] Moving on with where we were.

[18:23] Here's another site that does the same thing, which is good.

[18:30] But as you can see,

[18:31] it does the same thing where it's giving you

[18:33] this string to paste into the other wallet.

[18:38] Ideally, where this is going is,

[18:43] this is the source code for the proposal generator.

[18:48] Once we've written all the internals

[18:54] to be able to make these commands and submit them,

[18:58] we will probably want to submit a pull request to this code base.

[19:05] I'm not sure if that will be

[19:08] something that Dash Core Group wants to put in here.

[19:12] Before we do that, we'll probably talk with them.

[19:15] But I want to get it into at least one JavaScript code base.

[19:22] Here's the one option is to just enhance this site right here with

[19:28] the ability for somebody to do

[19:31] the submission and payment right within this web app.

[19:36] We would be making a pull request to this code base.

[19:42] But in addition to that,

[19:45] we would then integrate it into the incubators web wallet,

[19:51] which at the time is a wallet and that's primarily what it is.

[19:57] But the idea is that we'll be moving this,

[20:02] transitioning this more from just a web wallet to all things Dash.

[20:07] This is where I was talking about our proposals and whatnot.

[20:12] This is where Jojobite would be doing some of this,

[20:17] or at least I'd be working with him.

[20:19] Unfortunately, we weren't able to get that funding to do a lot of work on it.

[20:25] But I think he's motivated to keep working on this regardless,

[20:30] even though this past proposal didn't pass,

[20:34] I think he's just going to keep going gung-ho.

[20:37] I just wanted to get into the actual UI here,

[20:42] so I'll just do a dummy here.

[20:44] This is showing the web wallet.

[20:47] I'll just fake like I backed that up and put in a dummy password.

[20:54] But as you can see,

[20:57] this is our web wallet interface.

[21:01] It's just a simple send and receive for now.

[21:05] It does have contact support.

[21:08] I think once platform is stable on testnet and/or mainnet,

[21:15] we'll be integrating contacts,

[21:18] Dash Pay contacts with this as well.

[21:21] But as you can see this coming soon section,

[21:24] CrowdNode, Maya, Protocol,

[21:27] Dash Spend would be another one that would be on here and then Dash Proposals.

[21:32] It's intended to be a lot more than just a wallet.

[21:38] It's intended to be a place where you can make the most leverage out of using Dash.

[21:44] Whether you want to stake your Dash in

[21:46] CrowdNode or you want to transfer your Dash to Bitcoin or something,

[21:53] or Bitcoin to Dash using Maya,

[21:56] or you just want to use the Dash that's in your wallet and stake it through,

[22:02] or not stake it, but put it in Maya Savers, for example.

[22:05] If you want to spend your Dash,

[22:07] this is a big part of this wallet as well as when Ash can get the Dash Spend,

[22:16] API completely finished,

[22:20] then we'll integrate that into here as well.

[22:23] These are all things where what somebody wants to be able to

[22:29] know before they even start working for Dash is how they can actually use Dash,

[22:33] and so that's what this will be.

[22:35] Then that proposal would also be something that we would add there.

[22:41] Anyway, getting back into the subject a little bit.

[22:47] This is the little script that AJ wrote to help guide you.

[22:55] Niles, you're new to Dash,

[22:57] new to the project.

[22:58] You just had your first stream on your own.

[23:02] We had Michael Cluster, XKCD,

[23:04] helping us out with some of this serialization issue,

[23:12] so the main thing that we're running into.

[23:14] I'll let you describe it actually.

[23:16] You can just tell me to scroll up or down,

[23:21] but can you give us an idea of what the problem is that you're trying to

[23:24] solve and how you're going about it?

[23:28] Feel free to tell me to scroll or whatever.

[23:32] >> Yeah. Can we go down to the bottom first and look at the main function,

[23:36] and then we'll come back up.

[23:39] >> Okay. So the main function.

[23:43] >> Yeah. So let's go to the definition of main.

[23:46] So I'll scroll up. All right.

[23:52] So right here,

[23:54] you can see we're declaring this G object,

[24:00] and it has a couple of these properties in it.

[24:04] The main thing that we're trying to solve is we need to reproduce the way that

[24:14] Dash D does the encryption of

[24:18] this object before submitting it to the blockchain as a proposal.

[24:24] >> I'm sorry. Do you mean serialization or can you describe what the difference is?

[24:31] >> Yeah. So what I mean is we're serializing it,

[24:35] and we are doing SHA-256 on it,

[24:38] actually double SHA-256.

[24:41] >> So you get this data from the user from, say, some interface.

[24:49] They're giving you that data that I showed here.

[24:54] >> Right. So yeah,

[24:57] inside the wallet commands or yeah, right here in the dashboard.

[25:01] >> Then you're taking that data and then you're using some of that data,

[25:05] serializing it, and then patching it.

[25:09] >> Yeah. So some of the data is obscured a little bit here.

[25:13] So you can see we have a hex JSON field,

[25:15] and so that's going to encode more of the information that you saw on

[25:19] that website where you type in how much Dash you want, when it should go.

[25:26] Then you can see some of the fields are

[25:28] not inside of that hex JSON but are outside of it.

[25:33] So yeah, basically, what we're trying to do is reproduce

[25:36] the semantics that we got from the C++ implementation.

[25:41] But there have been a couple of hiccups involved with that

[25:47] where there seems to be some piece of it that we're missing.

[25:54] Currently, even with my slightly updated version

[25:58] of this script that is being shown on the screen right now,

[26:01] we are getting a different answer at the end after doing

[26:06] a double SHA-256 than we're supposed to get.

[26:10] Yeah. If you want, we can go look at the implementation of those at the top now.

[26:16] >> Do you want to share your screen if you wanted to?

[26:21] I can go where you want it,

[26:23] but feel free to share your screen as well if you

[26:25] wanted to look at the C++ code base or anything like that.

[26:29] >> There's a question for you in the comments, Ryan.

[26:32] >> Okay. With Alex preoccupied with Cardano integration with Maya,

[26:40] would there be time to work on DPE?

[26:43] I think that's Dash Platform Explorer.

[26:45] That was my main concern on that proposal.

[26:48] Anyway, back to Niles just responding to Ryan's intro.

[26:52] Alex, I think this is Ash's Alex.

[26:56] Ash has a programmer named Alex,

[26:59] and he's doing Cardano integration with Maya.

[27:03] So as far as I know,

[27:06] there's no plans for him to just quit working on Dash Platform Explorer.

[27:12] Oh, Dash Pay Extension.

[27:14] Yeah, that's what I meant actually.

[27:16] I just, for some reason, I said the wrong thing.

[27:18] But Dash Pay Extension is what DPE was,

[27:22] and that's what I was referring to.

[27:25] I don't think that he's going to stop working on that.

[27:28] But you're concerned that Alex doesn't have time to work on that.

[27:34] That's something that we can look at.

[27:36] It goes along with the SDK stuff that I was talking about in the intro as well.

[27:44] There's only so much we can do at one time,

[27:48] but this particular proposal stuff isn't necessarily my,

[27:53] it's not the most important thing that we need to be doing right now,

[27:56] the Dash SDK stuff is,

[27:59] and potentially Dash Pay Extension.

[28:02] This was just a project that I felt like was a good introduction for Niles

[28:06] to get a lay of the land with a somewhat scoped and simpler project.

[28:16] Yeah, we can move Niles to wherever we want to in

[28:22] the future as long as you're okay with that, Niles.

[28:26] But right now, I think the focus is going to

[28:31] be getting this wrapped up as soon as we can,

[28:34] and then looking at the JavaScript SDK stuff.

[28:38] >> Sure. I think we should be able to finish this today or tomorrow.

[28:44] When I say we, I mean me primarily.

[28:47] But yeah, so the training rules were off for

[28:52] the first time on that last stream that we did.

[28:56] >> Because we did two streams before that with AJ,

[28:59] and he was helping you, guiding you,

[29:01] giving you [inaudible]

[29:06] >> It was more like I was aiding him and he was just going through.

[29:13] There were a couple of times where I lost what he was trying to accomplish,

[29:17] but I was just trying to assist him in that.

[29:19] But yeah, definitely this last time I was like,

[29:22] all right, now I'm in the driver's seat,

[29:25] and now I have a plan for exactly how I will address this.

[29:31] I'm thinking today or tomorrow,

[29:34] we should be able to put this in the rear view mirror.

[29:38] Yeah, there is still going to be submitting the PR,

[29:44] maybe a little bit of web interface stuff that will have to be added.

[29:49] But I don't think that should be too big of a hurdle.

[29:51] Honestly, that should be pretty good as well.

[29:54] Yeah, if you want to look at serialized for collateral TX real quick,

[29:58] and then I can just show the C++ code in question,

[30:00] if people are interested in that, scroll on to the top.

[30:03] >> Okay.

[30:05] >> Here's our serialized for collateral transaction function.

[30:14] It starts off by computing data len.

[30:18] What that is, is we're allocating a UN8 array on line 77.

[30:24] How those arrays work is you have to allocate all the memory for them upfront,

[30:29] unless you want to make another one and resize it that way.

[30:32] But yeah, so we just say,

[30:35] okay, this is how many bytes we're going to need.

[30:38] Then we make a data view into it as well on line 78.

[30:43] Then if you scroll through, basically all we're

[30:46] doing is we're just taking each individual data element,

[30:49] and we're putting it into the buffer as a series of bytes.

[30:55] You can see on line 84,

[30:59] we say, okay, take the 32-byte hash parent and drop it into the first 32 bytes.

[31:07] You can see on line 85,

[31:08] we add 32 to the offset.

[31:11] That means we're going to use offset throughout this function,

[31:15] and that's going to be like our pointer into the buffer or index.

[31:19] That's where we're writing.

[31:21] So you can see on line 87,

[31:22] we're going to write a 32-bit integer.

[31:24] That's four bytes, and it's the revision,

[31:28] and yeah, we add an offset of four.

[31:30] So you can see the pattern there.

[31:32] This is just writing it into a buffer.

[31:35] Then after this, we return that buffer,

[31:41] and then we do a double-shot 256 on it back in the main function.

[31:46] Yeah, there's a discrepancy.

[31:50] There's some piece of this that is

[31:54] different in functionality between our current JavaScript implementation.

[32:00] I made a few really small changes to this file,

[32:04] but this one's mostly the same.

[32:08] Yeah, so we're getting a different answer than we're expecting.

[32:13] So we basically are just hunting down in the C++ code.

[32:17] There's some piece of it that we're not taking into consideration.

[32:20] So my plan, I guess I can just say it.

[32:24] What I'm going to do is I'm going to make a build of dash D that

[32:29] cuts out the blockchain syncing and also will not commit a proposal.

[32:34] All it is, is just going to strip out the particular code that

[32:39] is putting the data in a buffer and doing the double-shot 256.

[32:45] >> That's dev, I want to do dot com.

[32:50] >> Then yeah, I'm going to step through it.

[32:58] I think I was looking at the code.

[33:02] When we left off last time on that last stream,

[33:05] I was suspecting that there's probably some oddity with padding,

[33:11] with the last chunk of 64 bytes that's not being reproduced faithfully.

[33:16] So I'm also going to take a look at the JavaScript Cryptolibrary,

[33:21] what specifically it's doing with the edge cases on that.

[33:30] I'm planning today on setting up my VS Code debugger,

[33:36] so it's a lot easier for me than using GDB,

[33:39] which is what AJ was trying to do before.

[33:42] Then you also have more features like you can

[33:46] see all the variables while going through line-by-line,

[33:50] which with GDB you can do it,

[33:52] but it's just more steps.

[33:54] >> Do you know where in the C++ code base that I'm looking at right now,

[34:00] where this work was?

[34:03] >> Governance object, object.cpp was one of them.

[34:11] This holds the c_governance object.

[34:16] That's the object that we're serializing.

[34:20] I could find you a specific line number if you want.

[34:28] >> Yeah, I just wanted to come here just in

[34:31] case it was easier for you as you're describing it.

[34:33] I can do a find on page as well.

[34:36] >> Sure. Let me just open up my VS Code.

[34:42] Yeah, so we started out in governance.cpp.

[34:46] We were looking at line 127,

[34:52] about, so there's the geogic prepare,

[34:56] maybe it's 126, and yeah,

[35:00] there's a governance object that's using the function and we call getHash.

[35:07] We believe that it returns the same hash every time,

[35:10] but that's another thing.

[35:12] >> [inaudible] prepare on this page.

[35:14] We might not be looking at this.

[35:16] >> I'm sorry, you're on object.cpp still.

[35:18] >> Yeah.

[35:19] >> My bad. If you could go to governance.cpp.

[35:26] >> Okay.

[35:27] >> Sorry, I was thinking of the folder and then the file.

[35:31] Yeah, if you try go to line 150.

[35:39] >> Okay.

[35:39] >> About there, scroll down.

[35:44] So scroll up.

[35:51] My file is probably a little different from stuff being added.

[35:58] Yeah, go to, the function is a geobject_prepare.

[36:07] >> Oh, it's in RPC, the folder.

[36:17] SRC/RPC/governance.cpp, my bad on that one.

[36:24] >> RPC, okay, yeah, RPC in it.

[36:27] There are different governance that's got it.

[36:29] >> Yeah.

[36:31] >> Then I'm going to prepare.

[36:34] Okay, this is looking more familiar, okay.

[36:38] >> Yeah. If you scroll down,

[36:42] you can see that geobject_prepare function is where the magic happens.

[36:47] You can see that it gets the JSON for the request,

[36:51] which you saw the JSON encoded as hex in the JavaScript file already.

[36:56] That's not a hard problem.

[36:59] Then you can see that we're parsing in the command line arguments.

[37:03] So you can see parse_hash_b for the parent hash if one exists,

[37:07] although it typically doesn't like it says in the comment there.

[37:11] Then we parse_revision as a 32-bit integer,

[37:16] and time as a 64-bit integer from the params array,

[37:21] which is like command line arguments.

[37:24] Maybe it gets passed in some other way in some other context,

[37:27] but that's how I've been interacting with it.

[37:30] Then you have str_data_hex,

[37:34] which is also the data that you see on the website,

[37:40] where it gives you the command,

[37:42] and it already gives it to you partially serialized in that way.

[37:46] Then yeah, in this function,

[37:50] we're calling gov_object.get_hash.

[37:56] That's the part that we haven't fully been able to reproduce yet.

[38:05] >> Which line?

[38:07] >> So the first appearance is on line 184,

[38:10] but it's called multiple times in this function.

[38:13] AJ thinks that it returns a different results run-to-run,

[38:19] and I'm not sure if that's the case.

[38:23] He actually spent more time with the logs and looking at those,

[38:28] so he might be right about that.

[38:31] I'm going to be doing that today and tomorrow as well.

[38:37] So we're going to look at that and see what the issue is.

[38:41] >> Awesome. Let's see.

[38:45] Let's go back here. So you're going to

[38:49] be looking at that today and tomorrow.

[38:52] >> That would be great. Then we'll see where we go with it.

[38:57] So I'd like to make it a JavaScript library,

[39:02] so that it can be imported very easily into lots of different sites.

[39:07] One of my strategies with this is that I get some people,

[39:12] I've actually got some people already that are interested in

[39:15] Dash and interested in doing some work for Dash.

[39:20] We can do that.

[39:23] So actually, I'm thinking about hackathons.

[39:27] So let's say you have a community of programmers that want to do

[39:32] a hackathon and Dash wants to sponsor that,

[39:35] or they want Dash to sponsor it.

[39:39] We will see how well this lands when I pitch this,

[39:45] but I want to be able to give them a site where I say,

[39:50] just fill out these fields and submit a one-paragraph proposal,

[39:57] and ask for the Dash directly from the Dash network.

[40:01] Because what that does is it illustrates

[40:06] the power of this decentralized funding mechanism.

[40:11] It's in itself an interesting marketing tool to developers,

[40:16] developer marketing tool where you can say, "Here's this website.

[40:21] Fill out this form with those five little pieces of data."

[40:27] Then what we need is in addition to that,

[40:30] in addition to those five fields that we're trying to do,

[40:35] we also want to be able to have them submit the body of their proposal.

[40:40] We don't want to have them have to sign up

[40:44] for Dash Central or sign up for any website.

[40:47] We just want them to be able to fill out a form that says,

[40:51] "Here's the three paragraphs of my proposal body as well,"

[40:55] and then submit that to say a Dash platform contract.

[41:00] No signing up here,

[41:02] no signing up to anything,

[41:03] just submitting data to either the Dash blockchain,

[41:07] or not the blockchain,

[41:10] but the proposal data through the RPC,

[41:13] and then the actual body of the proposal goes to a Dash platform contract.

[41:22] If you make this streamlined enough,

[41:28] you might see a bunch of people submitting even 10 or 20 Dash proposals,

[41:34] just bam, bam, bam.

[41:36] I think that's a lot more exciting than two organizations working for Dash.

[41:41] I'd love to see a future where individual developers or small programming communities,

[41:50] like the one I always think of is the SolidJS community,

[41:54] which I have an affinity towards.

[41:57] But Anthony will tell you there's a lot of little tribal JavaScript communities.

[42:04] Right now, not the political,

[42:07] but the economic landscape that we're in,

[42:09] I think a lot of people are looking for funding.

[42:12] They typically would have to go to VCs to get funding.

[42:15] But if we can give them some micro-funding,

[42:19] micro-grants, or even micro-loans in the future,

[42:24] I think that's very interesting.

[42:26] I think that's a very interesting future to pursue.

[42:28] But it all starts with the ability to make

[42:32] proposals very simple and easy in a one-stop shop to do that.

[42:37] But they could then embed some script in

[42:41] their web apps that give them the ability to have their users submit proposals.

[42:50] Anyway, there's lots of different possibilities,

[42:52] but it all starts with having good JavaScript tooling and libraries.

[42:56] >> For sure.

[42:57] >> That's what I'm going for here.

[43:00] I think that we can probably wrap it up for the most part with that.

[43:05] I did want to show one other thing actually before we got,

[43:09] before we left. If I can remember the site,

[43:15] I think I bookmarked it.

[43:19] Let me just try to find this real quick.

[43:23] Anthony, you may know this as well.

[43:33] I saw in some video there was an NPM,

[43:42] like you give it an NPM library and it shows you the graph of all the dependencies and things.

[43:50] Do you know what I'm talking about?

[43:52] >> Yeah, I'm pretty sure.

[43:58] There's probably a couple of different ones, but.

[44:02] >> Programming, I think I've been around programming JavaScript.

[44:08] >> Npm-graph.js.org.

[44:11] >> Npm-graph.js.org, that's right.

[44:13] You found it slightly before I found my bookmark.

[44:16] I mentioned that I wanted to briefly touch on the JavaScript SDK,

[44:29] which we'll have as a separate topic later,

[44:35] but am I still sharing my screen?

[44:38] >> Yeah.

[44:39] >> Okay. I'm going to show us real briefly.

[44:43] >> Pop up your font.

[44:45] >> Okay. Actually, I want to show something more simple first.

[44:54] I'm just going to show React.

[44:57] When you go to a code base,

[45:01] when you get a library,

[45:05] you can pop that JavaScript library into something like this,

[45:11] and it shows the dependencies of the library.

[45:15] If you want to import React,

[45:17] which is the most popular JavaScript front-end framework into your project,

[45:22] it's going to bring in this.

[45:24] It's also going to bring in the React dependencies,

[45:26] which surprisingly, for maybe some people,

[45:29] is only two dependencies.

[45:32] Yeah, because it gets a bad rap being very bloated,

[45:38] and it is a little bigger compared to other front-end frameworks.

[45:46] >> Well, React doesn't do anything without React DOM,

[45:49] so that's also deceptive.

[45:51] >> You wanted to say React DOM.

[45:52] >> Yeah, fair.

[45:53] >> It's going to be a little bit bigger,

[45:55] but it's surprisingly also pretty lean in terms of number of dependencies.

[46:01] >> That's just the schedulers,

[46:03] the only thing different, right?

[46:04] Those other two are the same.

[46:07] >> Yeah. I'm now going to put in Express,

[46:12] which is a back-end framework for JavaScript.

[46:15] There's going to be more stuff going on here.

[46:17] I'll zoom out a bit.

[46:20] You can see it can get pretty complicated,

[46:28] but now I want to show what our -sdk looks like.

[46:34] It's thinking.

[46:39] >> Wow, 320.

[46:45] Wow.

[46:47] >> 322 dependencies.

[46:50] There are 20 modules that have different versions of the same library,

[47:02] and I'm going to zoom out so you can really get a scope of this.

[47:08] >> But it says TypeScript is a dependency, is that right?

[47:15] >> Yes.

[47:17] >> Or that's a dev dependency, right?

[47:19] >> It's probably a dev dependency,

[47:21] but I don't think it actually is.

[47:23] I think that it's actually a dependency at some point.

[47:26] >> You actually need the TypeScript compiler to ship out?

[47:30] >> This is something that you'd be able to answer better than I would,

[47:33] but I'm pretty sure that it's actually

[47:36] a runtime dependency for whatever reason.

[47:38] Maybe it shouldn't be because you can actually go in here

[47:43] and toggle on include dev dependencies,

[47:47] and that will make it even bigger.

[47:49] But that's not something that's really relevant.

[47:52] But the fact that it's included without me having toggled that.

[47:59] So there's a lot going on here.

[48:03] >> I also will say for myself,

[48:07] when I first ever did an NPM package and I wasn't experienced with it,

[48:11] not really realizing the difference between dev dependency and not.

[48:16] Sometimes you install TypeScript,

[48:19] and then it will just get put in

[48:20] your normal dependencies when it should be in the dev dependencies.

[48:24] So I don't know, we can look at it.

[48:26] Maybe it is genuinely needed,

[48:28] but that does seem weird to me.

[48:30] >> So here's a look at Dash Core Lib,

[48:33] which is much better, right?

[48:37] So this is one of the main libraries that we use in Dash, and that's good.

[48:47] There's also Dash Wallet,

[48:52] which is the tooling that we're creating in the incubator.

[48:58] Which depends on Dash HD,

[49:00] this is stuff that AJ wrote,

[49:02] Dash Phrase, Dash Site,

[49:03] Dash TX, and so forth.

[49:06] So the idea with the JavaScript SDK thing is,

[49:12] we need to figure out what we should do here.

[49:15] This is obviously something that the Dash Core group is probably also thinking about,

[49:19] like how are we going to make our JavaScript SDK?

[49:26] Are we going to try to fix this and make it better,

[49:34] which is complicated, or are we going to just wrap the Rust SDK?

[49:41] So those are the questions.

[49:45] That's the project that I want to focus on next with you, Niles.

[49:51] So I just want to give a little bit of a flavor for this right here now,

[49:56] because I thought this would be a little bit of a shorter show,

[49:58] and we could do a little bit of a preview of

[50:01] the next show that we have you on with after you've had some time to work on it.

[50:08] But I think that wraps up the show.

[50:12] You're going to be working on this in the next couple of days.

[50:14] I know you're working full-time elsewhere as well on the rest of the week,

[50:19] but you have Mondays and Tuesdays off.

[50:21] So this is the time that we can get you on this.

[50:25] So let's look forward to getting that done,

[50:29] and then we'll move on to the next project.

[50:30] So anything else to say,

[50:33] Anthony, that you wanted to close out with, or are we good to go?

[50:37] >> Sometime probably tomorrow, if you're free,

[50:40] we can do a stream about DashMate.

[50:43] I've got a new tutorial that shows how to use that.

[50:48] Yeah, I think it's a lot smoother dev experience.

[50:52] >> Yeah, because that's setting up

[50:55] three little local nodes on your own local network rather than contacting testnet.

[51:01] >> Yes, exactly.

[51:03] >> Okay, cool. All right.

[51:05] Well, we'll see everybody next time then,

[51:06] and tune in this week later as well for other streams as well.

[51:10] So bye, everyone.