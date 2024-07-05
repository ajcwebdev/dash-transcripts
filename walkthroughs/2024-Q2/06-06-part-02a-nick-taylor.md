---
showLink: "https://www.youtube.com/watch?v=OlnmIzztYNk"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Platform Walkthroughs Part 2a with Nick Taylor"
publishDate: "2024-06-06"
coverImage: "https://i.ytimg.com/vi/OlnmIzztYNk/sddefault.jpg?v=665dffd5"
---

## Episode Description

Nick Taylor joins the Dash Platform Walkthroughs series but encounters issues connecting to the test network.

## Episode Summary

In this episode, web developer Nick Taylor attempts to follow a tutorial on building with the Dash platform. However, Nick encounters errors when trying to connect to the Dash test network to create an identity. Despite troubleshooting efforts, including using Dash Mate to set up a local environment, the issue persists. Anthony and Rion explain that these sporadic connection problems have occurred before and stem from instability on the test network side rather than the code itself. While unable to complete the tutorial, the episode highlights current challenges and the early stage of the Dash platform as Nick provides valuable feedback as an outside developer.

## Chapters

00:00 - Introduction and Setup

Nick introduces himself as a web developer trying out the Dash platform for the first time. He sets up a new Node.js project and installs the necessary Dash dependencies.

03:02 - Background on Dash

Anthony and Rion provide Nick with an overview of Dash, explaining its origin as a Bitcoin fork, its unique features like master nodes and InstantSend, and how the Dash Platform differs from other blockchains.

19:22 - Running the Tutorial 

Nick begins running through the tutorial steps, starting with generating a mnemonic seed phrase for a new wallet, obtaining test funds from a faucet, and setting environment variables.

37:39 - Encountering Connection Issues

When attempting to create an identity on the Dash test network, Nick runs into a connection error. Anthony and Rion suggest potential troubleshooting steps like updating Node versions, but the issue persists.

52:46 - Attempting a Local Setup

To circumvent the test network problems, Nick tries using Dash Mate to set up a local development environment per the documentation. However, configuration issues arise during this process.

1:13:18 - Purpose of Dash Platform

As the local setup attempt stalls, Anthony and Rion take a moment to explain the overall goals of Dash Platform to Nick - enabling decentralized data storage for applications without the reliance on corporate cloud providers.

1:20:50 - Calling It a Day

With the connection issues unresolved after further attempts, the group decides to end the tutorial there and reconvene once the underlying network stability problems have been investigated and addressed.

[00:00] >> All right. We are live. And so far, my internet hasn't crashed yet. That's good.

[00:07] >> Great. Yeah. Thanks, Anthony. And thanks. Welcome, everybody. And welcome, especially

[00:13] Nick. How's it going, Nick? >> Pretty good. Thanks for having me on, Rion.

[00:19] It's pronounced Rion. It's not Rion. I know that. But it's like Rion, like Orion, I'm

[00:24] guessing. >> Yeah. Yeah. Rion like lion. And if you're

[00:27] in Utah, then you can say like Zion as well. >> Okay. Yeah. That's true. That's true. Yeah.

[00:32] I was in Utah last year. So was Anthony. We're at RemixConf, a framework conference for web

[00:39] development. >> Very nice. You weren't in Utah for the

[00:44] Epic web conference, were you? >> No. Couldn't make that one. But I heard

[00:49] it was a banger. I heard from -- well, I'm sure this year. I've been to a local one.

[00:57] I gave two talks at confu.ca. I was at React Miami in -- when was that? Not late April.

[01:07] Yeah. I think it was late April. And then so far for the rest of the year, I'm going

[01:13] to All Things Open. I'm giving a talk there in October. It's from October 27th to 29th.

[01:20] I do have another conference I'm going to, but I can't mention it yet because it's not

[01:24] public. But yeah, pretty excited. This will be -- this seems to be the year of I'm finally

[01:32] getting to give in-person talks because I've given conference talks before, but they've

[01:37] all been virtual or I've done like panels and stuff. So --

[01:40] >> Yeah, I've done a lot of virtual stuff. >> Yeah. It's just funny because people for

[01:47] some reason just assume I've given a ton of in-person conference talks. Until January

[01:54] or February, I was like, nope, zero. So pretty excited.

[01:58] >> Cool. All right. Well, let's give some listeners a little bit of context of what

[02:03] we're doing here. We are going through -- we're continuing our tutorial series. What do we

[02:09] call it, Anthony? Dash walkthroughs? Dash platform walkthroughs. And we've got Nick

[02:16] here. So you're the second guinea pig here, Nick. And we've got a tutorial that we want

[02:22] to introduce people to Dash platform. But also, I'd like people to have at least a surface

[02:28] level understanding of what Dash itself is as well. And I want to get to know you a little

[02:34] bit, Nick, as well. So Nick, why don't you tell us who you are and how Anthony roped

[02:41] you into this and what you're doing here. >> Yeah, yeah, for sure. So my name is Nick

[02:46] Taylor from Montreal, Quebec, Canada. Been primarily a web dev, but I'll just say software

[02:54] developer engineer professionally since 2002. First two-thirds of my career was more in

[03:02] the .NET ecosystem, and then I was super interested in open source, and I always loved JavaScript.

[03:09] So in 2016, I got in early on TypeScript and React. So basically went on that whole Node.js,

[03:18] JavaScript, TypeScript, open source train, and that's kind of where I've continued on.

[03:24] Little side note, though, .NET did go open source eventually, so kudos to them.

[03:29] >> Real quick, what's funny about this is if you switch .NET for Java, this is the story

[03:35] Monarch told yesterday. You two have very similar backgrounds, that you came up through

[03:39] that world and then hit React and TypeScript, and were like there at the ground floor. And

[03:44] now it's like years and years later, you're like, "Oh, yeah, it's JavaScript. JavaScript

[03:47] brought me here." >> Yeah, it's pretty wild. People are talking

[03:51] about TypeScript now like, "Oh, you should get into it." And it's been around since 2012,

[03:55] like literally 12, almost 13 years now. And yeah, I got started with it in 2015, I think,

[04:01] fall of 2015, and it was way different landscape than no type inference. You had to explicitly

[04:07] type everything. We were using VS Code because I was at a Microsoft shop, and VS Code literally

[04:14] used to just be an editor. There was no extensions, nothing. It was literally like notepad on

[04:19] steroids that only supported TypeScript or JavaScript. It was fun though. And yeah, then

[04:26] basically, yeah, I got interested in open source. And then I've been working professionally

[04:31] in open source, like IE getting paid to work in open source since January 2020. Worked

[04:37] at a company called Dev2, which is a popular programming blogging platform. And then after

[04:44] that Netlify, and now I'm at Open Sauce, working in open source, spreading the love, trying

[04:52] to stay saucy. >> That's great. Yeah, that's a nice pedigree

[04:57] here. Dev2 is, yeah, that's a huge platform. Anthony, can you drop a link to that, by the

[05:05] way, and give us the link to the YouTube, drop it in our Discord so that people can

[05:11] then join us if they want to. And then Nick, let's go ahead and bring up your screen share

[05:20] and show people what we're going to be working on.

[05:23] >> Yeah, I think you got to bring it in for me, Anthony.

[05:26] >> I think I can do that, actually. >> Oh, yeah, okay, cool. I'll zoom in a bit

[05:30] here. For people catching the stream or both of you, just let me know. I'll definitely

[05:35] zoom in my editor too. Yeah, so I guess, do you want to kind of give me the lowdown of

[05:42] what we're going to be doing today, Rion? >> Yeah. Yeah, so I want you to actually tell

[05:47] me, what do you know about cryptocurrency? What's your familiarity, love, hate, whatever

[05:53] you want to say about cryptocurrency background? And then do you know anything about Dash as

[05:59] well? And then if you don't, then I'll give you a little bit of a baseline.

[06:02] >> Cool. Even though I'm not in the crypto space at the moment, it's kind of funny. I

[06:08] have, for context, Quebec, where I live, the province in Canada, they have the cheapest

[06:15] electricity in Canada and we typically sell a lot of electricity to New England. And so

[06:21] basically, a lot of people that, because also marijuana is legalized in Canada now. So basically,

[06:29] a lot of people are growing marijuana in Quebec. And also, there is a lot of crypto mining

[06:36] farms here. And I actually, one of the guys that played rugby with, he runs these farms

[06:42] and stuff. And he ran into this issue at one point where like, I don't know if you've ever

