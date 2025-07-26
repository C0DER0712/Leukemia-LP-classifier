# 🧬 Leukemia Classification using Linear Programming

This project implements a **custom linear programming (LP)**-based binary classifier for **leukemia subtype classification** using **gene expression data**. Instead of relying on traditional classification models (e.g., SVM, Logistic Regression), this approach formulates the classification task as a **linear optimization problem**, solved via the PuLP library.

---

## 📌 Project Overview

- **Objective**: To classify leukemia types using a linear programming-based classifier.
- **Approach**: One-vs-One strategy using LP as a base binary classifier.
- **Dataset**: Gene expression data sourced from the **CuMiDa** database. (Leukemia_GSE9476.csv)
- **Date**: December 2024

---

## ⚙️ Tools & Technologies Used

- **Programming Language**: Python
- **Libraries**:
  - `PuLP` – for defining and solving the LP problem
  - `NumPy` – for numerical computations
  - `Pandas` – for data handling
  - `Scikit-learn` – for preprocessing, train-test splitting, and evaluation

---

## 📂 Tasks Performed

- ✅ Preprocessed data:
  - Handled missing values
  - Normalized feature values
  - Selected significant features (based on standard deviation threshold)
- ✅ Implemented a **Linear Programming Classifier** from scratch using PuLP
- ✅ Adopted a **One-vs-One strategy** to handle multiclass classification
- ✅ Evaluated performance using:
  - Accuracy
  - Precision
  - Recall
- ✅ Demonstrated potential for clinical applicability by achieving strong classification results on high-dimensional genetic data

---

## 🧪 How the Classifier Works

The classifier optimizes a linear boundary to separate one class from others by solving a **linear programming problem**:
- Each instance must satisfy a constraint with slack variables to allow for minor misclassification.
- The LP objective is to minimize the sum of slack (classification error).
- This is implemented in the `LPClassifier` class.

---

## 🗃️ Dataset Info

- **Source**: [CuMiDa (Curated Microarray Database)](https://www.kaggle.com/datasets/brunogrisci/leukemia-gene-expression-cumida)
- Includes gene expression profiles for various cancer types
- This project focuses on **leukemia samples** extracted from CuMiDa

---

## 🤔 Future Improvements

- Use **L1-regularized LP** for automatic feature selection  
- Explore **non-linear extensions** using kernelized LP formulations  
- Benchmark against ensemble models (Random Forest, Gradient Boosting)  
- Apply to larger and more diverse clinical datasets  


