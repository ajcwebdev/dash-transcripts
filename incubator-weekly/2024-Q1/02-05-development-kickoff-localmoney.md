---
showLink: "https://www.youtube.com/watch?v=hTublYO0Gso"
slug: "development-kickoff-localmoney"
title: "Development Kickoff of LocalMoney"
publishDate: "2024-02-05"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/hTublYO0Gso/maxresdefault.webp"
---

Mikhail discusses plans to build a decentralized peer-to-peer fiat to crypto exchange on the Dash network.

## Episode Summary

tl;dr: Mikhail discusses plans to build a decentralized peer-to-peer fiat to crypto exchange called LocalMoney on the Dash network. The exchange would allow users to trade fiat for Dash and other cryptocurrencies without relying on centralized exchanges. Key features include a trustless escrow system using multi-signature transactions, censorship resistance, and cross-chain atomic swaps. Challenges and potential solutions around decentralized infrastructure and user adoption are discussed.

## Chapters

00:00 - Introduction and Background on Centralized Cloud Storage 
The episode begins with a discussion on the proliferation of digital information, centralized cloud storage providers like Amazon, Google and Microsoft, and the censorship and surveillance concerns around centralization.

04:53 - Introduction of Guest Mikhail and LocalMoney Concept
Mikhail is introduced to discuss plans for building a decentralized peer-to-peer fiat to crypto exchange called LocalMoney on the Dash network as an alternative to centralized exchanges.

09:41 - Overview of LocalMoney and Escrow System
Mikhail provides an overview of the LocalMoney concept - a decentralized exchange allowing fiat to crypto trades through a trustless escrow system using multi-signature transactions. Other planned features like cross-chain atomic swaps are discussed.

16:49 - Development Plan and Decentralized Infrastructure 
The development plan is laid out, starting with research into the escrow and multi-sig system, building out the front-end and back-end, and then exploring approaches to decentralizing the infrastructure to make the exchange censorship-resistant.

22:56 - Challenges with Atomic Swaps and Adoption
Potential challenges with cross-chain atomic swaps are discussed, including the need for double coincidence of wants and the difficulties faced by similar projects like BISQ. Mikhail believes focusing on user experience and accessibility compared to desktop-only clients can drive adoption.

32:07 - Comparisons to Competitor Projects
LocalMoney is compared and contrasted with projects like BISQ and Local Bitcoin in terms of features, user experience, and potential reasons they struggled with adoption. The need to focus and avoid expanding scope too much is emphasized.

38:15 - Importance of Escrow and Mikhail's Personal Commitment
The importance of a solid escrow system to the minimum viable product is highlighted. Mikhail expresses his personal commitment to using LocalMoney himself, especially for Ruble trading pairs, and openness to community feedback.

## Transcript

