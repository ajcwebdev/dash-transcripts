---
showLink: "https://www.youtube.com/watch?v=rBhjrYGDxY0"
slug: "summoners-dash-layer1-and-platform"
title: "Summoners Game To Use Dash L1 + Platform"
publishDate: "2023-04-10"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/rBhjrYGDxY0/maxresdefault.webp"
---

Ash Francis discusses the development of a decentralized, blockchain-based game called Summoners built using Dash and Dash Platform.

## Episode Summary

tl;dr: Ash Francis, along with his co-founder Alex, have developed a proof-of-concept game called Summoners using Dash and Dash Platform. The game is a turn-based strategy game inspired by Hearthstone and Magic the Gathering. It utilizes Dash transaction signatures for provably fair random number generation and aims to leverage Dash Platform for decentralized game state storage and staking. The project serves as a reference for other developers to integrate Dash into their games easily. While currently in a basic state, the team plans to enhance the game's visuals and features in the future.

## Chapters

00:00 - Introduction and Beginning of Episode
The episode starts with an introductory video discussing the importance of the upcoming FedNow service in 2023.

03:15 - Guest Introduction and Background
Ash Francis, a strategist within the Incubator, is introduced as the guest. Ash and his co-founder Alex have been working on a game called Summoners, inspired by the potential of blockchain gaming.

06:31 - Summoners Game Demo and Explanation
Ash demonstrates the current state of the Summoners game, explaining the gameplay mechanics, game balance, and planned improvements. The game is a turn-based strategy game played on a hexagonal grid.

22:13 - Development Plans and Dash Platform Integration
Ash discusses the development timeline for Summoners, focusing on making the game testnet compatible and integrating it with Dash Platform. The goal is to use Dash Platform for decentralized game state storage and staking.

27:21 - Potential Monetization and Network Ownership
Ash explores the possibility of the Dash network owning and profiting from successful games like Summoners in the future, with the decision ultimately being up to the network.

30:53 - Decentralized Application Architecture on Dash Platform
The discussion delves into how decentralized applications work on Dash Platform, with the execution happening on the client-side and the data storage being decentralized on the platform.

37:49 - Summoners as the First Dash-Based Game
Ash confirms that Summoners is likely the first fully-fledged game built on Dash, with previous attempts being abandoned or limited to simple concepts like coin flipping.

## Transcript

