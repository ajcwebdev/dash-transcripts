---
showLink: "https://www.youtube.com/watch?v=dNIU0g7-28o"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Platform Walkthroughs Part 1a with Monarch Wadia"
publishDate: "2024-06-04"
coverImage: "https://i.ytimg.com/vi/dNIU0g7-28o/sddefault.jpg?v=665dff5d"
---

## Episode Description

Monarch Wadia, a full stack web developer, explores the Dash Platform for the first time through a hands-on tutorial.

## Episode Summary

In this episode, Monarch Wadia, an experienced full stack web developer, goes through a hands-on tutorial introduction to the Dash Platform. Along the way, he provides feedback on the tutorial, encounters some technical challenges with the Dash testnet, and discusses the potential of the platform with Anthony and Rion. Despite some glitches, Monarch finds the learning experience valuable and eye-opening. The episode highlights opportunities to improve the onboarding process for developers new to the Dash Platform.

## Chapters

00:00 - Introduction and Guest Background

The episode begins with an introduction of the guest, Monarch Wadia, a full stack web developer with 12 years of experience primarily in React, TypeScript, and Java. Monarch shares his background, including running his own software development firms and a hackathon platform called Mintbean. Anthony and Rion provide an overview of the episode's focus on a hands-on Dash Platform tutorial.

02:56 - Tutorial Walkthrough Begins 

Monarch starts working through the tutorial, beginning with setting up the project and installing the necessary Dash Platform dependencies. Anthony and Rion guide him through each step, clarifying the instructions and answering questions along the way. Monarch provides feedback on the clarity and structure of the tutorial as he progresses.

18:53 - Mnemonic Phrases and Key Pairs Explained

Rion provides an in-depth explanation of mnemonic phrases and hierarchical deterministic key generation used in cryptocurrency wallets. He discusses how these 12-word phrases are used to derive public and private key pairs for various purposes, including password management and cryptocurrency addresses across different blockchains.

37:39 - Faucet Issues and Workarounds

Monarch encounters issues with the Dash testnet faucet while trying to fund his wallet for the tutorial. Anthony and Rion troubleshoot the problem, discussing potential solutions and workarounds. They explore using different testnet explorers and sending testnet funds directly to Monarch's wallet to bypass the faucet issue.

58:39 - SDK Version Troubleshooting

The group investigates errors Monarch encounters during the tutorial, suspecting that the version of the Dash SDK being used might be the culprit. They attempt to resolve the issue by installing different versions of the SDK and re-running the problematic commands, eventually finding a version that works.

74:54 - Dash Platform Overview and Wrap-up

As the episode nears its end, Rion provides a high-level overview of the Dash Platform, explaining how it allows developers to store application data on a decentralized network without needing to set up servers or databases. Monarch shares his thoughts on the tutorial experience, praising its hands-on and informative nature while noting the frustration caused by testnet glitches. Anthony and Rion discuss potential improvements and next steps, wrapping up the episode with plans for future collaboration.

[00:00] All right, welcome to the first episode of our new series, Dash Platform Walkthroughs.

[00:07] Oh yeah, Monarch Wadia is our first guest.

[00:11] What's up, Monarch?

[00:12] You want to give a little intro, who you are, what you do?

[00:15] Hey, Anthony.

[00:16] Thanks for having me here.

[00:18] I am a software dev, I've been working in full stack web for 12-ish years or so.

[00:24] I've never touched crypto, so this is the first time that I'm actually touching crypto

[00:28] as a developer, which is exciting.

[00:31] Most of my work is React, TypeScript, I've done a bunch of Java, that sort of thing.

[00:37] Sweet.

[00:38] And then, Rion, do you want to talk about this new series we're launching?

[00:42] Yeah, we've talked about it a little bit before already, so we don't have to say much about

[00:46] the series.

[00:48] I mostly just wanted to get to know Monarch a little bit more in detail before we jump

[00:54] right into what we're doing.

[00:56] Of what we are doing, what we will be doing eventually, I would say maybe in about five

[01:00] minutes or so, as we'll jump into a tutorial where Monarch's going to lead the way.

[01:08] He's going to basically perform the live QA, the action that a developer might do offscreen.

[01:22] We want to get it on screen so that we can see how the experience goes with developers

[01:29] using our Dash platform product and tutorial.

[01:33] But yeah, before we jump into that, Monarch, I don't know you at all.

[01:37] The only way I know you is through Anthony and getting this live stream going, but I'd

[01:43] like to know a little bit more about just your technical background.

[01:47] You said you have 12 years of experience, and what specifically are you usually working

[01:52] on?

[01:54] Yeah, I started off with a lot of front-end stuff back before React was really a thing.

[02:04] And when React became popular, my boss at the job I was working at the time said, "Hey,

[02:11] we don't really trust this new thing called..."

[02:14] I think it wasn't even Redux, it was a thing that came before Redux back then, "We don't

[02:19] really trust it.

[02:20] Why don't you just implement your own state management from scratch?"

[02:23] So I got into React, and I built my own Flux architecture from scratch.

[02:27] That was kind of fun.

[02:29] So after that, I sort of moved more towards the back end, did a bunch of Ruby on Rails,

[02:35] was an architect at Ericsson for a while, leading all the front-end projects.

[02:41] And then I forked off and started my own business, did my own business for the last six or seven

[02:44] years.

[02:45] I ran two software development firms, I ran my own startup called Mintbean.

[02:50] And that's...

[02:51] Sorry, what was the startup called again?

[02:53] It was called Mintbean.

[02:54] So it was a hackathon platform, at the peak of it, we'd get about 800 developers registering

[03:01] for our hackathons a week, which was...

[03:04] And this is how me and Monarch knew each other, is Redwood did a hackathon, and then that's

[03:09] how we met.

[03:10] And then eventually, my first company, Stepset, did a hackathon also with Mintbean.

[03:14] It was awesome.

[03:15] It was such a cool experience, and so we've kind of been buddies ever since.

[03:19] Yeah, yeah.

[03:20] Good times.

[03:21] It was a lot of fun.

[03:23] So we built the whole platform in GraphQL, and TypeScript, and Node, and deployed it

[03:30] on AWS.

[03:31] Had the community working on the platform, hired from the community as well.

[03:35] Had about 10,000 people overall in the community at peak, all of them software engineers, most

[03:43] of them from bootcamps, that sort of thing.

[03:45] So that was a lot of fun, made me realize that I'm really technical, and I don't necessarily

[03:51] want to do the CEO job forever, and ever, and ever.

[03:54] So yeah, that's why I'm doing more geeky stuff these days.

[03:58] Anthony and I have been collabing on some LLM stuff, which has been really awesome and

[04:04] fun.

[04:05] But yeah, that's sort of what I'm up to these days, is large-

[04:07] Yeah, you've got an open source library, Ragged.

[04:10] Oh, yes.

[04:11] I just did a whole overhaul over the weekend, so I just deleted everything, I just started

[04:15] from scratch.

[04:16] It's so much better now.

[04:17] Yeah.

[04:18] Yeah, yeah.

[04:19] Wow, that's quite the list of accomplishments.

[04:23] So you're both on the technical side, you ventured into the entrepreneurial side, you

[04:29] don't like the management as much as the technical, but it looks like...

[04:34] Are you still doing anything with that hackathon software, or has that just been retired, or...

[04:39] Oh, that retired a couple of years ago, but thanks for asking, it was a lot of fun.

[04:46] Never going to do that again, it was a lot of fun, but the energy over there...

[04:50] Yeah, it was crazy to manage, I can only imagine.

[04:54] Yeah, yeah.

[04:55] All right, well, I guess maybe now's a good time to jump into the tutorial then, and kind

[05:00] of see, I have a better frame of mind of who I'm talking to, and what kind of experience

[05:06] you have.

[05:07] So this'll be good.

[05:08] Sweet.

[05:09] All right.

[05:10] Yeah.

[05:11] So if you scroll down just a little bit, we don't need to read the whole intro, 'cause

[05:16] we'll be kind of talking you through everything.

[05:17] So you're gonna want to just run each of those commands, unless you already have a directory

[05:22] set up.

[05:23] No, I have nothing set up right now, so...

[05:25] Excellent, perfect.

[05:26] So just run through them.

[05:29] So this is doing, this will set up your projects, initialize your package.json, and install

[05:36] the one and only dash platform dependency.

[05:41] So I'm gonna be working inside VS Code for most of it, or it's not all of it?

[05:46] Yeah, pretty much all of it, yeah.

[05:47] There's some times where you'll have to reach out to a browser once or twice to seed your

[05:52] wallet.

[05:53] Gotcha.

[05:54] Awesome.

[05:55] Also, you shouldn't use pnpm, you should just run the, run the commands as written.

[06:05] Ah, okay.

[06:06] Yeah.

[06:07] So, let's see.

[06:08] npm init...

[06:09] This is the trick I learned from you, how to set your type to module with a command.

[06:14] Oh!

