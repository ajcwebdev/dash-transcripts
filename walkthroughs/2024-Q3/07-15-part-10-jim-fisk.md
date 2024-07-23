---
showLink: "https://www.youtube.com/watch?v=9HibmCtjlX8"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Platform Walkthroughs Part 10 - Jim Fisk"
publishDate: "2024-07-15"
coverImage: "https://i.ytimg.com/vi/9HibmCtjlX8/sddefault.jpg?v=668c52fc"
---

## Episode Description

Jim Fisk, a web developer, explores Dash Platform's decentralized application capabilities through a hands-on walkthrough with Rion and Anthony.

## Episode Summary

In this walkthrough, web developer Jim Fisk learns about Dash Platform's decentralized application (dApp) capabilities. Guided by Rion and Anthony, Jim goes through the process of setting up a Dash Platform environment, creating identities, registering names, and interacting with data contracts and documents. The tutorial covers key concepts like proof-of-work vs. proof-stake blockchains, DAOs, and the potential applications of Dash Platform. Jim builds a simple dApp using Express and Next.js, demonstrating how to integrate Dash Platform functionality into a web application.

## Chapters

00:00 - Introduction and Background

Jim Fisk introduces himself as a web developer with experience in CMS technology, Jamstack, and microservices. He expresses his interest in learning about Dash and blockchain technology. The hosts, Rion and Anthony, begin to guide Jim through the Dash Platform walkthrough.

02:55 - Understanding Dash Platform Basics

Rion explains the fundamental concepts of Dash Platform, including proof-of-work and proof-of-stake blockchains, masternodes, and the dual-blockchain structure of Dash. They discuss how Dash pioneered concepts like staking and DAOs (Decentralized Autonomous Organizations).

17:27 - Setting Up the Environment and Creating Identities

Jim begins the hands-on part of the tutorial, setting up his environment and creating a Dash identity. They discuss the concept of credits in the Dash ecosystem and how they relate to the platform's functionality. Jim encounters and resolves some initial setup issues.

35:35 - Data Contracts and Documents

The conversation shifts to explaining data contracts and documents in Dash Platform. Jim creates his first data contract and submits documents, learning about the structure and purpose of these components in building decentralized applications.

57:03 - Building a Simple dApp

Jim starts building a simple decentralized application using Express and Next.js. He sets up an Express server to interact with the Dash Platform and creates a frontend to display identity information. This section demonstrates how to integrate Dash Platform functionality into a web application.

76:47 - Wrap-up and Future Applications

As they finish the tutorial, the discussion turns to potential applications for Dash Platform. They talk about its suitability for public data, censorship-resistant applications, and how it could simplify development for certain types of applications. The episode concludes with Jim successfully running his first Dash Platform dApp.

## Transcript

[00:00] All right, we are at part 10, made it to the double digits of Dash platform walkthroughs

[00:08] with my good old buddy, Jim Fisk.

[00:10] What's up, Jim?

[00:11] Hey, how's it going?

[00:12] Good.

[00:13] Why don't you introduce yourself to our audience?

[00:16] Sure.

[00:17] So I'm Jim.

[00:18] I'm a web developer.

[00:21] I've had a kind of a meandering career of doing different things.

[00:25] I mainly started in CMS technology, building websites for governments and nonprofits.

[00:32] I got excited about Jamstack technology.

[00:35] That's how I met Anthony back in the day.

[00:38] Like static site generators and beyond, and just a whole general gamut of things.

[00:45] So through that work I was doing on static sites, everything's kind of microservice architected.

[00:50] So building microservices with Go has been something that I've been doing for the last

[00:53] few years and yeah, I'm a crypto enthusiast, but I'm a newbie in terms of like blockchain

[01:00] and decentralization.

[01:01] I love the idea of that stuff, but it's like I've never really dove too deeply myself into

[01:09] that world.

[01:10] So I'm excited to connect with you guys, learn a little bit about Dash, which is something

[01:13] that's been on my radar for a little bit, but to actually get some brass tacks knowledge

[01:17] is really exciting.

[01:18] And you built a Svelte framework, I'm not sure if you mentioned that.

[01:22] Yeah.

[01:23] So one of these walkthroughs was to get JavaScript developers and like front end framework kind

[01:28] of people on.

[01:29] So Rion, this is your Svelte guy right here.

[01:33] It's funny.

[01:34] I built the Svelte framework, it's like a static site generator, but yeah, it's funny

[01:40] because I'm like the least JavaScripty JavaScript guy.

[01:43] I actually built that out of like spite of a lot of the JavaScript ecosystem.

[01:46] It's probably the oldest Svelte framework there is now.

[01:49] Yeah, it was pretty early.

[01:52] That was like back in the Sapper days, so yeah.

[01:56] Svelte framework, what does that even mean?

[01:58] Svelte is a framework.

[01:59] So how do you build a Svelte framework without building Svelte?

[02:02] What does that mean?

[02:03] Yeah.

[02:04] Yeah, that's a good point.

[02:05] So, yeah.

[02:06] So I mean, Svelte is still doing the heavy lifting of SSR and DOM targets, but we're

[02:13] basically just handling all the things like routing and hydration.

[02:18] And we actually built a little CMS into the system itself.

[02:22] So if people are familiar, Static Site Generator is the whole thing.

[02:25] That's cool about that is you can deploy them on like GitHub pages or GitLab pages.

[02:28] And what we do is we shipped basically a small Svelte app that uses OAuth to connect back

[02:33] to those platforms.

[02:34] And then, so what you can do is you can log into your website, which is a static site,

[02:38] you can make changes, and then that basically writes back to your repo, CI rebuilds it and

[02:41] then deploys it.

[02:42] So it feels like a CMS, but there's no server on the backend.

[02:45] Yes, that's very cool.

[02:47] And that's actually kind of near and dear to my heart, because I personally, I have

[02:55] this thing with corporations running the world, and I don't like that trend.

[03:02] And I think static sites are a good technical solution to have people build sites.

[03:10] And like, you own the site.

[03:13] And if we could just get people, like, it's not, you don't have to, I understand there's

[03:18] a very small connection there.

[03:20] But it's an important small connection in that when you are interacting with servers,

[03:30] by nature, you're kind of like, assumed into like, into the board to some degree.

[03:37] Whereas if you can just author static sites, that's something that you own, and as long

[03:42] as you can deploy it to any number of, it's just a more decentralized option, overall,

[03:48] in general, is what I'm trying to get at.

[03:50] So yeah, I like that trend, and I think it pairs well with web three, which is what we're

[03:54] here to talk about today, dash specifically, dash platform, but also hopefully, not hopefully,

[04:02] it will work with a static site, because it's just an SDK that you import into your site.

[04:10] And let's go ahead and get your screen share going.

[04:14] And also, we're going to talk about you've used that you've had, you've owned dash before.

[04:18] That's right.

[04:19] Yeah.

[04:20] Yeah.

[04:21] You mentioned it on a pre show, but I said, Oh, hold that.

[04:24] Let's, let's share that with the folks.

[04:26] Yeah.

[04:27] So, I mean, this was a while ago, but I can't actually even remember the date when I purchased

[04:32] my first dash, but I, you know, I had heard some kind of, you know, murmuring about some

[04:38] of the advantages of dash over something like Bitcoin for, for being a transactional product

[04:43] in terms of, you know, reached you somehow.

[04:46] Yeah.

[04:47] Yeah.

[04:48] So, so, I mean, that was exciting to me because I actually, I know a lot of people think of

[04:52] crypto as this, this investment product, like the store of wealth that grows.

[04:57] I'm less interested in that.

[04:58] I like the idea of it being a transactional product, that is something that people actually

[05:01] use.

[05:02] And so that was exciting to me.

[05:03] So I just wanted to have some, and, you know, I would love to live in a world where that's

[05:08] something that I'm using on a day-to-day basis, whether it's, you know, using that as a crypto

[05:12] payment process or doing something like we're going to talk about today about using it as

[05:16] a dash platform to actually build products and things.

[05:21] That sounds exciting to me too.

[05:22] I think decentralization is the, is the future.

[05:24] I hope that it succeeds and people embrace it.

[05:27] So I'm excited to learn more.

[05:29] Cool.

[05:30] Very cool.

[05:31] I'm glad to hear that the message got to you somehow.

[05:34] We'll add you to the screen.

[05:38] The looks like you, so you, you got a little bit started, which is awesome because everybody's

[05:44] seen these, these first steps several times.

[05:47] We'll probably want to start at create wallet and identity, I think is about where you were

[05:51] at.

[05:52] Yeah, so I'm, so, yeah, I'm not super far along.

[05:57] So basically I've, I've done a couple of things here, right?

[05:59] So I've set up some of the scaffolding.

[06:02] I tried to do my first transaction via the, this faucet thing that you guys had, or I

[06:08] don't know if you guys had set it up or who runs this.

[06:11] What's that?

[06:12] How'd that go?

[06:13] So it, it didn't, so I had a trouble.

[06:16] So when I, when I went through and I did the transaction, I got like a, like a 500 error

[06:21] and the, the server seemed like it went down for a brief second.

[06:23] So it worked.

[06:24] Yeah.

[06:25] Oh, it did.

[06:26] Okay.

[06:27] Well, I don't see it.

[06:28] And so I'm supposed to be able to confirm this in my, via this address, right.

[06:31] But I don't see any transactions, so I don't know if it did work.

[06:34] Okay.

[06:35] And it did, it did lock me out for, it said, try back in an hour too.

[06:40] So it said both those things.

[06:41] And so I figured instead of spamming this and having it not work when you guys are on

[06:45] the call, I might as well wait for you and we can take a look.

[06:48] This was over an hour ago.

[06:49] We should be good to try again if you want me to start here.

[06:52] Yeah.

[06:53] Let's do it.

[06:54] Let's do it.

[06:55] Okay.

[06:56] So you already have an address then.

[06:57] Yeah.

[06:58] Is this in my API?

[06:59] I can't remember where this is.

[07:00] All right.

[07:01] Great.

[07:02] So I'll grab my address and let's put this in here.

