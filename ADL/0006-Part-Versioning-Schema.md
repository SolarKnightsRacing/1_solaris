---
log: solaris
index: 6
title: Part Versioning Schema
status: proposed
date: 2025-06-09T01:09:00-05
decision_makers: [Technical_Director, Chassis_Lead, Electrical_Lead, Ergonomics_Lead, Vehicle_Dynamics_Lead]
consulted: [Technical_Director, Chassis_Lead, Electrical_Lead, Ergonomics_Lead, Vehicle_Dynamics_Lead]
informed: [Everyone]
tags: []
---

## Context and Problem Statement

We must standardize part versioning in order to prevent breaking assemblies.

## Decision Drivers

* Ease of creation: Creating new version numbers should be easy and quick.
* Readability: One should be able to gether usable information from a version number. 
* Uniqueness: Each version number should be unique.
* Chronological: The version numbers should be in chronological order when sorted alphabetacally.

## Considered Options

* Semantic Versioning
* Branching Method
* Incremental
* None

## Decision Outcome

Chosen option: "Semantic Versioning", because It allows version numbers to provide critical information about revisions.

### Consequences

* Good, because revisions are classified as compatable or incompatable
* Good, because it is a popular way of tracking versions
* Good, because PATCH level changes don't need to be updated with any urgency
* Good, because MINOR level changes won't halt development if they aren't imeadiately updated

## Pros and Cons of the Options
### Semantic Versioning

In short, Semantic Versioning consists of a MAJOR version, a MINOR version and a PATCH version. like the following: `MAJOR.MINOR.PATCH`

PATCH level changes include those that simply fix existing geometry or make something work the way it was originally intended to.

MINOR level changes include those that make a significant change to the inner functionality of the part but do not change the way the part interacts with others.

MAJOR level changes include those that make incompatable changes to the part that require others to adapt to.

This blog post explains semantic versioning and how it streamlines CAD iteration: https://www.cadtrainingonline.com/5-best-practices-for-cad-version-control/#1_Use_Semantic_Versioning_for_Design_Iterations

* Good, because revisions are classified as compatable or incompatable
* Good, because it is a popular way of tracking versions
* Good, because PATCH level changes don't need to be updated with any urgency
* Good, because MINOR level changes won't halt development if they aren't imeadiately updated

### Incremental
Each time a change is made, a singular version number is incremented.

Ex. v1 -> v2 -> v3

* Good, because it is intuitive
* Bad, because numbers becomes unweildy when part changes are frequent.
* Bad, because the new version could be entirely different or have one insignificant adjustment.
* Bad, because parts must be manually updated in assemblies for every change.

### Branching Method
This method relies on different git branches that use the same part name. The version of the part is tied to the git branch it is on.
* Good, because solidworks would automatically use whatever part is currently checked out in the working directory.
* Neutral, because part versions are implied rather than explicit.
* Bad, because it is fragile

### None
* Bad, because bad
