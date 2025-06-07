# Kaggle-Bird-CLEF-2025

```markdown
# 🐦 BirdCLEF 2025 - Bronze Medal Solution

This repository contains the code and experiments used for participating in the [BirdCLEF 2025](https://www.kaggle.com/competitions/birdclef-2025) competition hosted on Kaggle. The competition challenged participants to build robust models for identifying bird species from audio recordings collected in diverse and often noisy field environments.

---

## 🏆 Competition Overview

- **Goal**: Detect bird calls from long-duration audio recordings using machine learning.
- **Hosted By**: [Kaggle](https://www.kaggle.com/)
- **Challenge Type**: Multi-label classification using spectrograms and raw audio.
- **Evaluation Metric**: ROC-AUC Score.

**Statistics:**
- 👥 2,569 Participants  
- 👨‍👩‍👧‍👦 2,025 Teams  
- 📦 70,674 Submissions  
- 🥉 Ranked **186th** out of **9,630 entries**  
- 🔥 Achieved **0.893 ROC-AUC Score**  

---

## 🧠 Models & Approach

This solution primarily used an **ensemble of advanced CNN-based architectures**, along with audio-specific augmentations and pooling strategies:

### ✅ Core Models Used:
- **EfficientNet-B0 & B3**
- **ResNet34** (customized for spectrograms)
- **SE-ResNeXt50** (fine-tuned with PANN pre-trained weights)
- **Conformer** (for temporal modeling)

### 🛠️ Technical Highlights:
- Used **Mel spectrograms** and **Log-mel spectrograms** with and without noise.
- Integrated **multi-head self-attention pooling** and **GeM pooling** layers.
- Employed **Focal Loss** to handle class imbalance.
- Optimized using **AdamW** with learning rate warm-up and cosine annealing.
- **5-fold Stratified Cross-Validation** with test-time augmentation.
- **SpecAugment** and **mixup** techniques applied to augment data diversity.

---

## 🥉 Final Result

> 🎉 Our final submission scored **0.893 ROC-AUC**, securing a **Bronze Medal** with a **Global Rank of 186** among 9,630 entries.  
> This solution stood among the top **10%** of all teams in a highly competitive environment.

---

## 🔗 Links

- 🧪 [Kaggle Competition Page](https://www.kaggle.com/competitions/birdclef-2025)
- 📓 [View the Kaggle Notebook (if public)](https://www.kaggle.com/your-notebook-link)

---

## 📁 Repository Structure

```

.
├── configs/                # Model and training configs
├── notebooks/              # EDA and training notebooks
├── src/                    # Core model and data loading scripts
├── outputs/                # Logs and model weights
└── README.md

```

---

## 🙌 Acknowledgements

Huge thanks to the [xeno-canto](https://www.xeno-canto.org/) community and organizers for providing high-quality biodiversity data and pushing forward eco-acoustic ML research.
```
