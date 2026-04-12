---
title: Notation/Introduction
layout: default
parent: Preface
nav_order: 1
---

Please note that most of the following can be defined in much greater detail in other mathematical courses. While I will do my best to include all necessary details, please note that some definitions/concepts might require more intricacy than given in this section. If so, I will cover said intricacy when the need arises.

## <u>Logic</u>

Mathematics builds upon itself by making statements and consequently proving their truth beyond any reasonable doubt. But how can we go about proving these statements/sentences? First we should fully understand the underlying logic behind such statements. 

| In mathematics, a <u><strong>statement</strong></u> is a declaration in which a boolean value can be attributed to. |


In simpler terms, a statement is a claim that it is either true or false. Common examples of these would be:

$$
\text{The number 51 is not prime.}
$$
$$
\lim{x \to \inf} \sin{x} \text{ does not exist.}
$$
$$
\sqrt{2} \text{ is irrational.}
$$

## <u>Language</u>

| A <u><strong>set</strong></u> is a collection of distinct elements. A set's elements can be characterized by either listing the elements or stating some property that the elements fulfill. |

| The <u><strong>empty set</strong></u> is the set containing no elements. The empty set is given by this notation: $\emptyset$. |

If $x$ is an element of the set $A$, we write $x \\in A$. Conversely, if $y$ is not an element of the set $A$, we write $y \\notin A$.

When stating some property that characterizes elements of some set $A$, it might come in handy to use logical quantifiers and operators. Logical quantifiers and operators help us communicate both the existence and quantity of x that fulfill the property. First we use the symbol $\\forall x$ to assert that the property holds for every $x$. Next we use the symbol $\\exists x$ to assert that the property holds for at least one $x.$ Lastly, and we won't use this symbol much at all, but we can communicate the negation of either quantifiers with this symbol: $\\neg$. We will generally denote $\\neg \\exists$ by $\\not \\exists$, but $\\neg \\forall$ is a little trickier. We generally will not use a notation for this negation, but it is equivalent to saying that there exists some $x$ where the property does not hold.

> Note that set builder notation can imply a for all quantifier without use of the symbol. For example, the following statements are referring to the same collection of elements:
>
> $$
> \{x \in A \ | \ x \neq y\}.
> $$
>
> $$
> \forall x \in A \text{ such that } x \neq y.
> $$
>
> $$
> \text{ every x in A that is not y}.
> $$

| A set $U$ is a <u><strong>subset</strong></u> of $V$ if $\\forall x \\in U$, $x \\in V.$ We denote this by $U \\subseteq V.$ |

| Similarly, a set $U$ is a <u><strong>proper subset</strong></u> of $V$ if  $\\forall x \\in U$, $x \\in V$ AND $U \\neq V.$ We denote this mainly by $U \\subset V$, but $U \\subsetneq V$ is also used occasionally. |

## Exercises

### ADD EXERCISES BASED ON QUESTIONS BELOW LATER

- We can say $A = \\{1,\\, 2,\\, 3\\}$ is a set because we have listed its elements.
- Likewise we can say $A = \\{\text{all positive integers less than }4\\}$ is a set by stating a property.
- <span>$B = \\{x\\ |\\ x > x\\} = \emptyset$.</span>
- If we have $A = \\{1,\\, 2,\\, 3\\}$, then $1 \\in A$ and $4 \\notin A.$
- Let $A=\\{0,\\, 1,\\, 2, \\, ...\\}.$
  - If we let $P(x)$ hold when $x$ is odd, then we get the following:
    - $\\forall x P(x)$ is NOT true, so its negation is true: $\\exists x \\neg P(x).$
    - $\\exists x P(x)$ is true, so its negation is NOT true: $\\not \\exists x P(x).$
