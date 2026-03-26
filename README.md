# SVM Kernel Tutorial: How Different Kernels Change Decision Boundaries

A visual tutorial on Support Vector Machine (SVM) kernel selection, created as part of a Machine Learning course assignment.

## Overview

This tutorial demonstrates how the choice of kernel in a Support Vector Machine fundamentally changes the shape of the decision boundary and classification performance. We compare four kernels — **Linear**, **Polynomial**, **RBF**, and **Sigmoid** — on the `make_moons` dataset, a non-linearly separable two-class problem.

By the end of this tutorial, you will understand:
- What the kernel trick is and why it matters
- How each kernel behaves on non-linear data
- Which kernel to choose for your own problems

## Repository Contents

```
svm-kernel-tutorials/
│
├── NAHKUM.ipynb                  # Main Jupyter notebook (code + tutorial)
├── SVM_Kernel_Tutorial.pdf       # Written tutorial (PDF, under 2000 words)
├── README.md                     # This file
└── LICENSE                       # MIT Licence
```

> **Note:** All figures (decision boundaries, scaling comparison, RBF hyperparameter sensitivity) are generated automatically when you run the notebook.

## Getting Started

### Prerequisites

Make sure you have Python 3.8 or higher installed. Then install the required packages:

```bash
pip install numpy pandas matplotlib scikit-learn
```

### Running the Notebook

1. Clone this repository:
   ```bash
   git clone https://github.com/queenSpora/svm-kernel-tutorials.git
   cd svm-kernel-tutorials
   ```

2. Launch Jupyter:
   ```bash
   jupyter notebook
   ```

3. Open `NAHKUM.ipynb` and run all cells (Kernel → Restart & Run All).

The notebook will:
- Generate the `make_moons` dataset
- Visualise the effect of feature scaling (before vs after StandardScaler)
- Train four SVM models (Linear, Polynomial, RBF, Sigmoid)
- Plot decision boundaries for each kernel
- Display an accuracy comparison table
- Show how RBF hyperparameters γ and C affect the decision boundary

## Results Summary

| Kernel     | Test Accuracy | Notes                          |
|------------|---------------|--------------------------------|
| RBF        | ~98%          | Best performer; flexible boundary |
| Polynomial | ~95%          | Good; captures curved structure |
| Sigmoid    | ~85%          | Inconsistent; not always valid |
| Linear     | ~86%          | Underfits non-linear data      |

## Accessibility

- All plots use the **RdBu colourmap** (`cmap="RdBu"`), which is distinguishable for readers with red-green colour blindness (deuteranopia/protanopia). This replaces matplotlib's default colourmap which is not accessible.
- All three figures (decision boundaries, scaling comparison, hyperparameter sensitivity) include **alt-text captions** in both the notebook and the PDF tutorial.
- The PDF tutorial uses clear heading structure for screen reader compatibility.
- Sufficient colour contrast is maintained throughout all text and figures.

## References

1. Cortes, C. & Vapnik, V. (1995). Support-vector networks. *Machine Learning*, 20(3), 273–297. https://doi.org/10.1007/BF00994018
2. Scikit-learn developers (2024). *sklearn.svm.SVC*. https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html
3. Scikit-learn developers (2024). *Support Vector Machines — User Guide*. https://scikit-learn.org/stable/modules/svm.html
4. Müller, A. C. & Guido, S. (2016). *Introduction to Machine Learning with Python*. O'Reilly Media.
5. Pedregosa, F. et al. (2011). Scikit-learn: Machine learning in Python. *Journal of Machine Learning Research*, 12, 2825–2830. https://jmlr.org/papers/v12/pedregosa11a.html

## Licence

This project is licensed under the MIT Licence — see the [LICENSE](LICENSE) file for details.
