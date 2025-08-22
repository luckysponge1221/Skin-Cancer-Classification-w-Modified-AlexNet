# Skin Cancer Classification with Modified AlexNet
This repository contains experiments on **skin cancer classification** using the [HAM10000 dermoscopic image dataset](https://www.kaggle.com/kmader/skin-cancer-mnist-ham10000). The project explores the use of **AlexNet-inspired CNN architectures** with different activation functions, comparing the baseline **ReLU** to a **custom activation function** proposed in a referenced journal.

## Repository Structure
- **`skincancer (A).ipynb`** – Baseline **AlexNet-inspired CNN** implementation using **ReLU activation** (~75% accuracy).  
- **`hore siscer pt 2 (B).ipynb`** – Modified CNN using the **custom activation function** $$y(x) = (x e^x) \cdot \tanh(\text{softplus}(-x))$$ from the referenced journal (~76% accuracy).  

## Dataset
- **HAM10000**: 10,015 dermoscopic images of skin lesions, 7 classes.  
- **Preprocessing**: resizing, normalization, augmentation.  
- **Imbalance handling**: **SMOTE oversampling** applied to balance classes.  

## Methods
1. **Baseline (Notebook A)**  
   - AlexNet-inspired CNN with ReLU activation.  
   - Input size: 64×64.  
   - Achieved ~75% accuracy.  

2. **Modified Model (Notebook B)**  
   - Custom activation function from journal: $\((x e^x)\cdot \tanh(\text{softplus}(-x))\)$.  
   - Input size: 28×28.  
   - Achieved ~76% accuracy.  

## Evaluation
Both models were evaluated using:  
- **Accuracy**  
- **Classification Reports (precision, recall, F1-score)**  
- **Confusion Matrices** to analyze per-class performance.  

## Tools & Libraries
- [TensorFlow/Keras](https://www.tensorflow.org/)  
- [scikit-learn](https://scikit-learn.org/)  
- [pandas](https://pandas.pydata.org/)  
- [numpy](https://numpy.org/)  
- [matplotlib](https://matplotlib.org/)  
- [seaborn](https://seaborn.pydata.org/)  

## Reference
[Rajput, G. (2021). *An accurate and noninvasive skin cancer screening based on imaging technique*.](https://onlinelibrary.wiley.com/doi/abs/10.1002/ima.22616)  

## Conclusion
- The baseline AlexNet-inspired CNN with ReLU achieved ~75% accuracy.  
- The modified CNN with the journal’s proposed activation function slightly improved performance to ~76%.  
- Results highlight the role of **activation functions** in medical image classification tasks.  
