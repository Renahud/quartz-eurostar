---
title: "draft-keynote-renaud"
---

# draft - Keynotes
[[people/Renaud]]
## My essence of Testing
by *Richard Edgreen*

Testing starts in your head, it's dependant of your understanding of the problem the application is trying to solve.

There is no universal essence of testing.

This is *his* essence of testing:

> [!quote] Essence of testing
> By understanding relations, you will among many things understand what is important, so you can do good testing (while also providing value in other ways)

Testing is a samplig business because it's never finished. You can never say you've tested everything. Therefore, your way of sampling is crucial in testing. 

How the sampling is designed, executed, evaluated and reported can be decided by
- other people
- tradition
- something you read in a book / website
- **your own understanding of this particular situation**

> No one can step in the same river twice, because it is not the same river and you're not the same person. Everything changes (Panta rei)


## Relations

What are you trying to understand ? relations.
There are different types of relations:
- Within the system
- Between the system and other systems
- Between the system and it's users
- Between the people making the system (social relations)

![[drawings/relations-with-production.excalidraw.png]]

## Continuous Learning
You must know things to be able to test the product
Testing the product is learning about it.
By testing it, you will have new ideas about what to test
New perspectives -> value to the team -> chances to find important information

For this reason, the best strategy is learning to learn faster.
Different ways to learn:
- experimenting
- discussing
- talking
- trying
- reading
- thinking
- writing
- teaching

### Testing is not an island

The relations we have with other people are also important to feel good and do good work.

The value of testing happens outside of testing

Testing what's important != testing requirement != testing everything(impossible)
![[drawings/the-potato.excalidraw.png]]
How to find what's important ?

>[!quote] Diverse Half-Measures 
>It's better to do more different kinds if testing to a pretty good level, than to do one or two kings of testing perfectly

## Serendipity
_Good testers are often lucky_

**Serendipity** : When looking for something, you found something else that is important and that you weren't looking for.

Making serendipity happen :
	- preparations
	- wide awareness
	- sagacity :by knowing a lot about the software and its usage,  you can miake wise judgments about what happens and what more should be tested

By unterstanding differences and similarities -> know what to tests

## Models
Models are a way of simplifying one's understanding, Hence, having multiple models is important  (more views of the subject).

Models can come from multiple source
	- the developers
	- data
	- usage
	- knowledge of the product
	- a lot of other things...

Some models are not visible, this is a representation of the speaker's mental representation of a product :
![[drawings/overlapping-models.excalidraw.png]]


### Modeling - Product elements

[[SFDIPOT]]

- Structure - what the product is
- Functions - what the product does
- Data - what the product operates on
- Interfaces - how the product can be accessed or expressed
- Platform - the environment the product depends on
- Operations - what the users want to accomplish
- Time - relations between the product and time

It's harder to evaluate the tests for the structure than the functions.




Modeling resource : [[SFDIPOT]]

## Binary disease
A lot of tools are binary : pass/fail
- pass/Fail addiction
	- need to put pass/fail on every test, bad feeling if you canot say either way
- Coverage Obsession
	- Obsessed with the percentage of coverage
- Metrics Tumour
- Sick Testing Techniques
	- too much equivalence partitionning (formalized)
	- thing of techniques first

A human's software
made by humans
for humans

Human can make better judgement about what's important.

