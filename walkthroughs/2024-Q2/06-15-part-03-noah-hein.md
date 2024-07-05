---
showLink: "https://www.youtube.com/watch?v=lGfFgD85U8c"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Platform Walkthroughs Part 3 with Noah Hein"
publishDate: "2024-06-15"
coverImage: "https://i.ytimg.com/vi/lGfFgD85U8c/sddefault.jpg?v=666c6bab"
---

## Episode Description

Noah Hein, an AI engineer, joins Anthony and Rion to test the Dash Platform by creating a decentralized application that stores and retrieves data on the blockchain.

## Episode Summary

In this episode, Noah Hein, an AI engineer with a background in crypto, joins Anthony and Rion to explore the Dash Platform. They walk through a tutorial, creating identities, data contracts, and documents on the Dash blockchain. Noah shares his experience and compares it to other blockchain platforms he has worked with, providing valuable insights and feedback on the process. The trio successfully complete the tutorial, demonstrating the capabilities of the Dash Platform for building decentralized applications.

## Chapters

00:00 - Introduction and Guest Background

Noah Hein introduces himself, shares his background in tech and crypto, and discusses how he met co-host Anthony. Noah has worked in developer relations for companies like Quick Node and Phantom, and currently works as an AI engineer.

02:56 - Overview of Dash Platform and Tutorial Setup

Rion and Anthony provide an overview of the Dash Platform, discussing the proof-of-work and proof-of-stake blockchains within the Dash ecosystem. They set up the tutorial environment and begin the process of creating a decentralized application.

14:27 - Creating a Wallet and Funding the Identity

Noah creates a new wallet using a mnemonic phrase and requests funds from the testnet faucet to fund his identity on the Dash Platform. Anthony and Rion discuss the process and the occasional challenges with testnet faucets.

22:11 - Registering an Identity and Exploring Contracts

Noah registers an identity on the Dash Platform and explores the concept of data contracts, which define the structure of data stored on the decentralized network. They discuss the JSON schema and its role in creating composable units within the application.

41:47 - Creating and Updating Data Contracts

The tutorial progresses to creating and updating data contracts, with Noah adding a note-taking functionality to the application. They examine the process of defining schemas and discuss the potential use cases for such a feature.

58:08 - Submitting, Retrieving, and Deleting Documents

Noah submits a document (a note) to the blockchain, retrieves it, and then deletes it, exploring the lifecycle of data on the Dash Platform. Anthony and Rion discuss the intricacies of the process and the role of the block explorer in tracking these changes.

68:19 - Building a Backend API and Connecting to a Frontend

In the final part of the tutorial, Noah creates a backend API using Express.js to serve the data stored on the blockchain. He then connects this API to a Next.js frontend, completing the decentralized application.

73:40 - Reflection and Comparison to Other Blockchain Platforms

As the tutorial concludes, Noah reflects on his experience with the Dash Platform, comparing it to other blockchain ecosystems like Solana. Anthony and Rion discuss the learning process, the ergonomics of the tutorial, and the potential for building decentralized applications on the Dash Platform.

[00:00] We're live. What is up, Noah?

[00:04] Hey, thank you so much for having me, Anthony. I really

[00:08] appreciate it.

[00:08] Yeah, good to have you know, as well. I don't know you at all.

[00:14] So Anthony is introducing us for the first time. So I would like

[00:19] to get to know you a little bit personally, where how Anthony

[00:23] roped you into this, what your interest or disinterest in

[00:27] crypto is, where you're from, what you do, all that kind of

[00:31] good stuff, just whatever you would like to share about

[00:34] yourself.

[00:35] Yeah, totally. So I'll start. I'm from Texas. I recently

[00:41] moved from Austin. I'm in San Antonio. Currently, I met

[00:46] Anthony, as I was learning to code, Anthony was like very much

[00:50] my first friend ever in tech, as it were, neither of us were

[00:55] employed in tech at the time we were both aspirationally coding.

[01:00] I pivoted from frying chicken. I worked in fast food for about

[01:06] seven years as a manager in the food service industry.

[01:09] Yeah, you were you were fried chicken. I was driving for

[01:11] Uber.

[01:12] Yeah. And so I started teaching myself how to code I got into

[01:17] Twitter and the whole tech Twitter kind of ecosystem. As I

[01:23] was learning to code met, became friends with Anthony. And we

[01:27] both shortly got jobs after become friends with each other.

[01:30] And eventually I hired Anthony to come work at the company that

[01:34] I was working for quick node. Quick node is an RPC provider in

[01:38] the crypto space. So if you are looking to read or write

[01:41] blockchain data, they're kind of the go to solution for things

[01:45] like that. I think AWS for for blockchains for anyone that

[01:49] isn't super familiar with that whole side of node operations.

[01:54] So that's how I got to know Anthony and kind of got my foot

[01:57] in the door into tech and crypto at the same time. And so I

[02:03] worked in developer relations and general content, technical

[02:07] content creation slash engineering for about two and a

[02:10] half years in the crypto space did about a year and a half at

[02:16] both quick node and phantom phantom is the the best crypto

[02:21] wallet in the game as far as I'm concerned. Obviously, I'm a bit

[02:24] biased there. But I think they have a really good product.

[02:27] Are they are they focused on the what what ecosystem are they

[02:34] focused on? Is it cosmos or something else?

[02:36] No, so they're the largest wallet in Solana. And then

[02:40] they're the second largest wallet in Ethereum. And then

[02:44] they just added Bitcoin support recently for all the ordinals

[02:47] DGNs. I think they announced a move. I'm not I'm not 100% sure

[02:53] about that. I think they're targeting move as like the next

[02:56] like move related languages. So what is that like sweet and

[03:00] aptos? Those kind of guys will probably be next on the roadmap.

[03:04] I don't have any insider information there. I don't work

[03:07] at phantom anymore. So that's I think speculation on my end, but

[03:11] they're, they're a multi chain wallet. And that's like their

[03:14] main focus is actually making that an enjoyable experience. So

[03:17] you just kind of have one, one account, and then you can have

[03:22] all of your addresses associated with it. So I've like one phantom

[03:25] account, and it has all of my polygon, Ethereum, Bitcoin, and

[03:29] Solana addresses all stored in that and I can just kind of

[03:32] interrupt, interrupt, interoperate across chains

[03:35] easily. So that's kind of what they did. I did developer

[03:40] relations for them as well kind of leading there. At the time,

[03:45] their EVM go to market. So I had to go in and integrate with all

[03:49] the various kind of like wallet suites like wallet connect and

[03:52] rainbow kit and some wag me all of those kind of ancillary react

[03:59] front end services because nobody wants to code their own

[04:02] wallet UI because the logic there is quite finicky. And

[04:06] there's even some VIPs that are like still being shipped like

[04:10] two years later trying to fix the whole kind of monkey patch

[04:14] situation because everyone just clobbers window dot Ethereum. So

[04:17] you have like 10 different wallets that are all just trying

[04:19] to jump the exact same

[04:20] window has become window dot everything anybody ever wanted?

[04:26] Yeah, yeah. So it's, it's not great. There's there's some

[04:29] technical stuff happening there. That's

[04:31] your own namespace on that, like window dot, you know, cosmos or

[04:36] window dot dash or window dot Solana.

[04:40] Because one, depth developers don't want to deal with that,

[04:46] like, it's already hard enough to integrate however many

[04:48] different wallets that you're going to have. So it's, it's

[04:52] difficult on on the ecosystem as a whole to be able to adopt all

[04:57] of those. So you kind of need some sort of standard. So web

[05:01] three, or, you know, window dot Ethereum is very much the

[05:04] standard currently, but just due to how the architecture exists,

[05:09] currently, it's like every single wallet that the person

[05:12] has installed, tries to go to window dot Ethereum, and just

[05:17] tries to do various things. And so there was also some odd

[05:21] awkwardness in kind of the incentives for some of the

[05:26] wallet models were not always aligned to being as open as

[05:30] possible. And so that led to people trying to impersonate

[05:34] MetaMask. So MetaMask tries to inject that window dot Ethereum

[05:37] dot MetaMask. And there's just like an is MetaMask flag there

