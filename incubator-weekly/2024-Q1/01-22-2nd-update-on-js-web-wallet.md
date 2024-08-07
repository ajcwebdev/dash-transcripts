---
showLink: "https://www.youtube.com/watch?v=TTlk_HxfCoY"
slug: "2nd-update-on-js-web-wallet"
title: "2nd Update on JavaScript Web Wallet"
publishDate: "2024-01-22"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/TTlk_HxfCoY/maxresdefault.webp"
---

A web wallet for Dash digital cash is being developed with a focus on speed, security, and simplicity.

## Episode Summary

tl;dr: Jojobyte and Rion demonstrate a web wallet being developed for Dash in the Dash Incubator. The wallet uses client-side encryption for security and loads in under 0.3 seconds. Near-term plans include integrating features like Crowdnode masternode pooling, gift card purchases, and the Maya savings app. The wallet aims to make Dash more accessible as digital cash, especially compared to a larger competing web wallet.

## Chapters

00:00 - Introduction and Background on Bitcoin ETF Approval
The episode begins with a satirical intro about the SEC approving a spot Bitcoin ETF, framed as underwhelming compared to protocol improvements that could make Bitcoin better electronic cash.

05:08 - Demo of Dash Web Wallet in Development 
Jojobyte shares his screen to demonstrate a web wallet for Dash being built in the Dash Incubator. Key features shown include generating a new wallet, pairing wallets to send funds, backup and restore functionality, and client-side encryption.

22:19 - Discussion on Benefits of a Web Wallet
Rion and Jojo discuss the benefits of a web wallet, including censorship-resistance, accessibility without app store approval, and ease of integrating new features. Near-term priorities include Crowdnode pooling, gift card purchases, and Maya app integration.

39:45 - Security Considerations and Comparison to Other Web Wallet
Amanda asks about adding multi-sig support for security. Rion suggests it's not an immediate priority as the wallet is not intended for large balances. The wallet is compared to another Dash web wallet, with this one loading much faster.

## Transcript

[00:00] The most historically significant thing that's ever happened to Bitcoin just happened.

[00:10] What, privacy at the protocol level and an increase in block size to end congestion, drastically lower transaction fees, and become peer-to-peer electronic cash?

[00:18] A spot Bitcoin ETF was finally approved. A spot Bitcoin ETF?

[00:24] Following that decision that some have described as historic, is the SEC Chair, Gary Gensler.

[00:30] Chair Gensler, we appreciate you being with us. Let me start by asking you this.

[00:34] Do you consider the decision historic? The decision referenced is the U.S. Court of Appeals for the D.C. Circuit,

[00:40] siding with Grayscale over the SEC to launch a Bitcoin ETF. And it appears that it's a decision that you made either reluctantly or perhaps even begrudgingly.

[00:52] Well, look, Andrew, this has been considered for a long time. As you know, starting under Chair Clayton,

[01:04] we had disapproved a number of these over the years and something had changed. I'm a deep believer in the rule of law and a respect for the courts

[01:14] and taking a new court decision into consideration. We move forward.

[01:20] I think this is the most sustainable path forward. Gary says he's, quote, a deep believer in the rule of law.

[01:26] Does that mean he previously acted unlawfully? Really, though, this demonstrates the arbitrariness of the so-called rule of law.

[01:32] What Gary conflates to be the rule of law are merely opinions put forth by a small group of people. But that's a rabbit hole for another day.

[01:38] Let's continue. Why are Bitcoin ETFs important?

[01:41] Well, a report from Galaxy points out the key reasons. Greater reach for both retail and institutional investors.

[01:49] It's the big money and the nation states that are now chasing it. It's the retirement accounts, the pension funds, the 401ks, the IRAs and the Fortune 500 companies

[01:58] where we could see billions of dollars flowing into Bitcoin. 4.6 billion dollars.

[02:03] That was the amount of money that flowed into the long awaited Bitcoin ETFs on their very first day of trading last week.

[02:11] The new Bitcoin ETFs are meant to benefit Wall Street, which will collect management fees for doing very little.

[02:18] And even though Gary often spouts nonsense, he occasionally does drop some truth. There's an irony in the midst of this.

[02:25] Satoshi Nakamoto said this was going to be a decentralized system. And in finance, this has led to centralization.

[02:34] We benefit directly from this. Kraken provides the indice for six of the 11 spot Bitcoin ETFs that were approved.

[02:44] And 10 of those companies will outsource custody of the Bitcoin in their ETFs, most going with Coinbase.

[02:50] Will these Bitcoin ETFs grow acceptance of crypto? Some think so.

[02:54] CeFi, this intermediate step, is necessary. It's why companies like Coinbase and Kraken are so valuable.

[03:01] So if we think about that as this is an interim step for longer term full adoption. Our mission is to grow cryptocurrency adoption that can achieve this end goal of financial

[03:13] freedom. And, hey, this, you know, the introduction of ETFs is another access point for individuals to come into the space.

[03:21] But others disagree. Crypto's promise was a decentralized digital currency.

[03:26] Handing your money to BlackRock and Wall Street defeats the purpose of the asset class altogether. And if enough people give up the freedom Bitcoin offers,

[03:36] it will simply become the next asset class Wall Street completely owns and controls. Indeed, this control by Wall Street and the regime is likely the aim.

[03:46] If we look historically, we see that the powers that be try to co-opt any perceived threat, to then steer them, control them, and ultimately neuter them.

[03:54] In the United States, recent examples include the Occupy Wall Street and Tea Party movements, and going further back, the civil rights movement and the peace and isolation movements.

[04:03] Is that why Bitcoin is now being embraced by the regime? What better way to control this technology than to buddy up to it,

[04:09] while ignoring and targeting crypto networks that could actually offer real competition? Perhaps, I mean, it ceased being useful as peer-to-peer electronic cash years ago.

[04:18] Again, Gary, with some truth. Is it being used as a payment anywhere?

