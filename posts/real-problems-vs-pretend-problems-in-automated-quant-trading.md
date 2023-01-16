---
title: real problems vs pretend problems in automated quant trading
date: 2022-03-22T04:37:42.408Z
tags:
  - post
---
occasionally i read a long twitter thread about some quant thing.

and - let's try to be kind - it is clear the person is writing from an "inspirational" rather than "experiential" standpoint.

such threads often discuss:

* things that would be infeasible to manage in a production trading environment without a massive team
* things that would be a terribly naive thing to prioritize unless you were already extremely operationally advanced.

**the problems you'll actually have tend to be much more mundane than the glamorous ones you'll think you'll have.**

allow me to provide some color...

any good trading strategy will be centered around a single idea.

you should be able to explain it in a few sentences.

you need to know:

1. why people are willing or forced to trade at prices that are disadvantageous to them
2. why, in a highly competitive market, you get to be the party taking the other side of those trades.

answer those questions convincingly, backed up with data, and you have a sensible starting point. 

**now, model that effect in the very *simplest, most direct way possible*.** 

and i really mean that. throw away the de prado textbook. model it as simply and directly as you can.

now you've modelled the effect in theoretical land. 

and you think your model explains enough about future price moves that you can trade it profitably in the real world.

your model is as simple and direct as it can be without taking unreasonable shortcuts.

then internet quant thread guy appears: 

> "dude. you're gonna leave money on the table. there are tons of microstructural reversion & x-asset rv effects that you could harness with this statistical learning model technique."

and he's not necessarily *entirely* wrong...

but you'd be entirely wrong to listen to him. 

when you put your model live, you're going to find:

1. there's a wide gap between actual trading performance and the predictive performance of your model
2. you quickly become overwhelmed by the sheer number of jobs you have.

**the first is mostly caused by the fact that markets are highly competitive.**

what you see as a good opportunity, others also see. so being able to trade there is highly competitive.

what you *think* is a good opportunity, but isn't, will be uncompetitive.

so, you'll be getting filled much more often on your uncompetitive shitty bets than your competitive good bets.

adverse selection innit?

**your second problem is that literally everything is uncertain and needs to be tracked and managed.**

you have two data feeds?

each one arrives slow. 

and the slowness of them is variable. and different for each feed.

and they fall over. and some of the data is just wrong.

and you've gottta handle all this operational stuff.

you got all these jobs, plus you gotta work proactively to minimize the mean and variance of the latency of each feed - and try to align them as best as you can whilst under uncertainty.

and every bit of code you make is an overhead and a potential liability.

**you have two simple features?** 

doesn't sound much, right?

but you've still got to monitor everything. 

is the distribution you're seeing the same as you expect? is scaling ok?

are misalignments, outliers or downtime screwing up your feature generation? better deal with that.

**now the predictive model...**

is it behaving the way you expect? gotta monitor it. does it need to be re-fit?

this stuff all gets harder to reason about the more stuff you threw in there.

hopefully you kept it simple.

**now the trading logic...**

you've got to track order state and risk exposures. 

and you find these problems are really *prediction* problems.

you don't know you got filled till some time afterwards. do you wait? or predict? 

your exposure is really a probabilistic thing.

and let's not even talk about the reconciliations and other checks and balances you have to do...

**your most important problem now is likely:**

* your theoretical model is still performing fine
* but your trading is significantly worse.

so you gotta chunk down and work out why.

you'll find - as @0xdoug has mentioned previously - that "it's not just one thing, it's everything" 

but you chunk down, make your way through it.

some of the work to fix it *might* be "make the theoretical predictive model more effective" - but you wouldn't start there.

the impression i am trying to give here is this...

**even with the simplest, most direct model of what you are trying to trade - you are going to find yourself completely overwhelmed with operational jobs and data analysis problems.**

so, you see some thread about throwing multiple x-asset rv factors and microstructure features at <statistical learning thing> to explain a teeny bit more market variance.

that's cool and all, but explaining theoretical variance is unlikely to be one of your bigger problems.

and everything you add introduces more jobs, confusion, and failure points. 

if you concentrate on large scale feature gen and sophisticated statistical modelling techniques in this context, either:

* you're already very operationally sophisticated
* you skipped a ton of steps

it's absolute chaos out there.

chunk down as small as possible, and prioritize the stuff that actually matters. the real jobs you know you have. not the stuff you read online. 

b﻿eep...boop.