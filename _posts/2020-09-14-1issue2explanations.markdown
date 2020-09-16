---
layout: post
title:  "2 Users, 1 security notification"
date:   2020-09-13 02:56:18 +0200
categories: cybersecurity
---

Over the last year, due to the acquisition of my company, I took the position of GM of Customer Security at Coalition Inc., an MGA that sells cyberinsurance.

We continued to build features into the [scanning platform](https://app.binaryedge.io) but also a new product [Attack Surface Monitoring.](https://asm.binaryedge.io)

One of the features of ASM is the capability for a user to receive notifications about issues found in the organizations they are monitoring (all of the policyholders get this for free with their policy). 

When building the notifications feature, it led me to think about communication in cybersecurity, and specifically how an issue should not have just one way of being communicated to the end user, the reason for that is because you might have different cases of end users using your platform.

Communication is a soft skill that I would put at the top of the most important to have if you are in infosec/cybersecurity, finding the coolest vulnerability but then not being able to explain its impact to the users affected, makes it harder for organizations to evolve and improve their security level.

[Watch this talk by the master of communication in infosec, Javvad!](https://youtu.be/ijdGz3FeIOw)


## RDP - The gift that keeps on giving

We don't like RDP. Don't believe me ? 

See what happens when you visit: [justsaynotordp.com](justsaynotordp.com)

My colleague Jeremy Turner wrote an excellent blogpost about RDP, what it is and why we don't like it.

The short version of the story is that RDP is regularly attacked, we've seen it present in ransomware cases and at a very basic level, even the mere presence of RDP is believed to act as a signal of opportunity for ransomware.

We will come back to RDP in a second...

## Enter personas...

As mentioned on the Coalition site, we sell (at this point in time!) insurance to companies with revenue from $0 up to $1 Billion. As you can imagine, we have different types of what would typically be considered "end-users".

These "end-users", as you can understand will have different levels of IT knowledge, which immediately poses a super interesting challenge for us.

If I look at the range of people that use BinaryEdge (Coalition's Security Platform) and our policyholders,my range of end users looks something like this:

* Business Owner
* CEO
* CFO
* CISO
* IT Person
* Security Staff
* Developer
* Consultants
* etc...

So for the sake of this post lets reduce all these types of individuals into 2 groups:

* **Non-Technical / Money people**: CEO,CFO, Business owner

* **Technical people**: IT Person, Security Staff, Developer, Consultant 


What we need to work out next is personas to represent each of these groups of people. 

**Personas** are fictional characters created to represent a type of user that might use or be a target of your product. They are used across multiple industries to assist in solving problems. 

As an example in a previous work-life, I used personas when working at a bank in their innovation team.  As part of our internal process we used the [business model canvas](https://www.designabetterbusiness.tools/tools/business-model-canvas?utm_source=dbb&utm_medium=link&utm_campaign=Business%20Model%20Canvas&utm_content=title) but also the [persona canvas](https://www.designabetterbusiness.tools/tools/persona-canvas) to better understand the people we were solving problems for.

I often find my self going back to old books and tools from my banking innovation days.

So what do our persona canvas look like for these two groups and how do they impact our cybersecurity notifications?


**Non-Technical/Money People**

![Persona-Money](/assets/img/persona-money.jpg)



**Technical people**

![Persona-Tech](/assets/img/persona-tech.jpg)


Now we can use these two persona canvas to drive how we would describe the RDP issue to the two target groups.

___

### Non-Technical notification

**Subject/Title**: Security issue discovered in a device associated with your organization.

**Body/Content**: When scanning the devices associated with your organization, we detected the usage of a service that we see being attacked by hackers and used to deploy malicious software that can result in a ransom or data loss. We are here to help. 

We have already forwarded a full technical debrief to the associated technical contact of your account. 

Your devices will continue to be scanned on a daily basis, and upon detection of correction of this finding you will receive a separate notification letting you know this has been addressed. 

For your own reference and in case you want to follow up your with your technical contact, the issue discovered has been assigned the code **XYZ-123**.

As a reminder this type of issue is covered by your policy with the number 123456 and the technical contact on file is techdoe@acme.org.

___

### Technical notification

**Subject/Title**: Critical security issue detected in IP address associated with your organization

**Body/Content**: When scanning the devices associated with your organization, we detected the IP address XXX.XXX.XXX.XXX (with associated DNS subdomain xyz.acme.org) running RDP on port 3389. 

RDP is a service that we have seen as one of the most attacked and used vectors of compromise that lead to deployment of ransomware. For more information about our findings on ransomware please visit [justsaynotordp.com](https://justsaynotordp.com).

**The associated remediation for this type of issue is as follows:**

We advise that RDP is not directly exposed to the internet. RDP should only be accessible via VPN and should be completely firewalled from direct internet access, even if using NLA. 

Alternatives to RDP can be found in [Logmein](https://www.logmein.com) and [Teamviewer](https://www.teamviewer.com/en/).

A high level overview has been sent to the business contact associated with your account and the ference code **XYZ-123** was attributed to this finding.

Your assets will continue to be scanned on a daily basis, and upon detection of correction of this finding you will receive a separate notification letting you know this has been addressed. You can proactively login into the [Attack Surface Management](https://asm.binaryedge.io) platform and trigger a scan after having fixed the associated issue. 

If you feel you might need help addressing this issue or that it might be some sort of erroneous information please contact us on security@bla.com.

___

## Analysing notifications

If we compare the two notifications we can easily see how they differ.

The technical notification contains a lot of technical indicators such as IP address and the port running, and even that it is a critical security issue, while the non-technical notification avoids mentioning technical jargon that would not be useful for the individual, while providing him with a uniquely generated code in case he wants to follow up internally.

We give the technical individual clear guidance of what the issue is, where it was found, and how he can remediate and check that remediation was correctly applied. We also provide a contact in case he needs further help.

For the non-technical notification the focus is on making sure that the user is aware, but that there is no need to panic, we tell him there is an issue, but that we have notified the people that can fix it, that he is covered under the current policy and that we are there to help. We avoid mentioning the word "critical" as to not cause panic (which is a feeling that tends to be unhelpful when it comes to security issues).

In both situations we presented a message that focused on a sensitive issue that affected their **needs** but always with messaging adapted and focused on helping and giving the different users explanations that were phrased in a way that didn't feed into their **fears, headaches** or **negative trends** and while being on their level of technical understanding.


## Conclusion

We've seen how we can use personas to drive communication and product decisions that will benefit our users. I intend to find more tools similar to these that can help me do a better job, build better products and focus on my end users.

These tools help structure my mind and help me think and one of the best things about my job is that I get paid to think. 

Think about how to talk to our end customers about complex technical issues, how to break it down for them in a way they understand the impact this can have on their organization and I get to think about how a customer might interact with our products and features.

The other best thing about my job? The team around me. I can't do any of this without them.

My team of developers who is never afraid to build, what sometimes might sound like crazy experiments that I ask them, when trying to find alternative ways for users to interact with our data and platform more easily, like the example you see in the following image, where we built a bot that can give you responses about technological and security findings based on a natural language processing interaction:

![alfred](/assets/img/alfred.jpg)


I get to collaborate with people like Karl Schultz, who does amazing customer interviews and really digs deep into building personas that help us understand who our customers are, their needs and desires, and how to build the most customer centric produts and reports, or Ashley Slate, that has an enviable customer obsession on how well images and the message they are meant to transmit fit into the overall work that we are doing. (Don't believe me? [Download](https://www.coalitioninc.com/blog/coalition-releases-new-2020-cyber-insurance-claims-report) the claims report we just published, pay attention to the art work.)


## Hiring
If this sort of problem interests you, or you would like to join a team that is building the future of cyberinsurance, while tackling the ["small" task of solving cyber risk](https://www.coalitioninc.com/blog/why-we-acquired-binaryedge), we are hiring across multiple positions, teams and geos. Check out our current open jobs [here](https://jobs.lever.co/coalitioninc).