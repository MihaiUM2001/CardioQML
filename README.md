# QuantumBoostNet: A Hybrid Classical-Quantum Architecture for Enhanced Accuracy in Cardiac Ultrasound View Identification

## Contents

- [1. Project Structure](#1-project-structure)

## 1. Project Structure

The repository is organized around the main `CardioQML` directory, which contains the following resources:

```text
CardioQML/
├── Dataset/View Classification/   # View Classification dataset used by VC_Default
├── ViewClassification/            # View classification experiments and other related assets
│   ├── VC_Default/                # Experiments on the ViewClassification dataset
│   ├── VC_FashionMNIST/           # Experiments on the FashionMNIST dataset
│   └── VC_MNIST/                  # Experiments on the MNIST dataset
├── .gitattributes                 # Git attribute configuration
├── .gitignore                     # Git ignore rules
└── README.md                      # Project documentation
```

The relevant structure inside `ViewClassification/` is:

```text
ViewClassification/
├── VC_Default/
│   ├── Models/                                 # Saved model weights and related outputs
│   ├── paths_setup.py                          # Path configuration helper script
│   ├── ViewClassification.ipynb                # Default training/evaluation notebook
│   └── ViewClassification_NISQ.ipynb           # NISQ training/evaluation notebook
├── VC_FashionMNIST/
│   ├── Data/                                   # FashionMNIST dataset used by VC_FashionMNIST
│   ├── Models/                                 # Saved model weights and related outputs
│   ├── paths_setup.py                          # Path configuration helper script
│   └── ViewClassification_FashionMNIST.ipynb   # FashionMNIST training/evaluation notebook
└── VC_MNIST/
    ├── Data/                                   # MNIST dataset used by VC_MNIST
    ├── Models/                                 # Saved model weights and related outputs
    ├── paths_setup.py                          # Path configuration helper script
    └── ViewClassification_MNIST.ipynb          # MNIST training/evaluation notebook
```
