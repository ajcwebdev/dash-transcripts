---
showLink: "https://www.youtube.com/watch?v=YKWEPimMT3A"
slug: "dash-tools-part-3"
title: "Dash Tools #3: “DashHD” JavaScript SDK for BIP 32 Keys"
publishDate: "2023-05-08"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/YKWEPimMT3A/maxresdefault.webp"
---

AJ and Rion discuss the third installment of the Dash Tools series, focusing on Dash HD wallets and their role in the crypto ecosystem.

## Episode Summary

tl;dr: In this episode of Incubator Weekly, AJ and Rion dive into the third installment of the Dash Tools series, focusing on Dash HD (Hierarchical Deterministic) wallets. They provide a technical overview of how HD wallets work, explain the process of generating keys and addresses from a seed phrase using a standardized derivation path (BIP44), and discuss the importance of sharing extended public keys (XPUBs) for contact functionality. The discussion also covers the documentation and code examples in the Dash HD repository and explores potential improvements to the contact setup process and decentralized storage solutions using Dash masternodes.

## Chapters

00:00 - Critique of John Oliver's Crypto Episode
A video segment analyzes John Oliver's recent coverage of three major crypto industry disasters, arguing that he lacks important context when comparing these issues to similar events in traditional finance.

06:21 - Introduction to Dash Platform Developer Discussion
The main discussion begins with an introduction to the third installment of the Dash Tools series, focusing on Dash HD (Hierarchical Deterministic) wallets and their importance in the crypto space.

07:55 - Technical Overview of Dash HD and Hierarchical Deterministic Wallets
AJ provides a technical overview of how Dash HD wallets work, explaining the process of generating keys and addresses from a seed phrase using a standardized derivation path (BIP44).

22:25 - Sharing Extended Public Keys (XPUBs) for Contact Functionality
The discussion delves into the process of sharing extended public keys (XPUBs) with contacts to generate addresses for receiving payments while maintaining privacy and security.

31:24 - Walkthrough of Dash HD Documentation and Code Examples
AJ walks through the documentation and code examples provided in the Dash HD repository, explaining the different levels of complexity and the importance of making the code accessible and easily portable to other programming languages.

39:51 - Improving the Contact Setup Process and Decentralized Storage Solutions
The conversation concludes with a discussion on potential improvements to the contact setup process and the possibility of using decentralized storage solutions with Dash masternodes to store encrypted contact information.

## Transcript

