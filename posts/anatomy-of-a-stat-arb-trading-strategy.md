---
title: anatomy of a stat arb trading strategy
date: 2022-08-15T01:46:31.131Z
tags:
  - post
---
if you do not suffer from stat arb brain, it can be easy to mix up concepts like:
- expected returns
- risk modelling
- rebalancing

and when you mix concepts up together, it becomes hard to reason about things.

so let us try to get a clear view.

assume there's a bunch of assets you might be trading, and let's think about how we might go about trading them.

**the first order of business is expected return prediction.***

work out what's likely to go up most and what's likely to go down. 

your default assumption should be that stuff is roughly fairly valued outside of a discount for taking on certain risks.

but inefficiencies exist.

trend, momentum, seasonal regularities, temporary dislocations from lumpy flow etc.

so you predict expected moves for each of your assets over some forward period.

**the next order of business is risk modelling**

you want to estimate the riskiness of each asset and the extent to which stuff tends to move together.

this is useful because you can use this in conjunction with your return estimates to answer: "how do i get the biggest expected return per unit of risk?" 

"tisk" becomes the accounting unit, effectively.

you want more risk in assets with larger expected returns.

you can afford more *size* in assets that are less volatile or tend to wiggle differently to the other assets. 

now.... you might be tempted to try to distinguish between "good risk" and "bad risk". 

you don't need to.

you already should have done that in your expected return forecasts.

if not, there's something you haven't modelled in your return estimates. Go model it. 

**now you have a set of weights that you think maximizes your objectives over the next time step**

now you have a set of weights that, based on your modelling of return and risk, maximize your expected returns per unit of risk (or any other objective you have) subject to real world constraints.

so, you put the assets on in those weights.

**now, time rolls, and stuff happens in the market**

this affects you in the following ways:

1. some positions will have grown, and some will have shrunk - so you will now have different exposures to the ones you wanted. 
2. the exposures you want will also have changed because new information has appeared, and old information has become irrelevant.

this changes both your return forecasts and your risk estimates - and therefore the weights you think will maximize your objectives. 
You've ended up with different exposures to the ones you want.

if trading were free, you would trade to push them back to the weights you want continuously.

*(you think those weights are "optimal". If they're not you have more work to do.)*

**but trading costs money, and we need to think about whether it's worth doing**

in reality, you only want to rebalance when it's cost effective to do so. or when your risk exposures exceed some tolerance.

this is the rebalancing trade-off: minimizing cost of trading vs minimizing the difference between your target exposures and the ones you ended up with. 

you might be tempted to think that certain idiosyncratic rebalance approaches can harness some market effect.

if it can, that's because of an inefficiency you should have modelled in your expected return forecasts. so go back to that. 

if continuous rebalancing isn't optimal in the costless case, that's a tell that there's some return inefficiency that you haven't modelled.

so go back and try to model it. 

**keeping these concepts nice and separate will be helpful**

in the single period case, expected returns can come only from buying stuff that's too cheap (+ve expected returns) and selling stuff that's too expensive (-ve expected returns.) 

if you're seeing benefit in expected return space from certain idiosyncratic risk modelling or rebalancing schemes, that's a hint that there's non-randomness in returns you haven't modelled explicitly.

beep...boop