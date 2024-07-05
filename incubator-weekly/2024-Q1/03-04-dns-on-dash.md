---
showLink: "https://www.youtube.com/watch?v=Rrrv51XmPcI"
slug: "dns-on-dash"
title: "2nd Discussion Domains/DNS on Dash"
publishDate: "2024-03-04"
playlist: "Incubator Weekly"
coverImage: "https://i.ytimg.com/vi_webp/Rrrv51XmPcI/maxresdefault.webp"
---

DNS, IPs, and hosting on Masternodes: Exploring the benefits and challenges of adding DNS support to the Dash platform.

## Episode Summary

tl;dr: This episode delves into the potential benefits and challenges of adding DNS support to the Dash platform, discussing how it could improve usability, decentralization, and censorship resistance for hosting websites on Masternodes. The hosts explore the technical aspects, the need for certificates, and the importance of meeting web developers' needs to ensure the platform's success.

## Chapters

00:00 - Introduction and Background

The episode begins with a discussion on the importance of mindfulness and purposeful action in building projects, highlighting examples of individuals who have faced challenges for their efforts to empower others.

04:46 - Transition to the Main Topic

The hosts introduce the main topic of the episode, DNS, IPs, and hosting on Masternodes, and discuss the change in the show's hosting lineup.

06:51 - Certificates and IP Addresses

The conversation turns to the need for certificates in the Dash platform, the challenges of obtaining IP certificates, and the centralization of the IP address system.

18:12 - Benefits of DNS Support

The hosts explore the potential benefits of adding DNS support to the Dash platform, including improved usability, decentralization, and the ability to host websites on Masternodes.

35:01 - Challenges and Concerns

The discussion touches on the challenges and concerns surrounding the addition of DNS support, including the need for further research, potential pushback from the community, and the importance of meeting web developers' needs.

44:15 - Hosting Websites on Masternodes

The hosts delve into the opportunity and potential benefits of hosting websites on Masternodes, including improved censorship resistance and income generation for Masternode owners.

52:30 - Questions for Dash Core Group Developers

The episode concludes with the hosts posing questions for Dash Core Group developers regarding the removal of DNS support and the potential reasons behind it.

## Transcript

[00:00] Why We Build, that's the title of this segment. Three words, three syllables that communicate so much.

[00:13] Why speaks to the motivation, ideally it will involve mindfulness, intent. We speaks to us, our community, our collaborative efforts.

[00:23] Build speaks to the action, it connotes constructing, it is positive. Through this segment we aim to make clear our rationale and showcase our subsequent

[00:32] steps. Opposite of that mindful action may be what's shown in the 1997 sci-fi movie Cube in which

[00:38] a handful of individuals awaken to find themselves in interconnected, booby-trapped, cube-shaped rooms.

[00:44] It's hinted at that the cube was a military industrial project gone awry, that no one had the complete picture, that each contributor never bothered to ask why, and the result

[00:53] was a Kafkaesque killing machine. A far-fetched example certainly, but one that underscores the importance in contemplating

[01:00] the why before acting. Pausing to inquire why can stimulate each person to think for themselves, to weigh the

[01:07] merits of an idea they have or of a suggestion or order given to them. By checking that idea, suggestion, or order against their own conscience, they are more

[01:16] likely to act efficiently, purposefully, and in harmony with themselves and others around them.

[01:22] In the past "Why We Build" episode, we discussed the harassment Alexey Pertsev was facing.

[01:27] He was not accused of harming a person or property, but of simply writing code. Pertsev saw a demand to bring privacy to a crypto-protocol where it was absent.

[01:36] His why was clear, he acted and built a service that other individuals voluntarily used. So why was he harassed?

[01:43] He was harassed because he empowered everyday individuals, something that threatens the status quo, the very people who in turn harassed him.

[01:52] Does that mean such efforts should not be undertaken because of fear, because of the what-ifs?

[01:56] No. If those of us who champion personal responsibility or self-sovereignty or self-governance were

[02:02] to self-censor, we'd individually be worse off because we're not being true to ourselves and we'd be worse off as a human organism.

[02:11] But we can each learn from others to minimize risks, and we can, and I'd argue should, acknowledge those who have advanced this quest for human liberation.

[02:23] In early October 2013, a handsome man in his late 20s entered a small library branch in San Francisco.

[02:30] He found a table, sat down, and opened his Samsung 700Z laptop to tackle some online work.

[02:37] But he soon heard a commotion. A man and woman were arguing nearby.

[02:40] He looked up. At that moment, a stranger swiped his computer away while others pointed firearms at him.

[02:47] That man, Ross Ulbricht, has been caged ever since. Ulbricht was well-read in philosophy, Austrian economics, and agorism.

[02:55] He had a drive to abolish violence and coercion, especially its systemic application from institutions and governments, and not content just to theorize, he built.

[03:06] No doubt a smart, capable dude, he was an Eagle Scout and had degrees in physics and materials science.

[03:12] He taught himself how to code and build a marketplace akin to eBay, which he called the Silk Road.

[03:17] Among other items, vendors there offered substances said to be illicit. The Silk Road facilitated voluntary interactions, triumphed self-ownership, and helped bring

[03:27] a use case to cryptocurrency, which was still relatively new to the scene. Ulbricht's why was clear, but what about those who kidnapped and caged him?

