---
showLink: "https://www.youtube.com/watch?v=w0aGNYjGAe4"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash XDEFI Integration | Incubator WEEKLY"
publishDate: "2024-05-20"
coverImage: "https://i.ytimg.com/vi/w0aGNYjGAe4/sddefault.jpg?v=664b6645"
---

Mikhail provides updates on integrating Dash with xDefi wallet and recent improvements to the Dash Platform Explorer.

## Episode Summary

Mikhail is working on integrating Dash into the xDefi wallet's chain-sleep library, which will enable Dash support in xDefi and associated DeFi applications like Maya and Eldorado. He also demonstrates recent updates to the Dash Platform Explorer, including a redesigned homepage, asynchronous loading, and plans for adding validator information. The episode discusses the importance of supporting and retaining Dash developers.

## Chapters

00:00 - Introduction and xDefi Integration Overview

Mikhail explains the xDefi wallet and the process of integrating Dash support into its chain-sleep library. This will allow Dash to be used in xDefi and associated DeFi applications. The integration is straightforward and involves implementing Dash-specific methods in the library.

03:07 - xDefi Integration Details and Eldorado Example

The discussion delves into the specifics of the xDefi integration, including the different layers involved (wallet, SDK, and DeFi applications). Mikhail demonstrates how the integration will enable Dash support on platforms like Eldorado, making it more convenient for users. The next steps involve coding a pull request and waiting for the xDefi team to complete the integration on their end.

16:37 - Dash Platform Explorer Updates

Mikhail showcases recent improvements to the Dash Platform Explorer, including a redesigned homepage that displays real-time network status and trending data contracts. He also discusses plans for adding human-readable names for data contracts and validator information. The episode explores the technology stack behind the Explorer and potential optimizations using GroveDB.

26:14 - Closing Remarks and Dash Developer Support

The hosts discuss the importance of supporting and retaining Dash developers, acknowledging the challenges in finding qualified individuals to work on Dash and Dash Platform. They encourage the community to support developers through the proposal system and express their hope for attracting more talent to the ecosystem.

## Transcript

