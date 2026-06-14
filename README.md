[README.md](https://github.com/user-attachments/files/28925316/README.md)
# 🩺 Oral Cancer Detection using CNN & Vision Transformer (ViT)

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-red?logo=keras)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

> A deep learning project for binary classification of oral cancer from lips and tongue images, comparing a custom CNN baseline against a Vision Transformer (ViT) architecture built from scratch.

---

## 🌐 Live Demo

> [Live Demo](https://manideepnellipalli.github.io/Oral-cancer-/)


The live demo hosts an interactive HTML summary of the project including model architecture diagrams, training curves, and sample predictions — viewable directly in the browser without any installation.

---

## 📌 Project Overview

Oral cancer is among the most underdiagnosed cancers globally, largely due to limited access to specialist screening. This project demonstrates how deep learning can assist in early detection by classifying oral tissue images as **cancer** or **non-cancer**.

Two architectures are implemented and compared:

| Model | Approach | Test Accuracy |
|-------|----------|---------------|
| Baseline CNN | Custom 2-layer CNN with regularization | **81.48%** |
| Vision Transformer (ViT) | Patch-based self-attention from scratch | *See training results* |

The project addresses real-world medical imaging challenges including **small dataset size (131 images)**, **class imbalance**, and **high-stakes binary classification**.

---

## ✨ Features

- **Custom CNN baseline** — Conv2D layers, MaxPooling, L1/L2 regularization, and Dropout
- **Vision Transformer (ViT) from scratch** — patch extraction, positional embeddings, multi-head self-attention (no pretrained weights)
- **Class imbalance handling** — `compute_class_weight` with balanced strategy
- **Data augmentation pipeline** — random flip, rotation, zoom via `tf.keras.Sequential`
- **Evaluation suite** — confusion matrix, classification report, training/validation curves
- **Architecture visualizations** — layer diagrams via `visualkeras` and `plot_model`
- **Interactive patch viewer** — `ipywidgets`-based patch exploration for ViT input

---

## 🛠️ Technologies Used

| Category | Tools |
|----------|-------|
| Language | Python 3.10 |
| Deep Learning | TensorFlow 2.x, Keras |
| Data Processing | NumPy, Pandas, OpenCV (`cv2`) |
| Visualization | Matplotlib, Seaborn, Plotly, Visualkeras |
| ML Utilities | Scikit-learn |
| Notebook | Jupyter / Kaggle Notebook |
| Dataset | [Oral Cancer Lips and Tongue Images — Kaggle](https://www.kaggle.com/datasets) |

---

## 📁 Project Structure

```
oral-cancer-detection/
│
├── notebooks/
│   └── oral_cancer_cnn_vit.ipynb       # Main Kaggle notebook
│
├── docs/                                # GitHub Pages site
│   ├── index.html                       # Project summary page (live demo)
│   ├── assets/
│   │   ├── images/
│   │   │   ├── cnn_architecture.png     # CNN model diagram
│   │   │   ├── vit_architecture.png     # ViT architecture
│   │   │   ├── training_curves.png      # Loss & accuracy plots
│   │   │   ├── confusion_matrix.png     # Confusion matrix heatmap
│   │   │   └── sample_patches.png       # ViT patch visualization
│   │   └── style.css
│
├── src/                                 # (Optional) modular Python scripts
│   ├── data_loader.py
│   ├── cnn_model.py
│   ├── vit_model.py
│   └── evaluate.py
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## ⚙️ Installation & Usage

### Prerequisites

- Python 3.10+
- pip or conda

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/oral-cancer-detection.git
cd oral-cancer-detection
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

**`requirements.txt` contents:**
```
tensorflow>=2.12
tensorflow-addons==0.23.0
opencv-python
numpy
pandas
scikit-learn
matplotlib
seaborn
plotly
visualkeras
ipywidgets
vit-keras
Pillow
```

### 3. Download the Dataset

Download from Kaggle: [Oral Cancer Lips and Tongue Images](https://www.kaggle.com/datasets/ashenafifasilkebede/dataset)

Place it as:
```
/kaggle/input/oral-cancer-lips-and-tongue-images/OralCancer/
    ├── cancer/
    └── non-cancer/
```

Or update the `folder_path` variable in the notebook to your local path.

### 4. Run the Notebook

```bash
jupyter notebook notebooks/oral_cancer_cnn_vit.ipynb
```

Or open directly on [Kaggle](https://www.kaggle.com) for GPU-accelerated training.

---

## 📊 Screenshots

### Model Architecture — Baseline CNN
> *Add `docs/assets/images/cnn_architecture.png` — generated via `plot_model()` in the notebook*

![CNN Architecture](docs/assets/images/cnn_architecture.png)

---

### Training Curves — Loss & Accuracy
> *Add `docs/assets/images/training_curves.png` — generated via Matplotlib in the notebook*

![Training Curves](docs/assets/images/training_curves.png)

---

### Confusion Matrix
> *Add `docs/assets/images/confusion_matrix.png` — generated via Seaborn heatmap*

![Confusion Matrix](docs/assets/images/confusion_matrix.png)

---

### ViT Patch Visualization
> *Add `docs/assets/images/sample_patches.png` — captured from the interactive patch viewer*

![Patch Visualization](docs/assets/images/sample_patches.png)

---

## 📈 Results

### Baseline CNN (200 epochs, Adam optimizer)

| Metric | Value |
|--------|-------|
| Training Accuracy | ~99% |
| Validation Accuracy | **81.48%** |
| Optimizer | Adam |
| Loss Function | Binary Crossentropy |
| Regularization | L1L2 + Dropout (0.5) |

> **Note:** High training accuracy vs lower validation accuracy indicates mild overfitting — expected for a 131-image dataset. Class weights mitigated class imbalance.


---

## 🔮 Future Improvements

- [ ] Expand dataset using medical imaging repositories (e.g., TCGA, ISIC)
- [ ] Add **Grad-CAM** visualizations to highlight cancer-relevant image regions
- [ ] Fine-tune a **pretrained ViT** (e.g., `vit-b16` via `vit_keras`) for higher accuracy
- [ ] Build a **Streamlit or Gradio web app** for real-time image upload and prediction
- [ ] Apply **k-fold cross-validation** to produce more reliable accuracy estimates on small data
- [ ] Experiment with **EfficientNet transfer learning** as a stronger CNN baseline
- [ ] Add **LIME / SHAP** explainability for clinical interpretability

---

## 👤 Author

**Manideep**
- 💼 Software Engineer | RPA & Python Developer
- 🏢 QBotica, Chennai, India
- 🔗 [LinkedIn](https://www.linkedin.com/in/manideep-nellipalli-3a33b5270/)
- 🐙 [GitHub](https://github.com/ManideepNellipalli)
- 📧 manideepnellipalli1@gmail.com

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- Dataset: [Kaggle — Oral Cancer Lips and Tongue Images](https://www.kaggle.com/datasets)
- ViT architecture reference: [An Image is Worth 16x16 Words (Dosovitskiy et al., 2020)](https://arxiv.org/abs/2010.11929)
- Keras ViT tutorial: [keras.io/examples/vision/image_classification_with_vision_transformer](https://keras.io/examples/vision/image_classification_with_vision_transformer/)
