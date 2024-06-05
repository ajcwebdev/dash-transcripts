---
showLink: "https://www.youtube.com/watch?v=MdmVNVDSsbg"
slug: "metamask-for-dash"
title: "MetaMask for Dash: Wallet/Extensions Update"
publishDate: "2023-06-05"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/MdmVNVDSsbg/maxresdefault.webp"
---

Ash discusses three Dash wallet extension projects aimed at enabling seamless user interactions with Dash and the Dash platform.

## Episode Summary

tl;dr: Ash presents three wallet extension projects: a layer one Dash transaction wallet, a platform-focused wallet enabling communication between DApps and the wallet, and a user-friendly wallet with chat and social features. The goal is to create an ecosystem that empowers users and developers to interact seamlessly with Dash and the Dash platform.

## Chapters

00:00 - Introduction and Overview of Wallet Extension Projects
Ash introduces three wallet extension projects: a layer one transaction wallet, a platform-focused wallet, and a user-friendly wallet with chat and social features.

06:19 - Layer One Dash Transaction Wallet Demo
Ash demonstrates the layer one transaction wallet, which focuses on basic Dash transactions and account interactions using existing libraries and SDKs.

16:55 - Platform-Focused Wallet Extension
The platform-focused wallet aims to create a library for DApp developers to communicate with the wallet, enabling seamless user interactions with Dash platform features.

30:39 - User-Friendly Wallet with Chat and Social Features
Ash presents a user-friendly wallet that combines layer one and platform features, with a focus on chat, social features, and a seamless user experience across desktop, mobile, and browser extensions.

39:23 - Future Goals and Ecosystem Development
Ash discusses his vision for expanding the wallet's features, empowering users, and creating a supportive ecosystem for developers to build DApps on the Dash platform.

## Transcript

