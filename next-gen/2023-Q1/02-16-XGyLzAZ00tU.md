---
showLink: "https://www.youtube.com/watch?v=XGyLzAZ00tU"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Code Hangout: Next-Gen DASH Tools #19: Dash HD: Docs, Docs, Docs & Publish"
publishDate: "2023-02-16"
coverImage: "https://i.ytimg.com/vi/XGyLzAZ00tU/maxresdefault.jpg"
---

## Episode Description

This episode covers the development of Dash HD, focusing on documentation, code updates, and preparing for publication.

## Episode Summary

In this code hangout session, Joe Neal works on updating and refining the documentation and code for Dash HD, a reference implementation of BIP 44. He focuses on creating a clear README with usage examples, a quick start guide, and a detailed walkthrough. Throughout the session, Joe iterates on the code structure, improves error handling, and discusses various implementation details. He also touches on some personal frustrations with community management and communication challenges.

## Chapters

00:00 - Introduction and Project Overview

Joe Neal introduces the session, mentioning that they'll be working on Dash HD, a reference implementation of BIP 44. He explains that the focus will be on documentation and preparing for publication. This chapter sets the context for the work to be done and highlights the importance of creating clear, user-friendly documentation for the project.

05:25 - Structuring the README and Quick Start Guide

Joe begins work on structuring the README file, focusing on creating a quick start guide. He discusses the importance of providing clear, concise information for users to get started quickly. The chapter covers the process of organizing information, deciding what to include in the quick start section, and how to present code examples effectively.

21:31 - Refining Code Examples and Error Handling

This chapter focuses on refining the code examples in the documentation. Joe works on improving the error handling in the code, discussing the importance of accounting for edge cases such as invalid derivation paths. He also explains the reasoning behind certain code structures and how they contribute to the robustness of the implementation.

47:23 - Community Management Challenges

Joe takes a brief detour to discuss some challenges he's facing with community management, particularly around a Meetup group transition. This chapter provides insight into the non-technical aspects of managing an open-source project and the communication challenges that can arise.

64:05 - Walkthrough Development and API Documentation

Returning to the main task, Joe begins work on a detailed walkthrough section for the documentation. He discusses how to break down the code examples and explanations to make them more accessible to users of varying experience levels. This chapter also covers the process of documenting the API, ensuring that all functions and their usage are clearly explained.

95:26 - Final Touches and Documentation Structure

In the final chapter, Joe works on structuring the overall documentation, ensuring that it flows logically from basic usage to more advanced topics. He discusses the importance of layering information, allowing users to find the level of detail they need. The chapter also covers some final tweaks to code examples and explanations to improve clarity.

133:43 - Wrapping Up

Joe concludes the session, reviewing the progress made on the documentation and code updates for Dash HD. He summarizes the key improvements and discusses next steps for the project.

## Transcript

