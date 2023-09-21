---
layout: post
title: "9.1: A Fair Game of Change"
categories: notes
chapter: "9: Recurrences and Markov Chains"
modified_date: "Sep 21, 2021"
author:
- Jovan Sardinha
---

Since the game is symetric, we can look at it from any of the two players' perspective.

Let $p(n)$ be the probability that Alice wins a+b.
The terminal condition is $p(0) = 0$.

Hence,
$$ p(n) = \frac{1}{2}p(n-1) + \frac{1}{2}p(n+1), n > 0 $$

$$2p = p(n+1) + p(n-1)$$
$$2p = p(n+1) - p(n)$$
$$2p = p(n) - p(n-1)$$

Recursively, we get
$$ p(n+1) - p = p(n) - p(n-1)$$
$$ p(n+1) - p = p(n-1) - p(n-2)$$
$$ p(n+1) - p = p(n-2) - p(n-3)$$
$$ ... $$
$$ p(n+1) - p = p(1) - p(0)$$
$$ p(n+1) - p = p(1)$$

It follows that $p(n) = np(1)$ since $p(a+b) = 1$, $p(1) = \frac{1}{a+b}$.

Hence,
$$ p(a) = \frac{a}{a+b}$$
