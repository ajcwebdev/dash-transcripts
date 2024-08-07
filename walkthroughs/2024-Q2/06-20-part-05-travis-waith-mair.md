---
showLink: "https://www.youtube.com/watch?v=0M4wdG4atBk"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Platform Walkthroughs Part 5 with Travis Waith-Mair"
publishDate: "2024-06-20"
coverImage: "https://i.ytimg.com/vi/0M4wdG4atBk/sddefault.jpg?v=66731b61"
---

## Episode Description

Travis Waithmayer learns to create identities, contracts, and documents on Dash Platform, overcoming network issues to build a simple blockchain application.

## Episode Summary

In this episode, Travis Waithmayer, a developer new to cryptocurrency, walks through creating a basic application on Dash Platform. The hosts guide Travis through setting up a wallet, registering an identity and name, creating data contracts, and submitting documents to the blockchain. They encounter and resolve some network connectivity issues along the way. The walkthrough demonstrates how Dash Platform's SDK abstracts away much of the blockchain complexity, allowing developers to interact with it using familiar CRUD operations. By the end, Travis successfully deploys a simple React frontend that displays data from the blockchain. The hosts also discuss Dash's approach to usernames, privacy, and decentralized data storage.

## Chapters

00:00 - Introduction and Network Issues

The hosts introduce Travis and discuss network issues encountered in the previous episode, explaining the need for better node selection in the SDK.

05:20 - Setting Up the Project

Travis begins setting up the project, following the tutorial to create a wallet and connect to the Dash testnet. The hosts explain the concept of mnemonics and their role in generating key pairs.

18:33 - Creating an Identity and Name

Travis creates a Dash identity and registers the name "Wolverine". The hosts explain the importance of usernames for privacy and usability in cryptocurrency transactions.

44:35 - Understanding Data Contracts

The concept of data contracts is introduced as a way to store application data on the Dash blockchain. Travis creates and updates a data contract.

59:08 - Submitting and Retrieving Documents

Travis submits a document to the blockchain and retrieves it, demonstrating basic CRUD operations using the Dash Platform SDK.

67:14 - Building a Frontend Application

In the final section, Travis sets up a simple React frontend application that displays data from the Dash blockchain, completing the end-to-end demo of building on Dash Platform.

73:00 - Conclusion

The hosts wrap up the episode, discussing the ease of use of the Dash Platform SDK and its potential for blockchain application development.

## Transcript

[00:00] All right, we're live with episode 5 of Dash Platform Walkthroughs with Travis Waithmayer.

[00:11] What's up, Travis?

[00:12] >> What's up?

[00:13] How's it going?

[00:14] >> I'm good, man.

[00:15] Good to have you, old buddy of mine, as all these people have been.

[00:22] >> Except for yesterday.

[00:23] >> Yeah.

[00:24] Yes, yes.

[00:25] >> Speaking of yesterday, so good to meet you, by the way, Travis.

[00:29] I'm looking forward to getting to know you a little bit better.

[00:32] Before that, I wanted to talk a little bit about yesterday's stream, so we ran into some

[00:38] network issues, which are a combination of network issues and SDK issues.

[00:46] The issue, I believe, from what I can tell, we had two different issues, and I think they

[00:52] may have both been separate issues, but dealing with the same problem, the same fundamental

[00:57] problem, which is when you're dealing with a network of different nodes, especially in

[01:05] like a permissionless context, sometimes nodes are not operating well, and sometimes nodes

[01:13] may even be operating maliciously, and you need a way for your SDK to kind of drop nodes

[01:23] that are not working for you and find newer nodes, so there is a way to do that, so we're

[01:28] going to go the first thing that we'll probably do is look into that option on how to connect

[01:34] to a specific node, or at least how to not connect to the bad nodes that you know of

[01:40] on the network.

[01:41] Again, this should be probably handled automatically by the SDK, but apparently it's not at this

[01:46] point yet.

[01:50] But first, before we do any of that, let's get to know Travis a little bit.

[01:54] Where did you come from?

[01:55] Where did you go?

[01:56] Where did I go?

[01:57] Where did I go from Sunny Joe?

[01:58] Sorry.

[01:59] That's exactly what I was about to say.

[02:00] Sorry, I can't help it.

[02:07] I am a sarcastic person, which is why Anthony and I get along so well.

[02:12] True.

[02:13] But yeah, I'm just a dev that's been out there hanging out for in the world five or

[02:23] six years now, might be closer to seven.

[02:27] And after three or four years, you start counting how many years you've been working.

[02:31] But yeah, kind of like Anthony, I'm a second career dev switched over from the world of

[02:38] finance a few years back, then primarily, I'm a full time developer, but I've really

[02:45] been like, I really where I enjoy myself hasn't been in the front end all my life.

[02:50] I have a library, a layout library called Bedrock Layouts, and that's probably the biggest

[02:56] thing I've known for out there.

[02:57] Okay.

[02:58] But yeah.

[02:59] Very cool.

[03:00] So crypto is definitely the intersection of tech and finance.

[03:05] So you should feel at home here, but from what I gathered just from our little pre chat,

[03:12] you don't have much experience with crypto, which is which is good, because we want to

[03:18] test this product out with people who may not be familiar with crypto and just want

[03:23] to develop cool things using underlying technology of blockchains and whatnot.

[03:29] Yeah.

[03:30] Yeah.

[03:31] All right.

[03:33] And then one more disclaimer.

[03:34] So the purpose of this of this series, altogether, these walkthroughs is there's multiple reasons,

[03:41] one of which is testing platform itself, testing our documentation, helping me to explain the

[03:50] value proposition of dash and dash platform to all of that.

[03:54] If we run into issues, it's not a big deal.

[03:57] That's just part of the purpose here.

[03:59] So but hopefully we get a little further than yesterday.

[04:03] So with that, I think let's go ahead and do your screen share and go ahead with the Anthony,

[04:11] you've dropped the tutorial link to him.

[04:13] I assume we're not going to look at the graph on a board at all.

[04:18] We will.

[04:19] We will.

[04:20] But probably later.

[04:21] Yeah.

[04:22] We'll look we'll look at that later.

[04:23] So let's look at the tutorial itself.

[04:25] Yeah.

[04:26] And then go to a jcwebdev.com.

[04:33] And then go to blogs.

[04:34] And I'll be the first one.

[04:36] And bump your font way up.

[04:40] No.

[04:41] We already.

[04:42] Oops.

[04:43] 200 was good.

[04:44] Right.

[04:45] That looks good.

[04:46] Yeah.

[04:47] And then start at the setup and configure node project.

[04:48] Yeah.

[04:49] There you go.

[04:50] And then we'll go to blogs.

[04:51] And then we'll go to blog.

[04:52] And then we'll go to blog.

[04:53] And then we'll go to blog.

[04:54] And then we'll go to blog.

[04:55] And then we'll go to blog.

[04:56] And then we'll go to blog.

[04:57] And then we'll go to blog.

[04:58] And then we'll go to blog.

[04:59] And then we'll go to blog.

[05:00] And then we'll go to blog.

[05:01] And then we'll go to blog.

[05:02] And then we'll go to blog.

[05:03] And then we'll go to blog.

[05:04] And then we'll go to blog.

[05:05] And then we'll go to blog.

[05:06] And then we'll go to blog.

[05:07] And then we'll go to blog.

[05:08] And then we'll go to blog.

[05:09] And then we'll go to blog.

[05:10] And then we'll go to blog.

