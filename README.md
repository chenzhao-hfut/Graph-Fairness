# Sensitive-Aware Fairness

## Ⅰ. Contrastive Learning

### 1. Heuristic

The author established the connection between graph counterfactual fairness and stability. Based on this, they proposed a fairness and stability framework comprising a feature augmentation (random mask), a graph perturbation (random node dropout), and a layer-wise weight normalization.

- [[UAI-2021] Towards a Unified Framework for Fair and Stable Graph Representation Learning](https://arxiv.org/abs/2102.13186) [[code](https://github.com/chirag126/nifty)]

This paper studies the correlations between sensitive attributes and learned node representations and proposes several fairness-aware graph augmentations to minimize the upper bound of the correlation to achieve fairness.

- [[arXiv-2022] Fair Node Representation Learning via Adaptive Data Augmentation](https://arxiv.org/abs/2201.08549) [[code](https://openreview.net/forum?id=4pijrj4H_B)]



### 2. Automated

They proposed a method to learn fair representations based on automated graph data augmentations. This augmentation can circumvent sensitive information (fairness) while preserving other useful information (informativeness).

- [[ICLR-2023] Learning Fair Graph Representations via Automated Data Augmentations](https://openreview.net/forum?id=1_OGWcP1s9w) [[code](https://github.com/divelab/DIG)] 

This paper studies the feature propagation could vary the correlation of previously innocuous non-sensitive features to the sensitive ones. Therefore, they proposed FairVGNN to generate fair views of features by utilizing adversarial learning to automatically identify variation after feature propagation. Otherwise,  they also proposed to adaptively clamp weights of the encoder to decline the contributions of sensitive features and highly-correlated features.

- [[KDD-2022] Improving Fairness in Graph Neural Networks via Mitigating Sensitive Attribute Leakage](https://arxiv.org/abs/2206.03426) [[code](https://github.com/YuWVandy/FairVGNN)]


## Ⅱ. Distribution-Related Methods

The author removed the bias at the feature level and the topology level. They introduce the learnable parameters to de-bias the original feature matrix and adjacency matrix, the optimization by minimizing the Wasserstein distance between two groups.

- [[WWW-2022] EDITS: Modeling and Mitigating Data Bias for Graph Neural Networks](https://arxiv.org/abs/2108.05233) [[code](https://github.com/yushundong/EDITS)] 


# Degree-Related Fairness

## Ⅰ. Contrastive Learning

### 1. Heuristic

This paper found that Graph Contrastive Learning (GCL) has a better performance for degree-related fairness, compared to Graph Convolutional Networks without GCL. Then they theoretically show that this fairness stems from intra-community concentration and inter-community scatter properties of GCL. Based on the theorem analysis, the design of heuristic augmentation interpolates the tail nodes and purifies the head nodes.

- [[NIPS-2022] Uncovering the Structural Fairness in Graph Contrastive Learning](https://arxiv.org/pdf/2210.03011.pdf) [[code](https://github.com/BUPT-GAMMA/Uncovering-the-Structural-Fairness-in-Graph-Contrastive-Learning)]



