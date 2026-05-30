---
title: "DP-SPRT: Differentially Private Sequential Probability Ratio Tests"
collection: publications
category: conferences
permalink: /publications/dp-sprt
date: 2026-05-01
venue: 'International Conference on Artificial Intelligence and Statistics (AISTATS)'
paperurl: 'https://arxiv.org/abs/2508.06377'
citation: 'Michel, T., Basu, D., &amp; Kaufmann, E. (2026). &quot;DP-SPRT: Differentially Private Sequential Probability Ratio Tests.&quot; <i>The 29th International Conference on Artificial Intelligence and Statistics (AISTATS)</i>. Spotlight presentation.'
excerpt: 'We revisit Wald''s celebrated Sequential Probability Ratio Test for sequential tests of two simple hypotheses, under privacy constraints. We propose DP-SPRT, a wrapper that can be calibrated to achieve desired error probabilities and privacy constraints, addressing a gap in previous work. DP-SPRT relies on a private mechanism that processes a sequence of queries and stops after privately determining when the query results fall outside a predefined interval. This OutsideInterval mechanism improves upon naive composition of existing techniques like AboveThreshold, achieving a factor-of-2 privacy improvement and thus potentially benefiting other continual monitoring procedures. We prove generic upper bounds on the error and sample complexity of DP-SPRT that can accommodate various noise distributions based on the practitioner''s privacy needs. We exemplify them in two settings: Laplace noise (pure Differential Privacy) and Gaussian noise (Rényi differential privacy). In the former setting, by providing a lower bound on the sample complexity of any $\varepsilon$-DP test with prescribed type I and type II errors, we show that DP-SPRT is near optimal when both errors are small and the two hypotheses are close. Moreover, we conduct an experimental study revealing its good practical performance.'
---
