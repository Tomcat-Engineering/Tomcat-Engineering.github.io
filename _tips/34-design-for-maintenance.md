---
layout: tip
title: Design for installation and maintenance
number: 34
tags:
 - design process
---

As engineers we tend to focus on the normal operation of our products, but for many products the main human interaction will be during installation and maintenance.

Think about this at the outset.  How is the installer going to know everything is working correctly?  How is a maintenance technician going to diagnose problems or work out when something is worn out?  Is it simple to access all the parts which require inspection or maintenance?  Are we giving clear error messages or just obscure codes?

Nobody likes that design where you have to dismantle everything just to get at some basic part.  There is usually no excuse for this type of design.

This applies equally to software.  Even if you are just writing a software tool for yourself, it is usually worth the investment to add a few lines of logging to help diagnose problems later on.

Getting this stuff right will not only make you popular with those who interact with your product (or more likely just mean that they don’t curse you all the time), it can also save you a lot of time personally during R&D work or third-line support.
