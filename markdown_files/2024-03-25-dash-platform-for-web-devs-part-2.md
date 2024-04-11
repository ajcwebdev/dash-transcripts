---
showLink: "https://www.youtube.com/watch?v=gbhl_EjK9m0"
slug: "dash-platform-for-web-devs-part-2"
title: "Dash Platform for Web Devs - Part II"
publishDate: "2024-03-25"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/gbhl_EjK9m0/maxresdefault.webp"
---

In this episode, Anthony introduces a tutorial for web developers to get started with Dash Platform and discusses automating podcast show notes using AI.

Anthony walks through a tutorial he created to help web developers get started with building applications on Dash Platform using the Dash JavaScript SDK. The discussion also covers the process of automating the generation of podcast show notes using OpenAI's Whisper speech recognition model and ChatGPT for summarization. They explore the benefits and potential monetization of this workflow.

Chapters:
00:00 - 04:57 - Intro and discussion of using Spritz for paying with Dash
Rion discusses his experience using the Spritz card to pay for services like StreamYard with Dash.

04:58 - 17:29 - Automating podcast show notes with AI  
Anthony explains his process for automatically generating podcast show notes using OpenAI's Whisper and ChatGPT.

17:30 - 21:41 - Comparing options for automating show notes as a service
Rion and Anthony discuss the possibilities and tradeoffs of offering automated podcast show notes as a paid service.

21:42 - 29:53 - Introducing a Dash Platform tutorial for web developers
Anthony introduces a tutorial he created to help web developers get started with Dash Platform using the JavaScript SDK.

29:54 - 37:01 - Walking through the tutorial steps  
Anthony walks through the initial steps of the tutorial, including setting up the environment and creating a wallet.

37:02 - 42:05 - Wrapping up and discussing future episodes
They wrap up the episode, recapping what was covered and discussing plans for future episodes on IPFS and Dash Platform.