[04:23] Are we buying cups of coffee with it? Not really.

[04:26] Indeed, Bitcoin went from something that encouraged personal responsibility to now, with these Bitcoin ETFs being protected by SIPC insurance.

[04:35] In a worst case scenario, if a firm were committing fraud, and they were not actually purchasing the securities that you own,

[04:44] that's what the SIPC insurance would cover for you. Bitcoin ETFs are a long way removed from Bitcoin's disruptive roots as the first cryptocurrency.

[04:53] Oftentimes, with any endeavor, the first try doesn't succeed. How about we try again?

[04:58] How about we learn from Bitcoin's missteps? How about we bring to market a peer-to-peer electronic cash?

[05:05] Hey, everybody. How's it going?

[05:11] Welcome to Bitcoin Weekly. Sounds good to me.

[05:15] Let's bring this digital cash. Let's bring it.

[05:18] Right? I was just saying, I don't need to mess with private key management if I get SIPC insurance.

[05:24] Dang. I wonder what the cost comparison is.

[05:28] You know, I don't even want to go there, because I want to talk instead about a web wallet that supports digital cash.

[05:34] Are you here to talk to us about that, Jojo? Yes, I am.

[05:38] Well, without any further ado, should we hop right into your screen share? And by the way, everybody, this is our second update about this wallet.

[05:46] And yeah, we're pumped to see what you have for us. Jojo, is that all right?

[05:50] Can I pull that up? Sure.

[05:51] Great. Yeah, so in the Dash Incubator, we've been building this wallet

[06:00] from scratch using some tools that CoolAJ86 has built for the incubator, and maybe some other stuff that have been forked off and on here.

[06:10] But yeah, we've been building this. And it's two stage one.

[06:16] Oh, I should have brought this up, actually. Let me see if I can find this real quick, is the code base.

[06:23] Let's see. So this is all open source inside of the Dash, well, the Dash Hive channel.

[06:35] But we've got the wallet UI here. So this is open source.

[06:40] You can download it, run it yourself. But other than that, let's generate a wallet.

[06:48] There's a link to that repo on this URL that we're looking at right now as well, right? So if you scroll down to the bottom.

[06:56] Correct. Well, it's not showing yet.

[06:59] But once I get in here, so let's actually start and just generate a wallet. So I'm going to call this one Jojo.

[07:05] Okay. But I'm going to ask you to kind of slow down a bit

[07:09] and tell us what you're doing while you're doing it. Because you've done this probably 300 times.

[07:16] But most people are seeing this user interface for the first time. So yeah, just take your time.

[07:22] So what I just did on the left side here is click the generate new wallet. And this requires you to enter an alias.

[07:32] It's kind of like a username, but it's not enforced by any centralized server. It's enforced by your local wallet in your browser.

[07:39] And so you select an alias that you're identified for. And that will get shared with any contacts you make.

[07:47] And they'll store that alias for you in their wallet. Okay, so I'm making a new wallet.

[07:54] I'm giving myself a name that I want to be known by with contacts that I share my contact information with.

[08:03] And so a lot of the functionality for this wallet is more in line with being a Venmo alternative.

[08:16] So it's like sending money to a username type of thing. But because we're not centralizing the username process,

[08:24] there's nothing backing that up other than when you pair with a contact, you're saying, hey, this is what I want to be called type of thing.

[08:35] And that can be overridden in the pairing process. Okay, so this one on the left, I'm generating a new wallet.

[08:46] And I'm calling my alias. Oh, I clicked out.

[08:50] Let me start over. I'm calling my alias Jojo.

[08:53] I click next here. It generates a new phrase.

[08:57] So this is a recovery phrase or seed phrase that can be used with Dash Core Wallet or other wallets that are

[09:09] recovery phrase compatible, essentially. So once you've got that copied or printed out or whatever, you click back up.

[09:18] And then you have to get to this encryption phase. And with the encryption phase, this is a password for you.

[09:26] And your data inside your browser is encrypted using this. Beyond that, when you back up,

[09:35] the biggest feature from the last few days is we now have backup and recovery. And so your data will be encrypted with this right now.

[09:45] We may eventually have a feature where you can back it up without encryption. But right now, it's backed up and encrypted.

[09:55] So you need this password to restore your backed up data, essentially. Okay.

[10:00] So I'm just going to enter a short password there. And I'm going to click remember.

[10:06] If you don't click remember, it just asks you if you refresh to enter this encryption or decryption password again.

[10:15] I'm going to click encrypt. And that loads.

[10:18] And I've got a wallet here. Okay.

[10:22] I like the styling you've chosen. If I can just say that, Jojo.

[10:26] I like it's like clean and slick. I like it.

[10:30] And of course, I'm always a fan of dark mode as well. Yes, I am too.

[10:34] I can't take credit for the styling, though. A lot of this was done by Nick.

[10:40] I've adjusted some of the design to suit things we had missed in the planning process. But most of this styling is from the Figma designs

[10:54] that another designer had made for the project. Fair enough.

[11:00] And this is the source code link that Rion was talking about. So that is in the wallet.

[11:08] You should easily be able to find it once you've generated or imported a wallet. So we've got a wallet here.

[11:17] This is a new one. I've never used it before.

[11:21] It has no funds. I'm going to go ahead and import or add an existing wallet in this right one here.

[11:29] And so some of the new functionality we've got is you can use a key store. And these key stores should be compatible with Eldorado wallet or more specifically XChain.

[11:46] There's a framework or library called XChain that is used by, I believe, Eldorado and by Thor wallet and I'm sure many others.

[11:58] And they allow you to use a key store for your cryptocurrency. Now what do you mean it should be compatible with it?

[12:05] Like one could monitor one's liquidity balance or what do you mean? So if you've generated a wallet inside of Thor wallet or Eldorado.

[12:24] I don't think Maya itself handles this but some of the interfaces create key stores. And so if you've used a key store with that and sent Dash to it,