[07:09] Okay.

[07:10] So that's my address.

[07:11] I got to see, this is the thing I always struggle with is passing these.

[07:14] Okay.

[07:15] So bridges we're looking at, that looks like that's, I think that's a bridge.

[07:18] That's always ambiguous.

[07:19] Bridge, bridge, bridge.

[07:20] Is that a bridge?

[07:21] I don't know.

[07:22] Good question.

[07:23] I'm going to say, yeah.

[07:27] More bridges.

[07:28] That's a bridge.

[07:29] That's a bridge.

[07:30] That's probably a bridge.

[07:31] Okay.

[07:32] And then.

[07:33] It's going to tell you the same thing if it already gave you a message saying no more

[07:38] dash for you.

[07:39] But that usually means that it gave you dash is probably just not showing up in the block

[07:43] explorer.

[07:44] Okay.

[07:45] Should I click get coins now?

[07:47] Let's go ahead and forward the coins and see what happens this time.

[07:50] And then Anthony, if you could do this on your side, we may have to send him some coins

[08:00] instead of getting them from the faucet.

[08:02] I think that we're still running on the same test net that we did last time.

[08:05] So if you already have some from last time by chance, Anthony, we could just try sending

[08:10] him some.

[08:11] Yeah, I can also get him set up with dash made on a local node pretty easily now.

[08:17] Oh, okay.

[08:18] So we might end up going that route.

[08:20] Let's just try.

[08:22] Let's go forward like we have funds and see what happens when we try and register the

[08:26] identity because I think it's the funds are probably in there.

[08:29] Oh, well, I'm not so sure about that.

[08:32] If the block explorer is not showing any, because usually I know that too, but we'll

[08:37] find out, I guess.

[08:40] So Jim, just so you know, our test net infrastructure isn't a top notch here.

[08:49] So sometimes the explorer doesn't show us what we're looking to see and sometimes the

[08:53] faucet doesn't work, but we have an alternate plan if it's not working, which we want to

[09:02] test anyway.

[09:03] So it might be a good time to do that.

[09:04] Well, let's go ahead and go back to the tutorial and we'll act like we have funds.

[09:12] And if it in fact shows that we don't, then we'll go with the local route.

[09:17] Okay.

[09:18] Okay.

[09:19] So you want me to skip ahead here?

[09:20] So this would be the transaction link that's not appearing, but we'll get that in a minute.

[09:23] It sounds like.

[09:27] Some more about that.

[09:28] Okay.

[09:29] Then I did register and retrieved an identity.

[09:32] Oh, okay.

[09:34] Then you already have the funds.

[09:35] You can't do that without funds.

[09:36] Okay.

[09:37] Okay.

[09:38] So, and this is my identifier.

[09:40] So this is, this means I have a valid identity with credits.

[09:43] Yeah.

[09:44] The credits were because you loaded the funds from the faucet and then transferred that

[09:48] when you created the identity.

[09:50] Oh, okay.

[09:51] Okay.

[09:52] That makes sense.

[09:53] And I was able to verify that balance.

[09:54] I know there was a, like a step here of where is it?

[10:03] Doing the retrieve identities.

[10:04] I did this and I can see like a balance when I run that script.

[10:09] So I got, I got something like this.

[10:11] That script was failing last time we were doing this.

[10:14] That's good.

[10:15] Yeah.

[10:16] It seemed to work for, I can run it.

[10:17] I don't know if it.

[10:18] You should have your identity ID in your .env also.

[10:20] Oh, okay.

[10:21] I don't think I.

[10:22] Just run that retrieve identities and then we'll see if it, is this, is this where it

[10:31] spits out the.

[10:32] Yeah.

[10:33] The whole object.

[10:34] Yeah.

[10:35] It took a second the last time I did it, but it did spit out the balance.

[10:41] Here, actually I copied it over to a text file just in case.

[10:46] So it looked like this.

[10:47] Nice.

[10:48] And it gave me this.

[10:50] Okay.

[10:51] So you just copy that identity ID and create a environment variable.

[10:56] Is it called identity ID?

[10:58] Snake, snake, snake, a screaming snake case.

[11:05] Okay.

[11:07] Right.

[11:09] All caps.

[11:13] Yeah.

[11:17] We want that snake to be screaming.

[11:19] I never heard that.

[11:22] Screaming snake case.

[11:23] I like that.

[11:24] Yeah.

[11:25] Okay.

[11:26] Let's see.

[11:27] I command probably finished by now.

[11:30] Cool.

[11:31] Yep.

[11:32] Oh, cool.

[11:33] So we have this here.

[11:34] Yeah.

[11:35] Cool.

[11:36] Same identity, right?

[11:37] Yeah.

[11:38] So that's the, yeah.

[11:39] 7BR, 6PA.

[11:40] All right.

[11:41] You're cooking.

[11:42] You're ready to go.

[11:43] Okay.

[11:44] Yeah.

[11:45] All right.

[11:46] Back to the tutorial?

[11:47] Yep.

[11:48] We go.

[11:49] All right.

[11:50] Okay.

[11:51] So we have an identity.

[11:52] Actually, maybe this is a good time to explain.

[11:53] So the identity, this is like a personal identifier for myself on the network.

[11:57] Is this like a username for me or what is the identity?

[12:02] It's like a public private key pair.

[12:04] And what you see that was outputted is like the public part of it.

[12:10] And this is something I keep telling myself to look into specifically so that I can have

[12:15] a more confident answer.

[12:16] But what you would need to know about this is that it's kind of like a public private

[12:22] key pair where, or in fact it is exactly that.

[12:28] And the identity is what you use to do all of your interactions with the Dash platform.

[12:38] So it holds a balance as well.

[12:42] And you can register names, which we'll do, and you can register data contracts and submit

[12:48] documents all through this identity.

[12:50] Okay.

[12:51] And then this balance is not actually debt.

[12:54] This is like some kind of equivalent credit that relates to a Dash?

[12:58] Yes.

[12:59] So one Dash, if you're familiar with Bitcoin, in Bitcoin you have one Bitcoin.

[13:07] There are a hundred million Satoshis is the smallest unit of Bitcoin.

[13:11] So a lot of people in the early days used to think you could only buy one Bitcoin, but

[13:16] now you can buy like sub parts of Bitcoin.

[13:19] It's the same in Dash.

[13:21] So 100 million Satoshis in Dash is one Dash.

[13:26] And then that gets further divided into thousand credits.

[13:29] So one hundred, instead of million, it's 100 billion credits is one Dash, essentially.

[13:37] So you get a bunch of credits.

[13:39] They're very small unit and that's how you, and the reason for that is that like the smallest

[13:45] unit of computation, all the things that you do on Dash platform is either it's computation,

[13:53] like any cloud service, you would have storage costs and you would have compute costs and

[13:57] things like that.

[13:58] And the smallest unit of computation is a credit.

[14:03] Well there's like a price list, which we haven't shown or gone through, but you can imagine

[14:08] that everything that you do, whether it's storing data or registering data, which has

[14:13] computation along with that, would cost a certain amount of credits.

[14:18] So instead of using very, very small decimal points, we just use very small units.

[14:23] Gotcha.

[14:24] And so obviously, you know, through this process, I got some credits from the Fawcett app, but

[14:29] like if I were to do something in production, I would basically, would I exchange Dash for

[14:36] the credits or can I buy these with U.S. dollars or how would I obtain these to start a platform?

[14:41] Yep.

[14:42] Yep.

[14:43] So you exchange Dash for the credits.

[14:44] Exactly.

[14:45] And that's like a built-in exchange feature of Dash.

[14:49] So there are high level architecturally, Dash consists of two blockchains.

[14:58] You have a proof of work blockchain, and then you have a proof of stake blockchain.

[15:02] Do these terms mean anything to you with the level of knowledge that you have with crypto?

[15:07] Do you know, I'm vaguely familiar with the terms, but I'd love a quick recap if you're

[15:12] able to.

[15:13] Sure.

[15:14] Yeah.

[15:15] So proof of work is where...

[15:16] So every cryptocurrency has to get created and put into circulation somehow.

[15:22] And in Bitcoin, since that was the first cryptocurrency, that's always a good place to start.

[15:27] In Bitcoin, Satoshi defined it so that you would have to do some work.

[15:35] So he was like killing two birds with one stone.

[15:38] One thing that he needs to do is he has to incentivize the node operators on the network.

[15:45] And another thing he needs to do is get his currency into circulation.

[15:51] And so you might as well do those, like pair those up and have those all be done with one

[15:56] process and that's the mining process.

[15:58] So the mining process is you have a bunch of transactions that happen on the peer to

[16:02] peer network.

[16:04] Somebody has to assemble these transactions and put them into a block of transactions

[16:08] and put a stamp on it that says these are all valid transactions.

[16:12] That's what the whole process of mining is.

[16:15] And because that is a process that takes computation power, and Satoshi recognized that you can't

[16:22] just let this be a volunteer thing, you have to incentivize and compensate the miners for

[16:30] doing this work.

[16:31] Otherwise, it's a non-sustainable network.

[16:34] And so the method of which he used to allow miners to be the one miner on the network,

[16:41] because it's an open network, anybody can choose to be a miner.

[16:45] So he decided that we're just going to have this work function where you're just crunching

[16:53] a bunch of numbers to show that you've done some work.

[16:57] And so the whole purpose behind that is civil protection, because you don't want an attacker

[17:02] to be able to spin up, let's say a thousand miners and just take over the network.

[17:07] And so to protect against that, there was this work function that had to be performed

[17:12] so that you could, proportional to the work that you're putting into the network, you

[17:18] could be chosen to be that miner that gets to append the blockchain with new data of

[17:24] transactions that are occurring on the network.

[17:27] And so that's proof of work.

[17:30] And it goes a lot deeper than that, I just barely skimmed the surface, but that's proof

[17:33] of work.

[17:34] Now, then later came along proof of stake, where some people recognize, hey, like, there's

[17:41] another way to secure this network.

[17:45] And we call it proof of stake, and it's basically instead of people showing, proving that they've

