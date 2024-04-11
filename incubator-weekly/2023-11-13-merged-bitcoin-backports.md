---
showLink: "https://www.youtube.com/watch?v=y5g844y0vuY"
slug: "merged-bitcoin-backports"
title: "Merged Bitcoin Backports"
publishDate: "2023-11-13"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/y5g844y0vuY/maxresdefault.webp"
---

Vijay discusses his experience with Dash, Bitcoin backports, and the state of crypto in India.

## Episode Summary

tl;dr: Vijay, a software developer with 16 years of experience, shares his journey with Dash and his contributions through Bitcoin backports. He explains the process of selecting and customizing Bitcoin changes to integrate into Dash. The discussion also touches on the perception and legal status of cryptocurrencies in India, as well as Vijay's interest in further contributing to the Dash project.

## Chapters

00:00 - Introduction and Vijay's background
The episode begins with an introduction of Vijay, a software developer with 16 years of experience. Vijay shares his background in computer science and his journey into blockchain development.

06:15 - Vijay's contributions to Dash and Bitcoin backports
Vijay discusses his initial contributions to Dash, starting with small Bitcoin backports and gradually taking on larger pull requests. He explains the process of selecting and customizing Bitcoin changes to integrate into Dash.

11:07 - Understanding Bitcoin backports and the selection process
The hosts and Vijay delve deeper into understanding what Bitcoin backports are and how they are selected for integration into Dash. Vijay shares a spreadsheet that tracks the progress of backports across different Bitcoin versions.

22:06 - Progress and challenges of Bitcoin backports
The conversation focuses on the progress of Bitcoin backports, the challenges involved, and the reasons behind certain versions not reaching 100% completion.

27:09 - Crypto situation in India
Vijay shares insights into the perception and adoption of cryptocurrencies in India, including the hype in 2021, the interest among students, and the general public's view of crypto as a speculative instrument.

31:38 - Legality and taxation of cryptocurrencies in India
The hosts inquire about the legal status of cryptocurrencies in India, and Vijay confirms that it is not illegal. However, he mentions that crypto is taxed similarly to speculative instruments like gambling or horse racing.

36:15 - Future plans and roadmap for Dash
The discussion concludes with Vijay expressing his interest in learning more about the future plans and roadmap for Dash. The hosts mention the focus on completing version 20 of Dash Evolution and gaining product/market fit. Vijay also expresses his interest in contributing more to the Dash project on a full-time basis.

## Transcript

