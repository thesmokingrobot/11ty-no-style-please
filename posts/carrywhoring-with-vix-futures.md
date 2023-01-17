---
title: carrywhoring with vix futures
date: 2021-09-20T00:29:55.555Z
tags:
  - post
---
in [this article](https://robotjames.com/posts/why-do-vix-futures-trade-at-a-different-price-to-the-vix-index/) we looked at vix futures and why they tend to trade at a premium to the vix index most of the time. 

> how might you apply this understanding?

let's discuss how you might think about a systematic vix carry trade based on these concepts.  

in the original article we noted:

* you can't trade vix
* so there's no market mechanism to stop it from being predictable
* but vix futures do trade and their price incorporates where the market thinks vix is likely to go.

if the market thinks vix is going to go up, the futures will likely already be trading at a premium. 

* sellers won't sell low if it's likely to go up.
* buyers will be happy to buy higher if it's likely to go up.

![](/media/cw1.jpg)

if the market thinks vix is going to go down, the futures will likely already be trading at a discount. 

* buyers won't buy high if it's likely to go down.
* sellers will be happy to sell lower if it's likely to go down.

![](/media/cw4.jpg)

to trade vix futures, it's not enough to be able to predict vix moves. 

*(everyone can do that to an extent. it's not hard. it's more likely to go up when it's low and down when it's high.)*

* vix is at 20
* you think it's going to 22 by the nearest future expiry
* but that future is trading at 22.

you might be right, but you have no trade.

![](/media/cw5.jpg)

**in trading, it's not enough to be right.**

**you have to be "more right" than the aggregate market.**

or, less wrong. 😀

there's another element tho... 

**sometimes we can make money by being prepared to take on risk others dislike**, even if we're not less wrong than the market. 

if we *could* trade vix we would rather be long than short. 

vix is positively skewed. *(moderately valued most of the time, occasional extreme high values.)*

so long vix would tend to be a high potential reward, low potential downside trade.

and short vix, the opposite.

![](/media/cw7.jpg)

vix is also negatively correlated to global risk. 

(it tends to go up when the stock market pukes.)

this makes it more attractive to be long vix. 

lots of demand for things that go up a lot when most everything else is going down.

so if being long is attractive, and being short kinda sucks...

**then we would expect vix futures, on average, to be priced higher than "where we expect vix to go."**

recall our example.

even if the market expects vix to go to 22 by expiry, the futures might still trade above 22.

because shorts demand a premium for taking on the less attractive risk profile. 

and buyers are happy to pay up for the more attractive risk profile.

![](/media/cw8.jpg)

so, even without "being able to predict the vix better than the market" there is maybe a trade for us, if we are willing to take on risk that others want to avoid.

in this case, by selling vix futures at 23 when we expect vix 22 at expiry, our expected pnl is 1 point.

![](/media/cw11.jpg)

so we can think of the premium/discount the future trades at over the index ("the basis") as consisting of two main elements:

1. where the market thinks vix is going to go by expiry
2. a premium shorts tend to demand for taking on an unattractive risk profile.

and given:

1. we can observe the basis
2. we can predict vix changes (albeit sloppily.)

if we take our prediction of vix changes away from the basis, then what remains is an estimation of the premium the market is pricing in to take the short volatility position. 

and we find reasonable evidence that this premium changes over time, and is sometimes even negative.

sometimes we appear to be well rewarded for taking short vix futures positions:

* vix at 20 
* our forecast vix 22 at expiry
* future trading at 23
* 1 point expected risk premium

![](/media/cw14.jpg)

sometimes we don't appear to be rewarded:

* vix at 20
* our forecast vix 22 at expiry
* future trading at 22
* zero expected risk premium. 

![](/media/cw15.jpg)

sometimes it appears that a long vix futures is expected to be rewarded: 

* vix at 50
* our forecast vix 46 at expiry
* future trading a 45
* \-1 point expected risk premium

![](/media/cw16.jpg)

**so - this suggests a systematic carry trade that looks something like this.** 

1. observe the basis
2. forecast the change in vix to the expiry of the future contract
3. take 2 away from 1 to get a residual "risk premium"

**if the residual "risk premium" is large, you might consider being short vix futures.**

**if the residual "risk premium" is small or negative, you might consider being long vix futures.**

*(none of this is financial advice. i'm a drunk robot on the internet, smoking a cigarette.)*

there is quite a lot to think about in the research and implementation of a simple trade like this.

* you have to deal with the fact that futures are constantly expiring.
* you have to decide what period you are forecasting over.
* you have to create the forecast (start simple).
* you have to think about sizing, and minimizing unnecessary transaction costs.

there are a lot of moving parts to consider. 

**but whatever you do, a sensible approach will have the following characteristics:**

**it will:**

* **tend to be short more often than long.**
* **require a larger premium to be short when vix is low, (and will get long on a smaller premium.)**
* **require a larger discount to be long vol when vix is high (and will get short on a smaller discount.)**
* **be sized small.**

the last point is crucial. 

if you're trading vix futures, it's only a matter of time before you experience a large vix spike when you're short.

so these things must be sized to the worst-case scenario and treated with the utmost of care.

hopefully, i have given you a useful mental model. 

the real work is in the forecast. hints:

* vix prices are mean-reverting.
* the basis itself is also important. 
* when might info-insensitive systematic pressures lead to depressed prices?
* are recent big events "remembered"?

honestly, the first one is probably good enough to get you started.

g﻿ood luck.

.﻿..

beep...boop