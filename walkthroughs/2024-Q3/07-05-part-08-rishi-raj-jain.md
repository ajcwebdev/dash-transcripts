---
showLink: "https://www.youtube.com/watch?v=geUc_aHJu-0"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Platform Walkthroughs Part 8 - Rishi Raj Jain"
publishDate: "2024-07-05"
coverImage: "https://i.ytimg.com/vi/geUc_aHJu-0/sddefault.jpg?v=66878c7f"
---

## Episode Description

Rishi Raj Jain explores Dash Platform, creating a wallet, identity, and basic app using Node.js, Express, and Next.js, demonstrating blockchain interactions without prior crypto experience.

## Episode Summary

In this walkthrough, Rishi Raj Jain, a developer with no prior cryptocurrency experience, explores the Dash Platform under the guidance of the host. They create a wallet, establish an identity, and build a basic application using Node.js, Express, and Next.js. The process demonstrates how to interact with the Dash blockchain, covering topics such as wallet creation, identity registration, data contracts, and document management. Despite encountering a few technical issues, Rishi successfully completes most tasks, gaining insights into blockchain development and discussing potential use cases for the technology.

## Chapters

00:00 - Introduction and Developer Background

Rishi Raj Jain introduces himself as a developer from India with experience in Angular, TypeScript, and various web technologies. He discusses his recent project, LaunchFast, which provides starter kits for Next.js, SolidJS, and Astro. The conversation touches on his limited experience with cryptocurrency and sets the stage for exploring the Dash platform.

04:35 - Overview of Dash and Blockchain Basics

The host provides a brief explanation of Dash, its origins as a Bitcoin fork, and its focus on payments and low transaction fees. He introduces the concept of the Dash platform, which adds identity and storage layers to the cryptocurrency. The discussion covers basic blockchain concepts such as decentralized ledgers, nodes, and consensus mechanisms, preparing Rishi for the hands-on tasks ahead.

08:49 - Setting Up the Development Environment

Rishi begins setting up the development environment by creating a new Node.js project, installing the Dash SDK, and configuring the necessary files. They discuss the use of ESM modules and the current state of the Dash platform, which is preparing for its mainnet launch. This chapter covers the initial steps required to start working with the Dash platform.

13:15 - Creating a Wallet and Obtaining Test Dash

The walkthrough continues with creating a wallet on the Dash testnet. Rishi generates a mnemonic phrase and address, learning about the importance of keeping these secure. They then use a testnet faucet to obtain test Dash, experiencing some technical difficulties with the faucet website. The host explains the concept of block explorers and how to verify transactions.

25:30 - Identity Creation and Management

Rishi creates an identity on the Dash platform, learning about the process of registering a name and topping up the identity with credits. They explore the platform explorer to view the created identity and its associated transactions. This chapter demonstrates the key steps in establishing and managing a digital identity on the blockchain.

36:35 - Data Contracts and Document Management

The tutorial progresses to creating data contracts, which define the structure of data to be stored on the platform. Rishi implements functions to register, retrieve, and update contracts. They also create and manage documents within these contracts, learning about the relationship between contracts, documents, and the blockchain structure.

47:26 - Building a Simple Web Application

Rishi creates a basic Express server to expose an endpoint for retrieving identity information. He then builds a Next.js application that interacts with this endpoint, demonstrating how to integrate Dash platform functionality into a web application. This chapter covers the practical aspects of building a user-facing application that leverages blockchain data.

59:05 - Reflections and Potential Use Cases

As the walkthrough concludes, Rishi and the host discuss potential applications for the Dash platform. Rishi proposes an idea for a Splitwise-like expense tracking app using the platform's document management capabilities. They also touch on the security considerations in blockchain development and the potential for integrating Dash payments into existing applications.

65:49 - Exploring LaunchFast and Future Developments

The final segment shifts focus to Rishi's project, LaunchFast. He demonstrates the features of his starter kit, including authentication methods and database integrations. They discuss potential improvements, such as incorporating Astro's upcoming content layer and exploring cryptocurrency payment integrations with Stripe.

## Transcript

[00:00] All right.

[00:02] Hello, everyone.

[00:03] Welcome to part eight of the Dash walkthroughs.

[00:07] We got one of my former coworkers, Rishi, who I met, I think I met you before, actually,

[00:13] I was working at Ezio, but that's where we got to know each other better.

[00:17] And you kind of went solo, I think, and you do, you have this project that is under your

[00:24] name.

[00:25] But why don't you introduce yourself and talk a little bit about, you know, your dev background

[00:29] and what you're doing.

[00:30] Sure.

[00:31] Thank you for having me on the stream.

[00:33] I am Rishi from India.

[00:36] And the dev experience always starts from building starting websites to so the first

[00:42] thing that I learned in my dev experience was Angular with TypeScript.

[00:45] And so that was a whole lot of learning.

[00:47] And so that made, you know, switching between frameworks much easier, I would say.

[00:52] Recently, I launched LaunchFast, which is a collection of starter kits in Next.js, SoilKit

[00:57] and Astro, I am pushing, you know, new integrations every day.

[01:01] And in the last two days, I've added AWS S3 as the storage provider and Cloudflare R2

[01:10] as another.

[01:11] So I'm really pushing into being the right starter kit for you to get started.

[01:17] Do you have payments integrated with any of them?

[01:20] Yes, I have Stripe and Lemon Squeeze integrated in both of them with the webhooks and checkout

[01:25] support.

[01:26] Lemon Squeeze.

[01:27] I don't know if I know that one.

[01:30] I'll have to check that out.

[01:33] But yeah, that's one of the things I'm like, ooh, we should have you build in a Dash integration

[01:37] for it.

[01:38] But that would be its whole own stream.

[01:41] But so we've been doing, you know, you're number eight, so you'll be the eighth person

[01:45] to do this.

[01:47] We're bringing devs on to kind of try out Dash platform, which is actually first, what's

[01:52] your experience with crypto?

[01:55] I have literally no experience with crypto.

[01:57] I do have friends who are enthusiastic about it, but I have no experience.

[02:01] Okay, cool.

[02:02] Yeah.

[02:03] Well, then this will be good.

[02:04] You'll be going in totally fresh.

[02:07] You probably at least heard of Bitcoin, I would assume.

[02:10] Yeah, I've heard of it and its fluctuating rates.

[02:13] That's all I've heard.

[02:14] Sorry, I didn't hear what you said.

[02:16] What about Bitcoin?

[02:17] What I've heard is there's Bitcoin and it's been fluctuating quite up and down.

[02:24] And that's all I know about it.

[02:26] Yeah.

[02:27] Yeah.

[02:28] The price is very volatile.

[02:29] And that's, for crypto in general, it was such a huge problem.

[02:31] They had to invent a new type of cryptocurrency that was called a stable coin that would specifically

[02:36] not change in price, it would be pegged like the US dollar.

[02:39] But Dash was originally a fork of Bitcoin.

[02:44] And it evolved because Bitcoin evolved to be more of what you call a store value, where

[02:50] it's like you own a big hunk of gold, you're not going to parse that to pieces and go out

[02:56] and spend them or that kind of thing.

[02:58] So Dash was more like, we want this to be a way to do payments.

[03:02] So you can use it to buy all sorts of stuff and has extremely low transaction fees.

[03:07] So if you're doing cross-border payments, you're really good for that.

[03:10] So that's cool.

[03:13] And then that's been around for 10 years or even longer.

[03:17] And now there's been this five to seven year long development of the Dash platform.

[03:24] And that is probably pretty easy to explain, actually, because you know enough about web

[03:28] apps.

[03:29] It takes the currency and the ability to transact with people, it adds an identity layer and

[03:35] a storage layer.

[03:37] So that now you can actually have your own specific identity that you could make public

[03:41] or private, and you could transact with people privately, and that you can also store kind

[03:46] of JSON-like blobs in there.

[03:49] So if you wanted to have an app that had user-generated content, you could do all of that.

[03:56] So does that all make sense so far?

[04:00] Yeah, totally.

[04:02] Sounds new and cool, yeah.

[04:07] So the most important thing to really know about working with blockchain is that the

[04:11] way it works and the way it's able to secure your funds is by having the ledger itself

[04:19] and everyone's balances decentralized across various computers.

[04:24] So it's kind of like if you ever downloaded movies on BitTorrent or something like that,

[04:30] you know, once you download the movie, you got the seed and then other people can seed

[04:33] from you.

[04:34] So it's kind of like that.

