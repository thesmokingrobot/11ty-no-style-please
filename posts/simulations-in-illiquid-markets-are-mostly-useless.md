---
title: simulations in illiquid markets are mostly useless
date: 2023-05-28T22:29:32.020Z
tags:
  - post
---
if you naively simulate trading illiquid stuff, your assumptions around fills will totally dominate your results. 

* get a universe of illiquid stuff
* normalize it
* simulate buying the stuff that looks cheap and selling the stuff that looks expensive. 

if you simulate that assuming no trading frictions (trade at midprice whenever you want) then it will look like you can make lots of money. 

> why?

because nobody can do that.

everyone wants to get paid to donk things back into line, but to do that you need to trade with others. you can't donk the midprice.

and if there's only a few contracts quoted a mile wide, there's nobody to donk against at any good price.

if you simulate that you can trade at midprice, you're simulating an environment in which you've always got someone to trade against when you want.

in practice, you'll find that you only really got someone to trade against in size when you're wrong. 

and when you're right, poof, there's nobody there to trade with!

so, unlike your sim where you took every trade, in reality you'll miss the good trades, take the bad ones.

this is especially a problem for options, sh!tcoins etc.

i've traded illiquid stuff that required significant execution skill. it's a big job.

generally, i think you want whatever you are doing to survive taking liquidity everywhere in your sim.

b﻿eep...boop.