[12:34] you can actually load your key store here and check your funds without going into one of the Maya interfaces.

[12:41] But this will only show Dash right now. I got it.

[12:48] Or if you're one of the Maya people who isn't really in the Dash community and you have a wallet created by Eldorado,

[12:56] instead of creating a new one at that first screen that we did, you would just import your Eldorado key store.

[13:04] And that key store contains the seed phrase and the key pairs for all of the coins that you were doing with Eldorado.

[13:16] But the Dash wallet here would just show your Dash balance. Okay.

[13:21] Yes. So I've got this key store I've already generated.

[13:31] I'm going to import that. I'm going to call this wallet byte.

[13:34] I'm going to say add wallet and then I need to get the password in here. And this instead of usually this says encrypt for when you're generating one,

[13:46] but because this key store exists, it's decrypting the key store. It exists and it's already encrypted.

[13:53] That's why you have to decrypt it so the wallet can then interface with it, right? So actually the key store has a recovery phrase in it that is encrypted.

[14:06] So that is. But I did just a key store in this example.

[14:10] So it doesn't have any of the other encrypted data of what we just got where you can backup your wallet.

[14:18] Okay. So we do now have the ability and I suppose I should run through this is

[14:25] you can add contacts here and our backup wallet will backup all of your contacts. I believe all that addresses you've generated

[14:41] and several other things needed to run the web wallet. But I'm not going to do that yet.

[14:47] I'm going to pair these two wallets. So these are two different wallets.

[14:51] This is my local version here. It's at local host, but it's running on my computer.

[14:57] This is the live version. It is a static site we're hosting.

[15:01] Other than just serving plain HTML, JavaScript and CSS, there's no other background services there.

[15:12] It's just serving static files. And so we can go ahead and copy the URI here and paste it right there.

[15:20] And this begins the pairing process and we can do the same thing here. And actually, maybe I won't do it here yet.

[15:29] So I'm going to click add. And one of the things I believe we've added since the last stream

[15:35] was if you had clicked out of here, there was no way to finish this pairing. But now if, say, Jojo here, so this wallet on the left,

[15:47] forgot to send their pairing code, you can actually go in and get your pairing code. Oh, not there.

[15:56] Where is it? So right here, you can click on that and you can get this URI that you need to share.

[16:03] And so you can actually finish the pairing with the other person. I'm going to add a name here and say add contact.

[16:10] So now I have both of these wallets paired together. And I can send funds between them.

[16:18] So there is a small amount of funds. I guess it is in the gray in this wallet.

[16:22] But I could send some funds from this one to this new account and say 0.1. And does it send to the same address every time or it creates a new address every time?

[16:38] No, it should increment the address every time. So it's like the HD type stuff.

[16:44] Actually, that should have updated. There we go.

[16:49] Yeah, it's an HD wallet under the hood. So that's and that's, you know, it'd be relatively simple to do this

[16:57] if you were just coding one address behind this username. But it's actually exchanging Xpub keys.

[17:04] And each wallet's generating new addresses for each subsequent transaction, just like you would expect or hopefully expect at this point.

[17:15] So Jojobyte, I have a web wallet on my side of things right now. Do you want to, can I pair with you to send you some funds so that you have more,

[17:31] so you have some digits in the white instead of gray? Yeah, sure.

[17:39] Okay, so how would we go about that process? So the other edge of the universe and I want to pair with you.

[17:47] If you've got this link pulled up, the backup restore wallet, I can share that again if you don't have it.

[17:53] I do, I do. And I've logged into my wallet already.

[17:56] Okay, I have not paired any contacts. So I'm basically working fresh here.

[18:02] Okay, so I will share this URI in the chat here with you. And you'll pick the URI that I just shared and paste that into your wallet.

[18:12] Okay, and you need to share your URI with me. So you've just copied some text.

[18:18] I'm copying it and then I'm going into my web wallet and I'm going new contact. I'm clicking new contact and then I'm pasting that in.

[18:32] And it brings in your preferred alias, Jojo. And I can put Jojo in my, as the contact name if I want to do anything other than your alias.

[18:44] And then I click add contact. And now I see you as a contact for me.

[18:51] So I'm just going to click your username and then hit send. And I'm going to enter, let's say, 0.01- and I'm clicking send.

[19:03] And then I confirm. So hopefully that will come over to your side momentarily.

[19:11] Yeah, so that should come in here. But I haven't finished pairing with Rion's.

[19:16] So I need to give you my pairing. I should be able to see those funds regardless.

[19:25] Yeah, so look at that. I'm actually not sure why they didn't.

[19:29] There was not a fee deduction there, or am I wrong? Tell me about the fees.

[19:33] The fees are extremely minimal. But there are fees we're sending on the Dash network.

[19:46] So there are fees. But KoolAJ86 had done a lot of work to optimize what he could.

[19:55] And a lot of it, if I recall correctly, I think Rion's probably watched more of his streams on Dash than I have.

[20:02] But he investigated how things were being done. I like that Rion sent 0.01 and you received 0.01 instead of 0.009.

[20:15] I'm just wondering why. Yeah, so it added it on.

[20:20] Yes, that's automatically subtracted from whatever wallet he's using. Okay.

[20:28] Okay, now, Jojobite, can you tell me where do I go to help share my information with you so that we can do this pairing?

[20:39] Inside your wallet, you would click the Jojo contact. Okay.

[20:44] You would click the avatar little icon here. Okay.

[20:49] And that should show you the pairing information. Copy URI, and then I'm sharing that with you over StreamYard.

[20:57] Okay, go ahead and you should see it now. All right.

[21:04] Okay, so now I can finish this pairing. Pasting his in there.

[21:12] And it's got a getKeyStore alias. I'm going to actually call this Rion though.

[21:20] Yep. I'm going to add contact.

[21:24] So now I've got his finished pairing. And we've already received funds from him.

[21:31] So we've got a little bit more in this brighter text area. Okay.