[05:11] And then we'll go to blog.

[05:12] And then we'll go to blog.

[05:13] And then we'll go to blog.

[05:14] And then we'll go to blog.

[05:15] And then we'll go to blog.

[05:16] And then we'll go to blog.

[05:17] And then we'll go to blog.

[05:18] And then we'll go to blog.

[05:19] And then we'll go to blog.

[05:20] And then we'll go to blog.

[05:21] And then we'll go to blog.

[05:22] And then we'll go to blog.

[05:23] And then we'll go to blog.

[05:24] And then we'll go to blog.

[05:25] And then we'll go to blog.

[05:26] And then we'll go to blog.

[05:27] And then we'll go to blog.

[05:28] And then we'll go to blog.

[05:29] And then we'll go to blog.

[05:30] And then we'll go to blog.

[05:31] And then we'll go to blog.

[05:32] And then we'll go to blog.

[05:33] And then we'll go to blog.

[05:34] And then we'll go to blog.

[05:35] And then we'll go to blog.

[05:36] And then we'll go to blog.

[05:37] And then we'll go to blog.

[05:38] And then we'll go to blog.

[05:40] And then we'll go to blog.

[05:41] And then we'll go to blog.

[05:42] And then we'll go to blog.

[05:43] And then we'll go to blog.

[05:44] And then we'll go to blog.

[05:45] And then we'll go to blog.

[05:46] And then we'll go to blog.

[05:47] And then we'll go to blog.

[05:48] And then we'll go to blog.

[05:49] And then we'll go to blog.

[05:50] And then we'll go to blog.

[05:51] And then we'll go to blog.

[05:52] And then we'll go to blog.

[05:53] And then we'll go to blog.

[05:54] And then we'll go to blog.

[05:55] And then we'll go to blog.

[05:56] And then we'll go to blog.

[05:57] And then we'll go to blog.

[05:58] And then we'll go to blog.

[05:59] And then we'll go to blog.

[06:00] And then we'll go to blog.

[06:01] And then we'll go to blog.

[06:02] And then we'll go to blog.

[06:03] And then we'll go to blog.

[06:04] And then we'll go to blog.

[06:05] And then we'll go to blog.

[06:06] And then we'll go to blog.

[06:07] And then we'll go to blog.

[06:08] And then we'll go to blog.

[06:09] And then we'll go to blog.

[06:10] And then we'll go to blog.

[06:11] And then we'll go to blog.

[06:12] And then we'll go to blog.

[06:13] And then we'll go to blog.

[06:14] And then we'll go to blog.

[06:15] And then we'll go to blog.

[06:16] And then we'll go to blog.

[06:17] And then we'll go to blog.

[06:18] And then we'll go to blog.

[06:19] And then we'll go to blog.

[06:20] And then we'll go to blog.

[06:21] And then we'll go to blog.

[06:22] And then we'll go to blog.

[06:23] And then we'll go to blog.

[06:24] And then we'll go to blog.

[06:25] And then we'll go to blog.

[06:26] And then we'll go to blog.

[06:27] And then we'll go to blog.

[06:28] And then we'll go to blog.

[06:29] And then we'll go to blog.

[06:30] And then we'll go to blog.

[06:31] And then we'll go to blog.

[06:32] And then we'll go to blog.

[06:33] And then we'll go to blog.

[06:34] And then we'll go to blog.

[06:35] And then we'll go to blog.

[06:36] And then we'll go to blog.

[06:37] And then we'll go to blog.

[06:38] And then we'll go to blog.

[06:39] And then we'll go to blog.

[06:40] And then we'll go to blog.

[06:41] And then we'll go to blog.

[06:42] And then we'll go to blog.

[06:43] And then we'll go to blog.

[06:44] And then we'll go to blog.

[06:46] Yeah.

[06:47] For context, I think they announced, they first announced platform around the same time

[06:52] React announced suspense.

[06:55] Oh, really?

[06:57] Yeah.

[06:58] Yeah.

[06:59] It was, it was, it was mostly an idea, um, in the making, but you know, scope creep and

[07:05] all that, um, trying to get, there are specific reasons for the delay, but, um, yeah, mostly

[07:12] around broadening the scope and changing the infrastructure.

[07:17] So initially, uh, the backend was developed in JavaScript, uh, and we've moved over to

[07:22] rust.

[07:23] So.

[07:24] Hmm.

[07:25] Yep.

[07:26] Which makes sense.

[07:27] JavaScript is good to like hurry and get out there, but then rust allows you to then solidify

[07:32] it in a more stable way.

[07:34] So yeah.

[07:35] Yep.

[07:36] Yeah.

[07:37] Yeah.

[07:38] So let's, uh, let's see, well, what do we have here?

[07:41] While you're talking, I went ahead and did all this and now I'm onto this.

[07:48] Let's add some information to the getting nor here.

[07:52] Maybe.

[07:53] Oh, and by the way, um, feel free to, to just go ahead and, and, and do your thing, Travis.

[07:59] Um, we will help if you have questions, but go ahead with the tutorial.

[08:03] In the meantime, as you're, as you're doing that, I'm going to answer this question, um,

[08:08] which digital nomad, John says, does someone have to have a masternode to submit a proposal?

[08:16] I'm newer to dash.

[08:17] Uh, the answer to that is no, uh, you do not have to have a masternode to submit a proposal.

[08:22] Anybody can submit a proposal.

[08:24] Um, all you have to do is have, you have to have one dash, which is about $24 right now.

[08:33] And so you pay that one dash to submit a proposal and you can ask for any amount of dash in

[08:38] return for your proposal.

[08:40] Um, and if the, if the stakeholders in dash, uh, which are masternode operators, as you

[08:48] already know, uh, if they want to support that proposal, then they'll vote for you.

[08:55] You have to have a certain amount of votes, 10 net, 10% of all the masternodes.

[09:00] So yes, votes minus no votes, greater than 10% of all the masternodes is the passing

[09:05] criteria.

[09:06] You're popular, Travis, a huge audience here.

[09:10] I bring in the crowds.

[09:11] What can I say?

[09:12] Yeah, it is now to be honest, this is going to be like, you've seen nacho Libre, right?

[09:20] Or like, it was one of my friends in college.

[09:22] It's her all time favorite movie, literally.

[09:25] Well, I mean, I'm wearing the right show.

[09:28] It's nacho and it's, I'm going to be the Jack Black of this.

[09:32] I'm going to be like really super excited and embarrassing the entire way.

[09:37] So

[09:38] we've done all this and just making sure that all it's worked and we want the test

[10:01] environment.

[10:02] Yep.

[10:03] Network.

[10:04] Testnet.

[10:05] Okay.

[10:06] Sweet.

[10:07] I'm going to build this client.

[10:11] I like it when I don't have to write things.

[10:13] I really appreciate this copy, this, all this code.

[10:17] Oh yeah.

[10:20] Copy pastable.

[10:21] That is the name of the game.

[10:22] This is a, for my library, my code library, Anthony, I put him down as one of the, what's

[10:32] it called?

[10:33] Contributors.

[10:34] Contributors.

[10:35] Yeah.

[10:36] And even though he hasn't written any code, he helped like improve my doc site immensely.

[10:41] So that's why he gets to be down as a contributor.

[10:43] Yeah.

[10:44] It's usually the first thing I do is I go read the read me and see where it's broken.

[10:52] Oh, come on prettier.

[10:56] But does money grow on bits?

[10:58] Oops.

