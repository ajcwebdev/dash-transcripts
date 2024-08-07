---
showLink: "https://www.youtube.com/watch?v=M6_Ft3kY_G8"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Platform Walkthroughs Part 2b with Nick Taylor"
publishDate: "2024-06-14"
coverImage: "https://i.ytimg.com/vi/M6_Ft3kY_G8/sddefault.jpg?v=666b339b"
---

## Episode Description

Nick Taylor continues exploring the Dash platform by registering identities, names, and data contracts in this blockchain tutorial.

## Episode Summary

In this episode, Nick Taylor continues following the Dash Platform tutorial with guidance from Anthony and Ryan. They successfully register an identity, top it up with credits, and register a name for the identity. Then they create and update a data contract schema, discussing concepts like data contracts vs smart contracts along the way. The episode ends with a teaser for the next part where they will write to the contract and build an app.

## Chapters

00:00 - Recap and Continuation of Dash Platform Tutorial 

The episode begins with a recap of the previous part where Nick had trouble creating an identity due to network issues. This time, the identity creation works and they proceed with the tutorial.

05:56 - Creating an Identity and Topping Up with Credits

Nick creates an identity on the Dash platform and tops it up with testnet credits. They explore the created identity on the block explorer.

19:20 - Identities vs Wallets and Platform Credits vs Dash

Anthony and Ryan explain the differences between identities and wallets on the Dash platform. They also clarify how Dash is converted to credits for use on the platform chain.

31:32 - Registering a Name for the Identity 

Nick registers a name for his identity, linking a human-readable name to the identity. They debug an issue with invalid name characters.

44:01 - Data Contracts vs Smart Contracts

Anthony and Rion discuss data contracts and how they differ from smart contracts. Data contracts define a schema for data storage without executable methods.

53:47 - Creating and Updating a Data Contract Schema

Nick creates a data contract that defines a schema for "notes" with a message property. They encounter some delays and errors from the test network. Later they update the contract schema to include an author property.

67:47 - Wrapping Up and Teasing the Next Episode

As the episode nears the end, they decide to wrap up and continue in a part 3. The next episode will cover writing to the contract and building an app using the contract.

[00:00] All right, we are live.

[00:05] Welcome back to Part B of Part 2 of Dash Platforms.

[00:13] Appendix A.

[00:14] And this time the network works, so Nick, welcome back.

[00:19] For those who did not see our first parts, we are running through our Dash Platform tutorial,

[00:26] which gets you started with doing everything on Dash Platform.

[00:30] We went through the first part of this tutorial with Nick last time, we made it up to creating

[00:35] an identity, which has been a kind of sticking point as a difficult thing for the network

[00:40] to handle for whatever reason, this is something that I was kind of dealing with as I built

[00:44] this tutorial.

[00:45] So we tested it out right before we went live and it seems to be working.

[00:49] So Nick, you want to give any kind of thoughts or just things you felt after the first time

[00:57] and things you're looking forward to for this time?

[00:59] Yeah, it's always fun digging into interesting technology.

[01:06] I know blockchain's got a bit of a rap at the moment, but regardless of that, I'm always

[01:13] just curious to try out stuff.

[01:14] And obviously we didn't accomplish what we wanted to do last time, there was some network

[01:19] issues like you mentioned, Anthony, and stuff, but we gave it a good go and I think Ryan

[01:25] went back with some feedback and I think some things got stabilized in the network, I'm

[01:29] guessing.

[01:30] If I were only so powerful.

[01:32] Well, there's some good karma today.

[01:37] I cracked some whips and things are in line now.

[01:41] Yeah.

[01:42] So I guess, do you want to let them know, Anthony, where we are, I guess, right now?

[01:48] Because we did part of the tutorial in a speed run just before the live stream.

[01:53] Yeah.

[01:54] Yeah.

[01:55] So basically we created a wallet, we put testnet funds into that wallet with the testnet faucet,

[02:03] and then we created an identity.

[02:05] So just real quick, let's just look at the code for the create identity one specifically

[02:10] and kind of go over what's happening there.

[02:13] Yeah, cool.

[02:14] So scroll to the top.

[02:16] Oh, yeah.

[02:17] Sorry.

[02:18] Yeah.

[02:19] Yeah.

[02:20] Great.

[02:21] So we're importing our client, which is what has our wallet mnemonic.

[02:24] That's how you authenticate yourself.

[02:27] And then we're just running, this is like really, really simple, it's literally just

[02:30] run a single function, which is dot register on identities dot platform dot client.

[02:37] And then you have your identity and then the console logs out the identity ID and something

[02:43] we haven't done yet, actually, which we should do.

[02:46] It also gave you that link to the platform Explorer.

[02:51] So let's take your identity ID, put it in that URL, and we can go look at it on the

[02:56] platform.

[02:57] This is the new Explorer, which is different from the one we were using when we got the

[03:01] testnet funds on.

[03:04] This is going to be more specific to the identities, the documents and the things like that.

[03:10] That 404, it's because I don't have my ID in there yet.

[03:14] Yeah, it's in your terminal.

[03:15] Oh, okay.

[03:16] Sorry.

[03:17] Sorry.

[03:18] Or your .EMP, either place.

[03:19] Oh, I think I cleared my terminal.

[03:22] All right.

[03:23] Identity.

[03:24] There we go.

[03:25] Well, right away, I can tell they're using a Next.js site.

[03:28] Okay.

[03:29] So, all right, let's load this up.

[03:32] Okay.

[03:33] So here, I'll make this a bit bigger so we can see.

[03:38] Yeah.

[03:39] Oh, that's a little too big.

[03:40] Yes.

[03:41] We see here.

[03:42] Yeah, that's perfect.

[03:43] Yeah.

[03:44] So we got your identifier.

[03:45] We've got your balance.

[03:46] And then the identity create.

[03:47] You can see that that just happened, what, seven minutes ago.

[03:52] So if you click on identity create, you can see more information about that specific transaction

[03:57] on the right.

[03:58] Okay.

[03:59] Yeah.

[04:00] Okay.

[04:01] So what these are, basically every time you do an action, it's all logged on the blockchain.

[04:07] So this is like the cool thing about blockchains is that they're very transparent, they're

[04:11] very inspectable, and you can kind of just go in and see what everyone is doing.

[04:17] And then, obviously, there's ways to have privacy with things like CoinJoin and stuff

[04:21] like that.

[04:22] But have you ever used a block explorer before, Nick?

[04:29] I don't think so, unless we did in the tutorial last time, but.

[04:35] Yeah.

[04:36] That was just the one time when we checked your funds.

[04:39] Yeah, these are really important tools for blockchains in general.

[04:45] Like if you're using like Ethereum, there's Etherscan, and Bitcoin has their own.

[04:52] And there are things that anyone can make, because the blockchain is just this thing

[04:57] out there with all the data.

[04:59] And so it just has to basically make a front end that has some sort of search functionality

[05:04] to it.

[05:05] So yeah.

[05:06] So we'll be referencing this as we go through all the next steps, because we'll be creating

[05:14] data contracts.

[05:15] You can see at the top, there's home, blocks, transactions, data contracts, and identities.

[05:19] And if you go to the API, you can kind of see all the different things that are viewable

[05:26] here.

[05:28] So you can even check the status and things like that.

[05:33] Okay.

[05:35] And this is, we're on the platform explorer.

[05:39] Is this specific to only the Dash network or, because from what I remember, I think

[05:47] from blockchains, like you wouldn't have like, obviously like an Ethereum and like a Dash

[05:53] on the same network, I don't think.

[05:55] Or is that possible?

[05:56] Yeah.

[05:57] So you're totally right.

[05:58] Yeah.

[05:59] So each blockchain is kind of, it's an island of itself in one sense.

[06:04] So it's this network, bunch of computers talking to each other, they're syncing with each other,

[06:09] they're validating each other's blocks, but they're all just doing it in the confines

[06:12] of whatever blockchain, whatever cryptocurrency they're using.

[06:18] So there's other kind of like multi-chain things out there that can combine different

[06:24] chains or there's some chains that are made so that you can have kind of different cryptocurrencies

[06:29] on the same chain.

[06:31] But this Dash is like, it's like old school, it's like Bitcoin, it's just its own chain.

[06:36] And if you want to work with other things like Ethereum or Bitcoin, you can use kind

[06:41] of like services that will translate between the two or DEXs, decentralized exchanges,

[06:46] stuff like that.

[06:47] Okay.

[06:48] I will, I'll jump in and give a little bit more context there as well.

[06:51] Okay.

[06:52] Thanks.

[06:53] So if you could open a new tab on your web browser and go to blockchair.com, block chair,

[07:04] these guys obviously were capitalizing on muscle memory mistakes.

[07:09] When people.

[07:10] I've never heard of block chair.

[07:13] Block chair.

[07:14] So blockchain obviously is the closer word that you're familiar with, but sometimes when

[07:19] you're right typing, instead of like your, your muscles just take over and instead of

[07:24] writing chain, you write chair.

[07:27] So these guys got some SEO boost early days from that alone.

[07:32] But in addition to that, they also have one of the best blockchain explorers out there

[07:41] because they are multi-chain.

[07:43] Yeah.

[07:44] And so they've got Dash and just as a refresher from some of the things we discussed last

