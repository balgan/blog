---
layout: post
title:  "I want to block internet scanners!"
date:   2019-10-27 02:56:18 +0200
categories: internetscanning cybersecurity
---

### “Hi, can you please stop scanning me ? My IP Addresses are XXX.XXX.XXX.XXX”.

For years I received,read and replied to emails like these. As founder and CEO of a [company](https://binaryedge.io) who’s in the business of port scanning the Internet it is normal to see these types of emails. I always attempted to explain what we are doing, why we are doing it and why people should consider not having us block their IP addresses.

The base premise of the complaints is that people don’t like us scanning their IP addresses and checking which ports are open.

I won’t attempt to go into analogies on ports or windows and buildings as it’s not the objective of this post, this has been previously discussed and it is not a pandora box I intend to reopen here. Though, I will refer to one analogy at the end, however I would like to focus on trying to answer some questions that I typically get asked.

**“How can I block all internet scanners?”**

In this article by using data, I will try to explain why this is not feasible, what are some of the benefits and the problems that come with attempting to do this.

### The Internet is a noisy place!

Every second, there are multiple actors scanning your IP address. There are multiple reasons for this and the data from understanding who is scanning the internet can be quite interesting as it enables answering lots of different questions blue teams (defenders) typically have.

It’s because of the value of this data [BinaryEdge added the sensors](https://blog.binaryedge.io/2019/02/07/listening-to-the-internet/) to its data set or why [GreyNoise](https://greynoise.viz) exists.

The following image gives you a visual perspective, of the quantity of traffic that the BinaryEdge sensors see in just 15 minutes split by the source country that the traffic originates from.

![Data Source - binaryedge.io](/assets/img/sensors-15m.gif)

What is important to understand is that similar to a lot of topics in infosec there are different shades of color to what the organizations generating this traffic are attempting to do. You have benign players like BinaryEdge, Rapid7, Censys and Shodan but what does benign mean in this context?

- **They respect blacklisting** - if you request one of these organizations not to scan you again they will respect your request

- **No active exploitation** - the scanning is focused merely on identifying services running on the internet, no active exploitation of vulnerabilities occurs at any point in time

- **Benefit for you** - Most of these platforms allow you to check what data they have collected on your IP address. BinaryEdge allows you to check via [securityrating.io](https://securityrating.io) or via [app.binaryedge.io](https://app.binaryedge.io), Rapid7 makes data available via their open data program and other players have their respective platforms.

But, like everything else, there are also a lot of malicious actors on the internet and we will talk about their objectives in a few paragraphs.

Multiple companies have honeypots or sensors on their internet facing perimeter to try and understand what the different actors are trying to do to them. And some companies spread sensors across multiple points of the internet and try to tag these actors and their actions.

[Lots of different actions, actors and behaviours](https://docs.binaryedge.io/sensors-tags/) exist and happen on the internet.

Over the course of 1 hour we see different actors and actions happening as seen by the following image which represents the amount of tagged events seen in the BinaryEdge platform for 1 hour.

![Wordcloud Sensor Tags](/assets/img/sensor_wordcloud.png)

From this image we can see the top seen action is 

**ICMP_ECHO_REQUEST** - this means its a “ping” this makes sense as there are lots and lots of services checking for uptimes on machines worldwide, following this we have lots of different actors like **BinaryEdge**, **Censys**,**Netsystems**, **Shodan** and **Rapid7** in a smaller quantity, we also see actions that happened over this hour in the form of **HTTP**, **SIP** and **RDP Scans**.

### You’re targeting me on your attacks!

This is a common misconception that we also see people having. Specifically for the people doing internet wide scanning, you are not a special snowflake, this is actually a common factor between benign and malign internet wide scanning organizations. Neither of us cares about your specific IP address. We want to see the global picture. Rather than thinking from the perspective of “How am I gonna hack John Doe, that is behind IP address XXX.XXX.XXX.XX” we think on a global scale.

**Benign actors** are looking to answer questions like:

If a vendor fails to provide a patch, how many systems worldwide are affected?

If a vulnerability for a router is released how many ISP’s worldwide have that router deployed?

Do we see a specific country attacking another?

And some of these are hard to answer, even looking at the same 1 hour sample of traffic, we see what appears to be a specific country focused on just targeting another country, like in the case of Germany, Moldova, or Panama .

And this is where a big difference exists between the real and digital world. In general the concept of country means very little (exceptions exist).

An American hacker, can hack a machine located in Brazil and use it to attack an IP address that belongs to France. Now imagine any mix and match combination of this that you might want, and you have a spaghetti puzzle on your hands. With the development of cloud systems, companies have servers in my different countries, even though they might have their HQ or satellite offices registered elsewhere.

Everyone is scanning everyone and trying to tie to a country is not typically a good metric for attribution.

![Sensors - Events per country](/assets/img/sensors_countries.png)

But what about **malicious actors**? What are they trying to answer?

Their questioning is typically focused around machine infection or cryptocurrency available to be stolen.

You will often see scans that will identify the services running and then using the latest vulnerability that will give them control over a machine which they can then use on botnets, to mine cryptocurrency (due to changes in crypto prices you don’t see this as often anymore), or to install some type of ransomware that can give them a payday.

In this case if you try to file an abuse request as you do with benign actors, they will not respect your request and will continue to scan your IP address, many times a way of filling an abuse can even not exist as some providers are collaborating with these bad actors.

### So are you saying my worries are unfounded for wanting to block internet scanners?

No. Not at all. What I am trying to convey is that you are never going to be able to block them all. For as long as you have a device that is internet connected it will be scanned.

By asking non-malicious actors to block your IP addresses, you are however losing visibility into your own exposure as well. You should try to leverage the tooling that the attackers use as well.

Blocking an internet wide scanner, can bring you small benefits such as being removed from a tool like Shodan, BinaryEdge or Censys but it won’t fix your root problem.

**The root problem…**

If you’re exposing services you don’t think should be found by BinaryEdge, Censys or Shodan you shouldn’t be exposing them in the first place. Use these tools to your advantage, look for your company name, look for your IP addresses and understand what you are exposing.

Situations we see often where you can use these tools for your benefit:

- **Firewall rule deployment fail** - ports are exposed that organisations thought that weren’t but because of some part of their process of deployment of firewall rules failed, these ports ended up exposed to the internet

- **Lack of patching** - organisations forgetting to update some software running on their servers

- **Visibility into targeted attacks** - Let’s say you do have proper logging and start seeing some weird traffic on your edge network that you haven’t before, check the internet scanners and sensors. Are they also seeing this? was it a new internet wide scanner that showed up and is looking for some new vulnerability?

If I had to use an analogy, which I typically hate doing, its as if you have your building, with the windows without any curtains, internet wide scanners are the people on the street, and you are asking 5 out of 1000 on the street to cover their eyes and not look at your windows. And it just so happens that these 5 are the neighbors that would be respectful and tell you “Hey, I can see inside your house because you have no curtains”.

If you don’t want people to see inside your house, you need to put curtains on your windows.
