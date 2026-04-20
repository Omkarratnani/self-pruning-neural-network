# self-pruning-neural-network
This project implements a self-pruning neural network using learnable per-weight gates.  During training, each weight is multiplied by a differentiable sigmoid gate, and an L1 penalty encourages sparsity.  After training, a hard-pruning step removes connections whose gate values fall below a threshold.
