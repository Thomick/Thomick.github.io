---
title: "Sequential Membership Inference Attacks"
collection: publications
category: preprints
permalink: /publications/sequential-membership-inference
date: 2026-02-23
venue: 'arXiv preprint'
paperurl: 'https://arxiv.org/abs/2602.16596'
citation: 'Michel, T., Basu, D., &amp; Kaufmann, E. (2026). &quot;Sequential Membership Inference Attacks.&quot; <i>arXiv preprint arXiv:2602.16596</i>.'
excerpt: 'Modern AI models are not static. They go through multiple updates in their lifecycles. We propose to design Sequential Membership Inference (SeMI) attacks leading to tighter privacy audits by exploiting the sequence of models and injecting a target canary at a controlled insertion time. First, for empirical mean computation, we develop SeMI*, an optimal SeMI attack to identify the presence of a target inserted at a specific insertion step. We derive the power of SeMI* to show that accessing the model sequence yields more powerful MI attacks than scrutinising only the final model. SeMI* exhibits an isolation property—its power depends on the statistics obtained right before and after insertion of the target. Leveraging this insight, we develop practical white-box (accessing model gradients) and black-box (accessing loss) SeMI attacks against models trained with (DP-)SGD. Across datasets and models trained with (DP-)SGD, our experiments show that SeMI attacks achieve higher powers than snapshot-independent baselines, and yield tighter privacy audits thanks to (a) control over the insertion time and (b) observations across the model sequence.'
---
