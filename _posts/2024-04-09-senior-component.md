---
title:  '"A few notes on reading Convex unique approach to AI\'s Backend-as-a-Service"'
date:   2024-04-09 10:20:00 # 4/10 16:25
layout: page
description: "James Crowling on database, rag, and dropbox - talk at Cerebral Valley"
# toc: true
# categories:
---

Q: You recently released a vector database as part of Convex’s product offering. How has the advent of generative AI shaped the trajectory of your product roadmap?

The simple answer is that we built vector search into Convex because there was demand for it. Perhaps the more profound answer is that we've been surprised at how well Convex is suited to AI applications. I have a belief that for the vast majority of AI apps, the hard part is building the app itself. There are a lot of AI apps where it talks to a model and uses vector search, but the thing teams find hard is to actually build the application around this desired product experience.

So, they need a platform like Convex - which makes it easy to talk to third party services, interact with models, provide vector search, run queries, and dynamically update client applications when data changes. While Convex was started before this boom in generative AI, it's turned out to be a surprisingly good fit for developers who want to move fast and build an AI application.

One thing I find fortunate is that `good abstractions tend to be evergreen`- how we interact with functions hasn't changed in almost half a century. Things like strong guarantees, strong invariants, abstractions that hide complexity - these are the building blocks that help developers move fast. The Convex roadmap doesn't change dramatically because it already fits in really well with modern development use-cases.

So of course, we'll make improvements to our vector search and continue to scale the platform, and we'll keep building support for larger teams. But, I don't see a tremendous shift in direction for the company because I think that good abstractions always have enduring value for developers.


Q: LLMs have introduced an entirely new paradigm of computing. How are you thinking about the shift from deterministic to probabilistic computing inside of Convex?

My model of the AI landscape is that LLMs are great at doing human tasks and computers are great at doing computer tasks.There's been a huge increase in efficiency from modern generative AI being able to come up with good approximate solutions to probabilistic jobs that once were the domain of humans. But, this hasn't reduced our reliance on logic and strong guarantees - things like databases, strong consistency, knowing your data is stored correctly and easy to interact with. Strong guarantees on the lower layers of the stack allow developers to move faster on the probabilistic stuff because they don’t have to deal with unexpected corner cases and ambiguity.

So, I think these two things go hand in hand. I don't think we should consider AI as a replacement for traditional systems engineering. In many ways, AI solves problems that humans are good at, but databases empower humans and AIs to do the interesting things that they do.

Q: What differentiates Convex from alternative BaaS platforms like Firebase and Supabase? What’s unique about the way you’re approaching this problem?

If you’re a startup founder, you are a capitalist building a business that has to make money. What will often differentiate your business is the data that you store, the users that you maintain, and the quality of the product on top of that. The central building block in all of this is your database and the functionality it provides for managing your data.

The ability to write transactional functions in Convex is a huge asset because you can perform rather complex data transformations that are extremely difficult to do in SQL. You don't have to have this strong separation between the code that queries the data transactionally and the code that the client interacts with, because it's the same code that's running inside the database.

The ability to manage workflows in Convex greatly assists in your ability to interact with third party services like AI models and to build business workflows. End-to-end type safety and end-to-end consistency allows you to rapidly build applications that are not only correct but also provide a consistent view of application state to the client, without cumbersome caching, polling or data synchronization.

Overall though we think Convex is just easier to use. This is the real differentiator because it translates into better applications built faster.

Q: How well does Convex’s current architecture - where you’re using functions in place of SQL - scale for companies that are experiencing a viral moment, AI or otherwise?

We're very fortunate to have a very experienced team at Convex - a team that has built some of the largest distributed systems in the industry. I think the core to building systems at scale is to come up with elegant designs that have simple building blocks and can grow over time. So, Convex is very well placed to be able to scale because it eliminates complexity in the interaction between applications and the backend.

For example, the developer doesn't have to think about polling the database, because subscriptions are able to give you updated information much more efficiently. Developers don't have to complicate their applications by having manual caching and validation - that's taken care of. So, the ability to hide all of the backend problems from the developer allows us to focus on scaling out a platform without these rather complex interactions between backend code and the glue that holds it together.

Q: RAG has become the de-facto method of accessing and interacting with one’s data using AI models - given Convex’s heavy focus on data management, what’s your perspective on how effective RAG is as a standalone application?