[04:35] You got all these nodes, and they each have ledgers and they have transactions made, it

[04:40] gets added to a new block, and then once a block is full and enough blocks have been

[04:45] confirmed, they all come to a consensus, and then it's said, "This is the canonical block.

[04:48] Now we go to the next block."

[04:50] And that's what the blockchain is.

[04:52] So the challenge with that is it is the same challenge as a decentralized system where

[05:00] sometimes the network will just get confused or slow, and sometimes you'll hit a bad node.

[05:07] So if you want to put that out there, except it may or may not happen, we'll see.

[05:10] I haven't tested the network today, so I have no idea what's going to happen, but that's

[05:13] kind of the fun of doing these live streams.

[05:16] So we should probably get into it now if you want.

[05:21] Yeah, let's get started.

[05:25] Sweet.

[05:26] So let's get your screen sharing, and you'll probably want like your code editor on like

[05:33] one side, the blog post on the other side, so you can kind of just scroll along.

[05:39] Yeah, let me share my screen.

[05:42] So yep.

[05:44] Cool.

[05:45] Does this look correct?

[05:49] Yeah, and do it the other way so that the blog post is a little smaller than the code

[05:54] editor.

[05:55] Ah, I see.

[05:56] How do I switch?

[05:57] I really don't know.

[05:58] I'm just going to...

[05:59] Drag them.

[06:00] Yeah, just drag them.

[06:01] Yeah.

[06:02] That should be good.

[06:03] I would say bump up your font in each of them like one or two times.

[06:09] In the code editor?

[06:10] Yeah, let's do one up in the code editor, and then two up in the browser.

[06:14] Got it.

[06:15] Cool.

[06:16] And then you can start at the setup and configure node project, that's where the code actually

[06:22] starts.

[06:23] Yeah, this one.

[06:24] That's the one.

[06:25] Cool.

[06:26] So, what I have right now is node 20, this one, correct?

[06:35] Yeah.

[06:36] So, I'm going to create a directory, I already have, and then I create a package.json, and

[06:46] then I'm setting up the type module, so we are operating on ESM.

[06:53] That's right.

[06:54] And then we're installing a dash version, which is in dev, all right?

[07:01] Yeah, and that's because, like I said, they've been working on this for years and years and

[07:04] years and years, but what's funny is actually they're launching the first kind of official

[07:11] mainnet version in probably two months or so, and then the SDK that you're using is

[07:17] going to be an alpha version, so it's going to go from dev to alpha, then eventually a

[07:22] beta, and the network will then get more stable as the new versions go up.

[07:27] Makes sense.

[07:28] Makes sense.

[07:29] All right, so I'm going to do the next step, which is add the .gitignore while it installs.

[07:35] So, copy there, yep.

[07:39] We will create each script file individually throughout the tutorial, but for the sake

[07:43] of simplifying life, while following along this tutorial, I would recommend adding...

[07:47] All right, yeah.

[07:48] Sounds good.

[07:49] Yeah, so then you'll get, so you're going to basically build each of these files, scripts

[07:54] individually, but then you'll just be able to run the command after you've done that.

[07:58] Got it.

[08:00] Let this install command complete, and then we can add the scripts.

[08:05] Cool, yeah.

[08:06] While that's going, you can go to the next step and create some of the first files and

[08:10] directories if you want.

[08:11] I'm going to create two directories, which is api and script, and then in api, I am going

[08:25] to create a client JS.

[08:29] How's the internet connection in India?

[08:32] I am not sure what's happening though, but yeah.

[08:36] This tends to happen when I'm streaming as if I were trying to do anything involving

[08:43] NPM.

[08:44] It goes very slow.

[08:45] No worries.

[08:46] I am still proceeding with the rest of the parts.

[08:48] It's good for now.

[08:49] Let me copy this.

[08:50] So, we installed the dash module.

[08:53] We are using dash module.

[08:55] We get the process in V, and then we specify client on the current network.

[09:00] The network is testnet.

[09:01] Yeah, I've heard this as well.

[09:02] There are two, correct?

[09:03] Testnet and mainnet, if I'm not mistaken.

[09:04] Yes, and that's what I was saying.

[09:08] You cannot do this on mainnet today, but you will be able to in like two months.

[09:13] Got it.

[09:14] And this also means all the money is pretend money.

[09:16] So, like you're going to get some dash, you're going to spend some dash, but it's not a real

[09:19] dash.

[09:20] Whereas like a dash, like one dash is like $25 or something right now.

[09:25] Okay.

[09:26] Cool.

[09:27] So, we create a script, which is create wallet JS.

[09:32] Do that.

[09:33] So, what we're doing is creating a wallet.

[09:36] Finally, it installed.

[09:37] That's great.

[09:38] Let me quickly jump to my package steps and JSON, replace what we have in here.

[09:50] What we're doing in here is we are basically running the scripts that we will add.

[09:54] Okay.

[09:55] So, we're just going to run for running the API server.

[09:58] Makes sense.

[09:59] All right.

[10:00] Sounds good to me.

[10:01] Let me add the create wallet.

[10:04] So, we get the wallet.

[10:08] I have no idea what this is doing.

[10:11] And then we get the address for this particular thing.

[10:13] And then we're just logging them on.

[10:15] Makes sense to me.

[10:16] Yeah.

[10:17] I'll have you run it first, and then I'll explain kind of what happened.

[10:19] All right.

[10:20] Let me do npm run create wallet now.

[10:23] And now I own your computer.

[10:24] No, I'm kidding.

[10:25] Okay.

[10:26] So, for this, you have two things.

[10:29] The mnemonic is a 12-word seed phrase.

[10:32] And that is kind of like your password is basically how you think about it.

[10:35] So, since this is on testnet, all the funds are made up.

[10:38] It doesn't matter that it's on a stream.

[10:40] But when you have a real wallet, you have real money in, you never, ever want to expose

[10:45] this.

[10:46] Because anyone who has this can take all your money.

[10:47] And then the address is going to be if you want to transact with someone, that's the

[10:52] thing.

[10:53] So, if I want to pay you $10 because you bought me a coffee the other day, you would send

[10:58] me that address.

[10:59] And then I would go into my Dash wallet, put in that address, and say, give a half a Dash

[11:04] or something to him.

[11:05] Got it.

[11:06] So, it's like...

[11:07] Yeah.

[11:08] Mm-hmm.

[11:09] Yeah.

[11:10] And every time you have a command where it outputs something that looks like this, you're

[11:14] going to want to copy, paste, and put into your .env, because this will be integrated

[11:18] into the following commands as you go.

[11:21] Okay.

[11:22] Let's put them here.

[11:24] Great.

[11:25] Done.

[11:26] Yeah.

[11:27] So, we have copied them into .env, and now we have to add funds to my fake wallet.

[11:35] So, how do I go about this?

[11:42] How do I go about this?

[11:45] You can check the status information.

[11:47] Yeah.

[11:48] There's two links in here.

[11:49] First, go to the testnet faucet, so open that guy up.

[11:53] And then this site is notoriously awful and flaky, so you're going to have to continue

[11:58] through that.

[11:59] Yep.

[12:00] And so, grab that address and put it into the top field.

[12:05] The one that was...

[12:06] No, not...

[12:07] Sorry.

[12:08] Not that one.

[12:09] The one that's in your terminal.

[12:10] Yeah.

[12:11] Got it.

[12:12] Got it.

[12:13] So, this one is what I put in here.

[12:14] And don't put it there.

[12:15] That's the promo code.

[12:16] I absolutely hate this website.

[12:17] I do.

[12:18] I do.

[12:19] I'm not going to put it in here.

[12:20] You're not the first one to do that.

[12:23] Don't worry.

[12:24] And then click get coins, and then wait for the site to crash.

[12:30] And then we'll be good.

[12:31] Okay.

[12:32] Like, one out of ten times, it will give a message saying, "You now have one and a half

[12:38] dash."

[12:39] But nine out of ten times, the site crashes, and that means it completed.

[12:45] Something that needs to be fixed in here is for sure.

[12:47] Yeah.

[12:48] Yeah.

[12:49] Yeah.

[12:50] Yeah.

[12:51] Totally.

[12:52] And what this is doing...

[12:53] So, a faucet, a testnet faucet.

[12:54] That's good.

[12:55] That's what we want.

[12:56] The testnet faucet is just a way to load up some dash.

[12:59] And so, like I said, it's all pretend dash.

[13:02] So, this is not just, like, a pile of money sitting on the internet.

