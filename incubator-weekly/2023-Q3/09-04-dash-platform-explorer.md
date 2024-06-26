---
showLink: "https://www.youtube.com/watch?v=S1mb7_U7u3Q"
slug: "dash-platform-explorer"
title: "Deep Dive Into Dash Platform Explorer"
publishDate: "2023-09-04"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/S1mb7_U7u3Q/maxresdefault.webp"
---

Dash Platform Explorer, a new tool to visualize and explore data on the Dash platform, is discussed in-depth.

## Episode Summary

tl;dr: The Dash Platform Explorer is a new tool in development to enable users and developers to visualize and explore data on the Dash platform. It will provide insights into data contracts, network health, and the relationship between the Dash layer 1 proof-of-work chain and the Dash Platform layer 2 proof-of-stake chain. The explorer aims to be a comprehensive resource, offering both a user-friendly interface and developer-oriented features.

## Chapters

00:00 - Introduction and SEC Ruling Discussion
The episode begins with a discussion about a recent court ruling in favor of Grayscale against the SEC regarding crypto-related exchange-traded products.

05:09 - Introduction of Ash and the Platform Explorer Project
Ash, the incubator strategist in charge of the Platform Explorer project, is introduced. The importance and purpose of the Platform Explorer are outlined.

08:35 - Existing Dash Explorers and Their Limitations
Existing Dash explorers, such as Insight, and their limitations are discussed. The need for a dedicated Platform Explorer is emphasized.

16:38 - Third-Party Blockchain Explorers and Dash Platform Support
The likelihood of third-party blockchain explorers, like BlockChair, adding support for Dash Platform is considered.

23:10 - Data Contracts vs. Decentralized Applications (DApps)
The difference between data contracts and DApps is clarified, with data contracts being the building blocks for DApps.

27:35 - Tendermint-Based Blockchain Explorers
Examples of Tendermint-based blockchain explorers are shown, illustrating the type of information the Dash Platform Explorer aims to provide.

33:44 - Dash Platform Explorer Design and Features
The current design and planned features of the Dash Platform Explorer are presented, including network health, data contracts, and user growth metrics.

40:52 - Core vs. Evo Transactions and Blocks
The distinction between transactions and blocks on the Dash Core layer and the Dash Platform (Evo) layer is explained.

45:36 - Smart Contracts and Decentralized Computation on Dash Platform
The need for smart contracts and decentralized computation on Dash Platform is debated, with the focus being on decentralized data storage and verification.

49:38 - Dash Coins and Platform Credits
The relationship between Dash coins on the layer 1 chain and credits on the layer 2 chain is discussed, including their interchangeability and potential valuation differences.

## Transcript