[17:50] done a bunch of work to be able to participate in the network, let's just prove that they

[17:56] own a bunch of the stake of the network, meaning the native tokens of that cryptocurrency.

[18:04] Also contrary to popular belief, Ethereum was not the first proof of stake blockchain,

[18:09] it was actually very, very far behind in the list of proof of stake blockchains.

[18:13] It's now a proof of stake blockchain, but it wasn't until just recently.

[18:19] So proof of stake is similar in concept, but instead of doing a bunch of work, you just

[18:25] have to prove that you own a bunch of coins.

[18:28] And so Dash came along after Bitcoin and said, hey, there's this hybrid model where we can

[18:36] mine coins through proof of work, but we can also introduce some kind of staking elements

[18:43] into this.

[18:44] And we call that a master node, where a master node is a certain node on the network that's

[18:49] running this node, meaning that somebody running the computer, running the software that relays

[18:55] transactions and validates them and things like that.

[18:59] If we have a node that proves that they have 1000 Dash, then we can assign these specific

[19:08] special nodes certain responsibilities to perform, and because they're backed by stake,

[19:17] we can trust them.

[19:19] And so every master node on the Dash network is collateralized by this 1000 Dash stake.

[19:26] And they perform things like private send functions and instant send confirmation so

[19:31] that you can get instantly confirmed transactions, things like that.

[19:35] So that's not necessarily proof of stake, but it's proof we pioneered that concept of

[19:40] staking some coins to do some service.

[19:43] And then later on, we wanted usernames on our blockchain.

[19:50] And so long story short, we developed this product called Dash Platform, and we wanted

[19:57] this to be a proof of stake blockchain, because we already have this set of validators that

[20:03] we already know and trust.

[20:04] And so we use a subset of the master nodes to be the stakers on the proof of stake network.

[20:13] So yeah, you have these two different blockchains, and then there are ways to move funds from

[20:19] the proof of work chain to the proof of stake chain.

[20:23] And that's what we're doing when we're doing this top-up identities transaction.

[20:27] So that's a long answer to your question about moving, how do you get credits?

[20:35] So yeah, you do this special transaction called the top-up transaction that moves the coins.

[20:42] And then there's also going to be a withdrawal function as well that will do the opposite

[20:47] and move it back from the proof of stake platform chain back to the proof of work core payments

[20:53] chain.

[20:54] Hmm.

[20:55] And anyway, this is done for an efficiency standpoint, is that to not waste compute or

[21:01] what is the basic like, what is the impetus behind that structure?

[21:07] Yeah, like why have two different blockchains?

[21:10] So proof of stake blockchains, proof of work blockchains, I guess I'll start with that.

[21:15] They're not really designed to be able to hold data and have like indexing and proofs

[21:27] and stuff like that.

[21:29] You can store data in proof of work blockchains.

[21:32] A lot of people have done that.

[21:35] You store data in like the op return field is what it's called, but it's not specially

[21:40] designed for that.

[21:42] So the proof of work blockchain, which is based on Tendermint, if you've heard of blockchains

[21:49] like Cosmos or things like that, they developed a blockchain that you could basically just

[21:57] like kind of like a white labeled blockchain almost like it just, it's got the bare bones

[22:02] minimum infrastructure that you need to create a blockchain.

[22:07] And then you can just, anybody can pretty easily spin up their own blockchain.

[22:11] Well, we took that and we modified it.

[22:14] But basically at the end of the day, the purpose behind that is because we, the purpose behind

[22:20] having two blockchains is that we have two main different types of functions, storing

[22:26] data and retrieving data.

[22:29] This is better done on a proof of stake blockchain that has like, yeah, it's just better tailored

[22:39] for that, whereas we don't want to get rid of the proof of work chain because there are

[22:45] certain security properties that that has, and actually not just security, but some people

[22:53] think it's even more fair ways to distribute coins.

[22:59] So we have both.

[23:00] So we have, if we want certain properties of one, we can use the one.

[23:04] If we want certain properties of the other, we can use the other.

[23:07] So it's kind of like a marriage between these two different types of blockchains.

[23:12] And those are really like the main two.

[23:14] And you also have proof of authority chains where it's like, you know, very indistinguishable

[23:20] from just a centrally controlled corporation.

[23:22] So we're not too interested in that anyway, but yeah.

[23:27] And the "we" that you're talking about, this is like, what is the term, DAO, is that Decentralized

[23:32] Organization?

[23:33] Yeah, so DAO is Decentralized Autonomous Organization.

[23:38] It's just a kind of a funny term for an organization that's open for anybody to participate in.

[23:46] So do you know much about DAOs or DAOs?

[23:51] Besides the name and yeah, the general concept, but no, I don't know functionally how they

[23:56] work.

[23:57] Well, there are a ton of them.

[23:59] There are a lot of them in the Ethereum ecosystem and other proof of stake ecosystems.

[24:08] It's basically, Anthony, I've been talking quite a bit.

[24:12] Why don't you, and you're pretty familiar with this topic.

[24:15] So why don't you give Jim your explanation of a DAO?

[24:19] Yeah, so a DAO is like a corporation and a government had a baby written in code.

[24:30] It's like a bunch of contracts that allow funding to be set aside to basically build

[24:37] new stuff or maintain the network that is then decided on by people submitting proposals

[24:43] that are voted on and then it gets paid out to the network.

[24:47] So if you own Dash, you can vote on like where the Dash funds should go.

[24:55] So it kind of is more transparent in terms of everyone sees where the money is, who the

[25:01] money is going to, and it's a really interesting system.

[25:05] A lot of them are pretty dysfunctional, but this one is like going for a while and seems

[25:10] to, I mean, I always get paid, so.

[25:14] Is it registered with any government body or anything like that?

[25:18] No, the DAO itself is not.

[25:22] So the DAO itself, or any DAO for that matter, is just software.

[25:28] At the end of the day, it's just software and what that software does is depends on

[25:33] the specific DAO.

[25:35] But in our DAO, what it is, is our DAO is mostly part of our proof of work chain.

[25:43] So that's, I mean, obviously we started as a proof of work chain.

[25:46] We don't even have any proof of state chains on the main net yet.

[25:50] This is still in test net.

[25:53] But yeah, like our DAO is essentially a function in the C++ code or a set of functions in the

[26:00] C++ code of the, that's synonymous with a node.

[26:08] It just happens to be written in C++.

[26:11] It's just certain functions there that say, "Hey, there's a certain cycle where we're

[26:16] accepting proposals on our network and those proposals can be requesting funds.

[26:22] They can be asking a question and then the node operators or specifically the master

[26:28] node operators are allowed to then vote yes, no, abstain on those proposals.

[26:35] And if it's a funding proposal, then if it reaches, if that specific proposal reaches

[26:40] a certain amount of votes, then the funds are then created and then sent to the owner

[26:46] of that proposal, which putting the address to pay out to is part of the proposal creation

[26:52] process.

[26:54] If it's just a question, like sometimes people, like a very classic example of a governance

[27:00] question would be like, "Hey, should we raise the block size limit from one megabyte to

[27:05] two megabytes?"

[27:08] That was something that the Bitcoin community got mired in for many, many years and people

[27:15] still look back on that huge debate and people are still actually having that debate.

[27:21] But in Dash, we actually had that question and somebody just submitted a proposal to

[27:25] the network and the stakeholders, meaning the master node owners, they voted on it and

[27:30] it was done within a month.

[27:32] So it's just a very easy way for your network to come to decisions on important matters

[27:40] instead of going back and forth on Reddit.

[27:44] There's some importance of going back and forth and having discussions on Reddit and

[27:48] Twitter and things like that.

[27:50] But at the end of the day, you want to know what the stakeholders view as their opinion.

[27:55] So we actually pioneered the whole concept of DAOs as well in that sense where we were

[28:02] the first functional DAO back over, not over 10 years, our blockchain has gone on for over

[28:09] 10 years, but our DAO is probably eight or so years old now.

[28:14] So it was the first one even before the quote, the DAO in the Ethereum land, which is a little

[28:20] bit more popular, but wasn't the first.

[28:23] Anyway, so yeah, that's the Dash DAO and that's DAOs in general.

[28:26] It's just like Anthony was saying, if you had governments which operate by polling and

[28:34] voting and things like that, for the most part, and married that with corporations which

[28:39] have funding and all that stuff, that's what a DAO is.

[28:43] And it's the distinguishing feature is that it's open.

[28:47] So anybody can make a proposal.

[28:49] Anybody can join, if you have a thousand Dash, you can operate a masternode and become a

[28:55] voter.

[28:56] Nobody's going to say no, because it's just software.

[28:58] Yep.

[28:59] And the funding itself is what's coming from the blockchain, right?

[29:03] Like the funding is Dash?

[29:04] Yes.

[29:05] Cool.

[29:06] Yep.

[29:07] So we're in Bitcoin, 100% of the newly issued Bitcoin on a daily, monthly, yearly basis,

[29:13] that's all going to pay miners, which is important, but in Dash, we recognize that's not the most

[29:18] important.

[29:19] It's not the only important thing to fund.

[29:22] It's also important to fund your core developers.

[29:24] It's also important to fund community developers.

[29:26] It's also important to fund marketers.

[29:30] And so we split out a portion of the block reward, 20% actually to this generalized fund

[29:38] that can pay anybody who submits a proposal and has a successful proposal, including yourself,

[29:44] Jim.

[29:45] So you could make your own proposal to the network and try to ask for funding if you

[29:50] wanted to work for Dash more in the future.

[29:54] And then so I assume like someone who's well respected in the community can probably propose

[29:59] something larger and then they might get funding that they then allocate to other developers

[30:04] or other people to help them like carry out that vision.

[30:07] Okay, cool.

[30:08] Yeah, that's exactly, that's where we are.

[30:11] That's what we're doing.

[30:12] So I get funding from the proposal system actually just a few hours ago, we had our

[30:18] call to give our quarterly report from last quarter and ask for more funds for Q3.

[30:25] And yeah, so I received those funds and then I pay out because not everybody has to have

[30:30] their own specific proposal.

