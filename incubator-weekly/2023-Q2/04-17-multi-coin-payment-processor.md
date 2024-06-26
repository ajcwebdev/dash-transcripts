---
showLink: "https://www.youtube.com/watch?v=HE_phiVr-C8"
slug: "multi-coin-payment-processor"
title: "Multi-Coin Payment Processor Back & Better Than Ever"
publishDate: "2023-04-17"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/HE_phiVr-C8/maxresdefault.webp"
---

Mikhail, a Dash developer, demonstrates the functionality of AnyPay, a multi-coin payment app that he helped fix and improve.

## Episode Summary

tl;dr: Mikhail, a Dash developer from Russia, joins Incubator Weekly hosts Amanda and Rion to discuss his work on AnyPay, a multi-coin payment app. He explains how he updated the project, added continuous deployment, and fixed issues that were causing the app to malfunction. The hosts share their experiences using AnyPay and discuss the app's features, such as supported coins and the merchant registration process.

## Chapters

00:00 - Introduction and Beginning of Episode
The episode starts with a discussion on central bank digital currencies (CBDCs) and their potential implications.

05:34 - Guest Introduction and Background
Mikhail, a Dash developer from Russia, is introduced. He shares his background in coding and his involvement with the Dash incubator.

09:29 - AnyPay Project and Incubator Involvement
Rion explains how the AnyPay project became a bounty within the Dash incubator and why it was important to support the app's development.

15:19 - AnyPay Demo and Functionality
Mikhail demonstrates the functionality of the AnyPay app, showing how merchants can accept payments in various cryptocurrencies. Rion tests the app by making a payment using Dash.

20:22 - Additional Features and Development
The discussion covers potential future features, such as split payments, and the technical aspects of adding new coins to the app.

21:13 - Merchant Registration Process
Mikhail explains the process of registering as a merchant on AnyPay and the ease of setting up the app to accept payments.

25:27 - Wallet Compatibility and Payment Protocols
The hosts discuss wallet compatibility issues with AnyPay and how the app handles different payment protocols.

27:16 - Monetization and Conclusion
The conversation concludes with a brief discussion on AnyPay's monetization strategy and a thank you to Mikhail for his work on the app.

## Transcript

