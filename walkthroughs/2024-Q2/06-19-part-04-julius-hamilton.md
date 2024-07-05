---
showLink: "https://www.youtube.com/watch?v=MDqbaGzIKt0"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Platform Walkthroughs Part 4 with Julius Hamilton"
publishDate: "2024-06-19"
coverImage: "https://i.ytimg.com/vi/MDqbaGzIKt0/sddefault.jpg?v=6671fdcb"
---

## Episode Description

Dash Platform walkthrough encounters technical issues, highlighting challenges in testnet development and the need for mainnet deployment.

## Episode Summary

In this episode of Dash Platform Walkthroughs, host Ryan and guest Julius attempt to work through a tutorial for creating an identity on the Dash testnet. They encounter several technical issues, including problems with the testnet faucet and network errors when trying to create an identity. The episode highlights the challenges of working with alpha-stage blockchain technology on a testnet environment. Despite not being able to complete the tutorial due to network issues, the hosts use the opportunity to discuss troubleshooting steps, the importance of reliable explorers and faucets, and the potential benefits of moving to mainnet. The episode concludes with a call for voters to support mainnet deployment to improve the development experience.

## Chapters

00:00 - Introduction and Guest Background

Julius introduces himself, discussing his background in linguistics, self-taught coding, and interest in cryptocurrency, mathematics, and philosophy. The hosts explain the purpose of the walkthrough series and the target audience for Dash Platform.

07:06 - Tutorial Setup and Initial Steps

The walkthrough begins with setting up the project environment, installing dependencies, and configuring necessary files. Julius follows the tutorial steps, with the hosts providing guidance on potential issues and best practices.

20:25 - Testnet Faucet and Explorer Issues

The team encounters problems with the Dash testnet faucet and explorer. They discuss the unreliability of testnet tools and attempt to troubleshoot by trying alternative faucets and explorers to verify transactions and balances.

35:54 - Network Errors and Troubleshooting

When attempting to create an identity, Julius encounters network-related errors. The hosts discuss the various error messages, their potential causes, and the challenges of diagnosing issues in a testnet environment. They decide to document the errors in the Dash Discord for further investigation.

43:54 - Conclusion and Reflections

The episode concludes with the hosts reflecting on the challenges faced during the walkthrough. They discuss the implications of these issues for developers working with Dash Platform and emphasize the potential benefits of moving to mainnet. The hosts encourage viewers who are voters to support mainnet deployment to improve the development experience.

## Transcript

[00:00] You're good.

[00:02] Keep your screen the way it is.

[00:03] We moved it off-screen,

[00:04] but we'll move it back on when we're ready to go.

[00:06] >> Great.

[00:07] >> But we are live.

[00:08] Welcome back to Dash Web Throughs Part 4.

[00:13] >> Web Throughs. Nice. Walkthroughs.

[00:16] >> Did I say that? That's silly.

[00:19] Didn't mean to.

[00:20] >> Today, we've got Julius with us.

[00:26] Why don't you introduce yourself a little bit.

[00:28] Julius, tell us,

[00:30] both of us and everybody who's watching who you are,

[00:34] what you do, how you found Dash,

[00:36] how you, yeah, why you're here?

[00:41] >> Well, I originally was very interested

[00:44] in linguistics in university,

[00:47] and then around 2021,

[00:50] during the pandemic and the lockdowns,

[00:53] I started teaching myself coding.

[00:56] Then I was in Berlin and I had

[01:00] some friends that were interested in cryptocurrency,

[01:03] and that was the first time I got exposure

[01:05] to the development and coding side.

[01:08] I saw they were really experienced developers,

[01:11] and I saw what they were doing,

[01:13] but I wasn't able to follow along.

[01:15] Then fast-forward a few years,

[01:18] I just started thinking more about political topics,

[01:23] and I started to get a lot more interested

[01:25] in libertarianism and anarchism

[01:28] and decentralized systems and stuff like that.

[01:32] That's when my interest in cryptocurrency got renewed.

[01:37] I still don't really know that much on the technical level,

[01:42] but I met someone in Denmark who was working

[01:45] on Cardano and talking about how it was

[01:49] a really interesting cryptocurrency from

[01:52] the algorithmic and mathematical perspective.

[01:55] I've just been learning over the years in my own time,

[01:59] more and more programming.

[02:01] What I do in most of my free time right now,

[02:04] I actually study mathematics category theory,

[02:07] which is very useful in computer science.