[00:00] (dramatic music) In 2021, the Nigerian government pushed out at CBDC
[00:08] the e-Naira. - This made Nigeria the second country in the world
[00:11] after the Bahamas to roll out a CBDC. And certainly with 230 million people
[00:16] and the largest economy in Africa, the biggest political jurisdiction to do so.
[00:21] The CBDC efforts have been led by Godwin Emefili, who since 2014 has headed up the central bank
[00:26] of Nigeria or CBN. In July of 2021, Emefili announced
[00:31] the pending launch of the e-Naira using proprietary software built on Hyperledger fabric
[00:36] with mobile apps for consumers and merchants. Three months later, in partnership with 33 banks,
[00:42] the e-Naira was launched. To use the e-Naira,
[00:44] individuals go through a tiered KYC system, the transaction and balance limits
[00:49] hinging on the level of information they provide. Once the individual's biometrics are captured
[00:54] by the Nigeria Interbank Settlement Services Database, they become a number,
[00:58] a bank verification number assigned to them for life. Emefili stated in no uncertain terms,
[01:04] "The destination, as far as I am concerned, is to achieve a 100% cashless economy in Nigeria."
[01:10] This, despite the fact that Nigerians were overwhelmingly reliant on cash.
[01:15] - Nigeria is a really cash-heavy population. They use cash a lot.
[01:19] - Fully 90% of business in Nigeria was cash-based. So it was no surprise that a year
[01:24] after the e-Naira was launched, only 0.5% of Nigerians had downloaded a wallet.
[01:30] An IMF report about e-Naira penetration, which begins by stating that,
[01:34] "CBDCs have become one of the fanciest concepts among central bankers,
[01:39] called the adoption rate, disappointingly low." - Given this pathetic showing,
[01:43] the Nigerian government then turned to hardball. First, they mandated discounts for paying in CBDCs,
[01:49] then they redesigned the physical currency to flush out informal cash.
[01:54] - Under the guise of looking out for the weak and vulnerable,
[01:56] mitigating political corruption, and deterring counterfeit notes,
[02:00] Nigerians were told they had to turn in their old banknotes as they would cease to be considered legal tender
[02:05] at the end of January, 2023. Nigerians soon found that this new banknote scheme
[02:10] was part of the push to force them away from using cash and into using the e-Naira.
[02:15] Because when they turned in their old banknotes, they were not given new banknotes in the same amount.
[02:20] - Finally, they went nuclear, limiting cash withdrawals from ATMs to $40 per day
[02:25] to force people into the CBDC and to achieve a "100% cashless economy."
[02:33] - Despite claims by MFLE that everything was gonna work smoothly,
[02:36] there was a shortage of new banknotes. That's no surprise because in just one calendar year,
[02:41] the physical currency supply of cash was halved. - The latest cashless policy of the Central Bank of Nigeria
[02:48] remains a topical issue among the citizens. While some stakeholders applaud the policy
[02:53] as a step in the right direction, many others have critiqued the initiative
[02:59] as insensitive to the common man. - We are telling them and we are warning them
[03:04] that they should not allow Nigerians to suffer. - The cash limits led to complete chaos.
[03:09] People could not buy groceries. Stores could not stock their shelves.
[03:13] Gas stations ran out of fuel in the largest oil-producing country in Africa.
[03:19] Nigeria was rocked by widespread riots, including burning down banks
[03:23] and even central bank branches. - With the cash supply made so tight,
[03:27] the CBN claims the adoption rate for the e-Naira jumped from 0.5% to 6%.
[03:33] - The Naira redesign and cash withdrawal limit policies have resulted in a sizable reduction
[03:38] in currency outside the bank, indicating expected improvement
[03:43] in the potency of monetary policy tools. - MFLE's complacency for the well-being
[03:48] of people on the ground was echoed by Simon Chantry,
[03:51] co-founder of Draper Utah-based Banking Innovation Through Technology, or BIT,
[03:57] with whom the CBN partnered to release the e-Naira. During a recent Zoom meeting,
[04:01] Chantry likened the harsh policies imposed by the CBN to a creative option.
[04:06] - I wouldn't be surprised if we see central banks try different creative options
[04:09] to see what's gonna stimulate adoption. - I can only say that the adoption rate
[04:14] continues to increase and improve. And everything is being done to continue
[04:23] to make sure that this going to go up. - And to try to further push top-down adoption
[04:28] onto more Nigerians, MFLE and the CBN is now courting
[04:32] New York-based tech outfit R3. MFLE purports to be a humble civil servant.
[04:37] - The truth is this, you know, we are all servants. We are serving Nigerians.
[04:44] - But really, MFLE is most comfortable in his ivory tower, where he has received praise from technocratic cohorts
[04:51] who seek to control and surveil. Overall, the draconian measures by MFLE and his cronies
[04:56] to transition almost a quarter of a billion people from a cash-based existence to one they manage
[05:01] was shoddy, to say the least. As Bloomberg reported,
[05:05] Nigeria has been among countries at the forefront of initiatives
[05:08] to establish and support blockchain-based digital versions of their hard currencies.
[05:12] And like most of them, it has struggled to win wide adoption.
[05:15] Still, numerous central banks around the globe are crafting similar efforts.
[05:19] Indeed, the regimes of 114 countries, representing 95% of global GDP,
[05:24] are looking into CBDCs. Their ambitions are driven by the need
[05:28] to keep up with private sector innovations in digital payments,
[05:31] which have pushed consumers to go cashless and led to the creation of cryptocurrencies
[05:35] and stablecoins. The sentiment was echoed by the Atlantic Council,
[05:39] which noted, "The world's central banks have realized that they need to provide an alternative
[05:43] or let the future of money pass them by. We are at a place in history
[05:47] where we can move away from centralized money and its inherent control, corruption, and coercion.
[05:52] We need not be passive. Waiting to see how things unfold,
[05:55] we can be active, building better alternatives,
[05:57] building the future of money, which will empower individuals and liberate humanity.
[06:02] What say you?" - Damn, son.
[06:12] I liked that newsreel. I could spend a half an hour just discussing that.
[06:17] Sorry, go ahead. - Right, right.
[06:19] Welcome to Incubator Weekly, everybody. I have with me today,
[06:22] not one, but two incubator strategists. As always, my co-host, Rion,
[06:27] and also strategist, Ash. How are you, fellas, today?
[06:31] - I'm really good, thank you. Yeah, really good, thanks.
[06:33] - Great. So we have a ton to cover today.
[06:37] Let's jump right in. We're covering not one, not two,
[06:40] but actually three wallet or wallet extension-related projects.
[06:46] Is that right, Ash? - Yeah, I would say they all kind of like sit
[06:50] within the same sort of general umbrella. The way I see these things being built
[06:56] is somewhat of two reference projects and then one sort of production project.
[07:00] The idea is that anyone can look at these smaller scale projects
[07:05] and see how a wallet is built, either layer one or interacting with platform,
[07:10] and learn from that without having to build a huge monolithic application
[07:13] that understands the workings of that. It's just a more granular
[07:16] sort of microservices-based approach. That's kind of the goal behind them.
[07:21] - Okay. - I would guess that also helps with debugging
[07:24] and things like that. - Yeah, exactly.
[07:26] - If you're experiencing some problem, you know it's one, two, or one of these three things
[07:32] instead of, oh, it's like the React framework or it's this wallet library
[07:37] or it's some other tangential thing. - Yeah, and they act as like an upstream sort of master
[07:44] where all of their benefits that's developed against those wallets,
[07:48] the reference wallets, will then be pushed down to any implementation of those.
[07:53] And even where they learn, for example, those two reference projects,
[07:57] if they learn from the work that you've been doing, they will then implement that.
[08:01] And likewise, it's that whole sort of rising tide for all ships that are using the same sort of process.
[08:08] So yeah, that's the goal behind. - Okay.
[08:11] Well, I know that we have some demos. Can we take a look at the first one?
[08:14] - Absolutely. Let's give it a go.
[08:16] Let's try. - Let's do it.
[08:18] - Okay. - Nice demos.
[08:20] Love demos. - I love demos, live demos.
[08:23] Interesting. Has it stopped sharing my screen?
[08:25] It has stopped sharing my screen. Let's share my screen again.
[08:28] Okay. All right.
[08:33] So, you know, live demos are sometimes prone to be going wrong.
[08:36] - Yes. (indistinct)
[08:38] - Okay. So to begin with,
[08:40] this one I actually built very shortly ago. As you can see, 8.53 AM.
[08:45] It is now 9.09. The reason being, it takes a little while.
[08:49] One thing we're developing on Dash right now against a platform specifically,
[08:55] but some of these tools, they take quite a while. There's a long sort of process
[09:00] because you're building a development project against another development project
[09:04] that's often in a state of flux. This will not be a long-term problem.
[09:08] You know, most people, for the vast majority of time, will be developing against test net and then live net.
[09:14] For us, it is a bit more complex right now because, you know, these things are changing constantly.
[09:19] You kind of have to build and rely on your own local structure.
[09:22] So this does take a while to build this project. Maybe, when I say a while, maybe five minutes,
[09:27] but you've got dependencies you have to build before that. So I wouldn't say this is the easiest
[09:32] for everyone to get running, but in the future, it will be a lot easier.
[09:35] And it will also be a lot faster because you would just install an extension
[09:39] from your browser store or, you know, just a load and unpacked extension,
[09:44] and it would take you, you know, 30 seconds to get this up and running.
[09:47] But anyway, as you can see here, I have built the extension just using
[09:51] sort of the build process within this Mayfair. - And what do you call this, Ash?
[09:56] Is this, 'cause I know there was one- - Yeah, so this is called the Dashbay web extension.
[09:59] I'm not really, that's not the name I gave it. That's just the original name from DCG.
[10:03] I just consider this sort of a Dash core reference extension. So this is all about layer one.
[10:09] This is just about doing transactions and accounts layer one interaction.
[10:13] There's no platform features in this one. This is purely transactional basis
[10:16] using existing libraries that DCG have published and are working on, the SDKs.
[10:22] You know, for Rion, for example, some of the work he's doing is a lot more sort of purist.
[10:26] It doesn't rely too much on the SDKs produced by DCG and their dependencies and things like that.
[10:32] Whereas this is built on that basis. So that, you know, different approaches to the same problem.
[10:37] - When you say extension, do you mean web extension? - Browser extension, yeah.
[10:41] So this is purely a browser extension. One key thing with the browser extension is, you know,
[10:46] it's kind of just a web app, but with some sort of concessions for Google sort of manifest
[10:52] and different browser limitations. Instead of a thing called a web worker,
[10:56] you have a service worker, but that's just like a little messenger behind the scenes
[11:01] that goes and pulls things from, you know, it's part of the communication layer between a webpage
[11:07] or a decentralized application and an extension. But this wallet doesn't really have any of that.
[11:12] This one, it's all about just the extension itself running as a wallet.
[11:16] So let's carry on with this and see if we can get this going. I'll go into a new tab rather than the recursion.
[11:30] Okay, so I'm going to load an unpacked extension and I am going to browse to my profile,
[11:38] dash Bray web extension. And I'm going to load up the folder
[11:43] for the Chrome extension. It can be shipped to Bray, Firefox, Chrome, whatever,
[11:48] any modern sort of browser. So yeah, there's no real issue in running it.
[11:54] And now I'm just going to pin the extension. So this is the, just the dash layer one extension.
[12:00] And I'll begin by creating a new wallet. - That's pretty.
[12:04] - Let's show my recovery first. Don't worry.
[12:10] This one key thing I'd say about these projects is they are not ready for production use.
[12:14] That there needs to be security audits. Do not go out there and start using this
[12:17] and putting loads of money behind it. It is a development project.
[12:20] It is not production use. This project is largely complete
[12:23] aside from some minor work on, you know, securing with pins and how the keys are stored.
[12:29] One, the developer behind this actually looked into all the major sort of extension wallets
[12:34] like MetaMask and how they securely store those keys. I'm not going to bother with the verification.
[12:40] I'm just going to click off it. This is just a shortcut for now.
[12:43] And you can see, I have a little dash wallet. There's no transactions or anything.
[12:47] So why don't we just test that out by going to crowdloads, nicely hosted faucet.
[12:53] Thank you. I will take the address, put it in there
[12:58] and see CPFFJ, coins. Oh, I entered it wrong.
[13:06] It looked like English. I can review this.
[13:09] Oh, two, okay. Hey, I've been awarded three dash.
[13:15] So as you can see, that balance is already reflected in there.
[13:18] So this works really well as just like a quick wallet in your browser.
[13:21] And this is just demonstrating all those sort of layer one features of grain transactions,
[13:25] broadcasting to the network in a very sort of minimal JavaScript focused way.
[13:31] When I say about like the web app and wrapping it for Chrome, the reason I say that is these kinds of lightweight wallets
[13:36] could be built easily for other devices. They can be built for mobile, for desktop
[13:41] or with different wrappers. And that's a key thing I want to touch on in the future.
[13:45] It's important for me to be able to deploy these applications to different things.
[13:50] I don't want any limitations. I want people to use the system that works for them.
[13:54] I want you to be able to sign on to a decentralized application by scanning a QR code on your mobile phone
[14:00] or anything like that. So I'm just gonna send the dash back to them
[14:04] just to show the same feature. I think the confirmations counts are wrong.
[14:09] How did it, is it upset with me? Something's upset.
[14:13] Well, we got there. We got some transactions going on.
[14:16] We should receive some things. It could be just a, let's just try it.
[14:21] Sad. Well, there you go.
[14:24] I could see it sending and receiving some dash. Well, you saw it receiving the dash, not sending it yet.
[14:30] But yeah, it seems to be. - Does refreshing a browser tab, does that affect it?
[14:32] - No, no, but it might've been sort of just reading something on the page.
[14:37] I could try closing, but if I close this, it'll break the whole stream.
[14:41] Different tabs run in different threads on your device, but the actual extension runs entirely
[14:48] in its own separate thread. So a different tab wouldn't necessarily fix it,
[14:52] but I was seeing if it was picking anything else up, but it doesn't look very happy with me.
[14:56] So maybe not now. I probably have a debugger somewhere.
[15:01] I mean, I could even show you, you can see errors coming up here.
[15:04] So I'd have to spend quite a lot of time to fix that, I'm sure.
[15:09] So yeah, there's definitely some kind of issue that's happened there.
[15:13] But this is a development project, and so it's not always expected to work perfectly
[15:18] and be production ready. - So one question about this one.
[15:21] I seem to recall that this project was spearheaded by DCG. I think you mentioned that also.
[15:29] - Yeah, yeah. - Are they intending to continue working on this,
[15:36] even if it's through the incubator and supporting that project?
[15:40] - Yeah, ultimately it's an incubator project now. Yeah, ultimately it's an incubator project now.
[15:45] So DCG originated this, it was an internal thing, then they weren't sure on bandwidth
[15:50] and they had an external developer resource they wanted to continue using, Vasily.
[15:55] So Igor Markin, who works at DCG, actually managed this project as the admin on it.
[16:01] So I was the strategist, then Igor was the admin, and then the developer Vasily was underneath.
[16:07] And that worked really well, actually. It was a way for DCG to leverage the incubator
[16:12] and create that wider sort of participation and keep this project building,
[16:17] 'cause it is a really valuable project. But DCG, they're very focused on platform immediately
[16:23] and the mobile sort of dash page side of things. So yeah, they brought it, they came to us.
[16:28] We said, yeah, we'd happily support that. And yeah, since then Vasily's been working on it.
[16:33] Unfortunately at the moment Vasily's time limited, but that project is largely complete
[16:39] for what we need it for in terms of a reference way to implement layer one transactions within an extension.
[16:46] Yeah, that's how that worked. - Great.
[16:49] Okay, can we have a look at the second project? - Absolutely, let's go for it, let's go for it.
[16:55] Do I need to re-share my screen? Nope, we're still here.
[17:00] Cool, excellent. So I'm gonna start by going to the GitHub repository
[17:05] for this. This is built by Alex Werner,
[17:07] so I'm just gonna start by cloning that. Actually, I may actually already have the repo.
[17:12] Let's see. - And then what's this one called?
[17:17] - So this is just called Dash Platform Extension Reference or something.
[17:22] It's a very, yeah, a very open ended name. Well, a descriptive name, not a very interesting name.
[17:29] - Okay, and then the last one, which was L1. This is a platform.
[17:33] - This is platform focused, yeah. So I'm just gonna re-clone this in here.
[17:39] - Dang, I feel like I'm watching Mr. Robot. - Hardly.
[17:46] I am so far away from AJ and stuff. Well, okay, there we go, it's sped up.
[17:50] I was wondering why it was taking so long. We're gonna be sitting here for a while whilst this works.
[17:55] Strange how slow it is. - So that previous one is called Dash Pay, but yeah.
[18:02] - It's not Dash Pay, yeah. - Yeah, we should probably rename that because--
[18:05] - We have renamed the card, but we haven't renamed the repo.
[18:08] I think we should bring that repository into one of our organizations, whichever works.
[18:13] And right now it's a case of if we wanna finish that off and take that to a production state
[18:19] of just being a pure layer one extension using the SDKs, we'd need another developer, but not for very long.
[18:25] It would be maybe a week or two's work to just polish that off into something that is ready.
[18:33] The main thing there is the secure storage of the keys. And Vasily already did the sort of discovery work on that.
[18:40] It's just implementing that and the pins. - Okay.
[18:43] - Okay, so if I go into the extension folder, you can see there's actually a dist folder,
[18:50] so I can just load that up. So the difference between this one is the last one
[18:54] I had to actually build it, whereas this one is, there's a pre sort of built.
[18:58] - They're checking in the dist into the Git repo. - Yes, so I'm gonna just go that.
[19:07] It's still obviously all open source. It's not like a compiled binary.
[19:10] It's just a folder for a repo. So I can then go back into code.
[19:16] And this one has a very unhelpful name of just extension. So the distributor is,
[19:24] so I can just load that entire folder into Chrome. And now I can open new tab,
[19:31] and let's unpin the old one and pin this one. And we're gonna open up this extension.
[19:37] This one's a little less visual. So this one's a bit more early stage.
[19:40] So the goal for this one is those layer two interactions, the dash platform interactions.
[19:46] The idea here is to create that library that dApp developers will use
[19:50] to communicate with the wallet. And we're exploring different ways to do that,
[19:54] whether we have that wider interoperability by using something like Wallet Connect,
[19:58] an existing sort of standard for these communication between different coin wallets and the extension,
[20:05] or if we have to roll our own. And to a degree,
[20:08] we probably will have to roll our own features because there's no other project
[20:13] that quite has the same data writing sort of, they don't have dash platform ultimately,
[20:18] and they're not designed so much for that data storage. So yeah, I'll just get started by creating a wallet.
[20:26] And as you can see, it's a usual typical wallet. And now I'm gonna go to the boilerplate
[20:32] for an example, decentralized application. So this page has that,
[20:37] this is a very much a basic page for having that sort of decentralized application boilerplate.
[20:42] It has the library that communicates with the wallet itself.
[20:46] So I can just click connect wallet, and you can see it's connected to the wallet
[20:50] and it's brought in the same address that's on the wallet itself.
[20:54] And what happens here is there's like a layer of communication
[20:58] between the webpage or the decentralized application and the extension.
[21:02] And in fact, it's somewhat more like a triangle where the extension and the DAP can communicate,
[21:10] the webpage, the DAP can communicate to each other, but also the DAP can communicate request to the extension,
[21:17] which the user then approves. And the extension is then writing that to layer one
[21:21] or to platform. And then the DAP itself is reading that from platform.
[21:24] So there's almost like this flow. There will be the two way communication
[21:28] between the extension and the page, but there's also more data sources there.
[21:33] And the key important part to this is just that communication layer.
[21:36] So if I have a governance website and I wanna create a G object
[21:42] that's now on platform in the future, I can do that.
[21:45] I can prompt the user to write that governance object and create it.
[21:49] Or I can say, hey, do you wanna, I would like a key that gives this page permission,
[21:56] the DAP permission, all on the front end, never going off to any servers,
[22:01] to write to a dash platform data contract. And then the user will get that approval pop-up
[22:06] within the wallet. They'll get in a pop-up, they'll say,
[22:10] yes, I approve sharing this data, this key. And they'll be able to revoke that within the extension,
[22:16] however that looks like. And the goal is that there's this passport
[22:21] between all these decentralized applications that you're bringing around with you,
[22:24] your user, multiple users that you can use for different verticals.
[22:29] You might have an incognito user you wanna be really private with,
[22:32] or a user that's your public facing professional profile, whatever it is.
[22:36] Yeah, and you can bring these all around. Any DAP can just integrate a very basic library
[22:43] and have the ability to create those actions on dash platform without any sort of real complexity.
[22:49] And the goal is also this would be mobile too, that you would have a QR code.
[22:53] I'll show more on the slides that I'm about to show you, that you'd have a QR code you'd scan
[22:58] that will create this communication layer between a DAP and a mobile wallet and platform.
[23:02] And there's just, the goal is just to make everything very free flowing, very easy for developers,
[23:07] very easy for dash users to onboard and to just get access to this whole ecosystem.
[23:12] Yeah, question time. - So does, do any of these buttons down at the bottom,
[23:18] are they wired up yet? - They're semi-wired up, they're semi-wired up.
[23:22] I think they're broken as of the latest test net 0.25 platform, but they did work for it briefly.
[23:30] There was a way to sort of write contracts. It's similar to a dash chump in that respect.
[23:34] It had those sort of like a more dash mate side of things. They had, yeah, had a little bit of extension data.
[23:40] It has layer one transactions in there already as well, even though it doesn't really, you know,
[23:44] that's not necessarily the point of this project, but having a different approach to that is good.
[23:48] And it has all the kind of like service worker and communication layers updated for the latest
[23:54] sort of Google Chrome rules and manifest. So yeah, this is again, early stage.
[24:01] A key thing I would say, so the last one's kind of semi-complete.
[24:04] This one is, I would say early stage. And the next one is TBC.
[24:08] I would say that the, you know, the key thing with this is like looking into that option
[24:15] of interoperability. So I think ICJR has said he's, you know,
[24:18] very interested in doing that, but he's quite busy at the moment.
[24:21] I really want to see if there is a way that we can, you know, be part of that greater ecosystem.
[24:26] If people can log on to, you know, whatever other dapit is using their Dash wallet
[24:32] and use their Dash identity in some fashion, you know, any way where we can,
[24:35] 'cause it's not just about making it easy for us and our developers by using Wallet Connect.
[24:39] It's just access for everyone using our systems to that whole ecosystem and just the wider back and forth
[24:46] between everything. You know, if you can sign onto a decentralized exchange
[24:49] using Dash because they've already got Wallet Connect on that decentralized exchange,
[24:54] and you can just use your Dash Pay wallet, that's ideal. And as that expands in the future,
[24:59] as we get Dash onto other wallets, more other sort of web three sort of native wallets,
[25:06] if we can, you know, have them support Dash usernames built in.
[25:10] You know, it may require a lot of work just improving Wallet Connect and other standards
[25:14] to include those sort of data structures and support for Dash usernames 'cause, you know,
[25:19] unstoppable domains and whatever, usernames and things, they're a different beast
[25:23] than our approach. Like ours is significantly more complex
[25:27] and significantly better in my opinion. So yeah, there's a lot of work there.
[25:32] - So how would you see this interacting with something like Wallet Connect?
[25:37] We are in talks with them, by the way. I'm not sure if that will be successful or not,
[25:46] but the Maya guys, they spearheaded that discussion. And so we are trying to get connected
[25:56] through Wallet Connect. So would this be something that would work in tandem
[26:01] with that or be replaced by that? - Yeah, no, a hundred percent.
[26:05] So Wallet Connect would act as the effective library for the dApp developers to use.
[26:11] And they would, you know, use the Wallet Connect SDK and libraries
[26:15] to create that sort of communication layer. But at that point, you know,
[26:19] anyone can then connect any wallet or, you know, to that site.
[26:23] But, you know, how many wallets are actually gonna support that sort of platform feature set?
[26:28] Even if, you know, Wallet Connect add and extend their standard to include
[26:33] Dash Pay username features and platform features and whatever else, you know, instance,
[26:37] any of these sort of things, how many, you know, how many wallets
[26:42] will be able to do that? So there's both sides of this.
[26:44] It's the, you know, the Wallet Connect would be the library used by the dApp developers
[26:49] if we can get it to, you know, do everything we need it to do.
[26:52] Whereas the actual extension has to do a lot more than that in terms of where it's signing,
[26:58] what it's creating, what it's writing to platform, how it's sharing keys to write to data contracts.
[27:03] Like all these features are very novel and they're not something that Wallet Connect
[27:07] or Ethereum wallets, MetaMask, anything like that has quite even touched upon yet really.
[27:13] You know, there are features not too dissimilar in terms of, you know, authorizing,
[27:18] writing smart contracts and things like that. But it's, you know, it's very different.
[27:23] And I think that we'd have to do a lot of work with Wallet Connect to get that feature sort of equivalency.
[27:29] But yeah, I'm excited on that challenge really. And I think it's really important that we are
[27:34] participant in that wider ecosystem. - Okay.
[27:38] So I saw a question for a minute there. It looked like from Halaway, let's.
[27:43] - I think it's more of a comment, but yeah, I guess. - Yeah.
[27:48] - Had a less than ideal experience with MetaMask. - Yeah, I mean, that is a demonstrable sort of like,
[27:54] yeah, that's how sort of we build the dApps at the moment. And it's a good way to do it.
[27:59] It's allows you to basically quickly insert a wallet or create a seed.
[28:04] But the goal is that you won't have to do that. You're not gonna have to write your mnemonic
[28:08] into every website everywhere and trust it. You'll be able to just create that sort of barrier
[28:13] of permission to this extension and everything will be revocable or approvable.
[28:18] Yeah, there's definitely a massive user experience factor here and you'll be able to switch accounts
[28:26] and approve with different accounts and just use this as your passport around the dApp ecosystem.
[28:33] That's the goal anyway. - Nice.
[28:36] Is there any more for us to see on this one? - Yeah, not on this one, not on this one.
[28:40] Yeah, this is like early stage. It's more just about creating those sort of early boilerplate
[28:45] for the dApps and creating those flows and then expanding upon them, iterating upon them.
[28:49] Especially now that, so the reason this was kind of like stopped four months ago was just that lack of consistency
[28:56] with test net platform, but now it's more reliable. The actual ability to build your own sort of platform
[29:04] network is a lot better. So building your own developer network to work against
[29:08] is a lot better and there's just been a lot of improvements. So I'd say, you know, DCG have really focused on getting
[29:13] that whole sort of process a lot better. So yeah, the development will be resuming
[29:20] quite heavily on this. - I think you mentioned that you were connecting
[29:24] to version 0.25 on this one. - Yeah.
[29:31] - Have you tried 0.24? 'Cause my understanding was 0.24, while maybe not,
[29:38] it's maybe not going to be the one that's going forward, it is working right now.
[29:46] - Yeah, well, the issue with that first extension was there was a branch that was necessary
[29:52] for it to function, but that branch has been deleted off DCG's repos for whatever reason.
[29:59] And that included fixes for the extension to work. But I think those fixes may have been merged into 0.25.
[30:07] As you can see, it is working to a degree. It's just a question of whether, you know,
[30:12] I could get these running. I was up very late, early this morning,
[30:16] trying to get this, you know, some of these things running because this was developed, you know,
[30:21] against a much earlier version of platform really. - Cool.
[30:27] Well, then let's check out the third demo and- - Not a demo for this one, unfortunately.
[30:32] This one is more of a presentation. Yeah, yeah, unfortunately, yeah.
[30:36] - Let's do it. - Let's go for it.
[30:39] - Okay. - Okay, can you, is it sharing my screen anymore?
[30:48] - No, I don't see that one just yet. - Let's get it up again, share screen.
[30:55] (indistinct) Okay, so the sort of dashboard side of things,
[31:07] it's a, you know, a wallet that just allows you to, you know, have that actual, all those social features,
[31:14] all those designs. This is taking those two other projects
[31:17] that are more reference projects and develop a sort of implementation
[31:20] into something that is visual and production, user-friendly, has all the extended features
[31:25] that you could hope, including, you know, chat, which is the major sort of the killer part
[31:30] of this application, end-to-end encrypted chat. Well, not end-to-end because it's, you know,
[31:35] it's user to platform encrypted, platform to user encrypted.
[31:40] Like it is a fully encrypted chat wallet paid by a social wallet powered by Dash platform.
[31:48] So users will be able to just completely sort of communicate with each other, request payments, send payments,
[31:55] attach memos. There'll be this whole flow of communication
[31:59] where, you know, you can actually add your friends, you can explore your social graph.
[32:04] So rather than being, you know, here's an address or here's a username and you're just sending money
[32:08] and you're communicating on whatever else in person or WhatsApp or Facebook or Discord,
[32:14] whatever it is about that transaction. In this, it will be stored within the flow
[32:19] of the sort of wallet itself. So this will be produced.
[32:23] Yeah, go ahead, sorry. - Are these payments, layer one payments?
[32:27] - So these are all player one payments, but they'll have information attached to them
[32:30] powered by layer two. So the communication is all layer two
[32:34] or the payments are layer one. At some point in the future, obviously,
[32:37] as more payment features are unlocked on a platform and it becomes more part of that system,
[32:42] this would obviously expand to cover that side of things. So yeah, the goal for this is that it's gonna be
[32:48] full sort of extension, as well as a desktop wallet, as well as a mobile wallet,
[32:54] all produced from a very similar code base and just allowing everyone to sort of,
[32:59] anyone that wants to, to use very simple apps. Obviously, there will be the power users
[33:03] that still wanna run their own full sort of blockchain, index blockchain.
[33:07] Whereas this is more for that sort of retail user, I guess, more casual user.
[33:13] It'll still be full, you know, it's full, you know, self-custody at the moment.
[33:17] It will still be seed words, but this project could easily be expanded
[33:21] because of the social features to have guardians and private key sharding,
[33:26] where you have recovery systems, whether you can use, you know, your social,
[33:31] your OAuth logins, like your Google login as one part of that recovery.
[33:36] You could use a two-factor authentication because of how, you know, you could store the, you know,
[33:41] but it wouldn't be Google's two-factor authentication. It would be like a platform two-factor authentication.
[33:46] But there's so much you can do with this and expand it to cover.
[33:49] And the idea is just, it's a different wallet experience, you know, where you're communicating and chatting
[33:55] and requesting money and talking to each other and sending payments.
[33:59] Yes, that's a great question, PME. Great question.
[34:02] I'm a big fan of private send. My goal for this is to take a slightly different approach
[34:06] and test how that works and validate that idea. And the goal for this is that you'll have an incognito user
[34:10] or multiple incognito users whose funds are always private. The funds that go into them that are mixed,
[34:16] the funds that go out of them are entirely mixed. They will be, obviously, the funds that go into them
[34:21] that are mixed, it's complex, but as soon as funds come in, they would be mixed and reset.
[34:25] The goal is that you will have a way that's more user-friendly.
[34:29] We're familiar with incognito and private modes and things where the, and it'll be less sort of like,
[34:35] choose your coin control, choose your coins and things. It'll be more, that complexity will be extrapolated
[34:40] from the user. And in the future, as there's like more, you know,
[34:45] tornado cash or whatever it is built against platform as like the matchmaking service,
[34:50] we'd implement all of that, definitely. - So I'm looking at what looks to be a web app.
[34:57] Is that? - No, that's the desktop.
[35:00] That's the example of the desktop. The mobile layout is the sort of example of the extension,
[35:05] but there's more slides. I will get moving on the slides so you can follow on there.
[35:10] So here's an example of how this would work in a real sort of situation.
[35:15] So Sodality is a dash platform patron alternative. So it's a way to sort of support creators,
[35:22] create a reoccurring revenue for creators that can't be canceled, can't be stopped,
[35:27] isn't controlled by platforms that can, you know, just de-platform you at any point.
[35:32] You're not building up value into something that, you know, isn't.
[35:36] - We covered this last week. - Exactly, perfect, yes.
[35:38] - I was just wondering. - Yeah, and, you know, it's important
[35:43] this kind of thing is, you know, accessible for users and that they can log in very easy
[35:48] and it's part of that ecosystem. It needs to have that symbiotic sort of seamless relationship
[35:52] with their wallet because of those regular payments. Even if you can have creation of smart contracts,
[35:58] the goal is that it's super user-friendly. If a creator is referring people to it,
[36:02] they don't want them to have to, you know, import loads of sea birds
[36:04] or manually set loads of things up. They want it easy.
[36:07] So the flow would look a little like this. You would begin by clicking the sign in
[36:11] and you've got two options there. You can either scan a QR code using your mobile wallet,
[36:16] which will probably-- - The DashPay wallet?
[36:18] - Yeah, the mobile version of this, not the current DashPay wallet.
[36:22] So DCG's DashPay wallet doesn't have much in the way of DApp onboarding.
[36:27] They only, they're focused on DashPay as in the username based system right now.
[36:31] I'd like to think that in the future, this kind of, whether we lead that or they,
[36:36] they will implement features like this. But it's logical that they leverage the incubator
[36:41] and the work that we'll do in discovery and exploring and, you know, developing a standard
[36:45] for how that might look. So the goal, and also because the wallet,
[36:50] an extension wallet and a pure JS wallet is a lot more simple to iterate and build upon
[36:54] than a, you know, in-bus and iOS and the questions of when's this coming to my iPhone?
[36:59] When's this coming from Android? So yeah, you could scan this with your mobile phone
[37:04] and it will create a communication layer. I'm still not quite sure how that works.
[37:07] I'm still exploring how you would have that sort of communication between a DApp
[37:11] and a mobile wallet in terms of web workers and things. I'm pretty sure it's possible,
[37:16] but it may limit some of the feature set. It might be something where, yeah,
[37:22] it's another day, a chat for another day. But the other option here is that
[37:28] if you have that extension, you could just click to your connect wallet.
[37:33] And once you click to your connect wallet, it's gonna prompt you in,
[37:35] it's gonna ask you what account you wanna use. So you have multiple accounts you can choose.
[37:40] If you're gonna use your public facing or your private account,
[37:44] you can always sort of revoke that access. You could have multiple accounts.
[37:48] They don't wanna know necessarily who you are. It's not a, there's no like a proof of individuality
[37:54] in this, it's just whatever account you want. And you'll approve that connection
[37:58] and then you'll be logged in. So Grogu here is nicely logged in,
[38:01] he can do all his actions. And further actions like creating a payment
[38:05] will always prompt that authorization. But in the future,
[38:08] I imagine you could set some threshold for that as well. And writing to sort of the network,
[38:16] writing to the platform, whether you're creating a comment that's stored on platform,
[38:21] that will also be approved by the extension. And they'll just trigger that pop-up,
[38:24] it'll be really seamless. They have limited some of what extensions can do
[38:28] specifically on Chrome, but that those limitations won't really hurt us in any way.
[38:34] They're actually healthy limitations for security. So yeah, the wallet, like I said,
[38:40] full chat wallet fully focused on being on mobile, on desktop and extension.
[38:45] We're gonna start with the extension. So don't expect everything to all come at once.
[38:48] The extension is the simplest and the most accessible really to do.
[38:54] And it creates, it's easy to do that layer of communication between the decentralized application and the extension.
[39:00] The extension will probably have a full screen view pretty soon after that looks like this.
[39:03] So you'll be able to still use the extension as a full wallet.
[39:07] You'll be able to pop it out and it will just be in the sort of web browser view.
[39:11] And you'll be able to use it for that, but it will also be seamlessly integrated
[39:15] with your browser in terms of interacting with decentralized applications.
[39:20] So that covers that side of things. And let's talk about the future briefly as well.
[39:23] And then I'll answer all the questions. I wanna just expand this.
[39:27] I wanna turn this into something that's really production ready, accessible to anyone to use,
[39:32] empowering like the users. I want them to use this
[39:36] and I want them to have that Eureka moment. I want them to see all the dApps they can use,
[39:40] the accessibility. I want them to be able to move in and out.
[39:42] I want them to have incognito and be private. That's their purpose.
[39:46] I want them to be able to stake and earn money, whether that's adding liquidity to decentralized exchanges
[39:51] or any money through a trustless mass node or shared mass node shares, whatever it is.
[39:56] I wanna implement all these things. And these services are not that complex.
[40:01] I've already, obviously you guys know, I put a lot of time into on and off ramps
[40:04] and decentralized exchange and dash direct. So all of these things I know are reasonably possible
[40:11] and DCG are working on this. This isn't, none of this is a,
[40:14] to supposed to completely like supersede DCG, but these things are more accessible
[40:21] within a web-based framework because they're kind of designed for that.
[40:25] And we can iterate quickly. We can test and validate ideas
[40:28] and that kind of thing will come quickly to DCG too. So yeah, now I'll open the floor.
[40:34] - When you say DCG is working on this, I think that you mean that they're working on
[40:40] integrating some of those things into mobile wallet. - Yeah. - Specifically.
[40:45] - Yeah, exactly. They're focused, they're very heavily focused
[40:48] on the mobile wallet sort of user experience. My concern right now with that,
[40:54] and it's not a criticism of DCG 'cause we all understand the bandwidth constraints.
[40:59] My, I wouldn't say my concern, but my focus is ensuring
[41:02] we have a really healthy platform launch. I'm worried about, you know, launching something
[41:08] and expecting the expectations there not being managed without having a actual ecosystem to back it up.
[41:15] And it's probably true that the, you know, the launched app will be Dash Pay
[41:20] and Dash Pay, the username system is a decentralized application.
[41:24] But having an actual, you know, wider ecosystem and not just for us,
[41:29] but for developers coming into this space. So they see reference projects and they see, you know,
[41:34] that this is a supportive ecosystem, supporting third parties building against this
[41:38] is really important. And that's, you know, what I'm keen to keep working towards.
[41:44] - Nice. - Yeah.
[41:48] Well, I don't have any additional questions. Those were all really pretty.
[41:52] It was nice to see. And, well, no, I guess one question I might have is
[41:57] the need for all three. You said that the first two anyway,
[42:05] were more like reference. So that somebody becomes like, oh, how can I?
[42:10] 'Cause I guess- - This is being used.
[42:12] Those projects are being used to build this project. So this project isn't gonna be solving
[42:17] the layer one transaction problem or the Dash BAP communication problem.
[42:21] This is actually a simpler project because this is integrating those
[42:26] and then wrapping them in a more user-friendly like UI. And then also those extended services,
[42:34] which are also more simple in ways. So those projects will act as the upstream source of truth
[42:40] or how layer one transactions and DAP communication is done.
[42:44] And this project is actually taking those parts and then building it out.
[42:48] Yeah, exactly. Into something that's sort of user-focused and friendly.
[42:53] Yeah. - Great.
[42:55] Okay. - The only other question that people
[42:59] are gonna be wondering is when. - When?
[43:02] Yeah, that's a great question. That's a great question.
[43:03] So that first extension, obviously largely complete. We could get that production
[43:07] in probably two weeks of their time, I would say. Probably a security audit would be healthy
[43:11] for something like that. So that would take a longer period.
[43:15] For the other one, that is an open-ended question. Ultimately, whether we go for the wallet connect approach
[43:20] or whether we roll our own is very important. If we roll our own, I'd like to start just quickly
[43:25] with a sort of more minimal approach in terms of proving data contracts,
[43:29] like message signing and creation of transactions. It will be something that will be very quickly
[43:34] iterated upon and expanded. And it's something that's very important we do right.
[43:37] There would have to be dips associated with that. There would have to be a process of creating a standard
[43:42] that's very sort of open and libraries for that. So that would be very important because that once you,
[43:49] once there is sort of that library that's getting wider use, it's really important that,
[43:54] you know, most people, most developers will be implementing that library
[43:57] and that needs to, you know, work for all those developers and be very secure obviously as well.
[44:03] And for the extension, so the production extension, so that is being worked on now.
[44:10] I imagine I will have more to show in two months or so, which I'll come on a show with you,
[44:15] Amanda and Rion, hopefully, with actual real demos of that project as it progresses.
[44:21] Right now, there are features, but those features were built, you know,
[44:26] a year and a half ago, two years ago. And those features like the chat, the chat does work.
[44:30] There is a decentralized sort of chat end-to-end encrypted sort of chat in there.
[44:35] But this was built against a much earlier version of platform.
[44:39] Now that platform's stable again, we're kind of rebuilding a lot of it.
[44:43] Another thing, it was built against Ionic 4 using Vue. Now we're on Ionic 5.
[44:48] A lot of the stuff has been deprecated that it uses. It's a case of, we kind of got this large sort of workload
[44:55] ahead of us to basically refactor the entire code base and build some of these new features.
[45:00] So I imagine two months to a demo, sort of a testnet-based demo project
[45:05] that people will also be able to install. This isn't a, you know, I have to build it on my machine.
[45:09] In fact, none of these are. You could build any of these yourself.
[45:12] All of this is all open source and relatively easy, I guess. But in terms of actually taking that to production,
[45:18] I would say four to six months. Again, for the extension
[45:23] with some of the additional features. For chat and payments, definitely, obviously,
[45:28] and user account switching. All of that will be in, you know,
[45:31] four months, I imagine, ready to go. Obviously, security audits are a complex sort of thing,
[45:37] budgeting those and, you know, the timeframe to that kind of thing.
[45:42] And then after the facts, it will be a case of those extended features.
[45:46] So having decentralized exchange, we're already looking into how we can do that
[45:49] with Maya and 4Chain in a sort of more user-friendly sort of clean way.
[45:54] Because, you know, the issue with that is to create a decentralized exchange transaction,
[45:59] you need to be able to create like Bitcoin transactions and Ethereum transactions.
[46:02] And how do you do that in a wallet that's a light wallet without, you know,
[46:06] having all this, you know, huge amount of, what's the word for it?
[46:11] But just running so many more services, it's just exponentially more complex,
[46:15] more cryptos you add to it. So yeah, I would say, yeah, six months to a good,
[46:21] you know, feature, largely feature complete, not all those extended features.
[46:26] Those are, you know, the crowd though, the Dash Direct stuff,
[46:29] that's maybe production ready project, I would say. But in two months, I'll have a lot more to show
[46:35] on that front. - Okay.
[46:37] - Great. All right, well, thanks for joining us today, Ash.
[46:41] We definitely look forward to seeing that. And of course, we look forward the most of all
[46:46] to seeing that on Mainnet platform. - Oh, yes.
[46:49] - Yes? - Yes, indeed, of course.
[46:52] - Yes, good. Okay, well, that is everything for us this week.
[46:55] And we'll be back same time, same place next week. So we look forward to seeing you then.
[47:01] Bye. - Bye, guys.
[47:05] - Bye, thank you, everyone.