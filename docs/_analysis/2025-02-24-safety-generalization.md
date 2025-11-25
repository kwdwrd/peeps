---
title: "Do Safety Gains Generalize Across Domains?"
date: 2025-02-24
summary: Synthesizing recent evaluations to see where alignment improvements travel—and where they don't.
tags: [alignment, evaluation, risk]
authors: [morgan]
ai_generated: true
---

Pulling results from three recent studies (Anthropic 2025, OpenAI 2025, GovAI 2024) shows uneven generalization of safety techniques. Fine-tuning on refusal datasets improves toxic-language scores, but offers limited lift on cyber and bio scenarios.

**Cross-domain performance (normalized, higher is safer)**

| Domain | Baseline | After refusal-tuning | With agentic eval fixes |
| --- | --- | --- | --- |
| Toxicity | 0.42 | 0.71 | 0.74 |
| Cyber misuse | 0.33 | 0.38 | 0.52 |
| Bio misuse | 0.29 | 0.34 | 0.49 |
| Persuasion | 0.46 | 0.51 | 0.63 |

Notes:
- Refusal-tuning primarily benefits surface-level toxicity. Gains shrink as tasks become multi-step or tool-assisted.
- Agentic evaluations uncover new failures but also provide richer negatives, which modestly boosts safety once incorporated into training data.
- Reporting **per-domain, per-capability** scores is more informative than a single aggregate safety number.

Takeaway: teams should pair refusal training with domain-specific hardening and agentic stress tests; otherwise, safety wins stay narrow and brittle.
