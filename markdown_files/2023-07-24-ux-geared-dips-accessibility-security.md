---
showLink: "https://www.youtube.com/watch?v=XAA6nDl_H7k"
slug: "ux-geared-dips-accessibility-security"
title: "UX-Geared DIPs for Accessibility & Security"
publishDate: "2023-07-24"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/XAA6nDl_H7k/maxresdefault.webp"
---

AJ presents four technical DIPs to improve Dash's privacy, usability, and modularity.

## Episode Summary

tl;dr: AJ presents four Dash Improvement Proposals (DIPs) aimed at enhancing privacy, usability, and modularity in the Dash ecosystem. The DIPs cover topics such as defining mix tracking, creating canonical deterministic wallet and XPUB IDs, enabling offline-first contact payment subscription exchange, and implementing cash-like denominated sends. These proposals offer alternative approaches to existing solutions, focusing on simplicity, backwards compatibility, and progressive enhancement.

## Chapters

00:00 - Introduction and Background on Money
The episode begins with a discussion on the nature of money, government-issued currency, and the origins of gold and silver as money.

02:16 - Government Currency and its Limitations
The hosts explore the limitations of government-issued currency, its inability to issue unlimited debt, and the need for a sound, independent currency.

04:34 - Emergence of Decentralized Cryptocurrencies
The conversation shifts to the emergence of decentralized cryptocurrencies and their potential to create a better form of money through innovation and market action.

05:45 - Introducing the Hosts and Pioneer Day
The hosts introduce themselves and discuss the significance of Pioneer Day in Utah, drawing parallels to the pioneering spirit within the Dash community.

08:36 - Overview of AJ's Four DIPs
AJ introduces the four Dash Improvement Proposals (DIPs) he has submitted to the Dash core repository, aimed at enhancing the ecosystem's privacy, usability, and modularity.

09:00 - DIP 1: Define Mixing and HD Mixing to Define Mix Tracking
AJ explains the first DIP, which focuses on defining mix tracking and improving the way CoinJoin transactions are handled in Dash wallets.

22:02 - DIP 2: Canonical Deterministic Wallet and XPUB IDs
The second DIP introduces a simple and secure method for generating wallet and XPUB IDs, essential for syncing and sharing contacts between devices.

30:37 - DIP 3: Offline First Contact Payment Subscription Exchange
AJ presents the third DIP, which defines a URL format for sharing contact information and enables offline contact sharing using QR codes and existing standards.

36:47 - DIP 4: Cash-like Denominated Send and XPUB Send
The fourth DIP proposes a cash-like denominated send feature, where every send is essentially a CoinJoin transaction, preserving privacy by default.

46:17 - Summarizing the DIPs and Their Potential Impact
The hosts summarize the key aspects of the DIPs, discussing their potential to provide alternative, backwards-compatible solutions to existing challenges in the Dash ecosystem.

49:26 - Future DIPs and Modular Masternode Services
The episode concludes with a brief discussion on a potential future DIP that would enable masternode owners to offer modular services to the network, enhancing scalability and flexibility.

## Transcript

