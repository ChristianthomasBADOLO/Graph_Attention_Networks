
---

# Graph Attention Networks (GAT) for Chest X-ray Image Classification

## Overview

The Graph Attention Network (GAT) is a type of Graph Neural Network (GNN) that utilizes attention mechanisms to process graph-structured data effectively. In this project, we focus on applying GAT to the classification of chest X-ray images.

## GAT Overview

GAT takes a graph as input, including edge and node feature tensors, and produces updated node states by aggregating information from neighboring nodes using attention mechanisms. Unlike traditional convolutional networks, GATs dynamically weight the importance of neighboring nodes during message passing, enhancing their ability to handle variable connectivity and lack of spatial order in graphs.

### Key Components of GATs

1. **Message Passing:** Nodes aggregate information from neighbors.
2. **Attention Mechanism:** Nodes use attention coefficients to weigh the importance of neighbor information.
3. **Feature Transformation:** Neighbor features are transformed for compatibility and dimensionality alignment.
4. **Aggregation:** Transformed and weighted neighbor features are aggregated to create refined node representations.
5. **Node Feature Update:** Aggregated representations update the features of each node in a context-aware manner.

## Data Preprocessing

### Node Definition

In our model, nodes represent images themselves.

### Edge Establishment Process

1. **Extract Features:** Use the VGG16 model to extract features from images.
2. **Dataset Creation:** Construct a dataset with image paths, features, and labels.
3. **Similarity Determination:** Calculate cosine similarity between image features.
4. **Edge Creation:** Generate a dataset capturing similar images based on feature similarities.

By following this preprocessing pipeline, we transform raw image data into a format suitable for GAT-based analysis and classification of chest X-ray images.

---

