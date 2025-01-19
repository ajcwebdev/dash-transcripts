---
showLink: "https://www.youtube.com/watch?v=91t9jrki0rc"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Decoding Platform: Rust -⟩ JS | Incubator WEEKLY"
description: ""
publishDate: "2024-09-10"
coverImage: "https://i.ytimg.com/vi/91t9jrki0rc/sddefault.jpg?v=66de52c6"
---

## Song

### ChatGPT o1

1. Rust And Reason
2. Chain Of Signatures
3. From Blocks To Bytes

Verse

Traversing synergy from proof of work to staked authority refined
Dash forging forward with visionary code so seamlessly aligned
We strip verbose clutter in bin code constructs meticulously designed
Testing fixtures matching rust outputs with veracity combined
Every annotation conjures versions that shape a novel storyline
Striving for smaller payloads that still sparkle with cryptographic shine
Identity creation mapped to this architecture supremely entwined
No extraneous data in signable streams we keep transitions defined

Chorus

We strive for clarity bridging languages with fervent energy
Pushing the threshold of minimal overhead with synergy
Expanding the dash horizon in unstoppable resiliency
Creating new directions through platform's code transparency

Verse

From gRPC channels we harness bytes in methodical streams
Excluding fields that hamper signatures forging robust schemes
A JavaScript library emerges fueling these unstoppable dreams
Manual transformations bring forth expansions beyond what it seems
Transition structures gleaned from enumerations with elaborate themes
No repeated rhymes no stammering bars each syllable redeems
Synergizing dash with browsers enabling cryptographic regimes
We unify dev mindsets hooking rust logic to front end beams

Chorus

We strive for clarity bridging languages with fervent energy
Pushing the threshold of minimal overhead with synergy
Expanding the dash horizon in unstoppable resiliency
Creating new directions through platform's code transparency

Verse

One chain for payments another for data weaving trust so complete
Offering swift actions and minimal fees forging progress elite
Identity births from these coded instructions with no sign of defeat
Rust macros cradle complexities while JS echoes the beat
Ensuring each field aligns with logic that cannot retreat
Versioned expansions await but we stand sturdy on repeated feats
No punctuation needed each phrase resonates discreet
Collective ambition guides the synergy networks cannot delete

Bridge

Evolving the schema with unstoppable flow forging the future so bright
Nodes verifying each cryptic fragment intensifying insight
Inviting a legion of creators to unify code day and night
Shifting the landscape of decentralized brilliance in ascending flight

Chorus

We strive for clarity bridging languages with fervent energy
Pushing the threshold of minimal overhead with synergy
Expanding the dash horizon in unstoppable resiliency
Creating new directions through platform's code transparency

## Episode Description

Two Rust enthusiasts explore how to encode Dash Platform’s Rust-based data structures in JavaScript, highlighting the nuances of serialization, versioning, and toolchains.

## Episode Summary

This conversation focuses on bridging Dash Platform’s Rust-based code into JavaScript, demonstrating how two developers tackle the intricacies of serialization and encoding for identity creation. Early on, they outline Dash’s evolution from its proof-of-work beginnings to the newer proof-of-stake platform responsible for handling more complex data. The discussion reveals how fields are converted from Rust to JavaScript, delving into signable versus signed versions of transitions and showcasing the importance of minimizing bandwidth usage. Significant emphasis is placed on the advantages and challenges of bin code—a compact Rust-oriented format—compared to more verbose encodings like JSON. The speakers also touch on potential future improvements, such as automating code generation to reduce manual upkeep. By highlighting test scenarios that confirm whether the JavaScript matches the Rust outputs, the conversation underscores the project’s progress toward a flexible framework for interacting with Dash Platform through multiple languages.

## Chapters

### 00:00 - 06:00 Introduction and Project Background

In the opening moments, the host welcomes a Rust developer named Matt, providing context about Dash Platform and its layered approach. They explain how Dash originally emerged from Bitcoin, focusing on fast, low-fee payments, and eventually expanded into a second blockchain with Rust-based tooling. The conversation outlines Dash’s dual structure, where one blockchain handles payments and another maintains data integrity. While Bitcoin remains largely a speculative store of value, Dash aims to make day-to-day transactions practical and affordable for users worldwide.

The speakers also introduce the motivation behind bridging Dash Platform’s Rust code into JavaScript. They acknowledge the large community of web developers who could benefit from straightforward tools to interface with Dash’s new network features. At this stage, it becomes evident how speed, security, and minimal bandwidth form the backbone of Dash’s design, driving a need for carefully optimized serialization. By highlighting the importance of documentation, they set the stage for explaining the intricacies of bin code and signable messages.

### 06:00 - 12:00 Meeting Matt and the Rust Meetup Connection

Here, Matt shares how he became involved through a Utah Rust meetup, a space frequently frequented by AJ, the original project instigator. Matt’s background includes various programming languages and a longstanding interest in cryptocurrency, although this project marks one of his first hands-on experiences with Dash. The pair discuss AJ’s knack for organizing developer communities, revealing how creative collaborations often emerge in local tech circles.

They also address Rust’s growing popularity and how it attracted curious participants at the meetup. Matt describes how Rust macros, annotations, and code generation can be mysterious or challenging for beginners. He underscores the complexity of handling advanced features like enumerations and derived traits. This section highlights not only the technical leaps required to make the project functional, but also the collaborative environment that fosters these new developments.

### 12:00 - 18:00 Dash’s Dual-Chain Concept and Data Storage

The conversation shifts to a deeper explanation of Dash’s dual-layer architecture. One chain remains proof-of-work for traditional transactions, while another proof-of-stake chain maintains the state for user-generated data. This allows developers to store structured data and build applications on top of a decentralized network. The host emphasizes how the new platform extends beyond just payments, inviting developers to consider public, permissionless data storage for various projects.

During this span, they highlight how Dash Platform’s second chain is run by specialized nodes called Evo nodes. The discussion covers how these nodes validate and store data contracts, illustrating the potential for broader development. By detailing how data immutability and consensus-driven design can enhance application reliability, they set the groundwork for understanding the importance of consistent serialization across languages and nodes.

### 18:00 - 24:00 Decoding Rust Serialization and BIN Code Basics

Attention shifts to the technical challenges of decoding Rust-based serialization, specifically with bin code. Matt describes how bin code encodes data in an ultra-compact manner, lacking self-describing markers like those found in JSON. For JavaScript developers, this presents a learning curve, as the encoding demands precise knowledge of what fields to expect and in what order. They point out that Rust’s standard tools, like SERDE, are commonly used for flexible serialization, but bin code pushes it further by compressing data to a minimal footprint.

