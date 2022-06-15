---
title: "Chaos Engineering using Docker Compose"
author: [Renaud, Manon]
---


## Chaos engeneering using Docker compose
By _Richard Rostad_

**[[Chaos Engineering]]** is a form of  ***Testing***

It's ok to test things that are already in production if you don't have the time to wait for the tests. But you shouldn't test _IN_ production.

Thanks to containers, you don't need a complete test environment to be maintained, you can build it for yourself.

>Testing in production is anti-agile

### So, how then?
With Docker, you can have different copies of the environment, mess with one and see how it reacts in comparison to the others.

![[drawings/system-vs-docker.png]]

What we can configure in a docker compose file:
- Deployment resources (memory, CPUetc.)
- Networks (ELK)
- Dependencies
- ...

When you start up you docker container, you always start in a _known state_.
Whatever you do during a testing session, the next time you start up your container you'll get the same initial state.

### Automation

You can include some chaos engineering tests inside a pipeline to ensure a consistent response to those unexpected events.

This can be really useful in a microservice environment to make sure your service can always serve it's core purpose all by itself.

> [!NOTE] Side note on data
>  Tests servers should run on synthetic data taylored to match real world expectations. (using AI can help ?)

### For big legacy applications

The setup showed is mainly designed for microservices.
**With big heavy leagacy applications**, it's often too large to run on a laptop, so you might need to go back to setting up a testing environment that you can mess with.
