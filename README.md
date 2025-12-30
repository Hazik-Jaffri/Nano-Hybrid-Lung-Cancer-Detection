You are completely right to be concerned. The `**` symbols are **Markdown syntax**—they tell GitHub to make the text **bold** when it is displayed on the website. However, looking at the raw text can indeed look messy and "noisy."

Here is a **Cleaner, Professional Version** for your README. I have removed the aggressive bolding in the text so it looks much smoother, while keeping the necessary code (like `#` for headings and `|` for tables) so it formats correctly on GitHub.

**Copy and paste this exact block into your README.md file:**

```markdown
# Nano-Hybrid: Lightweight Lung Cancer Detection

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0-ee4c2c)
![License](https://img.shields.io/badge/License-MIT-green)

A lightweight deep learning model (Nano-Hybrid) designed for efficient lung cancer diagnosis on edge devices. This architecture integrates InceptionNeXt blocks with Global Self-Attention, achieving state-of-the-art performance with approximately 89% fewer parameters (2.03M) than comparable baseline models.

## Key Results

| Dataset | Accuracy | Sensitivity | Specificity | AUC (Normal) |
| :--- | :--- | :--- | :--- | :--- |
| IQ-OTH/NCCD | 95.41% | 96.2% | 99.1% | 1.00 |
| Chest CT | 86.11% | 85.5% | 100.0% | 1.00 |

## Model Architecture
The model is designed to be trained from scratch without heavy pre-trained weights.
- Stage 1 & 2: InceptionNeXt blocks for local feature extraction.
- Stage 3: Self-Attention mechanism for global context modeling.

## Visuals

### Efficiency Trade-off
![Efficiency Plot](images/efficiency_comparison.png)
Our model (Right) matches the baseline accuracy with only 2M parameters.

### Confusion Matrices
![Confusion Matrices](images/confusion_matrices.png)
(Left) IQ-OTH/NCCD dataset. (Right) Chest CT dataset.

### Explainability (Grad-CAM)
![Grad-CAM](images/gradcam_result.jpg)
The model focuses on pulmonary nodules (red/yellow) rather than background artifacts.

## Usage

1. Clone the repository
   ```bash
   git clone [https://github.com/Hazik-Jaffri/Nano-Hybrid-Lung-Cancer-Detection.git](https://github.com/Hazik-Jaffri/Nano-Hybrid-Lung-Cancer-Detection.git)

```

2. Install dependencies
```bash
pip install torch torchvision matplotlib seaborn scikit-learn

```


3. Run Training
Open Nano_Hybrid_Training.ipynb in Jupyter Notebook or Google Colab.

## Files Included

* best_iq_model_300epochs.pth: Best weights for IQ dataset.
* best_chest_model_300epochs.pth: Best weights for Chest CT dataset.
* Nano_Hybrid_Training.ipynb: Complete training and visualization code.

```

```