[00:00] Central bank digital currencies are a hot and controversial topic of late. We've seen everything from U.S. state governors claiming that they're banned in their respective
[00:10] states, to presidential hopefuls and even senators claiming that CBDCs must be banned nationwide. But what are these individuals actually saying? Is it possible that, in true political style,
[00:25] they're actually saying not much at all? Because really, doesn't America, and basically every other country on earth, already have a CBDC? Bear with me here.
[00:36] Take the U.S. dollar, for instance. It's issued by a central bank, and most people who use it do so via digital methods. That is, with their bank account, they digitally spend dollars by swiping
[00:50] a debit or credit card, or connect to Venmo or other payment apps, etc. Thus, we're talking about a central bank-issued currency being used digitally. A central bank digital currency, CBDC.
[01:06] But wait, wait, you say, that's not what a CBDC is. A CBDC is when end-users interact directly with the central bank. That is, the central bank itself oversees and processes every transaction
[01:22] in real time. You may even say that such a scenario would inevitably lead to much-touted horrors like carbon allowances and social credit scores. But just how technically feasible is it
[01:36] that a single institution could process, secure, and monitor every financial transaction within an entire country 24/7? To find out a plausible answer to this question, we should just listen
[01:51] to what one of the pilots of the world's single most advanced and longest-running CBDC programs has to say about it. The Chinese digital renminbi, or e-yuan as it's been called, has been in
[02:06] development since 2014. This is longer than most cryptocurrencies have existed, by the way. And six years into testing the e-yuan, Deputy Governor of the People's Bank of China,
[02:21] Fan Yifei, had this to say about it. A one-tier system where the central bank directly interacts with the public would not be viable. A two-tier model, on the other hand, where intermediaries
[02:35] are involved, could help the central bank to optimize the convenience and accessibility of a CBDC. Financial institutions, such as commercial banks, have fully developed IT infrastructure
[02:47] application and service systems with strong processing capabilities. To build a separate system would be a tremendous waste of such existing resources. Instead, the central bank
[03:00] can leverage market forces to optimize related systems through close cooperation with commercial banks and other organizations. It would be unrealistic to expect the People's Bank of China
[03:14] to develop such a massive system all by itself, while ensuring a high level of transaction security, efficiency and reliability, and user satisfaction at the same time. In other words,
[03:28] Fan Yifei is saying that the best system for a Chinese CBDC is the system they already have. That is, a system in which their central bank issues the monetary units, and their commercial
[03:43] banks make these units available to the public. It's basically the same setup we've all known our entire lives, with some minor tech upgrades. But this viewpoint isn't very sexy, is it?
[03:57] It's not exciting to think that the cryptosphere's greatest boogeyman is already here and has been the whole time. So let's end this report on a note of excitement.
[04:08] Let's just pretend that, against all odds, one or more legacy governments around the world is able to create, maintain, secure, and operate a centrally monitored payment system for an entire
[04:24] country. And that it's complete with all the horrors you've heard about online, like account freezes for exceeding a carbon score threshold, and seizures of funds for expressing unpopular
[04:38] opinions on social media, and prohibitions against buying things like guns and gold, etc. etc. In case it hasn't dawned on you, any people confronted with such a dire situation
[04:53] would be more ripe for cryptocurrency, and specifically Dash, adoption than ever before. Such serious impediments to everyday commerce would make the permissionless, private,
[05:06] and uncensorable nature of Dash more attractive than any ad campaign we could possibly come up with. So, whether you agree that CBDCs are already here, or whether you think that they're yet to
[05:20] come, we can agree on one thing - that the worse and more dystopian they are, the better the market opportunity for digital cash. And this is why we build.
[05:34] Hello and welcome to Incubator Weekly. I'm your co-host Amanda and I'm joined by my co-host Rion. Hi Rion. Hi everyone. Today our guest is Mikhail. He is a Dash developer within the incubator
[05:57] who is calling us from smack dab in the center of Russia. How are you this evening, Mikhail? Hi, I'm feeling very great. Great. Well, Mikhail, let's start out before we dive into AnyPay,
[06:13] which is the multi-coin free and open source payment app that you saved. Before we dive into that, first we want to learn a little bit about you. For example, your professional
[06:26] background. How did you learn to code? Well, it's been a long time since I started coding. I think I started coding in high school and it always was something about the cryptocurrencies.
[06:43] I even remember the times when there was CPU mining and I'm actively developing some crypto stuff. Since 2016, I believe, there was a lot of products like
[07:04] payment gateways, like mining pools, what else, wallets, other projects that I developed for the foreign customers. So, yeah,
[07:20] kind of like that. And for the last year or one and a half year, I was working for Dash. I even worked in the DCG for a while and now I'm here in the incubator, pushing stuff together.
[07:39] So, how did you find us as your current foreign customers? How did you find the Dash incubator? Well, actually, Sam Westrich asked me to here. I was working in the DCG and then he just told me
[08:01] about the incubator that I can work here and, yeah. Right on. And by the way, are you calling us from within a sort of spaceship or maybe decommissioned missile head or where are you?
[08:19] Well, it's just a cafe in the city of Innopolis. It's near Kazan. This is a very modern town that connects IT people together. A lot of IT people work here. So, that's something like an
[08:43] incubator for IT projects for different. And there are a lot of science stuff, you know. And, yeah. This is a very modern city, a very modern town.
[09:00] It almost looks like one of those Zoom backgrounds that's fake. It really does.
[09:05] I think it's real. No, it's not fake at all.
[09:08] And I was told that everybody who lives in Russia lives in a mud hut and eats dirt. And so, here is Mikhail totally proving me wrong.
[09:15] Yeah, yeah. There is concrete everywhere here in this Innopolis. Excellent. Okay. So, Rion, will you tell us how the Anypay project came to be a bounty
[09:29] with an incubator? Yeah. It came to me from Joel, actually. And Joel was saying there's some problems with the
[09:40] Anypay app and we've got a lot of merchants, especially here in New Hampshire, here meaning where he is. And can the incubator help out? Because I guess Anypay has pivoted their focus
[09:56] a little bit more towards API users rather than their users of a user interface from them. And so, they didn't have the bandwidth and time to take these issues on.
[10:14] And so, Joel was asking, "Can we do this in the incubator and just knock it out?" And I think I just posted a message to see, "Is anybody willing and able to do this?" And
[10:26] Mikhail stepped up and said, "Yeah." And so far, it's like he's just been knocking them down, knocking down these issues one by one pretty easily. So, I've been very happy with that.
[10:38] And I was a little bit reluctant to take this on because it's like helping out a third party. And I don't want to play favorites with any one provider, but the reality is we don't really have
[10:58] a lot of great applications for if a merchant wants to accept Dash payments and they have hardware to do so, like a tablet, then what are our options? We have a lot of, it seems like,
[11:15] e-commerce options where it's not like a physical location and a physical device that you're interfacing with. But if you have a physical location and you want to accept Dash payments
[11:27] or any of the other supported payments on their platform, what do you use? And Anypay is one of the only ones that I know of, and it might be the easiest one to use. I actually remember several
[11:39] years ago, we had a food truck event in Salt Lake City. And we weren't running a food truck, but we were running a Dash booth. Me and my now wife were running a Dash booth because they gave
[11:57] us some free space there. And so we wanted to connect with all the food trucks and say, "Hey, you want to accept Dash, we're going to give out some Dash at this event just to people who are
[12:09] interested in walking by so they can take the Dash that we give them. And then these food truck merchants, they can just really quickly download the app or whatever the process is." Maybe Mikhail
[12:22] can talk more about that in a minute. And accept Dash payments. And so we actually used that Anypay in that capacity several years ago. And I don't know of any other better solution at this point
[12:34] even. But I just figured, we need to get this fixed so that we can serve these customers that are using Dash in the best way possible. This is really our end goal is for merchants accepting
[12:51] Dash natively. And so yeah, I wanted to support this project. And I have to also say, because it's been on my mind this morning, I'm on a little bit of a natural high this morning because
[13:08] my wife celebrated, we celebrated her 40th birthday today. Her birthday is actually tomorrow. But we took a hot air balloon trip this morning in the beautiful Heber Valley. And it was amazing.
[13:27] It was just like the perfect weather and everything, perfect views. And at the end of the balloon ride, I wanted to give our guide, our pilot, a tip in Dash. And he was super excited to
[13:42] get that tip in Dash. And so yeah, at some point, maybe they'll accept cryptocurrency natively for their services. But it was amazing. And just wanted to say, happy 40th birthday to my wife.
[13:58] And couldn't be happier. And made a little Dash connection as well there. So hopefully that was okay. >> Well, it does sound like a wonderful day. Happy birthday, Rachel. I know that I'm
[14:10] personally, or have been in the past, personally affected by the performance of the AnyPay wallet as well. My husband and I used to live in New Hampshire, which is the area, as Rion mentioned,
[14:21] that has the most brick and mortar merchants using AnyPay, to my knowledge. And my parents came to visit us. And we took them to this coffee shop. And I was, as we're standing in line,
[14:36] I'm bragging to my dad. Oh, dad, this place takes Dash. Wait till you see me pay for our order with Dash. We were really living in the future now. And I was just super bragging.
[14:49] And we order. And the cashier brings up the AnyPay invoice. And I pay. And it was broken. Like nothing happened on their side. I don't even remember if my payment went through or not. But
[15:03] it was just broken. And thus did break my spirit. And so, yeah. Super glad to have this back online. So, without further ado, shall we have a look at your demo, Mikhail? Okay. Let's do it.
[15:19] >> Sure. So, basically, AnyPay is an application that you can download from App Store or Google Play. When you open it on your device, you will see a login screen where you can
[15:36] log in to your account. I will log in to my account. And I will show you how it works. So, basically, you can see the cashier. So, anyone who wants to accept payments in crypto,
[15:58] he opens the app, then goes to the settings. There are a couple of coins that are supported by this application. You can see it on the screen. So, for example, Dash, you set the address that
[16:14] you want to receive for your products on the screen. I already have a defined one. I said later. I mean earlier. Sorry. I will go back to the main screen. For example, you want to charge
[16:34] two dollars for something. You just type in the numbers and try to create an invoice. Here we have the QR code. You can scan the QR code with the Dash wallet.
[16:55] I have a Dash wallet on my iPhone. I just type the scan button and scan it with my phone. >> Well, maybe one of us should have scanned it.
[17:10] >> Yeah, Brian. >> Are you sure? >> Okay. You can go and go ahead. >> I'll try it.
[17:17] >> Oh, sweet. >> Since I just used this this morning, the sync should be updated. Hopefully, you're not charging me. Oh, it's two
[17:28] dollars. So, okay. Please wait. Wow, that was an interesting. I've never seen that animation on the Dash wallet. That was interesting. So, I see the two dollars. I should have shown the wallet,
[17:39] actually. Let's see. Two dollars. Sending. And just sent. Oh, wait. Yeah. I sent. Yeah. There we go. Nice. Joel was saying that that was the part that there was a problem before.
[18:02] >> Yeah. Easy as a piece of cake. So, previously, the application was broken, and on this view, we had like blank screen, the white screen, and it wasn't showing anything. It was updated by me.
[18:20] The most hard part was about updating the projects because the application wasn't pushing any code for, like, two years or something, and a lot of things changed,
[18:34] especially on the devices. I think, like, SDKs were upgraded or something like that, and, yeah, the first big part is updating the project for the recent SDKs, and then I made a very big feature,
[18:54] which is called, like, continuous deployment. As the project is open source, anyone can suggest changes to this project, and after the pull request is being merged into the repository,
[19:12] the CircleCI pipeline is getting called, and the application automatically deploys into App Store or Google Play. So, now, Anypay have continuous deployment CircleCI pipelines, and it will
[19:30] reduce amount of resources needed for maintaining and deploy application because previously, it has to be approved with Anypay app. They had to check. They had to
[19:47] hire someone to make a build, then this guy that was making a build was necessary to get the keys, and the keys are now in the CircleCI, so they never get shared with the developers,
[20:08] which is great, even with me. So, yeah, everything is secure and automatic. Okay, James Doe wants to know, "Can you make a payment where several people can
[20:22] pay to complete a larger payment, like individual payments for dinner?" Technically, it's possible, but it's not implemented yet. I think
[20:34] just the task needs to be given, and I will make it. And with crypto, such a thing would be a bit easier in that, you know, all the people who
[20:50] did want to throw down on a bill or whatever, worst-case scenario, instead of paying the same bill, they just pay their single friend, and then their single friend pays the bill. And with Dash,
[21:01] you would get instant confirmations all around, wouldn't even need to wait for a confirmation, or I guess instant settlements, I should say. Don't use the wrong terms.
[21:08] Rion, how about you take it away from me? Take what away from you?
[21:13] I don't know. What did we want to know about? We wanted to know, are there any particular… I did have a question. So, you started the demo from the point where you were already a merchant
[21:24] and already had registered, but I'm kind of curious what the process is for registering as a merchant. What kind of information is required? How long does it take? Is it something
[21:36] that you could set somebody up with on the fly, or is it more of an involved process? Is AnyPay involved in this, or is it mostly self-hosted? Can you speak to that? I know
[21:50] you're on the development side, and it's not your product and everything, but what do you know about that?
[21:57] Yeah, I can answer that topic. So, basically, AnyPay is an open-source app, and you can build and deploy everything, including the backend and the client application. But by default,
[22:15] for what we have in the App Store, the system is using the default backend server deployed by AnyPay. So, in order to register you as a merchant, it's very easy. You just
[22:30] download the application, register there with your email, set the address for your favorite coin, and then you can accept payments.
[22:41] So, let's see those coins. If you can bring up your demo again, what coins do they accept, and how easy would it be to add a different coin if you were interested in doing so?
[22:52] So, right now we have like eight coins, I believe, yes, and other coins can be easily added, but you have to make the changes in the backend. So, just implement the new coin and add it in
[23:21] the application. Yeah, not that I'm interested in that. All I care about is that middle blue option that's
[23:29] dashed. I like the order there. It kind of pops right in the middle. It's the best one in there, but I do like a lot of these other coins as well. Bitcoin Cash, particularly, is
[23:40] very functional. Yeah, I'm kind of surprised to see Polygon on there. Yeah.
[23:47] Mikhail, when somebody chooses to pay with any of these coins, does the paid screen show up immediately upon receipt of broadcast, or are there any coins where the app
[23:59] waits for a confirmation before the paid screen shows? In other words, they accept zero-conf payments.
[24:09] They accept zero-confs. Yeah. So, as long as the transaction is getting into the network, the application will see it.
[24:21] Okay. So, it shows paid when the network sees the transaction, not when it's settled?
[24:28] Yes, yes. Okay.
[24:32] Is AnyPay integrated in the Dash wallet? Is that a plan, or are these two completely different projects?
[24:38] I can answer that, I think. So, that's like a different project, but you can pay the AnyPay invoices with your Dash wallet. So, it's kind of like connected together, I think.
[25:03] And also, we had previously a map where you can find the merchants on the map. So, where you can see the merchants that are active, and you can filter them by Dash.
[25:21] So, yeah. That brings up another question for me.
[25:27] Can AnyWallet pay an AnyPay invoice just as easily as any other wallet? Because I want to say I remember years ago, again, in New Hampshire at this pub,
[25:41] I went to pay an AnyPay invoice, and I don't remember there was a problem, and somebody said, "Oh, you need to use a different wallet.
[25:50] You need to use a wallet that supports such and such protocol." And I'm like, "What?" So, yeah. What's that about? And is it still the case?
[25:58] Well, when you scan the QR code, some wallets will try to recognize some protocols, and try to use it. But as I know, there are issues with the Edge wallet right now,
[26:18] because it incorrectly, well, they drop the support for the payment protocol that is implemented with AnyPay. And we are going to break it up again.
[26:30] I've already got this task. But on the other hand, you can always pay by the address.
[26:44] So, if any of your wallet automatically doesn't recognize the invoice, you can always pay by the address, and it should definitely work.
[26:55] Great. Okay. Well, I think that, yeah. I guess the only question I had was, just out of curiosity, does anybody know how the AnyPay team did or did not monetize this
[27:16] back when they were developing it? Or maybe did they kind of abandon this project because, hey, it was free and open source, and there wasn't a monetary model? Does anybody happen to know?
[27:27] I don't know. I would just say that it sounds like their API service is doing better, and so that's what they're focusing on.
[27:35] So, the API service does serve up this AnyPay, or it doesn't? I don't know. I could probably wing an answer, but I'll leave it to the AnyPay guys
[27:48] to maybe comment on the video or something. Cool. All right. Well, absent any final questions or comments,
[27:57] do either of you have any final questions or comments, gents? No. Just thanks to AnyPay for me. It's nice to have a company that's supporting Dash and has
[28:07] been for a long time. So, it's a great application, and I'm glad that we could help fix it. Great. Well, yes, we wish the AnyPay guys well, and we thank Mikhail for joining us today and
[28:21] giving us that demo. And we will see you all again next week here on Incubator Weekly at the same time and in the same place. So, thanks for joining us.
[28:31] See you. Later. Bye.