[00:00] All right, we're live. Hello. Hello, everyone. Welcome to the incubator weekly show. Again, we
[00:12] are jumping straight in this week, like we did last week. And yeah, first thing I wanted to mention is last week, we
[00:22] started the show a little bit in disarray because our payments had lapsed on StreamYard. And so we were only able to like
[00:31] stream to one, one provider, one platform. And I, I've been wanting to test out the the spritz card option.
[00:45] What is spritz? What is spritz? Good question. So spritz is a service. And
[00:51] actually, if you could just, I will, I'll do a little screen share here. And hopefully, I won't dox too much myself. But I
[01:00] do want to show it just a little bit. Let's see window. Let's see which window. Too many windows. Too many windows. This is the
[01:14] one I think. Okay. That's Yeah, on the wrong side. But but good enough. Okay, coming up next. Coming up next. Yeah. So so this
[01:28] is spritz. spritz allows you to go. Let's see. Yeah, there. There command click isn't isn't the greatest. This is this is
[01:38] fine, though. So I pay my rent with spritz. I have a checking account that I can, I can send money to through spritz. It's
[01:48] basically like a bank. And then I have the spritz card as well now. It's basically like a crypt a bank for crypto people. So
[01:58] you can pay like it says here, you can off ramp to any bank account, you can set up a spritz card, which I did here. You can
[02:05] pay your bills with spritz. I haven't actually set up actual bills yet. I just I'm still using my legacy bank for that.
[02:12] So I instead of sending dash, and the main thing is that you can you can do it with dash, you can do it with Bitcoin, you can
[02:19] do it with a lot of different EVM stuff. So I took the opportunity to set up a spritz card. I guess I did it for me
[02:29] personally. We also have an incubator one that the AJ controls as well. But yeah, if you want to load the card, you
[02:37] just you just go in here, and then send crypto from a wallet or exchange. And then you select the best coin, which happens to
[02:49] be at the bottom of the list, unfortunately, but that's, that's the least it's on the list. On the list. You can see
[02:56] I've got $475 already $25 I already paid for the I paid for the StreamYard account. So StreamYard accepts spritz
[03:08] accepts dash through spritz essentially. So just to give people an idea real quick about some of the fees if you wanted
[03:16] to send $100 the this is actually incorrect. I don't know why it just showed that I think it there's a little bit of a UI
[03:24] bug there. Let me back up one and then add another zero. That's better. So $2 $2 fee. That's the man's a lot more
[03:32] reasonable than $20. You're like, Whoa, that's crazy. But yeah, no, that's, that's, that's not bad at all.
[03:38] You of all people should know exactly what happened. There's a little bit of a state management issue with their front end.
[03:44] $1,000 and that's what made the $20 and then I backed it up and it hadn't updated the fee yet. Anyway, so bug report spritz, I
[03:54] guess. So that's nice. And then you just go pay with dash and then it gives you a QR. So if anybody wants to pay and load my
[04:05] right now my crypto card with $100 feel free to scan that QR code in the next 30 minutes. But anyway, I'm gonna cancel out of
[04:17] that. If you do open your wallet, by the way, and you have the dash wallet, it'll pre populate all these fields. So
[04:22] that's nice. Anyway, that's how I've been using that for. I've been using that for a while now just I haven't had the card.
[04:35] I've been using it for several, several months now. Pretty much all my expenses go through there. But yeah, I've used the
[04:44] card only once now. What else did I want to show here? I don't think anything. Going back to just us for a minute just a just
[04:57] a chat. Yep. Um, the other thing that I wanted to mention briefly at the beginning of the show here is you, Anthony have done a
[05:09] little bit of magic with our show notes. Do you want to talk about that?
[05:15] Yeah, this is something that I've been working on kind of piecemeal for like almost a year now actually is a long time in
[05:23] the works where basically, so let me back up a bit. One of the things we talked about, I think last time was when I was on like
[05:32] a week or two ago is that you know, I had this podcast called FS jam. And I just I make a lot of content in general, you know,
[05:39] a lot of video content, a lot of spoken content among other podcasts, I have my own podcast. So it was like, the amount of
[05:45] words I have like spoken into a microphone over the last three years is vast, I could fill many books. But like transcription,
[05:53] especially technical transcription is hard and time consuming and expensive. At least it always has been in the
[05:59] past. But there's this thing called whisper, which is a open source transcription model from open AI is actually the only
[06:09] like open source thing open AI has anymore, because they've had closed source all their stuff. This is one thing that they they
[06:15] they let the let the clubs get so we are able to basically use this model. And I had this I basically, so I wanted to like
[06:26] automate as much of this as possible. So basically, I started with, like, you would run transcript, you would run
[06:32] whisper, and you like get a transcript. And then what I would do is I would kind of like copy paste that into like chat GBT
[06:39] and be like, hey, create a summary of this. And then it would like create a little summary. And I'll like read the
[06:45] summary. And I'll be like, yeah, that's like pretty good. Like, you know, maybe I'll tweak it a little bit, you know, sometimes
[06:50] you'll get like the names of people wrong road, say like, the guests instead of like the actual guests name. So you know,
[06:57] be a little bit manual editing there, but not a lot. And then I'll be like, Alright, cool. Can I generate, you know, chapters
[07:03] with it. And that's, that's one of the really big lifts is how we like go through a whole video and be like, what are the
[07:09] sections? How do I title the sections? When do the sections start? When do the sections end? And if you feed it a transcript
[07:16] with timestamps, it can kind of figure that out. Sometimes doesn't quite get the exact times, right? Like when a
[07:23] section starts or not. So usually you have to listen to it back, you may have to adjust the times a bit. But the
[07:29] descriptions and the titles are pretty accurate. So basically, what I did is, let me share a link in the chat. I have a blog
[07:39] post now about this one. Actually, I'll share my screen real quick. So I can show people this. So hopefully, I'm all
[07:49] configured. Great. So this is and even the even the cover image here is generated with chat GPT. This is kind of a blog
[07:59] post where I walk through the whole the whole process. And I use this tool called the YouTube downloader. Can you zoom in?
[08:10] Yeah, yeah. Yeah. So there's this tool called YouTube downloader. That allows you to basically take a YouTube link,
[08:20] and then straight up, download whatever you want into an audio file. So you basically use this actually, I can I can run
[08:30] through I had a dash video that I could actually run through this and it won't take very long. So let me grab this. And
[08:42] then let me grab this. So this is going to do is it's going to basically take this video and output a WAV file. And then this
[09:05] is the whisper command. And what this does is it runs the actual whisper AI transcription model. If you see here, you can see the
[09:19] stuff coming out. So it's talking about central bank digital currencies, all the shitty lack of accountability,
[09:25] infinite money printing. So you can see this, this looks like some dash content right here, doesn't it? Yeah, it doesn't
[09:35] hold back, does it? Yeah. All right, cool. And then go ahead. Yeah. Yeah. And then the this part is not as interesting. I
[09:44] have like this massive kind of node script or Python script that just kind of transforms the the output to make it a little
[09:53] more amenable to being being modified. This is the the interesting part right here is the prompt. So while that's
[10:03] running, I'll kind of explain the prompt. So the prompt is where all the magic comes in. So you've used chat GPT, I'm
[10:08] assuming at this point, right? I'll be honest, I have not used chat GPT. You know what stops
[10:13] me? I don't I don't like signing up for their service. I want the open source version. I want the version that I can actually pay
[10:22] with dash and have a monthly monthly subscription to GPT and AI general tooling.
[10:30] Okay, well, I don't want Microsoft version. Yeah, there's ways to do that. I'll get you set up with an open source LLM
[10:35] because like, you really gotta start using this stuff. So with a prompt, this is basically what you feed the LLM to tell it what
[10:44] to do. So I have a multi step prompt here that basically says is the technical transcript of with timestamps of a technical
[10:52] conversation. And I asked it to do a couple things, not all of which I really use this is kind of like just an example of what
[11:00] people who are generating their own content may want to do. So I have a generate five potential titles, have it write a one
[11:06] sentence summary, one paragraph summary, two paragraph summaries, you get summaries of different lengths, have it create the
[11:12] chapters, and I tell it, you know, make sure the chapters aren't too short or too long. And then I say create some key
[11:20] takeaways, and then like potential future topic ideas. So you know, when I was doing this for dash, I didn't do like the
[11:28] key takeaways or the extra topics, and we already had a title for it. So basically, I just took like this section
[11:34] right here is really the meat of it. Then you kind of show it, hey, this is what I want to look like. So it kind of knows, and
[11:41] they can be like, give it to you in markdown format, which is really nice. So oh, nice. Yeah, I think most of these should be
[11:51] good. Let me do it. I'll get to do it with a actually let me do it with a full prompt. So
[11:57] and while you're doing that, I probably should have explained a little bit more of today's show. We do we have we going through
[12:10] this whole process, Anthony basically made some timestamped summaries of last week's show. And we're going to do that going
[12:20] forward with with all of our shows, because every now and then we'll get some people coming in and saying, Oh, this
[12:25] is like 50 minutes. I don't know if this is worth my time. Do you have timestamps or whatnot? So we will going forward. And we
[12:33] could even put these on the shows going back as well, right? Yeah. So that might be nice. And then for the rest of
[12:41] the show after that, we're going going to introduce a tutorial that you made as well, for just getting started with web
[12:49] development with dash platform. So that's the that's the show going forward. And probably we probably won't go get through
[13:00] the whole tutorial. But we'll start it and then we have scheduled for another stream already for tomorrow, where
[13:07] we'll do it at a more leisurely pace or whatever, whatever pace we want, because we try to keep these shows within 50 minutes or
[13:15] so. So yeah, go ahead and finish up what you were saying here. Yeah, yeah. So pretty much pretty much done here. So the
[13:22] last step is you just kind of take the the transformed transcript output, and then concatenate on a prompt here. So
[13:33] I have like a prompt file that includes the prompt. And then I was kind of like smash that together with this. So you can
[13:41] kind of change the prompt if you want. And then you can kind of just generate as many as you want in like a pipeline. And
[13:49] then you see here, this is this is the output. It's still it's still going. Once that finishes, I'll pop that into a gist. So
[13:57] you can kind of see that the markdown actually rendered. But if we just kind of look at what it's doing, it's saying, you
[14:02] know, exploring the history and implications of technocracy and central bank digital currencies on global freedom and control.
[14:10] So you know, it's not like the fanciest summary, but it's it's functional. And it's like, broadly correct, you would say,
[14:17] right? Yeah, yeah, of all of the things in the world that this could be about it narrows it down pretty well. Yeah, exactly.
[14:25] So let me pop this in a gist real quick. So we see here, this is this is the whole show notes. So you got your potential title
[14:38] technocracy and CBDC steering the future of finance and freedom. You got your one sentence summary, one paragraph
[14:46] summary, two paragraph summary. And for this one, you know, it's a short video. It's only like five minutes. So it just has
[14:52] three chapters, which is pretty good. And then key takeaways, technocracy seeks to govern society through technology and
[14:59] scientific expertise potentially need to increase central control. CBDCs represent a modern application of
[15:05] technocratic ideas offering both efficiencies and risks for surveillance and control. Understanding and engaging with
[15:11] alternative systems and technologies is crucial for preserving individual freedoms and decentralization. So yeah,
[15:17] so again, that would be, you know, you can take as much of this or as little of this as you want. So what I've been doing
[15:24] for the last was I basically grabbed this stuff, edit it together, and then grabs the chapter. So I used a bit of a
[15:32] reduced prompt. But this is an idea of, you know, you could, you could ask it for whatever you want it to do, you know, you
[15:38] could say, I want these show notes, but like said, like a pirate, you could do that if you want.
[15:44] Yeah, cool. So let's, let's show briefly. I'll show my screen again, now that now that we've explained how we did it. So this,
[15:52] this is last week's show. And I'll just kind of scroll through there so that you people can see. I read this. And I think
[16:01] it's like you said, it's a pretty accurate description of what we talked about last week. So yeah, we'll, we'll go through
[16:08] this. And it even these blue links look like they're actual links that you could actually just throw this into the
[16:13] description. And bam, YouTube has the chapters. Yeah, that's, that's a YouTube thing where the YouTube will
[16:19] sense that you have put timestamps in your description, and that turns those into the chapters itself. So this adds
[16:26] like an extra layer of kind of automation that is native to the YouTube platform itself. And podcasts will usually do that as
[16:34] well. If you were to feed this into like podcast show notes, you could use it as timestamps for your podcast as well. And
[16:40] I was like, it's going back to why I built this in the first place. I built this for FH Jam. Haven't even used it for FH Jam
[16:46] yet, funny enough. But um, because the show's kind of been on hiatus. But you know, I just I wanted this and I didn't have
[16:53] the time to do this for every single episode. So I'm just kind of like slowly built up this pipeline. Now that I have
[16:58] it. It's just like, it's so sweet. Yeah. And the punchline was I all those steps that I went through a second ago, like
[17:05] downloading the YouTube video, running whisper, concatenating the prompt on at the end of the blog post, it gives you a single
[17:11] command that does all that for you. And you basically feed it a YouTube URL, and then it runs through all those steps. And it
[17:18] gives you a single file that you copy paste into chat GPT to get the answer back. And I'm actually using cloth now instead
[17:24] of chat GPT, because it's slightly better that they have the most current model these days.
[17:29] And as all of these, these functions, are they accessible through just like a straight raw API? Or do you always have to
[17:39] use their their user interface? So, um, yeah, so chat GPT has an API. And so does Claude now
[17:46] clauses was only open for like, people who would like go through their whole system. He's like vetted, like onboarding and
[17:53] stuff, but they just opened it up recently. Doing that you need to like do a little more in terms of need to like hit it
[18:02] with a curl command, which may be a little weird, or you can like they have like, node and Python client libraries that you
[18:09] can use at the very end of my blog posts, I kind of give it a next steps, which is, I'm going to have a blog post after that
[18:16] we're going to show how to do this with API's. The downside with that is you're paying per token when you do that. So if
[18:28] you wanted to, so if you want to like do this on like 100 episodes, you could do that, but it's going to cost you some
[18:34] amount depending on, and this is where you need to be really smart about like, what do I actually need in my show notes.
[18:39] So, you know, if you just need a description in chapters, you would only do that because you're paying per word
[18:46] essentially, like it's, you know, it's, you know, fractions of a cent per word, but they add up over time, of course.
[18:51] Fractions of a cent. So so if we were to do this on all of our incubator content, how what's your ballpark figure of how much
[18:59] that would cost? I cannot give you a number right now. I would, I would need to
[19:03] like run it on an episode, go look at how many videos you have and like do the math on that. I really could not give you a
[19:10] number right now. That would be accurate. Yeah. And the other, the follow up question I had with that
[19:15] would be, is this something that that we could, I mean, obviously we could, if anybody out there is interested in having this,
[19:22] like doing this thing for the DCG sprint reviews, I'm sure that once we got this process ironed out, it would be as simple as
[19:32] just saying, okay, use this YouTube link instead. And do it for the DCG sprint reviews, because I know that that would
[19:41] be useful for me personally. And it'd be cool to make this into somewhat of a service where it's just pay us, you know, pay us
[19:51] $1 in Dash, and we'll pop this out for you as a web app. I don't know.
[19:57] Yeah, I mean, that's fine. That was the same thing my wife said when I showed her that she's like, why are you giving this
[20:02] away for free, basically. And there's other services that already do this, basically. So people have built many, many,
[20:10] many things like this that you'll be competing with. But this could be a fun thing to build. Actually, that would be
[20:17] like, if any of them do it in a way that I don't have to register, I
[20:22] just have to pay some money. Sure. Yeah. Even crypto, basically, because I wouldn't want to be entering credit
[20:30] cards. Yeah, I mean, for that, I mean, you use sprints, right?
[20:35] Yeah. But the idea is that we'd want to get people moving on to the money of the future, which is just, you know, scan a QR
[20:44] code, or connect a wallet app, and you're done. But I mean, I don't think many of them are probably crypto enabled yet. And
[20:52] um, you know, they'll, they'll, they're, they're paid. I'm not sure if you like that. There's not many apps these days where
[21:01] it's like you could pay without creating an account. Like that's kind of rare, unless you're like on a porn site or something.
[21:06] Yeah, well, that's the future that I want to see. I hate registering. One of the reasons I don't use chat GPT is, it's
[21:14] just one more login, one more company that's got my my information. I just want to pay for a service and be done. Even
[21:21] if it's a subscription. But anyway, we should probably use the crappy GPT without signing up. You know, it's just not as
[21:29] good. Yeah, yeah. Okay. So let's move on to the tutorial that you've put together. We can, we can do your screen or mine
[21:41] doesn't matter. I've got mine up already. But um, um, I mean, I wanted to actually like, run through these commands
[21:50] and see what happens, especially now that so let's switch to my screen. Especially since now we have testnet back up. Yes. Let
[21:59] me just make sure real quick. Just double check. There's nothing weird on my screen. Like yeah, there's our discord chats
[22:08] right there. So let me close that. Okay. There we go. Great. So while you're bringing that up,
[22:27] I'll explain some of my, my rationale for both having you do this, as well as us taking some time to go through it. One
[22:38] of my one thing I've been thinking about is who is who is going to be using dash platform for data storage? Are we going
[22:50] to be targeting existing web to developers and trying to get them to essentially use use our database use our platform for
[23:01] your applications, even if they aren't necessarily crypto people or libertarian type people? Or on the other hand, are we trying
[23:10] to target crypto people and libertarian people and trying to help them be to become developers because they have
[23:19] some something that requires the the value proposition that that crypto and dash platform have like, this is permissionless and
[23:30] censorship resistance and data storage. And if you have an application that you really need this for, then we can help you
[23:39] out but you need to know some basic web development skills. So the question is, is it easier to convert a non crypto non
[23:48] libertarian type person to using dash platform? Or is it easier to convert crypto and libertarian type people and
[24:00] entrepreneur type people to become to have to get the skills the basic skills that they need to make their website?
[24:07] You know, this reminds me of this reminds me of Armageddon. Is it harder to train an astronaut to be an oilman or an
[24:14] oilman to be an astronaut? I feel like Armageddon. Armageddon. Yeah, because that's the whole army has to be about an asteroid
[24:23] coming to hit Earth. And so they need to stop it. And the way they're gonna stop it is by drilling a hole into the
[24:29] asteroid and putting a nuke in it and exploding it into two halves. So it goes around Earth. It's like it's such an absurd
[24:35] concept. But the point is, they get a bunch of oilmen and train them to be astronauts. And a lot of people were like, wouldn't
[24:41] it be easier to get astronauts and have them trained to be oilman?
[24:44] That's exactly what I'm talking about. I do remember watching that show. I was like, two decades ago or something like
[24:52] like when it first came out and I went to at a drive in movie if anybody doesn't know that that you take your truck and you park
[24:59] it backwards and there's a huge screen you watch outside and it's awesome. And the reason I don't remember anything about
[25:05] that is there's a certain stereotype for when you go to drive ins what you do, you don't actually watch a movie. But
[25:14] anyway, go ahead. Okay, so I'm, I'm just gonna get a setup so I can make sure like
[25:18] the first kind of command runs and then I'll like explain what the heck I'm doing. So we're basically, I what I did is
[25:28] works. Yay. Okay. So let me go back and have explained what the heck I just did. So now it's successful. Yeah, yeah,
[25:40] exactly. Yeah. So what I like to do, I was actually I was going back and rewatching some of the videos I did last last summer.
[25:46] And this is something I kind of explained is that I always like to have a full like workflow in my tutorials, the point where I
[25:55] could go back and just like copy paste commands and it's gonna work and I don't have to worry about like, configuring my
[26:02] environment again, and just like all sorts of little stuff like that. So this is a tutorial that currently exists right now just
[26:10] in my GitHub. But this will probably be somewhere, you know, more official, and easy to find for people in the dash community
[26:19] at some point, we're still kind of figuring out where's will make the most sense to be. But basically, what it does is it
[26:24] takes you from like zero to one with a node enabled dash project. So this is using the dash JavaScript SDK. So do you
[26:34] want to talk a little bit about what that is? Yes, the JavaScript SDK for node and the browser is basically
[26:46] like the culmination of all things dash platform. If you want to use dash platform, this is the this is the one package
[26:55] that you need that wraps up a lot of other different libraries. This is what we were talking about last week. That is
[27:03] quite big. And we can hopefully slim that down in certain ways. Watch last week, last week's episode if you're more
[27:13] interested in that. But yeah, this this is the package for web developers.
[27:17] Cool. Yeah, so what's so this is basically what I learned to use. And this is like the sum total of my dash knowledge now is all
[27:25] contained within just this this package. So I created basically a ton of node scripts, if you see here that take the
[27:36] functionality of each kind of chunk of code that are in the dash docs and kind of stick them all in one project and walk you
[27:44] through a flow of how how you use them. So you need to set up a dash client. And that is what is going to let you basically
[27:56] connect to testnet. So I have a dot EMV here. And as you go through the tutorial, you basically continue to add on to
[28:04] your dot EMV file, you'll create a wallet, you'll create an identity. And the first couple ones are just like actually
[28:12] querying from the chain. So this is get best block hash. And I think that means that's like the most recent block hash, I think
[28:21] is what that means. Yeah. Yeah, great. And then you can do there's getting a specific block hash, I'm gonna skip past those
[28:30] and just go straight to the create a wallet and identity because this is the this is where the important stuff really
[28:36] starts happening. So you are able to run the create wallet function. And if it doesn't have a mnemonic in it already, if
[28:47] mnemonic is set to null, it will generate you a new wallet. So this guy, so this is the command right here. And so it's like an
[29:00] async node command, we're running get wallet account, and then exporting the wallets to this mnemonic variable. And then
[29:09] you return that and then just kind of print it. So let's do that. And so there we go, right here, we see we have a wallet.
[29:20] And I really make it as simple as possible you it's even it prints it out in the format for your dot EMV. So you just paste
[29:29] it straight from the terminal straight into your dot EMV. And then there you go, you're kind of set up. Beautiful. Um, any
[29:36] any comments so far? Yeah, this is what I love about your work is you make it as simple as it needs to be for somebody like me
[29:45] that I don't want to mess with. Don't make me think you know, it's that it's like that. Don't make me think. Don't make me
[29:52] think as a web developer either. But I know that obviously, you do a lot of thinking as a web developer. But that's the thing
[30:01] you have to do so much thinking that people can just give you some steps that require less thinking. Like it makes such a
[30:09] difference. Yeah, exactly. And it comes back to what I was saying earlier, if
[30:14] you are the type of person who you have a great idea, you you know, the crypto market, well, you know, the general market,
[30:24] well, you have something that that you want to build, but maybe you're not a great web developer. Theoretically, you
[30:31] could follow your tutorial. And with a little supplemental Google searching and whatnot, you could throw together a basic
[30:39] web application and test proof of concept. And that's what I that's what I want to go for is I want, I think that I do want
[30:49] to target it from both angles where we're, we're making the oilman, an astronaut and the astronaut and oilman. So, yeah,
[31:01] and that's what that I do want to when we stream tomorrow, I do want to take a little bit more time with this stuff so that if
[31:09] somebody if this is too fast for somebody, they don't really know what's going on, then we can we can explain a little bit more
[31:15] when we have a little bit more time. Yeah, let's let's um, actually, we do have to stop right here
[31:21] because I'm having some issues with testnet or not testnet. I mean, the faucet. So, um, I just dumped my the wallet into chat.
[31:33] It says to Rion, can you try just getting some funds into this from your faucet or from the faucet?
[31:41] Yes. Let's see. Do you have a link to the faucet handy that you could throw into the chat? Yes.
[31:53] I put it in regular chat and private chat. And someone is in the chat here saying, very well done. It's a simplicity. Thank
[32:05] you. Appreciate that. And then incorporate some chat GPTMO saying we're starting Yeah, unless they're philosophically
[32:12] opposed to I suppose. So, um, faucets faucets are always challenging. This is you only have the one dash faucet, I
[32:24] think is the situ right now. We have multiple ones, but it's it's like faucet roulette. Which
[32:37] one which one's working at any given time? So let's see, I'm gonna build company quick note actually got into fauceting. And
[32:44] I'm out the average one, because that's not one of the chains they support. But there's a pretty dang reliable. So yeah,
[32:52] if they want to get one set up, and I'm going to put in the promo code master node to get you a bunch of coins 1000. Hey,
[32:58] let's see. Oh, that's the promo code. That's the hot tip. Yeah. Oh, I got the no more dash. Come back in one hour. It looks like
[33:08] we've drained the faucet. Okay, that means I actually got the got the coins, then you should try it. Yeah, you should you
[33:16] should look on on a block explorer and see. Yeah, let me go back to sharing because I have had I, I do recall several
[33:24] times where I didn't think I got the coins, but I got the Yeah, it looks like I do. Because this is this is the
[33:30] address I just created. And this is our block explore right here. We got three confirmations looks like I'm looking at three and a
[33:37] half dash. Yeah. Okay, great. That's a forge ahead. So these are the steps here. This this looks weird, because these are
[33:48] supposed to be a screenshot. So I need to just fix that. But um, now we're gonna copy paste this. And what this is, is now we have
[34:00] our mnemonic is set to mnemonic. So we have some dot EMV process variables going on. And yeah, so let's create an identity. And
[34:14] the identity. This is where Yeah, so we're getting to the point we can create like a dash name, I believe. Yep.
[34:26] Yeah, you need the identity before you can create the name on top.
[34:30] That makes sense. This command, I think, takes a second to run. So let me just, um, so people see like kind of where this all
[34:44] came from. So the dash dot org, the dash platform, and then guides and documentation. So we're running through right now
[35:00] is basically the tutorial on dash dot org. So here we have the connect to the network. And this is the kind of client
[35:12] thing. They're showing you how to do it with this testnet account over here, still running. And then this is the
[35:20] creating a wallet. So you see here, they say this indicates that we want a new wallet to be generated for a new address for
[35:28] existing wallets that replace null with a wallet you've already got. So I admit, so like some, so we see here, like
[35:36] there's some differences already in terms of how I how I set this up. I extracted out the client into its own file. And I'm
[35:44] keeping all the functions in separate files. And then I'm also using ESM instead of require to get that new school
[35:55] JavaScript. And this is actually one of the things that I remember the past I was going to, like open some PRS and
[36:02] stuff. This is I think this is actually on. Is this on a get repo now because I remember in the past you're using like read
[36:09] me docs instead, you know, if I can open a PR to change anything here.
[36:15] You can but I don't I don't remember exactly how I I'm fairly certain that it is.
[36:22] Looks like it's right here. Yeah. Great. Okay, cool. So, um, I will, that'll be for another time. But let's see what's going
[36:34] on here. Okay. So it looks like we got some error. Not sure if this is an error with testnet or an error with my code. But this
[36:54] may be Yeah, we'll have to have to call it. That's probably a good place to stop anyway. So let's let's do a
[37:01] quick recap of what of what you did get done there. And then what we have ahead of us in terms of the tutorial. I'm going
[37:12] to open up myself. So you did you did get an identity to work right? And you got initialize the dash client, you we skipped
[37:24] the querying blocks thing, that's fine. And create a wallet and identity. Yeah, export of the mnemonic added fun. Yeah,
[37:35] that's the creating the wallet is the most important step because everything else in in the in the tutorial depends on
[37:41] having that wallet. Right, but the while creating the wallet doesn't require any connection to actual testnet. So I was
[37:48] wondering if we got any of the steps that actually connected to testnet. So maybe, maybe that's better for tomorrow anyway. I'm
[37:57] fairly certain testnet is up and running right now. But we we will want to see if there's some something that we can run that
[38:06] shows that we were connecting to the actual network. But let's Yeah, and I'm thinking back to like a week or two ago, this was
[38:13] how far I got last time. So yeah, so something going to something still going on testnet, man. Okay, cool. Well,
[38:21] I think we'll wrap it up there. And just reminder, tomorrow, do we have a time set for our stream? Yeah, it was gonna be I
[38:31] think 1pm Pacific, 4pm Eastern, that would be to your time three my time, or we're sandwiched there in the in the middle, I
[38:40] think pretty sure that's what we got set for. Okay. So if anybody's interested in doing a deeper dive into this tomorrow,
[38:46] join us on the stream. Feel free to ask questions while we're going to do it at a more leisurely pace and just take our
[38:52] time. And people can ask questions if you're a developer especially join the stream. Next week, I believe we are going to
[39:00] have on somebody, we had a discussion in the dash discord a few days ago, where we were talking about kind of like the
[39:11] trust, the trust model, the trust assumptions when you create an application, like how how trustless really is it? If,
[39:20] you know, you're, say you're using dash platform, and it's doing all this stuff that is supposedly decentralized. But if
[39:31] you're serving that application through traditional means, like a traditional hosting provider, for example, and the developer
[39:43] can change that application at any point and update the service on his server, and potentially deliver malicious code, then how
[39:55] decentralized really is it? And then we talked about IPFS. So serving, serving your application through like, say
[40:05] you wanted a poker game, and you wanted to make sure that it was completely trustless, where you start the game, and then you
[40:12] know, you have certain assurances that you put the money to, to the pot. And then you know that the application
[40:20] just runs and there's nobody that can steal your funds. So we talked about having like an application that is, is audited
[40:30] just like a smart contract would be audited. You'd have some people auditing the application itself that talks to the dash
[40:40] platform as the back end and has certain functions. And then once that's kind of audited, and has eyeballs that are on it, then
[40:50] you could put a hash into IPFS. And because IPFS serves content that is at an address that is static based on the content,
[41:04] it's contract content addressable, rather than location, addressable, or I don't know if that's the actual
[41:12] term they use. It's been a while since I researched it. But anyway, we talked about IPFS. And so because I have a friend
[41:19] that works for or worked for Protocol Labs, which is the company that made IPFS, I'm going to have him on next week.
[41:30] And we'll talk about some of those assumptions and how to deploy to IPFS your application to IPFS.
[41:37] That's cool. Yeah, I know of Daniel at IPFS. He's one of their dev rels used to work at Prisma. I've had him on FS jam.
[41:44] And I have a little IPFS tutorial actually. Daniel. Okay, cool. And yeah, maybe we can have him on as
[41:50] well. We'll, we'll check that out. And we will. Yeah, we'll talk some IPFS and probably a third part of this series next
[42:00] week. So if you're interested in that, tune in next week, and we will catch you then.
[42:05] All right. See you guys next time. I see Anthony.