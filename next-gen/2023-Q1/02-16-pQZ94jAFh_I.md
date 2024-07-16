---
showLink: "https://www.youtube.com/watch?v=pQZ94jAFh_I"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Code Hangout: Next-Gen DASH Tools #20: Dash HD: Publishing. Really. For Real."
publishDate: "2023-02-16"
coverImage: "https://i.ytimg.com/vi/pQZ94jAFh_I/maxresdefault.jpg"
---

## Episode Description

A developer works on updating and publishing Dash cryptocurrency libraries, discussing coding practices and challenges along the way.

## Episode Summary

In this lengthy coding session, the developer works on updating and publishing several Dash cryptocurrency libraries including dash-keys, dash-phrase, and dash-hd. They make various code changes to improve functionality and consistency, run tests, and ultimately publish new major versions of the libraries. Along the way, they discuss coding practices, debugging techniques, and some of their views on programming vs. web development. The session ends late at night after successfully publishing the updated libraries.

## Chapters

00:00 - Introduction and Setup

The developer begins the coding session, setting up their environment and reviewing the tasks ahead. They mention working on Dash cryptocurrency libraries and discuss recent changes made. This chapter provides context for the work to be done in the stream.

04:02 - Working on dash-keys Library 

The developer dives into working on the dash-keys library, making updates to improve functionality and consistency. They discuss changes to key encoding/decoding, type definitions, and API design choices. This chapter covers a significant portion of the work on dash-keys.

69:07 - Updating dash-phrase Library

After finishing work on dash-keys, the developer moves on to updating the dash-phrase library. They make similar consistency improvements and ensure compatibility with the updated dash-keys library. This chapter shows the interconnected nature of the different Dash libraries.

126:25 - Final Updates to dash-hd Library

The developer works on final updates to the dash-hd library, including renaming some functions for clarity and exposing new methods for raw key bytes. They run tests and fix any remaining issues before preparing to publish the updated libraries.

183:33 - Publishing Updated Libraries

In the final stretch, the developer prepares to publish the updated libraries to NPM. They bump version numbers, run final checks, and ultimately publish new major versions of dash-keys, dash-phrase, and dash-hd. The chapter ends with reflections on the completed work and future tasks.

200:50 - Wrap-up and Programming Discussion 

As the lengthy coding session winds down, the developer engages in some discussion about programming, web development, and CSS with viewers in the chat. They share opinions on different approaches and frameworks before concluding the stream.

## Transcript

