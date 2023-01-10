---
title: "on puking quick: don't  outstay your welcome in relative value trades"
date: 2023-01-10T03:24:17.629Z
tags:
  - post
---
many traders have worked out that, if you think you've identified a mispricing, you want your trade to move your way pretty quickly. 

systematic traders have lots of data on this and it's nearly always the case.... 

...at least for things that can be systematized.

if you plot your cumulative pnl from acting on a signal as a function of time (assuming you don't update anything else) it'll tend to look like this.

![](/media/puke1.png)

at least if your signal is any good.

why?

**cos what is known to you is known to others too.**

an example will be useful...

imagine you trading relative value on a futures product. 

and, to keep things easy, let's imagine you have some simple model that adjusts for predictable seasonality and basis effects, so you can compare the relative value of the contracts.

![](/media/puke2.jpg)

now, for whatever reason, the demand for immediate liquidity in contract 2 is bigger than the normal liquidity that's available.

what happens?

well, it gets distorted a bit. contract 2 is becoming temporarily too rich.

![](/media/puke3.jpg)

more buyers than sellers, innit?

so you might consider trading the butterfly: selling 2 and buying 1 and 3 to offset your directional risk.

![](/media/puke4.jpg)

in this case, your trading will introduce extra:

* supply in contract 2
* demand in 1 and 3

your trading will start to flatten the dislocation out of the market.

you may have thought that your pnl expectation in this trade is the difference between the current price contract 2 and its fair value, less your trading costs.

![](/media/puke5.jpg)

...but that's only true in the case when your trade is so tiny it doesn't move price.

i﻿n fact, at a certain size, you'll find your market impact "fixes" the whole mispricing.

![](/media/puke6.jpg)

in this case your expected pnl would be much lower than assumed above because you are:

* selling 2 at lower and lower prices
* buying 1 and 3 at slightly higher prices

as you close the gap.

n﻿ow, if some other buyside quant were to come along and look at this signal and plot it like we did before, it would look like this:

![](/media/puke7.png)

it decays instantly.

the mispricing is eaten in full, the moment it is cost effective to do so.

you might do this if you found some really juicy structural edge you didn't want anyone to know about. 

*(you're basically squashing it out of the market so it looks like an unexciting and mundane arb to everyone else.)*

**but most of the time you want to let others fix it.**

so, you put the butterfly on at a size that doesn't converge prices much*. (you might even find that you're still absorbing excess demand on 2.)*

then you wait for other people to come along and fix it.

![](/media/puke8.jpg)

if it's a good trade, they will, cos it's obvious and they like money too.

now if some other kwant looks at this, it'll look more like this.

![](/media/puke9.png)

your pnl looks better here, but others will also know about it.

so there's going to be more competition to race, front-run, or take on less edge than if you ate it all.

for example, the trader who just traded contract 2, rather than the butterfly exchanges more directional market risk for higher expected returns *(fewer costs, reduced market impact.)*

![](/media/puke10.jpg)

if they can accept that risk, they can get into the trade at a smaller mispricing than you.

there's a race towards market efficiency as people compete to squash these dislocations for profit. 

this means that any real short/medium term mispricing should converge quickly.

there's a race towards market efficiency as people compete to squash these dislocations for profit. 

this means that any real short/medium term mispricing (based on observable data) should converge quickly.

**if you're in some relative value trade and it ain't moving your way, it's more likely there's something you haven't understood than something is becoming increasingly mispriced.**

so be quick to puke these trades if they aren't converging.

the exception to this is if you're in some 3d chess trade where you believe you have information or views that the market will slowly discover over time.

you wouldn't catch me doing something like that though.

beep...boop.