[30:33] There's a certain balance to take.

[30:34] You don't want too many people having proposals and then it becomes hard to manage and for

[30:41] the stakeholders to read 100 proposals, but you also don't want one proposal.

[30:46] So yeah, we try to strike a balance.

[30:49] That's what we're paying for.

[30:50] That's how we pay for this specific effort right here.

[30:54] So, yep.

[30:55] Nice.

[30:56] That sounds great.

[30:58] Should I start sharing my screen again and go back to the tutorial?

[31:02] Yeah.

[31:03] Okay.

[31:04] Let's see here.

[31:07] Are you with me?

[31:10] Yeah.

[31:11] We need to add.

[31:12] Yeah.

[31:13] There you go.

[31:14] Yeah.

[31:15] And then, so I think this kind of like this next section looks like it's going back to

[31:18] what we were talking about.

[31:19] So it looks like we're heading to converting Dash to credit.

[31:23] So that kind of goes to that initial question I had there.

[31:26] So it looks like I need to do my top-up identity script can pop over here.

[31:35] I'll create that file and then that will create a script file called top-up identities.

[31:42] Okay.

[31:43] And there's probably some code we want to put in here.

[31:45] Okay.

[31:46] Let's grab this.

[31:47] And then Anthony, I don't know if you want to walk through this, but it looks like we're

[31:57] getting our wallet, we're getting our identities and then we're running a top-up.

[32:04] So this here, are we just adding?

[32:07] Yeah.

[32:08] That's the credits.

[32:09] Yeah.

[32:10] Okay.

[32:11] So that's the amount.

[32:12] And that's what we're talking about with the smaller denominations and you just need the

[32:15] identity ID and then you feed that to the top-up.

[32:20] And the way I have this written is that you can end up with multiple identity IDs within

[32:25] a single wallet if you create more than one.

[32:27] And this just tops up all of them because it's all just Monopoly money right now, but

[32:32] you would want more granular control of that once this is on main net.

[32:36] Okay.

[32:37] So because this is a test environment, like that's what's allowing me to do, I don't actually

[32:41] have any real money right now, but because we're in a test environment, it's allowing

[32:45] me to do this.

[32:46] Is that the case?

[32:47] Yeah.

[32:48] Because you got the funds from the faucet and so that you can transfer into credits.

[32:55] So if you have like three identity IDs, you could top up each of them and it's not going

[33:00] to be very much.

[33:02] Gotcha.

[33:03] Okay.

[33:04] So the credits I got from the faucet are being converted here.

[33:08] That's what we're doing.

[33:09] The money I got from the faucet.

[33:10] Yeah.

[33:11] That's moving from the layer one, the original chain to the platform chain, which is where

[33:16] the identity and all that stuff lives.

[33:18] So what I got from the faucet, was that credits or was that Dash?

[33:22] What did I actually get from the faucet?

[33:24] That was Dash.

[33:25] Oh, okay.

[33:26] And then that is turned into the credits once you move on to the platform functionality,

[33:30] which is the identities and the storage and all that.

[33:33] Okay.

[33:34] Cool.

[33:35] And that's the process we're doing here.

[33:36] We're converting that.

[33:37] Okay.

[33:38] So run the script here.

[33:39] Yeah, I have another tutorial I'm working on and I made it even simpler toward the function

[33:48] that you need the credits.

[33:49] I just had a top up run right before anyway.

[33:52] So it just kind of does it automatically.

[33:55] But this is all stuff where you actually want granular control.

[33:59] Once this is real money, you don't want to be just throwing random money in different

[34:03] places.

[34:04] Yep.

[34:05] And while we're waiting for this to complete, how sensitive is the information in this?

[34:11] Is this all considered private if I was in a real world environment?

[34:14] Like should my wallet address, do I need to worry about this?

[34:17] The mnemonic is the most important thing.

[34:19] If this had real funds on it, that's the thing you would, that gives you control of the whole

[34:23] wallet.

[34:24] Okay.

[34:25] But this is like a public address.

[34:27] So this is something I could actually use to receive funds from someone I didn't know

[34:30] or necessarily trust.

[34:31] Yep.

[34:32] Yep.

[34:33] And that's what you do when you claim things in the DAO for tasks.

[34:36] You give your wallet address and the thing you did.

[34:39] Okay.

[34:40] And then my identity ID, is that private or public?

[34:46] That's public.

[34:47] Okay.

[34:48] All right.

[34:49] Let's see here.

[34:50] Let's see if I can.

[34:53] Okay.

[34:54] So it looks like, I'm sorry, let me just close my mini-map here.

[34:58] Okay.

[34:59] Get rid of the thing on the bottom too, that says, hi.

[35:03] Oh yes.

[35:04] Yeah.

[35:05] Thank you.

[35:06] So, okay.

[35:07] The block height handler is already set.

[35:08] My identity credit balance for my ID is this.

[35:12] So that just topped up, it converted to my dash to the credits.

[35:15] Okay.

[35:16] And then is this reflected over in my browser?

[35:19] Should I look at that or?

[35:22] Is that reflected here?

[35:28] This is the top up we just did.

[35:29] There you go.

[35:30] Yeah.

[35:31] So I could take a look at this.

[35:33] Okay.

[35:35] Cool.

[35:36] All right.

[35:38] Next step.

[35:39] So we got our output here.

[35:41] Okay.

[35:42] So now we want to register and retrieve name, create a file.

[35:45] Okay.

[35:46] We're going to create register name.

[35:49] Is this like a username I'm creating right now?

[35:52] Yeah.

[35:53] It's kind of like a domain slash username.

[35:56] Okay.

[35:58] So I create that script and then we're going to create a label in our env and replace your

[36:06] name here with my name.

[36:08] Okay.

[36:09] And do I need this comment?

[36:11] This looks like a, oh, it's just actually doing it.

[36:14] Gotcha.

[36:15] Grab this.

[36:17] I'm just realizing now, Anthony, you go ahead and keep working if you want, Jim, but I'm

[36:21] just realizing now that like introducing the name is actually conceptually should be subsequent

[36:27] to some of the other stuff that we do in this, because the name registering a name is just

[36:34] one type of one type of a document submission.

[36:40] Okay.

[36:41] So what we'll do in the later steps of this tutorial, Jim, is we're going to create a

[36:48] data contract and you can think of that very similar to a database schema.

[36:54] Okay.

[36:55] And then we're going to, after that, we're going to submit documents that adhere to that

[37:00] schema that are called documents.

[37:05] So we have these two concepts in Dash platform, data contracts and documents.

[37:11] And it's just like I said, the data contract is just like a platform version of a database

[37:21] schema or a document database.

[37:25] And then the Dash pay, there's a certain data contract that will be enabled on mainnet soon

[37:36] ish and is already on testnet as well called Dash pay.

[37:42] That's a certain data contract that the developers of Dash core group have written.

[37:49] And that was one of the reasons that we built Dash platform is to have this username system.

[37:55] But it's really just, it's, it's the same as any other data contract that you or I or

[38:01] Anthony could make.

[38:04] But it is a so-called system contract, which means it's kind of like launched with, with

[38:10] Dash platform.

[38:11] And it's kind of like a blessed data contract, but it's the same things conceptually as any

[38:17] contract that we would be making.

[38:19] So yeah, conceptually, we should probably actually put registering a name down a little

[38:26] further maybe as I'm thinking about it, because you don't have the, we haven't yet talked

[38:32] about the data contracts and the documents yet at this point in the tutorial.

[38:38] But anyway.

[38:39] Do you want, do you want me to skip ahead so we can do it in the sequence of what you're

[38:41] describing?

[38:42] We can, we can keep doing it in this sequence.

[38:44] I just, I want to, since it seems like you're pretty inquisitive, I wanted you to get the

[38:50] idea of what this registering of a data of a name is.

[38:56] It's just one instance of registering a data contract.

[39:00] Yeah.

[39:01] I think the, you're right that there should be a section where we just kind of talk about

[39:05] that there's pre-made contracts already.

[39:08] I think right now the way it's grouped is to keep all the identity stuff together.

[39:14] So you like have the concept of identity and then the concept of storage.

[39:19] And so that I think kind of makes sense.

[39:22] But I think once then the data contract is introduced, you can be like, oh, by the way,

[39:27] here are these other contracts you've already been working with under the hood.

[39:30] Yeah.

[39:31] So anyway, we'll, we'll work that out.

[39:33] Yeah.

[39:34] Yeah.

[39:35] And as we get there, I think I have a few questions on it, but just, just real quick.

[39:38] So as, if I was a platform developer, would I have multiple names registered or would

[39:44] I have like one?

[39:45] It sounds like I would have possibly have multiple.

[39:47] As many as you want.

[39:48] Yeah.

[39:49] Gotcha.

[39:50] Okay.

[39:51] Would that be typical?

[39:52] Like, like to carry out, you know, it really depends on, on what you're doing.

[39:57] Like if you had an application where you had some kind of, you know you have some kind

[40:04] of business idea in mind and just like any application, you're going to have users and

[40:10] those users are going to be doing something on your, on your application.

[40:15] Well, in the Dash platform world, you might, you might set up an easy way for your users

[40:22] to register for Dash platform usernames and just use that as your authentication method.

[40:30] Yep.

[40:31] And, and in that case, you would have your users, you would have an application that

[40:34] exposed the ability for your, for your users to register as Dash platform users.

[40:42] And in that case, you would be giving a user, you would be creating a username for each

[40:46] of your users.

[40:49] But you know, that's just one version.

[40:51] You could also, another application is you personally just want to register your own,

[40:59] you know, Jim Fisk name, but you might want a private one in addition to that.

[41:04] And you could use the same identity that controls these two different private, or these two

[41:09] different personas.

[41:11] So there's, that's a different application.

[41:13] Okay.

[41:14] And so if I were, so just the same way that I ran this register name script, I would be

[41:20] doing, I would potentially use the same mechanism for registering all my users of an application

[41:25] that I might build.

[41:26] Yep.

[41:27] Okay.

[41:28] So if in fact you wanted your users to leverage Dash platform as your authentication method,