[10:59] What is going on here?

[11:02] Okay.

[11:03] This code is causing, creating problems for me.

[11:07] There we go.

[11:09] Okay.

[11:10] So pulling in the network.

[11:14] I just want to see what we're actually doing here.

[11:15] We're creating a new client on this network.

[11:21] Testnet.

[11:22] Okay.

[11:23] And.

[11:24] Okay.

[11:25] I'm going to ask you guys, what does mnemonic mean for this wallet?

[11:33] The mnemonic, which is a terrible name, which I hope we can change in the SDK is just a

[11:40] 12 word seed phrase.

[11:43] It's a, it's a, it's essentially a random, a random number encoded in words instead of

[11:51] encoded in some other encoding mechanism, mechanism like hexadecimal or binary or whatever.

[11:57] It's encoded using a, how big is the dictionary?

[12:02] I don't remember.

[12:03] It's so, so many thousand words, a dictionary.

[12:08] And it, when you have 12 words amongst those, that huge dictionary of options, it gives

[12:14] you a lot of entropy or randomness.

[12:18] So it's a very, very random number that is, and then the mnemonic is used to generate

[12:23] your public private key pairs.

[12:25] Oh, okay.

[12:26] That makes sense.

[12:27] So you would definitely not have Johnny there on main net.

[12:32] If you had funds on this, like you wouldn't want to share your mnemonic.

[12:35] That's the one thing that you want to keep very close to the vest and not let anybody

[12:40] know or even have online.

[12:42] Have you seen Johnny mnemonic, Ryan?

[12:45] Unfortunately, yes.

[12:47] My kids have shown me bad movie.

[12:52] Oh my God.

[12:53] It's with the electric whip, right?

[12:55] Yeah.

[12:56] Movies that are so bad that they eventually kind of cross back over to the threshold and

[13:00] become good again in their own way.

[13:02] I kind of, it's like right there.

[13:04] It doesn't quite make it where you're like, this is so bad.

[13:08] It's good.

[13:09] But like, it's really close.

[13:11] It's kind of like, you know, like the, uh, like Anthony would appreciate it.

[13:15] Like the scale, you have your octave and eventually it starts over again.

[13:18] That's where it is.

[13:19] We're, we're, we're at like the 12th note of the octave and then we're whatever we're

[13:24] of the chromatic scale and we're about to go back again.

[13:26] Anyway, actually, now that you say that, I don't know if I've seen that now that I think

[13:31] I was thinking of a different reference, but anyway, let's get to the create the wallet.

[13:38] Once we do the next couple of steps, we'll know whether this is going to be a hard stream

[13:43] or an easy stream.

[13:44] So yeah.

[13:45] Yeah.

[13:46] Yeah.

[13:47] Appreciate you letting me ask random questions here.

[13:50] Yeah, you're good now, but I really appreciate the, like, we're even going to create the

[14:01] file so we can make sure you're creating the right file with the right name kind of things.

[14:06] Instead of saying, just create a script that create wallet.js.

[14:10] I think this is a good touch.

[14:11] Yeah.

[14:12] It's one of the things that bothers me most about a lot of tutorials or docs or things

[14:18] or like have certain things just written and it's like, but I don't want to read I'm illiterate.

[14:26] Well, and we could, we could literally just have a web app already written and have you

[14:32] click buttons and things, but what, what would that, what good would that do?

[14:36] We want you to start from scratch and so that, you know, exactly like you really didn't have

[14:40] to do that much to get some, something working on, on the dash platform, but we'll see.

[14:47] We're coming up to the step where we're going to have the moment of truth here.

[14:50] Yeah.

[14:51] Not that this will be the next one.

[14:53] This one always works.

[14:54] You can always create a wallet no matter how messed up the testnet is.

[14:58] Right.

[14:59] Because that has nothing to do with the network.

[15:00] That's all client side stuff.

[15:02] So the SDK is doing client side work to create your wallet.

[15:06] That's one of the beauties of blockchain technology, by the way, since, since you're new, I'll

[15:10] just go ahead and mention that, that like when you create a blockchain wallet, you're

[15:17] not asking for anybody's permission.

[15:20] You just following a protocol.

[15:24] And now you have an account, so to speak, on a blockchain.

[15:29] And so you're at that output and put it in your dot EMV and that's what you're going

[15:34] to do throughout the tutorial.

[15:35] Anytime it spits out environment variables for you.

[15:39] And then let's just make sure, yeah, it looks like he got it all in there.

[15:47] And then now we, I get you some testnet funds, sweet.

[15:58] So click that link to the testnet faucet.

[16:02] Where is it?

[16:05] Sorry.

[16:06] Oh, right.

[16:07] Right in front of my face.

[16:10] All good.

[16:11] And then you'll be using the wallet address, which is the random characters, not the new

[16:16] monic and for promo code, right.

[16:22] Master node, one word, lowercase.

[16:28] Yep.

[16:32] So as a heads up, I appreciate this aesthetic, the faucet.

[16:35] Okay.

[16:36] I do like the falling dash.

[16:37] It is nice.

[16:38] It's unfortunate.

[16:39] The site is so terrible.

[16:40] Otherwise.

[16:41] Did I?

[16:42] Oh, it's.

[16:43] It is.

[16:44] It is funny.

[16:45] Yeah.

[16:46] Just let it, let it do its thing.

[16:47] I would say 50% of the time it crashes and that means it works.

[16:54] And then like 10% of the time it will work and we'll give you a message saying it works.

[16:58] And then like 40% of the time you just have no idea what happened.

[17:02] So Travis, if you could paste your, your dash address that starts with a Y into our chat,

[17:11] I'm going to check alongside you, someone's asking about if there's going to be a library

[17:16] like the web three library.

[17:19] This is the dash library right now.

[17:22] We're teaching Travis.

[17:24] So you're seeing it in action.

[17:26] Yeah.

[17:27] And on NPM it's, it's the, the word dash D A S H that's the JavaScript SDK that yeah.

[17:35] Nope.

[17:36] No Python yet.

[17:37] Probably won't be for a very, very long time, but yeah, JavaScript.

[17:41] The way that it seems to be playing out is dash core group is building a rust SDK as

[17:47] well.

[17:48] And I think that that's probably what they'll focus on using for any language except for

[17:55] JavaScript.

[17:56] If we're going to get the JavaScript, so it'll be WASM based technically you probably could,

[18:04] you can use that in job JavaScript environments as well, but I think that people deserve at

[18:10] least JavaScript deserves its own SDK.

[18:13] Yeah.

[18:14] I built stuff with a WASM SDK backed on the JavaScript and it's fun.

[18:21] It's not, it's not hard, but it's also not like user friendly cause you're like, you

[18:26] have to go point it to the right file.

[18:28] Anyway, it was, it's always interesting.

[18:30] Yeah.

[18:31] Anyway.

[18:32] Okay.

[18:33] So yeah, out of the phones, you can check this as a company with a dashboard explorer.

[18:43] Yeah.

[18:44] So you'll search your address at the very top and that's the, uh, this Y address.

[18:49] Oh, okay.

[18:50] We got a transaction.

[18:53] It says, it says zero dash for the summary, but it shows the transaction.

[18:58] Okay.

[18:59] Good.

[19:00] But we can move ahead then.

[19:05] Yep.

[19:06] This fee.

[19:07] What's up with that?

[19:08] I'm just kidding.

[19:09] Come on.

[19:10] It's all monopoly money right now.