[13:05] It's a pile of fake money that everyone can kind of pull in if they want to test out different

[13:09] functionality.

[13:10] Because next thing we're going to do is we're going to create an identity, and that requires

[13:14] dash to do.

[13:15] So, don't even...

[13:16] Yeah.

[13:17] Are you trying to go to the block explorer?

[13:20] Was that the one that...

[13:21] Okay.

[13:22] So, we're done here?

[13:23] Yeah.

[13:24] You're done.

[13:25] We're done with the faucet.

[13:26] Yeah.

[13:27] So, go to the next link, the dash block explorer.

[13:28] Sure.

[13:29] And then now...

[13:30] Let's see.

[13:31] Try...

[13:32] Okay.

[13:33] Yeah.

[13:34] I think now it's starting to load.

[13:37] Yeah.

[13:38] Yeah.

[13:39] And then the same address, you're going to put that very top field and search for it.

[13:44] In here?

[13:45] Uh-huh.

[13:46] And so, what this is, this is like a UI to the blockchain itself, is what a block explorer

[13:53] is.

[13:54] So, when you have a transaction that's on the blockchain, you can go look at it through

[13:59] a block explorer.

[14:00] So, you don't have to access it through like an RPC endpoint or something like that.

[14:04] You can just have this nice kind of front end.

[14:06] And if you see here, you don't have dash, but it does say you have unconfirmed dash.

[14:11] That means that it's the transaction is being added to a bunch of blocks and they all need

[14:17] to come to consensus eventually, and then you'll have your dash.

[14:19] But this is good.

[14:20] We can move on because you have the stuff to make the identity.

[14:25] So, we have searched for the wallet and then we are...

[14:31] It needs to click on my transaction link, which I think I can skip for now.

[14:37] We can skip those parts.

[14:38] Yeah.

[14:39] So, you'll have your wallet, which will be on the block explorer that every individual

[14:42] transaction will have its own specific transaction ID with like some steps of what happened in

[14:48] the transaction.

[14:49] Got it.

[14:50] All right.

[14:51] Let's create the identity for this.

[14:52] It should be in here.

[14:53] So, to create an identity, we will run .register.

[15:02] All right.

[15:03] So, this is pretty easy to understand.

[15:05] I believe I'm creating my own identity on the platform.

[15:09] Yep.

[15:10] This is going to give you an identity ID.

[15:14] And then just run this, you get...

[15:17] And this takes usually about 15 to 20 seconds to go through.

[15:24] So, the identity ID will then be associated with a name, and the name...

[15:31] Did you ever see a couple of years ago, a lot of people had .eth after their Twitter

[15:36] names?

[15:37] Yeah, yeah, yeah.

[15:38] Yeah.

[15:39] So, that was like an Ethereum namespace.

[15:42] It's both a namespace and a wallet, so that if so...

[15:45] I had ajcweb.eth.

[15:46] And if someone wanted to send me some ETH, they could just plug that in and send it because

[15:51] I bought that.

[15:52] So, the name is going to be the dash, versus that you'll have rishi.dash or something like

[15:59] that.

[16:00] Yep.

[16:01] I'm just waiting for this to give me some...

[16:05] This is always the fun part.

[16:07] Okay.

[16:08] So, I can explain this in the next fraction.

[16:12] So, then we're going to have a slightly different explorer, we're going to go to the platform

[16:16] explorer, which is actually really nice.

[16:18] And it's...

[16:20] Because I was saying how we had the original dash, which was just the wallets and the payments

[16:25] kind of thing, and now platform has identities and storage, the platform explorer is going

[16:32] to expose those things.

[16:34] So, this identity ID you're creating right now, that wouldn't be in the first block explorer

[16:39] because that's not part of the original dash system.

[16:43] It's part of the dash platform system.

[16:45] And this is something that I only really know this at a high level, so...

[16:49] Yes, it works!

[16:50] Yes, it works!

[16:51] Oh my god, that means the rest of the stream is going to go so much better.

[16:54] All right, I'm going to kick back now and let you do your thing.

[16:58] So, I have added the identity ID to my ENV.

[17:02] And put that link that it gave you too, in your terminal, there's a link right there,

[17:08] you can click.

[17:09] Oh, okay.

[17:10] I see.

[17:11] So, basically, this is going to open the particular link that I'll be getting from these steps.

[17:18] Yeah.

[17:19] And...

[17:20] All right, let this open up.

[17:24] We have an identifier, some balance for me, and then write time, and then we have a transaction

[17:33] that has been performed already, and that transaction is creating the identity, correct?

[17:37] That's right.

[17:38] All right.

[17:39] Sounds good.

[17:40] And then for creating my identity, I got this much credits.

[17:46] Yeah, so the credits are the very next part of the blog post explains this, I always forget

[17:53] the conversions, because there's like hundreds of millions of something is a something and

[17:58] then there's a thousand of another thing.

[18:00] So, you have credits and duffs, which are both, one is like a hundred million dash and

[18:05] one is like a billion dash or something like that.

[18:08] These numbers are definitely wrong, but that's kind of the gist of it.

[18:12] All right.

[18:16] Let me create the retrieval of my identity.

[18:19] So, what this is doing is getting the wallet, getting the identities, and for all of what

[18:27] it detects, it's trying to print the balance of them.

[18:30] Yeah, this is your read or your get.

[18:33] You'll notice almost every commander you create is basically going to be some part of a crud

[18:37] operation.

[18:38] Okay.

[18:39] And this is going to take the same time, I'm going to skip this for now.

[18:45] Let's see what it comes back with.

[18:48] Let me create top of identity, which is probably going to add some balance.

[18:54] Let's add this script.

[18:57] What's it doing here is getting the wallet, getting the IDs, and then it's trying to top

[19:01] up with this much of credits.

[19:05] And then identity credit balance, but this ID is, so once it has topped the account,

[19:11] it will try to print it.

[19:15] Yeah.

[19:16] And so, the reason why this needs to be done, this took me so long to understand, is because

[19:22] you have the dash, which you got from the faucet, but then your identities are on the

[19:27] platform for them to do things.

[19:29] You have to turn some of that dash into credits and then give it to the specific ID.

[19:34] Yeah.

[19:35] Got it.

[19:36] Makes sense.

[19:37] All right.

[19:38] So, let me run this.

[19:41] I think this should be done after this is done.

[19:45] Yeah.

[19:46] This has come up.

[19:49] So yeah.

[19:50] This happens sometimes.

[19:51] So, this is the type of error that we get occasionally on the create identity, and it

[19:56] totally nerfs everything.

[19:57] This means you hit a bad node, basically.

[19:59] There's a way to go into your client to give a specific node, but we don't really need

[20:03] to do this command.

[20:04] We're just reading back the identity we just created.

[20:06] So, let's just skip this one.

[20:07] This one breaks half the time anyway, so it is what it is.

[20:13] I know the exact percentage of times specific things break, because I've done this so many

[20:20] times.

[20:21] No worries.

[20:24] Things are meant to be broken in software, so it's fine.

[20:29] Yeah.

[20:30] And hopefully, once we get to mainnet, things will be a little more stable, because it's

[20:36] hard to really have an incentive to make sure the testnet is always up.

[20:40] Just like, "Oh, you can't get your pretend money right now?

[20:43] Sorry."

[20:44] So, let's just now try to top up my identity and see what it comes back with.

[20:56] Meanwhile, I'm going to create another script that I can run and then wait for.

[21:02] So, we have register name, and then create a label in your ENV with your desired name.

[21:10] See the implementation videos for naming constraints.

[21:12] Okay.

[21:13] So, I have to name something in my ENV.

[21:15] So, I'll just go to my ENV, and then I'm going to say, "Label."

[21:21] So maximum length is 63, and then 0 to 9, E to Z.

[21:25] You're the first person to go to this section and actually read this part.

[21:31] I actually love documentation, so I always try to go to the links that I see in the blog.

[21:37] I didn't see some of them before, but I do.

[21:39] You've followed every line and read them all out.

[21:43] You're dialed in.

[21:44] I can totally tell.

[21:45] Yeah.

[21:46] All right.

[21:47] So, I have to have numbers, hyphen, and characters.

[21:52] Sounds good.

[21:53] Let me do something I don't know.

[21:56] Let's name it on my label.

[22:01] Does this look correct as a label?

[22:03] So, I think it says that it cannot be at the end, so that's where it says the note.

[22:09] Ah, I see.

[22:10] So, a prefix or suffix is not allowed.

