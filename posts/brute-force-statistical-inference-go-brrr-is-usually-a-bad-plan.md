---
title: brute force statistical inference go brrr is usually a bad plan
date: 2023-05-22T01:00:00.000Z
tags:
  - post
---
here are some thoughts on statistical inference in adaptive markets via a toy example...

say someone starts coming in every day at 2pm and doing a significantly large TWAP buy. 

maybe they're hedging or rebalancing or doing some other mechanical price-insensitive thing.

what happens?

![](/media/s1.jpeg)

well, we expect price to go up in that hour 

and, cos it was just a demand for liquidity with no information behind it, we expect price to go back down in the next hour when his buying stops. 

now... that's not what we necessarily see in the market.

![](/media/s2.jpeg)

we don't necessarily see price go up and revert nice and clean, cos there are a ton of other things going on at the same time.

but, if we could observe it, let's say that:

![](/media/s3.jpeg)

1. the presence of the new liquidity demand makes price go up more if the buyer wasn't there when he's buying
2. the absence of the liquidity demand when it completes makes price subsequently go down more than if the buyer wasn't there in the previous hour

now, imagine that every trader is just a data analyst / data miner, doing statistical inference, waiting for statistically significant things to happen and then acting on them. 

what happens?

well, nobody will do anything to start with. returns are swamped by noise, so nobody is going to notice the marginal impact on returns from this quickly.

maybe they notice that 2pm volume is a bit higher than usual, but anything could have caused that, stuff is super random... we only have a few data points.

so in this imaginary world in which traders are simply data analysts waiting for statistical significance, this edge persists for a while - nobody exploits it. 

eventually, it becomes obvious in the data.

the trader data analysts do their thing and the hourly return / volume patterns are now obvious. 

over time, if we're looking at expected return by hour of the day over some recent period, it's going to slowly start looking like this.

![](/media/s4.png)

and now, armed with clear evidence of a statistically significant effect, all the dataminer/traders are going to pile into the trade.

they're going to buy just before 2pm, ahead of our TWAPper, and they're going to sell to him towards the end of the hour, as he completes.

![](/media/s5.png)

what has this done?

well, they've just pulled the effect forwards.

there's now a ton more liquidity on the sell side for the 2pm TWAPper, but a demand for liquidity before that from our army of dataminer frontrunners.

![](/media/s6.png)

but, if these people are relying entirely on statistical inference, they won't realize this. 

they'll just notice, after enough observations, that they aren't making money, and the effect seems to have shifted backwards in time.

![](/media/s7.png)

given enough statistically significant observations of this, they'll change tack and do the trade earlier. 

and the same thing will happen. 

they have failed to realize that their trades - and the trades of others looking at the same obvious things - are changing the market.

now, of course, this imaginary world doesn't exist.

traders aren't just dataminers, brute forcing a search for patterns that occured in past without any context awareness.

* they know that every time someone trades, they impact the market, and leave clues.
* they know things cos ppl literally trade with them, leaking info.
* they know things because ppl gossip, and because ppl gossip, and brokers like steak lunches, wine, and talking, and lots of similar reasons.
* some of them know things cos they have good data and smart models

so what you're going to find is that ppl start front-running the 2pm TWAPper long before you can see it in the stats.

and that behaviour starts pulling the effect forward.

and other people figure it out too and they start front-running it too.

and other people work it out and start front-running the front-runners too. 

and throughout all this, the market impact is getting pulled forward and smoothed out.

the fundamental cause of the pricing inefficiency is the same (the price-insensitive buyer is the cause of all this.) but the way it impacts pricing is constantly changing due to adaptation of smart traders trying to compete for pnl.

every time someone trades or quotes, they change the market, they leave clues.

and other participants adapt, competing for pnl.

market behaviour is never static. it's changing, evolving all the time. 

so when the dataminer/trader looks back at this data they just see the average of the consequences of this game they didn't know happened.

![](/media/s8.jpeg)

maybe it just looks like a little bump, maybe it doesn't look like anything was ever really there at all. 

the data miner is going to be late to the party.

they miss the juiciest bit. they get the part others have passed up.

which leads us to a summary point.

if you need to look for market effects that can be shown to be statistically significant, they either need to be:

* super weird
* very unattractive to exploit (so they persist long enough you can find and exploit them).  

the latter tends to be called a risk premium.

this is also why lots of experienced people are always telling you that you can't brute force quant go brrrrr datamine your way to edge - at least not without some good organizing ideas based on market realities, some context-awareness, and a lot of care and attention.

beep....boop.