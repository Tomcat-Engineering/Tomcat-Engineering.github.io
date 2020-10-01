---
layout: tip
title: When debugging, don’t get confused by collateral damage
number: 60
tags:
 - faultfinding
---

Sometimes I waste hours trying to fix a problem only to find that I’d fixed the original fault ages ago and the system is now not working because of something I’d done as part of the debugging process.

Usually this is either:

- Something I thought I had put back into its normal state, but hadn’t.
- Something I put back incorrectly.
- Something I fried as a side effect of one of the debugging actions.

These faults are not usually in your mental list of potential causes so can take ages to find.