[22:13] Yeah, that's good.

[22:14] Were you born in 1990?

[22:15] No.

[22:16] No, I'm 2000.

[22:17] Okay, what's the 94?

[22:18] I just picked this up.

[22:19] These two numbers.

[22:20] I had no idea.

[22:21] Cool.

[22:22] I thought people would do the year they were born or something like that, you know?

[22:31] Got it.

[22:32] So, yeah.

[22:33] Identity credit balance.

[22:34] It comes up fine, and I do have some credits.

[22:37] We have created the label, which is great.

[22:41] Where is the script for register name?

[22:42] Okay, there it is.

[22:43] It's right there.

[22:44] Yeah, it's the next part.

[22:45] So, what it's trying to do is get my identity based off the env will make sense, then we

[22:53] get the ID, get the name, and then what it's trying to do after that.

[23:01] So, it's trying to register based on my dash label, and it's just printing my label.

[23:08] Is that correct?

[23:09] Or is this going to be something different?

[23:11] It's going to, yeah, so it's just going to give you the same label you already have to

[23:16] confirm that it worked, and it's also going to give you a link to see it on the block

[23:20] explorer.

[23:21] Got it.

[23:22] Yeah.

[23:23] And the link to it.

[23:24] Got it.

[23:25] Makes sense.

[23:26] Do you know much about JSON schema?

[23:33] I have heard of it.

[23:35] It's basically, you define how would a JSON basically look like.

[23:44] Because if you look over at the end of this console log, so just scroll to the right a

[23:47] little bit in your code editor, in the code part.

[23:52] In the core part.

[23:53] Okay, got it.

[23:54] Yeah.

[23:55] So, how it's name registration dot to JSON with the dollar sign ID.

[23:59] This is something that took me so long to figure out, and I kept getting undefined and

[24:03] stuff.

[24:04] I don't know what's going on.

[24:05] So this has to do with JSON schema, which I don't really know anything about.

[24:09] Got it.

[24:10] Yeah, those are usually the links of what the schema JSON is, and then it gets configured

[24:16] during, picked during the run time, whether in editor or when you're deploying something.

[24:22] I have seen this in probably sharedCN being used, or in another project.

[24:28] But yeah, I've seen JSON schema before.

[24:31] Cool.

[24:32] All right, so this is going to wait for some time, but we know what it's going to say.

[24:37] So let's create a script for retrieve name now.

[24:41] Retrieve name, yes, and then paste this here.

[24:48] What this is trying to do is pick up my label and get the document associated.

[24:54] That will be probably just getting out from this one.

[24:59] And yeah, all right, so I've got this.

[25:01] If I click on this thing, it has some identifier, the owner ID, and then it has my label.

[25:11] Sounds good.

[25:12] So now this is kind of both, this is the identity part, and it's also already the data storage

[25:19] parts.

[25:20] Like, you need your own kind of account information saved in there.

[25:24] So now you got this.

[25:25] This is your identity on the Dash platform.

[25:29] Got it.

[25:30] What's this normalized label?

[25:31] Like, probably this is for internal use, but it's somehow changed my eyes to one.

[25:36] Yeah, this is a very specific security thing, and that takes out basically attack vectors,

[25:43] so people wouldn't accidentally put like a zero for an O or a one for an I or something

[25:48] like that.

[25:49] So it's like, I think that's also why it's like 58 base instead of 64.

[25:56] So yeah, we have added the script part between name.

[26:02] Let's do that.

[26:03] Right.

[26:04] And that's going to give you back basically the exact same thing you just saw.

[26:08] The thing that we saw here.

[26:09] Yeah, yeah, yeah.

[26:10] It makes sense.

[26:11] Makes sense.

[26:12] Okay, so it did give me those.

[26:13] We should see label and normalized label.

[26:16] Yeah.

[26:17] All right.

[26:18] Makes sense.

[26:19] Now we come to data contracts, a data contract on Dash, so there's a blueprint for the data

[26:26] that is intended to be stored, it defines a JSON schema as you're talking about.

[26:32] So contracts enable the platform to validate, they're crucial, and they're used for runtime

[26:38] retrieval.

[26:39] Okay, so this is basically going to look at the data that we just saw pertaining to my

[26:43] ID.

[26:44] And it's going to allow you to create your own kind of data blob that you want.

[26:50] So your name was already predefined, and they already had a schema, whereas you're going

[26:56] to now be able to define, if you wanted to write hacker news, you would be creating users

[27:02] with posts that can make comments on other posts.

[27:04] This is going to be just a single string with some texts that will have an author.

[27:11] So there's going to be very, very little actually happening here.

[27:14] But it's like the, again, this is, you need to, it's kind of like this, this part is hard

[27:20] to map to CRUD exactly, so you have to first create the data contract, which defines the

[27:25] kind of data you're going to give it.

[27:27] And then you create a document, which is the actual data that the data contracts understand.

[27:32] So that will make sense once we do this.

[27:35] Yeah, I think it does.

[27:37] We're just defining what will be incoming, and then we said what is incoming, and then

[27:41] we're sending a document, which is what is bound to receive, like, we have configured

[27:48] here, this is what will be coming to you, and then we are, let's say, doing a put operation

[27:53] of the schema that we have defined.

[27:56] So that's what I understand, I believe.

[27:58] Yeah, all right.

[28:00] So in register contract, we are trying to get my ID, we have, we're defining the data

[28:05] that will go out, and then we create a contract on the basis of that, and then we are sending

[28:10] the actual data.

[28:11] All right, so that's good, then we're done with register contract, and this is going

[28:21] to give me the contract ID, and this is there.

[28:27] And make sure you let this finish, this is not done yet, this is something a couple people

[28:31] have messed up.

[28:32] So this, now that it has the contract ID, it needs to then publish command after console

[28:38] logging.

[28:39] Yep, totally, I see that.

[28:41] So yeah, this is, this has defined the destination, and now it's sending the data to destination

[28:46] is what I understand from this.

[28:50] So contract is registered, and then if we go to, okay, while this finishes, I'll probably

[28:57] get-

[28:58] You're flying through this tutorial, by the way, you're probably going to have the fastest

[29:02] completion time.

[29:03] Like, half the people didn't even get to get to the end, because the network was so messed

[29:08] up, we didn't really know how to fix it for a couple of the episodes, then we learned

[29:12] how, so then we had a better way of recovering after that, but for the ones that actually

[29:17] just worked the first time, everyone has gotten to the end.

[29:20] That's great, I think they should come to India.

[29:23] All right, so that's required, which is the one for registering the contract, and this

[29:31] was actually the publish command that failed.

[29:34] Okay, so this is a moment, I would say first, let's try running it again, and let's see

[29:41] what happens.

[29:42] It might fix itself, but if not, then we're going to go into our client and configure

[29:49] a specific IP address.

[29:52] But isn't that going to create another contract?

[29:56] It will, but both the contracts will have been the same thing, you didn't change your

[30:01] code, and you can see, are they the same or are they different?

[30:06] I do think they're the same, so I'm just checking with the first few letters, so 5yhk and yq2.

[30:14] Because what it might be doing is it might be taking the schema itself and then running

[30:18] some kind of hash on it, so it would always be the same if it's not changed.

[30:22] I don't know if that's the case or not, that's just my guess, because that's how IPFS does

[30:26] stuff.

[30:27] But give me one second, I think I know exactly where the code is that I need, if this is

[30:35] still broken.

[30:36] While this is getting resolved, I'm going to create my scripts.

[30:48] Keep on rolling.

[30:49] Update contract, yes.

[30:50] Let's add that, and then use our identity ID along with contract ID to create the document

[31:00] schema, and then update it.

[31:03] This probably makes sense to me, you're trying to get my identity, you get my contract that

[31:09] I have created, and then get the schema of it, and then we are updating it with my node

[31:17] ID, and then you send out the command to update it.

[31:25] This is done for update contract.

[31:29] Add an apps object to find options and pass the contract ID to enable name and document

[31:39] syntax while accessing contract documents, for example, this particular .node, that's

[31:44] what we did in I think update, so yeah, that's update, so the client is now basically aware

[31:52] of, okay, I think this worked, so yeah, contract is now registered, you have the contract ID,

[31:59] and I believe I need to add this to my ENV, because we are picking this up later, so let

[32:06] me quickly add that.

[32:09] Cool.

[32:11] So we have now updated the client to specify the particular contract ID this is all about.

[32:19] Let me go back to some commands now.

