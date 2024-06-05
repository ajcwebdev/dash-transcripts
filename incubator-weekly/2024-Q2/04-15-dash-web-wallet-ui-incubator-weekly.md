---
showLink: "https://www.youtube.com/watch?v=pz5Av9FeSfY"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
slug: "dash-web-wallet-ui-incubator-weekly"
title: "Dash Web Wallet UI | Incubator WEEKLY"
publishDate: "2024-04-15"
coverImage: "https://i.ytimg.com/vi/pz5Av9FeSfY/sddefault.jpg?v=661cb748"
---

Jojobyte, Rion, and Anthony discuss the Incubator Web Wallet's recent developments, features, challenges, and future roadmap.

## Episode Summary

Jojo provides an overview of the Incubator Web Wallet, highlighting its use of pure vanilla JavaScript libraries and recent focus on implementing transactions. Rion shares his vision of reaching out to web developers outside the Dash ecosystem to introduce them to cryptocurrency through the wallet's low-barrier, zero-friction experience. They discuss the wallet's challenges, such as handling edge cases and UTXO management, and future integrations like CrowdNode, Maya protocol, Dash Spend, and treasury proposals. The wallet's mobile-friendly design and potential delivery through decentralized methods like IPFS are also touched upon.

## Chapters

00:00 - Introduction and Wallet Overview
Jojo provides an overview of the Incubator Web Wallet, its use of pure vanilla JavaScript libraries, and recent focus on implementing transactions.

07:47 - Wallet Demo and Contact Pairing
Jojo demonstrates the wallet's features, including transaction history and contact pairing between Jojo and Anthony's wallets.

18:25 - Rion's Vision for Web Wallet Outreach
Rion shares his vision of reaching out to web developers outside the Dash ecosystem to introduce them to cryptocurrency through the wallet's low-barrier, user-friendly experience.

24:45 - Challenges in Building the Web Wallet
Jojo discusses the challenges faced while building the wallet, including handling edge cases, UTXO management, and implementing features seamlessly.

34:26 - Web Wallet Roadmap and Future Integrations
They explore the wallet's roadmap, discussing future integrations like Crowdnode, Maya protocol, Dash Spend, and treasury proposals, as well as mobile-friendly design improvements.

41:50 - Security Considerations and Wrap-up
The potential delivery of the wallet through decentralized methods like IPFS is mentioned, along with security considerations for web wallets. The episode concludes with plans for future updates on the wallet's progress.

## Transcript

