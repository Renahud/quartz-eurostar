---
title: "Tutorial  B"
alias: ["Tutorial B", "Developing Critical Thinking Skills for Testers - Andrew Brown"]
tags: [Jana]
---
Notes by [[people/Jana]]

Speaker: Andrew Brown

[Official introduction](https://conference.eurostarsoftwaretesting.com/event/2022/developing-critical-thinking-skills-for-testers/)

## Confirmation Bias
Often when we test we start from a hypothesis (our belief in how the system is/should work) and we're only looking for confirmation: we run tests that confirm the hypothesis instead of challenging it.

We can mitigate this bias by coming up with multiple alternative hypotheses before we start testing -> this way we can reduce our confirmative behaviour.

Excersises to illustrate this bias:
- discover the rule: 2,4,6
	
- discover the rule2: 2,4,8

## Information Bias
We tend to seek out information even if the result of a test does not provide us with any diagnostic information => we get influenced in our judgment, even though the information does not prove/refute the rule/requirement.

We should try to run only diagnostic tests and ask ourselves if the information we get is actually diagnostic about the rule we're testing.

Exercise to illustrate: 

There are 2 urns, that both contain 100 balls, with a differentcombination of red (R) and white (W) balls.

| urn A | urn B |
| :---: | :---: |
|70 W / 30 R | 70 R / 30 W |

Someone chooses 1 of the 2 urns and draws a random number of balls from it. After this first drawing you write down your guess of the probabilty of the selected urn being urn A. 

| drawing | W | R | probability of being urn A (%) |
| :-----: | :-: | :-: | :-------------------------: |
| 1st |  2 | 1  | ? |

The person will continue drawing balls from the urn and you will alter your probabilty based on the colour of the balls drawn.

## Indicative and deontic reasoning
Our logic is not always rational. As humans we're much better at deontic reasoning than indicative reasoning.

### Indicative reasoning
= Pure logic/abstract reasoning => true/false

Exercise to illustrate:

4  cards with a letter on one side and a number on the other:
| A | B | 4 | 7 |
| - | - | - | - |

RULE: if it's a vowel, it should always have an even number on the other side
=> which card(s) do you turn to test the rule?

### Deontic Reasoning
= Reasoning about permissions, obligations, prohibitions => social rules

Exercise to illustrate:

4 cards with an age on one side and a drink on the other: 

| 17 | 25 | coke | beer |
| -- | -- | ---- | ---- |

RULE: if you're under 18, you can't drink alcohol
=> which card(s) do you turn to test the rule?

>The first exercise (letter & numbers) is a lot harder than the second one (age & drinks), although the logic is the same. That's because humans are very good at social reasoning. This is linked with dominance theory and theory of mind.

#### Dominance theory
The size of the social group of an animal is linked with the brain size (size of the frontal cortex in relation to the rest of the brain) of that animal ==> you need a lot of brain capacity to keep track of all the social relations. 

Humans have the biggest brain size ratio and can have social groups of 100 to 150 individuals. This social group has a social hierarchy. If you're dominant, you need social skills to define the rules and make others follow them. If you're non-dominant, you use your social skills to mitigate those rules, form alliances, .... Most people are both dominant and non-domninant depending on the context.

#### Theory of mind
This is the capacity to represent & manipulate the internal representations in the mind of others (= recognize and predict others thougths)

### Tips
It's easier for humans to use logic when there is:
1. a social contract (f. ex. "spot the cheater")
2. a concrete example (a situation we can imagine)

Tips to increase our logic reasoning:
- think through, write down
- use concrete/meaningful examples
- ...

## Functional fixedness (einstellung)
A risk of having experience in certain tasks is that, once we spotted a pattern, we keep using it and we miss other options/solutions. Once someone has presented us a solution, our mind gets stuck on it and we stop trying to find other (easier) solutions.

Advantages to thinking in patterns:
- speed 
- standardization
- reduced cognitive load
- reduced uncertainty

Ways of avoiding this while testing:
- be aware of einstellung
- get multiple perspectives, discuss with others, do pair testing
- limit/challenge yourself to trigger creativity, f.ex. obligate yourself to find at least 2 different solutions
- swap subject/context
- change the order of test execution

Exercise to illustrate:
- measure a desired volume of water with 3 jars

## There's more information than we know
Sometimes a test/experiment yields more information than we realise, a test can give us both information about what we test and what we don't test. We should be creative in finding solutions to testing problems.

Exercise to illustrate:
> 12 weights problem: you have a scale and 12 similar objects of which 11 have the exact same weight and 1 is either heavier or lighter (this is unknown). You have to identify the object with the different weight and know if it's lighter or heavier in the least possible weighings. 

Spending a lot of time to find the most elegant/ideal solution to test something (f. ex. in the least amount of steps) might be too time consuming. If we can get the same result faster via brute force, this might be preferred, especially when the cost of running a test is low. When we have only 1 chance to run a test, or the cost or consequences of running the test are high, the most elegant solution might be better.

How can we generate other solutions?
- brainstorming
- assert/inform that a solution exist => f. ex. by knowing that there is a way to solve the 12 weights problem in 3 steps, you will try to find that solution

## Summary
![[_attachments/Pasted image 20220607205851.png]]



			
			
		






