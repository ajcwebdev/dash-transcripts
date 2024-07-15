---
showLink: "https://www.youtube.com/watch?v=7tmdWezydKw"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Platform Walkthroughs Part 7b - Niles Salter"
publishDate: "2024-07-10"
coverImage: "https://i.ytimg.com/vi/7tmdWezydKw/sddefault.jpg?v=668bf36d"
---

## Episode Description

Niles Salter explores Dash Platform, guided by Anthony and Rion, encountering network issues while setting up an identity, registering a name, and creating a simple React app using the Dash JavaScript SDK.

## Episode Summary

In this technical walkthrough, Niles Salter, guided by Anthony and Rion, attempts to set up and interact with the Dash Platform using its JavaScript SDK. They encounter several network-related issues, particularly with registering a name on the testnet. Despite these challenges, they successfully create an identity, register a contract, and build a basic React application that interacts with the Dash Platform. Rion provides valuable insights throughout the process, especially regarding the platform's architecture and future development plans. The session concludes with a discussion about potential improvements to the SDK, including the possibility of wrapping the more feature-complete Rust SDK for JavaScript use.

## Chapters

00:00 - Introduction and Recap

Anthony and Rion welcome Niles back for part 7b of the Dash Platform walkthrough. They briefly recap the previous session, which covered blockchain basics and Dash's dual blockchain system. Rion mentions that the testnet was down during the last session, so they'll be attempting to run the actual commands this time. The discussion highlights the importance of understanding Dash's architecture, including its proof-of-work and proof-of-stake blockchains, and how they interact.

05:24 - Setting Up the Environment and Initial Commands

In this chapter, Niles begins setting up his environment to interact with the Dash Platform. Anthony and Rion guide Niles through checking his code files, including the .env and client files, to ensure everything is correctly set up. They encounter some issues with the network connection, leading to a discussion about using specific DAPI (Decentralized API) addresses to improve reliability. Rion provides additional context on the importance of these steps in the overall Dash ecosystem.

20:00 - Troubleshooting and Network Issues

This segment focuses on troubleshooting the network connection issues they're experiencing. Anthony and Rion discuss changing the SDK version from 15 to either 12 or 16, hoping it might resolve some of the problems. They also explore the possibility of adding more verbose logging to better understand what's happening during the commands that are taking unusually long to execute. Rion shares insights from his experience with the platform's development, highlighting the challenges of working with blockchain networks, especially on testnets.

40:00 - Creating and Interacting with Contracts

Niles successfully creates a contract on the Dash Platform and begins interacting with it. They go through the process of submitting a document to the contract, updating it, and deleting it, demonstrating the basic CRUD (Create, Read, Update, Delete) operations possible with the platform. Rion provides additional explanations about how these operations relate to the broader Dash Platform architecture, illustrating its potential as a decentralized database.

59:44 - Setting Up a Frontend Application

The final part of the walkthrough involves setting up a simple frontend application to interact with the Dash Platform. Niles uses Next.js, a React framework, to quickly set up a web application. Anthony guides Niles through modifying the app to fetch and display data from the Dash Platform, while Rion offers insights into how this integrates with the platform's backend. This section gives viewers a glimpse into the full stack of building on Dash, from blockchain interactions to user interfaces.

67:27 - Wrap-up and Future Directions

In the closing segment, Rion leads a discussion about the current state of the Dash Platform and its upcoming mainnet launch. He explains the differences between the JavaScript and Rust SDKs, noting that while the Rust SDK is more feature-complete, it lacks documentation. They also discuss the possibility of wrapping the Rust SDK for JavaScript use, which could potentially provide a more robust solution for developers. Rion's insights highlight the ongoing development and decision-making processes in the Dash ecosystem, giving viewers a deeper understanding of the challenges and considerations of blockchain platform development.

## Transcript

