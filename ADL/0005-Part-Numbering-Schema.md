---
log: solaris
index: 5
title: Part Numbering Schema
status: proposed
date: 2025-06-09T10:16:00-05
decision_makers: [Technical_Director, Chassis_Lead, Electrical_Lead, Ergonomics_Lead, Vehicle_Dynamics_Lead]
consulted: [Technical_Director, Chassis_Lead, Electrical_Lead, Ergonomics_Lead, Vehicle_Dynamics_Lead]
informed: [Everyone]
tags: []
---

## Context and Problem Statement
We must standardize part numbering in order to ensure uniformity with regard to referencing parts. These part numbers will be used in file names, git operations, budgeting spreadsheets or just in conversation.

## Decision Drivers
* Ease of creation: Creating new part numbers, or typing out a part number in general, should be easy and quick.
* Readability: One should be able to tell what part it is referencing.
* Uniqueness: Each part number should be unique from any other part that will be created within the club.

## Considered Options
* Sol-El-1234-5

## Decision Outcome
Chosen option: "Sol-El-1234-5", because it's the only option right now. Omar and I spent a while trying to determine the best schema, and this is what we landed on.

### Consequences
* Good, because each part number will be unique. (216 Million combinations)
* Good, because it allows for up to 36 parts in an assembly without deviating from the schema
* Good, because part numbers are still very short
* Good, because part numbers will self-organize when listed alphabetically
* Neutral, because it must be paired with some sort of description schema if read out-of-context
* Neutral, because every part must belong to one, and only one, subsystem. This can be viewed as a good or bad thing, depending on if you value the benefits of having distinct responsibilities for each sub-system.

### Confirmation
Part numbering will be used for all official references to parts and assemblies.

## Pros and Cons of the Options
### Sol-El-1234-5
* Good, because each part number will be unique. (216 Million combinations)
* Good, because it allows for up to 36 parts in an assembly without deviating from the schema
* Good, because part numbers are still very short
* Good, because part numbers will self-organize when listed alphabetically
* Neutral, because it must be paired with some sort of description schema if read out-of-context
* Neutral, because every part must belong to one, and only one, subsystem. This can be viewed as a good or bad thing, depending on if you value the benefits of having distinct responsibilities for each sub-system.

## More Information
### Sol-El-1234-5 (AAA-BB-CDEF-G)
```
AAA -> Vehicle Name abbreviated --------> Solaris ------------------> Sol
BB --> Subsystem abbreviated -----------> Electrical ---------------> El
C ---> Top Level Assembly Identifier ---> Battery ----> 1000 level -> 1 (Arbitrary)
D ---> Sub-Assembly Identifier ---------> pack -------> 200 level --> 2 (Arbitrary or sequential)
E ---> Sub-Sub-Assembly Identifier -----> string -----> String 3 ---> 3 (Arbitrary or sequential)
F ---> Sub-Sub-Sub-Assembly Identifier -> module -----> Module 4 ---> 4 (Arbitrary or sequential)
G ---> Part Identifier -----------------> cell -------> Cell 5 -----> 5 (Arbitrary or sequential)
```

#### AAA -> Vehicle Name abbreviated
The vehicle's name abbreviated to 3 characters. \
Ex. Solaris -> Sol

#### BB -> Subsystem abbreviated
The subsystem the part belongs to abbreviated to 2 characters. \
Ex. **Ch**assis -> **Ch** \
Ex. **El**ectrical -> **El** \
Ex. **Er**gonomics -> **Er** \
Ex. **V**ehicle **d**ynamics -> **Vd**

#### C -> Top Level Assembly Identifier
The Top-level assembly the part exists under within the subsystem. \
1, ... , 8, 9, a, b, ... , y, z \
Ex. The battery might use the 1000 level identifier, so "1"

#### D -> Sub-Assembly Identifier
The Sub-Assembly the part exists under within the Top-Level Assembly. \
1, ... , 8, 9, a, b, ... , y, z \
Ex. The "pack" might use the 200 level identifier, so "2"

#### E -> Sub-Sub-Assembly Identifier
The Sub-Sub-Assembly the part exists under within the Sub-Assembly. \
1, ... , 8, 9, a, b, ... , y, z \
Ex. One of the strings might use the 30 level identifier, so "3"

#### F -> Sub-Sub-Sub-Assembly Identifier
The Sub-Sub-Sub-Assembly the part exists under within the Sub-Sub-Assembly. \
1, ... , 8, 9, a, b, ... , y, z \
Ex. One of the modules might use the 4 level identifier, so "4"

#### G -> Part Identifier
The identifier for the part. "0" is a sentinel value that means that the part is an assembly \
0, 1, ... , 8, 9, a, b, ... , y, z \
Ex. One of the cells might use the identifier 5
