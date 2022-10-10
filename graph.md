# Tools to model graph-structured data
1. graph kernels
    > Graph Kernels
2. random-walk
    > DeepWalk: online learning of social representations
    >
    > node2vec: Scalable Feature Learning for Networks

# 图上的经典问题
只是一小部分的例子！！
1. Node Classification: Classifying individual nodes.
2. Graph Classification: Classifying entire graphs.
3. Node Clustering: Grouping together similar nodes based on connectivity.
4. Link Prediction: Predicting missing links.
5. **Influence Maximization**: Identifying influential nodes.

# 关键问题
+ node representation learning: learning to map individual nodes to fixed-size real-valued vectors (called ‘representations’ or ‘embeddings’)
    1. Different GNN variants are distinguished by the way these representations are computed.

# GCN 
1. Polynomials of the Laplacian: 用卷积计算时，要卷积的格子是不确定的，所以构造拉普拉斯多项式，相当于CNN中的filter
    > https://csustan.csustan.edu/~tom/Clustering/GraphLaplacian-tutorial.pdf
    >
    > Convolutional neural networks on graphs with fast localized spectral filtering
2. ChebNet: 一是用Chebyshev多项式更稳定的插值，而是对L归一化
3. Message-passing机制（视角）GNN:
    1. GCN
        > Semi-Supervised Classification with Graph Convolutional Networks
    2. GAT
        > Graph Attention Networks
    3. GraphSAGE
        > Inductive Representation Learning on Large Graphs
    4. GIN
        > How Powerful are Graph Neural Networks?
    5. 考虑边更新的
        > Neural Message Passing for Quantum Chemistry
        >
        > Relational inductive biases, deep learning, and graph networks
4. Spectral
> Spectral Networks and Locally Connected Networks on Graphs