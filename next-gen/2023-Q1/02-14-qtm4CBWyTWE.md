---
showLink: "https://www.youtube.com/watch?v=qtm4CBWyTWE"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Code Hangout: Next-Gen DASH Tools #16: Dash HD: Derive Wallet, Account, Keys"
publishDate: "2023-02-14"
coverImage: "https://i.ytimg.com/vi/qtm4CBWyTWE/maxresdefault.jpg"
---

## Episode Description

Code Hangout explores Dash HD wallet development, focusing on refactoring and improving an HD key library for cryptocurrency wallet generation and management.

## Episode Summary

In this extensive coding session, AJ O'Neill works on refactoring and improving a hierarchical deterministic (HD) wallet library for Dash cryptocurrency. He discusses the intricacies of HD wallets, extended public and private keys, and the challenges of creating a cohesive SDK for Dash. The stream covers topics such as API design, documentation updates, and the broader goals of creating lightweight, user-friendly cryptocurrency tools. AJ also touches on the differences between frontend and backend development, the importance of cross-platform consistency, and his vision for a more accessible and understandable Dash ecosystem.

## Chapters

00:00 - Introduction and Initial Setup

In this opening chapter, AJ O'Neill begins the stream by setting up his development environment and addressing some technical issues with his microphone. He briefly outlines the focus of the session, which is to work on Dash Incubator projects, specifically refactoring and improving a hierarchical deterministic (HD) wallet library for Dash cryptocurrency. AJ also mentions recent changes to the channel, including the addition of a weekly Dash update. This introduction sets the stage for the detailed coding work to come and gives viewers an overview of what to expect during the stream.

08:22 - Refactoring the HD Wallet Library

AJ dives into the core of the stream's content by beginning the refactoring process of the HD wallet library. He explains the recent changes made to the code, emphasizing how the refactoring has simplified the structure and made it more browser-friendly and fully typed. AJ discusses the importance of allowing errors to bubble up rather than being squelched, which improves error handling and makes it easier to determine if keys are generated correctly. He also touches on the differences between BIP32 and BIP44 standards, explaining how BIP44 is essentially a revision of BIP32 with requested changes incorporated.

16:35 - API Design and Documentation

This chapter focuses on AJ's efforts to design an intuitive API for the refactored library. He discusses the naming conventions for methods and properties, debating between terms like 'fromSeed' and 'deriveWallet'. AJ emphasizes the importance of clear and consistent naming across the SDK to make it more user-friendly for developers. He also begins updating the documentation to reflect the changes and new API design, explaining his thought process for structuring the usage examples and ensuring they cover different use cases.

28:08 - Exploring Wallet Standards and Ecosystem Challenges

AJ takes a step back to discuss broader issues in the Dash ecosystem, particularly regarding wallet standards and implementation across different platforms. He explores the concepts of extended public and private keys (XPUB and XPRIV), noting potential inconsistencies in how they're used across different wallets like Edge Wallet and Dash Core. This discussion highlights the challenges of creating a cohesive SDK in an ecosystem with varying implementations and standards.

51:54 - Finalizing API Structure and Usage Examples

Returning to the code, AJ works on finalizing the structure of the API and creating comprehensive usage examples for the documentation. He focuses on demonstrating how to derive wallets, accounts, and keys, ensuring the examples cover both common use cases and more specific scenarios. This process helps AJ refine the API design further, making decisions about method names and parameter structures to create the most intuitive interface possible for developers using the library.

82:08 - Discussing Development Philosophy and Future Plans

In this chapter, AJ shares his development philosophy, emphasizing the importance of readability and understandability in code. He discusses his approach to creating a cohesive SDK for Dash, explaining how he's breaking down complex cryptocurrency concepts into smaller, more manageable tools. AJ outlines his roadmap for future development, including plans for additional components like dashTx, dashWallet, and dashSite. He also touches on the differences between frontend and backend development, arguing against the concept of "full-stack" developers.

168:51 - Wrapping Up and Future Outlook

As the stream nears its end, AJ summarizes the progress made during the session and outlines the next steps in the development process. He discusses his plans to finalize the core components of the SDK, including dash-phrase, dash-keys, secp256k1, and dash-hd. AJ also mentions upcoming projects like CrowdNode and the development of user interfaces for various components. This chapter provides viewers with a clear understanding of the project's current state and future direction, setting the stage for upcoming development streams.

203:39 - Closing Remarks and Stream End

In the final minutes of the stream, AJ concludes the session by thanking viewers for their participation and engagement. He reflects on the benefits of explaining his work during the stream, noting how it helps him clarify his thoughts and potentially drive towards perfection. AJ mentions his upcoming presentation plans for the weekly Dash update and expresses his appreciation for the conversation with viewers. He ends by discussing the channel's upcoming ability to raid other streams once it reaches one month old, providing a glimpse into future community engagement plans.

## Transcript

