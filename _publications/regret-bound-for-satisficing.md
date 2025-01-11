---
title: "Regret Bounds for Satisficing in Multi-Armed Bandit Problems"
collection: publications
permalink: /publications/regret-bound-for-satisficing
excerpt: 'This paper explores the concept of satisficing in multi-armed bandit problems, where we aim to find solutions that exceed a satisfaction threshold rather than seeking optimal outcomes.'
date: 2023-06-09
venue: 'Transactions on Machine Learning Research'
paperurl: '/files/regret_bounds_for_satisficing.pdf'
citation: 'Michel, T., Hajiabolhassan, H., & Ortner, R. (2023). &quot;Regret Bounds for Satisficing in Multi-Armed Bandit Problems.&quot; <i>Transactions on Machine Learning Research</i>.'
---

## From Optimizing to Satisficing

In reinforcement learning, finding an optimal policy often requires extensive exploration. However, in many practical scenarios, we might be content with a solution that is "good enough" rather than strictly optimal. This insight led us to investigate the concept of satisficing in multi-armed bandit problems, where we seek solutions that exceed a given satisfaction threshold rather than pursuing the absolute best outcome.

We tackled this problem by introducing the notion of "satisficing regret," which measures performance relative to a satisfaction threshold rather than the optimal reward.

## Key Findings

Our research yielded interesting theoretical results:

1. In the realizable case (when a satisficing arm exists), we can achieve constant regret - a significant improvement over traditional approaches that typically have logarithmic satisficing regret bounds.

2. For the general case, our Sat-UCB algorithm achieves:
   - Constant satisficing regret when a satisficing arm exists
   - Standard logarithmic regret bounds otherwise

These results demonstrate that by relaxing the requirement to find an optimal solution, we can achieve more efficient learning in certain scenarios.

## Experimental Results

Our experimental evaluation demonstrated that Sat-UCB is not only superior to standard algorithms in the satisficing setting but also performs competitively in classic bandit scenarios. We also introduced Sat-UCB+, a modification that showed even better empirical performance, though we did not provide theoretical guarantees.

## Future Directions

This work opens up several interesting avenues for future research, particularly in extending these concepts to more complex reinforcement learning settings. While our results in the multi-armed bandit case are promising, applying similar principles to general Markov decision processes remains a challenge.

[Download paper here]({{ base_path }}/files/regret_bounds_for_satisficing.pdf)
