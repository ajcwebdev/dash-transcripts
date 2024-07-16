---
showLink: "https://www.youtube.com/watch?v=NqL55LDoBHk"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Code Hangout: Next-Gen DASH Tools #13: Dash HD Keys, CLI, Bikeshedding, and Beyond!"
publishDate: "2023-02-04"
coverImage: "https://i.ytimg.com/vi/NqL55LDoBHk/maxresdefault.jpg"
---

## Episode Description

AJ discusses refactoring and rebranding the Dash HD cryptocurrency library, working through code changes and API design decisions.

## Episode Summary

In this lengthy coding session, AJ works on refactoring and rebranding the Dash HD cryptocurrency library. He discusses API design decisions, updates documentation and code examples, and works through various implementation details. Key topics include renaming functions for consistency, handling asynchronous operations, and organizing the codebase. AJ also touches on broader software development concepts like versioning, dependency management, and creating command-line interfaces. Throughout the stream, he engages with viewers, answering questions and discussing his thought process behind different programming choices.

## Chapters

00:00 - Introduction and Setup

AJ begins the coding session by setting up his development environment and reviewing the current state of the Dash HD library. He discusses his goals for the refactoring process, including improving API consistency and updating documentation. The developer also mentions his intention to rebrand certain components and explains the importance of maintaining backwards compatibility while making these changes.

04:08 - Initial Code Review and Refactoring

In this chapter, AJ starts diving into the codebase, identifying areas that need improvement. He focuses on renaming functions and variables for better clarity and consistency with the rest of the Dash tools ecosystem. The developer also begins updating code examples in the documentation to reflect these changes. Throughout this process, AJ explains his reasoning behind certain naming conventions and API design choices.

16:35 - Updating Documentation and README

AJ shifts his focus to updating the project's README file and other documentation. He works on improving the installation instructions, usage examples, and API reference. The developer discusses the importance of clear documentation for open-source projects and shares his approach to writing effective documentation. He also starts working on a glossary section to explain key terms and concepts related to the library.

37:26 - API Design Discussions

This chapter involves in-depth discussions about API design choices for the Dash HD library. AJ contemplates various function names and parameter structures, weighing the pros and cons of different approaches. He considers factors such as intuitiveness, consistency with other libraries, and potential edge cases. The developer also addresses the handling of asynchronous operations and debates whether certain functions should be synchronous or asynchronous.

69:00 - Implementing Code Changes

AJ begins implementing the code changes discussed in previous chapters. He refactors function names, updates parameter lists, and adjusts the internal logic of several key components. The developer explains his thought process as he works through each change, discussing potential implications and testing strategies. He also addresses some viewer questions about specific implementation details.

104:08 - CLI Development and Package Management

In this chapter, AJ starts working on the command-line interface (CLI) for the Dash HD library. He discusses the importance of having a separate CLI package and explains his approach to structuring the code. The developer also touches on package management challenges, particularly when dealing with multiple interconnected packages within a larger project. He shares some insights on versioning strategies and dependency management.

135:20 - Final Refactoring and Code Cleanup

As the session nears its end, AJ focuses on final refactoring tasks and code cleanup. He reviews the changes made throughout the stream, ensuring consistency across the codebase. The developer also discusses future plans for the project, including additional features and improvements he wants to implement. He addresses some remaining viewer questions and summarizes the progress made during the coding session.

169:13 - Wrap-up and Future Plans

In the final chapter, AJ summarizes the work done during the stream and outlines his plans for the next steps in the Dash HD library development. He discusses the remaining tasks, such as completing the glossary and finalizing the CLI implementation. The developer also reflects on the overall refactoring process and shares some insights on managing large-scale code changes in open-source projects. The stream concludes with AJ thanking the viewers for their participation and engagement throughout the session.

## Transcript

