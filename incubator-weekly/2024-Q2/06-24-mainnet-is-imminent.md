---
showLink: "https://www.youtube.com/watch?v=9_eHpNmmPbs"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Mainnet is Imminent | Incubator WEEKLY"
publishDate: "2024-06-24"
coverImage: "https://i.ytimg.com/vi/9_eHpNmmPbs/sddefault.jpg?v=6678ba47"
---

## Episode Description

Dash platform's mainnet release is scheduled for July 29th, with developers discussing the upcoming features, challenges, and plans for testing and adoption.

## Episode Summary

This episode discusses the upcoming mainnet release of Dash platform, scheduled for July 29th. Rion and Anthony review a recent blog post detailing the features and priorities for the release, including decentralized identities, data contracts, and a fee system. They emphasize that this should be seen as a "mainnet beta" with potential for chain halts and limited initial functionality like no withdrawals. The discussion covers the need for careful testing, documentation improvements, and real-world use cases to ensure stability and usability. Rion and Anthony also touch on the Dash Incubator's role in testing and developing practical applications on the platform post-launch.

## Chapters

00:00 - Introduction and Context

Rion and Anthony introduce the topic of Dash platform's imminent mainnet release, discussing the recent governance proposal that led to this decision and the general sentiment among the Dash community.

05:54 - Review of Mainnet Release Blog Post

A detailed review of the official blog post announcing the mainnet release, covering the release date, features to be included, and the rationale behind calling it a "mainnet beta".

18:42 - Technical Features and Capabilities

Rion and Anthony dive into the more technical aspects of the release, discussing features like Byzantine fault-tolerant consensus, threshold cryptography, and the decentralized API with its various queries.

42:46 - Post-Release Priorities and Incubator's Role

Discussion shifts to the priorities after the mainnet release, including ensuring network stability and enabling withdrawals. Rion and Anthony also explore the Dash Incubator's role in testing and developing real-world applications on the platform.

50:58 - Conclusion and Future Plans

The episode concludes with Rion and Anthony summarizing the importance of the upcoming release and outlining plans for future streams and development efforts.

## Transcript

