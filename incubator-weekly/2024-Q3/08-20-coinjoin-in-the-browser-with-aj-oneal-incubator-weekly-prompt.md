---
showLink: "https://www.youtube.com/watch?v=Gkv5qZU7IFE"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "CoinJoin in the Browser with AJ ONeal | Incubator WEEKLY"
description: ""
publishDate: "2024-08-20"
coverImage: "https://i.ytimg.com/vi/Gkv5qZU7IFE/sddefault.jpg?v=66c2c8c9"
---

## Song

### ChatGPT o1

1. Fragmented Ledgers Reign
2. Syntax Collisions of CoinJoin
3. Denominated Dreams in Code

Verse

Syllabic synergy saturates these cryptic pipes of connectivity
Masternodes muster impulses forging brand-new anonymity
Collateral metrics revolve generating novel identity
While testnet tangles resonate with ephemeral complexity
In-browser brilliance blossoms denominating versatility
Darksend transmissions hustle dss signals roam collectivity
No disclaimers stifle impetus concurrency beams vivacity
We finalize minted flows in unstoppable tapestry

Chorus

CoinJoin orchestration forging masks out of clarity
Sign the partial inputs watch anonymity marry me
Browser-based phenomena fueling vantage of synergy
Dash redefines transaction with unrivaled capacity

Verse

Nodal adjacency rivets ephemeral vantage
Data-laced impetus escalates cryptographic savage
Collated confirmations revolve in dynamic package
Non-stop denominations swirl devouring average
Coin flows hamper prying eyes with mesmerizing passage
Darksend synergy ascends dissolving invasive baggage
HD arcs finalize addresses discarding old cabbage
Merging partial signatures crafts unstoppable marriage

Chorus

CoinJoin orchestration forging masks out of clarity
Sign the partial inputs watch anonymity marry me
Browser-based phenomena fueling vantage of synergy
Dash redefines transaction with unrivaled capacity

Verse

Global disclaimers tremble under massive impetus
Scripting flows remain polished yet undeniably rigorous
Cross-network synergy amplifies volumes voluminous
Stealth addresses secure vantage against forces insidious
High-speed confirmations circumvent barriers precipitous
Masternodes unify forging presence omnipotent
Browser-based tactics highlight strategies meticulous
Now aggregated outputs remain cryptically ambiguous

Bridge

Foundation meets rotation in unstoppable creation
CoinJoin's invocation fosters subtle transformation
Denominated brilliance expands each open station
While partial-signed triumph reclaims privacy's libation

Chorus

CoinJoin orchestration forging masks out of clarity
Sign the partial inputs watch anonymity marry me
Browser-based phenomena fueling vantage of synergy
Dash redefines transaction with unrivaled capacity

## Episode Description

A discussion on in-browser CoinJoin, customizing denominations, and the future of Dash privacy features.

## Episode Summary

This conversation begins with an overview of an in-browser CoinJoin tool, explaining how Dash transactions can be mixed directly in a web interface. The participants highlight the differences between testnet and mainnet, underscoring the importance of connecting to a suitable node for forming mixing queues efficiently. They then explore how the Dash Core client handles coin mixing, discussing real-time debug logs, Darksend messages, and partial transaction signatures. Building on this, the group covers “cash drawer” concepts—how multiple denominations of Dash coins might be preselected to avoid privacy leaks when performing transactions. They also outline the theory behind typical fiat denominations, noting that adding more denominations could reduce the need for numerous inputs and outputs in each transaction. Finally, they present “cash send,” a proposed method of sending and receiving funds in a more private fashion, ensuring multiple addresses for each user and standardizing transactions in a way that preserves anonymity even when spending the mixed coins.

## Chapters

### 00:00 - 06:00 Introduction and Setup

In this opening segment, the hosts reconnect and set the stage for a deeper conversation about CoinJoin technology in a browser context. They discuss how the streaming software is paid for in Dash, quickly referencing the simplicity and utility of using digital currencies for everyday services. The introduction of AJ’s ongoing work follows, with mention of a new testnet domain and the background behind integrating private transactions into a browser. This sets an enthusiastic tone, showing the potential of a seamless Dash experience accessible via web-based tools.

They then outline what viewers can expect from this episode, emphasizing practical demonstrations of in-browser CoinJoin functionality. By highlighting recent proposals and how community members can experiment with testnet, they make clear that this innovation is still evolving. The conversation also touches on AJ’s previous appearance, suggesting continuity in his development efforts. Overall, these initial minutes promise an informative exploration of how modern browser features can align with Dash’s privacy-enhancing methods.

### 06:00 - 12:00 Matching Nodes and Testnet Dynamics

Here, the hosts address how Dash nodes are randomly selected, which can pose challenges when two parties aim to mix the same denomination at the same time. They note the difference between connecting to a specific masternode versus the typical random assignment among thousands. This distinction explains why mixing might fail if participants are not in sync—particularly relevant on testnet, where overall activity is lower than on mainnet. The tension between automation and manual coordination becomes a central theme for understanding how to expedite mixing processes.

The discussion then pivots to a practical demonstration of denominating coins in a browser wallet. They show the user interface, the steps taken to confirm transactions, and the small challenges posed by browser alerts. While functional, the interface is clearly described as a proof of concept awaiting further polish. Nonetheless, it illustrates that in-browser mixing can work smoothly, provided one understands the protocol’s background logic around denominating coins, selecting the right node, and patiently waiting for the necessary transaction queues to appear.

### 12:00 - 18:00 Viewing Logs and Coordinating Coin Selection

In this segment, they examine debug logs within Dash Core, aiming to see how mixing messages appear in real time. By comparing denominated transactions from the browser and the desktop client, they reveal a deeper layer of testnet mechanics—highlighting how often a machine randomly connects to a node that may or may not facilitate the desired transactions. They stress that simply activating coin mixing on the desktop client does not automatically line up with any specific in-browser session.

Attention also turns to the intricacies of partial mixing, clarifying why simply running default settings might not be ideal for quick or guaranteed results. The conversation underscores the importance of planning which coins to mix, acknowledging that proactive coordination—like selecting a node known to be hosting a needed denomination—is often essential. These minutes underscore a fundamental point: while Dash’s mixing is well-designed, strategic coordination can streamline the overall experience, ensuring multiple participants find each other without excessive waiting times.

### 18:00 - 24:00 Darksend Messages and Transaction Flow

Moving forward, they detail the various Darksend messages (DSQ, DSSU, DSF, DSS) that coordinate the coin mixing process. AJ methodically explains the significance of each step, from drafting a partial transaction to signing and finalizing it. By watching these messages unfold in real time, listeners gain insight into how each participant’s wallet confirms membership in a mixing pool. The conversation clarifies that Darksend “Final” ironically refers to a draft stage, proving how nuanced the protocol’s nomenclature can be.

They highlight how the browser-based mix logs each stage, reflecting input and output addresses and verifying which ones the local wallet can sign. After partial signatures are submitted, the master node compiles them into a complete transaction, ultimately publishing it on-chain without a typical transaction fee. The fee is effectively handled through collateral, an important piece of the puzzle for ensuring privacy and partitioning transaction costs. This behind-the-scenes look demystifies the cryptic-sounding message names while showing that the underlying protocol remains stable and reliable.

### 24:00 - 30:00 Inspecting Transactions on the Block Explorer

