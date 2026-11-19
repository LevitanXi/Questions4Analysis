---
type: Problem sets
topic: Problem&hint
status: learning
aliases:
  - 
  - 
  - 
tags:
  - real-analysis
  - set-theory
source:
created: 2026-10-28
updated: 2026-10-28
---
## W001

>[!Question] **Question*1***
>*From: Makarov - Selected Problems in Real Analysis, Ch. 3, Problem 1.21*
>
>Let $\delta>0$ and $f\in C([0,1])$. The graph of $f$ is said to have a horizontal chord of length $\delta$ if there is a point $x\in[0,1-\delta]$ such that $f(x)=f(x+\delta)$. Prove that if $f(0)=f(1)$, then for any $n\in\mathbb{N}$ there is a horizontal chord of length $1/n$. Show that for chords of a different length this is not true in general.
>
#functions #continuity

>[!hint]- Hint*1*
>Do not apply the Intermediate Value Theorem directly to f. First define the difference function g(x)=f(x+1/n)−f(x), and think about what it means for g not to take the value zero.

>[!hint]- Hint*2*
>Compute the sum of g(0), g(1/n), …, g((n−1)/n). Use f(0)=f(1) to determine whether they can all have the same sign.

>[!hint]- Hint*3*
>Counterexample part: Try to construct f(x)=x+p(x), where p is a continuous function with period δ. How can we ensure that f(0)=f(1)?

>[!Question] **Question*2***
>*From: Makarov - Selected Problems in Real Analysis, Problem 2.17*
>
>Suppose that $a_n\downarrow 0$ and let $\sum a_n=A$. For an arbitrary set $\nu\subset\mathbb{N}$, define the sum of the subseries corresponding to $\nu$ by $A(\nu)=\sum_{n\in\nu}a_n$ (by definition, $A(\varnothing)=0$). Prove that the following assertions are equivalent:
>
>(a) The sums of all subseries fill the interval $[0,A]$.
>
>(b) $a_n\le a_{n+1}+a_{n+2}+\cdots$ for all indices $n$.
>
> #series #monocity

>[!hint]- Hint*1*
>Think of the index set $\nu$ as making a choice for each $a_n$: include it or skip it. This is an infinite binary choice system.

>[!hint]- Hint*2*
>Necessity: If some $a_n$ is greater than the sum of all the terms that follow it, try to find a number that cannot be represented. Why is monotonicity needed here?

>[!hint]- Hint*3*
>Sufficiency: Given $t\in[0,A]$, decide one term at a time, starting with $n=1$, whether to include $a_n$. Try to keep the remaining target between $0$ and the sum of the unprocessed terms at every step.

---

## W002

>[!Question] **Question*1***
>*From: Makarov - Selected Problems in Real Analysis, Ch. 1, Problem 1.28*
>
>Let $K$ be the Cantor set.
>
>(a) Prove that a number $t$ belongs to $K$ if and only if it can be represented in the form $t=\sum_{j=1}^{\infty}2\varepsilon_j3^{-j}$, where each $\varepsilon_j$ is equal to $0$ or $1$.
>
>(b) Describe the sets $K+K=\{s+t\mid s,t\in K\}$ and $K-K=\{s-t\mid s,t\in K\}$.
>
> #set-theory #set

>[!Definition] **Definition*1*** Cantor set
>Let $C_0=[0,1]$ and, for $n\ge 0$, define
>$$
>C_{n+1}=\frac{1}{3}C_n\cup\left(\frac{2}{3}+\frac{1}{3}C_n\right).
>$$
>The Cantor set is $K=\bigcap_{n=0}^{\infty}C_n$.
>
>*Where, for a set $E\subseteq\mathbb{R}$, $\frac{1}{3}E=\{x/3:x\in E\}$ is its image under scaling by $1/3$, and $\frac{2}{3}+E=\{2/3+x:x\in E\}$ is its translate by $2/3$. The union takes both copies, corresponding to the left and right thirds.*

>[!hint]- Hint*1*
>Can you represent the set after the $n$th step as a union of intervals? Try using the ternary representation from the problem.

>[!hint]- Hint*2*
>Can you show that $C_n=\displaystyle\bigcup_{\varepsilon_1,\ldots,\varepsilon_n\in\{0,1\}}\left[\sum_{j=1}^{n}2\varepsilon_j3^{-j},\,\sum_{j=1}^{n}2\varepsilon_j3^{-j}+3^{-n}\right]$?

