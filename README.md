# 🧠 Multimodal Vision-Language Project: Image Captioning & Generation

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.10-orange)
![EfficientNet](https://img.shields.io/badge/EfficientNet-B0-green)
![Transformer](https://img.shields.io/badge/Transformer-Encoder%2FDecoder-yellow)
![StableDiffusion](https://img.shields.io/badge/StableDiffusion-v1.5-lightgrey)

This project explores **two complementary multimodal tasks** using deep learning: generating captions from images (Phase 1) and generating images from text (Phase 2). Both phases use the **Flickr8k dataset** and demonstrate how visual and textual data can be bridged using neural networks.

---

## 📌 Phase 1: Image Captioning with CNN-Transformer

An end-to-end deep learning system that generates descriptive captions for images using a hybrid CNN-Transformer model, implemented from scratch with TensorFlow/Keras.

### 🔑 Key Features
- **Dual-Model Architecture**: Combines EfficientNetB0 (CNN encoder) with Transformer decoder layers
- **Multi-Caption Training**: Uses 5 captions per image to improve generalization
- **Masked Loss**: Custom loss logic for handling padded tokens in caption sequences
- **Learning Rate Scheduler**: Warm-up strategy to stabilize early training

### 📊 Performance Metrics
| Epoch | Training Acc | Training Loss | Validation Acc | Validation Loss |
|-------|--------------|----------------|----------------|-----------------|
| 96    | 0.5133       | 10.1587        | 0.4064         | 15.5985         |

> Final model trained over 96 epochs using a batch size of 64.

---

## 🎨 Phase 2: Text-to-Image Generation with Stable Diffusion

This phase reverses the task—generating images based on textual descriptions using the **Stable Diffusion v1.5** model via Hugging Face's `diffusers` library.

### 🔧 Highlights
- **Pre-trained Model Usage**: No fine-tuning required; inference via `StableDiffusionPipeline`
- **Text Prompts**: Real captions from Flickr8k used as inputs
- **Zero-shot Inference**: Generates high-quality images from natural language
- **Prompt Variety**: Covers people, animals, landscapes, and abstract scenes

### 📂 Sample Prompts
- "a little cat playing with a dog in the park"
- "a group of people hiking on a mountain trail"
- "a couple walking hand in hand on the beach"

### 🖼️ Output Example
Generated images are saved as  `download (2).png`, etc., and displayed in grid format using `matplotlib`.

---

## 🛠️ Installation
```bash
git clone https://github.com/kalana-mihiranga/Image-Captioning.git
cd Image-Captioning
pip install -r requirements.txt