[07:51] time, Dash has actually two blockchains in, in the Dash ecosystem.

[07:58] There is our, our first blockchain, which was the proof of work chain.

[08:06] And that's, that's what you would see here in, on block chair the proof of work, typical

[08:15] Dash blockchain.

[08:16] But then coming up very soon, we also have this second blockchain that will soon be on

[08:22] main net that is now on test net.

[08:25] And that's our platform blockchain.

[08:28] And it's a proof of stake blockchain where the validators, which is a term for the node

[08:36] operator operators in proof of stake chains, it's similar to miners in proof of work chains,

[08:42] but the validators on Dash's proof of stake chain, which we call the platform chain, is

[08:51] for data, which we'll get into a little bit more in this, in this video today, that is

[08:58] the validators are master nodes, and not only, not all master nodes, but a specific subset

[09:07] of master nodes called Evo nodes.

[09:08] So I'm going through a lot of terms here.

[09:10] You don't have to remember or not, there will not be a quiz, but just for anybody that's

[09:14] interested and you too, especially how it works.

[09:20] So you will not see the platform on, you will not see a platform block explorer on block

[09:26] chair because it's just not even on main net for one.

[09:29] And it's when it is on main net, it would be something that we would have to like partner

[09:34] with them to get their engineers to inspect our proof of stake blockchain and index it

[09:41] and surface it to their user interface and things like that.

[09:44] But they could.

[09:45] And that's what to Anthony's point, all of its public data that anybody can tap into.

[09:53] So, but they do have our work chain, obviously.

[09:57] Cool.

[09:58] And just a quick question.

[09:59] The validators you're speaking of, they're on master nodes because it's super critical

[10:05] work.

[10:06] So you need it on something that's guaranteed to be up.

[10:08] Like I imagine there's like a failure mechanism for the master node if one goes down like

[10:12] some kind of round robin or some kind of networking thing going on there, but.

[10:17] Yep.

[10:18] Yeah.

[10:19] So as far as all the validators, they, they host the same blockchain.

[10:25] And so if one goes down, it's no problem.

[10:27] You know, hundreds, hundreds could even go down in our proof of work chain and that'd

[10:31] be no problem because we have thousands, literally thousands running the chain.

[10:36] So that's part of the security and reliability that's built into blockchains.

[10:42] So let's go back.

[10:43] Now, I just wanted to show you that, you know, there are like total third party block explorers

[10:49] that can just tap into any blockchain and surface lots of different blockchains, one

[10:55] user interface.

[10:57] So but this particular block platform explorer website, this was built by Mikhail Shenmik.

[11:03] He's part of the Dash incubator and he's one of our other strategists.

[11:09] So he made this site and he did that by running, he does that by, he has a node that's running

[11:18] and he's seeing, seeing blocks of data come through on the, on the public network.

[11:23] So he's listening to the right traffic on the right ports and things like that.

[11:29] And then he, you can just index whatever data you're, you're interested in, throw that in

[11:34] a local database and then surface it to this user interface, which you correctly identified

[11:38] as being an XJS app.

[11:40] Yes.

[11:41] I used to work on the frameworks team at Netlify, but also that, that white, that white error

[11:47] page, the 404 is a pretty common, it's kind of like when somebody goes, oh yeah, that's

[11:51] a, that's a WordPress site.

[11:53] Yep.

[11:55] So enough of the boring stuff out of the way, let's, let's maybe get back into some action

[11:58] with the tutorial and see if we can, we've now got past the step that we couldn't get

[12:04] past last time we registered an identity, we've got an identity ID, and now we can start

[12:09] doing things with that identity.

[12:11] Yeah.

[12:12] Cool.

[12:13] All right.

[12:14] I'm going to just take it, just follow along from, from here.

[12:17] I will just kind of observe and if things go wrong, then I'll hop in and I'm going to

[12:22] go grab some water.

[12:23] Okay.

[12:24] Cool.

[12:25] Early transactions.

[12:26] Cool.

[12:27] Yeah.

[12:28] Okay.

[12:29] We already saw my ID in the list, so that's all good.

[12:34] Okay.

[12:35] Yeah.

[12:36] This is just what we were kind of showing before.

[12:38] Okay.

[12:39] Cool.

[12:40] Cool.

[12:41] Let's go ahead and create a new file here.

[12:42] What do you think it'll do?

[12:45] Yeah.

[12:46] Yeah.

[12:47] Is that, is the browser still pretty readable or I'll, I'll, I'll make it a bit bigger actually

[12:53] there.

[12:54] Yeah.

[12:55] That's, that's probably fine.

[12:57] Just it's my paranoia from live streaming, always making sure people can actually see

[13:02] what I'm doing.

[13:03] Okay.

[13:04] Cool.

[13:05] All right.

[13:06] And it sounds like also my internet is going in and out.

[13:10] I'm at, I'm at a hotel right now with some hotel wifi.

[13:13] So if I totally crap out, then you can continue on, I'll come back in whenever.

[13:19] Yeah.

[13:20] Yeah.

[13:21] No worries.

[13:22] Cool.

[13:23] All right.

[13:24] So I'm just following instructions here to create a script to retrieve the identities

[13:28] and I imagine, yeah, we'll have an NPM run get identity.

[13:31] So let's make this, I'll just make this bigger so we can see.

[13:38] All right.

[13:40] So this is going to retrieve my identities.

[13:43] I believe.

[13:44] I'm assuming that means my wallets is that identity is wallet obviously, right?

[13:50] Or you should explain the difference between a wallet and an identity, right?

[13:53] You'll probably be able to do it better than me.

[13:55] Let's, let's see what the docs have to say about it.

[13:58] Okay.

[13:59] Cool.

[14:00] All right.

[14:01] Cool.

[14:02] So yeah, so this is retrieving them just like when we were creating the identity, I think

[14:07] it just takes a bit of time.

[14:12] Also I imagine running on a test net or a dev net would run slower than production as

[14:16] well.

[14:17] So, cause it's, but yeah, okay, cool.

[14:21] So we'll just let that finish running.

[14:23] Yeah.

[14:24] I don't know actually where the speed issue is coming from.

[14:29] Something I would like to look into.

[14:31] You go back to your, your client real quick and let's see where you're, where you're sinking

[14:35] to.

[14:36] Yeah.

[14:37] Yeah, no, that should be, that's like very, very recent.

[14:41] Yeah.

[14:42] Yeah.

[14:43] Okay.

[14:44] Yeah.

[14:45] And my, my internet's pretty fast.

[14:46] I have like gigabit up and down.

[14:49] So it's, it's definitely not on my end to, can do, can do a speed test, but I'm pretty

[14:53] sure we're good.

[14:54] Okay.

[14:55] So we'll just let that go.

[14:56] So you can go to the docs to look up the identity definition while this is happening.

[15:01] Yeah.

[15:02] All right.

[15:03] Docs.

[15:04] Docs.

[15:05] Docs.

[15:06] Dot dash.

[15:07] Dot org.

[15:08] I'll give you the shortcut there.

[15:09] Okay.

[15:10] And then once again, we are, you see now that what we discussed, we've got user docs, core

[15:16] docs and platform docs.

[15:17] We're going to go to platform docs.

[15:19] This is what we're dealing with now.

[15:21] All right.

[15:22] So introduction.

[15:23] Oh wait.

[15:24] Okay.

[15:25] It looks like we got our identity.

[15:26] So it returned an array of two identities.

[15:31] We can go look at that in a second.

[15:33] So I guess some background information.

[15:37] I'm inclined to look up identity, but let's see.

[15:41] Sure.

[15:42] Yeah.

[15:43] And just for the, you have two instead of just one.

[15:47] I'm not sure how that happened.

[15:51] Yeah.

[15:52] Okay.

[15:54] So okay.

[15:55] Identities are low-level constructs that provide foundations.

[15:58] Can you zoom in a bit?

[16:01] Okay.

[16:02] Okay.

[16:03] So yeah, it's public key.

[16:05] That makes sense.

[16:06] Sorry.

[16:07] Nick, could you zoom in just a little bit?

[16:10] Oh yeah.

[16:11] Yeah.

[16:12] Sorry, man.

[16:13] Yeah.

[16:14] No worries.

[16:15] Let's make this bigger.

[16:16] Boom.

[16:17] Boom.

[16:18] Boom.

[16:19] That okay?

[16:20] Or a bit more?

[16:21] Yeah, that's good.

[16:22] A little more.

[16:23] Okay.

[16:24] Yeah.

[16:25] Cool.

[16:26] Yeah.

[16:27] So it's essentially, I get that it's a unique identifier for you.

[16:30] So that part I guess you can have more than one wallet associated to your identity, I'm

[16:39] guessing.

[16:40] Just reading.

[16:41] Okay.

[16:42] So the ID, okay.

[16:43] Whatever.

[16:44] That's some hash calculation.

[16:45] Okay.

[16:46] It's regarding each public key associated with the identity.

[16:52] Multiple identities may use the same public key.

[16:55] I guess that's just for encrypting or not showing they're valid, I'm not sure.

[17:01] I'm definitely no cryptographer expert or cryptography expert, but I do know don't expose

[17:08] your private keys.

[17:09] All right.

[17:10] Okay.

[17:11] Okay.