[41:34] and that's, I've told this to Anthony before, one, one way to kind of easily remember what

[41:39] Dash platform is good for is it's kind of like a, it's kind of like a SPA for SPAs.

[41:46] And by SPA, I mean, it's a different acronym.

[41:49] So SPA meaning storage, payments, and authentication.

[41:54] Different than the SPA that I'm used to.

[41:57] Okay.

[41:58] So it's auth for SPAs, meaning storage, payments, and auth for single page applications.

[42:03] It's like a single page application.

[42:06] You don't want to deal with auth zero for your auth, and you don't want to deal with

[42:11] Stripe for your payments, and you don't want to deal with AWS for your cloud storage.

[42:17] You can use Dash platform for all of those.

[42:20] Gotcha.

[42:21] Okay.

[42:22] Okay.

[42:23] So I'm over here.

[42:26] It looks like that succeeded.

[42:30] I registered my Jim123.

[42:33] Cool.

[42:34] So you're on the platform now.

[42:38] Great.

[42:39] Okay.

[42:40] So following along here.

[42:43] So it looks like that's what I got there.

[42:47] This is, I think, just screenshotting basically what we were just looking at there.

[42:53] So now we're going to create a file to retrieve name.

[42:56] So I think this is basically just using the API to get the same information.

[42:58] Is that what we're doing here?

[43:00] Yeah.

[43:01] Okay.

[43:02] Let's create that file.

[43:07] And we have retrieve name, and let's see, we have a script here.

[43:16] Okay.

[43:17] Okay.

[43:18] So the application that you just went to earlier, the platform, platformexplorer.com,

[43:30] this guy that made this, he's basically doing functions similar to what you're doing to

[43:37] find the names on the platform.

[43:39] He's just doing a generalized approach where he's kind of capturing all the different transactions

[43:45] that go through.

[43:46] So that's this concept of an explorer is that you scour the whole blockchain and you're

[43:54] listening for all the events on the blockchain and you're dumping it into this explorer that

[44:00] anybody can just see if what they did was working.

[44:03] But yeah, you're doing the same thing with the code.

[44:05] Oh, gotcha.

[44:06] Yep.

[44:07] Yep.

[44:08] He's giving us like a GUI for the same basic API transaction.

[44:11] Yeah.

[44:12] Okay.

[44:13] That makes sense.

[44:14] Great.

[44:15] So, yeah.

[44:16] So I just added that there and then it looks like we're just going to run it to, to test

[44:21] it.

[44:22] Let's give that a test.

[44:24] Okay.

[44:25] Yep.

[44:26] And let me just expand that.

[44:30] So yeah, it's basically, this looks like a, maybe a more, like this, they're exposing

[44:36] more information here, but it's the same information as we're seeing here.

[44:39] It looks like.

[44:40] Yeah.

[44:41] And you can see there, there's the data contract.

[44:45] So this has all that information there.

[44:49] Okay.

[44:51] Okay.

[44:53] Great.

[44:55] Okay.

[44:57] And so, yep, we got our object, our name object, our data contract info.

[45:09] Yeah.

[45:10] So I guess the tutorial, I'm sure is going to get into this.

[45:13] Okay.

[45:14] I know we were just, Rion, you're just discussing this.

[45:19] Is it helpful for me to try to go, to go through this or do you want me to skip ahead?

[45:24] Let's see.

[45:25] I switched off.

[45:27] I was looking at data contracts.

[45:29] Yes.

[45:30] Yeah.

[45:31] We'll go through this.

[45:32] I'll breeze it.

[45:33] So it's a, it serves as a blueprint for the structure of data that an application intends

[45:36] to store on the decentralized network.

[45:38] Okay.

[45:39] It defines a schema documents, database records, and you had described this as kind of like

[45:42] a database schema for the decentralized network.

[45:47] Contracts enable the platform to validate data against these schemas to ensure consistency

[45:51] and integrity.

[45:52] Okay.

[45:53] They are crucial for decentralized apps.

[45:55] They provide a structured and predictable way to interact with the Dash blockchain.

[45:59] Data contracts facilitate data storage retrieval manipulation in a trustless environment.

[46:04] You can create data contracts through an online user interface, Dash Pay.

[46:09] Okay.

[46:10] Should I look at this?

[46:11] Or is this just an example?

[46:12] Oh, you can check it out.

[46:15] Yeah.

[46:16] It's a cool little app.

[46:17] Yeah.

[46:18] We won't, we won't go too much into this, but if you did, if you had no idea of what,

[46:21] how to create a data contract, this is, this uses AI to help structure your, your contract

[46:27] and give you a good starting point.

[46:29] Oh, cool.

[46:30] Great.

[46:31] I see that being useful.

[46:32] Okay.

[46:33] Register, retrieve and update contracts.

[46:35] So create a file, register contract.

[46:39] Okay.

[46:41] And then we're going to add a way to create new contracts.

[46:50] And so that first name retrieval it, it, it displayed some information about a data contract.

[46:57] So was it a data contract was created through that process and now we're creating another

[47:01] one.

[47:02] Is that what we're doing?

[47:03] Yep.

[47:04] Okay.

[47:05] Let's see.

[47:06] What did I just create?

[47:09] I just created register contract.

[47:12] Okay.

[47:13] Yeah.

[47:14] So now, so now you're, you're creating your own contract and then more.

[47:22] And what, and what is the purpose of this contract that I'm creating here?

[47:26] Anthony, you want to describe that?

[47:28] Oh, just, just hello world.

[47:29] Okay.

[47:30] It just did like.

[47:31] Contract document has a note.

[47:32] The note is type object.

[47:34] The object has a message.

[47:36] The message is type string.

[47:38] Okay.

[47:39] Yep.

[47:40] In.

[47:41] Okay.

[47:42] Cool.

[47:43] So we created that.

[47:44] We're going to run the script.

[47:47] Let's give that a run.

[47:51] And this will probably appear over here as well.

[47:57] If I come back here, I guess it doesn't like, no, it doesn't like that.

[48:09] It should give you the output of the terminal anyway.

[48:12] Yeah.

[48:13] Okay.

[48:14] So let's.

[48:15] It's not done.

[48:16] So give it a second.

[48:17] This is, that's another thing to do.

[48:19] Go over to the platform explorer and go to contracts, data contracts.

[48:27] And you see the, the latest one was seven nine.

[48:30] So that was like several days ago.

[48:33] Yeah.

[48:34] In theory, if we refresh this after it's done, you'll see a yours.

[48:38] Yeah.

[48:39] Yep.

[48:40] So this is me.

[48:42] Yep.

[48:44] Okay.

[48:46] Did it, was this supposed to say something, Anthony, or was it a blank message?

[48:53] Go back to your terminal.

[48:56] Okay.

[48:57] Let's see here.

[49:00] Sorry, what part were you talking about?

[49:03] The blank message?

[49:04] Oh, I didn't know.

[49:05] So was, does this, does this say hello world?

[49:07] In the.

[49:08] No, not yet.

[49:09] So this creates the schema that allows you to have a message type and then we're gonna,

[49:14] so this is the thing.

[49:15] So there's data contracts, there's documents.

[49:16] Okay.

[49:17] So data contracts says we want a string.

[49:19] Yeah.

[49:20] Okay.

[49:21] I get it now.

[49:22] Gotcha.

[49:23] Yeah.

[49:24] Okay.

[49:25] So, yep.

[49:26] So we have, we specified.

[49:27] Okay.

[49:28] Yep.

[49:29] Message type string.

[49:30] Okay.

[49:31] And now we're going to put a document on this contract, which is the actual data.

[49:34] That's right.

[49:35] Yep.

[49:36] Okay.

[49:37] So I continue on.

[49:38] There you go.

[49:39] Yep.

[49:40] Okay.

[49:41] All right.

[49:42] So we saw in the terminal, I believe.

[49:45] Okay.

[49:46] We looked at the platform Explorer.

[49:48] Great.

[49:49] And now we're going to do retrieve, retrieve contract.

[49:55] Okay.

[49:57] And retrieve contract.

[50:05] Copy this.

[50:07] Okay.

[50:09] Okay.

[50:13] Now we have that, and we're going to run the script.

[50:16] Retrieve contract.

[50:24] Okay.

[50:34] And this is, retrieve contract is again, we're directly hitting the, yeah, it's the

[50:40] same output that you got when you created it.

[50:42] Yeah.

[50:43] Okay.

[50:44] Cool.

[50:45] Yeah.

[50:46] So this, this one, there was an error sometime.

[50:49] I think, I think I actually know what I need to do to fix this, but we can move on to the

[50:53] next, next part.

[50:57] Okay.

[51:00] Just breeze ahead a little bit.

[51:02] Okay.

[51:03] So view on the platform.

[51:04] And we'll be able to check this out and next we're going to create update.

[51:10] Okay.

[51:11] So we're going to update the contract.

[51:15] And so we're going to update the schema of the contract.

[51:17] Is that what we're doing?

[51:18] Yeah.

[51:19] So it's like, if you decide, oh, actually my customers need, you know, country information

[51:25] or something like that, you could go back and modify it.

[51:28] Okay.

[51:29] So should be able to just do this in another window real quick.

[51:36] I'll let that continue running and I'll go to update contract and we'll copy this code

[51:48] here and I'll save it.

[51:53] Let me see if that's still going, it looks like.

[51:57] You could just kill that actually.

[51:58] Just, oh, just let this kill it.

[52:00] Yeah.

[52:01] You can kill that.

[52:02] Yeah.

[52:03] It's erroring out.

[52:04] Oh, gotcha.

[52:05] Okay.

[52:06] Yeah.

[52:07] Okay.

[52:08] So update contract is in there.

[52:09] We're probably going to run the script, these handy dandy scripts.

[52:14] And so this just adds an author information to the note.

[52:20] Gotcha.

[52:21] Great.

[52:22] So yeah.

[52:24] Coming through here.

[52:25] Uh-huh.

[52:26] Get note.

[52:27] Okay.

[52:28] So basically we just, yeah.

[52:29] Adding the author.

