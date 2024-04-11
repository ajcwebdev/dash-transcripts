---
showLink: "https://www.youtube.com/watch?v=qxenir9mwg4"
slug: "decentralized-dynamic-app-infrastructure"
title: "Decentralized Dynamic Application Infrastructure"
publishDate: "2023-08-28"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/qxenir9mwg4/maxresdefault.webp"
---

Tim provides an overview of a project that creates an easy platform for building decentralized applications using Dash Platform and IPFS.

## Episode Summary

tl;dr: Tim discusses a project that aims to provide an easy-to-use platform for building decentralized applications (dApps) by leveraging Dash Platform for structured data and IPFS for storing larger files. The project centralizes the command structure for uploading to IPFS and writing metadata to Dash Platform, making it simpler for developers to create dApps without needing extensive knowledge of the underlying technologies. The current version is functional but command-line based, with plans to develop a web interface for improved accessibility.

## Chapters

00:00 - Introductory discussion on current events and the future of blockchain technology
The hosts discuss their views on the current state of the cryptocurrency market and the potential implications of central bank digital currencies (CBDCs) on personal freedom and economic sovereignty.

05:24 - Introduction of the guest and the project overview
Tim is introduced as the guest, and he provides a high-level overview of the decentralized dynamic application infrastructure project, which aims to create an easy-to-use platform for building dApps using Dash Platform and IPFS.

10:36 - Explanation of the project's purpose and benefits
Tim explains how the project centralizes the command structure for uploading files to IPFS and writing metadata to Dash Platform, making it easier for developers to create dApps without needing extensive knowledge of the underlying technologies. The project's potential use cases, such as storing photos and creating content management systems, are discussed.

17:04 - Current state of the project and future plans
Tim discusses the current state of the project, which is functional but command-line based. The next step is to develop a browser extension and a web interface to improve accessibility for developers. The project's progress has been affected by changes to the Dash Platform, requiring rewrites and research to keep the project up-to-date.

30:16 - Closing remarks and announcement of the upcoming Dash retreat
The hosts conclude the discussion on the project and announce the dates and location for the upcoming Dash retreat in Utah. They also mention plans to live stream presentations and facilitate remote participation for those unable to attend in person.

## Transcript