The hosts shift focus to examining actual transaction data, attempting to load testnet block explorers. They acknowledge the common issue of testnet explorers being down or less maintained, underscoring the practical hurdles for developers. Still, through the Dash RPC console, they decode a sample transaction to confirm that input/output totals match perfectly, illustrating the essence of CoinJoin’s zero-fee mechanism. Each coin is accounted for in the newly formed UTXOs, proving that mixing took place.

Within this discussion, they address how the collateral transaction stands apart from the main transaction in the block. Though it is still identifiable to knowledgeable analysts, it offers at least some additional obfuscation. The group also points out that in typical usage on mainnet, a much larger pool of participants and denominations creates fewer patterns. By comparing testnet’s sparse environment with mainnet’s more robust activity, they make clear that real-world privacy improvements often scale with increased user adoption.

### 30:00 - 36:00 The Cash Drawer Concept and Real-World Denominations

Here, the conversation broadens to how real cash transactions mirror the “cash drawer” concept, involving multiple note denominations. They explain how fiat systems typically rely on one, two, and five within an order of magnitude—like $1, $2, $5, then $10, $20, $50, and so on—so that people can make exact change with fewer bills. This method, they argue, is also mathematically efficient, tying into the idea of “optimal” sets of denominations that a wallet should hold to minimize confusion and privacy leaks.

They note that the current Dash mixing system, limited to a handful of denominations (0.01, 0.1, 1, 10), sometimes forces users to combine too many outputs. This merging can weaken privacy by clustering coin histories. By borrowing the logic behind physical currency, the speakers suggest adding more denominations to create a more natural distribution of spending amounts. They connect the dots between practicality, user experience, and the cryptographic objective of obfuscating transaction trails in a busy network.

### 36:00 - 42:00 Exploring the Bell Curve of Usage

Continuing the discussion on denominations, they discuss how adopting a bell curve approach fits everyday transaction patterns. Users rarely need extremely large or minuscule denominations, so focusing on mid-level amounts can reduce the number of coins combined in a single transaction. This approach increases privacy by ensuring smaller sets of inputs are needed to reach a common payment size. For instance, if a user typically handles amounts in the range of 10 to 50 Dash, having more denominations in that zone is key.

They reinforce that the crux is about tailoring coin supply to expected transaction amounts. A wallet that recognizes a user’s spending habits can maintain a balanced spread of denominations that are most likely to be used, limiting unnecessary merging. The group ties these patterns back to broader usability concerns: people simply want quick, reliable transactions without fussing over complicated coin merges. By automating denominational variety, the network can reduce confusion and help privacy-minded users avoid accidental self-disclosure.

### 42:00 - 48:00 Introducing Cash Send and Redefining Privacy

In this chapter, they highlight how “Cash Send” is essentially the logical progression of CoinJoin and PrivateSend. While CoinJoin anonymizes coins and PrivateSend allows spending them, Cash Send merges the two processes in a uniform manner. It separates a transaction into denominated outputs—ensuring no single address or output inadvertently clusters user histories. This transforms typical sends into multi-address outputs, each still within the realm of recognized Dash denominations.

Moreover, the conversation explains how Cash Send could do away with collateral transactions by folding transaction fees into standardized amounts, reducing telltale traces on the blockchain. By using hierarchical deterministic (HD) wallets, each recipient can present an extended public key, facilitating truly private, repeated payments without the risk of address reuse. The potential outcome is a simpler, more comprehensive approach to privacy. Listeners learn how this system stands to unify mixing and spending in one cohesive user flow.

### 48:00 - 54:00 Deeper Look at Cash Send’s Practical Mechanics

Having introduced Cash Send’s principles, the group addresses how recipients might manage multiple addresses and how the blockchain would parse each output. They break down the idea of “dust” or minor leftover balances, explaining that these can be periodically reabsorbed into fresh transactions, effectively hiding traces of prior transactions. This re-averaging of fees ensures that typical usage patterns no longer expose which inputs belong together.

They also discuss the user experience side, emphasizing that once two parties exchange extended public keys, subsequent transactions can be made seamlessly. The wallet tracks new unused addresses, creating a near-invisible process for the end user. Despite this sophisticated setup, they stress that if it’s all baked into the wallet interface, people only see a “Send” button—no complicated steps. Cash Send is pitched as an ideal blend of cryptographic rigor and real-world convenience, promising a feature-rich future for Dash.

### 54:00 - 1:00:39 Final Thoughts and Next Steps

In the concluding segment, they reflect on the progress made with the current in-browser demo. AJ explains the immediate goals, such as displaying available mixing queues and connecting simultaneously to multiple masternodes for quicker pairings. They acknowledge a need to refine the user interface, removing confusion caused by browser alert prompts or overlapping state issues when multiple tabs run the same wallet data.

The speakers then address concerns about security and readiness for mainnet, noting that although the interface remains visually basic, the code follows Dash’s established protocol rules. They encourage community input while highlighting that the simpler it becomes to coordinate mixing, the more people will adopt privacy features by default. Wrapping up, they invite questions and feedback, leaving listeners with an optimistic vision for expanding Dash’s privacy capabilities—both in the official desktop wallet and through innovative web-based options.

## Transcript

