# Self-Pruning Neural Network

This project implements a self-pruning neural network in PyTorch using learnable per-weight sigmoid gates. During training, each weight is scaled by a differentiable gate, and an L1 sparsity penalty encourages the network to suppress unnecessary connections. After training, a hard-pruning step removes weights whose gate values fall below a threshold.

## Features
- Per-weight learnable gates
- Differentiable sparsity with L1 regularization
- Hard pruning after training
- Evaluation across multiple sparsity strengths

## Method
Each weight is associated with a learnable gate:

effective_weight = weight * sigmoid(gate_score)

Training objective:

Loss = CrossEntropy + lambda * L1(gates)

After training, weights with gate values below a threshold are pruned.

## Files
- `Tredence_SelfPruning_NN_Final.ipynb` — main notebook
- `Result.pdf` — output/results
- `requirements.txt` — dependencies

## How to Run
```bash
pip install -r requirements.txt
