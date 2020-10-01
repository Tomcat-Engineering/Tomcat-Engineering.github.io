---
layout: tip
title: Use binary search for faultfinding
number: 23
tags:
 - faultfinding

---

You typically have a chain of subsystems to work through. You could work your way logically along the chain, starting by checking the output of the first stage and then moving on to the next. However, it can be much more efficient to start by checking the output somewhere in the middle of the chain. Hopefully this will immediately tell you which half of the system your (first) problem is in. You can then repeat the process to isolate the fault.