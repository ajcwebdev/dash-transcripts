---
showLink: "https://www.youtube.com/watch?v=eWFV3-ytN8o"
slug: "dash-maya-integration-update"
title: "Update on Dash-Maya Integration"
publishDate: "2023-06-19"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/eWFV3-ytN8o/maxresdefault.webp"
---

Alux from Maya protocol discusses Dash integration, liquidity nodes, and future plans in a technical conversation.

## Episode Summary

tl;dr: Alux shares updates on Maya protocol's progress, including the upcoming Dash integration in version 105 on stagenet, the transition to liquidity nodes, and future plans for features like lending and streaming swaps. He also discusses the importance of front-end integrations and encourages the Dash community to participate and voice their needs.

## Chapters

00:00 - Introduction and Background on Maya Protocol
Alux provides an overview of Maya protocol's progress since its launch, including stabilizing the network and preparing for the Dash integration in version 105.

03:41 - Stagenet and Testing Environments
Alux explains the different testing environments used by Maya protocol, including Mugnet, Testnet (retired), and Stagenet, and how they facilitate testing of new features and integrations.

09:11 - Front-end Integrations and Incentives
The conversation covers the role of front-end integrations, such as wallets and user interfaces, in the Maya ecosystem and the incentives for developers to create these integrations.

13:21 - Handling Bugs and Reimbursements
Alux addresses how Maya protocol would handle potential bugs and reimbursements for users, emphasizing the importance of maintaining trust and supporting liquidity providers.

16:37 - Future Features and Roadmap
The discussion moves to upcoming features for Maya, including lending, streaming swaps, and the addition of more chains and smart contract layers. Alux also compares Maya's approach to that of Thorchain.

22:28 - Dash Masternodes and Liquidity Providing
Rion and Alux explore the possibility of combining Dash masternode rewards with liquidity providing on Maya, discussing the technical limitations and potential solutions.

25:28 - Estimated Timeline for Dash Integration on Mainnet
Alux provides an estimated timeline for the Dash integration to go live on the Maya mainnet, emphasizing the importance of thorough testing and the potential lag time for front-end integrations.

28:37 - Community Involvement and Support
Alux and Rion discuss what the Maya and Dash communities can do to support the integration, including using the protocol, providing liquidity, running nodes, and promoting the project to others.

## Transcript

