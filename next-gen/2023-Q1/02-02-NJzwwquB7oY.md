---
showLink: "https://www.youtube.com/watch?v=NJzwwquB7oY"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Code Hangout: Next-Gen DASH Tools #9: Finishing DashKeys.js for Browser JavaScript"
publishDate: "2023-02-02"
coverImage: "https://i.ytimg.com/vi/NJzwwquB7oY/maxresdefault.jpg"
---

## Episode Description

A developer works on updating documentation and example keys for a cryptocurrency-related JavaScript library, focusing on improving clarity and consistency.

## Episode Summary

The developer spends several hours refactoring and updating a JavaScript library related to cryptocurrency key generation and manipulation. They focus on improving the documentation, updating example keys to use consistent test values, and adding more detailed intermediate steps to help users debug potential issues. The work involves modifying code to generate various forms of public and private keys, addresses, and hashes, as well as restructuring the output to be more informative. Throughout the process, the developer encounters and resolves various typing and linting issues, reflecting on the challenges of JavaScript tooling and type systems.

## Chapters

00:00 - Setting Up the Development Environment

The developer begins by setting up their development environment, discussing recent changes to their vim configuration and linting tools. They express frustration with some recent updates that have made their workflow more difficult, particularly related to error reporting in their code editor. The conversation touches on the challenges of maintaining and updating development tools.

26:52 - Refactoring Code and Adding Type Definitions

The developer starts refactoring the codebase, focusing on adding type definitions and improving the structure of the code. They work on incorporating base58 check, ripemd160, and other cryptographic functions into the main library. This process involves careful consideration of how to structure the code to be both type-safe and user-friendly.

54:23 - Debugging Type Errors and Improving Documentation

A significant portion of the stream is spent debugging various type errors that arise from the refactoring process. The developer discusses the challenges of working with TypeScript-like type annotations in JavaScript and the limitations of current tooling. They also begin updating the documentation to reflect the changes made to the code and to provide more detailed examples for users.

152:17 - Generating and Documenting Example Keys

The developer focuses on generating a set of consistent example keys to be used throughout the documentation. They create various forms of public and private keys, addresses, and hashes, ensuring that all examples use the same underlying test values. This process involves careful consideration of how to present the information in a way that will be most useful to end users.

244:26 - Finalizing Documentation and Adding Debug Information