[17:12] This is more super technical.

[17:17] So that's less what an identity is.

[17:19] Yeah.

[17:20] It's really here.

[17:21] It's your unique identifier.

[17:24] But I guess if I look up wallet, it's going to say you can probably have more than one.

[17:32] Yeah.

[17:35] This is probably going to take you down, not a relevant path.

[17:40] Okay.

[17:41] TBT gave a pretty good answer.

[17:45] Let's go back to the, I think there's a concepts section in the documentation and that might

[17:53] be a better conceptual overview, which is what seemed to be looking for.

[17:59] And just so that everybody knows, I'm trying to test the documentation as much as the code

[18:06] in these live streams.

[18:08] So I want to be able to have people find their answers.

[18:13] Yeah.

[18:14] I mean, all the information is in the docs.

[18:16] It's just hard to find.

[18:18] The docs are pretty comprehensive, but they're not easy to navigate.

[18:21] Yeah.

[18:22] Well, I think one thing as a user of just searching a site in general, typing something

[18:27] in here should definitely bring me somewhere relevant for what I'm looking for.

[18:32] When I put in wallet, like you said, there's information about wallet, but it's not...

[18:38] We have an intro to wallet because this is like how you fund it and stuff, but I mean,

[18:45] I think most people understand the concept of a wallet, but just I'm getting back to

[18:48] my question about the identity and the wallet.

[18:52] But okay.

[18:53] So you're saying...

[18:54] I'm saying glossary.

[18:56] Scroll down the left-hand navigation and see there's...

[19:02] So we're in the tutorial right now, and then there's explanations and under explanations,

[19:07] there's identity.

[19:09] So maybe that might be a better approach.

[19:13] Okay.

[19:14] Yeah.

[19:15] So again, it's identity, so we can identify each other.

[19:23] Identities are separate from names.

[19:25] That makes sense because I could have a vanity name or a username, like NickyTOnline, but

[19:31] it's linked to my actual identity, just because it's typically not...

[19:39] I don't think people memorize their identities or wallet IDs usually.

[19:44] Maybe they do.

[19:45] I don't know.

[19:46] Okay.

[19:47] Cool.

[19:48] Yeah.

[19:49] So it consists of one or more public keys recorded on the platform chain that can be

[19:53] used to control the user's profile and sign in their documents.

[19:57] Each identity also has a balance of credits.

[20:01] Okay.

[20:02] So that's where I'm confused already because the identity saying it can have credits makes

[20:08] me think it's a wallet now.

[20:13] But also maybe it's...

[20:14] Maybe credits here is a different type of credits.

[20:20] What is this?

[20:22] That's weird.

[20:23] That didn't bring me to...

[20:25] Yeah, I think it's one of those weird links that it's just going to pop, do a little...

[20:29] Oh, it's an anchor tag.

[20:31] Yeah.

[20:32] It's in the page down below.

[20:33] Okay.

[20:34] Yeah.

[20:35] Okay.

[20:36] Oh.

[20:37] That was...

[20:38] Credits are the mechanism for paying fees that cover the cost of platform usage.

[20:41] Once the user locks Dash on the core blockchain for its ownership, create a top-up credit.

[20:46] Okay.

[20:47] So to me, at least from reading this, it makes it sound like the identity really is the wallet,

[20:54] which I find confusing because I know it's not.

[20:57] Yeah.

[20:58] So here's part of the problem.

[20:59] Understanding the difference between the wallet and the identity is something that's pretty

[21:02] specific to the difference between Dash itself and then the Dash platform, and what the difference

[21:09] between those two are.

[21:10] So the wallet is what lets you just transact and have money, and that's like Dash itself.

[21:15] That's the main thing.

[21:16] Oh, yeah, yeah, yeah, yeah.

[21:17] Okay.

[21:18] This platform thing is where we're going to have identities, which are going to allow

[21:22] us to create documents, which are going to allow us to persist storage, or allow us to

[21:26] create things like dApps and all that kind of stuff.

[21:28] So I don't think that explanation is anywhere in the docs.

[21:30] Yeah.

[21:31] Okay.

[21:32] Yeah.

[21:33] So wallet is like a physical wallet, whereas my identity is, think of it as like one of

[21:38] the credit cards in the wallet.

[21:41] But the wallet, since the wallet doesn't physically exist, it needs an address, and that's why

[21:46] wallets have an address in your identity.

[21:48] I don't know.

[21:50] Yeah.

[21:51] Yeah.

[21:52] They're very similar concepts.

[21:57] They're all based on public-private key pairs.

[22:00] And whether something is a wallet or, you know, the term "wallet" itself can be confusing

[22:08] because everybody uses it somewhat differently.

[22:11] For example, I think of a wallet as the 12-word phrase, because that's what derives your...

[22:19] Oh, okay.

[22:20] Yeah, that's what you can derive your public-private key pairs from.

[22:27] But some people think of wallet as like a public-private key pair itself, and other

[22:32] people might think of a wallet as like the user interface that takes in a 12-word phrase

[22:39] or a public-private key pair.

[22:40] It even gets more confusing because you have the 12-word phrase, and then you have the

[22:42] address, and you can create multiple addresses in your wallet.

[22:46] Yeah.

[22:47] So maybe what I'm getting from this conversation is it might help to have right off the bat,

[22:54] and maybe it is there, and maybe we just missed it in the intro-intro section, because that's

[22:59] where it would be, but something that shows the hierarchy of these terms and these concepts

[23:06] where 12-word phrase that you use to derive this and that, which is used to derive this

[23:15] and that, and then on the platform side, you have the 12-word phrase in addition to deriving

[23:21] wallets or addition to driving public-private key pairs that are associated with funds,

[23:29] they also can derive...

[23:31] You can also derive from that identities, which can then derive other things that are

[23:37] related to wallets as well.

[23:39] So I would note of that, and we can move on, but go back to...

[23:46] Last thing to say on this also is that I don't think this is just a Dash problem.

[23:50] This is, I think, a blockchain-wide problem, which is it's really hard to just explain

[23:55] things in a simple way that lets you get it.

[23:57] It's really...

[23:58] And I've worked with a lot of blockchains, and it's really only through actually going

[24:02] through a tutorial.

[24:03] And by the time you get to the end and then do it a second time, that you actually have

[24:07] a framework where you can kind of put everything in, it's really hard to just give a high-level

[24:12] explanation of this tech just because it's so specific and works in a very specific way.

[24:18] Yeah.

[24:19] Yeah.

[24:20] Yeah.

[24:21] Okay.

[24:22] So I don't know if you finished with the identity paragraph.

[24:25] Oh, yeah.

[24:26] I think we should at least finish that paragraph, and then we'll move on to continuing with

[24:31] the tutorial, because that might make things a little bit more clear.

[24:36] Yeah.

[24:37] Yeah.

[24:38] Yeah.

[24:39] Okay.

[24:40] Yeah.

[24:41] And we stopped because each identity also has a balance of credits.

[24:43] Yeah.

[24:44] That's just a blocking layer of one funds.

[24:48] That makes sense to me.

[24:50] And let me...

[24:51] Yeah.

[24:52] Let me explain that one just a little bit further conceptually, just because it is kind

[24:57] of an important concept.

[24:58] And we've discussed that we have two blockchains, the proof of work blockchain, that's where

[25:05] you're getting funds.

[25:06] So the way that we got testnet proof of work, layer one blockchain funds is from that testnet

[25:13] or that faucet.

[25:17] That's how we originally got the layer one funds.

[25:20] Now we have not, when we want to convert layer one funds to the platform chain, which is

[25:28] a completely different blockchain, but happens to use the same, well, it doesn't even use

[25:37] the same funds per se.

[25:40] What it does is you can do a transaction on the layer one proof of work layer one blockchain

[25:48] that locks funds.

[25:51] It locks funds on the layer one blockchain and says, these funds are no longer usable.

[25:57] Okay.

[25:58] Okay.

[25:59] And by doing that, you also unlocking a certain amount of funds on the proof of stake chain.

[26:08] And that's what this whole process, when it says credits, it means Dash that is living

[26:16] on the proof of stake chain has a certain denomination that we'll get into a little

[26:22] bit.

[26:24] But credits are Dash, they're a denomination of Dash.

[26:28] So you can think of like, you could have dollars in your wallet.

[26:32] And then if you give that to some kind of, you give that to a bank and then they give

[26:40] you one, 101 cent pieces back, like that's the difference between Dash and credits is

[26:47] it's just, it's the same money, but it's in a different form on a different chain with

[26:53] a different denomination.

[26:55] So that'll hopefully make a little bit more sense as we get through the examples as well.

[27:00] Okay.

[27:01] So the credits freezing on the proof of work, and then having funds accessible on the proof

[27:08] of stake is kind of the way of exchanging them, I guess.

[27:12] Yeah.

[27:13] Yeah.

[27:14] So there's the same transaction that you can do in reverse, where if you want to take your

[27:19] platform credits, the Dash living on the proof of stake chain and convert it back into the

[27:25] Dash that's living on the proof of work chain, then you can do a transaction to do just that

[27:31] and move them, move those funds back.

[27:34] So I'll have to think about better ways to explain that, but that's basically what's

[27:39] going on.

[27:40] Cool.

[27:41] All right.