[02:12] That's who I am relating to, cryptocurrency.

[02:15] But what I just do in my daily life,

[02:17] I've done many different jobs,

[02:19] and I'm not really someone with a fixed career identity.

[02:23] But in the long run,

[02:25] I'm really quite interested in mathematics and philosophy.

[02:30] >> Very cool.

[02:31] >> That's awesome. You could actually think of

[02:32] cryptocurrency as an applied version

[02:35] of mathematics and philosophy in one sense.

[02:38] >> Absolutely.

[02:39] >> How did you get Brian?

[02:41] >> That's what got me into it.

[02:43] >> Cool. I was new to Utah.

[02:47] I moved here very spontaneously,

[02:48] and then I just went to this technology-themed meetup around,

[02:52] I think it was this cross-platform framework called Ionic.

[02:55] I barely remember, and Ryan was there.

[02:58] That was almost six months ago,

[03:00] and he just said to the people there,

[03:04] "We're looking for people for our Dash incubator."

[03:07] Yeah, I just got in touch.

[03:09] Since then, I've just been messaging him now and then like,

[03:12] "Hey, do you need someone to do anything for you guys again?"

[03:14] Because it just seems like my thing when I see your guys as Discord server and stuff.

[03:19] I'm always looking to get more involved.

[03:21] >> Yeah.

[03:22] >> Yeah, very cool. That's a very good history because one of

[03:26] the purposes of doing these walkthroughs is we want to

[03:31] have a good idea of how people

[03:34] experience using Dash platform for the first time,

[03:37] unscripted, and so we're going to be walking through a tutorial today,

[03:42] getting familiar with the concepts of Dash and Dash platform.

[03:48] One of the things that I was just having a conversation

[03:51] with in the previous hour with somebody was that we have,

[03:56] there are two kinds of people that I think

[03:59] are our target market with Dash and Dash platform.

[04:03] One is developers who just need an easy global state storage solution

[04:10] that is not based on any kind of corporate sign-up or anything like that.

[04:17] It's just open-source software that you can plug in and

[04:20] have global state storage for developers.

[04:23] Then there's this completely opposite side where you

[04:26] have people that are more libertarian-minded and are in it for the freedom tech,

[04:32] and maybe even have some products that they want to sell,

[04:35] and they want to make a website to sell those products,

[04:38] and how can they do that?

[04:40] Dash platform can help them.

[04:42] You have basically non-developers that

[04:45] would be smart enough and motivated enough to make a website.

[04:49] That's who we can serve,

[04:50] or we can serve developers who don't really necessarily care about

[04:54] the politics or ethics or whatever cryptocurrency,

[04:58] but they want something that is just a technology that works for them.

[05:02] >> Dash platform like decentralized storage?

[05:06] >> Yes.

[05:07] >> Okay.

[05:08] >> Yes. If you're building a web application and

[05:12] you want to have data stored globally and persistently,

[05:21] your options are typically,

[05:23] now I need to build a server,

[05:25] and I have to hook up my server to the database and figure all that out.

[05:31] Or you can use some SaaS product,

[05:35] software as a service product,

[05:37] that just does all that for you and they give you an SDK to work with.

[05:41] Anthony, maybe you have some examples of things like that,

[05:45] but then they would provide that storage solution for you as a service,

[05:52] and then you would pay and sign up with a credit card or whatever.

[05:56] That's the target that we're trying to meet here,

[05:59] is a global state storage for people that have web applications,

[06:05] but don't necessarily want to sign up for a service,

[06:08] I guess, just use open source technologies.

[06:11] With that, I think we should probably jump right in.

[06:15] >> All right.

[06:17] >> Get your screen share going,

[06:19] and if you don't already have a link, Anthony,

[06:23] maybe you could drop a link to the chat for your tutorial,

[06:29] and we'll just start walking through it.

[06:32] >> Julie, you should go back to the Stream Yard

[06:36] real quick and just pop that link open.

[06:39] >> There you go.

[06:42] >> Cool. You want me to walk through this?

[06:46] >> Yeah. We'll just let you do as much as you can without our help,

[06:52] and that will help us test the documentation.

[06:55] You can scroll down to the Setup and Configure Node project.

[06:59] We don't need to sit here and read all the beginning part,

[07:03] but this is where the first part of stuff.

[07:06] Hopefully, these commands look familiar.

[07:09] You're just setting up a blank project and installing your dependencies.

[07:14] >> Sure. There you go. That's perfect.

