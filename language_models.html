---
layout: post
comments: true
title:  "Digging Deep into NLP models"
excerpt: "Exploring popular models like Transformers, BERT etc."
date:   2019-09-03 4:00:00
mathjax: false
---

# Bidirectional Encoder Representations from Transformers

<div class="imgright imgcap">
<img src="/assets/bert.png">
<div class="thecap">BERT model</div>
</div>

Generally speaking, some of the popular sequence to sequence models used RNNs and LSTMs to predict the next word given a context. Bi-directional LSTMs consisted of two LSTM networks running in forward and backworkd directions which are aggregated to produce a final representation.
However, BERT introduced a novel pre-training routine which is primarily trained on two tasks. The figure the two stages of BERT namely pre-training and finetuning.
There are several useful posts on BERT. In this post, I would focus on code-view of the paper.

## Pre-training stage

BERT is pre-trained on unlabelled data on two tasks 1) Masked language modelling and 2) Next Sentence Prediction task. The architecture of the BERT is adopted from Transformers paper (Attention is all you need).
BERT base model configuration: (Transformer blocks (L) = 12, hidden_size (H) = 768, Attention heads (A) = 12)

Code view for Pre-training:

* All the required [input parameters](https://github.com/google-research/bert/blob/master/run_pretraining.py#L121) are defined and are passed to [BERT model](https://github.com/google-research/bert/blob/master/modeling.py#L131)
Assuming a batch size of 32, the dimensions of input tensors are indicated in the line comments
```
input_ids = features["input_ids"] # 32 x 128 (batch_size x max_seq_length)
input_mask = features["input_mask"] # 32 x 128 (batch_size x max_seq_length)
segment_ids = features["segment_ids"] # 32 x 128 (batch_size x max_seq_length). This denotes if a sentence belongs to segment A or B.
masked_lm_positions = features["masked_lm_positions"]
masked_lm_ids = features["masked_lm_ids"]
masked_lm_weights = features["masked_lm_weights"]
next_sentence_labels = features["next_sentence_labels"]
```

* Look up the input ids and aggregate input embeddings along with their segment and position embeddings.

  Input embeddings - 768d (denoted as H) vector. These correspond to the word vectors associated with a fixed vocabulary size of 30000. Randomly initialize a 30000 x 768 matrix.
  Segment embeddings -