[00:00] [MUSIC] Central bank digital currencies.
[00:09] All of the shitty lack of accountability and infinite money printing of fiat combined with terrifying technological fascism.
[00:18] That is where we are going, and that is where the powers that be are pushing us. You know my views on CBDC, and you know that I have pushed that project.
[00:31] Central bank will have absolute control on the rules and regulations that will determine the use of that expression of central bank liability.
[00:43] And also, we will have the technology to enforce that. And, as we were told in a publication by the World Economic Forum,
[00:50] headed by Klaus Schwab, "You'll own nothing, and you'll be happy." And, Schwab added, "We see science banishing forever unemployment,
[00:57] hunger, and insecurity of income. We see science replacing an economy of scarcity with an economy of abundance."
[01:03] Actually, those last two quotes aren't attributable to Schwab. They're from a pamphlet printed in 1933 by Technocracy, Inc.
[01:10] Technocracy in today's modern world is the singular most important concept that people have missed and also that people need to get a hold of.
[01:18] What is technocracy? What does it mean? Yeah, well, it's a good question. I suppose it's a word that's been around for a long time,
[01:26] but really what we're talking about is a society which is more and more controlled by the technology that supposedly liberates it.
[01:33] I would suggest that we're pretty much there already, or we're certainly on the brink of it. I mean, if you look at who holds much of the financial power, much of the economic power.
[01:43] The development and rollout of CBDCs is just the latest iteration of this perspective. Let's take a step back to better understand how we got here.
[01:51] On the heels of the so-called "war to end all wars," a seed was planted in the minds of some men. Those men, engineers and scientists, believed that they could do away with problems that plagued humanity,
[02:01] that they could more efficiently allocate scarce resources, that they could better manage the world. This is called technocracy, what some have likened to "dictatorship with degrees."
[02:10] The forward-facing traction of the technocracy movement reached its zenith in the early 1930s in the midst of the Great Depression.
[02:17] The Committee on Technocracy was established at Columbia University, and Technocracy, Inc. boasted over half a million paid members with chapters across the Americas.
[02:25] They advocated for a technate, a self-sustaining geographical unit of North America, Central America, and the northern portion of South America.
[02:32] They advocated for a shortened work week and, rather than use existing mediums of exchange, suggested energy credits.
[02:39] Members did outreach via events, parades, and yes, decades before the Blues Brothers, via vehicle-mounted megaphones.
[02:45] The public technocratic movement of that era was not shy about critiquing democracy. I think it's fair to say that that stance, which was at loggerheads with the successful rhetoric of
[02:55] "make the world safe for democracy," coined by Edward Bernays, caused overt public support of technocracy to atrophy.
[03:01] In fact, leaders of the technocracy movement in the U.S.S.A. were called to testify, and in Canada, the organization was outlawed and some of its members arrested,
[03:09] including the grandfather of Elon Musk, former director Joshua Norman Haldeman. But technocrat adherents did not go away, they merely went behind the scenes.
[03:17] Many were involved in the creation of non-governmental organizations, which ultimately came to wield much influence.
[03:23] And, having learned from the past, rather than attack democracy, they now pay lip service. As Bernays wrote in 1928, "Those who manipulate the unseen mechanism of society
[03:33] constitute an invisible government, which is the true ruling power of our country." Well, here we are, almost a century later, and the ideas of technocracy are not constrained by political boundaries.
[03:43] Hence, why virtually all central banks in the world belong to the Bank for International Settlements and are working towards interoperable CBDCs.
[03:51] We see all of the genesis of these ideas back in the original technocratic technocracy documents. The problem is they did not have the technology at the time to do what they wanted to do,
[04:01] and I think they knew that. It was just an idea, the idea of a utopia, that they felt that technology eventually would bail them out.
[04:10] And it didn't happen, maybe quite as fast as they thought, but here we are today, and we see these things being implemented today, almost in lockstep with the original document.
[04:17] It makes no difference whether technocrats are driven by goodwill or by malevolent intent. Their ultimate aim is to control.
[04:24] Now we are armed with this knowledge, with this historical perspective. We need not act out of fear, but with confidence, knowing that our work is timely and is important.
[04:32] We need to act with purpose, to deliver a product, a medium of exchange, that works. In doing so, we will create a tool, a technology, that we and our neighbors can use
[04:42] to peacefully pivot away from the prison planet so long constructed by technocrats. We will be empowered, and we will flourish.
[04:50] [music] >> Hello, Bader Weekly, and hello and welcome to our guest Vijay.
[05:05] How are you, Vijay? >> Thank you, thank you, thank you very much for having the show.
[05:10] I'm very good, thank you. >> If anyone's wondering what that sound was that you just heard,
[05:16] it is the Festival of Lights in Vijay's area of the world. And so you're actually hearing fireworks explode, is that right?
[05:25] >> Yeah, yeah, yeah, yeah. >> Yeah, righteous. Well, super glad that you ducked out of the Festival of Lights to be on our show.
[05:33] So we are going to -- first of all, let me apologize to you, Vijay, that I announced last week that you were a new developer in the Incubator,
[05:45] but you've actually been around for like two years, is that right? >> Yes, yeah, yeah, yeah.
[05:51] >> Okay, so before we get into the work that you've been doing the past two years, I want to -- and hello, Rion, welcome.
[05:59] >> Thank you. >> Good.
[06:01] >> I apologize for being late. >> No problem.
[06:05] >> So since this is your first time with us, Vijay, would you tell us just like how and when you got started with coding?
[06:15] >> Yeah, sure. So I'll keep it short. My name is Vijay, Vijay Das Manikpuri.
[06:23] So I have around 16 years of experience around software product development. It started after my schooling, I would say.
[06:33] So I was always -- I mean, I was always like attracted with technology and stuff and computers just after my school.
[06:43] So after my schooling, I did a graduate course in computer science. And then after completing that, I did a post-graduation course in the same stream.
[06:57] And then I have been developing various -- I've been involved with various software product development products,
[07:03] companies, projects. And this is still continuing, growing very strong to date.
[07:11] And with respect to blockchain, I was interested -- I mean, looking into code, it all started in 2019.
[07:21] And then I happened to come across Dash in 2021. >> How? Do you remember how?
[07:31] >> Yeah, actually, yeah. So what happened is during 2021, I had this --
[07:38] I was actually infected with COVID and had a long bout. I was down.
[07:42] I was lying. I was lying on the bed and just exploring, like,
[07:46] projects on open source blockchain contributions. And I think I saw somewhere Dash and just clicked on the link
[07:57] and reached a couple of people. And then I think I remember the name Victoria who asked me to connect with Pasta.
[08:07] So if you are interested in doing more open source contribution to blockchain community.
[08:13] And then once I got introduced to Pasta, then it was slowly -- then it started and it's still growing strong.
[08:21] So I just -- full request, full request. >> Okay.
[08:26] I've never been more glad to hear that somebody got sick. I'm glad you got sick so that you could find Dash.
[08:32] >> I was going to say, that seems like it was the only thing that was good that came out of COVID.
[08:38] >> Yeah. Right on.
[08:41] Okay. So then before we get to your most recent Dash contributions,
[08:46] which are the Bitcoin backports that are the title of the show, what kind of work did you start doing for Dash when you started?
[08:56] >> So initially it was a small Bitcoin backport. So backport was -- basically I started with backport only.
[09:06] So there was some -- some of the issues were labeled as good first issues. So I just had a look at them.
[09:15] Some good first issues to make myself comfortable and be known to the -- make myself aware with that, how the coding works,
[09:26] what is the coding standards. So Pasta shared me all those links, like,
[09:31] to make myself understand those guidelines that we follow. So then after that I made myself comfortable and then started --
[09:43] gradually started contributing. First was two, three commit pull request.
[09:48] Then three, four commit pull request. Then I -- gradually then I started doing ten commit pull request.
[09:53] Larger pull request, substantial contribution to there. >> And I just noticed as I was driving over here, I look at notifications.
[10:04] I have the GitHub app. And I noticed you pushed six commits just 20 minutes ago, just before --
[10:13] >> Yes, yes. >> Always very, very busy and very, yeah, diligent.
[10:20] >> Wow. Okay.
[10:22] I would just like to -- I'm sure I don't need to try very hard to reveal some of my ignorance,
[10:28] but I'd like to reveal just a bit of it and get a bit more established on just what Bitcoin backports are before we proceed.
[10:37] My understanding is that they are updates that have been made to the Bitcoin code base, and they need to be reviewed individually,
[10:47] one at a time, to decide whether or not we want to bring them into Dash. Is that what they are?
[10:53] >> Yeah, it is. Almost there.
[10:57] You're right. In fact, most of the part is right, yeah.
[11:01] >> Okay. And so then is that a judgment call that you yourself are making, Vijay,
[11:07] as you review them? Are you saying, yes, this should be in Dash, no, this should not be in Dash?
[11:12] Or how does that work? >> So we have -- so there is a list which is shared.
[11:23] We have -- that list is being -- I think it is being prepared by Pasta. I think it is being prepared by Pasta.
[11:29] So there is a list of -- there is a list of all changes which has been pushed into Bitcoin version-wise.
[11:39] So for a particular version, there are a set of changes. And those set of changes that we want to bring into Dash and customize it to Dash.
[11:51] So basically there are certain things which are not -- which we are specific to Dash-specific, and we do not take, for example, segwits, which I understand
[12:01] that those are only Bitcoin-specific. In Dash, it is not required.
[12:06] So initially when I started, I was not aware of this. So I brought it all in.
[12:11] And then I got the suggestion that these things we do not have. And based on those suggestions, I started making those acknowledge that these
[12:22] will be not imported. These changes will not be importing.
[12:26] So that's how I make it -- make intro. So to answer your question, there are a set of lists already there which is
[12:38] shared across all the contributors. And we can mark it that this change, I'm going to take care of it.
[12:46] There are other contributors. They mark, okay, this is -- I'm going to contribute this one.
[12:51] So that's how we select whatever we want to select. If it is not marked, it is still open.
[13:00] Then anybody can pick up and start bringing in the changes, customize it according to the Dash, and then test it and verify it.
[13:12] And then it gets reviewed and approved. And then it gets merged.
[13:20] >> Nice. >> Yeah, I'm sorry.
[13:24] So just to tell that -- so I was just checking how many -- I mean, before doing the show, how many I have successfully merged so far.
[13:31] So far I have completed half a century of it. I have done 50 successful merges so far.
[13:38] >> Nice. Okay.
[13:40] So shall we take a look at some of those? Does that sound like the right thing to do next, Rion?
[13:44] Or do you have a different suggestion? >> I was just looking through the Trello board, the card for Dash Core
[13:51] contributions to try to find that spreadsheet. And I know it's public, but I don't know what the link is right offhand.
[13:59] So if you have that handy, Vijay, I think that would be interesting to look at.
[14:04] Because I'm one of those guys that's -- I'm always kind of seeing the notifications come in, and I'm always wondering, wow, it seems like there's a
[14:11] lot of backports that are always happening. When are we ever going to get caught up?
[14:17] Are we caught up? And what's the status?
[14:20] So I'm not seeing that list, that Excel sheet here. So if you have it handy, that would be great to show.
[14:28] >> I just shared it. >> Okay.
[14:31] You shared it. >> Yeah, I think --
[14:34] >> So at the bottom of your screen, Vijay, if you would just click the button "present," and then that will give you the --
[14:45] >> Yeah, yeah. >> So anyway, in the meantime, Rion, you may not have heard what we're
[14:56] hearing on Vijay's end. It's Firecracker, because it is the Festival of Lights.
[15:01] >> Oh. Dang.
[15:03] Well, sorry to pull you away from that. >> Don't worry.
[15:12] >> I'm not seeing the -- oh, here we go. La, la, la.
[15:17] >> Can you see it? >> Yes.
[15:21] >> So these are the most recent merged ones. So as you can see, these are all numbered.
[15:32] >> So do these need to be altered? Like when Pasta publishes the list and you start going through the list,
[15:41] what are you doing to these things exactly? Like are you changing them in some way so that they're not Bitcoin but
[15:49] they're Dash? >> Yes.
[15:51] >> How would you do that? >> So this is the list, actually.
[15:57] So you can see these are the versions, different Bitcoin versions. So when I started looking into it, I was here.
[16:08] Now I've seen this all things going in front of me. So now we have open to 25.
[16:15] So suppose we want to look for 21. >> I'm not sure if we're looking at the same thing here.
[16:21] I'm seeing a text file. And I think you're talking about a spreadsheet.
[16:32] >> Let me see if I can share it again. >> You might be sharing the wrong window.
[16:42] >> Yeah, so if you just go back down to present on the bottom of this screen here in StreamYard, it should give you the option to share
[16:50] different things. >> Okay, yeah, yeah, yeah.
[16:56] One second. >> Definitely.
[17:00] >> So Amanda, while he's looking that up, I unfortunately was late this morning and I didn't catch the intro video from Pete this morning.
[17:09] What was that about? >> That was about the history of technocracy.
[17:15] And I didn't know that there was such a vast history -- I didn't know there used to be an institution called like the Technocratic Inc.
[17:22] Or whatever. It used to be like a major think tank movement, I guess.
[17:28] And they published all kinds of documentation about their goals for how the world would work.
[17:35] But once they started making certain political kinds of statements, I guess, against democracy or whatever, they like fell by the wayside.
[17:45] But the Newsreel argued that actually all the original goals published in their original papers are still very much being worked on today by
[17:53] different organizations. But they just changed their names and they don't use the word
[17:58] technocracy anymore. And it argued that the idea of a global CBDC is very much in line with
[18:05] technocratic ideals. >> Yeah.
[18:09] I hope my screen is -- is it visible now? >> It is.
[18:18] >> Yeah, yeah, yeah. So you can see the -- we can select one version.
[18:24] And here's the status. So if this one is completed, then it will be marked as done.
[18:31] And if it is not marked, anybody can pick up. So these are my initials.
[18:38] So suppose I want to work on it, I'll select this. And then it will be with me.
[18:46] So I can contribute here for this one. And so, for example, I have this.
[18:57] And then what we have is I can show you one. So this I can bring ten such commits like this, one, two, three.
[19:14] Select ten of those. And bring it under one pull request.
[19:19] So just to -- this is the original one from Bitcoin. And so this is the Bitcoin.
[19:34] And this is our change. So some of those are -- some of the changes are direct.
[19:52] Which do not make use of -- which does not require customization. Some changes may require customization.
[20:01] And those changes are like, for example -- >> Just what the hell kind of changes are being made to Bitcoin that there
[20:13] are this many of them? I thought that the -- I thought that Bitcoin was the thing more or less
[20:17] that never changes. Like what is all of this?
[20:23] >> So you can see that there is refactoring going on. There's tidying up going on.
[20:31] There are -- so refactoring is going on. Some kind of issues like detecting double lock and threading.
[20:41] That issue gets solved. So we want to bring that in.
[20:47] >> So as you think back over all of the pull requests that -- or all of the backports that you've done, is there a broad theme of what kinds of code
[21:01] you're backporting? Or is it just kind of all over the place?
[21:07] Lots of different things. >> So there are lots of different things.
[21:12] And theme-wise, basically, so as you can see here, so there are various -- some are related to wallet.
[21:25] So there is a tag here also, which we can filter. See all wallet-related or net-related.
[21:32] So these kind of changes are -- so different wallet tools. So these -- just before pulling, there is a tag which makes -- which tells
[21:46] that these are the -- this is basically the area which it is focusing on. So net-related area, wallet-related.
[21:55] So those kinds of areas, basically. >> And have you shown the stats tab yet on the screen?
[22:06] Because that's what I'm looking at. >> Which tab, Rion?
[22:10] >> The stats tab. That's all the way to the left.
[22:14] I think that might be interesting to some people. I know that's what I'm kind of interested in.
[22:25] So all the way to the left. In the tab.
[22:29] >> Yeah, yeah, this one. Yeah.
[22:34] So you can look at the -- >> So on the left, we're seeing it looks like the Bitcoin version number
[22:44] in that column. And then all the way on the right, you're seeing the progress of basically
[22:51] how many of the pull requests, how many of the commits do we actually want to and what's the progress of all those.
[23:00] And it looks like up to version 20, we have nearly 99% backports done. And then version 21 through 25, ever decreasingly percentage number.
[23:15] So is that -- I guess, yeah, there's just like a few more commits to do on those versions 16, 17.
[23:24] Do they ever get done? Like I see the 100% on 17.
[23:31] >> Yes. >> And I guess the version 16, which sequentially was before 17, is there
[23:38] like -- is there a debate about whether we should do that or is this a difficult -- is it a difficult commit to backport or why would version 17 be
[23:51] 100% before 16? >> Yeah, so some of the changes are, as discussed, there's a column here
[24:02] which has one thing, which has DNM. It says do not merge.
[24:09] And because some of the changes are not applicable to or not related to our dash platform, for example, there are certain segwit related changes.
[24:27] So it depends on segnet. And those are not applicable to us, to dash.
[24:36] So that's the reason it won't be 100% because those are not -- for example, this does not seem dash specific.
[24:46] And these are segwit. So those are do not merge.
[24:52] So they are do not merge. So there are a couple of -- I think there are a few numbers of these
[24:59] changes which are not -- does not need to be bring into dash. So that's the reason it is not 100%.
[25:11] And for this one, these ones are added recently. So 23, 24, 25.
[25:20] So as in when it stays for more longer duration of time, we'll see further contribution going here and the numbers improving this time.
[25:36] >> It is insane to me that there could be -- I'm looking at hundreds of updates to the Bitcoin code base, right?
[25:44] None of which are what are considered breaking updates. Meaning if I was still running, like, what, version 1 of Bitcoin to this
[25:54] day, it would still be compatible with, what, version 25? Is that right?
[26:02] >> I don't think all the way back to 1. There have been hard forks in Bitcoin.
[26:07] >> There have? >> Yes.
[26:11] As far as I understand. I remember when I was first getting into Bitcoin.
[26:16] I think it was version 0.8. There was a bug.
[26:20] And they had to roll that back. I don't know.
[26:25] This has been, like, over ten years ago. So I'm not really sure.
[26:29] I'm fairly sure that Bitcoin has had hard forks in the past just to fix bugs, if nothing else.
[26:36] Like major bugs where there's an inflation bug. >> Oh, wow.
[26:40] I did not know that. Okay.
[26:44] >> But, yeah, like, recently, I think, is more when they adopted the soft fork only mentality.
[26:52] Yeah. >> Okay.
[26:56] Well, is there anything left to say on the topic of backports before I ask Vijay a bit about the crypto situation there on the ground where he lives?
[27:09] No? >> None for me.
[27:13] So, yeah. >> Okay.
[27:17] Well, yeah, I was telling Vijay just before the show that I just wanted to hear a little bit about what his friends and family think of crypto or
[27:25] Bitcoin. He's certainly never been to India.
[27:29] I don't know what the situation is there. I wanted to hear his reflections on that.
[27:33] >> Yeah, yeah, yeah. So 2021 has been the major year, actually, where a lot of voices, a lot of
[27:40] advertisements and a lot of new wallets and a lot of new exchanges that has been launched in India.
[27:48] Primarily was Vazirex and Coinbase. Coinbase is a coin exchange.
[27:55] So a lot of exchanges cropped up in 2021 in India. And then there were -- so mostly around friends, those who are not in tech,
[28:10] those are mostly, like, treat them as a speculative instrument to invest. And then there are a couple of talks about this, with respect to government,
[28:27] there are this digital currency talks, CBDC, that I think some of Indian government has -- I think it has launched in pilot basis.
[28:36] But mostly around friends, it's mostly a speculative instrument. And new students want to learn this contract, this blockchain contracts.
[28:55] So students, they are quite interested. So I remember in 2019, I first started to teach, actually, this contract
[29:10] thing, this Solidity and Ethereum blockchain around that time. >> You were teaching?
[29:16] >> Yeah, I was trying to teach. Not very successful.
[29:20] But I did try to -- teaching this blockchain, did not continue, pursued it for so long.
[29:27] So that's how I started this blockchain development. >> Not very successful.
[29:35] I'm just wondering, like, was it the actual -- the way Ethereum works that you think made it so you weren't successful in teaching?
[29:43] Or was it something else? >> Yeah, something else.
[29:47] I could not continue it for very long. >> Okay.
[29:51] >> For some other reasons. Yeah, so basically, so it was hyped up around '21 and then '22.
[30:00] And then as the market goes down, the interest vanes. So then the market comes up again, new people try to -- they hear that, like,
[30:15] this price is going up. And then this greed, fear, and what was that -- that thing.
[30:23] >> Yeah, it's interesting that that happens that way. Because you would think if your only interest in these technologies was for
[30:32] the speculative aspect, you'd think that there would be more interest at the bottoms of markets.
[30:38] And people wanting to get in at that point. But it's always the opposite.
[30:43] People always want to start buying when the price has already gone up. And then people start wanting to sell when the price has gone down already.
[30:51] >> And there's also the conundrum. I don't remember where I heard someone say this.
[30:55] But I thought, oh, dang, yeah. There's also the conundrum of should I talk to anybody about the coin or coins
[31:02] that I think are interesting? Because is it potentially me putting myself in a damned if I do and damned if
[31:09] I don't scenario? Because if I tell someone about a coin or coins I'm interested in and it goes
[31:16] down, then they're thinking, like, you bastard, why did you do this? Or if I don't tell them about a coin or coins I'm interested in and it goes up,
[31:28] again, they're thinking, you bastard, why didn't you tell me to buy back when you were buying?
[31:34] So, yeah. >> Well, it's a simple solution, though.
[31:38] You just tell them to buy when it's low and it goes up, right? >> Oh, right, right, right.
[31:44] My crystal ball. True.
[31:47] >> I'm interested in is it legal there or what parts -- what part of cryptocurrency is legal and what's illegal to your knowledge?
[31:56] Is it, like, can you work -- I mean, obviously you're here on screen. And, you know, if it's illegal there to do X, Y, or Z, then that's commendable
[32:09] that you're on the screen showing your face. But I'm guessing that it's not -- that it is legal and that it's not illegal
[32:19] to be doing certain things. But I would imagine, like, transacting or having a business that's dealing
[32:28] with crypto, is anything illegal? >> No, it's not.
[32:33] No, it's not. >> Okay.
[32:36] >> Cool. >> That's good.
[32:39] Because I'm always worried, like, that would be the worst reason to not have adoption.
[32:44] So if everything is legal and, like, I always wonder what the holdup is, you know?
[32:52] Why aren't people adopting it? And I obviously have some ideas about that.
[32:56] >> Only the taxation part, the way it is taxed, right, the way it is taxed is right now it is put in par with all those speculative instruments.
[33:07] For example, with -- what did I say? The tax rate for this crypto is equal to the level of the money earned through,
[33:23] like, gambling or horse racing kind of thing. So it is put on that same tax bracket.
[33:30] >> Okay. >> And what are people's -- in your experience, Vijay, what are people's
[33:36] feelings about the rupee in general? Like, do they feel, like, yes, this is super solid.
[33:42] I feel awesome about keeping my savings in it. Or, like, eh, I kind of want to move my savings into something that has a
[33:50] better outlook than the rupee. >> The thing is that the crypto has also not so far shown them that kind of
[34:02] stability. Everybody is trying to -- so currently there are financial awarenesses,
[34:10] awareness, which is at least in certain area of society, certain level of where people do want to conserve their buying power.
[34:22] But the problem is that they have seen so much down in crypto as well that they rather keep it there only.
[34:33] >> Yeah. >> That's the thing.
[34:37] >> Yeah. That's something that Rion has spoken extensively about in the past.
[34:42] I don't know if he has spoken in any of those presentations. But about whether any cryptocurrency can really compete with any legacy
[34:53] currency if it doesn't offer the same stability in purchasing power over time.
[35:00] >> Is India becoming dollarized to your awareness? Are people stacking dollars?
[35:07] Or -- and using dollars like some of the South American countries are doing?
[35:13] >> No. >> No.
[35:17] >> I think there is the financial system overall in India is pretty much stable.
[35:23] With respect to -- we haven't printed money. So I have very limited knowledge on that.
[35:29] But whatever I read in the newspaper or in the blogs and various financial experts, that in the recent times with respect to U.S. dollar, they have been
[35:43] printing a lot of money. But that is not the scenario with respect to Indian financial systems.
[35:51] Although there is the inflation rate is still around 8% here in India, 7%, 8%. But I'm not really expert.
[36:00] But this is in general layman's understanding of it. >> Yeah.
[36:07] That matters. Okay.
[36:11] I think that covers all the questions I had. How about you, Rion?
[36:15] Do you have anything left? >> No.
[36:19] Other than I will pass it back to Vijay. Is there anything that you need or want to say that we haven't talked about?
[36:27] >> I think we have covered pretty much every aspect. I'm just interested in like how -- what are the roadmaps for the -- with respect
[36:40] to Dash, what we are -- what we have major plans for. >> I, too, am interested in that.
[36:50] >> Yeah. I think that's -- yeah.
[36:54] Everybody is interested in what's the roadmap. As far as I understand, the roadmap is what it's been for the past several years.
[37:01] Get evolution done, version 20. Get them hooked up.
[37:06] And then move on from there to try to gain market -- product/market fit. And see if there is product/market fit, rather.
[37:17] So as far as like major -- there's a ton of new features that I'm sure that we can work on. Smart contracts, people have talked about.
[37:29] And just general adoption of Dash platform is the main focus, I think. For most people.
[37:39] >> Well, and given that you've already shown, Vijay, that you have an interest in teaching people to write blockchain contracts, I wonder if Dash platform's data contracts might be of interest to you
[37:54] and might even be of interest to you in teaching others, ultimately. Have you looked much into the platform data contracts currently on testnet, Vijay?
[38:05] >> I haven't yet. But I will definitely give it a look.
[38:11] >> All right. Well, I think that might be a good place to close it out.
[38:16] And look forward to seeing the Bitcoin backports speeding up. And then hopefully -- I know they'll never be finished.
[38:27] But I would love to catch up so that I feel like, okay, now we're just in maintenance mode instead of catch-up mode. I feel like they were probably neglected for several years.
[38:38] That was my -- that's my intuition based on how much work there is to be done at this -- over the past year or so. I think that that was coming off of maybe not doing a lot of backports in previous years.
[38:52] Or maybe there's just so much work to be done that it takes a lot of people to -- you know, a lot of time to -- on the surface, it doesn't seem like it should be a lot of work to bring code in that's already been written.
[39:07] But I know that that's just my naive understanding of it. And there's a lot of work to be done in reviewing and whatnot.
[39:15] But I would love to see that status -- let's see, the stats bar. Is this a public sheet, by the way?
[39:22] Can we share this? Yeah, okay.
[39:25] I guess we could share it and see if it's public or not anyway. But, yeah, like I'd love to see these version 21 through 25 just get those green bars like the other versions have been done
[39:37] and then basically just get in maintenance mode. But maybe there's some strategy about, you know, giving Bitcoin some time to prove that there's no bugs in these codes.
[39:49] And maybe we are at that point. I'm not sure.
[39:52] It might be more of an appropriate question for Pasta. Kind of making the sheet.
[39:58] But, yeah, thank you. Thank you for your work.
[40:00] And we're happy to keep funding it through the incubator, obviously. And I know that you expressed some interest in working more.
[40:11] So is that still the case? Like more on a full-time basis, if you could?
[40:20] That's what I was wondering if you might mention at the end here. Yeah, yeah, yeah, yeah.
[40:27] That sounds like a yeah. Yes.
[40:32] Okay, good. Well, thanks for joining us today, Vijay.
[40:35] And please enjoy the rest of the Festival of Lights if you can. And we'll see you all same time, same place next week.
[40:42] Yep. All right.
[40:44] See you. Bye-bye.
[40:46] Bye.