There are a lot of companies that get by just fine with talking to a general purpose model on OpenAI, and there are a lot of startups that periodically train their models, and these are close enough to give good results. Now, what it takes to `build an actually compelling product is for the results from your application to be fresh`. If you add something to a shopping cart and you want to ask the product something about the contents of your shopping cart, you need the latest data. This requires the data to be stored somewhere consistently and easily accessible.

In addition, you need to have your state programmatically accessible. You need to be able to look up historical state for user interactions, and compute usage for users on your platform. So, the ability to have your data stored in a database, but then to be able to use that to supplement AI queries in your product, I think is what really provides a very compelling use case. When we think of the key building blocks of a RAG application, `you've got a model, a vector database storing embeddings, a regular old database storing user state, and then you have some mechanism for scheduling activities between these three.` This is what Convex provides in terms of our database, vector search and scheduling, plus of course the backend to run the rest of your application.

Q: What’s the biggest technical challenge around what you’re building with Convex today?

A: The hardest challenge at Convex has been determining the right development abstractions that hide complex problems with simple interfaces. These are oftentimes hard decisions, and oftentimes the solutions seem obvious in hindsight. You can look at the Convex product and see our queries, mutations and actions, the fact that queries are deterministic and that we run code transactionally in the database. You can look at the design of Convex and also think that it's relatively simple. But, it took us a long time to get there - that design was really hard to achieve.

The hardest challenge we deal with day-to-day is around introducing new features, and how to think about incorporating that into a very simple API that makes life easier for developers. Convex isn't the kind of company that just exposes complexity to the developer and makes it their problem. That's the thing that we have to work hard on every day. Fortunately, I have just a tremendous team that I really enjoy working with and who really embody these values.




Q: You're leading a team at Convex that is very technical and engineering-focussed. Share a little bit about your leadership style and how you think about Convex’s product development approach internally.


The most joy I've had in my career has been mentoring senior engineers - I've been fortunate enough to mentor quite a lot of them. The conversation I almost always have with them is that to move up the conceptual stack and take on higher domains of ownership, they have to be good at thinking about why they're doing something. In any decision, I'm always fixating on the ‘why’ that motivates our actions.


Our team will also be familiar with me fixating on the value of clean abstractions. Oftentimes I'll say that if we have a lot of corner cases in a solution, that's probably a sign that we haven't thought through the design carefully enough. At Convex, we take the time to think very hard about clean, composable abstractions that make complexity go away, rather than a whole mass of interacting components that introduce multiplicative complexity and make every new feature harder to develop than the previous one.

I think back to when we built the storage system at Dropbox and migrated Dropbox away from Amazon S3. We designed that storage system with less than a handful of engineers, and we did most of the work in a matter of months. `The only way we were able to build such a large system in such a short period of time was having a religious obsession with simplicity.` The counterintuitive thing for a lot of junior engineers is discovering that simple is hard. Simple is not a sign of a lack of sophistication - it’s the hallmark of sophistication.




Q: You were part of a high-impact group of Senior Engineers working on migrating Dropbox from S3 to native storage. How has your time at Dropbox impacted the way you lead Convex today?

A: I'm often asked by engineers which blogs or what books they should read to improve their abilities. Generally, my answer is perhaps dissatisfying, but often the way to `become a better engineer is to be better at dealing with humans and understand more about psychology`. **Big challenges are too large to be solved by a single person, and managing large teams attacking large problems is an extremely difficult challenge**.

The way you do that is by building alignment and developing people on your team. So, we talk every day about why we're doing things and why we made decisions. I feel the way to develop a truly world-class engineering team is to always push on this alignment on the why. If you have strong engineers who are very values-aligned and understand the why, they'll figure out the how. But, `no matter how good your engineering team is, if they're not aligned on values and why we're here, you will never get the results that you want to see.`

Q: Lastly, what do you look for in prospective team members joining Convex today?

A: We look for two big things. One, I want `people who care.` I think we're tremendously fortunate to work in an industry where we can solve fun problems and get paid a lot to do so. And so, I think it's a shame to be cynical about it, and I love working with people who are deeply passionate about their job. We want people `who like working with their team members`, where that’s not a burden for them. They like being in person and getting stuck into problems - this is always a strong positive to me.

The second thing we look for is systems thinking. This is not just the domain of backend engineering - systems thinking is for all engineers. How do you think of software systems as building blocks and how they fit together, and do you put in the work to` understand how to design and articulate those conceptual units?` I think these two things together define what a really strong engineer is. All I'll say is, if someone deeply cares about the why in everything they do, and deeply cares about throwing down and being part of a company that has impact, those are the people that I love working with every day.
