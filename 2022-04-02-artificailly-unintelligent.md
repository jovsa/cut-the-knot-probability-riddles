---
layout: post
title: "9.6: Artificially Unintelligent"
categories: notes
chapter: "9: Recurrence and Markov Chains"
modified_date: April 02, 2022
author:
- Jovan Sardinha

---

### Question

An electronic device is being devised for transmitting 1 bit of information at a time. So far, the device is not 100% reliable. With the probability `p` the bit is transmitted correctly; otherwise, it's flipped.

`n` such devices are chained output to input and the first receives a bit. What is the probability that the bit will be transmitted correctly throughout the chain of `n` devices?

### Approach

The binomial theorem:

$$ (a+b)^n = \sum_{k=0}^n \binom{n}{k} a^{n-k} b^k $$

We can use this but only for the even number of failures. Hence,

$$ P = \sum_{k=0}^n \binom{n}{k} p^{n-k} (1-p)^k * \frac{1+(-1)^k}{2} $$

$$ P = \frac{1}{2}(\sum_{k=0}^n \binom{n}{k} p^{n-k} (1-p)^k)+\frac{1}{2}(\sum_{k=0}^n \binom{n}{k} p^{n-k} (p-1)^k) $$

$$P = \frac{1}{2}((p + (1-p))^n+ (2p-1)^n) $$
$$P = \frac{1}{2} + \frac{1}{2}(2p-1)^n $$


