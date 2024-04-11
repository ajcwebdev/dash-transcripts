---
showLink: "https://www.youtube.com/watch?v=7o_2kDnrKEg"
slug: "what-is-a-dapp"
title: "What is a dApp"z
publishDate: "2024-04-01"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/7o_2kDnrKEg/maxresdefault.webp"
---

## Links and Resources

- https://ajcwebdev.com/first-look-ipfs/
- https://someantics.dev/ipfs/
- https://trello.com/c/xLrc4Bcr/69-ipfs-dash-platform-integration
- https://trello.com/c/q16cvr5A/171-decentralized-dynamic-application-infrastructure
- https://dash-incubator.github.io/dapp-sdk/
- https://github.com/imestin/DP-IPFS-hello-world
- https://github.com/dash-incubator/dapp-sdk
- https://github.com/ipfs/helia
- https://github.com/Permissionless-Software-Foundation/ipfs-service-provider
- https://github.com/ipfs/helia-verified-fetch
- https://github.com/ipfs-shipyard/service-worker-gateway
- https://blog.ipfs.tech/dapps-ipfs/
- https://www.dash.org/news/introducing-the-platform-chain/
- https://read.cash/@Devalbo/bch-ipfs-they-say-but-then-what-280a206a
- https://docs.ipfs.tech/concepts/ipfs-gateway/
- https://developers.cloudflare.com/web3/ipfs-gateway/
- https://dnslink.dev/
- https://www.pinata.cloud/
- https://fsjam.org/91
- https://thefutureofjamstack.org/

## Guest Information

- Walker Ford on LinkedIn: https://www.linkedin.com/in/walkerford/

## Episode Description

In this episode of Incubator Weekly, we're joined by Walker Ford to discuss decentralized applications and IPFS.

## Episode Summary

tl;dr: Decentralized applications (dApps) are complex, requiring various components to be decentralized. dApps aim to be verifiable, not tied to a single host, and interact with blockchain for data storage. They comprise decentralized components like hosting, domain names, code, and storage. IPFS is a distributed file storage system using content-based addressing. Challenges include discovery, ensuring data availability, and integrating with browsers. The goal is to provide users with the ability to verify content, especially when dealing with blockchain transactions, but there are still hurdles to overcome.

## Chapters

## Chapters

00:00 - Background and Experience of Guests with IPFS and Decentralized Applications (dApps)
The episode begins with an introduction to the topic of decentralized applications (dApps) and what it means for an application to be truly decentralized. The guests, Walker and Anthony, share their background and experience working with IPFS and decentralized applications in the blockchain space.

06:20 - Defining Decentralized Applications and Their Characteristics
Walker and Anthony provide their perspectives on what constitutes a decentralized application, including verifiability, resilience, and not being tied to a single host.

11:49 - Traditional Web Hosting and Its Pros and Cons
The discussion moves to traditional web hosting methods, such as servers and CDNs, and the advantages and disadvantages of these approaches.

14:48 - Introducing IPFS's Role in Decentralized Storage and Its Relation to DNS
IPFS (InterPlanetary File System) is introduced as a distributed file storage system that uses content-based addressing, and its potential role in decentralized applications is explored.

27:00 - Dash Platform IPFS Integration and Past Efforts
Rion shares some of the past work done in the Dash Incubator related to integrating IPFS with the Dash Platform, including a "Hello, World!" application.

32:19 - Challenges and Solutions for Delivering IPFS Content to Users
The guests discuss the challenges of delivering IPFS content to users, including the need for browser support, and various solutions like DNS link and gateways. Walker explains the newly created Trustless Gateway Specification and the problem it seeks to address.

46:38 - Updates on IPFS Development and Helia Implementation
The conversation touches on recent developments in IPFS, including the Helia JavaScript implementation and ongoing efforts to improve verification and browser integration.

54:01 - Closing Thoughts on Decentralized Applications and Getting Started
As the episode wraps up, the participants share their final thoughts on what constitutes a decentralized application and advice for those looking to get started with IPFS and dApp development.

## Transcript

