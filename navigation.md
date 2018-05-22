---
layout: page
title: Mathematics
navigation: 2
---

# Display Mathematics

The Mathematics on this site is typeset in <div>`$ \latex $`</div> and rendered by [https://www.mathjax.org/](https://www.mathjax.org/)

To give you an example, the drake equation, which helps estimate the number of planets which might contain intelligent life is:

 <div>`$$ N = S \times f_{p} \times n_{e} \times f_{l} \times f_{i} \times f_{c} \times f_{L} $$`</div>
 
 by right clicking on this you can copy the equation, or change the way in which it is rendered.

### Interactive mathematics
Below we have some python code that will simulate your results.<br>
You will notice a number of variables that you might like to investigate to see how they might affect your investigation - these include the initial population (the number of dice you start with) and the number of experiments you do (they will be automatically averaged) <br>
Each time you chage a variable, click "Evaluate" to re-run the code.
<div class="sage">
<script type="text/x-sage"># some library objects we need
from numpy.random import binomial, seed
from numpy import zeros, arange
from matplotlib import pyplot as plt
# initial population
P0 = 80
# number of rolls per experiment
n_rolls = 50
# number of experiments
n_exp = 1
# probability that any given die will "decay" on a given roll
p = 1/6
# location to track average dice remaining for each roll number
pop_avg = zeros(n_rolls+1)
# "seed" the random number generator
# (This makes the results look different
# each time the code is run.)
seed()
# loop over experiments
for n in range(n_exp):
  # reset the dice population
  P = P0
  # roll the dice
  for k in range(1,n_rolls+1):
    # figure out how many dice decay this time
    r = binomial(P,p)
    # remove the dice
    P -= r
    # update the average
    pop_avg[k] += P
# final division to compute the averages
pop_avg /= n_exp
# we always started with P0
pop_avg[0] = P0
# compute the model predictions
model = (1.0-p)**arange(n_rolls+1.0)*P0
pl1 = list_plot(pop_avg,plotjoined=True,marker='+',legend_label='Model results',axes_labels=['roll #', '# dice'])
pl2 = list_plot(model,plotjoined=True,linestyle='--',color='red',marker='x',legend_label='Theoretical curve')
show(pl1+pl2)
</script>
</div>

## Adding a Page to Navigation

Not every page by default is part of the navigation. If you want to add a page to the navigation you have to add the `navigation` attribute with a desired `index`:

```
---
layout: page
title: Navigation
navigation: 2
---
```

The navigation `index` is starting with 1 representing the first item. 
