---
title: kwant signal trade-offs in the real world
date: 2023-07-09T23:14:31.291Z
tags:
  - post
---
a couple of simple trade-off considerations re: kwant trading signals that may or may not be obvious.

here's the price of a thing....

![](/media/img1.jpg)

the main job is to predict how it's likely to move.

to do this you used information about it.

at any point: 

* new information is appearing (trades, quotes, events, chatter)
* old information, that used to be very important, is becoming less so.

![](/media/ing2.jpg)

you use this information to try to create a forecast (explicit or implicit) of how you expect price to move over some future period. 


to tell if your forecast is any good, you might get a bunch of observations of your forecast and the price changes in some period (let's say a minute).

then you might plot the subsequent returns against the forecast and, ideally, it'd look a bit like this.

![](/media/img4.png)

but you've probably got more observations than usefully fit on a scatter and it's gonna look like a big old blob cos market returns are super random.

so instead you'll do some reduction. you might sort your observations into centiles or similar and plot mean returns.

and you prob wanna transform it a bit so it is clamped to some range, likely distributed in a way you understand, and doesn't go crazy in the tails.

![](/media/centile.png)

now, being able to predict short term returns might not be the win you think it is.

trading is expensive, and it's even more expensive if you are doing when YOU want to (rather than someone else) 


if your forecast signal looks like this, you're going to have a bad time.

![](/media/pic5.jpg)

you might be really good at predicting minute ahead returns, but you don't actually want to turnover every minute.

you can't afford that.

so you'd prefer your signal to be less volatile, more auto-correlated, smoother, like this.

![](/media/likethis.jpg)

thus the first trade-off between how effective your forecast is vs how auto correlated your signal is.

**you'd prefer a smoother signal over a hyperactive jumpy one with slightly higher correlation to future returns.**

some things are naturally more auto-correlated *(carry, rv signals)* 


other naturally jumpy things can be smoothed with EWMAs and the like, which quite nicely model new information appearing and old information becoming slowly redundant. 

**we can look this from the other direction too.**

the choice of 1 min future returns was kinda arbitrary.

we might be making trading decisions on that frequency, but we don't intend to turnover on that frequency. 


so we care about how predictive our signal is over longer horizons too.

we might calculate the correlation of our signal with future returns over a range of other horizons.

and we'd much rather this decayed slowly, rather than quickly.

![](/media/decayslow.png)

if it decays quick, it's going to be very competitive to get in for the good bit.

and, if we're going to trade it successfully after costs, we're going to be have to sat in positions with zero or very low expected return until we can get out of them cost effectively. 


**so all things equal, we'd prefer the slightly less predictive thing that decayed slower.**

these trade-offs are important and aren't always easy to navigate and reason about. 

**s﻿ome tips:**

* plot everything
* keep everything as simple as it can be, chunk down, and think through things as clearly as you can
* but understand that the whole of parts interacts in wonderful confusing ways
* use simulation to explore this best you can
* thank the market gods.

b﻿eep....boop.