[03:49] Their why was clear, too. Their clout was threatened.

[03:52] Worse than being lobbied to change, change their draconian drug policy and their interference into the lives of consenting adults, they were completely ignored.

[04:02] And unlike the Ebays of the world, they weren't even receiving a cut of the action. So they threw the book at Ulbricht.

[04:08] At what was essentially a show trial, Catherine Forrest told Ulbricht that he would be caged until he perished, two life sentences plus forty years, again just for writing code.

[04:18] Though those targeting Ulbricht had engaged in all sorts of character assassination before and after his trial, at the end of the day, Ulbricht was never charged with hurting a

[04:27] person or property, because he didn't. Common sense makes clear just who in this situation are the criminals.

[04:34] Efforts to see Ulbricht pardon have yet to materialize, but there's always hope. If you feel so inclined, you can impart some hope directly by writing him, and by thinking

[04:46] constructively and working to build a better world. Welcome everyone.

[05:01] As you can probably see already, I am your sole host today, and I have with me AJ. How are you doing AJ?

[05:09] I'm a little under the weather. A little under the weather.

[05:13] Also your mic could use a little volume, I think. Might just be on my end, but, so, just so everybody knows, and what to expect, Pete

[05:25] and Amanda won't be doing the Incubator Weekly live show, continuing from today on. Pete's helping out with the back end today, so thank you for that Pete.

[05:38] And then next week, I will either, we will either not be having a show, or I will be finding a new host, or potentially just hosting myself.

[05:50] So that is what we can expect going forward. Today we are talking about, for the second time, I suppose, the topic of DNS, IPs, and

[06:08] hosting things on masternodes, although I think the focus today will be, last time we talked about this, AJ, we talked about it in the context of what services can we provide

[06:22] from the masternodes, potentially even serving static websites, having the masternodes actually serve websites.

[06:33] And today, I think, because of some of the things that we've talked about, you and I, as well as over Discord, I want to focus more on the IP and the DNS topic specifically.

[06:51] Getting SSL certificates, and what this whole business is about, getting certs in an automated way and in a way that can be scripted, so that masternode owners don't have to do any

[07:10] manual steps to get their EvoNodes running. So you have recently gone through the documentation for setting up an EvoNode, and have scripted

[07:26] it to the point where I believe you got a successful bringing together of all the components of an EvoNode without using DashMate or Docker.

[07:38] I didn't script it, I just went through the manual process and kind of reverse-engineered the manual process from what was available.

[07:46] Right. Yeah.

[07:48] When I said scripted, I meant that kind of more or less loosely, because I do believe you were writing some basic shell scripts along the way, but it's not all packaged.

[07:58] I don't know. You can correct me if I'm wrong on that, but...

[08:02] Yeah, sure. There's a few things that I wrote, but mostly it's just going through it manually, trying

[08:09] to go through it manually. Yeah.

[08:13] Okay. So yeah, we've had some discussion on Discord about why...

[08:21] So I guess I'll back up even further. We recently found out that we will not be able to rely on...

[08:30] IP certs aren't going to work. Rely on ZeroSSL as our sole provider for IP certifications, or certificates rather, because

[08:43] they are moving to a paid plan. Moved.

[08:46] They've already moved to a paid plan. They've already moved.

[08:49] It's already enacted, and it's 10 times more expensive than a traditional certificate would be.

[08:55] So let's just paint the picture for what the process would be if nothing changes. We still want to use IP certs, and what will the process be for an EvoNode operator to

[09:11] get their EvoNode up with a cert so that... And I guess we could even back up a little further, like why do we need certs in the

[09:20] first place for these master nodes? Because people typically have been operating without certs for a long time.

[09:29] So what about evolution makes it required to have a cert from a... Not just a cert, but a certificate from a certificate authority?

[09:42] So it all depends on what level of this that you actually buy into, right? So if you believe that people are going to be building web applications that run in a

[09:54] browser, and you believe that those web applications are going to contact some central set of seed nodes, and then they're going to get a list of other nodes, and they're going to connect

[10:06] to them directly from the browser, if that's what you believe, then TLS certificates are necessary for that belief to come to fruition.

[10:16] And particularly TLS certificates that are from a known certificate authority, and if you want it to be decentralized, then you also need to add what's called a CAA record,

[10:31] which is basically the newest standard in DNS for decentralizing certificate authorities. It basically means that you can choose to pin your certificate authority so that it

[10:47] can't be hijacked, which in reality has happened, but is very, very rare. But it's, you know, it's like at the level of governments and stuff, and when it's found

[10:59] out, that certificate authority just gets revoked. So somebody's basically got one shot at doing it, and once they've done it, they're blacklisted.

[11:09] So it's not something that happens very often, but nevertheless, it is really important to be able to choose your certificate authority, and the CAA record allows you to do that.

[11:18] So anyway, so you need to have a certificate. The only way that you can get an IP certificate that I know of is through 0SSL.

[11:28] There are probably other ways to get an IP certificate that go the more traditional route of manual process of verification of the IP address, and then you could get a cert that

[11:40] maybe lasts for a year or something. I'm really not sure what that looks like because, you know, the web has been around for 20 years,

[11:48] and there's not really a lot out there that relies on TCP/IP without the web. So there's not really a use case for that outside of the masternodes that I've ever

[12:02] heard of. So there may be something that we just haven't researched yet and discovered yet, a service

