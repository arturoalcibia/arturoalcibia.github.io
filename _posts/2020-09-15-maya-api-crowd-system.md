---
layout: post
title: Crowd system | Maya Api
subtitle : 
tags: [Maya, python, c++, maya api, maya deformer, crowd, crowd system]
author: Arturo Alcibia
comments : True
---

## TL;DR

This node is a basic crowd system for taking 'agents' from point A to point B
while dodging other agents and mesh obstacles (walls, non-walkable areas, etc.)

- A* algorithm
- Written in C++ for better performance

Below a demonstration on the crowd system.

{% include vimeo-player.html id="458343983" %}

---

## Functionality

Every agent, based on its priority, will wait if another agent is obstructing its path and continue when it's clear.

![Desktop View](/assets/img/crowdSystem/multipleAgents_compressed.gif)

For each agent it will calculate per frame:
- Position
- Aim direction ( For smooth turns )
- Distance ( Useful for auto walk on characters. )

![Desktop View](/assets/img/crowdSystem/nodeImage.png){: width="240"}

An agent in action!


You can see the autowalk and aim direction being fed from the crowd system node.

![Desktop View](/assets/img/crowdSystem/closeUpAnt_compressed.gif)

Changing the end point of an agent, the node calculates and outputs the new path.

![Desktop View](/assets/img/crowdSystem/live2_compressed.gif)

To conclude, this crowd system is able to:

- Use as many agents as you want to procedurally get from point A to point B.
- Mark geometry as obstacles for agents.
- Attribute to get the direction of the path.
- Progress float attribute to implement "auto-walk" on rigs.
- Change the goal point on the go.
- Store the procedural path on cached playback.

---
## Future plans:

- [ ] The aim direction is calculated by inspecting the next position on the path, the path itself could be smoother for a more natural looking walking
- [ ] There is ton of theory to study from for optimization and features.
- [ ] Multithreading

