Exercise 1
==========

> **Show that the set of all langauges is uncountably infinite, while
> the set of DFAs is only countably infinite**

### Answer:

If we have an alphabet $\Sigma$ that is finite and non-empty, then
$\Sigma^*$ is countably infinite as there is a bijection from
$\Sigma^* \to \mathbb{N}$. Cantor’s theorem shows us that $\mathbb{N}$
has uncountably infinite subsets.

Exercise 2
==========

### Answer, 2.1

[-\>,\>=stealth’,shorten \>=1pt,auto,node distance=2.8cm, semithick]
=[fill=red,draw=none,text=white]

\(A) <span>$1$</span>; (B) [above right of=A] <span>$2$</span>; (C)
[below right of=B] <span>$3$</span>;

\(A) edge node <span>c</span> (B) edge [loop above] node <span>b</span>
(A) edge [loop below] node <span>a</span> (A) (B) edge [loop above] node
<span>c</span> (B) (B) edge [loop below] node <span>b</span> (B) edge
node <span>a</span> (C) (C) edge [loop above] node <span>c</span> (C)
edge [loop below] node <span>b</span> (C);

### Answer, 2.2

[-\>,\>=stealth’,shorten \>=1pt,auto,node distance=2.8cm, semithick]
=[fill=red,draw=none,text=white]

\(A) <span>$1$; $S^{yes}$</span>; (B) [above right of=A] <span>$2$;
$S^{yes}$</span>; (C) [below right of=B] <span>$3$</span>;

\(A) edge node <span>c</span> (B) edge [loop above] node <span>b</span>
(A) edge [loop below] node <span>a</span> (A) (B) edge [loop above] node
<span>c</span> (B) (B) edge [loop below] node <span>b</span> (B) edge
node <span>a</span> (C) (C) edge [loop above] node <span>c</span> (C)
edge [loop below] node <span>b</span> (C);

### Answer, 2.3

[-\>,\>=stealth’,shorten \>=1pt,auto,node distance=2.8cm, semithick]
=[fill=red,draw=none,text=white]

\(A) <span>$1; S^{Yes}$</span>; (B) [right of=A] <span>$2$</span>; (C)
[right of=B] <span>$3$</span>;

\(A) edge [bend right] node <span>1</span> (B) edge [loop above] node
<span>0</span> (A) (B) edge [bend right] node <span>1</span> (A) edge
[bend right] node <span>0</span> (C) (C) edge [bend right] node
<span>0</span> (B) edge [loop above] node <span>1</span> (C);

Show that any finite language is DFA Regular
============================================

> ** **

### Answer:

We can show this via induction over the number of strings in the
language.

Base case: $\epsilon$ is the empty string Inductive Hypothesis: A finite
language $L$ is comprised of finite strings

We know that if the string ${a}$ is regular then the string $L \cup {a}$
is also regular and finite, by the IH.

Closure under complement
========================

> **Prove that if $L$ is DFA-regular, then $\bar{L}$ is DFA-regular.**

### Answer:

A DFA will make exactly one type of transition given input from a
specific state. Given DFA $M$ and language $L$, $w_1 \in L$, swapping
accept and start states of $M$, $L$ is not guarenteed to be recognized
by $M$ any longer, though as a DFA, $\bar{M}$ still can accept a regular
language. Hence, regular languages are closed (produce another set of
the same set) under complement.

Closure under Union without DeMorgan
====================================

> **If $L_1$ and $L_2$ are DFA regular, then $L_1 \cap L_2$ is DFA
> regular**

### Answer:

If we define a product automata $P$ of two automata $S,T$ with states
$s_1,
s_2, \dots s_n$ and $t_1, t_2, \dots t_m$ as a resultant $P = ST$ to be
the automata produced by the product of their individual states, such
that $P$ has state pairs $(s, t) $ with $ s \in S \text{and } t \in T$.
A product automata can be visualized as a matrix with row $S$ and column
$T$. This $P$ now recognizes the new language created by $S \cap T$.

Exercise 6
==========

> **Consider two DFAs, $M_1$ and $M_2$ with $n_1$ and $n_2$ states
> respectively. Show that if $L(M_1) \neq L(M_2)$ there is at least one
> word of length less than $n_1n_2$ that $M_1$ accepts and $M_2$ rejects
> or vice versa. Contrapositively, if all words of length less than
> $n_1n_2$ are given the same response by both DFAs, they recognize the
> same language.**

### Answer:

By making a product of $M_1$ and $M_2$…

