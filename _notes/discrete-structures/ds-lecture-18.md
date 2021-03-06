---
date: 2020-10-27
title: DS lecture 18
author: Shashwat Singh
code: ma5.101
number: 18
---

# Mathematical induction  
## Peano's postulates on $\mathbb{N}$  
- **postulate 1**: $1 \in \mathbb{N}$ , that is 1 is a natural number.  
- **posulate 2**: for each $n \in \mathbb{N}$ , there exists a unique natural number $n^+ \in \mathbb{N}$ called the successor $| n^+ = n + 1$  
- **postulate 3**: $1$ is not the successor of any natural number.  
- **postulate 4**: if $m, n \in \mathbb{N}$ and $m = n$ then $m^+ = n^+$ i.e. each natural number if a successor is the successor of a unque natural number.  
- **postulate 5**: if $k \subseteq \mathbb{N}$ such that $1 \in K$ and $n \in K \implies n^+ \in K$ then $K = N$  
**Deduction 1**: Every element $n|n \in \mathbb{N}$ and $n \not=1$ is the successor of some other element in $\mathbb{N}$  
**Deduction 2**: $m^+ \not= m \forall m\in N$  

## Order relations in the system of natural numbers  
- **Law of trichotomy**: if $m, n \in \mathbb{N}$, any of the following *must* hold:   
        - $m > n$ 
        - $m = n$
        - $m < n$ 
- **Law of transitivity**: if $m, n, p, \in \mathbb{N}$ then $(m > n) \land (n > p) \implies m > p$
- **Monotone law of addition**: if $m, n, p \in \mathbb{N}$ then $m > n \implies m + p > n + p$
- **Monotone law of multiplication**: if $m, n, p \in \mathbb{N}$ then $m > n \implies m.p > n.p$

## Well ordering principle  
The set of all natural numbers is said to be *well-ordered* that is, every non empty subset of $\mathbb{N}$ has a least element.  

## First principle of Mathmatical induction  
For a given open open statement $P(n)$ involving $n|n \in \mathbb{N}$ *if* we can show that:  
1.  $P(n_0)$ is true
2.  and $P(k+1)$ is true given for an **arbitrarily chosen but particular** $k$ $P(k)$ is true.  
Then we can conclude that $P(n)$ is true for all natural number $n \geq n_0$  
- First step is referred to as the basis of induction
- Second step is referred to as the *induction step* and the assumption that $P(k)$ is true is referred to as the induction hypothesis. 

**Proof**:  
Let $P(n)$ be an open statement satisfying conditions (1.) and (2.) and let $A = \{t \in \mathbb{N} \land t \geq n_0 | P(t) \text{is false}\}$ note that $A \subset \mathbb{N}$. We need to prove that $A = \phi$ and thus we assume the *contrary* that is $A \not= \phi$ and thus by the *well ordering principle* we can conclude that $A$ has a least number. Let $m$ be the least element of  $A$, we know that $m \not= n_0$ because $P(n_0)$ is true by condition (1.) and thus $m > n_0$ . By our definition of $A$ we can also say that $P(m-1)$ is true and since $P(n)$ also adheres to condition (2.): if $P((m-1)+1)$is also true  there will be a contradiction.  
Hence, by proof by contradiction, we can say that $A = \phi$ if 1. and 2. imply $A = \phi$ .  
or in other words $P(n)$ is true for all elements $n|n > n_0$ 

## Second principle of mathematical induction  
For a given statement $P(n)$ involving a natural number $n$ if we can show that:
1. $P(n)$ is true for $n = n_0$ 
2. The statement $P(n)$ is true for $n = k + 1$ assuming it is true for $n_0 \geq k \geq n$  
The we can conclude that $P(n)$ is true for all natural numbers $n \geq n_0$  
- The first step is called the basis of inductions 
- The second step is called the induction step and the assumption is called induction hypothesis.  
  
This can be proved in a very similar way as the first principle.  

## Tips and template for using Methematical induction  
- Express the statement that is to proved in the form "for all $n \geq b, P(n)$" for a particular integer $b$ 
- We need to show $P(b)$ is true, this is the basis case.
- Write out the inductive step, i.e. assuming $P(k)$, $k \geq b$ for an arbitrarily chosen particular $k$ is true. 
- Now show that $P(k+1$ ) is also true. 
- "$P(n)$ is true for all $n \geq b$" 
