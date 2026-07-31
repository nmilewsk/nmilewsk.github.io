---
title: Notation/Introduction
layout: default
parent: Preface
nav_order: 1
---

Please note that most of the following can be defined in much greater detail in other mathematical courses. While I will do my best to include all necessary details, please be aware that some definitions/concepts might require more intricacy than given in this section. If so, I will cover said intricacy when the need arises.


{: .text-center}
# <u>Logic</u>



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




While all of the above are true statements, what if we had a false statement, but wanted to represent it as true? We would turn to negation. Given a statement $P$, we represent the negation of $P$ as $\\neg P$ or "not $P$." We can show the truth of $P$ and $\\neg P$ with a truth table, which is a mathematical tool to, given some initial statements, show the truth of related statements where T is true and F is false:

| $P$ | $\\neg P$ |
|:----|:----------|
|T    |F          |
|F    |T          |

This is pretty straight forward, $\\neg P$ is true when $P$ is false and vice versa. Two or more statements can be linked to form a single joined statement known as a compound statement. The truth of a compound statement relies on the truth values of the statements involved. Think about the following two statements: 

$$
\text{It is raining.}
$$

$$
\text{It is sunny.}
$$

Given these two statements, we can create two distinct compound statements: 

{: .text-center }
$$
\text{It is raining and it is sunny.}
$$ <span id="and"><strong>(1)</strong></span>

{: .text-center }
$$
\text{It is raining or it is sunny.}
$$ <span id="or"><strong>(2)</strong></span>

