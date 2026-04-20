# self-pruning-neural-network
This project implements a self-pruning neural network using learnable per-weight gates.  During training, each weight is multiplied by a differentiable sigmoid gate, and an L1 penalty encourages sparsity.  After training, a hard-pruning step removes connections whose gate values fall below a threshold.
Title
# Self-Pruning Neural Network
Description
This project implements a self-pruning neural network using learnable per-weight gates. 
During training, each weight is multiplied by a differentiable sigmoid gate, and an L1 penalty encourages sparsity.

After training, a hard-pruning step removes connections whose gate values fall below a threshold.
Features
- Per-weight learnable gates
- Differentiable sparsity via L1 regularization
- Hard pruning after training
- Experiments with multiple sparsity strengths
Method
Each weight is associated with a learnable gate:
effective_weight = weight * sigmoid(gate_score)

The loss function includes:
Loss = CrossEntropy + λ * L1(gates)

After training:
weights with gate < threshold are removed
Results
- Accuracy remains stable after pruning
- Sparsity increases with higher λ
- Demonstrates trade-off between sparsity and performance

 (Make sure your results actually show this — fix earlier issue if needed)

How to Run
pip install -r requirements.txt
run the notebook in Google Colab
 5. requirements.txt

Create a file with:

torch
torchvision
matplotlib
pandas
numpy
 6. How to Upload to GitHub
Step-by-step:
Go to GitHub
Click New Repository
Name: self-pruning-neural-network
Click Create