[05:42] that's set to true. And so as a new wallet that has no users,

[05:45] you're just like, Hey, I am window dot Ethereum dot is

[05:49] MetaMask true. And hopefully that'll make the other dApps

[05:51] pick it up whenever a user has us installed, without having to

[05:55] go to the dApp and actually integrate with them. So there's

[05:57] like, it's a complicated situation, and it's not great.

[06:02] But that story is getting better. So I did a lot of work

[06:04] over there. And wrapping up to the present, I now work in the

[06:08] AI space as an AI engineer for a company called small AI, we're

[06:12] pre products currently. And so we're just building out that

[06:16] product, we're going to do kind of like AI powered data

[06:19] summarization, you can kind of see, if you go to AI news,

[06:24] that's a button down newsletter, there's a web archive, it's run

[06:27] by SWIX currently, he makes that newsletter entirely using the

[06:32] platform that we're building out currently. But that is

[06:35] essentially a way to stay up. As well. So that whole process

[06:43] just goes through and takes, we do it daily. So it takes all of

[06:48] the information from a particular subset of people. So

[06:52] we have a Twitter list that we've kind of specially curated

[06:56] for this. And so we take a newsletter, or we take a Twitter

[07:00] list, we take some subreddits, and we take some discords, and

[07:03] we just grab all of that information. And then we write a

[07:05] summary for it, and you get emailed that daily. So that you

[07:09] can get, essentially, you don't have to scroll all three

[07:12] separate services, all day, every day, you can just go

[07:16] through and, you know, it's a longer newsletter. So you can

[07:19] definitely kind of pick what you're interested in, or Ctrl F

[07:22] for some of your interests on a given newsletter. But it's just

[07:25] a way to kind of stay up to date and keep your finger on the

[07:28] pulse of a given space, in this case for AI.

[07:30] Very cool. So Swix, you mentioned, Shawn Wang, for

[07:34] anybody who isn't in the Web 2 space. That is one of my goals

[07:40] here is to try to find the Web 2 people who are also Web 3

[07:45] friendly. And it's a, it's a little bit of a challenge. But

[07:48] it sounds like, you know, there are quite a few if you know the

[07:52] right corners to look in and whatnot. You're definitely if

[07:55] anybody hasn't already picked that up, like you are definitely

[07:58] right at that nexus. So thanks for joining us today. And I'm

[08:02] sure that we can probably make some good progress if our

[08:05] network is running well today. So we are running on a testnet

[08:09] right now. And I think without further ado, we will jump right

[08:15] into that because Anthony, correct me if I'm wrong, but I

[08:21] think today we should try to speed through and see how far

[08:25] we can get in like, record time. What do you think?

[08:29] Yeah, yeah, I think we could probably get pretty far. Because

[08:34] there's not going to be as many kind of like, new questions of

[08:38] like, what's a chain and stuff like that.

[08:40] There's anything wrong with that. But yeah, yeah, let's,

[08:45] let's bring up your screen, Noah, and and we'll jump right

[08:48] into the tutorial. And basically, yeah, Anthony, you

[08:52] can you can tell them how to navigate that since you wrote

[08:54] it. And I will field questions when they come and add anything

[09:01] that I really feel like I did. But for the most part, I think

[09:05] we will let you do your thing. And we'll just be a resource for

[09:09] you as you go.

[09:10] Awesome.

[09:12] Alright, so Anthony, am I what am I doing here? Am I just going

[09:17] going through the blog post step by step tutorial mode?

[09:19] Pretty much. Yeah, you can skip all the preamble just go right

[09:24] to creating the project.

[09:26] Cool. Okay. So I was a little bit ambitious here before the

[09:34] stream, I already made this this dash examples here. So I'm just

[09:38] going to copy all of this and see if that that runs through.

[09:41] My favorite thing is installing.

[09:51] Rion, do you which which dash version do we want to do?

[09:55] So yesterday, we did this and we were using dash 15. I'm not

[10:02] seeing which one we're using. We're on 1.0 dot slash.

[10:06] This is good. It's good to the same thing. It's going to

[10:09] install. We'll have to look in the package, Jason, but it'll

[10:11] probably show dev 15. And I think that we should maybe try

[10:18] 12 today and see if see if things run quickly.

[10:21] Dash says four for dev 15.

[10:27] Yeah, let's change that to 12. And then new here node modules

[10:32] and npm install again, because we're there's controversy over

[10:37] what version we should be using and what's going to be the most

[10:40] the most current.

[10:43] Yeah, so the SDK is up to version dev dot 15. But the

[10:48] network is kind of running, tailored to dev dot 12. So far,

[10:53] and in theory, it's supposed to be compatible. But one of the

[10:58] things we ran into yesterday suggested otherwise, at least in

[11:01] terms of speed. So we'll test this test 12. And see if we run

[11:08] into issues and we'll put the 15 if we do.

[11:12] Okay, so we're making some new scripts here. As y'all are

[11:16] talking, I'm just going through I assume that is okay. Give it

[11:18] you said speed run. So I am trying to

[11:21] Yeah, a couple extra these, these curlies. Thank you very

[11:25] much. And we need a comma.

[11:28] There we go. Cool.

[11:32] And so I want to create a scripts directory. Okay, so

[11:38] we're gonna so this this is telling me what and then I'm

[11:43] just running this command. So essentially, I it's one or the

[11:46] other. Is that right? So if I'm just if I just copy this, I just

[11:50] did that. Okay, cool. Great. I have an empty

[11:55] API should have a client j s and an empty scripts folder. Okay,

[12:01] that is wonderful.

[12:04] And so so I don't need to add anything yet to my scripts. I

[12:08] just have an empty an empty thing. Okay.

[12:11] We're gonna import some dash. Great. We haven't created a

[12:19] wallet yet. So yeah, my mnemonic is no, that's, that's great.

[12:24] And we'll just run that. And now my, my scripts has a create

[12:30] wallet j s. And then we will put in here, a new thing. That's

[12:38] great. And now npm run, create wallet. Bad option, ENV file

[12:46] equals dot ENV. That is peculiar.

[12:51] dash V. Oh, use 20.

[12:58] Yeah, and this is this is why I should use Volta not nvm. nvm

[13:02] is the scourge of my life because of stuff like this.

[13:04] Well, if we're talking nvm alternative, there's also webby

[13:10] by AJ O'Neill. So I just have to throw that out there. webby

[13:15] web install.dev.

[13:17] Okay, so did this script right to my dot ENV? Or do I need to

[13:23] copy this?

[13:24] You got it? Yeah. Okay.

[13:27] Cool. And the yeah, the space. Okay, cool. I'm doing the right

[13:39] thing. Have 12 words for your mnemonic. Because 9, 10, 11, 12,

[13:52] 13, 14. Yeah. Yeah, that was 12. All right. Yeah, certainly not

[14:02] 24. That's, that's for sure. Okay, we're actually let me let

[14:07] me actually, I feel like I counted 14. But this is

[14:11] different from what's in your terminal. The terminals is I

[14:15] made so I didn't want to copy this from my terminal. So I ran

[14:19] another one and piped it to my clipboard. And then I copied

[14:22] that. So there's an additional an additional run.

[14:24] Yeah, yeah, I could write the script so that they would write

[14:27] straight to your dot ENV. But um,

[14:29] said, by the way, we just created some magic in your dot

[14:36] ENV file for your your secret phrase. So let me try not to do

[14:39] that. Okay, so now my favorite part, adding funds to a fresh

[14:45] wallet. So I'm going to go to the test net faucet, I am unable

[14:49] to handle this request,

[14:52] delete your HTTP, whatever, whatever, and just search

[14:55] straight from that. This is a

[14:57] this is I kind of wonder if you're joking about the this

[15:01] being your favorite part, but

[15:03] notorious for being terrible, and we are no exception.

[15:08] Okay, so what did you tell me to do, Anthony, I need to say so

[15:11] just like delete, delete the HTTP or HTTPS and just start

[15:15] with the beginning of the domain.

[15:16] unsecured, unsecured.

[15:23] Let's see, I am not a robot. And let's get some quick Do I need

[15:30] Oh, yeah, put your well, okay, this is that that's not entirely

