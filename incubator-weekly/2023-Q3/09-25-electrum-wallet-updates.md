---
showLink: "https://www.youtube.com/watch?v=TkTgWMwkzjo"
slug: "electrum-wallet-updates"
title: "Updates on Electrum Wallet & Other Projects"
publishDate: "2023-09-25"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/TkTgWMwkzjo/maxresdefault.webp"
---

Dash cryptocurrency updates: CBDCs, Electrum wallet, Platform Explorer, AnyPay, and Dash Mate.

## Episode Summary

tl;dr: Mikhail provides updates on several Dash projects, including the Dash Electrum wallet's compatibility with mainnet v19, the Platform Explorer's new indexer model for improved transaction decoding and data querying, AnyPay's addition of new payment options and interface improvements, and Dash Mate's updates for v25 testnet compatibility and SSL certificate renewal fixes.

## Chapters

00:00 - CBDCs and Cryptocurrency Legislation
The episode begins with a discussion on recent legislation and efforts to prohibit or restrict CBDCs in favor of cryptocurrencies.

04:50 - Introduction and Overview of Projects
Mikhail is introduced and provides an overview of the Dash projects he will be discussing, including Electrum, Platform Explorer, AnyPay, and Dash Mate.

06:13 - Dash Electrum Wallet Updates
Mikhail discusses the current state of the Dash Electrum wallet, its compatibility with mainnet v19, and some remaining issues with private send functionality and testnet support.

16:44 - Platform Explorer Updates
The Platform Explorer has been updated with a new Rust-based indexer model for improved transaction decoding and data querying using PostgreSQL, with plans to migrate the API and frontend to utilize this new system.

28:49 - AnyPay Updates
AnyPay has received updates to its payment interface for better mobile responsiveness and the addition of new payment options like USDT and USDC via the Brave Wallet.

34:37 - Dash Mate Updates
Dash Mate, a tool for easily setting up masternodes and local development environments, has been updated for v25 testnet compatibility, with fixes for SSL certificate renewal and Docker Compose plugin compatibility.

## Transcript

