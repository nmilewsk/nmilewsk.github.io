---
title: Notation
parent: Preface
nav_order: 1
---

# Notation

Please note that most of the following can be defined in much greater detail in other mathematical courses. While I will do my best to include all necessary details, please note that some definitions/concepts might require more intricacy than given in this section. If so, I will cover said intricacy when the need arises.


## Language

A <u><strong>set</strong></u> (might also be referred to as a family at times) is a collection of distinct elements. A set's elements can be characterized by either listing the elements or stating some property that the elements fulfill.

The <u><strong>empty set</strong></u> is the set containing no elements. The empty set is given by this notation: $\emptyset$.
- We can say $A = \\{1,\\, 2,\\, 3\\}$ is a set because we have listed its elements.
- Likewise we can say $A = \\{\text{all positive integers less than }4\\}$ is a set by stating a property.
- <span>$B = \\{x\\ |\\ x > x\\} = \emptyset$.</span>

If $x$ is an element of the set $A$, we write $x \\in A$. Conversely, if $y$ is not an element of the set $A$, we write $y \\notin A$.

When stating a property that characterizes elements of a set, it might come in handy to use logical quantifiers. We use the symbol $\\forallx$ to denote every x. We use $\\exists$ to denote that such an x exists. These can also be negated with $\\not\\forall$ and $\\not\\exists$.
- Note that set builder notation, like in the examples above, implies a for all quantifier. For example, the following statements are referring to the same collection of elements:
$$
\\{x\\in A \\ | \\ x \\neq y\\} = \\forall x \\in A \\text{ such that } x \\neq y =  \\text{ every x in A that is not y.}
$$

## Logic
