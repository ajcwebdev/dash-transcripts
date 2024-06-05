---
showLink: "https://www.youtube.com/watch?v=MKha_n_ZVB4"
slug: "js-web-wallet-alias-support"
title: "Update: JS Web Wallet w/ Alias Support"
publishDate: "2023-10-30"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/MKha_n_ZVB4/maxresdefault.webp"
---

Jojobyte showcases a JavaScript-based Dash web wallet with contact pairing, fund requesting, and a roadmap for future development.

## Episode Summary

tl;dr: Jojobyte demonstrates an experimental JavaScript-based Dash web wallet with contact pairing using XPUBs, fund requesting, and sending/receiving payments. The wallet aims for simplicity, security, and minimal dependencies. Future plans include transaction history, multiple wallet support, and various integrations like Dash Direct, CrowdNode, and mixing. Development progress is steady but limited by funding through the Dash Incubator.

## Chapters

04:57 - Introduction and Overview of Wallet Features
Jojobyte introduces the experimental JavaScript-based Dash web wallet, discussing its features like contact pairing, fund requesting, and sending/receiving payments. The hosts discuss the wallet's technical aspects, including its use of pure JavaScript without frameworks for security and performance, and the storage of wallet data in the browser.

08:28 - Live Demonstration of Wallet Functionality
Jojobyte demonstrates the wallet's features, including generating a new wallet, importing an existing one, pairing contacts, and sending/receiving payments.

29:07 - Explanation of Contact Pairing and XPUBs
Rion and Jojobyte explain the contact pairing process using XPUBs (extended public keys), discussing privacy considerations and compatibility with other wallets.

45:32 - Roadmap and Future Development Plans
Jojobyte shares the project's roadmap, detailing completed tasks and future plans like transaction history, multiple wallet support, and various integrations. The hosts note that progress is steady but limited by funding.

## Transcript