[12:09] that would allow us to do this. Not an automated service, but there may be something that would do a manual process like

[12:17] what is done with 0SSL because you can use 0SSL for free three times if you use their manual process, which would mean that every 90 days for three times, you could get a free

[12:32] IP certificate. But then after the end of that, either you've got to create a new account, and it's a manual

[12:37] process, so you don't get to automate it. Every 90 days, you'd manually have to go in, revalidate, configure.

[12:44] So if you're going to do that, it makes sense to just go the more traditional route. If you can find a traditional certificate provider that will give you an IP cert, which

[12:52] I imagine there must be some out there, it's just, like I said, the use case doesn't exist, so I've never heard of anyone doing it before.

[12:59] Okay, so maybe it just needs some more research and finding a different provider. So outside of that, let's say the worst case scenario is that there is not another provider.

[13:17] After that, you say, three 90-day period process, my biggest concern for, not for myself necessarily because I'm not as privacy focused as many of the other masternode owners.

[13:35] I do value privacy, but I'm obviously here on screen with my full name right there in my handle.

[13:43] But I imagine most masternode owners would not want to provide, to me, the bigger deal is not necessarily a manual step.

[13:55] It's more that after that period, they will be required to pay for the service. Well, if you were going to do that, then you just pay from the start.

[14:06] The problem with paying for it is it's $100 a year, or $120 a year, something like $10 a month, which a traditional certificate is $10 or $12.

[14:17] So I'm not saying $100 a year is outrageous. Okay, so yeah, it's expensive, relatively speaking.

[14:28] But to me, that's not even the bigger problem. The bigger problem is the only payment method that these guys accept is credit card, as

[14:36] far as I know. I think that's a ridiculous argument because look at the reality, right?

[14:42] I mean, I don't know what fairytale people are selling, but the reality is most of the masternodes are on AWS.

[14:50] They've already given their credit card, they've already done KYC, you know. Yes, there are a few masternodes out there that are on independent platforms or running

[14:59] off of ISPs or whatever. And I would love to see the pie chart for this.

[15:03] Maybe I'm wrong. I don't.

[15:05] I don't think so. I don't either.

[15:10] So it's not like these people didn't already do all of this, right? So to say, I mean, to get an IP address, all IP addresses have been bought.

[15:21] All of them. There's 4 billion IP addresses.

[15:24] Every single one, not necessarily individually, but in groups, they have all been bought. There are none left for purchase.

[15:31] There are a few that are left in a reserve pool. I won't go into the details on that.

[15:36] These were purchased by people like AWS, like they purchased large blocks of IP addresses. Not people, but organizations.

[15:44] Organizations. So an individual cannot buy an IP address.

[15:49] I don't think that an individual ever could have bought an IP address. You're saying that these masternode owners, because they can't buy their own IP address,

[15:59] and even if they would be able to do that, they'd probably have to buy a credit card. I don't know who they buy these things from.

[16:07] You get it at least from AWS or from DigitalOcean or from Volter or from your ISPs. You're getting it from a second-hand provider.

[16:15] Right. And in America, when you go through an ISP, typically you get a real IP address.

[16:21] My understanding is that in a lot of the European countries, you actually don't get connected to the internet.

[16:28] You're on a private network and you have to go through a bridge to get to the internet. Because the only way you can be on the internet is with an IP address.

[16:34] If you don't have an IP address, you can't get on the internet. So my Comcast connection, they give me an IP address.

[16:41] That IP address is what makes me part of the internet. Without that IP address, I'm not part of the internet.

[16:46] So you harken back to the dial-up days. The dial-up days, you didn't have an IP address.

[16:52] You dialed in, you used your phone number to dial in to AOL or whatever, and they had, they were actually connected to the internet, and you were going over their bridge, and

[17:05] then they might be masquerading an IP address over a bridge, but there wasn't, your computer didn't have, well, actually, technically, I think it did have an IP address, but you

[17:14] weren't connected to the internet. You were connected to a bridge service that was bridging a connection to the internet

[17:21] and then masquerading an IP address to your computer. And that's what happens in networks where the IP addresses have been exhausted and there's

[17:29] no more to supply to people who are connecting to the internet, because they have private networks that are not on the internet, and they just bridge them through a technology

[17:38] called NAT, and that will happen at the ISP layer in some cases. Okay, so maybe your overall argument there is you're saying most of these people must

[17:53] have already given their credit card information to some provider on some level anyway, so asking them to give their credit card information to ZeroSSL shouldn't be a big deal, but what

[18:07] if it is? And what if they just don't want to go through this process?

[18:12] Are there alternatives? I know that you've suggested if we supported DNS, having masternodes be able to register

[18:24] with their DNS name rather than their IP address, both on the core side and on the platform side in the masternode list itself, then...

[18:35] So this is not an either or, just want to be really clear up front, this is not an either or.

[18:40] Right. So this is having the possibility to use DNS to be able to register.

[18:49] In addition to the possibility of using an IP address. So right now you have Pepsi, let's let masternode owners have the choice of Pepsi and Coke.

[19:01] So why, how would this help us and what other opportunities would it provide for us if we had this?

[19:12] Like, why make a big deal out of this? I mean, again, like, do you believe in the web or do you not believe in the web, right?

[19:21] Because when we talk about TCP/IP, that is literally not the web. That is part of the internet upon which the web is built.