[06:15] Oh, that's neat.

[06:16] Does that actually persist to your package.json?

[06:18] Yeah.

[06:19] Okay, sweet.

[06:20] Let me...

[06:21] So, check your package.json, yeah.

[06:25] Oh, look at that!

[06:29] Hey, thanks for that tip, Anthony.

[06:33] That's awesome.

[06:34] Back to...

[06:35] I'm gonna have to put that in my back pocket.

[06:38] So I'm installing dash 1.0, so I'm just gonna take a look at it.

[06:42] Yep, exactly.

[06:43] I'm just gonna take a look at the dash.

[06:48] Is this us?

[06:49] Yep, that's it.

[06:51] Yeah, nice.

[06:52] You guys, you guys landed the best package name ever.

[06:57] That's awesome.

[06:59] Yep.

[07:00] Yeah, we got...

[07:01] Dash is old.

[07:02] We've been around for a while, actually.

[07:04] Dash has been around for over 10 years.

[07:08] Ah, gotcha.

[07:09] So it was one of the earliest projects.

[07:12] Gotcha.

[07:13] Quick question.

[07:14] Yep.

[07:15] Do you want me to follow the tutorial the way I normally would, or is the goal over

[07:22] here to take a look at the tutorial and run through the tutorial?

[07:25] We can go wherever direction you want in terms of, like, if you want to go to different links

[07:28] and look at different stuff.

[07:30] We should follow the steps as closely as possible up until we get to a point where you can start

[07:35] deviating from it, which we can do at certain points along the way.

[07:39] But the most important stuff is going to be the setup commands and things like that.

[07:43] And you won't find this stuff in the Dash docs is kind of the point of this tutorial.

[07:48] So the idea is to see if this is going to work as you go.

[07:52] So if you skip steps, do it at your own peril.

[07:57] Gotcha.

[07:58] Okay.

[07:59] And that way we won't really be queuing the document either.

[08:02] So okay.

[08:03] I'll try and satisfy my intellectual curiosity quickly and on the side, but I'll follow the

[08:08] tutorial as it presents itself.

[08:12] So then we could get it going.

[08:15] I mean, it would be interesting.

[08:16] I imagine that that's probably an issue because of Windows.

[08:21] Yeah.

[08:22] Yeah.

[08:23] I wonder if just putting that in, like, a separate thing, like a separate markdown block

[08:34] might help.

[08:35] Yeah.

[08:36] Yeah.

[08:37] Cool.

[08:38] And yeah, this is mostly just to do your basic kind of get ignore setup and keeps you from

[08:48] accidentally committing your, your keys, which at this point is not a huge deal because platform

[08:53] is all, there's no real, real money that you're using, but at a certain point it will be,

[08:59] it will be a little bit of a pain in the ass to go through all these script files individually.

[09:10] Yeah.

[09:11] So actually I'll just, I'll just let you, let you read and go and see if this makes

[09:16] sense.

[09:17] Sounds good.

[09:18] Let me just refine the tutorial.

[09:19] All the note scripts that will be implemented by the end of the tutorial.

[09:25] Okay.

[09:26] So.

[09:27] This is, this looks like the package.json, it doesn't say that it's a package.json, but

[09:37] it's pretty clear that it is.

[09:39] Okay.

[09:40] So.

[09:41] I'll add here, I'll add a little open package.json right above it.

[09:51] That's good.

[09:52] I'm going to, let's see, a description, keywords, author, license, type, dependencies is important

[10:00] and scripts is important, so I'll take those and get blocked like this.

[10:10] Huh.

[10:11] Node and file is dot n and then there's script slash.

[10:15] Ah, okay.

[10:16] So we'll be adding these scripts.

[10:17] Oh, can you check a node version real quick?

[10:19] Yeah.

[10:20] Node-v.

[10:21] Okay.

[10:22] Great.

[10:23] Cool.

[10:24] I should add that node 20 is required.

[10:30] Yeah.

[10:31] It says that explicitly anywhere.

[10:39] So initialize dash client and query blocks.

[10:42] I'll create a scripts directory for scripts, so scripts and API and network will be set

[10:50] to testnet via network environment and dot n.

[10:53] Okay.

[10:54] So.

[10:55] Gotcha.

[10:56] So let's see what we did.

[11:06] So API and scripts and this should be empty, yep, and dot n should have network equals

[11:17] testnet, yep.

[11:18] So import dash from dash and pass the project's network in, okay, I see, and wallet configurations

[11:30] through dash's client constructor, okay, so I'm going to, I want to see how it feels

[11:37] under my fingertips.

[11:38] So.

[11:39] Yeah, if you want to like console log stuff out or things like that to kind of explore

[11:44] the code, feel free to do that as you go.

[11:50] Yeah, yeah, I'll probably do that, so dash dot n, and let's, dash dot, no, yeah, it's

[12:11] not in typescript, I'm sorry, no problem.

[12:17] You know, it should be though, it should be the way to get the types anyway, yeah, no,

[12:26] it is, it is, the intention is to have it give the typescript types, so if it's not,

[12:33] then we need to fix something.

[12:36] I might just not have done the pnpm install, so.

[12:40] No, it's the, the project is really not configured for typescript, so if they haven't made it

[12:45] so you'll get the types anyway through javascript, then I would, oh, look at that.

[12:51] Yeah, it'll have some default stuff, but I hear you.

[12:54] Okay, so you got, so you do have things in there, cool.

[12:58] Yeah, okay, capital C, and, yeah, we're, we're actually pretty good, so that works.

[13:07] So I didn't need to include a typescript dependency, that's so nice.

[13:14] Yeah, so we have the dash client set up, yeah, and create the wallets and mnemonic is set

[13:38] to null.

[13:39] To indicate we want a new wallet to be generated to get a new address or interesting wallet,

[13:45] we'll replace null with an existing wallet mnemonic.

[13:49] Okay, is a wallet mnemonic an ID, or is it more of an authentication method?

[13:55] It's an authentication method, you're gonna get a mnemonic and also an ID when you create

[13:59] your wallet.

[14:00] Gotcha, so a mnemonic is like my password.

[14:03] Yeah, it's 12 random words, and this is kind of a crypto convention.

[14:09] If you were to use MetaMask, which is Ethereum-based, when you start, that's the first thing they

[14:13] do, they give you 12 words.

[14:14] Some of them make you, like, write them back to you, or say, like, what was the first and

[14:18] what was the last, to make sure you actually saved it.

[14:21] Everything we're gonna do here, all the keys will be exposed, so that's, you don't really

[14:25] want to, like, use this wallet for anything, but like we said, there's no actual, this

[14:28] is all testnet still, so it's not really a big deal, but yeah.

[14:33] So I'll say a little bit more about that.

[14:36] The mnemonic is 12 words.

[14:39] It's not exactly random, it's 12 words from a dictionary of, I believe, maybe 4,096, or

[14:49] one of those powers of two, and I don't remember exactly how many, but it's in the thousands

[14:56] of words that are possible, and it's essentially a seed that you use.

[15:05] It's a random seed, but instead of, you know, zeros and ones, you start with 12 words, because

[15:12] it's a way for you to, a lot of stuff is derived from the 12 words, with different algorithms,

[15:23] but because this will be, one of the things it's deriving is private key, public key pairs,

[15:31] many of them, potentially, and because there's value in there, you know, when you have private

[15:39] and public keys, it can be used for lots of different things.

[15:43] One of those things that it's used for is to store, like, that's how you actually transact

[15:48] value on the blockchain.

[15:49] So stop me if you want some more detail on any of this, like the public/private key pairs

[15:57] I'm sure you're familiar with from a development standpoint, but in, yeah, in cryptocurrencies,

[16:05] they're used primarily to derive private key and public key pairs, and so because that

[16:11] will eventually or potentially have value on it, it's put in the 12-word format so that

[16:18] it's easy to, like, copy down and back up as, you know, write it, like, physically writing

[16:23] it down on a piece of paper, and then importing 12 words into a wallet, for example, from

[16:31] a written down piece of paper is easier than zeros and ones, or I's and L's and things

[16:37] like that.

[16:38] So that's the whole purpose behind the specification, there are a lot of technical specifications

[16:45] that go around these 12 words, but yeah, it's pretty involved, but that's kind of the basis

[16:51] of this.

[16:52] Gotcha.

[16:53] Yeah, I was doing the, I was trying to do the math in my head, so that's what, some

[16:58] number followed by three, what, three times 12 zeros, so something followed by 36 zeros

[17:06] is the kind of entropy we're talking about, so that's interesting.

[17:10] Yeah, and if you just want to open up a new tab, just so that you have this in your browser

[17:15] history if you want to look at more, go ahead and look, go to github.com/dashhive, and yeah,

[17:29] and so if you know AJ O'Neill, one of the hosts of JavaScript Jabber podcast, he's done

[17:35] a lot of the low-level work in building libraries that, and documentation that discuss in detail

