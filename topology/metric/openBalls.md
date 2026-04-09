---
title: Open Balls
layout: default
parent: "Chapter 1: Metric Spaces"
nav_order: 2
---

# Open Balls

{: .definition }
> Let $(X,d)$ be a metric space.
>
> An <u><strong> open ball </strong></u> of radius $r$ centered at $x_0$ is defined as:
>
> $$
> B_r(x_0) = \{x \in X \ | \ d(x_0,x) < r\}.
> $$


> Note that open balls can also be referred to as open neighborhoods

<video autoplay loop muted playsinline width="100%">
  <source src="{{ site.baseurl }}/assets/videos/OpenBall1.mp4" type="video/mp4">
</video>

Defining open balls now allow us to begin characterizing sets as opened/closed.

{: .definition }
> Let $(X,d)$ be a metric space and let $U \\subseteq X$.
>
> $U$ is <u><strong> open </strong></u> if and only if $\\forall x \\in U, \ \\exists \\epsilon > 0 \\text{ such that } B_\\epsilon(x) \\subseteq X$.

<video autoplay loop muted playsinline width="100%">
  <source src="{{ site.baseurl }}/assets/videos/OpenInterval.mp4" type="video/mp4">
</video>

{: .definition }
> Let $(X,d)$ be a metric space and let $U \\subseteq X$.
>
> A point $x$ is an <u><strong> interior point </strong></u> if $\\exists \\epsilon > 0 \\text{ such that } B_\\epsilon(x) \\subseteq X$.

{: .definition }
> Let $(X,d)$ be a metric space and let $C \\subseteq X$.
>
>$C$ is <u><strong> closed </strong></u> if and only if $X \\setminus C$ is open.

Please make a strong note for later that, for a metric space $(X,d)$, $X$ itself is open, as is $\\emptyset$. This means that $X \\setminus X = \\emptyset$, so $X$ is closed. Similarly, $X \\setminus \\emptyset = X$, so $\\emptyset$ is closed. Both of these, trivially, are known as clopen sets. There do exist sets that are both open and closed. 

{: .example }
> Consider $\\mathbb{Q}$ equipped with the standard Euclidean metric. Show that
>
> $$
> A = \{q \in \mathbb{Q} \ | \ q^2 < 2 \}.
> $$
>
> is both open and closed.

{: .proof }
> Take any $x \\in A$. By construction, $x^2 < 2$, so $x^2 - 2 < 0 \\implies  2-x^2 > 0$.
>
> We want to show that, $\\exists r > 0 \\text{ such that } \\forall y \\in \\mathbb{Q} \\vert y-x \\vert < r \\implies y \\in A$.
>
> Pick $r>0$ to be $r = min(1,\\frac{\\epsilon}{2( \\vert x \\vert +1)}) <span id="clopen1"><strong>(1)</strong></span>
>
> Let $\\epsilon = 2-x^2$. Now take arbitrary $y \\in mathbb{Q} \\text{ such that } \\vert y-x \\vert < r$.
>
> Note that $ \\vert y^2 - x^2 \\vert = \\vert y-x \\vert \\vert y+x \\vert$. By triangle inequality, $\\vert y+x \\vert = \\vert (y-x) + 2x \\vert \\leq  \\vert y-x \\vert +  \\vert 2x \\vert = \\vert y-x \\vert + 2 \\vert x \\vert$.
>
> Now $ \\vert y-x \\vert \\vert y+x \\vert \\leq \\vert y-x \\vert (\\vert y-x \\vert + 2 \\vert x \\vert)$. By choice of $y$, we have that $\\vert y-x \\vert(\\vert y-x \\vert + 2 \\vert x \\vert) < r(r + 2 \\vert x \\vert)$.
>
> By [(1)](#clopen1), $r \\leq 1 \\implies r + 2 \\vert x \\vert \\leq 1 + 2 \\vert x \\vert < 2(1 + \\vert x \\vert) \\implies r(r + 2 \\vert x \\vert) < r \\cdot 2(1 + \\vert x \\vert)$
>
> Once again by [(1)](#clopen1), $r \\leq \\frac{\\epsilon}{2(\\vert x \\vert +1)} \\implies r \\cdot 2(1 + \\vert x \\vert) \\leq \\frac{\\epsilon}{2(\\vert x \\vert +1)} \\cdot 2(1 + \\vert x \\vert) = \\epsilon$
>
> We now have $\\vert y^2 - x^2 \\vert \\leq \\vert y-x \\vert (\\vert y-x \\vert + 2 \\vert x \\vert) < r(r + 2 \\vert x \\vert) < r \\cdot 2(1 + \\vert x \\vert) \\ leq \\epsilon \\implies \\vert y^2 - x^2 \\vert < \\epsilon$
>
> $\\implies -\\epsilon < \\vert y^2 - x^2 \\vert < \\epsilon$. Since we only care about positive, this is equivalent to $y^2 < \\epsilon + x^2 = 2$.
>
> Thus $B_r(x) \\subseteq A \\implies$ A is open.
>
> Now we show that A is closed as well.
>
> Let $B = \\mathbb{Q} \\setminus A = \{q \\in \\mathbb{Q} \ \\vert \ q^2 \\geq 2 \}$.
> 
> Note that $x$ such that $x^2 = 2$ is NOT in $\\mathbb{Q}$, so $B = \{q \\in \\mathbb{Q} \ \\vert \ q^2 > 2 \}$.
>
> With the same logic as above, we take $\\epsilon = x^2 - 2$ and choose $r = min(1, \\frac{\\epsilon}{2( \\vert x \\vert +1)}).
>
> Similarly, take $y \\in B_r(x).$ Then $\\vert y^2 - x^2 \\vert \\leq \\vert y-x \\vert (\\vert y-x \\vert + 2 \\vert x \\vert) <  r(r + 2 \\vert x \\vert ) < r \\cdot 2(1 + \\vert x \\vert ) \\ leq \\epsilon \\implies \\vert y^2 - x^2 \\vert < \\epsilon$
> 
> $\\implies y^2 < \\epsilon + x^2 = 2 \\implies B_r(x) \\subseteq B \\implies$ B is open $\\implies$ A is closed.
>
> Therefore A is both open and closed $\\square$$.