---
showLink: "https://www.youtube.com/watch?v=0NfH2B2MXxs"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Code Hangout: Next-Gen DASH Tools #10: DashKeys.js CLI & Browser JavaScript"
publishDate: "2023-02-02"
coverImage: "https://i.ytimg.com/vi/0NfH2B2MXxs/maxresdefault.jpg"
---

## Episode Description

This episode covers the development of Dash Keys, a library for generating and managing cryptocurrency keys and addresses for the Dash blockchain.

## Episode Summary

In this lengthy coding session, the developer works on finalizing the Dash Keys JavaScript library and CLI tool. Key tasks include refining the README documentation, implementing core cryptographic functions, creating a glossary of terms, and structuring the codebase. The developer dives deep into the mathematics and implementation details of public key cryptography, exploring concepts like curve points, compression flags, and checksums. Throughout the session, there is an ongoing effort to balance comprehensive functionality with clear, concise code and documentation. The episode showcases the intricate work involved in building cryptographic tools for blockchain applications.

## Chapters

00:00 - Introduction and Setup

The stream begins with the developer setting up their environment and dealing with some technical difficulties related to camera and streaming software. They briefly introduce the Dash cryptocurrency project and explain the goals for the coding session ahead.

04:13 - Working on Dash Keys CLI Documentation 

The developer starts working on improving the README documentation for the Dash Keys command-line interface (CLI) tool. They refine the usage examples, structure the content, and ensure the information is clear and comprehensive for users.

47:53 - Refactoring Core Cryptographic Functions

This chapter focuses on refactoring and optimizing the core cryptographic functions in the Dash Keys library. The developer examines functions for generating keys, converting between formats, and implementing cryptographic operations, aiming to improve efficiency and readability.

91:47 - Deep Dive into Public Key Cryptography Implementation

The developer does a deep dive into the mathematics and implementation details of public key cryptography. They explore concepts like elliptic curve points, scalar multiplication, and compression flags, working to understand and document these complex operations.

146:41 - Creating a Comprehensive Glossary of Terms

This section involves creating a detailed glossary of cryptographic terms and concepts relevant to Dash Keys. The developer carefully defines and explains key terminology to assist users in understanding the library and the underlying cryptographic principles.

199:47 - Finalizing Documentation and Project Structure

In the final stretch, the developer focuses on polishing the overall documentation, ensuring consistent formatting, and structuring the project for clarity. They also make decisions about which utility functions to include and how to organize them within the codebase.

259:00 - Wrap-up and Next Steps

The developer summarizes the progress made during the session, outlines the remaining tasks to complete the project, and discusses plans for publishing the library. They reflect on the day's work and set goals for the next coding session.

## Transcript