[00:00] Hey, how are you doing, just by the skin of your teeth.
[00:11] Yep.
[00:12] Yep.
[00:13] Yeah.
[00:14] Thanks for waiting for a couple minutes.
[00:15] Mikhail, good to have you on the show again today.
[00:19] I think it's been a few weeks, probably more than a month actually.
[00:23] Yeah.
[00:24] Yeah, how have things gone in the past month or so, just in general?
[00:31] It was good.
[00:34] There were a couple updates on the Platform Explorer.
[00:37] There was some work on the DashMate side, so ...
[00:44] Good, good, good.
[00:48] So Anthony, have you ever heard of the xDefi wallet?
[00:52] I have not, actually.
[00:54] I've looked at the website, though, since Mikhail mentioned it, and it looks pretty
[01:00] legit.
[01:01] Yep.
[01:02] So that's the topic of today's discussion, xDefi.
[01:05] I would personally like to hear some general updates from your side of the things, going
[01:12] into a little bit more detail of what you've been working on with the Platform Explorer,
[01:16] because I know that you had an update, and I wanted to show that if you have time at
[01:22] the end, but if not, that's okay as well.
[01:26] But let's go ahead and jump into the xDefi stuff.
[01:30] How did you get started with this, Mikhail, and what is xDefi?
[01:35] Yeah.
[01:36] Let me share my screen, I will show you.
[01:41] So basically, xDefi is a wallet that allows you to do some DeFi stuff, like there are
[01:52] some farming pools and stuff like that, basically an extension where you can buy some different
[02:03] chains and different coins, and also buy NFTs straight right away from your wallet.
[02:09] But it's basically missing support of Dash, for example, if you want to add some asset,
[02:28] there is no Dash.
[02:29] There is a Bitcoin, there is a Litecoin, but there is no Dash in there.
[02:36] And also this xDefi wallet is used, as I know, on the Maya protocol, on the Maya's frontend,
[02:45] so it also will allow you to use Dash right away through the xDefi wallet.
[02:58] So when you say wallet, do you mean, is it a browser extension?
[03:07] Yeah it's a browser extension, and yeah, and I don't have a link to the Maya frontend right
[03:18] now.
[03:19] If you have, you can send me in this Discord.
[03:24] Okay, yeah, I'll send you a link to Eldorado.
[03:29] Yeah, if you have, yes, I don't have it right away.
[03:36] So the general idea is to make an integration with Dash so that you will be able to keep
[03:42] Dash in the xDefi wallet to allow you to use some different decentralized applications
[03:53] and websites through the xDefi wallet, for example, like a Maya protocol.
[04:02] And yeah, there are some statistics on the xDefi wallet, on the volume that is happening
[04:08] through the xDefi, so it's quite, it's quite, it's quite a lot, I think.
[04:20] I don't really quite get these numbers because I just, I just do the code, I don't really
[04:26] understand everything, but yeah, there is a volume, there is amount, there is a community
[04:33] of the xDefi, which is pretty big, and it will be...
[04:39] I think we should mention that, was it, was it Joel that, that was asking you about this
[04:46] project?
[04:47] Yes, exactly, exactly, yeah, Joel connected me and the xDefi team so that we can do this
[04:54] integration, and before that, xDefi was a closed source product, but they started releasing
[05:04] some open source code, as a first step, they released a chain sleep library that just a
[05:13] collection of, it's like an SDK to connect to different blockchains, to throw some requests
[05:19] like get transactions, you can subscribe on some info, like transactions and UTXOs, and
[05:28] it supports a lot of chains, like this amount of chains, 30, 50, I don't know, yeah.
[05:41] So the general idea of the integration is that we can implement the dash in this library,
[05:48] in the chain sleep, and then the xDefi team will be able to implement dash on their side
[05:54] straight in the, in the, in the extension, sorry.
[06:00] Is the extension part not open source, or?
[06:03] Yes, not yet, it's not yet open source, so what we can do is just implement dash in chain
[06:11] sleep library, and then xDefi team will be able to implement dash on their side.
[06:17] Okay, so that sounds pretty straightforward, seeing how, my guess is that that's just giving
[06:24] some chain parameters for...
[06:27] Yeah, yes, so the chain sleep part is not that, not long, like it's pretty quick to
[06:35] implement.
[06:36] And do you have any idea, have you, have you been in contact with the xDefi guys personally,
[06:42] and are they into accepting this, and do you have any idea, I'm just curious, do you have
[06:48] any idea why it hasn't been supported so far, has it just been not a priority, or what was
[06:55] your impression?
[06:56] Yeah, I think that it wasn't just a priority, there wasn't such task, so, and the other
[07:03] part that the chain sleep was closed source, and I don't know, but, but yeah, I contacted,
[07:11] I contacted with team, caught up with them, and they're pretty active, so we're in touch
[07:21] with the devs and other guys, so, so yeah, should be pretty, pretty, pretty good.
[07:32] Yeah, so, another good thing is that they have a documentation where we can also get
[07:41] listed, as I remember, I think that was the, the different...
[07:56] You're looking for the, the process of, of getting accepted as a newly listed client?
[08:05] One second, I'll show you, so there is a dev docs, yeah, that would be good to, to get
[08:19] listed in there, so whether we, there is a dev documentation of Xdify, where the integration
[08:27] listed like for different coins, so when the developers is going to integrate Xdify on
[08:34] their website, they get to this documentation, they can see there are different chains, so
[08:40] we can also add a dash in there, so that will also increase the presence of the dash, so
[08:47] it's in different sections, for example, in mobile and others, so yeah.
[08:55] A question regarding that, so is it, is it the case that Xdify will eventually support
[09:05] Dash, but then the different, the different products have to enable it as a coin that's
[09:14] supported on their sites, like for example, Eldorado's Xdify integration, would Eldorado
[09:20] have to do anything in particular to start supporting Dash, or does it just, is the way
[09:29] that it's coded up, do all the integrations automatically populate on all the front ends
[09:35] that support the Xdify wallet automatically?
[09:40] It should be coded up automatically, yeah, so this documentation is about different parts,
[09:48] like some specific, chain specific things, yeah, so stuff like that.
[10:03] So the My part shouldn't take that long, like maybe a week or so, or maybe even less, so
[10:11] let's hope that Xdify team will also do this pretty quickly.
[10:16] Yeah, I mean my experience with Xdify so far is through the Maya ecosystem, and my overall
[10:26] impression is that Xdify is pretty much everywhere, and so there are a lot of integrations that
[10:33] this would enable, so if the Xdify team is watching, I'm very excited about this integration
[10:41] and hope that we can get this going as soon as possible, and you know, whatever the process
[10:46] is, we're happy to do whatever we need to, to get that, to get that in as soon as possible,
[10:53] so it seems like a great product, and thanks for taking that on.
[11:02] What other questions do you have, Anthony, about this so far, as I know you haven't used
[11:10] the product much, but any questions so far on that?
[11:15] I guess I'm just curious, like where is the entry point for Dash, because it looks like
[11:22] there's chains and there's wallets and there's, so I'm just kind of curious about the different
[11:29] layers and where it is exactly that we're integrating.
[11:34] So we're integrating Dash in their SDK, which allows you to query and construct, sign, and
[11:43] broadcast transactions in different chains, so there are like a lot of chains, but there
[11:49] are no support for Dash, so we implement Dash in their library, and then they will be able
[11:57] to take it into their, they will be able to integrate Dash in their wallet extension and
[12:04] other parts.
[12:05] And then once that happens, is it something where you could basically swap it for anything
[12:09] that is supported on the DeFi wallet, or are there specific integrations that you need?
[12:16] Is that, like, you will be able to access different XDeFi features, like any, which
[12:25] is on their application?
[12:28] So I sent a link to Eldorado, it's the one that comes to mind first, do you want to pop
[12:34] that open, Mikhail, just so Anthony and anybody can see?
[12:39] I can see, where did you send it?
[12:42] You just type in Eldorado.market as the URL.
[12:46] Yep, and that way people can get an idea, because these, you know, the layers get a
[12:53] little confusing if you're not doing this every day.
[12:57] It gets a little confusing about, especially cross-chain.
[13:02] So there are several different layers, the first thing is XDeFi is a wallet, and that
[13:09] just means that it has key pairs that are supported, and they can generate keys, they
[13:17] can generate, they can sign transactions, things like that.
[13:21] But then when you integrate it into something like Eldorado, which is used to swap from
[13:27] chain to coin, one coin to another coin, or chain to another chain, that's a further integration.
[13:35] So when you go to a site like this, I'll just narrate as you're doing this, when you connect
[13:41] a wallet, you know, there are different options for connecting a wallet, and most of these
[13:45] are browser extensions, but there are also like key stores, which would be like the most
[13:52] plain vanilla way to connect to Eldorado.
[13:56] But you see up at the top there, there's the XDeFi wallet.
[13:59] So if you click that, what do you see?
[14:02] It shows a little grayed out Dash logo, which to me means that Eldorado supports Dash, but
[14:12] XDeFi does not.
[14:14] So that's what we're trying to fix right there.
[14:18] Yeah, so basically if you want to use Dash on the Eldorado front-end, you have to use
[14:26] the key store, which is not that convenient.
[14:30] While there is the XDeFi wallet, that will be much more better, much more convenient
[14:36] to use.
[14:37] Yeah.
[14:38] Okay, so that gives you an idea.
[14:42] I don't know what other integrations right now, I know Joel was pushing this for a variety
[14:47] of reasons, not just Eldorado obviously, but if Joel, if you're listening, let us know
[14:55] what other examples you might have of integrations.
[15:03] So what's the process ahead of you in terms of what you need to do to get this, other
[15:07] than you just need to code up a pull request into that GitHub repository?
[15:15] Have they given you any insights as to other things that you need to do, or is it just
[15:23] a matter of coding and waiting?
[15:25] No.
[15:26] They said that they only wait for the Chainsleep implementation, and they will be able to hop
[15:33] on to the integration.
[15:35] So that's the only thing they wait from us.
[15:39] So it's pretty straightforward.
[15:40] In the Chainsleep, there are different packages, like Bitcoin Core, so all we have to do is
[15:47] just make a dash package, which will implement some, you know, like blockchain API or inside
[15:58] API.
[15:59] So we just need to make some methods, implement some methods, which will be pretty quickly,
[16:06] I think, through the blockchain API.
[16:10] So yeah, that's the only thing that we need to do.
[16:15] Okay, well, anything else to say about that then before we shift over to something else?
[16:22] Mikhail?
[16:23] No, not from our side.
[16:27] Okay.
[16:28] Do you want to show us the latest updates on your floor or anything else?
[16:37] So last few weeks we were working on the homepage, and it was redesigned, but there were a lot
[16:49] of changes.
[16:50] Like, first of all, all of the information of the platform state is now on the main page,
[16:57] and we can see that the network right now is functioning okay.
[17:04] And if there are no blocks in more like 15 minutes, it will be yellow and will show the
[17:11] chain propagation is degraded, and that means that something is happening, something is
[17:17] not okay in the network.
[17:18] So basically, when people were visiting the platform server, they want to see whether
[17:28] the chain is working or not, so it's very important.
[17:32] Yeah.
[17:33] So right now it does appear to be working.
[17:34] I see a flat line from May 16th through today.
[17:40] Was that just because there were no transactions?
[17:42] I did see that platform down, so I was...
[17:45] Well, nobody was testing the chain because it was the weekend, so it was flat.
[17:56] Okay.
[17:57] So actually, yeah, I do have a question about that then, because I did see chatter about
[18:00] platform being down.
[18:04] Does your Explorer show historically when the chain has been down versus just not being
[18:11] used?
[18:12] I know that when this goes to main net, it will probably be obvious because there will
[18:15] be more activity, but...
[18:17] Actually, no.
[18:18] I only have the history of the blocks.
[18:23] So the chain was down for some infrastructure reasons.
[18:27] The first time it was stopped because of the free disk space was...
[18:35] So the first reason was the disk space, and the second, I don't know what was the reason,
[18:43] but I don't think that I'm able to determine whether the chain is down or just stopped
[18:50] or paused.
[18:51] So I think it's just showing as it is.
[18:55] Yeah.
[18:56] Also, we have added some lists, some trending lists of some data contracts and identities.
[19:04] We made it like that.
[19:07] Maybe later, when we have some popular data contracts, like for example, DPNS, Dash Money
[19:17] applications, I think we can also list it somewhere here, so that users will be able
[19:24] to look at the main page and get to it straight away.
[19:30] Is there something on a contract that says a human readable name of any sort rather than
[19:37] just the identifier?
[19:38] Because I'm looking at this trending data contracts, and I see a bunch of identifiers
[19:42] with a bunch of documents for each.
[19:45] Yeah.
[19:46] It will be the next feature of the Platform Explorer.
[19:48] So the feature will allow developers to register a name for their data contract.
[20:05] It will be implemented as a separate Platform Explorer data contract, which will hold the
[20:11] names of the data contracts associated to the given data contract.
[20:18] The owner, for example, can verify their data contract on the Platform Explorer and set
[20:25] a name for this data contract.
[20:29] So for example, the Dash Pay data contract developed by Dash Core Group, that could be
[20:37] listed as a name, and that will be a data contract itself, listing those names.
[20:47] Are those unique names?
[20:49] Yeah, it will look similarly, like the contracts get verified and approved in the Ethereum.
[21:00] If you are the owner of the data contract, you will be able to submit the document in
[21:11] the Platform Explorer data contract with the name of your data contract in the Explorer,
[21:16] so that the Platform Explorer will be able to catch this document that was submitted
[21:22] by the developer, and it will verify that the document was sent by the owner of the
[21:29] data contract.
[21:31] And if so, then it will add a name for this data contract in the Platform Explorer database.
[21:38] So basically, it's like a way for developers to make a custom name for data contracts on
[21:52] the Platform Explorer site, like through the chain, you know?
[21:56] All right.
[22:00] Anything else to say about the Platform Explorer, or is there anything in addition to that that
[22:07] you want to add?
[22:09] Yeah.
[22:10] So what we've also done is we made an asynchronous request, so when we load the page, all the
[22:17] sections get loaded independently.
[22:21] We plan to extend it on every page on the Platform Explorer.
[22:26] For example, right here, we don't have asynchronous loading.
[22:33] And the next feature will be the validators.
[22:37] So there will be a separate page where you can see the validators in the platform chain
[22:44] and whether they're active or, you know, and stuff like that.
[22:51] Validators for the platform chain, and that is a subset of the masternodes.
[22:55] Yes.
[22:56] Yes.
[22:57] Yes.
[22:58] Basically, the same.
[22:59] The masternodes, the HPMNs, and yeah, they will be listed on the website and we can see
[23:06] the statistics for the validators and stuff like that.
[23:12] Yep.
[23:13] Okay.
[23:14] Just curious, what's the technology stack for the website itself, the Platform Explorer?
[23:20] Next.js on the front end, on the back end, it's Node.js with PostgreSQL.
[23:32] And also the Rust for the indexers part, which indexes the blockchain.
[23:39] So Rust, Node.js, and JavaScript.
[23:44] Rust indexes the blockchain.
[23:46] Is that something that you wrote or is that something that somebody else wrote?
[23:49] Yeah.
[23:50] Yeah.
[23:51] It's the MyPark, which basically scans every block in the platform chain and just indexes
[24:02] that in the traditional database like SQL.
[24:07] And have you thought about, I know it's a little bit too meta and probably too early
[24:11] to do this, but have you thought about doing your, instead of using a SQL database to actually
[24:18] have the metadata for this site beyond platform?
[24:21] Sorry, what you mean?
[24:25] So you have an indexer, the Rust indexer that scans the blockchain, and then you're popping,
[24:32] you're putting data into, you're populating data into a database, a SQL database.
[24:39] Have you considered populating that data into a platform contract itself?
[24:44] I know that's probably not a reliable thing to do right now, but.
[24:49] Well, I think that will be working that way.
[24:52] I think that will be pretty heavy.
[24:58] So it's just, will not be working like that for the users.
[25:03] Right.
[25:04] Yeah.
[25:05] And so if platform is down, you wouldn't be able to see any of the data on your site,
[25:09] obviously.
[25:10] Yeah.
[25:11] I talked with Sam recently, and he said that we could possibly use the GoDB to query data
[25:19] so that we can avoid the indexer part.
[25:23] But that's something that should be researched because I don't have all the picture of how
[25:31] GoDB working.
[25:32] There are not much documentations out there that will, how to use it, but I will do research
[25:39] and probably it will be better because indexer part.
[25:43] Yeah.
[25:44] That would be interesting because GroveDB is the database that powers Dash platform,
[25:51] but you don't need to use it.
[25:54] You can use GroveDB independently as a standalone database.
[25:58] Yeah.
[25:59] It'll be interesting to see, you know, a centralized version of GroveDB operating.
[26:04] So yeah, interesting.
[26:06] All right.
[26:07] Anything else to say about the Explorer or I did want to ask just your general strategy
[26:14] going forward.
[26:16] One specific question is how is it going with expanding or maintaining a team besides yourself?
[26:26] Are you, do you have other developers that you're working with that are doing work?
[26:32] How many and what are your plans going forward as far as like expanding your team itself?
[26:38] Yeah.
[26:40] So I'm working full time.
[26:44] Also there is Alexei, which helps me on the platform Explorer side.
[26:51] I'm seeking for one or two guys right now, but haven't chosen yet.
[27:00] So I'm looking for someone, maybe one full time or maybe a few part time guys.
[27:11] Okay, cool.
[27:13] Any questions, Anthony, or should we start wrapping up?
[27:17] I mean, it looks great.
[27:19] Just want to say good job on the front page.
[27:21] It looks very clean.
[27:24] Cool.
[27:25] Thanks.
[27:26] All right, Mikhail, final closing words.
[27:30] I don't know.
[27:33] Let's keep it going.
[27:34] A little bit of a shorter discussion today.
[27:36] Sorry?
[27:37] Yeah, it was just, we're at 27 minutes now, so we can, we can close it out now.
[27:45] But if you wanted to talk about anything else, we have some time.
[27:48] Yeah, I think it's okay.
[27:50] I know.
[27:51] Okay.
[27:52] All right, guys, with that, then there are a couple of days.
[27:55] I think just over one day left of voting in the cycle.
[27:59] So everybody, please take a look at those proposals.
[28:03] There are a few that have not been funded yet, including not incubator proposals, which
[28:10] you know, it's, I think it's difficult.
[28:13] One of the reasons why I asked you that question at the end, just your general team building
[28:18] and who you're working with is, I don't know if people understand how difficult it is to
[28:26] find a qualified person to develop in Dash and Dash platform.
[28:34] Feel free to say anything more about that, but the people that we have, like Dash Money,
[28:39] for example, was not funded last quarter or last month in this quarter, but I'm hoping
[28:45] to see him funded.
[28:48] And then there was a new developer, Paulinus, or something like that.
[28:54] I invited them both to be on the show.
[28:57] So that invitation is longstanding because I want people to see inside what they're working
[29:04] on, what their challenges are, because I think that, yeah, until we have more developers
[29:12] actually doing this, it's tough to say whether their proposals are overpriced or underpriced.
[29:21] So I would just encourage everybody to support those developers that are actually trying
[29:27] to do the work on here.
[29:29] And yeah, the more developers we can get, the better.
[29:33] But up until now, I'd like to retain the ones that we have.
[29:37] So that's my closing remarks, and if anybody else doesn't have anything else to add to
[29:43] that, then we'll say see you later until next week.
[29:48] And yeah.
[29:49] >> All right.
[29:50] Catch you next week.
[29:52] >> Bye.