[15:33] clear to me. Okay, everybody. Yeah, that's everybody, too.

[15:37] So let's pull that, put that in there. That is not what I want.

[15:45] Why to dash?

[15:48] There we go. Do I have a promo code? Does this matter? Am I

[15:54] just gonna you can put in master node, and that will give you

[15:57] more coins. One word? Yep.

[16:00] Yes.

[16:01] Master node.

[16:03] Hell, yeah, I love getting more coins. That's my favorite thing.

[16:08] More.

[16:08] Okay, so I see some my bar is loading. I've made a request of

[16:16] some sort.

[16:17] Yeah, this is like the American part where it will probably

[16:21] crash. And then that generally means that you probably have

[16:25] some coins. Verification expired. Okay. That's a new one.

[16:31] Try that again.

[16:32] Anthony, do you have some coins that you can send him?

[16:40] No more dash for me to come back in one hour. Okay, great.

[16:44] Well, you know, that means you might have gotten it.

[16:45] I believe that is what that means. Here, I'm going to pull

[16:52] up this again. So I don't want to share all of that. Let's see.

[16:58] We can open this back up and scroll, scroll, scroll. We did

[17:03] this. We did this. Okay. So we want to go to the dash block

[17:07] Explorer. Okay, I wish we should make these link a new tab. And

[17:16] so I want to put in my address. Yeah. And see what I've got. I

[17:20] have no doubt. I have an unconfirmed. Okay, that's good.

[17:26] That means you're good. Okay, so even though it's, how long

[17:30] should it take to confirm?

[17:31] This, it'll confirm. Basically, it's already confirmed. It

[17:39] generally this, this block Explorer doesn't recognize our

[17:45] instance and feature which it did, but it's probably already

[17:49] confirmed. Okay, cool. It's the difference between transaction

[17:54] confirmation, the way that dash does it, which is an instance

[17:57] and feature, and block confirmation. So if you're

[18:00] familiar with Bitcoin, which you are, you know that the blocks

[18:03] confirm every 10 minutes.

[18:05] That shit sucks. 1010 minutes. That's tough.

[18:08] Blocks confirm every two and a half minutes or so. But the

[18:13] transactions actually confirm instantly. And so they're

[18:16] instantly usable.

[18:18] Okay, cool. So do you want me to walk through the transaction

[18:20] that I got sent? Or am I just scrolling down to more more

[18:23] code?

[18:23] You can keep going to the next script.

[18:25] Keep going. So this is my client j s. And so now I need to make

[18:30] some adjustments. So I am just gonna paste that in. And we'll

[18:38] kill. We'll kill that. That's fine. Great. And we're going to

[18:44] create a file called interesting. What was what was

[18:53] that? Excuse me. Okay, that was weird. Okay, so in create

[18:59] entity j s, we're going to create an identity. That's

[19:03] that's great. We're gonna log out some stuff. My identities ID

[19:08] along with my platform block Explorer. Okay, that's great.

[19:14] Um, and then we're gonna run it. npm run, create identity.

[19:20] This is where we find out whether the network works or not.

[19:24] Do do do do do do do do do do talk a little about what an

[19:30] identity is Ryan while this is running.

[19:32] Are you tracking my identity on the blockchain? I don't

[19:37] appreciate that I'm supposed to be anonymous at all times.

[19:41] Yeah, it's a, it's a permissionless identity. So,

[19:46] yeah, I, I'll use this time, I guess, to, to talk about the

[19:53] difference, the two different blockchains in dash. So we have

[19:56] a proof of work blockchain and a proof of stake blockchain. What

[20:00] we're dealing with with this tutorial is the proof of stake

[20:02] blockchain.

[20:03] Hey, ran awesome.

[20:06] Yeah. So it's a tendermint. It's a it's based loosely on

[20:11] tendermint proof of stake. But we have some pretty heavy

[20:16] modifications to that. And the identity that we just made is is

[20:23] basically the first step to interacting with gap platform,

[20:29] which is the product that we're that we're going to be using.

[20:35] It's probably identity wrong.

[20:36] I identity. Okay, I'm just gonna copy this.

[20:42] Cool.

[20:49] Great. So the whole thing that this right, I've got my identity

[20:56] ID, I need to make another. I'm curious. What? What do you have

[21:03] echo instead of touch? That's like, totally. I don't think

[21:08] touches cross platform.

[21:10] Ah, see things things that you definitely have to think about.

[21:15] Yes, that's a big one.

[21:16] Scroll up a little bit, actually. And let's let's check

[21:19] out that platform Explorer thing that it was talking about. It

[21:23] does.

[21:23] Yeah, my it did generate a thing. However, my current

[21:29] environment is very prone to crashing when I tried to copy

[21:32] directly from the terminal. And that's what I did. I rolled the

[21:34] dice. So I could run the command again, if you want to see it. Is

[21:39] there another way that I could just

[21:40] Okay, you just need to go look at the link that is being

[21:44] console logged out. So go back to your file, like the create

[21:48] identities file. And then copy paste that URL, just pop your

[21:54] the identity ID in there. Gotcha. Select this, and then

[22:04] we're gonna do this. But actually, it's working up here.

[22:14] Okay. So over here, identity slash, well, bam, do I have to

[22:24] fantastic.

[22:26] No data contracts created yet. Let's see. Is this a good

[22:34] URL? It shouldn't be data contract, it should be identity,

[22:38] I think.

[22:43] Yeah, it's just a platform explorer.com slash identity,

[22:46] slash I identity ID, or whatever. Yeah, your identity ID.

[22:51] Yeah, this is this is right. Weird. Not sure why that's not

[22:55] working. I have no transfers or documents.

[22:57] Oh, did we did the script finish Anthony? And no, I did.

[23:02] Yeah, the the thing I assume because it logged out my

[23:06] logout, but sometimes the script, everything that happens

[23:10] afterwards, we do on the block Explorer, that's the last thing

[23:13] that happens.

[23:14] Yeah, no, that was that was the other one. Okay, that was a

[23:18] different script that Nikki T. Or might just have,

[23:25] I will chalk this up to block explorers. Yeah. And so we'd

[23:30] just go to the next thing and assume all of that worked or is

[23:34] that odd?

[23:35] Let's keep going. The retrieve identities one is finicky. So

[23:38] this one may or may not work. So we'll see what happens. Okay.

[23:43] Okay. So we can retrieve identities, confirm that we're

[23:48] good.

[23:48] Excuse Oh, oops.

[23:51] There we go.

[23:57] Fantastic. And so what this is doing is it's grabbing my

[24:06] account, and it's grabbing my ID. And then it is going through

[24:12] all of my IDs, and it's logging out the identities ID and the

[24:18] balance. Okay, great. That seems reasonable.

[24:22] npm run, retrieve identities.

[24:29] npm use 20.

[24:31] Yeah, sorry, it's been a I am thankfully not using node on a

[24:38] regular basis currently. So I have not been dealing with.

[24:41] Yeah, you're in that Python, Python life, right?

[24:44] No, I'm actually in that elixir life, because I could not

[24:48] complain about nodes ecosystem at all if I was living in

[24:51] Python land, because node is way better than Python as far as

[24:54] environments go. It's yeah, I thought is is quite it's, it's

[24:59] bad.

[24:59] What do you what are you doing? What are you writing elixir for?

[25:02] Everything, actually, like I'm elixir front to back currently,

[25:07] and I

[25:08] agree to achieve identities worked,

[25:10] worked fantastic. And I have a balance here, I have one

[25:14] identity, and I have some balance there.

[25:16] So now I'm gonna keep going, I'm gonna top up my identities.

[25:24] That's, that's my favorite thing. So we're gonna make a new

[25:27] script here. And we're gonna copy my top up identities. And

[25:34] here, it seems like the same thing, but I'm gonna call this

[25:39] top up command. I assume this is like a request for more testnet

[25:44] funds. Is that is that what we're doing here?

[25:46] So this is topping up the funds in your identity, and it's going

[25:52] to convert funds from the proof of work chain to the platform

[25:57] chain, essentially.

[25:58] Interesting. Okay, so my wallet lives on the proof of work

[26:04] chain, and my identities live on the platform chain. And so I'm