[17:43] what a lot of this is all about, specific to the Dash cryptocurrency, but the 12-word

[17:48] concept is not specific to Dash, it's just there are certain bits and whatnot that Dash

[17:56] uses that other cryptocurrency doesn't, like there are certain ones that each cryptocurrency

[18:01] will have their own bits for certain things, but you can look at a lot of this stuff if

[18:08] you're ever interested, like Dash phrase is the one that we're talking about right now,

[18:13] that's a library that generates this 12-word phrase, and you can kind of see, yeah, documentation

[18:23] about that if you're interested, and then the other Dash Hive libraries build on that

[18:29] concept, derivation of the keys and whatnot.

[18:33] >> Gotcha.

[18:34] Very cool.

[18:35] Thanks for the walk-through, that's actually super useful, because a lot of people think

[18:44] that it's just theory, but really that's how you orient yourself, so this is kind of giving

[18:49] me that bearing, thanks, Rion.

[18:51] >> Yeah, you bet.

[18:52] >> Yeah.

[18:53] I see what you mean.

[18:55] So this will get turned into some sort of --

[18:58] >> And if you could bump up your font, just for anybody that might be watching, we do

[19:04] have at least five people watching, so who knows?

[19:07] >> Yeah, 100%.

[19:08] Who knows how many in the future?

[19:12] >> So the Zoomonic thing is just, yeah, that's a play on words for the mnemonic and using

[19:18] a test case for the words.

[19:21] Zoo is one of those permitted words in the dictionary, and you'll notice at the very

[19:26] end it says "wrong," the reason for that is that there's actually a checksum involved,

[19:34] and so if you -- that Zoo, Zoo, Zoo mnemonic is derived from some other random number -- oh,

[19:45] it's the FFF, the input entropy right there.

[19:49] If that's your -- that's obviously not random, but if you did use that as your input entropy,

[19:55] then the recovery phrase that you get from that is that Zoo, which you can imagine that

[20:02] that's because F is near the end of a list and Z is near the end of an alphabetical list,

[20:09] but the "wrong" at the end is just how the checksum works.

[20:12] So we won't go into all that detail, nor do I really know all the detail, but it's there

[20:18] for you if you want.

[20:20] So that's a mnemonic that's primarily used for test cases.

[20:24] >> Gotcha.

[20:25] So what's a seed?

[20:28] >> So the seed is -- so the 12-word thing -- and it's fine that we're spending some

[20:35] time on this, because it's an important key concept.

[20:38] The seed -- so the 12 words is called a seed phrase, and the seed phrase ultimately gets

[20:46] translated into a seed, which I think is -- I don't know what -- that looks just like hexadecimal

[20:53] to me, but yeah, that's derived from the seed, and that's what's actually used to seed the

[21:02] key pairs.

[21:03] So it's kind of like if you think about it as a pipeline, you have input entropy that

[21:10] comes into the pipe, and then through an algorithm that spits out a recovery phrase so that users

[21:16] can have a user-friendly 12 words to work with instead of writing down any kind of hexadecimal

[21:22] or other alphabet for their backup.

[21:25] And then this secret salt is one of the things that goes into the algorithm as well, and

[21:32] then further down the pipe, then it pumps out a seed.

[21:35] So I believe that this particular library is focused on just that small part of getting

[21:46] whatever device you're using would create some input -- a random input entropy, and

[21:53] then it would go through the algorithm.

[21:55] It might use some certain defaults, like the secret salt of Trezor.

[22:00] Trezor is a company that created this specification, among other things, hardware wallets, things

[22:07] like that, and the seed is what you get out.

[22:11] And then you would take that seed, and then you'd put it into a different library that

[22:15] would use the seed as an input to create the private/public key pairs, for example.

[22:22] So this is sometimes done all in one library, but the way that AJ made it, he just wanted

[22:28] to -- so that it's more understandable and more of a Unix philosophy, doing one thing

[22:35] with one library.

[22:37] That's what you would then get out of this library as a seed, but that would be the input

[22:41] to another part of the process.

[22:43] Makes sense.

[22:45] This almost feels like the future of passwords, to be honest.

[22:49] Coming from someone who's more of a traditional web dev, this is a neat solution for a lot

[22:56] of problems.

[22:57] But yeah.

[22:58] Yeah, AJ is one of the biggest cryptocurrency skeptics around, and he says that this is

[23:05] one of the best things that the cryptocurrency industry has actually developed, is these

[23:10] standards around 12-word seed phrases, and the subsequent creation of what's called hierarchical

[23:19] deterministic key generation.

[23:21] So from these 12 words, you can couple that with a -- what's called an HD path, a hierarchical

[23:29] deterministic path, and that's a different library, if you looked into that.

[23:34] I think that's called dash -- it's either called -- it's the next library built on top

[23:40] of this would probably be dash keys, and then on top of that is called dash HD, and that

[23:46] dash HD is the thing that then takes those key pairs and makes deterministic key pairs

[24:00] based on a path that's cryptocurrency agnostic.

[24:06] So you could have these 12 words, and then those 12 words could create Bitcoin addresses,

[24:14] Ethereum addresses, Dash addresses, any cryptocurrency addresses, or even just things that you might

[24:22] not use cryptocurrency -- for cryptocurrencies, you could put as part of the HD key path.

[24:29] And so that way, you would have -- you could have a whole password management system based

[24:33] on this concept of HD keys and deterministic keys built on those -- on that 12-word phrase,

[24:42] and so that you could literally have, like, all of your life's passwords derived from

[24:48] a single 12-word key phrase, including, you know, cryptocurrencies of every flavor.

[24:55] So we went a little bit deep in that, but there you go.

[24:58] >> No, that's fascinating.

[25:01] It's fascinating.

[25:02] So you could actually build a password manager where the input is a deterministic input and

[25:09] a deterministic output, so you could maybe hash together your input pair -- your input

[25:16] 12 set and the domain that you're trying to log into, and you get a deterministic password

[25:23] for that domain.

[25:24] Like, I sort of -- I think I see where that's going.

[25:27] That's really neat.

[25:28] >> Yep.

[25:29] And I think there are some people that have done this, and so it's -- you know, with 10

[25:33] years of this specification, there's been a lot of work, but it hasn't really creeped

[25:38] into -- crept into the Web 2 space as much as it might in the future.

[25:44] But, yeah, maybe -- maybe we can head back to the tutorial then.

[25:50] Now I just wanted to give you some more context behind that 12-word stuff.

[25:53] >> Gotcha.

[25:54] Thank you.

[25:55] >> That was -- you are enriching my life, so thank you.

[25:59] >> Yep.

[26:00] >> Cool.

[26:01] I guess we were setting mnemonic to null, and now that I know what that mnemonic is,

[26:08] it makes sense.

[26:09] Offline mode is true because we don't want to sync the chain when we use minus null.

[26:15] Okay.

[26:16] So we're basically in dev mode right now with mnemonic and offline mode?

[26:21] Is that -- is that right?

[26:24] The way that this library works, which is not something that we've developed.

[26:27] This is something that a different organization within Dash has developed.

[26:31] I think that their use -- their use of the -- those -- those option -- that option object

[26:40] is that if you have null for the mnemonic, the library is going to create a 12-word phrase

[26:46] for you, but if you already had a mnemonic, you could put that in there, and then it would

[26:51] use that.

[26:52] >> Gotcha.

[26:53] Okay.

[26:54] So...

[26:55] >> I'm not exactly sure what the offline mode does.

[26:59] >> Gotcha.

[27:01] Get this block hash, return block hash, change it.

[27:10] I guess this is describing -- this is a bit of a non-sequitur over here.

[27:19] All of a sudden, I'm reading things that I haven't seen before.

[27:23] So...

[27:24] >> This is explaining the code that's coming up.

[27:32] So...

[27:33] >> Yeah.

[27:34] >> Put it after the code is what you're saying.

[27:35] >> Yeah.

[27:36] I think so.

[27:37] >> Okay.

[27:38] >> So...

[27:39] >> Yeah, you just write the code first, and then reorient yourself.

[27:43] >> Yeah.

[27:44] So...

[27:45] Inside here...

[27:46] Oh, okay.

[27:47] Gotcha.

[27:48] Gotcha.

[27:49] So...

[27:50] I got this into getBlockMethods, and at this point, it's getBlockMethods, okay.

[27:59] Okay.

[28:00] So...

[28:01] DAPIClient.core, getBlockHashes, getBlockWeights, or getBlockByHeight, okay.

[28:20] All right, I see.

[28:37] So getBestBlockHash returns the BlockHash of the chained up, getBlockHash returns the

[28:43] BlockHash of the given height.

[28:47] We're not passing in a height right now, a position of a block in the chain, first block

[28:54] to ever align is a height of zero, okay, I see.

[28:58] Subsequent block is added, increase the height by one, okay.

[29:02] So it's getting bestBlockHeight would be, I guess, the absolute, like, the current height,

[29:10] I guess.