[06:48] been to an actual crypto farm, but basically, you have to set each one up, like say, this

[06:54] is going to mine this particular coin and stuff.

[06:56] And we're talking like he had hundreds and then eventually thousands of machines and

[07:00] he couldn't do this manually. So I basically wrote some software that he's since evolved,

[07:05] but basically, it would provision this configuration for each server, like in his network with

[07:11] like a Raspberry Pi. And it's kind of funny because I literally had a Litecoin server

[07:18] in my garage one winter to build this out. So I didn't have to heat my garage basically.

[07:26] That's awesome. I was just thinking, the marijuana growing and crypto mining, they could probably

[07:32] combine those to be a pretty cool combination with all the heat that the miners throw.

[07:37] Yeah. No, no, for sure. For sure. Yeah. Mine some coins, heat up the marijuana, keep it

[07:43] nice and warm. But I digress. That's just like I thought an interesting story. But in

[07:50] terms of like me actually in the crypto space, I dug into it a little bit. You know, I can't

[07:59] remember the name of the program. It's called Nights and Weekends now, but before it was

[08:03] called something else. And they were doing these like, let's build a dap. And then like

[08:09] two weeks later, it was like, let's build another one. And it was like building off

[08:12] of a different chain and stuff. And I was starting to get a little bit bored with work.

[08:19] And so like, I found these interesting, not necessarily because it was crypto currency

[08:24] related.

[08:25] Yeah. No, it's not that. It's going to come to me. But anyways, like I was a little less

[08:34] interested in like, okay, I'm building it for this particular chain and stuff. For me,

[08:38] it was just interesting to build something. And funnily enough, that work I did for my

[08:45] friend, he actually paid me in Bitcoin, which was kind of cool because I was like, I'm never

[08:49] going to buy cryptocurrency. So he said, can I pay you in Bitcoin?

[08:52] That's Rion's whole thing. Was it Buildspace?

[08:56] Yes. Thank you. Thank you. Buildspace. Yes. Yeah. Yeah. And you know, I joined developer

[09:03] DAO, that Natter DABit started and I'm still in there. But like, to be frank, I haven't

[09:12] been in there really in like the past two years probably. And so that's kind of like,

[09:19] you know, and I have purchased some cryptocurrency, just, you know, curious about these things.

[09:27] And there was some opportunities potentially working in the space, but in the end, I decided

[09:32] to stay in Web2 land. And to be honest, we talked about this a little briefly before

[09:38] the stream, Rion, but there's obviously some bad rap about Web3, like, you know, rug pulls,

[09:46] all the NFT stuff, you know, like bored apes, like there's a lot of stuff. I don't know,

[09:52] the way I would summarize it is, I think decentralized is a great idea. I think right now, to me,

[10:00] at least from what I experienced back then, is it's too slow at the moment and people

[10:04] are creating layers on top of it to make it appear faster. And there's obviously a bad

[10:11] wrap up around a lot of it. And that's kind of how I'd summarize it. I don't know if that's

[10:16] a good enough summary, but...

[10:18] Yep. Yeah, that's good background. I just like to know who I'm talking to and what kind

[10:23] of experience they have. So I guess we'll jump into the tutorial and I will help give

[10:28] context about how Dash compares to some things that you might have been familiar with when

[10:34] you were playing around with some dApps and whatnot. And yeah, we'll just, we'll just

[10:40] jump right in. And Anthony was saying, and I agree, we'll probably kind of let you go

[10:48] through this and we'll just kind of take a step back and to see if you have any questions,

[10:55] you know, "Great, we're here." But yeah, we'll just let you do your work.

[11:00] Okay, cool. Sounds good.

[11:02] Let him cook.

[11:03] Yeah, yeah.

[11:04] Let him cook.

[11:05] I'll go ahead and cook. And like I was mentioning, or Anthony mentioned, I do live stream pretty

[11:10] frequently in my own work. So I'm probably going to go through the tutorial, but I'll

[11:14] probably talk some things through while I'm just going through it. But so I guess I do

[11:21] have one question before I get started. So Dash is a cryptocurrency. So there's a coin

[11:27] behind it. But like, what chain is it on? Or is it based off of another coin? Like,

[11:33] is it based off of like Solana or Bitcoin? Or I don't know, maybe not, probably not Dogecoin,

[11:40] but-

[11:41] It is based on Bitcoin. It's a Bitcoin fork is how it started. But for so long ago, now

[11:45] it's its own thing.

[11:47] Cool. So cryptocurrencies, they're organized in a certain way where you have what are called

[11:53] so-called layer one cryptocurrencies, where that cryptocurrency will have its own blockchain,

[11:59] its own network of nodes running the blockchain, running the software. Bitcoin, for example,

[12:06] is the prime example. And then there's Ethereum. And those are completely separate networks.

[12:11] They don't talk to each other at all. They're not aware of each other. Dash is, then you

[12:17] mentioned Litecoin. That's completely separate. Layer one, L1. Dash is the same, completely

[12:24] separate L1. And then things like Ethereum, they'll have like a token ecosystem where

[12:30] you'll have tons of different tokens that are built on top of Ethereum. So that's what

[12:35] you're thinking of when you have. And Solana, same thing. You'll have different token ecosystems

[12:41] built on top of it. But Dash is its own independent layer one blockchain, its own network, completely

[12:48] independent of these. And it doesn't not currently have any kind of token layers on top of it.

[12:54] But Dash platform is the first kind of pieces to building something like that potentially.

[13:01] But one of the distinguishing features of Dash platform. Oh, I'll give you since you're

[13:06] not too aware of the cryptocurrency structure, I will say this. So Dash has a layer one blockchain

[13:15] that's a proof of work coin. And then it has a separate blockchain that is a proof of stake

[13:25] chain. So the classic example of a proof of stake chain right now, the most popular one

[13:30] would be Ethereum. Although Ethereum started as proof of work, it's now proof of stake,

[13:35] completely proof of stake. So Dash has both has a proof of work chain and a proof of stake

[13:40] chain. And the proof of stake chain is basically operated by a subset of the of the nodes that

[13:48] are operating the proof of work chain. So if you if you picture this network of different

[13:53] nodes operating this blockchain, a subset of that, that are required to show that they

[14:00] all run, they all operate a certain number of they all hold a certain number of Dash.

[14:08] So say 1000 Dash or 4000 Dash. Right now, what we're dealing with is a test network.

[14:16] And so none of this is none of this is live and public on a mainnet. The tokens that we're

[14:24] working with, the coins that we're working with have zero market value. It's all a a

[14:30] subset of basically it's a provisioned network that's operated by Dash core group. And it's

[14:39] just meant to kind of test out the features. So later, these nodes will be the nodes that

[14:46] are running the proof of stake net network and blockchain. They will be what we call

[14:52] collateralized by 4000 Dash. You have to have 4000 Dash to operate one of these nodes and

[14:59] to be authoritative as a network participant. But that's not the case right now. Right now,

[15:06] since we're on a test network, it's just I think maybe I want to say 20 to 100, something

[15:18] like that. Computers that are running this software and they're all operated by one organization.

[15:24] So absolutely not decentralized, but the code works in the same way that the mainnet will

[15:29] work. So that's the context of this.

[15:34] Okay, sounds good. And I'll start the tutorial in a second. One more question I had was,

[15:39] so it's a fork of Bitcoin and that's why the proof of work exists still because that's

[15:44] what most things were. And then like, is that only there for legacy reasons? Because proof

[15:49] of stake is there for security.

[15:53] Yeah, there's different opinions and different, I guess, facts as well about proof of work

[16:01] security versus proof of stake security. And I just wanted to be clear about one thing.

[16:06] When Anthony's saying fork from Bitcoin, what he means is the code base is forked from Bitcoin.

[16:13] That would be opposed to something like a network fork where there is Bitcoin and Bitcoin

[16:18] cash forked from Bitcoin.

[16:20] Yeah, or Ethereum and Ethereum classic.

[16:22] Okay, literal code versus the, okay, yeah, yeah.

[16:25] Yeah, so this is no more than...

[16:28] Started a new one with it.

[16:30] Yeah. So this is no more than like a literal GitHub fork of Bitcoin that started a completely

[16:38] separate network and there was no history that's shared with it.

[16:42] After Bitcoin was created, there was a period where a lot of new products were created.

[16:47] Dash being one of them that kind of started with that code as like the base, but then

[16:52] started to create new coins. And then Ethereum ended up like really blowing up. There's a

