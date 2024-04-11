---
showLink: "https://www.youtube.com/watch?v=3RrbgIkQXxY"
slug: "state-of-dashmate"
title: "The State of Dashmate"
publishDate: "2023-03-13"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/3RrbgIkQXxY/maxresdefault.webp"
---

Dashmate is a command-line tool that simplifies setting up Dash masternodes, full nodes, and local networks for development.

## Episode Summary

tl;dr: Dashmate is a Node.js NPM package that uses Docker and Docker Compose to simplify the process of setting up and managing Dash masternodes, full nodes, and local development networks. The tool, originally created by Dash Core Group (DCG), is now being developed by the Dash Incubator with input from DCG. In this episode, Dash Incubator strategist Tim introduces Dashmate, and developer Mikhail demonstrates how to set up a mainnet masternode, create a local development network, and interact with it using the Dash SDK.

## Chapters

00:00 - Introduction and Overview of Dashmate
The episode begins with an introduction to Dashmate, a command-line tool for managing Dash masternodes and local development networks.

03:44 - Tim's Background and Involvement with Dash Incubator
Tim discusses his background in data analytics and product management, and how he became involved with the Dash Incubator through a mutual friend.

10:28 - Dashmate's Purpose and Development
Tim explains that Dashmate is designed to simplify the process of setting up masternodes and local development networks, with the Dash Incubator taking over development from DCG.

16:15 - Mikhail's Demo: Setting Up a Mainnet Masternode
Dash Incubator developer Mikhail demonstrates how to set up a mainnet masternode using Dashmate, including installation, configuration, and checking the node's status.

21:37 - Mikhail's Demo: Configuring a Local Development Network
Mikhail shows how to configure a local development network using Dashmate, create a sample application, and interact with the network using the Dash SDK.

## Transcript