[00:00] and we are live back in high quality without any ad thing oh yeah no
[00:12] no uh stream yard duck this time i got my i got my spritz card
[00:20] refilled with dash um and that's what we're paying for the stream yard with so
[00:00] we've got that up to date and um yeah we've got aj back with us
[00:28] again for the second week in a row welcome again yep hello more aj if
[00:36] you missed it last week we talked about uh aj's um rpc library and service
[00:46] that uh he has a current uh current proposal up for four dash to maintain
[00:00] that service so check that out if you haven't seen it already from last week
[00:53] this week we're talking about digitalcash.dev digitalcash.dev is the domain and specifically rpc.digitalcash.dev and trpc
[01:08] not the kind of trpc that you're thinking of anthony because i know that you're
[00:00] thinking of typescript rpc when i say you know how much i'm thinking of getting
[01:14] dash testnet.dev and putting all the testnet stuff on a separate domain okay rather than
[01:20] having t prefixes so yeah the trpc will probably change at some point yeah okay
[01:29] cool um so anyway today we're talking about coin join and private send and the
[01:37] browser and bringing those all together we've got um we've got coin join working in
[00:00] the browser do you want to give us a little uh just description of what
[01:43] you've done aj and then we'll jump right let's let's tease it let's tease it
[01:49] let's tease it put me up on the screen coach uh let's see screen share
[01:57] window here we go we're gonna we're gonna share it all right so here we
[00:00] are and what basically you've got your your faucets you've got all this wallet information
[02:08] this is testnet stuff right now and you know it's not it's not polished everything
[02:14] everything is on one page there's no tabs you kind of have to watch a
[02:20] little demo video to know exactly how to do it but you know whatever so
[02:27] here whoops you got your wallet information here um you've got information about coins that
[00:00] you currently have here you have the ability to send to an address to send
[02:33] a memo because a collateral ends up being much like a memo uh actually it
[02:42] just is a memo uh with a with a specific fee and then we've got
[02:48] a cash drawer which we'll talk about that later and this is basically targets for
[00:00] for what we want so let's say i actually don't want any of these i'm
[02:55] just going to zero things out for a minute and then i'll just we'll we'll
[03:05] we'll do we'll do part of well there's let me go down you've got unspent
[03:11] addresses unused change addresses spin addresses let's say i just want to denominate some coins
[00:00] let's say that i want uh five of these so i'm going to just do
[03:18] denominate coins all right are you sure yes yes yes oh and by the way
[00:00] just so you know we we don't see those um alerts that you're oh you
[03:25] don't see the alerts yeah okay well next time i'll click share window or share
[03:30] screen instead of share window so yes there were alerts i i use i use
[03:36] pop-ups because it was simpler than you know i just i just went simple like
[00:00] i didn't do any styling on this this is a free theme that i i
[03:42] just like because it's fairly simple and clean so i use it a lot so
[03:48] i didn't actually create a modal and the theme doesn't have a specific modal in
[00:00] it you can do a modal with it it's just it's not there's not a
[03:55] modal thing anyway using the browser alert which we don't see yeah maybe when you
[04:00] when you do come up with those just say what they say yeah so it
[00:00] says are you sure you want to send uh what was it 0.012 and then
[04:08] whatever address that it had picked and so now you can see there's five spin
[04:14] addresses the unused addresses have gone shorter and then now if we go back up
[04:20] to our coins you can see that these are bolded and italicized which means that
[00:00] they are denominated and then we'll do a demo a little bit later or let's
[04:26] just do the demo now actually we'll just do the demo now i just have
[04:31] to open up in two browsers in order for it to work actually um so
[00:00] i'm going to actually share my screen because i want to show something other than
[04:37] that real quick because i'm going to actually be your mixing partner oh yeah so
[04:43] i'm going to share my screen and bring up let's see how do i i'll
[04:51] just bring this up so you guys aren't seeing the infinite thing there um and
[00:00] then i'm going to bring up my test net node if you're wondering i've increased
[04:59] the font and completely unbolded it as much as possible so hopefully it's a little
[05:04] easier to see i have not yet uh done any this is the test net
[05:11] you can see can you see my my little window popping up here yeah yes
[00:00] okay so you can see this is orange that means uh it's a test net
[05:18] you can also see this is test dash right here down here um so i
[05:24] haven't done this yet ever on this wallet so i'm going to run the coin
[00:00] process on you this is not going to work the way you think okay you
[05:31] need to do it in in the browser and the reason is so your computer
[05:39] is semi-randomly selecting from four thousand nodes and the in order for coin join to
[05:45] work you have to connect to a node where someone else is advertising the same
[00:00] denomination that you want to join on the way that it's done in my demo
[05:51] is that it connects to a specific node so rather than connecting to one out
[05:57] of four thousand nodes randomly it connects to a specific node so when both browsers
[06:05] connect to a specific node then they immediately have the same queue for the same
[06:12] denomination of coin if your computer picks one it randomly and my browser picks one
[00:00] randomly and we're on test net where there's just not as many pools available and
[06:20] then we both try to and and my browser demo right now is only opening
[06:28] up one pool whereas the desktop is opening up 10 pools at least from what
[00:00] what we saw the other day it looks like and so the desktop is and
[06:35] the desktop has been running in the background for a while so it already has
[06:42] its pools built up whereas the browser is not okay well the browser is not
[00:00] built to run 10 pools at a time right now it can it's just i
[06:48] don't have that functionality in because it was you know the the mvp demo that
[06:56] i was aiming for so sure it it can do you can do the coin
[00:00] join between the desktop and the browser it's just that if you want to do
[07:01] it quickly and you don't want to be having it wait there for several minutes
[07:08] potentially uh trying to find a partner then you need to connect to a node
[07:12] that you know already has the pool that you want and when you listen there
[00:00] will be a table for this what do you mean just just just tell people
[07:18] what you mean by pools so there's a message called dark send queue and the
[07:28] dark send queue message is broadcast from master node that you're connected to and for
[00:00] every coin join round that is in the um what what would we call that
[07:43] in the aggregation phase or the in the join phase for the not ready phase
[07:56] so it's it they're broadcast and the desktop client and the other clients that do
[08:02] this they keep a running list so right now while we're unaware as to what
[08:10] the pools are the desktop client is receiving broadcasts from 10 masternodes about the available
[08:18] pools so the likelihood that any given masterhood master node is currently processing a pool
[08:25] that you're interested in joining of the the five possible denominations is actually decently high
[00:00] um i'm not sure if that holds on testnet as well as it does on
[08:31] mainnet uh because i i know that lots of people that's all they're doing all
[08:35] day long is just running coin join and you know their coins have been mixed
[08:42] hundreds or thousands of times at this point but anyway um yeah so there's there's
[00:00] that aspect to it where the in in the browser demo we're only connecting to
[08:50] one masternode and we're not listening for pools ahead of time to know which coins
[08:54] we should select because that's the other thing it's opportunistic if you've got coin join
[09:00] running and you need mixes of every coin well there's going to be a pool
[09:05] open and even if it's not the pool you need most right now it's going
[00:00] to be a pool that you can use on some denomination of coin until you've
[09:13] hit your your cash drawer limits which the cash drawer is not ex the cash
[09:22] drawer exists in um in dash qt the desktop client but it's not exposed there's
[00:00] no way for you to access it okay so i was actually just going to
[09:28] talk about that because this is basically this is basically your cash drawer options for
[09:36] the desktop client you've got how many parallel sessions you want to allow you've got
[09:43] the mixing rounds that you want to run i'll just bump that up to 10.
[09:49] you got your target balance this these are all these were all the defaults i
[00:00] haven't changed anything about these so it's interesting that the default inputs per denomination is
[09:54] targeting 50 and giving a maximum of 300. i'm going to bump that way down
[10:06] to 20 and 10. this is basically you did 50 and 10. say say what
[00:00] you did 50 and 10. i don't know why but um okay so let's do
[10:15] 20 and 10 and i'm just going to go ahead and start this um i
[10:24] have something like 10 i have like 40 dash i think of balance in my
[00:00] uh in my wallet so i guess go ahead and say yes i might be
[10:33] the only person mixing on text testnet right now like not many people are using
[10:40] testnet um there definitely there definitely are mixes going on on testnet because i see
[10:45] the dark send q message come through quite frequently but it's it's not uh omnipresent
[10:54] and it's not always the denomination that i want so if i select 0.01 and
[00:00] a q comes through for 1.0 and 0.1 i can't use it and so one
[11:06] of the updates that will be coming i believe this week to this tool will
[00:00] be to put the dark send qs in a table so that uh it's easier
[11:17] to select and then also uh collect connecting to multiple master nodes at a time
[11:26] so that there are many queues available okay so i i'm just um i i
[00:00] just kind of wanted to get this on screen just for out of out of
[11:34] out of out of curiosity i'm gonna open my debug.log um and i i don't
[11:46] know i guess probably nothing on here is private but i don't know how do
[00:00] i zoom in on this uh i guess i i don't know if i can
[11:54] actually um i'm just kind of trying to see oh no that's that's a qt
[12:02] window not anyway um you can see the submitted denominations here so it's going for
[12:13] 0.01s and 0.1s at this point and i was just kind of curious to see
[12:20] if i will have any kind of mixing partners right now and then when you
[00:00] join in if it would speed things up so you're saying it won't connect to
[12:26] my the nodes that i'm connecting to but if you if you can give me
[12:32] a list of nodes you're connected to and and yeah if you could that's what
[00:00] i was doing here on my peers i don't know do you know the ip
[12:42] address of your um so you're connecting through rpc your rpc service right and you
[12:54] got 35 90 252 3 because i could so all of these are dcg ones
[00:00] that say dcg so it'd be just the ones that don't um i'm assuming i
[13:03] don't know but if you could copy and paste that to me i could put
[13:07] that in the browser and then that would guarantee that we're connected to one of
[13:12] the same nodes okay uh let's see but i i anyway we don't have to
[13:21] go through this i thought it might just be interesting um to see some of
[00:00] the to see if we could connect to each other and and and see that
[13:31] but um anyway let's um let's go ahead and share your screen now and we'll
[13:38] yeah let's let's just share my screen i can i can demo this and then
[13:46] we can yeah we can definitely get it later so that it works um for
[00:00] that use case okay i'm going to share the screen all right so what i
[13:57] have is two browsers open and i need to make sure that the second one
[14:00] is actually connect yeah it looks like i can get my dev console open too
[14:06] so what you can see there's these dark send q messages that come through and
[00:00] then i have here printed out what denomination that q is for and so the
[14:13] q represents basically a round that's being built up i don't think we're seeing what
[14:19] you're seeing uh you are not seeing what i'm seeing uh sorry i showed the
[14:27] wrong screen let me try that again that there we go okay sorry about that
[14:37] so there's two wallets i've got one blue and one purple they're in different browsers
[00:00] because if you have shared state between the wallet and you try to open up
[14:42] both wallets it's it's not going to work because the wallets do things like try
[14:47] to make sure that you get a unique address and if they both mark the
[14:53] same address is pending and then yeah it and there's checks to make sure that
[14:57] you know things are the way that they they're supposed to be and if if
[00:00] the wallet if the wallet is in an inconsistent state because it's opened up in
[15:04] two different tabs but it's using the same data storage then it gets confused because
[15:09] the memory state is not the same anyway so here we are and you can
[15:14] see there's some dark send q messages going through and they come through a different
[00:00] amount so there's the smallest one right there you can kind of count the zeros
[15:19] from the end um and then i think that represents the one that has no
[15:27] zeros at the end has three zeros at the beginning so it's 0.00 or maybe
[15:34] 000 i don't remember but anyway so you can see they're coming through in different
[00:00] denominations this is actually you know by random chance this is a really good node
[15:38] to have connected to right now uh in terms of the the the variety of
[15:47] denominations that are in this pool and then i've got another one of those windows
[15:51] open for the other browser so that i can see that both are connected and
[00:00] working so anyway i can go through here and let's see what have i got
[15:59] 0.01 so i'm going to select two of these over here and i'm going to
[16:06] select run coin join and then wait wait before you do that have you done
[00:00] have you done any coin joining yet or just the denominating what have you done
[16:14] any coin join have you done any coin joining yet or just denominating just denominating
[16:21] okay on my side i am seeing denominated 100 percent partially mixed 3.6 percent and
[16:30] mixed zero percent that just means that somebody outside besides you must be mixing on
[16:40] this uh network yes i guess yes so once i click the button i kind
[00:00] of have to click the other button otherwise it's gonna time out so i just
[16:45] went ahead and clicked the button okay um on both of these browsers so i'd
[16:53] selected i'd selected this coin here on this browser and then two coins in the
[16:58] other browser and it already completed it already worked out so there's a bunch of
[00:00] dsq messages broadcast right as you started speaking i was going to point out that
[17:03] the messages had just bumped up because as soon as i click over in one
[17:08] browser the other browser is going to get the dsq that that that that that
[17:15] brought that browser is causing to announce or re-announce okay and so that dsq for
[00:00] the amount had gone through along with other dsqs that are happening on the network
[17:21] dark uh the dark send queue and then and then uh we see that it
[17:30] signs collateral so you can see that the collateral signing calls the memo signing because
[17:36] the collateral is a type of memo uh in most cases you can actually do
[00:00] the collateral in a bunch of different ways at least not according to the spec
[17:41] as much as according to the implementation because i've tested things that are against the
[17:46] spec and they work so that would mean that it would not be safe to
[17:52] do it that way in the future because when we have multiple dash clients and
[17:57] it's not just the dash core client they would probably follow the spec anyway um
[00:00] so yeah so you can see that i've got my collateral and memo signed messages
[18:03] and then the dsa comes in so i'm sending the dsa that's what i'm announcing
[18:09] a dssu comes back to let me know that i've been accepted into a pool
[00:00] and that happens immediately so that means that the pool is already open so this
[18:14] console may have been for the browser that um was the the first the second
[18:23] one anyway so the dssu message usually comes back to say you're accepted or that
[18:29] you're rejected and i i don't have that debug print out then the dsqs continue
[18:36] the whole time because that's whatever's going on on the network some more dssus uh
[00:00] and then we have the dsf which is it's really weird it's called the dark
[18:44] send final it's actually the dark send draft it's very weird that it's called final
[18:51] because what it is is it's a draft transaction and then you create the final
[18:56] transaction and send it in or rather you create your you create a partial transaction
[00:00] so a transaction with partial signatures and you send that in so that's what the
[19:01] dsf message looks like then i've got that logged out so you can see it's
[19:07] drafting these inputs and it's drafting these outputs and so if we were to look
[19:16] at this uh let's see does it actually show the addresses we could we could
[00:00] see we could convert these pubkey hashes into the and find out which addresses are
[19:21] in my wallet and that's what this does because when it gets this draft it
[19:25] has to look through all the inputs and say okay which of these inputs are
[19:32] the inputs that i can sign and which of these outputs or outputs that i
[00:00] can sign and then i'm going to send back a message that includes partial signatures
[19:41] across the inputs i care about and actually all the outputs it's gonna it's gonna
[19:49] sign all the outputs not just the ones i care about um and then then
[19:56] i send a message called dss which is dark sense i think it's dark send
[00:00] signed and then we get back a message dsc which is dark send complete and
[20:03] so that lets us know that it was it was already processed in the queue
[20:10] and then if we were to look at these addresses so i could go look
[00:00] at these these addresses here um let's let's look at the rpc tool real quick
[20:18] and then we'll do uh get address deltas and then oops address i think it's
[20:38] addresses addresses address oh bless me either way all right so now we'll run the
[00:00] rpc and we can see the output and you can see exactly what you'd expect
[20:48] is that you see one coin one coin that had received and one coin that
[20:58] was spent and this spend right here was if we were to do uh get
[21:06] raw transaction oops and then uh we put in our transaction id and true that
[21:15] we want it back decoded then we can take a look at these and we
[21:19] can see that this is a coin join transaction so there's a value there's a
[21:26] value there's a value we can expect several of these because there's other others connected
[21:32] there's a value and so you can see from this that that was in fact
[21:36] a coin join transaction another thing that you can that will let you know it's
[00:00] a coin join transaction and not some you know magic trickery that i'm doing to
[21:41] fool everyone is that there's no transaction fee if you add up the inputs and
[21:45] the outputs you'll see that they're synonymous there's no transaction fee and that's the only
[21:51] reason that um a master note is required for this is that the collateral is
[21:57] submitted via a side channel now you know it's kind of tomato potato because the
[00:00] collateral still ends up in the same block so it's not like it's not linked
[22:02] because anybody who knows the protocol is going to know that they're going to be
[22:06] looking for a collateral transaction and they know that the collateral transaction is likely very
[22:12] small although according to the current implementation you can just send any transaction like if
[22:16] i wanted to pay you for something and it didn't matter when i paid you
[22:21] i could pay you any time in the week i could set up that payment
[00:00] and i could use the payment to you as a collateral transaction it doesn't it
[22:26] doesn't have to be a memo as per the implementation that exists in dash core
[22:33] it will accept any transaction as collateral as long as the fee is uh the
[22:39] the right amount so but but knowing that understanding the way the spec works you
[22:45] can still figure out which transaction was the collateral related to um you know coin
[00:00] join sessions you can't tell which of the coin join sessions and the block it's
[22:51] related to necessarily uh ideally yeah you definitely you definitely can't but you can still
[22:57] tell it's related so it's still a signal it's just it's like one step removed
[23:03] so yeah potato but can you can you pop this open uh this transaction open
[23:11] in in the insight and yeah yeah sure so let's let's go to insight here
[00:00] whoops just so that people can see that with the more familiar uh interface anthony
[23:20] you're smiling i don't know if you're just having good times over there if there's
[23:25] something relevant to this that you know sorry i'm i'm messaging my partner i'm okay
[23:30] off my own world sorry no worries uh so i don't think the test net
[23:38] insight's working right now that is often the state of it test that insight well
[23:44] insights on life support and test net insight has not quite made life support priority
[00:00] you're on the dash evo domain and that's not yeah that's not the one that's
[23:52] actively maintained i think all right well which one is the one that's yeah it's
[23:57] the it's the one that has like um networks dot test net something or other
[24:07] um let me see if i've got it on digitalcache.dev whoops because i did include
[00:00] yeah let's see this one it's this one insight ui here okay yeah on on
[24:20] dash uh digitalcache.dev i'm including links to resources that are common resources like this well
[24:25] i yeah see i think it's defunct it's not it's not showing up try refreshing
[24:32] all right i'll try refreshing but you're right yeah these these tools are not uh
[24:41] very well maintained right now all right so um simpler tools i mean simpler maintenance
[24:47] okay so so anyway but yeah you were able to see this we could have
[00:00] put this in a table and and you know you'd be able to see it
[24:53] in a more familiar way but but yeah so the point is that's the coin
[24:56] join demo works cool you know and and we we only we only go up
[25:06] from here but this is this is simple debugging tool uh yeah so that that
[00:00] uh unfortunately took a little longer than i was hoping but it does the business
[25:12] as they say yeah so uh bridgewater has a comment on the discord and a
[25:20] question as well he says regarding that last thing which was um talking about the
[25:29] priority column when you or jojo or whoever makes a nice front end for it
[25:34] i'd recommend using words instead of numbers for priority like highest versus 10 because there's
[00:00] already so many numbers to look at when dealing with the denominations just one little
[25:40] thing that jumped out at me it's not too important i find your presentation so
[25:45] anyway i wanted to kind of echo that as well like um for me priority
[25:52] one is the highest priority so maybe if you did it like a's and then
[00:00] translated those into uh numbers on the back end that oh yeah it it really
[25:59] is not that big of a deal i really like the idea of using um
[26:10] the the alphabet the reason for numbers is that numbers there's an infinite number of
[00:00] numbers so if you decide that okay i want to make i actually want to
[26:15] make this thing the highest priority you can just increment the number by one without
[26:21] having to redo everything else right so say say like right now at this moment
[26:27] what i want to do is i want to make i want to make this
[00:00] coin the highest priority because i'm debugging then all i have to do is increment
[26:34] that you know i all i have to do is make that number the biggest
[26:40] number and then now it takes the highest priority when i click the button but
[00:00] yeah i i there there is only a i guess the better way to do
[26:48] it might be to have the like have the columns move up and down or
[26:56] something but but yeah the the i i think that's a great idea it's a
[00:00] great suggestion and there's so few of these that you don't need infinite numbers it's
[27:01] just nice for me because i don't want to say well i had this at
[27:07] highest but now i want to make this highest so how do i make it
[00:00] highest er okay um most highest yeah yeah but then you need most or highest
[27:17] okay so let's let's talk about that uh cash drawer um a little bit more
[27:30] and your concept uh that you you've submitted a dip for called cash send how
[27:40] um actually i'll just ask uh in preface for to to preface that conversation what
[27:48] do you think the pros and cons would be of adding newer uh additional denominations
[00:00] so right now coin join has denominations of 0.0001 0.1 1 1 10 and i
[28:02] think that's it so there's like all they're all orders of magnitude of of 10.
[00:00] now i know that whenever i almost almost 100 of the time i would say
[00:00] uh like not quite that much but 90 plus percent of the time that i
[28:16] do coin join transaction it's uh it gives me that warning that says you're using
[28:26] more than 10 coins in this um in this transaction that's detrimental to your privacy
[28:33] and i know that sometimes that doesn't really matter like if i if i'm doing
[28:40] 16 rounds of coin join uh mixing and i get that like some people have
[28:47] said you know you don't need to worry about that or whatnot um but the
[00:00] overall statement i think is true the more coins you're using the less the less
[28:56] private or less secure that transaction is actually uh in order to be like traced
[29:03] or whatever so so so okay let's i'll speak for a minute and then i'll
[29:09] ask you to pull up the the screen that i've shared okay but okay so
[29:17] first of all there's a difference between mathematical perfection and reality and sometimes the two
[29:23] are the same and sometimes they're not one of the things that is the same
[29:30] between mathematical perfection and reality is that the optimal number of bits of information is
[00:00] the number e which is 2.7 something something something e is a mathematical constant it's
[29:38] not as famous as pi but it's used for things like calculating population rates and
[29:45] bacteria cultures and and economic systems it's it's a number that has emerged from mathematical
[29:53] formulas that describes a lot of things so the perfect amount of information that can
[30:00] that could be stored would be e now this is one of those things where
[30:05] mathematical perfection and reality kind of don't mix because e is not a countable number
[00:00] it's not like one two e three you know it's one two three and so
[30:13] you round to three so in practical sense three is the most perfect um medium
[30:24] to store information now let's bring that back to reality it's the rule of threes
[00:00] right we have all these things that are three we have uh the in religion
[30:32] there's there's there's the trinity in uh engineering there's that the triangle of um fast
[30:41] cheap and good whenever you list something off it just feels right to list it
[30:51] off in threes we have the idiom bad things come in threes so three is
[30:58] kind of a magic number in terms of choices and trade-offs that is just kind
[00:00] of appeared in humanity that's just something very natural and this has to do uh
[31:05] in with with the way our you know our brain works but it it's it's
[31:12] very nice that coincidentally having three options for something is is mathematically as close to
[31:18] perfect as we can get because three is as close to 2.7 as a as
[31:28] a countable number is but when you look at um money you there this pattern
[31:34] also exists although you might not have recognized it humans are built such that they
[00:00] understand orders of magnitude right so i need to understand is this group of tigers
[31:41] bigger or smaller than this other group of tigers and and by what order of
[31:48] magnitude is it like twice as big or is it 10 times as big i
[00:00] can't tell you that there's 100 here and there's 357 there by looking but i
[31:55] can tell you this group is twice as big as the other group so it's
[32:03] one order of magnitude bigger or if we're if we're looking at uh you know
[32:09] depending on what you consider to be order of magnitude whether you're doing two like
[00:00] binary and computers or 10 like people often do uh you know you you can
[32:17] you can get a sense of scale even though you can't count and so in
[32:26] our money our money has become three choices for every order of magnitude so you
[00:00] have your i mean it's not perfectly true in all situations but it tends this
[32:33] way that you have your your ones your twos and your fives right so and
[32:42] this is how we originally our dollar system was one two five that's one order
[32:50] of magnitude three choices but actually well we'll we'll go into this in a second
[32:56] it's actually representing the orders of magnitude even better than you think when you count
[00:00] this way but then it's 10 20 50 we used to have a 50 bill
[33:03] and then it's a hundred and we stopped there because uh by the time we
[33:13] had useful use by the time we had enough inflation to regularly need above 100
[33:21] we also were inventing credit card systems check systems digital cash systems you know so
[00:00] we we didn't we didn't keep going with the alternate explanation to that is that
[33:28] governments didn't want people having high cash values easily transportable so they get away i'll
[33:35] drink to that i'll drink to that yeah but the the point is like that
[33:42] was our number system and if you go down it's 50 and then this is
[00:00] where it gets a little weird because we have a 25 and a 10 but
[33:47] i think that that is a trade-off because the amount of silver that you could
[33:54] use and like the different um the different metals that you were working with between
[34:02] silver nickel copper um i think that the reason that it breaks down at the
[00:00] coin level has more to do with the the way that the metals were processed
[34:08] than that it was the you know the the natural choice but yeah then you
[34:14] know you go down one and we used to have a tuppence we don't have
[00:00] a tuppence anymore but we had one two five but then dimes were silver and
[34:21] so it was a tenth of a silver dollar and i i think quarters were
[34:28] silver as well and then we had the half dollar which would be the five
[00:00] again so but so what this actually is is it's doubles holes and halves so
[34:35] but when we think about it we think about it across orders of magnitude rather
[34:39] within an order of magnitude but within an order of magnitude you have ten dollars
[34:46] as your starting point 20 is your double and then five dollars is your half
[00:00] so this is the pattern that appears in i want to say in in nature
[34:56] as well as in human logic so if we wanted to create a monetary system
[35:03] that reflects both mathematical perfection as well as the way that humans understand money thankfully
[35:10] the two systems are actually the same system which is double holes and halves of
[35:18] an order of magnitude so one double is two half is 0.5 tens double is
[00:00] 20 half is five hundreds double is 200 half is 50. yep and if we
[35:32] take that now if you share my screen one of the problems that you saw
[35:39] with the cash drawer in dash core that implementation of the cash drawer is that
[00:00] it did not give you any um option to deal with the scale of the
[35:47] money which is actually really important because you know you think about a lot of
[35:57] kids may not get this but the adults um you know will when you used
[00:00] to have money in your wallet what did you have you had one 100 you
[36:05] had two or three 20s you had a handful of fives and several ones right
[36:15] because you organize your wallet your cash drawer or like the reason i call this
[00:00] cash drawer is because it's the cash drawer at the registry you know or register
[36:20] you go to the grocery store this is how the cash drawer is organized more
[36:25] or less right i accept that they're using the double holes and halves that we
[36:34] have in and and uh you know paper money but the the system uh is
[00:00] that you don't you don't make lots and lots of room for the hundreds because
[36:42] you're not dealing with hundreds often you might have two slots dedicated to fives yeah
[36:48] you're not aj right i'm just kidding but but you know whatever the scale of
[36:55] the transaction is there's a bell curve to it right like you're never using pennies
[37:00] and you're rarely using a hundred dollar bills but you're probably using a hundred dollar
[37:06] bills more often than you're using pennies right so this option is the one that
[00:00] you almost want none of if you can ever avoid it this one doesn't really
[37:14] matter it's just sometimes more convenient for certain types of transactions and it's really you
[37:20] know the two things that you need are your 20s and your twos so if
[37:25] we were to look at this this represents about two and a half dollars you
[00:00] know so you need a few of these to make up the difference and and
[37:31] you need a few of these but most of what you need is this so
[37:35] if i was going to build a cash drawer it should look like a bell
[37:44] curve where i have something like 25 um you know obviously it depends on on
[00:00] the size of transactions that you're typically doing sure yes um and this comes back
[37:50] to the back to the issue that i was raising where sometimes you're doing it
[37:57] uh almost always i i get that warning that i'm doing um i'm spending too
[00:00] many coins and that would you know there's toggles that i can i can change
[38:04] this is well they're not or you don't have any toggles you can change for
[38:08] that you would need something like this that allows you to totally exactly um because
[38:14] it doesn't the wallet doesn't know and sometimes i don't even know what size of
[38:19] a transaction i'm doing so if i'm doing a transaction where i need 20 uh
[00:00] you know to send 20 dash and my drawer doesn't have any tens i'm going
[38:26] to be using hundreds of hundreds of coins and that and that's what happens because
[38:33] this is what needs to be built in regardless of the size of transaction you're
[38:38] doing it's not going to be off by more than an order of of magnitude
[38:43] most people are going to be transactions that are based primarily on the 20 dollar
[00:00] amount you personally because of what you do i think i think you actually still
[38:49] fit into that category that most of your denominations are in between yeah because the
[38:56] rules of dash incubator that you can't spend more than a hundred dash it's not
[39:00] incubator stuff it's it's actually my personal use because i don't okay i don't do
[39:07] coin join transactions for for incubator but um i think the the point is if
[00:00] if we had more denominations to choose from if we had 20s if we had
[39:16] 50s if we had fives and twos you're going to use less coins for sure
[39:23] um yes and this is and this is going to be the better outcome because
[39:28] again that's mathematical perfection the number of choices needs to be three and it needs
[39:32] to be a logarithmic so this is mathematically perfect you cannot design a better system
[00:00] not this but what i just described you cannot build a better system than that
[39:37] it is the guaranteed perfect system both from a mathematical perspective and from a practical
[39:42] human perspective that is it is a perfect union yeah and so there are two
[39:47] issues here there's there's the one issue of this also gives you the customizability of
[39:54] saying exactly which of each coin you want but what we're also talking about is
[40:01] introducing more denominations the twos and the fives i know that one one um concern
[00:00] about that is that the more denominations you add the less uh likely it is
[40:11] that you're going to find mixing partners that need those denominations so it might take
[40:17] longer to mix so that's that's a trade-off right if you um but it's about
[40:24] that a little bit yeah it's not it's not the trade-off that you think it
[00:00] is right because again there's a bell curve here right so if the way that
[40:31] the current wallet is set up if the current wallet doesn't doesn't get this where
[40:38] it provides a bell curve to what you're actually going to need most often then
[40:45] yes that that problem would persist so if we introduced more denominations and we did
[00:00] not adjust at all the way that we cash drawer the denominations then yes that
[40:54] problem would exist but that problem is the same problem that you already have it
[40:59] already does exist and that you're not getting the denominations you need and you're getting
[41:04] a bunch of denominations you don't need yeah um and so then you're having to
[41:12] spend way more than you should and so coin join is ineffective from a mathematical
[41:18] perspective you're not getting the mathematical privacy that you want because you have to you
[41:23] have to break the mathematical rules in order to do a regular transaction so where
[00:00] if you put it in a bell curve most of the time you're going to
[41:36] need these transactions so most of the transactions that are going to be happening on
[41:40] the network are the ones that people need the most rather than all transactions be
[41:46] done equally according to how much money people have so no matter what you need
[41:52] you're always getting 50 of each but that doesn't that doesn't mat that matches what
[00:00] you have it doesn't match what you need yeah so and i i know that
[41:59] um bridgewater in particular he's the one that made the comment about the priority thing
[42:06] and i know that he has he's been there might not be anybody that knows
[42:11] more about the coin join stuff than him in the dash community and he's been
[00:00] pushing for an implementation like this where you in the actual core wallet you can
[42:17] actually describe what you have here so hopefully at some point dash core will also
[42:26] have this ability to show exactly what you want and give priorities and things like
[42:33] that um and that will i think help the situation a little bit but um
[42:36] i wonder so is this something that you think would be a priority like do
[00:00] you want to see the introduction of new denominations and i do know that uh
[42:55] you also have this concept of cash send let's yeah so that for a little
[43:02] bit so that people can see like i see a path where if we introduce
[43:09] more denominations to coin join that like the twos and the fives and then also
[43:16] transition that into something that like what you're talking about with the cash send which
[43:22] i'll ask you to describe in a bit that would be the best of both
[43:29] worlds where uh even like normal transactions that aren't coin join transactions they would be
[00:00] more private they would be uh more secure is the term that you like to
[43:35] use more more they would be more private um but also then you would have
[43:41] the option to coin join those as well uh so talk about what what cash
[43:49] send is and um how this relates and and what the path might be to
[00:00] okay getting from here to there so there's two components there's coin join and there's
[43:55] private send right so coin join is when you mix the coins private send ironically
[44:02] is when you unmix the coins yeah i'm gonna have you pause on that because
[44:07] i want to describe that a little bit in in the way that i understand
[00:00] it so when you look at a block explorer and you see a coin when
[44:14] you see um a transaction where the inputs and the outputs are equal in length
[44:23] that's a coin join transaction so work i don't think that the community uses these
[44:28] terms like the way like we're using them i think that we're using them in
[00:00] a way that's more descriptive because a lot of times people think coin join is
[44:33] synonymous with private send um and well that that'd be like saying the brake pedal
[44:39] is synonymous to accelerator pedal i mean you need both i'm just but they do
[44:44] the opposite thing i know i'm describing it for the folks at home because historically
[44:53] we have had this transition where we had a term called private send and then
[00:00] in the ryan taylor era of dash core group there was a push to d
[45:05] um d unbrand the private send and not use the term private because the japanese
[45:11] regulators didn't like that for whatever reason they don't like privacy and so there was
[45:17] this push to just say okay well the industry is using this term coin join
[00:00] which is the technology that private send uses mostly um and so let's unbrand private
[45:23] send to coin join and but that never really took root and so now a
[45:31] lot of people in the community have this synonymous relationship where coin join is just
[45:37] a different branding of private send but i would like uh and i and you
[00:00] would agree i'm sure i would like us to have a more uh defined distinction
[45:47] between these two where coin join transactions are those transactions where you're taking let's say
[45:53] five inputs and five outputs and then mixing them and and that is what de-anonymizes
[46:02] and and gives some kind of uh ambiguity of of who owns which coins that's
[46:10] what we are calling a coin join transaction and private send would be when you
[00:00] take the outputs of a coin join transaction and then spend them on say something
[46:16] that costs 27 dollars and it's going to take two tens uh and seven ones
[46:24] to uh and it's going to combine those uh doesn't combine them it well it
[46:33] uses it uses two tens and five ones so seven coins of of inputs and
[00:00] it has let's say one out sorry sorry were you talking about cash send or
[46:38] are you talking about private send i'm talking about private send oh sorry yes it
[46:43] does come i'm not at cash send yet uh i'm talking on this so that
[00:00] it's clear so and a private send transaction which is the the term that the
[46:51] aj and i use for what that is is you're taking coin joined inputs and
[46:59] using that as your inputs coin joined outputs which you're using as your inputs to
[47:04] the next transaction and the output of that transaction is let's say 27 dash and
[00:00] that uses uh two plus seven so nine coins to do that and the output
[47:14] of that transaction is let's say 27 like literally the number 27 and so that's
[47:21] why you're saying aj that actually unmixes the coins because it actually combines the the
[47:27] previously mixed coins into one output that's no longer mixed so now so you you're
[47:33] combining all of the histories back together which is why you're getting that warning about
[47:38] more than 10 coins because when you combine so many coins you can't determine specifically
[00:00] which coin it came from but what you can tell is the probability of a
[47:47] coin it came from so you can come up with a cluster of coins and
[47:52] say it's 50 likely that it came from these cluster of coins and it's 70
[48:00] likely that it came from these three coins you know well and what it definitely
[00:00] tells people is that these these nine coins definitely belong to somebody that has control
[48:09] over them in one wallet so those nine coins were definitely controlled by one person
[48:16] um and the the cash send transaction that that you haven't fully described yet but
[48:22] i want you to describe now that i've given some more context that is actually
[48:30] a better transaction because even on the output side of that 27 dash transaction you
[48:40] have multiple outputs that are um it's not one output it's multiple outputs there you
[00:00] go yeah there's different terms we're flirting with in the beginning okay so now now
[49:00] you describe it uh now since i've given the context okay so what cash sin
[49:09] does in in its ultimate form there is no difference between a coin join and
[49:14] a private send with cash send a coin join transaction is a cash send transaction
[00:00] and a private send transaction is a cash send transaction so cash send is that
[49:21] you only use denominated inputs and you only use denominated outputs and there is a
[49:30] a happy bit where you get rid rid of the collateral because in cash send
[49:40] you only use denominated payments uh so there's two segments there's the segment that represents
[49:45] the value and there's the segment that represents the fee and so the first three
[00:00] zeros after the decimal place represent the value and the next five zeros after the
[50:00] decimal place represent the fee and that is that is a programmatic something that could
[00:00] be changed but it turns out that with our current fee structure that's the best
[50:05] way to do it uh for a variety of reasons and as long as dash
[50:12] stays under a thousand dollars that still works because the reality is when you do
[00:00] an exchange from francs to euros to dollars you're going to lose a few pennies
[50:21] and you don't throw a fit about it because they're pennies right like if i
[50:27] need to do a money exchange and the exchange rate says that for a hundred
[50:34] us dollars i should get 95 euros or british pounds or whatever but i end
[50:46] up getting ninety four dollars and fifty cents it's like you know it's not in
[50:53] real in real life transactions when we do a trade between um a financial system
[50:58] or currencies and we lose a few pennies like the tax is more than that
[51:03] in the traditional systems right so you just you're you're not concerned that something rounded
[51:12] down that it didn't round perfectly to okay i got 94.9978 you know like that
[00:00] that's not the way that that's not the way that you expect it you're okay
[51:19] with the fact that it rounds down and the person that's facilitating the transaction gets
[00:00] the bits that were rounded down in in their account essentially so that's that's one
[51:31] of the things is that there's the stamp value meaning the fee value and every
[51:38] coin is denominated in the top portion the important portion um the top portion over
[51:47] here i guess is denominated with the money that you actually spend the money that's
[51:54] useful and the bottom portion the dust is denominated for fees in orders of 200
[00:00] and so the way that the way that it works is you've got your uh
[52:04] here's here's the outline of all of the available denominations you cannot have denominations other
[52:10] than these denominations these are all of them of course you could have fewer if
[52:16] you wanted to do coin join on 1000 that probably you'd probably have to connect
[52:21] to a lot of nodes and wait a long time but you're also probably not
[00:00] going to be spending it right away so you know there there's that um maybe
[52:29] like in in practice we would probably still keep it to be something like 20
[52:36] to you know say let's go all the way down to 0.1 you probably only
[52:42] use these for coin join you probably wouldn't use ones that realistically you would get
[52:47] so few mixes that it wouldn't do you any benefit at the current time um
[00:00] but that would just happen naturally i mean that that wouldn't even be a thing
[52:53] of we have to explicitly define it that way if the protocol allows all of
[52:59] these and these are simply not available it's the same as not having them and
[53:05] if and if mysteriously they are available well then great you know we're we're we're
[53:10] no worse off so this is every possible denomination obviously it's uh more than three
[53:16] times more than the current number of denominations but like i said with the bell
[00:00] curve what you're going to be tending towards you know is the most somewhere in
[53:22] this region and then almost none down in this region almost none up in this
[53:30] region you know so so you're going to get that bell curve and that's going
[53:36] to define how quickly you can get those done um and then let's see if
[00:00] i if i had like another table or anything and then yeah the trailing the
[53:41] trailing bits are just fees and so every time a cash send happens fees are
[53:47] redistributed the dust just gets redistributed as part of the cash send so you never
[53:54] get a signal of like oh this was related to that because every time you're
[53:58] sending the denominations stay the same and the fees are slightly adjusted whatever the cost
[00:00] of the transaction is the fees are re-averaged across the coins yeah um and so
[54:07] yeah well i don't want to i don't want to get too much into details
[54:12] about like how the fees and the dust and the the stamps and stuff work
[54:20] i just wanted to give people a a brief um introduction reintroduction to that concept
[00:00] of cash tokens or cash cash send not cash tokens cash the key thing the
[54:28] key thing is that it uses hd wallets which none of the current software uses
[54:35] hd wallets they only use hd wallets most wallets do nowadays even no no no
[54:41] not not a single one not a single one uses hd wallets to send to
[54:44] that's what i was saying i think you're saying right none of them use hd
[54:51] wallets for the transaction so that's that's the other key thing right because you would
[00:00] give somebody your your um x pub for them so if if jojo and i
[55:03] are contacts i have an x pub that represents jojo jojo has an x pub
[55:09] that represents me whenever i need to send to jojo i'm not re-scan i only
[00:00] scan his qr code the one time that i create his contact any other time
[55:17] i need to send to jojo i just select him from the list and then
[55:22] my wallet is going to pick addresses that haven't been used yet and they're going
[00:00] to send you know the one the five the 0.02 it's going to send the
[55:30] denominated amounts off to jojo and this also makes it so that we'll be sending
[55:36] to multiple addresses that all belong to that person but the blockchain and anybody observing
[55:42] the blockchain doesn't necessarily know that um that that that's actually sending to one person
[55:47] they just they see inputs and they see outputs and there are many inputs and
[55:54] many outputs and that's what cash send is all about that's what we could have
[56:01] we could we could uh there's these and you can mix in cash send coin
[56:11] join transactions with cash send person-to-person transactions so you get like quadruple the benefits because
[00:00] even within the transaction you don't know which coins are a payment you don't even
[56:17] which coins there's no rotation exactly so there's no difference at the blockchain level um
[56:26] in a spend transaction versus a mixed transaction and that's that's kind of where you
[56:33] and i are going we've been going down this road in our heads for over
[00:00] a year now we haven't really we have done those dips uh but the first
[56:42] step uh the first step towards this is increasing the number of denominations for coin
[56:48] joins uh i i just i disagree that's the first step it doesn't because you
[56:54] can do you can implement the dip without ever touching anything in in that layer
[00:00] of the code the the dip can be implemented all the way up at the
[57:01] highest layer of the code sure where where the ui is touching it doesn't have
[57:07] to go anywhere near the blockchain code but yes to get the full advantage as
[57:13] far as coin joins concerned the first step towards improving coin join would be adding
[57:18] the denominations yes which is the topic of today's uh you know that's that's the
[00:00] topic today so that's why i was bringing it up as well uh so i
[57:23] think we've gone for almost an hour um is there anything else that you wanted
[57:30] to talk about uh your let's go back to the the tool again the the
[00:00] web the web um coin join interface anything else that you wanted to say about
[57:38] this plans moving forward um before we wrap up today i you know i don't
[57:47] i don't really know i i need to take a breather for a day or
[00:00] two uh from it because i i did a lot of high intensity work on
[57:55] it and uh you know for those people that do knowledge work you know how
[58:00] it goes and people who do physical work they know how that goes too because
[00:00] it's the same thing you know like you you do a real big push to
[58:04] meet any sort of goal or deadline and you need a couple days to recuperate
[58:10] we got a great little meme i share with my wife or it says that
[00:00] was fun now i'm gonna take a 21 hour nap yeah yeah yeah and that
[58:18] and that's that's kind of how i feel but um i want to get the
[58:25] cues i want it to get so that you can see which cues are available
[00:00] so like maybe put a little asterisk by the coins for which if you choose
[58:31] those coins you'll be able to mix them right away so as cues come in
[58:37] and cues have i don't really i have to go look up in the spec
[00:00] what the lifetime of a queue is because it times out after i don't know
[58:43] if it's 30 seconds or if it's five minutes but at some point a queue
[58:50] times out and so i think some of that information the main thing that that
[58:56] people might be wanting to know is when when is this going to support mainnet
[00:00] um oh it sure it supports mainnet as soon as i flip the bit but
[59:03] you know i've got the word for it i need to blank that out you
[59:10] know put hide that under when a little lock icon in a menu or something
[00:00] yeah and even when it does go to mainnet this will definitely still be like
[59:16] alpha don't use this unless you're willing to lose money kind of stuff no no
[59:22] no please stop saying that oh well that is that is both offensive and untrue
[59:29] this this is fully tested it goes by the spec if a transaction goes on
[00:00] the blockchain it is there there is no like because the ui is ugly the
[59:37] protocol doesn't work right it's like if you have an ugly email client it doesn't
[59:42] mean that because the email client is ugly the person might not get the email
[59:49] no this is production code this is not alpha code when we talk about the
[00:00] ability to do the coin processes so like i wish you would stop saying that
[59:55] because it's not true and it gives a false sense of insecurity i'm not talking
[60:01] to you right now i'm talking to the audience so please okay talk to the
[60:07] audience all right i'm saying to the audience do not use this code even though
[00:00] it's even though what despite what aj said if you are not comfortable with coins
[60:13] in a browser setting do not use this code if you are this is perfectly
[60:21] safe code that's what i'll say okay yes yeah certainly certainly you could clear out
[60:26] your browser cache and lose the money that's in the browser or not the browser
[60:33] cache but the browser application cache which is separate from the normal browser history cache
[00:00] okay fair enough all right so with that i think we'll say goodbye thank you
[60:39] everybody for joining in if you have any questions drop them in the comments and
[00:00] we will get back to you