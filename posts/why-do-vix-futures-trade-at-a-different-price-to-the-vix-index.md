---
title: why do vix futures trade at a different price to the vix index?
date: 2021-09-14T22:41:16.126Z
tags:
  - post
---
> **why do vix futures trade at different prices to vix?**

derivatives can be complicated, but the answer to this question is not.

if you understand how the market prices risk then you'll know a lot without needing to know a lot. 

let's walk through it...

pull up a chart of the vix index.

![](/media/vix1.jpg)

if you're an experienced trader, you'll recognize immediately that this is not a thing you can trade.

> *why?*

cos it wouldn't look like that if people could trade it.

cos, just by eyeballing the time series chart, you can tell vix is very predictable:

* it stays about the same in the short term
* but if it's low it's more likely to go up
* and if it's high it's more likely to go down
* it has a floor under which it's unlikely to go lower.

![](/media/vix2.jpg)

so trading it would be really easy.

* you'd buy it when it was very low 
* you'd sell when it was higher

trading real instruments ain't that easy. 

if everyone who can look at a chart thinks it's gonna go up, there will nobody to sell it cheap. 

![](/media/vix3.jpg)

so we come toimportant point 1: ***vix is a calculation. it's not a real thing you can trade***

that's why the chart looks like that.

![](/media/vix4.jpg)

we'll discuss what vix actually is in a sec. 

but let's keep pretending we can trade it cos i have another important point to make. 

look at the vix chart again and pretend you can trade it.

> *which trade would be easier?*
>
> * *long when it's low?*
> * *short when it's high?*

the long is easier, right? 

vix essentially never goes below 9 - but it can spike to very large values. 

![](/media/vix5.jpg)

so you, as imaginary trader of untradeable indices, would rather long vix when it's low than short vix when it's high.

and you'd be happier sizing the long bigger.

cos you're relatively confident that vix isn't going to go much lower than 9.

![](/media/vix6.jpg)

but who knows how high vix could go on a spike?

if you were shorting vix that could cause you a lot of pain for you and your broker.

important point 2: **if you could trade vix you'd rather buy it than sell it.** 

*(what might this imply about the price of tradable vix bets?)* 

![](/media/vix7.jpg)

> probably time to explain what vix actually is, eh?

we're gonna hand-wave this a bit, cos it's not actually that crucial to the main question here.

and we don't wanna get lost in the weeds.

but we're traders, not neanderthals. so - here comes the science bit... 

![](/media/vix8.png)

vix is an index calculation from the cboe designed to estimate the option market's expectation of the "volatility" of spx over the next 30 days

![](/media/vix9.png)

*how do they calculate it?*

they get all spx option contracts, expiring in 30 days.

(assume they exist.)

then they ask *"what would the variance of spx returns need to be over the next 30 days to justify these prices (if we expect that spx only goes up, on average, by the risk-free rate?)"*

![](/media/vix10.jpg)

then they take the square root of that to get a number that looks like volatility. 

> *nerd aside: technically vix estimates return variance expectations, scaled to look like volatility. this is one reason it is biased higher than spx vol, as we'll touch on later.*

now, a lot was glossed over there.

but we don't need to have much more than a good insight into risk preferences to understand why tradeable vix derivatives trade at different prices to the vix index. 

**so let's introduce ourselves to vix futures.**

a vix futures contract is basically a bet on the future value of the vix index.

consider the vix futures contract that expires on 19th october 2021. 

at expiry, that contract will be worth $1,000 x the vix index.

*(the $1,000 is called the contract size - it's arbitrary.)*

![](/media/vix11.jpg)

the vix future contract is quoted in vix terms. 

so, if you long the october vix future at 20, the nominal value of your position is 20 x $1k =  $20k

on 19th october expiry, if the vix index is at 21 - then the nominal value of your position is $21k 

you made $1k

![](/media/vix12.jpg)

**stay with me...**

![](/media/vix13.png)

i know that was boring, but i thought that detail was important to cover. 

from now on we're just going to talk about prices in vix terms.

the important thing is this... 

we know the price of the vix future will converge with the value of the vix index at expiry.

and we know we can't trade vix, so there's no arb trade between index and futures. 

**so there's no invisible force tethering the vix futures to the *current* vix index value.**

![](/media/vix14.jpg)

**so vix futures are really just bets on the *future* value of vix.**

> *and what do we recall about vix from earlier?*

1. it's predictable
2. if we *could* trade it, we'd rather be long than short.

so we would expect these 2 things to be represented in the vix futures price. 

.﻿..

let's go back in time to illustrate this. 

it's 3rd jan 2018. vix closes at 9.2 - the lowest close ever.

the jan vix futures expire in 15 days, what price do they trade at?

![](/media/vix15.jpg)

consider that, for them to trade, a buyer and seller must both be happy to trade at that price.

> *would you be happy to buy jan vix futures at 9.2?*

hell yeah you would!

vix is more likely to go higher, not lower.

and it's unlikely to go much lower, but it could go a lot higher!

long at 9.2 would be a nice positive expectation bet with limited downside and huge potential upside.

![](/media/vix16.jpg)

> *would you be happy to sell jan vix futures at 9.2?*

hell no you would not!

vix is more likely to go higher, not lower.

and it's unlikely to go much lower, but it could go a lot higher!

shorting at 9.2 would be a negative expectation bet with huge potential downside and very limited upside.

![](/media/vix17.jpg)

for vix futures to trade, we need a price that both buyers and sellers are happy with. 

* buying at 9.2 is very attractive
* selling at 9.2 is very unattractive

so: 

* unhappy sellers demand a premium - they want a higher price.
* and happy buyers are willing to pay it.

**so we'd expect the jan vix futures to be trading higher than 9.2**

l﻿et's check if this actually happened...

go to <http://vixcentral.com> and click "historical prices" and go back to 3rd jan '18. 

the jan futures contract, expiring in 15 days, is priced at 10.7 - which is 1.5 points higher than the vix index.

![](/media/vix18.png)

sellers were only prepared to sell at a premium cos the bet was so unattractive.

buyers were prepared to meet them there cos the bet was so attractive. 

everyone knows vix is more likely to go up from a super low print. 

and everyone prefers high upside/low downside bets.

.﻿..

**the difference between the futures price and the index is called the "basis".**

it consists mostly of two components:

1. rational market expectation of predictable future changes in vix
2. a premium sellers demand for taking on exposures with low upside & high downside.

.﻿..

i﻿n the next article, i'll discuss how you can apply these concepts to a systematic carry trade.

.﻿..

b﻿eep...boop.