[29:11] >> Yeah.

[29:12] I went back and forth whether you would leave this in the tutorial or not.

[29:20] It's kind of a way to just query it, so it's like a good kind of first step, but it introduces

[29:25] a whole bunch of terms and jargon that kind of takes a while to understand.

[29:29] So it might make more sense to just kind of have a link there to the docs and say, if

[29:34] you want to learn more, click here, then kind of have this in here.

[29:38] >> It could be something that we could hide behind a details triangle.

[29:42] >> Yeah.

[29:43] >> Yeah, I think a diagram would be helpful, because what I'm, like, I'm not sure if this

[29:49] is a 2D space or a 3D space, or if it's just like, you know, a spinal column.

[29:55] >> It's a linked list.

[29:56] >> Okay.

[29:57] So it is like a spinal column, cool.

[29:59] And since it's a linked list, I can get the thing at the tip, okay, so it's the tip of

[30:06] the linked list, get the block hashes.

[30:11] I don't know what these things are doing, so I guess you can move on, because the code

[30:17] is there.

[30:18] So there's this specific block by its height, and the buffer is a block, it's a corresponding

[30:23] block hash.

[30:24] Yeah, this is also, I'm not sure why this needs to be done, I'm not sure why any of

[30:28] this needs to be done, so, yeah, expandable column would be amazing.

[30:33] And then I do get block methods.

[30:44] Okay.

[30:49] So no idea what that did, but okay.

[30:53] >> Yeah, let's keep going, let's do the wallet one, we'll hopefully make a lot more sense,

[30:58] let's just skip past this part.

[31:00] >> Sounds good.

[31:01] So, get block by height, returns a buffer object, okay.

[31:14] So buffer, okay, block hash, so that's the block that I got, and then the hash of the

[31:35] block, the hex string, that's the hash, okay.

[31:41] And get best block hash, returns a hash of the lowest block, this is the current state,

[31:51] okay.

[31:52] Gotcha.

[31:53] Okay, gotcha.

[31:54] And this is a type one, but that's like ancient history, right?

[32:00] >> So if you read the last sentence in that block, it says it's the first block after

[32:04] the genesis block.

[32:05] So every block chain, when it starts, it has its first block that records the block.

[32:10] So the thing in the chain has started, and then people make transactions, and those get

[32:13] recorded on new blocks that then stack on top of each other over time.

[32:18] So this kind of is written to assume that you know what a block chain is, I should also

[32:21] probably put a little link to be like, here's what a block chain is, you know?

[32:26] And none of this stuff is really like necessary for the tutorial, it's more so to, if you

[32:33] want to get some insight into what's actually happening on this block chain before you create

[32:36] a wallet and start throwing money on it and interacting with it, here's some stuff you

[32:40] can kind of do to inquire into it.

[32:43] But it really makes more sense to kind of bump around a platform explorer, which we're

[32:49] going to do later.

[32:51] So yeah.

[32:52] >> Gotcha.

[32:53] So all of this is describing the what, but --

[32:55] >> The dash block chain.

[32:56] >> No, sorry.

[32:57] No, no.

[32:58] What I'm trying to say is that this is describing the what, but not the why.

[33:02] >> Correct, yeah.

[33:03] >> So I know what it's doing, but I don't know why we're doing it yet.

[33:07] So I'm assuming that'll sort of reveal itself as we go.

[33:11] But just feedback and notes, that's all.

[33:15] >> Yep.

[33:16] Yep.

[33:17] >> So create wallet and do we need -- quick question, do we need all three functions over

[33:28] here and then all three functions over here?

[33:31] Do we need all --

[33:32] >> So this is just going to do a single thing and create wallet.

[33:36] So these will all be kind of more single use than the get block methods.

[33:41] So this one is just going to do -- it's going to create something for you that is going

[33:47] to console log two things.

[33:48] So it's only running a single function to do that.

[33:51] >> Gotcha.

[33:52] >> So go back to your terminal output.

[33:56] >> Yeah.

[33:57] >> Yeah.

[33:58] There you go.

[33:59] So you're going to want to copy/paste that and put it in your .emv, which may or may

[34:03] not be written.

[34:04] I'll make sure it is, but it's not -- yep, it's there.

[34:09] You got it.

[34:10] >> Great.

[34:11] And that's going to be a recurring pattern as we go.

[34:15] You're going to be writing these commands and get this info back.

[34:19] And it's written in a way where you can just -- you should be able to just copy/paste what

[34:23] you get out because it's giving it to you in this format.

[34:26] So it's trying to make it as error proof as possible for people who are writing through

[34:30] this.

[34:31] Because if you have -- every time you run a command, you have to be like, here's what

[34:32] you need to find in the output, and then copy/paste it into .emv, and it adds more steps, which

[34:38] can help with learning, but also makes it much harder to ensure that things aren't going

[34:42] to go awry along the way.

[34:44] >> Makes sense.

[34:45] I wonder if this could be wrapped into a CLI of some sort.

[34:49] But I digress.

[34:52] This makes sense so far.

[34:56] I'm not a super huge fan of different one-off scripts for different sections.

[35:05] I don't know if we're going to go back and use create wallet any time in the future or

[35:10] use get block method any time in the future.

[35:14] But if these are one-offs, then it might be better to just do all the one-off stuff in

[35:18] one script and just get that out of the way, maybe?

[35:21] Just a thought.

[35:23] >> Well, then, yeah, so, yeah, I think we should revisit that one for further, and then

[35:29] you kind of see what's happening in terms of each of these and what they're doing.

[35:31] I think it will make more sense as we go, and then you can kind of let me know how you

[35:37] would actually want it to be structured, because if we did that, everything would be in a single

[35:40] file.

[35:41] >> If we did that, everything would be in a single file.

[35:44] Yes.

[35:45] Yeah.

[35:46] Exactly.

[35:47] And that might just be -- I mean, it depends on what your goal is.

[35:49] If your goal is to -- if you're assuming that the person going through this has a large

[35:56] amount of time and patience, and for whatever reason, then maybe they're working on it,

[36:03] or maybe, you know, they're getting paid to go and curate a tutorial like I am, but if

[36:08] I was just somebody coming here and trying to set up something on the platform, then

[36:15] I may or may not have the patience to go and actually find out what all these things are

[36:19] doing.

[36:20] So it's not the most gentle learning curve.

[36:22] >> That is -- well, it's a gentle learning curve since that's slow.

[36:28] You can -- at the very beginning of the post, there's a link to the repo.

[36:32] So if you want to just clone the repo and play with it in its finished state, that's

[36:37] an option as well.

[36:39] So the point of this tutorial is kind of to make every step explicit so that you can learn

[36:46] it as you go, not necessarily get me to the end as quick as possible.

[36:52] Does that make sense?

[36:54] >> It does.

[36:55] >> And so -- but I do agree that there should be a way to just like kind of do like clone

[37:00] this thing, get -- run this command to spin it up, and then you could just do a couple

[37:04] steps and kind of get to the end product.

[37:06] There would be like a kind of cheat sheet maybe at the beginning that would just give

[37:10] you a really, really condensed version would probably be good.

[37:14] >> Yeah, it's hard writing these because you don't -- you know, different people have different

[37:20] goals and both -- on both the producer side and the consumer side.

[37:25] >> We actually -- what I would like to look at, if we go to dash.org and just compare

[37:29] this like the official docs, it's similar but has a couple slight differences.

[37:34] So zoom in a couple.

[37:35] And then we're going to go to developers in the top, I think, and then documentation,

[37:40] yeah, platform, the middle one.

[37:45] So go to tutorial introduction, yeah, and then bump your font up.

[37:52] Yeah, so what this does is it breaks each step up into -- so if you go to connect to

[37:59] a network, this will give you the first script, I think.

[38:06] >> So basically Anthony's tutorial is this tutorial somewhat modified.

[38:14] >> Yeah, so you see here that they sort of set it up also as one-off scripts but they

[38:21] also put the client in each script in general.

[38:24] So I've already abstracted some things into my version that makes it more -- make more

[38:29] sense as a unified project because otherwise if you were to copy and paste the code straight

[38:34] from here, things get very confused very fast because you have all these different client

[38:37] objects around.

[38:39] So there would be ways to consolidate the script functionality but every script is kind

[38:48] of important.

[38:49] And not necessarily -- some scripts could be skipped and there's even more in this docs

[38:53] that I didn't include.

[38:55] But it's kind of like more of an API reference that also goes in a sequence that you could

[39:02] follow, like a tutorial.

[39:04] >> Understood.

[39:05] Yeah.

[39:06] I think -- I think your documentation is way more detailed than what I'm seeing over here.

[39:13] Because over here it's just saying do this stuff but these are just magic words.

[39:17] Meanwhile, what I'm reading over here is actually way more -- where did it go?

[39:22] Like this is way more detailed and this is way better in my opinion.

[39:26] >> I'm glad to hear that.

[39:27] Thank you.

