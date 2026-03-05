---
layout: post
title: Paper published at JBCS about LLM Brazilian Fauna
date: 2025-10-08 09:00:00 -0400
inline: true
related_posts: false
---

🦜 **Exploring Brazil's LLM Fauna: Evaluating Generative Performance in Portuguese**

We are excited to share our new paper, **“Exploring Brazil's LLM Fauna: Investigating the Generative Performance of Large Language Models in Portuguese.”**

As Large Language Models (LLMs) become increasingly embedded in real-world applications, their evaluation still relies heavily on narrow, mostly English-centered benchmarks. These traditional evaluations often neglect essential generative aspects such as discourse coherence, adequacy, and linguistic transformations — all crucial for practical use.

In this work, we provide a comprehensive evaluation of Brazilian Portuguese LLMs across three core Natural Language Generation tasks:

- 📝 Text Summarization  
- ✂️ Sentence Simplification  
- ❓ Generative Question Answering  

We evaluate six Brazilian models and compare them with **GPT-4o**, combining automatic metrics, an LLM-as-a-judge framework, and human evaluation.


🔎 **Key findings:**
- GPT-4o achieves the strongest overall generative performance in Portuguese.
- The Sabiá-3 family follows closely behind.
- The open-weight model Tucano stands out for its computational efficiency, making it a strong candidate for deployment in resource-constrained environments.

All experimental code is publicly available:
👉 https://github.com/MeLLL-UFF/brfauna-gen-eval

This work contributes to a broader understanding of how LLMs perform beyond English and supports more realistic, generation-focused evaluation pipelines for Portuguese NLP.