[32:23] So this one in particular was about register contract, let's run retrieve contract.

[32:34] So the sense I'm getting that even though you don't know anything about crypto or blockchain

[32:37] or anything, all of this code has made perfect sense to you so far, for the most part.

[32:42] Yeah, it looks fine to me, like I'm able to understand what's happening, so right now

[32:48] what I've got is that there are two platforms, one has the currency, and then we're converting

[32:53] the currency to another, and then we're specifying two things, that is my storage area and then

[32:58] one is my ID area, and then we are operating on creating transactions in form of contracts,

[33:06] I believe.

[33:07] Yeah, that's all I have got for now.

[33:10] Yeah, you nailed it.

[33:13] All right, so I've run retrieve contract, and this is now trying to, it says print to

[33:19] the JSON.

[33:20] That's it, that's the output, I think.

[33:24] Yeah, and it has the node to the schema.

[33:26] All right.

[33:27] Yeah, you should take a look at that link to the platform or the one that it gave you.

[33:33] I think this will be the last time we'll do this, or maybe not, but this is just a good

[33:39] way to always kind of like double check exactly what happened.

[33:42] So I think you can go to the schema on the bottom.

[33:45] Yeah.

[33:46] Yep, there you go.

[33:48] Yeah, there has been no message, and we can attach basically a node to the transaction,

[33:56] so that's what I get.

[33:59] All right.

[34:01] Now, let's move on to creating the update contract, which is, yeah, I think I've walked

[34:09] through this.

[34:10] This will get the existing node, and then specify a string, which has author, and then

[34:15] set it to the node itself.

[34:17] Okay, so let's run this, which is update contract.

[34:27] So it should be updating in this particular link, correct, where we have the schema already?

[34:35] And then-

[34:36] Yeah, that's a good question.

[34:37] If the contract ID is not changing, then yeah, that should be in the same place.

[34:41] Got it.

[34:45] Let's see, how does this go?

[34:50] I'll use this time to create my own scripts for now.

[34:58] I have updated this client.

[35:00] I will now create a script that is submitNodeDocument.js, and then we put it in here, which is going

[35:15] to take my identity, create a document, and it says hello from this particular user at

[35:21] this particular time.

[35:23] And then we're sending it out to all the nodes I just described earlier, and then we have

[35:29] document ID, which is the new document that we have created, the schema ID of it.

[35:35] And then, yeah, we're just printing JSON off it, sounds good.

[35:39] So this will give me the document ID and the JSON and stuff, sounds good.

[35:45] Let's pick up documents while this runs.

[35:49] All right, so this work, which is update the contract, so this updated the contract to

[35:57] have a node.

[35:58] Let's go here and refresh the page to see the updated schema.

[36:02] And yes, in the node, we see the author here with some message, but yeah, I do see the

[36:09] author updated in the schema, so that's great.

[36:11] All right, let me quickly copy the Git documents thing.

[36:17] Now I'm going to first run the Git documents to see what all is there in my particular

[36:22] document, and then we'll update it using submitNodeDocument.

[36:27] Okay, so I have no message, because I've not run submitNodeDocument, let's get that out.

[36:36] What is the script for running Git in this one?

[36:45] All right, yeah.

[36:46] All right, so we are now publishing another document, which has a note.

[36:56] Then we'll fetch it using the Git document, sounds good to me.

[37:06] Cool.

[37:07] You would probably assume they'll all take a decent amount of time, so if you want to

[37:18] just, as soon as you run the thing, you just start doing the next part every time.

[37:22] Let's do it, we create update node document.

[37:27] So right now I am able to create one, I am able to fetch all of them.

[37:32] Next is updating them.

[37:34] Yeah, this is starting to feel like good actually, and yeah, I think I'm getting the hang of

[37:40] it.

[37:41] I don't know what's happening really underneath it, but yeah.

[37:43] Yeah, that's one of the nice things about the platform is you don't have to worry about

[37:47] any of that, the idea is it's just like a globally distributed database that you can

[37:52] interact with.

[37:53] Yeah.

[37:54] All right, let's re-emphasize, I added an extra s.

[37:58] Are you a relational guy or a NoSQL guy?

[38:02] I am learning relational now, but I am a sort of a NoSQL guy.

[38:08] You probably grew up on the Mern stack, if I had to guess, or I guess it would be mean

[38:12] for you.

[38:13] Yes, that was Angular first, and yeah, really, not using Mongo really, Dynamo was the one

[38:22] that I would use more or less.

[38:24] Oh, that's way better.

[38:26] All right, so we have submitted the document, now let's try to fetch it using the getDocuments.

[38:35] And now I have added two scripts, which is going to update it and delete it.

[38:39] Yeah, all right, make sense?

[38:43] So I have this message that I added in submitNodeDocument, where is that, yeah, this one.

[38:51] So we have added a message with the name and the time, which is here, sounds good.

[38:56] Now let's update the document.

[38:58] So this will try to get my identity, get my documents, the specific one with the ID, and

[39:04] then update the message with the new time zone, new time able, let's update it.

[39:16] And then it's going to again broadcast it to everyone with the replace command instead

[39:19] of adding to it, okay, make sense?

[39:23] And then we're going to delete this node, this is fun.

[39:27] That's cool, yeah, I remember the first time, I was in this process with, oh, it looks like

[39:34] it broke.

[39:35] Yeah, let's run this again.

[39:38] Interesting.

[39:39] I didn't used to have it give you the label in the, in there you said have my own name

[39:54] hard-coded.

[39:55] I'm not sure if that might be an issue.

[40:00] This says internal server error or storage protocol.

[40:05] Try getting rid of label and writing your thing directly in it.

[40:09] So hello from Rishi-90.

[40:10] Got it.

[40:11] Let's do Rishi-90.

[40:12] Just so I can narrow down whether that's what's actually happening or if this is a different

[40:19] error.

[40:22] And if we can't get this one working, it's not the end of the world because we just need

[40:29] something to be written there.

[40:30] Yeah.

[40:31] So.

[40:32] Yeah, it says internal server error for storage protocol, structure value or non-bytes a string

[40:42] or array of values.

[40:44] And this looks particularly internal SDK issue probably, I don't know.

[40:51] But I think for now we can skip this part because it's just updating the document.

[40:54] How about we delete it?

[40:57] So let's delete the document with the ID, so let's delete that.

[41:05] All right.

[41:07] So this is now going to fetch the document and then delete it.

[41:14] And the delete failed as well.

[41:16] So there's probably something on the address.

[41:20] Yeah, so this is the last part where you're writing to the chain.

[41:35] So I'm going to say we should just move on because you understand what the updating and

[41:39] deleting is going to do.

[41:41] From here, you now turn this into like an actual full stack app, you're going to build

[41:47] an express endpoint to expose your name endpoint, essentially that will return your name information.

[41:56] So we can just go ahead on that part.

[41:59] I'm just trying to fetch the documents again to see if the message is there and that's

[42:04] there.

[42:05] So it's in particular to delete or update functionality, I believe.

[42:09] Yeah, I'll have to do some testing on that to figure out what's going on there.

[42:13] So now we have, now we are just basically going to map this to, yeah, Express NCIS,

[42:19] if that makes sense.

[42:21] So we're creating server.js.

[42:25] If you were to build a node backend with like a node framework, what would you use?

[42:31] If you're, or would you not use a framework, I guess?

[42:33] Right now, I think Hono is quite hot right now, so I'll link over that.

[42:38] Hono is tight.

[42:39] I'm just starting to learn Hono.

[42:41] Yeah, that's great.

[42:43] But yeah, Express is a good old thing for us to get started with.

[42:48] A lot of times I'll go with Express if I'm just doing like a tutorial like this, because

[42:51] I know everyone's going to understand it.

[42:53] It's like, it's probably the worst choice for like an actual production server compared

[42:57] to things like Fastify and Hono and like all these other amazing ones out there, but it

[43:02] gets the job done.

[43:04] Yes.

[43:05] Cool.

[43:06] So we have created an Express app with CRS enabled, and then we're on eShout that is

[43:14] dynamic to name.

[43:15] It will get the identity and try to get basically the ID of the person, as I understand.

[43:21] Yeah.

[43:22] So it's trying to say no identity found in case it's not done, and it's going to disconnect.

[43:26] Makes sense.

[43:27] So now we run the Express, which is now running on 3001, and then I'm trying to curl.

[43:36] So the name I should be entering here is Rishi-90, correct?

[43:39] Yeah.

[43:40] Yeah, that'll be the one.