[39:28] >> Yeah, like I'm looking at this going what?

[39:32] So yeah.

[39:33] >> Yeah, it took me a little while to figure it out.

[39:34] And I had like two years of Web 3.0 blockchain experience already.

[39:38] >> Oh, wow.

[39:39] >> So can you imagine?

[39:40] >> Yeah.

[39:41] This is the big challenge here is we're trying to -- we're trying to get a tutorial that

[39:48] introduces Dash platform to developers.

[39:51] And those developers are going to have different purposes, different desires, different styles

[39:57] that they like.

[39:59] So it's impossible to please everyone.

[40:00] But what we'll do is -- you know, you're the first, Monarch.

[40:03] You're our guinea pig.

[40:06] But we'll probably do at least five before we make any -- well, not at least, but we'll

[40:13] want to get a good broad lay of the land about like what people's experience is.

[40:19] And then we'll make some changes based on at least a few --

[40:22] >> A couple changes I'm already pushing.

[40:25] Like --

[40:26] >> A couple changes we can make.

[40:27] Those are the things that need to be pointed out.

[40:28] But if there's any like broad structural changes we want to make and people suggest or desire

[40:34] or something, then that could definitely be possible.

[40:37] Or just create another one that is also what some people want, because some people might

[40:40] like this one or some people might want it to be slightly different.

[40:42] So we'll kind of see.

[40:44] >> So let's keep plugging along, and then we'll -- you know, we'll see how far we can get.

[40:49] And it might make more sense why things were done a certain way at the end.

[40:55] >> Yeah.

[40:56] So this part's pretty important.

[40:57] You've got to go to the test net.

[41:00] So scroll up a little bit.

[41:03] Yeah.

[41:04] >> Yeah.

[41:05] Sorry.

[41:06] I'm just going to go ahead and do that.

[41:10] This thing?

[41:11] Okay.

[41:12] >> Yeah.

[41:13] Ideally, it would be easy to just Google the test net and find it, but that should open

[41:17] a link for you.

[41:18] >> Yeah.

[41:19] >> There you go.

[41:20] And it might take a second to load or possibly crash.

[41:23] So -- >> Sounds good.

[41:27] >> Yeah.

[41:28] So this also happened to me.

[41:32] >> Oh, really?

[41:33] >> So copy/paste the URL, but take off the HTTPS.

[41:38] Like, just do the thing, and then try re-running that.

[41:41] Yeah.

[41:42] Because their freaking HTTPS is all messed up.

[41:45] It's been like that for a year and a half.

[41:49] >> Yeah.

[41:50] At some point, we need to have a better faucet experience, for sure.

[41:53] We'll deal with it for now.

[41:54] >> Yeah.

[41:55] So now you've got to put your -- okay.

[41:57] So go back to your wallet and copy/paste the address.

[42:01] Yeah.

[42:02] So your wallet address right there, and then that's what you've got to put in at the very

[42:06] top.

[42:07] Yeah.

[42:08] And that gets you the coins.

[42:10] This is, like, the step where the most error can be added in.

[42:15] And I wish there was a way I could just -- there probably is, but I want to see how they're

[42:19] doing the API call, and literally just build that also into a JavaScript command.

[42:23] >> Yeah.

[42:24] We'll work on this.

[42:25] >> Because what's going to happen now -- this is -- actually, the last time I used this,

[42:29] this was able to complete.

[42:31] What it used to do is it used to then crash when it completed, and you got the money.

[42:36] So you'd get no feedback, and it would crash.

[42:38] You would think it would be broken, but you would get the -- let's see what happened.

[42:42] >> I think exactly what you said.

[42:44] >> Yeah.

[42:45] So what I did, it actually refreshed and worked and told me how much it gave me.

[42:49] But that seems to be a rare occurrence.

[42:51] But I think you do -- you did get it.

[42:53] So let's go back to the post.

[42:58] And then go to the dash, click the other link.

[43:01] Yeah.

[43:02] And then put your -- add to the same address that's in your clipboard.

[43:06] Yeah.

[43:07] Search for that.

[43:08] Uh-huh.

[43:09] >> Nothing yet.

[43:10] >> Yeah.

[43:11] So if you refresh -- let's see -- just make sure -- double-check that that's the address

[43:21] that you had in your .env.

[43:24] Okay.

[43:25] >> Yeah.

[43:26] It definitely is.

[43:31] >> Okay.

[43:34] Well, let's keep going.

[43:38] And if it's --

[43:39] >> If it didn't work, it would have been there by now.

[43:41] So we got to do that.

[43:42] >> Sounds good.

[43:43] >> Yeah.

[43:44] It's not going to work, though, if we do this.

[43:45] Let's see what happens, though.

[43:46] >> Oh, man.

[43:47] This is brutal.

[43:48] >> No, no.

[43:49] It's not horrible.

[43:50] I mean, no more dash for you.

[43:51] Come back in an hour.

[43:52] >> Yeah.

[43:53] So that's what we think.

[43:54] It might be in there, but it's not showing up for some reason on the block explorer.

[44:05] So let's try to keep going through the commands.

[44:08] If things don't work, it will tell us that you don't have funds.

[44:11] >> Gotcha.

[44:12] Sounds good.

[44:13] Is there a way to do this via the client in JavaScript?

[44:18] >> Not that I'm aware of.

[44:21] It's not in the documentation.

[44:22] If there is a way.

[44:23] That's why I was saying I needed to figure out how they're connecting to the faucet at

[44:28] all from the web UI and then try to -- let me look at that right now, actually.

[44:34] >> Gotcha, gotcha.

[44:35] Cool.

[44:36] I've been saying I wish this part was nicer for a very, very long time, and I've done

[44:40] my best with it.

[44:41] Here we are.

[44:42] >> You've done a hell of a job here.

[44:47] It's like reading this stuff is -- if I'm going slow and I'm reading this, then there's

[44:52] a wealth of information over here, and I'm honored to be the guinea pig, and as a guinea

[44:58] pig, it's not that horrible.

[44:59] It's like I can actually make sense of what's going on.

[45:02] >> And ideally, yeah, if something doesn't actually go quite as planned, you can compare

[45:07] to the screenshots and see what should be happening.

[45:10] >> Makes sense.

[45:11] Okay.

[45:12] So are we dead in the water until we finish this?

[45:16] >> Not necessarily.

[45:17] Let's keep going, and then we'll know immediately if we need to send you stuff, and we could

[45:22] -- one of us could wire you some dash, we could loan you some.

[45:28] >> Gotcha.

[45:29] >> Anthony, why don't you -- while he's doing that, why don't you -- can you try to get

[45:36] some dash to that address?

[45:38] >> Yeah.

[45:39] Can you copy -- so we just need him to copy/paste it into the chat for us.

[45:46] >> I'll go ahead and go to the -- I'll see if there's a different faucet that I can get

[45:51] working.

[45:52] >> I should have one that's pretty much good to go.

[45:58] I just got to -- >> You can also drop that in the chat.

[46:13] >> I'll go ahead and -- >> I'll go ahead and -- I'll go ahead and -- I'll go ahead and -- I'll

[46:41] go ahead and -- >> It sounds -- it looks like the faucet

[46:57] is using the address, the dash testnet address to determine whether people get dash or not

[47:07] rather than, like, an IP address.

[47:09] I don't know why it would do that.

[47:12] These faucets are old and made by other people than us as well.

[47:20] Did you have any luck doing -- getting that, Anthony?

[47:23] >> So I'm -- I think I'm going to be able to send funds.

[47:26] Just give me one second.

[47:27] I'm going to try and send him one dash right now.

[47:29] >> Okay.

[47:30] So you maybe got some testnet dash -- >> I got some earlier today, and I've got

[47:35] my whole wallet set up right here, so I'm just going to see -- I'm looking at this.

[47:55] >> The next step is a little messed up, too.

[47:58] >> All right, Monarch, so I'm now looking back at your screen.

[48:02] So what did you -- what command did you run that didn't -- wasn't --

[48:05] >> Create identity.

[48:06] >> Yeah.

[48:07] >> Create identity is not going to work without dash in the wallet.

[48:11] >> That's what we're trying to do right now.

[48:15] >> So that's -- we are kind of dead in the water until we can get that worked out, but

[48:19] is the error at least clear?

[48:21] Let's see.

[48:22] >> Ish.

[48:23] It says unimplemented, which I don't know what to make of.

[48:29] That doesn't sound like it's a payment issue, then.

[48:37] >> Are you able to send him money, Rion?

[48:39] You've done that for me before.

[48:42] >> I don't have any testnet funds on me or even an address, so I'd have to --

[48:46] >> I can give you -- I mean, I can give you a daddy in via call, so how do you send funds

[48:50] when you do that?

[49:00] >> I know our web wallet doesn't support testnet yet, but there are wallets that do.

[49:06] >> I just sent you everything in Discord with the wallet address and mnemonic and stuff.

[49:12] This has got, like, four dash on it, I think.

