---
title: measuring
date: 2023-06-28T20:00:00.020Z
tags:
  - post
---
the process of trading involves a lot of measuring.

in a trading system, you've made a bunch of assumptions and decisions, added a lot of moving parts.

and you need to isolate and track all those individual bits as best you can.

**you've made forecasts about future returns**

do those still hold up? is the nature of them changing? is information decaying at the same rate? Are you seeing different behaviour in different places? how confident are you in that?

**you've combined those forecasts in some way**

there are several ways you could have chosen to do that. are you happy the choices and assumptions you made (about persistence/momentum/whatever) are still valid?

**you modelled the risk and co-riskiness of positions somehow**

maybe you did this in a simple way or a complicated way but, ultimately. it's a forecast of the future informed by past data. you need to measure how effective you are and how stable your estimates are.

**you modelled your trading costs**

there are elements of this that are very simple (bro & other fees) and elements of this that are complicated to model (market impact, opportunity cost, adverse selection). you need to track your execution performance against those assumptions.

**you modelled all the constraints you're under**

what you would like to do and what others will let you do are different things. you should also impose some sensible position and risks limits upon yourself even if this weren't true.

**then you created a system to navigate the trade-offs inherent in the above**

* "i want to maximize returns but i also need to think about risk"
* "my return forecast decays fast, so i want to turn over fast - but turning over fast is expensive"
* etc

these trade-offs add a whole bunch of nuance and complexity to the things above.

you're smoothing everything to make it more auto-correlated so forecasts don't jump around much.

you never really know what forward period you actually want to forecast (you might be making decisions every t - but you certainly don't want to turnover that fast)

you're trying to sensibly navigate the "lower confidence in alpha vs 100% confidence in costs" trade-offs, and you don't really know how to do that cos you can't see the future.

and even when you've managed to isolate and measure and track things as best you can it can feel like the system as a whole is behaving in non-intuitive ways.

## a lot of work

anyway... my point is that a trading system is like any other system you would like to perform well under uncertainty.

it needs to be measured and tracked and assessed against simple baselines at a variety of levels.

it needs to be iteratively adapted in careful ways.

things quickly get out of hand so i'd recommend you keep things as simple as they can be. 

beep...boop.




beep...boop.