[21:39] And so I could send funds back to him as well. I could go here and click send, but you can also do it from these buttons.

[21:46] You can just select the contact here. So I could, let's do 0.005.

[21:56] Let's do that. Sure.

[21:58] It should leave us some still in the white area. Okay.

[22:06] There we go. So it's deducted and I'm not sure what my balance was before,

[22:12] but I think it's probably, yeah, updated. So, okay.

[22:19] So why this wallet? We have Dash wallets.

[22:22] Why this wallet, Rion? So yeah, we have Dash wallets.

[22:29] We have a mobile wallet, either on iOS or Android. And we have a desktop wallet, or at least, yeah.

[22:39] Speaking of DCGs wallets, they create a mobile wallet and a desktop wallet, but we don't have a web wallet.

[22:46] We did have, I think we did have a web wallet at one point, but that's no longer maintained.

[22:52] And I don't know what, I was never a user of that wallet. I just heard that we had a web wallet at some point.

[22:58] But the purpose here is to, for one, you know, have a web wallet for anybody who prefers web wallets,

[23:07] for one, just as a matter of giving people choice. But also, there's one aspect of decentralization

[23:16] that you can only achieve through a web wallet. If in the worst case scenario,

[23:22] Apple decided to remove wallets from their app store, cryptocurrency wallets, you would, I personally would not be able to access my mobile wallet,

[23:35] because they would just, it wouldn't be around. - And that's not an inconceivable scenario at all.

[23:41] Or even if they didn't do something as broad as like, "Hey, all crypto's out the door," they could just say, "Dash is out the door."

[23:48] - Yeah, and I don't think that's a very likely case, but it is a case nonetheless.

[23:52] And I don't necessarily, I don't want Apple being in control of whether I can use digital cash or not.

[24:00] Now, Android's a little bit better. There's also, you know, Google controls Android for the most part,

[24:05] but there are alternative app stores that you can use for Google phones, Android phones. So that's nice, but there's nothing more decentralized than the web platform itself.

[24:15] Nobody can stop me from just hosting my own web wallet. And if I wanted to use somebody else's as a different provider,

[24:29] because I just want convenience. And if that provider gets shut down,

[24:33] then somebody else can just take the open source code and run that hosted wallet, hosted UI themselves.

[24:41] And so I could just switch providers very easily. That's a game of whack-a-mole that nobody could ever beat

[24:49] by shutting down every, you know, web address that deals with cryptocurrency. It's just a losing battle.

[24:56] So that would never happen. So in terms of decentralization, it's a little bit of a bonus there.

[25:01] But primarily, I want this wallet to be very up to speed on all of the integrations. So if we have, let's say, BitRefill,

[25:13] we want to integrate BitRefill right into the wallet using their API so that I can buy gift cards with Dash.

[25:22] Then, you know, we can just integrate them really quickly. If some other provider comes around, we can integrate that really quickly.

[25:31] We can integrate Crowdnode. We can integrate Maya.

[25:36] So we can do all these integrations in a way that is quick and multiple people can work on because it's just the web platform

[25:45] that there are millions and millions of developers available to us. So right now, it's been a slow start, relatively speaking.

[25:56] But now that we've got some of the preliminary security and base functionality out of the way, such as encryption and just the key generation and everything like that,

[26:07] the integration should be relatively straightforward from here on out because it's mostly just, OK, what's the API?

[26:15] And we just slap a user interface on there and just build that out pretty quickly. OK, so then do you want to talk about, like, in terms of when integrations,

[26:27] do you want to talk about the roadmap next? Or do you want to delve more into, like, the code base type stuff

[26:32] of what you said is now finally out of the way, like the encryption stuff and the whatever other stuff you said I forgot?

[26:39] Yeah, well, Jojo and I need to do a little bit of re-roadmapping just now that we've got this key functionality out of the way.

[26:49] I need to see, and community, just give us your input. Like, what do you want next?

[26:55] My plan is to do Crowdnode and Maya savers. Probably Crowdnode first because that's the most attractive, I think, use case.

[27:10] We've already built a Crowdnode CLI and SDK. And can they be used for this?

[27:20] Like, those can just... Very simply, we've already even built a UI for it.

[27:25] So Jojobite has done a separate UI for Crowdnode. We just need to pull that and put it into the web wallet.

[27:32] So that should be pretty straightforward. That's probably my priority right now.

[27:36] And then when Maya savers comes out, that would be another very easy, clear win because we've already dealt with Maya.

[27:46] We have a user interface for Maya already. It's a separate thing as well right now.

[27:50] But just bring that into the web wallet as well. And then the next one after that would probably be the best gift card API that we can find.

[28:02] And I think that would probably be Bitrefill right now. But I know that Ash has something in the works as well at some point.

[28:11] But whenever that comes, we would add that as well, provided that they have an API. So in my screen share here, I've got the code pulled up and I can show the roadmap here.

[28:25] So this was our original roadmap and we are reaching the end of stage one. So we've got stage one here.

[28:33] - Can you zoom in just a little bit? - Yeah, I tried.

[28:37] - Yeah, there you go. - Is that good?

[28:40] - One more. - For some reason, this is not going.

[28:44] - Yeah, that's okay. So that's why it is like, yeah, all right.

[28:51] Let's see if that's enough. - It's bigger text anyway.

[28:53] - Yeah, all right. So our roadmap, we had it sectioned up into stage one through five.

[29:02] And each stage got a little more loose and up in the air. So stage one was, these are the core features we need.

[29:13] This is our MVP essentially, minimum viable product. So stage one is MVP.

[29:19] And with the backup features that we've just got added over the last few days, it is reaching the end.

[29:27] The only reason this isn't checked off is because I want to tweak the backup dialogue a little bit. But once that's done, we've completed stage one.

[29:37] We need to do some bug like testing and stuff like that. But other than that, we should be good to move on to stage two.

[29:46] However, that's where Rion is saying we should, he and I and anyone else involved in the community that's interested in this

