# 🧠 Temporal Clustering in Dynamic Medical Datasets

## 📌 Project Overview
This project explores **temporal clustering techniques** for identifying disease progression patterns in **longitudinal medical imaging biomarkers**, with a focus on **Alzheimer's detection**.

We use unsupervised learning to discover patient trajectory clusters and apply supervised learning (SVM) for binary classification of Alzheimer's based on temporal biomarker trends.

---

## 📚 Dataset

**Source**: [[OASIS-3 Longitudinal Dataset]([https://www.kaggle.com/datasets/jboysen/mri-and-alzheimers])
](https://www.kaggle.com/datasets/jboysen/mri-and-alzheimers)

**Biomarkers used**:
- `CDR` – Clinical Dementia Rating
- `MMSE` – Mini-Mental State Examination
- `eTIV` – Estimated Total Intracranial Volume
- `nWBV` – Normalized Whole Brain Volume

---

## 🧪 Methodology

### 1. **Preprocessing**
- Extracted subjects with ≥ 6 visits
- Interpolated missing visits
- Z-score normalization
- Principal Component Analysis (PCA) for dimensionality reduction

### 2. **Temporal Clustering**
- Applied **KMeans clustering** on PCA-transformed data
- Optimal `k=2` selected via Silhouette Score
- Visualized mean biomarker trajectories per cluster

### 3. **Alzheimer’s Detection**
- Label: `CDR >= 0.5` → Alzheimer’s
- Model: **Support Vector Machine (SVM)**
- Features: PCA components of temporal trajectories
- Evaluation:
  - Accuracy: `96%`
  - ROC-AUC: `0.985`
  - F1-score (Alzheimer’s): `0.95`

### 4. **Generalization Check**
- 5-fold cross-validation
- ROC curve, confusion matrix, classification report
- Cross-validated AUC: `0.984` ✅

---

## 📊 Visualizations
- Biomarker trajectory plots (cluster-wise)
- Confusion matrix heatmap
- ROC curves (train and cross-validation)

---

## 📁 Files
- `Temporal_Clustering_in_Dynamic_Medical_Datasets.ipynb`: Main Jupyter notebook
- `README.md`: Project documentation
- `paper.pdf`: IEEE-style research paper (coming soon)

---

## 🛠️ Technologies
- Python 3.x
- Scikit-learn
- Pandas, NumPy
- Matplotlib, Seaborn

---

## 📈 Results
The pipeline demonstrates that temporal biomarker clustering can be a robust basis for early Alzheimer’s detection, with strong generalization and interpretability.

---

## 📃 References

1. Goutte, C., et al. (2001). “Clustering fMRI time series.” *NeuroImage*.
2. Chi, Y., et al. (2007). “Evolutionary spectral clustering by incorporating temporal smoothness.” *KDD*.
3. Marcus, D. S., et al. (2007). “Open Access Series of Imaging Studies (OASIS): Longitudinal MRI Data in Nondemented and Demented Older Adults.” *JCN*.

---

## 👤 Author

**Mirza Shaheen Iqubal**  
M.Sc. Data Science, FAU Erlangen-Nürnberg  
Supervised by: Prof. Dr. Jana Hutter