[27:42] Let's get back here and I'll just get my editor back up.

[27:48] Okay.

[27:49] So we got the identities.

[27:52] I have two and Anthony said he wasn't sure why.

[27:56] I wonder if that's somehow from the last tutorial that didn't work, maybe.

[28:00] I don't know.

[28:01] Maybe we did it a bit because we created a fresh wallet at the beginning.

[28:04] Okay.

[28:05] Yeah.

[28:06] I'm a little surprised by that too, but that's because I haven't played around with this

[28:10] that much.

[28:11] That's why we're doing this series.

[28:13] Okay.

[28:14] So, okay.

[28:15] So this one seems pretty self-explanatory to me.

[28:18] We're going to create a script called top up identity.

[28:20] So we're going to put some Dash in there, I guess.

[28:24] So let's go ahead and copy this and let's paste that in.

[28:37] So I'm just going to look at this real quick.

[28:40] So another async function importing from the client API.

[28:47] So we're getting the wallet account and then getting the identities associated to it, then

[28:54] we're looping or iterating over all the identities we have.

[28:59] And this is a test net.

[29:00] So I guess I'm allowed to give myself, is that a billion?

[29:05] No, sorry.

[29:06] That's three, 10 million Dash, I guess I get to top off.

[29:12] That's pretty sweet for a live stream, not too bad.

[29:15] They're not Dash, they're Duffs.

[29:16] A Duff is like a Satoshi, which you don't know what that is either.

[29:19] So that doesn't help.

[29:20] I've heard of Satoshi, he's the supposed creator of Bitcoin, but I guess there's a coin named

[29:27] after him too.

[29:28] So Anthony, just real quick.

[29:32] Are you sure that the 10 million is a Duff value or is it a credits value?

[29:39] I thought credits are Duffs.

[29:41] No.

[29:42] I explain this specifically in my blog post, so go back over to the blog post and either

[29:47] scroll up or down, there's a specific explanation for this.

[29:51] Okay, yeah.

[29:52] So, okay.

[29:53] Okay, 100 million Duffs.

[29:54] Go ahead and read it out.

[29:56] I'll read it all out so that we don't have to rush through this.

[30:01] Yeah.

[30:02] Yeah.

[30:03] Okay.

[30:04] Yeah.

[30:05] All right.

[30:06] So it says when an identity is created a special, here, I'll just make this a bit bigger, might

[30:10] as well.

[30:11] So when an identity is created, a special transaction transforms Dash into credits,

[30:17] which are used to interact with the Dash platform.

[30:20] When Dash is equal to 100 million Duffs, is that like Duffman from like the Simpsons?

[30:25] Just curious.

[30:26] That's what I thought.

[30:27] That's exactly what I thought.

[30:29] Dash is a version of Satoshi, which is, I guess, a lower value coin.

[30:35] And 100 million Duffs is equal to 100 billion credits.

[30:39] Interacting with Dash platform applications increases your credit balance.

[30:43] At a certain point, you need to top off the balance by converting some Dash to credits.

[30:48] And that makes sense, like if you're using it-

[30:52] That's basically what I just described.

[30:54] Yeah.

[30:55] Yeah.

[30:56] Okay.

[30:57] And if you're working with a Dapp, a distributed app, distributed application, right?

[30:59] That's what Dapp stands for?

[31:00] Yeah.

[31:01] Decentralized application.

[31:02] Yeah.

[31:03] Decentralized.

[31:04] Thank you.

[31:05] Yeah.

[31:06] I'm going to throw some credit to use it.

[31:09] Okay.

[31:10] So we're going to run the top off here.

[31:14] Let's go back down here.

[31:15] Before we do that, did we get a layer one blockchain explorer working for us?

[31:24] Which one was that?

[31:25] Which shows the balance of the address that we've funded.

[31:30] Okay.

[31:31] Oh, yeah.

[31:32] We were there before it's here, I believe.

[31:35] Yeah.

[31:36] So let's see how much we have in this address so far or at this point.

[31:43] So it says 4.1712 Dash.

[31:47] Okay.

[31:48] This is surprising because it has a final balance of zero.

[31:53] Let's just refresh it.

[31:54] This is old, I think.

[31:55] Okay.

[31:56] It should have been confirmed by now.

[31:57] There we go.

[31:58] 7.62.

[31:59] Okay.

[32:00] It still has zero balance for some reason.

[32:04] So that's going to be a problem.

[32:05] I thought that might be an error with the UI.

[32:08] This happened to me when I was using this the other day.

[32:10] Oh, you're kidding.

[32:11] You mean it's not...

[32:16] You mean it's...

[32:17] Okay.

[32:18] No.

[32:19] It's got zero in the markup.

[32:20] You mean it's just calculating something wrong client side or the API is just...

[32:23] If it was zero, we wouldn't have been able to create the identity.

[32:25] So it can't be zero.

[32:27] We know for a fact it's not zero.

[32:28] That's why I say all this stuff is broken, man.

[32:31] Your whole deal is broken.

[32:33] Well, this is the summary up top, but can we see the individual transactions?

[32:38] There's 10 confirmations.

[32:39] That's what I...

[32:40] Yeah.

[32:41] Scroll down to the bottom.

[32:42] The bottom will be the earliest transactions.

[32:43] Let's just follow this.

[32:45] Okay.

[32:46] So the four is the initial when I created the account.

[32:52] This I don't know.

[32:53] So 6,040, 6,240 confirmations is way long ago.

[32:58] So the address that we're looking at, let's make sure that this is the address that you

[33:02] own.

[33:04] And it's not like some...

[33:06] Oh yeah.

[33:07] Yeah.

[33:08] I feel it.

[33:09] Yeah.

[33:10] I wonder if...

[33:11] YZPZ.

[33:12] YZPZ already at the end.

[33:13] Okay.

[33:14] So that is your address.

[33:15] That's the identity, Nick.

[33:16] Sorry?

[33:17] That's the identity.

[33:18] Oh yeah.

[33:19] Sorry.

[33:20] Sorry.

[33:21] Sorry.

[33:22] Sorry.

[33:23] So your wallet address is that.

[33:31] But how on earth could we have a wallet address that we just created have some activity 6,000

[33:42] confirmations ago?

[33:43] Nick, you drop the wallet in the chat just so I can try it.

[33:48] I want to try searching this on the regular old Explorer, not this other one.

[33:55] Yeah.

[33:56] Okay.

[33:57] And well, the confirmations are what exactly?

[34:00] It's like the change is saying this transaction is valid, and then there's a bunch of nodes

[34:05] that confirm?

[34:08] Confirmations is how many blocks have occurred since a certain date, a certain action.

[34:16] So this is saying, this is a list of transactions that we're looking at.

[34:22] And the very earliest activity on this is 6,240 confirmations or blocks ago.

[34:32] And as you can see, that's June 3rd.

[34:35] We haven't done anything.

[34:37] We should not have had any activity on this until today.

[34:40] So why we're seeing something from June 3rd, I don't know.

[34:46] So scroll.

[34:48] Any ideas, Anthony?

[34:50] Scroll up to, let's see what the first thing was that happens today instead of June 3rd.

[34:55] So just scroll up a bit on this.

[34:58] Are you, oh, you're muted, Nick.

[35:07] Go ahead and scroll up on that page.

[35:09] Nick, you're muted.

[35:11] I cannot unmute him, I think.

[35:15] Oh, cannot unmute, yes.

[35:17] Their mic isn't connected.

[35:19] Oh, he's having some technical issues.

[35:27] So any ideas on this, Anthony?

[35:29] I mean, I'm just like...

[35:30] I think it's a bug in the code somewhere.

[35:32] I mean, this isn't the actual Explorer.

[35:34] This is this weird extra Explorer on this different link, which probably means there

[35:38] might just be like a bug in the code somewhere or the way it's reading in the blockchain,

[35:42] it's getting messed up somehow.

[35:43] I mean, like I remember there was like a, you used to show me there was like a status

[35:46] page and the status page said it was like November or something.

[35:50] So it could be a similar thing, you know.

[35:58] Nick, we still can't hear you.

[36:13] He's talking.

[36:16] I wonder if he can hear us.

[36:18] That's the question.

[36:19] Okay.

[36:20] We lost him.

[36:21] He's gonna...

[36:22] I think he probably bailed on purpose to reconnect.

[36:25] Let's see what the private chat says.

[36:27] Okay.

[36:28] That's just you.

[36:29] Yeah.

[36:30] I think we should just keep going through the tutorial and not worry about this.

[36:32] Okay.

[36:33] I mean, yeah, I was looking at this so that we could see the actual when you did that

[36:42] transaction to see how much was taken out.

[36:45] But anyway, on the topic of transaction, but yeah, well, when he comes back, we'll just

[36:50] we'll just keep going through the tutorial and we'll forget the conceptual stuff.

[36:54] Because the part of the issue is that like, there's this weird separation between, you

[36:59] know, the Dash and the Dash platform.

[37:01] So if we just like stay in Dash platform world, create an identity, create documents, like

[37:05] by the point of this tutorial.

[37:06] So I think we're going out of scope, I think, by trying to worry about all this other stuff.

[37:11] So Nick says he'll be back in a second, not sure what happened.

[37:14] While he's talking about that, or while he's gone.