[26:08] moving one, one to the other. Is that what's happening?

[26:11] Yeah, the wallet, the wallet is associated with the L one

[26:15] blockchain. And then everything actually is derived from those

[26:20] 12 words, both the l one block proof of work blockchain wallet,

[26:25] you know, public private key pairs, and the platform

[26:30] identity. They're both derived from the same thing. But they

[26:33] are interacting with separate chains technically under the

[26:36] hood.

[26:37] Yeah, so the identity lives on the L two, even though it's

[26:40] derived from my from my mnemonic. Yeah. Okay, cool. And

[26:45] so we're gonna run some top up identities. Setting the TLS

[26:55] server name to an IP address is not permitted. This will be

[26:58] ignored in the future version.

[26:59] Great. Yeah, it's said that for as long as I've been doing this.

[27:03] I have no idea what's up with that error.

[27:06] It's like you boot up a new react project. And it's like,

[27:08] can I use light is not going to be, you know, out of date or

[27:13] whatever. I'm just like, Okay, sure. Whatever, dude. Yeah.

[27:16] And this, this running without a specific adapter thing has been

[27:20] here for years also. So I guess we'll, we'll get around to

[27:25] cleaning that up at some point to Yeah, there's, I mean, dash

[27:28] core group. So just while we're waiting here, dash is and was

[27:34] actually the first DAO, believe it or not. It's a very

[27:38] rudimentary DAO. But we we have what's called a superblock. And

[27:44] that pays out to proposal owners that have successful proposals.

[27:49] And dash core group is one of those organizations that gets

[27:54] funding from the dash DAO, and dash incubator as well. But

[27:58] we're, we're separate entities. And we're, we're dealing mostly

[28:01] with products that were built with dash core group and by dash

[28:05] core group. So dash platform has been the big project that

[28:09] they've been working on for several years. And we are

[28:12] helping test it. Interesting. Very cool. So what did we, we

[28:17] have an identity credit balance. Yeah, this is this is great. I

[28:22] want to preserve I don't want to run into the copy issue I did

[28:25] again. Did I get enough funds to run this again and still go

[28:29] through the rest of this tutorial? I assume I'm not like

[28:31] starving for tokens. Okay. Yeah, so we're gonna run that again.

[28:37] So that'll take a minute while that runs since it ran correctly

[28:40] last time, it'll surely run correctly again. So while that

[28:43] runs, I will just go over to our register name. We can just dash

[28:50] examples, we can make a new script. And register name, use

[28:59] 20. And this is the registered name here. That's great. I've

[29:09] skipped this because I don't quite have my thing yet. So

[29:13] before we run the name, I guess I'll stop here.

[29:15] You can just go to your.ev and pick a pick a name.

[29:23] Oh, is that the label is different than what what was the

[29:28] output from top up? Did I need to actually copy that my

[29:31] identity credit balance?

[29:32] No, no, you didn't. You don't know. That's just well, then my

[29:35] bad for you. My bad. Okay, well, Anthony, you wrote it in all

[29:40] caps, which means it has to go in the dot ENV.

[29:43] I guess I didn't need to run that again. Oh, well. So my

[29:47] label, what what am I labeling exactly here?

[29:50] What is your your name? It's like your your like your like

[29:55] your Ethereum name service kind of thing. dash DPS dash platform

[29:59] name service.

[30:00] Want to be in high def dot dash. Let's go. Okay, cool. So I'm

[30:07] going to the register name. I already made this. And so this

[30:13] is what I did. Yeah, yeah. Okay. So I can NPM run register name.

[30:18] And so this is another right action to the blockchain. I'm

[30:28] saying like, hey, here's my label, along with my pub key,

[30:31] please validate my label.

[30:32] Yes. Yep. Cool. I'll skip that. I know, I know stuff about

[30:40] blockchains. I know what's happening here. Okay. And so

[30:46] this document here, what is a document? Is this the output

[30:52] from my label? Is there going to be some here's where it's

[30:56] interesting. This is pretty dash specific. So

[30:58] you want to go for it, Anthony?

[31:01] Explain that a little bit? Or?

[31:04] I mean, yeah. So what's what's happening here is you can kind

[31:08] of think of the dash platform as a way to persist data without

[31:13] needing to write your own smart contracts, because the the read

[31:17] write update functionality is built into the platform. So the

[31:21] document is going to be the data you persist onto the blockchain.

[31:25] So right now you're creating a name so that you can associate

[31:28] yourself with the documents, you're going to create the

[31:30] document. And so just kind of like JSON blobs that are going

[31:33] to be stored on dash platform.

[31:35] So it's very much the terminology is, is using the

[31:41] term document in the sense of document databases, where you

[31:48] have JSON like objects that are stored in, in the database. So

[31:55] there are, there are what we call data contracts. And that's

[32:00] essentially what you can think of as a schema, that certain

[32:05] documents must adhere to that right against that schema. So

[32:10] you could think of a basic schema as like, a blog post, and

[32:16] the blog as a title and a description and text. And that

[32:21] would be your schema. And then documents be all the things that

[32:25] adhere to that schema.

[32:26] Yeah, TBD does something similar to that for the

[32:29] decentralized identifiers, but the dibs, they have a similar

[32:33] thing like that you define some schema from scheme, it's some

[32:37] very old web standard, if it's like schema.org, or whatever has

[32:41] a bunch of records, but it's just like you yank some schema

[32:45] from there. For compatibility.

[32:47] Is it JSON schema?

[32:50] The that doesn't ring a bell, but it's something very similar

[32:56] to that, where it's just like it has a bunch of entities, and you

[32:59] just declare, okay, here's the entity, and it goes to the

[33:01] website and yanks the schema and expects that to be the kind of

[33:05] object that it works with. So it's a very similar idea. I'm

[33:07] sure there's variations in the actual implementation. But it's

[33:10] a, I think that's a good approach to things allows pretty

[33:14] good interoperability, as long as everyone can see, okay, this

[33:18] is what the blog looks like. So I can, you know, kind of have an

[33:21] idea on what what keys I have to the object. Yeah, going to the

[33:26] document that got logged out here. I don't have any data

[33:29] here. This is this is the yeah, I just went and looked up

[33:33] Platform Explorer, and it's only showing stuff up to June 13. So

[33:37] I think something's happening with the Platform Explorer.

[33:41] Okay, let me let me ping Gail and see if there's anything that

[33:46] he knows about. He's the one that wrote that. So let's, let's

[33:51] keep going and see. Technically, we can keep doing stuff without

[33:55] knowing from the Yeah, it seems to all be working. Just we don't

[34:00] see see it on the block Explorer. But so in theory, I

[34:03] should see something kind of, I just wanted to get a bit Can I

[34:08] Can I do this? Yeah, I should be kind of looking at. Come on,

[34:13] come on now. Something like this. That's, that's what I

[34:17] should be looking at where my I would have some unique identity

[34:21] by ID, but my label would be in hind dev that I put in. Is that

[34:27] right? Okay. Yeah. So now I want to make a retrieve name, I

[34:33] created my name, I registered it. And now in retrieve name,

[34:39] thank you a little bit smaller and move back over here. Move

[34:45] back over here. Oh, that is crazy. What is happening? That

[34:53] was wild. I've never seen that before. Um, let's see retrieve

[34:57] name. Cool. So this is grabbing my my label dot dash in hindev

[35:08] dot dash, and then we're grabbing the name from that

[35:11] document. And then we're saying that, hey, we grabbed our name.

[35:16] And here's your name ID. Okay, cool. That seems good. And so we

[35:22] can run that retrieve name. And then we can, I'm going to assume

[35:28] that this doesn't work if the platform Explorer is down, but

[35:32] we will we will click anyways.

[35:35] Error loading. Let's go. Let's go to the platform Explorer and

[35:38] just go to the main homepage and see if anything's showing up

[35:41] there.

[35:42] That's what I was looking at. It only shows up to June 13. So

[35:47] latest block was 296 minutes ago. Okay, I assume that should

[35:53] be two minutes approximately two to three minutes. Let's see.

[35:58] Yeah. Click the API thing. There's a

[36:03] new working in that case. API indexing is disrupted. There you