[00:00] We are live. Welcome, everyone, to another Incubator Weekly.
[00:09] I've got my trusty co-host, Anthony Campolo. How are you doing, Anthony?
[00:13] Hello. I'm doing good.
[00:15] How are you? Good.
[00:17] And we've got our guest today, Jojobyte. How are you, Jojobyte?
[00:21] Hello. I'm doing pretty well.
[00:23] How are you guys? Good.
[00:25] Good. You're good.
[00:27] Today we are talking about our Incubator Web Wallet. I think it's been probably over a month since we had you on last, Jojo.
[00:38] Why don't you give us a quick just synopsis of what the Incubator Web Wallet is from your perspective, and then I will give an overview from my perspective of why we're doing this
[00:55] and how it fits into my overall strategy. So go ahead and give us an overview of what you're building.
[01:01] Sure. So the Incubator Web Wallet that I've been working on is more or less implementing a
[01:12] bunch of the tools that-- well, it's implementing an interface using the tools that CoolAJA86 is built.
[01:20] And so we've done a lot of work in the incubator to build a set of libraries that are pure vanilla JavaScript and aren't basically transpiled C libraries, which adds a lot of bulk to libraries
[01:42] when you import them rather than being multiple megabytes where, you know, sub megabyte, we're usually sub hundred kilobyte for a lot of our libraries.
[01:53] So it allows us to build modern web apps using a lot smaller of a footprint than some of the stuff with Dash Core.
[02:05] Yeah. And you said this is not using, like, compiled C libraries, but it's not even using compiled
[02:12] JavaScript. It's not.
[02:14] Yeah. It's not transpiling at all.
[02:16] It's not transpiled JavaScript. It's just native, fits right into your browser or node environment, works in both.
[02:23] So you're bringing it into the web environment, obviously, the browser environment. So why don't we since since you talked about the libraries that it's incorporating as one
[02:36] of your first things, why don't we go ahead and start your screen share and bring in that code as well first so that people, the developers among us can see a little bit of what you're
[02:51] talking about? Sure.
[02:53] Let's see. I guess I yeah.
[02:55] Go ahead. Yeah.
[02:57] So this is the open source repository under Dash Hive that the wallet is in, and it's got all the code up to, I believe, the the main focus of this last push has been on getting
[03:15] the transactions view showing. And so this is the branch we're working on right now, the feature transaction view.
[03:26] And we're also oh, I should have pulled up the roadmap. Let me see if I can get that up.
[03:31] I might be helpful to show what we're working on and it's not showing. Hmm, interesting.
[03:39] Maybe I won't show that right now. Right.
[03:42] Right. There we go.
[03:44] All right. Yeah.
[03:46] So we've got a lot in in the pipeline here. This is the main focus that is probably more in review now, but there are some more features
[03:57] that probably need to get added to it, specifically filtering based on contact and stuff like that.
[04:04] And so we've been knocking out a bunch of different things that just improve the wallet and improve the feel of it.
[04:15] And the code here is we have one minor deploy step, but it's not really a build step. It just it restructures the folder structures.
[04:27] But other than that, if you open up the wallet and you view source on the page, which I suppose I could do that, it's not compiled at all.
[04:40] So you're seeing, you know, not even minified files. You don't even need source maps because, you know, like nothing up our sleeves type of
[04:49] thing. Like, yeah, we're showing you exactly what's there.
[04:53] And it's a little bulkier because we're not minifying or g zipping anything. But it's actually not that bad.
[05:00] All things considered. Yeah.
[05:02] Yeah. Normally, when you would these days, when you would open up view source, view source
[05:09] is one of those things which is kind of like old school. That's how a lot of a lot of people, 40 plus years old, would have learned how to do web
[05:17] development as they would. They would go to a Web site that was interesting and then they would right click on the Web
[05:23] site and they would say view source and then they would just read the code that somebody has written.
[05:29] And that's how they would learn how to develop. But these days, because most people what so-called minify their code, it just looks like gibberish.
[05:43] And so you can't really see what's going on there without looking at the source code, where the code that ultimately got delivered to your browser, where it came from, which
[05:53] is usually GitHub. So you're moving around a lot here and might be wondering what's going on.
[06:01] This is an example of what view source looks like on GitHub. Like it's very not readable.
[06:08] So they transpile all their code into a bunch of different JavaScript. If you click into any of these, you can't really get a good grasp of what's going on.
[06:20] And so that's why I was jumping around to kind of demonstrate that where this is ours. You've got all of the functions without it kind of obfuscating any of the information.
[06:34] Okay, now, let's go ahead and just jump right into a demo, I think would be a good thing to do just to give people an idea of where we're at with this wallet.
[06:49] It looks a little bit different than last time we looked at it. It does have some, I think the first thing that people might notice here is there's some
[06:58] icons with Crowdnode and Maya protocol. Those are future roadmaps, things that we hoped to get to last quarter, but weren't
[07:09] able to because we decided to reprioritize some of the things that we were working on. We needed a better transaction view mainly.
[07:18] Last time we didn't have transaction views. And that's one of the main things that we worked on this quarter.
[07:24] But before that, we had a lot of work dealing with just the low level libraries that we had to go back to AJ and say, hey, can we, this isn't user friendly, developer friendly
[07:38] enough. So can we move some of these functions into the library and like different levels of the
[07:44] library. So a lot of work was done there.
[07:47] But why don't you tell us what we're looking at in terms of the transaction views. And then after that, we will go ahead with like having you pair with Anthony, a friend
[08:01] request and we'll talk about that after that. Sure.
[08:06] So the transaction view now shows actually, it's a lot easier to see now that I got the green versus red, so you know, if something's been sent or received from someone.
[08:19] But it also says to or from right here. There's not much to it.
[08:27] You can click on these and it will open up the actual transaction. So you can view the transaction in the Dash Insight.
[08:34] But other than that, when you send a transaction, it updates here. So if I click here to Ryan and I say send, I'm just going to do that full amount and
[08:45] say send. All right.
[08:48] And then it shows us how much which, of course, it's not in the, I've already sent too much. So I didn't have enough in there.
[08:57] But do we have any more to work with? We've got an error.
[09:01] This is one of the recent things we've implemented is when we run into fee errors. So surfacing those errors was, yeah, was something that we spent some time on as well that just
[09:16] troubleshooting the errors. So yeah, I don't think people know how difficult it is to write a wallet from scratch.
[09:24] I mean, even Dash Core Group's wallets, like the core wallet, that's a desktop wallet, the mobile wallets, they're both forks of other wallets that had a lot of runway that
[09:37] was done before them. So like, you know, forked from Bitcoin Core and forked from Bread Wallet or I can't remember
[09:44] the Android one, but there's been a lot of work. It takes a lot of time to get all the things right with building a wallet from scratch,
[09:52] which we've done. So go ahead.
[09:55] Do we have, do you have some more funds to work with so that people don't have to look at grayed out text?
[10:00] Yes, I do. I was going to send this one.
[10:04] So that one worked. I sent half of it rather than the full amount.
[10:07] And so I just popped open the transaction, but that's sending to Ryan and it should update here, but it might take a moment or maybe a refresh.
[10:20] Yeah. Refresh should have grabbed it, so let's see.
[10:40] Interesting. Hmm.
[10:42] This is why this is, this feature is still in development. Yep.
[10:45] Yep. That's why it's not merged to the main branch yet.
[10:49] I've tested this thoroughly, uh, over the past couple of days and then you always run into errors in the demo.
[10:56] And of course it always happens right on demo day. Yep.
[11:02] So we got a problem with something not coming through. Let's see.
[11:20] So none of this, none of this would be, um, you know, funds related, obviously it's just a view, something, some issue with the view not being updated.
[11:31] Actually. I know.
[11:33] Yeah. I can tell what it is.
[11:36] Um, I don't know if you want me to share that, but, uh, one of the things that, that happens is we've got web sockets to listen to balance changes and now the transactions.
[11:50] And so when that initial, uh, I think I can actually fix it here real quick. So when, when the initial web socket runs and detects a transaction, the data that comes
[12:05] through the web socket is actually different from the data that comes through the, um, the rest API.
[12:18] So that rest API ended up, um, or sorry, the web socket API ended up putting data that doesn't actually match the format we were expecting.
[12:29] And I thought this was actually taken care of, but clearly it is not taken care of. All right.
[12:35] Well, maybe, maybe what we'll do is we'll, we'll move on to, uh, the pairing with Anthony instead and then we'll see, uh, we'll see if that one goes through smoothly.
[12:48] So walk us through it, uh, Jojo. All right.
[12:53] So I need to click a new contact here and get Anthony added into my list. So I need to copy this URI, or if he's able to see his screen and wanted to, he could
[13:03] scan that, uh, QR code, but I will drop this in him and, uh, the chat for him. So while you're doing that, I'll, I'll describe what the plan is.
[13:19] The plan is that at some point we would, we'll have at the point where, um, where platform is on main net, uh, which maybe three or six months away from now, I'm guessing, uh, we
[13:32] would have an upgrade path to doing these parrot contact pairings on platform, uh, and not just, uh, through sharing links with, with, uh, one another.
[13:43] Um, okay. I think I paired with you.
[13:47] Okay. Can you share your URI?
[13:51] So I can add you. Yes.
[13:58] Okay. So Anthony's creating a link and sharing it with Jojo.
[14:08] And then Jojo is going to copy that link, paste it into this field and then add contact again that would be improved with platform when it's ready.
[14:19] Um, and now you have a contact that is paired. So you've exchanged what you've done essentially is that you've exchanged some metadata, which
[14:30] is your username, your preferred username, and X pub. And um, so now when you send to each other, you can be using different, a unique address
[14:41] each time you send funds back and forth to each other. And then the transactions would then be able to be filtered by eventually when the transactions
[14:52] feature is complete, you'd be able to look at your contacts, click on it, and then see all the transactions from that contact and that, that user experience would not change
[15:02] between now and when, if, and when we do the platform, uh, update, if, and when each user decides to do that, I should say, you'll probably always have the option to do this local, um,
[15:19] what's what I would consider more private contact pairing, um, or, uh, the public, uh, on the dash platform, blockchain contact pairing.
[15:33] I think we need some more funds to work with. Let me, let me check and see if I have any on my mobile wallet.
[15:40] So I do have this other wallet here, let me do split screen. So this one was already paired, which it has a bit more funds, at least into the, you know,
[15:53] uh, lighter text area. So I can send a bit more funds here.
[15:59] So let's do that. Actually, I haven't refreshed this for a while, so let me refresh real quick.
[16:04] All right. So if I do Jojo and let's do 0.002, maybe I'll do three.
[16:16] Let's do three. All right.
[16:18] And it's showing three, the network fee, and then the price of the send with the network fee.
[16:27] We can open that up. And so now this is, um, what was sent to the other way.
[16:36] No, this is what was sent to the other wallet. And this is the change based on the UTXO that was used.
[16:43] And so this one should be updated. Let's see.
[16:47] Yeah. So, Ooh, that's interesting.
[16:52] It went full screen. Here we go.
[16:56] All right. So, um, Oh, it's cause I'm zoomed in.
[17:00] Let me zoom out a little bit. Okay.
[17:05] So we've got a bit more funds here. We've got three there and, uh, we should be able to send to Ryan.
[17:14] Let's do a send, 0.001. Okay.
[17:23] So it's sending one and the fee send sweet. And then I can also go to Anthony here and say, send 0.001, Oh, overspend.
[17:42] So, uh, I think with the glitch that broke the transactions in this latest branch, it actually needs a refresh.
[17:50] So I just refreshed it and we'll see if it updated so that I can spend again. There we go.
[18:03] Okay. So now we've got these transactions out there.
[18:09] If, uh, Anthony or Ryan want to check your wallets, you should. Yeah.
[18:15] I checked. I've got it.
[18:17] Cool. Yep.
[18:19] There it is. Okay.
[18:25] So I want to talk about, I want to talk about the overall, um, vision of, of why we're, why we're doing this once more, um, this quarter, this coming quarter, I want to really focus
[18:41] on outreach to people outside of the dash bubble, um, at developers specifically. So, uh, at the, at the end of last week, I had an opportunity to go attend, um, a conference,
[18:58] the Anthony, did you hear about the, uh, the Epic web conference? Yeah.
[19:03] Yeah. It's a Kenzie Dodds's new conference.
[19:06] Yeah. Yeah.
[19:08] It was actually, I didn't really realize it, but it was the first conference of the Epic web conference, um, before he was doing remix conferences, I think.
[19:17] And now that he's doing his own thing, you know, he's rebranded it and remixes. It's one thing.
[19:23] And then Epic web is another thing, but anyway, I went to that conference. It was a great experience.
[19:29] I spoke with a lot of people, had my dash shirt on, um, talk to some people about dash, but my, my main purpose wasn't necessarily to, um, to be like preaching and teaching
[19:40] the good word of dash to everybody. But, um, when people would ask about, uh, what was my, what my shirt was about, I would
[19:46] talk to him about dash, but I wanted to more just see what's going on on the ground in the web development scene.
[19:55] And that was a really good opportunity to do that. And this quarter, now that we have, or at least we'll shortly have more of these bugs
[20:04] worked out and transactions showing and, and more features of this web wallet, I want to, um, reach out to these developers to get, get them trying these things, um, probably
[20:18] on screen. So I think I'm going to be doing like inviting people to incubator weekly, for example, or
[20:25] even during the week to try some of these tools out. So our web wallet, which is one of our focuses in dash is like payments and using the traditional
[20:34] layer one blockchain. And then the other thing is platform.
[20:38] So those two things I want to be reaching out to, um, developers outside of the dash ecosystem, um, that may or may not be skeptical of cryptocurrency.
[20:50] Give them a, uh, a try, you got to scroll down, uh, Jojo by, because I I'm seeing this, that half point or scroll up, actually, it was just midway into that, into that number.
[21:03] So anyway, um, I lost my train of thought because of that, but, um, sorry, but yeah, I want to, I want to have them try out cryptocurrency in a way that they will be able to see this
[21:14] is actually very useful technology. And one of the focuses would be then like, pretty much what I found is a lot of people
[21:24] there, you know, they're building, they're building products. So they're building SAS products, um, uh, that require payments.
[21:31] So I want to see what is it, um, about like, what would they have to do? What would we have to say, or what would, what product would we have to do to, for these
[21:41] people to be interested in integrating cryptocurrency payments into their applications? Whether that's, whether they have a SAS product, SAS, meaning software as a service where you're
[21:52] charging money for, uh, to, to use software, a software service, um, why not integrate cryptocurrency and, um, specifically dash like, so creating, um, maybe incentive programs
[22:07] for them to, to look into it, um, paying them to come on the show, just to explore what we have in terms of payments and data storage.
[22:17] I don't think we're, we're there yet. So this isn't something that I would be doing, um, in the first, first month of the quarter,
[22:25] probably, but, um, something near the end of the quarter. Uh, but, but yeah, and then like trying out these, these integrations like crowd node,
[22:34] like Maya protocol, um, and then just giving them a flavor of that. So that's, uh, I want to make it as easy and low barrier, zero friction experience for
[22:46] them because they're not going to want to necessarily go to a website, download software. I mean, it's not, it's not hard to download an app on your mobile phone or on your desktop,
[22:57] but it is, it's just that much more friction. If they can just, if I can give them a URL and say, here's a web wallet, all you have
[23:04] to do is go to this website and get started. I think that's a lower barrier to entry.
[23:10] So what, what do you think, uh, Anthony, do you think that, do you think that the web uh, 2.0 traditional web developers, what do you think their overall experience would be
[23:21] with cryptocurrency at this point? And with this wallet specifically?
[23:26] Um, I mean, I would say probably not a ton and if so, their experience would be with a wallet like MetaMask is probably the one that they would most likely have used.
[23:38] So the idea of like having a wallet and the idea of using it to send funds back and forth, they might be familiar with that and have a general idea of how that works.
[23:48] There's someone who's just kind of interested in, you know, newer technologies, they're, they probably come across that idea, but in terms of working with it in like actual development,
[23:58] that may be something that they're not as familiar with. Yeah.
[24:01] I think that they're actually very unfamiliar with this stuff. Um, very few people that I rubbed shoulders with over that conference had really any idea
[24:14] of what was going on in cryptocurrency other than what they see in the headlines. And so that's, that's part of the problem is that they don't actually have hands on
[24:21] experience with this. Um, so that's why I want to give them that hands on experience and say, look, this isn't
[24:27] a product that's very easy to use. You don't even have to install a WebEx, you don't even have to install an extension.
[24:34] All you have to do is go to this URL and um, follow a couple of prompts. Like it's very, very simple.
[24:43] So, uh, Jojo, what other, can you, can you give us an idea of what, what have been your challenges with building, building this wallet?
[24:55] Um, and what are you looking forward to coming up in terms of features? I am certainly looking forward to getting the, uh, crowd node and Maya stuff in there.
[25:07] That's one of the main features that I always want. I believe, uh, I advocated for that strongly when we were first, uh, planning this out.
[25:17] Um, I also think the, uh, the, what is it? Gift card stuff.
[25:25] Um, I think that would be great to get in here where if you can just grab a gift card straight from the wallet, um, that will be awesome in my opinion, um, that, that would
[25:38] be good for these people that are uninitiated and uninterested in, in crypto right now. Cause a lot of them don't know like, Oh, actually can use this in the real world.
[25:49] And this would be a super easy way to just say, here, pop open this wallet, um, save your seed phrase, and then I'm going to send you one dash and then let's see what you can
[26:01] do with it. Send it back and forth to each other's buy a gift card.
[26:06] And then one other thing that I wanted to mention that I, I didn't want to forget. So I'm going to say it right now in the middle of your sentence.
[26:12] Um, another thing that I want to put into this wallet is creating a proposal on the network.
[26:19] Um, and that's something that, uh, we have also on the side, AJ has, has built, um, a bridge to the RPC.
[26:30] Um, we built a library called dash RPC recently in the last couple of weeks for, uh, different purposes, but now that we have that in a JavaScript library, it would be really easy.
[26:43] And we have a wallet right here. It'd be easy to say, Hey, I want to submit a proposal right here from the web wallet,
[26:49] um, on the net, on the dash to the dash treasury. I submit, I, it costs me one dash, but a little markdown editor modal pop-up that says, you
[27:00] know, just gives a description. It saves it to dash platform and no messing with any other interfaces other than this,
[27:10] this one web wallet. So that's, that's, um, that's something that would be a future integration in this quarter
[27:16] as well. And uh, there was one hour, so there, there would be four, I guess, and we haven't talked
[27:21] about this, uh, Jojobyte yet, but so we have the crowd node, Maya protocol, dash spend or CTX spend, whatever that ends up being branded as that, that Ash very, very close
[27:33] to being, um, to launching, I think. And then once that's launched, we're going to integrate that into this wallet as well.
[27:39] We should probably already put the, put the logo there. Um, once we get that.
[27:45] Yeah. Yeah.
[27:47] I think I just don't have the logo. That's why it's not there yet.
[27:50] Yep. And, and all of those I think are relatively simple now that we have the, uh, the nuts
[27:56] and bolts of transactions, uh, we still haven't got the transaction view working out, uh, seamlessly, but that will be done shortly as well.
[28:05] Uh, but yeah, um, what other thoughts do you have on that? As I interrupted you, uh, Jojo, you there, whoops, Mike got muted, uh, to continue what
[28:22] I was saying, um, one of the other things that I'm excited for, but we haven't implemented yet is, um, we, we do have this set up where it would be possible to send coins from.
[28:38] So rather than breaking up coins into new, uh, UTXOs and stuff like that, we could organize transactions so that when you go to send a contact, it does a one-to-one pairing, which
[28:54] would be, it would be more, uh, akin to, uh, the coin join stuff. And so you would be sending coins directly rather than breaking them apart.
[29:07] Um, and I, I am excited for that. It's, it's more low level.
[29:13] It won't be as obvious to the user, but, uh, from a, from a privacy, maybe not privacy, maybe even security.
[29:22] I, I think, uh, AJ always says it's a security thing. Um, it will, it will allow you to send to, so if I sent to Ryan and I have three different
[29:37] UTXOs and, uh, the transaction will use all of them, it would send Ryan as much as possible, use the minimum fee possible, but also try to keep the coins together so that he has
[29:51] more or less whole coins. And that's, that's one of the things we've been working on.
[29:55] We've got it partially in here for the cash send stuff. Yeah.
[29:59] That's something that we've already been working on, but it's not seamless yet. Yep.
[30:05] It's not seamless thing right now. And I, I should mention also that, uh, one of the things I've got AJ working on on the
[30:12] side is, is doing coin join in the browser and bringing, bringing that functionality to JavaScript environment so that you could use it in browser or node.
[30:24] And uh, that is one of the purposes is that if you, if we have that cash send feature that you're talking about that we haven't really discussed in detail, I don't want to
[30:33] discuss it too much in detail yet until it's, it's working seamlessly. Um, but then if you combine that with a coin join as well, you'd have excellent privacy
[30:43] right from the browser as well. And or if you want to call it security, either way.
[30:49] So yeah, uh, what else, um, I think, yeah, go ahead. Do you have anything else that you wanted to say about, you didn't mention any of the
[30:58] challenges, but, um, that you've been facing, but, uh, did you want to say anything about that?
[31:04] Yeah, I can, I can talk about challenges, um, cause there's been plenty. Oh yeah.
[31:09] Yeah. Uh, especially as we, we got to the MVP stage and we're, we were trying to get to stage
[31:15] one, we have added enough features to this, that there are things we just didn't know until we combined everything to, uh, look out for.
[31:25] And, um, there has been a lot of underlying stuff where it's, it's a little harder for the end user to see, but especially with sending the transactions and stuff, there's fee issues.
[31:40] And, um, you, you can have weird scenarios where because you want to send a smaller amount, you end up, uh, using multiple UTXOs and because it's using multiple UTXOs, the fees go up.
[31:54] So even though you're trying to like, there's just these weird edge cases we didn't know to account for, or at least I didn't know to account for that.
[32:03] Maybe AJ has in the, uh, command line version. And so there were things like, for example, that were done in the command line version
[32:12] that AJ built, but weren't moved over to the library. So once I ran into it, we had to get with AJ and go, okay, where is this function?
[32:22] Why, why isn't this working? And, uh, there's been stuff like that.
[32:27] There's also been, I mean, I'm literally looking at this transaction thing and, uh, I apparently flip flop the from and to, because it's saying I sent funds, uh, I sent funds to Anthony,
[32:43] but it's saying I received funds from Anthony and same for Ryan. So I somehow flip flopped the, uh, uh, transactions here.
[32:52] So that actually should be a two and it should be minus, not plus. So there's stuff like that, where, um, that that's an easy, more, more or less innocent.
[33:04] It's literally just reading the transactions and flip flop the values. But there's been, there's been just a lot of underlying stuff to the libraries and that
[33:15] are complex, I mean, this is cryptocurrency. So it's not just cryptocurrency, it's, it's working with a UTXO or coin models, as I like
[33:24] to call it. Uh, it's much different than something in like Ethereum land, where you're, you have
[33:30] an account model where your funds just, it's, it's more like a bank account. Um, and all the problems that come with that as well, like when you have one bank account,
[33:43] it's very easy to just look up and see coins moving in and out of the, that funds in and out of that account, increasing or decreasing the balance.
[33:52] You have almost zero privacy with that. If you're not using something like, um, tornado cash or some other, um, privacy preserving
[34:00] protocol on any kind of EVM chain, when you're dealing with UTXOs, the digital cash, um, chains like Bitcoin, Litecoin, Dash, um, it's just harder to develop, uh, because you're,
[34:16] because you're dealing with these inputs and outputs. And I think a lot of people probably don't understand how, how difficult that is creating
[34:25] transactions. Um, but let's look forward to, um, what's, what, what do you have coming up?
[34:32] Um, what do we have on our roadmap? Let's let's take a look at that, uh, for, for this wallet.
[34:42] So, uh, the things that are next up on the list are this ready column here. And so we've got a shareable dash URL.
[34:53] So that is connected to, um, this URI could also be a link. So you would just copy and paste the link you're wanting someone to pair with, which
[35:08] will make things quite a bit easier. So that's high on the list, third-party integrations, um, that is these, uh, Crowdnode, Maya, I've
[35:18] actually got it here. Let's see.
[35:20] Um, Dash spend bit refill, and there might be another, so what, what was the reasoning between Crowdnode and Maya being saved and what would go under earn Ryan?
[35:33] Oh, we, we haven't really ironed that out specifically how we're going to present those things to the users.
[35:39] I just thought of potentially categorizing them under, um, what they do, like they help you save money or they help you spend money or they help you earn money.
[35:50] Um, but there are just lots of different integrations that we can, that we can bring into the wallet. Um, under earn, we would have like what I talked about earlier today, um, the proposal
[36:03] integration still straight into the Dash treasury. I think one of the, if we look higher level here, one of the issues that we have in Dash
[36:12] is that we don't have enough competition. We don't have enough developers that are competing to bid down prices, um, and provide value
[36:23] to try to, to try to provide value. And so I think making it easier to submit proposals to the network, even as a solo developer,
[36:33] um, and saying like, I would like 50 Dash to do X, or I would like 100 Dash to do X, Y, and Z, just making that whole process a lot easier.
[36:44] And I think bringing that into the web wallet would be a step toward that. So under earn, we would have treasury proposals under there.
[36:53] Um, we could also have other, we could also bring in our own bounties from the incubator of like, okay, these are ways to earn Dash in the, in the Dash incubator.
[37:05] So however we decide the, the user experience we want to put on that, whether it's just like straight integrations, um, and not categorized or whether we categorize them, I haven't decided
[37:17] that yet, but, um, if anybody watching has an idea of another integration that they'd like to see and, uh, prioritize, let me know, but otherwise we have our work cut out for
[37:29] us in that area as well. Um, to continue on, we've got, uh, some more technical stuff.
[37:40] Uh, this is a, uh, quality of life thing that is complicated. So right now we've got the only way to get access to send your main wallet to fund is
[37:53] from right here. Uh, actually it's not the only way anymore.
[37:57] So we want to get rid of this. Um, right now you can actually just do receive here and send directly to your wallet.
[38:05] Um, but we didn't originally have that. So this needs to get removed essentially, and it will just be editing your profile from
[38:14] there on out. Um, we've got bubble improvements, but actually some of these were done.
[38:20] Um, I've, I had done several fixes while, while implementing transactions to get this to work in mobile.
[38:30] So some of the mobile improvements might actually be done. Um, we've got the contact pairing QR share flow improvement, um, that is related to this
[38:41] same stuff. This is not exactly intuitive.
[38:46] Um, it, it, it's okay, but like even it should be, it should be easy enough that a user knows exactly what's happening when they, and it's not, yeah.
[39:01] And part of the reason why I haven't prioritized that yet is it works for one and depending on how quickly platform comes out, it may not be something that we need to think too
[39:15] much about. Although, um, I would like to give users the option to do contact pairing either way.
[39:22] So, uh, we would, we would definitely do need that on the list. So, um, yeah, I think that's in case anybody wasn't sure about the mobile part that you
[39:35] were talking about, this wallet can be used as a mobile wallet quite simply, um, by going to the web address, go going to the URL of the wallet and then installing the app as
[39:48] a progressive web app. And then you would have an icon either on your Android phone or your mobile phone or
[39:55] your, um, your Apple phone that looks and feels very much like a mobile wallet or a mobile app.
[40:03] Um, and so you have to design it in a way that it, it has a different view and mobile and, um, you've done a pretty good job of that it looks like as you, as we're looking
[40:16] at here. Yeah.
[40:18] So this is showing off some of what's been accounted for. This is where it's, it's decent.
[40:26] Like it's okay. There, there are things that could definitely be improved here.
[40:30] Um, but it's certainly not the best mobile design ever, but it's certainly not the worst. Um, it does make it usable, but our main focus with the MVP and we're just at, so stage one
[40:46] was our MVP. We're now in stage two.
[40:49] Uh, we did not intend to include any mobile in it. So the fact that it has any mobile support is I think a good thing.
[40:57] Yeah. And that was mostly because I wanted to test it on mobile.
[41:00] So we brought some of those things up higher in the list. I would have liked to have gotten further into the integrations, like with the crowd
[41:09] node and Maya and other things, but I was, I was the problem. I wanted to have a better mobile experience just when I was testing it.
[41:17] So we did bring some of that stuff up in the priority at the expense of other things. But that, that is why we have mobile improvements.
[41:26] Is it's worthwhile now that we're past the MVP to get this flushed out a bit more and make it.
[41:33] I mean, the reality is we will have mobile users. People will try to use this from their cell phone and it should work at least reasonably,
[41:41] you know, with a reasonable degree of certainty that it will work. Right.
[41:48] Yeah. All right, Anthony, you've been pretty quiet today.
[41:52] Any questions about what you've seen so far, comments, uh, concerns? Um, I mean, I really liked the fact that it's just like a URL that you can go visit.
[42:03] It's basically a website. It's not really like you're saying a extension.
[42:07] I think that definitely helps because when you need to download like a browser extension, some people may be like, well, what's it going to do?
[42:15] Is it going to like, you know, be stealing all of my traffic and tracking me around the web and things like that.
[42:22] And you don't have to download an app. So I think, um, it's all really good stuff.
[42:27] Yeah. Extensions can be scary.
[42:29] Uh, you give, when you download an extension, it can have significant privileges on your machine.
[42:36] Oh yeah. Literally.
[42:38] It could log all your passwords, like, yeah, yeah. So another thing that we haven't talked about today is, uh, the potential to deliver this
[42:49] app through decentralized, um, methods like IPFS. And we talked a little bit about, uh, IPFS in previous episodes, but I want to bring
[43:01] that all together into how, how do we deliver this mobile wallet in a way that's the most secure that people can trust, uh, trust the most.
[43:11] But in the end, um, you know, this is a web, a web wallet and all things web, you know, you're, you're dealing with pretty vulnerable, uh, environment.
[43:23] So in all of this stuff, I would definitely only use this for like convenience purchases at convene convenience levels of, um, funds.
[43:35] So you're not going to throw, you're not going to throw like $10,000 in this wallet. You're going to, you know, treat it like a, like your wallet, like your physical wallet.
[43:45] Maybe you put 20 bucks. Sometimes you put a hundred bucks in there, but I wouldn't, uh, wouldn't trust anything
[43:52] much more. Uh, yeah.
[43:56] At least at this, at this phase, while we don't have a super solid security, um, it would be like the wallet you keep on you.
[44:06] You're probably not going to keep a thousand dollars in your wallet, but you might keep a hundred or it, the, the other thing I can think
[44:15] of is for example, if you're going to the movies and we've got the, the, uh, gift card stuff in there, like there's, I think, uh, Cinemark and AMC theater gift cards and stuff.
[44:30] So if, you know, you're going to the movies, you've got a date night or whatever, you can stick, you know, 50 bucks or a hundred bucks in there.
[44:36] And then when you get to the theater, you can actually get a gift card for, uh, that theater and, you know, get all your snacks and stuff straight up using dash.
[44:46] And so I, I think that that will be a great thing going forward. Once we've got the gift cards integrated, I know I, I used to do that with, um, what
[44:57] was it? Dash direct.
[44:59] Like I had done that several times with dash direct and I thought that was awesome because suddenly the cryptocurrency is not, you know, as esoteric as it may have otherwise been.
[45:10] Yeah. Yeah.
[45:12] It's, it's going to be usable for something, not just an investment. All right, guys, let's, let's wrap this up unless anybody has any closing thoughts, any,
[45:20] anybody? Nope.
[45:22] Nope. All right.
[45:24] Well, we will keep you posted on the status of this throughout the, you know, throughout the next months.
[45:30] And we will probably, I'll try to have you back on Jojo in, let's say, I don't know, four to six weeks, uh, get an update on, on where we're at and then, uh, we'll see you
[45:45] next time. Alrighty.