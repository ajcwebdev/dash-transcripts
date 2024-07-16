---
showLink: "https://www.youtube.com/watch?v=PPJU6LbM28I"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "Code Hangout: Next-Gen DASH Tools #11: DashKeys.js Details are the Devil..."
publishDate: "2023-02-03"
coverImage: "https://i.ytimg.com/vi/PPJU6LbM28I/maxresdefault.jpg"
---

## Episode Description

Cool Age 86 spends over 7 hours meticulously refactoring and finalizing a cryptocurrency developer tool called dash-keys, focusing on consistent naming and documentation.

## Episode Summary

In this marathon coding session lasting over 7 hours, Cool Age 86 works on finalizing dash-keys, a cryptocurrency developer tool. He meticulously refactors the codebase, focusing on consistent function naming, updating documentation, and ensuring proper typing. The process involves careful consideration of API design, thorough testing, and resolving various bugs. Throughout the stream, he discusses the challenges of creating developer-friendly tools for cryptocurrency, emphasizing the importance of clear documentation and intuitive design. The work is part of a larger effort to create a suite of vertically integrated tools for the Dash cryptocurrency ecosystem, aiming to make them accessible even to developers not deeply familiar with cryptocurrency concepts.

## Chapters

00:00 - Introduction and Initial Refactoring

Cool Age 86 introduces the dash-keys project and begins the refactoring process. He discusses the importance of consistent naming conventions across the cryptocurrency ecosystem and starts updating function names for clarity and consistency. The developer also begins updating the project's documentation, particularly the README file, to reflect these changes.

59:52 - API Design and Documentation Updates

This chapter focuses on the meticulous process of designing the API and updating the documentation. Cool Age 86 carefully considers how users will interact with the library and what information they'll need. He spends significant time updating usage examples, function descriptions, and parameter explanations in the README file.

2:12:31 - Debugging and Issue Resolution

In this lengthy segment, Cool Age 86 encounters and resolves various bugs in the codebase. He methodically goes through error messages, tracing them back to their source and implementing fixes. This process involves careful consideration of asynchronous functions, ensuring proper use of await keywords, and addressing issues with data types.

4:23:02 - Testing and Validation

This chapter covers the extensive testing phase of the project. Cool Age 86 creates and runs various tests to ensure the functionality of the library. He updates existing tests to match the refactored code and adds new tests where necessary. The developer also considers edge cases and potential misuse of the library, adding appropriate error handling and validation.

5:46:55 - Final Documentation and Publishing Preparation

In the final segment, Cool Age 86 focuses on finalizing the project's documentation and preparing for publication. He ensures all functions are properly documented, adds a comprehensive glossary to explain cryptocurrency concepts, and updates the package.json file. The developer also discusses the process of publishing the package and updating dependencies.

## Transcript