[00:00] Meet Hassan. While a youngster growing up in Syria, his grandmother would each year send him a birthday card. He cherished the personal notes scribbled on the card, as well
[00:10] as what was inside the card, some money. Though it wasn't much, it made a big difference in his life, giving him options. Fast forward to today, Hassan is now living and working
[00:18] in Brazil. He and his grandma are still in touch, but now he's the one who sends her mail. Specifically, he sends money home every week, which she relies on to cover her living
[00:26] expenses. And they're not alone. In fact, 1 in 9 people worldwide rely on money sent home by loved ones working abroad, an act known as remittances. Globally, it's a pretty
[00:34] big deal, amounting to $626 billion in 2022. If we're talking crude, nation-state-based data like GDP, that figure would make it the 24th largest economy in the world, larger
[00:45] than that of almost 90% of nation-states. Traditionally, a person sending a remittance would physically go to an agent of the company, provide the money to be sent, the money to
[00:52] cover the transaction, their information, and the information about the intended recipient, usually involving regime-issued identification. What likely started out pretty innocuous,
[01:01] just to ensure the money got to the right person, has nowadays proven to be a place rife for data collection and surveillance. Regime actors want to know who is sending
[01:08] what and how much to whom. They set maximum limits or outright prohibitions, depending on the location of the intended recipient and the political climate of the day. On top
[01:17] of that, transactions tend to be rather slow, averaging 5 days for resolution and sometimes up to 3 weeks, and the average remittance fee is over 6%, an amount that translates
[01:25] annually to tens of billions of dollars. And because the recipient needs to go to a specific location to pick up money, they may be targeted by muggers. It's no surprise, then, that this
[01:33] model is facing increased competition from fintech startups and other actors in the digital remittance space, which enables individuals to use an app rather than physically going
[01:42] to an agent, and which promises faster transactions and lower fees. For example, AZA facilitates remittances within Africa. At 48 hours, their rapid settlement is better than the global
[01:52] average, but it still takes 48 hours. Centralized blockchains Ripple and Stellar have partnered with establishment players, and even Bill Gates has gotten into the act. His endeavor, Mojaloop,
[02:01] looks to create payment systems to enable digital financial services for all, which sounds great on its face, but it, like all the others, is just a shiny version of legacy
[02:10] remittance companies. They are still centralized, they still act as gatekeepers, they still collect information, they still line up policies with the wishes and regulations of regime
[02:19] actors, and they still command big fees. There's got to be a better option, right? In 1860, the Pony Express was founded. It slashed from weeks to days the time it took to deliver
[02:28] mail to the west coast of the US. Then in 1861, the first message was sent over the newly erected transcontinental telegraph. Two days later, the Pony Express ceased operations.
[02:37] The technological leap of the telegraph had made the Pony Express obsolete. The same is true for us today. Decentralized, blockchain-based money is a leap forward. But still, there's
[02:46] a lot of room for growth. According to Kenneth Stokowski, a payments and fintech analyst at Autonomous Research, in 2021, cryptocurrencies accounted for just 1% of the remittance market.
[02:56] But it may very well be more than that, because the total remittance market may be undercounted by as much as 50%. That is, individuals are finding means to send money to loved ones
[03:05] outside of the tracked system. This very likely includes transactions in decentralized cryptocurrency networks. And it certainly includes remittances sent via the Hawala system, which is popular
[03:14] in the Arabic world and Indian subcontinent. It relies on trust and emerged as a way to mitigate theft for traders using the Silk Road. In this system, remittances are sent
[03:23] via a network of money brokers that operate parallel to the legacy financial systems. Might this demographic be ripe for peer-to-peer cryptocurrency? And what about the 1.6 billion
[03:32] adults worldwide who don't have bank accounts, who can't receive traditional remittances via bank transfer? They too seem like prime candidates for peer-to-peer crypto adoption.
[03:41] The two biggest factors that need to be addressed for decentralized cryptos to expand their admittedly small tollhold in the remittance market are, how easy is it for the sender
[03:49] to obtain, and how easy is it for the recipient to use? Can the sender be paid in the cryptocurrency, or do they need to buy it? Can the recipient easily spend the cryptocurrency for food,
[03:58] rent, or other necessities, or pay people locally with it? These are network or scale questions. Further, what type of technology is needed? Can these transactions be facilitated
[04:07] on a feature phone? What can we do now, individually, to see this use case advance? A use case that seems so ripe for decentralized cryptocurrency. If you know anyone who sends remittances,
[04:16] have you discussed crypto with them? And if you want to go a step farther, you can inform strangers who send remittances by, say, posting flyers with information at places they're
[04:24] apt to patron. Perhaps reach out to crypto ATM operators and get their buy-in. If you attend a crypto meetup, consider broaching this issue and suggest some outreach to others
[04:32] in your community. If you want to take an even larger step, you can install a crypto ATM or solicit businesses to accept crypto directly. And you likely have some ideas of
[04:39] your own. After all, this is a decentralized endeavor. Transitioning one gig, one person, one business, one industry to using decentralized crypto rather than centralized legacy structures
[04:50] will not happen overnight. But the more this occurs, the more that real options emerge. For Hassan and his grandmother, and for so many millions of others. Options that facilitate
[04:58] the freedom to transact. You change the world with modern technology. You change the world by coding. That's that's crypto for you. This is how we can change the world.
[05:15] Hello everybody. Welcome to Incubator Weekly. We're so glad to have with us today, Rion, my cohost and I are glad to have Alux, who is the spirit animal that guides the Maya
[05:28] protocol. Something like that.
[05:32] Very good. Well, let's jump right in to the update. I know that that's that's the main thing. And and of course, we're extra glad to have Alux with us today, given that he
[05:46] had a first wedding on Saturday. Is that right? You had your first wedding and there were more to come?
[05:55] Civil wedding. Yeah. In Mexico, you sometimes separate the like the state registration of your of your wedding day and you celebrate that. And then you have like the religious
[06:07] ceremony with a bigger party later on. So just had the first part and then the religious party in October. But yeah, anyway, it sounds like you had a lot of fun. It sounds like
[06:22] you did did a lot of singing or something. Yes. My voice is not very happy, but it's still functioning. That's not something many
[06:31] of my friends can say with many of their voices. So but mine is good enough for a show or two. So we can keep it up.
[06:42] Well, you've been busy. I know that you had the Maya Twitter spaces this morning just an hour ago. So, yeah. Thanks for thanks for putting in all the time for us.
[06:54] Yeah. Anytime. Anytime. For sure. OK, so I guess let's please start with just a catch up for anybody who maybe
[07:07] only knows that, hey, once upon a time we were talking about a Dash Maya integration. Let's get that person caught up from from then to here.
[07:18] Yeah. Well, it's been a lot of work first on on my side in the sense of launching the network. We had a very good launch with raising liquidity, but there was there was a lot of
[07:33] work of getting the system stable, which wasn't easy, given, you know, the ETH Shanghai update and the Bitcoin, you know, the BRC 20 stuff with the failed mempool and fortune also constantly
[07:50] updating to address that and other issues. So we were kind of balancing a lot. It was just a lot of operations, you know, like having having the chain, the live chain
[08:03] working and, you know, kicking out swaps with our issue. So during that time, very thankful for the Dash team to be very patient with us through
[08:14] that time. But we finally had the time to actually go and include Dash in our next update, which is version 105. So, for example, version 104 was just a lot of little stuff to stabilize
[08:29] the network and little features and little details and polishing a lot. Whereas version 105 finally has probably two features we're most excited about, which is
[08:40] Dash on the one hand and liquidity nodes on the other hand. So definitely super exciting for us of having these up and running.
[08:52] We really we really would like to have it as soon as we can, but we obviously need proper proper testing.
[08:59] So we're just going through those motions of making sure that these sound stable things work as they should in order to release to mainnet.
[09:11] So speaking of mainnet and testing, I saw in the Maya Discord that the Dash version 105 has been released to Stagenet.
[09:21] So in Dash, we have a testnet that is just using, you know, you put different versions on it and it uses just fake Dash, T-Dash.
[09:36] And then we also have devnets, but I'm not sure if people in Dash understand the difference between Maya's different networks and staging environments.
[09:47] Can you tell us more about Dash being on Stagenet, what that means and what the what the path forward is towards actual mainnet?
[09:58] So, we can talk about four environments when you're talking about Maya and 4Chain, and one of which is retired and no longer being used.
[10:09] So what are those for? So first is just Mugnet, and what do we call Mugnet?
[10:14] Mugnet is when we run Maya, whatever version we want, and locally also run the other chain. So we locally run a new Dash chain from the beginning that starts mining and we just run
[10:28] all the nodes and we run a Bitcoin and we run ETH and we run whatever. So we run many chains in parallel, but all of them are run locally in the developer's
[10:38] machine. So that's what we call Mugnet, like we're mucking all of these chains.
[10:44] Then we, 4Chain used to have Testnet, and what Testnet did was go and look for like legit testnets of other ecosystems, like a Bitcoin testnet, and how is it called, Ruxton
[11:02] on Ethereum and all of those, and have like also a test environment 4Chain, so T-Rune for instance.
[11:14] But the problem with that one is that in Maya we care a lot, in Maya and 4Chain, in a cross-chain dex, we care a lot about the actual state of history of the chains we're testing with,
[11:28] and even a small change can be huge for us. So they used to have a lot that we would be using Ruxton, but then some things wouldn't
[11:38] translate well into actual ETH, so Testnet was essentially retired, in favor of Stagenet. And what Stagenet is, is 4 and Maya are fake, or are tests, or are like not the real deal,
[11:54] but everything else is. So it's a very costly testing environment because we test, we pay actual gas fees, but
[12:06] we simulate the real deal, because a live mainnet like ETH, like Bitcoin, like Dash, you have mempool, you have latency, you have a lot of issues, actual non-zero gas and other
[12:21] things that are super relevant to our work and what we do as integrations. So Stagenet is meant to be as accurate as can be of the real world, and that's why we
[12:34] call it Stage, you're on the stage already, you're there, and it's kind of close to reality. So when we say we're releasing a version 105 of Maya on Stagenet that includes Dash, it
[12:49] includes mainnet Dash, and we already have mainnet Bitcoin and mainnet ETH, and we can do ETH to Dash swaps.
[12:56] The only thing is cacao in the middle is relatively worthless, because the liquidity is very shallow. And we all agree that it's not the real deal, right?
[13:05] But aside from that, Maya Stagenet is 105, except we're having slightly different histories, because Stagenet hasn't had the 5,000 swaps we've had on mainnet, or it doesn't have other
[13:18] several things, like the exact transactional history. Aside from the history, the code is exactly the same as mainnet.
[13:28] So then we can test a lot of stuff, like once we put Dash on top, we're going to try adding Dash, withdrawing Dash, swaps, all sorts of things.
[13:39] So definitely a very close to reality thing. It also helps us see, perhaps, or update us on consensus failure or memory stuff or whatever,
[13:52] just to make sure it's pitch perfect. Obviously sometimes that's not enough and things need to be ironed out later, but the
[13:59] more we can manage a priori, the better we can stress test and catch things early on, the better.
[14:06] What wallets do people usually use? Is it mostly command line testing or are some of your user interfaces, like, for example,
[14:15] maybe Eldorado, do they support Stagenet or how do you do your testing? Yeah, ThoughtWallet does, and ThoughtWallet, we actually use it for testing Stagenet as
[14:27] well. I'm not a developer, so although my orders can do those command line testing, I need
[14:35] to go to the motions. It's good also because ThoughtWallet can also just iron out anything they have on Stagenet.
[14:47] ThoughtWallet has two testing environments. One is a private ThoughtWallet pointing towards Stagenet, and they also have a private environment
[14:59] pointing towards mainnet. So right now, as we push Dash here on Stagenet, they're going to do some testing here, and
[15:07] then once it's on mainnet, we don't use this anymore. We just use the mainnet one, but we might iron out a few details of the front end before
[15:15] actually pushing to production on the front end side. Remember, Maya is kind of just like the back end of things.
[15:24] We usually rely on front ends to essentially make it easy for users to play around. And Rion, is any of this testing and staging something that the incubator node is participating
[15:39] in if in fact that incubator node is being run, or Alux, would you know that? Oh, it's on mainnet, not Stagenet.
[15:46] It's running an actual mainnet node on Maya, helping protect essentially funds and run the chain, run the code.
[15:58] So SuperDashNode is protecting the mainnet right now. And I don't know, you talked about in this coming version, you're going to be moving
[16:10] to liquidity nodes, which, am I coming through here? Liquidity nodes is just a frozen picture.
[16:18] Okay. So you'll be moving away from the Genesys nodes and into nodes that are backed by actual
[16:26] liquidity or competing with liquidity to be nodes. So maybe you could tell us a little bit about that transition, how that's going to happen,
[16:36] when that's going to happen. Yeah.
[16:42] So liquidity nodes start churning in as soon as version 105 is set, a few days later actually. But we can have liquidity nodes and Genesys nodes coexist.
[16:57] We will retire Genesys nodes over time once we have achieved economic security, which is a point where essentially nodes have a lot of skin in the game and they have more
[17:10] points than what they protect essentially. So once we're over collateralized.
[17:14] So that's kind of the path we need to take. So in the meantime, Genesys nodes are still around helping secure, because it helps us
[17:23] have more nodes kind of on our side. And yeah, so liquidity nodes was always in the plan.
[17:32] It actually already is, most of the code for liquidity nodes, it's already in mainnet, but node operators requested, node operators of blockchain are going to be running Maya
[17:44] as well, requested a few features to make it more practical for them and their delegators. So yeah.
[17:51] Fantastic. Yeah.
[17:53] Thanks. Hello.
[17:55] I won Maya. Yeah.
[17:58] Good. Okay.
[18:00] So while we are waiting for Rion to rejoin us, you can hear me all right, Alux, is that correct?
[18:08] Yep. Great.
[18:10] Okay. So I had mentioned before on social media this past week, that an individual from a
[18:17] front end of Maya was, he had initially expressed interest in joining us today, and that was an individual from the Eldorado front end.
[18:29] And so hearing him kind of like describe how like Maya backend, Eldorado front end kind of thing helped clear up a lot of things for me, because I'm one of the people who did
[18:41] not dive in and use any of the Thor chain stuff yet. And so when I saw how many Thor whatever there were, like online media, I was super confused,
[18:52] like Thor wallet, Thor decks, Thor chain, Thor, and I frankly was scared off by it all. And so now that I get a little more clarity around like, oh, okay, these various things
[19:05] that are branded as Thor whatever, are various front ends, is that right? And they're all kind of like competing to be the front end that users choose?
[19:14] Is that? Yep.
[19:16] Okay. So the same thing is cropping up around Maya.
[19:20] Is that, is that correct? Yeah, it's actually desirable.
[19:25] You don't want, you don't want your devs to be focusing on front end stuff, and you also don't want to have these kind of official front end that then essentially you make wallets
[19:44] not want to compete with you because you already have the main thing. So actually what we want is for Maya to go into these various wallets that already exists.
[19:57] So like the original vision was, you know, let's have trust wallets integrate Thor chain, right?
[20:03] And they already did, by the way. So you can already swap on trust wallet.
[20:06] And the way to incentivize these wallets to integrate Thor chain was with something called an affiliate fee, which is something that these front ends append to the transactions
[20:16] in order to get some commission on the transaction. So just that was a very good incentive, so much so that some people just wanted to specialize
[20:28] in Thor front ends. So that's why you see many of these cropping up.
[20:35] You have on Thor chain, you have like DeFi, ThorSwap, ThorWallet, Rango, FirstWallet, several others.
[20:44] And the same will happen on Maya. Many of these existing ones will integrate Maya.
[20:50] Some will emerge that just do Maya, and then some will be non-Maya related or all just wallets that already exist, like TrustWallet or EdgeWallet, but those take time.
[21:00] And it's good. We essentially are bringing Maya to the users instead of having users go to Maya.
[21:06] So that's kind of the logic behind that. And so I think, okay, we'll go for this question first.
[21:14] Helai asks, "During ChaosNet, Thor chain reimbursed people when their LP had bugs and funds were lost.
[21:23] If that happens to Maya, how would you handle it?" Yeah, well, similarly to Thor chain, obviously there's a limit on how much we can take of
[21:33] these failures and reimbursing before we break the bank, but we've already had a few bugs and some people have been already reimbursed.
[21:42] Very small ones at that. So we're talking about hundreds of dollars, not even the thousands.
[21:49] We had several thousands, so that was, I was an ETH, actually an ETH Ruin LP back at those times.
[21:59] So I know what you're talking about. And yeah, we essentially want to make, LPs are VAPs on Maya, per citizens.
[22:11] They're not only the ones bringing the liquidity, but also the ones bonding to run nodes, since nodes on Maya run with LP bonds.
[22:21] So yeah, definitely we want to make them whole and have them trust the system. It's in our best interest to do so for the long term of the project.
[22:31] So we would act very similarly, yeah. Got it.
[22:36] And so will you spell out a little bit more for me, the incentive that some of these wallet creators are working with in order to provide the front end?
[22:47] I think maybe there was just a brief cutout. You had said that there's a fee that gets paid to wallet creators if they are facilitating
[22:59] the transactions? Yeah.
[23:01] They have the choice, not the obligation, but the choice to add affiliate fees, which they essentially say, "This is Trust Wallet.
[23:13] I sent this transaction, please pay, I don't know, 30 basis points to me or 10 basis points to me."
[23:22] So that would mean for every $10,000 your swap had, $10 will go to these guys. And they can be added to swaps, to liquidity ads, small withdrawals, and coming soon also
[23:40] to saver ads. So that means usually user interfaces spell out what their fees are.
[23:49] So always just be careful because you could be in one that charges, I don't know, 2% and that's too much.
[23:55] Like that's definitely over what the market has. They're typically below 1%.
[24:04] So yeah, it's a choice also for you as a user. Sometimes some front ends are offering no affiliate fees for a while or for a set time,
[24:14] or if you hold their NFTs or something, or you also have always the choice to use custom memos, which is just a way to actually send instructions to Maya yourself, jumping essentially
[24:26] the front end and not pay any affiliate fees. But that requires some technical capability, not really coding capability because I use
[24:36] memos myself a lot for testing and stuff, but rather just conceptual knowledge of Fortune and Maya and a bit of practical knowledge on using blockchains.
[24:48] So that's always an option. That's great because people have a choice and part of the centralization is choice.
[24:57] That's a very important thing in decentralized systems. So we care a lot about that.
[25:04] Great. I have a question that I'm pretty sure you probably didn't answer while I was gone, but
[25:11] I have a question about upcoming features for Maya. I know that the Thorchain guys are releasing a lending feature.
[25:23] I think that you had some disagreements about that feature. So I wanted to get your take on what's the future of Maya and lending?
[25:34] Maybe you could give a little bit of background on lending and tell us what Maya is planning on and how that might contrast with Thorchain.
[25:42] Yeah. Well, one of the key things of having two systems like Maya and Thorchain in parallel
[25:47] is that we can tweak stuff, kind of A/B test. So part of the things we're doing is obviously looking to catch up with a lot of Thorchain's
[25:59] features, but also putting in our own little sauce on what we think would be best. Because also Thorchain and Maya are not completely equivalent.
[26:07] We do have a fair share of changes. So it's not only plug and play.
[26:15] We need to think some things through and think the implications of others. So for instance, in our case, due to the capital efficiency of the query nodes, we have our
[26:27] reserve being constantly backfilled by 10% of swap fees. So this is something that allow us to just drop dynamic outbound fees, which is something
[26:40] Thorchain did, but they're now looking on how to replace some of the reserve income because it don't backfill it.
[26:47] So what I mean to say is just every future tastes different in Thorchain and Maya and has slightly different implications.
[26:56] Now on the specific case of lending, the future has matured a lot, actually, since we last spoke.
[27:04] And as we've been moving forward, they've been tweaking a few things, some to make it make a bit more sense.
[27:11] For instance, in the past, they used to look to have a starting collateralization ratio of just 100% and start there, and then dynamically increase it.
[27:22] I didn't agree with that a lot. It seemed like too much of a great deal for the ones starting, the first few people opening
[27:29] the loans, and they dropped that now. That's not the case anymore.
[27:34] So that makes me happy. So just like that, there's a little more technical details that I think are moving in the right
[27:42] direction. We'll see whatever ends up coming out of the oven.
[27:48] And then once that's out, we'll see how and if we tweak it for Maya. It would definitely be a few months later.
[27:59] So we will definitely also wait. Part of the reason for Maya to exist is also redundancy.
[28:06] So we want to see the implications of lending, how it benefits or harms the economy. I'm very bullish on it personally, but we want to see it rolled out, see how it works,
[28:21] and then see whether it makes sense for Maya or not. And there's other features that are coming up as well, for instance, streaming swaps.
[28:30] That's great. That would be a way to reduce the slippage of transactions by allowing arbitrage essentially
[28:37] to happen concurrently to the swap as it was broken down in kind of smaller swaps. So that's very interesting.
[28:45] And that's something we wouldn't wait months for that. We probably would wait just weeks to other Maya.
[28:51] So depending on how much it affects the economic environment of the chain, it's how careful we are on how fast we kind of put it into the fork.
[29:06] So yeah, what you can expect in Maya, aside from kind of rolling out or classic features of liquidity nodes and all of that is catching up, we would be having savers on version 106.
[29:20] It also works a bit differently and I'm actually happy to see that how we were going to plan it to be different.
[29:28] Some of our proposals to change it are making it into Thorchin as well. They're having the problems we thought they were going to have in the future.
[29:38] So very excited and happy to see that. And also, we will be working, aside from more chains, so we have Dash, we have Cougie, Arbitrum,
[29:51] later Cavano. We also look forward to having more smart contract layer, hopefully this year, depending
[29:59] on many factors. But yeah, our main priority right now is swaps.
[30:05] And when we're comfortable with swaps and volume and how that works, we can pay attention to things like the smart contract layer and stuff like that.
[30:14] Okay. So the other one question I had, besides the classic when question, which I guess we'll
[30:20] leave to the end if we haven't already covered it, masternodes, are you familiar with Dash's masternodes and do you think that it's possible to have Thorchin or Maya running Dash masternodes
[30:38] in the liquidity pool so that you can get extra yield? Because one of my concerns is that the swap volume in the bear market may not be high
[30:54] enough to justify a lot of people moving over to being, say, masternode owners, getting a 7% yield, and swapping over to being a liquidity provider on Maya, getting less yield.
[31:11] So is it possible to combine those features? I would have to see.
[31:17] This is a good question. For instance, one way is using liquid staking derivatives, but that sometimes requires some
[31:28] centralized trust, so we don't do those. In the case, for instance, of ADA, ADA is a coin that can be safely delegated, but then
[31:37] also used anyway, and it remains delegated to the node despite being moved around. So it's a very interesting concept.
[31:47] So in that case, I would say a hard yes. In the case of Dash, I'm not sure how locked the tokens are.
[31:54] That's something I would have to research. I can tell you that the technical limitation for a Dash masternode is that you have to
[32:00] have exactly 1000 Dash in one UTXO that you point to. So in the case of Maya, the only way that I would see it potentially being possible
[32:16] is if Maya's liquidity pool could be like tiers of 1000 Dash each where you're running masternodes on each 1000 tier, and then if there comes a swap that needs to dip into
[32:34] one of those 1000 Dash tiers, in Dash there's no locking, there's no time lock requirement to run a masternode.
[32:46] It just has to be that 1000 Dash increment in a UTXO. So if there was a swap that needed to dip into 1000 Dash, you could just spend it.
[33:03] But I also know that in Maya, there's one and only one address that is associated with the liquidity pool.
[33:10] So I'm not sure how that would work, if that would work, but I think it might be something worth looking into because if we could get that feature where liquidity providers on
[33:22] Maya are getting the yield of both a masternode and the swap volume liquidity fees on top of that, that would be very interesting.
[33:33] So maybe just something to look into. Yeah, it's something to think about.
[33:38] I remember also, addresses on Maya change every churn, so they're also constantly changing. So that's something to think about.
[33:47] And my question is always like, who's running the code? So like, sure, the funds are custody by the Asgard Vault with a 20-node multi-sig, essentially
[34:00] in simple terms. So but who are those is the one running the code for the Dash node?
[34:07] Who's the one doing that? So that's kind of a question to think about.
[34:12] But yeah, something like we should speak about this with Exodus and explore it. I'm happy.
[34:19] I'm happy. I'm always happy to explore.
[34:21] So definitely. Did you guys talk about when we're getting to mainnet yet?
[34:28] Yeah, not yet. How much testing?
[34:31] Okay. Devs do something, huh?
[34:35] What's your best estimate? Yeah.
[34:38] As we were giving an update this morning on Mondays with Maya, we have version 105 station ready.
[34:49] We already clarified a bit what stage it is, but then Dash is going there again today. It went on Friday, but we found a few issues, not with Dash, but with the other concurrent
[35:01] feature called the Query Nodes. So we fixed those over the weekend.
[35:06] We have a new version coming today, like a newer version 105 to test again. So that's going out today.
[35:16] And we essentially are testing on that station environment, which is like real Dash being swapped for real ETH or real BTC.
[35:26] So we're going to be doing that. And essentially, we have no major issues.
[35:31] It's this week. We do think, though, that that's going to mainnet to the chain, and it takes some time
[35:40] for frontends to catch up. So it doesn't mean that you will find it on Rango on Friday.
[35:47] Rango might take a week or two to support it as well. It's quite normal to have a lag there.
[35:54] But it depends on testing. We're not going to ship it unless we're confident it has a high likelihood of success.
[36:02] So we are careful with that. We took a lot of time to have smoke tests updated.
[36:09] So essentially smoke tests is another concept, which essentially the chain launches Dash and launches Maya both in magnet and then automatically does like over 100 transactions
[36:27] of different kinds with different amounts, different parameters, different transaction types of ads, withdrawals, swaps, all of that.
[36:37] And we essentially see whether they run like they should. So it's a very important thing that was added to 4Chain to make it safer.
[36:47] We have it on Maya as well and had to work a lot on getting that on Dash to pass. So we have a high certainty that tests should go well.
[36:56] But again, on real life, Dash has gas fees, has mempools, has delays, has latency, has all sorts of issues, momentary forks, sometimes probably, well, I'm not sure if that happens
[37:12] in Dash but happens in some UTXOs. So all of that needs to be taken a look at.
[37:21] So yeah, anyway, but if everything goes well, I do see it this week, we'll see. And good estimate, David, well done.
[37:32] We did where they laid a bit, but I would like to mention that it was mostly on Maya's side of getting a lot of work done on stabilizing the network.
[37:42] The actual work by Dash has always been prompt and actually always in front of what we need. So shout out to the team, Rion, really great team you have.
[37:53] Thank you. When doing estimates, a lot of times people will ask like, when's the latest?
[37:59] When's the absolute latest? I should expect it like we'll see it no later than this year or we'll see it no later than
[38:07] this month. But the question I like to ask and better than that is when would be the earliest?
[38:14] You definitely won't see it before at least a week or at least a month. So it sounds to me like you're saying probably at least a week and then no estimates on,
[38:28] you know, when. The easiest, the latest.
[38:30] Yeah, but don't expect it in the next week kind of thing. So it could happen.
[38:36] It could happen this week if testing goes terrific today and tomorrow, then we'll just be preparing the update for mainnet, which takes a few hours and then actually pushing
[38:49] it and then or six nodes need to actually run the update. So once, you know, it's just going through the motions.
[38:59] It's possible. But we'll see what I can tell you is that we won't ship it unless it's ready, which
[39:07] is the important part, and we will be cutting any corners or we haven't been cutting any corners.
[39:13] So that's kind of the important part. Nice.
[39:17] Well, I know that I know that the volume is king in indexes, like having transaction volume swap volume is the most important thing other than other than swap volume.
[39:31] What do you need from the Dash community? I have one thing other to say after after you answer this question about swap volume.
[39:37] But other than just using it, what what do you need from the Dash people? Yeah, just using it, considering adding liquidity, promoting it.
[39:47] At the end of the day, I do see a lot of activity in the last few weeks of, you know, security dramas and the listings and central exchange issues and Binance shutting down in the Netherlands,
[40:04] for instance, crazy stuff like that. So it's definitely something useful that you can tell your friends that use Dash, OK, you
[40:13] might be in this situation just like me. You can use this thing called Maya to move around, you know, to move to Bitcoin for some
[40:21] reason or back to Dash and whatever. So or even invest a bit on the liquidity, expose yourself to that possible upside, please
[40:33] not bet your house, as I've always said, be careful and mindful of the risks associated with crypto.
[40:41] And obviously, having Dash in Maya has increased risk of now what you're exposed to two networks. So if Dash fails or Maya fails, your money is compromised.
[40:50] So just be you have to be conscious of that. But yeah, participating, sharing, if you are considering putting a large bag of Dash on
[41:02] the pools, you can also use it to bond the node, a liquidity node. Those are super helpful since they help secure the network, scale the security and just make
[41:14] the network more decentralized and more resilient. So that's a great thing to do.
[41:19] And what's your estimate of how much cacao or Dash, if you can do that conversion, or the US dollars?
[41:28] Yeah, you have half and half of both and it should be roughly a hundred thousand dollars. A hundred thousand dollars.
[41:33] Give or take, perhaps 50 percent more, perhaps 30 percent less, something like that. Yeah.
[41:41] Yeah. So if you're running, if you're running like four or more Dash masternodes, maybe it's
[41:46] something to consider running a Maya node instead, a liquidity node. So in terms of volume, I can tell you one other project that we have in the incubator
[41:58] is I'm trying to get us back to the privacy roots of Dash where one of the key features of Dash is privacy.
[42:09] We're bringing our CoinJoin implementation into a JavaScript implementation so that we can do CoinJoins using the masternode network in browser settings.
[42:24] And one of the reasons I want to do that is I want to offer kind of like a privacy or fungibility as a service through Dash and Maya.
[42:35] So if you have Bitcoin and you want to make that more private, you can run it through this application that is yet to be built, but will be at some point.
[42:48] And then it will convert your Bitcoin to Dash, mix it using CoinJoin masternode over the masternode network, and then convert it back into Bitcoin.
[43:00] And you will. Via the Maya swap.
[43:02] Yeah. Via the Maya swap.
[43:04] Yeah. So that's one application that we're working on.
[43:08] I don't know the demand for that, but that would definitely increase the volume through both Bitcoin, Litecoin, whatever coins are supported, Ethereum through Maya.
[43:22] So we'll give updates on that, but I think by the time everything is humming along well on the whale oil machine of Maya, I would probably say that's probably going to be a
[43:36] couple of weeks at a minimum. That's after that point, we might have something to test.
[43:44] But Rion, when is the earliest? One month is the earliest on that.
[43:55] Don't ask me before that. The time frame I'm using for all of these is before Alux's second wedding.
[44:03] And that's the one I'm going for. Right.
[44:07] Yeah. So good.
[44:09] All right. Well, thank you for joining us today, Alux.
[44:11] Thanks for your questions and comments, everybody. And we'll see you next week, same time, same place.
[44:16] Yeah. We're finishing?
[44:18] Oh. No.
[44:20] No, we're not. We want that final comment from you, Alux.
[44:23] Okay. Just final comment, because I did have one more point of one thing that you guys can
[44:27] do on Dash. Please.
[44:29] And it's a shout out to everyone. There's many ways you use Dash, many places you use Dash, like Dash Direct and others.
[44:35] Just give them a shout out. Make them aware of Maya, what we're doing.
[44:39] Encourage them to support Maya somehow in some use case that you're interested in. Like voice your needs.
[44:45] Hey, I'd love to do this. Share that with the user interface you use.
[44:50] And that would make them more likely to work with us and do that integration job. We're super happy to work with them all.
[44:59] We have a long list of UIs that we work with and happy to be adding more of those on the Dash side.
[45:05] So yeah, that's just like voice your needs. That's kind of what I would like to say.
[45:11] And if they see it's hundreds of people, they'll hurry and they will have that earlier. It doesn't take many, actually.
[45:18] It just takes a few people to ask for a feature, I think. Yeah.
[45:23] Yeah. And that's right.
[45:25] So the wise man, Ash, he knows what he's talking about. Just so that somebody who's listening can hear it.
[45:34] The more we use Dash on Maya, the deeper the pools, the better the rates. Yeah.
[45:38] And that comes from Ash, the incubator strategist who many moon ago started up the code that was not even written for the Maya integration at the time, but eventually made its way to
[45:53] become that. So it's been a long road and you all have done good work and we're looking forward to
[46:00] the next manifestation. Yeah.
[46:02] All right. Well, thanks for having us.
[46:05] Looking forward to being here again in a few weeks with the good news of a lot of Dash volume on Maya and anything you need, guys, we're here for you.
[46:14] I'm super happy to join our communities. So thank you for having us.
[46:18] Likewise. Awesome.
[46:20] All right. Thanks, guys.