[16:56] whole bunch of other ones that came out a couple of years right before that.

[17:00] Yeah. And Dash was one of the first of that generation in 2014 era forks of Bitcoin. It

[17:09] was actually live, I think even before it was live, I think before Ethereum even, and

[17:15] I may be wrong with that, but it was one of the first ones.

[17:18] 2014, they would have been developing it, but like that's when the paper I think came

[17:22] out, but 2015 is when it really launched.

[17:25] Okay.

[17:26] Yeah. And one other thing that I should probably mention that is important distinction between,

[17:33] so it's most similar to Bitcoin or Litecoin, but one thing that's different about those

[17:37] is that in Dash, one of the first things that we developed was this concept of a master

[17:42] node, which is just a node that also shows that you own 1000 Dash, and therefore you

[17:52] are considered, yeah, so you're going to be running different services on top of the blockchain.

[18:04] So one of those services was one of our flagship features, which was called PrivateSend. And

[18:10] then another one was InstantSend. So those two features where instead of a blockchain

[18:17] needing to wait for, let's say 10 minutes to confirm a block of transactions as confirmed,

[18:24] and the merchant can trust that these coins aren't going to be double spent. Bitcoin,

[18:31] you'd need to wait like 10 minutes or so to get that block confirmation. One of the technologies

[18:37] that Dash has separately is that we have this concept of instant finality, where transactions

[18:43] are considered secure after about one to two seconds instead of 10 minutes. And that is

[18:49] because of this concept of master nodes, which is very similar to the concept of proof of

[18:55] stake, where if you can show that you are a participant that has a large stake in the

[19:01] network, meaning that one Dash, then there's certain trust assumptions that come along

[19:06] with that.

[19:07] Okay. Gotcha. All right. Sounds good. Okay. So I'm just going to go ahead and get started

[19:15] here. I already have node 20 on my machine, so I just copy pasted the instructions. So

[19:21] this is going to init a new Node.js project using ESM modules, and it's installing Dash,

[19:30] which I don't know if that's the SDK or what it is, but we'll see once we're done installing

[19:35] here. It should go pretty quick. I have a fast internet connection. Okay. So let's go

[19:40] to... Let me just... Okay. I'm already in there, so let's do this.

[19:45] Now we own your whole machine.

[19:47] Yeah. Yeah. Yeah. Okay. Cool. All right. So there's nothing in here really right now.

[19:53] We just have the package.json and the node module, so I'm just going to keep moving on.

[19:57] Okay. Cool. Okay. I'm just going to run npx git ignore node. This will just put all the

[20:07] default node stuff. So I don't know if you want to update the tutorial.

[20:10] I think, yeah. Can you show me the git ignore with that create real quick?

[20:15] Yeah. It'll... Here. So it puts in like... So like if you pn, pn, pn...

[20:20] Yeah. All this crap which you don't need, but it is simple. Just do it a single step,

[20:26] yeah.

[20:27] Yeah. Yeah. Anyways. Okay. So, okay. Now we got to go and create some scripts here. So

[20:32] let me just close this. I'm just going to make my editor a little bigger and make the

[20:38] side... Okay. That's a little tiny. Oh, you know what? I'll go half, half. Let's do that.

[20:45] I think I went too far. Okay. Hold on a sec here. Okay. Here we go.

[20:51] Yeah. There's copy paste buttons on the top, right? The code blocks.

[20:54] Yeah. Yeah. Okay. Cool. All right. Let's go in the package.json. Let me know if you can

[21:00] see that okay. Scripts. Okay. All right. There. Malformed. Oh, this is not necessary. There.

[21:11] Okay.

[21:12] Got one at the top too.

[21:16] Oh yeah. Okay. Cool. Cool. Let's save that. Okay. So these are just some scripts that

[21:23] we'll need at some point. So creating contracts, registering them, et cetera. Okay. So we need

[21:29] to initialize the dash clients. Let's go back to the terminal. Let's go. Oh yeah. I can

[21:36] just copy it. That's why this will go faster. Copy. All right. So we created API and scripts

[21:46] folders. We've got some client in there and we've got a key for a network for the test

[21:55] net. Sounds like. Okay. Let's keep moving. All right. So let's close this and let's go

[22:01] into API client. And okay. So we're just going to grab here, copy that in. So this looks

[22:10] like, okay, we're saying import. So we're going to, the dash client's going to hit the

[22:14] test network. And then there's some wallet offline mode is true. I'm not sure what the

[22:20] name is. I can't say it. Johnny mnemonic. There we go. Yeah. Okay. Okay. So I'm just

[22:31] going to see what it says here briefly. We haven't created a wallet yet. So the non-monop,

[22:36] Johnny mnemonic. There we go. That's the only way I can say it.

[22:39] There's no. Yeah, yeah, yeah. Yeah, exactly. Exactly. And you're going to say it again

[22:45] and I'm still not going to do it. All right. So we set that to null to indicate we want

[22:50] a new wallet to be generated. Okay, cool. And then we'll get an address that we'll fill

[22:56] in where the null is. Okay. Offline. So we don't want to sync to the chain for some reason

[23:03] yet. Okay, cool. I'm going to make a note of that just verbally that we really should

[23:08] change that. I hate the word mnemonic. It doesn't, it doesn't describe anything useful.

[23:14] That just needs to be a seed phrase. Don't you agree? It just needs to be said.

[23:20] I propose Johnny mnemonic. Yeah. Hey, real quick, Nick, could you refresh the blog? So

[23:30] just push. That should fix one slight thing. So you're good. Keep going.

[23:35] Cool. All right. We're live editing here, folks. Okay, cool. All right. So we've got

[23:41] a script here that we're going to probably put some code in for, for creating a wallet.

[23:48] Let's come back here. Okay. So get wallet account, get our wallet, export to export

[23:56] the seed phrase, and then get unused address to create a new address. Okay. I'm not sure

[24:04] why we need to do that yet, but okay. We'll find out as they go along. Okay. Going to

[24:10] keep moving on here. Okay. So now we need to run the script. All right. So npm run create

[24:19] a wallet. Okay. All right. So here, let me open this up a bit bigger. Okay. So it got

[24:29] me a wallet address and it gave me a seed phrase, which is, I guess that's for my recovery

[24:35] if I lose my wallet. Is that what that is exactly?

[24:39] You want to put this in your .env and are you going to do this throughout as every time

[24:43] it spits out environment variables for you?

[24:45] Yep.

[24:46] So yes, to answer the question that those 12 words are your wallet, essentially. They 12

[24:57] words hold the keys to the kingdom in terms of they, they hold your, they, they derive

[25:03] your private keys. The 12 words are used to drive your private keys, which is what holds

[25:08] your funds.

[25:10] Okay. And I'm not going to worry about it right now because we're just in a test net

[25:14] and this is just, this is not going to be used later. So I'm just saying that because

[25:20] if people ever do a live stream and they're putting their real credentials, do not show

[25:24] them. That's, that's the only reason I'm bringing that up. So I don't, I have done that. Okay.

[25:32] So yeah, so we got our, our environment variables that I pasted into the .env file. Okay. So

[25:39] now we got to, oh yeah, that's right. I remember faucet now. Okay. So yeah, so we need to put

[25:46] in some test funds into our wallet. So I got to search for my wallet. So I got to go to,

[25:53] is the address. Oh yeah. That test net faucet. So go there. I am not a robot. Enter your

[26:03] dash address here.

[26:05] Yeah. Boom, boom, boom, boom, boom. Good to see CAPTCHA is alive and well. Okay. All right.

[26:15] I can toggle this. Okay. Get my address. Okay. Promo code. I do not have one. All right.

[26:27] Okay. Getting coins. I can't tell if it's processing it or not, or if that's just an

[26:34] effect on the button. Oh, I pressed it again. So, okay. Oh yeah. It's processing up top.

[26:43] I can see. Okay.

[26:45] Yeah. This, the dash faucet is a terrible experience. So we'll probably fix this. This

[26:54] is...

[26:55] Okay.

[26:56] Hey, it broke. That means it worked.

[26:57] Okay. Is that what it means? Okay. All right. Cool. Cool. Okay. So, well, you're aware of

[27:03] that, I guess. So, but yeah. So it looks like I have gotten some cash. So I have to go to

[27:11] the Dashblock Explorer now and look up my wallet.

[27:17] So he made a Russian comment and I didn't know what he was saying. So I put it through

[27:21] a translator and what he was saying is I'm going to watch this tomorrow with the translator.