[00:00] [ Music ]
[00:24] >> Mic check one two.
[00:25] Mic check one two.
[00:27] [ Music ]
[00:36] [ Music ]
[00:45] [ Music ]
[00:55] [ Music ]
[01:03] [ Music ]
[01:13] [ Music ]
[01:23] [ Music ]
[01:33] [ Music ]
[01:43] [ Music ]
[01:53] [ Music ]
[02:03] [ Music ]
[02:13] [ Music ]
[02:23] [ Music ]
[02:33] [ Music ]
[02:43] [ Music ]
[02:53] [ Music ]
[03:03] [ Music ]
[03:13] [ Music ]
[03:23] [ Music ]
[03:33] [ Music ]
[03:43] [ Music ]
[03:56] >> Hey! And welcome back, everybody.
[03:59] I'm A.J. O'Neill, and we're going to do some code,
[04:02] because that's what we do.
[04:04] At least that's what I do.
[04:06] Okay, so I am over my frumpiness from this morning.
[04:11] I got to get into an argument with somebody
[04:15] that actually made me feel a lot better.
[04:18] It's always nice when you get to tell the truth.
[04:23] It's also nice when the other person tells you some truth
[04:27] and reply to truth.
[04:29] The whole thing they say, "The truth shall set you free."
[04:34] Oh!
[04:37] Anyway, there was probably a little bit of self-deception,
[04:41] you know, mixed in with the truth,
[04:43] but I think there was more truth than not.
[04:46] Helps to finally be able to just get it out.
[04:49] All right, so anyway, I think we need to have a better culture
[04:55] of arguing and being aggressive to solve problems,
[05:00] because problems can be solved
[05:02] when you can be clear and voice them.
[05:05] Ugh, problems cannot be solved
[05:07] when you hide behind codes of conduct and other nonsense.
[05:14] You have to be truthful.
[05:16] All right, so where were we here?
[05:19] How in the world did Dash Phrase Tools get open?
[05:22] Where is that coming from?
[05:24] Okay, now, as I recall,
[05:27] the only thing that's keeping us from pulling this all in--
[05:30] and I actually do need to contact somebody about some API changes.
[05:35] Let me go ahead and do that.
[05:40] Let's see.
[05:41] First of all, is this version published?
[05:44] That's the first thing we need to know.
[05:46] Is this version actually published?
[05:50] Because I don't know if it is or if it isn't.
[05:54] But we need to check to see if this is published,
[05:56] because if this isn't published,
[05:58] this, I think, is worth publishing on its own.
[06:04] This has all the await stuff in it, right?
[06:07] Yeah. Okay.
[06:10] So this might be worth publishing on its own.
[06:18] Let's see.
[06:20] And I need to ask somebody,
[06:24] "Which version of Dash HD were you using?"
[06:42] I'm...
[06:49] Let's see.
[06:59] "Which version/branch?" That's what we need to ask.
[07:06] There's some...
[07:11] The final version has several simple but hard-breaking changes.
[07:23] For example,
[07:26] "private extended key"
[07:48] becomes "old",
[07:54] "new",
[08:23] "old".
[08:33] Okay, I'm about to publish this now,
[08:34] but I could publish an intermediary version
[08:37] with what you've been using,
[08:40] so that it's not a PETA to pick up to keep going.
[09:02] Let's see.
[09:11] Let's see.
[09:13] Also, there's a question.
[09:16] "Also, there are a few different encodings."
[09:21] "Hex is base 16."
[09:26] "Most key formats are in base 58 check when presented to a user,
[09:37] but are sometimes in hex as an intermediary format between APIs."
[10:01] "Always base 58 check when presented to a user between APIs,
[10:10] and the canonical form is UN8 array, but that's not serializable."
[10:39] So it goes to hex or base 58 check depending on the API.
[10:47] Okay.
[11:01] Okay, so I definitely need to expose that serialize function.
[11:05] That's something that needs to happen,
[11:06] but we don't need to do that yet.
[11:08] Let's back up.
[11:09] So let's just get out of a bunch of things here.
[11:12] Let's get out of here.
[11:13] Get out of here.
[11:14] Get out of here.
[11:15] Get out of here.
[11:16] Get out of here.
[11:17] Get out of here.
[11:18] Get out of here.
[11:19] Get out of here.
[11:20] We're just going to start way back at the beginning.
[11:21] Okay, let's go back to -heim.
[11:22] So we've got four things that we've got to worry about.
[11:25] One of them is -phrase.
[11:28] One of them is -keys.
[11:30] One of them is -hd.
[11:32] And the final one is secp256k1.
[11:38] So these are the four things that we have to worry about.
[11:40] Now, -hd is at the back of the line right now.
[11:44] So we could publish that, but we need to make sure that first,
[11:48] we have our final version of, most importantly, -keys,
[11:52] which means that we need to have our final version of secp256k1.
[11:56] So then -keys.
[11:58] Then -phrase is not dependent on these two,
[12:00] but we do need to have our final version of it.
[12:03] And then finally -hd.
[12:05] So we need to go this wise.
[12:07] Now, the CLI for secp256k1 is probably going to be -message.
[12:14] That we already built with -core, and we will rebuild it with this.
[12:26] But these four are the chain.
[12:28] So, let's take a look and see what we've got.
[12:31] First thing, I want to check out and see where Paul Miller is at with Noble.
[12:38] Because his v2 is really interesting.
[12:44] It's exactly what we need.
[12:46] And so I want to check and see where he's at on this.
[13:03] Okay, sign.
[13:12] Alright, getting rid of micro-optimizations.
[13:18] So this is interesting.
[13:21] So we could expect to get, let's see, 7,000.
[13:29] Get shared secret, recover public key.
[13:36] It looks like we could expect to get a few thousand keys per second with our library.
[13:51] Okay, where is he at?
[13:57] Oh, he already commits last bomb. Is there another benchmark here?
[14:08] Yeah, whatever.
[14:20] Blah, blah, blah. Yeah, yeah, yeah.
[14:42] What have we got?
[15:03] Interesting.
[15:19] So one nasty thing that might happen here, which wouldn't be too bad in terms of what we're doing.
[15:25] Is he might make this...
[15:30] So the problem with the ESM modules is that they have asynchronous imports.
[15:36] Which means that it just breaks everything else.
[15:38] Because you can't require an asynchronous import from a synchronous import.
[15:43] And so it's just a big pita.
[15:51] That's okay. That's just a little syntax at the top and the bottom.
[15:55] We can make a copy of that.
[15:57] The one thing that I am concerned about, I need to see...
[16:03] With block TX, the way that this currently works is correct.
[16:07] And that's what we need to optimize for right now.
[16:09] I don't think we use sign anywhere. Let me go ahead and check.
[16:12] We don't use... Do we use the sign function?
[16:16] We can delay that choice. We can delay that choice.
[16:18] We can publish the final version of secp256k1 without making the decision.
[16:28] I think.
[16:41] Can we just force pull? Nope. Nope, we can't.
[16:48] Get rebase. Let's see. Get reset --hard head... I don't know, 50?
[16:56] There we go. That's what I wanted.
[17:00] So I'm going to come out of here. I'm going to go into...
[17:08] Okay, in -TX we have to sign. That's important.
[17:15] Oh, and there was one other issue that I need to look at.
[17:20] The one that I was already part of for something else.
[17:26] Tweak. Okay, yes.
[17:29] So this tweak stuff, let me go back to...
[17:36] Alright. Tweak utils when tweak is zero throws.
[17:42] Copy the code.
[17:46] And this one new test does not pass.
[18:15] This should be adjusted then.
[18:20] Current behavior was made on purpose. Why would you add an all zero private key?
[18:26] It's invalid ECDH context.
[18:46] I'm interested to see... So he basically was doing the same thing I was doing.
[19:01] Alright, so for the time being, I just want to double check here. We don't need sign for -HD.
[19:14] Except for in the test. There's a little help thing. JS config. Key usages. Okay. Change log.
[19:36] Okay, so we don't use sign there. This is one of the things I'd like to delay.
[19:40] So we're going to have to take a look at the way that the dash message is done.
[19:55] I'm pretty sure it's going to be with ASN1 signatures.
[19:58] So I think we're going to have to keep ASN1, which is fine. I've got the code for it either way.
[20:03] But if he removes it, I would like to actually expose the raw RNS values as the canonical form.
[20:13] And have the ASN1 form be non-canonical.
[20:19] Because that... Well, it's easier... For serialization purposes, ASN1 is easier.
[20:24] But for the purposes of how you actually use the signature, the bytes already separated into two separate values is easier.
[20:31] On 601, half a dozen on the other on that one.
[20:34] Okay, so, clear. We don't need it for that. We don't need it for dashphrase.
[20:39] I'm positive we don't need it for dashphrase, but we're going to look through it anyway.
[20:48] Dashphrase config. Yep. Okay.
[20:53] And then... What did I say? Dashphrase, dashkeys. Dashkeys.
[21:01] I think we do... We might have it in dashkeys. We don't. Okay, we're good.
[21:07] Alright, so we're not going to worry about the signing until the next set of tools.
[21:13] By the way, this series is wrapping up. We are done.
[21:16] 20 videos is way too many videos. We're wrapping up with this.
[21:20] We're moving on to the next series after this, which is going to be focused on a different set of tools.
[21:25] Well, some of the same tools, but...
[21:31] Dashkeys, right?
[21:35] That's what we need to publish.
[21:56] Encode key. Okay, I need to say...
[22:09] I'm publishing a new version of dashkeys right now that includes a fix for encode key.
[22:28] So that it will work with raw public keys and distinguish between XProve and XPub.
[22:51] What's up?
[22:58] Oh, we need to do it again, but we need to make it antiposix, bashism, bashismful.
[23:06] You know, you can make that play on words when you're standing there across the glass from me.
[23:15] But if you were in the room, we'd be fighting.
[23:19] Could use a good fight.
[23:25] Remember back in the good old days when we used to solve our irrational problems by irrational means?
[23:31] You know, just...
[23:34] You're making me upset. You're making me upset.
[23:37] It's your fault. No, it's your fault. Let's wrestle about it.
[23:41] Oh, dang it. You won. I guess it's my fault.
[23:45] You know, it was a less civilized age, but a more civilized time.
[23:51] You know what I'm saying?
[24:00] Okay, so the one thing that I did not do here that I still need to do is I need to figure out which byte exactly.
[24:09] And I believe that the way this is serialized, I believe it's always the same byte.
[24:13] I need to figure out which byte exactly is the xprev byte.
[24:23] Because we should not actually have to encode xkey.
[24:33] Oh, bless me. We should not actually have to have the version. The version should be optional.
[24:45] So we should have the same thing that we have right here. So I'm going to go check in the other repo.
[24:50] Josue, what's up? How you doing, man? It's good to see you. Welcome to the Dash Incubator channel.
[24:54] I think you've already been on this channel, but welcome anyway.
[24:59] If you're not subscribed on this channel, make sure to subscribe on this channel as well.
[25:04] And ring the bell so I can tell Ryan Well about the sell of the Dash Incubator channel.
[25:17] If that didn't do it for you, I don't know what will.
[25:30] Oh, excuse me. If I'm not mistaken, is the 41st byte. I think that's what I discovered earlier.
[25:38] Or is it the 42nd byte? Because it's the 41st index. Let's see how this plays out.
[25:47] So we've got our 4 + 1 + chain + 1. So 1 + 32 is actually the way to think about that.
[25:58] That's the way that I would prefer to think about it.
[26:06] Okay, so if we count these bytes up. So this starts at 0. So 4, 5, 9, 13, 45.
[26:24] That doesn't seem right. Did I count that right? Oh, the version is not on this at this stage.
[26:35] And this may actually be a problem in the library that has to get fixed later.
[26:40] It would require probably a major version bump, but it would be one of those compatibility issue major version bumps.
[26:49] Not a "Oh, we rethought the library" major version bumps.
[26:55] I'm not sure if it would or wouldn't be.
[27:00] Doing great. Already subscribed to the channel. I've been seeing some of the videos after the fact lately.
[27:04] But the corporate world calls me and I have to go to bed at this hour. We'll get to bed at that hour.
[27:11] Now. Go. Or keep me company. Whatever.
[27:18] 45, so 41. Yeah.
[27:24] So I think we just look at magic byte 41. So if.
[27:53] Okay.
[28:14] So I think we just look at magic byte 41. So if.
[28:34] Okay.
[28:54] So.
[29:22] Okay.
[29:33] So op's dot version dot.
[29:37] Two string.
[29:40] I wonder if we could we get rid of type of would that be possible. Can we do. Can we do type checking without having type of.
[29:54] Okay, that is array. No, it's easy to compare. Undefined is easy to compare. I don't know how to compare object.
[30:10] Compare Boolean because you compare true or false exhaustively.
[30:23] I'm looking at how do we eliminate keywords from the language. How do we make the language really small.
[30:52] Okay.
[31:06] And how much padding do we need for that.
[31:13] One, two, three, four, five, six, seven, eight. That makes sense. Four bytes. So we need eight. And we're going to pad with zeros.
[31:31] Okay. So.
[31:54] Okay.
[32:20] Okay.
[32:32] So that one is going to be home lab.
[32:35] But in all of the excitement.
[32:44] So, he, I don't know if he buys them up or if he just gets them because he's the one that's doing the order for the replacements or whatever.
[32:52] But that one I, because we were talking about, oh, you know, you know, you parted out for me and I'll buy it.
[33:03] No, no, no, no, no. I got one that I'm taking out of service. It's going to be ready. And then, you know, a month later.
[33:09] Well, you know, but I'm still, I'm going to take this one out of service. I took it out of service, but it's at my friend's house or, you know, that kind of thing.
[33:18] So, anyway. So, finally, it's coming. And I think that we will actually, it sounds like we're going to be putting four more in co-location in a secret location.
[33:32] Secret. Secret co-located servers. Can you imagine that? And swapping over enough of our client machines that it should break us even.
[33:46] The idea is that it will break even on month one. But not from the cost of the servers, but the cost of the, we won't be paying any more with co-location than we're currently paying if we just take a couple days to migrate everything over.
[34:01] I mean, taking a couple days is, that's a lot of time is money, but we have to do this in the end. We have to get off the cloud. We have to co-locate.
[34:11] I need to code a lot tomorrow. Okay. I'll try to get better notifications so you'll actually notice when the stream's done. Okay. Have a good one.
[34:24] So, you didn't hear my whole conversation about the server to myself. That's okay. Somebody will.
[34:32] But I'm excited about co-locating. I'm, yeah, that's exciting to me. That's been my dream for a long time.
[34:42] Okay. If number type of op stop version.
[35:02] What the letter L is this going on about?
[35:14] Encode key, you want a array.
[35:29] Okay. Ops. Yes.
[35:45] Okay. Prop version.
[36:02] Let's try this again.
[36:16] And then I don't know what to call this. Because this one is the string. Well, we could do it this way. How about this?
[36:26] Oh, the type definitions run hard.
[36:47] All right.
[36:56] Take that, version.
[37:13] I don't know what this is saying. Property. Oh.
[37:20] Ah, okay. No, good call. Good call. Good call, TSC. Good call.
[37:34] Type string.
[37:45] Ah.
[37:59] Yes, it is. Get off my back.
[38:04] Type def version.
[38:10] That's Albanian for your mom.
[38:39] Okay. There we go.
[39:05] Now, this is something that I'm thinking about AI script. I don't know how I'd handle this situation in an AI script other than to say, I don't know, I might actually have to back down and say, okay, well, this is just a string, but I don't like that idea.
[39:20] I wonder if there's a way that we could type it to say, if you're making an assignment to it.
[39:31] Because you could say, well, if we've done the exhaustive check, then there's no need to check anything else because we've checked it exhaustively, right?
[39:40] So you could say that it's, it's inappropriate.
[39:57] To do checking beyond what is strictly necessary.
[40:00] Okay.
[40:01] No matter, this is not that big of a deal.
[40:04] But, okay, so the thing here is.
[40:08] That the version that's being passed in.
[40:18] It has to be a specific string or a specific number.
[40:23] Not any string, not any number.
[40:36] This is one of those things where I don't know what the right solution is.
[40:51] But it doesn't, it doesn't, it shouldn't matter, really.
[41:07] I mean, it's the type hinting could be, could be that if you want to pass in a type that's not supported.
[41:08] Well, we really are pretty hard on those types, actually.
[41:09] Okay, but.
[41:10] Here's the deal.
[41:11] So if this has.
[41:13] Oh, we need to, we need to.
[41:19] We need to do a few things here.
[41:36] Whoops.
[41:43] That version is wrong.
[41:53] Huh.
[41:59] 20 bytes should be PKH.
[42:01] So there's a bug fixed.
[42:03] Glad I happened to see that.
[42:11] Yeah, I know I've been wrong.
[42:13] I think that actually hadn't been committed yet.
[42:18] Okay.
[42:20] So 20 bytes is a pubkey hash.
[42:23] 32 bytes is a private key.
[42:25] 33 bytes is a public key, which means it's a pubkey hash.
[42:32] Actually, I want to put this after the transformation because I feel like that's more semantically clear.
[43:01] Okay.
[43:24] I generally don't like to have an else.
[43:26] I generally like to have.
[43:31] Well, in this case, I think an else makes sense.
[43:43] I think it's a little more readable, but I generally like to say, well, here's the default value.
[43:49] If the default value is not good enough, then reassign it with the other value.
[43:58] In this case, I think this looks right.
[44:00] Okay, cool.
[44:02] So this should fix that problem.
[44:05] So now the encode key should behave properly in every scenario.
[44:11] It does make the code a little bit more verbose than I'd like it to be.
[44:18] This is something where, eh.
[44:34] Oh, that's not me, is it?
[44:46] Okay, so it knows what to do to encode the key.
[44:48] And let's see if we can get encode and decode to be a little bit tighter.
[45:12] Okay, so there's a slight difference between the encode and the decode.
[45:22] And that difference is basically the ops.
[45:26] So the decode has to explode to give you back an object that has multiple parts to it.
[45:45] What did we choose here? Yeah, we've got the parity.
[46:09] To do X keys.
[46:12] I don't think I'm going to do that one yet.
[46:21] Did I sidestep that one in some way?
[46:31] It looks like I am.
[46:35] I am handling X keys there.
[46:38] Okay, so I left the to do. This is the problem with to do's.
[46:41] You actually put the code in right with the to do.
[46:44] Don't delete the to do.
[46:46] Let's see what else we got here.
[46:49] So my only to do is to have parity with decode.
[46:52] And let me see where we're at with that.
[46:54] So the problem is this decode takes base 58 check.
[46:58] And base 58 check is going to decode to several parts.
[47:03] Which is going to include whether or not it's valid.
[47:07] You can throw that away.
[47:13] What it's type is.
[47:16] Again, that's not actually that important.
[47:24] Because we can tell what the type is by the key.
[47:27] Okay, so that's another one that's not needed.
[47:31] The version.
[47:35] And this just totally depends on what we're dealing with.
[47:46] Parts dot version.
[47:54] The reason we're doing this in hex is because that's what we need for this.
[47:57] So we leave that in hex.
[48:00] This library deals completely in hex.
[48:02] So before something's passed in here, it needs to be hex.
[48:05] I kind of want to take out that check for the number.
[48:08] In fact, I am going to do that.
[48:10] Because the way this works.
[48:16] Well, I'm not yet.
[48:17] I'm not going to do it yet.
[48:18] I'm going to publish it this way.
[48:19] We could do a minor release and move the number compatibility.
[48:26] That could just be internal number compatibility.
[48:30] Actually, let me go check over here real quick.
[48:32] Let's see how it's used.
[48:33] So dash keys dot encode key.
[48:37] And then version.
[48:39] We don't pass in a number.
[48:41] But we want to pass in a number.
[48:42] That's one of our issues.
[48:45] So what we could do.
[48:51] Is we could take ops.
[48:59] And we could say.
[49:00] If let version equals.
[49:06] Xpriv.
[49:08] If ops.version.
[49:14] Version equals ops.version.to string.
[49:24] Version equals version.add start to.
[49:44] Okay.
[49:47] So we could take in version as a number here.
[49:50] And then we pass it through as a string there.
[49:57] That's acceptable.
[50:02] I'm also, I am seeing the wisdom in actually moving the version.
[50:06] Out of the base 58 check entirely.
[50:11] Because that is something that is not really.
[50:14] I thought it was part of base 58 check.
[50:16] I was wrong.
[50:17] I think I'm wrong.
[50:18] I don't think the version is actually part of base 58 check.
[50:21] I think the version.
[50:23] Is part of the serialization format.
[50:28] And the check.
[50:30] It's literally just base 58.
[50:32] And then a check.
[50:33] And the version.
[50:35] Doesn't have anything to do with it.
[50:37] I think, I think I picked from a library that had implemented it.
[50:40] Slightly incorrectly.
[50:43] And continued to implement it slightly incorrectly.
[50:49] But the difference is it's important definitionally, but it's not important.
[50:53] From a practical perspective.
[51:01] All right.
[51:19] Oh, and this should be optional.
[51:41] Of course.
[51:54] Ferrison.
[51:57] Version.
[51:59] There we go.
[52:00] Cool.
[52:04] All right, so that's fixed there.
[52:05] So we don't need to carry that over into here.
[52:07] These two can have slightly different.
[52:11] Uses in terms of how they deal with the hex.
[52:15] Okay, so what do we need to fix then?
[52:30] So we don't deal with this.
[52:32] It's not a number.
[52:34] We guarantee we don't pass it in as a number.
[52:36] Because this, this is dealing with.
[52:41] Hex and I think it just.
[52:45] I could be wrong.
[52:48] Could we even transition this one into using.
[52:53] You went eight arrays.
[53:06] There's this one where you have to do.
[53:16] Version.
[53:24] Oh, oh no.
[53:26] You know what else I realized.
[53:31] When I unplugged and replugged everything earlier.
[53:36] It took my mic volume back down.
[53:39] All right, Mike volumes about to get a heck of a lot nicer.
[53:47] Okay, now I'm going to be significantly louder.
[53:51] So if the music was too loud.
[53:53] That was why and that's a problem.
[53:55] That's another problem.
[53:56] I, I bought a book on Apple script so I can start to learn Apple script.
[53:59] I got too many books, not enough time to read them.
[54:02] My, my things I'm going to do code studies on is piling up, but.
[54:08] Yeah, I don't know how I'm going to make it through that.
[54:10] Here's the book on Apple script.
[54:11] Old book, old book.
[54:18] You want to learn how to change your volume for your mic settings on your Mac.
[54:24] There you go.
[54:26] The easy guide to Apple script.
[54:29] This is third edition and it's Apple approved or some such.
[54:36] Actually, I think there was another one.
[54:38] The definitive guide.
[54:41] That one's a lot smaller.
[54:44] Oh, how am I going to find time to learn all these things?
[54:49] But I do, I do want to learn some Apple script.
[54:51] I just, I want to learn the basics of it.
[54:53] I want to learn it enough to understand because right now it's such a mystery to me.
[54:56] It makes no sense.
[54:57] It looks like plain English.
[54:58] How can anybody code in that?
[55:00] You know, because it's, it's not clear what the syntax is.
[55:04] Cause there is no syntax.
[55:05] It's just letters.
[55:08] There has to be some syntax.
[55:11] You know, there has to be some, not a hundred percent, but some anyway.
[55:22] Yeah.
[55:23] I bet if we did this with you and eight arrays, it'd be a little bit better,
[55:26] but we're definitely not going to make that change now.
[55:33] Okay.
[55:34] But all right, let's, let's get diff dash keys here.
[55:38] Oh, I need to go make that changing.
[55:42] Hold on.
[55:43] Zero X zero.
[55:44] All right.
[55:45] Get rid of all these.
[55:47] This is a bad idea.
[55:48] Dash keys is going to be in hex.
[55:51] Dash HD is going to be in numbers and it's going to be fine.
[55:58] Everyone's going to live.
[56:26] We're going to go four wheeling soon.
[56:28] It's been too long.
[56:32] Okay.
[56:33] So this little bit of code.
[56:37] This makes this a little bit more versatile and easy to use.
[56:40] Okay.
[56:41] And then I've got my last to do on this.
[56:43] Okay.
[56:44] That's what we were.
[56:45] That's what we were checking out.
[56:46] All right.
[56:47] So the question is, what are the parts?
[56:54] Maybe we don't need them.
[56:58] I like it when you can take something directly from the decode object and.
[57:03] And plug it directly into the encode object.
[57:08] That's ideal for me.
[57:10] But.
[57:14] In this particular case, I think that this is the better API.
[57:21] Because all you need from.
[57:24] This object.
[57:26] Is whatever its key is.
[57:29] And you pass it into the encode.
[57:38] And you determine by the size, what type of key it is.
[57:41] This is elegant.
[57:45] So I'm deleting the to do for parody with decode because.
[57:50] Despite the fact that you can't directly pass the one into the other.
[57:56] I think that it is the right API.
[58:02] Okay.
[58:03] So.
[58:05] That settles that.
[58:07] And we had to do pub key versus pub key.
[58:11] And I have settled that debate, by the way.
[58:18] First, let me just go ahead and.
[58:21] Get this.
[58:23] One more time.
[58:24] What are we doing here?
[58:25] We are.
[58:30] So this is feature.
[58:32] Complete.
[58:34] Key detection.
[58:36] And encode key.
[58:47] All right.
[59:07] And then let's take a look through this one.
[59:11] And what are we at in terms of version?
[59:14] Not quite one good.
[59:43] So I think what I landed on with this.
[59:47] Was.
[59:50] Let's see if I can go back here.
[59:55] Let's take a look at it.
[59:58] Dash keys.
[60:01] Last bike shed.
[60:26] It's a type is public key function is.
[60:32] To.
[60:35] Pub key.
[60:37] Right.
[60:43] Property is.
[60:45] Public key.
[60:48] Variable is.
[60:50] Public key.
[61:12] Public key to.
[61:26] Pub key hash.
[61:31] Probably want to put names here, too.
[61:36] Function is to.
[61:50] Property is.
[61:53] A key hash.
[61:55] Variable is.
[62:01] We've got.
[62:04] Is the type.
[62:07] To prove key.
[62:09] Is the function.
[62:11] Brief key.
[62:13] Is the property.
[62:15] Or private key is the property.
[62:18] Proof key.
[62:21] Proof bites is the variable name.
[62:30] So this is kind of what I'm thinking.
[62:44] So.
[63:03] Type is address function is to adder.
[63:08] Property is.
[63:10] Address.
[63:13] Variable is.
[63:14] Adder.
[63:17] A.
[63:18] Outer.
[63:20] Change.
[63:21] Other.
[63:25] See where I'm going with this.
[63:50] So these, these are, these are my.
[63:53] These are my final thoughts.
[63:57] Is that.
[63:58] It's going to be the function name is shorter.
[64:04] The property name is longer.
[64:09] And more closer to the type.
[64:24] I actually wish I could just.
[64:27] Swappy doodle these.
[64:31] Because I actually want property.
[64:35] To come over here.
[64:40] We're going to do so.
[64:41] So we'll see that there should be.
[64:43] Basically parody between the name of the type.
[64:47] And the property name.
[64:50] That's what I'm envisioning.
[65:19] All right.
[65:38] Address public key.
[65:40] Pub key hash.
[65:41] Private key.
[65:43] So we have the name of the type.
[65:46] And there's one more, which should be.
[65:48] It should be name.
[65:52] Which is address.
[65:54] This should almost always be the same as.
[65:57] Basically this is going to be.
[66:11] So is this still going to work.
[66:13] Oh, what did I do?
[66:14] I broken aided it.
[66:16] I broken aided it.
[66:25] There we go.
[66:30] So I would like to have this table.
[66:34] Up in the.
[66:36] The dash tools of.
[66:38] Here's all the things.
[66:39] And then.
[66:41] It would be good to link to the glossary for them as well.
[66:46] And this is, it should be this way across the whole ecosystem.
[66:50] Anywhere that it's referenced.
[66:52] These are, this is, this is what you can expect it to be called.
[66:57] This is the.
[66:59] Capitalization that's being used.
[67:02] So the property is closer to the type.
[67:04] So name type property.
[67:06] These are similar.
[67:07] And then function.
[67:08] Slash argument variable.
[67:09] These are going to be similar.
[67:13] Okay.
[67:14] So with that in mind, this is the last change I need to make to dash keys.
[67:17] I think.
[67:19] So param.
[67:22] Key hash.
[67:25] That can, it could take that.
[67:27] That doesn't matter because it's a parameter.
[67:29] It doesn't matter what we call it.
[67:32] But.
[67:47] Okay.
[68:11] I am.
[68:23] And then we're going to swap be doodle.
[68:26] A key to adder.
[68:30] It's going to become pub key.
[68:34] To adder.
[68:36] Final answer.
[68:46] All right. So let's take a look at this branch.
[68:53] And it's branch just a little updates here and there.
[69:07] Okay. We got bites to hex. We got hex to bites.
[69:09] But did I decide on.
[69:13] This is how I decided to use them.
[69:17] Okay.
[69:18] I think that's fair enough.
[69:21] Final answer.
[69:25] Because in the future, we could have a big end or a UN UN eight.
[69:29] Which I still don't know how to. Oh, bites. That's what we're calling.
[69:32] Duh.
[69:33] UN eight is bites.
[69:35] I need to put that in the table.
[69:53] This one's the most confusing one.
[70:15] Okay.
[70:33] So there's yeah. So generically.
[70:35] When, when.
[70:37] We say it's a buffer. It's actually a UN eight array.
[70:44] So we're going to call it key for example.
[70:48] But then we're going to call it bites.
[70:51] Okay. Good.
[70:59] And I'm going to change this to.
[71:02] Non HD to generate lossy with.
[71:24] Should I call that.
[71:29] Adder were settled on.
[71:32] Priv key to whiff, whiff to adder.
[71:35] Added a PKH.
[71:37] PKH to adder.
[71:39] Pub key.
[71:41] That one I think I just fixed priv key.
[71:43] Whiff to priv key, whiff to adder.
[71:46] Pub key to PKH.
[71:48] So we need to make sure pub key two.
[71:52] Let me fix that one first.
[71:56] Pub key two is going to become.
[71:59] Pub key to.
[72:01] Oops.
[72:04] And then let's do.
[72:06] Let's say to.
[72:08] Pub key.
[72:10] It's going to be to.
[72:12] Pub key.
[72:15] Switch that one around.
[72:17] Final answer.
[72:19] Encoding options decode.
[72:22] Decode key.
[72:24] Compressed private PKH.
[72:29] Private key pub key hash.
[72:30] That's appropriate.
[72:33] Bites to hex, hex to bites.
[72:37] Okay.
[72:46] Do I want to call it.
[72:49] Non HD.
[72:50] I think lossy.
[72:55] It's kind of the right.
[72:57] It's a little bit of a mix because it's non HD is correct.
[73:01] But lossy, I think has more of that.
[73:04] Tinge to it.
[73:06] That really.
[73:11] So let's see.
[73:17] It's not lossy in the sense that.
[73:19] Like lossy compression.
[73:21] It's lossy in the sense that.
[73:23] There's no way to rederive it.
[73:25] It is non recoverable.
[73:40] Yeah, it's lossy is not technically correct.
[73:52] I think I'll leave it since I, I don't, I don't know for sure what I would want to call it.
[73:56] I think I'm going to leave it.
[74:02] Okay.
[74:07] Do we want to change to public key to be to pub key.
[74:36] Okay.
[74:38] Okay.
[75:04] Let me see what we had over here.
[75:23] Public key.
[75:27] To public key.
[75:56] Okay.
[76:09] So currently we are using.
[76:12] To public key here.
[76:16] According to our.
[76:20] To public key here. Should this be to pub key.
[76:45] I'm going to guess on that one.
[76:54] It either has to be to public key.
[76:59] Or to pub key, which is my final answer.
[77:04] I really like the aesthetic of public key better.
[77:09] It just becomes a matter of where else pub key is used and I think that was mostly in dash TX.
[77:14] Let me check that out real quick.
[77:16] Because I think that's the main area where.
[77:21] This comes up.
[77:23] So let me, let me open up another one of these.
[77:29] Dash TX.
[77:41] Pub key hash.
[77:44] That's not nice.
[77:45] So pub key hash.
[77:46] Expanded.
[77:48] That makes sense.
[78:03] Let's see, where is it used as a property.
[78:08] Pub key.
[78:10] It's not used as a property anyway.
[78:15] It's public key when it's a property that makes sense.
[78:18] So.
[78:39] Public key.
[78:58] Script to pub key.
[79:02] Dang it, we have to choose one.
[79:04] It's either pub key 2 or it's public key.
[79:11] Can't straddle the line here.
[79:30] It mostly rests on the use of public key 2 and 2 pub key.
[79:34] Let me check this out real quick.
[79:57] Okay.
[80:25] So.
[80:33] That makes sense.
[80:47] All right, let me copy down a couple more of these.
[81:13] To PKH.
[81:28] Pub key.
[81:57] Let's try this again.
[82:02] I just want to see what it looks like.
[82:03] I know I need to reread my argument.
[82:07] That I had.
[82:19] I really like the idea.
[82:21] It's going to be pub bytes.
[82:24] Pub hex.
[82:34] Pub hex 2.
[82:56] All right, let's take a look.
[82:58] Maybe the function name being too long is really only in a few places.
[83:03] Public key to public key hash.
[83:07] That was way too long.
[83:11] Pub key to PKH makes sense.
[83:16] To public key.
[83:18] Public key to PKH I don't like.
[83:21] So I think we're going to just do.
[83:24] I don't know why I wish I could voice this.
[83:30] Because I don't like to be inconsistent.
[83:33] But I think it's going to be pub key to PKH.
[83:40] And to public key.
[83:42] And to priv key.
[83:46] Because if it was, if it was.
[83:49] Okay, let me check again.
[83:50] Do we have to priv key or do we have.
[83:53] To private key.
[84:00] To priv key.
[84:06] To priv key.
[84:08] Okay.
[84:15] Nothing goes to public key except for a private key.
[84:20] I think that it's okay.
[84:24] To have these be different.
[84:31] All right, let's take a, let's take a look at the diff.
[84:33] So I think this is good now.
[84:35] So pub key to adder.
[84:40] For better or for worse.
[84:43] All right, pub key there, adder to pub key hash.
[84:48] Okay.
[84:58] Okay.
[85:25] Okay.
[85:48] Oops. Oh, RRGSD.
[85:50] Okay.
[86:02] Oops.
[86:10] Hold on.
[86:28] Pub key hash.
[86:29] Can we look for that?
[86:32] And.
[86:35] Pub key hash.
[86:37] Okay, here's what we need to do.
[86:39] Pub key hash needs to go back to pub key hash.
[86:43] That is the proper canonical form for it.
[86:47] And pub key hash needs to go back to pub key hash.
[86:52] All right, there we go.
[87:20] All right.
[87:44] Let's normalize pub key hash and pub key.
[88:05] Okay.
[88:06] Is that really it?
[88:08] Let's push.
[88:09] Let's refresh.
[88:13] And let's see.
[88:16] Okay.
[88:37] Okay.
[89:02] Pub key to adder, priv key to whiff, whiff to priv key, whiff to adder, pub key to PKH.
[89:08] Did I already do that one?
[89:10] Pub key to adder.
[89:12] Ah, right, because pub key can only go to PKH.
[89:19] Pub key can go to adder, but.
[89:21] Got it.
[89:23] Decode, encode.
[89:28] Write to public key.
[89:46] Okay.
[89:51] I'll swappy doodle this one.
[90:15] Private key to whiff will be priv key to whiff.
[90:44] Okay.
[90:57] Hmm.
[91:26] Whiff to adder does not exist.
[91:54] Oh, apparently it's not been defined.
[92:05] Okay.
[92:06] Wait.
[92:07] Oh, it is defined.
[92:10] I'm so confused.
[92:39] Ah, why is it?
[92:49] Why is it freaking out?
[92:50] Stop freaking out.
[93:13] All right, so this is missing.
[93:37] Ah, that noise.
[93:41] Kind of rings in the ears a little bit.
[94:08] Okay.
[94:21] Pub key to adder.
[94:25] Pub key to PKH.
[94:53] Ah, this is something I need to update.
[94:56] So the type in wherever that was.
[95:04] So the type of the function is address to pub key hash.
[95:11] Type of this function is public key to pub key hash.
[95:19] Oh, that's not the name, that's the type.
[95:23] Let me fix that.
[95:24] So types are longer.
[95:44] I don't have whiff to.
[95:50] I don't know.
[95:51] Maybe I've got some extraneous stuff with the type system.
[96:13] All right.
[96:33] Pub key hash to address.
[96:58] What is this one?
[97:23] Conqueror's Bad Fur Day?
[97:25] Xerox.
[97:26] Salad memories.
[97:28] Interesting.
[97:29] I like it.
[97:58] Okay.
[98:24] PKH to adder.
[98:25] Private key to whiff.
[98:28] Oh, we still need that one.
[98:32] So we're going to do private key to whiff.
[98:37] So priv key to whiff.
[98:41] And then priv key to adder.
[98:54] PKH and utils.
[98:56] Okay.
[98:57] So now I think I've completed the missing types on that one.
[99:01] That's good.
[99:30] Okay.
[99:54] Okay.
[100:23.00] All right.
[100:40.00] There goes.
[101:02.00] What to do's do we have here?
[101:05.00] Solve those.
[101:06.00] Boom.
[101:07.00] Done.
[101:08.00] All right.
[101:09.00] So before I publish that, however, I do need to actually publish this.
[101:22.00] All right.
[101:25.00] So what are we at here?
[101:32.00] Since I am tracking sec p256k1, we're going to leave this pre-release version as the actual
[101:39.68] version that we're going to go with.
[101:43.24] Because that's going to bump to two, and then I'm going to have to, well, not have to, but
[101:47.08] I'm going to want to bump these to two as well.
[101:54.00] Oh, except that we decided that we're not actually going to list this as a dependency.
[102:19.00] Because it is up to the individual to decide.
[102:26.00] Okay.
[102:32.80] It was save dev.
[102:35.00] Okay.
[102:36.00] So it is a dev dependency.
[102:37.00] Fair enough.
[102:38.00] All right.
[103:01.00] Is the read me clear enough on that?
[103:15.00] Yes, it is.
[103:19.00] Oh, except that it's not right here.
[103:22.00] Let me double check on this.
[103:25.00] So this should be at 1.7.
[103:32.00] Just 1.x.
[103:38.00] Make sure that's correct.
[103:42.00] Does it resolve?
[103:47.00] Okay, yes, that resolves.
[103:50.00] That's good enough for me.
[104:19.00] And I like to always put the version number in there, because I mentioned this before,
[104:28.00] when it gets copied to tutorials and such, you want the tutorial to match.
[104:34.00] When people follow the tutorial that somebody copies this from, you want it to match.
[105:01.00] So what is this?
[105:29.00] NPM, run, bump, and we're going to bump major.
[105:49.00] We're bumping major.
[105:53.00] There it goes, folks.
[105:59.00] Press enter, open your browser.
[106:07.00] Of course, it always opens the wrong browser.
[106:11.00] It doesn't matter which browser I've got in focus.
[106:14.00] It's always 100% of the time going to open the wrong browser.
[106:19.00] Just never accidentally open the correct browser.
[106:23.00] Not as of yet.
[106:42.00] All right, there we go.
[106:44.00] And push!
[106:48.00] That needs a double.
[106:54.00] Okay.
[106:56.00] That's it, 1.0, baby.
[106:59.00] It's out.
[107:01.00] Can't stop it now.
[107:05.00] Okay, so from Dash Keys.
[107:10.00] Next step in line, if I remember my to-dos here.
[107:24.00] All right.
[107:26.00] Secp256k1, we're not worrying about the raw RNS yet.
[107:30.00] We'll worry about that when we get to Dash Message.
[107:35.00] Dash Keys, we got the detection in.
[107:39.00] We handle the version number versus version string.
[107:42.00] Let's go check out Dash Phrase.
[107:45.00] Oh, there might have been one other thing that I need to check out about Dash Keys.
[107:50.00] Just the way that it's exported, just to make sure that it's exported correctly.
[107:58.00] Hold on.
[108:12.00] Where are we?
[108:26.00] Okay.
[108:28.00] Okay.
[108:38.00] Okay.
[108:48.00] Okay.
[109:08.00] Good, that's all just two pubkey hash, just the way that it should be.
[109:35.00] Okay.
[109:40.00] Let's see.
[110:08.00] So pubkey hash, pubkey.
[110:11.00] We all have an easy to steamish shape at a glance.
[110:14.00] And with tab autocomplete tooling.
[110:20.00] Let's do it.
[110:30.00] Let's do it.
[110:58.00] Let's see here.
[111:27.00] Okay.
[111:53.00] What was I doing right here?
[111:57.00] Oh, I just wanted to see.
[111:59.00] I just wanted to make sure that the export was window.DashKeys.
[112:05.00] Or global this.DashKeys.
[112:07.00] Or .DashKeys.
[112:12.00] Dang it.
[112:21.00] The window object.Module.Export=DashKeys.
[112:42.00] Did we seriously forget to export?
[112:51.00] No, okay.
[112:52.00] It's exported here by virtue of being declared as a var.
[112:56.00] That's how it's exported.
[112:57.00] Got it.
[112:58.00] Okay.
[112:59.00] So this is ready for the Jojobite fix.
[113:18.00] We're in the pull request.
[113:38.00] This is a done deal.
[114:04.00] Okay, let's see here.
[114:19.00] Let's see here.
[114:48.00] Let's see here.
[115:12.00] So let's go make dash rays hit V1 if it hasn't already.
[115:23.00] There's only one thing I'm concerned about right now.
[115:27.00] And that is dash rays should be this.
[115:34.00] This.
[115:35.00] Have we already hit V1 with this?
[115:38.00] Yes, we have.
[115:40.00] Okay.
[115:43.00] So we're just going to do both then.
[116:10.00] Okay.
[116:39.00] All right.
[116:55.00] Let's just.
[116:56.00] Well, how much left do we have to do?
[116:58.00] Okay.
[116:59.00] Let's look for.
[117:01.00] Let's try dash rays.
[117:06.00] Dash rays.
[117:09.00] So that one we're going to leave this one, this one, this one, this one, this one, this
[117:35.00] one.
[117:45.00] Oh, whoops.
[117:52.00] I don't know how to address that.
[117:55.00] Something in my head.
[118:20.00] This and ignore next line.
[118:48.00] Okay, good.
[118:51.00] Okay.
[119:01.00] Okay.
[119:23.00] Dash rays.
[119:28.00] Dash rays.
[119:31.00] Old name kept for browser.
[119:41.00] Let's see.
[119:58.00] Dash rays.
[120:27.00] All right.
[120:41.00] So that one's done.
[121:10.00] Okay.
[121:22.00] Was there anything else that needs to be done with this?
[121:28.00] Let's go back to dash phrase real quick.
[121:42.00] Okay.
[121:43.00] So this is actually going to be our first release of this.
[121:49.00] So we actually can get rid of.
[121:54.00] This is our first non pre-release.
[121:57.00] So this includes the rebrand.
[122:00.00] Right.
[122:07.00] Or no.
[122:11.00] NPM dash phrase.
[122:14.00] Let's see.
[122:20.00] Take a look at versions.
[122:21.00] Five versions.
[122:25.00] Okay, so this is beyond that.
[122:28.00] All right, nevermind.
[122:29.00] We're going to keep this the way that it is.
[122:49.00] Anyway.
[123:06.00] Okay.
[123:07.00] And do I have a little test?
[123:08.00] I do.
[123:10.00] Good, good, good.
[123:36.00] Okay.
[123:47.00] Pretty good.
[123:49.00] NPM bump.
[123:51.00] Minor.
[124:00.00] That's what I wanted.
[124:08.00] I think I wanted.
[124:12.00] Match maybe.
[124:41.00] Nope, we don't want to beta tag that.
[124:43.00] We just want to let it go.
[124:48.00] Let's see that last one.
[124:49.00] We didn't beta tag it, did we?
[124:50.00] When we did the git push.
[124:53.00] Okay, good.
[124:54.00] No beta tag.
[124:55.00] Excellent.
[124:57.00] All right.
[125:00.00] So I will open this over in the browser.
[125:07.00] Use my security key.
[125:12.00] Publish.
[125:13.00] Boom.
[125:14.00] All right.
[125:23.00] So 1.3.
[125:26.00] 1.0.
[125:28.00] 1.7.
[125:34.00] Custom.
[126:00.00] And we need to go to check out main git rebase chore types.
[126:07.00] Git push.
[126:09.00] Make sure we did that over here, right?
[126:11.00] We did the git push.
[126:12.00] Yeah, we did.
[126:13.00] Good.
[126:14.00] Okay.
[126:15.00] So there it is.
[126:24.00] All right.
[126:25.00] Dash HD, here we come.
[126:29.00] We've got a V1.0 and we're coming for you.
[126:43.00] All right.
[126:44.00] So we still have this issue of derive key.
[126:47.00] So we've got derive key.
[126:49.00] Oh, and I was going to check the bit 44 to get some clarification on this.
[126:55.00] There's a bit 44 that I was going to, I think it was bit 44.
[127:02.00] Account index.
[127:16.00] Address.
[127:29.00] Okay.
[127:30.00] I think I'm going to go with derive address.
[127:34.00] Because I don't like having derive key, derive X key, and just -- so we're going to move over to derive address.
[127:46.00] And we're going to expose the serialization methods.
[127:50.00] So that's what we've got.
[127:52.00] That's what we've got left.
[128:12.00] Okay.
[128:37.00] Index pass version to dash keys.
[128:51.00] Update comments.
[128:52.00] That's it.
[128:54.00] Oh, I'm sorry.
[128:55.00] I have not been looking at the chat in a while.
[128:58.00] Oh, okay.
[129:01.00] There's nothing there.
[129:03.00] Y'all are not saying anything.
[129:05.00] I'm being quiet.
[129:07.00] You can say hello.
[129:14.00] All right.
[129:15.00] What was I going to do?
[129:17.00] I had a specific thing that I was just looking at.
[129:21.00] It was in my to-dos, wasn't it?
[129:24.00] Ah, yes.
[129:25.00] I'm going to rename derive key all over the place.
[129:42.00] Wait, derive keys?
[129:43.00] What the heck was that?
[129:46.00] Hold on.
[129:51.00] What is this?
[129:52.00] Derive key.
[130:06.00] Where did that belong?
[130:14.00] That belongs right there.
[130:23.00] Oh, whoops.
[130:24.00] Another thing.
[130:26.00] I hope that I had this in there.
[130:28.00] Do we have the files?
[130:29.00] Yes.
[130:30.00] Dash phrase.
[130:31.00] Do we have anything else?
[130:39.00] No.
[130:40.00] Good.
[130:41.00] In this one, do we have files in there?
[130:44.00] Try to always make sure that files is specified.
[130:47.00] Good.
[130:48.00] Do we have anything else that we needed?
[130:51.00] No, I don't think so.
[130:59.00] Okay.
[131:05.00] Now, we probably need to have a minify step for all of these that we need to have work across them.
[131:14.00] Okay, so what is this?
[131:20.00] Rebecca dash keys.
[131:29.00] I'm getting a little tired.
[131:31.00] I need to get to bed.
[131:33.00] But I will not go to bed before this is published.
[131:35.00] It will be published tonight.
[131:38.00] It will be published now.
[131:45.00] All right, tests are passing.
[131:48.00] So, we're going to do derive key.
[131:53.00] It's going to become derive address.
[132:00.00] Final answer.
[132:04.00] Done.
[132:33.00] Looks good.
[132:44.00] Okay.
[132:45.00] And then run test still works.
[132:49.00] Example still works.
[132:50.00] Excellent.
[132:52.00] And then I wanted to take a look at HD.
[133:01.00] Let's see.
[133:19.00] Drive key, should be nothing, good.
[133:33.00] Drive key.
[133:35.00] Okay, that's appropriate.
[133:36.00] Drive address.
[133:37.00] HD key.
[133:38.00] Oops.
[133:44.00] That's one of the things I was looking for.
[134:12.00] Okay.
[134:31.00] Apparent fingerprint stays.
[134:34.00] I don't know what else to call it.
[134:36.00] Well, actually, let me think again about that.
[134:41.00] Let's look at BIP.
[134:43.00] Is it fingerprint?
[134:45.00] No.
[134:46.00] It must be BIP32.
[134:48.00] Because if I can rename it from parent fingerprint to just fingerprint, that's better for me.
[134:56.00] First 32 bits of the identifier.
[134:59.00] Fingerprint of the parent's key.
[135:02.00] Okay, yeah, parent fingerprint fits.
[135:22.00] Internally the 160-bit identifier could be used.
[135:36.00] Parent fingerprint, parent fingerprint.
[135:50.00] First 32 bits.
[135:54.00] So this is confusing because it says both.
[135:59.00] Oh, the first 32 bits of the identifier are called the fingerprint.
[136:04.00] Parent fingerprint.
[136:05.00] Okay.
[136:06.00] Locked and loaded.
[136:07.00] Done.
[136:08.00] This is the way.
[136:23.00] Alright, so the last thing is get xpriv, get xpub or whatever we want to call that.
[136:29.00] Just doing the serialization.
[136:55.00] That's in general all these changes.
[137:02.00] Okay.
[137:05.00] Oh, that's no good.
[137:24.00] Okay.
[137:28.00] Okay.
[137:32.00] Okay.
[137:36.00] Okay.
[137:40.00] Okay.
[137:44.00] Okay.
[137:48.00] Okay.
[137:56.00] Okay.
[138:00.00] Okay.
[138:05.00] Okay.
[138:09.00] Okay.
[138:13.00] Okay.
[138:17.00] That's weird.
[138:24.00] I swore they weren't going to pass.
[138:36.00] I thought they weren't going to pass because when I did a reinstall over top of the -- oh,
[138:42.00] because I didn't do an npmci.
[138:44.00] So it didn't blow it all away.
[138:45.00] Maybe.
[138:47.00] Maybe that's why.
[139:04.00] Okay.
[139:06.00] So there's all of that.
[139:11.00] And...
[139:19.00] Okay.
[139:20.00] So what was left?
[139:22.00] We're going to do this one.
[139:24.00] Then we're going to update the dependencies.
[139:26.00] And that is the final step before we publish this is we have to update the dependencies and then there's going to be a number of methods that need to be renamed and whatnot.
[139:37.00] But we should be good.
[139:41.00] Okay.
[139:47.00] So let's update that example derive test.
[140:07.00] Okay.
[140:35.00] Okay.
[140:40.00] Okay.
[140:50.00] Okay.
[141:10.00] Okay.
[141:36.00] Okay.
[141:40.00] Now...
[141:44.00] If I go back to -- what was it?
[141:47.00] Where's that one where I -- the start bit?
[141:55.00] There's a lot of places where that key start is there.
[141:58.00] So if I got rid of this, it should fail.
[142:02.00] Excellent.
[142:04.00] That's what I wanted to see.
[142:05.00] Just wanted to make sure that it can indeed fail.
[142:09.00] There we go.
[142:11.00] Okay.
[142:13.00] Okay.
[142:17.00] Okay.
[142:22.00] Okay.
[142:26.00] Okay.
[142:30.00] Okay.
[142:34.00] Okay.
[142:38.00] Okay.
[142:51.00] All right.
[142:53.00] Now what I want to do is --
[143:01.00] Oh, that's not what I want.
[143:29.00] Okay.
[143:38.00] Okay.
[144:07.00] Let's see.
[144:12.00] Where are we at?
[144:25.00] Get that test.
[144:47.00] Okay.
[144:48.00] Now test.
[144:49.00] Great.
[144:54.00] So now we got that in place.
[144:55.00] Let's check out the serialize.
[144:58.00] And I just want to expose this, really.
[145:09.00] I just don't know what to call it.
[145:10.00] I guess I should check and see serialization format.
[145:26.00] They call it serialization format.
[145:44.00] Hmm.
[145:47.00] Maybe just two bytes.
[145:49.00] Would that be fair?
[145:58.00] Can I call it two X bytes?
[146:26.00] Okay.
[146:31.00] Okay.
[147:00.00] And then the question is, which bytes do you want?
[147:28.00] So maybe it's two X bytes.
[147:57.00] Okay.
[147:58.00] Hmm.
[148:01.00] Hmm.
[148:30.00] Okay.
[148:31.00] Okay.
[149:00.00] All right.
[149:21.00] There we go.
[149:22.00] So two X bytes.
[149:25.00] Okay.
[149:54.00] There we go.
[150:21.00] So there's that.
[150:23.00] And then we can just have --
[150:26.00] Let X proved bytes equals X proved bytes dash HD dot two X bytes.
[150:55.00] Okay.
[151:00.00] Okay.
[151:19.00] All right, there we go.
[151:31.00] So we got that one done.
[151:33.00] I need to go put the type on this so that it stops freaking out.
[152:02.00] Okay.
[152:04.00] Okay.
[152:32.00] Okay.
[153:00.00] This one's not the right one.
[153:05.00] That's okay.
[153:06.00] This one is the right one.
[153:20.00] So I'll have X proved and X proved bytes, and we will just return dash HD dot --
[153:31.00] These will be public-ish.
[153:37.00] Two X bytes.
[153:45.00] I'll just return it like this and like that.
[153:54.00] And I wonder if it should be -- should it be a get or a to?
[154:19.00] Hey, should this throw an error?
[154:24.00] I don't remember why it's not throwing an error.
[154:25.00] Oh, I do.
[154:26.00] I do know why this is not throwing an error.
[154:47.00] Missing private key.
[155:15.00] Oh, the reason -- sorry, I forgot to say what the reason was.
[155:18.00] The reason was because this was originally part of the JSONification mechanism, and that's been done away.
[155:45.00] So now that it's been done away, I kind of want to put this down below because it's just kind of a helper.
[156:08.00] Two X proved -- two X proved bytes.
[156:13.00] That's what we needed.
[156:15.00] Just that right there.
[156:30.00] Sorry that YYs is complaining.
[156:59.00] Sorry that YYs is complaining.
[157:28.00] All right, why is this so -- why is this so gripey?
[157:39.00] Why can't I find it?
[157:40.00] It's defined right here.
[157:46.00] Oh, whoops.
[157:48.00] Dang it.
[157:50.00] Because I get confused, that's why.
[157:53.00] I don't know why we need those extra brackets.
[157:57.00] They don't carry any meaning.
[158:00.00] I don't know why we need that.
[158:02.00] That's a good question.
[158:04.00] I don't know why we need that.
[158:06.00] I don't know why we need that.
[158:08.00] I don't know why we need that.
[158:10.00] I don't know why we need that.
[158:12.00] I don't know why we need that.
[158:14.00] I don't know why we need that.
[158:43.00] I don't know why we need that.
[159:10.00] Let's see here.
[159:18.00] How's it going, everybody?
[159:32.00] Why is this -- why is this griping?
[159:57.00] Why is this griping?
[160:24.00] Oh, hey, just me.
[160:30.00] Going to learn via osmosis.
[160:32.00] Are you woodworking again in the middle of the night?
[160:35.00] It's about time for me to go to bed.
[160:37.00] Darn it.
[160:42.00] Will throw ethanol.
[160:51.00] Wait, why is this not griping?
[161:08.00] Oh, because those are hub keys.
[161:11.00] All right, got it.
[161:19.00] Key bytes is possibly null.
[161:25.00] There we go.
[161:27.00] Not anymore, sucker!
[161:32.00] What now?
[161:51.00] All right, there we go.
[161:59.00] Now that looks about right.
[162:03.00] Make sure -- oh!
[162:16.00] Good.
[162:36.00] I'm a little confused as to how there's a problem here.
[162:42.00] But let's take a look at it.
[162:46.00] So HD public key, encode pub bytes.
[163:03.00] Okay, where is this?
[163:16.00] Okay, what?
[163:17.00] What the heck just happened?
[163:20.00] What? It was working!
[163:23.00] All right, two X bytes.
[163:24.00] HD key, HD key private key.
[163:27.00] No problem there.
[163:28.00] X priv bytes, X priv bytes encode.
[163:33.00] That should be the exact same thing.
[163:36.00] No magic here.
[163:38.00] All right, two X priv bytes, two X bytes.
[163:43.00] It's just private key or public key on either of these.
[163:50.00] So I'm really not clear -- it is the exact same code, is it not?
[163:58.00] Key bytes.
[164:01.00] All right, let's run our little test here and see what's going on.
[164:07.00] Invalid bytes length undefined.
[164:10.00] Must be 20 blah, blah, blah, blah, blah, blah, blah.
[164:14.00] So it sounds like I'm not -- I'm either not calling the right method or I'm not passing in the bytes.
[164:21.00] So two X priv, get wallet keys and test.
[164:27.00] 304. Okay, 304. Where are we at?
[164:47.00] Oh, let's get rid of the async on this.
[164:50.00] That is not necessary.
[164:53.00] In fact, it's quite bad.
[164:56.00] Oh, there we go.
[165:00.00] Gets me every time, every time, every time.
[165:11.00] All right, and test needs to be updated.
[165:28.00] Should it return null and not throw?
[165:36.00] Let's see.
[165:44.00] If you think that you have a private key and you actually have a public key, I disagree.
[166:04.00] I think it should throw.
[166:08.00] Okay.
[166:12.00] [ Music ]
[166:17.00] [ Music ]
[166:25.00] [ Music ]
[166:30.00] [ Music ]
[166:38.00] [ Music ]
[166:43.00] [ Music ]
[166:48.00] [ Music ]
[166:55.00] That's weird.
[167:10.00] [ Music ]
[167:35.00] I'm a little confused by this.
[167:45.00] [ Music ]
[168:10.00] Two X priv, missing.
[168:16.00] Oy.
[168:20.00] Dang on testing frameworks.
[168:29.00] Hi and bye. Okay.
[168:32.00] So how do we give it two X priv?
[168:42.00] [ Music ]
[169:06.00] Private data, set private key to null.
[169:16.00] I'm a little confused about this.
[169:21.00] Let's try that test again.
[169:24.00] Hmm.
[169:34.00] Should not have private data.
[169:39.00] Key bytes null.
[169:42.00] How, what?
[170:06.00] Okay, that doesn't make sense.
[170:09.00] I was going to tell me.
[170:22.00] Okay, key bytes, key bytes to null.
[170:26.00] And then by and then should throw.
[170:30.00] What the letter L?
[170:39.00] It should throw right away.
[170:43.00] Right, okay, let's.
[171:12.00] Okay.
[171:14.00] Error.
[171:15.00] Should throw.
[171:16.00] Missing key bytes.
[171:22.00] But it does throw.
[171:24.00] So why is it so confused?
[171:30.00] Assert, rejects.
[171:58.00] Ugh.
[172:27.00] Oh wait, maybe it should be like this.
[172:31.00] Await, assert, rejects.
[172:34.00] Huh?
[173:03.00] Okay.
[173:14.00] So if did not reject, it's not equal to error.message.
[173:22.00] Then throw E.
[173:24.00] There we go.
[173:31.00] Missing key bytes.
[173:43.00] So confused.
[173:44.00] It says it should throw.
[173:46.00] Should throw.
[173:48.00] Oh, there's probably another one.
[173:50.00] But no, we should be one viewer at least.
[174:07.00] Private key is null.
[174:25.00] 293.
[174:35.00] I'm so confused.
[174:51.00] Oh, just get rid of that.
[175:08.00] So it was the assert.okay that was happening beneath.
[175:28.00] And then assert.rejects.
[175:37.00] We probably can put this in now.
[175:47.00] Copy that.
[175:51.00] And then get rid of it.
[176:17.00] NPM run test.
[176:20.00] So that test, okay good.
[176:23.00] So we actually can swappy doodle the wipe private data should not have private data.
[176:32.00] To xprev so we can assert rejects because we actually want this to reject.
[176:55.00] Not have private data.
[177:03.00] Wait assert.rejects.
[177:32.00] Okay, there we go.
[177:46.00] So it updated the pass again, good.
[178:14.00] Okay, so xprev.
[178:43.00] Okay.
[179:01.00] So raw, xprev.
[179:30.00] Oh, maybe missing the version header.
[179:36.00] I might should have that.
[179:44.00] I think it actually is supposed to have that let me go check serialization over here.
[180:01.00] Let me check BIP, is it BIP-44?
[180:04.00] Or BIP-32? No, BIP-32.
[180:07.00] All right, serialization format.
[180:10.00] Okay, so it should have the bytes in the serialization.
[180:15.00] All right.
[180:44.00] Okay.
[181:13.00] Okay.
[181:16.00] Hmm.
[181:18.00] Hmm.
[181:37.00] Hmm.
[182:06.00] Let's see.
[182:24.00] All right, I see where I have a problem here and I'm not going to be able to fix that right now.
[182:37.00] So...
[183:05.00] I think...
[183:08.00] I think this is my problem with the base 58 check modifications I made, which I'm not going to undo right now.
[183:17.00] But I think what I need to allow for is the version to be specified at a different layer.
[183:26.00] Let me think about this.
[183:27.00] Okay, it is 3:08 a.m.
[183:33.00] Um...
[184:02.00] All right.
[184:04.00] Okay.
[184:06.00] Okay.
[184:11.00] Okay.
[184:38.00] So this is what we need.
[184:48.00] We need a data view.
[185:12.00] All right.
[185:41.00] Let's see, where's the version I need to set?
[186:07.00] So basically, this one, yeah, that's all right.
[186:19.00] And then this one is going to be the same.
[186:22.00] Let me let expo bytes.
[186:36.00] So it'll be usable. It'll be usable for debugging purposes.
[186:56.00] But if I want to fix it up, I need to go back and rework a little bit of the base 58 check code.
[187:03.00] I need to actually understand base 58 check a little bit better.
[187:11.00] I may need to have some sort of way of kicking that can down the road a wee bit.
[187:22.00] Where the data goes in a different place.
[187:30.00] Have the version go directly on to at least xprevs and xpubs as it was before.
[187:38.00] I kind of fixed it to shim it, but then didn't actually fix it.
[187:41.00] You know, xprv xpub.
[187:59.00] Okay.
[188:02.00] Test drive. What?
[188:04.00] Oh, whoops.
[188:06.00] Test. Excellent.
[188:08.00] Cool.
[188:31.00] All right. So this is feature direct.
[188:41.00] Export raw.
[188:43.00] X key bytes.
[188:57.00] Okay, there we go.
[188:58.00] Now that one's done.
[189:00.00] Okay, last thing.
[189:02.00] We need to save.
[189:06.00] Dash keys at latest.
[189:10.00] Now we're going to break all sorts of stuff.
[189:13.00] And then what else do we need?
[189:17.00] Just dash keys.
[189:31.00] Save dev on dash keys.
[189:35.00] How long have I been coding tonight?
[189:37.00] Or how long have I been coding in my lifetime?
[189:41.00] What's up?
[189:43.00] Schumacht.
[189:54.00] All right. I expect this to fail miserably.
[189:58.00] That's not what I expected.
[190:05.00] Hmm.
[190:20.00] I think the reason that it didn't fail miserably is that all the changes that I made in dash keys were actually self-consistent.
[190:28.00] I didn't NPM CI before so it didn't delete the version of dash keys that I had with the local modifications with the patch that was in the published version.
[190:43.00] So that's how I managed to escape this this whole time so we verified that the patch works.
[190:48.00] And that all of the internally consistent changes are internally consistent for what's needed here.
[190:56.00] In general.
[190:59.00] And both work.
[191:01.00] So tonight I've been coding for...
[191:06.00] I don't know. Over 15 years.
[191:14.00] My first job where programming was a part of the job that I made part of a job.
[191:22.00] Was when I graduated high school. I worked at a high school managing the AV cart and I modified some software.
[191:32.00] It was called MRBS meeting room booking system.
[191:36.00] So that rather than booking rooms it booked carts and so I changed the name the names of the rooms to be the names of the cart with 32 inch TV plus VCR 27 inch TV plus DVD or something like that.
[191:58.00] I don't remember exactly how I did it. And then I changed it so that the appointments they were still by time but rather than a person scheduling the room it was a room scheduled the cart.
[192:16.00] And that was my that was my forehand programming. Well I mean I did some programming before then but that was when I started getting serious.
[192:26.00] I did in high school.
[192:30.00] Add a one line change to a scanner driver to make my scanner work in Linux with some coaching from the person who wrote the driver because I just tried to copy and paste one line to another line.
[192:46.00] And then that didn't work out. And because I had to increase the size of the array as well.
[192:56.00] But I didn't know anything back then. So there's that.
[193:00.00] But then when I went to college I kind of bootstrapped from two things one going to meetups. And that was really good. That was really the most important thing.
[193:14.00] But then just learning learning Java and learning the the incorrect way of doing object oriented programming was a good springboard to later learning the correct way to do object oriented programming.
[193:29.00] OK.
[193:36.00] So we got two X bytes. I was looking for dash keys in here.
[193:43.00] OK. Decode. Encode. Encode.
[193:47.00] Ripe in the encode encode decode and we're wrapped back around. OK.
[193:55.00] So yeah. So none of the things that changed in.
[194:00.00] Dash keys are things that we depended on here.
[194:03.00] So then this just becomes a really simple chore.
[194:07.00] Update depths.
[194:13.00] And then from there.
[194:17.00] Define basic level stuff.
[194:20.00] But good for you for starting.
[194:22.00] Remember the best time to start programming is 20 years ago and the second best time is now.
[194:37.00] I happen to get in on it early.
[194:44.00] All right. So.
[194:49.00] Whole bunch of commits here.
[194:57.00] We had some sort of midway point.
[195:12.00] All right.
[195:14.00] Well.
[195:17.00] This is it.
[195:18.00] I'm feeling good about it.
[195:20.00] Tester passing.
[195:23.00] We're going to bump this to.
[195:28.00] 3.0.
[195:40.00] HTML CSS and JavaScript. I have ideas I want to build. That's awesome.
[195:44.00] You should have ideas of things you want to build. That's great.
[195:47.00] Completed most of free code camp.
[195:49.00] But sometimes I'm still confused with laying out websites properly with CSS and HTML.
[195:54.00] That's a good sign.
[195:55.00] You might make a good programmer.
[195:57.00] If you're confused about CSS and HTML, you might make a good programmer.
[196:01.00] If you felt really good about CSS and HTML.
[196:04.00] Then I would say that you probably are not going to make a good programmer.
[196:08.00] Because you can.
[196:10.00] You kind of have one mindset or the other.
[196:12.00] CSS and HTML.
[196:14.00] Don't follow a set of rules.
[196:17.00] That's you can't envision in your head.
[196:20.00] Okay. This is what I want the output to be.
[196:23.00] And then have it be that thing.
[196:26.00] Or at least I don't think I met anybody that can do that.
[196:29.00] Because it's not logical.
[196:30.00] It's experimental.
[196:31.00] You play with it back and forth.
[196:34.00] Until it happens to work.
[196:36.00] Whereas programming is something that it makes sense.
[196:40.00] Because it's logical.
[196:41.00] Because if you follow the steps from beginning to end.
[196:44.00] You can arrive at a guaranteed conclusion.
[196:47.00] And you can know before you run the code.
[196:50.00] What the result is going to be.
[196:53.00] CSS you can't really do that.
[196:55.00] You have to.
[196:56.00] The only way to see it.
[197:00.00] But CSS is more like empirical science.
[197:06.00] What I mean by that is.
[197:08.00] Empirical science.
[197:10.00] The real world.
[197:11.00] The way the universe actually works.
[197:13.00] Is that you never know what's going to happen until you do it.
[197:15.00] You don't know when you mix two metals together.
[197:17.00] Are they going to have a higher melting point?
[197:20.00] Or a lower melting point?
[197:22.00] Are they going to be more conductive?
[197:23.00] Or less conductive?
[197:24.00] Is it going to be stronger?
[197:26.00] Or weaker?
[197:28.00] The truth is you just don't know.
[197:32.00] How are you going to take two metals with higher melting points.
[197:35.00] Bismuth and lead.
[197:37.00] And then end up with something that melts in your hand.
[197:40.00] Right?
[197:41.00] Well, it doesn't quite melt in your hand.
[197:43.00] But still.
[197:45.00] The real world.
[197:47.00] You can never know what the result is going to be.
[197:49.00] Unless you try it.
[197:51.00] There are laws and rules that we discover.
[197:54.00] But gallium nitride chargers were only discovered within the last couple of years.
[197:59.00] We've had computers for many, many decades.
[198:02.00] And we only just recently discovered gallium nitride chargers.
[198:06.00] And that is because in the real world.
[198:08.00] There is no predictability.
[198:10.00] You have only the faintest of idea how two things may interact.
[198:14.00] But in the world of logic.
[198:17.00] It's all made up.
[198:19.00] There's nothing real about the logical world.
[198:22.00] It's all completely fake.
[198:24.00] And so you can have in your head an idea.
[198:27.00] And take it through a thought experiment.
[198:31.00] And at the end of the thought experiment.
[198:33.00] You can arrive at what the conclusion will be.
[198:35.00] Based on principles of logic.
[198:37.00] That the same shared principles of logic.
[198:40.00] That have nothing to do with the real world.
[198:42.00] You can share with anybody else.
[198:43.00] And they can understand them.
[198:44.00] And computers, thankfully.
[198:46.00] Are built upon.
[198:47.00] Well, they're built upon the real world.
[198:49.00] In the sense that.
[198:50.00] We have gallium nitride.
[198:52.00] And we have potassium doped silicate.
[198:56.00] What's that?
[198:58.00] Silicate?
[198:59.00] Silicate?
[199:00.00] Whatever.
[199:01.00] Anyway.
[199:02.00] We've got all those things that make it up.
[199:04.00] But.
[199:05.00] Within a degree of tolerance.
[199:07.00] It can produce the fake world for us.
[199:09.00] That operates according to predictable nature.
[199:12.00] And that.
[199:16.00] That's where I want to be.
[199:18.00] Yeah.
[199:19.00] Real world?
[199:20.00] No.
[199:21.00] Owl City said it quite well.
[199:22.00] I can't remember it off the top of my head.
[199:24.00] But it was.
[199:27.00] Reality is a lovely place.
[199:28.00] But I wouldn't want to live there.
[199:35.00] Okay.
[199:36.00] So, I think this is done.
[199:39.00] I need to work on the CLI stuff.
[199:41.00] But these are.
[199:43.00] These are published.
[199:48.00] We're going to get these published.
[199:51.00] So, NPM.
[199:52.00] NPM.
[199:53.00] Run.
[199:54.00] Bump.
[199:55.00] Major.
[199:56.00] Hey!
[199:57.00] Vaxoril.
[199:58.00] What's up?
[199:59.00] Thanks for the follow.
[200:00.00] I am.
[200:01.00] I am just about to get off.
[200:02.00] And I apologize.
[200:03.00] We will not be able to raid.
[200:04.00] Because the channel is still under a month old.
[200:05.00] Hey!
[200:06.00] Shemacht!
[200:07.00] You too.
[200:08.00] That's awesome.
[200:09.00] Thank you.
[200:10.00] I'm going to go ahead and get off.
[200:11.00] I'm going to go ahead and get off.
[200:12.00] I'm going to go ahead and get off.
[200:13.00] I'm going to go ahead and get off.
[200:14.00] I'm going to go ahead and get off.
[200:15.00] I'm going to go ahead and get off.
[200:16.00] I'm going to go ahead and get off.
[200:17.00] I'm going to go ahead and get off.
[200:18.00] I'm going to go ahead and get off.
[200:19.00] I'm going to go ahead and get off.
[200:20.00] I'm going to go ahead and get off.
[200:21.00] I'm going to go ahead and get off.
[200:22.00] I'm going to go ahead and get off.
[200:50.00] I'm going to go ahead and get off.
[200:52.00] I'm going to go ahead and get off.
[200:53.00] I'm going to go ahead and get off.
[200:54.00] I'm going to go ahead and get off.
[200:55.00] I'm going to go ahead and get off.
[200:56.00] I'm going to go ahead and get off.
[200:57.00] I'm going to go ahead and get off.
[200:58.00] I'm going to go ahead and get off.
[200:59.00] I'm going to go ahead and get off.
[201:00.00] I'm going to go ahead and get off.
[201:01.00] I'm going to go ahead and get off.
[201:02.00] I'm going to go ahead and get off.
[201:03.00] I'm going to go ahead and get off.
[201:04.00] I'm going to go ahead and get off.
[201:05.00] I'm going to go ahead and get off.
[201:06.00] I'm going to go ahead and get off.
[201:07.00] I'm going to go ahead and get off.
[201:08.00] I'm going to go ahead and get off.
[201:09.00] I'm going to go ahead and get off.
[201:30.00] I'm going to go ahead and get off.
[201:57.00] I'm going to go ahead and get off.
[202:04.00] I'm going to go ahead and get off.
[202:09.00] I'm going to go ahead and get off.
[202:11.00] I'm going to go ahead and get off.
[202:12.00] I'm going to go ahead and get off.
[202:13.00] I'm going to go ahead and get off.
[202:14.00] I'm going to go ahead and get off.
[202:15.00] I'm going to go ahead and get off.
[202:16.00] I'm going to go ahead and get off.
[202:17.00] I'm going to go ahead and get off.
[202:18.00] I'm going to go ahead and get off.
[202:19.00] I'm going to go ahead and get off.
[202:20.00] I'm going to go ahead and get off.
[202:21.00] I'm going to go ahead and get off.
[202:22.00] I'm going to go ahead and get off.
[202:23.00] I'm going to go ahead and get off.
[202:24.00] I'm going to go ahead and get off.
[202:25.00] I'm going to go ahead and get off.
[202:26.00] I'm going to go ahead and get off.
[202:27.00] I'm going to go ahead and get off.
[202:28.00] I'm going to go ahead and get off.
[202:29.00] I'm going to go ahead and get off.
[202:30.00] I'm going to go ahead and get off.
[202:31.00] I'm going to go ahead and get off.
[202:32.00] I'm going to go ahead and get off.
[202:33.00] I'm going to go ahead and get off.
[202:34.00] I'm going to go ahead and get off.
[202:35.00] I'm going to go ahead and get off.
[202:36.00] I'm going to go ahead and get off.
[202:37.00] I'm going to go ahead and get off.
[202:38.00] I'm going to go ahead and get off.
[202:39.00] I'm going to go ahead and get off.
[202:40.00] I'm going to go ahead and get off.
[202:41.00] I'm going to go ahead and get off.
[202:42.00] I'm going to go ahead and get off.
[202:43.00] I'm going to go ahead and get off.
[202:44.00] Finally, I need people that are good at CSS.
[203:00.88] I need people that are good at programming too.
[203:06.04] Oh, whoops.
[203:11.68] Is this?
[203:12.68] No.
[203:13.68] This is not updated.
[203:14.68] There we go.
[203:15.68] Holy moly, that's long.
[203:20.84] All sorts of stuff in there.
[203:25.56] Okay, so the next time I work on this, it's going to be CLI Tools.
[203:31.92] Boom!
[203:32.92] This is all published.
[203:36.84] Alright.
[203:46.10] Is vanilla CSS really used over CSS frameworks in the wild?
[203:50.16] Unfortunately, no.
[203:52.32] No.
[203:53.32] Because people don't know about--was it--there's two things you need to know about CSS for
[204:00.36] your world to be a better place.
[204:02.28] One of them is box sizing, okay, and the other one is CSS variables.
[204:26.56] I still don't think anybody knows what flexbox is and flex and flummox and flimflam.
[204:48.40] What's up, slippy goat?
[204:51.56] But this is what I do know.
[204:53.16] If you know--if you can use CSS box sizing, it fixes most of the problems that you have
[205:00.40] with calculating sizes in CSS.
[205:03.20] In particular, they show you on the page, and the other thing is to use variables.
[205:09.60] If you use variables, you don't need sass.
[205:12.56] The only thing that sass does other than variables is nesting, and so if you just--if you can
[205:21.08] just bear to actually use cascading stylesheets in a cascading manner until we get the nesting
[205:28.28] stuff, or there is a one-off module that just does the nesting, but there's no need for
[205:33.72] sass anymore.
[205:34.72] There's no need for sass other than the--you can use something else to do nesting if you
[205:41.48] must, but you can also just use a prefix, you know, it's not the end of the world to
[205:47.20] hit the tab key to complete the name of something.
[205:51.52] It's not the end of the world.
[206:06.60] I thought tailwind and things were more common on projects.
[206:10.36] I would say that tailwind is not as bad as sass.
[206:17.00] Wait.
[206:21.52] Flexbox is what made you stop second-guessing?
[206:24.56] I don't know.
[206:25.56] I don't do CSS, okay?
[206:28.36] I just know that box-sizing border box solves problems.
[206:35.24] That's what I know.
[206:37.56] I know that if you use box-sizing border box, you can actually calculate a thing, and that's
[206:47.72] pretty nice.
[206:54.96] And then the variables, yeah.
[207:01.80] The problem with the web today is that just about everything that we need is native.
[207:05.92] It's available in the browser, it's available in the standards we have, but all the frameworks
[207:10.08] are basically a hundred years old, and none of them are built to use any of the stuff
[207:15.56] that actually works.
[207:17.48] They're all built to solve problems that we don't have, with a few exceptions, but...
[207:25.52] Frontend is crazy.
[207:26.52] I try to stay away from it.
[207:29.56] I do--I write libraries, so my libraries will work on the frontend, but I'm not concerning
[207:35.76] myself with what color something's going to be, because I'm working on the hierarchical
[207:43.52] deterministic wallets.
[207:44.92] That was the thing today.
[207:47.20] Anyway, I've got to go.
[207:48.76] I'm so glad to see y'all, and to be able to rant and rave a little bit, but I--it is 3:30
[207:57.76] AM here.
[207:58.76] I've got to get to bed.
[208:00.84] So I'm going to go do that, and then I need to get some CLI work done on these things
[208:13.04] as well, but that's not as big of a deal.
[208:18.92] CLI is going to be a bit simpler, but it's so nice to--all four of these tools are now
[208:27.20] published--not a good version.
[208:31.64] Okay.
[208:32.76] Also some other couple links here, if you're interested.
[208:37.28] Like sub follow if you want to, you already followed, that's great.
[208:39.92] There's a Discord you can join if you want to.
[208:43.00] It's fairly quiet because I'm not a very sociable person, and I don't know how to get people
[208:47.68] to engage, and I don't necessarily know that I want to.
[208:58.68] And then, let's see.
[209:00.32] We also have Creeds of Craftsmanship--is that going to pop up with this one?
[209:07.32] No.
[209:08.84] Anyway.
[209:10.36] If you're interested in software engineering, creedsofcraftsmanship.com--that's a curated
[209:18.20] list that I keep--of great engineering talks that I come across.
[209:31.32] And with that all said, time for me to go to bed, y'all.
[209:36.14] Have a wonderful noon, night, day, morning, whatever it is, wherever you are.
[209:41.76] I'll catch you later.
[209:43.76] Adios.