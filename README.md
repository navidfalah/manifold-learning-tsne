# 🌌 Manifold Learning and t-SNE

Welcome to the **Manifold Learning and t-SNE** repository! This project explores dimensionality reduction techniques, specifically **PCA** and **t-SNE**, to visualize high-dimensional data in 2D space.

---

## 📂 **Project Overview**

This repository demonstrates how to use **Principal Component Analysis (PCA)** and **t-Distributed Stochastic Neighbor Embedding (t-SNE)** to visualize the **Digits Dataset**. It includes:

- **PCA**: Linear dimensionality reduction.
- **t-SNE**: Non-linear dimensionality reduction for visualizing clusters.
- **Visualizations**: 2D scatter plots of reduced data.

---

## 🛠️ **Tech Stack**

- **Python**
- **Scikit-learn**
- **mglearn**
- **NumPy**
- **Matplotlib**

---

## 📊 **Dataset**

The project uses the **Digits Dataset**, which contains 8x8 images of handwritten digits (0-9). Each image is represented as a 64-dimensional feature vector.

---

## 🧠 **Key Concepts**

### 1. **Principal Component Analysis (PCA)**
- A linear dimensionality reduction technique.
- Projects data onto the directions of maximum variance.

### 2. **t-SNE**
- A non-linear dimensionality reduction technique.
- Focuses on preserving local relationships between data points.
- Ideal for visualizing clusters in high-dimensional data.

---

## 🚀 **Code Highlights**

### PCA Visualization
```python
pca = PCA(n_components=2)
digits_pca = pca.fit_transform(digits.data)
plt.figure(figsize=(10, 10))
for i in range(len(digits.data)):
    plt.text(digits_pca[i, 0], digits_pca[i, 1], str(digits.target[i]),
             color=colors[digits.target[i]], fontdict={'weight': 'bold', 'size': 9})
plt.xlabel("First principal component")
plt.ylabel("Second principal component")
```

### t-SNE Visualization
```python
tsne = TSNE(random_state=42)
digits_tsne = tsne.fit_transform(digits.data)
plt.figure(figsize=(10, 10))
for i in range(len(digits.data)):
    plt.text(digits_tsne[i, 0], digits_tsne[i, 1], str(digits.target[i]),
             color=colors[digits.target[i]], fontdict={'weight': 'bold', 'size': 9})
plt.xlabel("t-SNE feature 0")
plt.ylabel("t-SNE feature 1")
```

---

## 🛠️ **Installation**

1. Clone the repository:
   ```bash
   git clone https://github.com/navidfalah/manifold-learning-tsne.git
   cd manifold-learning-tsne
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:
   ```bash
   jupyter notebook manifold_learning_tsne.ipynb
   ```

---

## 🤝 **Contributing**

Feel free to contribute to this project! Open an issue or submit a pull request.

---

## 📧 **Contact**

- **Name**: Navid Falah
- **GitHub**: [navidfalah](https://github.com/navidfalah)
- **Email**: navid.falah7@gmail.com
