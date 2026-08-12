# Projects - Machine Learning

Practical assignments developed for the **Machine Learning (MC886)** course at **UNICAMP**. Each project is a self-contained Jupyter notebook (plus its dataset) exploring a different family of models, moving from classical linear methods to deep neural networks and questions of generalization under distribution shift.

## Repository Structure

```
├── Project01/   # Linear Models
├── Project02/   # Model Selection and Regularization
└── Project03/   # Neural Networks and Overparameterization
```

---

## Project 01 - Linear Models

**Purpose:** Predict hourly bike-share rental counts from a time-ordered dataset (Bike Sharing), using linear regression and other generalized linear models. The focus is on understanding the assumptions behind linear models and how feature engineering choices affect predictive performance on a chronological train/test split.

**Skills & techniques:**
- Exploratory data analysis (distributions, correlations, temporal trends, categorical vs. continuous features)
- Data preprocessing: outlier handling, feature scaling, one-hot encoding of categorical variables
- Time-respecting train/test split to avoid data leakage
- Linear Regression implemented from scratch with gradient descent
- Custom implementation of evaluation metrics (MSE, R², MAE)
- Hyperparameter exploration (learning rate sweep) and its effect on convergence

## Project 02 - Model Selection and Regularization

**Purpose:** Study how regularization interacts with data availability and distribution shift, using a corrupted variant of MNIST (MNIST-C). Models are trained only on corrupted images across three data regimes (scarce, partial, full) and later evaluated on both corrupted and clean test sets to see how well decisions made purely from cross-validation transfer to unseen, uncorrupted data.

**Skills & techniques:**
- Image data preprocessing (flattening, min-max normalization) with correct train/test statistic isolation
- Multinomial (softmax) logistic regression implemented with PyTorch
- L1 and L2 regularization, with weight-sparsity/weight-map visualization for interpretability
- K-fold cross-validation for hyperparameter (λ) selection
- Model evaluation under distribution shift (in-distribution vs. out-of-distribution test performance)
- Comparative analysis across data regimes to study overfitting under data scarcity

## Project 03 - Neural Networks and Overparameterization

**Purpose:** Investigate how architectural choices and overparameterization affect generalization under distribution shift, using the Camelyon17 histopathology benchmark (tumor vs. normal tissue classification across different hospitals). The project isolates the contribution of specific inductive biases (transfer learning, convolutional structure, color features) to out-of-distribution (OOD) generalization.

**Skills & techniques:**
- Exploratory analysis of medical imaging data (class imbalance, per-hospital variation, pixel intensity distributions)
- Transfer learning via a frozen pretrained ResNet-18 backbone with a linear probe classifier
- Architectural ablations: MLP vs. small CNN to isolate the effect of convolutional (spatial) inductive bias
- Feature ablations: grayscale conversion to test reliance on spurious color correlations
- Binary classification with PyTorch (custom training loop, early stopping)
- Evaluation via AUC-ROC, ROC curves, and confusion matrices
- In-distribution (ID) vs. out-of-distribution (OOD) generalization analysis across hospital sites
- Parameter-count vs. generalization trade-off analysis (overparameterization)
