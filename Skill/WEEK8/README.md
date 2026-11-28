# Week 8 – Multi-Head Attention Using PyTorch

## 📌 Overview
This project demonstrates the implementation of the Attention Mechanism and Multi-Head Attention using PyTorch.

It explains how attention mechanisms work in Transformer-based deep learning models and how causal masking is applied in decoder-style architectures.

## 🎯 Objectives
- Understand Scaled Dot-Product Attention.
- Implement Multi-Head Attention using PyTorch.
- Understand Query (Q), Key (K), and Value (V) matrices.
- Implement self-attention.
- Apply causal masking.
- Observe attention weights and output tensor shapes.

## 🛠️ Technologies Used
- Python
- PyTorch
- Google Colab
- Math Library

## 📚 Concepts Covered

### 1. Scaled Dot-Product Attention
Calculates attention scores using Query, Key, and Value matrices.

### 2. Multi-Head Attention
Splits input embeddings into multiple attention heads and processes them in parallel.

### 3. Self-Attention
Allows each token to focus on other tokens in the input sequence.

### 4. Causal Masking
Prevents a token from attending to future tokens. It is commonly used in decoder-based Transformer models.

## ⚙️ Implementation
The notebook contains three main sections:

1. Imports and Scaled Dot-Product Attention.
2. Multi-Head Attention Module using `nn.Module`.
3. Testing Self-Attention and Causal Masking.

## ▶️ How to Run
1. Open the notebook in Google Colab.
2. Make sure PyTorch is available.
3. Run all cells sequentially.
4. Observe the attention weights and output tensors.

## 📊 Sample Output
- Input Shape: `[1, 3, 4]`
- Output Shape: `[1, 3, 4]`
- Number of Attention Heads: `4`
- Attention Weights Shape: `[1, 4, 3, 3]`

The notebook demonstrates both unmasked self-attention and causal masked attention.

## 📁 Project Structure
```text
Week-8/
│
├── week8_colab.ipynb
└── README.md
```

## ✅ Conclusion
This experiment demonstrates how Scaled Dot-Product Attention and Multi-Head Attention work using PyTorch. It also shows how causal masking controls information flow in Transformer decoder architectures.

---
**Topic:** Deep Learning – Attention Mechanism  
**Week:** 8
