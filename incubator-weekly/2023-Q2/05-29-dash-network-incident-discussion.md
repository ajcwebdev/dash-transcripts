---
showLink: "https://www.youtube.com/watch?v=J2MiS5uiuG4"
slug: "dash-network-incident-discussion"
title: "Discussion of Dash’s Recent Network Incident"
publishDate: "2023-05-29"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/J2MiS5uiuG4/maxresdefault.webp"
---

Dash network experienced a 16-hour chain halt due to a bug in the BLS signature code during a hard fork to version 19.

## Episode Summary

tl;dr: The Dash network recently experienced a chain halt for approximately 16 hours following a hard fork to version 19. The issue was caused by a bug in the BLS signature code that resulted in nodes crashing when trying to obtain the masternode list. While a small chain continued producing blocks, it was not accepted by the majority of the network. The incident raised questions about Dash's proof-of-work vs. proof-of-stake nature and the control dynamics between miners and masternodes. A fix is being developed and tested, with plans for a mandatory upgrade to version 19.2 before activation in June.

## Chapters

00:00 - Introduction and Background on the Dash Network Incident
The episode begins with a discussion of the recent Dash network incident, where the network experienced a 16-hour chain halt following a hard fork to version 19.

06:05 - Description of the Network Incident and Its Causes
Rion and Mikhail provide a detailed description of what happened during the network incident, including the bug in the BLS signature code that caused nodes to crash and the presence of a small chain that continued producing blocks.

22:40 - Examination of Dash's Consensus Mechanism and Control Dynamics
The hosts discuss the implications of the incident on Dash's proof-of-work vs. proof-of-stake nature and the control dynamics between miners and masternodes, questioning the network's Byzantine fault tolerance.

41:05 - Dash Core Group's Response and Plans for Resolution
The discussion moves to Dash Core Group's blog post addressing the incident and their plans for a fix, which involves a mandatory upgrade to version 19.2 before activation in June.

53:08 - Reflections on the Impact of the Incident on Dash's Identity and Future
Amanda and Rion share their thoughts on how the incident has affected Dash's identity as a reliable payment network and the importance of finding a resolution to prevent similar occurrences in the future.

## Transcript