[29:55] should voice their opinions of what is higher priority. So a lot of this was done, for example,

[30:05] I don't think Maya was released with Dash when we were planning this. - Right.

[30:11] - So I think we knew it was a possibility, but when it was up in the air, there was no sense saying,

[30:18] this is going to be our next feature. But now that it's released and we can integrate it and we've done testing with it,

[30:26] and we know how to integrate, that might be higher priority. It might very well be the next thing we do.

[30:33] And so that's where Rion and I probably need to reorder this to move things around to like, what should be stage two?

[30:43] Should stage two be this long? Should we try and shorten it to just a couple of things?

[30:47] Should we, you know, there's a lot here that can be done. But all in all, stage one was the biggest stage

[30:57] just because we had to get all of the core groundwork done. And, you know, the foundation laid for the rest of it.

[31:06] And to your point, Rion, the advantage to doing this as a web wallet is people don't, sorry, not people.

[31:19] We don't need to submit this to an app store to get it approved. If we want to integrate with, and I think we had it down here somewhere.

[31:28] So if we want to integrate with Crowdnode, if we want to integrate with Maya, I thought we had, oh, there we go.

[31:34] BitRefill, DashDirect, sorry, rest in peace. That proves how long this has been planned is DashDirect is still on there.

[31:44] That makes me sad. But if we want to integrate with any of these,

[31:49] we don't need to submit it for approval to an app store. We can also do that integration.

[31:54] - Exactly. And also, I don't know if it's on there or not, but CoinJoin,

[31:59] we do want to support as well. So we'll need to put that somewhere in the web wallet,

[32:04] but we need to figure out the CoinJoin. We got, I think, like seven eighths of the way

[32:11] through the CoinJoin protocol using JavaScript on the backend. And so we need to finish that 'cause it wasn't documented,

[32:21] but now that we have, so we had to figure out what the CoinJoin protocol was at very low level,

[32:28] just using bits and bytes and things like that. And it was a lot of work.

[32:33] But now that we have the Python implementation in the Electrum done, we can use that to see,

[32:43] okay, what was that last little bit that we weren't quite getting to finish that CoinJoin protocol?

[32:49] And then we'll integrate that as well. And we can also look then at the mobile wallets

[33:00] that DCG is putting out to see what that implementation is, 'cause it's a little tricky looking at just the C++ code.

[33:07] So anyway, that's on the roadmap as well, but we need to put it in a certain place.

[33:12] So Jojobite, can we continue with the demo and just show a little bit of like the backup features

[33:19] and clearing or just connecting the wallet just so that we have more or less a whole demo complete?

[33:30] - Yeah, yep. So I'm going to backup this wallet first.

[33:35] - And what does that mean? - It will backup all the data that is stored in the browser.

[33:45] So right now, if you clear your browser, and I'm using private browser tab.

[33:52] So if I just close this, everything in here is gone. If I didn't backup that recovery phrase,

[33:58] it's really, really gone. Like we're not storing that.

[34:02] There ain't no backups for you. This is not being sent to our server.

[34:05] - It's all client side. - Yeah, it's all client side.

[34:08] It's all happening on your side and your browser. So there is no backup on some server

[34:16] that we can get for you. - Yeah, we don't even have a server.

[34:19] The only thing our server does in this case is serves a static webpage.

[34:22] You're not, this is not a backend, front end kind of application.

[34:26] This is a static webpage that you only interface with on the client side for all the security related things.

[34:33] That's why it's secure. - Correct, yep.

[34:37] So backing up entails grabbing all of that data and putting it into a JSON file.

[34:46] And then you're able to import it. Actually, let me show locking first.

[34:53] So I can now lock the wallet and that just puts us into a state

[34:59] where it no longer has the encryption password. And if you refresh, it won't log back in.

[35:06] So I refresh, you can probably tell, but there's no encryption password.

[35:11] So until I enter that again, you can't get access to the information

[35:18] the wallet needs to run. So that's what lock does.

[35:22] Disconnect would clear it, but let's back it up first before we do that.

[35:26] So I'm gonna click back up here. Backup now shows the recovery phrase.

[35:32] Let's see here. - So this is presuming that you hadn't written it down

[35:38] the first time it showed it? - Correct.

[35:40] - And all of this stuff can be tweaked. Like for example, it might be nice

[35:48] to hide those words by default and then have a little show button or something,

[35:53] but those are just finer details that we can always add later.

[35:56] - Yeah, so that dialogue was slightly updated from the one over here.

[36:02] So this one still says new wallet, for example, and this one actually shows backup wallet.

[36:11] And this is part of why I haven't completed it is instead of showing this,

[36:16] I think you should have to reenter. Even if it's stored temporarily in the browser,

[36:22] I think you should have to reenter your decryption password to see the recovery phrase.

[36:27] At least that's where I stand. Maybe Rion disagrees.

[36:31] - Yeah, we'll talk about it later. - Yeah, this should show a couple different buttons

[36:37] and that's what I'm planning to do that I wasn't able to get done before this presentation,

[36:42] but it should show a backup key store so you can get just the key store.

[36:48] It will do a full backup. So all the data that file just downloaded does,

[36:53] and then it should also do the show key phrase, I think, or show recovery phrase.

[37:02] But that's interface elements that I just still need to update.

[37:07] - Does that back up your contacts as well? - Yes, the backup right now backs up your contacts,

[37:15] the full wallet backup. So I can go ahead and disconnect this wallet

[37:19] and actually I'll do this. These are two different browsers.

[37:23] I think this one is the nightly version and this one is the normal version of Brave.

[37:29] So they're completely different browsers. If I disconnect them, I can come into add existing here

[37:36] and I can select and go here. - You selected backup there, not the...

[37:45] - Key phrase, key store. - This is actually one giant button.

[37:50] So it doesn't matter which one you click actually. It's just opening the same dialogue.