[00:00] Alright, we're alive with a very exciting mainnet is imminent stream.
[00:09] Yes, I don't know about imminent like it's maybe a little bit of a what's that term?
[00:19] When you when you make phrases to get people to click click baby, it's a little bit of
[00:23] I mean, I would say it's I would say it's imminent me it's like a month away.
[00:26] That's like, it's been there for like five years.
[00:30] It's imminent.
[00:31] Yeah.
[00:32] It is scheduled.
[00:33] And that's the most important part.
[00:35] I think it is scheduled.
[00:37] That's what we're going to talk about today.
[00:39] We're going to go into the the blog posts that talks about this.
[00:42] And then we're also going to look at another blog post regarding testing.
[00:49] And I want to just have a kind of an exploratory session with you, Anthony, I will somewhat
[00:55] I'll guide you through what I'd like to cover.
[00:59] And as a lot of our streams go, we're just going to kind of figure a few things out as
[01:05] we go.
[01:06] I want to because I always like to test the documentation, right?
[01:11] And granted, the documentation is not in a state that is completely reliable, but some
[01:18] things are and some things are we'll go into it.
[01:21] Let's go ahead and Anthony, bring up your screen share and then get right into the blog
[01:26] posts.
[01:27] And that'll make a little bit and also, I don't think this is going to finish.
[01:33] No, it's not.
[01:35] It's not going to.
[01:36] But we'll it won't finish but we'll get started with it.
[01:42] Okay.
[01:43] So he's just or slash blog, right?
[01:46] Yep.
[01:47] Yep.
[01:48] So we're at dash.org/blog.
[01:49] I like this cover image you got.
[01:55] Nice.
[01:56] Yeah, I don't know who made that.
[01:59] But AI probably.
[02:00] Yeah.
[02:01] AI for sure.
[02:02] But who prompted it?
[02:03] Who knows?
[02:04] Maybe.
[02:05] Maybe it was Sam Quantum Explorer.
[02:07] So the high level overview is that we had a proposal.
[02:12] We're going to read through this blog, just word for word.
[02:14] Actually, that's probably the best way to go go with this.
[02:18] So Evo accelerated release is the title.
[02:22] The Dash Network participated over the last two weeks in a wonderful example of what makes
[02:26] us great.
[02:27] Masternodes collectively voted on whether we should have an accelerated release.
[02:31] This poll was aimed to understand the wishes of the network.
[02:34] We had multiple people advocate for releasing for releasing as soon as possible, but also
[02:39] some others on the other side expressed how they wanted to release the release to go more
[02:44] smoothly.
[02:45] So my own perspective on this is, you know, we there were some people that the when Evo
[02:54] thing has been a meme in Dash for a long time.
[02:57] So actually, funny story about that.
[02:59] When I first started streaming last summer in 2013, I think the very, very first comment
[03:06] someone came in as I was streaming was like, "When Evo?"
[03:09] I'm like, "When?"
[03:10] I don't even know what Evo is.
[03:13] On one of your streams?
[03:15] Yeah.
[03:16] Huh.
[03:17] Probably a different Evo, I'm guessing.
[03:18] No, no, no.
[03:19] It was, it was just the, it was when I was the first time I was going to the Dash platform
[03:23] docs.
[03:24] Oh, okay.
[03:25] Gotcha.
[03:26] Yeah, yeah, yeah.
[03:27] So it wasn't one of your just JavaScript.
[03:28] No, my first Dash stream last year.
[03:31] Yeah.
[03:32] So yeah, so I was one of the ones that was in support of the proposal to get a scheduled
[03:39] release.
[03:40] I didn't even really care when it was, but I, because Sam came out and said, we're at
[03:46] a point I'm surprised they didn't link to the proposal.
[03:50] Let's go to that real quick and just so we can get it on screen, go to open a new tab
[03:56] and go to dashcentral.org and maybe they did link to it and I just didn't see it, but scroll
[04:08] up and to the left, go to click budget on the top left and then the Evo accelerated
[04:15] release schedule.
[04:16] So if, if you saw there was some, a yellow bar instead of a green bar and it shows here
[04:23] that it wasn't, it wasn't, it didn't pass by the typical standard that we usually have.
[04:30] This is what's called a governance proposal.
[04:33] It's not a proposal asking for funds.
[04:35] It's a proposal asking for an opinion and anybody can release, submit one of these and
[04:44] you typically just ask for one dash in return because one dash is the proposal fee.
[04:49] And let's, it's just a way for masternode owners to be able to vote on something.
[04:54] And in this case it was a question posed by Quantum Explorer, Sam Westrich, the CTO of
[05:01] Dash Core Group.
[05:03] And some people have different opinions about this in terms of like, what should qualify
[05:09] as passing?
[05:10] Should it be passing if it passes the typical criteria of 10% net yes votes of the, of the
[05:18] total enabled masternodes, meaning yes minus no is greater than 10% of the total masternodes.
[05:25] And that's typically what that is definitely what's required for the funding to kick in.
[05:31] But I agree with Sam in the sense that you, if you're asking a question that technically
[05:39] doesn't necessarily need masternode approval, but it's more of a sentiment thing, like I
[05:45] want to know what the network thinks, then I think it's okay to set your own criteria
[05:52] because technically Sam and DCG could release Dash Evolution to mainnet, make, meaning they
[06:01] can make binaries that the network can adopt or not adopt.
[06:06] They can do that without our approval anyway.
[06:08] So it's no worse submitting a government proposal that, go ahead.
[06:14] Yeah.
[06:15] So I would say this is probably not likely, but could there be a situation in which actually
[06:19] they ship it and then no one adopts it?
[06:21] Yes.
[06:22] Yeah.
[06:23] So it's always in the network's hands, whether they adopt anything in Dash.
[06:27] So this is more like, in theory, Sam and DCG can make any software they want.
[06:34] And that's fine.
[06:36] It doesn't mean the network has to adopt it.
[06:39] But this is a step in an even better direction where they're saying, yes, even though we
[06:44] could release to mainnet or release, do a mainnet release, meaning they write the software
[06:51] that can be adopted and put it on dash.org and GitHub and whatnot, and ask the community
[06:58] to adopt it.
[06:59] But they went a step further and said, hey, we actually want to know your opinion on this.
[07:04] And we internally will take that opinion and say, if two thirds of the votes say that we
[07:12] should go ahead and do this, then we will push to do this.
[07:16] And that's what the voting criteria was.
[07:19] So if you scroll down a little bit, that's what Sam's voting criteria was.
[07:22] So just wait, scroll up.
[07:24] Are you talking about right here or?
[07:26] No.
[07:27] So scroll down a little bit until you see the button that says expand the proposal,
[07:33] because it doesn't show all of the proposal, all the details.
[07:37] Just scroll through this slowly so that people can read it if they haven't already looked
[07:40] at this.
[07:41] But in here, he basically says, if we see that two thirds of the nodes, meaning the
[07:46] master nodes and the Evo nodes, vote yes for this, then we will take that as a sentiment
[07:52] signal from the stakeholders that we should go ahead and push this within our internal
[07:58] organization.
[08:00] So that's what they said.
[08:01] So even though technically, by funding standards, it hasn't passed by those criteria, it has
[08:07] passed by the criteria that Sam was requesting and that DCG would follow.
[08:12] So that's and then because that if you then scroll down a little bit further to see Sam's
[08:18] comment, Quantum Explorer is the username here.
[08:22] So as he says, he's acknowledging it does look like we passed by a slim margin.
[08:28] And so they're going to go ahead and and do this.
[08:31] So he says he's going to write a blog post ban.
[08:35] Yeah, so so any like anybody can write comments on this.
[08:39] And it's Dimo is one of the people who's, you know, he has strong opinions about things.
[08:45] And I don't know if this his opinion here, stop the post band master nodes, whether those
[08:51] were counted in the vote or not.
[08:52] But again, I'm just curious, what does that even mean?
[08:55] What is a post band master node?
[08:57] What that means is poses proof of service.
[09:01] And if you proof of service band means if you are not, if your node is not performing
[09:08] the services that the network is expecting, then you will be banned from the network.
[09:14] That's part of the consensus rules in Dash.
[09:18] So if, if you have 1000 Dash in a node, and you have it running, and it's enabled, so
[09:26] the other status is enabled, and that means everything's good, like you're, you're getting
[09:30] a good, you're providing good service.
[09:33] That's the the enabled status.
[09:35] And then if you if the network's asks for your node to participate in a distributed
[09:40] key generation process, for example, and you do not do that, you are unable to participate
[09:47] in that because you're, you're nodes down or whatever, for whatever reason, then the
[09:51] rest of the nodes on the network will say, hey, IP address, blah, blah, blah, blah, blah,
[09:57] is not able to participate in this quorum generation.
[10:01] So let's, let's as a network, give this node a score showing that he is a score in this
[10:09] context is a bad thing.
[10:10] So if the score gets up to a certain point, then you're banned.
[10:14] And then the network gives you a pose band status.
[10:19] So yes, in theory, if, if we were counting band nodes, then then that would be a bad
[10:27] thing.
[10:28] But again, getting back to what I was saying earlier about this is only a sentiment thing.
[10:33] So I don't we don't have to get into the Yeah, I was just I was kind of curious to see what
[10:38] this link was.
[10:39] And it's like, this is like, it looks like a very, very old website.
[10:46] Old looking.
[10:49] So anyway, HP, the big the big takeaway here is that Sam's recognize that this the network
[10:58] has support for just go ahead, going ahead and releasing platform in the state that they
[11:04] can get to in a month.
[11:05] So now let's go back to the blog posts and continue from there.
[11:08] Now that we've got a little bit more context.
[11:12] So if the proposal had passed with a resounding yes, our release date would have been the
[11:16] 19th of July.
[11:19] Not counting abstains, we currently have 68% for this proposal and 32% against, it's about
[11:25] the same for Evo node operators, Evo nodes, again, those are the nodes that instead of
[11:28] having 1000 dash and just running core services, they're the ones that are running 4000 dash
[11:35] and have also platform services.
[11:38] While the reasons for voting yes have been pretty straightforward, we've heard serious
[11:42] reasons for masternodes in the no camp.
[11:44] My perception from this feedback was that the most common reason for people voting no
[11:48] was that they wanted more stable release.
[11:51] Second, many people wanted withdrawals enabled for them from the moment of activation.
[11:57] So withdrawals are saying you, you and I have been doing these tutorials, Anthony, and we've
[12:04] been doing top up proposals where not proposals, top up transactions, yeah, where we take some
[12:14] take some dash on main net or on.
[12:19] We take some dash on the main blockchain, the L1 blockchain, the proof of work, blockchain,
[12:26] and move it over to the platform side, the L2, the proof of stake chain.
[12:31] And that's called topping up or you could say adding or whatever.
[12:38] So withdrawing or depositing, you could use all those terms synonymously.
[12:41] So withdrawing from the platform back to layer one, yeah, yeah, yeah.
[12:47] So that's if you lock up your code, if, if, as we were doing our tutorials, we were saying,
[12:54] let's deposit some credits into the platform side.
[12:57] And if we, even if we wanted to withdraw them back, we couldn't have.
[13:01] Okay.
[13:02] So this is good for me to know, because in that specific function, there had been a confused
[13:08] about how much we should be topping up.
[13:11] And at a certain point when it wasn't working, I just kept adding more zeros to the end.
[13:15] And now if I keep doing that, eventually gets to the point where you're going to be putting
[13:19] too much in if you can't get it back.
[13:21] So that's, that's important to know.
[13:22] Yeah.
[13:23] Yeah.
[13:24] It's like a hotel, like style, you can check in, but you can't check out.
[13:29] So that, and that's an important thing for the network to know is that if we enable this
[13:34] without withdrawals, if we activate this, I should say, if we activate platform, allowing
[13:42] people to deposit funds on the L2 proof of stake chain, they need to know that they can't
[13:48] withdraw yet.
[13:51] And that's just part of the, that's part of the deal here.
[13:55] I'll show you a quick note for myself to make sure I have a note of that.
[14:00] Yep.
[14:01] Okay.
[14:02] Okay.
[14:03] So, um, so second, many people want withdrawals enabled, uh, from the moment of activation.
[14:11] And in the third, and in third, we had people who thought that we should have everything
[14:16] ready in order to have a complete release that would be completely ready for external
[14:21] developers.
[14:22] That we can all use it in 2030.
[14:24] Yeah.
[14:25] And so that's like a big unknown, like the scope can continue as far as our imaginations
[14:30] will let it.
[14:31] So, yeah, I think everybody was, or most people, obviously, uh, the, the slim margin, 68%.
[14:38] They're in the camp of like, let's do this.
[14:40] Let's just do this.
[14:41] We'll have limited features and a little bit, uh, you know, less stability, but it's time.
[14:50] So decision and implementation strategy.
[14:52] This was not so straightforward decision for many people since the vote did pass by the
[14:58] slimmest of margins.
[14:59] We at DCG will respect the wishes of the majority.
[15:01] However, we also see, uh, an activation, which does require two thirds of the network to
[15:07] actually run the new version.
[15:09] So again, even if the proposal passed, you cut the release, you people adopt the release.
[15:15] Uh, it doesn't guarantee that two thirds of the network will actually, uh, adopt the release.
[15:21] So that's still in play.
[15:22] So it's not like DCG is forcing this by any means.
[15:26] Uh, we have therefore decided to follow the direction of the accelerated release, but
[15:29] to add an additional 10 days of testing by doing so, uh, we should see a healthier release
[15:35] with the straight, with the slight less chance of chain halts.
[15:39] This means that main net release is set to be on Monday, July 29th.
[15:43] So there's the big date.
[15:44] Okay.
[15:45] And then we'll have a big party on that incubator weekly.
[15:47] Yeah.
[15:48] Yeah.
[15:49] So this release should be seen as a main net beta, and this is an important note.
[15:52] This is something that I, uh, support also and would have suggested that we need to control
[16:00] like expectations from just, uh, yeah, from a communication standpoint, like this, people
[16:06] shouldn't expect that everything's going to be hunky Dory and roses and every rainbows.
[16:11] There is still a decent chance that there will be a chain halt.
[16:16] And what that means is that the nodes can't come to consensus for whatever reason.
[16:22] And that's not the end of the world.
[16:24] That doesn't mean funds are lost or anything like that.
[16:26] It just means that the chain has stopped.
[16:29] Now I don't know personally, uh, it stopped producing blocks specifically.
[16:34] Now I don't know if that means that we can't, uh, get data.
[16:39] So I don't know if blocks not being produced is also the same as not being able to query
[16:48] the network.
[16:49] Um, I mean, if you're, if it's only historical blocks, those are never going to change.
[16:53] So you would still be able to use like a platform Explorer, especially if it's like indexed in
[16:57] the database.
[16:58] Yeah.
[16:59] So I think that it would depend on the nature of the halt.
[17:02] If it, if it was halted because all the nodes crashed, for example, then yeah, you wouldn't
[17:07] be able to even query the blockchain.
[17:10] If it was halted because of consensus issues where the nodes are still running, but they
[17:16] are not producing blocks anymore because they can't come, come to, uh, consensus about which
[17:22] is the valid block.
[17:23] That's a different thing.
[17:24] So I don't see this as a big deal.
[17:26] Even if the chain does halt, I, I, I'd rather be moving on to main net and have that risk.
[17:33] Okay.
[17:34] So where was I?
[17:35] Um, release should be seen as a main net beta.
[17:39] We will also be releasing the rust SDK as a beta part to us, the part of that's coming
[17:45] up.
[17:46] Yeah.
[17:47] Yeah.
[17:48] Do you want to, do you want to, uh, read from here on out?
[17:50] Yeah, sure.
[17:51] So it's, um, while the JavaScript SDK does exist, it should be seen as an alpha version.
[17:56] So even more experimental than the rust SDK, which is kind of what you've been talking
[18:00] about on some of our recent streams that a lot of the energy has kind of gone into the
[18:04] rust SDK.
[18:05] And, um, this is kind of interesting and say that, um, since documentation isn't finished,
[18:11] we should be very cautious when trying to get external developers at this stage as we
[18:15] can only make a first impression once.
[18:18] So I guess what we're doing is we're trying to find people who can get us a first impression
[18:25] that may or may not have actually been using it anyway.
[18:29] So it's probably not the end of the world if they have necessarily a bad experience.
[18:34] But um, I do think that's kind of important for us to think about as we're bringing in
[18:37] developers to go through my tutorial.
[18:40] Yep.
[18:41] Yeah.
[18:42] And I've, I've thought about that as well.
[18:43] I I've been worried for a while now, uh, of introducing something and giving a bad first
[18:49] impression, but that's, that's why I, and I think you to some degree.
[18:55] So both of us, these are developers that we know these people, we have good relationships
[19:00] with these people and these aren't people that will just trash us, you know, because
[19:07] they had some, some errors using an SDK.
[19:12] These are developers who we, the only reason they came on the stream was because we have
[19:17] good relationships with them in the first place.
[19:19] Uh, yeah.
[19:20] And, um, and I should say we did get, um, very good comment here yesterday.
[19:26] Someone was thanking us for doing these streams.
[19:29] So I think, um, people have been appreciating them.
[19:32] Oh, good call.
[19:33] I haven't, I hadn't seen that until just now.
[19:36] So thanks for mentioning that.
[19:38] Yeah.
[19:39] Yeah.
[19:40] I think, I think there's a healthy balance where we're bringing in trusted friend developers
[19:45] to help us test our documentation, test the clients, test the network, and all this is,
[19:52] I think, important work.
[19:55] It's also important that we don't take it too far where we're revealing to the entire
[20:01] world, even people that we don't really, you know, know, uh, and don't have the right expectations.
[20:10] That would be a bad thing.
[20:11] So quantum, you know, Sam, he's got a good point here.
[20:13] So I want to continue, um, talking about that or talking.
[20:16] Yeah.
[20:17] And then, um, uh, but yeah, one of the thing is that the saying is this documentation isn't
[20:23] finished.
[20:24] I'm curious what in their mind still needs to be done with the documentation.
[20:29] So obviously like I have my ideas, it's kind of why I wrote the, the tutorial, but that's
[20:34] something that I'm kind of curious, like what do they think still needs to be done with
[20:38] the documentation?
[20:39] Well, a lot of it needs to be cleaned up there.
[20:42] There is a lot of dead documentation that where links are stale or pointing to the wrong
[20:47] repos that have been, um, moved and, or abandoned.
[20:52] Like, uh, there is a lot of that that needs to be cleaned up and reference reference documentation.
[21:00] We haven't looked into that very much, but I don't know if that's complete either, just
[21:06] like a straightforward reference API reference.
[21:09] Um, we've been doing tutorial documentation for the most part, but, um, but I don't know
[21:16] what the state of the reference documentation is by reference that I can help out with is
[21:25] getting the documentation in good shape.
[21:27] Yep.
[21:28] Yeah.
[21:29] And so that, that this, this whole process helps with getting the documentation better
[21:34] because you need both the people who are writing the application level software code to do
[21:42] the documentation, but you also need it from the other perspective of the people that are
[21:45] consuming the documentation.
[21:47] So without some amount of testing, it's hard for, it would be hard for them to really get
[21:55] the documentation nailed down.
[21:56] All right.
[21:57] Um, all right, let's get, it will take a few months to get the SDKs to a level where we'll
[22:03] be comfortable knowing that non-advanced third-party developers can use them with ease as definitely
[22:09] true internally.
[22:10] However, we'll be using the rust SDK on mobile in order to activate dash pay, which enables
[22:16] payments between identities with payment happening on the core chain and where the identities
[22:21] of the sender and receiver are not obvious to other parties.
[22:24] Yeah.
[22:25] Yeah.
[22:26] That's, that's expected, you know, dash dash core groups products are mainly native applications,
[22:34] meaning they've got the desktop, uh, they've got the desktop core wallet, they've got mobile
[22:41] mobile wallets, but they haven't done much with in the web space.
[22:45] And that's, that's something that I feel very strongly about that the dash platform needs
[22:51] to be very web accessible.
[22:53] And I think that they, they agree with that.
[22:55] It's just not their priority because that's because it doesn't, that's not their products.
[23:00] So this is where, you know, I think incubator can, can help out and should help out.
[23:06] I don't know how much we can help out with, you know, the funding that we have, but it's
[23:10] something that we definitely do want to help with.
[23:13] Cool.
[23:14] You want to continue for this part, accelerated release features.
[23:18] Furthermore, we would like to stress that while we were going down the path of an accelerated
[23:22] release, we are still releasing a product that is quite feature rich in this version.
[23:27] Some of the more important features that we are releasing are decentralized identities,
[23:33] creation update, top up credit transfer.
[23:36] So we've, we discussed that a little bit above where, you know, you and I have experienced
[23:42] the, the identity creation, updating, topping up, and we didn't, we haven't done much of
[23:48] credit transfer or at all.
[23:50] I don't think we've done credit transfer.
[23:52] It's always just been one, one person with one wallet.
[23:55] Yeah.
[23:56] Yep.
[23:57] That's when you, you would, you have two users, both on platform and you're, you're transferring
[24:01] credits just analogous to two users on Ella one transferring credits to each other.
[24:08] And we haven't done that yet, but that will, yeah, you'll be able to do that credit transfer.
[24:12] And then, so the next bullet point, data contract support, creation update, historic historical
[24:18] support, various mutability configurations.
[24:21] We've done that document support, document based NFT, basic support.
[24:28] So transferring and selling.
[24:30] So NFTs is one of these things that there's a lot we could probably say about this, but
[24:39] I don't know how much I want to say about this NFTs, non fungible tokens for anybody
[24:44] who doesn't know that's in contrast to fungible tokens.
[24:49] The difference being fungible tokens are like a collection of things that are all supposed
[24:53] to be the same, like units of dash non fungible tokens, a better name, a more accurate name
[25:00] would have been unique assets where there's just one of these things or a specific number
[25:08] of these things.
[25:10] How you get your loopy donut avatar.
[25:15] This is my NFT of choice for the longest time.
[25:18] I used to buy all these and give it to my friends back when I was working at Quicknode.
[25:23] Yeah.
[25:24] And those are, it's mostly like an Ethereum thing or EVM thing, Ethereum virtual machine
[25:30] thing where some people would define NFTs as having both the asset, like a unique asset
[25:40] on a, on chain, but also the ability to transfer that asset.
[25:46] And so when, when we're saying here that document based NFT basic support, transferring is news
[25:55] to me.
[25:56] Like I didn't know that we would have transfer support, but it's, it's not the same NFT that
[26:01] most people would, would consider an NFT, meaning that it has an API that's executed
[26:08] through an Ethereum virtual machine.
[26:12] It does the same thing.
[26:13] Obviously you can transfer an NFT, like the ownership of an NFT from one person to another,
[26:20] and it will be happening in a different manner on the dash blockchain.
[26:25] It won't be doing it through EVM API that is executed on the blockchain.
[26:33] It will be some different mechanism, but I think that's the point being, if I had a wallet,
[26:38] I could buy my 10 donuts and give like five to my friends and then they would have a donut
[26:42] in their wallet.
[26:43] Yes.
[26:44] But it wouldn't follow the same API as an EVM NFT is what I'm saying.
[26:49] Right.
[26:50] So you couldn't expect to just take the contract that you used to make your donut NFTs and
[26:59] transfer it over to Dash.
[27:00] So we would have to make some brand new Dash donuts.
[27:03] Yes.
[27:05] Contested resource masternode vote resolution, contested resource.
[27:11] So I don't know if anybody would know what this means, but because I'm hanging around
[27:16] the forums, I know what this means.
[27:19] Let's use an example.
[27:21] One of the biggest and most important contracts on Dash platform initially is going to be
[27:27] the Dash pay contract.
[27:30] The Dash pay contract is what gives people the ability to register a username.
[27:36] And one of the issues with registering usernames is always the issue of land grabs, where you
[27:46] might have somebody that says, I'm just going to register AJC web dev, even though I'm not
[27:52] AJC web dev, I'm going to register Ryan Gold.
[27:55] I'm going to register Sam, you know, Quantum Explorer.
[27:57] I'm going to register every letter A through Z.
[28:00] I'm going to scrape the Discord.
[28:03] I'm going to get, I'm going to make an array of all the usernames on Discord, and I'm just
[28:08] going to run a script that registers all of them and screw them over for everybody.
[28:12] That is so smart and evil.
[28:15] And that won't cost that much.
[28:16] It wouldn't cost that.
[28:17] Like, let's say the Dash community is a thousand people, so just as a round number, a thousand
[28:25] people times, I don't know how much it's going to cost in the end to register a username,
[28:30] but I'm guessing it's going to be about a dollar, something on that order of magnitude.
[28:34] It's not going to be $10.
[28:35] It's not going to be 10 cents.
[28:37] It's going to be somewhere on the order of magnitude of the dollar, I think.
[28:41] So that'd be like a scalp or a hundred Taylor Swift tickets and sold to everybody.
[28:47] Yeah.
[28:48] I mean, a thousand dollars to screw over something that we've been working on for seven years.
[28:53] That seems like somebody definitely could want to do that, and they could do that.
[28:59] So this contested resource is this process where there's going to be the ability, registering
[29:05] a username on mainnet is going to be a process.
[29:08] In other words, it's not an event.
[29:11] First you'll have to request to register the username, and you're requesting not from a
[29:16] centralized party, but you're requesting from the decentralized network.
[29:21] And there will be a time period where the network will see that somebody has requested
[29:27] to register AJC web dev.
[29:31] And if through some kind of social proof, you, Anthony, say, "Yeah, this was me."
[29:39] And you post that from your Discord account or your Twitter profile, then the network,
[29:46] it's not like the network is just a bunch of robots that have no kind of conscience.
[29:51] They are people running these nodes, and they will be able to vote and say-
[29:56] This is super interesting.
[29:57] Because in my case, I've got the Discord handle, the Twitter, the Twitch, the YouTube.
[30:01] I have AJC web dev registered in seven places, so it would be extremely easy for me to prove
[30:07] that.
[30:08] But for some people, if it's kind of a more obscure thing, and maybe they have a couple
[30:11] different names in a couple of different places, it could be a bit more ambiguous.
[30:15] Well, and just to be clear, this isn't a process that most organizations go through.
[30:27] Most organizations, say there's some startup that has a username system, and they're a
[30:33] centralized company, they're not going to go through this process because they don't
[30:38] care.
[30:39] It's up to the user to be the first on their platform, and AJC web dev, if you really want
[30:45] that, then you're going to go out of your way and make sure that you get that registered
[30:49] username.
[30:50] But Dash is a little bit of a unique case where it's a decentralized organization, and
[30:56] well, maybe centralized organizations do this to some degree, but I'm thinking about something
[31:03] like a Coca-Cola or a Pepsi, right?
[31:07] Coke, it could be any, just think of any big, think about X.
[31:13] Faceless corporation.
[31:16] Some big corporation that may or may not someday, let's get our grandiose vision caps on and
[31:22] just say that even though Dash is not well known right now, at some point, maybe it will
[31:28] be.
[31:29] And we don't want somebody to have been squatting on very important usernames like Donald Trump
[31:36] or something, because Donald Trump, he's not going to care about mainnet release.
[31:42] He doesn't know about this, right?
[31:43] His username is obviously available.
[31:47] So I don't know the details of this contested resource voting process.
[31:56] It's still a work in progress.
[31:58] Well, I guess, no, it's not, because it's on this-
[32:01] It's going to launch, it says so, but we don't need to get into the details, just so people
[32:06] know what it is.
[32:07] It's probably enough.
[32:08] Yeah, that's what it is.
[32:09] So there will be a process.
[32:10] Yeah, let's keep going.
[32:12] Dash platform name serve.
[32:14] I think name service, I guess maybe that's a typo.
[32:19] Yeah, it's a typo.
[32:22] Yeah.
[32:23] DPNS contract.
[32:24] We've done this.
[32:26] Dash pay contract.
[32:27] We've talked about this.
[32:28] Verification of total system balance based on Sumtree technology.
[32:33] This is basically saying we know that the amount of Dash that came in is verified at
[32:41] all times.
[32:42] And there's very, very, very, very small chance that there will be a quote unquote inflation
[32:49] bug where new Dash credits are minted somehow on the Dash L2 chain.
[32:55] And then they attempt to, let's say they mint a million coins on the L2 chain because it's
[33:03] maybe less secure than the L1 chain.
[33:07] And they then try to withdraw a million Dash onto the L1 chain.
[33:12] Well, the Sumtrees is a technology low level developed that says cryptographically we can
[33:19] prove that a million Dash is not supposed to be in the system.
[33:25] So it's not going to have an inflation bug on the L1 system, let alone the L2 system.
[33:33] A fee system with fee refunds when removing data from system.
[33:39] Okay.
[33:40] So that's important to know because I didn't know this.
[33:41] I was wondering about this in one of our previous streams.
[33:45] If you have data, if you register data on the...
[33:52] Can you put your cursor on the item that we're talking about just so I can track the viewers?
[34:00] When you submit data and you pay for that data to be stored on Dash platform, you're
[34:05] paying money.
[34:06] But when you do the opposite transaction and say, "Actually, I was just testing some things.
[34:11] I don't really need all that on there.
[34:13] I'm going to remove that," you get refunded.
[34:16] So according to this bullet point, that's saying that even though withdrawals aren't
[34:21] enabled, in other words, you can't take the Dash on L2 and bring it back to L1, you will
[34:30] still be able to get refunds for Dash that you remove data for.
[34:36] So that's good to know.
[34:37] Reward distribution to EvoNodes, the EvoNodes, it's a paid service.
[34:46] They get part of the newly issued Dash currency that gets created in the mining process.
[34:54] Some of that will be shifted over to EvoNodes now and rewarding them for doing the proof
[35:00] of stake consensus.
[35:07] That distribution comes periodically and that's to be expected.
[35:10] So you will be getting paid as an EvoNode operator in the sense that you'll be accruing
[35:16] a balance that's owed to you.
[35:19] Even though you can't withdraw that balance and move it back to L1, you still will be
[35:23] accruing that from day one.
[35:25] So that's to be expected.
[35:27] Protocol versioning support for hard fork upgrades, state transition execution cryptographic
[35:33] proofs.
[35:38] We talked about that yesterday when we were talking about GroveDB.
[35:43] Platform state with efficient cryptographic proofs for like clients based on GroveDB storage
[35:47] system hierarchical authenticated data structures.
[35:55] We went over a little bit of that when we looked at the GroveDB.
[35:58] All of this stuff Sam could obviously explain better than I can, but he's busy.
[36:03] A scalable Byzantine fault tolerant consensus solution using threshold cryptography and
[36:09] same block execution.
[36:14] So BFT, Byzantine Fault Tolerance Consensus, that's the consensus mechanism of TenderDash
[36:22] in general, or TenderMint in general, the Cosmos based TenderMint consensus algorithm,
[36:29] which we adopted and have modified a little bit.
[36:33] That's pretty standard for most like Bitcoin, you know, was Byzantine Fault Tolerance.
[36:40] Everything has every modern proof of, most I say, most modern proof of stake consensus
[36:48] algorithms are BFT type consensus.
[36:53] Now what it says when it says using threshold cryptography and same block execution, those
[36:58] are some things that are different than most and something that Dash has developed.
[37:04] The threshold cryptography part is saying we are using 1000 Dash or 4000 Dash rather
[37:15] for each of these nodes.
[37:16] And so they're all the same nodes.
[37:19] And there's the technology that we have says that we can have threshold based voting on
[37:27] our nodes because of the cryptography, again, it's above my pay grade.
[37:32] But the idea from the user level is that we can use these nodes to vote and have all sorts
[37:38] of different criteria for the voting.
[37:43] So for example, there are lots of different quorums that get, among the Evo nodes, it
[37:48] gets further subdivided into lots of different quorums that are always continually forming
[37:55] and unforming on the network and rotating.
[37:59] So you might have 300 nodes, or you might have like, let's just say 100 nodes participating
[38:07] in a certain type of quorum that's responsible for verifying that transactions are locked
[38:13] and that 100 of these quorum nodes have seen the transaction and they're coming to a consensus
[38:19] and saying, if 60 out of 100 of these nodes see that this specific transaction has occurred
[38:27] and they all see it, they're going to then create a transaction that says, or a message
[38:34] on the network that says, okay, this transaction is locked.
[38:37] And we saw it in half a second, and it's now considered completely settled, it will not
[38:46] change state.
[38:48] And that's a good feature.
[38:50] And that's enabled by this threshold cryptography.
[38:54] Now the same block execution bit, again, this is all above my detailed pay grade.
[39:02] But the high level on this is that in Cosmos, in the Cosmos world, that's like the Atom
[39:12] token Cosmos blockchain world, they have, to my understanding, the best that they had
[39:21] developed by the time that we had forked at least from them, was next block execution,
[39:29] meaning you have to wait at least one block before anything can be determined, settled.
[39:38] And the folks at DCG, Dash Core Group have developed that further into saying, we can
[39:45] settle these things in the same block that they're seeing.
[39:49] So like the current block, so you don't have to wait for the next block.
[39:52] So it's just a speed issue.
[39:54] We can see these things that are settled very quickly, very, very quickly.
[40:00] Decentralized API with 23 different platform queries.
[40:02] So we won't go into each of these sub-bullets, but getting identity, identity keys, contract
[40:10] keys.
[40:11] Yeah, this is not the stuff that's in the actual tutorial.
[40:14] Yeah.
[40:15] So like, this is, this would be like the API reference that I would be interested if we
[40:19] have this documented anywhere except for right here, but it is, yeah, this, this stuff is
[40:24] documented in the docs.dash.org.
[40:28] Okay.
[40:29] So like one, one that's, that's probably more important for most users, like get getting
[40:33] data contracts, getting, getting documents.
[40:36] If you're building, if you're building just a typical application, the, maybe the only
[40:42] thing that you're, you're interested in is getting documents.
[40:47] Because maybe somebody else has created the, the data contract and so here's like consumer
[40:53] of this.
[40:54] Yeah.
[40:55] So this, the platform docs for that.
[40:57] Yep.
[40:58] DAPI client usage platform, get documents.
[41:02] And so if you just click on platform in the left column, let's just see, see, you have
[41:11] a broad cat.
[41:12] You have like six or seven, but you don't, but yeah, yeah, that's true.
[41:19] So I guess like some like get identity keys and see if we just search that comes up.
[41:30] So, so, okay, here, so they have, so here's the DAPI end point.
[41:34] So this is, this is the GRPC end point.
[41:37] So this probably had, this is the whole list right here.
[41:40] Whereas usage, I'm not sure what the difference is between this and that.
[41:46] I guess the difference is the client versus the GRPC end point.
[41:49] Yep.
[41:50] Yeah.
[41:51] They could be all there for, for all I know.
[41:52] I, I, like I said, I, we haven't really been this low level yet.
[41:56] We've been using the SDK instead of the, the RPC commands.
[42:00] Okay.
[42:01] So keep scrolling down, we'll, we'll skip through this.
[42:07] These are all of these things, 11, 11 helper queries to get core chain based information.
[42:13] So again, these, these are all going to be available.
[42:17] I'm guessing first in the rust SDK.
[42:21] And the idea with the SDKs is that it will give you the, the opportunity to the ability
[42:27] to query data from L1 and L2, the core blockchain and the platform blockchain.
[42:36] So it is a nice handy feature to be able to, to get data from, from both blockchains in
[42:43] the dash ecosystem.
[42:46] So keep scrolling down.
[42:47] So that's what that's saying.
[42:49] Post prior post post release priorities.
[42:52] The immediate goal after we'll release will be to make sure that the network is stable.
[42:57] Then it will be to get DPNS dash platform naming service and dash pay activated.
[43:06] Dash pay is like a super, like a built on top of DPNS.
[43:10] So that makes sense.
[43:11] That order followed by being able to provide the next version with withdrawals enabled.
[43:18] So again, the main, the main issue from the user standpoint, that's not enabled here is
[43:23] withdrawals and other random stuff like documentation.
[43:27] So I think it's a good decision, a good roadmap.
[43:34] The other thing that I wanted to just touch on since we, we actually talked about that
[43:38] for a lot longer than I thought we would.
[43:41] But if you could just bring your screen share up, well, it's a quick pause for a second.
[43:45] So where did you, I feel like we probably shouldn't go, it's like the, the terminal
[43:49] stuff.
[43:50] We could probably do that for next week.
[43:51] We won't go through it, but I was just going to, we can discuss it without the screen share.
[43:56] I wanted to say that based on our tutorial walkthroughs, it's pretty clear that we need
[44:03] a smoother experience for people.
[44:07] We can, we can keep doing the JavaScript stuff, but I, I've done it enough to know that it's,
[44:13] it's pretty like the SDK needs more work.
[44:17] But I think that we could probably give people a pretty good experience if we went through
[44:22] and use the, the terminal user interface that a DCG has developed.
[44:28] I haven't tried that at all yet.
[44:30] I haven't even looked into it, but it is, it is a tool that's available and it's all
[44:35] open source.
[44:36] So I just haven't looked into it because I wanted to test the JavaScript.
[44:39] Yeah.
[44:40] So next week we should plan on just taking a whole chunk and just doing that.
[44:43] Cause that sounds like something that's probably pretty substantial and could go in a lot of
[44:47] different directions.
[44:48] But what I was curious about is now that we are at this like crucial point, how do you,
[44:54] I want to know where your head is at in terms of the incubator, its role, whether it's changing
[45:01] or not, whether there's like important things you want to prioritize now that we're actually
[45:07] launching cause like this seems like you said that they've been wearing this for like seven
[45:10] years.
[45:11] So like it's a pretty big deal.
[45:12] So I'm just kind of curious where your head is at in terms of the incubator and its place
[45:16] within this launch.
[45:19] Yeah, I think mostly just doing what we've been doing recently.
[45:28] So I want to keep testing.
[45:30] I want to keep exploring.
[45:33] I want to have a real world contract that I'm working with instead of just hello worlds.
[45:48] So in parallel to doing the hello worlds with a few more developers, I think we at least
[45:54] get to that 10 point.
[45:56] So we've got six so far that we've introduced.
[45:58] I want to get to at least 10.
[46:01] And then with those developers, we can continue to test other tooling like the terminal user
[46:09] interface that we talked about just recently and developing real contracts.
[46:18] So for example, Trent that we had on yesterday, he has a real world example and there are
[46:25] other real world examples.
[46:28] I personally would like to start storing incubator claim data on platform.
[46:34] So that's the one that I want to target personally, where we just had a rule change in the incubator
[46:41] where we are expanding our project management to not just be Trello.
[46:47] Like if incubator strategists want to continue using Trello, that's fine.
[46:54] But I'd like to start storing that data on dash platform and developing a contract that
[47:00] can store that data so that, and then an application, a client application that's giving users the
[47:08] ability to make claims, giving me the ability to pull down all the claims and their various
[47:17] states like this is a claim that has been claimed, but not approved.
[47:23] This is a claim that's been claimed, approved, but not paid, that kind of stuff.
[47:29] I want to develop that contract so that I can start using dash platform in a real world
[47:36] scenario.
[47:37] And we would probably have backups and stuff, but I want to start moving in that direction
[47:42] so that we're not just playing with hello worlds anymore.
[47:46] Yeah, no, that makes a lot of sense.
[47:48] And that's, that's, it's just the stock foodie like, and that's, I think that any, any technology
[47:54] company or, you know, platform or whatever that is not dog food, he's kind of saying
[47:59] themselves up to fail because they'll never know what other shit works or not.
[48:02] Yeah.
[48:03] You have to use your own product.
[48:05] There's just no way around it.
[48:06] And I personally, I wouldn't be, I wouldn't be comfortable and I'm not comfortable saying,
[48:10] Hey, this is ready.
[48:12] Even though it's on main net.
[48:14] Yeah.
[48:15] It's on main net and it's also ready.
[48:17] Like, I'm not comfortable saying that I'm not, even though it is on main net in a month
[48:21] or two from now, like for, just to clarify the 29th of July, what that is, is that's
[48:28] saying we are going to release the software that people can then adopt and it will take
[48:36] some time.
[48:37] It will probably take two weeks to, for the network to actually adopt and activate that
[48:43] software if it so chooses.
[48:45] So it's going to be mid August before it's actually functional on main net.
[48:53] But we can, we can test like the, the contract development on test net still using either
[49:00] the rust tooling or the JavaScript tooling.
[49:04] And I, yeah, I'm not going to recommend anybody put any kind of production level contracts
[49:12] or software on platform until I personally have, and I'm using it in a way that I'm relying
[49:18] on platform.
[49:19] Cause if you can't trust it yourself to do anything, then you really shouldn't be recommending
[49:23] it to others.
[49:24] So that's, yeah.
[49:25] Yeah.
[49:26] No, it makes a lot of sense.
[49:27] And that's like when we, you know, hung out the other, back in Utah, you're like, let's
[49:30] pay with Dash.
[49:31] Like the whole process of trying to pay with Dash, it's the same idea, you know?
[49:36] Yep.
[49:37] Yeah.
[49:38] I think the thing that Dash actually has above most other networks is that we have a lot
[49:43] of users that really want to use these things.
[49:46] It's not just some VC technology that, you know, four or five developers are, are using.
[49:56] But nobody else is like, I, I don't want to crap on anyone specifically, but I'm going
[50:02] to like Cardano, Cardano, for example.
[50:05] Cardano was the go-to coin we crapped on at QuickNotes, but it's okay.
[50:09] You're a good company.
[50:11] It's like, there's so much, so much work that has gone into and so high of a market cap.
[50:17] So many investors investing in Cardano, but like, who's using Cardano for anything in
[50:22] the real world?
[50:23] Yeah.
[50:24] Like, at least in the joke, it was the, you know, like we, we want to actually use this
[50:31] stuff for real, real problems.
[50:33] And you know, granted, not a lot of people are using Dash to pay for things in the real
[50:41] world.
[50:42] I wish it were more, but it's certainly a lot more than, than other projects that and
[50:48] compared to the market caps, like we have a lot more user activity is the, is what I'm
[50:52] trying to say based on our market cap.
[50:54] So totally.
[50:55] Yeah.
[50:56] Yep.
[50:57] Anyway.
[50:58] Yeah.
[50:59] We've been going for 50 minutes now, so we'll probably wrap up.
[51:00] That was great, man, that was a ton of information you just, you just spewed out of there.
[51:06] So this will be one I'll probably go back and watch this whole episode again, because
[51:10] there's a lot of good stuff in here.
[51:12] And we had a bunch of people in the chat.
[51:14] We had both Dash Italia and Dash Russia kicking it with us.
[51:21] I was, I was telling Jen, I was like, you might actually watch this stream because this
[51:25] is a big one.
[51:26] And then we had a black mirror designer talking about how much they love NFTs and dolphins.
[51:33] Yeah.
[51:34] Yeah.
[51:35] We're obviously not, we don't have a ton of viewers still because this is like, you know,
[51:41] it's a developer podcast and whatnot, but I think once we've got some, some usable products,
[51:47] some usable applications, then it will be a little bit more real.
[51:52] So yeah, we'll look forward to that.
[51:55] And we'll, we've got to, we've got to make them be the change you want to see in the
[52:00] world.
[52:01] Yeah.
[52:02] All right.
[52:03] Thanks everybody for joining us.
[52:04] We'll see you next week and we'll probably do a few more walkthroughs in the meantime
[52:08] as well.
[52:09] So bye everyone.
[52:11] - Thank you.
