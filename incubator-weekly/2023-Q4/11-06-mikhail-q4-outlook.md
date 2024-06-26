---
showLink: "https://www.youtube.com/watch?v=9EIaZdx6C-M"
slug: "mikhail-q4-outlook"
title: "Mikhail's Q4 Outlook"
publishDate: "2023-11-06"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/9EIaZdx6C-M/maxresdefault.webp"
---

Mikhail discusses his current and future Dash projects including Dash Platform Explorer, Electrum, DashMate, and Trust Wallet InstantSend support.

## Episode Summary

tl;dr: Mikhail provides an update on his various Dash projects. Platform Explorer now supports searching Identities and viewing associated data. Dash Electrum and DashMate have new releases with bug fixes and improvements. Mikhail plans to work on enabling InstantSend support in Trust Wallet by modifying the BlockBook API it uses. He also discusses ideas for data contract migration tools and educational videos to help developers working with Dash Platform.

## Chapters

00:00 - Why We Build
Intro video explores crypto scams and misconceptions about crypto.

04:55 - Platform Explorer Updates
Mikhail discusses the recent updates to the Platform Explorer, including the addition of Identities features that allow users to search and view data related to Identities. He also mentions some UI improvements and future plans for the Platform Explorer.

13:07 - Dash Testnet Status and Electrum
Mikhail and the host discuss issues with the Dash Testnet being stalled. They then move on to talk about updates to Dash Electrum, including fixes for the v12 testnet, new Coinbase transactions, and updated translations. Mikhail also introduces a new "dashcore-cli" command in Dash Electrum.

23:02 - Dashmate Updates and Config Migration Tests
Mikhail shares updates on Dashmate, including changes to how it renders service configs and the introduction of a new "dashmate-core-cli" command. He also discusses a config migration unit test that ensures builds don't break the config.

29:10 - Trust Wallet and InstantSend Support
Mikhail talks about his efforts to get the Trust Wallet to support InstantSend transactions by working with the BlockBook API used by the wallet.

34:12 - Dash Platform Development Tools and Tutorials
Mikhail discusses his ideas for improving Dash Platform development tools, including a migration tool for data contracts and creating video tutorials to help developers get started with Dash Platform.

41:52 - Dashmate Mobile App Idea
Mikhail shares his idea for a Dashmate mobile application that would allow users to monitor and control their Dashmate nodes remotely. The app could be useful for masternode operators and hosting services. The video ends with the hosts thanking Mikhail for his presentation.

## Transcript

