---
title: "Tutorial F - From Business Workflows to Automated Tests"
alias: ["From Business Workflows to Automated Tests", "Tutorial F"]
---
Notes by [Renaud](people/Renaud.md)


Tutorail By _Dr Anne Kramer_,  using [Yest](https://marketplace.atlassian.com/apps/1221359/yest-agile-test-design-automation)
(Yest has a jira integration)
# Introduction

We want to Atomalte Tests, but it is difficult.

In agile teams, there's often no dedicated testers.

ISTQB was born from the observation that it doesn't work. Teams need specialised testers, because they have a different mindset.

Developers tend to focus on unit tests and miss the top of the pyramid. Which require more business knowledge.

End to end can be multi-aplication, but also in a single application.

The tester should have the most knowledge about functionalities of the system, they are needed to free time from developers.

## Approaches to test automation

### 3 amigos approache
- [PO](Product%20Owner.md)
- Tester
- Developper
All working together.

### Behavior driven development

**Given -when -then** syntax used to describe a behavior.
Bridre between manual test and automated test.

### Keyword driven Testing
older apporach.
Action words + parameters
The developers must create a framework/library to execute the keywords.
Nice idea, but this approach still stems from code and development. Thus still usually developper-driven.

### Model-based Testing

Visualising Busines Workflows

Workflows + business rules.

### Visual acceptence test driven development (Visual ATDD)

Best of everything, the goal of this tuto.

- Test-friven like BDD
- Visual with MBT
- Colaboration of 3 amigos
- Separate logic and code using keywords.

# Tutorial

## Business Wrkflows to visualization

Program to test : [Car insurance simulation](https://eur03.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdemo-simulator.herokuapp.com%2F&data=05%7C01%7Crenaud.pirson%40sfpd.fgov.be%7C714366dbeafb43409be208da4490f877%7C66c008a4b56549a993c9c1e64cad2e11%7C0%7C0%7C637897686686314826%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=xQzUXQDDltuNcoyZpnXcySON9rppRoKpXjZFhbQl%2Brk%3D&reserved=0).

Tests focused on the business flow. 

Workflow as modeled in Yest :

![[_attachments/Pasted image 20220607100248.png]]


The discussion should stay at a high level. Acceptence driven -> can be discussed with the [PO](Product%20Owner.md) as well as with the Devs.

The detailes whould be discussed when the time of the execution comes (manual or auto). 

This visualization is helpfull to validate and discuss requirements.



---
## Automated test cases Generation

In yest : 
- right click -> analyse workflow
- generate test scenarios

![[_attachments/Pasted image 20220607113827.png]]
![[_attachments/Pasted image 20220607113941.png]]

You should also parameterized data.

### Two kinds of data

- Design data
	- based on business rules
	- defined by PO/ analyst
	- equivalence partitions in test design
- Implementation Data
	- concrete values for test automation framework
	- usually specified manually by the tester
	- realization strongly depends on tool

In Yest, there's a possibility to inject datasets.


---
## Creation of automated Tests

Yes can generate tests scripts in various languages, including java / selenium, using a keyword approach. In case of java, those keyords would be function calls with parameters extracted from the dataset in Yest.

The function calls corresponding to the keywords must be implemented by a developer/ automation sepcialist.

