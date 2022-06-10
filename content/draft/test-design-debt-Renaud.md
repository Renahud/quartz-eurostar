---
title: "What's your Test Design Debt ? Avoid the inevitable!"
---

[[people/Renaud]]
# What's your Test Design Debt ? Avoid the inevitable!
by _Wim Decoutere_

## **Requirements WILL CHANGE**
- business processes change
- Cometitors innovate
- Legislation regulation
- Business change priorities
- New technologies
- Users ask new features
- Defects may induce changes to be fixed

When faced with a chege, we can accept, reject or postpone it. To make the decision we must consider all factors.
- value
- cost
- time
- resources
- risks
- impact
	**- impact on test cases is often forgotten**

## Other reasons to change test cases

- Multiple testers work on the same test cases
- time pressure
- Copy-paste errors
- Musunderstanding requirements
- missing conditions
- New testers joining the team with new ideas
- Migration to new tools
- => **Test design debt**

## Test design debt
>Implied cot of having to clean up te mess testers made by documenting tests _quick and dirty_ and not sticking to best practices and design patterns.

Maintainability is a key for test cases also.

### Maintainability
criterias inspired from sofware criterias
- modularity
	- small test cases
- reusability
	- test cases should be more generic
	- externalize data
- Analyzability
	- Good naming practices
	- Don't make assumptions about the person that will execute the test. Steps should be explicit
- Modifiability
	- should be easy to update
	- Using a glossary with stadard terms, makes it easier to replace a term in all test cases
	- Simplicity
- Testability
	- Testing tools should be tastable
	- Test cases should be reviewd
		- quality criterias for test cases
			- adequate
			- understandable
			- tracable (link to requirements and back)
			- Unambiguous
			- Complete

### How to get there
Using _Test design techniques_ can help achieving good coverage.
Use the right tool for the right job. If tools are available, try to use them if relevant.

Evaluate your exising testcases, should they be documented ?
	What's their purpose
	What's their size
	What's their lifespan 
	How are they documented

The execution order shoudl be externalized from the test
1 test 1 goal
Creating a blueprint of the test

/backup