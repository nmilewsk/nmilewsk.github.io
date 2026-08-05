---
title: What is a Metric Space?
layout: default
parent: "Chapter 1: Metric Spaces"
nav_order: 1
---

# <u>What is a Metric Space?</u>

Metric spaces, and their associated metrics, have been around you your whole life whether you were aware of it or not. A metric space, very simply, is a set where you can quantify the distance between any two elements using an associated distance function, better known as a metric. Have you ever used $\\vert x-y \\vert$ to measure the difference between two numbers? How about using the distance formula $d=\\sqrt{(x_{2}-x_{1})^2 + (y_{2}-y_{1})^2}$ to find the distance between two points on the Cartesian plane? Well if so, then you have utilized metrics!

{: .definition }
> A <u><strong> metric space </strong></u> is an ordered pair $(X,d)$ where $X$ is a set and $d(x,y)$ is a metric on X.

{: .definition }
> <span id ="test1"><u>Test Definition</u></span>

[test link](#test1)

{: .definition }
> A <u><strong> metric </strong></u> on a set $X$ is a function
>
> $$
> d: X \times X \mapsto \mathbb{R}
> $$
>
> where $d$ satisfies the following conditions $\\forall x,y,z \\in X$:
>
> <span id="M1">1.</span> (Non-negativity) $d(x,y) \\geq 0$, and $d(x,y) = 0 \\iff x = y.$
> 
> <span id="M2">2.</span> (Symmetric) $d(x,y) = d(y,x).$
> 
> <span id="M3">3.</span> (Triangle Inequality) $d(x,z) \\leq d(x,y) + d(y,z).$

When you think about measuring distance between two objects intuitively, these seem very straightforward. Distance does not care about direction, so it is always positive. The distance from a to b is the same as from b to a, and the shortest path between two points is a straight line. We now move to show a couple of metrics and proving that they, with an associated set, form a metric space.

{: .theorem }
> If we let
>
> $$
> d: \mathbb{R}^2 \times \mathbb{R}^2 \mapsto \mathbb{R} 
> $$
> 
> where $\\forall{x,y} \\in \\mathbb{R}^2$, $d(x,y)$ is defined as:
>
> $$
> d(x,y)=\sqrt{(x_{1}-y_{1})^2 + (x_{2}-y_{2})^2},
> $$
>
> then $d(x,y)$ is a metric and $(\\mathbb{R}^2, d)$ is a metric space.


> Note that this is referred to as the <u><strong>Euclidean Metric</strong></u> and can be generalized for $\\mathbb{R}^n$ by
> 
> $$
> d(x,y)=\sqrt{\sum_{i=1}^n (x_{i}-y_{i})^2}
> $$


{: .proof }
> <details class="faq-container" markdown="1">
> <summary class="faq-button">Non-negativity</summary>
> <div class="faq-answer" markdown="1">
>
> $\forall{x,y} \in \mathbb{R}^2$:
>
> Note that the square root function is already non-negative, so we simply need to check $x=y \iff d(x,y) = 0$.
>
> If $x=y$, then $d(x,x)=\sqrt{(x_{1}-x_{1})^2 + (x_{2}-x_{2})^2} = \sqrt{0 + 0} = 0.$
>
> If $d(x,y) = 0$, then $(x_{1}-y_{1})^2 + (x_{2}-y_{2})^2 = 0$
> $\implies x_{1}-y_{1} = 0 = x_{2}-y_{2} \implies (x_{1},x_{2}) = (y_{1},y_{2}) \implies x = y$
>
> </div>
> </details>
>
> <details class="faq-container" markdown="1">
> <summary class="faq-button">Symmetric</summary>
> <div class="faq-answer" markdown="1">
>
> $ \\forall{x,y} \\in \\mathbb{R}^2$:
>
> $d(x,y)=\\sqrt{(x_{1}-y_{1})^2 + (x_{2}-y_{2})^2}$ 
> 
> $= \\sqrt{(-1(y_{1}-x_{1}))^2 + (-1(y_{2}-x_{2}))^2}$ 
> 
> $= \\sqrt{(-1)^2(y_{1}-x_{1})^2 + (-1)^2(y_{2}-x_{2})^2}$
> 
> $= \\sqrt{(y_{1}-x_{1})^2 + (y_{2}-x_{2})^2} = d(y,x)$
>
> </div>
> </details>
>
> <details class="faq-container" markdown="1">
> <summary class="faq-button">Triangle Inequality</summary>
> <div class="faq-answer" markdown="1">
> 
> $\\forall{(x_{1}, x_{2}), (y_{1}, y_{2}), (z_{1}, z_{2})} \\in \\mathbb{R}^2$:
>
> WTS: $\\sqrt{(x_{1}-z_{1})^2 + (x_{2}-z_{2})^2} \\leq \\sqrt{(x_{1}-y_{1})^2 + (x_{2}-y_{2})^2} + \\sqrt{(y_{1}-z_{1})^2 + (y_{2}-z_{2})^2}.$
> 
> First, let $a_{i} = (x_{i}-y_{i})$ and $b_{i} = (y_{i}-z_{i}),$ then $(x_{i}-z_{i}) = (a_{i}+b_{i}).$
> 
> It now suffices to show that $\\sqrt{(a_{1}+b_{1})^2 + (a_{2}+b_{2})^2} \\leq \\sqrt{a_{1}^2 + a_{2}^2} + \\sqrt{b_{1}^2 + b_{2}^2}.$
> 
> Squaring both sides gives us $(a_{1}+b_{1})^2 + (a_{2}+b_{2})^2 \\leq (\\sqrt{a_{1}^2 + a_{2}^2} + \\sqrt{b_{1}^2 + b_{2}^2})^2$
> 
> $\\implies a_{1}^2 + a_{2}^2 + b_{1}^2 + b_{2}^2 + 2(a_{1}b_{1} + a_{2}b_{2}) \\leq a_{1}^2 + a_{2}^2 + b_{1}^2 + b_{2}^2 + 2\\sqrt{(a_{1}^2 + a_{2}^2)(b_{1}^2 + b_{2}^2)}.$
> 
> After cancelling, we just need to show $a_{1}b_{1} + a_{2}b_{2} \\leq \\sqrt{(a_{1}^2 + a_{2}^2)(b_{1}^2 + b_{2}^2)}.$  <span id="metric1"><strong>(1)</strong></span>
> 
> Because square root is a non-negative function, we can say $(a_{1}b_{2}-a_{2}b_{1})^2 \\geq 0$
> 
> $\\implies a_{1}^2b_{2}^2+a_{2}^2b_{1}^2-2a_{1}a_{2}b_{1}b_{2} \\geq 0 \\implies a_{1}^2b_{2}^2+a_{2}^2b_{1}^2 \\geq 2a_{1}a_{2}b_{1}b_{2}.$
> 
> Note now that $(a_{1}^2+a_{2}^2)(b_{1}^2+b_{2}^2)= a_{1}^2b_{1}^2+a_{2}^2b_{2}^2 + a_{1}^2b_{2}^2+a_{2}^2b_{1}^2.$ 
> If we subtract $(a_{1}b_{1}+a_{2}b_{2})^2$ (which is non-negative), we get:
> 
> $(a_{1}^2+a_{2}^2)(b_{1}^2+b_{2}^2) \\geq a_{1}^2b_{1}^2+a_{2}^2b_{2}^2 + 2a_{1}a_{2}b_{1}b_{2} = (a_{1}b_{1} + a_{2}b_{2})^2.$
> 
> Finally, if we take the square root of both sides (since both are non-negative), we get that:
>  $a_{1}b_{1} + a_{2}b_{2} \\leq \\sqrt{(a_{1}^2 + a_{2}^2)(b_{1}^2 + b_{2}^2)} \\implies d(x,z) \\leq d(x,y) + d(y,z)$ by [(1)](#metric1).
>
> </div>
> </details>
> Thus, $d$ is a metric, and by definition $(\\mathbb{R}^2, d)$ is a metric space. $\\square$

The Euclidean Metric is fairly straightforward and indeed should make a lot of sense as to why it is considered a metric. However, metrics don't always "measure distance" in the canonical sense. Take for example the discrete metric:

{: .theorem }
> If we let
>
> $$
> d: \mathbb{R} \times \mathbb{R} \mapsto \mathbb{R} 
> $$
>
> where $\forall{x,y} \in \mathbb{R}$, $d(x,y)$ is defined as:
>
> $$
> d(x,y) = \begin{cases}
> 1 & \text{if } x \neq y \\
> 0 & \text{if } x = y,
> \end{cases}
> $$
>
> then $d(x,y)$ is a metric and $(\\mathbb{R},d)$ is a metric space.

{: .proof }
> [Non-negativity](#M1):
>
> By construction,  $\\forall{x,y} \\in \\mathbb{R}, d(x,y) \\geq 0$ and $d(x,y) = 0 \\iff x=y$
>
> [Symmetric](#M2):
>
>$\\forall{x,y} \\in \\mathbb{R}$:
>
> If $x=y$, then $d(x,y) = 0$ and $d(y,x) = 0 \\implies d(x,y) = d(y,x)$
> 
> If $x \\neq y$, then $d(x,y) = 1$ and $d(y,x) = 1 \\implies d(x,y) = d(y,x)$
>
> [Triangle Inequality](#M3):
> 
> $\\forall{x,y,z} \\in \\mathbb{R}$:
> 
> WTS: $d(x,y) \\leq d(x,z) + d(z,y)$
>
> If $x = y$, then $0 \\leq d(x,z) + d(z,y)$, which holds regardless of the value of $z$.
>
> If $x \\neq y$, then $ 1 \\leq d(x,z) + d(z,y)$. Note that his fails if $d(x,z) = 0 = d(z,y)$
>
> $\\implies x = z$ and $z = y  \\implies x = y$, which contradicts that $x \\neq y$.
>
>$\\implies \\forall{x,y,z} \\in \\mathbb{R}, d(x,y) \\leq d(x,z) + d(z,y)$, as required $\\square$


EXERCISES:

determine if they are a metric

NORMED SPACES!!!
Future Exercise: Show that, in an inner product space $V$, that the inner product $<\\cdot,\\cdot>$ induces a norm $\\lvert \\lvert \\cdot \\lvert \\rvert$, and from that every norm induces a metric (i.e. given $(V,\\lvert \\lvert \\cdot \\rvert \\rvert)$, show that $\\lvert \\lvert x-y \\rvert \\rvert$ is a metric on $V$). Conclude that every inner product space is a metric space.
