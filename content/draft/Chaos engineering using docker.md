---
title: "Chaos engeneering using Docker compose"
---
[[people/Renaud]]
## Chaos engeneering using Docker compose
By _Richard Rostad_

**Chaos Engineering**: A systematic approach to pushing a system encironment outside its comfort zone in order to leard about the system(s) under test and discover potential problems before they become actual problems.

It's ok to test things tat are already in production if you don't have the time to wait for the tests. But you shouldn't test IN production.

Thanks to containers, you don't need a complete test environment to be maintained, you can build it for yourself.

if you scale both the test load and the server capabilities, you can still have good info about the production load capabilities.

>Testing in production is anti-agile

### So, how ?

Having 2 copies of the environment in Docker Compose. Then you can mess with one of the system and compare the reaction to the intouched one.

In the dockerfile, you can set limits to CPU and Memory usage.

When you start up you docker container, you always start in a _known state_.
Whatever you do during a testing session, the next time you start up your container you get the same initial state.

### Automation

You can include some chaos engineering tests inside a pipeline to ensure a consistent response to those unexpected events.

This can be really useful in a microservice environment to make sure your service can always serve it's core purpose all by itself.


sidenote: tests servers should run on synthetic data taylord to match real world expectations. (using AI can help ?)

### Side notes

The setup showed is mainly designed for microservices.
**With big heavy leagacy applications**, it's often too large to run on a laptop, so you might need to go back to setting up a testing environment that you can mess with... sorry ;)

