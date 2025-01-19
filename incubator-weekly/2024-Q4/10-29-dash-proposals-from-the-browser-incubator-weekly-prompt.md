---
showLink: "https://www.youtube.com/watch?v=Z1RsH0bQ-EI"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Dash Proposals from the Browser | Incubator WEEKLY"
description: ""
publishDate: "2024-10-29"
coverImage: "https://i.ytimg.com/vi/Z1RsH0bQ-EI/sddefault.jpg?v=671fabc4"
---

## Song

### ChatGPT o1

1. Collateral Symphony
2. Epoch Overdrive
3. Masternode Alchemy

Verse

I calibrate code to conjure synergy
forging data flows locked in memory
block based proposals fueling energy
bridging trustless steps to the treasury
shedding the consoles aging legacy
refining protocols with cryptic chemistry

Chorus

Consolidate data with absolute precision
propel those concepts through fervent ambition
secure your vantage with purposeful volition
broadcast that outcome minus any permission

Verse

Local storage retains ephemeral progress
masternodes stand guard like a decentralized fortress
verifying each G object through a rigorous process
forging new references anchored by every address
testnet expansions spark dev labs with boldness
culminating in triumph that validates success

Chorus

Submit that collab with a method unstoppable
catalyze dreams through a route uncrushable
nullify friction with code incorruptible
ride these epochs with a force intangible

Verse

Freed from constraints we chase concurrency
refining frameworks to heighten efficiency
dissolving outdated queues with fluid currency
crafting a platform that thrives on propensity
dash central merges data with steadfast resiliency
expanded horizons proclaim unstoppable ascendancy

Bridge

Advance each concept with code and unity
foster each viewpoint under pristine immunity
harvest the future through blazing continuity
embrace fresh proposals igniting this community

Chorus

Submit that collab with a method unstoppable
catalyze dreams through a route uncrushable
nullify friction with code incorruptible
ride these epochs with a force intangible

## Episode Description

An overview of a web-based Dash proposal tool that streamlines governance and fosters wider participation.

## Episode Summary

This transcript focuses on a browser-based solution for creating and submitting Dash governance proposals, highlighting its potential to simplify and broaden community participation. Early on, the discussion covers the motivation behind the tool, emphasizing how it bypasses the traditional need for full-node setups. Technical explanations follow, detailing the JavaScript library used to generate and broadcast proposals, as well as its compatibility with both older and newer Dash software environments. The conversation also addresses proposal timing, fee payments, and practical steps to prevent mistakes when broadcasting to the network. Toward the end, the participants explore broader ecosystem implications, including potential competition for treasury funds, the benefit of storing proposal details on Dash Platform, and the possibility of future enhancements. Throughout, they stress reducing barriers for those who want to add value to Dash and encourage further experimentation and refinement of the submission tool.

## Chapters

### 00:00 - Introduction and Overview

In this opening segment, the hosts exchange greetings and set the tone for the conversation, noting that AJ has recently been working on a lengthy live stream. They briefly describe how he spent numerous hours developing and testing a browser-based proposal submission tool, intended to help individuals more easily submit Dash proposals without relying on command-line interfaces. This early discussion frames the project as both a technical achievement and a means to reduce friction for newcomers seeking funding through Dash’s treasury.

They also discuss the motivation behind simplifying the proposal process, emphasizing how many potential contributors have been discouraged by the complexity of operating a Dash full node. By creating a user-friendly web app that connects to Dash’s governance system, the team aims to bring more fresh ideas and competition into the Dash ecosystem. This introduction concludes with a promise to walk through the app’s functionality and highlight the library responsible for generating and submitting governance objects.

### 05:08 - Technical Overview of Dash Gov Library

Here, they shift to the specifics of the “dashgov.js” library. AJ explains that it abstracts the intricacies of Dash governance object creation, handling most of the heavy lifting involved in preparing, signing, and validating proposals. This approach lets developers focus on building custom user experiences, rather than reimplementing lower-level logic. The discussion illustrates how smaller pieces, such as cryptographic key management, have been modularized to keep the library lean and avoid unneeded dependencies.

They also touch on compatibility: the library is designed with modern JavaScript standards in mind, allowing it to work seamlessly in browsers and Node.js environments. AJ notes that the ability to interact with the Dash network through a clean, standalone library is critical for future growth. By providing accessible tooling, they hope to inspire innovative use cases and encourage more experimentation with Dash’s built-in funding mechanism.

### 10:00 - Implementation Details and Node ESM

As the conversation progresses, the speakers address challenges encountered while transitioning to ECMAScript Modules (ESM) in Node.js. They explain how Node’s evolving support for ESM has caused confusion in prior attempts to build cross-platform libraries. In earlier periods, developers had to rely on older CommonJS syntax or complicated bundlers, but recent updates have simplified the process of distributing packages for both browser and server environments.

During these minutes, they highlight how the new approach streamlines development, allowing dashgov.js to neatly import or export modules without elaborate workarounds. This technical leap reduces barriers for other developers who want to integrate proposal functionality into their own projects. By embracing these standards, the library is set up to remain compatible with the modern JavaScript ecosystem, offering a future-ready path for Dash governance tools.

### 15:00 - Understanding Proposal Time Windows

Next, they focus on how Dash governance proposals are inherently tied to block-based time intervals, rather than precise calendar dates. This detail can surprise new users who expect a simple monthly schedule. The speakers review how block production varies, sometimes quicker and sometimes slower, making it impractical to rely on exact timestamps when planning proposal submissions or payouts. Instead, the library estimates corresponding calendar dates based on recent block intervals, offering a usable approximation.

They go on to describe how each proposal includes start and end “epochs” that frame when voting occurs and when treasury payments take place. Listeners learn why it’s beneficial to include buffer periods in these time windows, accounting for network fluctuations or unexpected delays. By incorporating a safety margin, proposal owners can avoid missing payouts due to small timing shifts, ensuring that their efforts to gain masternode votes align with the actual superblock schedule.

### 20:00 - Checking G Object and Submissions

In this section, the speakers examine the process of validating a governance object (G Object) before it’s broadcast to the Dash network. The tool includes a preview function that shows essential metadata—like the JSON-encoded proposal details—to ensure everything lines up correctly. This is especially important since any mistake in constructing or signing a proposal can lead to the irreversible loss of the collateral fee, typically one Dash.

They also reveal that the application queries a masternode through RPC to verify the object’s format and readiness, mirroring the checks traditionally performed in a Dash Core console. By automating these steps, the web-based tool reduces user error, prompting the masternode to either accept or reject the submission. Although acceptance does not guarantee immediate visibility on popular proposal-tracking sites, it indicates that the request has been propagated into the network.

### 25:00 - Payment Confirmations and Broadcasting

Attention then shifts to the payment transaction that funds a proposal. Because Dash’s treasury system predates instant confirmations, a single block confirmation is still required before the associated governance object is recognized. The hosts explain that the tool coordinates both the payment and the proposal broadcast, waiting for on-chain validation to ensure everything remains synchronized.

They note the challenge in bridging older and newer parts of Dash’s protocol, describing how the application signs the transaction beforehand but holds off on fully submitting until the final checks pass. This approach shields users from losing their collateral in the event of a misconfiguration. By carefully managing the sequence of steps, the tool prevents common pitfalls that once plagued developers using manual command-line processes.