[19:11] Yeah.

[19:12] And I still got a fee on my monopoly money.

[19:13] I'm just, yeah.

[19:14] Oh, let's get back.

[19:15] Yep.

[19:16] There you go.

[19:17] Perfect.

[19:18] All right.

[19:19] So now we're going to create the identity on the transactionally really cool stuff.

[19:33] Thanks man.

[19:34] Okay.

[19:35] Oops.

[19:36] I should have, do I still need to go back to the dashboard?

[19:40] Skip all this.

[19:41] Skip all this.

[19:42] Okay.

[19:43] Perfect.

[19:44] Just go to the, create the wallet or update your client first.

[19:45] So now that you have the mnemonic, you got to put it in your client.

[19:49] Yeah.

[19:50] Okay.

[19:51] Yeah.

[19:52] Just, just go to client.

[19:53] Oh yeah.

[19:54] Yeah.

[19:55] Don't make my, don't make this complicated.

[19:56] Unsafe options.

[19:57] I love a good unsafe options.

[19:58] Yeah.

[19:59] That's, that's kind of a technical thing because the blockchain is massive and long.

[20:15] You want to only have to sync like the last couple of blocks.

[20:18] Yeah.

[20:19] That makes sense.

[20:20] Yeah.

[20:21] Okay.

[20:22] Let's create an identity.

[20:26] Dun, dun, dun.

[20:30] Can it be Wolverine?

[20:32] Probably.

[20:33] The identity will be an ID, but your name can be whatever you want.

[20:42] Even Wolverine.

[20:43] Even Wolverine.

[20:44] Okay.

[20:45] So we're going to client, perform identities, register.

[20:50] Okay.

[20:51] Awesome.

[20:52] Okay.

[20:53] Then we're going to create the identity.

[21:00] So let's run this thing.

[21:01] Yeah.

[21:02] This will take 15 to 20 seconds and may or may not work.

[21:05] This is, this is the step where you find out whether the test net network gods have shined

[21:11] upon us or not.

[21:15] So what, what the SDK is doing under the hood here is it's, it's contacting the blockchain

[21:21] and finding the list of master, the list of Evo nodes, evolution nodes that perform the

[21:29] services for, for the platform.

[21:34] And it's connecting to a random one.

[21:36] And sometimes you connect to a random one that is not healthy.

[21:41] And sometimes you connect to a random one that is.

[21:44] And sometimes, so who, who can we, who can we talk to about having this fixed within

[21:51] the library itself so that it can do the retries and actually find a working node?

[21:55] Because this is like, this has been a huge sticking point.

[21:58] This is like tanked more than half of the walkthroughs we've done.

[22:02] It's like, this is clearly something that we need to figure out who we can talk to to

[22:04] fix this.

[22:06] Yeah.

[22:07] That's a conversation that I'll have with, with Dash Core Group, because I think it's

[22:12] a bigger conversation.

[22:15] They I'm not sure if even if it's putting in a better error message to say, Hey, you

[22:20] need to connect to a different node and explain how to do that.

[22:23] Like even, even it doesn't necessarily, I know, I know.

[22:27] Yeah.

[22:28] They're just, they don't have any bandwidth to, to, to help with the SDK it seems like

[22:32] right now.

[22:33] So I mean, obviously we can, we can help do some, some things if we really wanted to,

[22:39] but yeah.

[22:40] So this is what we're talking about.

[22:41] This is what happened yesterday.

[22:42] Certificate expired.

[22:43] So you just keep trying and they'll keep working, eventually working.

[22:47] So let's try the let's try, I'm going to the Dash Discord.

[22:55] We ran into this before Dev Talk.

[22:59] There's an option that you can allow different, allow, allow self-signed certificate.

[23:08] So let's find the documentation, by the way, you guys go to, go to docs.dash.org and let's,

[23:20] let's get those docs up so that we can, we can look at them.

[23:24] Okay.

[23:25] Are we looking for like self-signed certificate?

[23:32] So you want to go, no, no, so just go to, on the left, you're going to want to go connect

[23:37] to a network under tutorials to go to platform docs.

[23:41] Actually.

[23:42] So at the, yeah, just any of those.

[23:47] Yeah.

[23:48] Tutorial.

[23:49] There we go.

[23:50] And then connect to a network.

[23:51] Sweet.

[23:52] Can you bump up the font?

[23:55] Oh yeah.

[23:56] I think you connect via address is what you want.

[24:00] So we want, ideally we want to find a place that shows all of the, all of the, the client

[24:07] options.

[24:08] You see that object where it says network testnet.

[24:11] That's the client options object.

[24:16] And I want to see somewhere in the documentation that has all of the options available.

[24:22] And I, I saw a link to SDK documentation a little bit above.

[24:28] So maybe that's where we can go.

[24:32] Now it's down.

[24:34] Before you do that though, scroll down to connect via address, let's keep going.

[24:40] Connect via address.

[24:41] So look at, look at this, Ryan.

[24:42] So this is showing you the IP addresses.

[24:45] Yep.

[24:46] Yeah.

[24:47] That's yep.

[24:48] Yeah.

[24:49] I was just curious.

[24:51] I was just curious if the, if the documentation has a very clear place where it shows all

[24:56] the options instead of just examples.

[24:59] Cause I want to know.

[25:00] Yeah.

[25:01] I'm not sure.

[25:02] I feel like these examples probably are all the options.

[25:05] Scroll up a bit, Travis.

[25:09] Keep going.

[25:10] Cause that link to the, the JavaScript.

[25:14] Once this returns successfully, you're ready to begin developing.

[25:17] See the quick start for recommended next steps for details on all SDK options and methods.

[25:22] Please refer to the SDK document documentation.

[25:26] Get best block hash, is that what.

[25:29] So click that link that says SDA SDK documentation, open it in a new tab or whatever.

[25:47] Keep going down.

[25:48] Oh, that was, I was at the bottom.

[25:51] Oh, let's see.

[25:53] Usage examples.

[25:56] Okay.

[25:59] I'm looking for a reference, a reference document, not usage examples, but I don't know.

[26:06] We'll just keep going.

[26:09] We have the examples there to both disallow.

[26:13] Let's see.

[26:17] Where did you find that Anthony?

[26:18] Was it, was it down a little further now?

[26:20] Yeah.

[26:21] Okay.

[26:22] By address.

[26:23] So we're not, we're not doing whatever.

[26:25] We're not doing the disallow.

[26:26] This would just be, cause you said you gave me a specific IP address.

[26:29] You're like, this one works.

[26:30] So we would put that in under DAPI address.

[26:33] Yeah.

[26:34] So update your object to say under or just, yeah, under the mnemonic or whatever to say

[26:41] that DAPI addresses copy and paste that if you want, and then we'll actually, yeah, yeah.

[26:48] Just the DAPI address and put it at the very top, I think you're right there.

[26:53] Yeah, that's fine.

[26:54] Yeah.

[26:55] I think we should, do you want to give him the specific IP that you had sent to me?

[27:04] Sure.

[27:05] Okay.

[27:06] I got it.

[27:07] I got it right here.

[27:11] Okay.

[27:12] I just put it in the private chat, which, which you can, you can pull up on screen.

[27:19] Travis, the, the stream yard chat.

[27:21] Oh.

[27:22] You got it.

[27:23] Cool.

[27:24] Great.

[27:25] Okay.

[27:26] So do you want to try it again?

[27:29] Sure.

[27:30] This is the first time I've ever done this.

