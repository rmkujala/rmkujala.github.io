# Book of Why - my introduction to causal inference

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

Compared to frequentist approaches, one key (and much debated) ingredient of Bayesian models was the introduction of prior distributions of parameter values. This, together with a probabilistic model of the data-generating process, then allows for the estimated model parameter values to be expressed as easily interpretable probability distributions.

While I have not really done much work (apart from playing around with some toy examples), I had felt that Bayesian modelling was the way to go, and did not foresee anything as remarkable behind the corner. Not before I read the Book of Why.

## Book of Why - introduction to causal modelling

I grabbed the Book of Why from library after seeing it being recommended by a friend who I know to be an established expert on Bayesian inference.
In the beginning, I was a bit sceptical though, as Book of Why had also the appendum "the New Science of Cause and Effect", as some pop science books have provided similar bold promises in their titles and have not then been able to match their expectations. 

The key idea of the book, is to try to model the *causal* dependencies between different observed variables - isn't this really what we are after whenever we are analyzing data of any kind?

So, whereas Bayesian & frequentist models typically model the *correlations* between different variables, in causal modelling it is also made explitic which variable causes changes in another. While this kind of models have existed also before, the forthcoming of causal modelling (and the book and work by Judea Pearl) to me seems to be the formalization of many causal concepts (such as "necessary cause") and e.g. providing principled rules on when to consider a variable a confounder to control for (and when not!).   Finally, the book also touches the surface of the so-called *do*-calculus helping to estimating causal effects from data.

When "upgrading" from frequentist methods to Bayesian modelling the new ingredient was the introduction of priors on parameter values. In causal modelling, the key addition seems to be the inclusion of causal diagrams, which can be present using directed graphs, where the nodes are the modelled variables and directed edges point in the direction of interaction. 

Throughout the book, these causal diagrams are always the starting point for the analysis of a new problem to solve. Now, after reading the book, I think this something I should also start my every new data analysis / modelling task. If nothing else, it should clarify the problem to myself, and help understand the role of confounders.

While I'm     

Additional assumption, causal diagrams i.e. what affects what. , what affects what?

Reasoning why double-blind random controlled trials are good for estimating causal effects.

Limitations: 
- Support only for causal structures that are DAGs, but what if there are cycles?
- How can we determine the causal diagrams in the first place? (On the other hand, bayesian model building requires similar type of modelling choices.


# Dynamic models

E.g. in physics the models are 

# Neuroscience reflections:
- functional MRI -> correlations
- dynamic causal modelling (very challenging, but the direction to go?)

# Causal modelling & AI
Neural netwo
