---
showLink: "https://www.youtube.com/watch?v=S4sWlcIynMw"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Integrations | Incubator WEEKLY"
publishDate: "2024-06-03"
coverImage: "https://i.ytimg.com/vi/S4sWlcIynMw/sddefault.jpg?v=665dde46"
---

Anthony and Rion discuss the importance of integrations in the Dash ecosystem and explore potential new integrations to pursue.

## Episode Summary

TL;DR: In this episode, Anthony and Rion dive into Dash integrations, discussing the current state, potential improvements, and strategies for onboarding new developers and entrepreneurs. They explore integrating Dash payments into web2 platforms, targeting startup entrepreneurs, and incentivizing Dash usage. The conversation also touches on the challenges of crypto adoption and the need for streamlined user experiences.

## Chapters

00:00 - Recapping Previous Episode and Setting the Stage 

Anthony and Rion briefly recap their previous discussion on XD5 (formerly XRP) integration and set the stage for their conversation on Dash integrations, emphasizing the importance of visibility and hardening one's product through integrations.

03:04 - Exploring Existing Dash Integrations

Rion and Anthony navigate to the Dash.org website to explore the current state of Dash integrations. They discuss the need for updating and better organizing the information to make it more accessible and user-friendly.

10:01 - Identifying Areas for Improvement in Dash Integrations

Anthony and Rion identify areas where Dash integrations could be improved, such as adding the Dash npm package and updating outdated SDK links. They also discuss the future roadmap, which includes a rust library by Dash core group.

17:49 - Strategies for Pursuing New Integrations

The conversation shifts to strategies for pursuing new integrations, particularly in the web2 space. Anthony shares his perspective on the importance of finding crypto-friendly developers within web2 communities to gain a foothold and better understand the landscape.

24:45 - Onboarding New Developers and Entrepreneurs  

Rion explains his strategy for onboarding new developers and entrepreneurs to the Dash ecosystem. This includes providing an easy-to-use web wallet (wallet.dashincubator.dev), educating them about Dash, and potentially incentivizing Dash usage through discounts and premiums.

35:23 - Identifying and Connecting with Potential Integrators

Anthony and Rion brainstorm ways to identify and connect with potential integrators, such as using the Dash incubator Twitter account to reach out to startup entrepreneurs and developers. They discuss the importance of solving real-world problems and targeting individuals with complete control over decision-making.

43:45 - Incentivizing Dash Usage and Solving Real-World Problems

Rion elaborates on his idea for an incentive program that would offer discounts to customers and premiums to entrepreneurs for using Dash. He emphasizes the need to solve real-world problems, such as global e-commerce, and provide incentives for people to try using Dash for payments.

47:53 - Integrating Dash Payments into Web2 Platforms

Anthony and Rion discuss the technical aspects of integrating Dash payments into web2 platforms, particularly through the stripe API. They examine the ease of use and potential challenges, comparing it to other payment processing solutions.

51:48 - Challenges in Crypto Adoption and User Experience

As the episode concludes, Anthony and Rion touch on the challenges hindering widespread crypto adoption, despite the apparent ease of integration. They highlight the need for streamlined user experiences and fewer hurdles in the payment flow.

## Transcript

