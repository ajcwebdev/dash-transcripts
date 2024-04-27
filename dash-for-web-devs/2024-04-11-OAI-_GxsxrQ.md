---
showLink: "https://www.youtube.com/watch?v=OAI-_GxsxrQ"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "End to End Dash Tutorial: Next.js - 6d"
publishDate: "2024-04-11"
coverImage: "https://i.ytimg.com/vi/OAI-_GxsxrQ/maxresdefault.jpg"
---

This is a transcript with timestamps.

Write a one sentence summary of the transcript and a one paragraph summary.
  - The one sentence summary shouldn't exceed 180 characters (roughly 30 words).
  - The one paragraph summary should be approximately 600-1200 characters (roughly 100-200 words).

Create chapters based on the topics discussed throughout.
  - Include timestamps for when these chapters begin.
  - Chapters shouldn't be shorter than 1-2 minutes or longer than 5-6 minutes.
  - Write a one paragraph description for each chapter.
  - Note the very last timestamp and make sure the chapters extend to the end of the episode

Format the output like so:

    ```md
    One sentence summary which doesn't exceed 180 characters (or roughly 30 words).

    ## Episode Summary

    tl;dr: One paragraph summary which doesn't exceed approximately 600-1200 characters (or roughly 100-200 words)

    ## Chapters

    00:00 - Introduction and Beginning of Episode
    The episode starts with a discussion on the importance of creating and sharing projects.

    02:56 - Guest Introduction and Background
    Introduction of guests followed by host discussing the guests' background and journey.

    ## Transcript
    ```

TRANSCRIPT ATTACHED

---