[07:18] Then if you could bump up your fonts on both sides a little bit, that would be great.

[07:25] >> Is that better? I can go more.

[07:30] >> I think that's good.

[07:32] >> Okay.

[07:34] >> All right.

[07:36] >> [inaudible]

[07:43] >> [inaudible]

[07:53] >> [inaudible]

[08:03] >> [inaudible]

[08:13] >> Are we going to stick with this version, Ryan?

[08:30] This is going to get us 15.

[08:32] >> No, let's bump it back down to 12.

[08:36] >> Once this is finished,

[08:39] open up your package.json and we'll tell you what to do.

[08:43] >> Okay. Is this okay?

[08:49] Six moderate severity vulnerabilities?

[08:52] >> Oh, yeah.

[08:53] >> Okay.

[08:54] >> That's chump change in most NPM world.

[08:58] >> It shouldn't be okay,

[09:01] but we're going to go with it now.

[09:03] >> Word says dev.15, change that to 12.

[09:08] >> Great.

[09:17] >> Then save that and then just run NPMI again.

[09:22] >> Just NPMI?

[09:24] >> Yeah.

[09:25] >> Cool. Then you can create the get ignore.

[09:33] >> Right.

[09:44] >> Add the following to get ignore as text,

[09:50] like it's a text file, right?

[09:51] >> Yeah, exactly. Yes, you can just copy-paste that.

[09:54] So we're using Vim within your VS code.

[09:57] >> Yeah, it's stupid, isn't it?

[10:01] >> What's that setting to see hidden files again?

[10:15] >> No, it's the dot get ignore.

[10:18] >> Oh, right there.

[10:19] >> It's right there. Yeah, you just copy-paste all of it.

[10:22] There's no steps to actually create to initialize your get repo,

[10:27] but this is just in case if you did,

[10:29] it makes sure that you don't commit your secret dash.

[10:33] >> Got you.

[10:33] >> Which is not actually secret to doing this on stream.

[10:36] There's no real test funds,

[10:37] but it's a good practice.

[10:40] All my tutorials include this step.

[10:42] >> Nice.

[10:44] >> [inaudible]

[11:00] >> Yeah, and this is something that trips up everyone.

[11:03] I'm going to modify this right now.

[11:04] When you copy this in,

[11:05] you're going to have two outer brackets you're going to have to delete.

[11:08] >> Okay, because I'm going to put it.

[11:12] >> Oh, yeah, just going to replace this whole thing, right?

[11:15] >> No, just the scripts part.

[11:17] Yeah, don't get rid of it, just the scripts part.

[11:21] >> Oh, whoops. Okay, I got you.

[11:23] >> Then delete the outer bracket,

[11:29] add a comma at the end of the scripts.

[11:32] >> Cool. The indentation is okay?

[11:35] >> It's fine. Then you should be good.

[11:43] >> Cool.

[11:46] >> Oh, shoot.

[12:13] I set it right here. Okay.

[12:15] >> Echo network testnet 2.env.

[12:18] >> Don't worry about that. So some wonky is happening here

[12:30] because we started off where you're creating, so.

[12:36] >> Oh, I created the wrong one.

[12:38] >> Dash examples, yeah.

[12:43] >> Is that okay?

[12:46] >> Yeah. Yeah, it should be good now.

[12:50] >> Just a bit of a disclaimer.

[13:00] I am not super skilled with JavaScript,

[13:03] but I do have a little bit of experience.

[13:06] >> Yeah, ideally, the tutorial setup is that you can just copy,

[13:11] paste, and everything should work.

[13:13] So someone who literally has never even

[13:15] coded before should be able to follow along.

[13:17] That's how I write all my tutorials that way.

[13:20] So this is putting us to the test.

[13:22] >> Okay. So do you want me to copy and paste,

[13:23] or do you want me to type it out to learn better?

[13:26] >> No, you can copy and paste.

[13:28] >> Okay.

[13:28] >> Yeah.

[13:29] >> Because I don't mind typing it out.

[13:31] >> I appreciate that impulse,

[13:34] but just for the sake of time.

[13:35] >> Sure, sure.

[13:36] >> Because there's going to be some pretty chunky scripts later on

[13:39] that would require a certain amount of time.

[13:42] >> So you don't want me to read through this and try to understand the code?

[13:45] >> Well, what you could do is just be like,

[13:47] what do you see here?

[13:48] What do you think is happening?

[13:49] >> Okay. Importing dash,

[13:53] I understand more or less,