[52:30] And this, this is not affecting the message string that we had already put in here.

[52:34] It's just like adding to that.

[52:37] Yeah.

[52:38] Okay.

[52:39] Great.

[52:40] So.

[52:41] So then the next thing would be run this, did I already run this?

[52:52] No, I don't think I did.

[52:56] Okay.

[52:57] So that's updated.

[52:58] So I should probably check that out here in my schema, right?

[53:00] If I come here.

[53:01] So that actually also errored out.

[53:05] Oh, okay.

[53:07] See here.

[53:08] Oh, actually.

[53:11] Check your .env real quick.

[53:17] Oh yeah.

[53:23] I think you, let's see.

[53:27] There there's a part where you update, go to your client also.

[53:34] The contract ID.

[53:35] I think it needs, yeah, two things at once.

[53:49] So there's a part in the tutorial where we update the client.

[53:55] Okay.

[53:56] Actually that.

[53:57] I, I, yeah.

[53:58] Cause I wrote the client as one thing and then I.

[54:02] That's right after the update contract part actually.

[54:04] Oh, okay.

[54:05] I missed it.

[54:06] Oh wait.

[54:07] You need to have the contract ID in the update contract.

[54:09] So you need to contract ID in your .env.

[54:12] The contract ID in here.

[54:14] Okay.

[54:15] Yes.

[54:16] And my contract.

[54:17] That's also why the retrieve contract is failing.

[54:19] Okay.

[54:20] And my contract ID is this.

[54:22] Yeah.

[54:23] Go back to your, go back to your terminal output and just scroll, scroll up to whenever

[54:32] you did the create contract.

[54:35] Yeah.

[54:36] Yeah.

[54:37] Right there.

[54:39] Contract ID.

[54:40] Go.

[54:41] It's up a little higher actually.

[54:42] Oh.

[54:43] Is this not it?

[54:44] It's lost in the, so right up there, actually it's kind of the, the warning kind of obscures

[54:49] it.

[54:50] So.

[54:51] Higher.

[54:52] Sorry.

[54:53] Too far.

[54:54] Go back down.

[54:55] It's here?

[54:56] Go back down.

[54:57] It's going to be in the format of, of an env, an environment variable.

[55:03] So it'll have.

[55:04] Scroll down a little bit.

[55:06] Keep scrolling.

[55:08] Keep scrolling.

[55:09] Okay.

[55:10] Right there.

[55:11] There it is.

[55:12] Contract ID.

[55:13] Up a little higher, above.

[55:14] Oh.

[55:15] Oh.

[55:16] Oh, gotcha.

[55:17] Gotcha.

[55:18] Oh, gotcha.

[55:19] Yeah.

[55:20] Yeah.

[55:21] Yeah.

[55:22] Yep.

[55:23] Gotcha.

[55:24] There we go.

[55:26] And then run this update contract again.

[55:29] Yep.

[55:30] Mm-hmm.

[55:31] Okay.

[55:32] He might, he may need to update the client at this point, right Anthony?

[55:41] After this you update the client, yeah.

[55:44] Okay.

[55:45] Let's give this a second and then.

[55:49] Okay.

[55:50] So we updated the contract.

[55:53] Hopefully we get something like this back.

[55:55] Uh-huh.

[55:56] Okay.

[55:57] And then add an apps object to the client options and pass the contract ID to enable

[56:03] contract name dot contract document syntax while accessing contract documents, for example.

[56:10] Okay.

[56:12] Tutorial contract dot note.

[56:14] So is this a, is this a document?

[56:16] It's like a query syntax kind of.

[56:19] Okay.

[56:20] Okay.

[56:21] Okay.

[56:22] So we're adding our contract ID here.

[56:26] Let's see if this finish.

[56:28] Oh, it did.

[56:29] Okay.

[56:30] So that looks good.

[56:31] And then I should probably be able to see that over, let's see, here.

[56:35] Okay.

[56:36] Yep.

[56:37] We have our author.

[56:39] All right, cool.

[56:42] So let's go to client JS.

[56:44] Let's just get rid of this whole thing.

[56:47] Oh, and I got to copy this actually.

[56:53] Okay.

[56:57] So I updated the client to use our contract ID, and then we're going to submit and retrieve

[57:04] documents.

[57:05] So we're going to submit our first document.

[57:07] Let's create a file that does that.

[57:11] Then we're going to put some boilerplate in that file.

[57:19] So it was called create document, submit note document.

[57:26] Okay.

[57:29] And then we're probably going to run it right?

[57:32] Okay.

[57:33] Submit note document.

[57:35] Run that.

[57:41] Okay.

[57:46] And that would appear on.

[57:47] So right now, there's no documents, but we have our schema and then documents in this

[57:51] Explorer.

[57:52] I assume we'll get it over here.

[57:53] This is where the magic happens.

[57:55] This is what makes it all worth it.

[57:57] Right?

[57:58] I actually didn't even check what we're writing over here.

[58:04] Everything good?

[58:06] Hello from a label.

[58:10] You can change that if you want.

[58:12] Oh yeah.

[58:13] You can say how to.

[58:14] Yeah.

[58:15] Whatever.

[58:16] Get crazy.

[58:17] Get crazy with it.

[58:18] Yeah.

[58:19] Yeah.

[58:20] We'll get crazy.

[58:21] We'll write another one after this.

[58:22] If I just keep running the script, it'll just keep adding new ones, I assume.

[58:26] Yes.

[58:27] And then you're also going to see how you can edit an already submitted one.

[58:32] Oh, cool.

[58:33] All right.

[58:34] I'll let this...

[58:35] It's still running.

[58:36] Yeah.

[58:37] I'll let it finish before I get too crazy here.

[58:41] Oops.

[58:45] So okay.

[58:46] So we're letting our submit document note run.

[58:49] And once this does run, you're going to want to save that document ID.

[58:53] This ID here.

[58:54] I put this in our...

[58:55] Yeah.

[58:56] Okay.

[58:57] Yeah.

[58:58] Okay.

[58:59] It should be done by now.

[59:00] Let's take a look.

[59:01] Okay.

[59:02] It looks done.

[59:03] I just want to check over here, get the validation of having it.

[59:08] All right.

[59:09] Cool.

[59:10] All right.

[59:11] And I can look at this document and I can see it grabbed my registered name, picked

[59:16] a date.

[59:17] Cool.

[59:18] That's great.

[59:19] All right.

[59:22] I could just add another one here, right?

[59:24] So I could just run this again.

[59:27] All right.

[59:30] So now we're going to do get documents again, I think we're...

[59:34] Save your document ID to your .info.

[59:36] Oh, yeah.

[59:37] Yeah.

[59:38] Sorry.

[59:39] I forgot.

[59:40] My document ID is here.

[59:45] Okay.

[59:47] And we want to go to...

[59:53] And then real quick, you go to the error that you got from trying to submit the other one.

[60:00] Scroll up just a little bit.

[60:03] Okay.

[60:05] Sometimes this just is an issue, I think, with the network.

[60:09] If I want to run it again?

[60:15] Let's go on to the edit.

[60:16] Okay.

[60:17] Next one.

[60:18] Okay.

[60:19] Get the documents first.

[60:20] Yeah.

[60:21] Okay.

[60:22] Okay.

[60:23] It was called get documents.

[60:41] And then we'll test it.

[60:45] Okay.

[60:46] So we'll get something like that.

[60:51] And then we're going to remove it or update it first.

[60:56] Okay.

[60:57] Hello.

[60:58] Great.

[60:59] Update.

[61:00] No document.

[61:01] Update.

[61:02] Update.

[61:03] Do you...

[61:04] I don't know, for your tutorial's sake, if you guys want to be going through, stepping

[61:16] through this code anymore.

[61:17] I'm kind of just going through the most...

[61:21] Yeah.

[61:22] You can take a look at it.

[61:23] We don't have to go over it too much.

[61:26] Okay.

[61:27] I mean, yeah.

[61:28] Get the gist of what's happening.

[61:30] The where part is what's important, because that's basically grabbing the ID with the

[61:34] document ID.

[61:36] And you can, in theory, use that search based on the message and other stuff.

[61:43] Okay.

[61:44] Yep.

[61:45] Okay.

[61:46] So yeah.

[61:47] Right here.

[61:48] Gotcha.

[61:49] It just loops through and gives you all of them.

[61:53] Okay.

[61:54] Actually, sorry.

[61:55] That's the get one.

[61:56] The loop.

[61:57] This is just grabs a specific message.

[61:59] Yeah.

[62:00] And so I guess, are we resetting...

[62:06] Like how are we resetting just one specific note here?

[62:09] Okay.

[62:10] That's where the document ID comes in.

[62:11] Gotcha.

[62:12] And then the document you submit has its own ID, separate from the contract ID.

[62:16] Okay.

[62:17] Okay.

[62:18] So then we probably want to run this, I imagine.

[62:25] Update.

[62:26] Okay.

[62:27] So we're going to run that.

[62:36] So we're basically adding in again to our message here.

[62:40] Yep.

[62:41] Okay.

[62:42] So our message will go...

[62:47] Forget where I was, actually.

[62:48] It was the one you were just on.

[62:49] It's this one here.

[62:50] Okay.

[62:51] Oh yeah.

[62:52] Here we are.

[62:53] So yeah.

[62:54] So change from this to hello again.

[62:57] When's this done?

[63:00] Yeah, it should be two at that point, I think.

[63:06] Oh, it appears as like that.

[63:08] It'll only be one because it's just modifying the one that was already in there.

[63:12] Okay.

[63:13] Gotcha.

[63:14] Yeah.

[63:15] Yeah.

[63:16] And then there's like, so since this is an update, I don't know how blockchains work

[63:26] with data history.

[63:28] Is this initial message scrubbed completely or is that something that stays somehow in

[63:32] history?

[63:36] It would probably remain on indexing services.

[63:42] But as far as the platform goes, it's scrubbed because you can...

[63:46] There's the state transitions that basically say, you know, submit note, like if you go

[63:51] back to your main identity page in the platform explorer where it shows like all the different

[63:57] things you've done.

