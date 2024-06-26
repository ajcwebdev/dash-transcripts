---
showLink: "https://www.youtube.com/watch?v=zZaSU5RylYU"
slug: "pseudonymous-work-crowdnode-privacy"
title: "Pros & Cons of Pseudonymous Work + Enhanced CrowdNode Privacy"
publishDate: "2023-02-27"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/zZaSU5RylYU/maxresdefault.webp"
---

Jojobyte discusses the benefits and challenges of working pseudonymously as a Dash developer and demonstrates a new privacy-focused user interface for staking Dash via CrowdNode.

## Episode Summary

tl;dr: In this episode, pseudonymous Dash developer Jojobyte joins the hosts to discuss the pros and cons of working pseudonymously in the cryptocurrency space. They explore the importance of privacy in an increasingly AI-driven world and the trade-offs between anonymity and building trust. Jojo also demonstrates a new privacy-focused user interface for staking Dash via CrowdNode, which aims to streamline the staking process without requiring personal information. The discussion touches on the technical aspects of the project, its funding through the Dash Incubator, and the potential future improvements.

## Chapters

00:00 - Introduction and discussion on the importance of building projects
The episode begins with a thought-provoking intro discussing the significance of creating and sharing projects in the cryptocurrency space.

04:22 - Introducing Jojobyte and his background
Jojobyte shares his experience as a web developer and his involvement with the Dash community and the Dash Incubator project.

08:17 - Benefits and challenges of pseudonymity vs. public identity
The discussion delves into the trade-offs between maintaining privacy and building trust, as well as the possibility of having both pseudonymous and public-facing profiles.

19:04 - Overview of the current CrowdNode staking process
The hosts provide context for the current staking process on CrowdNode and the potential improvements that Jojo's project aims to address.

23:27 - Demonstration of privacy-focused CrowdNode user interface
Jojo walks through a new user interface for staking Dash via CrowdNode, which utilizes the CrowdNode API and an SDK developed by the Dash Incubator team to enhance user privacy.

30:56 - Technical discussion on the project's development
The hosts and guest discuss the choice of using vanilla JavaScript for the project, the benefits of a reference application, and the interaction with the CrowdNode API.

37:11 - Future improvements and trustless staking
The conversation touches on the potential for integrating CrowdNode's trustless staking solution and the importance of having a streamlined process for users.

40:01 - Closing thoughts and upcoming opportunities for community involvement
The hosts and guest wrap up the discussion, mentioning potential bounties for testing and providing feedback on the project.

## Transcript