[37:20] Just so you know, if you haven't seen yet, Anthony, there is a proposal up.

[37:25] And if you could bring, share your screen for a minute, this might be interesting for

[37:32] viewers and you, if nobody else.

[37:37] Bring up your website, share your screen and then go to dashcentral.org.

[37:47] This is somewhat relevant to this conversation, that's why I'm bringing it up.

[37:51] Now go to budget.

[37:54] Yeah.

[37:57] So these are all the active proposals.

[37:59] Not all of them are budget proposals.

[38:01] Most of them are proposals requesting funding, which is how the Dash incubator is funded.

[38:06] But this one at the very top here, Evo accelerated release schedule, click in there.

[38:13] This is a proposal by Quantum Explorer, Sam Westrich from Dash Core Group, basically asking

[38:21] the network, hey, telling the network, we're basically at a point where we could actually

[38:26] launch platform on mainnet instead of testnet.

[38:32] But there would be, you know, if we do it now, then there would be some features that

[38:37] might not be, that would be missing that we wanted to put in the version one that goes

[38:43] to mainnet.

[38:47] But there would, and there would also be some, a little bit higher degree of risk that there

[38:53] might be a platform halt, like a chain halt, but nothing that should jeopardize the stability

[39:01] of layer one blockchain or steal funds from platform.

[39:07] And part of it is that you won't be able to withdraw your funds from platform.

[39:12] But at least we could get it on mainnet.

[39:14] So that's the reason that that's relevant to today's discussion is all of these issues

[39:20] that we're seeing with like block explorers not working and not reliable.

[39:27] And those would all kind of go away once we get to mainnet, because.

[39:30] Exactly.

[39:31] And that's what I'm saying.

[39:32] I feel like it's kind of out of scope for us, like really worry about too much right

[39:35] now.

[39:36] Yeah.

[39:37] Because it's just going to work itself out.

[39:40] So this is cool.

[39:41] So what is, when it says accelerated release schedule, what does that mean?

[39:44] How accelerated, what would the actual schedule be?

[39:47] Yeah.

[39:48] So just, it's in here somewhere in the text.

[39:51] We'll find it.

[39:52] It's not a long proposal, so we should be able to find it pretty quickly.

[39:56] I think it says, let's see, middle July.

[40:06] So the paragraph right above the underlined bolded text, that would be tight.

[40:12] Yep.

[40:13] So basically like a month from now, it would be, I would say that that's going to be end

[40:18] of July.

[40:19] Yeah.

[40:20] Yeah.

[40:21] But that would be nice because then we wouldn't have to deal with these testnet issues that

[40:27] are unrelated to what we're doing.

[40:30] Yeah.

[40:31] Hey, what's up?

[40:32] Hey, Nick.

[40:33] Welcome back.

[40:34] Perfect timing.

[40:35] That was really weird.

[40:36] My internet didn't go down, but like my USB, like headphones and mic just, they just died.

[40:44] Well, not died, but it's just.

[40:46] If you go to your settings real quick and make sure you're going through the right mic

[40:49] right now, you sound kind of echoey.

[40:51] I think that's probably the issue.

[40:53] He's on a different mic now because that one wasn't working, I would guess.

[40:57] This should be okay now.

[40:58] There we go.

[40:59] Yeah.

[41:00] All right.

[41:01] Let's get back into our business.

[41:02] All right.

[41:03] Back into the decentralized matrix.

[41:04] All right.

[41:05] So did you run the top up?

[41:06] Yeah.

[41:07] Top up identities.

[41:08] Yeah.

[41:09] Yeah.

[41:10] I ran that.

[41:11] So.

[41:12] All right.

[41:13] Cool.

[41:14] I'm just going to take discord off the screen cause we don't need that there.

[41:22] Okay.

[41:23] Yeah.

[41:24] I ran the top up and then we were just looking at the, I'm going to have to go back to the

[41:28] tutorial and go forward with a function, whatever function is after top up identity.

[41:35] Okay.

[41:36] So I did top up.

[41:37] I don't know.

[41:38] Run the, run the retrieve identities one again, and then we can see what you're, what you're

[41:43] at.

[41:44] Okay.

[41:45] And then while that's going, you can kind of scroll to the next, the next section after

[41:52] top up identities in the blog.

[41:54] Okay.

[41:55] This is, this is a good, this is a good place to, to get you cause this is where, I think

[41:59] the identities makes more sense once you understand how it connects to the name.

[42:03] Okay.

[42:04] Okay.

[42:05] So, okay.

[42:06] This output that's from the top up identities that already happened.

[42:12] Okay.

[42:13] So we'll create this file.

[42:14] Let me just open up another tab.

[42:17] Okay.

[42:18] And let's exit that.

[42:21] Okay.

[42:22] Cool.

[42:23] And then I'm just going to pop this here and register name.

[42:30] Cool.

[42:31] Why did it, sorry, so that's, that's a little bit, oh yeah, .env.

[42:38] This is for your identity, so this is whatever name you're going to want to give yourself.

[42:43] So all right, let's go Jake Peralta or Pontiac Bandit.

[42:54] Anybody watch Brooklyn Nine-Nine?

[42:56] I didn't catch the reference.

[42:57] Oh nice.

[42:58] Sorry.

[42:59] Yeah, it's a team show.

[43:00] I really liked, okay, cool.

[43:05] So let's just check on the script here.

[43:08] Okay.

[43:09] That's still running.

[43:10] I'm not sure if you can have underscores in your name.

[43:12] I know you can do dashes.

[43:14] Okay.

[43:15] If that's the case, I would suggest that the tutorial not have them in it.

[43:20] Well, we could see what happens when it doesn't work.

[43:22] Yeah.

[43:23] Let's find out if it works then.

[43:24] Yeah.

[43:25] All right.

[43:26] Fire it up.

[43:27] Hashtag YOLO.

[43:28] Let's do this.

[43:29] Yeah.

[43:30] Okay.

[43:31] This is still running in terms of retrieving identities.

[43:32] Retrieving identities is forever slow.

[43:35] You got to make an effort.

[43:36] Yeah.

[43:37] Cool.

[43:38] Okay.

[43:39] So we're going to register a name here.

[43:40] I'm just going to read through the code here.

[43:41] So we've got the, my identity ID, which is coming from my environment variables.

[43:49] We get the unique identity on the dash network, and then I decide on a name and this creates,

[43:58] it registers my name dot dash.

[44:01] That's not, that's not for a file name, is it?

[44:03] Or is that just, just a syntax for, for a name registration?

[44:10] And then here, okay.

[44:12] We're just going to say view on the blocks floor.

[44:14] Okay.

[44:15] And then I can see my name and that will be my ID, which comes from.

[44:22] Dot dash is because, do you remember a couple of years ago when everyone had like AJCwebdev.eth

[44:28] in their Twitter handle?

[44:29] Oh, okay.

[44:30] Yeah.

[44:31] Yeah.

[44:32] Yeah.

[44:33] Yeah.

[44:34] Okay.

[44:35] Gotcha.

[44:36] Yeah.

[44:37] Okay.

[44:38] I was getting confused.

[44:39] I thought this was a template string issue, but this is actually the property on the object

[44:40] dollar ID.

[44:43] I do believe so.

[44:44] Yes.

[44:45] Okay.

[44:46] Cool.

[44:47] Yeah.

[44:48] All right.

[44:49] Let's just go check on the, okay.

[44:50] This is still running the retrieve identities.

[44:52] It ran faster last time.

[44:53] I'm not sure why it's slower now, but okay.

[44:56] We'll just, okay.

[45:00] So anyways, this is gonna, am I able to register my name even though the retrieving identities

[45:06] is happening?

[45:07] Like we're, we'll just let that do its thing.

[45:10] Okay.

[45:11] Cool.

[45:12] All right.

[45:13] Cool.

[45:14] And let's come here and let's go register name.

[45:19] All right.

[45:24] Boom.

[45:27] Okay.

[45:30] We'll let that go and oh, okay, there we go.

[45:46] Just let that go.

[45:48] So, okay.

[45:49] So it should output my label.

[45:52] Is that what it's going to do?

[45:55] Okay.

[45:56] Okay.

[45:57] And then.

[45:58] Let's go ahead and open that platform explorer again.

[46:05] Okay.

[46:06] Go to the main page.

[46:08] Let's see if there's activity on, yeah.

[46:13] Okay.

[46:14] Okay.

[46:15] So just go to the home page.

[46:18] Yeah.

[46:19] Okay.

[46:20] And let's see, go to the transactions and just let's see if, okay, I thought those were

[46:32] links there.

[46:35] Trending data.

[46:36] Okay.

[46:37] Yeah.

[46:38] Yeah.

[46:39] Okay.

[46:40] Identity create.

[46:41] I wonder if that was us that did that 6/13.

[46:45] So there's documents batch.

[46:49] I wonder if that's all of our transactions.

[46:51] I'm just going to go see in the terminal.

[46:56] Yeah.

[46:57] Okay.

[46:58] Okay.

[46:59] So it looks like the retrieve identities finished.

[47:00] Yeah.

[47:01] So I didn't do this in the post, it's just because my environment variable brain just

[47:08] writes everything with underscores, but it only accepts characters, numbers, and dashes.

