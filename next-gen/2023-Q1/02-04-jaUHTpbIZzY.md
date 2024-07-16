---
showLink: "https://www.youtube.com/watch?v=jaUHTpbIZzY"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Code Hangout: Next-Gen DASH Tools #14: More Bike-Shedding about Dash HD Keys..."
publishDate: "2023-02-04"
coverImage: "https://i.ytimg.com/vi/jaUHTpbIZzY/maxresdefault.jpg"
---

## Episode Description

A 6+ hour coding session focused on extensively refactoring and simplifying an HD key derivation library for cryptocurrency wallets.

## Episode Summary

In this marathon coding session lasting over 6 hours, the developer undertakes a major refactoring of an HD (hierarchical deterministic) key derivation library, likely for use in cryptocurrency wallets. The session covers a wide range of tasks, from simplifying core functions to reorganizing the overall structure of the library. Key focus areas include streamlining the derivation process, improving public and private key handling, simplifying serialization methods, and enhancing the overall API design. Throughout the session, the developer frequently runs tests to ensure functionality is maintained while making significant changes. The long duration allows for deep dives into complex cryptographic concepts and careful consideration of design choices. By the end, while substantial progress is made, some final decisions are left for further contemplation after rest, highlighting the complex and iterative nature of refactoring cryptographic code.

## Chapters

00:00 - Introduction and Initial Code Review

The developer begins the extended session by thoroughly reviewing the existing codebase, discussing plans for refactoring, and setting goals for the improvements.

27:38 - Refactoring Set Private Key and Related Functions

A significant portion of time is spent on simplifying the setPrivateKey function and related methods, with careful consideration of security implications.

54:54 - Reworking Derive Child and Derive Path Functions

The developer focuses on improving the crucial deriveChild and derivePath functions, considering various approaches to enhance efficiency and clarity.

1:22:10 - Simplifying Serialization and Deserialization

Extensive work is done on simplifying the serialization and deserialization processes for HD keys, removing unnecessary complexity while ensuring compatibility.

1:49:26 - Revising Public Key Handling

The developer works on improving how public keys are handled and generated within the library, balancing efficiency with security concerns.

2:16:42 - Restructuring Core Library Components

Time is spent on reorganizing the core components of the library, aiming for a more logical and maintainable structure.

2:43:58 - Enhancing Error Handling and Edge Cases

The developer focuses on improving error handling throughout the library and addressing various edge cases in key derivation.

3:11:14 - Optimizing Performance-Critical Sections

Efforts are made to identify and optimize performance-critical sections of the code, particularly in key derivation algorithms.

3:38:30 - Improving API Design and Usability

The developer works on enhancing the overall API design of the library, aiming for a more intuitive and flexible interface for users.

4:05:46 - Implementing Additional Test Cases

Time is dedicated to expanding the test suite, adding more comprehensive test cases to ensure robustness of the refactored code.

4:33:02 - Documentation and Code Cleanup

The developer focuses on improving documentation throughout the codebase and performing general code cleanup.

5:00:18 - Final Refactoring and Comprehensive Testing

The session concludes with final refactoring efforts and extensive testing to ensure all changes work as intended across the entire library.

5:27:34 - Reflection and Future Planning

In the closing segment, the developer reflects on the changes made, discusses potential future improvements, and plans next steps for the library development.

## Transcript