[00:00] (upbeat music) Earlier this year, Ron DeSantos made news
[00:05] when he signed legislation to prohibit CBDCs in Florida. But what exactly did this legislation say?
[00:11] What would prevent CBDC functionality under another name? What DeSantos and his colleagues did
[00:16] was to modify the definition of money within the Uniform Commercial Code, or UCC.
[00:20] In 2022, the group that seeks to standardize the UCC across states, the Uniform Law Commission, or ULC,
[00:27] updated some of their language, including the definition of money.
[00:30] Some, like DeSantos, saw the new definition as favoring CBDCs at the expense of cryptocurrency.
[00:36] But the ULC responded and claimed that their new definition did not favor CBDCs
[00:40] over cryptocurrency, and further, that the issue of cryptocurrency is the exclusive authority
[00:45] of the federal government, so attempts to stymie it need occur in that realm.
[00:49] And that's just what Tom Emmer is attempting. For three consecutive years, he's introduced a bill
[00:53] to prohibit CBDCs on the nation-state level, specifically to prevent the Federal Reserve
[00:58] from transforming into a retail bank with access to personal financial data.
[01:02] And this time, his bill has 62 co-sponsors and the support of a number of industry groups.
[01:08] On this issue, Emmer stated, "If not open, permissionless, and private like cash,
[01:12] a CBDC is nothing more than a CCP-style surveillance tool that can be weaponized to oppress the American way of life."
[01:19] This sentiment was echoed by Edward Snowden, who called CBDCs a perversion of cryptocurrency
[01:24] and likened them to a crypto-fascist currency. Last Wednesday, September 20th,
[01:29] Emmer's bill passed the House Financial Services Committee. He called it a "historic step in defending against
[01:34] an ever-expanding government surveillance state." Next, it'll go to the full House for a vote,
[01:38] and there's a companion bill in the Senate, sponsored by Ted Cruz.
[01:42] We'll see what unfolds. Even if the bill's passed the House and the Senate,
[01:45] would Biden sign it? After all, it was Biden who last year
[01:48] signed an executive order that mandated continued exploration into CBDCs,
[01:52] including the supportive efforts undertaken by those at the Federal Reserve.
[01:56] Perhaps this is why Alex Mooney introduced a bill in May that sought to prevent the Federal Reserve
[02:01] from even researching and testing a pilot version of a CBDC. But back to Biden's executive order
[02:06] to point out the stated "commitment to multi-country experimentation,"
[02:10] something that is at the core of what the Bank for International Settlements, or BIS,
[02:14] has been pushing. They know pushback to CBDCs would be greater
[02:17] if their centralizing agenda was front and center. Thus, their emphasis not on one global CBDC,
[02:23] but a CBDC for each nation-state, using each nation-state's own currency.
[02:28] These would then be synced behind the scenes. All of this is laid out
[02:31] in the latest BIS report on the subject. And surprise, surprise, among the entities who helped craft it
[02:36] was the Federal Reserve's own Board of Governors. Inside were all the expected phrases,
[02:41] such as interoperability, tokenized assets, and programmable payments.
[02:46] Further, the report highlights the need not to omit legislative actors
[02:49] with the aim of garnering more public trust, and thus achieve legal tender status.
[02:54] Indeed, this seems to be a critical point, as they write, "The central banks in this group recognize
[02:58] "that no meaningful retail CBDC could be issued "without the support of respective governments."
[03:04] So, will the timely actions of Eamer and his colleagues triumph?
[03:07] Or will the BIS and Biden and their comrades have their way? A poll conducted by the Cato Institute
[03:12] provides food for thought. The bulk of respondents were opposed to the idea of CBDCs
[03:16] when they're framed as a tool that would give the government the ability to monitor
[03:20] or prohibit their transactions. It's interesting, though, that this figure drops off
[03:24] when the people in question are reframed as political protesters.
[03:27] Then respondents, apparently believing that they themselves can never be labeled as such,
[03:32] aren't nearly as concerned. The Cato survey found that the segment
[03:35] most likely to use a CBDC, and also the least likely to oppose one,
[03:39] are the youngest demographic. And while that's a bit sad to see, is it surprising?
[03:44] I mean, they have spent almost their entire lives in institutions that preach
[03:48] that government and centralization is the answer. And this question, about attributes thought beneficial,
[03:54] should be of interest to those of us in the cryptocurrency space.
[03:57] Though more respondents chose none of these, the options that did net the most affinity
[04:01] were inexpensive transaction fees, privacy, security, intuitive interface, and instant settlement.
[04:07] Of all those, the intuitiveness seems to be the one we can most improve upon.
[04:11] With this data in mind, and with an aim to not give too much importance
[04:15] to political maneuverings, what can we do? We can position cryptocurrency as an option,
[04:19] a better option. As mentioned before, we very likely need
[04:22] to make it more intuitive and appealing to the user, and not just compare and tout and promote our network
[04:27] against other crypto networks, but juxtaposition our network
[04:31] against what the legacy banksters are pushing. Clearly, no one likes the idea
[04:35] of their transactions being disallowed. In stark contrast to centralized, programmable CBDCs,
[04:40] which would empower technocrats with this ability, it is not a function of decentralized,
[04:45] open, uncensorable cryptocurrencies. This, then, is a feature of our product.
[04:50] There's a fork in the road ahead. Now is the time to create.
[04:54] What other ideas do you have? (upbeat music)
[04:58] - Dang, I liked that pretty graphic at the end. I guess I'll ask Pete later if you wanna chime in now, Pete.
[05:11] Was that a new one from Jaloise? Does anyone know?
[05:13] That was pretty, that's all I can say. - I hadn't seen it.
[05:17] - Yeah, that was nice. Well, hi, Rion, and hi, Mikhail.
[05:21] These are two faces we know well, of course. And Mikhail is here today to give us updates
[05:28] on several projects, actually, so many, in fact, that I think we ought to just jump right in.
[05:33] And are we starting with, you know what? I'll just let you talk, Mikhail.
[05:39] - Hey, everyone. What's up, deaf people?
[05:43] Yeah, I wanted to tell you about the work that was going, that I was doing last month, I think.
[05:56] Like, all this work was done during the September. There are several projects that I wanted
[06:05] to share updates here with. And yeah, I wanted to just cover
[06:13] how the thing is going in some projects. So the first one is the Dash Electrum.
[06:21] A lot of people was, a lot of people is asking, like, what's the state of the Dash Electrum?
[06:28] Some people just can't find the link to the downloads in that.
[06:35] And I checked the whole project, and this is what I have found.
[06:44] Well, the basic operations is working in the Dash Electrum. And thanks to the Bertrand256,
[06:52] he made it work to be compatible. So it's now compatible with our mainnet and v19.
[07:03] But there are still some things. So the basic functionality of Dash Electrum
[07:10] is currently working, and yeah. So what I found out-
[07:17] - That's just the client side, right? - Yes.
[07:23] - You might cover this in your future bullets, but I think that a lot of people don't really realize
[07:29] that Electrum is basically split into two projects. There's the client, and then there's the server.
[07:34] And as far as I know, DCG is the only one that's running Electrum servers.
[07:40] - I did not know that it was- - The client and server side
[07:47] currently updated to the v19, which is what mainnet is currently running.
[07:52] But not for the v12 yet. So in the testnet, Electrum client is actually able
[08:00] to run on the v12 version, but the server- - 12, are you saying, or 20?
[08:09] - I mean, Electrum server is not running in our testnet yet. So it just, v12 hard fork have some extra fields
[08:20] in the coinbase in some, it also adds some asset log transaction view
[08:27] that is not yet put up in the Electrum server. So the mainnet Electrum dash is actually
[08:38] the basic functionality is working. So Electrum client is working,
[08:43] and the Electrum server is working. Yeah, but not about the testnet.
[08:50] So- - And then there's also Electrum mobile,
[08:53] which a lot of people might hear about people coming in and saying,
[09:00] "Hey, what's wrong with Electrum?" Or, "The features of Electrum aren't working."
[09:05] I'm a little confused about what they're talking about. I'm not an Electrum user myself,
[09:10] so I don't know all the features that may or may not be available or are working.
[09:15] But what's the state of Electrum mobile and mixing specifically?
[09:20] - To be honest, I haven't checked the Electrum mobile yet. I know that Bertrand also provided binaries
[09:31] for the Electrum mobile in the GitHub. So I guess it's there in the Electrum client repository.
[09:39] I just need to check it carefully. - Okay.
[09:43] - I also saw that the transactions that you're receiving with Electrum dash
[09:53] is not marked as instant send. So it just was confusing for me
[09:59] because I was sending the funds from the Dash Core wallet. It was into the Dash Electrum,
[10:05] like I was able to get it into the Electrum, but it was just marked as unconfirmed.
[10:12] That was just confusing me. And private send is broken right now, even in mainnet,
[10:19] because there was some changes in the quorums of the Dash Core and I think this is not updated yet.
[10:28] The basic functionality is working, but not the private send.
[10:33] Private send is failing to the error about LLMQ quorums. - Did you say even in the core wallet?
[10:41] - No, no, I said that, I mean-- - So mixing doesn't work in Electrum
[10:51] because of one of the more recent updates in core, right? - Yeah, private send is not working in the Electrum
[11:01] right now in the mainnet, because the Dash Core have some updates in the quorums
[11:09] and Electrum is not updated for these changes yet. So I think it wasn't working in the V19.
[11:20] Perhaps it was working in the V18, but in the V19, something changed.
[11:26] - Do you know if that is on the Electrum client side or on the Electrum server side?
[11:31] - Not yet, not yet. - I'm just concerned that a feature that's a network feature
[11:45] wouldn't be working for one of the clients. And if that's the server side, then that's one thing.
[11:53] If it's the client side, it's another thing. But I guess we'll look into that more.
[11:58] - Yeah, yeah, we will figure out. So I saw the message on the Electrum client,
[12:04] not sure where the actual issue is. So the goal--
[12:11] - Just so everybody knows, you haven't, you picked this project up more or less pretty recently.
[12:17] Like, I've been relying on Bertrand to do most of the Electrum stuff
[12:23] because he's very familiar with Dash and everything. And several people, including Joelle,
[12:28] were really wanting me to push this forward and prioritize this in the incubator.
[12:34] And I'd said several times that unless there's somebody that's already familiar with Dash and can code in Python
[12:44] and all these criteria, I wasn't really too interested in doing much more on Electrum
[12:49] unless we had that kind of person. And you stepped up recently to kind of take over
[12:55] because Bertrand's busy on his stuff. And you said that you're willing to do this recently, so.
[13:01] - Yes, exactly, exactly. So yeah, so my goal here is just to establish
[13:08] development workflow to keep the application up to date. And also, when a feature is requested from the community
[13:17] or anyone else, well, I will be able to make it. Any more questions about the Dash Electrum projects?
[13:30] - I have a question. I, too, like Rion has said, I'm a non-user.
[13:39] I think I downloaded Dash Electrum once, five years ago, and I don't know.
[13:44] I guess I didn't stick with it, obviously. But why, in your opinion, Mikhail or Rion,
[13:49] would someone use Dash Electrum? What is the value here?
[13:53] - Well, Dash Electrum is an SQV wallet, so it doesn't require you to download the whole chain.
[14:00] So it's the same as mobile. It's just easy.
[14:07] It's easy to install. It's easy to use.
[14:10] You just put in your words, your seed phrase, and here you go.
[14:15] It also-- - That was before Core started supporting HD wallets,
[14:23] is that it was an HD wallet, where Core wasn't until somewhat recently.
[14:30] Correct me if I'm wrong, but can you, if somebody really wanted to use Core,
[14:37] but didn't want to store 50 gigs or whatever, maybe even higher, I think it's probably closer
[14:44] to 70 or 80 gigs when you-- - The Dash blockchain?
[14:47] - Indexes for the Dash blockchain. You can prune a Core node, as well,
[14:54] and so what's the difference, then, between a pruned Core node and an SPV wallet
[15:01] in terms of, like, weight? - Well, you will still need to store some amount of blocks,
[15:10] and as I remember, there is a minimum, like, there is a minimum amount of blocks
[15:18] that you need to store in the pruned node, first, and second--
[15:23] - I think you have to download the whole thing, and then you can prune it, right?
[15:27] So it's kind of a cost that you have to bear, regardless of how much you want to keep it.
[15:34] - You have to get over each single block, you have to sync up with the whole chain,
[15:41] while with Electrum, you just, we're just looking in the headers,
[15:46] and the sync up is, like, you know, it's fast, and you just download the Electrum,
[15:53] and you can use it straight right away. - And then, so you all had said
[15:59] that there is a mobile version of Electrum, and that if it were working,
[16:04] that there would also be CoinJoinMixing/PrivateSendMixing on Electrum, so does that mean
[16:10] that if the whole thing were working, there could be mixing on mobile,
[16:13] and there just isn't right now? - I hope so.
[16:18] - Yes, yes, yes, and that's why I think a lot of people are kind of upset
[16:24] that Electrum has been languishing in without development. That's my understanding.
[16:33] - Okay, all right, well, let's keep rocking and rolling. - Yeah, yeah, let's step over to the next project.
[16:44] The next project is Platform Explorer that we're doing together with Ash,
[16:49] and she's a strategist on this project, and I will take care of the backend updates,
[17:01] because there was a lot of stuff going on under the hood. - Just a little bit of a note for context before you,
[17:12] 'cause you brought it up. We should have actually brought this up at the beginning,
[17:16] but you, Mikhail, are going to be submitting a proposal this quarter,
[17:22] and that means probably this week. Actually, we were planning on submitting them
[17:30] before the last quarter ended so that we could start getting some voting in,
[17:35] but with the heavy decision proposal, I thought it would probably be best
[17:42] to not throw incubator proposals into the mix so that people could focus on that question,
[17:50] which I'm very happy actually did pass the 60-2020 reallocation proposal.
[17:58] But so you are going to be submitting an incubator strategist proposal,
[18:03] like I said, probably this week, and so you can expect people,
[18:09] you can expect four incubator strategist proposals this quarter, and we will,
[18:15] this time, we will definitely be taking into account DCG's budget constraints as well as our own,
[18:27] and we'll go from there, but this quarter hopefully should be the only quarter
[18:34] that we really have very, very tight budget constraints because hopefully Evo-Evolution will be on main net
[18:45] by the end of this year, and then by Q1 of 2024, we'll have an increased budget.
[18:52] So that's kind of a broad schedule for our timeline and our proposal submissions.
[18:59] - Okay. - So go ahead and continue with these projects then,
[19:03] if you're interested in these projects, Electrum and the ones that Mikhail's gonna talk about
[19:08] after this, then you'll want to vote for his proposal. - Yeah, yeah, for sure.
[19:18] Okay, so what was done, in the Platform Explorer?
[19:28] There was, so the major change is that I have added a new model in the application,
[19:36] in the backend, so it's called a chain indexer, simply indexer.
[19:42] So this is a Rust-based web service. It decodes and writes data in some storage,
[19:54] in our case it's Podger SQL. So basically, what does it do?
[20:00] It fetches the data from the tender dash, from the blockchain, from the platform chain,
[20:09] and it decodes each transaction. Each transaction that it decodes,
[20:13] it goes to the handler, and it inserts every information into SQL.
[20:24] Yeah, so later this data could be acquired via API on our frontend.
[20:33] We had to move this way because the tender dash have only info about the transaction,
[20:43] like it only have encoded transactions in the chain. It doesn't have any platform entities like identities,
[20:51] like the documents, data contracts, and so on. To be able to search this data on the Platform Explorer,
[20:59] we need to check it, to parse it. And for this, we need to have indexer model
[21:08] that allows us to fetch all the transactions, to read all the transactions,
[21:14] and construct an index in the SQL that we can use from our Platform Explorer frontend.
[21:23] - So for those of us, for anybody wondering, okay, I just saw an API and an indexer
[21:32] going to platform chain. Whatever happened to DAPI?
[21:37] So how did the decentralized API get lost in this, or where does it compare?
[21:44] How does this compare to quote-unquote DAPI? And maybe you could back up on your statement this time.
[21:50] - Well, DAPI, yes. Well, DAPI is more for the clients.
[21:54] Like, it's for the, like, it's for decentralized applications
[22:00] where you need to check proofs. When you just have a Platform Explorer
[22:04] where you trust the Platform Explorer, where you can check the data,
[22:10] you can compare this data with other sources, you can compare the data that you have
[22:15] on the Platform Explorer with your local client, with your local full node, for example.
[22:22] And Platform Explorer will allow you to source the data, to explore the chain,
[22:29] because even if you have client, local client, local DAPI client instance to make requests,
[22:37] you still need to read the data. Like, Platform Explorer just gives you
[22:45] an user interface to do that. Like, you just need to, don't need to download anything,
[22:52] you just open up the website. - Okay, so this is not just to Insight,
[23:01] but for the Platform Explorer. - Yes, yes, exactly, exactly.
[23:04] It's like Insight, like whatever we have, like blockchain.com, like we have for Bitcoin,
[23:11] I don't know, many else explorers that we used to see.
[23:16] Yeah, and I decided to go Rust because the platform protocol was recently rewritten in Rust.
[23:27] And I first checked with the Node.js, like I was doing the decoding of the transactions
[23:37] like we have right now on the website. It's decoding on the server via JS.
[23:42] But JS code goes for the Wasm transition to the Rust code, like.
[23:52] And I just thought that like, I saw some performance decrease,
[23:59] that the performance was decreased. And I checked it with the Rust.
[24:06] I just sampled an application that decodes the same Base64 string.
[24:12] Yeah, and it worked really, really, really faster. So in my case, on my laptop,
[24:21] the parsing of the blockchain like gained literally really, really good performance
[24:29] because we like omitting the Wasm layer, the JS layer.
[24:33] JS layer also have some verifications that checks the storage of the data contracts
[24:39] and some other stuff that we can just simply disable in the Rust.
[24:42] Because we are searching through the trusted source, like the tender-rpc that you have locally.
[24:51] So yeah. So what I made is I just created an application
[25:04] and implemented only first state transition, which is data contracts.
[25:11] And I'm going to implement other state transitions. So currently, what's working currently?
[25:25] I was able to get it syncing up to the chain tip, like it continuously syncing up to the latest block.
[25:34] It decodes every single block that is coming from the network.
[25:38] It also stores the basic units like blocks, state transitions that is needed for the processor
[25:47] because, well, not only for the processor, but it also helps email.
[25:57] It's like, without that, I would need to query tender-rpc directly,
[26:06] but on the front end, on the API side, we don't really want to do that.
[26:12] And I decided to move everything into the storage, into the PostgreSQL.
[26:17] So we can do queries, you know, a lot of queries, like fast queries, like, you know, limits.
[26:29] We can do joins and with this data, like, and yeah. So the first data contract create handler was implemented.
[26:41] I will do the rest. I will do the rest soon.
[26:44] So what I'm going to do now is I'm going to, well, this one is in the process already.
[26:55] I'm going to migrate all the API layer and front end layer to the PostgreSQL call.
[27:02] I will also need to make sure that all the fields that I was using with tender-rpc
[27:10] is also available in the Postgres. So basically after that,
[27:19] I will move everything to the Postgres on the API and front end.
[27:23] We will be able to search data contracts. So data contracts is already in the database.
[27:29] So after that, we will be able this thing to be searchable and index it on the website.
[27:38] Yeah, I'm going to implement the rest of the state transition as well.
[27:45] And after I will finish with the rest of the state transitions,
[27:49] I will be able to expand all available data on the front end.
[27:52] What does it mean? Is that we'll be able to search documents.
[27:56] We will be able to search the data contracts, identities. We will be able to see identity balances.
[28:03] We will be able to see what was happening, what transactions was happening on the given identity.
[28:12] We will be able to link all these data in different places on the front end.
[28:21] - Okay. - Yeah.
[28:25] Yeah. So any questions?
[28:29] - Nope. So we had Electrum.
[28:36] That's one that you're working on. We just did Platform Explorer.
[28:40] How many other projects are you going to feature today? - There are two more.
[28:47] - Two more, okay. Let's move right into them then.
[28:49] - Okay. So the third one is the AnyPay.
[28:55] Well, if someone doesn't remember, doesn't know, this is like a payment processor, non-custodial,
[29:07] that you can use to make payments straight on your wallet. So it works like you download an application
[29:15] from the App Store and then you can like build someone. It works like a mobile terminal.
[29:24] The user, the client will be able to scan the QR code or pay it with any favorite crypto.
[29:33] So what was done first is that the payment interface wasn't scrollable.
[29:43] So we just made it mobile responsive on the, well, on the website when you are going to pay
[29:52] with your crypto. This one was very fast and easy to fix,
[29:58] but it was very, very important because when you open up it in the mobile,
[30:05] you can't just, you couldn't just even invade because you can't scroll to all of your payment options.
[30:12] - Can I just ask, this wording about Web3, I don't remember that being on AnyPay before.
[30:18] Is that a new addition and is that your addition, Mikhail? - Yes, I was working on this feature this summer.
[30:27] We have added a few tokens like USDT, USDC on three, ah, yeah, it was USDT and UDC on three chains.
[30:36] So six chains was six tokens was added. So it's now allow you to pay with your Brave Wallet,
[30:46] with your favorite crypto. Well, not favorite, but USDT and USDC.
[30:51] - With the which wallet, sorry. It allows you to pay with which wallet?
[30:56] - Brave Wallet, Brave Wallet. - Got it, thank you.
[31:00] - So this was a major feature that we were doing. So that I was doing, actually I was doing it
[31:16] with my colleague. So what we did is that we reworked the interface
[31:25] because it was like reloaded. Some of the payment options wasn't really working.
[31:34] Like it wasn't working at all. And we carefully checked everything out
[31:39] and we refactored the code to make it more clear for the user, because when you open up the link,
[31:55] it was just giving you all of the available options. And now you can just choose whatever option you want to pay.
[32:03] And then you will have some few options that you can pay with.
[32:09] This one was not just about redoing, reworking the interface.
[32:17] It was also important for, sorry. It was also important to check the code,
[32:25] to get into the code of this interface because it was pretty long, like not developed.
[32:34] And yeah, we had to check all the things that working or not working with these projects.
[32:43] Yeah. So this one is not live yet, but we'll be very soon.
[32:52] It also now renders the interface from the config. Like in the config, we can have different chains
[33:06] or configs available, sorry, to be enabled or disabled, or it also checks what payment options
[33:13] is coming from the server side. So any questions?
[33:22] - Will you go back one screen, Mikhail? So this image that's on the right side,
[33:29] is that, which of these screens would the user see first? Or are these two different ones?
[33:36] - User will see first the first point. Yeah, the first point that was set, his address in there.
[33:49] - Okay, I guess I do have a question, which is when will Dash be moved up the list,
[33:57] either as a result of alphabetical sorting or pure preference?
[34:03] Because we don't like to see Dash at the end of the list. We talked about this the last time.
[34:07] - Yeah, any time I can- - There's gonna be a little remote flogging
[34:12] after the show, Mikhail, if this doesn't get fixed. - Okay, yeah, actually it's just alphabetically, yeah.
[34:19] Yeah, it depends on how many cryptocurrencies addresses you have in your account.
[34:27] How long is the list depends on that. Okay, if there are no more questions,
[34:37] I will go to the next project, it's the Dash Mate. This is the project that I'm helping with DCG,
[34:46] like we are doing this project together. For those who didn't know,
[34:57] like who didn't know about this project, is that it's like a wizard for setting up
[35:04] your master nodes or your local development. And it allows you to easily handle your nodes
[35:13] on your servers. Like you don't need to mess up with a lot of comments.
[35:18] Instead, it just gives you an easy command line interface. So what was done is first,
[35:27] I updated it to the v25 testnet. So it wasn't working.
[35:33] There was some stuff. There was some stuff around Docker entry point.
[35:40] So some Docker stuff, and there was, I needed to update some config in the Dash Mate
[35:49] to meet recent v25 images. Then what was, (coughs)
[35:58] sorry. Then we found out that the Dash Mate SSL renewal
[36:04] is going to be triggered soon in the testnet. And the Dash Mate SSL renewal wasn't working right.
[36:13] So this trophy alarmed us about that. And we checked it together with Ivan.
[36:23] We were checking different stuff. So there was different stuff
[36:31] because different things that we fixed. And eventually we checked that all the flow is working.
[36:40] So the Dash Mate have a renewal mechanism for, so when you deploy your node with the Dash Mate
[36:52] and you run platform, you need an SSL certificate. Dash Mate allows you to issue the certificate from zero SSL
[37:03] and make an automatic renewal. So it happens, everything happens in the background.
[37:09] Yeah, it took time for us to make all the fixes because there was different things,
[37:19] but we finally get it. So when all of the testnet nodes
[37:26] was able to renew the certificates. So the testnet wasn't disrupted,
[37:32] at least at some point. Yeah, we also checked the issue
[37:41] that firstly reported by Queasy on the Dash forum. So what happened is that Docker Compose plugin
[37:50] was recently updated. Not the Dash Mate, but the Docker Compose plugin.
[37:55] And the people who was updating their system via this upgrade or any other way,
[38:03] they were experiencing a year that they couldn't make any comments.
[38:12] So that happened because the Docker Compose plugin introduced a breaking change.
[38:16] And yeah, we found out what was the reason. The reason was that the JSON
[38:25] was transmitting the different way. And we made the code to use the different schemes.
[38:44] So the Dash Mate is now able to read all the Docker Compose plugin versions.
[38:49] So whatever you updated or not, the Dash Mate on the recent version
[38:54] will be working for you. So a little plans about the Dash Mate
[39:00] that we will be working on is, this one is really, really not much.
[39:11] Like it's about reorganizing the structure of the SSO certificates.
[39:16] We need to put it into each of the node config there because right now it moved out and it just,
[39:28] well, it's blocking us in the code in some places and also it's just not convenient.
[39:36] It's better to have it inside. We also need to disable the config re-render.
[39:43] It will increase the performance of the Dash Mate commands because right now Dash Mate re-renders all the configs,
[39:53] all the service configs, the JSON configs, the Dash D config and all the,
[40:01] everything it re-renders on each command run. Like there is a base command handler
[40:07] which first read the JSON config and then writes it again. That doesn't look great and it actually makes some troubles
[40:20] in the Dash network deploy tool because it makes the JSON config not consistent.
[40:27] Like it's not indepotent, if I'm saying it correctly. Sorry.
[40:35] - Yeah, it's not indepotent for anybody who's running. That just means if you run it twice,
[40:42] it's not going to have a problem. No matter how many times you run a certain command,
[40:48] it's not gonna have a problem. It's not gonna be different if you run it once
[40:51] versus three times. - Yeah, so the task is about disabling Kafka re-render
[40:58] and the config will be only re-rendered if something important was changed,
[41:05] like config is changed or some reset happened, stuff like that.
[41:10] We also need to extend the test suite to execute the migration process.
[41:20] In the Dash Mate config, we have like migration mechanism. Like many backend developers can see
[41:32] for the databases like they do database migrations before they run their server, their backends.
[41:41] So the process is similar. We have different versions
[41:44] and different versions have different config schema in the Dash Mate.
[41:49] And to meet the latest versions, we have to do some migrations.
[41:55] Right now, we don't have the test for successful migrations.
[41:58] That means that if someone uncarefully push some code and someone will miss this like typos or stuff like that,
[42:09] the test will check that at least migrations is working and basically operations is working.
[42:18] So yeah, we just missing this exactly this case. Yeah, so any questions?
[42:28] - Nope, I don't think I have any questions on that other than maybe, well.
[42:39] Yeah, no, I don't think I have any questions on that. Amanda?
[42:46] - No, definitely not. Other than, it's not a question, it's more a comment.
[42:52] Did I hear you use the word uncareful, Mikhail? I think that's the first time I've ever heard that word
[42:57] and I like it a lot. That was an uncareful thing you did, sir.
[43:04] Do try to be more careful next time. Good, okay.
[43:09] Well, that is it for us today. Thanks for joining us, everyone.
[43:14] And next week, we will be fresh off the Dash retreat and we're live streaming it all weekend,
[43:23] every presentation from every speaker will be live streamed whether they're there at the conference
[43:28] or calling in remotely and we have a smashing mix of both. And so do check the, we'll just put the link
[43:37] as a comment to this video because in our medium post with the agenda of the event,
[43:43] there's a hyperlink to every streamed presentation. So you can just click right on them as they're happening.
[43:48] And then we'll have a recap about the whole thing next week on Monday.
[43:52] That sound good? - Yeah, do we get to see that over the top promo video
[43:59] for the retreat on our way out of the show today? - Oh shoot, let me see if it's still on the backend.
[44:07] Let me check. No, it's gone, so sad.
[44:14] But yeah, we'll put it as a link in a comment as well. If you haven't seen the promo video for the Dash retreat,
[44:22] be sure to click that and watch that. - Okay, all right, see you guys, thanks.