[00:00] (upbeat music) If you attend business school,
[00:08] you can expect to read a lot of case studies. They offer real world examples
[00:11] of why businesses and products succeed or fail. Let's review a handful of products
[00:16] and see what can be learned from each. Google set to create a new flagship phone, the Pixel 6.
[00:22] At the center was its Tensor SoC, or sensor on chip. Google did a lot of marketing, or created hype,
[00:28] as one write-up put it, which included ads online, in magazines, and on billboards.
[00:32] They partnered with professional athletes and aired a Super Bowl commercial.
[00:35] When the Pixel 6 was released, record sales were reached. The Pixel 6 sold more
[00:39] than the previous two models combined. The takeaway, this was not happenstance,
[00:43] it was due to being focused. Google spent years developing
[00:46] the technological underpinnings, and then coupled it with tremendous marketing,
[00:50] which even their hardware chief saw as investing. A few years ago, the COVID lockdowns,
[00:56] aka the Plandemic, or Scandemic, or COVID-1984, was foisted upon us.
[01:01] Many businesses struggled, especially the mom and pops, and 200,000 closed their doors for good.
[01:06] Meanwhile, one business thrived, Amazon. As individuals shifted buying habits
[01:10] from in-person to online, Amazon massively expanded its workforce,
[01:13] grew its air fleet, and built more distribution centers. The takeaway, Amazon, being an e-commerce company
[01:18] from the get-go, was well-positioned to supply this demand. Their operations worked, they merely scaled them up,
[01:24] and revenues spiked accordingly. In 2022, a new pickup hit the market, the Ford Maverick.
[01:30] It had a base price of $20,000, half the price of the average vehicle sold in the US.
[01:35] There was so much interest that Ford stopped taking orders, and added a third shift to the production line.
[01:40] The takeaway, better foresight is warranted, not just of one's product,
[01:43] but of the industry and related variables. In 2001, a new product,
[01:48] codenamed Project Ginger, hit the market. Backers included Jeff Bezos of Amazon,
[01:53] venture capitalist John Doerr, claimed that the product may be bigger than the internet,
[01:57] and Steve Jobs predicted that in the future, cities would be designed around the product.
[02:01] The product was the Segway. Its inventor, Dean Kamen,
[02:04] believed they'd be selling 10,000 Segways a week. Sales were less than 6,000 a year.
[02:09] The takeaway, know the market. Michael Jackson was working on a new album, Thriller.
[02:14] He liked the energy and creativity of Quincy Jones, and convinced his label, Epic,
[02:19] to bring him on as co-producer. The two sought not to be pigeonholed
[02:22] by any one specific music genre, but to transcend the music landscape.
[02:26] They made one song with guitarist Eddie Van Halen, and another with singer and songwriter Paul McCartney.
[02:30] Rather than aim for two or three singles from the album, they sought to have six or seven.
[02:34] The label believed in the product, evident by their financial backing.
[02:37] They marketed the album for two years, and they flexed on the new cable network, MTV,
[02:41] to see Thriller aired. Jackson's manager said that they wanted to make music
[02:45] to appeal to the masses, and that they did. Thriller sold 70 million copies,
[02:49] and still remains the best-selling album of all time. The takeaway, hard work, a vision,
[02:54] and a team acting in concert, bore fruit. In early 2019, the New York Times reported
[03:00] that Facebook was hoping to succeed where Bitcoin failed. Now two years into research,
[03:05] and with a team of over 50 engineers, led by the former PayPal president,
[03:09] and with the backing of meta-platforms, it seemed destined to succeed.
[03:12] But the project, called Facebook Coin, then Libra, then Diem,
[03:16] was met with pushback from regulators, and Facebook groveled.
[03:19] They said their product would not be released until the regulators were satisfied.
[03:23] Eventually, seeing that there was no way to appease regulators and be attractive to users,
[03:27] Facebook shuttered the product. The takeaway, trying to appease those
[03:30] who will never be your customer, is a fool's errand. So what can be learned from these case studies?
[03:36] Unlike many of the aforementioned products, Dash operates in the digital world.
[03:40] We need to stay abreast of market trends and be responsive. We need to have a tight vision
[03:44] that we execute on efficiently. We need to market effectively from a multitude of angles.
[03:49] We need developer tools that are honed, in short, to be poised for greater adoption.
[03:53] Dash needs to be a usable product in every aspect, and backed by a tight community.
[03:57] - I know adoption's coming. It's gonna come for us.
[04:01] We're not gonna have to go and try to beg and plead for adoption.
[04:06] What we need is something that actually works when the people come running.
[04:11] - Earn the adoption. - Not earn the adoption.
[04:15] We need to be something that's functional so that when, A, the fiat financial system fails
[04:22] and/or is a dystopian nightmare, and B, people start fleeing into Bitcoin,
[04:29] thinking, "Hey, this is the savior. "This is what I've been hearing about."
[04:32] We need to have a clear solution that says, "You thought Bitcoin was the solution.
[04:38] "This actually does work, and here it is." The adoption will come eventually,
[04:45] but we're actually not quite ready for it if the masses stampeded our way.
[04:51] (upbeat rock music) - G'day, g'day, and welcome to "Incubator Weekly."
[05:02] How's it going, co-host Rion? - It's going good, thank you.
[05:06] I just listened to Michael Jackson's "Thriller" yesterday, so there you go.
[05:12] - The best-selling album of all time, right on. - Yeah, not to be, not surprising.
[05:16] - And Jojo, how are you today, sir? - Doing well, how are you all doing?
[05:23] - We're well also. We're keen to show everybody what you have been working on,
[05:30] which is a JavaScript-written web wallet. And I've got to say, this has kind of weirded me out,
[05:40] because I guess I haven't used a web wallet for six or seven years.
[05:46] I used to use blockchain.info, as I think maybe many people did during certain years.
[05:51] And so it's cool to have a web wallet as an option again, and it got me thinking, first of all, why a web wallet?
[05:58] We have mobile phones, we have downloadable clients on desktop,
[06:02] so why a web wallet? - I'll take a stab at that,
[06:06] and then maybe Jordan can answer as well. But the reason that I wanted to focus on a web wallet first
[06:12] is because if you build a web wallet, you can, with technologies that currently exist,
[06:21] you can package that as a mobile app and a desktop app easily,
[06:26] like using the same-- - You mean like the code can be repurposed, or?
[06:34] - Yeah, exactly. So whereas if you built,
[06:37] for example, our current existing Dash Core wallet is a desktop wallet,
[06:44] primarily that's what it's built first as, and it's written in C++,
[06:51] and you can't port that to the browser. But if you build it for the browser,
[06:57] there are a ton of packages and libraries and tools that you can use to package a web,
[07:04] something that was built for the web, into something that can be built
[07:07] for a mobile wallet and desktop. So the vision is that this will eventually be
[07:14] all of those, on all of those platforms. - Okay, okay.
[07:19] And then let's just start looking at it. Can we do that, Jojo?
[07:23] Can I bring up your screen share at this time? - Yeah, yeah, sure.
[07:27] - Okay, let's do it. - Alrighty, so this is what I've been working on
[07:34] for a few months now, and we're using a bunch of the tools
[07:38] that Kool-Aid J86 has built, and they're all built in vanilla JavaScript,
[07:43] so they're not based on any other frameworks, and we're able to generate an entire wallet,
[07:50] we're able to add existing ones, importing via recovery phrase.
[07:54] So I'm actually gonna run through the importing step for both of these,
[07:58] because in testing, I've generated so many recovery phrases at this point,
[08:03] I don't want any more recovery phrases. So it's kind of--
[08:07] - I think you should do one of each, Jojo. - One of each?
[08:11] Okay, I can do that. - Yeah, yeah.
[08:13] I get the impression that you're afraid that we're gonna run out of 12-word phrases.
[08:19] - No, no, no, no. I'm just afraid I'm going to lose track
[08:22] of one that has funds in it. - Okay.
[08:25] Well, let's show 'em both ways so they can see both processes.
[08:30] Sorry, what was that, Amanda? - I was teasing, nothing.
[08:33] - Okay. So the left screen here,
[08:37] I'm going to import a phrase here. I'm gonna say this is Jojo right for my alias.
[08:42] And I'm gonna enter a password here. It's just pass password for encrypting.
[08:51] And so this will encrypt it inside the browser. And then over here,
[08:58] we just need to insert, let's see, I'm gonna reverse this
[09:04] so byte Jojo. And now I've got a new recovery phrase
[09:10] that I have to keep track of. So thanks for that, Rion.
[09:12] - So there's now one last recovery phrase for the world to use.
[09:16] - Exactly. All right, so I'm gonna enter
[09:20] a encryption phrase there or password there. So now we have two wallets.
[09:26] I'm gonna go ahead and edit this and just enter a name here real quick.
[09:33] And I'll save that, and I'm gonna bring this up.
[09:35] So I can fund this wallet now by copying this. And let's see.
[09:43] - So can we slow down a little bit here? 'Cause when I see something happening in the browser,
[09:47] my spidey senses get nervous, probably because I don't really know
[09:52] how the code works exactly. But okay, so first of all,
[09:55] unlike blockchain.info, we're not using username and password here, right?
[10:00] So already there's something different here from what I used to use on blockchain.info.
[10:06] From a very high level, what's the difference here?
[10:09] Why don't you need a username and password? - So all the data is stored in your browser,
[10:16] and it's not backed up to any server. But beyond that, we don't quite have it yet,
[10:24] but we'll have an export option. So you can back up this wallet data,
[10:28] which will include your contacts and all the addresses that you've used thus far.
[10:34] But until, or like if you're concerned about privacy,
[10:42] the only thing we're interacting with is the insight.dash.org.
[10:48] So we're using that to get all of the wallet data. But other than that,
[10:52] it's not storing a full chain inside of your browser. It's just getting the data
[10:59] for the addresses you're interacting with and the contacts you're interacting with.
[11:04] - Okay, and so you, Jojobyte, are not even running a blockchain,
[11:09] a full blockchain node to feed data to this, but this is just using the Insight API?
[11:15] - Correct, yep. - Okay.
[11:17] - And I think that it won't be very hard to just have a custom Insight API
[11:22] or even different Explorer that you could host on your own.
[11:29] So AJ says, "All private keys come from the 12-word phrase. "That's all you need to back up your funds to be safe."
[11:37] And I was thinking about that when Jordan was saying that exactly.
[11:41] So even though you have all of the backup that you need for your funds already with the 12 words,
[11:48] you don't have the metadata backed up. And that's what the backup would be for, so.
[11:56] So I'm gonna go ahead and test sending funding this wallet here.
[12:02] And we'll see if it gets funds in a moment once I get my other encryption passphrase.
[12:10] Let's see. - So then in the interim, I've thought to ask,
[12:15] I don't know, Rion, or if you know the answer to this, but I just thought just this morning
[12:22] when I was chatting with Pete that back in the day, back when Evan was about
[12:26] and talking about his vision for Evo, I remember him talking about usernames and passwords.
[12:33] Can you or anyone in the chat or whatever tell me, is that something that's still supported by platform
[12:39] or are platform apps destined to need these 12-word seeds for interaction
[12:45] or what's on the horizon there? - Yeah, let me do a little bit of a high-level summary
[12:53] of what we're doing here. So Dash Core Group is building Dash Platform.
[13:01] And Dash Platform is going to enable usernames that are globally unique where you'll register,
[13:10] or in the initial phases, you'll request to register. There's nuance there.
[13:15] I think that you can claim a username for, that's called the Dash Pay Project.
[13:20] So that's what I'll refer to it as, the Dash Pay Project is DCG's username solution.
[13:27] And those address, those usernames are globally unique. And initially, I think that you'll be able to
[13:36] just claim one that has both letters and numbers in it. But then there will also be a process where you can,
[13:47] if I wanted to get just like @RyanGull with no names or anything,
[13:53] or no numbers or anything with that, I think I have to request it.
[13:57] And then like the network votes on whether I'm the actual Rion Gull,
[14:03] will the real Rion Gull please stand up kind of style. And that basically allows some time for the network to say,
[14:12] if I'm trying to register Nike or Apple or something like that,
[14:18] or I'm clearly not Nike or Apple, the network doesn't want to allow that right away.
[14:25] So that's DCG's Dash Pay product. And we're building something different.
[14:31] We're building a username system that's not globally registered on Dash Platform.
[14:37] And so it has nothing to do with Dash Platform at this point. When Dash Platform is ready,
[14:42] we will be able to have a migration path or an update path to having our usernames be like register
[14:52] as Dash Pay usernames. But that's not something that's on our roadmap yet
[14:56] because Dash Pay is not done yet and probably won't be done until Q1 of next year
[15:01] as far as I can tell. So in the meantime,
[15:05] we're building something that's different in the sense that when we are using usernames
[15:12] and we're not sure exactly what we're gonna be calling those,
[15:15] but right now we're calling them aliases just so that we can distinguish between a username
[15:24] and we don't want to confuse the community. We're calling them aliases.
[15:28] So our aliases are just local to the wallet itself. They're not registered anywhere.
[15:37] They're local to whatever storage mechanism your wallet is using.
[15:43] So in the browser, it's storing that username and the username of your contacts in the browser itself.
[15:50] And there are suggestions. So we'll show this process in a little bit,
[15:56] how you actually make a contact request. So when Jojobyte, sorry,
[16:07] when Jojobyte requests a username contact with me, then he will have a requested,
[16:20] like preferred username I think is the term that it's used. And I think there's a standard behind that.
[16:26] So that's why it's called preferred username instead of preferred alias.
[16:30] But yeah, that's not registered anywhere except for our respective wallets.
[16:38] So maybe we should show the process first. I think that might be a good point
[16:42] to jump back into the demo here. - Sure.
[16:46] So we've got funds in this wallet now, as you can see, and we can go ahead and pair these two wallets.
[16:53] So I'll go ahead and open new contact here. We'll open it here.
[16:58] So I need the data from this QR code, but it's also right here in this field.
[17:03] And you can just copy the URI like that. And I can paste this one over here.
[17:08] And then I can do the same thing, but in reverse and paste this one over here.
[17:12] And so with adding contact, we now have these two wallets paired.
[17:20] So Jojobyte is going to ByteJojo and Jojo is going to Jojobyte.
[17:26] And so now with them paired, we should be able to send funds.
[17:31] So I can go in here and you can select an alias, or if you have a dash address,
[17:39] you should be able to put a dash address in and still send funds that way as well.
[17:46] But with this method, I can select ByteJojo and then I'll enter a small amount to send here.
[17:54] - And this is real dash, yeah? This is not test dash that we're seeing?
[17:58] - The real dash, yep. So this is just confirming.
[18:03] I want to send that much to this other wallet. So I'll click send here.
[18:09] And let's see. There we go, there it is.
[18:15] - Oh, you didn't send enough to have it be part of the highlighted.
[18:19] - Yeah, okay. - Well, good news, I can send some more.
[18:25] - Yeah, go ahead. - And I would like to note that it was my assumption
[18:29] that I would need to type the 12 words back in every time I wanted to access this wallet
[18:37] 'cause I now have an account also, but I was surprised when I went to log back
[18:41] in the second time that the 12 words had been saved in my browser
[18:46] and all I needed to do was reenter my decryption key. So that was nice and convenient.
[18:52] I can see, 'cause I know that there's been a bit of chatter recently of like, oh, sorry that my app has,
[19:02] you have to use 12 words, you have to use 12 words, sorry about that.
[19:05] But shoot, if my browser saves it, provided it's a private session or private machine,
[19:10] that's not so bad. - Right, and some people might remember
[19:17] trying out Eldorado, for example, using Maya with Eldorado.
[19:22] And I think that there was something where you had to keep entering,
[19:28] I don't think it was the 12 words, but there was something where you had to keep entering.
[19:32] The reason that that's doing that is that it's not saved in the browser storage,
[19:37] and so you have to keep reentering it. So we decided, obviously, it's a better user experience
[19:44] to not have to reenter that. Jordan, do you want to continue with your demo here then?
[19:52] - I would love to. However, I'm actually getting a transaction lock,
[19:57] so I'm not able to send more of the funds right now. By the way, this is very experimental,
[20:04] so don't move all your funds into these wallets. Just everyone-- - Yeah.
[20:09] - Fair warning. - Yeah, we are not ready with this.
[20:14] We are kind of moving slowly on this, partly due to funding and partly due to just,
[20:20] we don't have full-time employees at the incubator. We just do work as we can,
[20:26] and based on scheduling of different people. So it's a little bit of a slow process,
[20:34] but that's kind of how the incubator works. So yeah, I guess we can go back to the, let's see.
[20:42] I'm not sure who this comment is from. Seven months ago, this wallet was discussed.
[20:48] Curious search. We're building our first wallet.
[20:52] - It's a reference to the first time when we announced this project, actually.
[20:56] - Yeah, yeah, yeah. - But there's something I want to discuss,
[20:59] which was the radical claim that AJ just made in the prior comment.
[21:03] Pete, would you bring that up? That was kind of insane.
[21:06] - Yeah, actually, let's see. It's perfectly secure and perfectly decentralized this way.
[21:13] It's more secure than a hardware wallet. I mean, it depends how you're using these things.
[21:20] However you secure your 12 words, there are pros and cons to each,
[21:30] but if you secure your 12 words properly without a hardware wallet,
[21:35] I would say I would agree with that claim that it's just as secure.
[21:38] I don't know exactly what the claim was. It was more secure.
[21:41] That's a bit of a subjective claim, but yeah. Did you have a specific question about that, Amanda?
[21:51] - Just the notion that I guess anything online, particularly in a browser,
[21:58] I don't know why browsers sketch me out. - Well, they do have a bad rap
[22:03] for being very insecure places, so that's why you probably do feel that way.
[22:08] - Maybe that's justified. Okay.
[22:10] Okay, so briefly, Jojo, will you tell us, what do you mean when there's like a transaction lockout?
[22:19] Just what does that mean? - Just like in any sort of Dash,
[22:24] if I suspect that it's adding up the values wrong and trying to,
[22:32] because I had slightly more funds before I sent, I think the cash layer that I have
[22:38] is cashing funds that have now been sent. And so when I'm trying to send,
[22:43] it's trying to send funds I don't have anymore. And so it's going up.
[22:47] You can't do that. And so this is why it's experimental.
[22:52] We're finding this stuff out. The sending feature is only available as of two days ago.
[22:59] And so it's very new to be able to even send. So there's some bugs and stuff we need to work out.
[23:05] So that's apparently one of them. - And I'll also say one of our strategies with this wallet
[23:10] is we are trying our very best to use as few dependencies as possible.
[23:18] And so that has pros and cons. One of the pros is obviously
[23:23] the fewer dependencies that you use, the more secure and performant it is in general.
[23:29] So by dependencies, I mean, we are building this in pure JavaScript, CSS, and HTML.
[23:37] There are no UI frameworks involved. We're not using React or Angular or Vue or Svelte
[23:44] or Solid or any of those things. And that has, like I said, it's pros and cons.
[23:52] One of the cons is that it's more difficult to develop this way.
[23:57] It's developing, it's like the browser version of very low level development
[24:03] because you have to create all of your own user interface updates.
[24:10] That's what frameworks like React and Angular are supposed to do for you.
[24:15] So there's a ton, there are huge businesses that are built on building these frameworks.
[24:22] But if you can build it without that, then there are benefits to that.
[24:26] But the cost is that it does take a little bit longer to develop these things.
[24:31] You have to have a different skillset. Jojobaite's one of the better,
[24:36] one of the only people that actually is even attempting development like this.
[24:41] There are very few developers that they get this low level in the browser.
[24:45] And along with not just the user interface updates, but also state updates is very, very tricky to do as well.
[24:56] And you're not using any state libraries as well, right? Jojobaite?
[25:02] - Correct, yeah. To add to your point, I would say
[25:07] that when you add and build on top of other frameworks, so many of them nowadays include their own tracking
[25:15] and analytics literally in the code. And so it's hard to build something without any tracking.
[25:22] And at least in this wallet, you should never get like a warning from your ad blocking
[25:28] saying something was trying to track you because we've built it all by hand
[25:33] and made sure there is no Google Analytics in here. There's nothing tracking when you enter your recovery phrase
[25:39] and sending it off to Google Analytics. And yet some of the frameworks you could build upon
[25:44] if you do choose to go that way would have Google Analytics in.
[25:49] And so that is an advantage. - Is that because the origin,
[25:53] like the people you're getting the libraries from or whatever they want to know who's using it
[25:58] and where to sell their product better? - Yes, correct.
[26:03] And you can also have, it might not be Google Analytics type of stuff,
[26:08] but they might include stuff for bug tracking. And so that will also track.
[26:13] And if the scripts throw an error, that might report back to the library maintainer
[26:20] or something. And so if you care about that kind of stuff,
[26:23] you might not want your, like you don't know,
[26:28] like if it did break on your recovery phrase, it could throw an error out to someone
[26:32] you don't even realize it's sending stuff to, and it might include your recovery phrase.
[26:37] So by doing it from scratch, we know it's not sending any of that.
[26:41] All of this is open source, by the way. So anybody can look at the source code already
[26:47] if you want to help out, that's great too,
[26:51] adding your pull requests and whatnot. Like Jojobite said,
[26:55] this is very alpha level at this point still. We're just getting the contact feature.
[27:02] We're demonstrating that, that it is working.
[27:04] The payment feature is working. But again, like state updates
[27:09] where if something changes on the blockchain, the user interface automatically updates.
[27:14] That's stuff that we're building like on our own because we're not using libraries for the most part,
[27:21] as few as possible at least. So just to get back into the demo again,
[27:28] I wanted to explain a little bit more high level what is going on under the hood
[27:35] with this contact feature. So maybe we could,
[27:39] Jojobite, can you pull up the demo again? - Yeah, and I still want to be added as a contact
[27:46] if at any point we can work that out. - Yeah, so let me explain this just conceptually first.
[27:53] So we are using HD wallets and the contacts,
[27:59] each time you make a contact with somebody, you're getting their XPUB
[28:06] and your wallet is generating several addresses in advance to use for them.
[28:12] So it's kind of the same, in a lot of ways it's the same technology
[28:17] as the Dash Pay, DCG's Dash Pay, other than the fact that we're not storing any data
[28:24] and doing contact requests through Dash Platform. It's all just using standard
[28:33] existing BIPs, I will say, not even DIPs.
[28:39] And it is using those XPUB features. So you are getting a new,
[28:45] when you send a new payment to and from each contact, you're sending it to a new address for them.
[28:52] So I guess, should we go into adding you as a contact, Amanda,
[29:02] or did you have something else to share? Do you want to talk about the URI more, Jojobite?
[29:07] 'Cause we haven't really done that. - Yeah, we can talk about the URI when,
[29:14] and I suppose we can, Amanda and I can add each other here.
[29:18] So with this URI here, which you can't really see it very well.
[29:25] Let me see if I can find a way to make this bigger. Well, I don't think zooming in is gonna help much.
[29:32] - This control plus, would that work? - Well, I'm already zoomed in pretty.
[29:37] So it'll make it bigger, but not show more. That's the real issue is I can't show more of the URI.
[29:45] And if I paste it in the contact address, there's functionality here that parses the URI
[29:52] and grabs the address or XPUB and various attributes like the contact information.
[29:58] - Maybe you could just open up like a notepad or something and paste it in a text document
[30:03] and then zoom in on that. Is that--
[30:06] - Let me see if that works. - 'Cause that'll give people an idea
[30:11] of what kind of data is transferred when you're sending these contact requests.
[30:19] - Hi, ES, tell us who you are. (laughs)
[30:29] - Okay, yeah, now zoom in as far as you can on that one. - Yeah, let me see if I know how to do that in here.
[30:37] - Maybe try-- - I'll move it back in a second.
[30:43] - And the QR code, by the way, the QR code is just the graphical depiction
[30:52] of the same text. So that's what you're seeing there.
[30:56] - Yeah, sadly, Control + is not working in this. - Yeah, I think I remember that from Apple products.
[31:06] It's not always the same shortcut. - Trying to find it real quick.
[31:11] - WordPad online. - Okay, here we go.
[31:23] - Oh, right on. That makes two of us.
[31:27] Glad you're here. Hey, that looks better.
[31:33] - Yeah, and I found it. I just have to modify it manually.
[31:39] So let's do that. All right.
[31:43] - Now we're talking. - Maybe I'll go, I guess it's too large.
[31:49] Let's go a little smaller. - That's good, it's fine.
[31:53] - All right, yeah. So the XPUB is, oh, wait, no.
[31:56] XPUB is mostly on the screen now. There we go.
[31:59] So what we're sharing right now is the initial address, which if you know about HDPaths,
[32:07] this is the account index zero and the address index zero with a use index zero.
[32:13] And so that's essentially the very first address that's generated.
[32:18] And it gives you an XPUB to share. And so this is an XPUB to my wallet
[32:26] or to an index position in my wallet that I'm sharing with you.
[32:32] And if you send funds to it, I'll be able to access those funds.
[32:38] - And then are those unique for each time you share them with someone
[32:42] so that no one person can know every future address that is yours or, remind me how that works.
[32:49] Okay. - Yes.
[32:51] - The XPUB is something that you can derive a lot of addresses from.
[32:59] So in a way, these really shouldn't be completely public if you want privacy.
[33:06] So it depends on how you want to share this information. So the best way is if you're in person
[33:16] and you scan the QR code and that way there's no third party medium
[33:23] that this is being transferred over. AJ is saying that they are pair wise, not public.
[33:30] I guess that's just the terminology that you would use for that.
[33:33] And so I wouldn't want to, obviously we're just doing demos here,
[33:40] but I wouldn't want to share my XPUB completely publicly because I don't want people knowing all the addresses.
[33:48] That kind of defeats the purpose of doing HD, sending to a different address
[33:56] every time you do a transaction. That defeats that whole purpose.
[34:00] So you do want to share these in a way that you and the person you're contacting
[34:06] are comfortable with. Now, some people don't care about privacy that much
[34:09] and so they might as well just send it over social media or whatever.
[34:15] You're not gonna lose funds that way. You just lose privacy that way.
[34:18] But being in person is the best way. If you share it over an encrypted medium
[34:24] like Apple's text messaging, if you're sending to another Apple user,
[34:33] I think that's encrypted. And so even Apple can't see that data.
[34:40] You'll see that in a blue message, for example, instead of a green message.
[34:43] Yeah, this is an important point is that each contact gets a different XPUB.
[34:50] - So I was gonna say, what prevents if I send my XPUB to Rion
[34:53] and my XPUB to Jojo, what prevents both of you from sending me a payment
[34:57] at the same address? Okay, but-
[35:00] - Nothing. So that's exactly what could happen.
[35:02] The wallet does not prevent that. - The wallet doesn't prevent that,
[35:08] but the wallet is designed so that if I share my XPUB with Amanda,
[35:14] then the next time I'm sharing an XPUB and I wanna contact,
[35:17] I wanna make a contact with Jojo by it, it's not gonna give me,
[35:21] it's not gonna give her that same XPUB for me. It's gonna give her a different one.
[35:26] - Okay. - Correct.
[35:27] But for example, in our case, if you share it in a group chat with multiple people
[35:34] and you have multiple people use that same XPUB, like I'm showing this here,
[35:39] I could have people pairing with this, anywhere in the world right now,
[35:44] and then anyone sending to that XPUB would be colliding with addresses essentially.
[35:51] So these should be unique to the contact parent, but it's not the worst thing ever.
[35:58] You shouldn't lose funds using an XPUB, but I know we've discussed using an XPRIV,
[36:05] and if for example, you shared an XPRIV like this
[36:08] and multiple people paired to it, from what I understand is,
[36:12] someone with an XPRIV could recover funds having access to that XPRIV.
[36:17] So that would be one advantage to using XPUBs if you were to share something like this in a group,
[36:24] it wouldn't be ideal, but it also wouldn't be like two or three people
[36:29] could take funds from that contact. - Okay.
[36:34] And so what are we seeing now highlighted on your WordPad? - So I just broke this up a little bit,
[36:43] and what it's showing is we've got the XPUB, that's this second line here.
[36:49] Well, I guess I didn't actually break that. There you go.
[36:54] So the XPUB is the XPUB, so the XPUB is this second line,
[37:05] and this is a unique identifier. Then we've got our preferred username,
[37:11] and the reason we're not saying alias, we're saying preferred username,
[37:16] is this follows the OIDC claims. That's close to the name.
[37:22] I don't know the exact name off the top of my head, but it's following their claim process.
[37:27] And then name is also one of those, so that allows us to set a name.
[37:32] And then this scope is also specific to the dip that A.J. O'Neill there made.
[37:41] - Okay. - I guess he's saying XPUBs are safer
[37:45] because the funds still can't be taken back if they're received,
[37:49] but they can be recovered by sending party if the funds are lost.
[37:52] And so my counter to that is the exact thing I just said. If you shared it in a group chat,
[37:58] anyone who paired with that would technically have the XPUB,
[38:02] so a third party could take the funds because any of those people would have that XPUB.
[38:08] But as long as it really was one-to-one, you paired with someone and only they had it,
[38:13] then yeah, it would be good because if you sent funds to it,
[38:16] and for some reason I didn't receive it, the person sending it could recover.
[38:22] So that would be the advantage. - That's not something that we're building into the wall
[38:26] is exchanging XPUBs at this point. And we have no plans to do that.
[38:31] AJ thinks out of the box a lot, and he sometimes makes claims
[38:36] that do sound a little outrageous to people in this space. I like that.
[38:44] I like that out of the box thinking, but just know that we are considering these all
[38:52] with a grain of salt, all those kinds of things. So, go ahead, continue.
[38:59] - Okay, so, and then the scope just defines what each of these variables are.
[39:05] So there's an XPUB, that's right there. There's a sub, which is right here.
[39:09] That's the unique ID. There's the preferred username, which is here.
[39:14] And then there's the name. That's all scope does is it defines
[39:16] what you're sending through so that like anyone implementing it should know.
[39:22] And so all of this dash URI, I haven't actually tested pasting this in,
[39:28] but this portion of the dash URI, you can paste into a dash core or dash mobile wallet,
[39:36] and it should work. - And that's why we have that first address.
[39:43] Normally you wouldn't need that, but to be backwards compatible with other wallets,
[39:47] it should work that way. Even if you have a wallet
[39:50] that's not respecting these other data points. So.
[39:56] - And so this dash URI, that's what this QR code is. It's literally this dash URI encoded into a QR code.
[40:05] And so when you pair with that, we do have the scan feature,
[40:09] although I don't think I have a camera hooked up, so that won't work right now,
[40:13] but you should be able to scan the QR codes and load a contact that way as well.
[40:19] And I believe it should also work for sending. But that's, this is the gist of what our URI is doing.
[40:28] It should be an extension. And I think these extra fields
[40:31] that dash core doesn't support should just be ignored by dash core,
[40:37] unless they, for example, decide to implement these things. - And just so people know,
[40:43] Joseph, I click on the QR code, just so people know that when you click on that,
[40:47] it does get bigger. - Yeah, so if you're having trouble scanning it,
[40:51] you're able to click on the QR code and if you can't scan that, that's a different issue.
[40:57] - I'm gonna actually try to scan that right now. - Oh yeah, you want me to leave it up there?
[41:01] - For mobile, okay. - Just leave it up there for a little bit.
[41:04] Yeah, it scans just fine. And if actually, if I scan that,
[41:09] it opens up my dash wallet. - Yeah, does it fill out the address correctly?
[41:14] - I don't know if it would, but it didn't because I have no funds
[41:21] in my mobile wallet at this point, so maybe it would if I had the funds
[41:25] or something like that, but I'm not sure. We'll have to test that later.
[41:29] - Yeah. - Okay, so Joseph, I still want to be in your contacts list.
[41:35] And so I, on my end, I have clicked copy URI and I'm not getting this really long thing
[41:41] that you're getting, I'm getting just the shorter one, if I can maybe show that for a moment.
[41:46] So when I click copy URI, what you see there is all I got.
[41:52] You're in edit profile, not add contact. So if you want to fund your wallet,
[41:58] if you have no funds in there, you can go to your edit profile.
[42:02] I can show that real, well, yeah. So if you go to edit profile
[42:07] and you need to put funds in the wallet, that's what Amanda just showed is that it just,
[42:13] so you can drop and paste, like I was saying, into Dash Core or mobile wallet or, you know,
[42:22] any other- - That's for funding your own wallet.
[42:25] - Got it, so I just, I clicked the wrong thing. Okay, so now in the private chat, Jojo,
[42:29] I am sharing the contact URI, if that. - All right, let's see.
[42:36] All right, and then I'll share this one with you. - Jojo Byte's copying the URI that Amanda sent
[42:45] and he's going to enter that into his wallet. - I'm going back to mine.
[42:50] I pasted that in mine. It's got the XPUB she just shared with me,
[42:54] the name she specified, Amanda B. Johnson, and ABJ. - Okay, and I see you in my contact list now.
[43:01] - Yep, and so I just added that and I've now got Amanda in my contact.
[43:07] - So send a payment to Amanda now. - Yeah, maybe you should send the whole balance
[43:12] just to test. (laughing)
[43:16] Let's see if this works. All right, it's out of my hands.
[43:36] Hope it's in yours. - Okay, I'm watching it.
[43:40] Here, I'll bring mine up on screen. - You can also click the balance right now.
[43:45] - So we were having some, so if you click just the zero, it should refresh it.
[43:52] - Hey, there it is. - There you go.
[43:54] - Okay. - Yeah, and that's one of those things
[43:59] that we should automate so you don't have to do anything and have the balance refresh.
[44:05] But again, that's one of those things that it just takes some time
[44:08] to develop that kind of responsivity, if that's a word. - Well, so what I started to say
[44:14] is I had that in there and it was partially working, but there was one or two scenarios
[44:20] where instead of just adding the new or subtracting the new balance,
[44:25] it was doubling the balance. And I think it was in the instance
[44:29] that if you sent all of the coins you had, it would then give you the new balance,
[44:36] but I couldn't see any way of indicating that you no longer have these coins,
[44:41] so you should subtract all the coins, at least through the socket API.
[44:45] So I removed that temporarily because I haven't figured it out yet,
[44:51] and I didn't want people going, "I just doubled my funds."
[44:55] - Yeah, yeah, that's a relatively simple thing to fix when you have the time.
[45:02] We just didn't have the time. - Well, I guess I just have a final question,
[45:09] provided that the demo is more or less wrapped, which is like what remains to be done
[45:16] or what remains to be done before you might say, "Okay, we're no longer calling this alpha
[45:22] "and be careful," to like, "Hey, it's cool, use it now." - So right now we've got this mapped out
[45:32] and I can pull it up here actually, let's see. - Oh yeah, that's right, your roadmap, please.
[45:37] - Yes, so I have a roadmap that we developed for the wallet here.
[45:42] So let's see. I want that bar to go away.
[45:56] And in any case, I guess it's not going away, but I'll zoom in.
[45:59] - Yeah, that's good. - Okay, so we've got a lot of this accomplished.
[46:03] Actually, I haven't checked some of these off since my last update, so some of this might be done.
[46:12] We've really just been trying to flush out the contact pairing and the funding,
[46:18] which now funding is at least partially working. We've got requests also.
[46:23] Oh, we didn't show that, I suppose I'm still sharing. So we also have the ability to request funds.
[46:30] And if you don't specify anything, that will go to your main wallet
[46:34] and this address should change each time. So that address changes every time
[46:41] if you don't specify anything. However, if you were to specify a contact and request,
[46:47] it should show an address for that contact specifically. And then you can also specify an amount here
[46:56] and add that to the request. And so then it adds the amount on the end of the dash URI,
[47:02] and that's compatible with Dash Core and Dash Mobile. So we've got that working.
[47:09] I'm sure there's some things that need to be flushed out, but we're closing up on finishing stage one here.
[47:15] Once stage one is complete, as in, I believe I finished everything,
[47:20] we'll probably need to do a round of bug fixes and just have people test and report whatever fixes happen.
[47:28] And then we would get into stage two, which stage two would include transactions,
[47:34] which right now we have no way to display transactions. You would literally have to look up every address
[47:40] in Dash Insight Explorer or whatever, or anything like that. But we would also have the wallet balance
[47:51] for fiat currency. So you could see if you want USD
[47:55] or British pounds or euros or whatever. And then we would also improve some of the settings,
[48:04] which as these are all listed here in the public repository for the wallet UI.
[48:10] And so we would improve the settings as well as we would have multiple wallet support,
[48:16] which would translate to, if you have multiple recovery phrases,
[48:21] you could either add them under different aliases. Say, if you have one wallet you treat as a savings account
[48:28] and the other that you use to spend with friends, we would have support for multiple wallets like that.
[48:35] And that would also include, say you create a wallet on your laptop or your desktop
[48:44] and that has a recovery phrase, and then you're out with friends and you wanna show,
[48:49] send them Dash and you forget, you never imported that wallet
[48:53] or backed up the recovery phrase somewhere when you're out and about,
[48:57] you could generate a new phrase and later reconcile those. So both wallets have both phrases in them.
[49:06] And then you would be able to see funds and you would be able to connect to contacts
[49:10] who you met someone and you only had your phone and you made a contact,
[49:15] you'd be able to import them and track them and send funds regardless of where,
[49:21] like which phrase they're using. And it would tie back to whichever alias you wanted.
[49:27] And then we have contact payment share features improvement. So right now, like this only shows a QR code
[49:37] and the Dash URI, we would also have things that automatically attach the QR code to an email
[49:44] or insert it in a text message and that kind of stuff. And then set fund denomination
[49:54] for sender request payments. So in other words, I wanna send $20
[50:00] and then it would translate that to whatever the current value of Dash is in dollars.
[50:07] And so that would be stage two and then there's stage three and stage four and five.
[50:15] But all of these other stages will probably be, they're more fluid.
[50:22] They might be updated as we near like mid or end of stage two,
[50:28] we might refactor or decide, actually, this is pretty good,
[50:33] let's get it working with a towery wrapper so you can install it on your desktop type of thing.
[50:38] So we might reorder these, but this is at least the plan as it stands now.
[50:45] - And just to kind of emphasize some of those things that you didn't mention,
[50:50] there are one of the things that I wanna use this wallet for
[50:54] is being able to just basically add every feature that we have in Dash.
[50:59] This will be a Dash specific wallet. Everything that we want added in Dash,
[51:05] whether that's the Dash direct successor that's coming or Maya transfers or like adding liquidity
[51:18] or adding savings to Maya or Crowdnode, all these integrations,
[51:26] once you get a good foundation to work with, then the integrations are relatively,
[51:33] they're not simple, but you can add integrations at will.
[51:40] And this being a JavaScript-based wallet, in theory, should help the speed
[51:49] of adding those kinds of integrations because there are literally millions and millions
[51:54] of JavaScript developers where there are only, not gonna name any numbers here,
[52:01] but there are far fewer C++ developers that would be willing and able to dig into Dash Core,
[52:08] for example, and try to do a PR for a pull request to add some kind of Crowdnode or whatever integration
[52:17] or spritz, for example. That's one thing that I just barely started using recently
[52:23] and it's a phenomenal user experience. So it'd be interesting to have a native integration
[52:31] with spritz to pay bills. I don't know if they have an API,
[52:36] but that's just an example of when you have an integration that adds Dash, make it a native integration
[52:43] right into the wallet. And that's something we definitely,
[52:47] Maya would be one of the first things that we add. And that's just an example,
[52:53] but hopefully there would be a lot more different kinds of integrations that we could just add very quickly
[52:59] as we have them. - Right on.
[53:02] Okay, well, it seems like we basically covered what we needed to cover.
[53:06] Thanks especially for going over the roadmap, Jojo, that cleared things up.
[53:13] Any final words from either of you gentlemen? - Oh, I forgot to say mixing.
[53:17] That's another feature that we like to add as well, having mixing right in the browser.
[53:23] That would, when you combine that with Maya, that is a killer feature that I think a lot of people
[53:30] are interested in where you could swap Bitcoin to Dash, mix the Dash,
[53:38] swap it back to a different Bitcoin address, all in one seamless user experience application.
[53:44] - That's so feasible. Now, just hold on just one second there.
[53:48] How many times have we been tantalized with having mixing available to us
[53:53] somewhere outside of Dash QT? Are you being serious?
[53:58] Like, is there any reason to believe that that is actually possible and might happen?
[54:02] - Well, we've already done a fair amount of work on it. The only thing hanging us up really,
[54:08] I hate to say it, is funding. So that's really the only thing that's slowing us down
[54:13] on these kind of things. There's only so much we can do in the incubator
[54:17] with the amount of funding that we have. So I'm hoping that that picks up at some point
[54:23] when we have a bigger treasury to work with, but that's kind of the hangup right now.
[54:28] But we are working on it, and we've made some pretty good progress.
[54:33] And I've heard, though, that DCG is now adding mixing to the existing mobile wallets.
[54:41] So that's good to hear. And depending on...
[54:44] Yeah, they may actually have that done before we can get ours done, but I'm not sure.
[54:53] It just depends on a lot of things. - Well, my goodness.
[54:57] Okay. - Mixing in mobile is coming, is the bottom line.
[55:00] - Okay, right on, right on. That'll be great.
[55:03] Joelle will be glad to hear that. Okay, well, thanks for joining us today, everybody.
[55:08] And that is all we have for you. And we look forward to seeing you next week, yeah?
[55:14] - Yep. - Good. - Bye, everyone.
[55:16] - See you all. - Bye. - Bye. - Bye.