[00:00] We live in the information age, kicked off by the invention of the transistor in the mid 20th century, digital technology has since proliferated and radically altered the way
[00:15] almost everyone worldwide lives, works and plays. Online, no matter what it is, what type of content, information is stored and manipulated as binary code, ones and zeros.
[00:26] Each one or zero is one bit, it takes 8 bits to make one character, like the letter A or the number 7. Despite this minute size and aggregate, there is a ton of digital content
[00:37] now being generated. It's estimated that in 2025, the amount of digital information created globally every day will be 465 exabytes, an amount equal to the storage capacity of
[00:49] 210 million DVDs. Certainly all that data is not being burnt onto DVDs, so where does it go? Some of it goes to personal hard drives and on-site servers, and a lot of it goes
[01:00] to the cloud, centralized cloud servers maintained by corporations. It's big business and is growing fast. A couple of years ago, the cloud storage market was about 90 billion.
[01:11] Last year, it was about 110 billion. By the end of the decade, it's expected to be about 500 billion. Today, the biggest cloud service providers include the following, Amazon Web
[01:21] Services or AWS, Microsoft Azure, Google Cloud Platform, etc. They tend to use a pay-as-you-go model, exbytes of data for y period of time with z retrievability guarantees. To retain
[01:34] and attract more customers, they seek to excel in a number of attributes. Latency, the amount of time it takes between a user request and the server response, mostly influenced by
[01:44] geographical proximity. Throughput, the amount of data handled by the network at a given time, mostly influenced by bandwidth. Availability, the percent of time that the cloud is functioning
[01:54] correctly, also called uptime. Durability, the probability that data stored to the cloud is retrievable in one year, measured in nines, such as 10 nines of durability. To improve
[02:05] durability with much less overhead, data isn't simply replicated in entirety, but is sharded. Pieces are sent to various locations so that even if some of the pieces are lost, the content
[02:15] can be reconstructed. Today, just three corporations, AWS, Google Cloud Platform, and Microsoft Azure, account for two-thirds of the global cloud storage industry. Centralization can
[02:26] bring economies of scale. It can net the corporation bulk deals on hardware for manufacturers, the ability to land favorable offers when determining in what political jurisdiction to build a
[02:36] data center, and greater efficiency due to specialization of labor. But centralization can bring vulnerability in the form of data leaks or loss, and hacker attacks, and can
[02:45] be fragile. Consider just one month, December of 2021. AWS had three major outages, the last due to the loss of power at a single data center. And centralization brings with
[02:57] it surveillance and censorship concerns. These big corporations include not just individuals as customers, but government agencies, and they've been known to do them favors. In 2020,
[03:07] a documentary called "Plandemic" was making the rounds. After big tech platforms like YouTube and Facebook censored the content to comport to the narrative being pushed by
[03:15] DC, some folks uploaded the video to Google Drive, which relies on Google Cloud Platform. Made aware of this content that questioned the official narrative, the Google Cloud peeps
[03:25] deleted the content. The following year, AWS canceled the hosting of Social Network Parlor after it disagreed with content posted by users. And let's not forget about this, Jim,
[03:35] when Amazon, which of course uses AWS, deleted the book "1984" from customers' Kindles. In 2021, the largest cloud corporations crafted what they dubbed "Trusted Cloud Principles."
[03:46] Ostensibly motivated to protect customer privacy, their principle proactively notes the desire to "partner with governments to resolve international conflicts of law that impede innovation, security,
[03:57] and privacy." But as governments are the biggest transgressors of law, innovation, security, and privacy, this is only window-dressing, demonstrating the willingness of these corporations
[04:07] to click their heels when so ordered. The allegiances of these centralized cloud corporations and the censorship that they have engaged in has spurred some discussion, including
[04:16] this insight from Courtney McSherry of the Electronic Freedom Foundation. When you engage in content moderation, you are inevitably oversensitive. You take down more content
[04:24] than is "harmful." There is no reason to think that the situation would be any different at an infrastructure level. Might there be a better option than relying on these censorship-prone
[04:33] centralized corporations, options that are not just uncensorable, but possibly more robust and speedy? There may be. Decentralized storage. We'll delve into that next week.
[04:53] A two-parter. Dang. Now I'm for sure tuning in next week. How about y'all? I'll be there. That'll be interesting. Maybe we'll have to have a show that kind of dovetails
[05:03] with that. We'll have to see. Okay. Here for the intro only. Nice. I for sure didn't know that Amazon had taken copies
[05:11] of the book "1984" out of people's drives. That's too much. You can't make that up. Mikhail, how are you today?
[05:19] I'm doing good. Yeah. Splavik says, "Wow." Well, I say, "Wow," too, because we are here today with one of
[05:29] the strategists from the Incubator, Mikhail, to speak about something that is pretty dang important to me anyway. And that is a decentralized... Oh, I'm almost so sick of using that word just
[05:47] because of how often it's abused. But a fiat to crypto exchange, because there's the occasional sprinkling of this or that out there, but nothing robust or popular that I've seen.
[06:02] The last time there was a popular version, it was centralized. It was called LocalBitcoins.com. I was a big time user, thought it was awesome. And then five, six years ago, they started
[06:16] like taking away trade options, and they just slowly took away more and more trade options until what was it, guys? Do you remember? Like two years ago, they just said, "We're
[06:24] closing our doors. Goodbye, everyone." And then the market has been bereft since. So where did this idea come from for you, Mikhail? Was it that same thing or something else?
[06:36] Yeah, the idea... Actually, the project was picked up by me, and also there is another developer in the Dash Incubator called Emmanuel, which really love to see this product is going.
[06:56] So he told me about this project, about the possible building of decentralized exchange on top of Dash. And yeah, we are driving this product through together.
[07:15] Just to add a little bit to that, the project actually has been in the incubator for a long time, predating, I think, even Mikhail's involvement as a strategist. And that was originally started...
[07:33] I don't know who started it particularly, but Tim, Spectaprod, was the strategist that had that project originally. And then Tim's budget went down to essentially zero. So he
[07:51] wasn't able to continue working on it. And so we needed to find a home for that project. So Ash and I both discussed it, the pros and cons. And for various reasons, we declined
[08:05] to pick up personally as one of our own projects. But Shenmik, Mikhail, has picked it up, and I'm looking forward to seeing if he can breathe new life into it.
[08:21] And so everyone is clear what we're talking about. Okay, I'm sure you've heard the term DEX. So for example, we're not talking about the DEXs that live on top of a single network,
[08:33] you know, like what's the one with the unicorn or the sushi swap, where you can only trade tokens that live on top of a single network, right? Like Fishcoin, Gigabyte, Swap, whatever,
[08:48] right? Okay, so we're not talking about what are essentially colored coins, or on Ethereum they'd be called, you know, ERC20 tokens, whatever. We're not talking about that. We're
[08:58] also not talking about a DEX that is cross-chain, right? Which in the case of Dash, we're most excited about, like Maya, where we can swap natively, like chain to chain. It is not that.
[09:11] We're talking about an exchange where somebody who has rubles in their bank account, or even rubles in their hand, stack of them in their hand, wants to get their hands on some crypto.
[09:22] How on earth do they do it? That's the market that LocalBitcoins.com used to serve. So shall we bring up your slides, Mikhail?
[09:31] Sure, sure. Let's get to it. Can you see that? Yes.
[09:41] So originally, the concept is a decentralized peer-to-peer exchange, where you can exchange fiat, which uses ETH or token by admin through the DEX wallet. So what problems do we have?
[10:02] The first is that centralized exchanges like Binance, Paxful, or any others, they enforce some censorship rules. They can block access for different people, for example, for Russian
[10:14] people, or any other people, just choosing randomly or not. And also they enforce to abide the rules of the country that they registered into. They also enforce to use know your client
[10:33] and your money laundering clause that's required to make trades. Even for small trades, if you trade like $10, $100, you know, you have to give out your IDs and stuff like that.
[10:49] And the most important thing is that they hold all the access to your funds. Like to exchange your Dash on the fiat, you have to load it up onto custodial exchange. And yeah,
[11:04] that's something that has to be done. So what's the idea of LocalMoney concept? LocalMoney concept is a decentralized peer-to-peer
[11:23] exchange where you can run trades through the escrow using multi-sign transactions to make trades. So how does it work? You want to trade Dash for your fiat, for example,
[11:39] for USD or Rebels, and you, buyer and the seller, they get registered on the LocalMoney. Then they create an escrow address that all three parties have access to. This is the
[11:59] buyer, the seller, and the arbitrary of the LocalMoney that would be chosen by the DashDAO. So the money gets loaded up and then the fiat transactions gets executed. Once the transaction
[12:21] is done, once the fiat is getting loaded up onto a bank account, for example, or in cash, both parties are chosen to approve and confirm the trade. But what if one of the party want
[12:40] to scam you and just doesn't want to approve you? Like they accept the money but don't want to release the money. The third party comes into the game. So the arbitrary, the
[12:56] escrow admin that will be chosen by the voting in the DashDAO have the access to choose which part of this transaction will be approved. Like he will get access to all the history
[13:18] of the trade, like both parties will be able to post the screenshots or stuff like that, some details of how the payment was going. And then he will choose what party will receive
[13:36] the money. So how do multi-sign transactions basically work? This is the way where we can have three private keys held by each party. But in order for the transaction to succeed
[13:57] in the network, two or three parties have to sign with their private keys. So we have three private keys, but only one address. So the money gets loaded up on this address,
[14:11] but in order to transfer it, you will have to have the approval of the two parties. And I want to bring up here, if I may, that this escrow function, and granted LocalBitcoins.com
[14:26] had this too. So what Mikhail is talking about is also having this excellent escrow function that doesn't just address like, "Hey, how do we make trades safe between two people
[14:39] who are potentially thousands of miles from each other and don't trust each other, don't know each other? How can we make that work?" But this escrow mechanism also addresses in-person
[14:51] trades for unbanked people or people who are doing cash trades. I bring this up because I've seen a comment in the Dash Discord at some point saying, "Oh my gosh, how could
[15:03] we ever, ever sign on for in-person trades? That's so dangerous. That's so dangerous." And this escrow model and the arbiter model where someone else ultimately has the say
[15:18] if there's a dispute as to whether the trade went well, that really adds a lot of protection. And I'll say, I remember back in the day, reading trade posts for people who wanted
[15:29] to buy or sell cash with crypto. Some of them would say, "Hey, I'll meet you in the lobby of the police station." So I mean, it was like people set up secure trades, surrounded
[15:45] by police with escrow on the other side of things. And so I just want to say, it seems like it's just a good tool. I'm glad you've included it. Please continue.
[15:54] Yeah. So basically fiat trades will be available to exchange, to buy Dash or sell Dash. And some other crypto pairs will be available to exchange, but these trades will be available
[16:13] through atomic swaps, through the time-locked contracts and stuff like that. So it's not only about buying and selling Dash. You can also choose to exchange different cryptocurrencies
[16:29] on the platform, on this platform. Yeah. So what is the plan? The plan is to prepare, so the first, what we need to do is to do a lot of researches. The first research is
[16:49] how can we make this escrow work. We have to research how to do this multi-sign transaction. To do that, we plan to prepare classical front-end, back-end infrastructure where we deploy front-end
[17:08] and front-end will be taking the back-end. On the back-end we have an SQL. So at this point the application will look like a regular local Bitcoin application. But at this point
[17:25] we will try to make this trustless escrow transactions in the meaning that only you have access to the fund and this multi-signature transactions. Once we get this, we can think
[17:41] of migrating infrastructure to the decentralized way. What does it mean? It means that anyone could just clone the code, clone the repository, download the source code on their computer,
[17:57] laptop or mobile phone and start making trades. So at this point the application will be able to sync up to the network and once it's done, everything will be done in decentralized ways.
[18:19] That means that you don't have to connect to any given concrete back-end server or reach out to website which can be closed down by the government, it can be taken down by the
[18:41] hoster, by the owner of this website. So there are several approaches how can we do it and we're still searching the best way to do it. One of the way is to use Dash platform probably,
[19:08] but since it's not live yet in the testnet, we can't really rely on that yet. What is the back-end doing, Mikhail? What is the back-end doing in this case?
[19:21] Right now back-end is used to store the information about the user like login, password, the orders, all the chat info, but later we will delegate it to the decentralized databases.
[19:48] Is there business logic on the back-end? Actual code that has to be run I assume? Yes, for the first stages, yes. Every logic will be in the back-end.
[20:03] So if you did need to or when you do want to move to a decentralized back-end and if you planned on using Dash platform for that, then presumably you would need some kind of
[20:15] code execution to do the business logic, which would not be possible without smart contracts or some other solution to run code on certain data.
[20:28] Right, so there are a few approaches. The first approach is that everything will be run on the client's device, like the client can verify everything integrated in the source
[20:44] code, so for example, the person who would like to make trades, he will download the front-end and the back-end, which will act as a gateway between the decentralized database
[21:02] and the code that verifying the state that is stored in the decentralized database, and he will connect via front-end to his local.
[21:15] Another approach is to integrate it as a single application, but in that case, the web application would be harder to do because web browser doesn't allow you to do much things, like
[21:36] you know, the DCP connections are pretty limited and some protocols are not available, and for example, storage level is not so powerful, and stuff like that.
[21:54] Okay, yeah, and after we make this infrastructure in a decentralized way, we can then step on to implementing some different crypto pairs to exchange, it will be done via atomic swaps,
[22:14] which can be done via time-locked contracts, so you can exchange Dash on Ethereum, on USDT, and any other cryptocurrencies.
[22:26] Okay, let's pause a moment on that point that you just made. So you are saying that you'd like the application to, it sounds like, is it Dash-native, like the only way, or the
[22:39] only crypto that anyone can buy in their first step in the application is Dash, and then only afterward can Dash be swapped to other currencies, is that right?
[22:49] Yeah, yeah, exactly. Now I don't know that much about atomic swaps, except that I've just always thought they
[22:56] sounded cool, like very cool, but for whatever reason, and I'm sure I don't need to tell either of you or anybody else this, atomic swaps have not taken off. I mean, am I right?
[23:06] I haven't seen them take off nearly to the extent that, for example, automated market makers have. So are we just headed for another black hole, like all these other people who
[23:18] have dumped resources into atomic swaps, or is it different for us? And if so, why? Well, they work. At least what I can say is that the scheme is working, that atomic swaps
[23:35] exist. I don't know how much volume they have, but it's possible to do, and it's a way to do to exchange the Dash on other cryptocurrencies, trustless.
[23:56] So because you asked, maybe I'll give some of my understanding of atomic swaps and my concerns. The term atomic is more or less a database term. In databases, you have what
[24:11] are called atomic transactions, where one part of a transaction only happens if the whole part of the transaction happens. So you can imagine one part of the transaction
[24:23] being, I'm going to lock up my coins, and another part of the transaction could be somebody else is going to lock up their coins, and another part of the transaction would be those
[24:35] coins get swapped or something like that. So sometimes there are multiple steps in a transaction. Atomic means the whole thing either completes or none of it completes.
[24:45] You can't have a situation where half of the transaction happened, like I locked my coins or I sent my coins to this place, but the other half of the transaction didn't happen.
[24:55] That's just the etymology of the term atomic transactions. And atomic transactions, like I said, that's a database, general database thing, not just a blockchain thing.
[25:11] In this case, you know, you definitely want those transactions to be atomic when you're doing exchanges from one person to another. I want to have assurance that if I send my
[25:21] dash somewhere, then the Bitcoin that I wanted is also going to come as part of that transaction or the whole thing gets canceled. So that's obvious, nice user benefit. The reason why
[25:35] I think that they have not succeeded very well is that they're basically predicated on the idea that of an order book where I want exactly $1,000 worth of Bitcoin, and
[25:48] I need somebody that also wants exactly $1,000 worth of Dash on the other side of my trade because I'm trading with a specific person, not necessarily with a protocol. And I could
[26:00] be wrong with that, but that's my understanding of primitive atomic transactions. And that's one of the reasons why they haven't taken off is because you just need it's very difficult
[26:10] to find somebody with that what economists would call a double coincidence of needs. And so it's, it's not there, the liquidity is not there to use another dumb term. I don't
[26:22] like it. But there's just not, it's not very likely that you'll find somebody in that scenario. And that's why automated market makers have been more successful, because now you're trading
[26:33] against a protocol of a whole pool of funds that are managed by liquidity providers. And so it's mostly like a market meeting a market need rather than a technical, it's not a technological
[26:47] problem. Like Mikhail was saying, atomic swaps are more or less a solved problem technologically, but they don't necessarily solve the problem in the marketplace, at least not yet. And
[27:00] that could also change. So that's one of my concerns with this project is just that whole idea. And why has why has, for example, bisque not taken off because the problem, the market
[27:16] problem that I just described, exists in the fiat world as well, not just the atomics transaction, you need to find somebody that has $1,000 of fiat that you want for your $1,000 of dash.
[27:28] So that that problem is not a technological problem. It's a market problem. It's also a problem of having enough, like being the dominant market player in an industry. And
[27:41] that's a big, big challenge. So I obviously hope that this project succeeds. But those are kind of my concerns with it. And I think that Mikhail has a better, a better idea of
[27:54] what the demand for this would be might might be like in the Russian community, for example. Splavik says, can this be done on the Maya decks as part of local money?
[28:05] Yeah, good question. So local money, just so everybody's clear. I think that could mean two different things, because there is a local money project in the Maya community that actually,
[28:18] I think it's in the Kajira community, which is one of the other coins on the Maya decks. And they're building a project that's very similar. It also has the exact same name called
[28:30] local money. And so that that would be, in my opinion, a competitor. So I don't know what that if that question was referring to maybe Splavik can chime in and verify, was
[28:44] that referring to this local money? Can somebody bring up the question again? And then I'll just shut up and let Mikhail answer this question.
[28:53] Yeah, I think the question was, maybe it's a good idea to implement the Maya straight into the local money. Is that his question? Like to do exchange between cryptocurrencies?
[29:05] Well, if so, I was thinking about that, but I have to research it as well. So I think it should be possible to do that, but I haven't checked this out yet.
[29:26] Okay. Splavik just made a comment saying that local money's Michael wants to build. So I don't know.
[29:33] I think he meant. Oh, okay. I was going to say, maybe there's a contact for you, Mikhail. It just happens
[29:38] his name is Michael. Okay. Can we talk about BISC for a moment? I'm glad you brought that up, Rion, because it is, as you said, in a lot of ways, fairly similar to what we're
[29:49] talking about here. And I don't know about the traffic that BISC is or is not seeing to this day. Somebody please chime in if you know that. But I did try to become a BISC
[30:08] user four or five years ago or whatever. I actually interviewed the guy the week after he launched it back when it was called BitSquare. And I guess that wasn't a good name. It was
[30:20] already in use somewhere else and he didn't know. But yeah, long story short, BISC was a client you had to download to your desktop and it needed to be left running in order
[30:35] for trades to happen. And one side of every trade always had to be in Bitcoin, didn't support any other coins. And then the fiat...
[30:48] There was a small period, I think there was a small period where they actually did support Dash.
[30:53] Really? Yeah, I think so. At least they were talking about it because I was following the project
[31:00] very closely and I heard either plans or actually it was working and I do believe it was actually working. But anyway, keep going.
[31:08] My stars. Okay. Well, the fiat options were similar to what was available on LocalBitcoins.com. So it was like an ACH transfer. Did they actually support cash deposits at a bank branch? I
[31:26] don't know. Yes.
[31:28] Yeah. So that was cool. I don't know if they supported in-person meetups for people who happen to be in the same area. And then there were... Yeah. And then I don't know if they
[31:38] just supported gift cards or whatever, like, "Hey, send me your gift card for this store." I imagine they supported PayPal, et cetera, and et cetera, et cetera.
[31:47] I might have to walk that back just a little bit. Sorry. I may be getting my experiences mixed up with LocalBitcoins and things like that. So I'm not 100% sure that they did support
[31:58] bank transfers, but keep going. Okay. Yeah. Well, anyway, yeah, I just remember I downloaded the client. I was ready to make
[32:07] a trade. I was feeling excited. And kind of just like you mentioned, Rion, there seems to be... Well, I guess it didn't support the trade I was looking for. But anyway, la, la,
[32:22] la. No more of my experiences. I just want us to discuss, if we might, why didn't BISC take off? And can we prevent ourselves from going down that same path?
[32:40] I kind of already gave my opinion on that. I think it's going to be very difficult. Is it possible that BISC did not take off because of Bitcoin fees? Or is that not the
[32:58] thing? I think there is also another reason, is that it's hard to adopt because you have to download
[33:09] the client on your laptop. And with the local money, our goal is to allow you to use it on your mobile phone, to use it from your web browser so that it targets more people,
[33:29] more audience to use the local money. Yeah, that's a significant issue, I think. That was one of the big problems with BISC.
[33:39] Yeah. I remember people saying that that was another reason they thought that this is not that related, but open bazaar, why they thought that that didn't go anywhere. Because, again,
[33:49] you had to keep basically acting as a node all the time. So, Mikhail, do you just hope that it's possible that no one has to act as a node in this case, or you know it's possible?
[34:00] And if so, why has no one done this yet? Yeah, what are the tradeoffs? Because they were obviously requiring that you download
[34:07] the software to your own machine so that there was more or less no middleman. So what are the tradeoffs to the solution that you've proposed?
[34:19] The tradeoffs is in, the first, the BISC have, you have to download the client. In the local money, you can have an application on your web browser and you can have just, you can
[34:37] visit via your browser. So the tradeoffs between usability and, and, and the, like, yeah, yeah, the convenience of using the application. Yeah, the project, like, the project that
[35:12] we're bringing is surely possible. Like, it's, it's, it's, I know how to do this. So that's why, why we are building it.
[35:24] And maybe it, maybe it was just, maybe it boiled down to, they didn't have anywhere to store data in a decentralized way. And their, their solution to that was storing
[35:34] the data on everybody's node. But maybe that's exactly what Dash platform solves. I happen to think that, you know, it might be tricky to solve that problem without, without some
[35:48] kind of execution engine on the backend. But I think it's also a solvable problem. Maybe, maybe you could do that on the front end. Actually something that I, I've wondered about
[36:00] for a long time, whether we actually ever need execution on the backend on Dash platform. So I do think it's solvable. The other, the other issue, the other challenge that I think
[36:12] we will have with this is just the, the amount of time that it might take and resources. Do you think with your current budget that, that this is something that you can have a
[36:23] successful project with, with your current budget? We will see, we will see. I think it's doable. I don't think that will take that much amount,
[36:34] but with my budget, we will see how, how it goes. If it will take really a lot of efforts, we will, we will think about that, maybe redesign or, or do something about this. At least we
[36:51] will posting the results of this project and we will, we will be able to see, we all will be able to see whether this is a good project or not.
[37:01] Yeah. So along those lines, if I had any kind of recommendation or advice, I would say focus on just one feature, the most, the one feature that you're trying to solve the most, which
[37:13] might be fiat to crypto and crypto to fiat, and maybe just atomic swaps or something that you leave to other projects until you have more budget to work with. Because my experience
[37:28] with incubator in general is that we are spread very thin and my mistakes have probably mostly boiled down to too many projects, not enough developers to make many of them successful.
[37:43] And so that's why I've actually pivoted to being focusing more on one, two or three projects, three projects max that I feel comfortable with taking on, which is why I didn't take
[37:57] this project on because projects just need a lot of focus in order to be successful. So yeah, if you could just, you know, solve the one problem that you want and do it well,
[38:11] I think this problem, this project could succeed. Yeah.
[38:15] And I want to follow up that comment with I'm glad that you have taken on something so ambitious, Mikhail, because it seems like the other stuff that you took on over the
[38:26] past year or whatever is more or less under control or fixed or fine, I guess I'll say. And so now that those things are like, hey, all the fires are put out, I'm glad that you've
[38:43] seen that you have the bandwidth for something new and it seems fairly ambitious. Let's read TL's comment.
[38:49] Does the minimum viable product have to include a third party escrow? Would it just include connecting two parties together so that the in-person meetup could
[38:58] happen like Amanda described? Yes, the MVP will include the escrow as the minimum viable product feature.
[39:06] So yeah, that's the first thing that we want to make. Sorry, you said that having escrow is part of the minimum viable project?
[39:16] Well, yes, that's the first thing that we want to make done. Can we talk a little bit more about how that third party escrow works then?
[39:29] You said that... Oh, sorry.
[39:31] I mean, multi-sign signature and not third party. Oh, just like a two of two, where if one of the two parties disagrees, the funds get
[39:44] returned and that's without an escrow agent. Yes.
[39:48] Yes. Yes.
[39:50] Exactly. Well, now that I think about it, what is the point of having a third party escrow agent
[39:56] if just one dissatisfied party can... Oh, yeah.
[40:00] Because... Yeah, because that actually involves a good deal of trust because maybe if we trade in
[40:06] person and the trade goes well, but then I dishonestly just be like, "Nope, I was unhappy with the trade," and then I get both.
[40:15] I keep my crypto that I traded for and I keep the... Right?
[40:21] Am I making sense? Well, I think what the problem is, is it's very difficult to make an atomic transaction
[40:30] in the fiat world because, for example, if I'm on the fiat side, let's say that you and I are doing a trade, Amanda, and you want my fiat, you want my dollars, and I want your
[40:43] crypto, and let's say that I'm going to do that through my banking app or something that's reversible is what I'm trying to get at.
[40:59] I send you fiat in a way that's reversible, but you send me the crypto, which is irreversible, that's tricky because I can reverse my transaction and keep the crypto.
[41:14] But yes, go ahead, Mikhail. I think you had something to say about that.
[41:19] Yeah, so the idea is to make it trustless so that you don't have to trust a third party. So that's why we're building these two or three multisignature transactions as part
[41:32] of the escrow. I'll ask this viewer question and then I have one more of my own.
[41:41] Herman wants to know, would this be all based on platform using Dash usernames for those transactions?
[41:50] Not explicitly, we haven't thought about this yet. So probably not initially, at least.
[42:03] Yes. Yes.
[42:05] Okay. I have a question for you, Mikhail.
[42:07] Would you use this application? Of course.
[42:11] I would like to add some rebels trading pairs. So like, would you?
[42:17] Okay. Yeah.
[42:19] I guess I just asked because I can only imagine that as a developer, how challenging it would be to build something that I didn't intend to use myself without a ton of market research
[42:32] first. Yeah.
[42:34] Yeah. Yeah.
[42:36] So, yeah, actually all of my products that I do in the Dash Encryptor, almost all, yeah, all of the products I usually use myself, like everything that I do.
[42:51] Okay. Do we have any more questions?
[42:56] I know that you had said, Mikhail, that you want to hear more from people about, I don't know, what they want or what they're concerned about or whatever.
[43:06] And so I imagine if anyone watching this not live wants to reach out to Mikhail, you know what his contact information is, it's in the description section.
[43:17] And absent any final comments, I think that will be it for us today. Yeah.
[43:23] Yeah. I think that's good for me.
[43:27] Okay. Good.
[43:29] Well, we look forward to getting an update about this project. I hope sooner than later, Mikhail.
[43:34] And yeah. Godspeed.
[43:36] We'll see everyone next week. For the second half of the Newsreel.