[13:55] but that's probably a node package, right?

[13:57] >> Correct.

[13:59] >> But I guess I already installed it. Yeah, okay.

[14:01] Constant network equals processed environment.

[14:04] Is that like a global variable or something?

[14:06] >> So that's what's in your.env file.

[14:09] >> Okay. Export, that's because this is a module,

[14:13] so we can import it from other files.

[14:16] Client is new dash client.

[14:19] Network, mnemonic, offline mode, true.

[14:24] I know Bitcoin and Ethereum and stuff,

[14:28] they have different networks,

[14:30] so I guess dash has multiple options for the network.

[14:34] >> Go back to your.env file.

[14:39] >> You can save that file also.

[14:42] So you see how we have network set to testnet,

[14:44] and this is because the dash platform

[14:46] only exists in testnet version right now.

[14:48] So testnet is where you have a fake pretend version of the chain,

[14:53] where the money is all made up,

[14:55] like who signs in AOA, points are all made up.

[14:57] >> Okay.

[14:58] >> Yeah.

[14:59] >> Cool. The mnemonic,

[15:02] is that your password sort of?

[15:06] >> Yeah.

[15:07] >> Okay. All right.

[15:09] Well, yeah, that's fine.

[15:11] So to get a new address for an existing wallet,

[15:23] so I thought that with blockchains and stuff,

[15:28] the wallet is essentially your public key, right?

[15:35] >> Yeah. You can define it in different ways,

[15:38] but wallets are a combination of public-private key pairs.

[15:45] So the mnemonic is just the thing that

[15:48] generates those public-private key pairs.

[15:51] >> It's that 16-word thing they make you write down?

[15:55] >> Yeah. That's exactly what it is, a 12-word.

[15:58] >> Okay, cool.

[16:01] >> So the -sdk that you imported, the npm package,

[16:06] that will do all the work for

[16:08] the derivation of the key pairs under the hood.

[16:11] >> Okay.

[16:12] >> As contacting -platform.

[16:15] >> Yeah. When you generate a new address for an existing wallet,

[16:20] is it some kind of algorithm which can generate

[16:23] different hashes or whatever for the same mnemonic?

[16:31] Sorry if that doesn't make sense.

[16:34] But it's saying, okay,

[16:36] so the mnemonic generates

[16:38] the public and private key pair?

[16:42] >> Yes.

[16:43] >> Right. But is it going to do that in an identical way every time?

[16:47] Because it's a new address.

[16:49] >> Yeah. It will generate them deterministically.

[16:56] >> Okay, cool.

[16:57] >> Specific algorithm. So every time that you generated the first address,

[17:00] you'd get the exact same first address every time.

[17:03] >> Okay, cool.

[17:05] >> [MUSIC]

[17:15] >> [MUSIC]

[17:25] >> [MUSIC]

[17:45] >> So getWalletAccount is like what's it actually getting?

[17:53] >> This is actually - so the getWalletAccount

[18:00] is basically just deriving those public-private key pairs.

[18:05] That's probably the easiest way to explain that.

[18:08] >> Okay.

[18:11] >> You don't - yeah, we've got like -

[18:15] >> I don't need to worry about this?

[18:17] >> What's that?

[18:19] >> Were you going to say, I don't need to worry about this?

[18:21] >> You don't have to worry about every detail of it,

[18:24] because that will probably push us over

[18:27] the edge based on what we know is the duration of the tutorial.

[18:34] Do feel free to ask questions that you are curious about along the way.

[18:40] But we can also circle back to things after we've -

[18:45] like maybe when we're waiting for scripts or after we've done certain things.

[18:50] Because a lot of times it's easier to explain after we've concrete steps then.

[18:56] >> Cool. All right. So just copy and paste this createWallet.js script.

[19:01] >> Yeah. That's just going to create your public-private key pairs,

[19:05] so that we can get terms and whatnot.

[19:08] So yeah, part of this process is also like we'll

[19:14] probably rush it a little bit more than you would,

[19:17] if you were working on this on your own.

[19:20] Yeah, we do want to test whether the tutorial itself is.

[19:25] >> What I was going to say is we want to

[19:32] test whether the tutorial itself makes sense.

[19:35] But I'll keep going.

[19:37] So right here,

[19:39] what you're going to want to do is what you got outputted,

[19:41] you're going to want to copy-paste those two things and put them in your .env.

[19:45] This is going to happen throughout the tutorial.

[19:48] Every time you have an all caps with underscores thing,

