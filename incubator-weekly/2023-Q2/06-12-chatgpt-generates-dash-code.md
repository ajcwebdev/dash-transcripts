---
showLink: "https://www.youtube.com/watch?v=U5jEgYsiqho"
slug: "chatgpt-generates-dash-code"
title: "Watch ChatGPT Generate Some Dash Code"
publishDate: "2023-06-12"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/U5jEgYsiqho/maxresdefault.webp"
---

ChatGPT-4 demonstrates advanced code generation and debugging capabilities, saving developers significant time and effort.

## Episode Summary

tl;dr: In this technical conversation, developer Anthony Campolo showcases the capabilities of OpenAI's ChatGPT-4 in assisting with code generation and debugging. By providing ChatGPT-4 with a React component, Anthony was able to rapidly generate equivalent components in multiple frameworks like Vue, Svelte, and SolidJS. The discussion also covers the potential of integrating AI assistants into documentation, the challenges of open-source alternatives to proprietary AI models, and tips for developers to incorporate AI tools into their workflows for improved productivity.

## Chapters

00:00 - Introduction and Overview of ChatGPT-4's Capabilities
The conversation begins with an introduction to ChatGPT-4 and its advanced natural language processing capabilities, which have the potential to revolutionize various aspects of computing and software development.

05:26 - Anthony's Experience with ChatGPT-4 for Code Generation
Anthony shares his experience using ChatGPT-4 to generate equivalent code components in multiple frameworks based on a single React component, demonstrating the AI's ability to significantly reduce development time.

18:53 - Discussing the Potential and Limitations of AI Code Assistants
The participants explore the current capabilities and limitations of AI-powered code assistants, including their ability to generate functional code, debug errors, and provide explanations for their suggestions.

30:11 - Integrating AI Assistants into Documentation and the Open-Source Landscape
The conversation shifts to the potential of integrating AI assistants like ChatGPT-4 into documentation platforms to enhance user experience. The challenges of developing open-source alternatives to proprietary AI models are also discussed.

37:52 - Tips for Developers to Incorporate AI Tools into Their Workflows
Anthony provides practical advice for developers looking to incorporate AI tools like ChatGPT-4 into their daily workflows, emphasizing the importance of identifying repetitive tasks and gradually integrating AI assistance for improved productivity.

## Transcript

