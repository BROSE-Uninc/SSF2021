# Sensitivity Analysis Made Easy with the EMA Workbench
*"Since all models are wrong the scientist must be alert to what is importantly wrong. It is inappropriate to be concerned about mice when there are tigers abroad."* George Box, 1976.

<p align="center">
  <img src="img/logo.png" width="640"  title="What's going on?">
</p>

## TL;DR
You must do SA. Just must to. Why? Because it helps to:

* identify a subset of important model parameters,
* debug the model,
* better plan policy interventions.

If you aren't convinced yet, [here](https://www.nature.com/articles/s43588-021-00028-9) is a nice example of SA usage. So get some ☕, jump into [`sa_demo_virus_on_network.ipynb`](sa_demo_virus_on_network.ipynb) and check how easy it is now!

## SA explained visually
What to expect from SA? Let's explain it with a figure that we borred from the EMA Workbench [documentation](https://emaworkbench.readthedocs.io/en/latest/). 

Imagine an abstract model that have 5 parameters: `b`, `delta`, `mean`, `q` and `stdev`. And a single outcome of intersest `y`. We run a fancy algorithm on it and get this: a barplot 🤯. This barplot shows how impactful each on the parameters to our outcome of interest. The more the bar, the more the impact. For example, `b` is very impactful, while `delta` has no impact whatsoever. Each of the bars also have error bars in them representing confidence intervals. You can also notice that there are two types of bars: S1 and ST. These are *Sobol* indices. In short, S1 shows how much does a variable add to the variance of `y` on its own and ST shows how much does a variable add tothe variance of `y`, including all its interactions? Tricky to understand at first, but don't worry, [here](https://salib.readthedocs.io/en/latest/basics.html) is an extra reading material. To summarize, now we know which variables are "important" the most and to what extent: `beta` (the most impactful), `mean` and `q` (less impactfull). 

<p align="center">
  <img src="https://emaworkbench.readthedocs.io/en/latest/_images/indepth_tutorial_open-exploration_25_0.png" width="640" title="What's going on?">
</p>

## How to use this repo?

## Authors & acknowledgements
 *Raphael Klein* [@RaphaelKl1](https://twitter.com/RaphaelKl1),
 *Patrick Steinmann* [@steipat](https://twitter.com/steipatr),
 *Mikhail Sirenko* [@mikhailsirenko](https://twitter.com/mikhailsirenko)

 And of course we would like to thank *Jan Kwakkel* and *Marc Jaxa-Rozen* for their practical and theoretical contribution into ideas and the code behind this workshop, core developers and contributors of [EMA Workbench](https://emaworkbench.readthedocs.io/en/latest/), [Mesa: Agent-based modeling in Python 3+](https://mesa.readthedocs.io/en/stable/) and [SALib](https://salib.readthedocs.io/en/latest/).