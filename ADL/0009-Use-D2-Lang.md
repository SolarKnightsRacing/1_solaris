---
log: Solaris
index: 9
title: Use D2 Lang
status: draft
date: 2025-05-28T23:45:00-05
decision_makers: [Electrical_Lead, Technical_Director]
consulted: []
informed: [Electrical]
tags: []
---

## Context and Problem Statement

We must decide on a diagramming tool for electrical systems.

## Decision Drivers

* Free
* Version control: It would be useful to have a text-based tool so that version control can effectively track changes.

## Considered Options

  * WireViz
  * Graphviz
  * D2 lang
  * Mermaid
  * PlantUML
  * AutoCAD Electrical
  
## Decision Outcome

Chosen option: D2 lang

### Consequences

* Good, because {positive consequence, e.g., improvement of one or more desired qualities, ...}
* Bad, because {negative consequence, e.g., compromising one or more desired qualities, ...}
* ... <!-- numbers of consequences can vary -->

## Pros and Cons of the Options

  ### WireViz

  {example | description | pointer to more information | ...}

  * Good, because we would be using the same tool for the wire harness and the system diagrams.
  * Bad, because WireViz uses a mostly right-to-left layout which is not suitable for complex system diagrams.

  ### Graphviz

  {example | description | pointer to more information | ...}

  * Good, because it is very flexable.
  * Bad, because it is very tough to learn.
  * Bad, because it is ugly.

  ### D2 lang

  {example | description | pointer to more information | ...}
  ```D2
  battery: "9V Battery"
  resistor: "220R\nResistor"
  led: {
    shape: circle
    label: "LED"
    style.fill: "#FF0000"
  }
  ground: "Ground"

  battery -> resistor
  resistor -> led
  led -> ground
  ground -> battery
  ```
  ![Example D2 Diagram](assets/D2lang-Diagram-Example.svg)

  * Good, because it is very flexable.
  * Good, because it was built from the ground up with the mistakes of Mermaid, Graphviz and similar tools in mind.
  * Bad, because there is a DSL that you must learn.

  ### Mermaid

  {example | description | pointer to more information | ...}

  * Good, because it has native embeddings for things like Github and obsidian.
  * Good, because it is common.
  * Bad, because it is not very flexible.
  * Bad, because it is slow.

  ### PlantUML

  {example | description | pointer to more information | ...}

  * Bad, because it is ugly.
  * Bad, because it is not good for systems diagramming.

  ###AutoCAD Electrical 

  {example | description | pointer to more information | ...}
  
  *Good, because we'll be using the same system for the wire harness design. 
  *Good, because it was designed for efficiently designing electrical systems. 
  *Nuetral, it is industry standard. 
  *Bad, no native github integration. 

 ![AUTOCADELECTRICAL](https://github.com/user-attachments/assets/a052fa3f-4fa1-4732-8ae4-d75bbbac9b01)