[00:00] (scratching)
[00:02] (scratching)
[00:04] (scratching)
[00:07] (scratching)
[00:09] (scratching)
[00:12] (scratching)
[00:14] (scratching)
[00:16] (scratching)
[00:19] (scratching)
[00:21] (scratching)
[00:24] (scratching)
[00:26] (scratching)
[00:28] (scratching)
[00:31] (scratching)
[00:33] (scratching)
[00:36] (scratching)
[00:38] (scatting)
[01:01] (scatting)
[01:04] Hey, the mic is hot.
[01:17] Hot mic, hot mic.
[01:20] Watch out everybody, hot mic.
[01:22] ♪ Something to say ♪
[01:26] ♪ To set you off ♪
[01:27] ♪ Let you know now ♪
[01:29] ♪ Don't look the other way ♪
[01:32] ♪ So don't push your luck with me friend ♪
[01:37] ♪ I'm one step away from letting you know how to offend ♪
[01:42] ♪ I'm just a cowboy ♪
[01:46] ♪ Tryna wrangle my pride ♪
[01:49] ♪ I'm just a loud ♪
[01:52] (microphone feedback)
[01:55] (upbeat music)
[02:04] Oh, we still have the hot mic again.
[02:16] (upbeat music)
[02:18] (upbeat music)
[02:21] (upbeat music)
[02:24] (upbeat music)
[02:26] (upbeat music)
[02:29] (upbeat music)
[02:32] (upbeat music)
[02:35] (upbeat music)
[02:40] (upbeat music)
[02:47] (upbeat music)
[02:54] (upbeat music)
[02:59] (upbeat music)
[03:02] (upbeat music)
[03:27] (upbeat music)
[03:29] (upbeat music)
[03:40] (upbeat music)
[03:54] (upbeat music)
[03:57] (upbeat music)
[04:00] (upbeat music)
[04:02] (upbeat music)
[04:05] (upbeat music)
[04:07] (upbeat music)
[04:10] (upbeat music)
[04:12] (upbeat music)
[04:15] (upbeat music)
[04:18] (upbeat music)
[04:20] (upbeat music)
[04:23] (upbeat music)
[04:48] (upbeat music)
[04:51] (upbeat music)
[04:53] (upbeat music)
[04:56] (upbeat music)
[04:58] (upbeat music)
[05:19] (upbeat music)
[05:21] (upbeat music)
[05:29] (upbeat music)
[05:36] (upbeat music)
[05:44] (upbeat music)
[05:46] (upbeat music)
[05:49] (upbeat music)
[05:51] (upbeat music)
[05:54] (upbeat music)
[06:18] (upbeat music)
[06:21] (upbeat music)
[06:40] (upbeat music)
[06:42] (upbeat music)
[06:45] (upbeat music)
[06:48] (upbeat music)
[06:50] (upbeat music)
[06:53] (upbeat music)
[06:55] (upbeat music)
[06:58] (upbeat music)
[07:01] (upbeat music)
[07:03] (upbeat music)
[07:06] (upbeat music)
[07:08] (upbeat music)
[07:11] (upbeat music)
[07:13] (upbeat music)
[07:16] (upbeat music)
[07:19] (upbeat music)
[07:21] (upbeat music)
[07:24] (upbeat music)
[07:26] (upbeat music)
[07:47] (upbeat music)
[07:50] (upbeat music)
[07:53] (upbeat music)
[08:19] (upbeat music)
[08:22] - Well, hello, hello and welcome back.
[08:45] I'm AJ O'Neill and we're doing some live code
[08:47] on Dash Incubator work.
[08:50] As is always the case with this particular channel.
[08:55] Well, actually no, now we have the weekly Dash update.
[08:58] So there's that, there's that as well.
[08:59] That's another thing that's now going on on the channel.
[09:03] And the video's a bit jittery.
[09:04] Give me just one second to check into that.
[09:06] Okay, so the mic problem, fingers crossed,
[09:09] should be fixed by virtue of,
[09:12] I got a different device to plug in my monitors to
[09:17] and it has USB on it.
[09:21] And so I've got the mic now plugged into that
[09:24] while I'm still waiting for the USB hub to get here,
[09:27] the new USB hub.
[09:28] So hopefully, I've got my fingers crossed.
[09:31] I'm hoping this is it.
[09:32] I'm hoping it's not that the mic is bad
[09:34] 'cause I replaced the cable.
[09:35] Now I've replaced the USB hub.
[09:38] I haven't noticed any actual failures
[09:41] since plugging it into a different USB hub.
[09:45] So there's, that's hopeful.
[09:50] All right, and then it looks like USB hub
[09:55] is scheduled to get here tomorrow.
[09:58] So then I will plug in the rest of everything else
[10:02] and hopefully all of the problems that I've had
[10:04] in relation to connectivity will all go away
[10:08] 'cause I think they're all related to getting a great deal
[10:11] on this USB hub that turned out to not be
[10:13] such a great deal after all.
[10:15] All right, also, I'm not ready for Mountain Dew yet.
[10:20] Actually, I probably am ready for Mountain Dew now,
[10:22] but I'm drinking some sort of strawberry drink mix.
[10:25] It's kind of weird.
[10:26] And in terms of what we're working on today,
[10:30] there, so I think that this is pretty much
[10:37] completely refactored.
[10:38] I feel really, really good about,
[10:41] it's all browser-friendly code, it's all typed,
[10:46] and there was a couple of pieces that were complicated.
[10:51] And one piece I consider a bug
[10:54] because it basically, it just, it squelched an error message
[10:59] rather than letting the error bubble up
[11:01] so that it's more difficult to tell if a key
[11:05] was actually generated or not,
[11:08] or whether it was reused was the problem.
[11:12] So I feel pretty good about that.
[11:14] And I think that we're ready to make what are probably,
[11:18] what are hopefully the final adjustments to this,
[11:21] which is now that we've got everything as an object,
[11:24] let me bring this back over here.
[11:26] Now the idea is, well, let's take it a step back
[11:34] to the way that it used to be
[11:36] and give it some instance methods.
[11:38] So let me get in here.
[11:41] Oh, this says it's still open somewhere.
[11:43] Oh, it's open right there.
[11:44] Oops, let me grab that one instead.
[11:46] Bloop, bloop, bloop, bloop, bloop.
[11:50] There we go.
[11:54] Okay, so let's get out of here.
[11:56] All right, so right now,
[11:59] there was, I did want to give this another name,
[12:03] the From Seed and From Xpub.
[12:06] I don't remember which names I wanted to give it.
[12:08] I think I wanted to give it,
[12:09] I think I kind of wanted to go with the stringify and parse,
[12:15] but the problem is I don't like an A.
[12:19] Oh, what's up?
[12:22] So I don't actually have,
[12:24] I guess I should have that tag, but it's this one.
[12:27] Here you go.
[12:28] There's the discord.
[12:30] Welcome back, Exploding New.
[12:33] All right, so I'm looking at my sheet of paper here,
[12:36] and I'm just going to take a minute to consider these.
[12:41] One thing that I thought about that I think makes sense
[12:44] in this implementation is that when you derive an account,
[12:48] at the point that it's deriving the account,
[12:51] it should also have the Xpub and Xpriv keys ready,
[12:56] because it's not a lot of extra work
[12:59] and you're not going to be deriving accounts very often.
[13:02] So it's not on every derive it needs to go through the work
[13:05] of encoding the Xpub and the Xpriv,
[13:07] but whenever you derive an account,
[13:08] I think it should do that,
[13:09] because that's the layer at which those things should happen.
[13:12] And this library, again, is going to be more focused
[13:15] on BIP44 and less focused on BIP32.
[13:19] So BIP32 is what this library came from,
[13:22] and BIP44 is what we're actually trying to implement,
[13:26] which is basically just some more well-defined information
[13:31] around BIP32, which now I understand why BIP32
[13:36] was marked as unanimously disagreed upon
[13:42] or something like that, and BIP44 was accepted.
[13:45] It's because BIP44 is basically just a revision of BIP32,
[13:49] and the revision has the requested changes, essentially.
[13:54] Okay.
[13:58] (soft music)
[14:00] And I think from the perspective
[14:16] that this is not truly a JSON object, it's totally okay.
[14:21] Whoops, I don't like that music.
[14:27] I'm gonna, we're gonna skip this one.
[14:29] This one's a little bit too cray-cray.
[14:31] Oh, what was I saying?
[14:35] So from the perspective that something, something,
[14:38] something, something, oops, oh, come on, there we go.
[14:41] Oh, these objects aren't really JSON.
[14:45] They have, I mean, JSON is something
[14:47] that can be perfectly stringified back and forth,
[14:50] and these objects are not that,
[14:52] because they are primarily made of buffers.
[14:55] So if we go back to this create,
[14:56] we can pretty much get rid of the create function,
[14:58] (soft music)
[15:01] which I think what we might do instead
[15:04] is have not a create function, but rather,
[15:08] well, maybe a create function.
[15:10] I don't really know.
[15:11] I was thinking about having, you know,
[15:12] you create and you pass in the seed and then you,
[15:15] and then when you derive, it does the work.
[15:18] So it just kind of keeps the state,
[15:20] and then when you do the first derive,
[15:21] when you derive wallet, it will,
[15:25] (soft music)
[15:27] it will do the async stuff.
[15:29] So I thought about doing that.
[15:30] I'm not quite sure what the API for this should be,
[15:32] but I can work on the parts that I understand
[15:35] that I'm very confident on,
[15:36] and then I can go back and work on the other parts.
[15:38] Not to derail the stream,
[15:41] but I think it would really help having links
[15:43] to everything in your, in your panels commands,
[15:47] in your panels and commands.
[15:49] I don't know what you mean by panels,
[15:51] but yeah, go ahead.
[15:53] Tell me what links that you think there should be.
[15:56] So we do have,
[15:57] because the way that Dash works is very open-ended,
[16:02] there's not a lot of hierarchical structure.
[16:05] There is some, so Ryan is, is kind of more of a
[16:09] anti-disestablishitarianist.
[16:14] I don't know if that really does it justice,
[16:16] and Ryan will be, you know,
[16:18] leave a comment to figure out
[16:19] how you want to describe yourself.
[16:21] But this, this actually,
[16:22] this is a point where Ryan and I disagree,
[16:25] and it kind of, it bugs me.
[16:27] Ryan likes things to not have form or structure,
[16:30] or that's the way it comes off to me,
[16:32] because every time I,
[16:33] I suggest that we should have what I consider to be
[16:37] just the lightest layer of structuring,
[16:39] he kind of pushes back on it.
[16:41] And so we don't have an official,
[16:46] there is nothing official.
[16:48] There is no official Dash Incubator Discord.
[16:52] There is no official Dash Incubator,
[16:57] there's just, there's, there's not,
[16:59] I am strongly of the opinion
[17:01] that we need to have something that is,
[17:03] this is the brand.
[17:05] You know, whether you want to call it legal,
[17:07] or a legal structure, or not a legal structure,
[17:09] or an organizational structure, or not an organization,
[17:12] we need a brand and we need a place
[17:14] where people get in touch with the brand.
[17:17] And I may be misrepresenting Ryan's views,
[17:20] but he is the leader, whatever he wants to call himself,
[17:25] he is the leader.
[17:26] And I wish that he were a little bit stronger of a leader
[17:30] in some regards.
[17:31] I like a lot of the freedom and the loosey-goosiness,
[17:34] but I do want to say,
[17:38] okay, this is where you get in touch with us.
[17:40] This is the point of contact.
[17:42] This is what the logo is.
[17:45] This is the process for such and such.
[17:48] I would like more of that,
[17:49] but yeah, we'll have to, we'll have to figure it out.
[17:55] Twitch panels are customizable features
[17:58] that allow streamers to add images and text
[17:59] to their channel page to provide,
[18:01] are you directly quoting this from something?
[18:04] This seems a little too formal to be an ad hoc information.
[18:08] Typically located between the stream,
[18:11] yeah, I think you are,
[18:13] I think you are actually directly quoting this.
[18:15] You want to just give me the URL?
[18:16] Streamer schedule, social media links, about me.
[18:22] Panel provides brief description of the streamer.
[18:26] Okay, yeah, I think I know what this is.
[18:28] This is basically when I go to the kind of the homepage,
[18:31] it asks me to, if I could, you know, to add some things.
[18:34] Well, I will do this.
[18:39] I will give you the Discord command at least.
[18:42] I'll go into the reply commands
[18:43] and I'll add the Discord right now.
[18:45] So let's do create Discord and then message text is,
[18:51] let me see if I can, let me just grab it from here real quick.
[18:59] But this, so this is my Discord
[19:03] and then there is a link in that Discord to,
[19:08] I mean, there is a dash incubator channel in that Discord.
[19:13] (gentle music)
[19:15] Okay, so, oh, whoops.
[19:24] I accidentally just dropped all of the comments.
[19:27] My bad.
[19:30] Oh, whoops, and there's another thing going on.
[19:36] Sorry, hmm, I had not thought about this.
[19:41] Okay, there is another issue that we have here,
[19:45] which is that this is the wrong, hmm, hmm, dang it.
[19:50] Darned if I do, darned if I don't.
[19:57] Okay, I'm gonna need to group these items into BCB bots.
[20:04] There we go.
[20:08] And then I actually, I need to switch something real quick.
[20:11] Give me just a second.
[20:13] I'll make sure the chat comes back up correctly.
[20:15] So I need to switch over
[20:16] to the dash incubator scene collection.
[20:18] This is probably gonna,
[20:19] everything's gonna go goofy for.
[20:21] Okay, so now I need to take this one.
[20:30] Let me grab these links real quick.
[20:32] 'Cause basically I need to make sure
[20:35] that I swap back and forth
[20:36] and I'm gonna need to give these
[20:38] some sort of color grade or something
[20:40] so that I remember the difference between the two.
[20:42] 'Cause I'm trying between Streamlabs,
[20:45] or not Streamlabs, between Stream Deck.
[20:49] I'm trying to get my Stream Deck buttons
[20:50] to work across the channels,
[20:54] but the problem is that there's sub things.
[20:56] And I can do this,
[20:57] if I make everything one scene collection in OBS,
[21:00] then I think I can do this a little bit better
[21:03] because I can click on, for example,
[21:05] the dash incubator button
[21:08] and have it load dash incubator OBS
[21:11] and then have it turn on and off certain scenes.
[21:15] But it's still a little bit wonky as of right now.
[21:20] So give me just one second
[21:23] and I'm gonna get the chat working properly again
[21:25] 'cause I'm seeing the right chat
[21:27] and nobody else is seeing the right chat.
[21:28] This is the Beyond Code chat.
[21:29] So I'm gonna try to fix that.
[21:34] (keyboard clicking)
[21:36] And then I'm gonna have to have some sort of button
[21:39] to fix this.
[21:42] Okay.
[21:46] We're gonna switch back over to the Beyond Code.
[21:50] All right, there we go.
[21:56] And this one doesn't have that LUT applied either.
[21:59] That's okay.
[22:01] Delete me, oh.
[22:02] Oops.
[22:04] Yeah, that one says delete me.
[22:06] I'm gonna delete it.
[22:07] I just wanted to see what it was before I deleted it.
[22:10] Okay, so now I need to add another,
[22:13] basically I need to duplicate.
[22:15] Let's see.
[22:17] Okay, copy and then paste.
[22:23] I don't wanna paste a reference.
[22:25] I wanna paste a duplicate.
[22:26] I can't duplicate this.
[22:28] So 320 by 600.
[22:31] All right, I'm gonna go back to browser here.
[22:34] And this will be DI Restream Chat.
[22:39] And then we're gonna do 320 by 600.
[22:45] And we're gonna put it right like this.
[22:50] And then the real chat should start showing up.
[22:53] One day I'll figure out how to manage all this stuff.
[22:56] Okay.
[22:59] (typing)
[23:01] Okay, now if you do a chat message,
[23:15] it should show up.
[23:19] So here's the Dash Incubator Bots.
[23:23] We're gonna put this into the Dash Incubator Bot.
[23:29] And then we need to copy this one as well.
[23:31] This one's 800 by 600.
[23:33] I think it's just been scaled down.
[23:36] Okay, so give me a second here.
[23:38] So we're gonna do another browser source.
[23:40] And this is gonna be DI Streamlabs Bot.
[23:44] And this is gonna be 800 by 600,
[23:48] which is its default size anyway.
[23:50] And then we're gonna paste in the URL
[23:54] for the Dash Incubator one.
[23:57] And then we're gonna make this small.
[23:59] And then next time there's a sub or a follow,
[24:03] it should pop up right there.
[24:06] That should be okay.
[24:07] And then I'm gonna move this into the DI Bots folder.
[24:11] And then I'm just gonna have to have a multi-action.
[24:13] Thanks.
[24:14] Thanks for that test.
[24:16] So now I need to add a multi-action to the stream deck.
[24:18] So then when I press the Dash Incubator button,
[24:20] it will
[24:26] swappy do
[24:27] from between the two,
[24:31] which that is less complicated
[24:33] than having a whole bunch of buttons
[24:36] and having to switch between button profiles
[24:38] and blah, blah, blah.
[24:40] So I'm moving everything back to just one profile
[24:43] is what I'm saying.
[24:44] Okay, and I don't need that timers on
[24:46] and I don't need that BRB on.
[24:48] And then we do have, okay, good.
[24:51] The pixel mask is over here.
[24:52] I've been playing out with a couple new features,
[24:54] playing around with a couple new features.
[24:56] And then we don't need this one.
[25:00] That's not gonna be there.
[25:02] The pixel mask, that can stay there.
[25:04] That's my primary capture.
[25:06] Okay.
[25:10] All right, so let me just test something real quick.
[25:15] Make sure all of this is still working.
[25:17] That's still good.
[25:19] And that's still good.
[25:21] Excellent.
[25:22] All right.
[25:24] Do I have anything in the works as far as Twitch tipping?
[25:27] I am so not a real streamer.
[25:31] I'm just so a plebe.
[25:33] So I don't...
[25:39] We do have a plan to do some dashy things
[25:43] where you can, one, when the stream starts,
[25:49] there will be a QR code
[25:50] and the first person to scan it
[25:52] gets the monenes.
[25:54] And we could implement a QR scanner
[25:59] so I could make something
[26:01] so that if you want to send a tip,
[26:03] that the QR code is just down over there.
[26:08] Well, that way, over, over.
[26:11] Let's see if it, here.
[26:12] Yeah, you can kind of see my hand moving.
[26:14] You know, put it over in that corner
[26:17] or maybe up here over in this corner.
[26:21] We could do something like that.
[26:23] That would be interesting.
[26:30] I know Jojobite and I are both kind of interested
[26:32] in some of these tools,
[26:33] but not from an integration specifically with Twitch,
[26:36] but an integration with Dash Tools.
[26:38] No QR scanner needed with the Twitch Extensions API.
[26:46] Yeah, we can look into that at some point.
[26:50] I mean, you can tell me more, link me to stuff,
[26:52] especially if the link doesn't work through here,
[26:55] which sometimes I have to put on strict mode
[26:57] because occasionally I've been bombed by retards.
[27:00] I shouldn't call 12-year-olds retards.
[27:05] I mean, they're just teenagers,
[27:06] but you know, people doing dumb.
[27:10] And so, yeah, but feel free to drop those suggestions
[27:16] in the Discord and you could, if you wanted to,
[27:21] I bet Ryan would be willing to set up a bounty
[27:25] for you to go in and Twitchify us, right?
[27:28] So if you wanted to @Ryan in, so in that Discord link,
[27:33] now you should be able to do bang Discord
[27:35] to get the Discord to load like you were trying
[27:37] to do earlier to get that link.
[27:39] So if you want to join in on the Discord
[27:41] and then go into, it is the Dash Incubator AJ Squad,
[27:47] group, General Dash Incubator.
[27:50] If you plop in there and just @Ryan and say,
[27:52] hey, I want to Twitchify the Dash Incubator
[27:56] and set it up with all the stuff,
[27:57] I think that there's a good chance he would let you do that.
[28:04] So there's an idea.
[28:09] Okay, this one is not the one I want to look at.
[28:13] This is the one I want to look at.
[28:15] I think, let me just Git pull
[28:17] and make sure everything's good here.
[28:19] All right, dash HD dot JS.
[28:23] Okay, so let's go back to this create function.
[28:26] I need to make sure that all the types are updated and stuff.
[28:28] But look, look how simple this is now.
[28:30] Now these are just integers.
[28:35] This is an integer, this is an integer,
[28:37] this is an integer, this is a buffer,
[28:39] this is a buffer, this is a buffer.
[28:41] But now, this was not super apparent to me before,
[28:45] but after all this refactoring, now I know,
[28:47] hey, look, this is what a,
[28:50] an HD key is.
[28:54] It's just these things.
[28:55] That's it, that's all that's needed.
[28:57] You know, it's nice to be able to see it in simple form
[29:00] without all of the hoopla.
[29:02] So this is basically,
[29:06] I would say what we're kind of doing here,
[29:10] this is the create function, sure.
[29:13] This could be a more like a validate function.
[29:16] This is basically, this does nothing.
[29:18] We don't need a create function anymore
[29:20] 'cause now we understand exactly what this object is.
[29:23] What we could have,
[29:25] let's see, from,
[29:29] I kind of want to call this derive wallet.
[29:36] That's what I want to call this one.
[29:38] And so you give it a seed and you give it versions.
[29:43] (soft upbeat music)
[29:45] And you derive the wallet.
[29:48] And I kind of just want this to be more like this,
[29:56] where versions are optional because again,
[30:06] we don't have any other versions.
[30:07] The only versions that we have are for testing.
[30:11] So I do want to export that.
[30:13] However, I think that's actually kind of important
[30:16] that we should,
[30:18] we should export.
[30:24] I want to call these main net versions and test net versions
[30:31] and then get rid of all of this reference to Bitcoin
[30:40] because it's kind of confusing.
[30:42] If you were to go in this code,
[30:43] you might think that it has something to do with Bitcoin.
[30:45] It really doesn't have anything to do with Bitcoin.
[30:48] It is main net and test net.
[30:50] And you can have alternate test nets,
[30:52] but that's basically what it is.
[30:55] This is main net and test net.
[30:57] And I think that we actually ought to export these.
[31:10] Main net.
[31:10] That's the one thing that's nice about the create function
[31:20] is that this is done automatically.
[31:23] And I like that.
[31:24] I think that makes a lot of sense.
[31:26] So that makes the create make sense.
[31:29] All right, but now we need to figure out
[31:32] this test net stuff as well.
[31:34] And I'll have to go check and see because we had this,
[31:39] I think it was in the bit 44.
[31:40] Yeah, Ryan is R-I-O-N, like Ryan the lion.
[31:51] He's the dude.
[31:54] (soft music)
[31:57] Okay, now the five levels.
[32:12] And what am I looking for here is test nets,
[32:15] registered coin types.
[32:17] Dang it.
[32:21] This is not actually the right one.
[32:23] So I need to find the BIP that is X priv X pub.
[32:28] That's the BIP I need to find.
[32:30] Do we not have a BIP for this?
[32:54] (soft music)
[32:56] Okay, maybe it's defined in BIP 32
[33:02] and I didn't notice it before.
[33:03] Okay, test net, there we go.
[33:17] That's what I needed.
[33:19] (soft music)
[33:48] I think we could just drop versions.
[33:50] We could potentially put this out further.
[34:11] Let's see.
[34:13] (soft music)
[34:16] Where is versions actually even used?
[34:43] That's another question.
[34:44] Okay.
[34:48] (soft music)
[34:53] HD versions.
[35:02] Main net, X priv and X pub.
[35:09] (soft music)
[35:12] Test net, T priv and T pub.
[35:17] So I think they are anyway.
[35:21] (soft music)
[35:25], okay I need.
[35:53] Oh, all right, what's going on here?
[35:55] So Discord is now saying it detected a new mic,
[36:00] but it doesn't look like my mic actually stopped working.
[36:05] So is something else, what else is connected
[36:10] that it might think is a mic?
[36:12] Because I bet the USB hub just did its wonka doodle thing.
[36:21] Let's see here.
[36:22] Okay, well good.
[36:35] Audio has still not gone out the entire time
[36:38] since I switched the USB hub plug.
[36:43] So it's still good.
[36:45] All right, so we've got from extended key.
[36:46] I actually don't want,
[36:47] I do want to look at this a little bit further.
[36:50] (soft music)
[36:53] So I'm gonna derive the wallet from a seed.
[36:55] I don't know if that's quite.
[37:01] Drive wallets a tricky one.
[37:19] I guess.
[37:20] From seed makes sense.
[37:26] From extended key.
[37:30] And this one, I just want to rename it to X key.
[37:46] And I did want to change the HD from seed.
[37:49] I did want to change the function signature on this
[37:53] so that it actually is using,
[37:55] so we're gonna change this around a little bit.
[37:59] So these are gonna become prop, not param.
[38:02] And then this is going to be type def,
[38:07] not callback, and options.
[38:12] And then, whoops, what did I do?
[38:15] Okay, and then here.
[38:18] So this needs to become now HD from seed options.
[38:26] I'll just call that ops.
[38:28] And then it needs to have these two properties on it,
[38:36] which is seed bytes.
[38:40] Call that, we're getting rid of the word buffer.
[38:42] (upbeat music)
[38:45] Okay.
[38:49] From seed.
[38:55] From X key.
[38:59] (upbeat music)
[39:01] I think that we want that to be true by default, actually.
[39:15] And we want this to be main net by default.
[39:26] And we want this to be probably just X key by default.
[39:30] Ah, there we go.
[39:44] (upbeat music)
[39:46] Okay, versions equal.
[39:54] (upbeat music)
[39:56] Yeah, okay, good.
[40:02] (upbeat music)
[40:04] So I don't think that we need the skip verification.
[40:14] False or true.
[40:17] (upbeat music)
[40:19] I don't think we need the skip verification
[40:24] just seems kind of silly
[40:28] because I don't think there's any instance where we...
[40:33] I mean, this already has checksum bytes in it.
[40:44] So yes, it is possible to construct an extended public key
[40:48] or an extended private key that is wrong,
[40:50] but that's kind of not our problem.
[40:57] If you are using a tool that is generating bad keys,
[41:02] the likelihood that this is going to help catch it
[41:05] is really low because there's a lot of different ways
[41:09] to generate bad keys and I don't know.
[41:12] (upbeat music)
[41:15] I don't know.
[41:15] And it's not really verification.
[41:20] That's also the wrong terminology to use here.
[41:22] This would actually just be a normalized public key.
[41:27] And this is gonna happen here anyway.
[41:40] So basically what you're saying is
[41:43] you're taking a public key and you're plotting it
[41:45] on the graph to make sure it fits on the graph.
[41:47] That's what it means by verification.
[41:50] Is it just, it's just seeing,
[41:51] does this key plot on the graph, yes or no?
[41:54] And if you're, I don't know why the performance
[41:58] is important in this case.
[42:00] I don't know why this option was given,
[42:02] but yeah, I think we can basically say
[42:07] normalize public key is false.
[42:12] And then if normalize public key...
[42:23] (upbeat music)
[42:25] All right, then we're gonna do the same thing here
[42:43] that we did before.
[42:45] We're gonna create a type def
[42:49] and this is gonna be options.
[42:52] And then this is gonna become a defrom X key options.
[42:57] We'll just call it ops again.
[43:02] Get rid of all of these.
[43:04] These params become props.
[43:07] Oops, if I could spell.
[43:09] And then this is gonna become X key.
[43:18] (upbeat music)
[43:20] And there we go.
[43:24] Oh, whoops, add prop, not add props.
[43:32] (upbeat music)
[43:35], okay.
[44:02] Oh, from X key.
[44:05] So I've decided for my rationale on this,
[44:09] which good or bad, this is my rationale
[44:11] and I'm sticking with it.
[44:13] It's X key in a function name
[44:14] because it's short for extended key.
[44:17] Capital X, capital K, 'cause it's short for extended key.
[44:21] So it's actually two things put together.
[44:24] But as a property name, it's all lowercase X key
[44:28] because the property name is actually X key as one word.
[44:33] It doesn't stand for anything.
[44:36] So it's, that's kind of a, it's kind of a cop out,
[44:40] but it, because this just doesn't look good
[44:44] because it's too close to, whoops.
[44:47] It's the X looks more like a this by that.
[44:51] It doesn't look like an X.
[44:52] So in function form, it's capital X, capital K.
[44:58] But we wouldn't turn it into lowercase X underscore key.
[45:03] So this is where it's incongruent.
[45:06] But for the sake of readability, this is,
[45:11] I think it's pretty easy to argue.
[45:13] That's much more readable.
[45:14] Okay, so this TX ignore, do we still need that?
[45:26] It looks like we don't need that anymore.
[45:27] It doesn't look like it's a problem anymore.
[45:30] Okay.
[45:32] All right, we've got the TPRIV stuff going on here.
[45:41] (soft music)
[45:44] Canful version.
[46:01] Okay.
[46:08] (soft music)
[46:11] Oh, bother.
[46:15] It does have a zero.
[46:34] Okay.
[46:36] (soft music)
[46:38] Versions.private.toString.
[47:05] Public.
[47:05] There we go.
[47:19] Okay.
[47:33] (soft music)
[47:35] (computer beeping)
[47:38] (computer beeping)
[47:41] Let's see here.
[48:07] (soft music)
[48:10] I really don't like going with versions,
[48:17] but I don't know if I've got anything better to offer.
[48:22] Okay.
[48:37] (soft music)
[48:39] Just so we clean that up a little bit.
[48:41] Okay.
[48:53] (soft music)
[48:59] (computer beeping)
[49:02] Wait, didn't we already do this up here?
[49:29] I don't think we need to do that assert yet.
[49:31] Yeah, I think we can actually cut this one out.
[49:40] Let's put that there.
[49:53] Let's put this here.
[49:55] (soft music)
[49:58] But let's move that,
[50:13] move this assert out of the way in just a second.
[50:17] (soft music)
[50:20] All right.
[50:34] So we can get rid of this assert.
[50:39] There we go.
[50:40] 'Cause it's gonna be either.
[50:44] (coughs)
[50:46] Either a public key or a private key.
[50:49] And I think that this is wrong.
[51:04] Public key must be 33 bytes.
[51:08] (soft music)
[51:10] I think technically there was once an allowance
[51:26] for these larger keys, but we don't use them.
[51:30] And I don't like the idea of supporting them
[51:32] because it just adds confusion
[51:36] that nothing in the ecosystem actually works that way.
[51:39] At one point,
[51:45] X, Y pubs were allowed.
[51:50] One plus 64 bytes.
[51:54] But nothing in the ecosystem actually works that way.
[52:00] (soft music)
[52:03] (keyboard clicking)
[52:06] Okay, so that's simpler.
[52:20] Okay, cool.
[52:24] So we've got another thing here
[52:31] that I think is actually important
[52:33] to recognize and check out,
[52:35] which is that if,
[52:45] let's see.
[52:54] If 44 equals true, I wanna do this.
[52:58] (soft music)
[53:01] Or rather BIP 32 equals false.
[53:07] If not BIP 32,
[53:17] if depth,
[53:20] let's see, and it's gotta be,
[53:27] I forget what the depth has to be on these,
[53:30] but it's a specific number.
[53:32] If I think it's four, if depth is not equal to four,
[53:39] then.
[53:40] (soft music)
[53:44] (keyboard clicking)
[53:47] 'Cause this, deriving an X key should be for an account.
[54:03] (soft music)
[54:12] (keyboard clicking)
[54:15] Okay, so we just throw.
[54:21] X key should represent an account.
[54:36] (soft music)
[54:40] (keyboard clicking)
[54:43] With depth.
[54:51] Depth.
[54:55] (soft music)
[54:58] (keyboard clicking)
[55:01] All right, so that should not be a magic number,
[55:20] but should be,
[55:21] (sighs)
[55:26] should be better.
[55:28] Should be, should be specific.
[55:31] (soft music)
[55:33] I'll just put this here too.
[55:38] (soft music)
[55:40] (keyboard clicking)
[55:43] Right.
[56:03] (keyboard clicking)
[56:06] (soft music)
[56:08] Let's see.
[56:30] Depth 32.
[56:33] (soft music)
[56:35] (keyboard clicking)
[56:38] Allow non-account keys.
[56:47] (soft music)
[56:50] (keyboard clicking)
[56:53] Okay, so we got that in place.
[57:14] Let me go check.
[57:17] So this M is, I forget what it's for,
[57:20] but I think it's for basically the level of the mnemonic
[57:25] or the seed.
[57:26] And then let's see, depth.
[57:31] Where's depth increased?
[57:33] Depth is increased every time we derive.
[57:36] So we skip deriving for the top level M.
[57:42] (soft music)
[57:45] (keyboard clicking)
[57:48] And then we derive, what is it?
[57:56] Oops.
[57:58] Let's see.
[58:02] So level one.
[58:06] So this is depth of, is that depth zero or one?
[58:09] So this is where I get confused.
[58:12] Is this depth zero or is this depth zero?
[58:15] Technically, that should be either way is appropriate.
[58:21] M doesn't matter.
[58:23] Okay.
[58:23] So let me go take a look at this and see.
[58:29] I need another tool
[58:40] to compare against this, I think.
[58:42] Well, how was I doing this before?
[58:48] Hold on.
[58:49] We've got the CLI tool.
[58:50] Let me see, how is it doing?
[58:54] It is doing seed to X keys.
[58:57] (soft music)
[59:01] (keyboard clicking)
[59:04] And how did I do this?
[59:15] That's not what I wanted.
[59:22] I want path.
[59:25] (soft music)
[59:28] Zero dot X prove.
[59:54] (keyboard clicking)
[59:57] Oops, that's not what I wanted to do either.
[60:00] I wanted to run that in this case.
[60:03] (soft music)
[60:06] Hmm.
[60:19] (soft music)
[60:21] (keyboard clicking)
[60:48] So why is it griping?
[60:50] (soft music)
[60:52] 34.
[60:54] Let's see what's up on line 34.
[60:55] (soft music)
[60:58] Hmm.
[61:14] (keyboard clicking)
[61:18] (soft music)
[61:20] Console dot log.
[61:32] (soft music)
[61:34] HD key.
[61:36] (soft music)
[61:38] (keyboard clicking)
[61:41] Okay.
[61:53] So that was my doing, it looks like.
[61:55] Oh, I'd copied over.
[61:58] Got it.
[61:59] (soft music)
[62:02] Let's go, let's have it go back
[62:04] to the original version though.
[62:07] And I'll make these changes later.
[62:09] (soft music)
[62:11] Do we have a mnemonic to X pub?
[62:30] X proof?
[62:30] Yeah, we do.
[62:31] Okay, good.
[62:32] (soft music)
[62:35] (keyboard clicking)
[62:38] So M44, whoops, I need to do these in 12 quotes.
[62:48] 44, was it?
[62:52] Five.
[62:53] (soft music)
[62:56] Zero.
[62:57] (soft music)
[62:59] (keyboard clicking)
[63:02] All right, I didn't do anything special there, right?
[63:28] Reset.
[63:29] (soft music)
[63:32] (keyboard clicking)
[63:38] Derive.
[63:51] (soft music)
[63:53] And this is still HD key.
[63:57] So that's not our updated version.
[63:59] (soft music)
[64:01] Is it this way?
[64:19] Do we need to do this?
[64:20] (soft music)
[64:22] Derive is not a function.
[64:27] (keyboard clicking)
[64:30] Ah, simple enough.
[64:37] (soft music)
[64:39] I'm a little bit confused here.
[64:48] Wondering if, ah, yes.
[64:57] (soft music)
[65:25] (grunts)
[65:26] Okay, now let's try this.
[65:27] Great.
[65:31] And then I want to decode this
[65:37] and find out what its depth is, essentially.
[65:39] (soft music)
[65:42] (keyboard clicking)
[65:45] (grunts)
[65:59] Okay, depth.
[66:00] (soft music)
[66:02] (keyboard clicking)
[66:05] Zoo.xprev, zoo.0.xprev.
[66:19] (keyboard clicking)
[66:22] I should get the xpub as well.
[66:23] (soft music)
[66:26] Okay, so.
[66:30] (soft music)
[66:33] Then xprev to width.
[66:35] (soft music)
[66:37] Okay, depth is four.
[66:51] (soft music)
[66:54] Let me double check on that.
[66:58] (soft music)
[67:01] (keyboard clicking)
[67:04] That's odd.
[67:12] (soft music)
[67:14] (keyboard clicking)
[67:30] Where's depth?
[67:31] (soft music)
[67:34] Okay, this is weird.
[67:44] I must be editing a different file than what I'm...
[67:46] Ah, ah.
[67:50] Indeed, I am editing a different file.
[67:53] That is why it's coming out weird.
[67:57] Console.log, depth, private root.depth.
[68:02] (soft music)
[68:06] Okay, depth is three.
[68:09] (soft music)
[68:11] That's what it's at.
[68:14] (soft music)
[68:17] (keyboard clicking)
[68:20] And then where's that other console?
[68:31] Okay, htkey.
[68:34] (soft music)
[68:36] Okay, so that's not correct.
[68:44] So total depth is five.
[68:46] So the depth we should be looking at is depth of three.
[68:49] (soft music)
[68:52] And let me just double check that this makes sense.
[69:14] So this is zero, this is one.
[69:18] Oops.
[69:20] This is two, this is three.
[69:30] All right, that makes sense.
[69:31] Zero, one, two, three.
[69:33] Depth is three.
[69:34] That makes sense.
[69:35] (soft music)
[69:38] (keyboard clicking)
[69:41] All right, so this is the level that we're at.
[70:02] Okay, good.
[70:03] So that makes sense.
[70:04] So we can check the keys
[70:07] to make sure they're at the expected depth
[70:08] and we don't do something weird with them.
[70:11] (soft music)
[70:13] Okay.
[70:29] (soft music)
[70:32] Hmm.
[70:33] (soft music)
[70:36] All right, so we've got from X key.
[70:53] (soft music)
[71:00] From HDC, all right, so what have we done here?
[71:04] (soft music)
[71:07] We just tightened up these two so far.
[71:15] That makes sense.
[71:16] (soft music)
[71:18] (keyboard clicking)
[71:21] What is going on here?
[71:42] Oops.
[71:43] (keyboard clicking)
[71:46] (soft music)
[71:48] What's the ops for?
[72:02] (keyboard clicking)
[72:05] I don't know what ops is.
[72:06] (keyboard clicking)
[72:09] (soft music)
[72:12] All right, encode priv.
[72:25] (keyboard clicking)
[72:26] UN8 array.
[72:28] (keyboard clicking)
[72:29] Key bytes.
[72:30] (keyboard clicking)
[72:33] There we go.
[72:34] (keyboard clicking)
[72:35] Whoops.
[72:36] Oh, this needs to be able to have
[72:39] a version attached to it.
[72:42] We actually currently don't have that.
[72:46] (keyboard clicking)
[72:49] Hmm.
[73:02] So that's a to-do.
[73:04] (keyboard clicking)
[73:07] (soft music)
[73:10] All right.
[73:18] (soft music)
[73:20] Okay, and then we need to redefine
[73:24] a little bit about HD from seed options.
[73:29] (soft music)
[73:32] (keyboard clicking)
[73:35] Okay.
[74:02] And then here.
[74:03] (keyboard clicking)
[74:06] HD derive helper needs to be updated.
[74:20] (keyboard clicking)
[74:29] Actually, I'm gonna stash all these changes.
[74:32] (keyboard clicking)
[74:35] (soft music)
[74:38] (keyboard clicking)
[74:41] (soft music)
[74:43] (keyboard clicking)
[74:46] (soft music)
[74:48] (keyboard clicking)
[75:18] Okay.
[75:18] (soft music)
[75:21] (keyboard clicking)
[75:28] All right, good.
[75:36] So we got some basic type fixes
[75:38] that I think I actually wanna put in
[75:41] (keyboard clicking)
[75:43] before.
[75:45] (keyboard clicking)
[75:48] (soft music)
[75:50] (keyboard clicking)
[75:59] (soft music)
[76:02] Oh, I think I was supposed to do a dot there.
[76:21] I don't remember.
[76:22] (keyboard clicking)
[76:25] (soft music)
[76:27] I think it's supposed to be like that, object dot.
[76:37] (keyboard clicking)
[76:40] Whatever.
[76:40] (keyboard clicking)
[76:43] (soft music)
[76:46] Oops.
[76:56] (keyboard clicking)
[76:59] So this needs to be a unit eight array.
[77:03] (keyboard clicking)
[77:13] And this one needs to be, there we go.
[77:16] (keyboard clicking)
[77:21] Okay, and then what else?
[77:31] Nothing else.
[77:32] (keyboard clicking)
[77:35] (soft music)
[77:37] And then I'm gonna have a little bit of,
[77:52] yeah, I put the wrong thing for that.
[77:54] No big deal.
[77:55] (soft music)
[77:57] And then I actually like the way I set it better there,
[78:00] but whatever.
[78:01] (soft music)
[78:03] (keyboard clicking)
[78:06] Oh, whoops.
[78:14] (keyboard clicking)
[78:17] (soft music)
[78:20] Oh, whoops.
[78:47] (keyboard clicking)
[78:50] Okay, so if we look at just this now.
[79:04] (keyboard clicking)
[79:07] (soft music)
[79:10] What?
[79:27] (keyboard clicking)
[79:30] (soft music)
[79:32] I need to drop that, I think.
[79:40] (soft music)
[79:42] Okay, so let me, okay, let me fix this once more.
[79:53] Oh, I just fixed it.
[79:55] (soft music)
[79:58] (keyboard clicking)
[80:01] All right, git commit -m.
[80:23] (keyboard clicking)
[80:26] (soft music)
[80:29] Okay, let's push that up.
[80:41] And then you git stash pop again.
[80:43] No, please don't tell me.
[80:47] There's from X key.
[80:49] Okay.
[80:50] (keyboard clicking)
[80:53] (soft music)
[80:56] Wait, I'm a little confused here.
[81:10] (soft music)
[81:13] (keyboard clicking)
[81:18] (soft music)
[81:20] Okay, so I need to go back a little bit.
[81:29] Let me do this.
[81:31] We're gonna go here, we're gonna grab all these.
[81:35] Not a big deal.
[81:37] And we're just gonna do git rebase -i main.
[81:41] (soft music)
[81:44] (keyboard clicking)
[81:47] Simplify.
[81:49] (soft music)
[81:52] (keyboard clicking)
[82:07] (soft music)
[82:10] Okay, fix.
[82:33] (soft music)
[82:36] (keyboard clicking)
[82:39] I am, oh no, refractoraptor.
[82:51] All right.
[82:53] (soft music)
[82:55] I will give you the wave.
[83:03] (soft music)
[83:05] (keyboard clicking)
[83:08] There.
[83:12] (soft music)
[83:15] I have attited you.
[83:18] (soft music)
[83:21] (keyboard clicking)
[83:24] (soft music)
[83:26] (keyboard clicking)
[83:29] (soft music)
[83:32] Hmm, how far back does this go?
[83:59] (soft music)
[84:01] Interesting, I can go back pretty far.
[84:12] (soft music)
[84:14] All right, let's try taking it back one further.
[84:25] (soft music)
[84:29] Oh, it is exactly at the right place, cool.
[84:31] (soft music)
[84:33] Okay.
[84:51] (soft music)
[84:53], hmm.
[84:54] (soft music)
[84:57] (keyboard clicking)
[85:00] Hmm.
[85:24] (soft music)
[85:26] (keyboard clicking)
[85:29] Hmm.
[85:44] (soft music)
[85:47] (keyboard clicking)
[85:54] (soft music)
[85:56] Okay, so here, this is where we have the question of,
[86:04] do we want to say, derive wallet?
[86:07] (soft music)
[86:09] I think we kind of want to have.
[86:13] (soft music)
[86:16] All right, here's what we should do.
[86:22] (keyboard clicking)
[86:24] Purpose is going to be 44,
[86:27] and what is the official name for this?
[86:31] Is it coin or network or whatever?
[86:33] (soft music)
[86:35] Back to this one.
[86:46] (soft music)
[86:51] Okay, purpose, coin type.
[86:54] (soft music)
[86:56] (keyboard clicking)
[86:59] (soft music)
[87:02] (keyboard clicking)
[87:05] There we go.
[87:31] Check that out.
[87:32] (soft music)
[87:34] That's some awesome sauce.
[87:36] (keyboard clicking)
[87:39] Okay, what is it still upset about?
[87:54] (soft music)
[87:56] 407, oh, equals, that's what it doesn't like.
[88:02] (soft music)
[88:04] Okay, now I think I'm okay with calling it derive wallet.
[88:26] (soft music)
[88:28] (keyboard clicking)
[88:31] Because the wallet is really up to the point
[88:36] of the coin type.
[88:37] (soft music)
[88:40] And we could have a derive coin.
[88:51] (soft music)
[88:54] (keyboard clicking)
[88:57] Actually, I don't really wanna deal with that.
[89:02] If you wanna derive the coin, you just derive.
[89:05] You derive, yeah, so this, there we go.
[89:10] Derive wallet, and then we get a seed.
[89:13] We have the coin type and all that.
[89:21] (keyboard clicking)
[89:24] Derive path, okay, and then we get.
[89:29] (soft music)
[89:34] (keyboard clicking)
[89:37] Okay, well, maybe we actually can do this in this way.
[90:03] (soft music)
[90:05] Well, I guess it doesn't matter which way we do that.
[90:13] We can look at it either way.
[90:14] It's the same thing.
[90:15] Okay, so we're gonna be able to derive a path.
[90:17] Whoops, what is going on?
[90:20] And here.
[90:25] (soft music)
[90:27] (keyboard clicking)
[90:30] I'm supposed to add param, number, account.
[90:40] Okay, there we go.
[90:45] (soft music)
[90:48] (keyboard clicking)
[90:51] And then I can plop this here.
[91:18] And then I actually could do, I can type this.
[91:23] So this would be at callback, derive account.
[91:28] And then we can put the type on here
[91:35] and I can export that elsewhere.
[91:38] So we can just call this at type, derive account.
[91:43] Boom.
[91:45] (soft music)
[91:47] Use before it was defined.
[91:54] Brr, brr, brr, brr, brr, brr.
[91:56] Fine, we can move this down below.
[91:59] Tomato, potato, it's the same thing.
[92:01] Just to get that off my back.
[92:05] (soft music)
[92:13] (keyboard clicking)
[92:16] Okay.
[92:34] (soft music)
[92:36] (keyboard clicking)
[92:39] Hmm, I might just call this HD derive account
[92:57] and then put it down.
[92:59] Well, I guess either way it still goes in the same place.
[93:02] Okay, so this is gonna be a little bit unique
[93:03] in that it's going to return a type
[93:05] that has a method that nothing else has.
[93:07] (soft music)
[93:10] Or rather we're going to have a type that nothing else has.
[93:13] (soft music)
[93:15] (keyboard clicking)
[93:18] (sighs)
[93:37] (soft music)
[93:40] (keyboard clicking)
[93:43] And then we're gonna have the HD wallet.
[94:07] So, this is going to have HD derive key.
[94:12] (soft music)
[94:14] And it's also going to have...
[94:22] (soft music)
[94:25] Some sort of...
[94:32] (soft music)
[94:34] (keyboard clicking)
[94:37] Okay.
[94:39] (keyboard clicking)
[94:42] Oh, and we need to...
[94:51] Do we need to specify whether this is...
[94:56] (soft music)
[94:58] (keyboard clicking)
[95:01] We drive up to that point,
[95:13] but then when we get the XPUB...
[95:18] (soft music)
[95:20] I'm trying to remember how we do this.
[95:25] (soft music)
[95:28] (keyboard clicking)
[95:30] We derive the XPUB...
[95:32] Well, we don't derive.
[95:34] I guess...
[95:34] So, if we're a count...
[95:36] (soft music)
[95:39] Do we...
[95:42] (soft music)
[95:44] (keyboard clicking)
[95:50] All right.
[95:50] (soft music)
[95:53] Something like that.
[96:03] (soft music)
[96:06] (keyboard clicking)
[96:09] Okay, yeah.
[96:22] I think we can have an X...
[96:23] (soft music)
[96:25] XPUB.
[96:28] (soft music)
[96:30] Hold on.
[96:31] I gotta think about this.
[96:32] (soft music)
[96:33] Do we wanna derive it down one layer?
[96:35] (soft music)
[96:37] I think we also need a GET.
[96:42] (soft music)
[96:45] (keyboard clicking)
[96:48] (soft music)
[96:50] (keyboard clicking)
[96:53] (soft music)
[96:56] (keyboard clicking)
[96:59] (soft music)
[97:01] (keyboard clicking)
[97:04] (soft music)
[97:07] (keyboard clicking)
[97:10] (soft music)
[97:12] (keyboard clicking)
[97:37] This should probably be a GET, GET keys.
[97:41] (soft music)
[97:44] Okay, so I think the way that this is gonna work
[97:50] is that we're going to pull out...
[97:54] (soft music)
[97:56] (sighs)
[97:59] I'm just gonna...
[98:00] I'm gonna have to build a little bit and play a little bit.
[98:01] But I think the way that this works,
[98:03] if I'm understanding correctly,
[98:04] is we derive the account,
[98:07] and the account is a private...
[98:12] XPUB.
[98:20] We go one layer down
[98:23] to have what we would give.
[98:32] So, derive account.
[98:34] (soft music)
[98:37] (soft music)
[98:39] (soft music)
[98:42] (soft music)
[98:44] (soft music)
[98:46] (soft music)
[98:49] (sighs)
[98:50] Okay, which is the layer at which...
[98:53] So, that's hardened.
[98:55] And we don't wanna give away the one that's hardened.
[98:58] We wanna give away the one that's not hardened.
[99:01] (soft music)
[99:04] (soft music)
[99:07] So, I think the way that I've been doing XPUB keys
[99:11] might be wrong.
[99:13] So, I may have to transition my wallet,
[99:17] the one that I built.
[99:20] I think I might be off by one layer of indexes.
[99:30] (soft music)
[99:33] Because the keys that I wanna give away...
[99:39] Actually, this is one where I don't know
[99:42] how the other tools in the ecosystem are doing this.
[99:45] I don't know of any other tools in the ecosystem
[99:49] that are actually using XPRIVs and XPUBs.
[99:51] I think that EdgeWallet is.
[99:53] Let me take a look at EdgeWallet real quick.
[99:55] Let me see if I can find that.
[99:57] (soft music)
[99:59] (soft music)
[100:01.92] Let's see.
[100:17.50] (soft music)
[100:19.92] (soft music)
[100:48.96] I wonder if I can go in the app somewhere
[100:52.08] and get access to the XPRIV and XPUB.
[100:55.72] (soft music)
[100:58.36] View XPUB address.
[101:00.14] (soft music)
[101:02.56] Interesting.
[101:09.40] (soft music)
[101:11.82] Uh-oh.
[101:18.76] (soft music)
[101:21.00] This doesn't look right.
[101:22.24] So at least EdgeWallet is not compatible
[101:28.44] with what I'm doing here because EdgeWallet,
[101:30.64] instead of using XPUB and XPRIV,
[101:35.24] it's using...
[101:36.36] I think it's using DarkP and DarkS is what it looks like.
[101:44.16] And that's not right.
[101:47.36] (soft music)
[101:49.78] Uh-oh.
[101:54.60] I mean, we can fix that later.
[101:56.08] But I don't think that there's any reason
[102:01.32] for us to be using Dark.
[102:06.16] I'm pretty sure that's not what anybody else is using.
[102:08.12] Hold on, let me...
[102:09.84] (soft music)
[102:12.92] (humming)
[102:15.08] (humming)
[102:27.70] (keyboard clacking)
[102:32.90] (keyboard clacking)
[102:35.90] (keyboard clacking)
[102:46.20] (soft music)
[102:55.48] (keyboard clacking)
[102:58.48] (keyboard clacking)
[103:01.48] (soft music)
[103:19.46] (keyboard clacking)
[103:28.46] (keyboard clacking)
[103:31.46] Let's see.
[103:49.08] Let me post this over here as well.
[103:55.30] (soft music)
[103:57.72] (humming)
[104:02.68] (keyboard clacking)
[104:09.68] (soft music)
[104:15.42] (keyboard clacking)
[104:18.42] Okay, well, we'll find that out.
[104:29.56] And if I have to go change it, it's not that big of a deal.
[104:32.88] I mean, we've got everything.
[104:35.08] I do have to...
[104:36.22] There are some changes that we'll have to make it through,
[104:39.20] but it's not that big of a deal.
[104:42.04] I don't think we're using dark P and dark S.
[104:44.28] And I would guess it'd be
[104:47.20] DRKP for public and DRKS for secret, but I don't know.
[104:52.20] Maybe it would be DPRV.
[104:57.16] I don't know what the...
[104:58.40] Just keep an eye out for any feedback I get back on that.
[105:10.36] Okay, all right.
[105:11.20] So that aside,
[105:13.20] let me get back to thinking about the types
[105:15.96] of how this is gonna work here.
[105:17.52] Okay.
[105:22.90] Good keys.
[105:29.96] All right, so an account partial,
[105:33.90] and then we're gonna have to have basically the same thing.
[105:38.28] (upbeat music)
[105:40.86] But then we're gonna have HDXKeyPartial.
[105:49.64] (upbeat music)
[105:52.22] (keyboard clicking)
[105:55.22] And that's just gonna have an XKeys.
[106:18.46] Okay, I think this will be right.
[106:21.10] (upbeat music)
[106:23.68] I wish I could see what the path is on that.
[106:27.54] I probably can't.
[106:28.58] I probably can't.
[106:30.34] I can probably go in here.
[106:32.74] Well, I mean, they're so...
[106:34.68] I just don't think these things are very, very much used.
[106:37.18] Let me try opening up Dash Core,
[106:40.26] because I think that my Dash Core
[106:42.40] has been converted to HD keys.
[106:44.02] I don't know how I can get an HD key out of Dash Core.
[106:47.08] (upbeat music)
[106:49.66] But let me go ahead and bring it over here.
[106:56.38] I'm gonna look up some documentation here.
[107:03.76] (upbeat music)
[107:06.34] (keyboard clicking)
[107:09.34] Yeah, XPUB.
[107:24.80] XPUB.
[107:27.22] (upbeat music)
[107:36.02] XPUB from Bitcoin Core.
[107:37.72] That'll probably be about the same.
[107:40.74] (upbeat music)
[107:43.32] Oh, no.
[107:47.26] We might have an incompatible...
[107:50.34] It may be the Dash Core actually uses
[107:53.14] hardened BIP32 the whole way through.
[107:57.38] It might be old enough to not use.
[108:02.34] 'Cause Dash Core is not something that Dash built.
[108:05.70] Dash Core is a fork of Bit Core,
[108:10.70] the old, nasty, dirty, ugly Bit Core
[108:14.74] with a handful of modifications.
[108:16.48] And I'm hoping that part of this whole,
[108:23.42] the broader spectrum here of this tools,
[108:26.62] this Dash tools stuff,
[108:28.98] is to have every piece of Dash Core independent
[108:34.04] in code that is easy to read
[108:36.36] and doesn't have a lot of hoopla around it.
[108:38.92] So that somebody could go in and,
[108:41.24] I mean, what I wanna see is I wanna see Dash Core die.
[108:44.80] Both the JavaScript library and the C++ code.
[108:48.70] I just wanna see it dead.
[108:50.24] It is old, it is crufty.
[108:52.64] I guess it works, but it doesn't work well.
[108:57.80] It's not composable.
[108:59.04] It doesn't follow the Unix philosophy.
[109:00.40] There's no way to use it in a sensible way.
[109:05.08] It's just a giant monolith, and that's all it is.
[109:07.64] And it's not useful as a reference implementation.
[109:10.80] It's not useful, it's terribly difficult,
[109:15.48] not difficult, it's not as difficult to use,
[109:17.40] it's just cumbersome to use.
[109:19.40] Just, ah.
[109:20.24] Okay, and of course it's gonna take years to load
[109:27.28] 'cause that's how it is.
[109:29.20] But I would, the future I'm hoping for
[109:34.20] is fresh, lightweight, easy to use, easy to debug tools.
[109:39.04] That's what we're doing here.
[109:41.20] Okay, so that aside, we've got a count partial.
[109:46.20] And we could, at the top level, have,
[109:51.56] we could derive from seed,
[109:56.96] we could derive all the way from seed
[109:59.04] down to anything.
[110:03.76] We can derive from seed to a specific key,
[110:06.36] we can derive from seed to a wallet.
[110:09.68] Let me see if there's any way for me to,
[110:13.96] if I open up the console,
[110:15.28] I'm gonna try command line options.
[110:17.76] Let's see.
[110:20.04] I don't see any command line options.
[110:24.64] No, that's for opening.
[110:26.68] That's not for using it, okay.
[110:28.48] Create wallet, open wallet,
[110:35.36] close wallet, backup wallet,
[110:38.88] open wallet configuration file,
[110:42.00] change passphrase, console.
[110:44.68] Okay, so I'm gonna open up my console on the other screen.
[110:49.80] And one thing that it did do, I thought,
[110:53.40] maybe it doesn't, was I thought it gave help.
[110:57.00] And so as you type, it helps you know what you can do.
[111:00.72] But I'll just do, I'll just type help.
[111:03.80] Okay, and then let's see.
[111:06.92] I'll bring it on my big screen
[111:14.28] so I can see it from top to bottom.
[111:16.60] So network mining,
[111:19.80] Evo dash control blockchain.
[111:24.80] Let's see if I could just get
[111:28.96] dash core help.txt.
[111:38.32] Yeah, there's no,
[111:48.68] there doesn't appear to be,
[111:49.60] and I'll just check with our G.
[111:51.16] X pub.
[111:54.20] Yeah, I just wanna do case insensitive.
[111:59.96] X private now.
[112:02.36] Extended, nothing.
[112:06.16] Okay, so there's nothing in the help
[112:08.24] about how this uses an HD wallet.
[112:12.40] So my guess is, well yeah, I mean,
[112:16.40] I think, I don't think there are any tools out there
[112:18.52] that use the HD wallet.
[112:19.72] I don't think that's a thing that's actually,
[112:21.72] I think the edge is probably the only thing
[112:23.24] that actually uses an HD wallet.
[112:24.92] I don't think I've seen anything else do it.
[112:29.36] Well, actually, hold on.
[112:33.40] Let me open up the dash wallet too.
[112:35.56] (soft music)
[112:37.96] I think on the mobile phone it does to some degree.
[112:53.16] So I'll just continue forward with the caveat
[112:56.32] that I do need to talk to some people
[112:58.96] to confirm at what layer we expect these
[113:03.20] X priv and X pub keys to be,
[113:05.40] and that I may have to swap a doodle
[113:11.40] the way that my wallet software works,
[113:14.60] because my wallet software may not be doing
[113:19.60] what I want it to do.
[113:22.60] I think I'm off by one layer of depth.
[113:29.84] Okay, so let's go back to this though.
[113:32.88] All right, so what do we got here?
[113:34.72] And I am gonna have to take a bio break fairly shortly.
[113:38.80] (soft music)
[113:42.16] (keyboard clacking)
[113:46.00] (keyboard clacking)
[113:49.84] (keyboard clacking)
[113:52.84] (keyboard clacking)
[113:55.84] I think I may want this one
[114:22.16] to be called derive account.
[114:23.56] 'Cause we're gonna have the seed.
[114:29.76] Oh no, I'm not really sure.
[114:46.40] (keyboard clacking)
[114:49.40] Okay, the point is this can derive an account.
[114:54.84] What?
[115:03.12] (soft music)
[115:11.52] (keyboard clacking)
[115:14.52] (keyboard clacking)
[115:17.52] I'm very confused about this.
[115:40.92] Oh, it doesn't need to be HD.
[115:43.84] Okay, I don't know if it should be HD.
[115:46.56] All right, we're gonna leave it as such for now though.
[116:04.64] 'Cause this is at a lower layer.
[116:08.48] (soft music)
[116:10.88] (keyboard clacking)
[116:13.88] Okay, so, ooh, this one's a tricky one.
[116:33.36] Because...
[116:34.64] Ah, temporal dead zone with let, ah!
[116:43.00] Maybe we can just call it account key.
[116:58.40] (keyboard clacking)
[117:01.40] Ooh.
[117:13.00] So, account to X key.
[117:21.52] (keyboard clacking)
[117:24.52] (soft music)
[117:26.92] (keyboard clacking)
[117:29.92] (keyboard clacking)
[117:32.92] Okay, let me just think about this
[117:57.72] at the simplest level here first.
[118:00.36] I'm getting a little ahead of myself.
[118:01.76] All right, so we got an account key.
[118:03.56] And to the account key,
[118:12.04] we want to assign a couple of functions.
[118:14.48] (keyboard clacking)
[118:17.48] (soft music)
[118:19.88] We want to have a derive XProve.
[118:33.04] (keyboard clacking)
[118:36.04] A get XProve.
[118:40.32] (keyboard clacking)
[118:43.32] And then the same thing with the XPUBs.
[118:46.20] (keyboard clacking)
[118:49.20] Okay.
[118:52.48] All right, so what is that actually going to mean?
[119:05.40] (keyboard clacking)
[119:14.92] So, this is an XProve key.
[119:16.64] (keyboard clacking)
[119:19.64] (soft music)
[119:22.04] (keyboard clacking)
[119:25.04] So, what was that serialize at?
[119:52.12] (keyboard clacking)
[119:55.12] Maybe we should just leave this at the top level
[120:00.80] and let that be that.
[120:02.08] (keyboard clacking)
[120:05.08] (soft music)
[120:07.48] I think we should.
[120:24.32] (keyboard clacking)
[120:27.32] That simplifies that quite a bit.
[120:32.40] (keyboard clacking)
[120:35.40] Well, maybe not.
[120:50.52] (keyboard clacking)
[120:53.52] (soft music)
[120:55.92] (keyboard clacking)
[120:58.96] (keyboard clacking)
[121:02.00] (keyboard clacking)
[121:05.04] (keyboard clacking)
[121:08.04] (keyboard clacking)
[121:11.04] And then what do we call this?
[121:37.04] This is the internal, external.
[121:39.52] We can't call it purpose,
[121:41.28] but I don't like calling it internal, external.
[121:43.68] Let me see if in the spec it's got a better name for it.
[121:46.68] Change.
[121:48.52] I don't like calling it change.
[121:51.44] (keyboard clacking)
[121:54.44] Okay, public derivation is used at this level.
[122:06.60] (keyboard clacking)
[122:09.60] Yeah, all right.
[122:12.44] (keyboard clacking)
[122:15.44] So it has to go down at least one,
[122:27.52] at least one level more.
[122:32.68] (keyboard clacking)
[122:35.68] (soft music)
[122:38.08] Count key.
[122:43.36] (keyboard clacking)
[122:47.12] Count key.
[122:48.32] (keyboard clacking)
[122:51.32] And then it's no longer derived child.
[123:03.68] Yeah, it's coming up on that time for me too.
[123:05.96] (soft music)
[123:08.36] Should've had one before I started.
[123:14.64] Bio break.
[123:15.56] (soft music)
[123:18.48] (keyboard clacking)
[123:21.48] (soft music)
[123:23.88] All right, so we're gonna have a sub-purpose.
[123:50.76] (keyboard clacking)
[123:53.76] I'm trying to think.
[124:01.52] How do we want to use,
[124:05.32] an XPIV should be tied to an account.
[124:11.76] True or false.
[124:14.36] It should be tied to an XPIV,
[124:20.76] an XPIV should be created with a non-hardened.
[124:25.76] So I'm just gonna make some notes to myself here.
[124:35.88] XPIV should be non-hardened.
[124:40.32] (keyboard clacking)
[124:43.76] XPIV should be able to generate a non-hardened.
[124:48.76] Able to generate keys.
[124:51.36] If we say these two things are true,
[124:59.24] then that means that an XPIV is at the sub-purpose level.
[125:04.24] (soft music)
[125:07.36] (keyboard clacking)
[125:10.36] Which should be zero.
[125:28.24] (soft music)
[125:31.76] (keyboard clacking)
[126:01.60] Ah, what did I do?
[126:03.12] (soft music)
[126:05.52] (keyboard clacking)
[126:08.52] Okay.
[126:32.60] (soft music)
[126:35.00] (keyboard clacking)
[126:38.00] So we don't have a path there.
[126:45.64] (soft music)
[126:48.04] I'm trying to think about how would I want to use this.
[127:02.24] (soft music)
[127:04.64] 'Cause I don't really want a count.
[127:10.80] I pretty much always want to go straight down
[127:14.04] to the XPIV.
[127:16.52] (soft music)
[127:18.92] (keyboard clacking)
[127:21.92] This almost needs like a two XP, would we ever?
[127:28.12] (soft music)
[127:30.52] (keyboard clacking)
[127:33.52] I have to make some choices that there may have to be
[127:41.84] another release of this to challenge or undo.
[127:46.12] But I just have to make the choices
[127:48.00] 'cause I don't actually know what the right choice is.
[127:51.76] (soft music)
[127:54.16] (keyboard clacking)
[127:57.16] (soft music)
[127:59.56] All right, public derivation.
[128:12.72] (soft music)
[128:15.12] (keyboard clacking)
[128:18.12] (soft music)
[128:20.64] (keyboard clacking)
[128:23.64] (soft music)
[128:28.52] (keyboard clacking)
[128:33.92] (soft music)
[128:47.12] (keyboard clacking)
[128:50.12] So I think we may need to have
[129:06.72] a create X key that does this.
[129:15.44] (soft music)
[129:17.08] That might make sense.
[129:18.52] 'Cause I don't want all this stuff nested down in here
[129:21.20] where it's potentially confusing.
[129:24.28] (soft music)
[129:26.68] And I think I do wanna split these out
[129:32.12] into actually two functions.
[129:33.92] One that is from XPIV, the other one that's XPub,
[129:42.80] from XPub, because I don't want it to be possible
[129:46.64] to return an ambiguous type.
[129:49.20] And you know going in, you know what it is.
[129:53.56] (soft music)
[129:55.96] Okay, from X key.
[130:12.44] Yeah, I agree about the Beyond Code bootcamp intro.
[130:16.12] I just keep on forgetting to do that.
[130:19.72] Also that means I need a different button.
[130:22.00] (groans)
[130:24.08] But yeah, what do you say we put the Dash logo up on Fiverr
[130:31.16] and just tell them to copy that same logo roll?
[130:36.16] Thoughts?
[130:38.68] (soft music)
[130:41.08] Let's see, yeah, I would have a,
[130:47.40] I would just need to put a Dash button on my stream deck
[130:52.52] and copy the same key sequence essentially.
[130:56.32] It'd be nice if there was a meta button
[131:01.24] that when I pushed it, it Dashified all the other buttons.
[131:05.48] (sighs)
[131:07.48] (soft music)
[131:15.52] Let's see.
[131:16.36] ♪ I'm hoping for something to say ♪
[131:29.20] ♪ Set you off, let you know ♪
[131:32.28] ♪ Now look the other way ♪
[131:35.60] ♪ Don't push your luck with me ♪
[131:38.52] Let's see, do I still have these hooked up?
[131:41.16] ♪ I'm one step away from letting you know ♪
[131:44.08] Okay, so that one's still hooked up.
[131:46.44] ♪ Man, I'm just a cowboy ♪
[131:50.20] ♪ Tryna wrangle my blood ♪
[131:52.16] Hmm.
[131:53.00] ♪ I'm just a loud man ♪
[131:56.04] ♪ Who's got something to hide ♪
[131:58.56] (sneezes)
[132:00.96] Dust or something.
[132:02.88] ♪ Eyes on the floor, looking for power ♪
[132:07.68] ♪ So I can't be ignored ♪
[132:11.24] ♪ I'm hoping for something to say ♪
[132:16.24] ♪ To let you know I'm afraid ♪
[132:19.68] ♪ Don't look the other way ♪
[132:23.76] ♪ Want me to be your friend ♪
[132:28.24] ♪ Can you love me in the ice too ♪
[132:33.24] ♪ I'm just a cowboy ♪
[132:37.32] ♪ Tryna wrangle my blood ♪
[132:40.04] ♪ I'm just a loud man ♪
[132:43.08] ♪ Who's got something to hide ♪
[132:45.84] ♪ I'm just a coward ♪
[132:49.04] ♪ Keep my eyes on the floor, looking for power ♪
[132:53.68] Okay, so we're gonna move all this down into
[132:57.84] ♪ One breath, one hand, hold me back from the wind ♪
[133:02.84] ♪ One breath, one hand, hold me back from the wind ♪
[133:09.52] ♪ So let me say what I need to say ♪
[133:12.60] ♪ I don't think that I'll need much more ♪
[133:15.40] ♪ I don't believe in fate ♪
[133:17.00] ♪ I don't believe that love can erase ♪
[133:19.32] ♪ What he said in James four ♪
[133:20.96] ♪ He says that you're gonna ignore those who are proud ♪
[133:24.72] ♪ Well you can't ignore me friend ♪
[133:27.32] ♪ And all this hope that I feel yet's in the sounds ♪
[133:30.44] ♪ And I'm thinking you're liking the end ♪
[133:34.00] Dang it, how do I want to do this?
[133:35.60] ♪ Something to say ♪
[133:38.20] The layering, the layering, Duke, the layering.
[133:40.56] ♪ I won't let you know, now look the other way ♪
[133:44.44] ♪ So don't push your luck with me friend ♪
[133:49.44] ♪ I'm one step away from letting you know ♪
[133:54.36] ♪ How to offend, I'm just a cowboy ♪
[133:59.36] ♪ Trying to win your mind ♪
[134:03.04] (soft music)
[134:05.44] (soft music)
[134:08.80] (soft music)
[134:11.20] (soft music)
[134:13.60] (soft music)
[134:16.00] (soft music)
[134:18.32] (soft music)
[134:20.72] (soft music)
[134:22.96] (soft music)
[134:25.36] (soft music)
[134:27.76] (soft music)
[134:30.16] (soft music)
[134:32.48] (soft music)
[134:34.80] (soft music)
[134:37.12] (soft music)
[134:39.52] (soft music)
[134:41.92] (soft music)
[134:44.32] (soft music)
[134:46.72] (soft music)
[134:48.16] Let's see.
[134:49.00] (soft music)
[134:51.42] (soft music)
[134:53.84] (soft music)
[134:56.26] Whoops.
[135:16.42] (soft music)
[135:18.84] (soft music)
[135:21.88] Did I just call that git pub by mistake?
[135:24.20] (soft music)
[135:26.62] Where did it go?
[135:35.92] (soft music)
[135:38.34] (soft music)
[135:46.96] (soft music)
[135:49.38] Where did it go?
[135:55.42] (soft music)
[135:57.84] Oh, git X key, it became git X key.
[136:12.92] But it should have been X.
[136:16.58] Okay, I see what happened there.
[136:18.26] (soft music)
[136:20.68] Okay, it makes more sense.
[136:28.54] (soft music)
[136:30.96] Maybe this shouldn't be much as git as two.
[136:41.42] (soft music)
[136:43.84] I think that actually is more clear
[136:56.50] and makes for less likely to be ambiguous
[136:59.70] in the documentation.
[137:00.74] Okay.
[137:03.62] (soft music)
[137:06.04] (soft music)
[137:08.46] All right.
[137:13.22] (soft music)
[137:15.62] Well, it's a little bit early to be taking a break,
[137:21.26] but I do need to take a bio break
[137:22.70] and I need to just kind of let this ruminate for a minute
[137:25.50] with where I'm at right now and kind of see,
[137:30.06] 'cause I think, well, I'll just finish up
[137:33.74] with the documentation here.
[137:36.12] And then we need to take it back into some testing.
[137:39.86] So there's the install and then usage.
[137:44.76] So we need to update the usage.
[137:52.04] Let's update the usage to what I think
[137:59.40] that this is gonna look like.
[138:00.44] And I think this is actually gonna be really helpful.
[138:02.88] So -hd.deriveWallet,
[138:07.88] and then you're gonna be able to give it, whoops,
[138:10.88] seed.
[138:16.48] So I'm gonna say -phrase.
[138:30.44] -phrase.toSeed.
[138:35.44] Let words equals zoo, zoo, zoo, zoo.
[138:43.60] So two and three and wrong.
[138:50.10] (upbeat music)
[138:52.68] This one has two seed, yep.
[139:15.58] Oh, and it needs the salt.
[139:17.04] (upbeat music)
[139:19.62] Secret salt.
[139:36.22] I'll just call it secret.
[139:45.74] (upbeat music)
[139:48.32], so I kind of think derive account should be,
[139:56.26] (upbeat music)
[139:58.84] So I kind of think derive account should be accessible.
[140:20.82] I don't know if it should only be accessible at this level,
[140:24.52] but I kind of feel like that's where it's got the most oomph.
[140:29.10] Because, well, I don't know.
[140:32.84] I mean, I guess if we have a wallet object,
[140:34.48] we can derive accounts from it many times.
[140:37.16] That kind of doesn't make sense.
[140:39.12] So drive account zero, let xpriv equals account.derivexpriv
[140:51.20] zero, let keys equals xpriv dot,
[140:56.20] let's say xkey, let xpriv equals xkey-hd.to xpriv.
[141:05.84] (upbeat music)
[141:08.42] All right, let's see, get keys.
[141:31.22] (upbeat music)
[141:34.80] Okay, so I guess,
[141:35.80] there should be a get keys and a get address, maybe.
[141:54.90] (upbeat music)
[141:57.48] (keyboard clicking)
[142:00.48] (upbeat music)
[142:03.06] (keyboard clicking)
[142:06.06] (upbeat music)
[142:08.64] (keyboard clicking)
[142:11.64] Can we call it use?
[142:38.96] (upbeat music)
[142:41.54] Zero equals perceive, one equals change.
[142:50.64] (upbeat music)
[142:54.84] (keyboard clicking)
[143:01.36] (upbeat music)
[143:03.94] I don't know if this is right or wrong,
[143:11.66] but I'm kind of imagining this.
[143:13.56] (upbeat music)
[143:17.06] (keyboard clicking)
[143:20.06] Hmm.
[143:37.98] (upbeat music)
[143:40.56] (keyboard clicking)
[143:43.56] (upbeat music)
[144:12.68] So the question is,
[144:14.72] (upbeat music)
[144:17.30] Hmm.
[144:37.90] (upbeat music)
[144:41.32] (keyboard clicking)
[144:44.32] I think we'd maybe call this use.
[144:53.52] (upbeat music)
[144:56.10] (keyboard clicking)
[144:59.10] Hmm, is this how it boils down?
[145:19.72] (upbeat music)
[145:22.30] (keyboard clicking)
[145:25.30] (upbeat music)
[145:27.88] (keyboard clicking)
[145:55.44] All right, so this is basically,
[145:58.18] one way to look at it.
[146:04.72] (upbeat music)
[146:07.30] (keyboard clicking)
[146:10.30] A typical use where the wallet will be used
[146:34.26] with multiple accounts
[146:38.10] and each account will be used for several keys.
[146:44.66] There's addresses.
[146:53.78] (upbeat music)
[146:56.36] So this is kind of the golden example.
[147:03.22] (upbeat music)
[147:05.80] A one-off where...
[147:11.96] (upbeat music)
[147:15.06] Where...
[147:15.90] (upbeat music)
[147:18.50] (keyboard clicking)
[147:21.50] (upbeat music)
[147:24.08] (keyboard clicking)
[147:27.08] (upbeat music)
[147:29.66] (keyboard clicking)
[147:32.66] (upbeat music)
[147:35.24] (keyboard clicking)
[147:38.24] (upbeat music)
[147:40.82] (keyboard clicking)
[147:43.82] Oops.
[147:59.98] (keyboard clicking)
[148:03.34] (keyboard clicking)
[148:06.34] I don't know if this is what I actually wanna have it as,
[148:14.54] but...
[148:15.38] (keyboard clicking)
[148:31.30] Something like this.
[148:33.26] (keyboard clicking)
[148:36.26] Maybe parse XPRIV.
[148:41.50] (keyboard clicking)
[148:44.50] Okay.
[148:53.92] (keyboard clicking)
[148:56.92] (keyboard clicking)
[148:59.92] I guess we're gonna use to, we should use from.
[149:15.82] That makes sense.
[149:16.80] (keyboard clicking)
[149:19.80] (keyboard clicking)
[149:22.80] Okay.
[149:47.00] (keyboard clicking)
[149:49.12] (keyboard clicking)
[149:51.92] So I do wanna support this use case of a quick one-off.
[149:54.92] (keyboard clicking)
[149:57.92] Which is that.
[150:00.58] (keyboard clicking)
[150:03.58] This could be fun.
[150:17.44] This could be very boring.
[150:18.52] That's true.
[150:19.42] Hey, just me.
[150:20.26] How's it going?
[150:21.08] I am, I'm, I'm just kind of,
[150:25.56] it's probably more on the boring side.
[150:26.84] I'm just kind of wrapping my head around
[150:29.36] how to work with this library
[150:34.36] that I've been refactoring and rebuilding.
[150:40.22] It's a, it's a cryptocurrency wallet generator,
[150:45.36] hierarchical wallet generator library.
[150:48.38] And I'm trying to figure out what the,
[150:54.62] kind of the main use case is for it,
[150:58.62] so that I expose the right methods.
[151:00.30] And so I'm just doing a little bit of documentation.
[151:01.78] I'm, I'm thinking I'm about to take a break
[151:03.90] so that I can kind of re,
[151:06.96] just, just kind of let my brain sit on it for a while
[151:09.02] now that I've been back in the code again.
[151:10.94] Cause I am, I'm in,
[151:13.10] I'm in it at a point where the,
[151:16.16] the bulk of the code,
[151:18.24] the code is mostly complete
[151:19.56] and I'm down to some final decisions of,
[151:22.92] should it be like this or like that?
[151:25.22] Let's see.
[151:37.60] M445.
[151:38.44] M445.
[151:39.28] And then 0, 0, 0.
[151:51.48] So here's an HD key.
[152:08.36] And from that,
[152:11.60] thinking, let me do this.
[152:31.94] (keyboard clicking)
[152:34.94] (keyboard clicking)
[152:38.90] Ow.
[152:39.74] (keyboard clicking)
[152:42.74] (keyboard clicking)
[152:45.74] Let's see.
[153:09.58] (keyboard clicking)
[153:12.58] (keyboard clicking)
[153:14.62] X key.
[153:15.78] (keyboard clicking)
[153:18.78] Maybe down here at this level.
[153:23.14] And then I could say,
[153:26.68] (keyboard clicking)
[153:29.68] I want to, I want to allow deriving a path.
[153:35.44] (keyboard clicking)
[153:39.44] (keyboard clicking)
[153:42.44] Okay.
[153:50.52] (keyboard clicking)
[153:53.52] This is going to be a string.
[154:03.08] This is going to be a string.
[154:04.58] (keyboard clicking)
[154:07.58] (keyboard clicking)
[154:10.58] Okay.
[154:27.02] (keyboard clicking)
[154:30.02] So we also want a way just to get,
[154:34.94] let's see, from the seed.
[154:37.38] So I don't want to derive a wallet.
[154:39.12] (keyboard clicking)
[154:41.70] I might really just want a from seed method.
[154:45.66] (keyboard clicking)
[154:48.66] So you're making a billet yourself wallet,
[154:57.88] not a coder program myself.
[154:59.66] Is a wallet made for a specific purpose
[155:01.50] needed for some specific use cases on platform?
[155:04.14] (keyboard clicking)
[155:07.14] A billet yourself wallet.
[155:11.18] (keyboard clicking)
[155:14.58] So let's see.
[155:16.50] (keyboard clicking)
[155:19.50] So the wallet, it's a little bit confusing terminology
[155:29.26] because there are things that were semi-standardized
[155:33.48] at different times a decade ago.
[155:36.62] And the words don't all, they're not congruent.
[155:41.18] And so one of the broader thing I'm doing here
[155:43.54] is working on a set of tools that are smaller tools.
[155:47.02] So each tool can be used independently
[155:49.74] and they each can be used as reference implementations.
[155:52.78] So you don't need to have the full everything or nothing.
[155:57.78] You can say, well, if I need to just understand this piece
[156:02.94] and work with this piece for some tool,
[156:05.26] you have just the tools that are for that.
[156:07.90] So particularly in the browser use case,
[156:10.78] you're not bringing in megabytes of JavaScript.
[156:14.82] You're bringing in just a few kilobytes
[156:16.90] for the things that you need.
[156:18.34] So this is a tool for,
[156:24.56] so the wallet from a user perspective
[156:29.48] is just a collection of 12 words and then a secret.
[156:34.10] But it seems that in our ecosystem,
[156:36.46] the secret is typically set to an empty string.
[156:39.02] But that's what a wallet is.
[156:42.86] A wallet is nothing more than 12 words and a secret.
[156:47.58] And I don't know if we are using the de facto secret
[156:51.68] because the documented secret is Trezor, all caps.
[156:56.68] This is what is used in all the documentation,
[157:01.98] all the fixtures, all the tests, it's Trezor, all caps.
[157:05.86] So I haven't looked in our mobile wallet
[157:08.62] to know under the hood what we're using.
[157:10.94] My understanding is that we're actually,
[157:13.46] Dash Core is just an old junky piece of crap
[157:17.54] called Bit Core with a little bit of rebranding
[157:20.78] and some colors changed.
[157:22.38] And it has a few extra functions implemented.
[157:26.10] But it's actually so old that from what I understand,
[157:29.86] it doesn't actually use the wallet spec.
[157:32.28] But that can't be right because it seems like
[157:37.10] it is synonymous between mobile and this,
[157:42.10] but there's no way to inspect what's going on
[157:44.64] with the wallet as far as Dash Core goes.
[157:49.02] I think that I actually tried sharing the 12 words
[157:53.18] between Dash Core and the mobile wallet once
[157:56.18] and it did work.
[157:57.94] It broke the mobile wallet because it had a bunch of
[158:01.54] private send transactions in there,
[158:04.54] as in hundreds or thousands of them,
[158:06.90] and it broke the mobile wallet.
[158:08.50] And I had to completely remove it in order to use it again.
[158:12.26] So maybe it's not that bad.
[158:14.34] Maybe it's not as bad as Bit Core
[158:16.62] because more things have been updated.
[158:19.10] Or maybe Bit Core's been updated too, I don't know.
[158:21.14] It's a fork of Bit Core.
[158:22.52] Anyway, so the 12 words and the secret
[158:26.58] are the wallet from the user perspective.
[158:29.06] From the technical perspective,
[158:30.50] that gets turned into a seed.
[158:33.06] So basically a hashing algorithm is run on these
[158:37.12] and then it produces a seed.
[158:38.82] And then from that seed, there's a path.
[158:41.18] And so if you use Edge Wallet on your phone,
[158:44.18] which also does not seem to follow the same standard
[158:47.26] that we're following for extended keys,
[158:52.74] but the Edge Wallet will at least
[158:57.74] let you make multiple accounts.
[159:01.72] And I'm not sure, I think that the way that it does it,
[159:07.86] though, is I think it just creates a separate wallet.
[159:10.58] I think that's what it means by account.
[159:12.86] But the specification actually does define
[159:15.12] that you can have an actual account identifier.
[159:21.74] And so I'm going off of the specs
[159:24.78] and applying it to the way that we use the mobile wallet
[159:31.46] and that is intended to be used with platform
[159:37.38] for being able to share between friends.
[159:39.98] So I give you an XPUB key, you give me an XPUB key,
[159:43.60] we now can make payments back and forth to each other.
[159:47.10] So it's not to, you could make any manner of,
[159:51.96] this is the base layer,
[159:57.34] and you can make any manner of thing on top of it.
[160:01.74] But if you wanted to make a wallet
[160:08.06] where funds were pooled together,
[160:10.74] the question is, what do you mean by that?
[160:16.64] Because that sounds more like,
[160:18.74] I think that's what they call multi-sig with a lock.
[160:28.86] I think is what that is, where you pool together.
[160:32.02] But if you wanted to just pool funds together
[160:34.14] and let anybody who has access to the funds spend it,
[160:36.66] then yes, this would be great for that.
[160:38.54] Because you could share the XPRIV key
[160:40.70] and whoever you share the XPRIV key with
[160:45.30] has the ability to spend.
[160:47.78] And if you share the XPUB key,
[160:50.58] anybody who has the XPUB key has the ability to contribute.
[160:55.06] So you could create a shared wallet from that perspective.
[160:58.34] But as far as I know,
[161:00.58] I think this is actually a pretty good standard.
[161:03.62] And I'm a very critical person.
[161:05.12] You can ask anybody who's interacted with me.
[161:07.56] I'm very blunt, very straightforward,
[161:09.82] and I think most things suck and are wrong.
[161:12.46] I don't think that this is a bad standard.
[161:15.18] I think this is actually pretty good,
[161:17.50] but I don't think that it has been implemented well.
[161:22.50] And so I'm working on,
[161:29.58] there's different,
[161:31.78] again, the term wallet is really overloaded,
[161:34.70] but I'm working on a wallet as in a program
[161:37.98] that could completely replace Dash Core on desktop
[161:42.38] and hopefully could replace the mobile app.
[161:47.38] Although I don't think that there's as strong
[161:53.98] of a need for that,
[161:55.18] whereas the Dash Core on desktop
[161:56.74] is just so clunky and terrible.
[161:58.74] We need something that has those tools.
[162:02.34] So I have, for example, there's a Dash Sign.
[162:05.42] So if you need to sign or verify a message,
[162:07.98] that is its own tool.
[162:11.26] To be able to create a wallet from a phrase
[162:14.94] is its own tool.
[162:16.30] To be able to create all of the keys is its own tool.
[162:21.30] So each of these things can be used.
[162:25.22] Right now, from the perspective of a developer,
[162:29.10] you can see the pipeline from any part of the process
[162:31.54] to any other part of the process.
[162:32.86] It's all distinct atomic pieces.
[162:35.42] And then you can have the pieces play together
[162:37.46] to have the whole.
[162:39.22] So I am working on a live wallet
[162:44.22] so that you could do, for example, subscriptions.
[162:48.98] So if a merchant,
[162:50.50] 'cause this is how the real world works, right?
[162:52.94] I wanna say, I wanna get this amount of service,
[162:55.42] this level of service,
[162:56.46] and I'm willing to pay this much per month for it
[162:58.74] for an ongoing service,
[163:00.06] not for just some crap that costs per month for no reason.
[163:03.68] I hate that stuff.
[163:04.84] But I prefer paying a fixed price
[163:06.86] for things that are actually a fixed thing.
[163:09.86] Why would you pay month after month after month
[163:13.06] for something that you get once?
[163:15.60] But anyway.
[163:18.02] But the ability to have subscriptions
[163:20.62] is something that I think is absolutely 100% critical.
[163:24.78] You cannot get adoption with a payment system
[163:26.86] if there's no ability to do subscriptions
[163:28.62] because then a person has to remember
[163:31.02] to do an action all the time or lose access to their account.
[163:34.22] So there's, at the macro level,
[163:38.86] so there's, at the micro level,
[163:40.86] there's all of these individual tools.
[163:43.06] I'm specifically working on something for HD keys.
[163:45.58] At the macro level,
[163:48.02] I am working on tools that any developer
[163:53.02] can go into the tool and, fingers crossed,
[163:57.86] understand what that part of the process is about.
[164:00.98] Because if you just consider everything that happens
[164:03.70] in a cryptocurrency network,
[164:05.46] it's too big to fit in your head certainly in one sitting.
[164:08.34] But if you just need to,
[164:09.96] if you need to understand just one piece of it,
[164:12.26] so that's at the macro level.
[164:14.14] And then at the high level,
[164:17.34] what all of this is contributing towards
[164:19.34] is a lightweight wallet that can run in a desktop web view
[164:24.34] so that you could have something that is kilobytes.
[164:31.58] You could actually download the desktop app
[164:34.10] and the desktop app itself would be kilobytes.
[164:37.74] And then just open up and be able to use it
[164:41.42] the way that you use, say, for example, Slack or Discord.
[164:46.22] But those are based off of not a web view
[164:49.62] as part of the operating system.
[164:50.86] They're based off of an entire tool chain
[164:54.06] that is hundreds of megabytes.
[164:56.06] But we don't actually need those tool chains anymore.
[164:58.66] We needed them back in the day
[165:00.02] because we had to deal with Internet Explorer 6
[165:04.18] and stuff like that.
[165:05.02] And so when Slack first came out
[165:08.06] and people were still using Internet Explorer 6,
[165:11.06] Slack needed to have the whole Google Chromium tool chain
[165:16.02] embedded into the Slack app
[165:18.26] because it couldn't open up Slack in a web view.
[165:20.06] Now, every operating system essentially uses Chromium
[165:25.06] as the web view for the browser.
[165:29.40] And Mac uses Safari,
[165:31.70] but they're not that far divergent from each other
[165:35.42] from when Chromium forked off of Safari.
[165:38.94] 'Cause originally it was KHTML, which was Linux.
[165:41.56] Apple took KHTML and developed it into WebKit.
[165:47.50] And then Google took WebKit and developed it into Chromium.
[165:52.46] And all three still exist and are at different points
[165:57.86] where you can't merge them back together anymore
[166:00.52] because they're so different.
[166:01.68] But KHTML and Linux has continued
[166:04.28] to evolve the entire time.
[166:06.12] WebKit and Safari has continued to evolve the whole time.
[166:09.64] And Chromium from Google has evolved the entire time.
[166:14.64] So what we have, well, I think they call it Blink.
[166:19.68] Blink is the underlying web view engine.
[166:22.72] Chromium is not just the web view engine,
[166:25.56] but the browser components that you can click on
[166:29.94] and make the window bigger or smaller, click and drag.
[166:33.76] Blink is the engine, just like WebKit's the engine
[166:38.06] and KHTML's the engine.
[166:39.10] Anyway, all that stuff aside.
[166:40.54] So a modern cryptocurrency wallet could be kilobytes.
[166:48.40] It could be something that someone,
[166:53.96] and this is kind of a contrived use case,
[166:56.62] but I'm gonna throw it out there
[166:57.62] 'cause it is one that's said and used in the media
[167:00.22] and why this is great,
[167:02.86] why it's gonna revolutionize the world.
[167:04.26] I don't buy into all of that necessarily,
[167:05.86] but I do think that this is a moral good
[167:08.58] that someone in a third world country
[167:10.70] could download and use it.
[167:12.44] I think that that's a moral good.
[167:14.08] So, and it's a better experience for everybody
[167:18.90] because most people are not on gigabit fiber,
[167:21.62] especially not in America
[167:23.44] and especially not in third world countries.
[167:25.16] Now over in Europe, they have a lot more gigabit fiber.
[167:28.24] Over here, America kind of sucks
[167:30.84] because we've got all the old infrastructure
[167:33.02] and everybody else built their infrastructure after us
[167:35.24] and so they already had better infrastructure
[167:37.04] by the time they were building the infrastructure for it,
[167:38.80] but so it goes.
[167:40.22] Yeah, so you said, sorry,
[167:46.64] I went on rambling for quite a bit there,
[167:48.20] but you said just saw you here
[167:49.48] and yeah, was exactly thinking that.
[167:52.78] So what was it that you were thinking exactly that?
[167:55.58] What were you referencing specifically?
[167:58.40] Okay, I'm gonna get back to this for a minute.
[168:05.66] Okay, so do I want to have,
[168:17.46] let's see.
[168:18.30] Okay, so do I want to have, let's see.
[168:21.46] (keyboard clacking)
[168:50.10] Bless you, my son.
[168:51.66] Thank you.
[168:52.70] That would be super cool.
[168:53.94] Update, so, so much easier to use.
[169:00.30] Can't talk two way, but very cool.
[169:01.98] Can't remember, okay.
[169:03.10] (keyboard clacking)
[169:06.10] (upbeat music)
[169:09.52] (keyboard clacking)
[169:12.52] (upbeat music)
[169:15.10] (keyboard clacking)
[169:18.10] (upbeat music)
[169:20.68] (keyboard clacking)
[169:23.68] (upbeat music)
[169:26.26] (keyboard clacking)
[169:55.38] Okay, so I think this is what I want the API to look like.
[170:00.38] I think this is, they're basically two use cases.
[170:05.14] Either you just need to do something really quickly once.
[170:08.02] Whoops.
[170:20.86] (keyboard clacking)
[170:23.86] Actually, let me move this up.
[170:33.14] 'Cause I think I kind of want to get to this point.
[170:37.98] There we go.
[170:38.82] 'Cause this is kind of boiler plate.
[170:39.98] So I'm gonna put this up with the installation here.
[170:44.46] (keyboard clacking)
[170:47.46] All right.
[171:10.88] So yeah, this is AI.
[171:13.22] I want to show this part here.
[171:15.14] Just gonna move this boiler plate up a little bit.
[171:39.42] (keyboard clacking)
[171:42.42] There we go.
[171:48.82] So by the way, I'm not gonna be working
[171:59.74] on any of the UI stuff.
[172:00.78] That's not what I do.
[172:02.26] There's no such thing as a full stack developer
[172:04.26] in my experience.
[172:05.38] There are people who are good at front end,
[172:09.14] who can dabble in the backend
[172:11.02] and make choices that aren't absolutely stupid.
[172:14.38] And there are people who do
[172:16.86] the more algorithmic slash
[172:24.34] engineering-esque programming,
[172:30.54] who can make a box blue if they need to.
[172:35.54] But there's no such thing as a full stack developer.
[172:38.62] Any more than there's such a thing as a professional chef
[172:43.62] who's also a professional motocross.
[172:48.38] That such a thing does exist.
[172:51.26] There is somebody who has these two
[172:52.94] completely unrelated skills
[172:54.30] out of the universe of all the world.
[172:56.54] There are people who have completely unrelated skills
[172:59.58] who are true masters in both unrelated skills.
[173:03.58] But in the case of development,
[173:07.10] front end and backend are as unrelated as being a...
[173:12.10] At the very least,
[173:14.78] as unrelated as being a cook and being a baker.
[173:17.54] And quite possibly closer to the difference
[173:21.96] between being a baker
[173:23.82] and being a professional motocross racer.
[173:27.82] Okay.
[173:33.64] All right, so if we do that,
[173:34.86] we can get rid of this boilerplate here.
[173:37.10] Okay, and that makes that a little bit easier to digest.
[173:40.02] 'Cause then we're just focused in this documentation on...
[173:44.02] There we go.
[173:46.90] (upbeat music)
[173:49.48] (keyboard clacking)
[173:52.48] (keyboard clacking)
[173:55.70] (sighs)
[173:57.70] (sighs)
[174:16.54] (keyboard clacking)
[174:19.54] All right.
[174:27.40] Okay, there we go.
[174:39.40] I think that this is pretty good
[174:42.32] for what this should look like.
[174:44.72] (upbeat music)
[174:47.30] If we wanna serialize it,
[174:50.96] that's how we serialize the XPRIV.
[174:55.56] That's how we serialize the XPUB.
[174:57.26] If we wanna just do a quick one-off,
[175:00.18] here's how we use the key,
[175:03.94] and then we derive it.
[175:06.22] So,
[175:13.72] I think that we might still be able to use...
[175:17.18] We don't have a to seed,
[175:18.28] so I kinda don't wanna do the from seed,
[175:20.84] but we could just do the derive wallet.
[175:22.84] I think this works.
[175:39.06] (keyboard clacking)
[175:42.06] Yeah, so an SDK,
[175:54.72] this is one of those terms that's a little bit fuzzy.
[175:57.38] So, software development kit
[176:00.66] is kind of a more corporate, enterprise-y term,
[176:04.04] but yes, I am building a Dash SDK
[176:07.82] that is composed of various tools.
[176:11.94] So, I'm calling that SDK Dash Tools at present.
[176:16.94] And that's kind of the meta collection.
[176:22.12] That's where Dash Tools is the umbrella
[176:24.30] of the library-level stuff that I'm building.
[176:27.76] Somebody who's a front-end developer
[176:29.58] is highly unlikely to be able to build the things
[176:34.46] that I'm building in a reasonable amount of time.
[176:37.32] But what I need to do
[176:40.78] is make sure that the documentation and the use case
[176:43.10] is good enough that the front-end developer
[176:45.42] can then take it and understand it.
[176:47.82] And I'm not trying to dumb this down to nothing.
[176:51.22] I expect that there is a certain level of terminology
[176:54.44] that you have to understand.
[176:56.50] I'm not trying to build something that's very abstract
[176:58.62] because things that are very abstract are very complicated.
[177:01.30] The beauty of abstraction is that it hides the details,
[177:05.14] but the curse of abstraction is that it hides the details.
[177:08.62] And so, I'm building something at a level
[177:11.42] where the wallet that I talked about,
[177:13.68] the wallet project, which would also be a library,
[177:17.58] but that would be very abstract.
[177:19.30] That would be something that probably more people
[177:22.02] would want to use at a higher level.
[177:24.90] The tool that I'm working on right now is not,
[177:28.30] it's kind of below the layer of abstraction into details.
[177:33.78] So, a lot of people may not want to know
[177:37.74] what an extended private key or XPRIV is,
[177:41.42] or an extended public key or an XPUB is.
[177:43.78] And this library is not for those people.
[177:45.90] I think that it is important to have an understanding
[177:51.30] and a demonstration of the core technologies.
[177:53.62] So, most people, I don't think there's anywhere
[177:57.22] in the Dash documentation as far as I'm aware,
[177:59.54] but there's a lot of it, and I haven't looked at all of it.
[178:03.38] But I don't think that there's a place
[178:05.34] where we actually use these standard path strings.
[178:09.58] And that kind of makes sense,
[178:11.58] because when you create a Dash wallet,
[178:13.86] you assume all of those.
[178:16.02] So, all of this stuff up front, if you're creating a Dash wallet,
[178:20.22] you would never use anything else.
[178:21.94] So, why would you need to expose that?
[178:24.34] And that's kind of what I'm doing, actually,
[178:26.38] in this previous example, is I do hide that away.
[178:28.90] When you create the wallet,
[178:30.54] unless you specify additional options,
[178:32.74] it assumes that it is going to be a BIP-44 wallet of type 5,
[178:39.50] which is Dash.
[178:41.18] But then these pieces are the pieces
[178:42.98] that you do generally have to change.
[178:47.50] The first one is the account,
[178:49.70] which is the thing that I think is the least well-understood
[178:52.70] and implemented across the ecosystem,
[178:54.82] as I see it right now.
[178:56.42] And then there is the use, and the use is either right now,
[179:02.26] for all applications I've seen,
[179:03.98] it's either a receiving address or a change address.
[179:08.34] And then the last thing is the index.
[179:10.26] So, every time you use a key, an address,
[179:14.10] you increment to the next one.
[179:18.54] So, if you've done 100 transactions,
[179:21.50] you have 100 different indexed keys.
[179:25.02] So, your next number would be 100 here, like that.
[179:30.50] [typing]
[179:53.90] Okay. So, this, that I feel pretty good about
[179:57.90] in terms of this documentation
[179:59.62] being the right, this is at the right layer.
[180:02.62] The one thing that I might want to split out
[180:06.22] is that this is actually kind of a third use case.
[180:10.86] I think I will split this out.
[180:12.50] [typing]
[180:21.14] For creating XPRIV/XPUB wallets to share with contacts
[180:32.14] for future payments.
[180:34.54] So, I think I will actually cut this out.
[180:39.74] [typing]
[180:45.74] Because that really, it's a separate use case
[180:49.26] from what this one was.
[180:50.50] [typing]
[180:54.50] And I think if I'm going to always have this be there,
[181:01.02] I may actually bring these back.
[181:03.22] [typing]
[181:04.22] Okay. So, there's wallet.
[181:06.22] [typing]
[181:07.94] And then I think I could say, yeah, there's a usage.
[181:11.94] [typing]
[181:12.94] Then we don't need to do this one either.
[181:14.42] [typing]
[181:17.14] Okay. So, now wallet, we're going to say derive account.
[181:22.14] I'm going to specify use.
[181:24.14] [typing]
[181:40.74] Okay.
[181:41.74] [typing]
[181:43.54] And then we would actually want to show this same thing again.
[181:48.54] [typing]
[182:04.54] Okay.
[182:05.54] This might need to be split out even a little bit further.
[182:08.54] [typing]
[182:18.54] I don't know if I want that method that way.
[182:20.54] I think I do.
[182:21.54] I'm not sure.
[182:23.54] We'll come back around to that later.
[182:25.54] [typing]
[182:52.54] [typing]
[183:00.54] Okay.
[183:01.54] [typing]
[183:06.54] Maybe, I don't know if this will be cleaner or clearer if we do it this way,
[183:11.54] but I think it might be.
[183:13.54] So, I'm going to shorten this up to look like that
[183:17.54] in hopes that that will actually be easier to read
[183:27.54] with the comments on the side there.
[183:30.54] [typing]
[183:37.54] Okay.
[183:38.54] So, I missed something.
[183:39.54] Oh, okay.
[183:40.54] That bit came later.
[183:42.54] Front-end developers can build functions off your new library.
[183:45.54] Yes.
[183:46.54] And somebody on mobile, you should be able to use it, too, actually.
[183:50.54] No, you said you're not a developer.
[183:53.54] Can't hunt.
[183:54.54] So, I'm on mobile, can't hunt and peck.
[183:57.54] I don't know exactly what you meant by that,
[183:59.54] but I'm guessing you mean you can't scrub back and forth very easily?
[184:03.54] Or maybe you're saying you can't zoom in to see very easily?
[184:06.54] Yeah.
[184:07.54] So, front-end developers, yes, they can use this library,
[184:09.54] and I think mobile as well.
[184:11.54] And this is the other thing.
[184:13.54] I really think it's a bad idea to create Android apps
[184:18.54] and iOS apps using the same toolkit because they always look crappy.
[184:23.54] I mean, you know when you're on an app that was built for Android
[184:27.54] when you're on iOS.
[184:29.54] It doesn't work right.
[184:30.54] It's clunky.
[184:32.54] You know, you can tell.
[184:34.54] The back button's not in the right place.
[184:36.54] The home button behavior's not correct.
[184:40.54] And I think that the same goes the other way around.
[184:42.54] If you're on an Android app that was built for iOS, you can tell.
[184:45.54] Again, back button's not in the right place.
[184:49.54] The confirm button's not in the right place.
[184:51.54] You just get wrong behaviors.
[184:54.54] And I think there is a use case where if you have a really strong brand,
[184:59.54] I think there is a use case to saying,
[185:03.54] "No, we're going to build an app that is the same on iOS and Android
[185:07.54] because our brand is so strong."
[185:11.54] But I don't know of any brands that can pull that off.
[185:13.54] I can name zero brands that I think are strong enough
[185:16.54] that they should have a synonymous experience across iOS and Android
[185:21.54] because people who use iOS don't use Android,
[185:23.54] and people who use Android don't use iOS.
[185:26.54] People that are on Android expect it the Android way.
[185:28.54] People who are on iOS expect it the iOS way.
[185:32.54] So if somebody is introduced to an app on Android
[185:34.54] and then they go get it for iOS,
[185:37.54] they're going to expect the same options to be available in the menu,
[185:41.54] but they're not necessarily going to expect the back button
[185:44.54] to be in the same place on both apps.
[185:47.54] And I get the idea of you want to create a tutorial
[185:53.54] and you want to show how to use your app and it should work the same on both,
[185:56.54] but anyway, that aside,
[185:59.54] the point that I was getting to is that with this,
[186:02.54] because this code is so simple,
[186:05.54] I've dumbed it down.
[186:07.54] I've taken it from super-duper, super-smart JavaScript developer code
[186:13.54] to idiot moron JavaScript developer code.
[186:17.54] So, I mean, maybe that's a little bit of a stretch
[186:21.54] because you can't do this stuff if you're a moron
[186:24.54] because it's really hard.
[186:26.54] But if you're at the level of you're not a JavaScript nerd
[186:32.54] and you understand all the different things about JavaScript,
[186:35.54] about how all the nuanced details,
[186:39.54] but you know how to program in, say, Swift
[186:42.54] or you know how to program in Kotlin.
[186:44.54] Swift is the iOS language and Kotlin is the Android language.
[186:50.54] You could look at this,
[186:52.54] and I have an extremely high degree of confidence
[186:55.54] that you could know what it's doing
[186:57.54] because this doesn't have anything--
[187:00.54] this is almost at the level of pseudocode
[187:03.54] in terms of how simple it's written.
[187:05.54] Everything is spelled out, everything has a variable name,
[187:08.54] there are no shortcuts.
[187:10.54] So, you could take this
[187:12.54] and you could probably cut the number of lines in half
[187:15.54] by getting rid of intermediary variables and all that.
[187:18.54] But when you're talking about web development,
[187:20.54] all that stuff happens anyway.
[187:21.54] When you run the minifier,
[187:22.54] it gets rid of all the intermediary variables.
[187:25.54] So, the idea of doing that in your source code
[187:29.54] is not a good idea, in my opinion,
[187:35.54] because we should always optimize for readability and understandability.
[187:40.54] So, anyway, I think that someone could come through here
[187:43.54] and they could re-implement the 15 functions
[187:46.54] that they need to have in order for this to work,
[187:49.54] and I believe that they could actually do it.
[187:51.54] And that's another thing that I'm hopeful for about this,
[187:56.54] because I don't really understand our community that well.
[187:58.54] I don't know if I'm really part of our community that much.
[188:01.54] I'm just kind of off in my own little corner
[188:04.54] doing some AJ stuff
[188:06.54] and hoping that it will turn out to be really, really useful.
[188:13.54] This project is wrapping up this week,
[188:16.54] along with a few others that were related.
[188:18.54] So, there's basically a ball of four projects
[188:21.54] that have so many different interconnected parts.
[188:23.54] They are discreetly separate in terms of
[188:26.54] you can understand the passphrase library
[188:28.54] without understanding the extended public key library,
[188:31.54] and you can understand how WIFs,
[188:35.54] otherwise known as private keys and addresses, work
[188:38.54] without understanding those other two things.
[188:40.54] So, they are logically separated,
[188:42.54] but there's also a lot of interplay,
[188:43.54] and they need to be consistent,
[188:45.54] which is something that we don't have in the ecosystem.
[188:47.54] We don't have...
[188:49.54] One library will call it XKey with a capital X.
[188:51.54] Another library will call it XKey with a lowercase x.
[188:54.54] One library will call it XPriv with an i.
[188:57.54] Another library calls it XPriv without the i.
[189:00.54] So, XPRV versus XPRIV.
[189:03.54] And so, I want this SDK...
[189:07.54] I want it to be cohesive within itself,
[189:10.54] where everything has a similar name.
[189:13.54] If it's called parse here, it's called parse there.
[189:15.54] If it's called to there, it's called to there.
[189:16.54] If it's called get here, it's called get there.
[189:19.54] So that, when you look at it as a whole,
[189:22.54] it feels like it was made by...
[189:25.54] It feels like it was made intentionally.
[189:28.54] Not accidentally.
[189:30.54] Which, the things that have been made were made accidentally.
[189:33.54] They were made intentionally in terms of functionality,
[189:35.54] but they weren't published intentionally.
[189:37.54] They were published incidentally,
[189:39.54] I guess would be the correct word to say.
[189:42.54] [typing]
[189:50.54] I actually don't think we need a getKeys.
[189:53.54] I'm going to push back on that one.
[189:56.54] [typing]
[190:05.54] This is going to be -keys.toWiff.
[190:11.54] Oh, whoops.
[190:13.54] Ooh.
[190:15.54] Actually, we do need getKeys.
[190:18.54] So this is going to be privateKey.
[190:21.54] Um...
[190:24.54] [typing]
[190:29.54] And this is going to be publicKey.
[190:32.54] [typing]
[190:35.54] Yeah, okay, whoops.
[190:38.54] [typing]
[190:41.54] And this will be -keys.toWiff
[190:48.54] and -keys.toAdder.
[190:53.54] [typing]
[190:57.54] Keys.privateKey.
[190:59.54] [typing]
[191:02.54] Keys.publicKey.
[191:07.54] [typing]
[191:10.54] Okay.
[191:11.54] So I'm actually going to bring that back over this way
[191:15.54] so we look at it from this perspective.
[191:19.54] Um...
[191:21.54] [typing]
[191:29.54] So this one will go away
[191:31.54] and this one will be, again, privateKey.
[191:40.54] Let me make that over here.
[191:43.54] So this will be both.
[191:47.54] And this one will be just the one.
[191:50.54] Just be the publicKey.
[191:53.54] And we will do this again.
[192:06.54] Okay, there we go.
[192:08.54] That's the correct API.
[192:31.54] Okay, I think this is the right layering.
[192:36.54] sgPath =
[192:45.54] We could call this keyPath.
[192:51.54] And likewise we could call this accountPath.
[193:19.54] There we go.
[193:34.54] And this one would need to be like that.
[193:53.54] Okay, is this right?
[194:07.54] Okay.
[194:08.54] Now that's at the right level.
[194:09.54] Okay, so these are all correct now.
[194:12.54] That's all correct.
[194:15.54] And unfortunately my syntax highlighting doesn't dive down into...
[194:18.54] I'm editing the documentation now so the syntax highlighting is mostly off.
[194:22.54] Okay, but this is correct.
[194:23.54] I feel really good about that.
[194:25.54] Okay, now I'm going to go take a break
[194:27.54] and I'm going to kind of let that simmer
[194:31.54] before I finalize it for good, hopefully.
[194:36.54] So this is going to be updateDocs.
[194:44.54] So yeah, I think that if I just fill out the rest of...
[194:49.54] I think I'm 99% there in terms of what I just did before.
[194:53.54] But I think if I just fill out the rest of the methods
[194:58.54] to match the documentation I made, I think I'll hit the use case.
[195:02.54] And then I'll move on and then I will be...
[195:07.54] I will be making sure that -phrase, -keys, and setp256k1, and -hd.
[195:22.54] Those four things, they need to all be finalized.
[195:27.54] So that will be the rest of today and tomorrow.
[195:32.54] We'll be finalizing those four things, I think.
[195:36.54] And then once those are finalized,
[195:40.54] and I do need to add, I want to add a few more test fixtures,
[195:43.54] or tests from the official canonical BIP44 test fixtures
[195:49.54] for this library, not just the tests that were included with it.
[195:52.54] Because it includes tests in the library, but I believe that...
[195:56.54] Well, I know that it's been working for me.
[195:58.54] Because I'd been using this library before it was all refactored and everything.
[196:02.54] So I should be able to swap it out with my wallet,
[196:06.54] and I should get back the same things.
[196:10.54] And so I guess that would be a good test to try first.
[196:15.54] But then the next one is going to be the blockTx and the wallet and dashSite.
[196:20.54] So those three things are going to go together next.
[196:22.54] So let me actually write this down.
[196:31.54] Okay, so what we have is...
[196:34.54] "Phrase" is what creates the wallet.
[196:37.54] "DashKeys", well, "secp256k1"
[196:44.54] is what actually allows you to sign, a.k.a. make a payment.
[196:53.54] "DashKeys" is what provides the abstractions
[196:57.54] with the "wif" and the "adder" and some of the encoding.
[197:05.54] And then "dashHD" is what...
[197:17.54] Let's see here...
[197:19.54] Ah, and we have to use "dashKeys" anyway.
[197:23.54] So, yeah, and then "dashHD" is what actually handles the hierarchical derivation.
[197:29.54] So you can use "dashKeys" without ever touching "dashHD".
[197:33.54] If you use "dashHD" realistically, you need every...
[197:37.54] These two are pretty tightly coupled,
[197:39.54] but "dashPhrase" can be used independently of "dashKeys".
[197:43.54] And then these two are pretty tightly coupled, but for various reasons,
[197:48.54] someone may want to substitute the "secp256k1" library that's being used.
[197:54.54] So this is the layer that we're going with.
[197:57.54] So this is "dashSDKCore", "dashToolsCore", whatever.
[198:07.54] And then the next layer up, that will be next...
[198:11.54] So this will be presented next week, I think, is all of these three and a half things together.
[198:18.54] And then this will be presented...
[198:21.54] Perhaps the next month will be "dashSite", "dashWallet", and what was the other one I said?
[198:31.54] "dashTx".
[198:35.54] This is kind of the grouping for these.
[198:37.54] And so this is "dashTools", the "walletSDK" is really up at this layer.
[198:44.54] And so then we've got some other stuff on top of that,
[198:47.54] which is kind of the "dash", I don't know, community or whatever.
[198:51.54] But we have "crowdNode", which actually we need to rename that, potentially,
[198:59.54] to be maybe "dashCrowd" or, I don't know, "dashPool".
[199:06.54] But this one is getting a UI soon.
[199:10.54] UI is coming on that soon.
[199:12.54] And the UI on this one is being developed simultaneously.
[199:20.54] And the frontend is also being developed for this presently.
[199:28.54] So I've got to do each of these first.
[199:33.54] And then we have the core CLI, which needs to take place.
[199:38.54] And that is going to include "dashMessage" rather than "secp256k1".
[199:48.54] But these are the core CLI tools.
[199:58.54] Anyway, I will be back later, but I'm going to take a break for now.
[200:05.54] Before I explode in my pants.
[200:10.54] And then grab something to eat as well.
[200:12.54] Let's see, what time is it? 1.24?
[200:14.54] That's a great time to take a break. So I'm probably going to take a break for a couple hours.
[200:18.54] And then I'll be back.
[200:21.54] And this is my roadmap.
[200:24.54] So last week, I was just out of sorts. I didn't really do much at all.
[200:29.54] The week before that, I was just burning hard on these things.
[200:33.54] But in the intervening week, while things were settling in my mind,
[200:38.54] I had some better ideas about how to approach some things.
[200:40.54] And then I also... It was good and bad.
[200:45.54] Because sometimes if you go on something too strong, you lose the big picture.
[200:52.54] Because you're too focused in the details.
[200:54.54] But when you pull back away from the details, sometimes it's a little bit rougher to get back into them.
[200:59.54] Because there's too many details to know them all.
[201:02.54] And so yesterday was a little bit more of... And some of today was a little bit more of that.
[201:08.54] And kind of reacquainting myself with details again.
[201:12.54] So that I can get the finer pieces done.
[201:19.54] And the finer pieces are a little bit more abstract and higher layer.
[201:27.54] Anyway, I'm going to get out of here. Thanks for tuning in.
[201:31.54] Like, sub, follow if you want to.
[201:33.54] So let me go ahead and just pop that back up.
[201:35.54] It did come up just a minute ago, but I'll put it back up again.
[201:37.54] So there's the like, sub, follow if you want to.
[201:40.54] And I really appreciate the conversation, JustMe.
[201:42.54] It makes it a lot more enjoyable to do the work.
[201:48.54] And beneficial when I have a chance to explain what I'm doing.
[201:51.54] And kind of hear myself say it and think through things.
[201:54.54] And I think that's what drives towards perfection, in a sense.
[202:00.54] And if you were a developer and you could give me some critical feedback, that would be even more awesome.
[202:07.54] But I guess not if you were.
[202:09.54] If we had another person who were more of a developer and could give me some critical feedback, that would be awesome.
[202:14.54] But I enjoyed the conversation with you and your feedback.
[202:17.54] And we will get back to this later today.
[202:23.54] And carry on.
[202:25.54] And then this segment that I just went over.
[202:31.54] This is what I should be able to present on during the weekly update next Monday.
[202:41.54] Yeah, you'll learn something.
[202:45.54] If nothing else, the osmosis of just terms being thrown out can be highly helpful.
[202:51.54] Alright, I'm going to pause the music here.
[202:55.54] I think we still can't raid because we're still not a month old.
[203:00.54] So we should be a month old in, I think, not this week, but at the end of next week.
[203:08.54] Because I think we're two or three weeks old now.
[203:12.54] So as soon as we're a month old, we can do raids again.
[203:15.54] But right now we can't do raids.
[203:17.54] Thanks for joining in. I will catch you later.
[203:21.54] Adios.
[203:26.54] Wait, why didn't it -- uh-oh.
[203:29.54] What did I break?
[203:35.54] We need -- so I'm going to flash up the screen here.
[203:39.54] I think I'm going to flash up the screen here.