[19:29] But the web is built on DNS. That is what the web is built on.

[19:33] So do you believe in the web or do you not believe in the web? If you believe in the web, then you have to definitionally believe in DNS.

[19:43] DNS is what gives you names. So it is, you know, example.com.

[19:50] And at the root level, well, there's a couple of problems here because we could talk about this either way, right?

[19:56] So let's say that you don't want to do KYC, then you have to be on a private network or you have to be on a private domain, and maybe both.

[20:03] So if you want to avoid KYC, then you actually don't want to have to be going through a public IP address.

[20:11] You want to be able to have a private IP address. And you don't want to have to have a root, not root level, secondary level domain.

[20:18] I said root level. Apex is what it's called.

[20:20] Apex domain. Apex domain is what people purchase.

[20:22] So example.com is the root. Example is the apex.

[20:28] So if you wanted to not have any sort of KYC, you would go through a provider that, like for example, DuckDNS.

[20:41] DuckDNS doesn't have any KYC. And just so you know, or just so everybody knows, when you say KYC, you're not saying

[20:47] that these providers actually do the formal KYC process. You're just saying any kind of name associated with it.

[20:54] I should have said PIA. Sorry.

[20:57] PIA. Personally identifying.

[20:59] P-I-I. P-I-I.

[21:01] P-I-I. P-I-I.

[21:03] Information. Personally identifiable information.

[21:05] So yeah, if that's what you wanted, we actually need to change two things. One is that the code, at some point, it appears that it allowed you to choose port numbers

[21:24] arbitrarily. Which is actually really important.

[21:27] Because if you can choose port numbers arbitrarily, then you can run through a private network because you can have a public network bridge to a private network and do the port translation.

[21:39] All stuff that just kind of basically gets taken care of for you. You don't really need to worry about it.

[21:42] And that also, in some of those networks I talked about before, like some of the European networks that don't have public IP addresses for the ISP, still have what's called UPnP

[21:54] and NATPnP, which is basically a port mapping protocol to be able to get things from a public network to a private network.

[22:01] So there's that, and then there's the name. And the thing with the name is that the IP system is incredibly centralized.

[22:12] So much so that it is not possible for a person to participate in it independently. Every single thing is bought.

[22:21] You cannot choose an IP address. You cannot go to AWS and choose an IP address.

[22:27] You get whatever is assigned to you by whoever owns that fiefdom of IP addresses. So just to hold you out there for a second, when you say IP is centralized, what exactly

[22:42] do you mean? I mean that it is not possible for you as an independent person, it's not possible for

[22:53] an independent party to participate in the system. You have to have a service provider, and are you saying that there are a very few number

[23:03] of service providers which you can get an IP from, or what makes it centralized? Wherever it's owned is where it's owned.

[23:14] So we've abstracted away phone numbers. You can't really abstract away IP addresses.

[23:19] So phone number, if you're on Verizon and you want to switch to AT&T, you can keep your phone number.

[23:25] But if you're on AWS and you want to switch to DigitalOcean, you cannot keep your IP address. And I have to argue from the technical standpoint of the way TCP/IP works, trying to do that...

[23:41] It's not necessarily an evil that IP is centralized and hierarchical. It has to be, right?

[23:53] Because you have to have a system by which the numbers match up, by which you can route things.

[24:00] And if you could just pick and choose an IP address at random, and then you had to go register it with a bunch of routers across the internet, and every router had to have

[24:08] a big table of... Then there's no meaning in the structure of IP addresses itself at that point.

[24:14] Yeah. And then you wouldn't get any of the optimizations that you get with TCP/IP, or not any, but

[24:20] you'd be missing out on many of the optimizations. It would degrade the system.

[24:25] But, I mean, that's why we have the web, right? Because the web is an abstraction over top of that, that allows us to pick and choose

[24:33] providers and not be tied to any individual one, and you can... There's lots of different political entities you can choose from.

[24:43] There's lots of choice in the web. You're not tied to any specific organization, any specific value system.

[24:50] You can run your own name servers. You can't run your own router for the internet.

[24:58] The idea that the TCP/IP layer could be decentralized to the layer of the web is just... It's not feasible because TCP/IP, for all of its faults, was designed well.

[25:16] If you were to redesign it from scratch, you would end up with a very similar system with slightly different trade-offs.

[25:24] If you could redesign it from scratch, it'd be a better system, but it wouldn't be ten times better, and you wouldn't solve for the centralization/decentralization issue.

[25:35] Other than that, you... Essentially what IPv6 would have done, if it had succeeded, would have been that you'd

[25:45] have an entire... Every public address would come with, essentially, an infinite range of private addresses that

[25:52] are routable that come with it. I can understand the purpose behind domain names in a web context, meaning when the web

[26:05] was getting going, people wanted to have a name so that they could say, "My website lives at ryan.com, and I want to be able to have and use that specific name regardless of the

[26:21] IP address that it points to." If I did want to change providers, let's say I'm hosting my website at AWS now, but I want

[26:33] to move over to DigitalOcean, then I can maintain the same name, ryan.com, and my users and all their users' browsers and all those things can still remember.

[26:45] When I go to ryan.com, I'm getting the same content, even though it's routed to different IP addresses underneath.

