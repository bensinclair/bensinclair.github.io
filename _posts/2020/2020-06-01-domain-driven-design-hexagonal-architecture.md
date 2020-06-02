---
layout: post
title:  "Why we use Domain-Driven Design and Hexagonal Architecture"
description:  "Thoughts on why we use Domain-Driven Design and Hexagonal Architecture at Tithe.ly and the pros and cons."
tags: [ programming ]
date:   2020-06-01 15:38:00 +1000
excerpt_image: /assets/images/dave-pe8TXM7j_q8-unsplash.png
excerpt_image_credit: Photo by Dave on Unsplash

---

We have been using Domain-Driven Design and Hexagonal Architecture for several years in both legacy and newer products we are building. This post is dedicated to why we use Domain-Driven Design and Hexagonal Architecture.

![{{ page.excerpt_image_credit }}]({{ page.excerpt_image | relative_url }})
<small>{{ page.excerpt_image_credit }}</small>

One of our engineers, Josh McRae made the call all those years ago to utilize these approaches and I'm glad we did. Since then, he's been leading the way with leading in this area as well as providing education.

Engineers who come to work at Tithe.ly may not have been exposed to Domain-Driven Design so I had Josh write up some documentation around it to help educate them. I figured this would be good to share. 

The below text is all written by Josh (minus the quotes).

> ### Domain-Driven Design
> 
> **Why Domain-Driven Design?**
> 
> Domain-Driven Design is an approach to software development that places focus on the model of the business problem being solved and allows both technical and non-technical people to participate in its discovery by way of a shared language called the 'Ubiquitous Language'. Once a model has been established using this language, it can be turned into readable code using a common set of building blocks. This process lends itself to Agile Development methodologies particularly well as the model can grow in response to product iteration.
> 
> The process for discovering a model and implementing a solution in code will be discussed step-by-step in the following sections of this book. Alternative approaches will be used to explain the motivations for Domain-Driven Design where possible.
> 
> *The most significant complexity of many applications is not technical. It is in the domain itself, the activity or business of the user. - Eric Evans*
> 
> **Discovery**
>
> Modern software development involves heavy iteration - it's rare to see a project reach its final form, if that even exists, after a single cycle of planning and execution. Market demands shift, assumptions are challenged and understanding changes. Discovery is happening before the first line of code is written and continues well into project maturity.
> 
> A shift in understanding can only come through feedback, however. This may come from a change in requirements driven by end-users, more sophisticated design from a product owner, or a developer finding that code they tried to implement is logically inconsistent. Discovery is thus a collaborative process and familiar to anyone who has practiced an agile development methodology.
> 
> A byproduct of this ever-evolving understanding is a mental model that gathers together the business rules and relationships to be expressed in code and corrected by an ongoing process of refactoring.
> 
> ### Hexagonal Architecture
> 
> While developing new software and refactoring legacy code, we should aim for loose coupling and high cohesion in the codebase; software components should have little direct knowledge of the inner workings of other components and each module should have a clear and single purpose.
> 
> Domain-Driven Design results in a layer of software that is already highly decoupled from the rest of the system. Business rules exist in isolation from the UI, persistence details, and third-party services and as a result, are easily (and efficiently) tested.
> 
> Most modern web frameworks for PHP are based around the Model-View-Controller pattern. The purpose of each layer could be summarised as
> 
> - Model: Coordinates domain operations, including querying/persistence concerns
> - View: Provides facilities for user input and renders information about the model
> - Controller: Accepts commands from the view, triggers behavior in the model and queries the model for output
> 
> Each of these layers has a certain level of dependence on the others, and each has more than one purpose. Each action that can be performed by the application is bound to the controller coordinating it and the model is responsible not only for business logic but also persistence.
> 
> We can decouple these layers by introducing a rule about dependencies:
> 
> *High-level modules should not depend on low-level modules. Both should depend on abstractions. Abstractions should not depend on details. Details should depend on abstractions - Robert C. Martin*
> 
> Enter Hexagonal Architecture (also known as Ports and Adapters).
> 
> ![Hexagonal Architecture]({{ '/assets/images/Hexagonal-Architecture.png' | relative_url }})
> 
> The outer layers may only depend on inner layers. Inner layers must not depend on outer layers. Each layer is defined as follows.
> 
> **Infrastructure**
> 
> The Infrastructure Layer contains code that interfaces with application infrastructure - controllers, UI, persistence, and gateways to external systems. Many of the objects found in this layer will be provided by a web framework or persistence library. Concretions of domain repositories are placed in this layer while the actual interfaces are defined in the domain layer.
> 
> **Application Layer**
> 
> The Application Layer provides an API for all functionality provided by the application. It accepts commands from the client (whether web, API, or CLI) and translates these into values understood by the domain layer. As an example, a RegisterUser service would accept a Data Transfer Object containing a new user's credentials and delegate responsibility for the creation of a user to the domain layer.
> 
> **Domain Layer**
> 
> The Domain Layer contains any core domain logic. It deals entirely with domain concepts and possesses no knowledge of the outer layers.

That's a lot to process but I trust it makes sense :)

I recently got my hands dirty again with code (it's been a while) and started building a product using these approaches. I wanted to share some of my perspective on why I think we made a good choice.

### Shared (ubiquitous) language for everyone
Domain-Driven Design emphasizes creating a shared language for domain experts, programmers, and users. This shared language is used from the planning phase into how programmers write their code. 

Having a shared language removes ambiguous language from the mix and helps all parties have a clear understanding as the domain evolves. 

### Focuses on defining the domain and the problem being solved
We are building software for humans to use. Domain-Driven Design focuses on defining the domain and what problems need to be solved for real-life use cases. 

Rather than thinking about how you're going to structure your database tables or your API endpoints upfront, you're thinking in use cases or user stories.

### Great for documentation
Because you're using the shared (ubiquitous) language as you write code, it makes it easy for others to look at the code and understand what's going on. For example, verbs that you'd use in real life to explain a use case would be used when writing the code.

### Clear separation of layers
I really love how Hexagonal Architecture separates the Domain, Application, and Infrastructure layers. This sets some clear boundaries around how everything interacts and helps prevent programmers from creating complexity in their code if approached correctly.

### Great for flexibility and refactoring
Software is often complex and the domain evolves over time. Without a good approach to how you design your code, technical debt can pile up. 

I've loved the ease of refactoring in Domain-Driven Design code using Hexagonal Architecture. The separation of layers and the quality object-oriented design makes it easy and painless when it comes to continual improvement.

### Feels like more code than needed for simple CRUD
One downside is it feels like there's a lot of code for simple CRUD needs. 

We've helped combat this at Tithe.ly with simple code generation tooling that builds the different layers and unit tests required. This allows us to pump out simple CRUD code effortlessly so we can focus on the real problems.

### Cost in efficiency
Domain-Driven Design makes it super easy for development but it does come at a cost in code-efficiency. 

Quantifying that is hard but the way I see it, I'd rather spend a little more on server costs to make up for the lack of efficiency rather than having a codebase that is hard to maintain and slow to iterate on.

### Closing off
So there is a little insight into why I've enjoyed working in Domain-Driven Design and Hexagonal Architecture. No approach is ever going to be perfect but making sure you have an approach to help the software you build to be maintainable in years to come is so important.