[49:20] >> As part of the SDK, Anthony, to answer your question, there's a way in the SDK to

[49:24] send funds.

[49:25] But I --

[49:26] >> Yeah, I'm trying it right now.

[49:29] I'm getting a weird error.

[49:31] It says permission denied.

[49:32] I'm not sure why.

[49:33] >> Okay.

[49:34] >> This is one thing that I did not put in the tutorial, which I'm realizing now probably

[49:40] should be.

[49:42] >> Because the faucets aren't reliable, that might be a good thing, but obviously the thing

[49:47] we really need to fix is the faucet itself.

[49:53] But we could go back and start the tutorial over, getting a new mnemonic and address,

[50:01] and then the faucet might be --

[50:02] >> It might work this time.

[50:03] >> It might work.

[50:04] >> I mean, that's pretty easy.

[50:05] We just got to run the create wallet command again, but first we got to go back to client

[50:12] and API and change new mnemonic to null real quick.

[50:18] Yeah.

[50:19] >> Yeah.

[50:20] So did that.

[50:22] Should I clobber --

[50:23] >> Yeah, might as well.

[50:25] Yeah.

[50:26] >> Yeah.

[50:27] >> Everything but network.

[50:28] Yeah.

[50:29] >> Yeah.

[50:30] I think everything else should be the same, so --

[50:34] >> Yeah.

[50:35] >> So you just got to run the npm, run create wallet.

[50:57] And then I think that will go to the faucet.

[51:22] >> You have to do the same as you did last time.

[51:30] >> Yeah.

[51:31] >> Okay.

[51:32] >> All right, everyone cross your fingers.

[51:52] And then while you're waiting for that, you can just go ahead and go to the Explorer,

[51:58] which is --

[51:59] >> And if this doesn't work and we can't send him funds, what we can do is I can give him

[52:05] my wallet that I created and that I just sent to you and he can go forward in the tutorial

[52:11] with that.

[52:12] >> Oh, I got that.

[52:13] >> It worked that time.

[52:14] Look at that.

[52:15] Sweet.

[52:16] >> Faucet gods.

[52:17] >> This is a common thing with Dash and blockchain stuff.

[52:23] You're copy pasting the right address.

[52:31] Let's try going to the actual platform Explorer.

[52:35] So go to platform-explorer.com.

[52:50] >> I don't think -- I don't know if this platform --

[52:53] >> The link is in the -- it's a little bit further in the tutorial.

[52:58] Hold on.

[52:59] Give me one second.

[53:00] >> I don't know if it shows wallet addresses, though, balances.

[53:03] I don't know if that's right.

[53:05] >> Oh, it is.

[53:06] Platform-explorer.com.

[53:07] Yeah, actually, you're right.

[53:08] >> So I'm wondering, let's see, what's the Explorer that you're using?

[53:30] Not the platform Explorer, but the core Explorer.

[53:33] What's the URL on that?

[53:39] >> This one?

[53:40] Are you talking to me?

[53:41] >> Yeah.

[53:42] >> Yeah, go to the first Explorer you're looking at.

[53:47] >> Presnet.insight.dashevo.org.

[53:53] That's -- okay.

[53:54] I'm going to look at a different one.

[54:00] And then can you, Anthony, or Monarch, can you post the new testnet address in --

[54:12] >> I think I might know what the issue is.

[54:16] I think we should be using a different URL.

[54:19] Hold on.

[54:20] >> Yeah.

[54:21] >> Go to explorer.dash.org/insight.

[54:22] Try that.

[54:23] Actually, just explorer.dash.org.

[54:24] >> Explorer.dash.org.

[54:30] >> Yeah.

[54:38] See if this is different, if this works.

[54:40] >> No matching records, no.

[54:43] >> Oh.

[54:44] >> No.

[54:45] Let me go to this one.

[54:50] I'm going to post the link.

[54:58] Try it in that one.

[54:59] >> Let's see.

[55:00] >> Yep.

[55:01] There you go.

[55:02] >> Whoa.

[55:03] So what is this?

[55:10] >> This is the best testnet inside Explorer that I know of.

[55:14] So I'm not sure where the one was that you have in your documentation.

[55:18] >> I mean, so now I see all these go to the same site.

[55:23] They all have different URLs and apparently give back different information.

[55:26] The one that comes up first in Google was the second one, platform.

[55:29] >> Yeah.

[55:30] >> Explorer.dash.org.

[55:31] >> You're not going to want to use anything on Google because Google is going to be wanting

[55:38] -- it's going to be trained to find the main net explorers, and we're dealing with testnets

[55:44] right now.

[55:45] So --

[55:46] >> It used to work, though, with that link in the past.

[55:49] It's just not anymore, but it did in the past, so I'm not really sure why that changed.

[55:54] >> Yeah.

[55:55] We'll need to have --

[55:56] >> This link you gave me, again, this is HTTP, so people are going to go to this link and

[55:59] they're immediately going to be told by their browser this is an insecure site.

[56:03] >> Yeah.

[56:04] Take it up with Dash Core Group.

[56:07] >> I mean, in theory, we should be able to host our own, and if we really want to be,

[56:18] you know --

[56:19] >> I wonder how hard it would be just to build in these couple things into platform explorer

[56:23] so you can actually see the addresses.

[56:24] Like, that's the thing to do, because platform explorer is, like -- that seems to be the

[56:28] thing.

[56:29] There's not going to be a whole bunch of extra ones that work in different ways.

[56:32] It's going to be, like, a single maintain thing.

[56:34] >> Yeah, in theory, this one's supposed to be maintained also.

[56:38] >> Anyway, we have the money, so let's create the identity.

[56:42] >> Yeah.

[56:44] >> So I go here, and I modify my client to what it was, and then I create an identity.

[57:11] It seems better than the last time.

[57:21] >> Yeah, and this one takes a while, so if it's hanging, that probably means it's going

[57:24] to work.

[57:25] >> That's good news.

[57:26] Okay.

[57:27] So, Rion, that link you had, where did you originally get that?

[57:44] >> No, I got errors again.

[57:45] >> Okay, let's see.

[57:47] Let's read it.

[57:48] >> Max retry is unimplemented.

[57:50] >> Okay, this hopefully is just one of those errors that will go away if we try it again.

[58:00] This is a step that involves sometimes things will just break for reasons that don't entirely

[58:04] make sense, and it's just because testnet is not very reliable.

[58:10] I'll put it that way.

[58:13] >> It is true.

[58:14] It is true.

[58:17] This looks like it's going to probably get the max retries again as well, so we'll keep

[58:26] trying for a little bit.

[58:29] Let's --

[58:30] >> Looks like, yeah, I got you saying there -- can we try this?

[58:36] Let's have you use my keys and see what happens.

[58:41] So I'm going to put these -- actually, what would be the best way for me to send you a

[58:48] message, Mark?

[58:49] >> Yeah.

[58:50] >> Well, do you want me to just -- actually, let me just put this right in the chat.

[58:56] I think you should be able to just copy/paste it and just go back to the stream.

[58:59] >> Should I hide these off the stream?

[59:01] >> You don't need to hide any of this stuff.

[59:03] This is all stuff that's totally fine to expose.

[59:05] So just go to the stream.

[59:06] You already can do all this on camera.

[59:07] It's fine.

[59:08] >> Okay.

[59:09] So I'll drop -- so just confirming, I'll drop your credentials in my .env.

[59:15] >> Correct.

[59:16] Yes.

[59:17] The credentials are in the private chat right now.

[59:18] And then -- yeah, I was afraid that was going to happen, so just do that real quick.

[59:32] And then for now, let's comment out everything below ID.

[59:39] Yeah.

[59:40] Yeah, exactly.

[59:41] And then comment out yours off the top as well.

[59:43] Yeah.

[59:44] Okay.

[59:45] Well, let's give this a try.

[59:48] See what happens.

[59:49] So now just rerun the create identity again.

[59:57] >> You're going to want to know -- you're going to want to put the 12 words from your

[60:00] mnemonic right in there.

[60:02] Have you done that?

[60:03] >> Yes.

[60:04] >> The 12 words in the mnemonic are there with the address, yeah?

[60:07] And those are both in the API client through the environment variables.

[60:11] >> Okay.

[60:12] Oh, yeah.

[60:13] I got it.

[60:14] >> Yeah.

[60:15] >> No.

[60:16] >> Same issue.

[60:17] Hold on.

[60:18] >> While you're doing that, I'm going to mess --

[60:25] >> So you're using PMPM, so I'm not sure if that's an issue or not.

[60:29] >> It shouldn't be.

[60:30] But --

[60:31] >> Let me -- let me -- what were you going to say, Rion, what were you going to say?

[60:43] >> I was just going to say, I'm going to message the Discord testnet channel to see if there's

[60:49] any known issues on testnet right now.

[60:54] >> Anthony, if you -- or Monarch, can we print the -- can you post the error so I can post

[61:03] that in Discord and see if there's any issue?