[26:53] I understand that from the web level, but from our perspective, when we're running Masternodes, I suspect that nobody needs to remember the name of a specific Masternode server.

[27:09] I would say that most people don't really care about having a name. This is part of the centralization of the Masternode system.

[27:18] The Masternode system is not designed to be maximally decentralized, for better or for worse.

[27:25] I can't run a Masternode on a Raspberry Pi at my house. The reason for that is that at my house, every 90 days or so, my IP address is going to change.

[27:33] There is not a mechanism to automatically re-register by IP address, and there's not a mechanism to provide an abstraction over the IP address.

[27:42] If I wanted to run a Masternode on a network where I'm not in control of the IP address, I can't do that.

[27:50] Well, you can. You just have to write some kind of an automation script so that if and when your service provider

[27:57] does change your IP address, it detects that, it picks it up, and it re-issues the registration transaction, the pro-reg.

[28:10] So I'm just playing devil's advocate here, trying to get to the root of the issue, because I want to know specifically what adding DNS support to the Masternode list, for example,

[28:26] would provide us that we aren't getting right now. Well, I will point out AWS isn't connecting everything.

[28:37] They're not keeping big lists of IP addresses, I mean, they are, but when you look at any AWS service, even if it's an IP address, it's being done over DNS.

[28:46] So you'll see something like EKS 16-5-244-12.amazonuswest.aws.com or something like that, right? So just lots of systems use DNS because it's an abstraction over IP addresses, and because

[29:12] it's convenient to use and have things automated quickly, they'll use it even when something is directly tied to an IP address.

[29:24] So DNS is, it's just a good abstraction layer in general for automation. It's easier to automate.

[29:39] Is it because the tooling is much more mature, like there are a lot more tools and services that use DNS rather than IP alone?

[29:49] Is that kind of what you're saying, is the tooling is more mature? Yes.

[29:53] Absolutely, because IP, like I said, you don't get to choose your IP address. You don't, you know, with the rare exception of if you work at a company or an organization

[30:05] that owns a block of IP addresses, but then again, you're not choosing it, the company chose it.

[30:11] Anyway, whatever. Yeah.

[30:13] So yes, yes. The tooling, there is almost all dynamic DNS, well, all dynamic DNS is DNS, right?

[30:22] So all of the dynamic IP systems are DNS systems. And that makes sense, but the, you know, you said, well, what could we do that we can't

[30:33] do presently? Yes.

[30:35] Well, again, like I think the way that this is really going to happen, if we look historically what's happened with those systems, I don't think that people are going to be connecting

[30:42] to master nodes in the browser. If people develop web-based systems, I think that there's going to be too many technical

[30:49] challenges for it to be realistically done in the way that the current thought process seems to be.

[30:55] I think there's going to be too many technical challenges and what's going to happen is people are going to develop proxies at the server layer and their web app, their example.com

[31:04] is just going to talk to their server.example.com and then their server.example.com is going to handle all that complexity of figuring out master nodes and stuff like that.

[31:15] That's what I think would happen if this system evolved naturally with the current constraints. Now if we change the constraints, we say, okay, you can use DNS and we'd have to change

[31:28] at least two constraints. One is that we'd have to have a federated decentralized system rather than a mirror,

[31:36] meaning that rather than 4,000 nodes, each having a copy of some data, we'd have to have it so that there's some sort of sharding where a hundred nodes have a copy of this data,

[31:48] a hundred nodes have a copy of that data, and so on and so forth. At some level, you need to have a system that's scalable.

[31:56] You need to have a system that as you add more nodes, the system has more capacity, not the system has less capacity as you add more nodes.

[32:06] If you had it so that there's domain names and so that you have some form of sharding, well then you could have applications hosted directly on, I keep on saying Evo nodes, we're

[32:17] not really even talking about Evo nodes or master nodes, we're talking about Evo nodes. I keep on saying master nodes, but we're talking about Evo nodes.

[32:24] In an Evo node system, if you have domains and you, on the client side, can pick and choose, and I think this is one thing that maybe a lot of the people that are pro the

[32:36] Evo node system are actually against is the idea that a user would pick and choose or that the software that the user is using would pick and choose which systems, because I think

[32:46] that there's somewhat of a love of the idea that it's on all 4,000 nodes, and that's a good thing.

[32:53] In my mind, that's a terrible thing because it's just a huge waste of resources, and I don't understand how that provides any benefit to a user.

[33:02] As a user, I want things to be fast, I want them to be affordable, I want it to be easy. If you had a system that used DNS, then you have the option, at least, to be able to host

[33:17] an application directly on Evo nodes in the Evo node network, and I don't think that you should be returning a list of, for DNS, returning a list of 4,000 IP addresses that the thing

[33:31] could connect to. I think that would be detrimental.

[33:36] That's not how it works in any other system in the world that I'm aware of, and I don't think such a thing exists other than that somebody may have done it as attempting to

[33:46] do an attack on DNS or something like that. I don't even think that it would fit in the packets.

[33:51] I don't think you could do it, because I don't think the technical constraints allow for it, but in any case, at the name server level, you can select some number of nodes that participate

[34:06] in that grouping, and then that grouping of nodes is that application. So even if you wanted all of the nodes to be able to verify the application, which all

[34:21] of them should be able to verify the application, not all of them necessarily would have a copy of the application, and certainly not all of them would be running the application or

[34:29] be connected to for the application. I don't know if that made any sense.

