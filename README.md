# Deforestation Detection using Satellite Imagery

This repository presents a deep learning–based semantic segmentation approach for detecting deforestation and analyzing land-use changes from satellite imagery. The model is built using **U-Net with a ResNet50 encoder** to classify pixels into different land-use categories such as Forest, Agriculture, Urban areas, Water bodies, and Barren land.

This research work was **presented at the IEEE ICICNIS 2025 Conference** and the paper is available on IEEE Xplore.

Paper Link:
https://ieeexplore.ieee.org/document/11315536

---

# Project Overview

Monitoring environmental changes such as deforestation is important for sustainable development and ecological protection. This project uses semantic segmentation techniques to analyze satellite images and detect land-use patterns.

The system performs the following tasks:

• Detects land-use categories in satellite imagery
• Identifies forest regions and changes over time
• Performs year-wise land-use analysis
• Finds similar satellite images across datasets using deep feature similarity
• Visualizes forest probability change maps

---

# Model Architecture

Segmentation Model: **U-Net**

Encoder Backbone: **ResNet50 (ImageNet pretrained)**

The encoder extracts deep spatial features from satellite images while the U-Net decoder reconstructs high-resolution segmentation maps for accurate pixel-level classification.

Frameworks and Libraries used in this project include:

• PyTorch
• segmentation-models-pytorch
• OpenCV
• Albumentations
• NumPy
• Matplotlib
• Seaborn
• Scikit-learn

---

# Land-Use Classes

The model classifies satellite image pixels into the following categories.

| Class ID | Land-Use Category |
| -------- | ----------------- |
| 0        | Forest            |
| 1        | Agriculture       |
| 2        | Urban             |
| 3        | Water             |
| 4        | Barren            |

Each class represents a different type of land-use observed in satellite imagery.

---

# Training Configuration

Patch Size: **128 × 128**

Batch Size: **8**

Epochs: **100**

Learning Rate: **0.001**

Loss Function: **CrossEntropyLoss**

Optimizer: **Adam**

Data augmentation techniques such as flipping, rotation, and brightness adjustments were used to improve model generalization.

---

# Model Performance

Overall Validation Accuracy:

**87.96%**

Evaluation metrics used:

• Mean Intersection over Union (IoU)
• Dice Coefficient
• Pixel Accuracy
• Confusion Matrix

These metrics measure the segmentation performance across all land-use classes.

---

# Training Results

## Training Curves

![Training Curves](results/training_curves.png)

The training curves show the progression of:

• Training vs validation loss
• Mean IoU and Dice score across epochs
• Training and validation accuracy

These graphs indicate the learning behavior and convergence of the segmentation model.

---

# Confusion Matrix

![Confusion Matrix](results/confusion_matrix.png)

The confusion matrix provides a detailed visualization of pixel-level classification performance across all land-use classes.

---

# Forest Change Detection

![Forest Change](results/forest_change_uploaded_2020.png)

The system generates forest probability maps and compares them with historical satellite imagery to identify forest changes.

Color interpretation:

Green → Increase in forest probability
Red → Decrease in forest probability

This helps visualize deforestation patterns across different time periods.

---

# Year-wise Land-Use Change

![Land-Use Trend](results/landuse_trend.png)

The model analyzes land-use distribution across multiple years and calculates the percentage of each category.

Example outputs:

2010
Forest: 0.00%
Agriculture: 29.44%
Urban: 66.85%
Water: 3.58%
Barren: 0.13%

2012
Forest: 0.00%
Agriculture: 22.17%
Urban: 67.27%
Water: 9.99%
Barren: 0.57%

2014
Forest: 0.00%
Agriculture: 23.94%
Urban: 69.05%
Water: 6.85%
Barren: 0.16%

2015
Forest: 0.00%
Agriculture: 24.15%
Urban: 70.58%
Water: 5.22%
Barren: 0.04%

2016
Forest: 0.00%
Agriculture: 21.80%
Urban: 72.96%
Water: 5.10%
Barren: 0.14%

2017
Forest: 0.00%
Agriculture: 44.29%
Urban: 50.22%
Water: 5.10%
Barren: 0.39%

2018
Forest: 0.00%
Agriculture: 11.71%
Urban: 68.62%
Water: 18.55%
Barren: 1.12%

2019
Forest: 0.00%
Agriculture: 11.71%
Urban: 68.62%
Water: 18.55%
Barren: 1.12%

2020
Forest: 0.00%
Agriculture: 11.71%
Urban: 68.62%
Water: 18.55%
Barren: 1.12%

2021
Forest: 0.00%
Agriculture: 26.31%
Urban: 44.22%
Water: 29.13%
Barren: 0.35%

---

# Repository Structure

```
Deforestation-Detection-using-Satellite-Imagery
│
├── README.md
├── LICENSE
│
├── results
│   ├── training_curves.png
│   ├── confusion_matrix.png
│   ├── forest_change_uploaded_2020.png
│   └── landuse_trend.png
│
├── model
│   └── best_model.pth
│
└── code
    ├── training.py
    └── inference.py
```

---

# How to Run the Project

Install required libraries

```
pip install torch torchvision segmentation-models-pytorch albumentations opencv-python matplotlib seaborn scikit-learn
```

Train the model

```
python training.py
```

Run inference and land-use analysis

```
python inference.py
```

---

# Citation

If you use this project in research or academic work, please cite the published paper.

Deforestation Detection using Satellite Imagery
IEEE ICICNIS 2025

Paper Link:
https://ieeexplore.ieee.org/document/11315536

---

# License

This project is released under the **MIT License.

---

# Author            

Gajanand Immannavar
