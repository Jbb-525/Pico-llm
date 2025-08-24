# PicoLLM

A minimal Transformer language model with KV-Cache optimization and RoPE for efficient text generation.

## 🚀 Features

- **KV-Cache Implementation**: Dramatic inference speedup (up to 31.62x for long sequences)
- **Rotary Position Embeddings**: Modern positional encoding
- **Multiple Sampling**: Greedy, nucleus (top-p), and random generation

## 📊 Performance

| Length | Without Cache | With Cache | Speedup |
|--------|--------------|------------|---------|
| 50     | 0.425s       | 0.304s     | 1.40x   |
| 100    | 1.103s       | 0.603s     | 1.83x   |
| 150    | 2.014s       | 0.924s     | 2.18x   |
| 200    | 34.065s      | 1.077s     | **31.62x** |

## 🏃 Quick Start

```bash
# Install dependencies
pip install torch tiktoken datasets matplotlib pandas

# Train model
python script.py --block_size 256

# Run benchmark
jupyter notebook tinystoriesgpt.ipynb
