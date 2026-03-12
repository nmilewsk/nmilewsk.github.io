---
title: What is a Metric Space?
layout: default
parent: "Chapter 1: Metric Spaces"
nav_order: 1
---

# What is a Metric Space?

Metrics, and their associated metric spaces, have been around you your whole life. Have you ever used $\\vert x-y \\vert$ to measure the distance between two points? How about using the distance formula $d=\\sqrt{(x_{2}-x_{1})^2 + (y_{2}-y_{1})^2}$ to find the distance between two points on the Cartesian plane? Well if so, then you have utilized metric spaces!

{: .definition }
> A <u><strong> metric space </strong></u> is an ordered pair $(X,d)$ where $X$ is a set and $d(x,y)$ is a metric on X.


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

We now move to show a couple of metrics and proving that they, with an associated set, form a metric space.

{: .theorem }
> If we have $d$ be defined as follows:
>
> $$
> d: \mathbb{R}^2 \times \mathbb{R}^2 \mapsto \mathbb{R} 
> $$
> 
> where, for $x=(x_{1}, x_{2}), \\, y=(y_{1}, y_{2}) \\in \\mathbb{R}^2$, we let $d(x,y)=\\sqrt{(x_{1}-y_{1})^2 + (x_{2}-y_{2})^2}$,
> then $d(x,y)$ is a metric and $(\\mathbb{R}^2, d)$ is a metric space.


> Note that this is referred to as the <u><strong>Euclidean Metric</strong></u> and can be generalized for $\\mathbb{R}^n$ by
> 
> $$
> d(x,y)=\sqrt{\sum_{i=1}^n (x_{i}-y_{i})^2}
> $$


{: .proof }
> [Non-negativity](#M1):
> 
> Note that the square root function is already non-negative, so we simply need to check the case where $x=y$. $d(x,x)=\\sqrt{(x_{1}-x_{1})^2 + (x_{2}-x_{2})^2} = \\sqrt{0 + 0} = 0.$
>
> [Symmetric](#M2):
> 
> $d(x,y)=\\sqrt{(x_{1}-y_{1})^2 + (x_{2}-y_{2})^2}$ 
> 
> $= \\sqrt{(-1(y_{1}-x_{1}))^2 + (-1(y_{2}-x_{2}))^2}$ 
> 
> $= \\sqrt{(-1)^2(y_{1}-x_{1})^2 + (-1)^2(y_{2}-x_{2})^2}$
> 
> $= \\sqrt{(y_{1}-x_{1})^2 + (y_{2}-x_{2})^2} = d(y,x)$
> 
> [Triangle Inequality](#M3):
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
> After cancelling, we just need to show $a_{1}b_{1} + a_{2}b_{2} \\leq \\sqrt{(a_{1}^2 + a_{2}^2)(b_{1}^2 + b_{2}^2)}.$  <span id="metric1">(1)</span>
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
> Thus, $d$ is a metric, and by definition $(\\mathbb{R}^2, d)$ is a metric space. $\\square$

NEXT IS DISCRETE METRIC



NORMED SPACES!!!
Future Exercise: Show that, in an inner product space $V$, that the inner product $<\\cdot,\\cdot>$ induces a norm $\\lvert \\cdot \\rvert$, and from that every norm induces a metric (i.e. given $(V,\\lvert \\cdot \\rvert)$, show that $\\lvert x-y \\rvert$ is a metric on $V$). Conclude that every inner product space is a metric space.