[00:00] We're going live and we're live.
[00:02] Okay, sounds good. Welcome, everybody. Welcome, Anthony.
[00:06] Hello. How you doing?
[00:08] Good. Good. Yeah. I guess we'll jump right in. So last week, we
[00:16] had a conversation or not last week, but the week before because
[00:19] last week, we took off for the holidays. Right. But the week
[00:23] before we talked about the XD5 integration.
[00:27] Apparently, they're rebranding. Do you know they're rebranding
[00:30] to XD5?
[00:31] I do not. Do you?
[00:33] No, I don't. Yeah.
[00:34] Okay. I guess we'll find out but I welcome that rebrand. So this
[00:41] week, I guess I'll let you take charge on the discussion this
[00:47] week since this was kind of your idea. So why don't you tell us
[00:51] what you had in mind and we'll go ahead and discuss.
[00:55] Yeah, this is partly just based on the thoughts I was having from
[00:59] the previous episode, the integration, because we were
[01:03] talking about how are we going to integrate with this thing
[01:06] that a lot of people are using and supports all these other
[01:09] coins but doesn't currently support us. And I think that's
[01:12] just kind of like a general thing that is good to be aware
[01:15] of with any of these projects is something I know with, if you're
[01:17] like an open source front end framework, you're usually like
[01:21] trolling through docs looking for the frameworks integration
[01:24] section. It's like, alright, it's got React and Vue, but it
[01:27] doesn't have Svelte. So then you open a PR for Svelte to get like
[01:29] Svelte in there. So that's a process I'm kind of like, I
[01:34] think is really important because it's like, want to get
[01:37] you visibility, people who already use this thing will then
[01:40] possibly see you in the docs or we'll see even like the example
[01:43] templates. And it's also good then because it hardens your own
[01:48] products because you need to make it work with a lot of
[01:49] different stuff. So it makes you aware of your own service area
[01:53] and kind of where things can go wrong or where weird edge cases
[01:57] and bugs are. And then also just builds connections like in the
[02:01] community, like you usually have some sort of process of working
[02:04] with people through doing that, even if it's just having getting
[02:06] like a PR approved, or something like that. And then you know,
[02:11] the crypto space is also just like the the money layer and
[02:13] the it's like you we want to be able to transact with each
[02:16] other. A lot of people have different coins. But if you can
[02:18] build in that thing that allows people to use kind of whatever
[02:21] coins they want, then you can have access to the whole the
[02:25] whole crypto space regardless of what kind of coin you want to
[02:27] use, which is not really where we're at. Because everything is
[02:31] so kind of bespoke still because crypto is just such a new
[02:34] technology.
[02:35] Yeah, yeah, it's a it's a bit fragmented still. And there's
[02:39] multi coin support has some there's there's a little bit of
[02:47] multi coin support, but it's tricky. So yeah, I think this is
[02:52] a good topic to discuss. I will say right off the bat that the
[02:59] dash growth team that Joelle Valenzuela leads up is is doing
[03:04] good job here with integrating into like finding partnerships
[03:08] and stuff like that. And
[03:10] there, where would I be able to, where would I be able to get
[03:13] visibility into that for for myself, so I can see what other
[03:16] parts of the dash world is doing?
[03:19] Well, that's a good question. And the first place that I would
[03:22] say let's start is if you if you've got your screen share
[03:26] going, let's, let's go to dash.org. And the way that I
[03:31] like to the way that I like to have these discussions where
[03:36] it's something that I may or may not know. But I want it to not
[03:42] be something that just I know if I do know it, and
[03:46] you want to be something other people can answer for themselves
[03:48] to randomly have the same question
[03:49] on their own, even if I do know it. And in this case, I don't
[03:55] really know the full answer to this question. So we would have
[03:59] to find out ourselves. And if we find that we can't find out,
[04:02] then you know, that's something that we should address. But I do
[04:05] know that there is at least one page on the dash.org site that
[04:10] lists integrations. And so I'd like to see if you can go ahead
[04:15] and find it. And if not, I'll, I guess we'll,
[04:20] this is not exactly the same thing. But this is actually is
[04:25] this? These are is like a picked up picked up version of stuff.
[04:30] This is like, okay, so this is things like the Twitter
[04:34] accounts, the social media accounts. I know it's not what
[04:37] you're talking about. But I just want to look at this real quick.
[04:39] Now this is this is fine. Because this is this is one of
[04:42] the first things that you come across. I'm actually kind of
[04:44] surprised to see this right on the Are we on the homepage?
[04:49] We're on the homepage. So right on the home page, dash ecosystem
[04:55] overview. This is actually something that the incubator did
[04:59] put together, dash incubator, image together, and it's a
[05:03] little outdated. And maybe we can update it. Yeah, I don't
[05:09] know if we should update it. Or if we should. Yeah, focus on
[05:15] something that's a little bit more user friendly. But um, but
[05:20] yeah, this is kind of like an impressive image of some of our
[05:24] the whole ecosystem. It says,
[05:27] so keep looking at this, you want to keep scrolling around
[05:31] the website?
[05:31] Yeah, there's a so you tell me like, what kind of integrations
[05:38] were you interested in? And
[05:40] that's kind of what what I wanted to kind of talk about, I
[05:44] feel like there's there's a discussion to be has like, what
[05:48] are the most high leverage integrations like if we weren't
[05:52] in like, if you couldn't buy dash on Coinbase, that would be
[05:55] like the first number one thing you'd be like, we got to get on
[05:58] Coinbase, like, maybe you disagree with that. But I think
[06:01] that in terms of like actually allowing people to use dash that
[06:05] if it was that would be huge. So that is kind of one thing is
[06:09] like, what are other places where like, there's already a
[06:12] very large contingent of crypto users who could be using dash,
[06:16] but currently aren't like people who like were the defy wallet
[06:20] users. So I guess you have have exchanges, you have wallets, you
[06:24] have dApps, you have just like payment providers that accept
[06:28] crypto. So it's like, you want to look at the what are the
[06:32] number one options for all those and is dash there. So that's
[06:37] kind of partly what I was what I was thinking. But then you also
[06:40] just have the broader open source, kind of crypto world. So
[06:45] when you said that you said it was Joel was the person who was
[06:48] working on integrations.
[06:49] Yeah, Joel, and Joel. Yeah, and he's primarily focused on some
[06:56] of the web three spaces, I want to, to branch out more and focus
[07:03] with you on the web to space and just general web space rather
[07:10] than web three space. But that's something let's let's find what
[07:14] I was looking for, at least. And if you see under developers,
[07:17] there's providers and tools. Yeah. So let's click through
[07:21] there. And this this will kind of show you some of the some of
[07:28] the integrations that we have with, like it's showing here
[07:32] payment processors, exchanges, you were mentioning Coinbase. I
[07:39] don't know if that's on this page or not.
[07:41] Probably, it probably isn't, I guess.
[07:44] I know that we are on Coinbase.
[07:47] That's where it's where I hold my my dash shadow for some people
[07:51] like, don't you hold your own keys, bro? It's like, No, I do
[07:57] not. I'm sorry.
[07:58] Well, we do. We should fix that for sure. So there's software
[08:03] development kits. I don't think that's what you were talking
[08:08] about. But
[08:09] I'm not really talking about anything. I'm talking in a very
[08:13] is as general of a sense as possible because like the word
[08:17] we're trying to get more people into into dash. So that's really
[08:23] good. So things like things like this is like, I have found I
[08:29] like I've known I've been on all sorts of crypto sites like
[08:31] rambling. It's like a polo pop up. And like, it's like the
[08:33] first thing you kind of use. That's why it's like a fiat on
[08:36] ramp. So stuff like this. I think this stuff is huge. That's
[08:40] partly why I think having a Coinbase is important. A lot of
[08:42] people use Coinbase as their fiat on ramp. That's how they
[08:45] transact regular old cash like USD to one of these cryptos.
[08:51] Yeah, I'm actually surprised that we don't have Coinbase on
[08:54] this on our site here. Because I do know that we have that we are
[08:58] on Coinbase. Business solutions is currently empty. So let's
[09:03] let's look at that for a minute. So yeah, this is this is
[09:07] definitely something that I we should we should ask Joel if he
[09:10] can get into the dash.org website and try to spruce this
[09:15] up a bit because
[09:16] yeah, if I did, I would have I would have invited him to the
[09:18] stream if I if I kind of knew that someone else was already
[09:21] was like, I, you know, still a lot of parts of the dash
[09:25] ecosystem. So learn about but um, yeah, so no, no, it's,
[09:29] that's fine. And and it's not, you know, we don't have to limit
[09:32] ourselves to one team working on this dash growth doesn't have to
[09:35] be the only people that are aware of and working on
[09:38] partnerships important to know what the other what our, you
[09:42] know, bordering groups are working on. So we can know
[09:44] whether we're duplicating work or like being synergistic with
[09:47] it.
[09:47] Yeah, absolutely. So the first step would be trying to get this
[09:52] page up to date. So I will reach out to him and see if if if
[09:56] he's on, he's probably already on that if I know him. So he's
[10:00] he's doing a great job there.
[10:01] Yeah, so we could all have like, having soon if there's like one
[10:04] word we're working on or something like that.
[10:06] Yep.
[10:07] So yes,
[10:10] business solutions.
[10:12] And then these are software developed. This is this is
[10:16] interesting. So
[10:17] and this is probably probably outdated as well.
[10:20] But yeah, let's see. This is
[10:23] let's see.
[10:25] Dash core library. So this is
[10:29] five months old. So is this still currently being used?
[10:34] Yeah, dash core lib. That's a that's a current library.
[10:39] Okay, so. So what we would probably want to add to this is
[10:42] we would want to add just the regular dash npm package that
[10:47] that we're using for everything.
[10:48] The one for Yeah, this one. So we will probably want this to
[10:56] be on the
[10:58] list that links outdated. So that
[11:02] that should be fixed as well.
[11:07] Yeah, so
[11:09] dash SDK. Yeah, this is probably
[11:14] then you could have if you want to put this for just like
[11:17] JavaScript, not necessarily node because this can be used in
[11:22] whatever. Yep.
[11:23] Python dotnet PHP objective C. Let's see if there's others
[11:33] floating around the GitHub repo.
[11:37] So these, these, let's see, I want to see where some of these
[11:42] other ones live.
[11:43] Yeah, and as you're looking through those, I'll mention
[11:48] that. I believe that the the roadmap going forward is that
[11:54] dash core group is building a rust library that's actually not
[11:58] on there as well. And that may or may not replace some of these
[12:04] or all of them. Other language SDKs instead of having native
[12:10] SDKs in these languages. I believe their game plan going
[12:16] forward is to us on image is to replace most of them, they got
[12:21] the mesh rust SDK and then have bindings to those languages.
[12:25] Yeah, yeah. No, say four different Bitcoin still says
[12:30] rust Bitcoin library.
[12:31] Oh, interesting. Yeah.
[12:35] Yeah. So as you can see, I mean, there's there's a lot, there's
[12:38] a lot of tidying up that we can do here. Obviously, pull
[12:43] requests are welcome to see custody solutions, API
[12:47] providers. So this would be like RPC providers.
[12:52] Yeah, it's like quick node where I used to work. Yep. And then
[12:57] these were payment processing solutions. So I think the
[13:01] payment processing solutions, that's probably where more of
[13:05] the we could bring more of the web to stuff. And so like, so
[13:08] that's the first thing I would ask, like, what's the deal?
[13:10] What's what's the story with stripe and dash? Like, I think
[13:13] stripe has accepted crypto for a little while, though, a long
[13:17] time. So that would be something I'll be curious. You want to go
[13:20] down that that route right now?
[13:22] Stripe? Let's see, I, I don't know. I mean, the first place
[13:31] that we would look for that would probably be stripe. It's
[13:34] exactly I look for cryptocurrency support. And I
[13:39] would be surprised to see it on here. I don't remember getting
[13:44] support on stripe. I don't remember what support stripe has
[13:48] for cryptocurrencies in general, if at all.
[13:51] So they do is that it offers very little support for
[13:55] businesses according to use case and region. So it's like, it's
[13:59] probably very dependent on a specific country's legal stuff.
[14:03] So here we go, build your crypto business with stripe. So it
[14:10] supports MetaMask, blockchain.com, Mew, like that. So
[14:16] if it supports a thing that supports dash, then there could
[14:19] be a way for us to get in.
[14:22] Yeah, most likely what will what would be the case here is that
[14:25] stripe would probably be using an integration under the hood
[14:29] with some other provider, like a crypto specific provider, like
[14:36] BitPay or Coinbase. And if we're on there, then we would be
[14:42] supported. If we're on that integration, then we would be on
[14:46] stripe as well. But yeah, there again, probably the most
[14:54] knowledgeable person with this with this specifically is Joel.
[15:03] Which one second I'm just opening up my, my chat GPT
[15:06] window.
[15:07] So I'll just I'll just read some of the notes that you sent to me
[15:19] before the show. Yeah. Wondering, number one, what are
[15:23] the most important integrations that we already have and want to
[15:27] maintain? We do have quite a few integrations. But as you can
[15:33] see, it's not super straightforward, it would be kind
[15:37] of nice to have a JSON object somewhere hosted that that just
[15:43] has our current list of integrations, what type of
[15:48] integration it is, so that so that updating it would be a lot
[15:54] easier. Instead of getting into some content management system,
[15:58] it would be, you know, maybe even something hosted on dash
[16:02] platform eventually, so that everybody would have access to
[16:05] it. And everybody could write to it. And there would be a process
[16:09] where it gets updated and whatnot. The second thing that
[16:13] you mentioned here was what are the most important ones that we
[16:16] currently do not have, but we want to pursue? Yeah, it's a
[16:24] separate question. And it's into the question of strategy and
[16:29] different organizations have different strategies. Like I
[16:32] mentioned, Joel's got dash growth that he's working on dash
[16:37] core group has their own strategy. And then my strategy
[16:41] is trying to get integrated into into different front end
[16:48] frameworks. And I've got a call this week that I'm going to be
[16:52] talking with one of these front end frameworks and seeing if
[16:56] there might be something interesting to explore there.
[16:59] Getting into the development process, like the, the
[17:05] development framework, ecosystem itself is important. And you
[17:13] probably you know, this from being very familiar with the web
[17:18] to space, there are whole frameworks like, like remix that
[17:25] have been purchased by e commerce companies. So that
[17:32] coming to mind is obviously the Shopify owns remix now. And
[17:38] there's a reason for that. So there's that's something that I
[17:42] want to explore a little bit more to see what we can do
[17:46] there. So so tell us what you're what you're looking at here now.
[17:49] Yes, I was cat. So I'm just searching around for like
[17:53] front end frameworks and where their kind of crypt integrations
[17:55] are. So the first time I picked was just view because a view
[17:58] ecosystem is one that I usually don't know a whole a whole lot
[18:01] about. And so when you when you google that you just get stuff
[18:11] like view crypto j s. So there's this view crypto dashboard view
[18:24] crypto j s because the the thing and now because, you know, for
[18:34] any of these front end frameworks, like, they're not
[18:38] gonna, if they're gonna have anything crypto related on their
[18:41] kind of like main site or repo or something like that would be
[18:44] like the most high level possible, like integration, so
[18:48] be very unlikely that it would just be like a specific
[18:51] integration with something like dash platform. So that route, I
[18:55] think is hard to go down. So the you have to figure out who,
[19:01] where are the points for those already people who are thinking
[19:04] kind of friendly to crypto in those spaces. And that's where
[19:08] like, honestly, I've struggled with just because when I was
[19:12] working at quick node, most of the developers who I knew before
[19:16] that from the web to those trying to get into quick node
[19:18] were very skeptical of it. And this is also during like the
[19:23] crazy bull run and then crash and like 2022. So I think
[19:28] getting getting a foothold with crypto friendly people in those
[19:34] communities already, if we could find them, then that would be at
[19:37] least a start, because that would then they had give us a
[19:43] lay of the land in terms of like, who else we would want to
[19:45] connect with. So that's kind of like me thinking off the dome
[19:49] right now.
[19:50] Yep. Yeah. Let's mention that real briefly. Because right now,
[19:57] one of our strategic angles here is, you're actually, I've asked
[20:05] you to reach out to some of the developers that you know, that
[20:08] that are in the web to space to see if they can if they'd like
[20:12] to try out dash cloud, you
[20:14] so let me let me show you the first people that I got to say
[20:17] yes. So we're gonna get my friend monarch, Wadia, we're
[20:22] doing the stream with today, actually. And so he he's someone
[20:26] who is not into crypto at all, but is totally, like, cool, has
[20:32] a philosophical kind of thing. And he's been doing JavaScript,
[20:35] TypeScript, and also like, you know, dotnet, they're not that
[20:40] that Java, similar for he was doing that, like, over a decade
[20:45] ago, I think. So I'm gonna be super curious to get his take
[20:49] and you're gonna get to meet him today. And he was telling me
[20:53] that we're gonna like do a live stream, you like give, you know,
[20:56] feedback on the onboarding process is like, wow, you do
[20:59] that live. That's gutsy. And I was like, well, yeah, it's like
[21:01] kind of the spirit of dash in public. You know, what was that?
[21:06] Yeah, that's the ethos is at least it's my ethos. Like I, I
[21:10] don't, I don't want or need things to be super polished
[21:14] before we present them to the world. You know, the whole idea
[21:17] of learning in public, or a lot of people will will kind of
[21:21] start their, their development career, and they'll just,
[21:24] they'll do it all public. And there's something that's magical
[21:28] that comes about with that. Because on the one hand, you
[21:31] know, you're sure you're showing all of your warts and whatnot,
[21:34] and you show your, your limitations. But on the other
[21:38] hand, you know, people do just kind of want to participate with
[21:42] people that show that raw, you know, I'm just learning, and I'm
[21:49] figuring this out, and I'm going to have problems and issues. So
[21:54] I think that, yeah, that is that is something that I definitely
[21:57] kind of stand behind is just this learning in public kind of
[22:00] approach, and having people use our products in public. And we
[22:06] don't have to, you know, hide things, it's not going to be
[22:08] perfect. But I did want to give a little bit more context to
[22:13] what we were talking about there with Monarch. Yeah. So with our
[22:19] last proposal, we kind of pivoted and said, so, Jojobite
[22:23] and, and Kool-Aid 86, they're, they've got a proposal that got
[22:28] passed and whatnot. And, and I'm trying to reach out to more and
[22:31] more developers to have them try all sorts of dash products,
[22:35] whether that's payments, or our platform solution that's
[22:40] upcoming, where you have global state storage, that's
[22:46] accessible. That's something I want to, I want to reach out to
[22:49] more developers. So you and I are going to be working on that.
[22:52] We've got what, I think, five people that are interested.
[22:56] Yeah, yeah, we have five lined up right now. And then I put out
[23:01] a tweet about it yesterday that I'm going to retweet probably
[23:04] right after this stream. So so yeah, so we got the ball rolling
[23:08] with that, which I think is really good. It's just getting
[23:10] the first couple will probably make it easier to get other
[23:13] people so we can kind of show them what it, what it will be,
[23:17] you know, I think, um, I got a lot of people just kind of
[23:19] reaching out who are just like, random, like freelance devs,
[23:24] like the third world and stuff, which is like, that will be kind
[23:27] of interesting to a lot like you vet them, obviously, make sure
[23:31] they actually know how to code and all that stuff. But um,
[23:34] actually, that might be good. Like, those are just gonna be
[23:37] like a lot of your average devs out there in the world, you
[23:39] know, or people in other countries. And, you know, so I
[23:43] think, yeah, a wide variety. So we'll have some people that you
[23:46] know, personally, some people that I know, personally, some
[23:49] people that we don't know, that neither of us know, but, you
[23:53] know, they're, they're a very popular developer, some people
[23:56] that are very unpopular developers that may be more on
[23:59] the beginning side of things. So just a broad swath of people to
[24:04] get to try this product. And, you know, we can't, can't
[24:09] obviously give job offers to all these people, but I want to at
[24:14] least incentivize them to take some time and and learn about
[24:19] dash, because one of the things that's nice is, you know, it's
[24:22] not like I don't view is it as an expense, even some of the
[24:27] best, some of the like, the best way to get people interested in
[24:30] crypto is to give them some crypto, and they can actually
[24:33] try it and use it. So not only are we going to get these people
[24:37] to to try the product and help us with our documentation and
[24:41] whatnot, but you know what I used to use the currency.
[24:45] So what I used to do back when I was working at quick note, and
[24:48] I was trying to get some of my friends into it, I would tell
[24:51] them to set up a wallet and I would send them a donut. So I
[24:56] had a whole bunch of these loopy donuts. This used to be my
[24:59] avatar on Twitter, and they're like dirt cheap. And so, you
[25:03] know, I had just a bunch of them. And it would be a good way
[25:06] to like, for some type to actually set up a wallet, get
[25:09] keys, learn how to figure find their address, send that to me
[25:12] so that then I could like send them this kind of this kind of
[25:15] NFT. And so the with dash, that's, you know, you send them
[25:18] a little bit of a little bit of dash as also this ties into
[25:22] being sure we're integrated with all the things because I would
[25:25] usually if I'm going to, if we're going to be paying these
[25:28] developers in dash, then they like, like, first one who I
[25:33] reached out to ask, he was like, Can you pay me on PayPal? I'm
[25:36] just like, I don't think so. Right?
[25:39] No, no, we're gonna have them go through the whole dash process.
[25:43] So that that I, if you didn't hadn't said that I was that's
[25:47] exactly what I was going to say next is one of the beauties of
[25:51] doing this, this payment in dash is that they can then use the
[25:56] integrations for the subject of the topic today. We need to be
[26:01] able to tell them like, this is how you can actually use dash.
[26:05] And, like, maybe we should do that part in the stream.
[26:08] No, we will. Yeah, we definitely will. Because they'll need they'll
[26:12] need a general introduction to dash itself, if not crypto
[26:17] itself.
[26:18] So let's, let's actually let's, let's, let's do this real quick.
[26:20] So I'm a I'm a developer. I'm like, you need to pay me in
[26:24] dash. And I don't know how to go get a dash address and give it
[26:28] to you. So I didn't know how to do that when I started working
[26:30] for you. So I just gave you a dash address. And I knew what to
[26:32] do. What would you tell us? I'm assuming you wouldn't tell them
[26:35] to go create a Coinbase account. That's what I tell people to do.
[26:38] No, I wouldn't, I wouldn't tell them that that's actually ties
[26:41] into one of my earlier strategies with, with what I was
[26:46] paying developers to develop in the incubator, which was, we
[26:51] have a web wallet. So we do need that super easy way to just get
[26:58] a dash address without going through a budget, which web
[27:02] wallet are you talking about? So, so the, as far as SEO goes,
[27:09] you're going to have, like, the best SEO is going to be the
[27:13] longest running dash wallet web wallet, which probably is going
[27:18] to be the my dash wallet stuff. And as far as I know, I've
[27:21] tested this and it, it's very functional. It works. And this
[27:25] this would be a good way to, to get a dash wallet. What this
[27:29] doesn't have is it doesn't have some of the integrations.
[27:31] It doesn't have a fiat offer. If someone wanted to take the dash
[27:35] that they're paying, convert it to USD, could they do it with
[27:38] this?
[27:39] No, and you can't do it the wallet that I was I was alluding
[27:43] to either. So but if you go to open up another tab, and go to
[27:47] wallet.dashincubator.dev. And this is, this is
[27:55] something that we have been working on. So this Yeah, this
[27:58] I'm this I'm familiar with. Yeah.
[27:59] Yeah. So this is probably this is where I would take them for
[28:02] their first wallet receive dash. And we'll go through this in the
[28:07] stream with Marna later today. But this is this is where I
[28:12] would have them start. And then on the side, you know, I'm not
[28:18] going to use this for anything important about having having
[28:21] that on screen.
[28:21] No, I know. I don't get paranoid about that. Because I know that
[28:25] you know, yeah. So this is why I also would not have a fiat
[28:30] offering, though.
[28:31] It does not, but I want there to be eventually. So what I would
[28:36] tell them is this build, make your wallet here. And this this
[28:42] probably won't. So what we'll do is I'll have Jojo bite, add a
[28:49] couple links to that integrations thing with some of
[28:52] the other integrations that I would like to funnel these
[28:55] people into. And one of those is going to be spritz. So spritz is
[29:01] probably the easiest way easiest dash integration that we have to
[29:05] get into fiat. I use it.
[29:10] Right? Yeah, you've heard about this for paying your bills.
[29:13] Yeah.
[29:14] But it's not just paying bills. It's also if you if you have, if
[29:22] let's you have a bank account, right? Unfortunately, yeah. But
[29:27] if there if these are United States residents,
[29:30] yeah, so this would be if we had this, this was built into the
[29:33] wallet, that would be that would be the thing.
[29:35] Yeah. And I have to talk with the sprints guys to see if they
[29:39] have any kind of API or SDK to integrate with sprints directly.
[29:45] Or if you have to just be easy to figure out.
[29:48] Sprint's finance API.
[29:51] Yep. Yeah, what we would want. Yeah, current. Um, let's see
[29:59] seven months. So yeah, they got base SDK. Okay, a lot of these
[30:05] aren't super updated that frequently. No read me. Okay, so
[30:11] this thing then.
[30:13] Yeah, I'm kind of surprised to see them even have this because
[30:16] I they've never advertised this SDK or, or even the API that I
[30:22] know of the the best way that I know of is to just go through
[30:25] their website and to sign up on their website. And that's kind
[30:31] of a drag. Like I don't like signing up with I like a more
[30:40] than going to even a API though you have to you have to get API
[30:44] key don't you? Yeah, absolutely. But you can you can control the
[30:49] the user experience a little bit better. And we just go off
[30:52] screen real quick and create a spritz account. Oh, okay. So I
[30:57] can start. Well, let's let's do that after the stream here, I
[30:59] think. Because I want you to use my affiliate link. Okay, fine.
[31:05] But also, I don't I don't know if people are too interested in
[31:09] seeing that yet. But that's that that is like the process that I
[31:13] want to go through with with all these developers that we're
[31:16] bringing on. And again, I'm planning on even though we only
[31:19] have one month left, I think that we can get that 10 to 20
[31:22] developer target of introducing them to the dash and, and the
[31:27] dash ecosystem with the integrations that we that we
[31:31] want to funnel them through
[31:32] to this week, if we do two or three a week, then we'll get to
[31:37] get to 10. Yeah.
[31:38] Yeah. And, and I've got some people as well that I've reached
[31:42] out to. So in addition to the one, the five or so that you've
[31:44] already gotten into loop me into those discussions.
[31:47] Yep. So let me let me look back at your list. So we talked about
[31:52] some of the integrations that we have and want to maintain ones
[31:58] that we currently don't have, but we want to pursue. I think
[32:06] that's probably Yeah, that I want to, I want to get people
[32:15] into. Let's see, how do I say this? I want to solve real world
[32:21] problems with with with dash. And so the integrations that we
[32:27] pursue, like, no offense, but I'm not a big fan of the NFT
[32:32] stuff. And I know that you might not be either. But it's
[32:34] something fun to play with. But that doesn't really solve a real
[32:38] world problem to me. So the integrations that I want to
[32:41] pursue are things that basically solve existing problems that
[32:48] that people just generally have, such as, well, the main problem
[32:57] that I want dash to solve for people is basically giving
[33:02] people employment and being able to help entrepreneurial startups
[33:07] deliver their product. And so it's payments, it's it always
[33:14] comes back to payments for me. So helping solve that,
[33:18] it doesn't have to be payments, though, what if it was, you
[33:21] know,
[33:21] yeah, and startup funding as well.
[33:25] But that's what Yes, that's all I was gonna say. Yeah. Because
[33:27] like get funding in, you know, or have some sort of funding
[33:29] mechanism, like crowdfunding platform or something like that
[33:33] crowdfunding platform. So we actually did start a crowd
[33:37] funding platform. A while back in the incubator. We called it
[33:42] springboard. And so that's, that's one of those applications
[33:46] that that we may want to dust off now that platforms getting a
[33:50] little closer to being ready. So that is there we go. Perfect.
[33:56] That I would like to like, that's an integration that that
[34:00] started the world. Yeah. So this is just one app, one, one
[34:06] example, but
[34:07] is a nuts app. Interesting.
[34:10] Yeah, it's a little it's pretty dated at this point. So we would
[34:15] need to put some serious time into that. But your third
[34:21] question here is, what are the first steps to taking getting
[34:25] integrated with us, integrated with the project identified in
[34:29] step two? So yeah, like, what's the process? We're Yeah, right
[34:35] now, that's not very streamlined. The process is
[34:38] basically, you know, like I said, Joel is leading those
[34:41] partnerships and integrations with the with the web three
[34:44] space, typically, and I want to focus more on the web to space.
[34:49] So right now, it's just, you know, basically, I'm contacting
[34:53] you if I think it's interesting, but there's not a very
[34:56] streamlined process.
[34:58] So is there a thing on our homepage, where people can get
[35:03] in contact with us if they wanted to integrate dash?
[35:05] No, so I think I think it would probably be mostly like a
[35:09] Twitter game, an ex game, where we're reaching out to people,
[35:13] and becoming a little bit more active with the with the dash
[35:17] incubator account. So let's talk about that, then what, so
[35:23] nothing's actually dash incubator, should we be making
[35:28] more tweets and stuff to be like, or, yeah, so I guess what
[35:33] will be your ideal thing that this Twitter account will be
[35:37] doing, I guess.
[35:38] So it would be would be reaching out to entrepreneurial startup
[35:44] developers and saying, Hey, how can we how can we help integrate
[35:49] payments for you? So you have a product, you would like to
[35:56] integrate dash, or not just dash, but maybe potentially just
[36:00] crypto payments, and have a have a partner that we have, that
[36:05] that does have dash support. So there are different, different
[36:12] payment providers that we have already partnered with, for
[36:16] example, helping those entrepreneurs get that
[36:20] seamlessly integrated into their site so that they can start
[36:23] making money. So like, I know that getting, getting stripe
[36:33] payments, for example, or any kind of credit card payments is
[36:37] not the most, well, you tell me, is it? Have you ever gone
[36:40] through the process of integrating payments into any of
[36:44] your websites? Um,
[36:46] so I actually something that I'm about to do for the first time
[36:49] with the AI tool that I'm creating, but just knowing the
[36:53] developers I have known and having talked to many people
[36:56] about this, if you're integrating payments, like the
[37:00] is a huge, just like 8020 rule where it's almost everyone is
[37:04] just like pulls in the stripe API, because it's so widely
[37:08] supported, the API docs are considered like, best in the
[37:11] world. And the company is like been around, it's like very
[37:14] stable. So that is what almost everyone I know who is building
[37:19] in payments, who is just like a solo dev, who's doing like uses
[37:22] like services and APIs and have pulled that together into some
[37:25] sort of app. It's like, it's always stripe like this, the one
[37:29] and only answer. So
[37:30] yeah, so that's why it was striped that we were looking at
[37:34] earlier on the show today, right? Yeah. To see if they had
[37:37] crypto support. Didn't answer to that, by the way.
[37:41] So yes, it we it we are well supported, because two of the
[37:44] main platforms they supported were on. So let's go back to
[37:48] that. What was the page we were on before providers and tools?
[37:52] Yeah, so now payments. And the other one was coin payments.
[37:58] Both of these are supported on stripe. So if you have stripe,
[38:02] you can integrate with these two, and then you can accept
[38:04] dash. So that's huge. So we should have like a doc that
[38:07] explains just how to do that.
[38:09] Yeah, yeah. So if you click through and into are those
[38:13] links, API documentation or website? I don't know right
[38:19] offhand if that's what we wouldn't integrate with it
[38:21] integrate with the stripe API, not their APIs. So but it can be
[38:27] as simple as, as targeting those, those web to
[38:33] entrepreneurs, like I'm thinking like, take for a very public
[38:39] example, someone like Theo, right. He has a product, he has
[38:47] upload thing. But I don't know if he has crypto payments
[38:53] integrated.
[38:53] Doesn't and he won't, he won't want them. He used to be into
[38:56] crypto, he says back like a long time ago, and then fell out of
[38:59] it. And now he's not into it anymore. So
[39:02] right. And so I just use him as a public example is somebody who
[39:06] has, who's an entrepreneur has a product that he's trying to
[39:11] sell. And figuring out why. Yeah, if they this is the gap
[39:20] where they're already, you know, levels like levels didn't
[39:23] already have prep integrations. I'm sure he probably does.
[39:26] Yeah. So like finding these guys is the is the process that I
[39:30] want to follow is, okay, I
[39:32] just like my buddy, Noah, my buddy, Noah is super tapped into
[39:36] that space. Actually, I will ask him.
[39:38] Yeah, that's, that's my major target is small startup
[39:43] entrepreneurs, who are maybe even solo developers that have
[39:47] complete control over over the decision making. And you could
[39:54] hand you we can handhold them into accepting crypto payments,
[39:59] especially dash because it's gonna be a really hard sell to
[40:03] try and tell them like building an integration just with dash.
[40:07] We don't we don't necessarily need to do that or want to do
[40:10] that. But we want to we want to promote something that does
[40:14] support dash, obviously.
[40:16] Yeah. And that's why this is the whole the whole integrations
[40:18] question then because if we can get them onto something that
[40:21] already has a very easy onboarding thing and just
[40:23] happens to also support dash, then you get to kind of square
[40:26] that whole circle, you know. Yeah, but that's only the start
[40:30] of the process, obviously. So, and different people have
[40:34] different perspectives and views about this. But I would also
[40:38] like to in addition to getting them set up with that, I would
[40:42] like to have some kind of a incentive program, where their
[40:46] products, let's just say for an easy example, they get their
[40:51] customers would get a 10% discount if they're using if
[40:55] they pay using dash. And not only with a customer get a 10%
[41:01] discount, but the entrepreneur company itself would maybe even
[41:07] get a 10% premium. So and that would obviously have to be
[41:11] subsidized. So again, people have different perspectives
[41:15] about subsidies. But I don't think that anybody would deny
[41:20] that. That companies spend a lot of money typically on customer
[41:26] acquisition. And this is just one way.
[41:29] Would you have like a proposal to have a certain amount of
[41:32] subsidies and then be given to a certain amount of people that
[41:35] that would be voted on?
[41:36] Yeah, it could be, you know, it would basically just be a
[41:39] program. So this is just an idea that I'm presenting here for the
[41:43] first time. This is just something in my head right now.
[41:46] But just the general idea of like, hey, if your if your
[41:53] customers pay with dash, which would require them to go through
[41:57] some problems, some steps, obviously, so it is work for
[42:00] them to probably pay in dash. But that's exactly why we need
[42:04] to incentivize this. Because people aren't going to do it on
[42:07] their own. But give a 10% discount to the customer and
[42:11] then a 10% premium to the entrepreneur slash company
[42:14] owner, and subsidize that. So something costs, let's say
[42:19] something costs $10 on their site, or let's just say $100.
[42:24] Something costs $100. They're paying for whatever $100 thing.
[42:31] It costs them $90 if they pay with dash cost and then the the
[42:37] site owner gets $110 if they do that. So it gives it
[42:42] Would that be just indefinitely? Or would that be for a certain
[42:44] amount of time?
[42:45] No. And again, I don't have the details specified. Even 10%
[42:49] isn't specified, like could be 5% could be nothing. 1% you know,
[42:54] who knows what the number is actually, but just to use a
[42:56] round number to illustrate what I'm talking about. Do that and
[43:01] then have like a tight integration with them so that
[43:03] you could actually verify these numbers. And you'd have limits
[43:07] obviously. So maybe maybe there's like a $100 limit to the
[43:12] the benefit that the company gets.
[43:16] Yeah, you got it. Yeah. Capitalists just like market
[43:19] forces take over and then you end up like getting getting
[43:23] hosed.
[43:23] Yeah, I mean, if you if you design it, right, then, then
[43:28] it's, it's fine to have more quantity because that's achieving
[43:32] your objective, but you can't let it be gamed as well. So
[43:36] these are things like, that itself would be kind of a
[43:40] difficult prod product to build. So we've talked about a lot of
[43:44] things. And
[43:45] no, that's interesting, though, because the ones that we talked
[43:48] about before we started was how like, I'm building this AI
[43:50] thing, I'm going to put payments in. Yeah, like a way to do it
[43:53] with dash, it's like if you could, so it's generating show
[43:55] notes of like you, you have five hours of content is gonna cost
[43:59] you $12 to generate your transcripts and shows for that
[44:02] you could be like, use dash and pay $10 kind of thing.
[44:06] Yeah, exactly. So you just breeze through that real fast.
[44:10] And probably people didn't even catch what you were saying. But
[44:13] you have a product that you're building right now, you're one
[44:16] of the you're one of my target market, because you have, you
[44:20] have a digital offering that you want to charge money for. And
[44:25] obviously, like, digital cash is something that should be easy
[44:30] for you to integrate. And if it's not, then we need to fix
[44:33] that. But I would like you to integrate dash payments for your
[44:37] product, and possibly even have some kind of an incentive
[44:41] program so that your customers look into dash, and maybe you
[44:47] know, because it may end up being I don't know how you're
[44:49] going to price your product. But let's say that you price it at
[44:52] that $100 mark. And if we had that 10% 10% program, where
[45:01] you're giving a 10% discount to your customers, and you're
[45:05] getting a 10% premium for, you know, extra bonus for using
[45:10] dash, that might end up being $20 total, right that the dash
[45:16] ecosystem would have to subsidize. Well, that's a small
[45:18] price to pay for acquiring a user who down goes through the
[45:22] whole process of downloading a dash wallet, looking into it
[45:26] potentially probably having to actually convert some fiat to
[45:30] buy dash, like that's a lot of work for them for $20. Maybe
[45:33] that doesn't make sense for them, but maybe it does. And so
[45:38] that's, that's the whole thing that I'm kind of exploring these
[45:41] integrations, payment integrations, because I want
[45:44] dash to be actually solving real world problems, which is just
[45:49] global e commerce. That's that's a big problem that I want to
[45:54] solve. Like how do we get people using dash because that's the
[45:57] whole premise of the product? If using payments, then we've kind
[46:02] of failed. And if people and people aren't really using it
[46:06] for payments right now. So what do we have to do to get them to
[46:08] at least try it. And then if they have tried it, then maybe
[46:13] they'll see that this is a really cool experience. And I
[46:18] want to do more of that. And I'm going to go look for the next
[46:21] partner that has dash payment integration. You know, maybe I
[46:26] bought Anthony's AI tool, and I have I see a website somewhere
[46:31] that lists all the different products that we have support
[46:36] for, you know, this discount thing or whatever, and then they
[46:40] look into those. So, you know, these things don't, these kind
[46:44] of issues don't solve themselves, somebody has to go
[46:47] out and put the incentives in the right places to get people
[46:50] to actually look at, look at dash, right? Because it's not
[46:55] just going to grow on its own. Somebody has to actually do
[46:58] something to give people incentive to use it.
[47:01] Yeah, no, that's really interesting. I'll be curious to
[47:04] see how that that develops. But um, this is great. I definitely
[47:08] I think got what I needed as episode where my big takeaway is
[47:11] that for the web to developers to be able to use dash, they
[47:16] already can, it's actually not that challenging. But we have to
[47:20] leave people down the right, not actually golden path, but like
[47:23] what the path is going to make the most sense for them. So I
[47:26] think for the vast majority of web to developers, I know, they
[47:30] are already familiar with or are planning on using the stripe API.
[47:34] So I am going to first figure out how to do that with my own
[47:39] app and integrate that so that then you could do the do the
[47:42] dash stuff with their their integrations and just get or
[47:45] have really, really good documentation for that so that
[47:49] someone else could then go through that whole process. So I
[47:51] think that would be highly valuable.
[47:53] So are you are you planning on doing like using the stripe API
[47:58] directly? Or do you have some kind of third party plugin that
[48:03] makes it a lot easier for you to do that?
[48:06] No, you just use stripes API and they have their own SDKs. I'm
[48:10] sure.
[48:10] Okay, so I'm, I'll be curious to see how difficult that product
[48:14] that process is for you. So I'll,
[48:17] I'll, I mean, it's not gonna be difficult. So that's why
[48:20] everyone uses the stripe API and their tooling because it is so
[48:24] flippant simple.
[48:25] Okay, I believe I'll believe you if you say that. I will also say
[48:30] though, that one of the ways that I found AJ is that I was
[48:35] following him and his streams. And it he was integrating
[48:40] payments and building like a payment processing solution. And
[48:47] I, I don't know if he was using PayPal or stripe.
[48:51] What do you mean by payment processing solution? What do you
[48:53] mean?
[48:53] Well, I'd have to look back on it. But I think he was just
[48:59] getting you someone be able, can you pay me $10? Like you're
[49:02] talking about something that's not just that not just accepting
[49:04] payments, right?
[49:05] Yeah, I'd have to look back into it. But it seemed a little bit
[49:10] more, more involved than
[49:12] wasn't I because AJ was trying to build something highly
[49:16] involved. That was the problem.
[49:18] But, but yeah, payments shouldn't be hard. And I think
[49:24] that's one of the biggest value propositions that crypto has is
[49:27] that it should be easier to just drop in a script tag or a react
[49:34] component button to say, okay, now you have now you've enabled
[49:38] payments that was that's been the promise for a while now. And
[49:41] it hasn't picked up. So it leads me to believe that there are
[49:45] other challenges that are preventing people from adopting
[49:48] crypto as payments solution. These are things that I kind of
[49:52] have ideas about why why it hasn't been adopted.
[49:57] Last thing we can that we can close it out. So I guarantee AJ
[50:01] would not have gone to this because he refused to do such a
[50:05] thing. But this is the react structure as documentation.
[50:07] Here's the checkout form with 19 lines of code, including
[50:11] comments. And here's the the where are you bringing your
[50:16] payments on it. So this is all of the code. This is like 40
[50:20] lines of code.
[50:20] I need to go back to that second one. Is this pure JS? Or is this
[50:24] react component? So this is this is react. Yeah. component. So
[50:29] this is a couple of components. I wish they had a screenshot so
[50:32] you could just see it. But I'm like, so this would be a drop in
[50:38] component. And it has card numbers, cash app, actually cash
[50:43] app takes crypto. And then we chat. Yeah. So this is a
[50:50] dropping component. First, right? This is what a drop this
[50:52] would allow you to accept payments by just dropping a
[50:55] component on share site.
[50:56] Yeah, yeah. And I know that react rules the world right now.
[51:00] And so most most developers will be able to use this react
[51:03] component. It would be nice if it if it was something that like
[51:08] do you know if this would you be able to drop this into a solid
[51:13] app, for example, or a view app.
[51:15] So definitely not view solid. You would have to probably make
[51:21] modifications depending on how deep the code goes. And if
[51:24] they're using a lot of specific react isms. But if you wanted
[51:29] to just do your own thing with solid, you would go you go to
[51:34] this one, you would just go to the pure j s. And you this this
[51:37] would work in solid. Yeah, solid. Usually you could just
[51:40] drop in pure j s and it will work.
[51:41] Yeah, so I think I think one of the one of the big questions is
[51:48] just like, why? Why have people if it's so easy? And even even
[51:54] having crypto support, I just don't come across? Well, there's
[52:00] a few things. I think that the flow that Stripe brings you
[52:05] through is a little bit difficult for the consumer that
[52:08] I don't like it to be so difficult. Like, why do I have
[52:11] to add my address? Why do I have to add all this crap?
[52:13] If I just want to be able to apply support, like KYC and
[52:18] stuff like that.
[52:19] Yeah, I know. And that that's why I would, I would like to see
[52:23] a crypto option that's that's less, less fewer hurdles to jump
[52:29] through. Anyway, we're not going to solve all this on this
[52:31] stream. And we've gone 52 minutes. So I think we better
[52:35] wrap it up there. Thanks for kind of coming up with the idea
[52:40] of the topic idea here, something that we've discussed
[52:43] in the past, but not you and I personally, I think.
[52:45] At least so that it's kind of good to reevaluate every, you
[52:49] know, some amount of interval.
[52:52] Yep. Yeah. Okay.
[52:55] Next week, we do have a plan already, but I don't remember
[53:04] what it is right offhand. I think Ash might be coming on the
[53:07] show. So I have to look at that. Ash is building some good
[53:14] products that I want to see if there's updates on like gift
[53:18] cards, basically resurrecting the whole dash spend, or dash
[53:23] direct product that we used to have, but got shut down. Yeah,
[53:29] he's gonna resurrecting that. So hopefully, we'll be able to get
[53:32] an update from him next week. If not sometime in the future. We
[53:36] haven't really nailed that down 100%. But tune in next week to
[53:41] see that if I'm pretty sure that's scheduled, but I have to
[53:46] double check. And yeah, thanks for tuning in.
[53:50] Yep. And if you catch the we'll be streaming with Monarch today.
[53:56] That's going to be so we go by UTC. So what's I'm trying to do
[54:03] the math in my head. So it's gonna be four and a half hours.
[54:06] So 830 UTC, I think. Yeah, that's about right. Cool. Yeah.
[54:11] So you can check that out if you're interested.
[54:14] - All right, later everyone.
