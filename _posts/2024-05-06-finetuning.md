---
title:  "Fine tuning"
date:   2024-05-06 9:00:00
layout: page
#
# toc: true
# categories:
---

A Recipe for Training Neural Networks 
- a collection of attempted advice for training neural nets with a focus on how to structure that process over time
https://karpathy.github.io/2019/04/25/recipe/

## TWeets
New open weights LLM from 
@MistralAI


params.json:
- hidden_dim / dim = 14336/4096 => 3.5X MLP expand
- n_heads / n_kv_heads = 32/8 => 4X multiquery
- "moe" => mixture of experts 8X top 2 👀

Likely related code: 
https://github.com/mistralai/megablocks-public

Oddly absent: an over-rehearsed professional release video talking about a revolution in AI.
source: https://x.com/karpathy/status/1733181701361451130 (12/2023)