---
showLink: "https://www.youtube.com/watch?v=da3kd2MAXJo"
slug: "2nd-update-on-electrum"
title: "2nd Update on Electrum"
publishDate: "2024-02-12"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/da3kd2MAXJo/maxresdefault.webp"
---

Mikhail provides updates on recent development work on the Electrum Dash wallet, including PrivateSend mixing demo.

tl;dr: Mikhail discusses the recent updates and fixes made to the Electrum Dash wallet in January, such as upgrading the Dash P2P protocol, BLAS library, and Tor Proxy bundle. He demonstrates the now-working PrivateSend mixing feature and shares the wallet's new website designs. Mikhail also shows the monitoring dashboards for his Electrum server infrastructure. He outlines the remaining tasks, including marking InstantSend transactions, resolving log warnings, and pulling in the latest upstream Electrum changes.

00:00 - Introduction and Electrum Dash Overview
Mikhail introduces himself and provides an overview of the Electrum Dash wallet, its features, and recent development work.

02:50 - PrivateSend Mixing Updates and Demo
Mikhail discusses the fixes made to the PrivateSend mixing feature, including upgrading dependencies and libraries. He demonstrates the mixing process within the wallet.

14:35 - Electrum Dash Website Redesign
The new website designs for Electrum Dash are presented, which include download links, documentation, and frequently asked questions.

25:18 - Monitoring Dashboards for Electrum Infrastructure
Mikhail showcases the dashboards he created to monitor metrics and usage for his Electrum server infrastructure.

31:47 - Remaining Development Tasks and Wrap-up
The remaining tasks for Electrum Dash development are outlined, such as marking InstantSend transactions and resolving log warnings. Mikhail also mentions his search for additional development help.

---