[36:09] go. That's the issue. Yeah. Okay. All right. Well, that's

[36:12] good to know. But I know, sir, is failing as the blockchain

[36:17] continues to chug along. There you go. There you go. The first

[36:20] time I was having platforms for it's usually it's usually pretty

[36:22] reliable. So

[36:23] Mikhail is on it. He I pinged him about it. He's he's looking

[36:30] into it. But we can see we got some stuff logged out here. So

[36:37] while I can do it on the block Explorer, I have my owner ID. I

[36:40] don't have any schema definitions. That's no, but I've

[36:43] got some document schemas that have domains and pre orders. I

[36:46] have a lot of null objects here. But I do have my normalized

[36:52] label doesn't like my eye. It now has a one that's

[36:56] interesting. Wow.

[36:58] In the other one in the docs about that. It's has some

[37:04] that is some security mechanism, but it's also like, oh, is turn

[37:07] to zeros or something like that. I think it's so people can't,

[37:11] like, give create different links that look like a thing

[37:15] that would actually steal someone's crap, you know?

[37:17] Yeah, I, I think that. Yeah, exactly. There that may or may

[37:22] not be temporary. But there is that measure that they're

[37:27] trying to prevent people from, you know, if I, if I register

[37:31] Ryan, our IO and and somebody else registers are one Oh, and

[37:36] then they could try to be scamming people with

[37:40] homograph attacks.

[37:43] Okay, nice, fancy. So yeah, that's interesting that we ran

[37:49] into that. Cool. All right. So that's, that's, that's why we

[37:52] explore, explore the outputs. So I just retrieved my name. That's

[37:58] the result name object. Cool. That's, that's what I looked

[38:00] like, we're not gonna click on the block explorer. Now we have

[38:02] a data contract. So I'm gonna create my first data contract,

[38:06] which is a blueprint for the structure of data that an

[38:09] application that tends to in store on the decentralized

[38:12] network, it defines the schema of documents within the JSON.

[38:15] Okay, that that seems good. So we'll make a register contract

[38:20] and then register, register contracts, we will create some

[38:27] new stuff. Let's see. So we're grabbing my identity, I'm going

[38:33] to make a contract document. So is this the shape of my JSON

[38:37] schema? Is this like implicit that I'm like this? This is the

[38:40] schema? Is that what's happening? Okay. So I'm creating

[38:45] a note with some properties. And those messages have a type

[38:49] string and a position with them. Okay. register contracts. And so

[38:55] we want to run we want to run this. And then we should get

[39:04] something like this put out. Fantastic. Now here's

[39:08] what I make sure. Yeah, it's not finished yet. Okay, back but

[39:13] you got the string. And it may take a while. So we'll see.

[39:18] Yeah, that was where we're publishing the contract right

[39:22] now in the script. And so that that takes a minute to go up to

[39:25] the network. Yep. Yeah. Okay.

[39:28] So far, the network seems to be running pretty, pretty well. So

[39:31] maybe you're right, maybe dash 12 is the one to use. That's

[39:34] what, um, the Platform Explorer is running. It's running version

[39:37] 12. Yep. Much to its chagrin, it would appear.

[39:41] This is long, to be fair, this is still not a great user

[39:47] experience. So I'll, I'll have to look into this and see if

[39:50] this is known that it's this slow, or if there's some issue.

[39:54] But, I mean, not not terrible. It's done now. So cool.

[39:58] And so we have another thing, where we have my format version,

[40:03] and then here's my document schema that I that I already

[40:06] talked about with my note and my type of my properties. That's

[40:08] that's great. We'd love to see that. That's cool. What is

[40:13] your we need to grab your contract ID and put that in

[40:18] your.emv. Okay, I can I will grab that. What's what is this

[40:24] dollar sign stuff? What is that?

[40:27] That's above my pay grade. I'm not actually sure why they have

[40:31] a key with $1 on it. Because I saw a bunch of them in the one

[40:35] up. It may maybe something so this is adhering to Jason

[40:41] schema, I looked up schema.org. And that's different from what

[40:44] we're using, which is, you know, you said schema.org was the

[40:48] other. Yeah, I'm, I think that's what I'm not 100% sure. But it's

[40:53] something similar, similar to that. So we use we use Jason

[40:57] schema. And I don't know if the dollar thing has special

[41:01] meaning in Jason schema. So I'm looking to

[41:03] Hello, can I there we go. So I want this the contract ID. Okay.

[41:14] And so where do I want to put that? Mr. Anthony, I need to put

[41:21] this in my in my.inv.

[41:23] Yeah, they don't grab the one from the blog.

[41:29] Yeah, I just highlighted contract ID. So I need to go

[41:36] back here and kill that. Cool.

[41:38] So we did that.

[41:44] Jason, Jason schema thing specifically, it's to denote

[41:55] specific keywords that have been used in JSON schema things like

[41:58] schema ref ID.

[42:00] That's what I was thinking.

[42:03] Okay, so we registered the contract. And that gives us a

[42:07] contract ID. Cool. And so now we can retrieve the contract using

[42:14] that ID. Is that what we're doing here? Yep. Okay, so we're

[42:19] going to retrieve the contract to do. So yeah, from the

[42:30] contract ID, and we want a, okay, contract to JSON depth of

[42:35] five. And then we view that on the block explorer. Okay, cool.

[42:40] That seems reasonable. So we can run retrieve contract.

[42:48] Cool. And this is the same the same URL where it's like, Hey,

[42:52] here's the data contract.

[42:53] Let's try it now and see if it works. Oh, you need to do the

[42:57] UPV copy, I guess.

[42:58] Now, my link links work. My terminal is smart enough to see

[43:03] the link. But if it's just the whatever. Yeah, cool. So we can

[43:07] see it. That's really cool. So I have my identifier, which is my

[43:13] contract ID, and my dot ENV. And this, this is me on I'm the

[43:17] owner. We've done some stuff. We've done some creates and some

[43:21] top ups. We did two top ups on accident. Oh, well. Cool. And

[43:26] that's, that's my transaction revision. If like, I make an

[43:30] edit to this, does my revision go up?

[43:33] Yes. I think that's part of the tutorial, right? Anthony?

[43:37] Yeah, the update tutorials get update contracts. The next next

[43:41] thing to add in authors, we retrieve the contract, and now

[43:45] we're going to update it. Fantastic. My update contract.

[43:49] Update contract.

[43:57] And we're gonna update it. So what is what am I doing here? I

[44:03] am setting my document schema to note. And that goes to that.

[44:11] What'd you say you guys use JSON schema. And so in the JSON

[44:16] schema website, there is a note. That's where we're at.

[44:21] That's free text. That's that's your what you're you're

[44:26] defining. Yeah. Oh, that's like my note. Okay. Gotcha.

[44:33] Interesting. Okay. So we update the contract by running, running

[44:39] this script. So in other words, the tutorial is making a notes

[44:43] taking app. Yep. Yeah. And we'll get essentially this same thing.

[44:54] This is just a contract object because we got where I've spit

[44:58] out two or three of these now already, and they just get I

[45:04] should see something similar to this because I had the other

[45:09] one. Is it expected that my schema deaths is still no, even

[45:15] though I have the document schema? What is schema deaths at

[45:20] that point? What is? That's a good question. Let's see.

[45:26] Because, because I feel like that should point to, like some

[45:31] JSON schema, maybe some JSON schema spec on like, hey,

[45:34] here's a note, or a blog or something. So I'm poking, I'm

[45:40] poking holes in your thing. I'm asking, asking all the

[45:42] questions. We don't just run scripts.

[45:44] No, no, no. Yeah, I don't know right off hand. It's not in your

[45:50] tutorial text either, Anthony. So it looks like we're, we're at

[45:53] least on tracking. Yeah, the yeah, I'm not sure about all of

[46:00] the pain in the ash. Looking at docs, all they have schema

[46:05] depths is Sentinel.

[46:07] We can look at let's actually do that because part of the I know

[46:13] that we're steamrolling through here, but let's at least bring

[46:15] up the dash docs go to docs dot dash.org. All right. And there

[46:25] is a reference section. So let's see if we can figure this out

[46:29] through the docs.

