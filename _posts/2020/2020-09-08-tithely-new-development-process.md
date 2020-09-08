---
layout: post
title:  "Our new software development process"
description:  "Insight into how we are changing our software development process to bring more value to our customers."
tags: [ software development, programming ]
date:   2020-09-08 14:54:00 +1000
excerpt_image: /assets/images/chris-lawton-c0rIh0nFTFU-unsplash.png
excerpt_image_credit: Photo by Chris Lawton on Unsplash
---

Building software is hard. It's an uphill battle and you need endurance as the software matures. Building software is also super satisfying and such an amazing adventure, especially when you start seeing momentum as well as a multitude of happy customers. I think the best software companies aren't the ones who write the best code but those who can make really good decisions on where to dedicate their time.

I've been running a software company for over 10 years now, 2 of the most recent years as the CTO of Tithe.ly. This article is a little about my journey and what we are doing that's producing strong positive results here at Tithe.ly.

![{{ page.excerpt_image_credit }}]({{ page.excerpt_image | relative_url }})
<small>{{ page.excerpt_image_credit }}</small>

## A view of my software development journey

### The early days
I started a software company called [Elvanto](https://www.elvanto.com) a little over 10 years ago. I was 19, full of energy and motivated and I felt called to build software for the church. It started as a Volunteer Scheduling tool which soon developed into a fully-fledged Church Management platform. Little did I know I was building a SaaS startup.

With no formal training in software development, I was lightning fast. I pumped out features like there was no tomorrow. Customers were blown away and loved the product. Building software was fun!

After a few years of development on my own, I branched out and hired my first couple of engineers. It wasn't long after they started that the technical debt I had created unwillingly started to show. With a lack of structure, decoupling and unit tests, the code I had built was your typical [big ball of mud](https://en.wikipedia.org/wiki/Big_ball_of_mud)...

So we set out bringing structure to the code to modernize it and make it easier to build. Big shout out to [Paul Jones](http://paul-m-jones.com/) and his book [Modernizing Legacy Applications In PHP](http://mlaphp.com/) for setting a path for us at that time.

### Adding a software development process
The behind the scenes changes we implemented from the above section meant customers weren't seeing new and improved functionality in the software like they were used to. By now we had a few engineers in the team so we decided to look for better ways to build software so that we could move faster and bring value to customers. 

That's when I found [Scrum](https://www.atlassian.com/agile/scrum). It was an a-ha moment for me! I became the Product Owner, our customer service employee Hannah did some training and became the Scrum Master and we had our dev team. The structure was good but we were horrible at estimating and our sprints always blew out. After several months, morale was low at the end of sprints. Again, I went searching for a better way. 

I then stumbled across [Kanban](https://www.atlassian.com/agile/kanban) ([a video](https://www.youtube.com/watch?v=-Rsmdg9NY80) by the guys at [Thrillist](https://www.thrillist.com/) really inspired me). Kanban suited us greatly because there were always so many unknowns every time we took on work, bugs would pop up out of nowhere, there were fewer meetings - all-in-all, it was awesome! We implemented [Work In Progress limits](https://www.atlassian.com/agile/kanban/wip-limits) as well as some good processes to help our workflow. We felt productive at this point.

Reflecting on this time, me being a Product Owner and a developer, I felt I made bias decisions that were more code-focused than customer-focused. We refactored more code and tried to build for all the use cases. Even with proven processes in place, we were still not moving at the right speed and the backlog of feature requests was starting to pile up.

### Scaling products and teams
When I came on as CTO at Tithe.ly, I stepped away from the day-to-day runnings of Elvanto and focused my energy on the greater team which I have been blessed to grow from a handful of devs to now a team of about 40. We had several dev teams, some working on legacy software and others on new software. Again we needed a process. 

Kanban was working well at Elvanto but we were maintaining a product. We weren't building anything from scratch. With the new software we were building, we wanted to impose some deadlines so we felt to try Scrum again, with it's fixed sprints to help keep us moving. This time we took Scrum head-on with a dedicated Product Owner and Scrum Master. Again the structure was good but we just didn't seem to be moving quickly enough. Morale dwindled as time went on. We still had a habit of not understanding all the pieces, we went down rabbit holes, spent time on the wrong things, and had to try to explain to leadership why we were taking so long. 

The same old problems were appearing. Something had to shift.

## A change in mindset
Before reading [Ryan Singer's](https://www.feltpresence.com/) book [Shape Up](https://basecamp.com/shapeup), the team at [Basecamp](https://basecamp.com) seemed to have all their ducks in a row. They were productive, they released great features, their customers loved them, so did I, they were just so practical in everything they did. 

After reading their book, something that stuck in my mind out of everything was "fixed deadline, variable scope". In simpler terms "build the best version you can in the time you have been given".

It struck me, I'd been doing it all wrong. I realized all along it wasn't the processes that were failing, it was the mindset. I was promoting "build the best version you can" and this flowed into how we planned out a feature (which was generally over baked and solved every edge case under the sun) and how we wrote our code (we spent too much time on unimportant things).

## Fixed deadline, variable scope
I was starting to get a grip on things as Tithe.ly's CTO so I had an opportunity to go back to Elvanto and see how I could bring this new mindset to the team. 

The team was still chugging along with Kanban and they were so inefficient. Without the right mindset, that team had become less focused and even less productive. They were context switching all the time and tasks that should take a week literally took 3 months. 

One of the biggest things I noticed right away was their mindset. It was the exact mindset I had left them with a couple of years earlier. They continued on from what I had started and it was killing the team. I was so frustrated and upset at myself. I'd left the worst kind of legacy in that team.

So I set out on a journey to first change their mindset and secondly implement a process that allowed the team to become focused and productive. 8 weeks later, that team had shipped two pretty decent features all thanks to a change in mindset, a complimentary process, and some strong leadership. What was a very unproductive team became one of our most efficient teams here at Tithe.ly. This blew my mind at how quickly things had turned around and I was excited to try the process out in other teams.

## Our new process
Our new process is mainly using Shape Up with a sprinkle of Scrum. We don't follow either exactly and have tried to come up with a process (that we'll tweak as we go) that suits our business model and structure. 

Big thank you to [Dan Irmler](https://www.linkedin.com/in/daniel-irmler-4466b290/) and [Sarah Schelbach](https://www.linkedin.com/in/sarah-sinclair-schelbach/) who have spent countless hours putting an overarching process together for our team. I'm not going to go into the whole nitty-gritty today but talk about some of the high-level changes that can easily be implemented into any team.

### Pitches
The word "Pitches" can sound like a buzz word. But from my experience, these little beauties are huge game-changers. If you haven't read Basecamp's [Shape Up](https://basecamp.com/shapeup) book, do it as soon as you can as it goes into great detail on their process which we have mostly adopted.

Pitches empower us to:

1. Truly understand the problem we are trying to solve
2. Encourages us to think through what a solution would be
3. Forces us to think through and remove rabbit holes and no-goes (what to avoid doing so we can meet the deadline)
4. Decide on our appetite (how much time we want to dedicate to the scope of work)

All questions and clarity need to come before a pitch is finalized. So we encourage our Product Owners to flesh out the pitch as best they can. They then run it by our dev team who can ask questions and the pitch can be updated as more clarity comes. 

The goal of a pitch is to present a document to our stakeholders and dev team that gives complete clarity on what we are building and what the deadline is based on the appetite.

![Example of a Pitch]({{ '/assets/images/pitch-example-group-finder.png' | relative_url }}){:.image.portrait}

### Betting
We want to make sure whatever we are pitching has stakeholder support. We have taken on the [Bets, Not Backlogs](https://basecamp.com/shapeup/2.1-chapter-07) and [The Betting Table](https://basecamp.com/shapeup/2.2-chapter-08) approaches from Shape Up to get stakeholder buy-in but I won't share about these in detail as the book explains them well.

### Developer Scope Mapping
When a pitch has been bet on, before we start work, we break the solution in the pitch into bite-sized chunks. It's very similar to what the Shape Up book talks about in their chapter about [Map the Scopes](https://basecamp.com/shapeup/3.3-chapter-12). Jeff Patton's idea of [User Story Mapping](https://www.jpattonassociates.com/user-story-mapping/) was what first inspired this before reading Shape Up but I think Basecamp's approach to how they explain it is more digestible.

Anyway, getting back on track, this step is extremely beneficial to get a birds-eye view of a pitch before conducting our full planning.

![Example of a Developer Scope Map]({{ '/assets/images/developer-scope-map-group-finder.png' | relative_url }}){:.image}

### Sprint Planning
Now that we have a very clear picture of what we are building and a fixed deadline, we can plan out the work. Right now we work in sprints to bring structure and consistency across our teams. We no longer have the Scrum Master role and Product Owners are now less/not involved in sprint planning because they did all the hard work in the pitch.

During sprint planning, we use Story Points to predict effort involved in each task with the primary goal of creating discussion. If one dev says a task is small and another says it's large, this opens up and opportunity to talk, bring clarity, and get on the same page. 

Note: We are toying with ideas but Story Points is likely not going to be our KPI like it is in Scrum.

### Building
Even though we've planned out the sprint, things can change. That's where variable scope comes in. We adjust the scope if we feel like the deadline is slipping. This is a key factor that I failed to realize when doing Scrum. Not getting all the tasks done was like failing in Scrum. The shift now is we only fail if we don't deploy a version of what we set out to build. 

Some things we do to help meet the deadline:

- Do not, at all costs, build anything out of scope
- Be more relaxed on code standards and avoid having team fix unnecessary things (auto-lint and fix where possible!)
- Don't allow code reviews to block progress, set your team up so they can keep moving
- Try not to over bake unit tests and focus on what is most important to test
- Avoid refactoring code as much as you can
- Add tasks that aren't imperative to release a body of work to a list that can be completed in a cool down week
- Cut out features completely from the scope

On the flip side, if we are ahead of schedule, we might be able to add some niceties in as long as they don't blow out the project.

### Shipping
Work isn't done until it's deployed into production. We want whatever we work on to be in customer's hands by the end of the deadline. This needs to be factored in.

### KPIs
Our KPI will be whether we shipped the best version we could create in the time we had. 

This shifts our thinking from "how much can we squeeze out of the dev team in x time" to "we are going to ship in x time". 

The latter is where true value comes:

* There is a calm and a healthy motivation in our dev team
* Our customers get value in us releasing a finished, complete version of what we were trying to build.

### Cool Down Weeks
Cool down weeks is a 2 week period where the dev team can do whatever they want inside the product they are working on. We encourage this every 6-8 weeks. This allows the dev team to go back and refactor code, make improvements, fix bugs, implement tooling, etc. 

By having this time set aside, engineers can focus on sprints and still have a space to tinker in cool down weeks. It also helps the mental state of engineers who are used to perfecting everything knowing they have the time they can do this.

## Closing off
I encourage you to check out Basecamp's [Shape Up](https://basecamp.com/shapeup) book. I am not getting paid a cent by those guys, this is all purely based off my experience and gratitude to their generosity of sharing knowledge freely.

We are seeing some great momentum happening by applying this process, mostly formed from Shape Up's teachings. Every company is different so we are testing and refining as we go. But with everything we do, "fixed deadline, variable scope" is at the front of our mind.

If we could only do two things, pitches and the mindset of "fixed deadline, variable scope" are hands down the powerhouse players in this whole shift. Building the right things and getting them deployed to customers is the greatest thing a software company can achieve.

I encourage you to dig deep and see how you can create a high output and high-value dev team at your company.