[19:51] those are environment variables that we're going to copy-paste into our .env.

[19:57] Great.

[20:05] God's just smited you, Ryan.

[20:14] >> Yeah, for sure.

[20:16] I don't know what that was, but I'm glad it didn't happen to you guys either or also.

[20:20] >> Okay. You want to lead him through the test net faucet part?

[20:25] >> Yeah. Well, just keep going.

[20:32] >> Everyone's favorite faucet.

[20:34] >> While you're doing that,

[20:35] you just keep doing what you're doing,

[20:37] but I'll just mention that

[20:39] the test net faucet is not the greatest faucet in the world.

[20:43] >> Okay.

[20:45] >> It will crash and look like it didn't work,

[20:49] but that means it works and sometimes it actually doesn't work.

[20:52] We'll see if the test net gods are with us today.

[20:56] >> Cool. Send test funds to

[20:59] the unused address from the console output using dashes test net faucet.

[21:08] >> Yeah. You should have seen something in your console output to get your address.

[21:17] >> Yeah, and I put that in my environment file.

[21:20] Should I go to this link?

[21:21] >> Yeah, correct.

[21:23] Then unintuitively, the address field is above the CAPTCHA.

[21:33] >> Okay. I got you.

[21:36] >> Paste that in there and then you can use a promo code.

[21:42] Type in masternode, just one word,

[21:48] and then go ahead and get coins.

[21:55] It'll hang for a little bit,

[22:01] but you should get the coins.

[22:05] >> While you're doing that, we'll wait here for a little bit.

[22:09] >> Have you ever used a faucet before?

[22:12] >> Maybe. I'm aware of the concept,

[22:14] but I don't really remember if I actually used one or not.

[22:18] >> Your knowledge of blockchain specifically is actually beyond some of

[22:23] our other guests despite being a fairly new dev, so that's good.

[22:29] I was the same way. I first got into

[22:32] blockchain before I even knew how to code at all.

[22:37] >> What did you say?

[22:39] >> I first got into blockchain stuff before I knew how to code at all.

[22:43] >> Oh, really?

[22:44] >> It was extremely confusing.

[22:46] >> That's interesting.

[22:48] >> It was back in 2017 when there was the first big,

[22:55] so that's good. That means it worked.

[22:57] The first big Ethereum run-up is when I got into it.

[23:03] >> Let's keep going on the thing.

[23:06] >> You guys see this? This page isn't working.

[23:09] >> Yeah, that's what I was warning you about.

[23:11] Sometimes that happens.

[23:13] >> Okay.

[23:13] >> Skip the whole Explorer step.

[23:16] >> Search for your wallet address, blah, blah, blah.

[23:19] Are we going to assume that my wallet receives funds or?

[23:23] >> Yeah.

[23:24] >> Okay.

[23:25] >> Yeah, let's just move on to the next script.

[23:31] >> Anthony, I wonder if we could,

[23:40] yeah, never mind. That's too much.

[23:44] In theory, we could be able to write some script in

[23:47] your tutorial that just gives us the coins,

[23:50] but we won't worry about that.

[23:52] >> For the faucet step?

[23:56] >> Yeah, essentially.

[23:58] >> I would like to do that, yeah.

[24:01] >> Yeah, because it's a bad experience to do that whole faucet thing.

[24:07] But I'm waiting for two days from now.

[24:11] There's a proposal that is deciding whether we're going to

[24:16] release Dash Platform onto mainnet soon or later,

[24:21] and I think it's stating that it's soon.

[24:24] Hopefully, we won't have to deal with testnet for very much longer anyway.

[24:29] >> Well, we still would because then people

[24:32] are going to have to pay money to do this.

[24:34] >> True, but it's not going to be that expensive,

[24:37] so I would expect it to be less than a dollar of all of the playing around.

[24:42] >> Interesting.

[24:43] >> We can just, I can just send them.

[24:46] >> That would be great actually,

[24:47] because then we could have them get set up with a wallet,

[24:51] and then we send them a couple of dollars,

[24:54] and then when we need to pay them at the end of the stream,

[24:55] they'll already be good to go. I like that.

[24:58] >> Yeah, yeah, yeah.

[25:00] >> [inaudible]

[25:29] >> Error, MTSPV chain?

[25:32] I mean, yeah.

[25:43] Do you want me to copy this error message into the messages?

[25:51] >> I know. Scroll up and see what you ran.

[25:55] NPM run create identity,

