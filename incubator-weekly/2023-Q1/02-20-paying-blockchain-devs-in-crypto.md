---
showLink: "https://www.youtube.com/watch?v=JqMnrqeKMUc"
slug: "paying-blockchain-devs-in-crypto"
title: "Is It Important for Blockchain Devs to be Paid in the Crypto They Work On?"
publishDate: "2023-02-20"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/JqMnrqeKMUc/maxresdefault.webp"
---

AJ O'Neill of Dash Incubator discusses building modular, well-documented Dash libraries for developers.

## Episode Summary

tl;dr: AJ O'Neill, a developer at Dash Incubator, is working on creating modular, well-documented libraries to make Dash development easier and more accessible. The libraries break down complex functionality into small, reusable components with clear documentation and examples. Rion, Dash Incubator's strategist, and Joel discuss the importance of blockchain developers being paid in the cryptocurrency they work on to expand the Dash economy, improve their work through real-world usage, and align incentives.

## Chapters

00:00 - Introduction and Beginning of Episode
The episode starts with a discussion of central bank digital currencies and their implications.

02:39 - Overview of Cloud Storage and Privacy Concerns 
A segment on how cloud storage has become crucial but raises privacy concerns when using popular providers.

04:25 - Dash Incubator Introduction
Rion and AJ introduce themselves and their roles at Dash Incubator.

05:40 - AJ's Payment Tools Project Overview
AJ explains his work on creating modular, well-documented Dash libraries to simplify development.

23:46 - Importance of Developers Being Paid in Crypto They Work On
A discussion on how being paid in Dash expands the Dash economy, improves developers' work, and aligns incentives.

33:13 - Dash Incubator's Accounting and Payment Processes
Rion walks through the Incubator's transparent accounting and payment processes using Trello and public spreadsheets.

40:44 - Future Plans for Incubator Workflow and Hiring
Rion and AJ discuss potential workflow improvements and the Incubator's approach to onboarding new developers.

## Transcript