[00:00] What is the Bank for International Settlements? Well, I always say it's the most important bank in the world that you've probably never heard of.
[00:08] I think the best way to think about them is a bank for central banks. The central bank of central banks, exactly.
[00:13] You know, most people think about the financial system and they just think about, you know, the Federal Reserve, U.S. Treasury,
[00:19] and that's where they think it stops. But we live in a very globalized world,
[00:23] and there's these organizations that are filled with unelected, you know, they're non-governmental.
[00:29] Like, I didn't vote for anybody at the biz, but they work in the stratosphere, like above everything else.
[00:35] Historian Carol Quigley wrote in his epic book, Tragedy and Hope, the Bank for International Settlements was part of a plan to, quote,
[00:42] "create a world system of financial control in private hands, able to dominate the political system of each country
[00:49] and the economy of the world as a whole, to be controlled in a feudalistic fashion by the central banks of the world,
[00:55] acting in concert by secret agreements." The real reason it was set up was so that central bankers,
[01:02] i.e. the governors of national banks like the Bank of France, the Bank of England, and the Federal Reserve and so on,
[01:08] could have a place to meet that was supremely protected and legally inviolable. Every two months, the BIS organizes a meeting weekend,
[01:18] and today, all of the central bank governors who are members of the BIS are attending. The main purpose of BIS meetings is to build consensus
[01:30] among central banks and supervisory authorities. And so there's 63 member banks, which make up 95% of GDP.
[01:38] I picture like an octopus. I know it sounds funny, but who has tentacles, who just moves everything around to these central banks and above them.
[01:46] I had an org chart of the way I see the world, and on the org chart, the BIS sits at the top.
[01:51] Below the BIS, then you have some of these think tanks. So the World Economic Forum is one of them, the Club of Rome.
[02:00] And so they're the policy makers. And then they push it down to the next row in the org chart
[02:05] to the policy enforcers, which are the governments. They are a bank beyond the reach of any national or international law,
[02:14] and it's because they are set up under international treaty. Have you ever thought much about, say, digital currencies
[02:21] or the impact of negative interest rates on the economy? Well, these are just some of the topics that are discussed here.
[02:29] In 1947, basically there was an agreement made between central banks that they wouldn't transact between each other directly.
[02:44] They would work through the BIS. The thing about the BIS is that they're focused on improving
[02:52] the transaction capabilities of international finance. So when the BIS looks at the CBDC, they're like, "This is finally it."
[03:01] The rise of crypto over the last several years has been a remarkable spectacle.
[03:06] It highlights the place of technology in the popular imagination and its galvanizing role in debates on the shape of things to come.
[03:15] So in this respect, crypto offers a tantalizing glimpse of new arrangements and technical features.
[03:23] But as we argue in the chapter, everything that can be done with crypto can be done also with central bank money.
[03:31] This is Augustin Karstens. He's the head of the Bank of International Settlement.
[03:35] My main message today is simple. The soul of money belongs neither to a big tech nor to an anonymous ledger.
[03:41] The soul of money is trust. And central banks have been and continue to be
[03:46] the institution's best place to provide trust in the digital age. While potentially hundreds of millions of people
[03:51] are on the brink of starvation around the world right now, the direct result of the monetary policy from central banks all around the globe,
[03:58] he's sitting here telling us central banks are the only people we can trust while using a money printer as a background.
[04:05] Our vision for the future monetary system, as laid out in chapter 3, is the fusion of enhanced technical capabilities
[04:13] around the core of the trust provided by central bank money. You know, CBDCs don't really work
[04:23] unless everyone's on kind of a digital ID system. It's kind of like a precursor.
[04:30] We don't know, for example, who's using a $100 bill today. We don't know who is using a $1,000 bill today.
[04:38] A key difference with the CBDC is that central banks will have absolute control
[04:46] on the rules and regulations that will determine the use of that expression of central bank liability.
[04:54] And also, we will have the technology to enforce that. And so I can see the direction we're heading,
[05:00] and I'm certainly going to make sure I keep as much wealth in the traditional financial system as possible.
[05:06] I don't think the path forward is to, like, win over the regulators. We have here unstoppable financial systems that are uncensorable.
[05:15] We should be relying on that. There are just too many opportunities
[05:20] for people to embrace technology in this way that flips the script. Crypto is a great equalizer, right?
[05:29] If you fix money, you allow the world to heal. And we have lived in a world of sick money for many decades.
[05:38] Legacy banks, legacy financial institutions, writing's on the wall, and we'll see kind of how it plays out.
[05:44] Yeah, yeah, they're in trouble. And I'm so inspired, really, by all the awesome entrepreneurs
[05:49] in this industry that are building this stuff. I'm proud to be part of it.
[05:55] [Incubator Weekly] Hello, hello, everybody.
[06:05] Welcome to a somewhat different episode of Incubator Weekly. I'm joined, as usual, by my co-host, Rion.
[06:14] Hi, Rion. Hello.
[06:16] Lead strategist at the Incubator, and also joined by a developer at Dash Incubator, Mikhail.
[06:23] How are you today, Mikhail? Joining us from Siberia, which I will never tire of saying,
[06:30] as it is just about like saying joining us from the moon, in my point of view.
[06:35] So the reason that things are a little different today is because we are not going to talk about a particular concept
[06:42] or project within the Incubator today, but rather we are going to discuss,
[06:48] ideally with input from viewers as well, what I'm calling the network incident of exactly one week ago.
[06:57] So there's not even an exact agreement on what to call it. Like just before the show began, Rion was saying,
[07:07] you know, do we call it a stall or do we call it an incident? And really that brings up the very crux of the reason for this show today,
[07:17] which is to discuss the lack of consensus rather around what happened. So I guess I had said that I was going to lead us off with sort of my view,
[07:33] but now that I think about it, I think it's actually better that you start us off a bit, Rion,
[07:39] with just more or less kind of what happened. And then Mikhail will chime in with the same.
[07:46] And then we're just going to start getting into our different viewpoints. Some of us are more sure than others of what happened.
[07:54] And others of us have questions that others think are irrelevant. So, Rion, will you please get us kicked off
[08:01] and then we'll move in that direction. Yeah, sure.
[08:07] Part of the point of what I wanted to discuss today was that we still don't know exactly what happened.
[08:17] And I know that I had several conversations in Discord with some people. I know you did too, Amanda, and we did discuss it a little bit.
[08:27] And a little bit, some people might think we discussed it a lot and so much that it's actually a boring topic at this point.
[08:35] But I want to push back on that because this was a big thing that happened. And I think that we need to fully understand it
[08:46] to the point where we're pretty sure that it's not going to happen again. And not only that, but I want to understand it
[08:55] in not only what happened in that sense, but also what it implies about whether Dash is a proof-of-work network
[09:05] or whether it's a proof-of-stake network or even whether it might be just simply a proof-of-authority network
[09:13] with extra steps. I tweeted about this, that is this a Rube Goldberg machine
[09:22] that basically is just we trust DCG-CoreGroup in whatever they're doing. And that's an extreme interpretation, obviously.
[09:34] But I want to at least go down that path and say, explore what that might mean.
[09:41] So my understanding of what happened is basically we had a hard fork to version 19.
[09:52] And the hard fork happens in phases where there's a certain lock-in phase and there's an activation block.
[10:00] And the lock-in phase happened, which triggers the activation block. And at the activation block, that's when certain if clauses,
[10:10] for example, in the code trigger and say, now that we're at this block, have these other rules
[10:18] and enforce these other consensus rules. And so when that happened, I don't know what blocks we're at,
[10:26] 1 million, da-da-da, 880 or something like that, the network or at least a part of the majority of the network stalled.
[10:38] And in further discussions in Discord, that was explained as the nodes actually crashed
[10:50] or at least a lot of the nodes crashed and therefore couldn't really do anything, let alone produce blocks.
[10:58] So I'm actually not 100% sure if that was the case or whether these got restarted
[11:05] or perhaps Mikhail will help us with that a little bit. But then there was also a small chain that actually did progress.
[11:17] And that chain that did progress, they were mining blocks and running on version 19.
[11:28] I did ask, and I think I got an answer, and I'm pretty sure it was version 19.0.0.
[11:34] But yes, so one of the version 19s. And I was told that that chain was like a "ghost chain"
[11:44] and it was producing blocks that weren't viable and things like that. And those are kind of descriptions,
[11:51] but they don't really tell me enough of the story about that's not descriptive enough to me.
[11:58] So maybe we could turn just as I see Mikhail's video. He's a little fish circling a pond, I guess, right now.
[12:11] Mikhail, can you join us via audio only? Or I could kind of go into, I could share my screen
[12:19] and kind of go through somewhat chronologically what I saw on forum posts and things like that.
[12:26] Yep, that's fine. Or, you know, you can jump in any time, Amanda,
[12:30] with your interpretation of what happened. But feel free to share my screen at this point
[12:36] and we can just kind of discuss what some of the other, it looks like Mikhail is back.
[12:43] Yeah, so before, I guess, I too am interested to hear Mikhail weigh in if his Siberian internet can get cleared up.
[12:54] I have total empathy for that, as I myself have had internet troubles lately as well.
[13:00] But the questions that I would like to talk about are similar to yours, Rion.
[13:11] And I think that I will just bring them up as we progress through your slides.
[13:16] So let us go ahead and have a look at that now. Yeah, so my slides meaning just a series of Chrome tabs, basically.
[13:27] So yeah, there was a forum post that described a skeptical view of what happened.
[13:34] And I want to give some voice to that forum post. Grandmaster Dash, Masternode owner and operator,
[13:42] so a well-known member. He says, "Until now, Dash could proudly say,
[13:47] not only is it an OG, but operated 24/7 without any downtime. No chain halts ever.
[13:54] Thanks, DCG, for taking away that from Dash." So clearly a very critical take.
[14:01] But it is one that I kind of sympathize with. We are all in this together.
[14:07] And although it looks like the market has not really reacted too poorly to this so far,
[14:14] this might be something that comes back and back and back again, similar to the whole Instamine thing,
[14:22] where eventually Tao Satoshi made a video that basically kind of set the record straight.
[14:30] And I think that perhaps we might want to have both a text version and a video version that sets this record straight,
[14:41] a very clear way that says this is actually what happened. This is why it won't happen again,
[14:47] or this is why we feel like we're safe moving forward. But this is like second page of that same forum post.
[14:57] So these next three will be the same forum post, but just different parts of them.
[15:03] So Agnepickin says, "It was not 4K Masternodes that caused the chain halt." Stop spreading misinformation because it was the BLS signatures.
[15:14] I see some head nodding from Mikhail. Mikhail, do you care to weigh in at this point?
[15:19] Yeah, yeah. So basically the issue was in the BLS signatures.
[15:29] And the BLS signatures are the new standard in the cryptocurrency industry. And with the v19 fork, we were switching to the new version of the BLS signature
[15:47] because there was a new – at the time when Dash first introduced the BLS signature in the network, there was no quite standard in the industry.
[16:02] But as the years go, so now there is a new BLS signature standard and there was immigration.
[16:14] And during this immigration, there was one bug that – basically when the node was trying to get the Masternode list for the block,
[16:28] it was using the legacy signature to obtain the Masternodes. That's one of the things I've heard, but what is it getting the list for?
[16:42] And you're talking about each instance of the Dash D software, the C++ code running on both Masternodes, mining nodes, even merchant nodes,
[16:54] all the nodes running Dash D to check the state of the network. That's what you're talking about when you say the network.
[17:03] And what stage is it trying to get a list of Masternodes? What is it doing at that point?
[17:12] When the v19 hard fork happened, the nodes that were trying to get the Masternode list diff, basically the Masternode list is just the list
[17:28] of all Masternodes when you're updating your Masternode or removing or adding a new one, the Masternode list gets updated.
[17:37] And when the node was trying to get the new Masternode list diff after the v19 fork, it was trying to get those entries allocated
[17:53] in the HashMap, and to query this HashMap, the Masternode key was used. And at this point, the legacy scheme was used to obtain these entries.
[18:09] But the Masternode owners were already migrated to the BLSV2, and obviously couldn't find the Masternodes, and that was leading to crash.
[18:20] There was also the part of non-determinism in this issue. So some nodes were crashing, some were not.
[18:32] And even if you crash and re-index, you could probably regain the health. But the blocks weren't accepted by the network,
[18:44] such blocks that were purchased by the re-index nodes. Can we stop here and maybe talk about a few of the terms
[18:50] that you've mentioned so far, Mikhail? So the first one, I'll just bring the elementary viewpoint here.
[18:58] That's the only viewpoint I have. First of all, is there such a thing as a blockchain
[19:06] without a daemon, or -d in this case? Or is there such a thing as a --
[19:11] When we say blockchains and daemons, are these absolutely inseparable from each other?
[19:18] The reason I ask this is because if we say stuff like, oh, in blockchain we trust, or the blockchain is a trust machine,
[19:27] a Byzantine -- getting around the Byzantine generals problem, is there an implied subtext that says,
[19:36] if the daemon doesn't act randomly that day? Well, I'll take a stab at that.
[19:43] So the so-called daemon, which is the D after the dash term. So you see a binary, which is, for all intents and purposes,
[19:53] just the computer code that your computer runs. It's called -d, and the D stands for daemon.
[20:00] Dash didn't invent this, right? There's a Bitcoin D. This is not even cryptocurrency.
[20:05] Any program that's intended to run kind of in the background continuously is referred to as a daemon.
[20:12] So this is what -d is doing. It's contrasted with something like -cli,
[20:19] which is the client that contacts the daemon and says, hey, you're running all the time.
[20:25] You know the state of everything. Tell me what the state of the blockchain is.
[20:30] What's the latest block? What's the best block? What's the longest chain? Those kind of things.
[20:37] And so I would say blockchain, in its most technical sense, is a data structure that represents the chain,
[20:49] which is more or less, like I said, it's a database. So they're separate in that way, in that they're just different things,
[21:01] but they are connected in the sense that the blockchain, the daemon, is what is supposed to represent, or at least know,
[21:11] what the current blockchain state is. So that would be my explanation.
[21:18] So then, Mikhail, can a blockchain run without a daemon? I guess I'm just wondering, why am I hearing our blockchain got crashed
[21:25] because daemon? Like, what the hell good is a blockchain if it can be taken down by a daemon, I guess?
[21:31] And I want to add one other thing to that, and you mentioned the term Byzantine fault tolerant.
[21:37] Byzantine fault tolerant is a fancy term that's supposed to mean if there are adverse environments, this thing still runs.
[21:49] It's fault tolerant in the sense, and Byzantine basically just means bad environment.
[21:54] Either somebody's attacking you, or you have certain amount of nodes on your network that just fall over
[22:01] and crash due to memory crashes or whatever. That's Byzantine.
[22:05] It means bad people, whether intentional or not. It's supposed to be Byzantine fault tolerant,
[22:12] which means even if there are bad guys or bad nodes on the network, it's supposed to be tolerant to that.
[22:19] But the question becomes, what happens when all of the nodes on the network are faulty because of a bug that's written in the code?
[22:29] Well, is it fault tolerant at that point? And I guess, let me just let Mikhail jump in with what he had to say
[22:36] because it looked like he did have something to say there. Please.
[22:40] Well, according to the BFT, if all nodes are down or in default state, the data will be stopped.
[22:49] It will just become stalled. So until, for the BFT, as I remember,
[22:56] like 30% of nodes should be alive or stuff like that. So according to the incident, yes, the daemons that were running,
[23:11] just follow the people, that's just why this was happening. And like you can predict everything.
[23:24] The v19 fork was like the big step for the platform that was needed for the platform, for the platform stuff that we were waiting for for long.
[23:39] The network, we were kind of waiting for it so much that the DCG was really trying hard to make it live.
[23:53] And obviously we, like, everyone makes, like, there will be always the bugs. Always will be the bugs that probably it could be looked better,
[24:08] tested better, but at the same time, even in the testnet, in the devnets that we have to test functionalities.
[24:19] Sometimes it does not have the exact representation of the mainnet because in the testnet, we all have the same kind of software.
[24:29] We have predefined conditions and you can catch all the cases. There could be cases that you can catch only in production.
[24:43] I have another question about that, Mikhail. Is it true that in a specific Dash core group used to have sports
[24:53] that would enable a few of their members to, I guess, unhard fork a situation if it had ever happened like this, but that more recent versions of the code
[25:07] coming from Dash core group have removed those sports? And so that's kind of why this happened the way it did.
[25:15] Like, old Dash would have been able to, hey, let's just, like, spork back out of this, but current Dash is like, no,
[25:21] the whole network needs to have a new version now to get out of this. Yeah, there is a sporks and probably such spork could be implemented
[25:34] that will revert the hard fork, but you can't just predict all the cases. Like, even if we had the sporks, you would possibly run into another situation,
[25:50] another thing that-- For which there was not a spork.
[25:54] Yes, and the last signatures have nothing to do with the sporks. Like, even if we had the spork, it would still crash.
[26:08] Well, let's talk about-- I think some people were wondering whether this was due to the complexity
[26:17] of platform, and, like, if we could maybe go back to my screen share. I just want to kind of run through that just so that I get through
[26:30] at least some of the things that I had prepared. Quizzy in the forum post says this was coming off of--
[26:39] Well, I won't go back, but what we witness now is Dash network down before Dash platform is even up and running,
[26:46] and the Dash network was down due to a bug code meant directly to support Dash platform.
[26:54] So that's one question, is whether this was related ultimately to Dash platform.
[27:02] I think we all-- In Dash, we all take pride in the fact that we have these separate chains,
[27:09] and whatever new features we are going to be adding to Dash platform, that's insulated, and it won't affect whatever happens there,
[27:22] which is, like, the experimental stuff that we're trying to evolve with, like, that's the whole idea of Dash evolution,
[27:29] is that we're building new features and new features, which is a good thing.
[27:33] But I think the understanding among many of the people in the network was that this is an isolated thing.
[27:41] So if Dash platform goes down, our payments, you know, our bread and butter, our payments chain doesn't go down.
[27:47] And so that kind of just calls that into question a little bit. Whether it was ultimately caused by VLS migration,
[27:55] this whole thing was related to Dash platform, and that's the end of that forum post.
[28:03] I'll go ahead and say what you were going to say. I just wanted to say that it's not directly the platform.
[28:16] Like, the Blaze signature is used in the messages, in the transactions, but the functionality for the platform, like HPMS, were good.
[28:29] There was no issues with the high-performance masternodes. The issue was in the Blaze signature that is used in the L1,
[28:39] and I just want to make a little bit. That's not 100% directly for the Dash platform.
[28:48] So, Amanda, before the show, we talked briefly about is this an incident? Is this a chain halt?
[28:56] And there was that issue of, you know, there was this minor, minor in the sense that small chain that was continuing to grow.
[29:06] And can you talk a little bit about that and what you had, what your thoughts were on that?
[29:13] Essentially, if it is true, I don't monitor the network with tools and things, so I go off secondhand information.
[29:25] So, if what I have heard, which is that at least one minor and maybe some even smaller minors with him did continue producing blocks
[29:36] throughout the entirety of the thing, whether they needed to re-index or not, they continued producing blocks, if that is true.
[29:44] And I guess when I hear that chain called a non-viable chain, it makes me think there are two ways of looking at it.
[29:55] To call that chain a non-viable chain because it is not interacting with the special transactions with which the masternode network runs.
[30:07] Basically, is it the masternode's jobs to get on board with minors or is it the miner's jobs to get on board with masternodes?
[30:17] Calling their chain non-viable says that it's the miner's job to get on board with masternodes.
[30:23] And to me, that flips the logic of Dash's infrastructure on its head and makes it upside down.
[30:30] Yeah, and I wouldn't necessarily say upside down. I would say that it's different than what a lot of people might assume
[30:37] because we are supposed to be a fork of Bitcoin and we retain Bitcoin as a proof-of-work network.
[30:44] And I think if you asked the average Dash person, they would say Dash is also proof-of-work.
[30:52] But I wanted to, if we could go back to my screen again, just briefly talk about the white paper.
[31:00] And if you do a search for the word "longest" in this, this is basically what Bitcoin's white paper says about the longest chain,
[31:09] which is supposed to be the canonical way to determine who is the chain, what is the blockchain.
[31:19] It's supposed to be the longest chain. So it says messages are broadcast on a best effort basis
[31:24] and nodes can leave or rejoin the network. And I would add, even if they're just failing,
[31:30] accepting the longest proof-of-work chain is proof of what happened while they were gone.
[31:36] Or while they were crashed. While they were crashed.
[31:40] And there are several other references to the longest chain. Nodes always consider the longest chain to be the correct one
[31:51] and will keep working on extending it. So do we need to update our documentation
[32:00] to basically say what actually happened in this incident? We are not following the longest chain.
[32:10] And Pasta, the developer, had some insights about that as well, which I'll share after you had...
[32:21] Mikhail, what were you going to say? Yes, yes.
[32:24] Well, there was a chain fork, but it was, from my understanding,
[32:36] it was on the mining pool operator only. The network wasn't accepting such blocks
[32:42] that were posted by such mining pools. Wait a minute.
[32:48] The network wasn't accepting the blocks. It wasn't the miner, the network, at the time.
[32:54] Wasn't he the bulk of the network? He was the only network, actually.
[32:57] He was the only network at that point because all the other nodes were off.
[33:02] So he was not only the majority chain at that point, he was the only chain at that point.
[33:09] So he was the network. And I realize there's controversy there,
[33:15] but what would you say to that? Well, if the other clients would accept such blocks
[33:23] that were produced by this mining pool, that could be considered as the longest chain.
[33:30] But as long as this mining pool was mining its own chain, its node wasn't seen by the network at all.
[33:40] So the longest chain was still a stuck block. The longest valid chain, I think, is what you mean, right?
[33:52] Because he was definitely a longer chain and he wasn't using any customized software or anything.
[34:00] Granted, it was later termed buggy software, but what's the distinction there?
[34:08] And I think the distinction is something that Pasta clarified, if you could go back to the screen share.
[34:16] This is a tweet that Samuel Westrich, the CTO of Dash Core Group, tweeted while we were--
[34:25] I think this was about a week ago, May 21st. But what was more interesting to me was this part that Pasta says here.
[34:36] "It's important to realize that blocks and transactions on the Dash network that are not chain locked and not instance unlocked
[34:43] should not be assumed to have true finality." And that makes me think, okay,
[34:52] so I guess the master nodes are in charge, to answer your question from earlier.
[34:57] The master nodes are the ones that do the chain locking. The master nodes are the ones that do the instance unlocking.
[35:03] So if that's the definition that we can only consider a chain valid if it's chain locked and instance unlocked,
[35:12] I think that needs to be very clear in our documentation that confirmations don't matter.
[35:17] And there's a silver lining to all this, of course, which is all the exchanges and everything that keep--
[35:27] we need six block confirmations in order to consider this secure. That should all go away.
[35:35] We should just be telling them, if your transaction, if a transaction is instance unlocked or a block is chain locked,
[35:43] that's your confirmation. And this event was evidence of that
[35:49] because if one of the exchanges happened to be running one of these nodes that was like, yeah, I'm cool with this longer minor chain
[36:00] that happens to be invalid by the rest of the network or whatever, he wouldn't know that, and he'd be doing exchanges and stuff.
[36:10] And he wouldn't know. He would see there were definitely six blocks,
[36:14] and so some of that could have been confirmed. And I understand that these transactions were all eventually--
[36:21] they were piling up in the mem pool, in the memory pool, and they eventually got confirmed on--
[36:27] In some people's memory pools. Sorry, say again?
[36:30] I just said in some people's memory pools. In some people's memory pools.
[36:34] But, yeah, that was my point is if one of these exchanges' memory pools was following that longer chain that the other ones considered invalid,
[36:43] he wouldn't know that those other ones were considering it unvalid because his daemon, his client, was actually considering them valid.
[36:53] But they weren't getting chain locks, and they weren't getting instance unlocks, and that's important.
[36:58] So while he might have a rule that says six blocks confirmations, that's good, I kind of wonder what might have happened if the minority chain
[37:08] actually was more of a majority chain but was still not getting chain locks or instance unlocks.
[37:14] What would have happened then? But we can speculate on that.
[37:18] But one other thing that I wanted to share was kind of like a reiteration from Pasta, to reiterate as there was some confusion.
[37:29] There is no path that will result in invalidating an instance unlock or chain lock, an instance unlock or a chain lock.
[37:40] Chain lock signatures are the finality in the Dash network, and a chain lock block will never be orphaned.
[37:46] So that's good to know. I mean, that's good to know that, like, DCG is kind of dedicated
[37:55] to basically holding that true. I say DCG is dedicated to that, but I guess what I mean by that is,
[38:07] you know, they made a decision to -- well, I don't want to go down into that tangent.
[38:17] Mikhail, Amanda, anything that you wanted to add before I go further with my screen share?
[38:23] Well, we had a question come in I think that's most appropriate for Mikhail. And just reiterate, why was the BLS signature change needed?
[38:32] You said it actually had not to do with supporting future platform stuff, Mikhail. It was plain core entirely.
[38:40] Yes, exactly. Like, having the same interface for different things,
[38:50] like it will enable the inter-blockchain communication, because when you use the same standard, you will expect the same things.
[39:00] And there are also the improvements in the BLS signatures. So this was needed for new upcoming stuff for both for the dash car,
[39:15] for the dash network, and the platform network. So this was like a big step for the new capabilities of the dash network.
[39:27] And why wasn't a current list of master nodes captured and used just prior to the hard fork?
[39:34] Was it an oversight? I think what happened there was there might have been
[39:44] some kind of a caching issue where certain nodes had a cached version, which means that they store a version that they took a snapshot of in the past,
[39:56] and then they put that in their memory. And instead of reaching out at some later time,
[40:02] instead of reaching out to get that list, you just kind of call back to the thing that you cached earlier.
[40:12] And I have no idea whether that was actually playing a role. I just heard something about that.
[40:16] So there seems to be several issues here where, on the one hand, you had certain nodes that were using the legacy BLS scheme
[40:33] and then certain other nodes that were looking at the new BLS scheme and were saying, "Hey, these are giving me different results."
[40:42] And it may have had something to do with the cache. But kind of stepping back again to the broader picture here,
[40:50] and I just wanted to -- if you could go back to my screen share again once more, Pete. Quantum Explorer, a.k.a. Sam Westrich, CTO of Dash Core Group, did post this.
[41:05] It looks like three days ago, maybe four days ago if I refresh. Chain Halt, what actually happened -- yeah, still three days ago.
[41:15] So it's a few days ago. I'm just going to scroll through this real quick.
[41:19] For any viewers that don't necessarily want to look this up or find it, you can kind of read through here.
[41:28] This whole first part basically is kind of just describing, like, the sequence of events of discovering that there was a bug
[41:38] and then observing that there was a new chain, like we talked about, and even if they reindexed it, it wasn't giving them the same results for different times.
[41:52] They tried that, which they call non-determinism. The root cause section I think is a good section to read.
[42:08] We won't read it because I think we're already getting pretty late into the show here. But to me, this was a good post to know, like, what the current state was,
[42:20] but it was not quite telling me what the root cause -- why this bug in the BLS thing, why that went ahead with a full chain halt.
[42:32] But moving forward a little bit, I did want to point out that what I see as -- I think this is probably the main resolution right here, pull request.
[42:53] This is, like, the code before, if you're not familiar with GitHub's interface. This is the Dash Pay repository, and this is the Dash software.
[43:03] This is the software that creates the Dash G client that we've talked about. And on the left-hand side here, you see code before changes,
[43:13] and then on the right-hand side, you see code after the changes. And so the red lines is code that has been eliminated with the change,
[43:22] and the green lines are code that has been changed. So you can see more specifically this dark red part and this dark red part.
[43:30] These have been changed to these other values. And so this whole little block of code has been removed.
[43:36] Sorry, this is a little bit basic stuff for most programmers, but I just wanted to give a little bit of context here.
[43:43] This is the fix that I'm seeing happening. And if you scroll all the way down, there's a lot of these things, right?
[43:50] So this was not a trivial thing to fix, obviously, and I'm not going to pretend like I understand everything at this point,
[43:57] but I did want to have just a high level. There's 342 lines that were added and 114 lines that have been removed
[44:04] in this change so far, and this pull request is in a draft state. So this is not even at a point where it's considered to be complete.
[44:17] So even though we're a week later, we don't have at least what I would consider 100% full understanding of the issue.
[44:27] Otherwise, we'd have a merge pull request and things like that. So just one real brief mention, a lot of the changes here,
[44:36] you can see all of these files are changes where the changes happened and in what files in the code repository.
[44:45] So you can see this is in the Evo folder, and a lot of the changes are in this deterministic masternode file
[44:57] and then in several other deterministic state, these kind of things. So definitely was part of the code that was related to Dash Platform,
[45:07] at least if their organization is correct. And, you know, these are all under the Evo folder evolution.
[45:17] So that's just one thing worth noting. And then RPC, you can see this is the RPC is remote procedure call
[45:25] where they were doing that request to get the masternode list, I presume. So I think I wanted to just kind of go over this
[45:36] because to illustrate the point that I think that this blog post by Sam was it was good to have something at least,
[45:46] but I don't think it's complete because we don't even have a completed pull request yet. And so we clearly don't have 100 percent handle on what actually happened.
[45:59] And I would like to get to a point where we do have 100 percent clarity on what happened and then maybe document this either clearly more in more technical detail,
[46:17] what happened either in GitHub or in our current existing Dash docs, like docs.dash.org somewhere.
[46:27] So that it's very clear what happened. Do you have a comment on this as to why there wouldn't be a pull request yet for the fix?
[46:38] Well, I don't actually, but as I know, the activation was postponed. The new version was released and the activation was postponed on the 14th of June.
[46:54] So meaning that at the 14th of June, the nodes will start signaling again and the hard work will occur like at the June.
[47:07] So we have some time until the June in June. And when you say the nodes will start signaling in early June,
[47:18] is this something that is already in 19.1? Like if you're running 19.1, your node is going to start signaling whether you want it to or not.
[47:26] So you're talking about a path of inevitability for anybody who's running 19.1? Yes, yes. But I suppose there will be new versions that could change that.
[47:39] So if we would need more time on this, on testing stuff, then the new version will be released and probably postponed again.
[47:54] So the code that I was showing you is going to be ultimately wrapped up into a new version that's 19.2. And I would guess that we would need that released before the June, whatever it was,
[48:08] 15th deadline for things to go smoothly. Is that your understanding Shenmuek?
[48:15] Yes, yes, I believe so. Okay. All right. Well, any final thoughts, guys?
[48:23] I just want to have a better understanding to the point where we could have like a video and/or some text that's clearly like this, this, this, this,
[48:33] that shows all of our stakeholders what happened so that we don't have something like, you know, an instant mind of, oh, dash blockchain goes down.
[48:43] You can't, that can't be considered secure. That's what I want to have is something that we have a strong defense against that.
[48:54] I do have a question, which is, okay, so if there is a path of inevitability to a hard fork already hard coded into 19.1,
[49:06] and as we already know, the whole network is running 19.1 or 90 plus percent of them. I guess, I mean, how would anyone,
[49:19] how would anyone express that they don't feel comfortable heading into a, say this activation time is coming near and someone feels like, actually,
[49:30] I don't feel that the problem that has been solved yet. I don't yet feel comfortable hard forking.
[49:36] Do they revert to, what was it, 18 dot something? Or, I mean, tell me more about this path of inevitability that's already in play,
[49:45] even though there's no pull request for the fix. Well, if you, if you go back to my screen, once again, Pete, Sam did cover this.
[49:54] He says in further news, we're pleased to announce that we're beginning to test resolution. This fix set to included in version 19.2 prior to activation will necessitate mandatory upgrade.
[50:06] I don't know if it explicitly answers your question, but they did say that to help ensure your voice is heard, we'll move forward together.
[50:18] Let's see. I think I missed part of it, but yeah,
[50:24] we plan to consult the community about the potential of expediting the activation date. I don't know.
[50:29] Every, every, every change, you know, obviously has to be adopted by the nodes. So, you know,
[50:36] it just depends on how much trust we have in Dash Core Group that this is actually fixed. So let's end on that note, because Mikhail,
[50:46] I know that you have expressed that you believe that there is a, I don't want to use that word viable again, but hell, I'll use it.
[50:56] There is a viable future in which we don't have to worry about these kinds of things anymore, and that we can trust future releases.
[51:05] So would you expound on why you think we can trust future releases and that this problem can be solved? The first, the first, the network was revived like in less than 16 hours.
[51:24] And that's, that's the good thing to know. There will be always something that I cannot like promise you that,
[51:40] that something would never happen again. But we got to, we got to pay more attention in testing, I think.
[51:51] And, yeah. Sorry to put you in the hot seat here, Mikhail.
[51:59] The reason that I think that we're asking you questions is you're the only one in the incubator, at least probably the most, the person who has the most experience actually working with Dash Core Group.
[52:11] Although, you know, I guess it would be nice if we had somebody actually from Dash Core Group currently that was actually working on the problem here.
[52:21] That would be ideal. And actually what I would say is ideal is I'd love to see something like this from Dash Core Group,
[52:29] where it's not just the three of us, or at least the two of us, Amanda and I, who don't know what we're talking about, that they actually kind of clear it up and say this is, this is what happened.
[52:41] And this is what we're, this is the fix and everything. So I kind of hope that that's in the future.
[52:48] But yeah, again, sorry, sorry to put you in the hot seat here as Dash Core Group representative, so to speak. But I think, Pete, if you wanted to put that question up, once again, I think we could maybe close on that.
[53:08] There was a question from somebody, let's see, from Dash Friend. It's not about the longest chain, but the chain with the most cumulative work.
[53:16] We all know, okay, that's pretty clear. I use those terms synonymously.
[53:22] Even Satoshi in the white paper said, clarified that longest chain doesn't mean, you know, the chain with the highest number. It means the chain that represents the largest proof of work.
[53:33] But I wasn't sure what that, that said one of four. So maybe there was something else regarding who's in control.
[53:40] It's both the miners and the masternodes that are in control. Miners provide the proof as in proof of work and masternodes provide chain locks.
[53:48] So, yeah, and that's kind of my point is, you know, do miners really in control if it's the masternodes that, you know, if masternodes won't accept any chain that's not chain locked, then are they really in any control? They're just kind of like janitors that kind of make blocks for us.
[54:10] And we decide to accept them or not, but they're not really, they're not the governors. And I would say I would go so far to say is that that basically means that we're not like a Nakamoto consensus chain.
[54:29] So there was probably two more messages on that, but I think we're OK. Here we go. Let's let's have it.
[54:39] The bug has nothing to do with platform as stated by Rion. It was an issue on the core chain, as Mikhail said. Right. And the nuance there is that it was not something running in platform because platforms not even on mainnet.
[54:56] My point was that it was something that it was part of the code that that we have written to facilitate Dash platform. So one of my other questions is and sorry for everybody watching this, there are more questions than answers.
[55:14] But one of my other questions is could something like this happen on Bitcoin? Could can Bitcoin have chain can can Bitcoin have a chain halt, I guess, is is the main question.
[55:32] And I would guess that that's the answer is probably yes. Through a hard for if if and when Bitcoin does a hard fork and everybody if they activate it in the same way that we do that we did,
[55:45] which I think was derived from Bitcoin's one of the Bitcoin dips. Could they experience something like this happening where all the nodes do some kind of RPC call and then there's a problem with that RPC call for whatever reason?
[56:02] And then they all go down. Could that happen on Bitcoin? And my guess would be yes. But in in this particular case, it was something that was related to the platform development.
[56:17] As far as I understood. Why else would it be in the evolution folder? So tell me why I'm wrong. Pasta's coming in here. You could have asked me to join.
[56:29] Planning to discuss this on the next development update tomorrow. Great. Yeah, I mean, OK, I don't necessarily have you on for like four minutes, Pasta.
[56:40] I could send you the link right now. Would you like to join? I would almost rather I would almost rather have the two separate calls.
[56:48] And that's why I you know, I also didn't want to impose by inviting somebody that's like very busy fixing the actual problem. But, yeah, there would have been no reason to not have somebody from Dash Core Group on the call.
[57:06] But I did want to have like at least our side of the story expressed where, you know, this is concerning. Again, it's not concerning in the sense to me right now that in the in the state that we're in, we're very, very few people actually care about cryptocurrency, let alone the Dash cryptocurrency at this point.
[57:32] And on a global basis, you know, what is very, very much less than 1 percent of people even know what's going on right now with Dash. And so in that sense, it's fine that this kind of thing happens. But 10 years from now, this would be catastrophic.
[57:47] Like you can't have a global payments network that we that we intend to replace the U.S. dollar system just go down for 16 hours. So. OK, well, we definitely look forward to the broadcast that you're talking about, Pasta, and we'll watch it with eagerness.
[58:08] And my closing comment would be that. I really look forward to, I guess, what could be considered a full resolution of what happened. And as Rion has mentioned, if there's any needed update and documentation for us to have a more accurate identity of who we are in Dash, to me, that's what's the most important.
[58:33] Because for this past week, I've just been thinking to myself over and over prior to last Monday, if anybody had asked me, why should I use Dash? Why should I buy Dash? You know, there's no DeFi. There's no smart contracts.
[58:51] There's no, you know, built in cryptography that keeps everything a secret. Like, tell me what's so cool about Dash, Amanda. I would have said we're the most trustworthy. We've never gone down and we're never going to go down because we hold the payment chain, the payment function to be our single most important function.
[59:13] And we see everything else, DeFi, smart contracts, this, that, you know, NFTs, loo, loo, loo, loo, we see that as bonuses and treats and things that we'll get to in time. Yeah.
[59:26] And so now that I can no longer say that. It's a shame.
[59:31] This has taken like a core part of my life, I guess. Yeah, I think that that's how I feel to some degree, too. And like I said last week, you have to balance it with this is sort of the price of progress.
[59:49] We have to we can't just be completely, completely stagnant. And, you know, we just we're just running on a stable version forever. We have to make up updates and upgrades.
[60:04] So I'm stuck kind of somewhere in between here where on the one hand, it's very sad that this happened, because like you said, Amanda, I can't now say that in all honesty. Like, you know, when Solana goes down or when some of these dumb, you know, what I consider they're not they're not payment, they're not they're not supposed to be money.
[60:27] But then they go down and kind of make fun of it is what's we can't make fun of them anymore. Not that I did that specifically and relished in making fun of them, but I took pride in the fact that the Dash doesn't go down.
[60:42] So, yeah, I'm a little sad about that, but I'm hoping that it's eventually and ultimately made up for by the awesome features that the Dash platform enables. And, you know, hopefully we can get in we can get it to a state where our payments chain is just very rock solid and never goes down again and isolated from any anything that's that might be related to development of any existing or any platform features.
[61:16] Yeah, I hope a new and better identity comes out of this because, yeah, that that would be great. Maybe maybe the prior identity is what's been keeping us in the 70s, 80s market cap because it's an OK identity, but it could be better.
[61:31] Yeah. Mikhail, do you have any final thoughts? Yeah, exactly what Brian said.
[61:39] We have to balance. We have to balance between upgrades and the stability of the network. And I hope there will be no such issues in the in the upcoming years, for example.
[61:53] I don't know. But but, yeah, upgrades have to be done and it's always a risk. But as the network grows, I think that it will well, everything about experience and we and the network is teaching ourself, you know, and hope everything will be fine in the near future.
[62:24] Let's let's read this comment by Sam. I'd like to say, though, from a user perspective, using our wallets, a normal user would not have actually seen anything wrong using exchanges. Yes, they would have. And that's that. Yeah, I agree with that statement that a user, you know, they send a transaction and they they don't necessarily users don't necessarily look to see, you know, is this getting confirmed?
[62:48] Is this getting chain locked? I think a power user probably would have noticed, like if you're using the Dash Core software and you send a transaction and you're accustomed to looking for that lightning bolt that that that signifies this is a this is an instant send locked transaction. They probably would have noticed even if they weren't using exchanges. Maybe correct me if I'm wrong, Sam, there either now or next week when you do your show.
[63:12] But I think they would have noticed that. But regardless, all the transactions that we know of did end up getting confirmed, even though they may not have been confirmed immediately. So the worst case scenario, somebody sends sends a transaction and 16 hours later, it got that instant send lock. I think it might have been actually a little further longer than that to get instant send locks and chain locks.
[63:45] Actually, I think chain locks came first. But you know, regardless, glad that no money got lost. One one thing that I'm a little bit sad about is, you know, there was that one minor that that did a bunch of work. And then they, they had to that work was basically nullified. They thought they were producing blocks that were giving them block rewards. And then that did end up getting reversed, as far as I know.
[64:14] And again, all of this can be corrected by a Dash Core group next week. But his blocks that he thought he was getting block rewards for are gone. It's obviously not great. But yeah, no one lost a Duff. Again, except for that minor correct me if I'm wrong, no economic transactions were reversed. Correct. Okay, but one more thing about the documentation. If that minor had known what pasta's tweet had said, if he had if that had been clear to to him and all the other miners that, hey, you might be mining on a chain.
[64:54] And you also you think that you're in control, because you're a minor, and we're presumably proof of stake network, and you see that you're the longest chain, you also need to check to see if the master nodes are validating your transactions. And more importantly, your blocks, don't keep mining, if you're not getting chain locks. So that needs to be clear in our documentation. And that will help us ultimately get better, get better validation from exchanges and folks like Dash Direct, who, or Dash Direct already knows this,
[65:35] but like other merchants that have historically been relying on confirmations, that is the silver lining here is that hopefully they can then say change their systems to say, just look for, look for instance and locks. And then if you're really paranoid, look for chain locks. But hopefully that will result in a lot of people considering instance and locks more, more secure than confirmations. And on average, that will that will make the user experience for anybody using the Dash network much better on average, because you'll have 99.99% of transactions being considered locked and settled.
[66:20] At the expense of maybe this one in every 10 years for 16 hours event where you might have to wait a little bit longer. Okay, they thought they'd hit the jackpot. But yeah, but yeah,
[66:35] Oh, moneybags over here is saying $120 is not worth being upset about. Well, okay, let's all let's all remember that. Yeah, that may or may not be true. But I think the issue is that it's the principle that counts. Like, who knows, maybe this would have taken days to resolve. And instead of 16 hours, and then it would have been more or the price of Dash could have been 10 times or 100 times higher, and then it would have been much more, or that that mining chain could have been 60% of the network instead of 10 to 15 to 20% of the network.
[67:11] There are lots of different things, but it was the it's the principle that counts here. Anyway, let's let's wrap it up, guys. I think we've said enough, probably some of it inaccurate, but at least it's it's my current understanding. Okay, well, thanks for joining us today, Mikhail. And we are we were glad to have had this conversation and we look forward to it continuing. We look forward to more complete resolutions of what we experienced last week. And above all, we're glad that the network is still running and that we have something to improve upon, rather than being left with nothing.
[67:51] So thanks for joining us today, everybody. And we'll see you next time. Same time, same place. Do it again.