[46:30] So I'm in the API reference.

[46:33] And now we'll go to go to platform docs. So that's

[46:37] platform docs. I have the protocol, the reference. Here

[46:40] we go. Yep. We're over here now. So we're making this big. And

[46:45] I'm schema defs. We'll just do schema def. Capital D, F, s

[46:57] schema defs. Okay, so that's just another these are just

[47:01] examples. And I assume from what Anthony said, if I do schema

[47:08] deaths is just going to be no. Yeah. Interesting. Okay, well,

[47:16] so not no, no clear, clear explanation. Let's see, what

[47:22] about the contract, the contract object? A data contract object?

[47:36] And what about schema? deaths schema? Okay, a lot of schema,

[47:42] no schema deaths. And

[47:44] okay, it's saying here. It's used at the convention to

[47:49] organize and reference schema definitions of the JSON schema

[47:54] document, you create a section where reusable schema components

[47:56] are defined, which can then be referenced throughout the

[47:59] schema.

[47:59] That's exactly what I thought it was. Okay, cool.

[48:03] Did you read that from is that chat GPT? Yeah, is this a JSON

[48:10] schema concept then?

[48:11] Yeah, that's basically what I'm saying here. So like, if you

[48:16] wanted to, like I say here, you could create a user object. And

[48:22] then you can reference that within your schema. So it's kind

[48:25] of like creating kind of composable units. And I guess

[48:30] they don't really use that very much in the dash docs. So I

[48:34] guess they're not really pushing you towards that direction.

[48:37] Well, any, any kind of application that would be useful,

[48:44] I would guess would need this. So it's something good to note

[48:47] that we should probably have some documentation about it.

[48:50] Because if you're making Twitter on on chain, where you wanted to

[48:54] let anybody like, like forecaster, whatever, some some

[48:58] protocol, you would want to say, like, hey, this is all of our

[49:01] schema definitions that we expect you to adhere to, to be

[49:06] inspect to the protocol. And having that explicit is is a

[49:09] nice thing to have, and allows everyone to reference the same

[49:13] thing. So that's cool. That's what I thought it was. I just

[49:16] thought it was interesting, because we, we clearly have a

[49:19] schema here in my note. So I should create a note schema

[49:23] definition, and then just use that everywhere. Cool. Okay, so

[49:30] my rabbit hole has has been officially, we've we've answered

[49:35] that one. I just updated my contract. And so now, I want to

[49:41] add a application here to my client. Okay. client.js. So I

[49:52] have my unsafe options, my wallet. So I'm just gonna yoink

[49:57] the apps here. I'm grabbing my contract ID. So I need to also

[50:03] add my contract ID. Cool. Skip synchronization before height.

[50:13] Interesting. Okay. So this is like just making sure like I

[50:17] don't grab everything from the history of the chain. Is that

[50:20] yeah. Yep. Great. So we are submitting a note document. And

[50:30] so a note is has been defined by us. Okay, great. So no document.

[50:38] And so let's read through this. We have we're grabbing our

[50:45] identity. Again, we're creating a new document. And we're

[50:49] calling it a tutorial contract dot note. What? What is this?

[50:53] Is this a label? The label of our contract? What? What is

[50:58] this?

[50:59] So it's not the label of a contract. It's the label of a

[51:04] document.

[51:05] label of a document? What? Sorry, I thought a document was a form

[51:10] of contract. Is that not? Is it just its own thing? It's

[51:13] entirely separate. They're they're both primitives

[51:15] contracts and documents.

[51:18] Yes, they're both primitives. The contract is like the schema

[51:21] and the document is an object that adheres to the schema.

[51:25] Ah, okay. All right. So we give it what did you call that again?

[51:32] This is a document label for like a it's the name the name of

[51:36] a document.

[51:37] I'm actually not sure what the arguments technically are. But

[51:44] Anthony, do you? Let's see.

[51:47] Yeah, so what this is, so if you scroll back up to your client,

[51:50] the the reason why you had to put your contract ID and your

[51:54] client was because this allows you to basically define specific

[52:00] methods that then you can pass in as you're submitting the

[52:03] documents. So there's a there's a there's information about this

[52:10] in the I think I said something about this in the tutorial. But

[52:15] there's also a doc.

[52:16] Sorry, I've completely omitted all of the actual explanation

[52:19] that you do in your tutorial. I'm so shut up. Just copy paste

[52:22] code. Yeah, so

[52:23] yeah, so just if you scroll to where it's right above the part

[52:26] where you put the client in it explains this part. So just

[52:29] scroll up a little bit more. Yeah, right there.

[52:30] Add apps object to the client options and pass the contract ID

[52:35] to enable contract name dot contract document syntax while

[52:38] accessing contract documents. Okay, so this is the tutorial

[52:42] contract. And then we have the note that we will that we had

[52:46] established earlier. That's that's what we've been calling

[52:48] it. Okay, that's cool. I want to dig deeper than that. I don't

[52:54] 100 I think I think I get that there's a message but on this we

[53:01] had a message Do we not add a position? Do we do that later?

[53:06] Because there was definitely a position key on the messages.

[53:08] So I guess that was it can just be no.

[53:13] I think it will know that because you define the position

[53:17] is going to make that the first position or that's your position

[53:21] interesting.

[53:21] It should be zero. I believe if we if we do need to write it

[53:25] should be zero.

[53:26] It was zero. Yeah.

[53:28] Submit note document. Oh, I already already wrote that. Okay,

[53:33] and then we create and then we have like the this is the

[53:36] protocol essentially if we wanted to replace or delete

[53:39] things. Okay, cool.

[53:42] We have the submit note documents. And we're going to

[53:46] have an output of my document ID, and then a bunch of other

[53:50] stuff. Okay. Yeah, with some ID to your dot EMV.

[53:55] This is we're actually writing to the chain. This is our our

[54:03] hello world right here. Yeah. Yeah, I'm sending a message to

[54:08] my so I created my my contract and then I created my documents

[54:15] and now I am updating one of my documents with my note. Yes,

[54:22] schema stuff. Okay. Cool. Yeah, my document schemas are of type

[54:29] note. That makes sense. Man, that's a whole lot of Nolan

[54:34] false. Just every everything is non existent except for mutable

[54:38] contract, we can do that and can be deleted contract. Okay.

[54:42] Interesting. And it's of type note. That's cool. I like that.

[54:47] So we're writing to the chain and then we want to be able to

[54:50] get my document. Whenever I write to this, I have my is this

[54:57] the same document ID that I got earlier, this should still be

[55:00] the same document, right? Like it should log out, whatever. I'll

[55:05] probably answer this question myself.

[55:07] Did it? Did it finish that script?

[55:09] Or no, yeah, we just got it. So there's my, my ID, my owner's

[55:13] ID.

[55:14] Hello, web dev is the message.

[55:20] Oh, yeah, I should have changed that to you should you should

[55:23] make this dynamic to be my label.

[55:27] That'll be good. Yeah.

[55:29] At Friday, June 13. June 14. Sorry. Whatever GMT. Okay,

[55:38] great.

[55:38] I am going to do that again. We're gonna pb copy. So while

[55:44] that runs again, so that's that's cool. I like this.

[55:47] That's, that's great. It has

[55:48] what did the Explorer choke on there?

[55:51] This was, I'm sure it's probably running now. Yeah, this was just

[55:55] from before I hadn't updated it.

[55:57] Yeah, so I have my label and my records. That's all cool to to

[56:05] you know, yeah, my owner ID is right here. That's cool. My

[56:08] document. Okay, so I'll close these two.

[56:10] And when that's done running again, I will go ahead. So

[56:16] as that runs, I'll create a new script. And we will call this

[56:23] the

[56:25] get

[56:26] documents.

[56:29] And then we will copy this in here.

[56:35] And then we'll go to my dot ENV. And what did what did we call

[56:42] it? My document? Do I do I need this? Does this need to go in my

[56:47] dot ENV? I think so. I don't I don't think you don't say that I

[56:51] do. You just say that

[56:54] we document it. Because that's just a reference to the specific

[57:00] instance of you're getting you're going to use it in the

[57:02] update. No, no document.

[57:04] Yes. So in here, but where do you? You don't get