[27:31] The first time we've ever done this.

[27:33] So we're about to see whether this works or not.

[27:34] I don't know if this one's going to fix this, this issue because this is a cert issue and

[27:41] well we could have fixed it a different way is what I was going to say, but this will

[27:47] probably fix it too.

[27:48] Well, at least hopefully.

[27:49] Yeah.

[27:50] I guess the question is how would someone find, if this does fix it, how would someone

[27:55] know to find this address versus any other?

[27:59] Yeah.

[28:00] I know that Mikhail Shenmik is working on in the, in the platform Explorer site, which

[28:07] we haven't seen yet today, but we'll, we'll open that again or we'll open that today.

[28:13] He's working on a page that lists the validators.

[28:17] So hey, look at that.

[28:19] Go back to your output.

[28:20] Woo hoo.

[28:21] Woo.

[28:22] All right.

[28:23] That's nice.

[28:24] We can continue.

[28:25] Yup.

[28:26] We can go farther.

[28:27] The magic incantation worked.

[28:28] That was pulled out of the ether randomly that no one knows how, why, or where, but

[28:38] it worked.

[28:39] Well, I mean.

[28:41] I'll take all the credit for this one.

[28:42] It is right there in the docs, so I mean, there is that.

[28:46] But that IP address is not in the docs.

[28:49] I had to have special insights to know what that was.

[28:52] So just grab your, actually.

[28:54] So first grab your identity ID and then put that in your .env and then follow that link

[28:59] and we'll show you where.

[29:00] Okay.

[29:01] Identity ID.

[29:02] Oh, right there.

[29:03] Yeah.

[29:04] I should put another line break before it to make it more obvious.

[29:09] What I think would be a good advice here, if you could like throw some chalk colors

[29:14] on these in the output, that would, you know, make it pop out and go, Hey, this is, yeah.

[29:22] That's a good idea.

[29:25] Yeah.

[29:26] I mean, or I could literally just have it right straight to your .env, but I'm going

[29:30] to avoid that.

[29:31] Cause I always thought like writing to someone's .env is a little sketch.

[29:35] Yeah.

[29:36] I agree.

[29:37] Okay.

[29:38] And then follow that link.

[29:41] This is the, this is the, this is the good explorer.

[29:47] Okay.

[29:49] Okay.

[29:51] So I'm here now through the identity and the follow that link.

[30:05] These tab here, Anthony, can you update your site to include that DAPI addresses, the,

[30:20] the tutorial just so we don't have to go looking for it next time.

[30:26] Yes.

[30:27] Okay.

[30:28] So we're going to see my ID in the list.

[30:34] So I'm a GW, oh yeah, I'm right there.

[30:40] Do you ever like see these random hash and try to like sound them out sometime just for

[30:50] the fun of it?

[30:51] Or is that just me?

[30:53] That's just you.

[30:54] Okay.

[30:55] Fair enough.

[30:56] Anyway, fun, fun.

[30:58] Let's see.

[31:00] Okay.

[31:01] Let's create these retrieve identities.

[31:06] Do you want to address anything that's happening in the chat right now?

[31:26] Oh, I haven't been looking at it.

[31:28] Let's see.

[31:29] Let's see what's going on.

[31:30] They're having a lot.

[31:31] I don't know where you found this idiot, but like, don't bring him back on the stream again.

[31:35] That's what they're saying.

[31:36] Right?

[31:37] Oh, that would be nice.

[31:38] No, they're, they're not talking about you at all.

[31:42] That would be good if they would at least talk about you.

[31:51] So let's, let's get our IDs.

[32:09] You can throw one of those CLI gloating spinners.

[32:28] There we go.

[32:32] I got my ID back.

[32:36] Sweet.

[32:39] I'm rich.

[32:40] Look at that.

[32:43] Awesome.

[32:46] Okay.

[32:48] Special transaction transforms, that's Chris Houston, that's perform.

[32:59] One dash is equal to a hundred thousand deaths.

[33:01] Okay.

[33:02] Does this mean after like the Simpsons, Duff beers, I'm just kidding the second person

[33:10] that has the second, uh, there's many people mentioned, uh, Duff is actually, uh, comes

[33:18] from Duff field, which was the founder of Dash creator of Dash that fork it's a fork

[33:25] of Bitcoin.

[33:28] So it was, uh, he named after Duff beard.

[33:32] No, I don't think so.

[33:36] Increase some Dash to credits.

[33:42] Okay.

[33:43] So let's top up.

[34:01] Getting in this, in my two pup identities, maybe you should do a capital U so it doesn't

[34:11] look like two pup.

[34:12] That is true.

[34:13] Yeah.

[34:14] Now we're getting into like over overly, like I don't do code reviews like that.

[34:26] That is the fifth walkthrough.

[34:29] So that's pretty much all we got left to fix now, which is good.

[34:35] Could you just be consistent with your styles or your naming conventions?

[34:39] I'm just going to find something to put back in your code review.

[34:42] Cause I, I feel like I have to, okay, I'm just coming back to the, just coming back

[34:52] to where we are.

[34:54] We are, which are we running in command right now?

[34:58] Yeah.

[34:59] We're running.

[35:00] Okay.

[35:01] Yeah.

[35:02] Oh yeah.

[35:03] There we go.

[35:04] Okay.

[35:05] So we've got a balanced, oh, I just keep getting more rich.

[35:33] Yes.

[35:34] And you don't need to copy paste any of that into your .env.

[35:36] That's just so you can see your balance.

[35:41] Oh, is this where I can now?

[35:59] My name here.

[36:05] So we already decided Wolverine, right?

[36:09] Sure.

[36:10] I bet it's not taken.

[36:14] I've got that in my mind cause not that I'll distract too much, but my kids got this for

[36:19] father's day for me.

[36:21] The old Marvel superheroes role playing game out of print anyway.

[36:29] So I've got Marvel on my brain cause of that.

[36:32] Are you going to open it or are you just going to keep it in the plastic?

[36:38] Oh, I've opened it and I've looked at it and now I'm too scared to play with it cause it's

[36:46] in good condition.

[36:48] Those are hard to find.

[36:51] I might do the copy and print out those spots.

[36:58] I don't know if you can hear my dog barking, I'm sorry.

[37:08] Someone honked down the street and now he's upset.

[37:11] Going back to register name.

[37:33] It's not a live stream unless, you know, something dumb happens in the background of somebody's.

[37:40] Okay, let's run this thing.

[37:48] Really liking this easy to like just copy and go through the tutorial kind of feel it's

[37:55] like it's got the right amount of like, I feel like I'm building it, but I'm not like

[38:01] going to get bored of doing going through this tutorial.

[38:05] That's a hard balance, I think.

[38:08] Yep.

[38:09] Got it.

[38:36] Right there.

[38:37] Oh, I've already got a Wolverine in there.

[38:40] Yeah, it's just letting you see it back.

[38:43] But yeah, let's view it on the blog explorer.

[38:44] It looks like we got her name registered.

[38:47] All right, we want to kind of stop here and give like a little explanation of what's going

[38:56] on here.

[38:57] Ryan.

[38:58] Yeah.

[38:59] Do you want to take a stab at it?

[39:01] Yeah.

[39:02] So you created an identity and then the identity has a name and your name is a little bit like

[39:09] a domain.

[39:10] So now if someone were to want to send you money, like someone's got some Dash, I got

[39:16] some Dash.

[39:17] I'm like, man, I want to give my buddy Travis some Dash.

