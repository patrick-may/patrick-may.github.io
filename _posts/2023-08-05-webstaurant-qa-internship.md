---
layout: post
title: Webstaurant QA Internship
date: 2023-08-14 12:00:00-0500
description: long-form ramblings about summer foray into qa automation industry work
categories: update
---

Summer 2023 is closing up! In an effort to confirm my knowledge and experiences from my summer internship, I will do my best to 'teach' is to the bottomless internet void!

# Prior

My internship search quite hectic. I think I applied to a couple hundred positions. I had a couple opportunities string me along for the better part of 8 months (which is a hiring critique for another time). Webstaurant was an opportunity I applied to later, and I have nothing but respect and positives to say about the recruitment process. Within 1-2 weeks I had a direct 1-on-1 phone call with a qa team manager! No multi step technical assessment prior to finding a real person, no HireVue, even the web application/resume drop portion was not excessive (I'm looking at you, financial orgs that have designed an in-house CMS such that wants to know the name of every pet rock I've ever had 😭). After our phone call, I had a very brief take-home technical assessment... and that was it for the hard part on my end. I cannot state how much it left me with a good feeling about the org to be legitimately given someone's attention during the hiring process.  

This tech role was a remote position, for which I recieved a large work-at-home supply drop about a week before starting. 

# Getting Started

My summer experience started relatively quietly. Going into this internship, I had no prior experience with any quality assurance work. My first week started with a few small orientation sessions, and then I was working through a training bootcamp. Webstaurant has an Automation framework build off of Selenium, wrapping in the JVM language `Groovy`. As someone who has never used Groovy before and hasn't done significant work in Java before either, there was a learning curve to Groovy scripting, and the in automation framework. 

Training involved working through pre-solved practice QA tickets. I have always personally been more interested in back-end development work, so working on emulating how a human interfaces to the front-end also took some getting used to. The main thing here was learning the concept of `XPaths`, and finding elements in a website's DOM in XML form. I am sure this is something trivial to many, but it was a first for me!! I didn't even know that chrome dev tools allowed one to `ctrl-f` and search for an xPath -- I was just interpolating the raw html and utilizing the JS console to see if my xpath was valid. (I eventually learned there are vastly superior ways to finding and checking XPaths).

My QA team was a group of around 10-15 people, with one manager, a team lead, and a distribution of different levels of analysts and automation engineers. Team dynamics were overall very positive and supportive. Our team loosely followed an Agile methodology, with daily standups, weekly checkins and sizing meetings, retrospectives after sprints, etc. etc. Whenever I faced an problems, I always recieved help as long as I asked for it. Knowing when to ask and when to grind is an impossible question (elaborated on further below).

# Day to Day

In all honesty, day-to-day work was quite routine. Our team had standup, which afterwards I worked individually on whatever automation tickets I had on my plate for that sprint. After breaking for lunch, I had another substantial block of time to focus on individual work. In the last few hours of the day, our team had '`office hours`', which boiled down to a groupwork/troubleshooting/socialization space. Plus/Minus an additional meeting or two each day, and that was the general routine! If anyone has more specialized questions about working at Webstaurant, feel free to DM.  

Automation tickets for me were pulled from an **existing backlog** of sized Product Backlog Items (PBIs). During my ~10 week internship, I completed around 15 PBIs with an average size estimate sitting between 5 (18 hrs)/ 8 (30 hrs) of effort per PBI. Aside from individual work, I also contributed in weekly sizing meetings that built our backlog of automation PBIs. 

# Internship Specifics

Along with my regular work, there were a couple additional responsibilities and opportunities that were available just to summer interns. As an intern, Webstaurant offered various professional development opportunities in both small and large group intern sessions. I enjoyed most getting to participate in a Q & A with upper management (large intern session) and discussing company cultures in a small roundtable setting. Perhaps this was my small liberal-arts school leanings coming out to play, but getting to set time specifically aside to work on analyzing other companies structure and introspect about the environment I believe I would thrive in was an exceptionally fun time and great surprise. This may be semi-typical intern socialization/professional development stuff, but it was a very welcome surprise to me. 

# Maturing as a Dev 

I always struggle walking the line of reporting and sharing my experiences while staying away from the LinkedIn style humble brags that are ubiquitous on that platform. (👋 If you are coming from my LinkedIn post about this). In my prior summer, I has many opportunities to mature as a 'student' -- hanging around other upperclassmen in the same field, at different universities broadened my perspectives on what academia can be for different people. Since I was living with roommates on Carnegie Mellon's campus, socialization was an easy, notable aspect of that program (as we were practically forced to socialize by proximity). The research that I conducted I believe was good (and I learned a ton about the process), but I ended up not doing much 'technical' work as part of the research -- I was doing a lot of qualitative analysis, scheduling/review board logistics, etc. etc. I concluded that summer saying that I knew pursuing further academia held some positives, but also had its own flaws. I resolved to work an internship in industry my next summer so that I could sample both post-undergrad opportunities. The industry application process is a blog post for another time, where I can separate my current company optimism with a much more critical systemic analysis. Long story short -- I ended up with a QA Automation internship at Webstaurant.

