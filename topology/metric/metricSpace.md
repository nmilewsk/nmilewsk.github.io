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
> $$
> d: X \times X \mapsto \mathbb{R}
> $$
> such that that $d$ satisfies the following conditions $\\forall x,y,z \\in X.$
> 1. (Non-negativity) $d(x,y) \\geq 0$, and $d(x,y) = 0 \\iff x = y.$
> 2. (Symmetry) $d(x,y) = d(y,x).$
> 3. (Triangle Inequality) $d(x,z) \\leq d(x,y) + d(y,z).$