[43:41] Gotcha there.

[43:42] Because that's my label.dash.

[43:43] Yeah.

[43:44] All right.

[43:45] Yeah, that's right.

[43:46] Let this, let's open this in my new tab instead of doing the curl, so Rishi-90.

[43:55] What does this give me?

[44:00] Okay.

[44:01] So it's probably using something from-

[44:03] Cool.

[44:04] That's funny.

[44:05] I think you're the first one to do that, just actually put it into a browser.

[44:08] So yeah, that's great.

[44:09] Yeah.

[44:10] Super not fan of curls.

[44:11] Like I had to see something in there.

[44:14] And probably that's because I didn't have JSON PP install, and I was hesitant to do

[44:18] it.

[44:19] And that's why I just went ahead with this one.

[44:20] But yeah, I see the data coming in for a particular ID.

[44:23] I have the nominalized table and the label.

[44:25] So this is basically just getting the ID.

[44:26] Could you try writing that command?

[44:27] Because I'm just curious.

[44:28] Because I don't think you need to explicitly install the JSON PP, but I'd be curious to

[44:33] figure out.

[44:34] All right.

[44:35] Let's do a curl, and then we take the output to be JSON compatible.

[44:42] This actually failed for some reason, which says cannot-

[44:45] You didn't put quotes around it.

[44:48] Oh, no.

[44:49] It actually disconnected the dash train.

[44:50] So the script exited, run the express, and then now the terminal didn't do that.

[44:57] So curl, and then JSON PP.

[45:02] Yeah.

[45:03] This is going to fetch.

[45:07] Okay.

[45:08] I do have it.

[45:09] Yeah.

[45:10] Yeah.

[45:11] Exactly.

[45:12] It's coming in.

[45:13] Nice to know that I have JSON PP.

[45:16] Yeah.

[45:17] Just specifically to pretty print your curl outputs is the only thing it does, at least

[45:22] that I use it for.

[45:23] All right.

[45:24] So now we are creating our next app, which is what I'm super familiar with.

[45:29] Let's name it as dash app.

[45:34] Yes.

[45:35] Oh, wait.

[45:37] Do you want me to use TypeScript?

[45:42] I don't know.

[45:43] You should try it out.

[45:44] We'll see what happens.

[45:46] The version I build, I usually don't use TypeScript, but it should still work.

[45:51] Yes.

[45:52] We're using this source.

[45:54] Okay.

[45:55] AppRouter, yes.

[45:56] And customization required.

[45:57] Can you do everything on AppRouter now?

[46:01] No.

[46:02] So LaunchFiles in XJS is on PagesRouter, and I had people and a poll on Twitter, which

[46:09] allowed me to start migrating it to the AppRouter, so I migrated the APIs, and now I'm migrating

[46:14] each component to AppRouter.

[46:17] I've heard, it's sort of tricky, because there's some things that just don't work with AppRouter.

[46:27] I recently learned about how to use Grammy SDK, that is for creating telegram bots.

[46:33] So I wrote an article about it, because I didn't know that there's experimental server

[46:36] components, config, that you can use in XJS.

[46:42] So yeah, there's a learning curve, but I'm doing it so that other people don't have to.

[46:48] Okay.

[46:49] Gotcha.

[46:50] Yeah, I think I got the link right here, I think I can flash that on the screen real

[46:56] quick.

[46:57] Bam.

[46:58] Yeah, once we're finished with this, we could take like five minutes, you can kind of show

[47:05] the homepage and stuff for LaunchFA.

[47:08] Sure.

[47:09] We're going to be done like 25 minutes early, and then I'll be curious to get your thoughts

[47:17] on the platform and what you would want to build with it if you were to.

[47:21] Sure.

[47:22] So let's walk through LaunchFast pretty quickly.

[47:27] Once we finish the tutorial, I'll say we should take a look at this.

[47:30] Let's get to the end of the tutorial first.

[47:32] All right.

[47:33] Sure.

[47:34] It makes sense.

[47:35] I'll hide this for now.

[47:36] You'll get a chance to make your pitch, don't worry.

[47:38] Oh, that's fine.

[47:39] That's fine.

[47:40] I'm here to work on Dash, so it's totally fine.

[47:46] This is going to take time, I believe.

[47:48] Let's just put the script for now.

[47:50] So we have page.tsx, let's put it here.

[47:56] So this is just going to fetch something and then print my identity.

[48:00] There's no JSON for it.

[48:02] So this is just to double check that you got your next thing set up and just have a kind

[48:07] of boilerplate page set up.

[48:11] Then you'll add the logic to actually get your stuff after that.

[48:14] Got it.

[48:15] Let's do then gem run dev, which is 3000.

[48:23] And yeah, the starter app is ready.

[48:26] Then we are to replace this with this particular code, which is going to do the same thing

[48:33] that we did.

[48:34] And actually, I have an error in here that I still need to fix.

[48:38] It has my own name hard-coded in the endpoint.

[48:42] So look where you're hitting that, yeah.

[48:47] And then I need to also have the server running, correct?

[48:51] Yeah, that's right.

[48:54] So we do npm run express.

[49:07] Okay, cool.

[49:12] Let's go to actually reload this page.

[49:17] So this should...

[49:18] Yeah, actually, you might need to...

[49:19] Fetch?

[49:20] I think this is...

[49:21] No, there we go.

[49:22] Yeah, cool.

[49:23] I think you need to update.

[49:24] Yes.

[49:25] You need some of them spinning, yeah, you need lots of spinners for this one.

[49:30] Yeah, so now we have the loading state that we were just prepping to.

[49:35] Ah, right.

[49:36] I already did that.

[49:37] I forgot.

[49:38] You need the fetch button though to get it.

[49:39] Yes.

[49:40] So we have fetch data.

[49:42] Let's click on fetch data.

[49:44] There's your loading.

[49:47] It doesn't spin, but it does tell you it's loading.

[49:52] Yeah.

[49:53] Yeah.

[49:54] Useful design.

[49:55] This is exactly what...

[49:56] I probably just do this by habit because Redwood JS, they have this concept of the cell, which

[50:02] will have a built-in loading state.

[50:04] And that's when you first create your boilerplate cell, it just says loading dot, dot, dot.

[50:11] Got it.

[50:14] Still loading.

[50:15] Loading.

[50:16] Loading.

[50:17] Yeah, it worked last time, so it definitely should...

[50:20] Again, again.

[50:21] This is the...

[50:22] Yeah, it is.

[50:23] I see, yeah.

[50:24] Let's redo the page.

[50:27] It should be much faster now.

[50:29] Yeah, once we get this to work, actually, since you know Next very well, could you just

[50:34] make an environment variable for me to fix that?

[50:36] Oh, sure.

[50:37] Yeah.

[50:38] Yeah.

[50:39] So you should be able to just access...

[50:42] Well, I guess you create the...

[50:45] Because of the Next app is now inside of your project, it won't necessarily be able to reach

[50:51] out to the .env.

[50:52] You need a separate .env.local file, I guess, probably.

[50:57] It's somehow not responding.

[50:59] Okay.

[51:00] This is responding now.

[51:01] Where's my Next app?

[51:02] Okay, let's...

[51:03] Just make sure to refresh that.

[51:04] Yeah.

[51:05] Okay.

[51:06] Refresh the page first.

[51:07] Okay.

[51:08] This is working, and now we have to set up an env, as you said.

[51:17] Let's do an env versus a Next public name, or let's make a label, and then 3c90, and

[51:24] then we can use this in the fetch, so I think it should be it.

[51:37] There we go.

[51:38] Reload the page, fetch data, and it comes in.

[51:42] So it's coming in now from an env.

[51:45] I think using Next public is important, because you're loading the page on the client side,

[51:50] and...

[51:51] That's right.

[51:52] Yeah.

[51:53] Cool.

[51:54] This is done, and this is great, I would say.

[51:59] We did have some of the commands that failed, and that was for updating the document.

[52:04] But apart from that, I think all worked fine for me.

[52:08] Yeah.

[52:09] Yeah, totally.

[52:10] Yeah, it was good.

[52:11] The stuff that needed to work pretty much worked.

[52:14] Yeah.

[52:15] So now you could imagine, like, you could build out endpoints to do all the other kind

[52:19] of functionality that we just implemented in scripts, and then you could expose that

[52:24] through your UI, and then you have kind of just -- it's just a general app-building platform

[52:30] with, you know, your basic kind of CRUD operations.

[52:33] So you could probably imagine things you could build with this, I would assume?