[00:00] All right, we're back for part 7b with Niles. Welcome back, Niles Arvunderkind, who we got to meet last time.
[00:12] Thank you so much.
[00:14] Yeah, welcome back, Niles.
[00:16] Just as a brief recap of our last stream together, you are fairly unfamiliar with blockchains in general, or at least were before the first stream.
[00:31] So we did an overview of what blockchains are, the Dash blockchain, the fact that Dash Platform is a separate blockchain that has a link to the Dash main blockchain.
[00:48] So we have a proof-of-work blockchain and a proof-of-stake blockchain.
[00:51] They're linked together and they can transfer funds from one chain to another.
[00:57] We discussed that conceptually, but the testnet was down for that day, so we did everything just reviewing code and whatnot.
[01:10] But today, we're going to jump into actually doing the commands.
[01:15] So let's go ahead and get your screen share up.
[01:18] Last time, we did start the tutorial, we got the wallet going.
[01:27] There's an auto-show, said we did.
[01:29] So we covered various aspects of Dash's architecture, including its dual blockchain system, consensus mechanisms, and ongoing development of platform features.
[01:37] Oh, nice. That's what your chat GPT show notes scripts gave us?
[01:45] That's part of it. Yeah, I cut off the end, actually.
[01:48] So that concludes the plans for future exploitation of the Dash ecosystem and potential contributions from Niles. Can't forget those.
[01:54] Okay, cool.
[01:56] We did get the testnet funds, and so that part's taken care of already, so let's add your screen to the blog post, and we'll just continue on, or basically start the actual commands.
[02:17] Real quick, can we just look at your code, including your .env and your client file, just to make sure everything is where it should be for where we're at in this point in this tutorial?
[02:27] Yeah, so those both look good.
[02:29] So we got your mnemonic in, okay, and then checker.env.
[02:34] So everything's good there, yep.
[02:38] And then go to your .env file real quick.
[02:42] So we got testnet, we got our address and mnemonic.
[02:45] Okay, cool, so you should be good to run the create identity command, and then we'll go from there.
[02:52] Yep.
[02:53] Okay.
[02:56] And, okay.
[02:59] Let me see, where were we in this?
[03:01] So go further down, past the pictures, and then past the create identity, and then right there, run npm, a little too far.
[03:10] So go back up a little bit.
[03:13] Yeah, a little bit more.
[03:16] Right there.
[03:17] So npm run create identity, that's the one you got to do.
[03:22] After this, this is where we'll be at the -- this will give you a link to a different block explorer, it will be for the platform explorer, and not the dash layer one explorer, so this is just for the platform.
[03:37] And this will -- because the platform is where things like the identity concept entirely exists, and documents, and data contracts, and all this stuff that is actually the point of dash platform, which is why it's always really funny, it would break at this point, because this is the point where it's like you would do all this throat clearing to get to the point of having an identity so you could actually use the freaking platform.
[04:06] That is the kind of the life of a blockchain person, so there's a whole lot of startup cost.
[04:18] >> Speaking a little bit, how long do you expect this one to take?
[04:21] >> At least 20 seconds, usually.
[04:23] So this is about correct.
[04:26] This is probably the longest command, again, being like the first one to get you started.
[04:32] Very inconvenient one.
[04:33] So there you go.
[04:34] You're good.
[04:35] So first put that -- before you click that, copy the identity ID and get it in your .env file so we don't forget this step.
[04:43] >> The whole line.
[04:44] >> The whole line.
[04:46] Yeah.
[04:47] Bam.
[04:49] Okay.
[04:50] Now follow that link.
[04:57] And then, Niles, if we have time in this show, since we got a little bit of a head start since there was a previous one, I would like to circle back after we get as far as we get and look at this create identity, look at the code that's actually running when we're doing that, and we'll see if we can together discover
[05:24] what is causing the slow -- like the slowness there.
[05:31] >> Okay.
[05:34] So, yeah, I'm sorry.
[05:35] I missed it.
[05:36] What are we looking at on this page?
[05:38] This is my identity.
[05:40] We have --
[05:41] >> So this is the platform explorer, and this is what's basically -- so if you go to transactions, click that.
[05:49] >> And zoom in a couple more if you could.
[05:51] >> Yeah.
[05:53] So this is breaking down specifically what is your identity and then what are the different state transitions that happen.
[06:03] So creating the identity is what's called a state transition because it's basically like a write on the blockchain versus a read.
[06:10] A read would not be a state transition.
[06:12] So if you just retrieve your identity, then you will not be changing anything, but you're creating identity or you're writing something.
[06:21] So this is what's happening there.
[06:23] So is that the whole thing or are you able to scroll down any more?
[06:27] >> This is it.
[06:28] >> Okay.
[06:29] So try clicking the identity.
[06:33] Yeah, click that.
[06:34] That will just take you back to where you were, right?
[06:36] So does that make sense?
[06:38] >> Okay, yeah.
[06:39] So that's my identity?
[06:41] >> Yep.
[06:42] >> Or the identity of the transaction.
[06:44] >> So this is your identity on the left and then the different things the identity is doing, like a transaction or transfer or creating a document, that's on the right.
[06:53] >> Gotcha.
[06:54] >> And you'll notice there on the previous screen that you've got a balance that's denominated in credits.
[07:03] Who wants to look at the number of zeros there?
[07:08] Is it --
[07:09] >> It's a billion.
[07:10] >> It's a billion.
[07:11] Okay.
[07:14] So that is a -- you can think of that as, like, a subunit of Dash.
[07:21] So it's a billion credits.
[07:24] 1,000 credits is the smallest unit of Dash and there are 100 million of those units in one actual unit of Dash.
[07:33] So that's how many credits --
[07:35] >> We need to pick up an intermediate unit that we can also display here just for everyone's sanity because that's such a large -- it forces everyone to all of a sudden have to use scientific notation to do anything.
[07:49] >> Yeah, and because that identifier is taking up so much space anyway, maybe we can ask Mikhail to write in parentheses that 1 billion credits is X number of Dash.
[08:03] >> This is a change I can even make.
[08:05] I know.
[08:06] It's a Next.js frontend.
[08:07] I can do that.
[08:09] >> Yeah, yeah, exactly.
[08:16] >> Yeah, totally.
[08:17] I don't know.
[08:19] >> That would be super useful.
[08:21] That's a good idea.
[08:22] >> Something like that.
[08:24] All right.
[08:25] Moving on.
[08:28] >> Okay.
[08:30] I'm going to go back.
[08:32] I got the identity ID.
[08:52] Okay.
[08:53] So, yeah.
[08:54] Do you want to do this?
[08:56] >> You just did that.
[08:57] >> Right.
[09:00] I can see the top identities.
[09:02] Yeah, I just saw my own.
[09:04] >> You have little glyphs now.
[09:07] That's fun.
[09:08] >> Yeah, if you see one of the ones from yesterday is Claire.
[09:11] >> Claire, that's me.
[09:12] Look at that.
[09:14] I'm famous now.
[09:17] All right.
[09:27] Should we do this?
[09:30] >> Yeah, I'm 90% certain this is not going to work.
[09:34] >> Should I kill this?
[09:36] >> Why did the process not end here?
[09:39] >> Go back to your create identity file real quick.
[09:45] Yeah, it should have disconnected once it was done.
[09:48] I'm not sure why it's hanging.
[09:50] We know it did finish because we got all the info on the explorer already.
[09:56] >> Yeah, this ran.
[09:59] >> Yeah.
[10:01] So, we can kill that.
[10:03] It's not going to be an issue.
[10:05] But what I was saying is I'm 90% certain this is -- the command we're about to run is not going to work.
[10:12] And I'm not really entirely sure why.
[10:14] But the last couple walk-throughs, this one has been giving us issues, which is strange.
[10:20] Because it has functions within it that are in other commands that don't give us issues.
[10:25] So I'm not quite sure what to do about that.
[10:37] Get identity IDs.
[10:44] Okay.
[10:47] And we can run it.
[10:53] Doesn't focus me on this window when I come down.
[10:55] I'm a little annoyed by that.
[11:09] Puny code is deprecated.
[11:13] >> Yeah.
[11:15] >> Yeah, it says that for almost every -- no, it says that for every single node project that I use right now.
[11:22] So that's one of those dependencies that's so deep in the sauce that literally there's not a single project I use that does not use it.
[11:29] It's really annoying.
[11:31] >> That sounds like a perfect package to exploit.
[11:36] >> Yeah, exactly.
[11:38] I know, right?
[11:40] But yeah, there's a -- flag you could give node to make it not give you such annoyances.
[11:47] Like fundamental broken parts of the ecosystem, you know?
[11:56] >> Whale.
[12:00] >> While this is running, you could probably -- so when I was doing this with Rishi, every time he ran a command, he would just start doing the next file while it was running.
[12:11] He's such a --
[12:20] >> Oh, duffs.
[12:25] >> This is what we were kind of talking about in terms of the credits and the billions and billions of them.
[12:43] >> All right.
[13:07] Should I run this right now or should I wait?
[13:09] >> No, it should be done now.
[13:13] >> Jeez.
[13:19] Is it slow on the network or is it slow on my computer?
[13:25] >> This is a little excessive, and the fact that the last one just kind of hung forever makes you think it might have something to do with your computer, but it's hard to say because we don't really get the observability that we would need to say right now.
[13:39] We would need to instrument the commands to somehow be separating your own compute time versus the network time, which I'm sure in theory is possible, but would need to do research to figure out how to do.
[13:54] But this -- so this command is just reading back the identity we already created, so honestly, we should probably just cut this one off if it doesn't eventually execute and just go to the top-up identity because the top-up one is important because that actually has ramifications on future commands.
[14:14] >> Okay.
[14:15] Do you want me to kill it?
[14:17] >> Let's let that run for just a little longer while we look at the top-up command and explain what's happening there because conceptually it's important to know what this command is actually doing.
[14:28] So what it does is it gets your wallet with the get wallet account, and that sets its wallet account, and then it gets your identities with get identities IDs, so that's the only thing the other command is doing is getting identity IDs, just trying to loop over them and display them, which for some reason is making an issue.
[14:47] But with this one, we're also then topping up each identity with a certain amount of credit.
[14:52] So I wrote this -- it just throws a bunch -- it throws credits into all of your identities.
[14:58] You may have multiple ones.
[14:59] It's not necessarily a good thing to do if you actually have real money and you want to be using a specific identity for a specific thing, but for this tutorial, I did this because there's ways in which if you're not following along exactly, you may have, like, created multiple identities and not necessarily realized it, so this ensures that you're always going to have identities ready to go with some money in it and kind of just, like, blast it out from your dash wall into each identity.
[15:21] And that's what the credits are.
[15:23] It's a way to offload your dash from your layer one wallet into your identities, which are on the dash platform.
[15:30] >> Okay.
[15:34] So your layer one wallet versus the dash platform.
[15:37] So that's what this line is doing.
[15:39] You have two different identities in the two different spaces that you just said.
[15:45] >> That is for logging them in the -- yeah, that's just for the --
[15:56] >> Oh, this is for the information about the identity.
[15:59] >> Yeah, because the command above that, the await client.platform.identities.topup, that's the topup command itself.
[16:07] >> Yeah, I see what this is doing.
[16:09] >> So that's looping over.
[16:11] So you already have each ID from the for loop happening.
[16:17] >> Okay.
[16:18] Well, let's check on our other command here.
[16:20] >> Yeah, so let's kill that.
[16:22] >> Still going.
[16:25] >> And then let's run the topup and see what happens.
[16:37] >> Yeah, so when we did this with Claire, we had an issue with the retrieve identities.
[16:46] >> I think we -- did we put the script in the --
[16:49] >> Oh, the you.
[16:51] >> Oh, yeah, we haven't -- no, no, we haven't -- so go to your package.json.
[16:59] Oh, no, we do have all of them.
[17:01] But -- oh, yeah, so I think at one point one got changed to have a capital U versus lowercase u possibly.
[17:11] >> Yeah, that's what it looks like.
[17:13] Yeah, so this has to be capital.
[17:17] And I could change it over here, too, I guess.
[17:29] So, yeah, that's an inconsistency.
[17:32] >> That's weird.
[17:33] I'm surprised that -- wait, hold on.
[17:35] >> So it's fine in here, but inside of here it was wrong.
[17:41] >> I don't think that's what's happening in the actual -- I'm looking at my blog posts, and they're all the same.
[17:51] So at one point I think you typed one yourself.
[17:55] >> I don't think I typed this.
[17:58] Where did I get the package.json from?
[18:03] >> From the tutorial also.
[18:05] Yeah, I'm not sure.
[18:07] But there's been two other people who have gone through this and were also using the copy buttons, and this didn't happen.
[18:12] So at some point I think you just wrote it out.
[18:15] I'm not sure.
[18:16] But it's fine.
[18:17] We know what the issue is now.
[18:20] >> What in the world?
[18:24] How did that happen?
[18:26] >> That's a good question.
[18:28] I don't know.
[18:29] >> Look at that.
[18:32] How did that happen?
[18:33] I don't understand.
[18:35] That's crazy.
[18:36] >> Actually, no, I think I know why.
[18:39] Because you went over this so long ago, this was before -- you were using an older version.
[18:46] So someone pointed this out to me and walked through either 8 or 9.
[18:52] And then it was -- actually, it might have been you who pointed it out.
[18:57] So there's -- someone pointed out that there was an inconsistency there, that we should be using capital U instead of underscore U, because it's a different word.
[19:07] So I then went back and changed it.
[19:10] So it's been consistent in the blog post, but your two walkthroughs were not consistent across the same blog post.
[19:18] >> Gotcha.
[19:19] So it was your fault is what I'm hearing.
[19:22] >> Sounds like a you issue.
[19:25] >> Oh, really?
[19:26] Okay.
[19:29] Okay.
[19:30] I got the results for that.
[19:43] Topic identities.
[19:45] So we just need to run the top of identity command correctly, right?
[19:50] Or did we do that already?
[19:52] >> Which I did.
[19:53] >> Okay.
[19:55] Great.
[19:56] >> This is my output.
[19:58] >> Yeah.
[19:59] And it went super fast.
[20:00] So like I'm saying, it's essentially -- it's doing the exact same thing the retrieve command did, but with a couple extra things.
[20:07] So it doesn't make any sense why one would crap out with the other one.
[20:11] But anyway, let's keep going.
[20:13] Okay.
[20:16] So we got a register name.
[20:20] And it says we want this inside of our environment.
[20:37] >> It can't be a space.
[20:38] It has to be a dash.
[20:40] >> It has to be a dash.
[20:42] >> It has to be a dash on dash.
[20:44] >> Yeah, there's a link to the naming constraints also, which explains stuff like that.
[20:51] But it's a little too much to put in the blog post itself.
[20:54] Zoom way up, yeah.
[21:03] Cool.
[21:09] Anyway, let's go back.
[21:14] Make a register name.
[21:22] And we run it.
[21:43] >> You can go ahead and hide that little bar at the bottom.
[21:47] There's a hide button there.
[21:50] Sorry if that was bothering you.
[21:55] >> So this is, again, one of those things where, you know, if we get to a point where we can circle back a little bit, I'd like to look into this and have you look into this, Niles.
[22:08] Have you done much JavaScript debugging?
[22:15] >> Yeah, I mean, I usually don't have bugs in JavaScript.
[22:18] No, I'm just kidding.
[22:21] >> I mean, I meant other people's code base, of course.
[22:24] >> Yeah, yeah.
[22:26] Yeah, a little bit.
[22:33] >> Because, frankly, I'm not sure what the holdup here is, what's taking so long if it's on the network side.
[22:53] And that would help.
[23:16] >> XKCD was saying something about that.
[23:23] Yeah.
[23:28] So let's move to the next step and let that run.
[23:36] This might be one of those -- it seems to be taking even longer than it usually does on that one.
[23:43] >> Yeah, it shouldn't take that long.
[23:58] Yeah, that link probably doesn't work, because whatever I created back when I wrote this may not still be there.
[24:13] >> What is this data in here?
[24:16] >> So that's what you're going to get once you create your name.
[24:19] So the label is what you gave your label.
[24:24] And then -- so what was it, Miles or Niles something?
[24:31] Just your name, yeah.
[24:33] So that's the label.
[24:35] So in my blog post, it's AJC web dev test 2004-08, which is when I did this first.
[24:43] So I was back in April.
[24:45] That's what that date is.
[24:47] And that's why the links probably don't work anymore.
[24:50] >> Yeah, test net's been wiped clean and restarted since then.
[24:57] And I have it on good information that we'll have some documentation on setting up a local network so that we can test that as well shortly.
[25:11] But right now we're still with the test net, which is a little finicky.
[25:15] I mean, I think it depends whether he has Docker set up or not.
[25:20] Do you have Docker set up, Niles?
[25:24] >> I don't remember if I have wiped my own computer clean since setting up Docker, honestly.
[25:30] I wouldn't be confident enough to, like, just open it on the stream.
[25:34] >> Yeah, that's the only hard requirement for getting a local network, is you got to have Docker set up already.
[25:43] So we'll just keep going on here, I guess.
[25:47] But if we can't get the name to register, then we can't -- I mean, I think we can still create documents and all that stuff.
[25:54] So the fact that it just hangs, it doesn't eventually throw an error, that makes me think it's something on Niles' computer, not the test net.
[26:06] Because this is something that's never happened before.
[26:08] It's never just hung forever and never returned anything.
[26:11] It always eventually gives an error or it works.
[26:14] Like, this is totally new to me.
[26:17] >> Anthony, are you equipped to try to run some of this stuff in parallel?
[26:23] >> Well, I mean, we know the network itself works to create the identity.
[26:29] So it's not an issue of, like, is just the network down or not.
[26:33] So I could try it out.
[26:36] >> Could it be a version issue?
[26:38] I have 22.4.
[26:40] I don't think so.
[26:41] >> No, that's good.
[26:45] >> Well, this is still doing nothing.
[26:53] >> What makes you suspect that it might be Niles' computer, Anthony?
[26:58] Because it's not standard?
[27:00] >> Because this is the first time this has ever happened before.
[27:02] And just because he's running Linux, so that means absolutely anything can happen.
[27:05] I have no idea what would be a computer issue, not a computer issue.
[27:09] I don't think anyone else has run this on Linux before.
[27:12] >> Yeah, that is a variable that we haven't seen before yet.
[27:16] >> Really, most of your developers don't use Linux?
[27:20] >> I don't know anyone who uses Linux.
[27:23] >> A lot of developers will use Linux on their VPS.
[27:26] But when they're developing, they're usually using Macs.
[27:31] >> Oh.
[27:33] Gotcha.
[27:35] >> For better or for worse.
[27:39] >> But let's see.
[27:42] What can we do to kind of investigate this?
[27:45] >> Well --
[27:47] >> Well, so I'm trying right now just to create my own label.
[27:50] So I'm going to spin up a wall and do that whole rigmarole.
[27:53] But that's going to take like five minutes.
[27:55] So I think we should just try and create documents or try and create data contract and see if that's going to work.
[28:00] >> Let's move on to the next step, Niles, and then Anthony can do that in the background.
[28:04] We'll see if we can use some other commands.
[28:09] >> Should I run these two commands in parallel or should I kill this one?
[28:12] >> I'd go ahead and kill that one.
[28:15] >> Yeah, you should kill the other one.
[28:20] >> I lose my pace when I do that.
[28:23] >> What shell are you using?
[28:27] >> This one is bash right here.
[28:31] >> You should try zish instead.
[28:35] >> Well, I don't know.
[28:38] I don't know if that's --
[28:40] >> All the others you've done have been doing zish because zish is the default for Mac.
[28:45] That should definitely not affect anything.
[28:48] But if we want full consistency, zish would be more consistent.
[28:54] >> Yeah, I mean, it's just running this; right?
[28:56] Or it's just running one of these.
[28:59] >> It shouldn't make a difference.
[29:02] >> Definitely not.
[29:04] The things that shouldn't make a difference frequently do.
[29:09] >> Fair.
[29:13] I cannot read properties of null.
[29:16] This is null right here.
[29:18] Or, no, this is null.
[29:21] >> Let's see.
[29:22] So, sorry, what command did you run to get this?
[29:28] >> The retrieve name command?
[29:30] >> Yeah, it's not going to have the name yet because we had trouble.
[29:34] >> Oh, yeah.
[29:35] >> No, sorry.
[29:36] I wasn't saying do that one next.
[29:37] I was saying go on to the next one after that.
[29:40] >> Oh, okay.
[29:42] Gotcha.
[29:45] Okay.
[29:46] We've got a blueprint for the structure of data that the application tends to store.
[29:52] >> Okay.
[30:11] >> Yeah, we won't do this either because we've seen that that one -- there was an update that made that not work too well.
[30:20] >> Okay, but I can register a contract right now?
[30:22] >> Yeah.
[30:26] So you can open up the register, yeah, the register contracts code and see what it's doing.
[30:36] >> Okay.
[30:37] >> So we're pulling identity ID out, this, and then get information about our identity here.
[30:54] >> Yeah, so we've seen that we've already been able to do that.
[30:57] It's the name we weren't able to get.
[31:05] >> Okay.
[31:06] Do you want me to try to run this right now?
[31:07] >> Yep.
[31:24] >> That was quick.
[31:25] >> Yeah, it will get the contract ID quickly because that's client side work, but it will take a little bit to finish.
[31:36] Are those -- let's see, what are those?
[31:45] Have you seen those before, Anthony?
[31:48] >> No, never seen it before.
[31:50] >> Interesting.
[31:52] But it does say that the contract registered, and it finished the script, so that was --
[31:57] >> Yeah, it all worked.
[31:59] >> Yeah.
[32:01] Just out of curiosity, what version of the SDK are we using if you go to your package JSON file?
[32:09] 15.
[32:10] We've never used 15 before.
[32:12] How did it do 15?
[32:14] That must have been the latest version at the time of our last stream.
[32:19] >> That may be why we're having some issues.
[32:23] >> Possibly.
[32:26] >> Because we've never used 15 before.
[32:28] Let's change that to either 12 or 16.
[32:35] Do you remember which one we've had best luck with, Anthony, 12 or 16?
[32:40] >> 12 is in here.
[32:42] >> I haven't noticed any real difference between the two yet.
[32:45] That has been consistent.
[32:50] I can say for sure it worked on 12 and not on 16.
[32:53] >> The network is mostly running 12, and 16 is the latest release.
[32:58] >> But the network is not -- this is like -- we were talking about this dashmate, because dashmate, we could be on 12 or 16.
[33:07] And, like, that's what the network is.
[33:09] That's closer to what the network is running.
[33:11] Because the network isn't running the JavaScript SDK.
[33:14] >> No, I know, I know.
[33:15] But in theory --
[33:16] >> So I just don't think that makes any sense when you say that the network is running 12.
[33:20] Because you're saying it's running a completely different piece of software that also happens to be version 12.
[33:25] That's not the same thing.
[33:27] >> If it were semantic versioning, it would matter.
[33:30] Let me put it that way.
[33:32] >> No, it wouldn't.
[33:33] It only matters within its own -- semantic versioning only applies to itself.
[33:38] It doesn't mean other things in an ecosystem at the same number needs to be compatible.
[33:42] >> Listen, I know DCG much, much better than you do.
[33:49] So just calm down here.
[33:51] >> Okay.
[33:52] >> I know what they do.
[33:54] >> All right.
[33:58] >> Okay.
[33:59] So, yeah, do you want me to change this dependency here?
[34:04] >> Yes.
[34:19] >> He's defying you.
[34:44] >> So do you want to retry the step that we missed?
[34:50] >> Yeah, I think we probably should.
[34:55] Did you -- and do we have to -- sometimes it seems like you do and sometimes you don't.
[35:00] But the package lock, did that -- did we have to blow that away before we --
[35:09] >> Yeah, I always do that.
[35:11] I also usually delete node modules, too.
[35:14] >> Yeah.
[35:15] >> That will take longer to reinstall them.
[35:17] So you can probably blow away the package lock.
[35:23] >> Before what?
[35:25] I'm sorry.
[35:26] >> So delete node modules and the package lock.json and then do the install.
[35:34] Because if -- it's been too long since I've done this myself, this work myself.
[35:39] But I just noticed when I was developing that if you don't change your package lock, even if you change your package.json,
[35:45] if your package lock is still there, then it will just install the old one in the package lock.
[35:51] >> Gotcha.
[35:52] >> Yeah.
[35:53] >> So, yeah, do you want the 12 or the 16 version?
[35:58] >> I think let's go with 16.
[36:03] >> Let's do it.
[36:06] >> In theory, 16 should be all the good things from 12 minus the bad things from 12.
[36:17] >> All right.
[36:20] >> Yeah, because I think the times that we were messing around with different versions and stuff, the issues was really more so just because there's something cracked in a couple of the commands that make them inconsistent.
[36:34] And I don't think being on 12 versus 16 is going to specifically affect those.
[36:38] But I still have yet to actually see a point where I feel like I was confident that there was an issue that always happened on 16 that was not happening on 12.
[36:47] So I think at this point it would make more sense to kind of just go with the most recent version and see what happens.
[36:58] >> Is there like a verbose mode I could turn on?
[37:01] >> And you're running retrieve name, but I don't think that we ever actually did the register name.
[37:08] That never successfully finished.
[37:10] >> No, we didn't.
[37:11] >> So that's the one we should do next.
[37:17] >> Too far.
[37:18] You went way too far.
[37:23] There you go.
[37:25] Nope.
[37:27] >> I don't think I even saw.
[37:29] >> Go slower.
[37:31] There you go.
[37:32] You just went past it again.
[37:35] >> You're talking about the register contract one?
[37:37] >> There you go.
[37:38] No, not register.
[37:39] It should be register.
[37:40] >> It's not register name.
[37:42] >> Register name.
[37:43] It's register name.
[37:48] >> All right.
[37:49] Hopefully it works this time.
[37:54] >> I do think we should get a verbose mode maybe.
[37:59] >> Yeah, there may be one.
[38:24] A lot of these are any types.
[38:34] >> Yeah.
[38:40] It's supposed to be -- the type script never got all the way through.
[38:45] Let's put it that way.
[38:48] >> Rarely does, let me tell you.
[38:51] >> You know the any type is just the cop out.
[38:55] I don't have time to do this.
[38:56] Let's just make it end.
[38:58] This is what happened.
[39:00] >> Anytime is the admission that you should have been using JavaScript in the first place.
[39:04] >> Mm-hmm.
[39:06] >> You have time to write the type.
[39:08] Don't use type script.
[39:09] It's totally absurd.
[39:15] >> Yeah, we are still not finishing on register name.
[39:20] >> Okay.
[39:21] You should go forward with the rest of the contract stuff.
[39:23] I'm about to try and do it.
[39:27] >> Should I register contract?
[39:31] >> I think you already did register contract, didn't you?
[39:34] Did you ever save that contract ID in your .EMV?
[39:43] >> No.
[39:47] We did get it, though.
[39:48] >> We just didn't copy it and paste it in there.
[39:52] >> Yeah.
[39:53] >> It's in your history.
[39:54] Yeah.
[39:55] Scroll down a little bit.
[39:57] >> This one?
[39:59] >> Yeah.
[40:01] >> And then this, yeah.
[40:19] I hate it when it does that.
[40:20] Okay.
[40:21] So we got a contract ID, and then I have this information here.
[40:25] Should I put this somewhere, or is that just for my viewing pleasure?
[40:28] >> Just for your viewing pleasure.
[40:31] >> All right.
[40:36] >> Okay.
[40:38] So we registered a contract.
[40:40] Now let's go back to the tutorial and see what step we're on, which is going to be submitting the document.
[40:47] It will probably have you get the contract as well, but we can skip that part for now.
[40:51] >> Okay.
[40:59] Oh, yeah.
[41:00] Do we want to do this, retrieve contract?
[41:03] >> I mean, we can try.
[41:05] Sure.
[41:08] That one usually works.
[41:36] We can also try to find it on the platform explorer.
[41:47] >> Should I change this link to this?
[41:57] Hey, there's me.
[42:03] And I have a transaction.
[42:12] >> Mm-hmm.
[42:14] >> Cool.
[42:17] Still going in here for some reason.
[42:27] >> Well, let's skip that one again.
[42:30] We'll move on to -- we'll just do all the ones that seem to be working relatively quickly.
[42:37] >> Okay.
[42:44] Update contract.
[43:08] So this one gets an existing contract.
[43:16] Gets a document schema.
[43:36] Okay, so we're updating note.
[43:45] And then associating it with our identity inside of the existing contract.
[44:14] At least in theory.
[44:20] >> Okay, so mine crapped out on creating the identity, funny enough.
[44:26] We were able to get through.
[44:29] So I tried -- I switched the DAPI addresses and I'm running it again right now.
[44:34] This stuff is comical, I swear to God.
[44:37] >> Let's go to your web browser real quick and go to the platform explorer.
[44:50] >> Right here.
[44:51] >> And go to validators.
[44:56] Let's see if this is up yet.
[45:02] Okay, so we have active and inactive.
[45:13] I was hoping for a list of IP addresses that are known to be running, but I guess that hasn't been updated yet.
[45:23] I think they're working on that page.
[45:29] Can you click on those validators?
[45:33] If you click on that.
[45:36] >> Proposed blocks.
[45:40] >> Proposed blocks, active.
[45:45] Doesn't give an IP address.
[45:47] So, Anthony, are you just using the IP address that we've used before?
[45:52] >> Yeah, I just literally pulled up Travis's video and scrolled to the point in the video where we put in IP and typed that exact one out.
[45:59] It's running right now.
[46:00] I don't know if it's going to work.
[46:02] Very, very soon.
[46:03] >> Amazing.
[46:09] >> Yeah, the API might be a little further ahead.
[46:13] >> Okay.
[46:15] So, yeah, you want to keep going through this?
[46:17] >> Sure.
[46:18] >> Yeah.
[46:19] >> All right.
[46:21] I'm going to go back to the client options.
[46:27] Where are my client options?
[46:28] >> All right.
[46:29] Okay.
[46:30] So here's an IP address that I got to work with a command that we already got to work on his.
[46:34] So we'll see if this actually helps or not.
[46:39] >> You're going to put it in the stream yard?
[46:42] >> Yeah.
[46:43] So you're going to want to put this in your client.
[46:47] >> Inside of my -- I'm sorry, let me see what it is.
[46:55] >> Yeah, so not your .env.
[46:57] >> Yeah.
[46:59] It's going to go in my --
[47:01] >> Client.js, very top.
[47:04] >> Client.js.
[47:06] >> Yeah, and just put it right under network.
[47:15] >> Okay.
[47:18] So this helps with what?
[47:22] >> This lets you take the specific network node that you're going to connect to with the specific IP address instead of just looking for one and then crapping out because it hits a bad one.
[47:33] >> Okay.
[47:38] So which part of the tutorial should I go to now?
[47:48] >> Let's keep going to the end.
[47:50] >> Keep going for now.
[47:51] >> Okay.
[47:52] >> We'll go back.
[47:53] >> So we're going to change our name while you're doing this.
[48:07] >> Okay.
[48:10] So put that in.
[48:16] And then network.
[48:23] And then put the apps in there.
[48:32] Okay.
[48:34] And this contract ID.
[48:37] I have it.
[48:38] Okay, good.
[48:41] Okay.
[48:48] So we can submit note document.js.
[48:49] Kill it.
[48:59] And we run it.
[49:07] Have you tried connecting to this IP today and it worked for you?
[49:12] >> Yes.
[49:14] >> Okay.
[49:16] >> Yeah, this is what I was doing in the background.
[49:19] I'm right at the point now where I'm trying to register a name with this IP.
[49:24] I was able to create the identity.
[49:26] I wasn't able to create the identity without it.
[49:29] There we go.
[49:31] We got a name.
[49:35] >> So you were able to do that.
[49:37] >> Dammit, 20240709.
[49:42] >> Okay.
[49:44] So I did this.
[49:49] >> Okay.
[49:50] That's great.
[49:51] That worked.
[49:56] >> And, yeah, did I want to save that output somewhere?
[50:01] >> Just the document ID.
[50:03] >> Yeah, just that.
[50:05] >> Yeah.
[50:06] >> In my end.
[50:07] >> Yep.
[50:08] Uh-huh.
[50:09] And then you're going to -- the next step, you're going to update -- oh,
[50:11] wait, you already got that in there.
[50:12] Never mind.
[50:17] >> Okay.
[50:20] >> Cool.
[50:21] Yeah, so let's continue on this line.
[50:23] Once you get to the end of these commands, we'll circle back and do the
[50:25] register name.
[50:28] >> Okay.
[50:32] >> And I'm assuming we run it.
[50:38] Hello from Nell Salter.
[50:42] >> There you go.
[50:43] You wrote to the chain.
[50:45] Wait, hold on.
[50:46] >> Oh, yeah.
[50:47] >> The label is coming from your .env, not from the chain.
[50:50] That's why that works.
[50:54] I was like, I didn't know your name.
[50:56] You didn't register it.
[50:59] >> Okay.
[51:00] >> I didn't know.
[51:03] >> Okay.
[51:04] Update note document.
[51:11] >> We should probably --
[51:16] >> Yeah, the one thing that's been nice about going through this and having a
[51:19] break in so many interesting and unique ways is I've become very confident
[51:22] about what my code is actually doing here.
[51:47] What's your experience with like front-end frameworks, Niles, like React and
[51:50] stuff like that?
[51:53] >> I haven't touched those in a long time.
[51:55] On my website, I actually just use like vanilla JavaScript stuff, vanilla HTML
[52:00] and CSS.
[52:01] >> What's a long time mean?
[52:03] Are we talking a year, three years, five years?
[52:06] >> Probably five.
[52:09] >> Wow.
[52:10] So were you writing class components?
[52:16] >> For React, I don't think I even did that in the browser.
[52:23] I just did like React-flavored stuff, not React specifically.
[52:31] >> What's React-flavored stuff?
[52:37] >> Yeah, I mean, I actually like the TypeScript that I was using, it was for a
[52:44] different ecosystem.
[52:46] And so there were libraries based on React.
[52:49] >> Do you remember what they were called or what they were?
[52:52] >> Yeah, it was Roact because it was a Roblox-specific incarnation of it.
[52:59] And, yeah, so it wasn't for -- the React flavor thing that I used, it wasn't
[53:11] specifically for the browser.
[53:13] >> Oh, it's a Lua UI library similar to Facebook's React.
[53:17] So you haven't actually used React is what I'm guessing.
[53:21] >> Not React, no.
[53:23] >> Okay.
[53:28] >> He dodged that whole dumpster fire.
[53:33] >> Well, he didn't because he's right in front of him right now burning away.
[53:36] He's going to have to take a big old whiff.
[53:44] So, yeah, this tutorial ends with you building a React frontend.
[53:48] So it should be as painless as possible for you, though.
[53:52] >> Actually, I did Vue relatively recently, though.
[53:56] Because I had it for like -- I did like a code test that was using Vue.
[54:02] I made like a little Pokemon viewer for that.
[54:06] >> Okay.
[54:08] So that's more similar than probably to whatever that React Roblox thing five
[54:12] years ago was.
[54:14] Because Vue and React, they're very similar now, especially if you write them
[54:18] with the most modern syntax.
[54:20] So that means you do have some experience with the modern frontend.
[54:24] Basically, it's either React, Vue, Svelte, or Solid.
[54:27] If you've used any of those and you kind of got a handle on it in any respect
[54:31] whatsoever, the rest you're going to be able to figure them out, you know?
[54:34] >> Okay.
[54:36] >> All right.
[54:38] So where are we at, then?
[54:40] >> Props and state.
[54:42] >> Yeah, so I just did the update note document.
[54:45] >> And so now I can do -- >> Yeah, the last one is the delete document.
[54:50] So this is your basic CRUD commands.
[54:52] So this is kind of like the actual hello world part of the tutorial once you
[54:57] have your identity, once you've created your contract.
[55:00] You can actually put storage in there.
[55:02] You can edit that storage, pull it back out.
[55:05] This is like your global database.
[55:09] >> Awesome.
[55:16] And then set up a backend server.
[55:32] Hmm, the delete document doesn't seem to be very snappy either.
[55:39] >> You know, I'm using this -- >> Go ahead.
[55:44] >> I was going to say, I'm using a pretty good computer right now.
[55:47] I have like an AMD Ryzen 9 5950X inside of this desktop, which is not the
[55:54] latest generation, but it's Zen 3.
[55:59] The one that's coming out this month is Zen 5, so.
[56:04] >> Well, it actually -- >> It's not an actual like computer processing thing.
[56:08] It's more so just however it's connecting to the network.
[56:11] And also because we're using StreamYard as well, that may be just taking up
[56:15] more network bandwidth on your computer.
[56:19] So that's -- >> I wouldn't expect that.
[56:21] >> I would say it's more likely -- I mean, it affects things like installing
[56:26] node modules and other things.
[56:29] >> Yeah.
[56:32] >> Okay, so we ran all the individual scripts, and we can extend this
[56:36] functionality with a backend in front of that.
[56:38] Let's create an express server that will return information on a given
[56:41] identity name.
[56:48] Let's see what that does.
[56:55] So we've got a server, and we create a name endpoint here.
[57:08] Sorry, keep going the wrong way.
[57:11] And then we just start it.
[57:21] Okay, now it's open on Locals 3001.
[57:28] >> Oh, wow, this is funny.
[57:30] I'm just looking at the Roack documentation real quick, and it
[57:33] basically has you do -- it doesn't have you do class components.
[57:36] It has you do the -- if you were to write React from scratch, like how to
[57:41] create an element, which is more like using web components, actually.
[57:46] >> Yeah, I guess the Vue thing that I did more recently is probably a
[57:54] little more relevant then.
[57:56] >> Exactly.
[57:57] I mean, this is actually good, though, because this gives you more of an
[58:00] understanding about what those libraries are actually doing if you go
[58:03] through this exercise in the first place.
[58:05] It's not really the way you want to actually write this kind of stuff.
[58:09] But -- try it without the JSON PPP part.
[58:22] Without the S5 also.
[58:28] Oh, so we need to actually register the name to do this part.
[58:33] Because this is trying to get your name.
[58:39] We could do it with the one I just created.
[58:43] Let me just give you something real quick.
[58:48] So instead of your name, grab this from the private chat and just replace
[58:53] it with that.
[58:56] >> Amazing name.
[58:58] >> Yeah, I know, right?
[59:03] >> Okay.
[59:07] So I'm just going to kill this again.
[59:08] >> Do your last curl command.
[59:14] Let me get rid of the quotes.
[59:18] >> Whoa.
[59:19] >> There you go.
[59:21] >> We got some data.
[59:25] Beautiful.
[59:27] Okay.
[59:29] And they wanted us to put it into JSON PPP.
[59:34] >> That's just to format the output.
[59:36] It's not really that important.
[59:38] >> Right.
[59:39] Now let's add a front end.
[59:44] Could that be let's?
[59:47] >> Oh, yeah.
[59:48] >> Let's add a front end.
[59:49] >> Good catch.
[59:50] Still a couple bugs in here to find.
[59:55] Okay.
[60:12] Would I like to use TypeScript?
[60:13] Yes.
[60:17] Do I want an SRC directory?
[60:21] >> Yes.
[60:24] >> Okay.
[60:25] And you want basically all these.
[60:28] That one doesn't matter.
[60:29] You can say no on that one.
[60:30] Basically just choose the default for each.
[60:35] Yeah.
[60:37] So next is a React meta framework.
[60:40] It's by far the most popular.
[60:43] Although a lot of people complain about it all the time and hate it like most things in
[60:47] JavaScript.
[60:48] We're not even really using it to any sort of extent in this.
[60:53] It's just to get you a front end set up really quickly.
[60:57] >> Okay.
[61:11] That's the right one, right?
[61:16] Oh, yeah.
[61:19] So do I delete what I had before?
[61:23] >> Yeah.
[61:24] So you just delete everything and just -- yeah, exactly.
[61:30] >> Cool.
[61:32] >> Yeah.
[61:33] And this will just show you how to get the next app itself set up.
[61:40] Then run it.
[61:44] Okay.
[61:46] >> Cool.
[61:49] And then you can pop open that and give you a local host to open it up.
[61:54] Great.
[61:55] That's good.
[61:56] So this is just your shell.
[61:58] And then we're going to add in the logic to actually fetch the identity.
[62:03] Okay.
[62:13] So -- and then if I go back.
[62:37] >> Make sure you change the name.
[62:39] >> I will have ajc web dev hard coded in the code.
[62:42] This is the one last thing I still need to change.
[62:44] >> Okay.
[62:45] >> Yeah.
[62:46] >> So should I change that to the name that you sent me before?
[62:49] >> Sure.
[62:50] Yep.
[62:51] >> Okay.
[63:12] >> There it is.
[63:14] It's a beautiful app.
[63:16] >> Beautiful.
[63:20] >> Even gets lighter as you go down.
[63:24] Look at that.
[63:25] So fancy.
[63:28] I bet you had like a UX master work on this.
[63:32] >> Yeah.
[63:33] I mean whoever created the next template, I think that's just all I did.
[63:37] Just kept the same CSS.
[63:42] >> Okay.
[63:44] Well, you just created --
[63:46] >> A little more part, technically.
[63:50] Make sure you're -- you're going to have to fix the end point again.
[63:56] Yep.
[63:58] Yeah.
[63:59] All this -- what this does, it just puts a button so that you can click that.
[64:06] And then you also have a little loading thing while it's actually fetching.
[64:11] So you got to click fetch data underneath the -- yeah, there is a button in there.
[64:17] The CSS right now doesn't make it very clear.
[64:19] So it was good.
[64:20] You got to click where it says fetch data.
[64:22] >> Okay.
[64:24] >> And it pretty much --
[64:25] >> Look at that.
[64:26] >> You can see the loader.
[64:29] >> It's just so optimized.
[64:31] Amazing.
[64:34] All right.
[64:35] >> All right, Niles.
[64:36] >> Made it all the way to the end.
[64:38] >> So we're about -- we're an hour and five minutes in.
[64:41] >> Yeah.
[64:42] >> We made it through.
[64:44] We had some snags.
[64:46] I don't think we ever got the name registering end, did we?
[64:51] >> We can try -- let's just run the register name command one more time just to see what happens.
[64:55] I don't think we tried it since we changed that.
[64:58] So go -- yeah, that should be fine.
[65:03] Just run that guy.
[65:05] That will be the last thing to see whether that works or not.
[65:10] >> So, Niles, while that's doing its thing, how would you debug this if you were just alone figuring out what's going on?
[65:22] >> Yeah, well, first I would probably -- well, depending on which stage I actually want to debug first,
[65:35] I would make a note of which of the commands run fast and which don't, like we were talking about.
[65:42] And then I would probably put a little bit of instrumentation code in to see the data that's going in and the data that's coming out
[65:52] and also the time information so I can see what's taking a long time.
[65:56] But since we're thinking it's probably something that's happening not locally that's taking a long time,
[66:05] I would have to dive in to, like, what code is actually I'm calling in to.
[66:12] And, you know, from there I'd have to -- you know, I'd probably want to set up, like, a profiler or something or -- I don't know.
[66:26] It kind of depends what I see there.
[66:28] >> Yeah. Have you ever gone into debug mode, attached a debugger in the IDE?
[66:39] >> Yeah, with JavaScript, I think typically you can just -- on my computer I can just hit F5 and it will, like, let me step through it.
[66:47] And, yeah.
[66:53] Depends how it's set up, though.
[66:56] >> Now, wait a minute.
[66:58] Did it actually run?
[67:00] NPM run register name and it looks like it finished.
[67:03] >> Yeah.
[67:04] >> Yeah, that's because we put the DAPI address in there specifically.
[67:09] >> I thought we tried it after we had a new DAPI address, but maybe not.
[67:13] >> No, no, we did not.
[67:15] >> We just tried it after we changed the SDK version, but that didn't help with anything.
[67:20] >> Hmm.
[67:22] >> Okay.
[67:23] >> Okay.
[67:25] >> So what else did you want to do now?
[67:27] >> I think that's probably pretty good.
[67:29] I think we can call it a day there.
[67:31] I was going to see if we could -- we've got another 10 minutes, though.
[67:36] >> Specifically just to go over performance things, if you want.
[67:40] >> And we don't even have to do that on stream.
[67:42] We can just set that up as a separate task.
[67:45] But you and I, we had talked about having you look into the JavaScript SDK.
[67:53] So there's two main routes that we can go to.
[67:57] So right now the schedule is July 29th, which is coming up in three weeks.
[68:06] We are scheduled to move from test net to main net.
[68:12] So we'll have binaries to launch this and have the master node network adopt dash platform, meaning the core version 21 and the platform version 1.0.
[68:26] That's going main net starting July 29th.
[68:30] Before we get to that point, we want the JavaScript SDK to be better, obviously.
[68:39] The network should be healthier when it's on main net, should be, because the nodes are incentivized.
[68:45] But even that, I hesitate to say that.
[68:50] But regardless, we do have -- we talked about it a little bit last time.
[68:55] There's a Rust SDK and a JavaScript SDK.
[69:00] And they're both in -- if you're looking for the repo, go to platform.
[69:07] Up top, it's a pinned one.
[69:10] Yeah.
[69:12] And they're -- let's see.
[69:16] Packages.
[69:18] It's a mono repo, so it's split out into different packages.
[69:22] Okay, yeah, we have dash JS dash SDK, and then we have RS something SDK.
[69:33] Yes.
[69:35] So the Rust SDK is further along feature-wise and just stability-wise, but --
[69:44] Is that valid right here?
[69:48] Can you -- I'm sprinting too much.
[69:52] No, it's not.
[69:53] The zero needs to be deleted.
[69:56] Gotcha.
[70:00] Okay.
[70:02] Anyway --
[70:04] I noticed the little small thing.
[70:07] Yeah, I would have not known -- that was Rust code, wasn't it?
[70:11] Or was it something else?
[70:13] Toml.
[70:15] It's a configuration language.
[70:17] It's how you get -- this is like your package.json.
[70:19] It's how you get your dependencies in.
[70:21] For the Rust ecosystem.
[70:23] Yeah, I was going through these docs.
[70:25] I was thinking about creating another kind of getting started thing, like the JavaScript one with the Rust one.
[70:30] It's funny.
[70:31] You've been saying that Rust is way ahead in terms of features, but the JavaScript documentation is actually way ahead of the Rust.
[70:36] There's almost no Rust documentation at all.
[70:39] No, I believe that, because they're working on the code itself.
[70:42] And so the code for the JavaScript got set aside for coding the Rust SDK.
[70:52] But the documentation from the JavaScript, which was the original plan that we would have, you know, a robust JavaScript SDK.
[71:02] But now the plan seems to be that a lot of people -- some people in the community want to just take the Rust SDK and put a wrapper on it to use as a JavaScript SDK.
[71:15] So there will be really only one SDK, and then you'd have wrappers for every environment.
[71:21] And we -- yeah, there's an internal discussion about which approach we should do, whether we should fix the JavaScript SDK so that it performs better and more reliably,
[71:34] or whether we should just stick with one SDK, because there are several important features missing in the JavaScript SDK.
[71:44] One of the main features missing is the proofs.
[71:48] So when you're retrieving data from platform, one of the main ideas of this whole thing is that it gives you provable data that the network is storing,
[72:02] and this is the legitimate data that the network considers valid for certain data, schemas and documents, the things that we created today.
[72:13] When you're retrieving them from the SDK, the whole point was that they would be accompanied by proofs.
[72:20] Now, you don't need those proofs if you just trust the validator that you're interacting with, which is, you know, we did that DAPI address.
[72:29] We said this is the DAPI address that we want to connect to.
[72:33] So if you trust that node, then you don't need the proofs.
[72:36] But if you don't trust the node, then you need the proofs.
[72:39] So that's just one example of a feature that is not even in the JavaScript SDK, but is in the Rust SDK, or at least it will be soon.
[72:51] They just redid the proof system, so I'm not sure where they're at on that, but high level.
[72:59] Yeah, I'll have a longer conversation with you about this, maybe offline.
[73:04] We got Bloom filters, too. I love Bloom filters.
[73:08] Oh, good. Yeah, so if you know that stuff, then this is down your alley.
[73:15] So yeah, I guess I'll discuss that with you offline and see if that's something that you're interested in looking into.
[73:25] Would you know where to start with that? I guess I'll ask you that right now.
[73:28] Would you know where to start with, say, wrapping this Rust code so that you can put it into, using WasmBindGen, put it into a browser environment?
[73:41] I have not done that type of thing before, but I would start with looking up how to do that, and I can follow the instructions on that.
[73:52] I'm not sure how many roadblocks I would encounter doing it for the first time.
[73:56] I really have no idea, but I mean, I'm a little bit familiar with Wasm in terms of reading it, but I haven't tried to set it up in the browser before, honestly.
[74:10] Yeah, I thought you might be. You seem to be at the lower level of all these things.
[74:18] So anyway, we'll stop the stream there. Thanks, everybody who is watching.
[74:26] It shows that there are 38 of you, but I'm guessing a lot of those are Twitter scrollers.
[74:32] But yeah, we'll see you next time.