# Mini-GPT

A character-level language model implementation using transformer architecture, trained on the Tiny Shakespeare dataset.

## Overview

This project implements a GPT-like neural network that learns to generate text character-by-character. It uses a transformer-based architecture with self-attention mechanisms to predict the next character in a sequence. The model is trained on Shakespeare's works and can generate text in a similar style.

## Project Structure

- **Mini-GPT-v1.py** - Initial Python implementation of the character-level language model
- **Mini-GPT-v2.ipynb** - Enhanced Jupyter notebook version with additional features and improvements
- **best_model.pt** - Pre-trained model weights saved in PyTorch format
- **input.txt** - Training dataset containing Shakespeare text

## Key Features

- Character-level tokenization
- Transformer architecture with multi-head self-attention
- Configurable model hyperparameters
- CUDA support for GPU acceleration
- Train/test data splitting (90/10 split)
- Model checkpoint saving and loading

## Model Architecture

The model uses the following configuration:

- Embedding dimension: 384
- Number of attention heads: 6
- Number of transformer layers: 6
- Block size (context length): 256
- Dropout rate: 0.2
- Batch size: 64
- Learning rate: 3e-4
- Total iterations: 5000

## Requirements

- Python 3.x
- PyTorch
- TensorFlow (for utilities)

## Usage

### Training

Run the Python script to train the model:

```bash
python Mini-GPT-v1.py
```

Or use the Jupyter notebook for interactive training:

```bash
jupyter notebook Mini-GPT-v2.ipynb
```

### Using Pre-trained Model

Load the pre-trained weights from `best_model.pt` to generate text without retraining.

## Dataset

The model is trained on the Tiny Shakespeare dataset, a collection of Shakespeare's complete works. The dataset is automatically processed character-by-character to create a vocabulary and encode/decode sequences.

## Notes

- The model uses CUDA if available, otherwise falls back to CPU
- Training progress is evaluated at regular intervals (every 500 iterations)
- The implementation follows character-level language modeling principles commonly used in sequence generation tasks