[52:38] Yes, I do.

[52:39] So basically using these scripts, probably, I don't know if it's the right use case for

[52:44] you, but as I see that I can have transactions with documents, I'm using something called

[52:48] Splitwise, and that allows me to showcase -- allow me to add or maintain the expenses

[52:55] with other people.

[52:56] And so --

[52:57] What is it called?

[52:58] Splitwise.

[52:59] Splitwise.

[53:00] I think I've heard you talk about this.

[53:03] Splitbills is the easy way.

[53:05] And yeah, so we are always adding notes about what this transaction or expense is for.

[53:12] I'm really liking this update in Summit Node Document, which will allow, you know, me to

[53:20] have a label to a transaction apart from just the transaction ID and, yeah, some numbers

[53:25] that I don't understand.

[53:27] So yeah, I think I would straight up go ahead and build that for an example.

[53:32] It's like a to-do for finance, though, is where you can showcase --

[53:36] No, that's awesome.

[53:37] Yeah, and we're -- like, so the Dash itself, the way it funds its development is it has

[53:44] something called a DAO, Decentralized Autonomous Organization, where basically there's a certain

[53:49] amount of funds in the network that gets set aside for paying people who submit proposals

[53:55] to build stuff.

[53:57] So if you wanted to, like, build that and integrate Dash, then we could get in touch

[54:02] with Ryan.

[54:03] We could figure that out.

[54:04] Because we're always looking for more contributors.

[54:05] That was kind of one of the things we were hoping we would be able to get people in and

[54:08] show them this.

[54:09] And then they'd be like, "Oh, cool.

[54:10] I can build this thing with it now."

[54:11] So the fact you already have an idea for it is great.

[54:14] If you don't do it, then I can do it, but it'd be better if you did it.

[54:17] Sure, I will do it once I have some flexibility on my update, for sure.

[54:23] And it'll be more useful once we're on mainnet, like, a month or two as well.

[54:27] So no rush on that.

[54:29] But do you have any kind of, like, remaining questions about this whole deal?

[54:36] Yeah, I think I understood the flow and what's happening here.

[54:41] But probably it's great to have a distinction between the contract, the document, and where

[54:50] does my ID lie.

[54:51] So I don't know.

[54:52] I'm not a crypto expert, and that's why I'm asking for this.

[54:56] So we have a document, which has the ability to have a node.

[54:59] That's representing a transaction, I would say.

[55:01] But having a walkthrough of what's a document, what's a contract, and how are they separated

[55:07] is probably good to know, because I'm always assuming that there are transactions underneath.

[55:15] What's happening inside of that is sort of unclear.

[55:18] Probably we can have...

[55:20] Yeah, for me, the way I wrote it and the way I make sense of this stuff is through the

[55:25] Explorer.

[55:26] So that's why if I wrote it in a way where every time you do one of those steps, you

[55:32] can then go look at the Explorer to see what has changed.

[55:36] But you're right that a lot of this is jargon that might not necessarily make a whole bunch

[55:41] of sense.

[55:42] And this is one of the big problems with blockchain in general, is it's the whole network and

[55:48] all the data is public, and anyone can look at it, but it's just like, "But how?"

[55:52] Because it's just this huge hunk of code that has different ways of interacting with it.

[55:58] Because most blockchains will have an RPC endpoint, and then they'll have these client

[56:02] libraries.

[56:03] You're using the JavaScript SDK, there's also a Rust SDK, and they also are just exposing

[56:08] gRPC endpoints.

[56:11] So you could just hit the endpoints on testnet or your own node and kind of introspect it,

[56:17] but then you're getting really deep into reading all this docs to make sense of that.

[56:21] So that's why I think the Explorers can be a good way to kind of get some visibility

[56:26] into what's happening here in terms of how it's happening, how the transactions are being

[56:31] written and stuff like that.

[56:33] That's kind of being handled by the network.

[56:35] And you can go learn about how the network does it, but the network itself, there's a

[56:39] clear separation with blockchain where once the blockchain network itself is created,

[56:46] you just interact with it, and it shouldn't change.

[56:51] You'll write code that's like the app layer on top, but it's like a protocol.

[56:55] It's like you can learn how TCP works, but you don't have to worry about changing underneath

[57:01] you.

[57:02] >> Yeah, I think I get it.

[57:07] I am yet to use GRPC for building a super cool app, but yeah.

[57:16] >> I've never used GRPC, and I've used like JSON RPC, because that's how you would interact

[57:25] with like Ethereum is it gives you, you can just curl it and send JSON objects that kind

[57:31] of say like the information, how it works.

[57:34] And so this is kind of closer to that.

[57:37] Ethereum has also, they have something called smart contracts, which is totally like there's

[57:42] no way of mapping these things onto each other, because with Ethereum, you can actually put

[57:47] a program on the blockchain that has the ability to read, write and manipulate variables and

[57:53] do all this stuff, whereas you can't do that here.

[57:57] The actual logic is in the platform, and you can only write documents to it and then update

[58:03] those documents, interact with those documents, whereas with Ethereum, you can actually put

[58:07] a brand new program on that could do anything, it could just take all your money, you have

[58:11] no idea until you read the code.

[58:14] >> I see.

[58:15] That's why probably I'm not going into crypto, I believe, but I see a lot of things happening

[58:20] which sort of have me scared.

[58:23] >> It's crazy, man.

[58:24] Yeah, you got to be really careful about it and make sure you're using proper, it really

[58:29] makes you think about security a lot more, because everyone's worried or should be worried

[58:34] about getting hacked, but in the back of our minds, a lot of people will still skip steps

[58:41] and will be vulnerable in certain ways, whereas once you've actually had your wallet hacked

[58:46] and your money just stolen, you're like, "Oh, wow, this is why you don't click random links

[58:51] on the air that are fed to you with a random pop-up."

[58:55] >> Yeah, that sounds somewhat scary, I would say, but yeah, I don't know.

[59:05] >> Well, with Dash, they really think about security and they've been around for a really

[59:11] long time.

[59:12] So the newer a network is, the more kind of attack vectors are going to be, especially

[59:17] if they're trying to do brand new things you couldn't do before.

[59:21] So in terms of having a vulnerable wallet that someone could phish you, there's ways

[59:27] of doing that with different cryptos.

[59:28] If you just have your wallet as an extension in your browser, you're exposed anytime you

[59:34] click a link anywhere in your browser, because you have this extension running all the time.

[59:39] But a lot of times with Dash, I don't think there even is a browser extension.

[59:43] You can download a desktop app or a wallet app, and then that will let you generate a

[59:49] wallet like we did here, except it will be a wallet on mainnet on the original Dash.

[59:55] So that's where you would have your money.

[59:57] And then that is kind of secure, like a banking app or something like that.

[60:03] >> Yeah, that's a much-needed gap to cover.

[60:08] Yeah, we are using testnet for this, probably could have mainnet, but that would require

[60:15] real money.

[60:16] So definitely not going there for now.

[60:18] >> Yeah, Ryan was saying that even once this is on mainnet, it's still going to be pretty

[60:23] cheap to create NightData.

[60:24] He was saying it should be just a couple of dollars or something like that.

[60:28] When I got my Ethereum name, you know what I paid for ajcwebdev.eth?

[60:34] $200, because this is when the market was super run up, and once the network gets congested,

[60:41] you have to pay more to get it on there, because I was trying to use this as a supply and demand

[60:46] type thing.

[60:47] So if you want the .eth namespace, that's the only one you want.

[60:50] You don't want .ether, because you're going to be the only weirdo who uses this one other

[60:55] thing that you want the Ethereum namespace, so there's a scarcity to it as well.

[61:00] But yeah, according to Ryan, it's not going to be super expensive to buy one, but we shall

[61:07] see.

[61:08] So you got to make sure you get reishi.dash as soon as it's available.

[61:12] >> Sure.

[61:13] Where do I check it?

[61:14] Can you do a little checking for me?

[61:17] >> So let's, since we've got some time now, do you want to show your launch project for

[61:24] a bit?

[61:25] >> Sure.

[61:26] Happy to, always.

[61:27] >> How long have you been building this for now?

[61:30] Did you start this before or after you left Edge.io?

[61:34] >> This was definitely after Edge.io, and I think after six months after that.

[61:43] This started in October, so I had another, this is an inspired project for sure, and

[61:49] I saw Mark launching Shipfast, and then I was like, I can do something, but for Astro,

[61:55] because people are building websites in Astro for static content, but they can also use

