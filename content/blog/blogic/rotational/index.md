---
title: "Rotational Logic"
subtitle: ""
summary: ""
authors: []
tags: ["rotational logic", "logic", "fun"]
categories: []
date: 2023-03-11T11:40:09-08:00
lastmod: 2023-03-11T11:40:09-08:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: "Smart"
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []

pager: true
show_breadcrumb: true
show_related: true
---


FP Ramsey makes the following observation in the 1927 "Symposium: Facts
and Propositions":

> We might, for instance, express negation not by inserting a word
> "not," but by writing what we negate upside down. Such a symbolism is
> only inconvenient because we are not trained to perceive complicated
> symmetry about a horizontal axis, and if we adopted it we should be
> rid of the redundant "not-not," for the result of negating the
> sentence "p" twice would simply be the sentence "p" itself. (p161-2)
$\newcommand{\RR}[2]{\mathrel{\style{display: inline-block; transform: rotate(#1deg)}{#2}}}$
$\newcommand{\dotcup}{\mathbin{\unicode{x228D}}}$
$\newcommand{\dotg}{\mathbin{\unicode{x22D7}}}$


Ramsey's observation is a side comment in a larger argument about the
nature of relations between propositions, but it suggests a different
approach to logical notation. Rather than writing $\lnot p$, we can
write $\RR{180}{p}$.[^1] Perhaps
surprisingly, this rotated negation extends to more complex formulae,
capturing the De-Morgan laws.
$$\RR{180}{(p \lor q)} \leftrightarrow \lnot (p \lor q) \leftrightarrow (\lnot p \land \lnot q)$$
Using the standard notation for disjunction ($\lor$) and conjunction
($\land$), we can easily read off the meaning of a rotationally negated
formula simply by treating all logical connectives as they appear, and
rotated propositions as being negated.

Unfortunately, this happy situation does not remain for other
connectives. If $\supset$ is the material conditional, it is natural to
interpret $\RR{180}{\supset}$ as the
material conditional in the other direction, but this does
not correspond to negation.
$$\RR{180}{(p\supset q)} \leftrightarrow \lnot(p \supset q) \leftrightarrow (p \land \lnot q) \not\leftrightarrow (\lnot q \supset\lnot p)$$
Interpreting $\RR{180}{\supset}$ simply as
the negation of $\supset$ feels inelegant. Instead, we should hope that
the rotated notation intuitively conveys its meaning.

This blog post is an attempt to elaborate on what such a rotational
notation for logic would look like. During the course of exposition, we
will discover a new branch of logic (rotational logic) which deals with
invariance properties over permutations of logical connectives.

### Rotational Logic

Of Ramsey's observation, we will keep only the idea of rotating
formulas. In fact, we will make a great number of changes. Where for
Ramsey, rotation gives negation, for us it will merely result in a
change of logical connectives, not necessarily negation. Where Ramsey
rotated propositional letters, we will keep them upright, and rotate
only the connective. Where Ramsey's formulas were rotated overall
($(p \lor q)$ becomes
$\RR{180}{(p \lor q)}$), ours will be
rotated in place ($(p \RR{180}{\land}q)$
becomes $(p \land q)$). Finally, where Ramsey employs only 180 degree
rotations, we will also utilise 90 degree rotations.

Formally, the language of rotational logic is defined as follows:
$$\varphi:: = p \mid (\varphi\land\varphi) \mid (\varphi\supset\varphi) \mid {\varphi}^\circ \mid {\varphi }^\cdot$$
The notation ${\varphi}^\circ$ is understood to mean a single 90-degree rotation of the connectives in a formula. I will abbreviate this by writing:
$$\begin{aligned}
    {p}^\circ &= p \\\\
    {(\varphi\sqcup\psi)}^\circ &= ({\varphi}^\circ\RR{-90}{\sqcup}{\psi}^\circ),
    \end{aligned}$$
where $\sqcup$ is any binary operation (in any
rotation).
The notation ${\varphi}^\cdot$ indicates a change in the first truth value in a truth table for each connective. I will abbreviate this by writing a $\cdot$ inside each connective.

The language is fundamentally propositional, so we give semantic
definitions in terms of truth tables. The definition of each symbol
depends on the rotation of that symbol. We begin with the semantics for
the point symbol.
$$\begin{array}{c c | c | c | c | c}
    \varphi & \psi & (\varphi\land\psi) & (\varphi\RR{-90}{\land}\psi) & (\varphi\RR{180}{\land} \psi) & (\varphi\RR{90}{\land}\psi)\\\\
    1 & 1 & 1 & 1 & 1 & 1 \\\\
    1 & 0 & 0 & 1 & 1 & 0 \\\\
    0 & 1 & 0 & 0 & 1 & 1 \\\\
    0 & 0 & 0 & 0 & 0 & 0
    \end{array}$$
As can be seen, the $\land$ symbol matches closely
with the standard conjunction and disjunction symbols. The
$\RR{-90}{\land}$ symbol can be read as
"the truth value on the left", and
$\RR{90}{\land}$
can be read as "the truth value on the right". In this way, the symbols
and their rotations align with how we expect them to behave.

We have a similar correspondence with $\supset$, which behaves
identically to the material conditional.
$$\begin{array}{c c | c | c | c | c}
    \varphi & \psi & (\varphi\supset\psi) & (\varphi\RR{-90}{\supset}\psi) & (\varphi\RR{180}{\supset} \psi) & (\varphi\RR{90}{\supset}\psi)\\\\
    1 & 1 & 1 & 1 & 1 & 1 \\\\
    1 & 0 & 0 & 0 & 1 & 1 \\\\
    0 & 1 & 1 & 0 & 0 & 1 \\\\
    0 & 0 & 1 & 1 & 1 & 1
    \end{array}$$
As can be seen,
$\RR{180}{\supset}$
behaves like material conditional in the other direction.
$\RR{-90}{\supset}$ is the biconditional
and
$\RR{90}{\supset}$
is binary tautology.

For both sets of truth tables, the behaviour of the unfamiliar operators
$\RR{-90}{\supset}$,
$\RR{90}{\supset}$,
$\RR{-90}{\land}$ and $\RR{90}{\land}$
seems at first arbitrary. The justification for their definitions can be
seen in how we deal with ${\varphi}^\cdot$. The reader will notice that
in all truth functions thus far described, the output is $1$ when both $\varphi$ and $\psi$ have true value $1$. The $\cdot$ operator expands the system by
changing the value of the first bit.
In particular, we have the following truth tables:
$$\begin{array}{c c | c | c | c | c}
    \varphi & \psi & (\varphi\\RR{-90}{\dotg}\psi) & (\varphi\RR{-180}{\dotg}\psi) & (\varphi\RR{90}{\dotg} \psi) & (\varphi\RR{0}{\dotg}\psi)\\\\
    1 & 1 & 0 & 0 & 0 & 0 \\\\
    1 & 0 & 0 & 1 & 1 & 0 \\\\
    0 & 1 & 0 & 0 & 1 & 1 \\\\
    0 & 0 & 0 & 0 & 0 & 0
    \end{array}$$
$$\begin{array}{c c | c | c | c | c}
    \varphi & \psi & (\varphi\RR{-90}{\dotcup}\psi) & (\varphi\RR{180}{\dotcup}\psi) & (\varphi\RR{90}{\dotcup} \psi) & (\varphi\RR{}{\dotcup}\psi)\\\\
    1 & 1 & 0 & 0 & 0 & 0 \\\\
    1 & 0 & 0 & 0 & 1 & 1 \\\\
    0 & 1 & 1 & 0 & 0 & 1 \\\\
    0 & 0 & 1 & 1 & 1 & 1
    \end{array}$$

So where is the justification for our choice of semantics? Well, we now
have a relationship between the pointed operators $\land$ and the curved
operators $\supset$! What relationship, I hear you cry? Consider a
truth table for $\supset$ and
$\dotg$.
$$\begin{array}{c c | c | c}
    \varphi & \psi & (\varphi \supset\psi) & (\varphi\dotg\psi)\\\\
    1 & 1 & 1 & 0\\\\
    1 & 0 & 0 & 1\\\\
    0 & 1 & 1 & 0\\\\
    0 & 0 & 1 & 0
    \end{array}$$
The table for
$\dotg$
is the table for the negation of $\supset$! In fact, any binary
operation can be negated by switching between curve and point, and
adding a dot. We leave it to the reader to check this correspondence.

Let us summarise what we have defined. We now have a language with a
separate operator for each of the 16 possible binary boolean functions.
Our language intuitively allows us to select an operation to apply, by
combining rotations and dots. There is a natural correspondence between
the curved and the pointed symbols. Further, as the reader can check,
every pointed symbol takes $\varphi = \psi = 0$ to be false, and every
curved to be true. The system is made even more elegant by the lack of
unary operators, without losing expressiveness. To write $\neg p$, we can
instead use
$(p\RR{-90}{\dotcup}\varphi)$
for any formula $\varphi$ (again, the reader is encouraged to check
this).

### Defining Classical Logic

Call a formula *rotationally invariant* if it gives the same truth
values on every rotation. Is every formula equivalent to a rotationally
invariant formula? More specifically, are we able to define rotationally
invariant versions of the classical operators?

Negation is easy. Take
$$\neg\varphi := \varphi\dotcup\varphi.$$
It is easy to check this is equivalent to our classical $\neg \varphi$
for every rotation. Now can we obtain classical conjunction,
$\\&$? Indeed we can. Take
$$\varphi\mathbin{\\&}\psi := (((\psi\RR{180}{\land}\varphi)  \RR{90}{\land} \psi ) \land(\varphi \RR{-90}{\land} (\psi\RR{180}{\land}\varphi) )).$$
Then we have $$\begin{aligned}
    (\varphi\mathbin{\\&}\psi) &= (((\psi\RR{180}{\land}\varphi)  \RR{-90}{\land} \psi ) \land(\varphi \RR{90}{\land} (\psi\RR{180}{\land}\varphi) )) \\\\&\approx (\psi \land\varphi) \\\\\\\\
    {(\varphi\mathbin{\\&}\psi)}^\circ &= (((\psi\RR{-90}{\land}\varphi)  \land\psi ) \RR{90}{\land} (\varphi \RR{180}{\land} (\psi\RR{-90}{\land}\varphi)  ))\\\\
    &\approx (((\psi\RR{-90}{\land}\varphi)  \land\psi ) \\\\&\approx (\varphi \land\psi) \\\\\\\\
    {{(\varphi\mathbin{\\&}\psi)}^\circ}^\circ &= (((\psi\land\varphi) \RR{90}{\land} \psi ) \RR{180}{\land} (\varphi \RR{-90}{\land} (\psi\land\varphi) )) \\\\
    &\approx (((\psi\land\varphi)) \RR{180}{\land} ((\psi\land\varphi) )) \\\\&\approx (\varphi \land\psi) \\\\\\\\
    {{{(\varphi\mathbin{\\&}\psi)}^\circ}^\circ}^\circ &= (((\psi\RR{90}{\land}\varphi)  \RR{180}{\land} \psi ) \RR{-90}{\land} (\varphi \land(\psi\RR{90}{\land}\varphi) )) \\\\
    &\approx(\varphi \land(\psi\RR{90}{\land}\varphi) )) \\\\&\approx (\varphi \land\psi)
    \end{aligned}$$


[^1]: My interpretation of Ramsey as indicating a rotation, rather than a
    mirroring in the horizontal axis, is purely speculative, but it ties
    in more closely with the exposition in the rest of this paper.
