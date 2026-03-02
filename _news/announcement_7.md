---
layout: post
date: 2024-12-24 08:30:00 -0400
inline: true
related_posts: false
---

🚀 **New Publication: BERTweet.BR — A Pre-trained Language Model for Portuguese Tweets**

We are excited to share our paper **“BERTweet.BR: a pre-trained language model for tweets in Portuguese”**, now published in *Neural Computing and Applications*.

📄 Paper: https://link.springer.com/article/10.1007/s00521-024-10711-3  
🤗 Model on Hugging Face: https://huggingface.co/melll-uff/bertweetbr  

While most advances in neural language models focus on English, Portuguese — despite being the sixth most spoken language in the world — still lacks domain-specific large-scale resources. This gap is even more evident for social media, where Brazilian users are among the most active globally.

To address this, we introduce **BERTweet.BR**, the first large-scale pre-trained language model specifically designed for Brazilian Portuguese tweets. The model:

- 🧠 Follows the BERTweet architecture (BERT-based)  
- 📚 Was trained from scratch using the RoBERTa pre-training procedure  
- 🐦 Uses a corpus of 100 million Portuguese tweets  
- 📊 Outperforms multilingual Transformers and BERTimbau on sentiment analysis  

Tweets present unique challenges — informal language, cultural references, code-switching, abbreviations, and character limits. BERTweet.BR is designed to better capture these characteristics and support downstream tasks in social media analysis for Portuguese.

The model is publicly available in the 🤗 Transformers library, and the code, documentation, and experimental results are open on GitHub.

We hope BERTweet.BR fosters new research in Portuguese NLP and strengthens analytical tools for social media in Brazil.