[61:59] it for dynamic as well.

[62:01] So that's what the intention was initially, and that did receive great love, even from

[62:06] the Astro community as well, and then, yeah, it has been a great project, and I'm also

[62:12] learning while I'm building this.

[62:14] So it's basically, like I've initially started out to be a boilerplate, now it's more like

[62:18] a starter kit, because you get everything configured for you.

[62:22] You can accept logins using various methods, right now it's Google and Twitter, of course

[62:27] you can expand, like by default it's Google and Twitter, but it can use several methods.

[62:32] And then it can, I recently transformed it to use any Postgres or Redis, so it's like

[62:36] flip a switch, you change an environment variable, and you can now use Redis, or you can now

[62:41] use Postgres, you just need to define some URLs.

[62:43] >> Were you in the AstroDB preview at all?

[62:47] >> No, just not using AstroDB for now.

[62:51] So I've tried to focus this project on, like building it on REST APIs.

[62:56] >> And I was asking if you had just done the DB, like if you played around with it at all,

[63:02] not if it was in this.

[63:03] I know it's not in this project.

[63:04] >> I see.

[63:05] No, I didn't get a chance at it.

[63:07] >> Yeah, I need to definitely look into it and work it out.

[63:12] >> It's a bummer, 'cause I was planning on doing it, and then they closed it, 'cause

[63:16] they are, it was a preview, and then they're like, we're gonna close this until we release

[63:20] the real thing.

[63:21] If you're in the preview, you can still keep using it, but now they're not taking new users,

[63:24] so like, ah, now I gotta wait for the real thing.

[63:27] >> I see.

[63:28] >> Yeah.

[63:29] >> Okay.

[63:30] >> Hopefully it won't be too long.

[63:31] They ship pretty fast, so I'm assuming in the next three to six months, they'll launch

[63:34] the actual one, but the database is one you gotta make sure you don't mess up.

[63:39] >> By the time I make some updates, I see a new Astro version coming up all the time,

[63:43] so Astro's moving super fast, and I like it.

[63:46] I like that.

[63:47] >> Well, the content layer they're about to add will probably be really useful for something

[63:50] like this, 'cause that's gonna allow you to bring in a whole bunch of other crap.

[63:56] >> What's that?

[63:57] >> So did you hear, so they did that big release where they had three big announcements.

[64:02] They had the server, islands, and then they had the content, yeah, so content, yeah.

[64:09] So it's like Gatsby.

[64:10] It's just Astro now has a Gatsby thing, like a content mesh that lets you hit different

[64:15] endpoints and mash them all together.

[64:17] >> Got it.

[64:19] I see.

[64:20] Yeah, I'm yet to use this.

[64:23] Definitely when this, I'm excited for this, and I can probably merge this back into launch

[64:27] version.

[64:28] >> You don't have, like, CMS integrations yet, do you?

[64:31] >> No, there is no CMS as of now.

[64:34] >> Yeah, so that's kind of what this, I imagine what this is for, for someone who wants to

[64:38] bring in, you know, something 'cause they're using Contentful or whatever.

[64:43] >> Ah, I get it now.

[64:45] So using this, I can build components that correspond to parts in my CMS, and then I

[64:50] can plug them anywhere in my project.

[64:54] Okay.

[64:55] But yeah, let's see how does that turn out, because I need, probably I need to learn it

[64:58] first and then add it to, or play around it and then probably add it.

[65:03] Yeah, and then the payments thing that you were talking about is already configured.

[65:07] I'm yet to add a script where it auto-converts a currency, because in India you cannot, accepting

[65:14] foreign currency, so you have to convert every time you go to a particular country user,

[65:19] so yeah.

[65:20] >> So that's where crypto is really interesting, 'cause it takes that whole thing away.

[65:23] If someone has crypto, they don't want to pay someone else in crypto, they can just,

[65:26] if they have the Dash, they give someone else the Dash, and there doesn't need to be a conversion,

[65:31] then they can convert the Dash to whatever their national currency is once they have

[65:36] it.

[65:37] And Stripe integrates with a couple crypto solutions that support Dash, so whatever,

[65:45] as long as you have Stripe integrated in the project already, it should be trivial.

[65:49] This is actually, so I'm planning on building like a quick start guide of how to just build

[65:53] a quick Stripe integration that shows the actual steps of doing the Dash part of like,

[65:59] 'cause there's, I forget what the two things are that it integrates with, let me look this

[66:04] up real quick.

[66:06] So look up just Stripe crypto integrations.

[66:19] Okay, so keep going, keep going, yep, keep going.

[66:35] So I think at the very top, it showed a bunch of, hold on, stop right there, no, that's

[66:54] not it, hold on.

[66:55] I do know where this is on the actual Dash website, I just gotta pull it up, let's see.

[67:04] There's a tool, yeah, this is, okay, so now payments is one, and the other one I think

[67:20] was.

[67:21] - Now payments with Dash, is what I should search.

[67:25] - So look up now payments and Stripe.

[67:29] - I see, now payments and then Stripe.

[67:34] Okay, now payments, is that the one?

[67:37] No, it's the same one, okay, probably this one.

[67:46] - I think that's the one, yeah.

[67:49] - Yeah, I see a lot of providers here, where do you find the one for Stripe, in this one?

[67:57] - I don't know, I've never done this before, so we don't need to necessarily get too deep

[68:01] into this, but if you just go to their docs, or just, actually, let me do this, now, payments,

[68:09] let's open this one, oh, there's PayNow, is it?

[68:28] - Nice, okay, PayNow, Stripe, yeah, I don't see this Stripe in here, in now payments API,

[68:38] yeah, but anyways, yeah, I think we can.

[68:45] - I think, okay, here's something that's basically gonna get the idea across.

[69:05] Go to docs.stripe.com/crypto, there you go, and just kind of scroll through that.

[69:22] Try the sample integration, let's see what that is.

[69:27] - Okay, so this is using pre-built payable Stripe VR to crypto on RAM, and what is that?

[69:38] That's something I need to learn.

[69:39] - You go to the JS instead of Ruby, there we go.

[69:44] - Yeah, it's loading Stripe on RAM, creating a session.

[69:48] - Okay, cool, so what this is doing is, it says USDC, that's the destination currency,

[69:54] so USDC is a stable coin, pretty sure that's Coinbase's stable coin, so this is where you

[70:04] would turn basically whatever your country's native currency is into that, so for there,

[70:09] if this may not necessarily work, this may not be integrated with the right things, but

[70:13] ideally you could just change that to say Dash, and then it would turn into Dash.

[70:17] There might be more steps, like I said, I know that you need to use now payments or

[70:22] what the other thing that integrates with it, so these are things that I need to figure

[70:25] out in my, this is why I need to write the tutorial, but this kind of gives you an idea

[70:29] of like, once you have Stripe integrated, they have already built in a lot of crypto

[70:34] tooling and endpoints and client stuff for you.

[70:38] - Nice, that's great, I'm happy to add an integration once I learn about it.

[70:45] - Sweet.

[70:46] - Yes, looks good.

[70:48] - Awesome, man, well, is there anything else you want to talk about, or like, you can probably

[70:54] give your contact information and stuff if anyone watching wants to check your things

[70:59] out or contact you.

[71:01] - Sure, you could find me on Twitter, so that's Rishi.Chen, I'm always building launchpads

[71:08] as you can see here for sure, and then we have Rishi.app, where you can find my portfolio

[71:14] and you can have a lot of social links to reach out to me, so, yeah.

[71:18] - Is this built with Astro also?

[71:22] - This is built with SvelteKit, I believe, yeah, this is with SvelteKit, so I'm trying

[71:27] out different things, but I love the near-HTML syntax of SvelteKit, but I've heard that Runes

[71:35] in SvelteKit 5 is going to be something new, so I'm excited to try that out once that comes

[71:40] out.

[71:41] - Yeah, no, I liked SvelteKit when it first came out, I haven't really kept up with it

[71:45] recently 'cause I just have been sticking with Astro and React for the most part, which

[71:54] is just so fast to work with, and I really love Astro, so, that's why I was stoked that

[72:00] you built this really cool Astro project.

[72:02] - Yes, for sure, you should change that tutorial to use Astro instead then, just kidding.

[72:10] - Awesome, man, cool, so thanks so much for doing this, I'm gonna end the stream here,

[72:16] but stay on just once we go live so we can talk afterwards, and thanks everyone for watching,

[72:22] we'll catch you at the next one.