[27:26] We finally live in the future where everyone can speak the same language, guys.

[27:30] I thought for sure he, it was some kind of profanity that he knew he could get away with.

[27:38] That happened to me on a live stream. Somebody wasn't speaking English. I'm like, I was like,

[27:42] I'll go try, I'll go to Google translate live on my stream. And it was like, oh, nope, nope.

[27:49] Not that my streams for kids.

[27:50] I screenshotted his comment, gave it to chat GBT and said, translate this. That's how I

[27:56] did it.

[27:57] So while this is going on, I, so I put my, my wallet address in there and it's loading

[28:04] it.

[28:05] Yeah, I'm seeing that. And I'm.

[28:07] This is not the link you gave me, Rion, because I don't necessarily want to put that link

[28:12] in the blog post. If that's going to be, how often, how is that always going to be the

[28:17] one that we need to use for the rest of the test now, I guess. And can you send me that

[28:21] link again?

[28:22] I can refresh it. I'll send you the link again, Anthony. I think we should have that link

[28:26] in, in the blog post.

[28:29] Okay. I'll open it again. Open link in split view. Let's do that. Okay. So let's paste

[28:39] in my wallet address again. I know test nets are like any dev environment are typically

[28:48] slower.

[28:49] We, we should just skip this part because this is just, we'll assume it's in there.

[28:53] You got the money. You just, let's just assume it's there and keep going and not worry about

[28:56] it for now.

[28:57] Cool. Sounds good. All right. Okay. So I'm going to assume I've, I own tons and tons

[29:05] of cash now. Okay. Let's close all this. Okay. All right. Click on the transaction. Okay.

[29:15] Well, I don't, that's part of just checking if I got the funds, right? Okay.

[29:20] Yeah.

[29:21] We should, we should actually make sure that you did get the funds. I just sent the link

[29:25] to a different Explorer, Anthony. So check that.

[29:30] Is it okay to open that on the stream? Is that okay?

[29:35] Yes. Yes.

[29:37] Okay. Just, just check it. Just making sure.

[29:42] We definitely need to, we shouldn't have to specify the port, so we'll have to.

[29:50] Cool. Okay. So here we go. So there was three transactions. So here we, you can also click

[30:04] on the plus symbol. Okay. So it looks like I got some dash and there's three confirmations

[30:12] and I'm now the proud owner of 3.5 something dash. Okay. So we're good.

[30:18] Okay. I just pushed the change with the link.

[30:21] Cool. All right. I'll keep moving along here. Okay. So now we need to-

[30:26] You could have both, you could keep both links in there if you wanted to, if you wanted to

[30:30] figure out a way to freeze it.

[30:31] Yeah. Because the, I mean, the first time I did this at work, that's why the screenshots

[30:35] are there. So I'm just not sure what happened.

[30:37] Okay. All right. So I need to bring in my, okay. From process.env, and let's replace

[30:49] the null. Always good to use environment variables. Okay, cool. And then I'll add this and I don't

[31:01] need the offline, it looks like. Okay. What's the unsafe options, skip synchronization before

[31:09] a height? Out of curiosity.

[31:12] Yeah. So that is, instead of downloading the whole blockchain and syncing it from the Genesis

[31:18] block, block zero, it just starts syncing from a later height, which is perfectly fine

[31:25] on test net. And I think that there's something in the works to where we might not need that

[31:29] option in the future at any point. So, it's perfectly safe here, but not safe on a main

[31:36] net potentially.

[31:37] Okay. Cool. All right. So we're importing the API client here. I'm creating identity,

[31:47] view on platform block explorer. Okay. That's just console logging. And then something went

[31:52] wrong and then disconnect so we don't have a memory leak, I guess. Okay. And then it

[31:58] calls create identity. Okay. So now we need to run the script that's associated to this.

[32:04] Let's go ahead, copy paste. All right. Okay. So let's double check here. Maybe I didn't

[32:14] do an environment variable properly or something. Let's see.

[32:20] Oh, let's first check to see if we got the right version of the SDK, because we ran into

[32:26] that issue yesterday. And I'm not sure if you've, Anthony.

[32:29] Okay. Let's check. Let's go to dependencies. So it's dash, this version, I can paste it

[32:39] in the chat here.

[32:41] Yeah, I see it here.

[32:44] Okay. Cool.

[32:45] Okay. So let's go back and see what that error was.

[32:50] Yeah. Okay. So range error, the value of offset is out of range. I'm guessing it's reading

[32:58] some kind of array. It looks like it's reading a UN array and it's going out of the bounds

[33:05] for some reason. Should I double check?

[33:12] Let's just try it again. Try to run it again.

[33:15] Okay. So Anthony, I do know, did this, did this version of the SDK work last time in

[33:28] the end, or was it a different version? Because I know that, I know that test net running

[33:34] this.

[33:35] So when we, when we did this, so when we did this on Monday, it worked for me and it didn't

[33:42] work for Monarch. We did it the same day. We were both using the same version of the

[33:46] dependency.

[33:47] Okay. I'll try to one broke one day. Okay.

[33:52] Let's let's try to change it to 12 dev 12, the SDK to dev 12 instead.

[34:01] Okay.

[34:02] Just because I think that's what I think the network is running dev 12, even though there's

[34:07] an updated SDK test net itself isn't running dev 12 yet.

[34:12] But do the SDKs and the test nets versions run in parallel? Are they related to each

[34:17] other at all?

[34:18] I don't know, because this isn't my product. This is probably if I would guess, I would

[34:27] think that it should, it should work with any version of a 1.0, but we're not in semantic

[34:35] versioning at this point yet because we're still in development. So

[34:39] All right, here's what we're going to do. Nicky T, I'm going to send you some keys and

[34:46] you are going to give them a try. Okay.

[34:55] Also this isn't a bad thing. It's a live stream where, you know, we're debugging. It's all

[34:59] good.

[35:00] There we go. Well, it is a bad thing, which I'm looking into right now to see if there's

[35:06] any known issues on test net right now.

[35:09] Okay. So Nick, go off screen discord and grab all the, okay.

[35:17] And I'll put that in my dot ENV I guess. Okay. Yeah. Okay. You want to stop sharing my screen

[35:24] for a sec?

[35:25] Well, just, I mean, if it's whether you care about sharing your, your discord, like we

[35:29] have a shared group message where I sent it just cause it's good. If you copy paste it

[35:33] through the private chat, it does it all in one line. So the keys themselves don't really

[35:37] need to be a private. It's more if you want to keep your discord private, you know what

[35:40] I mean?

[35:41] Oh, okay. Okay. Okay. Okay. If it's, if it doesn't matter that I share them on screen,

[35:45] I'll just put my editor back. Okay. Yeah. Okay, cool. Yeah. No, I nothing to hide in

[35:52] my discord, but yeah, might as well keep it separate. So, okay. I'll just keep that out.

[35:57] Yeah. So these are keys. So now you should have an identity and actually, um, comment

[36:03] out document ID, contract ID, and give yourself a new label with your own name.

[36:13] Okay. Nikki T. Oh, five. All right. My man. Cool. And let's skip create identity and go

[36:26] to retrieve identity and see if he can retrieve the identity with these keys I just gave you.

[36:31] Okay. Should I stay on depth? Well, okay. Yeah. I'll just reinstall. And I would kill

[36:39] your whole package, lock Jason and your node modules folder, fully delete them and then

[36:45] rerun once you're on the new version. Yeah. I trust node modules, but I'll trash it again.

[36:56] Ni is just my alias for NPM install. All right. All right. Um, okay. So like you said, Rion,

[37:06] that's not expected obviously, but yeah, you're looking into it. So, okay. So we're under

[37:11] the assumption that my identity was created fine now, and I don't need to put an identity

[37:17] ID or anything. Cause we've done all that. Right. Yep. Okay. All right. So, uh, create

[37:25] ID. Okay. So retrieve identities, right? Okay. Um, cool. You'll notice that crud theme as

[37:34] we go throughout this tutorial. Yeah. Okay. Let's pop this in. All right. So this is going

[37:47] to, if I just look at this, okay. So it's just getting the identities from my wallet.

[37:54] Okay. All right. Cool. And then we'll run the script. Okay. So all right. Deprecation

[38:13] warnings. That's just no JS, nothing to do with dash. Okay. So it's retrieving things

[38:19] that the flashing cursor there, and I should see a similar out promising sign. This is

[38:27] good. And I should, I should see something like this output, right? Correct. Okay. Actually