[37:55] - But the key thing here is now you're actually selecting a file that was a backup file, not a key store file.

[38:02] And it figures out, oh, this is a backup file. - And so it prefilled my alias, for example.

[38:08] This was Jojo and this one was Byte before. And so it figured out my alias.

[38:16] And if I click add, it's telling me to decrypt it. So I enter the password there.

[38:22] If I decrypt, now I've got the contacts that the left wallet had

[38:27] and I've got the balance of that wallet. - Okay.

[38:30] - So those are the most recent features we've added is this backup lock and disconnect.

[38:39] - So you could, presumably, like if you really wanted to, you could walk around with a USB stick.

[38:48] You could go to the public library. You could plug your USB stick in

[38:51] and deal with your wallet stuff there and then clear the wallet from there

[39:00] without any kind of security holes. It would be secure way to do that.

[39:06] Presumably, I don't know. We can talk about it.

[39:09] But- - That would be nice. - You could do that.

[39:13] Like you could have your wallet on a USB stick, has all your contacts,

[39:17] hop a border or something like that. And you've got a wallet that's got all your stuff.

[39:24] - Theoretically, yes. I don't know if I would do that, but yes.

[39:27] - Yeah, I'm not suggesting it's 100% secure to do this at a public library.

[39:33] I'm just saying in terms of functionality and in terms of the encryption and everything

[39:38] and the fact that this is client side browser stuff, in theory, we could make it work and securely.

[39:45] - Yeah, yep. - Well, I think that anything that takes us more

[39:49] in the direction of not needing special hardware to feel at least pretty reasonably secure is great.

[39:57] Especially since Trezor lost their minds and decided that Dash is not an actual coin,

[40:03] quote unquote. And that actually reminds me,

[40:07] since you both said that you were seeking community input as far as what happens to the wallet next.

[40:14] I mean, obviously we've seen on the roadmap, you have the crowd node, the gift cards, the Maya,

[40:23] that's all cool, that's all righteous. And I just wonder if this would be an appropriate time

[40:28] for me to bring up something I've brought up before. And it seems almost crazy to me

[40:34] that we don't have this in the ecosystem right now. Because the benefits to me of multi-sig

[40:41] are at least twofold. The first fold being,

[40:46] it helps less than perfectly tech savvy people to be able to hold their private keys.

[40:54] As I brought up on the show before, there is someone who is close to me

[40:58] who was trying to hold his own Dash. He misplaced the private keys.

[41:04] And I feel at least partially responsible for that because I was the one who set him up with his wallet.

[41:10] And at the time I thought, "Dang, it would be nice if I

[41:16] and maybe another family member were able to hold like a two of three

[41:20] on this individual's funds so that if he misplaces his stuff,

[41:23] we can recover it for him." But we didn't and his funds are gone.

[41:26] And then the second fold benefit of multi-sig that I can see is protection against

[41:33] a $5 wrench attack, right? Because if someone is holding their,

[41:40] trying to hold their own private keys, you know, not being like,

[41:42] "Oh, you keep it Coinbase. You keep it Kraken."

[41:45] Then what is to protect them from the $5 wrench attack

[41:50] if not knowing that other people need to also be $5 wrench attacked

[41:55] at the same time to take their funds? - Okay, so a couple of things

[42:00] I would say about this. The first scenario that you mentioned,

[42:03] I would say the best way to handle that is for you to have kept a backup

[42:09] of the 12 word phrase. That's not necessarily a multi-sig scenario

[42:14] where you would need multi-sig to help protect a trusted individual

[42:20] that you both trust each other and you just think that maybe

[42:25] he will lose his keys. The best case scenario for that

[42:28] is to just use your, you keep a backup of the 12 word keys.

[42:32] If he trusts that you're not going to take his money,

[42:34] you're the one that presumably gave it to him. The second thing is

[42:38] the $5 wrench attack thing. You know, you kind of have to think about this

[42:43] in terms of cash as well. How many of us are getting $5 wrench attacked

[42:47] with cash right now? And if you are--

[42:51] - What is the $5 wrench attack? I haven't heard of this.

[42:55] - That's when I come to you and I say, "Give me your money,

[42:58] "give me your seed phrase right now "or else I'm going to hit you

[43:01] "over the head with this wrench." - Okay, yeah.

[43:05] - So it basically, it's just, you know, somebody attacks me because they know.

[43:10] And the risk is elevated in cryptocurrency because somebody, if I go to a merchant

[43:16] and I spend some money and they can see that I just spent from,

[43:20] you know, they've got a little widget on their computer that just basically

[43:24] pull up a block explorer and see that the transaction

[43:29] that I just got funded with for the coffee, me, the merchant,

[43:32] I can see that that came from an address that had 1000 Dash.

[43:36] You know, I'm just breaking up my masternode, I'm buying coffee for the first time.

[43:40] You know, they might say, "Oh, can you come over here?

[43:46] "I need to look at something "and take you to the back alley

[43:48] "and say, okay, give me that wallet right now." And they wouldn't be able to necessarily do that

[43:53] if they saw that you just had $20 in your wallet. Like they wouldn't do that.

[43:58] That's just a dumb thing to do. But if you had $3,000 or $30,000,

[44:04] then it becomes more likely. - I don't think that that's the only scenario though,

[44:10] where someone like just so happens to look back in the block explorer

[44:15] and, "Oh, this person who randomly came in today "actually has some funds."

[44:21] I'm thinking more about stories where just well-known crypto people

[44:25] who are suspected of having fat stacks because of their position in life, what they do,

[44:32] that those people have been targeted not as a matter of happenstance by a cashier,

[44:39] but as a matter of planning by someone who puts effort into targeting this person.

[44:47] - Sure. Again, I think it's a little bit...

[44:50] I do always try to be security oriented, but I think it has to be put in the proper context.

[44:57] Like you can know when somebody's fiat wealthy as well and how many wrench attacks are happening.

[45:03] So you might need to-- - But that's because their money's in a bank.

