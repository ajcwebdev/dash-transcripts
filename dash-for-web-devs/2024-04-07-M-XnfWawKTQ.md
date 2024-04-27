---
showLink: "https://www.youtube.com/watch?v=M-XnfWawKTQ"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "End to End Dash Tutorial: Return of the Rion - 6c"
publishDate: "2024-04-07"
coverImage: "https://i.ytimg.com/vi/M-XnfWawKTQ/maxresdefault.jpg"
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

[00:00] All right, hello, everyone. Welcome back to the Dash stream.
[00:09] Ryan will be joining me fairly soon, and, yeah, we're going to be working through more of the tutorials.
[00:16] Some of the stuff that was kind of broken was in the data contract things. I fixed one of them while just waiting for Ryan, though, so that's pretty cool.
[00:27] Let's go ahead and get some code set up here. Let me just double check.
[00:34] Ain't got any windows open. That's all good.
[00:38] Close that. Okay.
[00:40] And I'm going to shoot Ryan a message, too. Okay.
[00:49] I'm live! Woo!
[00:51] All right, sweet. So let's move this here and close that out.
[01:06] And actually, I should leave this open, at least in the corner, so I can see if Ryan joins.
[01:15] Okay. Okay, so the last part we were at was registering the data contract.
[01:29] I'm just going to close this, actually. Let me get the tutorial -- actually, I should push these changes first.
[01:48] Let's see. Actually, I should look at what changed so I can figure out what was broken.
[01:52] It looks like there was no position in the properties of the contract. So let's take a second and look at the docs for this.
[02:03] This is something that I know I don't understand super well. Yet.
[02:08] Because most of the time I spent working on this, over the summer, it was all around the wallet, the identity, the names, and that part of the service.
[02:19] So if we look at the platform itself, it's made up of a couple different things. And so what we were doing was the name, name service, DPNS was a big part of it.
[02:34] That's based around identities. But now we're going to the data contract part.
[02:42] So this is the storage. So Ryan always talks about SPA, storage, payments, and authentication.
[02:50] So the name service, you can think of it as kind of like the -- both, I guess, the identity and then once it's linked to your funds, it will be a component of the payments.
[03:02] But in terms of, like, what is the application, where does the data live, and all those kind of things, this is where our storage is.
[03:10] Now, one of the things we've talked about along this way, we had an interview with someone from -- somebody who used to work at IPFS, and we had a great discussion about IPFS and
[03:30] what decentralized solutions are. What is a DAP?
[03:35] Cool. I'm going to save a link to this over here.
[03:43] So, yeah, check this out. If you missed it, we had a great conversation around, you know, when is it a good idea to
[03:53] bring in something like IPFS and how does it relate to things like gateways and all of that nature.
[04:02] But with the data contract, this is something that is actually on the blockchain. This is not a separate decentralized distributed file storage thing like IPFS, and it's more,
[04:16] I guess, here it says it's grovdb. I don't know anything about grovdb.
[04:21] I'm assuming it was built -- yep, it was built for use with n-platform. Is it relational?
[04:29] Hierarchical authenticated data structure with efficient secondary index queries. I'm assuming that means it has to be relational if my database ignorance is not too high.
[04:41] Okay. So that's interesting.
[04:45] So that means, then, the data is not represented in just JSON blobs, which is what we had talked about in the past.
[04:52] So that's an important lesson right there. Let me go to the reference and let's kind of take a look at this.
[05:03] Okay. So the contracts are described in JSON schema, so it's both JSON schema, but stored in a
[05:08] relational database at the end of the day, or relational structure of some sorts. That's what that sounds like.
[05:15] Variety of constraints currently defined for security reasons. Interesting.
[05:22] Something I want to try, actually, just because I'm kind of waiting for Ryan, is -- I've been curious to try just -- I've noticed recently, so I use LLMs a lot to code, you know, chat2BT
[05:41] and stuff of that nature, and they have gotten much larger context windows recently, which basically means that now you could feed them a lot of code, or a lot of docs, and kind
[05:55] of preload it as -- you can kind of think of it like a really easy way to fine-tune a system.
[06:00] There used to be all these different hacks around how you would fine-tune things so you could get it to understand a code base that wasn't in the original training that the foundation
[06:07] models went through. So as the context windows have gotten larger, you can basically give them tons of code and
[06:14] docs and stuff and be like, hey, write me some examples of how to do this or that or whatever.
[06:19] And so I'm kind of curious. I just threw this entire data contracts thing, what would happen?
[06:24] So I just wanted to take that off so I could move my history away. But let's -- so basically what I would do is I would go -- you want to just feed it
[06:34] the actual markdown. Show source.
[06:37] This is a great button. I'm going to put this button here.
[06:39] Good job. I always have to click edit on GitHub and then bump one backwards and then go forwards,
[06:46] and that's how I would get to the -- and then hit raw. Single click.
[06:51] Look at that. I'm going to put this here as a genius.
[06:54] Okay. So let's do this.
[06:56] And then you want to give it some context. These are -- actually, this is a reference for working with data contracts on dash platform.
[07:16] Then write a brief one paragraph description of what a data contract is and what it is for on dash, then write code examples for -- let's see.
[07:35] I'm just kind of curious what it would do if you just asked it to do literally these things.
[07:42] Let's try both of those. Okay.
[08:01] Just write. Okay.
[08:03] That should be interesting. Okay.
[08:05] Data contract on the dash platform serves as a blueprint for the structure of data that an application tends to store on the decentralized network, if that makes sense.
[08:20] It defines the schema of documents, which are called data records, using JSON schema, enabling the platform to validate data against these schemas to ensure consistency and integrity.
[08:29] They're crucial for DAP, Delton, and Dash, so you need a structured, predictable way to interact with the blockchain, facilitating data storage, retrieval, and manipulation
[08:38] in a trustless environment. Okay.
[08:40] So it does make sense to kind of think of it like a database, because you still wouldn't store an image in a database, unless you're kind of silly.
[08:48] But this is registering -- actually, I'm going to say make sure to use DSM, if at all, code examples, and do semi-colons, obviously.
[09:01] Where's Ryan's going to go? Okay.
[09:16] So it -- ah! It punched on the third one.
[09:24] That's funny. So it says, "Go back to register -- to register a new data contract, you construct a contract
[09:29] object following the schema constraints, and submit the object within a data contract create state transition."
[09:36] Interesting. So state transition also has a protocol reference over here.
[09:49] "Means for submitting data that creates, updates, or deletes platform data results in a change to a new state."
[09:55] That makes plenty of sense. So it's like, when you write -- so I'm going to go -- when I've worked with stuff like
[10:03] this before, you know, it was usually with Ethereum. So I know with Ethereum, I would create examples where you would upload a smart contract, and
[10:12] that smart contract would have a little bit of code in it, that would be like a Hello World example, where you could write a little message, and then display it, and then you
[10:21] could read it back for the blockchain, and then you could update it, and then you could read it back, or, you know, but you can't delete it, can't delete anything on the blockchain.
[10:29] That's what I always say. So this is taking that part of it, and kind of making the update one in particular explicit,
[10:38] is what this sounds like. So let's see.
[10:45] And then you're going to obviously -- so this is why -- and this is smart to make this its own kind of thing that's separate, because reading is free, but updating is not.
[10:54] Or writing -- and writing is not either, you know. So if you have a very -- when you're working with blockchain, you want it to be very read-heavy,
[11:00] because you can read from the blockchain as much as you want, over and over and over again. But if you want to write to it, then that's where you got to pay, because it's a limited
[11:08] amount of block space, with a limited amount of time, and a lot of people using it, because it's going to the moon right now.
[11:15] Like, Bitcoin's like 70k or something. So hopefully all that trickles down to some sweet Dash moonage.
[11:20] Okay. I think I'm getting ahead of myself, so I'm going to go back to the Jibbity.
[11:28] Okay. So...
[11:30] Let me just see the -- I'm just going to grab some of these. I'm not going to just publish these, and this is kind of just how I get myself stuff to
[11:45] work with as materials, I write tutorials now. It's pretty great, actually.
[11:49] Let's see. So I was on -- yeah.
[11:51] So I lost out on a day of contracts. There you go.
[11:53] Let me make this bigger, actually. Okay.
[11:55] So... Okay.
[11:57] So... Okay.
[11:59] Let me make this bigger, actually. Just to clean this up a bit.
[12:27] It's the one thing, unless you explicitly say, be more concise, it's a little wordy. Okay.
[12:58] That's good. That's clean.
[13:00] I like that a lot, actually. That's a very, very clean definition right there.
[13:02] It defines the schema of documents. So, schema...
[13:32] I'm just going to start saying contracts, so I don't have to keep saying data contracts over and over again.
[13:41] Contracts enable a platform to validate data against the schema to ensure consistency and integrity.
[13:47] They provide a structure in particular way to interact with dash blockchain. Reuse dApps yet?
[14:06] Yes. We use dApps way back there.
[14:08] Great. I don't need to define it.
[14:10] Okay. There we go.
[14:18] That's pretty good. Oh, there we go.
[14:28] Right. It'll be on in about five minutes.
[14:32] That's good. So far...
[14:34] Let me go back to my code. That was already broken.
[14:36] I think I was able to register the contract. It was this thing right here.
[14:41] Cool. Yeah, baby.
[14:43] Cool. Copy/paste all of this into the docs.
[14:49] Oops. Yeah.
[14:51] Great. Yeah.
[14:53] And he told me testnet is back up today, so maybe that means this is broken and now it is healed.
[15:10] Who knows? Another thing I like to do is output after running register data contract if you will.
[15:34] Just register contract. [15:35], I think.
[15:36] I kind of like this example. This example looks a lot cleaner.
[15:56] Okay. Let me see if this actually works, though, first, before I do anything ridiculous.
[16:19] That's definitely -- this is slightly different. So let's see what happens.
[16:36] It's going to be interesting. Let's do that.
[16:38] And that. And identity ID.
[16:40] Go here. Let's see if that works now.
[17:10] Interesting. Yeah, I do this, I guess.
[17:38] Maybe this did not work as well as I thought it would have. Okay.
[17:50] Let's just shove all that for now. Interesting experiment.
[17:53] I think that's going to go back to working. Yeah, let's stick with that.
[17:58] Let's see. Oh, yes.
[18:00] I'm going ahead, though. Okay.
[18:02] So interesting. Let me see if this is even, like, in those docs at all.
[18:17] Okay. Why would you do that?
[18:23] It just doesn't -- oh, so I guess it didn't have any of the client stuff in the actual -- let me just try this.
[18:30] I'm going to just grab this part of the code, leave out the platform stuff. And let's see if that works.
[18:59] No. Wait.
[19:01] I do that part, too. Yes.
[19:06] That's the only part of this. No client at all.
[19:11] So it needs at least this, I guess. If any part comes up there.
[19:25] There? I should get a contract.
[19:33] Yes, contract.create. Huh.
[19:36] Okay. Maybe there's just not enough examples in here for it to understand what's happening
[19:46] based on -- yes, the functions of what we're doing might just be in the tutorial, not necessarily here.
[19:57] Okay. Yeah, this is where -- oh, wait, I think Ryan is almost here.
[20:08] Can I add you to the stage or -- let me probably add myself. Okay.
[20:20] So we were able to register a data contract. Let me just kind of reset from where I just was.
[20:34] Okay. That's working again.
[20:43] Oops. Okay.
[20:47] We're back, and I'll trust Ryan will join when he is ready. Okay.
[20:54] So definitely make sure to push those changes. Don't want to lose this last thing.
[21:03] Make sure this works. Okay.
[21:06] Great. Great.
[21:08] Great. Okay.
[21:10] And then make sure the tutorial has the most up-to-date code. That's important.
[21:29] So let's grab this and that. And then go to here.
[21:36] Great. Great.
[21:38] Great. And then let's see if we can retrieve this guy and see what happens.
[21:49] I hear sound. >> Howdy.
[21:53] >> Hey. What's up?
[21:55] >> Hello. >> Let me just run this real quick.
[21:58] >> Yeah. What are you talking about?
[22:01] >> Oh, you know, coding, I'm going to just real quick see if this thing works, and then we can chat.
[22:07] I don't even think I have a -- yeah, so I got some of the -- my bugs actually fixed already, which is cool.
[22:23] So npm run, retrieve contract, and let's get the identity ID in there. I'm trying to figure out how to get the resolution on my end to be a little higher, so --
[22:39] >> Oh, actually, and I'm glad you said that. We are on the version right now where we only get 720 instead of 1080, I think.
[22:48] We should definitely bump that to 1080, just because, like, for coding examples and stuff, it makes a pretty big difference.
[22:53] >> Yeah. And on the other hand, sometimes it's better to have larger text instead and not rely on
[23:01] high pixel count, but -- >> Well, mostly you need to rely -- it's not an either/or.
[23:06] You want both, ideally. >> Yeah.
[23:08] You want both. >> Because then someone might even be on their phone, you know?
[23:11] >> Yeah, for sure. >> Not super tight.
[23:14] >> I'm kind of surprised. Yeah, it doesn't look great on my screen, and it doesn't even look like 720 to me, but
[23:22] maybe it is. Anyway, what did I miss?
[23:27] Sorry, I was later than we had planned. All good.
[23:31] I'm just going to -- so I'm working through the data contract stuff. I've got all these tabs open, and now I'm confused.
[23:42] >> So my first question is, have you seen the new documentation page? I don't know if it's published yet, and if it is, it might be under something that's
[23:54] not the main site. I'm going to look it up right now.
[23:57] >> Could you grab the link and just send it to me? >> I'll send it to you.
[24:03] I just know that there were some changes made on GitHub issues. I don't know if they're merged in and deployed to the dash.org yet, but I'll check that.
[24:20] I'll send it to you. >> Okay.
[24:50] >> All right. >> Yeah, I don't think the changes are up on the website yet.
[25:40] Basically, the documentation lead over at Dash Core Group has made some changes to separate out the creation of the client along with documenting more of the options that the client
[25:59] accepts, but I don't think that those changes have made it to dash.org yet, so I was looking in GitHub to see if I could see a preview of what it looks like so that we could test
[26:15] whether or not those changes actually work. But while I'm doing that, can you give me a little update on bugs that are you still
[26:32] -- have you started over again, because we do have a new test net now. Test net has been updated to, I believe, dash platform 1.0.0 dev 10 where it was dev 9 before.
[26:53] So let's update dependencies. >> Yeah, it's 10 now.
[26:56] >> It's 10 now. >> Oh, yeah.
[26:58] >> But instead of writing 10 -- >> No, I wasn't going to. I was about to go and find the -- there's a specific way you set latest that -- yeah.
[27:11] >> So that will -- yeah, that will take care of -- that will give us the latest dash SDK. And then in addition to that, all the nodes on test net are -- should be running that
[27:25] new version as well, and on top of the new platform versions, I believe, but I'm not sure that the test net nodes are probably also running core version -- there was an
[27:43] update on core as well for a small bug fix as well. It shouldn't affect our work, but there were -- yeah, there were two releases, dash platform
[27:51] and dash core both got an update, and I think that test net has nodes that are running those updates.
[27:59] So I'm hoping that we either see -- >> I got the same error I got. As far as I can tell, this is exactly how it's written in the docs.
[28:07] So I think I do have something. So this is during the retrieve a data contract part.
[28:12] Maybe that -- let me just make sure I'm actually getting the right ID and I understand what's happening here.
[28:19] So this is the -- oh, so this is the ID. So that's me.
[28:23] That's a user error. So let me make sure that's correct first and see what happens.
[28:29] All right. There we go.
[28:31] Cool. So that is the step in my tutorial where I need to give you that specific environment
[28:38] variable back, because that's what I've been doing throughout this, so someone can just copy/paste that, because when I looked at it, there's two IDs.
[28:46] There's an ID here and an ID here, so that can be kind of confusing if you're, like, blown through the tutorial and not reading what the heck anything is like someone like
[28:55] me would do. >> Yeah.
[29:00] So let's back up just a little bit and give a brief introduction, if you haven't already, to what we're trying to do here.
[29:08] >> Yeah. So what we're trying to do here is basically I am taking essentially the whole of the dash
[29:15] docs and kind of creating a single end-to-end tutorial so that you would go through all the kind of important parts of creating the wallet, getting your identity and name registered,
[29:25] and then working with your data contract stuff. And I got everything up to the data contract stuff working back in last summer, and so
[29:35] now we're kind of working through the storage part, and this is something that now I'm kind of learning what even is a data contract, because I didn't really figure that out last
[29:43] time and worked with it too much, and there was one thing that came up, actually, that I wanted to ask you about, but is there anything more general high-level you wanted to hit
[29:51] on first? >> Well, yeah, just the screen that you're looking at right here.
[29:56] So did you -- you mentioned in your little intro there that last summer you were able to get through this -- to this step, but now that there's updates, were you able to connect
[30:09] to the network, create and fund a wallet, and go through the identity and names, all of those?
[30:18] Let's do that right now. Let's see what happens.
[30:20] I don't see any reason why it wouldn't work, but we'll see. So let me go back to here, and I'll wipe out my .env, and let me first actually get this
[30:46] over here. And in the bottom, you have terminal session, and you just ran a command, npm run create
[31:19] wallet. >> So this should be what I want, actually, so this, and then this is going to work this
[31:25] time. Yep.
[31:27] So this is -- >> Create wallet is -- is that an alias? If you scroll back up to create wallet, is that an NPM script that aliases to Cloud.js?
[31:38] >> So let me explain. All the scripts work exactly the same way, which is that they're all in a directory called
[31:43] scripts, and then they have a name, and then I aliased basically just running node to run that script to the exact same name, so you could do NPM run the name, or node scripts
[31:54] the name. Both will work.
[31:56] >> Yep. So the create wallet one that you just ran is going node scripts/create wallet?
[32:02] >> Yep. Which is this file right here.
[32:06] >> Okay. >> So in the terminal block down below, presumably that ran this code, which is creating -- it's
[32:16] getting the client from client.js, which you had open a little bit ago, and then trying to create the wallet from that instantiated.
[32:26] The reason I'm going through the, like, in deeper detail what you've done is because I have this weird hunch that creating a client and importing it from module to module may
[32:41] have some issue that I want to get down to the bottom of, at least rule it out. >> What issue are you referring to?
[32:52] >> Well, expand your terminal again, and did you run into an error just now as you ran that?
[32:59] >> No. The thing before was -- no, the error before was that I had the wrong code in there.
[33:03] The command worked. Just as expected.
[33:05] >> Okay. The command --
[33:07] >> Yeah, everything works just fine. Nothing's broken right now.
[33:09] There's no broken code. >> Okay, good.
[33:11] So far so good. >> Yeah.
[33:13] >> So create wallet you just did, and it gives you back the wallet and the mnemonic. It gives you back a wallet address and a mnemonic.
[33:24] Got it. So you can paste that and put it into your .env for the next couple of steps.
[33:31] >> Okay. And you did that -- you're doing that now?
[33:34] >> Yeah. >> Did it give you a different -- when you create the wallet, it's going to create a
[33:46] random wallet. So this is -- so you're updating your -- you're updating your environment variables now with
[33:54] the latest greatest that we just ran right now. >> Yeah, exactly.
[33:58] And there's nothing else in there except network set to test net. That's the only environment variable you start set, and then you build them up piece by piece
[34:06] as you go through the scripts. >> Okay.
[34:09] So now let's do the next step. >> And then I'll also keep these updated with the actual tutorial as well, just keep sanity
[34:17] in check. >> Yes.
[34:19] So I think we've got to give it some test net funds, that's the step here. Always a fun step, it's my favorite part, do it every time.
[34:34] And then you wait. You wait for the site to crash, that's how you know it worked.
[34:38] >> Yeah. >> Do you know why that happens, or if we could talk about fixing that, or if I could
[34:43] find another way to host this so that that doesn't happen? >> I don't know right off hand.
[34:49] All I know is that this faucet is a fork of a fork of a fork. It's from way early back when-
[34:58] >> Well, then can I just fork the current one and then deploy a brand new one? >> You could, but I don't know if it's the deployed version that's the problem, or if
[35:06] it's the actual source code that's just buggy. >> But even if it is, the front end can handle that.
[35:12] If it's breaking for some reason, or the front end, this should never, ever, ever happen on a web page.
[35:17] >> No, I get it. I think that you'll find, though, that it's not the most easy to use front end.
[35:24] >> Well, then I'll rewrite the front end, is what I'm saying. >> Yeah, and I think-
[35:29] >> It's just HTML and CSS. It can't be that hard.
[35:31] >> I think it's, I think it's something different. I don't think it's JavaScript.
[35:36] I think there's a backend that's, you know, some- >> What I'm saying, but regardless of what the backend is throwing, the front end shouldn't
[35:43] need to crash. The front end shouldn't be coupled to something that's breaking on the backend.
[35:48] Like, it just doesn't make any, I don't know, like, I understand how it's broken in a way that's causing it to do that, but I'm saying there's no reason that can't be fixed by someone
[35:56] who could figure out what's wrong with it. >> Yeah, it's not a big priority for me, but like, and if you, maybe what we need to do
[36:03] is- >> But not the onboarding experience.
[36:05] If every single person has that first onboarding experience, every person needs to add phones to their wall, and every person goes in, and it breaks, and they don't know whether it
[36:10] works or not, because they don't get any feedback. >> No, you're absolutely right, and I'm not disputing that.
[36:15] I'm just saying maybe the workaround right now is to use a different faucet by default. Like, I know that the Crowdnode guy-
[36:24] >> Yes, I don't know any others, so that's what I need to know, like, what is the next most reliable faucet that I should use?
[36:31] >> Yeah, that's, I'm going to go into Discord. I'm going into Discord, the Dash Discord channel, and-
[36:39] >> And I don't even need to put it in the tutorial, if you want to keep it secret so people don't wreck the fun, but I would like to, I'd be curious to know.
[36:47] >> I was just telling people so that people could know also, the Dash Discord testnet channel, you click on the channel description, and there-
[36:55] >> Do you want to share your screen with them in one second? >> It's fine right now.
[37:01] I just see the one faucet. I was just checking to see if there were multiple faucets linked in here, so that's one of those
[37:09] things. Let's make a note of this and we'll ping, I'll just do it right now, I'll just, let's
[37:20] see. >> There we go.
[37:24] Is this an actual faucet? That's weird.
[37:33] I thought that you had the Crowdnode faucet somewhere in your docs already. Maybe not.
[37:42] >> So the only one in the docs has been this one that I've been using the whole time. >> Let's try this one.
[38:02] I'm just going to make a note here. Is there a better testnet?
[38:11] Channel description. Yeah, there's a bunch of other stuff that comes up if you Google it, but they're not
[38:38] really faucets. They're, like, trying to drive people to buy stuff and things.
[38:43] I guess you have to sign up also, which is, like, I know Ryan would not approve of that, so.
[38:56] >> No. I would not.
[38:58] >> Yeah. Definitely not.
[39:00] >> All right. Well, for now, let's move on to the next step.
[39:04] Did you get the coins? >> I'm assuming so, yeah.
[39:08] So let's check a block explorer. Yep, let's do that.
[39:14] And if you haven't got that in your notes -- >> I did.
[39:17] I've gone through these steps, like, ten times. All these ones are good, trust me.
[39:22] >> Okay. Cool.
[39:24] >> Yeah. So we got three confirmations.
[39:26] We got .2 dash in there. >> Okay.
[39:28] >> Oh, real quick, while I'm playing this, what is a credit? A credit is a smaller denomination of dash.
[39:40] So it is -- >> Oh, it's like Satoshi.
[39:42] >> Yeah. It's like Satoshi, but even smaller.
[39:44] I think it's a thousand, possibly a million. I think it's a thousand, though, credits per Satoshi.
[39:56] And that -- >> What does it mean to top up something?
[39:58] Sorry, what was the last thing you said? >> I said that also should be documented somewhere.
[40:05] If it's not, then it probably should be. Let me see where it comes up in sense -- I'll know what that means later.
[40:21] So I was looking at the top-up identity one, and let's see. It might define it earlier.
[40:42] >> Right here is the link. It says additional details regarding credits.
[40:46] >> There we go. This is not a definition of what a credit is, though.
[40:52] This is telling us about something that was added on. This is -- I don't think this needs to be here.
[40:59] I guess not someone's working with older code. But hold on.
[41:03] So back at that, additional details around credits can be found in the credits description. Yeah, see, I don't think this is a credits description.
[41:10] This is -- >> Credits provide the mechanism for paying fees that cover the cost of platform usage.
[41:17] >> Hold on. Where does it say that?
[41:19] So it defines it in this doc, but it doesn't higher up. So that link should -- well, okay.
[41:24] No, I think I understand what's happening here. It's just a little confusing as to how it's linked.
[41:31] Lots of credits established. See, I think -- oh, sorry.
[41:38] Yeah, it's just a little bit. But it still doesn't really say anywhere that it's a smaller denomination.
[41:48] This is the first time it's mentioned on this page. It says each identity also has a balance of credits as established by locking funds on
[41:56] layer one. They're used to pay fees.
[41:58] And it gives you a link to this, which says they provide the mechanism for paying fees that cover the cost of platform usage.
[42:03] They lock Dash and proof of ownership. So -- but reading all this, I wouldn't know how it's different from just the actual cryptocurrency.
[42:13] You know, the money itself. So I'm not sure if it does say anywhere specifically that it's a smaller denomination.
[42:18] Yeah, I was just reading the description, and I agree with you. It's not enough to know -- It just needs a single sentence, you know?
[42:26] Like, right here. Because that's where the link goes.
[42:28] You want to put it right here before this note. Just say, "Credits are a butt," and just give a single line description right here.
[42:33] That's what you want. Let's make an issue.
[42:35] I'll fix everything. Let's make an issue right now.
[42:37] Actually, let me make a PR. Screw that.
[42:39] This is so simple. There's no way I can not PR this.
[42:44] Okay. I like it.
[42:46] No, it's a single line markdown change. This is my specialty for PRs.
[42:52] Yeah. And this is the purpose of this stream, right?
[42:56] The purpose of this stream is to go through the steps of the tutorial, make sure that all of our questions are answered, and if they're not answered, then we do our best
[43:06] to try to provide those answers ourselves, and, you know, if Dash Core Group wants to spice up or spruce up whatever we suggest, that's even better, but let's give it our
[43:19] best shot. Let me just make sure I'm on the most recent version.
[43:23] I think I am. Yeah.
[43:25] Cool. So I'm just going to go straight to that link.
[43:27] It's going to be right here. So it took you to 25.
[43:42] Yeah. There you go.
[43:44] Now we're in 1.0 dev. And then the credits thing was right here, right?
[43:56] So then I want to be on AJC Web Devs. There we go.
[44:06] Okay. You should give me the exact specific wording, though, because you're the guy.
[44:14] I see. You're throwing it back on me now.
[44:16] I see. I was going to say, let me write back what you've told me, and you can tell me whether
[44:20] it's correct or not. Well, the thing is, I'm not sure.
[44:23] So I heard somewhere sometime that it was a thousand or a million, but I'm not sure if what I heard was, if I'm remembering it correctly, or even if they have changed it
[44:38] since then. Because I know this was like years ago that I remember.
[44:44] So let's get off the Dash platform docs. Let's go to the original Dash docs, right?
[44:50] There's a separate one. Is there a separate one for that?
[44:52] I know there used to be. Do you know?
[44:55] There are multiple docs. There are user docs and developer docs.
[45:01] This is part of the issue. We're going to go to the core.
[45:03] Oh, yeah. No, this is definitely different.
[45:05] Okay. So let's go with this.
[45:07] We'll see how they define credits here. So they call them identity credits instead of just credits.
[45:23] Okay, "The life cycle of an identity is built with multiple different underlying state transitions. However, before an identity can be created, a special transaction that transforms Dash
[45:36] into credits must take place." Wow.
[45:40] That is so useful. That has not made sense to me.
[45:45] Okay. But that description is even not good enough yet.
[45:51] It may be down the paragraph here. But the important thing is...
[45:55] But it connects it to what it has to do with the identity. Yeah.
[46:00] So let me just explain it conceptually as a high-level description. What you do when you're creating credits is you're locking Dash on the layer one blockchain,
[46:13] the payments blockchain, the proof-of-work blockchain. You're locking Dash in there and creating a transaction to do that lock.
[46:23] And then it's unlocking... At the same time, it's unlocking Dash on the platform chain.
[46:30] So it's creating Dash on the platform proof-of-stake chain in the same amount that you have locked on the proof-of-work chain.
[46:40] Now, I don't know if they explain that. I guess let's just keep on reading and see if they explain that.
[46:46] Real quick, though. So if that's the case, then I don't think it makes sense to say it's like just another
[46:51] way to subdivide Dash, because it sounds like there's a lot more involved with where it exists.
[46:58] It is more involved. And the explanation, it takes several steps, obviously.
[47:03] So it depends... The first sentence that I give you is going to be context-dependent.
[47:09] I think that... My question is, if someone is just using Dash cryptocurrency, do they encounter credits?
[47:17] Or is it something that only people building the apps with it encounter? So normally, people don't encounter or use credits.
[47:31] In fact, on Mainnet, nobody even has... This is not even a thing.
[47:35] On Testnet, it is a thing. Because of identities.
[47:37] So there's no namespacing on the current chain. Say that again?
[47:44] So basically, the name service thing, what's it called? DPNS, I think, something like that.
[47:51] So that does not exist on Dash. That's correct.
[47:56] Layer 1. There's no proof-of-work, payments chain.
[47:59] That does not exist. All right.
[48:01] That makes sense. So that is why...
[48:03] So this is... You never encounter credits if you're working with Dash.
[48:05] This is an important topic. Yeah.
[48:07] No. I'm seeing now.
[48:09] Yes. Yeah.
[48:11] This is the bridge that connects the proof-of-work chain to the proof-of-stake chain in a way that...
[48:18] And there's some fancy cryptography behind this that only Quantum Explorer, Sam Westrich, CTO of Dash Core Group, really fully understands, or several people there in Dash Core Group.
[48:29] I don't fully understand it. But there is cryptographic proof that it's not like...
[48:37] You're not able to create extra coins on the proof-of-stake chain that you haven't... In one and the same transaction, or at least several transactions that occur that haven't
[48:53] been locked on the proof-of-work chain. So yeah, the credits in the end...
[49:01] I don't know. This is one of those things from a product...
[49:05] If I were a product manager at Dash Core Group, this is one of the things that I would be wondering about, if this is even a good idea to have this separate term, credits.
[49:18] And it's something that you and I, as we bring Dash Platform to Web2 developers, we have a say in this as well.
[49:31] Is this term, Dash Credits and Platform Credits, is it going to be more helpful than harmful? Or should we suggest that maybe we do away with something like this?
[49:44] So it sounds like, I think I'm starting to get this a little bit, it says here, so basically the credits are something that you're going to be using every time you need to interact
[49:53] with the thing. So you may or may not know this, but do you know how this relates to the concept of gas
[49:59] on Ethereum? That's exactly what it is.
[50:02] Then that's all you got to say. I mean, at least if you want to compare it.
[50:05] No, not necessarily, because we're not targeting somebody that has a thorough understanding of Ethereum.
[50:12] Yeah, sorry. Let me correct myself.
[50:14] That's what you could say to me, for it to make sense to me. I'm not saying write that in the docs, is what I meant.
[50:21] Yeah. But I could translate that to a definition that will be cleaner though, which is that
[50:27] as you interact with the chain, you need to provide a small amount of funds for the operation to succeed.
[50:34] Right? Yeah.
[50:36] Let's go back to where it's described, because this may be in there. We only read a couple of sentences.
[50:48] So I agree that this should be... I think this is the first time it's actually mentioned, because I'm not sure if it's mentioned
[50:59] earlier in the tutorial up until this point. So if this is the first time it's mentioned, that's where you want to make sure.
[51:07] It may even be up in the introduction for all we know. You might have to...
[51:12] There's only so many levels. You have to pop open all these.
[51:14] There's not that many. So yeah.
[51:16] Yeah. Okay.
[51:18] See, I know. The top up is the first time it's showing up.
[51:24] And this function is where I encountered this concept for the first time, and I was confused. So I think this is the first time it's mentioned, and this is where it would be good.
[51:32] So it says, "The purpose of this tutorial is to walk through the steps necessary to add credits to an identity's balance."
[51:37] And then it kind of says, "As you interact with it, the credit balance will decrease." So it doesn't kind of start with it.
[51:45] It kind of jumps into it already talking about the credits without having defined it. I think that's probably where it makes most sense, then, actually, is to define it here
[51:54] instead of defining it... I mean, you want to define it probably in both places, but in terms of if you're just
[52:01] walking through this tutorial, just this would be a good place to have a one-sentence description, I think.
[52:06] Mm-hmm. Okay.
[52:08] And do you want to take a stab at what that one-sentence description should be if this isn't sufficient?
[52:13] Sure. So...
[52:15] What should I do? Yeah.
[52:17] So I'm going to go back to here, and I don't want this page at all. I want the...
[52:31] Oops. I'm just going to get out of here.
[52:51] And we don't have to get the sentence exactly right to begin with. I think starting a PR is a good idea.
[52:59] That way, we can have the PR. They can know that there's a little bit of an issue with conceptually explaining what
[53:09] credits are before, because it is an important topic. And then we can just add on.
[53:16] As we go through the tutorial more, we can add on to that. And I want to go back to where they explained it earlier in the actual dash, for one...
[53:34] Give me just one quick second. So it was...
[53:55] So identity is created, special transaction, transforms dash into credits. Which are used to interact with the dash platform.
[54:22] Okay. I think to me, that would be something that would make sense to me, and that would explain
[54:30] what they are. And we should also add a sentence that says something about the unit conversion, if and
[54:37] when we find that. Yeah.
[54:39] So that's the thing. I don't know where that information is.
[54:41] So if you... Yeah.
[54:43] Do a placeholder sentence that says, yeah. Something like, one credit equals...
[54:51] Or no. One dash...
[54:57] The number one, though. The number one.
[54:59] Yes. One dash.
[55:01] The symbol equals 100,000,000. Let's put commas in there.
[55:11] No commas? Let's put commas in there.
[55:13] Oh, yeah. Yeah.
[55:15] 100,000,000 Satoshis. Comma or no comma for that?
[55:20] Should we see how they do it for... It's not a comma.
[55:27] Okay. Cool.
[55:29] Yeah. Equals...
[55:31] Like 100,000,000,000. Or you could just do question mark, question mark, credits.
[55:44] Yeah. Yeah.
[55:48] Okay. So I'll just commit this on my thing.
[55:54] I won't necessarily open the fork yet. Or do you want...
[55:56] Yeah. You can put commas on your fork, and then we can...
[56:01] You'll want to be consistent, whether you're uppercasing or lowercasing credits. And then, Satoshi's also is one of those things.
[56:13] I always uppercase dash, because in terms of units, I like to keep dash analogous to USD.
[56:23] Or BTC. Yeah.
[56:25] Or BTC. I always uppercase and whatnot.
[56:28] I don't know what the convention is or should be for Satoshi's and credits, but I think it's good enough for now.
[56:37] Great. Cool.
[56:41] That was a long rabbit hole for my question. That's good.
[56:51] I think that's great. It's important.
[56:53] That's the purpose here. Yeah.
[56:55] No, I dig it. Did you want to keep going along from where we were in the tutorial, where you just created
[57:00] a wallet? I was thinking back to a better way to describe that unit conversion thing, because it would
[57:14] also be better to write explicitly that one Satoshi equals 1000 credits. If I were the reader of this, I wouldn't want to have to decipher between the 100 million
[57:40] Satoshis equals 100 billion, or whatever number that is. I would want the definition in terms of stats.
[57:47] Yeah. I think you don't need to necessarily do the Satoshi conversion at all.
[57:51] You just say this is a smaller denomination, like how Satoshis are as well, or something like that.
[57:57] And you can just link to Satoshis. People can read about it more if they want.
[57:59] Yep. I think that would be the move.
[58:08] What is a Satoshi? You know what that is, right?
[58:14] Oh, yeah. Absolutely.
[58:16] Yeah. So that's what's interesting, though, is that it's like a Satoshi, it's also like gas in
[58:20] the theory. Again, I'm the type of person that compares and thinks it's helpful, so that's why I tend
[58:24] to frame them these ways. I know some people are like, "You don't want to talk about other projects, how they relate
[58:28] at all." But at least that to me is interesting, it's cool, because it helps you start to understand
[58:36] where the commonalities are of different projects. So that to me definitely just makes a lot of sense, because when I actually make real,
[58:44] when I use cryptocurrency, the times I use it, gas is always a thing, because you can pay more gas to get your transaction faster, or pay less gas, so it'll take longer.
[58:54] So I guess, does that exist, or is you just pay the credits and it just happens at whatever time it takes?
[59:01] In this system, in the Dash platform system, I believe it is deterministic. That's way better, way better.
[59:13] So in that way, it's not like gas, probably. That's the worst part about gas, you fix the problem with gas then.
[59:20] A certain transaction will cost a certain amount every time. And I don't think that there's a mechanism to speed that up, it's just, we have, it's
[59:33] fast by default, and if there's a problem with that, there is going to be a mechanism where we can change those rates, which, like allocating this amount of memory costs X amount
[59:48] of credits, doing a certain amount of processing costs another. And then, so like, Ethereum has this as well, where certain operations, low level operations,
[60:03] there is a table of costs, and then certain transactions will map to those certain low level operations.
[60:12] Like registering identity is one thing, registering a name is another thing. And then topping up your balance is just saying, "Hey, let's convert some Layer 1 Dash into
[60:24] credits at that given rate, so that when I do these transactions, I'm pulling from my credit balance."
[60:32] Okay, so yeah, so this is the thing that when I was running this, I just make sure this part is, could I explain, you're giving it a thousand also, number, oh, so duffs is,
[60:47] are duffs the smaller denomination? Yeah.
[60:50] Okay, so that's, those are duffs, I remember duff came up a lot the last, when I was doing this, the first time this came up over the summer, I was like, I need to figure out what
[61:00] a duff and a credit and all of this stuff is. Okay, so it is here in the documentation, maybe it's a little bit lower than you wanted
[61:07] it personally, that's subjective. But this doesn't explain what a credit is, it just says a duff is equal to a thousand
[61:13] credits, that's still, then that begs the question of what is a credit? Because you know how to convert duffs to credits, that still doesn't really answer the question.
[61:21] One duff is the same as one Satoshi. So that, this is a, this is an issue of not controversy, but just a difference of opinion
[61:31] among in the Dash community, what we should call our base unit. I'm in the camp that I think it should still be called one Satoshi for, just for the reason
[61:42] that everybody already understands Satoshis. I agree.
[61:47] Giving it a new name. Duff is short for Dufffield, which is the last name of Evan Dufffield, the creator of
[61:54] Dash. Yep.
[61:56] That's cool. It's a nice, it's a nice little tribute, I suppose.
[62:02] Yeah. I mean, so it's, it's the same in terms of like Satoshi, you know, was the creator of
[62:07] Satoshi. You have your real nerd to figure that one out though.
[62:10] Yeah. And Ethereum has their own base unit as well.
[62:14] So we were following that tradition and some people still are. I just personally think that Satoshi is a better term.
[62:24] It's less confusing. And I also believe that the Dash project is closer to what Satoshi would have wanted anyway.
[62:36] So I'm claiming the Satoshi, like I, I'm claiming Satoshi. Exactly.
[62:41] Yeah. Okay.
[62:43] Yeah. So I guess for me, the, the, what has been confusing is that there's like, there's,
[62:50] there's two concepts going on here. There's one, there's the, there's the denomination, which is like this converts into this.
[62:55] And then there's the credits are a thing that you need to interact with the platform itself. And those are, I think like you want to make that as explicit as possible.
[63:04] So people know like one, like just cause it's just a, a unit conversion is very simple. Everyone understands that.
[63:09] There's no real need to define that as a concept, just cents to dollars. Whereas we need to pay a specific extra thing to do to interact with the chain.
[63:18] And then it's somehow different from just a regular old Dash as a cryptocurrency. That's where the questions start to come in.
[63:24] Yeah. So, so yeah, we're going to have this, this draft PR and before we submit it as a poll
[63:32] request to, to, to DCG, I want us to, to let it like, let it simmer in your head. I was going to say, I would not open a PR like this, this is notes to myself.
[63:42] Yep. Yeah.
[63:44] But, but that answered our question right there in the documentation. It does say one Duff equals 1000 credits.
[63:49] So once Satoshi equals 1000 credits and therefore, so you could take the, you could take the double check off there.
[63:58] That's correct. That can double check that now that is correct.
[64:03] This is a Duff though, not credits. No, no, no, no, no.
[64:13] You could do another equals and say one, one Dash equals 100 million Satoshis equals 100 million Duffs equals 100 billion credits.
[64:24] You could, you could do that. I would do that.
[64:26] I would do that. Yes.
[64:28] That's even better. So yeah, you can take the one Duff equals 1000 credits off as well.
[64:33] Now. So now you understand it.
[64:39] I've confirmed the 1000 conversion ratio. So we're good to go as far as conceptually and let's move on to the next step in the
[64:54] tutorial. Okay.
[64:56] So the next step in the tutorial, let me get my tutorial back up here. Was we were at, after creating the wallet and then we added funds to the wallet and
[65:11] then we registered the name, I think it was going to be the next one. Yup.
[65:16] So let me open that up, registry name, that's going to be this right here. And you know what I'm thinking?
[65:29] I think that even though the new documentation isn't published yet, I think that we should actually start converting your your tutorial to follow that one more closely with the way
[65:44] that I know that they're moving toward, which is a link to that. Yeah.
[65:49] So let me try to find it, but you could try to find it as well. And if you know where the documentation is on GitHub, which you just, you just went there.
[66:00] Try to go to the branch of that. Is it a, okay, here we go.
[66:13] Yeah. And then let's go to the docs.
[66:18] It may not be in the 1.0 dev branch yet, but it's, it's in some branch. So let's find it.
[66:25] What are we looking for? Exactly.
[66:27] What we're looking for is what, let's see, two weeks ago. I don't think that would be it.
[66:34] Let's look at the branch names again. Let's look at the branch names in the dropdown and see if there's, yeah, VL branches.
[66:50] That's the best way to find this. Can you do a search?
[67:25] Let's see, this is, this is a, what repo is this again? Scroll up.
[67:32] Fpay, docs.platform. Docs.platform.
[67:34] And is that where, where this documentation lives? You're, you're sure of that part?
[67:39] I mean, it's where you go and you click the edit button on the docs. So that's what I'm assuming, but I don't know if it's actually being deployed from here
[67:45] or not, you know, could be, cause there's no real way to see that. This change that I'm talking about happened in the past week.
[67:55] So Oh, I don't know. Let's go back to where you were before.
[68:05] I mean, if we look at the commits, the most recent commit was just this thing. Yeah.
[68:12] So not the most recent, but where did you, who was talking about it? Like, where'd you hear about this?
[68:17] Like, have you seen it? Like what is the context of why, you know, about, I guess, the Fez, I know the, I'm pretty
[68:25] sure that the Fez is the one that. So ask them to say, Hey, let me just give me a second to read through these increased
[68:34] number of credits, SDK doc SDK doc updates. That might be it.
[68:54] So are there specific changes you're, you are worried about or that you think are different because it doesn't sound, it doesn't sound like there's any big co-changes in any of
[69:03] these. The only thing that the major thing that was, that was changed is the, the client instantiation
[69:14] was got its own separate page in the docs and then subsequently it imports it. Because remember when we were talking last time, there was that issue of the block at
[69:31] which to start syncing. So let's do this.
[69:41] Let's just go up to the most recent one, just go look at it. So if this is the most recent change, then let's go tutorial and just walk through it.
[69:52] So it's going to start with so connect to a network, so we want, yeah, so this is still the same as this, as it's always been like, nothing's different here.
[70:19] Yeah. I was saying that I don't think they've deployed it yet.
[70:22] The latest version I was, but it's not even on the, this is, this is the GitHub, so it's not a question of deployment.
[70:28] It's not in the repo at all, whatever you're referring to. It's not in this branch then.
[70:32] So there's only, there's so many branches, so we need to go look at the other ones. There's like five branches.
[70:36] So let's just see, I guess. Maybe it's on develop.
[71:03] It won't be in that one, that's 24. Yeah.
[71:15] I think you should just ask whoever you think was the one to make the changes. I don't think we're going to find it this way.
[71:25] Yeah. out of these have been updated in the last week, so it's none of these branches.
[71:41] We know that for sure. Yeah.
[71:43] Maybe it was just on his own machine. I don't know.
[71:49] Anyway, you do something for a while. I'll find it.
[71:53] Either. Yeah.
[71:55] So if we want to change things, like we need to know what we're changing. So if we need to document where the docs are, it doesn't make sense for us to just go continue
[72:00] to search around random repos to try and find, you just ask the person directly. No, that doesn't make sense either.
[72:07] He's not going to be online, even if he is. I'm going to search.
[72:10] Okay. Well then we should stop the stream now and we can't go on until we need this answered.
[72:14] I don't know. You just...
[72:16] I'm just saying, I just don't think it's a good use of time, is all I'm saying. Other things we can do.
[72:23] The tutorial is not even finished. There's other pieces.
[72:25] You go ahead. You go ahead with the tutorial.
[72:27] Just as... I want you to keep going on the tutorial.
[72:31] Make sure that the other steps are still working. I'll search for the issue.
[72:35] I'll find it. If I can just concentrate for a minute here.
[72:43] Okay, good work. I got to push my changes actually, is what I've done so far, so I'll do that.
[73:16] I don't know what I'm doing here. Okay, I just sent you a link to your message in Discord.
[74:00] So pop that open. That's the issue.
[74:02]hamilton.com/tutorials Okay so this is the Dash Play Platform Tutorials. So this is code for the tutorials found on.
[74:19] So they've updated the code, but does that mean the docs also have the updates as well? Oh yeah, so it says right here, "PR will also be required in the docs to apply the
[74:48] docs to this change." So the thing that would be in the docs, it sounds like, has not happened yet, but the
[74:54] change in the code. So this is Dash Pay/Platform Tutorials, and then there's this separate Dash Pay/Docs Platform.
[75:06] That's what's confusing us right there. Yeah, no, it makes sense to me because you've got the docs itself and you've got just a
[75:12] repo that is the code. It's the same thing with me.
[75:14] That's why I have a separate tutorial markdown file and then the actual Dash Examples repo. So I've consolidated them by just making the docs a single markdown within this project,
[75:26] and that wouldn't make any sense for you to do that. But that does make sense to me in terms of you want the example that you're building
[75:33] in the tutorial to be a separate repo from the thing that is the docs themselves. Okay, well, either way, let's take these changes and let's put those changes into your tutorial.
[75:47] But my tutorial is already doing it already. It's already doing that?
[75:53] Yeah, that's what I thought. Okay, so I just wanted to double check that it's all the same.
[76:03] I guess it is, yeah. So with that brief tangent out of the way, what step are we on now?
[76:14] What step were we on? We were trying to...
[76:23] Sorry, I was kind of on a different step from where we were actually, but I'm on two threads right now at the same time.
[76:27] So let's go back to where we actually were, which was just we created the wallet and then we loaded some funds into it.
[76:33] We were about to create an identity, which is going to be the next thing. I can probably go for maybe another 15, 20 minutes and then I'll have to call it.
[77:06] Yeah. Okay, so it looks like we ran into an error here.
[77:13] This one takes a while. It did work.
[77:15] Yeah. This one takes the longest of any of the commands, getting the identity ID back.
[77:22] Yeah, so then you save that and your .env and then you retrieve the identity. So that'll be this one.
[77:35] And all these were working as far as I'm, as far as I've read through all this before you were on.
[77:39] So all this stuff still works. So this gives you the identity object back.
[77:45] Okay. And then you can retrieve the IDs, which I probably have a million of them now.
[78:07] Interesting. Actually, no, because we created a fresh wallet.
[78:10] So yes, that makes sense why there will only be one. And then you got the top-up.
[78:14] Let's see, I think this one actually might have it in my here that it was broken. So this one still is, something's going funky.
[78:33] So state transition broadcast error, asset lock transaction output zero only has a thousand credits left.
[78:40] It needs a thousand initial credits on the asset lock, but needs 50,000 credits to start processing.
[78:44] Well, let me tell you that again, it's not just saying you don't have that money. Well, so I did the test net, I got my test net thing.
[79:02] And then I started with whatever that gave me. And then now it's saying I need 50,000 credits.
[79:12] Yeah. How do I get more, so do I need to use it, test a faucet again, or do I need to do something
[79:18] to, like, I'm not really sure what's happening right now. You tell me, is it clear enough?
[79:25] What's wrong? Well, the problem is it's not clear when you first do, so let's go back to where you first
[79:33] do the faucet. Cause it's not clear exactly how much you get at that point.
[79:39] So, yeah, I think the faucet gives you a random amount, but I think it gives you like at least one dash.
[79:47] As far as I, how many did, how many, like check your, check your block explorer, see how much dash you have.
[80:02] So it started me with 0.2 dash. Oh, okay.
[80:06] Is that, is that how many credits is that? That turns like still hundreds of millions of credits, doesn't it?
[80:12] Yeah. It should be.
[80:14] Yep. Cause, cause one dash is 100 million Satoshis and that's 100 billion credits, so we should
[80:20] have plenty. Um, so I think what's, so it sounds like what's happening is that it's saying here, um, I
[80:27] have a thousand credits left out of a thousand initial credits on the asset lock. So that's the step where the, we already talked about, there's the, the asset lock transition
[80:40] thing. So that is just something that's, that's happening.
[80:44] You, we, we're not controlling that through how this, how we're interacting with it. That happened under the hood, so it's a little confusing how, I mean, I certainly, I'm confused
[80:57] about how to fix it, I guess, but is this an issue that we just need to, there needs to be something fixed in terms of generating the right amount of credits?
[81:03] Yeah. This is, this is an issue.
[81:05] Um, I think the one thing that we could maybe do at this point, um, and then we could end after this is let's check to see, uh, what we need is we need a dash test net platform
[81:21] Explorer to see how many credits our account has. And yeah, let's, let's start with Google.
[81:30] Um, I'm curious to see if Shen mix, um, test net Explorer will show up here. Are there any of these?
[81:39] Um, no. Um, can you send me the link that if you haven't already know it, I'll send you the link.
[81:49] Um, but this is another one of those things that, you know, arguably should be in the documentation.
[81:58] So maybe worth another PR on this, uh, I mean, the way I would structure it, I would send people if there's a different block Explorer, I would send people straight to that.
[82:07] If they, if it's also going to give you your basic dash amount to, instead of trying to tell people there's two different tests, there's two different Explorers, one's for dash platform,
[82:17] one's for the other, you just want a single Explorer that give you all of these if it's possible.
[82:23] I don't, I don't think that we have, we don't have that. Um, yeah, we have, so the things you would see on the dash platform Explorer would be
[82:31] different things than you would see from the regular Explorer. Well think about, um, what we talked about last time.
[82:39] There are two blockchains in this, uh, in dash right now there there's the proof of work blockchain and the proof of stake blockchain.
[82:49] What we looked at right there was the proof of work test net Explorer. That's not going to have anything about how much I'm talking about the other way around
[82:59] the, once we're on dash platform, if you also can get this information, it's, I mean, and you can create the front end of the way where you could get information.
[83:09] I would need to see the dash platform Explorer first to, to know what's there and what's not.
[83:14] Yeah. So let, let's look at it, um, together on the screen real quick.
[83:19] I have ended up here before actually. So I think the stuff doesn't necessarily show up.
[83:27] So if I just put in my wallet address that transactions are April 6th. So that should be fine.
[83:36] We did that last one that I see is an identity create that could have been ours. Well, this is actually, um, I suppose 304 that was, that was probably us.
[83:52] Yeah. Cause it's three 11 my time right now.
[83:55] Oh yeah. That's that.
[83:57] Okay. So let me grab this.
[83:59] Actually, this was really important. So the first time we, so this is, Oh no, this is, yeah, this is very helpful actually.
[84:08] So this is after you do the create the identity. So that's going to be up here, create identity.
[84:27] And then if you go to the identity, so this is my question then, what can you see about it?
[84:33] Does it have any connection to the, the address, the wallet address is associated with this identity.
[84:37] Well, right now what I see is I see balance zero credits. So that can't be good.
[84:42] Well, that's also, and that's different from what our CLI said, which said, I still have, Oh no, I'll put, yeah, it says I have a thousand credits left out a thousand initial credits.
[84:52] So there's some mismatch there. Yeah.
[84:56] So let's, let's try to do another transaction. See if it shows up in real time on the platform explorer.
[85:02] Let's try to do an identity top up or funds, but that's what we just tried to run. Oh, we just tried to do.
[85:10] Yeah. That's what was broken.
[85:12] Yeah. Top up identity.
[85:14] Okay. Yeah.
[85:16] This is, this might be something that I have to, we're pretty much learning, learning this stuff together right now at this point, let's, let's see briefly what it says about top up
[85:29] identity. Because we expected that would be adding credits to your account.
[85:37] So we should try and see if there's references anywhere to the thousand initial credits, but I'm actually, does this transaction, I get that.
[85:50] Okay. So that's this, I guess, or no.
[85:56] So let me go check that top up. So as users interact with the application, the credit balance associated will decrease
[86:17] and eventually it'll be necessary to top up the balance by converting some dash to credits. Let's see if we have any additional details or areas we saw all that.
[86:25] So the top of amount we're doing is maybe I need to just do more than a thousand. Maybe it's just the, let's try that.
[86:33] So let's, let's do a million, like let's get crazy. I mean, but like, yeah, we definitely need more than a thousand.
[86:42] So that's another tutorial. Where did you get that thousand from?
[86:47] That's a tutorial. Right here.
[86:49] This is the, this is where it is from right here. Yeah.
[86:52] That's a tutorial fail. That, that default needs to be higher because you can't, if you can't do all the things
[87:00] with 1000 credits, then not good. There you go.
[87:05] Cool. We fixed it.
[87:08] Okay. So let me make a note of that as well in my repo that I was adding notes to.
[87:23] Works just well. Let's do a PR for that and let's call it good after, after that PR, cause we, we should
[87:28] definitely bump that up in, in the the official documentation to like something like a million credits.
[87:36] Just give them plenty of room to work with. No, let me do this.
[87:48] Even a billion credits, like just give them enough. I don't like, honestly, I don't like the credits thing.
[87:58] I'm going to have to talk to DCG about this, like why is this necessary? I know that there are on the, on the sub low level operational level, there are things
[88:11] that cost less than one Satoshi I'm sure, but I don't think it should be a user facing credit, a user facing unit that now we have three units to keep track of as, as developers.
[88:26] We have Dash, we have Satoshis, we have credits. And I just don't think that the, it's worth, you know, I don't know, I'm sure there's,
[88:38] there's probably a reason for it. I just don't know if the pros outweigh the cons.
[88:42] Yeah. So I'm just doing something, something right now so I can make this simpler for myself.
[88:53] Sorry, I just picked the PR directly. Okay.
[89:03] I'm going to open this PR by myself because my whole, my whole site is, I'm not a new computer assist.
[89:07] Yep. I get it.
[89:09] I get it. All right, cool.
[89:11] Well, I, we made some progress. We, we found out, we found some mistakes, some things that could be improved with the,
[89:17] with the tutorial. And the nice thing is we didn't really run into any actual bugs like on the testnet network.
[89:29] Everything's working well. Yeah.
[89:31] Other than that, we didn't have enough credits for that one transaction and we figured out why.
[89:39] So success. Sweet.
[89:41] Cool. So I'm going to do that PR and then did you want to hop on another time to keep going
[89:50] through the tutorial where we were? Yeah.
[89:53] Yeah. Let's, let's, let's do another stream next week.
[89:56] Sweet. Sounds good.
[89:58] All right. Thanks everyone for watching and yeah, we'll catch you next time.
[90:04] Yep. Bye.
[90:05] [BLANK_AUDIO] 
