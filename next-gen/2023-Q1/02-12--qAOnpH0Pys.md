---
showLink: "https://www.youtube.com/watch?v=-qAOnpH0Pys"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Code Hangout: Next-Gen DASH Tools #15: Implementing BIP-44 in Dash HD Keys"
publishDate: "2023-02-12"
coverImage: "https://i.ytimg.com/vi/-qAOnpH0Pys/maxresdefault.jpg"
---

## Episode Description

A coding stream focused on implementing BIP-44 in Dash HD Keys, refactoring code and discussing project structure.

## Episode Summary

In this 4-hour coding stream, the developer works on implementing BIP-44 functionality in a Dash HD Keys library. The session involves refactoring existing code, simplifying function structures, and discussing future implementation steps. The developer encounters and resolves issues related to async/await usage and subtle differences in cryptographic operations. Throughout the stream, there are tangential discussions about project management, open-source contributions, and other development tools. The developer also interacts with viewers, discussing various topics including anime subtitling software and personal projects.

## Chapters

00:00 - Stream Setup and Initial Discussions

The stream begins with the host setting up audio equipment and discussing recent personal activities. He mentions working on multiple projects, including Aliasman and a personal programming language. The host also talks about his sleep patterns and how they affect his health and productivity.

05:42 - Reviewing and Refactoring Code

The developer starts reviewing the existing codebase for the Dash HD Keys library. He begins refactoring the code, focusing on simplifying the structure of key derivation functions. This involves moving some logic to higher-level functions and adjusting the API to be more object-oriented.

32:34 - Debugging and Testing

After making initial changes, the developer runs tests and encounters failures. He spends time debugging, eventually discovering that an awaited promise was causing issues. The developer also discusses subtle differences in cryptographic operations that could potentially cause problems.

71:22 - Further Refactoring and API Design

The host continues to refine the code structure, discussing potential naming conventions and API design choices. He considers how to best implement functions for deriving root keys, accounts, and individual keys while maintaining a clean and intuitive interface.

120:30 - Viewer Interactions and Side Discussions

Throughout the stream, the developer engages with viewers, discussing various topics. This includes conversations about open-source project management, contributor dynamics, and personal development tools like Webby. The host also reviews a viewer's subtitle synchronization software project.

180:36 - Wrapping Up and Future Plans

As the stream comes to a close, the developer summarizes the progress made and outlines plans for future work on the project. He expresses satisfaction with the refactoring done and discusses the next steps, which include implementing derive account and derive key functions.

227:11 - Closing Remarks