[00:00] you
[00:02] you
[00:04] you
[00:06] you
[00:08] you
[00:10] you
[00:12] you
[00:14] you
[00:16] you
[00:18] you
[00:20] you
[00:22] you
[00:24] you
[00:26] you
[00:28] you
[00:30] you
[00:32] you
[00:35] you
[00:37] you
[00:39] you
[00:41] you
[00:43] you
[00:45] you
[00:47] you
[00:49] you
[00:51] you
[00:53] you
[00:55] you
[00:57] you
[00:59] you
[01:01] you
[01:03] you
[01:05] you
[01:07] you
[01:10] you
[01:12] you
[01:14] you
[01:16] you
[01:18] you
[01:20] you
[01:22] you
[01:24] you
[01:26] you
[01:29] you
[01:31] well hello hello and welcome back I'm a Joe Neal and we are doing some
[01:57] - incubator live code so we're gonna be we're gonna be doing a bunch of minutia
[02:04] today I'm not gonna lie it's gonna be little detail oriented stuff and
[02:11] publishing hopefully hopefully that's the goal here is actually get some
[02:15] stuff published but what we have is - HD which I've been working on for way too
[02:22] long but the result is that hey we've got a reference implementation now of
[02:30] BIP I actually need to update this to say BIP 44 not just BIP 40 32
[02:49] let's see - - - anyway actually I'm gonna take one more one more second here one
[02:58] more second here just okay actually I'm we're gonna we're gonna open the
[03:22] Mountain Dew first I need to get my I need to get the juices flowing so here's
[03:26] a little here's a little pep talk from mr. Mountain Dew right here oh that's
[03:37] good that's a good pep talk I can tell that's gonna help us out a lot okay all
[03:42] right let me get back in focus focus all right so what I've been doing is kind of
[03:49] documenting I'm trying to find the right the way to to go about this
[03:53] documentation is really hard so we want we want to kind of give the person the
[03:57] sense of hey this is what this does and I think that having this preview up here
[04:05] is a good first step let's see and then I'm gonna add a quick start so we're
[04:15] gonna maybe replace this usage with something that feels a little more
[04:20] quick-starty I'm gonna finish off the documentation for the API and the types
[04:26] which I think it's pretty much done at this point actually I had my I had my to
[04:30] do's and a little to do here hold on just one second let me bring that up I'm
[04:35] not firing on all cylinders yet
[04:39] Oh
[04:41] okay
[04:44] okay so we're gonna do the quick start we got to update the links we got to
[05:14] update the tests we got to add the glossary we had to remove the old junk
[05:17] okay let's do it in that order like I've got there so first we're going to go to
[05:26] quick start see one typical use for the wallaboo use multiple accounts this will
[05:51] focus on the most typical use case
[05:58] whoops actually let me change this to bit 44
[06:15] dang it
[06:43] we have bit 32 here bit 44 also should have bit 43 HD path is defined by bit
[06:53] no purpose purpose and the HD path is divided defined by bit 33 okay quick
[07:02] start
[07:04] where you intend to generate multiple addresses during the lifetime of your
[07:26] program okay
[07:37] as part of your applications lifecycle I think how do we in programming is
[07:55] lifecycle one word or two words life cycle I think it might just be
[08:01] lifecycle yeah lifecycle in programming is one word I think lifecycle yep I'm
[08:12] gonna add that to spell see I just do colon spell and then I add lifecycle and
[08:20] now it's not gonna bug me about it anymore lifecycle is one word in
[08:23] programming
[08:26] just another second here and responding to a message real quick
[08:55] Oh
[08:57] okay
[09:25] you'll generate let's see what's up here browser and okay so we'll have a
[09:49] small usage section this is too big
[10:13] okay let's actually we'll slim this down then we'll move this into the quick
[10:21] start
[10:23] and see
[10:32] okay
[10:35] you
[10:37] okay
[11:03] note no let's move down here okay so make a little use this section okay
[11:15] notes sec p256 k1 there are multiple options
[11:31] note
[11:34] let's do this
[11:44] a default plug-in the default configuration expects to to to to as
[12:04] the sec p256 k1 implementation this is not is not not a listed dependency as it
[12:26] is very easy to replace see
[12:40] dang it - keys it's doing that thing again where it's for some reason - keys
[13:10] - phrase - keys
[13:16] - phrase
[13:28] [ Background Sounds ]
[13:46] Recommended but not strictly required.
[13:51] [ Background Sounds ]
[14:16] There we go.
[14:24] Okay. Is a direct dependency which requires you to provide,
[14:37] I don't know how to say this, I'm not going to worry about it.
[14:41] Leave it as is, good enough.
[14:51] Since there are many, I got this, I got this,
[14:57] many Secp256k1 implementations that you might want to choose
[15:07] from for various reasons.
[15:10] Dash keys, let's see.
[15:24] [ Background Sounds ]
[15:38] And package.json for this.
[15:43] However, the default configuration will work
[15:58] by default if, da, da, da, da, is available, is available.
[16:09] It is easy, there are just a few, it's easy to replace
[16:31] with another implementation, C dash keys.
[16:37] There we go, that's it.
[16:38] That's the way to phrase it.
[16:39] [ Background Sounds ]
[16:54] For more info.
[16:56] [ Background Sounds ]
[17:22] You can work with bare seeds, non-passphrase,
[17:37] non-bare seeds without a word list.
[17:43] There we go.
[17:45] [ Background Sounds ]
[18:15] Let's see, because there are many implementations,
[18:24] many decent implementations to choose from.
[18:31] [ Background Sounds ]
[18:41] Oops. However, we'll use, do, do, do, do, do,
[18:56] by default if it is, if it is installed.
[19:04] [ Background Sounds ]
[19:17] If you'd prefer a different implementation, C. There we go,
[19:25] that's it.
[19:26] [ Background Sounds ]
[19:32] That's the one.
[19:33] [ Background Sounds ]
[20:03] Yeah.
[20:04] [ Background Sounds ]
[20:20] If you prefer to use another implementation.
[20:25] [ Background Sounds ]
[20:30] Good, this is great.
[20:33] All right, so install notes are updated, back to the quick start.
[20:37] [ Background Sounds ]
[20:55] HD wallet quick start.
[20:58] [ Background Sounds ]
[21:06] If your user does not have a passphrase mnemonic,
[21:14] you can generate one for them with dashphrase.
[21:22] [ Background Sounds ]
[21:30] Let words equals dashphrase dot, and then I need to figure out,
[21:38] how is it that I use dashphrase again?
[21:42] [ Background Sounds ]
[21:49] Generate.
[21:51] [ Background Sounds ]
[21:53] There we go.
[21:54] [ Background Sounds ]
[21:58] Word list, let's do this, let target entropy equals 128.
[22:06] [ Background Sounds ]
[22:10] Dashphrase dot.
[22:11] [ Background Sounds ]
[22:16] Target bit entropy.
[22:19] [ Background Sounds ]
[22:34] Let's see if there's another word list in the test vectors
[22:38] that is an all right one to use.
[22:43] Ryan had mentioned concern about people not understanding
[22:51] that it's supposed to be random.
[22:52] [ Background Sounds ]
[23:12] Hamster diagram, private dash, oh, that's too long, too long.
[23:16] [ Background Sounds ]
[23:22] Let's just pull something from the test vectors that's one
[23:26] of the shorter ones like this, vessel, ladder, sibling, chat,
[23:31] sunglass, valve, picture, meh, cat, swing, flag, there we go,
[23:40] that we could use that one perhaps, train,
[23:42] these are all pretty easy words, scheme,
[23:47] and that one starts out ozone, yeah.
[23:50] Some of these just start out a little too wonkadoodle.
[23:57] [ Background Sounds ]
[24:04] Okay, zoo is good, letter advice cage absurd amount,
[24:10] and then that starts repeating, so I don't really want
[24:13] to use that one, I want to use one that looks random
[24:16] but it's part of the test vectors, okay, good enough.
[24:19] Oops, and then train needs to go back there, okay, good.
[24:36] Okay, if you're using a pass, although not strictly necessary,
[24:49] let's see how to say this, you need a seed.
[24:57] Wallets are derived from a seed.
[25:07] A seed is typically derived from a passphrase mnemonic.
[25:18] Let's see here.
[25:29] [ Background Sounds ]
[25:40] If your user doesn't supply a passphrase mnemonic,
[25:58] you can generate one.
[25:59] If your user, oh, you, let's see.
[26:17] [ Background Sounds ]
[26:32] We, yeah, we don't actually use the secret.
[26:47] You can combine, you can generate a seed
[26:56] from a passphrase and a secret, typically blank.
[27:16] Although the secret is typically left as an empty string.
[27:27] So, here we go.
[27:34] [ Background Sounds ]
[28:00] Let's see, for convenience, we'll use the zoomonic
[28:11] from the test vectors.
[28:19] [ Background Sounds ]
[28:48] Okay.
[28:49] [ Background Sounds ]
[29:19] Let's see.
[29:19] [ Background Sounds ]
[29:32] For the purpose of this demo, we'll use a word list.
[29:44] I don't know how to say this.
[29:45] Okay.
[29:48] [ Background Sounds ]
[30:16] There we go.
[30:18] [ Background Sounds ]
[30:35] Let's see, BIP, what was this, BIP 39?
[30:41] [ Background Sounds ]
[31:01] Okay, five.
[31:02] [ Background Sounds ]
[31:32] For our demo passphrase, we'll use the zoomonic.
[31:49] One of the BIP 39 test vectors.
[31:58] [ Background Sounds ]
[32:15] Okay.
[32:16] [ Background Sounds ]
[32:23] Demo secret.
[32:25] [ Background Sounds ]
[32:39] Typically, the secret is left as an empty string.
[32:47] [ Background Sounds ]
[32:52] Okay, we'll just go with the empty string.
[32:54] That's fine.
[32:54] [ Background Sounds ]
[33:24] Let's see.
[33:25] [ Background Sounds ]
[33:34] Let's see.
[33:36] [ Background Sounds ]
[34:07] [ Background Sounds ]
[34:17] Okay, I'm just -- words are so hard.
[34:22] All right, wallet, a wallet is derived from a seed.
[34:30] A seed is typically derived from a random mnemonic passphrase.
[34:37] [ Background Sounds ]
[34:45] Generate one.
[34:46] [ Background Sounds ]
[34:55] For this demo, we'll use the zoomonic.
[35:05] Passphrase, our passphrase, mnemonic.
[35:18] [ Background Sounds ]
[35:31] For demos, testing demos and debugging.
[35:35] [ Background Sounds ]
[35:47] Okay.
[35:49] [ Background Sounds ]
[36:02] And secret salt.
[36:05] [ Background Sounds ]
[36:14] I don't know if I like that there.
[36:16] [ Background Sounds ]
[36:23] Okay, let's just go with that.
[36:25] [ Background Sounds ]
[36:39] Typically, the secret salt is left as an empty string.
[36:49] [ Background Sounds ]
[36:56] Kind of deprecated.
[36:57] [ Background Sounds ]
[37:21] Okay, let's see here.
[37:24] For this demo, we'll use however.
[37:28] [ Background Sounds ]
[37:44] For the purpose of this demo, we'll use values specified by the BIP 39 test suite.
[38:01] [ Background Sounds ]
[38:16] The zoomonic and secret.
[38:20] [ Background Sounds ]
[38:32] These values are specified by the BIP 39 test suite.
[38:36] For demos, debugging, et cetera.
[38:43] There we go.
[38:44] That's the way I want to phrase it.
[38:45] I'm trying to keep things on one line.
[38:48] It's just you read one line, you read one line.
[38:51] [ Background Sounds ]
[39:10] There we go.
[39:11] Yeah. Okay.
[39:15] Let secret salt equals treasure.
[39:19] [ Background Sounds ]
[39:26] Good.
[39:28] [ Background Sounds ]
[39:48] If you generate -- oh, I meant to say something here.
[40:05] [ Background Sounds ]
[40:26] I don't remember what it was.
[40:28] I had some thought last night, but I can't remember what I was going to do.
[40:31] Okay. So, if you generate a word list on behalf -- well, let's just go here.
[40:43] [ Background Sounds ]
[40:53] Use the passphrase and secret are used with a PB -- PBKDF2 variant.
[41:12] [ Background Sounds ]
[41:23] Expanded into the seed via PBKDF2.
[41:31] It's a specific -- what do we call it -- configuration of PBKDF2 under the hood.
[41:50] Key expansion is used to derive the seed from the passphrase plus secret.
[42:05] [ Background Sounds ]
[42:32] Let's see.
[42:33] [ Background Sounds ]
[42:43] Okay. Seven.
[42:45] [ Background Sounds ]
[42:51] A BIP32 key expansion, a different key expansion defined by BIP32.
[43:07] [ Background Sounds ]
[43:25] Stop. At this point, you should prompt the user to backup their --
[43:34] [ Background Sounds ]
[43:38] Okay. Prompt the user to backup their passphrase and/or seed.
[43:53] [ Background Sounds ]
[44:03] If they lose -- let's see, passphrase -- or seed, if no passphrase.
[44:21] [ Background Sounds ]
[44:28] User should backup their passphrase.
[44:33] [ Background Sounds ]
[44:47] Dang it. How do I get this to work?
[44:49] [ Background Sounds ]
[44:56] It's really important for the user to have -- no.
[45:01] The user should backup their passphrase or seed if no passphrase.
[45:06] [ Background Sounds ]
[45:35] It's common to print out passphrase.
[45:57] Passphrase.
[46:08] [ Background Sounds ]
[46:14] Unrecoverable.
[46:16] [ Background Sounds ]
[46:20] Okay.
[46:22] [ Background Sounds ]
[46:33] Part one, passphrase, secret, seed.
[46:41] There we go.
[46:44] Ah, here we go.
[46:49] [ Background Sounds ]
[46:57] A passphrase or seed is the wallet.
[47:06] [ Background Sounds ]
[47:19] Ah, I think this will be better.
[47:21] [ Background Sounds ]
[47:25] Okay.
[47:27] [ Background Sounds ]
[47:36] Okay. I think this will do well.
[47:38] Whoops. That didn't work out at all, actually.
[47:42] [ Background Sounds ]
[47:47] All right. There we go.
[47:48] [ Background Sounds ]
[47:54] Here's the -- from a code perspective --
[48:00] [ Background Sounds ]
[48:09] Okay. Stop.
[48:10] Prop the user make a backup at this point.
[48:12] [ Background Sounds ]
[48:17] Good. Here we go.
[48:18] And then part two.
[48:19] [ Background Sounds ]
[48:21] Part two.
[48:22] [ Background Sounds ]
[48:29] Wallet account X key.
[48:34] [ Background Sounds ]
[48:36] There we go.
[48:38] [ Background Sounds ]
[48:41] If the passphrase is lost --
[48:52] [ Background Sounds ]
[49:07] Make a backup.
[49:09] [ Background Sounds ]
[49:24] Passphrase.
[49:25] There we go.
[49:26] [ Background Sounds ]
[49:39] Passphrases.
[49:39] [ Background Sounds ]
[49:58] You're not implementing.
[49:59] [ Background Sounds ]
[50:03] Let's see. Can we do it this way?
[50:04] Passphrases.
[50:05] Okay.
[50:07] [ Background Sounds ]
[50:16] It's common to print this out and put it in a safe.
[50:22] [ Background Sounds ]
[50:32] Lost forever.
[50:34] [ Background Sounds ]
[50:39] And all money inside.
[50:41] [ Background Sounds ]
[51:05] All right.
[51:07] [ Background Sounds ]
[51:12] Okay. If the passphrase is lost, the wallet --
[51:13] [ Background Sounds ]
[51:18] And all money is unrecoverable.
[51:19] Great.
[51:20] [ Background Sounds ]
[51:25] Part two.
[51:27] [ Background Sounds ]
[51:39] Let's see. What did I save here?
[51:40] I want to make it similar.
[51:41] [ Background Sounds ]
[51:46] Maybe I do need to have a separate usage section.
[51:48] Oh, what did I get here?
[51:53] Notification.
[51:55] [ Background Sounds ]
[52:03] Ooh. There's a server headed my way.
[52:09] Call location. Watch out.
[52:12] [ Background Sounds ]
[52:35] Oh, whoops.
[52:36] Hold on one second.
[52:38] [ Background Sounds ]
[53:06] What?
[53:07] [ Background Sounds ]
[53:37] Okay.
[53:37] [ Background Sounds ]
[53:52] Maybe this is a walkthrough.
[53:53] [ Background Sounds ]
[53:56] Maybe a quick start should be a little quicker.
[53:58] [ Laughter ]
[54:00] Oh, let's see.
[54:02] [ Background Sounds ]
[54:29] Okay. So let's try this.
[54:31] [ Background Sounds ]
[54:35] Word list.
[54:36] [ Background Sounds ]
[54:57] A, pass, passphrase, mnemonic, and secret salt.
[55:09] [ Background Sounds ]
[55:31] Derive a wallet seed.
[55:36] Derive a wallet account and X key.
[55:43] Produce addresses as needed.
[55:50] [ Background Sounds ]
[56:00] Let's see.
[56:01] [ Background Sounds ]
[56:30] Let's see.
[56:31] Oh, this is wrong.
[56:32] [ Background Sounds ]
[56:35] That's okay now.
[56:36] All right.
[56:37] So.
[56:38] [ Background Sounds ]
[57:00] Um.
[57:00] [ Background Sounds ]
[57:17] Let's see.
[57:18] [ Background Sounds ]
[57:28] Let's see.
[57:29] [ Background Sounds ]
[57:31] Account index.
[57:32] [ Background Sounds ]
[57:51] Let's see here.
[57:52] We can do while not X key maybe.
[57:55] [ Background Sounds ]
[58:14] Dash change, dash HD dot receive.
[58:20] [ Background Sounds ]
[58:47] Index plus equals 1.
[58:50] [ Background Sounds ]
[58:52] All derivation paths are valid.
[58:57] Just skip to the next.
[59:00] [ Background Sounds ]
[59:14] So skip if.
[59:15] [ Background Sounds ]
[59:32] Mark as invalid account index.
[59:35] [ Background Sounds ]
[59:42] Most, but not all.
[59:45] [ Background Sounds ]
[59:50] Although very rare, some random numbers are not valid keys.
[59:59] [ Background Sounds ]
[60:02] There we go.
[60:03] And then we can just do this.
[60:07] [ Background Sounds ]
[60:36] Okay. Let's just do this one.
[60:45] [ Background Sounds ]
[61:02] Get a seed from the user's my password is in secret salts.
[61:08] There we go.
[61:11] Let's limit down.
[61:13] [ Background Sounds ]
[61:27] All right.
[61:28] Find the first valid account.
[61:31] Do or do not.
[61:34] There is no try.
[61:35] That's actually what I live by brother.
[61:37] That's what I live by.
[61:38] But on rare, rare, rare occasions, try is appropriate.
[61:43] It's almost never appropriate.
[61:45] But there are really rare occasions where try is appropriate.
[61:49] [ Background Sounds ]
[62:00] Let's see.
[62:02] [ Background Sounds ]
[62:12] Reject the seed if the first account is not valid.
[62:23] [ Background Sounds ]
[62:38] So how about this?
[62:39] [ Background Sounds ]
[62:46] Insert valid, a passphrase is valid but can't generate valid keys.
[63:02] [ Background Sounds ]
[63:24] There we go.
[63:25] Let's just keep this simple.
[63:26] [ Background Sounds ]
[63:56] OK, subs.
[63:58] I'm just trying to come up with usage examples and a walkthrough and stuff here.
[64:05] Kind of tutorial mode.
[64:07] OK, derive a wallet account in XKey.
[64:09] But reject in XKey if possible.
[64:24] Reject the phrase or seed if the first account is not valid.
[64:38] There we go.
[64:41] [ Background Sounds ]
[65:08] If other account indexes fail to produce keys, just mark.
[65:28] When working with multiple accounts, mark failed indexes as invalid.
[65:48] [ Background Sounds ]
[66:10] For multi-account applications.
[66:13] [ Background Sounds ]
[66:37] OK, and then step three would be derive the next 20 keys.
[66:47] [ Background Sounds ]
[67:08] All right, here's what we'll do then.
[67:11] [ Background Sounds ]
[67:18] Add keys.
[67:19] [ Background Sounds ]
[67:30] Address keys, there we go.
[67:32] How's my day so far?
[67:35] Well, I'm almost done with my first Mountain Dew, so I'm warming up.
[67:40] [ Background Sounds ]
[67:48] Going good.
[67:49] Provisioning some desktops so they can be shipped to future new hires.
[67:53] That's awesome.
[67:54] Imaging is probably a better word.
[67:56] Imaging, provisioning, same thing to me.
[67:58] Imaging is kind of old terminology.
[68:00] Provisioning is new terminology.
[68:02] You know, we provision servers.
[68:04] We're just imaging them, right?
[68:07] Well, I've got some good news.
[68:09] There is a server on my way.
[68:13] I've got a picture of it right now.
[68:16] And it looks like it's got nine drive bays.
[68:20] I'm hoping those are the right kind of drive bays.
[68:24] Yeah, those look like three and a half, right?
[68:27] The last row looks like it's empty.
[68:29] So it doesn't have 12 drive bays.
[68:32] That's OK though.
[68:34] I don't know what all is in it.
[68:36] I think it's a Dell R20X or something like that.
[68:41] But it's on its way to me, finally.
[68:44] So I'm going to have that set up for Homelab.
[68:50] And then I'm going to, my buddy and I,
[68:53] we're going to go in on some co-location together as well.
[68:56] [typing]
[69:18] [typing]
[69:30] [laughing]
[69:36] [typing]
[69:43] Just one second.
[69:46] [typing]
[70:12] [typing]
[70:24] Sorry. Message.
[70:27] I had this kerfuffle with Meetup.
[70:30] So, Meetup is very spammy, if you've ever used Meetup.
[70:37] They're just very predatory because they're the only solution.
[70:41] What are you going to do?
[70:43] It's just like those password managers and stuff, right?
[70:46] It's free to use until suddenly it's not,
[70:50] and then the more you need, the more it costs.
[70:53] So instead of getting economies of scale,
[70:55] you need 5 users, it's $20 a month.
[70:57] You need 10 users, it's $30 a month.
[71:01] You need 40 users, it's $35 a month.
[71:05] Instead of getting the economy of scale
[71:07] where the more you buy, the lower the cost is per unit,
[71:11] the more you buy, the higher the cost is per unit.
[71:14] So if you buy one, it's X dollars.
[71:16] But if you buy two and you want to manage two under the same account,
[71:19] then it's more than the cost of two, and so on and so forth.
[71:23] So the price does exponential SAS scaling.
[71:28] So, whatever. I got over that.
[71:32] I'm going to swap out of the plan that I'm grandfathered into
[71:38] the other plan because it's slightly less headache
[71:42] and when you consider the $10 a month per group or whatever,
[71:45] it's like, I feel like I'm being taken advantage of, whatever.
[71:49] That wasn't actually the issue.
[71:50] The issue was that in order to transition people,
[71:53] we had a group that had 2,400 people in it,
[71:55] and it was just trending down.
[71:57] So I wanted a group that was trending up rather than trending down.
[72:07] So rather than trying to reactivate the current group,
[72:09] what I decided to do was to move everybody over
[72:12] to let people know that we were creating a new group
[72:15] and then I was going to shut the old group down
[72:17] by introducing fees so that it would price everybody out of the group.
[72:26] Because if you just end the group,
[72:28] then it sends out an email to everybody saying,
[72:30] "Hey, so-and-so is stepping down as an organizer.
[72:32] Do you want to step up as the organizer?"
[72:35] Well, I didn't actually want a competing group.
[72:36] Oh, the package might have just been delivered.
[72:40] It might be the new USB hub.
[72:42] Oh, I think it was, in fact.
[72:45] Okay, anyway.
[72:48] But on my side, it's very clear that what's going to happen
[72:55] is people are just going to be priced out.
[72:57] On the other side, when they actually sent the email,
[73:00] first of all, the people who weren't active members of the group
[73:04] didn't get the emails that I was sending out.
[73:06] So I'm sending out an email saying,
[73:08] "Hey, we're shutting down this group.
[73:10] We're going to start up a new group.
[73:12] I'm just going to raise the price on this group
[73:15] to something ridiculous and then everybody's going to drop off
[73:18] and that's how I'm going to shut it down."
[73:20] Because I'm familiar with some of the problems of this.
[73:23] And I thought $999 was a high enough number
[73:30] that it wasn't believable.
[73:33] $100,000 was high enough that it wasn't believable.
[73:36] But apparently it wasn't high enough.
[73:38] And so people thought that I was actually requesting $999.
[73:43] They also thought that they were going to be charged automatically
[73:46] because the messaging that they receive
[73:50] as part of the spammy communication from Meetup
[73:52] is different from the messaging that Meetup shows me
[73:56] on my end when I'm setting up these dues.
[74:00] And thirdly, Meetup has got one of those 72-hour lags.
[74:05] You ever get those notifications where you unsubscribe
[74:07] from an email list and it says something like,
[74:09] "Please give us 7 days in order for it to be processed
[74:14] that you've unsubscribed."
[74:15] And you're thinking, "What the heck?"
[74:17] Well, Meetup has that for some of their...
[74:19] Well, it has that for the membership dues.
[74:22] So the membership dues have this lag time
[74:25] of something in the realm of 72 hours to a week or something.
[74:29] I don't know what it is.
[74:31] But I had realized that the description wasn't clear enough
[74:34] to just say, "We're moving to a new group."
[74:38] So we actually changed the message to say,
[74:42] "Do not pay. We're moving to a new group."
[74:45] But the message that went out didn't include the "Do not pay"
[74:48] and people, one, didn't read the "We're moving to a new group."
[74:51] This is the new group.
[74:53] And two, so anyway...
[74:55] And so then a bunch of ninnies are all complaining.
[74:57] "Oh, this is such a scam! I can't believe somebody wants $1,000!"
[75:01] It's like, flip and read your own screenshot.
[75:04] It says, "We're moving to a new group."
[75:06] Right?
[75:07] So these are the people that I didn't want in the group
[75:10] in the first place.
[75:11] The ones that are complaining, right?
[75:13] So they're not the people that I care about.
[75:18] And it's just... I don't know.
[75:21] So I just have a screwed attitude.
[75:24] So someone... This one guy is just...
[75:28] I don't know. Be in a D-bag.
[75:30] I think I'm just going to message him.
[75:32] "Quit being a D-bag."
[75:36] "Thanks."
[75:39] And then he's probably going to report me or something.
[75:44] But we'll see.
[75:49] There's probably no good... I shouldn't have done that.
[75:51] No good is going to come of it.
[75:53] Just sometimes, you know, I'm...
[75:57] I'm just calling you out on the BS is all.
[76:03] Okay.
[76:08] There we go. That ought to be good enough.
[76:11] Well, whatever. Shouldn't have done that.
[76:20] "You're making a mountain out of a molehill."
[76:26] "This was a simple error in process through a crappy tool with crappy options."
[76:39] Yeah, whatever.
[76:49] Anyway, sorry. I'll get back on task here.
[76:52] But anyway, that whole thing just happened and it's just...
[76:55] I don't like it when stuff like this happens.
[76:57] I don't like having to deal with it.
[76:59] Because I didn't expect it to blow up and become this thing
[77:01] that people are talking about on Twitter and talking about on Slack.
[77:04] It's like, seriously, I just...
[77:07] I don't know.
[77:11] Alright.
[77:12] It's just... I don't know.
[77:23] The inability for people to understand things that seem to be simple to me just...
[77:28] I just hate it. I just hate it.
[77:30] I just hate it. I just...
[77:32] This wasn't meant to be.
[77:34] It wasn't meant to be.
[77:36] This wasn't meant to be.
[77:39] I just... This wasn't... It wasn't that complicated.
[77:41] You got an email.
[77:43] It said that... I mean, I get how someone on the other side,
[77:48] when they get it from Meetup, thinks that,
[77:51] "Oh, I'm going to have to pay $1,000. This is something scammy."
[77:54] I kind of get that, but then once it's been resolved...
[77:57] Well, one, I mean, if you looked at any of the other communications,
[78:00] if you visited the group, the title of the group was
[78:03] "Do not pay moved to other group."
[78:08] You know? So, it's just...
[78:10] We included the "Do not pay" in the name of the group after a day.
[78:16] But, anyway, it's just...
[78:19] It's just so frustrating. I just hate these flippin'...
[78:23] These people that are just...
[78:28] Everything... I can't even go into it.
[78:31] Anyway, that's good, though. Gets my blood going.
[78:36] (sighs)
[78:38] Okay, so we want to try to get these keys.
[78:42] And so then we're going to try...
[78:45] Let key equals...
[78:48] So, for...
[78:51] Invalid indexes...
[78:56] (typing)
[78:58] Okay, let i equals 0.
[79:09] Let last index equals 0.
[79:17] Index i...
[79:25] (typing)
[79:28] i plus equals 1.
[79:41] (typing)
[79:45] (sighs)
[79:46] (sighs) Just...
[80:03] People. People.
[80:05] You can't live with them, you can't live without them.
[80:08] (sighs)
[80:12] (sighs)
[80:14] (sighs)
[80:29] (typing)
[80:32] (sighs)
[80:36] (typing)
[80:37] (sighs)
[81:05] (sighs)
[81:06] Okay, sorry. I keep getting distracted here.
[81:14] Alright, X key, derive key...
[81:17] Um...
[81:20] Let use equals...
[81:23] Use...
[81:29] And the rest of us. Happens to the best of us and the rest of us.
[81:34] I just get... I don't know how to explain it.
[81:36] I mean, I think it's... I think I'm actually fairly normal in this regard.
[81:40] But I just kind of get all... Ugh.
[81:43] You know, I just...
[81:45] I cause conflict a lot and I don't like the conflict I create.
[81:49] Especially when I didn't intend to create it.
[81:52] I just feel like...
[81:54] (sighs) I don't know.
[81:56] I don't know. But I'm not one to apologize much.
[82:02] Unless I actually believe that I'm wrong. In which case, I'll apologize.
[82:05] But...
[82:08] I often don't believe that I'm wrong.
[82:10] I think with what I did, you know, the situation is kind of the best.
[82:13] Where I am wrong is in just engaging with these people who A) are not members of the group.
[82:18] They're just...
[82:20] They're upset that they got an email that had a number in it that they didn't like.
[82:25] That they didn't need to do anything about.
[82:29] Except that for the fact that it...
[82:31] I have not seen the email that they got.
[82:34] They're claiming that it makes it look like this is an automatic payment.
[82:38] That if they did nothing, it's just going to charge them.
[82:40] Which I don't know that would have... How I think that would happen.
[82:43] Unless they're already paying for something anyway, which I don't think they are.
[82:47] So...
[82:49] You know, I mean that... I don't know.
[82:51] I don't know. I just...
[82:53] I just feel like so much of my life is a failure because...
[82:57] I want to create things that are simple and easy to use and easy to understand.
[83:01] Just in general, in all aspects.
[83:03] And it's just really, really hard.
[83:06] It's just so much harder than it seems like it will be.
[83:09] And...
[83:11] No matter whether it's technical or non-technical, it's just frustrating.
[83:16] Um...
[83:18] Okay. Last index plus equals one.
[83:32] Whoop! That didn't work out the way that I thought it would.
[83:37] Oh, I see why.
[83:39] Okay, good.
[83:41] Alright, so last index plus...
[83:44] (typing)
[83:55] Maybe instead of last it should be...
[83:57] Recent...
[83:59] (typing)
[84:01] Previous...
[84:04] (typing)
[84:20] Alright, X-Key, Derived Key...
[84:23] (typing)
[84:27] Use...
[84:30] (typing)
[84:47] Actually, I think this is pretty good code here.
[84:51] So when the code is at this level, I think that it's a good idea.
[84:57] When it's up at the level where you're controlling the index,
[85:00] I think it's okay to just kind of go past the index.
[85:04] You don't even really need to mark it as invalid.
[85:08] Um...
[85:10] (typing)
[85:12] You can just not use it.
[85:15] (typing)
[85:44] (typing)
[86:05] So, and the index is important for the path.
[86:09] (typing)
[86:24] Whoops, I meant to only do one of those, but I got two, that's fine.
[86:28] ToAdder...
[86:31] Public Key...
[86:34] (typing)
[86:50] There we go.
[86:52] Is that the better way to do this, I think?
[86:54] Alright, I've got some sort of syntax there I need to go fix.
[86:57] Let's take a look at this one.
[86:59] So this one...
[87:01] (typing)
[87:08] Yeah, we just want to derive the whole...
[87:11] We want to derive the key in each way.
[87:15] Drive a batch of addresses.
[87:18] 20 is the typical number.
[87:21] (typing)
[87:28] Anyway, I don't know, I just embarrass myself and make a fool of myself and...
[87:32] (sigh)
[87:34] I don't know.
[87:37] I could probably do something better.
[87:40] (typing)
[87:48] I really don't like petty criticism.
[87:51] Which is ironic, because I give out a lot of petty criticism.
[87:54] I guess, if you can't stand the heat, don't get in the kitchen.
[87:59] It's my own darn fault, is that...
[88:02] Maybe that's all there is to say about it.
[88:06] Alright, why is this wrong? What did I do wrong here?
[88:09] (typing)
[88:12] It says it's matched there, this says it's matched there.
[88:15] Am I missing a parenthesis? What's going on?
[88:18] 21, unexpected token. 21. Oh!
[88:23] (typing)
[88:26] There it goes.
[88:28] (typing)
[88:58] I just need to let it go.
[89:00] (typing)
[89:02] And maybe, you know, maybe I'm also a little bit paranoid.
[89:06] I would say, you know, I'm just a touch, just a little bit sometimes.
[89:10] But just, you know, in terms of misinterpreting things myself
[89:13] and then projecting on other people, maybe.
[89:17] (typing)
[89:32] Alright, here's a question. Do I just rename this to index?
[89:36] (typing)
[89:43] And then, have these, eh, I don't know, that's probably fine.
[89:47] (typing)
[89:50] And, do you not, do you have, no.
[89:58] He doesn't want his face to take up the whole of the thumbnail.
[90:08] (typing)
[90:11] You get the headshots and stuff.
[90:15] (typing)
[90:17] Okay.
[90:19] (typing)
[90:23] Look at what I said in the channel.
[90:27] Use that headshot and add those, those assets.
[90:38] (typing)
[90:47] Okay.
[90:49] (sigh)
[90:51] Okay, this, this should be right now.
[90:54] Alright, let me get out of here.
[90:56] (typing)
[91:07] Dang it.
[91:09] Everything's off by just one character.
[91:13] Just one space.
[91:16] Actually, if I just get everything in, it should fix itself.
[91:23] (typing)
[91:52] (typing)
[91:57] Oh, oh my gosh, hold on.
[92:02] So, I work with this one guy and sometimes I get so confused
[92:05] because it's like if you give him instruction, he does the opposite.
[92:08] If you give him no instruction and he knows what to do, then he does it right.
[92:12] I get so confused because I thought the instruction was really, really super crystal clear.
[92:18] Oh, goodness. One second, one second.
[92:23] (typing)
[92:51] Okay.
[92:53] (typing)
[93:14] Uh-oh, what happened?
[93:16] (typing)
[93:19] Okay, sorry.
[93:21] So, I'm going to push these.
[93:24] Previous index, blah, blah, blah, blah, blah.
[93:26] Alright, there we go.
[93:28] (typing)
[93:30] What pesky space? Oh, hello everybody.
[93:33] Everybody's joining in.
[93:35] (typing)
[93:38] Sure, come in when I'm distracted.
[93:40] Come in when somebody's, it's only, yeah, I don't know.
[93:44] Okay, so I think this is good now.
[93:47] (typing)
[94:01] Okay, so here we go.
[94:03] We get a seed from the passphrase mnemonic and the secret salt.
[94:07] We derive a wallet account in XKey, if possible.
[94:11] (typing)
[94:41] (typing)
[94:54] Oh, sorry.
[94:57] (typing)
[95:26] Okay.
[95:27] Let's see here.
[95:29] (sighs)
[95:32] Okay, I'm just going to, dang it.
[95:34] (groans)
[95:36] I got a message from somebody that I need to deal with
[95:40] because this thing's supposed to be updated before tomorrow.
[95:43] (typing)
[95:45] Okay, but I think this is, okay, so we try to get the wallet.
[95:48] We don't really care about the wallet.
[95:50] We don't really care about the account.
[95:52] (typing)
[95:55] We care about the XKey.
[95:56] That's the thing that we need to reuse.
[95:58] And then over here, I'm going to derive a batch of addresses
[96:02] using XKey from step two.
[96:11] And then I could maybe put here seed from step one.
[96:16] (typing)
[96:18] Okay.
[96:20] All right, so this is kind of the whole thing.
[96:24] I'm just going to go ahead and whip this.
[96:25] So if anybody wants to take a look at that and give me feedback,
[96:27] feel free to do so.
[96:31] All right, so here it is.
[96:35] (typing)
[97:04] (typing)
[97:29] Okay.
[97:35] So there we go.
[97:37] Here's the README that we're working on.
[97:41] Update it a little bit.
[97:47] So where is, let's see.
[97:50] All right, so let's go back up to the quick start here.
[97:55] Where is, wait, it didn't go?
[97:57] Did I do something wrong?
[97:59] Oh, I didn't push it.
[98:05] All right, so we're going to have a quick start.
[98:07] I guess I should put the usage back there.
[98:09] So we got a quick start, we got a walkthrough.
[98:11] That's what we got.
[98:13] Okay, you get a seed, derive a wallet and XKey if possible.
[98:17] Reject the passphrase or seed if the first account is not valid.
[98:21] I kind of want to change that to zeroth just to be more clear.
[98:33] F account, let's see, account index zero is not valid.
[98:41] There we go.
[98:43] Oh, and this does not have the account index, does it?
[98:48] There we go.
[98:56] There, that's a little better perhaps.
[99:00] Okay.
[99:02] Oh, and I forgot to turn the music on.
[99:07] Music.
[99:21] Music.
[99:42] Music.
[99:58] I'm going to turn the music down a little bit for myself.
[100:06.64] There we go.
[100:10.14] Nice.
[100:17.64] Okay, so all of this code should actually work is the thing.
[100:24.64] Seed from step one, XKey from step two.
[100:37.14] I could just put these in here maybe.
[100:51.64] Here we go.
[100:54.14] Music.
[101:23.64] Music.
[101:53.14] Music.
[102:22.14] Okay.
[102:35.14] I actually kind of think.
[102:48.64] May be useful.
[103:04.14] Let's try moving this here.
[103:21.14] How about this?
[103:37.14] Okay.
[104:06.64] Let HD path equals, there we go, do this.
[104:18.14] Music.
[104:39.14] Music.
[105:00.64] All right, there we go, that's good.
[105:03.64] All right, now let's do the walkthrough.
[105:05.64] So the walkthrough.
[105:08.14] So walkthrough is basically the same thing as above, but we're going to break it down basically line by line to try to really give an explanation of everything here.
[105:19.64] I think the walkthrough probably should go down lower.
[105:25.14] So we'll have the quick start.
[105:28.14] Walkthrough.
[105:57.64] Music.
[106:06.14] Let's see.
[106:32.14] Let's see.
[106:46.64] Music.
[107:04.64] However, there are some.
[107:11.64] The code will look more like this.
[107:39.64] This would be index.
[107:44.14] Three.
[107:47.64] Oh.
[108:16.14] Generate address keys.
[108:28.14] Maybe I should rename that generate address key.
[108:48.14] Okay.
[109:17.64] Let's see, gosh, there's so many different layers to this thing.
[109:45.64] Music.
[109:55.14] Okay.
[110:07.64] All right, account.
[110:18.14] Key extended.
[110:29.64] Or public key.
[110:41.64] Optional.
[110:45.14] Xpriv and Xpub.
[111:11.64] Music.
[111:41.14] Okay.
[112:10.14] Music.
[112:39.14] And.
[112:51.64] I think maybe I should call it address key.
[112:56.64] Then it would be a little bit more differentiated from.
[113:26.14] Music.
[113:33.64] Okay.
[113:49.14] All right.
[113:58.64] This has already been shown up above.
[114:01.64] Okay, so here's the simple usage.
[114:11.14] Okay, here's the quick start.
[114:23.64] Music.
[114:52.64] Music.
[115:14.64] Music.
[115:36.64] As a one off.
[115:39.14] You can directly generate an address key.
[115:49.64] Key equals way dash HD.
[116:04.64] Music.
[116:32.64] Oh, man.
[116:54.64] Music.
[117:04.14] Okay, as a one off, you can directly generate an address key by HD path.
[117:08.14] There we go.
[117:18.14] And there's the production quick start.
[117:20.14] And then we'll move the walkthrough deeper down.
[117:23.64] Finish the walkthrough.
[117:28.14] So it's kind of layered.
[117:29.14] It's.
[117:35.14] For some people, all you need is the usage overview.
[117:38.14] Boom, you're done.
[117:40.14] For some people.
[117:43.64] You need the production quick start.
[117:54.14] Oops.
[118:05.14] Production quick start.
[118:12.64] Usage overview.
[118:26.14] Oh.
[118:32.14] Yes.
[118:51.14] Music.
[119:20.64] Music.
[119:30.64] Music.
[119:54.64] Oh, wow.
[120:03.14] Music.
[120:24.14] Music.
[120:53.14] Music.
[120:59.64] So install.
[121:07.64] I don't know why my editor does this thing.
[121:12.14] API.
[121:28.64] Walkthrough.
[121:35.14] Music.
[122:04.14] Music.
[122:25.14] Music.
[122:46.14] Music.
[123:07.14] Music.
[123:18.14] Music.
[123:37.14] Okay.
[123:49.64] All right, we're gonna go through the API first.
[123:55.64] And the walkthrough.
[123:58.64] Or should we do the walkthrough and then I don't know.
[124:02.64] It's not important.
[124:03.64] I just need to finish it.
[124:05.14] I need to have all the examples ready and finish it.
[124:07.64] Okay.
[124:08.64] Usage is done.
[124:09.64] Locked and loaded.
[124:10.64] Production quick start is done.
[124:12.64] Locked and loaded.
[124:14.14] I mean, there's no errors or anything.
[124:36.14] All right, so we had part two.
[124:51.64] Part two, a direct derivation.
[124:57.14] Part to be.
[125:12.64] Hmm.
[125:42.14] Hmm.
[126:06.64] Okay.
[126:32.64] In fact, possible for.
[126:37.14] Seed derivation to fail.
[126:42.14] It's.
[126:46.14] As mentioned in the API section.
[126:50.64] It is in fact possible for any derivation to fail.
[127:04.14] It's highly unlikely that you'll ever.
[127:10.14] Counter it.
[127:12.64] But it should be handled nonetheless.
[127:37.64] Oh, let me Debbie.
[128:04.14] Okay.
[128:17.64] Three.
[128:18.64] Three.
[128:19.64] Three.
[128:21.14] I guess this is still kind of.
[128:50.64] So the sort of thing.
[129:00.14] You'd want to do in a loop.
[129:04.14] As it would.
[129:06.14] Five X.
[129:09.14] The number.
[129:11.14] Of derivations.
[129:15.64] Per key.
[129:31.14] As a one off.
[129:34.64] It's.
[129:37.64] Direct.
[129:46.64] Let's see.
[130:02.14] The.
[130:21.64] Again.
[130:23.64] To account for the fact.
[130:27.64] That.
[130:30.14] One may.
[130:34.64] Fail.
[131:01.14] Let.
[131:06.64] Max tries equals.
[131:11.64] Three.
[131:15.64] For let I equals address index.
[131:20.64] I less than Max tries.
[131:24.14] I plus equals one.
[131:30.64] Key.
[131:33.64] Equals.
[131:34.64] Wallet.
[131:37.64] Ht.
[131:38.64] Drive.
[131:40.64] Wallet.
[131:45.64] Account.
[131:46.64] Index.
[131:47.64] Equals zero.
[131:48.64] Use equals.
[131:52.14] Ht.
[131:52.64] Receive.
[132:21.14] The.
[132:50.64] More than one.
[133:09.14] Failure.
[133:10.14] In a row.
[133:11.14] Would.
[133:12.14] Indicate.
[133:13.14] A.
[133:14.64] Bad.
[133:15.14] Count.
[133:16.14] Index.
[133:39.14] C.
[133:42.14] Could not.
[133:43.64] Derive.