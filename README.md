# English-Japanese-transformer
English-to-Japanese Neural Machine Translation using a Transformer built from scratch in PyTorch.



# From Scratch Transformer Translator

A Transformer-based English → Japanese Neural Machine Translation model built completely from scratch using PyTorch.

This project started as an attempt to understand how modern translation models actually work under the hood instead of relying on pre-trained libraries. Along the way, it turned into a deep dive into attention mechanisms, tokenization, sequence modeling, CUDA debugging, and training large neural networks.

The model follows the original Transformer architecture and is trained using SentencePiece tokenization and mixed-precision training.

---

## Why I Built This

Most tutorials use pre-built models that hide the interesting parts.

I wanted to understand:

- How self-attention works
- How encoder-decoder Transformers perform translation
- How tokenization affects model performance
- How training behaves at scale
- How to debug real-world deep learning systems

So instead of using a pre-trained model, I implemented the architecture myself and trained it from scratch.

---

## Architecture

| Component | Value |
|------------|---------|
| Vocabulary Size | 16,000 |
| Embedding Dimension | 512 |
| Attention Heads | 8 |
| Encoder Layers | 6 |
| Decoder Layers | 6 |
| Feed Forward Dimension | 2048 |
| Maximum Sequence Length | 256 |
| Tokenizer | SentencePiece |
| Framework | PyTorch |
| Precision | Mixed Precision (AMP) |

---

## Features

- Transformer Encoder
- Transformer Decoder
- Multi-Head Self Attention
- Encoder-Decoder Cross Attention
- Positional Embeddings
- SentencePiece Tokenization
- Mixed Precision Training
- Gradient Clipping
- Custom Training Pipeline

---

## Training

The model was trained on an English-Japanese translation dataset using PyTorch.

During development, several issues had to be solved including:

- CUDA device-side assertion errors
- Position embedding index overflows
- Sequence length handling
- Vocabulary consistency checks
- Training stability issues

These debugging sessions ended up teaching me almost as much as the model itself.

---

## Sample Outputs

Example translations produced by the model:

Input:
```
cat
```

Output:
```
猫
```

---

Input:
```
Hello
```

Output:
```
もしもし
```

---

Input:
```
How are you?
```

Output:
```
気分は?
```

The model is still being improved and additional training/evaluation is planned.

---

## Project Structure

```text
.
├── model.py
├── train.py
├── inference.py
├── translator_sp.model
├── translator_sp.vocab
├── checkpoints/
└── README.md
```

---

## What I Learned

Building this project gave me hands-on experience with:

- Attention mechanisms
- Transformer architectures
- Neural Machine Translation
- NLP preprocessing
- GPU training workflows
- Mixed precision training
- Model debugging
- Tensor shape reasoning

---

## Future Improvements

- BLEU score evaluation
- Beam Search decoding
- Larger datasets
- Longer training runs
- Better inference pipeline
- Model checkpoint management

---

## Tech Stack

- Python
- PyTorch
- SentencePiece
- CUDA
- NVIDIA RTX 5070

---

## Author

Teja

Built as part of my journey into understanding modern NLP systems from first principles.
