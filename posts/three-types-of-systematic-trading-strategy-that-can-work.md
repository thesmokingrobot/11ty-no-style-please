---
title: three types of systematic trading strategy that can "work"
date: 2021-03-09T23:23:45.832Z
tags:
  - post
---
broadly, there are 3 types of systematic trading strategy that can "work".

in order of increasing turnover:

1. risk premia harvesting
2. economically-sensible, statistically-quantifiable slow-converging inefficiencies
3. trading fast-converging supply/demand imbalances

.﻿..

**1) r﻿isk premia harvesting** is typically the domain of wealth management, but it's important to any trader who likes money.

a "risk premium" is the excess return you might expect over and above risk-free cashflows for taking on certain unattractive risks.

"equity risk premium", for example, is how you say "stonks, they go up" if you work for blackrock *(though, they're really referring to the extent to which they "go up" more than an equivalent less risky thing.)* 

the basics of risk premia harvesting are:

* intentionally expose your portfolio to diverse sources of risk that tend to be rewarded
* manage risk sensibly so no risk dominates at any time
* be patient and chill the f out (hardest bit for most)

a very simple example is the 60/40 stock/bond portfolio.

more balanced implementations include bridgewater's "all weather" portfolio and "risk parity" strategies, generally, which attempt to equalize risk across assets or risk premia. 

**"doing useful things"** like providing liquidity in a highly stressed market - or making a 2 sided market at all times are also, arguably "risk premia harvesting".

(you're taking on the risk of getting run over by those who can choose when to trade) 
risk premia harvesting is something nearly every trader should do.

all active traders need to be aware of it too

*want to short stocks?* 

you're facing a big hurdle. you need to be right over and above the expected drift in the asset.

**it's better to play easy games than hard ones.**

.﻿..

**2) economically-sensible, statistically-quantifiable slow-converging inefficiencies.**

these are noisy tendencies for assets to trade too cheap/expensive at certain times due to behavioural or structural effects. 
examples include momentum effects, seasonal regularities, effects due to indexing inclusion/exclusion.

we can probably lump "style factors" (momentum, value, carry, quality, low vol) and most medium freq "stat arb" approaches in this bucket too. 
this stuff tends to be noisy and "slow converging".

it's just a noisy tendency for "cheap stuff to outperform expensive stuff" (say)

so you have to analyze it "in aggregate" over large data sets.

it also means that your p&l is very slow to converge to "expected returns" 
so to trade this stuff effectively we need:

* to understand why the inefficiency would persist
* faster converging metrics around what we're exploiting so we're not "the last to know" when the inefficiency disappears
* patience and discipline to "keep swinging the bat" 

u﻿seful sources for this kind of stuff include:

* expected returns, antti ilmanen
* efficiently inefficient - pedersen
* positional option trading - sinclair
* active portfolio management - grinhold, kahn 

generally, this stuff is less reliable than 1) risk premia harvesting and 3) fast-converging flow effects.

**"home gamer" traders usually spend too much time here, and too little time on risk premia harvesting.**

and active managers of size play here tho they'd probably rather be playing 3) if they could...

.﻿..

**3) trading fast-converging supply-demand imbalances**

this stuff is the bread-and-butter of proprietary trading firms.

short term supply/demand imbalances create dislocations in prices which fast traders can "disperse" by trading against and offsetting risk elsewhere. 
these trades are conceptually simple and economically sound.

for example, i might buy sell futures on shanghai ine and buy a similar contract cheaper on singapore sgx for a profit (after costs).

that's a simple "arb" though it carries risks cos we can't trade instantaneously 
more normally though, we're doing riskier trades that we expect to work out on average.

we're serially looking to buy cheap and sell high based usually on simple relative-value models.

the assumption is made that deviations from (relative) fair value will converge... 
so models are less about "predicting the future" (as per 2) and more about "extrapolating the present" (q vs p).

> "but you're *predicting* convergence to your model of fair value you're using to quantify cheap/expensive?"

yeah, exactly. 

advantages of these trades are:

* they're easy to understand and economically simple
* they converge fast to expected pnl. you know quickly when your model is out or you don't have edge anymore. they fit nicely with @krisabdelmessih's "measurement and normalization" paradigm 

disadvantages are that they are capital constrained (you can only eat what you are fed) and require significant investment in infrastructure and staff.

whilst this area isn't practical for "home gamers", the lessons here are crucial for a good understanding of the market. 

**takeaways for "home gamers"**

* do more of 1) and less of 2)
* dig into 3) to understand and appreciate "the terrifying efficiency of the markets" but don't think you can compete there.

b﻿eep...boop.