---
showLink: "https://www.youtube.com/watch?v=Kb8r5GqswI0"
slug: "dash-privacy"
title: "Dash’s Privacy & Browser-Based Mixing?"
publishDate: "2023-03-27"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/Kb8r5GqswI0/maxresdefault.webp"
---

Dash developers discuss improving privacy and accessibility of CoinJoin mixing through a new browser-based solution.

## Episode Summary

tl;dr: In this episode, Dash developers AJ and Will join Rion and Amanda to discuss the current state and potential improvements to privacy on the Dash network. Will presents his proposal for a browser-based solution to make CoinJoin mixing more accessible. They cover technical details of how CoinJoin currently works, its limitations, and how a browser SDK leveraging a node.js server could allow more users to easily mix funds for improved privacy.

## Chapters

00:00 - Intro on Banking System Issues and Privacy
The episode begins with a discussion on recent bank failures, bailouts, and the Federal Reserve's role. Rion emphasizes Dash's vision of giving users full control and privacy over their money.

03:18 - Analyzing Dash's Current Privacy 
AJ and Will are introduced to provide their analysis of the current level of privacy offered by CoinJoin mixing on the Dash network. They discuss results of past audits/attacks on Dash's privacy.

27:01 - Will's Proposal for a Browser-Based Mixing Solution
Will presents his proposal for a browser-based SDK to make CoinJoin mixing more accessible. It would leverage a node.js server to allow browser-based wallets to initiate mixing. Technical details of how this would work are covered.

43:13 - Discussing Implications and Applications of Browser Mixing
The group discusses how this browser-based mixing, while somewhat centralized, could be a stepping stone to wider adoption and usage of Dash's privacy features, even for non-Dash users. Maintaining decentralization and the ability for anyone to run a mixing server is emphasized.  

50:36 - Q&A on Mixing Denominations and Alternative Masternode Code
In the Q&A segment, AJ addresses a question about whether having fewer mixing denominations could improve privacy. Rion also fields a question on any plans for alternative masternode code, which is not currently a priority.

## Transcript