### 30:00 - Handling Proposal Data and Potential Issues

Here, they explore various edge cases and potential stumbling blocks, including how proposals rely on the masternode network for acceptance. If the proposal is broadcast at a time when blocks are mined slowly, for instance, it might not surface on aggregator websites as quickly as expected. The hosts clarify that once a masternode acknowledges the governance object, it can still take additional confirmations before the proposal becomes fully visible everywhere.

They also talk about potential naming collisions or repeating proposal titles, noting that although older tools suggested uniqueness was mandatory, the official network checks may not always reject duplicates. Listeners learn about the interplay between older assumptions and the present reality, where the new library’s robust checks ensure fewer surprises for users. By clarifying these quirky details, the development team aims to minimize confusion and thwart inadvertent errors.

### 35:00 - Local Storage and Recovery of Submission Data

Transitioning to user-experience improvements, the conversation turns to how this application stores data, such as proposal metadata, within a browser’s local storage. This approach helps safeguard against accidental closures or refreshes that would otherwise lose crucial sign-and-broadcast information. Since losing partial or complete proposal data can result in burning collateral, local storage offers a practical safety net.

They further explain why they’ve included an option to preview and preserve the final transaction hex. It allows advanced users to resubmit through alternative means or check their work for inconsistencies. This design acknowledges the wide range of skill levels in the Dash community, from those who prefer a guided, point-and-click method to veteran developers comfortable with raw transaction data. By capturing every step, the application helps mitigate the risk of failed proposals.

### 40:00 - Using Dash Platform for Proposals

In this segment, they highlight a new frontier: storing and retrieving proposal details on Dash Platform rather than relying solely on external websites like Dash Central. By leveraging platform’s data contracts, future proposals could embed full-text descriptions and supplementary materials on-chain, ensuring a decentralized, permanent record of their objectives. This concept could relieve the community’s dependence on single points of failure and guarantee more consistent accessibility of proposal information.

They stress how such an approach might unify the governance process, inviting third-party aggregators to fetch data from the same reliable source. While acknowledging that it’s not yet a formal standard, they see significant promise in using Dash Platform to manage proposal text, associated links, and identifying details. It would simplify cross-referencing and empower different websites to display uniform information without the risk of outdated or missing content.

### 45:00 - Competition, Treasury Limits, and Future Plans

Next, the speakers address the current economic landscape for Dash proposals. They acknowledge that the treasury budget is relatively small, especially in comparison to previous years, and that large allocations by organizations like Dash Core Group can crowd out other submissions. This competitive environment may discourage some developers from requesting funding unless they seek only modest payouts. The conversation touches on the tension between encouraging new proposals and recognizing the constraints of a limited budget.

Still, they maintain hope for the long term, anticipating the day when broader participation and potential protocol updates might create more funding opportunities. As they note, a core strength of Dash’s system is its capacity for direct, open competition, where proposals stand or fall on their perceived value to masternode operators. They underline the role of accessible tools as a means to promote healthy competition and new ideas in the ecosystem.

### 50:00 - Closing Thoughts and Next Steps

During these final minutes, the participants reaffirm their commitment to refining the proposal tool. They mention the possibility of generating QR codes to accept collateral payment from any mobile wallet, reducing the need to expose private keys in the browser. They envision further collaboration with designers and developers to create polished front-ends, ensuring a seamless experience for anyone—novice or expert—interested in Dash governance.

They conclude by reflecting on the broader significance of a straightforward proposal system. This feature sets Dash apart, granting the community direct access to treasury funds without centralized gatekeepers. The conversation wraps up on an optimistic note, reiterating the group’s excitement about expanding participation and building more decentralized solutions. Even with current budget limitations, they foresee the revised tools drawing additional contributors who can help shape Dash’s future.

## Transcript

