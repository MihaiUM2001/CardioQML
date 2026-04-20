# QuantumBoostNet: A Hybrid Classical-Quantum Architecture for Enhanced Accuracy in Cardiac Ultrasound View Identification

## Contents

- [1. Project Structure](#1-project-structure)
- [2. Environment SetUp](#2-environment-setup)
- [3. Configuring The Paths SetUp Files](#3-configuring-the-paths-setup-files)

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

The relevant structure inside `ViewClassification` is:

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

## 2. Environment SetUp

For this project, `Python` (version **3.12.12**), `Conda`, `Jupyter Notebook`, and `ipykernel` were the main tools used:

```bash
conda create -n QML python=3.12.12
pip install notebook
pip install ipykernel
python -m ipykernel install --user --name QML_kernel
```

The main libraries utilized (and their respective versions) are:

```text
matplotlib     3.10.8
numpy          2.4.0
pandas         2.3.3
pennylane      0.44.0
scikit-learn   1.8.0
seaborn        0.13.2
torch          2.9.1
torchvision    0.24.1
```

## 3. Configuring The Paths SetUp Files

The `paths_setup.py` files store the local paths used by the project to load and save important resources, such as datasets or models.

Here is an example of what the `paths_setup.py` file for `VC_Default` should look like:
```python
from pathlib import Path

TRAIN_DIR  = Path(r"/<INSERT_ROOT_DIR_HERE>/CardioQML/Dataset/View Classification/train")
TEST_DIR   = Path(r"/<INSERT_ROOT_DIR_HERE>/CardioQML/Dataset/View Classification/test")

MODEL_DIR  = Path(r"/<INSERT_ROOT_DIR_HERE>/CardioQML/ViewClassification/VC_Default/Models")
```

Here is an example of what the `paths_setup.py` file for `VC_FashionMNIST` should look like:
```python
from pathlib import Path

MODEL_DIR  = Path(r"/<INSERT_ROOT_DIR_HERE>/CardioQML/ViewClassification/VC_FashionMNIST/Models")
```

Here is an example of what the `paths_setup.py` file for `VC_MNIST` should look like:
```python
from pathlib import Path

MODEL_DIR  = Path(r"/<INSERT_ROOT_DIR_HERE>/CardioQML/ViewClassification/VC_MNIST/Models")
```