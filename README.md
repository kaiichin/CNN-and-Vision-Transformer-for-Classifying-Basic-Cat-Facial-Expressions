# 🐱 Cat Facial Expression Classification with CNN and Vision Transformer

This project compares the performance of two deep learning models—**ResNet18 (CNN)** and **MobileViT (Vision Transformer)**—for classifying basic cat facial expressions into four categories: `Pleased`, `Angry`, `Alarmed`, and `Calm`.

The objective is to identify which model performs better in low-data settings using both default and manually-split datasets.

---

## 📂 Dataset

This project uses a dataset of domestic cat facial expressions from Roboflow Universe.

The full dataset contains **1,348 images** across four emotion categories: `alarmed`, `angry`, `calm`, and `pleased`.

### 🔗 Original Dataset (default split)
The original dataset used in our experiment is publicly available at:  
[Roboflow Dataset Link](https://universe.roboflow.com/mubbarryz/domestic-cats-facial-expressions/dataset/4)

### 📁 Custom Dataset (manual 70/15/15 split)
We also created a custom-split version of the dataset (70% train, 15% validation, 15% test) to better control class distribution and test performance differences.

📥 The file manual_cat_dataset.zip is already included in this repository under the datasets/ folder.

---

## ⚠️ Runtime and GPU Recommendation

Training these deep learning models can take **a significant amount of time**, especially on large datasets or without GPU acceleration.

> ⚠️ **Note:** This notebook may take a long time to run without GPU acceleration.  
> It is recommended to use **Google Colab** with a **T4 GPU** enabled.

To enable it in Colab:  
`Runtime > Change runtime type > Hardware accelerator > GPU`

---

## 🧪 Models and Experiments

| Model       | Dataset Split         | File                             |
|-------------|------------------------|----------------------------------|
| ResNet18    | Original (default)     | `CNN_ResNet18_Original.ipynb`   |
| MobileViT   | Original (default)     | `VIT_mobileVIT_Original.ipynb`  |
| ResNet18    | Manual (70/15/15)      | `CNN_ResNet18_Manual.ipynb`     |
| MobileViT   | Manual (70/15/15)      | `VIT_mobileVIT_manual.ipynb`    |

---

## 🧠 Requirements

To run this project, install the following:

```bash
pip install torch torchvision timm matplotlib scikit-learn
