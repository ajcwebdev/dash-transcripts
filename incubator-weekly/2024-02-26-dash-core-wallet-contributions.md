---
showLink: "https://www.youtube.com/watch?v=niGN4q3DJVA"
slug: "dash-core-wallet-contributions"
title: "Dash Core Wallet Contributions"
publishDate: "2024-02-26"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/niGN4q3DJVA/maxresdefault.webp"
---

Alessandro, a physics student and cryptocurrency enthusiast, discusses his contributions to the Dash code base as a hobby developer.

## Episode Summary

tl;dr: Alessandro, a 23-year-old physics student and hobbyist developer, shares his experience working on various Dash Incubator projects, including BIP143 implementation for improved transaction verification performance, Masternode Multiparty Payouts, and theoretical ideas for Masternode Trustless Shares. Despite focusing on his final year university exams, Alessandro expresses interest in potentially pursuing full-time cryptocurrency development in the future, drawn to the practical application of advanced cryptography concepts.

## Chapters

05:04 - Introduction and Alessandro's background
Pete and Amanda introduce the episode's guest, Alessandro, a young developer who has been contributing to the Dash code base as a hobby alongside his physics studies at university. Alessandro shares how he discovered the Dash Incubator bounties through a friend and his prior experience working with the PIVX cryptocurrency, which has a codebase similar to Dash.

09:16 - Current focus: BIP143 implementation for improved transaction verification
Alessandro discusses his ongoing work on implementing BIP143 in Dash, which aims to improve transaction verification performance by optimizing the signature hash computation process.

17:37 - Progress and challenges with the BIP143 implementation
Alessandro outlines the remaining tasks for the BIP143 project, including writing more tests and addressing feedback from the Dash developers, while also noting that the implementation will likely be included in a future version of Dash due to the need for a hard fork.

18:49 - Other projects: Masternode Multiparty Payouts and Trustless Shares
Pete and Alessandro discuss two other projects he has been involved with, Masternode Multiparty Payouts and Masternode Trustless Shares, with the latter being a more challenging and theoretical project at this stage.

26:58 - Balancing Dash development with university studies
Alessandro shares that he is currently focused on completing his final year physics exams and master's thesis, treating Dash development as a hobby for now, but expressing interest in potentially pursuing it full-time after graduation.

31:20 - Personal motivation and interest in cryptocurrency
Alessandro discusses his primary interest in the technology and engineering aspects of cryptocurrency, particularly the practical application of advanced cryptography concepts, while also acknowledging the economic incentives as a secondary factor.

34:41 - Final thoughts and future plans
Pete and Amanda express their appreciation for Alessandro's initiative in contributing to the Dash project and inquire about his plans for full-time crypto development after completing his studies.

## Transcript