If we let $P=$ "it is raining" and $Q=$ "it is sunny", we can write [(1)](#and) as $P \\wedge Q$ and [(2)](#or) as $P \\lor Q$ where $\\wedge$ is a symbol for a logical AND and $\\lor$ is a symbol for logical OR[^a]. Here is a truth table for these connectives:

| $P$ | $Q$ | $P \\wedge Q$ | $P \\lor Q$ |
|:----|:----|:--------------|:------------|
|T    |T    |T              |T            |
|T    |F    |F              |T            |
|F    |T    |F              |T            |
|F    |F    |F              |F            |

Logical OR, as can be seen above, requires at least one of the statements to be true for the compound statement to be true. Meanwhile, logical AND requires every statement to be true for the compound statement to be true. Compound statements are statements themselves and can be used to form even longer/detailed compound statements. Quite often, the truth of a mathematical statement is linked to some other statement in some way. Let's assume that we have two statements, $P$ and $Q$, where the truth $P$ tells us the truth of $Q$, then we can form a conditional statement.

| A <u><strong>conditional statement</strong></u> is a statement in which the truth of a <strong>hypothesis</strong> ($P$) implies the truth of a <strong>conclusion</strong> ($Q$).|

These statements are better known as "if-then" statements and are everywhere in the world of mathematics. So given a hypothesis $P$ and a conclusion $Q$, we could say "if $P$, then $Q$" or write $P \\implies Q$. Here is a truth table for a simple conditional statement:

| $P$ | $Q$ | $P \\implies Q$ |
|:----|:----|:----------------|
|T    |T    |T                |
|T    |F    |F                |
|F    |T    |T                |
|F    |F    |T                |

This truth table might not be as straight forward as the logical AND/OR table, but first we focus on when $P \\implies Q$ should be false. $P \\implies Q$ tells us that whenever $P$ is true, $Q$ must be as well. For this to be false, we must have $P$ as true and $Q$ as false, which is where $P \\implies Q$ is listed as false. $P \\implies Q$ does <u>NOT</u> tell us about the truth of $Q$ when $P$ is false. Consider, for example, the following conditional:

{: .text-center }
$$
\text{If it is raining, then the lawn will be wet.}
$$ <span id="->"><strong>(3)</strong></span>

Indeed whenever it rains, the lawn will be wet. But what if it isn't raining, but you still watered your grass? Given this truth of our hypothesis and conclusion (i.e. $P$ is false and $Q$ is true) you say that [(3)](#->) is false? Well, for it to be false, we would need to show that it rained and the lawn was NOT wet. Since this scenario does not prove that it is false, we say that [(3)](#->) is true in this case. That seems a little confusing, because we aren't exactly confirming the conditional. However, remember that statements exist on a binary: they must either be true or false. Since [(3)](#->) cannot be false, it must be true. Now what if we had two statements, $P$ and $Q$, where the truth of $P$ implies the truth of $Q$ <u>AND</U> the truth of $Q$ implies the truth of $P$ ?

| A <u><strong>biconditional statement</strong></u> is a statement in which the truth of a <strong>hypothesis</strong> ($P$) implies the truth of a <strong>conclusion</strong> ($Q$) and vice versa. |

Given some P and Q, the biconditional statement would read "P if and only if Q" or be written as $P \\iff Q$. Since $P$ and $Q$ act as both hypotheses and conclusions, $P \\iff Q = Q \\iff P$  Here is a truth table for a biconditional statement (with $P \\implies Q$ and $Q \\implies P$ added):

| $P$ | $Q$ | $P \\implies Q$ | $Q \\implies P$ | $P \\iff Q$ |
|:----|:----|:----------------|:----------------|:------------|
|T    |T    |T                |T                |T            |
|T    |F    |F                |T                |F            |
|F    |T    |T                |F                |F            |
|F    |F    |T                |T                |T            |

Note that if either $P$ or $Q$ is true, then, in order for $P \\iff Q$ to be true, the other must also be true. To make sense of this, we again first focus on when $P \\iff Q$ would be false. We have two cases where $P \\iff Q$ is false: $P$ is true and $Q$ is false, or $Q$ is true and $P$ is false. This is because these imply that one of $P \\implies Q$ or $Q \\implies P$ is false, and $P \\iff Q$ hinges on the truth of both. The case where $P$ and $Q$ are both false ends up giving us that $P \\implies Q$ and $Q \\implies P$ are both true, so $P \\iff Q$ is also true. 

Some statements can be thought of as functions, where you have some input and the output is the truth value. Consider the following statement as an example:

{: .text-center }
$$
x \text{ is an odd number.}
$$ <span id="odd"><strong>(4)</strong></span>

This sort of statement is known as a predicate, where the input, $x$, is known as a free variable. In this case, the statement is true whenever we input an odd number. Given a predicate $P(x)$, we can form statements where their truth depends on the quantity of inputs such that the predicate is true. These statements are formed using quantifiers.

| A <u><strong>universal quantifier</strong></u> is a quantifier that means "for all" and is denoted with $\\forall$. An <u><strong> existential quantifier </strong></u> is a quantifier that means "there exists" and is denoted with $\\exists$.

Using quantifiers and [(4)](#odd) as our $P(x)$, we can form the statements $\\forall x(P(x))$ and $\\exists x(P(x))$ which read as "for every $x$, $x$ is an odd number" and "there exists $x$ such that $x$ is an odd number", respectively. We can combine everything that we've covered so far to make some pretty detailed statements. Here are some examples:

$$
\forall x(P(x) \wedge Q(x))
$$

$$
\exists x((P_1(x) \lor P_2(x)) \iff \neg Q(x))
$$

So far we've learned how to form and read statements logically, but how do we go about proving them? When you are given a statement, you are told to either prove or disprove it. There are generally three ways to go about this: direct, contradiction, or contrapositive. For any route, we first deal with the quantifier. A universally quantified statement will be of the form $\\forall x(P(x))$ and we want to assume $x$ is arbitrary and continue from there. An existentially quantified statement will be of the form $\\exists x(P(x))$, in which case you want to show that some $x$ makes $P(x)$ true.

<u><strong>Direct:</strong></u> We want to show that $P(x)$ is true. The direct route consists of no logical equivalences and working with what we're given. If $P(x)$ is NOT conditional at all, then it suffices to show that $P(x)$ is true for any arbitrary $x$, or show that $P(x)$ must be true for at least one $x$. If $P(x)$ is just conditional (i.e. $P(x) = (P \\implies Q)$), then we assume that the hypothesis holds and show that Q must also hold. If $P(x)$ is biconditional, then we prove $P \\implies Q$ and $Q \\implies P$. When you look back at the truth tables, these make sense as these are all cases where the output was true.

<u><strong>Contrapositive:</strong></u> Note proof by contrapositive requires $P(x)$ to be a conditional statement. Before we dive into the logic, consider the following truth table:

| $P$ | $Q$ | $\\neg P$ | $\\neg Q$ | $P \\implies Q$ | $\\neg Q \\implies \\neg P$ |
|:----|:----|:----------|:----------|:----------------|:----------------------------|
|T    |T    |F          |F          |T                |T                            |
|T    |F    |F          |T          |F                |F                            |
|F    |T    |T          |F          |T                |T                            |
|F    |F    |T          |T          |T                |T                            |

Note that $P \\implies Q$ and $\\neg Q \\implies \\neg P$ have the same truth values. This means that these two statements are logically equivalent. Furthermore, if two statements $P$ and $Q$ are logically equivalent, then $P$ is true if and only if $Q$ is true. Thus, to prove by contrapositive, we show that $\\neg Q \\implies \\neg P$ is true. This might seem confusing at first, but consider [(3)](#->) above. $\\neg Q \\implies \\neg P$ would be saying "if the lawn is not wet, then it did not rain" and this makes perfect sense logically. 

<u><strong>Contradiction:</strong></u>


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

[^a]: Note that logical OR can be either exclusive (ONLY one can be true) or inclusive (AT LEAST one can be true), we will generally be using inclusive.