[00:00] (upbeat music) - No one spoke about after the repo markets
[00:10] that one of the first things that happened in March, 2020 and post that
[00:14] was the huge trillion dollar transfers the Fed did to all the major primary dealers,
[00:19] including European bulge brands, such as Credit Suisse. And those ran into trillions.
[00:25] And I wonder why media has also thrown a blanket over that because that was, by definition,
[00:31] a bigger bank bailout than the subprime narrative. - People who trade cryptocurrencies
[00:41] often want to use dollars to buy crypto or they want to sell crypto and receive dollars.
[00:47] And the dollar side of those transactions is where things get bogged down.
[00:51] If you're transferring large sums of money to buy crypto, you need to deal with the US banking system,
[00:57] who might ask you a lot of questions relating to anti-money laundering regulations.
[01:03] Crypto people hate questions like this. Similarly, if you just sold some crypto
[01:09] and want to deposit the dollars you received, most banks will have a long list of questions
[01:15] about the source of your funds. And there's a really good chance
[01:19] that they'll simply refuse to do the transaction. - Every single week,
[01:26] we've been following the number of states with rising unemployment claims.
[01:31] That's it. - Yeah. - Very simple.
[01:33] We've now crossed to Rubicon. A majority of states have, year over year,
[01:38] rising state initial jobless claims date on a week over week basis.
[01:43] And guess what? They're the biggest states in the nation.
[01:48] 73.88% of the US population is living in states rising unemployment.
[01:56] I haven't even published this. It's being published in the morning.
[01:59] 73.88% of the US population is living in a state where the number of people collecting
[02:05] unemployment insurance is rising year over year. - Put simply, Silvergate's upcoming stablecoin
[02:14] may have been seen as a competitor to the Fed's own upcoming payment system.
[02:20] Unlike private stablecoins from commercial banks and regular stablecoins,
[02:24] Silvergate's stablecoin would see rapid retail adoption because of the Sen and its Wall Street backing.
[02:31] The Fed saw this and said, "Hell no." They do not want Wall Street involved
[02:37] in issuing a de facto digital dollar, and they certainly don't want crypto
[02:42] to be a part of it either. The US government wants to maintain
[02:46] total control of its currency, and that is fundamentally why
[02:50] it's fighting the crypto industry right now. (gentle music)
[02:56] - I feel like I'm living in a psy-op world because I can see things are turning down,
[03:00] and I'm sitting as a YouTuber, someone who's just monitoring news flow
[03:05] of a country far away. Imagine how the people closing their businesses feel.
[03:09] They don't see J-PAL's booming labor market. - This is one of the best orchestrated
[03:16] propaganda campaigns I've ever seen. There's a lot of potential
[03:22] for social unrest going on right now. - It feels like a plan.
[03:26] It does feel like a plan. It does feel like this is the big one.
[03:30] It does feel like the launching pad for the UBI and the Central Bank digital tokens
[03:34] as a result of solution to the problems we're about to encounter.
[03:38] (gentle music) (gentle music)
[03:44] - Hello, hello. Welcome to Incubator Weekly once again.
[03:54] Today, I'm joined by my co-host as usual, Rion. How are you today, Rion?
[03:59] - Doing great, thanks. - Great, I am as well, and I'm Amanda.
[04:03] Today is something a little bit different than what we've done so far, I would say,
[04:10] which is that we have a serious, what looks like, I mean, I know it's not technically command line,
[04:18] but it almost looks like command line, the demo, right, Rion?
[04:22] - Oh, it's command line. - Oh, shoot, it is command line.
[04:25] Okay, well, we are talking today about an administrative tool
[04:29] for the Dash network called DashMate. And do I hear correctly that it used to be called DashMAN,
[04:34] or did I dream that? - No, DashMAN was something different,
[04:39] but served kind of the same purpose. This tool used to be called MN,
[04:45] just like Masternode something, and the abbreviation on the command line was MN,
[04:51] but they then changed it to DashMate to kind of signify that it serves the same purpose
[04:58] as DashMAN used to serve. That DashMAN was built by MuCowMu, I think,
[05:04] and DashMate was built by DCG, Dash Core Group,
[05:11] and we're just helping out with that right now. So that's why we're featuring it on the incubator.
[05:17] - Got it. Well, there is a particular strategist
[05:20] in charge of incubators development of DashMate, and his name is Tim, aka SpectaProd.
[05:28] So let us go to a prerecorded segment with Tim to learn more about DashMate.
[05:35] Tim, SpectaProd. Am I saying SpectaProd right, by the way?
[05:39] - Yeah, you are. You are saying it correctly,
[05:41] although there's not really any kind of an official pronunciation.
[05:45] - No, it's not in the dictionary or encyclopedia? - No.
[05:50] No, my favorite is that I've had several friends over the years say that it sounds like a James Bond villain.
[05:55] - Let's go with that. Good.
[06:00] You are the third strategist, third and final, that we have met here on Incubator Weekly.
[06:07] And my first question to you is, how did you hear of Dash at all?
[06:13] - So my first introduction to Dash was probably 2017, 2018, as I initially began to dabble in crypto.
[06:27] And it was one of... It wasn't anything specific that brought it to my attention.
[06:35] It was more just looking to see what coins were out there. And I had a lot of interest in the altcoin space,
[06:44] and largely because just the price of Bitcoin was so high for my own personal finances.
[06:50] So the altcoins were more interesting 'cause they felt more accessible
[06:54] because I hadn't really grappled with the idea that it was infinitely divisible.
[07:00] And so you didn't need to buy a full Bitcoin. - Yeah, interesting.
[07:06] And then, so how then did you move from, "Hey, this particular altcoin Dash is of interest to me,"
[07:12] to, "The Incubator, I want to work there." - So that is, those two stories
[07:19] actually have nothing to do with each other. That has everything to do with,
[07:24] I was involved in the local community theater, and through a series of connections,
[07:31] one of the other actors that I was performing with was good friends with Rion
[07:37] and thought that we would make good friends. And then, of course, with Rion,
[07:43] if you spend any time with Rion, then cryptocurrency is always going to come up,
[07:50] and blockchain technology is always going to be a part of the conversation.
[07:54] And lo and behold, I knew just enough about the technology and about the goings-on to be interested
[08:01] not in just what he was saying, but then also interested in why he was saying it
[08:06] and what his story was. And so then it went from there.
[08:11] So that acquaintanceship and that small, nascent friendship was turned into joining The Incubator,
[08:21] a lot of it just out of curiosity. - Ah, the theater.
[08:25] What a fortunate connection there. Tell us then what is or was your professional background
[08:32] prior to the blockchainery? - Yeah, so I have been in data for a long time.
[08:40] It started out as marketing and website analytics, and then I worked in companies
[08:47] that were using the data for their own stuff and then that turned into consulting.
[08:53] And that has grown more into a broader perspective and a broader desire to get into more data.
[09:00] And that was actually one of the first things that I had, one of the first curiosities I had around The Incubator
[09:05] and around Dash was, this is a whole new data set, and what kinds of things can we do and learn
[09:11] from this data set? And this was the way to get a foot in the door
[09:18] to figure that out. Since then, my interest has been less about the data
[09:22] and the data set, just in that is largely a function of,
[09:26] I don't possess the technical coding skills to be able to access it the way that I would like to,
[09:33] and has turned more into another thing that I've always wanted to get towards
[09:37] is product development and product management. I've always thought that that would be,
[09:42] if I didn't do data and I wasn't a consultant in that, that I would get into product management
[09:47] and product development. So I've been able to use The Incubator for that,
[09:52] for actually learning about product management more so, but some product development also.
[10:00] A lot of what we're doing is a combination of, or as a strategist, a lot of what we're doing
[10:05] is a combination of project management and product management,
[10:08] and learning how to effectively steer projects and how to effectively manage the workflow of a project
[10:17] and evangelize projects and those kinds of skill sets that I hadn't really had an opportunity to develop
[10:24] and that I'm getting an opportunity to develop here. - Got it.
[10:28] So speaking of projects/products, today's topic is the piece of software called Dashmate.
[10:36] Generally, what is Dashmate? What does it do?
[10:40] - Dashmate is designed to make it easy, or at least easier, to set up a masternode,
[10:47] which is a critical part of the infrastructure for the Dash blockchain.
[10:52] - Got it. And so then I also understand that,
[10:57] and maybe this is when it was called Dash Man, that this software originally came from DCG
[11:03] and now has Incubator just totally taken over the responsibilities,
[11:08] or are they shared responsibilities, or what has happened there?
[11:12] - It's, so the current development is Incubator-run. - Okay.
[11:19] - The priority list is heavily informed by DCG, and in fact, a lot of the, not just the priorities,
[11:26] but a lot of the issues that are floated to the top are issues that DCG has been aware of
[11:31] and has specifically requested that the developer tackle and take on.
[11:39] So they've been essential in setting the priorities and for setting the trajectory of the product,
[11:46] and then really handed off the development responsibility to the Incubator.
[11:52] - I got it. Okay, so then, speaking of these developments,
[11:57] Dash developer at the Incubator, Mikhail, is going to give us a demo of what he has done
[12:02] on Dashmate here in just a bit. Can you tell us sort of what we can expect
[12:08] from that demo broadly? - A lot, so there's, one of the issues with Dashmate
[12:14] is that it was a legacy piece of software, essentially. There was a lot of tech,
[12:17] there was a lot of tech debt involved. There was a lot of, there were a lot of bugs
[12:23] that had arrived through various means, some of it just being old,
[12:27] some of it being progress that has happened to the protocol, and a lot of what he's done
[12:32] is to consolidate and pull pieces together so that it's actually easier to use.
[12:38] It used to be, even though it simplifies the process of setting up a master node,
[12:43] it's still a lot of command line understanding you need to have, and he has done quite a bit of work
[12:50] to streamline those processes and to unify technologies in the background
[12:55] and to make it more functional and more easily used for the existing master node operators
[13:02] and for anybody that would wanna be a new master node operator.
[13:05] - Got it. All right, well, I think that sets us up
[13:08] for what we wanted and needed to know before we get onto the demo later.
[13:13] So thanks for joining us today, and we'll look forward to, if not before,
[13:18] we look forward to speaking to you again in the Incubator's quarterly call,
[13:25] which will be coming up within about a month, and we look forward to hearing more
[13:29] about what you have going on. - Thanks, Amanda, I appreciate it.
[13:32] I'm looking forward to it too. - Well, all right then.
[13:38] So Rion, is this, I had one of these questions, I didn't ask Tim, and I wanted to ask you,
[13:44] is this one of those tools where we have any idea of its usage?
[13:50] Like, is anybody, like, is it Incubator and GCG only, or are other companies using it?
[13:57] - I don't know about companies, but I would assume that there definitely are
[14:01] other developers, even outside of the Incubator, that are using it.
[14:05] I've just seen that in Discord, that people are using it and whatnot,
[14:10] but I don't know what the extent is. But one thing to add to what Tim was saying is,
[14:16] this is not just to set up master nodes, it's also to set up normal full nodes.
[14:22] It's funny that we call them full nodes, 'cause, like, a master node is more full
[14:27] than the full node, but yeah, it sets up full nodes, and it's also recently been updated
[14:35] to set up networks. So instead of just setting up a node on the network,
[14:42] it can set up an actual network so that you can do local development
[14:46] without relying on test net. And it also, a big part of it is, like, the configuration.
[14:53] So setting up, like, telling your node which network you're connecting to.
[15:01] Also, I'm not quite sure if it's setting up miner, I think it's setting up miners along with that as well,
[15:11] as part of the network. So anything that you need in order to develop on Dash,
[15:17] it's supposed to set up that infrastructure. - Well, that does sound broad.
[15:22] Is there anything else before we get to the first segment of the demo, Rion?
[15:27] - I think let's just get to the demo, and then we'll talk about it after, yeah.
[15:33] - Okay. So you are about to see Mikhail,
[15:37] who is the Dash dev taking the lead on the developments that we have discussed so far.
[15:42] - From the incubator side. - Pardon?
[15:45] - From the incubator side. There's still a lot of work, I think,
[15:47] that's, I don't know, actually, about a lot of work, but this is still a DCG product,
[15:52] so I don't want anything that we say to be construed as, like, you know,
[15:58] this is Dash Incubator's product, or anything like that. Still very much DCG's product, we're just helping out here.
[16:05] But yeah, Shenmik, or Mikhail, he is the one that's really taking the lead
[16:11] from the incubator side. - Thanks for that clarification.
[16:15] Let's have a look. - Hi, my name is Mikhail,
[16:17] and I'm the Dashmate Incubator Developer. You may know me by the nickname Shenmik
[16:22] in the Dash Dev Discord. I'm happy to appear on this Dash Incubator Weekly,
[16:27] and today I will show you the software called Dashmate, which helps you running master nodes
[16:33] and creating local private Dash platform networks. This is experimental, but very useful tool
[16:40] that primarily designed for master node operators and also blockchain developers.
[16:47] Dashmate is a Node.js NPM package, and it uses Docker and Docker Compose to run all the things.
[16:53] So basically, Dashmate is a wrapper around Docker Compose. Instead of messing around
[16:59] with a lot of different configurations, different startup scripts,
[17:04] it uses one common JSON config and re-renders everything on each run.
[17:11] Developers will also find this tool very useful because it allows you to create
[17:17] private local networks of Dash platform, and you can use any Dash platform features.
[17:24] It works similarly like Ganache in Ethereum. You can just create a private test network
[17:31] and connect to it with your SDK. So let me show you a few examples.
[17:36] I will show you how to deploy a main net node and check its status,
[17:40] and how to configure a local network and register an identity there.
[17:45] Here we have the AWS Fresh EC2 instance with Ubuntu 22.04,
[17:51] and I'm going to install the Dashmate on it. I'm using the automatic installation script
[17:57] from the Docker website, and it just grabs all the packages,
[18:02] all the certificates to obtain it, and just installs the Docker on your computer.
[18:07] I also adding my user to the group Docker to allow using the Docker commands
[18:16] on my current user without getting the root permissions. The next step, I am using the NVM installation script
[18:27] and installing the NVM. NVM allows you to quickly change versions of your Node.js,
[18:33] and you can quickly switch between Node.js or LTS or whatever you want.
[18:39] The next step is install the Dashmate on your computer. You can install it via npm manager
[18:47] and install globally on your computer. So cool, it's there.
[18:54] So the next step would be the setup, because in order to run your Node,
[19:00] you have to set up it first. For this, you can use the Dashmate setup command.
[19:07] You can choose wherever you want to set up. In this case, we choose main net
[19:12] because we want to deploy main net Node and selecting master Node, Node type.
[19:18] And it asks for the public IP address. I just verify that it is correct.
[19:24] It is correctly detected. If not, you can manually type in it here.
[19:31] I'm also providing the BLS private key. I guess you already have it.
[19:37] If you already have the master Node. If not, you have to register your master Node
[19:43] and type it in here. At this point, I just submit the generated one.
[19:50] That should be fine for the testing because I don't have master Node in main net.
[19:54] The setup went successfully. Everything is green.
[19:58] At this point, I will try to run my master Node. Seems like it started.
[20:05] Let's check it. To check, you can execute the Dashmate status command.
[20:11] We can see that it is currently not in chain and it's syncing and waiting for the protex
[20:21] appearing chain. When you have the protex
[20:24] and actually the registration of your master Node, if the BLS private key is correct,
[20:30] it will pick up everything and your master Node will turn into ready status.
[20:36] - Dang, I got a little ASMR from that. Not sure anybody knows what that is,
[20:42] but if you do, maybe you'd agree. Relaxing.
[20:46] All I mean to say is I found it relaxing. Did you find it anything other
[20:50] or in addition to relaxing, Rion? - Well, when I saw he was doing main net stuff there,
[20:56] I hadn't looked at this demo yet. So hopefully none of that was a main net BLS keys
[21:02] that are compromised at this point. But I guess if it is.
[21:07] - Well, he said he didn't have a real master Node, so that couldn't be an issue, right?
[21:12] - Yeah, I wasn't paying 100% attention. I just noticed main net and then, whoa, okay.
[21:18] Hopefully there's nothing private there. Probably not.
[21:22] - Good. Okay, well, the second half of Mikhail's demo
[21:27] goes into configuring a local network. So shall we have a look at that now?
[21:34] - Yeah. - Okay.
[21:37] Here we go. - I showed you how to deploy a main net Node,
[21:40] but what about local networks? I will show you how to configure one.
[21:45] You can use the same Dashmate setup commands. Just choose the local mode from the menu.
[21:53] Just accept everything and just wait for it to come up. It is configuring some stuff like tender dash,
[22:04] the master Node, the seed Nodes, the drive, DAPI and so on.
[22:10] After we configure everything, we'll be able to start. We can see that it's successfully finished.
[22:17] We can try to start it. Use Dashmate group start command to do that.
[22:24] It will try to start everything. We should wait a little bit.
[22:32] But then it successfully ended up. Let's check if it's running
[22:37] by typing Dashmate group status command. Cool, we can see that it is green.
[22:44] You can additionally check this by typing docker ps command and ensuring that every container is up
[22:52] and nothing is crashing. Cool, we can see that it is okay.
[22:59] So let's try to maybe create a sample application and test it.
[23:04] What I'm going to do is create a sample application that will connect to our Dashmate local node
[23:11] and hopefully just print out the address. Just the test address that we can populate with some dash.
[23:19] To do that, I just create a new NPM project, install the dash SDK and create a sample file
[23:28] that I will execute via Node.js. So I have already prepared some code.
[23:39] This code is from examples in platform Monorepo. You can check it out.
[23:45] I just modified the network to local and added my seed node, my DAPI node actually,
[23:53] where SDK will connect to. By default, SDK will connect to main net.
[24:00] Typing in everything. Also, I will create, I will request a new address,
[24:10] the new unused address that is fresh and clean from our wallet and just print out it via console.
[24:19] Cool, let's try to run it, right? Nice, it's successfully connected and here is our address.
[24:33] We can use this address to request test dashes that we can request via Dashmate.
[24:40] To do that, we have to stop our network because minting dashes require a local network to be stopped.
[24:47] We first stop our network and then use Dashmate wallet mint command
[24:53] for issuing new dashes. Okay, let's try to use the wallet mint command.
[24:58] I have to pass the address that I took from the previous step and type local seed config
[25:05] to this command because it will initialize the dashes on the local seed node.
[25:14] Okay, cool, it's all green and said that it has generated some address.
[25:20] Let's check that. Let's start our network
[25:25] and modify our script a little bit. Let's add some balance checking
[25:32] in our Node.js script sample application. Let's use get total balance.
[25:43] Cool, we can see that we actually received our test dash and our unused address have changed.
[25:53] That means that we have successfully received our test dash.
[25:57] So what we are going to try now is register an identity. Let's modify our script a little bit.
[26:07] So let's just clear out the address and let's use the method from the SDK,
[26:16] which comes from the client, client.platform.identity.register.
[26:22] And let's log it out with a get ID method. If we run it,
[26:31] it is successfully registered an identity and we can see the ID of its identity.
[26:40] With this ID, you can do whatever you want. You can fetch identity,
[26:45] you can use it in your contracts or something like that. Okay, I just show you how to work with Dash Minute
[26:50] and I hope you liked it. There are a lot of stuff coming in for the Dash Minute
[26:54] in the future releases, like HPMN, HPMN registering support,
[26:59] Dash Minute HTTP, RPC, API, that will allow to build UI on top of the Dash Minute.
[27:06] Actually a lot of stuff. Thanks for watching and don't forget to like it.
[27:13] See you. - Oh, dang.
[27:17] I didn't even ask him to remind people to give the video a like.
[27:22] Let's keep him around. - I wish I would have watched the full demo
[27:30] through to the end 'cause I would have stricken the HPMN text.
[27:37] I would have censored that for sure. That's kind of an inside joke,
[27:41] but I don't like that term for high performance masternode. I think all of our masternodes on the network
[27:47] are just as high performance as the upcoming 4,000 Dash collateralized nodes,
[27:53] but it's good to hear either way that the Dashmate will be making that setup simple as well.
[28:00] - Yeah, it certainly seems like a multi-application tool. Quite a lot going on there, so.
[28:10] - Definitely a lot going on there and that's actually one of the reasons
[28:16] why I wanted to do this this week because there is so much going on with this tool.
[28:22] We definitely need testers for this and if there's not already a task for testing,
[28:30] then there should be and there will be and if you are interested in doing some testing
[28:35] with this tool, contact Tim Spectaprod on Discord or on Trello
[28:43] and he'll get you set up with that. This is a tool that's been a long time in the making.
[28:50] I've tested it myself over the years and it's sad to say over the years,
[28:56] but that's just the reality of it. But one of the things I don't,
[29:00] hopefully people noticed that in that last demo, that was demonstrating that you can set up a local network.
[29:09] So we've had a lot of trouble with instability of Testnet recently
[29:15] and that this tool allows you to kind of circumvent that. So if you wanna develop your application,
[29:23] you don't have to wait for Testnet to be stable. You can use this to set up a local network
[29:30] and mock the functionality that will exist on Testnet and on Mainnet later, but just using your local network,
[29:38] which is probably how you should be developing even when Testnet is up and online
[29:44] because it's just faster that way. Or, I don't know, I shouldn't say that
[29:49] as a blanket statement, but it's definitely an option even when Testnet is up.
[29:53] - Good call. All right, well, that is what we have for you this week.
[29:59] So again, if you are interested to claim a incubator bounty to test the tool that you have just seen,
[30:08] reach out to Tim as we have his contact information on the screen now.
[30:14] And absent that, we're going to, oh my stars. This is amazing.
[30:19] Mikhail's gonna join us to say goodbye to everyone. (Mikhail laughing)
[30:23] Mikhail. - Hey, good to see you as well.
[30:28] - You're here just in time to say goodbye to everyone and give them a righteous peace sign.
[30:32] Thanks for coming. - Goodbye everyone.
[30:35] - As he calls us from a moving vehicle. Excellent.
[30:39] All right, thanks for joining us this week, everyone. We look forward to seeing you again next week.
[30:43] Same place, same time. - See ya.
[30:45] - Bye. - Bye.