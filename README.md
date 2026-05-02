# AI Plant Disease Detection System

![Python](https://img.shields.io/badge/Python-DeepLearning-blue)
![PyTorch](https://img.shields.io/badge/Framework-PyTorch-red)
![Flask](https://img.shields.io/badge/Backend-Flask-green)
![Computer Vision](https://img.shields.io/badge/AI-ComputerVision-orange)

A deep learning-powered plant disease detection system that classifies crop diseases from leaf images across **39 disease categories** using CNNs trained on the PlantVillage dataset.

---

## My Contributions

This project was built on top of a base model. Everything listed below was implemented, refined, and documented by me:

- **Model evaluation & failure analysis** — evaluated the CNN across all 39 class distributions, identified underperforming classes, and iterated on data augmentation strategies to improve validation accuracy on difficult categories
- **Data augmentation pipeline** — implemented and tuned augmentation techniques (rotation, flipping, colour jitter) to address class imbalance and improve generalisation
- **Flask web application** — built and deployed the full prediction interface in `Flask Deployed App/`, including the disease detection UI, results page, and fertiliser/supplement recommendation output
- **End-to-end pipeline verification** — tested the complete flow from raw image input → preprocessing → model inference → prediction display across the full test image set (`test_images/`)
- **Demo image curation** — prepared and documented representative demo images (`demo_images/`) covering a range of disease classes for reproducible testing
- **Documentation** — rewrote the README and inline documentation so the project can be set up and run end-to-end without prior knowledge of the codebase
- **Repository structure** — organised the repo into clear folders (`Model/`, `Flask Deployed App/`, `demo_images/`, `test_images/`) with consistent naming

---

## Model Details

| Property | Value |
|----------|-------|
| Architecture | Convolutional Neural Network (CNN) |
| Framework | PyTorch |
| Dataset | PlantVillage |
| Disease classes | 39 |
| Task | Multi-class image classification |

---

## Project Structure

```
.
├── Model/                   # Trained model weights & training notebook
├── Flask Deployed App/      # Web prediction interface
│   ├── app.py               # Flask application
│   └── templates/           # UI templates
├── demo_images/             # Curated demo images by disease class
├── test_images/             # Test set for pipeline verification
└── README.md
```

---

## Setup & Run

```bash
pip install -r requirements.txt
```

### Run the Flask App

```bash
cd "Flask Deployed App"
python app.py
```

Visit `http://localhost:5000` — upload a leaf image to get a disease classification and fertiliser recommendation.

---

## Features

- **39-class disease classification** from leaf images
- **Fertiliser & supplement recommendations** based on detected disease
- **Interactive web UI** with image upload and results display
- **Demo images included** for quick testing without a camera

---

## Disease Classes

The model covers 39 plant disease categories across crops including tomato, potato, pepper, apple, corn, grape, and more — sourced from the PlantVillage benchmark dataset.

---

## What I Learned

Working through the per-class failure analysis on this project gave me a concrete understanding of how class imbalance affects CNN performance, how to read a confusion matrix to identify systematic misclassifications, and how iterative data augmentation can shift accuracy on specific failure categories without degrading the overall model.