[00:00] A new episode of Last Week Tonight features coverage of three of the crypto industry's most recent disasters.
[00:09] There is Terra, a cryptocurrency, Celsius, a crypto bank, and FTX, a crypto trading platform. In theory, they were supposed to be our next dollar, our next Bank of America, and our
[00:21] next stock exchange. While the accusations against these entities of unsound business practices do make for
[00:27] damning cases, the show's host, along with many other talking heads out there, try to make it sound as though the kinds of practices that led to these disasters are somehow unique
[00:39] to the cryptocurrency space. Is this true?
[00:42] Let's examine Oliver's claims. He starts with the collapse of the TerraLuna system, wherein people who bought the supposed
[00:50] stablecoin TerraUSD took on major losses when said system failed to keep its intended peg to the US dollar.
[00:58] The peg was lost, as Oliver correctly explains, because LunaCoins, the underlying asset meant to maintain the peg, were never suitable for the job to begin with.
[01:08] But doesn't this scheme, that is, backing a supposedly stable asset with an entirely unsuitable one, remind us of something else in recent history?
[01:19] Mortgage bonds are dog shit, CDOs are dog shit wrapped in cat shit. Yeah, that's right.
[01:25] And the 2008 financial crisis, precipitated by the very thing that Oliver accuses the TerraLuna system of, that is, the massive sale of supposedly stable assets, in this
[01:36] case US securities, that turned out to be backed by wholly unsuitable ones, in this case subprime mortgages.
[01:44] The telling difference between these two cases is that the major sellers of subprime mortgage-backed securities were bailed out by the US government in conjunction with the Federal Reserve and
[01:53] Walk Free today, while the major seller of TerraLuna tokens, Doquan, received no such bailout, is currently being held by police and may go to prison.
[02:06] Now to Oliver's second point, Celsius, the crypto bank and lender that filed for bankruptcy and declared itself unable to pay back billions in customer deposits.
[02:18] Banks not having enough cash on hand to cover withdrawals. Now where have we heard that story before?
[02:25] Oh yes, just last week. And a handful of weeks before that.
[02:31] Ooh, and shortly before that too. The main difference in this case is that legacy banks have something that crypto banks do
[02:38] not. That is, a relationship with the Federal Deposit Insurance Corporation, or FDIC.
[02:44] In each of the recent legacy bank failures, the FDIC, funded either indirectly through bank user fees or directly via loans from the federal government, has promised to make
[02:57] depositors whole again. Now that sounds pretty good though, right?
[03:01] That's a point in which the legacy system is definitely more trustworthy than the one run by crypto cowboys, right?
[03:09] Consider that the current coverage offered by the FDIC is $250,000 per account. But when the FDIC was first created in 1933, that amount was only $2,500.
[03:24] Now looking at those numbers, which is more likely? That for some unknown reason, bank users currently demand literally 100 times more insurance
[03:34] than they did only 90 years ago? Or that the U.S. dollar has lost nearly 100% of its purchasing power over that same time
[03:43] period? The FDIC may well have been key in keeping the legacy banking industry alive for as long
[03:50] as it has, but it has come at the near-total devaluation of the asset it maintains. Not really something to brag about.
[04:00] Now finally, Crypto Exchange FTX. The primary accusation here is that the entity, run by Sam Bankman Freed, or SBF for short,
[04:10] also filed for bankruptcy and also declared itself unable to pay back billions in customer deposits.
[04:17] Now, SBF was a darling among members of the federal government, making massive donations to the Biden campaign, being invited to speak at White House and Congressional Committee
[04:29] meetings, and even having multiple private chats with the head of the SEC, Gary Gensler. This extreme popularity, combined with the eventual massive implosion of his operations,
[04:43] takes a page straight out of the book of none other than the infamous fiat scammer Bernie Madoff.
[04:51] The danger is, regulation might give this sector more legitimacy. It'll make a risky investment look safe when it is clearly not, and that in turn might
[04:59] entice banks to start getting more involved in crypto, giving the sector even more legitimacy and also exposing all of us to its volatility.
[05:08] If regulated fiat markets are so much more legitimate than the supposedly unregulated crypto ones, how could it be that Bernie Madoff and Sam Bankman Freed were able to do essentially
[05:21] the same thing in each of them? All told, it appears that John Oliver isn't truthful in his claims that the crypto industry
[05:29] is somehow singularly and uniquely ripe for fraud and mismanagement when compared to the alternative.
[05:36] An examination of history suggests that the only real differences in crypto markets versus fiat ones is scale.
[05:44] That is, the crypto industry, currently in its infancy, suffers from a plethora of financial scandals, while the legacy financial industry, many more decades into its lifetime, suffers
[05:57] from even larger ones. Ideally, we'll create the education and tools to empower anyone who wants to, to avoid financial
[06:07] scandal wherever possible. With a backdrop of trustworthy money, accessible self-custody, and transparent exchanges, we
[06:17] just might have a chance. This is why we build.
[06:21] Hi, welcome to Incubator Weekly. Quick question.
[06:32] Can you hear me okay, AJ and Rion? Yep.
[06:36] Excellent. Wonderful.
[06:38] Well, we are back this week with the third installment of the Dash Tools series. And today we're covering Dash HD in particular.
[06:47] And in this case, the HD stands for Hierarchical Deterministic. So Rion, will you give us a quick overview as to why another hierarchical deterministic
[06:58] tool is useful in the space? Yeah, this is the continuation of the same theme that we've had for two weeks, basically.
[07:09] We wanted some lightweight tools that were standalone, that could act as good learning resources, good educational resources, and more importantly, perform well in a browser
[07:21] setting and in other compilation target settings, such as, you know, Webpack and BUN and things like that, that are coming up.
[07:31] So yeah, AJ can probably give you a better description of the technicals of that. But that's basically why I think this is an important project and an important part in
[07:43] the series, and the HD part specifically. This is kind of the culmination of the last two weeks, where the tools from Dash Phrase
[07:55] and Dash Keys are both used in this library to create a wallet that's very user friendly, and that can be backed up very easily.
[08:07] And yeah, we're going to learn more about HD pads and things like that. So let's jump right into, I think AJ can give us more of the technical description.
[08:20] All right. Well, first of all, my friends, let's pop a top and open focus.
[08:32] What Old Mountain Dew will help us explain things better. One second.
[08:42] All right. Now that I'm juiced, I can talk faster and take less time, right?
[08:47] No. So the 12 words that are the wallet...
[08:51] Let's zoom in if we can, AJ. Oh, yes.
[08:55] Thank you, dear. There we go.
[09:00] So the 12 words that are the wallet that we talked about with Dash Phrase goes through a technical term, key expansion, basically jumble it up and make it different in a secure
[09:15] way. And that results in our seed.
[09:19] So the 12 words turn into the seed, and the seed is actually what goes into the HD wallet. So we kind of resume from that point.
[09:29] And HD means hierarchically deterministic, but I also think that it ends up being a really nice term because HD, we think of things that are lossless or near lossless.
[09:41] And non-HD, we think of things that are lossy. So if you watch a standard definition movie on your HDTV, it looks like crap.
[09:52] And if you watch an HD movie on your HDTV, it looks pretty crisp. And the Dash HD is basically, if you have those 12 words, those 12 words are lossless.
[10:04] You print them out. You send them to a friend.
[10:06] Well, not a friend, but a legacy contact, I think, is the term, the appropriate term. You send them to a legacy contact.
[10:15] You do whatever. You keep those 12 words safe.
[10:20] Not in the sense of safe from bad guys, although you need to do that too, but safe is in the sense that you can use it to recover your wallet.
[10:28] So that's where the seed phrase comes from. And then the seed phrase is kind of hashed with, well, it's a kind of a, I don't know
[10:41] what the right term would be, but there's an HD path is what it's called. And the HD path, this is defined by the BIP, what is it, 32 and BIP 44 specs.
[10:56] So it is the address of your address. So this right here is what the software uses underneath in combination with this to produce
[11:10] keys that are safe to share with other people. Basically, this is what allows you to have contacts.
[11:16] And that refers to the Evo system as well. So when people talk about Evo and having contacts, the way that you have a contact is by taking
[11:29] your seed, mixing it up in a certain way with an HD path, and then getting out an X key pub that you share with that contact.
[11:39] And you share it typically in the form of a QR code, but the QR code is just the blocks that represent the same data.
[11:49] So this is the text version, but if we wanted to show what you share with somebody else, it'd be the QR version.
[11:55] And you can also embed this in a link and share it that way, or send it in a message that encapsulated in a way that the person doesn't necessarily see all of the text.
[12:03] But that's the essence of it, is that it walks down this path, it basically splits the path by the slashes here.
[12:13] And you'll notice there are some parts of the path that have an apostrophe. These are parts where you would not share even the public key with someone else.
[12:23] And then you have the parts that don't have an apostrophe, which would be the parts that you do share the public key with someone else.
[12:32] So they are known as the, I'm trying to think of the technical terms, I can't remember it off the top of my head.
[12:38] But it's essentially the, whether that entire segment will produce something that's considered to be private as a whole, even the public part, or public, meaning that the public part
[12:51] can be shared, not with the world, generally speaking, but with a specific contact. So in, oh, go ahead.
[12:59] - Okay, can I back up and just recap a little bit here? - Yes.
[13:04] - So the HD, Hierarchical Deterministic, the deterministic part is basically saying that when you have a seed, which is that AC27 number up above, when you have a seed, and remind
[13:21] me how many bits that is. - It's 256 bits.
[13:25] - Okay, so it's a 256-bit number. And it's basically saying, if you have this random seed, 256-bit number, and we want to,
[13:38] the whole premise behind this is we don't want address reuse. So we want to be able to create multiple addresses, but we only want to have one seed.
[13:49] And so the hierarchy part is that instead of just creating, you know, you could have, you could add some bit of randomness to create multiple addresses from this single seed in
[14:04] a deterministic way, but you also want that to be hierarchical, meaning it's organized in a certain way.
[14:11] And I think that's what these slashes mean, right? - Yeah.
[14:14] - Because those slashes kind of define the hierarchy. And the definition of the hierarchy is in that dip that you, or that bip that you referenced
[14:24] before. So that's just kind of the high level.
[14:28] But I also wanted to point out that when your HD key path, X key path, is a certain length, so you have the M44500, that results in what you're calling XPrivs and XPubs, and they
[14:48] have these prefixes of XPRV and XPUB. But when you extend that path, it's a little bit, it's different.
[14:55] Now it's creating WIFs and addresses, which we talked about last week. So are those the only two path lengths that matter, or could you have a shorter path that's
[15:08] just the M4450 part without the second zero, or are there only two types of key pairs that you get?
[15:19] - So according to BIP32, it's completely arbitrary. BIP32 does not specify any real structure.
[15:27] It just says, "Things are going to start with M, and it's going to have a slash, and there's going to be parts that are designated as purely private, and parts that are designated as
[15:37] partially public." But it does not define any structure in terms of what the numbers mean, or how long it is.
[15:44] So in practice, we use BIP44, and BIP44 defines that when it has one, two, three, four components, because the M doesn't really count, then that is an XPriv, XPUB path.
[16:03] And when it has one, two, three, four, five components, that is a WIF address path. So those are the only two that are useful, as far as I'm aware, in any-- well, then currently
[16:20] these aren't useful either, because currently no software actually uses these. There are spec that's defined.
[16:24] I think it's a glorious spec. I think it's something that actually was well thought out, well reasoned, and there are
[16:31] some bits about it from the technical implementation, I think they did a little bit of Rube Goldberging, but throw that in the noise, it's hashing anyway.
[16:42] This is a good specification, and I think that for the same reason that a lot of the Bitcoin specifications didn't take, mainly that people who understood that they were
[16:51] valuable and useful wanted to make sure that they didn't, I think that this hasn't really taken either.
[16:56] But the potential for this has been there, and there are one or two wallets that support it.
[17:04] And at the core, the Dash iOS wallet does support this for your main wallet, but not in the sense of Contacts.
[17:11] So Contacts, okay, so this has been used, this has been widely deployed for main accounts. This has not been deployed for Contacts, which is what it was intended for.
[17:21] Yeah. Okay, I just wanted to point out a couple of things.
[17:24] So the first thing that you mentioned is this is defined by a bit 44. That's what that 44 means in that XD, right after the M, that's what the 44 means.
[17:35] The next number means Dash. So when the Bitcoin creators were not maximalists, they actually wanted to support other coin
[17:46] types. And that's what that five is.
[17:49] And that just gives you an idea of how mature the Dash project is. We got the number five in this list.
[17:58] And I believe zero is testnet for all the coins, and number one is Bitcoin. And then number two and three and four.
[18:07] I don't know exactly what those are, but I think two of those are kind of like not even currently interesting projects anymore.
[18:15] We don't have to look it up. But yeah, just gives you an idea of how mature the Dash project is.
[18:21] We're number five on this list. And then the other thing I wanted to ask you, AJ, is when you're looking at this string,
[18:28] this M44500 string, is that actually in the code? Are you actually using that as a string, to use a coding term?
[18:41] Are you using it as a string in to hash the seed with, like literally just concatenating these strings or something like that, or how is this path actually used in the code?
[18:56] So it's hierarchical. So the M is ignored.
[19:00] The M is just kind of to say this is an HD path. And then the 44 is actually used as an integer, but the apostrophe is used as a flag because
[19:13] it's basically two code paths where it says derive this from the previous private key. So there is a, I guess the M stands for the master key, which is derived from the seed.
[19:28] So the seed isn't used directly, but the seed has a one-off algorithm that's very similar to the others, but slightly different because this is, well, the seed.
[19:40] So it generates the master key from the seed, and then in the next path, it uses the 44 to do part of the hashing, but it uses the tick mark to designate that this is a purely
[19:54] private hash. And so it uses the previous private key rather than using the previous public key.
[20:04] And then it generates a new private key and a new public key, and there's a variety of components to this that are internal mechanisms for how this thing carries forward, and some
[20:15] of them are embedded into these. And so these are kind of a sum of the state.
[20:22] This isn't a single value, but this is actually multiple values in a specific order so that it constructs the state of the hash system.
[20:36] And every time you go one layer down, it's a new algorithm, it's not a new algorithm, but it's a completely new key.
[20:48] So it's the same algorithm other than the very first one is tweaked slightly because there is no previous private key.
[20:56] It's working on the seed, so it has to convert the seed to a private key and then use that. As you go down, so it's bit 44 and then 5 is dash and then 0 is the account and then
[21:09] the next 0 is the usage. Now an account would also be a contact, so we would have some other mapping that's like
[21:17] 15 is John or 17 is @Rion or 258 is so and so at example.com. So we'd have some other mapping layer and Evo is putting that mapping layer in a, not
[21:37] a blockchain, but a persistent database. Maybe it is technically a blockchain.
[21:45] I'm not sure. I don't remember exactly what the spec is, but Evo is doing this too and they put the
[21:49] mapping layer down there. It also makes a lot of sense to just have that mapping layer in the software that you
[21:55] use and have it sync between the devices, but anyway, so you've got this, but then when you go sideways, it's different and the only place that it really makes sense to talk about
[22:07] going sideways for the purpose of this discussion is you go from 0 to 1 to 2 to 3 to 4 to 5 to 6 to 7, oh sorry, not there, here, the account, this one always stays 0.
[22:19] That's the usage and the usage is always 0 for this type of key. We could potentially use it for mixing to denote 0 is unmixed, 1 is mixed once and so
[22:31] forth, but that's something that's been talked about and I think is a really great idea, but for the purpose of this discussion right now, the account is the one that increments.
[22:40] So we can have account 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, whatever, up to 2 billion. And then as you go sideways on, so this produces different keys that all come from the same
[22:58] private key and we don't really use those. We use it down at this layer.
[23:03] This layer gives us one layer of separation from the origin private key and some people say that if you get enough private keys that are derived from a public key that it makes
[23:14] it possible to derive that public key. I would love someone who understands that better to explain it to me.
[23:22] As far as I could tell in the code when I was looking at it, I did not see how that would be the case, but I may have missed something or I may not have understood the mathematical
[23:33] concepts behind it well enough. But in any case, once we have the account generated, so we generate many accounts, then
[23:44] we generate the usage, which for all intents and purposes is always 0, at least in the contact scenario, and then we generate the address that would be, the contact, once they've
[23:54] received this public key, would generate addresses. So basically in their software, their software would keep track of the indexes of, hey, this
[24:03] address 0 has already been used, and then increment to address 1. This address 1 has already been used, increment to address 2.
[24:11] Address 2 hasn't been used yet. All of those are related in a sense to the key that's being used as the private key that
[24:27] came from this iteration. So whatever the child iteration is, there is a tweak to the private key of its parent
[24:37] that generates that child key. And this is the magic that allows you to have an XPUB that you can share with someone, is
[24:46] that the tweaking of the private key and the public key happen in step such that without knowing the private key, only knowing the public key, you can know that if you perform
[24:59] this mathematical operation on the private key, you can know what mathematical operation was performed on the public key, and therefore you can perform that mathematical operation
[25:10] on the public key independent of the private key. AJ, TL wants to know, is the XPUB key what you give to a "contact" so they can generate
[25:24] addresses to send DASH to you and get new keys every time? Yeah, exactly, exactly.
[25:31] So the XPUB, the software will, you know, you'll click create contact, and the software will create a path and map it to that contact in some way.
[25:41] And then that path will derive once, twice, three times, four times, and that gives you this XPUB.
[25:50] And then that XPUB, that XPUB encodes some of the information in it so that it doesn't need, the next time it actually doesn't need any of the other parts of the path.
[26:00] The only path, the only part of the path that it will know is its parent. It won't actually know that it's a DASH address, it won't actually know that it's derived from
[26:07] bit 44, it won't know anything about it except its direct parent. It'll know that it's direct parent was zero, and it will also know the depth that it's
[26:14] at. So it'll know that it is a depth five key.
[26:19] And so at that layer, the contact software would have to know that this is supposed to be for DASH because the information about DASH isn't encoded in it.
[26:31] But from there, it can take that XPUB and then it can just generate zero, then generate one, then generate two, just basically take that same key information, run it through
[26:42] the hashing algorithm as many times with a new number. And I do want to just point out one thing here, for anybody that's not aware.
[26:50] It would seem really ridiculous, like okay, if I know that there's this mathematical operation and it's done with the number one, well I could really easily guess that the next number
[27:01] is going to be two, so wouldn't I know what the next key is going to be even if I don't have all of the other pieces of information?
[27:10] And that answer would be no, because the way that hashing works, if you change a single bit of information, the output is changed in what appears to be a completely random
[27:24] way, which is why we use hashes for so many things related to security, because we can take a known value and produce a value that is not reversible.
[27:33] So you can know which value is going to come forward, but you can't tell what value it came from backwards.
[27:44] I think that we should scroll through this readme to see a little bit more of what documentation you have so that people can know what this repository can do for them.
[27:55] Okay. So the first part here is just showing you what this stuff looks like.
[27:59] So if you know what you're looking for and you see these things, you're like, ah, yes, this is the thing that I'm looking for.
[28:04] It also has examples, again, that are from the ZooMonik and the CatMonik, which are two sets of 12 words that were part of the original test spec, so that when you're developing
[28:17] against them, you can run the same tests that were run by Trezor and get the same results. And so all of the examples are based off of basically well-known test values, and those
[28:29] first ones I showed you were actually well-known, well, they're not well-known test values because the Trezor suite doesn't cover what they look like for Dash, but other than that, they are
[28:37] well-known test values. So this is library documentation, and it's kind of, this has been criticized, but I don't
[28:47] really know a better way. If somebody knows a better way, then by all means, open up a PR and help me.
[28:53] But it's the same information three different times. The first time is like, okay, I've done this before, I'm familiar with this in another
[29:01] library, I just need to know what this library looks like and calls it. And that's what this first one, two, three, four, five, six is, is it's like, you already
[29:10] know what you're doing, you've done this before, boom, there's your quick overview where you can copy and paste.
[29:16] If you're familiar with HD keys, this should be pretty familiar to you and it should make sense.
[29:21] Then the next one is, okay, if you're not that familiar and you need a little bit more of a refresher, it's the same thing, but it includes more of the steps like the predecessor
[29:30] step to get the seed. It also includes a little bit about error handling, because if you're familiar with
[29:35] HD keys, then you would know that they can throw errors because sometimes a particular number happens to go into a space that can't be used as a public key.
[29:48] So we've talked before about how a private key is any number that can produce a public key.
[29:53] But if there are a small set of numbers that for various reasons, usually either that they reach infinity or they go beyond the curve, they cannot produce a public key.
[30:06] And I don't know if you can know ahead of time what those numbers are because the way the hashing process works, I don't think that you can.
[30:13] So you actually need to do some, or you should do some error checking. In all likelihood, one customer will never have an error because the idea that they'd
[30:22] have a random number generated that happens to fall in the invalid range is vanishingly small.
[30:28] But across a near infinite number of customers with a near infinite number of transactions, eventually there will be an error that is not, it's an error in the sense that it's
[30:38] a mathematical impossibility, but you can just kind of skip that key or account or whatever it is and go on to the next one.
[30:45] So this one includes some of that error handling example in here as well. So if you try to derive an address and it fails, there should actually be some error
[30:55] handling on the error to make sure it's the right type of error. But anyway, just skip to the next one and continue.
[31:00] If you try that three times in a row, something else is wrong. The API has the from seed, from X key, from with, from adder, from X priv, from X pub,
[31:13] derive path, derive child. So it's some convenience methods here.
[31:18] Again we talk about the importance of being able to test if something is going to be valid. And then, yeah, so there was basically three different ways that we did that one thing.
[31:31] And then we're down into, I think, is this the glossary here? I think, yeah, this is basically the glossary, no, this is another, this is the top level
[31:41] exports of the API itself. Okay, so we're past examples and we're into just top level exports.
[31:47] And this is more for when you're trying to figure out what magic numbers mean, it's just really hard to find that information out sometimes.
[31:54] So I try to put it all in the README. So if you do a command F, a lot of this isn't necessarily meant to be read as much as it's
[32:00] meant to be searchable. So that if you hit command F or control F and type something in, it'll take you to the
[32:06] part that explains that thing. Then you've got references for the different functions and what the inputs and outputs
[32:13] look like and all that stuff. It's, I mean, it takes a big brain to get this stuff, or at least a lot of time.
[32:24] You have to expand your brain in order to fit all this in there. It's not simple.
[32:31] It is convoluted by design in kind of a good way, but it means that, yeah, it's difficult to grok this stuff.
[32:41] It's difficult to understand it. So there's a lot of examples and whatnot.
[32:46] So what I like about this documentation is that for all the JavaScript haters in the world, which there's a lot of them, including a lot of JavaScript haters on our own dash
[32:57] team, this is a good way. If you want to, you don't have any idea what this is all about, but you are a very good
[33:05] programmer in a specific language that's not JavaScript, you could look at this and know exactly how to port this over to a different language, right?
[33:15] It's sufficient documentation for you in one place to be able to port this over to say, you know, something like Python or Rust or Go or Zig or whatever.
[33:27] Yeah. The beauty of this, let me get back up to the top.
[33:30] I do want to show just a little bit of the code just to kind of give that perspective. But the beauty of this is that it's written in JavaScript the way that an absolute retard
[33:45] would write JavaScript. And there's no classes, there's no polymorphism, inheritance, I mean, basically all the computer
[33:56] science-y words that every language tries to capture a little bit differently, there's none of that in here.
[34:00] It's functions and it's objects. And when you say retard, I just want to make sure everybody knows what you mean by that
[34:06] because I know you well enough to know that you're talking about like, you know, there's that meme with the bell curve where on the left side of the bell curve there's the really
[34:17] dumb brain guy and he does a thing in a certain way. And then once you get to the middle of the bell curve, like your average intelligent
[34:24] person, it's this very complicated thing. And then once you get to the other side of the bell curve, the very, you're looking it
[34:31] up, I hope, the very intelligent person basically goes back to the way that the dumb person does it, which is really, it should be the right way to do it.
[34:41] Yeah. So, so this, this is it.
[34:45] So there's the, you know, the, the whoops, what happened? Something happened.
[34:50] There we go. Okay.
[34:52] There we go. Let's see if this one will open up.
[34:58] All right. Yeah.
[35:00] So you've got, you've got the caveman on the one side and then you've got the average person and then you've got the genius and the idea is that, that, yeah, that the average person
[35:10] is going to add in a lot of complexity and try to make it seem really smart. But both the caveman and the, the caveman, usually the caption is I'm dumb and have no
[35:19] idea what I'm doing, so I do it this way. And then the genius is something like, I realize that I'm really dumb and to compensate for
[35:28] it, I'm going to do it this way. So it's, yeah.
[35:33] And often in the meme, there's like one slight variation between the caveman and the genius and the, it's like in JavaScript, it's usually an error check or something like that when
[35:43] they show JavaScript examples of that meme. But yeah.
[35:46] But the idea is that you're, you're, you're bringing it back to like fundamentals in a very understandable approachable way.
[35:54] I hope so. I hope so.
[35:57] But I mean, one of the problems is that a lot of people are, you know, if you come out of bootcamp or something, you're so used to seeing all of the, the you know, complexity
[36:05] in the classes when you don't see it, sometimes it's a little jarring cause you're like looking for it, but then it's, it's not there.
[36:12] So there could be that. And you know, I'm open to criticism and somebody has a better way to organize the code by all
[36:17] means do it. But I think it's a heck of a lot better than what I had encountered when I, when I came
[36:20] here to two more things. So there's this walkthrough and this is if you're really not familiar with this and you'd
[36:29] like to understand it in a succinct, like I don't speak succinct, but I tried to write the documentation succinct.
[36:37] So if you wanted to go through this, the walkthrough is the, you're not familiar with this and you'd like to go through step-by-step copy and paste code, see how it works.
[36:46] Understand with more comments, more explanation, but still trying to be very succinct, no paragraphs, just individual sentences.
[36:55] And this is what the whole thing looks like. And then there's the glossary and the glossary is again, more for the, the command F ability
[37:03] of being able to go through and say, okay, what the heck does the term HD X key mean? What does HD path mean?
[37:11] And then again, single sentences and then single lines of code where possible. No paragraphs, everything is just single sentence anyway.
[37:21] So there's that. And then the code, a bunch of type information for tools, and then everything is basically
[37:31] just an object with functions for all of the utility functions and the same thing for the main functions.
[37:38] It's all just object with functions, object that contains functions calling on an object. So a very, almost, I hate, I don't know what the, a zig style.
[37:51] I would say C style because C is a very function oriented programming language. You don't really have objects, but then not having any name spacing at all is really,
[38:00] really bad and very difficult to work around. So it's not, it's got, it's got that benefit of everything is just a function that accepts
[38:07] an object and the objects as much as possible are very, very simple objects that just have keys and values in them or are values like the integer or the, the buffer or whatever.
[38:21] So the functions... I think I'll start calling you Dewey, AJ.
[38:26] Dewey? Yeah.
[38:28] Like Dewey decimal system. I don't know.
[38:31] A person who organizes libraries and organizes libraries. Dewey.
[38:36] Yes. Anyway, so here, hopefully you can kind of see that most of these functions fit in a
[38:43] single screen and I tried to make naming consistent between this and the other libraries. And I also tried to make it so that there's, that the functions are the right size.
[38:54] Cause if you make things too small, then you have to spend all your time just going back and forth between functions to understand what anything does.
[39:01] But if you make them too big and then it's difficult to tell where the pieces are. And so I did my best to, to orient this in such a way that code that changes together
[39:13] stays together and code that could be used independently is in its own function. And there are some very small abstractions that we could, we could potentially deem useless
[39:23] abstractions. Meaning that the abstraction adds more complexity than it adds value.
[39:30] So there's, you know, this is a very, very tiny abstraction, but there's a reason that I, that I did it when I did it.
[39:37] And it's often for naming conventions or consistency or something like that. So I tried my best.
[39:43] I feel like this is a heck of a lot better than what there was before. Well here's a question of how potentially it could be even better.
[39:51] A J T L wants to know a BIP 44 HD wallets seem like a great path forward, but the setup between users seems like unnecessary overhead.
[40:02] Do you think that perhaps there may be a way that HD paths could work without contact setup? Well, I need more information to understand from your point of view, what you're saying,
[40:17] because my headspace and your headspace are probably different. So let me, let me read this again.
[40:24] And I will, while you're reading that, I'll, I'll give my staff at this answer. Um, I, and also introduce next week or next, next show, I don't know if it's going to be
[40:33] next week, but next show, um, we, we have another library Dewey decimal guy, um, that is a wallet and the wallet is supposed to, uh, make this, make that contact creation
[40:51] very simple. And just with the caveat that this is not the same as, uh, dash core groups contacting
[40:58] system. This is basically just exchanging X pubs.
[41:01] Uh, and we do have a wallet library that's supposed to make that a very simple. So yes, it, it could be complex to do, um, this contact setup.
[41:13] It might seem like that, but that's why we've created another library for that. And I'll add to that, I think the minimum complexity, and again, we have to be practical.
[41:25] We have to think about the real world, not about Edward Snowden. Yes.
[41:29] Edward Snowden exists. Yes.
[41:31] There you, you're not Edward Snowden though. You might feel like you're Edward Snowden and you might want to follow the same practices
[41:36] as Edward Snowden. And that's up to you as an individual to kind of navigate that.
[41:42] And we shouldn't make it hard for someone to behave in the manner of Edward Snowden. If that's what gives them a sense of purpose in their life, but the average person's not
[41:52] Edward Snowden and we're not trying to protect from those types of things. The most important thing is that we have relationships with other people that we exchange with and
[42:02] that we can reliably count on those. So the simplest method would be literally to take a screenshot of the QR code and send
[42:12] it via text message, just like you do with Venmo. I think that that is the level that we need to start from and we can add more onto that.
[42:23] Also I envision a world and Rion kind of turned me onto this idea, but I envision a world where we have 4,000 servers that sit and do nothing useful almost, right?
[42:33] They run a couple of hashes every few minutes. They're doing almost nothing.
[42:38] What if we could take those 4,000 servers and make them of more use to the network? What if we could have services that run on them where you do store some of your information
[42:51] encrypted on them and you pay for that in a, let's say, a monthly way or a yearly way or whatever.
[43:00] What you would have to do in this scenario is you would have to basically pick three services at random, pay each of them whatever the fee is, and then publish your information
[43:11] to them and keep a local storage of which servers you had picked or have some mechanism to quickly query among the 4,000 servers, which ones have your information.
[43:23] And then if one of those servers disappears, your software would periodically just need to query to find out, "Hey, is my stuff still where I think it is?" and then be able to
[43:37] pay another server, and I'm imagining these fees would be very small, like 50 cents per year or something, if you'll pardon my fiat, but you can just publish multiple copies of
[43:51] something to a couple of places and have a really, really, really, really high probability that it's going to be there forever.
[43:59] You don't need a perfect probability, and if you feel like your data is more valuable, your contact information is more valuable, then pay $2 a year and store it on four or
[44:13] five or six or whatever. If you feel like you need a hundred copies, just pay for a hundred copies.
[44:18] And right now, what we have, what DCG is building is the default is just going to be you can store whatever you store, whatever you want to store, it's going to be stored on every
[44:31] single server, and it's a longer discussion we won't get into today about how we might ensure that and make it, first of all, more affordable because you're not storing on 4,000,
[44:46] you're storing on 4 or 10 or whatever. That's a totally different discussion, but worth having because we do want to have those
[44:57] fees a little bit lower, and it does seem a little excessive on the Snowden side that we're going to be storing that data on 4,000 servers for time and all eternity.
[45:07] When I'm dead, I don't really care about my contacts anymore, you know what I'm saying? If I stop paying, it's because I'm dead, and if I'm dead, then you don't need to store
[45:17] my data. Right.
[45:19] And even the solution that we're going for with Dash Platform Evolution, it will allow people to remove that storage and get refunded for a portion of what you paid originally,
[45:30] so that is a good part of the design system that we've already got with Evolution. I think we have one more question, and we should probably wrap up.
[45:40] Do we will find market for such storage? Will we find a market for such storage?
[45:45] Yeah, that's the question. I'm not sure, but I think that there is a market for, there definitely is a market.
[45:54] The only question is what size that market is, and this is going to kind of be a, if you build it, they will come.
[46:04] If you build it, they might come, who knows, but we're building it one way or the other. I'm going to say that, I mean, I don't know whether that question was directed towards
[46:13] the Evo scenario or the scenario that I outlined. I'm going to say with the scenario I outlined, we know there's a market for that because
[46:20] that's the way the market currently works, right? You look at something like, let's take S3, and I don't necessarily think that S3 is the
[46:29] bee's knees, but as a protocol, I would say that S3 is one of the smarter things that's happened.
[46:35] The storage backing for something like S3, if you want to look this up, there's things like Ceph FS, basically there's three copies of any item, and so you're paying for that.
[46:46] The reason that S3 is so expensive is because you're paying for three copies of the thing, right?
[46:52] So there's already, the technology for this already exists. The market for this already exists.
[46:57] It's already been proven. Is there a competitive advantage?
[47:02] Probably not, except for people who are Dash users. There's probably a competitive advantage there.
[47:08] So if we have Dash users, then yes, we'll have people that want to spend Dash to be able to have similar storage that is, in some ways, more censorship resistant.
[47:20] Okay. Well, that was an interesting topic to end on, and I know that we'll talk more about
[47:28] that in the future, and as Rion said, next week we will either be covering more of Dash tools or potentially talking more specifically about the application of these Dash tools,
[47:39] which in this case is for the incubator-specific developed wallet that we covered some five, six weeks ago.
[47:46] So that will be fun. We look forward to seeing you then, and until that time, take care.