---
showLink: "https://www.youtube.com/watch?v=sLsvDqr4Rhk"
slug: "building-our-first-wallet"
title: "We’re Building Our First Wallet"
publishDate: "2023-03-20"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/sLsvDqr4Rhk/maxresdefault.webp"
---

Nick Brunson, UI/UX designer, joins the Dash Incubator to create a new Dash desktop wallet.

## Episode Summary

tl;dr: In this episode, Rion and Joel are joined by Nick Brunson, a UI/UX designer with over 15 years of experience. Nick is working with the Dash Incubator team to create a new Dash desktop wallet that will serve as a lightweight alternative to the Dash Core wallet. The wallet will feature a user-friendly interface, XPUB contact support, and the potential for future integrations with the upcoming Maya platform. Nick discusses his research process and the importance of designing a wallet that is accessible to both experienced and new users in the crypto space.

## Chapters

00:00 - Introduction and Beginning of Episode
The episode begins with a brief discussion of current events in the cryptocurrency space, including the potential effects of deflationary money and systemic concerns beyond specific bank failures.

02:25 - Guest Introduction and Background
Nick Brunson, a UI/UX designer with over 15 years of experience, is introduced as a newcomer to the Dash Incubator. Nick shares his background, having worked in Utah, Silicon Valley, and Los Angeles, and discusses his initial exposure to cryptocurrency.

05:33 - The Need for a New Dash Wallet
Rion explains the motivation behind creating a new Dash desktop wallet, citing the need for a lightweight alternative to the Dash Core wallet that addresses syncing issues and allows for future integrations with platforms like Maya.

13:36 - Wallet Features and XPUB Contacts
The new wallet will be a lite client and support XPUB contacts, allowing users to share multiple addresses with contacts without requiring the full DashPay platform. Rion discusses the potential for upgrading to globally unique registered usernames on the blockchain when the platform is ready.

19:13 - Nick's Research Process and Design Approach
As a relative newcomer to the crypto space, Nick shares his research process, which involves studying existing Dash wallets, competitors, and general finance apps to inform his design decisions. He emphasizes the importance of creating a user-friendly experience that is accessible to both experienced and new users.

22:23 - Building a Reference Wallet and Fostering Competition
Rion explains that the new wallet will be built using vanilla JavaScript and the Tari framework, serving as a reference application for developers interested in building wallets using various frameworks. The goal is to encourage competition and innovation within the Dash ecosystem.

27:50 - Seeking Top Talent and Entrepreneurial Developers
Rion and Nick express their openness to welcoming top-tier developers and designers who can bring fresh ideas and initiatives to the project, emphasizing the importance of an entrepreneurial mindset and the ability to identify and address opportunities in the space.

## Transcript