[39:20] So he will let me know that he is currently hanging out at wolverine.dash and I could

[39:25] use that to send you Dash.

[39:29] Yep.

[39:30] Yeah.

[39:31] So the main thing is there's a couple of things that would help to know why that's important.

[39:40] First of all, when you are using cryptocurrency with either a coin model or an account model,

[39:49] coin model is like what Bitcoin uses, what Dash uses.

[39:53] People call it UTXO, Unspent Transaction Output, but that's unnecessarily complex.

[39:58] It's a coin model.

[40:01] And then there's account models.

[40:03] And either way, if you're using the same address every time, like the same Bitcoin address,

[40:09] same Dash address, same Ethereum address, then people can track you online and see what

[40:15] your activity is.

[40:17] And that's like no good for privacy.

[40:19] So this would not fulfill the use case that Dash is going for.

[40:23] Cash is supposed to be digital cash.

[40:26] And as we all know, cash is private.

[40:28] When I give a $5 bill to Anthony, nobody knows what my transaction history of that $5 bill

[40:37] was or how much other money I have.

[40:42] Because I gave a five doesn't mean anybody should know anything else about that.

[40:46] So you should always be reusing and generating new addresses for every transaction that you

[40:52] make.

[40:54] But doing that then complicates the idea that if you were using the same address for everything

[41:01] and you even had it posted on your social profile or whatever, that would be more convenient

[41:06] because at least you would have a static address and people would know where to pay you.

[41:11] But then you lose out on privacy.

[41:13] So usernames is the idea that, OK, even though we're generating new addresses under the hood,

[41:19] it's all going to a single username.

[41:21] So I can give you the username, Ryan, and then under the hood, it's generating new addresses

[41:29] every time I do a transaction.

[41:32] But from the user level, it's just all I need to know is his username is Ryan.

[41:36] Let me think.

[41:38] Can you have like multiple usernames?

[41:39] Can I register my financial name and my social network name and what like compartmentalize

[41:48] your life?

[41:49] Yes.

[41:50] So people only know you by one identity, but it's all pointing to the same wallet.

[41:56] OK, that's I like that.

[41:58] You can create these identities essentially.

[42:01] So that is the main thing that Dash is trying to distinguish itself from all the others

[42:07] is that we have this user friendly username system that gives you privacy and usability.

[42:16] A lot of username systems like username systems are coming around now.

[42:21] They're becoming more popular, more common in different cryptocurrency projects.

[42:25] But they're typically just mapping an address to a specific username.

[42:31] And that doesn't really help with the privacy aspect.

[42:34] So if it's one layer away from the identity problem, it doesn't help.

[42:42] Yeah.

[42:43] Yeah.

[42:44] So that that's really cool that the current job I work for, I worked for a company called

[42:50] Anonymous Labs, and that was a big thing that we were building was an SDK around people

[42:55] being able to create identities and you could create these like identities where you would

[43:01] have an email, a phone number and even potentially like a Visa card all attached to a single

[43:08] identity.

[43:09] And then you would like kind of like compartmentalize your life around that way.

[43:13] So you're never giving your, your base phone number, your, your real email address to any

[43:19] specific person.

[43:20] Anyway.

[43:21] Very cool.

[43:22] Yep.

[43:23] That's similar.

[43:24] Similar idea.

[43:25] All right.

[43:26] So what are we looking at?

[43:28] We're looking at the platform explorer.

[43:30] Yeah.

[43:31] So we were just looking at, sorry, we were looking at my identity here, the Wolverine.

[43:38] Okay.

[43:39] Sorry.

[43:40] So let's retrieve that name now.

[43:44] Yeah.

[43:45] So your name should be registered on the network now and we should be able to retrieve it.

[43:49] That's what this is saying.

[43:50] Retrieve name.

[43:51] There we go.

[43:52] Okay.

[43:53] I'll be right back.

[43:54] Okay.

[43:55] Oh yeah.

[44:08] Okay.

[44:14] Sweet.

[44:18] Awesome.

[44:22] We're now on to, we're halfway through.

[44:25] Yep.

[44:26] Give or take.

[44:27] A data contract on dashboard forum serves as a blueprint.

[44:33] Yeah.

[44:35] So yeah.

[44:36] Go ahead and read all of this.

[44:37] Cause it's, it's a new idea all together.

[44:45] Okay.

[45:02] So let's create some data contracts.

[45:13] Does this sum it up well?

[45:14] Do you feel the data contracts?

[45:18] Yeah.

[45:19] Yeah.

[45:20] For enough for our purposes here, at least.

[45:24] Yeah.

[45:28] The idea is basically if you want a, if you want data storage for your application, that's

[45:38] what this is serving.

[45:40] So an application might have the need to store data globally instead of just locally in application

[45:48] itself, in memory or in the browser or whatever.

[45:51] You may want to tap into global state storage, either because you want it persistent somewhere

[45:55] off site or because it's an application that's by nature collaborative, like a social network

[46:03] or whatever.

[46:06] And this then gives you the option to store data in the cloud per se on, on the dash blockchain.

[46:15] And further, it gives you all sorts of proofs under the hood that the data was not tampered

[46:23] with and that you know that the only person, for example, the only person that could write

[46:28] to this contract is the one that's allowed to.

[46:31] So you have all those cryptographic guarantees and that's, that can become very important

[46:36] for certain applications where other applications, it might not be as important, but nonetheless,

[46:43] you, you have all that at your disposal if you want it.

[46:47] So is this the schema?

[46:48] Is that what this is here that we're building?

[46:51] Yeah.

[46:52] So the data contract itself is, is, is very much like making a database schema for something

[46:58] like a document database that describes the type of data.

[47:05] And then the documents are what is data that adheres to the schema.

[47:13] So I'm sure some people have asked this before, are, are you guys looking to eventually get

[47:17] like a TypeScript types, at least for, for this, thankfully the first person to ask that,

[47:27] I know Anthony's love of TypeScript.

[47:30] There should be types already in there, I think.

[47:33] There should be types in there.

[47:35] I was just looking, it looks, oh yeah, it looks like there are some JS docs tile things,

[47:44] but anyway.

[47:46] Yeah.

[47:47] So the JavaScript SDK has been a little bit neglected, unfortunately with priority being

[47:53] given to the Rust SDK.

[47:55] So the TypeScript it's supposed to have TypeScript for, for the, everything, but some things

[48:00] are probably missing.

[48:01] Yeah.

[48:02] If the tutorial, the tutorial itself was written in TypeScript, that, that stuff would probably

[48:06] you get the auto-complete and stuff like that.

[48:08] And that's kind of just, oh yeah, yeah, yeah.

[48:11] I was just kind of curious.

[48:28] Is the contract ID, I'm assuming I put that in here, it's still running, oh, was it supposed

[48:56] to come out with some more stuff that I, yeah, you need to make sure this one runs all the

[49:06] way to the end.

[49:07] Oh yeah.

[49:08] Sorry.

[49:09] I was a little.

[49:10] Yeah.

[49:11] No, it's okay.

[49:12] This happened on another stream.

[49:13] A little excited to like be like, oh, I guess we're stuck.

[49:17] Yeah.

[49:18] Cause this is going to...

[49:19] You can copy it into your end file right now if you want, but you won't be able to get

[49:24] any further.

[49:25] Make sure you're going to use the new one you just got.

[49:28] So replace what you have with this one.

[49:30] Good call.

[49:32] Yeah.