[00:00] you
[00:02] you
[00:04] you
[00:06] you
[00:08] you
[00:10] you
[00:12] you
[00:14] you
[00:16] you
[00:18] you
[00:20] you
[00:22] you
[00:24] you
[00:26] you
[00:28] you
[00:30] you
[00:32] you
[00:35] you
[00:37] you
[00:39] you
[00:41] you
[00:43] you
[00:45] you
[00:47] you
[00:49] you
[00:51] you
[00:53] you
[00:55] you
[00:57] you
[01:00] you
[01:02] you
[01:04] you
[01:07] you
[01:09] you
[01:19] you
[01:31] you
[01:34] you
[01:44] you
[01:55] you
[01:57] you
[02:07] you
[02:17] you
[02:19] you
[02:29] you
[02:39] you
[02:41] you
[02:51] you
[03:02] you
[03:04] you
[03:17] you
[03:29] you
[03:31] you
[03:40] you
[03:47] you
[03:49] you
[03:59] you
[04:10] you
[04:12] you
[04:22] you
[04:35] you
[04:37] you
[04:47] you
[04:55] you
[04:57] you
[05:07] you
[05:17] you
[05:19] you
[05:30] you
[05:42] you
[05:44] you
[05:55] you
[05:57] you
[06:15] you
[06:17] you
[06:42] you
[06:44] you
[06:49] you
[06:59] you
[07:01] you
[07:19] you
[07:22] you
[07:38] you
[07:40] you
[07:46] you
[07:58] you
[08:00] you
[08:06] hey yo anybody tuning in yet let me check the chat here hey chat is live great i'll be live soon
[08:20] all right got that open
[08:26] move this over to where it ought be
[08:29] keep my eye on that
[08:34] so
[08:36] so
[08:38] so
[08:48] so
[08:50] so
[08:52] so
[08:54] so
[08:56] so
[09:02] so
[09:12] so
[09:29] so
[09:47] it's good
[09:49] so
[09:51] so
[10:01] so
[10:03] so
[10:19] so
[10:21] so
[10:23] so
[10:26] so
[10:33] so
[10:41] so
[10:43] so
[10:53] so
[11:08] so
[11:10] so
[11:20] so
[11:30] so
[11:34] so
[11:36] so
[11:50] so
[12:00] so
[12:02] so
[12:12] well hello hello and welcome back look the camera's working today
[12:31] so i rebooted my computer but now it works so there's that right and what else is going on
[12:38] okay so the details are the devil
[12:43] yeah last night i just
[12:46] i got i got into some things i just didn't have the brain power for i you know just certain things
[12:56] it was really the naming of things so i'm thinking that so for example look at this we've got with to adder but private key to with
[13:08] and
[13:12] generate so i'm mixing short and long and i think that for function names i want to just go short because the return values and the json values are going to be long
[13:25] and i think that that is good enough if something's going across the wire it should be long if something is part of a
[13:31] function definition so pubkey hash i could just use pkh that's okay because the in the description of what it does i can say pubkey hash right
[13:43] and then in
[13:45] in the
[13:49] how it comes out across the wire it can be pubkey hash and i am also forgive me i'm rethinking some of the stylization
[14:03] again this is something that i just i just want to have a chat with another developer about another clean code architecture oriented developer perhaps jojo bite perhaps somebody else
[14:12] but i just want to have a couple of conversations you know let's peg all these things to 0.9 and then and then make make the final decisions but i am going to the one thing i need to do here for sure
[14:26] regardless of whatever things are named is i need to move all of these utility functions that were utility functions all of them need to make it into the the base
[14:38] api because the reason that the base api was so small was for reasons that don't matter anymore because now we have the we're not we're not using separate dependencies for base 58 check and
[14:55] ripe md so now
[14:56] because i i tend to optimize around what's going to create the fewest dependencies so i can create i can give you some utility functions but if you're going to have a choice of i want to use this implementation or that implementation
[15:07] and we don't want to bloat with seven different implementations of ripe md you know so if we can just provide this and it's
[15:17] what it needs to be
[15:23] that's good you know if we can just provide one thing that has the tools that are needed for the ecosystem and i and i do think that this is the right separation like i said before because
[15:33] if you need base 58 check you're almost certainly going to be dealing with addresses there are very few use cases where you're not going to be dealing with addresses if you're going to be dealing with extended
[15:46] keys there are very few use cases where you're not going to be using addresses if you're using addresses you have to use ripe md
[15:52] there are very few use cases where you'd use base 58 without base 58 check in fact i know of none i cannot think of one
[16:00] use case for base x which is base 62 outside of base 60 or outside of base 58 but base 62 and base 58 have nothing to do with each other they're not in the same space as cryptocurrency yada yada so i don't see any reason
[16:16] to separate that dependency out it'd be better to duplicate the code if somebody needs a basic base 62 implementation so i think the dependencies are right i think that the way that this is going to be used
[16:28] it follows the solid principles and clean architecture guidelines so let's finish it up i don't want this thing i i didn't want this thing to spin out quite so long but i if we're going to do these new sets of tools the problem with the existing tools aside from being bloated is that the documentation absolutely sucks you have to know everything in order to know what to do
[16:55] so with this we do have an opportunity to you know like i've added the glossary here there's actually a couple of notes i took last night let me find my phone here i put it up in case i had to use it as the camera again let me grab that thing now okay so no disconnect we don't want continuity camera right now
[17:16] um let's see where are the notes notes we're in the notes app but i made some notes for myself as uh while i was while i was falling asleep what are the things that i forgot to do in the glossary and i have just a few items that i think are worth doing so i'm i'm going to start off with those and then we're going to go move things into the utilities so give me just a second to pull up
[17:43] this one is dash keys i want to just move this directory too while i'm at it dash keys.js maybe or i don't know how i want to do that never mind okay we're going to go into dash keys
[17:57] and i may actually want to add the cli um oh whoops hold on better snap tool where are you get out here better snap
[18:13] yeah that's what i want to see boom
[18:15] all right so back into the readme back into the glossary there was a few things that i thought about last night as i was laying in bed one we're just going to call this check not checksum and the reason for that is checksum is a more
[18:39] um
[18:42] generic term so if we just call it check then we'll be good
[18:49] so let's go ahead and just move this around also
[18:57] so
[19:08] all right so that was that was check also i realized that i probably ought to add base x
[19:22] i want that to be separated like this so that we get the hyphen in there um base 58
[19:30] base 58 check
[19:35] okay and how's it going everybody good morning welcome
[19:48] um also one other quick thing here i uh did not post in the dash discord because
[19:57] i've been posting in there quite a bit but i'm going to go ahead and post in there again
[20:01] because i do want feedback on this feedback wanted on naming things
[20:14] naming things so hard
[20:26] no stop stop reconnecting continuity camera i'm gonna have to disable that thing okay is that
[20:43] all the sound still working okay good we didn't mess up and didn't mess that up good
[20:49] okay so what's it gonna do oh yeah so i'm gonna add
[21:01] a base x and these are gonna be super short i'm not gonna go into detail on these
[21:09] um base 58 check a bespoke
[21:16] uh encoding similar to base 64 similar to but not compatible
[21:34] not not at all compatible um
[21:43] compatible with base 64
[22:00] we're encoding bytes with arbitrary um
[22:06] a bespoke
[22:10] algorithm for i'll go rhythm
[22:18] algorithm algorithm why why am i blanking on how to spell algorithm can somebody can somebody
[22:30] uh algorithm no not rhythm like music
[22:36] come on why am i what what is wrong wrong with my brain
[22:45] is it really spelled that way has it always been spelled that way
[22:55] seriously why oh man you know i mean every i think i assume everybody has these where there's
[23:01] something that for some reason for a moment just is really odd so a couple days ago i was looking
[23:08] at the word for f-o-r f-o-r as in for good or for evil and i just it just seemed odd to me for some
[23:17] reason just my brain lapsed and i looked at the word and i thought i know that's right why does
[23:22] it look wrong you know okay a bespoke algorithm for encoding bytes um for arbitrary
[23:34] arbitrary
[23:39] um arbitrary width bit encoding
[23:50] similar to but not at all compatible with
[23:58] base 64
[24:03] um bit width is based on
[24:14] provided on the size of the provided alphabet
[24:21] um and then i do want to actually grab out the specific alphabet
[24:34] so
[24:40] a specific base base x
[24:55] alphabet
[25:01] uh
[25:06] all right
[25:20] number of characters in the given alphabet
[25:26] number of characters there we go let's uh spell things correctly by the way if you are watching
[25:41] and you're interested in helping with the naming things just let me know because i'll talk about
[25:46] some of the things that i'm kind of uh feeling iffy about okay so base base 58 a specific
[25:55] 58 character base x alphabet
[25:57] the same is used for dash as most cryptocurrencies
[26:05] this was chosen to eliminate confusion between zero and and zero let's see
[26:24] so
[26:26] this character set was chosen to eliminate confusion between similar characters
[26:40] so
[26:43] so
[27:10] wait is that one nope oh look i'm already confused
[27:16] what no
[27:23] okay
[27:30] all right that's what we're doing and then base 58 check
[27:40] um
[27:40] so this is just going to be text this we can make a javascript and it's going to be
[27:50] version bytes
[27:52] check bytes
[27:57] data bytes
[28:04] comp flag
[28:09] okay
[28:13] then
[28:15] c also
[28:22] address with and check
[28:28] check
[28:28] go
[28:38] i'm just going to put these in here
[28:41] now notice i have been converted away from the oxford comma i know that this will displease
[28:52] many people i have my reasons we can talk about it later if you'd like
[28:56] but essentially it's because i often use lists of things and the last and doesn't have the comma
[29:03] which means that the next comma is the new group now if we want to go back to using semicolons
[29:08] we can discuss that too i'm happy to go back to using semicolons
[29:12] but you know it's a rough life
[29:24] a base 58
[29:26] um encoding schema that requiring
[29:35] um that requires headers and footers
[29:51] um prefixes and suffixes
[29:56] version is added as a prefix before encoding
[30:15] uh
[30:17] check bytes
[30:26] are added as a suffix before encoding wait is it before encoding or after encoding it is before
[30:41] encoding there we go
[30:50] some metadata
[31:09] may come before the data
[31:14] there we go that's it that's base 58 check okay
[31:22] so those were some things i thought yeah i had to put these in here um and then
[31:34] and then hdkey was something that is obviously uh well it's not it's not something that's used
[31:39] here but it's something that needs to be addressed here so let's see hdkey will go right here whoops
[31:47] it's important to reference hdkey
[31:53] compressed byte
[32:06] okay let's see so this is also an hd wallet with
[32:20] an hd wallet private key
[32:26] okay
[32:42] an hd key is a private key or with generated from an hd wallet
[32:52] c whoops i don't know why this does this there's some sort of plug-in that gets
[32:59] gets its knickers in a knot with how the um in certain situations it it is no longer able to
[33:08] parse an opening bracket i don't know i should read the error message and see what it's talking
[33:13] about but i don't know what plug-in it is so c dash hd
[33:26] ah
[33:35] i'm gonna have dash wallet
[33:51] so
[34:00] oh one of the things that have the cli's
[34:15] hmm
[34:25] what the letter l all right let me uh check in the cli here
[34:35] did i put did i is this where i i have these things
[34:44] okay here we go this is where i define those
[34:55] let's uh table of contents is a good section to put the links isn't it
[35:00] dash wallet cli dash hdcli github.com dash hive let's see what else we got here read me at
[35:13] my favorite language development is definitely go i would like to explore
[35:26] zygmore but i definitely i love go it's just javascript has become so universal
[35:34] uh it's whatever you write you have to write it in javascript if you want
[35:40] some level of portability and adoption hijk okay does anybody know intuitively
[35:50] which letters the alphabet come before another is that a skill that anybody on the planet has
[35:57] i've wondered this i'm assuming that everybody does what i do you have basically the groupings
[36:02] of the song that you learned and you just you go with those those groupings you you pick you pick
[36:16] from some starting point you know you can pick hijk lmnop qrs you know there's there's some
[36:26] there's some grouping to the twinkle twinkle little star song that you learned for the alphabet song
[36:32] twinkle twinkle little star a b c d e f g a lot of people didn't know that
[36:38] but you're old enough to know
[36:43] let's see
[36:47] let's uh take this back up here
[37:02] dang it see that look at my cursor wants to go back for some reason
[37:08] i don't think i'm gonna have that much longer
[37:26] okay and we're back dash keys
[37:32] oh there we go
[37:47] so
[38:09] okay there now all of the links are linkied
[38:16] actually i wouldn't mind just
[38:31] dash keys cli
[38:38] okay anyway i was getting a little off track there okay so what what did we have left here
[38:51] disconnect stop stop tag on phone keeps on going into continuity mode how do i tell it don't go
[38:58] into continuity mode i don't want you in continuity mode i don't want you i don't want you how do i
[39:05] tell it that all right so hd key checks um oh and then uh versions i'm just going to add x pub diversions
[39:15] and then just a link to c dash hd
[39:22] so
[39:24] all right
[39:47] okay c also address check and whiff c also address and whiff c also public key c also
[39:54] so this is where we're going to have glossary stuff is going to be in these
[39:59] so dash wallet js is kind of what i probably want
[40:02] dash wallet js and then we'll just get rid of cli and that'll be good enough
[40:16] okay and then the versions x pub and that was
[40:18] okay c c c c c i'll leave that one there for now c i'll just go ahead and change it
[40:33] all right references the cli and then the cli should reference the api let me go ahead and
[40:43] make sure that i got that
[40:49] install usage convert verify inspect
[41:02] generate okay api c
[41:11] dash keys js
[41:17] i should just go up in uh in the toc section
[41:25] api
[41:39] okay dash
[41:40] keys.js dash keys js
[41:46] all right cool that's good
[41:52] there we go and version okay cool
[42:04] um
[42:13] dash hd
[42:28] so
[42:37] for more info about extended private keys and oops extended public keys
[42:53] x pub
[42:56] x perv x priv
[43:05] cool and then i do want to
[43:14] um for the sake of use with um hd tools this base 58 check uh this
[43:27] uh this encoder
[43:31] base 58 check encoder codec
[43:43] includes
[43:52] also supports
[44:06] and then let me just go grab that real quick
[44:11] oops
[44:35] t pub no t t pub d priv
[44:43] all right i think i could have sworn 0 4 8 8 this was somewhere else in here but i guess it's not
[45:00] 0x blah blah
[45:02] base 58 encodes to x priv
[45:14] prefix
[45:30] base 58 encodes to the x pub prefix
[45:34] and
[45:38] and then
[45:51] these two ditties
[45:57] which encode to t priv and t pub
[46:03] okay question was how was the take-home assignment received or can i not ask about that here uh you
[46:13] can ask about that here so unfortunately i don't think they looked at it i could be wrong but the
[46:22] process was very mechanical and sterile the whole way through uh there was very it was very template
[46:28] response um which i i thought in some ways i think is good right i mean if you're them you need to
[46:35] filter through a lot of candidates and there's a statistical principle that basically you don't
[46:42] want to get the best you want to get good enough because if you try to get the best you'll wait
[46:45] too much time and so if you've gone through if you if you received a hundred candidates and you
[46:52] basically assume that they're in fairly random order if you go through the first one-third of
[46:58] those candidates i think it's one-third it might be 50 but and and it's also it adjusts based on
[47:04] market demands and stuff there's a formula you can actually use to calculate this it works for
[47:08] houses works for dating works for employment works for all sorts of things it's one of those
[47:12] natural laws like pi or e or whatever but essentially uh you will be most likely happiest
[47:20] and and feel the best if you go through it's either one-third or one-half i don't remember
[47:27] of of the possible options and then pick the next option that is adequate so and this works for
[47:37] adequate so and and this works for dating okay this is this is this is just it it's a statistical
[47:44] law of the universe um that on on the whole you are going to get better results if you have a
[47:53] particular goal of of achieving something just just get through one-third or one-half and then
[47:58] the next thing that's as good as what was in the top tier of that top of of the previous third or
[48:06] half the very next thing you encounter a person you encounter just take them on the spot that's
[48:11] that has all the right qualifications so there is there is an efficiency to being mechanical and
[48:19] methodical about this so they basically just took the stuff as far as i can tell they took the stuff
[48:25] put it through an automated test and didn't look at it so all of that work that i did to make sure
[48:30] that that so for me i was thinking okay i'm going to shine here because this is an area where i can
[48:35] shine i can show that i document things that i go through the little details that i understand
[48:42] how to use the apis etc etc right so from my perspective i thought i did a really good job
[48:48] and um but i don't i don't think that they looked at that so i did get to the next stage of the
[48:55] interview because i passed that but in the next stage of the interview i bombed for a very simple
[49:01] and clear reason which is that i don't actually program and go every day and so i had some
[49:06] hesitancies and some missteps um that were apparent and and i thought that the next step
[49:13] was going to be pair programming because that's what it said it said that there was going to be
[49:17] a pair programming interview it wasn't pair programming it was just solving um a problem
[49:25] that they picked that also it's not it's not really a common interview problem but it's uh
[49:34] they just picked a problem and then just said okay solve this and i started solving it the
[49:42] wrong way because i i misunderstood the context um and then i was kind of i was fumbling over
[49:52] which you know writing out the go because i'm not writing go every day right so if you were to look
[49:56] at that you would think okay this guy's obviously not a senior go engineer now if you'd actually
[50:03] looked at the code that i produce then i think you could see oh okay so this guy hasn't been
[50:10] writing go for the last year but he's obviously a very senior go developer i i just get the the
[50:18] sense that that didn't happen and the interview was very sterile and impersonal um not in a bad
[50:24] way it it wasn't it wasn't off-putting it was just so incredibly dry um it it i did not feel a sense
[50:39] of connection with the interviewer i mean oftentimes you don't you know you're not
[50:47] getting along with everybody but it just the process felt very sterile of okay do this okay
[50:54] do that okay do this all right wrapping up you know it was just
[51:00] i don't know and and so i understand if i were in their position and i was following
[51:08] a methodology like that i wouldn't have picked me either um but if and and they had so many
[51:16] applicants because that headline for the dollar amount was in the email subject they it drew so
[51:23] many applicants that i think it put them in a position of it probably was to their best advantage
[51:29] to take the approach that they took because they're going to get one of the best developers
[51:34] uh and you know i i honestly believe that i am one of the the best possible candidates
[51:44] for a go developer that you could ever pick because i subscribe to the philosophy i understand
[51:50] the the ethos i know the tooling and i think that more important than just
[51:56] the individual nitty-gritties of the language is the ecosystem as a whole the holistic approach
[52:02] to go programming um i think is really important and i don't and that i didn't feel that they were
[52:11] testing for at all i didn't feel at any point that that was really part of the evaluation of
[52:18] the criteria um so i i mean i did get nitpicked for using the wrong method for something to do
[52:27] with time there's there's basically a few different ways that you can do a timer in go and
[52:32] there's basically monotonic time wall clock time uh there's there's stuff that handles drift time
[52:40] and i i picked the wrong one for the situation and at that point when i picked the wrong one
[52:45] and he said well in go typically you would use x at that point i knew that i had basically failed
[52:52] and that was pretty early on because at that point he had asserted himself kind of in the
[53:00] role of the senior developer coaching me as as what i was expecting for the pair programming
[53:05] session was to be something where we approach a problem it i i was actually i was actually
[53:10] expecting it to be a pair programming style like i i actually thought that it was going to be okay
[53:15] we're going to spend an hour together pair programming we're going to be working on a
[53:19] problem um and that would have been great because then i could see the architecture and and and i
[53:26] could comment on that or they could ask what do you think about this and then i would have been
[53:30] able to demonstrate the holistic knowledge that i feel is you know where i where i shine
[53:37] especially because you know having not done it on the daily for a year you just you you can't
[53:45] remember all of those things like i said before you learn a second language and you forget how
[53:50] to say fork but spend a week in that language again and you'll remember how to say fork and
[53:55] knife and spoon and you know that so there's the things that and and this has actually been
[54:01] my experience it seems the bigger the company which this company wasn't big is the weird thing
[54:07] but it seems the bigger the company the more sterile the process is the more it's just
[54:12] kind of a a pass fail uh microscopic view of specific details which you could claim oh well
[54:22] this is a good litmus test and i don't know i i don't i want to hire people that have more of a
[54:28] holistic view personally i want it just me seeing the readme that that's the thing that would get me
[54:35] right if i saw somebody that had a readme and they had documentation boom i want them i don't care
[54:42] if they're not the smartest person in the room i don't care if they can develop an algorithm
[54:47] particularly quickly they can communicate what they know which is more than almost anyone can do
[54:52] so for me that is the most important thing is does this does this person do they have the ability to
[55:00] communicate and leave code that lasts so and i'm a little bit on the extreme of that as we've seen
[55:06] with this exercise but i think that the knowledge transfer is more important than the code so the
[55:16] dumber code you can write the better and if you have to highly optimize code then you need
[55:21] highly optimized comments yeah the bigger the company the more they automate it
[55:25] well thanks for thanks for the vote of confidence i thought you did a really good job as well thanks
[55:35] yeah so anyway i i'm not i enjoyed doing the assignment one of the rules of life
[55:42] is don't risk more than you're willing to lose don't put in more than than you're willing to
[55:49] let go completely unappreciated and in this case i was bummed i was bummed for the rest of the day
[55:56] it just it kind of put a damper on my spirits when i got that rejection letter
[56:00] i put a damper on my spends after the interview but i thought okay well maybe he'll take a look
[56:04] but when he told me that he was going through 50 candidates i thought he's probably not going to
[56:12] take a look at my work you know i sent him a sample a couple sample projects that were included
[56:18] in my resume he's probably not going to take a look at my work he's probably just going to find
[56:24] the person that he feels the best about out of doing the second or third day of
[56:32] straight interviews one after the other pick whoever he feels best about and move on with
[56:38] his life and that's not at all wrong uh you they will make progress that way
[56:46] and i think that they did want somebody that's a little bit quicker on their feet
[56:52] from the algorithmic perspective and the question that they gave in the interview
[56:56] i actually had a i i didn't well first of all i completely misunderstood it i
[57:02] i understood it the opposite way they wanted something that on a given time would give a
[57:08] selection and i was building something that from a set of selections would generate specific times
[57:14] so i know that's kind of it basically was like cron but but it was it was much more literally
[57:20] like cron i was thinking of it in terms of when people say it's like cron i often think they just
[57:25] mean it's on a timer but not that the selection process is literally behaving like cron and so
[57:34] if i'd under if i took it more at face value when he said that the task was like like writing a
[57:41] cron job utility i would have started off better because i'm i misunderstood i knew what i know
[57:48] what cron is um and then there was there was something that i've never actually done before
[57:53] which i had to stop and think about and in the pressure of the moment because i don't do really
[57:57] well in live situations especially when there's a timer i think i kept my cool pretty good but i i
[58:03] shortchanged my decision process when i'm in that situation and there was some questions about
[58:10] intervals uh and offsets and i just kind of had a brain fart and because i'm expected to you know
[58:19] produce the answer i i just didn't know i just didn't know and so so uh when when i was trying
[58:28] to redo it the right way i set up a an object that would contain the information and i was
[58:34] thinking okay first we can just batch we could match against the time anyway it's just i i just
[58:42] i just had the wrong approach to it so i don't regret the experience i was glad to take some
[58:47] time to program and go i found that to be enjoyable i'm sad that i was so quickly rejected
[58:54] i'm a little bit frustrated that that they said it was going to be a pair programming session
[59:01] and then it wasn't um because my expectations were just off i was really excited about the
[59:09] prospect of doing a pair programming session because that's something that very very few
[59:14] interview processes do and it's really enjoyable to do
[59:17] well this wasn't super heavy on the algorithms uh and you know most of the work that you need done
[59:26] it's not the algorithm work the algorithms are a very very small portion you know so if you're
[59:33] if you're three times slower at figuring out an algorithm first of all that's still pretty good
[59:39] and because the alternative is you don't figure it out you just write a bad solution period
[59:45] and the other the other thing is the most of your time is spent in business logic and trade-offs and
[59:55] decision making it's not spent and and you know documentation there's a lot of stuff that your
[60:02] time goes into and the the the algorithmic portion is not really i just don't think that the abstract
[60:14] thinking part is is important as the practical thinking part but you know and anyway so now plot
[60:21] twist first of all actually josh will you uh clip this whole segment because i think that this is a
[60:29] good segment the the failed the interview retrospective we could call it and that's that
[60:39] okay but now the flip side the thing that i didn't say i didn't want the job i wanted the
[60:48] offer letter i wanted the the justification not the opportunity so i'm i'm also not upset
[61:00] from that perspective the thing the company does i have really no interest in i think that it's
[61:04] kind of scammy
[61:06] scammy is the wrong word it's not scammy but i don't know it seems a little
[61:16] meh it's not you know a little uh by the way forgot are you subscribed on
[61:22] this channel because this is the dash incubator channel and my other channel i am still going to
[61:30] be posting on but i'm just gonna have more varied content so likes of follow if you want to on this
[61:37] one oh and then let me let me catch what other comments uh algorithmic style interviews only
[61:44] care about the algorithm unfortunately um then you can and then if you can't explain the space
[61:50] time complexity in my experience oh yeah the order order in that kind of thing yeah
[62:01] yeah i can i can often explain that pretty well i think that i've got
[62:13] i've got that figured out anyway
[62:16] josh that might be a good ending to that little clip
[62:26] with the just the might be a good outro
[62:33] okay now let's get pumped
[62:40] all right uh
[62:43] okay well um so let's see what was i finishing off here i was putting this in there that was
[62:51] the last thing i had in my notes for stuff that i think should be in here that i hadn't put in here
[62:56] yet yep okay great and so now let's go ahead finish that off so the readme is basically done
[63:04] [Music]
[63:11] now we need to go into this implement and implementation details portion and we need
[63:16] to pull this back up to the api so we're moving we're moving everything into the
[63:22] api that we can it looks like i might have already done this did we do this
[63:30] okay great
[63:40] hmm and i'm not quite sure what methodology i should use for
[63:51] documenting this because i feel like maybe this is the right way
[63:56] [Music]
[64:01] all right
[64:02] so this goes with this goes public key to pubkey hash pkh
[64:20] [Music]
[64:30] let's see
[64:31] so adder to pubkey hash this is
[64:44] pkh buff with stir
[64:48] well with is always a string so it's just the stuff that's hex we need to know whether it's
[64:54] a hex or a buffer pubkey hash to adder uh buff to
[65:13] hmm
[65:15] with to private key
[65:19] encode decode and we should have a verify true
[65:42] and i think this is basically right i just need to pull it in so i'm going to go
[65:45] down to that implementation details bit let's go ahead and snag this well
[65:52] all right given the existing libraries
[66:00] [Music]
[66:08] rather than
[66:14] uh let's see
[66:26] unique um
[66:29] doesn't do anything that other base 58 check libraries
[66:39] oh and i probably need
[66:49] [Music]
[66:55] okay here we go
[67:11] [Music]
[67:21] don't do it is however rewritten in modern javascript
[67:36] in class-free in modern class-free javascript that uses native apis
[67:45] using cross-platform
[67:58] js native apis for cryptography and such there we go
[68:07] its purpose is simply to fill the void for
[68:28] is simply to provide
[68:32] it's simply a rewrite the purpose of which is simply to provide a simple class-free
[68:52] javascript implementation that a
[68:58] simple lightweight
[69:03] class-free javascript implementation that takes advantage of modern cross-platform js native apis
[69:20] for cryptography and such such as web crypto
[69:26] really it's just a layer over a lot of tedium
[69:42] beyond that it does nothing more than provide convenience layers over a lot of technical
[70:03] tedium since it's valuable to understand that tedium here's a peek behind the curtain
[70:13] all right cool great excellent
[70:16] okay so i think
[70:28] [Music]
[70:40] as a reference implementation
[70:42] for porting to mobile
[70:51] it also serves as a reference implementation for porting to other platforms such as mobile and
[71:07] desktop there we go
[71:31] [Music]
[71:41] it does do a better job at exposing concrete
[71:58] exposing a convenience layer for the way that these libraries
[72:18] the way the base 58 check codec is used in practice rather than theoretically
[72:44] [Music]
[72:50] other libraries at present at least
[72:56] it also serves as a reference implementation for reporting to other languages
[73:03] as a reference it's valuable to understand the tedium here's a peek behind the curtain
[73:18] okay great so we're going to take this we're going to pull it in
[73:22] and then i think i'm going to leave it there as well
[73:31] [Music]
[73:34] okay uh let's see i'm getting back up on comments here
[73:37] i feel like i've asked this before but have you ever programmed in scala i think you have asked
[73:43] that before and i looked at some scala code once and it was confusing
[73:54] i don't like functional languages
[73:59] [Music]
[74:01] i like i like functional programming but not functional languages
[74:05] because the functional languages tend to they tend towards mathematical notation which i find to be
[74:14] um very confusing and and not clear because it's just a bunch of symbols and it's a lot of
[74:26] you're kind of expected to know all of the functional paradigms and then you can pattern
[74:32] match which is a big functional paradigm so it's kind of tautological or or recursive in that way
[74:40] the thinking process but you're you're pattern matching on these these notations and you're
[74:47] supposed to be able to intuit what the functional paradigms are from looking at the notation so if
[74:54] you see a bunch of symbols in a particular order then you know if you're highly highly intelligent
[75:00] you know if you are mensa or better then you're going to be able to just look at symbols and then
[75:07] understand what the pattern is because the symbols are opaque i mean it could be as much red squares
[75:12] and blue squares and green squares and whatever and you would understand because you could look
[75:18] at the pattern and you could say ah well out of the universe of these paradigms this paradigm has
[75:24] five pieces there are five pieces of syntax here so this this syntax must correspond to
[75:31] one of the paradigms that has five components or something that composes them to produce those
[75:38] components and and so then you can just kind of look at it and understand the paradigms and so
[75:43] people that walk around with that stuff in their head god bless them but it's not i don't find that
[75:50] enjoyable or desirable or or profitable because it's it's a very select few i would rather say
[75:57] have those patterns in your head and um
[76:07] oh hey what's up shimik how's it going um have those patterns in your head and express them
[76:16] clearly and i think that the way to do that is with macros and that's one of the things i'm
[76:20] considering with gpt script is that the language should include a set of macros that are the
[76:25] language but that are not the language that is saved to disk so the macros are something that
[76:31] you can have in your head but then when you type them they expand out to the actual code that could
[76:37] be read by someone else
[76:46] just one second
[76:54] i need to check two messages real quick
[77:06] oh okay give me just a second here uh something came up in production
[77:10] for someone i just need to basically uh this should be oh yeah it's just a one line change
[77:19] uh adding a return fixes a production bug approved so let me go ahead and boop boop eyes and check
[77:33] all right so that can now go through excellent okay so then we're going to go into dash keys
[77:41] here and down at the bottom this is where all the goodies are we do still have some typing to do here
[77:46] all right we're going to get rid of that
[77:52] okay adder to pub key hash and the other reason i want to shorten this is because if we do
[78:03] pkh instead of pubkey hash then i can say i can put hex on here i don't know if i really
[78:09] want to do that maybe i shouldn't maybe i should just say look you get the bites
[78:13] you want it to be hex call two hex on it fool
[78:17] i think that could make sense
[78:22] actually let me think about that let's go look at the usage here the usage
[78:26] let's do this let two hex equals dash keys dot utils dot bites two hex let
[78:41] two bytes equals dash keys dot utils hex two bytes i think that's fair i think that's very very fair
[78:55] borgod what do you think about this so this this is where i'm i'm kind of stuck right now is there's
[79:01] there's a lot of verbosity here and i don't want to provide there's a lot of verbosity
[79:07] there's a lot of verbosity here and i don't want to provide extra methods that could be
[79:13] explained in other ways i want to try to find the right the right abbreviations because some
[79:19] of the method names are for example public key to private key that's kind of long and i could
[79:25] do pub key to priv key but then we have this thing that's actually the canonical name is pubkey hash
[79:32] it's not public key hash as the canonical name it's pubkey hash as the canonical name but it's
[79:39] also referenced as pkh and so i don't want to have a pubkey and a pubkey hash because they look too
[79:44] similar and it doesn't communicate as well i think actually pkh communicates more because it is less
[79:52] descriptive in of itself because the pkh is not simply a hash of the public key as you might
[79:59] believe by the name as is quite common in cryptography there are words that are used like
[80:06] hash mod
[80:08] square root that they don't actually mean what we think they mean we think of a hash as you
[80:19] have a single hash probably a sha-256 we think of a mod as you literally just use the mod
[80:25] character between two numbers we think of a square root as you literally take the square root of one
[80:30] number but in cryptography these things are often shortened down to mod and what it means is
[80:37] fancy cryptographic algorithm complex multiple modulus but it's just called mod right and what
[80:48] will happen inside of that mod function is 10 different things multiplications divisions mod
[80:54] multiplication again against the prime curve and then you know division against the base number and
[80:59] then and that's the mod right and the public key hash is not that complex the public key hash is a
[81:05] double hash but its name is pubkey hash that is its name so pkh i think in some ways is more
[81:13] descriptive because if you don't know what pkh means you will look it up and if you look it up
[81:18] you will discover that it is not simply a hash of the public key but if you were to read pubkey hash
[81:23] that sounds dumb because why would you go from i mean this might clue you in too why would you
[81:29] go from public key to public key hash why wouldn't you just call a hash function on the public key
[81:35] and the reason is that the pubkey hash function is a specialized hash function
[81:41] so there's some of that that i'm i'm trying to figure out um
[81:48] how to how to deal with okay so if we do this at the top layer because i was thinking we just call
[82:00] it two hex two bytes but if we do this at the top layer then bytes to hex is perfectly clear
[82:06] there's no ambiguity hex to bytes is perfectly clear there's no ambiguity um i actually did
[82:13] have it hexed to un8array but i think hex to bytes is is good enough because javascript bytes
[82:20] are un8arrays that's what they are um and this term is not used anywhere else because buffer
[82:27] is often used to mean node buffer so that term is kind of already taken and u8 already means
[82:34] an int and then u8 array it just at that point why not just say uint8array because if you're
[82:40] going to say u8array and if you shorten it to u8arr then it just kind of none of it seems
[82:48] to strike the right balance but bytes seems to strike the right balance for me in terms of
[82:53] it is a un8array but it's not a node buffer and it is a sequence of bytes
[83:02] um because the alternative would be uint8array to hex and i'm trying to figure out what should
[83:10] the canonical name of this be should this be the canonical name that's what it was
[83:15] that seems like it's so many letters and words that it actually is hard to read because it's
[83:24] too descriptive and so if we do this and we say two hex and two bytes and those are the only two
[83:30] things now if we had two big ints which if you go deeper in the lower levels you actually do need
[83:36] a two big int as well but then two big ints the question becomes well how are you going to do
[83:46] that one and one could argue which i'm not entirely opposed to i'm i'm i'm very opposed
[83:51] to having separate types for return value i'm not super opposed to having separate types for input
[83:59] value saying that you can you can accept an enum you can you can receive either this or that but
[84:04] i'm extremely very strongly opposed to saying that you can return an enum that you could return this
[84:11] or that but two big ints it could be you know each of these actually could be that they this one
[84:18] accepts either a big int or bytes this one accepts either hex or a big int this one accepts either
[84:25] hex or bytes that's not a problem that we need to worry about right now but that is an ecosystem
[84:30] issue of there are three things that you that you need to transform between hex bytes and big int
[84:37] it's not particularly this library so yeah so i'm in between a lot of these right because
[84:45] if we shorten pkh if we shorten pubkey hash to pkh then we can shorten public key to pubkey
[84:54] and that shouldn't produce too much confusion because pkh becomes the canonical in the function
[85:01] name and pubkey hash becomes the canonical in the glossary and it's okay that because i i just don't
[85:08] want to function private key to pubkey hash that's just it's too it's so long that it becomes i think
[85:16] and i you know argue with me on this i'm i'm you know very open to try i want to figure this out
[85:22] i want to figure out what is the most ergonomic way to do this but um that's the part where i'm
[85:28] a bit confused is what is the best way and then same here we've got private key to whiff we could
[85:38] go priv key to whiff we've already got whiff to adder so if we don't go private key to whiff
[85:44] then we need to go whiff to address and so i'm thinking that we go private key to whiff whiff
[85:50] to adder so on and so forth and throughout the ecosystem adder is what we use in the function
[85:55] if the function does something with an address the function's name for the noun of that behavior is
[86:03] adder and then same thing a function and we could do we could even do say priv priv buff rather than
[86:12] priv key we could say priv buff and priv hex but i kind of like the idea of saying look everything's
[86:18] canonical form is un8 if you need to do something special mathematically then you use a to big int
[86:26] function on the un8 if you need to do something to transfer it across the wire to serialize it
[86:33] then you use to hex and from this perspective what would even be more clear is if we said
[86:42] to hex and from hex to big int from big int because the implicit is that the the canonical
[86:51] form is the un8 array and so if we're going we're going from un8 array to hex we're going from
[87:02] uint or we're going we're going from hex to un8 array we're going to big int from un8 array we're
[87:10] going from big int to un8 array so i think that this is actually the even more explicit form
[87:19] than to bytes but i think that to bytes that you know it's it's just it's it's it's hard it's hard
[87:27] to figure out what is the right way to name these things is one of the greatest problems of computer
[87:32] science you know anyway uh let me go ahead and get back out of it get back out of the readme and get
[87:38] back into here and see adder to pubkey hash do we already have this somewhere in here no we don't
[87:45] so we could have dash keys adder to pkh
[87:51] and that's what i'm that's what i'm thinking
[88:04] not base 58 check encoded
[88:08] let's see
[88:15] no version or check not b58c
[88:22] check not b58c
[88:32] hey what's up dubs good to see you
[88:51] okay
[88:51] i think naming something too long is better than not being able to understand what it is
[88:57] yes but the question is this
[89:02] that this is this is my argument against naming it too long one people don't like it you have to
[89:11] strike a balance because if you go too far with what people don't like they're not going to use
[89:15] your library they're going to have some sort of negative negativity towards it the second is it is
[89:22] clear what it is to the people who have used the tools to people that are part of the ecosystem
[89:29] they know what pkh means to people who are not part of the ecosystem it's unclear but that's why
[89:36] i've got this glossary so let me give you a link to the glossary here let me go ahead and um just
[89:43] push this up
[89:45] so whoops that's not what i wanted let's go back to v1 and beyond so
[89:59] where's my glossary section
[90:07] there we go so so take a look at this because i think this does the right thing
[90:14] wait why is this uh it's not showing the bits that i added what is going on here oh whoops hold on
[90:27] so
[90:29] okay so let me let me refresh this again take a look at that
[90:43] so if you were to search on this page pkh
[90:54] you see pubkey hash pkh right so i've tried to define everything such that where it's relevant
[91:01] you will
[91:04] come up against it so this is why i'm leaning towards it is because i'm putting comments in
[91:14] the code and stuff so that you will know that these are the what the canonical name is and so
[91:21] that's that's one of the reasons that i'm for it before i was against it but it's just
[91:26] address to public or address to pubkey hash it's just so daggone long
[91:34] and and when you start compounding these things because you need to compose them
[91:41] it's just it's it starts to become a little bit obnoxious
[91:46] so public key to pubkey hash
[91:54] adder pkh to adder with to priv key
[92:09] so
[92:18] so
[92:25] and then also the other thing that we can do is that in the return value we can give it the more
[92:48] expanded name so what you have to type is going to be shorter but what you will see in all of your
[92:55] tooling will be longer
[93:01] so
[93:10] i think i'm convincing myself more than i'm convincing you
[93:29] because i was on the other side of this where let's use the full name
[93:34] you know to be as clear as we can but it's just
[93:48] it's not it's not floating my boat
[93:54] so
[94:02] so
[94:11] so
[94:30] okay and some of these are actually
[94:39] now that i understand them that's not a valid prefix let's see so for example a wiff is always
[94:46] base 58 check encoded so that would just be wiff
[94:52] oh wait we could say maybe that's wiff info
[94:59] or wiff parts let's try that not with info but with parts
[95:18] so
[95:25] okay
[95:44] okay
[96:09] okay dash keys dot decode equals and this one's a little tricksy because this is really opaque
[96:20] and we need to have here ops so this needs to be
[96:27] decode ops and ops and we need to define decode ops so we're going to do the typing for all of
[96:38] these things yeah so what you type will be shorter what you see in your tooling is longer
[96:48] okay that's that's the specific thing you're commenting on
[96:51] so
[97:02] so
[97:11] just one second here
[97:27] so
[97:37] let's see
[97:52] so
[98:01] so
[98:11] okay sorry back over here so type def decode ops prop
[98:30] verify validate
[98:40] throw if
[98:54] check fails true by default
[99:00] all right this is call back decode and type decode
[99:23] dash 58
[99:24] oh okay
[99:27] if not valid
[99:33] um
[99:36] run through the same process again to throw the error
[99:47] okay
[99:54] well that's that's why we rubber duck you say i feel i feel like you figured out the answer to
[100:05.36] your own uh question that's that's why we rubber duck is because we have to explore things and we
[100:11.28] have to explore them with other people and we need pushback i need you to say no it should be longer
[100:16.96] that's my default position yeah it should be longer my default position is don't shave
[100:22.16] a few characters for readability in this particular case i have to argue the readability for
[100:27.68] whom the readability for the people who come across the library only ever once
[100:33.68] or the readability of the people that are coming into the ecosystem and the balance
[100:42.32] can be struck perhaps with providing some better documentation and tooling
[100:47.52] whoops
[101:12.00] whoops no this needs to be why do they even have these brackets at all
[101:16.16] okay dash keys dots encode equals
[101:33.04] wait you and ada ray i don't think so
[101:51.76] ah
[101:58.48] i see what's going on here
[102:02.80] hmm
[102:08.96] i actually don't like this implementation
[102:13.28] because
[102:19.68] it does not work for
[102:27.44] so we want to encode
[102:34.32] hmm i have to think about this
[102:41.84] we could break this into several pieces we could say because for decode you don't really i mean
[102:52.40] all the information is in the decode but for the encode you need extra information
[102:57.36] the decode it it knows ahead of time um what type is although
[103:02.56] hmm there this does kind of violate my rule that i mentioned earlier of multiple return types
[103:09.76] because these return types are actually really really similar but they are
[103:13.76] different so the return type here it could have
[103:22.40] a pubkey hash or a hmm there's a i have to think on this one for a little bit because the problem
[103:32.24] here is that there's actually four different types of keys two of them can be distinguished
[103:36.64] by their length but two of them cannot two of them are the same length and so when we encode
[103:43.76] originally my thought was ah it's enough to just say
[103:49.20] in code it because whatever this thing is we can tell by the length
[103:55.36] um i have to i have to think a little bit more on that
[104:00.72] to think a little bit more on it
[104:09.76] all right and we had this needs to come down
[104:14.16] also wondering
[104:22.24] it also raises the question should generate become
[104:38.56] new create or gin
[104:41.76] should it be generate with non-hd and the reason for this extra bits is because i actually don't
[104:59.20] want people to use this function and when they use this function i want them to know that
[105:08.32] it's but this is here's the thing though where this is my reason against create so let me tell
[105:14.40] you how i landed on generate create is usually when you're allocating memory for something that's new
[105:19.92] generating is typically for when there's a sequence of something so for example i generate a
[105:24.88] random number i don't create a random number generating a whiff kind of makes sense because
[105:30.72] you're just taking a series of bytes and then encoding them so you're generating a random number
[105:36.08] and then you're encoding it as base 58 you're not allocating new memory for a thing and that's where
[105:43.68] create a new i'm not as a fan of them and we could keep this long instead of gen whiff could be
[105:51.92] generate whiff and then because because i don't want people to use this anyway it's there for
[105:56.64] development purposes but you shouldn't use it you shouldn't use it in your code you should use it
[106:03.12] just for when you're it it's it's useful as a reference implementation but if you're going to
[106:08.48] be generating a whiff you should be generating a whiff that's an hd whiff so it's provided
[106:15.28] for convenience but don't use it it's kind of the thing so but feel free to sell me a little stronger
[106:30.24] on the idea you know i like the back and forth if after that you're thinking no no no no create
[106:36.72] mill it still makes sense because xyz by all means tell me the xyz i'm not trying to
[106:43.20] shut down the conversation that i'm asking for i'm just trying to find the right balance of
[106:51.04] of clarity and and whatnot
[107:04.48] all right and then where was this one at
[107:16.48] love so this is uint8 to hex
[107:39.92] so
[107:45.36] i think we can get rid of this little indian stuff
[108:06.16] okay i think i'm liking this more and more as i go the idea of shorter a little shorter with
[108:12.40] typing not not to excess not to be you know because we could just say oh it's to be it's to h
[108:20.56] that is excessively short can you explain what generate non with generate whiff non-hd is doing
[108:28.64] again yes so first it generates a random number so this random private key what that is is it
[108:39.12] it does two things it generates a random number that's a random byte sequence that's 32 bytes
[108:44.24] and beyond that it then verifies that that random number happens to be able to become a point
[108:56.64] on the sec p256 k1 curve so sex p sec p256 k1 is the name of a curve an elliptical curve
[109:10.56] and a mathematical function so there are different curves that follow basically the
[109:14.88] same mathematical principles but they have different parameters in terms of when they start
[109:20.80] and i don't really know much about it to say what it is but that's the first thing it does
[109:26.64] if a if a random sequence of 32 bytes can be placed on the curve and generate x and y coordinates
[109:35.76] then it is a private key that is the definition of a private key for sec p256 k1 it is a random
[109:44.80] sequence of bytes 32 bytes that can be used to generate public x and y coordinates so that is
[109:52.72] the private key part the next part is that it gets encoded as a whiff which means that we take
[110:02.80] a version magic byte which specifies that this this coin version is the dash private key coin
[110:11.20] version and then we take a checksum of oh and then there's also a compression flag which basically
[110:21.84] if you have an x coordinate on a curve unlike normal functions a normal function if you have
[110:27.04] one x value you get one y value but in an elliptic function if you have one x value you have
[110:34.56] potentially two different y values on either end of the curve and so there is a byte that is either
[110:43.68] o2 for even or o3 for odd which tells you which of the two points should be used for the y value
[110:56.00] so that is considered the compression byte or the compression flag this is in the glossary
[111:01.68] if you take a look at the glossary here so let's go to glossary
[111:07.36] okay so that's the compression byte
[111:15.28] so let me actually go to whiff here
[111:20.32] so it is a coin version byte the compression byte then the private key then the checksum of these
[111:31.04] three things and then take all four of those things and base 58 encode them and that is a
[111:40.96] whiff so in simplest terms a whiff is an encoding of the private key that includes the coin network
[111:51.84] prefix and a checksum suffix
[111:54.96] so that's what that function is doing is it is generating that
[112:06.56] okay so let me continue on here
[112:10.48] got the encode we've got the decode we've got the two
[112:15.12] bytes let me make sure that this two bytes is again the same
[112:18.96] okay
[112:19.46] yep i like that one better because it is more explicit on two fronts actually
[112:30.56] yep that is the best version that i have is that one above i like to check them against
[112:38.96] each other in the comments because occasionally sometimes i have one that
[112:46.40] uh
[112:49.12] all right the you that turned out to be wrong
[112:55.68] that's not necessary because as far as i can tell no matter what cpu architecture it's on
[113:03.92] so
[113:05.84] all right good that's it so i've got that one
[113:30.08] uh okay and that's that's the whole thing so i have to think about this encode function
[113:38.56] i might want to have
[113:57.28] let's see version version is essentially the type flag
[114:06.00] but it's not quite as nice as i would like it to be
[114:20.00] let me go back to the readme here
[114:25.60] 0 4 8 8 0 4 8 8
[114:40.32] let me do this
[114:53.36] so this is dash
[115:11.12] pkh
[115:17.60] this is dash
[115:22.64] priv key
[115:23.44] this is
[115:29.04] dash
[115:32.16] this is going to be x pub
[115:36.40] x priv
[115:40.48] okay x pub
[115:49.92] okay x pub
[115:50.88] x priv
[115:54.64] all right and then this would be
[116:19.20] x pub and x priv
[116:25.20] and we could maybe even make these constants
[116:41.76] so
[116:48.48] and then we could use these here i like that
[117:10.56] we have to decide is it priv or is it priv key like this or like that
[117:22.16] that one i don't think it really matters that's just internal stuff
[117:25.68] x pub x prv
[117:34.08] and again
[117:41.60] this is perfect
[118:02.48] and this was i forget what it was but i'm going to go ahead and put it in there as soon as i find it
[118:13.52] 8c and why is that in that order there we go ef 4c becomes 8c
[118:41.92] ct priv
[118:43.20] t pub
[118:46.64] all right so you okay you think generate is better
[118:59.12] okay do we have anywhere else where 4c is used
[119:06.16] so
[119:35.28] all right consolidate that all together but the point the what i was trying to look for
[119:40.08] is if there was a good way to say that this is priv key pkh
[119:46.24] x priv x pub
[119:51.84] so i kind of want to pull this out and bring it up
[119:59.36] fine we'll do a const for the base 58 there we go so then when we do the decode here
[120:21.76] um
[120:26.88] oops
[120:48.32] t priv t pub
[120:52.16] so
[121:00.80] so
[121:03.68] all right let's
[121:26.24] get rid of that
[121:35.36] there we go
[121:39.36] so now what i'm going to do is down in my decode method
[121:48.56] here before i return i want to add a new property which is parts dot type
[121:56.72] and we're going to switch on parts dot version
[122:02.64] and we're going to go through each of the cases as defined here
[122:17.68] you tell me what you think about this one too
[122:19.28] so what i'm thinking is we do k case pkh
[122:26.72] falls through and we do test net the same so what i'm thinking is we don't distinguish between
[122:36.80] test net and main net in terms of the type we just say parts dot type equals and this would be pkh
[122:46.72] and then we do case
[122:49.84] priv key oops again falls through and then case for the test net it's going to be parts
[123:08.08] uh
[123:14.80] maybe i don't know whether the type should be private
[123:20.80] or what it should be
[123:24.32] and then we say case
[123:29.60] x priv
[123:36.96] and case t priv
[123:38.72] part equals x priv
[123:45.28] and then the same thing here except pub pub and type is x pub
[123:59.68] so
[124:01.68] oops and then default is throw new error unknown version type
[124:16.24] type
[124:18.32] so
[124:47.44] so then this provides a little bit of convenience oh whoops
[124:50.56] did i not do this right
[124:56.48] what is it what is it griping about what is it griping about oh um semicolon rather than colon
[125:11.52] that makes sense i can i can respect an actual syntax error
[125:15.44] oh whoops uh const rather than case okay i get that
[125:25.12] oh oh right this isn't go
[125:38.56] there we go
[125:45.04] there we go
[125:59.04] oh thanks thanks for that hey what's up what's up fox tk
[126:06.96] uh let me see did i miss anything else uh okay line 10 43 thank you for catching that before i
[126:12.72] did that that since they will fell this issue yeah i was just excited i caught something yeah
[126:22.00] it's hard man it's all you know similar letters same colors yeah it does it well
[126:28.48] not just over time it all blends together it just it all blends together anyway
[126:32.16] it's too fast you see
[126:40.96] all right so this is good now this has one extra property that it didn't have before
[126:52.16] uh which i need to update the readme to show
[126:57.20] so well let's see uh
[127:05.52] let's see
[127:20.00] so
[127:26.00] the good news is we will reach the finish line we will not maybe we will
[127:49.04] okay what's the difference between these two nothing
[127:51.76] nothing is the difference between these two all right so this one gets gone
[127:57.20] all right and what's uh
[128:04.16] utils
[128:08.56] utils two bytes
[128:13.20] oh whoops
[128:20.80] there we go now that's right cool cool so now all of those are used as they should be
[128:32.80] so
[128:37.20] so
[128:46.16] so
[128:56.00] so
[129:05.84] so
[129:35.68] ah that feels good
[129:36.80] all right let's let's finish this
[129:45.28] i think the to public key is that a util i think it is i think we're gonna
[129:55.44] we're gonna move a couple things to utils here well no we're not gonna move a couple of things
[130:05.20] the things that are not specific at all to this process
[130:09.44] or that are really so that the two reasons things go in utils should be
[130:16.48] it's not highly specific to this process so for example two hex two bytes not highly specific at
[130:22.00] all and the other reason would be um dependent on a specific library
[130:32.32] so this one is also dependent on a specific library so this is going to move to utils
[130:44.64] oh and the other thing that i didn't mention about generate
[130:47.28] with non-hd the non-hd part of it so
[130:54.48] oops let's see i'm gonna i'm gonna go with we're gonna call it bytes to hex final answer
[131:05.36] because in the example we're going to show assigning it so this is final answer it's
[131:12.64] hex to bytes bytes to hex final answer um qrst
[131:18.64] what is this one generate generate coms abcde fgh
[131:28.24] all right and then bytes is going to move up here
[131:40.88] bytes moves to and bytes moves to the top spot taking taking first place and the bytes are wild
[131:46.08] okay so in the olden days which most of these libraries come from
[131:57.36] you know the 2000s or something they're ridiculously old
[132:01.68] in the olden days when the when bitcoin was first started the idea was that you were going to have
[132:10.64] an address and you were going to send money from that address and receive money to that address
[132:17.76] and that was not very private so the idea was well you're going to create many different addresses
[132:23.36] and you're just going to keep track of them you're going to have a database that keeps
[132:27.12] track of all your addresses that way they can be private well the problem with this is that
[132:33.60] if that database becomes corrupt which it did then people lose their their cryptocurrency
[132:40.80] and this is still a problem today where some version update or something can happen and if
[132:48.72] you're on the non-hd key system if something happens to that database of hundreds or thousands
[132:56.72] of keys it's not recoverable they are gonzo so then they came up with this idea of hierarchically
[133:05.68] deterministic keys which is basically where we're talking about the curve and the x and y values
[133:12.48] and the private key well there's a way that you can take a private key
[133:17.04] and use it to generate another private key in a deterministic way so you can you can create
[133:26.00] these private keys such that there's there's two algorithms one of which is easier to
[133:30.40] basically to share and the other one is easier to keep private so that there's no relationship
[133:40.00] between the private keys so basically if you were to take a hash of a private key if you take a
[133:47.04] private key and you hash it there's now no relationship between the private key that's
[133:53.68] the parent and the private key that's the child there's no mathematical way
[133:58.64] that you can reverse a hash that's known at present so
[134:04.08] the the hierarchy the the deterministic way of generating keys one of them is hashing but
[134:13.60] another one is basically doing some fancy elliptic curve multiplication which is not
[134:21.84] like normal multiplication an elliptic curve multiply is way more steps than
[134:28.64] basic arithmetic multiply but you do some fancy multiplication or some fancy addition i think
[134:35.68] it's actually the addition not the multiplication multiplication is for generating a public key the
[134:42.48] addition is for generating new private keys but you do some addition and through this it is possible
[134:51.44] that if you have enough of the child private keys leaked you're able to reverse it back to
[134:59.28] the parent private key so if you had thousands of your private keys leaked it's there each
[135:08.24] private key is going to have some relationship to the original parent and it's going to make it
[135:14.80] possible to reconstruct the parent private key so that is that's the difference between a hardened
[135:22.00] is a deterministic but unrelated and an and a non-hardened deterministic and related but shareable
[135:28.88] extended key system so with these you have the the the the the passphrase or as i term here
[135:40.88] there's the canonical zoomonic so you have 12 words and this is the this is one of the the test
[135:47.84] fixtures from the original standard zoo zoo zoo zoo zoo zoo zoo zoo zoo 11 zoos and then wrong
[135:54.72] the checksum word is wrong which is awesome for all sorts of reasons um at least three and so
[136:03.28] you can use that and then you give it a path and this basically tells it the the apostrophe tells
[136:08.64] it whether it's hardened or not so if it's hardened it's using the way that creates a wallet
[136:15.20] that is unrelated but then you can't use it to create an extended public key essentially
[136:20.64] and then down at the bottom these are unhardened which means that i can take this hardened wallet
[136:28.80] and i can use it to generate a system of public keys from this one so i can generate any public
[136:36.00] key that is lower than this and i can share that that extended public key and anybody can
[136:43.20] can send me money on that public key and there's an infinite number of
[136:49.84] keys that it can be just by incrementing this so that's essentially how it works
[136:53.68] and so the hierarchical key is with this system so all you need to know if you just write you know
[137:04.72] if you just write this down print it off in a safe your passphrase the the the mnemonic which
[137:11.36] here we have the canonical zoomonic the the the test fixture passphrase and then the secret or the
[137:17.44] the the salt password which the the test fixture one is trezor because trezor was one of the
[137:23.04] companies that i think helped in defining the standard or at least creating the test fixture
[137:27.84] for the standard so with that if you you know print this out put it in a safe and then take
[137:35.36] this and just memorize it and don't share it then you can recover hundreds of thousands of keys that
[137:44.08] way so you can create any number of keys so that's the difference between the two systems and that's
[137:48.08] why i'm saying that nobody should be using generate with non-hd except for the purposes
[137:54.88] of development debugging okay and i think i'm going to do something else kind of interesting here
[138:06.80] i think i'm going to define some types no i'm not going to do this right now well maybe i am
[138:17.52] so i'm going to define a type which is uh 4c it's the string 4c and this type
[138:27.52] is going to be called dash pkh
[138:31.60] and then i can type this
[138:36.48] i'm not i'm not going to go through the trouble of typing that but i want this to show up in
[138:43.44] the documentation and wherever possible very clearly
[138:47.84] so this is a this is a type for documentation only
[139:05.28] so cc and ef as i recall
[139:07.68] and then xpriv
[139:16.40] xpub tpriv tpub
[139:30.16] and we're gonna go grab those and bring them up
[139:37.20] xpriv
[139:42.96] xpub
[139:46.08] tpriv
[139:50.88] tpub
[139:59.20] here we go
[139:59.76] all right so now my decode's working better i feel i feel better about that
[140:10.80] and we're gonna have replace any two hex with
[140:17.12] bytes to hex we're going back to that
[140:27.20] and then we're going to replace any space
[140:30.64] bytes to hex with utils dot bytes to hex but this is not universal we're not going to do it there
[140:41.12] but we're going to do it here
[140:41.92] and then same thing with two bytes it's going to be hex two bytes
[140:53.28] not there oh wait yes we did want it there
[140:57.36] and then any space hex to bytes will become utils dot whoops utils dot hex to bytes
[141:12.56] not there but there and there
[141:17.60] and there
[141:23.60] and actually no we're not going to do that one at all
[141:38.24] so
[142:06.48] all right
[142:06.96] so we're just going to add the types to this uh i've got the naming figured out we're going to
[142:14.56] change the naming so this is going to be pubkey to pkh final answer for better for worse
[142:23.76] so
[142:29.76] okay and then this one is going to get what so you got hex to bytes bytes to hex
[142:46.88] so
[142:52.40] i don't think i want to call that type get public key
[142:56.40] i'll call that type to public key
[143:06.96] so
[143:14.24] all right then prop
[143:31.76] generate with
[143:39.12] well that takes no options you went eight array to hex
[143:52.40] yeah i like this i like there's some incongruity here but i think that it's the right balance
[144:00.32] so
[144:05.60] the type information is more specific
[144:16.56] than the name of the function and i think that really does strike the right balance
[144:25.12] so
[144:27.12] all right so
[144:33.36] developer tool for generating non-hd
[144:43.36] non-recoverable
[144:49.76] so
[144:52.00] private key wiffs
[145:17.28] okay pop quiz
[145:18.32] is utils dot generate with non-hd is this a method or a function
[145:31.60] you're free to look at the code or the docs it has not changed
[145:38.72] the entire time since i very first put it in there the thing that it is has always been that thing
[145:45.68] so
[145:47.68] all right and this takes no params and returns a string
[146:05.12] i guess it should take params actually
[146:09.68] i think that this actually would be appropriate
[146:18.48] to say
[146:25.12] that
[146:29.04] it it takes a version
[146:35.84] so
[146:46.96] so
[146:55.44] so
[147:10.24] that's interesting oh so check this out we can do this we can do type
[147:24.32] so
[147:26.24] version private
[147:30.24] and we can say main net
[147:34.80] so here's a value enum for you test net
[147:40.24] so then down in our generate
[147:56.48] i don't know what ops this has priv key to
[148:03.28] with
[148:29.68] actually
[148:34.64] priv hex
[148:54.64] and then
[149:01.60] and then this is version private
[149:07.04] hey what's up jajalt how you doing
[149:12.08] welcome
[149:15.60] so
[149:22.56] so
[149:30.40] so
[149:36.48] okay switch version
[149:55.68] case
[150:00.24] dash
[150:03.36] priv key might change that to private
[150:17.20] so
[150:25.20] so
[150:33.76] okay so dash priv key
[150:52.56] so
[151:05.12] priv buff private key
[151:19.36] so
[151:23.68] there we go
[151:38.24] so
[151:42.24] so
[152:10.48] okay
[152:15.20] buff
[152:19.20] there we go
[152:22.32] all right
[152:38.64] the type here is generate with i'm gonna make sure that's right down at the bottom here
[152:44.40] okay callback is generate with
[152:47.60] and
[152:54.32] oh whoops uh so what we actually need here because that's wrong
[153:08.00] is we need to have a local type def generate with ops
[153:12.64] and then this can have at prop
[153:17.20] version private version and that's it that's all it has right now
[153:34.88] so
[153:44.80] all right so generate with ops ops
[154:01.12] so
[154:11.20] great all right this is just getting better and better
[154:21.04] everything is finally coalescing the end is nigh
[154:25.68] so
[154:27.60] ah whatever
[154:52.72] so bytes to hex are great generate with non-hd is great hex to bytes is wait
[154:58.00] you say bytes to hex hex to bytes twice bytes to hex hex to bytes got it okay all of these are
[155:04.64] perfect to public key question is is it to public key or is it to pubkey
[155:21.92] that is the question
[155:25.52] and i'm going to leave it as to public key because it's under this utils thing
[155:49.92] um i don't know part of me says it should just be to pubkey
[155:59.12] eh not i don't know why i don't know why but it actually doesn't sit right with me
[156:17.44] i'm gonna leave it for now hey i can change it if i absolutely need to
[156:20.96] okay so from the top oh wait nope we still gotta put this one at callback
[156:27.28] um why would this need a version ops ops why would this need ops in code we're not gonna
[156:42.16] swap between versions on a wiff so i'm gonna get rid of that option that doesn't seem right to me
[156:48.40] so this is going to be of type
[156:52.88] um wiff to address
[157:01.28] so
[157:05.60] okay w x y z
[157:22.72] so
[157:31.44] a wiff
[157:35.68] coded private key to a pubkey hash of the same coin type
[157:48.24] so
[157:57.76] all right
[158:12.00] so
[158:19.28] and then also i realized that the term payment address
[158:25.68] should be reserved for context so a pay adder or a change adder those are context sensitive
[158:33.28] so a pay adder or a change adder those are context sensitive
[158:38.48] so this takes that goes right in okay dash keys dot utils dash keys dot
[158:49.68] all right encode is going to go up of course
[158:53.68] i still have not a b c d e i still um have a problem here though this is still a to-do item
[159:05.44] because we still haven't solved the x priv uh xpub problem with this that it it needs some
[159:13.68] additional type information in order to know what type of key it is if i i'm gonna go take a look
[159:20.88] real quick inside of dash hd or hd key but i'm pretty sure if what i remember if i can remember
[159:30.40] last week at all that there is actually no there are no bytes that tell us whether something is
[159:38.16] x priv or xpub
[159:40.80] i am going i am going to break i'm going to break this api we are going to make that xprv
[159:51.04] and this is not going to be called to json
[159:57.44] uh we're just going to get rid of this entirely
[160:04.48] and we're just going to get rid of from json because that makes no sense
[160:18.48] those two are just going to go away
[160:25.36] is it 32-bit int hold on oh yes
[160:54.56] i'm just going to get rid of those because they're confusing
[160:58.48] so
[161:01.76] so
[161:31.12] yeah i'm going to take a look at this again but as far as i can recall
[161:34.08] and we got nothing here to tell us
[161:37.84] from the key itself because the key size is always the same
[161:46.40] key size is going to be 78 no matter what
[161:53.28] uh is there something in there that will tell us
[161:59.76] so there's the buffer xkeydv it's going to set the version
[162:07.84] parent fingerprint
[162:16.16] htq.parentfingerprint
[162:24.64] oh
[162:38.80] oh
[162:42.08] yeah they both serialize
[162:49.28] they take version information
[162:56.08] but it is none the wiser it's the same process between the two there's no conditional logic here
[163:03.84] so we have no way to tell if something is extended public or extended private other than
[163:11.04] the information that we we pass in so if we want to encode
[163:22.72] hmm
[163:32.16] so if the buff dot length is what was it 70 was it 78 was that right i think it's half that
[163:49.92] x key size
[163:55.36] okay
[164:09.92] so
[164:15.92] i'm gonna go with we're gonna have an ops.type on this
[164:24.96] and it's going to be required
[164:32.88] case so we're gonna actually going to uh switch on ops.type and if we have case
[164:42.00] xpub then
[164:50.80] let's see i guess it actually needs to be version
[164:56.56] so
[165:03.76] we're going to switch on version or say version equals xpub
[165:21.04] xpub
[165:26.32] xpub default is going to be throw new error
[165:35.28] um cannot determine from
[165:45.44] key determine extended
[165:51.60] extended keys x x keys x priv uh cannot determine extended key
[166:05.44] x key type from buffer length
[166:14.56] please supply
[166:17.92] uh version
[166:23.44] as
[166:37.44] whoops
[166:40.96] xpriv xpub x tpriv or tpub
[166:48.96] and that's how we do it ladies and gents
[166:59.84] so
[167:08.72] oh and of course we need the brakes so glad for the winter
[167:26.56] okay we're going to need to have ops
[167:28.80] and we will need to have oh whoops call back in code
[167:36.72] uh do we have a decode in here
[167:45.44] q r s t
[167:52.24] u n sha s t there we go to public key
[168:01.12] call back decode
[168:07.68] and decode ops in code
[168:16.08] so
[168:24.00] all right in code ops and we're gonna have a version
[168:40.96] version
[168:51.44] ah
[168:58.64] so
[169:08.48] so
[169:22.32] all right here we go
[169:29.28] so let's say
[169:37.04] so
[169:46.16] let me just grab this real quick
[170:00.16] so
[170:24.48] okay okay let's go i'm only saying let's go because other people say it i really
[170:38.56] don't know how it's used but this seems like the appropriate situation
[171:02.00] rather than having these strictly alphabetical i am actually going to move them
[171:06.80] to in testnet order
[171:22.56] i am invincible
[171:23.84] uh i need to re-watch golden eye i did finally watch it i played the game as a kid but i had
[171:33.92] not seen the movie until i think within the last five years or so i may have watched the movie and
[171:41.12] just completely forgotten about it but i re-watched the movie watched it or re-watched it whatever
[171:48.00] i think i watched it for the first time because when i was a kid i was probably
[171:53.12] not i was not exposed to james bond until my stepdad my father
[172:03.20] but at least he exposed me to uh star wars like a good father should but he didn't james bond me
[172:16.00] my stepdad james bonded me but i think it was the next movie after that tomorrow never dies
[172:22.72] so i didn't actually see goldeneye goldeneye would have come out in 95
[172:27.92] i was not yet 13 when tomorrow never dies came out i was 13
[172:41.28] re-watched it the other week when they re-released the game yeah so how did that licensing work out
[172:51.04] isn't there some isn't there some game yeah okay that that is the one so they finally got that on
[172:59.28] the virtual console on the switch and i'm i'm very curious as to how the licensing around that is
[173:06.00] working out okay
[173:17.04] all right we're gonna have to
[173:31.04] do
[173:57.60] let's see where was this used before it was defined no it wasn't
[174:00.80] liar oh okay i'm wrong it was used before it was defined
[174:11.28] that puts us in a predicament doesn't it
[174:26.72] this is actually not a problem in this case
[174:31.52] whereas the reverse is true
[174:45.84] so
[174:54.32] so
[175:05.12] there we go
[175:20.08] so
[175:27.92] right so we have to create the type def for this
[175:46.56] at param
[175:55.52] um
[176:09.52] so
[176:18.48] so
[176:45.60] okay main net
[176:52.56] oh whoops that was not the right one was it oh it was
[177:01.04] i'm going to get back to comments in a second here i'm on a roll
[177:09.04] okay identifier expected version there we go
[177:22.96] so
[177:30.96] so
[177:55.92] okay
[178:06.88] i'm just uh
[178:15.84] in a mode of concentrated thought right now although i don't really have
[178:22.72] that much to concentrate on but i am in a mode of concentrated thought right now so i'm going to
[178:28.16] keep with that and then i'm going to resurface for air shortly i'm going to get these in alphabetical
[178:36.72] order we're going to make sure that i've typed up them all we're going to update the documentation
[178:42.00] we're going to update the cli and then we we are so close to done oh famous last words every single
[178:48.48] day every single day we're so close to done every day has there been a day when i've said you know
[178:54.40] what this is going to take a long time i can tell actually there was um i was in i was doing this
[179:01.36] process a little while ago and i said oh my goodness um this could take another month that
[179:12.88] was probably the most honest thing i've ever said in my life well it and it could because there's so
[179:20.00] much documentation that could be written there's so many examples that could be written the cli's
[179:25.28] if i'm i'm going to get this thing done for monday uh we're we are going we are going to publish
[179:33.20] monday and and the stuff's i mean we're gonna get we're gonna get this published and dash
[179:39.44] dash keys dash hd sec p 256 k1 dash tx those four things will be published today
[180:03.68] uh verbal stutter verbal stutter verbal stutter
[180:11.76] um
[180:39.68] all right let me catch up on comments rare owns it microsoft bought rare not too long ago supposedly
[180:46.08] the dev team behind the hitman games has the licensing now and they're working on a new one
[180:50.40] that's supposed to be an origin story thing you know you just kind of got to let it go
[180:56.40] it you got to let it be what it is because you when when has it ever worked i okay let's let's
[181:04.32] try this a different way people will pay money for nostalgia but they are always disappointed
[181:10.72] when when have you so it is profitable it is profitable because you will buy something that
[181:16.08] you are pretty sure you're not going to like and that turns out to be terrible but you will buy it
[181:21.68] for nostalgia so that that i think is the the thing that we're kind of fighting against here
[181:29.52] is that nostalgia really really does work against us but when was the last time
[181:37.20] that somebody made a nostalgia play and it worked out the thing that comes to my mind was
[181:45.76] link's awakening but link's awakening was not different it it it it had everything was the same
[181:58.16] there was no original anything in the re-release of link's awakening other than
[182:04.88] that all the code was original it was a complete from the ground rewrite more than a more than a
[182:12.72] remaster but they made no creative deviations the the worst thing that they did was that they added
[182:22.88] a dream effect right but they kept the bugs they kept the bugs that if you walk that they even kept
[182:30.96] so even though the scrolling works smoothly rather than you go to the screen and then
[182:37.36] voom it goes over and you go to the screen and then voom it goes over what i wish they had done
[182:41.92] though i wish they had kept that where it needs to load a new section of the map because what they
[182:47.20] did instead was drop the frame rate and i think it would have been much nicer is if they detected
[182:52.56] that it was going to need to drop the frame rate that instead it just did the womp like it did in
[182:59.20] the original um that's that's the one mistake they made and and then and then adding that haze
[183:08.56] the dream haze in front of the objects but other than that it was completely true and the art style
[183:14.48] the art style was completely true to what the game was even though before it was pixels everything
[183:20.40] about it was was true if you walked between areas the rupees would generate not when it was
[183:26.88] um the rupees would regenerate when you were in a position that would have caused a vump or a
[183:35.60] vump on the game boy version so you could walk basically one pixel down and then one pixel back
[183:41.84] up or not one pixel but one square down and one square back up without having changed the scene
[183:49.36] completely and any rupees in that area would have regenerated so they kept everything about it right
[183:55.76] that's the only nostalgia play i think i've ever seen that works if you try to i mean even with
[184:03.68] other games they they changed too much they they made it too complicated they didn't get
[184:09.84] the emulation right and there's a lot of complaints about the the mario 64 on the switch because
[184:16.88] the the emulation they just they just don't have the chops to do the emulation they need
[184:21.20] to bring in a third party that does emulation and they did but that third party just isn't
[184:25.84] as good as the emulators that we've already had so it's a weird situation
[184:41.44] wait where was where'd generate wiff go
[184:46.08] how did this get here this is the wrong place for this
[184:59.68] oh it's because of the comments i wish they would color these differently
[185:10.24] uh oh you were in a team's meeting what my whole comment was addressing you
[185:15.92] i was talking about how you said that they're maybe gonna do a remake whoops hold on i went
[185:27.12] the wrong direction on that i went to i meant to go there we go you're talking about how they're
[185:33.36] gonna do a remake and i was saying that nostalgia plays just don't work or an origin story and i'm
[185:40.08] saying that that's just not going to work it's just not going to be successful it might be
[185:43.68] commercially successful because people buy things for nostalgia but no one's ever satisfied with it
[185:49.20] so it's not successful in the long term sense it won't be
[185:56.88] so
[185:59.52] so
[186:08.00] so
[186:18.64] so
[186:27.28] so
[186:37.92] so
[186:46.56] so
[186:57.20] so
[187:21.68] oh decode unsafe this is code that i'm not going to
[187:26.00] mess with because that's kind of beyond the scope of what we're doing here
[187:41.28] so
[187:48.96] oh and then in here we actually should do version
[188:09.04] ops dot version
[188:12.64] so they could screw it up
[188:16.16] it is possible
[188:31.76] so
[188:55.92] okay
[189:06.64] so
[189:25.36] there we go
[189:33.20] so
[189:41.92] and i kind of want to put
[189:46.08] this in here as well
[189:55.92] so we're going to do something kind of similar except here
[190:01.52] so let's take the version all the way up to the top
[190:03.28] so it's just going to be let private key equals hex
[190:18.24] i'm gonna do it this way
[190:21.84] and then we're going to do the same thing here pubkey hash
[190:31.04] so we're not going to have any op stop version here
[190:39.20] so we could change this up
[190:47.60] i could say and maybe i should expose these encode pkh
[190:57.52] okay i'm i'm coming up on one other thought here which is that
[191:03.28] priv key should be priv key which why this is will come up later
[191:15.28] which is that priv key should be priv key which why this is will come up later
[191:25.84] and pubkey should be pubkey and the reason is
[191:37.52] oh no i can't do it i can't do it
[191:43.92] i have a good reason for it but we're not going to do it that way so we're going to do
[191:47.44] x priv
[191:50.32] and so x key there we go
[191:56.48] and this is actually duplicated so at some point in the future i could get rid of some of this
[192:04.48] logic from the encode up above or move this logic entirely into the encode up above
[192:11.12] so
[192:22.08] so
[192:31.12] so
[192:41.12] all right so that's gonna these are both going to go away
[192:58.72] they're going to go into the x priv stuff so it's going to be here and here and here
[193:05.44] and this is kind of what i hacky dude in the other one but i that
[193:09.28] i didn't realize they were going to support x keys at the time so i didn't do it very well
[193:14.96] okay let me catch up here let me read comments let's see if we can get this to go out hold on
[193:28.24] uh there we go okay
[193:32.40] i heard most i think of it just what game specifically oh i agree okay got it
[193:42.48] we're we're on the same page
[193:46.64] good
[194:15.52] well that clears things up great
[194:17.12] so to do we're gonna put the switch in here
[194:24.48] people better love this or i'm gonna lose my job
[194:32.08] this is taking forever
[194:35.20] people love it no big problem if people don't love it well not quite but kind of
[194:44.16] you know i'm saying you have to produce things that people want
[194:47.92] i really i think once the suite comes together i think it will be worth it i think basically at
[194:56.48] any cost it's worth it because there's nothing out there this is i i just i don't know i might
[195:03.92] be looking at it myopically i'm looking at it from the perspective i think is the right perspective
[195:07.84] people that don't give a darn about cryptocurrencies we need some hand-holding
[195:36.72] we need something that's great
[195:38.08] and that is designed for people who just don't give a darn
[195:47.12] because you know you don't get an iphone because
[195:51.12] you're convinced that risk processors are the best technology
[195:54.72] you get an iphone because it's an experience that you can understand
[196:01.12] so
[196:02.40] so
[196:15.84] so
[196:29.28] okay bites
[196:43.28] so
[196:52.72] okay so that looks good now
[197:06.72] so
[197:16.16] so
[197:27.64] so
[197:52.48] let me keep as is more polite language
[198:01.92] okay
[198:08.08] pubkey hash
[198:16.40] version should be main net
[198:27.36] pk dash pkh
[198:37.36] or test net
[198:43.68] dash pk h test net
[198:50.48] not version
[199:10.00] so
[199:12.56] there we go
[199:35.60] okay so pk h encode is correct
[199:39.84] and code priv key we need to do a similar switch here it's almost exactly the same
[199:59.28] so
[200:06.48] private key
[200:20.48] so
[200:29.92] let's see let me try this
[200:44.64] so
[200:53.36] okay i hope to not make a fuss but what's your thought on chat gpt
[201:13.52] more the tech than the actual product or you would you consider using it
[201:17.28] yeah so i think that it's kind of a new search engine and just like a search engine it's highly
[201:26.96] likely that the first result is going to be wrong or not what you wanted and just like a circuit
[201:34.48] search engine is going to bring you to stat a page of stack overflow posts of which only two of the
[201:40.32] 20 answers are actually correct i think that chat gpt can do a little bit of a better job
[201:46.88] because of the curation but it's well we'll see what happens because i fear the reason that search
[201:58.56] engines are broken actually i just watched this video let me give you a link to this video here
[202:03.52] um let me just let me scroll back a little bit
[202:12.80] come on
[202:19.52] i think the video is called something pretty generic like why you can't find anything
[202:29.52] okay so the title of the video is what happened to google search and the thumbnail says why you
[202:46.32] can't find anything so what happened to and i'm just going to say to search in general because
[202:52.88] it's not just google it affects the other search engines as well oh whoops that one's got a time
[202:56.72] code in it ignore the time code i i just i guess that's i've started watching it on this computer
[203:02.96] and finished watching it's finished watching it somewhere else and it just when i opened it it
[203:08.00] went back to the last time code but i think that the same problem that's happened with search is
[203:13.76] going to happen with chat gpt right now chat gpt you've got i mean it seems like somewhere between
[203:20.24] a 25 and 50 shot of getting a right answer and about a 75 shot of getting useful information
[203:29.84] that will help you construct better searches to get to the right answer because a lot of times
[203:35.76] you don't know what something is called so for example i i could ask it a question i'm not going
[203:40.32] to do this right now but i could paste it something from bash and i could say what's the name of this
[203:46.40] syntax right so i can't do a search on syntax because those characters are ignored so i could
[203:53.36] paste in something and i could say what is this doing or what's the name of this and because
[203:59.20] it's got a better model it can take syntax from something like a bash d uh what do they it's an
[204:08.16] indirect reference variable replacement very complicated looking it starts with a dollar
[204:13.44] sign bracket exclamation name slash slash has some other stuff but i don't know how to search for
[204:20.16] that thing to understand what it is so i could i could plop that into chat gpt and i could ask it
[204:27.92] and it's going to give me relevant words the problem with with search engines is that seo
[204:34.48] hacking took over search so now when you search for something nine times out of ten it's just
[204:39.92] absolute garbage completely worthless absolute garbage right and i think that the problem with
[204:47.20] chat gpt although it's proprietary and it's closed and it's being curated so the the models that it's
[204:56.72] being trained on right now since they're closed off and they're not live updated it has a buffer
[205:03.28] right so imagine if with google you had a buffer where you were guaranteed that changing your
[205:10.64] website to have different keywords wouldn't have an effect for a year there would be you would want
[205:17.04] to construct really really good websites but it would get rid of all of the fake product reviews
[205:22.88] you know it would it would get rid of so much stuff it would clean it up so much so chat gpt
[205:28.64] there's there's something like a year between releases of data set models so it has a buffer
[205:34.96] but my my biggest fear is that right now they know which websites they're generating so they know
[205:42.72] to ignore articles on websites that they generate articles for and because they're industry leaders
[205:48.32] they know generally which websites are completely chat gpt right so they know how to tell the
[205:54.00] difference between an article that's written by a human on forbes and article that's written by
[205:59.12] chat gpt i mean gpt3 whatever because it's got different names on forbes because they're the
[206:05.84] ones that are publishing those articles on forbes right so chat gpt generates the content for forbes
[206:12.48] and for fortune and for espn and for uh cnet and a bunch of these other sites and then a human
[206:19.44] curates that content you know so that it just generates paragraphs that are statistically
[206:24.24] relevant right so you know give me this thing find the stuff on amazon develop a model take
[206:30.48] from the reviews and the contents and suggest here's a top top 10 list so but eventually
[206:37.12] it's going to start to get really really bad like it is with search because right now
[206:41.84] chat gpt is kind of taken over search junk fake articles have taken over search so you can't get
[206:46.64] to the real stuff but that is eventually going to happen with chat gp2 chat gpt or just in general
[206:52.72] gpt i keep on saying chat but it's nothing to do with the chat chat is just it gives you a prompt
[206:57.52] that's why it's called chat but gpt is the model so it's it's eventually going to happen that that
[207:03.36] there are going to be competitors and i i think that it already has a name llm language learning
[207:10.32] model i think is the generic term chat gpt is the brand name or gpt rather is the brand name
[207:16.16] so llm as competitors enter the space the competitors are not going to know which articles
[207:23.04] are written by humans and which ones are written by other llm and as that begins to happen and the
[207:28.80] data modeling gets more and more muddled we're going to reach a point where chat gpt becomes
[207:33.76] just as useless as searches currently and it's probably going to happen even faster it might
[207:39.92] even happen before the the venture capital sequence is over so i don't have high hopes for it
[207:49.20] but it is a new tool in the toolbox
[207:52.24] okay at what point should someone feel ready to try applying for entry-level roles you don't wait
[208:01.84] until you feel ready that's numero uno you just apply what you it's it's like when you when you
[208:09.52] want to start dating the best thing you can do is pick the hottest girl in the room pick the girl
[208:15.12] you're most interested in right and ask her to dance or ask her to go get a coffee or whatever
[208:23.28] right you just strike up a conversation you say hey i like your shoes do you want to get coffee
[208:28.72] sometime i like trogdor do you like trogdor i mean that's not far from how i met my wife
[208:35.12] or yeah so it's actually incredibly close if you just change out a few words our
[208:40.72] our sentence to start dating our number of sentences to start dating was
[208:45.60] in the low ones
[208:48.80] to progress from the app to meeting in person and then to dating and then to getting married was
[208:55.92] very streamlined not not unintentionally but not intentionally anyway so it's like that you just
[209:04.72] you just do it and the good news is that you're probably going to get rejected and your your
[209:10.56] unrealistic ideal is going to be taken off the table and that's good and you're going to learn
[209:15.12] what failure feels like and you're going to learn that even though you had failure you're still an
[209:19.44] okay person and so go for the thing that's the most unrealistic and idealistic get off the table
[209:25.28] and the other thing is just like the hot girl in the room you know you totally biff it she's not
[209:31.60] going to remember you you're not important right so once you've gotten some experience and you feel
[209:38.08] more confident you know things you need to do you can come back around six months later she won't
[209:44.08] remember that you biffed it or if you if she does she'll just be impressed that you're better now
[209:48.40] same thing with the prospective employer they're not going to remember that you biffed their
[209:52.16] their take-home assignment or whatever it is but if they do they're going to notice the marked
[209:58.08] improvement so you just go for the hottest girl in the room and then you come back around six
[210:02.88] months if you haven't found something else that turns out to be better than what you thought was
[210:06.96] the hottest girl in the room if that makes sense okay thanks comparison to search engines with the
[210:12.00] first results mostly wrong is one of the best i've heard so far to be honest uh we'll save the vid
[210:17.44] and watch later great hey josh can we turn this into a clip uh what do you think about chat gpt
[210:23.44] and we'll have to split that other one about uh entry-level roles but i think we should turn that
[210:30.80] into a clip as well josh yeah yes using it to explain me is just awesome also generating test
[210:38.40] cases for a method is great oh that's cool i haven't uh tried that i've heard about people
[210:43.76] using it for rubber ducking but it responds oh okay i haven't put in huge large chunks code so
[210:53.12] i kind of do whatever uh and josh if you can just splice in between these
[210:59.76] because i'm reading the comments for two different possible clips out of order here
[211:04.16] but you can hopefully see which ones i'm reading and responding to the worst they can say is no
[211:11.04] exactly that's right and and pain emotional pain is just fear leaving the body so you feel that
[211:18.40] emotional pain that little bit of shame whatever you get over it and you are better off for it and
[211:22.32] you are stronger and you're more confident so when i'm curious about what happens when someone
[211:30.96] starts injecting ads into the responses oh my well that has already happened let me go ahead and give
[211:40.64] you uh this tweet i think was shared with me let me go check my dms this is the kind of stuff you
[211:48.80] just can't you just can't tell people about you know uh let's see
[211:53.76] where is it hmm let me see if i can find it real quick i'm not gonna spend too long on this but
[212:04.24] i'll i'd like to find it if i can which is chat gpt bias now this could be photoshopped
[212:15.04] it could be fake but i mean it certainly is convincing uh you could go test it and find
[212:22.16] out for yourself whether or not this is true i think that this is true i don't care to test it
[212:27.36] uh so take it with a grain of salt or whatever
[212:37.36] let's see bias bias bias here we go
[212:40.80] chat gpt bias check that out i will let you look at it for yourself i'm not going to comment on it
[212:52.00] on stream but you can you can take a look at that and you can draw your own conclusions
[212:57.12] but i think that was relevant
[213:02.40] so yeah i think it's going to be more in the realm of subliminal promotion and at some point they
[213:09.36] hmm well it's similar to what's happening now right there's a lot of there's a lot of algorithm
[213:18.16] bias that is built in on purpose and they don't have to market is advertising so they get money
[213:25.04] from some large political organization that shall go unnamed and they tweak the algorithm
[213:33.44] to respond in certain ways and they don't have to label it as promotion because technically
[213:40.00] it's not an ad so i think we're going to see possibly more of that as well where it's uh
[213:46.40] it's not an ad they just paid us on a side channel and we did some stuff but we didn't create an ad
[213:55.28] so yeah i think i think there may well be more of that and i'm sure it will switch sides
[214:03.84] as the money changes hands i don't think there's uh i don't know how much of it is vested loyalty
[214:14.40] in in particular biases biases or ideals or ideas or whatever it is okay so we had here let's go
[214:23.20] let's go back to the top
[214:24.48] uh so in our encode type let me go back to the encode ops
[214:32.96] right and that's anything great
[214:39.20] oh whoops and we need to change this to
[214:47.28] priv key or priv key testnet excellent all right so now this should be good
[214:55.52] adder to pkh decode and i gotta think about this for a second what is decode then decode is you're
[215:14.72] taking you're getting the whole the whole piece
[215:24.16] so
[215:46.48] hmm
[215:57.20] all right
[216:11.28] so
[216:19.92] is this what we want
[216:34.88] so
[216:36.64] yes this goes to bytes that is what we want
[217:02.24] okay good so adder to pkh is good decode looks good
[217:07.04] all right so we have to do type what's really strange to me
[217:32.00] is that this decode does not have a type on it but we are putting a type on it
[217:39.68] and this encode i think we just did that one we we solved that problem in a reasonable way
[217:56.64] um
[217:59.20] i kind of want to do the opposite
[218:04.00] 20
[218:08.72] so decode comes out to parts but not to bytes
[218:15.92] and encode
[218:23.60] hmm kind of makes me wonder
[218:28.72] these feel so here's a thing right the output of a decode should match the input of the encode
[218:45.60] they should have parody
[218:49.84] so that might be our last thing let's make sure that all the rest of this is here
[218:54.80] we could have we can choose to not have parody but then i think i'd want to name it encode bytes
[219:17.52] so
[219:26.80] so
[219:51.68] oh that's
[220:00.80] it's okay to not have parody as long as we are explicit about it we don't name
[220:08.24] things in a way that they look like they should have parody
[220:14.80] also have to consider use cases okay so i have a problem
[220:19.92] which is that dash keys here
[220:29.04] should be of the type dash keys
[220:43.12] so
[220:52.16] hey is this sonic
[221:09.84] nope it's chrono trigger again i think i thought this was sonic last time too
[221:21.12] so
[221:30.40] so
[221:39.20] so
[221:48.32] so
[221:57.44] so
[222:06.56] so
[222:28.24] so this would be priv key pkh or x key
[222:36.08] or xplug
[222:38.48] so
[222:47.68] so
[222:56.72] ah that is an array buffer indeed
[223:13.92] so
[223:27.04] let's see i should probably just uh
[223:39.44] try this way bytes bytes
[223:46.56] okay so i also need to rename u8 to bytes
[224:08.32] hmm
[224:14.72] this one also sounds like sonic but isn't maybe because i'm not listening loud enough
[224:29.12] so
[224:35.12] so
[225:02.72] so was it it was it was u8 it was buff
[225:08.00] i'm not gonna change that in there or in there i'm only gonna change that in this code down here
[225:31.76] whoops that'd be pub bytes so i want to be as descriptive as i can where possible
[225:42.16] so there we got buffer length
[226:00.40] and this would indeed be input is pub bytes
[226:27.68] you can just get rid of buffer entirely
[226:29.60] well those particular cases it doesn't matter
[226:34.32] if it works it works
[226:40.64] okay so do we still have any buff anywhere there's a buff there there's a buff there
[226:56.56] buff buff here and a buff buff there here above there above everywhere above buff
[227:23.68] okay let's try now lowercase bytes where are we seeing that
[227:27.44] that's truly bytes there's no other way to describe it because it is generic
[227:33.12] okay here we're naming it that because of where it's going
[227:42.72] hex to bytes there's no other way to describe that
[227:46.64] um and we have input bytes and output bytes i'm gonna call it hash bytes
[227:53.76] okay verify i think we're out of the area of code that we're interested in there
[228:15.04] okay and so this would be key bytes
[228:17.36] i'm going to change bytes to key bytes
[228:26.24] and then here
[228:39.20] i think it would be very fair to call it not bytes but pkh bytes
[228:46.40] same here not bytes but priv bytes
[229:05.28] whoops one too far
[229:15.28] so
[229:21.12] whoops so here at param encode key ops
[229:42.72] so
[229:52.64] all right that's appropriate to be bytes that's appropriate to be bytes
[230:06.64] all right
[230:12.24] wiff has already defined what encoding it uses
[230:18.72] source bytes
[230:24.40] okay all right let me check chat again sorry
[230:32.72] yeah not sure if that's real might try stuff like that when i'm in there next time
[230:42.72] yeah yeah because that i mean it it would be certainly easy enough to photoshop that
[230:48.40] you know or not you don't need photoshop you just copy and paste yeah it's very easy
[230:54.80] okay priv bytes
[231:04.80] and then do we have anything about hex version string ops encode key so we could say key bytes
[231:21.68] decode
[231:27.44] so
[231:56.16] oh we don't actually have a way to distinguish between
[231:58.40] see
[232:02.64] so
[232:30.88] hmm
[232:37.36] all right let's grab this decode
[232:51.76] so
[232:59.84] all right so another pass from top to bottom here
[233:06.08] adder to pkh
[233:10.88] this is of type address adder
[233:19.52] address is already very well defined in terms of what it is
[233:23.44] okay key bytes
[233:47.68] and maybe this should be not in code bytes but just in code key
[233:50.48] and i could get on board with that
[234:17.36] did i not do this
[234:22.96] ah it's not comparable to type version
[234:37.60] so
[234:42.56] so
[234:52.16] so
[235:03.76] okay encode key
[235:22.00] ah and this would be x x key bytes
[235:31.36] i heard something kind of beeping
[235:45.36] i don't know what it was or why
[235:47.36] i think it was all the heaters turning off
[235:59.36] because they're warm enough to not need to pump out any air they're all well above there
[236:07.68] so
[236:12.56] let's see
[236:30.56] so
[236:40.16] okay
[236:54.96] so
[237:05.28] let me make sure that this is correct here
[237:23.12] where was private private key
[237:37.84] hearts.xpriv and xbomb
[237:50.00] oh crap what about decode
[238:04.72] so
[238:14.16] oh there it is xpriv xbomb okay good so everything is there
[238:32.96] ah i am being inconsistent about the use of x key
[238:35.44] okay which way is it is it x key or is it x key
[238:49.52] okay to do
[239:02.24] wait do i expose that because if i don't expose it and it doesn't matter i do expose it
[239:06.96] we need to be consistent throughout the ecosystem we need to pick
[239:16.88] nomenclature and stick with it although again that is not exposed so let me just
[239:23.20] go up to the top here we started with uh dash keys dot wait why did that not work oh
[239:36.64] okay that is only internal
[239:45.68] that is not exposed to the outside world so it does not matter
[239:52.64] if if it's not perfect it's not going to become part of the v1 api so we are we are solid there
[240:01.92] all right next priv key pov key with all right pkh that's what i thought
[240:16.24] oh let me just start with this one pkh goes where pkh comes up battery backup ah
[240:25.92] yes yes so it was probably the battery backup just doing a little cycle that's probably what
[240:33.52] the beep was i thought that it was the the heater uh turning off but it wasn't that kind of beep
[240:39.68] because these ones they don't they don't typically beep when they change modes they just
[240:45.36] turn on and hum a little or they turn off i think you were right
[240:48.64] i think it was the battery backup was doing its self-test
[241:00.24] so
[241:29.68] so interestingly for a minifier i wonder if a minifier would be smart enough to evaluate this
[241:37.12] oh hold on - 58 check that okay good uh and be able to trim these down
[241:59.20] yeah it was a good guess
[242:05.28] and i'm not going to use the word pay anywhere in here
[242:15.52] good got rid of the word pay
[242:25.68] okay
[242:35.20] okay whiff to adder
[242:49.20] so
[242:57.28] oh priv key to whiff is in here twice let's see which one is better and why this one is better
[243:18.16] because it allows for the option to be passed in so of these two see this could lead to a
[243:24.64] subtle bug this is another reason to alphabetize because when you
[243:28.40] you're working on something over time and something changes
[243:44.24] so
[243:54.32] all right
[244:08.32] okay
[244:10.88] so
[244:20.88] all right this is obviously a little too long that's a
[244:35.20] little too long
[244:45.52] so
[244:55.52] so
[245:05.52] so
[245:15.52] so
[245:25.52] so
[245:35.52] so
[245:45.52] ah this one we also need to pass in a version too
[246:01.68] so
[246:09.20] and this one needs callback and this one is going to be pub key hash to address
[246:23.20] so
[246:31.52] okay and this is going to need probably encode ops i'm guessing
[246:51.76] lmn
[246:57.04] okay so this one goes right here and then we may also want to use
[247:11.92] so
[247:20.32] all right
[247:37.44] so
[247:46.56] oh
[248:00.56] do people often use shorthand syntax i'm finding a lot of variations in the way some things can
[248:06.00] be done and i guess most companies will spell that out in some kind of style guide
[248:09.76] no no they don't
[248:23.36] josh nice short hot take clip there
[248:33.04] uh verbal stutter verbal stutter
[248:36.64] if you're lucky they'll have a style guide top companies that have lots of employees
[248:45.52] do but give me an example of what kind of short short hand syntax you mean because there is a lot
[248:54.72] of shorthand syntax i prefer one operation per line that's what i'm driving towards more and
[249:01.52] more and more i don't think that there are two operations in any of the lines in this uh dash
[249:08.32] keys code some of the dependency code that i copied in has not been refactored that way but this
[249:14.32] has only one operation per line let's see i want to actually pull this out as well
[249:28.56] now i forgot what i was gonna what i was gonna do all right priv private key to whiff where were we
[249:36.32] at here like using ternary operator you mean using a ternary operator to complexify an if else
[249:48.32] statement what we need is we need to have more if expressions so that a ternary operator is not at
[249:58.24] all seductive because the thing that makes ternary operators seductive is that javascript doesn't
[250:02.40] have if expressions so in an if expression you can do something like this let x equals if a
[250:11.28] a else if b b so this is an if expression
[250:26.08] you could potentially have a return there but yeah we don't we don't have if expressions
[250:38.80] we don't have if expressions and it's a darn shame a darn shame
[250:53.76] a darn shame
[250:54.56] i well i don't know i haven't used if expressions to know whether or not they lead to
[251:01.12] ugly code they very well could yeah uh a good company
[251:06.16] a good company will have a style guy that certainly forbids ternary operators
[251:10.24] in general things that are nested just should not be allowed
[251:15.92] and ternary operators lend themselves to all sorts of confusion it is it is bad code style
[251:23.12] no one so people will tell you this people will tell you oh but did you know but did you know that
[251:30.48] you could shorten this to just one line that's people trying to tell you how much they know
[251:36.00] right but what you'll never find is someone never is a strong word because there are those people
[251:42.96] out there that literally their brain operates on terse mathematical notation but they should be
[251:48.88] using functional languages and not bother the rest of us there are those but in the general
[251:56.32] case you're never going to find somebody who looks at some code that's written out line by line and
[252:01.04] says oh this is too hard to read they may not like writing it but you spend most of your time reading
[252:06.64] code not writing code so ah what i do come back all right i was making sure that we have okay i
[252:24.80] kind of lost my spot i'm going to continue down to the bottom and then go back up to the top one
[252:29.20] last time okay public key to pubkey hash pubbytes and then this would be shawripebytes
[252:39.68] just call it that
[252:49.60] wiff is already self-defined there's nothing else needed
[253:04.08] i don't need anything else on top of it and then utils so this is looking really good
[253:16.16] i'm going to go ahead and whoa what the letter l okay
[253:22.64] nope
[253:36.64] okay
[253:45.44] finish utils and types
[253:52.24] all right so last last round here i'm going to just make sure every single one of these is as
[254:09.20] correct as it can be so decode we don't need any extra options let me just double check on that
[254:13.60] decode ops oh the decode ops that we would need if any is do we want to validate this yes or no
[254:19.60] so decode equals that's not what i'm interested in wait where'd this
[254:25.92] what what okay well i'm here this is where i want to be so address
[254:32.48] if we're going from address to public key hash yes we always want to verify no we don't want options
[254:44.08] uh we're always going to return the pubkey hash and this is
[254:48.72] pubkey hash pkh bytes and this oh this would otherwise be shawripebytes
[255:10.32] excellent decode and this is any base 58 check key
[255:17.04] so that had a typo let's get rid of it this does need ops for the verify
[255:26.88] but we're not going to pass those ops down into this decode
[255:34.24] oh whoops we need to make sure that we await everything
[255:39.44] await await await await await all the things
[255:43.76] all right okay so we're gonna check some of the parts we're gonna check
[255:55.76] so we're doing the verify step ourself
[256:02.32] we're gonna call verify if it's not valid so that we get the right error message that's all
[256:08.72] okay decode decode decode decode let me see here
[256:25.68] so we're decoding the right thing which is the encoded base 58
[256:32.64] we're doing the check that's right we're setting whether or not it's valid
[256:38.88] so the type is the thing that we have as a to-do here so let
[256:43.68] us consider that real quick hey what's up xplonidu yeah so dash incubator is
[256:52.80] this is the the channel where i'm doing the dash incubator work hardcore cool age 86 is still
[256:58.48] my main my main channel and sometimes i'll do dash incubator work there
[257:03.92] okay holy heavens holy heavens
[257:09.20] this is such meticulous work
[257:17.28] okay so this decode oh we don't say what it returns no wonder i'm missing a bunch of returns
[257:26.56] that's why we're having such a problem here
[257:30.32] okay so we're missing what this returns and what this returns is
[257:43.60] i forget what it's called parts
[257:52.72] we're gonna we're gonna redefine
[258:00.72] decode parts here
[258:07.28] so
[258:13.84] and what this is is going to be valid
[258:27.84] it's going to have pubkey hash and this is going to be
[258:37.12] hex we're also going to do a type alias in here let me go ahead and do that right up top type aliases
[258:45.44] type definitions
[258:57.52] so
[259:06.56] okay
[259:10.16] so
[259:20.56] i don't really want to do this one
[259:24.96] um
[259:26.00] i would actually i would rather go back into the base 58 check types and just add
[259:39.60] on here where there is valid
[259:42.24] that let's see why would that be
[259:51.28] so
[259:54.24] i'd rather add on here that
[260:11.52] there can be a type
[260:21.04] so
[260:23.36] uh let's see
[260:37.36] private pkh
[260:46.56] x pub x prove or
[260:50.48] x pub
[260:54.56] so let's go ahead and define
[261:02.88] what is that called key type so we're going to type def key type here
[261:13.92] oops
[261:23.76] so
[261:50.16] we do have the option of having nothing that's okay
[261:55.60] okay so then back up here
[262:02.00] oh this key type thing
[262:18.40] yeah pub key hash part okay
[262:21.60] give me a second i'll check chat again
[262:37.76] pkh
[262:44.40] actually q r s t so type should go after pub key hash this one
[262:52.96] type should be x priv type should be
[263:11.04] right
[263:20.48] so
[263:42.88] c parts
[263:49.52] and then with this ones we can actually be more specific
[264:00.80] let me go back to this because parts is any of these
[264:07.12] so we can go back to where was it
[264:11.28] because we know what we're going to return in most cases i think
[264:29.60] so
[264:37.92] ah that's getting really long i don't like it at all
[264:53.44] so
[265:02.00] all right so let's get back down
[265:21.76] to here and what are we returning we're just returning base 58 check parts simple as that
[265:30.64] so everything needs to have its return defined
[265:40.48] okay decode parts decode ops that doesn't have return in code returns a string
[266:02.88] call that generate with oh and this needs to be promised
[266:07.12] let's make sure that everything is promised
[266:13.12] i gotta go back through on the top and make sure everything is promised
[266:16.40] okay generate actually don't think that has to be a promise but we're going to keep it as
[266:26.80] no it does needs to be a promise okay pubkey hash to address yep that returns a promise
[266:36.80] public key to pubkey hash that's promise it's the promise
[266:52.40] to public key that should also be a promise need to make sure about that one that that's
[267:01.36] marked as a promise everywhere okay that has a return value and this has a return value
[267:09.44] okay so that was the only one that was missing the return value
[267:13.28] to public key let's just make sure that there isn't a wait wherever this is used
[267:20.72] in this particular case an await is not required but in the general case it is
[267:26.88] because we don't know what is going to be used to produce this
[267:32.16] we know that it's always possible to turn bytes to hex hex to bytes big n that's always possible
[267:42.88] synchronously but if we swapped out the implementation for the crypto module or if
[267:48.48] the web standards start to include the secp256k1 curve then that would become async so it needs to
[267:54.24] be marked async now all right so is everything awaited let's just doing a pass of is everything
[268:04.08] awaited yep that is awaited
[268:06.24] okay and this is marked async so i'm doing my everything's awaited pass
[268:17.04] are we await await await await okay await
[268:24.00] code
[268:33.60] i like to separate returns so that we can name whatever the thing is
[268:42.40] uh it's parts that's the right name that's the right name
[268:56.16] all right
[269:04.16] let me check a chat real quick
[269:08.08] i meant simplify lightly i definitely like the if statement spelled out because that's
[269:12.48] me from learning some c no that's everybody everybody everybody who's a sane rational person
[269:18.40] wants to see it written out what it does using mathematical shorthand notation is just a bad
[269:28.96] idea it never turns out well it never withstands the test of time never you never hear somebody
[269:37.60] complain you know it's too bad go doesn't have operator overloading or you know it's too bad go
[269:45.92] that go doesn't have ternaries you know and just those things should be macros that's what they
[269:54.96] the any type of of condensed syntax like that it should not be part of the language it should be
[270:00.00] part of a macro that you can type it and then it expands out into what the actual code is that's
[270:05.92] what it needs to be
[270:06.72] yeah i saw in the tutorial you know tutorials about teaching you cool things so you can look
[270:16.88] cool but in the office anytime someone says oh that's cool that is a reference to you know
[270:22.96] somebody says oh that's cool that is a red flag i turn around in my chair and i stop whatever's
[270:27.76] happening right then and i'm not kidding i really do if somebody says that's cool
[270:33.28] i get over there and make sure that mistake doesn't make it into the commits
[270:36.64] oh this is the ai replicant you can notice from the skin see how the skin's a little different
[270:45.04] that's because i am an ai replicant
[270:48.24] okay so here what is this one encoding
[270:53.12] that one's
[271:07.12] so
[271:10.64] oh where was x key used here
[271:24.64] oh
[271:28.64] let's see
[271:35.12] there we go cleans that one up
[271:39.68] all right two things i'm trying to do i probably should only do one
[271:48.80] do we have an await and do we have a return
[271:54.64] do we have an await and do we have a return
[271:59.20] await await
[272:06.48] await
[272:20.72] await
[272:25.76] return
[272:27.28] okay
[272:40.72] so
[272:48.80] now we are finally finally finally finally finally finally finally finally finally
[273:01.12] ready to finish the readme
[273:02.80] and now we finally have the api
[273:07.68] so here we are
[273:20.24] we actually need two of these we need utils
[273:26.24] okay so this is the full api
[273:34.96] so now we make sure that we include everything in the api section and we publish
[273:44.08] will it happen could it be i don't know i've got i've got a p
[273:50.16] i didn't mean that to rhyme it just it just happened you know
[273:59.52] so
[274:08.56] all right so
[274:22.56] so
[274:31.60] oops
[274:51.52] um with string
[274:58.48] so
[275:07.44] so
[275:16.40] so
[275:25.36] so
[275:34.32] so
[275:43.28] so
[275:52.24] so
[276:01.20] um
[276:17.20] um
[276:22.16] keys that are
[276:24.16] hierarchically i can't spell that word hd wallet
[276:36.32] i can't spell that word hd wallet
[276:55.92] hierarchically deterministic or simply generated from passphrase
[277:20.88] so
[277:42.16] 44 there we go
[277:49.12] all right let me see poet and didn't even know it
[277:58.40] rap a name little aj aj the dj wicka wicka so i was a wedding dj for
[278:07.36] for probably about five years i enjoyed it
[278:10.88] i could have made a living off of it i just did not choose to take that path
[278:17.36] well i did choose to take that path actually for a while
[278:28.96] but it was not my main source of income at any time
[278:34.88] so
[278:42.88] so
[279:10.40] okay looks like
[279:15.36] internet blipped
[279:19.52] what's the worst thing you've seen at a wedding well women with no underwear of course
[279:26.72] i mean that could be the best or the worst thing depending on how you look at it but
[279:30.16] there was uh i think somebody got alcohol poisoning
[279:37.04] but that was also the same that was the only wedding where one of the women
[279:42.80] i don't know if she told me she was i don't know how that happened she was drunk
[279:50.72] and somebody else got drunk to the point that they had to get people there they the person had
[279:59.12] alcohol poisoning that was the worst thing i've seen at a wedding because you know that really
[280:02.56] puts a damper on what should be a good day with your friends they just took it a little too far
[280:07.60] and sometimes people made crude jokes or whatever but it's not that big of a deal
[280:30.40] say hex string
[280:36.56] oh i guess i should expose
[280:47.20] the let me let me go ahead and make sure that's exposed actually where is ripe md
[280:55.44] so
[281:25.04] wasn't there a encode or something that i added to this i thought i
[281:29.44] i thought i did add something at the high the upper layer but maybe i didn't and then just as well
[281:34.96] okay hash
[281:39.20] sure
[281:53.92] so
[282:03.36] the other nice thing about one operation per line is it does make you well just makes you better
[282:15.68] at organizing your code and considering the api because if you think okay
[282:21.52] every operation needs to be on just one line you find a better encapsulation for your operations
[282:33.04] so
[282:39.28] qrs
[282:53.28] okay now i want to reach in to change 256 sum as hasher
[283:16.16] so
[283:25.04] so
[283:35.92] so
[283:54.80] so
[284:22.68] okay so it's going to take in bytes and it's going to return bytes
[284:26.60] i like that better
[284:51.16] ripe md 160 sum it's got a weird name but whatever it is what it is
[284:58.20] oh
[285:06.68] so
[285:16.20] so
[285:25.72] so
[285:35.24] so
[285:44.76] so
[285:54.28] so
[286:23.80] all right q r s t
[286:30.44] that's it
[286:44.44] so
[286:51.08] hash utils qtels byte utils i'm just putting these in the order that i want to put them in
[287:05.08] so
[287:13.72] again all of these are async
[287:27.72] so
[287:36.36] pubkey hash
[287:55.40] shaw ripe bytes
[287:57.96] all right
[288:05.96] okay and the reason
[288:16.84] oh no what is it true charade wow whoa everybody
[288:23.48] all right what's up
[288:45.32] okay so yeah let's go well first first i got i got uh one comment to catch up on
[288:52.28] while i'm fixing this here okay seems like a good hobby we're talking about me being a wedding dj i
[288:57.72] used to mix a little but it was for fun yeah i didn't mix anything i was i was mc i was all about
[289:02.92] the entertainment getting people in pulling people together making it fun i really didn't
[289:07.64] do much with the music other than that i had really nice speakers actually i still have them
[289:12.92] they're up for sale if you'd like them all right these speakers are from last season they're for
[289:18.04] sale if you want them anyway i use a little mix but it was just for fun mostly dubstep drums
[289:23.40] and bass although i take that back i did assist my friend host karaoke a bunch of the bar
[289:28.36] they liked when i was running the music said i actually played different songs every yeah that's
[289:37.80] good that's awesome okay so hey everybody uh we are doing super boring stuff so i apologize in
[289:46.68] advance i have been meticulously going through so first oh man there's so many disclaimers i need
[289:53.00] here first of all so this is the dash a commuter channel i'm cool aj 86 i'm ajo neal but i'm cool
[289:58.44] age 86 so if you like my style of stuff you can subscribe to both channels i'm on both channels
[290:05.96] and and i host either channel when i'm doing the one or the other but so i am working on some
[290:13.16] cryptocurrency stuff i'm not a scammer i don't want to take your money i promise but i'm working
[290:18.12] on some tools i'm working on developer tools for cryptocurrency particularly for the type of
[290:22.84] developers that don't really care about that stuff and wish that if you wanted to do anything with it
[290:27.56] it would just work okay that's what i'm trying to get to i'm trying to get to the point where
[290:31.56] merchants could just use this stuff and there are a collection of about 10 tools that over the past
[290:37.48] two or three months i've been working through and either heavily refactoring or rewriting from
[290:43.64] scratch in modern javascript so the work in node and in the browser using web crypto not having to
[290:50.12] have all these shims and it uses big ends uses web crypto so i've taken from different forks
[290:56.36] and from different i'm just doing a whole bunch of curation and now after doing all of that
[291:02.68] i'm about to publish the first module where everything has been meticulously designed from
[291:09.64] top to bottom as simple and complete as possible is what my goal has been
[291:17.48] so that's that's where i'm at one there's a few things i'm still not sure what to name them
[291:24.36] um
[291:28.36] let's see b58 c string and that's kind of where i'm at right now
[291:35.64] because i'm just trying to figure some of this stuff out so this one
[291:41.32] would be i think version are we saying decode version no validate
[291:48.52] validate is is what we're saying okay and so this is going to return
[291:53.24] of a type of key so this is going to be this is going to be a private key pub key hash
[292:06.76] um or x x key extended key that's too long
[292:21.72] a key it's type
[292:28.52] uh let's see i actually want to try
[292:42.52] version let's try this version type check
[292:50.20] etc this is
[292:55.32] so this is going to be
[293:00.52] there we go okay now let me check out uh let's let's check out some of the comments here so we
[293:08.92] got the raid raid raid super boring stuff liking like something like super mario kart
[293:13.32] we are listening to delta rune a glitch hops world so that's the musics
[293:19.64] i i like to listen to vgm we love stuff that works the job it works and does the job thank you
[293:26.36] and that's the boring stuff how do we make it boring that is the question i try to avoid writing
[293:33.24] this myself so this is i've also specifically tuned this for dash for the digital cash for the
[293:41.64] dash cryptocurrency but you could make a fork of this and you could make it work for something else
[293:47.32] uh it's just a matter of changing a bunch of magic bytes i can show that to you real quick so
[293:52.52] and there's a whole suite it's the whole suite it's everything the hd keys the wallet well the
[294:00.20] wallet's not going to get published by monday but this is this is going to get published today
[294:04.92] the the the payment transactions because transactions are so crazy there's a hundred
[294:10.68] million different types of transactions so basically if you just went in here and modified
[294:15.88] these four variables it would work just as well for anything else but in terms of i want to make
[294:21.32] this streamlined for the dash community because i want us to be able to make the best tools and
[294:25.96] not have to rely on what i've been saying the whole time for about a year is we need vertical
[294:31.24] integration we need this thing from top to bottom to sing every piece to be fit together on purpose
[294:37.40] and we need cohesive documentation that's the same across the board and so that's what this is
[294:43.88] that's what this is uh okay all right let me see what else what else we got uh oh man he pro i
[294:56.76] won't deny that thank you better use something someone spent time to make work something better
[295:05.40] uses yeah i'm like english please i'm just learning javascript okay well this is this is one of the
[295:12.52] distinctions between the cool age 86 channel and the dash incubator channel dash incubator channel
[295:17.56] is right now at least it is hardcore low-level cryptocurrency crap the cool age a6 channel
[295:25.72] i do projects and i try to keep things a little bit shorter but i recently just split them because
[295:32.60] i was doing too much of the dash incubator work but uh dad so javascript the best way to learn
[295:38.84] javascript i think i even have this in the little shebang thing if we do bang javascripts
[295:44.20] does it come back oh no let me try this again how about node if we do no there we go so there's a
[295:51.96] couple of playlists here you should take a look at specifically the crockford playlist is the best
[295:56.12] playlist it is dirt old but it doesn't matter because the core principles never changed yeah
[296:03.16] there's a lot of new syntax most of it is worse so i highly recommend checking out the crockford
[296:08.36] series that's what just popped up there uh yeah you can soak it in that's another thing you can
[296:13.88] just take stuff if stuff's too advanced it doesn't really matter you can just soak it in and you hear
[296:20.12] the words and the terminology and over time it starts to make sense you know over months of just
[296:25.16] listening to people talk about stuff it kind of comes through osmosis i mean of course you can
[296:29.64] study too um i'm seeing the comment lines we was struggling to get me to understand okay setting up
[296:39.72] so what i'm doing right here is i just i just did a grep let me show you what i did so i i i think i
[296:47.96] finished with all of this stuff and i just did a grep through my file to basically see what all of
[296:54.04] my exports are and so all of this stuff are my function definitions and i'm taking that and
[297:00.04] putting it back in the readme so that it can be there in the readme so that somebody can use it
[297:05.08] so there's somebody knows how to use it and we don't actually need these three those are
[297:08.60] those are more private uh as in i don't want them to be exposed as part of the guaranteed v1.0 api
[297:19.16] all right let me see if i can you're fascinated great that's awesome i'm gonna just kind of pop
[297:25.80] this up here i know it's a little bit early you don't know me yet but i'm just gonna pop a little
[297:31.00] likes up follow if you want to i'm not trying to tell tell you how to live your life but if you
[297:36.60] like what you like you get more of what you like caveat if we're talking about code i am definitely
[297:41.40] trying to tell you how to live your life okay yeah so the crockford series i still think is the best
[297:48.20] series because it's focused on the practical stuff not just what's shiny all right so this one
[297:55.16] encode bytes and i think all we really need for this is just version
[298:00.12] and then what comes after that so let me go ahead now i can get rid of these
[298:07.48] and then i can change this to js and i just need to decide what i want this to be called i think i
[298:16.76] want to call it encode key i think that's what this should be called is encode key not encode
[298:23.72] bytes because encode bytes it's it only takes specific types of keys and then decode the reason
[298:31.96] that these are not named the same i have a decode that's not the same name the same as the encode
[298:36.20] because the decode is going to give you back an object and the object is going to have
[298:44.60] it's going to be more debug information i guess i could i could create one called inspect
[298:49.72] and then i could have a decode and an encode that might be what i should do so i'm gonna
[298:57.16] i'm just gonna pop this out as an idea that we're gonna have an inspect
[299:01.96] and then we're gonna have this is what yeah to do
[299:11.96] so encode and decode will give you the minimal amount of information
[299:15.48] and inspect will give you all of the information which then i have to consider what is the
[299:22.76] difference between the two because generally you want the type information back as well
[299:30.04] so you'd want version and type back it's just if you have two functions that are of the same name
[299:39.32] so for example parse and or not the same name but a complementary so encode and decode
[299:45.08] whatever you take out of whatever the return value of an encode should be the value you can
[299:52.04] pass into the decode and whatever comes out of the decode you should be able to pass in
[299:56.52] into the encode but i don't actually want that symmetry for this use case
[300:01.56] because of the way the use case is okay so let me go ahead and get these we're going to comment
[300:10.84] these and then i'm pretty much that's it i mean this has been many hours this has been basically
[300:15.72] a 20-hour project after having been a 20-hour project that just just the the finalization of
[300:23.48] this package to bring it all together to get it documented you got the other problem in the
[300:27.88] cryptocurrency uh ecosystem is that because everybody's developing the modules independently
[300:34.20] everything has a different name so somewhere it's called pub somewhere else it's called pub key
[300:39.80] somewhere else it's called public key somewhere else it's called key somewhere else it's called
[300:44.20] validator or something like that or point point is another name for it so within the ecosystem
[300:52.76] everything has a different name even when it's the same thing and that's one of the things i've
[300:56.20] been doing is just very meticulously going through and deciding how can we make sure
[301:01.56] that across our ecosystem that we have consistency anywhere you see a name there's one of a few ways
[301:11.08] that it can be named and that name if it's different it's different for a specific reason
[301:15.88] all right you're not falling asleep yet well that's because you all joined it now i'm engaging
[301:22.84] in the chat but once i get back to the code then you go you know what i'm saying who needs shiny
[301:28.52] when you can have rocks you are my people god bless you uh i don't i just
[301:36.92] yes hopefully that came through loud and clear
[301:48.76] all right uh catching up here on chat so so much chat explains it well and the quirks in between
[301:54.20] keep you entertained involved that's oh thanks that's a good uh i'm gonna i'm gonna snap that
[301:59.88] as a as a testimonial here okay i do a blend of javascript sequel in python mainly for the day
[302:09.00] job data engineer but javascript and snowflake instead of web i don't know what snowflake is
[302:14.12] difficult things in program yes of course naming things cash and validation and off by one errors
[302:18.60] the two the two difficult things standardization is key well we've reached 100 messages
[302:23.48] you nailed the raid yes indeed indeed so unfortunately here's the bad news this
[302:32.68] channel is less than 30 days old so it can't raid yet so when when i go to take my potty break
[302:39.48] eventually at some point uh or when i'm done publishing this eventually at some point i
[302:45.72] unfortunately i cannot continue the raid because it's less than 30 days old if you know the channel
[302:50.12] that allows raids for channels other channels that are less than 30 years old you can feel
[302:54.20] free to suggest one okay so encode key i think that's the right name so let me go back here
[303:00.12] because it's not about encoding the bytes it's about encoding a key because specifically it is
[303:06.92] a key all right encode bytes so
[303:12.28] dash keys we can have encode key
[303:18.92] we could have a decode key i don't know i don't i'm gonna leave it this way for now
[303:29.16] because i just i i'm i'm sold on
[303:34.36] i'm sold on changing the name to encode key
[303:39.32] i don't think i'm using loose terms like bytes in any of the actual definitions okay
[303:51.32] all right so here encode key i'm gonna leave it like this
[304:00.92] all right so here encode key so what this is going to return is base 58 check encoded
[304:11.32] private key uh key i'm trying to keep these on one line as well that's that's tough
[304:19.80] so this one didn't quite make it for example
[304:29.16] so i'm going to get rid of that for now i don't need to to do that anymore
[304:33.16] all right so this one putting the shot right bytes and we're getting back
[304:47.48] address
[304:53.00] address
[304:58.12] with
[305:05.32] let's see pub key to pkh
[305:13.80] so that's going to be bytes take some pub bytes and then comes back with
[305:20.68] um so i'm also thinking this is one thing that i might still change is making pub key all lowercase
[305:32.20] one word making priv key all over case one word rather than being multiple words and the reason
[305:37.96] for that is for when because there's basically three different use cases there's internally
[305:45.16] what something is called what arguments it accepts you don't have to name it that same time
[305:49.16] have to name it that same thing there's externally when you write the name of a function
[305:53.80] i wouldn't be able to document it on one line if i put this function all the way out for what
[306:00.44] it's converting so i don't i shorten this to pkh rather than pub key hash
[306:07.00] and that allows me to shorten
[306:12.20] uh public key to pub key and some other things but then what it accepts i want it to be clear
[306:22.84] from the documentation the the type of thing it is too so the name of the thing should tell you
[306:30.04] what you're passing in and then you got some documentation about what you get back
[306:38.92] so yeah there's that and i think i'm going to take these two
[306:43.80] and
[306:46.54] generic base 58 check
[306:59.56] codec for all of private key pub key hash
[307:06.52] um extended privates extended ah i think i'm just gonna have to go with x pub x x priv x pub
[307:21.80] so maybe like this
[307:40.36] say and extended keys
[307:52.68] let me say
[307:53.40] extended private x priv
[308:01.24] and extended public x pub there we go
[308:18.92] conversions the the most important one is really just going to be this one
[308:28.28] i don't know i have to think about it whiff to adder but you can't go adder to whiff
[308:34.04] but the thing i think is most important typically is going to be
[308:42.68] well all of all of these end up being important
[308:45.08] common okay streamlined conversions there we go and then what were the what were these ops
[308:54.92] um i don't think we need any ops for public key hash to address oh we possibly do which is
[309:10.36] we possibly do which is version okay and then private priv key to whiff version
[309:19.24] yeah so that needs to be known
[309:39.00] i'm gonna for the sake of getting this to fit on the line i'm gonna move that one back
[309:43.96] i'm just gonna call it pkh bytes or call it hash bytes okay and then this one all right
[309:53.80] i'm checking out some other stuff here enchant key sure all right going to work on some stuff great
[310:02.04] all right i'm gonna check back here boom boom oh snowflake the data the cloud platform okay yes i
[310:10.92] know about that one the the database but i i used it only very little i just i connected to it for a
[310:17.88] thing i didn't use any of its features i logged into its portal just to debug some columns i
[310:24.12] didn't work with it closely oh yeah there is a discord too yes uh the discord is comes up with
[310:30.76] the like it doesn't come up with the discord command but it just did pop up a second ago
[310:35.56] listening enchant key all right i'm getting off to work i'll be headed home do you do any more
[310:43.48] streams later today i don't know probably because i did not get very far on this i mean i'm getting
[310:49.40] to completion but i really need to knock some of this stuff out of the park for a an announcement
[310:56.04] on monday so i thought i thought well i went down this big rabbit hole because i thought that i'd
[311:02.28] done the whole tool system and all i needed was to go update some documentation and then i came
[311:06.68] back around to these two modules and realized oh wait i because i was kind of doing things in rounds
[311:14.68] which i think was the right way to do it rather than completing one thing all the way through
[311:18.44] which is what you typically want to do typically you want to avoid having multiple projects open
[311:23.32] at a time but because this is an ecosystem problem i was getting different pieces in place and
[311:29.56] pulling them together and so it's not it's not a common project because it's a system of projects
[311:36.52] not a project in of itself each project was individually complete but systematizing them
[311:42.36] is taking pretty much just as much time it's embarrassing but
[311:52.84] okay so to do
[311:55.64] pub key versus pub key so i was all in on public key
[312:05.88] let's see is any of this stuff this is all just i don't need any of that anymore i'm just going
[312:17.96] to get rid of that those are my little to-do items that i need to i need to i need to walk
[312:23.56] away and sit on them but i can go ahead and publish this with as 0.9 and then if i decide
[312:29.88] in version 1.0 to change a few more of these that's fine but i think i need to publish the
[312:34.44] entire ecosystem to 0.9 and then figure out any of the little nitty-gritty stuff and then publish
[312:41.00] the 1.0 okay pubkey takes pubbytes to pubkey hash this is also so this is the shaw ripe hash
[312:49.56] uh uint8 array
[312:57.56] okay so some of these are reversible and some of them are not so for example
[313:10.12] we can do adder to address to public key hash and public key hash to address we can do
[313:17.08] um
[313:19.32] let's see paired streamline conversions we can do private kiff with to
[313:37.96] private key to whiff and we can do whiff to private key
[313:42.44] but we cannot go from address to public key we can go from public key
[314:03.48] to public key hash
[314:29.40] so basically we could put one more in here that would be pubkey to adder
[314:37.64] just kind of
[314:42.76] skip a step here
[314:47.00] i think i'll just go throw that in there real quick
[314:56.60] all right
[315:08.68] public key to address i can put that right below actually
[315:24.20] all right so this should be pubkey to adder and then this should take
[315:39.48] pubbytes and it does need to take ops
[315:43.40] but basically at this point we could say
[315:51.08] uh we could do
[315:53.16] pubkey to pkh
[316:11.80] and then we can do
[316:17.88] pkh to adder
[316:28.92] pass in the shaw write bytes and the ops
[316:37.64] and i'm being very very explicit with what these things are named because it was such a point of
[316:44.44] confusion when i started getting into this trying to figure out well which of these is
[316:48.92] actually this thing and which of them is actually that thing because they're among the different
[316:56.28] cryptocurrencies there are different standards and it's nice to know this is these are shaw
[317:01.72] write bytes they're not shasha bytes or shaw three bytes or shaw three shaw three bytes or
[317:07.32] shaw two shaw three bytes these are shaw write bytes because it's one of the things that is
[317:12.36] different okay so this is going to be public key to address and this is going to be pubbytes
[317:37.80] and then
[317:46.44] it's going to take back
[318:00.44] an address
[318:04.52] so
[318:13.08] okay what was what did i just do here i just added
[318:29.96] type and impl updates i'm going to rebase this before i finally get it in
[318:37.96] oh whoops that's not what i wanted to do
[318:43.32] okay
[318:52.52] so
[319:18.92] bi-directional conversions one-way conversions
[319:24.60] okay so this one ends up being
[319:36.12] address
[319:46.92] all right
[320:01.24] so
[320:09.72] okay so everything that i've got here most of it is uh you know was was there
[320:21.00] all right helper c helpful helper
[320:32.60] so
[320:41.08] so
[321:05.88] and x keys i'm just gonna leave it at that
[321:18.68] options let me just document some options here
[321:34.28] so i'm going to put this as json so we're going to have validate
[321:37.24] well i can actually put this as js true throw if check
[321:45.72] if check some fails
[321:58.28] and then version
[322:02.28] is going to be
[322:05.48] so okay this is this is what we need we need
[322:11.16] these are pretty simple they don't really need much more explanation
[322:16.28] common encoder decoder options
[322:27.64] so version can be main net or test net or
[322:33.80] uh what is it 4c or cc
[322:39.48] or it was cc or 4c or ef
[322:48.60] or 8c or
[322:54.92] um xpub xpriv or xpub
[323:01.48] which encoding to use hey what's up for god good to see you still here
[323:12.20] 24 hour stream i don't you know i the closest i've come i think has been 10 hours
[323:20.12] i think that's the longest i've ever done good call to improve consistency ecosystem wise
[323:27.56] yeah but i mean it's it's expensive though in terms of time the question is will it pay off
[323:32.36] and the other question is versus what other alternatives because i mean i'm not really in
[323:37.40] charge of making this decision i've been given the go-ahead i i don't think that either of us
[323:42.04] expected it was going to be going to take the time that it's taken but you know opportunity
[323:48.36] cost what else could we have been doing and would it have been any better with the budget that we
[323:52.52] have because we have a certain budget every month so if we don't spend that budget it accumulates
[323:57.96] in the savings awesome if we do spend that budget then we have some accountability to say hey here's
[324:03.88] what came out of it and so i'm hoping that this is i'm really hoping that this is going to be a big
[324:10.12] big win and that this is going to really get some some wind in our sails uh releasing some
[324:18.12] of this uh releasing this because there's i've been doing a lot of work and a lot of it's just
[324:23.24] been you know some people can kind of understand it but this is i'm hoping developer tools that
[324:30.84] that uh you know the the developers developers developers developers uh all right so
[324:41.96] let's see private pkh
[324:55.80] um
[325:09.16] there we go
[325:11.80] oops let's get rid of those
[325:25.80] it depends on
[325:38.52] only some
[325:39.32] which are valid depends on where they are used
[325:57.32] so
[326:06.28] okay
[326:14.84] so
[326:24.92] common conversions
[326:27.40] common encode decode options
[326:45.16] and then we're gonna have
[326:55.08] okay so
[327:12.60] i'm gonna say this two hex equals
[327:40.92] and two bytes i just want this to be the canonical way that this is used
[327:50.84] and hopefully this is going to look a bit a bit better
[328:09.40] oops what happened there something didn't go quite right
[328:14.04] oh this doesn't need to be there
[328:18.20] so i'm hoping this is going to look quite a bit better when it's actually on the readme
[328:23.32] but this is not just a repository this is a full tutorial it is uh it is a reference
[328:35.96] implementation as i've as i've dubbed it that you the idea is that you could port this
[328:40.68] to other places i might collapse that down um here we are
[328:48.36] yeah so that's that's how we're going to use those
[329:00.76] and then
[329:01.32] is this the right branch this is the right branch
[329:06.44] okay so we're going to get rid of these
[329:12.28] because we've already redefined all of this
[329:27.32] oh whoops no sorry that's the one that i did redefine so these are the ones that one we've
[329:33.64] moved that one we've kept that one we've moved that one we have moved almost all of
[329:40.44] these we've renamed or moved or changed in some way so they all need to go
[329:56.52] okay implementation details
[330:00.28] okay api
[330:14.28] however
[330:24.52] so it's always good to lead with something people don't expect
[330:37.48] dash keys doesn't do anything that other base 58 check libraries don't do okay
[330:44.60] that's a hook right wait why did you create it then it's simply a rewrite
[330:52.28] let's see the purpose
[330:55.40] of this rewrite
[330:59.80] has been to provide simpler more streamlined
[331:15.48] streamlined
[331:23.00] a simpler lightweight more streamlined
[331:37.00] reference implementation
[331:43.40] let's see production ready reference implementation that takes advantage of modern cross-platform
[331:51.96] lightweight
[331:55.32] all right
[332:04.04] okay so here's here's the kicker it does a better job of exposing a exposing
[332:20.92] um functions and exposing functions
[332:31.72] for for how the base 58 check codec is used in practice rather than everything
[332:42.84] it can theoretically be used for
[332:48.68] there we go
[332:58.12] so common conversions
[333:10.20] so
[333:16.36] let's put this here
[333:35.80] with address
[333:40.92] don't bury the lead this is what it does right here
[333:53.96] it gets you between with and addresses
[334:03.08] all right common conversions common encode decode options debugger encoder
[334:17.56] encoder
[334:18.20] note these all output either strings or
[334:32.44] either base 58 check strings
[334:42.52] or byte arrays
[334:49.96] so
[335:18.60] okay there's that then we have all the common encode decode options
[335:22.92] and then i need to put some of the output here of what this can look like
[335:42.44] okay decode output
[335:44.28] and this can look like type private version where it could be cc
[336:06.28] check actually go look at the check value here so this by the way i'm going to send you a link
[336:12.76] to this take a look at this i would love feedback on the glossary the glossary section is something
[336:18.84] that i created this for people who are not necessarily into this stuff that was my idea
[336:24.84] people that want to get into it but they're not necessarily into it not necessarily heavily
[336:28.84] invested into it uh there are there are at least two things that are highly technical
[336:34.52] but i make them as less least technical as possible i mean i could cut out the technical
[336:43.32] stuff but there's this balance right because if it's too shallow then you don't know what to go
[336:49.00] search for and you don't know how complex the problem is and if it's too deep then you can get
[336:53.96] completely lost and i hope that i struck the balance so each of these tools is going to have
[337:00.12] a glossary that is specific to just that set of tools so only the things in that glossary apply
[337:06.44] to this package nothing there's not extraneous vocabulary so if the vocabulary is not defined
[337:15.24] here it's not relevant to this package and if it is defined here it is relevant to this package
[337:21.08] perhaps even in a cursory way but the thing that's the most scary is going to be the public key and
[337:27.08] so this is this is actual code taken from the the the public key library i've modified it a little
[337:39.96] bit to make it a little bit easier to see rather than having to chase down 15 different functions
[337:47.00] or i don't think it's quite 15 but you know half a dozen to a dozen different functions
[337:51.72] where this is defined in one function and this is defined elsewhere and then this is defined
[337:58.12] somewhere else and this is defined somewhere else and this is defined somewhere else and this is
[338:02.04] defined somewhere you know instead of instead of if you wanted to this gives you the high level
[338:08.36] overview that curve square root mod is the thing that is very complicated all of the rest of this
[338:16.52] at least can be understood to some degree from this right here this is correct the the curve
[338:25.88] square root mod is the the piece that is the it is the complex algorithm it is the intense low
[338:35.64] level math that i don't really want to understand i want to understand me personally i'm kind of
[338:41.72] designing this for if i was to come across this stuff again today me personally this is helpful
[338:47.72] it's helpful to be able to say okay there is an x value and an a value and a b value you know
[338:58.20] to just just to have the nomenclature available to know this is what a public key is a public key is
[339:05.72] when you take some bytes some pub key bytes and you perform this operation so this is the most
[339:14.28] complex thing and this is the next most complex thing is describing a private key and i've tried
[339:19.88] to give what other names this thing goes by in this and other ecosystems as well as links to
[339:26.52] see more specifically what you know if you wanted to dive in deeper on this these are the two most
[339:34.76] complicated things this is where you'd go but for me this is helpful yeah so this is kind of the
[339:57.00] level that i wanted to see it at to understand what's going on so there's this whole thing called
[340:01.24] a jacobian point there's a jacobian multiply a jacobian affine all of this stuff very fancy
[340:09.32] i don't quite get it but it's enough that i can say okay it's some random numbers you check to
[340:17.88] see if it's on the curve you try to apply it to a public point and if you can get a public hex that's
[340:24.20] the private key so this this would be i don't know that this is going to be helpful to the average
[340:29.40] person i don't think the average person should know that much i think the average person should
[340:33.48] know this is what the average person needs to know that's that's my hope anyway okay
[340:53.56] let's understand once then it's boring it just works that's that's what we're hoping for
[340:58.52] fancy matrix talk
[341:00.60] yeah
[341:03.50] okay let's try a couple more things here glossary i'm actually going to try to bring this
[341:18.44] um let's see check
[341:20.04] i'm gonna leave that one out well let's
[341:29.24] compressed let's see how far we can go private key pubkey hash public key version with etc
[341:41.48] and i actually want to go
[341:47.96] glossary
[341:49.24] okay that is the right thing to do
[342:03.24] so i've already said
[342:18.04] "for developing" so i can just say "for testing" here that's good enough then i can collapse that down
[342:27.32] so
[342:35.80] okay so for each of these things that i've already defined i've got a lot of debug info here
[342:53.32] i've got a lot of code here
[342:54.84] gosh i hope this ends up being helpful i will literally be heartbroken as in it will hurt my
[343:06.12] heart if this is not a big win because i have i'm getting paid for the work so every hour that i
[343:16.60] get paid i'm getting paid for the work that i've accumulated but i will feel at such a tremendous
[343:23.00] loss if this doesn't have a significant impact on a few people
[343:29.88] works in command line node bun and browsers
[343:43.96] so
[343:55.16] so
[344:04.44] okay
[344:18.44] let's see node and bundlers is this just going to be node bundlers maybe
[344:38.52] browser maybe i should just back off here to install
[344:49.80] usage
[344:57.16] api
[345:06.20] license
[345:15.48] all right let's update the test here
[345:25.80] will this thing even work anymore oh and we also we need to update the test with the latest fixture
[345:34.44] data because one of the things that i did and part of the reason this took turns was because i was
[345:40.20] able i was very fortunate to uncover what i call the zoomonic which is this series of 12 words that
[345:48.76] happens to be a valid a valid private key seed zoo zoo zoo zoo zoo zoo zoo zoo zoo wrong and the
[345:57.48] checksum word is wrong so oh no updating tests yeah well i think i uh who knows i think we're in
[346:10.28] a good place here all right so check with is going to be here let me try to find the private hex
[346:21.00] and all this stuff has been renamed so that the test is very simple and the cli is more of a test
[346:27.08] than this is and then there's some other things that become more of a test because they've got
[346:31.40] actual tables and stuff but we've got dash keys so here's what we got we've got let two bytes equals
[346:39.32] dash keys first of all where's dash keys defined at dash keys okay so first of all let dash keys
[346:48.68] equal window dot dash keys then two bytes dash keys dot utils dot hex two bytes
[346:57.88] two hex dash keys utils bytes two hex all right so we got that
[347:07.24] then we've got here's our private hex and then we can go
[347:16.60] there's our private key i actually think that the
[347:19.48] private hex is probably better yeah there we go then we're going to have our check with
[347:25.32] and then we're doing now priv key to whiff so priv bytes
[347:35.32] so
[347:48.04] let's see
[347:51.32] all right and then we need to have our check address so there's our address
[348:03.40] nice fixture information anyway so across the entire ecosystem
[348:07.80] i'm i'm going to be using keys that are strictly from this this one set okay so whiff to adder
[348:15.88] that looks good
[348:24.52] all right so this is pretty simple
[348:26.12] oh let's see how bad it's broken
[348:37.16] well that's not what i expected
[348:52.36] it's just spinning
[348:58.44] okay whiff to private key is not a function that's awesome very simple
[349:13.24] so let me go ahead and let's take a look let's take a look at everything here
[349:30.52] where is this being used priv key encode x key pkh priv key to do pubkey
[349:41.00] priv key ah there we go there's another one where it's the old the old version so that was so long
[349:50.60] that it it seems like it there's too many words kind of getting in the way of being able to read
[349:55.08] what it is and that's why i decided to refactor it after refactoring it because after refactoring
[350:02.12] it to be clear i needed to refactor it to be more clear because if there's too many words you have
[350:09.80] to read and they're similar like public key pubkey hash etc etc and it's a long string of them it's
[350:16.92] just it's kind of difficult to understand all right so hallelujah hallelujah hallelujah hallelujah
[350:29.96] i don't have a good enough sound for this i don't i don't have a button i can press that can
[350:43.32] give the satisfaction uh we're just gonna go with but there's no sense crying over every mistake
[350:51.72] you just keep on trying until you run out of cake
[350:55.80] wait indentation
[351:01.32] where was the indentation not matching
[351:05.80] was that in the test indentation should be matching
[351:13.88] [Music]
[351:21.24] where where's where's the indentation not match
[351:23.88] yeah i i don't spend any time manually doing it ever since i discovered prettier a few years ago
[351:31.80] i i will i will write it and it'll be blah blah and then i'll just save and when i say it goes
[351:38.60] and then it's all good
[351:44.36] okay
[351:57.96] so we've got a few
[352:04.44] bits here so i'm gonna get rid of that pub.js proofpoint.js those are nothing
[352:10.28] pretty sure my fixtures.txt this is stuff that i don't need to worry about anymore
[352:15.40] all right examples.wiff-58examples this was all just stuff that was in the readme anyway
[352:33.64] uh let's see migrate this has happened so all of the information that i needed
[352:39.48] to know about this i already got so we don't need that note anymore
[352:43.96] tests i think this was just to get some of the pieces out we've already got that no worries
[352:52.60] okay so we've got very little to do so what i'm going to do
[353:00.60] is i'm first i'm going to go into the cli i'm going to go ahead and update
[353:05.32] what version we're relying here on it we're just going to bump both of these to 0.9
[353:09.00] i haven't published 0.9 yet but that's okay we're going to do a little a two-part publish here
[353:15.08] okay
[353:21.26] reference tools
[353:26.76] so
[353:54.04] all right so i need to go in here and i'm gonna have to change a bunch of stuff so i'm going to
[354:08.60] take what i was just working on i'm going to push it down in the dependency directory so that i
[354:13.56] don't have to do the whole publish cycle in order to test this out so i know the dash keys is going
[354:22.52] to be quite diffner okay so there's some things that we're not going to be able to do in the same
[354:32.36] way basically we still have to rely on this external base 58 check because for debugging
[354:41.24] we actually want to be able to allow things that don't pass validation and i need to add more
[354:50.52] validate options to to not validate things because right now i this pendulum swung towards
[354:59.56] too much validation and i'll have to relax it back later so for some of this we're still
[355:07.32] going to have to rely on this external base 58 check so package.json let me make sure that's
[355:17.00] referenced in the dependencies npm install actually let me let me do it this way real quick
[355:23.88] npm install save
[355:27.64] it's going to have to have secp256k1 yes it's also going to have to have base 58 check
[355:44.76] and yeah it's gonna have to have those dependencies
[355:52.20] and that reminds me actually i need to put in here
[356:06.44] npm install save secp256k1
[356:19.64] and then we have to have that as well okay and the reason for this which i need to make note of here
[356:34.52] um
[356:42.04] internal implementation details you can overwrite these functions this uh
[357:00.76] um
[357:03.08] was
[357:08.14] we felt it was important to not depend to not strictly depend on our chosen
[357:27.56] secp256k1 implementation
[357:33.16] that's why you have to install it as a dependency yourself
[357:45.48] okay
[357:57.08] you can overwrite these functions
[358:05.16] overwrite these functions to provide your own implementation
[358:13.48] so
[358:19.08] use these functions if as is or
[358:30.52] overwrite them
[358:34.52] with your own implementation
[358:41.88] whoops example
[358:47.48] you do not need to do this but you may if you wish it's really important
[359:06.68] let's go back to dash keys real quick generate this okay so i'm going to slim down what this is
[359:27.24] so
[359:31.88] okay so we want to be able to say you can replace this
[359:45.88] i'm just going to try to make this really simple
[359:52.04] okay privbytes privkey so two hex
[360:01.08] and then
[360:18.28] um okay encode
[360:23.88] privbytes
[360:30.60] oops version cc
[360:44.60] oh do i have a private key to whiff i think i do right privkey to whiff yes
[360:50.44] okay so then we could just implement this as
[360:54.04] privkey to whiff
[360:58.20] i'll leave it like this
[361:10.20] so
[361:19.80] and then i'm going to do the same thing for the public key
[361:29.72] very similar just show how to overwrite it and this is why we made it async it doesn't have to be
[361:37.56] we made it async so that it could be
[361:39.56] hey thanks appreciate it
[361:44.20] okay so
[361:51.16] to public key do kind of a similar thing in here
[362:00.76] yeah we're just gonna yep
[362:22.76] all righty basically you can just get rid of that
[362:29.08] there we go cool
[362:45.80] oh i think there's two internal implementation details section
[362:50.12] swappable um sec p 256 k1 utils there we go
[363:04.28] 256 k1 utils there we go
[363:08.44] use these functions as is or
[363:22.52] as is or
[363:26.76] so
[363:56.44] okay there so it's decoupled in case there's a security concern or a
[364:01.48] performance concern or something else it's decoupled that was the point of that
[364:05.32] okay
[364:13.10] now let's see here what was i gonna do dash keys let's just get the low hanging fruit
[364:24.60] so this is generate this is dash keys dot utils dot generate with non-hd
[364:32.76] with to adder that's great utils to bytes oh this was actually
[364:38.68] hex two bytes wait did we already do the two bytes bit okay hold on so we need to take this
[364:48.68] up top here um for anywhere that we want to use it so here's dash keys
[364:56.44] we need to be able to say two bytes is equal to hex to bytes
[365:06.28] two hex is equal to bytes to hex
[365:18.04] let me kind of bring this down and bring this up
[365:21.32] there we go two bytes
[365:41.00] fine
[365:41.50] so a lot actually changed here so this is now that is going to generate a whiff that's great
[365:51.48] i could have i could have had generate generate key non-hd could still add that
[366:00.12] so to public key so this is now it's going to be pub bytes we're going to try to be consistent
[366:09.72] so pub bytes and priv bytes is what we're now naming these things
[366:12.68] so adder oh this should be renamed to adder info
[366:21.16] or decoded
[366:25.88] maybe 50 i i think we should remove the adder because we don't know
[366:34.28] what type of thing this is we just know that we're going to decode it
[366:37.16] all right pub bytes priv bytes i probably should uh let's just go through here private key
[366:49.32] buff priv bytes
[366:53.96] what that was it i already replaced them all fine
[367:00.84] fine
[367:01.34] okay well
[367:08.84] and then this adder or whiff read adder or path i don't like the name adder or
[367:21.56] whiff as much as i like the other name i came up with which is b58 c string
[367:28.68] adder or whiff well i'm going to leave it adder or whiff because mostly that's what it is
[367:35.80] it's not 100 of the time but you know 99
[367:39.08] all right so to public key that is under utils this we can lift it up it's just two hex now
[367:50.92] it's just two hex now
[367:53.72] okay and now this is pub key to pkh
[368:07.16] and that's still just going to be two hex and this is going to be to public key
[368:16.44] and again let's just replace all dash keys dot utils dot two hex with just two hex
[368:22.44] really i replaced all that too already
[368:28.92] fine wait no there's this one right there
[368:42.52] oh whoops i had a five rather than a percent there we go yep yep yep yep yep yep yep
[368:52.76] and then same thing with two bytes but a lot of these
[368:57.40] now that it's more the ecosystem friendly thing we actually aren't going to need to do a lot of
[369:05.88] those conversions because those conversions are really only necessary when you they're necessary
[369:09.96] when you're developing on this stuff because when you're developing on this stuff you're going to
[369:13.56] be using test fixtures that have hex and you're going to be outputting to hex and you're going
[369:18.52] to be reading from hex because you're going to be reading from text files and json but when
[369:22.04] you're actually using this as someone who needs to use it not debug it you're not going to be
[369:27.40] outputting hex so it's it's wasted effort to just have everything being in hex when it doesn't need
[369:35.88] to be and so that's one of the things that's changed so this yeah so this is and then we call
[369:45.00] this shawripe bytes and this is shawripe bytes
[370:03.40] okay and if this is just a regular one then we can use what are we trying to do here
[370:08.76] pubkey to adder that's what we can do we can just go straight to address
[370:17.80] we don't need to go through the middleman anymore
[370:29.00] and okay this one we're doing it this way because we are decoding and debugging so
[370:34.04] we do want the intermediary values that was actually important here
[370:37.40] pubkey hash buff becomes shawripe bytes
[370:49.80] bytes for
[370:55.64] priv bytes
[371:01.64] but we're not going to do that okay so again we're back to super boring stuff my apologies
[371:09.56] if you do like this consider likes and follow if you want to
[371:12.20] and you can also join the discord if you want to
[371:15.08] but it's just down to pubkey to adder yep okay pubkey to pkh
[371:25.56] utils shaw256sum utils
[371:32.12] ripe md160sum
[371:34.12] and
[371:46.20] um
[371:47.40] okay and we're debugging because we're using that one tool because we actually
[372:08.04] want stuff to be able to be wrong
[372:12.36] so there's not too much to do here although i could replace all instances of dash keys
[372:19.56] ripe md hash with dash keys utils ripe md sum
[372:26.52] another thing is these hash functions are always designed as if you're going to be hashing large
[372:35.16] large bits of data but you hardly ever do that the only thing you do that with with is shaw256
[372:41.08] right and even in the browser you're not going to be doing that with large chunks of data so
[372:46.12] it's really weird they didn't think about the development use case when they were
[372:49.48] when they were creating these or they thought about the broad use case but not the shallow
[372:53.32] one because what you really want is a synchronous implementation of most of these these uh summing
[372:59.24] methods because the computational power that it takes to do the shaw sum on a short message
[373:04.84] that's you know less than a kilobyte it's going to take more overhead to do all of the async crap
[373:12.36] especially especially if it's going to go down into the into a syscall or something like that
[373:20.28] in a library that's a c library or or whatever a linked library and then calling the function
[373:26.68] on that so it has to copy the data over has to call the function on it it's really not a good
[373:33.48] way to go for the use case that you have in javascript it's it's a poor it's a poor design
[373:40.92] for the javascript use case okay
[373:57.96] more dash keys okay that's it is that really all we're doing we generate with
[374:03.32] uh let me see where else this b58c is being used because i have a feeling
[374:12.20] it's being used in places where we could do better
[374:20.04] so for example we could probably just do dash keys dot decode validate false
[374:29.64] and then that's that so we could where's raw decode at
[374:37.32] we just we just take this out we don't need it anymore
[374:40.92] so that's good where else is it being used
[374:50.92] okay any debug stuff we're going to leave alone
[374:59.96] okay dash decode and just get rid of that dash decode dash keys dot decode
[375:08.44] oh that's something i forgot to update in the readme
[375:27.56] i want to show there we go
[375:30.20] okay so we did not do this so this still needs private key
[375:36.92] this would be hex pub key hash that's going to be hex
[375:48.68] x prove it's going to be hex x pub it's going to be hex
[375:53.32] possible key types
[376:15.56] see the problem is if i set this to json5 then it's going to see it gets rid of all the
[376:20.04] sort of some of what i wanted there
[376:25.48] that's okay
[376:28.92] check matches
[376:36.28] so
[376:42.84] let me double check on how what can type be
[376:56.84] yeah it can only be one of these four things
[377:04.76] i think that's pretty much all that there is let me double check on that that's
[377:12.36] still important to get right okay base 58 check types private key
[377:17.96] or rather private parts check oh compressed
[377:29.88] type valid version type valid version check type valid version
[377:39.64] so pretty much all check type valid version check type valid version check type valid
[377:51.08] version and then compressed so that needs to be there
[378:10.20] so
[378:14.36] part of whiff
[378:28.36] whiff
[378:39.96] so
[378:45.64] we have four eight c
[379:02.68] so
[379:10.68] note
[379:13.08] keys are always compressed
[379:25.48] so
[379:33.32] is always
[379:52.44] only applies to private keys and is always
[379:57.64] true left in for compatibility with old with
[380:07.24] for compatibility but not used
[380:18.92] so
[380:23.96] okay good
[380:38.20] so
[380:45.96] all right well let's uh try a couple things out could not find module dash keys
[381:00.44] i know about that
[381:10.44] let's go ahead and move this over to
[381:16.20] all right now it should be able to find it just fine oh no bytes out for each is not a function
[381:26.44] so something did not return the right value it's okay we're gonna get through this it's gonna be
[381:34.60] fine no one's gonna be any of the wiser all right dash keys
[381:48.76] 97 pkh to adder i think this might actually be more likely
[381:54.92] pubkey to adder get payment address so let's take a look at this one and let's just walk it back
[382:05.32] so get payment address goes to what
[382:11.64] so
[382:19.64] all right it brings us here
[382:20.76] and then we decode by the way i just the command i ran i just had in my history i was just going to
[382:28.60] run the first command that was in my history and see how things went so decode
[382:39.00] i'm guessing that this is probably where it breaks
[382:43.56] all right so let's rerun it again
[382:57.56] all right looks like there's information in here so we've got a private key for example
[383:03.56] uh oh we've we failed much later so what was that 199
[383:08.04] so we've thrown it off by two i got back all right pub bytes two public key priv bytes let's just
[383:19.24] take a quick check and make sure two public key it still has a good return value it looks like it
[383:28.28] does okay what else two hex let's make sure that two hex has a good return value i'm very confident
[383:41.16] that it does otherwise i don't think anything could have worked but you know sometimes you
[383:45.48] forget to do your return bytes two hex it's got a return all right looking good so 199 let's take
[383:56.28] a look again on 199 what's happening pub key to adder pubbytes console.log debug pubbytes pubbytes
[384:09.80] all right pubbytes are going in that's great
[384:19.48] so and i'm pretty sure for each is a function on these it's not on a string but we're not passing
[384:27.32] in a string let's just double check on that pubbytes yeah two hex public key
[384:34.76] so i don't know if we're using that public key anymore
[384:39.72] my pubkey to adder so let's take a look in pubkey to adder on line 1149
[384:48.28] see what's going on there 1149
[384:53.72] okay pubkey to pkh pubkey to pkh i was expecting this to return us
[385:08.52] it's just console.log same thing here debug
[385:12.60] sha whoops sha ripebytes sha ripebytes
[385:21.72] i'm just gonna put a one here because we're now inside this thing i'm guessing what happened
[385:37.24] and i'm actually going to go look in this right now in the dash keys i'm guessing what
[385:40.92] happened is it's missing in a wait not missing in a wait there but you know where i bet it's
[385:45.64] missing in a wait i bet it's missing in a wait internally that's one thing where i just get
[385:53.72] so confused i bring this up almost every session because i have the same problem almost every time
[385:59.24] and i'm always confused as to how the type checker did not catch it
[386:05.64] so where is there let's see it's not a t and then there's dash keys
[386:14.68] i guess just equals dash keys dot something
[386:30.68] here it is right here boom that's it that's what i was missing
[386:49.24] let me make sure that i update the readme i think i think it's good actually all right here we are
[386:58.84] okay so we got a little further but we're still having the same problem
[387:02.68] probably because i didn't actually copy that version into here all right there we go that's it
[387:11.32] awesome so i'm gonna have a oops test.sh here debug log console dot nope okay good
[387:37.16] so
[387:39.40] burn the logs burn them all
[387:53.40] all right so let's see what all i've been doing here
[388:04.44] there's another one
[388:07.56] okay decode let me just open up my test file here
[388:18.60] so we're gonna have address we're gonna have like this we're gonna have the decode
[388:25.40] and uh this is kind of stupid i'm just looking for
[388:33.32] for it to just run
[388:55.16] whoops set dash e set dash u
[389:01.24] then sh okay so len is not defined
[389:08.60] in random bytes
[389:20.04] hmm
[389:29.08] oh let's see random bytes bytes length
[389:38.28] all right i'm going to go publish this real quick because i know exactly
[389:47.08] how that's going wrong so let me go get into there sec p 250 nope all right up to
[389:56.92] i'm kind of surprised that that didn't trigger before now
[390:15.32] whoa
[390:17.56] all right so
[390:31.56] okay fix
[390:35.00] uh typo
[390:44.76] i guess because in the places where i've used this i actually have not been generating the random keys
[390:51.48] that way recently okay so
[390:57.32] conversion that's right whoops
[391:11.96] npm version pre-release
[391:15.40] npm publish and let me go get this
[391:28.44] okay so now back over here was it over here
[391:38.60] so
[391:44.12] oh whoops
[391:49.32] all right and then we need to
[392:01.40] take that one down and then we also need to
[392:04.36] take the package json and then i can go back in the package here and i can add this back
[392:09.48] okay so let's run that test again cool and another place where 4-H is not a function
[392:27.00] dollars to donuts it's going to be the same problem so i bet it's right i bet this time
[392:33.72] rather than the library code it's probably right here 236 it's going to be a wait where's decode
[392:42.92] oh a little confused there i read that wrong somehow at decode dash keys 236 236
[392:54.76] 236 there is no decode here oh in the function decode
[393:01.56] await
[393:15.08] all right is this a similar one
[393:24.12] might be
[393:29.24] by the way feel free to ask questions and keep the conversation going
[393:34.20] all right 97 flights yeah but it's not going to be there that's not where our problem is
[393:44.92] our problem is that decode 244 244
[393:51.96] yep there's another another one with the await again await
[393:59.40] await again whoops
[394:11.00] all right again
[394:16.68] good
[394:23.02] okay
[394:27.82] 64 is not a valid length
[394:32.76] for an uncompressed private key oh and i think i know where this was
[394:40.28] uh i think i know where this was as well
[394:51.96] i think i'm just going to take that out maybe for now
[395:00.28] because it's basically i'm trying to exploit a bug
[395:05.80] and there's a bug and being able to exploit the bug
[395:07.80] 66 or 64 characters so the problem is this
[395:18.28] to do or no bite
[395:36.36] but i'll go ahead and fix it i mean it's simple enough as you can see
[395:40.12] just bump the version on this one
[395:43.32] fix check compression bites correctly
[396:04.44] okay so npm version
[396:08.04] patch npm git push tags
[396:17.24] oh i need to push the git tags for the other one as well
[396:24.04] oh whoops hold on
[396:30.84] okay i need to
[396:38.20] just create a pr for this so i can pull it back in
[396:42.84] fix
[396:52.28] bad compression byte check
[396:55.24] okay git checkout main git push
[397:03.16] what
[397:07.66] that's not right
[397:18.76] so
[397:30.04] so
[397:36.52] all right let me oh whoops this is on the wrong
[397:53.16] this is on the wrong thing sorry let me go back here i hate it when it does that to me
[398:00.36] i actually wanted to create a pull request on my own locally let me see if i can grab that
[398:06.76] again pull new hotfix i was going to say that's a lot of stuff that doesn't make sense
[398:10.92] all right so we're going to do
[398:15.96] fix check compression byte plus length correctly there we go
[398:27.32] so
[398:39.24] okay
[398:53.24] all right now we're going to publish to npm
[399:02.04] we need to go back on that set this one git push tags
[399:11.88] there we go
[399:18.36] all right that one already was updated okay so now we have to again we delete this
[399:26.76] that's okay right everybody's gonna live it's gonna be just fine
[399:30.52] push that one the latest
[399:36.20] push this one at the latest get this one at the latest everybody's at the latest everything
[399:43.80] everything's at the latest all the latest everybody calm down we're at the latest okay
[399:51.00] it's gonna be fine
[399:53.72] you can have your latest and eat it too
[399:58.20] of course of course
[400:11.08] okay
[400:11.58] that looks all good to me
[400:15.80] echo
[400:22.22] if this
[400:25.26] probably passed
[400:30.20] check output above for errors
[400:38.84] so because i've got set dash e
[400:45.32] oh it would error out rather than continue okay so let's do this again with the help
[400:59.40] so address generate inspect
[401:17.80] so we got we got one two three four
[401:29.72] other than the help in the version so i think we are only testing one two three
[401:34.44] so we need to test verify but verify is going to be redonkulous
[401:48.20] so
[401:54.12] so
[402:05.08] so
[402:11.08] i don't remember how to turn echo on and off
[402:26.68] that's i think that's windows um
[402:33.40] so
[402:39.88] cool that's it all right
[402:54.60] okay
[403:00.36] all right so start out with but not examples start out with
[403:15.24] samples start out with
[403:20.84] so sure ignore generated keys
[403:34.84] all right read me what needs to update about the readme
[403:39.08] do we need anything to update about the readme probably not i think the readme is good
[403:45.08] let's see what's different about the readme as is
[403:49.88] uh we had an api section we call it reference tools
[403:53.88] docs reference api and reference implementation
[404:14.20] so
[404:16.20] update for latest
[404:22.68] okay get diff package.json
[404:30.52] update package.json
[404:31.80] update package.json
[404:49.96] update uh depths and tests
[404:55.88] okay so let's do a little get rebase i dash dash root
[405:09.96] initial commit okay ignore generated
[405:16.20] update for latest let's put that right on in there
[405:22.76] okay cool
[405:30.60] so the only thing that we're missing is the package.json and we'll get to that in just a
[405:37.40] minute okay initial commit ref move cli to unrepo chore ignore generated docs oh yep that's all good
[405:45.64] that's all really good so we're gonna we're not gonna tag this one yet we're almost gonna tag it
[405:53.24] okay
[405:59.16] cli sub
[406:03.56] as far as i can tell
[406:09.16] hold on what did we put in the readme here
[406:13.16] okay oh there's one more thing that we need to update on in the readme
[406:30.04] and that is well these implementation details are probably fine right so i don't think the
[406:36.68] two hex and two two bytes has got a lot of value there let's see
[406:50.28] i think this is pretty good let's see
[407:01.72] so shah ripe
[407:15.72] bytes oh and a quick reminder in case you haven't seen this enough times every 10 minutes for the
[407:29.16] last seven hours like if you like because you get more of what you like or don't
[407:35.56] as you wish i'm not trying to tell you how to live your life
[407:40.92] just trying to help you have a better one
[407:45.24] maybe sometimes
[407:46.52] okay decode encode
[408:05.48] so
[408:10.12] address to pub key hash
[408:32.28] public no pub key hash to address
[408:45.32] with to private key
[409:00.20] so
[409:11.00] so we have with to public key public key to public key oops to pub key hash
[409:29.08] that's kind of everything right so these two are bi-directional
[409:32.44] this only goes in one direction this only goes in one direction
[409:51.64] we have an arrow that points both ways
[410:01.72] so
[410:08.52] come on give me the forward arrow seriously
[410:25.00] there we go
[410:32.44] there we are wait
[410:46.60] wait
[410:51.88] i'm a little bit confused by that let's uh
[411:00.04] okay there we go it figured it out it figured out the white space
[411:06.84] so
[411:15.32] there we go that's the way that that needs to be described actually
[411:34.12] so private key can go to public key public key can go to public key hash
[411:44.52] um
[411:46.52] all right let's go ahead and get rid of all of that stuff here we've got it
[411:58.68] and then i'm going to change this from -58 yeah no i'm gonna leave it -58 check
[412:08.92] so
[412:15.32] okay
[412:31.96] so
[412:42.76] so these are just simplified versions of what's already implemented
[412:57.00] so
[413:07.00] so
[413:15.64] all right this is it i think
[413:33.24] so
[413:37.96] uh let's see minor bug fixes
[413:51.96] so
[413:57.40] okay so we've got all this stuff
[414:11.40] i'm gonna see if there's any way to salvage any of these but i think there's probably not
[414:18.04] so
[414:27.40] well i think there is just in a sense of
[414:44.12] i'm going to take all of this stuff that's whip i'm going to reset it first first i'm going to
[414:49.64] push it up then i'm going to reset it and then i'm going to just separate the doc changes from
[414:55.40] the the code changes and we can have this chore update tests you know that's fine
[415:06.20] this one about the cli goes here not a problem doc updates await yeah all this stuff
[415:15.24] there we go
[415:25.24] and then if i look at this
[415:33.88] what okay good i was gonna say that's uh a little bit different than what i expected
[415:39.56] should be able to move update test there that's not a problem okay so now
[415:46.36] i'm gonna do let's check what we've got here it's just some to do
[415:50.76] okay that's still a to-do item and then an example which i don't really care about
[415:56.76] and then i guess i could just delete the example since i don't
[416:00.44] really care about it or get at it whatever
[416:05.40] okay it's good to have it by that that name too i guess anyway so here we are
[416:18.36] and i'm going to do let me go ahead and force push that there we go
[416:25.32] now we need to be careful so rebase reset head tilde one
[416:31.16] oh whoops
[416:36.84] good thing i
[416:42.52] get reset i i did that by accident i didn't realize that was a command
[416:53.40] head tilde what let's first check and make sure everything's here yeah
[416:57.48] so i pulled stuff down and i'm saying
[417:05.48] yeah
[417:07.48] i'm just gonna
[417:22.28] uh
[417:23.56] is there such drastic changes it doesn't even matter
[417:37.56] i'm just gonna replay that okay that worked good
[417:50.84] i'm gonna replay this
[417:52.36] maybe
[417:58.36] um okay so this is actually a complete refactor so i could just reword that one
[418:19.64] and then we could fold that in there i think this will work
[418:23.48] complete refactor
[418:30.44] for
[418:36.76] i don't call us
[418:44.76] just uh full full throttle
[418:57.80] refactor
[419:04.84] okay here we go so now we are ready to
[419:13.40] do
[419:13.90] update the version
[419:21.48] okay i do want to actually update this that's one thing we want to do
[419:40.36] npm install dash dash save
[419:43.24] latest of that
[419:47.40] oh and actually we're not going to make that a dependency
[419:52.44] that just goes into the documentation so this is
[420:01.32] 1.7 so this would just go into the readme
[420:07.08] at one and what are we calling this
[420:14.12] we're not calling it anything yet
[420:18.12] okay i'm i'm comfortable doing this we can definitely call it a dev dependency
[420:34.28] okay so
[420:40.20] docs shore kit add
[420:54.20] shore update version
[421:02.36] update deps well actually
[421:30.20] okay so
[421:34.12] all right one last look at this we added types
[421:50.36] we included base x updated the license we switched a bunch of stuff
[421:57.64] the full throttle refactor we revamped everything
[422:02.28] all right let's just make sure there weren't any stray oh i actually have triple shifts
[422:11.16] so triple shifts in javascript are to keep something from becoming a possibly negative
[422:15.80] integer to keep it a 32-bit integer rather than a 31-bit positive integer
[422:21.72] okay well with that npm version
[422:29.00] minor
[422:34.20] and then git push tags blah blah blah blah blah blah
[422:41.24] so
[422:43.64] all right that's it
[422:55.88] i'm too hungry to give a really big hurrah on this but
[423:03.56] npm install
[423:07.64] so
[423:14.04] shore update dep
[423:36.52] i guess that's not quite fair whoops
[423:38.92] it should be
[423:45.80] there we go
[423:52.92] okay so with that npm version minor git push tags da da da da da da da
[424:13.80] oops
[424:17.08] update sub module
[424:45.88] okay
[424:47.88] that was grueling grueling work
[425:01.88] one last change i want to make
[425:13.64] i'm going to make all of these sections top level headers
[425:17.56] because there just needs to be more everything
[425:22.84] great
[425:27.82] usage
[425:34.28] api there just needs to be more more distance between things
[425:41.80] because there's a lot of stuff going on here
[425:52.12] so
[425:56.28] so
[426:04.28] so
[426:33.24] all right so we got the license section still good there implementation details
[426:39.32] kind of going to bring that out into its own section and then the fixtures
[426:47.64] okay
[426:58.52] update adder style npm version patch
[427:05.48] git push tags blah blah blah blah blah blah blah
[427:11.64] git checkout main git rebase
[427:21.08] to v1 and beyond
[427:27.32] what
[427:29.48] okay so first of all
[427:55.80] i'm going to close this out with included in number 10
[428:05.96] and then i'm going to go ahead and change the branch protections on this
[428:15.16] because we don't have enough people to actually require approvals
[428:24.20] where's my usb key
[428:25.48] get ye in here
[428:29.56] there we go
[428:34.76] all right
[428:42.36] so
[428:48.52] okay let's see
[428:58.28] uh via number 10
[429:05.56] um
[429:07.48] okay that's just a note port issues to bun at jojo byte will you test
[429:26.68] um test this
[429:33.08] well let's see here let me try the cli here let's just do webby bun get the latest bun
[429:39.48] oh there's a new release of bun check that out
[429:43.08] and then we can do bin dash keys
[429:48.92] generate
[429:53.24] all right bin dash keys
[429:58.44] so
[430:06.12] all right bin dash keys
[430:20.12] say address
[430:23.32] let's try one that's pretty sterile
[430:27.24] there we go this one's pretty sterile
[430:32.68] icing function resume
[430:38.68] still crashing
[430:52.68] crashing
[431:04.52] so
[431:16.36] okay i am tired i am hungry
[431:31.32] i'm really excited that this is done and i mean this this this is a hallmark achievement
[431:38.36] let's see glossary stuff fixture stuff implementation details
[431:59.56] so
[432:26.68] all right okay there's one last test that i should make
[432:29.32] but i'm not ready to do it and that last test is i should send some money to a key
[432:37.40] possibly this one i'm actually interested to see what's what's the it's possible no one's ever used
[432:45.00] this but i i i don't know am i the look at that i'm the first person i'm the first person to ever
[432:51.40] consider using the simplest text fixture key or or i generated it incorrectly oops let's see here
[433:01.56] so do we have another tool that i can use to quickly convert this
[433:12.68] see dash private key to pub key hash
[433:19.32] online seems like somebody should want to do this you know get a bunch of people's private keys
[433:33.48] all right so maybe i should just try with the previous version of the tool
[433:39.56] global
[433:40.06] dash keys
[433:45.16] um location equals global
[433:51.56] no i i'm not talking right now and then
[433:59.48] dash keys at
[434:02.92] what is this going to do
[434:08.76] dash keys at 0.3 or something
[434:11.64] okay address
[434:27.32] let's do unsafe
[434:37.48] xrz is that what we got here xrz ends in c9 ends in c9 good whew makes my heart feel better all right
[434:47.00] i don't know uh give me a chance to wake up sweetheart i'm i'm tired now
[435:02.44] caffeinated lemon water only gets you so far all right what a thrill
[435:10.04] dash keys install
[435:19.96] dash key cli
[435:24.52] okay i'm getting i'm getting off i'm getting off i'm sorry we can't raid
[435:31.24] thanks everybody for joining in it was wonderful hope to see you again
[435:35.24] have a great time likes up follow if you want to i am out like a light
[435:39.88] adios