[63:58] Was I there?

[63:59] Search.

[64:00] Yeah.

[64:01] Just try searching for your identity, wherever that was.

[64:06] So like grab my ID from, this identity ID here.

[64:15] Gotcha.

[64:16] Yeah.

[64:17] Okay.

[64:18] And then if I just search this here.

[64:21] Yeah.

[64:22] So you see there's all those things you've done.

[64:26] So that saves the history.

[64:28] Nice.

[64:29] Okay.

[64:30] For each state transition.

[64:31] And this is like the blockchain transactions, right?

[64:35] So like creating identity, topping up.

[64:37] Yeah.

[64:38] Okay.

[64:39] So you can click through each of those little tabs and see, let's see, I'm not sure which

[64:45] tab you clicked.

[64:46] I clicked the identity create.

[64:49] Oh, okay.

[64:51] So like click on documents.

[64:54] One of the batches or...

[64:55] Oh, documents.

[64:56] Gotcha.

[64:57] Gotcha.

[64:58] There you go.

[64:59] So this was the create.

[65:00] So this is maybe the second time I tried to create it.

[65:08] Oh, that's your dash DPNS.

[65:15] That's your dash name document.

[65:17] That was a document against somebody else's schema.

[65:21] Okay.

[65:23] A document against someone else's schema.

[65:26] Meaning the dash pay contract.

[65:28] So you didn't create the dash pay contract.

[65:31] It existed before we did this tutorial, but you created a name on that contract.

[65:37] Okay.

[65:38] And then this is the document that you created on your own contract.

[65:43] Gotcha.

[65:45] Okay.

[65:47] So we ran the update.

[65:48] We got the update.

[65:49] It looks like that's all good.

[65:54] We have our update again.

[65:57] The ID should be the same, so I don't have to update the environment variable at all.

[66:02] We got this.

[66:03] Okay.

[66:04] Now we can create, read and update our notes.

[66:06] All we have left to do is delete.

[66:07] Okay.

[66:08] So we're just going to create a new file called delete.

[66:12] And let's see here.

[66:14] Update the file, delete note document, and we will copy the boilerplate.

[66:27] Okay.

[66:31] So it's getting our document ID from our environment variable, and it's running some code here

[66:37] to run a delete action on that.

[66:41] And let's give it a shot.

[66:54] So if you haven't noticed, we're just basically doing the CRUD operations that you would typically

[66:58] do.

[67:00] Yep.

[67:03] And then, so that should affect my data over here, I'd imagine.

[67:09] We'll see.

[67:12] Okay.

[67:14] That looks...

[67:15] Oh.

[67:16] I had an error, should I try it again?

[67:23] SPV error.

[67:24] Anthony, do you know what that one's about?

[67:29] I don't think we fully...

[67:30] Yeah.

[67:31] That's the one that is usually just a network thing that I'm setting the IP address can

[67:39] help, but I don't think it's really worth it to go through that whole thing.

[67:42] Yeah.

[67:43] We'll just keep moving on.

[67:46] Okay.

[67:47] And I guess a question that's coming to mind is, what kind of applications do you expect

[67:54] to be built on the platform?

[67:56] Like, is there like a certain type that shines or is the hope that the whole internet moves

[68:01] towards building applications on a decentralized platform like Dash Platform or what's the

[68:07] goal, I guess?

[68:08] Yeah.

[68:09] Yeah.

[68:10] So, every piece of software and every platform has its niche.

[68:16] And I would say the niche for Dash Platform is where you want public data.

[68:25] Okay.

[68:26] So, first of all, public data is what it's mostly designed for.

[68:32] You can encrypt things client side and store them, store the encrypted versions on the

[68:38] platform.

[68:39] Okay.

[68:40] But if you're going to do private data, then this may not be the perfect use case.

[68:46] It may, but it may not.

[68:47] So at a high level, platform is kind of like a clean slate, you could say.

[68:54] It's just anything that you can think of.

[68:56] But in practice, I would guess it's going to be applications where you want public data

[69:02] and you want it to be provably present data.

[69:08] So you could think of a decentralized Twitter.

[69:14] I don't expect a decentralized version of Twitter to overtake Twitter anytime soon,

[69:21] let alone Dash Platform's version of that.

[69:24] However, it is possible and to the degree that Elon Musk continues to allow free speech,

[69:35] it would make decentralized versions less appealing because why do you need decentralized

[69:42] free speech if you have centralized free speech kind of thing.

[69:46] But for things that are more controversial, you might have to turn to this or something

[69:51] like that.

[69:52] But my hope is that this just makes creating applications more streamlined and easier.

[69:59] So I'm hoping to get to a point where Dash Platform is performant enough and cheap enough,

[70:11] meaning expensive, not expensive, to make it appealing to just developers who they just

[70:18] want to spin up a proof of concept and they don't want to register with yet another cloud

[70:24] service.

[70:25] They just want to dump their data on Dash Platform, just like they would dump data on

[70:33] to any other service, but you don't have to register for it.

[70:37] You don't have to put contact information in, you don't have to pull out your credit

[70:42] card and sign up.

[70:45] I just hope it makes it easier to develop applications that need some kind of global

[70:51] state storage and some kind of authentication.

[70:54] So that's why I say spa for spas, storage, payments, and authentication for single page

[71:01] applications is kind of the niche sweet spot.

[71:05] If we can nail down the performance and the cost and that's yet to be seen and we'll be

[71:13] seeing that in the coming months, whether it's cost efficient, because time is money.

[71:20] If you can do all this stuff very quickly and easily with just an SDK, then that could

[71:27] be a lot cheaper when you factor in the time it takes to spin up your own database and

[71:34] create your own server and all that stuff.

[71:36] You can just create a single page application.

[71:38] Now you've got your global state storage and auth and payments and all that stuff integrated.

[71:43] That's where I see it shining.

[71:44] Yeah.

[71:45] The first example that comes to mind for me is Wikipedia.

[71:48] It seems like it'd be the perfect thing for something like that, where it's a generalized

[71:53] public service that potentially collecting payments through donations and whatever for

[71:58] people's time.

[71:59] It seems like it'd be great for that.

[72:01] Yeah.

[72:02] But it's kind of up to the entrepreneurs.

[72:04] We're building the technology and I'm hoping the entrepreneurs will see opportunities somewhere.

[72:09] But yeah, I just always come back to those three things.

[72:13] If your application needs storage payments and authentication, and you don't want to

[72:18] create your own server and database system, this is something you should look into.

[72:22] Yeah.

[72:23] Or people with censorship oriented governments, I feel like this potentially would be a very

[72:31] liberating platform for them.

[72:36] I am of the mind that I like to have the trust built into the actual contract.

[72:45] There are great free speech platforms all over the place, but I think nothing speaks

[72:51] like the technology that guarantees those types of things.

[72:54] Yes.

[72:55] Yeah.

[72:56] It's very exciting that there is options out there for this.

[73:00] In going through this tutorial, the one thing that comes to mind is what you mentioned about

[73:03] performance.

[73:04] It does seem like certain types of applications would be fine where it's not critical, like

[73:08] real time transactions.

[73:11] Is that something that you expect to improve over time?

[73:15] Is it something with just this tutorial set up in the sandbox and we're doing it?

[73:19] Or I guess, what's the thought on that?

[73:22] The network is actually, in theory, extremely performant.

[73:27] The software is very performant.

[73:29] The issues that we've been seeing are network and SDK related, so they're not necessarily

[73:37] limits to the underlying consensus mechanisms or things like that that are at the node level.

[73:50] They have to do with like, "Oh, the SDK isn't doing retries."

[73:56] Or it's-

[73:57] Or it doesn't cache the history.

[73:58] It doesn't cache the history.

[74:00] It's contacting a node that's not really operational and it should find another one that's better.

[74:08] That kind of stuff.

[74:09] And that's all fixable pretty easily.

[74:14] We just have to look into it.

[74:15] That's actually one of the things that I'm going to be looking into this quarter.

[74:18] Great.

[74:19] And so right now, I mean, obviously some of this stuff is abstracted with some of the

[74:24] prep work that Anthony did with the scripts.

[74:27] I assume these are just like, are these like post requests, like REST requests right now?

[74:32] What's the mechanism for actually, like how does that-

[74:35] It's all gRPC under the-

[74:37] It's gRPC.

[74:38] Okay.

[74:39] Because that was my next question actually was, I was wondering if, you know, I've been

[74:42] doing some like Go development and I was just wondering if like what kind of things are

[74:46] available.

[74:47] So gRPC is what's actually being used.

[74:49] Okay.

[74:50] Yeah.

[74:51] We haven't talked to expose some of it via REST and right now we're, yeah, we are focused

[74:59] on just using the SDKs, but I would like to expose some REST endpoints on the nodes themselves

[75:07] so that it can be client independent and language independent, but that's not something that

[75:14] we've focused on yet.

[75:15] Right now, actually the best SDK to use is the Rust SDK.

[75:18] Oh, interesting.

[75:19] Yeah.

[75:20] And there's talk about whether we should just wrap that in with a JavaScript wrapper and

[75:25] use that since it's a little bit better than the JavaScript SDK or whether it's better

[75:31] to have a better, fix up the JS SDK, but we haven't decided really on that, but yeah,

[75:37] it's under the hood.

[75:38] It is mostly gRPC.

[75:39] Interesting.

[75:40] And yeah, actually that was, so my other question was like, is node the way, the only way to

[75:45] really interact?

[75:46] It sounds like Rust even has a better like way to do it.

[75:51] Other languages that are supported, Go, PHP.

[75:54] We haven't done client libraries for Go or PHP.

[75:57] The only ones we've done is JS and Rust, but if people, yeah, like that, that is kind of

[76:05] the debate right now is do we need multiple clients or do we just need one all powerful

[76:09] Rust client that has wrappers?

[76:12] So.

[76:13] Yeah.

[76:14] No, that's a great question.

[76:15] And just an aside, like as for my project that we were talking about in the beginning

[76:20] with Svelte compilations, we were at one point wondering like, okay, like if someone's doing