[25:57] and have you saved your create identity file and everything?

[26:02] Do we have all the environment variables on there?

[26:05] >> Yeah, go back to your .env.

[26:08] Works to be good to me.

[26:13] >> Doesn't need commas or anything?

[26:15] >> No. I've seen SPV.

[26:19] I think this is what it said.

[26:20] I've seen errors like that before when test that's down.

[26:26] >> Well, Anthony, you can

[26:29] maybe help troubleshoot for him for a little bit.

[26:31] I'm going to look and see if there's

[26:33] anything going on with testnet right now.

[26:40] I'm just going to spin up my own wallet and run one real quick.

[26:58] >> Can you bring up a website, Julius,

[27:14] for go to testnet-explorer.com?

[27:23] >> Can't be reached.

[27:37] >> Anthony, can you get there?

[27:42] Because I can never reach it personally

[27:44] because my office firewall settings don't allow it.

[27:47] But are you able to go to testnet-explorer.com?

[27:52] >> Yeah. Let me just double-check

[27:55] to make sure that's the right URL.

[27:57] [wind]

[28:07] [wind]

[28:17] [wind]

[28:27] [wind]

[28:37] [wind]

[28:47] So this is where we're supposed to be going.

[28:50] Oh, I don't know what I told you to write.

[28:52] Did I say...

[28:54] [indistinct]

[28:56] But no, you shared Platform Explorer.

[28:58] Platform-Explorer.com, that's what's not working for you?

[29:02] No, Platform Explorer works.

[29:04] Yeah.

[29:14] So, should I use this?

[29:20] So this is showing, yeah, that's showing that it looks like,

[29:24] it looks like platform is up.

[29:31] Let's see when the last transaction was.

[29:37] If you scroll down just a little bit further,

[29:39] let's see what the date is on the latest transaction.

[29:44] Documents past 4.17 p.m.

[29:47] We should try and verify whether he got his funds or not,

[29:51] because I just ran the faucet and got a new error I've never gotten before.

[29:55] It says something went wrong, could not send you Dash.

[29:57] Please try again later.

[29:59] Oh, really? I wonder if...

[30:01] So let's actually, real quick, can you pop your address into the chat for us?

[30:08] Your wallet address.

[30:17] But even still, if that was the error, the error would say you have no funds.

[30:21] That's an error that usually works correctly.

[30:28] It's saying here you have no funds, but I'm not sure,

[30:31] because I can't trust this testnet explorer,

[30:34] because it doesn't usually say correctly whether we have funds or not.

[30:39] Yeah.

[30:46] Did you check it, Anthony, to see if it does?

[30:49] What does it say?

[30:51] It says he has zero funds.

[30:53] Okay.

[30:55] But then the error should say, when you create an identity,

[30:58] it should say you do not have the available funds to do this command.

[31:02] I'm going to go to the -- you can do this also, Anthony.

[31:08] Are you guys still there? Okay.

[31:09] Yeah, go to the faucet yourself, Anthony, and try to send him some coins.

[31:18] Did you already do that?

[31:21] I tried to send myself some coins.

[31:24] I'm going to try to send him some coins just with the address that he has.

[31:27] Oh, interesting.

[31:28] When I refresh, though, it said no more Dash for you.

[31:30] Come back in one hour, which is what it says when it works.

[31:33] Okay.

[31:34] I just ran the create identity command on my own computer.

[31:37] We'll see what happens.

[31:39] Okay.

[31:41] We'll get through this.

[31:43] So real quick, let's switch screens to mine.

[31:47] Okay.

[31:48] So in my case, because the faucet broke,

[31:52] it says here not enough balance to cover the burn amount.

[31:56] So the fact that you didn't get this error leads me to believe your faucet

[32:01] command did work, but you're getting a different error,

[32:04] which is related to the chain itself.

[32:07] Because this is the error you would get if you did not have funds,

[32:09] even though if you go search your address, which is this one,

[32:13] it says you have no funds, which is incorrect.

[32:18] So I think the testnet explorer is just slow or doesn't get new

[32:23] information fast enough.

[32:25] So I don't know, man.

[32:40] What's the address that you're looking at for the, for the,

[32:44] for your testnet?

[32:47] It's the testnet.networks.org,

[32:52] colon 3,001 for slash insight.

[32:57] Okay.

[33:01] I'm going to, I'm going to go there and see if it,

[33:04] what it shows on my side.

[33:13] Yeah, zero, zero dash.

