# COVID-19 Detection from SARS-CoV-2 CT Scans using Deep Learning & Transfer Learning

##  Project Overview
This project evaluates and compares multiple Convolutional Neural Network (CNN) architectures to diagnose COVID-19 infection using chest CT scan images. 
The repository contrasts custom baseline models with transfer learning approaches using **pre-trained weights**to determine the most effective classification pipeline.

- **Dataset:** 2,482 total CT scans (1,252 COVID-19 positive, 1,230 non-COVID) collected from real hospital data in São Paulo, Brazil.(Kaggle)
- **Split Ratio:** 80% Training / 20% Testing.
- **Top Performing Model:** Fine-Tuned Transfer Learning VGG19 (**90.54% Test Accuracy**).

---

## 🛠️ Models Implemented & Tested
1. **Custom Sequential CNN (CNN1):** 5-layer baseline network.
2. **Batch-Normalized CNN (CNN2):** 5-layer network with internal covariate shift stabilization.
3. **VGG16 (From Scratch):** Deep architecture with $3\times3$ filters built ground-up.
4. **VGG19 (From Scratch):** 19-layer architecture built ground-up.
5. **ResNet50 (From Scratch):** 50-layer deep network utilizing bottleneck residual blocks.
6. **Transfer Learning VGG16:** Pre-trained ImageNet weights with fine-tuning.
7. **Transfer Learning VGG19:** Pre-trained ImageNet weights with fine-tuning.
8. **Transfer Learning ResNet50:** Pre-trained ImageNet weights with residual connections.

---


## 🚀 Key Takeaways
- **Transfer Learning Superiority:** Pre-trained models (VGG19/VGG16) significantly outperformed scratch implementations, leveraging rich spatial visual representations learned from ImageNet.
- **Depth Constraints from Scratch:** Deep architectures like VGG16/19 trained from scratch struggled to converge within 20 epochs, confirming the need for pre-training or longer training cycles on small datasets.
- **Impact of Batch Normalization:** Adding Batch Normalization (CNN2) improved training stability and boosted accuracy over the simple baseline (CNN1).

## 🔗 Notebook Link
[You can open and execute the project in Google Colab:](https://colab.research.google.com/drive/1TMBj1Ff3AUGWUb-t7PNSqAB2nRVHTXlJ?usp=sharing)
