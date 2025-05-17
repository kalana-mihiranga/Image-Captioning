# Image Captioning with CNN-Transformer Architecture

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.10-orange)
![EfficientNet](https://img.shields.io/badge/EfficientNet-B0-green)
![Transformer](https://img.shields.io/badge/Transformer-Encoder%2FDecoder-yellow)

An end-to-end deep learning system that generates descriptive captions for images using a hybrid CNN-Transformer model, implemented from scratch with TensorFlow/Keras.

## 📌 Key Features
- **Dual-Model Architecture**: Combines EfficientNetB0 (CNN encoder) with Transformer layers for sequence generation
- **Multi-Caption Training**: Learns from 5 captions per image (Flickr8k dataset)
- **Attention Mechanisms**: Implements both self-attention and encoder-decoder attention
- **Custom Training Loop**: Supports masked loss calculation and warm-up learning rate scheduling

## 📊 Performance Metrics
| Epoch | Training Acc | Training Loss | Validation Acc | Validation Loss |
|-------|-------------|---------------|----------------|-----------------|
| 96    | 0.5133      | 10.1587       | 0.4064         | 15.5985         |

*Final metrics after 96 epochs (batch size: 64)*

## 🛠️ Installation
```bash
git clone https://github.com/kalana-mihiranga/Image-Captioning.git
cd Image-Captioning
pip install -r requirements.txt