[61:06] We're not going to solve them, I guess.

[61:07] >> Yeah.

[61:08] And then I would say, next thing we should do is uncomment out my identity ID and just

[61:11] skip this step and keep going.

[61:12] >> Let me put this in a paste bin.

[61:20] This should be safe to drop in a paste bin, right?

[61:23] >> Yeah.

[61:24] >> As long as you're -- like, your file structure for your code thing being in there, that's

[61:33] the only thing.

[61:34] That would be considered even slightly sensitive.

[61:36] >> Yeah.

[61:37] >> I actually just -- I actually just drop these in, you know?

[61:43] >> Okay.

[61:44] >> I got it.

[61:46] >> Cool.

[61:47] >> My npm install is still going, so I'm going to wait for that, then try running --

[61:54] >> Yeah.

[61:55] And this is why it's nice to use pnpm, because it's way faster, but I've found that every

[61:59] now and then some weird things happen.

[62:02] But it looks like that type of error you're getting makes me think it's testnet, not anything

[62:06] in your project.

[62:07] >> No, it's this.

[62:08] No matches found.

[62:09] Let me -- >> Yeah, that was just because you didn't

[62:38] blow it by your node modules at the same time, which I didn't realize you didn't do.

[62:44] I would have said to do so.

[62:46] >> Yeah.

[62:47] Huh.

[62:48] Okay.

[62:49] >> It was just confused, because pnpm and npm handle node modules differently.

[62:58] >> Yeah, yeah.

[62:59] I know pnpm likes symlinks, which they always work well, so I'm going to create an identity

[63:07] now.

[63:08] And I'm still going to get the same error, but I just wanted to make doubly sure that

[63:12] this is not the issue.

[63:14] >> It might be.

[63:15] Yeah, it's a good point.

[63:21] >> Yeah, this is the step that we were getting weird errors on, Rion, originally when I came

[63:32] back to do stuff, and it took us like -- we kept getting different errors, trying to figure

[63:37] out what the issue was, and then the issue was just always kind of, just try it again

[63:41] later, and that ended up just being what had to be done.

[63:46] It's weird, though, because -- >> Still getting weird.

[63:51] >> It's probably just network is messed up.

[63:53] So let's try this.

[63:54] Go back to your .env and uncomment out the identity ID, and let's see if we can just

[63:59] skip that step and keep going and see what happens.

[64:02] So let's go back to the tutorial and just go to the next step, just going to be retrieving

[64:06] your identity.

[64:07] Yeah, so we get the identity, and guessing this probably works.

[64:31] >> Yeah, wrapping this stuff in just CLI might be super handy.

[64:42] >> Yeah, I agree, actually.

[64:45] That would be the thing to do.

[64:48] I have to imagine there's already some sort of way to interact with Dash with a CLI, but

[64:52] maybe not with a platform.

[65:07] >> Say that again.

[65:08] Anthony?

[65:09] >> Well, he's just saying that we should just have a CLI where you could just run these

[65:14] commands, just have them embedded in the CLI.

[65:17] >> GRPC transport error, unimplemented.

[65:21] This seems slightly different from the one before, I think.

[65:24] >> Well, it still said 12 unimplemented, didn't it?

[65:28] I'm actually trying.

[65:29] >> Yeah, it's the same thing.

[65:30] That one was also GRPC transport error.

[65:32] >> Yeah, I think it's giving us the same error each time, which makes me think it's something

[65:36] with testnet.

[65:37] >> Okay, what version of the test, what version of the SDK are we using?

[65:42] That's something we need to figure out.

[65:44] >> Just package.json.lock.

[65:45] >> Yeah, this will give me the exact version.

[65:49] >> Well, so will the package.json.

[65:52] >> Sure.

[65:53] >> Dev.1.0.

[65:54] Actually.

[65:55] >> Okay.

[65:56] >> That might be the problem.

[65:57] >> That's not the most current one, actually.

[66:02] Blow that away and run the install again.

[66:06] You should be on 15.

[66:09] >> Yeah, I know that testnet is not at the very latest release of the SDK, so I'm not

[66:20] sure, honestly, which SDK is best to use, the latest.

[66:24] >> Well, 15 is working for me today, so we should try 15 and see what happens.

[66:29] >> Okay.

[66:30] >> So, what are we doing, retrieve identities, or what are we doing?

[66:40] >> Yeah, retrieve identities should be the one, yeah.

[66:43] Did you reinstall your node modules, or just, actually, this time, okay, yeah, it should

[66:49] be, that should do it.

[67:05] Same issue.

[67:09] So I'm on this exact version, so PR 18.25.11.

[67:17] >> We don't want to use a PR version.

[67:20] Why did it install a PR version?

[67:22] >> I did 15.

[67:24] >> That's dash setup.

[67:27] That's a dependency of dash, of the dash thing.

[67:34] NPM list, why doesn't it show me everything?

[67:53] >> Yeah, I'm not sure.

[67:54] This is not something I usually do.

[67:57] Okay, see, that's weird.

[67:59] It shouldn't be like that.

[68:01] >> So if I, and dash setup is the name of our project, just a heads up, so.

[68:12] >> Oh, it is?

[68:13] Okay, that's why it's saying dash.

[68:15] Okay, I was confused, I didn't realize that.

[68:18] Thank you.

[68:19] >> So if I do, so now we're on dev 10, maybe it'll actually run.

[68:25] So I have to take the hat off somewhere, so after I took that off, let me see if I'm

[68:32] actually able to retrieve.

[68:37] That went fast, but the server does not implement the method get status, which is different

[68:48] from before.

[68:51] >> What version of the SDK is it using now?

[68:56] >> Dash dev 10.

[68:57] Let me try 15 like Anthony said.

[69:03] >> Yeah, can you get it to install the exact version that Anthony has, was working with?

[69:12] >> Yeah, I have that, that is now 15, same as Anthony.

[69:18] >> Yeah, I'm pretty sure we've already tried this, I think this is just an issue with test

[69:23] net, honestly, I don't think we're going to be able to solve this.

[69:26] >> Let's try 12 before we totally bail on this, and then, because I think the test net

[69:35] is running dev 12 right now, even though the SDK is a little further up to date, they have

[69:41] >> Hey, there you go, it worked.

[69:42] See, I'm telling you, the only reason why is just because we waited, this has nothing

[69:45] to do with anything we've changed at any point in time, all of that was completely unrelated.

[69:50] >> So you're saying it's still using the dev 15 SDK and it worked, but it didn't work before?

[69:57] >> I updated dev 15 just now, this was the first run with dev 15, the previous run was

[70:01] dev 10, and it didn't work.

[70:03] >> Yeah, I think, okay, so I thought we had done dev 15 earlier, maybe we did, maybe we

[70:07] didn't.

[70:08] >> Maybe we didn't.

[70:09] >> Either way.

[70:11] it was downloading some weird PR version, instead of that version.

[70:17] >> Okay.

[70:18] >> Okay, so we're moving.

[70:19] >> We are.

[70:20] >> Moving along.

[70:21] >> So, Anthony, here's the exact thing, it doesn't have the caret in it, so.

[70:27] >> Yeah, the caret is added automatically, because it's set up to install dash at 1.0,

[70:32] so I don't have to specify the version, so it'll just be updated when someone runs it,

[70:36] but I'll have to figure out what to do about that.

[70:40] And we don't even know that that was the issue, because I've been in this space before, where

[70:45] we changed something, thought it fixed it, and then said, hey, this thing is broken,

[70:48] we did this, and they're like, no, that has nothing to do with it, so let's just move

[70:52] on from this step.

[70:53] >> Okay.

[70:54] We'll have to revisit that, Anthony, because I think, yeah, I don't know how the NPM, I

[71:01] don't know in detail how the NPM dev, or not dev, but semantic versioning, like the caret

[71:09] and the tilde, things work with dev branches, but --

[71:13] >> I think I might have an inkling there.

[71:17] The caret gives you the latest version in that minor batch, and p is higher than d,

[71:23] so a dash pr would be probably seen as higher than d.

[71:28] >> So it falls back to alphabetical in that case?

[71:31] >> I think so.

[71:32] That's my hunch.

[71:33] >> Once we get off of dev branches, no, even when we get on to alpha branches, that'll

[71:38] still be an issue.

[71:39] So yeah, I don't know.

[71:41] I don't know.

[71:42] That's something we just need to be aware of, Anthony, when we do this in the future.

[71:46] >> Well aware.

[71:47] Don't worry.

[71:48] Well aware.

[71:49] >> Okay.

[71:50] All right.

[71:51] So let's see if we can get through the next step, and then maybe we'll call it quits then,

[71:56] because I think we're coming up on our time.

[71:58] >> Cool.

[71:59] >> So I will quickly do top-up identities, and okay.

[72:16] >> Rion, do you want to schedule Monarch for a second go-around, where we try and keep

[72:21] going at another time?

[72:23] >> Yeah.

[72:24] That would be great.