[33:19] So I wish we had a different one to check it against.

[33:28] I know we've had multiple ones in the past.

[33:33] Do you have them documented?

[33:35] Do you have a different URL Anthony for a different testnet explorer?

[33:41] I mean, this is the one you, this is the one you've told me works.

[33:45] I know I have in there previously.

[33:47] I just had the, whatever you get from the docs.

[33:52] Yeah, that's the one I was looking for.

[33:54] If you have, you have that handy.

[33:57] I'm just having Google testnet.

[34:06] So I'm Julia.

[34:07] Google dash testnet.

[34:27] Just test net, not faucet.

[34:29] Yeah.

[34:30] Maybe that would be better.

[34:33] Let's go to the one that's in the docs.

[34:38] Okay.

[34:39] So just click the very first link.

[34:57] So what would you like me to do?

[35:00] So we're looking for a link to the right there.

[35:03] It should be testnet for, let's see.

[35:10] Yeah.

[35:11] Yes.

[35:12] Oh, that's a different faucet.

[35:14] But do we have a different explorer?

[35:16] We're looking for testnet insight.

[35:19] Do those ones.

[35:20] Try all of those.

[35:27] And then pop your address in there.

[35:37] Okay.

[35:38] Zero.

[35:43] And Anthony, you said you verified somehow that I actually did have.

[35:47] Oh, no, you thought because the error message I got.

[35:49] The error message you got implies that you do have the funds.

[35:54] Because if you did not have the funds, your error message would tell you.

[35:57] So.

[35:58] Okay.

[35:59] Even though all these explorers say that I don't.

[36:01] You don't think they're reliable.

[36:02] I don't think they're reliable.

[36:04] Correct.

[36:12] So I need to try and find a different faucet so I can get some funds.

[36:15] So I can verify whether I can create an identity.

[36:20] Let's try this crowd node one.

[36:22] I've never tried some before.

[36:25] Yeah.

[36:26] Let's try that one to get funds into his wallet.

[36:35] It doesn't work a lot better, actually.

[36:37] Success.

[36:38] You've been awarded 16 T dash.

[36:41] That's a good sign.

[36:42] That's a good sign.

[36:44] Yeah, I might switch out.

[36:51] Please make a note of that, Anthony, that to use crowd nodes faucet in the tutorial itself so that we don't have to go looking for it again next time.

[37:09] Okay, now go back to an explorer and see if you've got funds in there.

[37:14] I know the explorers are unreliable also, but let's just check it.

[37:23] You may have to zoom out or something to see the input field.

[37:29] The input field.

[37:30] Oh, you're using the same address, so it shouldn't matter.

[37:34] Yeah, just refresh, I guess.

[37:40] So, Anthony.

[37:41] I have it.

[37:42] Yeah, we got it.

[37:43] We got it now.

[37:44] 21 dash.

[37:46] Cool.

[37:47] I just I got it.

[37:48] I tried to create the identity.

[37:50] I got a different error message.

[37:52] It says request to this IP address failed reason certificate has expired.

[38:00] This is, this is definitely a network issue.

[38:05] All right. Well, now that I have it.

[38:08] I'll try that command again.

[38:11] Right, yeah.

[38:14] It's just, it's just so, so interesting because the network is broken for both of us but the network is throwing completely different errors to us.

[38:22] Yeah, hit hit enter on that, that command. Julius, see what happens.

[38:32] SPV or empty SPV chain on handled error event.

[38:37] Is it just a typo throughout er.

[38:41] No, this is, yeah, this is a.

[38:44] This is a network issue.

[38:52] Running on a node JS environment without any stuff that's unrelated after that, that's that it says that every time.

[38:59] Okay.

[39:01] Yeah, no, this is where we're stuck here, this is, this is all this is as far as we're going to be able to get this.

[39:07] Well, hang on.

[39:10] So, Anthony, I, I only see one transaction in the insight explorer.

[39:16] Did you see more on your screen, Julius.

[39:20] What I'm seeing, we just barely only got test net funds into that address.

[39:28] But if the issue was the test net funds, it would give him an error saying he does not have the funds that that is an error that does work correctly.

[39:35] It's these all it's these other weird obscure errors that it throws with the network is just broken.

[39:43] Yeah, I personally, I wouldn't I didn't know that the you don't have funds error is reliable enough because.

[39:53] You might get an error that doesn't look like that.

[39:57] That's that error has consistently been reliable for me in the past, anytime I've tried to do things without the funds.

