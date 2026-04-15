---
title: Notation/Introduction
layout: default
parent: Preface
nav_order: 1
---

Please note that most of the following can be defined in much greater detail in other mathematical courses. While I will do my best to include all necessary details, please note that some definitions/concepts might require more intricacy than given in this section. If so, I will cover said intricacy when the need arises.

## <u>Logic</u>

Mathematics builds upon itself by making logical expressions and consequently proving their truth beyond any reasonable doubt. But how can we go about proving these statements/sentences? First we should fully understand the underlying logic behind such statements. 

| In mathematics, a <u><strong>statement</strong></u> is a declaration in which a truth value can be attributed to. |

In simpler terms, a statement is a claim that it is either true or false. Common examples of these would be:

$$
\text{The number 51 is not prime.}
$$
 
$$
\lim_{x \to \infty} \sin{x} \text{ does not exist.}
$$
 
$$
\sqrt{2} \text{ is irrational.}
$$

Two or more statements can be linked to form a single joined statement known as a compound statements. The truth of a compound statement relies on the truth values of the statements involved. Think about the following two statements: 

$$
\text{''It is raining."}
$$

$$
\text{''It is sunny."}
$$

Given these two statements, we can create two distinct compound statements: 

{: .text-center }
$$
\text{''It is raining and it is sunny."}
$$ <span id="and"><strong>(1)</strong></span>

{: .text-center }
$$
\text{''It is raining or it is sunny."}
$$ <span id="or"><strong>(2)</strong></span>

If we let $P=\\text{it is raining}$ and $Q=\\text{it is sunny}$, we can write [(1)](#and) as $P \\wedge Q$ and [(2)](#or) as $P \\lor Q$ where $\\wedge$ is a symbol for a logical AND and $\\lor$ is a symbol for logical OR. We can then represent the truth of [(1)](#and) and [(2)](#or) using a truth table, which is a mathematical tool used to show the value of some logical statement/expression:

| $P$ | $Q$ | $P \\wedge Q$ | $P \\lor Q$ |
|:----|:----|:--------------|:------------|
|T    |T    |T              |T            |
|T    |F    |F              |T            |
|F    |T    |F              |T            |
|F    |F    |F              |F            |

Where T/F represent the truth of the statement. Logical OR, as can be seen above, requires only one of the statements to be true for the compound statement to be true. Meanwhile, logical AND requires every statement to be true for the compound statement to be true. Note that compound statements are statements themselves and can be used to form even longer/detailed compound statements. Quite often, the truth of a mathematical statement is linked to some other statement in some way. Let's assume that we have two statements, $P$ and $Q$, where the truth $P$ tells us the truth of $Q$, then we can form a conditional statement.

| A <u><strong>conditional statement</strong></u> is a statement in which the truth of a <strong>hypothesis</strong> ($P$) implies the truth of a <strong>conclusion</strong> ($Q$).|

These statements are better known as "if-then" statements and are everywhere in the world of mathematics. So given a hypothesis $P$ and a conclusion$Q$, we could say "if $P$, then $Q$" or write $P \\implies Q$. Here is a truth table for a simple conditional statement:

| $P$ | $Q$ | $P \\implies Q$ |
|:----|:----|:----------------|
|T    |T    |T                |
|T    |F    |F                |
|F    |T    |T                |
|F    |F    |T                |

This truth table might not be as straight forward as the logical AND/OR table, but first we focus on when $P \\implies Q$ should be false. $P \\implies Q$ tells us that whenever $P$ is true, $Q$ must be as well. For this to be false, we must have $P$ as true and $Q$ as false, which is where $P \\implies Q$ is listed as false. Note that $P \\implies Q$ does <u>NOT</u> tell us about the truth of $Q$ when $P$ is false. Consider, for example, the following conditional:

{: .text-center }
$$
\text{If it is raining, the lawn will be wet.}
$$ <span id="->"><strong>(3)</strong></span>

Indeed whenever it rains, the lawn will be wet. But what if it isn't raining, but you still watered your grass? Given this truth of our hypothesis and conclusion (i.e. $P$ is false and $Q$ is true) you say that [(3)](#->) is false? Well, for it to be false, we would need to show that it rained and the lawn was NOT wet. Since this scenario does not prove that it is false, we say that [(3)](#->) is true in this case. That seems a little confusing, because we aren't exactly confirming the conditional. However, remember that statements exist on a binary: they must either be true or false. Since [(3)](#->) cannot be false, it must be true. What if we had two statements, $P$ and $Q$, where the truth of $P$ implies the truth of $Q$ <u>AND</U> the truth of $Q$ implies the truth of $P$?

| A <u><strong>biconditional statement</strong></u> is a statement in which the truth of a <strong>hypothesis</strong> ($P$) implies the truth of a <strong>conclusion</strong> ($Q$) and vice versa. |


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