This section captures the thrill—and occasional frustration—of unraveling a system that seems opaque at first glance. Because bin code does not embed field names, developers must rely on references from the Rust structs or the actual code generating the bytes. Despite the steep learning, they affirm that bin code suits Dash’s performance priorities, especially given the need for minimized bandwidth and quick cryptographic checks.

### 24:00 - 30:00 Mapping Rust Structures into JavaScript

Here, they discuss the practical steps Matt took to replicate Rust’s serialization logic in JavaScript. The conversation reveals how entire structures were copied, then carefully re-implemented to ensure the same byte layout. Detailed code snippets show how signable message variants exclude certain fields, requiring multiple versions of the same struct. Such intricacies illustrate the interplay between Rust’s powerful macros and JavaScript’s more manual approach.

In describing these solutions, the speakers highlight the importance of passing specific test fixtures. By comparing side-by-side output from the Rust code and the JavaScript code, they confirm both are generating identical byte arrays. This thorough verification process underscores the precision needed to maintain network consensus and reliability. Despite the complexity, Matt finds ways to simplify the process and plan for future enhancements.

### 30:00 - 36:00 Testing and Validating the Approach

During this segment, they shift focus to the crucial testing methodology ensuring consistency between Rust and JavaScript. They share how, by capturing raw bytes from the Rust codebase and injecting them as fixtures, they can validate JavaScript’s output. Each step of encoding, signing, and decoding is verified against Rust’s “source of truth.” This gives the team confidence that developers using JavaScript libraries will stay in sync with Dash’s protocol requirements.

The speakers emphasize the significance of extensive test coverage, especially in cryptographic or blockchain-related code, where small errors can lead to major security or consensus issues. They also remark on how generating identical hashes or signatures demands precision at every step. Through these tests, they uncover minor tweaks and better understand how Rust’s bin code handles versioning and optional fields.

### 36:00 - 42:00 Identities, Data Contracts, and Future Plans

The focus broadens to Dash Platform’s key abstractions: identities, data contracts, and documents. Creating an identity is the first step for any user to interact with the network, requiring a cryptographic link between the entity and their set of public-private keys. They reiterate that bin code is vital here, shrinking the payload for swift verification. Beyond identities, developers can define data contracts (schematic definitions of structured data) and publish documents that adhere to those schemas.

Moving forward, they plan to replicate this approach for additional transition types, such as data contracts and document updates. Matt notes that while the current progress is promising, a fully featured library will require expansions and possible automation to avoid copying every struct manually. The discussion remains optimistic, highlighting how incremental steps in rewriting Rust logic make the network more accessible for new developers.

### 42:00 - 48:00 Wrap-Up and Upcoming Initiatives

In the final segment, the host thanks Matt for his rapid progress, expressing excitement about integrating these JavaScript tools with Dash’s ecosystem. They discuss passing the work along to AJ for further testing and possibly tackling other elements of the platform. Matt references potential code automation avenues to ease maintenance, but acknowledges it may not be a high priority until the platform stabilizes further.

The episode closes with a teaser for future content focusing on more visually engaging projects like transaction explorers. By wrapping up, they celebrate how bridging Rust and JavaScript positions Dash for broader developer adoption. The conversation underscores that while the foundation is laid, there remain plenty of opportunities to refine, enhance, and grow Dash’s developer resources in the coming weeks and months.

## Transcript

