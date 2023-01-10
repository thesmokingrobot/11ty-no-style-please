---
title: price discovery mechanisms
date: 2023-01-10T20:07:44.438Z
tags:
  - post
---
assume the purpose of a market or exchange is to find the balancing point of supply and demand where the most trading happens.

that way, the max amount of fees get collected by the venue, and customers are happy there are people to trade with.

**h﻿ow does this get achieved?**

well, let's think about what people want, and how to make as many of them content as possible...

rational buyers want to pay as little as possible, so you'll find:

* more people willing to buy at lower prices
* fewer willing to buy at high prices.

![](/media/price1.jpg)

r﻿ational sellers want to receive as much as possible, so you'll find:

* few people willing to sell at low prices
* more people willing to sell at higher prices.

![](/media/price2.jpg)

for a trade to happen, you need a buyer and a seller to both be happy with the price.

so, the amount of selling that would occur at each price is the *smaller* of the amount of buying or selling that is willing to occur at that price: the orange line.

![](/media/price3.jpg)

t﻿he process of "price discovery" is an attempt to find the price point depicted by the orange arrow below - in which the max amount of buying and selling occurs.

t﻿his can happen via a number of mechanisms. 

**i﻿n a batch auction (such as the closing auction in a stock)** participants submit the limit prices they are prepared to trade at, at what quantity. 

then the exchange can aggregate these to draw the lines we drew above. 

![](/media/price4.jpg)

t﻿he "auction price" is then the point at which the curves cross.

**i﻿n a central limit order book, price discovery is more iterative.**

"﻿the market" tries to iteratively "search" for an equilibrium price that balances supply and demand through a dance of quoting, re-quoting and taking liquidity. 

f﻿or price discovery to happen efficiently, we require:

* market makers (otherwise there's not enough people to trade with)
* i﻿nformed traders trading against them when they think their quotes are attractive.

this usually happens because:

* the market moved and market makers haven't updated their quotes yet (quotes are "stale")
* some big trader came and demanded more liquidity than is usually available, dislocating things.

A ton of infrastructure exists around these games.

**an "Automated Market Maker" (AMM) is an entirely algorithmic way of trying to iteratively find this point**, which doesn't require market makers.

effectively, price changes occur whenever someone trades with a pool. 

* buy make price go up
* s﻿ell make price go down

for this to work well, informed traders are required to trade against the pool when it is attractive to do so.

this usually happens because:

* the broad market moved, and nobody has traded with the pool yet (pool is "stale")
* some big trade came in and pushed price "too far".

.﻿..

t﻿here's a lot to say about quirks of the individual mechanisms *(esp when similar things trade in different places)* and ocasionally a lot of value in going deep on that...

.﻿.. but the overall goals and games of market price discovery mechanisms tend to look roughly the same.

b﻿eep....boop.