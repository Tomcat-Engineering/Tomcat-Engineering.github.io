---
layout: tip
title: Beware adding complexity to achieve "robustness"
number: 30
tags:
 - design process
---

[Simplicity is an important and oft-neglected characteristic of good designs](30-simplicity).

It is sometimes tempting to make your design more complex in order to make it more "robust".  Usually this is in the form of adding redundancy.  

Think carefully about what you mean by robustness in the context of your system.  Will the extra burden of complexity be worth it?  Will the more complex system even be any more robust?

A man with a watch knows the time.  A man with two watches is never quite sure... but he also has twice the winding to do, and double the chance of a dud watch.

# Example

Rather than running a single web server, it is now common to run three identical web servers behind a load balancer.  This increases your capacity and allows you to deploy updates to your website without downtime, by updating one web server at a time.

But maybe you don't need any extra capacity and updates were near-instantaneous anyway?

Now you have four computers to manage instead of one.  You have load balancer software to configure and update.  You still have a single point of failure.  Your attack surface is larger (in terms of computers, software applications and network connections).  When you are debugging an incident, you now have logs on four servers to sift through.  When an OS security fix is released, you have four times the work to deploy it - and it still involves downtime.  

And there are now also many subtle problems that you haven't thought of.  For example, during a rolling update, what happens when incoming requests from a customer's browser are routed to a mix of old and updated servers - will the site break?  Will the web server's internal cache be less efficient when it only sees 1/3 of the requests?  

These problems are of course all solvable - usually by paying for more complexity like a hosted load balancer service, a hosted log aggregation service and a hosted cache service... but now your website is ten times as expensive to run and takes five times more maintenance effort.  Has the uptime actually improved?  Enough to pay for the extra cost and work?

The answer obviously depends completely on the context, but make sure you ask the question.

PS - I'm not the only grumpy old programmer who complains about this complexity.  [The first few minutes of this Rails World keynote by DHH contains very similar ideas](https://youtu.be/gcwzWzC7gUA?t=210).
