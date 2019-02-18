---
layout: post
title: "Layered architecture succintly explained"
---

Each layer depends on the layer below them through an interface - they don't know how the layer below them implement things.

Each layer only exposes things to be used by the layer above them - they don't know how they're going to be used, they don't know anything about the layer above them, they are independent of the layer above them.

There are 4 layers, from top to bottom:
- input layer
- application layer
- domain layer
- infrastructure layer

Domain layer is the entities of the system (employee, department, etc.). Entities can only do things to themselves and answer questions about themselves - they can't interact with or control other entities.

Application layer controls the interactions of entities.

The input layer is where the system gets the input to trigger the application logic. It also displays the current state of the application using binary data, text file (like JSON), GUI, or other means appropriate for the user (which can be a human, another program, etc.)

Infrastructure layer implements the entities using existing technologies (operating systems, libraries, databases, external systems, etc.)