[00:00] We're live. >> Cool. Welcome everyone.
[00:05] Very excited to be joining this and hosting this call today. We're talking about, this could easily have been labeled.
[00:15] What was our label last week? Dash Platform for Web Developers.
[00:20] This could have been a part three. But instead, I thought it needed its own little title.
[00:26] We're going to be talking about what is a DAP? What is a decentralized application?
[00:32] I have with me my trusty co-host, Anthony. >> Hello.
[00:37] >> Our guest today, Walker. >> Hi, Rion.
[00:41] >> Anthony, you have a lot of background with decentralized applications,
[00:51] specifically with IPFS. Walker, you have worked with
[01:01] Protocol Labs as an employee there for a while, and we're intimately involved with these topics.
[01:12] Do you want to give an introduction to yourself, Walker? I know you personally.
[01:18] We've known each other for many years on both the personal and professional level.
[01:23] But give the audience a little bit of a taste of where you're coming from,
[01:28] and how you found Dash, and how you found Protocol Labs.
[01:33] >> Yeah, I've been a developer for many years. Stumbled on Dash a while back.
[01:41] I've just been observing the development over the years. I've been hopeful about it for a while,
[01:51] and I'm excited to dig more into the Dash platform. I have been working professionally in
[01:59] the blockchain space for a couple of years. I've worked for a big cryptocurrency exchange,
[02:05] and recently worked for Protocol Labs, helping them integrate Filecoin and
[02:11] IPFS with some of their portfolio companies. It's a really interesting field.
[02:19] It raises a lot of questions, and is trying to get to the answers.
[02:27] But it's fascinating, and we should have an interesting conversation today.
[02:33] >> Yeah. Anthony, why don't you give your background as it relates to this subject as well?
[02:39] >> Yeah. The first time I used IPFS was in 2022, when I was working at QuickNode,
[02:47] and I was getting involved in lots of things in the Ethereum and the Solana community.
[02:53] I'd heard of IPFS as this decentralized storage solution. At the time, I was like, "Okay, that's cool.
[03:01] We know it's a way to put files on the Internet." But until I dug into it,
[03:06] it really opened my mind and it really blew my mind. Actually, I ended up writing the longest blog post I'd ever
[03:11] written about it at the time to just get a spin-up tutorial with it.
[03:16] It was the first time since I learned to code that I felt like I was working with technology that was legitimately new,
[03:25] like something I'd never used before, and really it stretched my mind.
[03:29] It was the first time I ever had to actually learn how DNS worked, because there was different ways to connect to routing stuff,
[03:36] and it was awesome. I loved the idea of having a static front-end
[03:41] that you wouldn't have to deploy to Netlify or Vercel. You could just create this thing,
[03:47] you get a hashback, but then all of a sudden you had a link and it was on the Internet,
[03:50] and you paid nothing and you did it all from your CLI. I just thought that was so cool,
[03:55] and I've been really excited about that project ever since. >> Nice. I was trying to search
[04:02] for your blog that you just mentioned while you were saying that. >> Sure. It's been a couple of years since I looked at it,
[04:13] so this one might be a little bit out of date just for people, so I just want to put that out there,
[04:17] but it's called A First Look at IPFS. I just popped it in the chat.
[04:21] >> Okay, cool. I found a couple other things that you had to do with interviews and whatnot.
[04:29] >> Yeah, I did a couple of live streams about it as well, yeah. >> Yeah, we'll definitely have to include those,
[04:34] and I'll have to read those as well. A lot of history here,
[04:39] a lot of experience. The reason that I wanted to talk about this today was
[04:46] motivated by a conversation that I had probably a week or two ago
[04:53] about one of our Dash community members wanted to build an application that was decentralized,
[05:00] and I was asking questions about, okay, how should this application be deployed and delivered to the users?
[05:10] My line of questioning was trying to get at the, okay, if you want it to be fully decentralized,
[05:17] if you're delivering that application through traditional means because your users are traditional,
[05:24] then you might run into some issues. IPFS came up as a solution,
[05:29] a potential solution to this issue, and I've been aware of IPFS for quite a while,
[05:35] but I've never really dug into it myself. I wanted to have this conversation because there is going to be
[05:40] a time where we are really able to start building applications on Dash platform, using Dash platform.
[05:50] I just wanted to have a conversation about what does it actually mean to be a decentralized application.
[05:57] I'm going to go ahead and share my screen here because I really am focusing on Dash platform recently because it is getting closer and closer,
[06:09] and it's pretty exciting to be able to use this. One of the first lines in.
[06:16] >> Bump up your font just one. >> Yeah. One of the first lines in the documentation says,
[06:23] "Dash platform is a Web3 technology stack for building decentralized applications on the Dash network.
[06:29] The two main architectural components are Drive and Dappy." Let's see. The main thing that I wanted to emphasize here
[06:39] was building decentralized applications. That highlighting is probably not helping.
[06:44] But building decentralized applications, we've been talking about this for many,
[06:49] many years in crypto land, but what does it mean? I'm going to start out with that question to you, Walker.
[06:56] What does it mean to build? What is a decentralized application to you?
[07:02] >> Yeah. That's a deep well. But what we're going for is essentially an application that's verifiable,
[07:19] and an application that perhaps isn't necessarily tied to one host. It isn't just sitting on Amazon,
[07:30] or it has the potential to be moved. Digging in a little bit deeper,
[07:37] a decentralized application typically interacts with a blockchain. Using the blockchain as a sort of its database component,
[07:50] and any web app has a few components. There's the hosting provider,
[07:56] the domain name, the code itself, and then the storage.
[08:04] Depending on the size of the storage that's needed, blockchain works really good for storing a little bit of data.
[08:12] It's very expensive. When you need a little bit more data to be stored like the database,
[08:22] we haven't had a great decentralized option there, and that's what the Dash platform is proposing,
[08:30] a place where you store if blockchain is sub-kilobyte data, then maybe Dash platform is kilobyte to megabyte, something like that.
[08:41] Then you also need a place for your larger data, your megabytes plus, your multi-megabytes.
[08:48] That's the area where Protocol Labs has been working in with IPFS and Filecoin. But the decentralized app essentially at its purest,
[09:00] it combines all of these elements into one application that you as a user can be a little bit
[09:08] more assured of that it's verified and authentic and isn't going to run off with your funds.
[09:17] There's a lot of complexity. We'll talk about some of that today.
[09:23] But yeah, it's really an aspirational next generation application experience that we're trying to deliver to users.
[09:33] >> What about you, Anthony? Walker mentioned verifiable among other things.
[09:41] I'll ask you the question a little bit of a different way, but feel free to answer however you want.
[09:47] What is a decentralized application to you? But more importantly, for you,
[09:52] why do we want decentralization? Why is that a feature?
[09:56] >> Yeah. The thing that Walker said, that a decentralized application is something that doesn't just
[10:02] live on a single server owned by someone. I think that really gets at the core of it.
[10:08] If you have something on Amazon, Amazon service is decentralized in a certain way that if a bomb hits
[10:15] an Amazon datacenter, your stuff's probably going to be okay. They're going to figure out a way to route it around.
[10:20] But Amazon itself goes down, your app goes down, and this does happen.
[10:25] I think we have all been in the experience of seeing a third of the Internet shut down for an hour or two,
[10:30] while the Amazon elves run around with their heads cut off. The big thing you want is you want resilience.
[10:38] To me, this is a slightly different angle from the trust angle. But I think resiliency is a really key part of this,
[10:47] because you're not going to have to rely on IPFS necessarily to keep your application running because you have,
[10:55] and this is really to me, this is the promise of the Internet.
[10:58] I know there's controversy about what the Internet was really for. It was created, but one of the stories,
[11:03] I think one of the motivations of some of the people who built it, was to create something that would survive like a nuclear war.
[11:09] I think that that's pretty cool, bringing this full circle back to a highly resilient application
[11:17] that can run in many different places in many different ways, so that you don't have to rely on someone to keep the servers up and running
[11:24] to have confidence that your application will still function. - Okay, so to you, it seems like it might be as much about resilience
[11:34] as it is about security in terms of funds and trusting that your funds would be safe in a Web3 or crypto context.
[11:48] Let's dive into a little bit about traditional web hosting. Either one of you can jump in on this.
[11:58] How are traditional web applications hosted and delivered to users, and what are the pros and cons of that?
[12:09] - I'll take this real quick, and then Joaquim can give his thoughts. I mean, usually you have either a server or a CDN.
[12:16] I think that tends to be the way that most people have their app running, is that if you have a server,
[12:22] then there is literally a single computer on the world somewhere running, maybe Linux, running some sort of operating system
[12:31] that you'll then load up with, say, Node.js, if you're a JavaScript developer like me,
[12:36] and then when someone goes to your website, they will hit a URL that will route them to that computer,
[12:44] and then your computer talks to that computer, that computer hands you a website.
[12:48] CDN would be when some sort of service has built out somewhat of a globally distributed network of different computers,
[12:56] and instead of just having, like, code running, you would maybe have, like, static assets.
[13:01] It could be just an index.html file that returns a website. And so for that, if a user goes to some URL,
[13:10] it could get routed to different computers, kind of whatever is going to be closest to them,
[13:14] literally on the earth, because the speed of light actually is noticeable
[13:18] when you are trying to talk to a computer all the way across the earth. You'll have some latency.
[13:23] So those have been things like Amazon and Google and Azure have usually been what we call the layer one clouds,
[13:31] which just expose these resources to you. And then you have things like Vercel or Netlify for the front end
[13:38] and things like Railway or Fly for the back end, which kind of build high-level abstractions on top of those layer ones
[13:45] to make them easier for developers to use. And I have worked for a company like this.
[13:49] I used to work at Egeo, which was a deployment hosting kind of company with a big global CDN.
[13:56] - What do you have to add to that? - Nice, yeah. And then a hugely important component is the DNS system,
[14:03] the Domain Name Resolution system, which translates a human readable name into an address.
[14:13] Of course, this all sits on top of the internet, which is IP/TCP packets.
[14:22] IP addresses are controlled by your internet service provider. Everything is transacted across internet backbones,
[14:33] which are owned by telecom communication companies. So there's a lot of infrastructure, a lot of pieces,
[14:42] a lot of providers that are involved and that you're trusting in the process. So when I'm a user and I want to go to a website,
[14:52] what I experience as the user is I click into my address bar and I type in either a specific web URL,
[15:02] like you mentioned, a DNS name, dash.org, and then some magic happens and then I get some pixels on my screen.
[15:13] And you're saying what's happening is, we're not going to go through the whole history and structure of the internet,
[15:19] but the user level experience is I put in a name or a search term, and if I put in a search term,
[15:26] then my browser is defaulting to some kind of Google internet search, which could be Google or Brave or whatever.
[15:36] And then I click on results from that search term. But now in a decentralized context,
[15:46] what has to change in order to have your users have whatever they're trying to accomplish with,
[15:57] you know, I want a decentralized application and I want whatever that means to them, more resiliency, more security.
[16:06] How is the user experience different for decentralized applications? Can you even have a traditional user experience by putting search term
[16:17] or a URL into an address bar in a decentralized application context? Yeah, and that's where it starts to get interesting.
[16:32] If you, and where should we start? So like the domain name, for example,
[16:42] some people consider DNS somewhat distributed because it's a system with lots of different, it's portable.
[16:51] You know, you can choose different DNS providers. But if you want to resolve a name, a human readable name to a computer address,
[17:02] there are some interesting new ways that are available to do that. For example, blockchain now offers a name service.
[17:13] The Ethereum name service was one of the first ones where you can register a domain name essentially on the Ethereum blockchain and then connect with that
[17:23] an address or any arbitrary text. This continues in the tradition of location based addressing,
[17:32] which is that you provide a name and you resolve that name to an address that tells you exactly which machine to go to.
[17:45] Now, there's another paradigm. Meaning which IP address to get?
[17:50] Exactly, which IP address, which is comparable to like a postal address. You know, it's just an address that tells you where to go.
[18:01] A new paradigm that Protocol Labs started to pioneer with IPFS is content based addressing.
[18:09] So instead of specifying specifically where you go to get the content, you hash the data, you get a signature from the data and you use that signature
[18:24] as the address and it's called content based addressing. So in IPFS land, if you have a signature of some resource like a website,
[18:35] you can announce that signature to the peer-to-peer network and you'll get responses back saying, "Oh, I have that. Oh, I have that."
[18:46] The signature helps you get started. It gives you a hint of where to look, but it doesn't specify exactly where.
[18:54] And there can be any number of places that can resolve that, can allow you to get that content.
[19:01] So domain resolution is one component of decentralization that's a part of IPFS. But there are several options and that's just the one component.
[19:16] So like I mentioned before, we've got database and storage and collaboration and hosting to discuss as well.
[19:24] But let me pass it back to you for a comment or Anthony for elaboration further. Well, you did mention IPFS and I don't think that we've actually defined that term yet today.
[19:36] But can either of you just tell me what's wrong with our traditional apps that we would even want to go towards more of a decentralized system
[19:47] that maybe IPFS could help solve? I can give one specific example from myself.
[19:57] That is the wallet that we've been building in the incubator, which is currently hosted at wallet-incubator.dev, I believe.
[20:06] If you go to that site, you'll be given an application that is a web wallet. And that web wallet can do things.
[20:18] You can enter a 12-word mnemonic. And if we were bad people, we could literally have our application
[20:27] just taking those 12 words and stealing all the funds. So that's one area where I want to get the most secure and the most,
[20:41] I would say decentralized, but I don't care about decentralization. I care more about security and decentralization might be a means
[20:48] and content addressing might be a means. But yeah, help me and the users or the listeners understand
[20:57] what is the problem with location-based addressing that we know and love today and we've used for whatever, 30, 40 years.
[21:07] Yeah, well, I'm not sure if this is necessarily what you have in mind when you're asking this question, but just because I know this is near and dear to your heart,
[21:13] you would not need to create an account for a service. Like if you wanted to get a domain name, usually you got to sign up for Namecheap
[21:22] or any of these domain things. You also, if you're going to host it somewhere, you got to sign up for your Amazon account.
[21:28] You're going to have your identity linked to all these things. You got the, even DNS itself, you usually have to give it an address,
[21:35] which then you have to get an extra service to obscure that. And that all goes away with IPFS, if I'm remembering correctly.
[21:43] Okay, let's define IPFS and tell people what that is and what problem it's solving. Interplanetary file system because it runs on Mars.
[21:54] That's where its base is. Okay.
[21:58] Walker, can you? Yeah, literally, they wanted a system where,
[22:03] a distributed storage system where it can work over long distances. It can synchronize and be verified without necessarily needing an instantaneous connection.
[22:21] But at its core, it's a distributed file storage system that has an addressing mechanism built in that we started to talk about.
[22:37] It allows anyone to spin up a node and host files on it. In that way, it's sort of like a BitTorrent, an evolution of BitTorrent, more generalized.
[22:56] And yeah, its core feature is using this content-based addressing instead of location-based addressing.
[23:06] So your addresses specify what you want, not where you get it. And the other neat component about the address is that if you have an address
[23:21] and you get content, you can use the address to confirm that not a single bit of that content has changed.
[23:28] So you start getting into the ability to verify and validate that what you've received at least matches the address that you were given.
[23:41] Now, you step one step back and you have to ask yourself, how did you get the address? And is the address itself ultimately correct?
[23:50] So it's almost like a never-ending, "Well, why is that? Why is that?" type of situation. But IPFS, at its core, at least introduces the concept of verifying that the content
[24:04] that you ask for is actually real, authentic to what you requested. And it can be served from anyone and doesn't have user accounts or anything like that.
[24:24] And yeah, it's been used now extensively for many blockchain-associated applications. NFTs almost universally are stored in IPFS network, lots of other use cases.
[24:48] But that's some of the basics of IPFS. >> So you mentioned if you know what content you want, you can just search for that content
[24:58] and get that content instead of going to a location like dash.org or incubator-incubator.dev. But so are you suggesting -- so what would be the user experience of somebody that's trying
[25:14] to retrieve a website that's hosted on IPFS? Do I -- can I -- if I don't know what I'm looking for, how do I get that content?
[25:28] Or if I do know what I'm looking for, like, what's the overall user experience? >> Because I know that IPFS, you're getting basically this content ID, the CID, and that
[25:45] represents -- that's a hash of the content of the data of the application. And that's great.
[25:53] But what if I don't know that hash, or am I just expected to know that content ID number and then go to a traditional domain and put that in somewhere?
[26:08] Or how does that work? >> Yeah, it's a great question.
[26:14] Search is another component. Discovery is another important component.
[26:20] With this technology, we're essentially in an equivalent era to the pre-search engine era.
[26:27] So there's some rudimentary search engines. But essentially, if you don't know the content address, you've got to discover it somehow.
[26:36] So you're basically going to Google or better going to the specific website you trust or getting it directly from somebody you trust.
[26:49] But yes, discovery is an unsolved problem in the decentralized space. We're early days.
[26:57] >> Okay. I want to introduce just show some things on screen while you guys are thinking about
[27:06] some other things that you might want to share. But I want to just cover at least some of the things that we have already worked on
[27:13] in the incubator and which I hope to work on in the future. So right here, we have a bounty called IPFS-PlatformIntegration that's showing that's completed.
[27:33] We started this quite a long time ago, and this is briefly what we've done. And I'm just going to scroll through this just so people can see this and don't necessarily
[27:47] have to go to our board. It starts chronologically at the bottom.
[27:58] So you can see back in 2021, we started this project and we got some deliverables out of this.
[28:07] One of those, you can see this, Imestin, I don't know how to pronounce his name, in Israel. Casillas was working on this a while ago, and we have this Dash Platform IPFS Hello
[28:23] World repository that was created. And Anthony, one of the things I'd like you to do is pick this back up again, three years
[28:32] ago, pick this back up, see if it works with current version of Dash Platform, and maybe we can do some streams about this.
[28:41] One thing I noticed, there was a video as part one of the deliverables to just demonstrate this very basic Hello World application.
[28:54] It was posted on D2, which I believe also uses IPFS under the hood. And one of the ironic things that I found was that this, if I'm refreshing the page,
[29:08] I don't think that the video is available anymore. Talk about pinning, pinning and garbage collection.
[29:15] I'm not sure if that has anything to do with the issue here, but I know that if you don't really know what you're doing with IPFS, you might not save something that stays there
[29:23] forever. Yeah.
[29:25] And the other thing to notice here is that d.tube is the URL. So you're still, it's like that meme, the, and sorry, there's just a blank screen here,
[29:40] but that's the experience I'm getting, right? This is what I get.
[29:46] It's like that meme, the Scooby-Doo meme where he's got the mask and you pull off to see who the villain was all along.
[29:55] And it's like, okay, actually it's just DNS under the hood. I don't want that to be the case, but that does seem to be the case that a lot of the
[30:06] IPFS experience is actually DNS under the hood and HTTP. So we could talk about that.
[30:16] Anybody have anything to say about that while I just briefly scroll through this other bounty that we have that's a little bit more current?
[30:28] We're partly, I think, held back by the browsers we use in a certain way. If you're using a browser that only recognizes DNS, then well, you're going to be using DNS.
[30:39] I know Brave actually has native IPFS support that you could put in, like not HTTPS. You can put in like an IPFS, just thing, I forget the proper terminology to describe
[30:51] this, but Walker could probably give some more specific technical description of that. You're good.
[30:59] So that would be one thing that you want to do is that, you know, there needs to be a way to interface with regular browsers.
[31:06] So that's kind of why we end up pigeonholed into DNS to a certain extent, unless you trust your users are going to be using a more kind of crypto-native browser.
[31:16] Okay. Hey, Rion, tell me what did that IPFS dash platform app do?
[31:26] Can you just connect the dots? The hello world one?
[31:32] Yeah. This one.
[31:34] Basically, I mean, I'd have to review this, but I think it was basically just trying to say what's the most basic thing that we can do where we're hosting a hello world application
[31:46] that combines the two technologies. And I'd have to really look at it.
[31:52] It looks like just reading the readme real quick that it gave you a front end interface to like upload a picture or something like that.
[32:00] The picture lives in IPFS and maybe there's a hash of it or something stored on. I don't remember exactly, but I was just pointing out that we have done some things in the past
[32:12] with this, and I hope to pick that back up again now the dash platform is getting a little bit more stable.
[32:17] Yeah. Okay.
[32:19] That makes sense. Yeah.
[32:21] If you can have an index.html saved by an IPFS node, and if you have the content address for that, and if you have the Brave browser, you can put IPFS colon slash slash, and then
[32:37] the content address and Brave will pull it right up, provided that there is at least one person providing it here again, it's decentralized.
[32:52] So there's no one entity that's ensuring that there's at least one node with your data. So you would need to either be the interested party that ensures that your data is being
[33:10] provided, or you might need to pay multiple different entities to host that data on IPFS for you.
[33:20] Either way, you can't get away from the fact that somebody needs to host the data. And so there's now lots of different ways that you could approach in order to get whatever
[33:35] kind of service guarantee that you want. And as soon as content, as soon as no one cares about the content, then the system is
[33:45] going to naturally take care of it, remove it. The system, you can't have a system that just accepts everything indefinitely, that will
[34:02] grow too big. So there's a garbage collection mechanism that kicks out stuff that isn't being queried
[34:10] for, and there's lots of different parameters you can tweak on that, but a decentralized system in order to combat the fact that you can't carry everything has some of these other
[34:28] maintenance factors that you have to consider and can affect the user experience. Yeah, I mentioned pinning.
[34:37] This is what the garbage, pinning is to get around the garbage collection issue, and there's pinning services.
[34:45] So it's like, well, we got back to relying on a service now. But you can also, as I said, just run your own node.
[34:54] There's also even, there's different platforms, I'm blanking on the name right now, that will give you kind of like a part, you know, I was talking about web two, web three, we've
[35:04] talked about this a lot, Rion, where they'll give you kind of like a web two like deployment platform that syncs to a GitHub repo, and then they will stick that onto IPFS for you.
[35:15] So those can be pretty cool as like an entry point for people who don't want to like fully imbibe this whole IPFS mindset, they want kind of like a partway, and then they can
[35:24] get something that does have like a content hash, and then they can kind of work backwards from that, and then maybe start to get more comfortable with the system, eventually run
[35:31] their own node. But there's a lot of companies out there that are trying to kind of meet people halfway.
[35:38] Yeah, and I guess there is so much to say about this topic that I, I don't want to discourage users too much by throwing so much at them that they don't really understand how to even
[35:55] get started with this. But this this conversation is mostly just to introduce the topic.
[36:00] And there's there's a lot more to say. But one of the big one of the big takeaways that I want people to to go out with is not
[36:07] that we're closing off the show, I think we have about 20 minutes left. But one of the big things that I want people to take away is that decentralization is a
[36:17] spectrum and not a binary, either you have a centralized app, or a decentralized app. It's more about scales of trust, and which level of trust and verification and security.
[36:34] Where on that spectrum do you stand? And do you where do your users stand?
[36:40] Where do you think that your users stand? And then you can then design an architecture that is that accommodates where you want to
[36:50] stand where you think your users want to stand. Because that is the experience that I've had with IPFS is that it does kind of you do end
[37:01] up coming back to DNS and trusting gateways, like you mentioned, and pinning services. I think pinata was one of them that they have a great name for what I used.
[37:16] Exactly. Yeah.
[37:18] And then there. There are other under the hood services like Walker, you and I talked offline about this
[37:24] about DNS gateway or was it gateways, not gateways, DNS link. Can you tell us a little bit about DNS link and what how that gives users the same overall
[37:42] user experience, but with potentially higher security. And again, listeners, this isn't intended for you to you won't understand all this,
[37:53] but I just want to introduce some of the high level concepts. Yes.
[37:56] So we've talked a little bit about the ideal, the ideal decentralized application is one that you provide an address and and it gets resolved from any number of nodes.
[38:14] And ideally, in the course of providing the address, you verify the content so that you know, no middleman has tweaked the code.
[38:28] And then you interact with the blockchain through this application. So so that's the ideal.
[38:35] And if you're running brave, you can get pretty close to that because it has IPFS built in. Most users aren't running brave.
[38:45] And and so now we enter the world for anybody who's brave as a browser and is chromium based. So it's not really that and it's not that wild for a regular web user.
[38:56] It's not that different than using Google Chrome. That's right.
[39:01] That's right. But if we step back to the average web user, we're far away from that ideal.
[39:12] You can't request and you can easily request an IPFS resource from a vanilla browser, you need either a web application that's got a heavy framework built into it or or you need
[39:27] to add an extension. So coming at it from the perspective of the average web user, you have to employ a lot
[39:36] of a lot of different hacks to get different components of this decentralized delivery. And so since the browser doesn't speak the IPFS protocol, there's some hacks to to get
[39:52] around that. The two most notable are, as you brought up this, this DNS link.
[40:02] So DNS is a very flexible system in that you not only can specify a domain name and an IP address, you can create a generic record, a TXT record, put whatever data you want in
[40:17] there. So I can specify walker.com.
[40:24] If I own that domain, I can create a DNS text record and I can put a CID in there so that somebody could request, make a DNS request and get the CID and then use some other service
[40:42] to request the content that that CID points to. So DNS link, as it's called, is just a way to use the existing DNS system to deliver
[40:54] at least an address. Another mechanism to deliver content to regular browsers that don't understand the protocol
[41:06] is to use a gateway and that that's essentially a server that provides a standard HTTP experience, which is the default protocol that the browser speaks in order to request a website.
[41:22] So you can request from an IPFS gateway and you would put a normal domain name in, which with HTTP and slash, and then you put the content address.
[41:36] So you get that content address from DNS link, then you can put it in the URL to a gateway and that gateway then runs the IPFS subsystem and requests your content and then delivers
[41:53] it to you right there. So that is one way to have a normal browser deliver IPFS content, which is a neat hack,
[42:07] but it doesn't end up allowing you as a user to verify that the content hasn't been changed by anyone in the course of transmitting from server to you.
[42:26] So it still has an element of trust, but it's one step closer to that goal. And there's some new protocols that can help gateways provide that verifiable component,
[42:47] but those are still being worked on. So let me step back and see what you think.
[42:53] But in terms of getting the content address and delivering it over a standard protocol, there are a couple things available and new ways are being added, new holes are being
[43:09] plugged, but we're still trying to get to this ideal and we're a ways off. Yeah, I saw you had this trustless gateway specification.
[43:19] I saw this link in the blog post that Daniel wrote. Could you talk a little bit about the specification?
[43:25] Yeah. So when you request IPFS content, the address is a hash or a signature of the content.
[43:41] I think if you're a developer, you're familiar with hashes in Git. When you make a commit, that commit is a hash for your content and allows you to verify
[43:53] that the content hasn't changed. In IPFS, it's a little squirrelly in how it works in that it breaks everything apart into
[44:06] chunks. So one file, you could figure out a hash for the file, but IPFS will actually break a file
[44:17] into small pieces and then compile a tree of hashes and so your IPFS content address represents that tree.
[44:28] So it's more flexible that way, but that makes it a little bit harder to use. So when you request a file with IPFS through a gateway, the gateway will request all of
[44:44] these small chunks, they will put them all together for you and then deliver you the file.
[44:51] Now, if the chunks have been put together, you then lose the ability to calculate the hash that verifies everything.
[45:03] So this trustless protocol is saying, okay, a gateway will provide you the content, but instead of putting all these chunks together, they will just deliver you the browser, all
[45:18] of the chunks, and then you can go ahead and combine them together and then that allows you to actually verify it.
[45:25] So the trustless protocol is a way to get IPFS content over HTTP and still retain the ability to validate it.
[45:37] Okay, so that's one step closer. If we take a step back, what are we trusting in this scenario now?
[45:46] Because that sounds really good. And that is the fact that the browser still doesn't speak IPFS directly.
[45:54] So you still need to request that initial website shell that knows how to understand all of this.
[46:02] So who are you getting that shell from and has that shell been modified in any way? So the problem hasn't totally been solved.
[46:12] We've solved a big component of it, but there's still an element that's still web 2. But yeah, that trustless protocol is pretty cool in that it allows you to get a little
[46:24] bit closer to receiving content from the decentralized network and retaining the ability to verify it.
[46:33] Yeah, great. You're speaking my language.
[46:38] I'll just say that it's great to have a couple of people who know this technology pretty well and are able to speak honestly about the pros and cons of that.
[46:50] In preparation for this call, I did some searches to find what the latest state of IPFS was, because last time I checked, like three years ago, it was in this state where, like you
[47:05] mentioned, there's some holes and you patch some holes and then some other holes appears and you patch those holes.
[47:11] And it was a little too much in flux for me to want to do too much with it. But I think it might be getting to a little bit of a more mature state.
[47:20] And I want to show up on the screen here, let's see, this article, which I found was very honest, coming from somebody that was also working for Protocol Labs at the time
[47:38] maybe. You know this individual, Anthony, Daniel Norman, right?
[47:44] Yeah, I had him on my podcast, actually, back in 2022. He worked at Protocol Labs, he's at IPFS Shipyard now.
[47:52] Yeah. And I asked both of you to read this article.
[47:55] What were your main takeaways from this article? There's a lot going on in it, a lot of it was kind of review for me, stuff I had learned
[48:04] in the past. And there's a good chunk of stuff I'd never even heard of before.
[48:08] The Helia stuff really stuck out to me as something that it's like they're kind of, you know, I'm a JavaScript dev, JavaScript stuff will always jump out at me.
[48:17] That was really, it seems like that's what's aiming to kind of give me a lot of tools to work with with IPFS.
[48:24] And even I was messaging Daniel, he mentioned they have these new things like Verify Fetch and a Service Worker Gateway, I'll drop both those links in as well.
[48:35] He said these are not in the blog post, but that they're kind of some work that's happened in the last couple months.
[48:41] So yeah, I always think that stuff is kind of exciting. I had been just kind of dipping my toes into some of their JavaScript tooling when I first
[48:49] learned this stuff back in 2022, but didn't really learn how all of it worked. I think Helia is kind of what they've transitioned to being their real main focus for the JS
[49:00] dev. Yeah, it's a good, it's a good comprehensive up to date article.
[49:06] Keep scrolling. There's a nice point that I just alluded to that I want to read.
[49:13] And by the way, these markings are my own highlights as I read the article. The colors don't mean too much.
[49:22] Stop me when you find what you're looking for, Walker. But Helia was one of those things and it's near the end of the article that stuck out
[49:31] to me as something that we should look into in the incubator to try to see if we can create a framework around that that uses dash platform and an IPFS using Helia.
[49:46] Here's the Helia stuff. Helia is just a rebranding for the JavaScript IPFS implementation and they created the definitive
[50:00] implementation and would call it like JavaScript IPFS. And then in order to encourage other implementations, they've rebranded each of those to a name
[50:12] to give space for other JavaScript implementations. But they want to take over like the whole name, like this is the canonical IPFS JavaScript
[50:23] framework. So they gave it a name so that other people could compete on a level ground.
[50:29] That's good. Yep.
[50:31] That's right. They did the same thing with the Go reference implementation.
[50:33] It used to be Go IPFS. Now it's called Kubo, K-U-B-O.
[50:38] Do a search for today, Helia. I'll get down to the bottom because we're almost to the bottom of the article and then
[50:49] hopefully you're reading. I didn't see it.
[50:51] It is toward the bottom, but I'm looking for an icon. I didn't see it.
[50:55] Helia can fetch. Helia can fetch.
[50:57] I see what you mean. It's in the section of verifying top-level pages, sub-resources, and async data.
[51:08] Okay. Give me a better search term.
[51:12] Just do verifying top. Try that.
[51:14] Verifying top. There we go.
[51:16] Yeah. And then pop down one, hit enter, and then scroll down a little bit.
[51:22] Keep scrolling. Looking for the eye.
[51:24] Yeah. The eye icon.
[51:26] Okay. Yeah.
[51:28] You got it in pink. Verify async data and sub-resources.
[51:32] However, top-level verification without deeper browser integration remains an open engineering problem.
[51:40] That's exactly what I just talked about. The shell to interpret IPFS hasn't been solved yet.
[51:51] And what is that problem that they're alluding to? Explain it with a little bit more detail.
[52:02] What problem they're trying to solve and what is not quite solved yet? Hey, Daniel just hopped in the chat, actually.
[52:10] Right on. Oh, cool.
[52:12] Very cool. Yeah.
[52:14] Getting solved as we speak. When you request a website, you get an index.html, and that HTML, it doesn't know how to speak
[52:25] IPFS. So you need to give it the ability to understand it, and then you need to give it the ability
[52:33] to hydrate itself, to install in itself whatever IPFS content that the Helia platform brings into the browser session.
[52:48] So you just still have that problem. I've got the data now, how do I connect it up with my React framework or my Vue framework
[52:56] or that sort of thing? Well, great.
[53:00] And as Daniel just hopped in the chat, I want to give him a personal invitation to come on the show.
[53:06] I'm not exactly sure what week that would be. I've got to check what our schedule is.
[53:13] But I would love to have Daniel come in after we have had some time to play around with the current state of things, including the current state of IPFS and the current state
[53:23] of Dash platform, and know what problem we're trying to solve here. Because that is one of the most important things is knowing what problem you're actually
[53:37] trying to solve and why you're trying to solve that particular problem. Because there's so many technologies and so many solutions and so many places on this
[53:46] scale of decentralization, security, usability, that there's way too much unless you are really focused on it.
[53:57] Like Daniel just said, the problem space is very wide here. So any last closing remarks about what is a decentralized application anyway?
[54:10] I think I have a decent answer, but I'd like to hear from you two. What is a decentralized application after having had this discussion?
[54:20] I can go first and then you two can close it out. I would say in response to what you were saying about how this can be really overwhelming,
[54:27] and we kind of want to give a high level overview and for people who may have had trouble following along with this, what I would recommend to people who are new to this and think like
[54:35] this is cool, but I don't really know where to start. Start by just trying to get like a index.html file on IPFS and then expose that, because
[54:45] that's going to be just like a static website and it's a thing that you can conceptualize and you can think about.
[54:51] And that's something that can get you that instant kind of feedback of like, oh, I get this.
[54:57] Like for me, that was the moment where I really got IPFS. Once I had just HTML, regular HTML file on IPFS and I could access like, oh, this is
[55:07] what a decentralized website is, it was a really kind of like aha moment for me. So that's what I would recommend to people if they're really overwhelmed and confused
[55:15] right now. Very cool.
[55:17] And I think that we should probably do some streams, just some longer form streams about that, Anthony.
[55:22] Yeah. Yeah, I could run through my tutorials and update it.
[55:26] All my links are dead and all the content I put on is no longer accessible, so I need to go through and just run that whole thing again.
[55:32] Go through it again. Walker, what do you say?
[55:35] Yeah. That's a great tip.
[55:37] I've just been thinking about your IPFS incubator project. It would be neat if you created that shell that you imbue that project with Helia and
[55:48] the ability to, yeah, present the user with a nice badge that says this is the content address and we verified that everything that's come in is correct and then we display on
[56:04] the screen. That would be a neat hello world application.
[56:08] So in the blockchain world, the blockchain is the backend and the user cannot directly interact with that.
[56:18] You need some sort of frontend. So it's been easier to create the backend first.
[56:24] You have to have the backend and now we're working on delivering frontends that are, you know, that pair nicely with that.
[56:34] So a frontend that has trust and verification properties. We're still early days, but ultimately a DAP, a decentralized applications goal, is that
[56:46] the user has the ability to verify the content for dealing with money on the blockchain. So it has to have some security guarantees.
[57:00] The technology exists to do this and to have a nice user experience, but it's still, it takes some time to integrate, especially when you've got big incumbent interests that want
[57:14] you to use their web hosting service. They want you to use their name providing service.
[57:20] So there's some pushback to implementing it. It's not going to be as easy as we'd like.
[57:29] But progress is being made and there's good resources like the one Daniel wrote and active communities that can help you make the next steps.
[57:41] But yeah, it's, you know, ultimately with decentralization, like Rion said, it's a spectrum and there's a lot of pieces to understand.
[57:53] You can't just, you can't just have one decentralized solution and that solves it all. You know, there's a lot to consider.
[58:03] You have to pay, you have to pay for it to some extent, but the promise and the potential is there, which is, I think, why we're all here and expanding where we're at is part
[58:21] of the process to get to where we want to be. I think those are some good closing remarks.
[58:28] And I think that we'll probably just leave it right there. And please tune in, subscribe so that you get the notifications for upcoming.
[58:38] I think that's the first time I've ever asked people to subscribe to the channel. We get more views than subscribers.
[58:44] Smash that like button. Yeah.
[58:47] Which is kind of funny. But yeah, I'm looking forward to the further, further conversations around this and actual
[58:54] code coding and demos. Daniel, thank you very much for, for coming in on the show.
[59:00] And hopefully having you discuss this when we get Daniel on, just way too big to hit on now.
[59:08] But yeah, this is a good point. Cool.
[59:10] Yeah. Smash the like button and we'll, we'll, I'll have you on, we'll, we'll reach out to you.
[59:16] Anthony will reach out to you and we'll, we'll get you on the show and talk more about this. So thanks everybody.
[59:21] And we'll see you next week. Bye.
[59:23] Thank you. 
