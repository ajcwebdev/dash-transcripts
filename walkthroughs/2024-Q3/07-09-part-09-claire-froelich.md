---
showLink: "https://www.youtube.com/watch?v=fNynKtEZIlQ"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Platform Walkthroughs Part 9 - Claire Froelich"
publishDate: "2024-07-09"
coverImage: "https://i.ytimg.com/vi/fNynKtEZIlQ/sddefault.jpg?v=668bf29d"
---

## Episode Description

Claire Froelich explores Dash platform development, creating a basic application with identity, contracts, and document storage on the testnet.

## Episode Summary

In this episode, Claire Froelich, a developer returning to the Web3 space after a hiatus, explores Dash platform development with guidance from Rion and Anthony. The walkthrough covers setting up a testnet wallet, creating an identity, registering a name, and working with data contracts and documents. Claire learns about Dash's unique features, including master nodes and instant transactions, while experiencing hands-on development using the Dash SDK. The tutorial demonstrates how to interact with the Dash platform, create and update documents, and set up a basic server for a decentralized application. Throughout the session, Claire asks insightful questions, drawing comparisons to traditional web development and other blockchain platforms.

## Chapters

00:00 - Introduction and Setup

Claire introduces herself as a developer returning to the Web3 space after a two-year break. The hosts, Rion and Anthony, explain the focus on Dash platform development and its upcoming mainnet launch. They discuss the importance of the tutorial for developers and set up the initial project environment, including installing necessary packages and configuring the development environment. This chapter sets the stage for the hands-on development session and introduces the key concepts they'll be exploring throughout the tutorial.

05:57 - Creating a Wallet and Funding with Testnet Faucet

In this chapter, the team walks through the process of creating a wallet on the Dash testnet. They explain the concept of a testnet faucet and how it provides free test coins for development purposes. Claire creates a wallet address and uses the faucet to obtain testnet Dash. They discuss the transaction process, exploring concepts like inputs, outputs, and change addresses. This section provides a practical introduction to working with cryptocurrency transactions in a safe, test environment.

22:57 - Understanding Dash and Its Unique Features

Rion provides an in-depth explanation of Dash, its origins as a Bitcoin fork, and its unique features. He discusses the master node concept, which allows for instant transactions and additional services. The conversation covers Dash's approach to scalability, security, and usability, touching on topics like the blockchain trilemma and Dash's decentralized autonomous organization (DAO) for governance. This chapter offers valuable context about Dash's position in the cryptocurrency ecosystem and its technological innovations.

37:05 - Creating and Managing Identities on Dash Platform

The tutorial moves into creating and managing identities on the Dash platform. Claire creates her first identity, exploring the concept of decentralized identities and how they differ from traditional account systems. They discuss the process of registering a name associated with the identity and how it's represented on the blockchain. This chapter demonstrates the practical implementation of decentralized identity systems and their potential applications in Web3 development.

56:16 - Working with Data Contracts and Documents

In this section, Claire learns about data contracts on the Dash platform, which serve as schemas for storing and validating data. They create a simple contract, submit a document adhering to that contract, and explore how to retrieve and update documents. The discussion covers the similarities to document databases and the unique features provided by blockchain technology, such as cryptographic proofs of data presence or absence. This chapter illustrates how developers can build decentralized applications (dApps) using Dash's data storage capabilities.

74:52 - Setting Up a Server and API Endpoints

The final chapter focuses on setting up a server to interact with the Dash platform. They discuss creating API endpoints that correspond to the functionality explored throughout the tutorial. While they don't implement the full server due to time constraints, they explain how it would work in a real-world scenario, bridging the gap between the Dash platform and traditional web development practices. This section provides insight into how developers can integrate Dash platform features into full-stack applications.

## Transcript