[38:35] no, you, you, um, it's still broke. Okay. So let's just see what the error messages.

[38:45] Let me just actually try. This is what we got yesterday. Okay. Okay. So max retries

[38:53] reached 12. Okay. So should I try it again? Sure. Okay. And when it's doing the retries,

[39:07] that's because the network is potentially busy or well, um, we're trying to contact

[39:15] the master node network, the network, the test net network, obviously. And it's obviously

[39:22] trying to do something. Um, many times I'm not really sure what the issue is here. I've

[39:30] I've note, um, and we'll see if anyone gets back with us, but yeah, just general instability

[39:38] issues right now. Okay. We may have to, this is what got us around to the error last time.

[39:45] Right. Anthony, we, we tried credentials, um, and then that worked for us.

[39:53] So yeah, so, okay. So it's just retries still. Um, okay. GRPC transport error. Okay, cool.

[40:08] So at this point, should I retry again? Or what do you suggest?

[40:16] Let's see here. Um, we may have to, I may have to just call it, call it a day on this

[40:22] one. Um, cause I think a lot of stuff, how can we run our own local test? No, that's

[40:30] the only way we're going to get around this.

[40:34] Yeah. And that, that involves like setting up our own, that that's pretty involved. Internal

[40:41] network.

[40:42] Right. You guys just stick it in a docker container, just give you something that can

[40:46] give you a response back.

[40:47] Yeah. So we have like dash mate that, that can help with that. Um, I would be, um, we

[40:58] can try it, but we might end up having

[41:01] Let's do it. Let's see what happens.

[41:05] Okay. Yeah. I don't mind if you, if you want to, uh, yeah, I'll need you to guide me obviously,

[41:09] but uh,

[41:10] Yeah, we can, we can give it a try. Um, I'd be curious to see if you just, uh, Nick, you

[41:18] know, part of this is testing our own documentation as well. So let's say you're a developer,

[41:24] you're interested in dash, um, platform, and you want to just give it a try. Let's see

[41:32] if you can find out how to, how to do that by starting with Google or whatever search

[41:40] engine you use.

[41:41] Dash, uh, crypto.

[41:42] And hopefully you'll eventually get to, you know, the one hint that I'll give you, I guess,

[41:48] is that there is a tool called dash mate that lets you set up local, um, development environment.

[41:55] That's not a test net. It's like literally a local development environment.

[42:00] All right. Let's yeah, that's the thing. That's what is needed. So, okay. So here, boom, boom,

[42:11] boom. Boom. Okay. So, all right. So this is just showing

[42:16] around docker containers. This is what I was saying. Sticking in a docker container. Great.

[42:20] Okay. So detailed, all available features.

[42:25] Can you bump up your zoom a bit more?

[42:27] Yeah. Here we go. Is that okay? Or I can go bigger.

[42:32] One more would be even better. Yep.

[42:35] Yeah. Okay. So I can go to the docs here and so it's on GitHub obviously, because there's

[42:42] links to open issues and stuff. Okay. Let's zoom this in. Okay. Uh, that didn't take me

[42:49] to dash mate documentation. Hold on a sec.

[43:01] Let's look at that diagram real quick. Just, just as a view of something that I already

[43:07] mentioned. Um, yeah. Scroll up if you can, or maybe you can zoom out one. Yeah. Okay.

[43:17] So this is, yeah, this is the overall architecture of, um, looks like this is just a node itself.

[43:26] These are the different components. That's probably a little bit too detailed. That's,

[43:29] that's more deep. I thought the two blockchain, um, image, but okay. So let's keep going and

[43:37] just keep going on your journey to figuring out how to set up a development environment

[43:42] to test this stuff, um, based on our documentation. And one thing while you're doing that is,

[43:48] you know, be one of the, one of the pros and cons of decentralization, you know, pros obviously

[43:55] it's a path to security and whatnot, but one of the cons is that, uh, especially after

[44:01] having done this for 10 years, we do have a bit of fragmented documentation. So I'm

[44:08] not sure what it is on this one, but it might link to the readme. Just go down a little

[44:13] bit. It specifically says the detailed readme. This is what you want.

[44:18] Okay. Uh, here. All right. So this is dash mate open source. Scroll down, click to where

[44:25] it migrates to the correct one you want. Oh, okay. All right. I'd suggest updating the

[44:32] docs, uh, to here. Yep. Okay. So, all right. So this is dash mate. Okay. Let's go see here.

[44:39] Let's get set up, install. All right. Uh, okay. Docker desktop, right? Yeah. I just

[44:48] got to fire it up. Of course you do. You're a real dev. Uh, okay. Got node. That's the

[44:54] right version. All right. So we're going to install dash mate globally. Let that go. And

[45:01] then, uh, okay. Okay. I'll update to get latest patches, but I'm assuming if I'm just installing

[45:11] it now, it should be up to date. Uh, let's see here. Can let that go. Uh, okay. Dash

[45:25] mate set up. Okay. I'll just let this finish installing.

[45:30] So those are the, those are the services that, um, that a, one of these nodes that's operating

[45:35] the dash platform, uh, overall package. It was all those different services, uh, as Docker

[45:44] containers.

[45:45] Okay. Okay. I don't have a config. Okay. So hold on a sec. I've installed it. I don't

[45:52] need to stop it yet because I don't have a config. So I have to, let's see here. Okay.

[46:01] Posts for Linux is, I know I'm not a Linux installation, uh, unless it means like Mac

[46:07] as well, but let me check. Uh, no. Okay. All right. So that's been installed. The update

[46:14] command is quickly. I don't know your node section. Yeah, there it is. Okay. Dash mate

[46:27] config main. Okay. So I'm going to want to configure a test net, I imagine. So dash me

[46:36] a config, uh, or do I want a, we want, we wanted to go with local. Uh, it was test net

[46:51] that was the problem here. Okay. Uh, did I do that right? It's like we were developing

[46:58] it serverless and you always got to pull your AWS Lambda functions, but imagine AWS is just

[47:03] down two thirds of the day. That's what it's like. Okay. Uh, this gave, hold on a sec.

[47:17] I thought this was an error, but this is actually a config it generated. I think some sweet

[47:21] dash stuff right here. Okay. So it generated a local config. It looks like, I don't know.

[47:29] Okay. Let me go back to the races, buddy. All right. And then dash mates start. I'm

[47:37] assuming I have to do dash mates start with passing the configure. Does it just know that

[47:44] it's just, especially fun about this is that Nick is doing this for the first time and

[47:48] me and Rion have never done this. Yeah. Okay. All right. I'm going to see if this works.

[47:54] I'm guessing I'm going to have to pass the config, but maybe, okay. Default config not

[47:59] set. So let's do this. Uh, Oh wait. Uh, you can also use the config option or set the

[48:07] default dash mate config default. So let's do that just so I don't have to keep doing

[48:13] the same thing over with name. Undefined is not present. Okay. What if I do? Nope. Okay.

[48:27] I'm not sure what, let's keep moving. Um, let's do local configure set is, Oh, I meant

[48:36] to do start. Sorry. Also dash mate config set sets the config option. I don't know what

[48:43] that means. Uh, sick. Okay. Maybe that'll do local. Let's see here. Dash mate config

[48:50] set local, uh, set config option. Okay. I'm going to do this. I think that's for like

[49:03] particular values in the config. Maybe. I see. Yeah. All right. I'm just going to keep

[49:08] going on. So let's go back to the start and dash dash config local. Okay. External option

[49:21] is not set in local config. All right. So let's go, uh, config or actually I'm not even

[49:31] really sure where the dash mate config is. Um, cause it's a global, uh, thing. Uh, let's

[49:40] see here. Um, config value. You can modify. You know what? Uh, here we go. Hold on a sec.

[50:04] So I don't want to install that lately here. Let's just go, uh, dash me a tool for dash

[50:23] crypto currency is giving I'll zoom this in. Sorry. Oh, and I lost my prompt dash me dash

[50:39] tool for crypto is giving this error. I think we actually might have wanted to do test net

[50:51] not local. I'm going to try running that in parallel while you're doing. Okay. Look at

[51:00] the dash meter. It depends. It depends if the problem is on our client side or if it's

[51:08] on the network side, the server side, Jane side, but yeah, that's a good test to do.

[51:14] Anthony, if you can, if you can get that up in parallel. Um, what's the reason for requiring

[51:20] an external IP if I'm running this locally? Uh, that's a good question. Is it? So my,

