# A Hybrid Deep Learning Approach for Multi-Class Eye Disease Classification

Official repository for the paper: **"A Hybrid Deep Learning Approach for Multi-Class Eye Disease Classification"**, accepted and published in the **Springer Nature Lecture Notes in Electrical Engineering (LNEE) book series** (Proceedings of the 16th International Conference Confluence 2026).

---

## 📌 Abstract
Eye diseases are among the leading causes of visual impairment globally. This repository contains the source code for a hybrid dual-backbone deep learning architecture designed for the automatic classification of retinal fundus images into six distinct disease categories (ACRIMA, Glaucoma, ODIR-5K, ORIGA, Cataract, and Retina Disease). 

By simultaneously leveraging **DenseNet201** for fine-grained localized features and **EfficientNetB4** for global spatial context, the framework overcomes traditional single-backbone limitations. To mitigate severe class imbalances (up to a 22:1 ratio), the system integrates advanced data augmentation, progressive unfreezing strategies, and **Categorical Focal Loss with label smoothing**, achieving an overall test accuracy of **95.34%** and a micro-AUC of **0.9972**.

---

## 🚀 Key Features & Architecture
- **Dual-Backbone Feature Fusion:** Parallel feature extraction using DenseNet201 and EfficientNetB4 pipelines coupled via Global Average Pooling (GAP) and feature concatenation.
- **Imbalance Mitigation:** Implementation of mathematical Categorical Focal Loss to heavily weight misclassified minority classes (e.g., Glaucoma).
- **Academic Baseline:** Built explicitly to serve as a robust baseline for upcoming extensions in **Quantum Machine Learning (QML)**, generative data synthesis, and hybrid classical-quantum classification layers.

---


## 📊 Experimental Results & Metrics

The proposed hybrid network yields highly competitive classification performances across balanced and imbalanced targets:

| Class | Precision (%) | Recall (%) | F1-Score (%) | Training Samples |
| :--- | :---: | :---: | :---: | :---: |
| **ACRIMA** | 100.00 | 99.00 | 100.00 | 1741 |
| **Glaucoma** | 59.00 | 18.00 | 27.00 | 383 |
| **ODIR-5K** | 99.00 | 100.00 | 99.00 | 6678 |
| **ORIGA** | 82.00 | 100.00 | 90.00 | 529 |
| **Cataract** | 88.00 | 93.00 | 90.00 | 870 |
| **Retina Disease** | 58.00 | 50.00 | 54.00 | 870 |

* **Overall Performance Summary:** Best Validation Accuracy: `98.00%` (Epoch 48) | Final Test Accuracy: `95.34%` | Micro-Average AUC: `0.9972`.

---


 Dataset: The system uses the publicly available **Eye Disease Dataset** (11,913 images). Download the files from Kaggle and place them in your designated data directory.

---

## 📜 Citation

If you find this architecture or dataset strategy helpful for your research, please cite our publication:

```bibtex
@inproceedings{surat2026hybrid,
  title={A Hybrid Deep Learning Approach for Multi-Class Eye Disease Classification},
  author={Surat, S. S. V. N. B. and Harshith, Y. S. and Menariya, N. and Venkateswaran, S. and Batchu, R. K. and Kumar, C.},
  booktitle={Proceedings of the 16th International Conference Confluence 2026},
  series={Lecture Notes in Electrical Engineering (LNEE)},
  publisher={Springer Nature},
  year={2026}
}
```
