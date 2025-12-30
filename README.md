
```markdown
# Nano-Hybrid: Lightweight Lung Cancer Detection 🫁

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0-ee4c2c)
![License](https://img.shields.io/badge/License-MIT-green)

A lightweight deep learning model (**Nano-Hybrid**) designed for efficient lung cancer diagnosis on edge devices.
This architecture integrates **InceptionNeXt** blocks with **Global Self-Attention**, achieving state-of-the-art performance with **~89% fewer parameters** (2.03M) than comparable baseline models.

## 📊 Key Results

| Dataset | Accuracy | Sensitivity | Specificity | AUC (Normal) |
| :--- | :--- | :--- | :--- | :--- |
| **IQ-OTH/NCCD** | **95.41%** | 96.2% | 99.1% | **1.00** |
| **Chest CT** | **86.11%** | 85.5% | 100.0% | **1.00** |

## 🧠 Model Architecture
The model is designed to be trained from scratch without heavy pre-trained weights.
- **Stage 1 & 2:** InceptionNeXt blocks for local feature extraction.
- **Stage 3:** Self-Attention mechanism for global context modeling.

## 🖼️ Visuals
### Efficiency Trade-off
![Efficiency Plot](images/efficiency_comparison.png)
*Our model (Right) matches the baseline accuracy with only 2M parameters.*

### Confusion Matrices
![Confusion Matrices](images/confusion_matrices.png)
*(Left) IQ-OTH/NCCD dataset. (Right) Chest CT dataset.*

### Explainability (Grad-CAM)
![Grad-CAM](images/gradcam_result.jpg)
*The model focuses on pulmonary nodules (red/yellow) rather than background artifacts.*

## 🚀 Usage
1. **Clone the repo**
   ```bash
   git clone [https://github.com/Hazik-Jaffri/Nano-Hybrid-Lung-Cancer-Detection.git](https://github.com/Hazik-Jaffri/Nano-Hybrid-Lung-Cancer-Detection.git)

```

2. **Install dependencies**
```bash
pip install torch torchvision matplotlib seaborn scikit-learn

```


3. **Run Training**
Open `Nano_Hybrid_Training.ipynb` in Jupyter or Colab.

## 📂 Files Included

* `best_iq_model_300epochs.pth`: Best weights for IQ dataset.
* `best_chest_model_300epochs.pth`: Best weights for Chest CT dataset.
* `Nano_Hybrid_Training.ipynb`: Complete training and visualization code.

```

***

### **Step 3: Upload Your Files**
Now you need to put your actual work into the repo.

**Method A: The "Easy" Way (Web Upload)**
1.  In your repository, click **Add file** > **Upload files**.
2.  **Drag and drop** the following files from your computer:
    * `Nano_Hybrid_Training.ipynb` (Download this from Colab: File > Download .ipynb).
    * `best_iq_model_300epochs.pth`
    * `best_chest_model_300epochs.pth`
3.  **Important:** Create a folder named `images` for your screenshots so they show up in the README properly.
    * *GitHub Web Trick:* You cannot create empty folders. Instead, rename your images on your computer to `images/efficiency_comparison.png`, `images/gradcam_result.jpg`, etc., and then drag them in. Or, just upload them to the root folder and update the README links to remove `images/`.

**Method B: The "Pro" Way (Command Line)**
If you have Git installed on your computer:
1.  Open your terminal/command prompt.
2.  Clone the repo:
    `git clone https://github.com/Hazik-Jaffri/Nano-Hybrid-Lung-Cancer-Detection.git`
3.  Enter the folder:
    `cd Nano-Hybrid-Lung-Cancer-Detection`
4.  **Paste** your `.ipynb` file, `.pth` files, and your images into this folder.
5.  Create an images folder and move your pictures there:
    `mkdir images`
    (Move your png/jpg files into `images/`)
6.  Push to GitHub:
    ```bash
    git add .
    git commit -m "Initial release of Nano-Hybrid model and weights"
    git push
    ```

### **Checklist: Did you include everything?**
* [ ] **Code:** The Jupyter Notebook (`.ipynb`).
* [ ] **Models:** The two `.pth` files.
* [ ] **Visuals:** The Grad-CAM image, Efficiency Plot, and Confusion Matrices.
* [ ] **README:** The text I provided above.

Once this is done, you can paste the link to your new repository into your Research Paper under the **"Code Availability"** section!

```
