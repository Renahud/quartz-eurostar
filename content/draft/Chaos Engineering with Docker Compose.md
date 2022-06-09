---
title: "Chaos Engineering with Docker Composer (live notes)"
date: "09/06/2022 09:01"
author: "Manon"
---

## What is chaos engineering?

> Chaos engineering is the discipline of experimenting on a software system in production in order to build confidence in the system's capability to withstand turbulent and unexpected conditions - Wikipedia

But it's not really a good definition.

>A systematic approach to pushing a system environment outside its comfort zone in order to learn about the system's under test and discover potential problems before they become actual problem - The lecturer

Or, in other words : ***Testing***

Why people might want to test in production?
- Not the time to wait for testing before going on prod
- Don't want to maintain a complete test environment

***Testing in production is anti-Agile***

So how then?

With Docker, you can have different copies of the environment, mess with one and see how it reacts in comparison to the others.

![[drawings/system-vs-docker.png]]

What we can configure in a docker compose file:
- Deployment resources (memory, etc.)
- Networks (ELK)
- Dependencies
- ...

It might not be suited for too large legacy system as the container might be too big to run on a laptop. In that case, it's probably best to have a full test environment.

