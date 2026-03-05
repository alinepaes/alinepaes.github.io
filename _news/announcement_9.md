---
layout: post
title: New Paper Accepted at Machine Learning Journal!
date: 2026-02-04 10:00:00 -0400
inline: true
related_posts: false
---


We are happy to share that our paper <a href="https://link.springer.com/article/10.1007/s10994-025-06940-9"> **“Select First, Transfer Later: Choosing a Proper Dataset for SRL and GNN Based Transfer Learning”** </a> has been published in *Machine Learning Journal*.

Traditional machine learning models often ignore the relational structure present in many real-world domains. Approaches such as **Statistical Relational Learning (SRL)** and **Graph Neural Networks (GNNs)** address this by explicitly modeling dependencies between entities. However, like traditional models, they typically assume that training and testing data come from the same distribution — an assumption that often fails in practice.

Transfer Learning helps by reusing knowledge from one domain in another. But an important question remains largely overlooked:

👉 **From where should we transfer?**

In this work, we propose a principled method to estimate the suitability of transfer between relational domains using **Kullback–Leibler (KL) divergence**, computed from a Naive Bayes distribution of the target relational data and each candidate source model (SRL or GNN).

🔎 **Main contribution:**
- A strategy to select the most appropriate source domain before performing transfer.
- Empirical evaluation with state-of-the-art SRL and GNN transfer learning algorithms.
- Experimental evidence that selecting the right source significantly improves performance.

Our results reinforce that, in relational and graph-based learning, choosing the source domain is just as important as deciding what and how to transfer.

