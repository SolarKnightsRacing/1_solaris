---
log: solaris
index: 7
title: Part File Naming Schema
status: proposed
date: 2025-06-10T11:04:00-05
decision_makers: [Technical_Director, Chassis_Lead, Electrical_Lead, Ergonomics_Lead, Vehicle_Dynamics_Lead]
consulted: [Technical_Director, Chassis_Lead, Electrical_Lead, Ergonomics_Lead, Vehicle_Dynamics_Lead]
informed: [Everyone]
tags: []
---

## Context and Problem Statement

We must standardize part filenaming.

## Decision Drivers

* Ease of creation: Creating new part's filename, or typing out a part filename in general, should be quick and easy.
* Readability: One should be able to tell what part the filename is referencing. 
* Uniqueness: Each filename should be unique from any other part that will be created within the club.

## Considered Options

Subdirectory:
* /
* {subsystem directory}/
* {subsystem directory}/{Part Number}-{Part Description}/

Filename:
* {Part Number}-{Part Description}-{Part Version}
* {Part Number}-{Part Version}

## Decision Outcome

Chosen option: "Subdirectory: {subsystem directory}/{Part Number}-{Part Description}/  Name: {Part Number}-{Part Version}", because it satisfies the uniqueness driver and the Ease of creation driver.

### Consequences

* Good, because each filename will be unique as long as part numbers and version numbers are unique.
* Good, because filenames will self-organize when listed alphabetically
* Good, because filenames will be relatively short
* Good, because the part's folder name will provide the part description
* Bad, because part descriptions will only be available via the part's folder name

## Pros and Cons of the Options

### Subdirectory: /
All versions of a part will be stored in the root directory.

* Bad, because unorganized

### Subdirectory: {subsystem directory}/
All versions of a part will be stored in their subsystem's directory.

* Bad, because there would be way too many version files

### Subdirectory: {subsystem directory}/{Part Number}-{Part Description}/
All versions of a part will be stored in a subdirectory containing the part number and part description.

The Part Description will be a list of words that describe the location and functionality of a part, from most general category to most specific category. This description should sound natural when read from RIGHT to left.

General categories:
```
assembly --------> ASM
weldment --------> WLD
electronics pcb -> PCB
machined part ---> PRT
chassis tab -----> TAB
```

* Good, because all versions of a single part will be stored in one folder
* Good, because the part description

### Filename: {Part Number}-{Part Description}-{Part Version}

This naming schema will use the Part Number and Part Version along with a description of the part to create a filename that is descriptive, unique, and relatively easy to create.

* Good, because each part name will be unique as long as part numbers are unique.
* Good, because part names will self-organize when listed alphabetically
* Bad, because part names will be long

### Filename: {Part Number}-{Part Version}
This naming schema will use the Part Number and Part Version only to create a filename that unique, and easy to create.

* Good, because each part name will be unique as long as part numbers are unique.
* Good, because part names will self-organize when listed alphabetically
* Good, because part names will be relatively short
* Bad, because part descriptions will only be available via the part's folder name
