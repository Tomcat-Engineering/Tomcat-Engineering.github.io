---
layout: tip
title: You will forget what you did (part 2)
number: 15
tags:
 - writing
 - faultfinding
---

The [previous item](14-you-will-forget-what-you-did-so-document-everything) talks about recording your assumptions and analysis when delivering a result.  Another time when it is important to document everything is when you are testing or fault-finding.   

When we engineers discover a fault, our natural reaction is to try and figure out what is causing it.  We change things, run tests, swap out components, take measurements and look in log files.   We are building a model in our head of what is going on inside the system.

Often we can find the cause of the problem relatively quickly, so the mental model is sufficient.  But sometimes the problem is more complex than we thought or our assumptions are wrong, which means the diagnosis takes longer.  We run more and more tests and change more and more things, until eventually we start to forget what we’ve done.   Was that voltage high before we removed that smoothing capacitor, or did I not measure it until afterwards?  Did the weird thing we saw in the logs happen before or after the event we manually triggered?

At this point it is really easy to get confused and head off completely down the wrong track.  Sooner or later we all end up spending hours chasing a problem  induced by something we changed when trying to diagnose the original problem.

It probably isn’t appropriate to take detailed notes every time you start faultfinding, because often by the time you’d documented the initial symptoms you could have fixed the problem.  But if you spend more than five minutes trying to figure out what is going on, and definitely before you start swapping out components, it is worth starting a simple log of what you did and what you saw/measured.

I just use a piece of paper or a text file.  If there are timestamped log files within the system, record timestamps in your notes so that you can tie your actions to the log files.

The act of pausing and writing everything down will force you to step back, think about the problem logically and be explicit about your assumptions.  Occasionally, this is all it takes to see where you have been going wrong.