[45:07] That's because their money's in a bank. - This is true.

[45:11] This is true. So you're talking about self-custody

[45:14] is the distinguishing factor here, not necessarily crypto versus fiat,

[45:20] but the fact that it's self-custody. And most fiat people aren't walking around

[45:24] with their whole bank account in their possession. But again, I would say,

[45:31] you need to make sure that your security practices are such that you are also not walking around

[45:38] with tons of crypto wealth in your personal custody at any time.

[45:45] I don't wanna go down too far. We're getting a little bit into the security land

[45:51] and that's a deep rabbit hole. But I would say that the overall message is

[45:57] you have to practice the same kind of security that you do in the normal world.

[46:02] And sometimes that means you don't have... You only keep what you're comfortable with

[46:07] on your person at any time. And you keep the rest of your wealth somewhere

[46:12] that's like you said, like multi-sig and whatnot. But I don't know if this web wallet

[46:18] is trying to achieve that. It's more trying to achieve convenience

[46:25] for spending in online settings. And yeah, anything to add to that Jojo bite

[46:37] in terms of... Yeah, I don't want people walking around

[46:43] with $30,000 on the web wallet right away. I don't even want people walking around

[46:49] with $1,000 on the web wallet right away. - I fully agree.

[46:55] - It's just right now it's not the time to be thinking about those things.

[46:59] Right now it's time to focus on cool features with some base level of security,

[47:06] which we already have done with the encryption, I think. After that, if we're a year down the road,

[47:14] then we can start thinking about multi-sig and some of these higher level security features.

[47:20] But I'm not sure if those will ever be a web wallet focus.

[47:25] Does that help Amanda? - Yeah.

[47:27] - Okay. - As far as where I land on that,

[47:35] I would agree this is still definitely alpha stage software.

[47:41] Even as we reach stage one, this is where we need to do some bug testing.

[47:46] It might be a beta stage at some point soon, but until all the bugs that we can find are flushed out,

[47:54] I would not say this is a stick $1,000 worth of dash in this. But even then, I would generally use this in scenarios

[48:04] with probably less than a thousand. Like maybe I'd use up to a hundred dollars,

[48:10] but like I personally am not doing things on a day-to-day basis where I need more than probably,

[48:17] you know, 50 to a hundred dollars of dash. So I would use this in scenarios where it's like,

[48:22] oh, I'm going out to lunch with some friends. I might need some funds.

[48:26] I'll send a little bit more to my web wallet so that it's in there if I wanna pay them back type of thing.

[48:32] But eventually we do have some features that would be more like savings.

[48:38] Like if we're doing the crowd node or Maya stuff, and you're using this to store those,

[48:46] well, you're not, that's the reality. You're not really storing funds in this.

[48:51] It's all attached to your recovery phrase. So you can do these interactions with crowd node or Maya,

[48:58] and it's not stored in this wallet. As long as your browser's cleared, you're fine.

[49:04] But I would never use this in a scenario where it's got, you know,

[49:13] you're walking around with your cell phone in your pocket connected to your recovery phrase

[49:19] that has, you know, an entire master nodes worth of dash on it.

[49:23] Like that's, yeah, that's irresponsible. In the same way, I would never walk around

[49:29] with $30,000 in my pocket unless I'm going to buy a car or something

[49:34] and know I'm going to spend it immediately type of thing. Like that's just irresponsible.

[49:40] - Okay. Did we finish the feature set of the wallet

[49:45] or do we still have some things to demo? - No, I believe we demoed everything here.

[49:50] - Okay. Do you want to look at the code?

[49:53] Let's maybe look, take a brief look at the code base. Just, I want people to get an idea of, you know,

[49:59] what this looks like under the hood for those that are interested

[50:02] 'cause this is the incubator after all, and we're always welcoming contributions.

[50:06] So this is just as you're getting stuff ready. This is a pure JavaScript, CSS, HTML wallet,

[50:15] no frameworks involved here. And that's not very common.

[50:20] Most people, when they're developing something, especially an app that has user interactions,

[50:28] they're almost always using some kind of a user interface framework,

[50:33] like React or Vue or Angular or Solid or Svelte, or, you know, all of these different frameworks.

[50:39] There's a huge industry behind this, but we've decided to go with just pure HTML, essentially.

[50:46] And how does this look? - So these are the, this is the package.json.

[50:53] We've got a dev dependency just for some types, and these are the actual dependencies.

[50:58] A couple of these actually need to be removed. I don't think we're using IDB right now,

[51:04] but regardless, most of these, for example, all of these dash ones, this cryptic storage,

[51:12] and these ones were all built within the incubator. - So let's highlight the ones that are not built

[51:18] by the incubator itself, 'cause I think that's a smaller list.

[51:21] - Mm-hmm. So this is a QR code scanning library,

[51:27] which is used in the request side of it, but because we're not in person,

[51:33] it's not as useful. So we didn't demonstrate that.

[51:36] And I believe we demonstrated it last time. - Okay.

[51:39] - There's also the HTML5 QR code, which is used for generating.

[51:44] So this one is a reading library. This one is a generating library.

[51:48] And actually, that is also connected to the QR codes. So those are just QR code related.

[51:55] And then local forage is used for storing data. - Okay, and that's the only external dependency.

[52:02] So Shenmake is saying, "What's the bundle size?" That's a great, great question.

[52:06] - We don't bundle. - We do not bundle.

[52:09] - Vanilla. - This is shipped without bundling,

[52:13] without a bundling process. You just ship the HTML file.

[52:17] The HTML file gets read by your browser, and then it sends requests for these other libraries.

[52:22] Correct me if I'm wrong on any of this. So it's making requests to get all these dependent,

[52:28] these runtime dependencies without any kind of bundle. But if there was a bundle,

[52:33] I think the question still is valid. What is the overall size

[52:38] that you're loading into the browser is definitely a valid question because...

[52:43] - I definitely think it's valid, but I don't know. - Well, I would say just based on...

