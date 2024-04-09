---
layout: page
title: 101 Things I Wish I'd Learnt at Engineering School
---

Twenty years ago I finished university and started working as an engineer.

At that point I had a huge amount of theoretical knowledge and could confidently write you a mathematical model of anything in five minutes flat.  I assumed that I had basically finished learning and was about to put all that hard-earned knowledge to work solving the world’s problems.

Then I entered the world of work and spent the first two weeks waiting for the IT department to set up my login.  My boss was an idiot who couldn’t understand the simplest differential equation, and we spent most of the time in pointless meetings.  Apparently I still had a lot to learn.

Since then I have worked for huge companies and small startups, on academic research and on freezing building sites.  These pages list some of the things I’ve learnt about the non-technical aspects of engineering.  None of the insights are new and none of them are my ideas, but they have taken me many years of work to collect.

{% for tip in site.tips %}

# [ #{{ tip.number }}: {{ tip.title }}]({{ tip.url }})

{{ tip.excerpt }} [Continue reading...]({{ tip.url }})

{% endfor %}