[51:28] my main question, um, for you is, well, the, what we started on was, okay, the premise

[51:39] is you, you're an interested developer. You want to work on dash platform. Um, you want

[51:46] to try that out. I gave you the dash mate. Um, but does the documentation that you landed

[51:53] on give you context about what it's doing for you? Um, and if this is the right path,

[51:59] so I'm just curious, this is more documentation testing than anything. Yeah. Yeah. Okay. Well,

[52:05] I'm going to assume you didn't mention dash before dash crypto install locally. Okay.

[52:18] Okay. So no, that's not what I want. I want to develop environment, uh, dash crypto platform.

[52:34] Probably want to say dash platform. Cause that's, uh, like right together. All right.

[52:43] Dash for Python. Oh, and I'll say, okay. Um, you know, I'll just go to, that's not the

[52:57] same dash. I think I'm going to have to put crypto, uh, plot, Lisa, uh, JavaScript plotting

[53:05] library. Um, okay. We don't want to try that. We should try like the compose command. Docker

[53:14] compose or dash mate compose. So there's a, there's a Docker compose section. Um, here

[53:22] try just running this command that I just put in private chat. Okay. I guess one question

[53:30] I had is I don't even know where the config file is. Cause it's a, I'm assuming it's in

[53:34] my like dev, uh, like what happened there? Let's try that again. Okay. I'll put file

[53:45] dot E and V dot test net. So code dot V dot test net. Let's say dash G dot config dot

[53:55] Tomo. This generated it, but this is in my actual, uh, this is my actual project. Like

[54:04] I imagine that's not where I want this or do I, uh, I guess in terms of your initial

[54:11] question though, Rion, uh, it's, it's not obvious to me right away how to get set up

[54:16] locally. I'm trying to figure out the best way to find it on. I know Anthony's trying

[54:21] to guide me, but, um, cause we don't want to do master nodes that if we want to do local,

[54:28] uh, local or, uh, we'll just get you to the right place. Um, aside from Google, so to

[54:36] go to, go to docs.dash.org and then go from there. I was just curious on, on the, you

[54:44] know, I want to put myself in the position of a developer that doesn't have, you know,

[54:50] that only has the search engine to work with, but yeah. Cool. All right. So let's see here.

[54:57] And then you want to go to the platform docs. Okay. Okay. We won't, we won't do the, well,

[55:06] I can read the intro real quick to see about external IP maybe, but okay. That's not in

[55:12] there. Okay. Okay. Well, uh, I won't read through the intro cause you kind of explained

[55:18] it. Uh, basics of building platform. So just so you know, if you scroll up to the tutorial,

[55:25] uh, if you click in there, that is, that's what we're trying. That's Anthony's document

[55:33] is basically a, a, uh, a better version of this that is kind of expanded and has better

[55:42] output from the, from the code and whatnot so that you can put things in environment

[55:46] variables, but it's based on that. So I'd like to see if, if this does a good enough

[55:52] explanation to give you the content you need to get started. Cool. Yeah. So I'll start

[55:58] fresh here. Make sure you have your, make sure you have your Docker set up and try running

[56:03] NPX dash mate set up test net. See what, yeah, go ahead and do that. NPX dash mate. What

[56:11] did you say? Set up test net. Just set up and then test net. Yep. Okay. Boom. Okay.

[56:24] So I don't want to set up a master note I'm assuming or do I? Um, no. Well, I'm, I'm wondering

[56:35] if this has, it's supposed to set up what you need in order to run the, in order to

[56:44] run the local network. But it looks like what we're doing here, Anthony, is you're, you're

[56:49] asking him to try to set up so that it can connect with test net instead of a local network.

[56:53] Is that where you're, you're going down? As long as we're connected to it in some sense

[56:57] that we could talk to it. So this to me, I think is what we want. So we're trying to

[57:02] connect to test net in general. So we'll see what happens. Yeah. And so you're, you're

[57:07] assuming Anthony, that the error that we got was because our client wasn't set up right,

[57:13] but that the network might be fine. So that's, that's fine. Yeah. So it's just, yeah, it,

[57:21] I think the issue is just, there's some sort of latency problem that triggers something.

[57:30] So it just like, doesn't last long enough and then errors out. It's just some, I'm not

[57:34] really sure, but it happens, it's been happening consistently for many months and it throws

[57:38] different errors every time, but always happens on the same command. And it's not based on

[57:44] the code. The same code has not changed for the three months that we've done this. This

[57:48] code is literally every single line of code is not changed one bit. Yeah. Anthony, are

[57:53] you able to, to get past this step on your side? I'm just curious. I was on Monday. I

[57:59] didn't run, I didn't run a tutorial today. Do you want to try to run one today, right

[58:03] now while, while we're working? All right, let's do it. We'll try and set up one of these

[58:08] nodes and see, see what happens. Okay. Well, I'm a CLI. We're here. Yeah. Well, I'm assuming,

[58:15] well it defaulted to master node. So like, if this was me in the first time using it,

[58:19] I would press enter cause it's a default. So I'm assuming it's the recommended, whether

[58:25] that's the case or not, I don't know, but, is it, is it makes sense to do master node,

[58:31] Rion? Let's see. What, what action did you perform before getting to this menu? I ran

[58:37] just set up test net from dash mate. Okay. I mean, I don't really know, honestly, cause

[58:51] this third master node, just do master. All right. Hashtag yellow. Let's do it. Well,

[58:58] you'll need a thousand dash for that though. And we don't have that in there. Oh, I thought

[59:02] it said it, it populates it with a thousand or is that not the case? Oh, maybe it doesn't.

[59:07] Let's, let's see what happens. It says what? Oh, it just, okay. Full node or a full node,

[59:15] either of the ones that don't have collateral next to them. Okay. All right. Enter. Okay.

[59:22] I don't know what the node key is. That's the unique identifier for it. Do I, I guess

[59:27] it's take default here. Default. Yeah. I think your new will be created for you. Yeah. Okay.

[59:34] External IP address. Okay. Some peer to peer stuff. How do you want to configure SSL? I'm

[59:41] assuming zero SSL is kind of like, it's like what you would call it. Enter zero. I don't

[59:49] have a API key. Okay. I need an API key. Oh, well we don't. Yeah. So what this is doing

[59:59] for you, the Dashmate right now is Dashmate in this context, like the, the, the, the command

[60:07] that you ran is trying to set up a, a node on the network, but that's not what we were

[60:13] trying to accomplish earlier. What we were trying to accomplish earlier is to connect

[60:17] to the network, to do dash platform stuffs, not, not make a node to be part of the network

[60:24] so that we were asking you to do two separate things, Nick. Well, I try to do the whole

[60:29] time to get a node connected to the network. However, it is that that needs to be done

[60:33] because if you're just running locally, but you're still not connected to the network,

[60:36] then the problem is not solved. So, okay. I think, I think Anthony, if you could, if

[60:44] you could run through the tutorial to the step right now, if you get the same error,

[60:51] then I'm going to say, I'm calling the audible and saying, we're done trying today. Do you

[60:56] want to, do you want to share your screen, Anthony? Just while you do it, just give me

[61:00] just one second. I'll, I'll know very quickly whether it's going to work or not. Just let

[61:04] me two minutes and I'm going to just yellow and try and create an identity again.

[61:16] Sure. Yeah. Cause you know, one of the things that it's doing under the hood is it's contacting

[61:21] a random node on the net, on the test net and it's connected to it. And it's then doing

[61:27] commands with that random Evo node is what that's called. And if some of those nodes,

[61:35] like some nodes work and some nodes don't sometimes. Sometimes like, that's why I'm

[61:42] asking Anthony to do it again because the command isn't running right now. We'll know

[61:46] in 10 to 20 seconds. Okay. So yeah, so I got the error again. So, so we retried 12 times.

[61:58] I'm not sure what unimplemented is, but there's a GRPC transport error. I guess questions

[62:09] while Anthony's just doing that, Rion is, so you were saying like some of the nodes

[62:13] might not work. Is there a, I'm wondering just kind of spitballing here. Is there a

[62:19] way to kind of like do kind of like a, kind of like a pre-flight check to say like, is

[62:24] this node available?

[62:26] That's supposed to work with the SDK itself. That's supposed to work. So I'm not, I'm not

[62:33] a developer of this product specifically, especially let alone in practice much at all.

[62:42] So I wouldn't be able to like troubleshoot this specific issue. I just know that it's,

[62:50] it's already supposed to be like the retries is already supposed to handle that kind of