[52:50] - Smaller than dash SDK. - Yes, my guess is that it's in the hundreds of kilobytes

[52:58] rather than in the single digits or even tens of megabytes, which would be if we had used existing tools

[53:09] like the dash SDK. And that is why we've spent so much time

[53:14] building some of these things from scratch because I'm not going to ask my users

[53:21] to wait tens of seconds and download megabytes of data just to load a wallet.

[53:30] So as far as roadmapping goes as well, do we plan on adding dash platform support to this

[53:38] to this bundle of or suite of tools? Yes, we do.

[53:43] And I don't know the extent or timeline that we will do that.

[53:50] Obviously, we have to wait for it to get to mainnet first. Let's see, 64 requests, 115 bytes transferred,

[53:59] 1.1 megabyte resource finished in 295 milliseconds. So this thing loads in 0.3 seconds is what that's saying.

[54:08] Less than 0.3 seconds, this thing is up and rocking. I think that's a huge win.

[54:14] - Yeah. I actually...

[54:19] So some of the encryption stuff, I think actually slowed things down

[54:23] and I would like to improve that. It's not exactly high priority for me right now

[54:28] because apparently it's still fast, but it's added a noticeable delay to me

[54:33] and I dislike that. So I would prefer to have things set up in a way

[54:37] where it doesn't feel like there's a delay using the interface at all.

[54:41] But yeah, again, it's not high priority fix right now because it's so pretty dang fast.

[54:47] - Right. And just to wrap up with that,

[54:50] just to wrap up with that thought that I had about the platform integration.

[54:53] Websites, they need... Websites need a database on the backend

[54:59] in many, many cases. And that the whole thing with Dash Platform

[55:03] is can we give web developers an easy to use database as a service

[55:11] where you pay using Dash and then you get to store data on the Dash Platform

[55:19] instead of going through the whole mess of setting up a server

[55:23] and then having the server connect to a database. And it is pretty typical development work,

[55:29] but it would be really sweet if we could really offer a very slick user

[55:36] or developer experience where developers that maybe are only familiar

[55:42] with HTML, CSS and JavaScript, they can now have a full stack application

[55:49] using Dash Platform on the backend and then have their website,

[55:54] their web app to be a simple static HTML page just like our wallet is.

[56:00] But you can then also store data on the backend, meaning Dash Platform.

[56:05] So if we can get that user experience for developers and users really dialed in,

[56:12] I think that there is... And the cost's relatively low.

[56:17] I think that there's a good use case for Platform,

[56:20] but we need to build that in a way that is friendly to developers

[56:28] and not bloated in package size. So I'm hoping to look into that.

[56:32] How can we use our tools or build some additional tools

[56:37] to contact and store and retrieve data from Dash Platform in a much lighter weight way

[56:45] than we have with the Dash SDK? That's something I'm gonna be looking into.

[56:49] Okay. So final question from me then is,

[56:52] how does this web wallet compare to another web wallet

[56:58] that is also currently being funded from the treasury,

[57:01] which is viewable@dashmoney.io? I don't know if you're familiar with that, Jojo.

[57:07] I've just put the URL in our private chat. But yeah, is this guy doing something similar

[57:15] to what we're doing? Is this guy doing something totally different?

[57:17] Tell me about that. He's doing something very different.

[57:21] He's building applications that are primarily focused on using Dash Platform.

[57:28] And so he's dealing with using Testnet, Dash Platform on Testnet right now.

[57:35] And he's using that Dash SDK, which I just talked about.

[57:41] He's using the Dash SDK primarily for the Dash Platform features,

[57:48] not necessarily for... Part of what he's using the Dash SDK for

[57:54] is creating 12 word seed phrases. And yeah, like basically that.

[58:04] But that's... So there is overlap there with what we're doing.

[58:09] But that's, I think, the only non-platform feature

[58:14] that he's really using. I don't think any of his products

[58:18] are sending Dash on layer one to different people.

[58:23] He's trying to get platform credit transfers and things like that

[58:29] and storing data on Dash Platform. So mostly not overlapping efforts there.

[58:37] But yeah, like if you... If Shenmick wants to kind of analyze this

[58:45] the same way that he analyzed our web app, it would be interesting to see

[58:50] what the results would be. I haven't looked at it very much in detail,

[58:55] but I would guess that it's pretty slow load time. I mean, that developer's fault.

[59:02] - Just with DevTools, it has a lot of API requests,

[59:09] it looks like for Testnet. And then it also says 14.9 megabytes transferred.

[59:16] And actually, as I was reading that, it updated to 15.5.

[59:19] So it did something without me interacting with it. So it's transmitting a lot more data

[59:26] than ours is beyond. And it's also minified as far as I can tell.

[59:33] So one of the things we had mentioned was we're not bundling this at all.

[59:39] So that means no minification. That 1.1 is not being optimized

[59:46] from a bundle perspective. So we could probably drop that 1.1 down

[59:53] to my guess is under 500 kilobytes, probably even more just with minification.

[59:59] But we're trying to be as open and transparent as possible with the code.

[60:04] And that's why we're not bundling it right now. - Okay.

[60:08] Well, thanks for those overviews. I have clicked through that whole website,

[60:13] incidentally, through the dashmoney.io. And yeah, whether it's platform related

[60:17] or website related, I don't know. But yes, you're right.

[60:20] The load times are considerable. Okay, well, thanks for that.

[60:25] Does anybody, without any final comments, I think that closes us up for this week.

[60:30] - No, I think the only final comment would be that I would like to have another update

[60:37] on the web wallet, maybe a month or so from now. And depending on scheduling and whatnot,

[60:44] I think we could get some of these integrations that we've talked about, knocked out.

[60:48] - For sure, yeah. - That'd be righteous.

[60:52] All right, thanks for joining us, everyone. We'll see you next week.

[60:54] Bye. - See you, everyone.

[60:55] - Bye. - See you.