[76:24] this in Rust, like, could we just like call out to that instead?

[76:26] And yeah, it's hard to, it's hard to tell, right?

[76:30] Cause you know, you lose some flexibility of being able to build your API in a certain

[76:33] way, but you might just get performance and ease of use and portability across different

[76:37] technologies.

[76:38] So I think it's definitely a good debate to be had there.

[76:44] So I want to check in with you guys time-wise, are we coming up towards the end here?

[76:47] I don't know.

[76:48] Do you want to get into this Express stuff?

[76:50] What are we looking at timeline?

[76:51] Oh, I think we have another half hour actually.

[76:53] Oh, we have another half hour.

[76:54] Okay.

[76:55] Well, I think that these steps will probably only take like 10 minutes.

[76:59] Okay.

[77:00] So let's, we could, we could just go ahead and finish those real quick.

[77:04] Okay.

[77:05] All right.

[77:06] So, so it looks like we're getting into setting up a backend server with Express.

[77:10] So I'll just read here, I guess, now we've learned how to run individual scripts and

[77:15] perform all the main functionality on the dash platform.

[77:18] Like any JavaScript library, we can extend this functionality with a backend and frontend.

[77:22] Let's create an Express server that will return information on a given identity name.

[77:26] So we're basically creating a full web app to interact with the API stuff that we've

[77:30] set up.

[77:31] That's what it sounds like.

[77:32] That's what this is doing.

[77:33] We technically don't need a backend for this since the JavaScript SDK can be used on the

[77:38] client frontend itself, but, but yeah, this is how we do it in the, in the tutorial right

[77:44] now.

[77:45] And now is this like a different project entirely?

[77:47] Are we branching?

[77:48] It's all the same project.

[77:50] Yeah.

[77:51] You're going to connect to the same client file.

[77:54] Okay.

[77:55] All right.

[77:56] So install express.

[77:57] If we had more time, I'd have you build out a Svelte frontend.

[78:03] I can tell you there is, there is one actually because I built the same thing in all the,

[78:08] all the frameworks.

[78:09] I haven't run it in like a year.

[78:13] You're one of the most well-versed technologists I know.

[78:15] So I'm sure you, you've run the gamut with frameworks there.

[78:19] Okay.

[78:20] So, yep.

[78:21] So we have our server file.

[78:22] We're going to copy some boilerplate here and our server file, actually, that's in our

[78:27] API.

[78:28] Okay.

[78:29] Do you want to run through this at all, Anthony?

[78:36] Let's just, let's just blow through it as quickly as we can at this point.

[78:41] You know how an express server works.

[78:43] Okay.

[78:44] Yep.

[78:45] So we're going to run it.

[78:46] Yeah.

[78:47] It's just creating an end point for the name specifically.

[78:50] So your, whatever name you give the end point, it'll feed in as basically the query.

[78:56] So the whole page will return the output.

[78:59] Is that not what I want to do?

[79:05] Yes.

[79:06] There's a curl.

[79:07] Go back to the tutorial.

[79:08] It'll tell you the specific.

[79:10] Gotcha.

[79:11] Oh, okay.

[79:12] All right.

[79:13] So we're going to.

[79:14] Yeah.

[79:15] So it's localhost 2001 for slash name for slash Jim, whatever you're using.

[79:22] Okay.

[79:23] Gotcha.

[79:24] Cool.

[79:25] All right.

[79:26] Wow.

[79:27] Beautiful.

[79:28] Did you design this?

[79:29] Nice.

[79:30] This is great.

[79:31] Okay.

[79:32] Yeah.

[79:33] And then the next step is just a next step that fetches from that end point.

[79:44] Cool.

[79:45] All right.

[79:46] By the way, Jimmy Wales, the, one of the original creators of Wikipedia has like this vision

[79:54] of creating a new Wikipedia that is blockchain enabled.

[79:57] So you're actually right on the money with that.

[79:59] I think I, I actually think I might've saw an interview with him about that.

[80:03] So that might be.

[80:07] He's next on the platform walkthroughs.

[80:09] Oh yeah, nice.

[80:12] Yeah.

[80:13] That'd be cool.

[80:15] Yeah.

[80:16] I don't know what his intention there is leveraging an existing project or what, but it would

[80:23] be nice to, yeah.

[80:24] Get more people rowing in the same direction, right?

[80:27] Yeah.

[80:28] Yeah.

[80:29] Okay.

[80:30] Oh, I didn't, I didn't look at what you wanted me to put in.

[80:34] I just did all the defaults.

[80:35] Hopefully that's.

[80:36] Yeah, that's fine.

[80:37] Okay.

[80:38] And you can actually skip this part and just go to the next, cause this just sets you up

[80:44] with your main app.

[80:45] You can just, so scroll down a little further to the page JS, it'll give you all the, all

[80:50] the logic.

[80:51] Okay.

[80:52] This stuff here.

[80:53] Yeah.

[80:54] Yeah.

[80:55] Just grab that one.

[80:56] Okay.

[80:57] Cut to the chase.

[80:58] Get the good stuff.

[80:59] All right.

[81:00] XR is.

[81:01] Oh, did you not want a TypeScript?

[81:02] It's fine.

[81:03] Okay.

[81:04] Yeah.

[81:05] So just blow all that away.

[81:06] Okay.

[81:07] And then you're going to need a.env.local file with your name.

[81:08] Okay.

[81:09] And then you're going to need a.env.local file with your name.

[81:10] Okay.

[81:11] And then you're going to need a.env.local file with your name.

[81:12] Okay.

[81:13] And then you're going to need a.env.local file with your name.

[81:14] Okay.

[81:15] And then you're going to need a.env.local file with your name.

[81:16] Okay.

[81:17] And then you're going to need a.env.local file with your name.

[81:21] Okay.

[81:22] And that's going to be inside of your next project.

[81:26] Okay.

[81:27] And that's going to be inside of your next project.

[81:28] Okay.

[81:29] This, this here.

[81:30] Yeah.

[81:31] Okay.

[81:32] Yeah.

[81:33] Okay.

[81:34] All right.

[81:35] So we have.

[81:36] All right.

[81:37] So we have.

[81:38] So I have to create one here?

[81:41] Yeah.

[81:42] Okay.

[81:43] Yeah.

[81:44] Okay.

[81:45] Sorry.

[81:46] Yeah.

[81:47] Okay.

[81:48] Yeah.

[81:49] Okay.

[81:50] Okay.

[81:51] Okay.

[81:52] Okay.

[81:53] And.

[81:54] And then just same label that you were using.

[81:56] And then CD into the next directory and run NPM run start.

[82:01] Okay.

[82:02] Okay.

[82:03] All right.

[82:12] Sorry, not start.

[82:16] NPM run dev.

[82:17] Yeah.

[82:18] Sweet.

[82:19] Okay.

[82:20] And then localhost 3000.

[82:21] Okay.

[82:22] Oh, it wants to go to Firefox.

[82:23] How about that?

[82:24] Whoops.

[82:25] That's it.

[82:26] We're running a different application there.

[82:27] Do you know what?

[82:28] I thought I had stopped.

[82:29] Stop that.

[82:30] Maybe it's cache.

[82:31] Okay.

[82:32] Let me see here.

[82:33] Okay.

[82:34] That seems to be fine.

[82:35] Okay.

[82:36] That seems to be fine.

[82:41] Let me just open a browser and go to choose a different port, man.

[82:50] That's the next default.

[82:53] It's definitely not super convenient.

[82:55] Let's see if I can get us there.

[82:58] Okay, here we are.

[83:01] I think it's not getting your identity.

[83:06] Oh, I know why.

[83:09] Go look at your page again.

[83:12] Okay.

[83:13] Page.tsx.

[83:15] Next public label.

[83:17] Is that the correct thing?

[83:25] Oh, local.

[83:27] Oh, yeah.

[83:28] What am I saying?

[83:29] Does it translate it behind the scenes from next or?

[83:33] Yeah, that's fine.

[83:35] Yeah.

[83:36] Next public label.

[83:38] Next.

[83:39] You might have to restart your express server.

[83:41] Are you still running the express server?

[83:43] Maybe I didn't save that.

[83:44] Let me just try that again.

[83:45] Oh, I turned my express server off.

[83:47] Should that be running?

[83:48] Yeah.

[83:49] So that needs to be running.

[83:50] Yeah.

[83:51] Okay.

[83:52] I forget what we were actually, how we were running that.

[83:54] Was it?

[83:55] No, just npm run express.

[83:59] Okay.

[84:00] There we go.

[84:01] Okay.

[84:02] All right.

[84:03] Give it a second.

[84:08] I'll restart your, oh, there it is, actually.

[84:10] Yeah.

[84:11] There you go.

[84:12] Sweet.

[84:13] And there's your app.

[84:14] Hey, it looks good.

[84:15] It got a background color.

[84:16] Is it?

[84:17] It's got like a fade to it.

[84:18] I like it.

[84:19] It's the next default, I guess.

[84:22] Oh, yeah.

[84:23] Nice.

[84:24] Cool.

[84:25] So that's it.

[84:26] Wow.

[84:27] You just built a dApp.

[84:31] You built a dApp.

[84:32] There you go.

[84:33] I mean, yeah, I think a lot of that was just going over core concepts, which was super

[84:37] helpful for me.

[84:38] But honestly, it wasn't so strenuous of a thing to get up and running with a completely

[84:43] new paradigm that I'm used to.

[84:46] So I think that's great.

[84:47] I think this is, well, thank you both for taking the time to show me.

[84:51] And also, Anthony, I think this blog post is awesome.

[84:54] You did a great job.

[84:56] Thanks.

[84:57] Yep.

[84:58] Cool.

[84:59] Yeah, we have another stream coming up soon here.

[85:04] So I think we'll jump off here.

[85:07] And thanks, Jim.

[85:08] It was a pleasure to meet you.

[85:10] And maybe we can stay on the show for a little bit after we go off to the live show.

[85:16] Sure.

[85:17] And we'll get you squared away.

[85:18] And for everybody else, tune in probably 15, 20 minutes or so for the next show.