[00:00] A couple weeks back we reviewed a global survey done by ConsenSys. One question asked about the barriers to entering the crypto ecosystem.
[00:15] Too many scams. What's up there?
[00:17] Around this same time I received in my inbox an email from AAA. When scanning that email I was surprised to see a write up on "crypto scams".
[00:23] Is this actually a big problem or is it mere hype, perhaps made to discredit crypto? A quick search for "crypto scams" on Google brings up a lot of content, much of
[00:31] it recent. The same is true of YouTube.
[00:33] This first video return has almost 4 million views, it must contain some truth, right? It's an hour long, so I'll give a summary, and yes, I did watch it.
[00:41] The narrator puts forth that Bitcoin had promise, but suffered from scaling issues that were never addressed, and thus, can never function as a currency.
[00:48] That's fair. The narrator then says that Bitcoin attracted the "suits" who sought to use it opportunistically,
[00:53] and that "the subsequent waves of ICOs, NFTs, and now Web3 are a massive mania and bubble that is being fueled by greed and delusion."
[01:02] Admittedly, there have been plenty of scammy actors in this space, but is it fair to say that "crypto" is a scam?
[01:08] No, especially as some crypto projects have not given up the goal of being currency and have continued to innovate to see that reality.
[01:14] But viewers of this video were never informed about such offerings. Instead, many will leave with a tarnished image of anything that purports to be crypto.
[01:21] That's a shame. Back to that AAA email.
[01:24] Aside from this claim that "crypto cannot be double-spent," which is inaccurate for some crypto networks, the text relates to crypto scams involving older folks and cites
[01:32] a figure of $3 billion lost. One scenario would be victims receive an email or a cold call, are told there's an issue
[01:38] with their bank, and that they must buy and send crypto to put things right. This is known as a tech scam, and yes, people do fall for them.
[01:46] Consider Marjorie Bloom from CNBC covered last month. When Bloom was using her computer, it froze, and a pop-up, ostensibly from Microsoft, but
[01:53] really from a scammer, advised her to call a given number. She did, and was told that hackers had taken personal information from her computer and
[02:00] that she should speak with someone at her bank. Bloom divulged the name of her bank, PNC, and the scammer then transferred her to an
[02:06] accomplice who posed as a PNC employee. Over the next month, Bloom sent five wire transfers totaling $661,000, and which eventually
[02:14] landed in a crypto wallet controlled by the scammers. In another post, this one at Fortune, the most common crypto scam is said to be the
[02:20] fictitious investment opportunity, and that scammers may pose as successful investors, potential romances, or even known friends.
[02:28] A Department of Justice press release from earlier this year noted the seizure of over $100 million in crypto linked to investment scams.
[02:35] As one employee rightly pointed out, "Using the method of traditional con artists, high-tech fraudsters have taken advantage of the publicity and hype surrounding cryptocurrency to encourage
[02:44] an untold number of Americans to invest in 'get-rich-quick' schemes." This focus on investments is echoed in a write-up at Morgan Stanley, which is understandable
[02:52] as they're an investment bank. At least they acknowledge that crypto can be used for payments, and, unlike the other
[02:57] write-ups we reviewed, which tend to outsource responsibility, they conclude with some actionable advice, "Be vigilant."
[03:03] But be vigilant, or on the lookout, for what exactly? Let's turn to a pretty trustworthy source, Guy over at Coin Bureau.
[03:11] Last year, his team put together a lengthy video about crypto scams and how to avoid them.
[03:16] If it sounds too good to be true, then it almost certainly is. They covered the giveaway, the rug pull, the impersonation scam, Ponzi schemes, phishing
[03:25] scam, the pump and dump. So what can you do to not get scammed in the space?
[03:30] The moment you remove the idea of easy money from your head, you're never going to be scammed. Are you involved with crypto only to make a quick buck?
[03:37] Do you see it merely as an investment? Then chances are you'll be more apt to make quick decisions and thus more susceptible
[03:43] to scams. But if you're into crypto to help make the world better, then chances are you'll do
[03:47] your homework. You'll act deliberately.
[03:49] You'll have a long time horizon. That's not to say you won't lose money, but if that happens, it'll be due to the
[03:53] competitive forces of the free market, one product being preferred to another, rather than a malicious actor.
[03:59] To summarize this point, if you really want to mitigate your risk of being scammed, you may need to change your mindset.
[04:04] You may need to ditch the materialism that's pretty ingrained in our culture. Beyond one's mindset, what else can be done to mitigate being scammed?
[04:11] Easy. Don't trust a stranger with your crypto.
[04:14] Trust yourself. What does this mean?
[04:16] Cease using custodial services and instead self-custody your crypto. Especially attractive for older adults who may not be as tech-savvy, maybe a novel custody
[04:24] solution such as a multi-signature. Thus, if grandma is about to get scammed, her kids, before signing with their own keys,
[04:31] may realize that things sound odd and investigate to ensure that the scammers don't win. And while not the main aim, if we're successful, if we build a crypto that becomes currency,
[04:41] it will assuredly have more stability. And with more stability means less get-rich-quick schemes could find purchase.
[04:47] Let's make it happen. Hello, everyone.
[04:49] Welcome to Incubator Weekly. Hi, Rion.
[04:51] Hi, Mikhail. Hey.
[04:53] Yeah, let's make it happen. Right?
[04:55] You know, I have wondered, if anybody can give me a brief answer, what are we missing in Dash, if anything, that having a multi-sig wallet is not much easier?
[05:17] Because I am embarrassed to say that I actually am related to an older person who actually bought Dash from me.
[05:28] And fast forward a number of years later, despite my best efforts back then to show him how to guard his private keys, he lost them.
[05:36] And now his Dash is gone. And I'm just thinking to myself, why didn't I set him up with a multi-sig where, say,
[05:41] Pete and I could have kept track for him? What are we missing that's not in a wallet already?
[05:48] The mobile wallet. Yeah, like a one-of-two.
[05:50] One-of-two. What?
[05:52] One-of-two? Go ahead, Mikhail.
[05:54] Hey, everyone. So first of all, I want to thank everyone who voted for me in the last Superblock for
[06:12] my proposal. I really appreciate that really a lot of nodes have voted for me, and that's really
[06:20] a lot of support. So yeah.
[06:25] Before you get started, I'm actually curious, I don't know if you heard Amanda's question, but do you know of any multi-sig, do you know of any multi-sig libraries or applications
[06:38] for Dash right now? I can't remember one.
[06:50] I don't really remember. The last one that I remember was our fork of the, it was a BitPay wallet, and I can't
[06:59] remember what it was called, but it was-- Corelib.
[07:02] What was it? Dash Corelib.
[07:04] CoPay? CoPay, that's right.
[07:06] Yeah, that was the last application that I've seen that had Dash multi-sig support in a user interface, and I'm pretty sure that, I think that the library probably supports
[07:21] it, but I don't know of anybody who's put a UI around that library, if it even exists, the library at this point.
[07:30] Is CoPay still around? No, I don't think so.
[07:36] Not in the Dash version, anyway. Okay.
[07:39] I also don't remember this kind of stuff in the core, so I don't remember much in the libraries that we have in the JavaScript, you know, and all this stuff.
[07:50] Okay. Well, that is on my Christmas wish list for Dash.
[07:54] I'll just say that now. So moving on, we are here to speak today about Mikhail's projects for this quarter, both
[08:05] what is - well, actually, I don't even know what he's going to tell us, so why don't we just go right to what you have to tell us, Mikhail?
[08:14] Yeah. So I'm already working on a few of the projects in the Dash incubator.
[08:24] Some of them are Dash Electrum, some of them is the Dash Mate that I continuously contribute that helps you to set up master notes and stuff like that.
[08:41] I'm also taking care of the AnyPay integration, which is of the non-Custodial payment processor, and there are other stuff, like - so there are some other ones like Platform Explorer,
[09:02] for example, which have gained a lot of interesting features last week. So I wanted to share you with some of these that I have right now, and let me show you.
[09:20] Let me start from the Platform Explorer. Can you see my screen?
[09:30] Yes. Yeah.
[09:32] So the last two weeks, we spent the time on the Identities features, and the Identities features is finally live on the Platform Explorer.
[09:44] That does mean that now you can search Identities, you can see Identities data, like Identities balance, Identities transactions transfers, and other things.
[09:56] And that was a forum post on the Dash forum, so if anybody wants to look at that in detail, that's where it is.
[10:06] Yeah. So now we have pretty much basic functionality implemented in the Platform Explorer, and
[10:14] the API. So now we can see the extended statistics, we can see on the homepage the latest transactions,
[10:24] we can view all of our Identities, if we click on some of them, there are some UI issues on some resolutions, but we can see all the data, we can see the transfers, we can see
[10:41] the balance right here, for some reason this has zero balance, but it has documents, I don't know why this is happening, sorry.
[10:51] So anyway, this one, for example, has this amount of credits, and this was a top-up in these transactions, we can see the particular transactions that were sent by this Identity.
[11:10] And we can also check any data contracts, we also had a really big redesign of the Platform Explorer, so it can look more human-readable, you know, and stuff like that.
[11:24] We can check the data contracts and can see the documents that are being inserted inside the data contract, that is stored inside the data contract, we can see the schema of these
[11:36] applications that we have right now. For example, this one, I believe, I think that's something like Dash Money stuff, yeah.
[11:49] For example, this one, the first one should be the, some of them should be the DPNS, not this one, I think, but anyway.
[12:05] So yeah. I have a question before we move on, is Testnet, I've seen a lot of back-and-forth chatter
[12:14] on the Testnet channel of the IncuDevs or DashDevs Discord. Yeah, there are issues right now, there are issues with the banning of the Evernotes,
[12:27] the team is finding the problem right now. I guess it's stalled still, as we can see, yeah, for hours the platform Testnet is not
[12:38] working again, but the guys should fix it soon, and happily, I didn't do anything. For example, last time the chain was halted, they unbanned the nodes, restarted the platform,
[12:53] the platform chain wasn't, like, you know, it wasn't wiped, it was just, as soon as the quorums was restored, it just continued working, just continued proposing the blocks, and you
[13:06] know, and my node, I didn't change anything in the backend, it just continuously pulled up all the blocks, so as soon as the network will remain in stability, the platform explorer
[13:19] should continue indexing blocks. Is there anything on this platform explorer that shows the Dash Testnet uptime or downtime?
[13:33] Not yet, but you can see it by the timestamp of the last block. That's a good idea, I think it's worth making a message, like, you know, like some warning
[13:43] message, if there are no blocks in the last, like, one hour or stuff like that, we can show a yellow warning, like, the chain might be stalled or stuff like that.
[13:55] So yeah, it's a good idea, and actually we gotta have some kind of dashboard of monitoring of all of our services, eventually, so we can check and, you know, monitor stuff better.
[14:12] So yeah, the basic stuff is there, and the new features of the platform explorer, I don't know what would be the next step for the platform exactly, there are some features on the GitHub
[14:33] that we already have, not this one. So there are some of the issues that's left, but I think you can guys suggest me an idea
[14:53] for my platform explorer project, what you wanna see on the platform explorer, any kind of backend or frontend stuff, for example, one of the feature could be like, you know,
[15:05] like subscriptions on some kind of events or stuff like that. You can fill anything you want, I will check on that, and hopefully...
[15:12] How would you prefer people make those requests? In the GitHub, in the GitHub projects, like, in the GitHub issues.
[15:22] Okay. Just a technical question out of curiosity, what is the backend of your project for the
[15:29] explorer doing, other than delivering and serving the HTML page? Is it...
[15:36] Is anything being... Actually, yeah, I can answer your question.
[15:41] So the HTML is being created by React, it's totally the client-side application, and there is a Node.js backend API that could be used by anyone, like, I will create a separate
[15:54] how-to, like, you know, page, like, manual page where you can see how to use platform explorer API.
[16:02] So there is API where you can query blocks, you can query transactions, state transitions, transfers, you can decode transactions, like, you can just send straight base64 string and
[16:16] decode it without being, like, you know, dependent on the dash SDK library to decode it. Okay.
[16:26] So when a user makes a request to the website for the platform explorer, the backend presumably is then calling into platform on the server side and then delivering the data, populating
[16:38] the HTML, sending it to the clients? It actually pulls...
[16:42] It actually fires a request to the API backend, it fetches everything from the Postgres SQL, so there is an indexer...
[16:53] You have a Postgres database? Yes, yes, indexer is posting everything into Postgres database, each block, each block
[17:00] I continuously index each blocks in the platform network. And why, just from a technical standpoint, why do that versus just get data updates from
[17:12] the client? Because it's faster, it's more consistent, it's more flexible, because we can do some
[17:20] kind of statistics, we can... I think it's faster, it's faster because we have everything, like, you know, not locally,
[17:30] but it's much faster than we would fire a DAPI request, and actually I don't think that everything could be implemented with the DAPI.
[17:40] Okay, and then just one more technical question. When the application is served to the browser, is it real-time updating or do you have to
[17:48] do a hard refresh on your browser to get new data? Not yet, not yet.
[17:54] Yeah, you have to hard refresh right now, but it's a good idea to include it. So I was thinking about that.
[18:01] Thank you. Okay.
[18:03] Well, I'm pumped to look through this Platform Explorer, because I remember, you know, first learning about blockchain or whatever years ago, like, it's one thing to read about it
[18:15] and talk to people about it, but then for me, anyway, it was a whole, like, a little light turned on the first time I looked at a blockchain explorer, and it just, it helped
[18:26] it make more sense. So I'm keen to dig into this.
[18:29] What else do you have for us? So yeah, another project is the Dash Electrum that we recently fixed for the v12 testnet.
[18:42] We implemented new Coinbase transactions, and I also checked the Transifex translations. We updated the Transifex translations for the Russian translations, it's now 100% translated.
[19:04] We released a new version, which also includes new backend servers for the Dash Electrum, which was out for some time.
[19:14] So now we have Dash Electrum working, and everyone who downloads the recent Dash Electrum version, he will be able to use it, like, without any issues.
[19:25] There is... Wait, do they have to manually enter any server configurations, or does it come by default
[19:33] now? If you download the version, the latest version is 4.5.7.2, you don't need to do anything,
[19:45] you will be okay. The servers are hardcoded in the code, the default servers, which currently points to
[19:55] my infrastructure, which I maintenance. Yeah, people can change that if they want.
[20:08] Can they go to your repo, and is there enough documentation on the Electrum server repos so that somebody can spin up their own backend instance and reconfigure their frontend to
[20:22] point to their own server? Actually, the pull request for the Dash V12 changed.
[20:30] So for testnet, I think there is a pull request that should be merged by the maintainer, which is still not merged.
[20:38] But for mainnet, yeah, there is documentation that Electrum server is okay for mainnet. For V19, what we have in mainnet, everything is working on the Electrum server.
[20:48] So anyone who wants to deploy that, there is already documentation, there is already the codebase, everything is okay.
[20:57] Everything is supported. Yeah, for V12, for the testnet, for our future fork, we have to do some things.
[21:08] There is still missing private send support, the LLMQ quorum is still not quite working correctly.
[21:16] I'm looking into that already, and I think I will have something in the upcoming weeks. Do you know what specifically broke about the server-side or even client-side private
[21:35] send support that needed to be fixed? Yeah, I checked.
[21:41] I think there are different things. First is the client, which does not load up the masternode list for some reason.
[21:54] And I think the server-side will also need to be updated, like the Electrum stuff. There was some kind of breaking change in the protocol between the time that the last
[22:09] maintainer set it down and you picked it up. The breaking change was introduced, I believe, in July in the V19 fork, there were changes
[22:19] in LLMQ quorum, so I just had to update it. I don't think that would be so hard, so I just need to dig into that.
[22:34] And then the last question on Electrum for me is, have you tested the mobile client application? I'm not sure if it's a different application, I'm pretty sure it is a different application
[22:49] like Android. Is that working with your server backend?
[22:59] That's a good question. Personally, I don't.
[23:02] I didn't. So there is APK, so I mean, the build is out, the build is there, of the new version, we
[23:17] have to check. I personally haven't checked it yet.
[23:25] What else do we have? As for DashMate, there is another release, another stable release of DashMate, and we
[23:40] included some very important changes. Can you zoom in a bit if you can?
[23:47] Yeah. Let me just zoom it in.
[23:53] Looks good. So the most important change was that we changed the way DashMate renders the service configs,
[24:06] like the configs for the dash core, for the drive, for the tender dash. So previously, we just, every time you just run the DashMate command, it was re-rendering
[24:19] all the service configs. That was causing some troubles, because it wasn't so impotent in our deploy tool, in
[24:34] the Ansible, so it was changing some things, and it was also making some weird behavior in the Docker environment, where basically, I fixed it in the Docker entry point script,
[24:49] but it was causing some troubles with the permissions, because it was rewriting as root. So anyway, the approach was, like, there was some advantages of this approach.
[25:02] You could just simply change your config, and every run, it will just re-render all of your service configs, but it also has some downside, like, it's not quite efficient that
[25:12] you write your configs every run when there is nothing really changed. So we changed that and made it like, you know, it just don't re-renders everything on the
[25:28] each run. I also introduced a new command, which will be very, very, like, useful for people, like,
[25:40] when you need to throw some stuff in the core, like, there is now a command called "dashcore-cli", "dashcore-cli", which lets you execute core RPC commands.
[25:54] It may be helpful when you, like, for example, want to find out what's wrong with your node, or maybe you want to do some stuff, I don't know, you want to check chain logs, quorums,
[26:07] whatever. So, just to recap what that means to me, is anything that you could run using the dashcore,
[26:16] the native dashcore binary from the RPC, like, git status, or git info, or any of those, even masternode, proregtx, I'm assuming, anything that, any kind of command that you could run
[26:32] with dashcli, you can now run through dashmate, is that right? Yes, yes.
[26:38] So that you don't need to copy your docker container ID and manually execute docker access, so some complicated commands is just simplify the approach, like, you just can simply, you
[26:50] know, type the "dashmate-core-cli" and type your command without any unnecessary stuff. Cool.
[26:58] Yeah, I also fixed the payment key position that was reported earlier by Kwesi, and extended the enabled count to respect the dashcore statistics that they show, the total count
[27:15] of the regular masternodes, of the evenodes, total and enabled count. And very, very useful thing that really already helped us, this is the config migration unit
[27:27] test that ensures that our build doesn't break the config and everything is, you know, there is a configuration and this configuration often changes over the versions, like, some
[27:41] stuff is being added to the config and we have to migrate a config each version. When the new version is out, you have to do some kind of migration of your config too,
[27:52] so that it matches the new schema. So there is a unit test that's being run in the CI, which ensures that we don't break
[28:02] and all the versions that we have in our config matches what we expect. So it already helped us a few times during our latest release and this was really, really
[28:14] good stuff. Yeah, I also, so that was kind of all of my recent updates.
[28:29] And I wanted to let you know about my plans. One of the projects that people was asking me to check is the trust wallet that doesn't
[28:42] enable instant send. Like people always like asking why the trust wallet is not loading the, well, the zero
[28:50] confirmation is not working in the trust wallet. This is the trust, the mobile trust wallet application.
[28:56] Yes. Yes, exactly.
[28:58] It's like a third party, somebody they're asking about a third party wallet that, you know, DCG, nobody in Dash is maintaining, it's obviously a separate application altogether.
[29:10] Yeah. I reached out to devs of the trust wallet, happily they are also Russian speaking, and
[29:20] we talked about this thing. And so the thing is they use BlockBook API, which is the Trezor backend.
[29:30] If anyone knows that and yeah, they use like XPUB API call, which BlockBook does support the instant send.
[29:48] You can query things, specific things, like there is a query for the specific, but it isn't implemented for UTXO query calls.
[29:58] So there are different calls when you, you can get the transaction, yeah, you can get the transaction, but the trust wallet is loading the whole balance by the XPUB, which is basically
[30:08] the seed phrase. So there is a API call on the BlockBook API, which.
[30:15] It's called BlockBook or how was that spelled? Yeah.
[30:18] So BlockBook is the API backend for acquiring balances, like some kind of blockchain info or any other, you know, provider of the API.
[30:32] So basically there is an API call that shows you the account balance by the seed phrase. And this call doesn't include the instant send transactions.
[30:46] I made, I made an issue. I created an issue in the BlockBook trying to ask them, how can I proceed with that?
[30:58] So my idea right now is there is two approaches. First approach, I will try to modify the XPUB API call and suggest guys to include these
[31:12] changes. The second option is to go with some other thing, which is also in the API, but a bit
[31:24] different way. So right now, the key thing here in the trust wallet is that they rely on the BlockBook
[31:33] API that doesn't show you instant and confirmed transactions. So we have to have a way to, I don't know.
[31:46] It's a bit troubling because Trazor is, you know, obviously they, Dash didn't include, they didn't include Dash in their latest model.
[31:57] Yeah. Yeah.
[31:59] There's a little bit less of a priority to support Dash things over on the Trazor side. So hopefully, you know, they'll get this in there, but that is interesting to know that
[32:11] trust wallet is using BlockBook for their backend. Yeah, I know about this, this thing, but, but still, I think this just a software, like
[32:24] we can just pull the, the changes in and make all, all the work that we need without like, you know, it's just software, Trazor.
[32:36] Listen to Mikhail. It's pretty easy.
[32:38] Did, do they have any comments on, on your issue yet or no? Not yet, not yet.
[32:45] It's not, not that regularly maintain it. There is one maintainer, which I didn't find the explicit context, you know, which I can
[32:54] ask, but, but I hope if I have something already, like, you know, there is some go code, the whole project is in the goal.
[33:03] I think I need to make some changes and just make it easy for them to propose it. Yeah.
[33:10] Yeah. I'm seeing two weeks ago in, in the comment right there, and I'm just wondering, okay,
[33:17] you know, obviously they have triage over there and they're not going to get to issues right away, but two weeks, that's been quite a while.
[33:24] So yeah, I think, I think a pull request would be a good idea. Yeah.
[33:31] And yeah, I'm going to look into that so that more wallets, more third-party wallets will support InstantSend and zero, zero-coin transactions so that we can increase our adoption.
[33:46] Yeah. Trust wallets is a big deal.
[33:50] I think that they're, they're one of, if not the biggest and most, with the most users wallet, mobile wallet anywhere.
[34:01] So that, that is a big deal. Yeah.
[34:04] I use it. I use trust wallet.
[34:06] It's a good app. It's a good app.
[34:08] So I think this would be a good thing to do. Yeah.
[34:12] So there are other project ideas that I have that mostly about the development of the platform development and development tools.
[34:26] There are not quite, not quite, I don't have quite specifications on them yet, but I can just like briefly, just tell you about the things that we probably miss.
[34:39] One thing that I was thinking about is that we miss some kind of migration tools for data contracts.
[34:47] Yeah. For example, in the Ethereum, we have a tool for deploying your contracts.
[34:54] It's called, if I remember, it's inside the Truffle test suite. So there is a migration tool that allows you to just insert your seed phrase and it will
[35:07] deploy into your network and it will store some, some side, like it will deploy your contract.
[35:16] And as a result, it will give you some kind of state file, which you have as the deployed smart, like as a deployed thing.
[35:26] For example, we have a dash testnet being wiped pretty, pretty often. And every time that the network comes up again, every dApp creators have to deploy their tools,
[35:43] like their data contracts again. And they do that via custom scripts, like for the dash SDK, they just made it for the
[35:53] front end or some from the Node.js side. So I think it's worth to have some kind of migration tool that, that will help you keep
[36:04] your data contracts in the network, you know? Yeah.
[36:10] Yeah. Yeah.
[36:12] An easy, an easy redeploy tool. And not only redeploying after testnet is platform or mainnet, but also schema changes.
[36:24] So yeah, yeah, yeah, definitely. So as the project goes on, like you have different versions of the data contracts, you have,
[36:34] you have to deploy it each time. So developers should have some, that tool to do that.
[36:42] What are the, what's the overall process right now? If somebody wants to create a dash platform app, what, what is the overall process that
[36:53] they should go through? They have to write up a data contract schema, then...
[37:01] And what's the best way to do that? I think dashpay.io.
[37:08] I was wondering if you'd say that. So that is still the gold standard for, do you want to bring that site up real quick?
[37:17] Yeah, sure. So if you want to create a data contract that will be stored on dash platform, this is the
[37:27] easiest way to do that so far still. Yeah.
[37:30] Yeah. Maybe just, just scratch some fields, you know, and, and render it.
[37:40] So what's the next step? The next step would be to deploy it with your dash SDK.
[37:49] So for that, you need to create a page if you're doing it from the front end, or you need to make a script, which will, where you can import this, this contract, it can import
[38:03] via JSON, or you can just put it in straight into code. So it's kind of complicated.
[38:07] You can, you need to also take care of, of your private keys of the seed phrases and, and yeah.
[38:18] This site does not deploy your... Yes.
[38:21] Yes. Yes.
[38:23] Exactly. Just creates a schema.
[38:25] So yeah, it allows you to deploy your data contract. But as I remember, Paul, yeah, Paul, Paul was, was telling like, he's about to add this
[38:40] feature on the website. So maybe sometime this feature will come up on this website.
[38:48] Yeah. Okay.
[38:51] So yeah, what I'm also going to do is I want to like create some videos. I want to create some media on how to make this development, like how the development
[39:09] is working in the dash and how to make things like in the, in the recent like weeks, I'm going to shoot some videos, which will show you how to install some things like install
[39:23] some tools and stuff like that, like dash mate or videos like how to use dash SDK to query stuff or stuff like that.
[39:34] So that, that can help people which really running into problems while picking up, picking up the, the dash platform development, like they're, they're just getting into, into development
[39:52] and they, they get some errors and they just don't know why this is happening. And such videos, I think will, will show like the exit steps, like what is missing and yeah,
[40:05] it should also add some platform stuff and I believe that will increase like, like, you know, the whole, the whole thing will, okay, it's just a good idea to have this videos,
[40:22] you know? Yeah.
[40:24] I think a lot of people rely on, on stuff like that where when they want to get started with something, documentation is always a good place.
[40:31] It's good to have good documentation, but I don't think that there, there's no substitute for just seeing somebody do something.
[40:38] So that's a good idea. Yeah.
[40:42] And what channel do you intend to publish your videos on, Mikhail? I don't know yet.
[40:47] I'm okay with, with any, like, I only care about the, the, the content, you know? Okay.
[40:56] And will it be in English and Russian and both? What do you think?
[41:00] It's good. It's good question.
[41:02] Um, I think both, uh, I think we should do both. Um, there is a quite good demand, uh, in the both, uh, in, in the English and in the Russian
[41:13] language that are quite a good demand on such videos, uh, especially for the videos describing how platform works and what is actually platforms.
[41:22] Many people still don't understand, uh, what it is about and why, why, why this is important. Like, uh, they only might be careful like other things, but, but don't really understand
[41:35] what, what the dashboard for me is. So, so yeah, um, I think we should do all the, all of this stuff.
[41:43] Um, what I want to do is just, just start doing that, um, in, in any like term, like, you know?
[41:50] Okay. Yeah.
[41:52] That's good. And you know, you're, I don't want to put you on the spot, but, uh, I think as far as
[41:57] I'm concerned, you're, you're more than welcome to, uh, stream some of your work, uh, through the incubator channel like AJ has done.
[42:05] I'd like to get more people. Yeah.
[42:08] Yeah. It's a good idea.
[42:10] It's a good idea. Uh, it's a good idea.
[42:12] I will think about that. I was, I was thinking actually, uh, not really like I was doing some other stuff.
[42:18] Yeah. Yeah.
[42:20] Just, just something to consider that invitations open to, to you and you know, other others as well if they want to get involved.
[42:27] Okay. Okay.
[42:29] Yeah. Okay.
[42:31] Sure. Sure.
[42:33] That's, that's quite good. Yeah.
[42:35] Anything, anything else that you, so you covered what you have worked on, you covered what you are planning on working on in the next couple of months here through the end of Q4.
[42:45] Anything else that we missed? Um, um, yeah, there is some, uh, one project that, um, that we, that I was posting, uh,
[42:57] on the Dash forum that was about the DashMate, uh, related to the DashMate. It's just about the Dash, DashMate, uh, mobile application that will allow you to query,
[43:06] well, sorry, uh, to, uh, to check the status of your nodes. I remember you mentioning that before.
[43:13] Uh, it was called like, uh, DashMate, uh, uh, remote control, I believe. Uh, um, yeah, it was a proposal, uh, for such, for such application and, uh, I made a couple
[43:36] of, uh, you know, designs or something, you know, like scratches for this application to let you know, yeah, what you think about that.
[43:44] Uh, so the idea of application is pretty straight. Uh, you can have your DashMate deployments, uh, you have some DashMate nodes, like you
[43:54] have mainnet, you can have mainnet, uh, you can have testnet nodes, platform nodes, local nodes, uh, anything that is being deployed, uh, to the server.
[44:04] Uh, you can, uh, uh, you can configure, uh, your nodes in the application, you can add them as a list, uh, and then, uh, the application will query that, uh, through the SSH, uh,
[44:22] through the secure protocol, uh, this will query your status of your node, if it's online and when the next payment is occurring, uh, it will allow you to make some changes in
[44:33] your DashMate node, like you can restart it, uh, check logs, uh, execute some commands, uh, stuff like that.
[44:41] Um, does this launch nodes or just check the status of existing nodes? Um, um, because it's a lot more work, yeah, um, theoretically we can do, we can, we can
[44:57] do both ways. Right now it's just only checking, uh, like it's just a mockups, first of all, but right
[45:06] now, uh, the DashMate allows you to just to check the status, the DashMate API, I believe, uh, is only being run when you just start the node, but, uh, I think it's not technically,
[45:20] like, technically you can do that, um, there is nothing stops you from, uh, uh, from making that, like, uh, you can even set up, you can even, uh, you can stop, start and do all of
[45:35] the stuff and stop your, uh, new nodes and, uh, uh, and I think this application can also, like, be very useful for some, uh, master node operators, which, um, like, uh, I believe
[45:51] this can be integrated in some, uh, master node hoster, like, uh, crowd node, well, not crowd node, but maybe, maybe some other people who also have some master node hosting solutions,
[46:05] they can, uh, leverage, uh, this application, uh, for their clients, uh, to let know what, what, what is actually is going on, uh, with their, uh, DashMate nodes.
[46:18] Um, yeah, um, I think that's pretty much it, um, yeah, uh, what I wanted to share with you.
[46:29] Right on, okay. I think that's all we need to know, so, um, thanks for your preparation and sharing with
[46:40] all of that with us today, Mikhail, I'm gonna go dig through the platform explorer as soon as we end this call.
[46:48] Yeah, yeah. Yeah.
[46:51] Okay. We'll see you next week everyone.
[46:53] All right. Bye everyone.
[46:55] Yeah. Bye.