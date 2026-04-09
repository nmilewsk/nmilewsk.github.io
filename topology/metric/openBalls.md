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
  <source src="{{ site.baseurl }}/assets/videos/OpenBall.mp4" type="video/mp4">
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