[47:13] And dashes cannot be at the beginning or end of the name.

[47:16] That is the, there's a regex constraint that runs on, it's what it's showing right here.

[47:21] Okay.

[47:22] So that was a good error.

[47:23] That was an error where we expected an error, or it happens.

[47:27] Yeah.

[47:28] Exactly.

[47:29] Yeah.

[47:30] Yeah.

[47:31] I'm going to push that to the right now.

[47:32] So a regex can bring you to your knees.

[47:33] All right.

[47:34] Noted.

[47:35] Okay.

[47:36] All right.

[47:37] Cool.

[47:38] Cool.

[47:39] Yeah.

[47:40] So we got the, do I need to do anything with the retrieved identities?

[47:41] Do I need to just copy that array or was it just more informational?

[47:44] No, this is just, I wanted to see the balances and see how they change, but we don't really

[47:50] know what they were beforehand because you keep clearing your terminal.

[47:53] Cool.

[47:54] All right.

[47:55] A little trash talk, but I'll take it.

[48:00] Okay.

[48:02] So we looked at the Explorer.

[48:03] Okay.

[48:04] So should I go to my, like this says document here.

[48:08] So like, what is this document specifically?

[48:11] Because like, I know, is that a specific block on the chain?

[48:16] We should actually get, we should rerun the register name function, get actually working

[48:20] and then that will output the link for you and then we can explain it.

[48:23] So just go fix your, your label, your document.

[48:27] It's running right now.

[48:28] Oh, it's already running.

[48:29] Okay.

[48:30] Cool.

[48:31] Yeah.

[48:32] And I'll just get out of this one here.

[48:33] Cool.

[48:34] Yeah.

[48:35] So, okay.

[48:36] We'll let that finish.

[48:37] I'm just going to go back to the tutorial for a sec, but so, okay, so when I go to it,

[48:44] Well, because that's running and there's nothing we can do to make that any faster.

[48:49] Yeah.

[48:50] Yeah.

[48:51] So just click that link.

[48:52] All right.

[48:53] There you go.

[48:54] Here we go.

[48:55] Cool.

[48:56] Okay.

[48:57] So you are on the network.

[48:58] Good.

[48:59] Jake Peralta.

[49:00] All right.

[49:01] Cool.

[49:02] We did it.

[49:03] So yeah, I guess, so identifier, this, this is like my kind of network name and this is

[49:11] just like a, a label to make it easier, kind of like a URL redirect.

[49:16] Like you were saying, like jakeperalta.dash would go to my block explorer or address or?

[49:26] Well this is, okay.

[49:27] So we should probably keep going with the tutorial before I talk too much longer about

[49:33] everything.

[49:34] Let's just see how far we can get and then we'll, we'll circle back and answer questions.

[49:39] Yeah.

[49:40] Sounds good.

[49:41] Cool.

[49:42] All right.

[49:43] So we've got some data back.

[49:44] Okay.

[49:45] We did the retrieve.

[49:47] Let's do retrieve name.

[49:49] So let's copy that.

[49:51] I will not clear the terminal for Anthony.

[49:55] Cool.

[49:56] Cool.

[49:57] All right.

[49:58] Also, hopefully the tutorial, I think the tutorial does answer the question that you

[50:03] may have been asking there.

[50:05] Okay.

[50:06] Anthony's tutorial usually tells you what you're doing and, or what you just did.

[50:12] Kind of.

[50:13] It depends.

[50:14] All right.

[50:15] Cool.

[50:16] Let's see.

[50:17] Let's come back here.

[50:18] Okay.

[50:19] We've got that.

[50:20] Let's do NPM run, retrieve name.

[50:25] Just going to hide that.

[50:27] Okay.

[50:28] Cool.

[50:29] All right.

[50:30] Let's let that run.

[50:33] And so looking at this, it's going to take our label, which is Jake Peralta.

[50:38] It's going to say, go and resolve that, I guess, network address, which is jakeperalta.dash,

[50:44] like you were saying, kind of like the .eth.

[50:47] And then it found me.

[50:50] And this is my, no, that's not my identity.

[50:55] That's, I'm not sure what that is.

[50:59] I don't see my-

[51:00] I think that's your identity ID.

[51:02] Oh, is it?

[51:03] Yeah.

[51:04] Okay.

[51:05] I think so.

[51:06] Yeah.

[51:07] I'm confusing it with, in the .env with, I'm confusing it with the wallet address.

[51:12] That's why.

[51:13] Yeah.

[51:14] So that's what I was going to say.

[51:15] As we go on, hopefully it should be kind of more clear what the difference between the

[51:18] identity ID and wallet address is.

[51:21] Okay.

[51:22] Cool.

[51:23] Yeah.

[51:24] I see there is a little bit of an issue there, because one's called identity ID and one's

[51:27] called owner ID.

[51:28] Same string.

[51:29] Yeah.

[51:30] Yeah.

[51:31] I'd say in terms of when you're talking about the docs and stuff, Ryan, just keeping the

[51:37] uniform naming would definitely help.

[51:39] But okay.

[51:40] But that makes sense.

[51:42] Owner identity.

[51:43] Okay.

[51:44] And let's continue.

[51:46] So we got all that information and we can go view it on the block, explored it.

[51:54] Well we saw that before, actually, so we don't need to do that.

[51:58] Okay.

[51:59] So data contract on the platform, CIRM says blueprint for the structure of data that an

[52:05] application tends to store.

[52:08] Okay.

[52:09] On that network.

[52:10] Okay.

[52:11] Yeah.

[52:12] Yeah.

[52:13] Okay.

[52:14] Yeah.

[52:15] Yeah.

[52:16] Yeah.

[52:17] Okay.

[52:18] Yeah.

[52:19] Contract validates stuff.

[52:20] It's the same thing as a smart contract, right?

[52:21] Saying contract is equivalent to saying smart contract, or is smart contract a specific

[52:25] chain term?

[52:28] It's kind of a more of specific...

[52:30] Most contracts are smart contracts in blockchain world and web three world, but Dash is doing

[52:36] different things.

[52:38] We have data contracts, but you can...

[52:42] So instead of...

[52:43] A smart contract has both methods and properties on an object.

[52:50] You can think of it as that, where you have execution and you can perform functions with

[52:55] a smart contract.

[52:56] With a data contract, it's just data.

[52:59] So if you're thinking of it in terms of an object, you just have data fields, no methods.

[53:06] There's no concept of execution in data contracts.

[53:11] You just...

[53:12] So you can't have a bug where you accidentally can siphon off all your funds to someone else.

[53:16] It's a lot simpler.

[53:17] Okay.

[53:18] It's...

[53:19] Yeah.

[53:20] So the difference is, instead of a cloud Lambda function, that would be like the web three

[53:27] version of a cloud function would be a smart contract.

[53:32] The web three version of a decentralized database would be Dash platform.

[53:40] So we are just doing a decentralized database.

[53:43] We're not doing decentralized cloud functions.

[53:45] Cool.

[53:46] All right.

[53:47] I'm registering the contract.

[53:48] I got the contract ID back, which is good.

[53:53] And then it'll show us the contract registered.

[53:57] And imagine this is the definition of the contract.

[54:00] So the contract documents, is this a...

[54:05] I'm assuming this is a standard structure for a contract or is this the part of a contract

[54:11] where like...

[54:12] Well, I guess the properties are the thing that can be whatever you want.

[54:15] Yeah.

[54:16] See if this makes sense to you just reading the code.

[54:18] Yeah.

[54:19] So there's the...

[54:20] This doc has a note of type object and the object has the properties message and it has

[54:26] a...

[54:27] It's strongly typed.

[54:28] It's a string and it's the first position.

[54:31] And I guess in the block in the chain, which is the contract, I'm guessing.

[54:39] Kind of like a memory...

[54:40] I'm not entirely sure what the position means actually.

[54:47] I feel like it would be kind of like old school.

[54:53] Position is something that was literally just added like a few days ago to these documents.

[54:59] So I actually asked somebody about this before we got on the stream.

[55:06] Code was written over two months ago, that was that.

[55:09] It was in the docs somewhere.

[55:11] Yeah.

[55:12] We'll skip the position part because neither of us really know what it is.

[55:17] But basically it's just an object that has a message, the message is typed.

[55:21] This is a hello world example.

[55:23] Yeah.

[55:24] And even further up the chain there, note is something that you define.

[55:32] So you defined that this is going to be a contract that holds notes and this note is

[55:39] of type object and has these properties where you have a message that's of type string and

[55:46] so forth.

[55:47] Okay.

[55:48] So this is JSON schema validation basically.

[55:51] Okay.

[55:52] So here is whatever you want it to be.

[55:53] And you're saying there's no methods on here.

[55:57] It's just properties because you can't, I guess, because it's immutable.

[56:00] But if you create the contract, so here we're saying it's a note and it's an object and

[56:07] it has so note.message is a string.

[56:12] If this doesn't have methods, maybe this is further down in the tutorial, but how do I

[56:16] set the message then?

[56:19] So the platform itself, the chain side of this whole process basically has CRUD operations.

[56:29] You can create these things, you can edit these things, you can update them, you can

[56:34] delete them depending on how you set up your properties initially.

[56:40] So initially you can actually make it like this can't be deleted or this can't be updated,