[72:25] If Monarch's up for it, we could do a 1B, like I know that you've already numbered the

[72:31] next one as 2.

[72:34] >> I can rewrite that.

[72:35] It's not a big deal.

[72:36] >> Yeah.

[72:37] >> I'd be down.

[72:38] >> Well, it might be a good precedent to set anyway, because the numbers we could have

[72:46] as people trying the thing, and the B, the letters we could have as, you know, potentials.

[72:54] >> Yeah.

[72:55] That makes sense.

[72:56] Yeah.

[72:57] And ideally, after the first couple, hopefully we'll be able to iron out these things for

[73:01] this one, though.

[73:02] I don't know, man.

[73:03] It's probably just a luck of the draw to a certain extent.

[73:07] That's why we need to have fallbacks for when things don't work, so that's why having the

[73:12] extra keys was good to have.

[73:15] So anyway.

[73:17] >> So question, and maybe this is how people start getting involved in DASH, with, like,

[73:27] all of this work that Anthony's doing is really great work.

[73:30] I am nowhere as good at writing documentation as Anthony, but if I wanted to get involved

[73:35] and write code, then that might be a fun side thing for me to do from time to time, like

[73:41] how would I get involved?

[73:42] >> Yep.

[73:43] That's an awesome question.

[73:44] You're at the right place.

[73:47] That would be me.

[73:49] So me and Anthony, we can get you involved in other projects as well.

[73:55] When needs come up, like, for example, today, we came across the problem where there was

[74:00] a bad test net, right, and this is an issue that's come up several times before, so solving

[74:06] that might be as simple as creating a simple application that is a more reliable faucet.

[74:14] And so that's just a small example of something that we could put you on and then task you

[74:19] to work on, if that's something you're interested in.

[74:22] So there are a lot of different things that we could have you work on.

[74:26] >> That would really get you in the guts of the blockchain, too, and you would come away

[74:30] a changed man.

[74:32] >> Yep.

[74:33] So, yeah, we'll talk offline about that.

[74:38] There's lots to do, for sure.

[74:39] >> Cool.

[74:40] >> Yeah, we should probably start wrapping up here for about at our time that we said

[74:46] we were going to finish.

[74:47] And if we're going to do another one anyway, we don't need to worry about getting through

[74:51] as much of this as possible.

[74:52] This is probably a good natural stopping point.

[74:54] >> Yeah.

[74:55] Let's just bring it back a little bit high level to end.

[75:00] The high level of this is, again, we have a network that has nodes running, and those

[75:09] nodes that are running on this network, right now we're working with test net.

[75:14] And test net is a network that's essentially created by Dash core group, and they own and

[75:21] run all the servers, right?

[75:23] So they spin up a whole cluster of servers, nodes that are running the Dash blockchain

[75:28] and Dash platform, and one of the features of those, of that, of Dash platform specifically,

[75:36] is that you can store data on this network.

[75:39] So you can think of it as kind of like cloud storage, where you don't have to actually

[75:44] set up an account to work with this.

[75:47] All you have to do is pay the money.

[75:49] And right now, with test net, it's not even money.

[75:52] It's like fake magic internet money that you get for free, in theory, from faucets.

[75:59] But when it's on main net, you would pay, let's say, like 30 cents to store a certain

[76:06] amount of data that your application needs for global state management, for example.

[76:14] And that would be, that's the whole purpose here.

[76:17] So we ran into several issues.

[76:20] You have a wallet with an address, and then you need to create an identity, which gives

[76:25] you another ID.

[76:26] The identity is then what you use to create the document.

[76:30] You then use the document to write a note.

[76:33] Not confusing at all.

[76:34] No, not at all.

[76:35] I got all of that.

[76:36] Yeah.

[76:37] And when you compare it, though, there are some issues that we obviously need to work

[76:41] out in terms of developer experience.

[76:44] But at the end of the day, what's supposed to be the happy path is that you spin up,

[76:55] you put this SDK into your application.

[76:58] And then the SDK, it takes a little while to get to know the API and whatnot for the

[77:06] SDK.

[77:07] But after you do that, you basically have access to a database, a cloud database, that

[77:14] you don't even have to register for.

[77:16] So in theory, it's supposed to make the developer experience for creating an application that

[77:23] needs global state management a lot easier, because now you don't have to set up a server.

[77:29] You also don't have to set up a database.

[77:31] You just use SDK.

[77:32] Yeah.

[77:33] And so, Mark, it's about them being each one-off kind of scripts.

[77:37] As you go, once you have the identity, then you create and edit and manipulate documents

[77:43] and notes and stuff.

[77:44] So you end up kind of implementing a CRUD interface to a certain extent.

[77:49] So it's almost more like an ORM that you're kind of building in one sense.

[77:54] So the, like I said, if you wanted, you can just clone down the Git repo and in its finished

[77:59] form that you'll have all those commands already.

[78:01] And that's kind of why they're separate commands is because they could all be combined into

[78:06] one file, but you still will be running individual commands because they're doing specific composable

[78:11] functionality.

[78:12] Yeah.

[78:13] So it's like a command of commands is what you're describing.

[78:17] It's like building out a CLI is essentially what we're doing here.

[78:22] So what you're saying about this should just be a CLI with commands is like totally on

[78:26] the money.

[78:27] Gotcha.

[78:28] Yeah.

[78:29] Yeah.

[78:30] And if that's what we decide is the best way to introduce developers to this, then that's

[78:35] something that we could build.

[78:36] And I know how to do that now.

[78:38] I know how to build a node CLI because I did it already now, which I did not know how to

[78:41] do the first time I started doing all this Dash stuff.

[78:44] Heck yeah.

[78:45] Yeah.

[78:46] And then those developer tools that we looked at when we were going down the sidetrack,

[78:54] we actually do have CLIs for all of those tools.

[78:56] So we have both SDKs and CLIs.

[78:59] Yeah.

[79:00] I was going to say, there has to be already, there is Dash CLI that lets you interact directly

[79:04] with the RPC stuff.

[79:05] Yeah.

[79:06] There's a lot of different CLIs and things, but yeah, we have to figure out what the best

[79:16] DX is for just the introduction to developers.

[79:20] So yeah, we'll talk about that.

[79:21] I think maybe the best next step would be schedule another stream to go through this

[79:29] again and then just talk offline about what other things that we can get you working on.

[79:36] So thanks for your time, Monarch.

[79:39] And thanks for helping us.

[79:40] Do you have any closing thoughts, Monarch, so far?

[79:43] It's kind of hard to tell.

[79:47] So let's have your hot takes so far.

[79:50] On a scale of one to 10, how much do you hate cryptocurrency?

[79:55] Just kidding.

[79:58] I really love the tutorial because there's a lot of potential.

[80:02] I think what it's giving me is that hands-on, it's hands-on, but it's also theoretical.

[80:09] So it's teaching me as I go, and I'm really learning a lot as I'm going through it.

[80:15] That's the goal.

[80:16] That's the difference between a tutorial and a how-to.

[80:22] So you have, this is a thing with Diataxis, it's like this docs thing where they have,

[80:28] these four things they have, there's tutorials, how-to's, explainers, I think, and then, oh,

[80:37] this is a third one, but anyway, there's like, a how-to tells you how to do something specifically,

[80:42] like I need to know how to do this, whereas a tutorial is actually teaching you concepts

[80:47] as you're doing it.

[80:48] So that's kind of the idea.

[80:49] So what you're saying is, what was the point?

[80:50] Yeah.

[80:51] Yeah.

[80:52] I'm the kind of person who knows when to gloss over a paragraph.

[80:57] So I'll just go read, and if something catches my eye and I want to learn more, then I'll

[81:03] read more.

[81:04] And if I want to learn more afterwards, then I'll just do the tutorial, and then I'll get

[81:08] it working, and then I'll sleep on it and come back the next day and go back to the

[81:12] tutorial and read more.

[81:14] So this is really great.

[81:15] I think the part that I am not a big fan of, the glitches, I mean, it is what it is, but

[81:21] the glitches are painful.

[81:24] Maybe one way to get around it is, like, warning labels or, you know, inside the tutorial itself

[81:30] saying this step is glitchy, and just be transparent about that.

[81:35] And that might be one way to sort of mitigate the frustration or...

[81:39] It's really less frustration and more question marks going, "Hey, did I do something wrong?"

[81:44] Or "Is it my fault, or is it Dash APIs, or what's going on?"

[81:49] So that might be something that could be useful.

[81:53] Other than that, I think this is definitely a fun experience, and it's getting me curious

[81:59] about crypto, which I never thought I would be, so yeah.

[82:02] Well, I think Rion accomplished his goal, then.

[82:06] Yeah, yeah, several goals, for sure.

[82:10] Yep, let's chat offline, and then we'll figure out what the next step is.

[82:14] Awesome.

[82:15] Awesome, man.

[82:16] Thanks so much for doing this, Monarch, and we'll catch all you guys next time.