# Graph-Fairness



## Ⅰ. Data Augmentation

### 1. heuristic

### 2. automated

The author removed the bias at the feature level and the topology level. They introduce the learnable parameters to de-bias the original feature matrix and adjacency matrix, the optimization by minimizing the Wasserstein distance between two groups.

- [[WWW-2022] EDITS: Modeling and Mitigating Data Bias for Graph Neural Networks](https://arxiv.org/abs/2108.05233) [[code](https://github.com/yushundong/EDITS)] 

They proposed a method to learn fair representations based on automated graph data augmentations. This augmentation can circumvent sensitive information (fairness) while preserving other useful information (informativeness).

- [[ICLR-2023] Learning Fair Graph Representations via Automated Data Augmentations](https://openreview.net/forum?id=1_OGWcP1s9w) [[code](https://github.com/divelab/DIG)] 

## Ⅱ. Degree-related 

This paper found that Graph Contrastive Learning (GCL) has a better performance for degree-related fairness, compared to Graph Convolutional Networks without GCL. Then they theoretically show that this fairness stems from intra-community concentration and inter-community scatter properties of GCL. Based on the theorem analysis, the design of heuristic augmentation interpolates the tail nodes and purifies the head nodes.

- [[NIPS-2022] Uncovering the Structural Fairness in Graph Contrastive Learning](https://arxiv.org/pdf/2210.03011.pdf) [[code]](https://github.com/BUPT-GAMMA/Uncovering-the-Structural-Fairness-in-Graph-Contrastive-Learning)



## Application