[00:00] "If you've studied Austrian economics for more than 30 seconds, you know that inflation is always an increase in the money supply, it's a monetary event.
[00:13] And we've printed more money over the last four years than in the history of the country preceding it.
[00:19] In combination with interest rates at or near zero created massive, massive, massive distortions." The U.S. government has a knack for printing money and causing problems for other countries.
[00:31] As a result, countries are realizing the importance of reclaiming economic sovereignty and reducing their reliance on the U.S. dollar.
[00:39] "Another subject that's getting some attention this week is what I'm now told is de-dollarization. That is the question about whether the U.S.'s reserve currency is at least losing market
[00:48] share. There was a report on the Bloomberg that actually last year it lost market share at ten times
[00:54] the rate that was the average of the last 20 years." "And you touched on this idea that creating a weaker dollar, which leads to the collapse
[01:01] of the system, may be an intentional effort from within the U.S. to engineer a reset leading to a CBDC or central bank digital currency."
[01:12] "I mean, could you think of a better pathway than by first weaponizing the dollar, not just sanctioning Russian assets, but confiscating them and using them to rebuild, supposedly
[01:24] rebuild the Ukraine, and then telling Saudi Arabia, 'Hey, thanks, but we're going to go green, so we really, you know, we're not going to be as inclined to buy as much oil from
[01:37] you forever because this is, we're moving away from this.' You couldn't draw it up any better, and rather than falling on the sword and being blamed
[01:46] for destroying the American way of life through mismanagement. Better yet, you find a villain, and it was Putin's inflation and OPEC and Xi Jinping
[01:55] and this new alliance of countries that turned their back on the U.S., and they did it. When I started thinking about that and looking into it, and I came across who the number
[02:05] one economic advisor is for the United States government, I almost fell off my chair. His name is Jared Bernstein, and he wrote a report in 2014, I believe, an op-ed that
[02:17] was picked up in the New York Times called Dethrone King Dollar. And in it, he stated that the government needs to drop its commitment to maintaining the
[02:26] dollar's reserve currency status. The other gal that I talk about, the number two economic advisor, is Lael Brainard, who's
[02:33] a modern monetary theorist who wants a central bank digital currency. He's ran point with the government and the Fed on FedNow.
[02:41] So what is this FedNow system, where you can send money instantly from one person to another, at least anywhere in the United States, and it can happen in seconds instead of hours
[02:50] or days? The question is, is this the beginning of total overreaching control by the federal
[02:55] government into our personal lives? Well, let's be honest.
[02:58] The federal government definitely has some insight into our credit cards, our transactions, our histories, our banking records.
[03:04] All that stuff is really very closely networked to the federal government. Obviously, a CBDC is quite different because programmatically your money can just be shut
[03:12] off. And what did the BIS say?
[03:15] Every country needs to have one operational by 2025. 95% of the GDP in this country or the countries that make it up have a CBDC in development.
[03:25] It is coming. Just because they say it's not a CBDC, well, they know better now because the term CBDC
[03:31] has officially been done and dusted. It's a toxic term.
[03:34] And if they do enact some form of a CBDC, you better believe that they're not going to call it one.
[03:39] And so, look, you know, you have one advisor wanting to get rid of the banks and go CBDC and one wanting to get rid of the World Reserve status.
[03:48] So is it coincidental? Sure.
[03:50] I guess it could be. Are they really that stupid?
[03:54] Sure. I guess they could be.
[03:56] Or is there a modicum of a chance that some or a lot of this is designed in a very nefarious way?
[04:03] We live in an age where two visions of the world are colliding. On the one hand, there is the vision of freedom.
[04:09] In this vision we have the autonomy to shape our own life and to live in accordance with our own goals.
[04:14] Where the vision of freedom reigns, the rule of law is not an arbitrary expression of state power, but is shaped around the ideal that we may live as we wish so long as we do not
[04:23] aggress against the person or property of another. The vision of freedom is clashing with what the American economist Thomas Sowell has termed
[04:30] the vision of the anointed. In this vision the global population is to be divided into two classes, the rulers and
[04:37] the ruled, so that the anointed class can attempt to actualize their idea of a brave new world.
[04:43] This country seems to do its best when our back's against the wall. An organic movement, composed of men and women who are bound together by the idea of freedom,
[04:52] is what is needed to counteract the forward march of the vision of the anointed. For only power can thwart power, and the vision of the anointed is backed by immense institutional
[05:02] and financial power. But the vision of freedom can be backed by an even greater power, the power of individuals
[05:08] possessed by a vocation and united in pursuit of a shared cause. Hello and good day everyone, welcome to Incubator Weekly.
[05:24] I'm here today with my always here co-host Rion. Good day Rion.
[05:29] Howdy everyone. Howdy everyone.
[05:32] And today as our guest we have, okay so I want to make sure I get this right. So Tim, you withdrew your incubator strategist proposal this last cycle, but of course as
[05:50] you have shared in past quarterly updates, you have a reserve budget with which you are working and that is being applied to the project we're talking about today, is that right?
[06:02] Yeah, that's correct. This was one of the two priorities that the reserve has gone, well one of the three priorities
[06:11] that the reserve has gone towards, two projects, this one and then the Dash Challenge one which we talked about several weeks ago, maybe a couple months ago now at this point.
[06:19] And then some ongoing DashMate assistance work. Got it, thanks for that update.
[06:25] So before we jump into the project of which Tim referenced, which is the decentralized dynamic application infrastructure, I did want to make a little comment on today's newsreel
[06:39] because it, okay so the part of the newsreel where, I don't remember which guy said something like somebody has a future vision of two classes of people in the world, the class that does
[06:53] this and the class that does that, that I found to be quite ironic that I think a lot of people associate that sort of dystopian worldview only with the fiat, that's the fiat
[07:11] nightmarish future and crypto in any form, in all its forms is here to save us from that dystopia.
[07:19] And the ironic part is that the most popular figure, the most popular developer in one of the top cryptos by market cap gave an interview.
[07:35] Oh, come on, name names here, you're being very, just kidding. No, I, no, well for, okay maybe some people in the comments guess and how about I tell
[07:46] you if you're right. So in this video, which I saw on YouTube, I would say five years ago, and I don't even
[07:53] know if it's still on YouTube, I don't even know if I could find it. It was not a very highly watched video, but this individual said, I see a future in which
[08:08] only the people who are basically really good at programming blockchains need to work, need to have jobs, and everyone else can be freed from the need to work or have jobs.
[08:26] I'm going to guess, I'm, oh, go ahead, you finish your thought. No, I just, I remembered that, that creeped me out so much.
[08:36] Even now I have like, like creepy goosebumps on my arms just from how creepy I think that statement is, just that somehow like 99.5% of humanity is unnecessary, and like that
[08:54] wouldn't lead to something nightmarish. As such an interesting perspective.
[09:04] I mean, on two hands, you have the one perspective that, oh, this technology is the solution for all of humanity's ills.
[09:12] And then the other perspective that, and only those that know how to build on this technology are the ones with valuable things to offer the rest of humanity.
[09:23] Yeah. They're the saviors.
[09:26] Was this, was this Vitalik and Ethereum that you're talking about? Or was this?
[09:31] It was. You guessed it.
[09:33] Oh, I didn't even have to go with my second guess. The second guess was going to be Charles Hoskinson from Cardano.
[09:41] Those two both seem like they could say such thing, but yeah, that's just, that's not a world I want to live in.
[09:51] I see, I see a future where blockchains enable people to leverage their, their existing skills and their existing occupations even more in a more free manner, but certainly not doing
[10:05] away with them. Yeah.
[10:10] Turning them into Soylent is basically what it sounds like to me. Yeah.
[10:14] Yeah. Soylent Green, I guess is what it's called.
[10:18] I've heard of, there's a movie called Soylent Green. I've heard of it, but I haven't actually watched it.
[10:22] My wife brings it up every now and then. Oh yeah.
[10:26] Watch it. It's fun.
[10:28] Okay. In a bad way.
[10:30] Yeah. Yeah.
[10:32] Good. Well, on that note, I don't know why on that note, but let us do now jump into the decentralized
[10:36] dynamic application infrastructure. Tim, will you give us a high level overview of what that is?
[10:43] Yeah. So actually it, it is, the point of it is to create a more or less easy, and I put easy
[10:52] in quotes because there's different levels of easy, but an easy way to utilize platform for building your dApps.
[11:05] And the easy part is that it centralizes, maybe somewhat ironically, it centralizes the command structure for like the code command structure for uploading to IPFS, for being
[11:21] able to write to platform, the location and the metadata about what has been uploaded to IPFS and then being able to reference the dash, the, the, the platform document in whatever
[11:36] you're displaying to the user, whether, whether you're displaying like blog content or whether you've got a full blown, like a full blown user game interface that you're, that you're,
[11:49] that you've tried to, that you've gone ahead and built. And it can be used as simply as, Hey, I want to store photos in the cloud and the cloud
[11:57] is IPFS. And then your, your interface with that and knowing where, knowing what the locations
[12:02] are instead of having, if you've ever uploaded to IPFS, it is a really long hash that you wind up with, which is very difficult to work with and sure you could use you could use
[12:12] minimizers a bitly, for example, but then you've undone all of the benefit of having it decentralized and the really long hash part, I think is relevant because I think
[12:26] a lot of people have already started doing such things with embedding that hash into the op return fields of, of transaction in like a Bitcoin transaction where you're putting
[12:41] it on chain. Do you know right off hand if, if those hashes fit, I think that the limit is 80 bytes in,
[12:49] in the Bitcoin op return. Do you know if it's longer than that or how they're dealing with that?
[12:55] They're probably, no, I don't know if it's longer than that. And so I also don't know how it'd be, how, if it is longer than that, I don't know.
[13:04] And I don't know if it's dealt with yet or if that's on the roadmap. That's not, that's not something that we have talked about specifically.
[13:12] Yeah. But regardless, you know, just having, having structured data that you can name fields that
[13:19] is a definite bonus of Dash platform. So I'm assuming that this will allow you to, to not only upload the hash, but also some
[13:30] metadata about the hash. Yeah.
[13:33] So right now, right now it's a set group of metadata, but the future state will be that you can then do any definition that you need to for your own purposes or for anybody else's
[13:44] reference purposes. You can, you can customize that and what gets put into the document for, but for easy purposes,
[13:51] it's at the moment it's simplified. So it's like the name of it and a brief description of it and some categorization tags if you
[13:59] want to add those. So I'm thinking right away, like my wife is a photographer on the site and I know through
[14:08] just all the history and conversations that Dash platform is not suited to uploading actual images, but IPFS is more or less designed for that.
[14:20] So this is a good, a good application and this infrastructure I'm sure will help with applications like that, where the developer does it, has, has a use case where platform
[14:34] is not intended to serve that use case. And so they can work together with Dash platform, with IPFS to, to store both the metadata and
[14:43] the data. Cause I don't think that IPFS was designed specifically to store the data part of it.
[14:51] It's more, I think it's more, more designed for larger data and like image data and things like that.
[15:01] But I'm not sure that it's designed to store structured metadata. So the compliment, these two compliment each other, I think in a good way.
[15:09] Yeah. And that's, yeah, that's part of it is it does give that mechanism.
[15:16] So like to Amanda, what you were talking about, you don't even know if that YouTube video exists anymore.
[15:21] Well one of the, one of the benefits of the immutability of the blockchain is, and one of the benefits that we see from IPFS is like, you can't just, someone, some authority figure
[15:34] can't just go through and tell you to pull the video down. Cause it's not stored at a location.
[15:41] The whole idea of IPFS is you're storing, you're storing an image of an image in the sense of you're storing a hash of the content and that content is stored on lots of different
[15:57] places. So it's not like there's like URLs are just like the name says, they're location based
[16:06] resource locators where you, you find the resource that you're looking for based on its location.
[16:12] But IPFS, you're finding the content based on the content itself, which can be hosted in lots of different places.
[16:19] So that does seem to solve that problem. Tim, the developer of this, I know that he has a lot of experience with IPFS and whatnot.
[16:34] Is he, I think that we talked about a little bit before he's not able to, he was not able to join the show today, but how far along is he on this project?
[16:45] And do you think that he's able to finish this within the budget that you have? Because as I was looking, I did payments last time.
[16:53] Your budget's pretty much. My budget is pretty much kaput.
[16:58] It's spoken for. Part of part of one of the spoken for pieces is the wrapping up of this phase.
[17:04] So where we are right now, the, the code base is there. It's all on GitHub.
[17:09] You can, you can load the package that he's built and it creates a small series of uploader windows and then it's got a small interface, the, the, and then there is a quick start
[17:23] guide. Okay.
[17:25] Yes. And I should have given you the, that is the quick start guide link right there.
[17:32] And so that gives you the location for everything that you need to know. The next step for this was that his, his longterm vision is that this is a browser extension.
[17:43] So you can just click on the extension in your browser, go to your computer, go to your, your explorer or your finder window, grab the files that you want to load up and load
[17:55] them up and it does, it does the rest. You can create a wallet, a dash wallet.
[17:58] If you don't have one yet, you can use a dash wallet that you already have and then it will take care of loading it up to IPFS, confirming that, grabbing it, sending the information
[18:10] to platform and then building that document and then giving you the reference, the platform that you need.
[18:15] And then you can then reference those in your HTML or in your JavaScript, or you could even to the point you could even almost use this as a CMS of sorts.
[18:25] You could remotely load your HTML or your JavaScript into whatever that that is that you've built at your little URL.
[18:33] So you can have something that's really lightweight on your own server that then pulls down the information from dash platform, pulls down the locations for everything that you need
[18:43] to know. And if you script it properly, then you can asynchronously pull down all your images and
[18:47] audio and text and, you know, your markup and your functional JavaScript and build the site or your app on the fly and dynamically.
[18:57] And so that's, that's the name behind it being dynamic and decentralized because we have, we're very familiar with how to build, how to build interfaces and how to especially
[19:06] web interfaces dynamically. But the decentralized part is what this helps to solve.
[19:12] And so it combines those two and makes it more accessible for more traditional web developers where you don't have to be, you still need some familiarity with platform, but you don't
[19:20] need to know how to do it all yourself. The package does the, does many of the mechanics and long-term should do all the mechanics
[19:29] for you. So that someone like your wife can just say, Hey, I want to, I'm going to create a little
[19:36] site here and I'm going to make it possible for these clients of mine to view their photos for so long.
[19:42] And then she can even could even write in the little contract, like, okay, these photos can be accessible with this ID for six weeks.
[19:52] And after six weeks, they're just not accessible with the ID anymore, or they're always accessible or they're accessible three or four or 10 times.
[19:59] And then after the 10th time, you can't, you can't access it anymore. Yeah.
[20:05] Nice. And you said the, you said, you said CMS, I'm not sure if everybody's familiar with
[20:09] that content management system. That's how a lot of a lot of websites are built these days, where you have a front end
[20:17] application that just can contacts a so-called CMS contact manager content management system that holds all the data on the backend.
[20:29] And so you're saying this could be used as a CMS where basically, yeah, you could create very, that's the simple way.
[20:37] Like if you're a developer, and you don't want to spin up your own backend server and database and all this kind of stuff, you outsource that currently to a whole number of there
[20:52] are so many web two companies that are doing this CMS as a service, so that you can just build a front end application back, especially when when spas single page applications were
[21:03] all the rage, and they still are very, very useful. That's how you would do it.
[21:10] But you're saying the twist here is, is that you can have that CMS, but it's a decentralized CMS.
[21:17] Yeah, you can do that. And then also, a lot of my not dash world is wrapped up in the Adobe ecosystem.
[21:25] And one of Adobe's big things now is the digital asset manager, so the dam. And this is essentially a decentralized digital asset manager.
[21:33] You have all these assets that have been loaded up. And so they're, they're referenced on all the IPFS nodes.
[21:41] So you don't have to worry about someone coming through and taking them down and deciding that this is inappropriate for whatever purposes.
[21:47] And then you have the permanent reference to the locations and IPFS on the dash blockchain. So it can never get lost.
[21:58] Interesting. There's always there's always going to be a way to recover the location of that file.
[22:04] Well, this sounds great. Now, just remind me, because I did ask, and I'm not sure if I was even paying attention
[22:12] to the answer if you gave it, but how far along Oh, you said that he has a functioning site.
[22:19] Yeah. So the code, the code base is fully functional.
[22:23] Yeah, it is. It's command line at the moment.
[22:27] So it's it hasn't solved everything. It's still command line, you still need to be familiar with cloning a GitHub repo and
[22:32] then loading and then I don't even know it. Yeah.
[22:35] It's all NPM and starting NPM and it is written in that but it is it's a single package now. So instead of having when it first started, it was there was a video package and an audio
[22:47] package and a text package. And now those are combined.
[22:51] So you only have this the one package and then there's individual uploaders still but as long as you're familiar with that, and that's I, I have gone through the pains of
[23:03] doing one of those just as part of the QA process and to familiarize myself with it. And so even I was able to figure out how to load it up how to how to see and utilize the
[23:16] the platform reference the I don't even know what that the platform document how to know and utilize the platform document and then use that just to do a little really quick
[23:27] hello world since then things have changed. So I can't show it to you because this might be an interesting thing for our other developer
[23:35] Anthony who is a web to connoisseur and just very good with Anthony Campolo. Maybe he could take that and do a demo of of what this is and see how it see how it
[23:50] functions. So maybe there is a there's a task on the card to do exactly that to go through especially
[23:57] to go through the the how to the how to doc that Israel created for us and to create a small just hello world something and with a couple of different assets.
[24:09] So it's not just one text but you have a couple of different things just to go through it more than once and look for does it fall down on any of these other places or thing or how
[24:19] can the instructions be made more clear especially more clear to someone who's not as technically smart and as technically well-versed as Israel is that's one of the difficulties of what
[24:35] he's built is that it is in some ways it's very elegant which means if you if you don't know the bones and the foundation of what it's built on it can look like it can look
[24:46] like it's gibberish. And one viewer just asked how does one use ipfs is that I'm presuming the question means
[24:56] like is that a download or how does one get going with that is that a command line thing also that is so that's built into the package fortunately because I don't know how I don't
[25:08] know how to use ipfs I know that you it is my understanding is that you load you load the file and then it stores that file across the nodes across the networks.
[25:20] And so anyone you're a node like do you become an ipfs node you can be an ipfs node you don't have to be and if you are an ipfs node then I believe that there are that there are rewards
[25:32] off that chain for having a node and the rewards are based on like how large you make it and then how what kind of uptime you have if it's like me where you turn off your computer every
[25:42] night then it's not as much reward as for someone who keeps your computer on. There's a blockchain related to ipfs yes oh there's a blockchain and there's also a coin
[25:58] so there's there's the ipfs which is the protocol interplanetary file system we haven't actually said that name but that's what oh that's right I forgot the planetary bit that's my favorite
[26:10] part about it actually though is it's interplanetary yeah so that's just a protocol but then there are other things that are built on top of it and and that's a neutral protocol but then
[26:22] the other thing on top of that is file coin so you may want those are those are built by the same same organization I believe it's protocol labs actually I have a good friend
[26:35] that works for protocol labs so that's the incentivization layer on top of the protocol so ipfs you can think of as like http as a protocol as far as I as far as I understand
[26:54] I haven't dug into it but then there's that the blockchain file coin coin as well on top of that so well this is I guess to me the big decision that we have to make is is whether
[27:10] we whether and how we keep funding this project because like we said you're out of funds you you did have some funds but not a lot to work with and then we you didn't have you you withdrew
[27:25] your proposal in favor of at least having my proposal pass as well as giving - core group some more room to request some funds so there's a big big challenge right now and
[27:40] hopefully we have a solution to this in the future but but yeah I guess we'll have to make some decisions about whether whether we yeah how we keep this funded or just leave
[27:53] it as is and hopefully maybe that's the other option is yes code and people can just take that and run with it on their own and the next the next request on this is to put together
[28:06] a small web interface for it so that it doesn't require cloning a github package and doing everything command line yeah and but that's that that is that would be the next okay I've
[28:20] got a bow on it and it can sit this way I can sit the way that it is right now like I said the the package is functioning the difficulty comes in a platform changes so
[28:29] if there are any structural changes apply what you know that have an impact on what on the mechanics that are in use now one of the difficulties with the project has been
[28:41] it has been two or three steps forward making progress and then platform will change then everything needs to be or many things that need to be rewritten research needs to be
[28:50] done again in order to keep it in order to keep it up to date and part of that is there was an early assumption that the changes the platform wouldn't be as dramatic as that each
[29:00] time and that was an incorrect assumption and like that's yeah the risk of doing development on something that's in development yeah exactly so we I know that we will at least have one
[29:15] more change to platform because we right now on testnet which is what this developer is is building on that's running platform version 0.24 and that's where there's some javascript
[29:30] stuff on the back end still and the big the big rewrite of from javascript to rust is version 25 0.25 and that's going to be coming out soon if not already I'm not 100% sure
[29:48] if actually testnet might be running platform 0.25 already I don't actually know that but probably somebody else does but if it does if it is running 24 then then we'll have one
[30:00] change more to deal with and hopefully that's that's it but who knows so anything else to say about this this project I don't see any other questions in the comments section but
[30:16] anything else to say about this other than you know the the codes out there we gave a link to it and you're welcome people are welcome to use that and try it out no I don't are
[30:30] than I have I have a lot of hopes for it I think that this is one of those pieces that creates the kind of accessibility that's needed for platform to hit like a network effect
[30:45] of users using it so that usage takes off and we can see and we can see some dash performance that we've really been itching to be able to see as far as users and the the quantity
[30:59] of transactions and the use of it as a daily as a daily thing yeah Balazs just says test that's not running version 25 yet so so yeah that confirms that what I was what I was thinking
[31:12] that will happen this will still work for you if you go and test it now it'll work now and then when version 25 that comes out it may or may not work depending on if he's using
[31:23] apis that that change but yeah I echo your comment there about trying to get some like applications that actually require - I I know that just through my through my work my research
[31:40] with web - of just what kind of businesses are making money in web - a lot of those are CMS's and if we could create a very good very easy user friendly decentralized content management
[32:01] system built using - platform for structured data and leveraging IPFS for heavier image and and video related data that has a huge market so charge - for that for the use of
[32:20] that then then we've got a very good product so hopefully yeah and especially the thought just strike the thought just struck me that especially as we move more and we're beginning
[32:31] to see real practical functional applications of augmented reality and that is going to require the ability to access this data on the fly outside of a traditional web interface
[32:46] as well and it feels like this is that is a prime opportunity for using for using the platform documents and IPFS storage grand okay well as we close out today we want to
[33:06] be sure to announce that both the dates and the location for the upcoming - retreat in Utah have been selected so the dates are Friday September 29th through Sunday October 1st
[33:26] and the location is the Salt Lake City public library I think it's called the city library you know on Google Maps perhaps and so more details about the agenda and parking and you
[33:42] know where where we may all go eat lunches together and things like that are currently being like discussed if you want to you know join the discussion on a newly created server
[33:56] for this purpose we'll put the link to join that server in the description below but if you'd rather just wait for those details to be posted and you know no need to join any
[34:07] discussion you can have confidence that we will post them in the coming weeks so yeah yeah I'm looking forward to that we're gonna do it regardless of I know that it's difficult
[34:21] to get out to Utah for a lot of people that are from out of town but we'll try to make time and we're gonna have a good meetup just amongst us our little Utah crowd of which
[34:34] we are all part in this conversation and there's there's a lot more of us but yeah that that should be that should be a good little just one one comment on the it's called a it's
[34:47] called a retreat I I had envisioned maybe doing something a little bit more like a retreat like getting up into a cabin and just spending a few days together but logistically it just
[34:59] made more sense to have it very accessible from the Salt Lake airport and so we decided to to do it at the library and I think that if you are coming from out of town it should
[35:10] be pretty straightforward how to get there and it won't be you know a huge trip for you to get to go then beyond that and get into some mountain area which I would like to do
[35:21] but not this time so maybe in future and then also for anyone who's interested but won't be able to attend in person we are actively exploring live streaming not only at least
[35:39] some of the presentations there and some people don't want me to call what when they're talking a presentation la la la I'm still calling it that so we'd like to live stream at least
[35:48] some of the presentations as well as have a sort of you know whether it's via Jitsi or Zoom like discussion where if you're interested we can all hop on a call together and have
[36:02] a discussion so stay tuned for these kinds of things if you'd like to join us and on that note that wraps it up for us today let us say farewell fellas yes all right yeah
[36:15] thanks thanks everybody and we'll we'll talk later and see you in Utah okay