[40:04] It will tell you when you do have the funds, but the network is flaky.

[40:09] It will throw these errors that don't make any sense.

[40:12] That will say something like certificates expire with a random IP address or SPF chain errors or things like that.

[40:19] The whole host of random errors you get that are related to the network being down.

[40:25] Well, let's let's take some time then, I guess, right now.

[40:28] And Julius, do you have are you on the dash discord?

[40:33] Yeah. If you can, I guess, pop that open and you can do it off screen or whatever to get to your dash discord.

[40:49] Yeah, just get to the dash discord. And then. We'll we'll drop this error into the.

[41:01] There it is up top. I go to go to Dev talk.

[41:12] And then just, yeah, copy the error and dump it in here and ask if there's anybody that might know what this is all about.

[41:26] And that way we'll have it on record, at least. Cool.

[41:32] Did we get the same error? I believe so.

[41:36] Yeah. Yeah, the same error both times. Double check. But it was definitely SPV error, empty SPV chain.

[41:44] But I guess we can check very carefully. Deprecation warning. Yes.

[41:51] Wait a minute. I wonder if this is related to the SDK that we're using.

[41:55] Did you when you changed the Anthony, do you remember when we changed to the SDK?

[42:02] It doesn't matter. I'm running 15 on my machines, running 12 on his. We both got errors. They were different.

[42:08] So maybe they throw different errors, but the chain is down. This is an issue with the chain.

[42:12] I've had enough issues with the chain to know when the issue is with the chain.

[42:16] No, I know. I know it's an issue with the chain, but it might be. Yeah, I guess.

[42:27] We've run into issues with the chain before, is what I'm saying. We've run into issues with the chain where fixing,

[42:33] like changing the SDK did work. Correct.

[42:38] We have not been in a situation where changing the version actually fixed it.

[42:42] The chain is either up or the chain is down. The times where it's been down, we came back the next day and it was up.

[42:48] The way we fixed it was by coming back another day.

[42:52] OK, well, I just had him paste that error in there, so I actually.

[42:57] And I know what they're going to tell you. They're going to tell you, try it again later.

[43:02] All right. Well, we'll probably cut the stream short then today, because if we can't get past this, cut everything up to the node events.

[43:12] So it says node events, delete everything above that. Oh.

[43:20] Where's node events? To where it says. Oh, here we go.

[43:24] Yeah. Yeah. So keep that. That's the actual error message. Delete everything above that, because I see you're over the message limit.

[43:30] Yeah, that that should work. And do three back ticks above and below it so that it codifies it.

[43:39] Not one? Three. OK, yeah.

[43:44] And then three at the bottom. Yeah. Yeah, I see.

[43:49] We'll make you a developer in no time. It's still above the limit, I think, but it will work.

[43:54] No, he's good. Yeah. Cool.

[43:59] But yeah, I think I think we should we should probably call it here. All right.

[44:05] OK. All right. Well, I'm available for.

[44:14] Appreciate you, Julie. It's been a great sport. Hopefully we'll be able to get you back on and get further in the tutorial.

[44:20] I'd love to. And I mean, if you help debugging it or something.

[44:27] No, this is kind of out of our hands right now, so we'll we'll just we'll see if anybody can give us a definitive answer on why we have run into this one.

[44:36] But, you know, this is part of the process where this is alpha stuff.

[44:40] So we're we're at least trying to help show that there are some errors and here's the error that we got.

[44:50] And maybe that will help DCG debug something. But real quick, what was the discord channel that this is posted in the dash?

[45:00] Yeah. The dev talk channel of the dash is cool because I'm going to show that I'm getting a different error message.

[45:08] Cool. And where is this video going to be posted?

[45:12] I just just because I want to see it. Yeah, I'll drop a link.

[45:19] It's already. Yeah, it's on YouTube and Twitch and Twitter as well.

[45:26] So we'll drop a link to you. But everybody else for watching.

[45:30] If you're watching and we had success last time all the way through the tutorial.

[45:36] This time we got hung up on the first step, essentially. So.

[45:42] Kind of par for the course. I mean, we've had two others that didn't get all the way through.

[45:47] The last one that we did get through was kind of the anomaly. So, yeah, we'll work through it.

[45:54] But hopefully we can get on mainnet sooner than later.

[45:57] So if anybody's watching that is vote is a voter, make it known that being on mainnet would help the situation a little bit, at least.

[46:07] So thanks, everybody, for tuning in. We'll catch you next time. Thank you.
