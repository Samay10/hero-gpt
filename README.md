# Transformer-based Language Model Implementation

This repository contains PyTorch implementations of language models based on the Transformer architecture, showcasing the evolution from simple n-gram models to more sophisticated architectures.

## Project Overview

This project provides two implementations:

1. **Bigram Language Model** (`bigram.py`): A simple character-level language model that predicts the next character based solely on the current character.

2. **GPT-style Language Model** (`gptv2.py`): A more advanced implementation incorporating key components of the Transformer architecture including multi-head self-attention, positional embeddings, and layer normalization.

## Key Features

- Character-level tokenization and prediction
- Implementation of self-attention mechanisms
- Multi-head attention implementation
- Feed-forward networks with residual connections
- Layer normalization
- Position embeddings
- Autoregressive text generation

## Requirements

- PyTorch
- CUDA-capable GPU (optional but recommended for faster training)

## Usage

1. Place your training text in a file named `input.txt` in the same directory.

2. Run either model:
   ```
   python bigram.py
   ```
   or
   ```
   python gptv2.py
   ```

3. The models will train on your text and generate sample output upon completion.

## Model Architecture

### Bigram Language Model
- Simple embedding-based approach
- Directly maps input tokens to logits for the next token
- No context beyond the immediate preceding token

### GPT-style Language Model
- Transformer-based architecture with:
  - Token embeddings
  - Position embeddings
  - Multi-head self-attention (6 heads)
  - Feed-forward networks
  - Residual connections
  - Layer normalization
  - 6 transformer blocks
  - ~10M parameters

## Hyperparameters

Both models allow customization of various hyperparameters including:
- Batch size
- Context length (block size)
- Learning rate
- Number of training iterations
- Embedding dimensions (GPT model)
- Number of attention heads (GPT model)
- Number of layers (GPT model)
- Dropout rate

## Output

After training, each model will generate a sample text of 500 tokens based on what it has learned from the training data.

## Educational Value

This implementation serves as an educational resource for understanding:
- How language models process and generate text
- The architecture of Transformer-based models
- The importance of attention mechanisms in modern NLP
- How to implement these concepts in PyTorch

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

This implementation draws inspiration from the architecture described in "Attention Is All You Need" (Vaswani et al.) and subsequent GPT model designs.

---

Made with ❤️ in Python
