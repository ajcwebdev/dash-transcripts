Ash, Mikhail, Rion, and Anthony join the show to discuss the new Dash Incubator Quarterly Report covering the first quarter of 2024.

tl;dr: In this episode, the Dash Incubator team reviews their progress in Q1, including work on a web wallet, Dash Platform contributions, payment/merchant tools, and web framework integrations. They discuss strategies for Q2, focusing on courting web2 developers, attending conferences, improving Dash libraries and SDKs, and continuing work on key projects like DashPay and Dash Platform. Challenges and opportunities around developer outreach and improving Dash's reputation in the web3 space are also examined.

00:00 - Introductions and Dash Platform Testnet Update
The episode starts with an update on the latest Dash Platform testnet release, which is ready for testing and aimed at onboarding new developers.

02:56 - Quarterly Report and Q1 Project Funding Breakdown 
The host shares a breakdown of the projects funded in Q1, with the majority going towards a modern web wallet, followed by Dash Platform contributions, payment/merchant tools, web framework integrations, and strategy/research work.

11:09 - Strategies for Web2 Developer Outreach
The team discusses the importance of researching and engaging with the rapidly evolving web2 developer space in order to improve Dash's reputation and demonstrate the value of Dash Platform. Attending conferences and networking with key influencers is highlighted as a key strategy.

32:03 - Team Member Updates and Q2 Plans
Ash and Mikhail provide updates on their Q1 progress and shares their plans and funding requests for Q2. Key focuses include the DashPay extension wallet, Electrum Dash wallet, Dash Platform libraries/SDKs, and developer outreach.

62:19 - Q2 Budget Planning and Closing Thoughts
The host walks through the team's budget planning spreadsheet for Q2, explaining how funding requests, spending projections, and strategist rewards are calculated. The team shares closing thoughts, emphasizing their excitement for the quarter ahead and key priorities like the upcoming DashPay launch.

---