[00:00] (upbeat music) - Central bank digital currencies,
[00:11] this isn't just the Bank of England considering this, is it?
[00:14] - Exactly, currently more than 90% of central banks globally are all working on bringing out
[00:20] a central bank digital currency. And I think it's really important to elaborate
[00:24] on what exactly that is. A central bank digital currency
[00:27] is basically what we have now. So it's fiat currency,
[00:30] but it's gonna be entirely digital, which means absolutely in the control of the government
[00:35] and the central bank. So as you mentioned, government, since they own it,
[00:38] they're able to program it in a way that we've never seen before.
[00:42] So as you said, if for whatever reason you don't do as you're told
[00:44] and you don't take three vaccines, four vaccines or whatever it is,
[00:48] the money can just be programmed to be used against you. The perfect example is right now
[00:53] during this supposed climate crisis where they want to implement a carbon allowance.
[00:58] So how do you do that? Well, it's very simple.
[01:00] You just program the money in a way that you cannot do with the current cash that we have.
[01:05] - There it is, pumping 10.8 trillion yuan into the banking system.
[01:15] For all that pumping that's been going on, it doesn't seem to have produced much
[01:19] by the way of economic results. We're led to believe that that 10.8 trillion,
[01:22] that flood of credit into the economy engineered some massive robust recovery and economic boom.
[01:28] Reality could not have been farther from the case. Now China's economy didn't crash,
[01:32] but ever since then, it has been slowing and slowing and slowing
[01:36] and then slowing some more, which has led to these RRR cuts
[01:40] and other measures by central banks around the world, not the other way around.
[01:43] Central bank policies are a response to issues in the real economy,
[01:48] not a solution for those problems. (upbeat music)
[01:55] - Cloud storage. It allows us to access our files conveniently
[01:59] via the internet across multiple devices wherever we are. The cloud storage industry has boomed in recent years.
[02:06] Some of the most common consumer grade services include Google Drive, iCloud and Dropbox.
[02:12] People use these for their photos, videos, documents and all kinds of other files
[02:17] because it's a cost-effective way to make data accessible and also share it.
[02:22] Cloud storage has become a crucial part of our lives, but when you use the most popular cloud storage providers,
[02:28] you're handing your data off to someone else so that they can look after it for you.
[02:34] What are the privacy implications of this? (upbeat music)
[02:39] - Well, this takes us right back to basically where we were at the beginning
[02:45] where your drunk, insolvent Uncle Sam has to issue more and more and more of these treasuries
[02:52] into a market where there might not be a buyer. Interest rates go up even higher,
[02:58] asset prices go down even further, tax receipts go down. Janet Yellen's deficit problem becomes even more extreme
[03:07] and the cycle just continues to repeat itself over and over again,
[03:12] taking us right into the fiscal and economic abyss. This is the QT doom loop.
[03:20] So the main takeaway is the government is now admitting that they might be completely broke by July of this year.
[03:28] And the debt ceiling or increasing that debt ceiling by no means fixes the problem
[03:37] because this is what we really should be worried about. (upbeat music)
[03:46] - If we move towards full central bank digital currencies, but I don't want government to control
[03:52] potentially every aspect of my life. Presumably, this could be the biggest thing
[03:57] that's ever happened to Bitcoin and other crypto coins. - It's about being a sovereign individual
[04:03] because money is the energy which fuels your life. So if you don't have control of your money,
[04:08] you don't have control over anything and you, in my opinion, really just become a slave
[04:12] because if the government can make your money expire, if the government can freeze it
[04:17] in the name of terrorism or national security, then what freedom do you have in society as an individual?
[04:22] You have none. (upbeat music)
[04:25] - Hello, and welcome to Incubator Weekly. Great to see everybody.
[04:39] How are you today, Rion? How are you today, AJ?
[04:41] - I'm good. I hope I am coming through okay.
[04:45] I'm having a little bit of a connection issue, but hopefully you can hear me.
[04:49] - We can hear you at least. And you, AJ, how is your connection?
[04:54] - It should be perfect. - Well, okay.
[04:58] No two ways about that. So Rion and I introduced ourselves last week,
[05:04] but hey, this new character, AJ, is a new face. AJ O'Neill, will you tell us
[05:11] just a little bit about yourself? - Sure.
[05:14] I'm AJ, I'm a technophobic technologist, equal opportunity offender, chief offending officer,
[05:19] dangerous wrong thinker, father of two. - Wow, great.
[05:24] And you are a developer within the Dash Incubator also, yes? - Yes, and I happen to be a software engineer.
[05:32] - Right on, right on. Okay, so today's show is going to consist of three segments.
[05:40] The first segment is going to be an overview of a bounty within the incubator at this time
[05:48] called Payment Tools Project. And Rion is going to go through a Q&A with AJ,
[05:54] who is the lead developer on that. Next, we'll move into a discussion
[05:59] of whether it is important for blockchain developers to be paid in the crypto that they work on.
[06:07] And then finally, we're going to wrap up with Rion giving us a overview of incubators finances.
[06:16] Yeah, good. So Rion, let's kick it over to you
[06:20] to start the overview of AJ's project. - Well, I'll kick it right back over to AJ
[06:27] because I think that we'll have plenty to talk about today. So AJ, let me just ask you like the most obvious question.
[06:36] What are you doing and why are you doing it on this project? - Well, let me tell you, bring up my screen here.
[06:44] So I'm working on the Payment Tool Project has kind of evolved.
[06:48] Basically what happened is as I've come into the ecosystem, what I've discovered is that everything is very large
[06:56] and bulky and old and crufty. So on the Dash Core desktop side and server side,
[07:04] you've got all this C++ code that's all packed tight together.
[07:07] Everything is just one giant blob. And the Dash Core JS replicates that.
[07:14] So everything there is just one big giant blob. And the documentation is scattered all over the place.
[07:21] So if you want to find out about something and you're not a cryptocurrency native,
[07:26] then you've got to go over and look at BIP32 and BIP39 and BIP44 and BIP43.
[07:31] And you got to look at some Dash documentation, but it's not all updated.
[07:34] And a lot of it still says Bitcoin and BitCore and BitThis and BitThat.
[07:38] And so what this became was, okay, let's break these things down into Lego bytes
[07:45] or byte size, make them building block Legos that I can understand a component
[07:51] and I can understand another component and I can understand another component.
[07:54] And then I can put them together to build a thing rather than here's this whole huge thing
[08:01] and I can't even tell which piece does what. And that's resulted in either,
[08:09] oh, and then also there's the issue of, especially in the web world,
[08:14] is that these things are very, very large. So Jojobite said that it's a million lines of code
[08:19] for Dash Core. And a lot of that is because it was built a decade ago
[08:25] and has never really been updated 'cause it comes off of BitCore, BitCore JS.
[08:29] - Dash Core Lib, I think you mean, right? - Not Dash Core, the C++,
[08:33] but Dash Core Lib, the JavaScript library that was built from Core.
[08:36] - Yeah, Dash Core JS or, yeah, yeah. - Oh, you're talking about Dash, Dash SDK.
[08:42] Either one of those, they're both very big. - Okay, well--
[08:47] - One of them is 1.6 megabytes and one of them is 0.8 megabytes.
[08:50] - And that's minified. - Minified, yes.
[08:53] - That's what it's already been processed. - Minified and gzipped.
[08:57] So that's the smallest it's possibly going to get in a web application.
[09:01] If you want to make a web application, you want to include Dash functionality,
[09:07] you're going to be, you're asking all of your users to download 1.6 megabytes.
[09:11] I talked a little bit about this in the proposal text from the last quarter's proposal,
[09:16] but this is one of my main concerns. So we do want to have to,
[09:20] we want to trim that down as much as we can. So that's part of the motivation here.
[09:27] - Yeah, yeah, and that's big. And there's a lot of problems that,
[09:31] one, you've got dependency hell, which is there's hundreds of things
[09:35] that you don't know or understand that are being brought into that,
[09:38] that it makes it very difficult to audit, makes it very difficult to get the whole picture.
[09:43] And then you also have that no reasonable person is going to include that on their page
[09:48] for a payment that people just aren't using yet. Here, try this out.
[09:52] It's only a 1.6 megabyte load time. It's only going to add 10 seconds
[09:57] to your mobile user's experience. It's not, it's not a viable solution.
[10:02] But a lot of that is because this was built as a port of the C++ code and built for the server.
[10:08] And so all of the bundling that happens on the browser, most of it is including things
[10:12] that are either frizzle-less, excessive, or no longer necessary.
[10:15] So with this, I've either hand-selected other forks or other libraries that people have built independently
[10:24] or rewritten from scratch the most basic atomic particles of the, of what's necessary to do
[10:32] all of the offline action. So this, this, which may be dash SDK core
[10:38] is not the right name for it. So we'll figure that out.
[10:40] But this collection of tools, dash tools, is the atomic building blocks.
[10:46] And the first one is secp256k1. Now I brought this in from Noble Crypto,
[10:52] which is a fresh, modern, browser-first library for all of the math stuff that happens.
[10:59] The elliptic curve, all of the real nitty gritty that deals with the bits and the bytes
[11:04] for the signing, the public keys, all that stuff. And so this one, I didn't really do much to
[11:10] other than give it a light wrapping layer to make it a little bit easier to export in more ways.
[11:16] Because most developers are not cryptocurrency developers and most developers aren't even working on apps
[11:23] in the way that startup people think of them. Most of them are working on things like WordPress.
[11:27] And that's where we're, I believe, we're going to get people is the people that are hosting
[11:33] their, their, you know, Shopify, WordPress. They're not actually software developers.
[11:39] They're just people that are taking tools and bringing things together.
[11:42] And they want just a script tag or two that they can include to have something work.
[11:47] And so I went with that mindset. And so I took this library and I just massaged it
[11:51] a little bit so that it, it works better. And it works in node and in browser.
[11:56] So it'll work in the server environment and it'll work in the client environment.
[11:58] But there's not, not too much extra that I did there. Dash keys is all of the encoding
[12:05] and the hash primitives, but all together in one. So rather than have it across several dependencies,
[12:11] the truth of the matter is there is no one else that I've ever heard of in any of all of software
[12:17] engineering that is using base X, which is one of the encoding primitives.
[12:21] And likewise for the, the primitive that's built on top of that base 58.
[12:25] And then likewise for the primitive that's built on top of that base 58 check.
[12:29] And then likewise for a little bit aside, but the hashing function that's used ripe MD one 60.
[12:36] These are things that are exclusively used in cryptocurrency.
[12:40] They have never been adopted anywhere else. And so it makes sense to just bring those together
[12:45] into one package and have them documented together and have them delivered together
[12:51] because there's no other use case for them. It's not like, oh, well, I'm going to build this other app.
[12:58] And then I'm also going to need any of these tools. If you're doing cryptocurrencies,
[13:01] you're going to need all those tools. If you're not doing cryptocurrencies,
[13:03] you're never going to need them. So dash keys brings all that together
[13:06] so that the encoding of private keys into wallet import format with can happen in there,
[13:12] as well as the encoding of the address format from the hash of the public key, the pub key hash,
[13:18] as well as the encoding for the experts and the X pub. So all of the encoding stuff that we think of
[13:24] as our private key and our payment address and related byte formats,
[13:30] all of the encoding for that to make it human readable, other than the QR code, which is a layer on top of this,
[13:35] all of that's in dash keys. Then dash phrase is your recovery phrase generator.
[13:41] So it'll generate the recovery phrase from the list of words,
[13:44] and then it will convert that into a seed. It will encode that as a seed.
[13:50] And again, these, there's some primitives here that before they were split out into different packages
[13:56] and different classes. And I just, I brought this together.
[13:59] I rewrote it. It works in the browser and it works in node.
[14:03] And all of this is in one because you're not going to need these things
[14:07] outside of a recovery phrase. They're not used for anything else
[14:11] in the cryptocurrency space. And this is actually useful just generally.
[14:15] This is something that I had started working on before I was heavily involved in Dash Incubator.
[14:21] And so I actually took my previous version of this and then brought that into Dash Incubator
[14:25] and completed it specifically for Dash. So that's another thing, all of these,
[14:29] the options are all set for Dash by default, but you could use these with other cryptocurrencies
[14:34] to test them out. And then Dash HD is the creme de la creme.
[14:39] This is where everything comes together. This has the various types of hashing functions
[14:46] for hierarchical derivation so that you can take your recovery phrase,
[14:51] you can turn that into a wallet account. This is also what would be used, for example,
[14:55] in Dash Pay where you want to have a contact either via QR code or sending it over the network.
[15:00] You need to get somebody what's known as the XPub. This is the key structure, the hash structure
[15:07] from which you can generate millions and millions of addresses.
[15:09] So you give somebody one XPub, one QR code, one network request to a contact,
[15:15] and then they can send money to you for the rest of their life
[15:18] without ever needing to contact you directly again. So that's kind of the key feature of Dash HD
[15:25] other than that you're getting recoverable keys, which is what we want.
[15:29] And it's really important. I mean, Dash Core Desktop does not turn on
[15:35] recovery by default. If something gets corrupt in that directory,
[15:39] it's kaput. So this is something that's really, really important.
[15:42] It's turned on by default in the mobile wallet and some of the other software,
[15:45] but the hierarchical wallets are what make it possible to feel safe that you've got those 12 words
[15:52] locked in your safe box, it's recoverable. And then here, the last thing that I think
[15:59] that I wanted to go over with this is just the documentation.
[16:02] And I'm gonna use Dash HD. The other libraries are documented as well
[16:07] in a similar format, but this is the one that I think is the most complete
[16:11] because it has the most components. It's the most complex.
[16:13] And so when you hit one of these libraries as a developer, you're gonna see right up at the top,
[16:17] and this one's got a little bit more information because it does a little bit more,
[16:21] but you're gonna see, okay, here are examples of the inputs or outputs.
[16:25] So if I kind of know what I'm doing, I can look just at the top here and say,
[16:29] yes, this is the library that I'm looking for because yeah, I recognize this is an HD path
[16:33] or okay, I recognize this is an XPRIV. And so I know just from the first couple of seconds,
[16:40] am I in the right ballpark or am I out of the ballpark on what this thing is gonna do?
[16:45] And then they each have a table of contents. They have instructions on how to install.
[16:50] This one, because of the layering of it, has a little bit of depth to it where there's an overview,
[16:56] which we'll go to real quick. And this is just super, super, super fast
[17:00] and basically one screen. Here's just about everything this can do really quick.
[17:06] But if you're not familiar with it, the overview is not really gonna help you as much
[17:10] because you have a little bit more to learn. So there's also a quick start,
[17:13] very similar to the overview, but then broken down with here's how to handle errors.
[17:18] Here's some special conditions you need to be aware of, but just really light, just kind of more of the refresher.
[17:23] Then we have the API section, which is all of the different conversions, formats,
[17:29] things that this does, all condensed down as to how the functions are called.
[17:36] And then past that, we have each of them are broken down piece by piece
[17:41] with all the documentation that you need in order to operate this is in one place,
[17:45] not scattered across the entire internet. So we just go down and down and down here.
[17:50] Eventually we're gonna hit the tutorial section, which again is similar to the production overstart,
[17:55] except that it's for people that are yet a little bit newer, really need some handholding.
[17:59] So the tutorial section also references the API and the glossary sections.
[18:05] We'll just kind of go down here. So this walkthrough tutorial, again, like I said,
[18:11] it's just got more information. It's got more of the nuanced detail
[18:15] that you might not know if you're just getting started. It has a little bit more commenting.
[18:19] It has a little bit more code example, but essentially it's just, we're just looking at it.
[18:25] What scope of level of a developer are you? Do you need the full handholding experience?
[18:30] Do you need the refresher or do you need just, let me see what the functions are.
[18:33] I know which one I'm looking for when I see it kind of thing. And then down here, we have the glossary,
[18:38] which is where I've combined the terminology that's from the different BIPs,
[18:42] from the different libraries, and then not just the official names,
[18:47] but also the colloquial names, because there's a lot of times
[18:50] where you're searching for something, but it's referenced in many different ways,
[18:53] like PKH, pubkeyhash, publickeyhash. You might not know that PKH stands for publickeyhash.
[19:00] So if you just do a search here and you look for PKH,
[19:04] oh wait, this library doesn't deal with that. That's the dash keys deals with that.
[19:08] So nevermind, bad example. It's not in here, but this one has,
[19:14] you can see where in some of these, it says also key HD private key with address.
[19:21] So these are other terms that are synonymous with this term as we go through.
[19:27] - So as you, you were just about to, you called out one term that actually wasn't on the page.
[19:33] So I'm wondering maybe we could refactor this to have in the master glossary in that super repo
[19:40] or whatever you call it. - Yeah, so that is in progress right here.
[19:46] - Absolutely everything. 'Cause let me just say when I discovered you,
[19:52] which actually was many, many years ago, we live in the same town,
[19:56] but when I rediscovered you, you were doing some kind of PayPal integration
[20:00] into one of your websites. And I don't know if it was there specifically
[20:05] or somewhere else, but I've noticed along the way that you just do an excellent job of documenting everything.
[20:12] And that is worth so much because as kind of a novice developer myself,
[20:19] it's very hard to navigate these waters. And I've been doing cryptocurrency for like a decade now.
[20:26] And so I've read Andreas Antonopoulos' Mastering Bitcoin book, for example.
[20:31] So I know most of this stuff now, but even in that book,
[20:36] it's still difficult to, as a developer, really know exactly how to use these things
[20:43] and what they really mean. So this is a great resource.
[20:46] And speaking from the incubator's perspective, we need something like this if for no other reason
[20:53] than to be able to train new developers who are interested in the lower level intricacies
[20:59] of what's going on here so that we don't have knowledge just captured
[21:04] within six heads in Dash. We need this stuff to be very digestible
[21:10] for anybody who is, it takes some talent and it takes some skill
[21:16] to kind of grasp the concepts, but that's a necessary but not sufficient condition.
[21:22] You also need the smarts, but also the resources. And so this will bring,
[21:28] if somebody is like a talented developer that has no idea what cryptocurrency is all about,
[21:33] they could consume this and basically be up to speed in a month maybe instead of years.
[21:41] - Yeah, I mean, it definitely takes hands-on practice. The documentation alone isn't going to solve your problem.
[21:47] And there are nuances that are, I try to make more apparent,
[21:52] but that you do have to go through a little bit of trial by fire to understand.
[21:57] For example, the term passphrase is overloaded and misused across the ecosystem
[22:06] because in cryptography, we already have a concept of passphrase
[22:10] that has a specific meaning. In BIP44, I don't remember if it's BIP39 or BIP44,
[22:17] I get the numbers mixed up, but in one of the BIPs, it's referenced as one thing.
[22:21] In another one of the BIPs, it's referenced as not just the one thing,
[22:25] but two other independent things, including the industry standard definition.
[22:30] When you're learning about pubkey hash and address and stuff like that,
[22:34] it's a nuanced difference that they're the same thing, except one means the text representation
[22:41] that someone would see in the mobile app. The other one refers to the byte representation.
[22:46] So it gets kind of confusing with some of these things. Okay, address, wait, isn't this address?
[22:50] Isn't that address? Well, yes, this is address if it's been encoded as text.
[22:55] Take the same bytes, has the same meaning to the computer, decode it as a byte stream, now it's PKH.
[23:02] So there's a lot of that nuance that I tried to capture. Let me pull this back up on the screen here.
[23:10] As you can see right here, there's the pubkey hash definition.
[23:13] But if you are not, it's very easy, even with the documentation,
[23:18] there's a little bit of trial by fire that you're always gonna have to do.
[23:21] - Yeah, so this, it is fortuitous that we have, well, I guess technically all three of us
[23:29] are blockchain developers, and I'm defining a blockchain developer
[23:34] as anybody who gets paid in by, technically, I guess Rion is the main
[23:45] blockchain developer here, right? Because when the super block
[23:49] pays out of the Dash blockchain, it goes into however many wallets it goes into,
[23:56] and then being the proposal owner, Rion then divvies the payments out
[24:00] to contributors as necessary. But those details aside,
[24:05] technically all three of us are blockchain developers, as is Pete behind the boards today.
[24:10] And something that we got to talking about just loosely last week and then realized as we were,
[24:16] like, hmm, this is something we'd like to talk about with more people is, is it important?
[24:23] And if so, how important for a blockchain developer, whether it be software, marketing,
[24:31] business development, design, what have you, to be paid in the crypto that he or she works on?
[24:37] - Yeah, so we had a little after party, not official, but we kind of did a debrief last week,
[24:46] and we ended up talking about some of this stuff. And I just wanted to bring this
[24:50] more to a public conversation, because I think it's so important,
[24:53] and it's one of incubators primary values. So I thought it was appropriate.
[24:57] And I don't know when, should I press present here to get my screen going?
[25:03] - Yeah, go ahead. - So let me just share screen.
[25:07] And okay, and we'll share a Chrome tab. (mouse clicking)
[25:15] No, a window. Hmm.
[25:20] - Do, do, do, do, do, do, do, do, do, do, do, do, do, do. - I think this is the one.
[25:25] Let's see if this is the one. - That's the one.
[25:29] - Three tabs, yes, okay. I have way too many windows up,
[25:32] way too many tabs in each window. I'm gonna go back to my screen.
[25:37] So this is our monthly proposal, and I just wanted to kind of,
[25:41] I guess we're not quite into this segment, but as you can see, obviously,
[25:46] the Dash blockchain pays out in Dash. So the incubator asks for 1,000 Dash per month.
[25:53] And that, to me, is like the basis of how accounting should start.
[25:58] Like, we are a new currency. We are, to use Tao of Satoshi's term,
[26:05] we are a Dash nation that, basically, we have our own currency.
[26:11] And I think it's very important that we use that currency to its fullest extent.
[26:17] So money is a medium of exchange, a store of value, a unit of account.
[26:23] We've all heard these things. The unit of account, I think,
[26:26] is more important than we really realize. And so incubator does all of its accounting in Dash.
[26:34] So we're using it as a unit of account. And we only do payments in Dash.
[26:42] We don't support any kind of fiat payments. And I know that other organizations do, obviously.
[26:50] Dash Core Group does. My hope is that we, as a community,
[26:56] we, as a nation, whatever, as an economy, as I like to put it,
[27:00] that we move towards using Dash as a currency to the fullest extent.
[27:07] And so, like I said, we do that in the incubator. And when you, it's kind of interesting what happens
[27:13] when you kind of just make that decision. You make that decision, I'm going to do my finances,
[27:20] my payments, my savings, all in Dash. And sometimes you have to convert to fiat to pay a bill.
[27:28] But most people think of it in the opposite sense, where sometimes, they do all their thinking
[27:32] and they do all their accounting in US dollars or whatever. And then sometimes they'll convert some of that,
[27:40] some of those dollars into Dash, and then they'll maybe buy something with it.
[27:43] But when you flip the switch and you say, by default, everything is in Dash, things happen.
[27:51] Like, for example, I've kind of forced myself to, because I receive all my income in Dash,
[28:01] I have to find ways to use Dash in the most efficient way. And so I've actually convinced my landlords
[28:08] for many, many years to accept Dash. And that's what happens, not just with me,
[28:14] but with every single incubator developer. I'm sure AJ can actually also say something
[28:19] about this as well, because he gets paid in Dash. And I know that he actually does payments forward in Dash.
[28:28] So maybe you could talk a little bit about that, AJ. - Yeah, I think, I'm not a true convert like you are,
[28:36] but I believe that anytime you're doing work, you need to use the product.
[28:40] That is my pet peeve with, being a software developer, that's my pet peeve with all softwares.
[28:44] It's apparent that people who develop Google Maps, they sit in an office building,
[28:49] they walk one block to get to their dormitory, they've never driven a car in their life.
[28:54] They obviously, you know, and so the same thing, I get frustrated with the Dash tools,
[28:59] because to me, it looks like people aren't using this, because if they were using this on a daily basis,
[29:05] they would know that this does not work when I'm standing in line at Best Buy.
[29:10] This does not work when I'm trying to pay a contractor, et cetera, right?
[29:15] And so I think that it is incredibly important to eat your own dog food and not just blindly follow along
[29:24] with, okay, here was some spec, here was some idea, here was some proposal.
[29:27] No, you need to use it and figure out, does it work in the real world,
[29:32] not just does it work in the theory of the unicorn world? And it's interesting you mentioned Dash Nation,
[29:39] because that's the term that I independently started using when I'm talking to people.
[29:43] I say, well, Dash is not just, it's not a cryptocurrency, it is a belief system that people buy into
[29:51] that's, dare I say, libertarian, hopefully not to offend anybody out there
[29:55] that doesn't believe that that's what this is, but that's the way I see it.
[29:58] It's get out of my life, let me make, as an adult, agreements with other adults,
[30:05] and figure out what we believe together and not have that thrust down upon us.
[30:10] Yet within that system, we still have all of the same constraints and opportunities
[30:15] as with many other monetary systems. We wanna save, we want to put some things
[30:20] in a business account, we wanna put some things in a personal account,
[30:23] and we need tools for that. And I think that's where,
[30:27] I believe that's where Dash Incubator is going to be really shining this year and next year
[30:33] as we continue to develop the tools that have been seeded here.
[30:38] - So what I was hearing from you, Rion, is that a blockchain developer getting paid
[30:42] in the crypto they work on necessarily forces them to expand the economy
[30:47] of that cryptocurrency because they're looking for, okay, who's going to accept this
[30:53] for the various things that I need to spend? Even if it's no more, no less
[30:57] than I'm gonna sell it all for fiat, they're still looking for a broker
[31:02] or an exchange to do that. And then what I was hearing from you, AJ,
[31:06] is that a blockchain developer getting paid in crypto is going to improve his work
[31:11] because now he's using the product in real life as opposed to just working on it
[31:16] in the abstract or in theory. And I see both of those and would add maybe a third,
[31:23] which is, I think that a blockchain developer getting paid in the crypto that he works on
[31:30] also is going to create a sort of, whether he knows it or not,
[31:34] is gonna create a sort of shift in his mind as it pertains to, dare I say, loyalties or allegiances,
[31:44] which- 100% could not agree more.
[31:46] Yeah, because I've wondered before- It's subtle.
[31:49] Employees who get paid in stocks or have the option to take some of their payment in stocks.
[31:55] I've thought before, like, what if, you know, an Apple employee were being paid in Microsoft stock
[32:02] or a Coke employee paid in Pepsi stock? Like a lot- A lot of them do, actually,
[32:07] which creates that loyalty. Yeah, and so it creates someone who's, you know,
[32:13] I guess, looking to serve two masters, I guess. And as the saying goes, no man can serve two masters.
[32:19] And so that's another dynamic that I like to think about of just, you know, what-
[32:26] I think the user named Badger on Dash Central, he said something the other day, like, you know,
[32:34] at the end of the day, if Dash's developers don't need Dash to do well in order for their families
[32:41] to eat, you know, that's going to change things. Yeah, it's kind of like burning the ships.
[32:48] You know, you cross an ocean and you discover this new land and you might be tempted to go back
[32:56] to your former abode or land, but the truly dedicated, they just burn the ships.
[33:04] You know, you get there, you burn the ships. There's no getting back.
[33:07] You just have to make your way in this new land. And that's what we've done, so, or continue to do.
[33:13] So anyway, do we want to go? I did want to talk about a little bit about
[33:20] how we actually do that, those payments and whatnot in the Dash incubator, just for everybody's understanding
[33:31] of how it works and that everybody can know where this data is.
[33:38] And I brought up this proposal first because I just wanted everybody to know
[33:42] that you can recreate this data if you'd like. So you see these plots here, these figures,
[33:51] and I want to let everybody know where these come from so that they can either double check them
[33:59] or kind of create their own tables or views. So it all comes from this Dash incubator accounting sheet,
[34:08] and this has been public since day one. So we'll drop a link to it, I'm sure,
[34:13] in the video description here. But when we do work in the incubator,
[34:19] right now we're doing work using Trello as a project management tool.
[34:27] We have been trying over the months to switch over because it's not quite ideal for us.
[34:35] But when somebody comes and makes a claim, they do that or they want to work on a project.
[34:42] First, you sign up here. Then if you want to create a new project,
[34:45] you request a new concept to be considered from amongst the incubator strategists.
[34:53] And if one of those incubator strategists accept it, then it becomes one of these cards.
[34:59] And let's just say, let's bring up this, the project that we're working on right now,
[35:05] which is Incubator Updates. We could probably rename this to Incubator Weekly
[35:10] 'cause that's what this is. This is the project that we're doing right now.
[35:16] As you can see, my computer is really struggling because it's pretty old
[35:24] and I'm doing the streaming software, but let's see. As that pulls up, that's one of the things.
[35:33] Trello is actually one of the worst offenders when it comes to...
[35:36] - We can hear you, Rion, but there is a sort of freezing. - We could hear you.
[35:52] - Oh, he's disappeared. The internet took him.
[35:56] - This was actually planned. So while Rion is reconnecting,
[36:04] whatever he is reconnecting on his end, I wanted to make mention of something
[36:11] that we said on the show last week, which was that this week,
[36:15] we intended to give a full walkthrough of the incubator's workflow,
[36:21] which is to say like, these are the various websites that are used.
[36:25] This is the steps that one would take, which Rion just, again, talking about just a little bit,
[36:30] to sign up to be a contributor, to either try to claim a bounty
[36:34] or even propose a fresh brand new bounty. And Rion asked that we hold off
[36:43] on doing that full walkthrough for a future week because I guess the processes are seeking to be improved.
[36:51] Something about Trello and GitHub, I don't know. Don't ask me.
[36:55] So to touch back on that point, the full walkthrough of like a,
[37:02] hey, how to incubator steps one, two, and three is something that we will do in the future.
[37:09] Today was intended rather to be just an overview of the accounting process of the incubator
[37:19] so that if and when one would like to do a financial audit to whatever extent,
[37:27] that it's basically one goes to the treasury proposal. And in fact, maybe I can screen share from my side,
[37:35] especially if we have lost dear Rion for good. - Yeah, he said that his computer ran out of battery.
[37:44] It looks like, oh, and he's back. - I was still alive.
[37:48] - Well, hello, Rion. You fellows sure like to keep me on my toes, don't you?
[37:56] - Sorry about that. I'm blaming it on the presidents, by the way.
[37:59] This was President's Day problem because I went to the office and it was closed
[38:03] because of President's Day 'cause I work at a university for a coworking space.
[38:07] Anyway, I'm back. - Would you like to share your screen again
[38:12] or would you like me to share the same thing from my end, at least the Dash Central page?
[38:18] - I'll share it. - Okay.
[38:20] - Yeah, let's see. Okay.
[38:24] - Name that song. Whoever can name this song,
[38:26] I'm gonna give you a little treat. ♪ Do, do, do, do, do, do, do, do, do, do, do, do, do ♪
[38:34] - I know this is- - And it's back to you, Rion.
[38:36] - I don't, I'm not able to name it, but- - No, the treat is for you guys.
[38:40] It's for the viewers. Please continue.
[38:42] - Okay. So when somebody does a claim on a project,
[38:47] they enter it into the Trello board and then basically everything that is entered
[38:55] in the Trello board in terms of claims gets copied over. So somebody might claim task seven,
[39:05] for example, right here. And then when that claim is approved,
[39:09] it's the information is copied over to this spreadsheet, basically word for word,
[39:17] and just put into the various data fields. And that makes up this table.
[39:23] And then this table, you know, there's the address that is paid from the claim,
[39:31] and there's the output links. And then if the project is paid,
[39:36] then the transaction ID would go here. If it's not paid, somebody would write ready right here,
[39:41] and then it would populate a page for me to make a payment for that.
[39:46] But that's how basically this page is made. And you can see exactly what all the payments have been
[39:53] from the history from day one. Then that feeds over into this reward summary page
[40:04] where the data is put into summary tables, pivot tables. And then that's just copied over into,
[40:14] and then you make charts from that. So all of this is open to the public again.
[40:21] So that's where these figures all come from. I just wanted everybody to kind of know exactly
[40:28] where our tables come from in the proposals. That's where it comes from.
[40:32] And if anybody has any further questions about that, I'm happy to answer those,
[40:37] but that's probably enough for people to know where to get started if they want to look deeper into that.
[40:44] - Great. Okay, so if that covers the finance overview segment,
[40:52] while you were getting situated, Rion, I let the viewers know that you had expressed to me
[41:01] that we'd like to hold off on the sort of workflow walkthrough
[41:06] because of maybe some planned migration or something or some planned tweak to it.
[41:14] Is that something that you could enlighten us about? - It'll be better.
[41:17] We'll do the deep dive walkthrough about exactly how to get started with the incubator
[41:21] and how tasks are managed and how claims are made and all that, like the process of doing work
[41:30] and then claiming the tasks for those works and getting paid and all that.
[41:34] We'll do that when we actually do our full switch over to GitHub.
[41:37] - And what do you mean by full switch over to GitHub? You mean goodbye Trello?
[41:41] This can all be done via GitHub? What do you mean?
[41:44] - Well, we haven't fully decided yet, but we're all leaning towards
[41:47] just fully going over to GitHub. But there is a small chance that we might leave it open
[41:52] to have different platforms and that each strategist could have their own
[41:57] project management tool. And so maybe if somebody wanted to stay on the Trello board
[42:03] they could, but as far as I'm concerned, personally Trello doesn't suit my needs
[42:09] as well as GitHub does. Most of our work is software development.
[42:14] So, and most software development is done on GitHub. So it makes more sense to just have the project management
[42:22] there and GitHub's made a lot of progress in those terms recently.
[42:26] So that's why we're considering moving over. And when we do, we'll kind of create a new demo
[42:32] of how to do that. If anybody's interested in knowing how to do this right now,
[42:40] Joelle Valenzuela has made a video and we'll post a link to that walkthrough
[42:48] of how to do it in the Trello board. - Righteous.
[42:53] Well, that wraps up our three segments for today. AJ, Disruption Master,
[43:00] is there, are there any thoughts you'd care to leave us with?
[43:03] Oh, Holly, why are you muted? - Oh, that was me.
[43:12] I muted myself. Sorry, I wanted to be able to fart
[43:16] and not let everybody know. - As we've discussed before.
[43:19] Well, thanks for that. Okay.
[43:21] - Yeah, it's okay. I did that one time live.
[43:23] I thought I was muted, but anyway, I was just saying. - You've done it more than once live.
[43:27] I'll just tell you. I watch them all.
[43:30] - Well, yeah, but sometimes I point it out. You know, I'm like, oh, got to let one loose.
[43:33] But other times, anyway. Yeah, that's what I'd like to leave us with.
[43:37] I'd like everybody to have that imagery and smellagery and sense of my professionalism
[43:43] as I continue working on these tools. - Right on.
[43:47] And Rion, do you care to respond to Joelle-Louise here? - Sure.
[43:53] Honestly, we're not, I wouldn't say we're promoted anywhere. Like we don't really focus on promoting.
[44:00] Just recently, we have restarted our promotion efforts by, you know, Amanda right here,
[44:07] or right here does have run our Twitter account for the most part.
[44:12] So we are on Twitter. We do have a presence on GitHub,
[44:18] but we're not really actively promoting that either. And we spend a lot of time on Discord.
[44:28] So, but anywhere where you want us to be promoted, we, you know, we're happy to, happy to accommodate.
[44:36] - And if, and dare I say when, the Incubator has its first live event,
[44:41] be it a hackathon or a conference, we'll definitely have the booth babes on order.
[44:46] Okay, we do have one more question here from Joelle. Can you guys hire any former library dubs?
[44:53] - That's a good, I'm glad he phrased it that way, because it gives me an opportunity to say
[44:57] that we don't hire anybody. Everybody is both already hired and will never be hired.
[45:03] You don't have to be hired to work in the Incubator. You just show up and say, I'd like to do this.
[45:11] And the best place to talk, the best place is to talk to either me
[45:17] or one of the strategists or just anybody in the Incubator, and we'll be able to tell you how to get going.
[45:23] But you just, basically you show up and you say, I want to work on this task.
[45:27] And if that's a task that one of the strategists want to pursue, then we get you going.
[45:34] And that said, to really answer the question, yes. I think one of the, one of the things that I want more,
[45:43] more than anything is self-directed developers and self-directed project managers in the Incubator.
[45:50] I don't want to have to, I don't want to be the focal point or the choke point as it were.
[45:56] So if these developers are interested, tell them to, you know, come up with projects,
[46:03] have an idea, come to me with three tasks in mind that you want, you want to do work on this project
[46:10] and it has these three tasks, or I want to start with a specification task.
[46:15] You tell me what you want to do. And I will see if that fits within my strategy.
[46:20] And most things do. I mostly work, mostly looking for motivated self,
[46:26] self-starting, self-directed developers that already know what they, how they can add value to Dash.
[46:33] And then I just kind of help facilitate that and organize it.
[46:38] So yeah, send them our way. And they'd be great to work on some, some library projects
[46:44] if that's still allowed, I guess, by the government. It's such a silly thing.
[46:50] I know they're going through a hard time right now, but I don't know if that is affecting
[46:55] just the front end part of it. There was a separation.
[47:01] There's library and then there's something, Odyssey. Yeah, and I think the problem was with Odyssey,
[47:07] not with library. So I'd love to have some library integrations.
[47:10] Let's talk. - Okay, well, thanks for joining us today
[47:17] on Incubator Weekly, everybody. And we look forward to seeing you next week.
[47:24] Same time, same place. Yeah?
[47:26] - Yep. - Bye for now.