[00:00] [Music] Last week, the much criticized regulation through enforcement strategy of the Gary Gensler led
[00:12] Securities and Exchange Commission, or SEC, was checked by a ruling from the United States Court of Appeals in DC. Their decision, in support of Grayscale, a crypto asset management company,
[00:22] against the SEC, was celebrated by many in the crypto-verse. Crypto just went crazy, folks, and it's all because the SEC has just had another absolute
[00:33] nightmare day in court. This, folks, is what you call a good day. But what exactly happened, and where do things now stand?
[00:40] Grayscale, like many other companies, had solicited approval from the SEC to offer their customers derivatives, also called exchange-traded investment vehicles
[00:49] or exchange-traded products. And Grayscale, like many other companies, had their request rejected by the SEC. So, Grayscale sued, filing petition for review.
[00:58] After hearing oral arguments from SEC bureaucrats, Grayscale's legal team, and supporting entities who had filed amicus briefs, the court issued their finding and sided
[01:08] with Grayscale. That doesn't mean Grayscale can now go ahead and offer derivatives. It just means that the SEC must revisit their own decision-making. And only then, if they aren't able to give another
[01:17] reason that Grayscale should be prevented, then Grayscale should be given the go-ahead. In light of the court's ruling, the SEC postponed their decision on derivative applications from
[01:26] seven other companies. In the recent Grayscale decision, the need for "consistent and predictable rules" was outlined. This because the SEC had given the green light to two other firms to
[01:36] offer derivatives while declining Grayscale and many others. Further, these two approved firms have a surveillance-sharing agreement with the regulator, something other companies are willing
[01:45] to do to gain approval. Yuck. The SEC claims that it has acted out of concern for investors, and the public interest. But does receiving a blessing from the regulatory regime ensure this
[01:55] occurs? Consider FTX, which specialized in derivatives, which imploded despite having regulatory sign-off. FTX had exerted their power to enter this market. Rather than petition
[02:06] regulators for permission, they spent upwards of $2 billion to acquire companies that already had regulatory approval. Grayscale also exerted their power, not through a massive outlay of capital,
[02:16] though I'm sure their efforts weren't inexpensive, but through personnel. The person who headed up their suit against SEC is Donald Varelli. He's not only former deputy counsel to Obama, but the
[02:26] former US Solicitor General, a position some refer to as the 10th justice of the Supreme Court due to having an office in that building and representing the federal government in all cases heard in that
[02:36] venue. I think it's fair to say he's not a cypherpunk, but a DC insider through and through. So what's the deal with these derivative markets anyway? My odds are good. I'm on a winning streak.
[02:47] Everybody in this place wants to get in on the action. I love Selena Gomez. I bet you $50 million she wins. And I'll give you three to one odds. Three to one odds? Okay, I'll take that bet. I
[02:59] bet you $200 million that lady in the glasses wins that bet. She probably will win, so I want a great payoff. How about 20 to 1? Deal. And this will go on and on. And we can transform an original $10
[03:13] million investment into billions of dollars. Why are all these companies eager to gain permission? Companies like BlackRock, which has over $8 trillion under management, a number larger than
[03:24] the gross domestic product of all but two nation states, and which already has a sizable chunk of Bitcoin mining, perhaps to try to capitalize on or control the emerging crypto market. Grayscale,
[03:35] by the way, is said to own 3.4% of all the Bitcoins in existence. Not insignificant. So why was this story such big news in the cryptoverse? Sure, Gensler seems content in his role as archvillain
[03:46] working to throttle crypto, so it's refreshing to see him put on timeout. But is this a fight worth watching? I mean, we're talking about regulators and huge corporations. Are either
[03:56] relevant to decentralized cryptocurrency? I suppose as motivating factors to why decentralized cryptocurrencies were created in the first place and continue to be built. But that's about it.
[04:06] After all, what these firms seek to do, offer derivative trading for customers, is a long way off from self-custody and real-world use. Like FTX before it, Grayscale touts its regulatory
[04:16] approval as attractive. And like all the other corporations hoping to get into this game, the Grayscale peeps apparently don't believe you're competent enough to hold your own coins.
[04:25] At the end of the day, choice is good. So admittedly, this Grayscale ruling is a positive. If people want to put their money into derivatives, that's their prerogative.
[04:33] But it's not exactly a strategy of liberation. It's not exactly eroding the legacy institutions. What world do you want to live in? A world where billions maintain their own private keys and
[04:43] engage in voluntary interactions? Or a world where a few megacorporations hold the private keys and monitor every move? A world where transactions are fluid and unmanipulated?
[04:53] Or a world where yet another medium of exchange has houses of cards erected upon it? A world where individuals are responsible for their own actions? Or a world where intermediaries
[05:03] position themselves as gatekeepers? Through our actions, we can each help to create the world we want to see.
[05:09] Hello, everyone. Welcome to Incubator Weekly. How's it going, Rion? How's it going, Ash? Good, thanks.
[05:25] Great. So we are talking about the Platform Explorer today, which is currently in development and which is new and different enough that I basically have zero to say about it now.
[05:40] So let's just go straight over to Ash, who is the incubator strategist who is in charge of this project. And you may remember that it was first shown to us briefly a couple of weeks ago
[05:51] by the developer working on it, Mikhail. Okay. Yeah. So Platform Explorer. It's one of these things where it's not the sexiest project
[06:02] out there, but it's really important. It's important for our devs. It's important for our community to be able to actually see the information that we have going on in the network,
[06:10] both in terms of layer one and our actual network health and everything that's going on the platform. You need to be able to search up data contracts, see what documents are being written to them,
[06:21] what users are active, see how well it's performing. And really, this tool is just a tool. Ultimately, if you've ever used a blockchain explorer, this is a very similar
[06:31] tool, just more focused around Dash Platform. Ultimately, right now, we have tools like Insight and we have third parties like Blockchair and so on. I'll go through those. But the reality is that
[06:43] they are designed for our existing sort of infrastructure and core. And there isn't really a tool out there that's designed for platform. Platform is new. Whilst it's based on Tendermint,
[06:55] it has a different focus. So none of the existing sort of explorers that are built for that ecosystem are really quite suitable because they don't have that data feature. This is something new. This is
[07:06] something where unless we build it, there isn't a tool. It's not like we can hook into a multi-party explorer and have this tool because it doesn't exist out there. So for us to actually have that
[07:19] data accessible, then we need this explorer. And there's been attempts at it in the past, but this is now to get everything back on track with all of that and have that data.
[07:28] - So just a quick question before you jump in, and I'm sure you'll probably answer this question. Is it focused more than on the data contracts, exploring the data contracts?
[07:40] - It's everything. There is a huge wide area that I want to eventually challenge with this explorer. The first goal for that is to see everything that's happening on platform. So
[07:53] that will include all the sort of state transitions that are happening there. So all of the data contracts, all of the documents being written to them, all of the identities,
[08:01] everything that's happening, all the consensus, the validator sets and how they're working, the health of the network. Are they writing to it fast enough? What's the response time of our API
[08:13] for the decentralized API? How well are we doing all this? And what's the adoption rate? I think bringing a lot of transparency to those metrics and enabling sort of that data access is just
[08:25] really important. - Cool. - So is there a visual we should look at first? - There are some visuals. Yeah, I can run through
[08:35] some things, definitely. I'll switch over to presentation mode. I'll go through my entire screen. There you go. - Because I have a lot of questions.
[08:47] - Of course, yeah, absolutely. So I'll try and not go through things too fast. You know, firstly, let's talk briefly about Insight. Obviously, this is a tool that we've all used.
[08:59] We've all used different explorers. Insight is maintained, but it's not perfect, you know? It has some issues, and it is something that's kind of become a bit outdated, really. You know,
[09:10] it's a basic tool. - I have a question already. When you say Insight, first of all, is this maintained by DCG?
[09:17] - Yeah, this is maintained by DCG. You know, it's a minor project. I wouldn't say it's something that they're largely focused on. It's important that they keep it up to date and it
[09:25] keeps running because there are people that rely on it. And it is sort of, it's been a developer tool. You know, you can query it, the actual, the Insight sort of API behind it, you can query,
[09:36] although those aren't, like, the public endpoints aren't particularly well documented. So I had to kind of, like, reverse engineer those to kind of find out where they were if I wanted to query the
[09:45] actual live site. - So when I go to BlockChair or BlockCypher, are they pulling from Insight, or do they do their own thing?
[09:54] - No, so they'll have their own. So anyone like BlockChair or BlockCypher, they'll be running their own nodes. They'll be ingesting that data from their nodes, storing it in their own way,
[10:02] and then delivering that differently. So Insight's more for sort of solo devs and smaller scale operations. You know, any enterprise group like, yeah, BlockCypher or BlockChair are great examples
[10:13] or, you know, blockchain.com or even any exchange, they're going to be running their full node architecture. But for example, Spark, you know, small payments app was using Insight, and it's
[10:24] something where they can quickly scale. And I think it's really important for developers. And this is the whole, you know, point of DAPI. We don't want, oops, sorry. We don't want everyone
[10:32] to have to build and run their own node architecture to be able to develop against Dash and against platform. And the SDK is great for that, for developing against it, but we need
[10:42] that extra data source. And you can't really have one without the other. Having the ability to read data programmatically without the ability to visually explore that data creates this sort of
[10:54] unbalance. So yeah, I mean, Insight is a great tool. It's very useful for, you know, the time it was. It is a product somewhat of its time. You know, it does have live data. It all comes in.
[11:05] It's got, when you first load it, you're waiting for the latest transactions, but you can see what I mean. Like there's a good amount of data in there. There is some data that's kind of missing.
[11:12] So you can't see, obviously, that, you know, a transaction has an instant lock without looking at the actual code. And that's not the lock time. That's not related. You know, block proposers,
[11:24] like there's not much, we can see the block where it was mined. There's just like a lack of data. And we've ended up with multiple tools serving multiple purposes. And I kind of believe in this
[11:34] future where we have DAPI, which is providing the actual write and sort of true to the source data. And then the Explorer, which is providing all the ancillary data or the cache data.
[11:47] And I'd like anybody to run their own sort of Explorer, even just for their own API. It's just another approach. I've been looking at how other chains approach this, where they can get
[11:57] their developers onboarded quickly, but also production apps, which are very simple, that are relying on this sort of hosted API. And that's what a lot of our production apps will be doing.
[12:08] They'll be relying on the hosted decentralized API, but without more performant data and more just ancillary data, just data that's built up from the existing sort of blockchain and platform
[12:21] data, then it's not a useful tool. And if you can't explore that information, actually browse a data contract or see the history of that, the documents uploaded against it, you're blind.
[12:33] So we need an Explorer. It's not a, there has to be an Explorer, ideally immediately upon platform release, and that's quite capable. But it's something where we don't really have one up to
[12:46] here. We did have one historically within the incubator, but that's almost abandoned, where that was back in 2021. So this is kind of being built from the ground up to the current spec of
[12:57] Evo, really. Okay. So then you were going to tell us next about Tendermint Explorers. Well, yeah, I'll go a little bit onto Insight. So you can see down the bottom right here,
[13:08] we're running Insight 4.05. We're actually significantly far behind because Insight actually was made by BitPay. Obviously, the two have diverged. Not everything that BitPay builds
[13:19] is going to continue to be compatible. But there is, you can see down here, we're on version nine on BitPay. Now, this isn't a significantly better Explorer. You can see there's not a lot really
[13:30] going on here. One thing that it is, is it's very performant. So I can, as I'm doing this, it's scrolling in and bringing in more and more data. It's a very performant sort of tool,
[13:40] but I wouldn't say it is a case where we can just say, "Hey, let's just upgrade to the latest Insight and be covered." Because whilst that might cover us for some of layer one, we'd be losing
[13:50] other features that have been built into Insight and not covering anything platform. So it's not a case where we can sort of go, "Oh, let's just follow the upstream sort of master and then get
[14:02] our Insight up-to-date following that." >> It also looks like Insight's probably moved on to being a multi-chain Explorer. >> Yeah. Yeah. I mean, ultimately, they don't
[14:13] have Dash on here. It's just BitPay's own product, but we can bring Dash into this and just have only Dash. The way they've approached this is they've kind of created a whole new sort of
[14:24] set of tooling where they've got their own node, which ingests all the data from the nodes and normalizes it. This is actually with CTX. This is similar to what we do where we take all the
[14:34] different sort of arguments and queries and try and create a standardized way of querying the nodes and the datasets and storing that data in our own database. So they've got some really good
[14:46] bits there. I think there's a lot to be learned from how they've approached this. And I think that based on this and the current sort of knowledge that we have, which wasn't there when
[14:56] Insight was built, but I think Insight probably originated in 2015, '16 or something, like it's an old project and there's some legacy technical debt there. So we've got an opportunity to have
[15:06] like a seismic leap forward and do everything as best we can from the start here. With sort of a developer-driven sort of mindset, we still want the actual visual Explorer, because I think
[15:19] that's important for the network and for anyone to actually click into your data contracts and see the information. But I want to have this developer sort of tool set as well behind it, because that
[15:29] will both empower the actual user interface Explorer, as well as the developers. So yeah, I mean, the next thing on that one would be to say something about the other Explorers. Amanda,
[15:43] you mentioned earlier about BlockChair. They've got a very weird logo for Dash. I don't know what this logo is. If anyone has a contact at BlockChair, I would know. They weirdify all the logos. If you
[15:54] go back, it's just, they put their own little branding and style on all the logos. It's better than the old Dash D anyway. Yeah, I just feel like they particularly butchered ours. So it's strange
[16:07] considering the logos are all kind of like standardized, but yeah, as you can see, there's more information here. We've got some like kind of network data going on. We've got a bit of
[16:15] information here. At some point, it might be that BlockChair will implement some kind of platform Explorer, but we kind of need to take the lead on that front and not rely on the third party to do
[16:26] so. Yeah, I doubt it, because they're just focused on the layer one blockchain. Exactly. They're not going to make a block Explorer just for Dash performance. Yeah, the most likely sort of group
[16:38] to add Dash features to, well, platform or Evo features to their Explorer is someone that's already built an Explorer for Cosmos. So a tendermint sort of familiar Explorer. Ultimately,
[16:51] there would still be a lot of new features for Dash support. So it's not particularly likely either in the immediate sort of future. So we need to kind of do this ourselves. And even us doing
[17:01] it ourselves means that other people can do it in time too. One thing that they do really well, though, is they, if you go back to their other page, I think it's just back one or something.
[17:10] This is the homepage. Go forward one now. Oh, sorry. Yeah. The thing, the filters, the data. They have great filters. They even filter on special transactions. I particularly like their
[17:23] wildcard sort of search as well. Like you just, you know, instead of matching, you can kind of do this sort of like deeper search. But yeah, you can filter everything like that. It is a really
[17:35] powerful tool. And I think there's some things where they'll have done more stuff here than we could do in the immediate future, really. Like, you know, it's a complex tool. It's more advanced.
[17:44] There is some of this you can kind of like download sort of pre-made tools to kind of do some of that. But it's also in terms of the sort of architecture of the database to begin
[17:53] with and how we're populating that data and creating indexes and the technical knowledge. I'm okay, but I, you know, I'm going to defer to Shemek on the actual and Alex on that. I know
[18:04] we're going to be using something like that Elasticsearch and then RedisCache on the front end. You know, it's going to have quite a lot of moving parts to it. But I'd like to get to
[18:13] a stage where we've got at least a few useful filters for, you know, both the development and from the UI. What would we be filtering? Because what I just keep wondering with this notion of
[18:24] Platform Explorer is, okay, I've been shown the example data contracts. And in this case, I've been shown business use cases. So I'm wondering, is a Platform Explorer going to
[18:36] show my competition like how many pizzas I'm selling? Or like- Well, that's the thing, isn't it? You know, you've got this question and it's a question that,
[18:45] you know, I don't have a definite answer to. That's ultimately with something like this, are you revealing too much data? But ultimately, if that data is on chain and that's transparent,
[18:54] you know, that's how it is. I do think that there is a question of some of the privacy features, and there might be a case later on where more privacy is brought back into a platform to a
[19:06] degree and to the layer one side of things. Because for example, right now, the whole social graph is entirely public. So every friend I add, at least this is my understanding,
[19:16] maybe this has changed more recently, that every sort of connection to every other connection is public. So I get to see who you're connected to. And, you know, there's some complex questions
[19:30] around that and what that means for, you know, for users' privacy. Ultimately, I know we're going to be, most people are going to be using pseudonyms with this, but then this creates links
[19:39] between pseudonyms and links between people. - It would be like high school all over again. - There is a lot to it. Yeah, a couple of good things to note is all the data that you put onto
[19:51] platform you can encrypt. You don't have to, you know, you don't have to reveal private information on there. You can upload encrypted data that only you and your chosen sort of recipient or the
[20:02] decentralized application you're using will actually be able to understand. So, you know, there are some caveats there. - Yeah, I think that probably what
[20:12] you're going to see, I'll just give my opinion on this. I think the platform's mostly going to be used for data that's intended to be public. I imagine like one use case that I see being a
[20:33] viable use case is offering some kind of credit and loans on Dash platform and then tracking things about those loans. Or for example, let's see, I kind of lost my train of thought here, but
[20:55] also like reputation. - This is completely sort of like transparency and like that sort of immutable timestamp. It's like being able to
[21:04] notarize anything immediately and have that record of proof. Like there's so many use cases to it. It's like on that front, you know, I completely get the insurance one. The micro insurance one
[21:16] is a great example that, you know, the DFS has actually been involved with a company that does that and they were looking at using Dash, but Dash wasn't quite suitable for it at the time doing it
[21:26] as, you know, opt-return sort of data, but with platform it would be. You know, you could even have data which you subsequently reveal, you know, any sort of like online casino type site that
[21:37] operates on this sort of provably fair model. You can, you know, they can share, you know, the encrypted sort of, you know, code of their sort of whatever seeded their table, their roulette
[21:49] table, whatever it is. And then they can reveal that encryption afterwards and it'll cost them nothing to do so. And then there'll be transparent, you know, confident immutability and that like
[21:59] reassures users trust. But there's, you know, there's thousands of use cases and both the, for the encrypted and the unencrypted. You can also store immutable, both immutable and
[22:08] mutable data on platform as well. So everyone can browse this. It's not like someone's going to trick you by uploading a field that's, you know, this is another reason you need a browser.
[22:17] You need to be able to understand the schema of a data contract and having tools around that. You can't just trust a application, a decentralized application or a developer.
[22:26] You need to be able to verify that. And you need to have tools to enable you to do that as a user. We don't expect everyone to be able to understand a JSON schema of a, you know,
[22:38] a data contract just from reading that. We need to be able to communicate that, break it down, explain which fields are required, not required, which fields are immutable, which ones are
[22:47] mutable, you know, which ones are dynamic that you'll enter and which ones are automatically entered. It's everything like that. There's so many different parts to this that we need to
[22:57] create tooling around it for both developers and users. But yeah, Botshare aren't going to be the ones to do it. >> Right. My next question is super basic, which is when we say data contract
[23:10] and when we say DAP, decentralized application, are these the same thing? Are these two different things? >> No, two different things, really. So a data contract is kind of like a schema,
[23:19] like a structure. Like imagine you're filling in a PDF. DAP developers will create data contracts for their various decentralized applications. So even Dash Pay is based around data contracts. I
[23:30] think there's maybe four or something. >> So like the DAP is the umbrella up here and there are data contracts under. >> Yeah. So a DAP can just be a front-end
[23:38] sort of piece of software that then tells you to write, instructs you to write to various data contracts. And through those data contracts and the data that's written to them, that creates the
[23:49] whole everything behind the decentralized application. You know, whether you're pulling in that data that people have written. You know, let's go off the gaming thing again. We're playing
[23:58] roulette. I'm the DAP developer. I've created a data contract for just roulette, a generic roulette data contract. And people can bet and they can register their sort of deposits and funds to that.
[24:11] And then they can make their choice. They can say, you know, I'm going to bet it all on red. And they can write that to my bet data contract, which is like a child of my roulette data contract.
[24:20] You know, like it creates this sort of structure behind it. And then the decentralized app developer can use that to actually sort of power their app. But their app, you know, it's going to be this
[24:31] open source front-end code executing on the client's machine. Sorry, I'm getting a bit too technical here. But the advantage of it is that it is all transparent and the data behind it is
[24:43] stored securely on the blockchain and cannot be modified. You can't front run it as some sort of middleman unless you are somehow stepping between them. It's just important. Just the transparency
[24:54] and the immutability of it is important in so many industries and verticals. This is not a restricted to gaming or niche sort of notarization and corporate structures like any. There are many
[25:06] businesses that use this kind of like data or flows that could take use of Dash platform in various ways. And they need all those users, both the business case, their engineers and developers,
[25:19] their business analysts, everyone needs to be able to, and their customers, they all need to be able to explore this data. You can't require someone to actually run some CLI and then query it
[25:33] and then understand a massive dump of encoded data. You need to be able to create tools around that that makes it easy to understand, makes it comfortable. And also for checks and balances.
[25:44] - Yeah. James wants to know, "Developers are quite costly. Are the developers going to be the gatekeepers, quasi middlemen between platform and the end user?"
[25:54] - No, not at all. At the moment, there is a little bit of that, but anyone can create a data contract and they can create decentralized applications around it. I mean, just look,
[26:04] right now there's Dash money or Dash get paid or however, which project you want to talk about. And they've come before the network. They built an example project using Dash platform, using data
[26:17] contracts, and they've just done that as a developer. It was permissionless and they were able to build a decentralized application and get funded to continue building that decentralized
[26:26] application. The only caveat I have to that is right now, there is some functionality, which is, I wouldn't say like gatekept and locked down. It's just because this is early release.
[26:38] I won't be mean and say alpha, but let's just say beta, maybe it's alpha software. And there are some features which are kind of being enabled around specific use cases. So what I'm talking
[26:51] about here is just like these data triggers. So these are things where a layer one action can happen. So a Dash core, whatever layer one, a normal Dash transaction, as we currently have
[27:05] them, can be related to a functionality on Dash platform. So there are a few of these data triggers. In the future, I hope that those will be kind of created in more of an open format where
[27:16] developers on platform can make more use of them. But I completely understand that right now that's something where it's built around specific use cases and features and specific data contracts,
[27:26] really. But in time, I believe that will open up. >> Okay, so you've got several tabs here. >> Yeah, yeah, let's keep going. >> All of them?
[27:35] >> Yeah, I'm going to go quickly through them. So obviously, I've talked briefly about like layer one explorers. We also have other tooling built around Dash, which is kind of here and there,
[27:45] and it has a lot of value. And I'm really enthusiastic about the creators of this kind of thing. But there's a lot of that data that could be sort of normalized and just brought in
[27:54] and made sort of more sort of public. So if you look at this sort of fraction data, like siloed data, it's not even siloed because anyone can access this data. It's just there's been lots
[28:05] of different approaches and there's nothing wrong with that. But I'll just go through them quickly. So we have Dash Ninja here. It has governance data. It has some blockchain data, explorer
[28:16] and things. It's by Alvarezon. It's a great tool that's been around for a long time. It's pretty much free maintained and he asked for some funding for the actual hosting of it. But it's a useful
[28:27] tool. You can get a lot of data from this that might not be so visible elsewhere. Likewise, we have Moocow's masternode me data, which talks about some various sort of Dash data that's pulled
[28:40] from multiple sources. We got other dashboards. So we've got M&O Watch. So ASKCD and demos project has various dashboards. So we can see nodes by country and protocol versions and all
[28:53] this kind of stuff. So this is great data. I think a lot of people will be familiar with some of these, but maybe not all of them. Dash new user ID, some sort of visual dashboard. You can have
[29:02] this full screen on the monitor to have a look at. You can update it with your Dash addresses and things like that. So you can see your revenue. It's just quite a lot of tooling that's been
[29:13] created around Dash. It serves people for various purposes. But it's often sort of like fragmented and, you know, some of these tools break quite regularly for whatever reason, whether they're
[29:27] not running the latest version of Dash. And this data, you know, if you wanted to access this data as a developer or you were relying on this data for whatever business reason, you need to be able
[29:36] to query that. And we don't want people to have to query so many different sources in an ideal world. Now, I'm not saying, you know, it makes sense to have a lot of sources and a lot of
[29:46] availability of this kind of service, which is why this is obviously all going to be built open source and to a structure where anyone should be able to deploy this. Admittedly, you will need,
[29:56] you know, a server or a good computer to do so. But anyone should be able to deploy this and get all this information. So here's a little comic, obviously, you know. >> I was thinking of this
[30:07] very thing, actually. >> Everyone's trying to do all of this, you know. Now we need a universal one that covers everything. And now there's another one. To a degree, it applies in some parts,
[30:17] you know, especially Layer 1. There's a lot of Layer 1 explorers. And this is just going to add sort of another one when we add Layer 1. But that is a later feature. Right now there is no platform
[30:26] explorer. That is the core of this. Whilst I do want to create ancillary tools around that data, you know, ingest that data, do calculations on it, create tools which don't have an existing
[30:38] endpoint in DAPI or in Dash at all, yeah, there is a question of, you know, new tools there and just adding that. But I'm hopeful that we'll be able to get this to a point where it has its own
[30:50] unique usage in terms of platform, but also it serves other areas, you know. I'll go into some of those other areas momentarily. So, now we've gone into the crazy world of much more detail.
[31:02] You saw insight. We've gone from this to, you know, something where it's hugely involved. So, this is a interchain, blockchain of blockchains, Cosmos Explorer. Not that complex. Same sort of
[31:14] thing. We've got blocks. We have transactions. We have accounts. So, identities, usernames. We have all sorts of, well, this is just like wallets, effectively. You know, validators. So,
[31:27] this is the same for us for our Evo nodes. So, you know, the 4K sort of master nodes. They'll be, you know, some of them might not be signing very well. Some of them might not update
[31:37] very fast. And we need to be able to see how the network health is looking. You know, we want to make sure that we're not getting compromised, that there are, you know, XKCD does amazing
[31:47] profiling on people's, and Demo, they do amazing profiling on the wallets. And we don't want it to be a case where Binance and Coinbase are holding, you know, 60%, 70% power over the network. And
[31:59] we want to ensure that there's some bare metal nodes there. There's, you know, mixed providers. There's some on AWS, some on Azure, some on Google, some on, you know, OVH. There's,
[32:08] they're all over the world. So, being able to see this sort of network health, both in terms of response speed to APIs and things like that is going to be really important as well. Proposals
[32:17] doesn't, it applies for us, but it's not the same sort of thing here. You know, I do have another project that's a proposal explorer. Maybe that will end up brought into this as well as kind of
[32:26] like a single power tool, hopefully, or not necessarily a single, because there's always going to be other tooling that people grade, but it should be like a useful resource to cover.
[32:35] The Walmart of- Yeah, it's just like, yeah, like Uber, let's say Uber, you know, like a super app. So they cover,
[32:42] you know, your food, your, your taxiing, your courier, whatever else it is. So we'd like to have like quite a few different features, but you know, right now we're focusing on doing one thing
[32:52] fast and iterating. So, you know, whilst I'm getting ahead of myself with all this, this is going to be a long way off before we're like layer one and we've got all these ancillary functions
[33:01] around it. There is some stuff that can be done in parallel and I'm going to be working on some of the lesser deep dive coding stuff myself because, you know, why not? Resources are limited
[33:10] right now and do what I can on that front. So, you know, this is a Cosmos Explorer. We can see all this kind of information on it. So that's kind of like gives you the mix of the difference. Same
[33:21] with this one, AsmScan. In future, they could kind of add maybe some data, you know, exploration stuff and that all of this would be easy for the sort of validators and the blocks, but it wouldn't
[33:32] be easy for the actual data contract stuff. That would all be bespoke development. So we got to do that first. Even if it's just a reference for them. So Dash Explorer, Dash Platform Explorer.
[33:44] So this is only represents my weekend's work. So this is me coming up with sort of a UX sort of flow for it of what we might look to see on it. How we can see what's going on with the network
[33:57] and kind of network health. Early days, but I wanted to make sure that there was something more visual than what Chen McMichael demonstrated before. He's a developer. This is how development
[34:10] is done. You start off with, well, can be done. One of many ways. You can start off with something that's just UX simple, dumps the data out, and then you worry about, you know, polishing that,
[34:22] you know, form follows function, ultimately. So the goal with all of this is just to make things both visual for users that are browsing data contracts and, you know, looking at the
[34:36] network health and looking at transactions, but also useful for developers too. So ingesting all of that data and making it usable for, you know, various things. So really at the moment, this is
[34:48] just, you know, a starting design, a first pass on everything to allow sort of me to build upon that. So we're still at the exploring stage, looking at the data that we have available to us.
[34:59] Really. I think my Mac's just shut down, which might have killed off the server that I'm hosting this on my Mac behind me. I think that may have just killed it off. I can cover some of that. So
[35:20] we'll be browsing all the, you know, I'm just working on this locally. So I could go fix it, but I can talk through some of those bits on there anyway. Ultimately, it's going to be
[35:32] all the kind of like the validators. So the validator health, it's going to be all the data contracts and their activity. It's going to be the dash pay users. And it's also going to look
[35:42] at the kind of like the growth over time of those users. So as we, you know, as we expand, like I'm going to get as much data as we can. The goal with this is to ingest a lot of data and then provide
[35:53] useful output of that data. Some of that is going to be, you know, what's available right now as a platform sort of node or as, you know, through the Explorer, you know, when you look at this
[36:06] sort of data, it's not going to be super useful. And you then have to create additional data sets based on that data to get that. I mean, this is useful because this is, you know, very granular
[36:17] sort of itemized, but we will need the ability to sort of see things on a top level. Like we'll need to understand more than just, you know, strings of characters that people won't get and encoded
[36:31] sort of platform actions. - That was a very good tease that you had there. - Yeah, I apologize. I mean, I could, one second, give me one second. Let's see. - Okay. Well, while you're doing that,
[36:44] I'll read Halawi's question here, Ash, which is, I believe that capabilities, what does IBC even mean? - Inter-blogstream communication. It's a standard that the Cosmos ecosystem has developed
[37:01] and we plan on, according to DCG, we plan on integrating IBC at some point, but like Ash says, IBC capabilities will be a long way down the road because of how much TenderDash has deviated from
[37:16] TenderMint. So I guess, Ash, if you've understood. - Yeah. Yeah, I had my headphones out, but I can sort of assume context. Realistically, I think it's, everyone's got a different view. I believe
[37:31] in interoperability. I believe that on a level playing field, Dash outshines both in terms of the layer one speed, the security, the fact that it's combined proof of work and proof of stake,
[37:41] and the whole Dash platform. It's something completely new. And I think that we've done a terrible job of communicating that value. Even I understand the value, but I can't communicate it
[37:52] very well. So there is a lot of work to be done there. And I believe that if we connect to these other ecosystems and allow more fluid sort of interaction, then we open the doors for more
[38:02] people to use what our developers are building. It means it's more attractive for entrepreneurs that are building on platform, as well as just easier and accessible. And what better showcase
[38:12] of Dash's both ingenuity and speed, performance, network, everything, than to let people just move into it, experience it firsthand, have that eureka moment, and then hopefully explore more and
[38:27] understand the value proposition of everything, really. So I hope that answers some of it. I don't think it will. It is complex, don't get me wrong. But the fact that there is a common baseline
[38:38] between the Cosmos sort of IBC world and Dash doesn't mean that in the future, there could be some level of good interoperability on there. I mean, there are a lot of entities approaching
[38:50] this and our sort of mass node or Evo node ecosystem is actually what enables a lot of that sort of work. You know, all it takes is those, all it takes, sorry, I hate to oversimplify it,
[39:03] but the, you know, if those, each of those mass nodes, Evo nodes are running the sort of the equivalent chains, they can act, or any of them can optionally act as bridges and relays to enable
[39:17] assets to fluidly move in between those networks. I think it is, I don't believe in building these walled gardens and golden handcuffs. I believe in building value and giving people the opportunity
[39:30] to perceive that value. Sorry, heavy theoretical discussion, but yeah. I got it back running. There isn't much more to show than this, to be honest. There's some like, we were talking about
[39:41] doing APIs and having rates side of things, but you get an idea. - Is there anything like zoom in on the left menu? - Yeah, absolutely. Absolutely. Yeah. So you can kind of see things I'm talking
[39:52] about here, but you know, again, there's, there's a lot more to explore with this. This covers like some top level wins for us. So interestingly, both core and Evo have blocks and transactions.
[40:04] - And what's the difference here? What's an Evo transaction? I know what a core transaction is. - So I can, you know, if I go home here, you can kind of see the last transactions. So
[40:15] transactions can be changes in state. So anything that happens like I'm registering a username or I'm uploading a document to a data contract. - That's a transaction.
[40:24] - Yeah, that's a transaction. You can call them just actions. Transactions kind of implies that there's some monetary side to it, which there isn't necessarily. It's just a, I mean, there's
[40:33] always sort of a fee element of a dash platform sort of credit. But yeah, I would say you could call them actions. I think the, we kind of need to decide on some of the terminology of things
[40:46] there and how we approach that and how we communicate what an Evo block is versus a core block. But we'll get around to that. It's something where we kind of have to do this
[40:55] discovery process and learn what data we're going to be having on this service and what we're going to be ingesting and how we're going to be doing that. - Well, we are getting a little long on
[41:08] the time. I did want to actually try to answer Amanda's question there, because I think there might be some other people that don't really understand how these are related to each other,
[41:21] because there are, in Dash, we have right now a proof of work blockchain, and it's creating blocks every two and a half minutes on average. And every block has a lot of different transactions that go
[41:36] into that block. And with Dash platform, we literally have another blockchain. It's a completely separate blockchain, but instead of being proof of work, it's proof of stake. And the stake is
[41:50] controlled by the master nodes. So you have the same validator set, or at least the validator set from the proof of stake side is being drawn from the master nodes. So that's where it gets a
[42:06] little bit hard to understand, but there literally are two different blockchains. And because there are two different blockchains, the Evo blockchain, the proof of stake one that's a fork of tenderment
[42:18] from the Cosmos ecosystem, that's creating blocks also. And it's creating blocks at a different cadence. I think it's probably what every five seconds, one minute, something like that. It's
[42:32] more frequent than the proof of work blockchain, but it also has different transactions. And those transactions, they are representing different things. They can represent different things,
[42:47] like a difference in the state of if somebody registers a Dash Pay username, for example, that changes the state of the Dash Pay contract. And so that's a transaction. And like Ash said,
[43:01] we could use different names for that. And I think if you've heard the term transition, like a state transition, that's the same idea. It's saying it's a transaction from the blockchain's
[43:13] perspective, the proof of stake blockchain's perspective. It's a transaction just like a coin transfer on the proof of work is a transaction, but it doesn't necessarily
[43:24] have to be a coin transfer. It can be just a state transition. So that's kind of a high level explanation of those two separate things. Because that's important to understand when you're
[43:35] looking at that blockchain explorer, and you see core transactions, core blocks, Evo transactions, Evo blocks, that's because there are those two different blocks.
[43:45] I think it's a really good point that you make about the fact that the proof of stake validators are determined by proof of work from layer one. So our validators on Evo
[43:57] are secured by the proof of work of layer one. So we've got that dual benefit that's kind of like a sort of check and balance just to keep everything still reliant on a really good level of entropy
[44:09] and hashing power from our proof of work chain that also further secures the proof of stake. So there's this just win-win situation, really. Another thing that would be important to highlight
[44:20] in this explorer, I think, would be where is the money tied up? Where is all of the, if you take all of Dash's money supply, where is it currently locked up to use not a very
[44:35] accurate term, but you could also have the connection between those chains. This proof of work chain sent so many Dash units over to the proof of stake side, locked the units on the proof
[44:52] of work side, and sent them to the proof of stake side, and then they're doing different things on the proof of stake side. At the moment, we call them platform credits, because the credits on
[45:03] platform Evo will be able to be used for transactional purposes. So you'd be able to basically pay a decentralized app using platform credits, but right now they can't be withdrawn,
[45:12] as my understanding goes. I'm not quite sure how long that would be until they are. At some point in the future, I imagine there'll be that withdrawal process right now. At the moment,
[45:21] you can top up, but you can't withdraw. Halaway, that is a great question. That's a great question. It's a big question. I'll do a basic answer, but this could be-
[45:36] And the question is, does Evo need virtual machines or smart contracts? Yeah, this could be a whole incubator. So virtual machines, smart contracts,
[45:47] that's decentralized compute. The way I see Evo working is a decentralized output or verifiable output. Any open source app could be used with the same inputs and receive the same output that
[46:02] is stored on Evo. So you're able to verify the app without it having to be run by hundreds of different servers simultaneous, like on the Ethereum virtual machine, for example. Any
[46:14] individual can run that and verify that same output. There are differences. There are differences in terms of applications and value, but again, that is a much longer conversation. I'm a big fan of
[46:25] the platform approach. Obviously, it's early days. It's yet to be proven, but I think it's going to open up a lot more novel use cases. And there's a lot of things that are done on Ethereum that
[46:35] could be done on platform in the future. Some of them right now, but until we've got more in the way of the triggers side of things, which creates that layer one smart contract connection, then we
[46:48] won't be able to do a lot of the more transactional elements and the smart contract wallets and that side of things. But yeah, this is a very big discussion. My short answer is no, to be
[47:00] controversial. I don't think that we need smart contracts. I think that having the data on chain is the result of a smart contract execution. And I see no real reason that we should have to run
[47:17] all of those executions on thousands of servers when the data is really... That's the end result. So it is a longer discussion, but I'll just put my reputation on the line by saying that I don't
[47:33] think that we need smart contracts. It always depends on what you want to prioritize. So of course, if smart contracts, if we could get smart contracts on there just by one mandate of work,
[47:50] then of course, then we could copy all the functionality from the Ethereum land and get it on the Dash side. But it's just, if it takes much longer than that, then you're dealing with
[48:05] opportunity costs. And I think that the way forward is to focus more on the Web2 developers who don't necessarily have to, or we don't necessarily want to have them have to learn
[48:17] Solidity or other programming languages. We want to give them the same paradigm as they're used to, which is you just execute computation and functions on your server, and then you use
[48:34] Dash platform as your decentralized storage. And that accomplishes the same thing, essentially, but it opens up your market to all the Web2 developers who might not even like Web3 and
[48:53] all of that stuff. So they want to build, they want to have their functions written in something other than Solidity, something like that. So anyway, again, like Ash said, it's a long conversation.
[49:06] And there's nuance to even what I said. It's not like I'm against smart contracts. I just think that we have designed the storage of data with a very specific purpose in mind. And that's not
[49:23] really the same thing as doing decentralized compute. But again, there's nuance. To touch base again on the interaction between the two chains, will someone tell me an overview of
[49:38] how I'm supposed to think about Dash coins being on the Layer 1 chain, and these being transferable to credits on the Layer 2 chain? Do I think of them as being worth the same in USD? And why are
[49:53] they needed? Can I get an overview on that? >> Yeah, do you want to take this one? >> I can, but I spoke a lot just recently. >> Yeah, no, I'll do it. I'll take this one.
[50:05] So ultimately, yeah, your Dash is completely equal. You can turn it right now straight into the equivalent on platform. In the future, you'll be able to do the same the other way around,
[50:17] I hope, in the near future. But it's still going to be quite a while before that's the case. Ultimately, this is a different chain. This is a different technology. You can't
[50:26] fluidly move between the existing sort of Layer 1 and how the structure of consensus works on that into this Layer 2 without creating a kind of different asset. You can call it Dash. You can
[50:37] call it the same thing. If it's equal to, if it's fluid, it moves, it burns into Dash or out of Dash, it is very much the equivalent. People call these sort of like wrap Dash or whatever on different
[50:48] services. But the fact that you can move it fluidly and it is always equal to one Dash or whatever it is, or one Duff, then it's equivalent, really. You will need these credits to do
[51:02] platform functions, both in terms of creating these transactions, whether you're writing data or whether you're sort of creating a data contract, registering an identity.
[51:12] Anywhere where there's sort of the network is doing work. Obviously, you can read all this data. This data can be read for free. There's no cost to read that data.
[51:23] So that's something you can sort of do there. But I would consider it kind of equal, just this sort of parallel chain where your Dash can hop between the two.
[51:33] >> I see. Okay. But then, so even though it will be like a one-to-one in terms of Dash units, I can see how I might value them differently, though. For example, if I'm about to pay a
[51:46] merchant and I have $5 cash in my back pocket, and I also have $5 in my bank account, the merchant may say, well, I prefer cash, or I may say, like, we may come to value them differently, right?
[52:02] >> Yeah, I think as long as there's the mechanism where they're always instantly redeemable, I'm not talking about like the USD sort of teller sort of relationship. I'm talking about like a
[52:11] programmatic, completely equal side of things where you could trade over instantly. There is still going to be some disparity there, but it's going to be a lot closer. I think, obviously,
[52:20] if app developers can only receive credits, that's kind of what they expect. They won't want to try and receive both, because maybe there'll be a limited sort of feature set there. But realistically,
[52:31] if there is completely fluid one-to-one movement between the two, programmatically permissionless, and there is no sort of differentiation on that front, then they should be very closely sort of
[52:43] valued, realistically. >> Yeah, Amanda, that's a good analogy, because it really depends on how the developer integrations go. Like a merchant, they're not
[52:56] necessarily going to want to support accepting Dash credits, Dash tokens, whatever we want to call them on the Dash Evo side, if they're also accepting native Dash proof of work chain Dash,
[53:15] like they're not going to do both integrations necessarily. I think that for transactions, for payments, and things that are involving goods and services, you'll probably mostly see
[53:29] merchants accepting native layer one Dash. >> Yeah, I think the tooling can be created sort of around it, where if you hold Evo Dash or whatever, and you receive a normal Dash address
[53:41] or a normal transaction, then you can send your sort of Evo Dash, wherever it is, and it will automatically sort of do the conversion, pay the merchant in the sort of layer one equivalent.
[53:55] Just fully automated, fully sort of no involvement on the user's part or the merchant's part. And I think that we should aim to keep that sort of layer one Dash, the transactional Dash,
[54:05] the Evo side of things. Yes, it can be used for sort of these micro transactions for decentralized applications, but I think that's where it should be focused. I think if we try and
[54:16] get that to do everything, then that becomes problematic in terms of the security compromise, in terms of just bringing everything proof of stake and not creating that value and retaining
[54:27] that value in the proof of work chain. But exciting things for the future. I'm sure everyone has a different opinion on that one, though. It gets very complex. >> Yeah. Well, it's been a big
[54:36] old day. To answer the one question that didn't yet get answered from James, people developing on platform get paid depending on the sort of situation they're in. So someone working for
[54:51] the incubator, yes, always gets paid Dash and Dash only. I believe that someone at DCG has said they give their employees the option of whether they get paid in Dash or some other
[55:02] currency. And then, of course, a third option is people who apply to the treasury directly, like Ash referenced, the developer of the get paid Dash now or whatever those domains are.
[55:13] He's obviously getting paid Dash directly from the treasury. So it just kind of depends. So that does it for us today. And we look forward to seeing you next time. And we'll bid you adieu.
[55:26] >> All right. See you later, everybody. Thanks, Ash. >> Thanks. 