[00:00] I'm just going to join with a second PC that's going to share my screen. Okay. Yeah. Sounds good. I think we're live guys. Um,
[00:08] welcome everybody to the, this, this month's, uh, this quarter's, um, report and outlook report for Q1
[00:17] outlook for Q2. Uh, thanks for joining me, Mikhail and Ash and, uh,
[00:23] our cohost Anthony. Okay. So we are,
[00:33] it's pretty exciting quarter. I think. Um, I'm actually, I got excited, uh, with, I should share this on my screen, but,
[00:44] um, I don't know. Can I share two screens? Let's, let's try it. Um, let's try adding not that one. That one's coming up. Oops.
[00:56] Oh, no trains. Let's see. I want to present, uh, share screen again.
[01:05] I accidentally removed the one that I want to share. So I'll share that again, but we won't be talking about that one just yet.
[01:14] I want to see if I can share two screens. Oh, it's just one screen. You can share two screens. Yeah. Well, the only one was,
[01:24] yeah, I was just going to, um, talk about the, the tweet that just went out from a quantum explorer, basically saying that,
[01:33] um, that the, the version of test net, um, that's ready to be tested and possibly even,
[01:43] um, abused is, is out right now. It's been out for a day or so. Um, Anthony,
[01:51] you and I tested it a little bit on stream. Was that yesterday? Was that two days ago?
[01:57] It was Saturday, Saturday, two days ago. Yeah. So we tested it. Um, and we got through the part of the tutorial, uh,
[02:07] that is for new people working on dash platform, just fine without any bugs other than that one bug that we didn't have enough
[02:15] credits. So that was more of a tutorial issue than, than anything else, uh, network related. So, so far, so good. And hopefully everybody can,
[02:24] um, join and, and test test net, um, try to break it as Sam would say and try to use it. Um, so that's,
[02:33] that's really exciting. Um, and it's exciting for us this quarter, cause that's going to be a big part of my strategy going forward.
[02:39] This quarter is to try to get, uh, several new people that may know nothing about dash or even cryptocurrency for
[02:47] that matter, uh, using it, trying it out as traditional web developers,
[02:52] but I'm getting ahead of myself a little bit. Um, any opening remarks, Ash, or Mikhail that you wanted to just get out there?
[03:00] I mean, that's great news. Um, that's a, that's what we want to hear. I'm sorry. One second. My, uh, I love PC. I think it's, uh, audio is coming through. Um,
[03:08] yeah, I think that's great news. I think that getting tested at this point where we're ready to sort of bring
[03:13] developers in with a kind of step-by-step guide that's more open and, without them having to debug a load of things without them,
[03:19] unsure of test nets going to be reliable or not. Uh, it's a really great step. And I think, uh,
[03:24] I put a comment even on the dashboard yesterday or so that we really just need more developers, even if it's just hobbyist,
[03:31] even if it's people that aren't developers and they're just running through the tutorial and they're testing it because they're going to run into those errors
[03:37] as user experience sort of flaws where they can suggest revisions. And we just need more independent developers, uh, whether they come, uh,
[03:44] just voluntary, whether they, um, go by the incubator directly to the network, you know, just any, any developer,
[03:51] even anyone in the dash community that has a tiny interest in this should go through that tutorial and, you know, various different tutorials.
[03:58] There should be out there. Um, we should onboard them and encourage that as much as possible. So some good news.
[04:03] Any opening remarks while I'm going to actually find that tutorial on. So, uh, Mikhail, anything to say about that? Cause I, I did want to bring up,
[04:15] uh, the helpful tool that you built along the way as well. So you're, you're muted.
[04:22] Uh, well, yes. Uh, I'm excited about new platform version two, because, uh, as quantum said,
[04:33] we're supposed to kill it to destroy this platform and test it all the way. So some developer tools
[04:44] that, um, uh, they're working on. So, uh, so yeah, um, I want the stuff to do a lot of, uh,
[04:54] things that, uh, that we, that we can do and yeah. Yeah. Um, so the, go ahead and let's, let's share my screen.
[05:07] Okay. It's already there, but it's not. There we go. Cause you have to be on the view that also shares the screen.
[05:17] So gotcha. Okay. Yeah. So this is, uh, let's see, that's not it actually. Um, let's go platform docs.
[05:26] This is what we're talking about right now. And, uh, I will caveat this with,
[05:31] I think a dash core group might need a day or two to get the latest version of, um, yeah,
[05:40] get the latest version of dash core running on a test net before anybody really tries to hammer this. That's one thing that I saw in the chat. Um,
[05:52] so anyway, this is, this is the, uh, the tutorial that we're talking about connecting to the network,
[05:58] creating funding wallet, this, this little, these steps right here, um, identities and names has a bunch of sub steps. Uh, Anthony,
[06:06] you and I have gone through this, um, uh, a few times and had several bugs before, uh,
[06:13] two days ago. But like we said, two days ago was, it was all good. Um, and yeah, so that's, that's what we're talking about just in case anybody's
[06:23] wondering. And we do have a video of that. I'm going to, let's see. Oh, that's not the one I was looking for. Um,
[06:32] dash a youtube.com/dash at dash incubator is our YouTube channel. Subscribe. Um, and yes,
[06:42] the, the stream that we did about that was right here in the live.
[06:50] If you click on live, we're going to be doing a few more of these. So I, that's why I wanted to show people how to get here. Um, we do live streams,
[06:59] coding live streams and just a documentation review live streams. This is the one that we're doing right now. So this is, this is the series,
[07:07] this end to end dash tutorial, um, series was what we were talking about. So now let's go ahead and get into the,
[07:15] the quarterly report and discussion about what, what our strategy is going to be, uh, going forward as well. So, um,
[07:25] I will go ahead and start, let's see. Are we, yeah, we're on my screen. So in this quarter in Q1 last quarter,
[07:35] so looking back to from the previous quarter now, uh, I funded nine projects and the vast majority of my funding was for the modern
[07:44] vanilla web wallet. This is, this was my focus last quarter and will probably be a focus this quarter as
[07:57] well. Um, but maybe not the primary focus this quarter. Uh, but last quarter, uh,
[08:08] we did spend quite a bit on this. There were several issues that, so we, we had about five people working on this last quarter. Uh, the,
[08:18] the most, the bulk of it was, um, obviously the lead developer, uh, Jojo bite and myself and AJ and two other random,
[08:27] uh, testers were alpha testing it. We did run into several user experience type issues that required us to re
[08:36] architecture a few things and just like the flow. And we ran into some bugs that we needed to fix that required library updates
[08:45] and whatnot. So this was a little bit more than I wanted to spend last quarter. Um, especially considering the progress that we have so far.
[08:55] But this is, I think one of the most important things that we can be working on is having a
[09:01] great web, um, wallet with integrations into crowd node and, um,
[09:07] Maya and different, um, dash spend is, uh, I wanna ask, ask Ash about in the call later today.
[09:15] So we'll be doing those three integrations this quarter. Uh, we didn't want to get to some of those last quarter, but again, ran into some,
[09:22] some issues that we needed to, uh, tackle. Um, the next one down dash platform contributions. This was mostly AJ,
[09:32] um, basically trying to get platform, um, all the platform components working together and built without using dash,
[09:42] using Docker. And we were able to get that successfully completed in terms of, um,
[09:48] getting all the pieces talking together and built together. Um, we, I don't know if that's going to work with the current, we do need to update,
[09:58] update that with, uh, the latest dash platform, um, uh, test net and testing it to see if all the pieces are still talking together.
[10:08] Cause there were some significant re architectures on dash core group side that, um, may affect what AJ was doing. Um,
[10:18] and we're going to, I think right now is probably a good time to look back into that again, um,
[10:25] to see if, uh, if we have all those pieces talking to each other again, and then we would want to script that in a way that's makes it easy for,
[10:33] um, for masternode owners, um, specifically, uh, Evo node operators to easily spin that up,
[10:44] uh, without using dash made or Docker if that's their preference. So that's, that's one of the main focuses from last quarter. Um, and then the show,
[10:53] the next thing on the list was this, the show basically where we have various people coming in and talking about what
[10:59] they've been working on in the incubator. And, um, this is going to be, you know, we're going to continue this show, obviously.
[11:09] And I'm going to, I want to this quarter, um, also have more videos that are not on Monday at 10 o'clock.
[11:18] My time. Um, 4:00 PM I think is a UTC. Uh, I want to do some during the week as well. And then that's going to,
[11:28] um, that's going to, I mean, I'll talk about that a little bit later. That's part of my strategy. So the next item is the strategy.
[11:37] And I'll say that one of the main things, this is like the bucket that basically covers everything that's not itemized as
[11:44] a specific project. This is basically my time, um, figuring out what we should,
[11:50] what we should be working on and, um, researching the one,
[11:56] the main thing that I've been doing with this, uh, with this particular line item is researching the web to space.
[12:04] Um, in depth and getting myself to a point where I am very conversant with the current technologies of web development so
[12:14] that we can approach those web developers, um, and have conversations about how dash platform into their technology stacks.
[12:22] Um, and Anthony, I've been talking for a while, so I'm going to invite you to say a little bit about that. Um,
[12:29] it is a project that you've been working on. I'll talk about that. This is the web frameworks integrations. Um,
[12:36] but I want you to say a little bit about that now, just to, to give me a little bit of a break for one.
[12:41] And I think it's relevant to this strategy line as well because, um, it takes a long time. It's,
[12:47] it's kind of a full-time job keeping up with the web to space. Um, so, and it's, I think it's,
[12:54] it's very important strategically that we court these developers in a way where we're speaking their language and we know what technologies they're using because
[13:04] a lot has changed since, uh, the time that dash platform was envisioned and we have now in the web to space
[13:12] and how that might be integrated into their stack. So can you talk a little bit about that? Um,
[13:18] yeah, if you think historically, I think dash probably came around when react was just first invented.
[13:27] So as you said, a lot has changed. And, um, for us, I think what we've really been focusing on is getting first actual,
[13:37] like good front end examples created so that they have something to instantly spin up and work with and then do things like live streams and pair coding with
[13:47] other people who are in the web to space who are maybe popular streamers themselves and both to kind of get exposed to a different audience,
[13:55] but also to just get their feedback and hear how it is working with it. And we were talking about, you know,
[14:01] context and knowing what they're going to expect. I think knowing kind of where they're coming from and how they expect particular
[14:10] things to work is always interesting when you talk about web to a web three. And if you can kind of hide a lot of the kind of web three decentralized
[14:22] messiness from them, then you can make it basically as good of an experience.
[14:27] But it does take a lot of thought and time. But, um, yeah, I think it's something that, you know,
[14:33] I have been hosting a podcast about like all of these front end frameworks that have been going on for a while.
[14:40] So I definitely feel like I have a pretty good handle on like, what are the frameworks in terms of like how to actually convince a web to
[14:47] developer to want to do web three that's almost like a philosophical question to a certain extent. Cause you know, if they're not already into it,
[14:57] they may not really even know what the benefits are, why they would want to do it and be able to also kind of pair all of that with
[15:05] the tech is really important. Yeah. Just to highlight that a little bit. Um,
[15:10] what we're talking about here is, you know, stick, taking a step back, uh, the past few weeks in incubator weekly,
[15:19] we've talked about our topic has been, so three weeks ago it was, um, exactly the name escapes me exactly,
[15:28] but it was like dash platform for web developers or something like that. Yeah. We want to build, um,
[15:35] web applications that are decentralized web applications, so-called daps and what people need to know in the dash space,
[15:43] like masternode owners and community members in the dash space is that all front end web development, it's a very evolving space right now.
[15:53] It's kind of surprising if you're not researching it in depth right now to find that out that like, Oh wow,
[16:00] the traditional web space is still evolving very rapidly actually right now. Um, and so when we're talking about building daps,
[16:09] we have to remember that the front end of those decentralized applications are traditional technologies and the way that the space is going right now,
[16:17] we have these, uh, frameworks as you see here, here in the URL bar. Um, these are, this is best of js.org.
[16:25] It just kind of gives an idea of what people are building with. So you have react on the top, you have view, angular, Svelte view,
[16:34] um, uh, preact, htmx is a new kid on the block. Solid is one of my favorites. Um,
[16:43] that's focusing more on reactivity. Um, and the, these, these other front end frameworks, there's just a lot of them. Uh,
[16:50] quick is relatively new. Uh, lid is very lightweight and pretty cool, but I want to build integrations with,
[16:58] with all of the ways that web two developers are accustomed to. And so that it's very easy for them to, uh,
[17:07] use our technologies. So not asking them to come into the web three space, but asking, uh,
[17:13] but facilitating us to come into the web two space in a way that's, uh, familiar with them. Uh, if you,
[17:21] and maybe like other guys, uh, Ash or Mikhail, jump in if you want, if you have anything to say about this particular topic, but, um,
[17:30] I feel like there's a, there's a significant reputational damage that, that, uh,
[17:38] that web three has faced, um, which is our, our, our scene. Uh, I don't like to call it web three necessarily,
[17:45] cause I think it's creates an unnecessary divide, but that's what the industry has called us. Uh, web, web three,
[17:53] uh, basically bringing blockchain technologies into a full stack development of
[17:58] decentralized applications. Here's another view of that just by the way, that I don't know if we're still looking at this, my screen,
[18:04] but you can see like different trends. And so this is, um, like people put a lot of stake into this idea of like front end frameworks.
[18:14] Um, and I just wanted to give the audience here a taste of that because it takes a
[18:22] lot of time to research these and to get acquainted with the communities, the key players and influencers in the, in these various communities.
[18:31] And that's what, um, I've been trying to research. That's what I've, I'm bringing Anthony into the incubator for he's been in for a while,
[18:39] but it's, it's for this reason, because he's, uh, he's got some experience and has rubbed shoulders with a lot of these
[18:48] communities. So, uh, but what I was, what I was saying to close off that, um,
[18:55] that thought was that in this space, in this front end, uh, traditional web two developer space,
[19:02] I feel like they have a bad taste in their mouth for crypto and web web three stuff.
[19:10] And we need to do everything that we can including, but not limited to financial incentives to help bring them like to clear our name
[19:20] essentially and say, Hey, we were actually, we at dash, we, we are trying to build something that actually has value and that actually is
[19:33] useful for you as a, as a traditional developer. And it not until they, until they realize that,
[19:40] that we have something that's that we're offering them, uh, that actually has real utility and is not just some pump and dump scan scam that
[19:48] they have heard about. And that is really their primary, um, their primary perception, perception of this whole space.
[19:58] We need to help overcome that. And it's going to take some time to do that, I think.
[20:05] Yeah. Yeah. I'll just say it quickly and then we can switch. Yeah. I, we encounter this a lot. Like when I first got into web three,
[20:14] I went on a lot of podcasts cause I had come up through web two and then a job doing web three and then it kind of went on all my friends podcasts or most of
[20:21] them, like I would contact them. And some people were just like curious and just, you know,
[20:26] want to learn more cause they've been hearing about it. They don't really know anything about it. And some people were just like, nah,
[20:31] I don't really want that on my show. So there, you can kind of gauge people. Like some will be very anti, some will be, you know,
[20:38] maybe a little suspicious but open to it. And some will be like, eh, I'm just curious to learn more. But, um, if someone's already into it,
[20:46] you probably know already. Yeah. So I think, you know, I could talk about this for probably, you know,
[20:53] multiple hours. Um, but the, in terms of it, there is, there's a lot of different parts to it. Um,
[20:58] there's one part of it is that obviously the community building side and how passionate that community is. And you look at people like the T3 and just how big
[21:06] an audience they're able to cultivate and how people follow them. They'll follow tutorials. They'll build, you know,
[21:12] their Airbnb clones that are either clones and they'll take part in that world. But also like you say, there's this divergence in terms of, you know,
[21:20] what we're building and where the sort of web two space is and opinions of crypto versus, uh, this side of things. Uh,
[21:27] but then there's also a massive overlap between people working on these things or not necessarily working on these things, but working with these things.
[21:33] A lot of the crypto apps are using, you know, modern front end development frameworks or, you know, uh,
[21:38] let's say full stack side of things, whether it's next or, you know, some, something like that. And it's like,
[21:44] how do we bring the two together and actually offer value to those developers? And for me, I kind of see it in a way, kind of like a headless CMS, uh,
[21:53] for a front end developer to build application logic into their front end by using a tool like platform. So they're not hosting databases,
[22:01] they're not hosting a server, they're using platform for that. And where, how do we get to that? Is that case of,
[22:06] it's kind of like a gap in between the two right now. Is that a case of tooling? Is that a case of, you know, uh, different layers, integrations, um,
[22:14] and part of that, like you say, is being part of that community, um, and working with those sort of senior developers to introduce, um,
[22:21] these concepts into their sort of existing platform. Yeah. And another thing to say about that is that the, uh, the space,
[22:29] the web two space has changed a little bit, unfortunately, uh, to some degree in that, um, five years ago,
[22:38] the single page application was all the rage. And now people are moving back to the server side for their application
[22:46] delivery, um, server side rendering and hosting, um,
[22:53] your database on, you know, in servers instead of having API APIs. Um, and that's a little bit of an unfortunate trend for us, uh,
[23:03] for what we're delivering because, uh, what we're delivering was ideal for the single page application, uh,
[23:10] architecture, but I do think that the industry is going to start swinging back. You know, it's like a pendulum.
[23:17] It swings front end back in front end background every few years. And I do think that there will be probably a swing back to focusing on the front
[23:26] end and single page applications and using APIs and SDKs and things like that. Um, and we'll probably be in a good position for that. Um,
[23:36] and I think one of the main reasons that people are swinging back to the backend is that you have a lot of VC backed companies that are needing to get revenue
[23:45] and they get revenue from, um, doing storage and hosting and, um,
[23:54] computation, um, execution on their platforms. And that's, um, you know, that's understandable, obviously, like they,
[24:04] it's, it's good for them to, to get paid, but that's also what we want to take a part of, um,
[24:10] having people do that storage on our backend, essentially. So we're going to have to, you know,
[24:16] we're going to have to have a great product. Can we drop in and replace Mongo DV? Like how easily can we just straight up be
[24:23] like, yep, this is a decentralized version of a Mongo DV. We've made it really simple for you guys as devs,
[24:28] whether you're using next or another sort of a server side rendering. Um, you know, JavaScript based TypeScript based, uh, framework, you know,
[24:37] and then it's like, okay, yeah. Okay. Decentralized storage is, it's something, but really the value is in that decentralized application logic that when can we
[24:45] introduce that back in? Like how can we get that first bite, uh, open offer in the door and then, you know,
[24:51] there's other features that you can use here. You know, it has to be, it has to be easy and a gentle slope. We can't say, Hey, here's platform.
[24:58] You can do all this stuff with it and expect devs to be just like not, you know, immediately walls come up for most steps. I'm not saying,
[25:05] I'm not saying there aren't people that will persevere and put that effort in to overcome that first like learning curve. But there are a lot of people that,
[25:13] you know, will immediately be deterred, um, by a huge barrier in terms of new knowledge and new functionality and
[25:20] capability. I think platform already, we struggle to communicate the value of, um, so it has to be graceful and gentle.
[25:26] Yeah. Yeah. I'm going to ask you three to, to, to have a little banter while I go get my cup full of water again.
[25:35] And then I'm going to continue down my list and then we'll, we'll move on to, to, uh, Mikhail, uh, after that, and then Ash after that.
[25:42] So I'll be back in one minute. Literally what's everyone's favorite new TV show.
[25:48] No, let's talk, let's talk platform. Let's talk, talk development. Um, you know, Anthony, uh, Anthony or Anthony, um,
[25:56] Anthony. Yeah. I mean either. So my, my, my cohost calls me Anthony. He's from the UK. Exactly. Uh, there you go. Um, you know,
[26:04] in terms of this, how do you see us getting that earlier sort of penetration with
[26:09] developers who aren't familiar with platform? So not so, or even crypto, someone who's a web to developer pretty, let's say early,
[26:16] they've been working for a couple of years, a few years, mainly front end, maybe they played around with a bit of next node, whatever. Um,
[26:23] how would we get them on boarded to platform to, to even a basic degree? Yeah. Big open topic.
[26:32] Yeah. I think, um, we, I kind of hit on some of it high level earlier, but, um,
[26:39] I think first you just want to make sure that you're going to like have a very, very simple functioning working tutorial that you can,
[26:47] that is almost impossible to not be able to finish because especially when it's new tech,
[26:52] if they hit a weird bug halfway through and they had an error, they don't understand and they don't know where to look up stuff and they find
[27:00] different versions of docs and all these different repos. Like this is especially a problem when you have a huge decentralized project
[27:07] with lots and lots of resources, some of which have been created over the course of 10 years.
[27:10] So having that really good golden path, like a Ruby on rail style experience of just like,
[27:16] do you think like a, um, like an in browser, um, you know, terminal side of thing,
[27:22] or do you think people should just use their own dev tools? Like how can we, you know, uh, like, uh, what's the code that people use to code?
[27:29] Like it starts off with just like a terminal and you can just do it. Yeah. You're talking about things like replet and code sandbox and yeah.
[27:36] Yeah. I mean, you could actually use their tooling. I'm pretty sure they allow you to, you know, kind of use that. But like,
[27:41] like, like I'm saying, can we do a sort of developer, really clear developer funnel where we've got a, you know, in,
[27:48] in browser terminal and, uh, some sort of persistent storage, uh, however that's working, uh,
[27:54] how could we do something to make it really entry level? Because I think every, every,
[28:00] every little point of friction is a drop off point for developers. Uh, you know, how would we do that?
[28:05] No, I agree. And it's definitely possible to like the, the examples that I'm creating right now,
[28:11] you could run in like a stack blitz or code sandbox or get pod. There's, there's whole, there's a whole bunch of these.
[28:18] They come integrated with CLIs and then once you get the front ends that you can set up the front end and the main thing is getting test net
[28:27] funds. That is like the big thing. That is the huge part of the tutorial that will, that will get a lot of people. So, um,
[28:34] so can we just literally need to set it up? Yeah. Do we need to set up a faucet that just uses, you know, I hate to use like Google,
[28:41] but like recapture or whatever, can we just do a, or a JavaScript proof of work faucet that has significant levels of funds?
[28:48] Like this should not be a problem. Like running into this, uh, like when I use the faucet, I have to use the code mass node.
[28:54] Then I send it out to a little other, um, wallets to actually continue using it.
[28:59] I know we set up our own sort of faucet ourselves for our development here, uh, for our own, obviously you have your Genesis, uh,
[29:05] mass nodes and all that kind of stuff, but this needs to not be a problem. It cannot be that.
[29:11] I know it is a problem in Ethereum and stuff that you have to go and find some faucet somewhere that, you know, it's,
[29:16] they're often run by these blockchain as a service companies where you have to have an account with them. It's a mess.
[29:21] This should not be a barrier for developers. We need to have a faucet that has some JavaScript proof of work to prevent it
[29:27] just being spammed and emptied and just continually mining and adding funds. I don't care if the, you know, the, you know, uh,
[29:34] incubator is running miners on test net or whatever it is. You know, we just need to solve this problem permanently and never have to worry.
[29:41] You're saying that because I said the exact same thing on our last stream. Yeah. And actually the one funny thing is one of the first actual development
[29:51] projects that I worked on in the incubator was, was to try to solve this problem. I, I made a little app that, um, basically would,
[29:59] was a very streamlined, um, faucet and it, it did some basically IP checking to make sure that it wasn't being abused.
[30:09] So maybe we'll have to resurrect that, um, or that makes something better. But yeah, it's just a problem. Yeah. So let's go back to my list now. Um,
[30:18] I want to, I want to finish this up real quick so that we can get onto the other ones. Um,
[30:24] so payment tools and merchant tools, we did some work on this. This is, this is dash bread and butter stuff. Um,
[30:33] I, part of this was, you know, when we, when we're making the web wallet, uh,
[30:40] we're using incubator tooling for the payment tools. So we have our own, uh, libraries and SDKs that are very, very lightweight,
[30:49] very, very, um, efficient. And we need to do some work on that. Um, merchant tools,
[30:55] this is always going to be something that I will make room for if, if there's an opportunity. So, uh, we did a little bit of that last quarter, uh,
[31:05] the merchant credit loyalty credit system that's still a work in progress. Um, and, uh, I'm not really driving that one,
[31:15] but I am funding it when, um, when the developer, uh, is, is working on it.
[31:22] And I know he is continuing to work on that. So we'll probably see a little bit of that next quarter as well. Um,
[31:28] web framework integrations. We just spoke a lot about that. We didn't spend a whole lot of funds on that,
[31:32] but this will probably be our number one or two number two. It'll be in the top three, probably this quarter, cause this is,
[31:40] this is going to be one of my focuses. Um, and then just this that dash incubator org is just miscellaneous stuff that we
[31:48] spent, um, infrastructure or some kind of spreadsheet updating or something like that.
[31:53] Some internal, uh, funds for that. Um, Mikhail, do you want to jump in and talk about, I'm going to switch this,
[32:03] uh, well, I guess I'll, I'll show this little pie chart real quick, just so that people can see the distribution of that. I'm zoomed in here.
[32:10] So maybe I'll zoom out one more. Um, that's, you'll see this in the report as well.
[32:16] So I'm going to switch this to your projects and go ahead and talk about them. Uh, sure. Um, so there was, uh, some work, uh,
[32:30] can you, can I get the, uh, yeah. So, yeah, um, that was quite work on the Electrum mostly.
[32:40] Uh, so what we've done is, uh, the major features is that we recovered private send feature into the wallet and
[32:49] recovered, uh, Electrum dash org, uh, website, not the original domain, but we, we got a couple of others.
[32:59] And, um, and we built it, uh, on the next GS, which is, uh, server side rendering, which was, uh,
[33:08] which we were talking about, uh, recently. Yeah. And that allowed that allowed the website to be indexed into the search engine
[33:18] optimization in the search engines. Uh, and, uh, and yeah, and we already can see that, uh, if we Google Electrum dash wallet,
[33:28] uh, then, uh, sorry, I didn't mean to distract with this. I think this is just my,
[33:37] my office space has some kind of issue with your certificate. So, uh, it's a shame that we can't show that. Cause it was, it be,
[33:45] it was very useful in our stream two days ago. Can you not just get past that with the proceed, the advanced?
[33:51] You need to go ahead and do that. I'm dangerous. Okay. So I mean, you're not doing, uh, uh,
[34:00] duh, duh. Yeah, you can, I guess. Through the icon on the, not, not secure. So this normally works for me.
[34:10] Oh, basically, uh, the benefits of this, uh, website done via next GS is that we can,
[34:20] we can get the website in the search engines. And when the people searching through the Google, through other search engines,
[34:27] they will get results. And if we Google like dash, Electrum or Electrum dash into Google,
[34:33] you already can see that, uh, is there in the search results. Yeah. Can you do this real quick? Uh, right in place. Where do I go? Yeah.
[34:41] Just definitely from Electrum dash. Dash Electrum wallet. Okay.
[34:47] It should be there. Uh, uh, a bit, a bit down. Yeah. The second, uh, I believe is that what, what, what we have. Yeah.
[35:00] This is the website. It looks like it was a react app. You got the react logo there here again,
[35:08] probably the same issue. Yeah. So basically, yeah, it's working, but yeah.
[35:14] Yeah. So it's there in the search results. And that's the most important thing because when people be searching for the
[35:24] wallet, they first will be typing in it into the search engine to get the link to the download wallet and stuff. Um, yeah.
[35:34] So that's the main features, uh, that was done through Electrum dash, uh, concept project.
[35:41] And, um, we also maintaining, um,
[35:47] Shenmue dev infrastructure that allows us to, to keep the infrastructure for Electrum web servers for platform explorer.
[35:58] Uh, what else are the results? There are also dashboards for checking the monitoring status of the services.
[36:05] Um, yeah. Um, so that's basically, yeah. For, for the infrastructure, uh, for, for running the projects, uh, that,
[36:16] that we've been, that we will be doing. Um, there was also some work on the any pay app, uh,
[36:24] which is, um, so custodial payment, uh, uh, payment tab that you can use to,
[36:33] to accept payments in dash and Bitcoin or any other. So what we've done is we upgraded it to the latest SDK,
[36:40] Dart SDK, uh, to Dart free, uh, which introduces, uh, sounds no safety. Um,
[36:48] and also we've done some work on changing, uh, back into URL, uh, and, uh, something, uh,
[36:57] and we did the page, uh, something like about that, that shows the info about the application and the build number.
[37:04] Um, yeah. And the platform explorer, uh, of course, um, uh, there was some work, but mostly like, uh,
[37:16] maintenance, um, uh, I have added, um,
[37:22] some missing info about some system entities like system documents, system data contracts that, uh,
[37:29] that weren't available in the platform explorer. Um, the thing was the thing is that, uh,
[37:36] we basically have things that are on chain and there are some entities that gets, uh,
[37:43] populated off the chain, uh, before they actually blockchain starts, that's called sign any chain. And on the senior chain,
[37:51] there are several system system entities like, uh, documents, system, system data contracts and stuff like that. So, um,
[38:00] I have faded this information to platform explorer and, uh, and yeah, uh, on each, uh, platform network upgrade,
[38:08] I ensure that everything is running and just upgrade to the latest versions, to the latest network, uh,
[38:16] updates and stuff like that. Uh, and yeah, and the last one is this current contributions that, uh,
[38:23] is done by a crypto tour. Okay. Sorry. Um, and, uh, yeah, and, uh,
[38:34] yeah, those dashboard contributions are, um, uh, done with, um, past, with, uh, from the,
[38:45] with the DCG, the pastor from the DCG, the VJ, the name of the developer is a VJ.
[38:51] Yeah. We had him on a previous show before. He's doing back ports mostly. Yeah. Yeah.
[38:58] So what he's doing is he picking up some pull requests from Bitcoin repository and dragging them back into the dashboard so that
[39:08] we have a similar features in both, uh, like some, some backwards from Bitcoin into the dashboard. Yeah. Uh, yeah.
[39:18] Uh, stuff like that. Um, so my strategy, yeah, I was just going to ask a follow up on that. I,
[39:27] I do like to focus on that because I, that is this, you know, this, this 180 dash, it's not just for thinking,
[39:36] but it is a lot of like you, you want to make sure that you're building the right things. Cause you can,
[39:43] you can do a lot of work digging a hole and filling it back up again. But, uh, that would be a failure of strategy, right?
[39:49] Cause you want to be doing valuable things. I, for one, have found the platform explorer to be very valuable. Um,
[39:57] I'm not a dash Electrum user. So I think that you're doing a great job with strategy so far,
[40:01] but talk about this upcoming quarter. Yeah. Uh, so, um,
[40:08] I want to, I want to get some more developers into our projects. I have been searching for, for good guys, uh,
[40:19] the last quarter. Uh, but today the most, the most, the most important thing is that, uh, we need some, some,
[40:28] not just coders. We need hackers that really know what they are doing.
[40:32] And there are a lot of people that just on Ethereum, uh, hype stuff.
[40:38] And that the people that don't really know anything about Bitcoin blockchains, uh, about, but thing that we're building, that we are building.
[40:48] And these type of guys, uh, like not really understand what, what, what, what we're trying to accomplish, what, what, what we,
[40:57] what we are doing. So my strategy is to find those guys eventually. And a lot of time, by the way,
[41:04] like finding good developers is not easy recruiting as part of this. Yeah. Uh, yeah, there, uh, there were,
[41:13] there were people that I was, uh, contacted with and, um, and I didn't find really good, good, uh,
[41:23] good guys that, that could deliver, uh, really, uh, fair thing, uh, things for the dash, uh,
[41:31] because we don't want to really waste the budget on some people that just do things like, uh, like, like for money or stuff like that. We, we need,
[41:40] we need really, really hackers, hackers that, uh, that are interested in the, the, the, they would be like,
[41:49] uh, they'd be curious about things that. Yeah. They're going to look under the hood. They're going to peel stuff back.
[41:56] They're going to try and, you know, break things and make it better. You know, they're going to complain about shit that's broken and not just,
[42:02] just do the basics. You know, they're not going to put in their nine to five. They're actually going to really want to make this better.
[42:08] Um, so yeah, so I'm continue on searching for these people.
[42:16] Uh, I have some, um, I have some ideas, um, where to find them. Yeah. And, uh,
[42:23] uh, yeah, another, another things that we are going to do is to keep on
[42:31] developing, um, as the case and, uh, doing stuff for the platform. Uh, as an example,
[42:40] uh, uh, there is a platform explorer that, uh, we already, um, we, uh, we, um,
[42:51] there is a API of the platform explorer, and we are going to extend it with a more functionality on the platform
[42:59] explorer. There is a separate page on the API of the platform that developers already can
[43:03] use. Uh, this API is, um, heavily tested. Uh, there are integration tests for each of API endpoint that will ensure that
[43:13] everything, uh, works, uh, as expected. And some of the features are, um,
[43:22] that you could possibly, uh, subscribe on some actions that is happening in platform chains. For example,
[43:32] you could, uh, subscribe on documents happening on the data contracts,
[43:37] or you can, uh, subscribe on some transactions, uh, happening on identities or stuff like that, and that you can,
[43:45] uh, get the callback for your application, uh, that, that you, that you are building.
[43:54] That's mostly for the third-party developers. Um, yeah, also the, is the case, I'm looking, um, uh,
[44:05] for a way for, to interact with, uh, with the platform, why SDK, uh, like, uh, right now we only have dash SDK
[44:15] that is available from, from, from the DCG. They are developing a dash SDK,
[44:22] but it has some shortcomings like, uh, it waits too much. It, uh, sinks with the network.
[44:31] Like you have to download a lot of data to, to keep all the, to, to sync with the network. And, uh, what I'm,
[44:40] uh, researching, what I'm developing is, uh, some kind of SDK that, uh, would allow us, uh,
[44:49] to have lightweight, uh, connection with the platform and allow us to submit documents,
[44:55] submit, uh, register identities and do all of the basic operations without, uh,
[45:01] without taking those weights, taking, taking those, um, like, uh, without, uh, a lot of latency, a lot of waiting time.
[45:12] And, and yeah. Um, yeah, we've talked about it before. Um, and I fully agree with you.
[45:22] Um, I, we, we talked a little bit about before we, we were talking about how the dash SDK had actually shrunk in size and it turns
[45:32] out that the latest version of, um, dev 10 SDK actually grew again.
[45:43] So I'm not sure what's happening there. I remember last time we talked about this,
[45:47] we clicked on the latest dev version and it was like half of what it used to be. And even, um, dash money talked about it a little bit. Well,
[45:54] now it's back up and it's even higher than it used to be. So I'm not really sure what's happening there,
[45:58] but we do need a lighter weight version of, uh, to be able to contact. I find the, the performance is just even the, you know,
[46:06] ignoring the weight of the library, the performance of it is just, it's just not quite there. You know, like, uh,
[46:14] username lookups taking over 10 seconds and just, it adds, you know, several seconds to load times when you're booting it up. It's just, yeah,
[46:23] it's just too much. It's, uh, you know, there are just issues there. And I know we can do things where username lookups could be faster if we
[46:32] utilize, you know, platform Explorer or whatever else like that. And I'm kind of curious on how we can make it still decentralized and trustless,
[46:40] but much far more far it much faster because at the moment from a user, if they're waiting, you know,
[46:46] 12 seconds for a username lookup or it's adding to the page load, it is, because it's not just the, you know, it's not just the downloading the file,
[46:54] the package, it's the connecting to the blockchain and that taking several seconds, you know,
[46:59] it's just all of it feels slow and I can't contact web developers like that. Like I, I just feel good about it. So yeah,
[47:07] I would laugh to laugh out of the room if you show them this. Yeah, we'll, we'll, we'll keep working on this. Um, speaking up,
[47:15] um, to say on that, Oh, you got to get going. So do you have any final parting words before you get going?
[47:23] We'll continue to show. Yeah, no, just, I'm excited to do more web stuff. So, okay. Good to meet you, Ash. Yeah. You too. Yep.
[47:31] All right. See ya. Yeah. So, um, yeah, we'll, we'll stick on for a little bit longer.
[47:38] I had a few more things to say about, um, what my, um, plans are going forward.
[47:45] Let me talk about my project. Woo. Let's, let's, let's move on to you. Let's see if we can, uh, present. Um, unfortunately I hate developing a window,
[47:57] so I refuse to run the extension on my windows PC, which is what you're seeing me on here. All right, let's add this to the stage.
[48:03] I guess I'm just going to share screen on my other, uh, account and let's say, let's see if this works, uh, here. Uh, interesting.
[48:14] Whoa. Okay. Probably should have given this a little, uh, a little test run before we started, you know, uh, but it's going to be fun.
[48:22] It's going to be fine. I'm just, uh, allowing Google Chrome, uh, into my, uh, to, uh, record my screen basically. Uh, to, to, to do, let's do a,
[48:32] I'm just going to do entire screen because I'm worried that the extension, um, won't allow you to,
[48:38] it won't show that the extension pop up. Yeah. Yeah. Okay. Nevermind. It is not going to show it because, uh, it's booting in its own little, um,
[48:49] Chrome. Um, wait, I know what to do. I know what to do here. Sorry. I have to open this in normal Chrome, uh,
[48:56] cause it's being in its own sort of a single user session, um, which doesn't have permissions to view my screen.
[49:03] Whereas if I open a new user that isn't a guest profile, uh, let's see. Um,
[49:10] might be, might be dodgy. One second. One second. We'll get there. We'll get there. Here we go. Here we go. Stream yard. Let's go load up the cool way.
[49:23] I can, I can talk for a little bit. Um, while you're, I have, um, let's see.
[49:30] Now we don't have, uh, Anthony to help me do this, but let me go back to this screen. Uh,
[49:36] one of the things that I'm going to start doing is trying to go to web, to developer conferences and represent dash either formally or informally.
[49:45] The one, one that I found that's like, I'm super excited about this is Epic web conference, 2024. This is coming up,
[49:53] um, April 11th. So next week I don't, don't have my tickets yet, but I'm going to get my ticket and I'm going to try to pay for it with spritz.
[50:02] So I might actually show that on a live stream, uh, or at least a video, uh, update that or upload that to the incubator account.
[50:10] Uh, should be, should be good. Yeah. Okay. So, I mean, I want to say a little bit more about this later, but let's move on to you.
[50:17] Add to stage. How do we just, my screen share is the main thing. Let's see.
[50:25] I think I added you to screen. Let me remove this. There's one called my screen or whatever should be hash screen.
[50:38] It's showing right now, but I don't, I put it on the sharing. It says you're sharing your screen at the moment. Don't add me,
[50:44] add my share or whatever. Here we go. There you go. Oh, I've got some recursion going. Beautiful. All right. Um, okay.
[50:51] So let's just run this. Um, so this just boots up really easily.
[50:56] It used to be very complex to get this running because of another developer. Uh, let's just, can you zoom in or expand or something?
[51:03] Yeah. Let's just load that up and then we're going to pin this and we're going to try and zoom in or actually this isn't going to zoom in.
[51:13] The extension might be clear enough. I don't know. Let's see. Can you see this? All right. Yeah. Okay. So we got it.
[51:20] We got a basic view of what's going on here. Um, so dash pay extension is a equivalent sort of metamask with dash style project.
[51:29] Uh, the issue with, uh, any sort of, uh, decentralized application and using it, uh, you do not want to be uploading, you know,
[51:35] importing seed phrases every time you use one or uploading a key store. We needed a system that allows us to kind of log into these apps.
[51:43] I know dash core group have done some research in this, but you know, the mobile wallet is where we're doing a dash pay dash platform, um,
[51:50] stuff in dash evolution. Uh, and that's not going to allow our developers to really easily integrate, um,
[51:56] users into their systems. So, uh, be working on an extension, uh, for a long time, uh, through a myriad of developers. Uh,
[52:05] but now we've got it to a very stable state. Uh, this is mostly UI. We have scaffold there for integration into, um, sort of platform,
[52:15] but we've had issues developing against platform as, uh, mentioned a little bit earlier. Um,
[52:20] so part of this is going to be a case of leveraging the work that Chen make is doing both in terms of a lightweight library or using platform explorer to make
[52:29] things faster. And as well as the work that Rion's doing in terms of, uh, the vinyl,
[52:34] vanilla web wallet, just more efficient, faster, uh, more secure libraries, less dependencies, cleaner code base. You know, um, it might,
[52:42] may seem that three, the three of us are working on a separate sort of work, but there's a hell of a lot of overlap between what we do and part of what
[52:51] Brian's kind of job is, uh, is to kind of see that cohesion, uh, in terms of a longer term vision. Uh, so in terms of this,
[52:59] the goal with this is to be a kind of, um, I guess a social wallet. This is a different approach, you know,
[53:07] when MetaMask and a lot of the wallets that we currently use today are very transaction focused, they're very kind of like spreadsheet accounting.
[53:14] This is more supposed to be kind of like a Venmo, um, level, uh, sort of service. Uh,
[53:21] so it's more about the social interaction with your friends and with decentralized applications. Um,
[53:27] so the goal here is that you can kind of have these, uh, sort of conversations with people request and send, um,
[53:35] funds to them and, uh, interact with people in kind of a social way, uh, as well as with the legacy sort of transactions. Uh,
[53:43] and you can kind of see some of how this will sort of form. Um, but really the key thing here is that sort of interaction with, uh,
[53:51] decentralized applications with, uh, projects like, you know, CTX spend, um, with, uh, the other work that we're doing and creating sort of a,
[54:00] a passport between all these sort of, uh, different systems. Uh, if I go back to the debug screen, you can see some more of a sort of windows.
[54:09] So an individual chat, um, so you can talk and make payments to each other, uh,
[54:16] and just request funds, attach notes, those funds. Uh, and it gives you a way to make those transactions more social, more human, uh,
[54:24] rather than, uh, like a, yeah, you know, like a ledger, like a list. Um, so the idea is this would become sort of a social payment, uh, system, uh,
[54:32] but as well as those interactions with the decentralized applications. So you'll have your friends,
[54:37] you'll have your social graph on here and you can spend and receive funds, uh, to them and attach meaning, uh, to those sort of transactions. Uh,
[54:45] are the transactions, the payment transactions, are they going to be using primarily credit transfers or
[54:52] uh, in terms of actually paying, uh, obviously, you know, there will be a case of whether people do tokens and, uh, you know,
[55:00] NFTs and whatever else on platform. Uh, but there is all the platform interactions in terms of writing to, uh,
[55:06] data contracts and, uh, you know, using your identity. So everything is kind of that crossover between a platform and layer one.
[55:14] So layer one transactions, but attached to a platform sort of identities. Great. Uh,
[55:20] obviously built as a web extension. So it's quite like a limited on how, uh, you do things, but the advantage of that is it can be deployed to, uh,
[55:31] mobile. It can be deployed, you know, as a standalone web app, you know, if you actually even go into it, you know,
[55:35] it is actually kind of like a web app, um, itself. Uh, there are lots of things that we can do with this. Uh,
[55:42] I think the key thing is that whatever is being done on the vanilla web wallet, uh, whatever we're doing with SDKs and things,
[55:50] I want to either incorporate that into this or incorporate this into them. You know, I want to have an extension wallet where a user has their identity.
[55:59] They have, you know, multiple identities that they can, um, you know, go through, uh, like if they go to an accounts page and they could switch the,
[56:06] you know, they're using their personal for their personal payments, they've got their web two, web three sort of identities, um, there as well.
[56:12] And it's easy to manage, um, and work for those accounts. Uh, so yeah, there's a lot of, uh, different parts to this. Uh, mostly at the moment it's UX.
[56:21] We've, uh, we've made it like, uh, a lot cleaner now and a lot easier to develop. Uh,
[56:27] but obviously we're time limited because of other things. I would love to find another developer.
[56:31] I would love to have the time to put the effort into pursuing another developer. Now that this is a very clean sort of project,
[56:38] if someone is more interested in the hard, you know, focused development of the platform integration in terms of the contracts for the
[56:45] chat, because this is using, uh, the way this is designed to, um, what is to use the signal protocol, uh, which, uh,
[56:53] a project two or three years ago, uh, in the incubator built a, uh, an example of, uh, the, it was called what stat, uh,
[57:00] which was a decentralized messenger built on dash platform. Um, so now that this project is a lot cleaner packaged,
[57:07] it'll be a lot easier for a developer to pick up and work with that wants to focus on more of the platform integration side of things.
[57:13] So that's the next major stage. Most of the UX is done. There's a few little bits of polishing and things,
[57:18] but the actual core functionality, um, in terms of how, and you know,
[57:24] everything sort of looks and the fact that it's all scaffolded to have that data come in from platform, um, and everything like that. So, uh, yeah, it's there.
[57:34] It's just a case of turning this into an actual functioning platform app. And the other core part of that is that handshake between, uh,
[57:43] the web apps themselves and the extension. We did some early reference examples of that, which we have,
[57:50] but a key thing for me is that interoperability with the other, the rest of web too, whether that's a wallet connect or otherwise, um,
[57:59] I had some conversations with one of the guys at Dash Core Group that was researching, um, you know,
[58:03] while it connects and the equivalents, uh, web three JS sort of stuff. Um, and the, um, the issue with wallet connectors,
[58:12] some of it was closed source and it was kind of like a bit of a black box that, uh, data was going into. Uh, so we do want to do this,
[58:20] but we want to do it right. But we also want to do it fast and get it ready for developers so that we don't
[58:24] have to do this, you know, insert your keys, like your, your phrase, you know, we need to have this really simple developer at this library,
[58:33] which doesn't have lots of dependencies and isn't full of bloat. Uh, and then you can do a handshake with, um, you know, a platform extension,
[58:40] and then you can make your X, your decentralized application accessible to all of the Dash platform users.
[58:46] Um, and you know, a lot of this will become better and faster through use of things like the
[58:52] platform index, uh, through those better libraries. And like I said earlier, you know, it's important that we do this in a way where it isn't,
[58:59] we're not trusting, you know, anything that could form a man in the middle attack.
[59:03] I'm talking about things where when I'm looking up usernames and making sure there is no, um, you know, when let's say I go to the username creation flow,
[59:12] when I type in a username here, I can, I don't need this to check against Dash platform.
[59:18] I can check against platform explorers, username indexer. And then when I actually come to register that username,
[59:25] that's when the real check happens, the light check as such, you know, the indexer will probably be very up to date,
[59:30] but that's a way that we can make this a lot faster and not have people sitting there for however long, uh, waiting to, you know,
[59:38] check against the entire record of usernames, which is only going to get longer, um,
[59:42] on the actual blockchain rather than fire and explorer. Um, so yeah, there's so many parts of this, um,
[59:49] but it overlaps a lot with what Rion's working on the vanilla web wallet in terms of libraries that they built there that less dependencies, faster,
[59:57] more secure, just, you know, it's going to be a lot better on that and things like, uh,
[60:01] Mikhail working on the SDK, um, and the explorer. So my next quarter will be, uh, focused on more work on this. I don't,
[60:08] not really the only other project I would can see myself working on is a project that uses this,
[60:14] that would be a reference example of the integration of, um, the handshake between the, uh,
[60:20] decentralized application and the extension wallet, and then, uh, writing to, uh, uh, contracts, uh, data contracts using the extension, um,
[60:29] and then via a decentralized application. So the decentralized application is sending a message to the extension saying,
[60:35] Hey, ask the user permission to write this message to this data contract. Um, you know, and then the extension is going through that process.
[60:44] So that's the next quarter for me, really cool. Well, uh, speaking of that, there was already one question that said, uh,
[60:52] on my proposal that I have submitted, why is Ash not requesting any funds again?
[60:59] Yeah. I mean, not like I'm still sitting on, I think it's 600. I've got a, uh, um, proposal to, uh, a bit of spending to do today to, um,
[61:09] pay for some of the development work on the extension. Um, but you know, if I do need more funding, like a top up this quarter,
[61:17] I will do a small ask like a micro just a single proposal or something. But I, uh, right now I'm very busy with, uh, spend.
[61:25] And I also do believe in, you know, maximizing efficiency at the network. I know we had a treasury increase, but I think that that is the, you know,
[61:34] we don't have to spend it all. And I'm not going to, I don't need to build up a war chest right now. Uh, I do think that, um,
[61:41] my focus will be, you know, on, on spend, but we need to get spend out the door and then we're going to feature freeze on
[61:49] that, um, for a while. And that's when we'll be working on more of the integration side of things.
[61:54] So integration into, you know, the web wallet that Brian's talking about, uh,
[61:57] into multi-coin wallets and things like that. Like I do still want to largely compete a lot of my outstanding incubator,
[62:05] uh, work and work on more projects there, but it's a matter of bandwidth and allocating to what I believe the biggest wins
[62:12] are right now for, um, for us really. Yeah. Okay. So I'd pulled up on the screen here. Um,
[62:19] our quarterly reserve planning, uh, as you mentioned,
[62:24] you have 641 dash left in your reserve from previous funding. And last quarter you spent an average of 85 dash per month,
[62:34] uh, on this extension that you just talked about. So I just put 100 in here as a placeholder.
[62:41] I don't know how much you're going to allocate to it, but honestly, I think once this, uh,
[62:46] unless I find a developer that's interested in, um, picking up this, uh, project, there will be probably for the next few months, it'll be kind of, well,
[62:55] the next couple of months, it'll kind of be on a freeze, um, with maybe minor bits of work to it. Yeah.
[63:03] I mean, the UX is largely there. It's a case of, uh, building in that platform, um, functionality, uh,
[63:09] and some of the layer one functionality. I think you kind of are leading how we would implement the layer one
[63:15] functionality anyway. So there's no point in duplicating any efforts there. Um, and in terms of platform functionality,
[63:21] if there is going to be a faster SDK or, um, if more efficiencies made there, then yeah, that,
[63:27] that is logical to utilize that. The frustrating thing is, is this chicken and egg problem.
[63:32] Like I do believe that developers would be really well served by having a, you know, an extension that allows them to sign onto the app.
[63:39] So I do want to solve that side of it. Um, but that isn't that complex. If I can squeeze that in this, uh, quarter,
[63:45] then I would like to have that even if it's a separate extension that is just a developer focused, you know,
[63:52] use this to test and for the community to test decentralized applications as well. Yeah. There's so much you can do with this. It's, it's crazy. Like, uh,
[64:00] one of the things about platform that people don't appreciate is that it can handle a level of messaging between decentralized applications and wallets,
[64:08] like everyone right now with the metamask side of things, they're often using, you know, they're using their extension or their phone,
[64:14] which has like a adapt browser or whatever side of things in it. But with platform apps can actually communicate by post writing to platform.
[64:22] And that can be picked up by like a mobile app, you know, in the dashboard mobile wallets,
[64:27] we can have platform functionality and that handshake can be done through a QR code, you know, where there is, you know,
[64:33] things are being written to platform and then, you know, received by the mobile wallet and vice versa.
[64:38] They're communicating via platform rather than via, you know, local, sort of their own sort of connection.
[64:45] Like they're not communicating via a wrapper on a website like firing events up and down. They're actually communicating via platform.
[64:51] And even in terms of sending off alerts and pinging updates and things like that, it can all happen by platform.
[64:57] And there's a lot of cool stuff that we can do there that, you know, down the line, it'll be fun playing with it. Yeah, exactly. Yeah. So, um,
[65:07] you, so again, you were requesting zero this month, uh, Mikhail, I have a placeholder in here for 200 that we had discussed preliminarily.
[65:17] You have not got your proposal up yet, but it's coming shortly. Are you still planning on requesting 200 dash or is,
[65:26] is, uh, yeah. Is it something else? Uh, you're let's see, are you muted? You're muted. Yeah.
[65:35] So yeah, I'm going to request a hundred dash. I have, uh, a lot of, uh, reserve from the previous quarter, uh, that is still there.
[65:44] So I think, uh, that will be enough, uh, quarter, uh, 200 dash and, uh, yeah, I will be using the,
[65:54] the, there is, um, this reserve. 1161 dash specifically. Yeah. Yeah.
[66:04] Yeah. And I just wanted to explain this in case somebody hasn't seen my explanation about this spreadsheet yet. Um,
[66:11] or even if you just needed a review, uh, and I'll use you as an example here. So you have this 1161 in reserve you're requesting 200.
[66:20] I am estimating that you're, you'll spend 300 per month. So you'll be in a 100 plus a deficit. This, uh,
[66:30] each strategist gets a base reward for strategy, um, and, uh, miscellaneous things, recruiting, all sorts of, uh,
[66:38] stuff that's not itemized. That's that 20. And then, uh, each strategist then also gets 20% of tasks that are completed.
[66:47] If somebody else is completing them, or if you're completing them yourself, then it's obviously different. Uh, but that would add up to this 80.
[66:54] So total you'll be in a 180 dash deficit, uh, per month. Uh, but you do have that reserve. So at the end of the month,
[67:03] you would, you would be expected to have 981 dash. Um, assuming that that funding continues, you have a 5.5 month buffer.
[67:12] Assuming it doesn't continue that your proposal doesn't pass, you would have a 2.6 month buffer. That's how you interpret this spreadsheet.
[67:19] Um, and then same goes for Ash and myself. Um, I've requested 800 dash. Um,
[67:26] that's pretty much the minimum that I feel comfortable. Asking for with, uh,
[67:31] that's three to four full-time equivalents is what I'm targeting this quarter. Um, I do have a, uh, a pretty good buffer from last quarter that,
[67:41] um, grew a little bit from, from last quarter. Um, but I am planning to spend about the same that I'm requesting.
[67:49] So, um, when, when I add in my, um, my strategist rewards for that,
[67:56] I am in a deficit of 240 per month still. Now, if the price goes up, these numbers change,
[68:03] this projected output would go down. Most likely. Um, the budget request obviously is stays static throughout the quarter. Um,
[68:11] and, uh, but the, the, the pricing of outputs and tasks can change based on the purchasing power of
[68:19] dash. So depending on what the price does, uh, I may or may not have, uh, right now I have a 1.1 month buffer,
[68:27] assuming that no funding comes through, assuming that it does, I have a healthy buffer of 4.9 months, um, and 3.9.
[68:35] And then by the end of the quarter, 2.9. So that's, I just wanted to explain how this table works again, for anybody that's, uh,
[68:41] including you guys, Mikhail and Ash, you are always free to refine this as, as your needs come up.
[68:48] Um, but that's all I wanted to say about that. Ash, you mentioned something about, um, you guys are, are using remix, uh,
[68:57] framework. I wanted to mention just real briefly, that this epic web dev conference, uh,
[69:04] that I'm going to be attending next week is put on by, uh, Kent C Dodds, who is the creator of remix or not. He was one of the,
[69:14] uh, it was a Rion Florence. And, uh, what's the other Michael Jackson, not that Michael Jackson, but the other.
[69:22] They are Utah guys, uh, or at least one of them is, and, or two of the, uh, let's see, Kent's not part of the remix team,
[69:30] but he w he uses it extensively in his course and he's putting on this conference. I will see him. I will see here's Kent.
[69:37] I will see many of these coming right down the street from me. So we've been loving remix. So, uh, yeah, if you can, uh, get, get any, uh,
[69:46] dash of, uh, involvement or like, uh, collaborations down the line with them, obviously there's nothing ready yet at all, but yeah, it's great. I,
[69:54] I think remix we've been using for a lot of our internal tools and we found it really, yeah, really performant, really good. Like where, um, you know, we're,
[70:02] we're talking about, you know, 150,000 merchant locations loading up in seconds rather than, you know,
[70:07] trying to do that on pure front end, rather than subside rendering. It's just, it's a joke and it was just faster than the next as well. Just, yeah,
[70:15] we really like remix. I actually, um, last year I reached out to remix.
[70:20] They were having this conference last year and I reached out to them, um, cause I know them from local meetups, uh, Kent at least. And, and,
[70:27] and Michael and Rion I've met as well. Um, I wanted to sponsor them. I have dash sponsor them, or at least to open a conversation about it. They,
[70:36] they ultimately didn't feel comfortable with that because they are now owned by Shopify who is, you know, a payment provider. So they,
[70:48] they weren't comfortable with it. I, I would hope that at some point we can break into that, um,
[70:54] give them some money and, and help increase a dashes reputation in this space as we discussed earlier.
[71:00] But that's, um, yeah, plans down the road. So I think we've gone for a while here. Um, let's, let's,
[71:09] let's have some closing remarks, I guess. And, um, wrap this up. Anything else to say, uh, Mikhail,
[71:17] your proposals coming up, coming up in soon and mine's already up. Thank you for, uh, the early support on that, by the way, for, uh,
[71:26] those of you who have voted and yeah. Any, any closing remarks, Ash or Mikhail.
[71:32] You can go first. Well, um, I don't have anything specifically to say, but yeah,
[71:40] we, we will be continuing building, um, continue working on stuff and, and yeah,
[71:48] um, uh, let it be the, the great, the great Porter. I'm looking forward to it.
[71:56] I think, uh, from my case, obviously, you know, spend is outside the incubator. It's a sort of commercial sort of product.
[72:04] Uh, but everything that we do kind of like ties together, you know, there is overlap with incubator stuff. Um, I'm really excited to launch that,
[72:11] uh, pretty soon. I'm not going to go say dates. Cause I think that's always a, uh, a recipe for disaster, but then, you know,
[72:19] it'll be a case of, uh, bringing that into other products and leveraging that in ways to bring in
[72:25] audiences and add value to our existing audience. Um, I'm really excited for the next quarter and see what, uh,
[72:30] the future holds for us all. Yeah. Uh, just speaking for myself,
[72:35] we will definitely be integrating dash spend CTX spend into the incubator wallet on our end.
[72:41] And we are having Jojo bite will be coming on next week to, uh, show the latest state of that.
[72:48] And I don't know if CTX spend will be in there. Probably not. It won't be, probably.
[72:54] They have a placement collection and API queues it's happening, but you know, there's some, uh, outlying bits, uh, but things are very much progressing.
[73:02] So all right, guys, let's, let's call it there. Uh, thanks for joining us everyone. And we will see you next week.
[73:09] Thanks. See you around.
[73:11] Bye. 
