---
layout: page
title: Mathematics
navigation: 2
---

# Display Mathematics

The Mathematics on this site is typeset in $$ \LaTeX $$ and rendered by [https://www.mathjax.org/](https://www.mathjax.org/)

To give you an example, the drake equation, which helps estimate the number of planets which might contain intelligent life is:

 <div>$$ N = S \times f_{p} \times n_{e} \times f_{l} \times f_{i} \times f_{c} \times f_{L} $$</div>
 
 by right clicking on this you can copy the equation, or change the way in which it is rendered.

## Interactive mathematics

Some of the mathematics on the site is interactive in some way. In this example, a parametric plot is drawn. Currently you can generate a new, different image each time you click evaluate. This is because the value "u" is randomly generated. You can edit the contents of the box below and run your own code if you like! It will reset back to default if you refresh the page.

<div class="sage">
<script type="text/x-sage">
 
d,c,p,k = [0.05, 0.05, -0.15, 0.05]
u = [random() for i in range(3)]

x(t) = (sin(t*2*pi) + sin((1-c + u[2]*c*2)*t*2*pi) + p*pi)*exp(-d*t)
y(t) = (sin((1-c+ u[0]*c*2)*t*2*pi + k*u[1]*pi) + cos((1-c + u[2]*c*2)*t*2*pi) + p*pi)*exp(-d*t)

parametric_plot((x(t),y(t)),(t,0,100),color = u, axes= False, plot_points = 3000).show()

</script>
</div>