[00:00] (upbeat music)
[00:02] (upbeat music)
[00:05] the (upbeat music)
[00:10] (upbeat music)
[00:12] the (upbeat music)
[00:15] the (upbeat music)
[00:17] the (upbeat music)
[00:20] (upbeat music)
[00:22] the (upbeat music)
[00:27] the (upbeat music)
[00:32] the (upbeat music)
[00:37] the (upbeat music)
[00:42] the (upbeat music)
[00:47] (upbeat music)
[00:50] (upbeat music)
[00:53] (upbeat music)
[00:55] (upbeat music)
[00:58] (upbeat music)
[01:00] (upbeat music)
[01:03] (upbeat music)
[01:05] (upbeat music)
[01:08] (upbeat music)
[01:15] (upbeat music)
[01:24] (upbeat music)
[01:33] (upbeat music)
[01:36] (upbeat music)
[02:00] (upbeat music)
[02:03] (upbeat music)
[02:17] (upbeat music)
[02:29] (upbeat music)
[02:32] (upbeat music)
[02:42] (upbeat music)
[02:52] (upbeat music)
[02:55] (upbeat music)
[03:05] (upbeat music)
[03:16] (upbeat music)
[03:18] (upbeat music)
[03:36] (upbeat music)
[03:39] (upbeat music)
[03:41] (upbeat music)
[03:44] (upbeat music)
[03:47] (upbeat music)
[04:13] (upbeat music)
[04:16] Well, what, what, what?
[04:26] No, no, no, no, I tested this.
[04:30] Come on.
[04:33] Don't give me this now.
[04:35] Oh, come on.
[04:40] Am I gonna have to restart?
[04:42] Please don't make me restart.
[04:43] Hold on one second.
[04:48] I don't know what happened.
[04:50] My camera app says it's running and connected.
[04:53] Let me quit and restart the camera app.
[04:57] Camera app restarted.
[05:00] Anyway, we're gonna be working on the same thing
[05:01] we were working on before.
[05:03] We're gonna finish up the CLI,
[05:05] publish both these modules,
[05:06] get back to Dash HD.
[05:08] That's the goal.
[05:08] Okay.
[05:12] (upbeat music)
[05:14] Come on.
[05:15] Where's Cast Cable?
[05:16] You gotta be kidding me.
[05:21] We're live.
[05:22] Can't see anything.
[05:24] You know, I might just try this crazy feature.
[05:28] See, okay.
[05:29] It's saying that it failed.
[05:30] So something wacky donk is going on.
[05:32] I tested it before we started.
[05:37] I promise I did.
[05:38] It was working.
[05:40] Moments ago, it was working.
[05:42] All right.
[05:45] Give me just a second here.
[05:46] Do do.
[05:49] Oh, this is gonna sting.
[05:54] All right.
[06:03] Let's see what we can do.
[06:04] All right.
[06:08] Camera's fine this time.
[06:09] It's the software.
[06:10] The software is what's being wonky donk.
[06:12] And I'm gonna see, can we,
[06:16] I'm just gonna try adding the source again
[06:18] 'cause the source disappeared.
[06:21] So we're gonna try adding, re-adding the source.
[06:23] Okay, camera's back.
[06:24] So I think this one might go to OBS.
[06:28] You know, when you got a system of faulty software
[06:31] that's not working, you know.
[06:34] Or, okay, let's try this.
[06:39] (upbeat music)
[06:41] All right, here we go.
[06:45] Here we go.
[06:46] Oh, new phone.
[06:50] We're just gonna do this one, I think.
[06:53] Let's see if,
[06:56] how that works out.
[07:01] Oh, big head.
[07:02] Big head.
[07:04] Don't worry, we're gonna get it.
[07:09] We're gonna get it.
[07:10] I promise, I'm not wearing makeup.
[07:15] It's just how iPhone makes it look, you know.
[07:19] It's how iPhone do.
[07:22] Let's see here.
[07:24] Okay.
[07:32] Oh, that's not it.
[07:35] (upbeat music)
[07:37] Here we go.
[07:45] Sorry for the holdup, folks.
[07:48] Well, continuity camera's working pretty well, I might say.
[07:53] Let's see.
[07:56] Oh, that looks so weird, though.
[08:00] I look so like I'm wearing makeup,
[08:03] but I'm not wearing makeup, I promise.
[08:05] I'm really not wearing makeup.
[08:07] That's not how I roll.
[08:08] You know, not that I've got anything
[08:11] against people who do wear makeup, but.
[08:13] There we go, now that's,
[08:20] that's in, great.
[08:22] Oh, whoops.
[08:23] Sorry for the technical difficulties.
[08:27] What do you do, you know?
[08:28] It's just, such is life.
[08:31] (upbeat music)
[08:33] All right, so we're gonna ignore the fact
[08:38] that I look like I've been tanning.
[08:41] (laughs)
[08:42] Oh, good old AI.
[08:44] Good old AI images.
[08:47] Yes, yes, make me look as much like a woman
[08:49] as you possibly can.
[08:51] Look, look, it looks like I'm clean shaven.
[08:55] And I kind of am, I've got a five o'clock shadow,
[08:57] but you can't tell in the picture.
[08:58] Anyway, all right, so enough dealing with the camera crap,
[09:02] I guess, maybe.
[09:03] I'm gonna try one other thing real quick.
[09:05] I'm gonna click okay on that.
[09:07] Open this back up and look and see.
[09:10] Yep, it is still absolutely 100% not letting me use
[09:14] my main camera.
[09:17] So I'm just gonna turn that off real quick
[09:19] and we'll get started.
[09:20] (groans)
[09:24] I'm also gonna see if I can
[09:27] that turn off, I've got some filtering on here.
[09:32] Okay, that's a little bit better.
[09:35] That's a little bit better.
[09:37] There we go.
[09:39] All right, and I'll figure out later.
[09:41] Probably have to restart the computer
[09:44] in order to get that working again, but whatever.
[09:47] Okay, so here we go.
[09:49] Thanks for joining in, everybody.
[09:53] Let's go ahead and have a quick word
[09:54] from our not really a sponsor, not a sponsor,
[09:58] Mr. Mountain Dew, pop it up, my friends.
[10:00] And this is April Fool's Dew.
[10:02] That's right, it's diet caffeine-free.
[10:05] It's like drinking water, but more toxic.
[10:07] Mm.
[10:10] No focus in that, but a hint of fake orange juice.
[10:17] Excellent.
[10:18] All right, so where was I here?
[10:21] I think I was just finishing up.
[10:24] Nope.
[10:25] We were not gonna have all these things here.
[10:29] Wiff to private key, so a lot of this stuff
[10:33] is actually gonna move back over to the other readme.
[10:37] So we're gonna have some CLI.
[10:43] All right.
[10:52] And then we're validating.
[10:54] Wiff to adder.
[11:00] That's it.
[11:06] That's all this is really responsible for.
[11:08] All the other stuff.
[11:09] Wiff to adder.
[11:12] Adder to pub key hash.
[11:18] PKH, there we go, that's that.
[11:22] How y'all doing tonight?
[11:23] What's up?
[11:24] What brings you here?
[11:25] All right, validate base 58 check addresses.
[11:29] And now...
[11:33] Wiff and payment addresses.
[11:43] Base 58 check.
[11:46] (keyboard clicking)
[11:49] Let's see.
[11:53] Ah, actually.
[11:54] Private key import format.
[12:16] There we go.
[12:17] All right, that's good.
[12:32] So we're down to that.
[12:34] We got the help here.
[12:35] We've got the addresses.
[12:40] Let's see.
[12:45] (upbeat music)
[12:48] We got some...
[12:59] I was gonna fill out the examples here.
[13:01] That's where we were leaving off, I think.
[13:05] Was I was gonna do dash keys, inspect, dash dash JSON.
[13:15] I was gonna show what that example looks like,
[13:16] which I think is somewhat like this.
[13:19] So let me go ahead and grab that real quick.
[13:21] Dash keys dot JS.
[13:30] Cool.
[13:32] So where was that at?
[13:37] Right here, here's the inspect, JSON.
[13:42] And then I think, valid, true, compressed, true.
[13:47] All right.
[13:48] That looks good.
[13:54] Gonna get rid of this.
[14:00] I was going to...
[14:04] All right, generate a key.
[14:11] (upbeat music)
[14:13] This is for development.
[14:36] There's nothing wrong with these keys.
[14:41] They're just not HD keys.
[14:46] (upbeat music)
[14:48] Perfectly tested.
[15:08] Perfectly is a strong word, fully tested.
[15:12] (upbeat music)
[15:15] Okay, there we go.
[15:20] Generate a key.
[15:24] Okay, there we go.
[15:41] And I kind of would like to do this, dash wallet.
[15:45] And then I can do like that, dash wallet,
[15:50] just to make this a little easier to read.
[15:53] All right, dash HD.
[15:55] And here we are.
[15:59] Okay, cool.
[16:00] Moving right along there.
[16:04] (upbeat music)
[16:34] All right.
[16:35] Okay, inspect JSON.
[16:46] And then I want to show inspecting a WIF as well.
[16:54] Verify a pub key hash.
[17:02] Verify a WIF file.
[17:07] Inspect a pub key hash as JSON.
[17:27] Inspect a WIF.
[17:28] Let's see.
[17:49] (upbeat music)
[17:52] And then let's have inspect a WIF unmasked.
[18:06] And then note, there's a lot of debug information also.
[18:11] And then note, there's a lot of debug information also.
[18:16] Fields as well.
[18:27] Let's see, note.
[18:41] The XY debug fields are there for those
[18:46] show values, show incorrect values
[18:55] that come from common.
[19:02] So show incorrect values.
[19:07] (upbeat music)
[19:10] Are common mistakes.
[19:22] To help those developing their own
[19:27] key library in other languages.
[19:37] And what is, I forget, what is base 58 check BIP?
[19:42] Do we have BIP 38?
[19:49] What is BIP 38?
[19:51] Okay.
[19:58] (keyboard clicking)
[20:01] Maybe instead of unsafe, I could call it unmask.
[20:26] (keyboard clicking)
[20:28] 'Cause it's not that there's anything unsafe about it.
[20:31] Okay, and then let me go grab from this other readme.
[20:43] (keyboard clicking)
[20:46] (sighs)
[20:48] (keyboard clicking)
[20:51] (upbeat music)
[20:54] (keyboard clicking)
[20:57] (upbeat music)
[20:59] (keyboard clicking)
[21:05] There we go.
[21:26] (keyboard clicking)
[21:28] And then let's do, let's see, .wif.
[21:32] Oh, address, right, okay.
[21:39] Let's do that one too.
[21:41] That's probably one of the more important ones.
[21:44] Oops, that's not what I wanted.
[21:48] There we go.
[21:50] (keyboard clicking)
[21:53] (upbeat music)
[21:56] There we go.
[22:20] (keyboard clicking)
[22:24] (upbeat music)
[22:26] Verify, so wait, we've got verify,
[22:37] then we've got inspect.
[22:38] And we want to inspect unmask, there we go.
[22:45] (keyboard clicking)
[22:50] (upbeat music)
[22:53] So here we go.
[22:55] Let's go ahead and inspect this
[22:57] and we'll inspect it masked and unmasked.
[22:59] Oops.
[23:01] (keyboard clicking)
[23:04] bin-keys.js.
[23:09] Oops.
[23:10] (keyboard clicking)
[23:12] Where's the samples?
[23:14] Hmm, cannot read properly undefined of two public key.
[23:20] (keyboard clicking)
[23:21] Bin-keys 209, right.
[23:26] Okay, so let's copy our good friend dash keys here
[23:31] into the module for the sake of our experiments.
[23:36] (keyboard clicking)
[23:40] Hmm.
[23:43] (keyboard clicking)
[23:47] (upbeat music)
[23:49] Right.
[23:55] (keyboard clicking)
[23:58] 236.
[24:00] So this one.
[24:02] (keyboard clicking)
[24:05] Should have been like this.
[24:14] (keyboard clicking)
[24:17] Okay, so I'm going to go ahead and copy this over.
[24:20] (keyboard clicking)
[24:23] And then let's see, what does it show us?
[24:32] We're inspecting masked.
[24:36] (keyboard clicking)
[24:43] Got address, all the X, Y stuff we can get rid of.
[24:47] Pubkey hash is essentially the address,
[24:52] but the pubkey hash is already there.
[24:57] Public key is already there.
[25:00] Pubkey hash.
[25:03] Should I make this pubkey sha?
[25:09] (keyboard clicking)
[25:12] (upbeat music)
[25:14] Maybe.
[25:25] (keyboard clicking)
[25:28] I think I am going to do that.
[25:30] Let's go back into this one.
[25:33] And we're going to rename this to PK.
[25:37] How is it?
[25:40] PK, no.
[25:42] Shin, dash keys, PK, sha.
[25:47] How about pubkey, sha, 256?
[25:52] 'Cause that is a real intermediate value.
[25:59] Yeah, I think we'll do that.
[26:07] Let me try that one more time.
[26:08] All right, so with this one,
[26:12] we're not giving away anything about the private key
[26:17] other than the first and last byte.
[26:23] Okay.
[26:29] (upbeat music)
[26:31] (keyboard clicking)
[26:34] All right, that's good.
[26:56] And then let's do that as unsafe.
[27:00] (keyboard clicking)
[27:03] I kind of want to call it unmask.
[27:20] I think that's the right thing to do.
[27:22] (keyboard clicking)
[27:25] (upbeat music)
[27:27] All right, now let's see what this actually looks like.
[27:47] Oh, and we need the,
[27:48] let's put a little license information bit in here too.
[27:53] All right, copy over license information.
[27:56] (keyboard clicking)
[28:00] MIT license.
[28:11] (keyboard clicking)
[28:14] (upbeat music)
[28:17] Private key, public key hash.
[28:39] (keyboard clicking)
[28:42] Public key hash.
[28:44] (keyboard clicking)
[28:47] Let's just put it like that.
[28:48] (keyboard clicking)
[28:51] Debug info.
[28:59] (keyboard clicking)
[29:02] Oops, debug info.
[29:07] Maybe I ought to do a couple of things here.
[29:10] One, let's see, where is the unsafe used?
[29:15] Unsafe, mask.
[29:17] Unsafe.
[29:18] Unmask.
[29:25] (upbeat music)
[29:28] Okay.
[29:34] (keyboard clicking)
[29:37] Eh, we'll call it, we'll keep it with unsafe for now.
[29:47] (keyboard clicking)
[29:50] No, I really think it should be unmask.
[29:53] Okay, this, compromise.
[29:57] (keyboard clicking)
[30:01] (upbeat music)
[30:03] Okay, unmask.
[30:13] (keyboard clicking)
[30:16] (upbeat music)
[30:18] Don't mask private keys.
[30:41] (keyboard clicking)
[30:44] (upbeat music)
[30:46] (keyboard clicking)
[30:49] (upbeat music)
[31:18] Unmask private key.
[31:19] Are we using this anywhere else?
[31:22] Let's do two places.
[31:23] All right, how about this?
[31:26] (keyboard clicking)
[31:29] All right, what was this one all about?
[31:38] (keyboard clicking)
[31:41] (upbeat music)
[31:44] All right.
[31:51] (keyboard clicking)
[31:54] (upbeat music)
[31:57] Make new definition for CLI?
[32:18] What?
[32:19] (upbeat music)
[32:22] (keyboard clicking)
[32:25] Okay, so let's try this.
[32:40] I'm gonna try this three different ways.
[32:43] So the first way,
[32:48] hash keys.js, inspect.
[32:50] Oh, that one's gonna fail
[32:51] because I didn't actually have
[32:53] anywhere to point it at.
[32:57] Okay, so we're gonna show it that way.
[32:59] We're gonna show it this way.
[33:03] We're gonna show it this way.
[33:08] Okay, show it this way.
[33:17] (keyboard clicking)
[33:19] We're gonna show it this way.
[33:24] (keyboard clicking)
[33:44] will.go.m.sh history.
[33:47] (keyboard clicking)
[33:50] Okay.
[34:13] So let me try this one more time.
[34:15] What is unsafe actually doing?
[34:18] All right, generate address.
[34:20] If not, oh, if is string and not unsafe.
[34:27] All right, got that one.
[34:29] What about this one?
[34:30] What is this one doing?
[34:31] This is my nice decode.
[34:34] Okay, so if we decode, decoded private key,
[34:37] and it's a string.
[34:38] Ah, ah, new exposed key error.
[34:41] Got it, right.
[34:42] Yep, that's right.
[34:43] If not unsafe.
[34:46] So these are the two, it's just two places.
[34:47] It's just generate.
[34:48] No, verify, verify as well.
[34:50] Okay.
[34:51] New exposed key error.
[34:54] Okay, got it.
[35:04] So we're protected from providing
[35:06] the private key as a string.
[35:08] And we're given an error to let us know
[35:12] that it's been exposed to the command line.
[35:14] Got it.
[35:15] Okay, so we got that out.
[35:20] Let's go ahead and see what this looks like.
[35:22] Let's take a look at the README.
[35:30] That's what we're, that's what we're doing right now.
[35:33] Ah, the iPhone, ah.
[35:37] Sorry, it just, it just bugs me.
[35:41] It just bugs me so much.
[35:42] iPhone continuity.
[35:51] Don't make the source visible yet.
[35:57] Okay.
[36:08] (upbeat music)
[36:11] Sorry, just one second here.
[36:17] I need to be able to have different settings
[36:35] for the phone camera versus the regular camera,
[36:40] 'cause it's gonna drive me mad.
[36:42] Drive me absolutely mad to just look so girlish.
[36:47] I just, I can't handle it.
[36:48] I'm not man enough to handle it.
[36:51] Hey, is that, oh no, that's not working again.
[36:53] Was it, that's working again.
[36:54] No, that one's, that's because this one.
[37:05] This one went missing.
[37:06] Okay, delete and eight.
[37:10] And then, yeah, it's just gonna bug me.
[37:16] Color correction.
[37:17] Okay, can we make me look any less?
[37:21] There we go, how about that?
[37:23] Give me a little hue shift here.
[37:25] Just a tiny, tiny bit.
[37:28] Like a negative one, sorry.
[37:34] Sorry for the interruption, I just, I can't even.
[37:37] All right, apply LUT.
[37:42] Where's my LUT, LUT?
[37:44] That's a good one.
[37:53] Look at that.
[37:56] Okay, back it down just a little bit.
[38:05] Desaturate just a little bit more.
[38:07] I just, I can't, I'm sorry.
[38:11] I just hate seeing my face looking like a Barbie doll.
[38:14] What is wrong with you, Apple?
[38:16] What is wrong with you?
[38:18] I don't know, does it not bother anybody else?
[38:21] I mean, ever since they started introducing the AI
[38:24] on the camera, it just, I hate the way I look
[38:29] in the iPhone camera.
[38:34] (sighs)
[38:35] I'm gonna turn gamma down.
[38:39] Ooh, that looks kind of nice, actually.
[38:41] Saturation down a little.
[38:45] Okay, I think that's bearable.
[38:53] No, it's not, it's so ugly.
[38:55] I'm just gonna leave it alone, though.
[38:57] You're not here to see my face, maybe.
[39:01] (groans)
[39:03] Oh, oh wait, hold on, there is one thing that I,
[39:09] all right, I promise, this is gonna be the last thing.
[39:12] Let's see, chroma key, color key, crop pad,
[39:21] mask blend, sharpen.
[39:24] There we go, we can get rid of,
[39:30] all right, that's a little too much.
[39:32] I just wanna look like a human and not a baby doll,
[39:39] that's all I'm asking.
[39:40] Yeah, re-sharpening what Apple's taken away.
[39:46] It just looks, then it looks so, there's so many artifacts,
[39:52] it's so artificial at that point.
[39:53] Blech.
[39:55] (gentle music)
[39:58] Ooh, that looks a little better.
[40:10] And negative 0.5 here, negative.
[40:20] There we go.
[40:22] (gentle music)
[40:24] That's the best I can do, that looks a lot better.
[40:29] I look a lot less like a Barbie now, I think.
[40:32] I don't know, you tell me.
[40:33] Sorry for the detour there,
[40:35] but you know, I had to use the Apple camera,
[40:38] meh, meh, meh, meh, meh.
[40:39] Okay, so we got the license info in here.
[40:48] Oh, I just pushed, right?
[40:50] So let's go check out the README and see
[40:52] how great or terrible it is.
[40:56] Oh, whoops.
[41:00] Dash HD.
[41:02] (gentle music)
[41:05] (keyboard clicking)
[41:08] Oh, this should be CLI.
[41:23] (keyboard clicking)
[41:26] (keyboard clicking)
[41:29] All right.
[41:45] (keyboard clicking)
[41:54] And actually, I do want
[41:56] X-POM.
[41:59] X-PRIV.
[42:02] (keyboard clicking)
[42:07] Yeah, that looks good.
[42:16] (gentle music)
[42:23] Let's do a little bit of install here.
[42:26] One, install Node.js.
[42:30] And then we can have a little
[42:40] curl.exe.
[42:43] (keyboard clicking)
[42:50] (gentle music)
[42:52] Windows 10 plus.
[43:06] Mac, Linux.
[43:11] Oops, and I think we don't do that.
[43:18] This one, 'cause it doesn't matter.
[43:21] And then webby.sh and sh.
[43:24] There we go.
[43:26] Two.
[43:27] Install-keys-cli via npm.
[43:34] Oops.
[43:42] (keyboard clicking)
[43:45] (gentle music)
[43:48] All right, that works.
[43:53] We got the help.
[43:54] Oh, whoops.
[43:58] That's good, that's good.
[44:00] All right, so that looks better.
[44:02] (keyboard clicking)
[44:06] (gentle music)
[44:08] See the help for most up-to-date.
[44:32] Most up-to-date.
[44:35] Ask these help for the most up-to-date info.
[44:45] I do need to do address, the address information.
[44:53] (gentle music)
[44:58] (keyboard clicking)
[45:01] Also, there is some information
[45:04] that I wanna put here with version.
[45:07] So this dash-keys-version/package.json.version-info.
[45:13] (gentle music)
[45:15] And then dash-keys.
[45:31] Whoa, that's not right.
[45:32] That should be dash-keys.
[45:33] (keyboard clicking)
[45:37] (gentle music)
[45:40] All right, then dash-keys-version.
[45:58] (gentle music)
[46:01] Oh.
[46:02] (gentle music)
[46:04] (keyboard clicking)
[46:07] 'Cause that's important information.
[46:11] Coding in Vim like a mad man.
[46:14] Or just a happy man.
[46:18] You know?
[46:20] (gentle music)
[46:23] No, I'm using iPhone continuity mode like a mad man.
[46:29] That's what I'm doing like a mad man.
[46:31] (gentle music)
[46:34] (keyboard clicking)
[46:37] There we go.
[46:41] I really, have you been here long?
[46:49] No, you probably haven't 'cause you just said it.
[46:51] I was lamenting that something went wrong
[46:54] and I had just started the stream
[46:56] and my camera cut out in between the time
[46:59] that the timer was going and the stream started.
[47:01] And it's my camera software
[47:04] because heaven knows you can't even pay
[47:06] for good software these days.
[47:07] I mean, you can't just pay for something
[47:08] that will last for weeks on end.
[47:10] You know, you gotta reboot your computer every day.
[47:14] (computer chiming)
[47:17] Thank you.
[47:18] Thanks for the follow.
[47:20] Also, I have another channel, it's CoolAJ86.
[47:22] This is Dash Incubator where I do my Dash Incubator work
[47:25] and some other people may join in here too,
[47:28] such as JojoBite.
[47:30] Anyway, what was I gonna say?
[47:31] Oh, yeah, so I had a problem with my camera
[47:36] and then I had to switch to my iPhone in continuity mode,
[47:41] which thankfully was super easy.
[47:45] But then it, you know, it Barbie dolls my face
[47:49] and I just don't like looking like a girl.
[47:52] I just don't like it.
[47:53] I don't like it.
[47:54] I'm trying to think, there was a movie character
[47:59] that I was trying to do an impression of.
[48:01] It was Jeannie.
[48:02] It was Jeannie from Aladdin.
[48:06] I don't like doing it, it's not pretty.
[48:08] Talking about bringing people back from the dead.
[48:12] All right, inspect, so I just need to do adder.
[48:23] Oh, whoops.
[48:24] That needs to be, I've got some,
[48:27] I gotta check my tags here.
[48:29] Let's, so what are you up to Izabsurd?
[48:31] What do you do?
[48:33] What brings you to the channel tonight?
[48:35] Oops, now I need to look at this.
[48:37] Okay, so PowerShell, and this should actually
[48:41] just be sh at this point.
[48:43] Shell, shell, text, should be spelled out text.
[48:50] This should be shell, this should be text,
[48:57] this should be shell.
[49:02] This should be text, this should be shell.
[49:10] That should be JSON, this should be shell.
[49:14] This should be JSON, this should be shell.
[49:25] And this should be JSON, and this should be shell,
[49:30] and this should be text, and this should be text.
[49:37] Whoops, and that should be shell.
[49:42] Oh, whoops, this would be unmask.
[49:46] That should be text.
[49:53] It's important to use text, not TXT,
[49:55] because TXT isn't recognized,
[49:58] and then it just renders in whatever.
[50:00] But text is recognized, and then it doesn't render it.
[50:04] So TXT, it will actually try to guess how to colorize it.
[50:09] That has been my problem in the past.
[50:11] Seeing what scripting coding stuff people are up to.
[50:13] I am, so I'm working for Dash Incubator.
[50:16] Dash is a cryptocurrency, it's all caps.
[50:19] Dash, dash stands for digital cash,
[50:22] so it's a portmanteau of digital cash.
[50:24] And...
[50:28] It is perhaps the only quote-unquote cryptocurrency
[50:38] that is actually aimed at being a currency,
[50:42] and that the development of it
[50:43] is not directed by venture capitalists,
[50:46] like how the Bitcoin scene has gone.
[50:50] (upbeat music)
[50:52] It's kind of an anti-fork of Bitcoin,
[50:57] because Bitcoin forked in a material sense
[51:02] when the venture capitalists took over,
[51:05] and they stopped making improvements
[51:09] for it to function as a digital cash,
[51:11] and stopped following the roadmap,
[51:14] and stopped following the white paper.
[51:15] Now, I am not really into cryptocurrencies.
[51:18] I just work here, right?
[51:20] But I do, I would not be doing work for Dash
[51:26] if I did not, if I believed that they were evil and scammy.
[51:30] And I believe that a lot of the other things out there
[51:32] are evil and scammy, and Dash's technology
[51:36] is not necessarily 100% the best across the board,
[51:40] but I think the philosophy and the ethos
[51:43] that are driving the technology
[51:45] are the best across the board, if that makes sense.
[51:48] So, that's the dealio.
[51:54] Okay, so the last thing I need to do for this README
[51:58] is just add the address.
[52:01] So, we're gonna say address.
[52:04] I think that's the first thing that we need to do.
[52:12] (upbeat music)
[52:15] Convert WIF to payment address.
[52:22] And I'll do this in two ways.
[52:24] From a file.
[52:30] (upbeat music)
[52:33] From a string, dangerous.
[52:50] (upbeat music)
[52:59] Okay, oops, and this should be address.
[53:04] And then this should be address dash dash unsafe.
[53:10] And then this output is going to be,
[53:25] (upbeat music)
[53:28] dash dash JSON, or,
[53:39] let's see, where'd the help go?
[53:52] (upbeat music)
[53:55] So then, what it's gonna do,
[54:22] is it's just gonna output these file contents.
[54:27] And let's see here.
[54:32] This one, unsafe, and it's gonna be JSON,
[54:36] but it's not gonna be unmasked.
[54:38] So, let's see what happens when we do that.
[54:42] Then dash keys, address, samples, like this.
[54:47] (upbeat music)
[54:49] Actually, I need to change that.
[54:58] (upbeat music)
[55:01] (keyboard clacking)
[55:04] Oops.
[55:19] (upbeat music)
[55:22] (keyboard clacking)
[55:25] Okay, convert to pay adder.
[55:43] Convert with to payment address.
[55:46] (upbeat music)
[55:48] (keyboard clacking)
[55:51] The name of the file,
[55:54] is 58 check encoded public key hash.
[56:01] (keyboard clacking)
[56:04] The contents are the private key.
[56:15] Okay, great, fine and dandy.
[56:17] (upbeat music)
[56:20] Address.
[56:21] (upbeat music)
[56:24] All right.
[56:32] Now, let's say that I do this as JSON.
[56:37] I would like that to actually output
[56:41] the public key hash as well.
[56:43] (upbeat music)
[56:47] Let me see about that address.
[56:49] (upbeat music)
[56:52] Okay, with to adder.
[57:02] (upbeat music)
[57:15] Okay, generate adder or convert adder.
[57:18] Probably should be convert adder.
[57:19] (upbeat music)
[57:22] There we go, that's good enough.
[57:35] I'll take that.
[57:37] Especially on a Wednesday for half price.
[57:39] The pay adder is,
[57:43] (upbeat music)
[58:12] Let's see.
[58:13] What if I just want to decode.
[58:15] Decode, do I have a decode here?
[58:20] (keyboard clacking)
[58:30] bullshit.
[58:31] (keyboard clacking)
[58:34] Hmm.
[58:49] (keyboard clacking)
[58:52] I kinda want.
[58:58] (keyboard clacking)
[59:00] (upbeat music)
[59:03] Let's rename this.
[59:23] I want this to be not BS 58.
[59:26] (upbeat music)
[59:30] Oh wait, hold on.
[59:31] Base 58 check.
[59:33] Let me go check this out.
[59:35] (keyboard clacking)
[59:38] Okay, B58C.
[59:44] I don't know, can I?
[59:48] (keyboard clacking)
[59:51] Decode.
[59:54] Maybe I could have a decode with a decode adder.
[59:59] I definitely want access to this thing.
[60:02] The design here.
[60:04] I want to say,
[60:07] let's see.
[60:13] B58C, ah, that's fine.
[60:18] Window.
[60:21] (keyboard clacking)
[60:24] (upbeat music)
[60:27] Hmm.
[60:44] Actually, what I kind of want to do,
[60:51] (keyboard clacking)
[60:54] let's see if I can do this.
[60:56] I'm gonna try to expose on base 58 check
[61:01] a decode method.
[61:05] (upbeat music)
[61:19] It seems like
[61:20] this ought to have something
[61:25] that is a little bit higher level, in fact,
[61:29] so that there should be,
[61:30] say, a base 58 checksum at the top level
[61:35] that just uses,
[61:40] so here we have ops.xpubversion.
[61:46] Ops.xpubversion.
[61:47] Could we not just as well do
[61:53] a base 58 check?
[62:01] Well, yeah, I mean, could we not just as well say
[62:05] var defaults?
[62:10] I guess in this case it is in a function,
[62:12] so we could do let defs
[62:17] base 58 check defaults equals,
[62:32] so I guess we'd want it to be this way.
[62:38] So what we would want is B58C,
[62:43] no, that's what we need.
[62:47] How would we do this?
[62:52] Let me think about this for a second.
[62:54] (upbeat music)
[62:56] (keyboard clicking)
[62:59] I just want an easier way to reference this inside
[63:11] is basically what I want.
[63:13] (upbeat music)
[63:15] (keyboard clicking)
[63:18] Hmm.
[63:33] (upbeat music)
[63:44] So, for example, what's the downside
[63:49] of adding a function call on this?
[63:53] Well, then we gotta keep it that way.
[63:55] (mumbles)
[63:56] Okay, no, I'm not gonna do it.
[63:57] So what I was thinking about doing was I was thinking,
[63:59] well, maybe I'll just pull all these things
[64:01] back up to the top level,
[64:03] and then the create function will just have a small wrapper.
[64:06] No, no, it's not gonna work that way.
[64:10] I mean, it could work that way,
[64:11] it's just, it's gonna add more complexity.
[64:14] So if I want to do this,
[64:16] I mean, dash keys could have a decode function, right?
[64:21] Isn't that essentially what,
[64:22] what did I just see in the read me here?
[64:25] Adder to pubkey hash.
[64:29] Okay, pubkey hash to adder.
[64:34] With to private key.
[64:41] Yeah, I think this is basically what should be done here.
[64:45] As we should have a with to private key.
[64:50] (upbeat music)
[64:53] (mumbles)
[64:55] (upbeat music)
[65:23] Wait, what did I have going on here?
[65:25] I think I was gonna pass in the verify false option
[65:29] or something like that.
[65:52] Okay, but let's say we do take that one.
[65:57] I'll just put this in here for the moment.
[66:04] I'll put a little to do on it.
[66:20] Okay, let's see, dash 58, check.
[66:24] Where'd that come from?
[66:25] I probably defined that somewhere.
[66:27] I already got that here anyway.
[66:41] B58C.
[66:49] B58C.
[66:50] It's amazingly low latency, to be honest.
[67:16] Now that I look at it.
[67:20] It's almost like it's predicting the future.
[67:22] Okay, again, distracted by the camera.
[67:33] Decode, decode, decode, decode, decode, decode.
[67:37] So this looks good.
[67:38] (upbeat music)
[67:41] Oh no, that's what I was afraid of.
[68:04] So the problem when the camera is on like this
[68:09] is that it can't,
[68:14] let me see if I can plug it in the other way.
[68:16] The battery drains faster than it can be recharged.
[68:22] Let me try plugging it in directly to the computer.
[68:34] Let's see what that does for it.
[68:35] Is it charging now?
[68:40] Okay, now it says it's charging.
[68:43] We'll see, we'll see.
[68:47] All right, so I do want, oops.
[69:00] If not valid, if verify,
[69:05] if false is not equal to verify,
[69:10] throw new error, invalid address or WIF.
[69:16] (upbeat music)
[69:19] So I actually do want to decode this.
[69:47] (upbeat music)
[69:49] Public key.
[69:58] Let public key equals,
[70:08] and nothing.
[70:14] Public key hash.
[70:15] (upbeat music)
[70:17] Pub key hash, and then if adder.private key,
[70:22] then public key equals,
[70:29] dash.utils.to public key.
[70:37] Adder.private key.
[70:44] Pub key hash equals dash.utils.
[70:49] Let's see, what do we have presently with the dash to adder?
[71:05] Oops, WIF to adder.
[71:08] (upbeat music)
[71:10] Pub, we could call it pub to pkh,
[71:26] 'cause that method name is a little long,
[71:30] and it's kind of long in a way
[71:31] that I'm not sure that it adds a lot of.
[71:33] (upbeat music)
[71:36] Oh my goodness.
[71:39] (upbeat music)
[71:42] Let's see.
[72:04] Let's do public key to pub key hash.
[72:08] This is returning.
[72:11] Okay, I think this should be down
[72:13] at the utils level, actually.
[72:14] (upbeat music)
[72:17] I think the top level,
[72:24] I'm not sure how to split these.
[72:29] (upbeat music)
[72:32] (keyboard clacking)
[72:35] Okay, again, I might want to have
[72:40] just a teeny tiny bit of conversation
[72:43] before finalizing the names for these,
[72:46] 'cause I think I'm erring on the side of too long.
[72:49] Public key to pub key hash,
[72:51] where it could be pub to pkh.
[72:54] Pub to pkh.
[72:58] And I think the documentation
[73:01] maybe should be more explicit,
[73:03] and the code should be maybe less explicit in that way.
[73:07] Ryan, we'd love your thoughts on that one.
[73:09] Because I feel like this is a little, ugh.
[73:14] Okay.
[73:22] (upbeat music)
[73:28] Pub key hash buff.
[73:30] Key hash.
[73:33] Pub key hash buff.
[73:36] Oh, whoops.
[73:39] Maybe the things that are,
[73:45] the deal with buffers could be in one layer,
[73:51] and the things that deal with hex
[73:52] could be in another layer.
[73:54] (upbeat music)
[73:56] All right, so then we could say public key, public key.
[74:13] We could probably make this just address.
[74:19] No, that's.
[74:22] (upbeat music)
[74:24] I kind of want things to be synonymous too, though.
[74:49] And in the JSON, it definitely should be
[74:50] address public key pub key hash.
[74:53] I'm pretty solid on that.
[74:54] And if that's the way that it is,
[74:57] then the method name should be
[74:58] pub key, public key to pub key hash.
[75:02] We should be consistent across the ecosystem
[75:05] with the naming conventions internally and externally.
[75:18] But quite possibly,
[75:20] maybe bytes, maybe I could,
[75:28] I could go universally from UN8 array,
[75:31] say bytes to hex, hex to bytes.
[75:35] That makes sense.
[75:39] That's kind of a free word.
[75:41] Everybody uses buffer,
[75:43] but bytes is not something that I think is as commonly used.
[75:48] Okay, public key.
[75:49] Here we go.
[75:50] All right, so this should print out the right information now.
[75:54] Oops.
[75:55] Okay, where did this come from?
[76:13] (upbeat music)
[76:16] Function decode.
[76:27] Okay, let me double check on this.
[76:37] (upbeat music)
[76:39] Decode equals function string.
[76:48] Okay.
[77:02] (upbeat music)
[77:05] Let's see about this one.
[77:16] Dash keys dot 58 check.
[77:20] Let's try that.
[77:27] (upbeat music)
[77:29] I think I actually have something wrong.
[77:41] (upbeat music)
[77:44] (keyboard clacking)
[77:47] So let's try this again.
[78:00] DX18 decode.
[78:10] So what did I do wrong here?
[78:13] Decode, decode adder or with.
[78:18] 204.
[78:30] Is this around line 204 or is this somewhere else?
[78:33] 'Cause I think this might be somewhere else.
[78:34] It says 204.
[78:35] Console dot log adder or with.
[78:43] Let's go ahead and try that out.
[78:44] Okay, that looks right.
[78:47] So something didn't quite go right there,
[78:54] but I'm not really sure where.
[78:59] Oh, did I declare this function twice perhaps?
[79:12] I did, I did.
[79:16] Should probably call that something like raw decode.
[79:20] (upbeat music)
[79:23] (keyboard clacking)
[79:26] All right, buffed out for each is not a function.
[79:44] For what?
[79:47] (upbeat music)
[79:50] (keyboard clacking)
[79:53] (upbeat music)
[79:55] (keyboard clacking)
[79:58] (upbeat music)
[80:01] Hmm.
[80:08] (upbeat music)
[80:28] But what was my other function decode here?
[80:30] How did I do it in this one?
[80:33] Painstakingly, of course.
[80:36] (upbeat music)
[80:39] Uh-oh.
[80:48] Hmm.
[80:51] We might have a problem here.
[80:56] This may be a lot of wrong information
[80:58] because this decoded private key here.
[81:05] (keyboard clacking)
[81:09] I don't think that's a buffer.
[81:16] And I think that the to public key
[81:21] (keyboard clacking)
[81:24] just happens to work on strings.
[81:29] Oh, it does just happen to work on strings.
[81:36] Should still work.
[81:50] Yeah, it's the right size and everything.
[81:52] Okay, raw decode.
[81:56] (upbeat music)
[81:59] (keyboard clacking)
[82:02] Hex to UNA array.
[82:24] (upbeat music)
[82:27] Okay, private key buff.
[82:29] I guess this could be the rule.
[82:31] We could accept either hex or UNA array.
[82:36] We can be looser in what we accept,
[82:39] but we can only output one type.
[82:41] That's the thing.
[82:42] It has to be, and I prefer just to accept one type,
[82:47] but we could accept an enum type.
[82:50] (upbeat music)
[82:53] (keyboard clacking)
[82:56] But I definitely don't wanna be returning multiple types.
[83:04] I don't wanna have an encode type thing
[83:08] where depending on what you put in,
[83:10] you get out something different.
[83:11] Okay, so still buffed up for each is not a function.
[83:17] Let me explore this a little bit closer here.
[83:21] Oh, wait, which was this on line one, one, four?
[83:24] Okay, so this is gonna be a buff,
[83:28] console.log, debug, buff.
[83:32] And let's see what this buff is.
[83:34] Ah, it's a promise.
[83:39] Okay, so that's the more important part here.
[83:41] Await, await, await.
[83:50] (keyboard clacking)
[83:53] That doesn't need an await.
[83:56] There we go.
[83:59] So let's take a look again at public key.
[84:03] All right, public key buff, public key buff.
[84:14] It's tedious, but it's kind of the right thing to do.
[84:18] (keyboard clacking)
[84:21] Okay.
[84:32] Get rid of this debug info.
[84:37] Get rid of that.
[84:44] (keyboard clacking)
[84:47] And then I forgot to do, let's see.
[84:54] (keyboard clacking)
[85:13] All right, public key buff.
[85:15] And then I guess let address equals await,
[85:20] v58c.encode, pubkeyhash, pubkeyhash.
[85:27] There we go.
[85:32] Probably even one line that.
[85:35] (keyboard clacking)
[85:38] (keyboard clacking)
[85:41] (keyboard clacking)
[85:45] (keyboard clacking)
[85:48] (keyboard clacking)
[85:51] (keyboard clacking)
[85:55] (keyboard clacking)
[86:23] Okay, so let's print this out one more time.
[86:25] I think we're done now with this one.
[86:27] Yeah, okay.
[86:28] And I actually would like to add the SHA
[86:37] in the middle of this.
[86:38] No, that's for inspect.
[86:44] That's not for this.
[86:45] It's fair enough to print these out.
[86:49] (keyboard clacking)
[86:52] Pubkeyhash, address.
[87:00] There we go.
[87:08] (keyboard clacking)
[87:12] (keyboard clacking)
[87:15] Okay.
[87:27] (keyboard clacking)
[87:33] (keyboard clacking)
[87:36] (keyboard clacking)
[87:39] (keyboard clacking)
[87:42] Okay, so there we go.
[88:08] (keyboard clacking)
[88:11] Oh, right, address.
[88:37] Actually, I'm fine with just leaving that one as is.
[88:40] You can go either way on it.
[88:46] Here's what I'll do.
[88:56] I'll make these debug values
[89:01] so that they're not part of the public API,
[89:03] just so that I've got them for now.
[89:05] (keyboard clacking)
[89:08] Fair enough.
[89:12] Okay, cool.
[89:17] And then, of course, let us,
[89:21] let's cat examples, XR.
[89:29] (keyboard clacking)
[89:32] So this should give me a warning.
[89:38] Unsafe.
[89:45] And then,
[89:52] cool, all right.
[89:58] Let's go ahead, take this, put it in the readme.
[90:01] I think that's the last thing to go into the readme.
[90:03] Then I just need to sync up the versions,
[90:05] fix up the other readme.
[90:06] This one's done.
[90:07] Famous last words.
[90:13] Just.
[90:17] Okay.
[90:25] (keyboard clacking)
[90:28] All right.
[90:44] (keyboard clacking)
[90:47] Oh, one other thing,
[91:08] which I may not do right now.
[91:13] (keyboard clacking)
[91:16] Typically, let's print it out all caps.
[91:22] (keyboard clacking)
[91:41] All right, now let me rebase this.
[91:43] Whoops.
[91:44] Oh, whoops.
[91:47] Initial commit.
[91:53] Whip, whip, whip, whip, whip, whip, whip.
[91:56] Great.
[91:57] Reset head to one.
[92:11] (keyboard clacking)
[92:14] What?
[92:18] Okay.
[92:22] So.
[92:25] Is this top gear?
[92:32] No, this is metric.
[92:33] Let's see, is this charging?
[92:40] Or no.
[92:41] Hey, look at that.
[92:44] It's plugged directly into the USB-C in the computer,
[92:48] then it's suddenly got enough power.
[92:50] That tells me I need more USB-C.
[92:55] I don't know how I can swing that.
[93:09] Well, it's not even USB-C, it's Thunderbolt,
[93:12] and that is different as well.
[93:13] I don't think it gets enough power
[93:16] when I plug it in via USB-C.
[93:19] I would need another Thunderbolt hub somehow.
[93:22] And heaven knows those are atrocious.
[93:25] I'm just gonna check on that real quick.
[93:28] Thunderbolt hub.
[93:31] They're so incredibly expensive.
[93:35] Oh, wow.
[93:36] (upbeat music)
[93:39] Oh, well that's, I mean, they're redonkulously expensive,
[93:44] but.
[93:44] Thunderbolt 4 hub for $170 rather than $400.
[93:55] That's come down in price quite a bit, actually.
[94:01] Or maybe they weren't $400.
[94:06] Okay, here's one, CalDigit.
[94:08] CalDigit Thunderbolt 4 hub.
[94:15] That might be the thing that I would need.
[94:18] I'll have to check on that later.
[94:20] Oh, Plugable's got a Thunderbolt 4 hub.
[94:25] Okay, anyway, back over here.
[94:35] All right, what was my to-do?
[94:37] Print public key hash two.
[94:39] We got that.
[94:40] Now this is not, the CLI code I'm not particularly proud of.
[94:46] It's a little bit meh.
[94:47] Could go back on that later,
[94:52] but I'm really more interested in the library code,
[94:55] the documentation I'm interested in,
[94:56] the library code I'm interested in.
[94:59] So I think I might just...
[95:04] move on from this.
[95:07] Let's see, git pull.
[95:11] (keyboard keys clacking)
[95:15] Oh, whoops.
[95:39] (keyboard keys clacking)
[95:42] So I guess I should...
[95:44] (keyboard keys clacking)
[96:13] All right, git commit dash m.
[96:15] (keyboard keys clacking)
[96:19] Move CLI to...
[96:28] There we go.
[96:32] (keyboard keys clacking)
[96:33] On repo update docs.
[96:37] (keyboard keys clacking)
[96:39] There we go, that's that.
[96:41] (keyboard keys clacking)
[96:44] All right, so let's get rid of that to-do.
[96:57] (keyboard keys clacking)
[97:01] (keyboard keys clacking)
[97:05] Git stash.
[97:12] (keyboard keys clacking)
[97:16] (keyboard keys clacking)
[97:19] All right.
[97:38] (keyboard keys clacking)
[97:42] (keyboard keys clacking)
[97:45] All righty.
[97:54] (keyboard keys clacking)
[97:58] (keyboard keys clacking)
[98:01] Okay.
[98:15] (keyboard keys clacking)
[98:28] So let's just see what happens if we just reset add to...
[98:33] (keyboard keys clacking)
[98:38] Git sherry dash remain.
[98:41] (keyboard keys clacking)
[98:45] Git rm.
[98:50] (keyboard keys clacking)
[98:53] Git commit dash m.
[98:56] (keyboard keys clacking)
[98:58] Um...
[98:59] (keyboard keys clacking)
[99:02] Get a rebase dash I main.
[99:04] Whoops.
[99:05] Git stash.
[99:05] (keyboard keys clacking)
[99:09] All right.
[99:25] (keyboard keys clacking)
[99:26] Git stash pop.
[99:28] (keyboard keys clacking)
[99:31] And git stash list.
[99:35] (keyboard keys clacking)
[99:36] Stash prop again.
[99:38] Okay, cool.
[99:39] So...
[99:41] (keyboard keys clacking)
[99:44] All right.
[99:53] So what we're saying is with the read me,
[99:55] (keyboard keys clacking)
[99:58] we're removing the CLI section I think.
[100:01.12] Let's see.
[100:02.64] CLI.
[100:03.48] (keyboard keys clacking)
[100:06.90] (upbeat music)
[100:09.48] Oops.
[100:34.20] (upbeat music)
[100:37.26] (keyboard keys clacking)
[100:40.68] There we go.
[100:45.14] (keyboard keys clacking)
[100:48.56] All right.
[100:55.34] So we're gonna install the dash key CLI
[100:57.18] and that's all there is to say about that.
[101:00.10] (keyboard keys clacking)
[101:03.60] (upbeat music)
[101:06.18] C and then we'll put...
[101:16.40] All right.
[101:17.24] Go grab.
[101:18.08] What's the read me from a CLI here?
[101:21.74] (keyboard keys clacking)
[101:25.92] C more at...
[101:28.00] (keyboard keys clacking)
[101:31.42] (upbeat music)
[101:34.00] There we go.
[101:41.38] (keyboard keys clacking)
[101:44.80] And I think that we should just get the install
[101:54.06] simplified this way.
[102:00.58] Let's do like that.
[102:01.80] (keyboard keys clacking)
[102:05.22] Okay.
[102:11.96] (keyboard keys clacking)
[102:13.84] There we go.
[102:14.68] (keyboard keys clacking)
[102:18.10] C dash key CLI read me.
[102:25.20] (keyboard keys clacking)
[102:27.14] There we go.
[102:27.98] That's it.
[102:28.80] (keyboard keys clacking)
[102:32.30] That's good.
[102:50.66] Okay.
[102:52.20] So we're gonna move this one
[102:56.86] up to where it gets its own module.
[102:59.74] (keyboard keys clacking)
[103:03.16] We haven't really done anything to update this yet.
[103:18.60] Right?
[103:20.70] So let's take a look at dash keys.
[103:25.06] (keyboard keys clacking)
[103:28.56] Okay.
[103:35.98] Before I force push this,
[103:38.58] let me just double check.
[103:39.90] There's nothing that I wanted in here.
[103:43.14] Cause I just got a little bit of a sinking feeling,
[103:47.30] you know?
[103:48.74] Like maybe there was something.
[103:50.46] Okay.
[103:52.66] What was this whip?
[103:54.54] That's just deleting those couple of things
[103:59.54] and updating the sub module.
[104:02.92] Okay.
[104:09.26] And this is...
[104:14.34] Oh, I like that new diff on sub modules, by the way.
[104:16.86] That was awesome.
[104:22.66] To public key uncompressed.
[104:25.30] Oh, this has already moved over.
[104:31.90] I will double check that this has in fact been moved over,
[104:41.38] but I'm pretty sure all of it has.
[104:45.68] Yeah, all that debug stuff's over.
[104:51.18] This one, I don't know if this was moved over.
[104:53.48] Let me check by eBad input.
[104:56.28] I'm pretty sure that was moved over.
[104:59.54] So mask land private key.
[105:01.02] Those are two things I need to check for
[105:02.66] in the CLI repo here.
[105:04.36] eBad input.
[105:12.74] Okay, so this was not moved over.
[105:14.34] That's little bitty, I think does need to go in.
[105:19.08] (upbeat music)
[105:21.66] And let's see, what from there do we need?
[105:28.64] Private key dot length.
[105:35.46] So that made it in, but not whatever this was about.
[105:39.48] B58RE.
[105:45.64] (upbeat music)
[105:48.22] Where is B58RE?
[105:57.38] Oh, that is there.
[106:03.60] Why did I not think that was there?
[106:05.36] Oh, the first one I came across didn't have it.
[106:11.56] This one didn't have it.
[106:13.36] That's around line 200.
[106:15.48] This is around line 330,
[106:18.66] which seems like it's grown since then.
[106:23.64] Let's see what, let me give it a little more context
[106:26.92] around this one.
[106:28.20] What function is this in?
[106:29.80] This is in read, adder, or path.
[106:32.18] Read, adder, or path.
[106:35.48] So the function, that's where is valid as, okay, cool.
[106:40.80] So all that made it in, good.
[106:42.72] So we can go ahead and force push over that.
[106:45.60] And then let's update our package
[106:51.88] and read me and get this Mojanker published.
[106:55.02] (upbeat music)
[106:57.60] Okay.
[107:11.64] Dependencies, it no longer needs these two dependencies.
[107:16.64] I would want to get this updated to whatever the latest is.
[107:24.68] All right, so that's been updated by one.
[107:35.64] That's fine.
[107:36.48] (upbeat music)
[107:39.06] Okay, we'd get rid of the bin.
[107:45.52] Oops.
[107:53.92] All right, we get rid of the bin file.
[108:04.38] (upbeat music)
[108:06.96] Oh.
[108:17.62] (upbeat music)
[108:20.20] Okay.
[108:34.28] (upbeat music)
[108:36.86] Wait, why does this have a merge conflict?
[108:52.10] (upbeat music)
[108:54.68] Okay, bump goes number one.
[109:03.82] (upbeat music)
[109:04.88] Test goes at the end.
[109:06.34] Thumped gumps before lent.
[109:10.80] Same test, same test.
[109:16.30] Versions out.
[109:18.74] Thumped is the same.
[109:21.98] Lent is the same.
[109:25.28] Oh, I don't know why that was.
[109:31.34] Okay, get rebase continue.
[109:34.20] All right, why is it complaining again?
[109:39.94] Again, bump, thumped, lent.
[109:54.62] (upbeat music)
[109:59.64] Test.
[110:00.48] These are the same.
[110:07.16] These are the same.
[110:11.20] I don't know why it got confused about that.
[110:14.14] Always package JSON.
[110:15.62] (upbeat music)
[110:19.24] (keyboard clicking)
[110:22.24] Oh, whoops.
[110:38.20] (upbeat music)
[110:40.78] (keyboard clicking)
[110:43.78] I think something that I didn't want
[111:02.14] to have happen here happened here.
[111:04.26] Did I already push this?
[111:05.46] Uh-oh.
[111:10.46] (keyboard clicking)
[111:11.50] Let me redo that one a little bit if I can.
[111:14.26] Oopsies, hold on.
[111:25.62] I think I...
[111:39.78] Move that over.
[111:40.94] All right, so cleaning up the dependencies,
[111:53.90] that, for some reason that went into this one,
[111:57.98] which is fine, I guess.
[111:59.66] (keyboard clicking)
[112:08.94] Don't ignore this.
[112:11.02] (keyboard clicking)
[112:14.02] (sighs)
[112:16.02] Okay.
[112:41.54] (keyboard clicking)
[112:44.54] Clean up package.json.
[112:50.14] Let's just call it that.
[112:51.62] ARM-RNF package lock.
[112:59.42] NPM install.
[113:01.82] Hit add package lock.
[113:05.54] Hit rebase, continue.
[113:07.58] There we go.
[113:11.02] Okay, so that's all cleaned up now.
[113:13.02] (sighs)
[113:16.06] What do we need to do?
[113:17.94] We need to get some...
[113:20.42] We need to decide on what is a utility function
[113:26.26] and what isn't, and I'm actually getting
[113:28.02] a little bit tired, so I'd hate to...
[113:32.02] I want to power through this.
[113:33.60] Caffeine-free Mountain Dew, the rescue.
[113:36.66] (upbeat music)
[113:39.24] Wait, where's my update license?
[113:47.28] Oh, this is main.
[113:48.74] This is not to v1 and beyond.
[113:50.38] Here we go.
[113:51.22] All right.
[113:54.94] Oh, RipeMD.
[113:58.06] Oops. (chuckles)
[114:00.62] Forgot to add the RipeMD copyright info.
[114:02.92] Let's see where that comes from.
[114:05.94] (upbeat music)
[114:08.52] (caffeine-free music)
[114:11.68] (caffeine-free music)
[114:14.84] (caffeine-free music)
[114:18.00] (caffeine-free music)
[114:21.16] (caffeine-free music)
[114:24.34] (caffeine-free music)
[114:29.38] (caffeine-free music)
[114:36.04] (caffeine-free music)
[114:41.66] (caffeine-free music)
[114:48.26] (caffeine-free music)
[114:51.44] Do-do-do-do-do.
[114:57.78] (caffeine-free music)
[115:00.94] (caffeine-free music)
[115:07.26] (caffeine-free music)
[115:14.02] (caffeine-free music)
[115:17.20] Okay.
[115:26.38] (caffeine-free music)
[115:29.54] Okay.
[115:36.68] (caffeine-free music)
[115:39.94] (caffeine-free music)
[115:43.02] Just boring stuff right now.
[115:45.78] All right, get rebase-iMain.
[115:56.84] Let's see, what can we get back to here?
[115:58.84] Okay, we've got,
[116:01.52] I think all we gotta do is just get this,
[116:04.48] decide where to put these utility functions.
[116:09.88] (caffeine-free music)
[116:38.66] Yeah.
[116:39.50] I like using public key versus pub key.
[116:48.14] Pub key for pub key hash.
[116:50.62] Internally, pub key, pub buff, whatever.
[116:53.82] I think I wanna expose these on the outside as hex,
[117:02.70] and on the inside as util.
[117:04.54] (caffeine-free music)
[117:07.70] Let's go ahead and update this.
[117:16.74] We don't need this anymore.
[117:18.42] We don't need that anymore.
[117:21.82] We just need this one.
[117:22.98] I think we can slim the install down quite a bit.
[117:29.32] (caffeine-free music)
[117:32.48] Install.
[117:52.02] (caffeine-free music)
[117:55.18] Usage.
[118:03.72] (caffeine-free music)
[118:06.88] (typing)
[118:08.96] Node and bundlers.
[118:27.86] (caffeine-free music)
[118:31.02] (typing)
[118:33.10] Let's see, browser.
[118:44.48] (caffeine-free music)
[118:47.66] (typing)
[118:49.74] (caffeine-free music)
[119:03.56] (typing)
[119:05.64] Window.dash queues.
[119:28.88] (caffeine-free music)
[119:33.04] (typing)
[119:35.12] All right, let's get rid of the generate example.
[119:42.12] I kinda wanna move that into utils.
[119:48.04] (caffeine-free music)
[119:52.40] And I kinda wanna rename it.
[119:55.56] (typing)
[119:59.98] (typing)
[120:02.22] Let's see.
[120:03.88] Generate.
[120:04.72] (typing)
[120:09.66] (caffeine-free music)
[120:27.94] I could call it generate non-HD.
[120:29.88] That would, that floats my boat.
[120:37.74] (caffeine-free music)
[120:41.90] (typing)
[120:52.94] (caffeine-free music)
[120:56.10] Oh, we don't wanna do,
[121:06.34] yeah, we don't wanna do it like this.
[121:09.84] We would want to do uint8 array.
[121:14.82] (caffeine-free music)
[121:20.04] To dash keys dot utils dot.
[121:23.70] I need to decide what the naming convention
[121:26.84] for this thing is.
[121:27.80] Hex to bytes, I think is what I'm gonna call it.
[121:30.94] (caffeine-free music)
[121:35.96] Prove buff.
[121:48.48] (caffeine-free music)
[121:51.64] Let's see.
[122:01.94] Private to whiff.
[122:05.16] Whiff to adder.
[122:07.64] That makes sense.
[122:09.94] (caffeine-free music)
[122:14.20] (typing)
[122:16.28] (grunting)
[122:23.76] (caffeine-free music)
[122:26.92] Okay.
[122:36.26] (typing)
[122:40.34] (caffeine-free music)
[122:43.50] (typing)
[122:46.08] (caffeine-free music)
[122:49.24] (typing)
[122:51.32] (caffeine-free music)
[122:56.28] (typing)
[122:58.34] (caffeine-free music)
[123:01.52] (typing)
[123:03.60] (caffeine-free music)
[123:10.76] Okay, generate.
[123:25.02] (caffeine-free music)
[123:28.18] You know, I really think that I might just need
[123:41.06] to go to sleep and look at this
[123:43.58] with fresh eyes in the morning.
[123:45.42] I just feel like I'm kinda starting to slow down.
[123:47.86] Mentally, I'm just,
[123:52.14] this is, you know, it's been a good long day.
[123:55.24] And,
[123:59.30] I really wanted to finish this.
[124:03.52] I think we're pretty close.
[124:06.34] Of course, I said that, you know, a month ago,
[124:11.18] and then a few hours ago.
[124:13.26] (laughing)
[124:15.50] (caffeine-free music)
[124:18.66] Okay.
[124:23.44] All right, let's see where this is being used.
[124:36.40] Public key to pubkey hash.
[124:38.04] (caffeine-free music)
[124:42.38] (typing)
[124:44.46] (caffeine-free music)
[124:47.62] (typing)
[124:49.70] (typing)
[125:07.34] (caffeine-free music)
[125:10.50] Maybe I could just shorten it down
[125:35.94] to hex two bytes.
[125:37.32] And not have the dot utils in there, maybe?
[125:44.74] I just need it to be a little bit more ergonomic somehow.
[125:48.82] UN8 array two hex.
[125:51.60] Just two hex.
[125:54.34] Let's try that out for size.
[125:55.82] Actually, let's do a little bit better here.
[125:59.34] SD UN8 array two hex.
[126:04.86] It's just two hex, and we'll do that across star dot.
[126:09.06] Star, star, star, dot, star.
[126:13.30] Star, star, star, dot, star.
[126:18.28] And then...
[126:31.86] hex two UN8 array.
[126:34.94] It's just two bytes.
[126:52.16] Let's try that out.
[126:54.90] (typing)
[126:56.98] All right.
[127:06.38] And then...
[127:24.42] (typing)
[127:26.50] What if we did, let's see.
[127:32.16] Priv key two if.
[127:37.04] I just wanna shorten these names,
[127:39.74] 'cause it's just gonna be...
[127:41.18] It's just a little, I think it's a little too much
[127:45.18] for the function names.
[127:48.20] Maybe, maybe, okay.
[127:49.78] Maybe this is what we could do.
[127:50.82] Maybe the stuff that goes in the JSON
[127:53.06] can have the full name, because it's gonna be one item.
[127:56.46] But because the functions are so long,
[127:59.16] maybe we could do pubkey to pkh is the function.
[128:04.62] And then we could do pubkey hex to pkh hex, for example.
[128:08.28] (typing)
[128:10.36] (upbeat music)
[128:12.94] All right, that makes that a little bit better, at least.
[128:39.24] (upbeat music)
[128:41.82] Okay.
[129:04.14] (upbeat music)
[129:06.72] Well, let me get all of these functions in.
[129:13.78] (upbeat music)
[129:16.36] I do think that this is still worthwhile documentation.
[129:34.62] (upbeat music)
[130:01.40] Call this implementation details.
[130:04.88] There's enough of these, I'm just gonna pull 'em in.
[130:07.62] (upbeat music)
[130:10.20] Okay.
[130:22.76] (upbeat music)
[130:25.34] (typing)
[130:27.42] Given the existing libraries,
[130:37.28] dash keys is lighter,
[130:43.62] and less tedious is lighter,
[130:48.70] but really just a thin layer over a lot of tedium.
[130:54.58] (upbeat music)
[130:57.62] Since it's valuable to understand that tedium,
[131:02.62] here's some,
[131:06.42] (upbeat music)
[131:09.00] here's a peek behind
[131:22.28] (upbeat music)
[131:24.86] Okay, so I'm feeling good about that.
[131:40.60] (upbeat music)
[131:43.18] Where's our API at?
[131:48.44] (upbeat music)
[131:51.02] Okay.
[131:51.86] (upbeat music)
[131:54.44] With.
[132:00.60] (upbeat music)
[132:03.18] All right, await.
[132:15.14] (upbeat music)
[132:18.22] (typing)
[132:20.30] Payments address.
[132:23.38] Base 58 check encoded pub key hash.
[132:29.60] (upbeat music)
[132:32.28] Okay.
[132:36.16] (upbeat music)
[132:38.74] All right, let's do a little mini glossary here.
[132:44.78] (upbeat music)
[132:47.36] (typing)
[132:49.44] Public key hash.
[132:56.88] Also, public key hash PKH.
[133:07.08] (upbeat music)
[133:10.10] Pub key hash.
[133:16.78] (upbeat music)
[133:19.36] Let's see, maybe I'll move that one section down.
[133:42.38] (upbeat music)
[133:45.80] Yeah, that makes sense.
[133:47.96] (upbeat music)
[133:50.54] (typing)
[133:52.62] (upbeat music)
[133:55.20] (typing)
[134:22.94] Here are bunches of terms
[134:27.94] by their canonical name
[134:31.48] as well as a short description.
[134:36.48] (upbeat music)
[134:39.22] Okay, public key.
[134:48.52] (upbeat music)
[134:51.10] (typing)
[134:53.18] Crypto.get random values.
[134:59.28] (upbeat music)
[135:01.86] Is it 16?
[135:04.52] (upbeat music)
[135:07.10] The
[135:15.98] (upbeat music)
[135:20.98] Public key is hashed with SHA-256.
[135:25.98] That result is hashed with RIPE-MD-160.
[135:34.84] (upbeat music)
[135:37.98] Random number.
[135:49.18] A random 16.
[135:54.18] (upbeat music)
[135:56.92] That's 128 bits.
[136:03.94] Is that what it is?
[136:06.16] Hold on.
[136:06.98] Let me go look at this under the cover of myself.
[136:10.40] Generate.
[136:12.62] (upbeat music)
[136:15.20] Okay.
[136:16.02] Amount.
[136:16.86] (upbeat music)
[136:18.68] Dash incubator secp.
[136:20.60] (upbeat music)
[136:22.52] Okay.
[136:23.36] Generate.
[136:24.20] (upbeat music)
[136:26.78] Random.
[136:27.62] (upbeat music)
[136:28.90] Utils.
[136:29.74] (upbeat music)
[136:32.32] Random bytes.
[136:34.66] (upbeat music)
[136:37.24] (typing)
[136:39.32] Okay.
[136:54.22] (upbeat music)
[136:56.80] 32 random bytes, 256 bits.
[137:03.64] (upbeat music)
[137:06.22] (typing)
[137:09.00] Are generated.
[137:10.44] (upbeat music)
[137:13.02] Okay.
[137:19.06] (upbeat music)
[137:21.54] Get public key.
[137:23.92] (upbeat music)
[137:25.72] Private key.
[137:27.00] (upbeat music)
[137:29.58] Point.
[137:30.42] (upbeat music)
[137:36.10] Okay.
[137:36.92] Point from private key.
[137:38.28] (upbeat music)
[137:40.86] Okay.
[137:49.80] (upbeat music)
[137:52.38] Normalize private key.
[137:59.70] (upbeat music)
[138:02.96] Okay.
[138:03.80] Normalize private key.
[138:06.00] (upbeat music)
[138:08.58] Is within curve order.
[138:20.08] (upbeat music)
[138:22.66] Is not defined.
[138:26.80] (upbeat music)
[138:29.38] Curve
[138:32.78] (upbeat music)
[138:35.02] And.
[138:35.86] (upbeat music)
[138:37.82] Oh, that's a goodie.
[138:38.88] (upbeat music)
[138:41.50] (typing)
[138:43.58] (upbeat music)
[138:46.16] (typing)
[138:48.24] (upbeat music)
[138:51.82] (typing)
[138:53.90] (upbeat music)
[138:56.48] (typing)
[138:58.56] (upbeat music)
[139:01.14] All right.
[139:25.44] Curve order is.
[139:27.48] (upbeat music)
[139:30.06] Wait, if not, oh, okay.
[139:46.40] (upbeat music)
[139:48.98] (typing)
[139:51.06] Is within curve order equals.
[139:58.96] (upbeat music)
[140:01.54] (typing)
[140:03.62] (upbeat music)
[140:31.82] New error, not in curve order.
[140:36.82] (upbeat music)
[140:40.46] Oh, let's see if I understand this.
[140:49.90] So normalize.
[140:51.34] (upbeat music)
[140:54.08] (typing)
[140:56.16] (upbeat music)
[140:58.74] (typing)
[141:00.82] (upbeat music)
[141:03.40] Num and num.
[141:26.54] (upbeat music)
[141:29.12] And then what is base multiply here?
[141:34.12] Base dot multiply.
[141:37.26] (upbeat music)
[141:39.84] From private key.
[141:43.42] Normalize the private key and normalizing.
[141:46.18] Normalize private key.
[141:50.96] (upbeat music)
[141:53.54] (typing)
[141:55.62] Just to make sure I understood this right.
[142:02.28] (upbeat music)
[142:04.86] Number.
[142:07.66] Let's see.
[142:12.48] (typing)
[142:18.22] (upbeat music)
[142:20.80] Bytes to number.
[142:27.42] (upbeat music)
[142:30.00] Function bytes to number.
[142:37.78] Fine.
[142:39.84] (upbeat music)
[142:42.42] Hex to number.
[142:44.44] (upbeat music)
[142:47.86] (typing)
[142:49.94] Private key equals.
[142:57.64] (upbeat music)
[143:00.22] Gen random.
[143:03.40] (upbeat music)
[143:05.98] Num equals.
[143:11.36] (upbeat music)
[143:14.86] Hex equals two hex private key.
[143:19.46] (upbeat music)
[143:21.50] Num equals big int hex.
[143:25.24] (upbeat music)
[143:27.82] Magic sec p256k1 order value.
[143:34.74] (upbeat music)
[143:39.56] If not, is within curve.
[143:43.42] And then what does multiply mean?
[143:45.12] Oh, whoops.
[143:47.86] (upbeat music)
[143:51.06] Multiply equals.
[143:54.10] Multiply, where's base come from?
[143:58.12] Base, base, base, base, where's point come from?
[144:05.34] (upbeat music)
[144:10.42] Jacobean point.
[144:12.02] (upbeat music)
[144:14.60] Come on, where's the point at?
[144:21.24] (upbeat music)
[144:24.30] Okay, there's point base.
[144:25.94] (upbeat music)
[144:28.52] Okay.
[144:29.36] (upbeat music)
[144:31.94] No point.
[144:41.34] (upbeat music)
[144:43.92] Okay.
[144:53.80] (upbeat music)
[144:56.38] Okay.
[144:57.22] (upbeat music)
[144:59.80] Ooh, from a fiend.
[145:14.18] (upbeat music)
[145:16.76] Okay.
[145:17.60] (upbeat music)
[145:20.18] Okay, Jacobean point.
[145:32.50] (upbeat music)
[145:35.08] One in, okay, interesting.
[145:39.48] (upbeat music)
[145:42.06] So x, y, and z value.
[145:46.00] (upbeat music)
[145:47.06] And then multiply.
[145:48.54] (upbeat music)
[145:51.12] And then two of fiend, ugh, ugh.
[146:00.52] Ugh.
[146:01.36] (upbeat music)
[146:03.94] Let's see, s.
[146:15.06] All right, I'm just trying to figure out where,
[146:19.38] if I could, if this is documentable.
[146:22.38] Multiply.
[146:31.22] (upbeat music)
[146:33.80] Okay.
[146:34.64] (upbeat music)
[146:37.22] Gx.
[146:46.54] (upbeat music)
[146:49.28] Okay.
[146:50.12] (upbeat music)
[146:52.70] Okay.
[146:53.54] (upbeat music)
[146:56.12], I guess these are probably prime numbers or something.
[147:01.12] (upbeat music)
[147:03.70] I guess these are probably prime numbers or something.
[147:26.32] Just gonna guess.
[147:27.74] (upbeat music)
[147:30.32] Okay.
[147:31.16] (upbeat music)
[147:33.74] Magic.
[147:41.40] Curve values.
[147:44.92] (upbeat music)
[147:47.50] From fiend.
[147:54.02] (upbeat music)
[147:56.60] That's interesting.
[147:59.76] Why from a fiend this, rather than just new Jacobian point?
[148:04.60] (upbeat music)
[148:07.18] And then two of fiend, whatever that means.
[148:12.94] (upbeat music)
[148:15.52] stones.
[148:16.36] (upbeat music)
[148:18.94] Okay.
[148:32.74] And what was the new, was the constructor?
[148:36.04] Constructor of points.
[148:38.20] (upbeat music)
[148:40.78] Okay.
[148:44.80] (upbeat music)
[148:45.70] So it's really just,
[148:47.00] this is just kind of being silly.
[148:50.42] (upbeat music)
[148:53.00] So base, multiply, that just means.
[149:08.80] (upbeat music)
[149:12.38] Points.
[149:13.22] (upbeat music)
[149:15.80] Again.
[149:21.58] (upbeat music)
[149:24.16] All right, let me see what the multiply actually means.
[149:30.74] Multiply scaler and then multiply a fiend point.
[149:37.30] (upbeat music)
[149:41.50] Okay.
[149:42.34] (upbeat music)
[149:43.70] Okay, what does it use from a fiend point?
[149:45.84] (upbeat music)
[150:08.62] Point pre-computes dot get.
[150:10.54] (upbeat music)
[150:13.12] Okay.
[150:22.54] A fiend point.
[150:23.36] (upbeat music)
[150:25.94] Pre-computes, get.
[150:31.16] (upbeat music)
[150:33.58] Point pre-computes.
[150:35.88] (upbeat music)
[150:39.30] Ugh.
[150:40.14] (clears throat)
[150:41.30] Okay, a point is just something that has an X and Y, right?
[150:43.94] (upbeat music)
[150:46.52] What does this actually return at the end of it all?
[150:49.88] (upbeat music)
[150:52.46] Where is, where is anything actually done here?
[151:00.28] (upbeat music)
[151:02.86] (keyboard clacking)
[151:05.86] Window size.
[151:10.96] (keyboard clacking)
[151:13.96] Set window size.
[151:24.42] (keyboard clacking)
[151:26.68] Set window size eight.
[151:28.36] (keyboard clacking)
[151:32.76] Okay, that's it.
[151:34.10] (keyboard clacking)
[151:37.10] So what the heck is a WNAF?
[151:56.20] (upbeat music)
[152:01.28] Pre-compute window.
[152:02.98] (upbeat music)
[152:05.56] You gotta be kidding me.
[152:13.82] What, there, obviously, at some point,
[152:17.78] (upbeat music)
[152:20.84] that.
[152:21.68] (upbeat music)
[152:24.26] Okay, so a fiend point is passed in somewhere.
[152:29.88] (upbeat music)
[152:32.98] Point pre-computes, get a fiend point.
[152:35.32] Okay, a fiend, pre-compute, set a fiend point, pre-computes.
[152:41.76] So how does it not use the values of the point?
[152:49.64] How is that, how is it that it's never using
[152:55.18] the value of the point here?
[152:57.02] (upbeat music)
[153:00.60] It's got, I mean, obviously, if it's gonna do,
[153:03.34] if it's going to multiply something,
[153:05.02] it has to multiply something, right?
[153:08.32] (upbeat music)
[153:10.90] So it's got a pre-compute window.
[153:14.80] I mean, I can understand it might be called something else,
[153:16.88] somewhere else, but this has to be used, right?
[153:20.04] (upbeat music)
[153:22.62] Multiply, normalize scaler.
[153:28.10] (upbeat music)
[153:30.68] Seriously, so WNAF is the only place
[153:35.26] that uses the fiend point.
[153:36.70] That's it, that's it.
[153:39.60] It's the only thing that ever uses it.
[153:41.74] Multiplies in a fiend point.
[153:43.46] (upbeat music)
[153:55.94] And then, it neither, it neither accesses anything in it.
[154:00.94] (upbeat music)
[154:05.44] Okay, K1, scaler, endo in, right?
[154:10.28] So that's, I'm a little bit confused here
[154:15.28] because as far as I can tell,
[154:19.16] the only thing that it ever uses the fiend point for
[154:23.68] is the window size, if not a fiend point,
[154:28.24] and this is just probably a point base.
[154:33.24] A fiend point equals point base,
[154:38.10] but that's what was being passed in anyway.
[154:40.40] The window size,
[154:44.00] must be a power of two.
[154:52.60] (upbeat music)
[154:55.18] Wait, window size was eight, I thought.
[155:01.52] Okay, let me look at this again.
[155:04.56] Window size, set window size.
[155:08.84] Set window size is eight.
[155:13.04] (upbeat music)
[155:15.62] (keyboard clicking)
[155:18.62] Oh, 256 mod, it's 256 mod W, not W mod 256.
[155:36.74] Okay, so power of two, that makes sense.
[155:42.28] Anything's gonna go into that zero, got it.
[155:43.94] All right, now I understand what that was doing.
[155:46.66] All right, pre-compute.
[155:48.04] Pre-compute points is actually,
[155:54.58] Jacobian point normalized, pre-computes,
[156:01.78] Jacobian point zero,
[156:05.58] mask big, shift by.
[156:13.46] All right, so I see where the scalar does something,
[156:16.18] but as far as I can tell,
[156:18.06] I mean,
[156:22.66] the window size is the only thing that's actually used.
[156:42.50] I mean, I guess that could be.
[156:44.26] I don't know why it's necessary
[156:46.66] to go through the trouble of making a point
[156:50.30] if you're not gonna use it.
[156:51.72] But that, I mean, the code is what the code is.
[156:56.26] Point pre-computes.
[156:58.34] It's a weak map, and I'm guessing a weak map
[157:03.42] can have objects that are mapped by their properties.
[157:08.42] (soft music)
[157:10.84] All right, it sets the pre-computes.
[157:18.80] Really, that's it?
[157:22.38] If not pre-computes, pre-compute window.
[157:34.34] (soft music)
[157:36.76] But it's just eight.
[157:40.14] That's all it is.
[157:46.22] Literally, the window is eight.
[157:47.86] That's not even a value you get to choose.
[157:49.98] Okay, set window size.
[157:59.30] (soft music)
[158:01.72] Default window size is eight.
[158:15.82] It's never changed.
[158:21.60] (soft music)
[158:24.02] All right, let's see what 2-A-Fine is.
[158:48.76] (soft music)
[158:51.18] So, we do some inverted Z.
[158:57.64] What is the GX and GY ever even used for?
[159:04.90] (soft music)
[159:07.32] (keyboard clacking)
[159:10.32] Turn new point.
[159:24.12] Okay, and then to public key.
[159:32.82] So, from private key,
[159:35.92] (soft music)
[159:38.34] and multiply.
[159:40.92] (soft music)
[159:43.34] That's 2-A-Fine.
[159:45.92] (soft music)
[159:48.92] And then 2-Hex is...
[159:53.92] Oh, whoops.
[160:03.34] Oh, wow.
[160:05.30] So, I've been wrong about this.
[160:06.96] So, apparently, return prefix, hold on, is compressed.
[160:11.84] Oh, there it is.
[160:12.68] Oh, yeah, okay, good, good, good, good.
[160:14.76] Is compressed.
[160:15.80] Has even Y.
[160:19.38] Ooh.
[160:20.22] Now, I know what that is.
[160:25.72] (soft music)
[160:28.14] (keyboard clacking)
[160:31.06] (soft music)
[160:33.48] Mod two.
[160:54.14] (soft music)
[160:56.56] (keyboard clacking)
[160:59.56] Okay.
[161:26.98] (soft music)
[161:29.40] I wonder if that's even what that means, though.
[161:34.16] Has even Y.
[161:35.70] That might, that, the term even may not mean
[161:38.82] what we think it means.
[161:40.62] (soft music)
[161:43.04] Oh, it does mean the same thing.
[161:51.40] (soft music)
[161:54.82] (keyboard clacking)
[161:57.82] Okay.
[162:14.50] (soft music)
[162:16.92] (keyboard clacking)
[162:19.92] All right, so, the GX and the GY are used
[162:46.30] to set some pre-computed value.
[162:48.10] I don't know why, but they are important
[162:50.02] in terms of the set operation that's going on there.
[162:53.94] (soft music)
[162:56.36] Let me just make sure again.
[163:13.22] Multiply returns, so it does return.
[163:18.22] (soft music)
[163:20.86] Does this return a new point?
[163:42.78] Okay.
[163:43.66] (soft music)
[163:46.08] 0.1, 0.1.
[163:53.64] And then what was the two hex then?
[163:58.14] Oh, yeah.
[164:03.78] (soft music)
[164:07.00] (keyboard clacking)
[164:10.00] So, that's the gist of it.
[164:21.50] (soft music)
[164:23.92] What did the Jacobian point do with the new?
[164:35.56] Let's see.
[164:36.88] Yeah, Jacobian point.
[164:40.40] Is that a class?
[164:41.64] Okay, constructor.
[164:44.80] Literally doesn't do anything with it.
[164:47.82] An XYZ invert.
[164:52.72] (soft music)
[164:56.14] (keyboard clacking)
[164:59.14] X, Y, Z.
[165:12.46] What does underscore 1N mean?
[165:15.94] I think that doesn't mean anything.
[165:19.32] That could have just been a typo.
[165:25.96] 'Cause there's no difference between an underscore 1N.
[165:30.32] Oh, so for whatever reason,
[165:33.88] he just likes to put the underscore on that 1N.
[165:38.68] 'Cause it's, I don't know,
[165:43.84] maybe make it stand out or something.
[165:45.48] I don't know.
[165:46.76] (soft music)
[165:49.18] (keyboard clacking)
[165:52.18] Jacobian point.
[166:15.64] (soft music)
[166:18.06] (keyboard clacking)
[166:21.06] Okay, XYZ.
[166:26.10] And that multiply the scalar.
[166:31.32] GX and GY don't do anything.
[166:37.96] Oh no, they do when it comes into the inversion.
[166:40.82] That's, and then the modding stuff.
[166:42.36] Okay.
[166:43.20] (soft music)
[166:45.62] (keyboard clacking)
[166:48.62] Could be something else.
[167:08.94] (soft music)
[167:13.90] All right, so that's breaking it down
[167:16.70] to the point of all the normal stuff here.
[167:18.80] That normal, like this is what can be read.
[167:22.88] Okay, glossary.
[167:28.22] I might save this one for later.
[167:29.96] 32 random bytes are generated.
[167:32.70] The bytes are checked to,
[167:41.10] if the bytes can be converted.
[167:45.76] And point.
[167:52.94] Wait, so I want to learn a little bit more
[167:57.14] about this from compressed then.
[167:59.18] (soft music)
[168:01.60] (keyboard clacking)
[168:04.60] Hmm.
[168:07.06] (soft music)
[168:09.48] Where's Y1?
[168:29.56] (soft music)
[168:31.98] Okay, so yeah.
[168:48.02] Okay, public key.
[168:57.92] (soft music)
[169:00.34] (sighs)
[169:05.70] Let's see.
[169:25.52] An X, a, what is it?
[169:27.44] A 32 byte X value.
[169:32.00] Is that what that is?
[169:34.12] Yeah, a 32 byte X value.
[169:36.56] (soft music)
[169:38.98] Plus,
[169:41.28] an indicator of whether the Y value is odd.
[169:50.52] (soft music)
[169:55.98] Oh no, what happened?
[169:57.68] No!
[170:00.62] Oh, it came back.
[170:04.62] What was that about?
[170:05.62] Looks like my phone's charging.
[170:11.98] I don't know why that went out.
[170:14.18] Did I get a message?
[170:15.18] Eh, I don't know.
[170:24.30] Mic's still going, so we're good there.
[170:26.90] Okay, a 32 byte value plus an indicator
[170:29.58] of whether the Y value is odd,
[170:31.70] is even,
[170:34.62] is prefixed with a single byte
[170:50.42] to indicate whether the Y value is even or odd.
[170:55.42] Okay.
[171:11.18] (soft music)
[171:13.60] So the byte,
[171:40.30] having the Y value.
[171:42.40] The indicator is either,
[171:51.34] if Y, whoops,
[172:04.26] if Y is even
[172:09.66] or if Y is odd.
[172:14.66] (soft music)
[172:43.54] Prefixed with a byte.
[172:45.14] Since the Y value,
[172:57.06] let's see.
[173:03.58] (soft music)
[173:07.66], 32.
[173:08.50] There we go.
[173:28.30] (soft music)
[173:30.72] 32, any 32 random bytes,
[173:44.10] 256 bits, whoops,
[173:54.98] that are within the order,
[173:59.98] the order.
[174:01.48] Okay.
[174:27.26] (soft music)
[174:29.68] Is within curve order.
[174:55.98] Oh, that's a little bit weird.
[174:57.52] Oh, the scaler is the number.
[175:04.46] Hold on, let me just double check on that.
[175:16.02] (sighs)
[175:24.38] (soft music)
[175:26.26] And there's a private key, right?
[175:27.90] Hold on, hold on.
[175:40.82] They go to a private key.
[175:45.12] Okay.
[175:52.74] Is it new?
[175:53.80] Get public key.
[175:59.66] Let's just make sure I got this right here.
[176:02.10] From private key.
[176:04.72] From private.
[176:08.74] Base multiply.
[176:14.44] (soft music)
[176:16.86] Okay, got it.
[176:24.34] (soft music)
[176:26.76] Oops.
[176:54.70] (soft music)
[176:57.12] All right, I think I got this a little bit better now here.
[177:05.10] (soft music)
[177:08.86] (keyboard clicking)
[177:11.86] So this is basically base.
[177:35.16] (soft music)
[177:37.58] And then base.multiply.
[177:41.24] Okay.
[177:43.80] So the one thing that I don't know about this then,
[177:51.52] what was it?
[177:52.36] From compressed.
[177:55.60] (soft music)
[177:58.02] (keyboard clicking)
[178:01.02] Is odd.
[178:06.90] First by odd, assortability.
[178:09.40] (soft music)
[178:11.82] Mod negative y.
[178:20.36] (keyboard clicking)
[178:23.36] (soft music)
[178:25.78] Oh, what happened?
[178:39.50] Something's about to happen again.
[178:41.20] I heard a little crackle that I've heard
[178:45.56] right before the camera went out.
[178:47.26] All right, so pubkey hash.
[178:52.20] (soft music)
[178:54.62] All right, so if I unwrap this,
[179:05.80] I think this is about how it goes.
[179:07.60] Let me see here.
[179:10.98] (soft music)
[179:14.48] (keyboard clicking)
[179:17.48] Validity is checked.
[179:34.72] The public key is produced by creating
[179:42.84] (soft music)
[179:45.26] a point on a known curve.
[179:53.18] All right, so let
[179:57.48] prove_buff,
[180:00.20] two hex prove_buff.
[180:03.56] (soft music)
[180:05.98] (keyboard clicking)
[180:08.98] Okay, so here's some magic curve values.
[180:21.50] That is within curve, is all these things.
[180:27.26] (soft music)
[180:29.68] (keyboard clicking)
[180:32.68] Okay, let,
[180:48.08] let,
[180:50.56] let.
[180:52.46] (soft music)
[180:54.88] Hmm, I see.
[181:09.30] So I'll have that thing.
[181:10.46] Okay, we also have that thing there.
[181:14.32] (soft music)
[181:17.74] (keyboard clicking)
[181:20.74] All right, so is within curve order.
[181:30.44] (soft music)
[181:32.86] Order in.
[181:46.72] Curve in maybe.
[181:48.14] Jacobian point,
[181:55.36] whatever this is.
[181:57.74] Base pub_point is multiply_priv_num.
[182:02.58] (soft music)
[182:05.00] By all this crap in the window size.
[182:10.40] (soft music)
[182:12.82] (keyboard clicking)
[182:15.82] X, Y equals
[182:29.44] X, Y dot Y.
[182:34.98] (soft music)
[182:38.08] X, Y.
[182:39.26] (soft music)
[182:41.68] (keyboard clicking)
[182:44.68] J point,
[182:47.58] J point,
[182:50.10] pub_point.
[182:51.18] (soft music)
[182:52.62] And then,
[182:53.66] let's say pub_point
[182:56.30] (soft music)
[182:58.10] and pub_point.
[182:59.48] (soft music)
[183:02.30] There we go.
[183:03.14] (soft music)
[183:05.56] In essence.
[183:07.94] (laughing)
[183:10.18] (soft music)
[183:12.60] All right, let's see if I can actually
[183:17.92] make sense of this.
[183:18.76] I'm gonna try to bring this one back.
[183:20.92] (soft music)
[183:23.26] Oops.
[183:24.10] (soft music)
[183:25.72] Priv_point.js.
[183:28.40] (soft music)
[183:29.62] Unexpected token on line 14.
[183:32.56] (soft music)
[183:33.58] Oh.
[183:34.42] (soft music)
[183:36.24] Right.
[183:37.08] (soft music)
[183:39.62] (keyboard clicking)
[183:42.62] (soft music)
[184:12.28] Let's see.
[184:13.16] This is...
[184:14.60] (soft music)
[184:17.02] Hold on, let me make sure this is still right.
[184:25.52] Okay, so if I do
[184:27.04] (mumbling)
[184:28.20] in
[184:29.56] to_string_16.
[184:32.72] (soft music)
[184:35.14] I can get any amount there.
[184:38.04] One, two, three, four, five, six,
[184:41.64] seven, eight, nine, 10, 11, 12.
[184:44.56] So what I need...
[184:45.76] (soft music)
[184:48.18] I leave it with unexpected token, okay.
[184:51.44] So let's try this.
[184:53.92] Let's try something...
[184:55.92] Ah.
[184:56.76] (soft music)
[184:59.18] (keyboard clicking)
[185:02.18] Okay, I think it's something like that.
[185:24.10] So that's what a private key actually is.
[185:27.08] (soft music)
[185:29.50] Uh-oh.
[185:34.80] Curve has magic A and B values.
[185:38.00] (soft music)
[185:40.42] (keyboard clicking)
[185:43.42] I wonder if he was doing that as a parser trick.
[186:01.16] (soft music)
[186:03.58] (keyboard clicking)
[186:06.58] So there's some magic curve values.
[186:16.50] All right, let me just double check that again.
[186:21.38] There's only one thing called curve
[186:22.82] and it's got those figures to it.
[186:25.10] Curve equals, yep.
[186:27.74] That's good.
[186:32.54] So we used A, B, N, but not P so far, and not beta.
[186:36.82] Those must be used somewhere else.
[186:38.62] (soft music)
[186:41.04] Let X2
[186:45.06] equals
[186:51.18] pubkey.slice2.
[186:56.86] (soft music)
[187:01.78] (keyboard clicking)
[187:04.26] Okay, let's...
[187:05.70] (soft music)
[187:08.12] Okay, isfirstbyod is gonna be equal to pub
[187:32.50] key
[187:33.34] zero
[187:35.38] and one.
[187:38.54] What?
[187:44.74] Wouldn't it just be...
[187:45.86] Wait, where's bytes coming from?
[187:52.92] Let me go look for isfirstbytod.
[188:01.16] From compressed hex bytes.
[188:03.44] (soft music)
[188:07.00] (keyboard clicking)
[188:10.00] the world. (soft music)
[188:38.46] Oh, okay, so apparently there's a default
[188:40.48] that if it's just an X value,
[188:42.84] then you can assume that
[188:46.20] the first byte
[188:51.40] is even, I guess.
[188:54.80] That's what it appears to be here.
[188:56.48] Okay, so let's take a look at that.
[189:01.58] (soft music)
[189:04.00] Okay, expect
[189:14.46] odd equals
[189:17.70] subarray one.
[189:28.62] (keyboard clicking)
[189:31.62] And then X.
[189:35.22] Whoops, that's not what I wanted to do.
[189:38.96] Dang it.
[189:39.80] Oh yes, it went back, sweet.
[189:41.90] (soft music)
[189:44.32] (keyboard clicking)
[189:47.32] Let's see.
[190:04.56] Where was this one?
[190:08.50] (soft music)
[190:10.92] (keyboard clicking)
[190:13.92] All right, so then we say
[190:26.90] let X two,
[190:29.66] let X three,
[190:32.52] let Y,
[190:40.84] let Y two.
[190:42.36] Okay, Y squared.
[190:44.56] Got it, got it, got it.
[190:46.20] Okay.
[190:47.02] Why is there a square root function?
[190:53.86] Oh.
[190:58.56] Yeah.
[191:05.16] (soft music)
[191:07.58] Fancy square root mod.
[191:14.28] Very complicated.
[191:16.30] (laughing)
[191:18.68] We'll just elide that away.
[191:20.20] (soft music)
[191:22.62] (keyboard clicking)
[191:25.62] All right.
[191:39.62] And then there is no is short.
[191:42.82] And we already have our first by odd.
[191:51.58] So if,
[191:52.74] okay, expect odd.
[191:58.12] And not Y is odd.
[192:20.98] And Y equals mod Y.
[192:23.58] And what is this mod function, I wonder?
[192:26.88] It's probably no normal mod function.
[192:31.22] (laughing)
[192:33.46] It's probably the most complicated mod
[192:36.46] I've ever seen in my life.
[192:37.86] If I can find it.
[192:39.70] Wait, let's see.
[192:45.54] (soft music)
[192:47.96] Okay.
[192:52.16] All right, that's where the curve P value comes in.
[192:58.58] Okay.
[192:59.94] So let me see if I can go find that now.
[193:02.24] (soft music)
[193:05.80] (keyboard clicking)
[193:08.80] All right, so we got the P value there.
[193:29.36] All right, and these mods happen
[193:36.60] a few times.
[193:37.62] (soft music)
[193:40.04] (keyboard clicking)
[193:43.04] (soft music)
[193:45.46] (keyboard clicking)
[193:48.46] (soft music)
[193:50.88] (keyboard clicking)
[193:53.88] (soft music)
[193:56.30] (keyboard clicking)
[194:06.76] (soft music)
[194:09.18] Okay.
[194:28.38] (soft music)
[194:31.60] (keyboard clicking)
[194:34.60] Ah!
[194:40.08] Oh no.
[194:41.46] What is this?
[194:42.62] (soft music)
[194:45.04] All right, there we go.
[195:00.40] Let me see if I can fix this one.
[195:02.10] (soft music)
[195:04.52] All right, nine.
[195:15.56] (soft music)
[195:17.98] (keyboard clicking)
[195:20.98] Oh, there's a comma.
[195:32.88] Right, okay.
[195:35.44] (soft music)
[195:37.86] (keyboard clicking)
[195:40.86] Okay.
[196:04.42] Very, very boring.
[196:06.74] But kind of nice to finally have
[196:10.42] tenuous grasp, is that the word?
[196:16.02] Seems like that's the opposite.
[196:17.24] Tenuous would mean like very strong.
[196:19.46] This is like very weak.
[196:21.58] (soft music)
[196:35.86] All right, so that's not what I was expecting
[196:38.30] to do for this.
[196:39.82] (soft music)
[196:43.24] (keyboard clicking)
[196:46.24] All right, 11.
[197:10.72] It's missing a semi-colon.
[197:12.38] Maybe.
[197:15.62] (soft music)
[197:18.04] Okay, re-declared.
[197:37.52] What is this?
[197:39.26] Re-declared.
[197:40.54] Block scope variable X.
[197:45.02] Where was X?
[197:49.70] What?
[197:56.08] Oh, there we go.
[198:04.60] (soft music)
[198:07.02] There we go.
[198:22.00] (keyboard clicking)
[198:25.00] All right, I don't know.
[198:46.54] (soft music)
[198:48.96] All right, so
[199:15.58] generate some random bytes.
[199:16.82] Go to hex, go to big int.
[199:18.90] Find some fancy curve values.
[199:21.00] Fancy math.
[199:33.72] (laughs)
[199:35.06] Fancy math.
[199:45.54] All right, cool.
[199:46.38] So that's it.
[199:47.20] That's the essence of it.
[200:01.22] Okay.
[200:02.16] It's not what I intended to do,
[200:03.62] but that's what I did.
[200:05.14] Oh.
[200:07.20] All right.
[200:09.46] Private key, public key.
[200:10.70] Pub key hash.
[200:14.26] Let's actually get these.
[200:15.76] ABC, LMN.
[200:20.96] Okay.
[200:23.94] JJKL, yeah.
[200:25.34] So we're gonna say also
[200:32.76] pub key
[200:34.70] PK.
[200:37.54] (keyboard clicking)
[200:40.54] Also priv key.
[200:53.86] Let's do address.
[201:04.60] (keyboard clicking)
[201:07.60] Address.
[201:10.64] Base
[201:13.76] 58 check
[201:16.48] encoded
[201:19.08] pub key hash.
[201:20.64] (keyboard clicking)
[201:23.64] (upbeat electronic music)
[201:27.14] Version is CC.
[201:41.20] Pub key.
[201:43.74] Let's see.
[201:46.52] Is it CC or?
[201:47.52] It's private key.
[201:49.80] 4C.
[201:50.64] (keyboard clicking)
[201:53.64] Odd.
[202:04.88] Odd byte is, oh, whoops.
[202:09.72] Put 5DDD.
[202:10.92] (keyboard clicking)
[202:13.92] (upbeat electronic music)
[202:17.42] Comm byte
[202:24.48] is O2.
[202:26.92] (keyboard clicking)
[202:29.92] Y is even.
[202:32.30] (keyboard clicking)
[202:35.30] Pub key.
[202:37.68] Check sum.
[202:39.84] (keyboard clicking)
[202:43.04] (upbeat electronic music)
[202:45.04] The coin version
[202:47.32] encoding is like this.
[202:52.24] (keyboard clicking)
[202:55.24] Coin version bytes.
[203:03.28] (keyboard clicking)
[203:05.80] Compression flag.
[203:08.00] (keyboard clicking)
[203:10.44] Compression
[203:11.80] (keyboard clicking)
[203:12.88] byte.
[203:13.72] There's our two, four.
[203:16.52] Even Y, zero, zero, three.
[203:20.12] Or odd Y.
[203:21.24] (keyboard clicking)
[203:24.24] Public key X value.
[203:33.04] (keyboard clicking)
[203:34.44] And
[203:35.36] check sum
[203:37.60] (keyboard clicking)
[203:39.60] of
[203:40.44] (keyboard clicking)
[203:43.88] two, three, and four.
[203:46.84] (keyboard clicking)
[203:49.84] (upbeat electronic music)
[203:53.34] (keyboard clicking)
[203:56.34] (keyboard clicking)
[203:59.34], (keyboard clicking)
[204:04.34] (upbeat electronic music)
[204:07.84] (keyboard clicking)
[204:13.38] (upbeat electronic music)
[204:31.20] Value.
[204:34.54] (keyboard clicking)
[204:35.62] 32 bytes.
[204:37.12] (keyboard clicking)
[204:40.12] 5DDD.
[204:45.42] (keyboard clicking)
[204:48.42] Base.
[205:02.88] (keyboard clicking)
[205:04.10] 58.
[205:04.94] Check is
[205:06.32] (keyboard clicking)
[205:09.46] cat, coin, compression,
[205:13.42] hub key, check sum.
[205:15.94] (keyboard clicking)
[205:18.94] (upbeat electronic music)
[205:22.44] Oh, whoops, I got that one wrong.
[205:48.32] It's okay.
[205:49.14] It's okay.
[205:51.20] It's okay.
[205:52.04] My daughter has learned to say that when she makes mistakes.
[205:58.04] She says, "It's okay, don't worry, it's okay."
[206:00.36] (keyboard clicking)
[206:03.36] Ash, which is 20 bytes.
[206:11.24] (keyboard clicking)
[206:14.24] (upbeat electronic music)
[206:17.74] (keyboard clicking)
[206:20.74] (keyboard clicking)
[206:23.74] (keyboard clicking)
[206:26.74] (keyboard clicking)
[206:29.74] (keyboard clicking)
[206:32.74] (keyboard clicking)
[206:35.74] (keyboard clicking)
[206:38.74] (keyboard clicking)
[206:41.74] (keyboard clicking)
[206:45.82] (keyboard clicking)
[207:07.74] Four bytes of.
[207:09.74] (keyboard clicking)
[207:12.74] Comp byte,
[207:27.14] hub key, hash,
[207:30.54] check sum,
[207:37.46] decoded,
[207:38.54] encoded.
[207:41.96] All right, cool.
[207:51.98] All right, we're gonna keep this one really short.
[208:05.26] (keyboard clicking)
[208:08.26] I was gonna say, terse.
[208:16.14] Not necessarily short, but terse.
[208:18.18] Okay, so private key,
[208:21.66] hub key, hash,
[208:25.70] public key,
[208:32.90] also payment address,
[208:37.32] pay adder,
[208:38.16] adder.
[208:43.66] (keyboard clicking)
[209:10.98] Cannot be reversed into public key.
[209:15.86] There we go.
[209:40.68] (coughs)
[209:42.76] Let's take this down to the bottom.
[209:47.36] With also wallet import format,
[209:56.36] paper wallet import private key.
[210:02.92] (keyboard clicking)
[210:05.92] Import private key.
[210:34.12] Can be reversed into the private key.
[210:39.12] Coin version privacy pipe.
[210:55.22] (keyboard clicking)
[210:58.22] Okay.
[211:15.80] Wait, is this right?
[211:25.74] Hold on.
[211:26.58] Public key does contain the compression byte
[211:32.66] in its decoded form, right?
[211:38.30] No, when it's hashed.
[211:39.58] Okay, so address, sorry,
[211:42.38] address does not have the compression byte, duh.
[211:46.12] Okay, no comp byte.
[211:49.10] (keyboard clicking)
[211:52.10] There we go.
[211:56.48] (keyboard clicking)
[211:59.48] Import key.
[212:21.68] Okay, what do they call it?
[212:26.00] (keyboard clicking)
[212:28.04] Swipe, import key, private key QR, all right.
[212:32.30] Hallway is zero, zero, one.
[212:54.52] (keyboard clicking)
[212:57.44] Okay, private key, 32 bytes.
[213:02.44] Oops.
[213:11.56] Okay.
[213:12.40] (keyboard clicking)
[213:15.40] (keyboard clicking)
[213:18.40] (keyboard clicking)
[213:21.40] (keyboard clicking)
[213:50.30] All right, so private key is going to be RDDD.
[213:55.30] Oh, whoops, did I grab, did I grab the bat?
[214:06.48] No, I didn't grab the bat.
[214:08.56] Okay, good.
[214:09.40] Okay, whiff, whiff, whiff.
[214:17.26] Woof, woof.
[214:19.20] (keyboard clicking)
[214:22.20] All right, this is going to decode it, no, private key.
[214:33.04] Cool.
[214:36.90] (keyboard clicking)
[214:39.90] 22.
[214:42.24] (keyboard clicking)
[214:46.24] (keyboard clicking)
[214:49.24] I think I'm gonna move that one section
[215:08.84] to developer troubleshooting.
[215:10.34] (keyboard clicking)
[215:13.34] (keyboard clicking)
[215:15.94] Oh.
[215:16.78] (keyboard clicking)
[215:19.78] All right, so yeah, we've got the private key,
[215:23.86] got the comp byte, got the pay editor.
[215:27.06] I'm not interested in the pay editor, got the check.
[215:29.68] (keyboard clicking)
[215:32.68] Okay, so I'm decoded.
[215:39.82] (keyboard clicking)
[215:43.82] (keyboard clicking)
[215:46.82] (keyboard clicking)
[215:58.22] (keyboard clicking)
[216:01.22] (keyboard clicking)
[216:04.22] All right, there we go.
[216:31.48] Yeah, that's pretty much all I wanted to cover
[216:34.92] in the glossary.
[216:35.76] I went a little deeper on the public and private keys
[216:37.78] than I thought I was gonna go.
[216:39.28] But I was gonna get there eventually one way or another.
[216:44.04] Okay, so what do you need to know?
[216:48.36] What's the full scope of things you need to know?
[216:50.12] You need to know what private key is.
[216:52.82] You need to know what, so private key goes to public key,
[216:57.12] public key goes to pubkey hash.
[216:59.64] Let's see, compressed.
[217:03.56] So we do need to explain that.
[217:05.56] That's one of the things.
[217:06.64] Compressed, we need to explain version.
[217:10.00] W-X-Y-Z, so version.
[217:13.52] And these are pretty simple.
[217:17.60] Compressed.
[217:21.24] (keyboard clicking)
[217:25.12] A private key always has a zero.
[217:29.88] The first byte of a...
[217:38.48] Let's see, a private key always has a...
[217:44.56] Actually, first of all, let me look into this
[217:48.04] a little bit deeper real quick.
[217:50.50] Nope.
[217:53.40] Dash keys, compressed.
[217:56.90] Okay, good.
[218:03.50] So we don't, yeah, we don't ever put that
[218:09.96] with a pubkey hash, excellent.
[218:11.46] Has a compressed byte.
[218:23.08] Prefix of zero, one.
[218:27.32] And...
[218:31.28] Fine.
[218:41.68] This zero, one.
[218:52.28] The compression flag.
[218:54.08] This is a signal.
[219:04.56] This indicates that pubkey hashes should be...
[219:14.08] (keyboard clicking)
[219:17.08] Use only the X value.
[219:27.16] Do not include the Y value.
[219:43.68] All right.
[219:44.52] This indicates, that's a $3 word.
[219:50.72] What's something, you know, that...
[219:52.48] Mm.
[219:55.50] (yawns)
[220:07.84] Hmm.
[220:08.68] A public key starts with either...
[220:19.76] Okay.
[220:23.24] The Y value of C public key.
[220:35.20] Also, compression flag, recovery bit,
[220:40.20] odd Y, odd even Y bit.
[220:51.00] (keyboard clicking)
[221:18.88] Quadrants.
[221:20.00] Okay, pubkey all starts with a visual compression flag.
[221:26.28] This indicates where the C public key for more info.
[221:30.90] Ooh.
[221:36.44] (keyboard clicking)
[221:41.84] (keyboard clicking)
[221:44.84] C also public key.
[222:07.80] There we go.
[222:10.72] Compressed byte version.
[222:15.40] Also, base 58 check version, coin version.
[222:32.04] Privacy, privacy byte.
[222:39.12] (keyboard clicking)
[222:42.12] Okay.
[222:47.28] Dash mainnet private keys start with 0x4C.
[222:56.36] Oh, oops, CC.
[223:05.12] Public keys.
[223:07.88] Okay, CC.
[223:14.44] Did I say that right?
[223:20.44] Coin, compression, whoops.
[223:27.14] PKH.
[223:29.20] Check.
[223:33.88] (keyboard clicking)
[223:36.88] There we go.
[224:02.84] CF, is that what we said?
[224:04.92] Okay, here we go.
[224:10.16] Version, let's go back to that one again.
[224:15.10] Okay.
[224:20.96] Payment addresses start with 0x4C.
[224:31.40] (keyboard clicking)
[224:34.40] Dash testnet uses 0xEF and 0x8C respectively.
[224:43.68] (keyboard clicking)
[224:46.68] 0xEF and 0x8C respectively.
[224:54.52] The bytes were chosen because they encode to X or Y.
[225:11.36] The bytes were chosen because they encode to X or Y.
[225:16.36] (keyboard clicking)
[225:19.76] (dramatic music)
[225:22.52] Because they base 58 encode to X.
[225:48.46] (keyboard clicking)
[225:52.14] These base 58 encode to Y.
[225:57.02] (keyboard clicking)
[226:00.02] (dramatic music)
[226:02.76] It's used for dash mainnet widths.
[226:26.78] Private key.
[226:30.48] (keyboard clicking)
[226:33.48] Is the payment, the prefix for payment addresses.
[226:42.92] Public key hash.
[226:45.52] All right, these bytes are used because.
[226:50.48] (keyboard clicking)
[226:54.52] (dramatic music)
[226:57.26] To X, back to the dark coin.
[227:12.76] (keyboard clicking)
[227:18.92] For mystery.
[227:24.30] (dramatic music)
[227:27.68] IE dark coin.
[227:30.88] (dramatic music)
[227:33.64] Okay.
[227:47.12] (dramatic music)
[227:49.86] And.
[227:53.44] (dramatic music)
[227:55.52] Are used for.
[227:57.44] (dramatic music)
[228:00.20] Dash test net.
[228:09.44] (dramatic music)
[228:19.56] Is base 64 encode to Y.
[228:23.68] All right, version's done.
[228:25.10] Okay.
[228:27.08] Do we need anything about checksum, maybe?
[228:32.16] Yeah, just a little one.
[228:35.52] Checksum.
[228:38.04] (dramatic music)
[228:40.78] Okay.
[228:44.52] (dramatic music)
[228:48.10] Okay.
[228:48.94] (dramatic music)
[228:50.34] Also, SHA-256.
[228:54.00] (dramatic music)
[228:55.70] So what do we call this?
[228:57.14] (dramatic music)
[228:59.90] Okay.
[229:09.78] (dramatic music)
[229:12.18] The first four bytes of.
[229:16.62] (dramatic music)
[229:19.38] Checksum.
[229:24.82] (dramatic music)
[229:26.98] Of.
[229:27.82] (dramatic music)
[229:30.56] SHA of, so the first four bytes.
[229:44.98] SHA-256 hash of.
[229:49.22] (dramatic music)
[229:51.96] The decoded.
[229:55.58] (dramatic music)
[229:57.30] With or adder.
[229:59.94] (dramatic music)
[230:02.70] Eh.
[230:10.34] (dramatic music)
[230:13.08] (computer beeping)
[230:16.00] (computer beeping)
[230:18.92] (computer beeping)
[230:21.84] (computer beeping)
[230:40.32] (computer beeping)
[230:47.88] (computer beeping)
[230:50.72] Appended.
[230:51.56] (computer beeping)
[230:54.48] The last four bytes of a decoded.
[231:00.72] (computer beeping)
[231:04.16] With or adder.
[231:05.52] (computer beeping)
[231:16.32] These are the.
[231:17.56] (dramatic music)
[231:20.32] First four bytes of the SHA-256 hash of the same.
[231:29.24] There we go.
[231:31.32] (dramatic music)
[231:34.06] C, address and.
[231:40.72] (dramatic music)
[231:42.48] With.
[231:43.32] (dramatic music)
[231:46.06] With.
[231:46.90] (dramatic music)
[231:50.02] Okay, that's looking good.
[231:51.22] (dramatic music)
[231:53.98] Okay, is there anything else?
[232:03.26] (dramatic music)
[232:06.02] (computer beeping)
[232:09.94] (computer beeping)
[232:12.86] (dramatic music)
[232:15.62] (computer beeping)
[232:18.54] (dramatic music)
[232:21.30] (computer beeping)
[232:24.22] (dramatic music)
[232:53.54] Let's have a, whoops, a section called troubleshooting.
[232:58.54] (dramatic music)
[233:01.42] Using uncompressed keys.
[233:08.94] If you see these values,
[233:20.22] then you've mistakenly used an uncompressed key.
[233:25.22] (dramatic music)
[233:27.98] Let's see, incorrect.
[233:42.94] (dramatic music)
[233:45.70] (computer beeping)
[233:48.62] (dramatic music)
[234:12.18] Let's see, anatomy of with.
[234:17.18] (dramatic music)
[234:20.14] Outers and withs.
[234:23.90] (dramatic music)
[234:26.66] Okay.
[234:35.26] (dramatic music)
[234:38.38] (computer beeping)
[234:41.30] Glossary of terms.
[234:45.62] (dramatic music)
[234:48.46] All right, let me double check here.
[235:06.42] (dramatic music)
[235:09.18] Let's see, developer resources.
[235:18.78] (dramatic music)
[235:21.54] (computer beeping)
[235:24.46] What did I say?
[235:41.10] Oh, implementation details.
[235:44.38] (dramatic music)
[235:47.14] (computer beeping)
[235:50.06] Okay.
[236:05.78] (dramatic music)
[236:07.62] Fixtures.
[236:08.46] (dramatic music)
[236:11.22] (computer beeping)
[236:14.14] (dramatic music)
[236:16.90] (computer beeping)
[236:19.82] A reference implementation.
[236:46.54] (dramatic music)
[236:49.26] A fully functional, but simple.
[236:53.66] (dramatic music)
[236:56.42] Ready, reference implementation of dash keys.
[237:06.90] (dramatic music)
[237:10.90] (computer beeping)
[237:13.82] Withs and pay adders.
[237:33.26] (dramatic music)
[237:36.02] Pay addresses.
[237:40.22] (dramatic music)
[237:42.98] Let's see, what does it say in the package.json here?
[237:53.26] Generate, validate, and create.
[237:54.54] Didn't I call it something else in the CLI, maybe?
[237:57.26] (dramatic music)
[238:00.02] (computer beeping)
[238:02.94] Oh, that's good.
[238:26.50] (dramatic music)
[238:29.26] (computer beeping)
[238:32.18] (dramatic music)
[238:34.94] (computer beeping)
[239:03.38] Suitable for porting to other languages.
[239:08.38] Suitable for learning dash protocols,
[239:28.98] specs and protocols, and porting to other languages.
[239:33.74] (dramatic music)
[239:36.50] Okay, there we go.
[239:44.58] (dramatic music)
[239:47.34] Table of contents.
[239:49.38] (dramatic music)
[239:52.14] (computer beeping)
[239:55.06] Install.
[239:59.94] (dramatic music)
[240:01.94] Usage.
[240:02.78] (dramatic music)
[240:05.54] Zoomonic.
[240:21.74] (dramatic music)
[240:25.10] A canonical.
[240:26.02] (dramatic music)
[240:28.78] Yeah.
[240:34.02] (dramatic music)
[240:36.78] (computer beeping)
[240:39.70] Actually, I don't think that this makes
[241:04.94] a lick of difference.
[241:06.38] Well, the whips and the adders do, but.
[241:08.54] (dramatic music)
[241:11.30] All keys used in this example and across the...
[241:35.78] This ecosystem of dash tools uses our...
[241:40.78] Our HD keys derived from the Zoomonic.
[241:57.82] (dramatic music)
[242:05.30] (computer beeping)
[242:08.22] All right, this is looking really good, I think.
[242:25.42] All right, so we got the install.
[242:29.22] We got through CLI, node, bundlers, browser.
[242:32.50] We got usage, we got API, we got glossary.
[242:36.14] I need to double-check the glossary
[242:38.94] to make sure that we got everything in here.
[242:41.10] C.
[242:49.66] All right, github.com-hive-...
[243:01.90] Is it?
[243:02.74] No, sacp256k1.js.
[243:07.34] All right, what else?
[243:17.70] Oh, we do have implementation details.
[243:21.70] (dramatic music)
[243:24.46] All right, let's see.
[243:38.02] Rocket.
[243:38.86] Install.
[243:43.70] Usage.
[243:44.78] (dramatic music)
[243:47.54] Let's see.
[243:54.22] There's one that Matt likes to use.
[243:58.70] Where is it?
[244:00.94] Might be the teacher or the raised hand.
[244:05.46] API, maybe gears.
[244:14.62] (dramatic music)
[244:17.38] Developer resources.
[244:20.38] Toolbox.
[244:25.02] And then documents here.
[244:34.06] (dramatic music)
[244:39.18] (keyboard clicking)
[244:42.18] Okay, so there we go.
[244:48.74] So we've got that all in here.
[244:51.02] (dramatic music)
[244:53.78] Let's see.
[245:07.98] (dramatic music)
[245:09.94] Skeleton.
[245:11.50] What else do we have?
[245:15.62] Skull.
[245:16.46] That's probably not what we want.
[245:24.22] (dramatic music)
[245:26.98] Let's see what else we have.
[245:34.06] (dramatic music)
[245:37.82] I think zebra's the best one we got.
[245:40.86] Whoops.
[245:43.38] And then let's say for usage.
[245:45.86] (dramatic music)
[245:49.70] Maybe that, I don't know.
[246:00.86] (dramatic music)
[246:05.98] I'm gonna go ahead and, whoops.
[246:08.94] (keyboard clicking)
[246:11.94] Glossary, usage, glossary, TLC.
[246:23.70] (dramatic music)
[246:26.74] I'm just trying to get a feel
[246:32.06] for what this looks like right now
[246:33.42] and what I might be missing still.
[246:35.74] (dramatic music)
[246:38.50] All right, so we've got table of contents,
[246:41.78] usage, API, glossary of terms, fixtures.
[246:45.02] (dramatic music)
[246:47.78] All right, so checksum, compression byte,
[246:53.26] private key, with.
[246:55.74] All right, public key.
[247:03.50] Nope, didn't go nowhere.
[247:06.26] (dramatic music)
[247:09.02] Let's see, where is the public key?
[247:16.30] (dramatic music)
[247:19.06] Okay, that's kind of weird.
[247:28.58] Let me take a look at that again.
[247:30.54] (dramatic music)
[247:33.30] (keyboard clicking)
[247:36.30] Oh, okay, I see what happened there.
[247:43.42] (dramatic music)
[247:46.18] (keyboard clicking)
[247:49.18] All right, let's see.
[248:09.54] So we talked about version, we talked about private key,
[248:12.58] compressed pay address, check, valid.
[248:15.54] Valid is kind of self-explanatory.
[248:17.54] Compression bit, SHA-256, ripe MD-160.
[248:22.06] (dramatic music)
[248:24.82] I think it might be worth mentioning that in the glossary.
[248:34.58] (dramatic music)
[248:44.02] Ripe MD-160, just a short, brief mention.
[248:49.02] (dramatic music)
[248:51.82] An old, deprecated hash algorithm.
[249:07.38] (dramatic music)
[249:12.94] Oh.
[249:13.78] (dramatic music)
[249:16.54] (keyboard clicking)
[249:19.54] (dramatic music)
[249:22.30] (clears throat)
[249:47.98] (dramatic music)
[249:50.74] All right.
[250:17.14] (dramatic music)
[250:19.90] Oh, that looked wrong.
[250:43.02] Hold on.
[250:43.86] (dramatic music)
[250:46.62] (keyboard clicking)
[250:50.02] Oops, I got those mixed.
[250:51.90] That's okay.
[250:53.30] Fixed that.
[250:54.22] Okay, so I think that the only thing that's left
[250:56.82] is the thing that I, interestingly,
[250:59.62] don't really have the brain power for right now.
[251:02.02] And let me, let's see.
[251:05.02] I do want to adjust these as well.
[251:07.94] Address.
[251:10.14] Let's do this.
[251:15.18] So the thing that's left that I'm kind of hesitant on
[251:18.94] is just actually figuring out which of the utilities go,
[251:31.46] how to take those implementation,
[251:42.58] utilities, how to take the utilities.
[251:45.58] Check some, let's see, compressed bytes.
[251:50.58] Okay, private key.
[252:00.62] They just need to be put in and I need a little bit
[252:06.50] of a different type of brain power
[252:07.90] that I don't have right now to be able to finish that.
[252:12.30] Public key.
[252:13.74] Write md160.
[252:17.06] Conversion.
[252:23.98] Zoom on it.
[252:26.74] (upbeat music)
[252:29.32] (keyboard clicking)
[252:32.32] (keyboard clicking)
[252:35.32] (keyboard clicking)
[252:38.32] (keyboard clicking)
[252:41.32] (keyboard clicking)
[252:44.32] Ah.
[253:09.68] (keyboard clicking)
[253:39.04] An HD wallet used for all testing fixtures
[253:44.04] in this eco system of code.
[253:49.00] Also one of the original Trezor and BIP39 test fixtures.
[253:56.16] (keyboard clicking)
[254:07.52] (keyboard clicking)
[254:10.52] All right, I'm gonna do this and then I'm done
[254:22.04] and then we'll publish tomorrow
[254:24.04] once I move those functions around into their proper place.
[254:28.28] (upbeat music)
[254:31.86] (keyboard clicking)
[254:34.86] And then we're pretty much done with dash HD.
[254:43.62] We gotta take HD keys, pull that in, move the CLI out.
[254:49.06] We'll get there.
[254:52.02] (upbeat music)
[254:55.64] (keyboard clicking)
[254:58.64] I kind of want this to be stylized as dash keys.js.
[255:06.64] Let's go ahead and do that.
[255:08.40] (keyboard clicking)
[255:11.40] Oh, and let's go ahead and make sure that this.
[255:21.38] (keyboard clicking)
[255:24.38] (keyboard clicking)
[255:26.70] We got hub.com-hive-keys.js, there we go.
[255:31.70] (keyboard clicking)
[255:36.32] Nice, nice, nice.
[255:45.60] Install.
[255:48.74] Unbundlers.
[255:52.80] (keyboard clicking)
[255:54.54] Glossary.
[255:55.38] Address, let's go back.
[256:01.10] Oops.
[256:01.94] Ah.
[256:04.26] Roof.
[256:13.84] Conversion, I expect all of these are right.
[256:18.16] I'm just double checking.
[256:22.62] (keyboard clicking)
[256:25.62] Oh, whoops.
[256:30.90] Public key, so I should go up here to private key, right?
[256:40.22] All right, private key, I should go back up here
[256:44.38] to compressed byte, and then checksum.
[256:48.08] Okay, great.
[256:49.56] (keyboard clicking)
[256:52.56] All right, this looks good.
[256:55.52] So implementation details is the section
[256:58.96] that needs to be cleaned up.
[257:00.36] And moved inside.
[257:04.26] (keyboard clicking)
[257:10.18] Okay.
[257:17.20] And we're gonna have all that two bytes stuff.
[257:20.26] Interesting.
[257:22.88] Oh, we're not gonna need that anymore, huzzah.
[257:31.02] We're not gonna need that anymore, that's great.
[257:35.16] (keyboard clicking)
[257:44.04] (upbeat music)
[258:12.68] And we're not, we're only dealing with hex and bytes.
[258:14.84] We're not dealing with big Ns,
[258:16.36] so we don't need to qualify num to hex,
[258:20.96] num to whatever, we're good there.
[258:22.68] All right, I'm out for the night.
[258:24.74] Thanks for tuning in.
[258:25.80] I'll try to catch y'all tomorrow,
[258:28.16] and let's see, I actually do need to make a payment tonight.
[258:32.96] I was hoping, I was hoping against hope
[258:36.20] that I would be able to do this differently.
[258:42.72] But I wanted to get further along today.
[258:45.96] Obviously, I wanted to get really further along today.
[258:49.24] Okay, but we are so close on a number of things.
[258:54.26] They're all coalescing.
[258:55.70] All right, but I'm out.
[258:56.96] So catch you later.
[258:58.76] Like, sub, follow if you want to.
[259:00.32] Adios.