[49:33] Cause this is the contract ID that, there you go, there's the rest of it.

[49:39] That actually published it to the chain.

[49:41] Sweet.

[49:42] Review that it's published.

[49:45] Yeah.

[49:46] Identifier, my owner, created.

[49:52] Sweet.

[49:53] Oh, schema.

[49:55] That's good.

[49:57] Okay.

[49:58] Yeah.

[49:59] So you notice there's, there are no documents on that yet, but that's the next step.

[50:16] Created it.

[50:17] Okay.

[50:18] Okay.

[50:19] Here we are.

[50:22] So let's now retrieve our contract.

[50:31] Seeing a pattern here.

[50:33] There's the create and retrieve.

[50:35] Yeah.
[50:36], soon you'll be able to update too.

[50:47] Well, that was fast.

[50:54] Okay.

[50:56] So we got it.

[50:57] Got the schema.

[51:01] Nothing in here yet.

[51:03] Okay.

[51:04] So update.

[51:06] Okay.

[51:07] So we can grab the existing contract.

[51:24] Okay.

[51:26] Okay.

[51:28] Okay.

[51:30] So let's run this.

[51:47] We should get the update here eventually.

[51:58] We're probably going to make it through most of the tutorial at this point.

[52:21] Yeah.

[52:26] If I go back to that one link, when I see that in there, revision two.

[52:35] Yeah.

[52:36] Sweet.

[52:37] I mean, there's no document, but like I can see it's been changed.

[52:40] Yeah.

[52:41] The document is the next step I think.

[52:44] Okay.

[52:45] Okay.

[52:46] Okay.

[52:47] In the apps object to the client options, pass the contract ID.

[52:55] Okay.

[52:57] Where client?

[53:00] Oh, maybe I shouldn't have got rid of it.

[53:12] Oh no.

[53:13] Yeah, that's fine.

[53:14] Okay.

[53:15] Okay.

[53:16] Contract ID.

[53:17] Okay.

[53:18] Okay.

[53:19] Now we're going to submit.

[53:20] Yeah.

[53:21] Here we go.

[53:22] We're going to submit.

[53:23] I don't want to say AJC web tab.

[53:52] This is Travis.

[53:53] Yeah.

[53:54] I've updated the tutorial with a couple of things, but for some reason, CloudFlare has

[54:01] decided that my function is now too large and I need to upgrade to a paid plan.

[54:06] So I'm currently migrating to another plan.

[54:10] Okay.

[54:11] Paid?

[54:12] We don't pay for things.

[54:13] But then even, so that is the need to upgrade.

[54:15] So I tried to upgrade and then it crashed and wouldn't let me do it.

[54:19] So it's like, apparently you don't want my money.

[54:24] It won't even take my money.

[54:27] Oops.

[54:29] Okay.

[54:31] Uh-oh.

[54:33] Did I play around with things too much?

[54:42] What was the, what was the thing you just ran?

[54:46] I ran.

[54:47] Transmit no document.

[54:48] Okay.

[54:49] That's the, that's the same error we were getting yesterday, the empty SPV chain.

[54:55] So we might need to, the, the node we were using might have just crapped out on us.

[55:00] Oh, that's been hit by some guy in Texas over and over again.

[55:09] Just kidding.

[55:12] We need to do a different client.

[55:19] Delete.

[55:20] Oh, I know what happened when you copied you.

[55:23] We lost the Dappy client when we, when we copy paste our new client.

[55:28] Oh, let's go back.

[55:30] Hmm.

[55:31] So, so go back to your client.

[55:33] Yeah.

[55:34] Where did I go?

[55:35] And then copy the apps part.

[55:38] Yeah.

[55:39] I was going to say copy the apps part and then do that.

[55:42] Yeah.

[55:43] Where's the client?

[55:44] Yeah.

[55:45] That, that makes sense.

[55:46] Let's just throw the apps here.

[55:49] Okay.

[55:50] That should work now.

[55:53] And then I'll put it up in your dot ENV.

[56:09] Oh, Travis, as you've been doing this for the last hour, there's been an argument going

[56:28] on in the chat about whether Dash is dead or not.

[56:36] James Doe, yeah, he, he has good comments a lot of times, but he's also kind of a troll

[56:44] other times.

[56:45] Dash is dead.

[56:46] No, it's not.

[56:47] I mean, is that basically what it is?

[56:50] Yeah.

[56:51] When the price is down, that just makes the project dead for some people.

[56:58] And you know, the technology has never been better.

[57:01] Technically it's not an all-time low though, because the price used to be like a dollar.

[57:05] The price is zero for that matter.

[57:10] It's stabilized now, crypto and web 3 and all that is now stabilized because the hype

[57:15] is over.

[57:16] And so now the real like work is happening.

[57:19] Well, that's what they said in 2018, and then they said again in 2022 and 2023, and they'll

[57:24] say it again in 2029.

[57:29] In the end it's the market that will decide whether Dash is dead or not.

[57:36] If people want to eventually use free market money rather than state controlled coercive

[57:45] money, then, you know, that so be it.

[57:50] But yeah, at the end of the day, it's people that will decide whether the Dash or any other

[57:56] project will succeed or not.

[57:58] But you know, I'm always surprised by how much people will just be okay with tyranny.

[58:05] So we'll see.

[58:08] But yeah, I was just looking to see if I could find it and I can see I was in the transactions.

[58:15] So sweet.

[58:16] You got it, man.

[58:17] You're on the blockchain forever immortalized.

[58:22] I thought my claim to fame was going to be my library, but I guess not.

[58:27] You can throw up a URL for Bedrock Layouts when you update it.

[58:34] Sounds good.

[58:36] Then that will be in the blockchain.

[58:39] Okay, let's get the documents.

[59:08] Oh, I'm looking at the wrong one, update contract.

[59:31] I want to do the, where's the note one?

[59:36] Okay, so if I want to go, BedrockLayout.dev, check out BedrockLayout.dev.

[59:56] It's a cool project, it's very cool.

[60:22] I've heard about this, who covered this?

[60:29] I've heard about it.

[60:30] Me.

[60:31] It was on FS Jam and it would have been on my stream.

[60:34] Okay.

[60:35] I've been on Anthony's stream, been on a couple of podcasts, I've written a course off, actually,

[60:41] two courses, actually.

[60:42] Round up.

[60:43] You're going to have to zoom in for the folks.

[60:48] Oh, yeah, yeah, sorry.

[60:51] Basically, the idea is like, hey, the webpage is built and you can do it one way where you're

[61:00] like, I'm going to make this thing work.

[61:03] And then you solve all those problems and you start over again.

[61:06] And you solve the problems all over again, every single time, as far as layout goes.

[61:10] But a lot of layout patterns are pretty much reusable over and over again.

[61:16] And so that's the idea, is like, hey, let's create this pattern where we like.

[61:21] Okay.

[61:22] So this is specifically just layout components.

[61:28] Is this React only or is it compatible with other frameworks?

[61:32] So it's actually like, at the heart of it, it's a CSS layout.

[61:37] So you can do it with just CSS and it uses, for example, where's the example code right

[61:46] here?

[61:47] Yeah.

[61:48] So you can do it with just using data attributes.

[61:50] You just go data, BR, column drop, and then you throw some configurations in there and

[61:56] it will just make it work.

[62:00] But there is both a React and a SolidJS, like wrappers around that.

[62:08] And yeah.

[62:09] Nice.

[62:10] I'm a big Solid fan.