>[!hint]- Hint*3*
>For $K+K$, not hard to see $K+K \subset [0,2]$, what about converse? We may use the fact that a real number in [0,1] can be expressed by ternary. (Need to prove it.)


>[!Question] **Question*2***
>*From: Makarov - Selected Problems in Real Analysis, Ch. 3, Problem 1.7*
>
>Prove that the set of points of discontinuity of an arbitrary function on an interval $\Delta\subset\mathbb{R}$ is an $F_\sigma$-set, that is, a union of a sequence of closed sets. Is this still true if the function is defined on an arbitrary metric space?
>
> #topology #function #continuity 

>[!Definition] **Definition*2*** $F_\sigma$ set
>A set $E$ in a topological space $X$ is an $F_\sigma$ set if there exists a sequence of closed sets $(F_n)_{n\in\mathbb{N}}$ in $X$ such that
>$$
>E=\bigcup_{n=1}^{\infty}F_n.
>$$
>*(In this question, no need to know what is a topological space.)*

>[!hint]- Hint*1*
>What does it mean for $f$ to be discontinuous at $x$? Rather than treating all discontinuity points at once, can you assign a nonnegative number that measures the local “degree of discontinuity” at each point?

>[!hint]- Hint*2*
>Consider the local oscillation
>$$
>\omega_f(x)=\inf_{r>0}\sup\{|f(y)-f(z)|:y,z\in\Delta,\ |y-x|<r,\ |z-x|<r\}.
>$$
>Try to prove that $f$ is continuous at $x$ if and only if $\omega_f(x)=0$.

>[!hint]- Hint*3*
>For $\varepsilon>0$, consider $F_\varepsilon=\{x\in\Delta:\omega_f(x)\ge\varepsilon\}$. If $x\notin F_\varepsilon$, can you find a neighborhood of $x$ whose points all lie outside $F_\varepsilon$? Then consider $\varepsilon=1/n$.

---

## W003

>[!Question] **Question*1***
>*From: Makarov - Selected Problems in Real Analysis, Ch. 2, Problem 2.3*
>
>Suppose that $A$ is an infinite subset of $\mathbb{N}$, with $A=\{n_1,n_2,\ldots\}$, and let $p_n=\operatorname{card}\{m\in A:m\le n\}$. If the limit
>$$
>\theta(A)=\lim_{n\to\infty}\frac{p_n}{n}
>$$
>exists, it is called the density of $A$ (or the density of the sequence $\{n_k\}$). Prove that:
>
>(a) $\theta(A)=\displaystyle\lim_{k\to\infty}\frac{k}{n_k}$;
>
>(b) for every $\alpha\in[0,1]$, there exists a set $A\subset\mathbb{N}$ such that $\theta(A)=\alpha$.
>
> #density #sequences

>[!hint]- Hint*1*
>Suppose $n_k\le N<n_{k+1}$. What is $p_N$? Use this observation and a squeeze argument.

>[!hint]- Hint*2*
>For $0<\alpha\le1$, try to construct a set whose counting function is approximately $\alpha N$. For $\alpha=0$, construct an infinite but sufficiently sparse set separately.

>[!hint]- Hint*3*
>For $0<\alpha\le1$, consider $A=\{n\in\mathbb{N}:\lfloor\alpha n\rfloor>\lfloor\alpha(n-1)\rfloor\}$. What is $p_N$?


>[!Question] **Question*2***
>*From: Makarov - Selected Problems in Real Analysis, Ch. 3, Problem 5.2*
>
>Suppose that a function $f:\mathbb{R}\to\mathbb{R}$ satisfies the equation $f(x+y)=f(x)+f(y)$ for all $x,y\in\mathbb{R}$. Prove that:
>
>(a) $f(rx)=rf(x)$ for every $r\in\mathbb{Q}$ and $x\in\mathbb{R}$;
>
>(b) if $f$ is bounded above on some nonempty open interval, then it is linear, that is, $f(x)=ax$ for all $x\in\mathbb{R}$, where $a=f(1)$;
>
>(c) if $f$ is discontinuous at at least one point, then its graph is dense in $\mathbb{R}^2$.
>
> #functional-equations #continuity

