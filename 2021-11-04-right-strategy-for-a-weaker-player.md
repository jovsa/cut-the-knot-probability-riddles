---
layout: post
title: "7.17: Right Strategy for a Weaker Player"
categories: notes
chapter: "7: Conditional Probability"
modified_date: Nov 04, 2021
author:
- Jovan Sardinha

---

Given:
* `Player A`:
  * Daring game: 45% chance of losing and 55% winning
  * Conservative game: 90% draw and 10% losing.
* Q: How to make Player A win by 1 game.


From `Player A` perspective, after two games, here are the probabilities:
> Let {L,W,D} = {Loss, Win, Draw}

| Result      | Probability | Conclusion|
| --- | ---- | --- |
| LL | 0.55*0.55 = 0.3025 | Overall Loss  |
| LW | 0.55*0.45 = 0.2475 | Tiebreaker    |
| WL | 0.45*0.10 = 0.0450 | Tiebreaker    |
| WD | 0.45*0.90 = 0.4050 | Overall Win   |
$$ checkum: 0.3025 + 0.2475 + 0.0450 + 0.4050 = 1.0  $$

Hence,

$$P(tiebreaker) = 0.2475 + 0.0450 = 0.2925 $$

If A plays a daring game, then:
$$P(win) = 0.4050 $$

Hence, `Player A` total:

$$P(Win) = 0.4050 + 0.45 * 0.2925 = 0.536625$$
