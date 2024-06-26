---
showLink: "https://www.youtube.com/watch?v=N15GTo8saHc"
slug: "sodality-dash-patreon-alternative"
title: "Sodality: A Patreon Alternative on Dash"
publishDate: "2023-05-22"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/N15GTo8saHc/maxresdefault.webp"
---

Tim and Rene discuss Sodality, a Dash-based platform for creators to monetize content without hidden fees, built on Next.js.

## Episode Summary

tl;dr: Sodality, a project led by Tim Spectaprod and developed by Rene Cromer (Mr. Dev), aims to be a Dash-powered alternative to Patreon. It will allow creators to distribute and monetize their content using Dash, while providing users with a platform to spend Dash and support creators. The goal is to offer a transparent, commission-free experience that leverages Dash Platform features like login and tipping. The project is currently in development, with plans to integrate with Dash Platform once it's fully deployed on mainnet.

## Chapters

00:00 - Introduction and Discussion of Current Dash Network Issue
The hosts discuss the current stall in the Dash blockchain mainnet, noting that it's the first time they've experienced this issue. They acknowledge it as a growing pain and part of the process of improving the network.

04:30 - Overview of Sodality Project
Tim Spectaprod introduces Sodality as an alternative to Patreon, allowing creators to distribute and monetize their content using Dash. The project aims to provide real-world use cases for Dash and is close to launching a viable product.

10:13 - Rene's Involvement and Technical Details
Rene Cromer (Mr. Dev) shares his background and involvement in the Sodality project. He discusses the technical aspects, such as using the Next.js framework and integrating with Dash Platform for features like login and tipping. The goal is to create a free, accessible, and transparent platform without hidden fees or commissions.

15:46 - Walkthrough of Sodality Mock-up
Tim and Rene guide the hosts through a mock-up of the Sodality platform, showcasing its functionality and features. They discuss creator categories, subscription tiers, and the ability for creators to offer free, pay-gated, or freemium content.

19:11 - Discussion on Recurring Payments and Wallet Integration
The hosts and guests discuss how recurring payments will be handled on the platform, with Rene explaining that users will need to manually renew their subscriptions each month. They also explore the possibility of integrating with a future Dash web wallet for seamless recurring payments.

24:23 - Project Origins and Development Team
Tim and Rene discuss the original concept of Sodality, which was proposed by either Ash or Joelle. Rene mentions that he is working with Emmanuel Ecripsy to bring the project to completion.

## Transcript