[62:11] So that's cool that you have that one as well.

[62:14] I love Solid.

[62:16] I wish I could find more reasons to use it professionally.

[62:20] Well, we may have something in the works there.

[62:25] Just saying.

[62:26] Just saying.

[62:27] All right.

[62:28] No.

[62:29] Solid is everything I think React would be if it could start over again at this point.

[62:35] And then have the baggage of trying to be...

[62:37] Anyway, there's my two cents.

[62:40] Yeah.

[62:41] I agree.

[62:43] Let's check out that Grafana dashboard while we're there.

[62:49] And then let's go to...

[62:51] Let's see.

[62:53] Scroll up.

[62:55] And I think the responsive design is not showing the option, so maybe zoom out a bit.

[63:03] There we go.

[63:04] So go just...

[63:05] Let's do...

[63:06] Yeah.

[63:07] It is on last hour.

[63:08] Click the refresh button by the last hour.

[63:12] So those are what looks to be our three transactions.

[63:15] We're the only ones here, by the way, right now.

[63:19] So those are our three transactions.

[63:20] I guess one was creating the identity, top up, and what other transactions...

[63:26] We've done an update as well.

[63:28] So I think we've done more than three, but I'm just kind of surprised to not see the

[63:33] others.

[63:39] Oh, yeah.

[63:44] Now that I've checked out the documents, I see it was this, and now I can see I've added

[63:49] that.

[63:50] Okay.

[63:51] Sweet.

[63:52] Okay.

[63:53] Update now.

[63:54] Already done that.

[63:55] Okay.

[63:56] Let's delete it.

[63:57] Oh, we did all that work.

[64:16] Delete no document.

[64:37] That work.

[64:38] Looks like an error.

[64:39] Looks like a stack trace.

[64:40] Did we mess with your client again, or...?

[64:42] Not this time.

[64:43] Structure, value, are not...

[64:48] Hang on.

[64:50] Okay.

[64:51] Max retries reach.

[64:53] That hit really quickly.

[64:58] What's the most pessimistic release date for the Dash platform, Ryan?

[65:03] There is no...

[65:04] Never?

[65:05] 22nd century?

[65:06] Never.

[65:07] Yeah.

[65:08] Are we going to...?

[65:16] 2100, this has not been released.

[65:19] Just plan on it not happening, is what you're saying.

[65:27] This is trying to delete the note?

[65:29] Yeah.

[65:30] I mean, we could probably just skip this one and build out the front end if you don't really

[65:35] need to delete it for the rest of the tutorial to work.

[65:39] Ooh, now let's set up a back-end server.

[65:50] This is just going to basically serve you the thing that we've been doing with the scripts

[66:14] through an endpoint.

[66:16] Gotcha.

[66:17] Okay.

[66:18] Is that working?

[66:23] Okay, 3001.

[66:27] You just run that in the example.

[66:55] Take the "your name here" out, that would be helpful.

[67:05] There we go.

[67:06] Cool.

[67:07] He's got to slap a react on in front of that and we'll be done.

[67:14] Let's do this.

[67:17] Yeah, it's like you'll be our second person to make it all the way through in one go.

[67:24] Let's not use TypeScript right now.

[67:29] And you're going to select "yes" for Tailwind and "yes" for source directory and "yes" for

[67:34] app router, yeah.

[67:38] That one doesn't matter.

[67:39] And open the page and we're going to put this in here.

[68:03] Oh, paste, there we are, wait.

[68:24] Let's see if I missed something in here.

[68:45] This is just to make sure your next thing is set up.

[68:48] Yeah, it should probably read the tutorial.

[68:52] And then you're going to want to edit your in here for the page, it has my AJC web dev

[69:00] hard code in there.

[69:01] So you'll just have to change that to Wolverine.

[69:03] Gotcha.

[69:04] Yeah.

[69:05] So we're going to change page.

[69:08] You could try to get yours as well, Anthony.

[69:13] Is it still there?

[69:14] Have you done it?

[69:15] I have no idea.

[69:20] We'll try that next.

[69:24] Sweet, ship it.

[69:30] I think it needs some layout components.

[69:34] GC web dev.

[69:40] Let's just see what happens.

[69:41] No, it doesn't work.

[69:42] Actually, so instead of hold on, instead of that, do AJC web dev 2024-06-03.

[69:56] 2024-06-03.

[69:57] Try that.

[69:58] That should work.

[69:59] That's a more recent one.

[70:07] And then what was Nick's?

[70:08] Was it Nick that got through all the way?

[70:11] It was Noah.

[70:12] Noah.

[70:13] I forget.

[70:14] Noah in the ark.

[70:15] No, it would be N-H-E-I-N-D-E-V, probably.

[70:23] It's not Noah.

[70:24] It's N-H-E-I-N-D-E-V.

[70:25] H-E-I-N-D-E-V.

[70:26] That's his usual handle.

[70:27] I can't remember if that's exactly what he used or not, but we'll see.

[70:31] There we go.

[70:32] There it is.

[70:33] Still there.

[70:34] Awesome, man.

[70:59] I like it.

[71:02] SDK pulls the mystery and the technical, like the parts that are difficult to wrap your

[71:07] mind around and just turns it into CRUD operations, which are easier to understand.

[71:12] It's like, I'm just, I'm building, I'm creating identity.

[71:19] I'm, yeah, I'm creating a contract.

[71:22] I'm adding documents.

[71:23] These are all things that like I can wrap my head around because there's things I do

[71:27] like.

[71:28] Yep.

[71:29] And I like the technicality that is on the, how it gets on the blockchain and all that.

[71:34] I don't, I find it interesting to a point, but not interesting enough to implement it

[71:39] myself.

[71:40] But yeah, no, this makes it a lot easier to then go, okay, I'm, I'm using blockchain.

[71:46] I'm using all this.

[71:48] But I don't know.

[71:49] You too.

[71:50] Could rug a whole community.

[71:51] Exactly.

[71:52] Oh yeah, obviously we didn't do anything useful today, but that gives you the, the

[72:01] underpinnings of what you can do with dash platform and store data on there.

[72:09] At some point, maybe able to do execution on the chain so that you, instead of reaching

[72:15] for something like, well, what's your cloud functions of service provider of choice?

[72:27] Yeah.

[72:28] Like your AWS, your Azure.

[72:32] Yeah.

[72:33] So yeah, essentially you can do that without any kind of permission or account setup.

[72:39] So yeah, that's the idea.

[72:44] Oh, that was really easy.

[72:49] And yeah, like having a good SDK where you, yeah, it makes that easy to wrap your head

[72:54] around.

[72:55] Yeah.

[72:56] Really easy.

[72:57] Cool.

[72:58] I think we'll, we'll leave it there.

[73:00] Thanks for joining.

[73:01] Stay on when we, when we go off live Travis, just so we can explain to you how you can

[73:05] get paid and all that.

[73:06] Oh yeah.

[73:07] Yeah, for sure.

[73:08] Yeah.

[73:09] A little bit.

[73:10] Thanks everyone for watching.

[73:11] Thanks for the lively debate in the chat.

[73:14] Did we solve the world's problems?

[73:17] I don't know.

[73:18] But I mean, Dash went up $19 just while they were having that argument.

[73:22] So yeah.

[73:23] Right.

[73:24] All right.

[73:25] All right.

[73:26] Yeah.

[73:27] Next time.

[73:28] See everybody.

[73:29] Everybody.

[73:29] [BLANK_AUDIO]