[62:55] an issue where you are connecting to a bad node and it's not responsive or whatever.

[63:00] It's supposed to try it.

[63:01] Okay. All right. I got my faucet funds and it didn't crash this time, which is nice.

[63:08] And we, we may like as a last ditch effort, maybe, maybe we could start from scratch again

[63:18] on your side. And then maybe there may be something in your cache or something that's,

[63:24] that's saying, okay, let's, we're always going to try this, this node now. But if you blew

[63:29] that away and started from scratch, then maybe.

[63:32] Okay. I gotcha. Yeah. I'm just running the node JS debugger to see if, if I, if I hit

[63:39] a break point somewhere.

[63:40] I mean, the error is server side. So yeah, yeah, no. Hey, all right. I was able to create

[63:46] an identity ID. So try just running your reset, your API client file to null for your mnemonic

[63:55] and then run the create wallet command again. And then the problem is you won't be able

[64:01] to get faucet funds. Actually, I should, you should use the, you should use the wallet

[64:07] mnemonic that I just created.

[64:08] Yeah. That's a better idea, Anthony. Let's do that.

[64:12] Yeah. I'm just going to put these in the,

[64:13] We don't want to go through all that faucet stuff again.

[64:17] See if you can create an identity with this, see what happens. So just take the wallet

[64:21] address mnemonic and then keep your network environment variable, but comment out everything

[64:27] else except those three.

[64:29] Yeah. I got all kinds in here now. All right. Let's just move this down here. Okay. All

[64:38] right.

[64:39] Separate lines.

[64:40] Yeah. Yeah. It should be. Oh, that one isn't. Yeah. You're right. Sorry. Yeah. That's good.

[64:45] Steak and pumpkins. That's good.

[64:47] You can create an identity now. I just, I just did. So I can try again, right? The retrieve

[64:54] identity with the identity ID. If you're not able to create your own.

[64:57] Okay.

[64:58] So Anthony, in your logs, does it show what node you connected to? IP address?

[65:05] Go to your client real quick.

[65:08] Yeah. No, it's cause that was just set to offline true before.

[65:12] Okay. Yeah. Sorry. So, oh yeah. You're, you didn't put your environment variable back

[65:19] in for the new mock. Don't set offline true. Get rid of that.

[65:23] Okay. Yeah. Yeah. Gotcha. That's all right. Yeah. That's cool. So it's creating identity.

[65:35] We'd like to see flashing cursors. We like it, but not for too long.

[65:39] Yeah. Yeah. This one, this one takes a solid 10 to 20 seconds. Okay. This is the one where

[65:44] like you really have to stop and think about why you're a developer. And if this is what

[65:50] you want to be doing with your time and then it works, you're like, yes, or breaks again.

[65:55] You're like, God damn it.

[65:57] I'm questioning all my life choices right now. Okay. So same error. So, so it's possible

[66:02] like.

[66:03] Yeah.

[66:04] Well, it's crazy. So the host is 52, 12, 176, 90.

[66:12] Let's check node versions. I'm on node 20.14. What are you on?

[66:18] Node 20.11. I can, I can update NVM. Install LTS.

[66:25] Anthony, what, what do your doc, what do your docs say? The tutorial says the minimum.

[66:30] 20 and up. I don't think this is going to be it, but it's worth a try.

[66:37] Yeah. NVM. Whatever. Okay. Node dash V.

[66:44] It's the same version now. So try it again.

[66:50] Okay. Trash node modules. Okay.

[66:56] Trash, that's a command I haven't seen that.

[67:01] It's less destructive than RM remove. It just basically goes to your recycle bin, at least

[67:08] on a Mac. For node modules, probably not a good idea, but like sometimes when you accidentally

[67:15] delete something, most of my stuff's in get anyways normally. So, but yeah. Okay. So we're

[67:20] on node 20.14, reinstalled the dependencies and let's run NPM run, create identity again.

[67:27] And if this doesn't work, let's take this identity. I just put on the environment variable

[67:32] in the private chat and then we'll try retrieve identity. And if that breaks, then we'll call

[67:36] it. Okay. We can, I'll, I'll pour one out if I need to.

[67:42] Cause that means it's something that has to do with just either our internet connections

[67:47] or cause you're on a Mac, right? I'm on a Mac, but I have gigabit upload, download.

[67:54] I'm on a very fast connection. So I don't think it's low. It's that something is set

[67:59] wrong. I mean, I'm just so curious why that would happen, why it would be broken on yours

[68:05] and not on mine. This is the same thing with Monarch. Cause it was broken on Monarch, but

[68:09] it wasn't broken on mine last time also. We're all running on the same code and on the same

[68:13] versions of the dependencies. So it's completely outside of our control.

[68:17] Yeah. But like there are differences cause it's not, since you're not running in literally

[68:23] the same environment, there's something clearly different.

[68:27] But it's a Mac environment running the same version of node. So it's like, that's about

[68:31] as close as you can get. Oh yeah. No, no, no. I know. But what I mean

[68:35] is it's not, we're not truly literally the same environment. That's what I mean. Like

[68:40] maybe there's something on my machine. I don't know. But regardless, like yeah. So it's given

[68:49] the error. So what, again, what were you suggesting Anthony to try?

[68:52] So go to the private chat, grab the identity ID and put that in your dot EMV and then run

[68:58] the retrieve identities command. Okay. Let me actually also double check that. I can

[69:08] do that command. All right. And then do I have to go into here to put, I know that's

[69:18] already set. Okay. Nevermind. Okay. All right. So now I'm running create. I don't need to

[69:24] create identity. Now I have one. Yeah. I gave you the identity. Yep.

[69:28] So we're just going to retrieve identity now. That's the goal. Okay. All right. As I look

[69:39] at the flashing dash while I question all my life choices. Okay.

[69:44] So give us your take on dash so far, Nick. Yeah, yeah. No. No, I definitely have empathy

[69:52] for what's going on here. I'm working on software. Like it's, it's frustrating when things aren't

[69:57] working obviously, but okay. Okay. So real quick, just so people know or not why I'm

[70:03] going to show my screen real quick with the same environment variables. When I run it

[70:09] is you get back the retrieved identities ID is this guy right here with this balance.

[70:16] Okay. Cool. Cool. Did, did you want to continue through on yours or did you just want to call

[70:22] it out? I'm fine either way. We're, we're done. I think we're going to call it a day

[70:27] today. Okay. And you know, we'll, we'll try to figure out, we'll try to get to the bottom

[70:33] of this non-deterministic error issue because it happened the exact same point we're having

[70:41] with Monarch. That's as deterministic as it gets. Yeah. But I know, I know what you mean

[70:46] though. Yeah. I'm just curious why we can't get a straight answer. Why always breaks on

[70:50] this specific point? Yeah. Like, like, obviously I know this is not how you wanted the tutorial

[70:57] to go, but you know, but I was fully expecting this to happen actually. But, but, but on

[71:05] the plus side, like it's been replicated consistently now. So now there's something you can go back

[71:10] to the devs to see. And you know, I'm not saying it'll be an easy fix. I have no idea,

[71:16] but but if you're up for it, whenever it does get sorted, I'm, I'm happy to come back on

[71:22] and, and jump, jump through the tutorial again. We'll have a Dash Mate instructions and quick

[71:29] start when you're, when you're back. Yeah, I think that'd be great. Yeah, we'll, we'll

[71:35] give this some time and then we'll, we'll have you back. Obviously, you know, we're,

[71:43] we're happy that you help us either way, because it's good feedback, right? So part of the

[71:48] purpose of this, you know, even the live stream part of it is to yeah, just kind of go through

[71:55] what, what other developers go through when they're dealing with the product here. And

[72:00] like it shows, like we are still kind of in development. It's not even an alpha stage

[72:05] yet. So we, we, I expect some of this to happen, but I do want to, I did want to, to reach

[72:11] out to other developers just to just to kind of like, get the process going a little further

[72:18] and introducing it to the world, and not just the Dash bubble. Yeah, for worse. So yeah,

[72:26] well, one thing I'd suggest is like, like, I know you're looking to improve the documentation.

[72:32] I think that would be a great opportunity for people interested in this ecosystem to

[72:38] contribute to the project by helping update the documentation, potentially, just throwing

[72:44] that out there.

[72:45] Yeah, and we've got it all on screen. So we kind of know where the dead links were. And

[72:48] we can, we can look back on that and, and then make some improvements there. So appreciate

[72:53] that. And any other follow up questions that you had, Nick, before you take off today,

