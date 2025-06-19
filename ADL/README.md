# Architecture Decision Log (ADL) README

This folder holds all of the Architecture Decision Records (ADRs) for the vehicle.
The first record should be the vehicle name.

## How to Create an ADR
1. Create a file called {NUM + 1}.md
2. This file should have the following contents
```
ADR{NUM + 1} has not been accepted yet, check [pull request #{Current PR Index + 1}](https://github.com/SolarKnightsRacing/1_solaris/pull/{Current PR Index + 1}) for its progress.
```
> [!CAUTION]
> The ADR index (NUM + 1) and the Pull Request Index (Current PR Index + 1) most likely won't be the same.

3. Create a new branch called ADR{NUM + 1}
4. Replace the contents of {NUM + 1}.md with the ADR Template
5. Commit and push those changes to the new branch
6. Create a new pull request
7. Once there is a tentative outcome for the ADR, Rename the ADR to ADR{NUM + 1}-{Chosen-Option-Seperated-By-Dashes}.md
7. Once the ADR has been written, revised, reviewed, and accepted, squash the changes to the main branch.

## ADR Template
The following is a template for an ADR with a name ####-Title.md e.g. 0000-ADR-Template.md
The first four digits should be a chronological index of the ADRs.
The document must include the .md extension.

```Markdown
---
log: {Architecture Decision Log Name. Most likely car name}
index: 0
title: {short title, representative of solved problem and found solution}
status: { drafted | proposed | rejected | accepted | deprecated | ... | superseded by [ADR-0123](ADR-0123)}
date: {YYYY-MM-DD when the decision was last updated}
decision_makers: {list everyone with final say in the decision e.g.[Person1, Person2, ...]}
consulted: {list everyone whose opinions are sought (typically subject-matter experts); and with whom there is a two-way communication}
informed: {list everyone who is kept up-to-date on progress; and with whom there is a one-way communication}
tags: {tags for subsystems, components, events, regulations, etc. e.g. [vehicle_dynamics, Electrical, REG 8.1.A.1]}
---

## Context and Problem Statement

{Describe the context and problem statement, e.g., in free form using two to three sentences or in the form of an illustrative story. You may want to articulate the problem in form of a question and add links to collaboration boards or issue management systems.}

## Decision Drivers

* {decision driver 1, e.g., a force, facing concern, ...}
* {decision driver 2, e.g., a force, facing concern, ...}
* ... <!-- numbers of drivers can vary -->

## Considered Options

* {title of option 1}
* {title of option 2}
* {title of option 3}
* ... <!-- numbers of options can vary -->

## Decision Outcome

Chosen option: "{title of option 1}", because {justification. e.g., only option, which meets k.o. criterion decision driver | which resolves force {force} | ... | comes out best (see below)}.

### Consequences

* Good, because {positive consequence, e.g., improvement of one or more desired qualities, ...}
* Bad, because {negative consequence, e.g., compromising one or more desired qualities, ...}
* ... <!-- numbers of consequences can vary -->

<!-- This is an optional element. Feel free to remove. -->
### Confirmation

{Describe how the implementation of/compliance with the ADR can/will be confirmed. Are the design that was decided for and its implementation in line with the decision made? E.g., a design/code review or a test with a library such as ArchUnit can help validate this. Not that although we classify this element as optional, it is included in many ADRs.}

## Pros and Cons of the Options

### {title of option 1}

{example | description | pointer to more information | ...}

* Good, because {argument a}
* Good, because {argument b}
* Neutral, because {argument c}
* Bad, because {argument d}
* ... <!-- numbers of pros and cons can vary -->

### {title of other option}

{example | description | pointer to more information | ...}

* Good, because {argument a}
* Good, because {argument b}
* Neutral, because {argument c}
* Bad, because {argument d}
* ...

<!-- This is an optional element. Feel free to remove. -->
## More Information

{You might want to provide additional evidence/confidence for the decision outcome here and/or document the team agreement on the decision and/or define when/how this decision the decision should be realized and if/when it should be re-visited. Links to other decisions and resources might appear here as well.}
```