The host concludes the stream, thanking viewers for tuning in and encouraging them to follow his various Twitch channels for different types of content. He mentions being tired but generally more animated in other streams, and says goodbye to the audience.

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
[01:44] testing one two all right testing one two
[01:52] testing one two testing one two all right now when i get excited this is going to go a little bit over
[02:17] i got the new usb setup compressor and limiter are in order compressor is starting at negative
[02:24] six db limiter is at negative three db okay so i should not be able oh i can go over uh because
[02:32] i'm up by three db huh okay so i need to switch where the compressor needs to start at nine db
[02:43] and the limiter needs to end at negative six db okay and just by turning that gain down
[02:52] we should get a lot better quality on the audio and if i am kind of speaking a little softly
[03:02] we should still be doing all right okay let's go ahead and get a couple things moved over here
[03:11] desk is getting cluttered again it's time for a cleanup
[03:14] i'm just testing out the audio i think it should be a little bit higher
[03:18] let's see well our gain is pretty low
[03:23] and that's good
[03:40] i think negative four four negative 24 might be better okay let's testing
[03:46] we've got a three bb three db boost and well when i'm just speaking normally it looks like i'm
[03:56] getting a little bit lower than i want so i think i might change the mic settings just a just a touch
[04:07] bringing that up just a little higher just so we're just so even when i'm speaking low
[04:13] we're getting a little bit closer to negative 10 and not close to negative 18
[04:18] all right we'll give that a try
[04:36] so
[04:49] well hello hello everybody and welcome back i'm ajo neil this is the dash incubator channel where
[04:55] we work on all dash all the time all dash all the time all the time sunday sunday sunday
[05:01] that's usually not sundays uh let's let's start off with a quick can of our good friend
[05:08] mr mountain dew popped up my friends and let us open focus
[05:12] ah yes i'm gonna sip this one a little slower than the last one
[05:18] okay let me gather my thoughts here
[05:31] so a couple pieces of good news i think i think fingers crossed hope very much that the mic issue
[05:41] is behind us i have now plugged the mic into a different usb hub i actually got a hub
[05:51] that i'm replacing what the monitors connect to which i can't show you what they were connected
[05:58] to because i still have that plugged in in case i end up needing to swap it back
[06:01] but i replaced what they did connect into which was this very nice wavelength adapter thunderbolt
[06:09] 3 adapter i replaced that with basically just an upgraded version it seems to have all the
[06:14] same good stuff inside but then it also has a usb and ethernet and so i've plugged the mic into that
[06:19] momentarily soon within a few days i should also get a new thunderbolt hub that is from dell
[06:27] thankfully i was able to get it much less i think it's about half the price of what the new cost is
[06:35] getting it gently used and this will also have more stuff integrated in so that i need fewer dongles
[06:45] and watch my jiggers hopefully so i think that the problem that was affecting the mic
[06:53] is the same reason that if you're watching some of the other streams when i did the alternate
[06:56] angles with the cameras and sometimes the cameras would freak out i think that was the same problem
[07:05] i think it's this usb hub so that should be fixed up in other news so what we're working on
[07:12] i am glad that i had a few days i had a few more days than i intended away from this project but
[07:21] it was good to have at least a few days away from it because i was able to kind of sift through
[07:26] without being at the code just kind of let it sit in the back of my mind and i realized
[07:29] what's kind of bugging me about dash hd why you know there's just kind of something doesn't quite
[07:35] feel right and the reason is that dash hd in its present form as a fork of hd key was built to
[07:43] implement the dash 39 uh bip 39 spec not the bip 44 spec and there's one thing about that spec
[07:51] that i need to take a look at and make sure that we handle correctly and there's also there was a
[07:58] bug that was mentioned in the sec p 256 k1 library that may actually still be relevant in a very very
[08:05] rare edge case i need to take a look at again so those are some things that i need to put up here
[08:12] so one uh bit 44 differences we need to take a peek at that and sec p 256 k1 edge case we do
[08:23] need to figure out what that was but it essentially was i if it was when the key is zero i'm not
[08:30] worried about that but there's also an overflow case and i am worried about the overflow case
[08:38] because i don't know how often it happens in practice if it's one in a million times
[08:42] or one in 10 million times or what it is but there is this case where there is actually overflow
[08:50] and i need to make sure that we account for that because that would be very bad if it is
[09:00] something that happens at all really whether it's frequently or infrequently but if it's
[09:06] the zero key we don't have to worry about that because the zero key literally never happens
[09:10] that's it happens in a test suite but it doesn't ever happen outside of a test suite you you would
[09:15] never have a key that is literally zero that's just it's not only is it unfathomably unlikely
[09:24] it's just not possible i i don't think outside of a test case scenario you can't generate a
[09:30] random number you can't generate 32 random bites and have all of them be zero that's just
[09:37] that doesn't happen
[09:38] and i had written some stuff down on a sheet of paper
[09:48] a while ago because i was sitting having breakfast last week
[09:53] about i think it was last saturday the last time i'd worked on this it was the next day or
[09:59] something like that it could have even been a sunday afternoon but i i sat down and i started
[10:04] writing down on a sheet of paper what the api needs to look like and i realized that we need
[10:11] to have
[10:13] a derive
[10:16] essentially a derive account
[10:20] and a derive
[10:27] key or address either of those i guess we need to drive key and that should include the address
[10:36] so we'll get to work on that in just a minute i still need to take a few more
[10:41] sips of my mountain dew here get my get my head on straight you know uh let's see what else
[10:48] do i have i don't have the terminal over here yet do i no let's go ahead and get our terminal up here
[10:56] okay
[10:56] so here we go
[11:01] actually i don't want i don't want the lid on here makes it too hard to drink this
[11:10] just let me get that off i'm just gonna sorry we're gonna ease into this a little bit today
[11:15] because i'm still my brain is still kind of mulling over some of these ideas
[11:21] so there's no rush
[11:29] i think it's going to be pretty simple to get back into this i'm going to be so excited if
[11:38] we don't have any mic issues during this stream i'm going to be so excited that's going to be
[11:42] wonderful but i think all signs are pointing to it is the usb hub that's been the problem
[11:50] i think we do need to leave it called master secret what was i doing here
[11:57] this key size stuff this makes sense why did i not commit this
[12:00] i was probably thinking i'd get to it in the morning
[12:08] all right it's coming back to me i'm remembering it all it's coming back to me oh
[12:26] okay we have to check an email sooner or later
[12:30] all right so that changed i think i yeah i understand these changes i'm going to revert
[12:38] back to the usb hub and then i'm going to go back to the usb hub and i'm going to go back to the
[12:44] usb hub and then i'm going to go back to the usb hub and then i'm going to go back to the usb hub
[12:49] and then i'm going to go back to the usb hub and then i'm going to go back to the usb hub
[12:54] and then i'm going to go back to the usb hub and then i'm going to go back to the usb hub
[12:56] and then i'm going to go back to the usb hub and then i'm going to go back to the usb hub
[12:58] and then i'm going to go back to the usb hub and then i'm going to go back to the usb hub
[13:00] and then i'm going to go back to the usb hub
[13:02] and then i'm going to go back to the usb hub
[13:04] and then i'm going to go back to the usb hub
[13:06] and then i'm going to go back to the usb hub
[13:08] and then i'm going to go back to the usb hub
[13:10] and then i'm going to go back to the usb hub
[13:12] and then i'm going to go back to the usb hub
[13:14] and then i'm going to go back to the usb hub
[13:16] and then i'm going to go back to the usb hub
[13:18] and then i'm going to go back to the usb hub
[13:20] and then i'm going to go back to the usb hub
[13:22] and then i'm going to go back to the usb hub
[13:24] and then i'm going to go back to the usb hub
[13:26] and then i'm going to go back to the usb hub
[13:28] and then i'm going to go back to the usb hub
[13:30] and then i'm going to go back to the usb hub
[13:32] and then i'm going to go back to the usb hub
[13:34] and then i'm going to go back to the usb hub
[13:36] and then i'm going to go back to the usb hub
[13:38] and then i'm going to go back to the usb hub
[13:40] and then i'm going to go back to the usb hub
[13:42] and then i'm going to go back to the usb hub
[13:44] and then i'm going to go back to the usb hub
[13:46] and then i'm going to go back to the usb hub
[13:48] and then i'm going to go back to the usb hub
[13:50] and then i'm going to go back to the usb hub
[13:52] and then i'm going to go back to the usb hub
[13:54] and then i'm going to go back to the usb hub
[13:56] and then i'm going to go back to the usb hub
[13:58] and then i'm going to go back to the usb hub
[14:00] and then i'm going to go back to the usb hub
[14:02] and then i'm going to go back to the usb hub
[14:04] and then i'm going to go back to the usb hub
[14:06] and then i'm going to go back to the usb hub
[14:08] and then i'm going to go back to the usb hub
[14:10] and then i'm going to go back to the usb hub
[14:12] and then i'm going to go back to the usb hub
[14:14] and then i'm going to go back to the usb hub
[14:16] and then i'm going to go back to the usb hub
[14:18] and then i'm going to go back to the usb hub
[14:20] and then i'm going to go back to the usb hub
[14:22] and then i'm going to go back to the usb hub
[14:24] and then i'm going to go back to the usb hub
[14:26] and then i'm going to go back to the usb hub
[14:28] and then i'm going to go back to the usb hub
[14:30] and then i'm going to go back to the usb hub
[14:32] and then i'm going to go back to the usb hub
[14:34] and then i'm going to go back to the usb hub
[14:36] and then i'm going to go back to the usb hub
[14:38] and then i'm going to go back to the usb hub
[14:40] and then i'm going to go back to the usb hub
[14:42] and then i'm going to go back to the usb hub
[14:44] and then i'm going to go back to the usb hub
[14:46] and then i'm going to go back to the usb hub
[14:48] and then i'm going to go back to the usb hub
[14:50] and then i'm going to go back to the usb hub
[14:52] and then i'm going to go back to the usb hub
[14:54] and then i'm going to go back to the usb hub
[14:56] and then i'm going to go back to the usb hub
[14:58] and then i'm going to go back to the usb hub
[15:00] and then i'm going to go back to the usb hub
[15:02] and then i'm going to go back to the usb hub
[15:04] and then i'm going to go back to the usb hub
[15:06] and then i'm going to go back to the usb hub
[15:08] and then i'm going to go back to the usb hub
[15:10] and then i'm going to go back to the usb hub
[15:12] and then i'm going to go back to the usb hub
[15:14] and then i'm going to go back to the usb hub
[15:16] and then i'm going to go back to the usb hub
[15:18] and then i'm going to go back to the usb hub
[15:20] and then i'm going to go back to the usb hub
[15:22] and then i'm going to go back to the usb hub
[15:24] and then i'm going to go back to the usb hub
[15:26] and then i'm going to go back to the usb hub
[15:28] and then i'm going to go back to the usb hub
[15:30] and then i'm going to go back to the usb hub
[15:32] and then i'm going to go back to the usb hub
[15:34] and then i'm going to go back to the usb hub
[15:36] and then i'm going to go back to the usb hub
[15:38] and then i'm going to go back to the usb hub
[15:40] and then i'm going to go back to the usb hub
[15:42] and then i'm going to go back to the usb hub
[15:44] and then i'm going to go back to the usb hub
[15:46] and then i'm going to go back to the usb hub
[15:48] and then i'm going to go back to the usb hub
[15:50] and then i'm going to go back to the usb hub
[15:52] and then i'm going to go back to the usb hub
[15:54] and then i'm going to go back to the usb hub
[15:56] and then i'm going to go back to the usb hub
[15:58] and then i'm going to go back to the usb hub
[16:00] and then i'm going to go back to the usb hub
[16:02] and then i'm going to go back to the usb hub
[16:04] and then i'm going to go back to the usb hub
[16:06] and then i'm going to go back to the usb hub
[16:08] and then i'm going to go back to the usb hub
[16:10] and then i'm going to go back to the usb hub
[16:12] and then i'm going to go back to the usb hub
[16:14] and then i'm going to go back to the usb hub
[16:16] and then i'm going to go back to the usb hub
[16:18] and then i'm going to go back to the usb hub
[16:20] and then i'm going to go back to the usb hub
[16:22] and then i'm going to go back to the usb hub
[16:24] and then i'm going to go back to the usb hub
[16:26] and then i'm going to go back to the usb hub
[16:28] and then i'm going to go back to the usb hub
[16:30] and then i'm going to go back to the usb hub
[16:32] and then i'm going to go back to the usb hub
[16:34] and then i'm going to go back to the usb hub
[16:36] and then i'm going to go back to the usb hub
[16:38] and then i'm going to go back to the usb hub
[16:40] and then i'm going to go back to the usb hub
[16:42] and then i'm going to go back to the usb hub
[16:44] and then i'm going to go back to the usb hub
[16:46] and then i'm going to go back to the usb hub
[16:48] and then i'm going to go back to the usb hub
[16:50] and then i'm going to go back to the usb hub
[16:52] and then i'm going to go back to the usb hub
[16:54] and then i'm going to go back to the usb hub
[16:56] and then i'm going to go back to the usb hub
[16:58] and then i'm going to go back to the usb hub
[17:00] and then i'm going to go back to the usb hub
[17:02] and then i'm going to go back to the usb hub
[17:04] and then i'm going to go back to the usb hub
[17:06] and then i'm going to go back to the usb hub
[17:08] and then i'm going to go back to the usb hub
[17:10] and then i'm going to go back to the usb hub
[17:12] and then i'm going to go back to the usb hub
[17:14] and then i'm going to go back to the usb hub
[17:16] and then i'm going to go back to the usb hub
[17:18] and then i'm going to go back to the usb hub
[17:20] and then i'm going to go back to the usb hub
[17:22] and then i'm going to go back to the usb hub
[17:24] and then i'm going to go back to the usb hub
[17:26] and then i'm going to go back to the usb hub
[17:28] and then i'm going to go back to the usb hub
[17:30] and then i'm going to go back to the usb hub
[17:32] and then i'm going to go back to the usb hub
[17:34] and then i'm going to go back to the usb hub
[17:36] and then i'm going to go back to the usb hub
[17:38] and then i'm going to go back to the usb hub
[17:40] and then i'm going to go back to the usb hub
[17:42] and then i'm going to go back to the usb hub
[17:44] and then i'm going to go back to the usb hub
[17:46] and then i'm going to go back to the usb hub
[17:48] and then i'm going to go back to the usb hub
[17:50] and then i'm going to go back to the usb hub
[17:52] and then i'm going to go back to the usb hub
[17:54] and then i'm going to go back to the usb hub
[17:56] and then i'm going to go back to the usb hub
[17:58] and then i'm going to go back to the usb hub
[18:00] and then i'm going to go back to the usb hub
[18:02] and then i'm going to go back to the usb hub
[18:04] and then i'm going to go back to the usb hub
[18:06] and then i'm going to go back to the usb hub
[18:08] and then i'm going to go back to the usb hub
[18:10] and then i'm going to go back to the usb hub
[18:12] and then i'm going to go back to the usb hub
[18:14] and then i'm going to go back to the usb hub
[18:16] and then i'm going to go back to the usb hub
[18:18] and then i'm going to go back to the usb hub
[18:20] and then i'm going to go back to the usb hub
[18:22] and then i'm going to go back to the usb hub
[18:24] and then i'm going to go back to the usb hub
[18:26] and then i'm going to go back to the usb hub
[18:28] and then i'm going to go back to the usb hub
[18:30] and then i'm going to go back to the usb hub
[18:32] and then i'm going to go back to the usb hub
[18:34] and then i'm going to go back to the usb hub
[18:36] and then i'm going to go back to the usb hub
[18:38] and then i'm going to go back to the usb hub
[18:40] and then i'm going to go back to the usb hub
[18:42] and then i'm going to go back to the usb hub
[18:44] and then i'm going to go back to the usb hub
[18:46] and then i'm going to go back to the usb hub
[18:48] and then i'm going to go back to the usb hub
[18:50] and then i'm going to go back to the usb hub
[18:52] and then i'm going to go back to the usb hub
[18:54] and then i'm going to go back to the usb hub
[18:56] and then i'm going to go back to the usb hub
[18:58] and then i'm going to go back to the usb hub
[19:00] and then i'm going to go back to the usb hub
[19:02] and then i'm going to go back to the usb hub
[19:04] and then i'm going to go back to the usb hub
[19:06] and then i'm going to go back to the usb hub
[19:08] and then i'm going to go back to the usb hub
[19:10] and then i'm going to go back to the usb hub
[19:12] and then i'm going to go back to the usb hub
[19:14] and then i'm going to go back to the usb hub
[19:16] and then i'm going to go back to the usb hub
[19:18] and then i'm going to go back to the usb hub
[19:20] and then i'm going to go back to the usb hub
[19:22] and then i'm going to go back to the usb hub
[19:24] and then i'm going to go back to the usb hub
[19:26] and then i'm going to go back to the usb hub
[19:28] and then i'm going to go back to the usb hub
[19:30] and then i'm going to go back to the usb hub
[19:32] and then i'm going to go back to the usb hub
[19:34] and then i'm going to go back to the usb hub
[19:36] and then i'm going to go back to the usb hub
[19:38] and then i'm going to go back to the usb hub
[19:40] and then i'm going to go back to the usb hub
[19:42] and then i'm going to go back to the usb hub
[19:44] and then i'm going to go back to the usb hub
[19:46] and then i'm going to go back to the usb hub
[19:48] and then i'm going to go back to the usb hub
[19:50] and then i'm going to go back to the usb hub
[19:52] and then i'm going to go back to the usb hub
[19:54] and then i'm going to go back to the usb hub
[19:56] and then i'm going to go back to the usb hub
[19:58] and then i'm going to go back to the usb hub
[20:00] and then i'm going to go back to the usb hub
[20:02] and then i'm going to go back to the usb hub
[20:04] and then i'm going to go back to the usb hub
[20:06] and then i'm going to go back to the usb hub
[20:08] and then i'm going to go back to the usb hub
[20:10] and then i'm going to go back to the usb hub
[20:12] and then i'm going to go back to the usb hub
[20:14] and then i'm going to go back to the usb hub
[20:16] and then i'm going to go back to the usb hub
[20:18] and then i'm going to go back to the usb hub
[20:20] and then i'm going to go back to the usb hub
[20:22] and then i'm going to go back to the usb hub
[20:24] and then i'm going to go back to the usb hub
[20:26] and then i'm going to go back to the usb hub
[20:28] and then i'm going to go back to the usb hub
[20:30] and then i'm going to go back to the usb hub
[20:32] and then i'm going to go back to the usb hub
[20:34] and then i'm going to go back to the usb hub
[20:36] and then i'm going to go back to the usb hub
[20:38] and then i'm going to go back to the usb hub
[20:40] and then i'm going to go back to the usb hub
[20:42] and then i'm going to go back to the usb hub
[20:44] and then i'm going to go back to the usb hub
[20:46] and then i'm going to go back to the usb hub
[20:48] and then i'm going to go back to the usb hub
[20:50] and then i'm going to go back to the usb hub
[20:52] and then i'm going to go back to the usb hub
[20:54] and then i'm going to go back to the usb hub
[20:56] and then i'm going to go back to the usb hub
[20:58] and then i'm going to go back to the usb hub
[21:00] and then i'm going to go back to the usb hub
[21:02] and then i'm going to go back to the usb hub
[21:04] and then i'm going to go back to the usb hub
[21:06] and then i'm going to go back to the usb hub
[21:08] and then i'm going to go back to the usb hub
[21:10] and then i'm going to go back to the usb hub
[21:12] and then i'm going to go back to the usb hub
[21:14] and then i'm going to go back to the usb hub
[21:16] and then i'm going to go back to the usb hub
[21:18] and then i'm going to go back to the usb hub
[21:20] and then i'm going to go back to the usb hub
[21:22] and then i'm going to go back to the usb hub
[21:24] and then i'm going to go back to the usb hub
[21:26] and then i'm going to go back to the usb hub
[21:28] and then i'm going to go back to the usb hub
[21:30] and then i'm going to go back to the usb hub
[21:32] and then i'm going to go back to the usb hub
[21:34] and then i'm going to go back to the usb hub
[21:36] and then i'm going to go back to the usb hub
[21:38] and then i'm going to go back to the usb hub
[21:40] and then i'm going to go back to the usb hub
[21:42] and then i'm going to go back to the usb hub
[21:44] and then i'm going to go back to the usb hub
[21:46] and then i'm going to go back to the usb hub
[21:48] and then i'm going to go back to the usb hub
[21:50] and then i'm going to go back to the usb hub
[21:52] and then i'm going to go back to the usb hub
[21:54] and then i'm going to go back to the usb hub
[21:56] and then i'm going to go back to the usb hub
[21:58] and then i'm going to go back to the usb hub
[22:00] and then i'm going to go back to the usb hub
[22:02] and then i'm going to go back to the usb hub
[22:04] and then i'm going to go back to the usb hub
[22:06] and then i'm going to go back to the usb hub
[22:08] and then i'm going to go back to the usb hub
[22:10] and then i'm going to go back to the usb hub
[22:12] and then i'm going to go back to the usb hub
[22:14] and then i'm going to go back to the usb hub
[22:16] and then i'm going to go back to the usb hub
[22:18] and then i'm going to go back to the usb hub
[22:20] and then i'm going to go back to the usb hub
[22:22] and then i'm going to go back to the usb hub
[22:24] and then i'm going to go back to the usb hub
[22:26] and then i'm going to go back to the usb hub
[22:28] and then i'm going to go back to the usb hub
[22:30] and then i'm going to go back to the usb hub
[22:32] and then i'm going to go back to the usb hub
[22:34] and then i'm going to go back to the usb hub
[22:36] and then i'm going to go back to the usb hub
[22:38] and then i'm going to go back to the usb hub
[22:40] and then i'm going to go back to the usb hub
[22:42] and then i'm going to go back to the usb hub
[22:44] and then i'm going to go back to the usb hub
[22:46] and then i'm going to go back to the usb hub
[22:48] and then i'm going to go back to the usb hub
[22:50] and then i'm going to go back to the usb hub
[22:52] and then i'm going to go back to the usb hub
[22:54] and then i'm going to go back to the usb hub
[22:56] and then i'm going to go back to the usb hub
[22:58] and then i'm going to go back to the usb hub
[23:00] and then i'm going to go back to the usb hub
[23:02] and then i'm going to go back to the usb hub
[23:04] and then i'm going to go back to the usb hub
[23:06] and then i'm going to go back to the usb hub
[23:08] and then i'm going to go back to the usb hub
[23:10] and then i'm going to go back to the usb hub
[23:12] and then i'm going to go back to the usb hub
[23:14] and then i'm going to go back to the usb hub
[23:16] and then i'm going to go back to the usb hub
[23:18] and then i'm going to go back to the usb hub
[23:20] and then i'm going to go back to the usb hub
[23:22] and then i'm going to go back to the usb hub
[23:24] and then i'm going to go back to the usb hub
[23:26] and then i'm going to go back to the usb hub
[23:28] and then i'm going to go back to the usb hub
[23:30] and then i'm going to go back to the usb hub
[23:32] and then i'm going to go back to the usb hub
[23:34] and then i'm going to go back to the usb hub
[23:36] and then i'm going to go back to the usb hub
[23:38] and then i'm going to go back to the usb hub
[23:40] and then i'm going to go back to the usb hub
[23:42] and then i'm going to go back to the usb hub
[23:44] and then i'm going to go back to the usb hub
[23:46] and then i'm going to go back to the usb hub
[23:48] and then i'm going to go back to the usb hub
[23:50] and then i'm going to go back to the usb hub
[23:52] and then i'm going to go back to the usb hub
[23:54] and then i'm going to go back to the usb hub
[23:56] and then i'm going to go back to the usb hub
[23:58] and then i'm going to go back to the usb hub
[24:00] and then i'm going to go back to the usb hub
[24:02] and then i'm going to go back to the usb hub
[24:04] and then i'm going to go back to the usb hub
[24:06] and then i'm going to go back to the usb hub
[24:08] and then i'm going to go back to the usb hub
[24:10] and then i'm going to go back to the usb hub
[24:12] and then i'm going to go back to the usb hub
[24:14] and then i'm going to go back to the usb hub
[24:16] and then i'm going to go back to the usb hub
[24:18] and then i'm going to go back to the usb hub
[24:20] and then i'm going to go back to the usb hub
[24:22] and then i'm going to go back to the usb hub
[24:24] and then i'm going to go back to the usb hub
[24:26] and then i'm going to go back to the usb hub
[24:28] and then i'm going to go back to the usb hub
[24:30] and then i'm going to go back to the usb hub
[24:32] and then i'm going to go back to the usb hub
[24:34] and then i'm going to go back to the usb hub
[24:36] and then i'm going to go back to the usb hub
[24:38] and then i'm going to go back to the usb hub
[24:40] and then i'm going to go back to the usb hub
[24:42] and then i'm going to go back to the usb hub
[24:44] and then i'm going to go back to the usb hub
[24:46] and then i'm going to go back to the usb hub
[24:48] and then i'm going to go back to the usb hub
[24:50] and then i'm going to go back to the usb hub
[24:52] and then i'm going to go back to the usb hub
[24:54] and then i'm going to go back to the usb hub
[24:56] and then i'm going to go back to the usb hub
[24:58] and then i'm going to go back to the usb hub
[25:00] and then i'm going to go back to the usb hub
[25:02] and then i'm going to go back to the usb hub
[25:04] and then i'm going to go back to the usb hub
[25:06] and then i'm going to go back to the usb hub
[25:08] and then i'm going to go back to the usb hub
[25:10] and then i'm going to go back to the usb hub
[25:12] and then i'm going to go back to the usb hub
[25:14] and then i'm going to go back to the usb hub
[25:16] and then i'm going to go back to the usb hub
[25:18] and then i'm going to go back to the usb hub
[25:20] and then i'm going to go back to the usb hub
[25:22] and then i'm going to go back to the usb hub
[25:24] and then i'm going to go back to the usb hub
[25:26] and then i'm going to go back to the usb hub
[25:28] and then i'm going to go back to the usb hub
[25:30] and then i'm going to go back to the usb hub
[25:32] and then i'm going to go back to the usb hub
[25:34] and then i'm going to go back to the usb hub
[25:36] and then i'm going to go back to the usb hub
[25:38] and then i'm going to go back to the usb hub
[25:40] and then i'm going to go back to the usb hub
[25:42] and then i'm going to go back to the usb hub
[25:44] and then i'm going to go back to the usb hub
[25:46] and then i'm going to go back to the usb hub
[25:48] and then i'm going to go back to the usb hub
[25:50] and then i'm going to go back to the usb hub
[25:52] and then i'm going to go back to the usb hub
[25:54] and then i'm going to go back to the usb hub
[25:56] and then i'm going to go back to the usb hub
[25:58] and then i'm going to go back to the usb hub
[26:00] and then i'm going to go back to the usb hub
[26:02] and then i'm going to go back to the usb hub
[26:04] and then i'm going to go back to the usb hub
[26:06] and then i'm going to go back to the usb hub
[26:08] and then i'm going to go back to the usb hub
[26:10] and then i'm going to go back to the usb hub
[26:12] and then i'm going to go back to the usb hub
[26:14] and then i'm going to go back to the usb hub
[26:16] and then i'm going to go back to the usb hub
[26:18] and then i'm going to go back to the usb hub
[26:20] and then i'm going to go back to the usb hub
[26:22] and then i'm going to go back to the usb hub
[26:24] and then i'm going to go back to the usb hub
[26:26] and then i'm going to go back to the usb hub
[26:28] and then i'm going to go back to the usb hub
[26:30] and then i'm going to go back to the usb hub
[26:32] and then i'm going to go back to the usb hub
[26:34] and then i'm going to go back to the usb hub
[26:36] and then i'm going to go back to the usb hub
[26:38] and then i'm going to go back to the usb hub
[26:40] and then i'm going to go back to the usb hub
[26:42] and then i'm going to go back to the usb hub
[26:44] and then i'm going to go back to the usb hub
[26:46] and then i'm going to go back to the usb hub
[26:48] and then i'm going to go back to the usb hub
[26:50] and then i'm going to go back to the usb hub
[26:52] and then i'm going to go back to the usb hub
[26:54] and then i'm going to go back to the usb hub
[26:56] and then i'm going to go back to the usb hub
[26:58] and then i'm going to go back to the usb hub
[27:00] and then i'm going to go back to the usb hub
[27:02] and then i'm going to go back to the usb hub
[27:04] and then i'm going to go back to the usb hub
[27:06] and then i'm going to go back to the usb hub
[27:08] and then i'm going to go back to the usb hub
[27:10] and then i'm going to go back to the usb hub
[27:12] and then i'm going to go back to the usb hub
[27:14] and then i'm going to go back to the usb hub
[27:16] and then i'm going to go back to the usb hub
[27:18] and then i'm going to go back to the usb hub
[27:20] and then i'm going to go back to the usb hub
[27:22] and then i'm going to go back to the usb hub
[27:24] and then i'm going to go back to the usb hub
[27:26] and then i'm going to go back to the usb hub
[27:28] and then i'm going to go back to the usb hub
[27:30] and then i'm going to go back to the usb hub
[27:32] and then i'm going to go back to the usb hub
[27:34] and then i'm going to go back to the usb hub
[27:36] and then i'm going to go back to the usb hub
[27:38] and then i'm going to go back to the usb hub
[27:40] and then i'm going to go back to the usb hub
[27:42] and then i'm going to go back to the usb hub
[27:44] and then i'm going to go back to the usb hub
[27:46] and then i'm going to go back to the usb hub
[27:48] and then i'm going to go back to the usb hub
[27:50] and then i'm going to go back to the usb hub
[27:52] and then i'm going to go back to the usb hub
[27:54] and then i'm going to go back to the usb hub
[27:56] and then i'm going to go back to the usb hub
[27:58] and then i'm going to go back to the usb hub
[28:00] and then i'm going to go back to the usb hub
[28:02] and then i'm going to go back to the usb hub
[28:04] and then i'm going to go back to the usb hub
[28:06] and then i'm going to go back to the usb hub
[28:08] and then i'm going to go back to the usb hub
[28:10] and then i'm going to go back to the usb hub
[28:12] and then i'm going to go back to the usb hub
[28:14] and then i'm going to go back to the usb hub
[28:16] and then i'm going to go back to the usb hub
[28:18] and then i'm going to go back to the usb hub
[28:20] and then i'm going to go back to the usb hub
[28:22] and then i'm going to go back to the usb hub
[28:24] and then i'm going to go back to the usb hub
[28:26] and then i'm going to go back to the usb hub
[28:28] and then i'm going to go back to the usb hub
[28:30] and then i'm going to go back to the usb hub
[28:32] and then i'm going to go back to the usb hub
[28:34] and then i'm going to go back to the usb hub
[28:36] and then i'm going to go back to the usb hub
[28:38] and then i'm going to go back to the usb hub
[28:40] and then i'm going to go back to the usb hub
[28:42] and then i'm going to go back to the usb hub
[28:44] and then i'm going to go back to the usb hub
[28:46] and then i'm going to go back to the usb hub
[28:48] and then i'm going to go back to the usb hub
[28:50] and then i'm going to go back to the usb hub
[28:52] and then i'm going to go back to the usb hub
[28:54] and then i'm going to go back to the usb hub
[28:56] and then i'm going to go back to the usb hub
[28:58] and then i'm going to go back to the usb hub
[29:00] and then i'm going to go back to the usb hub
[29:02] and then i'm going to go back to the usb hub
[29:04] and then i'm going to go back to the usb hub
[29:06] and then i'm going to go back to the usb hub
[29:08] and then i'm going to go back to the usb hub
[29:10] and then i'm going to go back to the usb hub
[29:12] and then i'm going to go back to the usb hub
[29:14] and then i'm going to go back to the usb hub
[29:16] and then i'm going to go back to the usb hub
[29:18] and then i'm going to go back to the usb hub
[29:20] and then i'm going to go back to the usb hub
[29:22] and then i'm going to go back to the usb hub
[29:24] and then i'm going to go back to the usb hub
[29:26] and then i'm going to go back to the usb hub
[29:28] and then i'm going to go back to the usb hub
[29:30] and then i'm going to go back to the usb hub
[29:32] and then i'm going to go back to the usb hub
[29:34] and then i'm going to go back to the usb hub
[29:36] and then i'm going to go back to the usb hub
[29:38] and then i'm going to go back to the usb hub
[29:40] and then i'm going to go back to the usb hub
[29:42] and then i'm going to go back to the usb hub
[29:44] and then i'm going to go back to the usb hub
[29:46] and then i'm going to go back to the usb hub
[29:48] and then i'm going to go back to the usb hub
[29:50] and then i'm going to go back to the usb hub
[29:52] and then i'm going to go back to the usb hub
[29:54] and then i'm going to go back to the usb hub
[29:56] and then i'm going to go back to the usb hub
[29:58] and then i'm going to go back to the usb hub
[30:00] and then i'm going to go back to the usb hub
[30:02] and then i'm going to go back to the usb hub
[30:04] and then i'm going to go back to the usb hub
[30:06] and then i'm going to go back to the usb hub
[30:08] and then i'm going to go back to the usb hub
[30:10] and then i'm going to go back to the usb hub
[30:12] and then i'm going to go back to the usb hub
[30:14] and then i'm going to go back to the usb hub
[30:16] and then i'm going to go back to the usb hub
[30:18] and then i'm going to go back to the usb hub
[30:20] and then i'm going to go back to the usb hub
[30:22] and then i'm going to go back to the usb hub
[30:24] and then i'm going to go back to the usb hub
[30:26] and then i'm going to go back to the usb hub
[30:28] and then i'm going to go back to the usb hub
[30:30] and then i'm going to go back to the usb hub
[30:32] and then i'm going to go back to the usb hub
[30:34] and then i'm going to go back to the usb hub
[30:36] and then i'm going to go back to the usb hub
[30:38] and then i'm going to go back to the usb hub
[30:40] and then i'm going to go back to the usb hub
[30:42] and then i'm going to go back to the usb hub
[30:44] and then i'm going to go back to the usb hub
[30:46] and then i'm going to go back to the usb hub
[30:48] and then i'm going to go back to the usb hub
[30:50] and then i'm going to go back to the usb hub
[30:52] and then i'm going to go back to the usb hub
[30:54] and then i'm going to go back to the usb hub
[30:56] and then i'm going to go back to the usb hub
[30:58] and then i'm going to go back to the usb hub
[31:00] and then i'm going to go back to the usb hub
[31:02] and then i'm going to go back to the usb hub
[31:04] and then i'm going to go back to the usb hub
[31:06] and then i'm going to go back to the usb hub
[31:08] and then i'm going to go back to the usb hub
[31:10] and then i'm going to go back to the usb hub
[31:12] and then i'm going to go back to the usb hub
[31:14] and then i'm going to go back to the usb hub
[31:16] and then i'm going to go back to the usb hub
[31:18] and then i'm going to go back to the usb hub
[31:20] and then i'm going to go back to the usb hub
[31:22] and then i'm going to go back to the usb hub
[31:24] and then i'm going to go back to the usb hub
[31:26] and then i'm going to go back to the usb hub
[31:28] and then i'm going to go back to the usb hub
[31:30] and then i'm going to go back to the usb hub
[31:32] and then i'm going to go back to the usb hub
[31:34] and then i'm going to go back to the usb hub
[31:36] and then i'm going to go back to the usb hub
[31:38] and then i'm going to go back to the usb hub
[31:40] and then i'm going to go back to the usb hub
[31:42] and then i'm going to go back to the usb hub
[31:44] and then i'm going to go back to the usb hub
[31:46] and then i'm going to go back to the usb hub
[31:48] and then i'm going to go back to the usb hub
[31:50] and then i'm going to go back to the usb hub
[31:52] and then i'm going to go back to the usb hub
[31:54] and then i'm going to go back to the usb hub
[31:56] and then i'm going to go back to the usb hub
[31:58] and then i'm going to go back to the usb hub
[32:00] and then i'm going to go back to the usb hub
[32:02] and then i'm going to go back to the usb hub
[32:04] and then i'm going to go back to the usb hub
[32:06] and then i'm going to go back to the usb hub
[32:08] and then i'm going to go back to the usb hub
[32:10] and then i'm going to go back to the usb hub
[32:12] and then i'm going to go back to the usb hub
[32:14] and then i'm going to go back to the usb hub
[32:16] and then i'm going to go back to the usb hub
[32:18] and then i'm going to go back to the usb hub
[32:20] and then i'm going to go back to the usb hub
[32:22] and then i'm going to go back to the usb hub
[32:24] and then i'm going to go back to the usb hub
[32:26] and then i'm going to go back to the usb hub
[32:28] and then i'm going to go back to the usb hub
[32:30] and then i'm going to go back to the usb hub
[32:32] and then i'm going to go back to the usb hub
[32:34] and then i'm going to go back to the usb hub
[32:36] and then i'm going to go back to the usb hub
[32:38] and then i'm going to go back to the usb hub
[32:40] and then i'm going to go back to the usb hub
[32:42] and then i'm going to go back to the usb hub
[32:44] and then i'm going to go back to the usb hub
[32:46] and then i'm going to go back to the usb hub
[32:48] and then i'm going to go back to the usb hub
[32:50] and then i'm going to go back to the usb hub
[32:52] and then i'm going to go back to the usb hub
[32:54] and then i'm going to go back to the usb hub
[32:56] and then i'm going to go back to the usb hub
[32:58] and then i'm going to go back to the usb hub
[33:00] and then i'm going to go back to the usb hub
[33:02] and then i'm going to go back to the usb hub
[33:04] and then i'm going to go back to the usb hub
[33:06] and then i'm going to go back to the usb hub
[33:08] and then i'm going to go back to the usb hub
[33:10] and then i'm going to go back to the usb hub
[33:12] and then i'm going to go back to the usb hub
[33:14] and then i'm going to go back to the usb hub
[33:16] and then i'm going to go back to the usb hub
[33:18] and then i'm going to go back to the usb hub
[33:20] and then i'm going to go back to the usb hub
[33:22] and then i'm going to go back to the usb hub
[33:24] and then i'm going to go back to the usb hub
[33:26] and then i'm going to go back to the usb hub
[33:28] and then i'm going to go back to the usb hub
[33:30] and then i'm going to go back to the usb hub
[33:32] and then i'm going to go back to the usb hub
[33:34] and then i'm going to go back to the usb hub
[33:36] and then i'm going to go back to the usb hub
[33:38] and then i'm going to go back to the usb hub
[33:40] and then i'm going to go back to the usb hub
[33:42] and then i'm going to go back to the usb hub
[33:44] and then i'm going to go back to the usb hub
[33:46] and then i'm going to go back to the usb hub
[33:48] and then i'm going to go back to the usb hub
[33:50] and then i'm going to go back to the usb hub
[33:52] and then i'm going to go back to the usb hub
[33:54] and then i'm going to go back to the usb hub
[33:56] and then i'm going to go back to the usb hub
[33:58] and then i'm going to go back to the usb hub
[34:00] and then i'm going to go back to the usb hub
[34:02] and then i'm going to go back to the usb hub
[34:04] and then i'm going to go back to the usb hub
[34:06] and then i'm going to go back to the usb hub
[34:08] and then i'm going to go back to the usb hub
[34:10] and then i'm going to go back to the usb hub
[34:12] and then i'm going to go back to the usb hub
[34:14] and then i'm going to go back to the usb hub
[34:16] and then i'm going to go back to the usb hub
[34:18] and then i'm going to go back to the usb hub
[34:20] and then i'm going to go back to the usb hub
[34:22] and then i'm going to go back to the usb hub
[34:24] and then i'm going to go back to the usb hub
[34:26] and then i'm going to go back to the usb hub
[34:28] and then i'm going to go back to the usb hub
[34:30] and then i'm going to go back to the usb hub
[34:32] and then i'm going to go back to the usb hub
[34:34] and then i'm going to go back to the usb hub
[34:36] and then i'm going to go back to the usb hub
[34:38] and then i'm going to go back to the usb hub
[34:40] and then i'm going to go back to the usb hub
[34:42] and then i'm going to go back to the usb hub
[34:44] and then i'm going to go back to the usb hub
[34:46] and then i'm going to go back to the usb hub
[34:48] and then i'm going to go back to the usb hub
[34:50] and then i'm going to go back to the usb hub
[34:52] and then i'm going to go back to the usb hub
[34:54] and then i'm going to go back to the usb hub
[34:56] and then i'm going to go back to the usb hub
[34:58] and then i'm going to go back to the usb hub
[35:00] and then i'm going to go back to the usb hub
[35:02] and then i'm going to go back to the usb hub
[35:04] and then i'm going to go back to the usb hub
[35:06] and then i'm going to go back to the usb hub
[35:08] and then i'm going to go back to the usb hub
[35:10] and then i'm going to go back to the usb hub
[35:12] and then i'm going to go back to the usb hub
[35:14] and then i'm going to go back to the usb hub
[35:16] and then i'm going to go back to the usb hub
[35:18] and then i'm going to go back to the usb hub
[35:20] and then i'm going to go back to the usb hub
[35:22] and then i'm going to go back to the usb hub
[35:24] and then i'm going to go back to the usb hub
[35:26] and then i'm going to go back to the usb hub
[35:28] and then i'm going to go back to the usb hub
[35:30] and then i'm going to go back to the usb hub
[35:32] and then i'm going to go back to the usb hub
[35:34] and then i'm going to go back to the usb hub
[35:36] and then i'm going to go back to the usb hub
[35:38] and then i'm going to go back to the usb hub
[35:40] and then i'm going to go back to the usb hub
[35:42] and then i'm going to go back to the usb hub
[35:44] and then i'm going to go back to the usb hub
[35:46] and then i'm going to go back to the usb hub
[35:48] and then i'm going to go back to the usb hub
[35:50] and then i'm going to go back to the usb hub
[35:52] and then i'm going to go back to the usb hub
[35:54] and then i'm going to go back to the usb hub
[35:56] and then i'm going to go back to the usb hub
[35:58] and then i'm going to go back to the usb hub
[36:00] and then i'm going to go back to the usb hub
[36:02] and then i'm going to go back to the usb hub
[36:04] and then i'm going to go back to the usb hub
[36:06] and then i'm going to go back to the usb hub
[36:08] and then i'm going to go back to the usb hub
[36:10] and then i'm going to go back to the usb hub
[36:12] and then i'm going to go back to the usb hub
[36:14] and then i'm going to go back to the usb hub
[36:16] and then i'm going to go back to the usb hub
[36:18] and then i'm going to go back to the usb hub
[36:20] and then i'm going to go back to the usb hub
[36:22] and then i'm going to go back to the usb hub
[36:24] and then i'm going to go back to the usb hub
[36:26] and then i'm going to go back to the usb hub
[36:28] and then i'm going to go back to the usb hub
[36:30] and then i'm going to go back to the usb hub
[36:32] and then i'm going to go back to the usb hub
[36:34] and then i'm going to go back to the usb hub
[36:36] and then i'm going to go back to the usb hub
[36:38] and then i'm going to go back to the usb hub
[36:40] and then i'm going to go back to the usb hub
[36:42] and then i'm going to go back to the usb hub
[36:44] and then i'm going to go back to the usb hub
[36:46] and then i'm going to go back to the usb hub
[36:48] and then i'm going to go back to the usb hub
[36:50] and then i'm going to go back to the usb hub
[36:52] and then i'm going to go back to the usb hub
[36:54] and then i'm going to go back to the usb hub
[36:56] and then i'm going to go back to the usb hub
[36:58] and then i'm going to go back to the usb hub
[37:00] and then i'm going to go back to the usb hub
[37:02] and then i'm going to go back to the usb hub
[37:04] and then i'm going to go back to the usb hub
[37:06] and then i'm going to go back to the usb hub
[37:08] and then i'm going to go back to the usb hub
[37:10] and then i'm going to go back to the usb hub
[37:12] and then i'm going to go back to the usb hub
[37:14] and then i'm going to go back to the usb hub
[37:16] and then i'm going to go back to the usb hub
[37:18] and then i'm going to go back to the usb hub
[37:20] and then i'm going to go back to the usb hub
[37:22] and then i'm going to go back to the usb hub
[37:24] and then i'm going to go back to the usb hub
[37:26] and then i'm going to go back to the usb hub
[37:28] and then i'm going to go back to the usb hub
[37:30] and then i'm going to go back to the usb hub
[37:32] and then i'm going to go back to the usb hub
[37:34] and then i'm going to go back to the usb hub
[37:36] and then i'm going to go back to the usb hub
[37:38] and then i'm going to go back to the usb hub
[37:40] and then i'm going to go back to the usb hub
[37:42] and then i'm going to go back to the usb hub
[37:44] and then i'm going to go back to the usb hub
[37:46] and then i'm going to go back to the usb hub
[37:48] and then i'm going to go back to the usb hub
[37:50] and then i'm going to go back to the usb hub
[37:52] and then i'm going to go back to the usb hub
[37:54] and then i'm going to go back to the usb hub
[37:56] and then i'm going to go back to the usb hub
[37:58] and then i'm going to go back to the usb hub
[38:00] and then i'm going to go back to the usb hub
[38:02] and then i'm going to go back to the usb hub
[38:04] and then i'm going to go back to the usb hub
[38:06] and then i'm going to go back to the usb hub
[38:08] and then i'm going to go back to the usb hub
[38:10] and then i'm going to go back to the usb hub
[38:12] and then i'm going to go back to the usb hub
[38:14] and then i'm going to go back to the usb hub
[38:16] and then i'm going to go back to the usb hub
[38:18] and then i'm going to go back to the usb hub
[38:20] and then i'm going to go back to the usb hub
[38:22] and then i'm going to go back to the usb hub
[38:24] and then i'm going to go back to the usb hub
[38:26] and then i'm going to go back to the usb hub
[38:28] and then i'm going to go back to the usb hub
[38:30] and then i'm going to go back to the usb hub
[38:32] and then i'm going to go back to the usb hub
[38:34] and then i'm going to go back to the usb hub
[38:36] and then i'm going to go back to the usb hub
[38:38] and then i'm going to go back to the usb hub
[38:40] and then i'm going to go back to the usb hub
[38:42] and then i'm going to go back to the usb hub
[38:44] and then i'm going to go back to the usb hub
[38:46] and then i'm going to go back to the usb hub
[38:48] and then i'm going to go back to the usb hub
[38:50] and then i'm going to go back to the usb hub
[38:52] and then i'm going to go back to the usb hub
[38:54] and then i'm going to go back to the usb hub
[38:56] and then i'm going to go back to the usb hub
[38:58] and then i'm going to go back to the usb hub
[39:00] and then i'm going to go back to the usb hub
[39:02] and then i'm going to go back to the usb hub
[39:04] and then i'm going to go back to the usb hub
[39:06] and then i'm going to go back to the usb hub
[39:08] and then i'm going to go back to the usb hub
[39:10] and then i'm going to go back to the usb hub
[39:12] and then i'm going to go back to the usb hub
[39:14] and then i'm going to go back to the usb hub
[39:16] and then i'm going to go back to the usb hub
[39:18] and then i'm going to go back to the usb hub
[39:20] and then i'm going to go back to the usb hub
[39:22] and then i'm going to go back to the usb hub
[39:24] and then i'm going to go back to the usb hub
[39:26] and then i'm going to go back to the usb hub
[39:28] and then i'm going to go back to the usb hub
[39:30] and then i'm going to go back to the usb hub
[39:32] and then i'm going to go back to the usb hub
[39:34] and then i'm going to go back to the usb hub
[39:36] and then i'm going to go back to the usb hub
[39:38] and then i'm going to go back to the usb hub
[39:40] and then i'm going to go back to the usb hub
[39:42] and then i'm going to go back to the usb hub
[39:44] and then i'm going to go back to the usb hub
[39:46] and then i'm going to go back to the usb hub
[39:48] and then i'm going to go back to the usb hub
[39:50] and then i'm going to go back to the usb hub
[39:52] and then i'm going to go back to the usb hub
[39:54] and then i'm going to go back to the usb hub
[39:56] and then i'm going to go back to the usb hub
[39:58] and then i'm going to go back to the usb hub
[40:00] and then i'm going to go back to the usb hub
[40:02] and then i'm going to go back to the usb hub
[40:04] and then i'm going to go back to the usb hub
[40:06] and then i'm going to go back to the usb hub
[40:08] and then i'm going to go back to the usb hub
[40:10] and then i'm going to go back to the usb hub
[40:12] and then i'm going to go back to the usb hub
[40:14] and then i'm going to go back to the usb hub
[40:16] and then i'm going to go back to the usb hub
[40:18] and then i'm going to go back to the usb hub
[40:20] and then i'm going to go back to the usb hub
[40:22] and then i'm going to go back to the usb hub
[40:24] and then i'm going to go back to the usb hub
[40:26] and then i'm going to go back to the usb hub
[40:28] and then i'm going to go back to the usb hub
[40:30] and then i'm going to go back to the usb hub
[40:32] and then i'm going to go back to the usb hub
[40:34] and then i'm going to go back to the usb hub
[40:36] and then i'm going to go back to the usb hub
[40:38] and then i'm going to go back to the usb hub
[40:40] and then i'm going to go back to the usb hub
[40:42] and then i'm going to go back to the usb hub
[40:44] and then i'm going to go back to the usb hub
[40:46] and then i'm going to go back to the usb hub
[40:48] and then i'm going to go back to the usb hub
[40:50] and then i'm going to go back to the usb hub
[40:52] and then i'm going to go back to the usb hub
[40:54] and then i'm going to go back to the usb hub
[40:56] and then i'm going to go back to the usb hub
[40:58] and then i'm going to go back to the usb hub
[41:00] and then i'm going to go back to the usb hub
[41:02] and then i'm going to go back to the usb hub
[41:04] and then i'm going to go back to the usb hub
[41:06] and then i'm going to go back to the usb hub
[41:08] and then i'm going to go back to the usb hub
[41:10] and then i'm going to go back to the usb hub
[41:12] and then i'm going to go back to the usb hub
[41:14] and then i'm going to go back to the usb hub
[41:16] and then i'm going to go back to the usb hub
[41:18] and then i'm going to go back to the usb hub
[41:20] and then i'm going to go back to the usb hub
[41:22] and then i'm going to go back to the usb hub
[41:24] and then i'm going to go back to the usb hub
[41:26] and then i'm going to go back to the usb hub
[41:28] and then i'm going to go back to the usb hub
[41:30] and then i'm going to go back to the usb hub
[41:32] and then i'm going to go back to the usb hub
[41:34] and then i'm going to go back to the usb hub
[41:36] and then i'm going to go back to the usb hub
[41:38] and then i'm going to go back to the usb hub
[41:40] and then i'm going to go back to the usb hub
[41:42] and then i'm going to go back to the usb hub
[41:44] and then i'm going to go back to the usb hub
[41:46] and then i'm going to go back to the usb hub
[41:48] and then i'm going to go back to the usb hub
[41:50] and then i'm going to go back to the usb hub
[41:52] and then i'm going to go back to the usb hub
[41:54] and then i'm going to go back to the usb hub
[41:56] and then i'm going to go back to the usb hub
[41:58] and then i'm going to go back to the usb hub
[42:00] and then i'm going to go back to the usb hub
[42:02] and then i'm going to go back to the usb hub
[42:04] and then i'm going to go back to the usb hub
[42:06] and then i'm going to go back to the usb hub
[42:08] and then i'm going to go back to the usb hub
[42:10] and then i'm going to go back to the usb hub
[42:12] and then i'm going to go back to the usb hub
[42:14] and then i'm going to go back to the usb hub
[42:16] and then i'm going to go back to the usb hub
[42:18] and then i'm going to go back to the usb hub
[42:20] and then i'm going to go back to the usb hub
[42:22] and then i'm going to go back to the usb hub
[42:24] and then i'm going to go back to the usb hub
[42:26] and then i'm going to go back to the usb hub
[42:28] and then i'm going to go back to the usb hub
[42:30] and then i'm going to go back to the usb hub
[42:32] and then i'm going to go back to the usb hub
[42:34] and then i'm going to go back to the usb hub
[42:36] and then i'm going to go back to the usb hub
[42:38] and then i'm going to go back to the usb hub
[42:40] and then i'm going to go back to the usb hub
[42:42] and then i'm going to go back to the usb hub
[42:44] and then i'm going to go back to the usb hub
[42:46] and then i'm going to go back to the usb hub
[42:48] and then i'm going to go back to the usb hub
[42:50] and then i'm going to go back to the usb hub
[42:52] and then i'm going to go back to the usb hub
[42:54] and then i'm going to go back to the usb hub
[42:56] and then i'm going to go back to the usb hub
[42:58] and then i'm going to go back to the usb hub
[43:00] and then i'm going to go back to the usb hub
[43:02] and then i'm going to go back to the usb hub
[43:04] and then i'm going to go back to the usb hub
[43:06] and then i'm going to go back to the usb hub
[43:08] and then i'm going to go back to the usb hub
[43:10] and then i'm going to go back to the usb hub
[43:12] and then i'm going to go back to the usb hub
[43:14] and then i'm going to go back to the usb hub
[43:16] and then i'm going to go back to the usb hub
[43:18] and then i'm going to go back to the usb hub
[43:20] and then i'm going to go back to the usb hub
[43:22] and then i'm going to go back to the usb hub
[43:24] and then i'm going to go back to the usb hub
[43:26] and then i'm going to go back to the usb hub
[43:28] and then i'm going to go back to the usb hub
[43:30] and then i'm going to go back to the usb hub
[43:32] and then i'm going to go back to the usb hub
[43:34] and then i'm going to go back to the usb hub
[43:36] and then i'm going to go back to the usb hub
[43:38] and then i'm going to go back to the usb hub
[43:40] and then i'm going to go back to the usb hub
[43:42] and then i'm going to go back to the usb hub
[43:44] and then i'm going to go back to the usb hub
[43:46] and then i'm going to go back to the usb hub
[43:48] and then i'm going to go back to the usb hub
[43:50] and then i'm going to go back to the usb hub
[43:52] and then i'm going to go back to the usb hub
[43:54] and then i'm going to go back to the usb hub
[43:56] and then i'm going to go back to the usb hub
[43:58] and then i'm going to go back to the usb hub
[44:00] and then i'm going to go back to the usb hub
[44:02] and then i'm going to go back to the usb hub
[44:04] and then i'm going to go back to the usb hub
[44:06] and then i'm going to go back to the usb hub
[44:08] and then i'm going to go back to the usb hub
[44:10] and then i'm going to go back to the usb hub
[44:12] and then i'm going to go back to the usb hub
[44:14] and then i'm going to go back to the usb hub
[44:16] and then i'm going to go back to the usb hub
[44:18] and then i'm going to go back to the usb hub
[44:20] and then i'm going to go back to the usb hub
[44:22] and then i'm going to go back to the usb hub
[44:24] and then i'm going to go back to the usb hub
[44:26] and then i'm going to go back to the usb hub
[44:28] and then i'm going to go back to the usb hub
[44:30] and then i'm going to go back to the usb hub
[44:32] and then i'm going to go back to the usb hub
[44:34] and then i'm going to go back to the usb hub
[44:36] and then i'm going to go back to the usb hub
[44:38] and then i'm going to go back to the usb hub
[44:40] and then i'm going to go back to the usb hub
[44:42] and then i'm going to go back to the usb hub
[44:44] and then i'm going to go back to the usb hub
[44:46] and then i'm going to go back to the usb hub
[44:48] and then i'm going to go back to the usb hub
[44:50] and then i'm going to go back to the usb hub
[44:52] and then i'm going to go back to the usb hub
[44:54] and then i'm going to go back to the usb hub
[44:56] and then i'm going to go back to the usb hub
[44:58] and then i'm going to go back to the usb hub
[45:00] and then i'm going to go back to the usb hub
[45:02] and then i'm going to go back to the usb hub
[45:04] and then i'm going to go back to the usb hub
[45:06] and then i'm going to go back to the usb hub
[45:08] and then i'm going to go back to the usb hub
[45:10] and then i'm going to go back to the usb hub
[45:12] and then i'm going to go back to the usb hub
[45:14] and then i'm going to go back to the usb hub
[45:16] and then i'm going to go back to the usb hub
[45:18] and then i'm going to go back to the usb hub
[45:20] and then i'm going to go back to the usb hub
[45:22] and then i'm going to go back to the usb hub
[45:24] and then i'm going to go back to the usb hub
[45:26] and then i'm going to go back to the usb hub
[45:28] and then i'm going to go back to the usb hub
[45:30] and then i'm going to go back to the usb hub
[45:32] and then i'm going to go back to the usb hub
[45:34] and then i'm going to go back to the usb hub
[45:36] and then i'm going to go back to the usb hub
[45:38] and then i'm going to go back to the usb hub
[45:40] and then i'm going to go back to the usb hub
[45:42] and then i'm going to go back to the usb hub
[45:44] and then i'm going to go back to the usb hub
[45:46] and then i'm going to go back to the usb hub
[45:48] and then i'm going to go back to the usb hub
[45:50] and then i'm going to go back to the usb hub
[45:52] and then i'm going to go back to the usb hub
[45:54] and then i'm going to go back to the usb hub
[45:56] and then i'm going to go back to the usb hub
[45:58] and then i'm going to go back to the usb hub
[46:00] and then i'm going to go back to the usb hub
[46:02] and then i'm going to go back to the usb hub
[46:04] and then i'm going to go back to the usb hub
[46:06] and then i'm going to go back to the usb hub
[46:08] and then i'm going to go back to the usb hub
[46:10] and then i'm going to go back to the usb hub
[46:12] and then i'm going to go back to the usb hub
[46:14] and then i'm going to go back to the usb hub
[46:16] and then i'm going to go back to the usb hub
[46:18] and then i'm going to go back to the usb hub
[46:20] and then i'm going to go back to the usb hub
[46:22] and then i'm going to go back to the usb hub
[46:24] and then i'm going to go back to the usb hub
[46:26] and then i'm going to go back to the usb hub
[46:28] and then i'm going to go back to the usb hub
[46:30] and then i'm going to go back to the usb hub
[46:32] and then i'm going to go back to the usb hub
[46:34] and then i'm going to go back to the usb hub
[46:36] and then i'm going to go back to the usb hub
[46:38] and then i'm going to go back to the usb hub
[46:40] and then i'm going to go back to the usb hub
[46:42] and then i'm going to go back to the usb hub
[46:44] and then i'm going to go back to the usb hub
[46:46] and then i'm going to go back to the usb hub
[46:48] and then i'm going to go back to the usb hub
[46:50] and then i'm going to go back to the usb hub
[46:52] and then i'm going to go back to the usb hub
[46:54] and then i'm going to go back to the usb hub
[46:56] and then i'm going to go back to the usb hub
[46:58] and then i'm going to go back to the usb hub
[47:00] and then i'm going to go back to the usb hub
[47:02] and then i'm going to go back to the usb hub
[47:04] and then i'm going to go back to the usb hub
[47:06] and then i'm going to go back to the usb hub
[47:08] and then i'm going to go back to the usb hub
[47:10] and then i'm going to go back to the usb hub
[47:12] and then i'm going to go back to the usb hub
[47:14] and then i'm going to go back to the usb hub
[47:16] and then i'm going to go back to the usb hub
[47:18] and then i'm going to go back to the usb hub
[47:20] and then i'm going to go back to the usb hub
[47:22] and then i'm going to go back to the usb hub
[47:24] and then i'm going to go back to the usb hub
[47:26] and then i'm going to go back to the usb hub
[47:28] and then i'm going to go back to the usb hub
[47:30] and then i'm going to go back to the usb hub
[47:32] and then i'm going to go back to the usb hub
[47:34] and then i'm going to go back to the usb hub
[47:36] and then i'm going to go back to the usb hub
[47:38] and then i'm going to go back to the usb hub
[47:40] and then i'm going to go back to the usb hub
[47:42] and then i'm going to go back to the usb hub
[47:44] and then i'm going to go back to the usb hub
[47:46] and then i'm going to go back to the usb hub
[47:48] and then i'm going to go back to the usb hub
[47:50] and then i'm going to go back to the usb hub
[47:52] and then i'm going to go back to the usb hub
[47:54] and then i'm going to go back to the usb hub
[47:56] and then i'm going to go back to the usb hub
[47:58] and then i'm going to go back to the usb hub
[48:00] and then i'm going to go back to the usb hub
[48:02] and then i'm going to go back to the usb hub
[48:04] and then i'm going to go back to the usb hub
[48:06] and then i'm going to go back to the usb hub
[48:08] and then i'm going to go back to the usb hub
[48:10] and then i'm going to go back to the usb hub
[48:12] and then i'm going to go back to the usb hub
[48:14] and then i'm going to go back to the usb hub
[48:16] and then i'm going to go back to the usb hub
[48:18] and then i'm going to go back to the usb hub
[48:20] and then i'm going to go back to the usb hub
[48:22] and then i'm going to go back to the usb hub
[48:24] and then i'm going to go back to the usb hub
[48:26] and then i'm going to go back to the usb hub
[48:28] and then i'm going to go back to the usb hub
[48:30] and then i'm going to go back to the usb hub
[48:32] and then i'm going to go back to the usb hub
[48:34] and then i'm going to go back to the usb hub
[48:36] and then i'm going to go back to the usb hub
[48:38] and then i'm going to go back to the usb hub
[48:40] and then i'm going to go back to the usb hub
[48:42] and then i'm going to go back to the usb hub
[48:44] and then i'm going to go back to the usb hub
[48:46] and then i'm going to go back to the usb hub
[48:48] and then i'm going to go back to the usb hub
[48:50] and then i'm going to go back to the usb hub
[48:52] and then i'm going to go back to the usb hub
[48:54] and then i'm going to go back to the usb hub
[48:56] and then i'm going to go back to the usb hub
[48:58] and then i'm going to go back to the usb hub
[49:00] and then i'm going to go back to the usb hub
[49:02] and then i'm going to go back to the usb hub
[49:04] and then i'm going to go back to the usb hub
[49:06] and then i'm going to go back to the usb hub
[49:08] and then i'm going to go back to the usb hub
[49:10] and then i'm going to go back to the usb hub
[49:12] and then i'm going to go back to the usb hub
[49:14] and then i'm going to go back to the usb hub
[49:16] and then i'm going to go back to the usb hub
[49:18] and then i'm going to go back to the usb hub
[49:20] and then i'm going to go back to the usb hub
[49:22] and then i'm going to go back to the usb hub
[49:24] and then i'm going to go back to the usb hub
[49:26] and then i'm going to go back to the usb hub
[49:28] and then i'm going to go back to the usb hub
[49:30] and then i'm going to go back to the usb hub
[49:32] and then i'm going to go back to the usb hub
[49:34] and then i'm going to go back to the usb hub
[49:36] and then i'm going to go back to the usb hub
[49:38] and then i'm going to go back to the usb hub
[49:40] and then i'm going to go back to the usb hub
[49:42] and then i'm going to go back to the usb hub
[49:44] and then i'm going to go back to the usb hub
[49:46] and then i'm going to go back to the usb hub
[49:48] and then i'm going to go back to the usb hub
[49:50] and then i'm going to go back to the usb hub
[49:52] and then i'm going to go back to the usb hub
[49:54] and then i'm going to go back to the usb hub
[49:56] and then i'm going to go back to the usb hub
[49:58] and then i'm going to go back to the usb hub
[50:00] and then i'm going to go back to the usb hub
[50:02] and then i'm going to go back to the usb hub
[50:04] and then i'm going to go back to the usb hub
[50:06] and then i'm going to go back to the usb hub
[50:08] and then i'm going to go back to the usb hub
[50:10] and then i'm going to go back to the usb hub
[50:12] and then i'm going to go back to the usb hub
[50:14] and then i'm going to go back to the usb hub
[50:16] and then i'm going to go back to the usb hub
[50:18] and then i'm going to go back to the usb hub
[50:20] and then i'm going to go back to the usb hub
[50:22] and then i'm going to go back to the usb hub
[50:24] and then i'm going to go back to the usb hub
[50:26] and then i'm going to go back to the usb hub
[50:28] and then i'm going to go back to the usb hub
[50:30] and then i'm going to go back to the usb hub
[50:32] and then i'm going to go back to the usb hub
[50:34] and then i'm going to go back to the usb hub
[50:36] and then i'm going to go back to the usb hub
[50:38] and then i'm going to go back to the usb hub
[50:40] and then i'm going to go back to the usb hub
[50:42] and then i'm going to go back to the usb hub
[50:44] and then i'm going to go back to the usb hub
[50:46] and then i'm going to go back to the usb hub
[50:48] and then i'm going to go back to the usb hub
[50:50] and then i'm going to go back to the usb hub
[50:52] and then i'm going to go back to the usb hub
[50:54] and then i'm going to go back to the usb hub
[50:56] and then i'm going to go back to the usb hub
[50:58] and then i'm going to go back to the usb hub
[51:00] and then i'm going to go back to the usb hub
[51:02] and then i'm going to go back to the usb hub
[51:04] and then i'm going to go back to the usb hub
[51:06] and then i'm going to go back to the usb hub
[51:08] and then i'm going to go back to the usb hub
[51:10] and then i'm going to go back to the usb hub
[51:12] and then i'm going to go back to the usb hub
[51:14] and then i'm going to go back to the usb hub
[51:16] and then i'm going to go back to the usb hub
[51:18] and then i'm going to go back to the usb hub
[51:20] and then i'm going to go back to the usb hub
[51:22] and then i'm going to go back to the usb hub
[51:24] and then i'm going to go back to the usb hub
[51:26] and then i'm going to go back to the usb hub
[51:28] and then i'm going to go back to the usb hub
[51:30] and then i'm going to go back to the usb hub
[51:32] and then i'm going to go back to the usb hub
[51:34] and then i'm going to go back to the usb hub
[51:36] and then i'm going to go back to the usb hub
[51:38] and then i'm going to go back to the usb hub
[51:40] and then i'm going to go back to the usb hub
[51:42] and then i'm going to go back to the usb hub
[51:44] and then i'm going to go back to the usb hub
[51:46] and then i'm going to go back to the usb hub
[51:48] and then i'm going to go back to the usb hub
[51:50] and then i'm going to go back to the usb hub
[51:52] and then i'm going to go back to the usb hub
[51:54] and then i'm going to go back to the usb hub
[51:56] and then i'm going to go back to the usb hub
[51:58] and then i'm going to go back to the usb hub
[52:00] and then i'm going to go back to the usb hub
[52:02] and then i'm going to go back to the usb hub
[52:04] and then i'm going to go back to the usb hub
[52:06] and then i'm going to go back to the usb hub
[52:08] and then i'm going to go back to the usb hub
[52:10] and then i'm going to go back to the usb hub
[52:12] and then i'm going to go back to the usb hub
[52:14] and then i'm going to go back to the usb hub
[52:16] and then i'm going to go back to the usb hub
[52:18] and then i'm going to go back to the usb hub
[52:20] and then i'm going to go back to the usb hub
[52:22] and then i'm going to go back to the usb hub
[52:24] and then i'm going to go back to the usb hub
[52:26] and then i'm going to go back to the usb hub
[52:28] and then i'm going to go back to the usb hub
[52:30] and then i'm going to go back to the usb hub
[52:32] and then i'm going to go back to the usb hub
[52:34] and then i'm going to go back to the usb hub
[52:36] and then i'm going to go back to the usb hub
[52:38] and then i'm going to go back to the usb hub
[52:40] and then i'm going to go back to the usb hub
[52:42] and then i'm going to go back to the usb hub
[52:44] and then i'm going to go back to the usb hub
[52:46] and then i'm going to go back to the usb hub
[52:48] and then i'm going to go back to the usb hub
[52:50] and then i'm going to go back to the usb hub
[52:52] and then i'm going to go back to the usb hub
[52:54] and then i'm going to go back to the usb hub
[52:56] and then i'm going to go back to the usb hub
[52:58] and then i'm going to go back to the usb hub
[53:00] and then i'm going to go back to the usb hub
[53:02] and then i'm going to go back to the usb hub
[53:04] and then i'm going to go back to the usb hub
[53:06] and then i'm going to go back to the usb hub
[53:08] and then i'm going to go back to the usb hub
[53:10] and then i'm going to go back to the usb hub
[53:12] and then i'm going to go back to the usb hub
[53:14] and then i'm going to go back to the usb hub
[53:16] and then i'm going to go back to the usb hub
[53:18] and then i'm going to go back to the usb hub
[53:20] and then i'm going to go back to the usb hub
[53:22] and then i'm going to go back to the usb hub
[53:24] and then i'm going to go back to the usb hub
[53:26] and then i'm going to go back to the usb hub
[53:28] and then i'm going to go back to the usb hub
[53:30] and then i'm going to go back to the usb hub
[53:32] and then i'm going to go back to the usb hub
[53:34] and then i'm going to go back to the usb hub
[53:36] and then i'm going to go back to the usb hub
[53:38] and then i'm going to go back to the usb hub
[53:40] and then i'm going to go back to the usb hub
[53:42] and then i'm going to go back to the usb hub
[53:44] and then i'm going to go back to the usb hub
[53:46] and then i'm going to go back to the usb hub
[53:48] and then i'm going to go back to the usb hub
[53:50] and then i'm going to go back to the usb hub
[53:52] and then i'm going to go back to the usb hub
[53:54] and then i'm going to go back to the usb hub
[53:56] and then i'm going to go back to the usb hub
[53:58] and then i'm going to go back to the usb hub
[54:00] and then i'm going to go back to the usb hub
[54:02] and then i'm going to go back to the usb hub
[54:04] and then i'm going to go back to the usb hub
[54:06] and then i'm going to go back to the usb hub
[54:08] and then i'm going to go back to the usb hub
[54:10] and then i'm going to go back to the usb hub
[54:12] and then i'm going to go back to the usb hub
[54:14] and then i'm going to go back to the usb hub
[54:16] and then i'm going to go back to the usb hub
[54:18] and then i'm going to go back to the usb hub
[54:20] and then i'm going to go back to the usb hub
[54:22] and then i'm going to go back to the usb hub
[54:24] and then i'm going to go back to the usb hub
[54:26] and then i'm going to go back to the usb hub
[54:28] and then i'm going to go back to the usb hub
[54:30] and then i'm going to go back to the usb hub
[54:32] and then i'm going to go back to the usb hub
[54:34] and then i'm going to go back to the usb hub
[54:36] and then i'm going to go back to the usb hub
[54:38] and then i'm going to go back to the usb hub
[54:40] and then i'm going to go back to the usb hub
[54:42] and then i'm going to go back to the usb hub
[54:44] and then i'm going to go back to the usb hub
[54:46] and then i'm going to go back to the usb hub
[54:48] and then i'm going to go back to the usb hub
[54:50] and then i'm going to go back to the usb hub
[54:52] and then i'm going to go back to the usb hub
[54:54] and then i'm going to go back to the usb hub
[54:56] and then i'm going to go back to the usb hub
[54:58] and then i'm going to go back to the usb hub
[55:00] and then i'm going to go back to the usb hub
[55:02] and then i'm going to go back to the usb hub
[55:04] and then i'm going to go back to the usb hub
[55:06] and then i'm going to go back to the usb hub
[55:08] and then i'm going to go back to the usb hub
[55:10] and then i'm going to go back to the usb hub
[55:12] and then i'm going to go back to the usb hub
[55:14] and then i'm going to go back to the usb hub
[55:16] and then i'm going to go back to the usb hub
[55:18] and then i'm going to go back to the usb hub
[55:20] and then i'm going to go back to the usb hub
[55:22] and then i'm going to go back to the usb hub
[55:24] and then i'm going to go back to the usb hub
[55:26] and then i'm going to go back to the usb hub
[55:28] and then i'm going to go back to the usb hub
[55:30] and then i'm going to go back to the usb hub
[55:32] and then i'm going to go back to the usb hub
[55:34] and then i'm going to go back to the usb hub
[55:36] and then i'm going to go back to the usb hub
[55:38] and then i'm going to go back to the usb hub
[55:40] and then i'm going to go back to the usb hub
[55:42] and then i'm going to go back to the usb hub
[55:44] and then i'm going to go back to the usb hub
[55:46] and then i'm going to go back to the usb hub
[55:48] and then i'm going to go back to the usb hub
[55:50] and then i'm going to go back to the usb hub
[55:52] and then i'm going to go back to the usb hub
[55:54] and then i'm going to go back to the usb hub
[55:56] and then i'm going to go back to the usb hub
[55:58] and then i'm going to go back to the usb hub
[56:00] and then i'm going to go back to the usb hub
[56:02] and then i'm going to go back to the usb hub
[56:04] and then i'm going to go back to the usb hub
[56:06] and then i'm going to go back to the usb hub
[56:08] and then i'm going to go back to the usb hub
[56:10] and then i'm going to go back to the usb hub
[56:12] and then i'm going to go back to the usb hub
[56:14] and then i'm going to go back to the usb hub
[56:16] and then i'm going to go back to the usb hub
[56:18] and then i'm going to go back to the usb hub
[56:20] and then i'm going to go back to the usb hub
[56:22] and then i'm going to go back to the usb hub
[56:24] and then i'm going to go back to the usb hub
[56:26] and then i'm going to go back to the usb hub
[56:28] and then i'm going to go back to the usb hub
[56:30] and then i'm going to go back to the usb hub
[56:32] and then i'm going to go back to the usb hub
[56:34] and then i'm going to go back to the usb hub
[56:36] and then i'm going to go back to the usb hub
[56:38] and then i'm going to go back to the usb hub
[56:40] and then i'm going to go back to the usb hub
[56:42] and then i'm going to go back to the usb hub
[56:44] and then i'm going to go back to the usb hub
[56:46] and then i'm going to go back to the usb hub
[56:48] and then i'm going to go back to the usb hub
[56:50] and then i'm going to go back to the usb hub
[56:52] and then i'm going to go back to the usb hub
[56:54] and then i'm going to go back to the usb hub
[56:56] and then i'm going to go back to the usb hub
[56:58] and then i'm going to go back to the usb hub
[57:00] and then i'm going to go back to the usb hub
[57:02] and then i'm going to go back to the usb hub
[57:04] and then i'm going to go back to the usb hub
[57:06] and then i'm going to go back to the usb hub
[57:08] and then i'm going to go back to the usb hub
[57:10] and then i'm going to go back to the usb hub
[57:12] and then i'm going to go back to the usb hub
[57:14] and then i'm going to go back to the usb hub
[57:16] and then i'm going to go back to the usb hub
[57:18] and then i'm going to go back to the usb hub
[57:20] and then i'm going to go back to the usb hub
[57:22] and then i'm going to go back to the usb hub
[57:24] and then i'm going to go back to the usb hub
[57:26] and then i'm going to go back to the usb hub
[57:28] and then i'm going to go back to the usb hub
[57:30] and then i'm going to go back to the usb hub
[57:32] and then i'm going to go back to the usb hub
[57:34] and then i'm going to go back to the usb hub
[57:36] and then i'm going to go back to the usb hub
[57:38] and then i'm going to go back to the usb hub
[57:40] and then i'm going to go back to the usb hub
[57:42] and then i'm going to go back to the usb hub
[57:44] and then i'm going to go back to the usb hub
[57:46] and then i'm going to go back to the usb hub
[57:48] and then i'm going to go back to the usb hub
[57:50] and then i'm going to go back to the usb hub
[57:52] and then i'm going to go back to the usb hub
[57:54] and then i'm going to go back to the usb hub
[57:56] and then i'm going to go back to the usb hub
[57:58] and then i'm going to go back to the usb hub
[58:00] and then i'm going to go back to the usb hub
[58:02] and then i'm going to go back to the usb hub
[58:04] and then i'm going to go back to the usb hub
[58:06] and then i'm going to go back to the usb hub
[58:08] and then i'm going to go back to the usb hub
[58:10] and then i'm going to go back to the usb hub
[58:12] and then i'm going to go back to the usb hub
[58:14] and then i'm going to go back to the usb hub
[58:16] and then i'm going to go back to the usb hub
[58:18] and then i'm going to go back to the usb hub
[58:20] and then i'm going to go back to the usb hub
[58:22] and then i'm going to go back to the usb hub
[58:24] and then i'm going to go back to the usb hub
[58:26] and then i'm going to go back to the usb hub
[58:28] and then i'm going to go back to the usb hub
[58:30] and then i'm going to go back to the usb hub
[58:32] and then i'm going to go back to the usb hub
[58:34] and then i'm going to go back to the usb hub
[58:36] and then i'm going to go back to the usb hub
[58:38] and then i'm going to go back to the usb hub
[58:40] and then i'm going to go back to the usb hub
[58:42] and then i'm going to go back to the usb hub
[58:44] and then i'm going to go back to the usb hub
[58:46] and then i'm going to go back to the usb hub
[58:48] and then i'm going to go back to the usb hub
[58:50] and then i'm going to go back to the usb hub
[58:52] and then i'm going to go back to the usb hub
[58:54] and then i'm going to go back to the usb hub
[58:56] and then i'm going to go back to the usb hub
[58:58] and then i'm going to go back to the usb hub
[59:00] and then i'm going to go back to the usb hub
[59:02] and then i'm going to go back to the usb hub
[59:04] and then i'm going to go back to the usb hub
[59:06] and then i'm going to go back to the usb hub
[59:08] and then i'm going to go back to the usb hub
[59:10] and then i'm going to go back to the usb hub
[59:12] and then i'm going to go back to the usb hub
[59:14] and then i'm going to go back to the usb hub
[59:16] and then i'm going to go back to the usb hub
[59:18] and then i'm going to go back to the usb hub
[59:20] and then i'm going to go back to the usb hub
[59:22] and then i'm going to go back to the usb hub
[59:24] and then i'm going to go back to the usb hub
[59:26] and then i'm going to go back to the usb hub
[59:28] and then i'm going to go back to the usb hub
[59:30] and then i'm going to go back to the usb hub
[59:32] and then i'm going to go back to the usb hub
[59:34] and then i'm going to go back to the usb hub
[59:36] and then i'm going to go back to the usb hub
[59:38] and then i'm going to go back to the usb hub
[59:40] and then i'm going to go back to the usb hub
[59:42] and then i'm going to go back to the usb hub
[59:44] and then i'm going to go back to the usb hub
[59:46] and then i'm going to go back to the usb hub
[59:48] and then i'm going to go back to the usb hub
[59:50] and then i'm going to go back to the usb hub
[59:52] and then i'm going to go back to the usb hub
[59:54] and then i'm going to go back to the usb hub
[59:56] and then i'm going to go back to the usb hub
[59:58] and then i'm going to go back to the usb hub
[60:00] and then i'm going to go back to the usb hub
[60:02] and then i'm going to go back to the usb hub
[60:04] and then i'm going to go back to the usb hub
[60:06] and then i'm going to go back to the usb hub
[60:08] and then i'm going to go back to the usb hub
[60:10] and then i'm going to go back to the usb hub
[60:12] and then i'm going to go back to the usb hub
[60:14] and then i'm going to go back to the usb hub
[60:16] and then i'm going to go back to the usb hub
[60:18] and then i'm going to go back to the usb hub
[60:20] and then i'm going to go back to the usb hub
[60:22] and then i'm going to go back to the usb hub
[60:24] and then i'm going to go back to the usb hub
[60:26] and then i'm going to go back to the usb hub
[60:28] and then i'm going to go back to the usb hub
[60:30] and then i'm going to go back to the usb hub
[60:32] and then i'm going to go back to the usb hub
[60:34] and then i'm going to go back to the usb hub
[60:36] and then i'm going to go back to the usb hub
[60:38] and then i'm going to go back to the usb hub
[60:40] and then i'm going to go back to the usb hub
[60:42] and then i'm going to go back to the usb hub
[60:44] and then i'm going to go back to the usb hub
[60:46] and then i'm going to go back to the usb hub
[60:48] and then i'm going to go back to the usb hub
[60:50] and then i'm going to go back to the usb hub
[60:52] and then i'm going to go back to the usb hub
[60:54] and then i'm going to go back to the usb hub
[60:56] and then i'm going to go back to the usb hub
[60:58] and then i'm going to go back to the usb hub
[61:00] and then i'm going to go back to the usb hub
[61:02] and then i'm going to go back to the usb hub
[61:04] and then i'm going to go back to the usb hub
[61:06] and then i'm going to go back to the usb hub
[61:08] and then i'm going to go back to the usb hub
[61:10] and then i'm going to go back to the usb hub
[61:12] and then i'm going to go back to the usb hub
[61:14] and then i'm going to go back to the usb hub
[61:16] and then i'm going to go back to the usb hub
[61:18] and then i'm going to go back to the usb hub
[61:20] and then i'm going to go back to the usb hub
[61:22] and then i'm going to go back to the usb hub
[61:24] and then i'm going to go back to the usb hub
[61:26] and then i'm going to go back to the usb hub
[61:28] and then i'm going to go back to the usb hub
[61:30] and then i'm going to go back to the usb hub
[61:32] and then i'm going to go back to the usb hub
[61:34] and then i'm going to go back to the usb hub
[61:36] and then i'm going to go back to the usb hub
[61:38] and then i'm going to go back to the usb hub
[61:40] and then i'm going to go back to the usb hub
[61:42] and then i'm going to go back to the usb hub
[61:44] and then i'm going to go back to the usb hub
[61:46] and then i'm going to go back to the usb hub
[61:48] and then i'm going to go back to the usb hub
[61:50] and then i'm going to go back to the usb hub
[61:52] and then i'm going to go back to the usb hub
[61:54] and then i'm going to go back to the usb hub
[61:56] and then i'm going to go back to the usb hub
[61:58] and then i'm going to go back to the usb hub
[62:00] and then i'm going to go back to the usb hub
[62:02] and then i'm going to go back to the usb hub
[62:04] and then i'm going to go back to the usb hub
[62:06] and then i'm going to go back to the usb hub
[62:08] and then i'm going to go back to the usb hub
[62:10] and then i'm going to go back to the usb hub
[62:12] and then i'm going to go back to the usb hub
[62:14] and then i'm going to go back to the usb hub
[62:16] and then i'm going to go back to the usb hub
[62:18] and then i'm going to go back to the usb hub
[62:20] and then i'm going to go back to the usb hub
[62:22] and then i'm going to go back to the usb hub
[62:24] and then i'm going to go back to the usb hub
[62:26] and then i'm going to go back to the usb hub
[62:28] and then i'm going to go back to the usb hub
[62:30] and then i'm going to go back to the usb hub
[62:32] and then i'm going to go back to the usb hub
[62:34] and then i'm going to go back to the usb hub
[62:36] and then i'm going to go back to the usb hub
[62:38] and then i'm going to go back to the usb hub
[62:40] and then i'm going to go back to the usb hub
[62:42] and then i'm going to go back to the usb hub
[62:44] and then i'm going to go back to the usb hub
[62:46] and then i'm going to go back to the usb hub
[62:48] and then i'm going to go back to the usb hub
[62:50] and then i'm going to go back to the usb hub
[62:52] and then i'm going to go back to the usb hub
[62:54] and then i'm going to go back to the usb hub
[62:56] and then i'm going to go back to the usb hub
[62:58] and then i'm going to go back to the usb hub
[63:00] and then i'm going to go back to the usb hub
[63:02] and then i'm going to go back to the usb hub
[63:04] and then i'm going to go back to the usb hub
[63:06] and then i'm going to go back to the usb hub
[63:08] and then i'm going to go back to the usb hub
[63:10] and then i'm going to go back to the usb hub
[63:12] and then i'm going to go back to the usb hub
[63:14] and then i'm going to go back to the usb hub
[63:16] and then i'm going to go back to the usb hub
[63:18] and then i'm going to go back to the usb hub
[63:20] and then i'm going to go back to the usb hub
[63:22] and then i'm going to go back to the usb hub
[63:24] and then i'm going to go back to the usb hub
[63:26] and then i'm going to go back to the usb hub
[63:28] and then i'm going to go back to the usb hub
[63:30] and then i'm going to go back to the usb hub
[63:32] and then i'm going to go back to the usb hub
[63:34] and then i'm going to go back to the usb hub
[63:36] and then i'm going to go back to the usb hub
[63:38] and then i'm going to go back to the usb hub
[63:40] and then i'm going to go back to the usb hub
[63:42] and then i'm going to go back to the usb hub
[63:44] and then i'm going to go back to the usb hub
[63:46] and then i'm going to go back to the usb hub
[63:48] and then i'm going to go back to the usb hub
[63:50] and then i'm going to go back to the usb hub
[63:52] and then i'm going to go back to the usb hub
[63:54] and then i'm going to go back to the usb hub
[63:56] and then i'm going to go back to the usb hub
[63:58] and then i'm going to go back to the usb hub
[64:00] and then i'm going to go back to the usb hub
[64:02] and then i'm going to go back to the usb hub
[64:04] and then i'm going to go back to the usb hub
[64:06] and then i'm going to go back to the usb hub
[64:08] and then i'm going to go back to the usb hub
[64:10] and then i'm going to go back to the usb hub
[64:12] and then i'm going to go back to the usb hub
[64:14] and then i'm going to go back to the usb hub
[64:16] and then i'm going to go back to the usb hub
[64:18] and then i'm going to go back to the usb hub
[64:20] and then i'm going to go back to the usb hub
[64:22] and then i'm going to go back to the usb hub
[64:24] and then i'm going to go back to the usb hub
[64:26] and then i'm going to go back to the usb hub
[64:28] and then i'm going to go back to the usb hub
[64:30] and then i'm going to go back to the usb hub
[64:32] and then i'm going to go back to the usb hub
[64:34] and then i'm going to go back to the usb hub
[64:36] and then i'm going to go back to the usb hub
[64:38] and then i'm going to go back to the usb hub
[64:40] and then i'm going to go back to the usb hub
[64:42] and then i'm going to go back to the usb hub
[64:44] and then i'm going to go back to the usb hub
[64:46] and then i'm going to go back to the usb hub
[64:48] and then i'm going to go back to the usb hub
[64:50] and then i'm going to go back to the usb hub
[64:52] and then i'm going to go back to the usb hub
[64:54] and then i'm going to go back to the usb hub
[64:56] and then i'm going to go back to the usb hub
[64:58] and then i'm going to go back to the usb hub
[65:00] and then i'm going to go back to the usb hub
[65:02] and then i'm going to go back to the usb hub
[65:04] and then i'm going to go back to the usb hub
[65:06] and then i'm going to go back to the usb hub
[65:08] and then i'm going to go back to the usb hub
[65:10] and then i'm going to go back to the usb hub
[65:12] and then i'm going to go back to the usb hub
[65:14] and then i'm going to go back to the usb hub
[65:16] and then i'm going to go back to the usb hub
[65:18] and then i'm going to go back to the usb hub
[65:20] and then i'm going to go back to the usb hub
[65:22] and then i'm going to go back to the usb hub
[65:24] and then i'm going to go back to the usb hub
[65:26] and then i'm going to go back to the usb hub
[65:28] and then i'm going to go back to the usb hub
[65:30] and then i'm going to go back to the usb hub
[65:32] and then i'm going to go back to the usb hub
[65:34] and then i'm going to go back to the usb hub
[65:36] and then i'm going to go back to the usb hub
[65:38] and then i'm going to go back to the usb hub
[65:40] and then i'm going to go back to the usb hub
[65:42] and then i'm going to go back to the usb hub
[65:44] and then i'm going to go back to the usb hub
[65:46] and then i'm going to go back to the usb hub
[65:48] and then i'm going to go back to the usb hub
[65:50] and then i'm going to go back to the usb hub
[65:52] and then i'm going to go back to the usb hub
[65:54] and then i'm going to go back to the usb hub
[65:56] and then i'm going to go back to the usb hub
[65:58] and then i'm going to go back to the usb hub
[66:00] and then i'm going to go back to the usb hub
[66:02] and then i'm going to go back to the usb hub
[66:04] and then i'm going to go back to the usb hub
[66:06] and then i'm going to go back to the usb hub
[66:08] and then i'm going to go back to the usb hub
[66:10] and then i'm going to go back to the usb hub
[66:12] and then i'm going to go back to the usb hub
[66:14] and then i'm going to go back to the usb hub
[66:16] and then i'm going to go back to the usb hub
[66:18] and then i'm going to go back to the usb hub
[66:20] and then i'm going to go back to the usb hub
[66:22] and then i'm going to go back to the usb hub
[66:24] and then i'm going to go back to the usb hub
[66:26] and then i'm going to go back to the usb hub
[66:28] and then i'm going to go back to the usb hub
[66:30] and then i'm going to go back to the usb hub
[66:32] and then i'm going to go back to the usb hub
[66:34] and then i'm going to go back to the usb hub
[66:36] and then i'm going to go back to the usb hub
[66:38] and then i'm going to go back to the usb hub
[66:40] and then i'm going to go back to the usb hub
[66:42] and then i'm going to go back to the usb hub
[66:44] and then i'm going to go back to the usb hub
[66:46] and then i'm going to go back to the usb hub
[66:48] and then i'm going to go back to the usb hub
[66:50] and then i'm going to go back to the usb hub
[66:52] and then i'm going to go back to the usb hub
[66:54] and then i'm going to go back to the usb hub
[66:56] and then i'm going to go back to the usb hub
[66:58] and then i'm going to go back to the usb hub
[67:00] and then i'm going to go back to the usb hub
[67:02] and then i'm going to go back to the usb hub
[67:04] and then i'm going to go back to the usb hub
[67:06] and then i'm going to go back to the usb hub
[67:08] and then i'm going to go back to the usb hub
[67:10] and then i'm going to go back to the usb hub
[67:12] and then i'm going to go back to the usb hub
[67:14] and then i'm going to go back to the usb hub
[67:16] and then i'm going to go back to the usb hub
[67:18] and then i'm going to go back to the usb hub
[67:20] and then i'm going to go back to the usb hub
[67:22] and then i'm going to go back to the usb hub
[67:24] and then i'm going to go back to the usb hub
[67:26] and then i'm going to go back to the usb hub
[67:28] and then i'm going to go back to the usb hub
[67:30] and then i'm going to go back to the usb hub
[67:32] and then i'm going to go back to the usb hub
[67:34] and then i'm going to go back to the usb hub
[67:36] and then i'm going to go back to the usb hub
[67:38] and then i'm going to go back to the usb hub
[67:40] and then i'm going to go back to the usb hub
[67:42] and then i'm going to go back to the usb hub
[67:44] and then i'm going to go back to the usb hub
[67:46] and then i'm going to go back to the usb hub
[67:48] and then i'm going to go back to the usb hub
[67:50] and then i'm going to go back to the usb hub
[67:52] and then i'm going to go back to the usb hub
[67:54] and then i'm going to go back to the usb hub
[67:56] and then i'm going to go back to the usb hub
[67:58] and then i'm going to go back to the usb hub
[68:00] and then i'm going to go back to the usb hub
[68:02] and then i'm going to go back to the usb hub
[68:04] and then i'm going to go back to the usb hub
[68:06] and then i'm going to go back to the usb hub
[68:08] and then i'm going to go back to the usb hub
[68:10] and then i'm going to go back to the usb hub
[68:12] and then i'm going to go back to the usb hub
[68:14] and then i'm going to go back to the usb hub
[68:16] and then i'm going to go back to the usb hub
[68:18] and then i'm going to go back to the usb hub
[68:20] and then i'm going to go back to the usb hub
[68:22] and then i'm going to go back to the usb hub
[68:24] and then i'm going to go back to the usb hub
[68:26] and then i'm going to go back to the usb hub
[68:28] and then i'm going to go back to the usb hub
[68:30] and then i'm going to go back to the usb hub
[68:32] and then i'm going to go back to the usb hub
[68:34] and then i'm going to go back to the usb hub
[68:36] and then i'm going to go back to the usb hub
[68:38] and then i'm going to go back to the usb hub
[68:40] and then i'm going to go back to the usb hub
[68:42] and then i'm going to go back to the usb hub
[68:44] and then i'm going to go back to the usb hub
[68:46] and then i'm going to go back to the usb hub
[68:48] and then i'm going to go back to the usb hub
[68:50] and then i'm going to go back to the usb hub
[68:52] and then i'm going to go back to the usb hub
[68:54] and then i'm going to go back to the usb hub
[68:56] and then i'm going to go back to the usb hub
[68:58] and then i'm going to go back to the usb hub
[69:00] and then i'm going to go back to the usb hub
[69:02] and then i'm going to go back to the usb hub
[69:04] and then i'm going to go back to the usb hub
[69:06] and then i'm going to go back to the usb hub
[69:08] and then i'm going to go back to the usb hub
[69:10] and then i'm going to go back to the usb hub
[69:12] and then i'm going to go back to the usb hub
[69:14] and then i'm going to go back to the usb hub
[69:16] and then i'm going to go back to the usb hub
[69:18] and then i'm going to go back to the usb hub
[69:20] and then i'm going to go back to the usb hub
[69:22] and then i'm going to go back to the usb hub
[69:24] and then i'm going to go back to the usb hub
[69:26] and then i'm going to go back to the usb hub
[69:28] and then i'm going to go back to the usb hub
[69:30] and then i'm going to go back to the usb hub
[69:32] and then i'm going to go back to the usb hub
[69:34] and then i'm going to go back to the usb hub
[69:36] and then i'm going to go back to the usb hub
[69:38] and then i'm going to go back to the usb hub
[69:40] and then i'm going to go back to the usb hub
[69:42] and then i'm going to go back to the usb hub
[69:44] and then i'm going to go back to the usb hub
[69:46] and then i'm going to go back to the usb hub
[69:48] and then i'm going to go back to the usb hub
[69:50] and then i'm going to go back to the usb hub
[69:52] and then i'm going to go back to the usb hub
[69:54] and then i'm going to go back to the usb hub
[69:56] and then i'm going to go back to the usb hub
[69:58] and then i'm going to go back to the usb hub
[70:00] and then i'm going to go back to the usb hub
[70:02] and then i'm going to go back to the usb hub
[70:04] and then i'm going to go back to the usb hub
[70:06] and then i'm going to go back to the usb hub
[70:08] and then i'm going to go back to the usb hub
[70:10] and then i'm going to go back to the usb hub
[70:12] and then i'm going to go back to the usb hub
[70:14] and then i'm going to go back to the usb hub
[70:16] and then i'm going to go back to the usb hub
[70:18] and then i'm going to go back to the usb hub
[70:20] and then i'm going to go back to the usb hub
[70:22] and then i'm going to go back to the usb hub
[70:24] and then i'm going to go back to the usb hub
[70:26] and then i'm going to go back to the usb hub
[70:28] and then i'm going to go back to the usb hub
[70:30] and then i'm going to go back to the usb hub
[70:32] and then i'm going to go back to the usb hub
[70:34] and then i'm going to go back to the usb hub
[70:36] and then i'm going to go back to the usb hub
[70:38] and then i'm going to go back to the usb hub
[70:40] and then i'm going to go back to the usb hub
[70:42] and then i'm going to go back to the usb hub
[70:44] and then i'm going to go back to the usb hub
[70:46] and then i'm going to go back to the usb hub
[70:48] and then i'm going to go back to the usb hub
[70:50] and then i'm going to go back to the usb hub
[70:52] and then i'm going to go back to the usb hub
[70:54] and then i'm going to go back to the usb hub
[70:56] and then i'm going to go back to the usb hub
[70:58] and then i'm going to go back to the usb hub
[71:00] and then i'm going to go back to the usb hub
[71:02] and then i'm going to go back to the usb hub
[71:04] and then i'm going to go back to the usb hub
[71:06] and then i'm going to go back to the usb hub
[71:08] and then i'm going to go back to the usb hub
[71:10] and then i'm going to go back to the usb hub
[71:12] and then i'm going to go back to the usb hub
[71:14] and then i'm going to go back to the usb hub
[71:16] and then i'm going to go back to the usb hub
[71:18] and then i'm going to go back to the usb hub
[71:20] and then i'm going to go back to the usb hub
[71:22] and then i'm going to go back to the usb hub
[71:24] and then i'm going to go back to the usb hub
[71:26] and then i'm going to go back to the usb hub
[71:28] and then i'm going to go back to the usb hub
[71:30] and then i'm going to go back to the usb hub
[71:32] and then i'm going to go back to the usb hub
[71:34] and then i'm going to go back to the usb hub
[71:36] and then i'm going to go back to the usb hub
[71:38] and then i'm going to go back to the usb hub
[71:40] and then i'm going to go back to the usb hub
[71:42] and then i'm going to go back to the usb hub
[71:44] and then i'm going to go back to the usb hub
[71:46] and then i'm going to go back to the usb hub
[71:48] and then i'm going to go back to the usb hub
[71:50] and then i'm going to go back to the usb hub
[71:52] and then i'm going to go back to the usb hub
[71:54] and then i'm going to go back to the usb hub
[71:56] and then i'm going to go back to the usb hub
[71:58] and then i'm going to go back to the usb hub
[72:00] and then i'm going to go back to the usb hub
[72:02] and then i'm going to go back to the usb hub
[72:04] and then i'm going to go back to the usb hub
[72:06] and then i'm going to go back to the usb hub
[72:08] and then i'm going to go back to the usb hub
[72:10] and then i'm going to go back to the usb hub
[72:12] and then i'm going to go back to the usb hub
[72:14] and then i'm going to go back to the usb hub
[72:16] and then i'm going to go back to the usb hub
[72:18] and then i'm going to go back to the usb hub
[72:20] and then i'm going to go back to the usb hub
[72:22] and then i'm going to go back to the usb hub
[72:24] and then i'm going to go back to the usb hub
[72:26] and then i'm going to go back to the usb hub
[72:28] and then i'm going to go back to the usb hub
[72:30] and then i'm going to go back to the usb hub
[72:32] and then i'm going to go back to the usb hub
[72:34] and then i'm going to go back to the usb hub
[72:36] and then i'm going to go back to the usb hub
[72:38] and then i'm going to go back to the usb hub
[72:40] and then i'm going to go back to the usb hub
[72:42] and then i'm going to go back to the usb hub
[72:44] and then i'm going to go back to the usb hub
[72:46] and then i'm going to go back to the usb hub
[72:48] and then i'm going to go back to the usb hub
[72:50] and then i'm going to go back to the usb hub
[72:52] and then i'm going to go back to the usb hub
[72:54] and then i'm going to go back to the usb hub
[72:56] and then i'm going to go back to the usb hub
[72:58] and then i'm going to go back to the usb hub
[73:00] and then i'm going to go back to the usb hub
[73:02] and then i'm going to go back to the usb hub
[73:04] and then i'm going to go back to the usb hub
[73:06] and then i'm going to go back to the usb hub
[73:08] and then i'm going to go back to the usb hub
[73:10] and then i'm going to go back to the usb hub
[73:12] and then i'm going to go back to the usb hub
[73:14] and then i'm going to go back to the usb hub
[73:16] and then i'm going to go back to the usb hub
[73:18] and then i'm going to go back to the usb hub
[73:20] and then i'm going to go back to the usb hub
[73:22] and then i'm going to go back to the usb hub
[73:24] and then i'm going to go back to the usb hub
[73:26] and then i'm going to go back to the usb hub
[73:28] and then i'm going to go back to the usb hub
[73:30] and then i'm going to go back to the usb hub
[73:32] and then i'm going to go back to the usb hub
[73:34] and then i'm going to go back to the usb hub
[73:36] and then i'm going to go back to the usb hub
[73:38] and then i'm going to go back to the usb hub
[73:40] and then i'm going to go back to the usb hub
[73:42] and then i'm going to go back to the usb hub
[73:44] and then i'm going to go back to the usb hub
[73:46] and then i'm going to go back to the usb hub
[73:48] and then i'm going to go back to the usb hub
[73:50] and then i'm going to go back to the usb hub
[73:52] and then i'm going to go back to the usb hub
[73:54] and then i'm going to go back to the usb hub
[73:56] and then i'm going to go back to the usb hub
[73:58] and then i'm going to go back to the usb hub
[74:00] and then i'm going to go back to the usb hub
[74:02] and then i'm going to go back to the usb hub
[74:04] and then i'm going to go back to the usb hub
[74:06] and then i'm going to go back to the usb hub
[74:08] and then i'm going to go back to the usb hub
[74:10] and then i'm going to go back to the usb hub
[74:12] and then i'm going to go back to the usb hub
[74:14] and then i'm going to go back to the usb hub
[74:16] and then i'm going to go back to the usb hub
[74:18] and then i'm going to go back to the usb hub
[74:20] and then i'm going to go back to the usb hub
[74:22] and then i'm going to go back to the usb hub
[74:24] and then i'm going to go back to the usb hub
[74:26] and then i'm going to go back to the usb hub
[74:28] and then i'm going to go back to the usb hub
[74:30] and then i'm going to go back to the usb hub
[74:32] and then i'm going to go back to the usb hub
[74:34] and then i'm going to go back to the usb hub
[74:36] and then i'm going to go back to the usb hub
[74:38] and then i'm going to go back to the usb hub
[74:40] and then i'm going to go back to the usb hub
[74:42] and then i'm going to go back to the usb hub
[74:44] and then i'm going to go back to the usb hub
[74:46] and then i'm going to go back to the usb hub
[74:48] and then i'm going to go back to the usb hub
[74:50] and then i'm going to go back to the usb hub
[74:52] and then i'm going to go back to the usb hub
[74:54] and then i'm going to go back to the usb hub
[74:56] and then i'm going to go back to the usb hub
[74:58] and then i'm going to go back to the usb hub
[75:00] and then i'm going to go back to the usb hub
[75:02] and then i'm going to go back to the usb hub
[75:04] and then i'm going to go back to the usb hub
[75:06] and then i'm going to go back to the usb hub
[75:08] and then i'm going to go back to the usb hub
[75:10] and then i'm going to go back to the usb hub
[75:12] and then i'm going to go back to the usb hub
[75:14] and then i'm going to go back to the usb hub
[75:16] and then i'm going to go back to the usb hub
[75:18] and then i'm going to go back to the usb hub
[75:20] and then i'm going to go back to the usb hub
[75:22] and then i'm going to go back to the usb hub
[75:24] and then i'm going to go back to the usb hub
[75:26] and then i'm going to go back to the usb hub
[75:28] and then i'm going to go back to the usb hub
[75:30] and then i'm going to go back to the usb hub
[75:32] and then i'm going to go back to the usb hub
[75:34] and then i'm going to go back to the usb hub
[75:36] and then i'm going to go back to the usb hub
[75:38] and then i'm going to go back to the usb hub
[75:40] and then i'm going to go back to the usb hub
[75:42] and then i'm going to go back to the usb hub
[75:44] and then i'm going to go back to the usb hub
[75:46] and then i'm going to go back to the usb hub
[75:48] and then i'm going to go back to the usb hub
[75:50] and then i'm going to go back to the usb hub
[75:52] and then i'm going to go back to the usb hub
[75:54] and then i'm going to go back to the usb hub
[75:56] and then i'm going to go back to the usb hub
[75:58] and then i'm going to go back to the usb hub
[76:00] and then i'm going to go back to the usb hub
[76:02] and then i'm going to go back to the usb hub
[76:04] and then i'm going to go back to the usb hub
[76:06] and then i'm going to go back to the usb hub
[76:08] and then i'm going to go back to the usb hub
[76:10] and then i'm going to go back to the usb hub
[76:12] and then i'm going to go back to the usb hub
[76:14] and then i'm going to go back to the usb hub
[76:16] and then i'm going to go back to the usb hub
[76:18] and then i'm going to go back to the usb hub
[76:20] and then i'm going to go back to the usb hub
[76:22] and then i'm going to go back to the usb hub
[76:24] and then i'm going to go back to the usb hub
[76:26] and then i'm going to go back to the usb hub
[76:28] and then i'm going to go back to the usb hub
[76:30] and then i'm going to go back to the usb hub
[76:32] and then i'm going to go back to the usb hub
[76:34] and then i'm going to go back to the usb hub
[76:36] and then i'm going to go back to the usb hub
[76:38] and then i'm going to go back to the usb hub
[76:40] and then i'm going to go back to the usb hub
[76:42] and then i'm going to go back to the usb hub
[76:44] and then i'm going to go back to the usb hub
[76:46] and then i'm going to go back to the usb hub
[76:48] and then i'm going to go back to the usb hub
[76:50] and then i'm going to go back to the usb hub
[76:52] and then i'm going to go back to the usb hub
[76:54] and then i'm going to go back to the usb hub
[76:56] and then i'm going to go back to the usb hub
[76:58] and then i'm going to go back to the usb hub
[77:00] and then i'm going to go back to the usb hub
[77:02] and then i'm going to go back to the usb hub
[77:04] and then i'm going to go back to the usb hub
[77:06] and then i'm going to go back to the usb hub
[77:08] and then i'm going to go back to the usb hub
[77:10] and then i'm going to go back to the usb hub
[77:12] and then i'm going to go back to the usb hub
[77:14] and then i'm going to go back to the usb hub
[77:16] and then i'm going to go back to the usb hub
[77:18] and then i'm going to go back to the usb hub
[77:20] and then i'm going to go back to the usb hub
[77:22] and then i'm going to go back to the usb hub
[77:24] and then i'm going to go back to the usb hub
[77:26] and then i'm going to go back to the usb hub
[77:28] and then i'm going to go back to the usb hub
[77:30] and then i'm going to go back to the usb hub
[77:32] and then i'm going to go back to the usb hub
[77:34] and then i'm going to go back to the usb hub
[77:36] and then i'm going to go back to the usb hub
[77:38] and then i'm going to go back to the usb hub
[77:40] and then i'm going to go back to the usb hub
[77:42] and then i'm going to go back to the usb hub
[77:44] and then i'm going to go back to the usb hub
[77:46] and then i'm going to go back to the usb hub
[77:48] and then i'm going to go back to the usb hub
[77:50] and then i'm going to go back to the usb hub
[77:52] and then i'm going to go back to the usb hub
[77:54] and then i'm going to go back to the usb hub
[77:56] and then i'm going to go back to the usb hub
[77:58] and then i'm going to go back to the usb hub
[78:00] and then i'm going to go back to the usb hub
[78:02] and then i'm going to go back to the usb hub
[78:04] and then i'm going to go back to the usb hub
[78:06] and then i'm going to go back to the usb hub
[78:08] and then i'm going to go back to the usb hub
[78:10] and then i'm going to go back to the usb hub
[78:12] and then i'm going to go back to the usb hub
[78:14] and then i'm going to go back to the usb hub
[78:16] and then i'm going to go back to the usb hub
[78:18] and then i'm going to go back to the usb hub
[78:20] and then i'm going to go back to the usb hub
[78:22] and then i'm going to go back to the usb hub
[78:24] and then i'm going to go back to the usb hub
[78:26] and then i'm going to go back to the usb hub
[78:28] and then i'm going to go back to the usb hub
[78:30] and then i'm going to go back to the usb hub
[78:32] and then i'm going to go back to the usb hub
[78:34] and then i'm going to go back to the usb hub
[78:36] and then i'm going to go back to the usb hub
[78:38] and then i'm going to go back to the usb hub
[78:40] and then i'm going to go back to the usb hub
[78:42] and then i'm going to go back to the usb hub
[78:44] and then i'm going to go back to the usb hub
[78:46] and then i'm going to go back to the usb hub
[78:48] and then i'm going to go back to the usb hub
[78:50] and then i'm going to go back to the usb hub
[78:52] and then i'm going to go back to the usb hub
[78:54] and then i'm going to go back to the usb hub
[78:56] and then i'm going to go back to the usb hub
[78:58] and then i'm going to go back to the usb hub
[79:00] and then i'm going to go back to the usb hub
[79:02] and then i'm going to go back to the usb hub
[79:04] and then i'm going to go back to the usb hub
[79:06] and then i'm going to go back to the usb hub
[79:08] and then i'm going to go back to the usb hub
[79:10] and then i'm going to go back to the usb hub
[79:12] and then i'm going to go back to the usb hub
[79:14] and then i'm going to go back to the usb hub
[79:16] and then i'm going to go back to the usb hub
[79:18] and then i'm going to go back to the usb hub
[79:20] and then i'm going to go back to the usb hub
[79:22] and then i'm going to go back to the usb hub
[79:24] and then i'm going to go back to the usb hub
[79:26] and then i'm going to go back to the usb hub
[79:28] and then i'm going to go back to the usb hub
[79:30] and then i'm going to go back to the usb hub
[79:32] and then i'm going to go back to the usb hub
[79:34] and then i'm going to go back to the usb hub
[79:36] and then i'm going to go back to the usb hub
[79:38] and then i'm going to go back to the usb hub
[79:40] and then i'm going to go back to the usb hub
[79:42] and then i'm going to go back to the usb hub
[79:44] and then i'm going to go back to the usb hub
[79:46] and then i'm going to go back to the usb hub
[79:48] and then i'm going to go back to the usb hub
[79:50] and then i'm going to go back to the usb hub
[79:52] and then i'm going to go back to the usb hub
[79:54] and then i'm going to go back to the usb hub
[79:56] and then i'm going to go back to the usb hub
[79:58] and then i'm going to go back to the usb hub
[80:00] and then i'm going to go back to the usb hub
[80:02] and then i'm going to go back to the usb hub
[80:04] and then i'm going to go back to the usb hub
[80:06] and then i'm going to go back to the usb hub
[80:08] and then i'm going to go back to the usb hub
[80:10] and then i'm going to go back to the usb hub
[80:12] and then i'm going to go back to the usb hub
[80:14] and then i'm going to go back to the usb hub
[80:16] and then i'm going to go back to the usb hub
[80:18] and then i'm going to go back to the usb hub
[80:20] and then i'm going to go back to the usb hub
[80:22] and then i'm going to go back to the usb hub
[80:24] and then i'm going to go back to the usb hub
[80:26] and then i'm going to go back to the usb hub
[80:28] and then i'm going to go back to the usb hub
[80:30] and then i'm going to go back to the usb hub
[80:32] and then i'm going to go back to the usb hub
[80:34] and then i'm going to go back to the usb hub
[80:36] and then i'm going to go back to the usb hub
[80:38] and then i'm going to go back to the usb hub
[80:40] and then i'm going to go back to the usb hub
[80:42] and then i'm going to go back to the usb hub
[80:44] and then i'm going to go back to the usb hub
[80:46] and then i'm going to go back to the usb hub
[80:48] and then i'm going to go back to the usb hub
[80:50] and then i'm going to go back to the usb hub
[80:52] and then i'm going to go back to the usb hub
[80:54] and then i'm going to go back to the usb hub
[80:56] and then i'm going to go back to the usb hub
[80:58] and then i'm going to go back to the usb hub
[81:00] and then i'm going to go back to the usb hub
[81:02] and then i'm going to go back to the usb hub
[81:04] and then i'm going to go back to the usb hub
[81:06] and then i'm going to go back to the usb hub
[81:08] and then i'm going to go back to the usb hub
[81:10] and then i'm going to go back to the usb hub
[81:12] and then i'm going to go back to the usb hub
[81:14] and then i'm going to go back to the usb hub
[81:16] and then i'm going to go back to the usb hub
[81:18] and then i'm going to go back to the usb hub
[81:20] and then i'm going to go back to the usb hub
[81:22] and then i'm going to go back to the usb hub
[81:24] and then i'm going to go back to the usb hub
[81:26] and then i'm going to go back to the usb hub
[81:28] and then i'm going to go back to the usb hub
[81:30] and then i'm going to go back to the usb hub
[81:32] and then i'm going to go back to the usb hub
[81:34] and then i'm going to go back to the usb hub
[81:36] and then i'm going to go back to the usb hub
[81:38] and then i'm going to go back to the usb hub
[81:40] and then i'm going to go back to the usb hub
[81:42] and then i'm going to go back to the usb hub
[81:44] and then i'm going to go back to the usb hub
[81:46] and then i'm going to go back to the usb hub
[81:48] and then i'm going to go back to the usb hub
[81:50] and then i'm going to go back to the usb hub
[81:52] and then i'm going to go back to the usb hub
[81:54] and then i'm going to go back to the usb hub
[81:56] and then i'm going to go back to the usb hub
[81:58] and then i'm going to go back to the usb hub
[82:00] and then i'm going to go back to the usb hub
[82:02] and then i'm going to go back to the usb hub
[82:04] and then i'm going to go back to the usb hub
[82:06] and then i'm going to go back to the usb hub
[82:08] and then i'm going to go back to the usb hub
[82:10] and then i'm going to go back to the usb hub
[82:12] and then i'm going to go back to the usb hub
[82:14] and then i'm going to go back to the usb hub
[82:16] and then i'm going to go back to the usb hub
[82:18] and then i'm going to go back to the usb hub
[82:20] and then i'm going to go back to the usb hub
[82:22] and then i'm going to go back to the usb hub
[82:24] and then i'm going to go back to the usb hub
[82:26] and then i'm going to go back to the usb hub
[82:28] and then i'm going to go back to the usb hub
[82:30] and then i'm going to go back to the usb hub
[82:32] and then i'm going to go back to the usb hub
[82:34] and then i'm going to go back to the usb hub
[82:36] and then i'm going to go back to the usb hub
[82:38] and then i'm going to go back to the usb hub
[82:40] and then i'm going to go back to the usb hub
[82:42] and then i'm going to go back to the usb hub
[82:44] and then i'm going to go back to the usb hub
[82:46] and then i'm going to go back to the usb hub
[82:48] and then i'm going to go back to the usb hub
[82:50] and then i'm going to go back to the usb hub
[82:52] and then i'm going to go back to the usb hub
[82:54] and then i'm going to go back to the usb hub
[82:56] and then i'm going to go back to the usb hub
[82:58] and then i'm going to go back to the usb hub
[83:00] and then i'm going to go back to the usb hub
[83:02] and then i'm going to go back to the usb hub
[83:04] and then i'm going to go back to the usb hub
[83:06] and then i'm going to go back to the usb hub
[83:08] and then i'm going to go back to the usb hub
[83:10] and then i'm going to go back to the usb hub
[83:12] and then i'm going to go back to the usb hub
[83:14] and then i'm going to go back to the usb hub
[83:16] and then i'm going to go back to the usb hub
[83:18] and then i'm going to go back to the usb hub
[83:20] and then i'm going to go back to the usb hub
[83:22] and then i'm going to go back to the usb hub
[83:24] and then i'm going to go back to the usb hub
[83:26] and then i'm going to go back to the usb hub
[83:28] and then i'm going to go back to the usb hub
[83:30] and then i'm going to go back to the usb hub
[83:32] and then i'm going to go back to the usb hub
[83:34] and then i'm going to go back to the usb hub
[83:36] and then i'm going to go back to the usb hub
[83:38] and then i'm going to go back to the usb hub
[83:40] and then i'm going to go back to the usb hub
[83:42] and then i'm going to go back to the usb hub
[83:44] and then i'm going to go back to the usb hub
[83:46] and then i'm going to go back to the usb hub
[83:48] and then i'm going to go back to the usb hub
[83:50] and then i'm going to go back to the usb hub
[83:52] and then i'm going to go back to the usb hub
[83:54] and then i'm going to go back to the usb hub
[83:56] and then i'm going to go back to the usb hub
[83:58] and then i'm going to go back to the usb hub
[84:00] and then i'm going to go back to the usb hub
[84:02] and then i'm going to go back to the usb hub
[84:04] and then i'm going to go back to the usb hub
[84:06] and then i'm going to go back to the usb hub
[84:08] and then i'm going to go back to the usb hub
[84:10] and then i'm going to go back to the usb hub
[84:12] and then i'm going to go back to the usb hub
[84:14] and then i'm going to go back to the usb hub
[84:16] and then i'm going to go back to the usb hub
[84:18] and then i'm going to go back to the usb hub
[84:20] and then i'm going to go back to the usb hub
[84:22] and then i'm going to go back to the usb hub
[84:24] and then i'm going to go back to the usb hub
[84:26] and then i'm going to go back to the usb hub
[84:28] and then i'm going to go back to the usb hub
[84:30] and then i'm going to go back to the usb hub
[84:32] and then i'm going to go back to the usb hub
[84:34] and then i'm going to go back to the usb hub
[84:36] and then i'm going to go back to the usb hub
[84:38] and then i'm going to go back to the usb hub
[84:40] and then i'm going to go back to the usb hub
[84:42] and then i'm going to go back to the usb hub
[84:44] and then i'm going to go back to the usb hub
[84:46] and then i'm going to go back to the usb hub
[84:48] and then i'm going to go back to the usb hub
[84:50] and then i'm going to go back to the usb hub
[84:52] and then i'm going to go back to the usb hub
[84:54] and then i'm going to go back to the usb hub
[84:56] and then i'm going to go back to the usb hub
[84:58] and then i'm going to go back to the usb hub
[85:00] and then i'm going to go back to the usb hub
[85:02] and then i'm going to go back to the usb hub
[85:04] and then i'm going to go back to the usb hub
[85:06] and then i'm going to go back to the usb hub
[85:08] and then i'm going to go back to the usb hub
[85:10] and then i'm going to go back to the usb hub
[85:12] and then i'm going to go back to the usb hub
[85:14] and then i'm going to go back to the usb hub
[85:16] and then i'm going to go back to the usb hub
[85:18] and then i'm going to go back to the usb hub
[85:20] and then i'm going to go back to the usb hub
[85:22] and then i'm going to go back to the usb hub
[85:24] and then i'm going to go back to the usb hub
[85:26] and then i'm going to go back to the usb hub
[85:28] and then i'm going to go back to the usb hub
[85:30] and then i'm going to go back to the usb hub
[85:32] and then i'm going to go back to the usb hub
[85:34] and then i'm going to go back to the usb hub
[85:36] and then i'm going to go back to the usb hub
[85:38] and then i'm going to go back to the usb hub
[85:40] and then i'm going to go back to the usb hub
[85:42] and then i'm going to go back to the usb hub
[85:44] and then i'm going to go back to the usb hub
[85:46] and then i'm going to go back to the usb hub
[85:48] and then i'm going to go back to the usb hub
[85:50] and then i'm going to go back to the usb hub
[85:52] and then i'm going to go back to the usb hub
[85:54] and then i'm going to go back to the usb hub
[85:56] and then i'm going to go back to the usb hub
[85:58] and then i'm going to go back to the usb hub
[86:00] and then i'm going to go back to the usb hub
[86:02] and then i'm going to go back to the usb hub
[86:04] and then i'm going to go back to the usb hub
[86:06] and then i'm going to go back to the usb hub
[86:08] and then i'm going to go back to the usb hub
[86:10] and then i'm going to go back to the usb hub
[86:12] and then i'm going to go back to the usb hub
[86:14] and then i'm going to go back to the usb hub
[86:16] and then i'm going to go back to the usb hub
[86:18] and then i'm going to go back to the usb hub
[86:20] and then i'm going to go back to the usb hub
[86:22] and then i'm going to go back to the usb hub
[86:24] and then i'm going to go back to the usb hub
[86:26] and then i'm going to go back to the usb hub
[86:28] and then i'm going to go back to the usb hub
[86:30] and then i'm going to go back to the usb hub
[86:32] and then i'm going to go back to the usb hub
[86:34] and then i'm going to go back to the usb hub
[86:36] and then i'm going to go back to the usb hub
[86:38] and then i'm going to go back to the usb hub
[86:40] and then i'm going to go back to the usb hub
[86:42] and then i'm going to go back to the usb hub
[86:44] and then i'm going to go back to the usb hub
[86:46] and then i'm going to go back to the usb hub
[86:48] and then i'm going to go back to the usb hub
[86:50] and then i'm going to go back to the usb hub
[86:52] and then i'm going to go back to the usb hub
[86:54] and then i'm going to go back to the usb hub
[86:56] and then i'm going to go back to the usb hub
[86:58] and then i'm going to go back to the usb hub
[87:00] and then i'm going to go back to the usb hub
[87:02] and then i'm going to go back to the usb hub
[87:04] and then i'm going to go back to the usb hub
[87:06] and then i'm going to go back to the usb hub
[87:08] and then i'm going to go back to the usb hub
[87:10] and then i'm going to go back to the usb hub
[87:12] and then i'm going to go back to the usb hub
[87:14] and then i'm going to go back to the usb hub
[87:16] and then i'm going to go back to the usb hub
[87:18] and then i'm going to go back to the usb hub
[87:20] and then i'm going to go back to the usb hub
[87:22] and then i'm going to go back to the usb hub
[87:24] and then i'm going to go back to the usb hub
[87:26] and then i'm going to go back to the usb hub
[87:28] and then i'm going to go back to the usb hub
[87:30] and then i'm going to go back to the usb hub
[87:32] and then i'm going to go back to the usb hub
[87:34] and then i'm going to go back to the usb hub
[87:36] and then i'm going to go back to the usb hub
[87:38] and then i'm going to go back to the usb hub
[87:40] and then i'm going to go back to the usb hub
[87:42] and then i'm going to go back to the usb hub
[87:44] and then i'm going to go back to the usb hub
[87:46] and then i'm going to go back to the usb hub
[87:48] and then i'm going to go back to the usb hub
[87:50] and then i'm going to go back to the usb hub
[87:52] and then i'm going to go back to the usb hub
[87:54] and then i'm going to go back to the usb hub
[87:56] and then i'm going to go back to the usb hub
[87:58] and then i'm going to go back to the usb hub
[88:00] and then i'm going to go back to the usb hub
[88:02] and then i'm going to go back to the usb hub
[88:04] and then i'm going to go back to the usb hub
[88:06] and then i'm going to go back to the usb hub
[88:08] and then i'm going to go back to the usb hub
[88:10] and then i'm going to go back to the usb hub
[88:12] and then i'm going to go back to the usb hub
[88:14] and then i'm going to go back to the usb hub
[88:16] and then i'm going to go back to the usb hub
[88:18] and then i'm going to go back to the usb hub
[88:20] and then i'm going to go back to the usb hub
[88:22] and then i'm going to go back to the usb hub
[88:24] and then i'm going to go back to the usb hub
[88:26] and then i'm going to go back to the usb hub
[88:28] and then i'm going to go back to the usb hub
[88:30] and then i'm going to go back to the usb hub
[88:32] and then i'm going to go back to the usb hub
[88:34] and then i'm going to go back to the usb hub
[88:36] and then i'm going to go back to the usb hub
[88:38] and then i'm going to go back to the usb hub
[88:40] and then i'm going to go back to the usb hub
[88:42] and then i'm going to go back to the usb hub
[88:44] and then i'm going to go back to the usb hub
[88:46] and then i'm going to go back to the usb hub
[88:48] and then i'm going to go back to the usb hub
[88:50] and then i'm going to go back to the usb hub
[88:52] and then i'm going to go back to the usb hub
[88:54] and then i'm going to go back to the usb hub
[88:56] and then i'm going to go back to the usb hub
[88:58] and then i'm going to go back to the usb hub
[89:00] and then i'm going to go back to the usb hub
[89:02] and then i'm going to go back to the usb hub
[89:04] and then i'm going to go back to the usb hub
[89:06] and then i'm going to go back to the usb hub
[89:08] and then i'm going to go back to the usb hub
[89:10] and then i'm going to go back to the usb hub
[89:12] and then i'm going to go back to the usb hub
[89:14] and then i'm going to go back to the usb hub
[89:16] and then i'm going to go back to the usb hub
[89:18] and then i'm going to go back to the usb hub
[89:20] and then i'm going to go back to the usb hub
[89:22] and then i'm going to go back to the usb hub
[89:24] and then i'm going to go back to the usb hub
[89:26] and then i'm going to go back to the usb hub
[89:28] and then i'm going to go back to the usb hub
[89:30] and then i'm going to go back to the usb hub
[89:32] and then i'm going to go back to the usb hub
[89:34] and then i'm going to go back to the usb hub
[89:36] and then i'm going to go back to the usb hub
[89:38] and then i'm going to go back to the usb hub
[89:40] and then i'm going to go back to the usb hub
[89:42] and then i'm going to go back to the usb hub
[89:44] and then i'm going to go back to the usb hub
[89:46] and then i'm going to go back to the usb hub
[89:48] and then i'm going to go back to the usb hub
[89:50] and then i'm going to go back to the usb hub
[89:52] and then i'm going to go back to the usb hub
[89:54] and then i'm going to go back to the usb hub
[89:56] and then i'm going to go back to the usb hub
[89:58] and then i'm going to go back to the usb hub
[90:00] and then i'm going to go back to the usb hub
[90:02] and then i'm going to go back to the usb hub
[90:04] and then i'm going to go back to the usb hub
[90:06] and then i'm going to go back to the usb hub
[90:08] and then i'm going to go back to the usb hub
[90:10] and then i'm going to go back to the usb hub
[90:12] and then i'm going to go back to the usb hub
[90:14] and then i'm going to go back to the usb hub
[90:16] and then i'm going to go back to the usb hub
[90:18] and then i'm going to go back to the usb hub
[90:20] and then i'm going to go back to the usb hub
[90:22] and then i'm going to go back to the usb hub
[90:24] and then i'm going to go back to the usb hub
[90:26] and then i'm going to go back to the usb hub
[90:28] and then i'm going to go back to the usb hub
[90:30] and then i'm going to go back to the usb hub
[90:32] and then i'm going to go back to the usb hub
[90:34] and then i'm going to go back to the usb hub
[90:36] and then i'm going to go back to the usb hub
[90:38] and then i'm going to go back to the usb hub
[90:40] and then i'm going to go back to the usb hub
[90:42] and then i'm going to go back to the usb hub
[90:44] and then i'm going to go back to the usb hub
[90:46] and then i'm going to go back to the usb hub
[90:48] and then i'm going to go back to the usb hub
[90:50] and then i'm going to go back to the usb hub
[90:52] and then i'm going to go back to the usb hub
[90:54] and then i'm going to go back to the usb hub
[90:56] and then i'm going to go back to the usb hub
[90:58] and then i'm going to go back to the usb hub
[91:00] and then i'm going to go back to the usb hub
[91:02] and then i'm going to go back to the usb hub
[91:04] and then i'm going to go back to the usb hub
[91:06] and then i'm going to go back to the usb hub
[91:08] and then i'm going to go back to the usb hub
[91:10] and then i'm going to go back to the usb hub
[91:12] and then i'm going to go back to the usb hub
[91:14] and then i'm going to go back to the usb hub
[91:16] and then i'm going to go back to the usb hub
[91:18] and then i'm going to go back to the usb hub
[91:20] and then i'm going to go back to the usb hub
[91:22] and then i'm going to go back to the usb hub
[91:24] and then i'm going to go back to the usb hub
[91:26] and then i'm going to go back to the usb hub
[91:28] and then i'm going to go back to the usb hub
[91:30] and then i'm going to go back to the usb hub
[91:32] and then i'm going to go back to the usb hub
[91:34] and then i'm going to go back to the usb hub
[91:36] and then i'm going to go back to the usb hub
[91:38] and then i'm going to go back to the usb hub
[91:40] and then i'm going to go back to the usb hub
[91:42] and then i'm going to go back to the usb hub
[91:44] and then i'm going to go back to the usb hub
[91:46] and then i'm going to go back to the usb hub
[91:48] and then i'm going to go back to the usb hub
[91:50] and then i'm going to go back to the usb hub
[91:52] and then i'm going to go back to the usb hub
[91:54] and then i'm going to go back to the usb hub
[91:56] and then i'm going to go back to the usb hub
[91:58] and then i'm going to go back to the usb hub
[92:00] and then i'm going to go back to the usb hub
[92:02] and then i'm going to go back to the usb hub
[92:04] and then i'm going to go back to the usb hub
[92:06] and then i'm going to go back to the usb hub
[92:08] and then i'm going to go back to the usb hub
[92:10] and then i'm going to go back to the usb hub
[92:12] and then i'm going to go back to the usb hub
[92:14] and then i'm going to go back to the usb hub
[92:16] and then i'm going to go back to the usb hub
[92:18] and then i'm going to go back to the usb hub
[92:20] and then i'm going to go back to the usb hub
[92:22] and then i'm going to go back to the usb hub
[92:24] and then i'm going to go back to the usb hub
[92:26] and then i'm going to go back to the usb hub
[92:28] and then i'm going to go back to the usb hub
[92:30] and then i'm going to go back to the usb hub
[92:32] and then i'm going to go back to the usb hub
[92:34] and then i'm going to go back to the usb hub
[92:36] and then i'm going to go back to the usb hub
[92:38] and then i'm going to go back to the usb hub
[92:40] and then i'm going to go back to the usb hub
[92:42] and then i'm going to go back to the usb hub
[92:44] and then i'm going to go back to the usb hub
[92:46] and then i'm going to go back to the usb hub
[92:48] and then i'm going to go back to the usb hub
[92:50] and then i'm going to go back to the usb hub
[92:52] and then i'm going to go back to the usb hub
[92:54] and then i'm going to go back to the usb hub
[92:56] and then i'm going to go back to the usb hub
[92:58] and then i'm going to go back to the usb hub
[93:00] and then i'm going to go back to the usb hub
[93:02] and then i'm going to go back to the usb hub
[93:04] and then i'm going to go back to the usb hub
[93:06] and then i'm going to go back to the usb hub
[93:08] and then i'm going to go back to the usb hub
[93:10] and then i'm going to go back to the usb hub
[93:12] and then i'm going to go back to the usb hub
[93:14] and then i'm going to go back to the usb hub
[93:16] and then i'm going to go back to the usb hub
[93:18] and then i'm going to go back to the usb hub
[93:20] and then i'm going to go back to the usb hub
[93:22] and then i'm going to go back to the usb hub
[93:24] and then i'm going to go back to the usb hub
[93:26] and then i'm going to go back to the usb hub
[93:28] and then i'm going to go back to the usb hub
[93:30] and then i'm going to go back to the usb hub
[93:32] and then i'm going to go back to the usb hub
[93:34] and then i'm going to go back to the usb hub
[93:36] and then i'm going to go back to the usb hub
[93:38] and then i'm going to go back to the usb hub
[93:40] and then i'm going to go back to the usb hub
[93:42] and then i'm going to go back to the usb hub
[93:44] and then i'm going to go back to the usb hub
[93:46] and then i'm going to go back to the usb hub
[93:48] and then i'm going to go back to the usb hub
[93:50] and then i'm going to go back to the usb hub
[93:52] and then i'm going to go back to the usb hub
[93:54] and then i'm going to go back to the usb hub
[93:56] and then i'm going to go back to the usb hub
[93:58] and then i'm going to go back to the usb hub
[94:00] and then i'm going to go back to the usb hub
[94:02] and then i'm going to go back to the usb hub
[94:04] and then i'm going to go back to the usb hub
[94:06] and then i'm going to go back to the usb hub
[94:08] and then i'm going to go back to the usb hub
[94:10] and then i'm going to go back to the usb hub
[94:12] and then i'm going to go back to the usb hub
[94:14] and then i'm going to go back to the usb hub
[94:16] and then i'm going to go back to the usb hub
[94:18] and then i'm going to go back to the usb hub
[94:20] and then i'm going to go back to the usb hub
[94:22] and then i'm going to go back to the usb hub
[94:24] and then i'm going to go back to the usb hub
[94:26] and then i'm going to go back to the usb hub
[94:28] and then i'm going to go back to the usb hub
[94:30] and then i'm going to go back to the usb hub
[94:32] and then i'm going to go back to the usb hub
[94:34] and then i'm going to go back to the usb hub
[94:36] and then i'm going to go back to the usb hub
[94:38] and then i'm going to go back to the usb hub
[94:40] and then i'm going to go back to the usb hub
[94:42] and then i'm going to go back to the usb hub
[94:44] and then i'm going to go back to the usb hub
[94:46] and then i'm going to go back to the usb hub
[94:48] and then i'm going to go back to the usb hub
[94:50] and then i'm going to go back to the usb hub
[94:52] and then i'm going to go back to the usb hub
[94:54] and then i'm going to go back to the usb hub
[94:56] and then i'm going to go back to the usb hub
[94:58] and then i'm going to go back to the usb hub
[95:00] and then i'm going to go back to the usb hub
[95:02] and then i'm going to go back to the usb hub
[95:04] and then i'm going to go back to the usb hub
[95:06] and then i'm going to go back to the usb hub
[95:08] and then i'm going to go back to the usb hub
[95:10] and then i'm going to go back to the usb hub
[95:12] and then i'm going to go back to the usb hub
[95:14] and then i'm going to go back to the usb hub
[95:16] and then i'm going to go back to the usb hub
[95:18] and then i'm going to go back to the usb hub
[95:20] and then i'm going to go back to the usb hub
[95:22] and then i'm going to go back to the usb hub
[95:24] and then i'm going to go back to the usb hub
[95:26] and then i'm going to go back to the usb hub
[95:28] and then i'm going to go back to the usb hub
[95:30] and then i'm going to go back to the usb hub
[95:32] and then i'm going to go back to the usb hub
[95:34] and then i'm going to go back to the usb hub
[95:36] and then i'm going to go back to the usb hub
[95:38] and then i'm going to go back to the usb hub
[95:40] and then i'm going to go back to the usb hub
[95:42] and then i'm going to go back to the usb hub
[95:44] and then i'm going to go back to the usb hub
[95:46] and then i'm going to go back to the usb hub
[95:48] and then i'm going to go back to the usb hub
[95:50] and then i'm going to go back to the usb hub
[95:52] and then i'm going to go back to the usb hub
[95:54] and then i'm going to go back to the usb hub
[95:56] and then i'm going to go back to the usb hub
[95:58] and then i'm going to go back to the usb hub
[96:00] and then i'm going to go back to the usb hub
[96:02] and then i'm going to go back to the usb hub
[96:04] and then i'm going to go back to the usb hub
[96:06] and then i'm going to go back to the usb hub
[96:08] and then i'm going to go back to the usb hub
[96:10] and then i'm going to go back to the usb hub
[96:12] and then i'm going to go back to the usb hub
[96:14] and then i'm going to go back to the usb hub
[96:16] and then i'm going to go back to the usb hub
[96:18] and then i'm going to go back to the usb hub
[96:20] and then i'm going to go back to the usb hub
[96:22] and then i'm going to go back to the usb hub
[96:24] and then i'm going to go back to the usb hub
[96:26] and then i'm going to go back to the usb hub
[96:28] and then i'm going to go back to the usb hub
[96:30] and then i'm going to go back to the usb hub
[96:32] and then i'm going to go back to the usb hub
[96:34] and then i'm going to go back to the usb hub
[96:36] and then i'm going to go back to the usb hub
[96:38] and then i'm going to go back to the usb hub
[96:40] and then i'm going to go back to the usb hub
[96:42] and then i'm going to go back to the usb hub
[96:44] and then i'm going to go back to the usb hub
[96:46] and then i'm going to go back to the usb hub
[96:48] and then i'm going to go back to the usb hub
[96:50] and then i'm going to go back to the usb hub
[96:52] and then i'm going to go back to the usb hub
[96:54] and then i'm going to go back to the usb hub
[96:56] and then i'm going to go back to the usb hub
[96:58] and then i'm going to go back to the usb hub
[97:00] and then i'm going to go back to the usb hub
[97:02] and then i'm going to go back to the usb hub
[97:04] and then i'm going to go back to the usb hub
[97:06] and then i'm going to go back to the usb hub
[97:08] and then i'm going to go back to the usb hub
[97:10] and then i'm going to go back to the usb hub
[97:12] and then i'm going to go back to the usb hub
[97:14] and then i'm going to go back to the usb hub
[97:16] and then i'm going to go back to the usb hub
[97:18] and then i'm going to go back to the usb hub
[97:20] and then i'm going to go back to the usb hub
[97:22] and then i'm going to go back to the usb hub
[97:24] and then i'm going to go back to the usb hub
[97:26] and then i'm going to go back to the usb hub
[97:28] and then i'm going to go back to the usb hub
[97:30] and then i'm going to go back to the usb hub
[97:32] and then i'm going to go back to the usb hub
[97:34] and then i'm going to go back to the usb hub
[97:36] and then i'm going to go back to the usb hub
[97:38] and then i'm going to go back to the usb hub
[97:40] and then i'm going to go back to the usb hub
[97:42] and then i'm going to go back to the usb hub
[97:44] and then i'm going to go back to the usb hub
[97:46] and then i'm going to go back to the usb hub
[97:48] and then i'm going to go back to the usb hub
[97:50] and then i'm going to go back to the usb hub
[97:52] and then i'm going to go back to the usb hub
[97:54] and then i'm going to go back to the usb hub
[97:56] and then i'm going to go back to the usb hub
[97:58] and then i'm going to go back to the usb hub
[98:00] and then i'm going to go back to the usb hub
[98:02] and then i'm going to go back to the usb hub
[98:04] and then i'm going to go back to the usb hub
[98:06] and then i'm going to go back to the usb hub
[98:08] and then i'm going to go back to the usb hub
[98:10] and then i'm going to go back to the usb hub
[98:12] and then i'm going to go back to the usb hub
[98:14] and then i'm going to go back to the usb hub
[98:16] and then i'm going to go back to the usb hub
[98:18] and then i'm going to go back to the usb hub
[98:20] and then i'm going to go back to the usb hub
[98:22] and then i'm going to go back to the usb hub
[98:24] and then i'm going to go back to the usb hub
[98:26] and then i'm going to go back to the usb hub
[98:28] and then i'm going to go back to the usb hub
[98:30] and then i'm going to go back to the usb hub
[98:32] and then i'm going to go back to the usb hub
[98:34] and then i'm going to go back to the usb hub
[98:36] and then i'm going to go back to the usb hub
[98:38] and then i'm going to go back to the usb hub
[98:40] and then i'm going to go back to the usb hub
[98:42] and then i'm going to go back to the usb hub
[98:44] and then i'm going to go back to the usb hub
[98:46] and then i'm going to go back to the usb hub
[98:48] and then i'm going to go back to the usb hub
[98:50] and then i'm going to go back to the usb hub
[98:52] and then i'm going to go back to the usb hub
[98:54] and then i'm going to go back to the usb hub
[98:56] and then i'm going to go back to the usb hub
[98:58] and then i'm going to go back to the usb hub
[99:00] and then i'm going to go back to the usb hub
[99:02] and then i'm going to go back to the usb hub
[99:04] and then i'm going to go back to the usb hub
[99:06] and then i'm going to go back to the usb hub
[99:08] and then i'm going to go back to the usb hub
[99:10] and then i'm going to go back to the usb hub
[99:12] and then i'm going to go back to the usb hub
[99:14] and then i'm going to go back to the usb hub
[99:16] and then i'm going to go back to the usb hub
[99:18] and then i'm going to go back to the usb hub
[99:20] and then i'm going to go back to the usb hub
[99:22] and then i'm going to go back to the usb hub
[99:24] and then i'm going to go back to the usb hub
[99:26] and then i'm going to go back to the usb hub
[99:28] and then i'm going to go back to the usb hub
[99:30] and then i'm going to go back to the usb hub
[99:32] and then i'm going to go back to the usb hub
[99:34] and then i'm going to go back to the usb hub
[99:36] and then i'm going to go back to the usb hub
[99:38] and then i'm going to go back to the usb hub
[99:40] and then i'm going to go back to the usb hub
[99:42] and then i'm going to go back to the usb hub
[99:44] and then i'm going to go back to the usb hub
[99:46] and then i'm going to go back to the usb hub
[99:48] and then i'm going to go back to the usb hub
[99:50] and then i'm going to go back to the usb hub
[99:52] and then i'm going to go back to the usb hub
[99:54] and then i'm going to go back to the usb hub
[99:56] and then i'm going to go back to the usb hub
[99:58] and then i'm going to go back to the usb hub
[100:00.84] and then i'm going to go back to the usb hub
[100:02.84] and then i'm going to go back to the usb hub
[100:04.84] and then i'm going to go back to the usb hub
[100:06.84] and then i'm going to go back to the usb hub
[100:08.84] and then i'm going to go back to the usb hub
[100:10.84] and then i'm going to go back to the usb hub
[100:12.84] and then i'm going to go back to the usb hub
[100:14.84] and then i'm going to go back to the usb hub
[100:16.84] and then i'm going to go back to the usb hub
[100:18.84] and then i'm going to go back to the usb hub
[100:20.84] and then i'm going to go back to the usb hub
[100:22.84] and then i'm going to go back to the usb hub
[100:24.84] and then i'm going to go back to the usb hub
[100:26.84] and then i'm going to go back to the usb hub
[100:28.84] and then i'm going to go back to the usb hub
[100:30.84] and then i'm going to go back to the usb hub
[100:32.84] and then i'm going to go back to the usb hub
[100:34.84] and then i'm going to go back to the usb hub
[100:36.84] and then i'm going to go back to the usb hub
[100:38.84] and then i'm going to go back to the usb hub
[100:40.84] and then i'm going to go back to the usb hub
[100:42.84] and then i'm going to go back to the usb hub
[100:44.84] and then i'm going to go back to the usb hub
[100:46.84] and then i'm going to go back to the usb hub
[100:48.84] and then i'm going to go back to the usb hub
[100:50.84] and then i'm going to go back to the usb hub
[100:52.84] and then i'm going to go back to the usb hub
[100:54.84] and then i'm going to go back to the usb hub
[100:56.84] and then i'm going to go back to the usb hub
[100:58.84] and then i'm going to go back to the usb hub
[101:00.84] and then i'm going to go back to the usb hub
[101:02.84] and then i'm going to go back to the usb hub
[101:04.84] and then i'm going to go back to the usb hub
[101:06.84] and then i'm going to go back to the usb hub
[101:08.84] and then i'm going to go back to the usb hub
[101:10.84] and then i'm going to go back to the usb hub
[101:12.84] and then i'm going to go back to the usb hub
[101:14.84] and then i'm going to go back to the usb hub
[101:16.84] and then i'm going to go back to the usb hub
[101:18.84] and then i'm going to go back to the usb hub
[101:20.84] and then i'm going to go back to the usb hub
[101:22.84] and then i'm going to go back to the usb hub
[101:24.84] and then i'm going to go back to the usb hub
[101:26.84] and then i'm going to go back to the usb hub
[101:28.84] and then i'm going to go back to the usb hub
[101:30.84] and then i'm going to go back to the usb hub
[101:32.84] and then i'm going to go back to the usb hub
[101:34.84] and then i'm going to go back to the usb hub
[101:36.84] and then i'm going to go back to the usb hub
[101:38.84] and then i'm going to go back to the usb hub
[101:40.84] and then i'm going to go back to the usb hub
[101:42.84] and then i'm going to go back to the usb hub
[101:44.84] and then i'm going to go back to the usb hub
[101:46.84] and then i'm going to go back to the usb hub
[101:48.84] and then i'm going to go back to the usb hub
[101:50.84] and then i'm going to go back to the usb hub
[101:52.84] and then i'm going to go back to the usb hub
[101:54.84] and then i'm going to go back to the usb hub
[101:56.84] and then i'm going to go back to the usb hub
[101:58.84] and then i'm going to go back to the usb hub
[102:00.84] and then i'm going to go back to the usb hub
[102:02.84] and then i'm going to go back to the usb hub
[102:04.84] and then i'm going to go back to the usb hub
[102:06.84] and then i'm going to go back to the usb hub
[102:08.84] and then i'm going to go back to the usb hub
[102:10.84] and then i'm going to go back to the usb hub
[102:12.84] and then i'm going to go back to the usb hub
[102:14.84] and then i'm going to go back to the usb hub
[102:16.84] and then i'm going to go back to the usb hub
[102:18.84] and then i'm going to go back to the usb hub
[102:20.84] and then i'm going to go back to the usb hub
[102:22.84] and then i'm going to go back to the usb hub
[102:24.84] and then i'm going to go back to the usb hub
[102:26.84] and then i'm going to go back to the usb hub
[102:28.84] and then i'm going to go back to the usb hub
[102:30.84] and then i'm going to go back to the usb hub
[102:32.84] and then i'm going to go back to the usb hub
[102:34.84] and then i'm going to go back to the usb hub
[102:36.84] and then i'm going to go back to the usb hub
[102:38.84] and then i'm going to go back to the usb hub
[102:40.84] and then i'm going to go back to the usb hub
[102:42.84] and then i'm going to go back to the usb hub
[102:44.84] and then i'm going to go back to the usb hub
[102:46.84] and then i'm going to go back to the usb hub
[102:48.84] and then i'm going to go back to the usb hub
[102:50.84] and then i'm going to go back to the usb hub
[102:52.84] and then i'm going to go back to the usb hub
[102:54.84] and then i'm going to go back to the usb hub
[102:56.84] and then i'm going to go back to the usb hub
[102:58.84] and then i'm going to go back to the usb hub
[103:00.84] and then i'm going to go back to the usb hub
[103:02.84] and then i'm going to go back to the usb hub
[103:04.84] and then i'm going to go back to the usb hub
[103:06.84] and then i'm going to go back to the usb hub
[103:08.84] and then i'm going to go back to the usb hub
[103:10.84] and then i'm going to go back to the usb hub
[103:12.84] and then i'm going to go back to the usb hub
[103:14.84] and then i'm going to go back to the usb hub
[103:16.84] and then i'm going to go back to the usb hub
[103:18.84] and then i'm going to go back to the usb hub
[103:20.84] and then i'm going to go back to the usb hub
[103:22.84] and then i'm going to go back to the usb hub
[103:24.84] and then i'm going to go back to the usb hub
[103:26.84] and then i'm going to go back to the usb hub
[103:28.84] and then i'm going to go back to the usb hub
[103:30.84] and then i'm going to go back to the usb hub
[103:32.84] and then i'm going to go back to the usb hub
[103:34.84] and then i'm going to go back to the usb hub
[103:36.84] and then i'm going to go back to the usb hub
[103:38.84] and then i'm going to go back to the usb hub
[103:40.84] and then i'm going to go back to the usb hub
[103:42.84] and then i'm going to go back to the usb hub
[103:44.84] and then i'm going to go back to the usb hub
[103:46.84] and then i'm going to go back to the usb hub
[103:48.84] and then i'm going to go back to the usb hub
[103:50.84] and then i'm going to go back to the usb hub
[103:52.84] and then i'm going to go back to the usb hub
[103:54.84] and then i'm going to go back to the usb hub
[103:56.84] and then i'm going to go back to the usb hub
[103:58.84] and then i'm going to go back to the usb hub
[104:00.84] and then i'm going to go back to the usb hub
[104:02.84] and then i'm going to go back to the usb hub
[104:04.84] and then i'm going to go back to the usb hub
[104:06.84] and then i'm going to go back to the usb hub
[104:08.84] and then i'm going to go back to the usb hub
[104:10.84] and then i'm going to go back to the usb hub
[104:12.84] and then i'm going to go back to the usb hub
[104:14.84] and then i'm going to go back to the usb hub
[104:16.84] and then i'm going to go back to the usb hub
[104:18.84] and then i'm going to go back to the usb hub
[104:20.84] and then i'm going to go back to the usb hub
[104:22.84] and then i'm going to go back to the usb hub
[104:24.84] and then i'm going to go back to the usb hub
[104:26.84] and then i'm going to go back to the usb hub
[104:28.84] and then i'm going to go back to the usb hub
[104:30.84] and then i'm going to go back to the usb hub
[104:32.84] and then i'm going to go back to the usb hub
[104:34.84] and then i'm going to go back to the usb hub
[104:36.84] and then i'm going to go back to the usb hub
[104:38.84] and then i'm going to go back to the usb hub
[104:40.84] and then i'm going to go back to the usb hub
[104:42.84] and then i'm going to go back to the usb hub
[104:44.84] and then i'm going to go back to the usb hub
[104:46.84] and then i'm going to go back to the usb hub
[104:48.84] and then i'm going to go back to the usb hub
[104:50.84] and then i'm going to go back to the usb hub
[104:52.84] and then i'm going to go back to the usb hub
[104:54.84] and then i'm going to go back to the usb hub
[104:56.84] and then i'm going to go back to the usb hub
[104:58.84] and then i'm going to go back to the usb hub
[105:00.84] and then i'm going to go back to the usb hub
[105:02.84] and then i'm going to go back to the usb hub
[105:04.84] and then i'm going to go back to the usb hub
[105:06.84] and then i'm going to go back to the usb hub
[105:08.84] and then i'm going to go back to the usb hub
[105:10.84] and then i'm going to go back to the usb hub
[105:12.84] and then i'm going to go back to the usb hub
[105:14.84] and then i'm going to go back to the usb hub
[105:16.84] and then i'm going to go back to the usb hub
[105:18.84] and then i'm going to go back to the usb hub
[105:20.84] and then i'm going to go back to the usb hub
[105:22.84] and then i'm going to go back to the usb hub
[105:24.84] and then i'm going to go back to the usb hub
[105:26.84] and then i'm going to go back to the usb hub
[105:28.84] and then i'm going to go back to the usb hub
[105:30.84] and then i'm going to go back to the usb hub
[105:32.84] and then i'm going to go back to the usb hub
[105:34.84] and then i'm going to go back to the usb hub
[105:36.84] and then i'm going to go back to the usb hub
[105:38.84] and then i'm going to go back to the usb hub
[105:40.84] and then i'm going to go back to the usb hub
[105:42.84] and then i'm going to go back to the usb hub
[105:44.84] and then i'm going to go back to the usb hub
[105:46.84] and then i'm going to go back to the usb hub
[105:48.84] and then i'm going to go back to the usb hub
[105:50.84] and then i'm going to go back to the usb hub
[105:52.84] and then i'm going to go back to the usb hub
[105:54.84] and then i'm going to go back to the usb hub
[105:56.84] and then i'm going to go back to the usb hub
[105:58.84] and then i'm going to go back to the usb hub
[106:00.84] and then i'm going to go back to the usb hub
[106:02.84] and then i'm going to go back to the usb hub
[106:04.84] and then i'm going to go back to the usb hub
[106:06.84] and then i'm going to go back to the usb hub
[106:08.84] and then i'm going to go back to the usb hub
[106:10.84] and then i'm going to go back to the usb hub
[106:12.84] and then i'm going to go back to the usb hub
[106:14.84] and then i'm going to go back to the usb hub
[106:16.84] and then i'm going to go back to the usb hub
[106:18.84] and then i'm going to go back to the usb hub
[106:20.84] and then i'm going to go back to the usb hub
[106:22.84] and then i'm going to go back to the usb hub
[106:24.84] and then i'm going to go back to the usb hub
[106:26.84] and then i'm going to go back to the usb hub
[106:28.84] and then i'm going to go back to the usb hub
[106:30.84] and then i'm going to go back to the usb hub
[106:32.84] and then i'm going to go back to the usb hub
[106:34.84] and then i'm going to go back to the usb hub
[106:36.84] and then i'm going to go back to the usb hub
[106:38.84] and then i'm going to go back to the usb hub
[106:40.84] and then i'm going to go back to the usb hub
[106:42.84] and then i'm going to go back to the usb hub
[106:44.84] and then i'm going to go back to the usb hub
[106:46.84] and then i'm going to go back to the usb hub
[106:48.84] and then i'm going to go back to the usb hub
[106:50.84] and then i'm going to go back to the usb hub
[106:52.84] and then i'm going to go back to the usb hub
[106:54.84] and then i'm going to go back to the usb hub
[106:56.84] and then i'm going to go back to the usb hub
[106:58.84] and then i'm going to go back to the usb hub
[107:00.84] and then i'm going to go back to the usb hub
[107:02.84] and then i'm going to go back to the usb hub
[107:04.84] and then i'm going to go back to the usb hub
[107:06.84] and then i'm going to go back to the usb hub
[107:08.84] and then i'm going to go back to the usb hub
[107:10.84] and then i'm going to go back to the usb hub
[107:12.84] and then i'm going to go back to the usb hub
[107:14.84] and then i'm going to go back to the usb hub
[107:16.84] and then i'm going to go back to the usb hub
[107:18.84] and then i'm going to go back to the usb hub
[107:20.84] and then i'm going to go back to the usb hub
[107:22.84] and then i'm going to go back to the usb hub
[107:24.84] and then i'm going to go back to the usb hub
[107:26.84] and then i'm going to go back to the usb hub
[107:28.84] and then i'm going to go back to the usb hub
[107:30.84] and then i'm going to go back to the usb hub
[107:32.84] and then i'm going to go back to the usb hub
[107:34.84] and then i'm going to go back to the usb hub
[107:36.84] and then i'm going to go back to the usb hub
[107:38.84] and then i'm going to go back to the usb hub
[107:40.84] and then i'm going to go back to the usb hub
[107:42.84] and then i'm going to go back to the usb hub
[107:44.84] and then i'm going to go back to the usb hub
[107:46.84] and then i'm going to go back to the usb hub
[107:48.84] and then i'm going to go back to the usb hub
[107:50.84] and then i'm going to go back to the usb hub
[107:52.84] and then i'm going to go back to the usb hub
[107:54.84] and then i'm going to go back to the usb hub
[107:56.84] and then i'm going to go back to the usb hub
[107:58.84] and then i'm going to go back to the usb hub
[108:00.84] and then i'm going to go back to the usb hub
[108:02.84] and then i'm going to go back to the usb hub
[108:04.84] and then i'm going to go back to the usb hub
[108:06.84] and then i'm going to go back to the usb hub
[108:08.84] and then i'm going to go back to the usb hub
[108:10.84] and then i'm going to go back to the usb hub
[108:12.84] and then i'm going to go back to the usb hub
[108:14.84] and then i'm going to go back to the usb hub
[108:16.84] and then i'm going to go back to the usb hub
[108:18.84] and then i'm going to go back to the usb hub
[108:20.84] and then i'm going to go back to the usb hub
[108:22.84] and then i'm going to go back to the usb hub
[108:24.84] and then i'm going to go back to the usb hub
[108:26.84] and then i'm going to go back to the usb hub
[108:28.84] and then i'm going to go back to the usb hub
[108:30.84] and then i'm going to go back to the usb hub
[108:32.84] and then i'm going to go back to the usb hub
[108:34.84] and then i'm going to go back to the usb hub
[108:36.84] and then i'm going to go back to the usb hub
[108:38.84] and then i'm going to go back to the usb hub
[108:40.84] and then i'm going to go back to the usb hub
[108:42.84] and then i'm going to go back to the usb hub
[108:44.84] and then i'm going to go back to the usb hub
[108:46.84] and then i'm going to go back to the usb hub
[108:48.84] and then i'm going to go back to the usb hub
[108:50.84] and then i'm going to go back to the usb hub
[108:52.84] and then i'm going to go back to the usb hub
[108:54.84] and then i'm going to go back to the usb hub
[108:56.84] and then i'm going to go back to the usb hub
[108:58.84] and then i'm going to go back to the usb hub
[109:00.84] and then i'm going to go back to the usb hub
[109:02.84] and then i'm going to go back to the usb hub
[109:04.84] and then i'm going to go back to the usb hub
[109:06.84] and then i'm going to go back to the usb hub
[109:08.84] and then i'm going to go back to the usb hub
[109:10.84] and then i'm going to go back to the usb hub
[109:12.84] and then i'm going to go back to the usb hub
[109:14.84] and then i'm going to go back to the usb hub
[109:16.84] and then i'm going to go back to the usb hub
[109:18.84] and then i'm going to go back to the usb hub
[109:20.84] and then i'm going to go back to the usb hub
[109:22.84] and then i'm going to go back to the usb hub
[109:24.84] and then i'm going to go back to the usb hub
[109:26.84] and then i'm going to go back to the usb hub
[109:28.84] and then i'm going to go back to the usb hub
[109:30.84] and then i'm going to go back to the usb hub
[109:32.84] and then i'm going to go back to the usb hub
[109:34.84] and then i'm going to go back to the usb hub
[109:36.84] and then i'm going to go back to the usb hub
[109:38.84] and then i'm going to go back to the usb hub
[109:40.84] and then i'm going to go back to the usb hub
[109:42.84] and then i'm going to go back to the usb hub
[109:44.84] and then i'm going to go back to the usb hub
[109:46.84] and then i'm going to go back to the usb hub
[109:48.84] and then i'm going to go back to the usb hub
[109:50.84] and then i'm going to go back to the usb hub
[109:52.84] and then i'm going to go back to the usb hub
[109:54.84] and then i'm going to go back to the usb hub
[109:56.84] and then i'm going to go back to the usb hub
[109:58.84] and then i'm going to go back to the usb hub
[110:00.84] and then i'm going to go back to the usb hub
[110:02.84] and then i'm going to go back to the usb hub
[110:04.84] and then i'm going to go back to the usb hub
[110:06.84] and then i'm going to go back to the usb hub
[110:08.84] and then i'm going to go back to the usb hub
[110:10.84] and then i'm going to go back to the usb hub
[110:12.84] and then i'm going to go back to the usb hub
[110:14.84] and then i'm going to go back to the usb hub
[110:16.84] and then i'm going to go back to the usb hub
[110:18.84] and then i'm going to go back to the usb hub
[110:20.84] and then i'm going to go back to the usb hub
[110:22.84] and then i'm going to go back to the usb hub
[110:24.84] and then i'm going to go back to the usb hub
[110:26.84] and then i'm going to go back to the usb hub
[110:28.84] and then i'm going to go back to the usb hub
[110:30.84] and then i'm going to go back to the usb hub
[110:32.84] and then i'm going to go back to the usb hub
[110:34.84] and then i'm going to go back to the usb hub
[110:36.84] and then i'm going to go back to the usb hub
[110:38.84] and then i'm going to go back to the usb hub
[110:40.84] and then i'm going to go back to the usb hub
[110:42.84] and then i'm going to go back to the usb hub
[110:44.84] and then i'm going to go back to the usb hub
[110:46.84] and then i'm going to go back to the usb hub
[110:48.84] and then i'm going to go back to the usb hub
[110:50.84] and then i'm going to go back to the usb hub
[110:52.84] and then i'm going to go back to the usb hub
[110:54.84] and then i'm going to go back to the usb hub
[110:56.84] and then i'm going to go back to the usb hub
[110:58.84] and then i'm going to go back to the usb hub
[111:00.84] and then i'm going to go back to the usb hub
[111:02.84] and then i'm going to go back to the usb hub
[111:04.84] and then i'm going to go back to the usb hub
[111:06.84] and then i'm going to go back to the usb hub
[111:08.84] and then i'm going to go back to the usb hub
[111:10.84] and then i'm going to go back to the usb hub
[111:12.84] and then i'm going to go back to the usb hub
[111:14.84] and then i'm going to go back to the usb hub
[111:16.84] and then i'm going to go back to the usb hub
[111:18.84] and then i'm going to go back to the usb hub
[111:20.84] and then i'm going to go back to the usb hub
[111:22.84] and then i'm going to go back to the usb hub
[111:24.84] and then i'm going to go back to the usb hub
[111:26.84] and then i'm going to go back to the usb hub
[111:28.84] and then i'm going to go back to the usb hub
[111:30.84] and then i'm going to go back to the usb hub
[111:32.84] and then i'm going to go back to the usb hub
[111:34.84] and then i'm going to go back to the usb hub
[111:36.84] and then i'm going to go back to the usb hub
[111:38.84] and then i'm going to go back to the usb hub
[111:40.84] and then i'm going to go back to the usb hub
[111:42.84] and then i'm going to go back to the usb hub
[111:44.84] and then i'm going to go back to the usb hub
[111:46.84] and then i'm going to go back to the usb hub
[111:48.84] and then i'm going to go back to the usb hub
[111:50.84] and then i'm going to go back to the usb hub
[111:52.84] and then i'm going to go back to the usb hub
[111:54.84] and then i'm going to go back to the usb hub
[111:56.84] and then i'm going to go back to the usb hub
[111:58.84] and then i'm going to go back to the usb hub
[112:00.84] and then i'm going to go back to the usb hub
[112:02.84] and then i'm going to go back to the usb hub
[112:04.84] and then i'm going to go back to the usb hub
[112:06.84] and then i'm going to go back to the usb hub
[112:08.84] and then i'm going to go back to the usb hub
[112:10.84] and then i'm going to go back to the usb hub
[112:12.84] and then i'm going to go back to the usb hub
[112:14.84] and then i'm going to go back to the usb hub
[112:16.84] and then i'm going to go back to the usb hub
[112:18.84] and then i'm going to go back to the usb hub
[112:20.84] and then i'm going to go back to the usb hub
[112:22.84] and then i'm going to go back to the usb hub
[112:24.84] and then i'm going to go back to the usb hub
[112:26.84] and then i'm going to go back to the usb hub
[112:28.84] and then i'm going to go back to the usb hub
[112:30.84] and then i'm going to go back to the usb hub
[112:32.84] and then i'm going to go back to the usb hub
[112:34.84] and then i'm going to go back to the usb hub
[112:36.84] and then i'm going to go back to the usb hub
[112:38.84] and then i'm going to go back to the usb hub
[112:40.84] and then i'm going to go back to the usb hub
[112:42.84] and then i'm going to go back to the usb hub
[112:44.84] and then i'm going to go back to the usb hub
[112:46.84] and then i'm going to go back to the usb hub
[112:48.84] and then i'm going to go back to the usb hub
[112:50.84] and then i'm going to go back to the usb hub
[112:52.84] and then i'm going to go back to the usb hub
[112:54.84] and then i'm going to go back to the usb hub
[112:56.84] and then i'm going to go back to the usb hub
[112:58.84] and then i'm going to go back to the usb hub
[113:00.84] and then i'm going to go back to the usb hub
[113:02.84] and then i'm going to go back to the usb hub
[113:04.84] and then i'm going to go back to the usb hub
[113:06.84] and then i'm going to go back to the usb hub
[113:08.84] and then i'm going to go back to the usb hub
[113:10.84] and then i'm going to go back to the usb hub
[113:12.84] and then i'm going to go back to the usb hub
[113:14.84] and then i'm going to go back to the usb hub
[113:16.84] and then i'm going to go back to the usb hub
[113:18.84] and then i'm going to go back to the usb hub
[113:20.84] and then i'm going to go back to the usb hub
[113:22.84] and then i'm going to go back to the usb hub
[113:24.84] and then i'm going to go back to the usb hub
[113:26.84] and then i'm going to go back to the usb hub
[113:28.84] and then i'm going to go back to the usb hub
[113:30.84] and then i'm going to go back to the usb hub
[113:32.84] and then i'm going to go back to the usb hub
[113:34.84] and then i'm going to go back to the usb hub
[113:36.84] and then i'm going to go back to the usb hub
[113:38.84] and then i'm going to go back to the usb hub
[113:40.84] and then i'm going to go back to the usb hub
[113:42.84] and then i'm going to go back to the usb hub
[113:44.84] and then i'm going to go back to the usb hub
[113:46.84] and then i'm going to go back to the usb hub
[113:48.84] and then i'm going to go back to the usb hub
[113:50.84] and then i'm going to go back to the usb hub
[113:52.84] and then i'm going to go back to the usb hub
[113:54.84] and then i'm going to go back to the usb hub
[113:56.84] and then i'm going to go back to the usb hub
[113:58.84] and then i'm going to go back to the usb hub
[114:00.84] and then i'm going to go back to the usb hub
[114:02.84] and then i'm going to go back to the usb hub
[114:04.84] and then i'm going to go back to the usb hub
[114:06.84] and then i'm going to go back to the usb hub
[114:08.84] and then i'm going to go back to the usb hub
[114:10.84] and then i'm going to go back to the usb hub
[114:12.84] and then i'm going to go back to the usb hub
[114:14.84] and then i'm going to go back to the usb hub
[114:16.84] and then i'm going to go back to the usb hub
[114:18.84] and then i'm going to go back to the usb hub
[114:20.84] and then i'm going to go back to the usb hub
[114:22.84] and then i'm going to go back to the usb hub
[114:24.84] and then i'm going to go back to the usb hub
[114:26.84] and then i'm going to go back to the usb hub
[114:28.84] and then i'm going to go back to the usb hub
[114:30.84] and then i'm going to go back to the usb hub
[114:32.84] and then i'm going to go back to the usb hub
[114:34.84] and then i'm going to go back to the usb hub
[114:36.84] and then i'm going to go back to the usb hub
[114:38.84] and then i'm going to go back to the usb hub
[114:40.84] and then i'm going to go back to the usb hub
[114:42.84] and then i'm going to go back to the usb hub
[114:44.84] and then i'm going to go back to the usb hub
[114:46.84] and then i'm going to go back to the usb hub
[114:48.84] and then i'm going to go back to the usb hub
[114:50.84] and then i'm going to go back to the usb hub
[114:52.84] and then i'm going to go back to the usb hub
[114:54.84] and then i'm going to go back to the usb hub
[114:56.84] and then i'm going to go back to the usb hub
[114:58.84] and then i'm going to go back to the usb hub
[115:00.84] and then i'm going to go back to the usb hub
[115:02.84] and then i'm going to go back to the usb hub
[115:04.84] and then i'm going to go back to the usb hub
[115:06.84] and then i'm going to go back to the usb hub
[115:08.84] and then i'm going to go back to the usb hub
[115:10.84] and then i'm going to go back to the usb hub
[115:12.84] and then i'm going to go back to the usb hub
[115:14.84] and then i'm going to go back to the usb hub
[115:16.84] and then i'm going to go back to the usb hub
[115:18.84] and then i'm going to go back to the usb hub
[115:20.84] and then i'm going to go back to the usb hub
[115:22.84] and then i'm going to go back to the usb hub
[115:24.84] and then i'm going to go back to the usb hub
[115:26.84] and then i'm going to go back to the usb hub
[115:28.84] and then i'm going to go back to the usb hub
[115:30.84] and then i'm going to go back to the usb hub
[115:32.84] and then i'm going to go back to the usb hub
[115:34.84] and then i'm going to go back to the usb hub
[115:36.84] and then i'm going to go back to the usb hub
[115:38.84] and then i'm going to go back to the usb hub
[115:40.84] and then i'm going to go back to the usb hub
[115:42.84] and then i'm going to go back to the usb hub
[115:44.84] and then i'm going to go back to the usb hub
[115:46.84] and then i'm going to go back to the usb hub
[115:48.84] and then i'm going to go back to the usb hub
[115:50.84] and then i'm going to go back to the usb hub
[115:52.84] and then i'm going to go back to the usb hub
[115:54.84] and then i'm going to go back to the usb hub
[115:56.84] and then i'm going to go back to the usb hub
[115:58.84] and then i'm going to go back to the usb hub
[116:00.84] and then i'm going to go back to the usb hub
[116:02.84] and then i'm going to go back to the usb hub
[116:04.84] and then i'm going to go back to the usb hub
[116:06.84] and then i'm going to go back to the usb hub
[116:08.84] and then i'm going to go back to the usb hub
[116:10.84] and then i'm going to go back to the usb hub
[116:12.84] and then i'm going to go back to the usb hub
[116:14.84] and then i'm going to go back to the usb hub
[116:16.84] and then i'm going to go back to the usb hub
[116:18.84] and then i'm going to go back to the usb hub
[116:20.84] and then i'm going to go back to the usb hub
[116:22.84] and then i'm going to go back to the usb hub
[116:24.84] and then i'm going to go back to the usb hub
[116:26.84] and then i'm going to go back to the usb hub
[116:28.84] and then i'm going to go back to the usb hub
[116:30.84] and then i'm going to go back to the usb hub
[116:32.84] and then i'm going to go back to the usb hub
[116:34.84] and then i'm going to go back to the usb hub
[116:36.84] and then i'm going to go back to the usb hub
[116:38.84] and then i'm going to go back to the usb hub
[116:40.84] and then i'm going to go back to the usb hub
[116:42.84] and then i'm going to go back to the usb hub
[116:44.84] and then i'm going to go back to the usb hub
[116:46.84] and then i'm going to go back to the usb hub
[116:48.84] and then i'm going to go back to the usb hub
[116:50.84] and then i'm going to go back to the usb hub
[116:52.84] and then i'm going to go back to the usb hub
[116:54.84] and then i'm going to go back to the usb hub
[116:56.84] and then i'm going to go back to the usb hub
[116:58.84] and then i'm going to go back to the usb hub
[117:00.84] and then i'm going to go back to the usb hub
[117:02.84] and then i'm going to go back to the usb hub
[117:04.84] and then i'm going to go back to the usb hub
[117:06.84] and then i'm going to go back to the usb hub
[117:08.84] and then i'm going to go back to the usb hub
[117:10.84] and then i'm going to go back to the usb hub
[117:12.84] and then i'm going to go back to the usb hub
[117:14.84] and then i'm going to go back to the usb hub
[117:16.84] and then i'm going to go back to the usb hub
[117:18.84] and then i'm going to go back to the usb hub
[117:20.84] and then i'm going to go back to the usb hub
[117:22.84] and then i'm going to go back to the usb hub
[117:24.84] and then i'm going to go back to the usb hub
[117:26.84] and then i'm going to go back to the usb hub
[117:28.84] and then i'm going to go back to the usb hub
[117:30.84] and then i'm going to go back to the usb hub
[117:32.84] and then i'm going to go back to the usb hub
[117:34.84] and then i'm going to go back to the usb hub
[117:36.84] and then i'm going to go back to the usb hub
[117:38.84] and then i'm going to go back to the usb hub
[117:40.84] and then i'm going to go back to the usb hub
[117:42.84] and then i'm going to go back to the usb hub
[117:44.84] and then i'm going to go back to the usb hub
[117:46.84] and then i'm going to go back to the usb hub
[117:48.84] and then i'm going to go back to the usb hub
[117:50.84] and then i'm going to go back to the usb hub
[117:52.84] and then i'm going to go back to the usb hub
[117:54.84] and then i'm going to go back to the usb hub
[117:56.84] and then i'm going to go back to the usb hub
[117:58.84] and then i'm going to go back to the usb hub
[118:00.84] and then i'm going to go back to the usb hub
[118:02.84] and then i'm going to go back to the usb hub
[118:04.84] and then i'm going to go back to the usb hub
[118:06.84] and then i'm going to go back to the usb hub
[118:08.84] and then i'm going to go back to the usb hub
[118:10.84] and then i'm going to go back to the usb hub
[118:12.84] and then i'm going to go back to the usb hub
[118:14.84] and then i'm going to go back to the usb hub
[118:16.84] and then i'm going to go back to the usb hub
[118:18.84] and then i'm going to go back to the usb hub
[118:20.84] and then i'm going to go back to the usb hub
[118:22.84] and then i'm going to go back to the usb hub
[118:24.84] and then i'm going to go back to the usb hub
[118:26.84] and then i'm going to go back to the usb hub
[118:28.84] and then i'm going to go back to the usb hub
[118:30.84] and then i'm going to go back to the usb hub
[118:32.84] and then i'm going to go back to the usb hub
[118:34.84] and then i'm going to go back to the usb hub
[118:36.84] and then i'm going to go back to the usb hub
[118:38.84] and then i'm going to go back to the usb hub
[118:40.84] and then i'm going to go back to the usb hub
[118:42.84] and then i'm going to go back to the usb hub
[118:44.84] and then i'm going to go back to the usb hub
[118:46.84] and then i'm going to go back to the usb hub
[118:48.84] and then i'm going to go back to the usb hub
[118:50.84] and then i'm going to go back to the usb hub
[118:52.84] and then i'm going to go back to the usb hub
[118:54.84] and then i'm going to go back to the usb hub
[118:56.84] and then i'm going to go back to the usb hub
[118:58.84] and then i'm going to go back to the usb hub
[119:00.84] and then i'm going to go back to the usb hub
[119:02.84] and then i'm going to go back to the usb hub
[119:04.84] and then i'm going to go back to the usb hub
[119:06.84] and then i'm going to go back to the usb hub
[119:08.84] and then i'm going to go back to the usb hub
[119:10.84] and then i'm going to go back to the usb hub
[119:12.84] and then i'm going to go back to the usb hub
[119:14.84] and then i'm going to go back to the usb hub
[119:16.84] and then i'm going to go back to the usb hub
[119:18.84] and then i'm going to go back to the usb hub
[119:20.84] and then i'm going to go back to the usb hub
[119:22.84] and then i'm going to go back to the usb hub
[119:24.84] and then i'm going to go back to the usb hub
[119:26.84] and then i'm going to go back to the usb hub
[119:28.84] and then i'm going to go back to the usb hub
[119:30.84] and then i'm going to go back to the usb hub
[119:32.84] and then i'm going to go back to the usb hub
[119:34.84] and then i'm going to go back to the usb hub
[119:36.84] and then i'm going to go back to the usb hub
[119:38.84] and then i'm going to go back to the usb hub
[119:40.84] and then i'm going to go back to the usb hub
[119:42.84] and then i'm going to go back to the usb hub
[119:44.84] and then i'm going to go back to the usb hub
[119:46.84] and then i'm going to go back to the usb hub
[119:48.84] and then i'm going to go back to the usb hub
[119:50.84] and then i'm going to go back to the usb hub
[119:52.84] and then i'm going to go back to the usb hub
[119:54.84] and then i'm going to go back to the usb hub
[119:56.84] and then i'm going to go back to the usb hub
[119:58.84] and then i'm going to go back to the usb hub
[120:00.84] and then i'm going to go back to the usb hub
[120:02.84] and then i'm going to go back to the usb hub
[120:04.84] and then i'm going to go back to the usb hub
[120:06.84] and then i'm going to go back to the usb hub
[120:08.84] and then i'm going to go back to the usb hub
[120:10.84] and then i'm going to go back to the usb hub
[120:12.84] and then i'm going to go back to the usb hub
[120:14.84] and then i'm going to go back to the usb hub
[120:16.84] and then i'm going to go back to the usb hub
[120:18.84] and then i'm going to go back to the usb hub
[120:20.84] and then i'm going to go back to the usb hub
[120:22.84] and then i'm going to go back to the usb hub
[120:24.84] and then i'm going to go back to the usb hub
[120:26.84] and then i'm going to go back to the usb hub
[120:28.84] and then i'm going to go back to the usb hub
[120:30.84] and then i'm going to go back to the usb hub
[120:32.84] and then i'm going to go back to the usb hub
[120:34.84] and then i'm going to go back to the usb hub
[120:36.84] and then i'm going to go back to the usb hub
[120:38.84] and then i'm going to go back to the usb hub
[120:40.84] and then i'm going to go back to the usb hub
[120:42.84] and then i'm going to go back to the usb hub
[120:44.84] and then i'm going to go back to the usb hub
[120:46.84] and then i'm going to go back to the usb hub
[120:48.84] and then i'm going to go back to the usb hub
[120:50.84] and then i'm going to go back to the usb hub
[120:52.84] and then i'm going to go back to the usb hub
[120:54.84] and then i'm going to go back to the usb hub
[120:56.84] and then i'm going to go back to the usb hub
[120:58.84] and then i'm going to go back to the usb hub
[121:00.84] and then i'm going to go back to the usb hub
[121:02.84] and then i'm going to go back to the usb hub
[121:04.84] and then i'm going to go back to the usb hub
[121:06.84] and then i'm going to go back to the usb hub
[121:08.84] and then i'm going to go back to the usb hub
[121:10.84] and then i'm going to go back to the usb hub
[121:12.84] and then i'm going to go back to the usb hub
[121:14.84] and then i'm going to go back to the usb hub
[121:16.84] and then i'm going to go back to the usb hub
[121:18.84] and then i'm going to go back to the usb hub
[121:20.84] and then i'm going to go back to the usb hub
[121:22.84] and then i'm going to go back to the usb hub
[121:24.84] and then i'm going to go back to the usb hub
[121:26.84] and then i'm going to go back to the usb hub
[121:28.84] and then i'm going to go back to the usb hub
[121:30.84] and then i'm going to go back to the usb hub
[121:32.84] and then i'm going to go back to the usb hub
[121:34.84] and then i'm going to go back to the usb hub
[121:36.84] and then i'm going to go back to the usb hub
[121:38.84] and then i'm going to go back to the usb hub
[121:40.84] and then i'm going to go back to the usb hub
[121:42.84] and then i'm going to go back to the usb hub
[121:44.84] and then i'm going to go back to the usb hub
[121:46.84] and then i'm going to go back to the usb hub
[121:48.84] and then i'm going to go back to the usb hub
[121:50.84] and then i'm going to go back to the usb hub
[121:52.84] and then i'm going to go back to the usb hub
[121:54.84] and then i'm going to go back to the usb hub
[121:56.84] and then i'm going to go back to the usb hub
[121:58.84] and then i'm going to go back to the usb hub
[122:00.84] and then i'm going to go back to the usb hub
[122:02.84] and then i'm going to go back to the usb hub
[122:04.84] and then i'm going to go back to the usb hub
[122:06.84] and then i'm going to go back to the usb hub
[122:08.84] and then i'm going to go back to the usb hub
[122:10.84] and then i'm going to go back to the usb hub
[122:12.84] and then i'm going to go back to the usb hub
[122:14.84] and then i'm going to go back to the usb hub
[122:16.84] and then i'm going to go back to the usb hub
[122:18.84] and then i'm going to go back to the usb hub
[122:20.84] and then i'm going to go back to the usb hub
[122:22.84] and then i'm going to go back to the usb hub
[122:24.84] and then i'm going to go back to the usb hub
[122:26.84] and then i'm going to go back to the usb hub
[122:28.84] and then i'm going to go back to the usb hub
[122:30.84] and then i'm going to go back to the usb hub
[122:32.84] and then i'm going to go back to the usb hub
[122:34.84] and then i'm going to go back to the usb hub
[122:36.84] and then i'm going to go back to the usb hub
[122:38.84] and then i'm going to go back to the usb hub
[122:40.84] and then i'm going to go back to the usb hub
[122:42.84] and then i'm going to go back to the usb hub
[122:44.84] and then i'm going to go back to the usb hub
[122:46.84] and then i'm going to go back to the usb hub
[122:48.84] and then i'm going to go back to the usb hub
[122:50.84] and then i'm going to go back to the usb hub
[122:52.84] and then i'm going to go back to the usb hub
[122:54.84] and then i'm going to go back to the usb hub
[122:56.84] and then i'm going to go back to the usb hub
[122:58.84] and then i'm going to go back to the usb hub
[123:00.84] and then i'm going to go back to the usb hub
[123:02.84] and then i'm going to go back to the usb hub
[123:04.84] and then i'm going to go back to the usb hub
[123:06.84] and then i'm going to go back to the usb hub
[123:08.84] and then i'm going to go back to the usb hub
[123:10.84] and then i'm going to go back to the usb hub
[123:12.84] and then i'm going to go back to the usb hub
[123:14.84] and then i'm going to go back to the usb hub
[123:16.84] and then i'm going to go back to the usb hub
[123:18.84] and then i'm going to go back to the usb hub
[123:20.84] and then i'm going to go back to the usb hub
[123:22.84] and then i'm going to go back to the usb hub
[123:24.84] and then i'm going to go back to the usb hub
[123:26.84] and then i'm going to go back to the usb hub
[123:28.84] and then i'm going to go back to the usb hub
[123:30.84] and then i'm going to go back to the usb hub
[123:32.84] and then i'm going to go back to the usb hub
[123:34.84] and then i'm going to go back to the usb hub
[123:36.84] and then i'm going to go back to the usb hub
[123:38.84] and then i'm going to go back to the usb hub
[123:40.84] and then i'm going to go back to the usb hub
[123:42.84] and then i'm going to go back to the usb hub
[123:44.84] and then i'm going to go back to the usb hub
[123:46.84] and then i'm going to go back to the usb hub
[123:48.84] and then i'm going to go back to the usb hub
[123:50.84] and then i'm going to go back to the usb hub
[123:52.84] and then i'm going to go back to the usb hub
[123:54.84] and then i'm going to go back to the usb hub
[123:56.84] and then i'm going to go back to the usb hub
[123:58.84] and then i'm going to go back to the usb hub
[124:00.84] and then i'm going to go back to the usb hub
[124:02.84] and then i'm going to go back to the usb hub
[124:04.84] and then i'm going to go back to the usb hub
[124:06.84] and then i'm going to go back to the usb hub
[124:08.84] and then i'm going to go back to the usb hub
[124:10.84] and then i'm going to go back to the usb hub
[124:12.84] and then i'm going to go back to the usb hub
[124:14.84] and then i'm going to go back to the usb hub
[124:16.84] and then i'm going to go back to the usb hub
[124:18.84] and then i'm going to go back to the usb hub
[124:20.84] and then i'm going to go back to the usb hub
[124:22.84] and then i'm going to go back to the usb hub
[124:24.84] and then i'm going to go back to the usb hub
[124:26.84] and then i'm going to go back to the usb hub
[124:28.84] and then i'm going to go back to the usb hub
[124:30.84] and then i'm going to go back to the usb hub
[124:32.84] and then i'm going to go back to the usb hub
[124:34.84] and then i'm going to go back to the usb hub
[124:36.84] and then i'm going to go back to the usb hub
[124:38.84] and then i'm going to go back to the usb hub
[124:40.84] and then i'm going to go back to the usb hub
[124:42.84] and then i'm going to go back to the usb hub
[124:44.84] and then i'm going to go back to the usb hub
[124:46.84] and then i'm going to go back to the usb hub
[124:48.84] and then i'm going to go back to the usb hub
[124:50.84] and then i'm going to go back to the usb hub
[124:52.84] and then i'm going to go back to the usb hub
[124:54.84] and then i'm going to go back to the usb hub
[124:56.84] and then i'm going to go back to the usb hub
[124:58.84] and then i'm going to go back to the usb hub
[125:00.84] and then i'm going to go back to the usb hub
[125:02.84] and then i'm going to go back to the usb hub
[125:04.84] and then i'm going to go back to the usb hub
[125:06.84] and then i'm going to go back to the usb hub
[125:08.84] and then i'm going to go back to the usb hub
[125:10.84] and then i'm going to go back to the usb hub
[125:12.84] and then i'm going to go back to the usb hub
[125:14.84] and then i'm going to go back to the usb hub
[125:16.84] and then i'm going to go back to the usb hub
[125:18.84] and then i'm going to go back to the usb hub
[125:20.84] and then i'm going to go back to the usb hub
[125:22.84] and then i'm going to go back to the usb hub
[125:24.84] and then i'm going to go back to the usb hub
[125:26.84] and then i'm going to go back to the usb hub
[125:28.84] and then i'm going to go back to the usb hub
[125:30.84] and then i'm going to go back to the usb hub
[125:32.84] and then i'm going to go back to the usb hub
[125:34.84] and then i'm going to go back to the usb hub
[125:36.84] and then i'm going to go back to the usb hub
[125:38.84] and then i'm going to go back to the usb hub
[125:40.84] and then i'm going to go back to the usb hub
[125:42.84] and then i'm going to go back to the usb hub
[125:44.84] and then i'm going to go back to the usb hub
[125:46.84] and then i'm going to go back to the usb hub
[125:48.84] and then i'm going to go back to the usb hub
[125:50.84] and then i'm going to go back to the usb hub
[125:52.84] and then i'm going to go back to the usb hub
[125:54.84] and then i'm going to go back to the usb hub
[125:56.84] and then i'm going to go back to the usb hub
[125:58.84] and then i'm going to go back to the usb hub
[126:00.84] and then i'm going to go back to the usb hub
[126:02.84] and then i'm going to go back to the usb hub
[126:04.84] and then i'm going to go back to the usb hub
[126:06.84] and then i'm going to go back to the usb hub
[126:08.84] and then i'm going to go back to the usb hub
[126:10.84] and then i'm going to go back to the usb hub
[126:12.84] and then i'm going to go back to the usb hub
[126:14.84] and then i'm going to go back to the usb hub
[126:16.84] and then i'm going to go back to the usb hub
[126:18.84] and then i'm going to go back to the usb hub
[126:20.84] and then i'm going to go back to the usb hub
[126:22.84] and then i'm going to go back to the usb hub
[126:24.84] and then i'm going to go back to the usb hub
[126:26.84] and then i'm going to go back to the usb hub
[126:28.84] and then i'm going to go back to the usb hub
[126:30.84] and then i'm going to go back to the usb hub
[126:32.84] and then i'm going to go back to the usb hub
[126:34.84] and then i'm going to go back to the usb hub
[126:36.84] and then i'm going to go back to the usb hub
[126:38.84] and then i'm going to go back to the usb hub
[126:40.84] and then i'm going to go back to the usb hub
[126:42.84] and then i'm going to go back to the usb hub
[126:44.84] and then i'm going to go back to the usb hub
[126:46.84] and then i'm going to go back to the usb hub
[126:48.84] and then i'm going to go back to the usb hub
[126:50.84] and then i'm going to go back to the usb hub
[126:52.84] and then i'm going to go back to the usb hub
[126:54.84] and then i'm going to go back to the usb hub
[126:56.84] and then i'm going to go back to the usb hub
[126:58.84] and then i'm going to go back to the usb hub
[127:00.84] and then i'm going to go back to the usb hub
[127:02.84] and then i'm going to go back to the usb hub
[127:04.84] and then i'm going to go back to the usb hub
[127:06.84] and then i'm going to go back to the usb hub
[127:08.84] and then i'm going to go back to the usb hub
[127:10.84] and then i'm going to go back to the usb hub
[127:12.84] and then i'm going to go back to the usb hub
[127:14.84] and then i'm going to go back to the usb hub
[127:16.84] and then i'm going to go back to the usb hub
[127:18.84] and then i'm going to go back to the usb hub
[127:20.84] and then i'm going to go back to the usb hub
[127:22.84] and then i'm going to go back to the usb hub
[127:24.84] and then i'm going to go back to the usb hub
[127:26.84] and then i'm going to go back to the usb hub
[127:28.84] and then i'm going to go back to the usb hub
[127:30.84] and then i'm going to go back to the usb hub
[127:32.84] and then i'm going to go back to the usb hub
[127:34.84] and then i'm going to go back to the usb hub
[127:36.84] and then i'm going to go back to the usb hub
[127:38.84] and then i'm going to go back to the usb hub
[127:40.84] and then i'm going to go back to the usb hub
[127:42.84] and then i'm going to go back to the usb hub
[127:44.84] and then i'm going to go back to the usb hub
[127:46.84] and then i'm going to go back to the usb hub
[127:48.84] and then i'm going to go back to the usb hub
[127:50.84] and then i'm going to go back to the usb hub
[127:52.84] and then i'm going to go back to the usb hub
[127:54.84] and then i'm going to go back to the usb hub
[127:56.84] and then i'm going to go back to the usb hub
[127:58.84] and then i'm going to go back to the usb hub
[128:00.84] and then i'm going to go back to the usb hub
[128:02.84] and then i'm going to go back to the usb hub
[128:04.84] and then i'm going to go back to the usb hub
[128:06.84] and then i'm going to go back to the usb hub
[128:08.84] and then i'm going to go back to the usb hub
[128:10.84] and then i'm going to go back to the usb hub
[128:12.84] and then i'm going to go back to the usb hub
[128:14.84] and then i'm going to go back to the usb hub
[128:16.84] and then i'm going to go back to the usb hub
[128:18.84] and then i'm going to go back to the usb hub
[128:20.84] and then i'm going to go back to the usb hub
[128:22.84] and then i'm going to go back to the usb hub
[128:24.84] and then i'm going to go back to the usb hub
[128:26.84] and then i'm going to go back to the usb hub
[128:28.84] and then i'm going to go back to the usb hub
[128:30.84] and then i'm going to go back to the usb hub
[128:32.84] and then i'm going to go back to the usb hub
[128:34.84] and then i'm going to go back to the usb hub
[128:36.84] and then i'm going to go back to the usb hub
[128:38.84] and then i'm going to go back to the usb hub
[128:40.84] and then i'm going to go back to the usb hub
[128:42.84] and then i'm going to go back to the usb hub
[128:44.84] and then i'm going to go back to the usb hub
[128:46.84] and then i'm going to go back to the usb hub
[128:48.84] and then i'm going to go back to the usb hub
[128:50.84] and then i'm going to go back to the usb hub
[128:52.84] and then i'm going to go back to the usb hub
[128:54.84] and then i'm going to go back to the usb hub
[128:56.84] and then i'm going to go back to the usb hub
[128:58.84] and then i'm going to go back to the usb hub
[129:00.84] and then i'm going to go back to the usb hub
[129:02.84] and then i'm going to go back to the usb hub
[129:04.84] and then i'm going to go back to the usb hub
[129:06.84] and then i'm going to go back to the usb hub
[129:08.84] and then i'm going to go back to the usb hub
[129:10.84] and then i'm going to go back to the usb hub
[129:12.84] and then i'm going to go back to the usb hub
[129:14.84] and then i'm going to go back to the usb hub
[129:16.84] and then i'm going to go back to the usb hub
[129:18.84] and then i'm going to go back to the usb hub
[129:20.84] and then i'm going to go back to the usb hub
[129:22.84] and then i'm going to go back to the usb hub
[129:24.84] and then i'm going to go back to the usb hub
[129:26.84] and then i'm going to go back to the usb hub
[129:28.84] and then i'm going to go back to the usb hub
[129:30.84] and then i'm going to go back to the usb hub
[129:32.84] and then i'm going to go back to the usb hub
[129:34.84] and then i'm going to go back to the usb hub
[129:36.84] and then i'm going to go back to the usb hub
[129:38.84] and then i'm going to go back to the usb hub
[129:40.84] and then i'm going to go back to the usb hub
[129:42.84] and then i'm going to go back to the usb hub
[129:44.84] and then i'm going to go back to the usb hub
[129:46.84] and then i'm going to go back to the usb hub
[129:48.84] and then i'm going to go back to the usb hub
[129:50.84] and then i'm going to go back to the usb hub
[129:52.84] and then i'm going to go back to the usb hub
[129:54.84] and then i'm going to go back to the usb hub
[129:56.84] and then i'm going to go back to the usb hub
[129:58.84] and then i'm going to go back to the usb hub
[130:00.84] and then i'm going to go back to the usb hub
[130:02.84] and then i'm going to go back to the usb hub
[130:04.84] and then i'm going to go back to the usb hub
[130:06.84] and then i'm going to go back to the usb hub
[130:08.84] and then i'm going to go back to the usb hub
[130:10.84] and then i'm going to go back to the usb hub
[130:12.84] and then i'm going to go back to the usb hub
[130:14.84] and then i'm going to go back to the usb hub
[130:16.84] and then i'm going to go back to the usb hub
[130:18.84] and then i'm going to go back to the usb hub
[130:20.84] and then i'm going to go back to the usb hub
[130:22.84] and then i'm going to go back to the usb hub
[130:24.84] and then i'm going to go back to the usb hub
[130:26.84] and then i'm going to go back to the usb hub
[130:28.84] and then i'm going to go back to the usb hub
[130:30.84] and then i'm going to go back to the usb hub
[130:32.84] and then i'm going to go back to the usb hub
[130:34.84] and then i'm going to go back to the usb hub
[130:36.84] and then i'm going to go back to the usb hub
[130:38.84] and then i'm going to go back to the usb hub
[130:40.84] and then i'm going to go back to the usb hub
[130:42.84] and then i'm going to go back to the usb hub
[130:44.84] and then i'm going to go back to the usb hub
[130:46.84] and then i'm going to go back to the usb hub
[130:48.84] and then i'm going to go back to the usb hub
[130:50.84] and then i'm going to go back to the usb hub
[130:52.84] and then i'm going to go back to the usb hub
[130:54.84] and then i'm going to go back to the usb hub
[130:56.84] and then i'm going to go back to the usb hub
[130:58.84] and then i'm going to go back to the usb hub
[131:00.84] and then i'm going to go back to the usb hub
[131:02.84] and then i'm going to go back to the usb hub
[131:04.84] and then i'm going to go back to the usb hub
[131:06.84] and then i'm going to go back to the usb hub
[131:08.84] and then i'm going to go back to the usb hub
[131:10.84] and then i'm going to go back to the usb hub
[131:12.84] and then i'm going to go back to the usb hub
[131:14.84] and then i'm going to go back to the usb hub
[131:16.84] and then i'm going to go back to the usb hub
[131:18.84] and then i'm going to go back to the usb hub
[131:20.84] and then i'm going to go back to the usb hub
[131:22.84] and then i'm going to go back to the usb hub
[131:24.84] and then i'm going to go back to the usb hub
[131:26.84] and then i'm going to go back to the usb hub
[131:28.84] and then i'm going to go back to the usb hub
[131:30.84] and then i'm going to go back to the usb hub
[131:32.84] and then i'm going to go back to the usb hub
[131:34.84] and then i'm going to go back to the usb hub
[131:36.84] and then i'm going to go back to the usb hub
[131:38.84] and then i'm going to go back to the usb hub
[131:40.84] and then i'm going to go back to the usb hub
[131:42.84] and then i'm going to go back to the usb hub
[131:44.84] and then i'm going to go back to the usb hub
[131:46.84] and then i'm going to go back to the usb hub
[131:48.84] and then i'm going to go back to the usb hub
[131:50.84] and then i'm going to go back to the usb hub
[131:52.84] and then i'm going to go back to the usb hub
[131:54.84] and then i'm going to go back to the usb hub
[131:56.84] and then i'm going to go back to the usb hub
[131:58.84] and then i'm going to go back to the usb hub
[132:00.84] and then i'm going to go back to the usb hub
[132:02.84] and then i'm going to go back to the usb hub
[132:04.84] and then i'm going to go back to the usb hub
[132:06.84] and then i'm going to go back to the usb hub
[132:08.84] and then i'm going to go back to the usb hub
[132:10.84] and then i'm going to go back to the usb hub
[132:12.84] and then i'm going to go back to the usb hub
[132:14.84] and then i'm going to go back to the usb hub
[132:16.84] and then i'm going to go back to the usb hub
[132:18.84] and then i'm going to go back to the usb hub
[132:20.84] and then i'm going to go back to the usb hub
[132:22.84] and then i'm going to go back to the usb hub
[132:24.84] and then i'm going to go back to the usb hub
[132:26.84] and then i'm going to go back to the usb hub
[132:28.84] and then i'm going to go back to the usb hub
[132:30.84] and then i'm going to go back to the usb hub
[132:32.84] and then i'm going to go back to the usb hub
[132:34.84] and then i'm going to go back to the usb hub
[132:36.84] and then i'm going to go back to the usb hub
[132:38.84] and then i'm going to go back to the usb hub
[132:40.84] and then i'm going to go back to the usb hub
[132:42.84] and then i'm going to go back to the usb hub
[132:44.84] and then i'm going to go back to the usb hub
[132:46.84] and then i'm going to go back to the usb hub
[132:48.84] and then i'm going to go back to the usb hub
[132:50.84] and then i'm going to go back to the usb hub
[132:52.84] and then i'm going to go back to the usb hub
[132:54.84] and then i'm going to go back to the usb hub
[132:56.84] and then i'm going to go back to the usb hub
[132:58.84] and then i'm going to go back to the usb hub
[133:00.84] and then i'm going to go back to the usb hub
[133:02.84] and then i'm going to go back to the usb hub
[133:04.84] and then i'm going to go back to the usb hub
[133:06.84] and then i'm going to go back to the usb hub
[133:08.84] and then i'm going to go back to the usb hub
[133:10.84] and then i'm going to go back to the usb hub
[133:12.84] and then i'm going to go back to the usb hub
[133:14.84] and then i'm going to go back to the usb hub
[133:16.84] and then i'm going to go back to the usb hub
[133:18.84] and then i'm going to go back to the usb hub
[133:20.84] and then i'm going to go back to the usb hub
[133:22.84] and then i'm going to go back to the usb hub
[133:24.84] and then i'm going to go back to the usb hub
[133:26.84] and then i'm going to go back to the usb hub
[133:28.84] and then i'm going to go back to the usb hub
[133:30.84] and then i'm going to go back to the usb hub
[133:32.84] and then i'm going to go back to the usb hub
[133:34.84] and then i'm going to go back to the usb hub
[133:36.84] and then i'm going to go back to the usb hub
[133:38.84] and then i'm going to go back to the usb hub
[133:40.84] and then i'm going to go back to the usb hub
[133:42.84] and then i'm going to go back to the usb hub
[133:44.84] and then i'm going to go back to the usb hub
[133:46.84] and then i'm going to go back to the usb hub
[133:48.84] and then i'm going to go back to the usb hub
[133:50.84] and then i'm going to go back to the usb hub
[133:52.84] and then i'm going to go back to the usb hub
[133:54.84] and then i'm going to go back to the usb hub
[133:56.84] and then i'm going to go back to the usb hub
[133:58.84] and then i'm going to go back to the usb hub
[134:00.84] and then i'm going to go back to the usb hub
[134:02.84] and then i'm going to go back to the usb hub
[134:04.84] and then i'm going to go back to the usb hub
[134:06.84] and then i'm going to go back to the usb hub
[134:08.84] and then i'm going to go back to the usb hub
[134:10.84] and then i'm going to go back to the usb hub
[134:12.84] and then i'm going to go back to the usb hub
[134:14.84] and then i'm going to go back to the usb hub
[134:16.84] and then i'm going to go back to the usb hub
[134:18.84] and then i'm going to go back to the usb hub
[134:20.84] and then i'm going to go back to the usb hub
[134:22.84] and then i'm going to go back to the usb hub
[134:24.84] and then i'm going to go back to the usb hub
[134:26.84] and then i'm going to go back to the usb hub
[134:28.84] and then i'm going to go back to the usb hub
[134:30.84] and then i'm going to go back to the usb hub
[134:32.84] and then i'm going to go back to the usb hub
[134:34.84] and then i'm going to go back to the usb hub
[134:36.84] and then i'm going to go back to the usb hub
[134:38.84] and then i'm going to go back to the usb hub
[134:40.84] and then i'm going to go back to the usb hub
[134:42.84] and then i'm going to go back to the usb hub
[134:44.84] and then i'm going to go back to the usb hub
[134:46.84] and then i'm going to go back to the usb hub
[134:48.84] and then i'm going to go back to the usb hub
[134:50.84] and then i'm going to go back to the usb hub
[134:52.84] and then i'm going to go back to the usb hub
[134:54.84] and then i'm going to go back to the usb hub
[134:56.84] and then i'm going to go back to the usb hub
[134:58.84] and then i'm going to go back to the usb hub
[135:00.84] and then i'm going to go back to the usb hub
[135:02.84] and then i'm going to go back to the usb hub
[135:04.84] and then i'm going to go back to the usb hub
[135:06.84] and then i'm going to go back to the usb hub
[135:08.84] and then i'm going to go back to the usb hub
[135:10.84] and then i'm going to go back to the usb hub
[135:12.84] and then i'm going to go back to the usb hub
[135:14.84] and then i'm going to go back to the usb hub
[135:16.84] and then i'm going to go back to the usb hub
[135:18.84] and then i'm going to go back to the usb hub
[135:20.84] and then i'm going to go back to the usb hub
[135:22.84] and then i'm going to go back to the usb hub
[135:24.84] and then i'm going to go back to the usb hub
[135:26.84] and then i'm going to go back to the usb hub
[135:28.84] and then i'm going to go back to the usb hub
[135:30.84] and then i'm going to go back to the usb hub
[135:32.84] and then i'm going to go back to the usb hub
[135:34.84] and then i'm going to go back to the usb hub
[135:36.84] and then i'm going to go back to the usb hub
[135:38.84] and then i'm going to go back to the usb hub
[135:40.84] and then i'm going to go back to the usb hub
[135:42.84] and then i'm going to go back to the usb hub
[135:44.84] and then i'm going to go back to the usb hub
[135:46.84] and then i'm going to go back to the usb hub
[135:48.84] and then i'm going to go back to the usb hub
[135:50.84] and then i'm going to go back to the usb hub
[135:52.84] and then i'm going to go back to the usb hub
[135:54.84] and then i'm going to go back to the usb hub
[135:56.84] and then i'm going to go back to the usb hub
[135:58.84] and then i'm going to go back to the usb hub
[136:00.84] and then i'm going to go back to the usb hub
[136:02.84] and then i'm going to go back to the usb hub
[136:04.84] and then i'm going to go back to the usb hub
[136:06.84] and then i'm going to go back to the usb hub
[136:08.84] and then i'm going to go back to the usb hub
[136:10.84] and then i'm going to go back to the usb hub
[136:12.84] and then i'm going to go back to the usb hub
[136:14.84] and then i'm going to go back to the usb hub
[136:16.84] and then i'm going to go back to the usb hub
[136:18.84] and then i'm going to go back to the usb hub
[136:20.84] and then i'm going to go back to the usb hub
[136:22.84] and then i'm going to go back to the usb hub
[136:24.84] and then i'm going to go back to the usb hub
[136:26.84] and then i'm going to go back to the usb hub
[136:28.84] and then i'm going to go back to the usb hub
[136:30.84] and then i'm going to go back to the usb hub
[136:32.84] and then i'm going to go back to the usb hub
[136:34.84] and then i'm going to go back to the usb hub
[136:36.84] and then i'm going to go back to the usb hub
[136:38.84] and then i'm going to go back to the usb hub
[136:40.84] and then i'm going to go back to the usb hub
[136:42.84] and then i'm going to go back to the usb hub
[136:44.84] and then i'm going to go back to the usb hub
[136:46.84] and then i'm going to go back to the usb hub
[136:48.84] and then i'm going to go back to the usb hub
[136:50.84] and then i'm going to go back to the usb hub
[136:52.84] and then i'm going to go back to the usb hub
[136:54.84] and then i'm going to go back to the usb hub
[136:56.84] and then i'm going to go back to the usb hub
[136:58.84] and then i'm going to go back to the usb hub
[137:00.84] and then i'm going to go back to the usb hub
[137:02.84] and then i'm going to go back to the usb hub
[137:04.84] and then i'm going to go back to the usb hub
[137:06.84] and then i'm going to go back to the usb hub
[137:08.84] and then i'm going to go back to the usb hub
[137:10.84] and then i'm going to go back to the usb hub
[137:12.84] and then i'm going to go back to the usb hub
[137:14.84] and then i'm going to go back to the usb hub
[137:16.84] and then i'm going to go back to the usb hub
[137:18.84] and then i'm going to go back to the usb hub
[137:20.84] and then i'm going to go back to the usb hub
[137:22.84] and then i'm going to go back to the usb hub
[137:24.84] and then i'm going to go back to the usb hub
[137:26.84] and then i'm going to go back to the usb hub
[137:28.84] and then i'm going to go back to the usb hub
[137:30.84] and then i'm going to go back to the usb hub
[137:32.84] and then i'm going to go back to the usb hub
[137:34.84] and then i'm going to go back to the usb hub
[137:36.84] and then i'm going to go back to the usb hub
[137:38.84] and then i'm going to go back to the usb hub
[137:40.84] and then i'm going to go back to the usb hub
[137:42.84] and then i'm going to go back to the usb hub
[137:44.84] and then i'm going to go back to the usb hub
[137:46.84] and then i'm going to go back to the usb hub
[137:48.84] and then i'm going to go back to the usb hub
[137:50.84] and then i'm going to go back to the usb hub
[137:52.84] and then i'm going to go back to the usb hub
[137:54.84] and then i'm going to go back to the usb hub
[137:56.84] and then i'm going to go back to the usb hub
[137:58.84] and then i'm going to go back to the usb hub
[138:00.84] and then i'm going to go back to the usb hub
[138:02.84] and then i'm going to go back to the usb hub
[138:04.84] and then i'm going to go back to the usb hub
[138:06.84] and then i'm going to go back to the usb hub
[138:08.84] and then i'm going to go back to the usb hub
[138:10.84] and then i'm going to go back to the usb hub
[138:12.84] and then i'm going to go back to the usb hub
[138:14.84] and then i'm going to go back to the usb hub
[138:16.84] and then i'm going to go back to the usb hub
[138:18.84] and then i'm going to go back to the usb hub
[138:20.84] and then i'm going to go back to the usb hub
[138:22.84] and then i'm going to go back to the usb hub
[138:24.84] and then i'm going to go back to the usb hub
[138:26.84] and then i'm going to go back to the usb hub
[138:28.84] and then i'm going to go back to the usb hub
[138:30.84] and then i'm going to go back to the usb hub
[138:32.84] and then i'm going to go back to the usb hub
[138:34.84] and then i'm going to go back to the usb hub
[138:36.84] and then i'm going to go back to the usb hub
[138:38.84] and then i'm going to go back to the usb hub
[138:40.84] and then i'm going to go back to the usb hub
[138:42.84] and then i'm going to go back to the usb hub
[138:44.84] and then i'm going to go back to the usb hub
[138:46.84] and then i'm going to go back to the usb hub
[138:48.84] and then i'm going to go back to the usb hub
[138:50.84] and then i'm going to go back to the usb hub
[138:52.84] and then i'm going to go back to the usb hub
[138:54.84] and then i'm going to go back to the usb hub
[138:56.84] and then i'm going to go back to the usb hub
[138:58.84] and then i'm going to go back to the usb hub
[139:00.84] and then i'm going to go back to the usb hub
[139:02.84] and then i'm going to go back to the usb hub
[139:04.84] and then i'm going to go back to the usb hub
[139:06.84] and then i'm going to go back to the usb hub
[139:08.84] and then i'm going to go back to the usb hub
[139:10.84] and then i'm going to go back to the usb hub
[139:12.84] and then i'm going to go back to the usb hub
[139:14.84] and then i'm going to go back to the usb hub
[139:16.84] and then i'm going to go back to the usb hub
[139:18.84] and then i'm going to go back to the usb hub
[139:20.84] and then i'm going to go back to the usb hub
[139:22.84] and then i'm going to go back to the usb hub
[139:24.84] and then i'm going to go back to the usb hub
[139:26.84] and then i'm going to go back to the usb hub
[139:28.84] and then i'm going to go back to the usb hub
[139:30.84] and then i'm going to go back to the usb hub
[139:32.84] and then i'm going to go back to the usb hub
[139:34.84] and then i'm going to go back to the usb hub
[139:36.84] and then i'm going to go back to the usb hub
[139:38.84] and then i'm going to go back to the usb hub
[139:40.84] and then i'm going to go back to the usb hub
[139:42.84] and then i'm going to go back to the usb hub
[139:44.84] and then i'm going to go back to the usb hub
[139:46.84] and then i'm going to go back to the usb hub
[139:48.84] and then i'm going to go back to the usb hub
[139:50.84] and then i'm going to go back to the usb hub
[139:52.84] and then i'm going to go back to the usb hub
[139:54.84] and then i'm going to go back to the usb hub
[139:56.84] and then i'm going to go back to the usb hub
[139:58.84] and then i'm going to go back to the usb hub
[140:00.84] and then i'm going to go back to the usb hub
[140:02.84] and then i'm going to go back to the usb hub
[140:04.84] and then i'm going to go back to the usb hub
[140:06.84] and then i'm going to go back to the usb hub
[140:08.84] and then i'm going to go back to the usb hub
[140:10.84] and then i'm going to go back to the usb hub
[140:12.84] and then i'm going to go back to the usb hub
[140:14.84] and then i'm going to go back to the usb hub
[140:16.84] and then i'm going to go back to the usb hub
[140:18.84] and then i'm going to go back to the usb hub
[140:20.84] and then i'm going to go back to the usb hub
[140:22.84] and then i'm going to go back to the usb hub
[140:24.84] and then i'm going to go back to the usb hub
[140:26.84] and then i'm going to go back to the usb hub
[140:28.84] and then i'm going to go back to the usb hub
[140:30.84] and then i'm going to go back to the usb hub
[140:32.84] and then i'm going to go back to the usb hub
[140:34.84] and then i'm going to go back to the usb hub
[140:36.84] and then i'm going to go back to the usb hub
[140:38.84] and then i'm going to go back to the usb hub
[140:40.84] and then i'm going to go back to the usb hub
[140:42.84] and then i'm going to go back to the usb hub
[140:44.84] and then i'm going to go back to the usb hub
[140:46.84] and then i'm going to go back to the usb hub
[140:48.84] and then i'm going to go back to the usb hub
[140:50.84] and then i'm going to go back to the usb hub
[140:52.84] and then i'm going to go back to the usb hub
[140:54.84] and then i'm going to go back to the usb hub
[140:56.84] and then i'm going to go back to the usb hub
[140:58.84] and then i'm going to go back to the usb hub
[141:00.84] and then i'm going to go back to the usb hub
[141:02.84] and then i'm going to go back to the usb hub
[141:04.84] and then i'm going to go back to the usb hub
[141:06.84] and then i'm going to go back to the usb hub
[141:08.84] and then i'm going to go back to the usb hub
[141:10.84] and then i'm going to go back to the usb hub
[141:12.84] and then i'm going to go back to the usb hub
[141:14.84] and then i'm going to go back to the usb hub
[141:16.84] and then i'm going to go back to the usb hub
[141:18.84] and then i'm going to go back to the usb hub
[141:20.84] and then i'm going to go back to the usb hub
[141:22.84] and then i'm going to go back to the usb hub
[141:24.84] and then i'm going to go back to the usb hub
[141:26.84] and then i'm going to go back to the usb hub
[141:28.84] and then i'm going to go back to the usb hub
[141:30.84] and then i'm going to go back to the usb hub
[141:32.84] and then i'm going to go back to the usb hub
[141:34.84] and then i'm going to go back to the usb hub
[141:36.84] and then i'm going to go back to the usb hub
[141:38.84] and then i'm going to go back to the usb hub
[141:40.84] and then i'm going to go back to the usb hub
[141:42.84] and then i'm going to go back to the usb hub
[141:44.84] and then i'm going to go back to the usb hub
[141:46.84] and then i'm going to go back to the usb hub
[141:48.84] and then i'm going to go back to the usb hub
[141:50.84] and then i'm going to go back to the usb hub
[141:52.84] and then i'm going to go back to the usb hub
[141:54.84] and then i'm going to go back to the usb hub
[141:56.84] and then i'm going to go back to the usb hub
[141:58.84] and then i'm going to go back to the usb hub
[142:00.84] and then i'm going to go back to the usb hub
[142:02.84] and then i'm going to go back to the usb hub
[142:04.84] and then i'm going to go back to the usb hub
[142:06.84] and then i'm going to go back to the usb hub
[142:08.84] and then i'm going to go back to the usb hub
[142:10.84] and then i'm going to go back to the usb hub
[142:12.84] and then i'm going to go back to the usb hub
[142:14.84] and then i'm going to go back to the usb hub
[142:16.84] and then i'm going to go back to the usb hub
[142:18.84] and then i'm going to go back to the usb hub
[142:20.84] and then i'm going to go back to the usb hub
[142:22.84] and then i'm going to go back to the usb hub
[142:24.84] and then i'm going to go back to the usb hub
[142:26.84] and then i'm going to go back to the usb hub
[142:28.84] and then i'm going to go back to the usb hub
[142:30.84] and then i'm going to go back to the usb hub
[142:32.84] and then i'm going to go back to the usb hub
[142:34.84] and then i'm going to go back to the usb hub
[142:36.84] and then i'm going to go back to the usb hub
[142:38.84] and then i'm going to go back to the usb hub
[142:40.84] and then i'm going to go back to the usb hub
[142:42.84] and then i'm going to go back to the usb hub
[142:44.84] and then i'm going to go back to the usb hub
[142:46.84] and then i'm going to go back to the usb hub
[142:48.84] and then i'm going to go back to the usb hub
[142:50.84] and then i'm going to go back to the usb hub
[142:52.84] and then i'm going to go back to the usb hub
[142:54.84] and then i'm going to go back to the usb hub
[142:56.84] and then i'm going to go back to the usb hub
[142:58.84] and then i'm going to go back to the usb hub
[143:00.84] and then i'm going to go back to the usb hub
[143:02.84] and then i'm going to go back to the usb hub
[143:04.84] and then i'm going to go back to the usb hub
[143:06.84] and then i'm going to go back to the usb hub
[143:08.84] and then i'm going to go back to the usb hub
[143:10.84] and then i'm going to go back to the usb hub
[143:12.84] and then i'm going to go back to the usb hub
[143:14.84] and then i'm going to go back to the usb hub
[143:16.84] and then i'm going to go back to the usb hub
[143:18.84] and then i'm going to go back to the usb hub
[143:20.84] and then i'm going to go back to the usb hub
[143:22.84] and then i'm going to go back to the usb hub
[143:24.84] and then i'm going to go back to the usb hub
[143:26.84] and then i'm going to go back to the usb hub
[143:28.84] and then i'm going to go back to the usb hub
[143:30.84] and then i'm going to go back to the usb hub
[143:32.84] and then i'm going to go back to the usb hub
[143:34.84] and then i'm going to go back to the usb hub
[143:36.84] and then i'm going to go back to the usb hub
[143:38.84] and then i'm going to go back to the usb hub
[143:40.84] and then i'm going to go back to the usb hub
[143:42.84] and then i'm going to go back to the usb hub
[143:44.84] and then i'm going to go back to the usb hub
[143:46.84] and then i'm going to go back to the usb hub
[143:48.84] and then i'm going to go back to the usb hub
[143:50.84] and then i'm going to go back to the usb hub
[143:52.84] and then i'm going to go back to the usb hub
[143:54.84] and then i'm going to go back to the usb hub
[143:56.84] and then i'm going to go back to the usb hub
[143:58.84] and then i'm going to go back to the usb hub
[144:00.84] and then i'm going to go back to the usb hub
[144:02.84] and then i'm going to go back to the usb hub
[144:04.84] and then i'm going to go back to the usb hub
[144:06.84] and then i'm going to go back to the usb hub
[144:08.84] and then i'm going to go back to the usb hub
[144:10.84] and then i'm going to go back to the usb hub
[144:12.84] and then i'm going to go back to the usb hub
[144:14.84] and then i'm going to go back to the usb hub
[144:16.84] and then i'm going to go back to the usb hub
[144:18.84] and then i'm going to go back to the usb hub
[144:20.84] and then i'm going to go back to the usb hub
[144:22.84] and then i'm going to go back to the usb hub
[144:24.84] and then i'm going to go back to the usb hub
[144:26.84] and then i'm going to go back to the usb hub
[144:28.84] and then i'm going to go back to the usb hub
[144:30.84] and then i'm going to go back to the usb hub
[144:32.84] and then i'm going to go back to the usb hub
[144:34.84] and then i'm going to go back to the usb hub
[144:36.84] and then i'm going to go back to the usb hub
[144:38.84] and then i'm going to go back to the usb hub
[144:40.84] and then i'm going to go back to the usb hub
[144:42.84] and then i'm going to go back to the usb hub
[144:44.84] and then i'm going to go back to the usb hub
[144:46.84] and then i'm going to go back to the usb hub
[144:48.84] and then i'm going to go back to the usb hub
[144:50.84] and then i'm going to go back to the usb hub
[144:52.84] and then i'm going to go back to the usb hub
[144:54.84] and then i'm going to go back to the usb hub
[144:56.84] and then i'm going to go back to the usb hub
[144:58.84] and then i'm going to go back to the usb hub
[145:00.84] and then i'm going to go back to the usb hub
[145:02.84] and then i'm going to go back to the usb hub
[145:04.84] and then i'm going to go back to the usb hub
[145:06.84] and then i'm going to go back to the usb hub
[145:08.84] and then i'm going to go back to the usb hub
[145:10.84] and then i'm going to go back to the usb hub
[145:12.84] and then i'm going to go back to the usb hub
[145:14.84] and then i'm going to go back to the usb hub
[145:16.84] and then i'm going to go back to the usb hub
[145:18.84] and then i'm going to go back to the usb hub
[145:20.84] and then i'm going to go back to the usb hub
[145:22.84] and then i'm going to go back to the usb hub
[145:24.84] and then i'm going to go back to the usb hub
[145:26.84] and then i'm going to go back to the usb hub
[145:28.84] and then i'm going to go back to the usb hub
[145:30.84] and then i'm going to go back to the usb hub
[145:32.84] and then i'm going to go back to the usb hub
[145:34.84] and then i'm going to go back to the usb hub
[145:36.84] and then i'm going to go back to the usb hub
[145:38.84] and then i'm going to go back to the usb hub
[145:40.84] and then i'm going to go back to the usb hub
[145:42.84] and then i'm going to go back to the usb hub
[145:44.84] and then i'm going to go back to the usb hub
[145:46.84] and then i'm going to go back to the usb hub
[145:48.84] and then i'm going to go back to the usb hub
[145:50.84] and then i'm going to go back to the usb hub
[145:52.84] and then i'm going to go back to the usb hub
[145:54.84] and then i'm going to go back to the usb hub
[145:56.84] and then i'm going to go back to the usb hub
[145:58.84] and then i'm going to go back to the usb hub
[146:00.84] and then i'm going to go back to the usb hub
[146:02.84] and then i'm going to go back to the usb hub
[146:04.84] and then i'm going to go back to the usb hub
[146:06.84] and then i'm going to go back to the usb hub
[146:08.84] and then i'm going to go back to the usb hub
[146:10.84] and then i'm going to go back to the usb hub
[146:12.84] and then i'm going to go back to the usb hub
[146:14.84] and then i'm going to go back to the usb hub
[146:16.84] and then i'm going to go back to the usb hub
[146:18.84] and then i'm going to go back to the usb hub
[146:20.84] and then i'm going to go back to the usb hub
[146:22.84] and then i'm going to go back to the usb hub
[146:24.84] and then i'm going to go back to the usb hub
[146:26.84] and then i'm going to go back to the usb hub
[146:28.84] and then i'm going to go back to the usb hub
[146:30.84] and then i'm going to go back to the usb hub
[146:32.84] and then i'm going to go back to the usb hub
[146:34.84] and then i'm going to go back to the usb hub
[146:36.84] and then i'm going to go back to the usb hub
[146:38.84] and then i'm going to go back to the usb hub
[146:40.84] and then i'm going to go back to the usb hub
[146:42.84] and then i'm going to go back to the usb hub
[146:44.84] and then i'm going to go back to the usb hub
[146:46.84] and then i'm going to go back to the usb hub
[146:48.84] and then i'm going to go back to the usb hub
[146:50.84] and then i'm going to go back to the usb hub
[146:52.84] and then i'm going to go back to the usb hub
[146:54.84] and then i'm going to go back to the usb hub
[146:56.84] and then i'm going to go back to the usb hub
[146:58.84] and then i'm going to go back to the usb hub
[147:00.84] and then i'm going to go back to the usb hub
[147:02.84] and then i'm going to go back to the usb hub
[147:04.84] and then i'm going to go back to the usb hub
[147:06.84] and then i'm going to go back to the usb hub
[147:08.84] and then i'm going to go back to the usb hub
[147:10.84] and then i'm going to go back to the usb hub
[147:12.84] and then i'm going to go back to the usb hub
[147:14.84] and then i'm going to go back to the usb hub
[147:16.84] and then i'm going to go back to the usb hub
[147:18.84] and then i'm going to go back to the usb hub
[147:20.84] and then i'm going to go back to the usb hub
[147:22.84] and then i'm going to go back to the usb hub
[147:24.84] and then i'm going to go back to the usb hub
[147:26.84] and then i'm going to go back to the usb hub
[147:28.84] and then i'm going to go back to the usb hub
[147:30.84] and then i'm going to go back to the usb hub
[147:32.84] and then i'm going to go back to the usb hub
[147:34.84] and then i'm going to go back to the usb hub
[147:36.84] and then i'm going to go back to the usb hub
[147:38.84] and then i'm going to go back to the usb hub
[147:40.84] and then i'm going to go back to the usb hub
[147:42.84] and then i'm going to go back to the usb hub
[147:44.84] and then i'm going to go back to the usb hub
[147:46.84] and then i'm going to go back to the usb hub
[147:48.84] and then i'm going to go back to the usb hub
[147:50.84] and then i'm going to go back to the usb hub
[147:52.84] and then i'm going to go back to the usb hub
[147:54.84] and then i'm going to go back to the usb hub
[147:56.84] and then i'm going to go back to the usb hub
[147:58.84] and then i'm going to go back to the usb hub
[148:00.84] and then i'm going to go back to the usb hub
[148:02.84] and then i'm going to go back to the usb hub
[148:04.84] and then i'm going to go back to the usb hub
[148:06.84] and then i'm going to go back to the usb hub
[148:08.84] and then i'm going to go back to the usb hub
[148:10.84] and then i'm going to go back to the usb hub
[148:12.84] and then i'm going to go back to the usb hub
[148:14.84] and then i'm going to go back to the usb hub
[148:16.84] and then i'm going to go back to the usb hub
[148:18.84] and then i'm going to go back to the usb hub
[148:20.84] and then i'm going to go back to the usb hub
[148:22.84] and then i'm going to go back to the usb hub
[148:24.84] and then i'm going to go back to the usb hub
[148:26.84] and then i'm going to go back to the usb hub
[148:28.84] and then i'm going to go back to the usb hub
[148:30.84] and then i'm going to go back to the usb hub
[148:32.84] and then i'm going to go back to the usb hub
[148:34.84] and then i'm going to go back to the usb hub
[148:36.84] and then i'm going to go back to the usb hub
[148:38.84] and then i'm going to go back to the usb hub
[148:40.84] and then i'm going to go back to the usb hub
[148:42.84] and then i'm going to go back to the usb hub
[148:44.84] and then i'm going to go back to the usb hub
[148:46.84] and then i'm going to go back to the usb hub
[148:48.84] and then i'm going to go back to the usb hub
[148:50.84] and then i'm going to go back to the usb hub
[148:52.84] and then i'm going to go back to the usb hub
[148:54.84] and then i'm going to go back to the usb hub
[148:56.84] and then i'm going to go back to the usb hub
[148:58.84] and then i'm going to go back to the usb hub
[149:00.84] and then i'm going to go back to the usb hub
[149:02.84] and then i'm going to go back to the usb hub
[149:04.84] and then i'm going to go back to the usb hub
[149:06.84] and then i'm going to go back to the usb hub
[149:08.84] and then i'm going to go back to the usb hub
[149:10.84] and then i'm going to go back to the usb hub
[149:12.84] and then i'm going to go back to the usb hub
[149:14.84] and then i'm going to go back to the usb hub
[149:16.84] and then i'm going to go back to the usb hub
[149:18.84] and then i'm going to go back to the usb hub
[149:20.84] and then i'm going to go back to the usb hub
[149:22.84] and then i'm going to go back to the usb hub
[149:24.84] and then i'm going to go back to the usb hub
[149:26.84] and then i'm going to go back to the usb hub
[149:28.84] and then i'm going to go back to the usb hub
[149:30.84] and then i'm going to go back to the usb hub
[149:32.84] and then i'm going to go back to the usb hub
[149:34.84] and then i'm going to go back to the usb hub
[149:36.84] and then i'm going to go back to the usb hub
[149:38.84] and then i'm going to go back to the usb hub
[149:40.84] and then i'm going to go back to the usb hub
[149:42.84] and then i'm going to go back to the usb hub
[149:44.84] and then i'm going to go back to the usb hub
[149:46.84] and then i'm going to go back to the usb hub
[149:48.84] and then i'm going to go back to the usb hub
[149:50.84] and then i'm going to go back to the usb hub
[149:52.84] and then i'm going to go back to the usb hub
[149:54.84] and then i'm going to go back to the usb hub
[149:56.84] and then i'm going to go back to the usb hub
[149:58.84] and then i'm going to go back to the usb hub
[150:00.84] and then i'm going to go back to the usb hub
[150:02.84] and then i'm going to go back to the usb hub
[150:04.84] and then i'm going to go back to the usb hub
[150:06.84] and then i'm going to go back to the usb hub
[150:08.84] and then i'm going to go back to the usb hub
[150:10.84] and then i'm going to go back to the usb hub
[150:12.84] and then i'm going to go back to the usb hub
[150:14.84] and then i'm going to go back to the usb hub
[150:16.84] and then i'm going to go back to the usb hub
[150:18.84] and then i'm going to go back to the usb hub
[150:20.84] and then i'm going to go back to the usb hub
[150:22.84] and then i'm going to go back to the usb hub
[150:24.84] and then i'm going to go back to the usb hub
[150:26.84] and then i'm going to go back to the usb hub
[150:28.84] and then i'm going to go back to the usb hub
[150:30.84] and then i'm going to go back to the usb hub
[150:32.84] and then i'm going to go back to the usb hub
[150:34.84] and then i'm going to go back to the usb hub
[150:36.84] and then i'm going to go back to the usb hub
[150:38.84] and then i'm going to go back to the usb hub
[150:40.84] and then i'm going to go back to the usb hub
[150:42.84] and then i'm going to go back to the usb hub
[150:44.84] and then i'm going to go back to the usb hub
[150:46.84] and then i'm going to go back to the usb hub
[150:48.84] and then i'm going to go back to the usb hub
[150:50.84] and then i'm going to go back to the usb hub
[150:52.84] and then i'm going to go back to the usb hub
[150:54.84] and then i'm going to go back to the usb hub
[150:56.84] and then i'm going to go back to the usb hub
[150:58.84] and then i'm going to go back to the usb hub
[151:00.84] and then i'm going to go back to the usb hub
[151:02.84] and then i'm going to go back to the usb hub
[151:04.84] and then i'm going to go back to the usb hub
[151:06.84] and then i'm going to go back to the usb hub
[151:08.84] and then i'm going to go back to the usb hub
[151:10.84] and then i'm going to go back to the usb hub
[151:12.84] and then i'm going to go back to the usb hub
[151:14.84] and then i'm going to go back to the usb hub
[151:16.84] and then i'm going to go back to the usb hub
[151:18.84] and then i'm going to go back to the usb hub
[151:20.84] and then i'm going to go back to the usb hub
[151:22.84] and then i'm going to go back to the usb hub
[151:24.84] and then i'm going to go back to the usb hub
[151:26.84] and then i'm going to go back to the usb hub
[151:28.84] and then i'm going to go back to the usb hub
[151:30.84] and then i'm going to go back to the usb hub
[151:32.84] and then i'm going to go back to the usb hub
[151:34.84] and then i'm going to go back to the usb hub
[151:36.84] and then i'm going to go back to the usb hub
[151:38.84] and then i'm going to go back to the usb hub
[151:40.84] and then i'm going to go back to the usb hub
[151:42.84] and then i'm going to go back to the usb hub
[151:44.84] and then i'm going to go back to the usb hub
[151:46.84] and then i'm going to go back to the usb hub
[151:48.84] and then i'm going to go back to the usb hub
[151:50.84] and then i'm going to go back to the usb hub
[151:52.84] and then i'm going to go back to the usb hub
[151:54.84] and then i'm going to go back to the usb hub
[151:56.84] and then i'm going to go back to the usb hub
[151:58.84] and then i'm going to go back to the usb hub
[152:00.84] and then i'm going to go back to the usb hub
[152:02.84] and then i'm going to go back to the usb hub
[152:04.84] and then i'm going to go back to the usb hub
[152:06.84] and then i'm going to go back to the usb hub
[152:08.84] and then i'm going to go back to the usb hub
[152:10.84] and then i'm going to go back to the usb hub
[152:12.84] and then i'm going to go back to the usb hub
[152:14.84] and then i'm going to go back to the usb hub
[152:16.84] and then i'm going to go back to the usb hub
[152:18.84] and then i'm going to go back to the usb hub
[152:20.84] and then i'm going to go back to the usb hub
[152:22.84] and then i'm going to go back to the usb hub
[152:24.84] and then i'm going to go back to the usb hub
[152:26.84] and then i'm going to go back to the usb hub
[152:28.84] and then i'm going to go back to the usb hub
[152:30.84] and then i'm going to go back to the usb hub
[152:32.84] and then i'm going to go back to the usb hub
[152:34.84] and then i'm going to go back to the usb hub
[152:36.84] and then i'm going to go back to the usb hub
[152:38.84] and then i'm going to go back to the usb hub
[152:40.84] and then i'm going to go back to the usb hub
[152:42.84] and then i'm going to go back to the usb hub
[152:44.84] and then i'm going to go back to the usb hub
[152:46.84] and then i'm going to go back to the usb hub
[152:48.84] and then i'm going to go back to the usb hub
[152:50.84] and then i'm going to go back to the usb hub
[152:52.84] and then i'm going to go back to the usb hub
[152:54.84] and then i'm going to go back to the usb hub
[152:56.84] and then i'm going to go back to the usb hub
[152:58.84] and then i'm going to go back to the usb hub
[153:00.84] and then i'm going to go back to the usb hub
[153:02.84] and then i'm going to go back to the usb hub
[153:04.84] and then i'm going to go back to the usb hub
[153:06.84] and then i'm going to go back to the usb hub
[153:08.84] and then i'm going to go back to the usb hub
[153:10.84] and then i'm going to go back to the usb hub
[153:12.84] and then i'm going to go back to the usb hub
[153:14.84] and then i'm going to go back to the usb hub
[153:16.84] and then i'm going to go back to the usb hub
[153:18.84] and then i'm going to go back to the usb hub
[153:20.84] and then i'm going to go back to the usb hub
[153:22.84] and then i'm going to go back to the usb hub
[153:24.84] and then i'm going to go back to the usb hub
[153:26.84] and then i'm going to go back to the usb hub
[153:28.84] and then i'm going to go back to the usb hub
[153:30.84] and then i'm going to go back to the usb hub
[153:32.84] and then i'm going to go back to the usb hub
[153:34.84] and then i'm going to go back to the usb hub
[153:36.84] and then i'm going to go back to the usb hub
[153:38.84] and then i'm going to go back to the usb hub
[153:40.84] and then i'm going to go back to the usb hub
[153:42.84] and then i'm going to go back to the usb hub
[153:44.84] and then i'm going to go back to the usb hub
[153:46.84] and then i'm going to go back to the usb hub
[153:48.84] and then i'm going to go back to the usb hub
[153:50.84] and then i'm going to go back to the usb hub
[153:52.84] and then i'm going to go back to the usb hub
[153:54.84] and then i'm going to go back to the usb hub
[153:56.84] and then i'm going to go back to the usb hub
[153:58.84] and then i'm going to go back to the usb hub
[154:00.84] and then i'm going to go back to the usb hub
[154:02.84] and then i'm going to go back to the usb hub
[154:04.84] and then i'm going to go back to the usb hub
[154:06.84] and then i'm going to go back to the usb hub
[154:08.84] and then i'm going to go back to the usb hub
[154:10.84] and then i'm going to go back to the usb hub
[154:12.84] and then i'm going to go back to the usb hub
[154:14.84] and then i'm going to go back to the usb hub
[154:16.84] and then i'm going to go back to the usb hub
[154:18.84] and then i'm going to go back to the usb hub
[154:20.84] and then i'm going to go back to the usb hub
[154:22.84] and then i'm going to go back to the usb hub
[154:24.84] and then i'm going to go back to the usb hub
[154:26.84] and then i'm going to go back to the usb hub
[154:28.84] and then i'm going to go back to the usb hub
[154:30.84] and then i'm going to go back to the usb hub
[154:32.84] and then i'm going to go back to the usb hub
[154:34.84] and then i'm going to go back to the usb hub
[154:36.84] and then i'm going to go back to the usb hub
[154:38.84] and then i'm going to go back to the usb hub
[154:40.84] and then i'm going to go back to the usb hub
[154:42.84] and then i'm going to go back to the usb hub
[154:44.84] and then i'm going to go back to the usb hub
[154:46.84] and then i'm going to go back to the usb hub
[154:48.84] and then i'm going to go back to the usb hub
[154:50.84] and then i'm going to go back to the usb hub
[154:52.84] and then i'm going to go back to the usb hub
[154:54.84] and then i'm going to go back to the usb hub
[154:56.84] and then i'm going to go back to the usb hub
[154:58.84] and then i'm going to go back to the usb hub
[155:00.84] and then i'm going to go back to the usb hub
[155:02.84] and then i'm going to go back to the usb hub
[155:04.84] and then i'm going to go back to the usb hub
[155:06.84] and then i'm going to go back to the usb hub
[155:08.84] and then i'm going to go back to the usb hub
[155:10.84] and then i'm going to go back to the usb hub
[155:12.84] and then i'm going to go back to the usb hub
[155:14.84] and then i'm going to go back to the usb hub
[155:16.84] and then i'm going to go back to the usb hub
[155:18.84] and then i'm going to go back to the usb hub
[155:20.84] and then i'm going to go back to the usb hub
[155:22.84] and then i'm going to go back to the usb hub
[155:24.84] and then i'm going to go back to the usb hub
[155:26.84] and then i'm going to go back to the usb hub
[155:28.84] and then i'm going to go back to the usb hub
[155:30.84] and then i'm going to go back to the usb hub
[155:32.84] and then i'm going to go back to the usb hub
[155:34.84] and then i'm going to go back to the usb hub
[155:36.84] and then i'm going to go back to the usb hub
[155:38.84] and then i'm going to go back to the usb hub
[155:40.84] and then i'm going to go back to the usb hub
[155:42.84] and then i'm going to go back to the usb hub
[155:44.84] and then i'm going to go back to the usb hub
[155:46.84] and then i'm going to go back to the usb hub
[155:48.84] and then i'm going to go back to the usb hub
[155:50.84] and then i'm going to go back to the usb hub
[155:52.84] and then i'm going to go back to the usb hub
[155:54.84] and then i'm going to go back to the usb hub
[155:56.84] and then i'm going to go back to the usb hub
[155:58.84] and then i'm going to go back to the usb hub
[156:00.84] and then i'm going to go back to the usb hub
[156:02.84] and then i'm going to go back to the usb hub
[156:04.84] and then i'm going to go back to the usb hub
[156:06.84] and then i'm going to go back to the usb hub
[156:08.84] and then i'm going to go back to the usb hub
[156:10.84] and then i'm going to go back to the usb hub
[156:12.84] and then i'm going to go back to the usb hub
[156:14.84] and then i'm going to go back to the usb hub
[156:16.84] and then i'm going to go back to the usb hub
[156:18.84] and then i'm going to go back to the usb hub
[156:20.84] and then i'm going to go back to the usb hub
[156:22.84] and then i'm going to go back to the usb hub
[156:24.84] and then i'm going to go back to the usb hub
[156:26.84] and then i'm going to go back to the usb hub
[156:28.84] and then i'm going to go back to the usb hub
[156:30.84] and then i'm going to go back to the usb hub
[156:32.84] and then i'm going to go back to the usb hub
[156:34.84] and then i'm going to go back to the usb hub
[156:36.84] and then i'm going to go back to the usb hub
[156:38.84] and then i'm going to go back to the usb hub
[156:40.84] and then i'm going to go back to the usb hub
[156:42.84] and then i'm going to go back to the usb hub
[156:44.84] and then i'm going to go back to the usb hub
[156:46.84] and then i'm going to go back to the usb hub
[156:48.84] and then i'm going to go back to the usb hub
[156:50.84] and then i'm going to go back to the usb hub
[156:52.84] and then i'm going to go back to the usb hub
[156:54.84] and then i'm going to go back to the usb hub
[156:56.84] and then i'm going to go back to the usb hub
[156:58.84] and then i'm going to go back to the usb hub
[157:00.84] and then i'm going to go back to the usb hub
[157:02.84] and then i'm going to go back to the usb hub
[157:04.84] and then i'm going to go back to the usb hub
[157:06.84] and then i'm going to go back to the usb hub
[157:08.84] and then i'm going to go back to the usb hub
[157:10.84] and then i'm going to go back to the usb hub
[157:12.84] and then i'm going to go back to the usb hub
[157:14.84] and then i'm going to go back to the usb hub
[157:16.84] and then i'm going to go back to the usb hub
[157:18.84] and then i'm going to go back to the usb hub
[157:20.84] and then i'm going to go back to the usb hub
[157:22.84] and then i'm going to go back to the usb hub
[157:24.84] and then i'm going to go back to the usb hub
[157:26.84] and then i'm going to go back to the usb hub
[157:28.84] and then i'm going to go back to the usb hub
[157:30.84] and then i'm going to go back to the usb hub
[157:32.84] and then i'm going to go back to the usb hub
[157:34.84] and then i'm going to go back to the usb hub
[157:36.84] and then i'm going to go back to the usb hub
[157:38.84] and then i'm going to go back to the usb hub
[157:40.84] and then i'm going to go back to the usb hub
[157:42.84] and then i'm going to go back to the usb hub
[157:44.84] and then i'm going to go back to the usb hub
[157:46.84] and then i'm going to go back to the usb hub
[157:48.84] and then i'm going to go back to the usb hub
[157:50.84] and then i'm going to go back to the usb hub
[157:52.84] and then i'm going to go back to the usb hub
[157:54.84] and then i'm going to go back to the usb hub
[157:56.84] and then i'm going to go back to the usb hub
[157:58.84] and then i'm going to go back to the usb hub
[158:00.84] and then i'm going to go back to the usb hub
[158:02.84] and then i'm going to go back to the usb hub
[158:04.84] and then i'm going to go back to the usb hub
[158:06.84] and then i'm going to go back to the usb hub
[158:08.84] and then i'm going to go back to the usb hub
[158:10.84] and then i'm going to go back to the usb hub
[158:12.84] and then i'm going to go back to the usb hub
[158:14.84] and then i'm going to go back to the usb hub
[158:16.84] and then i'm going to go back to the usb hub
[158:18.84] and then i'm going to go back to the usb hub
[158:20.84] and then i'm going to go back to the usb hub
[158:22.84] and then i'm going to go back to the usb hub
[158:24.84] and then i'm going to go back to the usb hub
[158:26.84] and then i'm going to go back to the usb hub
[158:28.84] and then i'm going to go back to the usb hub
[158:30.84] and then i'm going to go back to the usb hub
[158:32.84] and then i'm going to go back to the usb hub
[158:34.84] and then i'm going to go back to the usb hub
[158:36.84] and then i'm going to go back to the usb hub
[158:38.84] and then i'm going to go back to the usb hub
[158:40.84] and then i'm going to go back to the usb hub
[158:42.84] and then i'm going to go back to the usb hub
[158:44.84] and then i'm going to go back to the usb hub
[158:46.84] and then i'm going to go back to the usb hub
[158:48.84] and then i'm going to go back to the usb hub
[158:50.84] and then i'm going to go back to the usb hub
[158:52.84] and then i'm going to go back to the usb hub
[158:54.84] and then i'm going to go back to the usb hub
[158:56.84] and then i'm going to go back to the usb hub
[158:58.84] and then i'm going to go back to the usb hub
[159:00.84] and then i'm going to go back to the usb hub
[159:02.84] and then i'm going to go back to the usb hub
[159:04.84] and then i'm going to go back to the usb hub
[159:06.84] and then i'm going to go back to the usb hub
[159:08.84] and then i'm going to go back to the usb hub
[159:10.84] and then i'm going to go back to the usb hub
[159:12.84] and then i'm going to go back to the usb hub
[159:14.84] and then i'm going to go back to the usb hub
[159:16.84] and then i'm going to go back to the usb hub
[159:18.84] and then i'm going to go back to the usb hub
[159:20.84] and then i'm going to go back to the usb hub
[159:22.84] and then i'm going to go back to the usb hub
[159:24.84] and then i'm going to go back to the usb hub
[159:26.84] and then i'm going to go back to the usb hub
[159:28.84] and then i'm going to go back to the usb hub
[159:30.84] and then i'm going to go back to the usb hub
[159:32.84] and then i'm going to go back to the usb hub
[159:34.84] and then i'm going to go back to the usb hub
[159:36.84] and then i'm going to go back to the usb hub
[159:38.84] and then i'm going to go back to the usb hub
[159:40.84] and then i'm going to go back to the usb hub
[159:42.84] and then i'm going to go back to the usb hub
[159:44.84] and then i'm going to go back to the usb hub
[159:46.84] and then i'm going to go back to the usb hub
[159:48.84] and then i'm going to go back to the usb hub
[159:50.84] and then i'm going to go back to the usb hub
[159:52.84] and then i'm going to go back to the usb hub
[159:54.84] and then i'm going to go back to the usb hub
[159:56.84] and then i'm going to go back to the usb hub
[159:58.84] and then i'm going to go back to the usb hub
[160:00.84] and then i'm going to go back to the usb hub
[160:02.84] and then i'm going to go back to the usb hub
[160:04.84] and then i'm going to go back to the usb hub
[160:06.84] and then i'm going to go back to the usb hub
[160:08.84] and then i'm going to go back to the usb hub
[160:10.84] and then i'm going to go back to the usb hub
[160:12.84] and then i'm going to go back to the usb hub
[160:14.84] and then i'm going to go back to the usb hub
[160:16.84] and then i'm going to go back to the usb hub
[160:18.84] and then i'm going to go back to the usb hub
[160:20.84] and then i'm going to go back to the usb hub
[160:22.84] and then i'm going to go back to the usb hub
[160:24.84] and then i'm going to go back to the usb hub
[160:26.84] and then i'm going to go back to the usb hub
[160:28.84] and then i'm going to go back to the usb hub
[160:30.84] and then i'm going to go back to the usb hub
[160:32.84] and then i'm going to go back to the usb hub
[160:34.84] and then i'm going to go back to the usb hub
[160:36.84] and then i'm going to go back to the usb hub
[160:38.84] and then i'm going to go back to the usb hub
[160:40.84] and then i'm going to go back to the usb hub
[160:42.84] and then i'm going to go back to the usb hub
[160:44.84] and then i'm going to go back to the usb hub
[160:46.84] and then i'm going to go back to the usb hub
[160:48.84] and then i'm going to go back to the usb hub
[160:50.84] and then i'm going to go back to the usb hub
[160:52.84] and then i'm going to go back to the usb hub
[160:54.84] and then i'm going to go back to the usb hub
[160:56.84] and then i'm going to go back to the usb hub
[160:58.84] and then i'm going to go back to the usb hub
[161:00.84] and then i'm going to go back to the usb hub
[161:02.84] and then i'm going to go back to the usb hub
[161:04.84] and then i'm going to go back to the usb hub
[161:06.84] and then i'm going to go back to the usb hub
[161:08.84] and then i'm going to go back to the usb hub
[161:10.84] and then i'm going to go back to the usb hub
[161:12.84] and then i'm going to go back to the usb hub
[161:14.84] and then i'm going to go back to the usb hub
[161:16.84] and then i'm going to go back to the usb hub
[161:18.84] and then i'm going to go back to the usb hub
[161:20.84] and then i'm going to go back to the usb hub
[161:22.84] and then i'm going to go back to the usb hub
[161:24.84] and then i'm going to go back to the usb hub
[161:26.84] and then i'm going to go back to the usb hub
[161:28.84] and then i'm going to go back to the usb hub
[161:30.84] and then i'm going to go back to the usb hub
[161:32.84] and then i'm going to go back to the usb hub
[161:34.84] and then i'm going to go back to the usb hub
[161:36.84] and then i'm going to go back to the usb hub
[161:38.84] and then i'm going to go back to the usb hub
[161:40.84] and then i'm going to go back to the usb hub
[161:42.84] and then i'm going to go back to the usb hub
[161:44.84] and then i'm going to go back to the usb hub
[161:46.84] and then i'm going to go back to the usb hub
[161:48.84] and then i'm going to go back to the usb hub
[161:50.84] and then i'm going to go back to the usb hub
[161:52.84] and then i'm going to go back to the usb hub
[161:54.84] and then i'm going to go back to the usb hub
[161:56.84] and then i'm going to go back to the usb hub
[161:58.84] and then i'm going to go back to the usb hub
[162:00.84] and then i'm going to go back to the usb hub
[162:02.84] and then i'm going to go back to the usb hub
[162:04.84] and then i'm going to go back to the usb hub
[162:06.84] and then i'm going to go back to the usb hub
[162:08.84] and then i'm going to go back to the usb hub
[162:10.84] and then i'm going to go back to the usb hub
[162:12.84] and then i'm going to go back to the usb hub
[162:14.84] and then i'm going to go back to the usb hub
[162:16.84] and then i'm going to go back to the usb hub
[162:18.84] and then i'm going to go back to the usb hub
[162:20.84] and then i'm going to go back to the usb hub
[162:22.84] and then i'm going to go back to the usb hub
[162:24.84] and then i'm going to go back to the usb hub
[162:26.84] and then i'm going to go back to the usb hub
[162:28.84] and then i'm going to go back to the usb hub
[162:30.84] and then i'm going to go back to the usb hub
[162:32.84] and then i'm going to go back to the usb hub
[162:34.84] and then i'm going to go back to the usb hub
[162:36.84] and then i'm going to go back to the usb hub
[162:38.84] and then i'm going to go back to the usb hub
[162:40.84] and then i'm going to go back to the usb hub
[162:42.84] and then i'm going to go back to the usb hub
[162:44.84] and then i'm going to go back to the usb hub
[162:46.84] and then i'm going to go back to the usb hub
[162:48.84] and then i'm going to go back to the usb hub
[162:50.84] and then i'm going to go back to the usb hub
[162:52.84] and then i'm going to go back to the usb hub
[162:54.84] and then i'm going to go back to the usb hub
[162:56.84] and then i'm going to go back to the usb hub
[162:58.84] and then i'm going to go back to the usb hub
[163:00.84] and then i'm going to go back to the usb hub
[163:02.84] and then i'm going to go back to the usb hub
[163:04.84] and then i'm going to go back to the usb hub
[163:06.84] and then i'm going to go back to the usb hub
[163:08.84] and then i'm going to go back to the usb hub
[163:10.84] and then i'm going to go back to the usb hub
[163:12.84] and then i'm going to go back to the usb hub
[163:14.84] and then i'm going to go back to the usb hub
[163:16.84] and then i'm going to go back to the usb hub
[163:18.84] and then i'm going to go back to the usb hub
[163:20.84] and then i'm going to go back to the usb hub
[163:22.84] and then i'm going to go back to the usb hub
[163:24.84] and then i'm going to go back to the usb hub
[163:26.84] and then i'm going to go back to the usb hub
[163:28.84] and then i'm going to go back to the usb hub
[163:30.84] and then i'm going to go back to the usb hub
[163:32.84] and then i'm going to go back to the usb hub
[163:34.84] and then i'm going to go back to the usb hub
[163:36.84] and then i'm going to go back to the usb hub
[163:38.84] and then i'm going to go back to the usb hub
[163:40.84] and then i'm going to go back to the usb hub
[163:42.84] and then i'm going to go back to the usb hub
[163:44.84] and then i'm going to go back to the usb hub
[163:46.84] and then i'm going to go back to the usb hub
[163:48.84] and then i'm going to go back to the usb hub
[163:50.84] and then i'm going to go back to the usb hub
[163:52.84] and then i'm going to go back to the usb hub
[163:54.84] and then i'm going to go back to the usb hub
[163:56.84] and then i'm going to go back to the usb hub
[163:58.84] and then i'm going to go back to the usb hub
[164:00.84] and then i'm going to go back to the usb hub
[164:02.84] and then i'm going to go back to the usb hub
[164:04.84] and then i'm going to go back to the usb hub
[164:06.84] and then i'm going to go back to the usb hub
[164:08.84] and then i'm going to go back to the usb hub
[164:10.84] and then i'm going to go back to the usb hub
[164:12.84] and then i'm going to go back to the usb hub
[164:14.84] and then i'm going to go back to the usb hub
[164:16.84] and then i'm going to go back to the usb hub
[164:18.84] and then i'm going to go back to the usb hub
[164:20.84] and then i'm going to go back to the usb hub
[164:22.84] and then i'm going to go back to the usb hub
[164:24.84] and then i'm going to go back to the usb hub
[164:26.84] and then i'm going to go back to the usb hub
[164:28.84] and then i'm going to go back to the usb hub
[164:30.84] and then i'm going to go back to the usb hub
[164:32.84] and then i'm going to go back to the usb hub
[164:34.84] and then i'm going to go back to the usb hub
[164:36.84] and then i'm going to go back to the usb hub
[164:38.84] and then i'm going to go back to the usb hub
[164:40.84] and then i'm going to go back to the usb hub
[164:42.84] and then i'm going to go back to the usb hub
[164:44.84] and then i'm going to go back to the usb hub
[164:46.84] and then i'm going to go back to the usb hub
[164:48.84] and then i'm going to go back to the usb hub
[164:50.84] and then i'm going to go back to the usb hub
[164:52.84] and then i'm going to go back to the usb hub
[164:54.84] and then i'm going to go back to the usb hub
[164:56.84] and then i'm going to go back to the usb hub
[164:58.84] and then i'm going to go back to the usb hub
[165:00.84] and then i'm going to go back to the usb hub
[165:02.84] and then i'm going to go back to the usb hub
[165:04.84] and then i'm going to go back to the usb hub
[165:06.84] and then i'm going to go back to the usb hub
[165:08.84] and then i'm going to go back to the usb hub
[165:10.84] and then i'm going to go back to the usb hub
[165:12.84] and then i'm going to go back to the usb hub
[165:14.84] and then i'm going to go back to the usb hub
[165:16.84] and then i'm going to go back to the usb hub
[165:18.84] and then i'm going to go back to the usb hub
[165:20.84] and then i'm going to go back to the usb hub
[165:22.84] and then i'm going to go back to the usb hub
[165:24.84] and then i'm going to go back to the usb hub
[165:26.84] and then i'm going to go back to the usb hub
[165:28.84] and then i'm going to go back to the usb hub
[165:30.84] and then i'm going to go back to the usb hub
[165:32.84] and then i'm going to go back to the usb hub
[165:34.84] and then i'm going to go back to the usb hub
[165:36.84] and then i'm going to go back to the usb hub
[165:38.84] and then i'm going to go back to the usb hub
[165:40.84] and then i'm going to go back to the usb hub
[165:42.84] and then i'm going to go back to the usb hub
[165:44.84] and then i'm going to go back to the usb hub
[165:46.84] and then i'm going to go back to the usb hub
[165:48.84] and then i'm going to go back to the usb hub
[165:50.84] and then i'm going to go back to the usb hub
[165:52.84] and then i'm going to go back to the usb hub
[165:54.84] and then i'm going to go back to the usb hub
[165:56.84] and then i'm going to go back to the usb hub
[165:58.84] and then i'm going to go back to the usb hub
[166:00.84] and then i'm going to go back to the usb hub
[166:02.84] and then i'm going to go back to the usb hub
[166:04.84] and then i'm going to go back to the usb hub
[166:06.84] and then i'm going to go back to the usb hub
[166:08.84] and then i'm going to go back to the usb hub
[166:10.84] and then i'm going to go back to the usb hub
[166:12.84] and then i'm going to go back to the usb hub
[166:14.84] and then i'm going to go back to the usb hub
[166:16.84] and then i'm going to go back to the usb hub
[166:18.84] and then i'm going to go back to the usb hub
[166:20.84] and then i'm going to go back to the usb hub
[166:22.84] and then i'm going to go back to the usb hub
[166:24.84] and then i'm going to go back to the usb hub
[166:26.84] and then i'm going to go back to the usb hub
[166:28.84] and then i'm going to go back to the usb hub
[166:30.84] and then i'm going to go back to the usb hub
[166:32.84] and then i'm going to go back to the usb hub
[166:34.84] and then i'm going to go back to the usb hub
[166:36.84] and then i'm going to go back to the usb hub
[166:38.84] and then i'm going to go back to the usb hub
[166:40.84] and then i'm going to go back to the usb hub
[166:42.84] and then i'm going to go back to the usb hub
[166:44.84] and then i'm going to go back to the usb hub
[166:46.84] and then i'm going to go back to the usb hub
[166:48.84] and then i'm going to go back to the usb hub
[166:50.84] and then i'm going to go back to the usb hub
[166:52.84] and then i'm going to go back to the usb hub
[166:54.84] and then i'm going to go back to the usb hub
[166:56.84] and then i'm going to go back to the usb hub
[166:58.84] and then i'm going to go back to the usb hub
[167:00.84] and then i'm going to go back to the usb hub
[167:02.84] and then i'm going to go back to the usb hub
[167:04.84] and then i'm going to go back to the usb hub
[167:06.84] and then i'm going to go back to the usb hub
[167:08.84] and then i'm going to go back to the usb hub
[167:10.84] and then i'm going to go back to the usb hub
[167:12.84] and then i'm going to go back to the usb hub
[167:14.84] and then i'm going to go back to the usb hub
[167:16.84] and then i'm going to go back to the usb hub
[167:18.84] and then i'm going to go back to the usb hub
[167:20.84] and then i'm going to go back to the usb hub
[167:22.84] and then i'm going to go back to the usb hub
[167:24.84] and then i'm going to go back to the usb hub
[167:26.84] and then i'm going to go back to the usb hub
[167:28.84] and then i'm going to go back to the usb hub
[167:30.84] and then i'm going to go back to the usb hub
[167:32.84] and then i'm going to go back to the usb hub
[167:34.84] and then i'm going to go back to the usb hub
[167:36.84] and then i'm going to go back to the usb hub
[167:38.84] and then i'm going to go back to the usb hub
[167:40.84] and then i'm going to go back to the usb hub
[167:42.84] and then i'm going to go back to the usb hub
[167:44.84] and then i'm going to go back to the usb hub
[167:46.84] and then i'm going to go back to the usb hub
[167:48.84] and then i'm going to go back to the usb hub
[167:50.84] and then i'm going to go back to the usb hub
[167:52.84] and then i'm going to go back to the usb hub
[167:54.84] and then i'm going to go back to the usb hub
[167:56.84] and then i'm going to go back to the usb hub
[167:58.84] and then i'm going to go back to the usb hub
[168:00.84] and then i'm going to go back to the usb hub
[168:02.84] and then i'm going to go back to the usb hub
[168:04.84] and then i'm going to go back to the usb hub
[168:06.84] and then i'm going to go back to the usb hub
[168:08.84] and then i'm going to go back to the usb hub
[168:10.84] and then i'm going to go back to the usb hub
[168:12.84] and then i'm going to go back to the usb hub
[168:14.84] and then i'm going to go back to the usb hub
[168:16.84] and then i'm going to go back to the usb hub
[168:18.84] and then i'm going to go back to the usb hub
[168:20.84] and then i'm going to go back to the usb hub
[168:22.84] and then i'm going to go back to the usb hub
[168:24.84] and then i'm going to go back to the usb hub
[168:26.84] and then i'm going to go back to the usb hub
[168:28.84] and then i'm going to go back to the usb hub
[168:30.84] and then i'm going to go back to the usb hub
[168:32.84] and then i'm going to go back to the usb hub
[168:34.84] and then i'm going to go back to the usb hub
[168:36.84] and then i'm going to go back to the usb hub
[168:38.84] and then i'm going to go back to the usb hub
[168:40.84] and then i'm going to go back to the usb hub
[168:42.84] and then i'm going to go back to the usb hub
[168:44.84] and then i'm going to go back to the usb hub
[168:46.84] and then i'm going to go back to the usb hub
[168:48.84] and then i'm going to go back to the usb hub
[168:50.84] and then i'm going to go back to the usb hub
[168:52.84] and then i'm going to go back to the usb hub
[168:54.84] and then i'm going to go back to the usb hub
[168:56.84] and then i'm going to go back to the usb hub
[168:58.84] and then i'm going to go back to the usb hub
[169:00.84] and then i'm going to go back to the usb hub
[169:02.84] and then i'm going to go back to the usb hub
[169:04.84] and then i'm going to go back to the usb hub
[169:06.84] and then i'm going to go back to the usb hub
[169:08.84] and then i'm going to go back to the usb hub
[169:10.84] and then i'm going to go back to the usb hub
[169:12.84] and then i'm going to go back to the usb hub
[169:14.84] and then i'm going to go back to the usb hub
[169:16.84] and then i'm going to go back to the usb hub
[169:18.84] and then i'm going to go back to the usb hub
[169:20.84] and then i'm going to go back to the usb hub
[169:22.84] and then i'm going to go back to the usb hub
[169:24.84] and then i'm going to go back to the usb hub
[169:26.84] and then i'm going to go back to the usb hub
[169:28.84] and then i'm going to go back to the usb hub
[169:30.84] and then i'm going to go back to the usb hub
[169:32.84] and then i'm going to go back to the usb hub
[169:34.84] and then i'm going to go back to the usb hub
[169:36.84] and then i'm going to go back to the usb hub
[169:38.84] and then i'm going to go back to the usb hub
[169:40.84] and then i'm going to go back to the usb hub
[169:42.84] and then i'm going to go back to the usb hub
[169:44.84] and then i'm going to go back to the usb hub
[169:46.84] and then i'm going to go back to the usb hub
[169:48.84] and then i'm going to go back to the usb hub
[169:50.84] and then i'm going to go back to the usb hub
[169:52.84] and then i'm going to go back to the usb hub
[169:54.84] and then i'm going to go back to the usb hub
[169:56.84] and then i'm going to go back to the usb hub
[169:58.84] and then i'm going to go back to the usb hub
[170:00.84] and then i'm going to go back to the usb hub
[170:02.84] and then i'm going to go back to the usb hub
[170:04.84] and then i'm going to go back to the usb hub
[170:06.84] and then i'm going to go back to the usb hub
[170:08.84] and then i'm going to go back to the usb hub
[170:10.84] and then i'm going to go back to the usb hub
[170:12.84] and then i'm going to go back to the usb hub
[170:14.84] and then i'm going to go back to the usb hub
[170:16.84] and then i'm going to go back to the usb hub
[170:18.84] and then i'm going to go back to the usb hub
[170:20.84] and then i'm going to go back to the usb hub
[170:22.84] and then i'm going to go back to the usb hub
[170:24.84] and then i'm going to go back to the usb hub
[170:26.84] and then i'm going to go back to the usb hub
[170:28.84] and then i'm going to go back to the usb hub
[170:30.84] and then i'm going to go back to the usb hub
[170:32.84] and then i'm going to go back to the usb hub
[170:34.84] and then i'm going to go back to the usb hub
[170:36.84] and then i'm going to go back to the usb hub
[170:38.84] and then i'm going to go back to the usb hub
[170:40.84] and then i'm going to go back to the usb hub
[170:42.84] and then i'm going to go back to the usb hub
[170:44.84] and then i'm going to go back to the usb hub
[170:46.84] and then i'm going to go back to the usb hub
[170:48.84] and then i'm going to go back to the usb hub
[170:50.84] and then i'm going to go back to the usb hub
[170:52.84] and then i'm going to go back to the usb hub
[170:54.84] and then i'm going to go back to the usb hub
[170:56.84] and then i'm going to go back to the usb hub
[170:58.84] and we could have a function for that, derive seed or something
[171:00.84] and we could have a function for that, derive seed or something
[171:02.84] and then we're passing in
[171:04.84] and then we're passing in
[171:06.84] the seed with the current chain code
[171:08.84] private key and public key
[171:10.84] and then we're adding that
[171:12.84] with the updated
[171:14.84] depth, fingerprint, and index
[171:16.84] depth, fingerprint, and index
[171:18.84] so if we get that block
[171:20.84] of code out of the way and maybe we move this
[171:22.84] to it's own function
[171:24.84] of derive seed
[171:26.84] of derive seed
[171:28.84] then
[171:30.84] this actually
[171:34.84] stays pretty simple as well
[171:36.84] alright well i think that's good enough
[171:50.84] to give it a check
[171:54.84] i'm going to go ahead and
[171:56.84] so i think npm run
[172:00.84] test should stay the same
[172:02.84] alright
[172:04.84] deriving a child key does not mutate
[172:06.84] internal state
[172:08.84] so something's
[172:14.84] majorly off here which is good
[172:16.84] i always like it when it fails huge
[172:18.84] i always like it when it fails huge
[172:20.84] i always like it when it fails huge
[172:22.84] i always like it when it fails huge
[172:24.84] i always like it when it fails huge
[172:26.84] i always like it when it fails huge
[172:28.84] i always like it when it fails huge
[172:30.84] i always like it when it fails huge
[172:32.84] i always like it when it fails huge
[172:34.84] i always like it when it fails huge
[172:36.84] i always like it when it fails huge
[172:38.84] i always like it when it fails huge
[172:40.84] i always like it when it fails huge
[172:42.84] i always like it when it fails huge
[172:44.84] i always like it when it fails huge
[172:46.84] i always like it when it fails huge
[172:48.84] i always like it when it fails huge
[172:50.84] i always like it when it fails huge
[172:52.84] i always like it when it fails huge
[172:54.84] i always like it when it fails huge
[172:56.84] i always like it when it fails huge
[172:58.84] i always like it when it fails huge
[173:00.84] i always like it when it fails huge
[173:02.84] i always like it when it fails huge
[173:04.84] i always like it when it fails huge
[173:06.84] i always like it when it fails huge
[173:08.84] i always like it when it fails huge
[173:10.84] i always like it when it fails huge
[173:12.84] i always like it when it fails huge
[173:14.84] i always like it when it fails huge
[173:16.84] i always like it when it fails huge
[173:18.84] i always like it when it fails huge
[173:20.84] i always like it when it fails huge
[173:22.84] i always like it when it fails huge
[173:24.84] i always like it when it fails huge
[173:26.84] i always like it when it fails huge
[173:28.84] i always like it when it fails huge
[173:30.84] i always like it when it fails huge
[173:32.84] i always like it when it fails huge
[173:34.84] i always like it when it fails huge
[173:36.84] i always like it when it fails huge
[173:38.84] i always like it when it fails huge
[173:40.84] i always like it when it fails huge
[173:42.84] i always like it when it fails huge
[173:44.84] i always like it when it fails huge
[173:46.84] i always like it when it fails huge
[173:48.84] i always like it when it fails huge
[173:50.84] i always like it when it fails huge
[173:52.84] i always like it when it fails huge
[173:54.84] i always like it when it fails huge
[173:56.84] i always like it when it fails huge
[173:58.84] i always like it when it fails huge
[174:00.84] i always like it when it fails huge
[174:02.84] i always like it when it fails huge
[174:04.84] i always like it when it fails huge
[174:06.84] i always like it when it fails huge
[174:08.84] Yeah, so something's gone catastrophically wrong, which is the best way for things to
[174:19.48] go wrong.
[174:20.56] It's not subtle in any way.
[174:23.28] Other than that, I don't immediately see it.
[174:27.68] Let me take a look at the function signatures here.
[174:39.68] Okay.
[174:45.80] Hey how's it going, Dungeoneer?
[174:52.76] Welcome.
[174:55.10] What brings you to Dash Incubator today?
[174:59.44] All right.
[175:06.16] Hmm.
[175:09.36] I'm a little confused here because, you know, one thing that we can do though is now that
[175:23.20] I understand what the API needs to be, let me remake the changes and just do the tests
[175:28.52] one at a time.
[175:36.46] Okay, so, from master seed, get reset-hd, get checkout-hd, okay.
[176:04.56] So there's from extended key, from master seed.
[176:09.84] All right, so let's just change this.
[176:16.18] First we're going to change it from bitcoin versions to, no, let's just call it from master
[176:28.06] secret to root chain.
[176:35.40] And everything should pass, good.
[176:43.50] Okay.
[176:47.14] Now let's change derive child so that all of this happens in that upper layer.
[177:04.26] So here's what we're going to do, changing derive child, moving everything into the upper
[177:17.14] layer.
[177:18.18] So now we no longer need index or hardened, we just need seed.
[177:31.38] So we say seed, we don't need indexed or hardened, say let chain and keys, and then we'll check
[177:50.58] that chain and keys equals this, and we're going to return, let's see, where did my,
[178:11.26] where did I get my depth, okay, so we're just going to do, what was it, versions, depth,
[178:24.18] index, and depth is going to be, we'll do hdkey.versions, hdkey., oh, somebody else
[178:33.98] sub, I just heard the sound, I didn't see the, it'll pop up though.
[178:39.94] So hdkey.depth, and then we've got index up above, and we're going to do chain and keys.
[179:01.78] Okay, go back to my favorite comment of all time, oh, and then we're going to need the
[179:19.66] parent fingerprint.
[179:22.66] So no matter what we do, parent fingerprint is based off of what, parent fingerprint is
[179:27.94] based off of the old key, so we'll bring that up here, parent fingerprint, index, and then
[179:43.78] the chain and the keys are going to be part of that, so no big deal there.
[179:49.70] Oh, and this is going to be plus one, so I might as well just do let versions equals
[179:57.38] hdkey.versions, let depth equals, oops, like this, and then we can use this style.
[180:13.52] So there's two styles of declaring an object, we can either do key value or we can do implicit
[180:19.62] but we can't do both, that's the rule.
[180:21.82] All right, so we've got that, and we've returned that, so we're good there, okay, great.
[180:28.74] So now, okay, derive child, seed, and key, great, and then we don't care about depth
[180:47.62] anymore and all we care about is returning the things that are really interesting to
[180:53.42] this particular function, versions, depth, parent index, index, none of that's really
[180:58.94] important to this function, this function just needs to be worried about chain code
[181:03.26] and keys, that's it.
[181:06.18] Okay, so just that change, let's go ahead and npm run test, everything passes again,
[181:13.50] great.
[181:14.50] So we're almost back to exactly where we started, so we have our public key, all right, so let's
[181:40.30] make sure that all of this is still good, all right, everything's passing, so I'm going
[181:47.18] to go ahead and add this, and then I don't actually care that it's not actually an HD
[182:02.04] function, it's really HD parts, or we could say chain parts.
[182:19.94] I don't even know if that's the right thing to call it, but that's what we're going to
[182:33.98] call it for now, to distinguish it from an HD key, so we're going to go to our derive
[182:40.18] child, and we're going to redo our type here, derive child helper, derive child, okay, derive
[182:54.86] child, and then we're going to have our derive child helper, and then we're going to take
[183:03.34] param un8array seed, that's what we got, and then we're going to have to create a type
[183:15.58] that's special for this, that we're going to type def, I'll call it, I'm going to call
[183:37.62] this HD derive helper, HD derive helper input, and that's going to have, what was it again?
[183:49.42] It was chain code, or not param, but prop, and then what else, it's going to have chain
[184:02.02] code and private key and public key, I think that's about it, I need to go double check
[184:14.78] on that, and then it will return a promise that is, well we're going to have to create
[184:32.74] a type def of the output here, that's as terrible of a name as it is, hmm, okay, derive, let's
[185:00.70] go take a look at derive, chain parts, chain code, private key, private key, public key,
[185:24.42] public key, that's it, but it returns the same type of thing, so chain code, private
[185:30.66] key, public key, there we go, so these are just the parts that change, based on the seed,
[185:57.54] the seed is derived from the index, okay.
[186:24.66] So, this looks right so far, run test, all tests pass, great, alright, so let's see where
[186:43.22] we failed, from master seed.
[187:08.98] So this derive needs a way to do next pub key, okay, that looks about right.
[187:36.34] Alright, -hd.derive, and we're just going to call this seed, very good, alright, very
[187:57.74] few changes here.
[188:21.74] Alright, so chain and key from root and seed, and let's just double check.
[188:51.50] What goes on there, because it basically seems like we should be able to return object out
[189:04.14] of sign, and again just all blanks, versions, depth, parent fingerprint, zero, oops, depth
[189:25.22] is zero, parent fingerprint is zero, index is zero, and then chain code, private key,
[189:38.02] public key, those are all things that are going to be figured out in the derive function,
[189:47.98] so, let's go take a look, oops, so, derive.
[190:15.82] Alright, let's see, is there anything different here?
[190:26.58] Chain code and seed, nope, that's the same, il, that's the same, ir, that's the same,
[190:35.86] private key, and that should be the same too, so, next priv key should just be il, wait
[190:59.38] that should be ir, oh, is that where we did dirty?
[191:18.42] That's the private key, the ir value, when it's from the seed, ir, okay, what was this
[191:36.54] before, from master, okay, let me go look in the other copy of this repository, because
[191:49.98] I think essentially I'm mixing up one of the values here, so, I'm going to pushd -hd.js,
[192:18.86] okay what is ir, ir is the chain code, ah, this might be where the devil's in the details
[192:30.10] here, private key is il, okay, so, let's take a look, chain code is ir, private key is il,
[192:46.04] that is correct in both cases, okay, let's run the test and see what happens, everything
[192:53.56] fails, hmm, how can this be explained, well, let's dig a little deeper, il, so seed buffer,
[193:15.62] and the previous chain, okay, so let's take a look, what comes in here, when we do derive,
[193:25.46] seed buffer, and the chain code is the previous chain, alright, that's the chain code, dynamic
[193:41.22] adaptive streaming over HTTP, what about it, hmm, interesting, it's a very interesting
[193:56.22] name, is that the dash we're talking about, that is not the dash we're talking about,
[194:05.14] I'm not familiar with that dash, there's so many dashes these days, no, this is the cryptocurrency,
[194:16.46] so maybe not as interesting, lots of low-level stuff though, I'm trying to figure out, I
[194:21.94] changed these two functions, I'm trying to figure out why they're different, so this
[194:34.74] one, let's go check again, SHA-512, il and ir, subarray il and ir, just make sure l comes
[194:46.86] first, r comes next, that's gotta be the way it is, SHA-512, HMAC, okay, so chain code,
[195:05.66] 032, 032, so i is the same for these, so I don't see why that would be a problem, and
[195:22.62] then chain code ends up being ir, so over here, no matter what we do, chain code ends
[195:31.26] up being ir, so that's correct, alright, no problem there, yeah, subarray will generate
[195:43.18] a reference, and I think that it's as you described, where it generates a reference
[195:50.18] and it also starts from a different index, slice will make a copy, oh, over here I'm
[196:03.38] doing subarray, and then here I'm doing slice, I wasn't even looking at that, I don't think
[196:13.18] that would be the difference, because the code is working for other things, I think
[196:19.66] the difference here, in this case, I'll double check the documentation on that, but, where
[196:29.54] this is left out, the value's left out, it just goes to the end, I'm pretty sure the
[196:37.70] only difference, there is a substr and a substring, and there is another thing with a data view,
[196:44.74] where the parameters get flip flopped and one becomes length and then the other one
[196:49.94] becomes index, but in this case, since we're dealing with 0 to 32, whether that's length
[196:56.82] or index doesn't matter, and then here, this is index, but we're not supplying a length,
[197:05.46] so it should get to the end, either way, good eye, good eye, and set private key is IL, so
[197:17.94] here, we're setting the private key as next_priv_key, which is IL, and then to_public_key, to_public_key,
[197:37.90] so as far as I can tell, I've transcribed this correctly, it returns back HDKey, and
[197:47.06] this returns back, this does not return back HDKey, but where it's actually called, does
[197:54.38] return back the HDKey, because it combines it with the other properties, so here, console.log
[198:05.50] chain and keys process.exit, let's just have that run, oh, whoops, oh, ain't it always
[198:20.22] the way, I forgot the await, that's one of the things that the tooling really ought to
[198:26.50] catch, it really, really ought to catch, there we go, dollars to donuts, now it'll pass,
[198:48.50] it gets me all the time, the tooling really should catch that.
[199:08.74] Alright, let's go through and just see where our little hiccups are, why it's griping about
[199:28.58] this, I don't know, eh, wait, oh, we don't have a decode in here, noted.
[199:57.62] Okay, so we need to add a decode here, noting that, probably these encodes as well, it probably
[200:11.26] is, let's see what it is, Elder Scrolls, the Vatican in Jamaica, by M. Benson, featuring,
[200:21.18] and then it faded out, yeah, so this is OC Remix, we're currently listening to the chill
[200:31.42] tag, which I don't 100% agree that everything that's popping up is chill, that one was.
[200:41.86] Alright, derive account, we're gonna, I think we're gonna get to this tomorrow, or Monday,
[200:52.46] because I don't think I've got it in me tonight, okay, and then, oh, of course we need to have
[201:11.68] derive, HD derive helper options, there we go, okay, so that one's pretty much fixed.
[201:35.68] Advanced Substation Alpha Subtitles, as-is, what is that?
[201:48.24] Is it for streaming?
[201:56.24] Sounds like it would be.
[201:57.24] Alright, I'm very, I'm very pleased with the progress today, I think this is a good place
[202:02.40] to call it, because I really, the week before last, I was just so gung-ho, it's so weird
[202:08.80] being in my mid-30s, because I feel like I've got the energy of a 20-year-old half the time,
[202:15.80] and then the next week, I'm just like, shouldn't have done that, so last week I was staying
[202:25.36] up until 3am, almost every single night, and just having a great time, I was super excited,
[202:32.12] super happy, and then this week, the week started off with a bunch of meetings, and
[202:37.96] then I did do, I was working on one project that I was personally really excited about,
[202:44.20] because I'm excited about this too, but I had a personal project I was really excited
[202:48.48] about, that was Aliasman, I think there was another, there was another project I was excited
[202:54.36] about too, oh, it's the, I'm working on my own language, with somebody else, and so,
[202:59.76] I was working on the language definition, and I was really excited about that too, and
[203:03.40] I just stayed up too late, and then, whenever I stay up too late, I start getting sneezes
[203:08.76] and just, you know, basically I get a cold, I can get a cold on command, all I have to
[203:14.64] do is stay up with only 5-6 hours of sleep for a week straight, and I get a cold, every
[203:21.40] single time, and so, blah, kind of sucks, oh, it's for video on demand, well that's
[203:30.12] what I meant, real time, real time streaming, that's what I, did I say live streaming?
[203:36.52] I meant that, like what you were talking about before, with the HTTPS stuff.
[203:48.84] So your username is very intriguing to me, because it's, it's so many, ah, what's
[204:00.56] the word, because it's not a double entendre, though it kind of is, and it's not a portmanteau,
[204:06.28] though it kind of is, you're just taking all of these words, that any, any segment of the
[204:14.32] words can have meaning, but then all together they don't.
[204:19.72] Because sin is a word, devil is a word, love is a word, pie is a word, but all of it together,
[204:32.96] and dev is a word, that's it, dev is a word, and I is also a word, it's just, it's so many
[204:43.76] overlappings of words, that you could read it so many ways, sin dev, I love pie.
[204:52.00] You could say it that way.
[204:57.12] Oh, well, the thing is, that might be what it's supposed to be, but when I look at it,
[205:11.20] I just see a bunch of overlapping layers, and I mean, I guess eventually I got to the
[205:19.26] sin dev, I love pie, but, yeah, okay, anyway, if you're interested in the alias man, neat
[205:37.32] little project I've been thinking about for years, literally for years, and took me four
[205:44.08] hours to get it to the point of being able to release it and feel good about it, but
[205:48.88] it was years in the making, okay.
[206:06.72] One second here, okay, but I'm, I'm closing up on this, I think.
[206:36.68] I'm just going to go ahead and pull out a few things, mainly derive account, we're going
[206:48.12] to get there, but I don't want to include it in this, I don't want to just include empty
[206:59.88] code in this, alright, let's see if we can do this, SaberJS, I'll take a look at it.
[207:26.60] Nice, lots of commits, that's good, got some stars, it's got a pear, an apple?
[207:56.04] Okay, cool.
[207:57.64] I'm going to star this as well, this is something that at some point in the future I, I could
[208:05.96] definitely see myself wanting, and I know somebody else who might be interested in this
[208:11.52] too, I'm actually going to post this in another Discord, or, well, I'll wait, I'll wait to
[208:27.36] actually post it, I'll put it in a notes to self, because I've got to have a little more
[208:31.34] conversation with this guy before I make any suggestions, because the project that he's
[208:36.42] working on, I don't know if he's worried about video with subtitles at all.
[208:42.36] I would want that, but I don't know if it's something that he's actually interested in,
[208:46.12] so I'm just going to, I'm just, I start it, put a little note to self, but I think this
[208:53.32] is cool, that's really neat, you got a lot of people involved in it too, that's great.
[209:14.16] All right, it's supposed to be hair, yeah, you might want to get on Fiverr for that one.
[209:31.56] Most of them don't contribute anymore, that's fine, I mean just somebody, somebody being
[209:35.24] interested enough to update documentation is great, you know, so here's my best project.
[209:43.90] This is my best project, you will probably find this useful, if you haven't already been
[209:47.78] using it.
[209:48.78] I'm finding that more and more it's becoming just a standard tool that people are generally
[209:54.98] aware of, and I'm really happy and excited about that.
[209:58.94] But this is Webby, and Webby is a way to quickly install the tools that you need.
[210:03.06] So for example, Node, you, there's, I won't enumerate all of it right now, but there's
[210:09.74] probably a number of problems that you've encountered when installing Node historically,
[210:14.80] and this makes sure that none of that happens.
[210:18.38] And it's very quick and fast, there's no, it's not like with Brew, where you have to
[210:23.82] update an entire ecosystem of things, each one of these installers is individual to itself.
[210:32.66] And then there's a cheat sheet included, and there's lots of tools.
[210:35.58] If you haven't been using Caddy, Caddy is one that I'd recommend to everybody, Phish,
[210:42.94] Caddy is a Let's Encrypt enabled web server, Phish is a modern shell, it's not, I don't
[210:49.90] recommend it to anybody for scripting, but I highly highly highly recommend it as your
[210:53.62] shell.
[210:54.62] It's got great autocomplete and history, it's fast, Vim Essentials, if you're a Vim person,
[211:03.18] it's just a quick and easy way to get set up without a lot of configuration, well with
[211:07.22] zero configuration, actually.
[211:10.58] Ducty and SSH, RipGrip, JQ, YQ, RipGrip, SD, FD, BAT, all the, basically the modern core
[211:28.98] utils, Hexel, so if you're not familiar with the modern core utils, most of them are written
[211:33.78] in Rust, but they're things that you just, you gotta have.
[211:41.62] You gotta have Schwumped, Shellcheck, WatchExec, Hugo, that's, I wouldn't really put that as
[211:48.54] core utils, but yeah, lots of good stuff here.
[211:51.46] Anyway, what I was gonna say is on this, so we've got 63 contributors, and there's only
[212:02.46] a few of them that are regulars.
[212:04.86] If we look at lines, this is really weird.
[212:11.50] So this person has, so the core contributors are myself and Ryan, oh, Ryan's commits aren't
[212:23.90] showing up because he mostly, most of his commits have gone into the frontend.
[212:30.46] That's what he's been working on.
[212:31.78] He's had very few commits in the backend.
[212:34.20] That makes more sense now.
[212:36.66] And then this person, I don't even know, I don't even remember what he did.
[212:40.58] I don't remember this username.
[212:43.86] Alright, so he actually worked on quite a few things.
[212:48.90] Go him.
[212:51.06] And then Yarun, he's a core contributor, and you know, he hasn't actually made much commits,
[212:57.14] he's not working on this on a daily basis.
[213:01.42] Duncan, he's hung around a bit.
[213:08.18] He was a core contributor for some Windows stuff, I should probably remove him from Midaccess
[213:13.58] by now.
[213:14.58] Jojobite is a core contributor, and he's done actually quite very little, but the one thing
[213:23.70] that he did was really important, and he reviews.
[213:26.66] So what he has committed, he's committed something that was very important, yes, the help command
[213:38.64] for Bash and for PowerShell, which was awesome, really really awesome.
[213:45.26] But mostly what he does is help review, and Yarun helps review as well.
[213:51.34] And then a lot of these other people, oh Josue, he hangs around sometimes.
[213:55.58] Vilarn, I didn't realize he was already in here.
[214:00.30] So some of these people are part of the community, the BeyondCode community, that's what the
[214:05.90] Discord is for.
[214:06.90] Oh, let me see if it, yeah, so it'll work with Arch Linux, yeah, it'll work with anything,
[214:14.30] it's all POSIX.
[214:17.18] Now the Servicemen is one of the tools on there that's referenced a lot.
[214:23.46] I would love help getting that to work for Arch Linux.
[214:26.66] At present, I don't think it does, because I think Arch Linux isn't dumb enough to use
[214:31.66] SystemD, but that's the most popular one, and so that's what's supported presently,
[214:36.74] and that's what I needed, so I haven't added some, I haven't added other stuff yet.
[214:41.42] Anyway, so, there's little spurts here and there where we work on it.
[214:46.66] Okay, let me get back to this, I need to wrap this up, or get this to a good, get this into
[214:54.22] a commit here.
[214:56.54] Okay, derive child.
[215:02.54] All right, this is, yeah, this all looks good.
[215:26.26] Whoops.
[215:33.50] Okay, so I gotta think, what do I have, let me take a look at my piece of paper here.
[215:59.22] Okay, now that we got this thing as a pure object, and things have pretty much been simplified
[216:07.94] down as much as they can be simplified, oh, so, let me get back to that, so, Webby goes
[216:16.82] from the principle of, if you're satisfied with Pac-Man, I don't know that you would
[216:21.28] need Webby, Webby is all stuff that is pretty much zero dependency.
[216:28.66] There are a few things where something might need node to be installed, but there are no,
[216:38.14] there's no, none of this code, almost exclusively, none of it is C code, and if it is, then it's
[216:45.90] something like Python, where everything installs into .local/opt, so there's no conflict with
[216:55.58] any of your system stuff, and that's one of the, the core tenets are this, we wanna be
[217:01.82] able to install stuff very quickly, you wanna be able to install it without having to use
[217:06.34] sudo or admin, you wanna install it without a package manager, and without changing file
[217:12.86] system permissions, so this is no conflict, and these are not patched revisions, like
[217:20.18] a lot of the maintainers of Linux distributions and whatnot, they'll put in little tweaks
[217:26.78] here and there.
[217:29.40] These are all unpatched, and if there is some sort of config change, if there's something
[217:34.50] that's different from the default install, which is very, very rare, but there is in
[217:40.22] just a very small number of cases, if there is something that's different from the default
[217:44.84] install, it'll be documented in the cheat sheet.
[217:51.42] So this is very, very, very, these come from the GitHub releases, what Webby does is it
[217:59.18] pulls GitHub releases, so that you always get the latest thing, and then it has the
[218:05.70] scripts are, hold on, I gotta sneeze again, the scripts are put in so that, and they're
[218:16.00] very, very small in what their base is, but the scripts just basically describe, you either
[218:24.90] need to use tar to unpack this, or zip to unpack this, or xz, or gzip, or whatever it
[218:30.96] is to unpack it, and then this is where it needs to move.
[218:36.66] So it's a very, at the high level, it's very simple.
[218:40.64] There's a lot of detailed complexity, so for example, on macOS, you have to remove the
[218:45.96] quarantine bit on things that you download before you can use them.
[218:52.40] So there's some small things like that that end up adding a reasonable amount of complexity
[218:59.62] in the scripts, so the scripts are longer than I would like them to be.
[219:03.64] Since it's been a few years, and we kind of understand better now what all the constraints
[219:07.64] are, I think that I could get the scripts down to half the size, because there's far
[219:11.30] fewer edge cases now, now that we really understand things, than there were when we started.
[219:17.56] And some of the assumptions we made at the very beginning were wrong, and so some of
[219:21.32] the edge cases for those assumptions are still in the scripts, even though they don't need
[219:30.24] to be, it's just they haven't been removed.
[219:33.18] So they do no harm by staying there, they're just not really active, or not effectual.
[219:40.00] But yeah, it's just Git, and it doesn't have to be GitHub releases, there are a few different
[219:47.38] release modules, it works with Gitty, it works with, what's that other one, it works with
[219:57.30] the Go release, Flutter release, Node release, they all have custom releases, so it works
[220:02.32] with all of that.
[220:04.26] It works with GitHub source files, that was added recently, because I needed that for
[220:14.82] the POSIX scripts, so, but it basically is just logic to say what CPU is this, what OS
[220:24.58] is this, and then what are the tools for unpacking and where does the thing go when it's installed.
[220:37.78] Do I see a clip of the output of your library?
[220:39.46] Sure, go ahead and link me to it.
[220:40.66] But I need to, I need to actually end the stream, oh there I go with the verbal stutters
[220:49.30] again.
[220:50.74] Okay, that's not what I wanted, is it?
[221:04.18] I was, let me finish up a thought real quick.
[221:07.34] Alright, I'll take a look at it, I'll take a look at it off stream though, because I
[221:12.46] need to end this stream, because this is actually, so dash incubators actually work for me.
[221:19.82] And so, I don't want to be doing a whole bunch of other stuff while I'm, I don't want to
[221:26.34] get off on too many tangents.
[221:29.34] Okay, so I'm just looking at some notes that I made a few days ago.
[221:35.82] On good old paper, I was able to think about this.
[221:41.30] So the next step is going to be to start recombining things.
[221:46.30] I'm actually really, really satisfied with the way this went, and being able to find
[221:50.38] out that yes, we could move that over, and it's only one little if condition with just
[221:55.50] one little difference, we moved some code up.
[222:00.18] The changes ended up being relatively small, and they simplified the code, they made it
[222:03.46] easier to read, so I'm really excited about that, or really, really glad about the outcome.
[222:11.46] And then next time, we're going to have to do, I think we might rename the from seed,
[222:20.74] we might rename that to derive root, and then we'll have derive account, and derive account
[222:27.10] will have the X keys methods on it, and then we'll have derive key, and that will have
[222:36.70] the ability to get the with, and the address, and then I think this library is good.
[222:59.78] There are some methods that we might want to add that are general helper methods for
[223:03.10] BIP 32, I kept on saying BIP 39 earlier, but the standard is actually BIP 32, but I actually
[223:15.18] don't think we need to spend too much time with that, it's mainly, it's more for test
[223:19.54] fixtures than anything else.
[223:22.18] It's not something that we really want to expose to the user.
[223:25.70] So I think, if I was going to spend another hour or two hours on this right now, I think
[223:32.14] I could finish it, but I'm just, I'm getting kind of tired, it's time for me to peace out.
[223:41.62] Alright, I will grab this and I will check it out, thanks for that link, I'm going to
[223:47.58] download it right now.
[223:50.10] Oh, whoa, this is, oh, okay, nevermind, yeah, yeah, yeah, hold on, let me get this over
[223:56.90] here.
[223:57.90] No, this is super cool.
[224:00.30] Okay, so you're just syncing the subtitles here.
[224:07.94] This is awesome.
[224:12.26] Hey, you know what else, if you want to join the Discord, or contact me, just send me an
[224:21.74] email or something, let me know what anime I should be checking out.
[224:26.74] Karaoke too, huh?
[224:27.90] That's awesome.
[224:28.90] That is so cool.
[224:30.98] That's awesome.
[224:31.98] Well, I hope to see you again.
[224:34.50] You have a good night, and I'm going to see if we can find somebody, oh, I still can't
[224:39.10] raid.
[224:40.10] This channel is new, I've got a few channels, actually.
[224:44.46] Cool Age 86 is my everything goes channel, I do all sorts of stuff on there.
[224:48.78] Dash Incubator, that's what I end up doing the most, because that's work, and so that
[224:54.02] I segmented off into its own channel, and then I also have a channel for some of the
[224:59.26] meetups that I run, Utah Rust, Utah Stack JS, and I think that's it, I think I just
[225:06.42] have the four channels, but if you want to like, sub, follow here, I do the Dash Incubator
[225:12.46] work here.
[225:13.46] If you want to like, sub, follow on Cool Age 86, I do more of a variety, and sometimes
[225:18.42] I do Dash Incubator work over there, but it's when it's more stuff that I think has more
[225:23.86] general appeal.
[225:30.70] Effects and fonts and stuff, yeah, that's really neat.
[225:32.98] I did see that a little bit.
[225:34.34] I'll watch it the whole way through later.
[225:40.06] That's really neat.
[225:41.06] Actually, yeah, I, well, I could just, let me bring it over here, I can just go through,
[225:47.22] yeah, so it's got fonts, it's got colors, okay, yeah, whoa, what's that?
[225:55.38] Is that part of it?
[225:57.66] Because that's, that's, that's crazy.
[226:01.70] Okay, so this is the karaoke bit for the, that's so neat, man, that is so cool, that
[226:09.98] is so cool.
[226:13.02] Feel free to share, if you do just join the Discord, feel free to share it in the Discord,
[226:16.90] in the general channel or whatever.
[226:18.38] That is so neat, I've wanted to do something like that, I've never wanted to do enough
[226:23.62] to take it on, but I've got my own media library, and I just, this is awesome, that is so cool,
[226:29.98] I definitely, I don't know if I'll actually get around to being able to have the chance
[226:33.66] to use it, but it's something that I would like to use.
[226:36.14] Anyway, I can't raid because this channel is too young.
[226:41.38] We have to get a full 30 days in and then we can start raiding others.
[226:45.50] Animations, 3D positions, that's so cool, that really is cool.
[226:51.46] All right, well, thanks for tuning in, like, sub, follow, if you want to, I'm a little
[226:57.42] more animated usually, but today I'm just kind of, I'm just kind of tired and it's late,
[227:01.90] it's 1230, well, I mean, it's not that late, that's pretty early for me, but it's late
[227:06.58] for most people, and I got to go, so thanks for joining in, appreciate it, hope to see
[227:11.62] you again, you have a good one, adios.