[34:36] I'm a little bit fuzzy-headed today anyway. Like I said, I'm a little under the weather, so I'm just babbling worse than usual probably.

[34:42] Okay. Well, yeah.

[34:44] I do want to get down to the root of the benefit of having a DNS system, but in all reality, I think that my plan going forward is basically this.

[35:01] I don't think that there's a lot of demand for adding support for DNS right now, and in addition to that, I think that there's a fair amount of pushback for it, for whatever

[35:17] reason. Oh, hold on.

[35:19] Wait, wait, wait. Adding support?

[35:21] That doesn't make any sense. What do you mean?

[35:23] No, I know your perspective. It's not because it's built in.

[35:25] Like the code is already there. It was built with DNS support.

[35:31] So there's no adding DNS support. The DNS support is there.

[35:35] A flag is being passed false instead of true. Yeah, and I don't know if that was ... I'd actually have to do the research on that.

[35:44] My guess is that that was taken out back in Bitcoin's day. I do seem to remember that you were able to, at some point, send money to a URL.

[35:58] That's just what I know from memory from back when I was getting into this over 10 years ago, but that was added originally, and then support for that was removed deliberately,

[36:10] like you're saying. And so I have to say that somebody at some point, whether that was Bitcoin developers

[36:17] or the Dash developers, removed that support deliberately. And I have to think that they had a reason for that.

[36:27] And whether we agree with that reason or not is ... They don't like the web.

[36:34] So many of these people, when you talk to them, they talk about how the web is bad. The web is terrible.

[36:39] The web is the worst thing that ever happened. That's just, it's empirically not true.

[36:47] It's a system that has been incredibly resilient. It's had incredibly high adoption.

[36:52] It's incredibly user-friendly. When you say web, there's a distinction to just traditional networking.

[36:59] You're saying specifically, you mean the DNS system, right? By web, you basically mean the DNS system, and websites, and web URLs, things like that.

[37:10] Yes, URLs, APIs, names, the stuff that whenever you open up a web browser, all of that stuff that happens, that wouldn't have happened in the '80s, before the internet came around

[37:24] in the '90s. Including the need that browsers have for certificates, certificates for reporting.

[37:32] Well, the certificates- The certificate system is actually below the web layer.

[37:41] It kind of straddles both layers, because a certificate has web information in it, and it has TCP/IP.

[37:50] It runs over TCP/IP, but it contains web information. TLS is in between TCP/IP and the web.

[38:06] You want TLS because it does two things. It gives you over-the-wire secrecy, and also over-the-wire integrity.

[38:21] Secrecy meaning that other people can't see what information is being transmitted, because it's encrypted.

[38:30] Integrity meaning that if someone is in the middle of an encrypted transaction, they can't just swap one byte for another byte to corrupt the message and have it go undetected.

[38:43] If someone ... Let's say that they were able to ... They don't know what the encryption is, but they're able to swap a byte, and when it gets decrypted, it was somehow still valid,

[38:58] which can happen with encryption schemes, and then your message is off by one letter. Go versus no.

[39:09] Like shall we launch the nuclear codes? They're able to swap out the n-byte for the g-byte.

[39:18] That would be ... It's somewhat unlikely, because the message is encrypted and they're changing a byte in the blind, but if they knew about how long the encryption header

[39:30] were, and they knew about how long the message were, and they could just kind of guess like if I could change this byte by so many bits, I could get it to ...

[39:39] I know that nobody's going to dispute the fact that we want privacy and integrity across ... Everybody is on board with TLS.

[39:51] My comment was about certificate authorities, and how you need to get ... Web browsers require you to get a certificate from a certificate authority that I think people have a concern

[40:04] with and they don't like that, and so the people want to go to systems like Tor and things.

[40:10] I understand all that. My big dog in this fight, if I just have to zoom back out for a minute, my big dog in

[40:17] this fight is that I want evolution, or platform, or whatever we're calling it, I want it to be as successful as possible, and for it to be as successful as possible, we want it to

[40:30] be easy to use for people and meeting web developers, specifically web 2 developers who know nothing or care nothing about blockchains, to be able to use this system in a way that

[40:43] just works, which just works with their Chrome browser, their Internet Explorer browser, Edge, whatever, their Firefox browser, their Chrome browser, Brave, all the browsers, it

[40:54] just works, and it gives no scary messages to their users. Right now ...

[40:59] Well, it wouldn't even give scary messages. It would just not work.

[41:02] It just wouldn't work. Right.

[41:04] Yeah. That's what I want to focus on, because I hang around these circles of web 2 developers

[41:10] a lot, and I know that they're not going to bend over backwards to build applications that they need to do it in a special way, so I want to meet these developers where they

[41:21] are, and so that's why, if making that ... And also, I want to serve Masternode owners so that they can host these services in a way that's just a click of a button.

[41:38] At the end of the day, I want it to work easy and cheaply and privately, and so I don't really care what technologies we end up deciding to use, whether we need to add DNS support

[41:54] or not. I just want it to work.

[41:57] The purpose of this show is basically just to say, "Let's get the arguments out there for why adding DNS support might help with that grander vision."

[42:06] I think you've got to turn it around. You have to ask the question, "Why would you remove DNS from the web?

[42:13] What benefit would you get by removing DNS from the web?" Because asking why to do it is such a dumb question from the sense of, "Okay, Google

