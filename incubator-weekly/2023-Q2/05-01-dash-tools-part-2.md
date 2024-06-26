---
showLink: "https://www.youtube.com/watch?v=KoJEC6VEO1I"
slug: "dash-tools-part-2"
title: "Dash Tools #2: “DashKeys” for WIFs + Pay Addresses"
publishDate: "2023-05-01"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/KoJEC6VEO1I/maxresdefault.webp"
---

Coinbase's lawsuit for regulatory clarity could result in winners and losers, but borderless crypto needs new decentralized markets to thrive.

## Episode Summary

tl;dr: Coinbase's lawsuit demanding regulatory clarity from the SEC could result in some crypto projects being favored over others in the US. However, crypto's borderless nature means that regulatory decisions in siloed legacy markets may not ultimately determine winners and losers. What's needed are new, decentralized markets that transcend borders and allow unrestricted global participation. The crypto revolution is incompatible with the old financial system, so the focus should be on building these new markets.

## Chapters

00:00 - Introduction: Coinbase's Lawsuit and the Potential Impact of Regulatory Clarity 
The episode begins by discussing Coinbase's lawsuit against the SEC demanding regulatory clarity, and how such clarity could favor some crypto projects while penalizing others in the US market.

04:34 - The Limitations of Regulatory Clarity in Siloed Markets
It's pointed out that crypto is inherently borderless, so trying to fit it into the frameworks of many different siloed markets is problematic. Regulatory decisions in any single market may not determine ultimate winners and losers.

06:58 - The Need for New, Decentralized Markets that Transcend Borders
What's really needed are new markets that allow unrestricted global participation, have no limits on trading, provide full user custody of funds, and are resilient against takedown attempts. Decentralization is the goal.

14:10 - Co-Host Introductions and Episode Overview
The co-hosts are introduced and they provide an overview of the Dash development libraries that will be covered, starting with Dash Keys. 

26:53 - Hierarchical Deterministic (HD) vs Non-HD Wallets
The co-hosts discuss the benefits of hierarchical deterministic wallets over non-HD wallets in terms of easier, more reliable backups and funding. Non-HD wallets are considered obsolete.

43:44 - The Need for Lightweight, Browser-Compatible JavaScript Libraries 
It's emphasized that the Dash libraries being developed are written in pure JavaScript for browser compatibility, improved auditability, and significant reductions in code size vs. older Node.js based libraries.

## Transcript

