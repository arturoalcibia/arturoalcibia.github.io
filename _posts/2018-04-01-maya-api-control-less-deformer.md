---
layout: post
title: Control-less rig deformer like Pixar's Presto
subtitle : 
tags: [Maya api, maya deformer, rig, pixar presto]
author: Arturo Alcibia
categories: [projects]
comments : True
---

# Control-less rig deformer like Pixar´s Presto

---
Below you can see the deformer in action with multiple controls plugged to the rig.

{% include vimeo-player.html id="266764598" %}
---

## Functionality

This deformer allows you to have rig controls directly on the mesh itself.

![Desktop View](/assets/img/control-lessRig/movingNode_compressed.gif)

The setup is fairly easy once automated. Selecting the faces that
you want the control to be and the solution should automate the duplication of
geometry and plugging it into the deformer.

This had to be ported to C++ since the performance in python wouldn't be able to get to real time
performance once multiple controls had been created.

![Desktop View](/assets/img/control-lessRig/patchNode_compressed.gif)

---

---

## Future plans:

- [ ] Using the GPU should improve performance and looks interesting to dive into.

---