[00:00] All right, we're back with part 9, one more to 10 of the Dash platform walkthroughs, and
[00:10] we got Claire.
[00:11] What is up, Claire?
[00:12] Hey, thanks for having me.
[00:13] Thanks for being here.
[00:14] You want to tell the audience a little bit about yourself?
[00:20] I am a curious person with Node installed in my computer, and I have been actually away
[00:28] from the Web3 space for about two years.
[00:31] So Anthony said this is going to be beginner-friendly, and I'm going to come back to this with beginners'
[00:36] fresh eyes, meaning if I can do this, anyone watching this can probably do it better.
[00:42] And I'm really excited to see what this is all about.
[00:44] If I remember correctly, you were into Algorand.
[00:47] Is that right?
[00:50] I was roped into it, but I was more into the development side of blockchain.
[00:55] I was really curious about that, and I'm really curious if it's gotten any less painful of
[01:03] the developer experience.
[01:04] So let's see how it is.
[01:07] That's perfect.
[01:08] Yeah, so we're definitely more geared towards and oriented towards the developer side of
[01:13] things in the incubator, Dash incubator, and Dash in general right now with our Dash platform
[01:21] that's coming out July 29th.
[01:25] So this on main net, well, it's not going to be on main net July 29th, but it will launch
[01:32] on July 29th, which is coming up this month, the end of the month.
[01:36] And it basically gives you a platform to store data that's provably present or absent, all
[01:43] sorts of things there that we can talk about through the stream.
[01:47] But I think we should just go ahead and jump right into the screen share, and we'll walk
[01:53] through it.
[01:57] And you were saying on the screen that you were just, you were working in another developer
[02:03] oriented position.
[02:06] So you called yourself a beginner, but I don't think, yeah.
[02:12] A blockchain beginner is definitely appropriate title for me.
[02:16] Got it.
[02:17] Got it.
[02:18] Yeah.
[02:19] You were a player, someone who kind of switched like mid, mid career from someone who was
[02:26] something just kind of getting more into coding because you, I first met you because actually
[02:31] we should mention Monarch was the first person who did this walkthrough with us.
[02:35] And we originally met because she worked for Monarch's company, Mint Bean.
[02:41] Cool.
[02:42] Yep.
[02:43] Yep.
[02:44] So what are we going to do today, by the way?
[02:47] I'm totally coming into this blind.
[02:48] We're going to build kind of like a hello world application with Dash platform.
[02:54] And I was going to say the most important thing to know before we get started is that
[02:58] there's Dash, the cryptocurrency, which has been around for a while, about a decade.
[03:03] And then there's the Dash platform, which has been in development for many years.
[03:08] And as Rion just said, it's like about to be released in about a month or so.
[03:13] And that is what is going to add things like identity and storage and the more app-like
[03:20] layers of the platform.
[03:24] So this is going to be mostly going through that.
[03:26] So this is going to be less like interacting with Dash cryptocurrency as it has existed
[03:31] in the last 10 years and more so using these higher level functionality pieces.
[03:37] Awesome.
[03:38] But with code, it sounds like.
[03:39] With code, exactly.
[03:40] Yeah.
[03:41] It's all JavaScript, baby.
[03:42] That's what we want to be.
[03:43] That's good.
[03:47] So part of this is we're testing the tutorial to some degree, you know, we've done nine
[03:51] or eight of these so far.
[03:53] So we're honing in on what is needed to make this something that somebody can work through
[03:59] unassisted.
[04:01] And we think it's there already.
[04:03] But if there's anything that's not clear, then just mention it or something like that.
[04:08] But I think we should just jump in and we'll we'll see as we get in.
[04:11] Cool.
[04:12] Yeah.
[04:13] Yeah.
[04:14] You can jump to the setup and configure node project section.
[04:16] There's some text at the beginning that's not as important.
[04:21] OK.
[04:22] So am I just going to walk through this out loud?
[04:26] Yeah.
[04:27] Go for it.
[04:28] All right.
[04:29] Cool.
[04:30] Well, let's first prove that I have the right node version because I haven't checked in
[04:33] a while.
[04:34] I'll make this.
[04:35] Is this big enough for you to see?
[04:36] That's good.
[04:37] Now.
[04:38] Yeah.
[04:39] OK.
[04:40] All right.
[04:41] So V20.
[04:42] We're good there.
[04:44] Also an odd version.
[04:46] Is that experimental of me living on the edge?
[04:50] Well.
[04:51] Well, yeah.
[04:52] So no one ever.
[04:53] You're specifically only supposed to use 21 for, like, testing new features.
[04:57] But if you're ever going to deploy, you're always supposed to be on the even ones.
[05:02] So I always think it's interesting.
[05:03] People have an odd one on their computer.
[05:05] So like, well, no one's really going to ever deploy.
[05:09] I would push to prod on V21.
[05:11] I'm that daring.
[05:13] There you go.
[05:14] All right.
[05:15] So I'm making a project folder called dash examples and heading in there.
[05:19] We're going to start a new MPM project.
[05:24] You missed the init.
[05:25] Oh, yeah.
[05:26] MPM init.
[05:27] Sorry.
[05:28] I'm on, like, preschool mode in my terminal here.
[05:33] OK.
[05:34] So we've got a new project open.
[05:36] Actually, I'm just going to open it from in here.
[05:41] All right.
[05:43] And we're going to set it to type module.
[05:49] I won't ask questions.
[05:50] I'll just paste what I'm told.
[05:53] That's just for the ESM.
[05:56] OK.
[05:57] And we're installing the package dash version 4.
[06:02] We're making a git ignore.
[06:06] Is this a big package?
[06:10] You tell me.
[06:11] It's not that crazy, I don't think.
[06:17] I think it is.
[06:18] It takes a bit longer to chew on than the average.
[06:22] I think it's too big.
[06:23] All right.
[06:24] So I'm going to make this a bit bigger, too.
[06:26] But we've got our git ignore ignoring the essentials now.
[06:30] OK.
[06:31] We'll create a script file individually throughout the tutorial for the sake of simplicity.
[06:37] Add all the node scripts that will be implemented by the end of the tutorial.
[06:40] All right.
[06:41] So I'm just going to copy this.
[06:44] These are-- that's so nice.
[06:46] You guys have given all of the cheat scripts.
[06:48] Yep.
[06:49] So I'm going to go ahead and paste.
[06:53] We don't need the test one?
[06:55] Well--
[06:56] No.
[06:57] Nope.
[06:58] I like-- see, we're living on the edge, v21 node, no tests.
[07:03] All right.
[07:04] So these scripts are basically going to be shortcuts for running script files that we
[07:09] make later, it sounds like, and running a server.
[07:14] Yep.
[07:15] OK.
[07:16] Initialize the dash client.
[07:17] Create a scripts directory and an API directory.
[07:22] Is that two separate directories?
[07:24] I guess so.
[07:25] And a file called client.
[07:27] So if client is in the API-- I'm just going to follow your code here.
[07:34] So make their API scripts-- OK, two folders.
[07:41] And we're going to create a client.js file.
[07:45] And in our env file, we're going to add an environment variable called network set to
[07:51] test net.
[07:52] So it should be here.
[07:55] Yep.
[07:56] And we have our empty client.js file.
[08:01] All right.
[08:05] While we're at it, should I get in it here?
[08:10] Because those node modules not being grayed out are freaking me out.
[08:14] Yeah.
[08:15] That's fine.
[08:16] Because that way, if we don't finish, then we can pick up where we stopped.
[08:20] All right.
[08:22] So import dash from dash, pass the project's network and wallet configuration through dash's
[08:27] client constructor.
[08:28] So that sounds like something I'm going to have to set up maybe in your UI or something.
[08:32] Well, let me just copy all this.
[08:39] So we got a little [INAUDIBLE] OK.
[08:46] So we're importing dash, getting our network environment variable, and setting it to the
[08:51] network property when we initialize.
[08:57] What's the mnemonic in Polish?
[08:58] I don't remember this term.
[08:59] Have you ever-- Password.
[09:00] That's super long.
[09:01] Have you ever dealt with the 12-word phrases?
[09:02] With what?
[09:03] Did you repeat that?
[09:04] Have you ever dealt with 12-word seed phrases when you were doing Algorand stuff or any
[09:20] other web 3D or crypto stuff?
[09:22] Is that like the secret password you don't share with anyone?
[09:25] Yes.
[09:26] Yeah.
[09:27] OK.
[09:28] So that's called a mnemonic?
[09:29] Yeah.
[09:30] In some circles.
[09:31] I'd like to-- I'd rather call it a seed phrase because that's what it is.
[09:36] But yeah.
[09:37] That's what the API has called it at this point.
[09:39] OK.
[09:40] Sweet.
[09:41] So the client is set up.
[09:45] And feel free to shout out, by the way, if I'm missing anything or any footnotes you
[09:49] want to add.
[09:50] Yeah.
[09:51] You're doing good so far.
[09:52] All right.
[09:53] So we haven't created a wallet yet.
[09:55] Mnemonic is set to null to indicate we want a new one to be generated.
[09:59] To get a new address for an existing wallet, you can use-- you can replace null.
[10:03] Offline mode is set to true, indicating we don't want to sync the chain.
[10:07] Interesting.
[10:08] So you can do this offline.
[10:10] It's just local to my computer.
[10:13] Is that for, like, development-- For this thing, yeah.
[10:17] Probably.
[10:18] So the syncing the chain thing, it is actually a client sync.
[10:24] We're not going to be downloading a blockchain, for one.
[10:29] But it's even lighter weight.
[10:33] Like this way, we don't have to have the client sync the headers and things like that either.
[10:37] So is the reason why you could do this because the way you generate a wallet, it always generates
[10:42] a unique one every time?
[10:46] That is, yeah, that's part of it.
[10:49] So yeah, generating the wallet.
[10:52] I'm not sure if I'm answering the question, actually.
[10:56] Well, actually, back up.
[10:59] What is Dash?
[11:01] What is unique about Dash?
[11:02] Because actually, I haven't done any research.
[11:04] I know there's a cryptocurrency called Dash, but the platform-- what's different about
[11:10] the Dash platform?
[11:11] So Dash, high level, yeah.
[11:15] So there's Bitcoin.
[11:16] You've heard of Bitcoin.
[11:17] There's other forks like Litecoin.
[11:20] Have you heard of Litecoin?
[11:21] Yep.
[11:22] Okay.
[11:23] So Dash is very similar in the sense of they're both forks.
[11:28] It's similar to Litecoin in the sense that they're both forks of Bitcoin.
[11:33] But it's very different in the technology choices that we've made since that original
[11:40] fork, which was over 10 years ago.
[11:43] And so Litecoin has made certain different improvements over Bitcoin, or I'll just say
[11:49] changes.
[11:51] And then Dash has made other changes that I personally consider big improvements.
[11:58] But it's, of course, subjective.
[12:02] And so Dash is just-- it's a cryptocurrency that focuses mostly on high speed, low cost,
[12:09] high security, decentralization, all those kind of things.
[12:14] And subjectively or objectively, just a better user experience, better developer experience
[12:20] than you'd get with Bitcoin.
[12:23] Some people say at the expense of security or whatever, but yeah, those are different.
[12:30] Different people will give you different answers on that.
[12:32] But the main difference, I think, is that Dash has a network of what are called master
[12:38] nodes, which are in Bitcoin, anybody can spin up a Bitcoin node and participate in the network
[12:48] as a node operator.
[12:52] You're not doing anything special as a node operator in Bitcoin by design.
[12:59] But in Dash, we have the master node concept, which is in addition to running a node, you're
[13:06] also saying you're also proving that you own a large stake in the network.
[13:10] So it's 1000 Dash.
[13:15] So there's incentive to run a node.
[13:19] There's not only an incentive, but I'm glad you picked up on that, because the node operators
[13:23] do actually get paid.
[13:24] The master node operators get paid part of the block reward, and that incentivizes them
[13:29] to keep a good service running, because otherwise they don't get paid.
[13:34] But it also creates certain efficiencies, because you have that staked node, and so
[13:44] you have better performance, and then you can add on services that these node operators
[13:49] are running.
[13:50] One of those services, one of the major services that they're doing is instant send or instant
[13:57] locking of transactions, which means when a transaction is seen on the network, then
[14:03] a quorum of these master node operators will see those transactions, and they'll say, "Hey,
[14:10] I've seen this."
[14:11] And as long as a certain quorum of those, certain subset of those node operators see
[14:16] the same thing, then they lock that transaction.
[14:19] So instead of waiting for 10 minutes or 20 minutes or however long you want to wait for
[14:24] your Bitcoin transaction to confirm on the network, based on certain block intervals
[14:30] of on average 10 minutes, instead of all that confirmation time business, you can just rely
[14:37] on the fact that if a quorum of master node operators have locked a transaction, you can
[14:44] consider it secure, and you can take it to the bank within one to two seconds instead
[14:50] of minutes.
[14:52] So that's kind of the speed aspect.
[14:57] And then there are other things as well, such as Dash is one of the, well Dash was the first
[15:04] decentralized autonomous organization, or DAO if you've heard of those, where we have,
[15:10] because the master node network, because there's a master node network, then we give each of
[15:17] those node operators one vote, and so that we vote on stuff like governance decisions,
[15:24] like should we increase the block size or those kinds of technical decisions, or even
[15:28] funding decisions where we direct a part of our block reward to developers or marketers
[15:36] or anybody who thinks that they can contribute to the Dash network, that anybody can submit
[15:41] a proposal to get funding and work in Dash, and then those node operators that are incentivized
[15:47] because they have a large stake in the network, they're incentivized to vote well, so they
[15:52] vote for funding, and that's actually how the Dash incubator, which is funding this
[15:58] project and this organization and this livestream, that's how we are funding this.
[16:03] Got it.
[16:04] Okay, well I'm glad I asked.
[16:06] I know I should have asked probably at the very beginning, but now I have a bit more
[16:09] context.
[16:10] I'll also add I've never developed on any blockchain derivative networks, I've only
[16:17] developed on Ethereum, so this will be really interesting.
[16:21] I don't have anything to compare it to yet.
[16:23] Yeah, I was the same way when I first got into Dash, I had done a lot of Ethereum and
[16:29] like some Solana, but not really any Bitcoin stuff, so I learned a bunch, and the Dash
[16:36] platform is totally different from Bitcoin also, so it's not even like really necessarily
[16:41] the best comparison.
[16:42] All right, so I just created a new script file for create_wallet, we'll use three functions
[16:52] to create a wallet, get_wallet_account, export_wallet, and get_unused_address.
[16:57] All right, and it's all coded for me and I'm going to copy it and paste it into our script
[17:01] file, here's the create_wallet function and we're calling it immediately, we have to define
[17:09] these other functions though, right?
[17:13] Or no, it's from our client that we imported, okay.
[17:16] Yeah, so those are all part of the Dash, that's like the built-in methods in the Dash library.
[17:24] Is this good form to log your secret seed phrase into the console?
[17:30] Somebody steal my seed phrase, please, I told you I wouldn't put my social security number
[17:33] on, but we're going to reveal my seed phrase.
[17:36] All right, so, oh, go ahead.
[17:39] No, yeah, it definitely is not good form to do if you're not working on testnet, but for
[17:44] testnet it's fine.
[17:45] Yeah, you got to get it somehow, it has to appear on your screen at some point in time.
[17:50] I've done absolutely no user signup or anything, so it sounds like for the testnet, it just
[17:56] gives you like a default address and mnemonic, or let's see what happens.
[18:00] Yeah, we'll see what happens, it's not default, it's random.
[18:05] Okay, random by default, so we ran it, I don't know what happened, did anything happen, I
[18:11] don't see any files.
[18:12] He didn't save the file before running it.
[18:15] Oh, thanks, Anthony.
[18:17] The white dot gave it away.
[18:19] Okay.
[18:20] There you go.
[18:22] Cool, we got it.
[18:23] There are some warnings, but that's just, that's typical stuff, so.
[18:27] Okay, to be ignored.
[18:29] All right, so this is the wallet address where people can't rob me because it's fake, right?
[18:35] Yep.
[18:36] And my seed code, seed phrase.
[18:39] Yes.
[18:40] Cool.
[18:41] Yeah, you're going to want to copy and paste both of those and put them in your .emv.
[18:44] Okay.
[18:45] Yeah, seed phrase is synonymous with mnemonic, just, you got it, I think.
[18:50] Just like this, yeah.
[18:52] Okay, so I'm going to pop these in here before we lose them.
[18:57] All right.
[19:00] And it says copy these just like we did.
[19:03] Okay, next is to add funds to the wallet with testnet faucet.
[19:06] Oh, I remember faucets.
[19:07] These were such a pain for the developer experience because you'd have to wait for them to drip.
[19:12] If only that was his biggest problem.
[19:16] You get more than a drop this time.
[19:20] Send test funds to unused address from the console output.
[19:24] Testnet faucet.
[19:25] I'm going to open that in the tab.
[19:27] Wait for them to be confirmed.
[19:28] It might take a few minutes.
[19:30] I'll get this kicked off.
[19:33] Lock Explorer.
[19:34] All right, so here's the test faucet.
[19:36] And sorry, my browser isn't Japanese, but that's a captcha.
[19:42] Should I use this promo code?
[19:45] So you'll want to enter your address above the captcha.
[19:48] It's kind of hidden up there.
[19:50] Oh, I see.
[19:51] Okay.
[19:52] Right here.
[19:53] My address here.
[19:54] Yeah, yeah.
[19:55] There you go.
[19:56] That would be this.
[19:57] That's right.
[20:01] Do all addresses start with Y or is this just a coincidence?
[20:04] Say again?
[20:06] Do all wallet addresses start with Y or is this a coincidence?
[20:10] The testnet always starts with Y.
[20:12] Main net addresses start with X.
[20:15] Oh, cool.
[20:16] Okay.
[20:17] So if I click this button, I should get some money?
[20:19] Yep.
[20:20] I like the sound of that.
[20:22] Yeah.
[20:23] And while we're waiting for that, yeah, don't click get coins again.
[20:29] This is a finicky site.
[20:31] You see the browser is loading by, you know, it's doing stuff.
[20:38] Sometimes it crashes.
[20:39] Sometimes it doesn't.
[20:40] I don't know what that said.
[20:42] It said that the confirmation time timed out.
[20:44] But I think we already kicked it off, right?
[20:46] So it's working on it.
[20:48] So let's open the insight tab now and see what's --
[20:51] Yeah.
[20:52] Is there any, like, transaction ID?
[20:54] Oh, wait.
[20:55] Look at that.
[20:56] It went through.
[20:57] It worked.
[20:58] 2.8 dash.
[20:59] Hey, tell me, how much is that in U.S. dollars?
[21:01] If it were main net, then it would be, like, 70 bucks or something.
[21:05] 70 U.S. dollars.
[21:07] Okay.
[21:08] Something like that.
[21:09] So I'm guessing this is the one that we launched a minute ago maybe.
[21:15] We might see the transaction down there.
[21:18] That would be our transaction.
[21:19] 2.8?
[21:20] Is that what we had?
[21:21] 2.86?
[21:23] I don't know.
[21:24] It's similar.
[21:25] Something like that.
[21:27] So let's go ahead and just pop the address into the search for block
[21:31] transaction.
[21:32] Yeah.
[21:33] Wallet address, right?
[21:34] Okay.
[21:35] Okay.
[21:38] Okie dokie.
[21:39] So this is the history of our transactions.
[21:41] I guess maybe some initial transactions happened behind the scenes.
[21:44] Yeah.
[21:47] So on the left, you see the inputs to the transaction.
[21:50] And on the right, you see the outputs.
[21:52] So your address is on the right, meaning it's received funds from the
[21:56] other inputs on the left.
[21:58] That's just kind of how blockchain transactions work.
[22:02] But so far, so good.
[22:04] We're rolling.
[22:05] Cool.
[22:06] All right.
[22:07] So I got money.
[22:09] Fake money.
[22:12] All right.
[22:13] So search wallet, we just did that.
[22:15] By the way, what was this address right here, the first?
[22:22] Good question.
[22:24] That is sending the change back to either the wallet or something that
[22:31] the faucet controls.
[22:34] Okay.
[22:35] So it's like an administrative step in the faucet process?
[22:40] Yeah.
[22:41] I mean, I don't know how much to go into the transaction theory here.
[22:47] But yeah, basically, when you're making a transaction, you're taking -- you
[22:51] can think of it like a bunch of coins that you dump out onto a counter when
[22:55] you're at the gas station or whatever.
[22:57] And you send those coins to the person.
[23:02] And then in order to -- like the sum of the inputs on the left side has to
[23:08] equal the sum of the input/outputs on the right-hand side.
[23:11] So you have to send change back to a certain address because --
[23:16] It's a leaky faucet.
[23:18] Yeah.
[23:19] Well, not all the inputs always add up to exactly what you want to send to.
[23:24] And so the remaining balance has to go back to an address, some kind of
[23:30] address.
[23:31] So if you want to control the change and get the change back as the sender
[23:35] of the transaction, then you want to provide your outputs an address that
[23:40] you control.
[23:41] And so I would assume that the faucet is just sending it back to itself.
[23:45] Got it.
[23:46] So it's like that little penny bar at the gas station for that extra penny
[23:49] change that you don't want to put in your wallet.
[23:52] Yeah.
[23:53] So YTCF9.
[23:55] If you go back to the -- if you go back to the dash faucet --
[24:00] This one?
[24:01] Yep.
[24:02] Okay.
[24:03] So that's -- I was wondering if it might be that address.
[24:06] Oh, going back here, yeah.
[24:07] Wallet will have multiple addresses.
[24:10] Maybe it's not the one that's shown here, but it's probably one that the
[24:13] wallet -- that the faucet owns.
[24:15] Are people donating real money to fund the faucet for the test net?
[24:20] Or what's --
[24:21] No, it's just that if the faucet ran dry for whatever reason, like somebody
[24:25] tried to get all the money, which is why you have to do a CAPTCHA.
[24:29] Sometimes, like, because this is an open network,
[24:32] anybody can interact with it.
[24:34] So if somebody ran it dry and you wanted to interact with it,
[24:38] you could send it some money, some test net funds,
[24:41] and then have it be working again.
[24:43] Got it.
[24:44] Okay, if we have any leftover change at the end of the stream,
[24:46] I'll donate it back just to keep things liquid.
[24:48] But just as a -- just since we're there --
[24:51] Oh, yeah.
[24:52] These faucets, they used to be on Bitcoin.
[24:55] And, like, all of these faucet apps, web apps,
[24:58] they're derived from really old-school faucet.
[25:02] They used to be, like, main net Bitcoin.
[25:04] And so that's one of the reasons why they have these donation addresses as
[25:08] well is because it used to be main net funds that if somebody was feeling
[25:13] generous, like they were an early miner and they mined 50 Bitcoins back in the
[25:17] day and they wanted to, like, spread the message,
[25:19] the good message of Bitcoin or, in our example, Dash,
[25:24] if it were main net, then you could actually send to that.
[25:26] And then people could then go to the faucet and say,
[25:29] "Hey, I want to try this out.
[25:31] And I'll take, like, I'd like to have 50 cents worth,"
[25:35] or something like that.
[25:37] And so, yeah, back in the day, it was very small amounts of money that
[25:42] you would be able to get from these faucets.
[25:44] But it was real money.
[25:45] And if you had hung on to it since the early times,
[25:49] then you would have done pretty well.
[25:50] Oh, yeah.
[25:51] To be a dev back in the day, I would have -- if I had the foresight,
[25:54] I would have just been dripping from the faucet once a day.
[25:57] Yep.
[25:58] I'd be rich right now.
[25:59] Exactly.
[26:00] Yeah, let's go ahead and move forward then.
[26:05] Yeah.
[26:06] Am I, like, behind on time?
[26:07] Do I need to rush?
[26:08] How are we doing?
[26:09] You're fine.
[26:10] We're good.
[26:11] We're good.
[26:12] Because we always -- we'll just go into part two.
[26:14] All right.
[26:15] If you're interested.
[26:16] Cool.
[26:17] Yeah, I got one buddy who's going to be on part three soon.
[26:20] I guess we'll just do part C and B because, yeah.
[26:24] All right.
[26:25] The transaction link.
[26:27] Is this what we just looked at together?
[26:28] Yeah.
[26:29] Okay.
[26:30] Yeah, you skipped it.
[26:31] I skipped the screenshots, yeah.
[26:32] And you can also expand it.
[26:35] For more info.
[26:36] We didn't do that.
[26:37] I'm kind of curious what else we can see in there.
[26:39] Hold on a second.
[26:42] I think I need to refresh.
[26:43] Click forward.
[26:44] Click your forward.
[26:45] Oh, yeah, we have the history.
[26:46] Yeah.
[26:47] All right.
[26:48] I think it's the arrow that you -- or, no.
[26:50] There's a plus right by the big long string right below transactions.
[26:55] Oh, here.
[26:56] Yeah.
[26:58] So that's if you really want to get into the nerdy details of the transactions.
[27:03] That's what I was wondering.
[27:05] How far do I go into this?
[27:06] Well, it's suggested to try it here, so everyone's going to go through it.
[27:10] But I think it's good to know because I never would have found that without being nudged.
[27:14] Absolutely.
[27:15] Okay.
[27:16] Register and retrieve identity.
[27:18] Modify the client.
[27:19] Again, include your mnemonic seed phrase in .env.
[27:22] Okay.
[27:23] So we're going to pluck that out and -- oh, okay.
[27:27] Because we didn't have a mnemonic before.
[27:29] Now we do.
[27:31] I think before in here we had offline modes at the true, but we're not using that anymore.
[27:38] It's going to override the file.
[27:42] All right.
[27:44] Unsafe options.
[27:45] Skip synchronization before height.
[27:47] What is height?
[27:48] I saw this in the -- over here somewhere, too.
[27:52] So basically each block starting with the first one is like height one.
[27:56] The second block is height two.
[27:58] It's like the pancake stack.
[28:01] Okay.
[28:02] Yeah, exactly.
[28:03] All right.
[28:05] So we are setting up our client with new configuration.
[28:08] I don't know what this does, but I'm just going to --
[28:11] So you don't have to sync the whole chain, the whole chain history.
[28:14] Okay.
[28:15] It just, like, looks at the last, you know, month of blocks or whatever.
[28:19] Got it.
[28:21] So if you actually wanted to implement this, you would probably go and look at the insights
[28:25] and find out what would be an appropriate height to put in there?
[28:29] Yeah, that's just kind of, like, the default right now.
[28:32] Okay.
[28:33] Next script, create identity.js.
[28:36] We will run identities.register function.
[28:42] What is an identity?
[28:43] Is it, like, a profile within a wallet?
[28:48] I don't know.
[28:51] So --
[28:53] Yeah, the way I describe it is it's just -- it's a public/private key pair,
[28:57] essentially.
[28:58] Oh, okay.
[28:59] This is what people will see in the public one they'll see on the transactions.
[29:04] So you're familiar with the concepts of SSHing and doing SSH key pairs and
[29:11] generations and things like that.
[29:13] You can kind of think of that as, like, an identity for your SSH server.
[29:19] Got it.
[29:20] Same idea, but it uses a little different cryptographic primitives.
[29:27] Cool.
[29:28] All right.
[29:29] So we've got the script there.
[29:34] It's going to create a new identity and count to log it and ask us to go to some
[29:39] website.
[29:40] So let's check it out.
[29:42] Create identity.
[29:44] All right.
[29:45] Ignore warnings; right?
[29:47] Yeah.
[29:50] And as that's waiting, I'll explain a little bit more about the identity
[29:53] stuff.
[29:55] One of the beauties of blockchains and decentralized cryptocurrencies in
[30:00] general is that as opposed to something like the traditional banking system
[30:05] where your identity in their system is something they give you; right?
[30:10] You go open an account at a bank, they're going to give you an identifier,
[30:16] like they're going to create an account for you, and it lives on their system.
[30:20] In blockchains, the role is completely flipped where the users --
[30:25] Tell us who you want to be.
[30:27] Yeah, the users actually create their identities, and then that's what's the
[30:31] authoritative identity system rather than --
[30:34] And that's what we just did; right?
[30:35] With the create identity script.
[30:37] When we ran register, we created our identity.
[30:40] Now I'm going to go where it told me to go.
[30:45] So this is the Dash platform that we're on right now; right?
[30:48] Yeah, this is an explorer, platform explorer.
[30:53] There are different ways to view things that are happening on a blockchain.
[31:00] The best, most, like closest to the metal way to do that is to run an actual
[31:06] node on the network.
[31:08] But that's resource intensive and takes time, and, you know, a lot of people
[31:14] don't have the technical chops to do that.
[31:16] So other people who can do that, like our good friend and colleague,
[31:21] Mikhail Shenmik, he has built this website that does that crawling
[31:28] of the blockchain itself.
[31:30] He's running a node.
[31:31] He's running an indexer on top of that node, which looks through all the
[31:34] transactions, organizes them in certain ways, provides a REST API,
[31:41] that this front end that he's also created would then contact and get
[31:46] information that originates from the blockchain but is presented
[31:52] in an easier-to-consume way.
[31:55] So that's what this platform explorer is.
[31:58] It's just a way to look at what's happening on the Dash platform blockchain.
[32:04] Very cool.
[32:06] I'm a freeloader, so I'll use the monitor version.
[32:09] And that's cool that you have an API.
[32:11] I'm guessing all of these are, like, get operations just for monitoring
[32:14] stuff that happens on the network?
[32:16] - Yep.
[32:17] - Nice.
[32:18] - Yeah.
[32:19] Actually, I don't even know if anybody has looked at this API site.
[32:23] Yeah.
[32:24] I checked that once.
[32:26] - Yeah?
[32:27] I used to work at Postman, so I saw this word "API," and I'm like,
[32:29] "Got to check this out."
[32:30] - Yeah.
[32:31] Yeah, that's right.
[32:32] - I was going to ask, do you have a Postman collection?
[32:34] Because it would be really cool if people could just, like,
[32:36] look at this and they could run all these examples in, like, one click.
[32:40] It would be pretty cool.
[32:41] - You know, I wasn't going to say the name Postman, but you had put it offscreen,
[32:45] so I didn't know if you wanted to share that.
[32:47] But that is very cool that you used to work for Postman,
[32:50] which is, for anybody who doesn't know, it's watching a very popular API client.
[32:55] Or you could explain it better than me.
[32:57] But, yeah, I don't know if we have that yet.
[33:00] I don't think we do.
[33:01] - Well, if I play with this more, I'll make a fan public Postman collection
[33:05] and play with it that way.
[33:07] - Yeah.
[33:08] - But cool.
[33:09] So even if you aren't using the API, you can just use this UI to see what's going on.
[33:13] Now, I see right here there was an identity create that happened today.
[33:18] I'm guessing that's me.
[33:19] - Yeah, that's the one that just happened.
[33:22] - Is this, like, the event ID and this is our identifier?
[33:26] What are we looking for?
[33:27] Maybe I should read it.
[33:28] - So click the thing.
[33:29] Click the create identity or identity create.
[33:32] - This guy, okay.
[33:33] - Yes.
[33:34] - So there's a specific transaction for.
[33:37] So, okay, this is state transition, that's what it says.
[33:41] So there's this thing they call state transition.
[33:43] It's basically that's, like, writing to the blockchain.
[33:46] - Right.
[33:47] And here's the hash of the block.
[33:48] - Yeah.
[33:49] So there's the identity ID itself and then there's the, like, this is the hash
[33:54] for the state transition, I believe, is what's happening.
[33:57] - So this is my new identity?
[33:59] - Yep.
[34:00] - 32A4N.
[34:01] That's how you should refer to me from now on.
[34:03] - Okay.
[34:04] - If I click on this, what do I learn about myself?
[34:09] Oh, it takes us.
[34:10] - Your balance.
[34:11] - It learns when I was born.
[34:14] - Yep.
[34:15] - I'm not in the system.
[34:17] - Well, you're not a system.
[34:19] Yeah, you're not the system.
[34:21] - But I'm rich.
[34:22] - Yeah.
[34:23] And that 1,000, whatever that number is, that's because we defined that in our
[34:29] request to make the transaction.
[34:31] That's what we said, one something.
[34:34] If you look back to your code, that's what you'd see.
[34:37] - Oh, I see.
[34:38] I can tell...
[34:39] Did we say 1,000 anywhere?
[34:41] - No, that's...
[34:42] You can think of the top-up credit function, Rion.
[34:45] - Oh, okay.
[34:46] - How do you have a balance then?
[34:48] - So there's an instant balance when you create the identity.
[34:53] There's some amount...
[34:54] And this is why you need the testnet funds to create the identity.
[34:57] You can't create an identity if your balance is zero.
[35:01] - I see.
[35:02] So we used our testnet funds to create the wallet, or excuse me, the identity?
[35:06] - To create the identity, yeah.
[35:08] Because there's...
[35:09] Basically, why they're called credits is because you have Dash in your wallet,
[35:12] and then when you go to the platform, you have this thing called credits.
[35:16] And so there'll be a part where you do something called top-up credits where
[35:19] you'll add more credits from your original Dash that you got from the faucet.
[35:24] - This is really fascinating.
[35:26] And I'm so glad that I can do this without adding my credit card to anything,
[35:30] knowing that I'm not sinking my savings.
[35:34] - Yeah, you're speaking Rion's language.
[35:36] - Yeah, I love it.
[35:37] I love it.
[35:38] I hope that the world moves this direction where people own their own money
[35:43] independent of banks and all that stuff.
[35:46] This should be in our full control.
[35:48] So, yeah, I'm glad that...
[35:49] - Yeah, that's what Michael's saying.
[35:51] So this is what I was saying.
[35:52] The create identity does a top-up kind of under the hood.
[35:55] - Yeah, and that's what I thought.
[35:57] But we define the number that it creates to do the top-up in the
[36:04] identity creation, did we not?
[36:07] - We did not.
[36:08] There may be a way to configure that.
[36:10] - I think it really has a default.
[36:12] - Okay.
[36:13] I'll have to look into that.
[36:14] - Yeah.
[36:16] Cool.
[36:17] So I've saved my new identity.
[36:20] You know, call me 32A4N.
[36:24] - But only for a short time, Clara, because you're going to actually get a real
[36:28] name soon.
[36:29] - Well, everything is ephemeral.
[36:31] - Yeah.
[36:32] - So earlier we saw...
[36:33] Oh, yeah, go ahead, Anthony.
[36:35] - Yeah, so the register function has a parameter called funding amount,
[36:40] which is default to 10,000.
[36:43] - Oh, okay.
[36:44] - You can change it if you want.
[36:45] - So if I wanted to change that, I would, like, you know,
[36:48] say in here default amount and set it to, like, 10 billion to be richer?
[36:53] - Something like that might exist, but I don't know the specific API.
[36:57] - Okay.
[36:58] Cool.
[36:59] Well, we got money anyway.
[37:00] Or credits, right?
[37:02] Not money.
[37:03] And next step.
[37:05] Earlier we saw how to view our transactions.
[37:07] We did this before in the identities tab.
[37:09] We clicked in here.
[37:12] And outputs to terminal.
[37:13] Yeah, so we clicked the terminal link from the terminal,
[37:16] inspected the identity creation.
[37:19] All right.
[37:20] So next we're going to make a retrieve identity script.
[37:27] And get IDs.
[37:31] Get identity IDs on our wallet identities.
[37:34] Okay.
[37:35] Copy the script and paste it into retrieve identities.
[37:42] And we're just going to -- that's it.
[37:44] We just call this SDK.
[37:45] I'm guessing it's using that API under the hood maybe.
[37:48] Or a different API.
[37:50] - Different API.
[37:51] - I'm just curious.
[37:52] Okay.
[37:53] All right.
[37:54] We're going to run this script.
[37:57] NPM run retrieve identities.
[38:00] That is very nice that you added all the scripts and packed JSON for us.
[38:05] All right.
[38:06] What did I break?
[38:08] Did I forget to save something?
[38:10] - The SPV chain.
[38:12] - Yeah.
[38:13] This function, for some reason, always has something weird happening with it.
[38:19] But we can skip this one because it's not really a huge deal.
[38:23] We've been talking about possibly doing usually like a local version of testnet.
[38:29] But we made it through the important commands that are actually blockers.
[38:33] So we should probably keep going with testnet for now.
[38:36] All retrieve does is it just gives you back the identity that you just created.
[38:39] So it's not really --
[38:40] - Cool.
[38:41] And this is like identities associated with your wallet.
[38:44] - Yeah.
[38:45] So your wallet can have multiple identities.
[38:47] - Okay.
[38:48] Cool.
[38:49] Okay.
[38:50] So good thing we have good short-term memory.
[38:52] We already know our identity.
[38:53] So we don't need to retrieve it.
[38:55] And we know our balance.
[38:57] All right.
[38:58] So when identity is created -- where should I skip to, Anthony?
[39:02] - So top up.
[39:04] We need to do top up.
[39:05] Because actually you skip this one.
[39:07] So just keep going from here.
[39:09] - Top up?
[39:10] - Yeah.
[39:11] - Cool.
[39:12] Top up identities.
[39:13] We're going to add a little credits here.
[39:17] We're going to use get identities again.
[39:18] Are we going to get blocked?
[39:22] - I don't think so.
[39:23] We'll see.
[39:25] - It's not -- we know our identity.
[39:26] So we could hard code it.
[39:31] - Okay.
[39:32] So we're going to loop through.
[39:33] I hope it works.
[39:34] We're going to loop through the IDs and top them up.
[39:37] Just the top up function.
[39:39] - Yeah.
[39:40] This is what I was thinking of.
[39:41] I thought we were at this step for some reason.
[39:43] My mind was -- yeah.
[39:44] Anyway.
[39:45] - That's what I was thinking.
[39:46] - Yep.
[39:47] - I see.
[39:48] Okay.
[39:49] - So we're going to add that much more credit to our account.
[39:50] - Yeah.
[39:51] I hope this works.
[39:52] Because we couldn't get this function to work in the last step.
[39:54] But let's see.
[39:55] - Yeah.
[39:56] You would think that that would be the case.
[39:57] But we'll see.
[39:58] - Well, I can always be surprised by code.
[40:03] Hey, hey.
[40:04] Just warnings.
[40:05] Just warnings.
[40:08] Okay.
[40:09] Something's happening.
[40:10] That's good.
[40:12] There's some crunching happening on the network.
[40:15] - Yeah.
[40:16] And while it's doing that, I'll say a few things about the network that we're
[40:19] working with right now.
[40:20] It's testnet.
[40:21] It's basically a network that dash core group, a different entity that is
[40:25] funded by the dash network itself.
[40:28] They maintain this network.
[40:30] And the network's generally healthy.
[40:33] But the SDK that we're using is a little bit out of date.
[40:38] They're focusing mostly on the rust SDK right now.
[40:41] And the JavaScript SDK is a little bit, well, rusty, I guess you could say.
[40:48] But, yeah, so sometimes we'll see errors that are associated with the SDK.
[40:55] And sometimes we'll see errors that are associated with the network.
[40:59] Let's see.
[41:00] - This one looks SDK-related from before.
[41:02] - It's the empty SPV chain error again.
[41:04] - No, no.
[41:05] That was before.
[41:06] Sorry.
[41:07] - Oh, that was before.
[41:08] - Yeah, yeah.
[41:09] But, yeah.
[41:10] So that's the type of error where it says empty SPV chain.
[41:11] That's one where it usually just means that it's tried to sync to a node that
[41:16] was wonky for whatever reason.
[41:19] And it's not able to retry.
[41:21] Or it is able to retry, but it doesn't do enough to actually figure it out.
[41:25] So, yeah, see?
[41:26] Told you.
[41:27] - So it looks like we got it this time.
[41:29] - Yeah, we have.
[41:30] We've topped up.
[41:32] I know we told it to put, like, 10,000 in each one, but we have slightly less
[41:36] than that.
[41:37] Is there, like, a transaction fee?
[41:39] - Yeah.
[41:40] Every interaction that modifies data, does actual state transition on the
[41:47] network, costs money.
[41:49] - Okay.
[41:50] So we had a tax of about 13%.
[41:53] - Yeah.
[41:54] Yeah.
[41:55] I'd have to look at the actual numbers again, but I think you're right.
[42:00] - Yeah.
[42:01] I'm used to a crypto world where you just expect your money to, like,
[42:05] disappear at various steps of the process.
[42:08] - Yeah.
[42:10] - Okay.
[42:12] Next.
[42:13] Register and retrieve name.
[42:14] Okay.
[42:15] Name.
[42:16] We had an identity.
[42:17] Now we're going to get a name, which is probably something that's easier to
[42:19] remember than 34-2a-n.
[42:23] Create a label property in the environment variables.
[42:26] Replace your name here with our name.
[42:28] So we have power to decide whatever we want?
[42:31] - Yep.
[42:34] - Who should I be?
[42:35] I don't want to put my real name here.
[42:38] Or will I?
[42:40] I will.
[42:42] I'll be Clairfro.
[42:43] Is it, like, conventional to do a screaming case?
[42:46] I see a lot of caps.
[42:49] - If it's conventional for you, then great.
[42:52] For now, just the other side.
[42:54] - Probably lowercase.
[42:56] Because I think it's kind of like a domain.
[42:58] Because it's going to have dots.
[43:00] It's going to be Clairfro.
[43:01] - Okay.
[43:02] - Clairfro.dash.
[43:03] - I shouldn't dare to be different.
[43:06] All right.
[43:07] We're going to add the script to register name.
[43:13] Register name.js.
[43:15] Whoa, didn't copy the script.
[43:18] Now I have.
[43:21] Oh, I was using a non-Mac earlier today.
[43:25] And now I'm on a Mac.
[43:26] And I can't copy/paste.
[43:28] My muscle memory is all messed up.
[43:30] Okay.
[43:34] Oops.
[43:36] So register name.
[43:37] We're going to pull our identity ID and label from .env.
[43:40] And get our identity by ID.
[43:45] And get the ID of the identity.
[43:48] Interesting.
[43:49] Is it a different -- it's a unique identity ID.
[43:54] I thought IDs were unique.
[43:57] - Yeah, the identity is actually an object or something, I guess.
[44:02] - Oh, okay.
[44:03] - Get the ID from it.
[44:06] - I got it.
[44:07] Okay.
[44:08] And we're going to create a new name registration on the client platform
[44:11] names that register.
[44:13] Here's what you were talking about, Anthony.
[44:15] Right?
[44:16] - Yeah, exactly.
[44:18] - And so here I could actually change this technically to be my own suffix.
[44:24] - Yeah, I don't actually know how this works.
[44:26] But I don't think it would work if you changed it to anything other than
[44:29] dash.
[44:30] - It has to be .dash, yeah.
[44:32] - It's interesting that you have the option to not put dash there.
[44:35] - Well, you don't.
[44:36] I mean, well, you do, but the code would break.
[44:38] So, like, that's why it's written this way.
[44:40] - Well, I mean, like, the SDK would be cool if, like,
[44:42] it took the label as a property and, like, did this for you.
[44:44] Otherwise --
[44:45] - Right.
[44:46] - Fat finger it.
[44:48] - It makes it look like you have a choice, but you don't, really.
[44:52] - Oh, the wild west of crypto.
[44:54] There's always some way to mess stuff up.
[44:57] Okay.
[44:58] So we're going to pass it some property, the unique ID, and the identity.
[45:01] What is an object, right?
[45:03] And we're going to put something out.
[45:06] We're going to get this label we made and then view it.
[45:11] All right, let's check it out.
[45:12] So we're going to run.
[45:18] Register name.
[45:21] And this operation, does it take dash to perform or is this on credits?
[45:28] - I think everything should be credits.
[45:30] - Everything should be credits.
[45:31] - That's done on platform, yeah.
[45:32] - Okay.
[45:33] So the only thing we've used dash for so far was making an identity.
[45:37] - Yeah.
[45:38] I mean, in some sense, everything that is a credit is dash as well.
[45:42] Dash, a credit is just a certain denomination of dash.
[45:45] - Oh.
[45:46] - It was --
[45:47] - Like dollars and cents.
[45:49] - Yes, exactly.
[45:51] - Okay.
[45:52] All right.
[45:53] We have Clarefro.
[45:55] Let's check it out on the block explorer.
[45:57] All right.
[46:01] So here is my name, my unique identity, my old identity, 32A4N.
[46:12] We have solved subdomain rules, a lot of subdomains, false, normalized label.
[46:17] Oh, you gave me, like, a leet label, too.
[46:19] That's cool.
[46:24] Okay.
[46:25] So what are we looking at here?
[46:30] View on the platform.
[46:32] Okay.
[46:33] Is there anything we should note here?
[46:37] - Not really.
[46:38] You already noticed the one thing that is -- might be surprising, that the name
[46:45] that you actually request gets modified under the hood.
[46:49] And that's basically so that it helps prevent -- what are they called?
[46:57] - People trying to, like, typosquat your label?
[47:00] Okay.
[47:01] - Yeah.
[47:02] - Well, there's more than one way to typosquat.
[47:04] - I could still think of some ways I could typosquat my own ID here.
[47:09] - Right.
[47:10] They become at least more recognizable.
[47:13] Yeah.
[47:15] - So if someone, like, tried to send money to this address, you might, like,
[47:18] pop up a warning that says, like, are you sure you want to talk -- or send money
[47:21] to this address?
[47:23] - Yeah.
[47:24] - Oh, that's cool.
[47:25] That's an interesting feature.
[47:29] Awesome.
[47:30] Okay.
[47:31] And then we'll retrieve name.
[47:33] Let's do it.
[47:35] And here's the script.
[47:38] Extended doc.
[47:41] Okay.
[47:42] So we're going to get -- we're going to look for our name.
[47:46] And we have to stringify and JSON parse this doc.
[47:53] What's a doc in this context?
[47:57] - Yeah, so that will make more sense as we go, but basically that's going to be
[48:01] what you're going to be able -- now that you have an identity, you'll be able to
[48:05] create documents, which is, like, kind of like a document database.
[48:11] You'll have just objects with data, and there will be some sort of schema that
[48:16] you can write to those with what are called notes.
[48:20] - Okay.
[48:21] And these are, like, filtered to be for my table?
[48:25] Related to that?
[48:27] - Yep.
[48:28] - Yes.
[48:31] - So let's run that.
[48:33] See what comes back.
[48:34] I'm very curious.
[48:36] Okay.
[48:38] - Yeah, so this is, like, a document, basically.
[48:42] - All right.
[48:49] Oh, and I can look at it here.
[48:57] This looks familiar.
[48:59] Okay.
[49:02] And -- oh, it looks like Anthony did this yourself.
[49:11] - Is there anything you want to call out about this?
[49:21] The name object?
[49:23] - No, I don't think so.
[49:26] So it says data contract in there.
[49:29] So that's what we're going to create next is data contract.
[49:35] So data contract is what allows you to create the documents.
[49:38] Like, data contract is the schema.
[49:41] It's kind of hard to -- the terminology is all a little bit confusing.
[49:44] But once you go through the examples, it becomes pretty clear.
[49:48] - All right.
[49:50] Trust the process, it sounds like.
[49:52] - Yeah.
[49:53] - Data contract.
[49:55] So it serves as a blueprint for the structure of data that an application
[49:58] intends to store on the network.
[50:00] It defines a schema of documents with JSON schema.
[50:03] Contracts enable the platform to validate data against these schemas.
[50:08] Okay.
[50:09] Cool.
[50:10] They're crucial for dApps and provide a structured,
[50:13] predictable way to interact with the blockchain.
[50:16] Oh, cool.
[50:17] - Real quick, we got a question in the chat, Rion.
[50:19] - Yeah.
[50:20] - Asking how Dash platform would solve potential scalability problem.
[50:26] - Well, the potential scalability problem -- I mean,
[50:30] this is one of the three things that blockchains are trying to solve
[50:34] simultaneously in general is -- well, Vitalik Buterin famously submitted his
[50:44] trilemma where you have -- where you're trying to do three things.
[50:51] A blockchain is trying to do scalability, security,
[50:57] decentralization, and scale.
[51:00] And that is -- historically it's been difficult to get all those three
[51:08] things at the same time.
[51:13] Yeah.
[51:15] And I actually -- I personally -- scalability, security, decentralization.
[51:25] I don't like his three choice, personally.
[51:28] I think it's more about security, scalability, and usability,
[51:34] meaning, like, features.
[51:37] So decentralization isn't -- is part of security, in my mind,
[51:42] is what I'm trying to say.
[51:43] So it shouldn't be one of the independent things.
[51:47] But it's difficult to do all these three things at the same time.
[51:51] And so I think to answer the question, the secret behind scalability for Dash,
[51:58] or not the secret, but just the approach, the strategy,
[52:02] is that we use incentivized nodes.
[52:05] Our node operators are paid to scale.
[52:09] So the argument goes that you can't have -- you can't have scale without
[52:17] sacrificing decentralization.
[52:20] Because if you think about it, the argument goes if you -- the bigger you
[52:26] scale, the more difficult it becomes to run a node on the network,
[52:32] because there's a high scale.
[52:34] And so the more difficult it becomes to run a node on the network,
[52:38] fewer people will do that because it's more difficult.
[52:42] And that is true in a network that does not pay the node operators.
[52:48] But once you start paying the node operators,
[52:51] then scale is actually a good thing.
[52:55] The more it scales, the more the node operators make,
[52:59] the more money the node operators make for operating that network.
[53:03] And therefore, there's no real tradeoff between security and scalability.
[53:14] But it's a deep topic.
[53:15] So I won't pretend that I've just solved the world's problems there.
[53:21] I know that you mentally model the trilemma differently.
[53:24] You said instead of decentralization down there,
[53:27] you would put usability and that you feel decentralization is part of security.
[53:31] But if you were to look at Vitalik's model, where would you put Dash?
[53:35] Which leg of the triangle would it be on?
[53:39] Well, I wouldn't put Dash in any part of the triangle.
[53:43] Every cryptocurrency and every network really is trying to do all of them.
[53:50] So I would put Dash in the middle, meaning you have to balance and have --
[53:56] Well, I think what she means, though, is --
[53:58] That's where you want to be, of course, but where is it in reality?
[54:00] Where is the strength?
[54:02] Yeah, some are more decentralized than others.
[54:04] Some are more scalable than others, you know?
[54:06] Yeah.
[54:07] So, again, yeah, I wouldn't put decentralization on there.
[54:11] And I would say that it's probably aimed more at the usability part of the spectrum
[54:20] or whatever we're calling this because that is --
[54:26] So, like, that's why we created Platform in the first place is to give developers
[54:32] like yourself the ability to easily create applications that use this platform.
[54:39] And so giving developers the ability to create all sorts of applications easily,
[54:46] as easily as they can create a database schema, for example.
[54:53] Got it.
[54:55] Cool.
[54:56] Well, thanks for the segue.
[54:58] How are we doing on time, by the way?
[55:00] We have 25 minutes.
[55:01] We're good.
[55:02] We're good?
[55:03] Yeah.
[55:04] So, yeah, we usually go through a little over an hour.
[55:06] So we'll get as far as we want to get.
[55:08] But what were you going to say, Anthony?
[55:10] Sorry.
[55:11] No, just that we might be a little bit short on time,
[55:16] but that's probably okay if we want to do another one.
[55:21] Well, I can always speed it up.
[55:23] I definitely -- I've been very vocal about my questions along the way,
[55:26] and I can tone that down a little too.
[55:28] No, I think that's even more important that you ask your questions because,
[55:32] like, if you're interested -- hopefully you are interested in doing some of this
[55:37] stuff, and we're trying, like, the Dash Incubator,
[55:42] the whole purpose of the Dash Incubator is to help folks like yourself get your
[55:46] questions answered, that if you're interested in it,
[55:49] that you could actually even submit a proposal for yourself to get funding or
[55:53] work through the Incubator or just try to develop an application that you try
[55:59] to gain users, like normal entrepreneurial activity, that kind of stuff.
[56:03] So we're here for you is the bottom line.
[56:07] Awesome.
[56:08] Also, I'm paid by the stream, so take your sweet time.
[56:14] In that case, I'm going to talk real slow.
[56:18] Next script is register contract.
[56:20] Oh, so we're going to make a contract.
[56:21] Awesome.
[56:22] This is the best part of being a blockchain developer is the whole reason that
[56:25] they exist.
[56:26] So -- all right.
[56:30] I'm going to paste this into our new script file.
[56:36] Getting that identity, we're making some of those documents -- not document
[56:40] object -- that, thank goodness, I could copy/paste the code.
[56:45] Don't know what it does.
[56:47] So we're going to create a contract with the configuration above for the
[56:52] identity we give it, and it's going to spit out the contract.
[56:57] We can look at it.
[56:58] Cool.
[56:59] Let's do it.
[57:10] Oh, that was fast.
[57:13] So it's not done yet.
[57:14] It's not quite done, actually.
[57:16] Does it make the contract ID locally, or is this some ping back from the
[57:21] network?
[57:23] I'm pretty sure -- we haven't actually dug into that, but I think it's
[57:26] client side.
[57:27] That part of it, anyway.
[57:30] Interesting.
[57:32] How does it avoid having a clash with another contract ID if it's client
[57:37] generated?
[57:38] Yeah, my guess is it's a combination of -- like, it's a deterministic
[57:43] process that uses both the data that you're trying to create and your
[57:50] identity.
[57:51] So if you tried to do the exact same thing again, you probably did the
[57:55] same thing.
[57:57] So contract ID is generated from the owner ID and entropy 32 bytes content
[58:02] media type.
[58:04] Maybe the current time stamp or something.
[58:06] I don't know.
[58:09] So this is the contract we just made.
[58:13] Owned by me.
[58:14] Remember my old wallet identity.
[58:21] Cool.
[58:22] I don't know a lot about the contract that we created, but it exists.
[58:28] Yeah, so have you ever worked with a document database like MongoDB?
[58:37] The idea is very similar.
[58:39] And it was kind of designed on that basis that you first -- in a document
[58:46] database, you create a schema where you're -- the documents that would
[58:52] adhere to that schema.
[58:55] And then the documents themselves are like instances that adhere to that
[58:59] schema.
[59:00] So it's the same kind of concept of a document database.
[59:03] Yeah, that's document.
[59:05] But I mean the contract itself.
[59:07] I don't really know what we made.
[59:09] But let's get it.
[59:10] Because I just got the retrieve contract.
[59:12] I'm guessing it's going to give us similar data to what we just saw in the
[59:15] dashboard.
[59:16] But let's see.
[59:19] Retrieve contract.
[59:21] Contract.
[59:22] Yeah, the contract is very much like a schema.
[59:26] It says that this contract says that documents that are created against it
[59:33] have to have certain properties.
[59:40] We got an error here.
[59:42] So let's see.
[59:44] It's expressing a buffer.
[59:46] But I don't think it's something we passed into it.
[59:49] We've only passed in contract ID.
[59:53] Did we update the environment file?
[59:57] Oh, contract ID.
[59:58] I don't think I put it in there.
[60:01] That's correct.
[60:04] Let me get out of here.
[60:13] I definitely saw -- oh, it's not in our command history.
[60:16] It was in the output.
[60:17] But here it is.
[60:18] Here it is.
[60:19] And let's try that again.
[60:26] Error driven learning.
[60:28] Yep.
[60:29] All right.
[60:31] So actually, I think this is what it output before when we created it,
[60:34] if I'm not mistaken.
[60:36] And this is the same URL.
[60:38] But now we're just getting it contract by ID this time.
[60:41] Is that like a hobby of yours to memorize random strings of characters?
[60:45] This is the first time we had a capital F identifier,
[60:49] and I saw it right here.
[60:52] So -- oh, that was the -- yeah, the contract ID.
[60:55] Okay.
[60:56] So cool.
[60:57] So we can get it with the SDK.
[61:00] And it has the schema that we defined.
[61:04] And took a look.
[61:05] Okay.
[61:06] Update contract.
[61:07] What are we going to do now?
[61:08] Let's see.
[61:11] Get the existing contract and its schema and change the author or add
[61:17] property called author, because I don't think we have one yet.
[61:23] And this is JSON schema, right?
[61:25] Yeah, that's right.
[61:26] Okay.
[61:29] So we're then going to update it to add author.
[61:36] Okay.
[61:37] Let's try it.
[61:39] Here's the update contract.
[61:48] No, I'm just going to copy.
[62:10] Are these properties like metadata about the contract,
[62:13] or what are these properties for?
[62:17] Yeah.
[62:19] So if you looked at the -- go back to the code, your code editor.
[62:25] Update contract.
[62:27] Yeah, this code right here.
[62:29] Basically it's -- what are we doing here?
[62:31] Update data contract, set documents, schema, note.
[62:38] What update is it actually making here, Anthony?
[62:43] Oh, it's adding -- right.
[62:45] That's right.
[62:46] Yeah.
[62:47] So it's adding a new property.
[62:49] Yeah.
[62:50] Yeah, I'm just wondering what these properties are for.
[62:53] It would be like if you had a database and you decided in your
[62:56] application, uh-oh, we need another property in this -- in the schema.
[63:03] And then you'd have to do a database migration to make all of your data
[63:09] adhere to that new property.
[63:13] That's kind of like what it's doing.
[63:15] Okay.
[63:17] So it's for dApps.
[63:19] Yes.
[63:20] That's right.
[63:22] And that would probably make sense more -- it makes more sense after
[63:26] you've done the document creation, because then it's like, oh,
[63:30] like, okay, now I know I can't create a document that has a required
[63:34] field of author that's not there.
[63:37] Cool.
[63:38] And now we're actually going to do that, right?
[63:40] Because we're going to go back to our client.js and overwrite
[63:43] everything.
[63:44] Yep.
[63:45] So that we -- we give a name to the contract now, it sounds like.
[63:50] Or this is free form, I'm guessing, on line 14.
[63:55] The name of our app.
[63:57] This allows you to create kind of like a shorthand syntax for calling
[64:01] the note from the contract in particular.
[64:07] So it's like a name for our app, essentially, a nickname.
[64:10] And we give it a contract.
[64:12] Am I doing that right?
[64:14] Okay.
[64:15] Yep.
[64:16] All right.
[64:17] So we don't run anything yet.
[64:21] So submit note document.
[64:26] Which is going to be -- get our identity, create a new note document.
[64:34] That's where it says tutorial contract.note.
[64:37] That's what you're able to do, because you set that in your client.
[64:42] Got it.
[64:43] And this is a property we named earlier, right, inside of our data schema.
[64:49] So hello, blah, blah, blah.
[64:52] Broadcast.
[64:53] Okay.
[64:54] So this is when it gets broadcast to the network.
[64:56] Create the note.
[65:00] Awesome.
[65:01] So now we have -- the contract is already live on the network.
[65:05] Now what we're doing is we're submitting a document that adheres to
[65:09] that contract.
[65:15] And then the network will do the job of validating whether or not our
[65:20] document is in compliance with the contract.
[65:24] So, in theory, this would allow you to set up an application where both
[65:31] your front-end application, but also anyone else's front-end application,
[65:36] could submit documents to the same contract.
[65:39] Very cool.
[65:40] It sounds like almost there needs to be, like,
[65:42] an interface management system for these dApps, right?
[65:46] It's like an API almost to make sure --
[65:48] Exactly what it is, yeah.
[65:49] Yeah.
[65:52] Awesome.
[65:54] I want to run this one.
[65:55] This is going to be --
[66:01] So if you made, like, an application,
[66:03] you'd be sending these documents as kind of records, I guess, in --
[66:08] Yep.
[66:15] So that's why -- that's part of --
[66:17] Dash Platform consists of a lot of different components.
[66:20] Two of the main components are the Dash Drive and then the Dash API,
[66:27] or the decentralized API.
[66:29] You might see it somewhere in documentation.
[66:31] You'll see Dash Drive and DAPI, D-A-P-I.
[66:36] That's exactly what you were talking about.
[66:39] It's like an API because it is an API.
[66:41] And it's a decentralized API that anybody can access as long as they pay
[66:47] the money to submit their documents to store on the decentralized drive,
[66:53] and you do that through the decentralized API.
[66:57] Cool.
[66:58] And for now we just have to remember the schema in our head
[67:01] and hope that we don't type it wrong.
[67:06] Where did we just do that operation?
[67:08] Let's see.
[67:13] Here.
[67:15] Yep.
[67:16] Yeah.
[67:17] Okay.
[67:18] All right.
[67:19] So we created the document.
[67:20] It looks like it's been broadcast.
[67:22] And I wonder -- next step is to get the documents.
[67:26] I kind of want to see -- you can do that in the Explorer, too?
[67:29] Yep.
[67:33] Okay.
[67:34] I think I just added this in there actually while we were talking.
[67:39] Get documents.
[67:40] Yeah.
[67:42] And let's run it.
[67:45] I'm guessing it's what we just saw up here on the create.
[67:49] Or not.
[67:51] Oh, we actually read the document.
[67:52] Okay.
[67:54] Because in the code here we're getting that property note.
[68:00] That's right, yeah.
[68:02] That's cool.
[68:03] Awesome.
[68:04] So we just read this document off of a decentralized network is what just
[68:09] happened.
[68:10] Yep.
[68:11] Sweet.
[68:12] That's our hello world right there.
[68:13] That's the hello world right there.
[68:15] That's right, it is.
[68:18] And here's where you can say goodbye world.
[68:25] Time to say goodbye.
[68:27] Update.
[68:28] Can't take the bear market anymore.
[68:31] This is about as far into crypto as I'll go.
[68:37] I just logged into Coinbase for the first time in like two years.
[68:40] And I realized I have $10 I didn't know I had.
[68:43] You missed your chance.
[68:45] That would have been $100 a month ago.
[68:47] It's all about the timing.
[68:49] Depending on what you were holding.
[68:51] We're going to update this note.
[68:53] So this is kind of like the REST analogy of making like a patch request
[68:57] or a put request in HTTP.
[69:02] And we're going to change to a new hello again with a new date string.
[69:09] Let's see if that works.
[69:15] It's pretty fast.
[69:17] Oh, did I mess up something?
[69:20] Yeah, so this happened with Rishi also.
[69:23] I'm not sure what's causing this issue.
[69:26] I'm curious if I get it again, if anything changed.
[69:32] As in that transaction failed.
[69:34] Yeah, because there's no again here.
[69:35] So we didn't quite succeed in updating.
[69:38] Should I try update again?
[69:40] Sure.
[69:44] I haven't watched through the end of that last one that you did with Rishi.
[69:48] What are we seeing here?
[69:51] An error.
[69:53] So stay right there.
[69:57] So it's query storage protocol value error, structure error, value are not bytes,
[70:03] a string or an array of values representing bytes.
[70:09] Is there anything I need to replace in here?
[70:15] Document ID.
[70:16] I don't think I ever put document ID in the end file.
[70:18] Maybe I missed that step.
[70:19] Yeah.
[70:20] All right.
[70:21] Oh, yeah, there you go.
[70:22] I have a Rishi's error too.
[70:25] Did I get that?
[70:27] Document ID, is that something I already see up here?
[70:33] Here.
[70:34] Okay.
[70:36] This is what happens when you blindly copy paste and don't really think.
[70:40] That's my bad.
[70:42] Because we're rushing you through it, I guess, right?
[70:44] I want to see how far I can get in nine minutes.
[70:46] Do we have to do any closing, by the way?
[70:49] No, we'll just stop when we feel like we're ready to stop.
[70:56] Yeah, you're probably going to make it to the end.
[70:58] After this, you just got to set up a server in your front end,
[71:02] which are both just two big blobs of code.
[71:07] Cool.
[71:10] We're going to check our -- right now, by the way, as a reminder,
[71:12] we're updating the document note property to say "again" instead of just
[71:20] "hello."
[71:23] Okay, so it's done.
[71:25] Let's get it.
[71:29] We're getting the last five documents in our query, right?
[71:32] So "hello" again, it worked.
[71:34] Awesome.
[71:35] There you go.
[71:36] That's pretty cool.
[71:37] Okay, so this is really interesting.
[71:39] It's a database, a decentralized database.
[71:42] Yeah.
[71:43] Exactly, yeah.
[71:45] Yeah, permissionless, open, all those fun --
[71:49] It literally has a database called grovdb.
[71:52] What db?
[71:53] Grovdb.
[71:55] It's specific to Dash, so you wouldn't have heard of it.
[72:00] Grovdb, cool.
[72:01] Is that something --
[72:02] Grov, G-R-O-V-E.
[72:05] Grov.
[72:07] Let me write it and put it on screen for you.
[72:12] Let's go to the website real quick, grovdb.org, I think.
[72:19] I hope I spelled it right.
[72:20] No, I did not.
[72:22] Is it going to correct me if I -- how do I spell it?
[72:27] G-R-O-V-E.
[72:33] V-E, as in very vegetable.
[72:37] Grove.
[72:39] Yeah, there you go.
[72:41] And then add the db.
[72:46] And then add Dash again.
[72:49] There you go.
[72:50] That's the charm.
[72:51] There we go.
[72:53] Is it something independent of Dash that you could use?
[72:56] You can use it independent of Dash, yes.
[72:58] That's pretty cool.
[72:59] It is an independent, standalone database.
[73:02] Yeah, just like how you can use the Redwood router without Redwood, but,
[73:06] like, obviously no one does.
[73:09] Awesome.
[73:10] So the main high-level idea behind grovdb is that it gives you
[73:16] cryptographic proofs of saying this data is provably there on the
[73:22] chain, validated by a quorum of node operators,
[73:27] or it's provably not there, these kind of things.
[73:31] The website talks more about it.
[73:33] But, yeah, that's the whole idea,
[73:36] is that you don't have to trust that the specific node that you're
[73:40] interacting with on the network to do these interactions,
[73:43] you don't have to trust that that specific node is being honest.
[73:47] Because if you have the proof of the data that comes back,
[73:51] then you know that the whole network has said, yes,
[73:54] this data exists on our network.
[73:57] Otherwise, you could have a rogue -- in theory,
[74:00] you could have a rogue node operator that's serving you false data
[74:04] without that.
[74:06] Oh, right, right.
[74:09] These issues don't even come up in the traditional world of web
[74:13] development.
[74:14] These kind of issues don't really even come up as an issue because
[74:18] you're already explicitly trusting a service as a centralized service
[74:23] provider.
[74:24] You can have a rogue employee inside the company.
[74:26] Yeah.
[74:27] Wrong data.
[74:31] Okay.
[74:32] I did something wrong again.
[74:33] Surprise.
[74:35] It says contact ID is not found, which is interesting.
[74:38] Maybe I already deleted it.
[74:47] So we're running get documents.
[74:49] Oh, well, it's deleted.
[74:50] Now we're not getting any documents.
[74:52] So maybe I tried running it twice subconsciously because our note is
[74:56] gone.
[74:58] Yeah, maybe.
[74:59] I wasn't paying too much attention there.
[75:03] But now we've said goodbye, world, then.
[75:06] Yes, we said goodbye, world.
[75:08] There's no more message.
[75:10] Okay.
[75:12] And the server step, what would we set up the server for?
[75:16] So this is going to -- because right now,
[75:18] everything you would do are just one-off scripts that you're running.
[75:21] So we want to be able to have a persistent server with an endpoint that
[75:25] you could then query to, like, get back information.
[75:30] I see.
[75:32] So what this is going to do is this is going to make an endpoint that's
[75:36] going to resolve to the identity information with -- when given the name
[75:42] as the endpoint, essentially, or as the -- so it would be, like,
[75:48] forward slash name, forward slash Clairefro is what it would be.
[75:51] Okay.
[75:53] And is there documentation for, like, this -- it's like a dynamic API
[75:57] kind of --
[76:00] This is just for the sake of the tutorial,
[76:02] just to, like, learn how to do this.
[76:04] This is not really documented in AWorks.
[76:06] This is not even something that's, like, in the dash docs.
[76:08] This is just something I did when I was building this.
[76:11] That's just an Express feature, right?
[76:14] Yes.
[76:16] Oh, well, I'm sorry.
[76:18] I meant -- I know that you're defining the route using Express,
[76:22] but what -- the server that we're actually launching is going to have
[76:26] some schema, right?
[76:29] Or is it just -- like, how would I call this API?
[76:36] It's just -- once you run it, it's just going to be, like,
[76:39] local host forward slash name.
[76:41] No, no, I get it now.
[76:43] We define the routes ourselves, but this is, like, a convention,
[76:46] or we can do whatever we want?
[76:48] No, this is -- no, this is just a way to show if you wanted to start
[76:52] using this library in, like, a full stack way,
[76:57] how would you actually integrate it into a front-end,
[77:00] back-end type situation instead of just literally just running
[77:04] one-off node scripts.
[77:06] So there's no real conventions.
[77:10] Got it.
[77:12] Because we -- this is just a suggestion.
[77:20] Okay.
[77:22] So now we're getting that information.
[77:24] So instead of calling scripts, we're calling our API at name
[77:30] slash Claireframe.
[77:33] And we're returning the platform name.
[77:42] Yeah, so the idea being that you could now create all the endpoints
[77:46] you wanted that would correspond to all the functionality that we've
[77:49] done throughout the course of this tutorial.
[77:52] You know, the ideal world would be someone like me just actually does
[77:55] that, and then, you know, someone would have the whole server.
[77:58] But this is kind of where we got to in the -- when we first did
[78:02] this tutorial.
[78:04] It's an invitation to open source developers to build it.
[78:06] Yeah, exactly, yeah.
[78:08] And I guess the practical use case would be, like,
[78:11] if you made an application that would need to, like,
[78:14] show all of the documents for a given user or something,
[78:19] you could make an endpoint for that.
[78:21] Yeah, exactly.
[78:22] Yeah, you got it.
[78:23] That's cool.
[78:24] Yeah, and you don't need to do a full stack application for this.
[78:28] You saw that the SDK that we were using,
[78:33] you can use that SDK on a server running something like Express,
[78:37] but you could also just use it with a single-page application.
[78:42] Right, which is what this next step was, right?
[78:45] Kind of.
[78:47] What this is doing is this is going to just give you a front-end
[78:49] that's going to call your Express app.
[78:51] Yeah.
[78:52] Yeah.
[78:54] Cool.
[78:55] I guess we're out of time, right?
[78:57] So I'll skip this step.
[79:00] But I assume it makes it just a UI for interacting with --
[79:05] Yeah.
[79:06] Yeah, we can do it there.
[79:08] And then we can either pick it up in another series or another part B
[79:12] of this series and then keep going and maybe even add some flair to it.
[79:18] We can have you also do the Dashmate stuff next time.
[79:21] I'm almost done with my Dashmate tutorial, so it would be good to have QA.
[79:25] What's Dashmate?
[79:27] So it basically just runs -- instead of using Testnet,
[79:31] it runs your own version of it locally with Docker.
[79:34] Okay.
[79:36] Cool.
[79:37] That's unlimited Dash.
[79:39] You can even make your own.
[79:42] That's cool.
[79:43] Awesome.
[79:44] Well, thank you both for walking me through this.
[79:46] This is really fascinating for me because I've been out of the Web 3
[79:52] space so much so that I think I saw Anthony -- you did a video with
[79:57] Rizal and you were joking about Web 5 or something,
[80:02] and I thought it was a real thing.
[80:03] I was like, "That's totally plausible."
[80:05] It is a real thing.
[80:06] It's Web 2 plus Web 3.
[80:09] But I thought it had already, like,
[80:11] gone through two evolutions since the last time I touched it.
[80:13] But that's cool that you're making Bitcoin fork development.
[80:19] Yeah.
[80:21] Yeah, there's a lot more that we could say about it in terms of, like,
[80:25] how it compares to smart contracts and things like that.
[80:28] But maybe we'll go into some of those ideas next time.
[80:32] Yeah, we've kept you pretty long already on this one.
[80:36] But thanks for joining us.
[80:38] I just had one question.
[80:40] Anthony mentioned that you do some streams yourself.
[80:43] What do you do with that?
[80:46] Oh, I just fool around.
[80:48] I like to do little side projects.
[80:50] Right now I'm building Stack Overflow Simulator,
[80:53] which uses AI to simulate Stack Overflow answer threads,
[80:59] as if you were using the old school Stack Overflow.
[81:02] But it's ironic.
[81:03] Yeah.
[81:04] So it's just a fun --
[81:05] And it includes all the snark and the answers, right?
[81:08] Yeah.
[81:09] Like, read the manual.
[81:10] Yeah.
[81:11] But it actually works.
[81:14] It's kind of cool.
[81:15] You get, like, six different answers to your question,
[81:17] and you can use it as a --
[81:19] I'm going to use it as a museum on the internet for people that start
[81:22] learning to develop after AI has already taken over.
[81:26] Yeah.
[81:27] Claire's a lot like me.
[81:28] She was always interested in jumping into all sorts of new tech stuff.
[81:32] You also created your CBT, ChatCBT,
[81:35] which is a bot that uses cognitive behavioral therapy techniques.
[81:41] Yep.
[81:42] Yep.
[81:43] So I'm playing around with AI lately.
[81:46] Cool.
[81:48] That's very interesting.
[81:52] We'll have to have you try out our dashpay.io site at some point as
[81:59] well and see.
[82:01] Yeah.
[82:02] Because that does a little bit of AI.
[82:04] We looked into it this morning, Anthony and I.
[82:07] But, yeah, you've got your Twitter, your X profile here.
[82:12] Yeah, I'm just sharing.
[82:13] If you want to follow Clairefro with an E.
[82:16] Definitely will do.
[82:17] And do you speak Japanese?
[82:19] Yes.
[82:20] I used to be an interpreter, and I lived in Japan.
[82:22] And I keep some of my browser stuff in Japanese so I don't forget it.
[82:26] That's awesome.
[82:27] That's really smart.
[82:28] Wow.
[82:29] Take too much energy to learn it.
[82:30] You don't want to forget it.
[82:33] All right.
[82:34] It says as a parting thing, thanks for your work, folks.
[82:38] I wish I'd learned some of this stuff, but above my pay grade.
[82:42] Maybe, maybe not.
[82:44] We're hoping for this to be accessible to any developers,
[82:47] any traditional Web 2 developers.
[82:49] I can learn it.
[82:51] I'm a music major, so you can do it, too.
[82:54] And I was a liberal arts major.
[82:56] So, it's everyone's invitation.
[82:59] All right.
[83:00] Thanks, Claire.
[83:01] And we'll see everybody next time.
[83:03] I'm not sure when the next stream is, but stay tuned, subscribe,
[83:06] and we'll figure it out.
[83:07] You'll find out.
[83:08] We have a stream tomorrow with Niles.
[83:10] So, catch us then.
[83:12] Sounds good.
[83:13] All right.
[83:14] Bye, everyone.