[42:25] does it. Amazon does it.

[42:27] Visa does it." You literally don't interact with any product that doesn't use DNS, so the onus is not on

[42:37] the world to prove why it has adopted DNS. The onus is on whoever has disabled it.

[42:46] The onus is on them to provide strong, really strong, validatable, verifiable arguments as to why to not have it.

[42:57] I understand that, and we're not going to be able to meet that answer today because we have nobody from that side of the argument on the show.

[43:06] I would like to see the answer to that, but right now I think the argument could be as simple as, "Well, somebody changed it at some point, and it would take work to change

[43:17] it back." It would take an afternoon, maybe a weekend, because I've gone through the code, and there

[43:26] could be a dragon that I'm not seeing, and I'm not a C++ developer to be able to go through and make all the changes.

[43:31] I'm not familiar with that code base, but just spending a couple hours, I've found the places where all of the code is still there.

[43:41] All the DNS code is still there. There's a couple of places where a network name needs to be added, more like half a dozen

[43:49] places where the network name needs to be added, and then a few places where the resolver needs to be enabled rather than disabled, but it's not like, "Oh, this is a heavy lift.

[44:00] We've got to halt the world and figure out how to rethink our lives." No.

[44:05] It's already a variable byte length. The code's already there.

[44:11] It just needs to be not disabled. Okay.

[44:15] Now, just to maybe wrap this up a little bit, I want to go back to the hosting websites on Masternode's concept that we haven't really spent a whole lot of time implementing.

[44:32] We haven't spent any time implementing. We've spent just the amount of time that we've talked about it on the show.

[44:38] That's the only time that we spent doing this, but what I'm seeing is I'm seeing a big opportunity, and I'm also seeing a big opportunity for income in terms of this could be a great service

[44:57] just to get income for Masternode owners, but I'm also seeing it in a dystopian future where websites are ... Well, not even a dystopian future, but I believe that there's in some

[45:17] abstract way that I'm not smart enough to be able to even express, I think that there is an opportunity to provide a more secure ... What am I trying to say here?

[45:36] I want to be able to build websites where I don't have to rely on AWS or Vercel or Netlify to keep my website up.

[45:45] In a future where it's criminal behavior to transact and swap cryptocurrencies, for example. Think about Eldorado or some of these front ends that do swapping services.

[46:02] If that's criminalized, then these providers like the Vercels and the AWSs and the Netlifys of the world, they could shut these websites down.

[46:13] How can we provide this service in a way that is more censorship resistant? I think it's a really good idea to, one, do the things that need to be done, like using

[46:27] DNS and allowing arbitrary ports, as the code was originally intended, so it seems, that would allow people to more easily work in diverse conditions, because the more it's

[46:38] restricted to, it has to be an IP address, it has to be on a specific port, the more that tends towards pulling people into AWS, because that's where, at your house, you're

[46:48] not going to be able to get two or three IP addresses, typically speaking. It's pulling people into those centralized services and concentrating the master.

[47:01] If you open it up so it's more easy to run a master node behind a private network, from an alternate port, etc, that's just the way the code was designed originally, then you're

[47:14] going to allow more diversity in where the EvoNodes are hosted. If you have more diversity in where the EvoNodes are hosted, then if you pick from a random

[47:24] pool of EvoNodes to host some software, then you're going to get a more random distribution of where it's hosted, which means that it's going to be more censorship resistant.

[47:36] If you look at EvoNodes as an abstraction over cloud service providers, you look at EvoNodes as a cloud service provider, but also an abstraction over cloud service providers,

[47:51] it makes more sense to use a service that's abstracted across many providers than a service that's on one provider.

[47:59] How many times a year does a whole region of AWS go down and a huge swath of websites you can't visit that day?

[48:07] Once or twice a year? Anything that's hosted primarily on one set of services is going to have the drawbacks

[48:17] of when that service, no matter how resilient and how great it is, eventually somebody hits the wrong button.

[48:24] Somebody clicks the wrong thing and the whole thing goes down for a day. Whether it's that or AWS comes out with a policy that truckers from MAGR or whatever

[48:36] aren't allowed to have their email hosted on AWS services and take them down or whatever ridiculous political nonsense goes on.

[48:46] You get away from that when you abstract it away. I personally find it very, very interesting the idea of using a hosting service that's

[48:55] abstracted across multiple hosting services without having to know all of the minutiae about the particular hosting service that's behind the hood.

[49:07] That is essentially what EvoNodes could provide. The more diverse of network environment the EvoNodes are in, the more of that you get.

[49:16] Yeah. I think there's a huge opportunity and I'd love to see exactly what you're describing,

[49:23] be able to have a service that's abstracted across many different providers. I think that that's a future that has promise.

[49:33] Not only promise, but in terms of censorship resistance, but like I said earlier, these guys like Netlify, Vercel, that are basically just companies that make using AWS easier,

[49:48] they make tons and tons of money. They bring in a lot of money, including venture capital money, but they bring in venture capital

[49:58] money because there is a lot of potential for actual revenue in the future. I think that if we could bring that money into the masternode system and make it so

[50:15] super simple for a developer to just say, "Here's my website, here's my HTML page, my CSS, my assets."

[50:25] Just throw it up to the masternode network with a click of a button, and also I get a DNS name so I can say, "This is ryanswapservice.com," and have the masternodes actually hosting