## Development at Scale 

One of the biggest realizations that I think one *has* to experience (as opposed to just being told) is that of development as a part of a much larger organization. When doing research in the summer of 2022, I was the research team -- quick fixes, todos, and tasks were all things I managed (in my head...) as a one man team that was getting advice from an external mentor. Or various school projects. The largest group project I've worked on in school was a semester long mobile app on a 3 person team. Compare that to this year, where I am on a multi-person team ($>3$), that is only a small part of QA, that is itself a part of the software division. *Much, much, much* developer person-hours being invested in parallel. 

- Version control becomes much more needed.

Sure, a trivial statement to any industry-wisened dev, but something worthwhile for us academic scrubs still on the learning curve. I got to experience multiple **Code Reviews** as I went through the process of Pull Requests. As a student and on one-man passion/personal projects, I have not really seen the use in pull requests before, and only semi-recently come into an understanding as to how useful branching can be. To the 2 people who have made it this far -- I do now know each of these version control structures' uses. I promise. 

- Projects need structured management 

Everything needs to be managed, even small projects. What was a noteworthy realization to me over my internship was the value in *some* team meetings and spending non-trivial time tracking progress and synchronizing work. Agile has many flaws, as does development system. However -- an anarchical style of 'everyone work on as much as they can, and glue it all together before the due date' of school projects completely breaks down when a project is instead a *product* that has to be maintained and iterated upon.

- Writing Code is typically the easy part 

Was the biggest idea I had to come to terms with. I wholeheartedly lean into being a 'programming nerd'. Making some random tool or visualization is fun! Getting stuck fighting an esoteric programming language construct for an afternoon is a positive because afterwards you get to ~~brag about it to all your friends and coworkers endlessly~~ write a blog post about what cool thing you just learned. In my industry internship experience that was primarily scripting QA tests, understanding the original manual tests is the hard part. Finding all the different sections on a webpage is tricky. The **scripting** itself doesn't require any fancy computer science theory or elegant terse solutions. Understanding where one's script and code fits into the larger software system, its acceptance requirements gets messy, quickly.

# Developing a Developmental Disposition 

(...Alliteration is fun...)

As an Intern that was stepping into an industry position, I tried to **make purposeful effort to learn new things**. Sure, this seems trivial, but perhaps I can quantify this buzzword soup into something a bit more practical. If there are multiple ways to do something, I would always try to take the path I was less comfortable with. (There are exceptions to this, but listing them is no fun. Obviously, common sense is required when one is about to make purposeful decisions that are short-term suboptimal.) 

As I was getting starting working in a new language and new IDE (IntelliJ), I purposefully made the decision to switch my keybindings towards `Vim`. JetBrains IDEs have `IdeaVim`. I was definitely slower for the first two weeks in writing code. But I was going to be slow anyways! I hadn't used a heavy IDE in a few years, and was writing in a language (`Groovy`) that I hadn't ever used before, extending an in-house framework that I (obviously) never worked with before either. 

When working through already-solved practice scripts, I tried to lean on `Groovy`'s builtin structures compared to what base Java would give me. This sometimes led to some really cool discoveries and design discussions (such as the `.&` bound method operator, `?:` elvis operator exists, etc.) but also led to wasting time tracking down that `Set<String>` as a return type will return a `Set<GString>`s as a regular set of strings but not type coerce the groovy strings even though the return type...... ugh. Suboptimal short term decisions don't always have immediate positive payoffs. Some don't bear any fruit (ever). I don't think this is a bad thing, just a part of the growth process. I obviously now understand, much more than I ever wished to, how GStrings lazy properties mess with their hash values, compared to Strings in Java. I *also* have a refined process of how to debug certain weird oddities that a program is throwing at me.

# Closing Thoughts 

This past summer I spent it at a great company with a lot of surprising benefits. In retrospective introspection (big word = smart 🤓), I have matured a ton as a developer throughout the summer. 

This post was written over multiple weeks while I was in various states of juggling other responsibilities -- so if anything feels half baked or you would like to discuss further, please reach out! 
Until the next time I guilt myself to write a blog post, farewell. Maybe I'll make some DevLogs about my senior thesis project. Maybe.

