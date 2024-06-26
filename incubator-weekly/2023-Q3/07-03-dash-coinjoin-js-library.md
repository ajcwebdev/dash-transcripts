---
showLink: "https://www.youtube.com/watch?v=oGkwON5EQ58"
slug: "dash-coinjoin-js-library"
title: "Javascript Library for Dash's Coinjoin"
publishDate: "2023-07-03"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/oGkwON5EQ58/maxresdefault.webp"
---

Dash developers are close to completing a JavaScript CoinJoin library for enhanced privacy in web and mobile wallets.

## Episode Summary

tl;dr: The episode discusses the progress made on creating a JavaScript CoinJoin library for Dash that will enable enhanced privacy features in web and mobile wallets. Senior developer William McFallin demonstrates how the library can connect to a masternode, initiate CoinJoin traffic, and is close to completing a full mixing round. The library is split into a client-side portion for the browser and a backend node.js portion to handle the networking aspects that browsers cannot currently do. Once complete, any JavaScript-based Dash wallet will be able to easily integrate CoinJoin functionality. There are also future plans to leverage this work for a web/mobile wallet that can mix other coins like Bitcoin through Dash.

## Chapters

00:00 - Introduction and Beginning of Episode 
Discusses the arrest of Tornado Cash developer Alexey Pertsev and how the modern day freedom fighters are coders writing privacy-preserving software.

02:56 - Guest Introduction and CoinJoin Library Background
Introduction of guest William McFallin and background on his work creating a JavaScript CoinJoin library for Dash. The library will enable CoinJoin in browser, mobile and desktop wallets.

13:43 - CoinJoin Library Progress Update
Will presents slides detailing the progress made on the CoinJoin library. The server-side SDK can connect to a masternode, initiate CoinJoin traffic and is close to completing a full mixing round.

22:19 - CoinJoin Library Demo
Will demonstrates the current state of the CoinJoin library running three separate instances that connect to a masternode on a regression test network. The demo shows the instances being accepted into a mixing queue and the masternode verifying and mixing the transactions.

31:16 - CoinJoin Library Code Walkthrough  
A look at the GitHub repository containing the CoinJoin library code, which is split into a client-side portion and a backend node.js portion due to browsers' inability to implement TCP sockets.

## Transcript