[56:46] but you can optionally make it that it can be updated and deleted.

[56:53] The blockchain itself is performing the CRUD operations, the user can't define methods

[56:59] at this point.

[57:00] Yeah.

[57:01] Okay.

[57:02] Okay.

[57:03] So if I were to put new data on, like, let's just say I have a note taking dap and I want

[57:08] to create a new note, I'm going to say, go get me this contract and it has this shape

[57:14] of an object and I can basically say, use that as the template to actually do the CRUD

[57:22] operation.

[57:23] Like the contract will validate to say, like, I want to go add a note and it's going to

[57:27] go check the contract and go like, oh, that's an invalid note.

[57:30] You didn't put a message, like that's basically what it's doing.

[57:33] Yeah.

[57:34] Yeah.

[57:35] That's the chain side or the server side validation will allow or not allow that.

[57:41] All right.

[57:44] The register contract worked, but I don't know why it's the script isn't finishing.

[57:51] I'm just going to stop it for now, but just mentioning that in case that's an issue.

[57:56] Okay.

[57:58] So we're going to go and create a retrieve contract script.

[58:04] Did you put the contract ID in your .env?

[58:15] No, not yet.

[58:20] All right.

[58:23] So we created the retrieve contract.

[58:26] Cool.

[58:28] Let's copy this.

[58:31] Again, it's going to just get the contract that we just created.

[58:35] So the note object in that particular contract, let's go ahead and run this.

[58:44] Anthony, just a quick note for you and the tutorial itself, maybe we should edit note

[58:52] to like my note or something so that it's obvious that it's like a user defined field

[58:57] kind of thing.

[58:58] But I think I'll just include an explanation that will make that clear.

[59:06] Okay.

[59:07] That ran.

[59:08] Okay.

[59:09] We got an error.

[59:10] Or what's this say?

[59:11] Okay.

[59:12] So yeah, we're getting a TLS error.

[59:18] I think there was a point where we were supposed to edit our client.

[59:24] Okay.

[59:25] Did we not get to that yet?

[59:30] I don't think.

[59:31] Well, it wasn't in the steps because I've been literally been going through here.

[59:36] So like we hit data contracts.

[59:39] Yeah, no, there was nothing about altering the client before retrieving the contract.

[59:46] The register contract work, this is just at the retrieve contract point now.

[59:53] I can scroll down a bit to see if it mentioned something about the client.

[59:57] No, no, that's a different, we're going to update the client with our document ID I think

[60:03] is.

[60:04] Okay.

[60:05] So I'm just going to paste this error in the private chat, if you...

[60:10] What it's just saying is that there is no output for the, we're running retrieve contract

[60:19] right now.

[60:20] Yeah.

[60:21] It's saying not permitted.

[60:22] I don't know why I'm not permitted, but, and then this is just a JavaScript error because

[60:31] obviously it returned, it can't read the JSON because there's nothing to read.

[60:37] So that's just a side effect error.

[60:40] Yeah.

[60:41] I've had issues with this, with that specific function in the past, so.

[60:46] Retrieve contract.

[60:47] Let's do what all great programmers do and just try it again.

[60:50] Yeah, that's what I'm doing.

[60:55] I'm burning a candle beside me, pouring one out.

[61:00] Cool.

[61:01] All right.

[61:02] So same thing, same error.

[61:05] So okay.

[61:06] Let's just get past this one because this doesn't really do anything.

[61:09] This is just to read back the contract that you created.

[61:11] So it's not really important and I've had issues with this in the past, so let's just

[61:16] go to update contract.

[61:21] Okay.

[61:26] And before we do this, okay.

[61:30] So we're going to get the contract schema, which is note.

[61:33] That's the free form JSON that we had in there in the contract to decide how we wanted the

[61:39] shape to be.

[61:42] And once we get that note, it looks like we're going to add an author property to enhance

[61:47] the contract and then the existing data contract.

[61:53] We're going to set the document schema to note again and okay.

[61:58] That's the document schema there and then it's just going to update it.

[62:02] So yeah.

[62:03] Okay.

[62:04] So literally just adding author field.

[62:06] So let's just copy that.

[62:09] And this is, I mean, this is blockchain stuff, but this is, I'm just reading JavaScript.

[62:13] This is like just crud stuff happening.

[62:15] That's a, even if you, even if you weren't doing blockchain, that's pretty straightforward.

[62:20] I think.

[62:21] Yeah.

[62:22] That's the whole point is that we want to make contract and blockchain decentralized

[62:28] app development as easy as developing a traditional app.

[62:34] Okay.

[62:35] So we've got the same TLS error now.

[62:39] Okay, interesting.

[62:45] So what I'm thinking when you had that, when you created the contract, we got the, the

[62:51] ID back, but then it was kind of hanging and you, you cut it off at the end.

[62:54] So I don't know if that may have messed anything up, but we go find the contract on the contract

[63:04] on the platform explorer.

[63:05] Uh, didn't look so let's, um, so the explorer, is it the same explorer, uh, this one?

[63:16] Yeah.

[63:17] So just go to, um, scroll to, or open up the hamburger and go to data contracts and then

[63:26] just append it to the end or actually it should be right there at the top.

[63:31] Not found.

[63:32] Okay.

[63:33] Sorry.

[63:34] No.

[63:35] Let me just put it in the URL.

[63:36] Oh, okay.

[63:37] Gotcha.

[63:38] I thought it was going to search for it.

[63:41] Okay.

[63:42] So it gives a 404.

[63:46] Okay.

[63:48] So that makes sense.

[63:49] So it check your URL check here's data contracts slash yeah, copy paste what you're doing.

[64:01] Right.

[64:02] I can't read any of your things, your, your URL is so fricking tiny.

[64:05] Yeah.

[64:06] That I can't zoom in here.

[64:07] Let me here.

[64:08] I'll do it here.

[64:09] I could use copy paste.

[64:10] What is in your URL right now?

[64:11] Yeah.

[64:12] Yeah.

[64:13] Yeah.

[64:14] I'll paste it in the chat.

[64:15] You can see it.

[64:17] Um, it's definitely 404ing.

[64:20] Um, okay.

[64:21] So that means the contract wasn't actually created.

[64:24] Okay.

[64:26] So we can run that again.

[64:27] So, so the problem was like, cause it was hanging for like a good five minutes.

[64:32] So even though it spit that out, it, it didn't necessarily, uh, maybe it hadn't finished.

[64:38] Maybe we need to try to create a contract again.

[64:41] Yeah.

[64:42] Let's do that.

[64:43] Okay.

[64:44] Uh, all right.

[64:46] And, and I'll just comment this out, uh, NPM run, create contract.

[64:55] Oh, whoops.

[64:57] Yeah.

[64:58] Not.

[64:59] Yeah.

[65:00] I see exactly what the issue is.

[65:01] Cause if you look at the code, it creates the contract at console logs, contract ID,

[65:05] and then it awaits, uh, contracts.publish, then it console logs contract registered.

[65:12] So we didn't wait for that part.

[65:13] We cut it off too soon.

[65:14] The contract ID, in other words, is not something that the chain gives you back.

[65:19] It's something that, that can be, um, client side derived.

[65:23] And so it can give you the contract back without actually having registered it.

[65:28] Okay.

[65:29] So to be clear, that was my bad, but it was hanging for like a good five minutes.

[65:35] So there's something on the network.

[65:36] Yeah.

[65:37] So it did it again.

[65:39] And it looks like.

[65:40] Oh yeah.

[65:41] Wait it out.

[65:42] Yeah.

[65:43] And it gives it.

[65:44] Go ahead.

[65:45] All right.

[65:46] Go ahead.

[65:47] I was just going to say, is it normal?

[65:48] It gives the same contract ID.

[65:50] Um, that's a good question.

[65:52] I don't know if it's, um, I don't know if these contract IDs are deterministically.

[65:58] If it's just hashing the whatever it shouldn't change, if it's just doing that, I'm not sure

[66:04] if it is.

[66:05] I'm not sure where that comes from, but I would guess it'd be like IPFS.

[66:09] You always get the same hash back for content doesn't change.

[66:14] Yeah, it would probably, it would probably give you a different one if you were registering

[66:20] the exact same document data, um, like schema, but from a different identity, I would guess

[66:29] it would be a different contract.

[66:32] If it wasn't, that would be a problem because then two people that wanted to create the

[66:36] exact same contract from different IDs would have the same contract and that would be a

[66:41] problem.

[66:42] Yeah.

[66:43] Yeah.

[66:44] Right.

[66:45] Um, so we'll, we'll let this run.

[66:46] I don't know how long it's going to take.

[66:47] Um, well, so we're getting close to the end of our, our time.

[66:52] Yeah.

[66:53] So, so basically, uh, we'll wait for the contract to get created.

[66:58] There's the retrieve contract just to show that it's there.

[67:01] And then, uh, then we up, then we're going to update it with the new author field.

[67:07] Um, that all seems pretty straightforward.

[67:09] I think, I think it's just, yeah, just waiting on the network.

[67:12] Uh, so it says here, if, um, you're updating existing contract, the identifier will stay

[67:16] the same, but version of the contract is incremented.

[67:19] Okay.

[67:20] That doesn't really answer the question that we had.