[00:00] [ Music ] >> Jill and her team looked at their own customer transactions
[00:09] and discovered an increasing number of customers moving funds to alternative payment services,
[00:14] such as digital wallets and mobile payment apps. This corresponded with a noticeable decline
[00:20] in customers' deposits and accounts at Community Bank. They knew they had to take action.
[00:26] [ Music ] >> Today, people and businesses expect to make
[00:34] and receive payments at the click of a button any time of the day, every day of the year, including account
[00:40] to account transfers, bill pay, and person-to-person transactions.
[00:45] The FedNow service will be here in 2023. Will you be ready?
[00:51] [ Music ] [ Music ]
[01:11] [ Music ] [ Music ]
[01:31] [ Music ] [ Music ]
[01:51] [ Music ] [ Music ]
[02:11] [ Music ] [ Music ]
[02:31] [ Music ] [ Music ]
[02:51] [ Music ] [ Music ]
[03:15] >> Hello, everyone. Welcome to Incubator Weekly.
[03:20] I am Amanda, and I'm joined, as always, by my trusty co-host, Rion.
[03:24] Hello today, Rion. >> Howdy, everyone.
[03:28] >> Hi. And our guest today is a fellow strategist within the Incubator, and you know him already as Ash Francis.
[03:37] Hi, Ash. >> Hey.
[03:39] >> So today, we're showing you something that we've not shown before, which is a game,
[03:44] a game that the Incubator built. So without much further ado, what is this game, really, Ash,
[03:52] and where did the idea for it even come from? >> Yeah. So probably about, oh, well, maybe even two years now,
[04:00] me and Alex and I were feeling sort of burnt out with a lot, well, a year ago, a lot of blockchain work
[04:07] and a lot of heavy, you know, compliance work on my end. Alex was just doing a lot of work on just hard,
[04:13] hardcore programming, and just -- >> And Alex. Remind us who Alex is.
[04:18] >> Yeah. So Alex is my co-founder. He's mostly the genius that does all the hard development work.
[04:24] I do some of the easier stuff, but he has been working with Dash since 2017, just as long as I have,
[04:32] but he's the wizard behind the curtain to a degree, whereas I'm more of the face of everything that we're doing.
[04:40] And, yeah, Alex is just a very talented developer, and he built the Maya integration prior to that.
[04:47] It was a Thor chain integration. So, yeah, about a year ago, we were feeling
[04:51] we wanted to do something somewhat different, but we were also seeing a lot of news about blockchain gaming.
[04:56] We spoke to some guy from a studio called Chibli Games who was building some blockchain games,
[05:04] and we'd seen Lightbringer as well that was adding all sorts of transactions and value to Litecoin.
[05:10] So we got thinking about how we could build a game using Dash. Obviously, Dash Platform was still on the horizon,
[05:17] as it has been for a while, and we wanted to take that and turn it into something, but we wanted to be original.
[05:24] So we started brainstorming some ideas. We drew on our whiteboard in the office a grid to play on.
[05:33] We printed out paper cards, and we just started game theory sort of testing.
[05:39] Our initial idea was an RNG-based game where you have your main character,
[05:45] and that can summon other monsters and creatures to help it in its mission to defeat the other player's character.
[05:53] It's a 1v1 head-to-head game. And unfortunately, the RNG element that you might summon
[06:00] or you might fail, that didn't prove that great gameplay-wise, so we moved to more of an energy structure.
[06:07] So yeah, we got started. We got dug in and started building all that out.
[06:12] Now it's at a playable state, and the next step is to really dashify everything,
[06:18] as well as build out a library and documentation for other game developers to very easily integrate
[06:25] Dash and Dash Platform into their games and into their processes and plays.
[06:31] Well, ding! Well, I was going to ask to see the demo a bit later, but now I just want to see it now. Can we watch it now?
[06:37] Yeah, absolutely. Yeah, let's get that going. Okay, so this is Summoners.
[06:42] As you can see, we have a hexagonal grid, and again, it's a turn-based strategy.
[06:46] On the left, we have Player 0, and on the right, Player 1. Some useful information is at the top here,
[06:51] including which player you are, whose turn it is, and how much energy you have,
[06:55] and how much energy you are adding per turn. You gain an extra energy per turn if you have a unit or your summoner
[07:00] on the green dotted tiles, and an extra 2 energy per turn if you have the pink tile captured.
[07:05] On the left here, you can see my deck. In the future, this will be hidden,
[07:09] and just below, you can see 5 creatures in my hand. Energy is the resource used to summon these down,
[07:14] to help you in the objective of defeating the enemy summoner whilst protecting your own.
[07:19] Okay, let's get started. As you can see, I've moved my summoner over
[07:23] and brought down some Burning Spears, which cost me 1 energy, which you can see
[07:27] from the number at the top right of the tile. You can also see the stats on this tile.
[07:31] It has 2 attack, 1 health, and 1 movement speed. As you can see, a card from my deck
[07:36] has been randomly brought into my hand following this, and I'm ready to end my turn.
[07:41] Okay, so the opponent has unfortunately not been able to summon on their first turn,
[07:45] because they don't have a 1-cost card. We're thinking of giving the second player an extra energy,
[07:49] or to allow their first summon unit the ability to move and attack right away.
[07:53] Game balance will come further down the line. Alright, let's keep moving and fast-forward
[07:57] through the rest of this game, and see how it plays out. One of the interesting bits, which I highlight here,
[08:03] is direction. Combat is one-directional, so rather than both units head-butting each other
[08:09] at the same time, it's more of a three-way combat.
[08:13] So, if the opponent is going to attack, it's going to be one-directional.
[08:17] If the opponent is going to attack, it's going to be two-directional.
[08:21] If the opponent is going to attack, it's going to be one-directional.
[08:25] If the opponent is going to attack, and they're guarding each other at the same time,
[08:29] it's just the first person to attack, whoever's turn it is,
[08:33] that unit does its damage. We experimented with a staggered approach,
[08:37] and with more sort of, you know, they both hit each other,
[08:41] or once they take turns, but we found this added the most novel gameplay,
[08:45] because you can bring down a unit, attack, and then retreat,
[08:49] or however you wanted to approach that. You'll see here, this game is definitely
[08:55] going in my favour at the moment, with three units on the board,
[08:59] and I think it finishes just after this, and we're given with a brief summary
[09:03] of the outcome of the game at the end. Okay.
[09:11] Here you go. So, similar to chess in a way,
[09:15] you have your units on the board, you've got to defeat the opponent's king,
[09:19] but this, you bring down the units, you can move around the table,
[09:23] different units have different mobilities, and yeah, it's, you know,
[09:27] obviously visual-wise, it is quite basic where it's at right now,
[09:31] the goal is not, you know, the design side of stuff at the moment,
[09:35] that's the next stage, we're actually in talks with a technical artist
[09:39] to turn those assets, and take the game from being a top-down,
[09:43] very, you know, basic visual game to almost a 3D game,
[09:47] somewhere between 2D and 3D, where it's kind of like an isometric perspective,
[09:51] which is called 2.5D, and that will be to turn that game
[09:55] into a very visual production. Huh.
[09:59] When you mentioned your initial, I guess, physical world playtesting,
[10:03] I wanted to show this image that I had found. Ah, yes.
[10:07] There we go. I don't know if everybody can see that.
[10:11] Yeah, definitely. So, yeah, early days,
[10:15] just printing out paper with, you know, those are the energy cards and the table and the board,
[10:19] so you can see how the game's progressed into an actual real game.
[10:23] From that first physical game,
[10:27] we built a web game, so it was just built in HTML5
[10:31] using Canvas with TypeScript, JavaScript,
[10:35] and then from there we've taken it to Unity, so now that it's in Unity,
[10:39] the key thing is building out that whole library for
[10:43] the use of Dash ecosystem, but it's a fun game, our friends have playtested it,
[10:47] we've spent, you know, hours playing it, there's still going to be balance
[10:51] and there's going to be new cards with different factions
[10:55] and right now the cards, for example, when you summon them down, they can't
[10:59] move until their next turn. We're going to add ones where they can move quickly
[11:03] or even when you summon them down, it does an area of effect damage or, you know,
[11:07] however it is, so there's going to be all sorts of features down the line.
[11:11] Okay. Well, going more in the thread of development,
[11:15] so we're not feature complete yet, as you've just
[11:19] said, and so I wanted to clarify,
[11:23] this was something that you had mentioned just this morning with regard to the title of the video.
[11:27] Is this game currently using Dash
[11:31] L1 or Platform Testnet? So right now
[11:35] the game isn't using Platform or Layer
[11:39] 1. We have done some experiments with using Layer 1 for
[11:43] random number generation. In fact, that was a game that we built previously, but we can
[11:47] cover that more in a very basic game where we use Dash transaction
[11:51] signatures, which after discussion with Dash Core Group, they were
[11:55] considered fair entropy,
[11:59] completely random data that we could rely on for seeding a
[12:03] random number generator, and that'll be part of this, you know, throughout
[12:07] hundreds of different games, thousands
[12:11] of different games, random number generation, whether that's drawing a random
[12:15] card from a deck in, let's say, a gambler game like poker, or
[12:19] in our case, the unit, or, you know, the damage a unit
[12:23] does if that is a varied, you know, between a certain amount
[12:27] and another, you need random number generation and especially when it comes
[12:31] to e-gaming, so poker or slots or however, it
[12:35] has to be fair, and there's this whole concept of provably
[12:39] fair where if someone can say, you know, this
[12:43] machine, I mean, there's huge, like, legal structures
[12:47] for this in the States, but if you could do this online in a way, and there are
[12:51] companies doing this where you can show that that number has
[12:55] been provably fairly generated and then odds aren't being manipulated,
[12:59] you know, people worry about machines saying, oh, you know, that machine
[13:03] will only pay out once it's had, you know, 100,000 in it, and then it'll pay out
[13:07] 50,000 or whatever it is, but there was a win on there last week,
[13:11] so I'm not going to play on that, you know, whereas if you can show that every
[13:15] role, every card draw, everything is completely
[13:19] fair, that's novel and that's good, and if you can do that
[13:23] in a way where it's cheap and effective and on the blockchain and fully
[13:27] transparent, that's powerful. - So does the random number
[13:31] generation using L1 come from blocks being found?
[13:35] - No, it comes from the transaction signatures, from the
[13:39] actual instance transaction being locked, so it's the work done
[13:43] by the Mars Node Quorum, if I'm not mistaken, to
[13:47] sort of, yeah, validate and lock that transaction.
[13:51] So it's a BL sig, I think. So yeah, it's
[13:55] part of Dash, really. It's, yeah, it's not
[13:59] just in every other crypto's transactions, it's something that's specific to
[14:03] Dash. - Okay, so then beyond random number generation on L1,
[14:07] where does the platform component come in? - Oh, it's, you know,
[14:11] obviously, how long's a piece of string? Ultimately, platform is, again,
[14:15] a very open-ended product and when it comes to gaming, that
[14:19] product could have hundreds of use cases. Obviously, you know,
[14:23] there's the economy side of things, whether that is you're building and releasing NFTs
[14:27] on Dash platform that are cross-game or cross-universe or even cross-studio.
[14:31] You know, if I could take my items from Fortnite and bring them into
[14:35] Counter-Strike or my identity, my avatar, if I could have
[14:39] my whole, sort of, economy and game state, even whether
[14:43] you know, in the case of Summoners, each move that's
[14:47] done on a state game where users bet against each other,
[14:51] we haven't spoken about that, so we should speak about that. - Yes. - Yes, that can be
[14:55] stored on Dash platform, so everything can be seen historically
[14:59] as a record of data and even just using Dash platform
[15:03] as an effective part of their back-end, you know, you probably still
[15:07] need some level of game servers for other aspects of the game, but if
[15:11] you can mitigate your need for that and just use Dash platform as
[15:15] that database or even in the future when data contracts have more
[15:19] features as part of the game logic, you can just outsource that
[15:23] and you know it's a reliable, bulletproof network hosted all around the world
[15:27] you know, on 2000 whatever it is, high-performance mass nodes,
[15:31] whatever it ends up being, you can be confident in the reliability,
[15:35] the availability of that data, the transparency,
[15:39] it's just, you know, the possibilities are endless, really, when it comes to
[15:43] using it. - So I remember reading in the initial
[15:47] specification of this game that the first feature
[15:51] intended to be added after what we've seen demoed is the ability
[15:55] to wager on the outcome of a game. Is that something that can be done on L1
[15:59] or does that require platform to be done? - It can be done
[16:03] on L1, but it requires platform to be beautiful and seamless.
[16:07] So on Layer 1, we can do this thing called, well,
[16:11] escrow to a degree, but reality is there's a concept called
[16:15] MAD, which is Mutually Assured Destruction, so each user
[16:19] deposits into a two-of-two
[16:23] multi-sig wallet, and then if they don't sign it, then
[16:27] that money is just destroyed. So there's a certain trust, but it's very limited.
[16:31] There's ways you can get around that, whether you have a bond that is
[16:35] sliced if the user doesn't sign the
[16:39] transactions they're supposed to, or one way that we're looking
[16:43] at doing it is having a third signatory, which will be operated by us,
[16:47] which is just an arbitrator, and then on the end of the game,
[16:51] it will automatically just sign the transaction to the winner, and then the winner
[16:55] only needs to sign that transaction. So effectively, you'd have a two-of-three
[16:59] multi-sig wallet that both users deposit into at the start of the game,
[17:03] and then at the end, we'll sign the transaction, and the winner will sign
[17:07] the transaction, and that's only in the case where the loser doesn't sign the
[17:11] transaction for whatever reason, and they would have to create a broken
[17:15] client and do all sorts of work to even be able to do that in the first place,
[17:19] and even then, it wouldn't work with this in place. But, bringing
[17:23] Dash Platform into the equation, data contracts right now,
[17:27] they don't have any sort of layer one interoperability.
[17:31] They can't be used as a transaction criteria, whereas
[17:35] in the future, they're not smart contracts in that sense. A future
[17:39] iteration, an early iteration intends for the ability
[17:43] to have Dash Platform data contracts to be able to
[17:47] be used in transactions. So, I would be able to say
[17:51] the output of this, so I would be able to write
[17:55] two transactions, but only one of them is valid, and that would be the
[17:59] valid one based on the winner. So, if this data contract is written to in
[18:03] this form, that this transaction's valid, i.e. the payment to the winner, otherwise
[18:07] this one is, and that way, there would be no third party. It would all be done
[18:11] via Dash Platform, and it would all be trusted or
[18:15] trustless, really. And the whole point is that
[18:19] that goes beyond just this game. That goes to any sort of escrow
[18:23] situation, any situation where that proof of transaction or
[18:27] proof of event occurring external to the transaction is stored
[18:31] on the database. So, it's really powerful.
[18:35] ... ...
[18:39] We just got a little bit of feedback from Rion's side, but it should finish out in a moment.
[18:43] So, then, okay. So, it sounds like this sort of engine is
[18:47] reusable, not only for other games, but even just for other basic escrow
[18:51] requiring applications. Yeah, I mean, Platform has
[18:55] huge, you know, ramifications in terms of anything like that,
[18:59] really, and the gaming is a great example, and it's one where we can build this reference
[19:03] project and this full product that uses
[19:07] that, but there are examples beyond that as well, and
[19:11] it's huge where any multiple parties need to reach some
[19:15] resolution or agreement where that data can be stored on Platform
[19:19] and then used as a transaction criteria. It's just, yeah,
[19:23] it's very powerful, and I'm excited to demonstrate this in the
[19:27] game, and to provide a library that allows other
[19:31] developers, game developers or Unity developers, to use
[19:35] this in their projects. But, yeah, it does go beyond that.
[19:39] I mean, even most of the casino games in
[19:43] Vegas are built using Unity. This is not a, you know, small technology.
[19:47] Unity is used by millions of developers from
[19:51] indie, small, one-man teams to, you know, thousand
[19:55] developer teams. It's a very big project, and
[19:59] building that Unity library is obviously the first step of the
[20:03] sort of Dash Platform and Dash gaming sort of journey
[20:07] in that regards. So, yeah, I'm very excited.
[20:11] - So, let's see.
[20:15] I don't know that that is a...
[20:19] Does that question make sense to anybody? - It sort of does, but it's kind of
[20:25] different in relation... I'll answer it anyway.
[20:29] So, WeChat money to Dash Platform. No.
[20:33] You can send WeChat to someone and have them convert it
[20:37] into Dash and then use Dash to top up your Dash Platform credits, but you will just
[20:41] use Dash on Dash Platform. You're not going to be using a separate currency. Apart from
[20:45] you may get people that release tokens on Dash Platform. We'll get into that in a
[20:49] future video, I'm sure. But if you were looking to buy Dash,
[20:53] you could use WeChat, and a Dash Platform application could actually act
[20:57] as the escrow provider for that in a way, so that they could have a
[21:01] proof of funds, a third-party escrow.
[21:05] You could do, effectively, a LocalBitcoins using Dash Platform, and I think that project's already
[21:09] been worked on, and may have been talked about last week, very briefly.
[21:13] So, yeah. - Okay, so people can, I mean, in its
[21:17] limited form, people can play this game right now, if we give
[21:21] the URL, right? - Yeah, it's just on summoners.gg.
[21:25] It is a very... Yeah, it's a very basic demo.
[21:29] So, it's... At this stage, you know, it's a proof
[21:33] of concept, it's a minimum viable product. We are looking to iterate
[21:37] on it, probably not until Q4 2022, because we're going to
[21:41] wait until Platform's a little bit more stable. There's been exciting news this week
[21:45] about a release on that front, going to
[21:49] a testnet, but we're going to be sort of stepping back from this for a little bit,
[21:53] and then we'll be hitting it again in Q4. So, right now,
[21:57] playable demo state, we'll probably work on some other proof of concept
[22:01] in terms of, you know, maybe the staking side of things,
[22:05] we'll have a testnet version with that on pretty, you know, in the next quarter, but
[22:09] it's going to be a slower development pace by now. - I was just
[22:13] going to ask about testnet. Do you have plans to
[22:17] make this testnet compatible, and
[22:21] if so, when is that happening? - Yeah, so
[22:25] I mean, we built a game, just an important sort of little segue
[22:29] on this. We built a game almost two years ago now, maybe three years ago,
[22:33] where there was a coin flip on testnet, effectively,
[22:37] and it was a provably fair coin flip, and that was, again, using that same
[22:41] Layer 1 transaction signatures. So, you know, we're really happy to
[22:45] do the Layer 1 stuff
[22:49] on testnet again. It's just the stability of
[22:53] Dash Platform and developing against that, and basically how we
[22:57] gracefully interact with Dash Platform. Obviously, myself and Rion
[23:01] and even, you know, there is another project I think Tim's working on,
[23:05] are trying to solve for that wallet decentralized
[23:09] application interaction layer. The way I'm
[23:13] approaching it is this metamask-style wallet where it all creates
[23:17] keys to write to certain data contracts and share them with the decentralized application,
[23:21] but do we want to, you know, build a project where
[23:25] you're importing a mnemonic and then it's handling all of that, or do we want to try and
[23:29] extrapolate that away and get that done now? And that's kind of where
[23:33] my focus is for this next quarter, that I want to not try and do
[23:37] everything in every individual vapp whilst we're waiting on platform. I want to build
[23:41] this sort of more, you know, this gateway solution in terms of
[23:45] this wallet that can handle all those keys and all the transaction signing, the reading and writing
[23:49] to Dash Platform, and sort of elegantly extrapolate that
[23:53] away from any dApp developers and dApps themselves. So that's
[23:57] kind of my focus for this next quarter.
[24:01] Oh, please go ahead, Rion. I was going to say, do you have any plans to
[24:05] monetize the app itself? At this stage, no.
[24:09] The core goal for this project really is that reference project.
[24:13] I'd love to see it be a production success. I enjoy the gameplay.
[24:17] I want to take this to production. I want it to be visual. I want it
[24:21] to be almost like a eureka moment for
[24:25] any game developer that once sees this, they'll play it. They'll be just like,
[24:29] "This is great. How is it using Dash Platform?" They'll see how easy it is to use Dash
[24:33] Platform. So we will take it all that way. We will try and turn it into a
[24:37] production success with actual users using it. And then at some point, maybe
[24:41] we would look to monetize it. Ultimately, I wouldn't make that decision myself.
[24:45] I would put that before the DAO. I would give them the option to say,
[24:49] "Hey, yes, we want this to go and be a property as part of the diff's portfolio,
[24:53] or we want this to be monetized slightly so that those
[24:57] funds can be used for marketing and it can be independent
[25:01] of the DAO's funding." But ultimately, I wouldn't
[25:05] make that choice myself. That would be the network's choice.
[25:09] And obviously, everything would be MIT licensed because that's the whole
[25:13] purpose of the incubator. Everything would be fully open source.
[25:17] Well, that was something I sure hadn't considered or heard of before.
[25:21] Ash, you're saying that games like this,
[25:25] should they ever be in a state that they can generate profit,
[25:29] that that profit could be directed anywhere? And in this case,
[25:33] it could be directed to somewhere like the diff, where the network
[25:37] itself can have these profits? Yeah. Ultimately,
[25:41] I don't think the diff would own it outright 100%. There would have to be
[25:45] some operating entity. I mean, they could own it outright 100% and then
[25:49] pay an operating entity to handle that side of things.
[25:53] It just depends what the diff is, the appetite of the diff and the DAO.
[25:57] The whole network has basically funded the building of this project as a
[26:01] reference project. If it then becomes an independent success of being
[26:05] a pure reference project, or they want it to stand on its
[26:09] own two feet, become revenue generating, bring that yield back into the network
[26:13] so that can be then reinvested, however that works, I'm game.
[26:17] Ultimately, that decision belongs to the network,
[26:21] not to me. You're game? Yeah.
[26:25] I'm game. I'm very game. And it'd be exciting for me to
[26:29] see that happen. Ultimately, this
[26:33] project, the advantage of this with many of the incubator projects is
[26:37] that we're killing multiple birds with one stone, effectively.
[26:41] This is a great reference project. It's the justification for building out a great library that
[26:45] other developers can use. It further tests and stresses Dash Platform.
[26:49] It could become a good stand-alone project. There's so much to this
[26:53] that is advantageous to the network. It's just logical.
[26:57] I'm very excited to see what's next there.
[27:01] You may have touched on this already, but maybe you could
[27:05] recap on it or expound on it.
[27:09] What do you plan on using Dash Platform for
[27:13] in the game? Would there
[27:17] be other alternatives? What would be the alternative, and what would be the pros and cons?
[27:21] I touched on this regarding the staking, so a brief
[27:25] recap on that is without Dash Platform, we can do a
[27:29] mutual assertion destruction, a multi-sig wallet, like two or
[27:33] three signatures with an arbitrator. With Dash Platform,
[27:37] the next iteration will have the ability for Dash Platform data
[27:41] to be used as a transaction criteria so that we
[27:45] could step back. There's no arbitrator needed.
[27:49] Arbitrator, arbitrator. You wouldn't need that third party. It would just be
[27:53] a two of two, but the transactions would be pre-signed,
[27:57] but only the one where the winner that had that
[28:01] data in Dash Platform would actually be a valid transaction.
[28:05] That's one part of it. The other part of it is game state. Rather than
[28:09] saying, "Hey, here's this centralized party that we're relying on for the state of our
[28:13] current game and what we agree on," we can write all that data. We can say,
[28:17] "Hey, this is what the player did with their first move, their second move, their third
[28:21] move," and that historical log will be immutable and on
[28:25] the blockchain and Dash Platform. That kind of thing is very
[28:29] powerful in terms of having that transparency but also removing
[28:33] that component. If you can say, "Okay, here's
[28:37] an application you can run in a browser and it will handle and read and write all that
[28:41] data without any third party," you're reading and writing data to Dash Platform.
[28:45] It is a fully decentralized application at that point. This is the whole
[28:49] beauty of Dash Platform versus Ethereum Smart Contracts.
[28:53] You're not... You know that data is valid
[28:57] because it's that data. You're doing the execution on your side
[29:01] rather than the Ethereum virtual machine. In the future, maybe we'll have
[29:05] more of that capability but there's no third party.
[29:09] You're not saying, "Hey, I need someone else to matchmake for me. I need someone else to
[29:13] handle the data of what's happening in this game. I'm just running an application on my
[29:17] device, be that my mobile phone or my browser." Again, Unity
[29:21] you can publish to browser, to mobile phones, to desktop. It's a
[29:25] multi-platform system. Instead of saying,
[29:29] "This service needs to be running for this game to be playable," this game
[29:33] is there. It's on everything I need for that,
[29:37] whether I'm matchmaking and looking for an opponent or whether
[29:41] I need to know what that opponent's moves have been. That can all be stored on Dash Platform
[29:45] and I don't need to rely on anyone
[29:49] to access that. No one can stop me accessing that at all.
[29:53] Just to recap from my understanding, what's
[29:57] interesting about this is that all of the execution,
[30:01] the code execution is done on
[30:05] the client's browsers, but the data can be stored
[30:09] on what would normally be a server, but in our case
[30:13] it's going to be Dash Platform, and that's what makes it you can have
[30:17] the full application. If you needed any kind of server-side
[30:21] execution, then we would need either smart
[30:25] contracts on Dash Platform or we would need a separate server, but you're
[30:29] saying that the game doesn't need any server-side code execution,
[30:33] just server-side code storage, or not
[30:37] code storage, but data storage, state storage.
[30:41] That is what makes Dash Platform unique as far as
[30:45] I can tell in this space,
[30:49] and this is one of those games that will test that
[30:53] and demonstrate that. I'm looking forward to a stable test net
[30:57] that we can port this onto and to
[31:01] show that, because I think that's one of the things that's been a big mystery to people
[31:05] is how do decentralized
[31:09] applications really work on Dash Platform?
[31:13] In a way, it's not even really a decentralized application. It's
[31:17] a decentralized state storage where the
[31:21] execution is happening on the clients.
[31:25] Each client can validate that.
[31:29] You're not trusting somebody else and how
[31:33] their client is operating. You can validate that that data matches your
[31:37] expectations and that it's been done in the right way.
[31:41] The data contracts provide the schema for how that is done and the structure.
[31:45] That is the beauty of Dash Platform. I hope we can try
[31:49] and communicate that better. I hope DCG can communicate that better
[31:53] to developers and to the community. I think that
[31:57] it's a very important point. To be able to take
[32:01] advantages of the kinds of things you guys are talking about, namely to access this
[32:05] decentralized storage wherein the execution
[32:09] of applications takes place on the client side only,
[32:13] are we talking about DAPI? Am I using an old-fashioned
[32:17] term here? What would the client need to do in order to be able
[32:21] to interact in the way that we're describing?
[32:25] Would there need to be a download of some kind, a browser extension?
[32:29] In terms of actually reading and writing the data,
[32:33] reading the data could be done without any other
[32:37] else running. You can just use the JavaScript library or whatever. There's multiple
[32:41] libraries and it's very lightweight. You don't have to download the blockchain,
[32:45] sync headers, whatever it is. You can use a library which you're then relying on a trusted
[32:49] node to give you that data, but you can independently verify
[32:53] that with multiple nodes. There's no issue there, really.
[32:57] In terms of actually writing the data, you would need to have a Dash account in
[33:01] some form, whether that's a wallet. You would need a wallet or even a
[33:05] private key, technically. You would need to be able to
[33:09] have that, whether you've installed an extension, you're using a web
[33:13] wallet, whatever it is, you would have to have something to be able to write that data
[33:17] with. The DAPI term that you're
[33:21] using, usually when people talk about an API,
[33:25] they're usually talking about application
[33:29] programming interface. It's usually
[33:33] a client that's requesting data, and
[33:37] that data, typically these days, that data comes back in the
[33:41] form of JSON, JavaScript Object
[33:45] Notation. It's just data. You're requesting data, you're getting data back.
[33:49] DAPI is just doing that exact same thing,
[33:53] but instead of interacting with a server,
[33:57] a trusted server, you're interacting
[34:01] with one of the Dash master nodes as your server
[34:05] instead of some corporate entity.
[34:09] That's the difference, and I think that term is still, it's not an
[34:13] old-fashioned, it's not an old term, that DAPI is still a
[34:17] thing. Yeah, DAPI is still
[34:21] a thing, so you're using the term properly, but that usually doesn't
[34:25] involve requests for execution.
[34:29] It sometimes can, and I'm not a master programmer by any
[34:33] means, but usually it's a request for data, not a request
[34:37] for a function.
[34:41] Typically, you'd use the term RPC for requesting a functional
[34:45] call. And so, the wallet that
[34:49] you and AJ are working on, Rion,
[34:53] the wallet that we covered two or three weeks ago here on
[34:57] the show, is that something that would
[35:01] perform these functions that you're talking about, so that no one
[35:05] would need to download more than, just say, that wallet to be able to get the full
[35:09] interaction of what one envisions the summoner's game to eventually be?
[35:13] Yeah, like, Ash can touch on this again when I'm done, but
[35:17] like he said, you need some kind of wallet
[35:21] to do the requests because that costs a small amount
[35:25] of Dash when you're requesting data, or when you're requesting
[35:29] to store data, at least. The wallet, so yes, our Dash
[35:33] wallet, our browser wallet
[35:37] would be able to perform that function, given that
[35:41] there are integrations with the game, but Ash
[35:45] could maybe talk a little bit more about that. Yeah, ultimately,
[35:49] the way we're looking at doing this, the approach that we're taking, myself and
[35:53] Rion, are different but complementary. Mine's more focused using
[35:57] the SDK side of things that CoreGroup have released, which
[36:01] has a lot of dependencies, and I appreciate that Rion's
[36:05] wallet is, it's called Vanilla, but I
[36:09] feel that's somewhat of a derogatory term these days, but it's more of a purist solution.
[36:13] It removes a lot of these dependencies, it's probably going to be more efficient and more secure,
[36:17] so I like it, and in time,
[36:21] there'll be established standards for how these wallets
[36:25] and DApps integrate. Here is the communication
[36:29] expected from a decentralized application, here is how the wallet will respond to that
[36:33] and vice versa. As we build out that standard,
[36:37] his wallet will have that, my wallet will have that, it will be
[36:41] something that we work on and we iterate going forwards, and we'll work together on that standard
[36:45] in the same way any sort of, the World Web Consortium
[36:49] agrees on HTML5 standards will have this communication layer
[36:53] as a standard, and that means that no matter what wallet
[36:57] the user has, even let's say Metamask added full-platform support,
[37:01] they would use the same structure, no matter what wallet, the user can use
[37:05] any wallet with any decentralized application, any supported wallet,
[37:09] I guess you could say. It should be agnostic,
[37:13] it shouldn't be locked into any provider in any structure.
[37:17] That would be a step further, that would probably come later though,
[37:21] like the prototype, the initial minimum viable product
[37:25] would most likely just come with the wallet that
[37:29] Ash has in mind, and then we would build integrations as we go
[37:33] based on what Ash just said, the standards that emerge.
[37:37] Okay. So,
[37:41] I don't know, maybe I just haven't joined that many conversations in years past,
[37:45] but this is certainly the first conversation I've joined that is about
[37:49] a game on Dash. Is this the first game on Dash, Ash?
[37:53] Yeah, it was a project back in 2018 that
[37:57] received some funding to build a Dash game. It was some students at the university
[38:01] that were working on game development in their third or fourth year, I believe.
[38:05] They came up with some concepts, but they never released anything, and that project,
[38:09] as far as I'm concerned, is abandoned and unfortunately
[38:13] did not go anywhere. Ourselves,
[38:17] myself and Alex, we built a game via the incubator again almost, yeah,
[38:21] like I said, three years ago, I think now, pretty much, maybe two and a half years ago,
[38:25] that's a coin flip game, a provably fair coin flip game.
[38:29] Very simple, very simple for developers to basically use to
[38:33] understand how you can use BL6 as
[38:37] entropy for random number generation. I would say
[38:41] between that and the other coin flip games, those are probably the ones that I
[38:45] know of. Brian, do you know of any other Dash or
[38:49] games? No, I don't. Yeah. Okay.
[38:53] Okay, well, that covers the questions that I had.
[38:57] I know that I'm still just left here reeling about, for example,
[39:01] so, diff aside, profits from games
[39:05] deployed onto the Dash network, say, by the incubator or by
[39:09] anybody else, could, for example, also burn profits,
[39:13] right? Couldn't profits just automatically be burned.
[39:17] Yeah, I mean, again, it's open-ended how people approach that.
[39:21] We've seen other projects in the crypto ecosystem that have
[39:25] used burning as a mechanic for even minting new tokens
[39:29] as well. There's all sorts of possibilities there, absolutely.
[39:33] Right. Oh, there's
[39:39] a good question from James, just to reiterate on the summoner's
[39:43] side of things. The game that this is sort of most analogous
[39:47] to would be Hearthstone, but instead of Hearthstone
[39:51] having just a flat grid like that where players and
[39:55] creatures attack each other whilst they're protecting their main units, this just has a hex grid.
[39:59] I know the UI isn't the most intuitive, but
[40:03] that'll come in time. All of these things are iterations. You start
[40:07] with the minimum viable product, and you iterate and improve. We'll make it
[40:11] easier for you to understand. We'll have a tutorial. There'll
[40:15] be nice cards in a hand, in a deck. Right now, the art
[40:19] style is just very basic. It is just a -- and I do have
[40:23] to run it when I demo it with people. I have to act as somewhat of a
[40:27] concierge. I have to help them and explain things, but that will get better.
[40:31] It is like Slay the Spire, but it's not like a roguelike, but from the visual
[40:35] aspect, the future design will be like Slay the Spire.
[40:39] Realistically, right now, the goal is more a Hearthstone or Magic
[40:43] the Gathering, which for Amanda, if you're unfamiliar with either of those,
[40:47] and Rion too, they are incredibly popular games
[40:51] with millions of users, and they're very revenue successful
[40:55] as well. People put a lot of money into those games,
[40:59] and they work on mobile as well, which it's a cross-platform game. The goal
[41:03] is that you can play it casually and have just a five-minute match, or you can
[41:07] play it on your phone super casually, however you like, really.
[41:11] That's the goal with this. We want to be as accessible as possible
[41:15] to anyone. - Fab. Okay.
[41:19] Well, absent any further comments from any of us, I'll say thanks for
[41:23] joining Rion and me today. Ash and viewers,
[41:27] we look forward to seeing you all again same time, same place next week.
[41:31] Yeah? - Thanks, Ash. - Thank you, guys. - Bye, everyone.