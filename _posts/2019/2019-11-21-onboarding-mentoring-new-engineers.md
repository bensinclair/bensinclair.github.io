---
layout: post
title:  "Onboarding and mentoring new engineers remotely"
description:  "Hiring a remote engineer is one thing but what are some practical ways to onboard and mentor them?"
tags: [ mentoring, onboarding ]
date:   2019-11-21 20:40:00 +1000
excerpt_image: /assets/images/mika-matin-mmylzhpso2i-unsplash.png
excerpt_image_credit: Photo by Mika Matin on Unsplash
comments_id: 4
---

Onboarding engineers is generally an afterthought for most engineering teams. When you start a project you're not thinking about how new people are going to be introduced in the future. It's one of those things I think everyone wants to spend time on but let's face it, we are too busy coding. This post talks about some practical ways you can onboard engineers and ensure they are mentored in a remote environment.

When we built our first onboarding process, we started it after we offered a new engineer a position. We scrambled to compile information before they started and tried to stay at least one step ahead of them. Relax. You don't have to have it all figured out.

Here are some ideas of what an onboarding process could include...

![{{ page.excerpt_image_credit }}]({{ page.excerpt_image | relative_url }})
<small>{{ page.excerpt_image_credit }}</small>

## New engineer preparation checklist 

Think through what needs to prepared before an engineer's first day. Create this checklist so you can refer to it each time a new engineer is about to start.

Some things to consider adding to your checklist are:

- Creating an email address for them
- Inviting them to software platforms you use
- Purchasing licences for any software they may need
- Sending a welcome email a day or two before they start

## Computer set up docs

Getting a new computer set up with all the software is a huge time sucker and can take a big chunk of an engineer's first day. So we created a new computer set up guide. We leveraged the power of Terminal on macOS (command prompt on Windows) to run automated scripts to install dependencies and required software.

Here's a quick example of our macOS new computer set up docs:

> Step 1: Install Homebrew
> 
> ```
> /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
> ```
> 
> Step 2: Install Python
> 
> ```
> brew install python
> ```
> 
> Step 3: Install Node
> 
> ```
> brew install node
> ```
> 
> ...
> 
> Step 9: Install Required Software
> 
> ```
> curl -s 'https://api.macapps.link/en/slack-github-chrome' | sh
> ```

The above cuts down a new computer set up by hours! My advice is to keep the instructions simple and doesn't have too many things running in each step in case one fails. 

## Required reading list

No doubt you will have common ways you do things whether it be how you code, how you communicate, general expectations and so on. New engineers must understand this early on. 

Required reading materials might include things like:

- Expectations
- Code style
- Documentation on libraries/frameworks you use
- How you approach writing tests
- How you except pull requests to be written
- Understanding your workflow
- Training videos on your software development methodology 
- Tooling you use

## Consider creating some training exercises to learn how you code

You probably follow some coding style and framework. If a new engineer jumping head first into your code is a steep learning curve, consider creating a small training exercise to help new engineers become familiar with your codebase without having to dive into the real thing.

Some of our products at Tithe.ly follow the [Domain Driven Design](https://en.wikipedia.org/wiki/Domain-driven_design) software development approach which is a powerful way to build software but can be a learning curve for engineers who might be more familiar with other models. 

Our lead engineer [Josh McRae](https://twitter.com/joshmcraeau) created a training codebase (dubbed [Kata](https://en.wikipedia.org/wiki/Kata)) we could give to new engineers. It contained unit tests that were pre-built and some base infrastructure. New engineers were to read the material we provided them about Domain Driven Design and then build out code to satisfy the unit tests.

As part of this process, we had a [Jira](https://www.atlassian.com/software/jira) Kanban board with tasks outlining the process. This was a great opportunity for new engineers to not only learn how we code but to learn our workflow, code review and QA processes. It also promoted our ♥️ of test-driven development.

When engineers finish our training exercise they are more than equipped to enter our real codebase and start contributing effectively.

## Create a mentorship and buddy program

New engineers need help from other staff. This can be time-consuming and normally it's left to a more senior or lead engineer who spends a few weeks of their time answering questions to get new engineers off the ground. This proves to be a huge hit to productivity.

We feel it's important to have a more senior or lead engineer involved in the process but they shouldn't be the go-to person for every question. That's why we created a mentorship and buddy program to set new engineers up for a win.

The way it works is a new engineer is assigned a mentor and a buddy. 

The mentor is the more senior or lead engineer. They meet with the new engineer on their first day, talk through what their first weeks will look like and set some measurable goals. Mentors generally check in once every week for the first month and then as per needed from then on.

The buddy, on the other hand, can be any engineer in your team. They just need to be at least one step ahead of the new engineer. The buddy's sole purpose is to help the new engineer get up to speed as quickly as they can. 

You don't have to be in the same room to make this work. Video calls and screen sharing is a perfect solution to the remote environment.

A couple of takeaways:

- After onboarding, a new engineer, that same new engineer is a great candidate to become the next new engineer's buddy. We find being a teacher after being a student helps solidify their knowledge.
- Continuous feedback is super important. Having a buddy at hand and weekly meetings with a mentor, this allows for things to be nipped in the bud quickly.

## First-day checklist

The first day of a new engineer can be overwhelming for them to say the least. We've always tried to not make the first day too overwhelming but that's hard to avoid. 

Some things to consider for the first day are:

- Meeting the team
- Understanding the culture
- Computer set up
- Ensuring they have access to what they need
- Reading any required material

## Wrapping up

There you have it! No process is perfect and you'll always be refining. Just get started 😜
