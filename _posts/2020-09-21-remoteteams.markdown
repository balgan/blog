---
layout: post
title:  "Quick guide on remote engineering teams"
date:   2020-10-04 02:56:18 +0200
categories: management remote engineering
---

As I write this post I have now managed a fully remote team for more than 6 years. 

Due to the current circumstances that exist in the world, lots of organizations are now dealing with teams being fully remote without being prepared for it, and Im having friends reaching out to me for advice on how to manage their remote teams, how to keep them happy and engaged and productiviy high.

On this blogpost I will **not** give advice but rather write down what works for MY team. It's up to you to figure out if it works for yours or adapt it in a way that works for you.

My current team consists of:
* Me - Switzerland
* 8 people in Portugal
* 2 people in the USA
* 1 person in Turkey
* 1 person in Canada

# Recruiting

If you know you're going to be building a fully remote team, you need to set standards on recruiting people from day one. Being remote isn't for everyone and you need to make sure you're testing for this while interviewing candidates. For us at Binaryedge I always knew I wanted a fully remote team, so I worked with that assumption from the beginning.

In my experience someone that is prepared to work remotely, is extremely strong on the following skills:

* **Time management and structuring** - I am the type of manager that does not control what time you got in and got out. We focus on tasks, and come to an agreement on what we believe is a succesful set of tasks to be delivered in a certain amount of time. Being able to plan and tell me yes/no to the tasks am presenting you and then execute them on time is critical for the success of the contribution of each IC and to the work of the team overall.
  
* **Asynchronous communication** - When I leave you a message I do not expect instant response, I ask what I need to ask and you will answer when appropriate. You should expect the same from me and from your colleagues. We span across multiple timezones, with people that have families they should be spending time with or having out-of-work activities they enjoy, and you need to trust they will reply as soon as they feel appropriate.


* **Maturity in interpersonal relationships** - When you are unhappy with a colleague, you do not get in a mood, you do not pout or act out, you message that person and say "hey I was not happy about X can we talk?", if that doesn't work you immediately reach out to your manager and among the three you solve the conflict. 
  
    When discussing projects, you need to have your opinions formulated well and arguments prepared with data to back it up, this will make it easier to have a factual argument rather than one just for the sake of.


Some questions that I have used to help me recruit that act as checks for these skills are:

* "If you are the tech lead of a project, and during project planning one of your team members disagrees with a decision you made, how do you handle that?"

* "If a colleague was rude to another and you noticed that how do you handle that situation?"

* "How do you currently structure your work hours?"

* "if your manager asks you to plan how many tasks you can take from a list presented, how do you plan for it and decide how many tasks you are capable of executing?"

Finding the right people for a remote team takes a long longer than normal hiring. The other part I've found to be a little bit tricky is Junior onboarding. You need to have a really strong foundation of processes and people in place, before you gain the capability to successfuly bring on board juniors.

# Team and project management/planning

When deciding what we are going to work on, no single person makes a decision (me included).

### At the beginning of the year

 I sit with the leadership team, understand the business goals and accomplishments for the year, and agree on high level deliverables for the team. Then I bring those back to the team and we define our year roadmap broken down by quarter.

### At the beginning of each quarter

We look at the deliverables for the upcoming quarter and define the following:

* **A tech lead per project** - this is a person that is the point of contact for this project - Its important that when questions arise about the project not every engineer is distracted with random questions, so this person is the go-to. This person is responsible for keeping the project going, the tickets and board organized, and keeping overall quality across the project. This position rotates across different people over the different quarters so that everyone can gain more experience on management, leadership, project planning.

* **Team distribution** - some of us have skills that fit certain projects better. Is this a mobile app ? only some of the frontend engineers can do react native. Is this a project that requires knowledge of cybersecurity ? Not everyone in the team has it either. We all agree, together on what the optimal team distribution looks like.

* **Quarter review** - We review previous quarter, think about which tech debt we want to repay in the following quarter and what processes do we need to change/improve in the upcoming quarter.

### Every week

We have 3 meetings per week:

**Monday** (30 minutes) - Check across all projects that things are aligned and that everyone knows what they are doing.

**Wednesday** (1 min per person) - Quick mid week updates, in case anyone is blocked, quick action team is put together to help.

**Friday** (1 hour) - Retrospective of the week (what went well and what went wrong), thinking about following week and if projects are still on time and tasking distribution/order still makes sense.

### **1:1** 

One-to-one's are currently held once every 2 weeks, in those we discuss how the person is feeling about the team, work, and life in general. We go over any issues the team member wants to raise, and 

### **Tooling**

Each tech lead is responsible for at the beginning of the quarter put together an Epic with description of the project and all tasks broken down and assigned as dependencies of that project. 

The second artifact we build per project is the description page which needs to contain:

* Title of project
* Description
* Why are we doing this 
* What are the metrics used to measure success of project 
* Repos associated
* Documentation
* Tech lead
* Team
* Epic associated with project

Our board looks super simple, and consists of the following status:

* **backlog**
* **to do** - things that are going to be worked on this week/sprint
* **doing** - currently being worked on
* **done** - work is finished
* **deprecrated**



# Keeping team engaged and happy


### Game night
Once a quarter we do a team game night. I organize some type of game, we book a call with everyone and play some games together, either competing against each other or working together as smaller teams.

![team](/assets/img/team.JPG)


Some of the games that work well for remote teams:

* **Quiz night** - [ahaslides](https://ahaslides.com/) works well to make a quiz night with points
* **Guess who** - have people in the team write facts about themselves and then have others try to guess who it is based on the fact.
* [Skribbl](https://skribbl.io/)
* [Geoguesser](https://www.geoguessr.com/)
* [Jackbox Party Games](https://www.jackboxgames.com/party-pack/)

### Discord / Alternative IM

If in your day to day use slack, have an alternative IM system where the team can just chat about non works stuff. For us, we have a discord, we logon at night, play some games together, share a TON of GIFs, etc...

### Moon shot projects

On our team at the beginning of the quarter we define one or two moonshot projects, these are projects that involve a strong research component, and that while they can and should contribute to business gains, they are not as direct as the normal busines defined goals. 

We do put some restraints around our moonshot projects, typically the rules are:

* Can only last a quarter
* People only work on it friday afternoons
* Must still be a potential solution to an existing problem

An example project:

* Problem : We have a lot of business people that want to easily understand the security state of a company, but aren't technical enough to read all of our technical data or launch a scan.
* Potential solution: an NLP slack bot that reads requests in english and writes/describes technical findings in  a way that is easy to read.

This is a practical example of something we built as seen in the following screenshot:

![alfred](/assets/img/alfred.jpg)

### Offsites

Being remote is fun, and lots of people enjoy it, but bringing people together at least twice a year is something that we have found also works extremely well for team morale. We typically pick some conferences, we even deliver some talks and end up booking between 3-5 days for all of us to hang out, and just chat or potentially architect new products (no coding).


# Last remarks

There are a couple more things I feel are important to mention:

* Velocity on development does tend to take a little bit longer at the beginning while the team is figuring out each others rythms.

* Not everyone is prepared for remote work, you will make mistakes and unfortunately this comes with a cost as well (people will leave because they don't like it, or they don't perform to expectations and you might need to fire them).

* Isolation can take a hit on people after a while, make sure you are keeping tabs on the mental state of people in your team during 1:1s and to make sure you are supporting them in the best way that you can. 