[00:00] (upbeat music)
[00:03] (upbeat music)
[00:06] (upbeat music)
[00:08] (upbeat music)
[00:11] (upbeat music)
[00:13] (upbeat music)
[00:16] (upbeat music)
[00:19] (upbeat music)
[00:21] (upbeat music)
[00:24] (upbeat music)
[00:28] (upbeat music)
[00:31] (upbeat music)
[00:35] (upbeat music)
[00:39] (upbeat music)
[00:43] (upbeat music)
[00:49] (upbeat music)
[00:52] (upbeat music)
[00:56] (upbeat music)
[01:01] (upbeat music)
[01:05] (upbeat music)
[01:10] (upbeat music)
[01:17] (upbeat music)
[01:20] (upbeat music)
[01:22] (upbeat music)
[01:27] (upbeat music)
[01:35] (upbeat music)
[01:41] (upbeat music)
[01:46] (upbeat music)
[01:49] (upbeat music)
[01:55] (upbeat music)
[02:04] (upbeat music)
[02:13] (upbeat music)
[02:16] (upbeat music)
[02:25] (upbeat music)
[02:31] (upbeat music)
[02:38] (upbeat music)
[02:41] (upbeat music)
[02:44] (upbeat music)
[02:50] (upbeat music)
[02:57] (upbeat music)
[03:03] (upbeat music)
[03:11] (upbeat music)
[03:13] (upbeat music)
[03:20] (upbeat music)
[03:26] (upbeat music)
[03:33] (upbeat music)
[03:39] (upbeat music)
[04:08] - Wax on, wax off.
[04:12] Well, hello, hello everybody.
[04:14] And welcome back.
[04:16] It's time for another exciting episode of,
[04:18] or maybe not so exciting episode.
[04:20] I'm gonna be honest here.
[04:22] This is getting a bit long and drawn out.
[04:25] I am, I'm actually kind of tired from, from yesterday.
[04:30] But I just, I really want to get this done.
[04:33] I really, really, really do.
[04:35] We are so close.
[04:37] It's gonna be, you know, the remaining bit,
[04:39] we've got all of the core work done
[04:42] and the remaining bit is just going to be
[04:44] death by a thousand paper cuts.
[04:45] But we're gonna burn through it.
[04:47] And this one, we're gonna get published within,
[04:49] I don't know, I'm gonna set a timer.
[04:51] That's what I'm gonna do.
[04:52] 'Cause I want to get, I want to get motivated on this.
[04:54] I'm gonna set this timer to 55 minutes.
[04:58] So in 55 minutes, I want to have this Mojanker published.
[05:03] All right, turn on the beats, let's go.
[05:06] Cue the beats, cue the beats.
[05:11] All right, I'm gonna get back here.
[05:13] So my main gripes right now, if we do NPM run test,
[05:18] test, what, what, what, what?
[05:23] Oh, I'm on the wrong branch.
[05:26] Okay, it's cool, it's cool, everybody.
[05:29] Calm down, calm down.
[05:31] Don't get your knickers in a pinch.
[05:33] We're doing just fine.
[05:34] All right, NPM run test.
[05:41] What?
[05:43] Oh, right.
[05:47] Okay, I'm just gonna get over to node, let's try 16.
[05:51] What did we say?
[05:53] 16, 14, NPM install.
[05:56] Hold on, let me go into temp.
[05:58] This is one of the really dumb things.
[06:00] When you do an NPM install, location equals global.
[06:03] If you have a package.json, it'll just start adding stuff
[06:07] to the package.json, that's not what I wanted.
[06:09] We'll try node at 14.
[06:11] And then I'm gonna do this too, NPM install.
[06:15] Yeah, let's do the same NPM install.
[06:17] Make sure all of our tools are up to date.
[06:20] And then what are we doing?
[06:24] Something, we're doing a thing.
[06:27] Mm, didn't get enough sleep.
[06:29] It's past noon and I did not get enough sleep.
[06:32] It's almost four and I did not get enough sleep.
[06:34] Okay, but you know what's gonna help us?
[06:37] A can of Focus, that's what's gonna help us.
[06:40] We're just gonna open up this little can of Focus.
[06:42] It's just gonna go.
[06:43] Just like that and we're just gonna take a little sip.
[06:49] (liquid pouring)
[06:51] It's okay, I've got a second can just outside getting cold.
[07:03] Ooh, mm, I think I feel some hair on my chest
[07:07] and some tears in my eyes.
[07:08] That's good, all right, now I'm more focused.
[07:12] Cool, now I remember what I was doing.
[07:15] Actually, I don't.
[07:17] Oh, npm run test, that's what I was doing.
[07:20] There we go, that's all I wanna see.
[07:24] Quit your whining, get the work done.
[07:27] All right, so npm package shields, blah, blah, blah, blah.
[07:35] I don't know, I don't know about all this shield stuff.
[07:47] I'm just, I'll be interested to see what happens.
[07:50] I'm probably just gonna delete these things.
[07:52] But I'll put it up for now.
[07:58] Boing.
[08:05] Standard style button, ugh, no.
[08:13] I'm just getting rid of these, these are terrible.
[08:16] Buttons are for dweebs.
[08:18] We're beyond that, we're dash HD now, high definition dash.
[08:23] Hmm, dash HD dot JS, yeah.
[08:32] GitHub.com dash hive dash HD dot JS, there we go.
[08:43] All right, JavaScript component for BIP32.
[08:47] Hark, hark, let's just do deterministic keys.
[08:50] What'd I call the other one?
[08:53] Let me see what I called the other thing.
[08:59] The dash keys.
[09:00] I had some good, some good language in here.
[09:13] (soft music)
[09:15] Okay, what I'd like to do is actually grab that zoomonic,
[09:22] if I can, let's see.
[09:25] So the things that are gonna be important are...
[09:28] Zoomonic seed path, yada, yada.
[09:36] All of that stuff we have in dash keys
[09:38] in the README, I think.
[09:40] Zoo, zoo, zoo.
[09:42] Look at that.
[09:42] I should also have seed here as well.
[09:46] But we're gonna do the same thing.
[09:49] So we're gonna say passphrase, secret salt, seed.
[09:55] This is the thing that I don't know.
[09:58] I don't know what our seed is, but we are gonna find out.
[10:03] All right.
[10:06] (soft music)
[10:09] All right.
[10:13] Generate and restore HD
[10:23] dash keys.
[10:28] (soft music)
[10:30] And extended keys, xpriv, xpub.
[10:41] (soft music)
[10:44] (keyboard clacking)
[11:13] Keys, wallets, and extended keys.
[11:17] That music sounds weird.
[11:31] It's got too many things mixed together in it.
[11:33] All right, wallets and extended keys.
[11:41] Yep, 32.
[11:43] (soft music)
[11:46] (keyboard clacking)
[11:49] (soft music)
[11:51] (keyboard clacking)
[11:54] (soft music)
[12:24] Addable with the BIP32, blah, blah, blah, blah, blah.
[12:29] Actually, let's bring this down.
[12:31] Yeah.
[12:38] BIP32 spec.
[12:50] (keyboard clacking)
[12:53] There we go.
[12:56] It looks good.
[12:57] (keyboard clacking)
[13:08] Now let's see.
[13:15] Can I, do we have a two seed method here?
[13:19] (keyboard clacking)
[13:21] Or from master seed.
[13:25] Actually, so this is more dealing with the seed part.
[13:28] So passphrase, which I think still deserves
[13:34] to stand on its own, dashphrase at least,
[13:36] still kind of deserves to stand on its own.
[13:39] Maybe not, maybe it should be absorbed into this.
[13:41] For now, I'm gonna let it stand on its own.
[13:43] (keyboard clacking)
[13:46] But this is really only dealing with it
[13:50] from the perspective of having a seed.
[13:54] So this is not really about,
[14:00] so this would be HD seed.
[14:08] (keyboard clacking)
[14:11] And then I also have the question of,
[14:32] should this be dashphrase with a capital P?
[14:36] And I think it should.
[14:37] That's one of the things that I'm thinking about
[14:40] as we go back through here.
[14:41] I think it should be dashphrase.
[14:46] Yeah.
[14:49] Let's see.
[14:53] Dashphrase.
[14:55] Good old Donkey Kong.
[15:01] (imitating Donkey Kong music)
[15:05] (imitating Donkey Kong music)
[15:09] I'm having a good time, all right?
[15:18] Don't stop me now.
[15:19] (whistling)
[15:24] Riding the wave.
[15:25] And I'm gonna get that second Mountain Dew.
[15:27] I'm gonna chug it.
[15:28] So, all right, I'm gonna be honest.
[15:30] I did go out to eat for lunch.
[15:32] I did, all right?
[15:34] I got fat.
[15:35] I did.
[15:36] But you know what?
[15:37] Their Dr. Pepper machine sucked.
[15:41] (crashing)
[15:53] Okay.
[16:04] Works with
[16:06] dashphrase.
[16:12] I don't know what the words should be,
[16:28] so I might just leave it for now,
[16:29] but let me think through it.
[16:30] So, it works with dashphrase
[16:32] to generate and restore dash HD keys,
[16:34] wallets, and extended keys.
[16:36] And dashphrase is the BIP39 or whatever it is, right?
[16:59] Let's see here.
[17:02] (typing)
[17:04] BIP39.
[17:11] Copy clean link, yes.
[17:21] So, I think copy clean link,
[17:23] I think what it does is it resolves it.
[17:25] So, if it's got a bunch of ads or stuff like that.
[17:28] (typing)
[17:30] It gets out of the way.
[17:34] There we go.
[17:56] (typing)
[17:58] And is this actually how we spell it?
[18:01] I think it is, but I'm not sure.
[18:04] Okay, good.
[18:10] Showed Russian nesting dolls for hierarchical.
[18:13] I guess that's appropriate.
[18:14] All right.
[18:16] (typing)
[18:20] (upbeat music)
[18:22] From dash seeds.
[18:32] All right, so right off the bat,
[18:47] I'm actually gonna start cobbling together.
[18:50] So, there's the usage section.
[18:53] So, oh, we need to update the license.
[18:57] (burping)
[19:03] Bless me.
[19:04] (typing)
[19:07] (upbeat music)
[19:09] Let's see, what do we got here in the license?
[19:21] (upbeat music)
[19:26] (typing)
[19:28] There we go.
[19:46] Maybe, maybe not.
[19:53] (upbeat music)
[19:56] Hmm, okay, I'm gonna update the license.
[20:03] It'll be its own commit.
[20:04] Actually, let's just go ahead and do that real quick.
[20:06] So, it gets dash.
[20:08] Little important bit here.
[20:17] (upbeat music)
[20:20] Was it, there we go, look at that.
[20:27] Alt + G, baby.
[20:28] (upbeat music)
[20:31] Okay.
[20:46] (upbeat music)
[20:49] There we are.
[21:14] Let's do a little git diffity diffity on this.
[21:16] See if we just added two lines
[21:19] or we changed anything else.
[21:20] Good.
[21:24] All right, add license.
[21:27] And I always like to put C license in license.
[21:33] Read me.
[21:41] (upbeat music)
[21:44] And because we can, I just like that little symbol.
[21:50] Little Unicode there.
[21:54] Not suitable for plain text, you see,
[21:56] but suitable for our purposes here.
[21:58] Package.json.
[22:05] Oh, crap, hold on.
[22:08] Webby, node at 18.
[22:10] Webby's so convenient.
[22:11] (upbeat music)
[22:15] Now, what in the world did package lock change for?
[22:28] That's the question of the ages.
[22:31] (upbeat music)
[22:35] (typing)
[22:37] There we go.
[22:52] That's good.
[22:53] Update license.
[23:00] Boom.
[23:02] (upbeat music)
[23:04] And of course, I'm gonna have all this little ditty here
[23:16] that it's upset about.
[23:18] Bleh.
[23:20] Okay, so what else were we gonna do?
[23:25] So I was gonna put, start the glossary section here
[23:30] because we've got a number of words.
[23:32] So we've got bip 32.
[23:35] C.
[23:37] Bless me again.
[23:44] Sorry, I'm just gonna be super crude today.
[23:46] Crass, not crude, but crass maybe?
[23:49] I don't know.
[23:50] I'm just gonna be myself.
[23:51] (upbeat music)
[23:53] Okay.
[24:18] (upbeat music)
[24:21] And then what's bip 39?
[24:27] (upbeat music)
[24:47] Unanimously discouraged for implementation.
[24:51] (upbeat music)
[24:53] (upbeat music)
[24:56] Hey, by the way, you know what we get to do?
[25:20] (upbeat music)
[25:23] (upbeat music)
[25:25] Wait to go here under JavaScript.
[25:29] Where's JavaScript?
[25:31] JavaScript, JavaScript, look at this.
[25:34] How are these listed alphabetically?
[25:36] (upbeat music)
[25:38] I don't know how these are listed.
[25:44] That's not alphabetic.
[25:45] (upbeat music)
[25:49] Uh, uh, uh, AJ's broken, AJ's broken.
[25:54] What's the sort order?
[25:58] What's the sort order?
[26:00] (upbeat music)
[26:02] HTTPS, github.com, dash hive, dash phrase.js.
[26:10] (upbeat music)
[26:16] (upbeat music)
[26:18] I don't think there's anything about this
[26:27] is actually dash specific.
[26:30] (upbeat music)
[26:33] (upbeat music)
[26:59] Implementations.
[27:03] (upbeat music)
[27:05] (upbeat music)
[27:08] (upbeat music)
[27:11] (upbeat music)
[27:13] (upbeat music)
[27:20] (upbeat music)
[27:27] (upbeat music)
[27:39] (upbeat music)
[27:42] Let me just assert or check my assertion real quick.
[27:55] (upbeat music)
[27:57] (upbeat music)
[28:00] Wizard.
[28:12] (upbeat music)
[28:27] Okay, net remove, spurious.
[28:31] Well, it's not spurious.
[28:33] I use that term way too often.
[28:35] It's not a correct term.
[28:36] Extraneous is what I mean.
[28:40] (upbeat music)
[28:43] (upbeat music)
[28:46] (upbeat music)
[28:48] (upbeat music)
[28:51] (upbeat music)
[28:56] (upbeat music)
[29:04] (upbeat music)
[29:09] (upbeat music)
[29:13] (upbeat music)
[29:16] Let's see, bun run.
[29:25] (upbeat music)
[29:27] What?
[29:28] (upbeat music)
[29:31] (upbeat music)
[29:41] (upbeat music)
[29:44] A little confused here.
[29:47] Where are my console.infos?
[29:51] (upbeat music)
[29:54] (upbeat music)
[30:11] (upbeat music)
[30:14] I'm very confused.
[30:33] (upbeat music)
[30:36] (upbeat music)
[30:38] I am so confused.
[30:58] What is going on?
[31:00] Seriously here.
[31:02] (upbeat music)
[31:06] (upbeat music)
[31:08] All right, why is this not running at all?
[31:27] Even a little bit.
[31:28] (upbeat music)
[31:30] (upbeat music)
[31:33] Okay.
[31:48] (upbeat music)
[31:51] Oh, whoops.
[31:56] (upbeat music)
[31:59] (upbeat music)
[32:02] Undefined is not an object.
[32:11] Ah, okay, fine.
[32:14] It's not bun compatible yet.
[32:15] (upbeat music)
[32:19] (upbeat music)
[32:21] Okay, cool.
[32:30] So, get ourselves on the official list.
[32:32] Yeah.
[32:33] (upbeat music)
[32:36] Interesting.
[32:46] (upbeat music)
[32:49] Is that a problem?
[32:58] (upbeat music)
[33:15] Okay, well, screw you.
[33:17] I mean, we could just add versioning to it.
[33:22] That seems fine.
[33:25] I don't know.
[33:26] That seems like a really small problem
[33:27] rather than unanimously discouraged.
[33:29] Maybe just add a version.
[33:32] It seems like pretty decent.
[33:34] I think that it should have more and more word
[33:35] for a checksum,
[33:36] but I'm not gonna complain about the way that it turned out.
[33:40] (upbeat music)
[33:43] These ought to be alphabetic.
[33:50] There needs to be a sort order.
[33:54] Whatever.
[33:57] Okay.
[33:58] If you don't want AJs to go nuts,
[34:02] have a sort order.
[34:04] Basic AJ-ism.
[34:07] (upbeat music)
[34:09] Oh, and then again, what was...
[34:19] The reason I came here was to learn,
[34:22] does this have an actual name?
[34:24] Title.
[34:36] See HD keys.
[34:39] Passphrase.
[34:48] Mnemonic.
[34:50] And then we're gonna have a secret salt,
[35:02] but that's gonna be in the other one.
[35:03] That's not gonna be here.
[35:04] (upbeat music)
[35:07] Okay, we're also gonna have a HD passphrase mnemonic.
[35:19] It's gonna be...
[35:21] You know what it's gonna be though?
[35:22] It's gonna be C-phrase.
[35:24] (upbeat music)
[35:26] (keyboard clicking)
[35:29] Also, BIP-39.
[35:41] BIP-39.
[35:42] Also,
[35:49] C-phrase.
[35:55] (keyboard clicking)
[35:58] Passphrase.js.
[36:01] 12 words.
[36:10] 11.
[36:17] 11 and...
[36:21] Oh gosh, what's the...
[36:23] Unicode 1/2.
[36:24] (keyboard clicking)
[36:27] (upbeat music)
[36:30] (keyboard clicking)
[36:34] (keyboard clicking)
[36:37] (keyboard clicking)
[36:40] (keyboard clicking)
[36:43] (keyboard clicking)
[36:46] (keyboard clicking)
[36:49] (keyboard clicking)
[37:19] (keyboard clicking)
[37:22] What a mouthful.
[37:43] (keyboard clicking)
[37:46] (keyboard clicking)
[37:49] Okay, so we got some of this stuff coming along.
[38:13] (keyboard clicking)
[38:16] HD keys.
[38:22] Also...
[38:26] (keyboard clicking)
[38:33] I don't know.
[38:40] Personally, I'm not actually sure
[38:41] what the right phrasing for this thing is
[38:44] in terms of...
[38:45] Which is the key?
[38:47] Is it referring to...
[38:49] (keyboard clicking)
[38:56] (keyboard clicking)
[38:59] Root seed.
[39:17] Derived child.
[39:20] Derive.
[39:23] (keyboard clicking)
[39:26] HD path.
[39:28] There's all sorts of stuff that comes off of this.
[39:31] QRST.
[39:32] (keyboard clicking)
[39:36] (keyboard clicking)
[39:39] (keyboard clicking)
[39:42] Um...
[40:05] (keyboard clicking)
[40:08] (keyboard clicking)
[40:11] Let's see here.
[40:22] (keyboard clicking)
[40:37] All right.
[40:38] Let's see, what does BIPS stand for?
[40:42] BIPS.
[40:43] (keyboard clicking)
[40:46] Let's see.
[41:02] Request for comments.
[41:06] (keyboard clicking)
[41:09] Let's see, what does BIPS stand for?
[41:30] Okay, my timer is...
[41:35] I wasn't thinking about my timer.
[41:37] I started thinking about the glossary.
[41:39] So, my timer's just ticking away.
[41:42] I'm gonna have to reset it.
[41:43] (keyboard clicking)
[41:49] Okay, Bitcoin.
[42:01] Can I get the standard?
[42:05] Okay.
[42:06] Bitcoin Improvement Proposal.
[42:09] (keyboard clicking)
[42:12] (keyboard clicking)
[42:15] (keyboard clicking)
[42:18] Oh.
[42:36] (keyboard clicking)
[42:39] (keyboard clicking)
[42:42] Okay.
[42:46] (keyboard clicking)
[42:50] (keyboard clicking)
[42:53] Not used directly in this...
[43:19] Not used directly in this library.
[43:23] But important.
[43:31] How the HD seeds are typically generated.
[43:40] (keyboard clicking)
[43:43] (keyboard clicking)
[43:46] Okay.
[44:06] Got some good stuff here.
[44:10] HD Path Example.
[44:13] Okay, so I do wanna fill out the glossary on this,
[44:24] but let me get back to some of the other stuff for a minute.
[44:28] What got me off on that was I wanted to find
[44:31] what the HD seed is for this phrase.
[44:36] I wanna know what the HD seed is.
[44:38] HD, HD seed.
[44:42] (keyboard clicking)
[44:45] Something like this.
[45:08] (keyboard clicking)
[45:11] I wonder, could we just do...
[45:15] No, it doesn't.
[45:16] 'Cause it doesn't actually matter which number you pass in.
[45:19] 'Cause one, so zero doesn't depend.
[45:28] So there's a difference between a child and a sibling.
[45:30] Siblings do not depend on each other.
[45:33] Children depend on their parents.
[45:35] (keyboard clicking)
[45:38] So basically, up to the hardened path,
[45:43] everything you can depend on, whatever.
[45:47] (keyboard clicking)
[45:50] (keyboard clicking)
[45:53] 99's a good number.
[46:13] Anyway, okay, so I wanna be able to generate these things.
[46:18] I want to be able to generate the pass phrase.
[46:22] Let me get back to dash phrase real quick.
[46:25] Let me get back to the read me.
[46:29] So it looks like I did not actually create a bin for the,
[46:34] or a CLI for this, which is a pity,
[46:36] 'cause there needs to be one.
[46:38] (keyboard clicking)
[46:42] (keyboard clicking)
[46:45] Okay, but this actually needs to define the salt,
[47:09] and it does not.
[47:10] (keyboard clicking)
[47:13] So.
[47:17] Let me get the seed.
[47:30] (keyboard clicking)
[47:33] Yeah, okay.
[47:38] So I need, just gonna, real quick.
[47:40] Famous last words, every day of my life.
[47:53] (keyboard clicking)
[47:56] (keyboard clicking)
[47:59] Okay, let dash phrase equals dash phrase dot generate.
[48:15] Let phrase console dot log.
[48:23] Actually, I don't care about
[48:24] generating the phrase that much.
[48:27] (keyboard clicking)
[48:30] Okay, so we got the phrase, and then we've got the,
[48:41] so at this point, I just want to say,
[48:43] actually, zoo, zoo, zoo.
[48:45] And then let's repeat that, and repeat that,
[48:50] and repeat that.
[48:51] Wrongo bongo.
[48:53] Zoo, zoo, zoo.
[48:54] Zoo, zoo, zoo.
[48:55] Zoo, zoo.
[48:57] Zoo, wrong.
[48:58] One, two, three, four.
[48:59] One, two, three, four.
[49:00] One, two, three, wrong.
[49:02] Excellent.
[49:03] Okay, let secret equals blah.
[49:10] And secret equals treasure.
[49:15] Okay.
[49:18] And then I think I did actually do this
[49:22] as part of the, what is now dash HD CLI,
[49:25] but some of that actually does need to move out
[49:27] to dash phrase.
[49:28] Okay, mnemonic generate.
[49:51] (keyboard clicking)
[49:54] Function generate.
[50:07] (keyboard clicking)
[50:10] Function generate.
[50:11] (keyboard clicking)
[50:14] And then just put out here,
[50:24] the canonical zoomonic
[50:30] should be used for developer,
[50:39] for test fixtures and documentation.
[50:42] I actually need to build that into this particular library,
[50:59] so we should have dash phrase dot zoomonic equals,
[51:03] something like that.
[51:09] (keyboard clicking)
[51:12] Let's see.
[51:33] (keyboard clicking)
[51:37] (keyboard clicking)
[51:40] (keyboard clicking)
[51:43] (keyboard clicking)
[51:46] (keyboard clicking)
[52:04] (keyboard clicking)
[52:07] All right, and then the secret.
[52:30] (keyboard clicking)
[52:33] (keyboard clicking)
[52:36] Okay, that's a little tongue and cheeky, but whatever.
[52:43] (keyboard clicking)
[52:46] (keyboard clicking)
[52:49] Your mnemonic.
[53:05] (keyboard clicking)
[53:08] (keyboard clicking)
[53:11] Okay, something like that maybe.
[53:20] Oh, and then we need to have,
[53:22] I think 128 should be the default.
[53:24] That's good enough for me.
[53:27] Okay, and then generate.
[53:32] (keyboard clicking)
[53:35] (keyboard clicking)
[53:38] And secret salt.
[53:57] (keyboard clicking)
[54:01] (keyboard clicking)
[54:04] Boom, there we go.
[54:10] (keyboard clicking)
[54:14] Why?
[54:20] Why, bun?
[54:22] Why don't you have web crypto implemented?
[54:24] Why?
[54:28] Seems like that should be the first thing to implement.
[54:31] Of course, I wonder.
[54:34] I do wonder.
[54:40] Maybe it is implemented.
[54:44] I should probably go look it up.
[54:46] But what about global this.crypto?
[54:50] Or let's try that one.
[54:53] (keyboard clicking)
[54:56] Hey, so that did work.
[55:03] Okay, so let's go update that PR.
[55:12] (keyboard clicking)
[55:15] (keyboard clicking)
[55:18] Okay, so, okay, here's our problem.
[55:39] (keyboard clicking)
[55:44] (keyboard clicking)
[55:47] This music's really interesting.
[55:48] I like it.
[55:49] But it's got an edge to it that's quite strange.
[55:54] (keyboard clicking)
[55:57] (keyboard clicking)
[56:02] (keyboard clicking)
[56:12] (keyboard clicking)
[56:15] No, that's not what I wanted to do.
[56:23] Oops.
[56:25] I wanted to check it out.
[56:31] I wanted to look at it.
[56:32] (keyboard clicking)
[56:36] (keyboard clicking)
[56:39] Okay.
[57:01] (keyboard clicking)
[57:04] (humming)
[57:09] Let's see.
[57:13] Ugh.
[57:25] Oh, sorry.
[57:28] There's something.
[57:30] Okay, I'm going to
[57:31] on GitHub.
[57:35] Node web crypto.
[57:44] (keyboard clicking)
[57:57] (keyboard clicking)
[58:00] So bug report.
[58:15] (humming)
[58:20] (keyboard clicking)
[58:24] (keyboard clicking)
[58:27] (keyboard clicking)
[58:38] Oh, what version of BUN are you running?
[58:46] Oh, oh, that hurts my heart.
[58:51] Oh, that hurts my heart.
[58:53] That should be a dash capital V.
[58:55] No, that's not supposed to be lowercase V.
[58:58] Um.
[59:00] (keyboard clicking)
[59:06] Okay, let's crypto equals require node.
[59:21] (keyboard clicking)
[59:24] Crypto dot subtle dot digest.
[59:35] Let's just see.
[59:38] What was it in here?
[59:39] (keyboard clicking)
[59:44] (keyboard clicking)
[59:47] All right, let's report this.
[60:05] All right, my timer's up.
[60:10] I sucked.
[60:12] But my other Mountain Dew is probably cold by now.
[60:15] So that's the good news.
[60:17] (keyboard clicking)
[60:20] (keyboard clicking)
[60:23] All right, is this enough to reproduce it?
[60:50] I think it shall be.
[60:51] (keyboard clicking)
[60:55] Get random values.
[61:20] (keyboard clicking)
[61:23] (keyboard clicking)
[61:26] (keyboard clicking)
[61:30] (keyboard clicking)
[61:58] Um.
[61:59] Global this dot crypto.
[62:04] And require node crypto.
[62:13] (keyboard clicking)
[62:17] Should all return the same.
[62:28] Web crypto object.
[62:31] What do you see instead?
[62:38] It's hodgepodge.
[62:43] There's some web crypto.
[62:49] (keyboard clicking)
[62:55] (keyboard clicking)
[62:58] Not all of it.
[63:04] Okay.
[63:11] And then just for giggles,
[63:25] let's change this to global this dot crypto.
[63:29] (keyboard clicking)
[63:34] Console dot log.
[63:39] (keyboard clicking)
[63:44] (keyboard clicking)
[63:47] See if this random bytes works.
[64:08] (keyboard clicking)
[64:12] (keyboard clicking)
[64:15] One run.
[64:18] (keyboard clicking)
[64:22] (sighs)
[64:39] (keyboard clicking)
[64:42] Oops, so X.
[64:47] X, X, X, X, X, X, X.
[64:54] Come on, I'm right here, man, I'm right here.
[64:56] Give me the X.
[64:57] There we go.
[65:00] (keyboard clicking)
[65:03] (keyboard clicking)
[65:06] Nah, I'm just not even gonna include that stuff.
[65:23] It doesn't matter.
[65:24] Or at least.
[65:32] (keyboard clicking)
[65:35] Node crypto.
[65:39] And.
[65:44] Should return.
[65:48] A web crypto plus node crypto object,
[65:58] just like node does.
[66:00] (keyboard clicking)
[66:03] All right, there we go.
[66:08] Okay.
[66:09] Okay, so now this is supported.
[66:14] So bug fixed, crisis averted.
[66:19] (keyboard clicking)
[66:23] (keyboard clicking)
[66:26] Hmm.
[66:40] (keyboard clicking)
[66:43] (keyboard clicking)
[66:46] Oh, the docs are a little bit better over here,
[66:57] is that what we're saying?
[66:58] Oh, interesting.
[67:10] Okay, so this actually is a little bit ahead.
[67:13] All right, fair enough.
[67:14] (sighing)
[67:23] Okay.
[67:33] Well, let me go ahead and
[67:37] git stash pull.
[67:42] Stash pop.
[67:44] Let me think about this.
[67:48] This is not the one I was intending to work on.
[67:59] Why did these not get propagated already?
[68:01] Oh, interesting.
[68:05] (keyboard clicking)
[68:08] Okay, so this does have a lot more.
[68:16] Why did those commits not show up
[68:17] when I was looking at it the other direction?
[68:19] We should actually have validate there, not verify.
[68:31] We need to get straight on that.
[68:34] (keyboard clicking)
[68:37] Okay, so I need to figure out real quick using this.
[68:43] Okay, so here we go.
[68:45] So bun run bin dash phrase.
[68:49] Oops, I'll wait.
[69:00] (keyboard clicking)
[69:03] Interesting.
[69:14] Hmm.
[69:26] (keyboard clicking)
[69:29] All right, let's see.
[69:37] So what if I don't want error?
[69:38] I want just warn, maybe?
[69:40] I don't know which of these is going out to
[69:56] standard error and standard out or whatever.
[69:58] Dev null.
[70:02] Hmm, that's not the behavior that I want.
[70:07] That is not the behavior that I want.
[70:11] That's not why I use standard error.
[70:20] That's not why I use it.
[70:23] Oh well.
[70:24] (keyboard clicking)
[70:27] Oh wait, oh, okay, good.
[70:33] Nevermind, it is working.
[70:35] It is working.
[70:36] It's working just the way I would expect it to work.
[70:38] Okay, I do like that it has top level of weight
[70:46] even in regular JavaScript files.
[70:49] That's really nice.
[70:53] Okay.
[70:54] So what else do I need to do?
[70:58] I need to use,
[71:00] I need to be able to generate the seed.
[71:02] I think this encode,
[71:14] this is basically to seed, right?
[71:19] Wait, what is encode?
[71:23] Oh no, encode is encode the bytes.
[71:26] So this should probably be called something like
[71:29] base 2048 encode.
[71:32] Oh, that's the other thing,
[71:34] is that this is also base 2048,
[71:37] base 2048.
[71:38] Okay, so let me go back to,
[71:41] blah, what is it?
[71:44] Dash HD, read me.
[71:48] (keyboard clicking)
[71:51] Oh, HD key, read me.
[72:11] (keyboard clicking)
[72:14] Bit 44.
[72:21] (keyboard clicking)
[72:26] (keyboard clicking)
[72:30] (keyboard clicking)
[72:33] (keyboard clicking)
[72:36] (keyboard clicking)
[72:39] (keyboard clicking)
[72:42] (keyboard clicking)
[72:45] (keyboard clicking)
[72:52] (keyboard clicking)
[73:11] (keyboard clicking)
[73:14] Encode data using whole words
[73:31] rather than characters.
[73:40] 2048 whole words
[73:43] rather than 32, 58, 62, 64.
[73:56] (keyboard clicking)
[74:07] (keyboard clicking)
[74:10] Okay, and we're gonna say, see this, got it.
[74:31] (keyboard clicking)
[74:34] Hmm.
[74:39] (sighs)
[74:44] (keyboard clicking)
[74:50] (keyboard clicking)
[75:00] (keyboard clicking)
[75:03] Each word represents 11 bits of information
[75:21] or 11 bits of information.
[75:26] 12 words represent 131 bits of information.
[75:42] (keyboard clicking)
[75:45] Extra bits can be used for a checksum.
[75:59] (keyboard clicking)
[76:06] (keyboard clicking)
[76:09] Rather than using a bank of the characters,
[76:31] you can encode data using a bank of whole words.
[76:36] If you use
[76:42] words, each word represents 11 bits.
[77:01] 12 words represent, yeah, there we go, that's good.
[77:06] Let me get out of there.
[77:08] So I'm back in here and the thing that I wanted to do
[77:10] was go to seed, to seed.
[77:14] And I think I am gonna have to take a short,
[77:17] short potty break and grab another Mountain Dew
[77:21] to spice up my life until the Spice Force 5 gets here.
[77:27] (soft music)
[77:30] Okay, dash phrase to seed.
[77:36] I'm also thinking one of the thoughts that's occurred to me,
[77:40] and this is not something I'm gonna focus on right now,
[77:43] but it is a minor change,
[77:46] is actually to hard depend in dash keys on,
[77:51] well, not hard depend, soft depend still
[77:55] on Sec P256K1, but move all of the Sec P256K1 methods
[78:00] into dash keys.
[78:03] So sign, verify, to public key, public key normalize,
[78:08] the whole gambit, because pretty much every time
[78:17] you're gonna be using the whole thing, you know?
[78:24] All right, and this is async.
[78:26] Then dash phrase.
[78:30] Oh, this is gonna be really good.
[78:39] So we're gonna do let seed equals await to seed.
[78:46] Then we're gonna have phrase and secret.
[78:51] (soft music)
[78:53] Let secret equals.
[79:07] Let phrase equals.
[79:16] (soft music)
[79:19] Console.log.
[79:34] Now, hopefully, I did the same thing,
[79:38] and this is coming out as, wait,
[79:43] I thought I had a bunch of types in here.
[79:45] I do have a bunch of types in here.
[79:47] But, okay, and they are typed down there.
[79:50] Good, good, good, good, good, good.
[79:52] Oh, interesting, but I didn't have to type them
[79:54] in the middle.
[79:55] That's so strange.
[79:57] Whatever.
[79:58] Okay, so to seed is gonna be phrase to seed,
[80:05] and it is returning a promise, excellent, of UN8 array.
[80:13] And then I just need to hex.
[80:18] (soft music)
[80:21] (typing)
[80:23] (soft music)
[80:25] (typing)
[80:27] (soft music)
[80:30] (typing)
[80:33] (soft music)
[80:35] (typing)
[80:37] (soft music)
[80:40] (typing)
[80:42] (soft music)
[80:44] (typing)
[80:46] (soft music)
[81:14] G.toString16.padStartToZero.
[81:16] Cheating, cheating, cheating.
[81:30] Yeah, definitely gonna need some macros
[81:41] for stuff like this in GPT script.
[81:44] (typing)
[81:46] Okay, so, and maybe that shouldn't really go in there.
[82:01] Because, again, this is a developer thing,
[82:05] it's not an end user thing.
[82:08] An end user isn't gonna be turning stuff in a hex,
[82:10] so why thrust it in there?
[82:15] It makes sense for dash queues,
[82:18] it probably doesn't make sense for dash phrase.
[82:20] (soft music)
[82:24] (typing)
[82:28] (soft music)
[82:34] (typing)
[82:39] (soft music)
[82:42] (sighs)
[82:51] (typing)
[82:53], okay.
[83:19] The canonical, whoops.
[83:23] Zoomonic HD seed.
[83:30] Oh, that did not work out.
[83:44] Did not work out at all.
[83:47] That reduce, oh, map, sorry, reduce.
[83:51] Hmm, that did not work out.
[83:59] Oh, so reduce works on a node buffer, maybe,
[84:05] but it doesn't work on an array buffer, I see.
[84:10] All right.
[84:13] (typing)
[84:16] Or let B of bytes, let's see if this will work.
[84:24] (typing)
[84:43] There we go.
[84:44] So this is with the treasure secret,
[84:50] but what if we take the secret away?
[84:51] Okay, so that's good news.
[85:04] Now I know how to document this properly.
[85:07] (typing)
[85:09] Let's see.
[85:24] (typing)
[85:33] (soft music)
[85:35] Indeed, it is salty.
[85:57] (typing)
[85:59] How's it going, Exploding New?
[86:13] Hey, are you, are you someone whose initials begin,
[86:18] whose initials, are you Chris?
[86:26] (typing)
[86:28] There we go, all right, out with it.
[86:32] The saltiest seed.
[86:35] Well, this one is.
[86:38] No, not Chris, okay.
[86:40] All right, 'cause somebody was watching the other day,
[86:44] and it was somebody I actually knew,
[86:46] and I don't remember how many times you've been here.
[86:50] Sorry, 'cause you know, there's hundreds of people
[86:52] over the course of the past year
[86:54] that, you know, have been on for a few sessions,
[86:57] and it's gotten to the point
[86:59] where I can no longer remember all the usernames.
[87:01] So maybe hundreds is strong, but maybe it's not.
[87:07] I don't think there's been 200 unique people
[87:10] that have said hello.
[87:13] I don't know, I've got, what,
[87:15] 300 followers or something like that?
[87:17] Maybe there have been.
[87:18] Anyway, it's getting to the point where, you know,
[87:22] it's more than I can manage on an individual level.
[87:25] That's all I'm saying.
[87:26] Okay.
[87:45] If we decode that, we get the input entropy.
[87:50] If we...
[87:51] Okay.
[87:58] For extra entropy/protection,
[88:03] we can also use a secret salt.
[88:19] On those, we get the seed.
[88:23] With secret salt.
[88:32] Without.
[88:38] Empty secret salt.
[88:46] (computer mouse clicking)
[88:49] You have several accounts on here?
[88:52] Okay.
[88:54] Well, I don't know which account you are,
[88:56] but I do know that my need to go tinkle-tinkle
[89:03] is becoming greater by the moment.
[89:07] Okay.
[89:14] (computer mouse clicking)
[89:18] Okay.
[89:29] Oh, so much terminology.
[89:32] Okay, where am I at right now?
[89:40] Where have I gotten lost?
[89:42] Where have I gotten lost here?
[89:44] My goal was to publish Dash HD, but then...
[89:48] Oh, wait, I gotta make sure the dash phrase is gonna work.
[89:51] Oh, wait, does dash phrase actually work with bun?
[89:54] La-da-da-da-da.
[89:55] Oh, whoops.
[90:14] (computer mouse clicking)
[90:16] What was that?
[90:17] An extra line got deleted.
[90:21] Okay, fine, I don't care.
[90:22] Add bun compatibility, break Node v12 compatibility.
[90:36] I don't care about that one.
[90:38] Goodness knows.
[90:39] The JavaScript ecosystem is so hard.
[90:44] I need to focus more on core features and bugs
[90:49] and less on cool, shiny crap.
[90:53] Okay.
[91:01] Support buns web crypto.
[91:10] (computer mouse clicking)
[91:14] Hey, Nextdoor, I do remember you.
[91:32] I don't remember any of the conversations we've had,
[91:35] but I remember the username at least.
[91:38] (computer mouse clicking)
[91:41] Okay.
[91:56] (computer mouse clicking)
[92:04] (computer mouse clicking)
[92:08] Let me just double check.
[92:17] (computer mouse clicking)
[92:22] (computer mouse clicking)
[92:26] All right, Canonicals, Emonic HDC.
[92:50] (computer mouse clicking)
[92:54] (computer mouse clicking)
[92:57] Okay.
[93:20] (computer mouse clicking)
[93:24] Secret is secret.
[93:33] It's a secret to everybody.
[93:37] It's a secret to everyone.
[93:41] (computer mouse clicking)
[93:46] (computer mouse clicking)
[93:50] Okay, run this again.
[94:15] I just wanted to make sure, yep, 069.
[94:19] Okay, so.
[94:21] (computer mouse clicking)
[94:25] Okay.
[94:44] (computer mouse clicking)
[94:48] (sighs)
[94:53] Show with and without secret salt.
[95:01] (computer mouse clicking)
[95:12] Zoomonic seed with and without secrets.
[95:17] Okay, rebase -i main.
[95:25] Where's this white space go?
[95:28] It goes right here, actually.
[95:30] (computer mouse clicking)
[95:35] (computer mouse clicking)
[95:39] Git, git push, tags, blah, blah, blah, blah, blah.
[95:48] Okay.
[95:51] Do not challenge me for the next five minutes, fool.
[96:02] You dare challenge me?
[96:05] Cool.
[96:17] So, a new dash phrase is published, huzzah.
[96:22] (computer mouse clicking)
[96:28] Wait, oh, no, that's not what I wanted to do.
[96:31] (computer mouse clicking)
[96:34] Well, maybe it is, actually.
[96:37] So, bun, run, dash phrase, cool.
[96:40] (yawns)
[96:48] Why so many frameworks?
[96:50] Exactly, exactly.
[96:54] Do you mean why so many that I'm supporting?
[96:59] Why there are so many, or what?
[97:03] Could you be more specific with your question, please?
[97:06] Let's see, what's a pithy way I could say this
[97:19] with empty salt and low sodium?
[97:22] (laughs)
[97:23] No sodium.
[97:24] (laughs)
[97:26] Okay.
[97:30] The good news is I'm quickly coming up against the problem
[97:42] that I need, I want to solve for,
[97:45] which is managing lots of NPM modules
[97:50] inside of sub-repositories.
[97:55] This is sub-modules.
[98:00] This is, because I want to prove that this is not difficult,
[98:04] and the way that I'm gonna prove it is by writing a script
[98:08] at the top level that walks everything down
[98:11] and then updates all things to be the same version
[98:14] with each other, and we're getting to a point
[98:16] where everything has a CLI that's its own package,
[98:19] which is the way it should be so that you're not polluting
[98:22] dependencies all over the place.
[98:24] Everything has a separate things
[98:27] that don't need to be together get to be apart.
[98:31] So anyway, it's getting to the point
[98:42] where it's gonna start to be tedious
[98:44] to manage all of these NPM modules,
[98:49] where maybe one change requires 10 of them to be updated,
[98:55] because if we update one at the bottom level,
[98:59] because we find a bug, and then three things depend on that,
[99:03] and four other things depend on those three things,
[99:08] then we have eight things that we need to update,
[99:13] and this should be actually really easy to do,
[99:16] just writing a script that walks the directory structure,
[99:21] skips any node modules folders, looks for a package.json,
[99:25] checks to see what the current resolution is,
[99:30] and then just sends out a prompt on the,
[99:34] on the terminal to say, this is out of date,
[99:42] do you wanna update it?
[99:43] Then gets everything up to date,
[99:45] and then once everything is up to date,
[99:46] saying these things need to be published,
[99:48] do you want to publish them?
[99:50] And that should be pretty quick and easy.
[99:54] The only thing that gets in the way of that right now
[99:57] is that if you have two-factor authentication
[99:59] turned on on NPM, it wants you to do
[100:01.80] two-factor authentication for every single publish,
[100:05.32] and that's kind of annoying.
[100:07.82] But, you know, that aside, having to copy and paste,
[100:10.68] copy and paste, copy and paste,
[100:11.76] I mean, I could get my two-factor key
[100:14.52] for NPM out of Authy.
[100:17.54] I could actually retrieve it,
[100:21.58] put it in a safe place
[100:27.12] where, basically put it in Apple Keychain,
[100:31.40] and then allow my program to,
[100:36.52] I could encrypt it with a passphrase,
[100:39.20] or a secret, or a salt, or whatever you wanna call it.
[100:42.12] And then I could let,
[100:44.06] I could let my program have access to it,
[100:49.48] ask me once, I think that's what I'll do.
[100:52.16] Oh, wait, but we still can't,
[100:54.02] then we have to still expect the output,
[100:59.16] so I'd have to learn how to publish with NPM
[101:02.08] a little bit more programmatically.
[101:03.26] But this is, even in the most secure case,
[101:06.28] this is completely doable.
[101:07.74] At worst, you have to sit and click copy and paste
[101:11.62] on a couple of two-factor codes.
[101:16.40] There's definitely an obsession with reinventing the wheel,
[101:23.26] but more importantly, there's an obsession
[101:25.90] with getting things wrong.
[101:27.44] So, I've got a video called We Hate Perfect Things.
[101:34.60] (soft music)
[101:37.02] Hey, and if you search YouTube, We Hate Perfect Things,
[101:46.98] it's the video that comes up, I'm quite surprised.
[101:51.70] Sweet.
[101:55.94] This is why there's so many frameworks.
[101:59.62] (soft music)
[102:02.04] Okay.
[102:10.48] All right, so now I've backtracked to
[102:28.76] this refactor.
[102:30.34] Let me see.
[102:32.96] I think I'm just too tired.
[102:34.40] I'm gonna have to pick this up maybe tomorrow.
[102:36.84] I might have to go to bed early tonight.
[102:38.84] Ah, this is what I was after.
[102:42.12] I was after the seed.
[102:44.74] I was after the seed.
[102:47.08] Right.
[102:47.92] (soft music)
[102:50.34] And this is the seed, by the way.
[103:12.54] Yes, I am going with it.
[103:17.80] 100% full send.
[103:19.48] Dash, phrase, seed.
[103:35.20] Oops, that's not what I wanted.
[103:39.82] Aw, you missed my beard.
[103:41.54] Aw, how sweet.
[103:44.16] (soft music)
[103:46.58] The zoomonic, the zikrit, and the zeed.
[103:51.10] That turned out really well.
[103:55.60] The gods are smiling upon us.
[103:57.62] I mean, this turns out to be really easy to remember.
[104:05.44] The zikrit is trezor.
[104:07.26] The zoomonic is zoo, zoo, zoo, zoo, zoo,
[104:09.96] with a wrong checksum word.
[104:12.72] The zeed, it's just, it's just too perfect.
[104:17.72] It's like it was meant to be.
[104:20.10] Okay.
[104:24.40] (soft music)
[104:29.70] the zikrit.
[104:30.70] (soft music)
[104:33.12] (soft music)
[104:35.54] (soft music)
[104:37.96] (soft music)
[104:40.38] (soft music)
[104:42.80] (soft music)
[104:45.22] (soft music)
[104:47.64] (soft music)
[104:50.06] (soft music)
[104:52.48] (soft music)
[104:54.90] (soft music)
[104:57.32] (soft music)
[104:59.74] (soft music)
[105:23.58] (soft music)
[105:27.00] (soft music)
[105:29.26] Okay, so.
[105:30.56] (soft music)
[105:32.98] (soft music)
[105:37.28] (soft music)
[105:44.22] (soft music)
[105:49.12] (soft music)
[105:54.00] (soft music)
[105:56.42] Let's see, what's the main selling point here?
[106:02.60] So we're going to rebrand this to dash HD.
[106:05.84] That's our thing.
[106:06.68] And I don't necessarily want to do all the things yet.
[106:12.84] So let's do this.
[106:16.60] (soft music)
[106:19.02] (soft music)
[106:22.00] (soft music)
[106:24.42] (soft music)
[106:26.84] Okay, dash HD.
[106:52.90] (soft music)
[106:55.32] Read me, glossary.
[107:02.72] (soft music)
[107:05.14] So we're going for the full rebrand here.
[107:09.60] (soft music)
[107:12.02] (soft music)
[107:14.44] Oh, whoops, these are not getter setters anymore.
[107:39.22] That should have been fixed a while back.
[107:41.82] (soft music)
[107:44.24] I'm not going to worry about that too much.
[107:59.84] So mainly what we want to do
[108:10.48] is we want to rebrand all of HDKey with dash HD.
[108:15.48] (soft music)
[108:22.22] (soft music)
[108:24.64] Okay.
[108:47.82] (soft music)
[108:50.24] (soft music)
[108:52.66] Bit 44 is actually kind of important
[109:07.36] to this whole discussion too.
[109:08.72] So I'm going to put that in the glossary one.
[109:10.84] (soft music)
[109:13.26] (soft music)
[109:15.68] See HD path.
[109:27.02] (soft music)
[109:29.44] Oh.
[109:43.16] (soft music)
[109:45.58] I just feel like I could work on this all month long
[109:52.62] and never be done.
[109:54.42] This is such a big can of worms.
[109:57.12] I was thinking of it.
[109:58.20] You know, there's just, well,
[110:02.02] I could work on this all month.
[110:05.06] I could.
[110:05.90] I could work on this all month.
[110:07.52] I will get these published by Monday.
[110:12.18] (soft music)
[110:13.18] But just the examples, the glossary,
[110:17.22] the really just refining this,
[110:21.46] this could be a huge,
[110:25.46] I mean, it already has been a huge project,
[110:27.10] but there's more here than meets the eye.
[110:32.10] (soft music)
[110:35.12] Okay.
[110:38.58] I don't know if I want to rename.
[110:41.18] (soft music)
[110:43.78] HD key, child key.
[110:45.88] I don't know if I want to rename any of that yet,
[110:51.74] but we do need derive and derive child.
[110:55.58] We need that documented.
[111:00.10] I think I'll get rid of the white private data.
[111:06.62] Okay. Anyway,
[111:08.26] the main thing here is,
[111:09.86] oops, that we're getting,
[111:14.10] we're getting this ready.
[111:16.10] Okay.
[111:16.94] (soft music)
[111:19.34] Oh, I did want to print out.
[111:31.78] (soft music)
[111:34.96] (keyboard clicking)
[111:37.96] I guess, yeah,
[111:45.88] this is kind of the best way to go about it
[111:47.92] is to say, have an account.
[111:52.00] You want to make sure you get the first one, right?
[111:54.68] And then if you can get, say the third one, right?
[111:57.16] And that kind of gets you around the off by one error
[112:01.98] or cause sometimes you get the first and second one, right?
[112:04.18] But the third one goes wrong.
[112:05.68] And so I think this would do that.
[112:09.12] Well generate a hardened key, a hardened key.
[112:12.40] Well, actually it doesn't matter.
[112:14.20] It really doesn't matter.
[112:15.04] It doesn't matter whether this number is one
[112:19.64] or two or 17,
[112:21.08] cause it's not actually incrementing to that number.
[112:25.32] So in theory,
[112:27.20] unless something is horridly, horridly wrong,
[112:30.24] these two are all that you need
[112:31.88] because whether this is 1000 in each of these spots
[112:36.48] or 10 or one or zero,
[112:38.82] it's the same amount of work.
[112:40.84] It's the same amount of work to produce this key
[112:46.70] as it is to produce this key.
[112:48.24] There are no additional rounds
[112:49.58] because the number of rounds is,
[112:51.38] this is the standard.
[112:53.86] It's 44.
[112:55.20] This is the coin type.
[112:56.58] That's round one.
[112:57.60] This is the account.
[112:58.66] That's round two.
[112:59.98] This is the purpose.
[113:02.94] That's round three.
[113:05.16] This is the index.
[113:06.40] That's round four.
[113:08.08] So if you've completed all four rounds successfully,
[113:11.86] it won't really matter whether you choose
[113:15.34] zero or 42 or whatever it is.
[113:20.02] It should be enough to say if two of them work,
[113:26.26] they all work.
[113:27.80] If two of them work, then none of them are hard-coded.
[113:30.54] Okay, anyway, with that said,
[113:34.16] let's go ahead and try this out.
[113:36.94] So I know that there is a CLI here.
[113:39.96] I think I already put it.
[113:40.98] Did I already put it in here?
[113:42.62] CLI, no.
[113:43.80] Okay, so we're gonna take what is currently called
[113:47.60] dash key, no, dash HD up here.
[113:51.44] This is gonna become CLI.
[113:55.68] And I am going to say
[113:58.66] we want to go from seed to,
[114:04.62] what is it that I'm trying to replicate in there?
[114:11.00] I think I just want to go to path.
[114:13.48] Oops.
[114:14.32] Yeah, I just want to be able to produce a path.
[114:25.96] (soft music)
[114:29.04] Hey, how's it going?
[114:31.00] What's up?
[114:31.84] Welcome.
[114:32.66] It's sleepy time.
[114:35.08] Okay, so let me go back in here.
[114:43.34] Everything is coming together,
[114:46.20] but it's just there are,
[114:48.04] there's even more pieces.
[114:49.56] It's not that there's more pieces than I realized.
[114:51.28] Well, there's twice as many pieces as I realized
[114:53.24] because there's each library and then there's each CLI.
[114:56.34] We need a command line tool for every library.
[114:58.64] And the pieces are interconnected
[115:01.96] and teasing them out and finding out
[115:03.72] which needs to be with what.
[115:06.56] That was its own thing.
[115:08.44] Refactoring so that there's consistent terminology
[115:11.48] between them.
[115:12.32] That's its own thing.
[115:13.84] So this is, you know, three or four phase approach.
[115:17.76] It's just, it's much, it's more,
[115:20.74] it's more massive than I realized.
[115:22.52] It's so much more massive than I realized.
[115:24.62] Okay, where's the path?
[115:28.48] There we go.
[115:33.42] Hmm.
[115:41.52] Is that it?
[115:46.92] (upbeat music)
[115:49.50], okay.
[116:15.30] (upbeat music)
[116:17.88] And actually the 44 may be one round.
[116:33.16] I have to double check on that.
[116:34.76] (upbeat music)
[116:37.34] (upbeat music)
[116:39.92] Okay.
[117:00.56] (upbeat music)
[117:03.18] (upbeat music)
[117:05.76] Zoo Monic, right.
[117:30.12] (upbeat music)
[117:32.70] (upbeat music)
[117:35.28] And then I could put this down.
[117:40.02] Every glossary needs to include the Zoo Monic.
[117:42.72] (upbeat music)
[117:45.30] Was it BIP 30, 39, BIP 44, Zoo Monic.
[117:55.10] BIP 30, 39, BIP 44, Zoo Monic, Zed.
[118:00.10] (upbeat music)
[118:06.64] (upbeat music)
[118:09.22] (sighs)
[118:30.64] (upbeat music)
[118:33.22] (upbeat music)
[118:35.80] Seed generated from the Zoo Monic
[118:55.12] to be used in documentation.
[119:01.42] Yes, it is dangerous to go alone.
[119:03.48] Take this.
[119:04.32] Did I make that reference recently?
[119:06.76] Or are we listening to Zelda?
[119:08.92] This is Terraria Enigma.
[119:11.68] We're not listening to Zelda right now.
[119:13.68] (upbeat music)
[119:16.26] Documentation, examples and test fixtures.
[119:26.82] (upbeat music)
[119:30.10] (upbeat music)
[119:32.68] There we go, all right.
[119:36.58] So we've got our Zed.
[119:38.34] (upbeat music)
[119:40.92] (upbeat music)
[119:43.50] (upbeat music)
[120:12.92] Let's see.
[120:13.76] I try to think of something clever to say when I join.
[120:16.88] Okay, dubs.
[120:17.82] Indeed, that's wonderful.
[120:20.24] I, you know, I won't get most of the references,
[120:22.64] but I'll get Nintendo references, at least half the time.
[120:25.44] Oh, is audio okay?
[120:29.98] All right.
[120:37.86] (upbeat music)
[120:40.44] Unfortunately, I don't know.
[120:46.58] How do you turn off continuity mode on your phone?
[120:49.50] 'Cause it wants to do it automatically all the time
[121:02.32] when I don't want it to do it.
[121:06.28] It's sitting here, burning up my battery.
[121:09.40] (upbeat music)
[121:24.86] What's a hum pod?
[121:32.12] Should I get one?
[121:35.92] Star Wars, I will get many of those.
[121:39.50] In video game lore, it depends.
[121:42.72] If it's Nintendo, yeah, it's an iPhone.
[121:46.60] It was in settings.
[121:47.70] I just had to search for continuity.
[121:49.50] (upbeat music)
[121:53.10] (keyboard clicking)
[121:56.10] HD key path.
[122:21.26] (keyboard clicking)
[122:23.20] HD key path.
[122:24.78] RIF address.
[122:28.80] HD wallets.
[122:46.04] (keyboard clicking)
[122:49.04] HD wallet and extended key paths.
[123:00.68] (keyboard clicking)
[123:05.64] (upbeat music)
[123:08.22] Let's see, an extended key paths.
[123:29.52] (keyboard clicking)
[123:32.52] (upbeat music)
[123:35.10] It's not really generate, but it's, what do we call it?
[123:50.28] When we, it's not, iterate's not the right word,
[123:52.40] but it's kind of like walk.
[123:53.72] Somewhere between walk and iterate.
[123:56.84] What's the word I'm looking for?
[123:58.44] (keyboard clicking)
[124:01.44] Probably is iterate.
[124:04.44] Okay.
[124:07.88] (keyboard clicking)
[124:10.88] (upbeat music)
[124:13.46] (keyboard clicking)
[124:16.46] (keyboard clicking)
[124:45.44] Take it from the top.
[124:46.56] Recapulation.
[124:47.92] Ah, dang it, I messed that up.
[124:50.34] So I was gonna go into a rap here.
[124:51.80] Take it from the top.
[124:53.76] Recapitulation.
[124:55.88] I'm gonna tell you a rap about Dash Nation.
[125:01.12] We're here to code.
[125:02.46] Crypto style.
[125:03.92] Gonna earn some Dash for a while.
[125:06.42] Spend it too.
[125:09.28] I'm not afraid.
[125:10.66] Living large and I get paid.
[125:12.64] I got an iPhone.
[125:14.48] That's my phone, fool.
[125:16.18] You other suckers out there, you just drool.
[125:22.40] Heard my friend K. Rool.
[125:24.64] He's in Super Mario Brothers Smash, you fool.
[125:28.20] All right.
[125:29.64] I'll stop embarrassing myself.
[125:31.40] Quite that much.
[125:32.34] What is the word I'm looking for?
[125:35.60] Let's just go with manage.
[125:42.16] (keyboard clicking)
[125:45.16] Okay, I think that's the right thing.
[125:50.12] (keyboard clicking)
[125:54.26] (soft music)
[125:56.68] (keyboard clicking)
[125:59.68] (keyboard clicking)
[126:03.68] (keyboard clicking)
[126:06.68] (keyboard clicking)
[126:09.68] (keyboard clicking)
[126:13.40] (keyboard clicking)
[126:16.40] Okay, let's just see.
[126:43.26] (keyboard clicking)
[126:46.26] All right, I'm just gonna take this,
[126:49.90] plop it down in the readme.
[126:51.20] Oh, that's not the one I wanted, actually.
[126:54.90] This readme.
[126:55.74] This is the readme that I wanted.
[126:58.34] Oh, well that was easy.
[127:05.42] Usage.
[127:11.58] (keyboard clicking)
[127:14.58] Okay, so install.
[127:29.50] Node, bun, and bundlers.
[127:40.14] (keyboard clicking)
[127:43.14] Browser.
[127:45.32] Always the browser.
[127:49.94] Oh, what was I looking at?
[127:57.32] Dash keys, readme, HTML.
[128:01.42] (keyboard clicking)
[128:05.90] (keyboard clicking)
[128:08.90] Dash hive, dash phrase, dash phrase dot JS.
[128:18.76] There we go.
[128:20.90] Oh, whoops.
[128:28.14] That also led me to see that I have an error here.
[128:33.14] (keyboard clicking)
[128:36.14] Oh no, I don't.
[128:40.02] No, I put an error here.
[128:42.86] So this is simply the module is dash phrase,
[128:45.94] and then here again, the module is dash keys.
[128:50.56] (keyboard clicking)
[128:53.56] (keyboard clicking)
[129:02.68] (keyboard clicking)
[129:05.68] Dash phrase at one point X.
[129:09.06] Let me just make sure that works.
[129:12.50] I think it does.
[129:14.06] Yeah, it does, good.
[129:15.06] And then dash keys at,
[129:20.96] I think this is gonna be three point X, maybe?
[129:25.42] No, this is gonna be dash HD.
[129:30.54] (keyboard clicking)
[129:33.54] Maybe I shouldn't go into this bit of it.
[129:41.16] (keyboard clicking)
[129:44.16] (keyboard clicking)
[129:47.16] Oh, look, there's a couple of goof-offs here.
[130:10.62] (keyboard clicking)
[130:13.62] (keyboard clicking)
[130:16.62] Okay, I'm actually convinced that I ought to,
[130:23.36] okay, let me do this.
[130:33.72] (keyboard clicking)
[130:43.18] All right, that's good.
[130:44.02] Git checkout, read me again.
[130:47.52] Let's see, git diff read me.
[130:49.04] Yeah.
[130:52.64] (keyboard clicking)
[130:55.64] (keyboard clicking)
[130:58.64] Wait, before I go into that,
[131:23.10] let me just fix a couple of these,
[131:25.12] a few more of these things.
[131:26.46] So, there is,
[131:30.46] await if our XPriv equals,
[131:38.50] await HDT, git private extended key.
[131:48.02] (keyboard clicking)
[131:51.02] (keyboard clicking)
[131:54.02] (sighing)
[132:07.52] XPub.
[132:08.36] (keyboard clicking)
[132:13.38] (keyboard clicking)
[132:16.38] XPub equals await.
[132:27.40] We're gonna change all these examples a little later.
[132:31.98] Right now, I just wanna get 'em sorted out
[132:34.78] so they actually work.
[132:40.94] That's gonna be XPriv.
[132:44.60] I probably need to go for dinner soon.
[132:47.18] This is, oh man, this is so much more bigger,
[132:53.72] much more bigger than I was thinking at the time.
[133:07.40] All right, now we can relive that moment forever.
[133:11.56] What?
[133:12.40] (faintly speaking)
[133:17.10] (keyboard clicking)
[133:33.12] (faintly speaking)
[133:36.04] (laughing)
[133:42.58] Thanks for that.
[133:53.72] (laughing)
[133:59.74] Uh-oh.
[134:00.84] (laughing)
[134:02.86] Someone discovered the clip feature.
[134:07.54] Uh, I put that in the Discord.
[134:17.10] It's awesome.
[134:19.30] Dubs is my main man.
[134:21.86] (laughing)
[134:24.62] All right.
[134:25.46] Do we have any other stuff where,
[134:30.96] oops.
[134:32.12] (keyboard clicking)
[134:35.96] (faintly speaking)
[134:38.88] (keyboard clicking)
[134:41.88] Let's see, do we have any docs?
[135:08.42] (keyboard clicking)
[135:11.42] See if that goes in cleanly.
[135:14.08] And it does, huzzah.
[135:15.18] (keyboard clicking)
[135:19.40] Okay, I'm gonna go check over here real quick.
[135:28.78] Ref, async, compat.
[135:31.12] (keyboard clicking)
[135:38.22] Boom.
[135:39.06] There we go.
[135:50.62] Excellent sidekick.
[135:54.70] Especially, you know, because it's dangerous.
[135:58.14] And I don't have to go alone.
[135:59.70] Because of you.
[136:02.02] Because of you, I don't have to go alone.
[136:04.60] I don't.
[136:07.86] (keyboard clicking)
[136:10.14] It's because of you, Dubs.
[136:11.44] It's all because of you.
[136:13.86] Sometimes, sometimes I wanna go alone.
[136:23.22] But, I don't have to anymore.
[136:27.02] I don't have to.
[136:29.30] Do I get an Emmy or an Oscar or anything?
[136:34.90] I think that was a pretty good performance.
[136:37.02] (keyboard clicking)
[136:40.54] No.
[136:41.38] (keyboard clicking)
[136:44.38] (keyboard clicking)
[136:47.38] (keyboard clicking)
[137:16.82] HD key.
[137:18.02] Dash HD.
[137:20.58] (keyboard clicking)
[137:24.52] Okay, make that change one more time.
[137:32.62] Oh, you know what?
[137:37.42] Hold on.
[137:38.24] No, wait, there's one more.
[137:39.08] There's one more.
[137:39.90] There's one more.
[137:41.10] There's one more.
[137:41.94] One more change I need to make.
[137:45.70] What is the consensus about tomorrow?
[137:48.02] What am I doing?
[137:51.62] Give me one second here.
[137:52.96] I'm gonna fix.
[137:55.50] There we go.
[138:02.14] There was a couple of other issues
[138:02.96] that I wanted to fix in here.
[138:04.12] While I'm at it.
[138:07.50] Because, where were they?
[138:09.74] Oh, is this the stuff about the getter setter?
[138:12.12] (keyboard clicking)
[138:15.12] (keyboard clicking)
[138:18.12] (keyboard clicking)
[138:21.12] (keyboard clicking)
[138:24.12] (keyboard clicking)
[138:27.12] (keyboard clicking)
[138:30.12] (keyboard clicking)
[138:57.84] That probably should have come much sooner.
[139:00.38] (sighs)
[139:04.32] Okay, yeah.
[139:05.14] That, there was just that small change
[139:06.20] that I wanted to get in there.
[139:08.00] And that was.
[139:09.02] (keyboard clicking)
[139:13.82] Get, check out.
[139:21.78] Ref, async, compare, Gary, base, dash, I.
[139:26.12] (keyboard clicking)
[139:29.12] Get, check out, ref, dash, keys.
[139:36.40] Okay.
[139:37.24] (keyboard clicking)
[139:40.82] Oops.
[139:41.66] (keyboard clicking)
[139:44.66] (keyboard clicking)
[139:47.66] Okay.
[140:05.70] Now, I'm finally ready to dig in here.
[140:09.40] (keyboard clicking)
[140:12.40] (keyboard clicking)
[140:15.40] Okay.
[140:23.24] Do these replacements.
[140:24.88] Do these replacements.
[140:29.70] All these still actually make sense.
[140:35.56] That's fine.
[140:36.48] I don't know that all these references
[140:41.56] are really necessary.
[140:42.68] I think we're gonna have those in here anyway.
[140:46.68] So, I'll drop them out later though.
[140:50.52] Once we get the glossary in here.
[140:52.62] That's why I'll drop those out.
[140:53.52] Okay.
[140:54.36] Okay, git commits.
[140:58.20] Rebrand.
[141:00.80] Okay, so now,
[141:02.06] we need to package.json and all the other things too.
[141:07.64] (keyboard clicking)
[141:10.64] Hdkey, whoops.
[141:16.46] Dash hd.
[141:20.28] Oh, whoops.
[141:23.32] That one's still gonna be the same for right now.
[141:26.10] Well.
[141:31.68] Yeah, all right.
[141:35.80] (keyboard clicking)
[141:37.84] Yes.
[141:38.68] We're actually gonna move this file up here.
[141:43.28] All right, and let's go ahead and say,
[141:50.68] it's gonna be, let's see, we got dash hd,
[141:55.92] the crypto, what's it?
[141:57.72] Okay.
[142:04.28] We need to replace this with dash hive.
[142:06.60] Whoops, the other way around.
[142:15.52] Dash hive.
[142:21.68] Oh, that's weird.
[142:27.40] File zero, I probably put that in, but I don't remember.
[142:31.44] (keyboard clicking)
[142:34.44] Ugh, that's a terrible description.
[142:40.86] Let me see, what would I want the description to be?
[142:45.92] Actually, I don't need to worry about that right now,
[142:48.36] 'cause right now all I need to do
[142:50.00] is do doc rebrand to dash hd.js.
[142:56.64] (keyboard clicking)
[142:59.64] What?
[143:10.44] Ugh.
[143:15.72] Okay, so hd key.
[143:23.48] I don't think we have any links to this one anymore.
[143:27.16] Great, okay, so that's that.
[143:31.60] And then we are going to smash a little here.
[143:37.36] (keyboard clicking)
[143:45.32] (soft music)
[143:47.74] Let's see.
[143:56.04] Change log.
[144:01.90] 3.0.0.
[144:12.96] 2023.02.03.
[144:16.28] Hey, what's up, VexFree?
[144:17.24] Sorry I didn't see you there.
[144:18.60] Just kind of in my own little world, you know?
[144:20.90] Let me catch up on comments here.
[144:24.12] Oh.
[144:27.68] Sounds smart, references sound smart.
[144:34.76] So I was saying I'm gonna nix the references
[144:37.96] because I'm gonna have a glossary,
[144:40.92] and so things that I need to link to
[144:42.88] will be linked to from the glossary.
[144:45.24] All right, thanks for stopping by.
[144:46.94] Have a good one.
[144:47.78] Oh, what?
[144:53.02] But wait, there's more.
[144:54.96] (laughing)
[144:57.22] Oh.
[145:05.48] Nice.
[145:10.74] I'm gonna, I wanna see what I actually
[145:14.18] look and sound like there.
[145:15.52] Okay.
[145:19.66] A brand to dash HD.
[145:25.02] .js.
[145:27.70] Complete refactor to async await.
[145:33.60] To web crypto noble crypto
[145:40.60] and async await dash tools.
[145:44.72] API redesign for consistency.
[146:10.88] With dash tools.
[146:12.76] There we go.
[146:23.12] That's what that will be.
[146:25.84] Okay, let's see what the package.json.
[146:28.76] Yeah, what?
[146:29.58] Let me see what I called this.
[146:35.10] (upbeat music)
[146:37.68] What did I call dash keys?
[146:50.20] I also need a consistent naming structure here.
[146:54.30] Validate, that seems okay.
[146:57.90] So it's the first part of the title here.
[146:59.96] (upbeat music)
[147:02.54] And I think that what this might need to do
[147:08.66] is go from the, I don't know if it should go from,
[147:13.30] maybe it should go from the read me to the description.
[147:15.86] But there should be a way to keep those things in sync.
[147:18.38] (upbeat music)
[147:29.66] And it maybe should be all caps dash code,
[147:32.78] part of dash tools.
[147:36.86] (upbeat music)
[147:39.44] All right.
[147:57.42] (upbeat music)
[148:00.00] So we're gonna have that.
[148:04.14] Oh, this needs to be .js at the end.
[148:08.26] All of these need to be .js at the end
[148:10.06] because one day in my dream of dreams,
[148:14.02] we will actually have this written in Go as well.
[148:18.46] (upbeat music)
[148:21.04] All right.
[148:21.88] (upbeat music)
[148:24.46] Do we need dash keys for dash HD?
[148:29.64] Yes, we do need dash keys for dash HD.
[148:34.20] So, yes we do, we absolutely do.
[148:40.48] (upbeat music)
[148:46.18] (keyboard clicking)
[148:49.18] We don't need dash keys for,
[148:55.66] I think where dash keys is at 0.9.
[149:01.28] So I'm just gonna not give it a designation yet.
[149:07.74] Yeah, we'll give it a designation at 0.9.
[149:14.34] We'll fix that.
[149:15.34] (upbeat music)
[149:17.34] Later on we need to dash HD at three.
[149:20.94] I like to put this in there because this is the reason,
[149:26.98] 'cause people copy and paste from your readme.
[149:28.74] When people go and make tutorials online,
[149:31.30] they'll just put the whatever
[149:32.50] without the at sign for the version.
[149:34.06] But if you make a breaking change to the version,
[149:37.00] it's nice to have that in there.
[149:39.34] So I like to put that in the readme.
[149:41.10] (upbeat music)
[149:43.68] (keyboard clicking)
[149:45.34] Okay.
[149:46.18] All right, did I hit everything here?
[149:54.20] Okay, so keywords, dash, dash.
[149:59.20] We could keep BIP 32, I suppose.
[150:05.00] BIP 44, kind of want those to be at the end.
[150:11.10] (keyboard clicking)
[150:14.50] HD, wallet, keys, path.
[150:18.86] (keyboard clicking)
[150:29.14] (upbeat music)
[150:31.72] (keyboard clicking)
[150:34.72] (upbeat music)
[150:37.30] (keyboard clicking)
[150:40.30] (upbeat music)
[150:42.88] Okay, so here we are.
[151:11.04] Updated that, updated all of these dev dependencies.
[151:15.92] I don't know if we need the biggie.
[151:18.36] We'll probably get rid of biggie,
[151:19.40] but I think it's just for the tests.
[151:21.72] And I think Ecurve is just using two separate libraries
[151:25.88] to validate that they both work or something like that.
[151:29.88] Oh, and then another thing that needs to be
[151:37.92] in the read me here is gonna be npm install.
[151:42.02] So at dash incubator/secp256k1@1.x.
[151:48.52] Wait, do we need that for this?
[152:05.38] Yeah, we do, we absolutely do.
[152:06.96] (keyboard clicking)
[152:09.96] And really, you don't have to have dash phrase.
[152:30.00] It's not a hard dependency.
[152:31.04] So I'm actually gonna take that out.
[152:32.84] (keyboard clicking)
[152:35.84] (upbeat music)
[152:38.42] (keyboard clicking)
[152:41.42] (upbeat music)
[152:44.66] (keyboard clicking)
[152:47.66] (upbeat music)
[152:50.24] (keyboard clicking)
[153:20.08] Okay, are we on node 18 right now?
[153:22.40] All right.
[153:33.64] Those ads are referencing version numbers.
[153:36.80] Yes, that's correct.
[153:38.12] Do those keywords help index or make it search easier?
[153:40.72] Yes.
[153:41.78] So yeah, on npm.
[153:43.68] So when this gets published,
[153:45.84] it's searched by that on npm.
[153:49.12] All right, package lock.
[153:51.62] Good, everything is changed.
[153:55.20] This is good.
[153:56.04] Rebrand.
[154:04.68] Oh, and do we need to do anything inside of here?
[154:07.12] Dash HD.
[154:10.12] (upbeat music)
[154:12.70] (keyboard clicking)
[154:16.54] (keyboard clicking)
[154:44.18] Just checking out here.
[154:46.30] Okay.
[154:51.98] So this is how the code is renamed.
[154:56.30] (keyboard clicking)
[154:59.30] (upbeat music)
[155:01.88] (keyboard clicking)
[155:04.88] (upbeat music)
[155:08.12] (keyboard clicking)
[155:11.12] Ah, let's see, what do I?
[155:34.32] Oh, I still have unstaged changes.
[155:37.00] (keyboard clicking)
[155:40.00] Sure.
[155:43.88] Update change log.
[155:47.52] (keyboard clicking)
[155:50.52] What?
[155:56.40] Oh, oops.
[156:02.52] That's not what I wanted to do.
[156:04.92] (keyboard clicking)
[156:07.92] Cool, so.
[156:22.76] (upbeat music)
[156:33.82] Let me see what I've got left to do here.
[156:36.68] That's not what I meant to do, but that's cool.
[156:45.58] Boom, boom, boom.
[156:53.76] This is Paper Mario, Thousand Year Door.
[156:56.10] Okay, let me check comments here.
[157:02.10] I can kind of read code
[157:03.18] and understand what its purpose is sometimes.
[157:06.22] Just need to ask, but yeah, keep asking.
[157:08.94] Always felt intimidated in the past
[157:10.30] to ask anything out of fear.
[157:12.02] I don't like humiliation.
[157:13.94] Well, the good news is A, I'll humiliate you
[157:16.66] and help you realize your fears
[157:18.30] so that you can come to grips with them
[157:21.56] and understand how petty they are.
[157:24.24] And number two is that, you know, it's not a big channel.
[157:28.06] There's not a hundred million people.
[157:29.22] So, you know, you're pretty free to be open and have fun.
[157:32.96] Okay.
[157:36.90] Updates, we got a bunch of that.
[157:41.86] So, we've got the glossary, still needs to get done.
[157:46.58] We've got the CLI.
[157:49.30] So, we still have a fair bit here.
[157:55.50] But I think, okay, before I go to the CLI,
[157:57.58] I should just get this finished.
[158:00.50] And I think I kind of know what I need to do
[158:02.66] to do that at least.
[158:26.74] I'm gonna have to look and see what this looks like
[158:29.82] in the README.
[158:30.66] (upbeat music)
[158:33.24] (upbeat music)
[158:35.82], (upbeat music)
[158:40.82], (upbeat music)
[158:45.82], (upbeat music)
[158:50.82] (upbeat music)
[158:53.40] Oops, meant to do, I used to do TXT
[159:18.50] until I found out that that didn't work.
[159:21.14] And now I do.
[159:22.14] Okay, now let me add these.
[159:31.18] (upbeat music)
[159:33.76] You know, we could bring those in by at least,
[160:00.38] I mean, it looks like we could bring those in quite a bit.
[160:02.62] Let me see about that.
[160:03.70] (upbeat music)
[160:07.30] (upbeat music)
[160:09.88] And then some of these will start to fit on the same line,
[160:32.70] which would be nice.
[160:33.66] (upbeat music)
[160:37.08] We could maybe even, you know,
[160:41.44] bring this all out to the same place.
[160:45.30] Sometimes, sometimes this looks nice too.
[160:50.28] I'm gonna try that out.
[160:57.76] Just see what it looks like with that alignment.
[161:04.52] (upbeat music)
[161:07.10] There we go.
[161:12.16] Okay.
[161:15.94] And then I think I'm gonna go and,
[161:22.94] let's see.
[161:32.32] The next piece that we'll have here.
[161:35.74] I think I actually do prefer
[161:50.04] having them line up correctly on both.
[161:54.04] Y'all tell me what you think.
[161:55.20] By the way, here's a link to this thing.
[162:01.88] Yeah, but does it look better when these are lined up?
[162:06.08] Should I line those back up again?
[162:08.28] If anybody wants to make that PR, feel free.
[162:09.92] You can even, well, right now would be a bad time to do it.
[162:14.36] I was gonna say, you can even make a little bit of dash
[162:17.16] yourself.
[162:18.04] All right, so that's good.
[162:21.54] Oh, whoops, one thing that I probably got wrong.
[162:29.96] (upbeat music)
[162:32.54] So this should be dash HD like that.
[162:40.54] (upbeat music)
[162:43.12], okay.
[162:53.96] (upbeat music)
[162:56.54] Okay.
[163:13.16] (upbeat music)
[163:22.56] I wonder if there's a difference between,
[163:24.68] is this to say master seed?
[163:28.44] I think master seed conveys a lot of meaning.
[163:30.84] (upbeat music)
[163:33.42] (upbeat music)
[163:36.00] (upbeat music)
[163:38.58] (upbeat music)
[163:41.16] (upbeat music)
[163:43.74] Hmm.
[164:05.32] (upbeat music)
[164:07.90] (upbeat music)
[164:10.48] I wonder what this process is called.
[164:20.66] (upbeat music)
[164:23.24] (upbeat music)
[164:25.82] What are versions supposed to be?
[164:40.76] (upbeat music)
[164:44.28] (upbeat music)
[164:46.86] I don't know that I actually use these anywhere.
[164:59.34] Yeah, I think I'm gonna get rid of that.
[165:05.14] (upbeat music)
[165:07.72] (upbeat music)
[165:10.30] (upbeat music)
[165:12.88] (upbeat music)
[165:15.46] (upbeat music)
[165:42.66] So for example,
[165:44.18] I want this to be not from master seed,
[165:48.46] but rather we could have a set seed
[165:51.66] and then the set seed,
[165:54.66] and this would probably be
[165:58.86] with HD key like this.
[166:03.98] And that's not gonna take versions.
[166:12.82] And it is gonna do the calculations that it needs to do.
[166:17.58] And then,
[166:20.10] ooh.
[166:23.42] (upbeat music)
[166:28.80] I do not like a create function.
[166:39.28] (upbeat music)
[166:41.86] Okay, here's where we have a problem
[166:48.36] where it might not be what I want it to be.
[166:51.16] So I don't, rule of thumb,
[166:53.08] create function should not be async.
[166:54.84] Create function should be synchronous.
[166:59.84] Now we can have an init function,
[167:02.56] but this does seem like,
[167:06.34] (upbeat music)
[167:08.92] Okay, set seed.
[167:25.36] Version's already set.
[167:27.78] We're not gonna do a create on this.
[167:30.12] (upbeat music)
[167:32.70] And we don't need to return anything
[167:43.80] 'cause I don't like chaining.
[167:46.48] I don't think it's a good pattern.
[167:49.50] (upbeat music)
[167:52.08], hmm. (upbeat music)
[168:20.16] Set seed doesn't even feel quite right.
[168:22.68] Because it's asynchronous,
[168:23.84] it needs to be something a little more clear
[168:27.16] as to what it is.
[168:28.72] (upbeat music)
[168:31.30] Wait, I'm a little confused.
[168:41.20] Is hardened.
[168:44.74] Oh, this is derive key.
[168:46.16] Okay, that makes sense.
[168:47.36] (upbeat music)
[168:49.94] (keyboard clicking)
[168:52.94] Seed bytes.
[169:13.14] Okay, I think I got a handle on what I'd like this to be.
[169:15.88] (upbeat music)
[169:19.22] (keyboard clicking)
[169:21.42] Oh, so back to the alignment issue.
[169:23.30] Would it be just as good or not as good
[169:31.42] to have them aligned?
[169:34.40] So basically they're off by three or four characters.
[169:37.32] Looks like one, two, three.
[169:41.44] So if we just moved all of these over,
[169:48.54] so these are all indented.
[169:50.54] Let me just do it to kind of show what I'm talking about.
[169:53.98] And so if we just take all of these,
[169:57.74] you know, one, two, three.
[169:59.32] Yeah.
[170:02.50] And let's just go boop, boop, boop, boop, boop, boop.
[170:06.82] (keyboard clicking)
[170:10.26] (upbeat music)
[170:12.84] (keyboard clicking)
[170:15.84] (upbeat music)
[170:18.42] (keyboard clicking)
[170:21.42] (upbeat music)
[170:24.00] (keyboard clicking)
[170:51.84] All right, so here we have set seed and it's async.
[170:56.00] (keyboard clicking)
[170:59.00] So from seed.
[171:21.44] So HD key is gonna have set seed here.
[171:26.44] (keyboard clicking)
[171:33.22] (upbeat music)
[171:35.80] I'm not gonna pass in versions there.
[171:54.72] Okay, I think this is appropriate.
[171:58.74] (keyboard clicking)
[172:01.74] (upbeat music)
[172:04.32] All right.
[172:30.92] (keyboard clicking)
[172:31.98] So generally speaking, I don't like from methods.
[172:36.34] Yeah, if a from, 'cause with a from method,
[172:45.52] the only reason it makes sense to do the from method
[172:51.10] is because it skips calling create.
[172:53.82] That's it.
[172:58.60] Because you're still calling create.
[173:00.44] You're still doing all the same stuff.
[173:05.42] I mean, look at this.
[173:06.26] Everything from there,
[173:10.12] and then all of this stuff is just the same
[173:14.34] as if it had called create.
[173:15.26] In fact, it's kind of funny.
[173:17.72] So does this even use any?
[173:22.78] Okay, so it does use versions after that,
[173:25.60] but this is the same.
[173:27.22] Yeah, this is the same as if we had just put it inside of,
[173:30.88] you know, and had a set extended key.
[173:38.34] And the other thing, though,
[173:39.54] is that this one actually kind of makes sense,
[173:42.14] if I'm not mistaken.
[173:43.70] Let's see, decode base 58.
[173:45.88] No, it doesn't.
[173:46.72] So we could put out the outside and maybe call it parse.
[173:56.26] Parse extended key.
[173:57.78] Parse seed is kind of weird,
[173:59.78] but you're doing something else.
[174:03.18] I don't really know what that's called.
[174:05.14] But I kind of want to pull these apart
[174:15.62] in the sense that I don't,
[174:18.86] are you ever really doing something with a key
[174:24.08] without knowing whether it's a public or private key?
[174:29.08] 'Cause it seems like what this ought to be
[174:35.32] is probably set X priv.
[174:38.36] And then there is a more private method, set X key,
[174:45.92] which has a lot of this in it.
[174:51.74] But it seems like there probably ought to be
[174:54.38] a set X priv and a set X pub.
[175:00.66] And this becomes a set X key.
[175:11.84] And then when we call this or this,
[175:18.02] we just check X pub,
[175:21.50] check X priv,
[175:31.20] and then throw if it's not the right type of key,
[175:33.00] because I don't think that you're going,
[175:38.00] it just doesn't seem like a really valid use case to me
[175:41.68] to not know whether you have a private or a public key.
[175:46.06] Even though the parsing logic
[175:47.46] is pretty much the same for them,
[175:48.60] and that's why this method would go underneath.
[175:51.28] As far as the API goes,
[175:55.38] it just doesn't seem to make sense to me
[175:58.14] that we would expose just a generic set operation.
[176:04.14] We would expose just a generic set operation.
[176:10.14] (dramatic music)
[176:12.90] (keyboard clacking)
[176:15.90] (dramatic music)
[176:43.94] So this is part of what the API change on this is gonna be.
[176:46.94] And then as far as this skip verification goes,
[176:57.50] I think the difference between the two
[177:11.34] was that setPublicKey calls normalize.
[177:14.88] And I think that it's fair,
[177:19.76] oh, it's time for me to go for dinner.
[177:22.88] So we'll have to continue these musings later.
[177:27.38] Yes?
[177:31.06] Okay, I'm coming, love you, bye.
[177:35.50] All right, time for me to go to dinner.
[177:40.98] I'm out.
[177:41.82] But yeah, we'll figure out what this API should be
[177:47.34] and we'll publish that.
[177:48.54] We're not gonna worry about the full glossary yet.
[177:51.98] That's gonna be put on the back burner.
[177:53.48] We're not gonna worry about the CLI yet.
[177:55.02] That's gonna be put on the back burner.
[177:56.50] We're just going to get the API
[177:58.54] to feel a little bit more dash tools-ish.
[178:01.94] So, oh, how do I?
[178:08.46] I can't reorder them.
[178:09.58] Oh no, I thought I could reorder them from out here.
[178:13.04] So CLI and glossary.
[178:14.84] So the rebrand is pretty much complete.
[178:36.90] This is still to be done.
[178:39.24] Okay, I'll see y'all later.
[178:49.30] Thanks for joining in.
[178:50.14] Really appreciated the conversation, Dubs.
[178:52.96] And explodinu and Vexfreeze, and I'll catch you later.
[178:57.96] Adios.