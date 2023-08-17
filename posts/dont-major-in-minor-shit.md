---
title: don't major in minor shit
date: 2023-06-28T23:50:03.701Z
tags:
  - post
---
if you try to teach yourself quant trading from the internet or from scientific papers, you run the risk of spending a lot of time majoring on minor shit.

you see it on twitter all the time. well-meaning beginner kwants are spending time worrying about niche modelling or inference techniques, rather than trying to understand and model market effect directly.

**the simplest, closest-to-hand tool for the job is what you want.**

at least to start. 

> **need to adjust for volatility?**

good, that's predictably time varying - you should do that.

but don't reach for some fancy forecast you need to fit.

use recent realized, estimated in an easy way, over an intuitively sensible period, based on what effects you're looking for. 

> **need to smooth something?**

good, that's important in lots of ways - not least that it's incredibly expensive to trade something that's jumping around all over the place.

you want something where it's easy to reason how old info is expiring and new info incorporated. 
nothing fancy.

you reach for a rolling mean/median or exponential smoothing first - depending on what you're trying to model.

>  **need to reduce trading?**

good, of course you do.

but don't suddenly start reading about multi-period optimization or some new-fangled thing.

focus on the simple causes first: can your signals be smoothed more? are your risk estimates as stable as they can be? 

then maybe you can incorporate some simple heuristics to reduce your trading before you get lost in the black hole of portfolio optimizer fuckery?

**trading systems get complicated and hard-to-reason-about at an alarming rate.** 

you want to keep things as simple as they can be. 


>
> *probably worth pointing out that the reason you'll see experienced practitioners writing about interesting new techniques is because they're not allowed to write about the stuff that matters.*
>
> *and the reason most others do is cos they don't know that stuff doesn't really matter.*

b﻿eep....boop