In the final portion of the stream, the developer works on finalizing the documentation. They add more detailed intermediate steps and values to help users debug potential issues when implementing the library. The developer also reflects on the importance of providing clear, consistent examples and how to anticipate and address common user mistakes.

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
[01:28] you
[01:30] you
[01:32] you
[01:35] you
[01:37] you
[01:42] you
[01:48] you
[01:55] you
[02:01] you
[02:03] you
[02:19] you
[02:22] you
[02:27] you
[02:29] you
[02:39] you
[02:49] you
[02:52] you
[03:02] you
[03:12] you
[03:14] you
[03:27] you
[03:29] you
[03:41] you
[03:53] you
[03:55] you
[04:05] you
[04:15] you
[04:17] you
[04:27] you
[04:37] you
[04:39] you
[04:45] you
[04:57] you
[04:59] you
[05:19] you
[05:21] you
[05:31] you
[05:41] you
[05:43] you
[05:53] you
[06:03] you
[06:05] you
[06:11] you
[06:21] you
[06:23] you
[06:25] you
[06:30] you
[06:40] you
[06:57] you
[06:59] you
[07:14] you
[07:31] you
[07:33] you
[07:39] you
[07:51] you
[07:53] you
[08:13] you
[08:16] you
[08:30] you
[08:33] you
[08:35] you
[08:37] you
[08:48] you
[08:50] you
[08:52] you
[09:07] you
[09:09] you
[09:29] you
[09:31] you
[09:42] you
[09:44] you
[09:58] you
[10:00] you
[10:14] you
[10:16] you
[10:27] you
[10:29] you
[10:39] you
[10:49] you
[10:51] you
[11:01] you
[11:11] you
[11:13] you
[11:23] you
[11:25] you
[11:35] you
[11:37] you
[11:53] you
[12:08] you
[12:11] you
[12:21] you
[12:29] you
[12:31] you
[12:41] you
[12:53] you
[12:55] ah screw it let's just dig into this early i don't want to wait all day i
[13:02] don't have all day to wait you have all day to wait nobody's got all day to
[13:05] wait let's just get into this okay so first and foremost uh okay good
[13:11] camera's all set up everything's looking good great all right so where'd my
[13:14] mountain dew go somebody give me a mountain dew here
[13:18] okay all right got the mountain dew oh and my video is a little choppy because
[13:21] i still have the other video preview software open let me close that out all
[13:26] right good so i'm a little bit of trouble with the camera uh while i was
[13:30] getting set up so uh here is our good friendly mr mountain dew for the morning
[13:35] and uh as you can see it's sweating or maybe you can't see but you should be
[13:39] able to see it's sweating it's sweating was out in the snow and it got hot now
[13:42] it's now it's sweating so a nice warm mountain dew is an ice warm
[13:49] mountain dew as i always say oh and this one's got real sugar so pop it up my
[13:54] friends let's open focus and dig into this
[13:58] i'm not sure if i'm going to like it with real sugar real sugar tastes
[14:01] different than corn syrup and you get used to corn syrup you know
[14:04] does the body good
[14:07] um that is good syrup's got a little our um
[14:15] sugar's got a little sharper taste you know or at least that's kind of how i
[14:19] think of it maybe just because the granules are
[14:22] you know they got a little sharp edges to them whereas corn syrup's just a
[14:25] liquid you know corn syrup's a little more
[14:27] syrupy and and and sugar's a little more crystal and
[14:31] i don't know why that would make the taste different in liquid form but it
[14:35] does for me okay so let me explain what we're going to
[14:40] do here real quick before we get started hello
[14:42] everybody welcome it's nice to have you uh please come again and and you know
[14:47] stay if you want to but the thing that we're going to be
[14:49] working on is actually not in the hd key repository
[14:54] right now we're going to come back to this
[14:56] but we are i think i think i fingers crossed i hope
[15:00] i hope that this is one of the last two days that we're working on this project
[15:04] in this incarnation of it we're going to go back to dash keys
[15:11] and we are going to bring in all of the dependencies that are
[15:18] basically just always going to be required anytime you're doing any of the
[15:21] functions that dash keys provides so we're going to make that one thing
[15:25] and this i would like to reference i was actually
[15:28] listening to the clean architecture book let's see clean
[15:33] architecture by uncle bob and here it is i'll i'll put a link in
[15:39] the chat for you just give me a second here let me grab
[15:43] it here is it here we go
[15:47] uncle bob's clean architecture architecture there we go there's uncle
[15:54] bob's clean architecture i put it in the chat
[15:55] it's right right there and then i'll bring it up on screen just so you can
[15:59] give it a look but i was listening to this and it's and
[16:04] he describes exactly what i was starting to do here already which is
[16:09] that things that change together go together
[16:12] and things that get used together go together and there's somewhat of a push
[16:15] and pull between these uh but you you know you
[16:19] just find the right balance for your project and
[16:22] i think that i've you know i've already said i think that
[16:25] i've done that in terms of oh where did did do we have more than
[16:28] one of these okay we can get rid of this noble
[16:33] crypto window in this window oh that one i
[16:36] might want to come back to i was going to actually
[16:39] answer this stack overflow question i had started writing it out in one of the
[16:43] videos and then as i was writing it out i
[16:47] reviewed some things and realized i was doing something wrong and then chose to
[16:50] do it a different way yada yada blah so okay but dash keys this is where we're
[16:56] at let's go roadmap to v3 and then dash
[17:01] keys so we're just going to absorb its
[17:04] dependencies and republish it and its dependencies
[17:08] are base 58 check ripe md 160 and then i'm
[17:12] actually not going to absorb the sec p256k1 because that is the one thing
[17:17] that's a bit unique that i could see that you might want to
[17:20] swap it i'm actually going to eliminate um well i'm not going to eliminate i'm
[17:23] going to turn the functions that use that into
[17:25] util functions instead
[17:32] and we are going to let's generate some keys real quick
[17:37] while we're here in dash hd so we should be able to see what's our mnemonic
[17:42] our mnemonic uh i don't want this mnemonic let's go
[17:46] oh okay we can do mnemonic and zoom on it so i said before
[17:50] i want all the documentation across the board to use the same
[17:53] keys so we're going to use the zoom on it and we're going to use
[18:00] the secret that is well the well-known secret which is trezor
[18:04] and then we're going to uh point this at zero zero zero zero
[18:11] and this is what we are going to start with
[18:15] um and then i think i want to put a few others of these in here as well
[18:20] so if we just if we did a search for this i'd be highly surprised if this did
[18:24] not show up in search results actually i wouldn't because it's probably not
[18:27] going to show up in search results in the dash community but if we did the
[18:30] bitcoin version of this i'd be highly surprised if it doesn't
[18:33] show up in search results because that's going to be a pretty common
[18:36] um example key because that's the first well maybe not because i chose zoo zoo
[18:42] zoo zoo zoo because of all of the test whoops
[18:46] of all of the test phrases in the in the test database this one's super easy to
[18:51] remember zoo zoo zoo zoo zoo zoo wrong and wrong is kind of in this case a
[18:56] triple entendre because it's literally the checksum
[18:59] and checksum should be right but they're wrong
[19:03] and if you were to guess what's the next word in this sequence
[19:07] you would say zoo but you'd be wrong so there's there's my
[19:11] my triple entendre for you um but yeah so i want to go ahead
[19:19] and just pop out probably let's see let's do this one that one
[19:25] i don't know i'm i'm just going to take a few of these
[19:28] and we're going to use them as let me get back over here we're going
[19:33] to use them in dash keys we're going to update the examples to be
[19:37] that what the examples give out if they give out anything here
[19:41] so dash keys generate for example so i think i'm going to make this this is
[19:46] actually going to go away so we're not even going to have that
[19:50] um but all all of the examples i'm going to update to use
[19:55] the the zoomonic
[19:59] zoomonic
[20:02] okay so let me take a look at the readme as is
[20:11] and see if there's anything else i notice that needs to change other than
[20:14] those few keys and then that we're going to bundle some stuff
[20:18] okay so we have a global install i think we should swap that
[20:22] i think we should have a dash key cli because the reason for this is i don't
[20:25] like having to include cli dependencies for
[20:29] things um
[20:33] let's see what what have i got here yeah i think that that's going to become a
[20:38] separate project so we're going to have a dash key cli and if you global
[20:43] install dash keys then
[20:48] it will just uh and install it'll give you a warning or something i
[20:54] don't know
[20:56] yeah so i think i think we're going to need to change that
[21:07] we're going to change this okay that makes it makes sense
[21:12] but i would say we actually want to use dash hd
[21:17] well we'll get there we'll get there eventually this is correct for what it
[21:21] is all right so we got the generate we've
[21:23] got the whiff to adder we've got the buffer from so i need to figure out what
[21:26] that that uh private key oh i think the
[21:30] private key now it's kind of something random
[21:34] because the the mnemonic ends up being f f f f f f f f it's all f's until the
[21:40] checksum okay browser so we're going to clean
[21:44] this up that's the main thing we're going to do
[21:46] here
[21:48] and we're going to move the cli out to its own package so let's go ahead and
[21:52] create a new repo for the cli and one thing that i would do but i'm
[21:57] not going to do is actually
[22:01] that sugar hits different
[22:04] i like the aftertaste a lot more of the real sugar
[22:08] it's noticeable anyway we're going to make a new repository here we're going
[22:13] to call it dash keys cli i might call it i'm not going to
[22:19] call it yeah.js i'm going to call it.js because
[22:22] in the future if i'm if i'm allowed to do it and there may not be a good use
[22:26] case for it yet but i would like to rewrite all of
[22:30] these tools in go they need to be in javascript because we need something
[22:33] that works in a browser i don't know if i can justify the cost
[22:37] of rewriting them in go more importantly i don't know if
[22:39] somebody else can justify the cost of me rewriting them ago i can justify it
[22:43] easily um i think that some of our newer tools
[22:47] are being written in go but anyway so this is going to be
[22:51] whatever whatever the name of dash keys was
[22:55] you know and this actually should be bun i think that's what this should be i
[23:01] think this should we should uh i need to get jojo bite on board with
[23:04] this but this should be a bun tool
[23:09] actually i'm gonna have these on that because
[23:17] although bun is fixing stuff all the time things went from completely not
[23:23] working in a month to working for a number of these crypto
[23:28] apis the other problem is that
[23:32] things do break in bun still so let's get let bun get closer to 1.0
[23:38] but i would eventually like this to be a tool that's a bun tool rather than a
[23:41] node tool because node is large and huge and
[23:45] bun is small and concise and so between the two bun
[23:50] aligns much more with my philosophy of you know good code
[23:54] so this is a cli for um for dash
[24:01] private keys
[24:06] with private keys and payment addresses
[24:13] pub key hash
[24:20] public key hashes
[24:23] for
[24:27] for for dash keys um let's see
[24:34] let's see generate validate create creates the same
[24:47] let me create whips whiffs private keys actually let's just make this
[24:53] a little simpler whiffs and pay addresses that's private keys and
[24:59] public key hashes
[25:03] dash keys cli all right there we go this is going to
[25:12] be public yeah sure we can add the readme yeah we
[25:17] can add repository yeah we can add the license
[25:22] all right so i'll just move some stuff over here
[25:26] and then this
[25:36] let's see
[25:43] rmdir cli git submodule add cli
[25:51] so there we go so let's go ahead and do that first and foremost
[25:55] so we're going to get checkout dash b um and i'm going to call this i don't know
[26:03] cleanup finalize
[26:07] we've already published this we're probably going to have to bump the
[26:12] version on it all the way oh yeah yeah yeah we'll bump it to 1.0 that's not a
[26:15] problem at all so we're gonna we're gonna let's call
[26:20] it something a little better
[26:23] to v1 and beyond
[26:29] so let's go ahead and get this out of the way how's everybody
[26:33] everybody's day going it's wednesday it's the first of february it's a new
[26:37] moon do you know what that means that means
[26:39] that my daughter's mario calendar gets to flip from yoshi
[26:42] to princess peach it's a pretty good pretty good advance i would say okay so
[26:50] here we are
[26:52] um
[26:55] and this is going to be ref add submodule
[27:00] for cli
[27:10] there we go that's it okay and we'll push this up and that's that
[27:17] all right now let's think about the rest of these how are we going to do this so
[27:22] with the base 58 check
[27:29] let's see here
[27:31] dash keys.js do we have an index.js jojo bite and i have have gone over some of
[27:47] this import export stuff and it's a little bit depressing but i think we've
[27:50] landed on the right way and why i say it's a
[27:55] little bit depressing is that it's well it's just it's depressing it's
[27:58] depressing how weird it is to have to do
[28:03] these things
[28:05] all right
[28:12] so we're gonna do i need to go back and there is going to be probably one pr
[28:19] that jojo bite's gonna need to put in on these which is he's got some boiler
[28:26] plate that i need to add so i'm glad that i didn't update the
[28:30] jswt initializer yet the thing that creates the projects
[28:33] javascript with types jswt because the way to
[28:38] update it is not the way that i thought it would be and i think that jojo bites
[28:42] discovered the right way so basically there's an
[28:45] index.js an index.mjs and then there's the whatever thing
[28:51] dashkeys.js and and so through a few layers of indirection what
[28:56] happens is if you want to use this in the browser you get to use it in the
[28:58] browser no problem it's going to work perfectly
[29:01] if you want to use it in node then
[29:06] let's see the window object becomes the export object
[29:13] if you want to if you want to use it in node it's going to work just fine
[29:17] which is what we have now but if you want to get the type information the
[29:20] type information gets a little bit wonky and so the
[29:24] workaround is to retype
[29:29] the type information to to retype the export object and then export it again
[29:34] and so this requires a minimum of three files you have
[29:37] your your index file your index.mjs and then your file that's actually the
[29:43] real code and i've i've gone back and forth
[29:46] about this i thought i i wish that i could move to import the
[29:50] thing that keeps me from moving to import
[29:53] is that import breaks everything else you cannot use a module that uses import
[29:58] from something else so if you're somebody who is
[30:01] the 50 of developers that are just doing jquery and wordpress and stuff like that
[30:05] you would not be able to use this module if it uses import you'd have to have it
[30:09] transpiled and then you know it just it's more confusing
[30:13] somebody who uses import can use this module without a problem other than the
[30:16] type you know we've got the type issues
[30:19] anyway that's kind of an update on that situation okay
[30:23] so i need to go into was it dash hd i think is i think is
[30:30] where we have the best version of this so far
[30:33] so it looks like this except i think we don't do
[30:36] global this
[30:39] no this one no that's not it that's not it hold on
[30:45] let me switch over here
[30:49] what what are my unstaged changes
[30:56] dash hd what was i working on the other day oh it was hd key
[31:01] okay sorry so let me go back into hd key
[31:05] okay and this this little snippet whoops at the bottom here
[31:11] seems to be the best we can do as far as i can tell
[31:17] ryan suggested that i throw it out to reddit to see what they have to say but
[31:25] i don't want to throw it out to see what they have to say
[31:28] okay and this is confusing
[31:32] my i updated my tools and vim that's never been a problem before but
[31:39] this new version of i don't know whether it's js hint or
[31:42] what it is probably an update to ale now the error
[31:45] message come beside the code but that's super annoying while writing code
[31:50] happening asynchronously i don't want that check i mean i like it when the
[31:53] checks happen but it's it's super annoying the way that
[31:57] it's being the way that it's implemented see i mean
[32:01] that's just i don't like that showing up there
[32:06] okay so that's the whole bit and then we've got this bit
[32:16] okay
[32:20] ah see it just makes it so difficult to understand what the heck is going on
[32:26] all right
[32:30] it's like sometimes i'm in the middle of typing
[32:34] or pasting and sometimes the whatever thing is not ready yet
[32:42] all right so we're going to move this as well hold on let me grab these
[32:48] i'm going to have to check the license on these because
[32:57] yeah
[32:59] all right
[33:08] so here's what i want to do everything that's called hd key
[33:16] it's going to rename to dash keys
[33:20] that's good and dandy
[33:26] and then here
[33:30] this is a little bit different
[33:54] basically this is going to be at type any
[33:59] was it like this
[34:06] oh hold on
[34:18] okay monday at three hold on i need to answer a
[34:22] message
[34:25] i'll just give this a yes do we have the thing in
[34:28] ios where you can just swipe and say reply yes or reply now or something like
[34:32] that options no okay we don't have a quick
[34:37] reply feature yet
[34:40] okay monday at 230 i need to leave let me just add that to my calendar real
[34:45] quick because if i don't well first of all i don't even check
[34:48] my calendar so by add to my calendar what i actually mean is also text my
[34:52] wife because she'll remind me i won't remember to look at my calendar
[34:59] on monday and
[35:13] okay so i'm getting my hair cut on monday so the mop's gonna go away
[35:16] so if you love it let it know now or forever hold your peace
[35:22] okay that did not work the way that i thought it was gonna work
[35:28] that is really just super annoying i really don't like that
[35:41] so
[35:44] okay if model
[36:07] hmm
[36:10] let's see here
[36:24] oh whoops base x
[36:37] oh okay right right right
[36:40] dash keys dot base 58 whoops
[36:53] so base x i think what i did was gave it a default dictionary or something
[37:04] i think that's the only difference between the two
[37:08] okay
[37:13] so uh i oh one thing that is going to have to happen
[37:20] is that we do need to pull out
[37:24] let's see we don't we shouldn't need to do that anymore
[37:31] does not exist
[37:34] on type well it should dang it why this never gave me any trouble before
[37:48] okay
[37:53] so
[37:56] i don't know i don't know what's going on here
[37:59] we are gonna have to have some high level
[38:05] type def dash keys
[38:12] okay now i'm getting now i'm getting problems that jojo bite was talking about
[38:28] i was not getting these before i was able to get rid of this dash keys circularly references itself
[38:34] i was past that
[38:51] oh well
[38:57] let's see what we can do here
[39:01] cannot re-declare block scope variable base 58 check how so where was this declared
[39:17] ah down here got it
[39:18] okay maybe what i could do here maybe i could put these types in a different file
[39:27] hmm i think i might be able to do that
[39:37] we'll have to see at the types going in different files not a big deal
[39:44] all right there's there's where i gave the base 58
[39:58] it's library in this one i have to figure out because i don't think i wrote this code
[40:02] or even wrote sufficiently enough of it to claim any sort of copyright status let me go check and
[40:08] see make sure that we put a copyright um notice in here that's an acceptable you know normal type of
[40:17] thing um
[40:22] you know normal type of thing um base 58 check maybe i did write base 58 check myself
[40:30] i have to take a look at that what do we have in the license
[40:35] mozilla public license that that seems like i might have i might have written it myself that
[40:41] doesn't seem right though there should be because i'm pretty sure i did not i did
[40:44] not rewrite base x i may have rewritten base 58 check um but i did not did not rewrite base x
[40:52] so this this stuff this this looks like i i rewrote that pretty much from scratch
[40:56] i i can i can go with that
[40:59] okay
[41:04] okay okay so i see what we're gonna have to do we're gonna have to pull in a few different utils
[41:18] and we're gonna have to pull in a few different types of stuff
[41:22] all right
[41:24] let's see parts this isn't in a type yeah yeah yeah yeah yeah yeah ah here we go here we go
[41:48] this is where base x comes from got it
[41:50] so i just want to make sure this is clear in the read the readme
[41:54] license
[41:57] this includes
[42:01] uh base x and base 58 check
[42:12] which are derivatives of
[42:19] um
[42:24] base 58.cpp
[42:39] so what we should have here is base x base 58 base 58 check and then
[42:49] ripe md 160
[43:00] and then dash keys
[43:24] to keep the dependency tree slim this includes base x and base x which are derivatives of base
[43:33] 58 cp as well as ripe md 160. there we go
[43:45] so
[44:08] wow can i not type the letter three the letter three
[44:12] everybody knows it is the letter three correct i'm not alone in that
[44:20] okay
[44:34] so
[45:03] okay
[45:09] and then ripe md 160 we're going to pull that in as well let me go grab that
[45:16] okay and again maybe we what we can do here to keep this all working nicely
[45:25] is we might be able to do a you know like a
[45:32] c ripe md.t.js
[45:41] and then put all the types there
[46:02] and then put the code in here
[46:08] let's see
[46:23] uh
[46:27] ripe md 160.types.js
[46:38] dot ripe md 160
[46:43] so
[46:45] and then we just need here module.exports.types equals true
[47:04] and that should be enough to cause this
[47:11] to get the things that it needs and then we can have base x
[47:15] do a similar thing there
[47:21] and then we would also need that base 58 check
[47:38] so dash keys
[47:42] and we would need base 58 check
[47:47] base 58 check
[47:54] and then we could do the same for
[48:04] base x
[48:09] there we go
[48:14] oops
[48:31] okay and then we just need to move that type information out
[48:36] okay this one we're going to say is unnecessary that kind of makes sense actually
[48:42] so i think what we'll do
[48:45] let's see
[48:58] ripe md 160 is equal to object type
[49:03] ripe md 160
[49:07] and i think we have a ts ignore on that as well
[49:19] and then we could do same thing here base x
[49:27] except for it's going to be base x
[49:33] and then base 58 check
[49:42] base 58 check there we go
[49:52] all right so with that out of the way we don't need any of this but let's go ahead
[50:02] and delete the bottom first because it's easier to go um bottom up because i can always go find
[50:09] the next closing bracket whoops so down here for example and that should bring me back up to the top
[50:18] all right so we've got this array 16
[50:23] which is probably just fine
[50:28] hmm actually let me go back to this
[50:31] because i think what we need here
[50:36] is actually going to be
[50:45] ripe md 160
[50:49] and this is yeah there we go
[50:57] so we're going to have to
[51:01] pass that in like this
[51:14] there we go
[51:15] hello so we need to update our js hints to allow bitwise
[51:26] so interestingly enough to allow bitwise you turn bitwise checking
[51:33] false all right so we've got that done
[51:44] okay what is it complaining about
[51:45] ripe md 160
[51:51] used before its declaration
[52:03] that's not true because it's declared up here
[52:11] it's declared right here
[52:12] oh wait we did we we declared it twice what did i how did i mess that up
[52:22] as defined but never used but it is used it's used right here
[52:38] um i am very confused as to why it's giving me grief over those
[52:43] all right base 58 check that's already declared up there there's probably some
[52:51] other syntax error lower down that's keeping it from knowing what it's doing all right base 58
[52:59] all right base 58 check
[53:07] okay and then a lot of this stuff i probably just need to call back and then type def
[53:17] no no no yes at type
[53:22] and then when we type something i think we put it in brackets that's probably what i didn't do earlier
[53:32] so this one we're going to call it base 58 check create
[53:37] i mean we could just call it create probably
[53:54] that should be good and then we can move that out to base 58 and the type checks
[54:03] and that should do just fine
[54:07] all right cannot find name create because it's base 58 check dot create
[54:21] hmm
[54:28] i see what i think i see what's going on here maybe not 100 sure base 58 check
[54:42] oh come on you've got to be kidding me
[54:47] hey
[54:53] it's right here
[54:59] whatever i'll figure this out later
[55:08] what does it mean okay base 58 check which i've already declared that this is of type base 58
[55:27] check so why is it giving me such grief all right i'm just gonna have to get further through here
[55:32] and figure out what's going on okay so
[55:43] all right
[55:48] let's just get this to the point where it runs and passes tests again so i do think
[56:01] that we need to bring this one up but here we're going to have base 58 check
[56:09] and then yeah so this one
[56:24] and pretty much
[56:31] and this one's going to be the same function base x
[56:45] and then
[56:52] hex to an eight array base x so there we go so all the way up at the top
[56:58] we're going to need to pull crypto out for everybody everybody gets a crypto
[57:03] let's see um
[57:08] at type well i guess it still need that txts ignore but we need
[57:17] at type crypto
[57:20] window.crypto
[57:27] maybe within here anywhere that window is referenced
[57:43] it needs to be referenced as
[57:45] capital w window
[57:49] and then we can reference it this way
[58:02] there we go
[58:09] all right
[58:20] block scope
[58:37] this may need a name like
[58:39] init ripe md 160 it's kind of a weird setup
[58:58] that may be what we need to do though
[59:13] ripe md 160 is going to need to be of type ripe md 160 fair enough
[59:33] oh okay those are easy enough to fix awesome
[59:42] all right data
[59:56] so this would be
[60:03] ripe md 160.ripeupdate okay
[60:15] so
[60:23] hold on hold on hold on
[60:38] so
[60:47] this does export ripe create
[60:55] and 100 exports the type ripe create
[61:05] it 100% exists on
[61:07] ripe md 160 okay let's let's see what's going on here i think i think i see what's going on here i
[61:20] think that this would need to be .ripe md 160 i'm saying it has no exported member but it does
[61:29] i just saw it okay again probably just going to have to ignore that
[61:33] whatever you say
[61:39] maybe we need to do a little bit more with the type stuff
[61:51] i'm just going to try something here do module.exports
[61:53] do module.exports
[61:56] let's let's do this let's do at
[62:04] let ripe md 160 equals
[62:18] at type ripe md 160
[62:24] and then let's go back into that ripe md 160 whoops
[62:42] all right
[62:47] and we don't have the typing there so let me go back into this one
[62:53] and grab the types from the bottom we don't have the types from the bottom
[62:57] ah
[63:01] no it's right there there's the that's the type right there that's the type that's got it
[63:11] that's the type that's got it
[63:12] whatever again i'm just going to try to get this stuff working
[63:26] and i'll worry about this type information crap later
[63:30] hex to uint8 array what do we need that first we need it first on line 373
[63:41] i think i'm just going to bring that up to the top and we're going to have probably a utils i
[63:49] don't know hex two
[64:00] so
[64:10] so
[64:19] all right i think what i'm going to do here i'm going to take this back up to the top
[64:35] and i'm just going to compare these to see if they're actually any different they're probably
[64:43] the same function or pretty darn close but i'll just compare real quick
[64:49] all right so this whoa what is it doing come on now
[64:59] so
[65:08] all right so this one's just broken down a little bit more it looks like
[65:22] and where does index come from in this one
[65:27] uh okay this one's a little bit better because here the index is incremented separately
[65:34] okay i like this one better so we're going to go with this one
[65:39] and i like the
[65:43] oh whoops
[65:47] i like the docs better on that one
[65:53] cool all right whoa whoa whoa whoa whoa stop stop stop stop oh man my linter is driving me
[66:12] nuts right now
[66:13] i've got to get better linting tools i'm just so sad with the state of linting in javascript it is
[66:21] horrendous
[66:21] why did i upgrade how can i go back the new tool just works so much better than the old one
[66:35] why did i upgrade how can i go back the new tool just works so much worse
[66:40] why did they change it it was working
[66:42] hey mighty house ink what's up
[66:48] i i don't know you tell me
[66:59] all right so here's utils dots see that how the why did they change it why why break my workflow
[67:11] oh man and this isn't the kind of thing that i keep track of the versions of i expect that if
[67:20] something's been working for the last five years i expect it not to update i expect to not get a
[67:25] new version i expect it to be complete um we
[67:33] ludoplex
[67:38] ludoplex i don't i don't remember the name ludoplex but go ahead ask away ask the perplexing
[67:49] questions okay so there's that one how can you do this to me
[68:12] oh wait module dot exports there we go
[68:15] all right defined but never used i can live with that callback
[68:35] all right let's try this again hey type of function declaration
[68:41] must match the function signature
[68:45] i just don't i just don't understand why it's upset
[68:53] so
[69:01] all right let's try this module dot exports equals function whoops dot create
[69:15] let's see if this works
[69:20] so
[69:33] why is it telling me there's an unexpected token what unexpected token that could there possibly be
[69:40] oh this thing yeah that linter is really getting on my nerves
[69:48] i'm i am seriously gonna have to turn my linter off and i've i've been using i think this is jshint
[69:54] i'm not sure it said yeah it says it's jshint i'm going to have to turn off jshint because
[69:59] it is driving me flipping insane i'm going to have to let me let me see if i can just
[70:07] check out an earlier version um so vim plugins no it's gonna vimpack plugins no start yeah uh vim jshint
[70:21] uh or maybe it's ale
[70:26] okay january 29th
[70:36] i'm going to go to vim ale real quick and see if i can just downgrade because i think they
[70:43] released a major update that i got by mistake let's see how many tags do we have tags 3.0
[70:50] 2.7 let me get back to 2.7 let me see if i can do that
[70:58] because this the new release is just driving me bonkers i cannot code with it popping up with
[71:05] erroneous areas i mean just it's not helpful i am typing i'm in the middle of copying and pasting
[71:12] wait until i save or something don't just flood me with so many errors okay so get checkout
[71:23] all right i'm going to go up one we're going to let me go into here rumruff ale
[71:31] git clone i'm just going to clone the whole repo
[71:34] and we're going to go back a couple versions and see what works
[71:41] that seems like that might be a little too far i mean it's been
[71:50] let's see when was this tag december 25th yeah that one
[71:55] okay let's try v3.2.0 git checkout v3.2.0 whoops
[72:05] all right
[72:14] because i don't think it was jshint's fault i think it was ale's fault okay there we go
[72:27] let's see if they've got any complaints about this yet
[72:41] let's see
[72:50] okay
[72:56] i i don't know
[73:05] go back to v3.2.0 style error reporting hundreds of error messages every
[73:16] not hundreds of of inline error messages uh i accidentally
[73:29] updated to the latest version incidentally not really accidentally but not intentionally
[73:37] updated to the latest version and now i get hundreds of inline error messages
[73:47] that are indistinguishable from comments every time i
[73:55] change a bracket this makes it nearly impossible
[74:13] to read my code
[74:20] it's quite often that i start writing a new function in the middle of a file
[74:42] um and don't
[74:47] a file and then all these messages pop up before i can finish typing
[74:59] uh the closing bracket
[75:07] so
[75:13] or i cut and paste
[75:20] uh some partial code to fill it out differently than a similar block
[75:34] and boom i'm so flooded with errors that i can't even see which line i'm on
[75:56] at the very least
[75:57] for now i've downgraded to v3.2.0 because v3.3.0 is
[76:17] not usable for for writing code in real time
[76:29] is there a way to turn that feature off
[76:39] so okay
[76:50] so
[76:57] okay i'm just going to try that we'll see what happens
[77:18] hey that seems like it worked
[77:19] ah crap oh i hate these i hate these so much
[77:26] i think what this means i don't want to play with this right now but i
[77:32] i've said this before i think what this means i think this is the same as this i think
[77:41] this i think
[77:42] all right i guess we're gonna just go ahead and allow plus plus here
[77:52] turn plus plus checking off
[77:57] oh that's that's just that's just
[78:09] okay type of function declaration must match the function's signature i don't know what that means
[78:35] let's try this one more time okay ripe update
[78:39] callback right update returns empty 160 this is correct i just don't understand
[78:49] why it's complaining i'll have to get together with jojo byte on this one
[78:54] because i i mean i guess i could just pull all the types into the same file but
[79:04] yeah it went a little cray cray on me
[79:06] all right and again why this is saying the variable is used before its declaration beyond me
[79:18] considering that it's obviously declared right here
[79:23] how is it both defined and never used and well we'll figure it out
[79:29] we'll find out how okay and then there's the base 58
[79:36] create encoder base
[79:49] check base x dot types oh we don't have any types for base x yeah that's okay
[79:56] all right so that's kind of annoying
[79:58] and i kind of want to move this down
[80:06] i kind of use the the ripe and move the ripe md down as well
[80:20] okay here we go all right this also needs to be utils sha256 um that needs to go on utils
[80:45] utils dot utils dot utils dot
[81:04] so
[81:05] let's just put this here
[81:33] so
[81:35] wait uh-oh
[81:49] duplicate identifier that's fine we're going to fix that in just a second
[82:02] wait i am a little confused oh there it is literally the code was so similar i didn't see
[82:08] wait hold on so this is line 60 where's the other definition of it
[82:17] oh oh they look really really similar those lines ah there's the base 58 check and the ripe md that
[82:27] are being re-initialized got it okay now i'm not so confused on that front
[82:35] all right so we don't need that crypto is not going to be used that way
[82:54] these look exactly identical
[82:56] and we are going to get rid of the node way of doing that
[83:04] and this looks i'm guessing that this is exactly the same as the above
[83:13] key for key let's see yep can't tell any difference between the two
[83:22] all right so we can get rid of that one all right now let's go look at that shaw some shaw some shaw
[83:27] some okay good so there's our utils function for this type hex to uint8 array and then this should
[83:45] just be at callback hex to uint8 array and there we are
[83:59] i'm actually going to move these util utility type definitions down to the bottom
[84:12] all right sec p 256 k1 and i actually don't want this to be here
[84:26] i don't want this to be here base 58 check maybe i could do
[84:34] type type separate type files i just don't i just don't know what to do
[84:56] all right so
[84:59] do
[85:28] okay this one
[85:29] great does not exist that's fine
[85:34] that's what you think but you don't know
[85:57] hmm
[85:58] fine
[86:02] wait i already have ts ignore why is this complaining
[86:11] i guess my ts ignore is not in the right place sec p
[86:18] the only other place that we should need sec p is going to be to get public
[86:23] key so that's also going to be a utils dot get public key
[86:28] priv buff
[86:43] so
[86:45] all right let's go look at utils real quick
[87:09] and then this should be type get public key and that type should be at callback
[87:23] get public key with that param uint8 array priv key
[87:42] sure we can call it priv buff that's fine
[87:51] and then returns is going to be the same type we're going to return uint8 array
[87:56] public key u8 buffer
[88:02] all right then is compressed
[88:17] that needs to be there
[88:43] okay
[88:49] what was that about
[88:53] and the microphone's still working okay good mic is still on
[88:58] had some problems the other day with the mic turning off hey how's it going welcome
[89:10] all right base 50 check okay so some of those have gone away
[89:12] let me go ahead and put this back the way that i had it before
[89:18] all right that's fine
[89:22] and then this is going to need to be a utils thing this one we don't need anymore that one
[89:29] got included in the main so this there's no longer any need for this random bytes to be anything but
[89:39] crypto dot get random values because that's both node and web crypto node crypto is now web crypto
[89:48] all right so i'm going to take this uint8 array to hex and we're going to bring this up
[89:54] and we're going to put it on the utils
[89:57] all right utils dot
[90:08] uint8 array to hex
[90:09] all right
[90:19] i want another mountain dew
[90:23] thankfully i've got another snowy mountain dew right here
[90:36] let's pop another top my friends open extra focus
[90:40] not as good as sugar at all not even close not even a little bit
[90:55] i mean this is diet so it's extra disgusting
[91:01] do
[91:11] let me see which which of these two implementations i like more
[91:30] they might be exactly the same
[91:31] okay that those lines are the same i like this one more this is the one i'm going with
[91:58] and i can get rid of the works for little indian cpus
[92:01] because i'm i could be wrong but i'm pretty sure that the buffer is always in big int format
[92:11] regardless of the cpu unless you're using a data view
[92:21] all right and here yeah we can get rid of the buffer the node buffer we're not making any
[92:27] allowances for a node buffer
[92:31] okay so there's basex
[92:49] okay encode decode decode unsafe and so this is going to have at returns
[93:00] c type base x dot create encoder encoder encoder
[93:19] okay
[93:22] do
[93:28] and this is going to return
[93:43] base x
[93:49] and then we have to define well for right now i can just get rid of
[93:55] this part that should be good enough and then we're going to say
[94:00] uh type def
[94:07] base x oh it's just base x right okay and then property is going to be encode decode and decode
[94:19] unsafe abcde so they'll go in this order and this will be decode decode
[94:34] encode
[94:43] so decode
[94:58] wait why is it decode unsafe what's the point of the two of these
[95:07] do i actually use decode unsafe anywhere
[95:11] no then i don't need to declare it there
[95:15] and one of these is just simply i'm gonna have some sort of metatype for
[95:23] you know buffer to string and string to buffer because that's basically all these are
[95:27] so decode is going to take a string and returns
[95:37] so it's going to take a string which is of aa base x
[95:49] what do we call it decode and then it's going to return
[95:57] uint8 array and then encode is going to do the opposite
[96:02] it's going to
[96:07] take a uint8 array
[96:16] let's see call it source decode is also called source
[96:44] base x types just paste these in here
[96:48] so
[96:54] hello
[97:06] so
[97:17] oh whoops hold on let me let me take this back i did misspell it
[97:31] okay create encoder it says it has no type create encoder fine
[97:54] so
[98:03] all right cool no no namespace beck base x has no exporting base x base x dot types
[98:20] base x dot types base x dot types
[98:26] what do you mean it has no exported member it's right here
[98:33] i'm just so confused
[98:41] it's right here create encoder right there
[98:50] it's exported it's in the file
[98:55] i just don't get it what is it whining about the type is there
[99:13] yeah
[99:21] oh you know what hold on hold on i'm gonna feel so dumb about this
[99:34] nope star.js right there it's right there
[99:41] i don't know what to say
[99:42] we've got all the type definitions they're on the right place this thing's just whiny
[99:49] oh wait wait wait wait wait i have one more idea
[100:09.56] let's try this
[100:11.88] that's kind of weird that's not the way i'd like to do it but let's just try it out like this for
[100:29.88] now
[100:34.20] base x only refers to a type
[100:50.84] but is being used as a namespace here
[100:55.72] so
[101:02.04] i don't know what you want me to say
[101:16.36] so
[101:20.36] okay well that made it finally calm down
[101:43.56] let me see if i can
[101:49.88] okay let's see if this works better now
[102:03.88] okay let's see if this works better now
[102:10.20] i really hope that somebody from the typescript team watches this
[102:16.52] but maybe not somebody from the typescript team because they probably want you to not
[102:21.64] use javascript because that's what typescript is for is to not use javascript
[102:27.24] uh
[102:34.84] hold on there i there's something i was going to do that i totally forgot about
[102:45.40] i was going to apply a lot
[102:46.84] we're gonna go
[102:50.68] teal's low orange is high
[102:56.36] what no
[103:01.48] that that was a little too much hold on hold on
[103:07.96] there we go
[103:13.56] then i was going to apply something else some color correction here
[103:18.36] before i apply the lot give me a second
[103:23.16] all right we're going to do some color correction so we're going to take gamma up to eight we're
[103:28.20] going to take contrast down we're going to take saturation down and then we're going to apply the
[103:35.32] light oh i'm going to take saturation up a little bit there we go do i look more pro now
[103:41.80] this is this is let me know what you think on that i discovered i discovered this the other
[103:51.24] day because somebody else had their camera set up so nice and it just looked so movie
[103:55.80] like because their contrast was low and their saturation was low and i thought oh that looks
[104:00.76] kind of neat i want to try that out the contrast might be a little too low on this let's let's
[104:07.32] take it back up a notch let me know what you think about that you probably don't think anything about
[104:12.28] it that's probably a little too much for a little aj here all right so
[104:19.00] property create encoder does not exist
[104:27.00] what
[104:37.32] okay
[104:45.16] i'm just so confused basic stop property create encoder well duh
[104:59.48] so
[105:07.00] okay base 58 here we go that's important where did that one go base 58
[105:17.88] ah yes we need this to i will allow this to be a const
[105:27.72] i will allow it
[105:28.52] it is a string probably better not though it's just confusing
[105:36.52] all right now we've got our base 58
[105:52.52] um
[105:59.40] oh prop decode prop
[106:02.92] encode surprised i didn't throw an error earlier
[106:14.12] so
[106:41.24] okay let's try this one
[106:47.08] so that returns base x let's go back to our create encoder here
[107:05.00] and yeah
[107:08.44] sure i don't think there's any need for that we'll get rid of it okay cool coming right along
[107:26.60] base 58 check types
[107:30.44] okay let's try this one
[107:45.24] so
[107:52.28] oh i see what's going on here
[108:13.32] let's try this
[108:14.44] i'm going to try base x base x and then let's try this to be base x
[108:24.84] and then we could try this one to be
[108:29.24] base 58 check
[108:33.24] so
[108:43.16] there's no exported member base 58 check what do you mean
[109:01.96] oh sure all right i i actually believe that now
[109:04.28] okay so this actually truly truly doesn't have a thing called
[109:11.56] um base 58 check type def base 58 check
[109:22.92] it's going to have properties like encode and decode and stuff
[109:29.24] i think the most important one it's actually going to have hold on it's going to be
[109:33.64] so that it's going to have a prop and it's
[109:39.08] going to be called or it's going to be of type create it's going to be called create
[109:42.20] and then it's going to return
[109:48.12] base 58 check let's see here okay so it's got to create
[109:58.84] ah but the create takes an ops
[110:00.76] the ops just has a dictionary is that it
[110:08.52] okay here we go this is important
[110:25.40] all right because we have to type def the options object because we have to
[110:36.92] type def base 58 check
[110:45.32] and we're gonna do this one has to be at prop whoops
[110:52.92] and well i guess we need to turn all these params into props is the thing so we're going to have
[111:01.32] param it's going to be base 58 check ops which is going to be optional ops and then all these
[111:09.88] params are going to become props so then we need to swappy do it from at param to at prop
[111:21.96] so
[111:35.08] so
[112:03.08] oh no that's not going to be the same line anymore
[112:14.20] how's it going everybody tell me what's up
[112:30.12] okay so we've got the dictionary we've got the private hash
[112:39.16] x pub and then we need to have
[112:44.44] okay x pub version
[112:57.80] so
[113:00.20] and then i don't remember what was the test net version i think it's called i think it's t pub
[113:10.44] so i think if we took
[113:14.20] if we found what prefix results in t pub that would be the right one
[113:25.40] so
[113:31.40] okay and these are the wrong order oh wait it does say something for test net here
[113:45.64] so
[113:54.36] oh wait which of those did i just do
[114:11.48] this is the pub version the priv version should actually come first so x prv
[114:21.96] and that should be this one
[114:31.72] or this one for test right
[114:38.68] so it should be x pub and t pub x priv and t priv
[114:55.80] so double check priv is de4 test is 2 1 e i mean pub is 2 1 e test is 3 9 4
[115:06.60] for private and 7 cf for public so let me just double check on just this in the main file here
[115:19.00] yep all right that looks good
[115:26.12] yep all right that looks good
[115:54.52] base 58 check options c blank and not blank but yeah see these things okay great
[116:22.28] and we
[116:27.64] okay we do need to define these things i don't think we have any type information for these
[116:32.92] let me double check in my latest version of this whoops get status get pull
[116:49.64] yeah we did not ever get very far in terms of typing any of this stuff in the middle okay
[116:57.64] so let's do that
[116:59.24] whoops we're going to add the types to
[117:06.04] base 58 stuff here by going into the base 58 check types and then just throwing this down
[117:19.96] and then we'll get to the checksum
[117:24.04] i'm just gonna
[117:27.32] make these small
[117:32.04] and this one this one can just literally it can just be functioned
[117:46.36] a lot of these ones can be
[117:47.48] oh we have to define what the parts are
[117:54.92] okay let's first define what parts are i think it's this
[118:12.60] so let's say well these two go together that's kind of a big one but whatever at type def
[118:41.16] let's see
[118:43.80] base 58 check parts
[118:47.80] ah what happened there
[119:01.88] all right string is the version i think i think versions of string yeah versions is
[119:10.28] everything's a string
[119:19.80] and we might have a distinction between private parts and public parts
[119:31.64] and we might be able to say for example that
[119:39.48] you know the private parts or public parts is the parts
[119:57.00] let's see here
[120:01.72] boolean i think it's literally just going to be true compressed
[120:16.44] it's not it's not even a boolean we only
[120:21.48] support compressed keys we have no reason to support anything else at this time
[120:31.24] let's see the four checksum bytes
[120:35.00] version the two to four i'll let the one to four
[120:50.36] magic bytes
[120:56.04] hex private key x public key compressed
[121:08.20] public key with only the
[121:15.80] x value and then i forget they don't call it quadrant there's a name for it
[121:21.64] there's a name for that that byte but i don't remember what it is
[121:45.48] okay so we got the version we got the key we got compressed we got check that's it
[121:49.80] all right checksum is pretty simple
[122:00.92] so
[122:10.44] hmm
[122:24.60] so
[122:32.92] first of all let's figure out the public parts here
[122:47.72] so
[122:55.40] all right so at callback
[123:14.84] it's going to be checksum
[123:18.12] and this is going to take in
[123:23.32] um parts
[123:35.32] and it's going to return
[123:42.60] string
[123:45.24] four bytes eight eight hex chars
[123:52.20] four bytes whoops four bytes of checksum
[123:59.56] public or private key parts
[124:11.24] so
[124:23.88] let's see there's probably something like encode or decode here
[124:38.52] and then i think we're gonna also have a verify if i'm not mistaken
[124:49.00] so
[124:57.16] okay
[125:11.40] so
[125:19.80] what do you mean cannot find the name that's what oh okay whoops
[125:30.84] just i'm defining the name that's what we're doing here that's the work to be done
[125:39.80] so
[125:41.88] well there we go checksum
[125:55.88] so
[126:22.68] okay so
[126:27.88] checksum raw hex set version i don't really care about these things
[126:45.72] they're private they're not going to be exposed so doesn't matter verify
[126:51.80] okay so at callback verify this one is important it's gonna take a string base 58 check
[127:10.12] oh yeah that doesn't matter and then it is going to returns
[127:16.76] i'm just going to return parts and this is at throws error
[127:32.04] so it's going to return or it's going to throw
[127:36.76] and we got verify hex it's going to be pretty similar
[127:45.48] so
[128:08.52] oh i'm a little confused here
[128:25.32] ah
[128:27.80] hmm if i was going to refactor this i'd probably use more un8 array
[128:42.60] and less hex but i'm not going to
[128:52.68] uh the
[128:57.64] version data and checksum
[129:14.60] so
[129:23.08] and we're probably going to have a decode and decode hex which is fine
[129:30.28] the decode is going to take in oh it's going to be the same except that it doesn't throw
[129:44.28] it just returns false or something
[129:45.88] right
[129:48.28] with or adder
[129:55.48] same thing here with or adder
[130:02.28] and then decode hex
[130:07.96] same thing except it doesn't throw an error
[130:13.00] um
[130:25.96] actually this is a little bit stronger than that because it's with adder x priv or x pub
[130:40.92] so
[130:47.16] all right so
[131:01.16] decode hex we already talked about that right oh wait and this takes options
[131:09.88] um
[131:16.28] so we're gonna have to figure out what those options are
[131:24.60] or not
[131:30.28] i don't i don't think i actually want to support the options here
[131:38.76] um
[131:43.40] yeah they're listed there but i don't think we actually use them good
[131:47.40] and then this can be it can return a private key it can return oh
[132:01.72] okay so it can also return x pub or x priv
[132:12.12] so we actually have a little bit more here
[132:24.04] so you have private or public or x private or x public
[132:51.24] okay x perv parts
[132:53.96] it's going to be x perv
[132:57.96] and this does not have compressed at all
[133:20.36] um
[133:28.92] and then these become x pub
[133:47.24] so these are four magic bytes and this is one magic byte
[133:52.04] okay so wait why is it giving me oh okay it's giving me crap because i still got a bunch of
[134:04.68] stuff that is not documented yet okay got it so decode hex man takes a while
[134:13.24] but we've got all of the possibilities there good and then encode
[134:20.28] is going to take various different types of parts
[134:31.96] it's basically just going to be the reverse
[134:36.84] of decode
[134:40.92] so let's say decode and make that encode boom boom boom there we are
[134:47.48] and then we're going to flippy doodle
[134:54.52] boom parts are param parts and then it returns base 58 check
[135:23.96] and let's see
[135:32.60] and i actually kind of want to say
[135:37.80] we know exactly what the output parts are
[135:46.60] uh we don't know the the input parts are a little bit more fuzzy
[135:54.36] in terms of
[135:55.32] let's call it encode parts
[136:02.76] so if you want to encode
[136:07.24] then you need to put in a check
[136:16.92] you might or might not need to put in a check
[136:22.60] you need a version
[136:24.44] not really you might have a private key you might have a public key
[136:32.44] you might have an x priv you might have an x pub
[136:45.88] so i guess encode parts are really just
[136:50.60] let's see uh what what was it it's not it's the opposite of require it's
[137:00.36] that's how do you make it loose optional is it optional
[137:09.08] uh whatever i'm just going to redefine it
[137:18.20] okay i actually should put these in the right order too so version goes down at the bottom
[137:28.44] and then what was the other thing compressed
[137:33.32] do
[137:41.32] i think they call it recovery bit
[137:50.84] all right so yeah let's go ahead and put these in the right order then
[137:57.32] so version just comes down here and compressed goes up
[138:02.92] and compressed goes up version goes down hickory dickory dock
[138:08.84] okay
[138:19.02] so when we decode or when we encode we can take in encode parts
[138:29.64] and then encode hex actually also takes in code parts
[138:45.64] well actually okay i want to make this a little bit
[138:56.84] so it needs to have here's the thing
[139:08.92] it needs to have one of these between these four
[139:23.24] so i think maybe i could say
[139:29.72] so we could do a type def
[139:40.20] private part
[139:45.08] which would be
[139:50.36] um
[139:58.36] private partial
[140:05.32] public partial
[140:12.36] um then we could have
[140:18.76] um
[140:21.24] x pub partial
[140:25.72] x priv partial
[140:36.20] wow
[140:40.12] and parts partial
[140:54.60] so
[140:57.00] so check compressed inversion
[141:21.08] these are all optional so then we could say
[141:23.96] parts partial is all of the things above
[141:38.20] so
[141:40.84] what the little mermaid is this?
[142:07.72] it is enigma of the broken soul from
[142:16.36] terra
[142:19.16] enigma but enigma spelled wrong
[142:26.36] so
[142:34.60] okay so let's see if now
[142:39.32] can we say that
[142:45.56] parts partial and parts optional partial
[142:54.36] so
[143:01.16] i don't know if that'll work
[143:05.08] to say hey it's got to have at least one of these keys it has to have one of these sets of keys
[143:16.12] so
[143:24.04] and then also it can optionally have any of these
[143:38.52] so
[143:44.92] all right
[143:48.92] so in code parts
[143:58.92] so
[144:05.80] it's going to return
[144:15.64] x bytes
[144:20.20] bytes
[144:22.68] wait hold on now encode
[144:38.68] encode hex
[144:48.60] so that probably should be called encode two hex
[144:51.24] and it returns a string
[144:59.64] so
[145:06.36] all right and then
[145:23.80] at prop function
[145:28.68] encode x key
[145:33.08] in code private key hex
[145:45.96] encode pub key hash hex oh and i have i used the term public key anywhere
[146:04.84] public key
[146:13.64] hmm i'm pretty sure that's supposed to be pub key hash not public key
[146:20.36] oh
[146:34.36] okay this is supposed to be address
[146:41.48] okay i'll fix that later
[146:43.00] but that's that's an important distinction that that is not a public key that is an address
[146:54.20] i i was i was less clear on that when i first embarked on this journey
[147:05.08] all right okay now it's later
[147:17.08] so
[147:46.36] let's change all of these
[147:47.56] because we are not taking a public key we are taking a public key hash
[147:54.52] so let me look for anywhere where i've said oblique
[148:10.12] so
[148:18.12] so
[148:37.64] so
[148:43.88] oh what's this
[148:58.28] i don't have any scheduled calls leave me alone
[149:03.08] so
[149:09.96] let me just make sure that do i have anybody saying that they were going to call me
[149:13.00] nope okay i don't have anything on my calendar nope all right good
[149:24.76] um
[149:30.84] all right which one is this address
[149:45.32] so
[149:51.72] it's my public key hash p of x value only
[150:10.20] so
[150:16.92] okay now this is actually a public key
[150:31.40] so
[150:37.80] okay with these ones i don't want any of that to actually
[150:58.36] show up
[151:10.04] so
[151:16.12] all right good now this documentation is correct and the good news is that i found
[151:36.68] an error oh that has to propagate through a lot of things
[151:42.12] but it's okay we're gonna be all right we're gonna survive
[151:48.76] everyone's gonna be okay everyone's gonna live mostly
[151:55.64] so
[152:04.60] i think
[152:24.12] okay this is actually not an address either
[152:26.20] so that's even wrong
[152:30.60] so
[152:39.08] so
[152:47.56] so
[153:15.16] okay that is an address
[153:16.44] that is an address that is an address
[153:24.36] that's an address that's an address that's an address okay those three things are addresses
[153:37.00] but what we are taking in
[153:43.00] is a pubkey hash hex right
[154:08.52] okay
[154:14.52] from the top address address address three places we decode a string address
[154:28.52] so
[154:36.52] all right pubkey hash version
[154:42.36] that's good pubkey hash pubkey hash so it's not quite the address because the address
[154:53.08] is base 58 encoded that's the distinction between the address and the pubkey hash
[154:58.52] as if it is base 58 encoded with the check
[155:20.04] let's just write a little c program see what is this 1960 you
[155:30.60] you want everyone to get viruses and all the things to crash
[155:48.68] and performance to suck except when written by experts
[155:58.28] how about a little zig or at least some rust
[156:17.08] so
[156:25.48] okay there we go
[156:30.28] just trying to piss off as many people as i can today that's that's my goal for the day
[156:43.08] just always be as controversial as possible never not be controversial
[156:47.00] oh no now you're now you're gonna troll me too
[156:55.08] why do people love vim you can use vim to vs code uh because vim is simple and fast
[157:05.00] and more importantly it's portable you can't use vs code on a server
[157:10.20] well you can but most people don't know how to set it up it's kind of complex vim is just
[157:15.88] dirt simple it's way easier to configure it's way easier to get the plugins for it
[157:21.16] i want you to compare this give me just a second here
[157:27.96] to to what you have to do in order to get vs code working on a new machine okay
[157:38.76] so when you're working on servers you log into a new server all the time
[157:42.04] here vim essential that was vim essentials hold on did i mistype that
[157:53.00] there okay yeah i've just got a sim link in place there you go vim essentials so this right here
[158:03.08] within a matter of just a few seconds you'll have all the sensible defaults that you would ever want
[158:09.64] from vim
[158:16.20] so when i set up a new machine it takes me basically no time
[158:30.20] [Music]
[158:33.56] oh okay
[158:37.32] hey cool this guy does the same thing i do
[158:51.32] [Music]
[158:55.24] [Music]
[159:04.20] [Music]
[159:10.68] virtual text cursor
[159:27.96] [Music]
[159:37.88] excellent speaking of them one of my vim plugins made a change that i did not like
[159:43.32] so i had to go back to version uh 3.2
[159:52.36] good i'm glad that you get it and i do accept sensei ship so remember
[160:00.12] wax on wax off wax on wax off
[160:08.20] okay so
[160:17.48] now we've got the base 58 check types are done the base
[160:21.32] x types i think are done i think all the type type type type types are done
[160:25.24] yeah it is a karate you know i have not seen the karate kid in ages
[160:36.44] i don't even remember really what that's the context of that scene but yes it wax on wax
[160:43.96] off is from the karate kid because basically what he's teaching him is this karate move
[160:49.88] so with karate i guess he's you know there's something about he's teaching him this repetitive
[161:00.84] motion that he has every single day he does this repetitive motion and then i think at some point
[161:05.56] in the movie he goes to fight against an opponent who uses some move that he's not familiar with
[161:12.60] but then reflexively he just is going to to bat the guy's arm or something and it's because the
[161:22.60] whole time that he was doing that he was waxing the the man's car it was actually he was actually
[161:30.68] being taught how to how to do the do okay let's see public key to pub key hash
[161:57.96] that's all looking good and i just had a couple of extra types down here
[162:03.32] all right so we're mostly looking good
[162:04.84] other than that this is saying
[162:11.00] there is no exported member base x let's see if that's true base x okay good
[162:20.92] so let's say wait no we wanted do we want it like this
[162:25.72] i don't know what happened here but this was supposed to be here
[162:36.28] there's supposed to be base x has prop of type create encoder create encoder i don't know
[162:50.12] what happened there
[162:59.88] create encoder does not exist on type base x
[163:15.56] but why not
[163:20.52] we've called this type base x
[163:37.32] so
[163:46.28] create encoder
[163:47.64] okay type of base x oh whoops that how did that happen
[163:58.60] okay so this is better now
[164:03.56] so decode string it doesn't like decode string
[164:15.24] decode unsafe decode string
[164:32.44] let's try this i think this is actually going to work better
[164:38.36] well actually we're not going to have a base x at all
[164:59.80] returned we're just going to do
[165:07.00] base x dot encode equals and this doesn't need to do any hashing or anything
[165:24.20] okay create encoder
[165:52.68] there we go
[165:53.16] and our encode function is going to come after our decode function only because alphabetics
[166:03.56] okay and then this should be type
[166:15.80] base x dot encode
[166:23.32] and this should be and this should this should be inferred but whatever
[166:32.36] decode i'll go up here and we'll say whoops
[166:42.92] base x
[166:51.24] all right
[166:57.88] return base x
[167:11.72] okay cool
[167:12.44] so that sets up our base x cool cool cool so this is now now it's coming together i don't know what
[167:21.08] all that hubbub was about at the beginning but i now it seems like things are starting
[167:26.44] to come together and we also need
[167:35.40] um
[167:39.56] we have our type def dash keys utils and this needs to have at prop something or other something
[167:50.12] or other something or other i think it's a get public key yeah i'm just gonna let me just do
[167:55.88] this utils dash keys there we go those are our lines that we need so i'm going to go up
[168:05.32] here give me just one second i'll get back to the comments
[168:09.08] all right so this is going to be get public key
[168:15.48] one thing that the gpt script that i'm working on is going to need is some way
[168:24.20] to deal with just bad syntax that when the syntax is bad it doesn't totally freak out basically
[168:33.80] they should try to look for the next best line that it can or something
[168:37.48] and then just continue from there so when it starts to encounter syntax errors say oh these
[168:43.56] are new lines because one thing that the language server has is that it knows what you just did
[168:49.72] so if line lines 1 through 16 are the same as they were and then you've got barf and then lines 31
[169:00.84] through whatever pick up from where line 17 was you know that barf was pasted and you could just
[169:06.52] ignore the barf and then rewrite everything else it's probably easier said than done
[169:30.04] all right sha256 sum
[169:32.28] sha256 sum yeah
[169:59.08] is this donkey kong i think this is donkey kong yeah this is oceanic aura
[170:04.60] courtesy of oc remix
[170:13.80] all right and then let me get this one in and then i'll check comments okay
[170:28.20] at some point i'm gonna have to take a potty break i've said that before
[170:34.84] and then i just went right here in the chair it's fine
[170:41.32] that's what it must have seemed like that's not actually true but
[170:52.28] so
[171:19.40] okay so that's looking a lot better so i'm going to go ahead
[171:22.52] and maybe stash this now that things are starting to work
[171:26.20] again okay let me check comments
[171:30.84] uh how many years have you been coding sensei because your writing style is not familiar to me
[171:45.32] you're writing a type to gs yes so this is called js doc and i have been doing js doc
[171:52.84] only for about maybe two years before that i don't know why i didn't invest in it there's
[171:59.24] a lot of things i've learned especially in the past two years or so where it's just so much
[172:04.92] better to take the little five minutes here and there to actually learn what you're doing
[172:12.12] rather than saying ah i'll get to that later so that's that's been a huge boost for me and
[172:21.00] the js doc stuff is really annoying it it's it is literally the strongest motivator for me writing my
[172:28.20] own programming language is that and i'm not actively working on that yet but i am i am
[172:36.60] actually trying to fire find someone that i can hire to help me with the first part with the
[172:41.48] language server protocol stuff and i i'm actively in that search right now but the the tooling
[172:50.92] around javascript is so incredibly bad and so we need better tooling and because you can't write
[172:56.52] all the tooling for everything all at once because javascript as a language is just huge
[173:00.68] i need a smaller language than javascript that i could have really really good tooling for
[173:08.68] and so that's one of the things i'm i'm working on but i've been writing code for over 15 years
[173:12.76] if you see my code you'll be hanging me out in public i probably would yep that's most
[173:21.72] likely what would happen there have been a number of deaths uh due to code style at my hands these
[173:30.20] hands yeah that's right so yes don't show me your code if you want to live
[173:41.96] all right
[173:48.86] all right what is this what is this crying about now
[173:55.24] what what
[174:07.24] oh hold on just a second message
[174:23.48] this has got to be the dumbest i mean i'm glad that it's giving me an error message
[174:32.12] to tell me to do it how it wants me to do it but this has got to be the dumbest
[174:36.44] type definition i've ever seen
[174:39.16] maybe i just do
[174:46.60] as a base x.d code
[174:48.60] yeah
[174:54.38] this is some of this stuff is just so redonkulous
[175:06.20] right so it's being used as a type but it's a namespace being used as a namespace but it's a type
[175:13.56] so
[175:21.56] this this is why i mean so douglas crockford who was one of the javascript's strongest advocates
[175:30.76] 10-15 years ago he in an article recently said basically javascript has been so abused
[175:40.28] that the only path forward is to abandon it
[175:47.24] i mean this this guy was he was the bomb.com
[175:53.88] oh i wonder what he's got on plural site
[176:02.84] retire it there we go
[176:09.80] all right so the reddit's probably a pretty authoritative source to find whatever the real one
[176:22.52] was interview last month oh
[176:27.48] the best thing we can do to javascript is to retire it 20 years ago i was one of the few
[176:39.72] advocates for javascript its cobbling together of nested functions and dynamic objects was
[176:45.48] brilliant i spent a decade trying to correct its flaws i had minor success with es5 but since then
[176:50.68] there's been strong interest in further bloating the language instead of making it better so
[176:54.76] javascript like other dinosaur languages has become a barrier to progress we should be focused
[176:59.72] on the next language which should look more like e than javascript now i don't know what e looks like
[177:04.44] but it's one of those esoteric languages that nobody uses i want to check it out now yeah
[177:13.96] 10 hours of good parts of javascript there's four hours
[177:18.92] cool he's actually updated this that's awesome
[177:23.96] oops and what was this
[177:29.56] yeah javascript is just a freaking mess man it's a mess
[177:42.12] but it could we just need better tooling and we need a smaller language we don't need
[177:46.84] everything that javascript is we just need a language that does what needs to be done
[177:51.00] okay anyway where was i out here i was trying to figure out what was going on with this
[178:00.76] so
[178:07.64] oh whoops
[178:21.64] all right
[178:26.68] so
[178:33.56] so
[178:44.44] so
[179:03.32] so
[179:14.20] so
[179:33.08] so
[179:43.96] all right i did say decode unsafe and i did put null here good
[179:58.76] so
[180:02.84] why are you giving me a hard time oh because i did the same thing twice there we go
[180:17.00] so
[180:23.72] hmm not sure if i like the way this is going
[180:42.84] why don't i use typescript because typescript sucks typescript is i think the biggest problem
[180:49.24] with javascript that in ecma script 20xdx those two things are the worst things that have ever
[180:57.56] happened to javascript because typescript takes a language that is far larger and far more obnoxious
[181:04.52] and tries to shim it on top of javascript c-sharp is not a great programming language it is a lot
[181:12.28] better than a lot of the languages that existed in earlier eras but as we get smarter and better
[181:19.32] at writing code look this is what should happen here's the problem we have with every release
[181:24.76] of a language so when you go from version 7 to version 8 version 8 to version 9 any type of
[181:30.92] language that you actually install here's what should happen there should be fewer keywords in
[181:36.04] the language and fewer patterns in the language and the standard library should be bigger that's
[181:41.40] what should happen if you're going if you're going to to advance a language you need to be
[181:49.40] figuring out what to take out of it because perfection comes not when there is nothing
[181:54.36] left to add but when there is nothing left to take away that is perfection that is the
[181:58.84] goal that we need to strive for is what features of the language have we been using that we can
[182:03.88] get rid of and with that needs to come better tooling so when that version of the language
[182:10.28] releases there should be a tool that can automatically refactor programs that use those
[182:16.20] bugs or misfeatures of the language to cleaner simpler code that's what should happen so the
[182:26.12] idea that you're going to try to take javascript and you're trying to make it work like c-sharp
[182:32.52] and add all of the feature set of c-sharp cobbled on top of you know twisty bendy ways trying to
[182:40.12] get it into javascript is is insane and the same thing with ecma script 20xdx es20xdx is this idea
[182:48.44] that we're going to try to take python and ruby and c-sharp and insert whoever's on the committee's
[182:54.84] favorite language here and and make javascript more like that language what we need to do is
[183:00.28] focus on the best parts of javascript the parts that are the necessary parts and that are actually
[183:05.48] easy to use and easy to understand that's what we need to be doing with javascript not creating
[183:10.68] more language features that are difficult to understand difficult to implement difficult
[183:17.08] to create tooling for break existing tooling we need to create fewer features because if we have
[183:22.52] fewer features you know it's not going to happen tooling that supports the the the greater feature
[183:30.60] set it's not going to break when you add things to the language you break the entire ecosystem
[183:36.60] of tooling and this is part of why tooling in javascript sucks because there's so many things
[183:42.76] being added all the time that it's impossible to have good tooling and if you don't have good
[183:47.88] tools then you can't be a good programmer because being a good programmer is tooling
[184:00.52] being a good programmer is about learning how to use your tooling well
[184:09.32] that's that's that's a huge huge huge huge huge part of it all right so let me go back here now
[184:15.80] this doesn't like the checksum probably because it's going to want me to type this
[184:21.64] oh i think i remember part of the problem i had with this thing here and why this is not going
[184:32.04] to work the way that i want it to work but it's okay this is not these things are not that important
[184:39.08] i think i'm just going to wait to do a big what when i get gpt script up and running
[184:45.40] i am i i'm well i also have to figure out how to export types from gpt script the name gpt script
[184:57.16] being that at first i thought i was going to create a language that was dumb enough for people
[185:00.60] to understand and use effectively and now i realize that i need to create a language that's dumb
[185:05.64] enough for ai to understand and use so the extension for gpt script is a dot j s and so
[185:15.40] that's kind of you could stylize it as ai j s
[185:35.40] all right so here i need the base 58 oh and i'm going to turn the music back on i turn the
[185:39.64] the music off to rant but we're going to switch over to chiptunes so we're now
[185:44.76] we're now going from the ambient tag to the chiptune tag
[186:03.48] so
[186:11.08] okay
[186:25.08] let's see here
[186:27.08] so
[186:32.92] base 58 check verify
[186:39.64] verify hex
[186:46.92] and again i don't think these ops are ever used
[186:55.56] oh they're used here
[186:58.84] let me double check that base 58 check
[187:04.84] verify hex and then what were these ops we don't have those in yet
[187:21.24] oh yeah so there uh we were so we were on the classical tag
[187:31.24] then we were on the ambient tag now we're on the chiptune tag
[187:46.76] so
[187:55.80] so somebody was complaining in a in a chat about not being able to post messages for for 30 seconds
[188:11.80] or something and i'm just i'm just being silly hopefully it's not you know seen as being rude
[188:18.76] because i'm just i'm just joking with him saying how how long am i considered a new user i said
[188:23.24] well at least 90 seconds for sure because he complained that that had been you know that he
[188:28.12] had a 30 second timeout or something like that and then he said well i joined yesterday and i said at
[188:32.92] least one day for sure we will find out empirically
[188:40.12] uh all right let's see
[188:45.48] fewer tool fewer tools better tools lots of tools is going more complex
[188:53.08] yeah we need fewer better tools and not lots of tools
[189:01.48] and fewer fewer better keywords in the language hey everybody how's it going
[189:05.88] let's see here
[189:11.48] why are you so a non-person did you do you have linkedin so cool aj86 is my handle so dash
[189:22.60] incubator dash incubator i'm streaming on the dash incubator channel because i'm doing dash
[189:28.20] incubator work and i don't want my main channel to be cluttered up with just dash incubator work
[189:33.00] because i do it several times a week and i want my main channel to be a little bit more beginner
[189:39.08] friendly content so you can you can also like sub follow if you want to here on dash incubator i do
[189:47.32] work here jojo byte is doing work here sometimes maybe i think and then also cool age 86 is my
[189:56.84] main channel where just everything everything anything that can happen will happen
[190:02.28] okay verify
[190:07.96] parts dot valid
[190:12.92] oh okay this is interesting so decode wait does this do decode hex decode hex
[190:25.48] hex does the checksum all right so verify can throw decode won't throw
[190:31.96] but then let me see here so if we have verify we had all of these different parts things
[190:41.40] i think i want to put back on the return
[190:46.60] i'm just going to be boolean
[190:55.80] um
[191:09.80] so
[191:32.60] all right
[191:40.76] uh
[191:55.72] so
[192:02.92] verify hex okay
[192:17.40] so
[192:23.08] let me try this one so do we have a verify hex hold on where'd i go wrong
[192:37.24] so
[192:43.24] oh wait those options are optional
[193:04.12] i think we're gonna say
[193:05.16] do type def
[193:08.52] verify ops
[193:12.28] and we're gonna have what is it
[193:30.36] boolean verify
[193:33.32] false to skip
[193:37.56] um set false to not throw when valid is false
[193:57.40] okay set to false to set valid false rather than throw
[194:14.84] so
[194:17.48] oh this is going to be prop of course not param that's why it's that's why it's griping at me
[194:39.96] okay why is why is this griping uh because return parts
[195:05.32] uh one two three four so there should be one two three four places where valid can be valid
[195:29.48] okay
[195:55.24] what do i do
[196:00.36] okay valid does not exist on
[196:15.24] so
[196:23.48] all right let me see what the return value is there
[196:28.36] because something is not right
[196:33.08] i'm saying it returns parts
[196:41.16] and parts is defined as any of these and every single one of those
[196:46.28] every single one of those has valid on it
[197:01.08] all right let's just double check to do something wrong we've got prop we've got boolean
[197:07.16] we've got valid we got checksum passed same here same here same here
[197:12.84] so i'm wondering i have an idea about what this why this is uh going this way
[197:20.20] so decode hex ah we just need to type these that's that's what's going wrong because it's
[197:29.16] saying hey it's doing this thing and we don't know why it's doing this thing
[197:36.52] all right so base 58 check
[197:38.44] decode and then this one's going to be decode hex
[197:47.64] and we're going to have to go up here and then do the same thing with base 58 check
[197:58.84] and switch out verify for decode and there we go we're golden
[198:04.28] all right and do we have a base 58 checksum
[198:17.72] i'll check comments again in just a second
[198:23.00] um
[198:28.44] of course
[198:31.64] all right
[198:42.44] compressed
[198:48.92] does not exist
[198:53.08] on x proof parts
[198:58.04] yes
[199:01.32] um
[199:14.76] so
[199:24.20] so
[199:35.64] okay let's see i'm gonna go ahead and just not worry about
[199:54.28] well i guess it's just as much effort let's see here to do this
[199:59.16] oh not type sorry that should be at param
[200:20.60] ram
[200:21.40] all right it's clear that that's returning a string
[200:34.12] uh
[200:43.40] i'll go back to comments in just a second or a minute
[200:49.96] or three minutes i'll get there
[200:54.52] decode to encode boom and then oops
[201:15.80] we'll do encode parts encode parts
[201:20.44] i don't know how this is griping let me go check this out again
[201:35.24] so
[201:44.68] let's see
[202:02.36] uh i i forgot what i came into this file for compressed okay
[202:06.04] so encode parts
[202:11.48] is parts partial and compressed
[202:16.68] private parts can be compressed pubkey hash can be compressed
[202:28.36] x proof parts can't really be compressed all right so what is it griping at me about
[202:53.64] yeah i don't think that x proof parts can have has a compressed option i need to go check that
[202:59.96] out extended extended extended x x
[203:15.96] version raw adder
[203:24.60] let me take a look at this for a second okay let me get that so my name is aj yes my name is aj
[203:31.08] i'm going i'm going to bed uh turkey 1 a.m okay have a good coding i will thank you very much
[203:42.92] when you write do you realize wait hold on
[203:46.60] and i wonder when i write did you realize
[203:53.64] to new message or should you head to next to left or right and see it
[203:58.20] so i think what you're at so i see your message right here so i when i'm coding if i could
[204:09.80] if i could um show you i well i'm not gonna do it right now but so
[204:15.80] the camera is at about a 45 degree angle for me and so when i'm coding i'm looking here at the
[204:25.80] screen but the camera is here so there's the camera here's where i code and then i have a
[204:32.04] monitor that's here so this shows me what i actually look like so my face is not actually
[204:38.92] this beautiful i have an ai filter on that makes me look manly has my hair longer you know i'll
[204:45.32] turn it off on monday and then you'll see what i really look like but um dang it i said um but
[204:55.88] yeah so i i'm monitoring on one screen i'm coding on one screen
[205:03.16] and the chat is on the screen that i'm coding on so i do see a little blip blip
[205:08.68] to know that that a chat came in plus so out of both corners of my eye because i'll see a little
[205:15.80] bit of something right here that is right here and then i'll see a little bit of something right
[205:22.28] there so for example i just saw it move yeah okay oh i need to get the ai to fix the stray hairs
[205:34.68] it's gonna it's gonna do that better on monday
[205:40.84] all right so i don't think that there's anything to do
[205:45.48] okay version pubkey hash version x prev version compressed
[206:02.20] okay fine fine it's not assignable to true
[206:15.64] so
[206:27.64] so
[206:36.52] so
[206:47.96] all right
[207:02.60] so
[207:11.40] so
[207:21.32] so
[207:31.24] so
[207:49.16] let's see for a private key
[207:58.76] used for pubkey hashes
[208:08.68] okay and encode private key
[208:22.68] so
[208:32.60] so
[208:42.52] so
[208:52.44] so
[209:08.36] let's see
[209:23.00] so
[209:32.28] for a compressed private key
[209:47.88] for private keys used with compressed public keys actually this is kind of wrong
[209:57.48] for a private key it should be 33
[210:14.20] with compressed bit or 32
[210:17.88] bytes
[210:23.80] it should be 30 32 bytes or 33 with compressed bit with compressed byte
[210:38.20] so
[210:41.40] or 64 x characters
[210:55.40] or 33 bytes
[211:05.24] okay so i'm gonna go ahead and do that and then i'm gonna do this
[211:09.64] marker byte there we go
[211:23.48] so
[211:26.28] okay uh let me check over here you're focusing focusing that's perfect skill in some random
[211:44.28] notification my focus is gone i learned this skill from you sensei yes indeed but i need to go to bed
[211:49.96] right now it's not bad you don't need to go to bad you need to go to bed b-e-d bed if you need
[211:57.24] to go be bad right now by all means go be bad but have a good time with whoever you're being bad with
[212:02.84] let's see
[212:08.68] and remember like sub follow if you want to let me put up the little like in my bob again
[212:15.88] [Music]
[212:19.96] but i'm only trying to tell you how to live your life if we're talking code
[212:22.92] elsewise do as you please when it comes to like sub following do as you please
[212:29.40] all right have a good one bye
[212:38.44] [Music]
[212:48.68] all right what else is access to your parts
[212:55.08] [Music]
[213:06.68] so
[213:08.68] [Music]
[213:23.00] so
[213:28.28] all right
[213:42.28] [Music]
[213:55.88] hmm
[214:09.88] [Music]
[214:25.96] thinking about this from a language design perspective how do we identify
[214:29.64] because i want to reduce the amount of boilerplate
[214:35.64] that is in here and i'm wondering how to do that because you have functions like this where
[214:41.24] they basically only take a subset of the enum that the enum type that they could take
[214:51.56] and that should be detectable and so it should only be an error if it uses things that are
[214:58.92] mutually exclusive so if it uses things from this enum type and that enum type then it should be an
[215:04.68] error but if it doesn't actually use things from the enum type then
[215:09.40] yeah i'm not i'm not sure how this sort of thing should be checked
[215:15.72] okay let's go back up to the top and come back down here
[215:30.84] [Music]
[215:38.12] okay pubkey hash
[215:41.72] the checksum doesn't actually need to know
[215:58.28] yeah this is weird because it should know here i'm checking if it's one of these
[216:03.48] what is the what is the point of having the type enum if it can't understand what it is
[216:13.16] i don't know i guess when i write my own utility for it they don't know all right utils dot
[216:23.48] [Music]
[216:35.80] there we go
[216:36.52] okay whoops
[216:49.00] [Music]
[216:54.92] oh what's this this sounds kind of cool
[216:56.52] cold boot
[216:59.96] kind of got a nice sonic feel to it
[217:08.52] [Music]
[217:22.44] [Music]
[217:34.68] dang what is the point of this what is
[217:45.80] now let's go back here
[217:59.80] [Music]
[218:07.16] all right so we got some ops
[218:08.36] verify verify hex
[218:25.16] okay decode hex what is does decode hex take anything decode hex
[218:30.68] all right let's check and see
[218:42.36] it's not using the options let's remove them doesn't look like it's reusing them let's remove them
[219:00.28] [Music]
[219:06.20] [Music]
[219:18.92] oh wait
[219:19.56] there we go
[219:26.20] [Music]
[219:42.92] this is just this is just so useless why
[219:51.08] [Music]
[219:58.52] this is just frustrating if i have to comment out every single use of the type
[220:02.60] what was the point of defining the type
[220:19.32] version and key hex okay so this one is pretty easy that's just going to be
[220:24.52] string
[220:26.84] version and key hex there we go
[220:45.64] i'm not getting any of the benefits of the typing and when i'm doing this it's just so frustrating
[220:51.24] okay so i think that's one down and maybe still kind of want to go
[221:03.72] [Music]
[221:15.64] ah update
[221:29.96] [Music]
[221:39.40] [Music]
[221:55.88] okay this is a good way to go about this that's a good way to go about this
[221:58.84] i don't know if there's any options
[222:03.56] oh it's not that we need options for this is that this includes a lot of state
[222:18.28] oh we can mark things up private oh
[222:21.56] i did not realize that and that makes them not get checked
[222:37.08] let me try that out
[222:51.72] [Music]
[223:04.36] [Music]
[223:06.36] [Music]
[223:30.92] all right
[223:41.40] oh oh no no that was just my own message going away okay i thought somebody said hello
[223:58.20] [Music]
[224:10.68] [Music]
[224:12.68] [Music]
[224:33.32] all right so we're going to do dot create
[224:35.72] update and of course
[224:43.16] update digest
[225:02.20] [Music]
[225:14.60] [Music]
[225:28.60] [Music]
[225:52.60] so hacky i mean seriously i i mean i wouldn't be surprised but i don't think
[226:00.28] anybody and microsoft codes in javascript i just don't i just don't think they do
[226:16.20] [Music]
[226:26.20] [Music]
[226:36.20] [Music]
[226:50.20] having all this hoopla to jump through i just can't see it
[227:04.20] [Music]
[227:14.20] [Music]
[227:24.20] [Music]
[227:40.20] [Music]
[227:48.20] okay
[228:00.20] type of a function declaration must must match the function signature
[228:14.20] [Music]
[228:24.20] what did i do differently between this one and what was the other one base 58 check let's just try
[228:31.24] let's just try and see what's different okay module dot exports
[228:40.76] okay base 58 check has a create and then we have callback create
[228:47.00] okay
[228:49.74] that callback create all right let's just take a look here
[228:57.80] make sure so we've got the dot create right there this is the same thing
[229:26.36] all right is it griping about this
[229:27.72] property create
[229:35.88] it's the only thing that it has that's it
[229:51.00] [Music]
[230:03.48] property create does not exist on type of import whatever whatever types
[230:19.88] ah because i have to explicitly define the type that it's yeah whatever
[230:30.60] all right so digest
[230:44.92] [Music]
[230:54.92] all right we don't need that
[231:06.92] this is an encoding free zone my friends an encoding free zone
[231:14.36] [Music]
[231:22.36] [Music]
[231:34.36] [Music]
[231:41.56] okay we're about four hours in now and uh it will be time for a potty break soon
[231:48.60] i think i think i'm just going to leave it going and just put up potty break here on the screen
[231:54.68] we'll see
[232:11.16] okay
[232:11.66] so we've added types to a few things that didn't have types before
[232:16.84] we're exporting some stuff on dash keys
[232:23.16] [Music]
[232:42.52] man this is frustrating this is just so frustrating
[232:44.76] i have to think about what what is the right way to handle a situation
[232:51.64] [Music]
[232:53.64] like
[232:55.64] [Music]
[233:10.92] let me think
[233:17.64] [Music]
[233:35.64] all right i don't i don't think that there's any reason that this would not run
[233:40.44] oh yeah that's okay never mind
[234:09.56] i can't get rid of this now hey i got rid of that one oh but i can't get rid of that one
[234:18.36] [Music]
[234:28.36] [Music]
[234:40.36] [Music]
[234:42.36] [Music]
[234:49.24] wait do we have a to public key
[234:51.00] get public key where's that at
[234:58.20] let me do we not have a generate ah right here okay so this one's going to move
[235:06.20] [Music]
[235:16.20] should it be get public key or to public key i think it should be to public key
[235:34.44] that means that alphabetically this should now go down
[235:37.08] q r s t
[235:40.04] and then what is this one
[235:43.48] this should be more clear
[236:00.68] so generate
[236:04.52] not sure what to do about this yet
[236:19.48] so
[236:22.36] because i don't really want to expose it anymore
[236:36.36] [Music]
[236:50.20] [Music]
[237:02.20] [Music]
[237:07.48] i'm just gonna
[237:08.04] i'm gonna do like this for now
[237:14.04] [Music]
[237:37.88] okay so now we've got those all together and they're all
[237:41.88] [Music]
[237:43.96] properly typed
[237:45.00] and then i need to update the documentation so i think i'm going to take a break
[237:52.12] before i get to the documentation and i think let's see here
[238:03.40] so this would be add types for base x base 58 check and ripe md 160
[238:32.92] ref um does this break anything i don't think it actually breaks anything
[238:38.76] include base x base 58 check and ripe md 160
[238:57.40] and actually one of the questions i have about that is the whole idea of base 58
[239:04.20] so base x i think what i said here
[239:09.88] the base x has a create function create encoder
[239:15.24] i think i just want to simplify that down to create so that it's
[239:21.08] more like what everything else is i think create encoder is a little bit
[239:29.88] super fluous
[239:44.60] [Music]
[239:54.60] two to two hundred and
[239:57.32] 55 characters
[240:00.84] [Music]
[240:25.72] [Music]
[240:53.48] all right
[241:02.36] create encoder and just create so
[241:17.24] [Music]
[241:29.24] what's that sound
[241:46.12] oh that's just part of the music okay
[241:47.80] let's bring a little more light in i think we got some clouds overhead or something
[242:00.60] there we go
[242:12.12] [Music]
[242:21.80] okay did i actually get somewhere
[242:39.24] [Music]
[242:48.20] so we're including base x
[242:51.00] include base 58 check and i was wrong about base x there's one other case it's used for
[242:58.36] it's also used for base 62 i believe
[243:01.00] actually no i'm wrong about that site is it used for base 62 or is it not
[243:09.80] i can't remember
[243:10.68] basics actually maybe it is i don't remember i think it is used for base 62
[243:32.68] 60
[243:34.68] update type
[243:38.68] [Music]
[243:40.68] so update docs
[243:42.68] [Music]
[243:44.44] move cli to cli all right this is what we're looking at
[243:47.96] [Music]
[243:51.48] okay so i'm gonna go take a five minute break
[243:54.36] [Music]
[243:56.28] about
[243:56.68] [Music]
[244:00.28] let me see if i can find my
[244:01.80] [Music]
[244:09.08] taking a bio break be right back
[244:11.00] [Music]
[244:19.32] okay
[244:19.64] [Music]
[244:26.20] um
[244:26.68] [Music]
[244:29.88] oh visually that looks better centered a little that way not that it much matters
[244:33.72] and then let's put a timer on here let's see if i can bring up so there's our our break
[244:39.96] and then where's our timers timers are up here
[244:46.12] [Music]
[244:53.96] there we go well i'll put it i'm gonna put a five minute timer i don't think it's really
[244:58.84] going to be five minutes whoops that's not what i wanted but be right back y'all
[245:09.08] um
[245:27.32] so
[245:37.56] so
[245:47.80] so
[245:58.04] so
[246:08.28] so
[246:18.52] so
[246:40.76] so
[247:03.00] so
[247:27.24] so
[247:51.48] so
[248:15.72] so
[248:39.96] so
[249:04.20] so
[249:28.44] so
[249:52.68] so
[250:16.92] so
[250:41.16] so
[251:05.40] so
[251:29.64] so
[251:53.88] so
[252:18.12] so
[252:30.36] and we're almost back the timer ran out the timer ran out i can't believe it i was slow
[252:38.52] but i had to clean up a little bit of a spill because you see i got this cup that has a lid
[252:46.92] and it's one of those uh you know it's it's got a a gasket seal on it so you'd think
[252:54.12] okay because it's got a lid with a seal and a top that flips back and forth you must be able
[253:01.64] to close this right it's probably to protect against spills right now it's just decorative
[253:08.28] 100 decorative
[253:16.44] uh where's my brbs there we go okay
[253:20.52] anyway so yeah i got a cup that doesn't actually protect against spills and we're back
[253:35.48] okay also
[253:38.20] i got some sort of you know chocolate shake thing that's probably really unhealthy but
[253:48.20] pretends to be healthy for some reason it probably ought not to
[253:51.88] it's a balanced energy drink with vitamins and minerals and protein
[254:05.16] hmm sure does taste good
[254:07.08] all right let's see here
[254:12.60] hmm
[254:26.60] so
[254:34.04] oh
[254:56.04] hold on i need to respond to something actually i don't need to respond something
[254:59.24] but i'm going to respond to it anyway
[255:03.48] uh
[255:10.92] so
[255:20.36] hmm
[255:34.36] hmm
[255:59.72] okay so i one of one of the guys said something about well i'd made my comment about bash and he
[256:07.88] says no no i said no no no why would you suggest bash and he said disagree on this and i responded
[256:14.20] look if you got 50 years invested in bash by all means keep using it as your interactive shell but
[256:19.24] don't script in it and don't lead others down the path of sticks and boulders when they could be
[256:23.64] taking easy street referring to fish for interactive shell and posix for um scripting language
[256:32.84] hmm okay fake lemonade love it all right let's uh move on so what do we got left here i think
[256:45.80] we just need to we got to move the cli we're going to update docs move cli and then we'll call it
[256:53.64] good um have you well see docker isn't serious it's for ninnies but it's super common these days
[257:13.64] kind of the de facto
[257:23.56] so
[257:33.48] hmm
[257:51.72] all right anyway get back to work
[257:53.64] cool so i'm actually going to take all of this stuff that's in the
[258:00.20] i think i'm i think i'm going to do both i think i'm going to
[258:06.68] we're going to have uh we're gonna get rid of generate
[258:09.72] uh maybe or if we do keep generate it's going to be generate whiff
[258:17.40] i'm just i'm not sure how to go on that one um
[258:20.68] but as far as
[258:28.20] the keys we use in the documentation my my big gripe was just say okay well let's
[258:34.68] mnemonic to
[258:37.56] adders.js is that what i'm doing here
[258:45.64] let's just use the first test key
[258:47.48] and then i'm gonna make a note in the documentation about this
[258:58.04] just put something down here at the bottom let's see license
[259:05.32] so
[259:15.88] so
[259:22.12] so
[259:32.52] um
[259:46.52] hold on the default linux distro
[259:57.08] for docker is alpine which doesn't have bash
[260:06.92] so
[260:17.32] um
[260:31.80] sorry
[260:37.72] ah crap ah yes there's all of this
[260:51.72] so
[260:58.12] these are all complete
[261:12.84] so
[261:18.52] they do not need updates
[261:32.52] these have all been complete for several years
[261:40.28] they do not need
[261:41.24] updates okay so
[261:50.52] example keys
[261:55.56] the keys used in this example come from the canonical
[262:08.68] zoomonic
[262:15.48] let's see
[262:21.24] mnemonic
[262:23.96] passphrase
[262:27.32] mnemonic
[262:32.04] zoo zoo zoo your boat gently down the stream so that's three six nine twelve wrong
[262:44.52] secrets salts
[262:50.44] password
[262:53.80] trezor
[263:00.76] hd path
[263:06.44] let's see if we do 80
[263:10.76] okay good so we got plenty of width left there
[263:20.44] so
[263:28.12] with adder
[263:42.68] so
[263:49.80] okay so now
[264:03.80] so
[264:11.48] i'll do the lifts
[264:25.48] and i think i will just double check that this all works
[264:30.84] and later i'll double check later it's uh it's literally the base of
[264:40.12] almost every docker container whatever
[264:56.20] well if docker is just a better documented way of writing
[265:05.56] posix scripts a better documented more complicated way of writing posix scripts
[265:17.88] if people would just avoid shared libs oops sorry i'm gonna get on
[265:40.44] so
[265:49.00] all right i got docker we gotta anyway if you want let me know if you want me to go on the
[265:55.80] docker tirade you just let me know we can do it with pleasure okay that looks a little awkward
[266:03.72] what if we do like this does that look any better no it doesn't so i'll just leave it like that
[266:10.04] okay cool so here we are
[266:18.60] uh
[266:32.60] so
[266:43.16] let's see here oh and i did i did this do from the right oh no whoops whoopsie doozies
[267:02.36] hold on i did that from secret what was secret
[267:05.96] no that was super secret one two three no we need the
[267:10.60] the trezor it okay my bad my bad hold the phone everybody go back everybody go back
[267:31.16] so
[267:41.96] okay now this is actually the right thing
[267:47.96] okay so
[267:51.56] hold on a second get diff read me
[267:59.00] license okay
[268:03.56] okay so get reset read me it oh whoops
[268:27.64] oh whoops no dang it argh
[268:32.36] no that's good that's good
[268:54.44] 22 2023
[268:59.00] see license and license great so license read me git commit sure update license
[269:13.24] so
[269:21.56] okay and now we're going to update the example keys and try to get this as far as we can
[269:35.56] yeah debbie and distros are still fine for containers
[269:42.20] oh yeah because because i'm 128 gb ssds
[269:50.28] on modern workstations can even hold three or four
[270:11.96] ah
[270:17.96] agree
[270:31.96] so
[270:42.92] so
[270:51.96] okay um sorry i'm getting sucked into a conversation with one of the one of the other
[271:08.44] dash guys mostly just joking around i think we're i think we're all joking around i think we all know
[271:21.32] that it's very hard it's very hard to know online when you're joking with people or when you're in a
[271:26.60] serious you know battle you know you say something like you say something like are you sure you know
[271:32.92] what recursion is and then all of a sudden it's boom which i mean that was a serious question but
[271:39.64] um yeah oh that one went sideways
[271:45.80] i lost a friend it's okay it was a friend i didn't need i don't need fragile people in
[271:54.20] my life i don't need people that feel the need to resort to emotional manipulation
[272:00.28] in order to get what they want in my life i don't need those people i really don't i don't think
[272:05.00] anybody does i i don't want to have a reverse cancel culture uh i don't want to cancel the
[272:13.08] cancelers but when people are you know are well you need to agree with me because my feelings are
[272:18.12] hurting if you don't agree with me then i'm gonna block you and i'm gonna tell all my friends to
[272:23.80] block you they're not my friends if they don't block you you know let's just grow a pair am i
[272:33.96] right yes i am right i don't need to ask i know i know i'm right okay let's see if we can figure
[272:41.08] out this one can we get that to a private key yay we get to get rid of these i'm not going to take
[272:54.04] those out yet
[273:05.00] you can tell that i'm emotionally scarred by this you can tell because if i weren't it wouldn't be
[273:21.16] that big of a deal i'd just be like whatever screw you now you can tell you can tell i'm hurt too i
[273:26.92] got hurt feelings do you know about hurt feelings you gotta be careful you might hurt someone's
[273:33.64] feelings jerome do you know about hurt feelings have you ever had hurt feelings
[273:46.04] i've got hurt feelings i've got hurt feelings
[273:51.24] all right so we are going to add all these back in because they really ought to be there
[274:06.28] all right so our correct values
[274:15.08] oh that's what we gotta put here hold on
[274:22.20] see we go all the way up here
[274:40.20] so
[275:07.48] okay let's see here
[275:08.52] so if i were to do
[275:13.64] dash keys inspect i think is what this is then i should get out all of this mess right
[275:25.40] i probably ought to check against the existing one to make sure that it still works
[275:49.96] let's see
[276:17.32] uh
[276:40.52] okay um so what i want to do is i want to say bin dash keys inspect test out with
[276:54.36] ah
[277:09.08] so
[277:16.20] oh wait what
[277:30.20] oh that's weird
[277:32.92] how
[277:37.88] so typed off dash keys
[277:41.88] well that's weird
[277:51.88] weird
[278:03.72] hmm okay so we still do have a little bit of trouble here
[278:18.68] so
[278:21.56] public key to pubkey hash
[278:35.56] dubs what's up man
[278:46.04] what's up how you doing
[278:48.84] public key
[278:53.40] okay i'm gonna go fix the rest of these later let me let me go back to this readme first
[279:03.64] okay so i wanted to inspect
[279:09.48] see examples m44-5-000.wif should it be this way or this way
[279:25.88] i think it should be one of these two i think this is how we should
[279:37.80] do it do it one of these ways
[279:41.88] okay let's see that way
[279:51.00] m44-5-000.wif
[279:55.56] i kind of like the harder underscores i don't know should be something like this
[280:06.92] so
[280:08.92] all right bin dash keys dot js inspects the wifi waffle
[280:20.68] wrapping up work planning to refresh further javascript knowledge yeah that's what i'm doing
[280:27.40] i'll probably be here for a few more hours though but uh yeah yeah i'm wrapping up work
[280:31.56] and refreshing my javascript knowledge um let's see here
[280:37.00] oh whoops test
[280:41.48] .wif two examples
[280:46.04] right now i'm working on updating some documentation
[280:53.96] so
[281:23.16] let's see
[281:33.16] version cc priv key
[281:51.72] compressed
[282:17.80] ah yeah
[282:21.88] i wonder if i could get this to spit out a little bit more verbose information
[282:31.56] could i get it to spit out
[282:34.36] all of these things i think maybe i could
[282:43.56] okay i don't want to go that far yet well i have to i have to go that far if i'm going to
[282:48.68] finish this so that's okay all right bin dash keys inspect
[282:56.36] decode so we're gonna do a little bit more than just decoding
[283:09.56] all right so at this point actually ah yeah okay yes i'm going to do this one i'm going to do this
[283:14.36] one all right so with the wiff we're not going to generate um on the decode here wait decode no decode
[283:25.96] there we are okay
[283:34.60] read adder or path yada yada blah okay so what i actually want to do we've got decoded private key
[283:41.40] so i want to turn this both into a compressed and uncompressed key that's what i want to do
[283:58.60] so oh i still have mountain dew as well
[284:03.40] there now that one's gone
[284:12.28] yeah so the the part here i'm trying to do is over the course of the last few months
[284:20.04] i've i've done a lot of different things in terms of generating keys versus using keys that have
[284:26.60] already existed and and i kind of tried to define a set of keys that i was going to use but then i
[284:31.16] changed it between the different libraries and so now what i'm doing is defining a set of actual
[284:39.24] honest to goodness this is this is the key set that we care about and i'm going to be and i'm
[284:49.32] going to use that so i'm done with bringing everything together in this library i'm just
[284:52.84] on to the documentation part okay so decoded private key secp let's see
[285:01.24] i need to grab this
[285:17.40] and i need i do need to test against known good keys as well
[285:31.56] but i think i've already done that for the other library so i do i do need to test my changes
[285:42.92] against the the fixtures that i already had but i need to update all my fixtures
[285:47.96] so that they use they use the same things okay so let me just ignore that for a second sec p
[285:57.00] 256 k1 oh also dash keys base 58 check dot create okay b58 c
[286:09.88] and then there's a broader piece of documentation i'm going to update after all of this that's going
[286:24.44] to be the next project is going to be to go through and basically document every term in
[286:30.20] the ecosystem up to this point and i've got maybe half of that done somewhere between 25 and 75
[286:38.52] all right
[286:49.72] so
[286:51.56] so
[287:08.12] whoops
[287:19.64] okay so we've got this one here and i just need to have
[287:24.04] okay let's see here what do i need to do for this
[287:34.28] function to public key
[287:40.60] to
[287:47.96] on to public key uncompressed so let me grab from dash keys here sec p 256 k1
[288:01.24] and this is it so i could just use utils let's see i actually wanted to export these on here
[288:16.12] so i wanted to have dash keys dot utils equals utils that was one thing i wanted to do
[288:23.16] i need to finish updating the types on that
[288:26.68] basically here's our to public key
[288:45.48] all right priv buff
[288:46.92] priv buff there we go
[288:51.88] so where's that private key bit private key
[289:14.44] so
[289:16.12] so
[289:44.28] adder let's see adder or with
[289:50.68] okay let pubkey equals dash dot utils whoops dash keys dot utils dot to public key
[290:11.88] decoded dot private
[290:13.24] and pubkey uncompressed is dash utils to public key
[290:25.56] now we're just going to do to public key uncompressed
[290:31.32] and then we will have
[290:41.16] oops
[290:51.16] public key
[291:06.60] dash dot utils dot u8 un8 array to hex
[291:14.36] the pubkey
[291:20.04] public key uncompressed
[291:24.92] pubkey uncompressed
[291:29.56] oops dash keys dash keys
[291:58.04] so then i want to have decoded dot pk h pk sha 256
[292:13.72] it's going to be equal to dash dot utils c08 sha 256 sum of the pubkey
[292:27.16] uncompressed public key that's what we'll call it
[292:43.40] uh you pk h
[292:45.24] shaw some
[292:47.88] um
[292:51.88] public key uncompressed whoa whoa whoa what happened what happened whoa whoa
[292:59.64] let's take it back step back here there we go
[293:02.12] and i think this was call i was going to call this u
[293:11.08] u
[293:11.32] let's do this pub key
[293:16.60] sha pubkey sha
[293:20.76] all right and then
[293:25.80] we have
[293:29.24] let's pk h equals
[293:39.32] uh ripe md dot create ramp md 160
[293:49.40] dash keys oh whoops i keep on doing
[293:56.44] dash dot utils should be dash keys dot utils
[294:02.52] let's call it pk hasher
[294:06.52] i kind of want a one and done for this
[294:12.52] i'm going to introduce that because it's it's kind of it's not very ergonomic to use it that way
[294:22.52] i guess it's not ergonomic to use it that way
[294:28.92] it that way i guess it doesn't matter this isn't being exposed publicly anyway
[294:34.52] well i don't know it's just kind of annoying
[294:44.68] and it's not going to take much to fix so let's go in here in a ripe md 160
[294:49.24] and let's go to that create and let's just add a hash function
[294:59.00] and then we could say you know you're going to take some u8
[295:08.44] u8 array
[295:15.00] well i guess this would be ripe md 160 hash is what i'll make it
[295:27.00] and then we can make this you know at param
[295:30.36] u8
[295:34.36] or make it buff whatever
[295:39.24] bytes
[295:44.52] let hasher equals hasher dot update bytes
[295:56.92] return hasher dot digest
[296:19.48] uh at callback ripe md 160 hash i'm just gonna uh i'm just gonna move it over
[296:28.04] all right let's go ahead and put this in the types for this
[296:45.96] at prop hash hash
[296:49.96] turns you in a array
[297:05.48] can't find name hash it's right here oh wait i always get confused about that where to put the
[297:13.80] brackets where not to put the brackets should just be positional brackets shouldn't be a thing
[297:18.04] if you're doing at prop obviously the thing after the prop is the type duh there's no need for
[297:25.08] brackets unless i'm wrong all right i do plan on well i plan is a strong word i have it in my mind
[297:47.88] that i will backport some of these changes into those modules at some point
[297:52.44] and then link to the updated stuff
[298:11.64] yeah
[298:21.24] all right so we've got that
[298:35.24] so now i can do this instead
[298:39.40] so
[298:46.28] let pkh
[299:01.24] so
[299:03.88] oh dang it i'm realizing something else
[299:26.92] so i'm pretty sure let me double check on this the shawsome
[299:31.56] should take a buff and return a buff and indeed it does good
[299:38.52] so
[299:48.12] pk right md 160 u8
[300:02.60] right md 160 u8
[300:06.76] is going to public key ripe md 160
[300:14.20] so i'm gonna i'm i want to include in the documentation the bad values that you could
[300:23.64] get if you were implementing so that it kind of leads you to know where you went wrong that's one
[300:29.32] of the efforts that i wanted to undertake with all of this whole tool set was that if we wanted
[300:36.76] to make this in go or we want to make this in rust or we want to make this on the phone
[300:40.52] we want to make it in swift we want to make it in kotlin that we have a step-by-step breakdown of
[300:45.72] how we've got some fixtures and we got a step-by-step breakdown of how it went wrong
[300:56.52] okay
[301:06.12] so if you were to hash in the wrong order for example
[301:15.08] that's one of the ways something could go wrong
[301:21.64] so
[301:28.92] okay
[301:42.92] if we were to hash the public key here we go
[301:51.16] let's get that out
[301:59.32] pubkey ripe md
[302:13.40] so
[302:21.48] pubkey pubkey i'm compressed
[302:24.76] pubkey
[302:35.48] pkh would be if we do it right
[302:40.68] okay so
[302:45.64] so pk sha 256 is going to be this one
[302:56.20] wait no we already did that um dash keys dot utils dot un8 array to hex
[303:09.16] so
[303:12.20] on this one
[303:14.52] okay decoded dot up upk sha 256 equals
[303:28.60] you put there we go
[303:36.44] so and then decoded pk rmd 160
[303:47.00] is this one
[303:51.56] and then
[303:56.68] i'm gonna have to go back and fix those types because it gave me all these warnings that i
[304:04.20] don't really you know they're not helpful
[304:09.96] all righty
[304:17.72] so then here
[304:21.96] i'm gonna call this one pubkey hash and basically this this should be the same as the other one
[304:32.60] in terms of this should be the underscore pubkey hash should be the same as the non underscore
[304:45.88] um let's see here
[305:00.04] um x y pubkey maybe i could call it y pubkey
[305:11.64] that kind of makes sense
[305:20.84] all right so here
[305:28.04] and this one would be the same as none other
[305:29.96] all right let's try this now
[305:37.80] cannot read properties of undefined reading hash
[305:51.08] ripe md 160 dash keys
[305:56.84] okay let me make sure that this actually made it in because it may not have
[306:11.64] i did not
[306:36.52] there we go
[306:45.08] so
[306:48.04] let's see bring in json this one
[307:12.84] okay so
[307:14.60] there's all of our stuff
[307:23.96] somebody's gonna throw this into the readme
[307:34.76] public key compressed
[307:46.52] all right good so pubkey
[308:01.48] so
[308:10.28] and then let's say pubkey x plus y
[308:24.60] so
[308:34.04] so
[308:44.04] and i forget what the restoration bit is
[308:58.04] so
[309:06.04] reviver byte or whatever
[309:11.72] pubkey sha
[309:20.12] 256
[309:26.04] let's do this
[309:40.04] i i wish i could remember what the name of that thing is called
[309:48.44] i do need i do need to get the name of that where can i get that from
[309:53.56] what other code can i get that from i can probably get it from the sec p 256 k1
[310:09.32] 0 2
[310:16.92] let's see from hex
[310:37.80] now let's go check this from compressed hex
[310:41.64] is short right not on curve
[310:47.88] bytes length 32 wait it should be 33
[310:56.28] and it is short episode first byte odd point x y insert point validity
[311:21.80] um what else could i find that the name of that thing
[311:25.40] whoops wrong button
[311:41.40] so let's see what we can find here
[311:45.96] sec compressed public key 33 byte
[312:07.96] all right let me see if i can find the name of that thing here
[312:15.72] i think it's called reviver byte or restore byte or something like that
[312:31.32] ah ah i'll ask chat gpt it probably won't know
[312:36.52] all right log in again okay fine
[312:53.08] what's the name of the first byte of a compressed public key i mean it does a good job for some
[313:05.16] things ah compression byte no it's not it's not just the compression but it's telling me
[313:17.40] it's known as the compression byte um let's try again compression flag
[313:26.44] try once more
[313:32.92] all right
[313:43.40] um
[313:51.40] oh gosh what code was i looking at recently
[314:10.84] what's the name of the byte that's used as a flag to restore a sec p256 k1
[314:23.48] public key
[314:27.40] let's see if it just calls it a restoration value it's got
[314:35.72] that's compression flag okay i don't know i don't know if that's right i've seen
[314:40.68] something else i've seen it called something else and that's what i'm looking for
[314:45.72] but we'll call it compression flag
[314:57.24] so
[315:02.84] pubkey
[315:20.92] all right then we've got the shot 256 we've got rmd 160
[315:28.20] i do want that
[315:32.52] and we've got
[315:36.60] pubkey hash
[315:43.48] which this should actually be in here twice
[315:48.28] let's make sure that we see that ae in here twice oh that's wrong that's okay i'll go fix that
[316:00.68] um why pub
[316:08.12] interesting
[316:14.20] ah there it is upub that's what that needs to be let's make sure that's upub
[316:19.96] and then this one should be upub too i think
[316:23.96] i should probably separate the pubs and the upubs
[316:35.00] just so that i don't mix and match them so much
[316:39.56] all right let me move this back up here
[317:04.12] all right pubkey
[317:15.24] all right
[317:29.24] all right
[317:57.32] public key and then pubkey hash
[317:59.16] let's see here so this i should probably just use i think i've got in here something that's
[318:14.84] to pubkey hash public key to pubkey hash there we go
[318:40.92] so
[318:49.08] a buff
[319:08.84] all right so there we've got pub
[319:23.88] excellent all right now we'll check this out i think i might call this y the y pubkey
[319:42.60] there that's a pretty decent name probably
[319:54.92] all right xy pubkey xy pubkey
[320:09.72] so
[320:19.24] xy xy
[320:25.00] okay
[320:29.18] i think i got this right it's hard to tell with all those warnings but
[320:36.20] let's run it and see what what pops out okay good so simple enough xy pub
[320:44.84] there we go xy
[320:49.88] xy
[320:52.86] okay now i think i got it all
[320:56.92] all right there's pubkey hash is coming out wrong so let's go fix that real quick
[321:04.20] so
[321:16.52] probably need a two hex and two un8 array that might be a better name for these because
[321:25.72] un8 array to hex is kind of long and not necessarily in a good way
[321:32.20] so
[321:40.20] okay here we go again
[321:47.80] so let me just grab all of this
[321:55.08] so
[322:02.52] but this is still missing something
[322:16.68] so
[322:24.84] where'd the private key go oh there's a private private key still there good
[322:32.20] okay so let me get back to the readme with this
[322:39.48] okay
[322:49.32] so there's the pubkey
[323:04.68] x plus y and i think i'm just going to bring this down to whatever it is
[323:11.16] looks like i'm off by one byte possibly two bytes
[323:19.00] okay there we go
[323:28.52] so
[323:36.36] okay cool so that still fits um
[323:46.36] i think i actually want to know
[323:53.56] so address xr let's see if we can get whoops what did i do let's see if we can get
[324:01.88] this to print out so we got the pubkey hash let's get the addresses out as well
[324:06.84] decoded dot xy address equals
[324:21.16] base 58 c dot
[324:22.92] encode
[324:29.00] ah
[324:43.00] okay
[324:52.84] i think that's the only thing i need in order for this to work
[325:06.84] so
[325:14.68] so
[325:26.52] there's pubkey hash
[325:40.52] so what was i complaining about
[325:50.36] 167
[326:04.92] um
[326:12.20] so
[326:22.04] so
[326:29.88] so
[326:54.04] figure out an array
[327:01.88] okay what about what else am i looking at here
[327:22.84] let's see what it's griping about right here 167
[327:27.80] parts dot pubkey hash yep it's got that encode parts
[327:38.52] okay i'm a little confused
[327:51.56] so
[327:58.52] oh
[328:12.52] so i don't know what's going on here we're gonna figure it out
[328:28.36] i doubt i would have seen that as fast
[328:38.04] yeah it's really hard with um especially with the tools reporting errors that aren't there
[328:42.68] console dot log parts
[328:55.48] parts parts parts
[329:05.80] okay so pubkey hash is undefined how is pubkey hash undefined
[329:09.96] because it seems like it was very defined just minutes ago
[329:14.20] qn8 array two hex i'm just gonna do a sanity check here
[329:23.40] that i didn't accidentally remove the return on this no i didn't
[329:29.96] but i think i think something else has gone wrong
[329:38.84] i think i missed i think i think i didn't pay close attention to that error message
[329:45.24] okay let's see where does it say it's originating from
[329:47.88] line 220 and 62 so let's just check both of those lines 220 is right here ah indeed
[329:59.64] there we go i was looking at a line that was similar called the same function but
[330:07.72] with different values that's why that was wrong okay cool so here we are again
[330:13.08] now with i think everything
[330:22.20] all right so
[330:28.84] the address that we're getting out of here is the same and i kind of would like to decode
[330:33.88] that address and make sure that it's the same well i don't have to because i've encoded these
[330:37.96] okay that one encodes the same and then x y address great so pubkey hash
[330:44.52] address
[330:56.36] she's um not used
[330:58.68] all right and then here's the address
[331:06.68] so let's take a look at these values and make sure that they all kind of make sense
[331:24.52] let's see can we call this comp flag
[331:32.84] all right so address is here
[331:46.84] and the address is the same as that address oh i don't need to print out the validity
[331:54.04] okay all right the sha has the same first letters and last letters that's good
[332:01.64] the rmd160 has the first the same first letters and last letters the pubkey hash
[332:08.84] which was used to generate the address has the same first letters and last letters so
[332:14.36] i'm convinced that all three of these
[332:26.68] um
[332:40.68] i don't know what to put there
[332:48.68] asterix not used
[332:54.68] okay pubkey hash so address let me just make sure and then we've got so we don't need the x y we've
[333:07.96] got the pubkey hash we've got the public key broken down same bytes okay we've got the check
[333:15.16] already represented up there okay and i kind of would like to do the check for the rest of this
[333:26.36] so basically i just want to provide if you did this wrong here are some values that you may
[333:33.64] this is a wrong value this is a value that you should not get if you get this value you did
[333:39.32] something wrong that's kind of what i want to do there um it's not likely to get that value but
[333:45.96] this other value it's it's incredibly likely to get the wrong value on so i actually want to do
[333:51.40] let's see x address this one this one's likely to get the wrong value on so pubkey x plus y
[334:01.00] you're actually likely to get the wrong flag here
[334:09.48] comp flag uncompressed
[334:14.76] so pubkey
[334:18.84] pubkey x
[334:27.00] and then pubkey y let's say
[334:31.56] x y
[334:38.04] so this is the x value that's the better way to represent that i think
[334:45.88] okay and then this one we're not really concerned with
[334:51.96] the private key we've already got that put up there so i don't need to worry about that
[334:57.24] the version we don't need to worry about that
[335:00.52] the version is cc that's already represented there so here we have x and y
[335:18.28] and then what do we have next we have the sha-256
[335:24.84] these values these are values you'd let's see
[335:42.20] let's just make that like this
[335:46.20] let's just make that like this
[335:50.20] and then we have
[335:52.20] let's just make that like this
[335:58.20] and then we have
[336:00.20] let's just make that like this
[336:02.20] and then we have
[336:04.20] let's just make that like this
[336:06.20] and then we have
[336:08.20] let's just make that like this
[336:10.20] and make this like this
[336:12.20] and make that like that
[336:14.20] there we go
[336:16.20] if you see these values you've accidentally used an uncompressed public key
[336:38.20] you've maybe mistaken accidentally mistakenly
[336:41.72] a little stronger word but a little more true might not have been an accidental but it was a mistake
[336:50.52] i could put sha-512 values or whatever too but i'm not going to do that
[337:07.56] end users
[337:09.56] let's see here
[337:37.40] um
[337:39.40] so pubkey hash would be this
[337:52.20] address
[337:55.64] would be this there we go
[338:03.40] so correct address this one incorrect address this one
[338:11.80] xy public key looks like yep that's good got that
[338:31.88] got that
[338:33.88] and then got
[338:35.88] this
[338:39.88] two
[338:59.88] cool
[339:01.88] maybe we could do that
[339:15.88] so now we've got some intermediary values
[339:39.88] for this
[339:41.88] so when you see it you know what it is
[339:51.88] end users never leave you surprised
[339:53.88] they don't get it right once in a while
[339:55.88] end users never leave you surprised
[339:57.88] they don't get it right once in a while