[00:00] Welcome, everybody, to today's episode of Incubator Weekly. Today, I have on the show,
[00:07] Matt Peterson. How's it going, Matt?
[00:09] Going good.
[00:10] Good. Nobody in the Dash community has probably seen you except for potentially AJ for
[00:10] sure,
[00:20] because that's how we got to know you. Today, the title of the show today
[00:20] is, let me just
[00:27] actually just check, just make sure. It's decoding platform, Rust to JavaScript. That's
[00:34] kind of like a little bit of a play on words, kind of literal, kind
[00:34] of not literal. Decoding
[00:38] platform is something that we are trying to do in the general sense of what's
[00:38] actually going on in
[00:48] platform, but also in the literal sense of decoding bytes and things like that and
[00:48] encoding. That's
[00:55] part of the reason that we brought you on, Matt. So I'm going to go
[00:55] ahead and share my screen to
[01:00] set up the purpose for what you're doing. And then we'll talk a little bit
[01:00] about who you are.
[01:08] So just a little bit of background. We in the Incubator are trying to build
[01:08] a
[01:22] lightweight library to talk with Dash Platform. Once again, just as an overview with
[01:32] the work that we've done in my corner of the incubator, we have been putting
[01:32] that in this DashHive
[01:40] repository. It's mostly work that AJ has done. And mostly up until this point, we've
[01:40] been dealing with
[01:49] layer one or actually, I'm not sure if I love the term layers. I'm kind
[01:49] of in Joel's camp on this.
[01:57] I'll just say the core blockchain, which is a proof of work blockchain. Most of
[01:57] the work has been
[02:02] interfacing and having libraries that interface with that core payments technology of Dash.
[02:08] But we're also trying to get a library to interact with Dash Platform itself, which
[02:08] is
[02:17] a separate blockchain. And I'm kind of explaining this both to the audience, but also
[02:17] to you, Matt,
[02:24] because you're not super familiar with Dash. We've brought you in as a ringer to
[02:24] do a specific
[02:31] thing that AJ was having some trouble with. And I'll talk about that in a
[02:31] little bit more in detail.
[02:36] But still in overview land, Dash Platform is a separate blockchain,
[02:43] but run by the same nodes, or at least a subset of the nodes that
[02:43] run the core blockchain, run a separate
[02:50] blockchain that is a proof of stake blockchain. And they use those nodes that are
[02:50] running this proof
[02:58] of stake blockchain are called Evo nodes. And they run additional services in addition to
[03:06] the core blockchain. They're running what are so called platform services like DAPI, DAPI, the
[03:06] Dash API,
[03:18] or the decentralized API, whatever you want to call it. That's one. And then Dash
[03:18] Drive is another one.
[03:28] And basically what it is, is it gives the opportunity for developers to store data,
[03:28] structured data on
[03:40] these Dash platform nodes and that all come to distribute consensus and sync up the
[03:40] state of that blockchain
[03:52] in terms of data and not just payment state, which is what the core blockchain
[03:52] does, is it's doing something
[04:00] similar, but just for payments alone. And this is general purpose data storage. And we'll
[04:00] talk a little
[04:08] bit more about that as well. But part of Dash platform is that the serialization,
[04:08] the service, the DAPI
[04:21] service is a GRPC service. And we needed somebody to be able to encode and
[04:21] decode messages for GRPC. And so that's,
[04:36] the high level of what AJ was trying to do. It's a lot of, a
[04:36] lot of that is based on the Rust code base.
[04:45] And AJ is not a Rust developer. So he typed in a message to the
[04:45] Rust meetup, which I'll share a little
[04:56] bit about here. And I'll ask you to talk a little bit about. Utah is,
[04:56] Utah has quite a few
[05:06] meetups in general. And one of those meetups is the Rust meetup. And so AJ
[05:06] popped in and said, Hey,
[05:13] I'm having some trouble with figuring out some encoding and decoding stuff in a Rust
[05:13] code base
[05:20] that I, I'd like some help on. Can you tell us a little bit about
[05:20] that message that AJ
[05:26] sent to you and what he was having, asking you to do? And the, the
[05:26] short, like the,
[05:34] the end result is that you were able to do that. And we're going to
[05:34] talk about that later in the show,
[05:40] what you did and that you got some, some tests passing that he set up.
[05:40] But first of all, just give us an
[05:47] introduction to yourself, Matt, who are you? And what are you doing in the Rust
[05:47] meetup? What's your
[05:56] interest in, in Rust? And yeah, just tell us about yourself.
[05:59] All right. So yeah, my name is Matt. I've been a software engineer for something
[05:59] like 15 years now.
[06:11] And I have been going to the Utah Rust meetup for a little while, which
[06:11] AJ actually used to like run
[06:20] the thing, which I think it's kind of funny that he was running the Utah
[06:20] Rust meetup and not actually
[06:24] being a Rust developer. He is now running the Zig meetup, which is like right
[06:24] next door. But anyway,
[06:37] yeah, he likes to get meetups going. He's, he's more of like a social guy.
[06:37] He just likes,
[06:42] you know, he likes to look into all the different programming languages. And so he
[06:42] just organized this.
[06:47] I, I, I recognize this clean cut guy because way back, like three or four
[06:47] years ago, Dash was actually
[06:56] trying to figure out, okay, originally platform was written in JavaScript on the backend.
[07:06] And because there was a lot of rage back then, like good kind of rage,
[07:06] like, yeah, it's all the rage.
[07:12] There's probably a lot of rage in the bad sense now for JavaScript on the
[07:12] backend. But long story short,
[07:20] we started it in JavaScript, and then we were going to start rewriting it in
[07:20] either Go or Rust. And so
[07:27] we were looking into these. That's when I started looking into Rust personally. And I
[07:27] joined the meetup.
[07:33] Then I talked with, with this event organizer, clean cut, what's his real name? His,
[07:33] anyway, he
[07:41] I don't even remember. He's got a pretty well known Rust, Udemy, I think Udemy
[07:41] course.
[07:47] Yes. Yeah.
[07:48] Yeah.
[07:48] So he's one of the, like, beginner and game dev and rust kind of things.
[07:48] He's, he does a lot of that.
[07:54] Yeah. So chances are several people in dash that, um, might have, might have taken
[07:54] his course because I
[08:03] was, I got him to give me access to like preview access to a course
[08:03] that he was making at the time, like
[08:10] on Rust and I shared a link to it. And so several people might have
[08:10] taken that course. That's,
[08:15] that's this guy right here. And then, um, yeah, it looks like the meetup has
[08:15] like 500 plus members now.
[08:22] And, uh, you're one of those guys. So yeah, continue on with your story. Sorry,
[08:22] I cut you off.
[08:28] Well, that's all right. So anyway, I, I met AJ because I went to the
[08:28] meetup, um, several times.
[08:35] Um, and I've even, I've even popped into the Zig meetup a couple of times
[08:35] too, because, um, the,
[08:43] the Rust meetup, uh, in the beginning, there was a little bit of more advanced
[08:43] things in there,
[08:48] but it seems to have been, it seems to be moving a little bit more
[08:48] towards, um, beginners now, uh,
[08:52] mostly towards just the, the people that are actually showing up. There seems to be
[08:52] a lot of
[08:56] Rust beginners that are also interested in like either beginning embedded things, um, or beginning
[08:56] game
[09:03] development. Um, so that seems to be where a lot of the interest is now.
[09:03] Um, but yeah, I'm, uh,
[09:10] I'm interested in, in, um, programming languages a lot too. Um, I like picking up
[09:10] new, uh, languages when
[09:16] they come up. So of course, when Rust, uh, showed up on the scene, I
[09:16] was very excited about that and using
[09:23] it a lot. Um, uh, unfortunately only in personal projects, I still have yet to
[09:23] really be able to
[09:30] work on a, uh, uh, a Rust project for work other than, uh, Dash now,
[09:30] except that I'm still not actually
[09:38] working on the Rust code, but anyway. Um, yeah.
[09:44] Halawi does say, yes, I took the course. Thank you. So that's cool. Um, yeah.
[09:44] So let's, let's jump into,
[09:51] uh, what you were working on, uh, unless you want to, wanted to say anything
[09:51] more about your,
[09:56] your background, what your interests are. I actually, I did want to ask you specifically,
[10:00] uh, we talked a little bit, I'm getting to know you right now. Uh, and
[10:00] I figured why not just open it up
[10:05] to the incubator, uh, audience in general. Um, but yeah, I, I would like to
[10:05] know what your, what your
[10:11] overall interest and, and experience is with cryptocurrency in general.
[10:16] Right. Yeah. So I was fairly early on in the Bitcoin investor game. I did
[10:16] not have a ton of
[10:24] cash at the time. I was pretty young, but I did invest in Bitcoin when
[10:24] it was around $400. It was
[10:30] the first time I ever invested. I then subsequently made a, a series of really
[10:30] stupid trading
[10:35] decisions and ended up losing most of it. So I'm not, I'm not particularly wealthy
[10:35] for it. I did make
[10:42] a small amount of cash off of it that went into, um, house down payments
[10:42] mostly. Um, but nothing too
[10:47] extreme, but I've been in the, I've been in the interest in, um, Bitcoin for,
[10:47] uh, most of its lifetime.
[10:54] Um, but I haven't actually done a lot in, in, uh, like the code, uh,
[10:54] strangely enough. Um, I never really
[11:05] uh, had much of an opportunity to actually work on anything. Like I never got
[11:05] into any of the crypto
[11:10] startups or anything like that. Um, so anyway, I've had some, uh, some kind of,
[11:10] I've had my eye
[11:17] on, on crypto for a while. I've read a lot about it, but I actually
[11:17] haven't done a lot of actual coding
[11:22] in that space. Um, Yeah. Well, most, uh, most of the code bases, Bitcoin itself
[11:22] is a C++ code base.
[11:30] It's the reference for that most people use dash itself is a fork of Bitcoin.
[11:30] And so our main client,
[11:39] I don't know, it kind of bothers me that we call them clients, but people
[11:39] do, they're more like servers.
[11:45] Um, most of, uh, the, the, the reference, uh, implementation of the node, the node,
[11:45] a node
[11:51] is a probably even a better term because it's, it's both a client and the
[11:51] server, honestly.
[11:55] Uh, but, uh, yeah, that's in C++ as well. But because we have this new
[11:55] project that is completely new
[12:05] blockchain that does have a native bridge between the two blockchains between our core C++
[12:05] proof of
[12:13] work chain and our, um, platform rust primarily proof of stake blockchain. Although there is
[12:13] a strong
[12:23] component, uh, that's written in go, the actual consensus mechanism is written in go, but
[12:23] platform
[12:29] is, is written mostly in rust. So there's all sorts of, you know, if you,
[12:29] if you're a JavaScript developer,
[12:35] if you're a go developer, if you're a rust developer, if you're C++ developer, you
[12:35] know,
[12:40] we've even got Python and all sorts of like Swift and Kotlin and, uh, we,
[12:40] we've got it all. So pretty
[12:46] much anybody who's interested in, and, and has experience with any language can, can do
[12:46] something
[12:51] in dash. And that's one of my main roles that I'm trying to take on
[12:51] is trying to, to get developers
[12:58] to take a look at dash, uh, see what we're doing and see why it's
[12:58] interesting. Uh, just a brief
[13:04] comment on dash versus Bitcoin, since you have a little bit of background with Bitcoin,
[13:08] um, dash is essentially trying to take the torch that Satoshi Nakamoto, creator of Bitcoin
[13:08] himself
[13:16] started. Um, it was originally intended to be for payments. Um, appear like the, the,
[13:16] the title of the
[13:26] white paper, it was peer to peer electronic cash or peer to peer digital cash
[13:26] to use a different word.
[13:33] word dash itself comes from it's a portmanteau of digital and cash dash. And so
[13:33] we are continuing
[13:40] that vision of peer to peer payments and not just trying to use it as
[13:40] a speculative asset that hopefully
[13:47] will go up and give you more fiat currency, uh, after you sell it. So
[13:47] we were trying to tell you
[13:54] it doesn't work unless you're really, really, really, really good at trading and you're not.
[13:58] Yeah. Yeah. Most people are going to lose that game. Yeah. Cause most, most of
[13:58] us don't have as
[14:06] much information as, as the big whales. Um, but yeah, like we, we want this
[14:06] to be actually a currency
[14:14] that's traded peer to peer and has low fees and is very, very fast and
[14:14] very secure, those kinds of
[14:21] things. Uh, so that's, that's still our vision. It seems like Bitcoin has given up
[14:21] on, on that. And
[14:25] it's mostly just trying to, they don't mind that the fees are high. They don't
[14:25] mind that, um, people don't
[14:32] actually use it. People it's actually considered a virtue to just buy it and hold
[14:32] it and not actually
[14:38] use it dashes is different than that. Um, especially with dash platform, we're trying to
[14:38] target, um,
[14:45] another use case, which is developers. If they want, if they have an application specifically
[14:45] where data is
[14:54] considered public, um, and they want to open that data up to anybody to draw
[14:54] from that data, to build
[15:04] on that data, to add to that data, um, to pull that data into their
[15:04] applications, uh, in a permissionless way,
[15:13] that's what dash platform is. And, um, let's go ahead and get your screen share
[15:13] started now that we've, uh,
[15:21] got some background and, uh, I've given you a little high level on dash what
[15:21] dash platform is.
[15:26] Let's, let's get a little closer to what you're working on. Um, uh, and while
[15:26] you're getting that
[15:35] going, I will also just give a little bit more background about what we're trying
[15:35] to accomplish
[15:41] here. So the, the way that people interact with dash platform is primarily with, uh,
[15:41] initially with
[15:50] mobile applications, our, our, um, our swift, um, iOS app and our Android apps, they
[15:50] have there, they have
[16:04] code bases that import, um, WASM bindings. And that's what our JavaScript library does as
[16:04] well. We have a dash,
[16:18] uh, on NPM D A S H that, that library, if you looked up on
[16:18] that library, um, that's what we're using,
[16:26] uh, that has WASM bindings as well. But, uh, I think JavaScript is particularly important
[16:26] because it gives
[16:35] access to web developers and there are way, way, way more web developers and web
[16:35] applications
[16:42] than, um, um, both desktop and mobile application developers. And so I think that JavaScript
[16:42] deserves
[16:53] to be, to have a native protocol that is calling into, um, into dash platform
[16:53] and not needing, uh, WASM
[17:04] some bindings, uh, for one reason, because it will be a lot more performance, um,
[17:04] in terms of both bandwidth
[17:13] and, uh, download size, things like that. Uh, but also just speed, um, of interacting
[17:13] and doing transit,
[17:21] doing transactions with dash platform. So that's why I have AJ working on this JavaScript
[17:21] library that
[17:29] would natively talking to dash platform, specifically natively talking to the nodes that are running
[17:35] the gRPC service on the platform, uh, Evo nodes. And so he was having some
[17:35] trouble with the encoding and
[17:46] decoding of messages that are, um, um, gRPC messages. So back to you now. Yeah.
[17:46] Let me, let me see if I can
[17:56] add a little to that. So, um, and I also want to mention by the
[17:56] way, that I learned about dash for the
[18:02] first time about a week ago when I, uh, got, uh, put onto this project,
[18:02] when AJ put out a call for help
[18:07] in the Utah rust discord. Um, so, uh, a lot of this is going to
[18:07] be based on my, uh, very limited understanding
[18:15] of what I did just to try to get this part done. Um, so I
[18:15] could be wrong at any point here. Um,
[18:21] my understanding is, is that, uh, there is a gRPC, um, layer that is like
[18:21] the first layer that, um,
[18:30] the nodes interact with, and then almost as soon as the art gRPC message gets
[18:30] decoded,
[18:36] it seems like the only thing inside is just a pile of bytes. Um, like
[18:36] it's just using a, a byte array
[18:42] as, um, the internals of the message. And then everything inside of that gRPC message
[18:42] is then, um,
[18:49] encoded in a different way. Um, and it seems like either the spec is out
[18:49] of date or maybe just not easy
[18:56] to read. Um, but there was some, uh, understanding that the, uh, encoding of the
[18:56] messages on the inside
[19:04] was either JSON or CBOAR or, um, something along those lines. Um, and not very,
[19:04] uh, very obviously
[19:12] understandable, at least by, uh, AJ. Um,
[19:16] my understanding of that is that, yeah, the, the spec isn't, isn't really documented yet.
[19:16] The
[19:24] implementation is the spec at this point and the implementation is rust. And so, yeah,
[19:24] that's,
[19:31] that's why like you understanding rust can look at the, everything's open source, right? So
[19:31] we can
[19:37] look at the rust code base and, and actually, um, uh, Sam Westrich, uh, Quantum
[19:37] Explorer, he did,
[19:43] he gave us some of the raw bytes that we were, that were passing across
[19:43] over the wire. Um, I don't know
[19:51] if you actually looked into that branch of the rust code base where he put
[19:51] some logs to log that out.
[19:56] I did. In fact, I added my own too.
[19:58] You added some, okay. So you got that, you got that rust code base going,
[19:58] built, added some of
[20:04] your own debugging statements. So you're, uh, I'm trying to get you up to the
[20:04] point where obviously
[20:11] you're not going to understand, uh, in one week, what, what Quantum Explorer, Sam, uh,
[20:11] CTO of dash
[20:17] core group has been working on for years. Um, but at least you could get
[20:17] the code base up and running
[20:22] and put some log statements in and, and just kind of tinker around with things
[20:22] and see how reverse
[20:28] engineer how it's working. Uh, because right now, like I don't want to bother dash
[20:28] core group with,
[20:35] uh, things if I don't have to. And so that's why it's good to have
[20:35] you as, as a rust developer,
[20:41] knowing the tooling, because it's not just knowing the language, it's knowing all the tooling
[20:41] and being
[20:46] able to get that stuff up and going that we, that we need. And even
[20:46] rust has many, uh, layers to it,
[20:53] which, uh, in this case, the, the layers is what made it really difficult to
[20:53] understand how the
[20:58] encoding was working. Um, so yeah, so I've got, for example, um, one of the
[20:58] identity create transition
[21:08] structs in here. Um, and, uh, this, this enum is a version denum. So the
[21:08] actual data inside is marked
[21:17] under this version zero so that they can, um, like add a new version if
[21:17] they need to evolve the, the,
[21:23] um, the layout of destruct or whatever information is inside it. Um, so, um, this
[21:23] is basically all you
[21:34] get when it comes to like, how, how is this, how is this serialized? Um,
[21:34] there's all of these extra,
[21:40] um, annotations on there. Um, uh, specifically all of these that end up deriving, like
[21:40] creating new code
[21:48] based on all of the rest of this. Um, so, um, for somebody who is
[21:48] not a seasoned rust developer,
[21:58] um, this could be, uh, quite confusing and overwhelming to see that, like there's areas
[22:03] of the code that, that, that just calls a signable bytes method on this struct
[22:03] and, uh, that, uh,
[22:12] function doesn't seem to exist. Um, so it can be kind of confusing, uh, as
[22:12] to where this is coming
[22:17] from. Can you bump up your font just a little bit? Because I know, I
[22:17] think that we're streaming
[22:21] in kind of low quality. Um, so it probably will help it to bump it
[22:21] up a bit. Is that good? Do you think?
[22:28] Yeah. So for a JavaScript developer, these, these hash, um, these hash things could be
[22:28] considered
[22:35] kind of like decorators in TypeScript. Is that, is that right? Yeah. Pretty similar. Okay.
[22:35] So they,
[22:42] they essentially do additional things, um, with the, with the actual functions and, and code
[22:42] below it.
[22:51] Right now, and this, the thing that gets interesting here is that this would even
[22:51] be a little bit
[22:57] confusing for a normal Rust developer because, um, it seems that they're, they have, uh,
[23:05] not been happy with the standard Saturday, um, serialize and deserialize macros, um, that people
[23:05] use
[23:16] in Rust. Um, uh, and it seems to be because they wanted an easy way
[23:16] of encoding in a couple of different
[23:24] formats or a couple of different, like, um, uh, ways of encoding the same message.
[23:24] So for example,
[23:32] the way that I'm going to point out this is, um, in the identity create
[23:32] transit transition, um,
[23:39] message or struct, I don't know what you want to call this. Um, there is
[23:39] a marker in here that says,
[23:47] exclude from the signature hash. So when you generate a signable version of this,
[23:56] um, it is going to run through the normal serialization code, except it's going to
[23:56] skip
[24:01] these, these two, um, fields, um, which I gathered mostly just from, uh, reading the,
[24:01] the code and a little
[24:10] bit of intuition here, um, and then verifying it in the actual, uh, testing of
[24:10] the JavaScript code.
[24:17] Um, but this is something that is not part of the normal, um, Rust, uh,
[24:17] ecosystem.
[24:24] So, so when you say, uh, the, the term that you've used a couple of
[24:24] times is CERDE,
[24:32] it's at the bottom right green, that's, that stands for CERDE serialized deserialize.
[24:38] Yep. And that's like, that is thing, right? So Rust has a split between, um,
[24:38] the,
[24:46] the ability to serialize and deserialize a struct and the actual encoding that it is
[24:46] serialized into.
[24:54] Um, so like, for example, you often want to have a struct that can be
[24:54] serialized in, uh, multiple formats.
[25:01] Um, so you might be able to want to serialize it into JSON and XML
[25:01] and, um, like CBOAR or BSON or various
[25:09] different other kinds of encodings. Um, and, uh, in Rust, you have to use code
[25:09] generation for this.
[25:18] Um, there's no way of just like reading out the list of fields and then
[25:18] just doing something like you can
[25:25] in Go or, or JavaScript. Um, in Rust, the only way to get the list
[25:25] of fields is by using one of these
[25:31] derived macros or some other sort of code generating macro. Um, and so you don't
[25:31] want to have a different
[25:38] macro for, um, encode and decode job, JSON, encode and decode XML, encode and decode,
[25:38] um, CBOAR, encode and
[25:46] decode VSON and all of the other, the different formats that you might want to
[25:46] use. And so they have, uh,
[25:53] SERDE, which is a, um, a kind of a generic serialized deserialize, um, that is
[25:53] encoding agnostic.
[26:02] So what it does is it expects a serializer when you pass, uh, when you,
[26:02] when you call the serialized
[26:09] function and the serialized function just tells the serializer, Hey, I have a field. Can
[26:09] you serialize
[26:16] this field however you want? And then here's the next field and serialize that however
[26:16] you want.
[26:19] And then the serializer is like the bin code version or the JSON version. It
[26:19] handles the actual like
[26:25] conversion to bytes. Okay. Just, just real quick. Um, I know a lot of developers
[26:25] will know these terms,
[26:32] but for the semi-technical or non-technical people, can you give a, an explanation of just
[26:32] what,
[26:38] what it means, uh, what serialization means, what encoding, uh, means, uh, just, just so
[26:38] that
[26:46] everybody can kind of have a rough idea of what you're talking about.
[26:49] Yeah, sure. So when, when you have this struct here, um, the, the general expectation
[26:49] is, is that the
[26:57] compiler will know where all of these things are. But other than that, there's no
[26:57] guarantee of what the
[27:04] actual real layout is in memory, or at least there's not a guarantee at this
[27:04] level. And there's no,
[27:10] in particular, there's no guarantee that the representation of the struct in memory will be
[27:15] the same between any two machines, um, or any two versions of the same code.
[27:15] Um, and so, uh,
[27:24] the serializing and deserializing is a way of, of converting this possibly unknown
[27:32] in memory representation to some specific sequence of bytes that can be read, um,
[27:38] and understood by any machine, by any version of the code that can be easily
[27:38] transmitted across the
[27:44] network. Um, this struct stuff can also include like things like pointers that are only
[27:44] valid for the one
[27:50] instance of it in memory right now. So you can't even send that over the,
[27:50] over the, over the network.
[27:55] So yeah, the, the, the general idea of serializing is I have some information, let's
[27:55] put it into a known
[28:01] format so that it can be transmitted to some other machine, um, some other piece
[28:01] of code somewhere else.
[28:07] Okay. And the encoding and decoding, how is that different or what, what, what's, what's
[28:07] that part?
[28:15] Yeah. So, and encoding, um, is there are just lots of different ways that that
[28:15] could be represented.
[28:21] Um, so JSON is a common one, um, that is fairly verbose and, and easy
[28:21] to use by lots of tools. It's
[28:30] JavaScript's kind of default, um, representation. Um, but when it comes to rust or when
[28:30] it comes to
[28:38] transmitting things over the network, um, JSON is very kind of verbose, it takes a
[28:38] lot more space than
[28:45] it really needs to. Um, and so here in, uh, this code base, for example,
[28:45] they've opted to use bin code,
[28:53] which is a fairly straightforward way of just like, just, just write it down in
[28:53] the most concise
[29:02] byte format that you could possibly use. Um, and, uh, that means that they, their
[29:02] messages take up a lot
[29:11] less space, which is especially important for these, um, cryptocurrency nodes when they're passing these
[29:17] messages back and forth, when they have to do a lot of cryptographic hashing to
[29:17] verify that things are
[29:22] correct. You don't want to have a large amount of bytes that they have to
[29:22] hash, um, because that just,
[29:27] that's just a lot of extra work. And so there's, there's a lot of emphasis
[29:27] in wanting to shrink the number
[29:31] of bytes done that they have to care about to as small as is reasonable,
[29:31] um, to make the work on
[29:38] these nodes, um, as low as possible and the storage requirements as low as, as
[29:38] reasonable.
[29:43] Right. And as far as I can understand it, there's, uh, the only downside to
[29:43] that might be that, uh,
[29:51] it's not as, it's not documented as explicitly because you kind of have to know,
[29:51] okay, what was omitted?
[29:58] What was, what's included? What order are these in? And so it's less self-documented. And
[29:58] so that's why
[30:05] it can be difficult if you don't already know, um, some data that is actually
[30:05] passing and fulfilling the
[30:14] required specification. Um, then you, it's hard to tell how to re-implement this in another
[30:14] language,
[30:22] for example, and that was exactly, that's the challenge. And, um, I guess maybe we
[30:22] could move
[30:27] into that if you're, if you're ready, what we're trying to do is we had,
[30:27] we had, we, we did get
[30:33] from Sam. Okay. Here's, and from that logging and the extra logging that you did,
[30:33] we, we know what bites
[30:40] are going across the wire. And so we can kind of recreate, um, we can
[30:40] have a test fixture
[30:48] that, um, says we know that this works in the rust, uh, that was, uh,
[30:48] uh, created by the rust code base.
[30:57] Now let's create a JavaScript code base that does the same thing and see if
[30:57] it passes the same test.
[31:02] So do you want to walk us through that? Sure. So, um, so the, uh,
[31:02] the description that I was given
[31:12] is essentially we need to be able to encode, um, state transitions to be able
[31:12] to transmit them to
[31:20] other nodes, possibly decoding them as well. Um, bin code being something that was invented
[31:20] for the rust
[31:26] ecosystem. Um, there are like hints of other people using it in JavaScript, but doesn't
[31:26] seem to be any
[31:32] standard way of doing it. Um, especially since, um, as I mentioned before, bin code
[31:32] is very concise.
[31:39] Uh, and one of the ways that it's very concise is it does not include
[31:39] any self-identifying information
[31:45] inside it at all. So for example, you can, you can open up, uh, anything
[31:45] in a JSON encoding. Um,
[31:54] and it has like field names and it has braces to delimit where objects start
[31:54] and end. Um, bin code has
[32:00] none of that. It doesn't tell you what you should be expecting next. It doesn't
[32:00] tell you what field
[32:05] you're at. It doesn't tell you what struct you're looking at. You just expected to
[32:05] know what you're
[32:09] decoding already. Um, and so I had to translate all of these struct encodings into
[32:09] JavaScript, um,
[32:17] because that is the, the, like how you decode and encode, um, with, uh, bin
[32:17] code. So I wrote, um,
[32:26] a few foundation bits, which is mostly the, the, the core, like how you encode
[32:26] the basic integers,
[32:33] um, and bytes. Um, so I have this quick little helper class, um, that is,
[32:33] uh, it's essentially a
[32:41] little bit of helpers to help you stream data into and out of a data
[32:41] view, which normally can't be
[32:46] appended to. Um, so I have a little bit of stuff for that. Um, and
[32:46] then I have a bunch of infrastructure
[32:53] that, um, tries to create, um, an object that has encode and decode, um, implementations
[32:53] bundled
[33:00] together, um, which acts a little bit like a type, um, because then I can
[33:00] write down a struct definition.
[33:09] Let me see if I can find this exact one.
[33:11] So we have the signable version and the, uh, signed version, as I was talking
[33:11] about before, that has the,
[33:19] um, the signatures as part of it, um, the signable version that does not. And
[33:19] so we can see here that
[33:26] there's this magic version constant, um, which pops up, uh, uh, as part of, um,
[33:26] I think it's actually
[33:34] built into the platform signable code or no, sorry, it's part of the, it's part
[33:34] of the enum. Um,
[33:41] but you can see here that I've just translated. So this was, this was literally
[33:41] a copy and paste and then
[33:46] a little bit of editing, um, where I copied this into here and then, um,
[33:46] the, there's this struct, um,
[33:55] constructor that, uh, creates the, um, code to encode and decode the struct based on
[33:55] this definition.
[34:02] Um, and, uh,
[34:08] I'm getting lost in my own thoughts here. Um, and the enum that wraps it,
[34:08] um, which is the version without the V zero over here.
[34:15] Um,
[34:16] Yeah. So is that, does that make any sense? Um, should I go into more
[34:16] detail here, um, how this works?
[34:27] Um,
[34:31] I think, I think maybe, um, maybe we could jump to like quote unquote cut
[34:31] to the chase, not because the
[34:41] details aren't important, but just to show people where it's going, you did, you ran
[34:41] a, you wrote a
[34:48] test, right? A test file. Let's talk about that. And then we can dig into
[34:48] details from that launching
[34:56] point. Um, start from the end, so to speak, uh, of like what you were
[34:56] given as this is truth. And how
[35:06] can we test that the JavaScript code is producing the truth?
[35:10] All right. So, um, this is a minor modification of the, um, the, the test
[35:10] that was created. Um,
[35:21] the test, uh, the, they were calling it a test fixture, but that doesn't, that's
[35:21] not actually
[35:28] what I would call this. Um, but anyway, just the test of like, can we,
[35:28] can we encode the same message?
[35:35] Can we sign it the same way and produce the exact same bytes as the
[35:35] official rest implementation?
[35:40] So the official rest implementation has this nice test, um, which tests how, uh, uh,
[35:40] encoding and decoding
[35:49] and signing of the, uh, create transition, um, message works. And as part of that,
[35:49] um, they, uh,
[35:57] added these print statements for us where they, they generated the signable bytes of the
[35:57] state
[36:02] transition and then in, and hex encoded them, uh, and printed them out.
[36:06] Now, is that, is that part of that special branch that, uh, that, that, uh,
[36:06] Sam wrote or did you write
[36:14] write this? Okay. I see the blue, I see the little blue. That means this
[36:14] is.
[36:18] I believe that is just formatting. I believe that I ran the formatter or something
[36:18] and it, uh, uh,
[36:26] just changed the, uh, order of, uh, it just changed the white space a little
[36:26] bit. Um,
[36:32] but anyway, this is just like, this is the test to show how state transition,
[36:32] um, serializing and signing
[36:40] and all that works. And so, uh, uh, this can be run pretty easily just
[36:40] by running the rest tests.
[36:49] Um, and then you just turn off the, uh, capture so that you can actually
[36:49] see the standard output.
[36:55] Um, and then I just copied those bites from that test fixture and a few
[36:55] of them from my own runs of this
[37:02] over here. And some of the, uh, messages also can generate a, uh, like canonical
[37:02] JSON encoding, um,
[37:11] which I'm not entirely sure what that's used for. Um, but, uh, maybe it's used
[37:11] for communication
[37:17] because this is part of the WASM bindings or it's used in the WASM bindings.
[37:17] So anyway, I have the, um,
[37:23] bytes of an actual, uh, actually I should go down to the bottom here. Um,
[37:28] so I have the bytes of an actual state transition here, um, as generated by
[37:28] the rest code. And then
[37:35] we test, um, whether it can be, uh, encoded, um, whether we can, sorry, first
[37:35] of all, whether we can
[37:43] decode it into a, uh, a valid JavaScript object. And then whether we can then
[37:43] re-encode it back to
[37:51] exactly the same bytes to test that the encoding and decoding is working correctly. Um,
[37:51] and there
[37:57] are other cases too, where, um, I don't have it in this case because it
[37:57] seems that state transitions
[38:03] don't have the JSON code in, um, in Rust, but there are places where like
[38:03] these, um, identity public keys,
[38:13] uh, do have a, uh, uh, specified JSON encoding. And so in those cases, I
[38:13] have the actual JSON encoding,
[38:20] um, pasted in here as well. And we tested it, um, with some minor tweaking
[38:20] that we get the exact same
[38:28] JSON out of, uh, the decoding process as the, uh, the Rust code also generates
[38:28] to prove that we're doing
[38:35] it exactly the same way. Okay. Well, should we run the test and see it
[38:35] work? Uh, sure.
[38:42] So I actually have it running here in, um, um, as my test here. Um,
[38:42] so it runs automatically when I
[38:51] save the code. Um, but you can see here that we've got all three of
[38:51] those passing. Okay. So the first
[38:57] test is it should encode and decode identity public key. Uh, then it should encode
[38:57] and decode the identifier
[39:04] and it should encode and decode the state transition. Now, I don't know if those
[39:04] mean that much to you,
[39:09] but, um, the main goal that I had AJ working on was, um, with this
[39:09] overall integration of trying to get
[39:18] a native JavaScript, um, library that can talk with a platform node and do platform
[39:18] stuff. The first and
[39:31] only thing that we were focusing on was the identity, create transition, uh, or transaction.
[39:31] Uh, transition
[39:39] is tip is just a term that is used for, um, like an instruction to
[39:39] one of these, um, Evo nodes that
[39:48] ask it to change the state of platform and identity, creating an identity is the
[39:48] first thing that you need
[39:56] to do on dash platform, uh, because that's what, uh, allows you to pay for
[39:56] things, um, and interact
[40:08] with dash platform. So that's like the first thing, the other things, and this is
[40:08] just for you, Matt,
[40:12] and anybody else who's interested. Uh, the main things that you do on dash platform
[40:12] is creating a so-called
[40:20] data contract. And what that is, is it's basically just a data schema. Let's say
[40:20] you're creating an
[40:27] application that is a note taking application and you want the, you want all notes
[40:27] to have a title,
[40:35] a description and an author. And, and so you would create a, a data contract,
[40:35] which is like a typical,
[40:42] like if you were dealing with Mongo, you'd, you'd have a schema that, uh, the
[40:42] database is supposed
[40:49] to adhere to that. We call that a data contract in dash in the dash
[40:49] world. And then there are documents
[40:57] that adhere to that data contract. So title, go buy some eggs, um, description, do
[40:57] it at this store,
[41:06] author Ryan. And that's, that's a so-called document. And so the main components of working
[41:13] with dash platform are your identity, which is the authorization kind of layer and payment
[41:13] layer.
[41:20] Uh, so identities, um, data contracts and documents. And so, yeah, we're, we're focusing
[41:28] just on that identity part right now. And that involves, um, identities are essentially a
[41:28] list,
[41:35] uh, a set of public private key pairs that allow you to do stuff. Um,
[41:35] and so that's what, that's what
[41:41] those are all about. And then the state transition itself is, um, the instruction to,
[41:41] to do this,
[41:49] like create the identity, for example. Okay. So, um, yeah, keep, keep going. Uh, I
[41:49] think we're,
[41:56] we've been going for about 40, 40 minutes, so we, we can wrap up at
[41:56] some point, but what else about this
[42:05] project did you want to talk about, can you talk about what, what part was
[42:05] interesting, challenging,
[42:11] um, things, steps, uh, going forward? What, what do you say?
[42:16] Uh, sure. So, I mean, I guess the thing that comes to mind right now
[42:16] is just that, um, as you said,
[42:24] the focus initially was just on creating an identity. Um, and so like, I don't
[42:24] have all of the other
[42:31] transition types actually implemented at the moment. Um, so going forward, I'm filling this out,
[42:31] uh,
[42:38] copying all of the other struct definitions here. Um, something else that's been bothering me
[42:38] a lot is,
[42:45] like, in, in the rest code, um, when they have a part of the message
[42:45] that, um, they don't want to be
[42:53] included in the signature. They just get to add this nice little, uh, annotation that
[42:53] says, um, we can
[42:59] just exclude it from the signature version and then it generates two different versions of
[42:59] the serialization
[43:03] code. Um, the most obvious, straightforward way to do that in JavaScript was just to
[43:03] create a copy of it
[43:12] that uses the signable versions. But then that means that everything that uses them has
[43:12] to also have
[43:18] a copy. So like in this case, we have to have the state transition into
[43:18] the signable version of the
[43:22] state transition, uh, which, you know, copying and pasting just to have like this as
[43:22] the only difference
[43:29] in the entire definition is really not great. Um, so one of the things I've
[43:29] been looking into is, um,
[43:38] possibly adding a, an option into the encoding to be able to say whether you're
[43:38] encoding in,
[43:46] in the signable, uh, encoding or not. Um, and then I could add a, uh,
[43:46] a wrapper around some of these
[43:54] where, um, for example, if we were to go here, I could add a wrapper
[43:54] that's, that's just, uh,
[44:02] something like signable only, um, which would, uh, completely ignore, um, encoding and decoding this
[44:11] field if the signable flag was set, uh, during encoding and decoding. And that would
[44:11] allow me to
[44:16] not have to have identical copies of the struct in both places. Um, so that's
[44:16] a possible future improvement.
[44:26] Another possible future improvement is some sort of automated mechanism for copying this from Rust
[44:32] because as of right now, any changes to the Rust code base, such as any
[44:32] added versions will require
[44:37] manual effort, um, uh, on the JavaScript side to maintain that. So, um, there's a
[44:37] handful of options
[44:46] that could be done there. Um, but you know, honestly, the manual effort is not
[44:46] too big of a deal.
[44:52] Um, so that is probably good enough to just deal with that for now until
[44:52] somebody wants to take on
[44:58] that. Yeah. In theory, uh, the protocol shouldn't change until the version, unless the version
[44:58] changed.
[45:06] And I don't expect that to happen too frequently. And so for this proof of
[45:06] concept, I, I think it's,
[45:12] it's fine to not overly abstract things and automate things necessarily. Um, especially with the
[45:12] budget
[45:19] that we have to work with, which is pretty much nothing right now. Um, and
[45:19] so, yeah, I think,
[45:26] I think what we'll do from here is AJ will take a look at this,
[45:26] um, and try to finish what he was doing
[45:36] with it. So the overall repository, you've added some commits, you cloned his repo, added
[45:36] some commits to,
[45:43] to add this test and, and the bin code, uh, encoding and decoding stuff. So
[45:43] he'll take a look at that,
[45:49] try to get the actual identity working, um, creating an identity, and then we'll see,
[45:49] uh, where to go
[45:57] from there. It looked like you had a list. I don't know if that was
[45:57] a complete list, but it looked like
[46:02] only like eight or nine things. Um, can you scroll back to that list real
[46:02] quickly?
[46:08] Cause I saw, yeah, this, this right, right here, it looks like this is, you
[46:08] know, if those are the
[46:16] only things, then that's definitely manageable. Uh, and now that you've, you've got the overall
[46:16] structure
[46:22] for, you know, how- Don't make the same mistake I did in thinking that that's
[46:22] all because each of
[46:27] these is a complicated struct with nested structs inside of it, so on and so
[46:27] forth. So there could be
[46:32] a lot of, of things to add from all of these, but the important part
[46:32] is that the core code is done. Um,
[46:40] and so adding these should be pretty straightforward. Should be. Yeah. Operative keyword. Yeah. That's,
[46:46] that's always tricky. Um, but I think this is good progress. Um, thank you for
[46:46] doing this. Uh, it's,
[46:55] I was like very impressed by, very, uh, very surprised to see that, that you
[46:55] got it working
[47:03] so quickly. Um, and yeah, I hope we can continue to work on this together
[47:03] and we'll pass it to AJ,
[47:11] see what he thinks. Any, uh, any last thoughts before we close out the show
[47:11] today?
[47:16] Nope. I don't think so. All right. Well, thank you everybody for joining in. Thanks
[47:16] Halawi for,
[47:25] uh, from posting a little comment there. It's always, it's always nice to see. Um,
[47:25] and until next time,
[47:33] we'll, we'll see next week. I think next week, we're going to have, um, a
[47:33] little bit of a more fun,
[47:38] uh, less low level, uh, topic. We've got TX city, which transaction street city. Uh,
[47:47] a lot of people remember, remember that from back in the old days. It's a,
[47:47] it's a fun little transaction
[47:53] viewer that we have dash support for now and are getting some more details and
[47:53] that those details
[48:00] should be done by next week. So we're going to have the developer come on
[48:00] and talk about that.
[48:05] So join us next week for that. And until then we'll see you next time.
[48:05] Bye.