[50:42] and serving that web content up. I would love to see that.

[50:48] I think that would be super cool, and I think that we could totally do it. The only thing I think that would be getting in the way, I think only masternodes could

[50:57] do that if Evo launches the way that it's architected right now. Evo nodes would not be able to do that because of the way that they constrain the ports through

[51:08] the use of Envoy, although I may have found a way around that. I'm not 100% sure.

[51:15] It seems like I found a way around that, but in any case, maybe there's a way around that, maybe there's not.

[51:21] But I think that on the existing ... That's software, right? That doesn't require the Dash centralized group to bless it in order for it to make

[51:31] it happen. Masternodes could opt into that.

[51:34] That's software that we could just provide. Right.

[51:37] Yeah. If, like you said, those restrictions were removed, those port restrictions, and maybe

[51:43] there's a way around it as well. No, the masternodes, we could just give them the software.

[51:48] If we built the software, we could give them the software to do the hosting like you're saying.

[51:52] Oh, okay. The masternodes, but not the Evo nodes.

[51:54] Right, because the Evo nodes have the certain port restrictions and the way that the system is built.

[52:02] It wouldn't be as simple as just, "Here, just add this software to your thing." You'd have to have a different installer for the Evo node, not the installer that's currently

[52:14] provided. Okay.

[52:16] Somebody had said something about certain code being only for test net uses only. I haven't really looked into that in detail, but maybe there's something that we need to

[52:25] look into there as well. Anything else that you want to ... We're coming on an hour here.

[52:30] Anything else that you wanted to say that we didn't discuss about DNS, IP? Question that you want to pose for Dash Core Group developers who may actually be open.

[52:45] I saw Aposta, he seems like he's interested in helping, so let's pose a question to Dash Core Group, why DNS support has been removed?

[53:04] Was that Bitcoin developers? I think that we could- It could have been.

[53:08] It could have been back in the Bitcoin days. There's a tool for that, right?

[53:11] Git Blame, right? Just run Git Blame to see who actually did those lines.

[53:17] It's not that easy. Not that easy.

[53:21] Okay. Because the lines would have been moved up and down and around.

[53:26] There's a difference of 40,000 commits, so Git Blame is not going to- Just so everyone knows, Git Blame is a technical term.

[53:36] We're not blaming anybody. That's what it's called.

[53:39] It's called Git. Who made this commit to change the code in this way?

[53:44] Anyway, yeah. Final thoughts?

[53:47] Yeah. Yeah, I definitely- I want to know- This is hard though, right?

[53:54] Because I say, "Okay." I mean, we've already seen this in the Discord a little bit, although it's probably not the

[53:58] people that were actually directly involved in making the decision. Is there a real, valid, practical reason for disabling DNS?

[54:08] Why is the thing that's working for Visa and PayPal, Wells Fargo, Google, Amazon, Netflix, Excel, the thing that all of us use every single day, why is that somehow technically

[54:26] not good enough? Why do users' choices need to be restricted?

[54:31] Why is it it's so incredibly bad and it's so dangerous that we have to tie users' hands behind their back and say, "No, no.

[54:40] As a masternoder, you are not sophisticated enough to be able to make this choice for yourself as to whether or not your masternode should run this way," right?

[54:50] So what is it? But my concern with what the responses are is lots of cherry-picking and straw-man arguments,

[55:01] right? Like, "Oh, well, such and such a service went down one time in 2016."

[55:07] It's like, "Okay, well, yeah, chain halt happened one time in 2023. Like does that mean that we should give up?"

[55:16] And we got through it and in a way that like, yeah, so there are providers that are going to go down, certain DNS providers.

[55:25] I don't see any reason why we couldn't have a fallback of an IP even if we did choose a DNS.

[55:30] That's a technical question I can't answer, but... And we shouldn't necessarily have every single Evo node or masternode on the same DNS provider.

[55:39] I mean, I would not think like that Dash should dictate, "You must use Cloudflare. Thou shalt use Cloudflare and other DNS providers thou shalt not use," you know?

[55:52] And I think that, well, the DNS system is too decentralized to be able to enforce that. Like it would be too difficult to enforce in the first place that somebody use a particular

[56:04] provider because it's just, you'd have to go track down the name servers and find out who they belong to.

[56:08] I mean, I guess you could do it, but you'd have to block the IP address of the name servers and you have to block all these resolvers and it'd be a lot of work to try to enforce

[56:18] someone to pick a particular system. Just as long as we're not in, I guess the more realistic thing would be encouraging

[56:24] everyone to use the same system. So like if the automated tool that sets it up only works with Cloudflare, obviously people

[56:31] would only pick Cloudflare. So it'd have to be, it'd just have to be done in a way that it supports a few major providers

[56:40] and then has a very simple hook system where, you know, it just gives the information and then calls out to that provider or, you know, gives you a place to put in a script that

[56:53] anybody could make and, you know, Dash Incubator could churn those out all day long, right? We've got people that say, "Oh, we need an integration for EZDNS or DNSimple or GoDaddy

[57:04] or whatever." I mean, like that's less than a day's work that could be done over and over and over

[57:09] and over again in Incubator to support any number of providers. All right, well, I think that's a good place to leave it.

[57:17] Thank you everybody for tuning in and we'll catch you next week or maybe not.