[00:00] The G7 is a group of the world's seven biggest economies. They meet every year for a single purpose, to keep the global economy stable.
[00:12] Guess what the G7 is worried about this year? The American economy.
[00:16] The US is two weeks away from a potential default. Again, understand how this works.
[00:21] The last several presidents here have borrowed from the Fed and have empowered the Fed more so than all the way going back to freaking George Washington, okay, before there was
[00:33] a central banking system, but the national debt has ballooned under the last several presidents faster than you could possibly imagine, but that has to happen.
[00:43] You understand that. Every president must outspend the one before him just to keep the system going here.
[00:49] This shell game Ponzi scheme, you know, it's this trick is, is becoming exposed. I mean, we've had 50 years of continuous deficit spending.
[01:05] The dollar is not attached anymore to anything. It was attached a little bit to, you know, not a little bit, but it was the petro dollar,
[01:13] but we're not now seeing that that's also kind of unraveling. You heard a lot of the de-dollarization and the brick countries really forming this alliance.
[01:25] So if we go back to the 1970s, let's say, where we have this cold war between the West and the East, now it's the West and the brick countries.
[01:35] We've obviously seen a banking crisis where four banks in the US have collapsed. Credit Swiss has collapsed over there in Europe and banks exist on the basis of trust.
[01:46] They're really just, don't take this the wrong way, sophisticated Ponzi schemes. And so when one thing happens in say the banking sector, you can be pretty well assured that
[01:59] it's going to have an effect, not just in those local banks or around those local banks, but far and wide.
[02:06] Global banking crisis means global economic fallout. And I have come to the position of asking, has monetary policy ever done any good?
[02:15] I don't think it has. I think it has done only harm and that's why I'm now pleading for what I've called denationalization
[02:24] of money. Over the past 14 years, since the advent of cryptocurrencies, we've finally had an alternative
[02:31] of a real money to use. It's not controlled by governments, banks, et cetera.
[02:35] However, in that time, almost no one uses this stuff on a regular basis. Still, almost everyone lives entirely off of fiat government controlled currencies.
[02:45] Well, hey, let's change that. I don't believe that we should ever have a good money again before we take the thing
[02:53] out of the hands of government because if we can't take them violently out of the hands of government, all we can do is by some sly, roundabout way, introduce something they can't
[03:04] stop. That is exactly in line with Dash's plans, right?
[03:07] Which is to reach out to the average person and offer them a truly useful product. So I've got to say I feel very optimistic about just about people's willingness to try
[03:18] out money in a different way, particularly the way that we are attempting to build it for them.
[03:25] The 2008 collapse was caused pretty much purely by corruption. There was a lot of like insider stuff going on, a lot of people just trying to make a
[03:39] buck and not really caring about what came out of that. And I think by aligning incentives, you can avoid a lot of that.
[03:53] And by building systems which are robust enough to kind of work their way around people that are corrupt themselves, they put up a greater fight.
[04:08] And so the digital cryptographic revolution is one of transparency, and transparency in general fights corruption alone.
[04:21] And so by using these principles over and over again and building out these structures, I hope to influence the world in a positive way.
[04:30] Hello, and welcome to Incubator Weekly. And we have just had our fourth guest join with us.
[04:48] Hi, Rene. How are you doing today?
[04:50] Hi, everyone. I'm doing all right.
[04:52] Hope everyone is all right over there. Good.
[04:57] So Rene is joining us, Mr. Dev, is joining us as the developer working on a project that is being a strategist led by Tim Spectaprod, who's also joining us today.
[05:07] How are you, Tim? I'm well.
[05:09] Great. So my co-host, Rion, and I, before we get into discussing today's project of Sodality,
[05:19] we would like to touch upon something that is currently happening in the Dash network. Would you care to start us off or give a synopsis of what's happening, Rion?
[05:31] I'm not the best person to give the synopsis of why or what specifically is happening. But actually, before I go into that, I did want to mention in the intro, it was great
[05:43] to see so many faces in the intro today. It was like a reunion.
[05:48] We had Evan, we had Joelle, we had even all the way back to Friedrich Hayek with the denationalization of money.
[05:56] So thanks for putting that reel together with so many gems, Pete and Amanda. Yeah, it was very inspiring.
[06:05] And one of the things that Evan actually mentioned in that reel, which I saw for the first time just now, was transparency and how transparency is, he didn't say this word for word, but
[06:20] the phrase goes transparency or sunlight is the best disinfectant. And he was referring back to the financial crisis and just banking in general, I think,
[06:30] and how much corruption can exist in that system because it's so closed. And blockchains and Dash with cryptocurrencies, we're like the polar opposite where everything
[06:43] is transparent by default. And that is actually one of the strengths.
[06:48] And to kind of segue into what's happening right now, the transparency part, everybody knows at least who's kind of who wants to know and is in the latest conversation knows
[07:01] that the Dash blockchain is currently stalled on mainnet, which is in my experience, I think this is the first time I've ever experienced something like this.
[07:12] It's something that we see in different blockchains a lot. But this is the first time that I've seen it happen in Dash's history.
[07:21] I think it probably did happen a lot in the past, like when it was first being bootstrapped, and I'm pretty sure it will be based on the conversations that I've seen.
[07:31] I think that we're honing in, we meaning Dash in general and Dash core group specifically honing in on what the cause is, and I think that we'll have a solution pretty soon here.
[07:44] But yeah, I think this is interesting territory to say the least to be in right now, where a lot of times we thought Dash never goes down and up until now, for many, many, many
[07:57] years, it hasn't gone down. But when you compare this to other systems, such as Visa networks, they go down, Amazon,
[08:10] they go down. Everybody has some amount of nines, as they call it in the industry, where your uptime
[08:19] is measured in 99.9% uptime, or 99.99%, or how many nines past the decimal point of uptime do you have?
[08:29] And I'm pretty sure that with Dash, we still have some pretty significant nines. But this is the balance that we take with, on the one side, being ultra-conservative
[08:42] and not doing anything new, not trying anything new, because we don't want to break anything. And on the other side, being ultra-progressive and changing everything, and the Silicon Valley
[08:57] slogan of move fast and break things. And I think that you want to be somewhere in the middle, and in my opinion, Dash is
[09:06] pretty well-balanced still. And this is evidence of progress, or at least attempted progress, that we would have this
[09:16] problem, because it would be easy to not have this problem. We would just basically have a system where we'd still be running on version 0.3 or whatever
[09:27] of Dash, and we wouldn't have any new features. So these are growing pains.
[09:32] I'm looking forward to it being in the past, obviously, but this is what we do. We have to improve, and we have to build in order to improve.
[09:41] So it's part of the game. Thank you, Rion.
[09:46] Well, sorry, Oheo, in watching the intro, I just realized how much I miss Evan. And your...
[10:00] Sorry. I appreciate what you've said, Rion.
[10:05] It feels like what Evan might have said, so thank you. Anyway, let us move on to sodality.
[10:13] Dear Tim, would you give us an overview of the purpose of sodality? Oh, there you are, you're good, you're good.
[10:24] One of the things that I appreciate about-- You're a gorgeous river running in the background, or am I the only one hearing that?
[10:31] Yeah, I hear you. That's why I have muted.
[10:33] How's that? That's better.
[10:35] I'll turn my gain down. Is that better?
[10:37] Yeah, and get close to the mic, as close as you can. There we go.
[10:43] Sounds good. Thanks, Tim.
[10:45] Good. Sorry about that.
[10:47] It is sweltering in this room, and the windows are open, and there's lots of traffic outside. So sodality is a-- It started out as an intent to be an alternative to Patreon.
[11:03] So it is one of the-- And that's one of the things that I really appreciate about this project.
[11:08] This is a project that I inherited from last year with all the restructure that we went through.
[11:13] And as we've been able to work on it, we're beginning to see this vision come through of being able to give a platform for creators to create and distribute what it is that they're
[11:22] creating and be able to monetize that using Dash. So Dashitize it, if you will.
[11:31] And then allowing Dash users to have a place where you can actually spend the Dash and support creators doing their thing.
[11:41] And so really, one of the purposes really behind the incubator, building those use cases, like actual, practical, real-world use cases.
[11:51] And this is one of those places where we are really close to being able to launch this and being able to have a viable product that people can begin to build things on and begin
[12:02] to pay for things on. Okay.
[12:07] And then will you please introduce Rene and share with us-- And Rene, will you share with us your involvement here?
[12:18] Sure. So this is Rene, Mr. Dev on Discord.
[12:22] He has been incredibly active in the last, really, probably about the last five or six months in the incubator.
[12:29] And this is one of the projects that I have brought him in on. And I'm really glad that, one, he was able to join this morning, but I'm also really
[12:35] glad to have him available on this project. I've been really impressed with the work that he does, and I've been really happy with the
[12:42] pace and his thoroughness and the details that he goes into. And we're fortunate to have him working with us.
[12:48] Great. Thank you, everyone.
[12:51] Thank you. So before I get started, my name is Rene Cromer, as everybody has introduced me.
[12:58] And well, I've been hearing Dash since 2017, and I've been trying to get in and try to build what Dash has been doing, because I believe it's a vision of being a decentralized
[13:11] currency out there. And it's one of the, if not unique, currencies out there.
[13:17] That has been, as Lionel said, it does have the almost uptime of 99%. So we have not, we didn't have any kind of, any broken staffs or any kind of centralization
[13:29] power to the chain. So after that, I've been working on Solarity for at least two months now.
[13:36] The project itself was tiled, and when I took in, I decided that it needed to have a new infrastructure and updated frameworks.
[13:47] So first of all, we built the Solarity using the next framework. I think that's the best in the current industry.
[13:55] And also, we have been trying to go on and use platform, as we saw in the last week news that platform is now stable on testnet.
[14:03] So what we are trying to do is use the platform and make sure that we have the best out of the platform.
[14:10] So we're going to use every feature from the Solarity using the platform, from the login up to the tipping of the users.
[14:18] So I think, as Spectre said, we have some of the outcomes that we need from the Solarity, and that's what we have been building.
[14:27] First of all, we are building this to be a free and accessible product to everyone. So there will be no any commission, otherwise Dash will be like powering each and every
[14:38] feature on it. So let's say a user might want to just use the app without signing up or logging in.
[14:45] We want to make sure that a user can use Dash without any hassle of using any of his information. So we'll just use, let's say, an address for user, a Dash address, and the user can tip
[14:58] or can subscribe to a creator. I think that's the best solution that we have not seen around this platform, for example,
[15:06] Patreon. And another thing is the biggest problem in Patreon is that there are hidden fees and
[15:13] commission that a user or a creator might not know. So that's what we are trying to remove that in Solarity.
[15:20] Also making sure that no any private information will be used when communicating with your creators.
[15:29] So that's another biggest point of Solarity. And I can give it over to Tim, and so we can continue.
[15:37] >> Okay. And would it be helpful if I were to I found this mockup, this sort of web mockup of Solarity,
[15:46] Tim? Could we have a look through that while we talk about it?
[15:49] Or what do you think? >> Yeah.
[15:51] Let's go for it. >> Yeah.
[15:53] It's so pretty. >> Yeah.
[15:55] So this is yeah, so this is are you on the are you on wireframes or are you actually on the site?
[16:01] Okay. You are on the site.
[16:03] >> Yeah. And I can do it if you want.
[16:05] Or if you'd rather do it, we can load it from your end so that you can be the one to take us around.
[16:10] >> No. That's fine.
[16:12] So right now what you see is a lot of placeholders. Because this isn't a company, there isn't a lot of marketing language around it.
[16:27] So we use Joel as an example across the board of different kinds of creators. And you'll see down here so as we get more creators in there, then we'll be able to update
[16:44] these places and these points. So once we're able to release it, which we're still in production, but what you see is actually
[16:50] a working model of what this will be. And so you're gonna have and so we have example pages of what this can look like.
[16:59] And you can get through and you can use it as an like as example. So it's all in demo mode.
[17:07] But it is functional. And what we're waiting on now really is the ability to fully integrate with platform.
[17:14] So that you can begin to create and begin to be paid for creating and you can begin to subscribe and pay for those subscriptions.
[17:22] And that's really the final piece that we need to be able to pull together. Some of the details are being pulled together.
[17:27] Being able to make it more editable and usable by creators and then by users. But the log in here is going to be using platform.
[17:37] And then to Renee's point, we also wanted to make it so that you don't have to give any personal information, just your Dash wallet address allowing you to actually make transactions.
[17:50] So when you say it's fully or when you say it's functional, what do you mean by that? What do you mean it's functional?
[17:54] So if you go to explore. And so you can make any selection.
[18:03] Let's be a local business. And so there aren't any creators in this category yet, unfortunately, because we don't have
[18:13] any creators. So as we bring them in, you'll be able to tag yourself as a local business so that you
[18:19] are doing something locally. And then you'll be able to search for local businesses that you want to be able to support.
[18:27] You can go ahead and connect through Dash Pay to your wallet. And then here's another example.
[18:32] So you can go into writers and journalists. And if you explore what Usman has.
[18:39] So then you can see this is how I would join this tier. And this becomes automated.
[18:43] And then as a creator, you can go ahead and put out creations that would be free, creations that would be pay gated, creations that would be a freemium, so to speak, edit your profile,
[18:58] be able to put snippets and be able to put previews of what it is that you have to offer. So I have a question about this, the monthly, the recurring payments.
[19:11] How are you handling that? Maybe this is a better question for Rene.
[19:14] How are you handling recurring payments? And maybe in particular, it looks like these are dollar denominated amounts.
[19:24] So how is that happening? Sorry, well, the user will use his Dash wallet.
[19:35] So let's say he or she will, let's say, go on-- he will want to go and join for at least three months of recurring, or let's say just recurring every month.
[19:45] So what we'll be charging is his address. Let's say his address doesn't have enough Dash, then that recurring payment will stop.
[19:52] So the user will have to fund his only Dash wallet so we can get that recurring payment. Otherwise, the subscription will be cut off.
[20:02] Hmm, OK. Yeah, I'm not sure if this is-- if we've got this far in the development, but how does
[20:11] a recurring payment happen? Are you-- is it like a prepayment with time distributed over time, or is it like a request
[20:21] to the wallet? Or how is the wallet actually even connected to the app at this point, or in the plans?
[20:28] Yes, so what will happen is every month when the user will come on to the app, and let's say he want to view other details for another month that it's recurring, he will have to
[20:42] pay at that point where he want to interact with the creator. So we don't actually use the payment, whereas the user doesn't look anything.
[20:51] That will be, let's say, taking funds from the user without his approval. So when it comes, when the subscription ends, and the user wants to continue viewing that
[21:01] subscription, he will have to pay, actually. So we'll have a pop-up, or let's say a timeline where the user will have to pay the amount
[21:10] when that first subscription ended. So actually, we'll have the user permission and not, let's say, a prepayment.
[21:16] OK, so it basically kind of like locks you out of the content. Is it...
[21:22] Yes. I'm not familiar enough with Patreon to know how they're doing it, but is it locking people
[21:29] out of content? Is this more of a donation, or is it like a I pay, like a subscription to get this person's
[21:37] content? OK, so we have all kind of the things you said.
[21:43] We have a one-time donation, and we have a subscription plan. So when the user subscribes for that month, it will actually, when that month ends, it
[21:53] will remind him that his subscription has ended, and thus he will have to pay for the next subscription.
[22:01] So it will actually lock you out. On Patreon, Patreon uses a prepayment.
[22:05] So when your card doesn't have funds, it will lock you out of content, same as what we're doing here.
[22:10] Thus, we're just giving a person more power to actually know what he's spending on at that time.
[22:16] So you just have a prepayment before even he doesn't use the subscription. And this is the MVP.
[22:23] So FutureState is going to deploy things like the ability to use smart contracts, the ability for creators to request payment from somebody, instead of it always being the purchaser pushing
[22:36] a payment to a creator. So there are...
[22:39] The roadmap has a lot more feature and a lot more functionality built into it. This is working to get the MVP out.
[22:49] That is a usable piece, both for patrons of creators and the creators. Okay, yeah.
[23:00] And my understanding of Patreon, again, as a non-user, just from the outside perspective, was that it's mostly like, "I just want to donate to this person.
[23:11] He's delivering content." And maybe even I'm able to consume that content, regardless of whether I'm paying.
[23:20] But it's like, "I just want to support this person." So it sounds like you might have features for both, locking people out of content, and
[23:31] the other one, which is just, you can pay and you can choose to pay, but you'll get the content regardless.
[23:36] But yeah, I'll have to look more into this. I think regardless, it would be interesting to see, when we get a little further along
[23:49] with the wallet project, to see how that might integrate. If we have a web wallet that could potentially, whether that's through an extension, or whether
[24:02] it's through browser storage, or however we end up doing it, it would be interesting to see if we could arrange some kind of recurring payments that's just requesting, you give
[24:16] it pre-authorization to do X amount of Dash per month, or something like that. But I guess we'll get to that when we get a little further down the road.
[24:29] Okay. So will you clarify for me, Tim, I just didn't quite pick up, how much of this is, rather,
[24:38] how much of the intended functionality is reliant on platform versus how much could work without it?
[24:46] So future state is to be heavily dependent on platform. The MVP is not going to be, simply because that's a lot more development, and also we're
[24:55] still waiting for full, we're still waiting, that won't be available until full deployment of platform on mainnet anyway.
[25:03] So the current state is that it will work with that, the current state really is to make Dash transactions available for creators and for patrons, and to be able to gate that
[25:17] which creators want to be able to gate for those wallets that have subscribed. Nice.
[25:23] Okay. And then, out of curiosity, whose original concept was this?
[25:30] I think the original concept was actually Ash's. Either that or Joelle's, looking back through the history, they were both heavily involved
[25:40] in the early stages, and then I picked it up last year, but it was, the concept was either Ash's or it was Joelle's, both of them were heavily involved in building out the
[25:51] original specifications. I think Joelle was the one who made the, I think Joelle was the one who made the original
[26:00] concept. Joelle.
[26:02] Okay. And are you like the, doing all the heavy lifting, Rene, or do you have other developers
[26:06] that you're working with, or how's that? Yeah, so I'm working with Emmanuel Ecripsy on this, so we are trying to collaborate and
[26:14] trying to, you know, get this to the finish line, at least, so we can use almost, let's say, the first Dash login, and then we can come to the next, let's say, integrate the
[26:24] tools that, I think, Coolidge made, that's our plan. Okay.
[26:32] Yeah, I would just be curious a little bit to hear about more of your personal background as we wrap up, like how you discovered Dash.
[26:41] Well, I was marching to Ethereum back in the day, I think it was 2017, I think that was the first time where Bitcoin launched to $20,000, so that was the time where, as a person, as
[26:55] a developer and also as a currency trader, I was trying to look to the alternatives of Bitcoin that will have, let's say, a real use, because at that time, the Bitcoin fees
[27:03] were almost too high, so we were trying to find the best solution that we could get alternative of Bitcoin that doesn't go far away from the Bitcoin, and that's when I found Dash.
[27:12] I think I've been following it for almost years, until I found, I think, last year, the Dash incubator.
[27:18] That's when I tried to join, and then I think I contacted you, and then tried to at least build more on this, because I much believe of what it was before it.
[27:27] I think it was that coin back in the day, that was it. Sounds good.
[27:33] Righteous. Okay.
[27:35] Well, thank you for coming on today, Tim and Renee. It was especially fun to see the mock-up of the site, and that is going to be everything
[27:47] for us today, unless anyone has any final comments that they would like to share. No?
[27:52] Okay. Well, in that case, thank you, everyone, for joining us.
[27:59] We hope to be, at the beginning of next week's episode, we hope to be discussing the totally awesome recovery and fix of the mainnet issue going on in today's Dash blockchain, and so
[28:17] until then, take care. Adios.
[28:20] Thanks, everybody. Thanks, everyone.