[00:00] (upbeat music) What did you do on Wednesday, April 26th, 2023?
[00:05] Well, it may be tough for you or I to pinpoint exactly what unfolded in our world on that date.
[00:09] It is a date that will be remembered by Alexei, or Alex Pirsev,
[00:13] because on that date, he was uncaged. For the first time in nine months,
[00:16] he was able to go home with his partner, Zina Malik, and sleep in his own bed.
[00:20] Last August, on the 10th, to be specific, 29-year-old Pirsev had been snatched up
[00:24] by strangers in the Netherlands. What had Pirsev done, you ask?
[00:28] He had merely written code. Open-source code used to create
[00:30] a decentralized mixing service called Tornado Cash that sought to bring some amount of privacy
[00:35] to the Ethereum blockchain. Bitcoin is really bad on privacy.
[00:39] I think the only people who do it worse, actually, are Ethereum.
[00:42] And for that, he was, and still is, being harassed. He's being told he must wear an ankle monitor,
[00:47] and he is told he will have to appear in court. Mind you, Pirsev is not accused
[00:50] of harming a person or property. Rather, he's accused of helping to create a tool
[00:54] that some bad actors used. There are a lot of neutral tools
[00:58] that can be used by criminals. I mean, just think of the internet.
[01:01] I mean, that's something that's used by criminals every day, but we don't get rid of the internet.
[01:04] So why did some people in the Netherlands decide to target Pirsev?
[01:08] Perhaps as a favor to their friends in D.C.? Because it just so happened
[01:11] that two days before Pirsev was kidnapped, bureaucrats 4,000 miles away in Washington, D.C.,
[01:16] employed at the Office of Foreign Assets Control, a division of the U.S. Treasury's office,
[01:20] added 45 wallet addresses to their specially designated nationals list,
[01:24] which they then claim prohibits 330 million other people, those within the political boundaries of the United States,
[01:30] from engaging with. The wallet addresses were those integral
[01:32] to the operations of Tornado Cash. This specially designated nationals list
[01:36] typically includes individuals, aircraft, and vessels. Listing wallet addresses is fairly new territory.
[01:42] The only related action happened a few months prior when those Treasury employees sanctioned Blender.io.
[01:47] But the targeting of Tornado Cash was new because it is decentralized
[01:50] and relies on code on smart contracts to execute. Almost immediately, centralized entities
[01:55] that had anything to do with the sanctioned Tornado Cash all complied with the dictates
[01:59] of the Treasury office employees. This targeting of a coder and of open source code
[02:03] has not been without pushback. The U.S. House Majority Whip, Tom Emmer,
[02:07] shared his letter that he sent to Treasury head, Janet Yellen, in which he noted that technology is neutral
[02:12] and privacy is normal. Colin Post, writing at The Block,
[02:15] called the targeting of Pirsev and Tornado Cash a major escalation in global enforcement
[02:20] against decentralized protocols. - What's your latest thinking
[02:23] on the sanctioning of Tornado Cash? - I think members of the public, certainly,
[02:30] they don't even know that this happened, but members of the crypto community
[02:35] largely aren't taking this seriously enough. This is absolutely a do or die moment.
[02:40] - In October, the D.C.-based Coin Center filed a lawsuit against what they perceive
[02:43] as an overreach of Treasury office powers. They acknowledged Ethereum's transparent public ledger
[02:48] and the desire of some users to have privacy using Tornado Cash, which nobody controls.
[02:53] Some have framed the actions against Pirsev and Tornado Cash through the lens of free speech.
[02:57] - Ever since the Bernstein v. U.S. hearings of the 1990s, one is protected by the First Amendment
[03:03] when publishing open-source software in the same way one is protected when publishing a book.
[03:08] - But that is not the case in the Netherlands. - Here in the Netherlands, one can actually be detained
[03:12] for writing open-source code that criminals take advantage of.
[03:16] - It's a question whether you can be complicit to a crime, whether you facilitated a crime
[03:21] by writing such an open-source code. - This is undoubtedly why Semenov and Storm,
[03:26] the two other main Tornado Cash developers, have not been targeted,
[03:29] as they reside not in the Netherlands, but within the political boundaries of the U.S.
[03:33] Despite all the saber-rattling and the extended caging, Pirsev has not been charged with a crime.
[03:38] He has merely faced allegations. Though the press release issued by Treasury employees
[03:42] claims that their aim is not to punish, but to bring about a positive change,
[03:45] that seems disingenuous. Indeed, an unnamed top dog at the Treasury
[03:49] was quoted in the Financial Times as stating, "We do believe that this action
[03:53] will send a really critical message to the private sector." In other words, they hope to cause a chilling effect
[03:58] to cause developers to self-censor. A month after Pirsev was encaged,
[04:02] he took the stage briefly at IFDAM. (audience applauding)
[04:07] - Thank you very much. It was so hard time for me.
[04:11] I really appreciate your support. - Where he introduced his lawyer.
[04:17] - There's a misconception that Tornado Cash is aimed at money laundering.
[04:21] I want to make clear from the start that Tornado Cash is a privacy data tool software.
[04:29] - So while some in the space continue to look to the people who are doing the targeting and harassing.
[04:33] - We're hopeful that the courts will see that OFAC did overstep their authority.
[04:41] - Others have suggested a more strike the root route. - You should have levels of privacy protection
[04:47] baked into the protocol. And this prevents the kind of tomfoolery
[04:53] that we see the US government beginning to engage in with things like OFAC and Tornado Cash.
[04:58] - As the transcendentalist Henry David Thoreau encouraged, "Live deliberately."
[05:02] Does it make sense to use the currency that empowers those at the office of the treasury
[05:06] or those that kidnapped and caged and are threatening Pirsev in the Netherlands?
[05:09] Or might it be better for ourselves and all of humanity if we use decentralized options
[05:13] that offer privacy at the protocol level? - The cards are about to fall on the table.
[05:18] We need to be ready. We need to do the best we can to respond to events
[05:23] as they occur and try to make the world a little bit better. (upbeat music)
[05:39] - Hello, and welcome to "Incubator Weekly." That was a relevant newsreel
[05:45] for what we are talking about today. Is it not, Koho Thrine?
[05:48] - Honestly, it makes my blood boil. Everything about this story really pisses me off.
[05:59] I guess I'm just gonna go off on a little tangent here. Not a tangent, but a little rant.
[06:10] This weekend is the 4th of July weekend, Independence Day here in the United States.
[06:17] And it's actually tomorrow, or actually historically, it was the Declaration of Independence was written,
[06:26] I believe, and ratified on the 2nd, which was yesterday. So we sit right here on the 3rd
[06:32] in between the 2nd and the 4th. I'm not a historian, so I don't know all the details
[06:37] behind that 2nd and 4th thing. But the point is, it's a historical weekend
[06:43] that we all celebrate for independence and having the ability to be autonomous human beings
[06:53] that are able to govern themselves. And we talk a lot about, we praise them, right?
[07:03] We look back on our forefathers who fought for independence and we honor them.
[07:11] We have every year since that date. But I wanna say that the modern day soldiers
[07:20] and the modern day freedom fighters do not look like they used to.
[07:25] It used to be, you carried this bayonet or gun and you were out on the battlefield
[07:33] and killing people. That's not what the modern soldier looks like today.
[07:38] The modern soldier looks like a coder, as far as I'm concerned,
[07:42] that is coding and fighting for freedom in on the battlefield that we find ourselves on today.
[07:50] And that is software. So much of our lives is software and technology.
[08:00] And that's where this fight is being fought. And I hope that on a little lighter note,
[08:08] I hope that this didn't totally freak Will out because Will is our guest today.
[08:17] He's the one that's been writing this CoinJoin implementation for JavaScript.
[08:23] And this story of Alex or Alexi or however you say his name, this goes back a year about.
[08:30] And I do believe that I've shared that with Will or at least with some of my team,
[08:36] but hopefully they have a little bit better of an idea. We have the first amendment here in the United States
[08:44] that protects free speech. And as the story told in the intro,
[08:48] writing code is considered free speech. So hopefully, I mean,
[08:54] things always change with politics, right? But hopefully those time honored rights
[09:02] or respected rights, we've always had the right, but at least in the United States,
[09:06] we do tend to respect that at least as the first amendment is written.
[09:12] We'll see if it continues to be enforced like that where we have the right to write free,
[09:19] freedom creating software, and that's protected under free speech.
[09:25] But I guess we'll see, but yeah, let's bring on Will. He's one of our modern day soldiers here
[09:32] fighting the good fight of freedom without even really knowing it.
[09:36] I mean, you don't have to necessarily have that as your goal.
[09:43] I think Will is pretty mild mannered guy that just wants to write cool software.
[09:48] But unfortunately, we're put in a position these days where that can get you just doing something good
[09:58] for the world can get you thrown in a cage on very rare instances.
[10:02] So with that, I guess, welcome Will. - Thanks for having me.
[10:06] No, I mean, I've heard a couple things thrown around when it comes to CoinJoint and Privatesyn.
[10:14] And I think the flaw is that these distributed ledgers just aren't centralized around privacy.
[10:24] I could figure out what you did. I can figure out who you paid.
[10:28] I think when Edward Snowden was saying in that video, he said, "Privacy must be baked into the protocol."
[10:36] And that seems like the last thing that was baked in. - Yeah, it was the last thing
[10:44] that was baked into the Bitcoin protocol. And Dash came around and tried to fix some of that
[10:50] with the Privatesyn feature that we have, which is now rebranded and called just CoinJoint.
[10:55] But it's got a long ways to go. And I think the work that you're doing
[11:01] to bring this into JavaScript and the work that AJ is doing
[11:08] with trying to make some of these transactions just default to a Privatesyn-like transaction
[11:18] is going to go a long way with that. So there's a lot more to say about the work that AJ is doing
[11:24] but let's focus on the work that you're doing. You're bringing the traditional CoinJoint implementation
[11:32] into JavaScript, sorry, the traditional CoinJoint protocol into a JavaScript implementation.
[11:43] So did you have any other leading questions before we get to that?
[11:49] So Will's demo, Amanda, or should we jump right in? - I do want to see the demo and the slides.
[11:56] And first, I just want to be clear on this library. Is this intended for its first use to be seen
[12:03] in the forthcoming incubator web wallet or is this for something else?
[12:08] - Yeah, I don't think that it's necessarily going to, it depends on how quickly we get it done, I guess.
[12:17] But I don't see it as being part of the first implementation of the web wallet
[12:22] but that is the purpose is our web wallet is going to be a JavaScript library.
[12:29] So it's a JavaScript library that can be brought into a browser application.
[12:37] So that can then be used with technologies like Ionic or Atari that can be used
[12:45] to create user interfaces on both the browser and mobile wallet and desktop wallet.
[12:54] So we can then use the same wallet to target all the different platforms.
[13:02] And so we can have a wallet that is unified in its user experience but across the different platforms.
[13:12] And the nice thing is that's what we're doing with this, the CoinJoin thing.
[13:18] When you bring that protocol into JavaScript then you can use that in any of those targets.
[13:25] So we can have a web app or a mobile app or a desktop app that all support CoinJoin.
[13:35] - Okay, all right, we better have a look. Will, would you like to do the slides first?
[13:40] - Sure, let's do that. - Let's do it.
[13:43] - All right. Okay, so my name's William McFallin.
[13:49] I am a senior full stack web developer. I am a systems development specialist and a DevOps guru.
[13:58] Essentially, I just love writing great software. Dash has given me the opportunity to do that
[14:04] and today I will be presenting the progress we've made on a CoinJoin SDK.
[14:13] A little bit about myself. Obviously, I said I was a full stack web developer
[14:19] but I also do C++ and I also enjoy writing network protocols.
[14:25] That's something that kind of appealed to me with this particular project.
[14:30] You know, CoinJoin requires me to look at how to write networking code.
[14:35] Not so much reverse engineering but a lot of it was, you know, kind of diving deep into like the C++ code
[14:43] that Dash Core consists of. But you can find me on GitHub or Twitter
[14:51] under my username, W. McFallin. And I will, let's see, we'll talk about where we left off.
[14:59] So, a couple weeks ago, we had the idea of creating a CoinJoin wallet that would exist in the browser SDK.
[15:09] We soon found out that we would need a node portion. So, we have a browser portion and then a node portion
[15:21] that kind of supports anything that a mobile or desktop or web wallet would need to do.
[15:31] - And when you said node in this context, you mean Node.js, right?
[15:36] - Node.js, yeah. So, we're essentially taking like the majority
[15:43] of the networking code that's in Dash Core, which has, you know, been, I mean, it hasn't been extracted
[15:54] and put into its own library. We're essentially doing that.
[15:58] And we're gonna allow other people to, if they want to, they can host it,
[16:03] they can modify it however much they want, but it'll be just its own little package
[16:07] that people can utilize. So, we do have a Node.js SDK.
[16:16] It'll do all the interaction with the peer-to-peer network. This project cannot just be a browser thing.
[16:24] It has to incorporate a browser, but it also has to incorporate Node.js.
[16:30] We are really close right now. The server-side SDK, which is ran in Node.js,
[16:42] it can connect to a master node. It can authenticate just like a full node.
[16:48] So, think of, you know, any wallet that you've used. A lot of them are supported by a full node.
[16:57] We can do that, and we can initiate CoinJoin traffic. Not only can we initiate CoinJoin traffic,
[17:04] we're very close to completing a full mixing round. The various steps in the CoinJoin mixing ground
[17:18] includes a lot of messages, call it, or they're all prefixed with ds,
[17:25] which I believe is dark sen, but they never went back and changed those.
[17:32] So, a lot of these things, even though it probably should be cj
[17:35] for CoinJoin or ps or whatever, it's all ds stuff.
[17:39] So, it's synonymous with CoinJoin and private sen. - All right.
[17:45] - There are, depending on which page you look at, there's, like, on the Dash Core Readme,
[17:53] there are 11 steps, but a lot of those steps include
[17:57] things the master node has to do. So, in reality,
[18:02] we're at, like, the last step. And to put it into, like, a good analogy,
[18:10] I would say, if this were the Super Bowl, it would be the last 30 seconds of the fourth quarter.
[18:16] That's how close we are to finishing a full mixing round. - You said last step,
[18:23] but your slide says eight out of 11, and I think that's because step eight is the last step
[18:29] that we have to do on our side, the client side, and steps 10 and 11 are done by the master node.
[18:36] - Correct. - Is that correct?
[18:38] - Yeah, yeah. So, our last hurdle right now
[18:43] is just signing the transactions in a way that the master node accepts.
[18:49] You actually see in the demonstration that I give that it actually accepts all the inputs that we give it.
[18:56] And more on that, I'll give more on that later, once I show it to you,
[19:01] but we are so ridiculously close. So, this is how the handshake works.
[19:12] Again, like, the numbers are different depending on where you look.
[19:18] This actually doesn't include steps eight, nine, 10, 11. They're actually numbered weird.
[19:27] We are essentially at the last step between the node and the master node.
[19:35] The next step after that would be the master node broadcasting to the network,
[19:39] which is step seven. Just a quick refresher.
[19:46] - You probably said this, but those steps are differently labeled, I guess.
[19:50] - Yeah. - Okay, gotcha.
[19:52] - Yeah. I'm gonna go over the packet types real quick.
[19:59] DSA, when you see, when you join a queue, you're gonna see something that says DSA accept
[20:06] is compatible, please submit. What that's saying is,
[20:08] yes, we would love to start a mixing session. Please submit your denominations.
[20:15] Steps two and three is a DSQ message, mostly. That's when you, when the master node has at least,
[20:26] so depending on the network, it's at least three, four mainnet and testnet, I believe.
[20:33] Once it has that many and then it can't find any more, it'll start with mixing, which is step four,
[20:44] which says, okay, you've accepted me into this queue. I have a bunch of inputs I wanna mix.
[20:54] Let me send to you. You'll see, you know, adding entry one of 20
[20:59] and depending on which entry you are, that's prone to change.
[21:05] Steps five, six, and seven, the DSF message is something that
[21:14] the master node will respond with. It'll say, okay, I've mixed all,
[21:19] or I've mixed everything that you've given to me. Let's sign it and you'll see finalized transactions,
[21:27] relay final transaction. The step that we're on right now is,
[21:35] well, we finished the DSS step. We just have to send it back to the master node
[21:40] and you'll see similar messages, like finalized transactions.
[21:45] Steps nine, 10, and 11, they're all the master node, essentially.
[21:52] The 11th step, which is get data, that's actually an optional step.
[21:57] And the dash core read me actually says, yeah, you don't have to send get data,
[22:02] but if you wanted to, you can optionally do that. And yeah, so I guess I will present
[22:11] this JavaScript library, see where we've gotten so far. Let me share my screen.
[22:19] - Okay. - And I'm not sure if it's in your demo or not,
[22:25] but let's take a look at the code repos that you're working with,
[22:30] just so people can look at that and see what you're doing, see if they can help, see.
[22:35] Yeah. - Okay.
[22:38] - What, just maybe give us a repo name and after your demo, of course.
[22:46] - Okay, okay. So, can you guys see my terminal here?
[22:51] - Yes. - Launch, okay.
[22:53] - I have a very nice Star Wars theme I see you've got going here.
[22:57] (laughing) - Yeah, for sure.
[23:00] Okay, so this is a launcher script. What it does is it launches three instances.
[23:10] There are gonna be three connections that connect to the same master node.
[23:17] They're gonna send their inputs and everything. So, when you see something like,
[23:22] Luke sends a DSS message or Chewy or Honda, those are just easy to remember names for each instance.
[23:33] And I'll go for, so we do have a log file, which I'll just reset for now.
[23:44] So, when I launched this, it creates three different users
[23:49] with the three different wallets. You get a lot of, a lot of debugging text.
[23:57] What this means is that Chewy has been accepted into a queue.
[24:06] You'll see that three times. Let's see here.
[24:13] Coin join is collateral valid. So, you'll see this stuff.
[24:18] So, let me highlight it with my mouse. So, DSA accept is compatible.
[24:24] Please accept. What that means is Chewy submitted,
[24:30] it says he wanted to mix 0.001 denominations. He sent one as well as a collateral transaction.
[24:48] That's what this message says. And that'll happen three different times.
[24:52] So, now we have, we go back. We have Han, Luke and Chewy.
[25:01] All three got accepted into the mixing queue. - Just one quick question before you keep going.
[25:10] - Sure. - To be clear, this is, you basically set up scripts
[25:15] to create all of this on the regression test network, reg test.
[25:22] This is not test net, as we know it. This is not main net.
[25:27] This is a local reg test, right? - Right.
[25:31] - Network. - Yeah.
[25:33] - And there was a lot of work getting that going, as I remember.
[25:36] - Yeah. - Like creating all the private key, public key pairs,
[25:41] denominating, pre-denominating the coins so you don't have to have that,
[25:48] 'cause that's required as part of the program, as part of the protocol to have those pre-denominated coins.
[25:56] - Yeah. So, to add on to that,
[26:01] this actually gives us a little bit more flexibility as far as, I know Amanda was saying prior to the show
[26:09] that she would like a different way of how we handle denominations.
[26:15] The way I built it, you know, whatever denominations you send me
[26:20] is what I'm gonna be sending through. However which way you want to cut it up and present it,
[26:27] you know, it's completely up to the client library. So I think there's a lot of flexibility with that.
[26:33] - Mm-hmm. - Okay, so this actually shows that,
[26:39] also let's go all the way back up. So we have HAN update accepted, accepting entries.
[26:47] What that means is we've sent the transaction inputs. They were accepted by the masternode.
[26:58] It mixed it, and then this signing accepted means that it did the mixing process.
[27:07] We sent, we signed off on that. And then the masternode, it's up to them as far as,
[27:15] so this is essentially the last step. And we can go and look at the traffic here.
[27:27] This is the masternode traffic, which has, let's see here.
[27:37] So we add scripts and enter it. It verifies all the scripts, add script,
[27:45] verifies scripts, successfully validated input and input script.
[27:49] And yeah, so this is the last step. This is all working on a reg test network.
[27:58] To make it work on testnet or mainnet, we just simply have to change a config file setting,
[28:05] that's it, and then attach another wallet to it. But this is, yeah, this is where we're at.
[28:16] And I think we'll be completing a mixing round within a few days from now.
[28:23] But yeah, that's what we got so far. - Nice, so this is, what you're looking at here
[28:32] is this would be the logs that you might see if you were to, if you had,
[28:41] if you were running a masternode, even on testnet or mainnet,
[28:44] and you said, print out all the logs, this is what you'd see.
[28:48] So these are logs that are created by the C++ code, right? - Right.
[28:53] - Yeah, cool. So the last step, you said you'll be able to get that soon.
[29:01] So the quote unquote soon. Do you have any kind of timeframe about when you think,
[29:11] once you've completed one round of mixing, it's just a matter of doing it over and over again
[29:19] to create multiple rounds, and then we're essentially done.
[29:22] So after that, what does the roadmap look like? - For this portion, it would just be to hook it up
[29:30] to whatever front-end wallets that we'd like to integrate with.
[29:37] There shouldn't be too much else besides finishing the mixing round,
[29:43] 'cause then we could just essentially run it in a loop, you know, and it can be very,
[29:49] you know, kind of, there doesn't have to be a ton of monitoring going on,
[29:57] you know, it's just, it should mimic in a way how Dash Core does CoinJoin,
[30:05] in the sense that if you wanted to, you could just say, okay, start, and then just let it run.
[30:12] But if somebody wanted more fine-grain control over how, you know, denominations are created,
[30:20] or, you know, a lot of that can be up to the user. It's just a matter of, you know,
[30:27] how much do they wanna control? - Yeah, and we'll make that all on the incubator side,
[30:35] so we're not expecting users to have to do their own denominating and all that stuff.
[30:41] So, yeah, that'll be part of a task, a separate task on the browser side,
[30:46] or the client side for the wallet to make those denominations.
[30:53] And I think we've got Jordan that's gonna be working on that with you.
[30:57] So, yeah, it seems to be all coming together, just need a little bit more time.
[31:03] Any other questions, Amanda? - Did you wanna take a peek at the repos,
[31:09] or sorry, did you do that when I was offline there? - Yeah, let's take a look at those.
[31:16] - So, I would take a look at -hive, look for -join.js. These are the pull requests.
[31:34] The code is all under alpha v1. And we have a nice readme of everything we've done so far
[31:46] and what we've accomplished. We haven't fully merged anything into main
[31:53] until, you know, a solid alpha has been released, and we've all tested it.
[31:58] But I can tweet this, or I can just send it here in the chat for now.
[32:06] But, yeah, so this is where it's at. We don't have any official releases yet,
[32:13] 'cause we're just waiting to finish this current piece, and then--
[32:16] - Do you see the question from Shenmick on the screen there? He says, I'll read it out,
[32:24] why the code base was split into client side/backend side? What parts actually prevent implementing it fully
[32:35] as a client side in the browser? So, can you answer that question?
[32:37] - Oh, yeah. So--
[32:40] - My guess is it has something to do with networking. - Yeah.
[32:47] Yeah, so the browser, if we were to do it purely in the browser,
[32:51] then the browser would have to implement, essentially, TCP sockets,
[32:58] which it can't do now. I don't know of any browser that can do TCP sockets.
[33:06] It can do HTTP requests, HTTPS requests. It can do WebSocket requests,
[33:14] but none of the kind of fundamental TCP socket traffic, it can't do that.
[33:23] So we had to add a Node.js portion there. There's kind of no way around that.
[33:31] I would be stoked to see that supported in a browser, even if it's just one browser,
[33:39] 'cause that would kind of... You can make this a pure browser only SDK,
[33:45] if that were the case. - Yeah, so maybe in the future,
[33:49] if browser vendors start supporting low-level TCP packets, if that's what I understood,
[33:57] then we could modify this so that it could be just
[34:00] a purely browser-side implementation. But that's the trade-off that we had to do,
[34:06] or not the trade-off, but that was the constraint that we had to work within,
[34:09] and so we split it to two different sides. But the important thing here is I think
[34:19] there will be that browser SDK so that any JavaScript wallet
[34:25] that wanted to implement Coin.join could just import this SDK,
[34:30] and then now you've got Coin.join. - Right.
[34:38] - Question for the end, just in case, I guess, this is what I see.
[34:42] Is a web wallet what's needed to make the phone wallet mix?
[34:46] A phone wallet, so basically, is what we're doing, making the web wallet,
[34:54] something that will make a mobile wallet support mixing? I think that's the question,
[35:02] and the answer is yes. So there are different ways.
[35:07] Dash Core Group has their mobile wallets, and those mobile wallets are native iOS and Android wallets,
[35:21] meaning they're written in Swift or Objective-C and Java or Kotlin.
[35:31] And that's how they implement their mobile wallets, and I think that there will be a governance question.
[35:40] I saw a poll about it from Joelle about whether we should have BCG's mobile wallets
[35:49] support Coinjoin, and I think that they're already starting on that,
[35:54] but that's kind of a question that the network will be able to vote on this cycle,
[36:00] as far as I know, could be next cycle. I don't know when Joelle's gonna put
[36:04] that governance question in, but we're gonna be working in parallel
[36:09] for this JavaScript SDK, so that mobile wallets that are built using JavaScript
[36:16] and those technologies that I mentioned earlier on in the show, such as Ionic or Capacitor or...
[36:24] I don't recall the other one right off of Atari. There are others as well.
[36:32] There are older ones as well, older technologies that convert JavaScript codebases into different platforms.
[36:40] So we do plan on doing that, and then like I've mentioned in some of the Maya shows,
[36:45] I'd like to combine this idea with exchanging between different other coins
[36:54] to have mixing as a service for a coin like Bitcoin, for example.
[37:03] So you deposit your Bitcoin into the web app, not deposit in the sense that you're giving up control,
[37:10] but just putting it into the mobile wallet, into the web app.
[37:14] And then it converts it over to Dash, mixes it, converts it back into Bitcoin,
[37:18] and then now you have more private Bitcoin. So that's something that's on the roadmap as well,
[37:24] but this is a prerequisite to both of those applications. - Groovy.
[37:30] Okay, well, was there anything else that we should see or talk about, Will, or does that about cover it for us?
[37:36] - I mean, yeah, that's all I've got for now. And I can field any more questions if anybody has something.
[37:45] - Okay, well, I think that's all the questions we've had so far.
[37:48] So thanks for joining us today, Will. Good topic for a good time.
[37:55] And we look forward to, I mean, it looks like you're on the home stretch here,
[38:00] and we look forward to seeing it ready to go. - Sounds good.
[38:06] - Yeah, so next week we have our, we have our quarterly report, right, Amanda?
[38:14] - That's right, yep. So same time as usual, but it will be, as Rion said,
[38:20] the quarterly report for the second quarter of this year. And of significance is that it will be the final report
[38:28] of the, I guess, what could be called the legacy funding model of the incubator so far,
[38:33] which is where all strategist budgets come from a single proposal payout.
[38:40] And as we discussed on the show last week, things will change up a bit in the future
[38:46] in that individual strategists currently associated with the incubator,
[38:51] or even just people who aren't currently associated with the incubator, but who want to come on
[38:56] as a strategist/project manager will be making their own decisions
[39:04] on that. I'm not sure if it's frozen on my end or everybody's end,
[39:15] but-- - It looks like she's frozen, yeah.
[39:17] - Okay, yeah, so, yeah, next month, next quarter, meaning this coming week, we'll,
[39:25] you'll see three different proposals from the incubator, one from each strategist requesting the funds
[39:31] that they need to complete their, complete and start new projects
[39:37] that they're thinking about under their strategy.