[00:00] (upbeat music) In the last Why We Build segment,
[00:12] we looked at the burgeoning data storage industry, specifically at centralized options.
[00:16] We concluded by expressing concerns about censorship. Today, we're looking at decentralized data storage options,
[00:22] which, due to their very structures, are not only more censorship resistant,
[00:25] but tend to have greater reliability, redundancy, security, and be less expensive.
[00:30] This is an emerging sector, and today, we'll just skim the surface.
[00:33] Cordel seeks not just to decentralize the storage of data, but to be an entire replacement for the internet,
[00:38] replete with mesh nets. Those who download the Cordel client
[00:41] are nodes in the Cordel data network. After a user uploads content to their own node,
[00:45] if and when another user views it via a queue app, like Qtube, chunks of that content
[00:49] are stored on the other node. If a user is concerned that their data won't be accessed
[00:53] and thus won't be as durable, the pending Cordel data market
[00:56] will facilitate a marketplace between node operators who can set their own terms.
[00:59] To prevent blockchain bloat, every piece of data is hashed,
[01:02] and those hashes are put into a file with a list of hashes
[01:05] that a single hash is published on-chain. With a market cap of $2 million,
[01:08] Cordel still has a lot of room to grow. Storage, which has a market cap of $264 million,
[01:14] is a bit more centralized than other projects in this space. Storage doesn't use a blockchain,
[01:18] and prices are set by storage personnel. It costs $4 to store one terabyte for one month.
[01:23] If the data is moved using bandwidth, that's another $7 per terabyte per month.
[01:28] Uploaded data first goes through one of six persistent nodes that storage operates, called satellites.
[01:32] It is then encrypted using erasure encoding, broken into pieces,
[01:36] and pushed to storage nodes, called farmers. Farmers, who are not required to have collateral,
[01:40] can be anyone with extra space on their computers, though many use Raspberry Pis.
[01:44] Satellites also perform data audits of the farmers, what they call proof of storage.
[01:48] Today's storage claims almost 24,000 nodes with 30 petabytes of storage capacity.
[01:53] Dash, which has a market cap of $313 million, is a layer one crypto primarily aimed at payments.
[01:58] Devs now have in Testnet a sidechain called Platform, which is described as a technology stack
[02:03] for building decentralized applications on the Dash network.
[02:06] One component of that tech stack is data storage, called Drive,
[02:09] which will rely on collateralized nodes, called EvoNodes. Platform is alone among all the options we've looked at,
[02:14] decentralized or centralized, that replicates data in full on all nodes.
[02:18] Platform credits will be used when any state transition occurs,
[02:21] creation, deletion, replacement, or updates. A rough estimate is that it'll cost $10
[02:26] to store one gigabyte with no ongoing fees, though after launch, EvoNodes will be able
[02:30] to collectively vote to determine the cost to host data. SIA, which has a market cap of $487 million,
[02:37] is open source, has an API for devs, and utilizes a trustless marketplace
[02:41] so buyers, called renters, and sellers, called hosts, can transact directly.
[02:45] Currently, it costs about $3 to store one terabyte for one month with three times redundancy.
[02:50] There's also a slight fee for the initial contract formation and for bandwidth use.
[02:54] SIA uses erasure encoding to break content into segments and distribute them to hosts around the globe.
[02:59] Hosts are required to have collateral to incentivize their adherence to terms of service.
[03:03] SIA claims over a million downloads of its software and petabytes of data uploaded.
[03:07] The network recently launched a completely rewritten version of their storage rental component
[03:11] to improve user interface and horizontal scalability. A 2020 hard fork saw the creation of a foundation
[03:17] which steers the project. Arweave, backed by Andreessen Horowitz, Coinbase Ventures,
[03:21] and others, has a market cap of $551 million. Its claim to fame is forever storage
[03:26] and 100% guaranteed uptime. The price to store one gig is about five bucks.
[03:30] Arweave uses a blockchain-like structure called BlockWeave to enable scalable on-chain storage.
[03:35] A new block is added when each node validates a randomly selected old block.
[03:39] Miners, called farmers, earn R for storing and/or replicating content.
[03:43] To future-proof data, user fees go to a storage endowment that slowly drips rewards to farmers.
[03:48] Arweave is open source, can handle 5,000 transactions per second,
[03:51] has an NFT marketplace, is the home of the Internet Archive's metadata,
[03:55] and has partnerships with Visa and other big outfits. Filecoin, famous for an ICO that netted over $250 million,
[04:02] now has a market cap of $2.64 billion. It's built on IPFS as a second layer
[04:07] and claims to be the world's largest decentralized storage network,
[04:11] with over 25 exabytes of storage capacity and 2.5 exabytes of data stored.
[04:15] The network relies on proof of replication to prove specific data is held,
[04:19] and proof of spacetime to prove the timeframe the data is held.
[04:22] Stored data is broken up via eraser encoding. Miners are required to stake about one Filecoin
[04:27] for each 150 gigabytes hosted. Filecoin's blockchain doesn't store the data,
[04:31] but records transactions. In recent years, Filecoin added HyperDrive
[04:34] to facilitate faster storage loading, and Filecoin Plus to attract clients with large datasets,
[04:39] such as NASA and NOAA. Data storage demands continue to increase,
[04:43] so too do concerns about data censorship. Will centralized options soon be eclipsed
[04:48] by one or more of these better performing decentralized options?
[04:51] (upbeat music) - Kind of brings a fresh perspective
[05:01] to some things, doesn't it? - Yeah, we certainly have a lot of options, don't we?
[05:06] - Yeah, indeed. Mikhail is back for us for a second week,
[05:11] and he has gone the extra mile to fit in today's show, because once he learned that we wanted to talk
[05:20] about Electrum's updates today, with him here or without him here,
[05:24] he basically said, "Oh, heavens no. "I'm gonna be the one to give the Electrum updates."
[05:30] And we're so glad he is. We might even, I think,
[05:33] are we getting a demo today of mixing? Is that right, Mikhail?
[05:38] - Yeah, yeah, sure, sure. - Well, I'm gonna let you take it away.
[05:41] Please get started. We're pumped.
[05:43] - Okay. I have prepared some slides,
[05:47] so I will show some slides about the updates that happened during the January and yeah.
[05:55] - Great. - Shall I add it?
[06:05] - Yeah, sure. - Yeah, so there was some hard work
[06:15] during the January on the Electrum Dash. This is like a wallet which has private sensor port,
[06:23] aka CoinJoin. So what the Electrum Dash basically is
[06:28] for those who didn't know, so it's a non-custodial wallet.
[06:33] That means that you hold all your private keys, all your private keys securely stored on your computer
[06:41] and doesn't leave your computer. It is an SPV wallet that doesn't store any blocks data.
[06:47] It only downloads block headers, then verifies that your wallet has transactions in it,
[06:55] and then constructs some indexes instead of storing the whole blocks data.
[07:04] - Can I jump in real quick there on that? In your previous slide, you said it was a light wallet.
[07:12] And in this slide, you're saying it's an SPV wallet. Can you explain to people what the difference is?
[07:16] - Well. - And what it means?
[07:23] - I mean, SPV wallet is a light, like for me, it's a lightweight wallet.
[07:30] Like that was the meaning I was, that's what I mean. And it means that instead of downloading the whole chain,
[07:40] it just checks the block headers for containing transactions in it.
[07:50] - And by it, just to make sure everybody's understanding, Electrum is a two-sided wallet, right?
[07:59] There's the server side and the client side. So when you say it, what are you referring to?
[08:03] - Yes, it contains both sides. It downloads the block headers
[08:09] and also requests information from the Electrum server about transactions.
[08:16] So it's kind of combined. - Okay.
[08:21] - And then do you personally, like does the incubator or you run the server for it?
[08:27] Or does it, okay. - Yes, I'm running the server from my cloud
[08:34] and I ensure the slave, this service, like maintenance. So it's available for desktop and Android devices.
[08:47] Android devices is not yet fully working. As I know, I haven't tested it yet,
[08:52] but some guys who was testing reported that there are some issues.
[08:57] It has private send support and it's completely open source.
[09:01] The client and server side, you can check the code yourself.
[09:06] Yeah, so the most of the work that was done during the January was about the private send.
[09:15] So the issue with the private send was that Electrum wallet wasn't updated for a quite long time,
[09:22] like for two years or maybe even more. The latest protocol that was supported,
[09:28] P2P protocol was supported by the Electrum wallet was Dash Core v15, even 15, not even v18 or v17.
[09:36] It's like way back. So what I did first, I upgraded the Dash P2P protocol
[09:47] to the latest version, which is the Dash Core v12. And then I had a lot of issues
[09:58] around P2P message structures that I had to fix. I was constantly contacting DCG
[10:08] to ask some questions about how does it work, what can be not working, like what's happening.
[10:16] There are a lot of changes in the structures that was leading to the different hashes,
[10:23] for example, LLMQ hashes, and also other data that needs to be synchronized.
[10:32] I also upgraded the BLAS library to verify recent legacy and basic schemes
[10:40] used in the P2P messages. Well, one of the coin-join messages have signatures
[10:51] and you have to verify it via recent BLAS libraries, which was outdated in the Electrum.
[11:00] So there was quite long work on it because it took me, well, the first part was just,
[11:12] the issue was that repository that was decode of the repository of the Dash PBLS signatures
[11:21] didn't allow you to specify legacy scheme in your masternode private key or public key.
[11:31] So I had to change the bindings, Python bindings, but then I realized that the bindings,
[11:41] that I couldn't just import that library from the GitHub on the Windows build.
[11:48] So I had to go another way. I had to go another way.
[11:51] And then I implemented an interface for C++ library of BLAS signatures that I will invoke from the Python.
[12:04] So that was quite hard. - This is an English show.
[12:07] Would you please stop with just speaking straight Russian here, Mikhail?
[12:11] This is English. Just kidding.
[12:13] That sounds like a lot of work. Okay.
[12:15] - I can kind of attest to what you're saying because when we first got this project going,
[12:21] I was asking for people to help out and I really, really needed somebody that already knew Dash.
[12:26] And so I just wanted to mention that Bertrand, anonymous developer, I suppose, I've never seen him.
[12:34] He stepped up and did a lot of this, a lot of the preparatory work
[12:39] and mentioned that there is a lot of work to be done to get this wallet back up to date and documented.
[12:47] So he did a lot of the work and then thankfully you picked it up from there
[12:52] and did a lot of the work as well. So just wanted to mention his role
[12:56] as well as Joel helped spec some of the work that needed to be done,
[13:01] like the features that he wanted. - Yeah.
[13:04] Yeah, there are a lot of dependencies, a lot of dependencies that getting built
[13:10] like from the source code. Like when you build the binaries,
[13:16] there are a lot of libraries that you have to build from the source and then include some DLLs
[13:25] or some statically shared libraries. So stuff like that.
[13:28] Yeah. So what I also did,
[13:32] we also dropped 32 bits system supports on the windows. So I don't think that makes sense to keep it maintaining
[13:44] because there are not really much users that has such systems.
[13:51] I also upgraded Tor Proxy bundle for the windows. It was quite outdated.
[13:58] Like I put it to the last version. So the Tor Proxy bundle,
[14:03] which bundles with the windows boundaries are up to date to the Tor network.
[14:09] Yeah, I updated a lot of internal and external dependencies so that the build is working on the latest Python
[14:17] and ensure that windows and Mac binary builds are working. So we tested it with the community,
[14:26] community reports that basically it's working. There are some leftovers,
[14:32] but basically everything is working. So let me show you,
[14:37] let me show you how it's going. So when we open up the wallet,
[14:48] this is the Electrum wallet that we can see. I want to show you the private send feature
[14:56] that was broken. - Is it possible to make the window
[14:59] of the wallet bigger, Mikhail? - Yeah, sure.
[15:03] - Yeah. - And we're looking at a test net or a main net wallet.
[15:09] - This is a main net, main net. Test net is also working,
[15:12] but this one is main net. And this is what I show you.
[15:18] Yeah, so basically previously when we were starting mixing,
[15:23] it was hanging on some LLMQ quorum, so it wasn't able to synchronize.
[15:30] So when we start mixing, we just put your password.
[15:35] Also, you may want to set the amount of dash that you want to mix and the amount of rounds.
[15:43] We can see that the process just started. We can see the transactions.
[15:55] Sorry, by the date should source it. Yeah, we can see that the wallet created some denominations
[16:03] and the mixing started. There are still some errors and warnings,
[16:14] but I suppose that it relates to the instance and transactions is not fully implemented
[16:23] in the Electrum wallet. So when the collateral is created,
[16:29] it's not yet confirmed, but then when it's confirmed, the error is gone.
[16:36] - And just, I think what this term collateral is referring to is not anything to do
[16:42] with a masternode collateral, which is what most people would think,
[16:46] but it's a little small amount of dash that your wallet has to put up as collateral
[16:52] before you even can start the mixing process, right? - Yes, yes, yes.
[16:57] Before you start mixing process, there is some kind of fee, aka collateral,
[17:03] that will be charged if you do mixing in the bad way, like if you break the rules, like stuff like that.
[17:12] So it's just taken by the network as a commission. - It's normally given back, right?
[17:18] - Normally, yes. Yes, if you finish normally, yes.
[17:24] But if you, for example, quit the mixing before just suddenly quit the wallet,
[17:32] this fee, this collateral, may be charged. - But isn't there always some kind of fee for mixing,
[17:41] even if you do everything correctly and don't quit early? I guess I didn't think that mixing was totally free.
[17:48] I thought that there was always like a-- - No, it's not free, it's not free.
[17:51] So it takes some kind of fee, some commission. - Transaction fees, at the very least.
[18:01] - Yes, yes, yes. - Okay, okay, okay.
[18:04] And Mikhail, is there any, has anyone noted any, is there such a thing as a performance difference
[18:10] between mixing on QtWallet versus mixing on Electrum? Is one faster, is one slower?
[18:16] - Honestly, I haven't checked myself. But Joel reported that the timing of mixing
[18:24] is pretty the same. Like, I was asking, is it okay that mixing of the Dash
[18:30] takes like about an hour or maybe less? And he said that on Dash Core,
[18:36] that happens for the same amount of time. - Okay.
[18:41] - So we can, for example, check the denominations, that we can check those on the Explorer, for example.
[18:51] - So you just pasted in one of the transaction IDs into a normal Dash Insight Block Explorer
[19:06] so we can see the actual on-the-network transaction. - Yes, so, I don't know why it's not showing.
[19:15] Why it's showing cutters? I'll just think.
[19:23] - Oh, and you're on explorer.dash.org/insight. I've never seen that URL, personally.
[19:34] I usually use insight.dash.org, I think. - Ah, okay.
[19:39] So I manually insert the transaction into the URL. So we can see that the denominations is happening.
[19:48] Those are denominations for my mixing process. So we can check that something is confirmed.
[19:59] Yeah, so the mixing is going. So mixing is going on.
[20:07] And as the process continues, the mixing progress should increase
[20:13] and then reach to the 100%. And then you will see a message that the mixing is done.
[20:20] Then you can use PrivateSend just from the Send tab. Just checking. - Now, wait a minute.
[20:29] Wait a minute, I thought we banned the word PrivateSend. Didn't we ban that word? - We're bringing it back.
[20:35] - What? I'm just kidding.
[20:37] It looks like the user interface still uses the term PrivateSend.
[20:41] I thought that was illegal now. - Really?
[20:45] - Yeah, I didn't, well, it was also confusing for me, but yeah.
[20:52] - You don't say. When people change the names of things, it's confusing?
[20:55] Oh, okay. - Well, I didn't know what PrivateSend or CoinJoin
[21:02] is now, what we operate, which term. So I wasn't sure about that.
[21:09] So I haven't changed that yet. Yeah.
[21:13] So yeah, the process is going and then we can see that the mixing progress has increased to the six persons,
[21:22] for example. We should wait some time to reach it to the 100
[21:27] and then the mixing will be finished. - Yeah, maybe by the end of the show,
[21:30] we'll actually have some dash, will it? I guess it probably won't be done that.
[21:36] How many rounds have you selected? Let's see.
[21:39] Okay, so yeah, maybe if you just bump that down to three, does the mixing process bump up?
[21:49] I've never used this Electrum Wallet personally, so I don't know much about it.
[21:55] - I don't know. - Well, why don't you try it and see.
[21:59] - I just want to select that four and bump it down to three, for example, or does it?
[22:06] - Well, I will have to stop the mixing first. - Not in the Core Wallet.
[22:13] In the Core Wallet, you can change it on the fly and it doesn't, it just basically says,
[22:19] what that means to me is it's saying, we consider four rounds to be fully mixed.
[22:24] But if you bumped it down to three, then the coins that have three rounds
[22:30] are now considered fully mixed. And then obviously the percentage usually goes up,
[22:34] at least in the Dash Core Wallet. But I was just curious about that.
[22:37] Now, I have a separate question that somebody, I don't remember who, but somebody reported
[22:46] that they were using the wallet and they were not able to,
[22:52] it wasn't that the client wasn't working for some reason. And I think the issue was maybe DCG,
[22:59] somebody's backend server, Electrum server wasn't working. And then you picked it up
[23:05] and made your own instance of a server. And you pointed them to say, hey, change in your settings,
[23:12] what your server is pointing, or what your client's pointing to,
[23:15] what server your client's pointing to, point it to mine. And then it started working for them.
[23:20] And we had a little bit of a discussion about, can we change the wallet so that it tries
[23:26] multiple backends from X? - Yes, now, let me,
[23:31] I can change it to the two rounds and start again. - Okay.
[23:37] - Yes, yes. Actually, we found out,
[23:41] we have someone deployed some Dash Electrum server, and now I hard-coded them into the wallet.
[23:52] So now we have four production servers, one which I maintenance,
[23:57] and three from the Komodo, I believe that is Komodo servers,
[24:03] which anyone in Dash can also use. I hard-coded them into my binaries,
[24:10] so anyone, it will also distribute the load when you're loading up your wallet from the scratch.
[24:18] It will also distribute the load between the servers if you choose the select server automatically,
[24:25] which is checked by default when you-- - Okay, now, would that setting detect a server that's down
[24:33] and just move on to the next one then? - Yes, yes, yes, yes.
[24:37] - And is that a feature that you implemented, or was that pre-existing feature?
[24:43] - This is pre-existing feature. - Okay, okay.
[24:46] So maybe the binary didn't have as many servers to look for before that person was having the issue?
[24:54] That was the main issue then? There just wasn't as many ElectrumX servers running?
[24:59] - Probably. I'll have to adjust the resource limits
[25:03] on my servers as well, but right now I don't see any issues with it.
[25:08] So there is one person was asking, he has a lot of transactions, a lot of addresses,
[25:15] so I'll have to check his case if it's hitting resource limits on my server.
[25:20] But I checked last week's, everything was fine, like no disconnections and stuff like that.
[25:28] No errors, I mean. So let's get back to the slides.
[25:34] I want to show you some other things going on. So what we did, we just designed a new website,
[25:45] Electrum-website, that we want to recover. So what I did, me and my colleague Alexei
[25:56] thought up about the design. We took Electrum.org website as a reference,
[26:05] and we already made the design in the Figma. We bootstrapped an initial code, initial repository.
[26:13] The pages are now blank in the front end, but we soon will start working on it.
[26:22] I also ordered a few domains where I will deploy my website.
[26:28] So the way that I registered to myself is Electrum-dot-com, dash Electrum-dot-com,
[26:35] and dash Electrum-dot-org. There's also Electrum-dot-org,
[26:41] which is still taken by the previous team. So I'm not sure about that.
[26:47] - Electrum-dot-org, is that the original one that's still maintained, or not maintained?
[26:55] - Yeah, yeah, I checked the registration of the domain. It was updated in the last November or December.
[27:06] So we will have to wait at least November, December of 2024.
[27:13] So I don't know whether we will be able to take over it. So at least we have another one,
[27:22] and they will be indexed, hopefully, in the Google. So when we search Electrum Dash,
[27:28] I hope that they will pop in the search results. - Now, a question related to that is,
[27:35] what are the chances, desires, yeah, of getting a link to Dash Electrum from Dash-dot-org?
[27:45] - Is there not one? - I don't know.
[27:50] I will check right now. - Sorry?
[27:54] - I'm just wondering if we can link to Electrum from Dash-dot-org, where all of the other
[28:01] Dash wallets are listed. Have you looked into that, or?
[28:06] - I'm checking it right now. On desktop, they have Dash Core, Exodus,
[28:10] Coinomi, Guarda, and Atomic. So no, it is not there.
[28:13] - It's not there yet, but I think we can update the link. We have to talk with DCG.
[28:20] Actually, last time I spoke with them, they raised some concerns about the code base,
[28:28] that it wasn't updated for a long time. But since we recovered everything,
[28:32] that I checked the dependencies and stuff like that, I think we can talk about that
[28:37] if everything is working with the wallet. I think there's no issues to add them to the website.
[28:42] - Yeah, I mean, if you look at the website, there's a, it's a two-column,
[28:48] you know, three-column, two-row grid. There's one blank spot just waiting for it.
[28:54] - Yeah, yeah, good idea, good idea. Also, we should include them in the documentation
[29:02] in the documentation right now. There is a message like Electrum Dash
[29:05] is not maintained and supported. So I think we also may want to include them
[29:11] in the documentation, the links. - Yeah, we'll look into that.
[29:16] - Yeah, sure. - Or you'll look into that.
[29:18] You're the best person for that, I think. - So I want to share with you some designs of the website.
[29:23] So basically, this is four-page website that will show the info about Electrum Dash wallet.
[29:31] It will show the downloads, the signatures that will be signed by me
[29:35] or any other maintainer that will be doing that project. Some downloads where you can download the recent builds,
[29:48] the current, which means that, which is actively developed and the latest stable build.
[29:54] Some info about previous releases, change logs. Some servers, this is just the demo servers,
[30:05] like, you know, just a list, just a sample list. Those are not really active,
[30:10] but it's just a sample for design. And the about page where you can see the info
[30:20] about the wallet and the frequently asked questions about how Dash, Electrum works, Electrum Dash,
[30:27] and some info about the maintainer. For example, for me.
[30:32] Yeah. So, yeah, stuff like that.
[30:38] So we plan to work on the front end in February. So hopefully we will see the website pretty soon.
[30:52] - And what about the mobile wallet? Can you say anything about that?
[30:57] - Yeah, so-- - Is there a mobile Electrum?
[31:01] Is that what y'all are saying? - Yes, there is a Android case,
[31:06] which is not yet fully working, but there is a plan for it.
[31:16] - Okay, so just like a question about how it's architected. My understanding then is you have,
[31:27] there's a mobile client that's an Android app only, not an iOS app, right?
[31:34] And from what I understood, you could use the mobile wallet client to do mixing,
[31:42] which I'm guessing is basically doing the same thing that the desktop client does.
[31:51] It's requesting that the server start a mixing session. Is that how it works or?
[31:56] And then the client just signs transactions as needed? - No, the servers are needed to request some info
[32:05] about transactions, about headers, about the network, but the CoinJoin is working through the P2P messages.
[32:14] So it connects straight to the masternodes network. So it sends the messages straight to the masternodes.
[32:23] So it doesn't require a server to make a CoinJoin. - Is that like similar to the implementation that,
[32:33] oh, I actually, I wish I had never even said this. I hate talking about things that don't actually exist
[32:39] because it sets expectations that so often don't get met. But since I said it,
[32:44] do I have heard that mixing is being added to the dash, like the DCG mobile wallet, if that's true?
[32:53] Are we talking about the same kinds of implementations here? - Well, implementations is more like,
[33:00] it's more like a dashboard wallet than the mobile wallet. I think mobile wallet was slightly changed
[33:08] the way it works because as I know from hash engineering that they are now synchronizing content list block headers
[33:18] while Electrum Dash are synchronizing everything from the get go.
[33:23] - Okay. - So yeah.
[33:31] And another thing that I want to share with you is the dashboards aka monitoring that I plan to do
[33:38] for all of my services that deployed into my cloud. So right now I have some dashboards on Electrum Max,
[33:48] the server of the Electrum on the main net and test net. And it collects usage metrics and blockades
[33:57] like where we are now and is it alive or not? Let me show you.
[34:03] So it's hosted on dashboards.treadmix.dev. So when you open it up,
[34:16] you will redirect it to the dash Electrum Dashboard, Electrum X Dashboard, sorry.
[34:24] And we can see some info. Like about session counts, about the request rates,
[34:33] about request total transactions that was sent through this Electrum server.
[34:37] Some height is the height differs from the inside API. So yeah, stuff like that.
[34:47] And we can change the time ranges. For example, in the last three hours
[34:53] we sent four transactions. I believe that's from my wallet.
[35:00] Yeah. - Is that how many transactions have been routed
[35:05] through your backend Electrum X server or? - Yes, yes, it's linked to the my Electrum X server
[35:15] which is dash Electrum.treadmix.dev. - Okay, so that would, yeah, that would not include
[35:22] transactions that were routed through different servers. - Yes, yes, yes.
[35:26] It's basically monitoring and dashboards for my infrastructure for my servers.
[35:33] I plan also to add dashboards from other services like Platform Explorer for any pay or any other services
[35:42] that I will be deploying on my own. If we go to the dashboards,
[35:47] we can also see the testnet server, it's also up. And yeah, we can choose the time ranges
[35:57] and stuff like that. So basically it shows the load and some usage metrics.
[36:08] - Okay. - Yeah, so what's left or what's left
[36:15] in the Electrum Dash wallet and what I want to implement? So the first thing that really bothering me
[36:26] is InstantSend transactions that is not marked. As InstantSend is confirmed,
[36:31] so when you receive the transaction, it shows you like zero confirmations,
[36:36] like you have to wait like six, but obviously they all, like 99% transaction
[36:43] getting an InstantSend, so you can use your dash received just straight away.
[36:51] It also, those warnings that, those errors that was showing in the logs
[36:59] of the private send mixing, I think that also relates to this piece of thing.
[37:06] Yeah, I think that won't take much long. I think we should just make sure
[37:16] all the libraries and dependencies I included that I was upgrading in the correct way.
[37:22] So I don't think that that will take much time. I want to also test Linux app image binaries.
[37:29] I don't have any Linux system. If anyone from community can jump on it
[37:36] and test the binaries of the Linux, it would be really, I would really appreciate it.
[37:44] It would be cool. - I guess there's not many people that would,
[37:51] like what's the benefit of running a Linux Electrum wallet because most, I mean, why I'm asking is
[38:01] most people who are running Electrum, it seems to be that they're trying to avoid
[38:08] the full download of the blockchain, but if you're running a Linux server,
[38:13] then you usually have-- - I mean, it's not, sorry, I mean the desktop,
[38:20] desktop like Ubuntu or any other desktop system. I haven't checked the app image binaries,
[38:26] but they should be working, but I haven't checked it myself.
[38:30] - Okay, so Linux desktop. - Yes, yes, Linux desktop, I mean.
[38:34] Also, I want to pull in the fresh Electrum code base. There was a lot of changes in the Bitcoin Electrum.
[38:46] So we would like to pull everything in our code base. - That sounds like a lot of work.
[38:55] - Yeah, yeah, but I think it's pretty doable. I already have some vision on it.
[39:00] How can we, how we can jump on it? How can we implement it?
[39:04] How can we do that? So that quite work, but not that,
[39:11] not that like, like we will do it. Also resolve all private send log warnings.
[39:24] That doesn't affect mixing right now. That was the errors that I was showing you in the first time
[39:31] and roll out a new Electrum Dash website. So that's the things I wanted, want this to happen.
[39:39] - Are you looking for help with this stuff or are you wanting to do most of this yourself?
[39:47] Do you already have somebody that's working with you on this?
[39:50] - Yeah, I'm looking for someone who knows Python, who can jump onto the code base.
[39:57] I already had one guy interested in it, but he haven't checked it out yet.
[40:04] So I'm looking for a guy who can help me with that, who will implement some things and I will review his code,
[40:14] but haven't found anyone yet. - And is the work to be done mostly on Electrum X
[40:23] or is it on the Electrum client? - Mostly on the Electrum client.
[40:27] Like the server is so stable. It never crashes, it runs very, very stable
[40:32] and it supports everything that we need. So almost the work that needs to be done
[40:39] is on the client side. - Is the server side, does it require a connection
[40:46] to Dash Core or is it an alternate implementation of Dash? I'm guessing it's the former, it requires Dash Core
[40:55] because I don't think we have an alternate implementation. - Yes, yes, it connects to the Dash Core instance.
[41:01] - Okay, hence why it would be more stable because it's basically just a lightweight wrapper
[41:07] that connects to a real up-to-date full node. - Yeah, it does have some indexes.
[41:14] It does indexes some stuff, but yeah, it requests some data from the Dash Core.
[41:21] - And when you say it requests data from Dash Core, is it a random node it's querying?
[41:27] Is it always the same node, like a known trusted node or which one?
[41:31] - Yes, it's a trusted node run by me. - Oh, okay, okay.
[41:36] And do you have download stats on the client? I've wondered this for a long time, actually,
[41:44] just how many people, if any, are using Electrum? - Well, I don't have download stats,
[41:51] but I have some stats on session counts, so average sessions during the day,
[41:58] like three, five users per day. That's what I seen on my dashboards.
[42:05] - And when you say sessions, is that mixing sessions? - No, no, that's just not the mixing sessions,
[42:12] that's the users of the wallet who open the wallet and connect it to the--
[42:15] - Oh, right, because your server gets pinged every time they open it.
[42:18] Okay, yeah, yeah. - But that's just your backend.
[42:22] - Yes. - So there might be many more that are using,
[42:26] I can't remember who you said was running those servers. I remember it being one of Agni's friends.
[42:32] - Yeah, I can't collect the load counts metric right now because downloads are happening from the GitHub,
[42:41] but once we get the website, I think we can do it. - Okay.
[42:47] Is yours the default backend server to connect for clients, or is there a default?
[42:56] - I think default is my server, yeah, because it's listed as the first thing in the list.
[43:06] - Okay. Okay, so any questions?
[43:10] - Well, I've asked plenty of questions. I'm not sure if we have any questions
[43:16] from anyone else right now, but Amanda, do you have any more questions?
[43:22] - There's some stuff in Russian, I don't know what it says, but no,
[43:26] I think I've asked my questions as well, yeah. - Okay.
[43:31] - Okay, good. Well, thanks for those demos, Mikhail,
[43:37] and yeah, next week we are booked, and I forget now who it is.
[43:48] I wanted to give you a little teaser, but maybe this is extra mysterious.
[43:51] - Is it the merchant tooling, not tooling, but the independent merchant creation,
[44:01] merchant credits, is that who we have on board, or was it something else?
[44:06] - The 17th of, if next Monday is the 17th, then that is probably, yes.
[44:13] I'm sorry, is it the 19th? Yes, okay, yes, we will.
[44:17] Thank you, Rion. Yes, next week we are going to have our first update
[44:22] since the initial announcement about the merchant credit system, if you'll recall.
[44:28] That was Jan, long time Dash lurker, who finally found some free time in his busy schedule
[44:37] and brought a brand new concept. First pitched it actually at the Utah Dash Retreat,
[44:42] and then brought it as a concept to the incubator, and he has, like Mikhail here,
[44:47] he has been hard at work on his stuff and has stuff to show, stuff to talk about,
[44:53] so we look forward to chatting with Jan this coming Monday. So without any further comments,
[45:00] that's when we'll see y'all next. - Okay, thanks everyone, thanks, Mikhail.
[45:04] - Yeah, thanks, bye. - You're right.