---
log: solaris
index: 7
title: Part Naming Schema
status: proposed
date: 2025-06-09T12:15:00-05
decision_makers: [Technical_Director, Chassis_Lead, Electrical_Lead, Ergonomics_Lead, Vehicle_Dynamics_Lead]
consulted: [Technical_Director, Chassis_Lead, Electrical_Lead, Ergonomics_Lead, Vehicle_Dynamics_Lead]
informed: [Everyone]
tags: []
---

## Context and Problem Statement

We must standardize part naming.

## Decision Drivers

* Ease of creation: Creating new part names, or typing out a part name in general, should be easy and quick.
* Readability: One should be able to tell what part it is referencing. 
* Uniqueness: Each part name should be unique from any other part that will be created within the club.

## Considered Options

* {Part Number}-{Part Description}-{Part Version}

## Decision Outcome

Chosen option: "{Part Number}-{Part Description}-{Part Version}", because it satisfies the readability and uniqueness drivers, and it is the only option right now.

### Consequences

* Good, because each part name will be unique as long as part numbers are unique.
* Good, because part names will self-organize when listed alphabetically
* Bad, because part names will be long

### Confirmation

Part naming will be used for any official references to parts or assemblies that require descriptive elements. e.g. CAD filenames.

## Pros and Cons of the Options

### {Part Number}-{Abbreviated Part Description}-{Part Version}

This naming schema will use the Part Number and Part Version along with a description of the part to create a filename that is descriptive, unique, and relatively easy to create.

The Abbreviated Part Description will be a list of words that describe the location and functionality of a part, from most general category to most specific category. This description should sound natural when read from RIGHT to left.

General categories:
```
assembly --------> ASM
weldment --------> WLD
electronics pcb -> PCB
machined part ---> PRT
chassis tab -----> TAB
```

* Good, because each part name will be unique as long as part numbers are unique.
* Good, because part names will self-organize when listed alphabetically
* Bad, because part names will be long
