---
showLink: "https://www.youtube.com/watch?v=9P94bG6gi-I"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Quarterly Report Q2 ‘24 | Incubator WEEKLY"
publishDate: "2024-07-15"
coverImage: "https://i.ytimg.com/vi/9P94bG6gi-I/maxresdefault.jpg"
---

## Episode Description

The Dash Incubator team provides quarterly updates on their projects and discusses plans for the upcoming quarter, highlighting the imminent Dash Platform mainnet launch.

## Episode Summary

This episode features quarterly updates from the Dash Incubator team, including Mikhail, Jojobyte, and Rion, with Anthony participating. They discuss progress on projects such as Platform Explorer, DashMate, wallet development, and PrivateSend SDK. The team emphasizes preparations for Dash Platform's mainnet launch and its implications for their work. They also cover developer relations efforts, upcoming blockchain meetups, and potential improvements to the Dash JavaScript SDK. The discussion underscores the team's focus on readying for Dash Platform's release and expanding the Dash developer ecosystem.

## Chapters

00:00 - Introduction and Team Updates

The episode opens with the team introducing themselves and outlining the structure of the call. Rion explains that they will go through each team member's proposals and accomplishments from the previous quarter. The discussion clarifies the Incubator's funding structure, emphasizing that team members are paid for completed tasks rather than calendar time. This introduction sets the context for the detailed updates to follow and provides insight into the Incubator's operational model.

02:44 - Mikhail's Update on Platform Explorer and DashMate

Mikhail provides a comprehensive update on his work, primarily focusing on the Platform Explorer. He discusses significant improvements made to both the backend and frontend, including a major redesign of the homepage. Mikhail introduces his expanded team, which now includes frontend and backend developers, as well as a UX specialist. He details new features such as the network status block, trending lists for platform entities, and plans for separate Platform Explorer instances for different networks. Mikhail also touches on updates to DashMate, including new features to help with the upcoming Dash Platform mainnet release.

20:54 - Jojobyte's Update on Wallet Development and PrivateSend SDK

Jojobyte discusses his team's progress on various projects, including work on the Dash RPCJS and its integration into Dash Join. He explains that personal commitments have slowed some progress but highlights the near completion of library work for Dash Join. Jojobyte outlines plans for the coming quarter, including finishing stage two of the wallet development, implementing third-party wallet integrations, and potentially exploring Dash Platform development once it reaches mainnet. The discussion also touches on the transition of some projects from Rion's budget to Jojobyte's, reflecting the evolving roles within the Incubator.

33:37 - Rion's Update on Developer Relations and Future Plans

Rion provides an overview of his work in the previous quarter, including funding for various projects such as the PrivateSend SDK, Incubator updates, and web framework integrations. He discusses his focus on developer relations, including attending a conference in Utah and plans for future blockchain meetups. Rion outlines his strategy for introducing more developers to Dash Platform, emphasizing the need to address current SDK issues before expanding outreach. He also mentions plans to investigate and potentially improve the JavaScript SDK for Dash Platform, considering different approaches to enhance performance and usability. Rion highlights the upcoming Permissionless conference in Salt Lake City as an important opportunity for Dash Platform exposure. He concludes by discussing the Incubator's budget allocations and reserves for the coming quarter.

47:46 - Q&A and Wrap-up

The team addresses questions from the chat, including updates on WalletConnect integration and clarification on Ash's proposal for DashSpend development. They discuss ongoing communication with WalletConnect developers and the potential for supporting UTXO chains. The chapter concludes with final thoughts from team members, emphasizing their continued commitment to building and expanding the Dash ecosystem, and looking forward to an exciting quarter ahead with the impending Dash Platform mainnet launch.

## Transcript