[00:00] "Bank." It's a phrase that, across our culture, seems to have reached almost axiomatic status. "Honey, you're no better than money in the bank. Yeah, yeah, yeah, yeah, yeah."
[00:11] "I got money in the bank." "Yeah." "Shawty, what you drank? I got money in the bank." "John Cena wins Money in the Bank!"
[00:19] It's tough to pinpoint when the phrase first emerged, though some sources point to the 1930s. And that makes sense, because it was at that time that central banksters were doubling down efforts
[00:28] to retain credibility in their institutions. It was the era of the Great Depression. "Don't look now, but there's something funny going on over there at the bank, George.
[00:36] I've never really seen one, but that's got all the earmarks of being a run." Almost half of all financial institutions in the United States collapsed, and along with them,
[00:44] the savings of millions of individuals. Despite their having put the money they earned in the bank, it wasn't there. Maybe the phrase "money in the bank" can be linked to FDR, a PR push of sorts.
[00:54] 36 hours after taking the presidential oath, he issued Proclamation 2039, which suspended all banking transactions. A few days later, in his first fireside chat, he stated,
[01:04] "I can assure you, my friends, that it is safer to keep your money in a reopened bank than it is to keep it under the mattress." Money in the bank. But is that true? I mean,
[01:15] after all, here we are, 90 years later, and the wildly popular card game "Cover Your Assets" includes cash under the mattress as a mechanism to protect your financial wealth, jokes,
[01:25] and the almost total depreciation of the Federal Reserve note since its creation. Aside, questions about bank solvency isn't just a historical footnote. Since 2000, there have been
[01:33] over 500 bank failures, including the collapse of First Republic Bank a few months ago, which, based on assets, was the second largest bank to fail in U.S. history, and the collapse of
[01:42] Washington Mutual in 2008, which was the largest bank to collapse in U.S. history. And there are hundreds of insolvent banks. At the end of the third quarter last year, there were 722 banks
[01:53] that were bankrupt, with losses exceeding 50% of their capital. And the situation has only gotten worse. That data, by the way, was in a report from the Federal Reserve, the same Fed that,
[02:04] for almost a decade, was headed by Ben Bernanke, who, in a 2002 speech, acknowledged that, and apologized for, the Fed causing the Great Depression. So maybe the meaning of the phrase
[02:14] "money in the bank" is a bit off. After all, in the United States, the banking system operates via fractional reserve. That means only a fraction of all deposits are actually kept on hand.
[02:22] But that's not exactly the case. Because in March of 2020, the Fed said that commercial banks were required to keep zero deposits. Since even the most brilliant mathematician cannot create a
[02:38] fraction of zero, perhaps it's time for a neologism, a new word, or expression. Isn't it more accurate to call the legacy banking system a zero reserve system? So what's to be done?
[02:48] Should we clamor for reform? Should we aim to end the Fed? Or should we, as individuals, each pivot and utilize alternatives to the failed Federal Reserve note scheme?
[02:58] Since 2009, when decentralized blockchain-based money emerged, I suppose you could say that the phrase "money in the bank" took on a new meaning,
[03:10] one tied to another phrase, "be your own bank." You see, if you own decentralized crypto, you have your private keys. If you rely on a third party to keep your crypto,
[03:33] like a centralized exchange, they have your private keys. You may be prevented from accessing what you believe is yours, whether due to an exit scam, hack, collusion with government regimes,
[03:42] or any other reason. So enter the phrase "not your keys, not your crypto." We could go on at length about wallets and storage options and the like, but that's beyond
[04:03] the scope of this video. Perhaps the key takeaway is this, we live in a time where we have the technological means to circumvent the legacy power structures, including money. We don't
[04:11] need to use a particular currency because of where we happen to be born. We have options. We can choose that which speaks to us, one that isn't constrained by banker hours and rife with
[04:20] fees and surveillance, but always fast, seamless, inexpensive, and offers privacy. As former Fed Chairman Paul Volcker admitted to,
[04:27] the banking system ultimately relies on you having confidence in it. "People have confidence in something that doesn't cost much to manufacture,
[04:36] namely a piece of paper with some printing on it. And so long as people have confidence in that piece of paper, that it's going to maintain its
[04:45] value. And it maintains its value because people are willing to accept it. It's all a kind of, not a con game, but it's a confidence game." Have they shown that they deserve your confidence?
[04:56] We are at the tipping point where things can actually tip in favor of the many of our favor from the small group of people who have been benefiting from a rigged system for nearly a
[05:06] century. One mind, one person, one technological breakthrough at a time. We're together building a new paradigm. Well, hello and howdy everyone. Welcome to Incubator Weekly. How's it going
[05:26] fellas? I'm good. Yep. Loving those intros, Pete. Thank you for doing those. Those pump me up every week. Me as well. Me as well. Maybe you put it together this week. No, no, no, no. You were right
[05:46] on key there. And we're hoping to keep the good vibes going with something that's a little irregular this week, which is that, yes, while our guest is currently working on an incubator
[05:59] project, Anthony, hi, working on a topic we covered, I think it was three weeks ago now, web integrations, web framework integrations. What we wanted to talk to him about more so today
[06:14] was his usage of AI to generate dash code. Now that sounds a little crazy to me. Rion, is there anything you can start us off with about why we want to talk to Anthony about this?
[06:27] Sure. And I think most like 99% of the code that he's working on in this particular project is probably generating more or less boilerplate code for the framework. Everything around the
[06:40] dash stuff. Yeah. But nonetheless, that is the majority of pretty much every application and every gap as they're called. They're mostly just traditional apps that call into a few
[06:53] functions from cryptocurrencies. So yeah, I'm looking forward to this. Personally, I have not really got into the whole AI thing. I'm going to ask Anthony some questions
[07:10] about that. But that's why we have him on because as far as I can see, I follow a lot of people in the web two space and a lot of people in the web three space. And there are various opinions
[07:25] about chat GPT and AI and everything. And Anthony is probably one of the leading voices that has a very good stance on this. It's very balanced, reasonable stance. And I think we'll get into
[07:43] why that is in the show. But that's why he's here. Well, Anthony, what is your balanced, reasonable stance in general?
[07:51] Well, I mean, I see myself kind of as like a fanatic with chat GPT at this point. I can still talk about the downsides, but I believe very strongly that everyone should be using it for
[08:03] all sorts of things that they haven't started doing it yet. And then you just need to be aware of what are its limitations, what are its downsides. But once you know that, what it can do
[08:13] for you, what it can't do for you, the things it can do for you is so incredible. And I've been following AI for a while. I was actually first learned to code because I wanted to do deep
[08:23] learning stuff years and years and years ago and never really got into it because I ended up learning web dev instead. But now that this whole thing has kind of swung back around,
[08:32] there's just really nice APIs where you can hook up JavaScript code to open APIs, AI API, if you want. But honestly, anyone can use this thing because the chat interface itself is the
[08:44] entire thing. It's a thing that can actually understand your language the way futuristic robots and sci-fi movies do. In every sci-fi movie, they talk to the computer. They don't
[08:56] type on their computer. They talk to HAL. They talk to the Lost in Space robot. So I think that's pretty cool that we now have that ability with computers. And I find some devs are like,
[09:07] they're correct to be skeptical of AI, but I feel like they kind of go too far into the, they emphasize the problems, then they just like don't use it at all. And it's like, well,
[09:20] the problems are limitations. Like the things it can do for you, I almost guarantee will save you time just because they can do so many small kind of little tasks. But I'll be curious, what are
[09:31] the stuff that you two have actually, have you ever used chat GPT? What have you done with it? Like, what was the first question you asked it? Yeah, I actually have a question right away.
[09:38] You said everybody can use it. And this is one of my, one of my first experiences with chat GPT was that I feel like I can't use it. And the reason for that isn't because I'm not technically
[09:54] able to, because it's very easy to use. But why I say that is when I first got on there, and I, the first thing I encountered was I have to sign up. I just, I hate that experience. I hate
[10:09] this point. I hate signing up for services. I want to just pay for services and not be a user on their system. I want them to be a user on my system. In other words, I want to be able to
[10:26] control my own identity and not be a user in Microsoft's database with all of my queries, cataloged and tagged as this guy is a dangerous wrong thinker to use AJ's term. I know like,
[10:42] personally, I'm not as I'm not as concerned about that as most people, like most people in cryptocurrency remain anonymous. And I am not so I generally am okay with the fact that,
[10:59] you know, I have bad ideas, like wrong ideas that are dangerous to the system. And I'm fine with putting my name to that. But I don't want that experience to be for everybody in the world
[11:11] that if you have, if you want to use this wonderful tool, you have to sign in and be categorized as whatever you're going to be categorized by, by Microsoft.
[11:22] I don't think so. This is gonna, so obviously, we're in the web free world. So we're kind of privileged that we can say we have systems that don't do this, but every other piece of software
[11:32] does what you're doing. And the social networks themselves are able to categorize you what you click who you interact with, to an extent that you can't extract that kind of stuff from like,
[11:43] really long conversations you have with an AI bot. And like, I've done I've had every wrong think ID could possibly think I'm gonna ask Chad to speak directly. So controversial ideas gonna get you
[11:53] canceled, then I'll be the first one. So I wouldn't really worry about that. The the thing about having to have an account and sign up and pay, this is, it's always gonna be a trade off,
[12:03] like, do you want to be able to run things yourself? You want to have a pay for use model? Or do you want a subscription service, they let you pay to use it, but you it's a monthly
[12:12] subscription. And the reason why it's worth it is because they have invented a core piece of new technology that you can't really use anywhere else, you can use other language models, but
[12:23] they're not as good. So and that's because it's integrated with Azure cloud. And there's a very tight moderation kind of model around it. Not moderation is not the right term. There's a
[12:35] there's, there's triggers on it to let them know when it starts producing content that they don't want, for lots of reasons. And they're, they're pretty good about like, not
[12:47] censoring political ideas and stuff. They're trying to like, make sure you can't build a bomb with chat GPT. Like, I think they've actually prioritized stuff like that pretty well. And,
[12:56] yeah, it like, you can purge your data if you want. How are we in the open source chat GPT alternatives, like is open source going to win
[13:06] this battle, and we'll be able to use chat GPT, or not chat GPT, but AI in general, with open source software and without accounts.
[13:16] So for anybody who actually hasn't seen this tool at work, I wonder if we could show Anthony's short demo clip, and then continue our conversation so that there is a visual behind.
[13:30] Okay, let's take a look at this. Let's just do this.
[13:47] Oh, the R support and TypeScript. Interesting. Oh, God, I already hate this.
[14:08] Yeah, no, no, no. Goodbye. Okay.
[14:18] So that was, I guess, maybe that clip didn't include the part where you initially asked it a question. Did that come before, Anthony?
[14:27] So what I did is I gave it my code, and the bug that my code was outputting, and I said, how do I fix this bug in my code?
[14:35] And then it gave you like those one, two, three, were they options? Or were they steps? Like first do one, then do two, then do three?
[14:42] I think it was probably going to do both. It would, usually it gives you a couple different things to do. And sometimes it may be a couple steps. So it was basically telling me to install
[14:49] like the Babel TypeScript dependency, and then configure TypeScript with Babel so that I could use decorators, which are only a stage two JavaScript language feature.
[14:59] So that's what was happening in that video. I just wanted to clarify one thing real quick. That clip was from a video that was on the
[15:06] Incubator's channel last week. So if you're curious to see more of that, just look at Anthony's video from last week, where he's actually working on that.
[15:14] And his voice that you were hearing was not today, Anthony, that was the video's Anthony. So yeah, just so everybody knows where we are right now.
[15:24] Yeah. On Dash Incubator's homepage of YouTube, there is a playlist that's called Anthony Campolo's Live Dash Coding. And that's where you can find that video.
[15:33] So I will answer the question that you posed to Rion and me before, Anthony, about each of our initial interactions with this tool. And then that'll lead us back to where we were before
[15:46] we watched the clip. So like Rion, when I first went to try out this chat GPT, I too was put off by, I want to say it actually asked me for my phone number.
[15:58] Yes, it did. That's where I drew the line. Yeah, you don't need to give it your phone number. You need to give it an email though, I think.
[16:04] Yeah, we need a service around this, Anthony. Whatever it was, I felt that it was asking for maybe even more information than I've
[16:14] been asked for at a bar or something. Like, you're not asking me for my phone number. You give me your phone number, that kind of thing. But then I broke down a few days later
[16:25] after I was looking through some of your videos, Anthony, and I thought, I'll just give it my phone number. I just really want to try it.
[16:32] Especially since you said the 4 version is, and others have said the 4 version is so superior to the 3.5 version. I thought, okay, I really want to give this a go. And so I went back to give it
[16:43] another go. And it was that time that I read the bit about like, la, la, la, we're getting better and better at withholding information we don't want you to have. I was like, what? However,
[16:56] they phrase it, like 83% better at not returning disallowed information or disallowed topics, whatever. So all that is to say, it brings us back to what we were talking about before the clip,
[17:10] which is, okay, so even though this comes from a company called OpenAI, it's not actually open source, right? Otherwise, there would be like many different versions of this.
[17:20] So the history of OpenAI is pretty complicated. They originally were open sourcing their stuff and writing papers, and they still write papers, and they still open source some of their stuff.
[17:32] Then they have some products that they just keep under their own kind of basically APIs. Because like I said, if you don't actually stop this model from doing certain things, it will be
[17:44] able to do things all three of us can agree we don't want it to do. I feel pretty confident about that. Or just like, not necessarily that we don't want to, but that we would feel reasonable as
[17:55] someone running a company that we would not want the liability of building a tool that would do this. That's the way I think it's really worth thinking about why what they're doing is not
[18:04] censorship-based actually is like, and not even cover your ass thing. It's just like, they started the company for AI safety concerns in the first place, and the term meant different things back
[18:16] then. So I don't know. I've been following this company for a long time, and I feel like they're actually of all the tech companies out there, they have better ethics than a lot of them.
[18:24] And there's just certain things that because it's such a unique technology, they want to have a gated API so they can work with it. And plenty of companies work that way. I think there's always
[18:35] going to be a mix of like totally open source web 3 stuff, and proprietary things that people want to lock down. I think those things can coexist with each other. They're giving you something
[18:44] preferably so valuable that you are going to want those trade-offs. - Uh-huh. I just want to clarify something before we move on to make sure I understand.
[18:53] When you say Anthony, I think we can all agree that there are some things that none of us would want this tool to do. Can the tool actually do anything other than simply return information?
[19:08] Like, can I tell the tool like, "Hey, chat GPT-4, take out the power grid of Shanghai." Like, can it actually do things, or can it just return information?
[19:18] - Yeah. So what I was referring to is like the kind of example I use, like returning how to like mix chemicals to make a bomb or things like that. And in terms of actually
[19:31] taking actions in the world, you can hook these things up to things that do things in the real world. By itself, right now, it's just a chat interface. It's not able to actually do things.
[19:43] It's this idea of kind of turning models into agents, where then they can kind of go off into the world and do stuff. Those things kind of freak me out, honestly. I think if I was concerned
[19:52] about anything AI-based, I would be concerned about the workaround agents right now, and that most people aren't really talking about why it's more dangerous than all this other stuff we're
[20:00] building right now. So yeah, that's kind of a weird thing, but chat GPT does not do that. - Can you give us a brief summary of what you've done for Dash specifically with this tool
[20:13] in your last couple of streams? - Yeah, actually, what I should do is I should get that thing up so I can just show it,
[20:26] show exactly what I did. Just give me... - Yeah, and while you're getting that up, I'll do my best job of explaining what you did.
[20:33] Like AJ, one of the things that I like most about you as a developer is that you are very, you take good care to document your work, and so I think that's probably what you're bringing up,
[20:47] but... - I'll get you the chat GPT interaction itself and scroll through what's happening here.
[20:54] - Okay. - Yeah, all right. I am sharing.
[20:58] Great. Probably not gonna have any of those. - So this is a conversation that spans the whole of your work with Dash, and...
[21:10] - So what happened here is that I started by... Let me also go to the example. So I started by building a React component that was just fetching some kind of Dash data, and so this was a React
[21:30] component that I wrote, and I knew that I was gonna be wanting to build this in a whole bunch of other frameworks. So the first idea, as I said, take this React component and implement
[21:42] the identical functionality with a Vue component. So this is what's called a prompt right here. You give it a prompt that basically kind of sets it up to do something, and then you feed it data
[21:54] after the prompt. So after you give it the prompt, then you give it the code, and it will hopefully take that code and do exactly what you told it to do with it. So does that make sense so far?
[22:03] - Yep. - And can we get any closer on your screen here, Anthony?
[22:08] - There we go. - Thank you.
[22:11] - And then for this, this is now the Vue component, and it even specifies that it's doing it with Vue 3 and the composition API, because Vue 2 had a slightly different syntax,
[22:25] which is nice, because this is more similar to the React component we just did. And let me pull these up like side by side. Let me show you. So if we look at the original component, we have
[22:46] things like the blockchain data. That's like the state. And in the React component, you have that state, and then you're going to show it down here. And it's the same thing with
[22:59] this component. You have your blockchain data state. So the syntax is different, but the component is doing the same thing in the sense that it has a button. You click the button, and then it displays
[23:12] data for the dash domain. You pass it. So then I just did that with every other framework, and it basically spits them out like one after the other.
[23:27] - Yep. And the specific data that you're getting here is very basic. It's just your hello world of Dash platform, right? Can you scroll to where that business logic is of
[23:40] getting the Dash blockchain data? - Yeah. So let me pull up the project itself. Okay. So we have here an API, which is an Express server, and we're importing a Dash client. So this
[24:10] is where we're connecting with a... So we do testnet, and then a mnemonic. And so I have these in environment variables, but on this, I just cloned out a new project. So there's none yet.
[24:24] - So you're using the Dash SDK, which is the culmination of all the work that Dash core group has done on Dash platform. The Dash SDK is what wraps all that together in one simple library.
[24:41] - Yep. And then we export the client, import the client here, and now this is what calls the whatever name you pass it, and then it adds the Dash domain, and then resolves it so you can get
[24:56] that data back. - Gotcha. So you wrote this in React, and then how many different frameworks did you have chat-gpt help you convert this into?
[25:07] - Yeah. And actually, just to clarify, so this is the Express server that returns it, and then in React here, this is the component that then fetches from that server running on localhost.
[25:20] So the Express server is just you create it once, and then you have this API that is going to give you back the data. So partly, this particular example worked really well because the front
[25:32] and the back are totally decoupled, and that's going to be the case for the most part when we do this stuff. So let's see. How many do we have here? We have...
[25:40] - Just so everybody knows, you can actually use this SDK on the browser as well without using an Express server or any server for that matter. I don't know if that's how you set this
[25:52] up. Are all of these front-end clients contacting the Express server, or...? - So you only want to call it from the client if you're not going to be passing it any important
[26:02] wallet information. And then I tried that. I hit a bug. I'm not sure if that was be here at the library, but that's going to be one of the first things I'm going to do once I finish these example
[26:12] apps is start doing other places for the Dash SDK, either like a serverless function or running on the browser or like an edge function. - Right. So your intuition was that,
[26:23] "Hey, this 12-word seed phrase is something that's very private. Therefore, I need to have my own server to have the Dash mnemonic," as it's also called, "in an environment variable." But a
[26:38] different project that the incubator is working on is bringing a wallet into the browser that's encrypted and everything where you could have potentially that be your secure storage for your
[26:51] Dash seed phrase. - Okay. That's super sweet. Yeah, I didn't know that. - So, cool.
[26:59] - Your question was, "How many of these did I do?" So I did... Let's go back to this one. So I did Vue, then Svelte, and then SolidJS, and then just vanilla JavaScript. So this is interesting now. So
[27:18] then I asked for Qwik. This is the first one that says this is too new. This is a problem if you try and work with really cutting-edge libraries that it only is trained up to September 2021. So there's
[27:31] ways to get around that. If you feed it some code from Qwik, you could get it to figure it out. But I just kind of skipped it for now. And then Angular, and then Preact. And all of these, by the
[27:43] way, every single one of these, you copy and paste it, and it works. It didn't give you kind of the component with some bugs you had to fix. It just gave you the entire working code. And then lit
[27:54] HTML, and then Alpine. So it's like eight, I think. - And how long did this take you, roughly? - The time it takes for ChatsGBT to export the answer, basically. Because you just
[28:08] copy-paste the code from React and say, "Rewrite this." And actually, I think I just said it each time. You should say, "Rewrite it again in Svelte. Rewrite it again in SolidJS." That's all you do.
[28:20] And then you wait, like, 30 seconds for it to do this. So this would have all taken, like, five minutes, maybe. Yeah. - So you wrote the original code, Anthony, and then you used this
[28:32] tool to translate it to as many other programming languages as you were looking for. - Yeah, right. Which is the thing I could have done on my own. I know most of these frameworks, but it would
[28:42] have taken longer because I'm not as fast in Vue as I am in React. And then there's, like, context switching. How do I fit these specific parts of the component to these specific parts
[28:52] of this other framework? So, yeah. Really, it's an incredible time-saver. - And so, other than translating one programming language to another, which you've shown us here,
[29:03] have you found that, at least in your Dash work, that the tool is useful for anything else? Like, ChatGPT make this Dash program do XYZ or whatever, like, something from scratch where you didn't
[29:17] ask it to translate? - Yeah. So I have also used it for debugging. So this is an example of where I have, like, and this is an Angular bug, but basically you just say, you, like, say what you
[29:32] did and, like, that you're getting an error. And you give it the error. Sometimes you want to give it some code, too, so it has, like, context. But a lot of times it'll say, like, so it says,
[29:41] this error message is from the Angular router. It's saying you have a rough configuration, it doesn't have one of these. And it kind of explains those concepts. So that's pretty cool.
[29:50] In terms of generating things from scratch, yes, that's not done yet just because I have, like, all these frameworks to kind of build out. But the great thing about ChatGPT is that
[30:01] whatever you can think of, you can try. And you'll get an immediate response whether it, like, works or not. So you can try just, like, start asking questions. Actually, I don't want
[30:11] to open my sidebar because it shows all your chat histories. I'm going to stop sharing real quick. - Maybe we can pull up Halawi's comment again. - He says I've used ChatGPT4 to comment
[30:28] my modern Fortran code and verify that I'm doing things efficiently. It's extremely powerful and has increased my productivity, but you have to verify the responses.
[30:36] - Modern Fortran code? Is that a joke? I'm not sure if he's being serious there. - If it is, I didn't get it. - Maybe there is modern Fortran code.
[30:51] Anyway, I have a question about what Amanda was talking about as well. I would love to be able to integrate ChatGPT in our documentation site at some point where a new user from Dash comes
[31:12] into Dash, and instead of, like, browsing the documentation just line by line and subject by subject, category by category, and trying to find out what he's looking for, you just have that
[31:24] prompt message in the documentation, and it's embedded, rather than going to, like, the ChatGPT site. Is that possible right now, and what would we have to do to our documentation site to get
[31:36] something like that? Because I know that, like, I think it's Svelte or one of these - - I was just about to pull this up. So there's a couple that are doing it. One that I think is
[31:47] pretty good right now and worth checking out is Houston. So Houston is the Astro one, and they got this set up back, like, January, so it's already been around for a while.
[32:00] - That's right, yeah. - Sorry, what are Astro docs? What's that? - So Astro is a front-end JavaScript framework that lets you build with a lot of - so it lets
[32:13] you use all the different frameworks, like, so I was showing you how I did all those things in those different frameworks. Astro is a way to build a site, and you can use kind of any of those,
[32:22] but it's also very content-focused, so you get really fast static builds and stuff. It's just a super sweet tool, and they have pretty good docs too.
[32:31] - And this is part of their docs, Houston.Astro.Build. So what is Astro, and why is it great? - Yeah, I would love to have something like this on the Dash site, so you could just say,
[32:46] "Hey, how do I set up a server, a Dash server, to listen for transactions?" And then, instead of manually going through the documentation, it just kind of tells you how to navigate the docs,
[32:57] because our docs are huge. - Interesting. So this gives a pretty good answer here. There's some weird going on in the resources here, so I would say don't try and
[33:12] get too fancy with it, would be my advice when you're doing this with Dash. Let's say - I've never actually used this. I just have known they've had this. Yeah, so I would - I'm not sure
[33:32] if this tech is in the place now where you can just plug it into someone's docs and actually get it to work the way you want it to work. I would say you're going to be able to do it if you're
[33:42] willing to put a lot of time into figuring out how to work with OpenAI's API specifically, but I wouldn't try and use a plugin or something, because you just don't know. This is - like,
[33:56] ChatGBT can handle this with no problem, so there's - this is why I say there's - not all language models are created equally, you know? - Right. But are there any generalized tools
[34:07] where you can feed it your own - like, feed it the documentation - our docs? - Yeah, so - - And then it kind of
[34:15] digests them and helps people get answers? - Yeah, so there's - the thing you got to do you got to think about first is that you can't just feed, like, questions about dash docs to
[34:33] ChatGBT, because it wasn't necessarily trained on the dash docs, so what you need to do is you need to use what are called embeddings. So embeddings are how you basically take a big
[34:44] chunk of text and then feed it to an already trained model and say, "Hey, I want to give you some new - it's like in the matrix, like, they plug Neo in, like, download a bunch of knowledge
[34:52] into their brain." This is how you would download Dash's knowledge into it. You create some embeddings, and then you could ask it questions through your normal kind of, like, chat type stuff.
[35:03] - And do they keep that data? Like, I guess the servers that make up ChatGBT, if you feed it the dash docs in order to execute on your particular goal, do they keep those dash docs, or do they
[35:16] kick them? - So they - the stuff has kind of been in flux recently. I want to say I think that now they delete data after a certain amount of time. If that stuff does particularly bother you, there
[35:29] are ways to do this without using OpenAI, so... - No, it would bother me if they kicked them. - Oh, they kicked them. Cool, yeah. Yeah, so, I mean, if you want the stuff to be open, like,
[35:39] that's why I say, like, don't - obviously don't feed ChatGBT, like, your credit card, but I would say, like, for the most part, if you're doing kind of fairly not ridiculous things,
[35:48] then it should be good. But yeah, so you basically do the embeddings, which I have not done, so I can't really speak too much about that, and then you actually feed it, but I was going to show you
[35:59] Hugging Face, which is here you can actually run, like, open source models, but let's see if you want to do - so this would have been GPT2 way back in the day. So this is an open source version of
[36:14] one of the older models of ChatGBT, or the thing that became ChatGBT. - CMDRskullcrush says, "Open source LLM lang chain is able to digest a knowledge base, become an expert within that
[36:29] domain, and build a chat bot on top. No OpenAI proprietary code necessary." - That's what I I'm looking for. - Yes and no. Lang chain can do it without OpenAI, but you want to use the
[36:40] OpenAI plugin with lang chain to do that, because then it would be better. But I agree, lang chain is super cool. That's a good call out. It works with a lot of other non-OpenAI APIs, but you kind
[36:54] of have to test those out each individually and see how good they are. - Well, I love this idea of language learning models, but I just - I wish that Dash could kind of help the open source
[37:14] competitors in this field, so that we have, you know, a viable open source alternative to the big box. - To the big box? You're talking about ChatGBT? - I mean the big companies. - Well,
[37:29] here's the problem, is that right now it's economically infeasible for anyone but a company with billions of dollars to have created this model in the first place. It cost many, many,
[37:42] many millions of dollars just to train the model to where it is now, let alone continuing to run it. So, this is actually - there's something I wanted to say, but I forgot, is that when you're asking
[37:52] about open source, so no matter what, in some amount of years, an open source model will be out that is good and as good and better than GBT4. It might be a year, it might be five years. It's
[38:04] kind of hard to say at this point, but eventually we'll get there. It's hard - - Well, only if you focus on it though, right? Like - - People are. There's a lot of open source work happening on
[38:14] this, don't worry. - Yeah, the open source community has to make it happen because they won't just - it won't just happen on its own. Open source will catch up and surpass closed source in AI. The
[38:27] article "Google has no moat" illustrates that very well. Well, that's encouraging. I hope that happens. I just know that open source has struggled against the very focused corporations that have
[38:45] VC and ultimately government backing as far as their funding goes. So, it's a big rabbit hole that I won't go into in this episode, but I would love to have Dash be part of the solution with
[39:00] open source funding in general. And yeah, well, we need a lot of changes for that to happen, but - - I mean, there's lots of interesting ideas about integrating blockchain and AI stuff because the
[39:12] models themselves are really, like, people are paying for a lot of compute and things like that. So, if you had some sort of, like, you've heard of Numeri? - Yeah, I have. - Yeah, it's like a
[39:24] stock market betting app, or, like, you bet, like, you, maybe it's betting, you have a coin and it's hooked up to, like, AI and just a market. So, it's all together. - I think, personally,
[39:37] I think that the only place that blockchain and cryptocurrency could help AI is in funding. Like, blockchains and cryptocurrency, blockchains in general, it's one of the most least efficient
[39:50] computing platforms there is because you have to do multiple things on multiple servers. It's built for security and robustness, not for efficiency. So, we're never going to, I don't know, I won't
[40:04] go into the details about my opinions on this because I'm not an expert, but I think that we could really help with the funding model, and that's, again, that rabbit hole that I won't go
[40:13] into. But any, before Amanda really closes us out, do you have anything that you wanted to tell us, Anthony, about your journey with open AI and that we haven't already discussed today?
[40:29] Because I know that you know a lot and we've only been 40 minutes in here, but. - Yeah, I mean, like, so, I. - Do you have any specific recommendations for any developers who want to save time
[40:41] and effort the way you are? - Yeah, sure. So, I would say, so, this is the advice I've been kind of giving people, is you should start by just identifying some sort of repetitive task you have
[40:54] within your every workday. You know, it can be scheduling a meeting, it could be writing an email, it could be doing something, and just, like, try and think of, like, okay, can I have
[41:02] chat2BT do that for me or do most of it for me, and then just kind of start, like, integrate, like, one or two things into your workflow. So, for me, what I do with that is I have a newsletter I write
[41:13] every week, and so I'll pick, like, I'll really, like, in-depth, like, kind of update for, like, a blog, like, an open source project, like, Asho 2.6 coming out, you know? I literally just take
[41:26] the entire article, plug it into chat2BT, and say, write me a one-paragraph summary or two-paragraph summary, however long you want it to be, and it just takes the whole thing and, like, condenses
[41:38] it down to, like, the exact summary I would have wanted to write myself if I had the time to read through every single line, perfectly condense it down the way I wanted to. So, that's pretty great,
[41:48] and you don't have the hallucination problems. It's not going out and finding data in its brain. It's just taking something, you give it, and it condenses it down, so it's not adding anything.
[41:57] So, that's where you don't get the hallucination problem, which is, like, really great because you still should check the output, but you don't have to, like, be as worried that the output's going to
[42:05] be totally crazy and ridiculous and incorrect, and then I also use it to, like, fix bugs in my code, but also, like, just ask it weird philosophical questions, like, or ask it to analyze a piece of
[42:16] art or ask it to write a poem about something in a style of something. Like, I do all sorts of just weird stuff with it just to see what it does, and it's, like, really fascinating, actually,
[42:26] sometimes, what it does. >> Okay. Well, right on. I will say thank you for sharing that with us today, Anthony, and I know that there were other places that were calling your attention today,
[42:44] and you chose to join us instead, so extra special thanks for that. >> It was way better than a meeting. >> Well, I wasn't going to come out and say
[42:53] Anthony skipped a meeting, but Anthony skipped a meeting. Maybe send chat GPT in your place next time. All right. Thanks, everybody. We will see you next time. >> Ciao.