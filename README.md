# K-Means Clustering on the Iris Dataset

This repository contains an implementation of the **K-Means Clustering** algorithm applied to the classic Iris dataset using `scikit-learn` and `pandas`.

---

## 📌 Table of Contents
- [Overview](#overview)
- [How K-Means Works](#how-k-means-works)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)

---

## 📖 Overview

K-Means is an unsupervised machine learning algorithm designed to partition $N$ observations into $K$ distinct clusters based on feature similarity. In this project, we cluster 150 Iris flower samples into 3 clusters corresponding to their underlying species features.

---

## ⚙️ How K-Means Works

The algorithm follows these core iterative steps:

1. **Initialization:** Randomly select $K$ initial points to serve as cluster centroids ($K = 3$).
2. **Assignment:** Calculate the distance (e.g., Euclidean distance) between each dataset point and all centroids, assigning each point to its nearest centroid.
3. **Update Centroids:** Recompute the position of each centroid by taking the mean of all data points assigned to that cluster.
4. **Convergence:** Repeat steps 2 and 3 until centroid positions stabilize (reach convergence).

---

## 📊 Dataset Information

The **Iris Dataset** consists of 150 instances with 4 numerical features:
- Sepal Length (cm)
- Sepal Width (cm)
- Petal Length (cm)
- Petal Width (cm)

Target classes present in the dataset (used for implicit context): `Setosa`, `Versicolor`, `Virginica`.

---

## 🚀 Project Workflow

1. **Data Loading:** Extract data from `sklearn.datasets.load_iris`.
2. **Data Transformation:** Load numerical features into a structured `pandas.DataFrame`.
3. **Data Splitting:** Divide dataset into training ($80\%$) and testing ($20\%$) subsets using `train_test_split`.
4. **Model Training:** Fit `scikit-learn`'s `KMeans(n_clusters=3, random_state=42)` model on the training data.

---

## 🛠️ Installation & Setup

Ensure you have Python installed, then clone this repository and install the dependencies:

```bash
git clone [https://github.com/your-username/kmeans-iris-clustering.git](https://github.com/your-username/kmeans-iris-clustering.git)
cd kmeans-iris-clustering
pip install numpy pandas scikit-learn