[00:00] >> Okay. We're live. >> All right. Welcome, everyone. Today we
[00:10] have our incubator quarterly call. Glad to have you guys with us. Mikhail and Jojobyte.
[00:16] >> What's up, guys? >> Hello.
[00:19] >> And Anthony, you're stepping in for Ash, right?
[00:23] >> I am now Ash. >> Just kidding. Yeah, Ash may be joining
[00:29] us later in the call today. Hopefully he'll be able to get here at the end at least. But
[00:35] we will go ahead right now. And anything to say just generally before we get started on
[00:43] each of our individual -- so what we'll go over is we'll go over each of our proposals.
[00:49] We will talk about what we did in the last quarter, what we funded, and what we're planning
[00:55] on working on this coming quarter. And we'll just do that by going through each of our
[01:01] proposals on Dash Central. Yeah. So Michael Cluster says where's Ash? Ash is our other
[01:10] -- he does have a proposal up this quarter. But there may have been some miscommunication
[01:15] about the time. So we'll see if he joins us today. I know it's a little earlier for him.
[01:21] But we'll see if he joins us. And if not, feel free to ask any questions. And we'll
[01:26] also cover his proposal at the very end. If he's here, he can talk about it. If not, we'll
[01:32] just skim through the proposal visually so that everybody can see it on the screen.
[01:37] So with that, Mikhail, we'll go ahead and start with you. And Anthony, because we have
[01:44] just the four of us today, I think we might as well keep you on the screen here. It was
[01:47] going to be crowded with five people on the screen. But I think four is doable with the
[01:51] screen share. It stacks up quite nicely. So let's go ahead and do that. We'll add myself
[01:59] to the screen. And then -- yeah. So this is my proposal. I'm not going to talk about my
[02:05] proposal in detail just yet, other than to say this is kind of a summary of all of our
[02:14] incubator proposals this quarter. So we have me requesting 350 Dash. Ash is requesting
[02:21] 200 Dash. He hasn't requested any funds for about a year. So in fact, I think it was exactly
[02:30] one year ago that he requested his last one. Mikhail, requesting 400 Dash, and Jojobite
[02:36] requesting 400 Dash as well. And then we will just jump straight into your proposal, Mikhail,
[02:44] and talk about that first. >> Yeah, yeah. Sure. Let me show you what
[02:50] we've done and what we are working on. So in the last quarter, most of the budget went
[02:59] to the Platform Explorer. So there was really quite huge work. So the changes both internally,
[03:07] like it's in the backend, in the indexer, and also on the frontend. You can see the
[03:13] new homepage that received a huge redesign. And more UX improvement is coming. We got
[03:26] a slight increase in our team. So we have more people working on the Platform Explorer
[03:31] and possibly other projects. Yeah. Currently, it's me. It's Alexey who is doing the frontend.
[03:41] There is an owl, which is our new backend developer, which works on some backend stuff
[03:49] on the Platform Explorer. We also have now a UX guy. He's working part-time, but he helped
[03:55] us with some interfaces on the Platform Explorer and also other projects. And Dan is also a
[04:06] new frontend developer. We just onboarded him. He's already done some tasks, so they
[04:15] are already in review. So yeah. >> Great. This is awesome to see. Just a side
[04:23] note. I love seeing you build up your team instead of just solo Mikhail doing lots of
[04:30] stuff. One of the main things that I'm hoping is that Dash can scale. We've done pretty
[04:40] well with our own little teams here, but the question is, can we actually get more people
[04:48] involved in Dash? Not just in the incubator and not just as proposal owners, but just
[04:56] are we able to get developers interested in Dash and Dash Platform at a higher scale than
[05:03] we are right now? So that's good to see. >> Yeah, sure, sure. So yeah, now we have pretty
[05:14] decent team. It's two frontend developer, backend developer plus me. So now we can get
[05:24] a little bit more since now. So expect more features to see on the Platform Explorer and
[05:31] other projects. >> I'm just going to open this up real quick
[05:33] since we've got some time, just so that people can see it, what you're referring to, Platform
[05:40] Explorer here. Do you want to talk about this briefly? Because I know this is like your
[05:45] project. >> Yeah, so the homepage of the Platform Explorer
[05:51] previously was, it was kind of simple. It was just showing the latest transactions list
[05:57] and just some network parameters. So right now we redesigned everything. We put some
[06:07] trending lists about some platform entities that people would like to see. We did a status
[06:13] block, which now shows the status of the network and the Platform Explorer, which is different
[06:20] because sometimes network may be up, but Platform Explorer is lagging or have some issues. Or
[06:28] there could be a network is down while Platform Explorer is working. So we can now clearly
[06:33] see what's going on. Yeah, some beautiful stats, like transactions to history and stuff
[06:43] like that. So we actually already have a redesign of the homepage, but that will happen in the
[06:50] next quarter. So it will receive much more beautiful and important information.
[07:01] >> I noticed, I just wanted to talk about, ask about this, this one, not DPNS, but you
[07:07] have this new Platform Explorer contract as well. Do you want to talk a little bit about
[07:12] that? >> Yeah, yeah. That's the feature that recently
[07:17] was added to the Platform Explorer. So basically we made a Platform Explorer data contract
[07:23] that data contract developers can use to make their data more recognizable and they can
[07:32] apply and they can set an alias, a custom name for their data contracts on Platform
[07:39] Explorer. So it works like that. Developer creates a data contract in the network. Then
[07:47] they can submit a document in our Platform Explorer data contract with identifier of
[07:57] your created data contract and its name. And then Platform Explorer will pick it up from
[08:03] the network and will assign a custom name and it will be shown on the website on the
[08:07] front end. >> Got it.
[08:10] >> Yeah. So right now, yeah, for now it's just Platform Explorer and system data contract
[08:17] that are there, but yeah. Yeah, we plan to add some sort of slider or stuff like that
[08:26] and that will show not just six of it, but also some more user-defined data contract
[08:34] names. Yeah. Yeah. We also added the validators page, which shows currently active validators.
[08:45] And we can see also inactive, which was active. Actually, there are also inactive masternodes,
[08:51] but masternodes are working like in quorums. So there are only 25 active nodes in the moment.
[09:00] >> Okay. So inactive doesn't mean like invalid or ban or anything like that. It just means
[09:08] they're not in a quorum. >> Yes. Yeah. Soon we will add a chart for
[09:14] proposed blocks of the validators on the specific validators page that will show where it was
[09:25] proposing blocks, when there was proposing blocks. And chart something like on mining
[09:31] pool websites where you can see that your miner is still working and stuff like that.
[09:37] >> And you also have this API page, which is last page.
[09:40] >> Yeah. Yeah. API. Yeah. Anyone can use this API to build things or query things from Planet
[09:48] One Explorer. This is mostly for the website itself, but maybe someone will find this useful.
[09:54] >> Right. So you build the API and the API mostly or exclusively serves this website
[10:00] itself. But in theory, anybody could use the API and put up their own Explorer, or if they
[10:09] just need a certain part of platform's information, they can get a display that on their page.
[10:16] Got it. All right. Back to the... >> What's next? Yeah. Yeah. We also added
[10:23] a DPNS name support in the indexer. It's not on the front end yet, but soon we should see
[10:30] some features like search by dash names. And you can see in the identity which aliases
[10:39] was assigned to this given identity. Yeah. Stuff like that. Also, there was a lot of
[10:49] work on the infrastructure to keep back-end working as it should. And yeah. On the side
[11:01] of the dash mate, there were no major tasks. There were some bug fixes. And one important
[11:09] feature that was merged is the DKG exchange session check. So when you stop your dash
[11:19] mate node, it checks if there is an upcoming key exchange session of your master node.
[11:28] So it's potentially dangerous to restart your node in this moment. So it checks before you
[11:34] stop your node and warn you about this so you can make it a bit later.
[11:42] Electrum dash is on like -- it's not on hold, but there were no much work on the side of
[11:52] Electrum, but we keep all of this infrastructure. We keep it live. And yeah. Soon there should
[12:02] be Dash Core V21, which I will ensure that it will be working with Electrum.
[12:10] Okay. Yeah. So my plans is like to keep working on
[12:18] the platform explorer. There will also XDify integration. Sorry, I forgot to mention that.
[12:25] Okay. I was going to ask, but -- Yeah. So yeah, XDify is like I believe is our partner.
[12:35] So it's a wallet, non-custodial wallet, and also a decentralized exchange -- oh, no. It's
[12:43] just transferring NFTs. So it's just -- you can buy NFTs with XDify wallet. It is also
[12:50] use this authentication method on the Maya decentralized exchange. So there is an extension.
[13:01] So basically it misses support of the Dash, but they said that if we add support of Dash
[13:07] in their SDK, then they will be able to add support of the Dash in their wallet.
[13:14] So they did give you verbal confirmation? Yeah. That's what they said, that they will
[13:23] add the support of Dash in their wallet. So the SDK is there to support the Dash.
[13:31] And yeah, I contacted with developers of the XDify. So we are in touch. And yeah, I created
[13:38] a pull request. I made all the code, which is now in review from the XDify site. So they're
[13:44] kind of busy. So I hope they will soon should get on it.
[13:52] Yeah. So my plans is to continue working on the Platform Explorer. There are also other
[13:59] projects that I would like to build, but mostly the work of the -- like what I do is Platform
[14:06] Explorer. There should be much more UX improvements. We should add separate Platform Explorer instances
[14:14] for each network. So there will be a network selector with the subdomains where you can
[14:21] choose the network, mainnet, testnet, possibly some devnets.
[14:26] That would be very helpful. I think a lot of people probably want to develop locally
[14:32] rather than working with a testnet or just developing on mainnet for a variety of reasons.
[14:39] So that would be helpful.
[14:41] Sure, sure. Yeah. Also, the Dash Platform should come with the NFT support. So we would
[14:49] like to build something like an NFT collection page where you can see all collectibles on
[14:54] the Dash Platform, which users submitted. Not sure how it works exactly yet, but we
[15:04] will figure this out, like how we will build it and how the UX will be working on the website.
[15:12] Okay.
[15:13] Also the platform console, GrowDB console, which lets you query the platform state straight
[15:21] from the browser. So there is a GrowDB with its own query syntax. So I think it's a good
[15:30] thing to have, to have this tool instrument that allows you to straight do those queries
[15:37] straight from the console and get the data straight from the state. That will be useful
[15:45] for developers which are working on the Dash Platform dApps.
[15:49] Yeah.
[15:50] Yeah, yeah. So there should be some useful DashMate features soon. We're already in touch
[16:01] with the platform team. There are some tasks that we want to do before the mainnet release
[16:08] to give people. So some things like, for example, DashMate Doctor, which tests your configuration,
[16:17] your, like, so in case of issues, you can generate the archive with, with all logs,
[16:29] you know, all of your stages, all of the system information that people could share with the
[16:35] team in case of some chain halt or some issues. Yeah. Yeah. So basically we're preparing for
[16:45] production of the Dash Platform. So yeah, we're working.
[16:52] Yeah. Release is scheduled for two weeks from today. So that's when the binaries get released
[16:59] anyway, but it won't be, won't be on mainnet for several weeks. I'm guessing after that,
[17:05] maybe even more than a month. But I also heard from Sam, BCG CTO, that they're also committing
[17:17] to never wiping testnet from its data as well. So, and I think that I don't remember the
[17:25] date on that, but I think it's coming up close like this week or maybe next week where they'll
[17:30] do a final wipe of the testnet platform data. As far as I know, core has never gone down
[17:37] on testnet. Core has remained up the whole time that testnet has been up, but platform
[17:43] gets wiped out and restarted, has been several times and they've committed to doing one more
[17:51] wipe and then not doing that anymore. So that's actually really good for incubators so that
[17:58] we can maintain continuity with our data so that developers can continue to have reliable
[18:05] data going forward. And obviously we need that on mainnet, so it's good that they're
[18:10] testing that on testnet as well. Yeah.
[18:17] Will DashMate work for production as well as testnet stuff? Or is it already working
[18:25] that way? I haven't used it in a while.
[18:28] It is already working, but there are some specific stuff, like you have to know a version,
[18:35] you have to set some maybe stuff because the team is constantly working, they're upgrading
[18:41] versions. So, but yeah, it's working for testnet and mainnet.
[18:47] Yeah, cool. Did you ever get that blog post written about how to set that up for testnet?
[18:55] Or is that still-
[18:56] I pretty much finished that. I significantly expanded it.
[19:01] Oh, and that was Anthony talking just now, because his icon doesn't like flash and whatnot,
[19:06] like Jojobites does.
[19:07] Yeah, no, I'm about to publish that actually. It's a huge introduction to DashMate that
[19:14] kind of builds on the initial gist.
[19:16] Okay, so you took Mikhail's gist that we covered a week or two ago, and you just went ahead
[19:23] and did your updated blog post on your site, Anthony. Mikhail, go ahead. You were going
[19:30] to do a Medium post, I believe, with that, right?
[19:34] Yeah, yeah. It's already in draft. I started it, but haven't finished it yet. So it's about
[19:39] the local DashMate development quickstart.
[19:44] So as to be distinguished from testnet, there are the three different options, local, testnet,
[19:52] and mainnet coming up. And right now, all we have is, as far as documentation goes,
[19:58] mainnet as far as- well, no, testnet. But yeah, all three should be supported soon and
[20:06] documented.
[20:07] Yeah, so-
[20:08] Go ahead.
[20:09] Yeah, yeah. So, yeah, I will finish the local stuff and then I want to go to the testnet
[20:14] as well, testnet out from DashMate.
[20:18] And I'm personally hoping that DCG can get that documentation into the docs.dash.org
[20:25] as well, because I think that's important for discovery for people that don't know incubator
[20:31] documentation sites. All right, so anything else to say on your side of things, Mikhail?
[20:38] Thanks for that update from the quarter. It looks like a great quarter that you had.
[20:44] Well, I don't know, nothing for me. Okay, but no. All right, Jojobite, would you like
[20:54] to go next or would you like me to go next? Any preference there?
[20:58] I'm fine with either. Up to you.
[21:00] All right, we'll switch over to you then.
[21:04] All righty. So this last quarter has been not as great as Mikhail's for AJ and I. We've
[21:13] had some personal stuff come up, but AJ was able to, so CoolAJ86, I'll say his full username
[21:20] for people who might wonder, CoolAJ86 was able to get to a bunch of the Dash RPCJS stuff
[21:30] and that is used in Dash Join. So I actually have that little summary of Q2 accomplishments.
[21:37] I know AJ has some more stuff that I have left out, but claims will likely be made today
[21:43] and get a few more things pushed. So we'll have a lot of the work on Dash Join for the
[21:51] library side of things done probably later today as far as I'm aware. And sorry, is my
[22:01] mic all right? It keeps turning itself down and I don't know what the audio is like.
[22:07] Yeah, it sounds good. I just wanted to also say while you're maybe thinking about your
[22:11] mic stuff, I also wanted to say that you and AJ, you guys are not full time by any means
[22:21] in Dash. So last quarter, just as a quick update, I'll talk about this a little bit
[22:27] more in my report, but you became a new incubator strategist this quarter. So welcome, first
[22:35] of all, this is your first quarterly report, I believe. But in addition to that, you guys
[22:43] have your own contracts and other things that you're working on because incubator can't
[22:49] fund you full time. It's not like we can expect you to be able to jump on a dime and turn
[22:55] on a dime and start incubator work. So for anybody who doesn't really know how our process
[23:02] goes, we don't fund people for the calendar time. We fund people for completing tasks.
[23:14] And so even if an incubator strategist didn't do any work, that means that they probably
[23:20] also didn't get any pay. So the fact that you didn't work full time shouldn't be any
[23:26] kind of problem other than it's always nicer to get things done sooner, but you guys have
[23:31] other contracts that you're working on and other life events. So just wanted to mention
[23:36] that as well. So go ahead, Joe, your mic sounds fine to me.
[23:41] Thank you for clarifying that. Yeah. As other projects come up, sometimes we have to prioritize
[23:47] other things other than the Dash work, but we are both trying to get back into the Dash
[23:52] work now. And I know we have a bit of budget. I think a lot of it will be gone after AJ
[24:01] gets paid out for his most recent work. And then there's a little bit of budget left for,
[24:07] well, actually most of my side of the budget for wallet and the third party integrations.
[24:14] I'm not sure I will get to the Dash join stuff before the next stuff is funded, but I think
[24:22] we'll be able to get a lot of the third party wallet integrations implemented over the next
[24:30] week or two here.
[24:32] So that's Maya, that's Dash spend, that's... What's the...
[24:42] I had them all listed in the Q2 proposal, but I removed them for some reason from this
[24:47] one. So let me look real quick.
[24:51] No, the other one is Crowdnode and we've got that from a while ago, it's just UI on top
[24:58] of it. We've also got part of the UI done, but yeah.
[25:04] Yeah. And the other thing that I think still needs a bit of work is the transactions. It's,
[25:12] I think 90% there, but might need a little bit more work on my part. And then neither
[25:20] AJ or I were able to get to the Dash proposal stuff. However, the Dash join stuff has been
[25:27] the main priority for us. And as that is close to library ready, I should be able to implement
[25:34] that hopefully soon here.
[25:37] Yeah. So I saw an update from AJ, he's got it working in the browser, but it's not library-ified,
[25:47] meaning it works, but it's not something that a third party could just pick up and say,
[25:55] here's the CoinJoin library that I can integrate for Dash. That's something that you do want
[26:01] to accomplish at some point this quarter, making that into a library, correct?
[26:11] Yep.
[26:12] And then on the Dash proposal.js side of things, I don't know if you, we were at a meetup together
[26:20] recently and I don't know if you were in the conversation at that time, but we're actually
[26:24] going to be streaming the initial work on that today for the library side of things.
[26:33] So the whole purpose, which I'll talk about in more detail on the stream later today,
[26:39] that's going to be with AJ and also Validark, who we've introduced Dash platform to and
[26:45] Dash in general, and he might be working on this. It might be a very simple thing to do
[26:53] because of some of the Dash RPC updates that you've done. So do you want to talk about
[27:00] that a little bit? Like what is Dash RPC.js and what has AJ been doing and why was that
[27:07] necessary for the Dash Join stuff?
[27:10] So as far as I understand it, the Dash RPC is required to actually trigger a lot of the
[27:16] coin join processes and the mixing of the coins. And so AJ has been figuring out what
[27:25] is needed and what he can do. And I believe he's doing it in a vanilla JavaScript way
[27:34] where there shouldn't be any dependencies I'm checking right now.
[27:38] Well, let's just look at this right now. And I understand that he's been doing most of
[27:46] the work here. And so maybe all of it hasn't been communicated back to you. So I don't
[27:51] want to put you on the spot here, but we'll just kind of go through this real briefly
[27:55] just so people can see what he's been working on, I guess.
[27:59] Yeah. So he's actually worked on this for quite a while and only recently got it to
[28:04] where he's been able to demonstrate it's working. And so he has been able to do a coin
[28:12] join mixing on a reg test environment that he's set up. And he's been able to repeat
[28:20] that several times. And I think there's some screenshots.
[28:25] And also, I think streaming was a big part of his latest work where he's got WebSocket
[28:33] support for all of this. So you don't want to have to keep doing manual updates to naturally
[28:42] coin join is naturally kind of a streaming process. So yeah, I'll go back here for now.
[28:50] But feel free to say anything more about that if you want, or just move on to what you're
[28:57] looking forward to this coming quarter.
[28:59] Yeah. So as far as what we're looking forward to, it sounds like the library side of the
[29:09] Dash proposal stuff will likely be handed off to Validark. I don't know if he's going
[29:16] to be doing the UI or not, but I'm happy to do the UI. But if that's the case, hopefully
[29:23] we'll be able to get to that in the next month or two here.
[29:28] And then wallet UI, we want to wrap that up. I think we want to get stage two done as far
[29:39] as the wallet is. And I think we're about halfway through the planned stage two, if
[29:51] I recall correctly. I'm looking it up here, which transactions view was a big one, but
[29:59] there's several things that will be finished off that have been worked on, but we were
[30:04] working out kinks and stuff. So we want to get through as much of stage two as possible
[30:09] and into stage three. And I know we've also shifted some stuff from stage three. I think
[30:16] originally had the third party integrations and we shifted those into stage two. So we
[30:25] might shift things around a little bit, but we should be able to finish up stage two of
[30:30] wallet and have that completed.
[30:33] If you want to send me a link of what you're looking at, great. If not, we can just go
[30:41] on the verbal there. I hear you clicking around. Yeah. Yeah. I was trying to find it. Hang
[30:48] on. I'll drop it in the chat here. Actually, that might not even be the best link. I think
[30:59] we've got a project that's a better... Actually, yes, this is a better link to look at there.
[31:07] Okay.
[31:08] So welcome to the world of project management, Jojo Vite. I know you're primarily a developer,
[31:15] but as we've seen from Mikhail, some of the best project managers are good developers
[31:21] as well. So I'm going to bring this link up that you sent me. And I will also say project
[31:32] managing AJ isn't the easiest thing in the world. All right. So do you want to talk about
[31:39] this a little bit?
[31:40] Yeah. So I had gone through and prioritized a lot of what needs to be done for the roadmap.
[31:46] And I believe everything in here right now is stage two. Some of these are... There's
[31:54] not great indication on the level or amount of work each of these are, but I'd say several
[32:01] of them are bigger. They're going to take several days worth of work and others are
[32:10] probably an hour or two of work. And so I do think we'll be able to finish up a lot
[32:16] of what's in here and then hopefully get what's left in the roadmap that is still in the readme
[32:23] transferred over into this list. But you can also click on, I think the status board tab
[32:33] to the left of that one. Yeah. And that is where it currently stands, where it was left
[32:41] off. So transactions view was in progress as I was last working on it and it is really
[32:47] close to being done. So that will be done. And then third-party integrations will be
[32:52] worked on next with those other ones that are in the ready section.
[32:58] Okay.
[32:59] Yep.
[33:00] And then...
[33:01] Can you go over that a little bit?
[33:05] Yeah. And then I'd also like to test out Dash platform, especially if it's getting to mainnet.
[33:13] So I do have a few ideas I'd like to try. I'll probably map them out a bit more before
[33:20] I do any work, but I figured I'd wait till platform is on mainnet and then invest a little
[33:28] bit of the funds in building some stuff to test out platform and contribute to that side
[33:36] of Dash.
[33:37] Okay. All right. I think that's pretty good then. Let's wait for Ash to see. We'll see
[33:45] if he shows up at the end here. I'll jump over, jump back to my proposal. I talk a little
[33:53] bit about you becoming strategist and what that means far as budgets go. This is today's
[34:02] show and this is just a brief look at my personal strategy budget. Now that we're separate,
[34:13] this is just me personally, not the whole incubator. And as you can see, my reserves
[34:20] are kind of going downhill. And as far as my projection goes, I made my request as low
[34:26] as I could sustain with targeting at the end of the quarter, probably be down to 268 Dash.
[34:38] The last thing that I want is for DCG to have to cut back on their staff at this point where
[34:46] we're finally launching Dash platform on domain net. So I wanted to be sensitive of that with
[34:54] my request. These are the projects that I funded last quarter, Q2, and I'll just talk
[35:04] briefly about each of them. So the PrivateSend SDK, that in the last quarter was funded primarily
[35:12] by me, my budget. And now moving forward, that will be in your budget, Jojobite. Incubator
[35:20] updates, that's kind of like Incubator Weekly, that's what Incubator Weekly is mostly. And
[35:29] Payment Tools is another one of those projects that is mostly done, but every now and then
[35:34] we have to do some updates on our libraries. And that's what this last quarter was as well.
[35:42] That's another one of those things that would probably primarily land in your budget, Jojobite,
[35:48] going forward, as well as the Modern Vanilla Web Wallet. So a lot of this stuff that we
[35:55] worked together on under my budget will be moving to you, and we'll see how well you
[36:02] can do with that with 400 Dash per month, but, you know, we'll see. And let's see, probably
[36:12] the main focus for me this last quarter was this, what we called web framework integrations.
[36:18] That's how the project started, but it ended up being mostly like tutorial walkthroughs.
[36:24] So if you've seen, if anybody's seen our video series on the Dash platform walkthroughs,
[36:31] that's what this is. And then I'll talk a little bit about that more down further.
[36:42] This Merchant Loyalty Credit System, this was work that Jan was doing. And we've talked
[36:50] about that in previous Incubator Weeklys. We had him on the show a couple times. I will
[36:57] probably not be funding this one much more, not because it's not a good project. It is
[37:02] a good project, but it's just, you know, with the budget being tight, that's something that
[37:07] I feel like we've gotten to a point with where he can maybe take that on his own and continue
[37:14] to work on that, which I believe he has plans for, but I'm not sure. So, you know, that's
[37:21] what the Incubator is. We incubate some projects and some of them will go on and some of them
[37:27] will die. But I hope that keeps going because it does have a lot of potential, I think,
[37:33] and it is potentially a good Dash platform project. Although it does do a lot of its
[37:40] work with by sending off return messages on the main net. So it's not like it needs Dash
[37:47] platform, but some of the metadata could be better done on platform. Dash developer relations.
[37:57] This is something that I started last quarter is basically, I'll actually just go down a
[38:04] little further so people can read these descriptions. They're a little bit better than what I'm
[38:11] talking about right now on the screen. But yeah, basically, I attended a conference here
[38:16] in Utah. All the, there's a lot of, there's a very big developer community here in Utah.
[38:22] You know this Jojobite, you're in Utah as well. So I would like to start attending some
[38:32] of the bigger conferences that are right here in Utah where I don't have to do travel expenses
[38:38] and you get pretty good bang for your buck. And one of those developer conferences that
[38:41] came to Utah Park City, Utah, I attended and was able to meet some very influential people
[38:48] in the developer community. And I won't name any names until I actually do some more work
[38:53] with them. But that was good to just kind of rub shoulders with developers, talk about
[38:59] Dash, talk about Dash platform. And hopefully this quarter we can do some more of that and
[39:07] reaching, continue to reach out to web developers, which is primarily, as far as I can, as far
[39:14] as I'm concerned, what Dash platform is created for to facilitate web developers to be able
[39:20] to make dApps, like decentralized applications, very easily using a JavaScript SDK. So let's
[39:32] do some of that. And in this coming quarter, what I'm planning to do is continuing work
[39:39] with developers, doing these platform walkthroughs, testing, testing for documentation, developer
[39:49] experience, performance, what we found out from the last 10. I'll open, let's see, did
[39:55] I have a link to this series on the, yeah, the walkthroughs, just open that up real quick
[40:04] so that people can see who we've been working with. So we did one, two, sometimes it took
[40:12] more than one stream to get through all of our, get through the tutorial, three, four,
[40:19] five, six, seven, eight. And we also have a ninth one that's not on this playlist. And
[40:26] then a 10th one that's scheduled for later today. Anthony, are you still, have you fallen
[40:32] asleep or are you still with us here?
[40:33] I'm here. I'll update the playlist right now.
[40:35] Oh no. I was just going to confirm with you, do we have, when is our 10th platform walkthrough
[40:41] scheduled for?
[40:43] That's today at, in two hours after this basically.
[40:47] Okay. So yeah, we'll, we'll have our 10th developer walkthrough on that after that.
[40:57] And so I'm going to, we're, we probably won't reach out to, well, maybe we'll do 10 more
[41:06] is what I'm thinking, but it, it would probably be mostly yeah. Like I don't want to, I don't
[41:15] want to introduce more people to Dash platform at this point until we have figured out what
[41:23] the issue with our SDK is and what, and if we can potentially fix that. So that's, that
[41:30] goes down to this. There's another item here that I wanted to talk about that. Investigate
[41:35] platform JS SDK issues with the solution, potential solutions as well.
[41:43] In the series, we noticed that there are some parts of platform that some certain calls
[41:52] that take a long time. So we want to investigate that a little bit more. And that's one of
[41:56] the reasons why I'm bringing in valid arc. He's somebody that I, we may task to do this
[42:04] with depending on which route we go. So there's, there's two main solutions to that. I won't
[42:12] go to get into the details because we're already getting long here, but the SDK that DCG is
[42:22] focusing on is the rust SDK. And we could potentially do a wrapper over that to be used
[42:30] in a JavaScript and JavaScript settings, but that has its pros and cons, or we could just
[42:35] try to add platform support to our existing incubator libraries. So those two major approaches,
[42:43] well, there is a third approach, which is basically trying to troubleshoot and fix what's
[42:49] in the existing JavaScript SDK, which is written in JavaScript. So those, those are the three
[42:55] main options. So we need to kind of get the pros and cons of each of those. And we haven't,
[43:00] we haven't dived into that yet, but we, that is something I plan on doing before I open
[43:06] it up to more people because the existing people that we've that we've introduced dash
[43:14] platform to, and that's always come with the caveat that, Hey, this is test net, this is
[43:19] kind of alpha software. And, you know, they're there, but they've been forgiving in that
[43:24] sense. And, you know, for web three, it's actually, it hasn't been too bad considering
[43:30] some of the other alternatives that people have to, you know, other jump hoops that people
[43:35] have to jump through to, to, to build like say Ethereum apps, you know, it's, it's difficult
[43:39] all the way around. We're trying to make it as simple as developing a traditional app
[43:45] and bringing in a different SDK. And that's been the goal. So hopefully we can, we can
[43:50] track that down. The other thing is I've been putting this off for a long time. I became
[43:57] the blockchain Utah meetup organizer a few months ago, and I've been meaning to do some
[44:03] meetups, but it just hasn't been the right time. And I think this quarter for sure is
[44:10] the right time to start doing some of those. Now that we have a release date for dash platform,
[44:17] I would like to, it's a, it's not a dash specific meetup. I do organize the dash specific meetup
[44:22] as well. And I'll invite everybody to that as well. But this one is more general. And
[44:27] so we'd probably start with Bitcoin and eventually cover Bitcoin and Ethereum, but then also
[44:34] eventually cover cross platform or cross chain exchanges like Maya that would introduce dash
[44:42] and then finish up the series with dash or something like that. So this isn't something
[44:49] that people want to just go and talk about dash only for, so it's important that, um,
[44:57] that we prepare people specifically for, you know, it's not just, it's all about blockchain
[45:03] and not just dash. So there would probably be like three or four, um, meetups in that
[45:09] series where we'd go through the different types of blockchains and then we would end
[45:13] it with like, okay, actually dash has quite a bit of all of these things. It has a proof
[45:19] of work chain. It has a proof of stake chain. It has a dash. It can be, um, natively swapped
[45:26] between Bitcoin and Ethereum using Maya, that kind of stuff. So I think now definitely is
[45:31] the right time to do that. Um, and then, yeah, it's, I've been, we've been talking with 88
[45:37] guys as well just recently and they're, they're ready to get started as well. So that's, uh,
[45:44] yeah, that's what my quarter is looking like. Um, I also, uh, I forgot to put this in the
[45:49] proposal, but, um, wanted to mention this at least permissionless, uh, blockchain, 9.4
[46:01] is 88. I, the insurance guys in Brazil or something was that or something like that,
[46:08] right? Yes. Uh, so they have an insurance product that they want to bring on chain and
[46:13] use dash platform for that. Um, cool. There is a very, very prominent, um, meet, uh, not
[46:23] meet up, um, conference coming up called permissionless. This is put on by the bankless guys and the
[46:30] block works guys, uh, together, or at least block permissionless two was, and this, this
[46:36] year they're coming to Salt Lake city. So I definitely want to attend this. I think
[46:41] it will be the perfect timing, October 9th through 11th. Um, it will be the perfect timing
[46:45] for, uh, dash platform. And, uh, yeah, there's going to be a lot of people here with lots
[46:54] of money, uh, to say the least, and lots of influence in the, in the cryptos, uh, scene.
[47:01] So yeah, I want to attend that. So that's another thing that I plan to do this quarter
[47:06] as well. Let's see, where are we? Did we ever get ash coming in? Nope, no ash. Um, we've
[47:14] got McHale's done. Um, anything, this is just a brief overview summary of our, um, of our
[47:24] budgets. So the three 50, 200, 400 and 400 requests that we have for each of our strategists
[47:32] here, this is our reserves. This is how much we intend to, um, to spend this quarter. And
[47:38] so, uh, that calculates out to these buffers. So if we're continuing to get, if we continue
[47:46] to get funding, uh, each of the proposals passed, then these will be our, um, our months
[47:52] of, uh, runway. And for each, for each month, this would be the runway if we didn't have
[47:59] funding. So we're all basically teetering on the edge of, um, zero, uh, as I've already
[48:08] talked about, that's it. Uh, that's it for me. Uh, let's see. Anybody else have anything
[48:15] to add there before we wrap up? Let's, uh, did you address the questions in the chat
[48:21] or two things? I haven't been seeing them, so let's, let's bring them up. Let's see.
[48:27] I'm a little behind, but was there any update on WalletConnect? Um, WalletConnect, I think
[48:32] that was you, Mikhail. Um, is that right? Um, I think it's related to xDefi, um, because,
[48:41] or no, it's not related to xDefi. I think, I think it's about, uh, Ash's project, uh,
[48:48] which is the wallet extension, which he put in his proposal. I don't think that that's,
[48:56] those are, those are different. So WalletConnect is, is a, I don't know if they call it.
[49:03] Ah, yeah, yeah. So basically, yeah, I remember this. Uh, sure. We got with the developers
[49:09] of the WalletConnect, but, um, but yeah, that's something that no one really did before. And,
[49:19] um, well, it's kind of difficult because I personally haven't used WalletConnect personally.
[49:26] Uh, I have like a review, like how it's working. Um, yeah. So we got with the developers, they
[49:36] said like, it should be possible, but nobody exactly knows where we should put the implementation
[49:44] and how to make this done. Yeah. So yeah, I was just reviewing my last communications
[49:51] with the WalletConnect guys and, um, they were, they were moving into, so as mentioned
[50:00] above, took his first stab at the address profile for the, there, there was some new
[50:06] version that they were, that they were trying to get out before they had any bandwidth to
[50:12] do any kind of third party help. Um, and, uh, this was, this was, um, this last update
[50:20] was from June. No, how are these? Let's see. I got to figure out what address format this
[50:30] is using. Yeah. June, June. So I'll, I'll reach back to these guys. Um, yeah. So basically
[50:40] the UTXO chains, the support of UTXO chains in the WalletConnect, that's something that
[50:45] the people really would like to see, but, uh, that's something that must be done. And
[50:51] okay. Um, well, because, uh, the digital cash network, which is Joelle, uh, asked this question,
[50:58] I just, um, bumped up our discord conversation to see if there's any traction. Yeah, there
[51:04] is, there is actually a Telegram group where, Oh, okay. Yeah. I think people, some people
[51:09] have moved to Telegram as well. So we'll look into that. Um, thanks for the reminder. Um,
[51:14] and then the other one, the other question, you want to bring that up? Uh, are the funds
[51:21] for Ash's proposal going towards the continuing development of Dashband? Let's look at Ash's
[51:25] proposal. Cause I don't think we've done that yet. Uh, he's not here, but we do have his
[51:30] proposal. So let's, let's bring it up. Okay. Wait a minute. Wait a minute. Wait a minute.
[51:46] Wait a minute. This is 23. Sorry. Sorry, everybody. This is, uh, I mentioned this, but he hasn't
[51:53] requested funds since Q3 of 2023 and they had the wrong link up. So here's the next,
[51:59] here's the, uh, active proposal, two projects, dash pay extension wallet, and the explore
[52:13] dash web plus mobile and explore dash web. I'm pretty sure this is CTX, uh, spend dash
[52:27] spend as well. So I'll just, I'll just pan through the proposal texts and we're not going
[52:32] to read the whole thing, but here is the proposal itself. So did anybody see, let's just, uh,
[52:47] let's just look at this. Uh, the goal, the, the explore dash web plus mobile. The goal
[52:55] of this is to take the mobile wallet, explore dash experience, uh, to discover dash merchants
[53:03] direct accepting and gift cards. So yes, that is dash spend the part of the trouble with
[53:09] all of this is that the names keep getting changed. So, um, but I believe when he says
[53:16] directly accepting merchants and gift card merchants, I'm sure that that's going to include
[53:21] the dash spend merchants that he's working on as well and ATMs to be available on the
[53:26] web and extended with some more functionality around third-party gift card providers, CTX,
[53:31] which is dash spend, uh, bit refill coins, B coin cards, or else want to extend this
[53:38] directory to utilize platform as a source of truth for multiple front ends deployments
[53:43] wherever the state is useful. Okay. So, um, I'm getting replies from the, from the wallet
[53:53] connect people. Um, so we'll, we'll talk about that in a different show, I guess, but it
[53:59] looks like they're, they're on it. Okay. I'll go ahead and remove the screen share. Now.
[54:10] Okay. Anything, any, uh, parting words, Mikhail or Jojo bites. It looks like we didn't get
[54:15] ash in here at the end of the day, but, um, yeah, anything else to say? Uh, well, I don't
[54:24] know. We just continue, uh, continue building, continue doing stuff in the incubator. Um,
[54:32] from my side, I'm still growing my team, growing amount of projects that we have. So let's
[54:40] keep it going. Yeah, it's a, it's going to be a very exciting quarter. So, um, yeah,
[54:48] we have that to look forward to and, um, a lot of potential here. So looking forward
[54:54] to all of that, anybody, uh, yeah. So I think we've answered all the questions that came
[54:59] through the chat. Uh, so with that, we have a couple different streams that we're going
[55:05] to be, uh, streaming on this channel later today. So tune in for that. And, uh, aside
[55:11] from that, we'll say, see you next time. See you.
