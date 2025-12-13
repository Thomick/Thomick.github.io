---
title: "Regret Bounds for Satisficing in Multi-Armed Bandit Problems"
collection: publications
category: manuscripts
permalink: /publications/regret-bound-for-satisficing
excerpt: 'This paper explores the concept of satisficing in multi-armed bandit problems, where we aim to find solutions that exceed a satisfaction threshold rather than seeking optimal outcomes.'
date: 2023-06-09
venue: 'Transactions on Machine Learning Research'
paperurl: '/files/regret_bounds_for_satisficing.pdf'
citation: 'Michel, T., Hajiabolhassan, H., & Ortner, R. (2023). &quot;Regret Bounds for Satisficing in Multi-Armed Bandit Problems.&quot; <i>Transactions on Machine Learning Research</i>.'
---

# Satisficing in Multi-Armed Bandits

Standard reinforcement learning algorithms aim to find optimal policies, which requires extensive exploration. But in many applications, we don't actually need the best option. We just need one that's good enough. This paper studies what happens when we design algorithms around that more modest goal.

## The Satisficing Approach

We work with multi-armed bandit problems, where an agent chooses between actions (think: slot machine arms) without initially knowing their rewards. This setting lets us study the explore-exploit tradeoff in isolation, without the added complexity of navigating between states.

The term "satisficing" combines "satisfying" and "sufficing." It captures the idea of seeking adequate solutions rather than optimal ones. Given a satisfaction threshold, we want an algorithm that finds an action exceeding that threshold and commits to it, rather than continuing to explore for marginal improvements.

We introduce "satisficing regret," which measures how much an algorithm loses compared to consistently playing a satisfying action. The algorithm faces two challenges: knowing when to stop exploring because a good-enough action has been found, and knowing when to abandon an action that reveals itself to fall short of the threshold.

## Results

When a satisfactory action exists, our Sat-UCB algorithm achieves constant satisficing regret. Standard bandit algorithms show logarithmic regret growth in this setting because they keep exploring even after finding satisfactory actions, accumulating unnecessary losses. Prior satisficing algorithms in the literature lacked theoretical guarantees of this type.

When no satisfactory action exists, Sat-UCB falls back to standard logarithmic regret, so it doesn't sacrifice performance in classical bandit problems.

## Experiments

We validated the theoretical results on synthetic data. Sat-UCB outperformed standard algorithms when satisfactory actions existed and remained competitive otherwise.

We also developed Sat-UCB+, a variant that performed better in our experiments. We don't yet have theoretical guarantees for this version, but the empirical results suggest it's worth further study.

## What's Next

The natural extension is to move beyond bandits to full reinforcement learning settings and general Markov decision processes. The satisficing perspective could be useful in applications where timely decisions matter more than squeezing out the last bit of performance.

[Full paper →]({{ base_path }}/files/regret_bounds_for_satisficing.pdf)