[57:12] the next one, the next script, you're going to need it.

[57:16] Okay. Is this Oh, this is get documents. Okay. I'm gonna go a

[57:22] little bit ahead. Yeah. So in the tutorial,

[57:25] we have to know which document.

[57:27] Yeah, just noting, you do not tell me that I need to do this

[57:32] in here as far as I can tell. I think it was a you like it's

[57:36] from here. Yeah, like it's like we said before, it's in all

[57:40] caps, it needs to go in there. But that was not true for for

[57:43] all of them.

[57:44] Well, I'm

[57:49] yeah, I didn't. No, but there's one part where the one you

[57:53] thought you had to copy it had something at all cast, but it

[57:56] wasn't like equal to a thing. So but yeah. Oh, okay. There's a

[58:01] point in the thing where I say, copy this and place them in your

[58:04] dot EMB. We'll do the same throughout the rest of this

[58:07] tutorial. But I'll make sure to specify each time like and make

[58:10] sure to take this specific environment variable.

[58:17] Okay, and I did some something I blew away my clipboard,

[58:20] unfortunately, so I'm running running that one more time.

[58:23] Apologies here. We're, we're chugging through this is good.

[58:27] This is a beefy tutorial. We're doing a lot here. Yeah, totally.

[58:30] This is I think the furthest we've got so far, right? Oh,

[58:34] yeah. Yeah, good. And then half the episodes.

[58:38] Okay, so I need to go back here. And we're gonna do this. We're

[58:46] gonna kill whoa, there's a lot there that I don't want. Wow,

[58:52] that was interesting. Transaction sync work. Did I?

[58:56] This is probably an is this an error block height block height

[58:59] changed handler is already set. Interesting. Okay, whatever. I

[59:05] have my document ID. That's all I care about. Forget all that.

[59:07] That didn't exist. All this in my dot EMB get out of here. Okay,

[59:13] cool. We have my document ID. And I'm still a bit ahead of

[59:18] myself because I need to do my get documents call. Okay, so I

[59:22] need to save this. I mean, to npm run get documents. And I

[59:30] didn't need the ID for that. I could have done that earlier.

[59:32] But cool. I since I ran it three times, we've got three of them.

[59:35] And we're about two minutes apart on each of them. I

[59:40] interesting. Is that from whenever I ran it or from

[59:43] whenever it gets confirmed on chain the time? I assume it's

[59:48] from when I ran it. Yeah. And then that just Yeah, that's

[59:51] definitely what you want. Yeah. Yeah. Okay, so we've got all of

[59:55] our documents. And now I want to get a single document. So we'll

[60:03] create a new script where I update note, document, update

[60:09] notes, documents. And we'll grab my tutorial contract note where

[60:15] my ID is my document ID. That's great. What What is this an

[60:20] array of? Why this is not just a single document.

[60:25] I mean, you could create multiple documents, I guess.

[60:28] But right now there's only one.

[60:31] There's a document, but you can create multiple documents, I

[60:35] think, like,

[60:36] but this is getting Oh, documents. Yeah, yeah. If I had

[60:41] just multiple, multiple things. Okay. All right. All right. That

[60:47] that makes sense. Cool. And then we're setting a message. This is

[60:55] gonna he's off script. I'm not plastering your name all over

[61:13] the dashing. Anthony, absolutely not. I will I will make I will

[61:17] make my mark here on the dash on the dash network. Let's update

[61:22] no document. That should do it.

[61:27] We'll get the document updated. And we'll have our message with

[61:42] the current time because we're calling new new date to UTC

[61:46] string again.

[61:48] So I'm kind of surprised that the created ads and the updated

[61:51] ads or no, honestly, I'll have to look into that because that's

[61:55] supposed to be a system, you know, system variable that that

[61:59] populates.

[62:00] Yeah.

[62:05] Is it not in the we had. So that finished running. I thought it

[62:14] had to do with. Well, have I already gone through that much?

[62:19] All right, I'm not gonna go through it. There was like some

[62:21] I had all of the arrays of like the created that the deleted and

[62:24] the updated and I think one of the notes earlier. Okay, so we

[62:29] updated the note document.

[62:30] I see that I see everything right here that created that and

[62:34] update that fields will only be present documents that add them

[62:36] to a list of required properties. So I need to update

[62:39] my con my contract to actually include that.

[62:42] Yeah, because those are just empty arrays in the tutorial,

[62:45] right? So you'd need to put the document in there. So they

[62:47] populate? Is that right? Something like that. But cool.

[62:51] We said hello from in hind of again. Great. We love to see it.

[62:55] I have successfully updated it. And now we're gonna delete it.

[62:59] Oh, no, dude. I just I just put my name on there. Okay,

[63:04] create it if you really want to.

[63:06] Okay, so we created it, we updated it, and now we're gonna

[63:11] delete it. So we can delete that document where my ID is the

[63:18] document ID. And then we will delete it. Does deleting it also

[63:25] take resources? Like do I need tokens to delete something on

[63:31] the network?

[63:31] I don't think so. In fact, I I'm pretty sure that you actually

[63:38] get money back back. Yeah, that's that's how it works on.

[63:41] So that's why I ask is like on Solana, if you like delete state

[63:44] from the chain, it's like, Oh, here you go have some dust back

[63:48] essentially.

[63:49] I think that's how we've we've done it to you.

[63:51] That's always a feel good one. There's nothing bad if let's

[63:59] let's see, like on on the platform Explorer website. There

[64:05] should be a history of an identity balance and see if it's

[64:10] going up and down.

[64:11] So in my dot EMV, what would I look up for that? Would I be my

[64:19] identity or my wallet address?

[64:21] identity, I believe.

[64:22] Okay, so here I did just delete it. So what was the identity?

[64:33] identity slash this?

[64:35] If you just pop it in the search bar, does that work?

[64:46] Oh, that's it would be probably smarter. Yeah.

[64:49] Yeah. And if you just go to the forward slash identity, you'll

[64:52] it'll be the first one you're right on top. It's the only one

[64:54] that's been created today.

[64:56] Oh, interesting. Or is it identity?

[65:00] Identity, just identity.

[65:02] My misspelling it, try using the hamburger menu.

[65:09] Identities. Fantastic. Oh, yeah, the only one created today.

[65:17] Look at me. Fantastic.

[65:18] Let's see transaction transfers, transfers. There you go.

[65:27] Absolutely. Okay. So those were from none of these were just

[65:33] not this was whenever I just created your funding. Yeah.

[65:36] Yeah. Okay. So I didn't get anything back for deleting it,

[65:39] it would it would appear.

[65:41] Did we do that? Does the delete show up yet on?

[65:45] I suppose that would be a good. Let's see. So we did delete it.

[65:52] Yeah, we have revisions of two. Although this kind of just

[66:00] returns the contract. Okay, it says it says document deleted.

[66:04] That's just Anthony that said that. Yeah, yeah. Yeah. Yeah.

[66:08] And the console log. So it's not necessarily apparent. So maybe

[66:12] in another two minute, whoa, identity creates.

[66:15] Yeah. So there's one issue here, which is that it's starts at the

[66:19] earliest one, and then it caps out after 10. So you're not

[66:22] going to be able to see it.

[66:23] Oh, it caps out after 10. Yeah.

[66:26] Transactions. Interesting. I'd also probably want that to be

[66:33] descending. Instead of us ending the most recent stuff first. Oh,

[66:40] well. Maybe maybe under transfer. Now, I will assume that doesn't

[66:46] work that way for now.

[66:47] Okay, that's the end. And documents, tabs.

[66:51] Documents. Let's see at 114. We did this. This document here is

[67:00] no because we killed it. I imagine that that would make

[67:04] sense to me. Whereas this one should still be alive. Yeah,

[67:07] cool.

[67:11] Contracts, I have the one I have three documents. So the

[67:18] document ID persists, it just kills out the data within it.

[67:22] Okay, yes, that that tracks to me. And yeah, revision count of

[67:29] two because we created it.

[67:30] And we believe that that's probably happening at the block

[67:35] Explorer level, though, I would be surprised if a history of the

[67:40] documents exists on the chain itself. But

[67:44] oh, you think like it completely obliterates it? And like, I

