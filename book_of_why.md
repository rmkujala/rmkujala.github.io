# Book of Why - My introduction to causal inference (early 2021)

Some time ago I saw a friend of mine in social media praising the [Book of Why](http://bayes.cs.ucla.edu/WHY/) by Judea Pearl.
Overall it was a great read, and really made me think about statistics in a whole new way.

I won't try to summarize the whole book's contents here, but rather try to capture the "aha moments" I experienced while reading the book.

But let's start first with some words on my statistics background first. 

## Statistics background

During the early (under grad) times at university, I studied mostly math and then steered towards physics.

In physics, I naturally encountered many models describing "how the world works". 
Often we also made experiments, and for validating those we often fitted straight lines to curves and obtained error estimates to slope coeffiients using standard statistical procedures (or "recipes").

During my early studies, we had only one major statistics course involving probability calculus. 
While the basics of probability calculus seemed very logical, I found the "testing for statistically significant effects" to be cumbersome, somewhat unintuitive, and often relying on strong assumptions. You know, p-values can be a bit difficult to grasp at first, and I find them nowadays to be mostly an historical artifact that will (hopefully) soon fade away in favor of better approaches (like Bayesian modelling).

## Enter Bayes
At a later stage, I then participated a course on Bayesian modelling, and the approach for Bayesian modelling felt compelling to me due to the consistent and intuitive theoretical framework. I think I really enjoyed the fact that effect estimates were described by probability distributions instead of a "treatment effect point-estimate + p-value" -combos, which I used to work with e.g. in my Master thesis.
During this course, we eventually wen't through and implemented Bayesian estimators and samplers by hand. Luckily, since then packages like Stan have made the application of Bayesian methods orders of magnitudes easier & faster.

Compared to frequentist approaches, one key (and much debated) ingredient of Bayesian models is the introduction of prior distributions of parameter values. This, together with a probabilistic model of the data-generating process allows then for the estimated model parameter values to be expressed as easily interpretable probability distributions.

While I have not really done much work (apart from playing around with some toy examples), I had felt that Bayesian modelling was the way to go, and could not foresee anything as remarkable behind the corner. Not before I read the Book of Why.

## Book of Why - an introduction to causal modelling/inference

I grabbed the Book of Why from library after seeing it being recommended by a friend who I know to be an established expert on Bayesian inference.
In the beginning, I was a bit sceptical though, as Book of Why had also the appendum "the New Science of Cause and Effect", as some pop science books have provided similar bold promises in their titles and have not then been able to match their expectations. 

The key idea of the book, is to try to model the *causal* dependencies between different observed variables - isn't this really what we are after whenever we are analyzing data of any kind?

So, whereas Bayesian & frequentist models typically model the *correlations* between different variables, in causal modelling it is also made explitic which variable causes changes in another. While this kind of models have existed also before, the forthcoming of causal modelling (and the book and work by Judea Pearl) to me seems to be the formalization of many causal concepts (such as "necessary cause") and e.g. providing principled rules on when to consider a variable a confounder to control for (and when not!). This formalization the made it even clearer to me why double-blind random controlled trials are the primary (but not necessarily only!) way to estimate causal treatment effects. Finally, the book also touches the surface of the so-called *do*-calculus which presents a formalized set of rules that help&support estimating causal effects in the right way.

When "upgrading" from frequentist methods to Bayesian modelling the new ingredient was the introduction of priors on parameter values. In causal modelling, the key addition seems to be the inclusion of causal diagrams, which can be present using directed graphs, where the nodes are the modelled variables and directed edges point in the direction of interaction. 

Throughout the book, these causal diagrams are always the starting point for the analysis of a new problem to solve. Now, after reading the book, I think this something I should also start my every new data analysis / modelling task. If nothing else, it should clarify the problem to myself, and help understand the role of confounders.

While I'm still a novice on causal inference and will need to study the topic more, while reading the book I started to more and more think that "Why was not this stuff taught to me at school?"

## Too good to be true?

As one could expect, a pop-science book mostly focuses on the successes and does not fully bring the weaknesses/challenges of the new way of working.
As of writing, I am not yet well educated&experienced on causal (and Bayesian) inference to make my own clear assessment. 

Nonetheless, it remains to be seen (to me), whether the causal diagrams underlying the whole inference analysis can be reliably estimated in real-world scenarios.
But assuming this is possible, I would expect that in many cases there are also cyclic dependencies between the variables, and as the Book of Why did not really cover such examples, I'm not sure how the presented causal modelling approach could work out in such a scenario. Also [within the scientific community there seem to be different perspectives on how to think about causal modelling](https://statmodeling.stat.columbia.edu/2009/07/23/pearls_and_gelm/).

## Summary

While the Book of Why may (very understandably!) cuts some corners along the way, it changed the way I think about statistics and how I approach potential new modelling problems. That is no small feat! Thus I would recommend anyone working with data analysis/statistics/modelling to read through the Book of Why, while at the same time keeping a critical eye on the assumptions made.

In the book, Pearl presents causal inference as a stepping stone towards more intelligent AI as causal diagrams provide a model of the reality and thus provide means for answering "what if"-scenarios. Compared to the currently trending neural network approaches where the progress seems to come through trial and error, causal inference presents to me as an interesting alternative path towards further methodological improvements on the AI frontier. So probably one my future next reads is then the more technical/rigorous book "Causality" on the same topic (and by same author). 