[00:00] (upbeat music) - Just to let you know where I stand
[00:15] right from the very top, for me, freedom means your right as an individual
[00:19] to be the person that God, or the universe, intended you to be.
[00:24] Beyond culture, beyond religious orthodoxy, beyond race, your right to be you,
[00:29] your right to your freedom. Not your right to tell other people what to do,
[00:32] from whatever perspective. And I believe in your freedom of expression,
[00:35] whether that's on the right or the left. As long as your freedom of expression
[00:38] doesn't involve oppressing others, I believe in your freedom.
[00:42] (upbeat music) - None of this is by accident.
[00:48] Pay attention. Today, collectively, World Central Banks
[00:50] are deliberately pushing the entire world financial system off of a cliff.
[00:55] Obviously, the people with it, and intentionally crushing the consumer,
[00:58] while at the same time, pushing the world ever closer to global war.
[01:01] The world's population today is in the middle of an intentionally created
[01:06] environment of rising inflation, a situation which in no way is gonna get any better,
[01:10] despite transitory, temporary, peaking, and freaking sticking.
[01:14] All right? And with that, the world economy itself
[01:17] is contracting at its fastest pace ever. (upbeat music)
[01:24] - Obviously, they're simply exploiting an opportunity to continue with their agenda as they have always done.
[01:30] I believe the issues that they're pretending to care about are important issues.
[01:35] And if these issues were correctly addressed, along with all inequality,
[01:38] most notably economic inequality, you would see real change in society.
[01:42] Real change in society means diminishing the potential for the powerful to continue
[01:48] to operate within systems that always prefer their desired outcomes.
[01:52] That change can never be allowed. The system will always happily make gestures.
[01:55] The system will always happily fund jamborees and galas that don't change anything
[02:00] and provide opportunities for Walmart. What we need is legitimate change,
[02:03] legitimate alliance, legitimate care and love that looks beyond identity and cares truly
[02:09] and authentically about all of our freedom. (upbeat music)
[02:14] - Do you feel like you have representation? Honestly, we have no representation anymore.
[02:19] Your votes don't count. We have no representation anymore.
[02:22] This whole thing has been taken over by a corrupt, twisted organization
[02:28] who's hell-bent on controlling the entire world. And we're talking about central banks collectively.
[02:33] Where's the outrage? Where's the uproar?
[02:35] People, remember what I'm telling you. You and me, we are the resistance.
[02:40] We raise our awareness. We get this stuff out there.
[02:42] We educate ourselves. We understand how the system works.
[02:45] We know who the players are. We can't lose, but we gotta get more people involved.
[02:49] The takeaway is this. Expect war to greatly expand.
[02:53] Expect the world's economy to contract much faster. Expect inflation to get a lot worse.
[02:59] Expect global debt to hyper-balloon. Expect job losses to skyrocket.
[03:04] And expect a major false flag event to occur with many people, maybe even some of you, maybe me,
[03:14] losing our lives just so they can get the general population to back another war.
[03:24] (upbeat music) So when people talk about the freedom is a dubious term,
[03:30] what they're attempting to do is prevent galvanization, prevent people coming together of all races,
[03:35] of all colors, with a wide range of interests, but all ultimately could sit within the framework
[03:39] of a popular movement where we all enjoy more freedom, where we all enjoy more access to resources,
[03:44] and more importantly, democracy. Sometimes life does involve suffering.
[03:47] Sometimes life does involve sacrifice. But what it needn't be about is increasing centralization,
[03:53] increasing institutional power, increasing surveillance and digital IDs,
[03:57] increasing bigotry and hatred of people of all hues and colors,
[04:00] turning people against one another in order to simply ensure that systems
[04:03] can continue to operate as they currently do for maximum profit and power without any concern
[04:08] for the impact it might have on you. (upbeat music)
[04:12] (upbeat music) (upbeat music)
[04:17] (upbeat music) (upbeat music)
[04:22] (upbeat music) - Hello, and welcome to Incubator Weekly.
[04:27] Today, I'm joined as always by Rion, and also our guest today is Dash developer, Jojobyte.
[04:35] Jojo, how are you today? - I'm doing pretty well, thanks for asking.
[04:39] How are you guys? - Great.
[04:43] - I'm well also. Well, we are going to start today's episode
[04:49] with introducing Jojobyte to you. We'll then move into a discussion
[04:55] for which he is uniquely suited to comment, and for which we hope to also receive your comments
[05:00] in the live chat, which is, what are the pros and cons of working pseudonymously?
[05:06] And then finally, we are going to show you a Incubator funded project that Jojo has been working on,
[05:16] which is an alternative interface for staking via Crowdnode,
[05:21] one which enhances privacy, I'm told. So we'll get to all that later.
[05:25] So to start, Jojo, please, will you tell us a bit about, I don't know, I guess about your professional background
[05:33] as a software developer? - Sure, I've been developing websites
[05:39] for a long time, I think near 20 years now. And I guess I've done a little,
[05:48] well, I used to do a lot of PHP, but mostly now I do a lot of JavaScript,
[05:54] both on the server and front-end. And I've done some React projects, I've done Vue.
[06:02] Yeah, I've bounced around front-end frameworks and all sorts of stuff like that.
[06:07] And now I've been doing a lot of vanilla JS type of projects where I'm hand-coding everything
[06:15] and not basing it on any frameworks, so yeah. - Okay, well, I'm sure to a lot of people
[06:22] that made a lot of sense. Will you tell us then what,
[06:27] first of all, how did you even hear of Dash? And then how did you hear of the Incubator in particular?
[06:36] - I heard of Dash years ago, just being semi-interested in cryptocurrency.
[06:43] It was popular enough, I had heard of it, but I hadn't done much with it.
[06:47] And then through a bizarre course of interactions, I ended up meeting CoolAJ86,
[07:00] and he was on the show last week. And he has been involved with the Dash Incubator
[07:06] and kind of got me involved, so yeah. - Wow.
[07:11] - Although you met and knew him from a long time before last week.
[07:16] - Did I say last week? Yeah, he was on the show last week.
[07:20] - No, you said that, but I didn't know if it was clear to other people.
[07:24] It's clear to me, 'cause I've worked with you for several months now.
[07:28] And yeah, but you've gone back with AJ quite a lot longer than that, so yeah.
[07:37] - So you met AJ in person then, Jojo? - Yeah, many times now, so yes.
[07:43] - Okay, so this kind of segues to our discussion of today, which is what are the pros and cons?
[07:52] Why have you chosen to work pseudonymously? And then what cons do you feel
[07:58] have come about as a result of that? And this is an especially nuanced discussion
[08:03] because it sounds like, correct me if I'm wrong, but it sounds like you met AJ in person.
[08:07] - Correct. - Yeah, so that's wild.
[08:11] - And we've met in person as well. So he's kind of straddling the line, I guess,
[08:17] between pseudonymy and whatever the opposite of that is. - So start by telling us, why did you choose to,
[08:25] at least when it comes to worldwide web-based appearances, such as this and an incubator work and whatnot,
[08:31] why did you choose to be pseudonymous, Jojo? - Hmm, I suppose there's,
[08:39] it's really just that once you put something out on the internet, you have no guarantee
[08:46] you can ever get it back. And I think actually cryptocurrency
[08:51] got me started thinking about this. Like once you've put something there,
[08:57] like it could be on a blockchain and you have no guarantee of it ever being deleted.
[09:02] And so you kind of have to really think about, am I okay if this never goes away?
[09:09] And in the other sense, I mean, we're now in the AI era and it's like, well, there's deep fakes.
[09:17] The more stuff you're putting out there, people could deep fake you.
[09:20] It might not be good enough to fool people close to you, but maybe it could.
[09:26] You don't know how bad things will get and things seem to be getting worse in that regard.
[09:33] And yeah, so maintaining your privacy as best you can, that's what I'm trying to do.
[09:40] But I also think privacy is for, I mean, privacy is for everything,
[09:45] but especially what I'm putting out on the internet, like that's, I'm more careful with that
[09:52] than people I know in person, like I know them in person. They already know me, they know I exist.
[09:59] But as far as the internet, like I could be an AI right now. I could be typing this into a chat program, so.
[10:07] - I'm starting to wish that I hadn't gone public. Those are really compelling arguments, Jojo.
[10:16] - Thank you. - Too late now. - And to be fair, well, Jojobytes got a voice, obviously,
[10:23] and I won't be the one to say if that's, so like his real voice or not.
[10:29] But if, so that's kind of straddling the line too, because I just feel like with the world going the way it is,
[10:37] you have, it's so difficult to remain private and anonymous or pseudonymous.
[10:46] If you can, if you've got your voice out there attached to your name, your real identity somewhere,
[10:54] you gotta believe that somewhere in some database, there's a record of this is this person's name,
[11:01] this is this person's voice. So I kind of like, that's one of the reasons why I'm not,
[11:07] and it's just one of the reasons, but I just feel like they're,
[11:12] the people that I care to be private from, they're going to find out whether,
[11:19] no matter what I do, pretty much. So I'd rather just be upfront with it and say,
[11:23] here I am, this is what I do, and just let the consequence follow that,
[11:31] and whatever those consequences may be. But one of the reasons why I wanted to talk about this
[11:36] was it's becoming increasingly scary, I guess you could say, for lack of a better term.
[11:43] You've got the developer of Tornado Cache rotting in a jail cell right now for no reason
[11:52] other than he wrote some code. And I don't know the particulars of that case,
[11:57] but that's definitely one reason to try to keep your privacy.
[12:02] And I know that there are a lot of developers in Dash that are anonymous, pseudonymous,
[12:10] and I can't blame them for that. And it might be me that's naive thinking
[12:18] that everything's going to be just fine, and I can be out here with my real identity and not worry.
[12:26] I do worry about it a little bit, but on the other hand, I've just made the decision
[12:31] that I'm not doing anything wrong. In fact, I'm doing everything right
[12:36] as far as what I'm doing for a living, trying to move forward the cryptocurrency cause,
[12:42] because to me, it's the most important thing that we can be doing right now
[12:47] is fixing the world monetary system. The intro, some of you may have noticed,
[12:54] was a little more intense this week. That was by design and by choice.
[13:00] I think the stakes are very high in cryptocurrency, both on the pro side and on the con side.
[13:06] Like you could end up like that developer of Tornado Cache just for developing something that gives people privacy.
[13:15] You could end up in a jail right now. On the other hand, you could be a total hero,
[13:22] and you are a total hero if you can further this cause, because the stakes are high on the opposite end too.
[13:30] Like we're witnessing in our lifetime a major crackdown on human rights,
[13:37] and that's unacceptable to me. And that's why we kind of have this intro section
[13:42] about why we build. It's a little bit personal for me.
[13:45] Granted, like I curate these clips every week for the past three weeks so far.
[13:50] And so I'm choosing what inspires me and motivates me, but I'm also open to having other people
[13:58] share clips that they find that are the reasons that they're building.
[14:03] It might be anything from, I just find this to be fun. You know, I like developing,
[14:08] and it's not a big thing for me. Like I'm not trying to save the world,
[14:12] but I just think it's fun, and it's really interesting tech.
[14:15] That's great. But for me, it's something much bigger.
[14:18] - And I guess there's maybe room to discuss a third option here
[14:24] between the pseudonymity versus public facing, which is the ability to have different identities,
[14:32] so to speak, online, different profiles, which is to say that, you know,
[14:36] hey, if I see an advantage for myself because, you know, I have a nice beard,
[14:41] I have nice hair and nice manly, you know, baritone voice. - Are you describing me?
[14:47] I'm just kidding. - And I can, you know, command a certain amount of attention
[14:53] or benefit via having that profile. Well, there is no preventing one
[15:00] from at the same time having, you know, a coding profile that, like Jojo's, is pseudonymous,
[15:08] that, you know, does stuff that the public face does not do.
[15:12] I mean, how feasible an option is that? - Well, I'm sure Jojo might have something to say to this,
[15:20] but I'll jump in real quick. There's a pretty good chance
[15:24] that I have maybe interacted with and even paid out some bounties to AIs for all I know.
[15:31] There's one in particular that I'm fairly convinced that it's an AI, or not fairly convinced,
[15:39] but I wouldn't be surprised if it turned out to be. And, you know, the work was somewhat questionable,
[15:46] but it was also somewhat valuable. So it doesn't really matter in terms of, you know,
[15:52] I don't need to know your identity to see if you're producing valuable work.
[15:56] But on the other hand, I just, you're not, I'm going to be leaning more towards funding
[16:08] and interacting with and spending time with to get to know real people that I know are real people
[16:15] and that are, you know, showing their true identity. That's just me personally.
[16:22] It's with the upcoming AI thing, it's going to be a little crazy.
[16:28] You might be spending a lot of time just dealing with random code, and that's scary to me.
[16:38] I don't know exactly why, but sometimes it can be a waste of time.
[16:44] So, but if I know that I can sit across the table from someone, like Jojobyte,
[16:48] I have sat across the table from him, that makes me feel like, okay,
[16:53] that's, there's more potential here. - Yeah.
[16:58] Well, I, this is probably, you know, an appropriate time for me to say
[17:03] that completely coincidentally, my husband and I were planning to return later this year
[17:13] to spend most of our time in an area that is not that far from Rion.
[17:20] And I guess from the sounds of it, probably not that far from Jojobyte or AJ.
[17:25] And so that's something that I really look forward to as well, Rion, which is just sitting across the table,
[17:30] the table from people who I, with whom I can speak. And, you know, in the case of Jojo,
[17:36] sitting across the table with someone, you know, like, "Hey, it was great talking to you online."
[17:40] And, "Oh, how much better to meet you in person now." Because as much work as we can accomplish online,
[17:47] and as we all have accomplished online together over the years, I don't know if I speak for many others
[17:54] when I say this, but shoot, you know, sometimes staring at a screen gets a little lonely
[17:59] and how nice would it be to, you know, sit down and share a meal or, you know,
[18:03] have drinks or coffee or whatever. And so that's something that I really look forward to
[18:08] and hope that within the DASH community, we can have more of in the future.
[18:12] You know, whether it's little hubs, just here and there, here and there.
[18:15] In this case, we're talking about the Northern Utah area or, you know, what have you, because I see the,
[18:24] as you've mentioned, Jojo and Rion, there's benefit to both. There's benefit to the online pseudonymous stuff,
[18:30] hell, to even paying out AIs for work contributed. And then there's also value to, you know,
[18:36] meeting up for a drink, shaking hands, and enjoying each other's company that way.
[18:41] - Yeah, and I think that's how adoption grows anyway. Your local scene is where to concentrate, personally.
[18:49] - Well, if we don't have any additional comments from the viewers on that topic,
[18:57] I think that now would be the perfect time for us to shift to today's software demo.
[19:04] And so to start out, I know you had mentioned, Rion, that we wanna make sure we have
[19:09] some common understanding of terms. But before we even move into our common understanding
[19:16] of terms, I wanna say first, I know that I myself don't understand the A/B contrast
[19:24] between what you're gonna show us today, Jojo, and what is currently the option.
[19:29] So Jojo, will you explain to us what is the current setup that crowdnode.io
[19:37] has going on for people who want to log on and stake any amount of Dash, you know, starting at one Dash,
[19:44] and why is it that it can be improved upon from a privacy standpoint?
[19:48] - Sure. Currently, at least as far as I'm aware,
[19:53] you have to provide an email address to sign up. And then I believe you might have to verify
[20:00] some sort of other identifying factors to be able to deposit into,
[20:08] well, I think you can deposit there, but you can't stake the money you deposit there
[20:14] until you've kind of identified yourself and verified you're a real person.
[20:20] - Actually, that's not the case. Crowdnode is a fairly private platform as it is,
[20:30] but you do have to provide an email address and a password. And I think that their authentication system,
[20:39] actually, the person who got this project started in the first place was coolage86.
[20:45] And I think I remember him saying something to the effect that the authentication system uses
[20:54] some kind of large company behind it. And that was part of the motivation.
[20:59] But another part of the motivation was, you know, Crowdnode puts out an API for a reason.
[21:06] And that reason is they want other people to be able to interact with their service,
[21:12] other applications to interact with your service. There's no other reason to put out an API.
[21:16] So we wanted to also have an implementation or a reference application for using that API.
[21:26] So we made an SDK first, which is an SDK, yeah, software development kit,
[21:34] is basically just a package of code that you import into your code and use those functions.
[21:42] And it makes it a lot easier to use those functions. And then you can put on top of that,
[21:49] you can use those functions in different interfaces. So the first interface that we did
[21:54] was a command line interface, which AJ did. And now we are putting a user interface on it,
[22:03] a graphical user interface on it, which is what Jojobyte has been working on.
[22:08] So rounding that all out, this is essentially a reference application
[22:16] to using both Crowdnode's native API and our incubator SDK for Crowdnode.
[22:25] And just so everybody's clear, we're not part of the Crowdnode team,
[22:29] we're the incubator, the Dash incubator, but we want to support that project.
[22:33] It's the project that I find has the most, has the best product market fit
[22:40] that I've seen in cryptocurrency. People want to save right now
[22:44] and they want to get a yield on their savings. And they're not finding that in fiat currencies,
[22:52] national currencies and cryptocurrencies. That's one of the biggest use cases right now
[22:57] is just saving and earning a yield on your savings. And we can't reject that.
[23:03] Like as much as we want Dash to be used in payments and day-to-day transactions,
[23:11] the reality is most people want to just save and earn both a yield and appreciation on their Dash.
[23:20] So we want to help serve that use case. - Okay, so I think I'm probably going to get a better idea
[23:26] of what's on offer here if we just start the walkthrough. So Jojo, may I bring it up the screen share?
[23:34] - Yeah, sure. - So let's just take it away.
[23:39] And if I have, or if anyone else has a question, we'll just pop in.
[23:43] - All right. So right now this Crowdnode.js UI
[23:49] is implementing several other, it's implementing both the SDK Rion just mentioned,
[23:56] but also several other projects that Kool-Aid J86 has worked on
[24:00] to generate the recovery phrases and various private public key pairs,
[24:09] which that's Dash HD and several other things connected to it.
[24:14] And so this is the first screen you land on right now. And you're given the opportunity
[24:20] to either add a pre-existing recovery phrase or a WIF, which is a private key that is not as memorable
[24:30] but it still works with this, or you can generate a new one.
[24:33] So I'm going to go ahead and generate. - This WIF is wallet import format
[24:38] for anyone that's wondering. It's just the private key in a wallet import format.
[24:43] - And Jojo, when you say that we land on this page, does that mean that as a new user,
[24:48] we've just navigated to a specific URL and this is what we see or how do we land here?
[24:53] - Yes, it's not fully deployed yet, but when you go to the website
[24:57] that will be deployed very soon, you would land on something like this.
[25:02] So you'd get to the website and you'd see something like this
[25:06] if you have no wallets already saved, but which in this case, I have nothing saved yet.
[25:14] So I'm going to go ahead and generate a wallet and this will use the tooling that Coolio J86 has built
[25:21] to generate a new recovery phrase and a new public address. And I can now interact with this
[25:29] just like any other dash address or a wallet. And so one of the first things you kind of need to do
[25:37] is deposit some funds. And so I will go ahead and deposit.
[25:43] - We should make somebody else deposit. I'm just kidding.
[25:49] - Who hosts this web server and how is the cost covered? Rion, you want to answer that?
[25:58] - Well, right now it's just on local host, I believe, but we will be like incubator
[26:05] will cover the cost of hosting the URL when that comes. - And then let's go to a PME's question who says,
[26:17] can you back up a bit from where you all are and describe a bit about the structure of Dash?
[26:22] How are payouts to stakeholders possible? Is this common to all cryptocurrencies?
[26:26] Ooh, that's a big one. That's a real big one.
[26:28] - Payouts, let's put that question back up on the screen if you could, Pete.
[26:33] The structure of Dash is that Dash is a DAO, meaning that it's a decentralized autonomous organization.
[26:43] That's just the fancy term that we use for it now, but basically you can put proposals to the network
[26:50] that you want to receive some funding from the Dash Block reward.
[26:55] And if the Dash Block, if the stakeholders, which is in our case, the masternode owners,
[27:02] vote with sufficient voting that they want to pay you out, then you get paid from newly minted Dash
[27:09] from the Dash Blockchain once a month. And that's how Dash Incubator is funded.
[27:13] And then we further divvy that Dash up to different projects that we find value with,
[27:20] including this project. So that's like really quick zoom out
[27:24] and then zoom back into what we're doing. How are payouts to stakeholders possible?
[27:29] I think I might've answered that question. Is it common to all cryptocurrencies?
[27:34] Definitely not. Dash is one of the only cryptocurrencies that does this.
[27:38] In fact, it might be the only cryptocurrency that does something like this on the layer of blockchain,
[27:45] natively to the original blockchain. There are other, there are a ton of different DAOs
[27:52] in different ecosystems, Ethereum, whatnot, that have DAOs as tokens, token projects,
[28:00] outside of and on top of their layer one cryptocurrency blockchain, but-
[28:06] And so they're not able to use it to govern or incentivize any of the layer one-
[28:10] It's not Ethereum itself, yes. Yeah.
[28:14] Thank you for the question, Viola. Let us get back to where we were in our demo.
[28:21] Okay. Please pick it back up for us, Jojo.
[28:27] All right. Let's see here.
[28:30] So I just managed to fund the address. Oh, we missed the best part.
[28:38] That's okay. My apologies.
[28:42] I guess I could fund another one. How about I do that?
[28:45] Because I was going to add another one from the recovery phrase.
[28:49] So this should add another one. It has a zero balance.
[28:53] So I can come in here. Let's see.
[29:03] So if you do deposit, you can copy that address. (keyboard clicking)
[29:11] And in a moment here, it should close out. See.
[29:24] So that's sent. There we go.
[29:29] So it just funded. So now both of the wallets have funding in them.
[29:35] These are separate recovery phrases. So they are individual.
[29:40] If you go into staking, then you're able to interact with these funds.
[29:45] You need some funds in the wallet to be able to sign up for CrowdNode.
[29:52] So these are the same ones from the other wallet page. So staking and wallet are relatively similar
[29:58] just for different purposes. So I'm going to click sign up on the first one.
[30:04] And this, I just made this up. We might want to change the wording here,
[30:10] but you have to click accept. - And I accept the CrowdNode.
[30:14] - Yeah. And then this just takes a little while.
[30:20] So. - So you'll notice that there's no username,
[30:24] no email, no password, nothing like that in this. - So while the signup is taking place,
[30:31] let us check out TL's question. First of all, thanks.
[30:37] We're glad you think it's an awesome show. Secondly, he says interface looks great.
[30:41] What are your thoughts about using vanilla JS versus a framework like React or Vue?
[30:47] Let's start with that question. Oh, I'm sorry.
[30:49] I guess it's the same question. Is it to reduce dependencies?
[30:52] And what about longer developer time? - I'll give a first answer to that question
[30:56] because we decided this mutually, Jojo, Biden and me. But the reason that I wanted to do it this way
[31:03] is because I want to have a reference application that any JavaScript developer,
[31:10] well, should be able to look at and say, okay, I understand exactly how this works
[31:15] 'cause I understand JavaScript. If we had made the reference application in React,
[31:20] somebody like a Vue developer might look at it and be like, I don't know React.
[31:23] This doesn't help me. So we wanted to, in my opinion,
[31:27] Jojobyte will object to this. But in my opinion, using vanilla JS
[31:34] is a little bit less efficient, but I wanted to do it this way for that reason
[31:39] so that any JavaScript developer can understand what's going on here.
[31:42] - I don't object to that, by the way. It is less efficient in many ways.
[31:48] - Yeah, it's like churning your own butter. - Yeah.
[31:52] - You can either go to the store and get the butter that professionals have put together in a nice, easy way,
[31:57] or you can churn your own butter and it might taste better and you understand exactly
[32:02] what the process was getting into it. But yeah, it's kind of the same idea.
[32:06] It takes a lot longer. But I think it was useful in this case.
[32:10] And just so everybody knows, the signup for Crowdnode, what it's actually doing
[32:14] is it's implementing the blockchain API that Crowdnode has, which uses on-chain-payments as the API.
[32:21] It's something that you'll probably very rarely see anywhere else.
[32:26] So instead of doing a REST API call and getting an API key and everything like that
[32:31] from Crowdnode, it's completely permissionless, it's completely private.
[32:35] All you have to do is send a certain amount of funds with the exact amount that the API requires,
[32:43] and that's what's doing the signup for you. And it's registering your address in their backend
[32:49] and saying, okay, whenever I receive funds from this address, now I know that that's going
[32:54] to this account. So that's what the signup is doing,
[32:57] and that's why you had to pay some DASH to do that. - Which is why it's showing here
[33:03] that there's this amount staked. It's not enough to actually start earning interest,
[33:09] but it used funds to basically trigger the signup process. - And so this is complete, this is all someone
[33:19] would have needed to have done to get started. - Yeah, this address is now signed up,
[33:24] this top one is not. So the bottom one is now signed up,
[33:28] and I can either send more funds or unstake the funds that are there.
[33:33] So I can go ahead and click this, and I've got, I guess I should show this,
[33:40] I've got 0.003 balance left. And so I'm gonna just send 0.0015,
[33:49] because to unstake also requires funds. So let's see.
[33:56] - Sinbit7 asks, "Wasn't a half a DASH "the minimum to stake through CrowdNote?"
[34:01] - To start earning interest, yes, but in this process, you can send these funds,
[34:08] you won't start earning interest until you reach that minimum, as far as I understand, but.
[34:13] - I see, so it acts as a savings account until you get to the minimum threshold.
[34:18] - Yeah, well, yeah, I think so. I'm not an expert on CrowdNote,
[34:24] I'm an expert on building this, I guess. So now we've got that much in our CrowdNote account,
[34:33] it might not be technically staked because it won't earn interest,
[34:37] but that's in the account, and it would go towards that staking amount
[34:40] for this address. And so I can also unstake the funds,
[34:47] and this is done by percentage. This is based on the SDK that CoolAJ86 made,
[34:54] and so I'm just gonna go ahead and unstake all of it, actually.
[34:59] - And I think that that percentage, I think it was percentage in the API as well,
[35:07] which is why it trickled down to the SDK, and now the UI. So, API designers out there,
[35:14] just know that your choice of API is potentially going to trickle
[35:19] all the way down to your users. - And so is it a, would it be safe to say
[35:25] that this API is not currently compatible with CrowdNote's trustless staking solution
[35:33] that starts at a minimum of 100 dash? - Yes, that is true.
[35:37] As soon as CrowdNote gives us, gives the community an API to work with
[35:47] for the trustless version, we will implement that API.
[35:52] We'll enhance the SDK with those API endpoints, and we'll be able to make that trustless process
[36:02] much smoother than it is right now by automating some of the signing,
[36:08] which is a lot of the other tooling that CoolAJ86 has made.
[36:13] We can, we have that signing functionality in JavaScript tooling already,
[36:21] so we can update the SDK, the CLI, the graphical user interface,
[36:27] all of that as soon as we get an API for the trustless part. So, please badger them, pester them,
[36:36] encourage them, whatever you can do to get that as a priority for them.
[36:41] That would be great, 'cause I think that we have seen some,
[36:46] I think we have four trustless nodes now, but if the process were a lot more streamlined,
[36:53] I think it would be much, much higher. And I think there are a lot of people
[36:58] that are probably waiting on the sidelines, like myself, that are waiting for that trustless API
[37:05] to make the smooth process before they'll even join, so. - Yeah, I would love that myself.
[37:11] - Is there anything else for us to see on this demo, Jojo? - Sure, I mean, it's just withdrawing the funds,
[37:19] but actually I'll use this as an example. I can send all of the funds to the other address.
[37:27] So now my entire balance is there. - So as you can see, this is,
[37:36] we went a little bit above and beyond what was strictly required,
[37:40] because we could have actually implemented CrowdNode and put a UI on top of that,
[37:49] on top of their functions without having an in-browser wallet,
[37:54] but we do take that extra step so that you can actually send funds to the application,
[38:00] which stores it in your browser storage, encrypted, and then you can kind of manage funds in a browser wallet
[38:09] in addition to managing funds on the CrowdNode side. So there's a two-step process.
[38:14] You send funds to the browser wallet that's displayed here, and then you can also then stake that into CrowdNode,
[38:21] so it can then go from the wallet in your browser to CrowdNode, and before I forget,
[38:27] this is not, I don't think it's deployed yet anyways, but it's not ready for anybody
[38:35] to be putting money through at this point. We still need to test it.
[38:40] - Okay. - Correct.
[38:44] - Okay, is there anything else for us to see on this demo? I saw you had just encrypted the wallet, righteous,
[38:49] and do you have-- - Correct. - Okay.
[38:51] - So this just encrypts the data that's stored in your browser.
[38:55] So if you're using a shared computer or something, that will just make it a little more secure
[38:59] so your keys can't be directly copied, and it will also decrypt them, so.
[39:05] And right now, we're just using emojis, but I would like to get these icons updated
[39:10] with some real icons, but now these are unlocked again and useful.
[39:15] - I did like the stake icon, though, if you ever thought to leave that one in,
[39:19] I wouldn't mind that, yeah. - And the takeout?
[39:22] - That's fine too. Okay.
[39:26] - Okay. So, okay, well, I think, Rion,
[39:31] does that cover everything we wanted to see here? - Yeah, I think so.
[39:35] We'll probably be opening up some bounties for testing this, giving feedback,
[39:39] user experience feedback as well as technical feedback, so be on the lookout for that.
[39:47] - Very good. Well, Jojo, it was sure a pleasure having you on today.
[39:52] So I will join Lavi and Bloch by saying good day to you,
[39:56] and we look forward to maybe touching base about this project again in the future.
[40:01] - Awesome, thank you. Thanks for having me on.
[40:06] - Definitely. And, oh, I guess we can get one last question here.
[40:10] What about the benefits of pseudonymous work if the Dash price appreciates significantly?
[40:15] Just a thought. - Yeah.
[40:18] Yep, and you never want to be telling people what your holdings are anyway,
[40:24] so that shouldn't be a problem even if you're not pseudonymous,
[40:27] but keep your funds private. - Righteous.
[40:34] Okay, very good. We were just pleased to talk with you this week, everyone,
[40:39] and we'll be pleased to see you again next week at the same time, the same place.
[40:44] Goodbye. - Bye, everyone.