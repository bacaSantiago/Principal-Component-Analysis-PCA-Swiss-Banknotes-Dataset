# Principal Component Analysis (PCA): Swiss Banknotes Dataset

---

## Overview

This project explores the application of **Principal Component Analysis (PCA)** to the problem of distinguishing between genuine and counterfeit Swiss 1000-franc banknotes. The dataset consists of **six key measurements** taken from both real and counterfeit banknotes, including features such as length, height, and diagonal dimensions. By applying PCA, we aim to reduce the dimensionality of the dataset while retaining the most informative aspects of the variance, ultimately improving our ability to differentiate between genuine and fake banknotes.

The project involves the following key steps:

1. **Exploratory Data Analysis (EDA)**: Computing the mean, variance, and covariance matrix of the original data.
2. **Eigenvalue and Eigenvector Calculation**: Extracting the principal components from the covariance matrix.
3. **Principal Component Transformation**: Projecting the original data onto the principal component space to generate new variables, known as the principal components.
4. **Dimensionality Reduction**: Selecting the most significant components that capture the majority of the variance.
5. **Standardization of Data**: Ensuring that all variables have equal influence by scaling them to have unit variance before applying PCA (Normalized PCA).

The analysis demonstrates how PCA can be used to simplify high-dimensional data, identify the most informative features, and visualize the inherent differences between genuine and counterfeit banknotes.

---

## Dataset

The dataset consists of **six variables** (measurements) for 200 banknotes, including 100 genuine and 100 counterfeit notes:

- **X1**: Length of the banknote
- **X2**: Height of the banknote (left side)
- **X3**: Height of the banknote (right side)
- **X4**: Distance of the inner frame to the lower border
- **X5**: Distance of the inner frame to the upper border
- **X6**: Length of the diagonal

Each variable is measured in millimeters.

---

## Key Concepts

### Principal Component Analysis (PCA)

PCA is a technique used to **reduce the dimensionality** of a dataset by transforming the original variables into a new set of **uncorrelated variables** called **principal components**. These components are ordered by the amount of variance they capture from the original dataset. The first few principal components typically capture most of the variance, allowing for **dimensionality reduction** while retaining the critical information.

### Eigenvalues and Eigenvectors

The **eigenvalues** represent the amount of variance captured by each principal component, while the **eigenvectors** represent the direction (or axis) along which the variance is maximized. By decomposing the covariance matrix into its eigenvalues and eigenvectors, we can identify the most important components in the data.

### Covariance and Correlation Matrix

The **covariance matrix** reflects the relationships between variables, showing how changes in one variable correspond to changes in another. In contrast, the **correlation matrix** standardizes these relationships, providing a clearer picture of the strength and direction of these relationships, independent of the units of measurement.

---

## Methodology

### 1. Exploratory Data Analysis (EDA)

- Calculation of the **mean vector** and **covariance matrix**.
- These basic statistics provide an initial understanding of how the variables are distributed and related.

### 2. Eigenvalue and Eigenvector Calculation

- **Eigenvalue decomposition** of the covariance matrix is performed to extract the **principal components**.
- The **eigenvectors** are used to transform the original data into the principal component space, while the **eigenvalues** indicate how much variance each component captures.

### 3. Principal Component Transformation

- The original data is **centered and projected** onto the eigenvectors to obtain the **principal component scores**.
- These scores allow us to visualize the data in the new reduced-dimensional space.

### 4. Dimensionality Reduction

- The **cumulative variance explained** by the principal components is calculated to determine how many components are required to retain a desired proportion of the total variance.
- For instance, the first two components may capture over 80% of the variance, allowing us to reduce the dimensionality from six to two without losing much information.

### 5. Normalized PCA (Standardized Data)

- To ensure that variables measured on different scales (e.g., millimeters vs centimeters) contribute equally to the analysis, the data is standardized using **z-scores**.
- This transformation makes the **covariance matrix equivalent to the correlation matrix**, allowing for a more balanced contribution from each variable.

---

## Dependencies

This project requires the following Python libraries:

- **NumPy**: For numerical computations, including matrix operations and eigenvalue decomposition.
- **Pandas**: For data manipulation and loading the dataset.
- **Matplotlib**: For creating visualizations such as scatter plots and unit circle plots.
- **SciPy**: For additional mathematical functions such as statistical analysis and matrix transformations (if required).

---

## Applications

This PCA analysis can be applied to various domains where **dimensionality reduction** is required. Some possible applications include:

1. **Fraud Detection**: PCA can be used to detect anomalies or outliers in financial data, helping to identify fraudulent transactions or counterfeit currency.
2. **Pattern Recognition**: By reducing the dimensionality of complex datasets, PCA helps to reveal patterns that would otherwise be difficult to detect.
3. **Data Compression**: PCA can reduce the storage and computational requirements for large datasets by eliminating less informative variables.
4. **Visualization**: High-dimensional data can be challenging to visualize. PCA provides a way to project data into two or three dimensions for easier analysis and interpretation.

---

This project demonstrates the power of PCA in revealing the underlying structure of the Swiss banknote dataset, helping to differentiate between genuine and counterfeit banknotes. The analysis highlights the importance of standardization in multivariate techniques and the role of eigenvalue decomposition in uncovering the most informative components of the data.

By reducing the dimensionality of the dataset while preserving its essential variance, PCA proves to be a valuable tool in fraud detection and many other data science applications.  