[67:23] So Michaela, if you're still listening, uh, we were, I was wondering if two completely

[67:28] separate people with completely separate, um, platform IDs try to create the exact same,

[67:35] um, con data contract, meaning it has a note and each note has a message, blah, blah, blah.

[67:42] And all of that schema data is the exact same.

[67:45] Would it have the same contract ID?

[67:47] Um, that's what I would guess would be different, but we'll, we'll see if Michaela has anything

[67:54] to say about that.

[67:55] By the way, that, uh, comment that just came up, that's the guy that made the platform

[67:58] Explorer.

[67:59] So if we have any, yeah, yeah, yeah, no, well, I think there's just the things that you're

[68:09] mentioning Anthony, like the, the, uh, the calculation for the total and the summary

[68:14] initially there, it was zero, even though there was, well, there was something going

[68:18] on with the totals from like when the, when it got topped up the identity there, um, that's

[68:27] the only thing I can think of, but cool.

[68:30] So if you're listening still, which you are, um, is it supposed to, like, does it usually

[68:36] take this long for you, um, when, when you're creating, what are we doing here?

[68:41] We're creating a contract, the, the, the sample with the note, we're coming up five minutes

[68:47] now, right?

[68:48] Things like the retrieve identity.

[68:49] We're also going really slow.

[68:50] So I think it might just be the network itself is just moving the speed today.

[68:54] Yeah.

[68:55] Um, but like we made a lot more progress than last time, obviously, uh, like this point,

[69:02] like I'm going to assume, like, once this finishes, uh, you know, I'll be able to retrieve

[69:07] the contract and then I'll be able to update it.

[69:09] And like, we can, like, I know we don't have a lot of time left, but we can just yet just

[69:13] show that again.

[69:14] So like, so if we go to register contract, like you were saying, Ryan, so this is where

[69:21] you define what your contract is going to have in terms of data.

[69:25] And so in our case, in the tutorial, we're just saying, we just want to note and it's,

[69:29] it's an object, uh, and then it's got these properties and this is the type we weren't

[69:34] sure what position was and additional properties, false.

[69:40] Does that, what does that mean exactly?

[69:43] Uh, because we updated the contract, well, we didn't do it yet, but we're adding author

[69:48] to it.

[69:49] So I'm curious what the additional properties to false means like, cause I would have thought

[69:53] reading that, that means that you can't change this contract.

[69:57] That's what it kind of reads like to me.

[69:59] Um, yeah, that, that's definitely not what it means, uh, go back to your client real

[70:04] quick, or this is, it sounds like this is an issue with, Oh, it came out, but real quick,

[70:11] I want to make sure we're on the same page here with, um, Mikhail go to your client and

[70:15] show the, the synchronization part.

[70:20] So this is, we have, so is this, um, skip synchronization before height?

[70:24] Yeah.

[70:25] So we've got that set.

[70:26] It's a different number, but it's still pretty close.

[70:28] Okay.

[70:29] Yeah.

[70:30] So that shouldn't be the reason that it's slow because we have done that.

[70:35] Um, coming back to this comment here, the execution of the SDK hangs because it syncs

[70:41] the transaction of the seed phrase from the first to the latest that I would guess, uh,

[70:48] you know, you can skip any amount of blocks to make it faster.

[70:51] I don't know exactly how to do that in this context, um, but, all right, we, we, it did

[71:00] finish.

[71:01] Um, yeah.

[71:02] And I'm just retrieving the contract.

[71:05] We should look at it on the platform explorer and then I want to just call it here.

[71:15] Is this it?

[71:16] Oh, there, here it is, okay.

[71:21] Still gives a 404 here.

[71:22] Hey, you should be able to just click the link in your terminal that it spit out.

[71:26] Okay.

[71:27] Yeah.

[71:28] Just click, just go straight to that.

[71:30] There you go.

[71:31] Oh, okay.

[71:32] Uh, uh, I don't know if it matters, but it's data contract here, but I think before it

[71:38] was data contracts in the explorer, but anyways, um, okay.

[71:42] So, uh, identifier, uh, so like, if we look, that's the contract there, the owner, this

[71:50] is my identity, uh, system.

[71:53] I'm assuming that false means that it's, it's from user land.

[71:57] It's not the, the network that created this contract.

[72:01] Cause I'm assuming there's probably network specific ones, uh, makes sense.

[72:07] I'm not sure about that, but I think that is, that is true.

[72:10] So like, for example, the name that we registered, uh, where you kind of registered that, that

[72:15] funny name, um, that itself is a contract.

[72:20] So that's one of those user, uh, or that's one of those core blessed, uh, contracts,

[72:28] I believe that it's called pay and registering a name to dash pay is, um, probably would

[72:37] be a system contract.

[72:38] So, okay.

[72:40] And we've got documents count is zero because we've created the contract, but nobody's actually

[72:44] created data with the contract yet.

[72:46] That's probably the next step in the tutorial is to create a document against that schema

[72:52] against that.

[72:53] Yep.

[72:54] And in terms of revision, this is what like Michelle was saying, uh, I ran it again.

[72:59] So it looks like it tried to create it a second time.

[73:01] So that's why there's one revision maybe.

[73:03] Okay, cool.

[73:05] Um, yeah.

[73:06] Okay.

[73:07] So let me just run the update contract real quick.

[73:09] Uh, I imagine it'll go pretty quickly cause the retrieve went quickly or maybe not, but,

[73:16] um, but yeah, I know we're wrapping up here.

[73:18] So I don't, I don't know if you wanted to take us out Ryan or Anthony, um, how far do

[73:24] we have left in the tutorial?

[73:26] Um, I mean, if we don't dally too much in the next one, we should be able to get through

[73:31] it in one more episode.

[73:33] We need to still, um, write to the contract and then create the whole backend and frontend

[73:39] with express and react.

[73:40] Oh, okay.

[73:41] So there's, there's plenty of stuff to do then let's, let's, let's cut it off here.

[73:45] We'll make a part C from this series if Nick's willing to come back again.

[73:50] Uh, yeah, no, I'm good saying it's, uh, like I said, I'm, it's just interesting exploring

[73:55] other technologies.

[73:57] So try to try to keep an open mind.

[73:59] I know, uh, like I said, I know there's a lot of people are, are not fans of blockchain

[74:04] right now, but not that I'm like an avid, like lover of it, but I think it's still worth

[74:09] it to explore these things.

[74:11] Like, I think it's, you know, and you've actually owned crypto before, which, which helps.

[74:16] Yeah, no, I do own crypto right now.

[74:20] So yeah.

[74:21] Um, cool.

[74:22] All right.

[74:23] So it did update the contract.

[74:24] It's at three 59, so we can just show that that happened.

[74:28] Uh, so this project, so that when we do our next one, we can go right where we were with

[74:35] the same dot EMV and everything.

[74:37] Yeah.

[74:38] Okay.

[74:39] Let's do that.

[74:40] Let's do, uh, uh, get, uh, yeah, I did, I believe, uh, hold on a sec.

[74:51] All right.

[74:52] Cool.

[74:53] Well, I guess we can take it out here.

[74:54] I think I took, yeah.

[74:55] I've got your getting Nori, but they're okay.

[74:57] Cool.

[74:58] Great.

[74:59] Uh, get in it.

[75:00] Uh, GA.

[75:01] Okay.

[75:02] All right.

[75:03] Cool.

[75:04] Yeah.

[75:05] I think we're good.

[75:06] Great.

[75:07] All right.

[75:08] Well, yeah.

[75:09] Thanks, Nick.

[75:10] And we will pick this up in a part C and hopefully get through.

[75:15] It's going to be a race from here on out, because we're, we've got some other people

[75:18] that are other developers that are going to come, come on and we'll see who has to go

[75:22] till G and who has to, who gets through it with just, uh, you know, Hey, yeah, I'm Friday.

[75:33] Yeah.

[75:34] I'm Friday.

[75:35] My buddy Noah is coming in to do this.

[75:36] Who's actually the person who got me working at a blockchain company in the first place.

[75:39] So he knows a lot about blockchain, so it'll be fun to have him on because he'll, he'll

[75:43] just blast blast through those hopefully.

[75:45] Yeah.

[75:46] Just in case that wasn't clear, definitely not Nick's fault that he's on C and then soon

[75:51] to be C on this series, definitely not Nick's fault.

[75:54] I'm just a C folks.

[75:56] Couldn't be an A. Sorry.

[75:57] Yeah.

[75:58] Those are the, these are the letter grades that you get after the end.

[76:01] Yeah.

[76:02] Yeah.

[76:03] All right.

[76:04] Uh, thanks everybody for watching, um, Anthony, you alluded to it, but we'll be on tomorrow

[76:09] to have another developer try this out, uh, for tomorrow.

[76:13] Right.

[76:14] Um, is that going to be Anthony?

[76:16] Oh, I'm in time zone land right now, so let's see.

[76:22] Um, I've got your, it's going to be 11, 10 o'clock, 10 o'clock your time.

[76:30] So that's, um, that's noon Eastern time, I believe.

[76:34] Um, okay.

[76:35] Something like that.

[76:36] Anyway.

[76:37] Um, yep.

[76:38] Tomorrow.

[76:39] Cool.

[76:40] Bye everybody.

[76:41] All right.