[00:00] Heyo, heyo, heyo, heyo!
[00:20] Heyo, heyo, heyo, heyo, heyo!
[00:47] Heyo, heyo, heyo, heyo, heyo, heyo!
[01:09] Heyo, heyo, heyo, heyo, heyo, heyo, heyo!
[01:33] Heyo, heyo, heyo, heyo, heyo, heyo, heyo, heyo!
[01:57] Heyo, heyo, heyo, heyo, heyo, heyo, heyo, heyo, heyo!
[02:25] Heyo, heyo, heyo, heyo, heyo, heyo, heyo, heyo, heyo!
[02:47] (soft music)
[02:50] (soft music)
[02:52] (soft music)
[02:54] (soft music)
[02:57] (soft music)
[03:00] (soft music)
[03:03] (soft music)
[03:13] (soft music)
[03:29] (soft music)
[03:31] (soft music)
[03:37] (soft music)
[03:56] (soft music)
[03:58] (soft music)
[04:18] (soft music)
[04:20] (soft music)
[04:23] (soft music)
[04:25] (soft music)
[04:28] (soft music)
[04:30] (soft music)
[04:32] (soft music)
[04:55] - Well, hello, hello everybody.
[04:59] Oh, that was perfect timing on the music too.
[05:02] Let's, I'm just doing a quick sound check here.
[05:04] Soundboard's on, good.
[05:05] Mic's on and background music's a go.
[05:09] Okay, 'cause we've had, over the past couple of streams,
[05:11] we've had a little bit of trouble with that.
[05:14] I'm actually gonna finish writing a message here
[05:18] that looks like it pertains to some work that I did
[05:21] that I just saw while I was prepping and everything.
[05:25] So give me a second on that.
[05:27] Let's go ahead and open up our trusty, rusty
[05:31] April Fool's Mountain Dew.
[05:32] It's weird.
[05:36] I mean, okay, so those of you that are soda drinkers,
[05:39] you know this is the difference in how a sugar
[05:43] or syrup can pops versus a diet can.
[05:46] There's just a little bit more of a give to it.
[05:48] It's kind of weird.
[05:49] Anyway, let me see here.
[05:54] ♪ Do, do, do, do, do, do, do, do, do, do, do ♪
[05:59] Let's see.
[06:02] It's about public-private key pairs.
[06:21] It's about the secp256k1 stuff.
[06:23] (dog barking)
[06:26] Okay, I'm gonna, so what we're gonna do,
[06:52] let me tell you what we're gonna do.
[06:54] Okay, now the music's coming back on.
[06:58] Let's see, the music's taking a little bit there.
[07:01] What we're gonna do is we're gonna listen
[07:02] to the dog bark in the background.
[07:03] That's really important to what we're gonna accomplish
[07:06] tonight and, but what, we're just basically,
[07:11] we're bike-shedding over Dash HD.
[07:14] We're trying to figure out what's the right API
[07:16] because I want this, as an ecosystem,
[07:18] I want the naming and usage to be consistent
[07:21] between the different libraries and components.
[07:24] And so before I give the stamp of v1.0,
[07:27] I want all the bike-shedding to be done.
[07:29] Now, I'm mostly bike-shedding with myself,
[07:31] but, you know, I appreciate comments
[07:38] from the peanut gallery.
[07:39] Oh, and we need to take a sip of this.
[07:41] Everybody, we all need to take a sip of this,
[07:45] a sippy of this.
[07:46] Drink the do-aid.
[07:49] (soft piano music)
[07:51] Okay.
[07:56] (soft piano music)
[07:59] Wait, what is?
[08:13] (dog barking)
[08:16] (soft piano music)
[08:19] Oh, this has just got a really slow intro.
[08:22] That's what's going on.
[08:23] All right, fastest JS implementation.
[08:26] So I think,
[08:43] so I need to,
[08:45] I need to update this.
[08:50] I don't know exactly how to update that right now.
[09:04] (soft piano music)
[09:07] Bench, compressed keys, improve math.
[09:16] At least 1.7.1.
[09:25] Were there, do we have any notes on this?
[09:34] I'd be interested to see.
[09:36] Recovery bit.
[09:44] Recovery bit.
[09:45] That's another name for that thing.
[09:49] Let me make sure I get that into this readme.
[09:53] Oops, not this one.
[09:58] One more up.
[09:59] (soft piano music)
[10:02] All right, where are we at right here?
[10:04] Okay.
[10:08] This is the big glossary.
[10:14] What do we have here?
[10:26] (soft piano music)
[10:29] QR.
[10:34] Let's see here.
[10:38] Recovery bit.
[10:41] C.
[10:43] Compression.
[10:47] Compression flag.
[10:52] And I need to add.
[10:55] (soft piano music)
[10:58] All the way up here.
[11:00] Compression flag.
[11:07] Also,
[11:10] compressed byte recovery bit quadrant.
[11:19] Quadrant.
[11:20] Let's see here.
[11:33] And this would be something or other.
[11:37] 0x2, if.
[11:45] (soft piano music)
[11:48] Related to compressed public keys,
[11:57] which only use the x value.
[12:10] Only the x value and the,
[12:15] and this bit are necessary to recover the y value.
[12:22] Okay.
[12:27] Public keys have x and y values, 32 bytes each.
[12:35] I think it was 32 bytes, yeah.
[12:40] It's only necessary to store the x value
[12:49] and a recovery bit.
[12:53] Key.
[13:03] A compressed.
[13:06] Key stores the x value and a recovery bit.
[13:11] Since both possible y values can be recovered.
[13:30] Can be recovered.
[13:31] An x.
[13:38] The recovery bit.
[13:47] Actually, I think I kind of want to call it that.
[13:49] Can tell us which to use.
[13:59] 0x2, if y is even.
[14:04] If y is odd.
[14:16] There we go.
[14:18] And I'll have to put all this stuff together at some point.
[14:27] (soft piano music)
[14:30] I do want to see where he takes this.
[14:41] I am looking forward to the,
[14:46] I think it's the 17 release.
[14:49] (soft piano music)
[14:52] Nice.
[15:07] As of today, fun also.
[15:16] (soft piano music)
[15:20] Supports.
[15:21] As of today, fun.
[15:25] So earlier on the stream,
[15:26] I made this issue on Bun.
[15:31] They fixed it.
[15:32] The dude fixed it.
[15:34] Boom, right then.
[15:36] (soft piano music)
[15:39] (keyboard clicking)
[15:42] Let's see.
[15:49] (keyboard clicking)
[15:53] (keyboard clicking)
[15:57] Hmm.
[15:58] (keyboard clicking)
[16:03] (keyboard clicking)
[16:07] (sighs)
[16:08] (keyboard clicking)
[16:11] (keyboard clicking)
[16:27] (keyboard clicking)
[16:30] (keyboard clicking)
[16:42] (keyboard clicking)
[16:45] All right.
[17:00] (keyboard clicking)
[17:03] Let's see.
[17:10] (sighs)
[17:12] Hmm, interesting.
[17:24] (keyboard clicking)
[17:28] (keyboard clicking)
[17:31] All right, so I was just kind of thinking
[17:58] to myself, it's hard to, I don't,
[18:00] I can't talk in, there's the verbal,
[18:03] I can think the programming stuff,
[18:05] but the verbal communication requires me to be silent.
[18:08] All right, so this we'll have to look at later.
[18:11] This is no bueno from the sense that
[18:14] I need,
[18:18] well,
[18:27] I need to update, at the very least,
[18:30] I'll go update this real quick.
[18:31] Let me, let me do that.
[18:40] I'm gonna update the readme.
[18:41] Let me go up to, let me update the readme.
[18:43] (keyboard clicking)
[18:46] No, that's, what?
[18:56] Oh, whoops.
[18:57] (keyboard clicking)
[19:00] NPM install save-incubator secp, yep.
[19:07] (keyboard clicking)
[19:12] Okay.
[19:24] (keyboard clicking)
[19:28] (keyboard clicking)
[19:31] I'm suspecting this might work.
[19:48] (keyboard clicking)
[19:52] (keyboard clicking)
[20:21] Okay, GJ, boom.
[20:23] (keyboard clicking)
[20:27] (keyboard clicking)
[20:30] (keyboard clicking)
[20:33] (keyboard clicking)
[20:36] (keyboard clicking)
[20:39] (keyboard clicking)
[20:43] (keyboard clicking)
[20:46] (keyboard clicking)
[20:51] (keyboard clicking)
[20:58] (keyboard clicking)
[21:07] (keyboard clicking)
[21:10] Okay.
[21:22] (keyboard clicking)
[21:25] (sighs)
[21:31] (keyboard clicking)
[21:35] pbrand@dashincubator secp256k1.
[21:38] (keyboard clicking)
[21:46] You know what?
[21:58] I do wanna show,
[22:00] let's see.
[22:06] (keyboard clicking)
[22:09] (keyboard clicking)
[22:12] Install, here we go.
[22:37] (keyboard clicking)
[22:41] Node, bun, and bundlers.
[22:44] (keyboard clicking)
[22:48] There we go.
[22:59] Browsers.
[23:02] (keyboard clicking)
[23:05] (keyboard clicking)
[23:08] (keyboard clicking)
[23:30] You spelled CommonJS wrong.
[23:34] I'm pretty sure CommonJS is spelled like that.
[23:37] I don't think CommonJS has a dot in it,
[23:40] but I'm gonna go correct myself.
[23:42] Oops.
[23:44] CommonJS, yes.
[23:46] That's not the correct stylization of CommonJS.
[23:49] (keyboard clicking)
[23:52] (keyboard clicking)
[23:55] Let's see, bar secp256k1.
[24:11] Well, as he has it, it's just secp,
[24:20] but... (keyboard clicking)
[24:23] Because I'm doing this because somebody else was saying
[24:33] that they're gonna try to use it.
[24:34] So I wanted to handle this first and foremost
[24:39] before I get into what I was going to get into,
[24:41] because if I can not block somebody, all the better.
[24:46] Okay.
[24:49] secp, secp256k1, so we're gonna look for b and, oh whoops, and I forgot in, there we go.
[25:02] And then gc, so yes, yes, yes, yes, yes, yes, yes,
[25:19] yes, okay, yes, yes, yes, yes, yes.
[25:27] I kind of want to standardize along what he's doing here, bytes to hex, I think I kind of did
[25:39] that already. That's interesting because I, I saw this, I forgot about it, but I think this is
[25:47] independently what I arrived at, because I had the whole thing about, well, there's un8array,
[25:52] but that's kind of long, and there's buffer, but that kind of means node buffer.
[25:58] So,
[26:08] so,
[26:18] so,
[26:28] so,
[26:38] so,
[26:48] so,
[26:58] so,
[27:08] so,
[27:18] so,
[27:30] so,
[27:40] so,
[27:52] so,
[28:02] so,
[28:14] so,
[28:24] so,
[28:36] so,
[28:46] so,
[29:00] so,
[29:10] so,
[29:24] so,
[29:34] so,
[29:48] so,
[29:58] so,
[30:12] so,
[30:22] so,
[30:36] so,
[30:46] so,
[31:00] so,
[31:10] so,
[31:24] so,
[31:34] so,
[31:48] so,
[31:58] so,
[32:12] so,
[32:22] so,
[32:36] so,
[32:46] so,
[33:00] so,
[33:10] so,
[33:24] so,
[33:34] so,
[33:48] so,
[33:58] so,
[34:12] so,
[34:32] so,
[34:52] so,
[35:02] so,
[35:16] so,
[35:30] so,
[35:40] so,
[35:50] so,
[36:04] so,
[36:14] so,
[36:28] so,
[36:42] so,
[36:52] so,
[37:06] so,
[37:20] so,
[37:40] so,
[38:04] so,
[38:24] so,
[38:34] so,
[38:48] so,
[38:58] so,
[39:08] so,
[39:34] so,
[39:44] so,
[39:54] so,
[40:14] so,
[40:34] so,
[40:44] so,
[40:54] so,
[41:04] so,
[41:14] so,
[41:34] so,
[41:54] so,
[42:04] so,
[42:24] so,
[42:44] so,
[42:54] so,
[43:04] so,
[43:14] so,
[43:24] so,
[43:34] so,
[43:44] so,
[43:54] so,
[44:04] so,
[44:14] so,
[44:24] so,
[44:34] so,
[44:54] so,
[45:14] so,
[45:34] so,
[45:44] so,
[45:54] so,
[46:04] so,
[46:14] so,
[46:24] so,
[46:44] so,
[46:54] so,
[47:04] so,
[47:14] so,
[47:24] so,
[47:34] so,
[47:54] so,
[48:14] so,
[48:34] so,
[48:44] so,
[48:54] so,
[49:04] so,
[49:14] so,
[49:24] so,
[49:34] so,
[49:44] so,
[49:54] so,
[50:04] so,
[50:14] so,
[50:24] so,
[50:34] so,
[50:44] so,
[51:04] so,
[51:14] so,
[51:24] so,
[51:34] so,
[51:44] so,
[51:54] so,
[52:04] so,
[52:14] so,
[52:24] so,
[52:34] so,
[52:54] so,
[53:04] so,
[53:14] so,
[53:24] so,
[53:44] so,
[53:54] so,
[54:04] so,
[54:14] so,
[54:24] so,
[54:34] so,
[54:44] so,
[54:54] so,
[55:04] so,
[55:14] so,
[55:24] so,
[55:34] so,
[55:44] so,
[55:54] so,
[56:04] so,
[56:14] so,
[56:34] so,
[56:44] so,
[56:54] so,
[57:04] so,
[57:14] so,
[57:24] so,
[57:34] so,
[57:44] so,
[57:54] so,
[58:04] so,
[58:14] so,
[58:24] so,
[58:34] so,
[58:44] so,
[58:54] so,
[59:04] so,
[59:14] so,
[59:24] so,
[59:34] so,
[59:44] so,
[60:04] so,
[60:14] so,
[60:24] so,
[60:34] so,
[60:44] so,
[60:56] so,
[61:16] so,
[61:26] so,
[61:36] so,
[61:48] so,
[62:00] so,
[62:02] so,
[62:04] so,
[62:06] so,
[62:08] so,
[62:10] so,
[62:12] so,
[62:22] so,
[62:42] so,
[63:10] so,
[63:12] so,
[63:14] so,
[63:16] so,
[63:18] so,
[63:20] so,
[63:22] so,
[63:24] so,
[63:34] so,
[63:36] so,
[63:38] so,
[63:40] so,
[63:42] so,
[63:44] so,
[63:46] so,
[63:48] so,
[63:50] so,
[63:52] so,
[63:54] so,
[63:56] so,
[63:58] so,
[64:08] so,
[64:10] so,
[64:20] so,
[64:30] so,
[64:32] so,
[64:34] so,
[64:36] so,
[64:38] so,
[64:40] so,
[64:42] so,
[64:52] so,
[64:54] so,
[64:56] so,
[64:58] so,
[65:00] so,
[65:02] so,
[65:04] sense for what this is in particular because if you change the public key you
[65:11] know okay let's just go through here again so utils pubkey normalize that
[65:16] makes sense utils pubkey tweak add that makes sense those are for creating
[65:21] extended keys okay I don't think I'm gonna it could be wrong so this one
[65:34] and take a copy of the public key okay here we set the public key so I'm I'm
[65:42] saying I think this method should just not be exposed or not separate yeah I
[65:46] don't think set priv key or set pubkey should be publicly exposed I think that
[65:51] they probably should just be private so here we have public key we set the
[66:01] public key what do we do with it we set it we set it we get it in code X pub
[66:10] and I I don't think that this is really a use case because if we're going to
[66:25] create an X pub we're going to want to create an X pub from something that we
[66:32] already know so I guess the argument could be made I want to take an
[66:38] arbitrary public key and I want to create an extended public key from this
[66:44] arbitrary public key I don't see the use case for that because the purpose of the
[66:51] extended public key is that it's recoverable and so I don't I don't
[66:56] understand the use case where you would want that why would you want to make a
[67:07] specific key recoverable rather than a phrase because if you make the phrase
[67:15] it's you have to you know you print it somewhere you store it in a file
[67:19] somewhere you do something with it I can't think of the reason that you would
[67:24] want to set a public key to do this in code X pub and if you did then I would
[67:34] say that you dig down into the utils and you use in code X pub and that's that's
[67:40] what you do so I'm going to take a look at the serialize method here okay so
[67:56] this is the only function that actually uses it derive child so would we want to
[68:02] derive a child from a public key that we set ourselves I don't see the use case
[68:10] for it and I think that providing more API surface area that you don't need is
[68:16] just not helpful so I'm actually going to say we're going to ditch the idea of
[68:30] a git pub key well we might not ditch we're gonna ditch the idea of a public
[68:36] set of the setting the private key or setting the public key it seems to be
[68:42] useful for debugging but it does not seem to be useful for the use case that
[68:48] I imagine these things to be used for so we're gonna change set priv key to set
[68:57] private key
[69:01] there's only a handful of places that's being done likewise set pub key whoops
[69:18] is going to become well first we have to deal with
[69:26] set pub key needs to become set pub public key unchecked
[69:51] and then set pub key simply becomes set public key but this becomes internals
[69:57] that we don't document or expose there's this one HD over here what is this about
[70:07] how do we do this in the other one do we just call it HD key yeah
[70:18] and what is this from derived child
[70:24] [Music]
[70:51] okay I'm a little bit confused about this one because there's another one
[70:56] where we do something similar to this
[70:59] so here we're actively using both okay I'm gonna hang on to that one for a
[71:10] second set
[71:15] [Music]
[71:18] oops
[71:23] [Music]
[71:26] I think this pub key to ID is going to go
[71:56] to utils
[71:59] um I'm interested to see this message so I cut I I paid for an app that was not
[72:13] cheap it's a yearly subscription and I hate doing really subscriptions but in
[72:17] this particular case I think that it may make sense and I want the app to get
[72:21] better so I'm happy to pay for it to get better anyway so I I paid for the
[72:29] subscription the premium account and then they and then I submitted a bug
[72:35] because now I've got the premium one and I'm expecting that my my my you might
[72:41] that I'm going to get the support that they promise with a you know a premium
[72:46] version of the app premium account and I send them a screenshot saying hey this
[72:54] is obviously broken and then they and then I send another screenshot about a
[72:58] different issue saying hey this is obviously broken and then both times
[73:01] they sent me back a message that said it's just a generic bot message I'm
[73:06] sorry I know it can be frustrating to not be able to use the app have you
[73:10] tried turning it on and off again and visit have you tried logging in from the
[73:15] website I'm not on desktop I'm on the flippin mobile phone you know and and
[73:21] then and then I responded to the message
[73:36] just did you read the message are you a human or a bot anyway so I'm just
[73:55] getting these generic messages back and that's not what I expect with premium
[73:58] support I don't expect to pay for premium support to get access to a bot
[74:03] that asks me have you tried turning it on and off again you know that's what
[74:08] that's the free support the free support is the bot that tells you have you tried
[74:13] turning it on and off again the premium support should be someone who reads the
[74:18] message that's so yeah I got back another message from the bot I literally
[74:26] just got the phone installed the app a couple of days ago and the bot is
[74:33] telling me have you tried upgrading to the latest version of our app but let's
[74:41] see maybe they did release one I'm gonna check and see if they actually did okay
[74:46] they did they did actually just release an update within the last couple days
[74:52] so okay I will I will let it update and I will put aside my frustrations for the
[75:03] moment okay so we're gonna bring this into the utils
[75:07] utils.pubkey2id I'm just gonna bring this on up where are my utils at
[75:31] and I don't know if this actually belongs on utils but I'm gonna put it
[75:42] there for now I like things being exposed I like them being able to be
[75:51] used all right I will I will try opening up this app and see if yeah this is same
[76:11] problem hold on I'm gonna I'm gonna try to make a recording here just one second
[76:17] sorry okay so I just updated the app all of the problems are the same as you can
[76:25] see in the middle here there's a space that looks like it's supposed to be a
[76:28] button this gray area in the middle of the screen if I tap on link nothing
[76:33] happens I can't scroll left or right I can't scroll up or down can't scroll
[76:39] left or right on the menu down at the bottom if I go to import I'm assuming
[76:44] that that's what's supposed to happen if I click on the link button here but I
[76:48] can go to import thankfully which on my other phone I can't get to import
[76:52] because it literally is off the screen and there's no way to scroll through the
[76:56] items and then I'll have to check on some of that other stuff like the the
[77:02] voices and whatnot but no this is not this is not fixed this does not help me
[77:08] maybe the voices are fixed but this is in general this did not solve my problem
[77:13] I still I cannot access things I can't click on things this is fundamentally
[77:18] broken in it in it in a in a broken way okay I will send that later
[77:26] bah okay so where are we at here yeah I've got the oh yeah I was saying I when
[77:39] when reasonable I like to have things
[78:00] something or other I like to have something or other so good get
[78:06] fingerprint so again get fingerprint I think is another one of those things is
[78:09] probably should just be a util get fingerprint is this an ID
[78:22] hmm read okay
[78:32] I don't know if this like I I don't know what of this should be public should the
[78:45] identifier be public I don't know
[78:50] all right let me go back to the top here let's do - HD from the top whoops
[79:01] - HD I've got a create function I've got a this I think is supposed to be on the
[79:14] inside yeah I think all of this is supposed to move on the inside
[79:28] I just I wish there was a better word than set
[79:38] [music]
[79:59] setting seed makes sense
[80:01] setting the
[80:03] uh
[80:05] extended private key
[80:07] or extended public key makes sense
[80:09] setting the public key and private key
[80:11] do not make sense to me
[80:13] I don't see where that would be useful
[80:15] alright
[80:17] set
[80:19] and I do want to understand this
[80:25] HD, so this is derived
[80:27] child
[80:29] [music]
[80:56] [music]
[80:58] [music]
[81:07] [music]
[81:32] hmm
[81:34] seems a little bit weird but I can't explain why
[81:37] what is wrong about this
[81:39] [music]
[81:53] I know what's wrong about this
[81:55] this is at the wrong level
[81:57] so this should be
[81:59] -h
[82:01] hd.derive
[82:03] I'm going to experiment with this
[82:05] and see if I'm correct
[82:07] and then it should take
[82:11] hdkey
[82:13] and path
[82:15] [music]
[82:21] hold on wait wait wait
[82:23] let me get back to that
[82:25] [music]
[82:41] it needs, or maybe it could be
[82:43] utils.derive
[82:45] but there needs to be some
[82:47] sort of
[82:49] [music]
[83:08] there needs to be some sort of separation
[83:10] where
[83:12] you are making
[83:14] a copy
[83:16] [music]
[83:45] [music]
[84:04] I think something like that
[84:06] it could be utils.derive
[84:08] I don't know, but it just seems
[84:10] because it's kind of confusing
[84:12] to have, this right here
[84:14] is what's confusing to me
[84:16] [music]
[84:42] so if the
[84:44] path is just
[84:46] m
[84:48] then just return it
[84:50] [music]
[84:54] that seems kind of weird, but
[84:56] that doesn't
[84:58] seem like a valid path
[85:00] but we could, I guess
[85:02] we could go with that
[85:04] [music]
[85:12] I'm not really sure how to take that
[85:14] okay, but
[85:16] [music]
[85:18] okay, we do that
[85:20] [music]
[85:48] [music]
[85:57] I just don't like that
[85:59] reassignment of self
[86:01] that's what feels wrong
[86:03] was the reassignment of self
[86:05] because hdkey is the self
[86:07] and if we're going to reassign it
[86:09] it just, it's weird
[86:11] [music]
[86:15] so this could go in utils
[86:17] I think that's fine
[86:19] in fact, I think maybe that's where I will put it
[86:21] [music]
[86:23] for lack of a
[86:25] better place right now
[86:27] [music]
[86:35] and we'll see
[86:37] we'll just kind of experiment and see how it feels
[86:39] [music]
[87:05] [music]
[87:15] okay, then we have derived child
[87:17] so what's going on here
[87:19] because I think
[87:21] there's some similar stuff in here that just
[87:23] doesn't feel like it's the right place
[87:25] [music]
[87:29] this has got all sorts of
[87:31] comments in here and
[87:33] crazy this and that
[87:35] [music]
[87:50] okay, so derive
[87:52] does
[87:54] call this
[87:56] [music]
[88:01] in a way recursively
[88:03] it's not actually recursive
[88:05] [music]
[88:07] but it kind of has
[88:09] a recursive feel to it, you're calling
[88:11] a function in a loop
[88:13] that returns a result
[88:15] and you call that same function on
[88:17] that result
[88:19] [music]
[88:27] another thing that would be interesting
[88:29] would be
[88:31] [music]
[88:34] to ditch the functions
[88:36] and try more
[88:38] of a
[88:40] [music]
[88:43] or ditch the methods, sorry
[88:45] ditch the methods and try more of a functional
[88:47] approach, which is what I typically try to do
[88:49] the thing with this is that there is a lot of state
[88:51] in it
[88:53] and that state needs
[88:55] to be accessed, so the reason
[88:57] basically the reason that you have
[88:59] classes
[89:01] is if you need to hide
[89:03] information, things
[89:05] that you don't want to serialize
[89:07] so there's a lot of
[89:09] buffers and things that wouldn't go
[89:11] to JSON
[89:13] and that is where this is a
[89:15] poor candidate
[89:17] it's a good candidate for
[89:19] the class approach because there's a lot of stuff
[89:21] that we want to hide, if we
[89:23] wanted to serialize something, the bits
[89:25] we want to serialize
[89:27] are the things that are
[89:29] either hex
[89:31] or
[89:33] base 58
[89:35] encoded, but we don't really want to serialize
[89:37] the
[89:39] the whole
[89:41] of the state of this because
[89:43] it's kind of got a machine to it
[89:45] this is, in a lot of ways
[89:47] actually in a lot of ways
[89:49] this is very
[89:51] much like a hash algorithm
[89:53] a hash algorithm is more
[89:55] of a state
[89:57] table that you're
[89:59] kind of cranking on
[90:01] cyclomatically
[90:03] you're trying, you're creating
[90:05] iterations and that's exactly
[90:07] what this is, this is
[90:09] well it is a key derivation
[90:11] I think the way that we need to think
[90:13] about this would be the
[90:15] same way that we model
[90:17] with PBKDF2
[90:19] in fact I think that that's exactly
[90:21] the right way to do it because look at it
[90:23] derive, you give it
[90:25] the key that you
[90:27] want to derive from
[90:29] and then you give it the path
[90:31] so this is very much similar
[90:33] to the
[90:35] the salt and secret
[90:37] that you get with PBKDF2
[90:39] or with an HMAC
[90:41] this has that kind of feel
[90:43] to it, so I think
[90:45] that the ergonomics of this actually
[90:47] ought to very
[90:49] very very closely mirror
[90:51] a hash
[90:55] function because that's
[90:57] what this is, you're calling update and update
[90:59] and update and update and that's exactly what this
[91:01] is right here, we're producing
[91:03] a hash and then we're doing rounds
[91:05] so this is
[91:07] kind of a rounds function
[91:09] this derive
[91:11] and you are providing
[91:13] different salt to each of
[91:15] the rounds, so you're basically
[91:17] providing a path of salt
[91:19] is what you're doing
[91:21] so this is
[91:23] for somebody that's familiar with cryptography
[91:25] outside of
[91:27] the cryptocurrency space
[91:29] HD keys
[91:31] are PBKDF2 on steroids
[91:33] that's what they are
[91:35] they're PBKDF2
[91:37] hmm
[91:39] that actually is really helpful
[91:41] in thinking about the design of this thing
[91:43] okay
[91:45] so with that approach
[91:47] let's see
[91:49] let me
[91:53] I'm just going to, again
[91:55] I'm kind of experimenting, some of this might go back
[91:57] I might throw it away, but I'm trying to discover
[91:59] what is the right approach
[92:01] so let's think of this as a
[92:03] hashing function
[92:05] so I'm going to create my hashing function
[92:07] and then let's think of
[92:11] let's think of the
[92:13] um
[92:15] so this is
[92:25] this is basically get
[92:29] private digest
[92:31] XPRIV
[92:37] digest
[92:39] ooh
[92:41] ooh
[92:43] I actually like that
[92:45] and it solves the weird
[92:47] double
[92:49] problem here
[92:51] so xpub digest
[92:53] hmm
[93:01] what do we call it
[93:03] hmm
[93:05] that makes a lot of sense now
[93:27] so
[93:29] so almost universally
[93:41] I think our hashing functions
[93:43] have
[93:45] update
[93:47] subtle digest
[93:49] hmm
[93:51] hmm
[94:07] so maybe not so much
[94:17] derive child
[94:19] as just update
[94:21] what would that look like
[94:25] okay
[94:45] hmm
[94:47] hmm
[95:15] hmm
[95:17] so what happens in derive child here
[95:37] set
[95:43] child, so this kind of
[95:45] looks the same, what else is this
[95:47] ibuff code
[95:49] il=
[96:01] is also in set seed
[96:03] so how is this different from
[96:05] set seed, are we setting a chain here
[96:11] okay so what happens
[96:13] this bit here in the middle
[96:15] this is important somehow
[96:17] this is the key distinction between
[96:33] setting a seed and deriving
[96:35] because if we look at this
[96:37] hmm
[96:39] we have to
[96:57] have the private key
[96:59] if we're going to
[97:01] harden something
[97:03] hmm
[97:05] okay
[97:23] my brain
[97:25] buds are tickling but I don't know what they're saying
[97:27] but they're telling me something kind of important
[97:31] hmm
[97:33] okay so it's set
[97:43] here
[97:45] alright and the word
[97:51] that we want is not set
[97:53] xpriv
[97:55] it is recover
[97:57] hmm
[97:59] or maybe even resume
[98:25] because what we're
[98:27] doing is, so what the xpriv
[98:29] is, it's part of a state machine
[98:31] it's part of a state machine just like a hash
[98:33] just like pbkdf2
[98:35] but what you're saying is at any
[98:37] number of rounds in the hash
[98:39] I can export
[98:41] the state of the hash
[98:43] and then if I want to resume that hash
[98:45] I can re-import
[98:47] the state of the hash and then resume
[98:49] the hash, that's what's happening here
[98:51] this makes
[98:53] so much more sense now
[98:55] I mean
[98:57] I understood it before but now
[98:59] I'm getting that this is
[99:01] a key expansion algorithm that's
[99:03] resumable
[99:05] that's really neat
[99:09] I don't know if the right word is recover
[99:19] or resume but
[99:21] I don't know
[99:23] probably one of those
[99:29] but what I'm a little confused about
[99:39] there's some stuff here that seems like
[99:41] and you know
[99:43] there's all the time
[99:45] you hear me say, a little copying
[99:47] is better than a little dependency
[99:49] I believe it, 100%
[99:51] there's just
[99:53] some stuff here that seems like
[99:55] it should go together
[99:59] so depth
[100:01.14] parent fingerprint index
[100:03.14] depth parent fingerprint index
[100:05.14] is a
[100:07.14] non-alphabetized
[100:09.14] normally
[100:15.14] I
[100:17.14] alphabetize
[100:19.14] these
[100:23.14] sorts of things
[100:25.14] in byte order
[100:29.14] setting
[100:31.14] in byte order
[100:33.14] for consistency
[100:35.14] [typing]
[100:51.14] so first is depth
[100:53.14] then fingerprint
[100:55.14] then index
[100:57.14] then chain code
[100:59.14] because that's the way the bytes are stored
[101:01.14] [typing]
[101:07.14] okay
[101:09.14] so again
[101:11.14] [typing]
[101:15.14] depth
[101:17.14] fingerprint
[101:19.14] [typing]
[101:25.14] and where is identifier stored then
[101:27.14] when does that come into play
[101:29.14] [typing]
[101:31.14] set that when we set the private key
[101:33.14] or we set the public key
[101:35.14] when is it used
[101:37.14] is it not used
[101:39.14] I think it is used
[101:41.14] because I think it's used for the fingerprint
[101:43.14] which is part of export data
[101:45.14] [typing]
[101:59.14] okay
[102:01.14] so here's the fingerprint
[102:03.14] [typing]
[102:05.14] identifier
[102:07.14] [typing]
[102:35.14] [typing]
[102:39.14] okay now I'm thinking about this a little bit differently
[102:41.14] [typing]
[103:09.14] [typing]
[103:13.14] hmmm
[103:15.14] [typing]
[103:35.14] [typing]
[103:53.14] alright
[103:55.14] [typing]
[104:23.14] [typing]
[104:27.14] so is this just a bunch of intermediary state stuff
[104:31.14] [typing]
[104:41.14] alright
[104:43.14] all of this may get deleted
[104:45.14] I may completely undo everything that I'm doing here
[104:47.14] but I'm just going to dive a little bit deeper in this
[104:49.14] because I think
[104:51.14] there's something unique to discover here
[104:53.14] I just don't know what it is
[104:55.14] I understand
[104:57.14] the components of the code
[104:59.14] I don't quite
[105:01.14] understand it
[105:03.14] holistically
[105:05.14] but I think
[105:07.14] there is something here
[105:09.14] that could lead to a very
[105:11.14] very nice
[105:13.14] and small API
[105:15.14] so
[105:17.14] let me try
[105:19.14] okay
[105:21.14] first of all what we're going to do here
[105:23.14] so private key copy
[105:25.14] private key
[105:27.14] copy, let me go ahead
[105:29.14] I'm just going to save and open this back up
[105:31.14] so all my history is erased
[105:33.14] alright
[105:35.14] next
[105:37.14] priv key
[105:39.14] [typing]
[105:49.14] okay
[105:51.14] set the private key
[105:53.14] set private key
[105:55.14] what is this really doing
[105:57.14] [typing]
[106:02.14] is this just doing a calculation
[106:04.14] [typing]
[106:18.14] alright so it's updating some internal state
[106:20.14] [typing]
[106:32.14] it's updating the public key and the identifier
[106:34.14] might as well update the fingerprint at that time
[106:36.14] the fingerprint is very simple
[106:38.14] [typing]
[106:40.14] I guess we don't need the fingerprint yet
[106:42.14] [typing]
[106:58.14] set seed
[107:00.14] [typing]
[107:20.14] so there's one
[107:22.14] two
[107:24.14] three places
[107:26.14] where you set the private key
[107:28.14] [typing]
[107:34.14] but because
[107:36.14] this, I can only imagine
[107:38.14] this being internal
[107:40.14] not external
[107:42.14] we don't really need to check
[107:44.14] those byte values
[107:46.14] [typing]
[107:52.14] so let's see
[107:54.14] see what this looks like if we actually just get rid
[107:56.14] of set private key
[107:58.14] and instead we say
[108:00.14] [typing]
[108:04.14] [typing]
[108:32.14] [typing]
[108:36.14] let's go back
[108:38.14] [typing]
[108:56.14] [typing]
[109:22.14] ok so we get rid of that
[109:24.14] [typing]
[109:30.14] I don't think we actually need to do the identifier
[109:32.14] until we need to get the fingerprint either
[109:34.14] [typing]
[109:36.14] so we might be able to reduce this
[109:38.14] quite a bit
[109:40.14] [typing]
[109:52.14] back on paper mario again?
[109:54.14] we are. alright I'm going to switch it up to
[109:56.14] classical
[109:58.14] or maybe
[110:00.14] folk. let's try some folk
[110:02.14] [typing]
[110:10.14] what does that even mean?
[110:12.14] [typing]
[110:28.14] [typing]
[110:52.14] ok
[110:54.14] alright now the person
[110:56.14] well they got a
[110:58.14] if the person
[111:00.14] was just hitting the bot buttons
[111:02.14] without reading my message
[111:04.14] the auto responder buttons
[111:06.14] then the person is now taking
[111:08.14] control and if it's a bot
[111:10.14] then I got past the bot
[111:12.14] to a person so I'll have to
[111:14.14] read that and respond accordingly later
[111:16.14] [typing]
[111:44.14] [typing]
[111:54.14] ok
[111:56.14] [typing]
[112:04.14] so we can just get rid of
[112:06.14] set private key in this
[112:08.14] form
[112:10.14] and set private key just becomes
[112:12.14] private key
[112:14.14] equals value
[112:16.14] so private key just becomes
[112:18.14] [typing]
[112:24.14] we could do one better
[112:26.14] [typing]
[112:28.14] set private key
[112:30.14] [typing]
[112:38.14] we could just encapsulate
[112:40.14] hdkey dot
[112:42.14] get
[112:44.14] get private key
[112:46.14] [typing]
[112:52.14] that's now
[112:54.14] um
[112:56.14] [typing]
[113:06.14] alright we don't need this anymore
[113:08.14] [typing]
[113:12.14] we can take that, we can just move this out
[113:14.14] [typing]
[113:28.14] ok
[113:30.14] [typing]
[113:36.14] alright what is this inside of
[113:38.14] this just has an
[113:40.14] index
[113:42.14] [typing]
[114:02.14] [typing]
[114:14.14] ok
[114:16.14] I have to think through this one as well
[114:18.14] [typing]
[114:30.14] alright how many places is set public key
[114:32.14] actually used
[114:34.14] [typing]
[114:36.14] here is one place where
[114:38.14] set public key is used
[114:40.14] there are two places, there are two places
[114:42.14] where set public key is used
[114:44.14] do they reduce down further
[114:46.14] [typing]
[115:04.14] again
[115:06.14] I don't actually think we need the checking
[115:08.14] on this because this
[115:10.14] doesn't need to be
[115:12.14] [typing]
[115:18.14] ok this is
[115:20.14] where the tweak
[115:22.14] so the
[115:24.14] ok so with a
[115:26.14] hardened key we're tweaking the
[115:28.14] private key the whole way down
[115:30.14] is that what I'm understanding
[115:32.14] [typing]
[115:38.14] I'm trying to get a
[115:40.14] feel for this
[115:42.14] [typing]
[115:54.14] function do a thing
[115:56.14] here is my do a thing
[115:58.14] function let's see if we can copy
[116:00.14] [typing]
[116:06.14] all of this into it
[116:08.14] [typing]
[116:32.14] so this is actually
[116:34.14] called
[116:36.14] private parent
[116:38.14] to private
[116:40.14] [typing]
[117:08.14] [typing]
[117:14.14] ok so what is this
[117:16.14] value, where does
[117:18.14] value come from here
[117:20.14] [typing]
[117:32.14] [typing]
[117:54.14] [typing]
[118:22.14] ok I think
[118:24.14] this is going to work
[118:26.14] [typing]
[118:38.14] ok so where did
[118:40.14] IL come from
[118:42.14] [typing]
[118:44.14] IL
[118:46.14] comes from I
[118:48.14] where does I come from
[118:50.14] ok it comes from the chain code
[118:52.14] so this
[118:54.14] is
[118:56.14] and then index comes from up here
[118:58.14] so at the highest level
[119:00.14] it's an HD key and then
[119:02.14] it's an index and then it's an IL
[119:04.14] [typing]
[119:08.14] ok
[119:10.14] so let's just try this out
[119:12.14] [typing]
[119:18.14] it doesn't need to return anything
[119:20.14] it might
[119:22.14] [typing]
[119:30.14] ok so it's going to try to do this
[119:32.14] [typing]
[120:00.14] [typing]
[120:16.14] alright
[120:18.14] [typing]
[120:34.14] this worries me a little bit
[120:36.14] this makes it seem like
[120:38.14] the index is not
[120:40.14] [typing]
[120:42.14] guaranteed
[120:44.14] [typing]
[120:48.14] so it's possible
[120:50.14] [typing]
[120:54.14] that two
[120:56.14] [typing]
[120:58.14] iterations
[121:00.14] two indexes could produce the same
[121:02.14] key
[121:04.14] so I think that's
[121:06.14] maybe that's part of the fingerprint that we need
[121:08.14] [typing]
[121:28.14] [typing]
[121:54.14] ok
[121:56.14] what is it that can
[121:58.14] throw out of all this
[122:00.14] [typing]
[122:02.14] because I think if we could be more
[122:04.14] specific, this is one of the things that is
[122:06.14] you know when I say it's
[122:08.14] a terrible code smell
[122:10.14] [typing]
[122:14.14] to use
[122:16.14] try catch
[122:18.14] [typing]
[122:26.14] let me back this up a little bit
[122:28.14] now that I understand
[122:30.14] it better
[122:32.14] back that up a lot
[122:34.14] [typing]
[122:44.14] ok
[122:46.14] [typing]
[122:48.14] value here, this is basically
[122:50.14] [typing]
[122:54.14] next probe key
[122:56.14] [typing]
[122:58.14] so this whole thing
[123:00.14] is in this try catch block right
[123:02.14] but what about it could
[123:04.14] be, what about
[123:06.14] it could go wrong
[123:08.14] so for example
[123:10.14] allocating the memory
[123:12.14] is not going to be something that we need
[123:14.14] to try catch
[123:16.14] [typing]
[123:18.14] what about this
[123:20.14] tweak
[123:22.14] normalize
[123:24.14] private key, that could fail
[123:26.14] [typing]
[123:34.14] ok, big int
[123:36.14] [typing]
[123:38.14] so this could fail
[123:40.14] right here
[123:42.14] [typing]
[123:44.14] could set private key fail, no
[123:46.14] [typing]
[124:00.14] could
[124:02.14] to public key fail
[124:04.14] I suppose it could
[124:06.14] for the same reason
[124:08.14] it's got to be normalized
[124:10.14] ok so that
[124:12.14] could fail
[124:14.14] [typing]
[124:16.14] and then
[124:18.14] [typing]
[124:20.14] pub key to id
[124:22.14] [typing]
[124:24.14] that can't
[124:26.14] fail
[124:28.14] [typing]
[124:30.14] furthermore
[124:32.14] [typing]
[124:34.14] yeah that's
[124:36.14] going to be the same here
[124:38.14] so set
[124:40.14] public key
[124:42.14] [typing]
[124:54.14] so normalize
[124:56.14] [typing]
[124:58.14] set unchecked
[125:00.14] so pub key
[125:02.14] [typing]
[125:04.14] to id
[125:06.14] [typing]
[125:08.14] fingerprint
[125:10.14] I'm pretty sure the only place this is used
[125:12.14] is in git fingerprint
[125:14.14] [typing]
[125:42.14] [typing]
[126:00.14] alright
[126:02.14] [typing]
[126:04.14] pub key to id
[126:06.14] [typing]
[126:08.14] [typing]
[126:22.14] there's only one place to get fingerprints used
[126:24.14] [typing]
[126:36.14] since there's only one place
[126:38.14] this is used
[126:40.14] and since this is only going to be used
[126:42.14] internally
[126:44.14] we don't really need to
[126:46.14] normalize the key, the key should be normalized
[126:48.14] before we get it
[126:50.14] let's see
[126:52.14] don't
[126:54.14] I mean aren't we the ones that decide
[126:56.14] yeah we don't
[126:58.14] need to normalize the key because it is
[127:00.14] yeah
[127:02.14] the only thing
[127:04.14] so if we
[127:06.14] set the public key then we
[127:08.14] unset the private key
[127:10.14] why would we do that
[127:12.14] and then we're not wiping
[127:14.14] this either
[127:16.14] we're just unsetting it, that seems kind of weird
[127:18.14] [typing]
[127:28.14] I'm trying to think about this
[127:30.14] so for
[127:32.14] so for
[127:34.14] [typing]
[127:36.14] hmm
[127:38.14] [typing]
[127:40.14] this is a tough one
[127:42.14] here trying to
[127:44.14] trying to kind of grok all this
[127:46.14] [typing]
[127:54.14] but you know for a minute let's just get rid of all the
[127:56.14] ceremony
[127:58.14] well let me check again where do we have
[128:00.14] set public key
[128:02.14] [typing]
[128:06.14] we do, we set a public
[128:08.14] key
[128:10.14] [typing]
[128:12.14] when we derive a child
[128:14.14] [typing]
[128:19.14] okay
[128:21.14] that is
[128:23.14] our own function
[128:25.14] public key tweak add
[128:27.14] so that's our own function
[128:29.14] [typing]
[128:31.14] so, and then what about
[128:33.14] this one here
[128:35.14] where is this happening
[128:37.14] set extended key
[128:39.14] I could see why
[128:41.14] we'd want to check
[128:43.14] that one
[128:45.14] [typing]
[129:14.14] [typing]
[129:25.14] alright set public key
[129:27.14] we just want to
[129:29.14] normalize
[129:31.14] [typing]
[129:48.14] I don't know why we would need to
[129:50.14] normalize this
[129:52.14] it seems like if we just check the bytes
[129:54.14] that should be good enough
[129:56.14] [typing]
[129:59.14] okay let's go ahead and normalize it
[130:01.14] [typing]
[130:03.14] alright
[130:05.14] [typing]
[130:15.14] so now let's
[130:17.14] set public key unchecked
[130:19.14] [typing]
[130:48.14] [typing]
[130:55.14] alright
[130:57.14] [typing]
[130:59.14] we don't need that overhead there
[131:01.14] [typing]
[131:27.14] that makes a lot more sense right here
[131:29.14] [typing]
[131:34.14] [typing]
[132:02.14] [typing]
[132:27.14] okay
[132:29.14] [typing]
[132:42.14] [typing]
[133:11.14] [typing]
[133:19.14] okay
[133:21.14] so we basically
[133:23.14] [typing]
[133:25.14] eliminate the need
[133:27.14] [typing]
[133:29.14] so public
[133:31.14] key
[133:33.14] normalize
[133:35.14] [typing]
[133:42.14] in one place we need that
[133:44.14] [typing]
[133:46.14] and then
[133:48.14] [typing]
[133:50.14] set public key just
[133:52.14] goes away
[133:54.14] [typing]
[134:01.14] alright
[134:03.14] that was nice
[134:05.14] [typing]
[134:10.14] set private key pretty much goes away
[134:12.14] [typing]
[134:41.14] [typing]
[135:04.14] okay
[135:06.14] fhdk.improvekey
[135:11.14] [typing]
[135:30.14] so what I'm doing is I'm checking to see
[135:32.14] if we can actually get this to just be
[135:35.14] basically an object
[135:37.14] an object that's mostly public values
[135:39.14] [typing]
[135:41.14] and then just have
[135:43.14] kind of a hash function so basically
[135:45.14] hdkey is the state of the hash
[135:47.14] and then
[135:49.14] we just pass that hash state
[135:51.14] into
[135:53.14] an update/derive function
[135:55.14] and then a digest function
[135:57.14] [typing]
[136:26.14] [typing]
[136:53.14] [typing]
[137:22.14] [typing]
[137:34.14] okay
[137:36.14] [typing]
[137:40.14] we don't need a set private key function
[137:43.14] [typing]
[138:01.14] let's see, as long as this is
[138:04.14] does this have scope?
[138:07.14] yes it does, so
[138:10.14] we are free
[138:13.14] to assign in that way
[138:16.14] now we don't need a set private key
[138:18.14] and we don't need
[138:20.14] [typing]
[138:32.14] let's see
[138:34.14] [typing]
[139:01.14] so hardened child
[139:04.14] [typing]
[139:32.14] [typing]
[140:01.14] [typing]
[140:08.14] okay
[140:10.14] [typing]
[140:39.14] [typing]
[140:42.14] let's see here
[140:44.14] [typing]
[141:12.14] [typing]
[141:15.14] where did value go?
[141:18.14] here
[141:20.14] [typing]
[141:22.14] oh this was
[141:25.14] oh right
[141:27.14] because before it was just called value
[141:30.14] [typing]
[141:36.14] okay
[141:38.14] [typing]
[141:40.14] alright, so
[141:43.14] [typing]
[142:11.14] okay, so the reason I don't like this
[142:13.14] drive child, it's kind of the same reason
[142:15.14] so here we have something
[142:17.14] that's creating a new state
[142:20.14] and I just kind of want to see
[142:23.14] [typing]
[142:25.14] hdkey
[142:27.14] the problem with this one
[142:30.14] [typing]
[142:35.14] is that
[142:37.14] [typing]
[142:42.14] we back up and try again
[142:44.14] if there's a problem
[142:46.14] the way that we back up and try again
[142:48.14] is what the problem is
[142:52.14] [typing]
[142:57.14] because basically the whole thing
[143:00.14] in this case, I think the whole thing
[143:02.14] should just be wrapped in a try catch
[143:04.14] and that try catch handling should happen there
[143:07.14] so I'm going to try making this
[143:09.14] something higher level and lower level
[143:11.14] so we'll have a helper function here
[143:15.14] so we have a drive child
[143:19.14] hdkey
[143:21.14] so let's say
[143:23.14] get the private key
[143:26.14] [typing]
[143:33.14] get the public key
[143:35.14] [typing]
[143:45.14] okay, what else?
[143:47.14] [typing]
[143:50.14] we get the chain code
[143:52.14] [typing]
[144:21.14] we get the versions
[144:23.14] [typing]
[144:28.14] kind of trying to see what we're working with
[144:30.14] [typing]
[144:48.14] I think I'll put this in a wit branch and probably
[144:50.14] just stuff it away for later exploration
[144:53.14] [typing]
[144:56.14] okay, but, okay, so
[144:58.14] we get the versions and then what?
[145:00.14] [typing]
[145:02.14] where does the hd happen?
[145:04.14] so this is where the hd happens, and then
[145:06.14] what then?
[145:07.14] after that, hdkey, so
[145:09.14] drive child
[145:11.14] [typing]
[145:13.14] which is just going to need the
[145:16.14] prior
[145:18.14] [typing]
[145:20.14] so I'm kind of getting the sense
[145:22.14] [typing]
[145:24.14] okay
[145:26.14] [typing]
[145:28.14] we're going to try
[145:30.14] [typing]
[145:32.14] so once this happens
[145:34.14] we're going to try
[145:36.14] [typing]
[145:41.14] let's say this is
[145:43.14] more like a
[145:45.14] [typing]
[145:47.14] tills
[145:49.14] drive child, but we'll just
[145:51.14] put this here for now, so we're going to
[145:53.14] pass this stuff in, and if we catch it
[145:55.14] [typing]
[146:10.14] oh, you can break
[146:12.14] from a for loop, like that
[146:14.14] [typing]
[146:16.14] so drive child with some
[146:18.14] stuff here
[146:20.14] if we break
[146:22.14] we're going to do index plus
[146:24.14] one
[146:26.14] and try again
[146:28.14] [typing]
[146:56.14] I don't know if it works that way
[146:58.14] [typing]
[147:02.14] let's just try this out real quick
[147:04.14] I'm going to go
[147:06.14] try break dot js
[147:08.14] for
[147:10.14] [typing]
[147:12.14] I'm going to try
[147:14.14] break
[147:16.14] [typing]
[147:39.14] [typing]
[147:50.14] alright, let's see if this works
[147:52.14] [typing]
[147:55.14] okay, so it does
[147:57.14] good
[147:59.14] [typing]
[148:02.14] because I think this is what we're trying to do
[148:04.14] this is kind of what I want to resolve this down to
[148:06.14] is
[148:08.14] where's the actual state of this thing
[148:10.14] why are we mixing
[148:12.14] [typing]
[148:14.14] two HD keys
[148:16.14] [typing]
[148:18.14] together around here
[148:20.14] and it looks like once we've
[148:22.14] constructed the new one
[148:24.14] [typing]
[148:28.14] the only reason we'd be doing
[148:30.14] the old one
[148:32.14] is to catch
[148:34.14] and to
[148:36.14] derive again
[148:38.14] [typing]
[148:46.14] okay, so we've got the public key value
[148:48.14] now isn't that odd
[148:50.14] [typing]
[148:54.14] HD
[148:56.14] public key
[148:58.14] but then wait
[149:00.14] what are we doing here
[149:02.14] [typing]
[149:09.14] I need to double check on this
[149:11.14] was this line
[149:13.14] [typing]
[149:15.14] so before this had a
[149:17.14] [typing]
[149:19.14] set public key
[149:21.14] ah yes
[149:23.14] [typing]
[149:25.14] so that's where
[149:27.14] [typing]
[149:30.14] that makes total sense
[149:32.14] oh except this looks wrong
[149:34.14] [typing]
[149:36.14] I probably copied this from
[149:38.14] another one which is another reason I don't like
[149:40.14] these being different
[149:42.14] they're so similar
[149:44.14] and yet so different that it's
[149:46.14] confusing
[149:48.14] because I think I copied
[149:50.14] that from somewhere else
[149:52.14] I don't know
[149:54.14] now I'm confused
[149:56.14] [typing]
[149:58.14] because the identifier of this
[150:00.14] I need to make another clone of this
[150:02.14] [typing]
[150:26.14] and then I need to be able to look at it
[150:28.14] oops
[150:30.14] [typing]
[150:34.14] okay
[150:36.14] [typing]
[150:57.14] alright so
[150:59.14] in this one I'm just gonna
[151:01.14] check out
[151:03.14] [typing]
[151:06.14] -hd and I'm gonna take a look
[151:08.14] in this loop
[151:10.14] and see if I can
[151:12.14] understand if
[151:14.14] my thoughts are correct
[151:16.14] here because if we're not, I think we should
[151:18.14] not be modifying
[151:20.14] the parent, what's the name
[151:22.14] of this loop again, this is the derive child
[151:24.14] loop, okay
[151:26.14] so let's take a look at derive child
[151:28.14] [typing]
[151:32.14] there it is
[151:34.14] so I want to look at hd key
[151:36.14] I want to see what's going on
[151:38.14] so we create some stuff
[151:40.14] using the original, using
[151:42.14] the parent, and then what else
[151:44.14] comes from the parent
[151:46.14] if something breaks, we try to
[151:48.14] redo the parent, so this is
[151:50.14] set private key
[151:52.14] we're tweaking it, so that's just setting it to itself
[151:54.14] right, that's what I thought
[151:56.14] and then down here
[151:58.14] we copy the public key
[152:00.14] we should already do that
[152:02.14] so we need not just the keys
[152:04.14] we need a copy
[152:06.14] of the key
[152:08.14] that's important
[152:10.14] so
[152:12.14] let me make this
[152:14.14] stipulation over here
[152:16.14] although, I don't
[152:18.14] does that really matter?
[152:20.14] why does it matter if it's a copy?
[152:22.14] because we're going to tweak
[152:24.14] we're going to, ah, okay
[152:26.14] because we're going to modify that
[152:28.14] so private
[152:30.14] key, tweak, add
[152:32.14] so
[152:34.14] let's take a look at the copy
[152:36.14] we normalize
[152:38.14] I don't think that we actually
[152:42.14] need to make that copy there
[152:46.14] so
[153:08.14] we're basically doing big int
[153:10.14] yes, we're doing
[153:12.14] big int math here
[153:14.14] so
[153:22.14] in this case, in the private key tweak
[153:24.14] we don't need the copy
[153:26.14] how about the public key tweak, do we need the copy?
[153:28.14] nope
[153:30.14] we're already making a copy
[153:32.14] okay
[153:34.14] so we don't need that copy
[153:36.14] so we actually can get rid of that
[153:38.14] that's great
[153:40.14] I'm not planning on
[153:42.14] using this in a way where that performance is going to be
[153:44.14] impacted, but I'm just saying
[153:46.14] you know, if I don't need to do it
[153:48.14] don't do it, right?
[154:10.14] okay
[154:12.14] so we do need
[154:18.14] that one there
[154:20.14] alright, but then, this is where I got
[154:22.14] confused, because I think I just copied this
[154:24.14] from the other similar function
[154:26.14] set public key
[154:32.14] and then if
[154:34.14] only in a failure case do we direct, yeah, okay
[154:36.14] cool, so I think we can
[154:38.14] simplify this quite a bit
[154:40.14] okay
[154:42.14] so
[154:44.14] okay
[154:46.14] so
[154:48.14] so
[154:50.14] so
[154:52.14] so
[154:54.14] so
[154:56.14] so
[154:58.14] so
[155:00.14] so
[155:02.14] so
[155:04.14] so
[155:06.14] so
[155:08.14] so
[155:10.14] so
[155:12.14] so
[155:14.14] so
[155:16.14] so
[155:18.14] so
[155:20.14] so
[155:22.14] so
[155:24.14] so
[155:26.14] so
[155:28.14] so
[155:30.14] so
[155:32.14] so
[155:34.14] so
[155:36.14] so
[155:38.14] so
[155:40.14] so
[155:42.14] so
[155:44.14] so
[155:46.14] so
[155:48.14] so
[155:50.14] so
[155:52.14] so
[155:54.14] so
[155:56.14] so
[155:58.14] so
[156:00.14] so
[156:02.14] so
[156:04.14] so
[156:06.14] so
[156:08.14] so
[156:10.14] so
[156:12.14] so
[156:14.14] so
[156:16.14] so
[156:18.14] so
[156:20.14] so
[156:22.14] so
[156:24.14] so
[156:26.14] so
[156:28.14] so
[156:30.14] so
[156:32.14] so
[156:34.14] so
[156:36.14] so
[156:38.14] so
[156:40.14] so
[156:42.14] so
[156:44.14] so
[156:46.14] so
[156:48.14] so
[156:50.14] so
[156:52.14] so
[156:54.14] the question is
[156:56.14] oops
[157:02.14] if we're trying
[157:04.14] to derive a child
[157:06.14] can we derive
[157:08.14] we cannot derive
[157:10.14] hard, okay, so this
[157:12.14] is important, and I knew this
[157:14.14] but I'm going to articulate it now
[157:16.14] we cannot derive
[157:18.14] a new
[157:20.14] a new child
[157:22.14] from
[157:24.14] something that's hardened
[157:26.14] without
[157:28.14] the private key
[157:30.14] so we cannot
[157:34.14] derive a new public
[157:36.14] key
[157:38.14] from a
[157:40.14] hardened key
[157:42.14] period
[157:44.14] without the private key
[157:46.14] yeah, okay
[157:48.14] so
[157:50.14] so
[157:52.14] so
[157:54.14] so
[157:56.14] so
[157:58.14] so
[158:00.14] so
[158:02.14] so
[158:04.14] so
[158:06.14] so
[158:08.14] so
[158:10.14] so
[158:12.14] so
[158:14.14] so
[158:16.14] so
[158:18.14] so
[158:20.14] so
[158:22.14] so
[158:24.14] so
[158:26.14] so
[158:28.14] so
[158:30.14] so
[158:32.14] so
[158:34.14] so
[158:36.14] so
[158:38.14] so
[158:40.14] so
[158:42.14] so
[158:44.14] so
[158:46.14] so
[158:48.14] have hardened
[158:50.14] key
[158:52.14] have
[158:54.14] private key
[158:56.14] can derive
[159:02.14] private key
[159:06.14] can derive
[159:10.14] public key
[159:12.14] public key
[159:14.14] public key
[159:16.14] public key
[159:18.14] public key
[159:20.14] public key
[159:22.14] public key
[159:24.14] public key
[159:26.14] public key
[159:28.14] public key
[159:30.14] no private key
[159:32.14] no private key
[159:34.14] no private key
[159:36.14] error
[159:38.14] error
[159:40.14] error
[159:42.14] error
[159:44.14] have
[159:46.14] unhardened
[159:48.14] and then
[160:02.14] have private key
[160:04.14] so
[160:06.14] so
[160:08.14] so
[160:10.14] so
[160:12.14] so
[160:14.14] so
[160:16.14] so
[160:18.14] so
[160:20.14] so
[160:22.14] so
[160:24.14] so
[160:26.14] so
[160:28.14] so
[160:30.14] so
[160:32.14] so
[160:34.14] so
[160:36.14] so
[160:38.14] so
[160:40.14] so
[160:42.14] so
[160:44.14] so
[160:46.14] so
[160:48.14] so
[160:50.14] so
[160:52.14] so
[160:54.14] so
[160:56.14] so
[160:58.14] so
[161:00.14] so
[161:02.14] so
[161:04.14] so
[161:06.14] so
[161:08.14] so
[161:10.14] so
[161:12.14] so
[161:14.14] so
[161:16.14] so
[161:18.14] so
[161:20.14] so
[161:22.14] so
[161:24.14] so
[161:26.14] so
[161:28.14] so
[161:30.14] so
[161:32.14] so
[161:34.14] so
[161:36.14] so
[161:38.14] so
[161:40.14] so
[161:42.14] so
[161:44.14] so
[161:46.14] so
[161:48.14] so
[161:50.14] so
[161:52.14] so
[161:54.14] so
[161:56.14] so
[161:58.14] so
[162:00.14] so
[162:02.14] so
[162:04.14] so
[162:06.14] so
[162:08.14] so
[162:10.14] so
[162:12.14] so
[162:14.14] so
[162:16.14] so
[162:18.14] so
[162:20.14] so
[162:22.14] so
[162:24.14] so
[162:26.14] so
[162:28.14] so
[162:30.14] so
[162:32.14] so
[162:34.14] so
[162:36.14] so
[162:38.14] so
[162:40.14] so
[162:42.14] so
[162:44.14] so
[162:46.14] so
[162:48.14] so
[162:50.14] so
[162:52.14] so
[162:54.14] so
[162:56.14] so
[162:58.14] so
[163:00.14] so
[163:02.14] so
[163:04.14] so
[163:06.14] so
[163:08.14] so
[163:10.14] so
[163:12.14] so
[163:14.14] so
[163:16.14] so
[163:18.14] so
[163:20.14] so
[163:22.14] so
[163:24.14] so
[163:26.14] so
[163:28.14] so
[163:30.14] so
[163:32.14] so
[163:34.14] so
[163:36.14] so
[163:38.14] so
[163:40.14] so
[163:42.14] so
[163:44.14] so
[163:46.14] so
[163:48.14] so
[163:50.14] so
[163:52.14] so
[163:54.14] so
[163:56.14] so
[163:58.14] so
[164:00.14] so
[164:02.14] so
[164:04.14] so
[164:06.14] so
[164:08.14] so
[164:10.14] so
[164:12.14] so
[164:14.14] so
[164:16.14] so
[164:18.14] so
[164:20.14] so
[164:22.14] so
[164:24.14] so
[164:26.14] so
[164:28.14] so
[164:30.14] so
[164:32.14] so
[164:34.14] so
[164:36.14] so
[164:38.14] so
[164:40.14] so
[164:42.14] so
[164:44.14] so
[164:46.14] so
[164:48.14] so
[164:50.14] so
[164:52.14] so
[164:54.14] so
[164:56.14] so
[164:58.14] so
[165:00.14] so
[165:02.14] so
[165:04.14] so
[165:06.14] so
[165:08.14] so
[165:10.14] so
[165:12.14] so
[165:14.14] so
[165:16.14] so
[165:18.14] so
[165:20.14] so
[165:22.14] so
[165:24.14] so
[165:26.14] so
[165:28.14] so
[165:30.14] so
[165:32.14] so
[165:34.14] so
[165:36.14] so
[165:38.14] so
[165:40.14] so
[165:42.14] so
[165:44.14] so
[165:46.14] so
[165:48.14] so
[165:50.14] so
[165:52.14] so
[165:54.14] so
[165:56.14] so
[165:58.14] so
[166:00.14] so
[166:02.14] so
[166:04.14] so
[166:06.14] so
[166:08.14] so
[166:10.14] so
[166:12.14] so
[166:14.14] so
[166:16.14] so
[166:18.14] so
[166:20.14] so
[166:22.14] so
[166:24.14] so
[166:26.14] so
[166:28.14] so
[166:30.14] so
[166:32.14] so
[166:34.14] so
[166:36.14] so
[166:38.14] so
[166:40.14] so
[166:42.14] so
[166:44.14] so
[166:46.14] so
[166:48.14] so
[166:50.14] so
[166:52.14] so
[166:54.14] so
[166:56.14] so
[166:58.14] so
[167:00.14] so
[167:02.14] so
[167:04.14] so
[167:06.14] so
[167:08.14] so
[167:10.14] so
[167:12.14] so
[167:14.14] so
[167:16.14] so
[167:18.14] so
[167:20.14] so
[167:22.14] so
[167:24.14] so
[167:26.14] so
[167:28.14] so
[167:30.14] so
[167:32.14] so
[167:34.14] so
[167:36.14] so
[167:38.14] so
[167:40.14] so
[167:42.14] so
[167:44.14] so
[167:46.14] so
[167:48.14] so
[167:50.14] so
[167:52.14] so
[167:54.14] so
[167:56.14] so
[167:58.14] so
[168:00.14] so
[168:02.14] so
[168:04.14] so
[168:06.14] so
[168:08.14] so
[168:10.14] so
[168:12.14] so
[168:14.14] so
[168:16.14] so
[168:18.14] so
[168:20.14] so
[168:22.14] so
[168:24.14] so
[168:26.14] so
[168:28.14] so
[168:30.14] so
[168:32.14] so
[168:34.14] so
[168:36.14] so
[168:38.14] so
[168:40.14] so
[168:42.14] so
[168:44.14] so
[168:46.14] so
[168:48.14] so
[168:50.14] so
[168:52.14] so
[168:54.14] so
[168:56.14] so
[168:58.14] so
[169:00.14] so
[169:02.14] so
[169:04.14] so
[169:06.14] so
[169:08.14] so
[169:10.14] so
[169:12.14] so
[169:14.14] so
[169:16.14] so
[169:18.14] so
[169:20.14] so
[169:22.14] so
[169:24.14] so
[169:26.14] so
[169:28.14] so
[169:30.14] so
[169:32.14] so
[169:34.14] so
[169:36.14] so
[169:38.14] so
[169:40.14] so
[169:42.14] so
[169:44.14] so
[169:46.14] so
[169:48.14] so
[169:50.14] so
[169:52.14] so
[169:54.14] so
[169:56.14] so
[169:58.14] so
[170:00.14] so
[170:02.14] so
[170:04.14] so
[170:06.14] so
[170:08.14] so
[170:10.14] so
[170:12.14] so
[170:14.14] so
[170:16.14] so
[170:18.14] so
[170:20.14] so
[170:22.14] so
[170:24.14] so
[170:26.14] so
[170:28.14] so
[170:30.14] so
[170:32.14] so
[170:34.14] so
[170:36.14] so
[170:38.14] so
[170:40.14] so
[170:42.14] so
[170:44.14] so
[170:46.14] so
[170:48.14] so
[170:50.14] so
[170:52.14] so
[170:54.14] so
[170:56.14] so
[170:58.14] so
[171:00.14] so
[171:02.14] so
[171:04.14] so
[171:06.14] so
[171:08.14] so
[171:10.14] so
[171:12.14] so
[171:14.14] so
[171:16.14] so
[171:18.14] so
[171:20.14] so
[171:22.14] so
[171:24.14] so
[171:26.14] so
[171:28.14] so
[171:30.14] so
[171:32.14] so
[171:34.14] so
[171:36.14] so
[171:38.14] so
[171:40.14] so
[171:42.14] so
[171:44.14] so
[171:46.14] so
[171:48.14] so
[171:50.14] so
[171:52.14] so
[171:54.14] so
[171:56.14] so
[171:58.14] so
[172:00.14] so
[172:02.14] so
[172:04.14] so
[172:06.14] so
[172:08.14] so
[172:10.14] so
[172:12.14] so
[172:14.14] so
[172:16.14] so
[172:18.14] so
[172:20.14] so
[172:22.14] so
[172:24.14] so
[172:26.14] so
[172:28.14] so
[172:30.14] so
[172:32.14] so
[172:34.14] so
[172:36.14] so
[172:38.14] so
[172:40.14] so
[172:42.14] so
[172:44.14] so
[172:46.14] so
[172:48.14] so
[172:50.14] so
[172:52.14] so
[172:54.14] so
[172:56.14] so
[172:58.14] so
[173:00.14] so
[173:02.14] so
[173:04.14] so
[173:06.14] so
[173:08.14] so
[173:10.14] so
[173:12.14] so
[173:14.14] so
[173:16.14] so
[173:18.14] so
[173:20.14] so
[173:22.14] so
[173:24.14] so
[173:26.14] so
[173:28.14] so
[173:30.14] so
[173:32.14] so
[173:34.14] so
[173:36.14] so
[173:38.14] so
[173:40.14] so
[173:42.14] so
[173:44.14] so
[173:46.14] so
[173:48.14] so
[173:50.14] so
[173:52.14] so
[173:54.14] so
[173:56.14] so
[173:58.14] so
[174:00.14] so
[174:02.14] so
[174:04.14] so
[174:06.14] so
[174:08.14] so
[174:10.14] so
[174:12.14] so
[174:14.14] so
[174:16.14] so
[174:18.14] so
[174:20.14] so
[174:22.14] so
[174:24.14] so
[174:26.14] so
[174:28.14] so
[174:30.14] so
[174:32.14] so
[174:34.14] so
[174:36.14] so
[174:38.14] so
[174:40.14] so
[174:42.14] so
[174:44.14] so
[174:46.14] so
[174:48.14] so
[174:50.14] so
[174:52.14] so
[174:54.14] so
[174:56.14] so
[174:58.14] so
[175:00.14] so
[175:02.14] so
[175:04.14] so
[175:06.14] so
[175:08.14] so
[175:10.14] so
[175:12.14] so
[175:14.14] so
[175:16.14] so
[175:18.14] so
[175:20.14] so
[175:22.14] so
[175:24.14] so
[175:26.14] so
[175:28.14] so
[175:30.14] so
[175:32.14] so
[175:34.14] so
[175:36.14] so
[175:38.14] so
[175:40.14] so
[175:42.14] so
[175:44.14] so
[175:46.14] so
[175:48.14] so
[175:50.14] so
[175:52.14] so
[175:54.14] so
[175:56.14] so
[175:58.14] so
[176:00.14] so
[176:02.14] so
[176:04.14] so
[176:06.14] so
[176:08.14] so
[176:10.14] so
[176:12.14] so
[176:14.14] so
[176:16.14] so
[176:18.14] so
[176:20.14] so
[176:22.14] so
[176:24.14] so
[176:26.14] so
[176:28.14] so
[176:30.14] so
[176:32.14] so
[176:34.14] so
[176:36.14] so
[176:38.14] so
[176:40.14] so
[176:42.14] so
[176:44.14] so
[176:46.14] so
[176:48.14] so
[176:50.14] so
[176:52.14] so
[176:54.14] so
[176:56.14] so
[176:58.14] so
[177:00.14] so
[177:02.14] so
[177:04.14] so
[177:06.14] so
[177:08.14] so
[177:10.14] so
[177:12.14] so
[177:14.14] so
[177:16.14] so
[177:18.14] so
[177:20.14] so
[177:22.14] so
[177:24.14] so
[177:26.14] so
[177:28.14] so
[177:30.14] so
[177:32.14] so
[177:34.14] so
[177:36.14] so
[177:38.14] so
[177:40.14] so
[177:42.14] so
[177:44.14] so
[177:46.14] so
[177:48.14] so
[177:50.14] so
[177:52.14] so
[177:54.14] so
[177:56.14] so
[177:58.14] so
[178:00.14] so
[178:02.14] so
[178:04.14] so
[178:06.14] so
[178:08.14] so
[178:10.14] so
[178:12.14] so
[178:14.14] so
[178:16.14] so
[178:18.14] so
[178:20.14] so
[178:22.14] so
[178:24.14] so
[178:26.14] so
[178:28.14] so
[178:30.14] so
[178:32.14] so
[178:34.14] so
[178:36.14] so
[178:38.14] so
[178:40.14] so
[178:42.14] so
[178:44.14] so
[178:46.14] so
[178:48.14] so
[178:50.14] so
[178:52.14] so
[178:54.14] so
[178:56.14] so
[178:58.14] so
[179:00.14] so
[179:02.14] so
[179:04.14] so
[179:06.14] so
[179:08.14] so
[179:10.14] so
[179:12.14] so
[179:14.14] so
[179:16.14] so
[179:18.14] so
[179:20.14] so
[179:22.14] so
[179:24.14] so
[179:26.14] so
[179:28.14] so
[179:30.14] so
[179:32.14] so
[179:34.14] so
[179:36.14] so
[179:38.14] so
[179:40.14] so
[179:42.14] so
[179:44.14] so
[179:46.14] so
[179:48.14] so
[179:50.14] so
[179:52.14] so
[179:54.14] so
[179:56.14] so
[179:58.14] so
[180:00.14] so
[180:02.14] so
[180:04.14] so
[180:06.14] so
[180:08.14] so
[180:10.14] so
[180:12.14] so
[180:14.14] so
[180:16.14] so
[180:18.14] so
[180:20.14] so
[180:22.14] so
[180:24.14] so
[180:26.14] so
[180:28.14] so
[180:30.14] so
[180:32.14] so
[180:34.14] so
[180:36.14] so
[180:38.14] so
[180:40.14] so
[180:42.14] so
[180:44.14] so
[180:46.14] so
[180:48.14] so
[180:50.14] so
[180:52.14] so
[180:54.14] so
[180:56.14] so
[180:58.14] so
[181:00.14] so
[181:02.14] so
[181:04.14] so
[181:06.14] so
[181:08.14] so
[181:10.14] so
[181:12.14] so
[181:14.14] so
[181:16.14] so
[181:18.14] so
[181:20.14] so
[181:22.14] so
[181:24.14] so
[181:26.14] so
[181:28.14] so
[181:30.14] so
[181:32.14] so
[181:34.14] so
[181:36.14] so
[181:38.14] so
[181:40.14] so
[181:42.14] so
[181:44.14] so
[181:46.14] so
[181:48.14] so
[181:50.14] so
[181:52.14] so
[181:54.14] so
[181:56.14] so
[181:58.14] so
[182:00.14] so
[182:02.14] so
[182:04.14] so
[182:06.14] so
[182:08.14] so
[182:10.14] so
[182:12.14] so
[182:14.14] so
[182:16.14] so
[182:18.14] so
[182:20.14] so
[182:22.14] so
[182:24.14] so
[182:26.14] so
[182:28.14] so
[182:30.14] so
[182:32.14] so
[182:34.14] so
[182:36.14] so
[182:38.14] so
[182:40.14] so
[182:42.14] so
[182:44.14] so
[182:46.14] so
[182:48.14] so
[182:50.14] so
[182:52.14] so
[182:54.14] so
[182:56.14] so
[182:58.14] so
[183:00.14] so
[183:02.14] so
[183:04.14] so
[183:06.14] so
[183:08.14] so
[183:10.14] so
[183:12.14] so
[183:14.14] so
[183:16.14] so
[183:18.14] so
[183:20.14] so
[183:22.14] so
[183:24.14] so
[183:26.14] so
[183:28.14] so
[183:30.14] so
[183:32.14] so
[183:34.14] so
[183:36.14] so
[183:38.14] so
[183:40.14] so
[183:42.14] so
[183:44.14] so
[183:46.14] so
[183:48.14] so
[183:50.14] so
[183:52.14] so
[183:54.14] so
[183:56.14] so
[183:58.14] so
[184:00.14] so
[184:02.14] so
[184:04.14] so
[184:06.14] so
[184:08.14] so
[184:10.14] so
[184:12.14] so
[184:14.14] so
[184:16.14] so
[184:18.14] so
[184:20.14] so
[184:22.14] so
[184:24.14] so
[184:26.14] so
[184:28.14] so
[184:30.14] so
[184:32.14] so
[184:34.14] so
[184:36.14] so
[184:38.14] so
[184:40.14] so
[184:42.14] so
[184:44.14] so
[184:46.14] so
[184:48.14] so
[184:50.14] so
[184:52.14] so
[184:54.14] so
[184:56.14] so
[184:58.14] so
[185:00.14] so
[185:02.14] so
[185:04.14] so
[185:06.14] so
[185:08.14] so
[185:10.14] so
[185:12.14] so
[185:14.14] so
[185:16.14] so
[185:18.14] so
[185:20.14] so
[185:22.14] so
[185:24.14] so
[185:26.14] so
[185:28.14] so
[185:30.14] so
[185:32.14] so
[185:34.14] so
[185:36.14] so
[185:38.14] so
[185:40.14] so
[185:42.14] so
[185:44.14] so
[185:46.14] so
[185:48.14] so
[185:50.14] so
[185:52.14] so
[185:54.14] so
[185:56.14] so
[185:58.14] so
[186:00.14] so
[186:02.14] so
[186:04.14] so
[186:06.14] so
[186:08.14] so
[186:10.14] so
[186:12.14] so
[186:14.14] so
[186:16.14] so
[186:18.14] so
[186:20.14] so
[186:22.14] so
[186:24.14] so
[186:26.14] so
[186:28.14] so
[186:30.14] so
[186:32.14] so
[186:34.14] so
[186:36.14] so
[186:38.14] so
[186:40.14] so
[186:42.14] so
[186:44.14] so
[186:46.14] so
[186:48.14] so
[186:50.14] so
[186:52.14] so
[186:54.14] so
[186:56.14] so
[186:58.14] so
[187:00.14] so
[187:02.14] so
[187:04.14] so
[187:06.14] so
[187:08.14] so
[187:10.14] so
[187:12.14] so
[187:14.14] so
[187:16.14] so
[187:18.14] so
[187:20.14] so
[187:22.14] so
[187:24.14] so
[187:26.14] so
[187:28.14] so
[187:30.14] so
[187:32.14] so
[187:34.14] so
[187:36.14] so
[187:38.14] so
[187:40.14] so
[187:42.14] so
[187:44.14] so
[187:46.14] so
[187:48.14] so
[187:50.14] so
[187:52.14] so
[187:54.14] so
[187:56.14] so
[187:58.14] so
[188:00.14] so
[188:02.14] so
[188:04.14] so
[188:06.14] so
[188:08.14] so
[188:10.14] so
[188:12.14] so
[188:14.14] so
[188:16.14] so
[188:18.14] so
[188:20.14] so
[188:22.14] so
[188:24.14] so
[188:26.14] so
[188:28.14] so
[188:30.14] so
[188:32.14] so
[188:34.14] so
[188:36.14] so
[188:38.14] so
[188:40.14] so
[188:42.14] so
[188:44.14] so
[188:46.14] so
[188:48.14] so
[188:50.14] so
[188:52.14] so
[188:54.14] so
[188:56.14] so
[188:58.14] so
[189:00.14] so
[189:02.14] so
[189:04.14] so
[189:06.14] so
[189:08.14] so
[189:10.14] so
[189:12.14] so
[189:14.14] so
[189:16.14] so
[189:18.14] so
[189:20.14] so
[189:22.14] so
[189:24.14] so
[189:26.14] so
[189:28.14] so
[189:30.14] so
[189:32.14] so
[189:34.14] so
[189:36.14] so
[189:38.14] so
[189:40.14] so
[189:42.14] so
[189:44.14] so
[189:46.14] so
[189:48.14] so
[189:50.14] so
[189:52.14] so
[189:54.14] so
[189:56.14] so
[189:58.14] so
[190:00.14] so
[190:02.14] so
[190:04.14] so
[190:06.14] so
[190:08.14] so
[190:10.14] so
[190:12.14] so
[190:14.14] so
[190:16.14] so
[190:18.14] so
[190:20.14] so
[190:22.14] so
[190:24.14] so
[190:26.14] so
[190:28.14] so
[190:30.14] so
[190:32.14] so
[190:34.14] so
[190:36.14] so
[190:38.14] so
[190:40.14] so
[190:42.14] so
[190:44.14] so
[190:46.14] so
[190:48.14] so
[190:50.14] so
[190:52.14] so
[190:54.14] so
[190:56.14] so
[190:58.14] so
[191:00.14] so
[191:02.14] so
[191:04.14] so
[191:06.14] so
[191:08.14] so
[191:10.14] so
[191:12.14] so
[191:14.14] so
[191:16.14] so
[191:18.14] so
[191:20.14] so
[191:22.14] so
[191:24.14] so
[191:26.14] so
[191:28.14] so
[191:30.14] so
[191:32.14] so
[191:34.14] so
[191:36.14] so
[191:38.14] so
[191:40.14] so
[191:42.14] so
[191:44.14] so
[191:46.14] so
[191:48.14] so
[191:50.14] so
[191:52.14] so
[191:54.14] so
[191:56.14] so
[191:58.14] so
[192:00.14] so
[192:02.14] so
[192:04.14] so
[192:06.14] so
[192:08.14] so
[192:10.14] so
[192:12.14] so
[192:14.14] so
[192:16.14] so
[192:18.14] so
[192:20.14] so
[192:22.14] so
[192:24.14] so
[192:26.14] so
[192:28.14] so
[192:30.14] so
[192:32.14] so
[192:34.14] so
[192:36.14] so
[192:38.14] so
[192:40.14] so
[192:42.14] so
[192:44.14] so
[192:46.14] so
[192:48.14] so
[192:50.14] so
[192:52.14] so
[192:54.14] so
[192:56.14] so
[192:58.14] so
[193:00.14] so
[193:02.14] so
[193:04.14] so
[193:06.14] so
[193:08.14] so
[193:10.14] so
[193:12.14] so
[193:14.14] so
[193:16.14] so
[193:18.14] so
[193:20.14] so
[193:22.14] so
[193:24.14] so
[193:26.14] so
[193:28.14] so
[193:30.14] so
[193:32.14] so
[193:34.14] so
[193:36.14] so
[193:38.14] so
[193:40.14] so
[193:42.14] so
[193:44.14] so
[193:46.14] so
[193:48.14] so
[193:50.14] so
[193:52.14] so
[193:54.14] so
[193:56.14] so
[193:58.14] so
[194:00.14] so
[194:02.14] so
[194:04.14] so
[194:06.14] so
[194:08.14] so
[194:10.14] so
[194:12.14] so
[194:14.14] so
[194:16.14] so
[194:18.14] so
[194:20.14] so
[194:22.14] so
[194:24.14] so
[194:26.14] so
[194:28.14] so
[194:30.14] so
[194:32.14] so
[194:34.14] so
[194:36.14] so
[194:38.14] so
[194:40.14] so
[194:42.14] so
[194:44.14] so
[194:46.14] so
[194:48.14] so
[194:50.14] so
[194:52.14] so
[194:54.14] so
[194:56.14] so
[194:58.14] so
[195:00.14] so
[195:02.14] so
[195:04.14] so
[195:06.14] so
[195:08.14] so
[195:10.14] so
[195:12.14] so
[195:14.14] so
[195:16.14] so
[195:18.14] so
[195:20.14] so
[195:22.14] so
[195:24.14] so
[195:26.14] so
[195:28.14] so
[195:30.14] so
[195:32.14] so
[195:34.14] so
[195:36.14] so
[195:38.14] so
[195:40.14] so
[195:42.14] so
[195:44.14] so
[195:46.14] so
[195:48.14] so
[195:50.14] so
[195:52.14] so
[195:54.14] so
[195:56.14] so
[195:58.14] so
[196:00.14] so
[196:02.14] so
[196:04.14] so
[196:06.14] so
[196:08.14] so
[196:10.14] so
[196:12.14] so
[196:14.14] so
[196:16.14] so
[196:18.14] so
[196:20.14] so
[196:22.14] so
[196:24.14] so
[196:26.14] so
[196:28.14] so
[196:30.14] so
[196:32.14] so
[196:34.14] so
[196:36.14] so
[196:38.14] so
[196:40.14] so
[196:42.14] so
[196:44.14] so
[196:46.14] so
[196:48.14] so
[196:50.14] so
[196:52.14] so
[196:54.14] so
[196:56.14] so
[196:58.14] so
[197:00.14] so
[197:02.14] so
[197:04.14] so
[197:06.14] so
[197:08.14] so
[197:10.14] so
[197:12.14] so
[197:14.14] so
[197:16.14] so
[197:18.14] so
[197:20.14] so
[197:22.14] so
[197:24.14] so
[197:26.14] so
[197:28.14] so
[197:30.14] so
[197:32.14] so
[197:34.14] so
[197:36.14] so
[197:38.14] so
[197:40.14] so
[197:42.14] so
[197:44.14] so
[197:46.14] so
[197:48.14] so
[197:50.14] so
[197:52.14] so
[197:54.14] so
[197:56.14] so
[197:58.14] so
[198:00.14] so
[198:02.14] so
[198:04.14] so
[198:06.14] so
[198:08.14] so
[198:10.14] so
[198:12.14] so
[198:14.14] so
[198:16.14] so
[198:18.14] so
[198:20.14] so
[198:22.14] so
[198:24.14] so
[198:26.14] so
[198:28.14] so
[198:30.14] so
[198:32.14] so
[198:34.14] so
[198:36.14] so
[198:38.14] so
[198:40.14] so
[198:42.14] so
[198:44.14] so
[198:46.14] so
[198:48.14] so
[198:50.14] so
[198:52.14] so
[198:54.14] so
[198:56.14] so
[198:58.14] so
[199:00.14] so
[199:02.14] so
[199:04.14] so
[199:06.14] so
[199:08.14] so
[199:10.14] so
[199:12.14] so
[199:14.14] so
[199:16.14] so
[199:18.14] so
[199:20.14] so
[199:22.14] so
[199:24.14] so
[199:26.14] so
[199:28.14] so
[199:30.14] so
[199:32.14] so
[199:34.14] so
[199:36.14] so
[199:38.14] so
[199:40.14] so
[199:42.14] so
[199:44.14] so
[199:46.14] so
[199:48.14] so
[199:50.14] so
[199:52.14] so
[199:54.14] so
[199:56.14] so
[199:58.14] so
[200:00.14] so
[200:02.14] so
[200:04.14] so
[200:06.14] so
[200:08.14] so
[200:10.14] so
[200:12.14] so
[200:14.14] so
[200:16.14] so
[200:18.14] so
[200:20.14] so
[200:22.14] so
[200:24.14] so
[200:26.14] so
[200:28.14] so
[200:30.14] so
[200:32.14] so
[200:34.14] so
[200:36.14] so
[200:38.14] so
[200:40.14] so
[200:42.14] so
[200:44.14] so
[200:46.14] so
[200:48.14] so
[200:50.14] so
[200:52.14] so
[200:54.14] so
[200:56.14] so
[200:58.14] so
[201:00.14] so
[201:02.14] so
[201:04.14] so
[201:06.14] so
[201:08.14] so
[201:10.14] so
[201:12.14] so
[201:14.14] so
[201:16.14] so
[201:18.14] so
[201:20.14] so
[201:22.14] so
[201:24.14] so
[201:26.14] so
[201:28.14] so
[201:30.14] so
[201:32.14] so
[201:34.14] so
[201:36.14] so
[201:38.14] so
[201:40.14] so
[201:42.14] so
[201:44.14] so
[201:46.14] so
[201:48.14] so
[201:50.14] so
[201:52.14] so
[201:54.14] so
[201:56.14] so
[201:58.14] so
[202:00.14] so
[202:02.14] so
[202:04.14] so
[202:06.14] so
[202:08.14] so
[202:10.14] so
[202:12.14] so
[202:14.14] so
[202:16.14] so
[202:18.14] so
[202:20.14] so
[202:22.14] so
[202:24.14] so
[202:26.14] so
[202:28.14] so
[202:30.14] so
[202:32.14] so
[202:34.14] so
[202:36.14] so
[202:38.14] so
[202:40.14] so
[202:42.14] so
[202:44.14] so
[202:46.14] so
[202:48.14] so
[202:50.14] so
[202:52.14] so
[202:54.14] so
[202:56.14] so
[202:58.14] so
[203:00.14] so
[203:02.14] so
[203:04.14] so
[203:06.14] so
[203:08.14] so
[203:10.14] so
[203:12.14] so
[203:14.14] so
[203:16.14] so
[203:18.14] so
[203:20.14] so
[203:22.14] so
[203:24.14] so
[203:26.14] so
[203:28.14] so
[203:30.14] so
[203:32.14] so
[203:34.14] so
[203:36.14] so
[203:38.14] so
[203:40.14] so
[203:42.14] so
[203:44.14] so
[203:46.14] so
[203:48.14] so
[203:50.14] so
[203:52.14] so
[203:54.14] so
[203:56.14] so
[203:58.14] so
[204:00.14] so
[204:02.14] so
[204:04.14] so
[204:06.14] so
[204:08.14] so
[204:10.14] so
[204:12.14] so
[204:14.14] so
[204:16.14] so
[204:18.14] so
[204:20.14] so
[204:22.14] so
[204:24.14] so
[204:26.14] so
[204:28.14] so
[204:30.14] so
[204:32.14] so
[204:34.14] so
[204:36.14] so
[204:38.14] so
[204:40.14] so
[204:42.14] so
[204:44.14] so
[204:46.14] so
[204:48.14] so
[204:50.14] so
[204:52.14] so
[204:54.14] so
[204:56.14] so
[204:58.14] so
[205:00.14] so
[205:02.14] so
[205:04.14] so
[205:06.14] so
[205:08.14] so
[205:10.14] so
[205:12.14] so
[205:14.14] so
[205:16.14] so
[205:18.14] so
[205:20.14] so
[205:22.14] so
[205:24.14] so
[205:26.14] so
[205:28.14] so
[205:30.14] so
[205:32.14] so
[205:34.14] so
[205:36.14] so
[205:38.14] so
[205:40.14] so
[205:42.14] so
[205:44.14] so
[205:46.14] so
[205:48.14] so
[205:50.14] so
[205:52.14] so
[205:54.14] so
[205:56.14] so
[205:58.14] so
[206:00.14] so
[206:02.14] so
[206:04.14] so
[206:06.14] so
[206:08.14] so
[206:10.14] so
[206:12.14] so
[206:14.14] so
[206:16.14] so
[206:18.14] so
[206:20.14] so
[206:22.14] so
[206:24.14] so
[206:26.14] so
[206:28.14] so
[206:30.14] so
[206:32.14] so
[206:34.14] so
[206:36.14] so
[206:38.14] so
[206:40.14] so
[206:42.14] so
[206:44.14] so
[206:46.14] so
[206:48.14] so
[206:50.14] so
[206:52.14] so
[206:54.14] so
[206:56.14] so
[206:58.14] so
[207:00.14] so
[207:02.14] so
[207:04.14] so
[207:06.14] so
[207:08.14] so
[207:10.14] so
[207:12.14] so that's at least a lot simpler
[207:40.14] so
[207:42.14] so
[207:44.14] so
[207:46.14] so
[207:48.14] so
[207:50.14] so
[207:52.14] so
[207:54.14] so
[207:56.14] so
[207:58.14] so
[208:00.14] so
[208:02.14] so
[208:04.14] so
[208:06.14] so
[208:08.14] so
[208:10.14] so
[208:12.14] so
[208:14.14] so
[208:16.14] so
[208:18.14] so
[208:20.14] so
[208:22.14] so
[208:24.14] so
[208:26.14] so
[208:28.14] so
[208:30.14] so
[208:32.14] so
[208:34.14] so
[208:36.14] so
[208:38.14] so
[208:40.14] so
[208:42.14] so
[208:44.14] so
[208:46.14] so
[208:48.14] so
[208:50.14] so
[208:52.14] so
[208:54.14] so
[208:56.14] so
[208:58.14] so
[209:00.14] so
[209:02.14] so
[209:04.14] so
[209:06.14] so
[209:08.14] so
[209:10.14] so
[209:12.14] so
[209:14.14] so
[209:16.14] so
[209:18.14] so
[209:20.14] so
[209:22.14] so
[209:24.14] so
[209:26.14] so
[209:28.14] so
[209:30.14] so
[209:32.14] so
[209:34.14] so
[209:36.14] so
[209:38.14] so
[209:40.14] so
[209:42.14] so
[209:44.14] so
[209:46.14] so
[209:48.14] so
[209:50.14] so
[209:52.14] so
[209:54.14] so
[209:56.14] so
[209:58.14] so
[210:00.14] so
[210:02.14] so
[210:04.14] so
[210:06.14] so
[210:08.14] so
[210:10.14] so
[210:12.14] so
[210:14.14] so
[210:16.14] so
[210:18.14] so
[210:20.14] so
[210:22.14] so
[210:24.14] so
[210:26.14] so
[210:28.14] so
[210:30.14] so
[210:32.14] so
[210:34.14] so
[210:36.14] so
[210:38.14] so
[210:40.14] so
[210:42.14] so
[210:44.14] so
[210:46.14] so
[210:48.14] so
[210:50.14] so
[210:52.14] so
[210:54.14] so
[210:56.14] so
[210:58.14] so
[211:00.14] so
[211:02.14] so
[211:04.14] so
[211:06.14] so
[211:08.14] so
[211:10.14] so
[211:12.14] so
[211:14.14] so
[211:16.14] so
[211:18.14] so
[211:20.14] so
[211:22.14] so
[211:24.14] so
[211:26.14] so
[211:28.14] so
[211:30.14] so
[211:32.14] so
[211:34.14] so
[211:36.14] so
[211:38.14] so
[211:40.14] so
[211:42.14] so
[211:44.14] so
[211:46.14] so
[211:48.14] so
[211:50.14] so
[211:52.14] so
[211:54.14] so
[211:56.14] so
[211:58.14] so
[212:00.14] so
[212:02.14] so
[212:04.14] so
[212:06.14] so
[212:08.14] so
[212:10.14] so
[212:12.14] so
[212:14.14] so
[212:16.14] so
[212:18.14] so
[212:20.14] so
[212:22.14] so
[212:24.14] so
[212:26.14] so
[212:28.14] so
[212:30.14] so
[212:32.14] so
[212:34.14] so
[212:36.14] so
[212:38.14] so
[212:40.14] so
[212:42.14] so
[212:44.14] so
[212:46.14] so
[212:48.14] so
[212:50.14] so
[212:52.14] so
[212:54.14] so
[212:56.14] so
[212:58.14] so
[213:00.14] so
[213:02.14] so
[213:04.14] so
[213:06.14] so
[213:08.14] so
[213:10.14] so
[213:12.14] so
[213:14.14] so
[213:16.14] so
[213:18.14] so
[213:20.14] so
[213:22.14] so
[213:24.14] so
[213:26.14] so
[213:28.14] so
[213:30.14] so
[213:32.14] so
[213:34.14] so
[213:36.14] so
[213:38.14] so
[213:40.14] so
[213:42.14] so
[213:44.14] so
[213:46.14] so
[213:48.14] so
[213:50.14] so
[213:52.14] so
[213:54.14] so
[213:56.14] so
[213:58.14] so
[214:00.14] so
[214:02.14] so
[214:04.14] so
[214:06.14] so
[214:08.14] so
[214:10.14] so
[214:12.14] I'm gonna, I'm gonna try my understanding trick again.
[214:39.72] A little later on.
[214:42.92] Let me get a little further.
[214:59.84] Cause I'm, I'm...
[215:20.80] Okay, now that, look how much simpler that is now.
[215:42.12] And I think we can do similar for this.
[216:07.20] In fact, so here's, here's another thing is we apply this harden offset.
[216:12.60] Okay, let me, let me think a little more about this.
[216:22.44] Okay, that, that, that thought that I had, I think it's going to come back to me.
[216:34.60] So 256 bit.
[216:46.80] So this is concat syntax.
[216:49.08] So this is saying, start 32, start 256.
[217:14.08] Okay, what, I'm a little confused by this syntax.
[217:30.26] I don't think it really adds anything.
[217:36.52] I think this is more confusing than it's helpful.
[217:39.36] I understand index byte goes at the end either way.
[217:47.96] I don't understand what this is saying, cause this is saying two things.
[217:51.60] I think this is saying that this is equal to either of these, that it's equal to a point
[217:58.04] lowercase K par, which looks like a private key or uppercase K par, which I'm guessing
[218:03.40] that's a public key because this is the private key.
[218:09.40] So it's zero bit and I'm thinking that it could, that basically this could be a compressed
[218:21.36] versus uncompressed capital K par might be compressed and maybe point of private is uncompressed.
[218:30.28] I don't know, but I'm just going to get rid of this because again, the comments hurt more
[218:36.20] than they help.
[218:43.12] On this one.
[219:01.84] Okay, let's move these right back around.
[219:31.36] Yeah.
[219:39.48] Yeah.
[219:56.60] Okay.
[220:19.72] Okay.
[220:42.84] Okay.
[221:04.20] Where am I at here?
[221:12.92] Where's private key used?
[221:15.24] It's used in these three places, four places, I'm going to try to see if I can resurrect
[221:44.88] that thought now that...
[221:45.88] Okay.
[221:52.88] Okay.
[221:59.88] All right, let me go back on that thought where I thought I understood something.
[222:29.80] So, we've got to derive child.
[222:33.36] We get an index of first actually see where the hardened inset is.
[222:54.36] Okay.
[223:02.44] Okay.
[223:18.52] I'm almost ready to go back to that thought.
[223:47.84] We're going to go back here.
[224:13.70] Derive child, we're going to harden it.
[224:38.36] Okay, now this changes how I used it and this will change how I use in my wallet function,
[225:07.14] but I think this needs to be more explicit anyway, that this needs to be something like
[225:13.72] derive path and this needs to be something like derive index rather than derive child
[225:24.68] because they both derive a child.
[225:27.04] This one derives it all the way down, derives the full path, and this one derives a single
[225:36.00] index that may be hardened or not.
[225:37.92] And I want to know, because we know whether or not we're supposed to harden it, because
[225:47.20] this top one, derive path, we don't know whether or not it's supposed to be hardened.
[225:50.56] I'm wondering if I can simplify this further.
[225:53.24] I don't think I really can.
[225:54.32] I think it would not simplify, but make it more, would actually increase complexity if
[225:59.92] I tried to swap out the harden piece here.
[226:07.32] Well we could say, what do we know about that?
[226:12.08] Harden data, do we do data.set anywhere else?
[226:16.36] We do not.
[226:18.28] So here's what we could say, potentially.
[226:24.48] All right, and what about offset?
[226:28.44] Do we use offset anywhere?
[226:39.16] Let's see if this turns out or not.
[227:02.42] First of all, let's see.
[227:11.36] Data needs to be used either way, right?
[227:15.04] Basically, it gets to be this I, so we could move it inside.
[227:31.76] Yeah that's kind of, that's kind of what it needs to be.
[227:40.84] So we could move this out for sure.
[227:58.96] Okay.
[228:20.40] Let's see.
[228:45.64] Okay.
[228:53.76] So, let's see.
[229:20.84] There we go, okay.
[229:36.08] So that's what we get here.
[229:46.96] And I'm not going to go, that one, offset index, yeah okay.
[230:02.16] I see the reason I did that, it's because index sounds like you're counting the number
[230:08.52] of bytes, but in this case, this is the, I kind of want to rename that to in, rather
[230:14.62] than index, because index sounds too much like, maybe we could call it path index, it's
[230:25.04] not even path index, what would we call that, what is that component, what's a better name
[230:28.92] for that component, I think in, honestly, no, just, hmm.
[230:53.24] All right, and then why do we have this here?
[231:23.22] Shah, 512, new UNA array, subtle crypto, okay.
[231:35.18] So this could actually just go directly to I, that's not necessary.
[231:42.42] And the same thing here, this can go directly to I, that's not necessary anymore, if it
[231:47.18] ever was.
[232:05.90] Okay, and this serialize function.
[232:34.82] Okay, we got a version in there.
[233:03.46] Okay, let's compute the result of this, -4 + 4 is 0, -4 + 5 is 1, -4 + 9 is 5, -4 + 13,
[233:32.34] that sounds like 9, and then -4 + 45, that sounds like 41, so now I can get rid of that
[233:45.18] my offset, right?
[234:03.98] What, oh, serialize is not the right word here.
[234:32.86] I mean, it kind of is, but it's kind of not.
[234:52.26] Okay, so let's do that.
[235:21.38] Okay.
[235:27.58] Okay.
[235:57.30] So there's our xpub raw.
[236:05.10] Okay, so I think I'm going to whip this.
[236:20.14] I'm going to go back over here to, let's see, what have we done with -hd recently?
[236:49.26] Code, rebrand, yeah, nothing much here.
[236:56.78] So npm run test, does this still work?
[236:59.30] That still works.
[237:00.30] All right, I'm going to see if I can get with my, oh, and I totally forgot to go back on
[237:06.14] what I think I understood.
[237:07.14] I might need to do it, still go through it one more time before I'm sure that I have
[237:14.86] a better and not lesser understanding.
[237:16.70] Okay, so this is, I mean, not now this almost fits in a page, it fits in two pages.
[237:21.30] So this is a much, much, much, much, much, much, much simpler function now.
[237:26.78] So this index buffer stuff is just to conserve memory because if this is only ever used synchronously,
[237:33.66] and so we don't need to allocate those bytes over and over and over again.
[237:36.18] It's just a small, it's just a small performance gain that was, if I understood correctly,
[237:41.74] it was in the original.
[237:42.74] So I just wanted to keep that, although with the other stuff that I've changed, this probably
[237:48.62] is a drop in the bucket, probably doesn't do any difference, but whatever, it's there.
[237:53.66] So and again, a code that you have to comment, if you have to comment the code, it's one
[238:01.14] thing to comment the code so that, hey, if you want, if you're curious about this, you
[238:05.50] know, that's what we got here.
[238:06.90] If you're curious about this, it's one recovery byte is going to be null plus 32 prep bytes.
[238:11.90] You know, this is, hey, you need to understand this.
[238:16.66] Don't change this unless you understand this is kind of thing.
[238:21.06] But so the, the index is part of the oh, we're, we're just setting, we're just setting that
[238:34.18] byte so that we can write it later.
[238:36.14] That's, that's all.
[238:37.70] So we've got the index key size indexed key size.
[238:44.94] So here's where I had to put that one recovery bits or no plus 32 private or, or X bytes.
[239:12.46] So here's our key size one plus 32.
[239:38.86] Index key size is four plus key size.
[239:45.18] X key size is 78.
[239:48.02] That's the total.
[239:49.02] That's the, the, you know, base 58 check size, I think is what that is.
[239:56.02] I could be wrong.
[240:02.52] X key size that becomes important later.
[240:07.22] Anyway, that's the only place let's use, you can actually just knock that down right there.
[240:31.06] Raw X key size, no version, okay.
[240:57.42] Indexed key so I don't know if this is true either because this does have the version
[241:08.10] in it.
[241:09.10] Oh, no, I get it, I get it.
[241:17.38] That's because this has the, yeah, okay.
[241:25.18] Back to this derived thing.
[241:26.62] I'm really good.
[241:27.62] I'm really gonna rubber duck it here.
[241:30.18] Okay, so we got some, some bytes that are just for storing the index.
[241:35.14] That's not really that important.
[241:36.42] We get, we get some data that's the size of the key plus the index.
[241:43.18] So the key is the, it could be a public key or a private key.
[241:48.88] So we're going to grab the private key.
[241:50.54] And if this is supposed to be hardened, then if we don't have the private key, then we
[241:54.90] cannot produce another hardened key because hardened keys require that they're based off
[242:00.42] of private keys.
[242:03.50] Now, um, that's nothing, nothing really interesting about that and we can get rid of that comment
[242:14.06] because those comments aren't actually instructive and if you want to find out why, then you
[242:18.54] can go, you know, read that thing up top that I just, I just did about key size.
[242:23.70] Okay.
[242:24.70] So, uh, then we put the index at the end.
[242:29.22] So the index can be as many as it can be, uh, for, for 32 bit, well, actually it's 31
[242:34.34] bit.
[242:35.34] You can see you can have a 31 bit index.
[242:37.26] Okay.
[242:38.26] Whatever.
[242:39.26] So that's the data.
[242:40.26] The data is just the key and the index.
[242:42.56] Now we're going to take that and we're going to, and it could be the private key or the
[242:46.30] public key.
[242:47.48] So chain code, now chain code has to do with the, if I'm not mistaken, I think that's a
[242:54.22] public part.
[242:55.50] I have to go dig through a little bit more to understand really what the chain code is
[243:03.14] all about.
[243:05.06] Um, cause I'm guessing it could be no, cause here we're saying the chain code, chain code
[243:23.38] might not exist.
[243:24.44] What happens in that case?
[243:25.98] Cause I think we actually do want to make sure that before we derive a child, we have
[243:31.62] a chain code chain code happens when we set the seed.
[243:35.66] Okay.
[243:36.66] So the initial chain code comes from setting the seed and that's part of this whole piece
[243:43.78] here.
[243:44.78] Okay.
[243:45.78] Got it.
[243:46.78] So that's the second half.
[243:47.78] The first half, which is treated as the private part is the, is the, uh, H Mac and the second
[243:58.06] part, which wait, hold on.
[244:02.18] Chain code should also be recovered when we recover the key, shouldn't it?
[244:06.50] There should be two places where, I mean three places, uh, they're serialized.
[244:10.74] Now that's where we set it on chain code.
[244:15.86] So there should be where we have the, the basically the recover.
[244:27.14] So set X key.
[244:29.02] Do we not have something about the chain code in here?
[244:31.74] Cause we should have it in here.
[244:34.42] Yeah.
[244:35.42] Chain code.
[244:36.42] Okay.
[244:37.42] Why was my previous search not finding that chain code?
[244:43.02] There it is right there.
[244:44.02] Okay, good.
[244:45.02] That's what I was expecting.
[244:46.02] All right.
[244:47.02] All is well with the world.
[244:48.02] Okay.
[244:49.02] So we got the chain code, drive child.
[244:53.70] All right.
[244:55.58] So, so chain code is the public part of both the private key and the public key.
[245:03.14] Um, I'm not really sure why that is cause the only thing it's used for is the H Mac
[245:10.38] and let's see, is it used for the entropy of the H Mac or the secret?
[245:13.90] Let me go check that out real quick.
[245:18.66] Okay.
[245:20.02] It's used for the entropy of the H Mac.
[245:22.42] So the chain code, we'll see how that's produced in just a minute.
[245:27.46] But I think it's basically every time you do an H Mac, five, 12 H Mac, you get a pretty
[245:33.74] big number and you got some bites on the left and some bites on the right.
[245:37.66] And since, since you have I L which is the private part, I R which is the public part
[245:43.10] and the I R gets reused over and over again as the chain code.
[245:48.10] So we're just generating entropy here.
[245:51.34] That's all we're doing.
[245:55.06] Okay.
[245:58.06] So so back to this point.
[246:00.30] So we're using the private key to generate that H Mac if it's hardened.
[246:07.46] Otherwise we're actually using the public key.
[246:11.32] So when we get to the part where it's not hardened, we use the public key of the, um,
[246:24.26] the parent.
[246:26.06] So when I get to the place where there's no apostrophes, we switch to using the public
[246:31.10] key to then, to then mix that with, mix that public key with the chain code and the index
[246:41.02] and that allows us to derive a private key.
[246:44.42] So while a private and public key.
[246:46.26] So the first half of that H Mac is the private key and the second half of that H Mac is going
[246:55.34] to become the chain code.
[246:58.50] So we create another, you know, HD Mabob here and then on that HD Mabob.
[247:10.98] So we set the public, oh, so we take the parent.
[247:15.70] So here's what we do.
[247:16.98] We take the parent private key and this is, if it's, if it's, whether it's hardened or
[247:26.18] not, we're going to take the parent private key, ah, this is where, this is where the
[247:36.10] unhardened piece that the one where I was like, I don't know if I understood it, I need
[247:40.10] to go back.
[247:42.10] This is where the weakness lives right here because we have the parent private key and
[247:47.14] we tweak the parent private key with the, um, some public pieces.
[247:59.02] So okay, that's where we tweak it and then we create a public key out of that.
[248:07.90] So we basically dilute the private key with public key or information that's, that's more
[248:20.06] or less wholly public and then we create a new public key from that.
[248:26.06] Now if we are just creating a public key, whether it's hardened or not hardened, then
[248:32.22] we use the public key and then that the component, if it's hardened, it'll be mixed in with a
[248:39.98] private key.
[248:44.74] So that seems, am I, am I understanding that right?
[248:47.78] So if it's hardened, the public key is going to be mixed in with the private key, the previous
[248:56.20] private key because private key chain code.
[248:59.22] No, hold on, let me think about this.
[249:03.58] Um, okay, but then the, no, we're, okay, so we're tweaking, okay, we're tweaking the public
[249:15.46] key with public data.
[249:16.46] So we're still diluting the public key either way, the data that gets put in there is data
[249:24.94] that is public-ish if it's not hardened, it comes, it's, it's using, well, it doesn't
[249:35.50] matter because it's an HMAC.
[249:36.78] So whatever happens happens, okay.
[249:39.98] But then the chain code, which is the other part of that, that, so that, that part becomes
[249:49.22] public.
[249:50.52] So half of the key becomes public.
[249:56.98] What's going to be, yeah, the chain code, because it's, it's part of what is generating
[250:00.98] a chain, just like a blockchain.
[250:02.82] You're taking a hash and you're taking some result and then you're hashing it again.
[250:06.98] So you're producing a chain code.
[250:08.66] Okay.
[250:09.66] some reason that a non-hardened key, the next, the private, and so I'm, I'm, I'm not
[250:28.48] a hundred percent on this, but I think I'm close to it.
[250:31.00] If you have a bunch of the children, so let me, let me think back in reverse.
[250:33.86] If you have a bunch of the children, okay, so if you've got a bunch of the children keys,
[250:39.64] what do you know?
[250:40.64] So you have a bunch of children keys.
[250:42.48] Let's say I have a hundred children keys.
[250:46.00] Then I have some information about the public key that they came from, because all of those
[250:57.66] public keys are diluted with.
[251:04.48] What, okay, I'm not, I'm not quite grasping it.
[251:11.88] No, it's not the public keys.
[251:14.04] It's not if I have a hundred public keys, it's if I have their private keys.
[251:17.26] So there's key pairs, there's public private key pairs.
[251:21.12] So if I have a bunch of private keys from a child, so, and it's not hardened, let me,
[251:36.08] let me think about this again.
[251:42.20] How is this any better if it's hardened?
[251:45.34] Why is hardening it better?
[251:48.62] Because if I harden it, then I'm using the private key as part of the mix.
[251:58.52] The private key of the parent becomes part of the HMAC.
[252:03.06] If I'm not hardening it, then the public key of the parent becomes part of the HMAC.
[252:16.28] So if I have children private keys, maybe the information that I had is wrong, but if
[252:21.44] I had children private keys, because once it goes through an HMAC, well, I guess the
[252:25.04] question is this, how much of the data do you know?
[252:28.60] Because the chain code, if it's a bunch of siblings, if it's, if they're siblings, then
[252:34.96] the chain code is the same between all the siblings, right?
[252:40.90] So if the data is going in with the chain code, I don't know, I'm not, I'm not at the
[252:49.46] intellectual prowess right now to grasp it, but there's something in here about the way
[252:55.98] that the key is tweaked.
[252:58.30] We use a private key to create a private, a private child.
[253:04.22] There's a, and if it's hardened, we have to use a private key, but if it's not hardened,
[253:13.74] then we're forced to use a public key.
[253:17.42] So even if we're creating a private key, when it's not hardened, the HMAC data originates
[253:26.14] from the public key, but once it goes through the HMAC, is there, is that recoverable at
[253:32.30] all?
[253:33.30] I don't know, I'm, I'm kind of having some doubts about what I was told.
[253:37.18] I see that they're different.
[253:38.18] I don't know, I have to reconsider this later because I think it's important to know this
[253:43.18] difference, but I don't know what this difference is.
[253:47.66] Maybe it's not that important.
[253:48.66] I don't know.
[253:49.66] I'm going to have to take a look at this again with fresh eyes, but it's 2 a.m.
[253:53.70] So what I want to do is, you know, my last trick at 2 a.m. is I want to go through here
[254:00.06] and just replay that change that I made and see if the test will still pass and I think
[254:05.26] that they will.
[254:06.74] So we're going to go to derive child.
[254:08.60] That's our, our, our function that is going to kill us and we're going to pass in hardened,
[254:16.34] except I would prefer to call it harden.
[254:20.68] So it's going to be hardened, hardened, but we're actually going to move this.
[254:28.04] All right, then we're going to go find derive, derive child and whoops, there are very few
[254:43.72] places where that's happening.
[254:46.20] Oh my gosh, that's so ridiculous now.
[254:48.84] All right, well, we're going to clean this up.
[254:50.68] We're going to clean this bad boy up so good.
[254:53.88] Okay.
[254:55.12] So this is going to be renamed to underscore derived child.
[255:00.20] We're going to copy over pretty much the exact same thing that we had.
[255:05.12] Let's see.
[255:06.12] And we've got index, we've got hardened.
[255:09.12] Now we don't have to D because before we were adding this just so that we could remove it
[255:14.08] so that we could find out if something's hardened.
[255:18.42] So I'm just going to say this is, is hardened or now I'm going to stick with the, the idea
[255:27.40] of hardened.
[255:28.64] So if harden, then we're going to increase the index, except that we can do it right
[255:41.60] here, hard and all right.
[255:48.98] So there we go.
[255:50.74] So we've already got that thing going.
[255:54.48] So we're going to return a weight, HD key dot derived child.
[255:59.38] Okay.
[256:00.38] We got that.
[256:03.74] So index and hardened.
[256:08.54] And this one now has hardened.
[256:10.94] And then if we look at derived child, wherever we've defined that, which I'll go figure out
[256:15.46] where we've defined that HD derived child.
[256:18.96] So we're going to take a Boolean, which is going to be hardened whether or not the index
[256:31.86] should be hardened.
[256:35.42] How about just enough said, ah, whoops.
[256:59.74] Okay.
[257:05.58] All right.
[257:10.42] So here we are.
[257:11.42] We've got that.
[257:13.06] And then I'm going to go find my loop here.
[257:15.58] There's my four loop.
[257:18.34] Okay.
[257:20.82] I'm just going to keep this simple.
[257:23.14] Oh, we're just going to copy it as is pretty much.
[257:28.58] Just going to bring that right on over.
[257:32.50] Okay.
[257:36.46] Except that we need to return it exactly as it is over here.
[257:41.50] Oh, it looks like we were missing.
[257:43.46] I never did add back the hardened there.
[257:46.46] Okay.
[257:47.46] Good.
[257:48.46] Good catch.
[257:49.46] Okay.
[257:50.46] So now we've got, we can derive this child.
[257:52.66] We can harden it.
[257:55.34] Harden the child.
[257:58.34] I don't need any of this nonsense because these, these comments are more hurtful than
[258:04.94] helpful.
[258:05.94] So let's just get rid of those comments.
[258:06.94] Then this is a lot easier to read.
[258:09.02] Okay.
[258:10.02] We already know that we're going to harden it.
[258:11.18] We don't need to comment that we're going to harden it.
[258:14.22] I know that we can get rid of this.
[258:18.74] That should have gone with the UN8 transition.
[258:21.58] Maybe I'll go back and add that.
[258:24.98] Maybe I won't.
[258:25.98] We'll see.
[258:26.98] Okay.
[258:27.98] But, okay, so here we are and then we create a new HD key.
[258:41.38] This is the thing that bugs me is because we're inside of an HD key and we're creating
[258:45.22] an HD key and I don't like that very much.
[258:52.38] We don't need a copy anymore.
[258:54.74] It's sufficient to just have private key.
[258:58.54] We already went through that bit.
[259:02.54] We can do set next proof key.
[259:08.26] That's fine and dandy.
[259:10.70] There's some other things that I did that I got rid of there.
[259:12.82] We don't need to worry about them right now.
[259:15.50] I don't need to worry about any of this catch at all.
[259:18.46] Get rid of all that.
[259:22.42] And now I don't need to worry about any of this catch either.
[259:26.62] And now this is the parent public key.
[259:32.14] That's important.
[259:33.14] We can get rid of that copy, we can get rid of throw, we can get rid of the return.
[259:59.70] Oh, we need to get rid of that comma and turn that into a semi-colon.
[260:06.02] Okay, and we get that public parent key, public child key.
[260:23.70] All right, we get that.
[260:25.70] That's there.
[260:27.54] And we don't need to do anything with the chain code.
[260:30.62] We could reverse see the fingerprint, but just doing this alone, now this is so much
[260:36.98] simpler.
[260:37.98] And I kind of want to get rid of this comment here, actually, because I don't know if it's
[260:42.82] really that helpful.
[260:51.50] And this seems self-explanatory with the variable names.
[260:54.74] You know, we're either generating next pub or next priv, setting the private key or setting
[261:00.66] the public key.
[261:04.50] Okay, so that's a big one right there.
[261:10.34] So let's just run the tests.
[261:11.34] Do they still pass?
[261:12.58] No!
[261:13.58] Why not?
[261:14.58] Oh, whoops, whoopsie.
[261:43.22] I'm going to, I am going to have to update the tests.
[261:54.26] Okay, maybe not.
[262:17.86] Okay, derived child, I mean this, this change was pretty copacetic.
[262:45.46] All right, let's see, what did I, what did I miss?
[263:08.58] Oh, whoops, well, setting that twice shouldn't be a bother.
[263:38.22] Let's just, just see if I'm wrong about that copy.
[263:57.66] Okay, what did I do wrong?
[264:08.10] Okay, so let's, let's back that up.
[264:33.18] And I'm going to try that again.
[264:42.98] So let's just try this change.
[265:04.94] Oh, hey, have a good one man.
[265:18.34] So if hardened, then update the index.
[265:24.70] Oh, whoops, oh, I see what the problem is.
[265:30.74] So index is used right, index is used right there.
[265:41.78] So if we want to update the index, I can do that, it needs to happen right here.
[266:07.06] Close to donuts, that's our issue.
[266:17.30] PM run test, really?
[266:27.30] Okay let's try this again, we're going to try an even smaller change.
[266:31.90] Okay first of all, and PM run test.
[266:34.62] Okay just making sure this branch, this branch still works.
[266:39.14] Oh wait, dang it, I know what the problem was already.
[266:43.50] It's okay, we're going to take it step by step.
[266:47.18] I forgot to pass hardened into, so these need hardened as well.
[266:52.74] I forgot to pass that hardened.
[267:07.22] Okay but nevertheless, we're going to start with a super small change.
[267:11.74] So we don't need an is hardened, we know it's hardened.
[267:22.14] Okay so we're going to change the index here.
[267:26.22] So this will pass the test, boom, test pass.
[267:29.90] So now, let's try this again, I'm going to move this offset stuff down below.
[267:41.84] I'm going to move the index setting down below where it's all the same.
[267:49.78] And I'm going to move the, so nothing else has changed.
[267:58.34] Should run, okay good.
[267:59.34] Passes test.
[268:00.34] Okay now, we're going to move this into here, alright, and then get rid of all this nonsense.
[268:19.22] Okay test pass, as they should, great.
[268:23.54] Okay and then in this particular case, I don't know, I kind of hope it's clear from, I just
[268:43.94] kind of want to get rid of that.
[268:46.00] Alright so here's this whole chunk where we're doing everything we need to do with data.
[268:51.18] Okay and then, like I said before, we can get rid of this, we can get rid of the other
[268:54.26] iBuff, just make that i, it's going to be fine, i equals, okay so now I need to deal
[269:04.70] with that other hardened.
[269:06.44] So let's just make one layer of quick abstraction here.
[269:11.92] So what we're going to do, is again, we're just going to copy this whole loop, and this
[269:20.14] should be almost correct as is, we're going to need to change that harden to hardened.
[269:28.58] Other than that, this is correct as is, okay.
[269:39.62] So if we don't do anything else, and we just call this, test should still pass, yep.
[269:44.94] Now we can get rid of those nasty try catch blocks, so try, and then just get rid of this
[269:52.18] thing, get rid of this thing, get rid of all of this, get rid of all of this, get rid of
[269:58.98] all of this.
[270:02.06] Okay now, this should function exactly the same, and it does.
[270:09.46] Okay so I'm going to go ahead and add this, because this is a change that I do want to
[270:13.82] bring over.
[270:16.42] Okay, let next priv key equals, I'm going to move this, next priv key.
[270:33.26] So we add our experimental branch, and then this is our cleanup.
[270:40.42] And we don't need that public key copy, because the way that this tweak works, it already
[270:59.34] makes a copy.
[271:04.26] Okay, all right again, npm run test, everything passes, I'm adding it.
[271:27.94] Yeah, this kind of makes sense just to group those together.
[271:57.22] All right and then, let's put these in the order that they go in, because I remember
[272:03.62] there was a little bit of confusion about that, where we serialize, let's get to serialize
[272:09.46] real quick, where is serialize?
[272:13.54] So the order that they go in when they are serialized is, there's the X key buffer, there's,
[272:24.22] okay that's, it's version, depth, fingerprint, index, chain code.
[272:32.70] Okay I'm going to write that down, version, depth, fingerprint, index, chain code, key.
[272:50.96] That's how they're stored in the file.
[273:02.70] So let's see how close we can get to that, in terms of, chain code comes last, even though
[273:08.86] alphabetically it comes first, fingerprint, depth, key itself, whatever the key data is,
[273:28.24] okay and then this is all, is any of this stuff that we could set before, does it have
[273:34.96] to be set after for some reason?
[273:38.04] But we don't know until we know the, no, that's the parent fingerprint.
[273:43.80] So I think I could be wrong, I think all of this information we already know.
[273:55.42] So when we go to create this thing, the only information, yeah, there's the version.
[274:00.48] The version is set, this is exactly the right order, excellent.
[274:12.36] Okay cool, so now this actually makes a little bit more sense in terms of parity between
[274:21.88] the way that the serialization works and the way that we're calculating the data.
[274:28.08] Alright, that one, so data, this is all necessary in order to calculate, and again SHA-512-HMAC,
[274:48.68] we'd call it seed buffer, okay.
[274:55.04] So I'd kind of prefer to call that, rather than call it seed, data, let's call it seed.
[275:08.96] That's a much better descriptor.
[275:25.44] So we're creating the seed, ah yes, that's beautiful.
[275:31.16] Now let's just double check, SHA-512, is there anywhere else?
[275:36.72] So here it's chain code and seed, and here it's master secret and seed.
[275:41.72] So that's more than master secret, it's more like the root secret, I would call it.
[275:45.48] In fact, I think I will call it that later.
[275:48.16] I'm going to change that over here, because like I said, this is my experimental playground,
[275:55.36] everything I'm doing here is just going to get thrown away.
[276:05.00] And this, this is my happy code.
[276:10.80] This is where the stuff works.
[276:13.74] Okay, so with that, okay, everything passes test, and another bug down, and another bug
[276:38.26] down, and another bug passes, and another patch passes test, don't, don't, don't, another
[276:44.98] patch passes test, and another bug down, and another bug down, and another patch passes
[276:50.26] test, patch passes test, little tongue twister there.
[277:01.22] All right.
[277:08.22] All right.
[277:14.22] What was I going to do next?
[277:39.34] Oh, I'm sorry.
[278:07.98] Okay, that one's pretty simple.
[278:28.90] Oh, I was going to change the function signature of derive child.
[278:35.06] That's what I was going to do.
[278:38.86] We're going to have another derive child.
[278:42.14] This is just helper, add param, boolean, hardened.
[279:07.58] Oh, I added before I tested, that was not good, but it's okay, everybody, it's okay.
[279:35.62] Yes.
[279:37.62] Okay.
[279:39.62] Yes.
[280:06.14] It helps so much to name that seed rather than data.
[280:12.50] Okay, everything else here is good.
[280:28.30] So what I'm looking forward to is where there is no -hd.create.
[280:32.54] It's just, here's an object, boom.
[280:41.46] And I don't know if that quite makes sense for this, because it's not an object that's
[280:49.66] really useful to pass around.
[280:52.34] It is something that is incredibly stateful.
[280:55.54] And just getting to that kind of place where, yeah, you can, the object, there is no wonky
[281:06.44] donk state.
[281:08.28] The state is very well contained.
[281:10.90] So the seed here, that makes sense.
[281:21.86] Okay, git commit -m ref simplify derive child.
[281:40.74] Okay, is there anything else I could do right now?
[282:04.14] Okay, so what information makes this thing?
[282:33.70] Okay.
[282:38.26] Okay.
[282:53.54] Okay.
[283:13.86] We're going to fingerprint.
[283:41.98] Okay.
[283:53.26] That's such a small helper method.
[284:23.24] I agree with myself that, or I disagree with myself, I don't want to export that.
[284:33.90] It's too useless.
[284:35.86] It was stupid to do the work to export it the first time.
[284:41.02] Okay.
[284:42.02] So, this is going to be async, so fingerprint await, git finger print.
[284:52.98] That was it.
[284:53.98] It was the only place that was ever used.
[284:56.58] Right there.
[284:57.58] Okay.
[284:58.58] And then identify.
[284:59.58] I actually had a really good methodology.
[285:06.82] Let me go back over to this fingerprint.
[285:26.00] It was actually smart.
[285:31.76] Every once in a while, I hit it out of the park, you know?
[285:36.46] There we go.
[285:37.46] It's actually an intelligent way to do this.
[285:40.90] It's not bad.
[285:48.82] Okay.
[286:06.78] Identify.
[286:30.78] Remove.
[286:53.02] Identify identifier.
[287:20.86] Okay.
[287:27.50] So, I got the fingerprint out of the way.
[287:42.30] What else?
[287:43.30] Let's get back to this, because this is where the core of it all is.
[287:49.74] Right here.
[287:50.74] We can simplify this.
[287:52.70] We can simplify anything.
[287:55.98] What else is there?
[287:56.98] Okay.
[287:57.98] There's the create.
[287:58.98] Ah, yes.
[287:59.98] There's the set public key.
[288:12.42] And there's the public key.
[288:36.10] Let me see here.
[289:03.34] Would we need to normalize the public key if we did public key tweak add?
[289:15.96] And the answer is no, because we already normalize it anyway, right?
[289:26.20] Tweak point at infinity, right?
[289:28.86] So, we already, we're already good there.
[289:33.22] So, we don't need that set public key.
[289:37.72] Don't need it there.
[289:38.72] Oh, I don't think we need it anywhere.
[289:45.34] I think the only reason that you'd want to be able to set public key and private key
[289:48.30] is if you wanted to use those sign methods, and they don't belong here.
[289:54.46] And you are the dumbest link, goodbye.
[290:01.90] Right?
[290:05.22] Yeah.
[290:07.86] Pretty sure.
[290:13.46] So... oh, whoops.
[290:39.86] All right, to public key...
[290:56.14] Oh, I see.
[291:02.66] Proof bytes, proof bytes, proof bytes.
[291:20.82] Okay, and then normalize is just not needed, so it ends up being these three things.
[291:32.46] So, we don't need that, and we don't need this.
[291:41.58] Okay.
[291:42.58] So, that's the next bit, is set private, oh no, public key.
[291:58.46] We'll assert, and then we will, if not, skip verification.
[292:28.18] Then we do this.
[292:34.30] Then we do this.
[292:48.70] HDKey.wipe.
[293:13.62] Wait, there's nothing there anyway, so we don't have to do that, because we're just
[293:29.90] creating one of these doodads from whole cloth, so we don't even need to do that.
[293:35.54] Yeah, that's great.
[293:40.34] Okay, so, all right, doodad creation, we literally, that's it?
[293:55.62] This is literally it.
[293:58.46] Okay, set public key.
[294:15.78] Nothing to do.
[294:37.74] Nothing to do in here.
[295:04.86] And if we didn't set a private key, then we don't have to wipe one, so there's nothing
[295:14.74] to do here, and because here we've already checked what the key can be, so again, no
[295:30.62] op, nothing to do.
[295:35.14] Working as intended, and then all we have is, all right, so now there's no set public
[295:48.70] key.
[295:49.70] We just got rid of it, it was super fluous, it was unnecessary and unimportant, and I
[295:55.66] didn't like it, and now it's gone.
[296:02.18] Excellent.
[296:03.18] Hmm, of course, the tests don't feel the same way.
[296:26.42] To do, adapt to X button.
[296:50.66] Maybe, probably never.
[296:57.62] All right, that's all the set public keys.
[297:15.22] Hmm.
[297:22.70] $4.59.
[297:38.22] $4.59, wait to hex, chain code.
[298:07.16] No extended key.
[298:08.30] Okay, was chain code not...
[298:10.18] Oh.
[298:37.08] Okay.
[299:00.38], set public key.
[299:25.78] Runtest.
[299:26.78] Okay.
[299:27.78] Oh, okay.
[299:28.78] All right, so something happened here, in removing that fingerprint bit.
[299:44.30] Let me think about that.
[299:54.94] Maybe it's the identifier.
[299:58.94] Indeed.
[299:59.94] Okay.
[300:23.94] Okay.
[300:51.94] All right.
[301:20.94] Hdkey-keys.
[301:21.94] No, -hd.
[301:22.94] That's what it is.
[301:23.94] -hd.
[301:24.94] All right.
[301:50.94] Okay, so there's that, and this should only be the -hd changes at that point.
[302:15.58] Yes.
[302:16.58] Okay, cool.
[302:17.58] So we're going to make that -hd change, git add test, git commit -m, and we're going to
[302:24.82] do, this is just -hd rebrand.
[302:42.50] Okay, now we're going to take this, and we're going to take a look at the test, and where
[302:54.58] is that, 2613, 2613.
[303:23.70] What's up?
[303:25.70] Oh, F is just shorthand for fold, or fix up.
[303:38.02] It's a commit message that I'm not going to keep, and I'm going to roll it together.
[303:42.66] That's not a dumb question.
[303:44.80] It's just something I do.
[303:46.50] It's not something that many people do.
[303:49.48] It's not a common practice.
[303:53.06] It's just an AJ thing, but it's, yeah, it's my shorthand, because those commits, I'm not
[303:58.62] going to keep around.
[303:59.62] I'm going to reorganize them, and then, yeah, so, let me just, if I were to rebase this,
[304:05.90] oh, it's not, okay, hold on just one second, yeah, so if I do git rebase 10, so I look
[304:14.06] at these ones right here, FFFFFFF, so this just tells me that it's like a little minor
[304:20.06] fix, a typo fix, a bug fix.
[304:22.42] It's somehow related to a different commit that's prior, and so then I go back and look
[304:26.76] at these things, and I'll say, okay, yep, this was this one.
[304:32.26] That goes to the docs.
[304:35.46] These two go to the docs, actually, and those have to go in order.
[304:39.30] This one goes here, and then this one goes here, so then they all replay, and it all
[304:50.26] works out well, boop, and then, when I actually get ready to do something with it, hold on,
[304:59.30] let me git stash that again, git rebase, so when I actually get ready to push this, because
[305:05.94] I'll have a bunch of these, then I change from pick to F over here, and then that just
[305:13.38] means they roll up, fold, fold, fold, they all fold up into this one, so it just keeps
[305:19.46] the messages clean, and the odd chance that someone actually looks at my code, you could
[305:25.94] tell atomically what I've done in most cases.
[305:30.42] I try to keep the commits atomic, and yeah, because if I have to make just a small change,
[305:40.62] say it's a whitespace change or something like that, and I'm working on a different
[305:43.50] piece of code, but then that change happens, then I'll just stash those changes real quick,
[305:49.74] I'll make the little change that I already just made in the main change set, and then
[305:56.66] I'll do an F commit on that with some little note of what it belongs to, and then git stash
[306:03.82] pop, and then continue.
[306:09.06] That's just an AJ thing, okay, so this is 32 bytes, so this is probably actually going
[306:14.92] to be 8, let's see, hey, thanks devware, also I run a second channel, coolaj86, it's, this
[306:31.06] is where I do my dash work, and that's where I do my non-dash work, but occasionally dash
[306:36.02] work too, alright, so this one here, u8 to hex identifier, I really need, is this the
[306:46.18] first one, okay, oh no, what was that, identifier, there we go, identifier, whoops, okay, so
[307:14.68] we're back up to the top, so now I just need to do the prints on that, so I'm going to
[307:36.92] print, okay, so next print, and then this is going
[308:06.68] to be, what did I just assign that to, print, and then this one is going to be, register
[308:17.68] is s, whoop, there we go, there we go.
[308:45.64] I think that was it.
[309:07.28] So what are you up to devware, devware, devware, I was working in dash, dash queues the other
[309:35.36] day, okay, u8.foreach is not a function, now that I can believe.
[309:57.48] Alright, this is just for the test, so I think, u8.foreach is not a function, 460, 119, let's
[310:16.12] just take a look at that real quick, 119, watching some twitch, saturday evening, saturday
[310:32.12] evening, oh yeah, yeah, yeah, because you're over there, way over there, I remember you're
[310:41.36] back there, it's 3am where I am, I'm going to do this and then I'm going to be done,
[310:52.36] right?
[310:53.36] Yeah.
[310:54.36] Okay, let's take a look here, fingerprint, did I actually return, because you know, sometimes
[311:01.08] you make a function and then you forget to do the return, read uint, oh whoopsies, I
[311:16.04] think I know the other thing that I forgot to do here, so I got the slice, the problem
[311:21.92] is, that's to string 16, that's my problem.
[311:44.84] Alright.
[311:51.84] Oh wait.
[312:11.84] Hmm.
[312:37.84] I think that's part of the fingerprint too, isn't it, it doesn't really need to be re-exposed
[313:01.76] here, oh it does actually, maybe kind of sort of in a way, I'll tackle that problem later.
[313:17.02] Okay the other problem that I still have is u82hex is not going to work on any of these
[313:27.04] because they are numbers, not buffers.
[313:42.36] Yay, alright.
[314:09.68] So now I'm going to do that thing that I said, where I go, look at all these, and I say pick,
[314:18.04] un, fold them all up, be gone, alright I might try one more thing and then be done, so we
[314:26.88] got rid of that, did we get rid of set private key, that one should be easy to get rid of.
[314:34.60] What's doing inside of a set private key, well we just set the private key, and then
[314:40.22] we set the value, so let's see here, is there any place where we actually set the private
[314:45.58] key in a way that would need, so from master seed, okay, from master seed needs, nope,
[315:01.88] from, what is this, from master seed, from extended key, okay so from extended key is
[315:08.18] the only place where we would actually potentially need to check the length of the key because
[315:14.68] that's the only place where it could be bad, or maybe even not because we do say exactly
[315:24.18] how many bytes we're going to grab here, so I don't see any way that we could ever possibly
[315:34.20] need to check the private key length.
[315:45.24] Because if it's from a seed, we know what the length is, if it's from, if we're deriving
[315:51.54] a child, then we literally know what the length is, so there's no way to set a private key
[315:57.94] and to need to know what the length needs to be, okay, let's go check out our other
[316:03.16] uses of set private key, because basically it's just two steps, set the private key and
[316:08.26] set the public key, okay, in this case, actually, you know the reason we have to call set private
[316:23.60] key is just because the private key is actually private, okay, so that checks out, and here,
[316:45.48] this is going to check out as well, where it literally just needs to be, okay, so this
[317:14.76] one, private key equals, yeah, okay, so I'm just going to call this privbytes, boom, okay,
[317:44.48] boom, boom, boom, boom, boom, boom, boom, boom, boom, boom, boom, boom, boom, boom,
[318:12.60] alright, so some private keys need, so when we set the private key, we also set the public
[318:22.44] key, that makes sense, that's just a matter of course, that's something that we need to
[318:45.16] do, alright, npm run test, and it's going to fail, because test is going to be testing
[319:01.20] things like set private key, alright, and we don't need this, because there's just literally
[319:22.12] nothing, there's no use case, okay, get stash,
[319:52.00] get stash real quick, make sure Ryan the test passes, yes it does, good, okay, so set public
[320:01.84] key, wait a minute, why do we still have the, uh oh, something went wrong, okay, so I'm
[320:30.16] just going to, okay, let's do this one first, simplify fingerprint identifier, okay, great,
[320:57.68] okay, good, that worked, alright, now for my next trick, okay, actually get, get reset,
[321:27.12] get checkout, test, and this, okay, so from here, oh, what am I going to do, okay, so
[321:55.72] I'm going to test, alright, test all pass, good, so we're in a good starting state, let's
[322:06.48] go to set private key, we just want to get rid of it, alright, there's no good can come
[322:15.04] of setting a private key, alright, so we're in a good starting state, alright, so we're
[322:42.36] in a good starting state, alright, so we're in a good starting state, alright, so we're
[323:09.46] in a good starting state, alright, so we're in a good starting state, alright, so we're
[323:37.54] in a good starting state, alright, so we're in a good starting state, alright, so we're
[324:06.14] in a good starting state, alright, so we're in a good starting state, alright, so we're
[324:34.50] in a good starting state, alright, so we're in a good starting state, alright, so we're
[325:02.26] in a good starting state, alright, so we're in a good starting state, alright, so we're
[325:31.92] in a good starting state, alright, so we're in a good starting state, alright, so we're
[325:37.02] in a good starting state, alright, so we're in a good starting state, alright, so we're
[325:44.66] in a good starting state, alright, so we're in a good starting state, alright, so we're
[325:51.30] in a good starting state, alright, so we're in a good starting state, alright, so we're
[325:58.30] in a good starting state, alright, so we're in a good starting state, alright, so we're
[326:03.68] in a good starting state, alright, so we're in a good starting state, alright, so we're
[326:09.20] in a good starting state, alright, so we're in a good starting state, alright, so we're
[326:15.64] in a good starting state, alright, so we're in a good starting state, alright, so we're
[326:22.12] in a good starting state, alright, so we're in a good starting state, alright, so we're
[326:28.26] I'm not I'm not I'm a cryptophobe just FYI. I don't I don't believe in that nonsense except sometimes
[326:35.60] Okay
[326:44.88] So let's set private key. What about set public key or to public?
[326:49.92] Key, all right. There we are. So there's two public keys. So set private key if it's from a seed then yes
[326:57.90] We actually should
[326:59.90] Figure out
[327:02.56] What this is going to be next
[327:06.52] So yeah, this this is not a good
[327:09.48] Lurk and learn session the cool age 86 channel. That is those are a bit better for lurk and learns
[327:16.18] Because a lot of times I'm doing stuff on here I am deep in low level bit mashing crap
[327:26.88] But
[327:28.88] I do try to answer comments and everything
[327:36.98] Okay
[327:40.64] Here we have let priv bytes equals
[327:45.86] I'm trying to get this. There we go priv bytes
[327:54.90] And priv bytes
[327:56.90] And then there we go
[328:02.70] So set private key I'm trying basically to remove code
[328:08.44] small tiny duplications here and there like
[328:12.50] Everywhere I said the private key. I also set the public key because I actually want to get rid of the set public key method
[328:19.22] I'm trying to get as as few functions as possible and get this as close to a plain object as possible
[328:25.50] and
[328:28.58] I am almost there
[328:31.58] What I actually want to do is have my
[328:39.26] Well, let me check and make sure this still runs. Oh great. It does
[328:43.98] Huzzah
[328:48.58] Okay, so I I actually want to make the
[328:52.10] See set private key
[328:58.16] Private key to null we don't set private key to null in any of these
[329:14.30] So one thing that I'm thinking about doing let me just get past this
[329:20.34] Remove our get not get commit - M
[329:27.46] Remove set private key
[329:33.66] Well
[329:36.78] not remove
[329:38.26] Simplify set private key. I could potentially remove it if I were going to remove it
[329:44.84] Is this free time or work? This is actually work
[329:48.46] But I also yes, I do work in my free time and
[329:53.12] 3 a.m. Is yet. I I get to work whenever I want to work right now, so that's great
[329:59.02] Okay, so
[330:04.34] Let's see internals of this
[330:08.52] Set private key, so I could just get rid of set private key and then it's instead
[330:15.10] I could do
[330:23.92] I
[330:25.92] Could do this little ditty, which it's a little bit weird
[330:42.84] But it suits my purpose as well for the time being
[330:48.22] So
[330:50.22] I just overwrite the get private key method
[331:08.50] Oops
[331:14.98] So
[331:16.30] Here's one of those things I was talking about. I'm gonna stash this
[331:18.78] I'm gonna go in here
[331:21.38] Paste what's in my paste buffer so that that's out of the way. I'm gonna move this up here, and then I'm gonna take these
[331:29.02] Out of my paste buffer again
[331:32.30] add that
[331:35.06] And then just
[331:37.50] Put the little F
[331:40.86] Gets - pop
[331:42.86] Get - HD, okay, so
[331:46.14] Where was that oh yeah, I was saying I just replaced this this is a little bit. It's a little bit weird
[331:52.78] It's not the normal way to do it
[331:54.98] but
[331:57.22] I'm just replacing the set private key
[332:03.62] With a
[332:08.58] Overwriting the get private key and the reason that I have a get private key is just to keep the private key hidden away
[332:15.62] So that it cannot be
[332:20.66] So that it cannot be reached
[332:23.94] By lookers on okay, so now
[332:33.14] See
[332:34.78] Set private oops get private key equals
[332:39.18] So it's probably a couple places where I did this wrong, so I'm gonna go check that real quick
[332:43.50] So get private key HTT get private key that looks right still
[332:50.10] Get private key
[332:52.74] that looks right I
[332:54.90] think it covered all the bases there, but
[333:00.66] Let me do this, okay, so 100%
[333:04.34] Something I did broke a test
[333:07.74] And I bet I know what actually
[333:11.14] Set private key so what we'd have to do here is
[333:16.82] Oh, yeah, this wants to have
[333:20.22] the private key
[333:23.22] throw an error if the size is incorrect and
[333:26.18] There is no set private key, so it's not going to do that
[333:30.46] I
[333:32.46] Wait
[333:39.74] Get status, okay, yeah
[333:46.10] Okay set private key
[333:58.62] All right, so that's that's kind of weird
[334:01.66] Yeah, I'm I'm a little bit better explain things when I'm not and it's not 3 a.m.
[334:11.26] All right, so I got rid of set private key and this really shouldn't have been a problem
[334:23.86] Because I'm just replacing it with whatever I need in order to get
[334:29.62] See that a weight doesn't need to be in a weight anymore
[334:35.20] Hmm I don't know why this would not be working
[334:40.62] Seems like it should work
[334:44.94] Very simple changes here
[334:47.86] proof by its proof by its
[334:50.74] I'll I'll
[334:53.38] The only thing about that that might not be the best is that it's gonna hang on to that memory reference, but
[334:59.74] that's
[335:03.14] Probably okay, and then next priv key next priv key
[335:06.54] Well how could how could this be failing
[335:14.06] Properly drive chain path let's check and see from master seed
[335:22.66] To
[335:24.66] Public key, I don't know what could possibly be going wrong here
[335:30.98] Delta
[335:36.42] I'm using Delta. It's supposed to mirror more the github style. So web install that dev
[335:42.74] For all of your developer tool needs
[335:47.14] slash Delta
[335:49.14] There you go
[335:51.58] linky-linky
[335:53.90] All right, so you tell me what's going on here I got rid of set private key
[336:00.78] And instead
[336:12.22] Oh, wait, I know why that didn't work. I know I didn't work. I know I didn't work
[336:16.78] Because then I have to get rid of all the places where I was using private key like this
[336:22.14] And then
[336:31.26] Let's see
[336:40.38] See
[336:42.38] Wipe private data, so then we have to do priv bytes equals
[336:49.94] Http.get private key
[336:53.94] Oops
[337:01.46] Priv bytes whoops secure race priv bytes
[337:08.94] And then
[337:10.94] We do hdkey.get private key
[337:19.38] Equals no
[337:36.66] This actually becomes if we have the function to get the private key, that's a little bit weird actually
[337:42.92] Let me
[337:47.82] So I need to undo part of this that that needs to stay
[337:54.02] So
[337:56.02] Let private
[338:09.38] Oops private key equals http.get private key
[338:16.42] Yeah, this is a little weird. I don't think I want to go down this route
[338:36.42] Yeah, I'm not gonna go down that route I think it's it's it's too weird
[338:43.94] I'm just gonna I think I'm just gonna undo that little bit. Okay, so we're not gonna completely remove subprivate key
[338:50.94] Yeah, so when I saw that dev me and a buddy of mine put it together
[339:10.82] We put it together because we do a lot of client work and stuff and
[339:15.42] It makes it easy, it's just it makes it
[339:20.78] it reduces
[339:23.90] documentation and explaining and and
[339:26.62] Yeah
[339:29.74] Subprivate key subprivate key subprivate key
[339:39.38] Let's get this test nothing crazy there
[339:43.46] Yeah, so
[339:53.26] If your eye twitches a little seeing programs recommend installing curl pipe into sh
[339:57.94] You might be too old or you might be too young
[340:02.02] So that's it's referenced in the FAQ
[340:07.66] but there are reasons why
[340:10.78] People said don't run. So here's the little FAQ bit. My mother told me not to run with shell pipes. There you go
[340:19.42] There you go
[340:21.42] There's a little FAQ for you
[340:40.62] It's not hard to return a different script one in ten requests but
[340:48.58] But this is the thing your your logic is completely flawed
[340:52.66] Because it's for anything that you download
[340:57.82] That same thing is true. There is nothing different
[341:03.14] About running an installer from any other source
[341:08.38] It's 100%
[341:11.90] Trust right all of the technical problems have been solved
[341:17.86] There are no technical issues here. The only issue left is trust and
[341:22.94] Again, I even you know, I say here trust matters. Don't use a pipe to shell from insecure sites or authors
[341:30.50] You don't trust so if it's not
[341:32.50] HTTPS which good luck finding a website that's not HTTPS that
[341:37.26] Anyone visits right?
[341:40.02] Except for probably some bank somewhere where they still have the employees using Windows XP
[341:45.70] But the win that the HTTPS is going to be there. So
[341:50.22] half of these old 90s
[341:53.38] Ideas, like I mentioned here. They're just they just don't apply anymore and then
[341:59.34] Yeah, if you if you don't trust the site then yeah, don't run it. Don't do it
[342:03.70] You know if you if you don't if you don't trust it, you can go
[342:08.22] Whoops, you can go let me pick pick back up Delta here. Hold on
[342:13.82] so let's go to Delta then you can just click on releases and
[342:17.98] Then you can say, okay. Well, what am I on? I'm on a Linux
[342:22.30] muscle
[342:25.02] X64 no, I'm looking for something that's arm. So we have any a
[342:28.82] Arch here. There we go. That's here you go. So here's your release boom
[342:34.42] All right
[342:36.38] So there's your there's your github release to exactly the download location, you know
[342:42.22] Grab it untie it put it in your path, right?
[342:45.50] so
[342:48.30] You know or just go to the just go to the website that's that's what that's what this does
[342:54.02] So yeah, if you don't trust me, don't use it
[342:56.26] simple
[342:59.18] I
[343:01.18] So interestingly this actually
[343:16.02] Set private key, right
[343:22.30] Interesting
[343:24.30] Interesting
[343:26.30] Interesting
[343:28.30] Interesting
[343:30.82] Interesting
[343:32.82] Interesting
[343:34.82] Interesting
[343:42.82] We have a problem here
[344:02.94] Because this didn't ever reject it. This didn't ever have that error
[344:06.70] So, why is the test passing
[344:30.30] Interesting
[344:32.30] Should throw an error if incorrect key size, but this actually
[345:00.26] Doesn't throw an error
[345:04.78] Throw an error
[345:06.78] So it seems like none of these rejects are actually working
[345:33.38] Or maybe they are I don't know just this one isn't working
[345:37.38] Why would this test pass it's obviously not throwing that error
[345:47.10] Because there doesn't exist anymore
[346:01.54] Yeah
[346:03.54] Hmm
[346:14.66] All right, I think I'm gonna call it a night. I'll trust you. Eventually. We just met a good answer sir. Good answer
[346:21.82] Yeah
[346:26.26] Well
[346:28.54] You know, I mean it's kind of like
[346:32.02] Same deal with all the other ones
[346:34.14] You know, you just check the stars on github. Does it have enough stars for you?
[346:39.96] Does it have enough forks
[346:43.90] Oh
[346:53.50] Okay, I don't think there's anything else that I can do and be productive at this point. I thought I was gonna remove that
[346:59.46] Well, maybe there's one more. There's always just one more. I gotta get some sleep though. I am so tired
[347:04.54] I'm gonna be so man tomorrow's gonna be the worst day ever. If I don't I
[347:10.14] Don't go to bed two hours ago
[347:13.18] When you're in a hole keep digging that's what I always say
[347:18.22] Just keep on digging till you get out on the other side it's the right thing to do
[347:28.82] All right, so we got the get private key
[347:31.26] Okay, get private extended key oh
[347:43.26] It's we could all right serialize sure I clean this one up a bit I can clean it up here, too
[347:53.90] You
[347:55.90] There's another branch where I was doing experimentations trying to figure out
[348:10.66] How to how to do stiff
[348:14.14] All right, and then I think the thing that I walked away with with this. Yeah. Okay, and this is still still the case here
[348:22.70] All right, my offset
[348:25.98] X-key size not 78. It's 74 and then I don't have to subtract from it
[348:34.86] That's the raw X key size, but all the same
[348:41.72] My offset we can just get rid of my offset
[348:45.44] And we're not gonna have version so we can just get rid of this
[348:49.78] Version bit and then I just have to think
[348:52.86] Subtract 4 on each of these lines my offset. So I said subtract 4 that's gonna be 1
[349:00.96] If I subtract 4 that's gonna be 5
[349:04.52] If I subtract 4 that's gonna be 9
[349:08.22] Let's subtract 4 that's gonna be 41
[349:19.30] I don't know from extended key, huh?
[349:23.52] This one's gonna be all sorts of wrong
[349:30.86] Okay, does this one have X key size
[349:43.80] Mama didn't raise no quitter
[349:45.80] Mama didn't raise no quitter
[349:53.44] My mama didn't raise no quitter, what is that from? I mean, I'm sure it's probably from a lot of things
[350:01.90] But I don't know
[350:12.56] All right, let's just run the test on this all right good test pass
[350:17.26] This would be
[350:25.24] Sure
[350:28.64] Remove unused
[350:31.88] Offset
[350:35.80] Serialize
[350:37.80] Serialize
[350:50.80] Okay serialize, okay remove removed and used
[351:04.56] All right again, this is gonna now be 0 this is gonna now be 1 this is gonna now be
[351:11.44] 5 I think these numbers are repeating
[351:15.48] Number 9 and 41. I remember those numbers and then 41 again
[351:21.50] And then 41 again
[351:24.92] And then I can get rid of all the dirty offsets that I had
[351:30.20] That I just kind of shimmed in there for a minute. Yay
[351:34.22] What does this function what's this function called?
[351:51.60] From extended key
[351:55.44] Yeah, that's not what I wanted to do make it stop
[351:59.86] Uh
[352:01.86] There we go
[352:04.02] All right little by little
[352:25.62] so now I
[352:28.70] Think this just is from seed. It doesn't need to be from master seed
[352:33.06] From extended keys or anything else that I want to well object wise
[352:38.86] Okay, so we got that the wipe private data. I don't think we really need that
[352:44.38] Okay, we've got
[352:51.10] Okay, drive child. We could move that out. That's fine
[352:55.06] So what what what instance methods do we have we got derived?
[352:58.90] And I think that derive is actually best not I
[353:03.42] Think this is where I would like derive to move in this way
[353:11.22] Where
[353:20.86] See whoops - HD
[353:24.50] There's create and then derive and I'd kind of like this to be called derive path
[353:36.00] Because we give it a key and a path and then we derive the path and
[353:42.86] Then that removes some some state stuff and then look
[353:49.50] Because of that
[353:51.50] We can get rid of these
[353:54.26] And I like that I like not having to have variables that have weird names
[354:01.30] Like this one here, and then I think we could do the same thing with the derived child, too
[354:08.82] So we could take
[354:14.54] I
[354:16.54] Could take both of these well first we need to fix the derived situation. So now the tests
[354:24.62] They're all gonna have all this derived stuff
[354:29.54] and
[354:32.18] Then I can just change that to
[354:34.18] - HD dot derive path
[354:38.22] And then do this and I should probably use the regular expression. So I just replace them all at once
[354:43.86] So, let's see
[354:45.86] I want to capture
[354:47.90] Dot derive and I want to capture whatever is from the non
[354:56.38] What do we call it
[355:00.54] There we go
[355:03.50] Want to capture all that just nice little Kirby symbol here and then I want to capture
[355:09.58] I
[355:11.58] Okay, and then I want to rename this to - HD dot derive path and then give it
[355:28.26] HD key and then whatever - is and then I'm gonna call that good
[355:33.70] So easy to read isn't it? Everybody loves regular expressions
[355:38.94] Nobody's ever been confused by a regular expression before
[355:41.74] Everybody knows that
[355:44.66] They're the easiest thing in the world
[355:48.10] Confused by regular expression, you know, that's unheard of
[355:54.78] Oh, whoops, what did I do wrong?
[356:06.74] Okay
[356:08.74] HD key not derive something. How do I match all those other ones?
[356:19.78] Regular expressions
[356:31.78] I
[356:33.78] Okay, HD key dot derive, right, okay
[356:52.06] Okay, let me check comments here. I'll leave you here. Happy coding and sleep tight when you eventually give in. Thanks
[357:00.70] F
[357:02.70] Dot blah does not match
[357:05.26] Hmm W plus
[357:08.22] Wait, hold on
[357:11.06] W plus
[357:13.50] Dot derive. Oh the dot was it the dot?
[357:18.54] Oops, there we go
[357:25.82] Oh
[357:27.82] Oh, yeah, yeah, yeah f dot path. Gotcha. Thank you. Thank you. Just put a little bit of this in here
[357:44.86] Little bit of that in there. Do I need to escape these two? Do we just escape all the things?
[357:54.42] Here we go
[357:56.42] All right, so now
[358:03.06] got - HD
[358:05.14] dot derive path
[358:07.54] This one that one
[358:09.86] Like that. Yeah
[358:12.62] Winner winner chicken dinner. Oh wait. Nope that didn't work out very well because
[358:19.74] Gotta put the closing bracket on there or closing for M
[358:23.10] Okay
[358:39.14] Heyo
[358:45.90] Thank you
[358:47.78] Much appreciated and you know come back again sometime when I'm not so tired, you know, I'm saying
[358:52.54] It's tough, but you have a good one
[359:16.02] All right ref
[359:18.02] Move dot derive
[359:21.46] To - HD dot derive path
[359:28.52] Adios to God with you and the more common parlance
[359:41.82] Adios to God with you and the more common parlance
[359:43.82] See you don't expect that but that's literally what it means
[359:53.36] Adios to God with you. It's kind of like to hell with you, but more polite way more polite
[360:05.26] Kind even
[360:09.14] Something people like to hear
[360:11.48] them say
[360:14.48] Hmm
[360:16.48], hmm
[360:46.48] Oh
[360:48.48] This was the only function I was supposed to comment out back in those days, I think
[361:00.24] Yeah, I know setpublickey is not a function. Oh, okay, nevermind
[361:02.24] Yeah, I know setpublickey is not a function. Oh, okay, nevermind
[361:26.96] Yeah
[361:28.96] Working as intended
[361:32.20] I
[361:34.20] I
[361:36.20] I
[361:38.20] I
[361:40.20] I
[362:09.08] Huzzah move two more, remove two more dependencies
[362:13.42] I
[362:15.42] I
[362:17.42] I
[362:19.42] I
[362:47.62] Wait, what's node version am I on right now? Okay good 18
[362:51.72] All right, what have I got left here I
[363:09.34] Want to get derive child?
[363:13.82] I'd rather call it something like derive index. I'm not really sure but
[363:17.20] - HD
[363:35.86] - HD
[363:37.86] - HD
[363:39.86] - HD
[363:41.86] - HD
[363:43.86] HD key
[363:56.62] Oh
[363:58.62] Whoops what am I doing?
[364:14.58] Okay
[364:16.58] Okay derive
[364:32.78] Oh
[364:34.78] Oh
[364:36.78] Oh
[364:38.78] Oh
[364:40.78] Oh
[364:42.78] Oh
[364:44.78] Oh
[364:46.78] Oh
[364:48.78] Oh
[365:17.70] Whoops
[365:19.70] Oh
[365:48.18] Okay
[365:50.18] All right, keep on trucking right along
[366:15.84] Okay, no matter how many of these there are
[366:17.92] Important bit is that this
[366:23.52] Okay, so this right here that's kind of important
[366:43.72] What
[366:45.72] I
[366:47.72] I
[367:16.88] 279 what's going on 279?
[367:18.88] Oh derive is gone, right
[367:30.40] Okay
[367:32.40] Okay, drive drive drive drive drive
[367:57.20] Drive
[367:59.20] Okay, good all the tests are still passing all right drive child then here we come I
[368:18.64] Think there's only one reference to drive child and it's that one there and this is awesome because
[368:27.68] We get to pull this up and then drive child becomes part of the public API, which is where I want it
[368:34.00] Okay, so then we take all of this with us
[368:50.88] That's great
[368:52.88] That's great
[368:54.88] That's great
[368:56.88] That's great
[369:18.24] Oh
[369:20.24] Right, so then what we need to do to let
[369:31.22] Product key equals HT key dot get
[369:42.72] Priv key
[369:47.36] HT key
[369:49.36] There we go
[369:52.88] And then what
[369:55.40] And then everything's happy, of course
[370:02.68] All right HT derive
[370:04.68] All right HT derive
[370:20.60] And
[370:22.60] Then the first parameter of course is going to be HT key and HT key
[370:44.64] HT derive
[370:50.48] Child
[370:52.48] Whoops yes, I do I
[371:05.76] Do mean get private key there we are
[371:11.32] All right - HD
[371:15.44] - HD
[371:17.44] Derive child
[371:23.32] And then we just take this - HD dot drive child HD key
[371:29.96] Now
[371:36.72] See
[371:40.72] You
[371:42.72] Can we call it parent parent key
[371:59.34] And it's a little bit easier to
[372:10.36] Deal with
[372:12.36] Yeah, let's call all that underscore stuff let's just call it child key
[372:25.04] And then all of the non underscore stuff, let's call that
[372:39.60] whoops
[372:41.60] Parent key
[372:44.36] Hmm I don't like that that went on to the next line, but I don't know what to do about it
[372:55.16] Maybe it's a parent key just parent
[373:03.12] You
[373:05.12] It's not solved my problem it does solve my problem
[373:13.80] And then instead of child key we could just call it child, I mean it is kind of apparent that it is a key I
[373:23.16] Don't think there's gonna be any other use of that here and then derive path
[373:32.28] We could call this HD key is just parent
[373:36.80] That's HD key sure but
[373:46.08] Kind of like the idea
[373:55.16] I'm saying okay
[373:57.80] return parents
[374:01.00] Whoo highlighted in yellow, that's not good
[374:03.48] So this is it is a little bit difficult
[374:30.04] Because
[374:32.04] We could say
[374:35.56] Well this is now a child, but then
[374:41.22] That's a child so you're passing in a child so you pass in a parent, so this is what it should read like
[374:49.24] Parent
[374:58.00] This is one of those things where recursion might make the most sense
[375:01.98] But I don't know you don't need to keep any of this stuff around really
[375:08.24] It's just logically
[375:13.32] You just well you'd be splitting over and over again you could pre split the paths and
[375:21.48] Then you could do this recursively, and you're only gonna do it a few times
[375:26.64] so
[375:28.64] Because right here a parent and a child are the same thing
[375:34.60] But you never use the parent so maybe it's just as well to call it HD key and that's that I
[375:42.44] Guess that's fair
[375:48.92] Because you never reference the original
[375:51.92] That was part of why I wanted to move it out was so that the original isn't a reference this one
[375:56.28] There's a much more clear parent-child
[375:58.28] Relationship because you need the parent and the child at the same time this one
[376:01.52] You don't need the parent the child the same time because all that is moved into the derive child
[376:06.24] Where you do pass in the parent, and then I don't know why this needs a child index
[376:13.96] Because at that point well
[376:19.08] Seems like it's all the same
[376:22.16] Okay, so
[376:24.16] The only time drive child was ever called was from Drive path
[376:30.84] So, but this is where I kind of wanted this to be a an update
[376:49.84] Let's see what which one of these so drive child. What is drive child really saying?
[376:54.52] Drive child is saying hey update this
[376:58.16] with this index it is definitely
[377:01.20] More incremental because you're exposing whether or not it's hardened
[377:13.84] I
[377:15.84] Think that's that's a little bit easier in some ways, so okay. Let's let's reconsider drive path for a minute so drive path
[377:30.76] you
[377:32.76] Okay, could I make this an update function and then have a digest function on what it returns
[377:50.60] That's kind of what I want
[377:58.36] And also
[378:00.36] Dang it what did I call it in the other one? I had some name rather than from master and from extended key
[378:10.68] I called it something else
[378:12.68] Set seed
[378:24.24] And I'd moved that internal
[378:26.24] But now I'm doing the opposite. I'm moving things external which is kind of what I want to do
[378:30.92] Okay, so I create it
[378:35.20] Update it I
[378:39.56] Could keep with that
[378:42.40] Okay, well
[378:53.80] Think I need to get some sleep and consider anything else tomorrow
[378:58.36] All right, so we got the fingerprint we got to create wait I had fingerprint get up here
[379:08.76] But that's not right
[379:15.16] I
[379:17.16] I
[379:19.16] I
[379:21.16] I
[379:23.16] I
[379:25.16] I
[379:27.16] I
[379:29.16] I
[379:31.16] I
[379:33.16] I
[379:35.16] I
[379:37.16] I
[380:06.56] Let's see how this goes
[380:08.56] the
[380:37.08] All right, so we're gonna drive child
[380:39.08] And we got a drive child drive child drive path hey actually did a good job this time
[380:57.32] Did an excellent job this time Wow get I'm impressed you really knocked it out of the park
[381:06.72] a
[381:08.72] Move all that derived child stuff up removed the
[381:34.28] Fingerprint stuff down so basically I'm gonna go with if the test pass it's good hmm could not find biggie
[381:49.72] Oh
[381:51.72], oh
[382:09.72] Oh
[382:11.72] Wait a minute what's going on here something's wrong
[382:26.96] Oh
[382:28.96] Oh
[382:30.96] Oh
[382:32.96] Oh
[383:02.12] Simplify fingerprint
[383:05.12] Fire
[383:07.12] Fire
[383:09.12] Fire
[383:11.12] Fire
[383:13.12] Fire
[383:15.12] Fire
[383:17.12] Fire
[383:19.12] Fire
[383:21.12] Fire
[383:23.12] Fire
[383:25.12] Fire
[383:27.12] Fire
[383:29.12] Fire
[383:31.12] Fire
[383:33.12] Fire
[383:35.12] Fire
[383:37.12] Fire
[383:39.12] Fire
[383:41.12] Fire
[383:43.12] Fire
[383:45.12] Fire
[383:47.12] Fire
[383:49.12] Fire
[383:51.12] Fire
[383:53.12] Fire
[383:55.12] Fire
[383:57.12] Fire
[383:59.12] Fire
[384:01.12] Fire
[384:03.12] Fire
[384:05.12] Fire
[384:07.12] Fire
[384:09.12] This is weird
[384:11.12] Fire
[384:13.12] Fire
[384:15.12] Fire
[384:17.12] Fire
[384:19.12] Fire
[384:21.12] Fire
[384:23.12] Fire
[384:25.12] Fire
[384:27.12] Fire
[384:29.12] Fire
[384:31.12] Fire
[384:33.12] Fire
[384:35.12] Fire
[384:37.12] Fire
[384:39.12] Fire
[384:41.12] Fire
[384:43.12] Fire
[384:45.12] Fire
[384:47.12] Fire
[384:49.12] Fire
[384:51.12] Fire
[384:53.12] Fire
[384:55.12] Fire
[384:57.12] Fire
[384:59.12] Fire
[385:01.12] Fire
[385:03.12] Fire
[385:05.12] Fire
[385:07.12] Fire
[385:09.12] Fire
[385:11.12] Fire
[385:13.12] Fire
[385:15.12] Fire
[385:17.12] Fire
[385:19.12] Fire
[385:21.12] Fire
[385:23.12] Fire
[385:25.12] Fire
[385:27.12] Fire
[385:29.12] Fire
[385:31.12] Fire
[385:33.12] Fire
[385:35.12] Fire
[385:37.12] All right, get rebase continue.
[385:48.24] And do the test still pass?
[385:50.04] No, they don't.
[385:52.40] But it's probably because let's see here.
[386:17.68] So we move to arrive, drive child, we got drive, child, drive child, drive path, okay.
[386:30.34] And then let's take a look at the tests.
[386:31.90] Where are our drives now?
[386:34.90] Drive path, drive path.
[387:00.66] All right.
[387:01.66] So let's go ahead and just drop this for a second.
[387:07.70] The test pass, they do.
[387:09.74] Okay.
[387:10.74] Let's put it back in and then let's just kind of take a look at reset.
[387:24.10] What's going on here?
[387:27.30] So we move to arrive child up there and all right, what's failing in the test here?
[387:37.34] It's just failing in a really weird way.
[387:41.54] I expect to arrive child to be the culprit, drive path, is there any drive path that doesn't
[387:51.50] have async on it?
[387:52.50] No, they've only got async on them.
[387:54.54] All right.
[387:55.98] What's going on?
[387:56.98] From master scene, I could create it and then when the first time updates called, have it
[388:23.34] do what it needs to do to set the seed if it's not been set.
[388:28.46] So have it do it's init on update and then digest.
[388:33.22] I do want to take a look at, I do want to see what that ends up looking like, but not
[388:38.18] right now.
[388:39.18] Right now I just want to get this, get this passing again and then I'm off to sleep.
[388:46.50] Okay.
[388:50.22] Implicitly has any type, blah, blah, blah, blah, blah.
[389:09.88] Okay.
[389:10.88] test, the tests, they all have the right thing here.
[389:34.88] Drive path, drive path, drive path, master key, HD key, key instance.
[389:49.40] Okay.
[389:52.00] Let's just, uh, all right, let's test.
[389:54.82] Let's test the test real quick.
[390:15.86] So the way that we're going to test the test is by, we're just going to create a method
[390:36.90] and we're going to put it right up here and we're just going to call it dash HD dot drive
[390:46.86] path.
[390:47.86] And it's going to be async and it's going to do return away, HD key dot drive path.
[391:02.10] So we're going to take in HD key and a path and we're going to drive the path and we'll
[391:09.82] do the same thing for drive child as we'll just call on here, drive child and then index
[391:34.42] and PM run tests.
[391:42.06] Okay, cool.
[391:43.58] So the dummy passes.
[392:02.26] Okay.
[392:27.10] Okay.
[392:47.02] I wonder if it's a legal keyword here.
[392:50.30] Nope.
[392:51.30] That don't work.
[392:52.30] Okay.
[392:53.30] All right, again, pass this great dash HD.
[393:20.82] Okay.
[393:24.54] Drive child, dash HD, drive child, HD key.
[393:48.86] And then let private key equals HD key dot get private key.
[394:10.42] Dash HD, drive child, HD key index.
[394:33.26] Oh, cool enough, all right, drive.
[394:45.98] This now becomes drive path, drive a full HD path from the given key, which I think
[394:55.30] that's an important distinction.
[395:11.06] Okay, get the next child X key in the path segment.
[395:37.50] And there's the helper HD derive path, again, HD key in here, HD key, and then, where is
[396:04.30] it?
[396:08.30] Okay, here we go.
[396:15.54] So we've got the create, we've got the derive.
[396:37.62] Oh, I think I know what was happening.
[397:07.02] I think it was in this infinite loop here, because that's what would happen.
[397:13.58] It's probably just a typo, missing argument or something.
[397:18.30] All right, there we go.
[397:24.06] Anyway, test, drive child, dash HD.
[397:33.34] Cool.
[397:37.42] All right, everything's back up here again.
[397:53.22] Drive path, drive child, and then, oh nice, this create is so, so small.
[398:15.46] Oh, this is nice, oh my goodness.
[398:24.46] So you could, well, I'm just gonna leave this for now.
[398:39.74] I'm out.
[398:40.74] My brain is too small, I need sleep.
[398:45.90] All right, so yeah, pretty much all the way there.
[398:57.54] Just the tiniest amount left to do to turn those public key functions basically into
[399:04.54] digest functions.
[399:06.42] I'm not really sure what to do about that wipe private data.
[399:13.38] I think we might be able to just get rid of that, because I don't know when you would
[399:17.46] use it.
[399:19.70] I don't know where it was last used, but it seems to be gone now.
[399:31.18] Secure erase, is there any other place where secure erase is used?
[399:34.66] No.
[399:35.66] I mean, we could leave a wipe private data or something, but I just don't know why you
[399:45.38] would do that, because you just, because the idea is that you have a private key, but you
[399:50.50] want to turn it into a public key, or I don't know, I just don't know exactly what the use
[399:56.38] case is there.
[399:57.38] But I'm going to think on this a little bit, because the last little bit for this relies
[400:03.70] on the fact that private key is truly private state, and I got to think about this just
[400:10.42] like what I did with the, over in the dash TX, where, oh, but look at this now, look
[400:19.10] at this now.
[400:21.90] Look at that.
[400:25.10] It's so easy to see what the properties are and whatnot, you know?
[400:32.06] So we could just add hdkey.update, hdkey.digest, I like that a lot, and the digest should return
[400:43.66] either both the private and public keys, or it should return, and then the update, yeah,
[400:48.82] you just pass the update with, I like this a lot, I like this a lot a lot.
[400:57.30] So I'm going to have to think about it.
[401:14.98] Oh, and I was going to say, something about the block TX and the private key, because
[401:21.54] originally there, well I wanted to have some method by which the private key wouldn't get
[401:27.42] put out in logs and error message and stuff like that.
[401:30.42] And I want that same thing here, and right now we have it.
[401:35.02] But I don't know if I want to keep it this way or not, I think maybe we will.
[401:39.70] I think maybe we'll just change the name of a couple of these things, but basically the
[401:42.78] only thing that needs to be here is whatever's managing the private state.
[401:46.94] And then there is some, there is some stuff to do actually with moving the from seed.
[402:01.18] Because basically, yeah, we need a way to be able to, well I guess we can't, yeah I'm
[402:15.50] just going to sleep on it.
[402:16.50] It's going to be good.
[402:17.50] Alright, anyway, y'all have a good one, again I can't raid because the channel's not old
[402:21.70] enough, but when we get there we will, adios!