[00:00] (upbeat music) - Massive bad steepening.
[00:12] The thing that we've been worried about is finally here. So we have the potential effects of deflationary money.
[00:19] This is not about Silicon Valley Bank and Signature Bank. It's not strictly about those.
[00:25] It's about systemic concerns that go beyond them. (upbeat music)
[00:31] We see this non-predictable, non-cyclical, tenuous sort of a nature occurring with the money supply.
[00:40] We may need to ask what is causing that? Is it the market or is it the state?
[00:45] We need more freedom. We need more banks interacting in the market freely
[00:51] by their own volition, taking deposits, making loans freely, able to fail by the way freely.
[00:58] Imagine where we would have been here if we had just had let all the bad actors fail
[01:03] in the global financial crisis instead of intervening. The reason that there's this tension in the economy
[01:08] is not because of the market itself. It's not because of fractional reserve banking.
[01:12] It's not because of free banking. It's because there's a monopolistic issuer in the society
[01:17] and that is the central bank. - We don't want a bank.
[01:25] We want a bank vault. Consumers do not want their deposits
[01:31] to be used for shenanigans. Should there be a service that provides no interest
[01:37] but is just a custodian of money that is absolutely protected,
[01:42] where is the bank vault product in the world? Does it exist?
[01:45] 'Cause I can't seem to find it. What would you pay for that?
[01:47] 'Cause right now we're basically giving every crypto entrepreneur at Zealot,
[01:52] you know, basically the high ground 'cause they could make this product.
[01:55] - Central banks say they have tools, say they're going to deploy those tools,
[02:00] but those tools never seem to produce the desired result. - I mean, why don't we just have one central bank
[02:09] controlling all the money in the entire world, right? As Cain said, the bank core.
[02:14] Or we could have free market money that can't be controlled by any one bank,
[02:20] any one government, any one individual, any one government, any one individual.
[02:25] - Hello, welcome to Incubator Weekly. Today I'm joined as always by my co-host, Rion.
[02:43] How are you today, Rion? - Doing great up here in a snowy Heber City, Utah.
[02:48] - Right on, right on. Well, and we have someone with us today
[02:51] who is not in the snow, though he almost was recently. This is a newcomer to the incubator
[02:58] and wallet designer, Nick Brunson. How are you today, Nick?
[03:03] - I'm great, how are you? - I'm great, thanks for asking.
[03:07] Might be the first time I've been asked that on this. So yeah, we are pumped today at the incubator
[03:14] to be talking about something that is, I mean, is it a first for us, Rion?
[03:18] Like a wallet, a brand new wallet? - I guess it depends what we mean by wallet,
[03:23] but we've had different wallet type products, but this is gonna be the first wallet
[03:32] that we have as like a desktop, more traditional, almost replacement
[03:38] for the Dash Core wallet, or at least a substitute for it.
[03:43] Not a full blockchain wallet, but light wallet. - Right, okay, well, let's start, I guess,
[03:52] from the beginnings of this wallet, which in this case is the design.
[03:57] And Nick, we want to hear a bit about your background, you know, professionally.
[04:02] - Sure, yeah, I've been a UI/UX designer for a little over 15 years.
[04:10] I grew up in Utah, I was born and raised in Utah, and worked there for most of my career,
[04:14] and yeah, another one. (laughs) And worked for a few years in Silicon Valley,
[04:19] and kind of bounced back and forth, and then made my way out to Los Angeles
[04:23] about four years ago. And I've been working mostly
[04:26] as a freelance UI/UX designer out here since then, so. - Okay, and when did you hear, I guess, first about,
[04:34] assuming Dash wasn't the first cryptocurrency you heard about, unless it was,
[04:39] when did you first hear about crypto and how? - I mean, I heard of crypto, honestly,
[04:45] back when I lived in Silicon Valley in the, like, 2012, 2013 era, you know,
[04:50] people were talking about it, but I just didn't know much about it,
[04:53] which, obviously, like most people, wished I would've paid more attention back then.
[04:57] But, you know, then, kind of over the years, learned a little bit more about it,
[05:03] but I've always just kind of casually paid attention, and every now and again, I'll, you know,
[05:08] bought a few coins. But I learned of Dash through a friend, AJ,
[05:14] who's also on the Dash Incubator, who introduced me to the group
[05:20] and told me about the projects and kind of, he and I have chatted about it a few times
[05:25] over the last little while, and then recently kind of brought me along
[05:29] and brought me into the crew. - Okay.
[05:33] So then, fellas, where did the idea for this wallet even come about?
[05:37] - So, we've been talking about, I've been talking about this with AJ for a while.
[05:48] So it's been kind of in our minds for quite some time about, you know, should we do a wallet, should we not?
[05:55] And we decided a while ago that the first step towards that
[06:03] would be building just wallet tools, so that we have all the primitives ready
[06:09] so that we can build a nice, clean, lightweight, and functional wallet eventually.
[06:18] And now that we've got those tools for the most part done,
[06:23] we figured it was time to actually put a UI on top and go with building a wallet.
[06:31] So AJ, obviously that's the connection with Nick, and I'm meeting Nick for the first time on screen here.
[06:40] We've talked over voice, but it's the first time I'm kind of meeting him
[06:45] in visual format. But I wanted to have Nick on as our guest for this
[06:53] because UI and UX, and by that I mean user interface and the user experience,
[07:04] is such a big part of cryptocurrency in general. And obviously a wallet is really dependent
[07:13] on the UI and the UX. And so I wanted to get a designer on
[07:19] just to have us kind of know what goes into that process, why it's important.
[07:27] And I think you've got some questions to drill down on that, but I think a lot of times we aren't as focused
[07:36] on the user experience as we should be, because that's really where it meets our customers.
[07:43] We can have the most functional products that we can, we can have instant confirmations,
[07:48] and we can have high security, and great tokenomics and everything like that in Dash,
[07:56] but unless we have a great user experience, it's just not going to reach the masses.
[08:02] - So I just have a question based on what you've just said, Rion, and do forgive me,
[08:09] this wasn't in the question list that I ran by you fellas, but that prompts me to ask you,
[08:14] Nick, what is your impression of wallets in the crypto space in general right now?
[08:21] Like, what do you think is, I mean, is anything very good? Is anything very terrible?
[08:27] Like when you're coming to the space, what's the mind frame you're coming with?
[08:32] - Yeah, it's interesting you ask, 'cause part of this process as I've gotten started
[08:38] with Rion and AJ and the team was to do a little bit of what we call discovery,
[08:44] where we'll kind of go and look at the market and see what's out there and help me get some research
[08:50] and understand a bit about just the crypto world in general, 'cause I'm a bit new to it.
[08:56] And so, yeah, during that process, we actually looked through a lot of the different wallets
[09:00] that are out there and kind of some of the products that are out there.
[09:04] You know, my general sense is that there are a lot, there are a lot of different wallets that exist out there
[09:10] and many of them are sort of, you know, don't have much thought or design thinking behind them.
[09:18] And then there are a few that are pretty good that are sort of kind of the bigger names
[09:22] that have pretty decent design and user experience, you know, like Coinbase being one of them, Robinhood.
[09:34] Those are kind of some of the bigger ones that seem to obviously put a lot of design
[09:39] and thought into the user experience. But there are a lot of really good tokens and coins
[09:46] out there that don't necessarily make it on those platforms or have a hard time sort of competing
[09:53] or getting exposure in some of those places. So it's kind of an interesting space right now
[09:58] for me to be learning about, I guess. - Right, okay, so let's talk a little bit about,
[10:06] I guess, just why is there need for this wallet, Rion? Like you said, you thought that it could serve
[10:14] as a sort of substitute, though not a full blockchain substitute
[10:18] for the Dash Core desktop wallet. What do you think can be brought by this wallet
[10:26] that we don't already have? - And as you asked that question,
[10:32] I see a comment from a girl named Rachel Rawson, who actually happens to be my wife.
[10:39] Her name's not updated on that profile apparently, but. - That's the name she uses online
[10:46] that you don't know about. It doesn't have your last name on it, Rion.
[10:49] - Yeah, exactly. And as it says in this comment here,
[10:53] she does all the heavy lifting in our household as far as like spending Dash and using Dash.
[10:59] And I do hear some complaints every now and then, like why is this wallet re-syncing again?
[11:05] Why is it not sending my transaction? So cryptocurrency, it's a hard space.
[11:13] So I understand there's challenges and no disrespect to the builders of existing wallets
[11:21] on the market right now. But I felt like we needed to have something
[11:26] that we kind of controlled as far as the performance and like syncing issues.
[11:34] I've had syncing issues forever with the Dash iOS wallet. And although we're not targeting mobile specifically
[11:43] as our first phase, I've had different experiences with desktop wallets as well.
[11:50] But beyond that, there's also a lot of integrations. Like recently we've had on the Maya guys
[12:00] where you can have instant exchanges between cryptocurrencies within wallets
[12:08] or providing liquidity on those platforms and earning a yield.
[12:13] And obviously we don't have any Maya integrations in any of our wallets yet because it's not live yet,
[12:21] but it will be live pretty soon. Actually, probably within a month,
[12:25] we will be able to have that opportunity to be integrated with Maya.
[12:31] But I'm not sure if we have any plans for our other wallets to integrate with Maya,
[12:38] but we certainly would at some point. And while we're keeping our scope limited
[12:43] in our first iterations and we won't have that Maya integration,
[12:47] that is something that we will have the ability to do very quickly when that happens.
[12:53] And so that's one of the other reasons is to be able to make integrations very quick
[12:59] and something that we control personally or as an organization.
[13:04] So that's part of it as well. - I'm not sure if I answered your question, but...
[13:12] - Yes, you did. So let's talk just a little bit
[13:18] about the sort of at time of launch features that can be expected from this wallet.
[13:25] So we already said Lite client, so it doesn't require full blockchain download.
[13:31] And there were a few other features and let's just cover those.
[13:36] I believe the main thing is XPUB contacts. That's the main technical term.
[13:42] I don't even like to use these terms, but I know that maybe there's not a better one.
[13:47] But will one of you give us just like a general overview of like, what does it mean
[13:51] that the wallet will have XPUB contacts and support hierarchical deterministic?
[13:56] What does that mean? - Well, I'll start that answer.
[13:59] And I would like Nick to give his feedback on this as well. After I go over the foundation.
[14:08] XPUBs is extended public keys. And it's the basis of being able to share multiple addresses
[14:17] with contacts that you make. And it's the basis obviously for our DashPay project
[14:24] that's been going on for several years. And what we've decided is that we can get XPUB contacts
[14:31] that we can get, I don't wanna put a percentage on it, but we can get a high percentage of the experience
[14:42] of what DashPay is going to offer with the friending process and whatnot.
[14:48] But without having the huge overhead of the DashPay contract and everything
[14:57] and having to wait for platform to get on main net, just using extended public keys alone
[15:04] and exchanging those and being able to name contacts and have that be a focal point of the wallet experience
[15:13] of just kind of like Venmo and like PayPal. Actually, I don't even think that they do it very well,
[15:20] but have the friending and the contacts experience upfront and a focal point of the wallet.
[15:29] And you can do that with just extended public keys. And so we've got the libraries to be able to do that.
[15:34] Nick doesn't have to worry about that obviously in terms of the blockchain internals,
[15:41] but he'll be focusing on that as part of the user experience.
[15:47] So the friend contact requests, and this is something that I think
[15:55] that we could have had a long time ago, but we went very far
[16:00] and like ended up building a whole separate blockchain, but we could have probably done this many, many years ago,
[16:08] just having exchanging public keys as friend requests. So that will be another feature of the wallet.
[16:15] And then later at a later time, when platform is done,
[16:20] we can just upgrade people to have these globally unique registered usernames on blockchain.
[16:27] So we can morph into that when it's ready. - Simple enough.
[16:32] Okay, so as you had said there, oh yes, I wanted to ask just a little bit about cost.
[16:47] As you had mentioned, Rion, the tools that Nick primarily needs to build this wallet
[16:56] have been built in a former incubator project that we covered several weeks ago
[17:03] with developer AJ called the Payment Tools Project. So does that mean that the majority of the costs are covered
[17:12] or like what do you expect things will cost in total going forward?
[17:17] And how would that compare to maybe what other wallets you may have heard of might cost?
[17:24] - I actually have no idea about where it's going to end up as far as costs go, but I will say one thing,
[17:30] like we have done a lot of the internal tooling already. But again, another reason that Nick is here as our guest
[17:40] is that I wanted to make it explicit that design and user experience is a very focal point of this wallet.
[17:48] And so while we do have a lot of the internal tooling already built and the costs are already absorbed there,
[17:59] we do want to spend some significant portion of time and effort into building the design.
[18:08] And specifically Nick is an asset here because he's not very familiar with cryptocurrency.
[18:15] I wanted to have somebody, well, actually it's not like I went out
[18:20] and I selected somebody. AJ kind of brought Nick into the project
[18:24] and I thought it was, I just happened to think it was great that he,
[18:28] he's not one of us yet as far as like in the inside group of Dash.
[18:33] And like, that's a feature not a- - Not a bug.
[18:39] - Not a bug, yeah. So as far as like the incubator goes though,
[18:45] one of the nice things about just our structure in general is that everything is exactly accounted for.
[18:52] So you will know real time how much we're putting into the wallet,
[18:59] both from the design perspective and the coding perspective.
[19:03] And so anybody who's interested in knowing how much it costs,
[19:07] they'll know exactly down to the Dash or Duff what we put into this.
[19:13] - So then Nick, with your not yet being a lemming, would you share with us a bit about the research process
[19:24] that you have gone through in order to come up with your initial design plans?
[19:29] - Sure, absolutely. So like I had mentioned before,
[19:33] what I like to do usually, especially with any new project,
[19:37] but especially with one like this where, like you said, I'm sort of new to the crypto world.
[19:42] I'm not fully initiated yet. I'm what I would consider myself
[19:46] like kind of a casual observer. We like to do a phase called discovery,
[19:51] which is essentially just a research phase where I take some time and some inputs from the team
[19:57] about kind of where to look and what to read. And so we did that.
[20:01] The team sent me some links and some places to look and some ideas to kind of spend some time on.
[20:09] And then what I did is just kind of went out and read through a lot of the documentation
[20:14] and looked at a lot of the competitors and looked at some of the other Dash wallets that exist
[20:20] and some of those types of things. And so you can see here what you're sharing
[20:24] is just sort of a bit of my notes and a bit of a live sort of document
[20:31] that was just a place for me to capture some of these thoughts and share it with the team
[20:35] as I went through this process. So you can kind of see here that,
[20:40] just went and learned a little bit about Dash in general and even some of the more technical things,
[20:44] which a lot of this was kind of over my head. And then, as I worked from left to right here,
[20:51] I went and researched some of the existing Dash wallets, both web and mobile, and even some of the desktop ones
[20:59] where you actually have to download the desktop app. I won't go too deep into each of these,
[21:06] but then sort of working my way towards some of the more well-known things
[21:12] and a little bit of the larger sort of platforms that are out there that exist.
[21:16] Again, I mentioned Coinbase, I think, before. And then even all the way out to just looking at
[21:21] some of the general finance apps that exist in the world. As Rion was talking about Xpub and Contacts
[21:28] and some of those things, he was mentioning things that are new to me
[21:31] that I am learning even as he talks. And so it's great to kind of learn a little bit about that
[21:38] and kind of get an idea of how we're gonna move forward with designing a solution
[21:44] that feels a little more open to everyone and something that, again,
[21:50] you don't have to be quite as initiated to interact with. And I think the contacts thing
[21:55] is definitely one of those sticky points. People tend to get a little nervous
[21:59] when you have to copy and paste a 70-digit hash code or something into the wallet address.
[22:07] I think that makes the normal user a little bit nervous. So those are some of the things that we're learning about
[22:14] and trying to get an idea of kind of how we can move forward and design some cleaner, simpler solutions for people.
[22:20] - Got it. - Yeah.
[22:23] - I wanted to say one thing before I forget. Another side purpose of this is to also,
[22:31] how do I say it? Create some competition and some education
[22:38] as far as Dash development goes. So if you looked at the project card
[22:45] for this specific project, you'd see it's named something like vanilla,
[22:51] vanilla- - Vanilla Web Wallet. - Vanilla Web Wallet.
[22:54] Yeah. - Yeah. - And the reason that vanilla is in there
[22:56] is because we are building this wallet. We're building it without a JavaScript framework.
[23:04] We're building it in JavaScript. And we're most likely going to use
[23:09] a framework wrapper called Tori, which is a Rust.
[23:17] It's a program that allows you to create desktop, cross-platform desktop wallets using HTML, JavaScript, CSS,
[23:31] but also Rust if and when you need it to create the actual executable for your binary
[23:41] that would actually run on your platform. So the desktop app, it's a desktop app.
[23:45] So if anybody has heard of Electron, it's very similar to Electron
[23:50] in that it creates a cross-platform. - Electron? - Electron,
[23:55] which is different than Electrum. So Electrum is a, I believe it's a Python web wallet,
[24:04] or not web wallet, but desktop wallet. And that's totally different.
[24:08] That's a desktop wallet written in Python. Electron is a technology that's used to,
[24:17] where you write HTML, JavaScript, CSS, web app, but then you wrap it in this container
[24:27] that makes it, instead of running just on the web, you can run it on as a desktop wallet
[24:31] or even a mobile wallet, I believe. And that's called Electron.
[24:36] And it's been around for a long time, but Tari is something very similar to Electron,
[24:42] but instead of, I don't know what Electron is written in, but it's kind of old and dated.
[24:48] It's got some cruft and some technical debt in it. And Tari is kind of like the new latest greatest
[24:56] built-in Rust application framework so that you can build your applications.
[25:02] And you can build them in just vanilla JavaScript, but you can also build them using a framework
[25:08] like React or Vue or Svelte or Solid. And so we're initially going to be doing
[25:16] the vanilla version, more or less, as a reference application.
[25:23] And then so that anybody who has JavaScript experience can look at this and see,
[25:29] this is how you build a Dash wallet in JavaScript. And it's very simple.
[25:36] You can put it in this Tori wrapper, and then now you've got a desktop app,
[25:40] but then other people can kind of take a look at that and see this is how the libraries are used.
[25:45] And I wanna do that in React, or I wanna do that in Solid.
[25:48] So as developers come into the incubator that might be more interested in,
[25:53] developers are kind of tribal in that sense that once you're a React developer,
[26:00] you just love React and everything that you wanna build has to be in React or Solid.
[26:06] Same thing, Svelte and Vue. So we can kind of take this application,
[26:11] as you use it as a reference, so that anybody who wants to build a wallet
[26:16] that's in one of these other frameworks, they can use this as a reference.
[26:23] So I guess that kind of fits in with my broader view of cryptocurrency and Dash in general,
[26:33] in that we're moving into a world where we have a new financial system,
[26:40] and we need to have lots of different wallets and lots of different developers building
[26:47] and competing to create the best experiences. And we're just getting started.
[26:52] So we need to have great solutions. And yeah, we need to have a lot of different wallets,
[27:01] I think, instead of just relying on one team with one wallet, we need to broaden that out a little bit.
[27:09] - Got it. So my final question that could apply to either of you
[27:16] is if you, I'm assuming that you're feeling pretty good on the talent front,
[27:25] as far as what's required to complete this wallet, but if you weren't,
[27:29] if there were like one dream person out there, if you were gonna send you a Discord message,
[27:35] today or tomorrow being like, this is what I could bring to this project,
[27:38] are you interested? Who would that person be?
[27:42] Like, is there anything in your dreams that remains to see this project be even better?
[27:50] - Um, not exactly. Like I just said about the different framework developers,
[27:58] I would like to have some more like experts in different frameworks come in and say,
[28:05] hey, I don't need a lot of guidance. I can see this reference application,
[28:12] and I think I could do it 10 times better, 10 times faster at a 10th of the cost.
[28:18] You know, obviously those numbers are inflated, but some developers are just awesome.
[28:24] And if they are watching this or they hear about this and they, you know, our accounting's open,
[28:31] they can see like, hey, I can build what you guys are building.
[28:37] Like, I'm way better, essentially. Then yeah, come in and join us.
[28:44] We have room, we have some funds to work with, specifically for top-tier developers
[28:52] that don't need a lot of hand-holding, mostly like entrepreneurial developers.
[28:57] Just come with your own idea and don't necessarily ask to be like, what can I do?
[29:04] But just come with your own idea and tell me what you wanna do.
[29:11] Tell one of us, one of us strategists, what you think is great, and then we'll see if it works.
[29:18] - Okay. - Yeah. - Please, Nick.
[29:23] - Oh, I was just gonna say, I don't have a good answer for that.
[29:27] I just started with the team and so far they've been great. So, you know, no complaints, but you know,
[29:34] I agree with Rion anytime anyone of top talent, even if there are more designers that could come join in,
[29:39] that'd be great too. So it's always fun to work with more people
[29:43] and have additional views and ideas, like you said. So yeah, I agree.
[29:50] - Yeah, and just coming in with an attitude of like, I see a problem, I see an opportunity,
[29:59] and I know how to fix it. That's the best thing that we can get.
[30:03] And yeah, Nick and I haven't worked together well, or not together long at all.
[30:09] And so it'll be, so I guess this is kind of like a dialogue for Nick as well.
[30:15] Like, just kind of look at the opportunities, look at the space, see what you see as opportunities
[30:22] that we're lacking and just kind of run with it. And we'll stop you if we need to,
[30:28] but just take the initiative. - Righteous. - You might have to stop me.
[30:34] - Yeah, good, good. - That would be a high quality problem to have, no?
[30:39] Like Nick is obese, someone please stop him. - Someone stop him.
[30:43] - Good. Okay, well, that is Incubator Weekly for this week.
[30:49] So we look forward to updating you more on this particular project in the future.
[30:55] And yeah, we'll have a new and different topic for you next week and look forward to seeing you then.
[31:02] - Okay, see you guys. Thanks. - Sorry I'm late.
[31:05] - Thanks for having me. Yep. - Welcome.
[31:07] - Thanks, Nick, bye. - Bye-bye.