>[!hint]- Hint*1*
>First use the additive equation to show that $f(0)=0$ and $f(-x)=-f(x)$. Then prove $f(qx)=qf(x)$ for every $q\in\mathbb{Q}$ and $x\in\mathbb{R}$; in particular, $f(q)=qf(1)$.

>[!hint]- Hint*2*
>Turn the upper bound on an open interval into an upper bound for $f$ near $0$. Then use oddness to obtain a two-sided bound near $0$.

>[!hint]- Hint*3*
>Use $f(nx)=nf(x)$ and the local bound near $0$ to prove that $f$ is continuous at $0$. Then use the density of $\mathbb{Q}$ and rational homogeneity to show that $f(x)=xf(1)$ for every $x\in\mathbb{R}$.

>[!hint]- Hint*4*
>If $f$ is discontinuous at one point, what can you conclude about its continuity and boundedness near $0$? Given an open rectangle around $(x_0,y_0)$, use unboundedness near $0$ and rational homogeneity to find a small $h$ such that $f(h)$ is close to $y_0-f(x_0)$. Then use $f(x_0+h)=f(x_0)+f(h)$.

---
## W004

>[!Question] **Question*1***
>*From: Makarov - Selected Problems in Real Analysis, Ch. 1, Problem 1.8*
>
>Determine whether there is a system $\mathfrak{A}$ of subsets of $\mathcal{P}(\mathbb{N})$ satisfying the following conditions:
>
>(a) $\mathfrak{A}$ has the cardinality of the continuum;
>
>(b) the system $\mathfrak{A}$ is linearly ordered by inclusion, that is, of any two sets in $\mathfrak{A}$, one is contained in the other.
>
> #set-theory #cardinality #order

>[!Question] **Question*2-1***
>*From: Makarov - Selected Problems in Real Analysis, Ch. 5, Problem 2.12*
>
>Two points are chosen randomly in the unit disk. What is the mean value $S$ of the area of the disk constructed with the segment joining them as a diameter?
>
> #integral #multiple-integral #geometric-probability

>[!Question] **Question*2-2***
>*From: Makarov - Selected Problems in Real Analysis, Ch. 5, Problem 2.13*
>
>Two points are chosen randomly on a circle of radius $R$. Find:
>
>a) the mean value $L$ of the length of the chord joining them;
>
>b) the mean value $\alpha$ of the angle ($\leq \pi$) formed by the radii drawn to these points.
>
> #integral #geometric-probability #random-chord

---

## W005

>[!Question] **Question*1***
>*From: Makarov - Selected Problems in Real Analysis, Ch. 1, Problem 1.19*
>
>Suppose that $E\subset\mathbb{R}$ and $(x+y)/2\in E$ for every $x,y\in E$.
>
>(a) Is it true that $E\supset[500,1000]$ if $E\supset[0,1]$ and $1992\in E$?
>
>(b) Prove that if $\operatorname{Int}E\ne\varnothing$, then $E$ is an interval.
>
> #sets #intervals

>[!Question] **Question*2***
>*From: Makarov - Selected Problems in Real Analysis, Ch. 5, Problem 2.10*
>
>Three numbers are chosen at random from the interval $[0,a]$. What is the probability that they are the lengths of the sides of a triangle?
>
> #geometric-probability #probability

---
## W006

>[!Question] **Question*1***
>*From: Makarov - Selected Problems in Real Analysis, Ch. 3, Problem 5.1*
>
>Describe all functions $f\in C(X)$ satisfying $f(2x)=f(x)$ for all $x\in X$ in the following cases:
>
>(a) $X=\mathbb{R}$;
>
>(b) $X=(0,+\infty)$.
>
> #continuity #functional-equations

>[!Question] **Question*2***
>*From: Makarov - Selected Problems in Real Analysis, Ch. 4, Problem 2.3*
>
>Let $a_n\downarrow 0$. Prove that
>$$
>\sum_{n=1}^{\infty}a_n<\infty
>\quad\Longleftrightarrow\quad
>a_n=o\!\left(\frac1n\right)\text{ and }\sum_{n=1}^{\infty}n(a_n-a_{n+1})<\infty.
>$$
>
> #series #asymptotics
