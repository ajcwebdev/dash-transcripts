---
showLink: "https://www.youtube.com/watch?v=oodJpjkWrtE"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Code Hangout: Next-Gen DASH Tools #12: Now on to DashHD.js v1... and Beyond!"
publishDate: "2023-02-03"
coverImage: "https://i.ytimg.com/vi/oodJpjkWrtE/maxresdefault.jpg"
---

## Episode Description

The stream focuses on refactoring and updating the Dash HD wallet library, switching to async functions and improving browser compatibility.

## Episode Summary

In this lengthy coding session, the developer works on refactoring the Dash HD wallet library. Key tasks include switching to async functions, improving browser compatibility, updating dependencies, and streamlining the codebase. The developer encounters and resolves various issues related to TypeScript, npm, and cross-version compatibility. By the end, significant progress is made towards modernizing the library and preparing it for integration with other Dash-related packages.

## Chapters

00:00 - Introduction and Initial Code Review

The stream begins with the developer reviewing the current state of the Dash HD wallet library code. They discuss the goals for the refactoring process, including making functions async and improving browser compatibility. The developer also examines the existing test suite and considers how to update it for the new changes.

36:40 - Refactoring to Async Functions

The developer starts the process of converting synchronous functions to async. They work through various parts of the codebase, updating function signatures and adding await keywords where necessary. This process reveals some unexpected challenges, particularly with crypto functions that need to be handled differently in browser environments.

73:51 - Addressing Compatibility Issues

As the refactoring progresses, the developer encounters compatibility issues between different versions of Node.js and browser environments. They spend time adjusting the code to work across these different contexts, carefully considering how to maintain backward compatibility while also modernizing the library.

161:07 - Updating Dependencies and Package Configuration

The developer takes time to update the project's dependencies and adjust the package.json configuration. This includes removing outdated packages, updating testing frameworks, and ensuring that the project can build and run tests in various environments. They also discuss the challenges of maintaining compatibility with older Node.js versions.

240:00 - Resolving TypeScript and Import Issues

A significant portion of time is spent dealing with TypeScript-related issues, particularly around importing types and ensuring that the library's types are correctly exposed to consumers. The developer expresses frustration with some aspects of TypeScript and considers potential workarounds.

300:09 - Final Refactoring and Documentation Updates

In the closing segment, the developer works on finalizing the refactoring process, including renaming some methods for consistency and clarity. They also begin updating the README and other documentation to reflect the changes made to the library. The stream concludes with the developer discussing next steps and expressing satisfaction with the progress made.

380:50 - Conclusion and Next Steps

The developer wraps up the stream, summarizing the work completed and outlining the remaining tasks for the Dash HD wallet library and related projects. They express optimism about the state of the library and discuss plans for future development sessions.

## Transcript