[00:00] welcome everybody to incubator weekly today uh we've got aj with us today how's it
[00:00] going aj
[00:08] you recently did a marathon uh nine hour stream close maybe close to 10. um
[00:08] what were you working
[00:18] on uh proposal web app yes so that is the topic today um we are
[00:18] going to do a demo of this we're
[00:31] gonna uh i've i've sectioned off a little five minute clip of the uh the
[00:31] video the nine hour
[00:40] video so if people are interested they can watch the whole nine hour video but
[00:40] if they just want
[00:44] the summary of it's it's done and uh this is how it works and then
[00:44] we'll we'll go over your your
[00:51] proposal a little bit and then i'll talk about um how i plan to use
[00:51] this and uh yeah we'll go from
[01:00] there so let's let me get my screen share ready and i do also now
[01:00] have it up locally again so if we
[01:09] want to talk about it and have me click on buttons live okay i can
[01:09] share perfect
[01:13] let me uh yeah okay first of all um i guess i'll just take a
[01:13] brief look at the code uh this is on
[01:27] github.com slash dash hive the repository is called dash gov.js um that's the repo name
[01:27] um and as the js
[01:38] suggests this is a javascript library for submitting preparing submitting and paying for doing the
[01:38] whole
[01:48] thing proposal uh dash proposals from a web browser uh zoom that in a bit
[01:48] web app so uh this is the dash
[01:58] gov.js library so when i asked you to to work on this i i asked
[01:58] for a library i understand through watching
[02:06] the videos that uh it's a little difficult to make a library out of this
[02:06] because there's a lot of
[02:13] handshaking going on and business logic and developer user experience issues uh so i've actually
[02:13] used this
[02:21] i copied and pasted it into a web app that i was making um and
[02:21] i asked if you could update it so that it
[02:30] was has esm modules and uh mainnet support you went full steam ahead and built
[02:30] a uh it's not even it's
[02:42] not a uh reference app in the sense that it's not like complete because it
[02:42] is feature complete i've seen
[02:47] it uh we're gonna see it in a minute uh but this being a library
[02:47] uh people can download this library
[02:56] and um make their own web app if they want to change the way it's
[02:56] presented uh the the user experience so
[03:05] i'm just obviously not gonna go through this code i just want to give people
[03:05] a rough idea 637 lines of
[03:14] code you got a single export of dash gov that has a bunch of utility
[03:14] methods on it do you want to
[03:21] describe this uh library and what it does yeah at the high level it's called
[03:21] dash gov because it
[03:29] is dealing with governance objects now i don't know what all the use cases of
[03:29] governance objects
[03:33] are we know one of them is proposals but it's it's dash gov because it
[03:33] is uh surrounding the governance
[03:41] process and there are two pieces here there's the library and then there's the implementation
[03:41] the
[03:48] implementation i'll probably move into a different repository uh as i've done with the other
[03:48] libraries
[03:53] but the implementation was important to be able to test and make sure okay have
[03:53] i abstracted as much
[03:59] as i reasonably can while this stays just focused on governance and doesn't creep into
[03:59] transactions or
[04:06] key management and the other stuff because the in the ecosystem many people are not
[04:06] going to be using
[04:13] our full suite of libraries they're going to be using the legacy code that they
[04:13] have and then they're
[04:18] going to be wanting to bring in say dash gov and i didn't want dash
[04:18] gov to be dependent on the rest of our
[04:26] sdk because then that means that they got to you know pull in two sdks
[04:26] so this will work with any other
[04:34] dash sdk i mean i there's only really one other sdk but other nars so
[04:34] anyway that that's the the
[04:44] implementation side is where all of the business logic is that where it that's where
[04:44] it does some of
[04:48] the key management or all of the key management all the key management is done
[04:48] in the implementation side
[04:54] and we're looking at that right now right um you're looking at the html the
[04:54] the one the proposal app.js
[05:02] is where all of the the javascript logic is for that is the very bottom
[05:02] file in your file picker on the
[05:08] left okay so so this is this is the html file that we'll be looking
[05:08] at in a minute here uh the the rendered
[05:15] version of this so yeah 472 lines of html gives you a full web app
[05:15] it obviously does import it imports
[05:23] the proposal app library from proposal app.js um and this looks like some html helpers
[05:23] is that is that
[05:32] right so what i've done there what i've done there is the application the implementation
[05:32] is the proposal
[05:40] app.js and it's assigning it to the windows so that the click handlers can have
[05:40] access to it
[05:47] because what what do i need to push to get back to that code
[05:50] i don't know oh oh yeah upper left there you go all right proposal app.js
[05:50] let's let's take a look at this
[05:57] this is the implementation so this is how you use the library which is separate
[05:57] that's the separate um
[06:05] um dash gov.js right yeah and one important thing that has happened between in the
[06:05] last two months
[06:12] is that node has now fully adopted esm and it it will be published in
[06:12] version 24. it's experimental in
[06:23] version 22. so for the last 10 years node only had partial esm support it
[06:23] yes follow the spec ecmascript
[06:31] modules basically means javascript modules native to the browser and node and did lots of
[06:31] different
[06:37] environments for anybody that's not aware yeah so one one thing that we'll do uh
[06:37] sometime within the
[06:46] next couple of months is we'll change everything out to being esm because the goal
[06:46] before was that this
[06:52] should be able to be should work in the browser and in node without any
[06:52] transpilation and the reason for
[06:57] going with old style javascript is that is compatible with both node in the browser
[06:57] albeit with a little
[07:02] bit of clumsy stuff you have to do on the library side but not really
[07:02] much clumsy stuff you have to do
[07:06] on the implementation side now that esm is fully supported both in node and browsers
[07:06] have now matured
[07:12] so browsers introduced esm support back in march of 2023 and now node introduced it
[07:12] in march of 2024
[07:20] so now we've got uh enough time that that's matured that it makes sense that
[07:20] uh to move it over that way
[07:27] there's some of the typing features that were a little cumbersome if you were uh
[07:27] if you were using
[07:33] the common js modules that work in the browser and in node the typing is
[07:33] better with esm because the way
[07:41] that some of the package mangling that that had to happen on the library side
[07:41] did is simpler on the
[07:47] the uh anyway so that's why there's there's both windows things that are coming from
[07:47] the window and
[07:52] things that are being imported stuff that comes from the window obviously is compatible with
[07:52] every
[07:56] generation of javascript that's ever existed uh the new stuff it had broken compatibility but
[07:56] they they
[08:03] finally completed the shims to make it so that things can work nicely together so
[08:03] that was that was a
[08:09] a little bit of technical background as to why there's there's um primarily we were
[08:09] working with
[08:14] the old system before the old system was universal whereas the new system was not
[08:14] yet universal so so
[08:19] what you're saying if i could summarize that is you've got you've got a few
[08:19] different um objects that that
[08:25] we are sticking onto the window that it's getting it from the html file and
[08:25] that's because these these
[08:31] libraries that we've written before um are they were written with the old style um
[08:31] compatible with um
[08:40] since 1995 yes um and what you're saying is this library that we have here
[08:40] dash gov.js is is pure ecmascript
[08:50] module compatible esm compatible but the libraries that it depends on are not so you're
[08:50] sticking them on the
[08:56] window got it yeah well the implementation will depend on it so for example if
[08:56] you were using
[09:02] the legacy dash sdk then you would be you would be importing that here right
[09:02] okay all right so i think
[09:14] we had a pretty good preview of the uh we'll just take a look at
[09:14] the package jason just so people can see
[09:20] that overview um and then we'll so very few yeah there's no dependencies for the
[09:20] dashgov library
[09:28] itself it is completely standalone it will work with the legacy sdk or the new
[09:28] sdks um but there
[09:34] are dev dependencies for the implementation but like i said those will probably move over
[09:34] because i will
[09:39] i will create a proposals dot digital cash dev dot uh or did digital cash
[09:39] dot dev and i will i will move
[09:48] this proposal app over to there as a reference that anybody can copy it and
[09:48] then you know make it pretty
[09:53] and make it work better okay all right um so you're looking at yourself here
[09:53] this was this was that nine
[10:02] hour stream that i was talking about uh we're looking at the last seven minutes
[10:02] so we'll go ahead and play
[10:08] that real quick let me know if the sound comes through sound is not coming
[10:08] i need to fit i need
[10:18] to uh figure out how to do this because this is not the first time
[10:18] this has happened so if you give me
[10:23] the link i can i think i can patch my sound through let me okay
[10:23] check real quick let me send that to you
[10:32] and i'll actually just send this in the uh the main uh comments here so
[10:32] anybody can see
[10:43] where this is time stamped and uh look at the the chat to find this
[10:43] video so i'm going to switch this
[10:52] over you'll have to give me a thumbs up or thumbs down uh because i
[10:52] won't be able to i won't be able
[10:59] to speak because i'm going to switch it from mic to browser output okay and
[10:59] am i just uh are you going
[11:07] to be on your own screen or are you going to share a screen separately
[11:10] adding this to the stage you're on the stage
[11:29] okay okay now i'm not hearing the video coming through
[11:32] no sounds so far
[11:56] nope
[11:56] i don't i don't hear it anyway okay so let's just go back to you
[11:56] aj um
[12:07] can you
[12:09] okay now you should be able to hear me again i can hear you now
[12:14] yeah so i had the correct audio device selected i don't know why it wasn't
[12:14] um that's okay we'll
[12:20] just uh people have a link to it so they can check that out do
[12:20] you instead of doing that can you open
[12:26] up your yeah let's let's open it up and just do it real time uh
[12:26] okay we can even submit a test net
[12:32] proposal um right now if that works so
[12:36] yeah let me oh whoops
[12:41] uh okay so there's there's a minor issue with the test that stuff that's probably
[12:41] going to prevent it from
[12:49] working at the moment let's do mainnet then you've already tested that we won't actually
[12:49] go through
[12:54] and submit it unless you feel confident enough right now but um yeah i don't
[12:54] want to debug it right
[13:01] now it's it's uh it's a typo and a variable name on the test net
[13:01] code but it's i yeah i don't want to
[13:06] debug it live well so let me just go let me just go through so
[13:06] first thing is the way that the proposals
[13:13] work is by block so it's not by date it's by block but um there
[13:13] is a little bit of gaming
[13:19] that happens with the block so you'll notice that blocks will go like it'll take
[13:19] 15 minutes 15 minutes
[13:24] and then it'll go two minutes two minutes two minutes and that's because basically there's
[13:24] a
[13:28] big group of miners that what they're doing is they put pause on all of
[13:28] their miners for half an hour
[13:35] let the difficulty go down and then they press resume on all of their miners
[13:35] and then they reap
[13:39] it really quickly and so that's how they're they're getting their profitability um so with
[13:39] that the
[13:46] accuracy of the date has gone down from a resolution of about three minutes to
[13:46] a resolution of about 20
[13:52] minutes but still that's a pretty decent resolution so six months in the future we
[13:52] can know within about
[13:59] 20 minutes when the vote deadline and the pay etc will will be so what
[13:59] we have here is three dates
[14:08] that are estimated based on the last uh i think it's 25 000 blocks so
[14:08] it takes the last 25 000 blocks
[14:15] does an average and then based on that it's projecting in the future what what
[14:15] date and time
[14:21] is is likely to be that the the blocks uh land so we have the
[14:21] submit after date which maybe there's a
[14:29] better name for this but this is basically these these proposals will be dated to
[14:29] start at this date
[14:37] and then the expectation is that the vote is going to happen within 20 minutes
[14:37] of this time and the
[14:44] time resolution is just set to uh 15 minute increments uh because it showing more
[14:44] than that is somewhat
[14:53] deceptive because it's not that accurate and then the pay date is similar so it's
[14:53] rounding up for the submit
[15:01] after it's rounding down for the vote deadline then it's rounding up for the pay
[15:01] date and in terms of
[15:07] trying to get as accurate as it can within that 15 minute window so that's
[15:07] that's just showing these
[15:13] are the next proposal periods is what we're looking at so if i say i
[15:13] want to start at the very next proposal
[15:19] period a lot of times you want to do that sometimes you don't the reasons
[15:19] that you might not want to do that
[15:24] is because you may have um you may have what what i call the lame
[15:24] duck period like for example there's
[15:36] only four days left before the voting deadline so you might actually want to start
[15:36] your proposal at the
[15:42] next one since you know unless it's you could get it in in the neck
[15:42] in the current voting cycle but with
[15:49] only four days left of voting it's not wise yeah so anyway here this is
[15:49] this is just the same visual
[15:56] representation that i had done for the command line but adapted to the web where
[15:56] we show okay here's your
[16:02] voting window we can make that you know you could do one payment you can
[16:02] do six payments you can do
[16:09] whatever but it's going to show you this is your window that you're going to
[16:09] submit uh after this time
[16:14] and you're going to get paid up until this time so that is your proposal
[16:14] window that you're looking at
[16:21] so most times people would probably have a start period of either one or two
[16:21] yeah
[16:29] okay yep so that's that part there then the amount that you want to get
[16:29] paid for each period so say
[16:39] it's 10 dash or 100 dash or 200 dash or whatever it is there's the
[16:39] total dash that you'll get if it
[16:47] passes for each of those periods then you have to have a url safe proposal
[16:47] name so this was the proposal
[16:55] name that i had used last you need to have a url can be any
[16:55] url doesn't need to be dash central if
[17:02] it's not dash central then dash central will just pick it up and then uh
[17:02] you'll be able to claim it
[17:07] and by the way you can claim using either the dash message tool that we
[17:07] just published for javascript
[17:12] or the dash message tool that is already available on webinstall.dev that's written in go
[17:12] either of those
[17:20] tools work with the dash central and other types of dash voting so i'll put
[17:20] that link in the and the
[17:28] thingma bob here okay all right then you have your payment address where you want
[17:28] the money to go to
[17:37] and that's enough that you can see a preview of if you wanted the technical
[17:37] information for what does this
[17:43] look like you've got the proposal json now something that's different about this from previous
[17:43] tools is
[17:50] that the epochs are actually noted in the code with a watch out this is
[17:50] dangerous people lose money
[17:57] because the you meant epic though by the way i'm just kidding whatever it's an
[17:57] inside joke uh people
[18:04] may find me for calling it epic so epoch yeah you're you got the nerd
[18:04] lingo going on so go ahead yeah so
[18:11] it doesn't make sense that it was ever down to the second because it's you
[18:11] know because because i don't
[18:19] know how the other tools did it but they kind of just picked a random
[18:19] time in the past and a random time
[18:24] in the future which doesn't really make a lot of sense because the proposal is
[18:24] based on blocks it's
[18:29] not based on time and so for the start and in epic what we do
[18:29] here is we just calculate the epic
[18:35] based on the did you just get me to call it epic sorry whatever so
[18:35] we we have the the start and end
[18:47] are based on the block time so what this means and i i actually am
[18:47] not entirely sure what this means
[18:55] but i think it means that you will not get paid for any activity that
[18:55] happens before the start epoch
[19:02] and you will not get paid for any activity that happens after the end epoch
[19:02] now we're going to see
[19:08] with my proposal because my proposal had a start epoch that was future dated so
[19:14] my i submitted it at 6 a.m and it was not set to start until
[19:14] 6 p.m so the question is
[19:22] what happens in terms of the voting i think the votes count at any time
[19:22] but it's just that if
[19:30] people had voted on it and i had actually submitted the start epoch before the
[19:30] voting window had closed
[19:36] and it got enough votes that it could have been paid that it would not
[19:36] be paid
[19:41] technical detail about the time window but i i think that's what that means anyway
[19:41] the point
[19:46] that i was getting at the short of it is that our start epoch and
[19:46] end epoch are based on the widest
[19:52] reasonable window of the of the the period which means three days after the last
[19:52] payment until three days
[20:03] after the final payment that means that if something were to happen like for example
[20:03] the chain halt were to
[20:09] happen again there could be a little bit of leeway so that you would still
[20:09] get that final payment if that
[20:15] final payment somehow got delayed uh you know right the day before there was a
[20:15] chain halt and then there
[20:22] wasn't enough time for it to rubber band back to its its normal um time
[20:22] increments i mean that's highly
[20:29] unlikely to happen but that's that's what this does so there's there's as far as
[20:29] i'm aware and somebody
[20:34] please correct me if i'm wrong there is no technical or practical reason to have
[20:34] a random start epoch or a
[20:40] random end epoch it makes the most sense to base it on the block times
[20:40] of when people would be voting so
[20:48] yeah it's just one of those implementation decisions i think that somebody made to to
[20:48] give it some kind of
[20:56] time based estimate but you're right that um the proposals this was my understanding is
[20:56] that you
[21:03] basically want to bracket your start and your end uh epoch to something something in
[21:03] between the super
[21:11] blocks that gives you a reasonable buffer so that the the actual payment is happening
[21:11] based on the the super
[21:18] blocks but those uh epochs are supposed to just uh kind of approximate how many
[21:18] payments you'd get if
[21:26] you spread them out like say three months apart uh and if you bracketed them
[21:26] properly then you'll get
[21:32] three payments i think that's what you just said though so yeah so so the
[21:32] epochs you don't have to
[21:38] worry you're not going if you were to recreate the same the same proposal and
[21:38] you knew what date you had
[21:45] created the proposal on you could actually tweak the library to give you back the
[21:45] same information
[21:50] so you don't have to worry about oh i you know i was working with
[21:50] the library and it turns out that
[21:55] i had a bug in my implementation and now oh no that money's lost not
[21:55] the case because you can you can
[22:02] idempotently recreate the same proposal json as long as you as long as you have
[22:02] a very approximate
[22:11] time stamp you know within the same couple of days so that widens it from
[22:11] it has to be you know you
[22:16] have to have that exact second stored somewhere or a screenshot of it too as
[22:16] long as you have a rough
[22:21] idea of like it was this day or that day you can just you can
[22:21] just recreate the proposal json for you
[22:27] know one two three days and then you'll you'll get you know it'll it'll get
[22:27] the right thing so there
[22:33] that's that's that that's just you know technical thing that was before was risky and
[22:33] now is not
[22:40] then the collateral let's see if i can get i'm going to export something over
[22:40] here
[22:49] with my wallet i'm going to export looks like this one
[23:03] okay
[23:03] all right so i just generated a whiff that has the amount that we need
[23:03] on it and then you can see
[23:14] here it it's filling in with info so again not something you need to know
[23:14] just technical details
[23:21] for debugging uh or for those interested so this is how much how many satoshis
[23:21] make up this dash
[23:30] and so it's it's 1.00 dash plus 3600 dust so that's enough to pay the
[23:30] fees that meets the burn criteria
[23:41] and then i we can do a preview and then it runs and says hey
[23:41] it passes a master node validation
[23:46] which is actually kind of funny because it shouldn't because this proposal name is a
[23:46] duplicate
[23:52] but uh there may be some additional checks that the math or maybe they don't
[23:52] maybe you're allowed to have
[23:57] duplicate uh submissions i i guess that's just something that we we believed before and
[24:03] until just now maybe we can test that on testnet and see see what happens
[24:03] if you do a exactly identical
[24:09] proposal name yeah because this is this is actually communicating with the master nodes and
[24:09] it's
[24:14] saying here is the g object that i'm going to submit what do you think
[24:14] about it it's like it's literally
[24:20] the rpc grpc check g object check right yep yep yep that's what it's doing
[24:20] and so if i were to hit submit
[24:29] then we would see what was in this video so let me see if i
[24:29] can just fast forward this a little bit
[24:36] um okay that was maybe too far
[24:38] i don't know where exactly you'll get there okay
[24:44] because we could just watch this part and then you'll see
[24:49] uh fortunately it was actually pretty quick i probably happened to submit it right when
[24:56] uh oh there okay so let me back up just a little bit here i
[24:56] probably managed to submit it right when
[25:04] the the uh adversarial uh worker nodes were doing their you know pause and resume
[25:04] and they were in a resume
[25:13] phase because it can take up to 15 minutes when they're in their pause phase
[25:13] of of the game and then
[25:19] when they're in the resume phase it's like you know super quick block times
[25:23] okay so that one i had already oh that's because i did it once before
[25:23] okay so we should see this okay
[25:37] hey now i've had enough confirmation oh i'm hearing the sound now let's see is
[25:37] there something else it's got
[25:44] enough confirmations
[25:54] all right get address balance
[25:58] yeah so i was waiting for it to get confirmed you can't use you can't
[25:58] use a instant send transaction for a
[26:10] proposal like you can with most things because i believe the proposal system was created
[26:10] before
[26:15] the instance and system was created system it is an instance that all transactions are
[26:15] instant send by
[26:21] default but it doesn't wreck the proposal system doesn't recognize instant send as being confirmed
[26:27] enough to recognize it so yeah it has to be it does wait for one
[26:27] block yeah it has to be in the pool
[26:37] okay all right passes validation great
[26:40] and i'm just going to go
[26:45] there we go digs by the way seven says what's up it's my proposal start
[26:45] now
[27:07] okay so it it does log the pulls the network it's that checking again every
[27:07] five seconds is looking
[27:23] for the block to confirm one block confirmation yeah so one of the things we
[27:23] did here is it fixed
[27:31] another one of the bugs in the dash core implementation the dash core implementation
[27:37] actually sends the the transaction before it's ready to send the g object and so
[27:37] this creates a
[27:47] situation where people in the past had lost money and so what we do instead
[27:47] is we run all of the build
[27:53] up and all of the checks and all of the signatures because you don't actually
[27:53] need to know what you
[27:58] you don't actually need to have the transaction published to the blockchain to know what
[27:58] its id
[28:02] will be when it goes into the blockchain so we actually do the signature and
[28:02] id phase ahead of time
[28:09] so that we know that everything is in concert everything is as valid as it
[28:09] can be checked we know that before
[28:17] we submit the payment and so what this is doing is it actually submits the
[28:17] payment and the g object at the same
[28:23] time which means that it has to wait for the confirmation of the transaction payment
[28:23] before the
[28:31] governance object will become valid and so that's why it's doing this check again check
[28:31] again check again
[28:36] because we are not optimistically assuming that everything was right we should just go ahead
[28:36] and pay
[28:43] we're delaying the payment until the very last moment so that we know that everything
[28:43] that could have been checked
[28:49] signed etc is checked and signed etc oh okay i actually thought that it was
[28:49] after you had paid
[28:57] and it was looking it was waiting for a confirmation on that block but i'll
[28:57] have to look at that again
[29:02] um it is it is waiting for the confirmation on the block but what i'm
[29:02] saying is the check runs before the
[29:10] payment not after the payment so in order to do the check you have to
[29:10] have the transaction id and so when we
[29:15] do the check we actually create the transaction id by signing the transaction without broadcasting
[29:15] it
[29:22] okay and so it's not until that it's not until we're ready to do the
[29:22] broadcast that we make the payment so
[29:28] the the governance object broadcast and the transaction broadcast are happening simultaneously so that we're
[29:35] not having you know potentially lost money and that money is burned so it's it's
[29:35] gone forever it's not
[29:42] given back to the community it's not contributed to the miners or the masternodes this
[29:42] was in a prior
[29:47] area so that's just a flat burn hopefully in the future that'll you know somehow
[29:47] be recovered but
[29:52] but right now it's it's burned all right i think i'm gonna i think i'm
[29:52] gonna hit the hay like some
[29:57] follow if you want to uh i will go ahead and give so some uh
[29:57] mikhail shenmick says i'm gonna use this
[30:06] tool for magic's proposal soon so that actually is a good lead into um unless
[30:06] you wanted to say anything
[30:12] before we left the the demo um aj i wanted to talk about why i
[30:12] went through the trouble of doing this
[30:19] uh and i think that there's a little bit more work that um could be
[30:19] done on this um sure finish uh finish
[30:26] what you were saying with the the demo if any if anything otherwise um i
[30:26] did want to actually mention
[30:31] yeah did you have anything to say first of all the one last thing one
[30:31] last thing which is what shows up
[30:35] here it says success it may take a few hours to show up on dash
[30:35] central etc so i want to bring up my
[30:41] proposal yep and i'm going to scroll down i've submitted this proposal twice so i
[30:41] manually update this so
[30:51] here's a link to rpc.digitalcache.dev and you can see here the output that's weird unknown
[30:51] oh because
[31:02] it's dead now interesting yeah okay so okay so these so this is interesting and
[31:02] i didn't actually know
[31:10] this part i think i had we talked about it at one point but i
[31:10] know it so my my um my previous proposal
[31:17] has expired that isn't committed to the blockchain so now the previous proposal object is
[31:17] gone and
[31:25] so now it says unknown governance object and over here my new proposal it shows
[31:25] all of this but this
[31:31] is just in memory in the masternodes it does not exist in uh in the
[31:31] blockchain but the point that i was
[31:39] making is that once you've had success and the masternodes have accepted your governance object
[31:46] i have not seen it take less than i think maybe the minimum amount of
[31:46] time i've seen is 15 minutes
[31:52] so i don't know if it's based on block or it's based on something else
[31:52] but i've seen it take an
[31:56] hour or two for from the time that you get the success message until the
[31:56] time that it shows up in
[32:04] the governance object output so if you run through this and it's not showing up
[32:04] immediately there's no
[32:11] cause for concern if you've got the success if it passed the check if the
[32:11] masternode
[32:16] accepted it you're good to go but there is just a little bit of a
[32:16] delay that i don't know why that
[32:23] i don't know what that delay is caused by but it seems to be something
[32:23] more than just a single confirmation
[32:30] of the transaction before it shows up in the governance uh data so just just
[32:30] be aware of that
[32:37] that that's because that's something you can make it go yeah i think actually technically
[32:37] what's happening
[32:42] is um there is something in the in the dash core implementation that says let's
[32:42] wait for six
[32:53] confirmations six blocks to present this as a governance object to the network something like
[32:53] that
[33:02] so there's the one block that you have to wait for the um for that
[33:02] burn one dash burn transaction and
[33:09] then there's six blocks that you have to wait for to see it on the
[33:09] network um so it is it's not arbitrary
[33:17] it's actually you know sometimes six blocks happens in 30 minutes and sometimes six blocks
[33:17] happens in
[33:23] three minutes um but typically not um typically it's six times two and a half
[33:23] so um anyway um
[33:33] i wanted to now uh talk about why i did this why why why i'm
[33:33] funding this you're partially funding this
[33:41] on your side as well we both believe in this uh this application and personally
[33:41] i think that the thing
[33:49] that dash has that's unique to all blockchains no other blockchain has the ability for
[33:49] developers or
[33:57] or marketers or any anybody that can add value to dash hopefully in the future
[33:57] and near future merchants
[34:05] even um to uh to request dash from the dash blockchain natively without any kind
[34:05] of you know permission
[34:16] required i try to help the process i'm going to try to try to help
[34:16] the process for developers to to submit
[34:23] their proposals i want to make that as easy as possible because the best thing
[34:23] that we can do for
[34:29] dash is get a lot of different people competing for who can add the most
[34:29] value to dash whether that's
[34:36] more developers more marketers more merchants whatever that is i i feel like not enough
[34:36] people know about
[34:44] this feature or ability in dash and even fewer people that maybe even know about
[34:44] it are willing to
[34:53] go through the trouble to submit the proposals because it requires a multi-step process currently
[34:58] where that multi-step process involves setting up your a full node and all sorts of
[34:58] things and we don't
[35:06] want to limit people um in any way we want to remove as much of
[35:06] the burden of as many of the barriers as
[35:14] possible uh to proposing uh to get funded for certain things so um yeah i
[35:14] have one one thing that that i'm
[35:26] seeing that this application does not yet do but in pre in the pre-call show
[35:26] the pre-show call that we had
[35:34] you mentioned that you mentioned that it's in your your plan to add just a
[35:34] qr code that if somebody doesn't
[35:40] have you know somebody doesn't have a wallet that they're gonna submit a whiff to
[35:40] we want a qr code
[35:47] that somebody can just scan and say here's the 1.001 dash payment for the proposal
[35:47] i'm gonna scan that and
[35:56] the web app's gonna gonna do that payment part for me as well uh because
[35:56] not a lot of people will know
[36:02] how to get a whiff with 1.001 dash on it yeah i realized that after
[36:02] the the fact well it's nor
[36:10] should they be really that people shouldn't really be doing i know that you know
[36:10] you you you are
[36:16] comfortable with throwing whiffs in into applications and things but it's really probably not the
[36:16] best
[36:22] practice um so i don't know i we'd have to make that argument separately yeah
[36:22] either way we're gonna have
[36:29] the ability to scan a qr code to pay for this yeah i think what
[36:29] i'll do is i'll just put up a
[36:37] a uh a simple wallet kind of like how i've got the coin join wallet
[36:37] i think i'll i'll create
[36:42] something like that where there's you know you can either put in or generate a
[36:42] phrase and then you can
[36:48] either put in or receive an index and get the qr code and just have
[36:48] it be two i'm thinking it might
[36:54] be just two separate apps like step one fill out this information step two either
[36:54] paste a whiff that you
[37:00] have or go load one over here that just not that this shouldn't have the
[37:00] qr code directly in it
[37:07] but just as uh what you know we come up with so many situations where
[37:07] we need to load and address
[37:13] i might as well just create a tool that's specifically for the purpose of loading
[37:17] and and link that to this again i i don't know if i want
[37:22] that the tools that i'm creating they're ugly they are i don't want to say
[37:22] okay yeah i i like
[37:31] well i don't i don't want to say that they're proof of concept because that
[37:31] sounds like they're incomplete
[37:36] but they are someone else needs to come along and uh you know hopefully we
[37:36] can we could work
[37:44] together and form a relationship at some point but somebody else needs to come along
[37:44] and say hey i'm a
[37:48] designer i want a proposal to take aj's thing and create the design for it
[37:48] and then somebody else needs
[37:55] to come along and say hey i i want to uh implement this design or
[37:55] you know there's something like that
[38:01] needs to happen because i'm not going to flesh these out first of all i'm
[38:01] not a front-end guy
[38:07] right like i don't do css uh this is not this is not my strong
[38:07] suit like i'm i'm down at the protocol
[38:15] layer i'm not going to be up at the css layer but i just want
[38:15] something that's like okay as a developer
[38:21] if you're going to build your own tool you need to see all the debug
[38:21] information you know you need to
[38:27] be able to see this is what the transaction json looks like okay when i
[38:27] use the library
[38:32] did i get the same result as what's shown in the demo application okay i
[38:32] did great that means that
[38:38] i implemented it correctly oh it looks different uh maybe i passed in some wrong
[38:38] arguments maybe i need
[38:43] to submit a bug report because there's some checking that's not happening that should be
[38:43] checked to prevent
[38:48] me from passing in wrong arguments uh you know do these things look right and
[38:48] then how are you gonna so
[38:55] this tool one of the things that it does is it actually saves all except
[38:55] for the whiff
[38:59] it saves everything in local storage so if i were to open it up it
[38:59] actually let's see i have to do
[39:05] something to have it show this in there let's try this way yeah so
[39:11] in the console it actually still has all the stuff from the command line because
[39:11] the command line was just
[39:18] doing console logs but if we go into application here and we look in storage
[39:18] so you can see here
[39:27] these are my submissions and and so one of the concerns with the the dash
[39:27] core console has has you know
[39:37] well documented in the forums and even in the code is people lose their submission
[39:37] data and uh you know something
[39:45] something goes wrong they come back to it the next day they lost their money
[39:45] so here
[39:49] even if something were to have gone wrong
[39:52] we've got the relevant data is being logged into
[39:57] local storage so we can go back we could take a look we can recreate
[39:57] this
[40:03] we can make sure that your funds get applied in the right way you know
[40:03] yeah and as you know and as much
[40:10] as we we can because there may be some conditions that uh you know there's
[40:10] there currently may not
[40:17] exist any checks for it all because up until this point as far as i'm
[40:17] aware i could be wrong i don't
[40:22] think anybody's ever made a proposal outside of dash core i think i'm the first
[40:22] person to ever make a
[40:27] proposal outside of the dash core console yeah and you know and technically to be
[40:27] completely precise we are still
[40:37] using dash core um because your rpc service does do the rpc submit through dash
[40:37] core um but right yes yes
[40:49] so so the rpc translates it from an rpc message to a p2p message which
[40:49] is then broadcast
[40:56] to a master node that that full node is connected to but none of the
[40:56] processing of the governance object
[41:06] or the transaction not none the dash core console is not used this does not
[41:06] use any part of dash core
[41:17] to construct the messages dash core is only being used as a relay service to
[41:17] say here are the bytes that
[41:23] need to make it to a master node send these bytes to a master node
[41:23] yep yeah well okay there's a little
[41:29] bit more than that in the submission process because of the way that dash core
[41:29] is constructed it actually
[41:36] deconstructs and reconstructs the message but but yeah the point being this all of the
[41:36] work is done
[41:43] client side such that you could take this json object and give it to anyone
[41:43] and they could take the
[41:51] the data hex out of it and they could they could submit it to the
[41:51] network by any means and it will
[41:57] it is the the data and that actually has happened before on a main net
[41:57] proposal um several i think two
[42:06] or three months ago ash was having some weird issue with his wallet he submitted
[42:06] a proposal paid for it
[42:14] fortunately still had the uh the records uh open on dash core so he could
[42:14] look into his console
[42:20] but his his wallet was not submitting it he was trying multiple times he gave
[42:20] me the hex i actually
[42:26] submitted it from my wallet i didn't have to pay for it because it was
[42:26] already paid for but because i had
[42:31] that hex data i submitted it and it went through fine so stuff like this
[42:31] has happened before it's not a big
[42:38] deal um but it is helpful to have that data persisted at least into local
[42:38] storage that actually leads me to
[42:46] one other thing that i wanted to talk about i'm going to share my screen
[42:46] if you're done um yeah go ahead
[42:53] and talk about a little bit more of the motivation um so again there are
[42:53] other tools that that do this
[43:04] proposal creation but they all involve uh the final step of okay now paste these
[43:04] commands into your uh into
[43:13] your dash core wallet so now you have this unfortunately i don't have a link
[43:13] to to show
[43:19] your latest tool but we just saw that the the one yeah it's not public
[43:19] yet i i will make it it was 6
[43:26] a.m so i was i just went to bed by the time i was done
[43:26] i didn't bother with the last hour of actually
[43:32] setting up the domain and publishing it to get hub pages yeah so a few
[43:32] weeks ago some of you that are
[43:40] watching may have seen i did a demo of this little application proposals dot dash
[43:40] platform dot app
[43:46] the purpose i asked you aj to to make a library for that i i
[43:46] pasted it in um so i was already doing
[43:56] this proposal uh submission thing before you did your big uh 10 hour refactor um
[43:56] but what i'm gonna do now
[44:04] is now is now that it's in an easily ingestible uh es module i'm gonna
[44:04] update this little application
[44:12] see if it still works and then the idea here is that um in in
[44:12] your application you're still assuming that
[44:20] people will then go to dash central and fill out the body of their proposal
[44:20] what i want to do with this application here is i want to give people
[44:20] a way of being able to
[44:32] uh fill out the body of a proposal um and store it on dash platform
[44:32] and possibly also including that
[44:42] metadata that uh we were just talking about that with the hex data and and
[44:42] all that uh ephemeral ephemeral
[44:49] data that would otherwise be lost once you closed your dash core console or if
[44:49] or if you cleared your browser
[44:56] history um people could potentially save that metadata onto platform when they're submitting their proposal
[45:03] as well so there's a few different reasons for wanting to do this i want
[45:03] to test um the just creating
[45:11] an app with the dash js sdk um and i think this is a good
[45:11] a good way to test that and also i do want
[45:19] to kind of reorient the community a little bit to at least trying out this
[45:19] alternative of instead of
[45:26] requiring everybody that wants to submit a proposal to um to create a dash central
[45:26] account as well
[45:35] again trying to remove barriers by the way my my the body of my text
[45:35] is on my own blog which happens to be
[45:47] happens to be hosted on github pages not because there's anything special about github pages
[45:47] well
[45:52] other than that i was able to put an automatic hook where every time i
[45:52] add or edit a file it republishes
[45:56] it automatically but you know aside from that and it does it with hugo so
[45:56] you could do that with
[46:01] with other tools but but the the thing that the reality is that people are
[46:01] gonna have to interact
[46:08] with dash central if they want to interact with the people who are doing the
[46:08] voting so that's it's not
[46:14] about the body of the text one with one caveat sure um if dash central
[46:14] if they implemented a feature on their
[46:24] website where instead of instead of instead of instead of just right now what the
[46:24] default is is it will say
[46:29] if it if you haven't entered in proposal text uh in dash central itself it'll
[46:29] just have a generic
[46:37] body that says go see this website which is the website that uh is listed
[46:37] in the actual proposal
[46:46] uh on the network so like you're saying technically the uh the proposals can list
[46:46] any any website that
[46:55] they want uh and that's by design that's supposed to make it decentralized so that
[46:55] you don't have to
[47:02] rely on any um any kind of um uh any operator to run this proposal
[47:02] system now what's happened over time
[47:11] is that dash central has become the place that people uh submit their proposals and
[47:11] their proposal body
[47:19] but if dash central if this idea did take uh root and people wanted to
[47:19] leverage dash platform for this
[47:29] feature dash central could um we could add um in the proposal you could add
[47:29] the contract identity
[47:39] that says here's the here's the contract um you could put it in like the
[47:39] slug of the url for example
[47:47] you could put the slug uh the uh the contract id and then other websites
[47:47] like dash central could go to that
[47:56] and and and get the proposal body text as well and so they could they
[47:56] could display what's on dash
[48:03] platform so anyway i don't want to go through all the details i haven't actually
[48:03] figured out all the
[48:07] details but i do think it's worth uh exploring that idea of maybe maybe it
[48:07] makes sense to have proposal
[48:15] data natively on dash platform and then these other sites that present that data can
[48:15] use dash platform as
[48:23] a source of as a source of truth not necessarily the source of truth but
[48:23] a source of truth
[48:28] i like that idea i i am kind of it does seem weird to me
[48:28] that we don't have a official permanence
[48:38] for the dash governance objects i i mean i guess maybe we could argue well
[48:38] there's no technical reason to but
[48:44] or even the there's actually no sense of robust permanence for even the the body
[48:44] of the proposal
[48:53] text like if dash central decided which they won't like we all trust dash central
[48:53] but um if they decided
[49:01] or for whatever reason you know bus factor kind of thing gets in and and
[49:01] and dash central is unavailable
[49:09] that data is gone um we only have the data of the of the proposal
[49:09] texts because dash central continues to
[49:19] um to serve us but again might be a good idea for for dash uh
[49:19] for dash platform itself i mean we did we did
[49:28] build this thing uh to store uh to store data so if we believe in
[49:28] that idea then we might want to use it
[49:38] so anyway um we've gone for 50 minutes now i know you've got a stop
[49:38] actually i think we're already over
[49:48] your time so yeah i'm joined in on my other my other meeting i'm just
[49:48] waiting to unmute myself
[49:55] over there okay so we'll we'll let you go um any any final words though
[49:55] regarding the web app that
[50:01] you've created and uh person like i i can tell you that i'm actually going
[50:01] to line up several
[50:08] developers to use this tool to submit small proposals i already have at least four
[50:08] in mind
[50:16] that i want to um direct to using your application um and that will help
[50:16] us test it out test out the
[50:26] the user experience and um yeah there will be more in the future so i
[50:26] don't want to we've already gone
[50:33] over time so i don't want to talk too much about that but i've got
[50:33] several uh small proposals that
[50:38] uh i'm i'm having these developers uh submit on their own i don't want to
[50:38] be the the gateway to
[50:46] uh i all the proposals in the incubator i want them to have their own
[50:46] proposals i so i would like to
[50:53] submit some more proposals as you know like so i i had to step away
[50:53] for a little bit because with
[51:01] incubator changing drastically and the price of dash going down and just you know the
[51:01] financial situation
[51:08] i had to focus on some other clients and there's there's some stuff i'd really
[51:08] like to be doing in
[51:12] dash but i'm also a little worried if i would actually be able to get
[51:12] funded which i guess if
[51:18] i'm not that's fine because that just means that's that's not what the master note
[51:18] owners want but
[51:23] there's so little money available in the pool right now and dcg is pulling i
[51:23] think uh 400 dash supplemental
[51:32] and so i i think some people are choosing not to vote on proposals uh
[51:32] that may be good proposals
[51:38] because they they want to wait for that last minute for dcg to put in
[51:38] their their extra 400 to 600.
[51:45] um so it the an honest question in my mind is okay we have this
[51:45] tool is there any room for anyone to
[51:52] actually make a proposal other than you know getting a token payment well there's not
[51:52] there's not yet or now
[52:00] and there may be in the future either due to price increases or um something
[52:00] other than that like
[52:09] we have increased the the treasury allocation before so there's no reason that we couldn't
[52:09] do that in the
[52:15] in the future it's not a it's not a topic i'm bringing up at this
[52:15] point but there will be potential in the
[52:23] future um and then also people should feel like they can compete with with dash
[52:23] core group uh there's
[52:32] there should be nobody in the community that um that thinks otherwise because these are
[52:32] just proposals
[52:38] right they're just saying um i would like to do this and i think even
[52:38] dcg would support other people
[52:47] trying to submit proposals because that's what's best for the network nobody wants um nobody
[52:47] wants
[52:53] a monopoly it's only a become a monopoly to some degree with dcg taking whatever
[52:53] 80 70 of the of the
[53:02] total funds because honestly uh people have found that dcg is doing a better job
[53:02] than anybody else who's
[53:11] asking for funds so but the minute somebody else asks for funds that is providing
[53:11] more value to dash
[53:20] then they will get funded um so that's the whole idea of competition is that
[53:20] um the more the competition
[53:26] the the better the value will get so it might not be something that a
[53:26] lot of people are going to get
[53:34] more than a token payment like you say in the near future but i'm in
[53:34] this for the long haul um and i think
[53:42] that there still is a very bright future where we might have a positive reinforcement
[53:42] cycle uh that's
[53:51] uh you know this this virtuous cycle has been something that we've seen in the
[53:51] past where uh the treasury
[53:58] gets the dash value the dash price goes up and that makes the the amount
[53:58] of purchasing power i'll say
[54:08] from the treasury increase and then more people can uh submit proposals that increases our
[54:08] budget now in
[54:16] the past we've we've done what i would consider somewhat foolish things with that with
[54:16] that funding
[54:22] you know but um yeah i think the the easier we can make it to
[54:22] get more people competing for that fund
[54:32] for those funds the better so that's my long rambly way of saying uh if
[54:32] not now then potentially in the
[54:40] future we'll have more funds to work with and regardless people should uh feel like
[54:40] they should
[54:46] they can propose uh they can make proposals um yeah
[54:55] um yeah anything any other final thoughts before we before we close out
[55:02] aj i don't know my wheels are turning on how how how could i make
[55:02] some proposals that would would both
[55:09] be easy win be easy wins all the way around but also be enough that
[55:09] it realistically you know as an
[55:19] american living in a tech city where prices are high and you know this we
[55:19] both have our our monthly payment
[55:26] to live in a house is exorbitant um you know like how do we i
[55:26] don't know i don't know that that's something
[55:35] i'm i'm i'm interested in because i like i even have a little bit of
[55:35] hesitancy i don't i kind of like i'm
[55:45] i'm hesitant to submit a proposal because i don't i don't know if the you
[55:45] know the price that i need
[55:50] would fill it but also i am a little conscientious of i don't want to
[55:50] be
[55:56] i i don't want to be competing in a way i mean like there's good
[55:56] competition and there's bad competition
[56:04] i don't want someone else with good ideas to have to lose for me to
[56:04] win and i don't want to have to lose
[56:11] for them to win uh and i last time i looked at one of the
[56:11] snapshots i saw one of the i think it was one
[56:19] of shemnick's proposals it well maybe it maybe it won at the last minute or
[56:19] something but you know it
[56:26] was losing and i was thinking well he's been very well respected why is what
[56:26] i don't know there's two
[56:32] there's not enough money in the system right now it seems like it seems like
[56:32] that's a big barrier i don't
[56:36] know this is yeah this is a stream of consciousness as always it is a
[56:36] big topic it's one that i've
[56:43] raised in the past i don't like how the treasury system is a zero-sum game
[56:43] it's not something that
[56:49] i will bring up now because um first of all we're already out of time
[56:49] but also it is a controversial
[56:55] topic um so i don't think that there should be a um uh an arbitrary
[56:55] cap that's what i will i've said
[57:09] that in the past uh i will probably say it in the future but it's
[57:09] not the the fight that i want to
[57:14] fight right now but it is you're right that it does create a little bit
[57:14] of an adversarial um environment
[57:23] where people are competing in a non-cooperative way and it does have negative effects so
[57:23] we'll bring that
[57:34] up and we'll we'll talk about that i think another time but for now i'm
[57:34] happy that uh you've created this
[57:40] application uh i think the the fact that there's a library underneath it is is
[57:40] great so that other
[57:47] people can also experiment with creating different uh user experiences around it and um like
[57:47] i said
[57:54] the the proposal system is is dash's best feature in my opinion it's it's what
[57:54] will create a success for
[58:02] the project long term i believe as long as we get the right people creating
[58:02] value in this ecosystem so
[58:08] with that thank you guys one last thing one last thing one last quick one
[58:08] sentence okay so i promised
[58:15] that the dash coin stuff would be done it hasn't been done i didn't really
[58:15] give a specific i said as
[58:21] soon as the mnos vote for it it'll be done that was not true but
[58:21] that will be coming so just i have
[58:26] not forgotten on my commitment to that the money is still there for that i
[58:26] just hadn't taken it
[58:31] because i was working on some other stuff because i needed to shift focus and
[58:31] let that that money for
[58:36] that project or crew for that final month so that will be coming i just
[58:36] wanted to put that out there
[58:41] so that you know that the the dash the coin join dash join project is
[58:41] not dead it is not um it is not
[58:49] in an unsuccessful place i just had to focus on some other things because of
[58:49] the economic shift so that
[58:55] was all i'm not dead yet okay cool thanks thanks for joining in everybody and
[58:55] we'll uh leave a comment
[59:02] below if you have a comment um about that final theoretical or philosophical discussion as
[59:02] well
[59:08] and we'll see you next week bye