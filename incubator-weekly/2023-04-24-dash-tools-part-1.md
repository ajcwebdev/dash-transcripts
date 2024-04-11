---
showLink: "https://www.youtube.com/watch?v=PHLnuPVS99U"
slug: "dash-tools-part-1"
title: "Dash Tools #1: Recovery Phrase Generator “DashPhrase”"
publishDate: "2023-04-24"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/PHLnuPVS99U/maxresdefault.webp"
---

AJ provides an overview of Dash Phrase, a JavaScript library for generating cryptocurrency wallet recovery phrases.

## Episode Summary

tl;dr: AJ discusses Dash Phrase, a JavaScript library that generates cryptocurrency wallet recovery phrases, which are 12 words that represent a wallet. He explains how the library works, including how it generates random numbers, encodes them into words, and uses checksum validation. AJ also differentiates between interpreting numbers in different bases versus encoding them. The episode includes a demonstration of the library's code and documentation.

## Chapters

00:00 - Introduction and Overview of Dash Phrase
AJ introduces Dash Phrase, a JavaScript library for generating cryptocurrency wallet recovery phrases, and explains how these 12-word phrases represent the actual wallet.

09:07 - Technical Details of Dash Phrase
AJ delves into the technical aspects of Dash Phrase, including how it generates random numbers, uses a 2,048-word dictionary for encoding, and incorporates checksum validation.

25:26 - Encoding vs. Interpreting Numbers
AJ clarifies the difference between interpreting numbers in various bases (e.g., binary, decimal) and encoding them into words or other representations.

33:24 - Demonstration of Dash Phrase Code and Documentation
AJ showcases the Dash Phrase library's code and documentation, highlighting its simplicity and thoroughness. He also explains the difference between the library itself and the command-line interface program.

## Transcript