[72:57] and we'll, we'll probably chat offline for a little bit afterwards as well for some logistics.

[73:03] But yeah, nothing at the moment, but I am as a Dev, I'm just curious to see this play

[73:10] out. So I want to finish the tutorials. So I'm excited to do it next time.

[73:16] All the interesting stuff happens right after this point, which is why it's where it breaks

[73:21] because once you get your ID, then you can actually create stuff on the chain.

[73:26] Let me actually now that you say that I did want to kind of give the high level purpose

[73:32] of what this is all about, because I didn't really go into that. Yeah, just for your own

[73:37] benefit, Nick, and anybody who might be watching, the whole purpose behind Dash platform is

[73:43] a lot of a lot of blockchains, they're focusing on what are called smart contracts. And that's

[73:49] basically where you have a network of node operators that are running, running their

[73:53] nodes. And each of those nodes is then running this Ethereum virtual machine as part of their

[74:02] node. And what that does is, you know, when somebody makes a request like an RPC command,

[74:11] and calls into one of the functions on this server side, which is the chain side, blockchain,

[74:18] then the nodes and run that execution, and they're doing execution on a blockchain. And

[74:24] one of the differences that we're doing here in Dash is we're just saying, we're going

[74:28] to actually kind of flip the script and say, instead of running execution on the blockchain,

[74:34] we're going to store data on the blockchain. And execution can happen elsewhere. But we're

[74:38] going to optimize to storing cryptographically proven and secure data on the blockchain.

[74:47] And again, this secondary payments chain. So just the way to think about this from the

[74:53] developer standpoint is let's say that you have an application, and you want data storage

[75:01] that anybody else can access and interact with. Yeah, that's what the purpose is here.

[75:08] So it's kind of like a decentralized database that you don't have to sign up to. So you

[75:13] can think of it as a cloud database where instead of, I don't know, you tell me, do

[75:17] you have any cloud databases of choice that you typically reach for when you're making

[75:24] an application?

[75:27] There's some, like Railway has some good offerings. I'm typically doing more front end right now.

[75:37] So single page applications, but also just web development in general. But yeah, typically

[75:47] looking at more serverless databases. But there's a bunch out there. There's Neon database.

[75:56] They're all a lot of Postgres options, I guess, basically.

[76:03] And so this is something like a cloud database, but instead of a corporation running it, it's

[76:09] just a network of operators that are running it. That has its pros and cons. Obviously,

[76:13] we saw the cons today where the network just wasn't responding well. But that's a thing

[76:19] that we need to get ironed out before we go live net, obviously. But in the end, it'll

[76:26] allow application developers to have a database in the cloud, but you don't have to register

[76:32] or anything like that. All you have to do is pay a very minimal amount of dash to do

[76:41] that data storage. And the first step to doing that is creating that identity so that you

[76:47] can then pay with your identity and have that reference to your identity is basically what

[76:57] you would, the analogy would be a username on a corporate, on a corporation.

[77:04] Right now, this is like the login form is broken.

[77:07] Yeah, basically the login form, the cloud. Yeah, yeah, yeah. Cloud storage, cloud is

[77:13] the login is broken right now. But that's the idea is once you get past that, instead

[77:19] of registering with a corporation, you just pay money and then you could store what are

[77:26] document database documents, instead of, yeah, like having your own server.

[77:33] Like a MongoDB, you know, it's a blob. Yeah.

[77:38] Yeah. And if I was understanding correctly before what you're saying, so it's closer

[77:42] to like an Atlas DB. So like a cluster of MongoDB instances that you, you don't have

[77:48] to operate. That's. Yeah. Yeah. And, and you were saying, like, obviously the, the data

[77:54] is stored on the blockchain, obviously, but you were saying it's different in the sense

[77:58] that the smart contracts don't necessarily live on the blockchain and they run on the

[78:04] exterior, but it's, it's just the result of them that just goes to the blockchain platform.

[78:09] Yeah. So, so we don't have smart contracts, at least not in the first, first iteration.

[78:14] So all we have is we have, but it's close enough for what he, what he's asking, he's

[78:19] asked about whether it's on main net or if it's on something else and it's on platform,

[78:23] which is separate from main net. Okay. So yeah. Cause I guess my question is,

[78:28] cause like, okay. Yeah. I guess my question was more like, cause I, I know that blockchains

[78:37] can be slow still. And that's why I was wondering, like, like storing the data is one thing,

[78:43] but if you're doing all the processing to, to crunch that.

[78:46] So the way you get around this, and I know because I work for a company that did this

[78:49] for a year, is that you take the whole history of Dash, stick it in a database. And then

[78:53] when people want to read from it, they are able to do that. So that's one of the ways

[78:58] you can make it super fast. So your reads can be instant. You just cache the whole thing.

[79:03] So the history never changes. That's the point of the blockchain.

[79:06] Yeah. This is my, my old coworkers work on this, a company called Streamfast. It's based

[79:13] out of Montreal, but they're basically indexing blockchains.

[79:16] That's it. Yeah. Quicknode indexed blockchains. That's exactly what it is.

[79:20] So Anthony, I'm glad you brought that up. Cause that's exactly the problem that we're

[79:23] trying to solve here with Dash platform is exactly the problem that you're, you're saying

[79:28] is that you're saying that when you, when you have a blockchain, you basically have

[79:33] a bunch of unindexed data that then requires companies like, like you're saying, like Edge,

[79:40] Egeo or

[79:41] Quicknode, not Egeo.

[79:43] Or Quicknode and in Ethereum land, you have, what's that? What's that? Infura?

[79:51] There's Alchemy and Infura were the two big ones. Quicknode was the better one though.

[79:55] But that's, that's a problem because then you have all of these indexers and the application

[80:00] developers are directly connecting with the index companies instead of the blockchain.

[80:05] And that's actually an issue as well as a performance issue because yes, you get better

[80:10] performance by index, having a corporation index your blockchain, and then you're querying

[80:15] from the corporation. But that's what we're trying to solve is we're trying to say, Hey,

[80:20] we're going to have that query. We're going to have that indexing and querying directly

[80:25] from client to blockchain and cut out the whole RPC index company issue.

[80:33] That means your chain and the developers who connect to it need to have a similar experience

[80:38] to what they would get. And every time I ever connect to a Quicknode API, it's like I sign

[80:42] up, I get a link, I hit it and I go, I'm on the blockchain.

[80:46] Yeah. So we are trying to, we are trying to give that same developer user experience.

[80:51] And it's a spectrum. That's why you want the ability to do that while still having the

[80:56] ability to run your own node. So it was like, just cause you, we off, just cause you can

[81:00] take that route, doesn't mean you have to. So it's like, you can trade off a little bit

[81:03] of decentralization for that. And then as you learn more about the network, you'd eventually

[81:07] like run your own node and do whatever.

[81:09] But I think it's good to have that kind of whole spectrum. It's like you worked at Netlify.

[81:12] It's like, you want to have Netlify before you get to straight AWS, you know?

[81:16] Yeah. Yeah. Yeah. And the other thing too, it's kind of ironic because blockchains are

[81:24] all about decentralization. And then essentially the index is centralizing how you access it.

[81:31] You know what I mean? Like, I know it's meant to speed it up, but like, it feels like it

[81:36] kind of diverges away from decentralization comes a trade off. So you can't, you have

[81:41] to give somewhere, you know?

[81:44] Yeah. Yeah. Yeah. I guess it's not literally all decentralized potentially, but it's more

[81:50] of the, yeah. What you're saying is exactly correct, Nick. We are trying to solve that

[81:58] problem. It is not an easy problem to solve. But in the end, if we can get, if we can get

[82:05] the applications to talk directly with one of these master nodes or Evo nodes, same thing.

[82:14] Then that is, we're trying to get that same speed that you would get with an indexed company.

[82:21] But with the decentralization of directly communicating with the blockchain. So with

[82:26] that, I think we have kept you a little bit, not over time, but at the back end.

[82:32] When do you want to come back? Do you want to do the same time next week?

[82:38] Next week. I'll have to, I'll check with you after. It's probably okay, but I'll have to

[82:43] check.

[82:44] If not, we'll find a date around there that works.

[82:47] Cool.

[82:48] All right. We'll go ahead and we'll end the stream now. We'll take care of some rescheduling

[82:52] logistics afterwards. So stick around with us, Nick, afterwards and to everybody else

[82:57] who's following along. Thanks for joining us and we'll see you next time.