[00:00] [ Silence ]
[00:26] [ Laughter ]
[00:28] [ Silence ]
[00:38] [ Silence ]
[00:48] [ Silence ]
[00:58] [ Silence ]
[01:08] [ Silence ]
[01:18] [ Silence ]
[01:28] [ Silence ]
[01:38] [ Silence ]
[01:48] [ Silence ]
[01:58] [ Silence ]
[02:08] [ Silence ]
[02:18] [ Silence ]
[02:28] [ Silence ]
[02:38] [ Silence ]
[02:48] [ Silence ]
[02:58] [ Silence ]
[03:08] [ Silence ]
[03:18] [ Silence ]
[03:28] [ Silence ]
[03:38] [ Silence ]
[03:48] [ Silence ]
[03:58] [ Silence ]
[04:08] [ Silence ]
[04:18] [ Silence ]
[04:28] [ Silence ]
[04:38] [ Silence ]
[04:48] [ Silence ]
[04:58] [ Silence ]
[05:08] [ Silence ]
[05:18] [ Silence ]
[05:28] [ Silence ]
[05:38] [ Silence ]
[05:48] [ Silence ]
[05:58] [ Silence ]
[06:08] [ Silence ]
[06:18] [ Silence ]
[06:28] [ Silence ]
[06:38] [ Silence ]
[06:48] [ Silence ]
[06:58] [ Silence ]
[07:08] [ Silence ]
[07:18] [ Silence ]
[07:28] [ Silence ]
[07:38] [ Silence ]
[07:48] [ Silence ]
[07:58] [ Silence ]
[08:08] [ Silence ]
[08:18] [ Silence ]
[08:28] [ Silence ]
[08:38] [ Silence ]
[08:48] [ Silence ]
[08:58] [ Silence ]
[09:08] [ Silence ]
[09:18] [ Silence ]
[09:28] [ Silence ]
[09:38] [ Silence ]
[09:48] [ Silence ]
[09:58] [ Silence ]
[10:08] [ Silence ]
[10:18] [ Silence ]
[10:28] [ Silence ]
[10:38] [ Silence ]
[10:48] [ Silence ]
[10:58] [ Silence ]
[11:08] [ Silence ]
[11:18] [ Silence ]
[11:28] [ Silence ]
[11:38] [ Silence ]
[11:48] [ Silence ]
[11:58] [ Silence ]
[12:08] [ Silence ]
[12:18] [ Silence ]
[12:28] [ Silence ]
[12:38] [ Silence ]
[12:48] [ Silence ]
[12:58] [ Silence ]
[13:08] [ Silence ]
[13:18] [ Silence ]
[13:28] [ Silence ]
[13:38] [ Silence ]
[13:48] [ Silence ]
[13:58] [ Silence ]
[14:08] [ Silence ]
[14:18] [ Silence ]
[14:28] [ Silence ]
[14:38] [ Silence ]
[14:48] [ Silence ]
[14:58] [ Silence ]
[15:08] [ Silence ]
[15:18] [ Silence ]
[15:28] [ Silence ]
[15:38] [ Silence ]
[15:48] [ Silence ]
[15:58] [ Silence ]
[16:08] [ Silence ]
[16:18] [ Silence ]
[16:28] [ Silence ]
[16:38] [ Silence ]
[16:48] [ Silence ]
[16:58] [ Silence ]
[17:08] [ Silence ]
[17:18] [ Silence ]
[17:28] [ Silence ]
[17:38] [ Silence ]
[17:48] [ Silence ]
[17:58] [ Silence ]
[18:08] [ Silence ]
[18:18] [ Silence ]
[18:28] [ Silence ]
[18:38] [ Silence ]
[18:48] [ Silence ]
[18:58] [ Silence ]
[19:08] [ Silence ]
[19:18] [ Silence ]
[19:28] [ Silence ]
[19:38] [ Silence ]
[19:48] [ Silence ]
[19:58] [ Silence ]
[20:08] [ Silence ]
[20:18] [ Silence ]
[20:28] [ Silence ]
[20:38] [ Silence ]
[20:48] [ Silence ]
[20:58] [ Silence ]
[21:08] [ Silence ]
[21:18] [ Silence ]
[21:28] [ Silence ]
[21:38] [ Silence ]
[21:48] [ Silence ]
[21:58] [ Silence ]
[22:08] [ Silence ]
[22:18] [ Silence ]
[22:28] [ Silence ]
[22:38] [ Silence ]
[22:48] [ Silence ]
[22:58] [ Silence ]
[23:08] [ Silence ]
[23:18] [ Silence ]
[23:28] [ Silence ]
[23:38] [ Silence ]
[23:48] [ Silence ]
[23:58] [ Silence ]
[24:08] [ Silence ]
[24:18] [ Silence ]
[24:28] [ Silence ]
[24:38] [ Silence ]
[24:48] [ Silence ]
[24:58] [ Silence ]
[25:08] [ Silence ]
[25:18] [ Silence ]
[25:28] [ Silence ]
[25:38] [ Silence ]
[25:48] [ Silence ]
[25:58] [ Silence ]
[26:08] [ Silence ]
[26:18] [ Silence ]
[26:28] [ Silence ]
[26:38] [ Silence ]
[26:48] [ Silence ]
[26:58] [ Silence ]
[27:16] [ Silence ]
[27:26] [ Silence ]
[27:36] [ Silence ]
[27:46] [ Silence ]
[27:56] [ Silence ]
[28:06] [ Silence ]
[28:16] [ Silence ]
[28:26] [ Silence ]
[28:36] [ Silence ]
[28:46] [ Silence ]
[28:56] [ Silence ]
[29:06] [ Silence ]
[29:16] [ Silence ]
[29:26] [ Silence ]
[29:36] [ Silence ]
[29:46] [ Silence ]
[29:56] [ Silence ]
[30:06] [ Silence ]
[30:16] [ Silence ]
[30:26] [ Silence ]
[30:36] [ Silence ]
[30:46] [ Silence ]
[30:56] [ Silence ]
[31:06] [ Silence ]
[31:16] [ Silence ]
[31:26] [ Silence ]
[31:36] [ Silence ]
[31:46] [ Silence ]
[31:56] [ Silence ]
[32:06] [ Silence ]
[32:16] [ Silence ]
[32:26] [ Silence ]
[32:36] [ Silence ]
[32:46] [ Silence ]
[32:56] [ Silence ]
[33:06] [ Silence ]
[33:16] [ Silence ]
[33:26] [ Silence ]
[33:36] [ Silence ]
[33:46] [ Silence ]
[33:56] [ Silence ]
[34:06] [ Silence ]
[34:16] [ Silence ]
[34:26] [ Silence ]
[34:36] [ Silence ]
[34:46] [ Silence ]
[34:56] [ Silence ]
[35:06] [ Silence ]
[35:16] [ Silence ]
[35:26] [ Silence ]
[35:36] [ Silence ]
[35:46] [ Silence ]
[35:56] [ Silence ]
[36:06] [ Silence ]
[36:16] [ Silence ]
[36:26] [ Silence ]
[36:36] [ Silence ]
[36:40] I don't know how to best represent that.
[36:42] That's what I'm going with.
[36:44] [ Silence ]
[36:50] Okay.
[36:52] [ Silence ]
[36:54] So we're going to go with --
[36:56] [ Silence ]
[37:00] What was that from extended key?
[37:02] [ Silence ]
[37:10] Go back to JSON.
[37:12] [ Silence ]
[37:18] Oh.
[37:19] [ Silence ]
[37:23] Let's clone before mutating.
[37:25] [ Silence ]
[37:42] Let's see.
[37:44] [ Silence ]
[37:53] So this needs to be new key, right?
[37:56] [ Silence ]
[37:57] Is that what we're doing here?
[37:59] [ Silence ]
[38:02] So clone.
[38:04] [ Silence ]
[38:05] But then we don't need the assert -- oh, wait.
[38:08] What am I doing here? Hold on.
[38:10] Let me back the truck up.
[38:13] Hold on.
[38:15] Let's back it up.
[38:17] [ Silence ]
[38:25] I'm going to check chat in just a second.
[38:29] All right.
[38:30] [ Silence ]
[38:33] So this is full key.
[38:35] [ Silence ]
[38:52] Oh.
[38:54] Wiped key.
[38:57] Full key.
[39:01] Full key.
[39:05] We don't need to worry about that.
[39:07] [ Silence ]
[39:11] Let's just keep with the style that's here.
[39:14] [ Silence ]
[39:25] Okay. Let's just say --
[39:27] [ Silence ]
[39:45] I do need to double check on this because I'm actually not sure --
[39:50] do I need to hex to U8 this?
[39:53] Get private extended key coming out that way?
[39:55] I think it is, actually.
[39:57] [ Silence ]
[40:07] Copied key, maybe.
[40:14] Copied key.
[40:16] [ Silence ]
[40:22] There we go.
[40:24] [ Silence ]
[40:31] Wait. Do we even need that?
[40:35] This is going to be wiped key.
[40:40] Wiped key.
[40:44] There we go.
[40:47] Okay.
[40:49] So there's no more to -- from JSON.
[40:51] There's no more to JSON.
[40:52] That was it.
[40:53] Those were the things that we need to test.
[40:56] And then I just want to take a look at the implementation of GIT.
[41:06] GIT private extended key.
[41:11] It says GIT string.
[41:15] So, yeah, this is the encoded version.
[41:24] From extended -- all right.
[41:26] So I messed up my test there a little bit.
[41:28] And I will get to chat in just a second.
[41:30] I just need to not do that.
[41:35] That's not necessary.
[41:36] And then we go back to the top where I first used it.
[41:40] And then we need to not do that either.
[41:43] Because that is wrong.
[41:45] All right.
[41:46] Now if I look at this, this should give me the test that -- let me
[41:54] eliminate white space from that as well.
[41:56] Okay.
[41:58] So we assert deep equals still, but on the child object and the
[42:03] object, not the child key to JSON.
[42:08] Probably could just call that child.
[42:11] Okay.
[42:12] From extended key rather than from JSON, because that doesn't
[42:15] make any sense.
[42:17] Okay.
[42:18] Cool.
[42:19] Let's go ahead and I'm going to commit this.
[42:35] Okay.
[42:36] I just want to check out that ref UN8 and just see -- I don't
[42:41] think we made any changes on the async nature of the different
[42:46] methods.
[42:47] Okay.
[42:48] Let me check out the chat.
[42:51] All right.
[42:53] How to make your job obsolete.
[42:56] Yeah.
[42:57] So if you make your job obsolete, typically speaking, you get
[43:00] promoted.
[43:02] Or you get more free time.
[43:05] My father started in support IT role for a hospital in Alabama
[43:08] and eventually moved to Texas, then Utah before he passed.
[43:11] Hey, I'm in Utah.
[43:15] He worked for the school board in Salt Lake City.
[43:17] Interesting.
[43:19] Cool.
[43:20] I worked for a school in Vermont.
[43:29] And depending on your writing style, VT and UT are
[43:33] indistinguishable.
[43:42] All right.
[43:47] Now let's see if these tests pass again.
[43:55] What was this one about?
[43:59] This one was more about browser than really anything else.
[44:05] I think that that could come later.
[44:08] Let me look at -- so this commit right here.
[44:16] I mean, really?
[44:21] Okay.
[44:22] One minute ago.
[44:23] So this one fails.
[44:24] I'm going to check that out.
[44:26] I'm also going to bring -- get checkout ref async.
[44:34] Get pull.
[44:49] Yeah.
[44:50] All right.
[44:51] Ref async.
[45:08] Okay.
[45:10] Let's see what it did not like so much about that.
[45:22] That was a bigger boom than I expected.
[45:30] All right.
[45:54] I'm going to abort that.
[45:59] Let me try looking at that change again.
[46:16] It seems like this should be really easy to bring around.
[46:23] I'm going to try this.
[46:26] Get rebase-i from ref simple.
[46:31] What if we just remove this for the time being?
[46:38] And then I'm going to do pics.txt.
[46:40] I'm going to bring that over.
[46:43] Get status at lib htkey.
[46:50] Okay.
[46:51] It's still -- it's just the shaw function gets put in there, and it makes -- bless me.
[47:19] I don't know.
[47:48] Shaw 256 doesn't get used anymore.
[47:58] All right.
[48:08] I'm a little confused.
[48:09] Let me take this back again.
[48:20] Okay.
[48:21] So -- ah!
[48:24] Okay.
[48:25] I think this is what it was supposed to look like.
[48:30] This is what the diff should have looked like.
[48:32] It should have been showing this.
[48:34] That's a new function that's been added in.
[48:46] I think.
[48:49] It actually should be like that.
[48:52] Well, I'm going to leave that for the time being.
[48:55] Okay.
[48:58] And then we're saying that this hash 160 --
[49:11] all right.
[49:12] Let me see if I can understand this.
[49:16] Try to get rid of that.
[49:17] Get rid of that.
[49:18] Get rid of that.
[49:19] So the function becomes async.
[49:21] Okay.
[49:22] That's clear.
[49:23] The function is returning new versus returning create.
[49:27] That could go later.
[49:34] That problem seems to be solved here.
[49:38] Let me see if I'm looking at this from the right place.
[49:41] Update test for UNAidArray.
[49:43] So this is going to be one of the very next things that could happen.
[49:47] Yeah, I see.
[50:08] Okay.
[50:12] I don't think this is the right route to go.
[50:18] Okay.
[50:19] Rebase abort.
[50:21] I see what's happening there.
[50:22] Okay.
[50:23] So let me go back.
[50:25] I want to make sure that that test is still passing.
[50:28] And let's see.
[50:30] Is there anything else I should get checked out?
[50:32] Okay.
[50:34] You could see me working in Vermont.
[50:37] Oh, no, no, no.
[50:38] That a VT and a UT could look the same.
[50:40] Yeah.
[50:41] I know a girl who her -- so she wanted to go to BYU,
[50:47] which favors people who are from out of state.
[50:49] And she got a rejection.
[50:52] And they -- her mom called up and tried to plead with them.
[50:59] And they asked her something.
[51:02] I don't remember where she lives.
[51:04] But where's Middlebury, Utah?
[51:07] No, no, it's Vermont.
[51:08] Oh.
[51:09] And so her being out of state tipped the scale of her being able to get in.
[51:20] Also, Vermont area codes start with zero.
[51:24] And Utah area codes start with eight.
[51:26] So 04 looks like 84.
[51:35] All right.
[51:36] What was it that was breakinating?
[51:45] Oh.
[51:48] Okay, what?
[51:51] All checks pass successfully.
[51:54] And then async all the things.
[51:58] Is everything breaking?
[52:01] Yeah, I want to know why this is breaking.
[52:03] Because these tests should have passed.
[52:16] Okay, actual versus undefined.
[52:18] Did I forget to do an await?
[52:21] Is that what happened here?
[52:24] From extended.
[52:34] Oh.
[52:36] Whoops.
[52:37] Is it new key?
[52:46] I'm so confused.
[52:56] Oh.
[53:03] Let's try this.
[53:28] I was applying to a Gov contractor and realized that I can choose to not answer demographic questions.
[53:33] There's one question that didn't give an opt-out.
[53:36] It was Hispanic or Latino.
[53:38] Yes, no.
[53:40] Yeah.
[53:42] I don't like that stuff.
[53:51] All right, so let me see if I understand the logic of what's going on here.
[53:56] Okay, should return an object read for JSON serialization.
[54:03] Okay, so from master seed, we've got our seed, we create our key.
[54:08] We derive a path, we get a child key.
[54:11] So then this is our fixture.
[54:16] I think F is for fixture.
[54:22] So seed plus path is private, public and private.
[54:26] Okay, so here's our object that has our private.
[54:30] Now we're going to take our child, which I don't think is quite the right term here.
[54:36] Because here's our child key.
[54:39] This is our expected.
[54:41] So here's our child object.
[54:43] And these are deeply equal.
[54:45] And that looks correct.
[54:47] So was it a strict equal?
[54:52] Expected values to be strictly equal, yes.
[54:55] All right, so then we're going to take that child object and the xpriv there.
[55:00] We're going to turn that into a new key.
[55:02] Then we're going to have a -- I think this -- if that wasn't my terminology, hold on.
[55:11] Get diff head one.
[55:19] Was it called a new key before?
[55:24] It was called a new key before.
[55:26] New key, get private.
[55:41] Okay, so let's see if we can just -- I just want to make as little change as possible here.
[55:46] So I think that this actually would be better off to be --
[56:03] new key, new key.
[56:06] All right, let's try this.
[56:08] Get diff head one.
[56:15] Dash w.
[56:22] All right, so now these are the same.
[56:23] Okay, good.
[56:24] So I think this test will pass now.
[56:25] I think that was just a mistake on my side.
[56:34] Nothing's broken.
[56:37] Okay, so let's go ahead and push that up.
[56:40] And I'm going to take a second to think through this, because we're -- let's see.
[56:51] I'm going to go to this one where I'm doing the PR and see if I can swap the branches that this is going to use.
[57:00] Edit. Ah, I can't edit that one. That's fine.
[57:09] Okay, so this -- here we go.
[57:12] Remove node lock-in.
[57:14] All right, so I'm just going to be really --
[57:26] and then do the buffer bit.
[57:32] And then do async all the things.
[57:36] Oh, wait, let's refresh here.
[57:39] Okay, good.
[57:40] Now this one passes.
[57:42] So we need to remove -- well, we could async all the things without breaking compatibility.
[57:51] So I do want to try that first.
[57:55] So let's do a git checkout -b ref async compat.
[58:03] And we can do the async without bringing over the few other changes.
[58:11] So I'm going to do ref un8array.
[58:15] So we don't need to swap that right now.
[58:19] We don't need to do crypto.
[58:23] We don't need to do this replacement.
[58:41] Can we do that? Okay, we can do that.
[58:44] So I'm going to drop this commit.
[58:49] I'm also going to drop this commit.
[58:58] So I'm going to explicitly drop rather than implicitly drop.
[59:06] Okay, and it's going to, of course, tell me that it doesn't know what the flippy doodle I'm trying to do.
[59:13] And I'm going to say, yeah, you do, you donk a donk.
[59:29] So I don't need to change that, but I do need to change that right there.
[59:49] Okay, I've got this. Okay, I know what I'm going to do. I know how I'm going to update this now.
[60:11] I've got a clear path forward that I believe is a good path forward.
[60:29] Okay.
[60:45] Oh, interesting.
[61:06] That one's really strange. This one right here. I don't know why it can't tell, because basically it had to modify. All I had to do was add something. It didn't have to modify anything, but it thought it had to modify stuff.
[61:34] So while that's running, I do want to change some stuff here. So I actually want to edit this one.
[61:49] And I want to not make web crypto changes. Or maybe I do. I don't know when I introduced this window thing.
[62:12] Let's find out when I did that real quick.
[62:41] 945E4.
[62:52] 945E4.
[63:00] Oh, right. Okay. So that was quite a ways back.
[63:06] And all of this.
[63:11] So yeah, do we do it then?
[63:18] We prep, but we don't actually make the change yet.
[63:36] So let's see. Require.
[64:05] And this would be one of those things where having the utils would actually make a lot of sense.
[64:14] So I'm going to do that utils pattern here as well.
[64:32] Oh, but this isn't asyncing all the things. Hold on. We need to async all the things.
[64:38] Create HMAC. Okay, good.
[65:02] And then I just need to go see, let me go check out dash keys again real quick.
[65:08] So dash keys, dash keys. SHA-256 sum. SHA-512 sum shouldn't be much different.
[65:19] We can even bring in. Yeah. Okay. So this is what we're going to do.
[65:34] Up top here, we're going to do let utils equals, and then we're going to have that type hasher.
[65:47] Let me go ahead and grab that type here.
[65:57] All right. So where does hasher go? Probably. We call it HD hasher. That's fine.
[66:11] A, B, C, D, E, F, G, H. So HD hasher, full UNAidArray.
[66:33] And then. Okay. I'm going to take a look at comments in just a second.
[66:58] Let me SHA-512. And then we're going to have down the bottom.
[67:10] HD key dot utils equals utils. So we need to HD key.
[67:19] So we need to do a similar thing to what we did over in dash keys where we have utils up at the top.
[67:26] Did we do that in something else? Maybe. Actually, I think it was dash TX.
[67:35] Let me check out dash TX real quick. Okay. Utils.
[67:40] So we defined utils on it and then we defined what the utils were.
[67:48] And this is what it kind of looked like. And we're going to redefine all of that one last time.
[67:55] Just renaming things. Nothing, nothing too crazy, just so that we have the same, the same util types throughout.
[68:03] And I think I'm actually going to drop those utils in favor of assigning them straight over from dash keys. We'll see.
[68:20] Okay. HD create. So HD key. So you basically want to have a prop that is HD utils.
[68:32] And then we're going to find HD utils. And then we're going to have something like HD hasher.
[68:42] And this is, we've got ripe MD 160 some. And then we've got SHA 256 some and SHA 512 some.
[68:59] So those are our utils. Okay. Now let me check comments again. Oh, nope. New comments. We're good.
[69:11] Thought I saw something new, but I was mistaken.
[69:20] All right. So there's the bytes and this is pretty much all the same.
[69:29] So now this is swappable.
[69:46] Oh, but we don't quite want to do this. Do we?
[70:04] Let me think about that for a second.
[70:32] Let's see.
[70:55] Okay. SHA 256. All right.
[71:07] There we go.
[71:14] So we could fix like that. There we go.
[71:34] And this actually, again, maintains compatibility without much cost at all. So it might backport that into dash keys.
[71:46] Because the cost of that is now so low that it kind of makes sense just to keep with it.
[71:53] I mean, look at that. Look how little cost there is to make this backwards compatible with previous versions of Node.
[72:06] That's difficult not to jump on.
[72:13] At that level of simplicity, that's difficult not to take. And that actually could be a big win for us.
[72:21] Okay, so let's do await_utils.sha256_sum. Call this bytes, bytes, bytes.
[72:41] So wait_utils.sha256_update.sha256_bytes.waits.ripe_md.
[72:57] SHA bytes, SHA bytes, but ripe SHA bytes, whatever.
[73:06] Okay, so what was it that needed the 512 then?
[73:10] Was it the HMAC? Is that what it was?
[73:25] But didn't I do this? Ah, yes, it's in the other branch. Okay, so I need to check this from the other branch.
[73:32] And I might need to bring in the same bit there.
[73:55] Okay, so this to_do_webcrypto.not_implemented, that has been implemented.
[74:17] Alright.
[74:22] So this is actually good. This is actually good. I was kind of thinking, "Ah, this is maybe a little pedantic."
[74:27] But discovering a way at a very low cost, very simply, to be able to extend...
[74:35] Because not everybody's updated in Node V18, and some people are not going to be updated in Node V18 for a few years.
[74:41] So to not have that be forced is nice for such a low cost.
[74:50] If it was a high cost, and we had to create big, huge wrappers or anything,
[74:54] but with the architecture that I already spent the time designing in the last couple of streams,
[74:59] applying that same methodology with the utils, and just being able to layer it with just that,
[75:03] basically three or four lines of code per function, and four or five functions,
[75:08] I think that's really worth it. I think that this is a good turnout.
[75:18] Okay.
[75:29] Oh, and we're going to need one more.
[75:32] That create_hmac function, this is going to need to go to utils.
[75:54] Yeah, massaging the code.
[75:59] Little by little.
[76:02] Then it came around, all right.
[76:13] So then we have hmac_sha_512.
[76:27] What is the correct word? We create_hmac, and then we...
[76:32] Do we sha_512_hmac? Is that what we do? Is that what it's called?
[76:47] Okay, we don't actually need this.
[76:50] So that one was mistaken. That's okay.
[76:54] No love lost.
[76:58] What's the right... How should this be called?
[77:02] Should it be called sha_512_hmac, as opposed to sha_512_sum?
[77:13] Or should it be called hmac_sha_512?
[77:17] I like this. This sounds better to me.
[77:23] We're going to hmac it. We're going to sum it.
[77:25] We're going to sha_sum it. We're going to sha_hmac it.
[77:28] I think that sounds about right.
[77:33] So this is going to be hd_hmac_er.
[77:48] And I don't think I want to call that hd_hmac_er.
[78:17] @type hd_hmac...
[78:26] And we'll go put this in its place, hd_hash.
[78:30] hd_hmac should be right below it, I think.
[78:34] And this also needs to be a promise.
[78:40] No, whoops.
[78:49] gh_hmac.
[78:52] Alright, happy coding. I'm going to get some rest. Good.
[78:56] Alright, dubs. See you on the next one.
[78:59] Exploding new. Chiropractic code. Yes. Yes.
[79:04] Night night everybody.
[79:11] Alrighty.
[79:17] And the web crypto does exist. I think I can pull it in right now.
[79:24] So async all the things.
[79:27] Why did this fail again?
[79:29] Did I not, or maybe I didn't push the change yet.
[79:32] But let's see why it failed.
[79:38] Failed because...
[79:42] Okay, cannot read property undefined of import key.
[79:47] Right.
[79:55] Wait, where is import key used?
[79:58] Import key.
[80:03] Perhaps that's in the test that it's using that.
[80:07] But if we go back here to, I don't know whether it was this PR or this PR, but one of these PRs.
[80:14] Let's look at the files changed.
[80:17] We look for hmac.
[80:20] Oh, this was the thing that pissed me off.
[80:23] Pardon my French.
[80:28] I remember this now.
[80:39] Let me see if I can find it.
[80:41] Yes. Yes. This just ticked me off. This right here, that it had to be so flippin complicated to do the digest in web crypto.
[81:01] Web crypto just made it insane nonsense and I was and I was peeved greatly.
[81:19] Alright, so then if I look back at this async all the things.
[81:28] So look at these commits.
[81:39] Was this not?
[81:45] Import keys not there. So where did import key come from here?
[81:54] Import keys not here.
[81:57] Okay, did import key come in in here?
[82:07] Alright, we're going to try this one though.
[82:13] Async all the things.
[82:17] Best effort compat.
[82:24] Like number 50, 60, 55.
[82:36] Oh, whoops. Nope. Nope. Nope. Against my own stuff.
[82:43] Against ref UN 8 array. Okay, like number nine, but with a few tweaks for better compatibility.
[82:59] With node V 16.
[83:13] I could make a lot of money by changing this in the keyboard. Blah, blah, blah, blah, blah. I love long digest functions. Oh my goodness.
[83:28] I don't even know what that means.
[83:31] I don't feel safe anymore. I don't feel safe.
[83:39] Okay.
[83:44] Alright, so if we could do it the simple way, do it the simple way. Otherwise.
[83:57] Okay.
[84:23] Look at this garbage.
[84:25] Look, okay, node, node, very simple.
[84:30] Entropy data update digest web crypto.
[84:38] They, I mean, they, they, they were successful in what they wanted to do, right? Which is they wanted to put a barrier to entry in place such that tards wouldn't use web crypto.
[84:53] And it's so daggone complicated. You gotta be a flippin genius to do it. They succeeded. They, they, they successfully shoved the use of web crypto into the domain of people who are much more expensive.
[85:09] Thankfully, some of those people wrap that stuff and exported it in a way that others were able to use it.
[85:23] Okay. Utils, SHA-512-HMAC.
[85:39] Alright, let's see if we didn't break the tests with all of this.
[85:43] Probably did.
[85:45] Probably some, something that's not quite the way it should be, but.
[85:50] Oh, wait.
[85:53] SHA-512.
[85:56] Bramp, bramp.
[86:01] So indeed, 512 does come after 256.
[86:18] Alright.
[86:24] Fix test for async functions. Why is this a problem?
[86:33] Ah, I see, I see, I see.
[86:36] So we wanted to get rid of from JSON. We wanted to put in htutils. This is not a problem.
[86:52] Okay, this still looks clean as a whistle. Just as I expected it to be.
[87:07] Alright, there we go.
[87:24] Alright, let's sit back and watch the check marks and Xs, my friends.
[87:37] A lot of people listen to typing to relax.
[87:39] So is my keyboard loud?
[87:42] Is that what we're saying?
[87:53] Alright, my mind's not blown that that failed.
[87:59] Operation was cancelled, of course.
[88:02] Can we rerun it?
[88:04] Let's rerun the job without it cancelling this time. Maybe.
[88:10] Okay.
[88:22] Alright, let's find out why you failed.
[88:32] Data must be a string or a buffer.
[88:46] Why is hash space in here?
[88:58] Oh, for RipeMD.
[89:00] Okay, update.
[89:02] So I may have mistyped something.
[89:06] Let's go ahead and take a look here. RipeMD 160.
[89:17] RipeMD 160 sum.
[89:22] So bytes go in.
[89:26] Interesting.
[89:30] So apparently I did not use this the way I thought that I had.
[89:54] Alright.
[89:56] Console.log.
[89:58] Debug.
[90:00] Show bytes.
[90:07] Okay, bytes go in.
[90:11] Bytes come out.
[90:19] Oh, right.
[90:23] This is why I had updated it earlier.
[90:27] Because I wanted to, okay.
[90:30] RipeMD 160.
[90:33] So this one comes into here.
[90:37] And this is not compatible. Let's see what it says that it can take.
[90:44] Data must be a string or a buffer.
[90:46] Okay. So let's try this then.
[90:49] We're going to do let hex equals.
[90:55] Do we have a two hex implementation in here?
[91:24] Forgive me, for I know what I do, and I'm doing it anyway.
[91:36] Let hex plus be two string 16.padstart.
[91:55] Let h equals this.
[91:59] I don't know when padstart got added.
[92:01] Well, we'll find out. We'll find out when padstart got added.
[92:04] Because this will probably not work.
[92:10] So return.
[92:19] Padstart two with a zero.
[92:23] Return hex plus h.
[92:25] Okay. So that's kind of the smallest way to do it.
[92:28] That's what I'm going for right now is smallness.
[92:37] Okay.
[93:06] There we go.
[93:33] There we go.
[93:36] And the creep begins.
[93:38] Okay.
[94:07] Yeah.
[94:15] Private key verify public key creates.
[94:19] But you really don't need the private key verify because the public key create is going to do that.
[94:24] But that's okay.
[94:44] All right. One problem at a time.
[94:54] Okay.
[95:17] Oh, good. It's at a comfortable level. I'm glad.
[95:21] So let's see. This is this touching in. No. Okay.
[95:26] Good. Yeah. The typing should be.
[95:32] Low. I have the mic.
[95:35] Let's see if I can show you.
[95:37] Man, I'm not going to bother with it right now.
[95:40] Okay. Let's. Why is this? Why is this failing?
[96:02] Oh, I forgot. I can.
[96:04] I do have the ability to run the test locally.
[96:24] Let's run locally and see what happened.
[96:26] All right.
[96:28] So things look really bad. Everything's failing. And that's good. It's nice when everything fails.
[96:35] It's really not nice when a few things fail.
[96:45] So what this is telling us is that.
[97:00] Everything is off wildly, which probably means that something went wrong with that.
[97:09] Ripe MD. So let me check out ref you an eight array.
[97:16] And let me see what it looks like over here.
[97:19] Ripe MD.
[97:38] Let's also take a look at the create HMAC.
[97:56] Make sure. So chain code.
[98:00] Master secret.
[98:05] Let's check out this other branch again.
[98:13] Utils dot shop 512 HMAC master secret.
[98:21] This other one should have chain code.
[98:25] Entropy created with the entropy and update the data.
[98:30] Just making sure those look about the same.
[98:34] My suspicion is it's the Ripe MD.
[98:51] And my suspicion is that it actually wants a bin stir, not hex.
[99:02] And a bin stir.
[99:12] Let's see is best done by.
[99:21] Going over each bite.
[99:28] Ben's dot push B dot.
[99:40] String dot from.
[99:44] Char code. If I remember correctly.
[100:13.00] All right.
[100:20.00] Let me just double check this here.
[100:23.00] String dot from.
[100:25.00] Char code.
[100:27.00] 255. There we go.
[100:48.00] Oh, that may not be what I want, though.
[100:56.00] OK, cons. Jason dot stringify. This should not be possible. This should result in an error.
[101:21.00] All right. I think.
[101:24.00] I'll try one more thing here.
[101:31.00] I think it may be the debug that's printing it out this way.
[101:36.00] Let's try this.
[101:42.00] One PM run test.
[101:52.00] Hold on.
[101:54.00] All right, now we're drifting into dangerous territory.
[101:58.00] What did I call it?
[102:04.00] Unabomber.
[102:13.00] Let's take a look at the old source here.
[102:28.00] Binary string.
[102:31.00] This is it.
[102:36.00] OK, so.
[103:05.00] That's not quite it, actually.
[103:15.00] What we want is.
[103:19.00] Buffered a binary string.
[103:24.00] That should be right.
[103:53.00] All right.
[104:15.00] This is just what I had.
[104:17.00] Maybe copying paste. It will just be better, though, you know.
[104:46.00] All right.
[105:14.00] All right.
[105:43.00] There we go.
[105:49.00] See, maybe what's coming in is garbage that looked like that might have been the case.
[106:18.00] OK, let me.
[106:21.00] Let me retry.
[106:25.00] I take a few steps back from this.
[106:38.00] So we've got these commits elsewhere.
[106:56.00] So we're gonna go ahead and drop this one that's that exists elsewhere.
[107:09.00] And we're going to update the test before we update the code in this universe.
[107:27.00] And then we're going to save a copy of this.
[107:36.00] And.
[107:44.00] We're going to take this in two steps.
[107:59.00] And then we're going to get rid of.
[108:03.00] Well, now we are we're just we are going to do dash hard get reset dash dash hard.
[108:12.00] OK, so then.
[108:18.00] We're going to.
[108:25.00] Remove.
[108:31.00] Our utils stuff.
[108:36.00] From here, just try to take it really slow.
[108:41.00] And walk it back.
[108:44.00] It's probably something really simple going on here.
[108:49.00] And if we take it one step at a time.
[109:01.00] We'll get it.
[109:04.00] For example, let me just test one thing real quick.
[109:08.00] H-Mack.
[109:11.00] SHA-512 H-Mack.
[109:16.00] OK, SHA-512.
[109:18.00] Let's go. OK.
[109:22.00] Seems to be all right.
[109:27.00] Crypto dot create H-Mack.
[109:34.00] SHA-512.
[109:40.00] Update data digest.
[110:09.00] OK, that should be about it.
[110:33.00] So if I did a diff between this one.
[110:40.00] My life. So my life is good since everything has failed.
[110:46.00] Great.
[110:48.00] Explodino.
[110:52.00] It all failed. Explodino.
[111:06.00] How can you explain this to me?
[111:24.00] OK.
[111:39.00] RIPEMD160.update.digest.
[111:59.00] Crypto dot create SHA-256.update.digest.
[112:28.00] All right.
[112:35.00] So basically now.
[112:38.00] It's just a sink away all the things.
[113:02.00] All right, so we need I back.
[113:31.00] All right.
[113:43.00] There's another one.
[113:48.00] SHA-512 strikes again.
[114:08.00] Promises promises.
[114:37.00] Ah, that was the buffer. OK.
[114:54.00] H-160.
[115:23.00] OK.
[115:47.00] Let's try this one.
[115:56.00] Make.
[115:59.00] Async.
[116:05.00] Run test. Hey, passing test is that. OK, so let me get check out.
[116:13.00] Ref a sink.
[116:16.00] And we're going to do get rebase against this one.
[116:21.00] Check out.
[116:23.00] Ref a sink compacts get rebase dash I.
[116:42.00] Async all the things in prep for browser compat.
[116:58.00] Web crypto prep.
[117:02.00] Async all the things. There we go. That's what we should call it.
[117:10.00] All right, now let's take this.
[117:16.00] A little bit more atomically than we did last time.
[117:28.00] HD to.
[117:54.00] We're going to move things to HD utils so utils dot.
[118:00.00] Whatever.
[118:06.00] But the trick is this time.
[118:16.00] We're just going to keep the existing implementation as is.
[118:27.00] So find our.
[118:31.00] H Mac. And we're just going to take this into utils. So a weight dot utils dot.
[118:54.00] HD chain code.
[119:00.00] Data.
[119:29.00] Wait utils dots.
[119:33.00] Shaw to fifty six some.
[119:37.00] Buff.
[120:00.00] And then.
[120:07.00] Wait utils. Right. Md 160 some.
[120:36.00] Okay.
[120:54.00] So.
[121:21.00] Okay.
[121:49.00] Crypto.
[121:52.00] Move things to utils.
[122:21.00] Okay.
[122:38.00] Okay.
[123:07.00] Okay, I don't remember what this means.
[123:13.00] Two fifty one to sixty five to eighty seven to ninety one.
[123:20.00] One twenty nine. So it's just a couple of places here.
[123:24.00] So let's move that out. Let's create utils for this.
[123:34.00] Utils to public key.
[124:03.00] Okay.
[124:22.00] I like this one.
[124:26.00] It's dangerous to go alone.
[124:33.00] CD potent.
[124:36.00] Hmm.
[125:02.00] Hmm.
[125:31.00] Hmm.
[125:52.00] Key convert.
[125:57.00] I'm going to take a look at this. This and dash keys is called what?
[126:05.00] No.
[126:07.00] What do we have? Get public key.
[126:12.00] That's in what that's in the block TX.
[126:28.00] Let me see. Actually, I've already got it. I've already got here locally.
[126:31.00] Let me just.
[126:34.00] Dash this get checkout ref a sink.
[126:38.00] And then take a look at this one.
[126:41.00] Sec P two fifty six K one.
[126:45.00] Point from hex.
[126:47.00] Two raw bytes.
[126:50.00] Is that the.
[126:53.00] So I think this is.
[126:55.00] Two raw bytes.
[126:58.00] From my set public key value.
[127:03.00] Equals point two raw bytes.
[127:06.00] Oh.
[127:08.00] Two.
[127:10.00] Two. So this is basically uncompressed.
[127:21.00] I think that's what this is saying.
[127:28.00] Point from from hex value.
[127:32.00] Point two raw bytes compressed key.
[127:36.00] Is value.
[127:56.00] Let me see how this was used in the tests.
[127:59.00] Set public key.
[128:04.00] That's definitely taken a buffer there.
[128:07.00] Or.
[128:08.00] You know it's taken bites.
[128:11.00] So what's going on set public key.
[128:33.00] Let me take a look.
[128:36.00] At.
[129:04.00] Two raw bytes.
[129:09.00] I think that's doing nothing more than validating the key.
[129:13.00] I think that's.
[129:40.00] Oh no.
[129:44.00] This is actually.
[129:47.00] Two raw bytes.
[129:50.00] Hex two bytes.
[130:18.00] Okay.
[130:36.00] Okay.
[131:04.00] So this is basically.
[131:06.00] Saying.
[131:12.00] To compress public key.
[131:15.00] Or.
[131:26.00] We could say.
[131:28.00] Normalize.
[131:30.00] Public key maybe.
[131:53.00] We could have let public key.
[131:56.00] By the way there shouldn't be any bar in here anymore right yeah good.
[131:59.00] Let public key equals utils dot normalize.
[132:24.00] All right.
[132:53.00] Hmm.
[132:56.00] Well that's kind of strange.
[133:02.00] Oh needs in a way.
[133:31.00] All right.
[133:50.00] CTSA sign.
[134:14.00] Public key tweak public key tweak.
[134:42.00] Public key.
[135:01.00] Oops okay.
[135:03.00] Let's do that.
[135:25.00] Public key normalize sure let's do that.
[135:28.00] Oops.
[135:38.00] Tells.
[136:07.00] Okay.
[136:12.00] Public key tweak add.
[136:35.00] Okay.
[136:46.00] Yeah.
[136:49.00] Okay.
[137:18.00] Okay.
[137:43.00] Okay.
[138:12.00] Okay.
[138:15.00] If public key length is so.
[138:19.00] Then public key.
[138:23.00] Equals.
[138:26.00] Public key.
[138:29.00] Here we go.
[138:56.00] Oops that needs a true there good thing I caught that.
[139:01.00] Okay.
[139:30.00] Okay.
[139:40.00] And then we'll have a private key.
[139:52.00] You know maybe I'll have hash functions together.
[139:58.00] Or I'll have these together.
[140:18.00] Private key tweak.
[140:21.00] And.
[140:25.00] Okay.
[140:28.00] Okay.
[140:56.00] Okay.
[141:00.00] What's next.
[141:07.00] Okay.
[141:34.00] Okay.
[141:44.00] HD private key tweak.
[141:52.00] HD public key.
[142:01.00] Public key tweak.
[142:07.00] To public.
[142:10.00] Public key.
[142:39.00] Okay.
[142:42.00] Why is this scraping.
[142:47.00] What's missing what's broken.
[142:49.00] What's broken so badly.
[142:55.00] Oh, comma.
[142:57.00] Fine fine.
[143:04.00] There's where our two public key will go.
[143:20.00] And in that regard I think this actually should go.
[143:23.00] You know that I had it before.
[143:51.00] These can all just be called.
[143:53.00] Key to key.
[144:22.00] Okay.
[144:36.00] So now this is going to go significantly higher.
[144:39.00] H I J K.
[144:47.00] And then key tweak.
[144:51.00] Okay.
[145:02.00] Tweak bites.
[145:08.00] Key bites.
[145:11.00] Okay.
[145:34.00] Okay.
[145:42.00] Private key tweak and.
[145:52.00] To public key.
[145:57.00] And public key.
[145:59.00] Yeah.
[146:02.00] Okay.
[146:05.00] Okay.
[146:34.00] Okay.
[146:47.00] No.
[147:13.00] Okay.
[147:42.00] Okay.
[147:57.00] Yeah.
[148:13.00] I don't like this here.
[148:15.00] I am going to get rid of it eventually but I'll bring it along.
[148:17.00] A little bit further.
[148:39.00] And private key.
[148:45.00] HD sign.
[149:08.00] Message to sign.
[149:21.00] Private key.
[149:42.00] I have an HT sign.
[149:51.00] Oh.
[149:54.00] HT tell sign.
[150:12.00] All right. There's HT you tell sign. What else?
[150:14.00] We're going to need an HT util verify.
[150:20.00] This is just going to be a hash and a signature.
[150:25.00] Okay.
[150:26.00] Okay.
[150:27.00] Okay.
[150:55.00] Okay.
[151:23.00] Okay.
[151:34.00] All right.
[151:36.00] QRS TV.
[151:39.00] Verify.
[151:42.00] Okay.
[152:11.00] Okay.
[152:12.00] Okay.
[152:41.00] I wonder what this Boolean is not assignable to type.
[152:46.00] All right. Oh.
[152:48.00] There we go.
[153:17.00] Okay.
[153:41.00] Okay. Functions.
[153:50.00] Okay. Now what are we left with?
[154:19.00] Okay.
[154:48.00] Let's make sure that this is still passing over here.
[154:58.00] All right. Good. All checks pass again.
[155:01.00] All right.
[155:30.00] Okay.
[155:59.00] Now.
[156:04.00] We can.
[156:06.00] Let's see.
[156:18.00] Oh, here's one.
[156:21.00] I've been wanting to get rid of.
[156:47.00] Less used.
[157:14.00] I think that one right there.
[157:17.00] Probably actually apply to.
[157:20.00] The simple JS one.
[157:35.00] Oh, wait. Oops. Hold on.
[157:38.00] Let's go back.
[157:46.00] Electrify.
[158:15.00] Okay.
[158:44.00] Okay.
[159:04.00] Okay.
[159:33.00] I'm not going to bother with that one.
[159:37.00] All right. Let's see what else we got left here.
[159:49.00] Wait, why is Mocha included again?
[159:53.00] Mocha is provided by what?
[160:06.00] Mocha.
[160:34.00] Okay. I'm starting to see where Mocha is coming from, I think.
[160:37.00] So it's a dependency of Mocha Chino.
[160:41.00] Mocha Chino.
[160:44.00] This is all just garbage. Okay. This is that's weeds.
[160:47.00] I'm getting out of there.
[160:54.00] Okay, I think I've taken this as far as I can take it in a compatible way.
[161:07.00] Time to start breaking things.
[161:31.00] Pull requests.
[161:35.00] All right. So --
[162:04.00] Okay.
[162:19.00] Oh, hey.
[162:21.00] Hit the limit of a government API.
[162:24.00] That's a kind of lame request limit. Yeah, I believe that one.
[162:38.00] Okay. So here you go.
[163:01.00] Switch to UN8 array. This builds on number --
[163:14.00] By two commits.
[163:17.00] Drops buffer in favor of UN8 array.
[163:25.00] To see just the changes between the two.
[163:54.00] Okay. Refactor.
[163:56.00] So this is async all the things.
[164:25.00] Okay.
[164:53.00] Okay.
[165:14.00] Web fixes for async functions.
[165:32.00] Browser compat prep.
[165:47.00] Okay. There we go.
[166:16.00] Okay.
[166:19.00] Switch to async await.
[166:30.00] This builds on number and paves the way for --
[166:42.00] Browser compatibility.
[166:56.00] With web crypto.
[167:02.00] Oh, that's right. That's what I've got to do.
[167:04.00] That's what I've got to do.
[167:29.00] Switch to SHA-256.
[167:47.00] We need to just update these thingamabobs.
[167:50.00] So lib http SHA-256 sum becomes --
[168:05.00] So crypto is equal to window.crypto.
[168:11.00] Or require crypto.
[168:40.00] There we go.
[169:08.00] All right.
[169:21.00] All right. Let's try this.
[169:43.00] Try the bottom one like that. See if that makes a difference.
[169:53.00] No, it doesn't. Okay.
[170:05.00] Okay.
[170:27.00] Duplicate identifier utils.
[170:49.00] That's a little confusing.
[171:15.00] Okay, well.
[171:26.00] Whatever.
[171:30.00] Just have to ignore that one because that was a weird
[171:35.00] one.
[172:03.00] Okay.
[172:15.00] Oh, whoops. Hold on. There's something else still.
[172:32.00] Whoops. We let one get away.
[172:36.00] All right. Hold on.
[172:41.00] What have we done wrong here?
[172:45.00] Not much.
[172:47.00] Okay. So let's get stashed this for just a second.
[173:03.00] Hmm.
[173:05.00] Let's see what's going on here now.
[173:08.00] So we still need utils dot SHA-512-HMAC.
[173:18.00] Master secret seed buffer. Let's get that one real quick.
[173:47.00] That's weird.
[173:49.00] I would catch it here, but not there.
[173:53.00] SHA-512-HMAC.
[174:12.00] Pan run. Whoops. Test.
[174:41.00] Hmm.
[174:54.00] Hmm.
[175:23.00] Hmm.
[175:43.00] Hmm.
[176:05.00] All right. Everything passes.
[176:14.00] All right. So in that case, everything passes. Why did things start failing now?
[176:43.00] Okay.
[177:09.00] Seed buffer.
[177:22.00] SHA-512.
[177:31.00] Entropy.
[177:37.00] Data.
[177:42.00] Ah, doi! As always, it's the await.
[178:11.00] Okay.
[178:18.00] Okay.
[178:42.00] Okay. Crypto dot random bytes.
[178:46.00] Utils dot...
[178:52.00] What do we call it?
[178:55.00] Scrub bytes.
[179:15.00] Sanitize scrub.
[179:17.00] What do we used to call it? When you overwrite the bytes.
[179:44.00] Okay. Let's not. We won't make that synchronous.
[179:55.00] Bleach.
[180:03.00] Thank you. Thank you for that good laugh.
[180:05.00] I appreciate that so much.
[180:17.00] Okay.
[180:37.00] Okay.
[180:57.00] Okay.
[181:24.00] Okay.
[181:36.00] Okay.
[181:45.00] That was a good one.
[181:50.00] Okay.
[182:18.00] Okay.
[182:37.00] Okay.
[183:02.00] Okay.
[183:19.00] Oh, they get added later.
[183:22.00] Okay.
[183:32.00] Because now we have to fix the same thing again right now.
[183:36.00] It's secure in it.
[183:53.00] Oh yeah.
[184:05.00] Okay, cool.
[184:07.00] Okay.
[184:36.00] All right, so here's the SHA-SUM one now.
[184:39.00] Okay, great.
[184:40.00] Everything's in place.
[184:43.00] Hopefully this works now.
[184:46.00] 256 SUM.
[185:00.00] Okay.
[185:29.00] Okay.
[185:53.00] That was it.
[185:56.00] Okay, let's see.
[185:58.00] No, they do not.
[186:06.00] There must be a string or a buffer.
[186:35.00] Okay, good.
[186:38.00] Now that passes again.
[186:41.00] That was a whole lot of Hubble blue over nothing.
[186:51.00] Do I not have in that poster over here, U and 8 array to buffer to binary string?
[187:14.00] I'm just curious.
[187:24.00] I'm just going to swap this real quick, just to see.
[187:53.00] Okay.
[187:57.00] All right.
[187:59.00] Okay.
[188:28.00] Okay, let's try this one.
[188:45.00] What kind of string is it expecting to take?
[188:48.00] That's where I'm confused.
[188:55.00] Well, whatever.
[188:58.00] I found the bit why it doesn't work, and now it works.
[189:01.00] So, we go with it.
[189:29.00] All right.
[189:52.00] Test still passing, excellent.
[190:13.00] Oh, test do not pass.
[190:17.00] Okay.
[190:32.00] Okay, so.
[191:01.00] All right.
[191:12.00] Port of crypto.
[191:36.00] Okay.
[191:57.00] So, I must not have gotten the test to pass in that other one.
[192:00.00] Because I'm pretty sure that that's what I copied this from.
[192:04.00] Let me think about that a little bit.
[192:18.00] Let me look up the HMAC algorithm real quick, though.
[192:39.00] All right, so it's the hash of K concatenated with the hash of -- what?
[192:50.00] How is -- somebody explain -- what is this -- H is a cryptographic hash function.
[192:57.00] M is the message -- concatenation, okay.
[193:00.00] Denotes concatenation.
[193:01.00] Denotes bit wise exclusive or.
[193:04.00] Okay, so you have a hash function.
[193:11.00] And M is the message to be authenticated.
[193:17.00] K is the block sized key derived from the secret.
[193:24.00] Okay.
[193:31.00] Okay, but it's definitely different from just -- from doing a hash.
[193:37.00] Okay, because I was thinking -- I thought HMAC was just if you just do the hash again.
[193:43.00] You know, but that's -- no, that's not what it is.
[193:46.00] Okay.
[193:47.00] HMAC is a separate thing and it requires bit wise oring, which is in itself a type of hashing.
[193:58.00] Okay.
[194:27.00] All right.
[194:52.00] Let's see.
[195:21.00] Okay.
[195:32.00] Interesting.
[195:40.00] Okay, so secure race.
[195:42.00] Yeah.
[196:11.00] Okay.
[196:30.00] Okay.
[196:36.00] So how do we get this HMAC function to work?
[196:40.00] This is actually kind of important.
[196:45.00] We do need the HMAC function to work as it turns out.
[197:04.00] I thought I -- I guess maybe I didn't get it working before.
[197:12.00] Let me just -- let's see.
[197:14.00] Let's just step by step on this.
[197:17.00] Okay, format of the key is raw.
[197:19.00] That makes sense.
[197:20.00] The algorithm is HMAC.
[197:21.00] SHA-512.
[197:23.00] That makes sense.
[197:24.00] Extractable.
[197:25.00] We want the key extractable true.
[197:28.00] We want the key usage to include sign.
[197:30.00] That makes sense.
[197:32.00] Crypto.subtle.importkey in the raw format with the entropy that's been given,
[197:41.00] with the certain algorithm and the key usages.
[197:44.00] And then we're crypto.subtle.signHMAC using the HMAC key and then the data
[197:55.00] that was provided.
[197:58.00] And then have a new signature.
[198:00.00] Crypto.log sig.
[198:03.00] Let's have it do both.
[198:13.00] I can think of one thing that might be wrong here.
[198:39.00] Hmm.
[198:45.00] Well, this is weird.
[199:11.00] This is weird.
[199:30.00] That seems like this is not running.
[199:55.00] Something must be wrong here.
[200:24.00] I'm going to ask chatGPT.
[200:42.00] What's the web crypto equivalent of nodes of this node code?
[201:04.00] Hmm.
[201:26.00] GPT wants me to change extractable to false.
[201:39.00] It wants me to make sure that I know the type of entropy, type of data.
[202:08.00] Node encoding 16.
[202:10.00] We can try hex then.
[202:19.00] Object, object.
[202:21.00] Great.
[202:32.00] Oh.
[202:34.00] Oh, is that our problem?
[202:36.00] Is there a problem?
[202:38.00] That, uh.
[202:42.00] Oh.
[202:52.00] Wait, one of these is coming in.
[202:59.00] Master secret.
[203:04.00] Oh, dang.
[203:07.00] Oh, shoot, dang.
[203:17.00] I did not see this before, but it appears that seed buffer from master seed.
[203:25.00] Okay, seems that seed buffer is coming in probably from the tests.
[203:52.00] Ah.
[203:58.00] Missing hex to U8 right there.
[204:21.00] All right, that's it.
[204:48.00] Uh, okay.
[205:17.00] Okay.
[205:19.00] Okay.
[205:46.00] Ah, this was not pulled in here.
[206:08.00] Got it, got it, got it.
[206:10.00] Okay.
[206:23.00] This was pulled in here.
[206:32.00] One test, yep, all right, cool.
[206:52.00] All right, now tests are passing.
[207:20.00] Okay.
[207:27.00] Okay.
[207:56.00] Okay.
[208:05.00] Missing option.
[208:11.00] Ah.
[208:14.00] This actually needs to be called hash, not digest.
[208:20.00] Okay, cool.
[208:23.00] Thanks, chatGBT.
[208:26.00] Thanks for rubber ducking with me and for being more correct in the example I was reading
[208:33.00] from, because the example I was reading from told me to use digest, and that was wrong.
[208:38.00] I suppose I don't need the key to be extractable, though that doesn't matter in terms of its
[208:47.00] function.
[209:16.00] All right.
[209:44.00] I want to try one more thing.
[210:13.00] Before I try anything, though, I should save this.
[210:42.00] All right.
[211:10.00] Okay.
[211:15.00] Cool beans.
[211:29.00] And now we're about ready to rip through this Mojanker.
[211:32.00] Don't remember where to have my paste buffer.
[211:38.00] Oh, okay.
[211:39.00] One last thing that I wanted to try on this, though, before I just rip it apart.
[212:03.00] All right.
[212:32.00] Oh, track mode.
[213:01.00] This is just purely for my own wanting to know if this can work.
[213:20.00] No, it can't.
[213:23.00] That's very interesting.
[213:25.00] Seems like it should be able to work.
[213:33.00] Okay.
[213:34.00] What about the read me has changed at this point?
[214:02.00] Wait, is from master seed, from master seed, yeah, that's become async, too.
[214:31.00] Okay.
[214:33.00] Okay.
[214:42.00] Okay.
[214:53.00] Okay.
[215:02.00] Okay.
[215:12.00] Okay.
[215:40.00] Okay.
[215:44.00] I'm pretty sure derive has become async.
[215:48.00] I think everything's become async at this point.
[215:54.00] So this would just be HT.
[216:04.00] Wait.
[216:07.00] Wait.
[216:12.00] Let me see.
[216:19.00] Are those actually changed?
[216:27.00] Oh, yeah, I changed those.
[216:52.00] Private key.
[216:57.00] It's pretty simple.
[217:21.00] Okay.
[217:27.00] Okay.
[217:33.00] Okay.
[217:54.00] I'm going to have to put in some effort tomorrow on this for getting the documentation up-to-date,
[218:02.00] but I'm going to get a little bit further tonight.
[218:07.00] The thing I want to do tonight is to finish off a series of PRs.
[218:21.00] All right, we've got...
[218:36.00] Now we're going to go whole hog on this bad boy.
[218:42.00] And try to keep compatibility.
[218:46.00] Oh, wait.
[218:48.00] Wait.
[218:49.00] Uh-oh, what broke?
[218:50.00] Oh.
[218:51.00] Okay, yeah, yeah, yeah, yeah, yeah.
[218:52.00] All right, all right, all right.
[218:53.00] Fine.
[218:54.00] Let me go back here.
[218:55.00] Okay.
[219:21.00] Okay.
[219:49.00] There we go.
[220:06.00] That should go through now.
[220:12.00] I should not break things.
[220:22.00] Check progress here.
[220:41.00] Looks like everything passed.
[220:44.00] All right, great.
[220:45.00] Cool.
[220:46.00] Okay.
[220:48.00] Cool.
[221:13.00] All right.
[221:42.00] Okay, so there's Mocha.
[221:56.00] Oh, wait.
[221:58.00] How was that there?
[221:59.00] Oh, I must have deleted that by mistake the last time I was looking at this.
[222:04.00] Yes.
[222:17.00] All right, so let's see.
[222:32.00] Istanbul at 0.4.
[222:47.00] Khabarovsk at 3.
[222:54.00] What else?
[223:00.00] MPX, Mocha 5 at 6.
[223:07.00] Wait.
[223:09.00] Yeah.
[223:11.00] Okay.
[223:27.00] Okay.
[223:31.00] All right.
[223:37.00] All right.
[223:43.00] Let's see.
[224:09.00] Update dubs.
[224:38.00] Only install necessary depths.
[224:45.00] Update Mocha.
[224:48.00] Mocha.
[225:16.00] What's wrong here?
[225:45.00] When did I take that one out?
[226:10.00] Oh, that's interesting.
[226:28.00] Hold on.
[226:30.00] Let me go take a look at this real quick.
[226:49.00] Okay.
[226:53.00] Update tasks, fix tasks.
[227:03.00] Let's check out rough and 8-Array.
[227:32.00] All right, let's just take -- oh, check out rough.
[227:59.00] Check out rough -- was it dash keys?
[228:07.00] Check out rough simple JS.
[228:15.00] And we probably just want to do this.
[228:35.00] Okay.
[228:36.00] So we're getting rid of Istanbul.
[228:39.00] Get rid of this old Mocha.
[228:42.00] We can get rid of Mocha 5.
[228:45.00] Get rid of pure random.
[229:12.00] Okay.
[229:32.00] Rebase.
[229:34.00] Continue.
[229:40.00] Check out rough.
[229:58.00] Check out rough 8-Array.
[230:10.00] So this one's okay.
[230:13.00] We don't need the Istanbul's or the Mocha's or any of that stuff.
[230:41.00] Check out rough.
[230:45.00] Rough AsyncCompat.
[230:54.00] Update tests.
[231:05.00] I don't think we actually want that one.
[231:25.00] Oh, whoops.
[231:26.00] I think I messed up on something there.
[231:29.00] Check out rough simple JS.
[231:37.00] Does this test still have the secure -- secure random?
[231:39.00] Secure random.
[231:45.00] So we actually should have -- instead of secure random.random
[231:54.00] dot hit random.
[231:59.00] So it was at random.
[232:01.00] Get random bytes.
[232:16.00] Okay.
[232:17.00] Get stash.
[232:18.00] Get check out.
[232:21.00] Look at the test here.
[232:25.00] Crypto's number three.
[232:26.00] That's great.
[232:50.00] Okay.
[232:52.00] Okay.
[232:54.00] It's random bytes.
[233:10.00] There we go.
[233:39.00] So I am just making my way through here.
[234:08.00] Not too much exciting right now.
[234:18.00] Just trying to get this stuff all in a row.
[234:23.00] Okay.
[234:25.00] Continue.
[234:36.00] Oh, you know what, though?
[234:38.00] Hold on.
[234:47.00] Dang it.
[235:01.00] There we go.
[235:16.00] Package -- okay, good.
[235:34.00] Get check out rough types.
[235:38.00] Get rebase dash iref simple.
[235:57.00] Update all tests with new APIs.
[236:00.00] What could that be?
[236:06.00] Oh.
[236:08.00] I know why it's showing these.
[236:11.00] We can just drop each of these.
[236:16.00] Okay.
[236:17.00] And then get check out.
[236:18.00] Is it ref?
[236:43.00] Oh, whoops.
[237:12.00] Let's see what's going on here.
[237:25.00] Okay.
[237:54.00] Let's see.
[237:55.00] Tests.
[237:56.00] HTTP.
[237:57.00] Crypto.
[237:58.00] 5E.
[237:59.00] Dang it.
[238:00.00] Right here.
[238:01.00] This one.
[238:02.00] Should be demo quotes.
[238:03.00] There we go.
[238:04.00] Okay.
[238:05.00] Let's see.
[238:25.00] All right, I've got to move this up here.
[238:43.00] Remove the safe buffer.
[238:47.00] Okay.
[238:48.00] Get check out ref.
[238:52.00] We're just going to go up the tree here.
[238:56.00] Hopefully for the last time now.
[239:01.00] Okay.
[239:02.00] Get rebase dash dash abort.
[239:05.00] And then do get rebase dash I this time.
[239:14.00] All right.
[239:17.00] Drop that in favor of this one.
[239:19.00] There we go.
[239:22.00] Then I'm going to go over to, again, the UNA array one.
[239:28.00] Get rebase dash I ref types.
[239:34.00] Again.
[239:38.00] Just drop all three of those.
[239:42.00] PM run test.
[239:43.00] Make sure everything's passing.
[239:45.00] Push it up.
[239:47.00] Get check out.
[239:50.00] Ref async compat.
[239:52.00] Get rebase off of UNA array.
[239:56.00] Oops.
[239:57.00] Get rebase abort.
[240:00.00] Rebase dash I so we don't get merge conflicts here.
[240:04.00] So this one.
[240:06.00] This one.
[240:08.00] This one.
[240:16.00] This one.
[240:18.00] This one.
[240:20.00] Fixed test for async functions.
[240:32.00] Hmm.
[240:34.00] Interesting.
[240:38.00] Ah, right.
[240:50.00] So I don't know exactly what this is doing here.
[240:53.00] This probably has to do with, let's see.
[240:58.00] We're not going to do the 4H.
[241:00.00] Instead we're going to do 4.
[241:01.00] So let's just bring that up to the top.
[241:04.00] And then as far as these two go, I have no idea what's different between them.
[241:08.00] Probably nothing.
[241:10.00] Oh, this one's async.
[241:11.00] Got it.
[241:14.00] Okay.
[241:15.00] I think I dropped something that shouldn't have been dropped.
[241:17.00] I think that's what happened.
[241:18.00] Get rebase dash dash abort.
[241:23.00] Okay.
[241:27.00] Oh.
[241:30.00] Okay.
[241:33.00] Okay.
[241:35.00] Okay.
[242:04.00] Where's that for loop stuff at?
[242:13.00] Nice.
[242:41.00] Let's see.
[242:49.00] Okay.
[243:12.00] What's this all about?
[243:17.00] How could this be possible?
[243:23.00] Oh, the test did not get updated back then.
[243:26.00] I see, I see, I see.
[243:29.00] So it didn't actually update the tests at that time.
[243:43.00] Okay, I'm just going to try this out and see how far it goes.
[243:49.00] Oops.
[243:51.00] Get rebase dash I.
[243:54.00] Okay.
[244:00.00] So.
[244:06.00] All right.
[244:09.00] It says.
[244:32.00] Okay, whatever.
[244:36.00] It seems to make enough sense.
[244:50.00] It's literally the exact same.
[244:52.00] Oh, except for it's let versus bar.
[244:57.00] Okay.
[245:01.00] That was it.
[245:04.00] All right, sometimes I'm just not sure where this is going here.
[245:14.00] Okay, now.
[245:25.00] Hmm.
[245:26.00] All right.
[245:27.00] So this is where both of these were modified.
[245:30.00] I understand what that's about.
[245:39.00] Run test.
[245:40.00] Test still run.
[245:41.00] Good.
[245:48.00] All right, fine.
[245:50.00] That seems great.
[245:53.00] Why does this have...
[245:56.00] It's really weird.
[246:02.00] All right, so now we got dash keys.
[246:05.00] And we just do a get log here.
[246:09.00] Update Mocha.
[246:10.00] Lazy install DevDevs.
[246:12.00] All right, so everything here should now be completely ready.
[246:24.00] Actually, get rebase dash dash abort.
[246:28.00] Get diff ref async compat.
[246:33.00] No difference.
[246:34.00] Okay.
[246:35.00] Then we'll do this.
[246:36.00] Get reset dash dash hard head 10 or so.
[246:41.00] Get rebase ref async compat.
[246:43.00] Okay.
[246:46.00] Get rebase abort.
[246:49.00] Oh, duh.
[246:50.00] Get resets dash dash hard.
[246:55.00] And then we're going to make it ref async compat.
[247:02.00] All right.
[247:04.00] So there we are.
[247:05.00] So now we got this.
[247:08.00] And now is where we rip it.
[247:12.00] So ref async.
[247:14.00] We're going to go ahead and grab what we have here.
[247:21.00] Sec 256K1.
[247:29.00] Get diff head.
[247:39.00] All right.
[247:40.00] We grab this in.
[247:43.00] Oh, we're going to need those tweak utils.
[247:45.00] Right.
[247:47.00] Okay.
[247:50.00] Let me just see.
[247:52.00] Let me expand this down by one.
[247:55.00] Okay.
[247:56.00] So I can just basically grab this whole thing.
[247:58.00] That's what we needed.
[248:03.00] Let's see.
[248:04.00] Get public key.
[248:05.00] Compressed key.
[248:06.00] Oh.
[248:07.00] Yep, yep, yep, yep.
[248:09.00] That looks good.
[248:13.00] The sign stuff, I'm not going to bring it over.
[248:16.00] I'm just going to delete it.
[248:17.00] That was unfortunately a lost cause.
[248:22.00] So with dash keys.
[248:28.00] Let's bring this back here.
[248:57.00] Okay.
[249:10.00] Okay.
[249:33.00] All right.
[250:02.00] So there's the private key tweak add.
[250:11.00] And then here's the point add scaler.
[250:17.00] Which is the public key tweak add.
[250:31.00] Compressed.
[250:35.00] Okay.
[250:38.00] This is going to be the tweak.
[250:50.00] Public key copy.
[251:08.00] Was that the whole tweak utils right there?
[251:10.00] And that's it?
[251:11.00] Okay.
[251:12.00] Let's add our dunzo.
[251:26.00] Public key normalize.
[251:30.00] To.
[251:48.00] Okay.
[251:49.00] Let's take a look at some of these PRs here.
[252:17.00] Wait, why are they all failing now?
[252:19.00] Dang it.
[252:20.00] What did I do?
[252:21.00] It worked locally.
[252:22.00] Oh.
[252:23.00] Mocha tasks aren't supported.
[252:24.00] Okay, that's fine.
[252:25.00] Is that the reason they're all failing?
[252:26.00] Okay.
[252:48.00] Okay, so it's just.
[253:06.00] Node 10 works.
[253:26.00] Okay.
[253:27.00] Okay, so what I was going to come here to take a look at.
[253:30.00] This version.
[253:32.00] And see the files changed and then take a look at.
[253:34.00] 6k1.
[253:38.00] How are you normalizing the private key?
[253:42.00] Do we normalize public key?
[254:06.00] That's to public key to public key.
[254:21.00] Bites.
[254:37.00] Okay.
[255:06.00] Okay.
[255:19.00] Rip outside and verify.
[255:22.00] No need.
[255:43.00] We can just have that at a different layer.
[256:12.00] Okay.
[256:26.00] Okay.
[256:54.00] Set browser.
[256:58.00] Crypto.
[257:00.00] False.
[257:26.00] Okay, fix.
[257:29.00] Set package.json.browser.crypto=false.
[257:39.00] Bundlers.
[257:55.00] Okay.
[257:59.00] So we're looking at here.
[258:02.00] Do we have the normalize?
[258:04.00] How is the key normalized?
[258:08.00] Basically, it's just this thing.
[258:19.00] Okay.
[258:46.00] All right.
[258:54.00] Bites.
[259:18.00] All right.
[259:29.00] We've got the normalize done.
[259:33.00] We've got the private tweak.
[259:35.00] We've got the normalize.
[259:37.00] We've got the public tweak.
[259:40.00] We've got the to public key.
[259:47.00] We're getting rid of verify.
[259:50.00] Because it's stupid.
[259:57.00] Is that it?
[260:00.00] Really?
[260:19.00] Npm install.
[260:21.00] Save dev.
[260:23.00] Dash incubator one here.
[260:26.00] Okay, Npm run test.
[260:33.00] Should be able to verify key signature.
[260:35.00] Nope.
[260:41.00] Absolutely not.
[260:42.00] That should go in the key library.
[261:04.00] Well, actually, hold on.
[261:06.00] Let me take this a little bit back.
[261:15.00] I do want to keep that test in there.
[261:17.00] But we're going to not expose that in the same way.
[261:21.00] So let me rethink this for a second.
[261:44.00] Okay.
[261:45.00] So here's what we're going to do.
[261:47.00] Again, I messed up.
[261:48.00] I was trying to do two things at once.
[261:50.00] I can only do one thing at once.
[261:52.00] If I only do one thing at once, I can only screw up one thing at once.
[261:55.00] See?
[261:56.00] See how advantageous that is?
[261:58.00] To just do one thing at once?
[262:01.00] Very advantageous.
[262:06.00] All right.
[262:07.00] Git checkout.
[262:10.00] I have HD key.
[262:14.00] I'm so excited to blow it all up.
[262:42.00] Okay.
[262:48.00] So same thing again.
[263:06.00] I actually don't know how signing works with this.
[263:09.00] Let's go ahead and take a look at it.
[263:13.00] No, I do.
[263:14.00] I do, because I did it over here.
[263:16.00] Okay.
[263:17.00] Let's take a look at the sign.
[263:19.00] So what we're going to do, though, is we're just going to treat signing as opaque.
[263:23.00] So the sign function should work both ways, but the tests have to change.
[263:30.00] Maybe.
[263:31.00] Or, I don't know.
[263:34.00] Okay.
[263:35.00] We'll put this in here as basically a -- this is going to be a debug thing for the tests
[263:47.00] specifically.
[263:48.00] That's what this is going to be.
[263:49.00] So we'll move it this way.
[263:51.00] We'll say, okay.
[263:54.00] We can have lib HD key -- well, we'll just put in our test tests.
[264:14.00] Oh, maybe not.
[264:42.00] Okay.
[264:49.00] So we'll put in our test tests.
[265:18.00] Let's see.
[265:47.00] There we go.
[265:48.00] So we'll just include this in here.
[265:53.00] And we will just move all of the signing into here.
[265:56.00] So we should be able to see that the signing still works.
[266:08.00] I'm going to replace HD key dot sign dot star with sign.
[266:36.00] Hmm.
[266:44.00] Why didn't it like this?
[266:45.00] Oh, because I put a five there instead.
[266:46.00] All right.
[267:14.00] And so what I actually need to do is we are going to HD key -- so this is going to come
[267:26.00] in as HD key like that and this is going to come in as HD key and we're going to do private
[267:44.00] key equals HD key dot get private key.
[267:49.00] There we go.
[268:02.00] So we'll just do that.
[268:22.00] HD key dot verify.
[268:45.00] Indeed, that is not something I had checked for.
[268:46.00] Full key sign.
[268:52.00] All right.
[268:53.00] Yay.
[268:54.00] And test pass again.
[268:55.00] Okay.
[268:58.00] And I can still rip all this out just as I wanted to.
[269:20.00] Sign.
[269:28.00] Verify.
[269:29.00] Sign.
[269:30.00] Verify.
[269:31.00] Okay.
[269:37.00] Maybe I should actually do this in two steps.
[269:43.00] Because right now everything works, right?
[269:52.00] This is going to be throw new error not implemented.
[270:15.00] Tells dot sign.
[270:22.00] Okay.
[270:24.00] Cool.
[270:25.00] So let's do this.
[270:27.00] Let's say test lib.
[270:31.00] What's different about package dot JSON here?
[270:39.00] Oh, dang it.
[270:43.00] Yeah, check out ref.
[270:47.00] Async compat.
[270:51.00] Npm install.
[270:55.00] Come on.
[270:59.00] There we go.
[271:27.00] Yeah.
[271:38.00] Oh, whoops.
[271:41.00] I actually don't want that.
[272:10.00] All right.
[272:35.00] Okay.
[272:36.00] Cool.
[272:38.00] All right.
[272:40.00] Cool.
[272:43.00] All right.
[273:07.00] Cool.
[273:34.00] Package dot JSON just changes that.
[273:39.00] Okay.
[273:40.00] That's fine.
[273:44.00] Get commit dash m and this is just going to be factor.
[274:03.00] Switch to mobile crypto.
[274:31.00] There we go.
[274:34.00] And then -- oh, let's go in here.
[275:00.00] All right.
[275:13.00] And commit dash m.
[275:18.00] Leave signing and verifying up to the ECDSA lib.
[275:39.00] All righty.
[275:45.00] Now let me see.
[275:48.00] Could the signing be opaque?
[275:50.00] Probably not.
[275:53.00] I'm going to just check and see.
[276:07.00] Actually, it would be interesting to see.
[276:09.00] Let's see what happens if we just let it be opaque.
[276:14.00] So forget all of this.
[276:27.00] Oh, it's just a sig, a hash, an HG key and verify ops.
[276:46.00] Yeah, that's what I was thinking.
[277:08.00] Yeah, okay.
[277:18.00] It's got extra bytes.
[277:34.00] And if we try to get rid of that, it's going to complain.
[277:40.00] I don't know.
[277:44.00] Let's see, when signing.
[277:55.00] There we go.
[277:58.00] Oh, and that's not going to work.
[278:02.00] I don't think.
[278:04.00] Because that's expecting -- it's expecting it to have the same signature every time.
[278:16.00] Oh, that's a -- that's interesting.
[278:22.00] Because I could have sworn -- let me check the package.json here.
[278:29.00] Which version this is? Yeah.
[278:32.00] I could have sworn that this version of secp -- whoops.
[278:53.00] Um...
[279:08.00] Random bytes.
[279:22.00] Random bytes.
[279:24.00] Extra entropy.
[279:28.00] Init sig args. See?
[279:39.00] So from sign, reseed.
[279:54.00] Okay, so init sig args, extra entropy.
[280:01.00] If it's not equals null.
[280:07.00] Oh, interesting.
[280:10.00] So...
[280:20.00] Oops, extra entropy.
[280:24.00] So that actually should be true. Well, I'm glad that I found that.
[280:28.00] Because that is actually going to be really important.
[280:32.00] What a lucky find. How fortuitous.
[280:52.00] Okay.
[281:02.00] Where are our sign ops?
[281:09.00] Note.
[281:17.00] Testing. Normally, we'd want this to be true.
[281:40.00] That's a little ill.
[281:47.00] Hold on.
[281:57.00] Expected string got boolean.
[282:24.00] Well, that's weird. Hold on. What's going on here?
[282:49.00] Oh.
[282:57.00] Oh, that makes sense.
[283:23.00] Okay. So here, extra entropy, util, random bytes, 32.
[283:31.00] Okay.
[283:36.00] Alright, so that works there.
[283:43.00] But then -- okay, let's go ahead and add that, because that's what we want.
[283:47.00] Let me go ahead and try this with the extra entropy, and then it should fail. Yes!
[283:54.00] And that's our first --
[284:02.00] Alright, we got the failure we wanted.
[284:05.00] Isn't that amazing?
[284:08.00] How often do you hear, "Yeah, we just wanted this to break."
[284:11.00] But it is indeed -- ah, this was a worthy find. I would have been -- I'm glad that I happened upon this, because I would have been confused, thinking that this was correct when it wasn't, because I could have sworn --
[284:27.00] Well, when I was looking through the code earlier, a few weeks ago, I guess I just thought that that was on by default.
[284:54.00] I think I just was a little bit confused by the "if" syntax being quite so wonkadoodle.
[285:03.00] And I remember fixing concat bytes, because I wanted the entropy to be there.
[285:08.00] Yeah, this is something that should just be turned on by default. You should have to turn it off.
[285:13.00] But we can get around to that later.
[285:17.00] Okay, so --
[285:23.00] Alpha entropy is null.
[285:41.00] Okay.
[285:49.00] Okay, sure. Explicitly set signature entropy null for tests.
[285:59.00] Okay.
[286:21.00] Move, assigning, assign, and verify.
[286:29.00] Okay.
[286:49.00] Okay.
[287:09.00] Okay.
[287:33.00] Okay.
[287:45.00] Okay, so we got that done. That's awesome.
[287:48.00] So all the tests are still running. What have we got left to do here?
[287:52.00] To really make me feel like I had a good night.
[287:57.00] That I'm worthy of the sleep that I'm being forced upon so shortly.
[288:06.00] Well...
[288:24.00] Dash keys, baby.
[288:27.00] That's what.
[288:44.00] Alrighty. We're switching to dash keys.
[288:50.00] Show me that ripety bipety.
[289:19.00] Okay.
[289:33.00] I should actually --
[289:37.00] I'll move that over to dash keys.
[289:48.00] Does that exist on dash keys?
[289:51.00] This is going to give me a major headache.
[290:01.00] Do not tell me.
[290:05.00] Oh, it's under -- okay. Alright. Alright, sorry.
[290:09.00] I was wrong. It was right.
[290:11.00] It's under utils.
[290:13.00] Now it's going to tell me utils doesn't exist on dash keys.
[290:21.00] Yes, it does.
[290:30.00] That's weird.
[290:59.00] I really don't care what the type of dash keys is.
[291:10.00] I've defined the type of dash keys, what, a bajillion times?
[291:16.00] Ugh.
[291:18.00] Alright, this is something that I want to leave to JojoBite to figure out.
[291:24.00] He's got that thing knocked right ways.
[291:33.00] We'll figure it out.
[291:37.00] We'll make him talk.
[291:49.00] Alright, that's --
[292:04.00] fix, export, utils type.
[292:33.00] Okay.
[292:46.00] If it compares colors to donuts, it does.
[293:15.00] Why did it not come through?
[293:17.00] Because it came through with the CLI and the CLI knew it was there, didn't it?
[293:21.00] I'll just take one more peek here.
[293:28.00] Typed off dash keys.
[293:33.00] I don't know.
[293:38.00] I've got to get started on GPT script.
[293:45.00] Spend a month on it.
[293:48.00] And never deal with TypeScript again.
[293:52.00] Have something that's fast, that makes sense.
[293:59.00] That'd be interesting. I wonder if I could spend a month on it.
[294:08.00] Um, okay. What was I doing?
[294:15.00] BS58, check. Dash keys, encode.
[294:44.00] Oh.
[294:54.00] Well, shoot, dang.
[295:07.00] The version info was here.
[295:36.00] Okay.
[296:04.00] Hmm.
[296:25.00] The BS58 check was a little aggressive.
[296:54.00] Okay.
[297:22.00] Okay.
[297:51.00] Okay.
[298:20.00] Let's try this.
[298:49.00] Okay.
[299:18.00] Okay.
[299:27.00] Let's try this.
[299:40.00] Okay.
[300:09.00] Okay.
[300:38.00] Okay.
[301:02.00] Okay, so encode key. There we go.
[301:05.00] That's what that was if I recall correctly.
[301:20.00] It absolutely does exist. Why is it telling me it doesn't exist?
[301:24.00] Why did I do all this type crap? Why? Why did I do it?
[301:29.00] Just to be told it doesn't exist.
[301:36.00] Okay, I'm going to do the weird thing here.
[301:43.00] I'm going to try to import.
[301:52.00] Let's see.
[301:59.00] Oh.
[302:04.00] Type import dash keys.
[302:22.00] What do you mean?
[302:27.00] What do you mean?
[302:29.00] It's clear.
[302:32.00] It's right here. It's right here.
[302:35.00] It's right here.
[302:45.00] What do you mean there's no exported member?
[302:51.00] There's the main. Main's right there.
[302:59.00] See, Ryan, this is the kind of stuff we got to put up with.
[303:03.00] It's the price of coding in JavaScript.
[303:11.00] It's right there. It's literally right there.
[303:16.00] Okay.
[303:31.00] Come on.
[303:51.00] Okay.
[303:54.00] Okay, so now it's happy.
[304:03.00] I just got to require the file directly for whatever weird reason.
[304:08.00] Wait, is it working again now?
[304:10.00] No. Now it's upset again.
[304:13.00] Okay. So I do that.
[304:30.00] It's absolutely 100% right here.
[304:34.00] It's right here.
[305:00.00] So screwy. Whatever.
[305:04.00] So wait, why is now utils there?
[305:11.00] But encode key is now not there.
[305:21.00] They're both right here.
[305:23.00] Encode key.
[305:24.00] Dash keys. Encode key.
[305:27.00] How is it telling me it's not there?
[305:29.00] How?
[305:31.00] What is wrong with you?
[305:54.00] All right. So we're going to have key info.
[306:23.00] Okay.
[306:42.00] Hmm.
[306:56.00] All right. So key buffer.
[307:04.00] Two bytes.
[307:06.00] Key info.
[307:10.00] Something or other.
[307:27.00] Oh, dang it.
[307:56.00] Okay, I'm going to have to find a better workaround for that at some point.
[308:03.00] So key.
[308:32.00] Okay.
[308:57.00] All right.
[309:26.00] Okay.
[309:45.00] What was that?
[309:49.00] Keyset.
[309:53.00] Private key.
[310:00.00] Interesting.
[310:02.00] Oh, so there is a way to tell from the version byte.
[310:11.00] I didn't notice that before, but there is a way to tell, apparently.
[310:23.00] Oh, right, right, right, right, right, right, right, right.
[310:25.00] Okay.
[310:26.00] So the compression byte.
[310:29.00] Is it the compression byte?
[310:37.00] Version.
[310:47.00] Let's see.
[310:58.00] So we've taken that.
[311:14.00] The version is key info dot version.
[311:29.00] 16.
[311:36.00] And this actually does not account for.
[311:40.00] So I need to have a to do T pub.
[311:51.00] All right, what am I doing here?
[311:53.00] I'm losing it.
[311:57.00] BS 58. Remember more BS 58 in here.
[312:16.00] Okay, cool. Well, that's good to know.
[312:20.00] We'll take that to the utils as well.
[312:30.00] Utils dot decode equals a sink function.
[312:50.00] All right, so these are not quite as streamlined as I would like.
[313:18.00] I don't know.
[313:43.00] Which is, which is, and so I'm mistaken about base 58 checking coding.
[313:49.00] Or is this thing? That's the question.
[313:54.00] Could be either.
[313:57.00] Wouldn't be the first time.
[314:03.00] 58 key, we need to make sure that we do, however.
[314:32.00] I kind of wish that I could do something.
[314:41.00] I can't remember what I'm thinking.
[314:44.00] All right, I'm going to move this over.
[314:48.00] Dash keys.
[315:08.00] Okay.
[315:31.00] What about the encode?
[316:00.00] Okay.
[316:29.00] All right.
[316:46.00] Okay.
[317:15.00] All right.
[317:36.00] So, I'm not expecting this to work.
[317:40.00] But I'm probably not in a state of mind to debug it.
[317:43.00] Cannot read properties of undefined.
[317:47.00] Oh, that's, that could be very simple.
[317:52.00] Could just not be returning.
[317:54.00] See, returning, returning, returning, returning.
[317:57.00] Always returning.
[317:59.00] Always returning he is. Never knowing why.
[318:22.00] Okay, let's see.
[318:28.00] 373.
[318:38.00] Ah.
[319:06.00] Oh, whoops.
[319:15.00] I also put in the glossary.
[319:18.00] I put the sequence in the wrong order.
[319:47.00] Okay.
[320:02.00] 58, check.
[320:30.00] So, this was wrong.
[320:44.00] Okay, compression.
[320:56.00] Ah.
[321:25.00] Okay.
[321:54.00] Swampy doodle that around.
[322:05.00] That's confusing.
[322:18.00] Affix docs.
[322:38.00] Okay.
[323:07.00] All right, let's see.
[323:22.00] Key length must be.
[323:51.00] Okay.
[324:19.00] What am I doing here?
[324:23.00] NPM run test.
[324:27.00] 74.
[324:30.00] Wait, is the version encoded in there twice?
[324:43.00] Let's see what happens if I just find the 78 here.
[324:53.00] Encode possibly should be 74.
[325:15.00] Ah, well, there we go.
[325:17.00] Okay, there's another one.
[325:39.00] Okay.
[325:41.00] Fix.
[325:50.00] Extended keys are 74 bytes, not 78.
[326:06.00] Extended.
[326:28.00] All right, let's see here then.
[326:35.00] All right, decode comes from dash keys, encode comes from dash keys.
[326:40.00] Although, really, it just needed the base 58.
[326:47.00] Well, yeah.
[326:56.00] I may be wrong about base 58 check.
[327:00.00] It may be that the version is actually at a higher level still.
[327:09.00] Base 58 check may only define the checksum.
[327:12.00] It may not define the structure of the data inside of it.
[327:17.00] So I'll have to figure that out.
[327:32.00] Public key normalize.
[327:35.00] Probably don't need that normalize stuff.
[327:47.00] Public key.
[328:03.00] All right.
[328:05.00] Well, it's kind of a big deal.
[328:31.00] All right, package.
[328:43.00] So feet is.
[328:57.00] I have to think about this.
[329:14.00] Hmm.
[329:39.00] Let me go back here.
[329:49.00] And I may also need to remove from the test matrix.
[329:57.00] Node 10.
[330:16.00] Node V10 from test matrix to old.
[330:45.00] Switch to dash keys.
[330:50.00] We need to do something about those types.
[330:57.00] Oops.
[331:25.00] Compare changes.
[331:40.00] Dash keys.
[331:43.00] Browser compatible.
[332:10.00] Okay.
[332:39.00] All right.
[333:04.00] All right, we got to remove.
[333:11.00] All the way back here.
[333:24.00] Sure.
[333:25.00] Remove node V10.
[333:31.00] Because new Mocha doesn't support it.
[333:58.00] Okay.
[334:27.00] Check out ref types.
[334:30.00] Rebase.
[334:37.00] Check out.
[334:41.00] Rebase ref types.
[334:45.00] Check out ref.
[334:48.00] Async.
[334:59.00] Check out ref dash keys.
[335:01.00] Rebase.
[335:05.00] Async.
[335:13.00] All right.
[335:32.00] So there's some things that we could, well, I want to, I still want to update the API.
[335:36.00] So now, now we're going to do the clean break.
[335:43.00] So I'm going to rename any of the methods that I want to.
[335:52.00] Get rid of sign and verify.
[336:07.00] Okay, git commit dash m.
[336:14.00] Remove sign.
[336:18.00] Verify.
[336:47.00] Wait a minute.
[336:58.00] Why is it failing?
[337:02.00] NPM run test.
[337:06.00] Everything's passing there.
[337:09.00] So why does it tell me it's failing?
[337:16.00] What environment thing is wrong here?
[337:45.00] Shouldn't mutate state.
[337:48.00] Okay.
[338:16.00] What version of node am I on?
[338:21.00] Can I go all the way down to 14?
[338:25.00] Looks like I might be able to.
[338:29.00] NPM install.
[338:34.00] NPM run test.
[338:37.00] Interesting.
[338:44.00] Whoa.
[338:47.00] That's because I need to republish.
[338:51.00] Duh.
[338:53.00] Because dash keys has a couple of bug fixes.
[338:56.00] Need to be applied.
[339:02.00] So how about we do this?
[339:03.00] How about NPM version pre-release.
[339:10.00] Git push tags.
[339:16.00] No.
[339:18.00] Hold on.
[339:31.00] Yes, git push tags, blah, blah, blah, blah, blah.
[339:36.00] And then here's my NPM key.
[339:41.00] All right.
[339:43.00] NPM install.
[340:10.00] Hmm.
[340:20.00] Hmm.
[340:49.00] Replacing all the things.
[340:50.00] Okay.
[340:58.00] Replaced by 12.
[341:12.00] Okay.
[341:14.00] Replaced by.
[341:32.00] All right, this one is replaced by.
[341:49.00] Wait.
[342:03.00] Okay.
[342:11.00] What is this about?
[342:18.00] So everything's failing.
[342:19.00] Great.
[342:22.00] Now tell me why.
[342:33.00] Okay.
[342:39.00] Well, that stinks.
[342:53.00] Cannot read digest of undefined.
[342:55.00] Hmm.
[342:59.00] I wonder if I can roll back the clock a few minutes because this was working and then I copied it over.
[343:12.00] Cannot read digest of undefined 156.
[343:19.00] Oh, yeah.
[343:29.00] We might.
[343:51.00] Reinstall all the latest tools here.
[343:59.00] All right, so this one.
[344:08.00] I'd have to go back and apply some of this.
[344:18.00] Let's see, what would I need?
[344:20.00] Not very much.
[344:22.00] I'm just saying, let me see.
[344:25.00] What is the cost on this?
[344:36.00] I think it's just the SHA-256.
[344:49.00] Crypto dot subtle dot digest.
[344:55.00] So.
[345:12.00] What?
[345:32.00] Let's see, fix.
[346:01.00] Okay.
[346:19.00] Let's see.
[346:48.00] Parts.
[347:12.00] Hmm.
[347:37.00] Hmm.
[348:06.00] Okay.
[348:26.00] 14D.
[348:55.00] Commit.
[349:05.00] Commit.
[349:21.00] Check for xprompt and xprove.
[349:34.00] Also, check some xpromption here.
[349:44.00] Expect xkeys to be 74, not 78.
[350:13.00] What are you talking about?
[350:42.00] Okay.
[350:57.00] Pre-release.
[351:01.00] All the things.
[351:21.00] Hey.
[351:23.00] I updated npm, so now I can use security keys in the browser.
[351:27.00] That's awesome.
[351:40.00] Okay, so.
[351:48.00] Update this version again, npm install.
[352:13.00] Okay, now I think all the tests will pass again.
[352:19.00] Let's see, let's do webby node at 14.
[352:25.00] And npm install.
[352:28.00] Location, global, all the things.
[352:41.00] Okay, run the tests.
[352:48.00] Cannot read.
[352:50.00] Okay.
[353:06.00] Oh, our good old HMAC friend, huh?
[353:26.00] Oh, weird.
[353:28.00] Here hashes an object.
[353:31.00] Huh, how strange.
[353:40.00] Okay, so let's take.
[353:43.00] We have HD key.
[353:48.00] And where is that.
[353:51.00] Okay, what are we trying to do right now.
[353:53.00] This one is HMAC SHA-256.
[353:56.00] Okay, so we can take this.
[354:22.00] Okay, 256.
[354:25.00] Okay.
[354:42.00] Okay.
[355:11.00] Okay, and then what was I doing here?
[355:21.00] Message.
[355:50.00] Okay.
[356:05.00] Okay, npm.
[356:08.00] Version pre-release.
[356:12.00] Tags, all the things.
[356:18.00] Wait.
[356:20.00] Oh, because I switched back to a different version.
[356:47.00] Okay.
[356:50.00] You know, I had this discussion with some people, some npm people.
[356:56.00] About how, you know, they ought to switch it from being in any format.
[357:03.00] Basically, they're using a weird format for the config file that is basically broken and doesn't work.
[357:10.00] As in, it actually has problems all the time.
[357:17.00] It doesn't parse correctly, it loses information.
[357:22.00] There's just a ton of problems with it.
[357:25.00] And I said, well, you know, just use YAML or JSON or whatever.
[357:29.00] Just switch it over to a standard format that'll just work.
[357:33.00] And they said, well, we can't do that because it'll break compatibility.
[357:36.00] Break compatibility with what?
[357:39.00] You break -- and then I pointed out, well, you all break compatibility with it all the time, which is why I'm having this issue.
[357:47.00] Is that you internally, you're not consistent with breaking compatibility about it.
[357:53.00] So just -- and, you know, it's extra dependencies because it's a special custom parser.
[357:59.00] It's got lots of rules that are special, that have evolved, you know, that's just specific to npm.
[358:05.00] And they could just run two in parallel, you know.
[358:09.00] They could just have a JSON version and they could have the old version.
[358:13.00] And they could support that for, you know, pretty much indefinitely.
[358:16.00] And you could just say, hey, edit the JSON version.
[358:19.00] That's the one that, you know, if both exist, the JSON version is the one that takes precedence.
[358:25.00] And you could backport that.
[358:28.00] You would have less code, you know, less custom crap.
[358:35.00] But whatever.
[358:37.00] What do you do?
[358:55.00] All right.
[358:58.00] Here we go.
[359:00.00] Hey, how's it going?
[359:02.00] I am so about to something or other.
[359:17.00] All right.
[359:18.00] Here it goes.
[359:22.00] npm run test locally.
[359:39.00] What the crap?
[359:49.00] Okay, I need to go back to this.
[360:11.00] Oh, no.
[360:13.00] Did this.
[360:23.00] Shems node crypto.
[360:32.00] Shems.
[360:43.00] Well, that's really odd.
[360:45.00] That's quite odd.
[360:59.00] That's incredibly odd.
[361:22.00] How?
[361:47.00] Okay.
[361:53.00] Okay, I can see that there's a Shems directory here.
[361:57.00] You all can see that, right?
[361:59.00] I can see here's files.
[362:03.00] Files has Shems.
[362:29.00] Let me just make sure here.
[362:32.00] Shems.
[362:43.00] That is correct.
[362:51.00] Oh, you know what, though?
[362:53.00] I needed this is okay because I actually needed both of these.
[363:22.00] Okay.
[363:51.00] Okay.
[364:03.00] So confused as to how that broke.
[364:06.00] New version of npm, I guess.
[364:09.00] Maybe we need to switch back to the old one to publish this.
[364:34.00] What was that?
[364:53.00] How is something going to fall in the middle of the night behind the desk while I'm sitting here?
[365:00.00] What is that?
[365:08.00] I don't know.
[365:12.00] Okay, well.
[365:14.00] This is really frustrating.
[365:16.00] All these little gotchas.
[365:20.00] Ah, you know what, though?
[365:22.00] We can get rid of this.
[365:24.00] Hold on.
[365:53.00] Wait, why is it going to have these on me?
[366:22.00] Okay.
[366:31.00] Cool enough.
[366:50.00] Run test.
[366:53.00] All right, so let me know that 14.
[366:58.00] All right, cool.
[366:59.00] There we go.
[367:05.00] Just for fun.
[367:06.00] Can we get down to 10?
[367:07.00] No, we can't.
[367:08.00] Can we get down to 12?
[367:37.00] Oh, look at all this.
[367:38.00] This is now.
[367:39.00] No, no, no, no, no, no, no.
[367:42.00] I was installing these globally.
[367:48.00] None of that is relevant.
[367:57.00] Oops.
[367:58.00] That needs to move back to save down.
[368:03.00] And then we need to be able to save dash keys.
[368:18.00] Oh, crap.
[368:47.00] All right, let's try again.
[369:11.00] NPM run test.
[369:14.00] That worked.
[369:15.00] Let me know that 12.
[369:18.00] NPM run test.
[369:21.00] Not quite.
[369:28.00] Ah.
[369:31.00] Yeah, I don't really want to go back and fix that.
[369:33.00] I'm going to call this one good.
[369:39.00] Cool.
[369:43.00] I'll go back to node 14.
[369:44.00] I'll call that good.
[369:55.00] Remove node v14 from test matrix.
[370:04.00] All right, there we go.
[370:05.00] This one should fully pass then.
[370:26.00] All right, I'm going to have to reconsider some pros and cons on this.
[370:30.00] I may backtrack on trying to have the node support.
[370:43.00] All checks passed.
[370:48.00] It's kind of annoying.
[370:50.00] And then you got all these little nitty gritty things.
[370:52.00] I don't think it's worth it.
[370:54.00] I thought, oh, yeah.
[370:56.00] It's just all we got to do is change this one little thing and then it's supported all
[371:00.00] the way back to node 10.
[371:01.00] And then we got to support a bunch of other little things.
[371:04.00] And then some other little things.
[371:06.00] Okay.
[371:07.00] We've reached the end of the other little things.
[371:10.00] 14 is good.
[371:15.00] And maybe with 1.0 I'll just strip out everything except for 18.
[371:19.00] I don't know.
[371:20.00] It just depends.
[371:21.00] But, hey, look at this.
[371:24.00] We've got to update the readme.
[371:27.00] We've got to do that for sure.
[371:34.00] But.
[371:37.00] Whoops.
[371:40.00] Let me see here.
[371:47.00] F dash keys.
[371:57.00] Now, there's a few other things we've got to do.
[371:59.00] But for the most part, HD key is good.
[372:04.00] Okay.
[372:05.00] So where does that leave us on our roadmap here?
[372:10.00] Oh, nope, not this one.
[372:17.00] Okay.
[372:18.00] So I think dash side is good.
[372:22.00] I don't think there's anything that we need to update on dash side anymore.
[372:25.00] If I remember correctly.
[372:28.00] Other than potentially minor renaming of things.
[372:34.00] Oh, yeah.
[372:35.00] We want to get rid of root request in favor.
[372:41.00] I think that's what one of these is, right?
[372:45.00] Okay.
[372:46.00] We've got to get dash TX in there.
[372:48.00] So dash TX with dash TX.
[372:55.00] I think I'm just going to say, yeah, dash keys.
[372:58.00] It's a thing.
[373:03.00] To have dependencies, base 58 check.
[373:07.00] Yeah.
[373:14.00] Yeah.
[373:15.00] This is going to be significantly better if we use dash keys and we avail
[373:19.00] ourselves to ripe MD.
[373:22.00] And just those convenience functions.
[373:25.00] Okay.
[373:26.00] Dash phrase.
[373:27.00] This one I think is already what it needs to be.
[373:34.00] It doesn't have any dependency.
[373:37.00] So, okay.
[373:41.00] So the full ecosystem is almost there.
[373:43.00] Dash HD.
[373:45.00] I still got to put some work in to publish it.
[373:48.00] And then, and then, and then dash TX.
[373:53.00] And then I actually want to get started on redoing dash wallet.
[373:58.00] Getting, getting this stuff integrated.
[374:01.00] But I think I need to go.
[374:03.00] I need to get dash TX first.
[374:05.00] First, finish up with dash HD.
[374:07.00] We got to update the readme.
[374:09.00] Got to update a couple of things.
[374:12.00] I got to get Georgia to help out with the type script.
[374:15.00] Import crap.
[374:22.00] I just don't understand.
[374:23.00] I put the types in the file.
[374:25.00] Why aren't the types in the file when somebody else imports them?
[374:27.00] I don't get it.
[374:29.00] Somebody please explain this.
[374:30.00] All right.
[374:31.00] Anyway.
[374:37.00] Okay.
[374:38.00] So Monday we'll have dash site.
[374:40.00] Dash phrase.
[374:42.00] Dash keys.
[374:45.00] Dash HD dash TX.
[374:46.00] These are the two that, this one, all of the crappy work is now done.
[374:53.00] All the tedium is over.
[374:56.00] The readme is not going to be the worst thing in the world.
[375:05.00] Just updating the readme.
[375:08.00] Not, not terrible.
[375:12.00] We're going to change the names of stuff.
[375:13.00] So we're going to change this from get private extended key to get XPriv.
[375:20.00] And get XPub.
[375:25.00] This is a property.
[375:26.00] It's going to stay public key.
[375:28.00] This is going to become get priv key.
[375:32.00] Wipe.
[375:37.00] I don't know about wipe.
[375:38.00] I don't even want that.
[375:53.00] I don't know that I have a use case for this.
[375:55.00] So I think I actually might just get rid of that.
[375:58.00] Derive.
[375:59.00] We need to expose derive and derive child.
[376:01.00] We need to update the examples with the Xumonic seed.
[376:16.00] Because this basically, this right here, all it is.
[376:19.00] There's no, there is no index.js.
[376:23.00] There is no dash HD.
[376:25.00] This is empty.
[376:26.00] This was, this was, all of, all of this is the bin.
[376:33.00] And so what we're going to be doing here is basically, basically this is going to become.
[376:43.00] We can just go ahead and do this now.
[376:44.00] This becomes dash HD CLI.
[376:50.00] And this becomes dash HD dot JS.
[376:58.00] [Music]
[377:01.00] [Music]
[377:04.00] [Music]
[377:07.00] [Music]
[377:10.00] [Music]
[377:13.00] [Music]
[377:35.00] So.
[377:40.00] That gets renamed.
[377:43.00] And then I'm going to say.
[377:50.00] GitHub on, on fork repo.
[377:58.00] He's just.
[378:18.00] All right.
[378:46.00] Cool.
[378:53.00] So we will go ahead.
[378:54.00] All right.
[378:55.00] We're un-forking this.
[379:12.00] I'm feeling pretty good about this.
[379:14.00] Check out main, get rebase.
[379:17.00] Push.
[379:19.00] Close that one out.
[379:46.00] Boom.
[380:04.00] Yeah, we need to.
[380:07.00] Get rid of repo crap.
[380:11.00] Okay.
[380:17.00] For parody, I would not, I'm not opposed to having a GitHub public key.
[380:25.00] That seems reasonable.
[380:33.00] We'll figure it out.
[380:34.00] All right.
[380:35.00] Well, it's been a good one.
[380:38.00] Oh, I am out.
[380:41.00] I will.
[380:43.00] I don't know when I'm going to wake up tomorrow.
[380:45.00] Today, whatever, but I'm out.
[380:47.00] Y'all have a good one.
[380:49.00] Catch you later.
[380:50.00] Adios.