[00:00] [music] Most of us have gained value from a pithy quote.
[00:08] Whether it be inspiration, a thought-provoking perspective, or witty summation, quotes can encapsulate timeless wisdom.
[00:15] So this week, we're going to visit some quotes and detail their relevance to Dash and why we build. [music]
[00:21] "If you are depressed, you are living in the past. If you are anxious, you are living in the future.
[00:26] If you are at peace, you are living in the present." - Lao Tzu, author of the Tao Te Ching.
[00:31] Instead of constantly harking back with longing at the previous all-time high, or spending hours a day staying abreast of the latest saber-rattlings emanating from DC and the BIS,
[00:40] focus on the moment, focus on acting. [music]
[00:45] "The real truth of the matter is that a financial element in the larger centers has owned the government ever since the days of Andrew Jackson, Franklin Delano Roosevelt."
[00:53] What FDR said is even more relevant, even more entrenched, today. It sets the stage for why we're in this space,
[00:59] why Satoshi published the Bitcoin white paper, and why we feel driven to build.
[01:03] [music] "Major change will not happen solely by asserting a long-term goal
[01:09] and by protesting against the status quo. Responsible, wise, and effective strategic action is required."
[01:15] - Gene Sharp, who researched and employed nonviolent action. "Simply clamoring to audit the Fed or to end the Fed is not sufficient.
[01:22] There must be a better alternative. That's what we need to continue building."
[01:25] [music] "We should cease looking to power structures,
[01:29] hierarchical systems, or governments to help us, and devise ways to help ourselves."
[01:34] - Bill Mollison, co-founder of the Permaculture Movement. This quote places emphasis not on courting corrupt institutions,
[01:40] but on understanding natural relationships and acting in accordance for true sustainability and thriving.
[01:45] [music] "There was no man born marked of God above another,
[01:50] for no man comes into the world with a saddle on his back, neither any booted and spurred to ride him."
[01:55] - Richard Rumbolt, a leveler who was executed for speaking truth to power. "We need to realize, to internalize the fact,
[02:01] that if an act is wrong for me or you, it cannot be right for someone else based on their surname or title.
[02:06] We need not to cower, but be bold." [music]
[02:11] "To have a good future, we must undertake good actions, now." - Jeff Nabel, an engineer who opted to vote with his feet
[02:17] rather than pay tribute toward a system he viewed as unjust. This quote encourages not just action, but good actions.
[02:23] "In our quest to see dashed adoption grow, we must not take questionable shortcuts."
[02:28] [music] "The easiest way to self-confidence is action." - Eric Hoffer,
[02:34] an autodidactic longshoreman. "We are confronted with a narrative ripe with fear, uncertainty, and doubt,
[02:39] one pushed by power centers that thrive on conformity and on regurgitation of their talking points.
[02:44] For example, associating crypto with criminality. Rather than be concerned by such red herrings,
[02:49] we need to keep moving forward." [music]
[02:53] "Correct movements under load are corrective." - Chris Duffin, engineer-turned-powerlifter.
[02:59] "We need not just to build, but to build smartly, in real time. We need not develop for years in an ivory tower,
[03:04] believing that perfection can be obtained in a vacuum. We need to subject our offerings to market forces at every iteration
[03:10] and remain ready and excited to adjust." [music]
[03:15] "Condemnation does not liberate, it oppresses. And I am the oppressor of the person I condemn,
[03:19] not his friend and fellow sufferer." - Carl Gustav Jung, psychiatrist known for his insights into the shadow self
[03:25] and the collective unconscious. "We need not position anyone as an enemy.
[03:29] We can recognize that individuals vested in the current power structure will find it in their short-term interest to lash out at competition.
[03:35] But we are working to supplant that unjust system with one more just, and we hope to gain them as users.
[03:40] Thus, it behooves us not to vilify, but to understand." [music]
[03:46] "When souls reach a certain clearness of perception, they accept a knowledge and motive above selfishness." - Ralph Waldo Emerson,
[03:52] transcendentalist author and speaker. "We are primarily motivated not by price go up,
[03:56] but to help reduce division, to help our fellow man." [music]
[04:01] "I am truly free only when all human beings around me, men and women alike, are equally free.
[04:06] The more extensive and comprehensive their freedom, the more extensive and profound my freedom becomes." - Mikhail Bukonin,
[04:12] 19th century writer and direct action advocate. "Unlike the current legacy financial systems
[04:16] which empower an oligarchy that relies on force, we work to empower each single person and rely on voluntary interactions."
[04:23] [music] "No one can violate a right that you have willingly and voluntarily relinquished." - John McAfee,
[04:30] programmer and privacy advocate. "If we seek permission to operate, such as obtaining special legal statuses,
[04:36] we cede authority and open ourselves up to being targeted. Rather than play that game,
[04:41] we should strive to make every component in the Dash ecosystem invulnerable to coercion, so any threats, now or in the future, are without purchase." - John McAfee,
[04:51] "As solid as these quotes are, remember, the most important is your own voice within." - John McAfee,
[04:56] "The most important is your own voice within." - John McAfee, "The most important is your own voice within." - John McAfee,
[05:01] "The most important is your own voice within." - John McAfee, "The most important is your own voice within." - John McAfee,
[05:06] "The most important is your own voice within." - John McAfee, "The most important is your own voice within." - John McAfee,
[05:12] "The most important is your own voice within." - John McAfee, "Yeah, I, as I appreciated, as always, the thoughtful introductions by Pete.
[05:21] I think what, how I would summarize all of those quotes, at least my feelings internally through watching that,
[05:31] was the importance of just mindfully thinking about what you want to accomplish, but then not stopping there and actually focusing towards action.
[05:43] So this healthy balance between thoughts and actions in what we're building and why we're building, and then actually building.
[05:50] So happy to, I don't know if you finished what you're eating there, but I'm happy to continue this conversation with our guest today.
[05:59] - Yes. - Because he is doing just that. He's actively engaging in this space.
[06:05] And I guess the first thing I'll say about the guest is that I did not recruit him, so I'm very interested to know
[06:16] how he came around and what he's doing here and, yeah, why he's building. - Alessandro, would you tell us how and when you first
[06:28] claimed a Dash Incubator bounty task? - So yeah, so like two months ago,
[06:37] or like during December of 2023, a friend of mine told me about Trello and,
[06:47] I mean, I already knew Dash, but I did not know that you had this Trello with the bounties and tasks.
[06:58] And so, yeah, a friend of mine shared me this link and told me that if I was interested, I could apply for one.
[07:09] Yeah, and I found many tasks are really interesting for me. And so I said, "Why not? I can."
[07:18] And I began working for Trello and for the portfolio. - And the method by which you came to have familiarity
[07:34] with the Dash code base came before. How did you, what kind of work were you doing before
[07:41] that gave you this familiarity with the Dash code base? - Yeah, like before Dash, I've been working like for one year or something
[07:52] with a fork, which is called the PIVX. - Oh, interesting. - If you know.
[08:01] And like the code is very similar. And so it really helped to transfer the, like to write code on Dash,
[08:13] it was useful knowing how to write code on PIVX because it was similar. - Fantastic. - So yes.
[08:21] - Right, yeah. And the first time I saw you was you popped in the Dash Developers Discord
[08:26] and mentioned something in the Jobs channel. So, yeah, that's how I came across you.
[08:32] And then since I always follow all of the repositories on Dash, like the Dash Pay organization on GitHub, and I saw your name popping up there,
[08:49] also saw, you know, you and I messaged back and forth about what you wanted to work on, and you said that you wanted to focus on C++ stuff.
[08:58] And we, as far as I can remember, you're working on, you've touched at least three projects in the incubator, but I think you're focusing mostly
[09:07] these days on one of those, which is, do you want to tell us about that? What you're focusing on right now?
[09:16] - You mean the one about BIP143? - Yes. - Okay, okay.
[09:27] - I think so, yes. - Yeah, because I work on more than one project at the same time.
[09:33] So, yeah, I was not sure. - Yeah, so basically, that one is like a more efficient way to compute
[09:47] the signature hash of transactions, which is the part of the transaction which is actually signed with elliptic curve cryptography.
[10:00] - Okay. - And so, it is like the slowest part of the whole verification process.
[10:16] And, like, on upstream on Bitcoin, they had a lot of problems because they received very large transactions, and the nodes took a lot of time to, like,
[10:29] to verify the correctness of the transactions, to verify the signature. And so, they came up with this improvement, which, like,
[10:38] makes verification time much faster. So, this is the idea behind.
[10:44] - Okay. - And so, on Dash, we want, like, to have the same feature, but there are some
[10:52] complications because our transaction fields are a bit different. So, our transaction have the type, have the payload of, like, the payload
[11:06] of special transactions. And so, the point is making an algorithm that include what our particular
[11:23] transaction type, that's the point. - Okay.
[11:27] - And is this something we can look at via screen share from your side, Alessandro? - Yes.
[11:33] - Let's have a little look. Okay, let me open the Dash.
[11:44] - I thought you had to be older than 50 years old to know C++, by the way. And you don't necessarily sound like you meet that criteria.
[11:54] I guess strange things can happen. - What did you say?
[11:59] - I'm just teasing you. - You're too young for a C++ programmer, is what she said.
[12:05] - You're a young chap to know C++. - No, actually, I'm 23.
[12:10] - Oh, so, you are plenty old. Okay, you're right.
[12:13] Good. - I had my time to learn.
[12:17] - Good. - Okay, so you can see a thing.
[12:30] - Yep, we can see it. - One second, because...
[12:52] No, okay, I opened the wrong folder, sorry. - It's all right.
[13:02] - So, I think I have to share again. - Okay, that's okay.
[13:16] Pasta doesn't either... Pasta doesn't either what?
[13:19] Oh, Pasta started learning C++ at the age of 16 with MooCowMoo as his mentor. There's an interesting historical tidbit.
[13:27] - Wow. - Okay, is this...
[13:32] - Go ahead. - Is this the right folder here then, Alessandro?
[13:41] - I don't know why I'm having a problem. Fetch only one.
[13:54] Okay, I found it. - Okay, so you can see it, right?
[14:04] Yes? - Yes.
[14:06] - Here. Okay.
[14:08] Okay, like, I can go directly into the code I've wrote. - Please.
[14:17] - Which is... Yeah, so, for example, like here, okay, so this is the function that takes the transaction
[14:45] and generates the signature hash, which as I said before, it's the part that gets actually signed with the elliptic curve cryptography.
[14:59] And so, what I did was basically saying, "Okay, if we have the new signature version, you apply the new algorithm. And so it takes pieces of the transaction, like the version, like the...
[15:18] here, yeah. So it takes in input pieces of the transaction, like the version, the hash of the prevails of the transaction, the hash of the sequence of all the inputs,
[15:36] the prevails of the transaction, the script code, the amount that the transaction spends, and so on. And so, for example, the extra payload, if the transaction has an extra payload,
[15:49] the lock time, and the SIGHASH type. So it takes in input all this information and it computes the double SHA-256 and return it. So this is it.
[16:07] Okay. And... Yes? Yeah, so it sounds like this is a performance-related issue, right?
[16:16] Like... Yeah, mostly performance, yes. Okay. And how... Have you actually... Have you submitted a pull request for these changes? And
[16:28] how has that been received so far? So, so far, I have a few comments. So a dev suggested some changes, like...
[16:40] And yeah, I think it will take a while to get actually merged because it's... Devs are currently working on other stuff. So this is, like... This change requires, like,
[17:01] an hard fork. And so it will be, like... It will be included in the next version, which is v21. And currently, they are releasing the v20.1. And so there is, I think, a lot of time yet to
[17:19] reach version 21. Okay. Yeah. But of course, I can finish... I will finish before they... I will try to finish before, of course.
[17:30] Okay. All right. What remains to be done? When you say you have yet to finish, what remains to be done?
[17:37] Like, I have to write more tests, I think. Because this needs a lot of testing. And the more we have, the better it is.
[17:48] Yeah. Okay. So now, I have at least three projects that I... Like I mentioned earlier, that it seems
[18:02] like you're working on. There was Masternode Multiparty Payouts. And then there was Porting Bitcoin Caches BIP143 to Dash. And what is that? What is BIP143?
[18:17] Yeah, that was this one. That's this one, right? That's what I thought. So this one actually origin... Like the idea,
[18:25] the concept was from Bitcoin Cache, not PIVX. I don't know if you said that maybe already. And then the third one that I have on my list is Masternode Trustless Shares. So
[18:37] Multiparty Payouts, this one that we've just talked about, and then Trustless Shares. Can you say anything about the other two? Have you done much on those? And what's your
[18:49] interest in those? Yeah, so I think the most challenging is the one with the Masternode with many shares.
[19:07] But it requires the Multipayouts first. So I haven't touched the one with many shares yet. Right.
[19:19] So whose concept is that, Rion? Let me just come out from under the rock I've been in under and say, I didn't know that there was a concept in the incubator
[19:28] for an implementation of Trustless Shares. Whose is that? Great. What? Yeah, it's actually been a project in the incubator, at least on the board for a long
[19:43] time, several years. I'm pulling it up right now. But it is one of the more complicated ones. And it's one of the more... It's one that I haven't focused on personally. It didn't used to be my
[19:58] project. It is now. I think it used to be Tim's. It's like I said, still pulling up, but it's not my focus yet. As far as I know, there are prerequisites that need to be done before we can
[20:14] do that. And I believe this Masternode Multiparty Payouts one is that prerequisite, at least one of the prerequisites. So I think maybe we could talk about that one real... Well, maybe not real quick,
[20:28] but let's talk about that one. Because I know that's one that users might be more interested in. Like the one that we talked about already, this improved signature verification. This is great
[20:43] from a performance standpoint, but it's not one that users probably care too much about. So let's talk about this Masternode Multiparty Payouts project.
[20:52] How did you come across this, and what have you done before? At the beginning, I thought that it was quite easy to implement. Because, I mean,
[21:08] there was already a DIP written. And so it was like, just implement what it says. And that's what I did on Core Wallet, like two months ago. And so, like here, I can
[21:31] share my screen again. It switched back to your code editor. I'm not sure if you noticed that. Yes, yes. I have to share another screen. Okay.
[21:45] No. If we were just talking about the card, I have it here, if that's okay. Or we can share something else from your end, Alessandro.
[22:03] Halawi says Masternode Multiparty Payouts has a lot of complexity and goes deep into the core code, according to developers.
[22:10] Yeah, it goes deep in the code, but I think it is not too difficult. I mean, at least, okay, so you can see here?
[22:21] Yes. Okay. So this was the pull request I opened.
[22:30] Like, yeah, that's given me a lot of comments. So they reviewed the code. Oh, wait. Can you go back up to the top and scroll a little slower?
[22:43] Oh, yes. Just if you're going to be scrolling, yeah.
[22:46] Like, so yeah, this is a bunch of things that I should change. This is like a review. Mm-hmm.
[22:55] And then, yeah, those are my commits. And this is more review. Mm-hmm.
[23:04] Yeah, so this is it. So how would you summarize the roadmap on this one? Is this something that
[23:20] the Dash Core group developers are interested in merging at some point? Or has the feedback been mostly positive or mostly negative or neutral? Or how has that been?
[23:33] So, so far, the feedback on the core wallet has been positive. The problem is that soon we will have Masternode reward relocation.
[23:48] And so the platform will pay some Masternodes too. And that's where issues begins. Because we need the same feature implemented on the platform,
[24:01] basically, before merging it into the core wallet. It can't work on the core chain without also functioning on a testnet side platform chain?
[24:19] Yeah, it can work. It works on the core wallet. But the problem is that the platform will need to pay Masternode too.
[24:30] And so the platform needs to support multi-Masternode payment. Does the platform pay Masternodes?
[24:40] It will pay Masternode soon. Or does it pay EvoNodes only? And by EvoNodes, that's what they call the Masternodes that
[24:49] have 4,000 Dash? Yeah, it pays EvoNodes, but EvoNodes is also a Masternode that can have more than one payee.
[25:02] So you're saying that what you have submitted could work on the core chain to pay Masternodes right now, but what you're sensing is that the DCG developers don't want that solution
[25:16] unless it also incorporates, unless it also works on the platform chain to pay the EvoNodes. Yeah, exactly. So there is the need of another pull request on the platform
[25:31] that does the same thing, but for platform. Okay. Yeah, I was just scrolling through the pull request itself again and looking at some
[25:44] of the comments in more detail. So are you going to continue, are you wanting to continue working on that other pull request that they and you are saying is necessary?
[25:57] I can try, but yeah, I will try. I actually have already looked a bit into the code of the platform.
[26:07] Yeah, it's a big, that's a lot to learn. Yeah, it's a lot of stuff, yeah.
[26:14] So in theory, it is not too difficult to implement, but for example, I saw that the platform uses another repository that does like
[26:29] RPC calls in Rust, and so that repository needs also to implement multi-masternode payees. And so it's getting like more and more work to do.
[26:42] Yeah, okay. Now, I just wanted to take a step back now from the actual work that you're working on and talk a little bit more about like how this is fitting into your life.
[26:58] Like is this, is working on Dash something that you're interested in doing more of? Is it something more of a side project? And then like the PIVX side of things,
[27:11] are you still working with them? And what's your personal path forward? And what are your personal goals, I guess I would ask?
[27:19] So at the moment, I am not working on PIVX at the moment. Actually, I shouldn't be working at all at the moment, because it is like an exam,
[27:33] we have like an exam at university. Okay, so you're in school.
[27:38] I'm focusing on exams right now. Okay, and what are you studying in school, if you don't mind me asking?
[27:45] Yeah, I study physics. Okay, nice. So programming is somewhat of a side thing to your vocational?
[27:55] At the moment, it's like a hobby for me. So something I do on my free time. But of course, when I finish with university, I could like decide to work full time on it.
[28:10] I still don't know, I mean. Right. Yeah, yeah, yeah.
[28:16] So I mean, C++ doesn't sound like the easiest side project thing to me. What, how long have you been doing development in general?
[28:26] And what's, yeah, how long have you been doing development? Is this something that you're just picking up?
[28:32] Or have you been doing C++ development for, you know, since you were 16 kind of thing like pasta?
[28:38] Like development in general, I've been doing it for like five or six years. Because yeah, at university, we learn something about programming.
[28:52] Yeah, yeah, that's kind of how I got into it as well. I studied mechanical engineering, a little bit of physics.
[29:01] And every engineering, you have to do some kind of programming. So yeah, I know exactly what you're talking about.
[29:08] It does kind of pull you in like, wow, this is interesting stuff. All right, so do you want to talk a little bit about the masternode payout?
[29:21] Or not the masternode payouts, but the trustless masternode shares at all? Or is it too early to talk about that?
[29:29] Have you done on that one? I think I have some ideas, but it's just some,
[29:45] I think some theoretical ideas, because I haven't really tried to implement because due to the lot of stuff that needs to be done before.
[29:57] May I ask what some of those theoretical ideas are? That's it's more than I have, so I'd be happy to hear it.
[30:07] Like, I was thinking of a way to have on, to implement the feature, like making a new special transaction, what to put inside, like the, like, of course,
[30:33] Maybe a little too theoretical? Yeah, it's a bit early thing to actually say.
[30:46] Yeah, I mean, no shame there. There's people been talking about trustless masternode shares for a decade here.
[30:55] So nobody's really prioritized it, at least, or done much on it. So, yeah, there are people that have done non-trustless masternode shares.
[31:08] And I think that that's working for quite a bit of people. So I mean, non-trustless is not, I mean, you have to trust someone and.
[31:16] That's not the point. Yeah.
[31:20] So the other thing that I wanted to know from you is just more of your general interest in cryptocurrency, I'm always interested in, in what draws people into the cryptocurrency.
[31:33] To me, there are people fall into one of three buckets, if not all buckets, or, you know, you can, you can be in multiple buckets.
[31:42] But the way that I see it, there's, there are people that are interested from the ethics side of it, where it's, it's just, they think that this is something that the world needs.
[31:54] And a lot of the things that we talk about in the why we build section, talk about the fact that we need privacy, and we need payments that are not controlled by big corporations,
[32:08] or governments and things like that. So that's, that's all on the ethical side.
[32:13] And then there are people that are in the economic side, where either you want the number to go up, like you're just you want to make a bunch of money, or you think that our traditional
[32:25] economic systems are suffering because of inflation, all those kind of things, all those kind of economic issues.
[32:32] And then there are people that are more interested in on the engineering side. So I call them the three E's, the ethics, economics and engineering.
[32:41] So where would you place yourself? And what's your overall interest in cryptocurrency?
[32:47] Yeah, so my main interest is surely on the technology side. Okay, so like, I'm, I really like how the abstract cryptography, like elliptic curves,
[33:00] number theory, and so on, can, can like meet the real application like cryptocurrency. But like, it's, it's, because usually, when you have like abstract, abstract math, math,
[33:20] it like stays here, far from reality. And like, it's, okay, researchers studies it.
[33:27] But it's really rare to have like, something which is also advanced, like cryptography, some of advanced topic of cryptography, which are actually applied in real life.
[33:39] So that's, for me, the main reason that I like crypto. But of course, also the economic side.
[33:46] Yeah, when, when crypto goes up, it's always good. Yeah.
[33:52] It's like the weather, right? It's like, everybody can talk about the weather, everybody can talk about the number going up.
[33:58] Everybody's interested in that. So and right now, Dash is, is doing better than it's been doing recently.
[34:06] So we're back up over $31, which is nice. That's us, of course.
[34:10] So, yeah, I mean, it's, I, what I love is that you just kind of jumped into things. And you didn't, like, I didn't recruit you.
[34:21] I don't think any of our, our strategists recruited you. Like you said, you just, you saw an opportunity.
[34:27] You have a friend that pointed you to this, and then you took some action. So I want to see more of that.
[34:33] And I'm looking forward to working more with you. Amanda, did you have anything, any other questions that you wanted to ask Alessandro?
[34:41] Or? I did have one final question.
[34:44] Yeah. So it's, Alessandro, it sounds like you're maybe already considering going full-time
[34:50] crypto development after you have graduated university. So I'm wondering, do you find that your physics studies contribute much to your crypto programming?
[35:04] Or do you just want to complete your studies, like, maybe to please your mother? Or for some similar reason, out of curiosity?
[35:15] Like, yeah, so in physics, we do a lot of math, of course. But it is, it is like different from the one that we use in crypto.
[35:27] Because like, crypto is more number theory, cryptography, elliptic curves, and so on. Physics is more like integrals.
[35:40] And yeah, it's more like, how do we say it? It's more like analysis, calculus, and so on.
[35:55] Yeah, while crypto, while crypto are more number theory and group theory. So.
[36:03] Okay. So yeah, I'm, I will finish my study because, of course, it's my last year.
[36:11] So no point in quitting at the end. Yeah, so when do your study, when are your final exams?
[36:18] So that we can get more of your time and attention at that point. Because we don't want to interrupt that.
[36:25] I know what it feels like to be at the end of something. You just want to focus on that one thing.
[36:30] And then you can, I'm a very linear, do one thing and then move on to the next after that. So when can we expect that?
[36:38] Sorry, when? Yeah, when are your exams done?
[36:44] Oh, like in, I have like two exams left and the master thesis. So I'm really, really close, I think.
[36:54] Okay, well, good luck. And so does that answer Halawi's question?
[36:58] Is a master's thesis, is that for a graduate program? Yeah, master thesis.
[37:02] Yeah, okay. Right on.
[37:05] All right. Well, thanks for sharing the work you've been doing on the show today, Alessandro.
[37:11] And that's it for us. Everybody, we'll see you next week.
[37:14] See you, everybody. Thanks, Alessandro.