[67:51] wouldn't be able to query for it. And the block Explorer just

[67:53] has the historical data and is holding on to it.

[67:56] That's my guess. But I have to look into that. Okay. Okay,

[68:04] moving on. Let's keep going. We're close to the end. We got

[68:07] 10 minutes left.

[68:08] Okay, so I can run this command.

[68:15] Got through all the scripts. scenario, yeah, create a

[68:19] backend.

[68:19] So my API in my was just my server. We're gonna toss all of

[68:29] that in there. And we're gonna npm run Express running on local

[68:37] host 3001. What is mine is my name, the label.

[68:44] That's an I and hi, Deb. Yeah, exactly.

[68:46] And that's my Okay.

[68:48] Yeah.

[68:49] Like this big. So here, I want to say behind us.

[69:01] Oh,

[69:02] tweet. Cool. Fantastic.

[69:13] Yeah. So now basically, you have an Express server that will

[69:17] serve you this data, this data. Very cool. Let's see here. And

[69:25] let's see. God help me. Let's see, do is this in a new folder?

[69:32] Should this still be in dash examples still in dash examples?

[69:36] Yeah, and then keep your server running? Yeah. Okay.

[69:39] Yes. Yes. Yes. Yes. Do I want an SRC directory? Yes, I do. Yes,

[69:53] yeah. Yep. Let's see. Would you like to customize the default

[69:57] alias? No, no, yes. Yes. No, I don't think that it matters

[70:02] either way. But no should be fine.

[70:04] Okay. Now, in my next step, I want to go to my page. js. Oh,

[70:17] but I have all my node modules. And let's see. Next SRC app. Oh,

[70:24] yeah, it's not even. So what do I want? I want my page dot TSX

[70:29] because it's not JS. Pretty sure this would be JSX anyways, even

[70:34] if I said no. I think this is because this is this is JSX.

[70:44] Although my home looks quite a bit different than yours.

[70:48] Yeah, no, it actually is.js. If you select not to use type

[70:54] script. Interesting. That's just how the create next app does it,

[70:57] you know.

[70:58] npm run dev. Okay. And so identity, where am I getting

[71:07] identity from?

[71:08] So yeah, so that's just to make sure that your next app is

[71:11] running. And then after that, actually the logic to catch it.

[71:14] Completed. Hey, there we go. Page dot TSX. Okay. Oh, this is

[71:26] like the Okay. So I'm gonna kill a bunch of bunch of this. Just

[71:36] say hello. Okay, cool. That's much less confusing.

[71:43] Yeah, I get that one and just grab the next one.

[71:47] So I went to my not using client currently, I'm not using client

[71:53] currently. Okay, so we're just gonna

[71:54] Yeah, just grab the whole thing.

[71:56] See, make sure I didn't get any errors here. Okay, fantastic. My

[72:05] identity is null. Hmm.

[72:06] Well, that's because I hard coded in my my name in there. So

[72:13] you want to change where it says localhost 3001 in your code or

[72:17] slash name. Yeah, I need to fix that.

[72:20] Oh,

[72:23] just to end on dev.

[72:34] Haha. Yeah, my next JS app. I'm using some clients. I'm rendering

[72:41] some data at a fetch button. Okay. Sure. Why not?

[72:48] You use? Okay.

[72:55] Oh, that's not what I want to do. I was away the whole thing

[73:01] and copy pasted in. Yeah.

[73:03] Well, Anthony, was there was there a reason that you chose to

[73:09] go with having a server? Instead of just a client side

[73:14] single page application?

[73:16] Because then you'd be exposing your wallet.

[73:21] Yeah. Yeah, that is a very good reason. If I have

[73:30] this the single page application can use, you know, it, it can

[73:36] prompt the user for things like that. Yeah, you can set it like

[73:39] local storage. Yeah.

[73:41] Or have a

[73:45] there. Yeah, let's do that. Okay, we did it. We got to the

[73:49] end. Everything worked. Oh, yeah, we got five minutes to

[73:52] spare. Noah, you're nice.

[73:56] You receive an A, Noah, because we'll only let's go. Let's go

[74:02] dude. So I'm gonna quit. Gotta do that. There we go. I did it.

[74:08] We got we got through it all. You love to see it. I was epic,

[74:11] dude.

[74:12] Yeah, so that's, that's dash platform. In a nutshell, it

[74:20] allows you to store data on the dash platform blockchain proof

[74:24] of stake blockchain. And it uses credits, which is just a

[74:29] different denomination of dash. So yeah, that's, uh, how does

[74:36] that compare with things that you've seen in this Lana

[74:39] ecosystem? Noah?

[74:40] I'm good, I would say.

[74:43] Without knowing more about like how to get dash and the

[74:51] monetary value, like how much money I would have spent for

[74:55] that to be on chain. And to do all of that. It's hard to do a

[74:59] straight compare contrast. But overall, that was a pleasant

[75:03] experience, like, definitely meets the bar to me for four

[75:09] things. As far as like, I don't want to do so many hoops.

[75:13] That's about the I say so many hoops, that's a lot of hoops to

[75:16] jump through. But that's just like where the space is that

[75:18] currently, I cannot hold that against dash. So

[75:22] just for learning, you know, we could have went straight to the

[75:27] app, for example, and just popped it in. But, uh,

[75:31] yeah, that could have been a web app where it said here, create

[75:33] contract, create identity, create stuff, update it, delete

[75:37] it. And I could have been like, cool, I clicked some buttons, I

[75:39] ran the web app, and I'm done. But I feel like I have a good

[75:42] holistic view of it. And going through each example, like I was

[75:47] able to ask questions of y'all and be like, Hey, what like

[75:50] schema defs, that's a good one where it's just like, what the

[75:52] hell is going on here? Why are there dollar signs in my JSON?

[75:54] So like, you don't get that from just like a GUI web app clicking

[75:59] around and being like, cool, I did some stuff on chain. I'm a

[76:01] DJ. Thanks for the airdrop. I'll be looking for that later. You

[76:06] know, that was like an actual I did an actual thing. I felt

[76:10] good.

[76:12] We will. This is this is something that we we do pay paid

[76:17] work. So we'll do that coordinate that off stream

[76:21] Anthony. And I will walk you through how to make your claim

[76:25] on that. But yeah, thanks for thanks for coming on getting

[76:29] right through all the way to the end. No. And yeah, we'll if

[76:34] there's anything else that you're interested in, if it's

[76:36] kind of piqued your interest, then there's, there's more more

[76:39] that you can do as well. So just yeah,

[76:43] yeah, of course. That was awesome. Thank you guys so much

[76:45] for having me. That was definitely an enjoyable

[76:47] experience. Always fun to do some live coding with friends.

[76:50] Thanks, Anthony. I'm sure that tutorial was a thing and a half

[76:53] to set up that was a lot to just go through, much less write all

[76:57] of it and make sure that it actually goes like that. Look,

[76:59] if I made that I'd be like, dude, so this is so much. So

[77:04] that was that was a lot of code that we went through. I

[77:06] appreciated like going through step by step. I think that

[77:09] scripts just additionally adding scripts and going through felt

[77:13] pretty good. I'm appreciate the ergonomics of defining all of

[77:18] the scripts up front in the package JSON that would have

[77:20] been very, it was like, already a thing like, hey, create the

[77:24] script in your, in your scripts folder, and then update it and

[77:27] then put something in your environment and then do it

[77:29] again. That felt like a learning process if it was also by the

[77:32] way, add this script to your package.json that would have

[77:35] been, that would have been a lot. So I appreciate the design

[77:37] decisions made in my learning journey. That was good. Anthony,

[77:41] who would have thought he is in fact, a professional tutorialer.

[77:44] So that's that's a show shows him the work. But yeah, thank

[77:49] you guys so much for having me. That was a blast.

[77:50] Yep. Yep. Thank you. And thank you for the listeners for tuning

[77:55] in. We will probably have several of these next week as

[77:59] well. Maybe even one every day. Depending on what you've

[78:03] scheduled. I know I've got some half lined up. So tune in next

[78:08] week. And we'll do it again. Thanks, everyone.

[78:11] Awesome. Bye.