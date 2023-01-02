---
title: funding rate manipulation shenanigans on ftx
date: 2023-01-02T21:51:07.064Z
tags:
  - post
---
g﻿ather around, friends. 

let's talk about various manipulative shenanigans that used to go on at FTX.

we'll start with something widespread on sh1tcoin perpetual futures: **funding rate manipulation.**

if you looked at trades in the trash that FTX listed, you'd see a lot of min qty trades.



> what are they?

![](/media/perp1.png)

![](/media/perp1.jpg)

![](/media/perp1.png)

they are attempts to manipulate the funding rate of the perp.

imagine you got hold of some trash like MEDIA at a discount, but it's locked up so you can't sell it. 

as an enthusiast of "+EV" you like that you got something below fair value. 

but you know it's volatile trash.

![](/media/perp2.png)

thankfully, your mate is a resourceful meth head with the energy and drive to create a crypto futures exchange out of python and sticky tape and lies.

so you ask him to list a perp future for the shitcoin you just bought so you can short it and hedge some directional risk.

![](/media/perp3.png)

now you're long shitcoin SPOT and you're short a bunch of shitcoin PERP.

![](/media/perp4.png)

so let's turn our thoughts to the experience of holding that position...

there's a payment that occurs every hour that you hold a perpetual futures contract called "funding". 

this exists cos perpetual futures never expire. the funding payment is there to keep the futures price tethered to the price of the index it tracks.

in this case, cos FTX listed a future on absolute trash, it's likely that the "index" it tracks is just the spot price of the same trash on FTX.

![](/media/perp5.jpg)

here's how it works...

if the perp trades above the spot index, we want to make it:

* more attractive to be short (to push price down)
* less attractive to be long (so price not pushed up more)

so, traders long the future must pay traders short the future a payment called "funding"

![](/media/perrp6.jpg)

if the perp trades below the spot index, we want to make it:

* more attractive to be long (to push price up)
* less attractive to be short (so price not pushed down more)

so, traders short the future must pay funding to traders long the future.

![](/media/perp7.jpg)

this funding payment happened every hour.

the payment is the average % difference between the perp price and the index price over the hour, divided by 24.

so if the perp stayed at a constant 1% premium to the spot index, shorts would get paid 1% a day and longs would pay it.

![](/media/perp8.jpg)

now... if you knew you were going to be short this perp future for a long time, it would be nice if you could get paid funding on that position, wouldn't it?

And, in most thin sh1tcoin perp markets, you could... at least if you had a flexible enough code of ethics...

you see, when when we talk about the *price* of the perp compared to the index, what are we actually talking about?

"what is the price?" rarely has an easy answer in markets.

rather, there is: 

* the current best bid price (price we can sell)
* the current best ask price (price we can buy)
* the last traded price.

![](/media/perp9.jpg)

when FTX calculates the premium that the perp trades at over the spot for the funding calculation, they are using the "mark price" for each, which is the median of: 

* the best bid
* the best ask
* the last traded price.

in the example, the mark price would be the best bid.

because both the best bid and the last trade are the same price. 

the mark price, in this case, is below the mid price cos the last trade occurred there. this might be significant if the bid ask spread is wide...

![](/media/perp10.jpg)

but, because we expect an equal amount of buying and selling to occur, we'd expect the mark price to bounce around bid and ask and in-between as buys and sells come in and net off to around the midprice.

at least we expect that if no shenangians is going on...

![](/media/perp11.jpg)

if you were short this perp, you might be motivated to keep that orange mark price line as high as possible, so you get paid more funding.

you can do by making tiny little buy orders on the ask whenever the mark price is lower than the ask.

here's what it would look like...

![](/media/perp12.jpg)

There are a few patterns... 

first - whenever someone trades on the bid, lowering the mark price down to the bid, immediately trade on the ask afterwards to push it back up.

![](/media/perp13.png)

second - whenever the ask goes up without a trade happening, the median will be the last trade price, which is lower than the ask, within the spread.

so the mark price is lower than it could be.

in this case, you might ping a small min qty buy trade to push the mark price to the higher ask price.

![](/media/perp14.jpg)

third - if the last traded price is above the best ask, don't do anything. the mark price will stay pinned to the ask by itself.

![](/media/perp15.png)

these tactics, if nobody is fighting on the other side, can manipulate funding significantly for sh1tcoin perps with large bid/ask spread. 

imagine the spread is 1% on both perp and spot.

by trading like this to pin the mark price to the ask, you can get paid up to 0.5% per day

![](/media/perp16.jpg)

that's 180% p.a. (assuming no compounding of the funding cashflow)

but there's more....

because the index the perp tracks is simply the spot price on FTX you can do the exact opposite on the spot, trading to mark the spot price as low as possible to the best bid.

![](/media/perp17.jpg)

now you could get paid up to 1% a day manipulating funding.

which is 365% p.a.

you saw this everywhere on FTX sh1tcoin futures, especially those which should never have been listed in the first place, and for which the spot index was easily manipulated.

you'll also see it on other venues too.

don't try it at home.

beep...boop