[00:00] (dramatic music) We've had a big, massive bank bailout again
[00:12] in the last couple of weeks. We've had a couple of banks fail out west,
[00:19] and of course this is all because of their poor risk management policies.
[00:26] But the real problem, the deep down problem in the roots is American central banking.
[00:32] We know these banks are bailed out by the Federal Reserve. And this issue of what banks can do or not do
[00:38] or the problem of central banking in particular to the American political and legal system
[00:44] and the economic system is something people have discussed in the United States for over 200 years.
[00:54] It is Wednesday, March 22nd, 2023. Let's start off with this.
[01:00] Today, we're gonna hear what the Fed's gonna do and they're going to dictate to all of us
[01:05] how we're gonna live our lives. That is, they're going to be raising rates.
[01:08] They will raise rates today. They're going to consolidate the entire banking system
[01:15] into fewer institutions. That's all this is, a setup for central banks,
[01:22] the Federal Reserve in this case, to issue their new monetary system.
[01:27] - Hi Chair, Katerina Saraiba with Bloomberg News. The minutes of the January, February meeting,
[01:36] the last meeting, indicate that you discussed the possibility of runs on non-bank financial institutions
[01:44] and the impact of large unrealized losses on bank portfolios.
[01:48] Can you talk a little bit more about that discussion? Kind of what was talked about in light of that?
[01:55] And then why didn't the Fed do anything about that at that point to ultimately prevent
[02:01] what happened this month? - I mean, to be honest,
[02:04] I don't recall the specifics of that. It's been quite an interesting seven weeks.
[02:09] But I think, as you know, as it is now in the public record, the supervisory team was apparently engaged,
[02:19] very much engaged with the bank, repeatedly and was escalating.
[02:23] But, you know, nonetheless, what happened happened. - Can you confirm whether or not the board knew
[02:28] about these escalations by the examiners in San Francisco? - I will have to come back to you on that.
[02:37] I don't know. - How many of you out here really believe
[02:44] that all this is happening only just by some kind of freak show accident?
[02:50] No, this is all deliberate here. Why do you think central banks
[02:54] have been raising rates aggressively into a free-fall economy, okay?
[02:59] Do you think, honestly, that this banking crisis, honestly, the regulators missed it?
[03:04] You really think so? You really think the U.S. Treasury missed it?
[03:08] You think that too? And you think the Federal Reserve wasn't keenly aware
[03:13] that all this was going on? (dramatic music)
[03:18] It's thought that we have this very wild swing, all these wild swings in the economy,
[03:23] because we don't have any regulation. We don't have proper control of this banking system.
[03:30] The real issue, though, is not that. The real issue in all of this
[03:34] is federal spending and federal policy. We just think this is the way,
[03:38] this is what we're going to do, and so we ride on the wave all the time
[03:43] of these kind of reckless things that happen, and who knows?
[03:47] I mean, we keep kicking the can down the road. Who knows how long we can keep kicking the can
[03:52] before it really does become a major problem in the United States,
[03:55] and we start seeing a major financial rupture, not just in the United States, but also around the world.
[04:01] (dramatic music) (upbeat music)
[04:06] - Hello, and welcome to "Incubator Weekly." We have a full house today, as you can see.
[04:21] Firstly, I'm Amanda, and I'm joined, as always, by my trusty co-host, Rion.
[04:25] How's it going, Rion? - Going really, really well.
[04:28] - Good. - Good for the financial system, of course.
[04:32] - One of them. We are rejoined this week by a prior guest,
[04:36] Dash developer, A.J. O'Neill. How's it going, A.J.?
[04:40] - Hello, hello. - Good. - I'm doing well.
[04:43] - Excellent. And then joining us for the first time this week
[04:46] is Dash developer, Will Merfalin. How are you today, Will?
[04:51] - I'm doing well. How are you guys?
[04:53] - Yeah, we're feeling good. So, Will, you're the one we know least here, naturally.
[04:58] So, before we get kicked off with other things, namely privacy in Dash things,
[05:05] would you tell us a bit about your crypto background and what brought you to Incubator?
[05:11] - Sure. I've been working with C++
[05:17] and full-stack web development for a very long time. Systems development, in general,
[05:22] is something that I'm very passionate about, and Dash Incubator has been one of those avenues
[05:29] in which I've been able to kind of use that talent and that passion.
[05:34] So, yeah, I've always been into tech. I got introduced to the Incubator through A.J.
[05:43] - Not another one, really. Dang, A.J., that offsets some of your negatives.
[05:50] All right, good. - So, yeah, thank you, A.J.
[05:57] Yeah, I would go to the meetups, and A.J. was just constantly talking about this Dash thing,
[06:04] and I was like, "I had better check it out," and I haven't looked back since.
[06:08] It's been a very cool experience. - Righteous.
[06:11] Well, happy to meet you and happy to have you, Will. So, today we're going to have a group discussion,
[06:18] of course, among the four of us, but also, of course, any live chat viewers
[06:22] are welcome to contribute just about the state of privacy within the Dash network in general,
[06:27] and then we will move into a new concept that has been brought to the Incubator by Will,
[06:34] which has to do with Dash mixing within the browser. I don't even want to say too much
[06:40] because I don't know too much, and then we will finish up by asking
[06:45] some user-submitted questions that came in via social media this past week.
[06:50] So, without any further ado, Rion, what is the state of privacy on the Dash network?
[06:57] - Well, I wanted to actually start by broadening it out to privacy in general, and as you know,
[07:06] we start each of these Incubator Weekly videos with a recap from what happened in the previous week,
[07:15] and something that, at least, I curate these clips just from what I'm watching throughout the week,
[07:22] each week, and it's becoming obvious. More recently, I think it's been pretty obvious,
[07:30] at least for me and most of you who've been watching, that central banks and governments,
[07:37] they do not want you to control your own money, and I believe, I have no direct evidence of this
[07:45] other than plenty, like, oodles and mounds of circumstantial evidence that there's basically,
[07:53] they're orchestrating a transition from our current monetary system
[07:59] to one that's even more dystopian, as if it could be worse than it already is,
[08:04] and how that relates to privacy, specifically, it relates to private property more generally.
[08:11] They don't want you in control of your money, and Dash has the exact opposite vision,
[08:17] which is that we want you in full control of your money, not only where you spend that and how you spend that,
[08:26] but we also want you to have privacy in that. It's definitely, it's a natural right.
[08:33] It's stemming from natural law itself, so no matter what your beliefs are,
[08:40] we shouldn't have to justify why we want privacy. They should have to justify why they want to spy on us
[08:49] and monitor and control all of our transactions, so I've just been, I want to get back to Dash's roots.
[08:58] Dash was the first cryptocurrency that had privacy as one of its fundamental focuses,
[09:06] and we may have slipped a little bit in our technology. I don't know that.
[09:13] We might still be on the top as far as I know, but very few cryptocurrencies have any kind of privacy,
[09:20] and I want to change that, so I'm taking a look at our current state,
[09:24] and I brought in Will to look at that more deeply because he has a pretty extensive understanding of C++
[09:34] and how our code base would work because he understands that,
[09:39] and I want him and AJ to look as skeptically as they can to our privacy and see,
[09:48] is it actually giving us what we think it's giving us? Is it giving us privacy?
[09:53] Is it more commercial-grade privacy where the barista might not know how much money that we have,
[10:00] but the NSA could definitely figure us out? What level of privacy do we have,
[10:08] and how can we make that better? Also, in terms of this project that's coming up,
[10:13] I want it to be more accessible to lots of different developers,
[10:18] so right now, the only way it's accessible is by downloading and running
[10:23] either the full Dash Core node or Electrum, which, as a side note,
[10:30] Incubator is working on getting back up and running and is pretty far along with that,
[10:38] but outside of that, we don't have JavaScript apps, web apps,
[10:43] which is a huge deal. They have no access
[10:46] to being able to use Coinjoin's functions. - "So how hard would it be," asks James Doe,
[10:56] "to create a Dash-based VPN? "I see a lot of content creators
[11:00] "advertising NordVPN and so on. "If Dash has a VPN,
[11:04] "maybe it would find a better entryway "into Dash usage itself."
[11:08] - Well, that is a different topic, but an interesting one.
[11:13] Let's save that for later, but I think that Dash could have a VPN,
[11:21] and a project that it will cross over into Dash at some point this year,
[11:29] I actually am putting servers in a data center right now. - Awesome.
[11:34] - So then there's also, I think a lot of people,
[11:39] when they talk about VPNs, they're like, "Oh, it's privacy,"
[11:44] and really what it is is you're taking the data
[11:50] that used to be under the control of your internet service provider,
[11:53] like let's say you have Comcast or Google Fiber, you're taking that traffic
[11:57] and now just giving it to a different party, like NordVPN, right?
[12:02] So the expectation is that, "Oh, it's private,"
[12:08] but it's just NordVPN now has your traffic, and your current ISP can't see it
[12:14] 'cause it's encrypted through the VPN, so. - It just moves the trust from the ISP to NordVPN.
[12:20] - Yes, and then they think, "Oh, cool, we're safe,"
[12:23] and it's like, "Well, did you do your due diligence "in researching NordVPN?"
[12:28] I'm not saying specific, I'm just using them as an example,
[12:32] but do your due diligence, learn who's behind the VPN,
[12:38] and then move forward with that. But I think that's what he was kind of getting at
[12:45] is that he wants to kind of shift his data to something that Dash owns,
[12:53] if I'm not mistaken. - Let's move back a little bit
[12:58] on the general topic that it sounds like, AJ and Will,
[13:03] you're both looking into, which is, as Rion asked,
[13:09] just what level of privacy are we being offered within the Dash network right now?
[13:14] To give a bit of retrospective, there are two main, I guess,
[13:20] tests of Dash's privacy that I'm aware of that have taken place to date.
[13:25] One, I think, was put out some seven, eight years ago, maybe by Macrochip, someone said,
[13:32] and it was a bounty. It was maybe even a $10,000 bounty,
[13:36] payable in Dash, I'm sure, for someone to effectively unscramble
[13:42] a specific CoinJoin transaction. And in the case of this CoinJoin transaction,
[13:48] I think it took place back when the default mixing rounds within the core wallet were, I think,
[13:54] only four or eight or something, which is half of what they are now.
[13:58] And to my knowledge, nobody ever claimed that bounty. The second test I'm aware of
[14:03] took place about two to three years ago when an individual who was actually quite active
[14:10] in the Monero community put up a donation request
[14:16] for an upgrade to his server and hardware infrastructure so that he could run a bunch of tests
[14:22] on Dash's CoinJoin transactions. And he published the findings of his report.
[14:28] And to my recollection, his general conclusion was something like
[14:33] all CoinJoin transactions on the Dash network ever, of all of them, roughly 80%,
[14:42] he could not find any origins of those inputs. And so it was our guess, or it was my guess,
[14:51] that the 20% where he said, "Hmm, actually, I think I can de-scramble these,"
[14:56] were probably people who didn't use best practices. And I'm sure all of us would agree
[15:01] that our users shouldn't have to read a whole report on best practices to use CoinJoin effectively,
[15:07] but those were his results nevertheless. So Will and/or AJ, what are your take on those two tests?
[15:14] What are the results of those two tests? What do you think?
[15:18] - So I'll start. - Please.
[15:22] - I think that the one, if you, so theoretically, theoretically CoinJoin works, in theory.
[15:29] So if you prop up a use case that's a purely theoretical use case
[15:33] and you follow the white paper, so to speak, then yeah, you end up with perfect privacy, whatever.
[15:39] But that's not how things really work. I have not actually looked into that.
[15:44] I've heard about that bounty. I haven't looked into it to solve it
[15:48] because I imagine that the bounty was created in such a way that it follows all the theory of it,
[15:56] and so it won't be reversible, and so it's a waste of time to try.
[16:00] But in practice, what you do with money is you spend it. The goal of money is not to hoard it in one location
[16:07] and never use it. Because if I want to keep my dollars perfectly safe,
[16:11] I just put them in the fire pit and I light them on fire, and now no one has access to them.
[16:16] And I think that that's effectively what's been done in the first case
[16:19] is the dash has been taken out of circulation. If the dash has been taken out of circulation,
[16:24] then yeah, sure, it's perfectly safe, whatever. But that's boring because you can't use it
[16:29] if it's taken out of circulation. So if all you do is CoinJoin
[16:32] and take your money out of circulation, sure. But the moment you take it into circulation,
[16:38] I think that that's where the problems are going to arise because this is, the protocol basically
[16:43] only benefits from network effect. If there's no network effect,
[16:47] then I understand theoretically that it shouldn't be reversible,
[16:52] but I just don't believe that in practice it's not easily reversible if the money is being spent.
[16:58] Now, 80% of that is probably, and I could be wrong, but 'cause I've got no real information,
[17:05] I'm taking a wild guess because I'm being super skeptical, I bet that 80% is in masternode money
[17:11] that's been taken out of circulation, and the 20% is the money that's actually been circulated.
[17:15] - And so what is it exactly about circulation that you think would be more revelatory?
[17:23] What would it be about that? - So the CoinJoin is not widely deployed.
[17:32] There's only one avenue of access for it, which is Dash Core.
[17:36] And most people, if you're spending money, you're not spending money through Dash Core.
[17:39] It's an absolutely horrible interface and everybody knows that, that's no surprise.
[17:45] It's old, it's crufty. It was college kids using the GTK framework
[17:50] that their professor told them about or something, or QT. - Shots fired.
[17:55] - But no, but this is what it is. And I mean, that's normal, that's normal.
[17:59] When you're a college kid and you're doing a project, you use QT or GTK or whatever 'cause it's what's on the table
[18:05] and you use C++ 'cause that's what your professor learned back in the '50s or, you know, and so that's normal stuff.
[18:12] But my point is that people aren't realistically using Dash Core to do transactions and none of the other stuff
[18:20] in the Dash ecosystem supports CoinJoin on either side, either sending or receiving.
[18:26] So for example, Dash Direct does not support CoinJoin. We don't have any way to get CoinJoin coins
[18:31] shared between wallets. If you try to create an HD wallet in Dash Core
[18:38] and share it on your phone, your phone app will crash and you will have to literally delete the app
[18:43] from your phone because the phone app is only designed to handle up to like 1,000 transactions or something.
[18:50] So you run CoinJoin once or twice and you've maxed out the limit of the number of transactions
[18:55] that it can display and it'll just crash. - So I think what you're talking about
[18:58] is 1,000 change addresses, which normally is not an issue. For wallets, like what you're getting at is,
[19:07] so when CoinJoin happens, it splits everything up into different change addresses
[19:13] and you're limited to 1,000 per wallet. But the wallet can regenerate those.
[19:18] - No, what I mean is that when you're on the phone, if you're not thinking about it, which you wouldn't
[19:25] unless you encounter the problem, you're gonna use the Android built-in
[19:29] or the iOS built-in data list. And that built-in data list consumes some amount of memory
[19:34] and there's some specifications for, hey, if you need to use more than so many items
[19:38] in a data list view, you need to do this to unload it out of memory and reload it into memory.
[19:43] And I'm just speaking from broad, I don't know the specifics of the Dash iOS wallet.
[19:48] I just know broadly speaking, this is how these things work. So what will happen is that the app basically,
[19:55] it runs out of memory. That it loads too many items in the data list,
[19:59] the data list can't handle it and then the app just crashes. That's my intuition from my observation of trying this.
[20:06] So, but my point is you can't use CoinJoin on your phone. Even if you share the HD wallet,
[20:11] you can't use CoinJoin on your phone 'cause the app just crashes.
[20:14] But let's say that you could. Let's say you could get it on your phone.
[20:17] Let's say that bug gets fixed. And maybe it has been fixed 'cause I raised this up
[20:22] six months ago or so and I just kind of, you know, plopped it in a channel somewhere and somebody said,
[20:27] "Oh yeah." And so maybe it did get fixed.
[20:29] So let's say that you can do that. Well now you try to use DashDirect.
[20:33] DashDirect has dirty transactions. And by dirty transactions,
[20:36] I mean transactions that are fingerprints. So if you send a CoinJoin transaction to DashDirect,
[20:44] it's a dirty transaction and it's got lots of extra digits, right?
[20:50] 'Cause when we transact, we generally, we don't care about fractions of fractions of a penny,
[20:55] you know, I don't care about one millionth of a penny. That should just round, you know,
[20:59] round it up to the nearest penny and move on with your life. That would be a clean transaction.
[21:03] But the dirty transactions, they carry every little fraction of a penny.
[21:09] Excuse me, pardon my French for saying the word penny, but that's, you know, that realistically,
[21:14] that's what we're doing. - You're saying because DashDirect requires
[21:17] like some certain dollar amount and then that dollar amount is converted into a dash amount
[21:21] that's like 2.97542. That's quite unique. - Well, except with eight digits,
[21:29] not just four. - Yeah, that's quite unique.
[21:32] And so you'd be able to trace that to a transaction. - Yeah, and so it's just like with other protocols,
[21:40] anytime you have something that's quote unquote private, but on the one side it's not private
[21:43] and on the other side it's not private, given enough transactions,
[21:47] you can just reconnect the strands. And in practice, when I've used CoinJoin,
[21:52] when I've used CoinJoin Send, it's like using 119 coins,
[21:57] any number of coins beyond 10 may affect your privacy. Well, it's like, well, the protocol doesn't support a way
[22:03] to give me denominations that make any sense. And so when I have to pay 28.93 of, you know,
[22:11] if that's what the amount comes out to, then it's gonna use 119 coins
[22:16] because it tends towards creating really, really, really tiny coins
[22:21] 'cause it always wants to take basically the change you get back and then split it up
[22:25] into really, really even smaller amounts. So to build up the smaller numbers,
[22:30] you have tens of coins. And then on the larger side,
[22:33] you have on average five coins per digit. So if you need to pay an amount that's four digits,
[22:39] that's 20 coins right out of the box, right? Because the denominations don't make any sense
[22:44] for the way that we actually spend money. In the natural world, we have doubles, wholes, and halves,
[22:50] right, so everything is a 20, a 10, and a five, a double, a whole, and a half.
[22:54] And that's what we would need in CoinJoin in order to bring the number of coins per digit
[22:58] down to below two on average, slightly below two, it'd be about two.
[23:02] - And so how feasible is that? And, you know, so if I'm thinking I'm a core developer
[23:10] and I wanted to choose the denominations and I chose, okay, 10, one, 0.1,
[23:14] and et cetera, and et cetera, and et cetera, how feasible is it actually to choose the wholes?
[23:20] Halves, and whatever? Instead, like, is the idea that maybe core developers
[23:26] didn't choose that because they imagined that it would be more difficult to find mixing partners?
[23:31] Or why does anybody imagine this was? - I mean, I think it's kind of taking suggestions
[23:39] from how usually like American-based currency is split up. You got $1, 5, 10, 20, 50, 100, et cetera.
[23:50] The five different denominations, like so if you use AJ's number,
[23:56] I think it was like 28.93 dash, you can use each of those denominations to split it up.
[24:06] You got 210, 210 dash, and then you have, what, 811 dash,
[24:14] and then the 0.93, there's also denominations for that. So like I don't understand what the real argument was
[24:24] for that, how it couldn't be split up like that. So you can split it up using those standard fives.
[24:30] - No, because it only gives you one. The only, it's only sliding one, right?
[24:36] So if you have a nine, that requires nine inputs. So anytime you have a digit that's the number nine,
[24:42] that requires nine inputs. There are no fives and twenties.
[24:47] Everything is only a one. It's a sliding scale of one.
[24:50] And as to why it's that way, I don't know, 'cause I haven't talked to them,
[24:54] but just looking at the code, I think it's because it's cute,
[24:57] because it makes a bit sequence. So basically in binary, there's ones and zeros,
[25:05] and it just looks cute. Like, if you look at it, if you look at the code,
[25:08] it's just cute code. It's just cute.
[25:10] It's cute because you can bit shift over by one for each. - Bit shift?
[25:15] - Bit shift, it's called bit shifting. - So I'm not gonna get into the details of that.
[25:19] - Yeah, it's, but it looks cute. That's the reason I think they did it.
[25:22] I don't think they did it for any other reason than that it's cute.
[25:25] It's like, oh, cool bits. - I have to soften that a bit,
[25:28] because I don't wanna say that, like, we don't have a solution that we know works better
[25:38] than what we have right now yet. The point of this discussion is to say
[25:44] that we are looking into it, and if we can find improvements
[25:47] that don't have the drawbacks that maybe Dash Core Group has already seen
[25:51] with other proposed solutions, we're going to pursue that. - Well, to what degree is Will's concept a solution?
[26:02] Obviously, correct me if I'm wrong, Will, your solution has nothing to do
[26:06] with changing denominations or anything, but rather to address one of AJ's other points,
[26:12] which would be to bring the mixing closer to the point of spending,
[26:16] in this case, maybe even mobile, or what? - Well, we want something that anybody
[26:25] can just drop into their browser and start using. Now, the browser alone won't be able
[26:32] to directly contact the Dash network and instigate a lot of this stuff.
[26:40] We would have to initiate a lot of that, so that's why I propose a solution
[26:45] where we have it run on server side and we have it run in the browser,
[26:49] and my presentation actually goes over that. - Let's have a look.
[26:53] - Okay, sounds good. Okay, so Dash PrivateSend, we're building a browser SDK.
[27:01] You guys know a little bit about me. Here's some stuff about me as well.
[27:08] I was born in San Diego, moved to Utah in 2012. I enjoy all the nerdy things.
[27:14] I'm a fairly decent artist, and I like making music. My technical qualifications,
[27:22] I've been doing full-stack web development for 10 years, Linux enthusiast.
[27:27] I also do C++ system development. I write network protocols, assembler programming,
[27:32] and that's my Twitter and GitHub right there. Some of the things I'll be talking about,
[27:41] the reasoning for using PrivateSend, how PrivateSend works in a high-level overview
[27:46] of the browser SDK, and then finally, I'll get into the nitty-gritty
[27:50] networking package structure. What is PrivateSend?
[27:55] I'm just gonna kind of gloss over this. We already know it's the way to mix, you know,
[28:01] coins so that you can have non-custodial, or so that you can obfuscate where your coins end up.
[28:10] It gives you consumer-grade financial privacy. You retain control over your money at all times,
[28:20] and it's incredibly easy to use. Why would you need it?
[28:26] The idea of a distributed ledger means that every transaction can be tracked.
[28:31] This is stuff that is well-known, and it's the purpose for PrivateSend.
[28:38] Privacy on the internet is a non-popular opinion. Everybody has your data.
[28:42] Everybody's trying to sell it. If companies or entities wanna track
[28:50] what you've been doing because of the way a distributed ledger is built,
[28:57] there's no way you can just go back and erase that. And also, PrivateSend mirrors
[29:06] the standard expectation of privacy with everyday transactions.
[29:09] And what I mean by that is there used to be a time where your parents gave you $5.
[29:14] You'd walk down to the store. You'd buy a conch book, a stick of gum, and a soda.
[29:19] And for the most part, there wasn't a ledger that kept track of that exact thing.
[29:25] Now, maybe the store might keep track of that, but they don't have your name
[29:30] and the address from which your bills came from. There's no such thing.
[29:37] I believe PrivateSend facilitates that for us a little bit. How it works, this is a little bit more in-depth,
[29:47] but you need a full node. It contacts a master node.
[29:52] It adds you to either a new or an existing CoinJoin queue with at least two other participants.
[30:00] So it relies on other people wanting to do this. The CoinJoin queue will be locked
[30:08] when the master node is satisfied with how many participants.
[30:12] The more, the better. That's great, but it only needs three.
[30:16] And on TestNet, it only needs two, so you and one other person.
[30:21] It breaks down the coins into denominations. They end up being paid to yourself in those addresses
[30:30] that the mixing begins. And this can actually be configured in your wallet,
[30:37] and you can say, "I want at least eight or nine," or you can tell how many rounds that you prefer.
[30:47] This will repeat until the number of rounds is performed, and then all peers sign their transaction.
[30:57] When I say peers, I mean everybody who's in the CoinJoin queue.
[31:02] The result is that your funds end up in denominations. We went over this.
[31:07] Any observer would have a hard time tracking where your Dash ends up.
[31:15] That's the purpose. And this can be performed many times,
[31:20] and you are limited to 1,000 change addresses, but normally this is not an issue at all.
[31:26] Your wallet can generate more. And there should be an option
[31:32] for even HD wallets to generate more. What does it cost?
[31:38] So there is a collateral that is attached to a CoinJoin session, and that's something
[31:45] that all peers kind of agree on before mixing begins. There is a one in 10 chance that collateral is charged.
[31:55] And the actual code looks exactly like this. If getRandInt, so give me an integer
[32:02] that's between one and 100, and if it's greater than 10, or in other words, if 90% of the time,
[32:11] or yeah, so if 90% of the time, we're gonna return early. We're not even gonna process this collateral.
[32:19] Also, if a peer misbehaves, masternodes can choose to charge them a fee.
[32:27] That's also random, too, and I can go into that, but I won't be speaking about that for the scope of this.
[32:33] - I am curious, is the getRandomInt, does that happen to be cryptographically random?
[32:40] Do you know? - It's a fast random context,
[32:46] is what they call it in the code. It's for speed over security,
[32:56] from what I can tell. But I'd have to really look into that.
[33:00] I can get a better answer for you. - We should make it so our browser version
[33:07] plays against the fast random algorithm, 'cause it's not gonna be an even distribution,
[33:11] and make sure our people don't get charged the fee ever. - Or use math.random, right?
[33:18] Okay, so if multiple peers misbehave, they will be put into a list,
[33:28] and it'll shuffle that list, and then it's basically,
[33:33] it's basically Russian roulette, the first person that gets charged.
[33:41] It's not, it's definitely not, there's no rules to it, really.
[33:47] It's up to the random number generator. My proposal for the SDK is that we have two parts,
[33:56] well, two parts and one optional part. We have the node.js SDK,
[34:01] which we'll have to run on a server. There's no way we can get around that.
[34:05] And then we'll have the browser SDK, which contacts the node part through RESTful API.
[34:12] The third optional part would be a WebSocket server, which would, I think, be the best way
[34:23] that a client can interact with our code, because they could get very fast, up-to-date information
[34:32] regarding their CoinJoin info, and the status and everything.
[34:37] I would say it would rival the Dash Core wallet as far as how much, or how fast you'll get a notification
[34:46] of that stuff. So, I kind of already went over that.
[34:52] So, the node SDK runs on the server. We'll be exposing, oops, we'll be exposing,
[34:58] oops, let me go back. We'll be exposing a RESTful API.
[35:02] The browser can start, stop, join session, get mixing status, CoinJoin info.
[35:09] And then the WebSocket stuff, as well, is reiterated there. The reason for a node SDK is because
[35:18] we can serve this over SSL. We're talking about privacy.
[35:23] If you have a browser SDK that's directly hitting like a node HTTP, or the node JSON RPC port,
[35:35] that's not authenticated, and it's not intended for public use.
[35:45] We need a secure web server that is running over SSL to give us maximum security for that.
[35:57] And also, a node SDK would give us a lot of flexibility, and we can actually add a lot more value
[36:04] to what we can offer a browser-based solution. Development has started.
[36:14] The node SDK and the browser SDK have started. There are, I'm thinking of coming up with nicknames
[36:24] just to be cute. Everybody has a nickname,
[36:26] but it'll probably just be called like Dash Join or something.
[36:30] Now I'm gonna go into the technical overview of Dash networking.
[36:36] This is for programmers and network enthusiasts. The Dash network package structure,
[36:46] it's a peer-to-peer networking layer that's all done in TCP connection-oriented sockets.
[36:51] Packets are sent over the wire. They're wrapped in a message header, which we'll go over.
[36:56] A node communicates with master nodes. Master nodes handle the coin join interactions.
[37:03] Really, the only responsibility of a node is just to let a master node that you wanna start
[37:15] and stop a session. Yeah, so 99% of all the traffic will be between a node
[37:26] and a master node. You'll never see any other peer
[37:31] within the coin join session. The message headers wrap the coin join interactions
[37:40] into the coin join messages. There's different types of messages here, DSA, DSQ.
[37:46] I'll have links to that in further slides. The Dash networking looks like this.
[37:52] There's the source. The node will send DSA, DSI requests.
[37:59] The master node responds. That continues for the entirety of the coin join.
[38:05] Start, join pool, start, mix, all that stuff. The entire process is handled by a node and a master node.
[38:12] The DSTX means that everybody in the coin join session has signed the transaction.
[38:23] And that gets sent over the network. The message header in depth.
[38:31] The message headers is typically 24 bytes as a message start, message command,
[38:37] or a message start, a command size and checksum. The command is literally just a string.
[38:42] When people say, oh, we're sending a DSQ over the network, if you notice on the right,
[38:49] you see K, then a dot, then DSQ. That's raw packet capture off the internet
[38:56] that you can capture with TCV dump or Wireshark. This is all readily available.
[39:04] See, I've correlated it. I've cross-referenced it with the C++ code.
[39:11] This is how it's done. So it's fairly open.
[39:16] Which, I mean, I don't particularly like that it's that open, but this is just how it works currently.
[39:27] I would like to see some improvements on that. These are the different message types.
[39:35] So the CoinJoin protocol, I guess you could say, is a lot of the stuff isn't directly available
[39:49] via the JSON RPC. The JSON RPC has three calls related to CoinJoin,
[39:57] and it's fairly limited in what we want. I would like to see potentially moving forward
[40:05] something that mimics the actual traffic that a node is sending to a master node.
[40:15] That's something I would like to see in our SDK, 'cause I don't think it's something
[40:22] that would be too difficult to accomplish. There's more info, but that is my presentation.
[40:32] I give links here for further reading. I have a link to the GitHub repo
[40:38] that we're currently working on, and I do have some links to,
[40:45] most of them are most likely gonna be Amanda B. Johnson's videos on PrivateSend,
[40:50] which I suggest everybody go check out. They're really helpful, but yeah.
[40:57] - Well, UginM6 coached me through the making of those, so thanks to him as well.
[41:02] - Can you drop that link, Will, so that we can get that in the chat
[41:06] so people like me, for example, can take a look at that and see it in...
[41:11] - Sure. - 'Cause the StreamYard kind of scales down.
[41:14] It makes it hard to read and see some of the particular words and links and stuff.
[41:19] - Okay. - So am I understanding correctly, then,
[41:25] what we're seeing here proposed, and of course, very technical detail,
[41:30] is the creation of an incubator-run server, which could facilitate dash coin join mixing
[41:41] by browser-based clients. Is that correct?
[41:47] Okay, okay, and please. - If I'm not mistaken,
[41:51] Will, you have enough information now that we're not limited to having to run a full node
[41:56] to do that. We could actually just pack that in a buffer
[42:00] and send it across the wire in Node, and we could have a standalone reference implementation.
[42:05] Is that correct? - Well, we would need access to a node.
[42:09] We definitely would. - So we can't do it standalone?
[42:16] Okay, nevermind. - Well, I think it's possible to do it standalone.
[42:26] Currently, right now, I think the easiest way would be to have Node,
[42:30] but I do think we could do it ourselves in Node as well, which I would probably prefer.
[42:36] - 'Cause my understanding was, because it communicates to the master node directly,
[42:40] not doing a broadcast to the network, we don't actually have to have 90% of the code
[42:47] that would be necessary for a normal transaction send, because we're just doing a round trip back and forth
[42:53] between one master node over a TCP session. - Yeah.
[42:59] - Okay, so we could do that part standalone. And I'm hoping that's the case,
[43:05] and I'm looking forward to that. - I wanted to give one potential application of this.
[43:13] As many of you know, we've had the Maya guys on recently, and so Dash will be part of the Maya-supported coins,
[43:23] which it goes along with Ethereum and Bitcoin, for example. So if somebody in Bitcoin wanted to have some privacy,
[43:35] get some privacy features through Bitcoin or through Dash, but for Bitcoin, they could do that through Maya.
[43:43] So you could have a web app that accepts Bitcoin. You send Bitcoin to the web app.
[43:50] The web app then transfers that into Dash. Then the web app, once it's in Dash,
[43:57] it mixes those coins in Dash, then transfers it back to Bitcoin.
[44:02] And now somebody that doesn't really care about Dash still can have a use case for Dash through Maya.
[44:08] - Okay. And so then, I guess, is this kind of like a...
[44:17] It's a sort of hybrid solution in a way. It's obviously not pure protocol executed, right?
[44:24] Because that, at least as of the current time, does require running a full node.
[44:29] And so it's incubator offering up a sort of stepping stone, which, you know, while we realize
[44:37] that having a single incubator-run server is not an ideal long-term solution,
[44:43] it would ideally get more people mixing. And like Rion just said,
[44:48] more people potentially using Dash just for the privacy features.
[44:52] And so it's like a sort of centralized stepping stone to the decentralized Dash network.
[44:58] Is that accurate? - Well, I think whatever code that we write
[45:03] will be open source. So if somebody doesn't like the centralized service,
[45:07] they can always spin up their whole infrastructure on their own.
[45:11] Got it. - That centralized is a dirty word.
[45:15] Decentralized is when you have the option of choice. This will be decentralized
[45:19] and that you will have the option of choice. - Yes.
[45:22] - It won't be decentralized from the perspective of you are forced to submit to anonymous untrusted services.
[45:29] I don't like that definition of decentralized, which seems to be used quite often.
[45:36] Because you don't know what something is doesn't make it trustworthy.
[45:39] And because you do know what something is doesn't make it trustworthy.
[45:43] But if you trust it, then it's trustworthy, or at least you trust it.
[45:46] - Yeah, I guess I'm more meant, in case of a weather event or a connection event,
[45:52] if incubators server that offers up this service goes down, the stepping stone would not be available
[46:00] for anyone who had been utilizing it. But as you two are saying,
[46:04] because this would be open source, anybody could spin up such a stepping stone.
[46:08] - Well, it's like spinning up a full node, right? Generally, you probably, well you,
[46:15] you personally may have your own full node running. I think most people don't have a full node running.
[46:21] And so whenever they're doing anything on the Dash network, they are connecting to some full node
[46:26] that's provided by the app that they're using or the service that they're using or whatever.
[46:33] And I think that it's really important to expose that so that you can see where are you connecting to
[46:40] and you can choose what do you wanna connect to. But ultimately, yeah, you,
[46:47] there should be multiple options for what you want to connect to.
[46:53] I mean, even we running this, we should run more than one. - And possibly in different data centers geographically.
[47:06] AJ, did you have a, yeah, did you have an answer to one time's question?
[47:11] - Yeah, so one time asked, doesn't fewer mixing denomination levels
[47:15] having only one per order of magnitude have the effect of making it more difficult
[47:20] to try to analyze and discern between identical input amounts
[47:23] because it means that there are more of the same mixing amounts.
[47:26] So fundamentally, this is the correct assumption because this is what we're trying to avoid
[47:32] in the first place. We don't want dirty transactions.
[47:34] Dirty transactions are where every single digit is so unique that it provides a fingerprint.
[47:40] We want clean transactions where there are a discrete number of inputs
[47:46] or a discrete number of categories of inputs that we can use.
[47:51] You have to weigh that against the cost of the other factors of the fingerprint.
[47:56] So yes, if you could only price things in the real world, if things were only priced,
[48:03] pardon my French, $1, $10, $100, then that would help make this the perfect system.
[48:12] But in the real world, things aren't priced by single denominations.
[48:16] So what we want to tend towards is the distribution average of coins per digit.
[48:22] So how many digits are there in the payment that you're going to make
[48:27] and how many coins do you need to make up that number, that specific number per digit?
[48:33] So while, yes, in one theoretical scenario, having only one denomination per order of magnitude
[48:43] would be the best, you have to weigh that against would you rather that the average
[48:49] be that you have five coins per digit, which means that you have five opportunities
[48:55] for fingerprinting, because even every coin represents an aspect of a fingerprint,
[49:01] a bit of a fingerprint, and we want to reduce the number of bits of fingerprint.
[49:06] So if you're looking at it from that perspective, the number of coins per digit
[49:14] are going to contribute more to the fingerprinting factor of unwinding where did this coin come from
[49:22] than having two more coins per order of magnitude so that you on average have slightly less
[49:31] than two coins per digit in an even distribution. And the distribution isn't even,
[49:36] but the way that we price things person to person actually tends towards one coin per digit.
[49:43] And the way that we price things commercially tends towards lots of nines,
[49:48] which would give us the highest number of coins. That would put us at an average
[49:51] of close to three coins per digit. But when we price things commercially,
[49:56] we also typically add taxes and taxes roll those nines over to zeros
[50:01] with a seven at the end, which brings us back closer to one coin per digit again.
[50:07] So on average, even with an uneven distribution and the way that we actually use money,
[50:12] I think that that would bring us to right around two coins per digit
[50:16] as opposed to five coins per digit. And not having so many threads
[50:25] through which you can trace where the coin came from is going to have more of an impact
[50:30] than a small number of extra denominations. - Okay.
[50:36] - I just wanted to clarify one thing. Like when you're saying coins per digit,
[50:38] you mean like the number six would require in your system a five and a one.
[50:45] - Yes. - Whereas in the base 10 factor system,
[50:50] it would require six ones. - Yes, exactly.
[50:54] - Okay. Well, we have covered quite a lot here
[50:59] and I know that we could probably talk a lot more about a lot more subjects.
[51:05] I will, however, move us now to two user submitted questions that came in over the past week.
[51:11] To make clear to everyone, we, of course, as usual,
[51:16] are always happy to accept questions live. But if you aren't able to join us live,
[51:22] you can submit them at any time via our social media channels.
[51:25] So in so doing, Grandmaster Dash asked, when alternative code for a masternode server,
[51:33] perhaps exchanges or financial services would appreciate the choice?
[51:37] - Alternative code for a masternode server, is that question like when are we gonna build
[51:46] a different implementation of a masternode, like as opposed to the C++ implementation?
[51:54] Is that how that question is supposed to be interpreted? - That's how I interpreted it.
[51:59] - Well, we've got a Go implementation, half-baked Go implementation, as far as I know.
[52:06] - It's Go, it's the RPCs, it's not. - Yeah.
[52:10] - I mean, I could be mistaken, but it's-- - Half-baked is probably too much.
[52:13] A quarter-baked or a tenth-baked or something like that. - It's like inside API, it's just a wrapper.
[52:19] - What I've seen, we could have something else that I didn't see, but what I've seen,
[52:22] all it is, is it wraps a full node and then makes requests to the full node.
[52:27] - Okay. We don't have any plans to build
[52:32] an alternative full node right now. - Will would have to do that.
[52:37] In order for that to work, we'd have to break the existing code apart into functional libraries
[52:43] that could be reused. Otherwise, I don't think it would possible to,
[52:46] that would have to be the path to get there. It'd have to be somebody that's C++, dude, or gal, dudette.
[52:53] - Okay. Then our second question, let's see that one, Pete.
[52:59] This is from Kryptosi, and he asked us, "When will the incubator start to tackle
[53:04] "or foster projects aiming to build on platform?" My guess is that that would be a question for you, Rion.
[53:19] - Can you guys hear me? I think I had an internet problem there for a minute there.
[53:24] "When will the incubator start to tackle "or foster projects aiming to build on platform?"
[53:29] As soon as platform's ready. We got burned a year ago where we started
[53:34] doing a bunch of platform work, and I think, at least I hope that some of our testing
[53:41] was useful for DCG, but it was very ineffective and inefficient development for us.
[53:46] We spent a lot of time on working with a product that wasn't done yet.
[53:52] So I've pretty much, as far as my own personal strategy, I'm not doing platform projects until it's ready,
[54:01] at least on testnet. - Okay, well, and that leads us perfectly
[54:08] into letting you all know what we have coming up next week. Rion just mentioned his own personal strategy,
[54:15] and next week, Incubator Weekly will actually be the quarterly report for the Dash Incubator.
[54:23] And so we'll hear not only from Rion as the lead strategist, but also from his fellow two strategists, Tim and Ash,
[54:30] and each of them will give us a full recount of everything that they have funded over the last quarter,
[54:38] will let us know anything that they decided to drop funding on and why,
[54:42] and then also tell each of us the financial picture according to their strategy budgets.
[54:49] So we will, of course, happily accept your questions during the call or prior to the call
[54:54] as submitted via social media. So that is all that we have for you today.
[55:00] And fellas, unless any of you has any gems of wisdom to leave us with, I think we'll say, "Sara Nora."
[55:11] That seems like a big no, so. - Mic was muted, but I have nothing more to add.
[55:16] Long show today, but I think it was important. - Good. - I agree.
[55:21] - Okay, well, AJ and Will, thanks for joining us, and we look forward to hearing updates
[55:24] from you in the future. - Cool, see you guys.
[55:27] - Adios.