[00:00] that the United Commission, or SEC, has, not surprisingly, filed yet another lawsuit against a company selling digital assets, claiming that these assets are unregistered securities
[00:13] under U.S. law. The surprising thing about this particular lawsuit, one that got a whole lot of attention
[00:19] from social media, was that one of the assets that the SEC alleges is an unregistered security is the native token of a nine-year-old proof-of-work blockchain that had no pre-sale or ICO, Dash.
[00:35] This is a kind of claim that the SEC has never made before. What would cause this group, led by Chairman Gensler, to make such a claim, especially
[00:45] given the fact that Dash is Bitcoin-based, and the chairman has already said that Bitcoin is not an unregistered security, but is rather a commodity?
[00:54] An examination of the lawsuit filing contains a clue. Masternodes.
[01:00] Dash is the digital asset industry's pioneer of masternodes. They're a technological breakthrough which has enabled huge advancements in proof-of-work
[01:10] capabilities like the instant settlement of all transactions, a protocol-level implementation of always-on CoinJoin, transparent stakeholder governance, and a block reward-issued treasury.
[01:25] All this is to say nothing of basic transactional scalability either, because with masternodes in place, Dash can comfortably scale to credit card-level throughput, all without sacrificing
[01:37] decentralization or security. So why is an organization claiming to have the best interests of investors at heart?
[01:45] I think we have a role to protect the American investor. Not steering the public away from technologies that are low-functioning and can't scale,
[01:54] and instead encouraging them to explore ones that are high-functioning and can scale. Why are they doing, in fact, precisely the opposite?
[02:04] We can't help but be reminded of Satoshi Nakamoto's message to us all, which was embedded in the genesis block of Bitcoin in 2009.
[02:12] Chancellor on brink of second bailout for banks. This message underscored the fact that banking institutions, in this instance in Great Britain,
[02:22] may have been working nicely for a small class of elite bankers, but they weren't working in the best interest of the general public.
[02:30] And if Satoshi were to embed another message for us today, but this time about the SEC in the United States, he may hint at something similar - that the agency may indeed be working
[02:42] for a small class of elite securities brokers, but that it just isn't working in the best interest of the general public.
[02:51] And it's for these very reasons that blockchain technology was invented in the first place. So that regardless of the actions of chancellors or chairmen, the general public could still
[03:02] have access to the economic tools and services that it needs. I actually at MIT taught a course called blockchain and money.
[03:10] I taught multiple courses called crypto finance and other courses as well. But you didn't own any crypto.
[03:17] You taught the course, but you weren't a user in the product. I did not own crypto assets.
[03:24] The majority of Dash users are likely very sorry that Chairman Gensler isn't interested in even trying out what we've built.
[03:32] We'd love to have him as a user, as a masternode operator, and it's a loss to our network if he isn't interested.
[03:40] Despite that, we must press forward to continue fulfilling Satoshi's vision of delivering economic value to the masses.
[03:48] The solution's got to be scalable. It's got to be secure.
[03:52] It's got to be affordable, fast, permissionless, and support both public and private payments. These are the things we deliver at Dash, and we'll continue delivering them.
[04:04] Whether our product is considered a commodity, an unregistered security, a digital asset, or something else entirely is up to each person to decide for himself.
[04:16] Everyone is entitled to his own opinion. And this, coincidentally, is why we build.
[04:24] Hello, and welcome to Incubator Weekly, joined by my co-host, Rion. Hi, Rion.
[04:31] Howdy, folks. And a developer for Dash in the incubator, whom you may know, AJ is back as well.
[04:40] Hi, AJ. Hello.
[04:42] So, we have given a brief and actually somewhat frenzied introduction of Dash tools in general. It was actually our second episode ever, and AJ gave us a sort of whirlwind overview.
[05:01] But we decided that it was time to start digging into these Dash tools one by one to learn what they actually do and what they actually are.
[05:08] So, without any further ado, AJ, let's start with Dash Phrase. What is that?
[05:17] Dash Phrase is something that is so simple that it's very difficult to explain, in the same way that describing what is salt is difficult to explain, because salt is just salt.
[05:32] Dash Phrase generates wallet phrases, often called recovery phrases. The term recovery phrase doesn't quite do it justice, because it actually is the wallet.
[05:44] The 12 words that you get when you go into, whether it's Dash Wallet or any other type of cryptocurrency wallet, they all use the same technical specification based on a word
[05:55] list, and they just randomly generate 12 words. The last word actually is also part of a checksum, but that is the wallet.
[06:08] That's what Dash Phrase does. It generates that, and then it also implements the key expansion algorithm, the hashing algorithm,
[06:17] that converts that into the wallet seed. The wallet phrase becomes the wallet seed, and then all of the keys, all of the signatures,
[06:28] everything else is a derivative of that. You can use lots of different software to do that, but your actual wallet, when you
[06:35] think, "What's my Dash Wallet?" it's not the software on the phone, it's not a hardware device, it literally is the 12 words.
[06:42] That's what the wallet is, and that's what Dash Phrase does. It just generates those 12 words.
[06:48] Okay. Then if Dash Phrase just generates these 12 words, there are certainly many a Dash Wallet
[06:55] in existence, and have been for a super long time. What was the need for another recovery phrase generator?
[07:05] This one is based on newer JavaScript technology. This one's written in JavaScript, and that means that we can use it in the web, we can
[07:13] use it on the server, we can use it on phones. JavaScript is, for better or for worse, the universal programming language.
[07:23] The old versions that were made 10 years ago relied on a lot of hacks. As far as I can tell, there wasn't really much out there in the way of things that didn't
[07:35] rely on those old hacks. You get these huge bundle sizes.
[07:40] If you wanted to use the current Dash Core Lib in order to do this, you'd be bringing in two megabytes just to do this one piece of functionality that is occasionally useful
[07:50] just on its own. The purpose was to make it so that it's browser compatible first, then it's lightweight, and
[07:59] then it doesn't have any extraneous dependencies. If you needed to do a security audit of this, there's one file that you need to do a security
[08:06] audit of, so there's no transitive dependencies. That is excluded for the CLI.
[08:13] I don't think the CLI has but two files, but the CLI may include other libraries for the purposes of interacting with the terminal.
[08:21] Likewise, when you use it in a web browser, you're probably going to use other libraries. A lot of people might be familiar with Vue or the less popular but still certainly out
[08:30] there React that people are using to develop sites. There are those transitive things.
[08:38] It's not an entire framework. It's just the library that does the one job.
[08:45] >> Okay. >> Thank you.
[08:47] I put a joke in there, by the way. >> That obviously was some kind of coding joke.
[08:52] Yes. >> That was actually way more popular than Vue, but it's funny that he slipped that in
[08:58] there without anybody noticing. I'll just say also, not that I'm a React fan, by the way.
[09:07] I do like some part of it, but I'll also say that one of the other purposes, at least from my perspective, is as an educational tool.
[09:17] Sometimes people think that cryptocurrency is black magic, and these 12 words just come out of nowhere and are incomprehensible, like what they actually are doing and where they
[09:29] come from. But when you actually look at the code, or just explain, describe the code, which hopefully
[09:36] we can get into a little bit today in detail, because it's not a lot of code, you'll see that it's actually very, like AJ was saying, it's a very simple concept.
[09:46] And I think everybody that is in cryptocurrency and holds cryptocurrency should know the basics of what this is, not just for programmers, but for users themselves, because this is
[10:00] the new financial primitive that we're building on, these 12 words, which, again, we'll get into a little bit more detail on, but at its root, these 12 words are just an encoding
[10:13] of a number, just a different encoding, a different way to describe, I believe it's a 256-bit number, right, AJ?
[10:25] Sort of, yes. I mean, it's 11 bits, but it's 248 bits of entropy within the 11 bits, but yes.
[10:32] You mean 11 bytes, right? Sorry.
[10:35] 11 bits per word, 12 words, 11 bits per word is 132 bits, four of those bits are checksum, 128 of those bits are the entropy, but the dictionary is a 2,048 word dictionary.
[10:51] It's a lookup table. It's really simple.
[10:53] It's like, imagine you had a 2,048-sided die and you just rolled it, and then every time you rolled it, you picked a word that was in a table of the number that it landed on.
[11:03] The words are selected to be easy to read, easy to spell, easy to pronounce, not ambiguous. So for example, there are some simple words like gray that are not included because gray
[11:13] has the English spelling and the American spelling. So it's basically third-grade reader-level words for the most part, so that it's easy
[11:23] to communicate. If you needed to remember it, because that's what you want to do if you needed to communicate
[11:27] to somebody else, you have a high degree of accuracy that you would not be in danger of, "Oh no, I missed a letter," or "I missed a number.
[11:38] Oops, I'm in trouble. My money's lost."
[11:40] This is really simple. You can print it out.
[11:42] You can store it in Apple Notes. You can put it in Google Docs.
[11:45] You can write it down. You can remember it.
[11:47] You can email it to people that you trust with your finances, whatever. There's an endless way.
[11:52] Well, not endless, but there's a myriad of ways to keep it safe by either sharing it or backing it up and have a high, high, high degree of confidence that you can't reasonably
[12:04] make a mistake with it. Okay.
[12:06] Well, part of that is I actually, when ... Is the seed 256 bit? Because there's part of what's in my mind, remembering some of this stuff from many years
[12:19] ago, is that instead of doing these 12 words or to make a private key, you could literally just flip a die or flip a coin 256 times, and then that's essentially what a private
[12:35] key is, is that 256 bit number. As long as it's with that caveat that you and I both know that it has to also generate
[12:48] a valid public key. If it's any private key that's 256 bits long, but it has to also be on that curve to generate
[12:58] a valid public key. But that's not part of this.
[13:02] That's later. Yeah, so there's a few different ways that it's done.
[13:08] So the recovery phrases have ... So first of all, I just want to say that I think that the whole idea of recovery phrases is ... You know that I'm really harsh on all of this
[13:21] cryptocurrency technology. I think anybody that's watched this show knows I'm very harsh on it.
[13:25] This is something that I love because this has nothing to do with cryptocurrency at all, whatsoever.
[13:32] It's something that people in the cryptocurrency community created. But this is just really, really useful because in a lot of cases, you need something that's
[13:39] really strongly random. And so there are 12 word variations all the way up to 25 word variations on this.
[13:46] So for example, the Brave browser previously used 24 word recovery phrases for password sync.
[13:55] So all of your passwords are encrypted with a recovery phrase. And they went to 25 words so that it adds a whole extra bite of checksumming, which
[14:04] increases the integrity in terms of not being able to pick a wrong word in some way, shape, or form and have it still pass the initial validation.
[14:15] It basically drops the chances of that being able to happen pretty much down to zero. But the different length of words in different wallets, you may see an option if you want
[14:25] to generate a 12 word phrase or a 24 word phrase or a 13 word phrase or 25 word phrase. These variations are just basically how many times the computer is rolling the dice before
[14:40] it selects the words from the table. In theory, this is kind of something that's more marketing speak than the reality of the
[14:50] situation. But in theory, if you roll the dice more times, then it's more secure.
[14:58] So in theory, 256 bits is more secure. And the layperson would reasonably think that 256 bits is twice as secure as 128 bits.
[15:12] But this is mistaken. 129 bits is twice as secure as 128 bits.
[15:23] And 130 bits is twice as secure as 129 bits. And this is really simple and deceptive because if you were to take a piece of paper, this
[15:36] can't be done, this is one of those imaginary problems. First of all, you can't fold a piece of paper more than 11 times.
[15:42] There was a myth buster on this. But if you were to fold a piece of paper 11 times, you need a piece of paper that's about
[15:48] the size of a football field, and you end up with something that after being folded 11 times is like three feet high, which just, it boggles the mind, right?
[15:58] If you were to take a piece of paper and fold it in half 64 times, it would reach the moon. So the exponential power is something that's a little bit hard for our brains to comprehend
[16:11] because it's deceptive. You think, "Oh, well it's twice as big, twice as big, twice as big," but very quickly you
[16:17] start to asymptotically reach infinity. And so at 128 bits, you're already so close to infinity that the average person can't
[16:30] fathom it. It takes something like 100 million millennia for all the computers on the planet to be
[16:36] able to create a collision with that. So by the time you get to 256, it's nonsense at that point.
[16:46] Any sort of fundamental understanding of math that breaks 128 bits would also break 256 bits because it would be a fundamental revelation of the way that math works, and it's highly
[17:01] unlikely to happen. There's a claim that there's quantum computers.
[17:05] No one, as far as I'm aware, has ever been able to demonstrate a quantum computer, but if there were a quantum computer, it would break 256 just as easily as 128.
[17:17] So there's, yeah, it's- But your overall point is that 128 is good enough, 12 words is good enough, we don't
[17:25] need the 24, and we use 12 in Dash. Yeah, but no matter-
[17:31] Well, show us. Show me.
[17:33] Oh. Okay.
[17:35] Just one second. No matter how many words you use, it's still going to use a key expansion algorithm, which
[17:46] is basically just a hash. It's basically like, if you were to only allow yourself to reach the number 12, and then
[17:53] every time you got to 13, you just started counting over at 1, it's kind of the concept of a hash, except much more complex and at the scale of near to infinity, so it's really,
[18:02] really hard to reach the number that it rolls over at, but anyway, all of the keys, no matter which one you choose, they get key expanded with a standards compliant algorithm that's
[18:16] been around for decades, or at least longer than cryptocurrency has. All right, well, I say we look at some code, look at some documentation, look at the library.
[18:27] Okay, let me do this back now. Oh no, secret's revealed, I'm actually in a shed.
[18:38] Okay, so this is the command line tool, it's dash phrase, and if we just run it, it gives you help and tells you what you can do, and there's a generate command, and you can output
[18:52] the words to a file, so this is the basic usage of this. Anybody who's going to implement this for phone or for anything else, this is kind of
[19:01] the best tool in existence. There are actually some web tools that exist too that are pretty good, but this is kind
[19:09] of your go-to tool if you wanted to just explore and see, hey, if I wanted to create this library in another language, say, was it Swift for iOS or Kotlin for Android, this would be a
[19:27] good go-to. So you can generate the words, and then you can't really see right here because of my
[19:32] color scheme. Let me actually do this a different way so that my color scheme doesn't get in the way.
[19:40] Okay, so you can see here, this is a wallet. There's no account, there's no password, there's no username, there's no software.
[19:53] Software created it, but this is a wallet. You could use this.
[19:59] You shouldn't because now it's public, but you could use this. This is a wallet.
[20:03] Now what that wallet came from was a roll of the dice, and if we want to reverse it into what the roll of the dice was, and this is useful for debugging.
[20:11] I've got to stop you here because you used an analogy, and you know how I don't like analogies.
[20:16] Yeah. You said it's from a roll of the dice.
[20:18] I think that we should actually look at the code because it's only one page long. Yeah.
[20:25] Well, it's more than one page. It's one file.
[20:28] One file, right. All right, let me go into the code.
[20:32] Because it's not a roll of the dice. It's actually just calling into a random number generator.
[20:39] I'm just imagining the dice being in the computer, like on that movie Zoolander, where they're opening up a computer looking for the files.
[20:47] The files are in the computer. Yeah.
[20:51] So it's not rolling the dice actually is one way that entropy is generated. Also video of a lava lamp is that's how the NSA does it.
[21:05] You have a clean room, and you have a lava lamp, and you just video record the lava lamp, and you take the bits of the video frame, and you hash them because a lava lamp demonstrates
[21:13] turbulence and kind of the double pendulum problem. A double pendulum would be another way.
[21:19] Reading background microwave radiation from the sky, random.org uses that. So how a computer generates randomness is through, there's a variety of means, CPU cycle
[21:31] clocking. So there would be slight variations in the speed of your CPU.
[21:34] You've got a two gigahertz CPU, but it will have slight variations in it. So there's basically a really, really, really low level function on your computer that monitors
[21:44] things like keyboard input, network traffic, CPU variances, et cetera. It takes all of these little hiccups that are happening and records them as bits and
[21:54] aggregates them. That is something that is not exposed to us plebes.
[22:01] That is something that happens down in the operating system layer. >> Actually, you're in your command line interface.
[22:10] >> But here's the get random values, right? So that doesn't tell you much.
[22:13] Get random values. Essentially, it's the roll dice command.
[22:17] It's read something from the universe. >> Yes.
[22:22] >> And so get random -- sorry. Can you pull this up?
[22:27] >> Sorry. Yeah.
[22:29] >> Get random bytes, random values. And it's taking as an input a new Uint8 array of byte length.
[22:37] And the byte length is 128 by default, it looks like. So that's where -- >> Bit length is 128 divided to get the byte
[22:46] length. There actually should be a math.round in there as well, but I think it will work out either
[22:50] way, it rounds it on its own. >> Right.
[22:53] But the point is -- so maybe I was wrong with the 256, it's 128. >> But it expands to 256 because there is a well-known standard algorithm.
[23:02] For example, when you enter in your password on your computer, it doesn't store your password, it stores a hash, and one of the well-known, secure, highly audited algorithms for that
[23:14] is called pbkdf2, succeeds pbkdf1, and that's pb -- private -- I don't remember what it stands for.
[23:28] But the kdf is key derivation -- >> Function. >> Function, yeah.
[23:34] >> Yeah. >> So it's a very secure, well-known, wasn't invented in the cryptocurrency space, but
[23:44] that is what expands -- or shrinks -- whatever it is you give it, it transforms it into a different value using a pseudo -- essentially, it's a pseudorandom generator.
[23:54] So you give it real random, it uses the real random as a seed for a pseudorandom generator, that produces what's actually called the wallet seed, and then the wallet seed is put through
[24:05] another pseudorandom generator known as hierarchically deterministic keys, and that pseudorandom generator generates your keys.
[24:16] So that's the part where it's technical, and it sounds more confusing than it is, because it's basically -- it's just tables of information and rotating tables, and it's a Rube Goldberg
[24:28] machine on purpose, because it's supposed to appear to be random. And if it has a random seed, then it is random, but it's deterministically random, therefore
[24:36] pseudorandom. All right.
[24:39] So then I think the next question that somebody that's not initiated into this would wonder is like, okay, you're telling me it's a random number.
[24:50] How does it get from being a random number to a random string of 12 words? And that's the part that kind of, you know, at least I had to do a little research to
[25:05] figure out what that was doing, because if you tell me that a private key is basically just a random number, you know, that makes sense.
[25:13] But if you then throw a bunch of, you know, 12 words at me, I don't know how that works unless I've done the research.
[25:19] So I wanted to go over that really briefly. The process is called encoding.
[25:26] Encoding just means that you take some -- all things on the computer are represented in a number -- in a numeric format, essentially.
[25:33] You know, there's an electrical charge or there isn't an electrical charge. That's the bit.
[25:38] The bit is whether or not there's an electrical charge, and that electrical charge is actually an addressing scheme, kind of like a street sign almost.
[25:48] But anyway. And so what you're doing is you're just looking at what effectively becomes -- I hate to say
[25:55] this because it's such a cliche that it's not at all the way you see it on TV -- nobody programs in ones and zeroes.
[26:02] Ones and zeroes is just a way to store things either magnetically or electronically because it represents has a charge or doesn't have a charge.
[26:09] But anyway, stores things as ones and zeroes. And then you essentially are just looking that up in a table, right?
[26:14] So the ASCII character code set, you take eight of those ones and zeroes, you chunk them off, and then you look it up in a table.
[26:22] And if you were to do a Google search for the ASCII table, it will tell you what that is.
[26:28] Now, as you may have learned in high school math or may not remember, converting from one base of a number to another base of a number is just a matter of multiplication,
[26:39] addition, and division. So if I want to represent five in decimal, I can represent five in octal or in binary
[26:49] or anything else. And that's not even an encoding.
[26:52] That's just a straight-up interpretation. But it's just a matter of essentially how you count.
[26:58] The Romans used base 12, right? They got all the way to 12, and then they started back at one.
[27:04] And we use base 10. We get all the way to 10, and then we start back at one, except for things like time where
[27:09] we still use the Roman base 12. Things go to 60 because that's 5, 1, 2, 3, 4, 5.
[27:15] And then what is it, 1, 2, 3, 4, 5, 6, 7, 8. No, I'm doing it wrong.
[27:20] No, it's the inner knuckle, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12. So now you can count like a Roman.
[27:26] You can count 5, and you can count 12, and that gets you 60. So that's all base conversion.
[27:32] And it's just a matter of where do you go back to one when you count? Exactly.
[27:38] So actually, I wanted to just pause on that for a second. Yeah.
[27:45] Because my understanding was that those were the same thing, that converting into different number systems is the same as encoding.
[27:55] It's not an encoding. It's more of an interpretation.
[27:57] Yeah, that's what I'm saying. So like, for example, if you wanted to count to 5 in binary, you start with 0, right?
[28:08] I guess, let me get my fist on here. So you start with 0, and the first number is 0.
[28:14] Then you have 1. Then you have, instead of 2, you don't have a 2 in binary.
[28:19] So you have to go to 10. Right, exactly.
[28:22] And then 11, and then you don't have a 2. So the next number is 100, and then the next number is 101.
[28:30] So the number 5 in decimal, the decimal number 5 is 101 in binary. And the idea of these private key, these private, these 128 or 256-bit numbers, is that when
[28:46] you're encoding them into these words, instead of having 10 digits with the base 10 system that we all know, or 2 digits with the binary system, you have actually 2,048 words.
[29:04] So instead of counting up to 10, you would, instead of having 10, you actually literally have 2,048 different characters.
[29:14] So it's not, there's a subtle distinction here. So if I have 10 rocks that are on the ground, right, the rocks are on the ground, I can
[29:25] count the rocks any way I want. I can count it in base 2.
[29:29] I can count it in base 3. I can count it in base 16, hexadecimal.
[29:34] I can count it in base 10, normal English decimal. I can count it in base 12, the Roman way.
[29:42] But the rocks don't change. The rocks are stored, literally stored on the ground.
[29:49] And I can read the rocks in a different way, but the rocks are stored in whatever position they are.
[29:57] Now if I were to take the rocks and form the rocks into words, that would be more, and then the words we're supposed to signify, so if I were to take the rocks and rearrange
[30:09] the rocks into the letters T-W-O, that would be an encoding because I wouldn't be counting the rocks.
[30:18] I would be counting, I would be aggregating the rocks into letters and then using the letters to interpret a meaning.
[30:27] So that's kind of the difference between an encoding and what I was saying before as an interpretation.
[30:36] When we often think of hexadecimal, yes, the hexadecimal has been encoded because we don't actually save the hexadecimal in a new format.
[30:47] We don't rearrange the rocks. We don't rearrange the bits when it's just reading the hexadecimal.
[30:54] But if we want to save hexadecimal to a file, we are rearranging the bits. We are rearranging the rocks because we're actually, we're transcoding them into the
[31:04] ASCII character set. So the English letter A that gets printed on a piece of paper when you type it out and
[31:11] print it or gets sent in a text message, that, I don't remember what it is, it's something like the number 47.
[31:18] And so a program knows I'm supposed to use the ASCII table to interpret these numbers. And so when you get to the number 2 in ASCII, that's something like, I don't know, 52 plus
[31:33] 47 is the base because all the punctuation, the bunch of punctuation and control characters come first and then there's a couple other characters and then there's the numbers start.
[31:42] I don't remember exactly what the table is off the top of my head. But the number 2 is something like 120, whatever, don't quote me on that, right?
[31:52] But the number 2 is encoded. The number 2 doesn't actually represent 2.
[31:57] The number 2 is a bunch of bits that have been rearranged into a symbol that means 2 so that when it's sent as a text message, the program on the other side that it's not,
[32:07] that is interpreting the numbers as pictures, pulls out the picture of number 2 in whatever font and then displays that.
[32:17] And so that's where the difference is when we say we're encoding the words, you actually are looking up these bits in a table and what gets saved out to the file is not the number,
[32:29] it is the words and if you wanted to get the number, which actually it turns out the number is only used for the generation.
[32:35] We don't ever use that number again. The only reason you would use the original entropy number would be to validate that your
[32:44] implementation and another person's implementation match. So if somebody wanted to write this in Swift or write this in Kotlin, they would want to
[32:52] be able to get the entropy, which was the command I was just about to show a while back, they would want to get the entropy number and make sure that their encoding matches
[33:03] the same encoding for any given entropy number. But it is, it is, it's a subtle nuance difference, but it's, I mean, if you're a developer, it's
[33:13] a critical distinction. Yeah.
[33:15] Okay. So you have a website that, that uses this library to generate pass phrases as well.
[33:24] I think that might be a better way to demonstrate this than the command line. So this is actually not this library, but it is, so before I was involved with Dash
[33:37] or towards the beginning of getting involved with Dash, I was, I was noticing how much I liked the way that Brave Sync works with the recovery phrase.
[33:48] And so back at that time, I had created a library called pass phrase, and basically it's stripped of the cryptocurrency nomenclature to be a little bit more friendly so that people
[34:00] don't think, Oh, cryptocurrency, run away, run away. You know, so this, this actually is Dash phrase is a derivative work of pass phrase JS.
[34:12] It's the same algorithm, but it's just a different way of exposing it in terms of the documentation so that people can feel more comfortable about it and not feel like there's that cryptocurrency
[34:26] enigma around it. This is just a great way to use a pass phrase generator and a recovery phrase in the way
[34:34] that lots of software starting to use this technology. Cause it's just, it's a generally good standard.
[34:41] It's well thought out it, the word selection is a good word selection. The algorithm uses, uses standard algorithms under the hood.
[34:50] It's not weird, funky wonka doodle cryptocurrency stuff that later is revealed to be, you know, insecure like some of the, you know, the ripe MD stuff and some of the other things that
[34:59] I've complained about in the past that the cryptocurrency community said, rather than do what has been approved and been tested and been audited, we're going to make up our
[35:06] own stuff. So this is something where it's like, everything is based on really reasonable, really rational
[35:13] things. So there is here salt, uh, just ignore that.
[35:17] So I'm just going to point that out right away. Just ignore that in, in the regular day to day with the way we use cryptocurrencies.
[35:25] This is a, that the salt thing is just a legacy. It's a remnant of a former BIP that is not actually used in practice, but for the purposes
[35:33] of, um, doing any sort of implementation and passing a test suite, you would be using that as a developer, as a user, you don't need to worry about it.
[35:40] So as a user, uh, you just, this, this generates a random number. It looks the letters up in the table and that's what it does.
[35:49] It ends up generating 132 bits, but every word is 11 bits wide. And so the last, the last, uh, few bits are a checksum.
[36:01] So basically it takes the first 128 bits, adds them all together, multiplies them, divides them, comes out with a number that says, if you get this number, you probably had the
[36:10] same 12 words. You probably didn't make a mistake.
[36:13] So just a question on that, um, if somebody that, you know, uh, was dangerously, um, educated on this and thought to themselves, okay, so this is just generating random numbers from
[36:27] this dictionary of, uh, 2048 words, I'm just going to select my favorite, um, 12 words out of this list that I can maybe memorize.
[36:39] What's the peril of doing that? So one, one pair, I would say it's relatively low.
[36:47] Other than that, you actually don't get to choose the 12th word. Because if you choose the 12th word on your own, you're going to get a prompt in almost
[36:56] all software and some of it will just flat out not allow you to do it. You'll get a prompt that says, um, the checksum doesn't match.
[37:05] Do you want to continue anyway? Because the last four bits out of those 11 bits in the last word are representative of
[37:14] the checksum. So you could choose your favorite 12 words out of this list and then have it calculate
[37:21] the checksum for you. But you could not, uh, yeah, for your favorite 11 words.
[37:29] This, this library doesn't, wouldn't assist with that, but you're saying it's possible technically.
[37:34] Yeah. So as long as they pass the checksum, the software is not going to complain about it.
[37:42] And there, I don't think that there's any particular peril in it, but I don't know. I mean, I think that if, I don't know, somebody is going to tell you, well, there's going
[37:55] to be less entropy because it's words that you chose. Well, yes, but somebody would have to know that you chose the words rather than them
[38:03] being random. I just, I think that in practice there's probably an edge case where it could actually have
[38:13] less entropy. Like for example, if you chose the same word 11 times, zoo, zoo, zoo, zoo, zoo, zoo, zoo,
[38:20] zoo, zoo, zoo, wrong. Um, I don't know how many zoos I put in there, but if you, the, the zoomonic, one of the
[38:27] great test phrases, the zoomonic chosen because it's in, in a, if you were to look at it as the binary representation, it's all ones other than the couple of checksum bits.
[38:38] Well, while you're in the browser there, why don't you just bring up the, uh, the GitHub repo so that people can see the documentation for this particularly particular library and
[38:47] they'll know more about what you're talking about with this zoomonic. Yeah, let me go ahead and bring that up.
[38:55] So there's two repositories for this. I like to keep the CLI, the command line interface separate from the library.
[39:03] And the reason for this is the CLI tends to have creep where dependencies start to come in whenever you're building a web app or, or a command line app or any, you know, server
[39:14] app, whatever type of app it is, you're going to have dependency creep cause you're want to, going to want to be able to show additional things.
[39:21] So the CLI is separate so that if we, you know, were to add color output to the CLI, we don't want that dependency to become part of a dependency of the main library.
[39:31] Or if we wanted to add, you know, more user friendly features of auto, you know, auto completion or any of those types of niceties, we don't want, we don't want the cruft to
[39:42] creep into the library just because we wanted the debugging tool to be more friendly. Right.
[39:47] And the CLI is that command line interface? Yeah.
[39:51] Command line interface, CLI, command line, terminal, shell. But like everybody's computer already has a command line program on it, right?
[40:01] So what is, what is this actually, what is that? So this is the dash phrase program.
[40:07] So we answer this. So the, the CLI, when, when AJ is saying the CLI, he means the, the program that takes
[40:17] the the code, the raw library code, also called the SDK, and then gives that a wrap, gives that a feature that, that allows the user to interact with that library on the command
[40:32] line interface. Connects it to the keyboard and the screen.
[40:35] He's talking about the code. So if you wanted to make, like he was saying, that code spit out colored words to you in
[40:44] the CLI, rather than just black and white text, then that would add another dependency to the CLI program, not the command line interface that you're interacting with.
[40:55] So I think that you're, you were just confusing the, the, the program CLI versus the actual CLI that you're interacting with.
[41:04] The thing is called the terminal, right? The terminal is what connects the keyboard and the screen.
[41:12] And then inside the terminal is the shell. The shell is where you type commands and then the commands themselves are often referred
[41:19] to as CLIs. They are a command line interface for a library or for an API or for a function of the computer.
[41:32] So CLI is often referred to as any layer of that because it gets used incorrectly. Yeah.
[41:38] Basically. At the technical level, the stuff that has the buttons on it and the title and all that
[41:44] is called the terminal. That's what's interacting with the operating system.
[41:47] The shell is where you type in your commands, which is not visually distinct because it's the thing that interprets the commands and then finds them and then executes them.
[41:56] And then what we're looking at here is, is a command called Vim that allows me to view code.
[42:03] So that's what the layers are of it. Go back to the web browse real quick.
[42:08] I want to, I want you to show something. Okay.
[42:11] So, so this is the documentation for how to use this, the, the command line interface program.
[42:17] Yeah. This is the most, this is the most basic usage of it is you would generate some words.
[42:24] So wait, just stop turn the words into seed. Yep.
[42:28] So to, to use this you could go into the terminal and you could type the command dash phrase space generate with that with those options at the end.
[42:39] And that basically is, is calling the same code, the library code, the SDK code as the website if you're pretending that the website uses the same code, which it technically doesn't.
[42:54] It's a little bit of a different library, but it's a copy with a few changes. They're doing the same thing.
[43:00] Clicking the generate button on the website is doing the same thing as, as typing dash phrase generate.
[43:06] Yeah. It's the same thing.
[43:08] It's just a different interface. They call the same function.
[43:10] It's just one is connecting between the mouse and the screen. The other one's connecting between the keyboard and the screen.
[43:16] Right. Okay.
[43:18] Now one, one thing go back to the code itself, a scroll up or let me find out where I actually too many windows up and what am I going to do?
[43:32] I think you can scroll up right there. Well, okay.
[43:35] Yeah. I just want you to click into the code for the dash phrase dot JS.
[43:39] This is the actual code and just scroll through this just so people get an idea. Um, so there's some documentation up here that basically describes, this is for automated
[43:51] systems that can generate the webpage and whatnot, but the, this is basically here, the function names, what the, and then hyphen function description.
[43:59] And then a, a more technical description of the function is given this name over here. So, uh, and this is the top level view down at the very bottom.
[44:10] There's, there's a whole bunch more of that where it's like, okay, here's this describes this function in more detail, both technically and for documentation.
[44:18] Scroll down to the bottom again. Oh, sorry.
[44:20] Um, so basically we have what two, 329 lines, most of which are documentation and spaces. So this is not most of which, but, uh, you know, uh, a third.
[44:31] Okay. Uh, but yeah, like I'm just saying like for you programmers out there, you can understand
[44:38] what is happening here with 15 minutes of, you know, reading. Yeah.
[44:44] And there's no external libraries. This is it.
[44:48] This is all, this is the whole thing. Some programming languages you would need to bring in an external library for PBKDF2
[44:54] is part of the standard library in JavaScript, uh, as part of the standard crypto library and in all JavaScript platforms, whether you're looking at the browser or node or Dino or
[45:05] fun, uh, it's, it's all, that's all the same. That's something where you might need to bring in a dependency if you're doing Swift or Kotlin.
[45:14] I don't know if they have it in their standard library. There's also normalization.
[45:19] You actually don't need this if you're just doing English, but as you, um, are aware there's emojis and stuff like that.
[45:28] If you were doing accented characters, say there's a French dictionary for this as well. French has accented characters.
[45:35] Accented characters can be produced in three different ways. They're part of the Latin ASCII character set.
[45:40] They're also part of the Unicode, uh, dead character set. And then they're also part of the Unicode, uh, zero width join character set.
[45:50] So there's a, there's a normalization that if you wanted to use what the standard French dictionary for this, rather than the standard English dictionary for those 2048 words, uh,
[46:01] you would need to run a normalization because you don't know which accented E, uh, character set the keyboard is going to be using depending on what software, you know, the web browser
[46:13] versus, uh, uh, a wallet software, whatever. So there's that thing that would require a library in, uh, most other languages, I believe.
[46:24] And then other than that, I don't think anything else would require a library it's, it's, um, okay.
[46:35] So, so just do a, do a find on, on the page and find the word generate. It's right here.
[46:42] Okay. Let me, let me, sorry, I should have, uh, bumped this up a little bit so you can read
[46:46] it better. So I just wanted to let people know, like, okay, so dash phrase dot generate.
[46:52] Now, now, if you could go back to the documentation, like that, that's that function right there. Bam.
[46:57] Very small. Yeah.
[46:59] It's documentation. You see how, like the documentation for all of those functions.
[47:04] Yes. Yeah.
[47:06] It's, I, I did try to make sure that everything is for, for these things that I would consider production ready for release there, there are a few libraries in the dash tools that
[47:16] are not quite yet at this quality, but I'd say for the most part, um, dash, dash phrase is well-documented.
[47:23] Yeah. And it's pretty easy cause there's not a whole lot to, to choose from.
[47:34] It's very, very simple. Well that's kind of what I wanted to go over just, just those, those things that I wanted
[47:43] to see. I wanted people to see the code, see the documentation, um, understand a little bit what the generate
[47:50] function was doing and, um, just let people know that this is something that you can, you can kind of look into and understand, even if you're not a programmer, you probably
[48:01] could look at the code and make some sense of it so that you are, you are more familiar with how cryptocurrency works and the keys.
[48:10] And in subsequent, um, in subsequent episodes of this little series, we're going to discuss more about how you take this, these 12 words, convert that, uh, this, this library converts
[48:24] it into a seed, but then in subsequent episodes, we're going to talk about how the seed is then used to generate what you're normally seeing as addresses, um, and, uh, HD pads
[48:38] and things like that. So yeah, for, for people out there that are familiar with the term seed, you know, like
[48:45] you seed a random generator, use a real random generator to get some words. You take the words, you hash them using a specified method, predetermined method.
[48:58] That is your seed. And then the next, the next pseudo random generator uses that seed that came from true
[49:06] random data, hopefully, or test data, you know, and the reason that they're separate is because this stuff was developed at different times by different people.
[49:18] So one of the unfortunate things is that there are 10 different hashing functions, methodologies used throughout, you know, if you were to follow all the way from what, what I would
[49:29] call the start is your, your, your recovery phrase. When you install a wallet app or open up a desktop wallet app, the very first thing that
[49:37] happens is it's generating recovery phrase and it's saying, Hey, here's your recovery phrase, which again is kind of a misnomer cause it is the wallet.
[49:46] It's not just a recovery phrase. It's literally the wallet, but it's kind of hard to communicate that.
[49:50] So they call it recovery phrase cause that is easier on the brain. But you know, the first thing it's going to do is generate that phrase and then ask you
[50:01] to save it. Now, one thing that I wish more wallets did was be really clear that this is good to share
[50:09] with someone that you trust, that should manage your money in the case that you pass on. Or you know, this isn't something that you need to keep uber secret from everyone.
[50:21] This is something that you, if you're Edward Snowden, you're going to memorize it and that's the end of the story.
[50:26] But if you're the average person, people though, if you do share this, you really do need to trust the people because they literally have your wallet.
[50:32] Yeah. It's giving them access to your bank.
[50:34] It would be this, it'd be the same as adding them as a co-signer on your bank account. Yeah.
[50:39] And it's not just trusting that they don't have ill intentions against you. I think that's the easiest to determine rather it's trusting is this person capable of keeping
[50:47] these words a secret? Very good point.
[50:50] And not accidentally leaking it. TL wants to know, is this library crypto agnostic?
[50:55] So it could be used on Bitcoin or Dash testnet or Dash mainnet? Yeah, it is.
[51:01] So this really has nothing to do with cryptocurrencies other than it was developed in the cryptocurrency space.
[51:07] Right? It's like I said, it's a word list that was chosen by folks in the cryptocurrency community,
[51:13] but it was chosen well, and it's a hashing algorithm that predates the cryptocurrency community.
[51:20] And the word list was chosen, this is not a Dash specific word list. This is actually chosen by, I think the folks at Satoshi Labs, which makes the Tracer hardware.
[51:32] And they helped author BIP39, I believe. So this library is, you know, you can use this library for any cryptocurrency out there.
[51:44] Any cryptographic function that needs a seed. Yeah.
[51:47] But later ones, there are magic strings that you do have to make sure are these Dash specific? Are these Bitcoin specific?
[51:56] Yes. Those magic strings.
[51:58] AJ has done a very good job of documenting when and where those happen, but that's for a later week.
[52:02] Yep. Yep.
[52:04] Those happen in three other places, and they're not the same magic strings. Well, magic strings sounds exciting enough for me to come back for these future episodes.
[52:17] So it's lookups in a table. Sorry, I missed it.
[52:21] What was that, AJ? I said, it's just looking something up in a table.
[52:25] Oh. It's just having to look up three different tables to determine which one you want.
[52:29] No, don't tell me that. It's like seeing how movies are actually made or how they actually do magic tricks.
[52:33] Don't tell me. Do you ever watch Captain Disillusion?
[52:36] I think that's his name. Oh, no.
[52:38] I'll have to look him up. Oh, yeah.
[52:40] He's great. He'll ruin every movie for you.
[52:42] You've got to watch his show on his episode on The Navigator. It's going to bring you to tears.
[52:47] Captain Disillusion. Very good.
[52:49] Yeah. Okay.
[52:51] Well, thank you, AJ, for this breakdown today, and we will be breaking down more of these lightweight, small, zero-dependency Dash tools in future installations of this series.
[53:03] So absent any final comments, gents, how many? Nope.
[53:09] Okay. Then we will see you all next time, same place, same time.
[53:13] Thanks for watching. Okay.
[53:15] See you guys. Bye.