[00:00] With Coinbase's newly-filed lawsuit demanding regulatory clarity from the US SEC, many are breathing a sigh of relief, welcoming the potential for such clarity with open arms.
[00:14] It's been rightly pointed out, however, that such clarity would likely end up giving preference to some projects and penalizing others.
[00:23] But you may be thinking, "Hey, I don't really care if the US government picks winners and losers in the crypto space, because at least there would be winners.
[00:33] Regulatory clarity would make it easier for me to pick who those winners might be and ideally make some profit."
[00:40] This viewpoint is a rational and reasonable one to take, yes? Well, it is unless it overestimates the importance of any single market in this world.
[00:51] In this case, could it overestimate the importance of the US market? Let's conduct a thought experiment.
[00:58] Suppose that various US federal agencies miraculously stop fighting each other and do, in fact, make unanimous declarations as to which cryptos have the green light and which ones have the
[01:11] red. You're thrilled, because now you can buy greenlit tokens knowing that they shouldn't
[01:17] face any lawsuits or discriminatory regulations in the future. And concurrently, you can confidently sell any redlit tokens you were unfortunate enough
[01:27] to own. And now you're all set for a bright future, right?
[01:32] Well, what if similar regulatory clarity emerges in the Chinese market, but their winners and losers are different from the ones in the US?
[01:42] And what about India? Brazil?
[01:46] Korea? What if the tokens you stocked up on last week, due to regulatory clarity in the US,
[01:53] become banned, actually banned, in several other markets which, combined, are larger than the US one?
[02:01] You can begin to see how creating any kind of crypto strategy based on the green or red lights issued by the siloed legacy markets would actually be quite difficult.
[02:12] Crypto's single most prominent feature is borderlessness, meaning that the blockchain goes wherever the internet goes.
[02:21] Trying to fit an inherently borderless tool into dozens or hundreds of different silos is not so different from trying to fit a square peg into a round hole.
[02:33] So what, do we want regulatory clarity or don't we? The answer to this question has likely been simmering just below the surface of the entire
[02:42] crypto industry for years. We don't want regulatory confusion nor clarity in the existing markets so much as we want
[02:52] entirely new markets. We want markets where buyers and sellers are able to participate regardless of where they
[02:58] were born. We want markets where there are no limits to the volume or frequency of our trades.
[03:05] We want markets where our deposits are not custodied by anyone, which protects us from the administrators who'd otherwise like to use our money to make loans to their friends
[03:15] or hey, just buy more speedboats. And we want markets that are resilient to any and all takedown attempts, keeping our
[03:24] commerce free and flowing 24/7. In short, we want the same level of decentralization in our markets that we aim for in our native
[03:33] token networks. For this reason, truly decentralized token networks need not care very much about the
[03:41] day-to-day green or red lights issued by legacy silos. Because the market that will end up being the most profitable in this world is the one
[03:50] that includes the most people. In other words, the market that transcends borders.
[03:58] So let us take our green lights in stride, if we happen to receive any, and also take any red ones with a similar grain of salt.
[04:08] Because a genuine revolution is underway. The old and new modes of commerce are fundamentally incompatible with each other.
[04:18] Given this, diamond hands have little more to do except keep hodling and keep building the markets we wish to see.
[04:28] This is why we build. >> Hello, hello.
[04:34] Welcome back to Incubator Weekly. What up, co-host Rion?
[04:38] >> Hey. Loved the intro this morning.
[04:41] I didn't get a chance to watch it before this time, and so it was the first week that I actually get to see that as everybody else sees it.
[04:49] So that was great. >> Oh, well, thank you.
[04:54] And what up, Coffee McCoughsalot? I'm glad you could join us despite your condition.
[05:00] >> It's not coffee. It's a virus of some sort.
[05:04] >> Oh. Sorry to hear.
[05:06] Well, I hope you get well soon, and I hope that you keep breathing just long enough to show us today Dash Keys.
[05:15] This is the second report on this entire suite of tools that has been headed up by AJ that we call either Dash Tools or Payment Tools, and so, Rion, will you give us like a brief
[05:29] high-level overview of what the purpose of Dash Keys is? >> Well, as the name suggests, everything in cryptocurrency has to do with keys, and
[05:41] as the name of this library suggests, this is a library that lets you make those keys, whether those are private keys or public keys.
[05:51] I think that there's a little sub-library that's -- I guess you could say it's a dependency, but AJ would probably disagree with that term, that actually does make the public keys from
[06:05] the private keys, but we'll get into that, I think, as we go. >> Okay.
[06:10] So then let us -- shall we start pulling up some visuals now, AJ? >> Sure.
[06:18] >> What do you want me to pull up first? >> Let's pull up the README, the README from the repository.
[06:28] So this -- these are being held right now in the repository called -- the organization called Dash Hive, and the repository -- the master repository for all of these tools is
[06:41] Dash-tools, and that links to each of the ones that we're highlighting in this series, one of them being this Dash Keys library.
[06:54] So -- and then that Dash Keys library then further links to, I think, what AJ's got up right now, which is the Dash Keys CLI, which is how to interact with the Dash Keys library
[07:10] through a command line, through the terminal. >> Yeah.
[07:14] >> And I'm going to actually jump out because I forgot to get my water, so I'll let AJ take it away.
[07:20] >> Okay. So there's a library and a -- there's a -- not just a library, but a formal specification
[07:30] known as secp256k1, which is basically -- >> It gives me chills just hearing it.
[07:37] >> Yeah, exactly. So that is a specification for a mathematical function.
[07:43] So basically you put a number in and you get a number out, and that is -- that is how private keys work.
[07:49] So we talked about before, a private key is any random number that can become -- or, sorry, it doesn't have to be random.
[07:57] It is any number that can become a public key. That is a private key.
[08:02] Now, if it's not random, then maybe it's not actually private, but yeah, all the same. So the lower level to this is the secp256k1, which is what does the conversion from private
[08:18] to public key and does the signing and the verification. So if you want to send money, you sign the coin that you're sending, and then you might
[08:28] receive a new coin back in another address web. Okay.
[08:32] That's the underlying technology. But the way that we interact with it is a layer above that, and that's what dash keys
[08:39] is. Dash keys is the layer above.
[08:43] So dash keys is meant to be more of a, again, a developer tool. This is something that you would not use on its own, whereas before we covered dash phrase,
[08:57] and dash phrase can work on its own. It's got lots of different uses.
[09:00] You could use it on its own. Dash keys, I would not ever recommend that you use on its own because if you were to
[09:08] not use what we call HD keys, then it's easy to lose your keys and you don't want that. You want things that are easy to keep.
[09:16] But, so this is kind of a mid-level tool in that regard, that it is above the cryptography piece but it is below the wallet-like piece, or the wallet key enumeration piece.
[09:37] So with this tool, you can convert, it essentially just wraps the other library that I just spoke about, or you could actually pick, because as Rion mentions, it's not a hard dependency.
[09:52] There's a reason that you might want to, depending on what you're implementing, you might want to choose one implementation of that specification versus another.
[09:59] You get the same results, but it's just different code. But this is a layer above that and it basically handles the encodings and going between the
[10:11] different formats. So let me see if I can actually find a good explanation of that.
[10:16] I had that in here somewhere at some point. Okay, yeah, so, well let me just show something first.
[10:32] So here's a command that you'd only ever run in development. You would never use this, hopefully, in an actual product.
[10:39] But there's -keys generate and it lets you know this is an option for developers. Don't use this for production.
[10:47] Use an HD wallet to generate keys. Don't just generate them purely non-deterministically.
[10:55] Which is, I'll jump in. So now I forgot what I was going to say, but I was going to say the -hd library, we're
[11:04] going to cover next time, I think, in the series, unless we want to go into detail about secp250k, whatever.
[11:17] That's an interesting topic, I think. So if we get requests to do that, I think we could do that.
[11:23] But yeah, most likely we'll go into the -hd thing, which skips back to last week on how you generate the randomness that that library will use.
[11:39] But like AJ said, this is just the encoding back and forth between the keys. So we will be talking about that, the hierarchical deterministic keys in the following.
[11:53] So worst case scenario, if one ran this in the way that we're saying is no good, it wouldn't support HD, and so any additional addresses generated beyond what some number would have
[12:07] no backup? Or what's the worst case scenario?
[12:10] So this is just literally generating a random number so that you can use it in isolation for development purposes, to be able to test, to be able to port between different programming
[12:20] languages. So this is just so that you can deal with a small piece, because we don't actually use
[12:26] random keys in the software that we consider to be wallets. We use deterministic keys.
[12:33] Some wallets do, though. Some wallets do, so I think it's important to note that, and in fact -
[12:37] If they do, run. Don't use that one.
[12:42] Not necessarily. Before recently, our actual main wallet did use that strategy of just creating, it's called
[12:51] a JBOC wallet, just a bunch of keys. That's what you call it because that's what it is.
[12:59] It's just a bunch of random keys that you're creating, and you can still back those up as a file of just a bunch of random keys rather than backing them up as a 12-word seed phrase.
[13:12] So this isn't unsafe in the sense that it's not correct. It's just that it's more difficult to back up, right?
[13:20] It's unsafe. You don't lose money when you use a recovery phrase.
[13:29] Recovery phrases mean that you never lose money. When people have trouble, you've heard about people upgrading from one version of a wallet
[13:38] to another version of a wallet and losing money. That's because of the JBOC, whatever.
[13:46] So I would never recommend anyone do that. I think that Dash Core does that by default still because Dash Core comes from BitCore
[13:53] and it's basically not been updated in 10 years other than a few changes that are Dash specific, but the basics of it is still just BitCore.
[14:03] I would never recommend that to anyone that I care about. I might recommend it to my enemies, but I don't have that much malice for my enemies
[14:11] to recommend them to do that. But I just want to be clear that that's because of the more difficult way of backing up, right?
[14:23] Yeah. It's just more failure prone.
[14:25] It's scary. To me, that's scary.
[14:28] I would not do it. I would not recommend it to anyone else.
[14:32] The recovery phrase is not scary at all. You generate it from pure randomness, and then from there, they are hierarchically deterministic.
[14:40] I feel perfectly safe with that. It's perfectly secure.
[14:43] I'm very, very happy with that approach. I would never use the other approach.
[14:48] Okay. Let's jump in.
[14:50] Yeah. But if you were going to use that approach, then you could just run this Dash keys generate
[14:54] over and over and over again and just generate a bunch of keys here. And then, if I, those are, they're all otherwise known as WIF, oh whoops, and I would need
[15:04] to do something else. This is actually putting them all out without new lines, so they all run together.
[15:13] Let me just print one of these out here. So I just created a bunch of these.
[15:17] I don't know if you can see it very well. Let me try to zoom that in a little bit.
[15:21] So this is a WIF. So this is just an encoding.
[15:25] It's a base 58 check encoding, and that's much of what Dash keys is, is the hashing and the encoding.
[15:31] So Dash keys includes RIPEMD 160. It includes the SHA, I don't remember if it's SHA-1 or SHA-256.
[15:40] It includes the base 58 encoding and the base 58 checksum encoding, which is base 58 check. So it's basically just converting between a more human-friendly format back and forth.
[15:55] And this is the format that would go into a QR code. So when you send someone a QR code, the QR code is a representation of a string that
[16:03] looks like this. They all start with the capital letter X, and then depending on if it's the private
[16:09] key, it's this long. If it's the public key, it's only this long.
[16:14] And then Dash keys will let you, so that's generating just a random number, and then it will let you, I can give it a WIF file, and then it will print out what the pay address
[16:29] is for that WIF file. So the private key has an associated address.
[16:36] The address is a hash of the public key, and that's what you pay to. You pay to the public key hash.
[16:43] And this just allows you to inspect those things. So for example, I could also run inspect, and then I could give it a file, and then
[17:04] it will say, "Okay, here's, is it valid? Yes, it's valid.
[17:09] What's the version? It's CC."
[17:11] That's the main net version for Dash. What's the pub key hash?
[17:15] There it is in hexadecimal. What's the pay address?
[17:17] That's the pub key hash in base 58 check encoding. What's the private key?
[17:22] There it is, masked. What's the checksum?
[17:24] That's the checksum in hexadecimal. And if I were to do unsafe on this, or no, unmask, then it will print out the private
[17:33] key without the mask on it, so I could see the whole thing. And then we could look at not just a, that was looking at a private key file, but we
[17:42] could also have it look at just a public key as a string, and if I do that, it's going to give similar information, except it's not going to have the private key information
[17:51] because it's just reading the public part. Because you can't get the private part from just the public part.
[17:58] Yeah. Let's look at this for just a minute.
[18:02] I want to talk about the version and what that means. Yeah.
[18:05] Because it's not- And you see the versions are different here.
[18:07] This is the version for the private key is CC, the version for the public key is 4C. The address, sorry.
[18:15] Strictly it's not encoding back and forth, because to me that assumes that it's just basically converting between one number system and another number system.
[18:26] But it's also adding these, like what we called last week, these magic strings, which are different for each chain, different for each, TestNet has its own different version.
[18:37] And the CC is what turns things into always leading with an X. Correct?
[18:45] Yeah. So having, basically when the encoding goes from the binary version of the, so this is
[18:55] hexadecimal, but if we take that and we encode the original bytes as base 58 check, these bytes are such that it always selects the letter X when it gets fully encoded.
[19:14] So this is a prefix to this. So the string that's actually encoded is CC, 1B, blah, blah, blah, blah, CB, 7, 8,
[19:24] 2, 4, da, da, da, da, da, da, C6. And that's this piece plus this piece plus this piece are all encoded together equals
[19:33] this piece. Okay.
[19:36] Yeah. And so when you convert that hexadecimal CC into base 58 or base 58 check, that's what
[19:44] makes the X. And that's what, you know, Evan originally, he, he deter, he decided I want, I want the,
[19:53] I want this prefix. I want this version to be hexadecimal CC so that when encoded in base 58, it turns out
[20:01] to be an X. Yeah.
[20:03] Yeah. So that's the vision that the developer made.
[20:05] Yup. And I, and I did say that wrong, by the way, it would be CC plus the private key plus the
[20:10] check would yield the private key that we don't actually, we're not actually looking at because it's in the file here on this one, it would be 4C plus the pub key hash plus
[20:20] the check would yield the original public key, which was this. So yeah, just to clarify, I did say the wrong thing when I was explaining that.
[20:29] And so, but this, yeah, that's, that brings up the point that this repository is a great educational tool because even though if you set it wrong, the documentation, it's very
[20:41] well documented. So if anybody developer or not is just curious what these things are, you can look at the
[20:48] documentation and get some idea. And this, this video version is just kind of a summary of this that we won't be able
[20:55] to go into the details of, of any of it, but basically hopefully, hopefully it gives people an idea of where these where these long cryptographic keys and addresses come from.
[21:08] It's not a mystery. It's just math and conversions and things like that, that people can and should understand
[21:14] that are using this on a regular basis, or at least, I don't know, that's one theory. The other theories is that people shouldn't know anything about this and they should just
[21:27] wait for usernames to come and then hopefully they won't have to think about any of this, but I think it's interesting nonetheless.
[21:33] I think it's important to know, I think the dash phrase is the most important thing. People need to know that their wallet is 12 words.
[21:40] And if they, if they don't, if they're, and they also need to know that if they don't have a, if whatever software they're using doesn't use the 12 words or potentially there's,
[21:50] there are other word sizes you could use, 24 words, whatever. But if it's not using a wallet that has a recovery phrase that just get the heck out
[22:01] of it unless you're Edward Snowden and you just want to remember all of your, your, your keys, but I don't think Edward Snowden, I think Edward Snowden would go with the recovery
[22:09] phrase because then he could remember it and never have to write it down and not have to have backups.
[22:14] But yeah, for the average person, you just want to have that recovery phrase and send it to somebody.
[22:19] And the, and, and what Dash Keys is going to do is Dash Keys is going to work hand in hand with the hierarchical deterministic wallet tooling to be able to convert between the
[22:30] different formats so that when you make a QR code or when you make a payment. So if, and again, when you, when you put this stuff on the blockchain itself, a lot of this
[22:39] stuff is layered. So what actually goes on the blockchain is this right here.
[22:44] So the blockchain does not get the version number. So we basically have the different set of seed files.
[22:51] And so when a Dash client connects to the Dash network, that's because there's a centralized route of, of, of locations that are in a file that's distributed with the clients.
[23:06] And so it selects from those predetermined well-known addresses to start connecting to the network.
[23:14] And then, then it starts to become more of a decentralized process in the sense that the nodes that it connects to refer other nodes and, and, and those nodes, they don't,
[23:26] they just assume that everything is for the Dash network. So there is no check to make sure that when you make a payment, that you're actually making
[23:33] a payment on the Dash network. All of that stuff is happening in the software layer up above.
[23:39] It's not happening down on the protocol layer. So that's important to understand.
[23:43] So what's actually sent on the blockchain is just the pubkey hash, not the address, not the version, not the checksum, it is just the pubkey hash.
[23:53] And the pubkey hash, could that, we could have that pubkey hash, if you could go back to AJ's screen for a minute, we could have that pubkey hash would be a valid pubkey hash
[24:05] for something like Bitcoin Cash or Zcash or any of these, these types of chains. I don't know if it works for Ethereum because they have something similar.
[24:19] To clarify a comment you made just a minute or so ago, Rion, you had said that, in your opinion, everyone who uses these tools should have a basic understanding of where addresses
[24:32] come from or how they're generated. And then you said a different opinion was that, no, it's fine to only be knowledge,
[24:41] like concerned with usernames or whatever. In the case that usernames become deployed and functional on the Dash network, would
[24:51] it be that any amount of what we're talking about today is no longer in use, or it would still be in use exactly as we're talking about it, but there would just be a layer of abstraction
[25:04] on top of it? The latter.
[25:07] Yeah. It still uses all of the same stuff under the hood.
[25:11] It's just buried underneath some abstractions. So the user would only have to know his 12 words to be able to generate all the private
[25:27] keys and then all the public keys from that and all the public key hashes. The 12 words can generate everything, but then one of those things that it generates
[25:38] is what's called an extended public key. And those are the things that usernames, when you're making friend requests and contacts,
[25:48] you're exchanging public key hash, extended public keys. And that way you can generate addresses for each other for a certain username.
[25:58] So we'll talk more about that in future shows as well. Okay.
[26:03] And that's what Dash HD is. Dash HD manages your first extended private key is for your own wallet, but you generate
[26:14] extended public keys to share with someone else for their software wallet. And so distinguishing software wallet versus wallet, wallet is the 12 words, software wallet
[26:26] is the tooling that you put the 12 words into or that generates the 12 words for you to back up that then does all the other stuff like user to user payments and whatnot.
[26:37] TL says, I haven't thought too deeply about this, but do any of you have a strong opinion on whether Dash should just use HD keys and stop using non-HD altogether?
[26:46] Oh, that's kind of what Ajay was talking about recently. Go ahead, Ajay.
[26:53] Yeah. Non-HD is just a terrible idea.
[26:56] It's the only reason that anything should have non-HD at all is simply because it's old.
[27:03] Because when these things were started, remember in the beginning, there were not payment addresses in the beginning.
[27:09] It was, this was the pub key hash. This is, you know, payment addresses came later.
[27:14] All of this stuff were part of the BIPs, right? So there is no reason to continue to use non-HD today.
[27:22] I can't think of a use case for it. It can only lead to lost money.
[27:26] There's, I can't think of a single benefit and if somebody else knows one, challenge me on that.
[27:32] But I don't think that there is any benefit whatsoever to non-HD wallets. I think they are just disaster waiting to happen.
[27:39] Yeah. I don't think of any either.
[27:45] Let's pick up where we left off. Do you want to show any more of the features of the CLI or should we jump back into the
[27:55] documentation? We can jump back to the documentation.
[27:58] This is pretty much it. I mean, it's just, it can, for the purposes of developer demonstration, it can generate
[28:09] a non-HD address or a non-HD key and a non-HD address, but that is just for the purpose of demonstration.
[28:17] I never recommend that anybody use this other than for, you know, it's just, like I said, it's so that we can make the tool small and you don't have to worry about all the other
[28:26] pieces. If you can pass these test cases, then you know that this part of the tool is working.
[28:31] That's why this exists in that way. And that's why every time you use it, it prints out, Hey, you know, warning, this is developer
[28:37] option only. But you know, it, it, it can, it can give you what an address looks like.
[28:42] It can convert it, or it can give you what a private key, a WIF wallet, import format, private key looks like.
[28:49] It can give you the address. It can inspect it and it can verify it and inspect the difference between inspect and
[28:53] verify is that inspect will, if something doesn't pass the checksum, it will still decode it without throwing an error.
[28:59] Whereas verify, if it doesn't pass the checksum, it will give you the error. And correct me if I'm wrong, but I think we started this one.
[29:10] And this was one of the earlier tools that we started when you were going down your journey and you were basically doing all of this to understand how this works.
[29:23] And it wasn't until later that we kind of dove into the HD stuff and, and then you created the HD library.
[29:33] And then my question is, does that kind of replace this or is this used as a dependency of the HD stuff?
[29:44] This is a dependency of the HD stuff, because this is all of the, the primary purpose of this is the encoding.
[29:51] And so you can think of going from the, yeah, the primary purpose of this is, is the hashings and the encodings and the HD wallet needs to use those too.
[30:03] And if someday in the future, we replaced RIPEMD 160 with a more secure hash algorithm, for example, we could replace that here in dash keys and dash HD would not be concerned
[30:19] with that because dash HD doesn't implement that hashing. So dash HD is only concerned with the processes that essentially generate and tweak the random
[30:31] numbers or the, or the pseudo random, because they come from a true random seed and then are pseudo random, but deterministically generated after that.
[30:41] So that's, that is the only responsibility that it has. So each of these libraries are separated according to a distinct responsibility.
[30:50] So basically code that changes together, lives together and change code that doesn't change together, doesn't live together.
[30:58] So that's why dash phrase is its own thing can be used independently. Dash keys is its own thing can be used independently.
[31:04] Dash HD technically can be used kind of independently, but only to an extent because it does, it, it does rely on the ability to encode and decode keys.
[31:19] So you, you could, you could export it in its raw format without the encodings and you could use it.
[31:25] So you could generate an X pub where you, you output the X pub as raw hexadecimal rather than as encoded, but we don't have any tools that use it that way presently.
[31:39] Gotcha. Okay, well should we just scroll through, do one last scroll through that documentation
[31:50] to give people an idea of, of what's, what's in this in case they want to look deeper into it?
[31:57] Sure. Let's I'm going to go over to the library here.
[32:01] So dash keys JS is the library dash key CLI is the command line tool. And again, the reason for the distinction is because the library is, there are things
[32:12] that you need to include in a command line tool that are not actually part of the library. They're just helper functions for being able to create that interface between the human
[32:21] and the keyboard and the code. Whereas the library is useless all on its own because there's no inputs or outputs.
[32:29] There's no way to connect to it or use it. You have to write other code that will use it.
[32:33] But this is the core of it is dash keys JS. And you know, essentially it's just, it's responsibility is to go back and forth between
[32:41] with an address format and do the check sums and the, and such. Can we zoom in a bit more on this if we don't lose anything?
[32:51] Let's see. 150.
[32:53] There we go. Yeah.
[32:55] There we go. So table of contents, you know, brief example of how you install it, how you use it, the
[33:00] API, and then the glossary of terms and the fixtures. So if we go down to usage, there's kind of two, two, um, namespaces.
[33:16] There's dash keys itself and there's dash keys dot utils, oops, excuse me. And the difference between those is basically dash keys is what the real responsibility
[33:24] of dash keys is, and utils exposes some stuff that's just a little bit lower, but it's still, you know, from a developer perspective, you'd still, if you, you could replace the utils
[33:39] stuff with something else, with your own implementation. But so we have generate with non HD, and this has a really long, annoying name to kind of
[33:48] cue you into that. You shouldn't use it.
[33:52] Getting back to that question that we answered before about, you know, why would we ever want to use non HD?
[34:01] So you're, you're naming it to suggest that non HD is kind of not the default that you want.
[34:08] Right. Yeah.
[34:10] Right. Yeah.
[34:12] But in order to use the other, the other functions, so all the other functions you would use with dash HD essentially but if you're not using dash HD and you're testing this in isolation,
[34:23] well you need something. And so that's where if you wanted to generate something, then, you know, here you go, that
[34:30] will do it for you so that you can test it, but there's the whiff to adder. And I, so one of my gripes about the existing libraries is the inconsistency of the naming.
[34:41] And so I tried to adopt a couple of conventions that still, I don't, I don't think that it's really possible to get it quite perfect, but I tried to adopt some conventions.
[34:53] So all the function names are abbreviated and all of the property names are non abbreviated. So because a function name, if it's really, really long, you know, if it had to be wallet
[35:04] import format to address, that's so long that it starts to become difficult to interpret. And so for the function names are typically abbreviated throughout this set of tools.
[35:16] And then sometimes the pub key and priv key are cased differently because pub key is often referred to as one word, whereas private key is most often referred to as two words.
[35:29] And also when you just look at it at a glance, you want there to be a distinction because pub key and priv key look very, very similar.
[35:38] And if you were looking for a mistaken code or you're auditing for security vulnerabilities, using the capital K on priv key just makes it a little bit more distinct because the
[35:48] visual pattern of it, as you're scanning, it has that bump of the capital letter rather than being completely lowercase.
[35:56] So that's some of the ergonomics that I went through with all of these was trying to try to make the right compromises in terms of security that you don't think about, which
[36:05] is the human element. The human needs to notice if something looks right or looks wrong and where things are
[36:11] very similar, there needs to be something to make them distinct as well as just the ergonomics of consistency that, you know, if it's spelled this way in this library,
[36:19] it should be spelled that way in the other library as well and whatnot. But then we have, yeah, so we've got the whiff to adder, priv key to whiff, so, and then,
[36:31] and then, did I have, I think there's whiff to priv key here too, I just didn't show that in this brief example.
[36:38] And then the API basically shows everything. So adder to PKH, which is pub key hash, this is a one-to-one conversion, so these are bi-directional
[36:46] conversions, one-to-one. Pub key hash to address, address to pub key hash.
[36:51] Pub key to address is, meaning that it goes from pub key to pub key hash, that actually is not one-to-one conversion, that actually belongs down here, I put that in the wrong
[37:04] place, but never mind. Priv key to whiff, whiff to priv key.
[37:08] So that one is, it's in the wrong section, it should be down here in the one-way conversions. Because we, once we go from a private key to a public key, we can't reverse it back.
[37:17] Once we go from a public key to an address, we can't reverse it back. Once we go to a pub key to a pub key hash, we can't reverse it back, but we can go one-to-one
[37:26] between address and pub key hash and whiff and private key. When you say one-to-one, I think it's actually probably more understandable how you have
[37:34] it written, the bi-directional, because they're both one-to-one, it's just one is a one-way conversion, you can't get a private key from a public key.
[37:47] That's not allowed under the typography. So I think that's how you have it separated.
[37:54] Yeah. And then we just have the raw decode and encode key.
[38:02] So this is for the base 58 check, and then you can see what the output looks like and what the possible types are, what the possible version numbers are.
[38:11] These are testnet versions, these are mainnet versions. There's some helper utils, such as, amazingly, after so many years, we still do not have
[38:22] a standard way in JavaScript to go from a buffer format to hexadecimal and back. So it's something that ends up being three or four lines of code, but it's just one of
[38:32] those things that needs to be available and exposed so that you have access to it and you're not needing to rewrite it yourself, because those three to four lines of code
[38:42] just get obnoxious. And then same thing, ripemd-160-sum.
[38:47] So most other libraries have this as a dependency. But the thing is, I chose to bring all of this together, because code that changes together
[38:55] stays together, is the idea, the clean architecture principle. So I brought everything that you need for the key conversions into one, and after surveying
[39:05] the entire landscape of the code, there is no other place where ripemd-160 is ever used except in dash HD, which it's used for a different purpose.
[39:16] So it actually is technically a true dependency of dash HD. But if we ever upgrade the ripemd-160 to be a more secure hash algorithm, we would also
[39:27] update it in dash HD as well at the same time as other cryptocurrencies have done. And AJTL wants to know, "How does dashphrase's seed connect to this library?
[39:40] Is it like the WIF?" No.
[39:43] So we'll talk about that when we talk about dash HD, but the dashphrase seed goes into dash HD, and then it is a custom non-spec key expansion algorithm, is what dash HD is.
[39:58] And the reason that it's non-spec, in terms of broader specifications like RFCs and NIST and all of that, is because of the way that it gets used with what's called an HD path.
[40:09] But we can, we've already gone on so many tangents right now with this, I think that it's better to save that for when we actually talk about dash HD, unless anybody disagrees.
[40:21] That is a great question though, because the dashphrase, the end of dashphrase, kind of the end of the line of dashphrase is that seed, and knowing what to use that seed for
[40:36] was kind of an open, like we didn't really talk about that last week, so we will talk about it next week.
[40:41] Yeah, and that's where the various hashing algorithms come into play. So like I said, you need to have a Secp256k1 implementation.
[40:50] There are different implementations that have different trade-offs, in terms of whether you want to use it server side, or you want to use it in the browser.
[40:57] I selected one that seems to have the best of all worlds. I selected the one that seems to have the best trade-offs in terms of it's easy to audit,
[41:06] it runs in the browser, it runs in Node. In some use cases, this one could be marginally slower, but I think that the use cases in
[41:16] which it's marginally slower are vanishingly small. But because someone may have a legitimate reason to choose a different Secp256k1 implementation,
[41:28] that is not a hard dependency of the library. And so if you wanted to use a different implementation, what you would do is you would just overwrite
[41:38] these two util functions with whatever your library is, and so here's an example of using the original Noble Secp256k1, which is, this is what we use, but it has a couple of tweaks
[41:52] because that one was before Node v18 was released, and so it was still using Node custom crypto rather than standardized web crypto.
[42:03] And so I just made a couple of tweaks to it so that it would use web crypto, and they actually have updated Noble Secp256k1 to the current release of Node, so we may actually
[42:15] go back to using this one rather than using our @-incubator/secp256k1. So if we were to do that, I would literally just copy and paste this code, and then I'd
[42:28] have to make sure that the new version has the same function signatures, and if it doesn't then I would have to change them.
[42:39] But basically, yeah, if you wanted to choose a different implementation, this is what it would look like to overwrite these two functions, and then everything else will work the same.
[42:48] So it's a semi-dependency, because you have to have some implementation, but I'm not picky about which implementation you choose.
[42:55] But if you follow the documentation, then you're going to install our implementation right here.
[43:01] So that's the one that's the default, that's the one that this is set up to use, it's a one or two line wrapper, so I just let that code hang in there without you having to do
[43:11] anything. And then we're kind of down to the glossary.
[43:17] All right, and so maybe one last thing that I wanted to end on is just a higher level recap of why we're doing all this in the first place again.
[43:29] Isn't all of this already done by the broader cryptocurrency space and/or Dash Core Group? I mean, we've already done all this.
[43:41] What would you say to that? And then maybe I'll add something to it.
[43:44] So I would say no. It's amazing to me.
[43:47] I mean, this is one of the things that just blew me away, is that in the 10 years or whatever it's been since these tools have been created, they have been largely untouched.
[43:57] So they pretty much rely on the same hacks, and by hack, I mean non-optimal way of doing things.
[44:04] You know, say that you don't have a knife, and all you have is a spoon, and so you just kind of sharpen the edge of the spoon.
[44:12] That's what I mean by hack. It's like you take the tool that you have, and you just make it work.
[44:17] You put that square peg in the round hole, and you just pound it until those square edges kind of round off.
[44:23] And that is the way that most of the code is written, and moreover, the code was not written for JavaScript.
[44:30] It was written for Node. And so it won't run in a JavaScript environment.
[44:37] And that's why when you try to get Dash Core Lib, or Bit Core Lib, or whatever, to run in a browser, it's megabytes of code, because it runs through a transpiler tool that turns
[44:49] that Node code and adds tons of stuff to it to make it compatible in a JavaScript-only environment.
[44:58] And so having code that's actually written in JavaScript that will run in any JavaScript environment is important.
[45:10] It's simpler to read code. It's easier to port to other languages.
[45:14] So like I said, if we need to port this over to Swift or Kotlin, we have a very relatively simple code base.
[45:21] Some of this stuff is complex, because it is complex, because the standard defines a complex standard.
[45:27] But in terms of not having complexity of shims and hacks, the complexity needs to be-- and this actually needs 138 screws-- it doesn't need to be that the complexity is, and we're
[45:45] making a screwdriver out of plastic and forks. It needs to be, well, we've got the screwdriver.
[45:52] We've got the right tools for the job. So this is built with the right tools for the job so that it'll run in the browser,
[46:00] and it doesn't break in the other environment. So it works in BUN.
[46:04] It works in Node. It works in Deno.
[46:07] It works in Chrome. It works in Safari.
[46:10] It works in Brave. It works in Firefox.
[46:13] And it's also very lightweight. Again, we talked about if you are-- we're trying to convince someone to accept Dash,
[46:23] or we're trying to provide-- I don't think we're going to convince anyone to accept Dash, but let's say that we're trying to provide a solution for somebody that wants to do payments,
[46:32] and that solution includes Dash. They're not going to want to include two megabytes.
[46:39] That's compressed, minified. That's like the minimum size, right?
[46:44] We're not going to want them to have to accept that they have to load two megabytes onto their page just in order for someone to eventually get around to the checkout screen.
[46:54] That's just an absurd amount of code and load time. I mean, it seems really small until you think about the way that the world actually works
[47:04] and the use cases where Dash might have an advantage. Right.
[47:08] The global world is much, much less forgiving on these kind of things. And that's why, as I was-- I do a lot of research into the Web2 space and what kind of trends
[47:22] are going on there, and what I'm seeing is people are doing crazy, crazy things to be able to shave off kilobytes of JavaScripts downloading into your browser, or to shave
[47:36] off a couple hundred milliseconds of load time. That's the trend that's happening in Web2 right now, and we need to accommodate that
[47:44] if we expect to have our Web2 friends pulling Dash into their web applications, which that is one of our biggest targets.
[47:55] So yeah, that's why I really wanted this to be done, not only for the educational aspects, but also for just those performance gains.
[48:07] Yeah, I think it's really important. Right on.
[48:13] Okay, so as mentioned, we will cover more of these-- sorry about the construction on my end, everybody.
[48:19] This is clearly a sign, like a cut transmission, but we will feature more of these tools in the future.
[48:27] And any final comments from either of you gents? No, just looking forward to having a good week, and yeah, we've got some changes coming
[48:38] up in the incubator. Not big changes, but just changes that I've been trying to get to for a long time, so
[48:44] hoping to get moved over to GitHub, and looking forward to that. I will drop this into the chat, if Pete could relay this into the YouTube chat for anybody
[48:56] that wants to take a look. So this is-- oh, whoops, I actually linked to the wrong spot, let me get the right link.
[49:03] This glossary here is helpful for anybody who wants to kind of understand what these things are.
[49:08] This is in alphabetical order, not in the order that you'll encounter them, but there's a hundred different terms you need to know, and there are a few glossaries across the
[49:17] repositories to kind of help you understand. This is the glossary that is just for this repository, and these-- you know, here I'm
[49:27] just running off the cuff. I tried to take a little bit more of a succinct approach to these glossary entries, so that
[49:34] they are, you know, a few concise sentences that give a pseudocode example where appropriate, so you can see these are not long, rambly-- well, except for that one, but there's a reason
[49:48] for that, because if-- yeah. But in general, these are not long, rambly entries.
[49:55] These are very concise and succinct, this is what this thing is, and then the two exceptions being the actual private key generation, and the reason for that is, if you were to look
[50:05] at the library for private key generation or public key generation, there's a lot of functions that, like, this function calls this function, calls this function, calls
[50:13] that function, calls this function, with, like, these variables set up. And so, for these, I just kind of cut out all the middlemen and put it all together
[50:23] so that you can see, almost in a single screen, the gist of what that looks like, as opposed to having to hop around between, you know, 15 different functions and variable declarations.
[50:33] But other than that, most of this stuff is pretty straightforward, and if you've got any feedback on it, you know, you can open up an issue, you can go up here-- let me see
[50:47] if we can get this-- you can go up here and open up an issue and say, "Documentation sucks for X, Y, Z."
[50:54] And you know, we can at least have whatever that is documented here, and then maybe eventually get around to coming up with better descriptions in the main readme or in the glossary.
[51:05] >> Righteous. All right, thanks for joining us, everybody.
[51:11] We'll see you next time, same place, same time, same time, same place. Sleep.
[51:18] Feel better. Bye.