[00:00] >> All right. We are live.
[00:05] Welcome back. My name is Anthony Campolo, and if you've been following these streams, I am building
[00:11] out some front-end examples/a tutorial for the Dash platform. I had started this project last summer, actually, many, many months ago, and these last couple
[00:26] weeks kind of picked it back up, and I've been working through it again, kind of reacquainting myself with the code I wrote and the general flow of the tutorial, and there are some issues
[00:40] we're having with test net for a while that kind of had to work out, and then just some kind of minor changes in how things are working with the code, but for the most part, almost
[00:51] everything worked exactly the same in terms of the code that was written back then, you know, with blockchains, especially, you have this kind of foundational chain with certain
[01:02] methods and ways of interacting with it that likely won't change, because it's such a frickin' pain to try and get anything to change on a blockchain, which is kind of by design,
[01:14] because the harder it is to change, the harder it is for someone to come in and subvert the system and change it for their own means, but the place we're at now in the tutorial
[01:25] is I had originally gone through -- well, actually, let me pull up the dash org platform docs so I can kind of show what I'm talking about here, because they separated out into
[01:45] two kind of big chunks, which I think makes a lot of sense. So the way they've got it with the docs is they have identities and names is a section
[02:00] with all the stuff in terms of registering and retrieving an identity, working with that identity's balance, and then creating and retrieving a name, and then separate from
[02:13] that then is the contracts and documents, and this is how you can create ways of saving data on the blockchain, and what this does is it kind of gives you, like, a hello world
[02:28] crud app without delete, so you learn how to register the contract, which then allows you to submit documents to it.
[02:36] You can kind of think of the contract as like the schema for the documents, so the simplest thing will just be a message with a string.
[02:43] That's kind of what we're going to create, what is created here, and then you can read it back, so CRUD, but I actually -- I guess you can delete documents here, but they'll
[02:58] still -- I mean, even if you delete it, there will still be a record of it on the blockchain, but this probably -- what this does, this just makes it inaccessible, so this is nice,
[03:08] because, you know, if you upload some sort of exploit or someone uploads an exploit, it will give you the ability to delete it, but maybe actually the contract itself, you'd
[03:24] have to delete to do that, but anyway, so this whole section was stuff that I had kind of just started doing when I kind of took a break last time, so I had mostly just kind
[03:38] of gone through and created headings for each of these, and -- because the way I've been doing this tutorial is every -- I basically go through script by script of what we're
[03:55] doing, so, you know, you have -- and Ryan had asked me to do, like, a clean run-through of this whole thing, and I will do that, I'm not going to do it today, though, because
[04:07] I want to finish the front-end part, the node part is all totally done right now, but if we're going to have a video example of the tutorial that we can kind of point people
[04:17] to, I don't think it makes sense to do it until we can actually do the whole flow, so I basically start with creating a script, and I give you the code for the script, and
[04:26] then I have you run the script. Many of these I still need to kind of fill in more explanations, and what I'll do is
[04:34] I'll make sure I'm just explaining, like, these three main functions, because this is where the important stuff is happening, but for the most part, that's kind of, like, how
[04:42] I've been going about making this, and so for all of this contract and data stuff, I had basically put, you know, the command, or create the script, run the command, and
[04:55] then I had just copy-pasted the code, like, straight from the docs, so the last two nights ago, I went through all of those and got them all working, and also converted - everything
[05:04] is now written in async/await, so I had originally, you know, updated the imports and exports to be ESM, because that's really a deal-breaker for - if you're trying to work with modern
[05:18] tooling that's getting harder and harder to work with, require, and almost impossible to work with both of them, unless you, like, want to have that be a full-time job for you,
[05:27] so we've been on the right imports this whole time, but all the code in the examples, you know, there's nothing necessarily wrong with this, but they're written with, you know,
[05:37] this .then kind of promise syntax, which is how many JavaScript developers were doing things for probably a decade or so, and that has been the kind of - if you watch, you know,
[05:51] tutorials and see how to do stuff in JavaScript, the modern way, and the way that now people - is async/await, and people held off from this and used promises for a while because
[06:00] of browser compatibility and things like that, but at this point, there's really no reason not to use async/await, I think, unless - I don't know, I'm not really sure what the argument
[06:10] to be made for why you would want to use promises aside from just, like, keeping compatibility with previous stuff, or for people who still kind of find that most useful, but, you know,
[06:23] I think it creates a situation where it's harder to get, like, outputs and console logs and stuff throughout the command, so I think that async/await is really the way to go,
[06:38] and for me, you know, I find it - and this is just - I find it simpler and more readable because I've done it more, and it's kind of, like, what I'm used to, but at the same time,
[06:48] the way - let me show this as an example, so - so, like, here, if you look at this example, there's - okay, hold on, this is slightly different - let me look at it - okay, there's
[07:16] some - I forget exactly which example, but there's, like, two places where there would be something console log, like, you console log something here, and then something, like,
[07:24] in here, so I think that can be a little bit confusing, whereas with async/await, you kind of just await wherever you need to, and then you have try-catch finally for the block,
[07:36] so that's how I wrote this. I'm not really sure how we want to manage this in terms of the actual docs, because
[07:45] I think for sure we're going to want to update this, whether to update the promises to async/await, I think it might - you know, some people consider it just, like, a manner of taste.
[07:54] I think it makes sense to just go with the most modern syntax, but something that might be a good idea is adding one of those tab things, so we can keep all of this old code
[08:05] the way it is, and then tab over to ESM, which would both give you the import and also written in async/await, so that might be the best of both worlds, in terms of we can keep both
[08:15] there, people can kind of choose which route they want to take, but anyway, let's go through these examples, so let me go into here, and close this up, great, so we would be at right
[08:43] now is registering the contract. So this is going to register the contract, which has the kind of schema, as I was saying,
[09:02] so schema is type string, and you're going to have a message, so basically we're going to get back an object that's going to be just message, and then some text, "Hello" from
[09:14] ajcwebdev, and then it's going to console.log your contract ID, and then the whole contract itself, so let's see if that's all working.
[09:47] So here's contract ID, so that is able to come out while the next part is, so I'm not sure if that's just because they async/await, but I feel like that's kind of what it enables,
[10:01] is stuff like that, okay, so if we look at this, we have an ID, an owner ID, and then the document schema, and document schema has, no, is that something that I did, yeah, I'm
[10:23] not sure, I think, that's probably, you can call that whatever you want, I'm guessing, but this is how the tutorial did it, I believe, so let's just keep that the way it is, let
[10:38] me copy/paste this, contract ID you want to put in your .env, because we'll need that for a future command, okay.
[11:13] So now we got the contract ID, oh yeah, and I also learned since the last time I was streaming, there's a whole different block explorer for the platform, so we've been on the original
[11:34] dash block explorer earlier to when you created your wallet and you have an address, you give us some test funds, you can do all that through the regular explorer, but here is where things
[11:44] like the identities and the data contracts come in, so this is our identity, so when we created an identity, we got an identity ID, and I'm modifying the commands I had a
[11:57] bit, so now it gives you the environment variable, like how it gives it directly, it basically says this equals this, I'm also going to have an output saying click this link to go see
[12:08] your thing, so right in the terminal, you get a link, just takes that and appends it to this, and then here we can see transactions, you can see how many credits you have, these
[12:21] are all the times I've been topping up this identity, and then you have all these documents, you see this is the 2am the other night when I was doing this, and then all your data contracts,
[12:33] yeah, see, I was hacking away on that, all right, and then this is the data, so I need a screenshot of this, I believe, cool, okay, so now we've got, that's good, there we go,
[13:11] that's good, so now retrieve contract, this will be, if we want to just get back the same thing we got back when we created it, so, and then that's why you need the contract
[13:25] ID here, so that you can get it back, and then there it is, just like before, I should give the link in both of these, yeah, okay, I'm trying to find, I have one that already
[14:15] has it in there, if you can find it, let's see, there we go, so let's copy paste that, okay, so let's just start with this one, except instead of identity, you want data contract,
[15:00] let's try that, wait, I gotta put in the actual, okay, yeah, so that's why it's not going to be name, it's going to be something else, it's going to be ID, so I need, or no, I got
[15:39] ID, but it's not name, it's, oh, I think it's this, let's try that, yeah, there we go, oh, what am I doing wrong there, oh, I see what I'm doing wrong, yeah, duh, I gotta have this
[16:34] whole thing inside there, I think, yeah, I'm doing, what am I doing wrong, okay, so, yeah, I think I had an issue with something like this before, because the way it gives you,
[17:12] oh, no, it's not dollar sign ID for this one, there's another one where sometimes the dollar sign like this thing, anyway, let's see if that works, there we go, great, great, yeah,
[17:48] that's right, because this one's dollar sign, yeah, it's name.dollar sign ID, which is a little bit confusing, okay, that was just at retrieve contract, cool, okay, yeah, so,
[18:22] actually, let's update the tutorial with what I got working, there we go, great, and then I'm just gonna copy paste that for when I created it, create a new one, nope, I can't
[19:10] put it, it's the only thing about when you are working with docs and you're also coding something, oh, he's flipping back and forth, one to the other, okay, yeah, so, yeah, that's
[19:45] great, okay, there we go, there we go, yeah, there we go, great, yeah, there we go, yeah, there we go, there we go, yeah, there we go, yeah, there we go, yeah, there we go, yeah,
[20:34] there we go, yeah, there we go, yeah, there we go, yeah, there we go, yeah, there we go, there we go, yeah, there we go, yeah, there we go, yeah, there we go, yeah, there we go,
[21:20] there we go, yeah, there we go, yeah, there we go, yeah, there we go, yeah, there we go, there we go, there we go, yeah, there we go, yeah, there we go, yeah, there we go, yeah,
[22:15] there we go, yeah, there we go, yeah, there we go, yeah, there we go, yeah, there we go, there we go, yeah, there we go, yeah, there we go, yeah, there we go, yeah, there we go,
[23:08] yeah, there we go, yeah, there we go, yeah, there we go, yeah, there we go, yeah, there we go. Cool. Yeah, because this is the stuff that I find that if you can connect the dots for people,
[23:18] like show them stuff on the block explorer along with what they're doing when they're writing the commands, and this stuff starts to make a lot more sense and come together versus when you're just kind of like interacting with the CLI and getting data back, and it's just a bunch of JSON, and you're just like, "Uh, what's going on here?"
[23:38] Okay, cool, cool, cool. I should do that for identity as well. Identity create. I'm going to do the top up.
[24:17] Where's the identity section? There we go.
[24:37] Okay, I have to create identity. Got this one. So, it doesn't actually look in the identity create transaction specifically.
[25:08] Okay. So,
[25:29] Okay. Okay, that's probably pretty good. So, let's keep moving here.
[25:59] So, we just updated the contract. Hey, what's up? Thanks for joining. Just running through the contracts and documents section right now of the tutorial. There's one point where they tell
[26:23] you to put your contract ID in the client itself, which they gave a reason for why you do that, which I forget. So, let me grab all this.
[26:41] All right. So, now we're going to submit the document. So, this is where we will write the message to the data contract that we just created.
[27:08] So, this is great. This is very similar to when I was first learning how to use Ethereum. I created a tutorial that did something basically like this. You create a -- they also call them contracts,
[27:20] called smart contracts, which would include the actual logic for, you know, what is being done with it, and then you would do a transaction with, like, your MetaMask wallet to update
[27:35] the message. So, this is similar to that. Hello from the stream. And then what it does here, it hopefully just tells you the exact time the message was written.
[27:55] And then it will be there until the end of time, until our machines turn to dust. Okay. So, let's kind of break down. There's the note document we create,
[28:14] and then there's this broadcast function, which takes the create thing here. And also your identity. So, you feed it the identity, along with the document you want to
[28:30] write, and then you broadcast it. So, that's probably all good. Let's go ahead and -- oh, hold on. So, what I also want to do is I want to get the document ID. Okay.
[28:51] Let me just start with Y. I think it might work. We'll see whether it does or not. Okay. Okay. So, this is hopefully going to give us back this, and then also this.
[29:43] Okay. Something messed up. Identity ID is not associated with a wallet.
[29:55] What do you mean? How can it not be associated with a wallet? Or it's not synced. Interesting. Interesting.
[30:10] Okay. Let me try retrieving my identities. I did create a couple. But they should all be associated with a wallet.
[30:36] How do you create an ID without it being associated with a wallet? Okay. So, let me try this and go back to registering the contract.
[31:02] And let me try this one this time. Actually, no. Let's try that.
[31:24] Okay. Then I'll use this contract. I'm going to hard code this in over here.
[31:47] Okay. Let me grab that identity ID one more time. Okay.
[32:16] Insufficient. Okay. That's fine. So, it said I had insufficient balance needed to top up.
[32:49] Oh, actually, I ran into this before. So, we fixed something in the docs for the top up identity.
[33:00] But this needs to be, like, this used to say 1,000 in this tutorial. And I changed it to 100,000. And I'm storing it into this error.
[33:09] Because it needs to be, like, a million, billion, trillion. Like, some really, really, really large ridiculous number.
[33:15] So, this is not ideal. But these, like, ridiculously large decimal places and stuff like that. So, yeah.
[33:27] I don't know. That's obviously not something for me to fix. Okay. So, not enough balance to cover that.
[33:36] So, let's try a little less. We'll work backwards until it eventually works.
[33:43] Because the amount I got from the faucet should be plenty. I was able to do all this last time. Okay. That's fine.
[33:54] More. It's like you look at this. Like, not enough balance to cover this.
[34:10] So, what is this? What is this? So, that's 414 million. This is a billion. So, now it should be
[34:23] 100 million, I think, is what I asked for. Need some scientific notation up in here.
[34:30] It looks like it's going to work, unless I don't have enough for each identity. Because for simplicity, I kind of changed this around.
[34:45] So, when you retrieve your identities, they give you all of them. When you top up, it does it to all of them, but that's not really a super smart idea.
[34:55] Okay. So, hopefully that did it. And if not, I'll use this one to create it next time.
[35:17] Looks like we got something. Great. Okay. That worked. And we got the document ID. That's great. Okay.
[35:24] So, this was 1, 2, 3, 1, 2, 3. So, 100 million is really what this should be. All right. Cool.
[35:47] So, now we'll have more stuff on the change of view, I think. So, we just submitted the document. So, that's after all this, after that.
[36:11] Okay. So, that's the document ID. So, let's go back to this. Actually, let me start from the identity. What was the identity I was just using?
[36:42] Okay. So, this should have documents now. There we go. Okay. There we go. Hey, look at that. But that's not the one I just created, though.
[37:02] Didn't say hello from the stream. Oh, no, I didn't. Where did I change that?
[37:22] Interesting. Cool, cool. So, we're gonna want a screenshot of that.
[37:44] For sure. That's where this whole exercise is just for this. The entire tutorial exists for this moment when you get this message and you say,
[37:55] yes, I did, I'm a real developer now. It's a fantastic moment. Okay. Thanks for the thumbs up. Yeah, so, you know, I learned to code probably,
[38:18] you know, like, five years ago or something, and I still vividly remember the times when just getting to this hello world felt like the most challenging thing I'd ever had to do in my
[38:29] entire life. And I didn't have chat GPT to help me. Man, kids these days, they have no idea how good they have it. Great. And then does it show up as transaction?
[39:05] That's okay. I'll look into that later. Yeah, I guess this is just for you. Okay. So, let's keep moving. So, now we're gonna do the get documents
[39:36] document. Okay. So, this is gonna give you back five. So, because you can create as many, you know,
[40:00] you submit as many note documents as you want with as many messages as you want. But if you are querying the blockchain and always want just everything,
[40:11] is that gonna be an issue if there's too much stuff? All right. There we go. So, there's the last five messages. Cool.
[40:21] Great, great. I did this in reverse. That's supposed to be after update. Okay. So, now we can update this.
[40:42] And then let me just double check. I got all the right things in.
[41:01] That's good. That's correct. Where was the other thing I hired? Oh, it's in here. Contract ID.
[41:34] Okay. That should all be good. So, hopefully that wasn't the issue earlier. Okay. So, here. Where is the message?
[41:56] Okay. So,
[42:15] contract not found. It might be that I was pulling the wrong document ID. Yeah.
[42:44] Okay. So, oh, I never copy pasted at all, did I? There we go. I missed this. Okay. Let's try that again.
[43:14] Expanding quotes around that. Here. There we go. Quotes.
[43:33] Quotes. Quotes. Okay. Okay. Now, I think that'll work. Great. Okay. So, we see here it's logging the thing. Great.
[44:12] Let's get the message a little more prominent. Let's see if that works.
[44:50] So, so,
[45:09] great. Yep. Cool. There we go. Awesome.
[45:32] Whoops. That's not a full line break there. Okay.
[45:58] Cool. Cool. So, next is deleting the document. Actually, hold on. There should be stuff back here.
[46:27] Cool. Another question is where are those transactions coming in? Okay. I think what might be happening here is the transactions need to be flipped around
[46:41] because it starts with the oldest one, and then it goes, but then it runs out after 1, 2, 3, 4, 5, 6, 7, 8, 9, 10. And I don't see any pagination. So,
[46:54] that might just be something that needs to be updated in Platform Explorer. Because it should have 14 transactions. Okay. All good.
[47:18] All right. Almost there. Almost there. And after we do this, I'm going to try and spin up a Next.js project and get the React code I had last time working in that, which should be trivial.
[47:48] Should be. We'll see. Whoops. Great.
[48:15] Yep. Message deleted. Okay. Sweet. And then the Express thing already got running. You know, the point of the Express
[48:39] example is that if you want to just use a regular old React front-end, you also need an API. So, this shows you how to get an API set up with Express. Then I was thinking, you know, we're
[48:52] then going to migrate that to a Next.js project with API routes that use serverless functions to handle this instead. And I think it might make more sense to just skip right past the Express
[49:05] part and show how to combine them with Next. Just go straight to Next. But we'll see. I got to first create the next project before I can decide that. So, this is good to run, I think. And then here,
[49:23] if we try and curl this or actually let's see what happens when we just open it up over here. Okay. Yeah. Wait, hold on. I want to I know what I want. You got to actually give it the
[49:41] name you want to see. So, let's do that. There we go. Okay. So, this is the identity that I created today.
[50:02] Stream test 2024, April 10th. And then we got all this information here. Cool. So, that's good. And then what we want to do now is get the React part set up.
[50:29] Okay. So, yeah. Okay. Let's do that. So,
[50:46] yeah. I always like doing setting up projects noninteractively. So, we're going to have to decide all of them. Actually, I'm not going to do that in the tutorial.
[51:22] I am going to save it for myself. I'm just going to call it text.
[51:50] Probably going to want to do app router in the future. Definitely want an SRC.
[52:03] And then I like to use NPM. Well, I don't like to use NPM. I do use NPM because too many other issues with creating tutorials with the others.
[52:29] Okay. So, that should do basically what I want. I think. Let's see. Let's see what happens.
[52:47] No, that's not what I want. Okay. So, I do have to say, no, I don't want ESLint. Okay. I got you a problem on that. Let's go back.
[53:24] Okay. I think that might be it. There we go. I left just that for a bit of readability. Okay. So, let's try this now.
[53:47] Okay. Hey, yo.
[54:06] Great. It's using a template, though. App TW. Maybe that's because I said app router. It has to pick some template.
[54:16] All right. That seems to have done it. And I'm going to, you know, let's do it here.
[54:45] I think it's going to be NPM run dev. Yep. Okay. So, here's going to be our next JS.
[55:11] Boilerplate. So, let's start by getting rid of all that. Okay.
[55:27] So, um,
[56:05] okay. It might actually want to put that off this. So, it's centered. Yep.
[56:12] Okay. Great. Okay. Cool.
[56:38] It's just something I like to do with Tailwind to keep the styles clean. Make the HTML, I should say, clean. What if we did that? What's that going to do?
[57:07] Now it's centered. Keep that.
[57:27] Call it content, I guess. There's a better variable name for that, but that's what we're going to get. Cool. Is this really far down because of this thing?
[57:50] Where's that Z10? That might be something to do with the global CSS.
[58:01] That doesn't look like it. Or the layout is probably. Is there any? No? Huh.
[58:16] There we go. This is what makes it wants to use the whole height of the screen.
[58:41] That's the createReactExample is the same thing. I've never liked that default. Okay. Great.
[58:50] Okay. One more thing. Okay. Look at that. I know Tailwind. Yeah. Cool. Now we're talking.
[59:18] Yeah. I've finally been learning CSS and Tailwind, what, like, three years without really knowing it all, and then every time I want to make my website look better,
[59:29] I would have a bad time. This is a pretty good setup. Yeah, I just do a little bit of Tailwind, get a nice default,
[59:39] and once you learn the important utilities, like, you know, these kind of things, then you start really flying. Not sure if I want this, though. Yeah.
[59:49] And I'm going to want -- ooh, there's actually -- I can grab a dash font. I'm going to do -- I learned recently about these dash brand guidelines. Very important.
[60:06] Okay. So let's just do -- can we do Open Sans? Oh, come on. I guess I'll just do Font Sans. That'll be probably the closest right now.
[60:38] Instead of Font Mono. Yep. And then the header is supposed to be Montserrat.
[60:53] That might also be a -- ah, yeah. So that'll be a whole thing. Custom font.
[61:10] I guess it doesn't look that hard. All right. I'll do this another time. I'll make a note.
[61:34] Where did it go? There we go. Okay. That's pretty good.
[62:18] Okay. Cool, cool, cool. So now that I've got all of that, let me copy/paste this. Okay.
[62:54] Cool, cool, cool. So now I'm going to keep the express part. Running right now and try and do that before migrating it to next functions.
[63:31] So I think we still got this running over here. Good. Change that to 10. And copy/paste this into page, I guess. Let's see what's going to happen here.
[63:48] I want imports up there. Use effect here and then return this here.
[64:08] In theory, that should be it. Let's see in practice whether that's the case. Let's make sure -- oh, hey, hey. Yeah, I'm probably going to be finishing up soon, Ryan.
[64:27] And you'll be able to kind of watch the whole thing. Just been kind of, you know, making a lot of progress just adding screenshots and cleaning stuff up in the -- in, like,
[64:38] the console logs and things like that. So just last kind of, like, tweaking step. Make sure this is still active and happening. Yeah, that's still there.
[64:50] Heck, I hit my first server component bug. Oh, exciting. That's so exciting. Really, that's what everyone's been complaining about?
[65:03] Sometimes we get an error that says you forgot to use use client and then you put in use client and it works. That is -- does not seem like a huge issue to me. But boy, does Twitter disagree.
[65:18] Sweet. All right. We're in. We are in the next app. And that's the type of thing that the use effect will -- could happen on the server, I suppose.
[65:35] But last thing. Copy/paste all of that. And then list. Okay. Cool.
[66:02] So, so,
[66:18] so, so there's also added a fetch button as well. So you can click a button to trigger the identity
[66:45] instead of just having it fetch by default when the page renders. That's a little weird. That shouldn't be lighting up.
[66:52] Anyway, actually, I bet if I did that -- nope. Okay. So,
[67:22] hmm. Okay. And that's that. And then you'll also need the actual button.
[67:50] Okay. Okay. Let's see if that works.
[68:19] Hmm. Hmm.
[68:35] Errors. Okay.
[68:56] Fascinating. A precalc appears instead of P. Why not? You say so, Next. That's fine. That's fine.
[69:17] That should be fixed. That should be fixed. Boom, boom. Great. Okay. So, the fetch button does not look so hot because it does not look like a button. So more CSS to fix.
[69:47] Thanks, Next create template. Thanks a lot. They probably had a button, actually, a style when I first generated the app, I bet.
[70:03] I just want -- what is just the basic one? Let's see what their with tailwind one looks like, I guess. >> Yeah. >> Actually, hold on.
[70:35] I was supposed to not get tailwind. What the hell? Give me tailwind, anyway. That may give me ESLint also. You can't actually say false. You can't do the whole thing
[70:54] not interactively. Okay. Anyway. Okay. Maybe just do the whole thing again, I guess.
[71:19] And then after I look at the CSS for the button, I think I'm going to call it -- there may not even be any CSS for the button. Let's see. Actually, are there buttons at all here? No. It just has
[71:47] links. There's no buttons. That makes sense, I guess. Anyway. All right. Cool. So that is great. All right. Thanks, everyone, for joining. So next stream we'll be porting the express stuff
[72:11] into the next app so that it's just running purely on the API routes and getting your serverless functions to handle the endpoints and then deploy that. You know, obviously,
[72:25] Vercel is going to be the simplest, but I might include an example for IPFS because we've been talking about that more. I could use Fleek, which is like the Vercel for IPFS. That would be very,
[72:34] very simple. Or I can kind of just show how to do it with actual IPFS, which would be very, very complicated. But that will be a decision for next time. But, yeah. So this is getting
[72:46] pretty close to being done. And then once the tutorial is done, I guess I'll have to talk to Ryan to see what to do with it. You know, I can just publish it on my blog. We can kind of link
[72:55] it around the community or try to find a way to do it more officially. I'm not sure. But, yeah. Probably -- I'm not sure when the next time I'll stream this. I think I'll stream Friday.
[73:07] So if you want to see more, then -- oh, actually, Ryan sent me a message. Okay. Okay. Great. Awesome. Yeah. So I'll catch you guys probably on Friday
[73:28] around the same time of day. Later, everybody. Thanks for watching. 