[00:00] It makes no sense whatsoever to think that a currency is money for the only reason that a government issues it. Ultimately, a state-issued currency is nothing but credit and what it
[00:19] is basically using is a unit of measure and as a way of transferring its fiscal imbalances throughout the entire economy. And it does it via inflation, which is the destruction
[00:34] of the purchasing power of the currency. Certainly, it cannot issue all the debt that it wants in its own currency because the demand for the currency is not unlimited. This is why,
[00:46] for example, so many governments need to issue debt in foreign currency. So are foreign currencies or world reserve currencies more sound?
[00:56] When they say that governments don't have a monetary constraint if they have a world reserve currency or if they are monetarily independent, that is a stupidity. Like all
[01:10] political constructs, when you pass all the limits of confidence, the entire thing crumbles. So if government currency is not money, what is money?
[01:20] Menger described money's origins as basically evolving out of market exchange, a commodity that's highly valued suddenly becomes acquired not for consumption, but rather in anticipation
[01:32] that it would be used later to trade for something else. Where does the value initially come from?
[01:36] What Mises says is that the exchange ratios that are associated with the commodity that becomes money can be traced back or regressed back in time when it was originally a commodity.
[01:48] So like gold and silver? The reason why J.P. Morgan said that gold is money and everything else is credit is
[01:54] because to a certain extent he was completely right, because supply is limited and everybody in the world views gold as something that is a unit of measure and a mean of payment
[02:09] and certainly as a reserve of value. So if gold and silver were used as money, how did government-issued currency come about?
[02:16] If gold and silver are just money, well why not just grab the gold and silver mines? And in fact governments would do that.
[02:21] Ancient kings would normally grab the gold and silver mines. In theory you have all the gold and silver you want, you've got all the money.
[02:26] Why would you then take the stuff, stamp your picture on it, give it to people and say "OK, everybody in the kingdom has to give me one of these macagams."
[02:33] Think about it, it's kind of odd. But it makes perfect sense if you're trying to feed an army.
[02:38] Here you have this army of 100,000 people, they're sitting in town on the border, well how are you going to get food to them?
[02:45] Under ancient conditions, unless they're next to the ocean where it's relatively easy to move stuff around, it's extremely difficult to move around large amounts of grain, they're
[02:52] going to eat everything within walking distance in a matter of weeks. So what are you going to do?
[02:58] Either you have to employ another 100,000 people just bringing them stuff, or you can give them all tiny little pieces of metal with your picture on it and say "OK, everybody
[03:08] in the kingdom has to give me one back, voila, you've just employed your entire population to feed the army."
[03:15] And that's what you're going to do. You're going to give them all the things they want.
[03:17] You're going to give them all the things they want. You're going to give them all the things they want.
[03:19] You're going to give them all the things they want. You're going to give them all the things they want.
[03:21] You're going to give them all the things they want. You're going to give them all the things they want.
[03:23] You're going to give them all the things they want. You're going to give them all the things they want.
[03:25] You're going to give them all the things they want. You're going to give them all the things they want.
[03:27] You're going to give them all the things they want. You're going to give them all the things they want.
[03:29] You're going to give them all the things they want. You're going to give them all the things they want.
[03:56] Independent currencies are closer to what money really is if they preserve the three principles of being a reserve of value, a generalized meaning of payment, and a unit
[04:09] of measure. An independent currency, independent money, is always going to have the benefit of not
[04:20] suffering from a government that will always have the incentive to transfer to the rest of the citizens its fiscal imbalances by destroying the purchasing power of the currency.
[04:34] Might we look to decentralized cryptocurrencies? Money has been nationalized for a hundred years and then seemingly out of nowhere in
[04:40] early 2009, we saw the emergence of a kind of revolutionary tactic from below to give us a better money.
[04:48] You have the use value of the blockchain leading to the monetary value of the currency unit itself.
[04:56] This is a technology that's not going anywhere. It's just going to continue to be played with and improved upon, and it's something that
[05:04] all economic actors everywhere in the world have to deal with. The great calling of our times today is for private actors in the private space where
[05:15] there's real innovation to use the new tools we have, among which are distributed networks, to create better versions of all the things the state has attempted to monopolize and
[05:26] thereby build out a new freedom that comes from creativity, innovation, and market action. G'day, g'day.
[05:45] Welcome to Incubator Weekly. Hi, Rion.
[05:47] Hi, AJ. How are you?
[05:49] Blue. Morning, everyone.
[05:51] I'm coming at you live, as AJ would always say on his streams, from Pioneer Day. Actually, all three of us are coming at you live from Pioneer Day.
[06:03] In the state of Utah, in the United States of America, we have what's called Pioneer Day, and it celebrates the Mormon trek into the territory of Utah.
[06:17] These people had to walk across the vast plains of the middle part of America and settle down in this valley that was basically completely dry, completely uninhabitable, but they made
[06:37] a huge city. It's now a huge city of, I think, probably two million, at least, people in Salt Lake
[06:44] City and down across the Wasatch Front, and I'm in the Wasatch Back, the mountain valleys on the backside, and I just wanted to mention that because I view Dash as another set of
[06:59] pioneers where we're basically, like, we have to go through extremely hard times crossing the plains of a new territory and completely found a new financial system, and I think
[07:18] that we'll find that this is, we'll look back, and it was what guys helped me out probably almost 200 years ago or something like that, is 1847, that Utah was just, like, re-founded
[07:34] again by the pioneers. So yeah, hopefully it doesn't take us that long.
[07:40] Maybe cut that in half, or cut that by 10, and maybe say 20 years from now, we'll look back and we'll have millions and millions of people using the Dash cryptocurrency.
[07:50] I can sign up for that. How about you, AJ?
[07:57] We'll see. Oh, well, it depends on us, right?
[08:01] We'll see. AJ, would you...
[08:03] The best way to predict the future is to create it, right? Yeah, I don't know what's going to happen, but I am trying to build things to help make
[08:13] stuff happen. Exactly.
[08:15] Well, that's what it seems, and that's what brings us here today, which is to discuss a whopping four dips that you have submitted to the Dash core repository within, I believe,
[08:28] the past month, AJ. And so without any further ado, shall we jump into those?
[08:36] Yeah. Okay.
[08:39] So the first one, I will go ahead and get pulled up here. It is called Define Mixing...
[08:47] Define Tracking. Let me go ahead and get this going here.
[08:54] Oh, yeah, yeah, yeah. HD Mixing to Define Mix Tracking.
[08:58] So, I don't know... So, what is that?
[09:00] Firstly, from a high level, what is that? Okay.
[09:05] So, there's only one wallet that I'm aware of that supports CoinJoin, and you've heard my criticisms of CoinJoin, but also, you know, it's better than nothing for certain use cases.
[09:21] And the way that it works in the Dash wallet presently is, and this is actually really scary.
[09:30] So, a lot of people don't know this, but if you just use Dash core without any tweaks to the configuration, it makes a lossy wallet.
[09:38] It generates all keys independently, it's not an HD wallet by default. And every time it needs to generate...
[09:46] It basically pre-generates a cache of 1,000 keys, and then when CoinJoin's turned on, it uses those keys, and if you've used CoinJoin, you've likely encountered where it pops up
[09:58] and says, "Needs to generate another 1,000 coins." And at the code layer...
[10:07] So this is bad for a few different reasons. One is, if you're actually trying to use the money...
[10:18] Say you wanted to share a CoinJoin wallet with your mobile wallet, it'll actually... Well, I don't know if it still does, but as of six months ago or so, if you tried to do
[10:25] that, it would crash the mobile wallet, because the mobile wallet was built to only handle a couple hundred transactions, and CoinJoin will make thousands.
[10:33] When you share the... Put the same seed into your mobile wallet as came from your Dash core wallet, that would
[10:40] cause a crash on the mobile side? If you're using CoinJoin, yes, because the mobile wallet can only handle a couple hundred
[10:47] transactions, and CoinJoin will generate thousands of transactions. And then it'll also be confusing, because it looks like a spend to the mobile wallet,
[10:55] because the mobile wallet doesn't have the software logic in order to interpret it. So what this does, it says, "Okay, look, first, we need to be using HD wallets by default."
[11:05] Well, that doesn't say that, but that's just... That's a given.
[11:09] We need to be using HD wallets by default. HD wallets have a path.
[11:15] So you'll notice that there it says M4450, and those all have apostrophes next to them, and then 00.
[11:26] And then the next one is, at the end, 10. And then there would be 20304050, all the way on to 160, and then potentially past that.
[11:38] So CoinJoin, the maximum number of mixes is 16. So we have this place in an HD path that designates what type of HD path it is, what coin it is,
[11:51] what account or contact that it's for, and then what the usage of it is. And usage traditionally has either been you're using it as a receiving address, or you're
[12:01] using it as a change address. Well, CoinJoin fits really nicely into this, because the change address could be mixed
[12:12] one time. And then the one meaning change is the way that it's presently used.
[12:18] But we can just add a two, and that means that it's mixed two times. So on to 16, that means that it's mixed 16 times.
[12:24] So this way, we can define in software how to track that the coin's been mixed. Something like the mobile wallet would know, oh, I don't need to, well, there's also other
[12:37] ways this can be done too, but I don't need to show all of these things as transactions from one to 16 for a CoinJoin-enabled wallet.
[12:47] I'll just know that those are mixing processes, and I don't need to show them all. And so this is just a really simple way to kind of take the thinking out of, how would
[13:01] we get this to work? It's not a complex problem.
[13:03] We already have a method that we use for wallets. We already have a place that has been used for something similar within the HD path,
[13:15] that starts with M and has those numbers in it. So this is just a finding, hey, this is the way that it can work so that we could have
[13:25] that unambiguously be the way that we determine that something's fixed. There's another problem though.
[13:34] So the Dash Core wallet does not actually track back, or I mean, sorry, it does not actually keep track of how many times a coin's been mixed.
[13:43] What it does is it looks at the previous coin and checks the value of it, and then looks at the previous coin and checks the value of it, and looks at the previous coin and
[13:50] checks the value of it, all the way back to the denomination event. And that's how it determines whether something's been mixed.
[13:56] So it doesn't actually know whether, there is no signal as to whether or not something is mixed.
[14:02] And this is why that when CoinJoin spins it, it unmixes it, which is ridiculous, right? Are you talking about, just let me back up for a minute.
[14:11] What you're saying is, my understanding of, like, I haven't really looked into how CoinJoin is tracking how many rounds, but I would have assumed that it's some kind of state variable
[14:21] within the wallet software of- That's what I would have assumed, but it isn't.
[14:25] Okay. And I don't think we need to get into the details of what it actually is, but what you're
[14:31] suggesting is, let's keep that state right within the path, the HD path, so that it can, the state can not only be in a wallet, but it can be in the HD path itself.
[14:47] So you can share it across devices, is that what you're saying? So I don't want to say so that you can share it across devices, because the use case of
[14:56] this is beyond that statement alone. A side effect of this is that you could make it easier to share across devices.
[15:08] But if there's no changes to the wallet software, this wouldn't make much of a difference. It could, if we took the existing wallet as it works now, and we took this strategy, then
[15:20] it would only see non-CoinJoin coins, and it wouldn't see CoinJoin transactions. Now are you also saying, what would be required for Dash to accept this dip?
[15:35] Is this a wallet-based dip? Is this a best practices standard that you're suggesting, or does this require any kind
[15:42] of protocol changes? Well, that's a matter of interpretation.
[15:49] I would say there needs to be a protocol change in that, well, not a protocol change on the blockchain, no.
[15:58] But Dash Core should be maintaining state of when something is mixed because as it stands, it will unmix coins to denote that they've been fully mixed, which is kind of absurd.
[16:14] So once your coins are fully mixed and you send them to someone else, it unmixes them. It combines them all back together in the send.
[16:22] And so there's some, and that's, this whole string of dips addresses in various aspects, either these user experience issues or these security flaw issues.
[16:35] Okay. And I wanted to get this on air because there was some confusion in the Discord a little
[16:41] bit ago about what you meant with security issues. And I made it clear in Discord that when you say security issues, you're really talking
[16:49] about what a lot of other people in the Dash community would think of as privacy concerns or privacy improvements.
[16:59] And so when you're saying, let's fix the security issues, you're saying, let's improve the privacy just by different terms.
[17:08] And I agree that those two are essentially synonymous in the sense that if your blockchain or your currency in general is leaking information about that can be potentially personally identifying,
[17:24] then that is a security concern. And that's exactly what we should call it.
[17:29] And that's even a less controversial way to talk about it because fixing security issues is definitely, you know, everybody would agree that you should always fix security issues.
[17:42] Yeah. So to be clear, this particular dip is not in and of itself a sort of workaround or hack,
[17:50] if I dare say, to get the core wallets mixing function to translate directly into mobile, but rather this is part of something that maybe would make more sense in context as
[18:03] we look at other dips. So this is just a strategy to solve the existing problem with how to track the CoinJoin in
[18:13] a way that is going to be easy. If we implemented it today in Dash Core, then Dash Mobile would work better.
[18:23] But Dash Mobile doesn't have any support for CoinJoin, which is silly because I think because people have stuck in their heads like, oh, the only way to implement CoinJoin on mobile
[18:34] is to have everything about it implemented on mobile. And this won't work because of the way that it has to use background process, like all
[18:41] this technical garbage, right? Which is true in a sense.
[18:45] You're not going to have the luxury of finding a way to make that app stay open or to force its background processes to take priority over a period of days in order for CoinJoin
[18:59] to work. That's perfectly feasible, but you don't have to do the mixing on the device that spends
[19:09] the money. So if all we did was make a minor update to the mobile wallet and make a minor update
[19:18] to Dash Core, because Dash Core does have the ability to use HD wallets, it just doesn't do it by default.
[19:24] And the mobile wallet uses HD wallets by default, but it doesn't have any ability to understand CoinJoin.
[19:31] So this would be something that bridges that gap. But also, yes, in the broader way of things, as I've worked in the various Dash tools,
[19:44] between mobile, Dash Direct, Dash Core, some of the developer tooling over the past couple of years, these are the things that, Rion and I have had conversations about all these
[19:56] things. I've had conversations with other developers about all these things.
[20:00] And this is just formalizing it to say, hey, after, not just, okay, initially I said, well, this is an obvious way to do it.
[20:08] Why not do it this way? This is actually, okay, I've implemented code that does some of these things this way, not
[20:13] particularly the CoinJoin, but among the devs. So I know that it actually works.
[20:19] I've seen other standards. I've got more exposure.
[20:22] So now, rather than just being like a pesky brat, know it all, I'm a pesky brat, know it all, that has the experience to back it too.
[20:33] A pesky brat, do it all is what- Yes. So let's say the worst case scenario, everybody ignores this, except for our little team here
[20:44] in the incubator. This basically will then, we can use this as a blueprint and say, whatever DCG does
[20:54] with their core wallet and with their mobile wallets, fine, take it or leave it, but we're going to use this so that we can build a mobile wallet that does mixing.
[21:07] Yeah, and so in the wallet that we're working on, yeah, Dash Core has DIP 14 and DIP 9, and DIP 9 is not really a specification as much as it is a specification for specifications.
[21:22] And then DIP 14 is actually a specification for HTWallet. They don't address this.
[21:28] And if Evo comes out at some point, we can be backwards compatible with that. But this is a simpler alternative solution basically to DIP 14 as well, well, not this
[21:45] in and of itself, but one of the other ones. So yeah, we can use it in ours, and then that doesn't preclude us from being able to use
[21:52] theirs if there's ever live code for that. Great.
[21:56] So should we look at this then in the context of the other ones that we're looking at today? Yes.
[22:02] Let us have a little view here. Okay, so next we are going to DIP 134, which-
[22:10] Well, PR 134, they don't get assigned numbers until they are approved. Excuse me, PR 134.
[22:19] Yeah. Okay.
[22:21] So, please. Canonical deterministic wallet and XPUB IDs.
[22:27] So when you are sharing contacts in particular, there's two pieces to a contact. It's like you can follow someone and they can follow you.
[22:40] You can share ability to pay to someone, and they can share ability to pay to you. In the case of a business, typically it's just one way.
[22:50] It could be two way because you could occasionally have refunds or something like that that they need to send you money back.
[22:55] But typically in the case of a business, it's one way. They're going to share an XPUB with you, which is an unlimited, well, a set of up to 2 billion
[23:06] addresses, an XPUB that corresponds to up to 2 billion addresses. So essentially unlimited.
[23:12] And you, every time you go to pay them, you're going to use preferably multiple addresses because preferably you wouldn't be unmixing your coins.
[23:23] You would just be sending your coins with whatever's needed to pay them. But in the worst case scenario, you're going to be using one address per payment.
[23:33] And that- - Let me know if you want me to show the preview also.
[23:37] - Oh no, you don't have to worry about the preview. I think the stuff that's in here is probably better than that.
[23:42] That's a bit longer. And then you also have your wallet phrase, also known as your recovery phrase, but recovery-
[23:49] - Seed phrase. - Yeah, seed phrase is a technical term.
[23:53] I am not really aware of anybody that uses it that way, but yeah, it's also called that. Rion and I have had, and Joey, we all have been debating about what to call this phrase
[24:02] thing because all the UIs on the phones call it recovery. Nevermind.
[24:08] Anyway, but this is important in that you may want access to more than one wallet on your phone and you definitely need access to more than one contact.
[24:20] And so you need some way to be able to reference these in the code. You need an ID.
[24:26] And so this provides a super, super simple, secure method of generating an ID that's short enough that it will neatly fit into a database, is easy to index.
[24:37] - Like this one here? - Yeah.
[24:41] - Okay. And let me also just back up a little bit, just in case people are wondering while you're
[24:47] talking, is this in any way related to Dash Pay, Evo, contacts that we've been working on for seven years?
[24:58] How is this related and is it compatible? Is it different?
[25:02] Is it an alternative? - It's an alternative because I've looked at, I don't remember which dip that was.
[25:07] I think that was dip 14. And they've got a way of doing it that kind of makes sense, but it kind of bends the rules
[25:13] of the existing software in a way that you can't just use existing software. You'd actually have to make changes to existing HTPath software.
[25:22] And I haven't gone deep enough to fully understand why they've taken the route they've taken exactly the way that they have, but they have a different way of doing this.
[25:32] This one is a way that works with the way that everything already works. So the way that all HD wallets already work, the way that the standard has already been
[25:42] defined, it's actually in the use case of BIP 32, I think it is. It's hard to remember numbers.
[25:47] I've never been good at that. I always failed those exams in class when they're like, which constitutional amendment?
[25:53] What does the number have to do with it? What the thing does?
[25:55] Why don't we call it by its name? - Yeah, BIP 32 is the description of HTPaths in general.
[26:02] And I think BIP 44 is a very specific type of that generally. So I believe that it was BIP 32 that describes HTPaths that actually lays out how to use
[26:13] an account for relationships. And it talks about it in the case of businesses and departments and businesses that do business
[26:21] with each other, but you can easily say, oh yeah, well, a business that does business with other businesses is the same as a person that has transactions with other people.
[26:29] So if you look at the use case given in BIP 32 in the context of BIP 44, then you can say, oh yeah.
[26:37] We just use the account as the contact as described in the BIP 32 use case. And we can use things that way.
[26:49] Now, what this does is it just says, we're going to take a wallet phrase. We're going to do the normal existing process.
[26:56] And we already have the code for this for the browser in terms of what we've done with the dash incubator dependency.
[27:02] So dash phrase, dash HD, dash keys. So we're going to take the wallet phrase.
[27:07] We're going to turn it into a seed. We're going to take the seed.
[27:10] We're going to turn it into an HD key, the root HD key, the root wallet. And then we're going to run a secure hash on that, truncate the first few bytes.
[27:20] Now in BIP 32, they do actually give a way for getting the ID of the wallet, but essentially in the BIP it says, this isn't secure and results in conflicts, don't use it.
[27:34] And it also uses a hash algorithm, which is now known to be insecure. And so this just does it a little bit differently so that it will, it's actually @_, oh, on
[27:50] GitHub. Okay.
[27:52] If you want to connect with me, the best way is actually @coolage86 on Twitter if you want my hot takes or @_beyondcode if you want my tame and my alter ego that's the better ego
[28:04] anyway. So this, this does that conversion to the root wallet and then uses more of the information
[28:12] because in BIP 32, it only says to use the public key, but that I don't feel like that's actually descriptive enough considering what is contained in a wallet.
[28:23] And then, but yeah, but it's, it's, it's a really simple everyday basic operation. Any programmer could do this if they couldn't do this.
[28:33] They're not worth their salt. Every, every programmer should be familiar with how to take bytes, pass it into a function,
[28:39] a hash function, and then truncate the bytes that you get out of it and then run a base 64 conversion.
[28:44] That's all this is. It's like a three-step process.
[28:46] Now the process of getting from the seed to the, or from the phrase to the seed, to the HD key, that's not something every programmer is going to do, but we have the tools for
[28:54] that. So there's, you know, those tools already exist.
[28:57] And then actually this now exists in dash HD as well. And then the same process applies if you're given an X pub, it's the same process, except
[29:05] that you're not deriving the X pub, you're just taking the, the HD key that represents the X pub.
[29:11] You're going from X pub to HD key. And then you're, you're running that same process where you're, you're taking the byte
[29:17] string of that HD key, hashing it, taking the, the, the first, I think it was 60. So in synopsis, could we say that this is like an alternate implementation of what could
[29:32] be considered usernames? No, no, no, this is, this is, this is for internal stuff.
[29:40] A user would never see this user would never see this. Okay.
[29:44] Yes. The reason that we need this is because if you are going to be syncing and sharing things
[29:48] between devices, or if you need to back up your contacts, there's been some criticism about do I really want to publish all of my information to a third party rather than keeping
[30:00] it with me and my devices? You know, so this is, if you are going to develop some strategy, we need the strategies
[30:06] to be compatible. And the idea is something that BEP 32 makes very clear, Hey, don't actually use this.
[30:12] This is just an example. And then we don't have something else for creating those IDs.
[30:17] And this is something that's simple. That's, that's a kind of common practice just applied to this specific use case.
[30:24] It's technical, it's implementation details. It's for caching and syncing.
[30:28] Got it. What other, what other dips are we covering today?
[30:32] We got two more. Okay.
[30:35] Let's move it. All right.
[30:37] Offline first contact payment subscription exchange. So that's a good way to go.
[30:42] This is super, super simple. this one, you should click on the preview. Okay. I'd say super, super simple. It's easy
[30:53] to explain. The implementation details are actually not as easy, but if see, for example, right there. So scroll that up a little bit so we can take a look at it. Um, no, up the
[31:04] other way. The other up. Yeah. That one push, push the page up. There we go. Yeah. So we, we can see that example, that big string of dash colon, blah, blah, blah, blah, blah, blah.
[31:16] So this is what the QR code looks like when you decode it presently. So when you have a QR code, it starts with dash colon and then an address and then some parameters. And that
[31:29] string is just, is just encoded into a QR code. So QR code is the same as text. It's just representing it in a way that before, before, you know, now, nowadays on the phone
[31:40] in the last year, all the phones now have, you know, like you can take live video and copy text out of it. Right. But that didn't exist until this, this past year. And so we
[31:49] use QR codes to put text in a format where it was easier for the computer to read it in a way that's, that's unambiguous. So if you're familiar with scanning the QR code,
[31:59] that's what it looks like. It looks like this. And so what we're saying here is, Hey, uh, we need to be able to put an X pub in the QR code rather than a single address, because
[32:10] that is essentially what a contact is. It is an X pub represents a possible 2 billion addresses. And so that's good enough for a contact in an X pub could represent a contact
[32:20] holistically right now, the way that things are currently used an X pub represents a particular device of a contact. So you would actually have multiple X pubs for a contact, depending
[32:31] on whether you're going to pay them to their phone, or you're going to pay them to their desktop, or you're going to pay them to their work phone versus their home phone or, or,
[32:39] or whatever. Right. And this is why we need IDs for X pubs so that we can differentiate multiple X pubs with a contact and multiple wallets where you might have more than one
[32:50] wallet phrase you want to check for money or whatever. Anyway, so it's just a URL. And this defines a couple of things. You can see the prior art section there. If you push up,
[32:59] there's a whole bunch of these because both in the private sector, as well as in the big B space there's been a lot of work in defining these and good work. And you know, I'm highly
[33:13] critical of things in general. Not all of this is great, but a lot of it is good and some of it's great. And so these specifications are specifications that already exist. Some
[33:23] of them, we kind of follow some of them, we kind of don't some of them are generally followed. Some of them generally aren't, but this is just taking a bunch of standards and saying,
[33:33] okay, we should be able to represent the URL in HTTPS form as well as dash form. Because if somebody doesn't have the dash app, we should actually have a way that they can receive
[33:44] money without having the dash app. They should just be able to use the QR scanner on their, on their phone and be able to receive money, right. Or receive a contact through, through
[33:53] a webpage. And then that could incentivize them to go get the app or that could redirect them to the app. So there needs to be a way that if they don't have the dash app, and
[34:01] this is what I would prefer is that we kind of ditch the dash colon and just go with using HTTPS URLs that, that then could redirect to the dash app as needed. But regardless,
[34:15] we need both ways. And then we need to be able to define, okay, this is the X pub. And then there's a standard called OIDC that defines basically contact information. So things like
[34:25] nickname, profile, profile picture, additional data that you would, that you generally would exchange with a contact in the way that you would usually exchange it. And the standard
[34:40] isn't a hundred percent for our use case, but it's close enough that, yeah, there's one or two things that we need to tweak from it. And that's defined in here. But with those
[34:48] tweaks, we use a standard way to share contacts that already exists. That's already well-known that other software already pretty much understands. And we add a couple tweaks so that, you know,
[35:00] X pubs are not part of any contact standard, right? Cause that's, that's purely in the blockchain space, but you know, we add the X pub to it. And then we add also the denominations,
[35:11] which is another thing that's related to X pub send. I actually created the X pub send depth so that I could go back and finish this dip and then reference that when I'm talking
[35:20] about denominations, but that's what, that's all this is. It's just, here's how we define a URL that has contact information that you could scan it. And then of course, what you'd
[35:28] want is that the software, if you scan someone and they click, okay, then they should, they should immediately be given the QR that you can scan back. And so then you mutually share
[35:39] the contact information if that's the way that it goes. So, you know, if you think about all the contexts in which you want to share a contact with someone, you already have a
[35:48] medium of exchange. You're already texting them or you're emailing them or you're with them. You know, we don't, we don't generally send payments that can't be reverted to people
[35:59] that we don't trust and have no way of contacting. So this is a simple way to do it that works with the software that's already out there with standards that are already out there,
[36:09] both standards in the normal commercial space, as well as standards in the blockchain space with just a couple of tweaks for our, our particular use case. But it's, it's just really
[36:18] well-defined standard stuff. Nice. Okay. Um, how much scrolling is there left on that page? Maybe we just finished
[36:27] that out and I already explained all of this, you know, I mean, you can scroll through it if you want. I mean, just so that just really quick so that people can read it without having
[36:35] to click through a link. Um, if they're already watching this, um, all right, so what's the next step then it's, this is the last one, right? Yeah. Okay.
[36:47] So otherwise known as cash, like denominated, send. Okay. There we go. And this also does tie back into the first one that we went over, which was that, that, uh, significant digits
[37:11] and how many significant digits last week. Yeah. Yeah. So the, the, the basic idea of X pub send is that traditionally, um, Oh man, these words have been so minced, but okay.
[37:25] Old, old, old, old, old school. A single address was once upon a time called a wallet before we came up with the term HD wallet, which now we just dropped the HD and we just call
[37:37] it wallet. Right. But back in, what was it, 2010 or 11 or whatever, when they first came up with addresses, because before addresses, there was just like hex codes and then, then
[37:48] they developed addresses and so on and so forth. But, um, so that, that's the heritage that we inherited. And so when they came out, the HD wallets, they wanted to be backwards
[37:58] compatible with that. So they would use one address at a time from the HD wallet. The problem with this, especially in our community with dash is that if you send money to a single
[38:10] address, you are unmixing that money. This, this is a security vulnerability. You are leaking data, right? So when, when Rion sends a payment to me and Jojo and will, and, and
[38:23] I think you pay Ash and then Ash pay someone else, or I don't know exactly how, you know, what your process is, but, but you, you do it in the most charitable way possible with
[38:34] the current software you have, which is that you send everybody's money in one transaction. So if somebody were to inspect that transaction, it's difficult to say which money is going
[38:47] to who just by looking at that transaction alone, because you've got multiple people in there, but you could tell by the amounts, what address is receiving, what, if you know
[39:00] the information about, you know, the, the basic range of, well, this person's working this much at this, you know, this person's working that much, this person's claiming
[39:08] this task, whatever. Yeah. It's all recorded on a spreadsheet. We do that intentionally, but most people
[39:13] don't want that information shared. Yeah. And I don't want that information shared, but not, but, but, but just the scenario,
[39:22] you know, take away our specific use case for a second that it's all public anyway, but then just the scenario, you still glean information about that. So if instead we were
[39:30] to send the denominated amount, so let's, let's take CoinJoin as an example, which it doesn't really work because it, it limitations in it, but let's, let's just pretend for a
[39:41] second that you could resend a CoinJoin coin, which theoretically with a few changes, you could without unmixing it. Well, then I'd see a bunch of tens and a bunch of ones and,
[39:53] and maybe a couple of hundreds and that's what I'd see. And then from that, it'd be very difficult to say, okay, which of these tens are going to which person, they'd be
[40:02] very difficult to aggregate it together. You know, not, not ultra difficult, not like the FBI couldn't figure it out kind of thing,
[40:11] but if you, if you were to send to multiple addresses, you know, to each person's X pub, you send denominated coins and we'll use CoinJoin as an example to multiple addresses and you,
[40:23] you just send those coins, then it's difficult for somebody to reverse that. And if you do that all the time, we've got a term for that. What is it? What is it when you just send
[40:34] to denominated coins over and over and over again, incessantly? What, what, why am I, oh, CoinJoin, right? So what if it's just part of the payment protocol rather than unmixing
[40:46] the coins so that when you send it to someone, somebody has to mix it for a day? What if you just don't unmix the coins in the first place? And that is what X pub sends.
[40:55] In other words, every send is a CoinJoin, but every send is a, is a denominated transaction. Every send is a quote unquote CoinJoin transaction in a sense.
[41:08] Yes. Yeah. And, and so tying this back to the first one from last week, the only way that we can reasonably do that is if we can kind of agree that fees are symbolic, they
[41:20] don't actually generate revenue. And if they did generate revenue, they'd be way too high. And then nobody would want to use Dash for cash because you'd be paying just as much
[41:27] as fees as you pay for, you know, PayPal or whatever. Right. So we, we have to, we have to recognize that the fees are symbolic and we want them to stay symbolic or disappear
[41:37] because if they, if they go up to the point of being useful, they just cost too much. And then also that we only want to bug the user with some number of decimal places, which
[41:47] again and again and again, I'm coming to, it just can't be more than three. And then if you have those other decimal places, you can use those for transaction fees. So
[41:55] I could have 10,000 Satoshis that are included in my Dash and those 10,000 Satoshis could be subtracted from and redivide every time I do a send. So they never carry any information
[42:09] about me because they're, they're protocol level at this point. And that I can send a bunch of coins and I'm not worried about like, Oh, this transaction is going to cost 200
[42:19] or sats. How am I going to eat today? You know, you're just, you're just using those, those fluff values that are left over from the legacy Big B era. That's not Dash, that's
[42:31] Big B. Satoshis are a Big B thing. They're not a Dash thing, you know? And, but anyway, so if we have an amount that we say, okay, this amount is the amount that the user cares
[42:43] about that's spendable Dash. And then we say the rest of it's just used for paying fees and adding on to coins. Then XPUB send that, you know, that, that kind of goes part and
[42:53] parcel with this because you could do XPUB send the way that we currently have it. You could implement this and it can work. You could say, I want to send whatever collection
[43:01] of coins I have that add up to about the amount that I want to send. And maybe I want to get changed back and maybe I don't. And it would look really, really beautiful with XPUB send,
[43:11] but it would be great and really preserve the security of not leaking user information. If we always used a denominated send for everything, we never unmixed things that had been denominated.
[43:23] We just left them denominated and let them continue to mix as they change hands, just like normal cash. And we, yeah, I mean, that's
[43:34] If and when this was ever implemented, let's say to a large scale so that you could kind of if it were implemented on a large scale, basically what you'd see on block explorers
[43:44] is every, every inputs, every, every series of inputs would be denominations of ones, tens, ones, twos, fives, tens, twenties, fifties, one hundreds, and so forth.
[43:59] That's what I'm suggesting. We could do it with coin join. If we made the change I'm talking about where the last four digits are reversed, reversed for stamps, which would
[44:06] require the previous dip that we put the coin join on the HD path so that you can count how many times it's been mixed empirically rather than by, you know, by a state that
[44:17] exists rather than by tracing back. But yes, we could do it with coin join or we could do it with what I laid out. I like what I laid out better because it's, it's less than
[44:24] two coins per digit on average, whereas coin join is five coins per digit on average. Or maybe the distinction that you're drawing is whether we have the twos and the fives
[44:37] sub-units between coin join and what you're, and I agree with you that, that I would, I would prefer to see ones, twos, fives. This is how most, most bill systems work in the
[44:49] world. I mean, the United States isn't totally compliant with this, but like if you go to Europe, then you see, you see one euro, two euro, five euro, 10, 20. And you know, the,
[45:05] the United States has a lot of those, but not all of them. But I, I think that they're the, they're the correct balance of, of denominations where you have, well, the way we come up with
[45:17] those numbers is from the lizard brain. Yeah. It's the doubles and halves. Yeah. It's from the fact that we have to determine, is this group larger than ours or smaller than ours?
[45:26] Are there many tigers or are there very few tigers? And so it is, it is doubles, wholes and halves is what it is because five is half of the next order of magnitudes double. So
[45:37] when you look at an army and you're, or, or a group or whatever, you know, if you go back to our tribal brain from a million years ago, you're trying to quickly determine, is this
[45:49] much more or much less? You're not, we're not, our brains aren't optimized to be able to look at a group and say, yeah, that's about 127 people. It's like, is it a hundred people
[46:00] or is it a thousand people? Is it this order of magnitude or this order of magnitude or is it in between? And that's why, that's why we do that with money too, is, is our brains
[46:08] are optimized for logarithmic scale of doubles, wholes and halves. I think we've covered the dips then at least at a surface level so that people can look
[46:17] deeper into this. But what I'm seeing from the big picture is you've come up with concepts of wrap together the concepts of paying by paying to users, making username connections,
[46:40] making private transactions within those users. And in a lot of ways, it's different alternatives to some of the tools that we already have and are already building, but in a much more
[46:54] simple backwards compatible way is that, would you summarize it like that as well? Yeah, there are some things that are not depending on your definition of backwards compatible
[47:05] or some things that are not entirely backwards compatible. Yes. The idea is that it progressive enhancement would be the term that I would use. Because if you want to make a big change
[47:17] to a system, you've got the waterfall approach and you've got the agile approach. The waterfall approach is you're going to design all aspects of the system. And before you prototype it,
[47:27] you're going to build the whole system altogether as one unit. And then you're going to treat that as your prototype after potentially years of development. And the agile approach is
[47:37] you're going to say, well, dag nab it to get to where I want to be from here would take a long time. What can I use about the existing system? Use or abuse about the existing system
[47:49] that with a small change within next week or next month, I can get one aspect of what I want out of the bigger system. And if you do that repeatedly, you can get to a point
[48:00] where all the aesthetics of the bigger system have been prototyped and implemented. And then you have two choices from there. You can say, okay, the little collection of hacky
[48:10] do's that we've done actually resulted in something that's good enough that we can use it. Or you can say, well, this has been a great prototype. Now we know all the constraints
[48:19] of the system. Let's go ahead and build that bigger monolithic change, but it's not going to be a system shock when it comes down the pipe, because we can run these two systems
[48:30] in parallel and they're both going to have the same aesthetic from the user perspective and perhaps even the same aesthetic from the developer's perspective. But the one system,
[48:40] the bigger monolithic system is going to be better because it's been optimized rather than a bunch of hacky do's, but you already know what the constraints of the system are,
[48:49] how it works and how people react to it. And so this is taking the agile approach, which agile is such an abused term. So I hesitate to use it because it doesn't, it means what
[48:58] is in the agile manifesto as uncle Bob Martin and his coworkers, you know, put out on the internet, not these books that are, you know, a hundred chapters thick with certifications,
[49:10] but just the idea that you're going to iterate on customer feedback and you're going to take small steps from where you are to get to where you want to be rather than branching off into
[49:19] something completely new and different. Gotcha. Okay. I just wanted to mention one thing real quick at the end here, we're coming
[49:26] to a close, but there is at least one more dip that we have discussed. You and I, AJ, we actually, I brought it up and we discussed it years ago, but it sounds like we're at
[49:40] the cusp of making that. And that's basically a dip to provide a specification of how you could say as a masternode owner, I want to, and I can provide X, Y, and Z services to
[49:59] the network. And I want to opt into this and potentially even set your own prices. And so instead of like, basically what we have with, with evolution and platform is we have
[50:12] one big, one big service that everybody's kind of doing. And it's, it's a mandatory thing for at least the evolution nodes. And what we want to propose is something that's
[50:26] more modular and more granular and say, but, but, and also more scalable and say, Hey, I'm a masternode owner and I want to provide X, X service, like maybe imagery sizing.
[50:38] Yeah. That's a perfect example too. And we charge dash for that. And it's a very simple thing and not the whole network doesn't
[50:46] need to run it, but maybe a quorum of 10 nodes or something like that, that, that randomly selected and each node all those 10 nodes run it. And if they come to the same conclusion,
[50:58] then you can say that that service is that that's legitimately done or something like that. We, we haven't gotten into the details, but I think that's something that I want to
[51:07] talk about more in detail and in a, in a later episode on, on incubator weekly, definitely not right now, but I just wanted to kind of introduce that as something that we have in
[51:18] the works. Yeah. And that one is, is much higher complexity in terms of, you know, we'd probably need
[51:25] to break that down in the three or four dips, but the simplest aspect of it would be, we already have an RPC to get the list of masternodes. So let's add or modify the RPC so that we
[51:37] can have keywords, say image resizing. Let's say that we actually decided on that as the keyword, but we could query, give me masternode list filter by imagery sizing. And then it
[51:49] would give me a list of masternodes that did imagery sizing. And the simplest approach would just be to say, okay, I'm going to pay three of you to do this task. And then I'll
[52:00] just compare that the results, the same, I'll just pick, I'll just pick three at random. I'll pay you to do the task. I'll check the results the same. And then, you know, there
[52:09] we go. Well, I look forward to hearing about that dip in a future episode, or it may be a PR
[52:16] at the time, AJ. And yeah, I, I, my main takeaway from the presentation of today's dips is a very, a sense of a strong, like juxtaposition, like on the one hand, hearing about these
[52:31] PRs, you know, just almost like gives me cancer. But then on the other hand, when I envision actually what you're talking about, as far as how the user would, and even to a sense,
[52:43] the developer would have a changed experience with the implementation of one or more of these, there's a real empathy there for just like, yeah, what, what feels natural to the
[52:56] mind, what feels natural to just what we're used to. So I guess all told, I'm just excited and glad that you've taken the time to work them out and submit them AJ.
[53:06] And this is going to be useful in dash incubator, because now we have shared reference material to go off as we prototype more of this out in a way that a user can experience it, not
[53:17] just down at the library level where I've mostly been working. Exactly. I was just going to say that I can imagine a lot of people probably don't really
[53:25] understand much of, of what we've been talking about, because there's just a lot going on and it's highly technical and highly technical, but most people don't know how the HD wallet
[53:34] works presently. So to describe a modification to that is the nice thing is that, that we're, we're going to be basically implementing these like incubator itself is going to implement
[53:46] these dips so that you can basically just experience what, what it is instead of having to process this and think about like, should, should we do this? We're, we're already doing
[53:58] this. And so when we're done with that, I think we'll, we'll circle back and say, okay, we implemented this dip on from the incubator and now other wallets can, can consider it.
[54:10] Yeah. Right. Okay, good. Well, that has been it for us today and we look forward to seeing y'all next week. All right. Bye.