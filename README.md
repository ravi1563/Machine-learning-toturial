# K-Means Clustering and Polynomial Regression on Diabetes Dataset

## Overview

This project demonstrates a combination of **unsupervised learning (K-means clustering)** and **supervised learning (polynomial regression)** on the classic Diabetes regression dataset from scikit-learn. The analysis explores the relationship between clinical features and disease progression, and identifies patient clusters based on key clinical attributes.

## Objectives

- Explore and visualize the diabetes dataset
- Use **Polynomial Regression** to model non-linear relationships between clinical features and disease progression
- Use **K-Means Clustering** to group patients based on clinical attributes
- Generate required visualizations for analysis and reporting

## Dataset

The project uses the **Diabetes dataset** from scikit-learn (`load_diabetes()`), which contains:
- **442 patients**
- **10 standardized clinical features** (e.g., BMI, blood pressure, serum measurements)
- A continuous target variable measuring **disease progression** one year after baseline

## Features Analyzed

The clustering analysis focuses on 8 key clinical features:
- `bmi` - Body Mass Index
- `bp` - Blood Pressure
- `s1` - Total Serum Cholesterol (tc)
- `s2` - Low-Density Lipoproteins (ldl)
- `s3` - High-Density Lipoproteins (hdl)
- `s4` - Total Cholesterol / HDL (tch)
- `s5` - Log of Serum Triglycerides (ltg)
- `s6` - Blood Sugar Level (glu)

## Visualizations Generated

The notebook produces the following figures:

1. **Figure 1: Histogram** - Distribution of diabetes progression target variable
2. **Figure 2: Heatmap** - Correlation matrix of features and target
3. **Figure 3: Scatter Plot with Polynomial Fits** - Disease progression vs BMI with polynomial regression fits (degrees 1, 2, 3)
4. **Figure 4: Elbow Plot** - K-means clustering inertia vs number of clusters (K=1 to 10)
5. **Figure 5: PCA 2D Visualization** - K-means clusters projected onto 2D using Principal Component Analysis

## Key Results

### Polynomial Regression
- **Degree 1 MSE**: 3890.46
- **Degree 2 MSE**: 3889.70
- **Degree 3 MSE**: 3883.35

The analysis shows that higher-degree polynomial regression provides better fit (lower MSE) for modeling the relationship between BMI and disease progression.

### K-Means Clustering
- **Optimal K**: 3 clusters
- **Cluster Distribution**:
  - Cluster 0: 107 patients (Mean progression: 171.40)
  - Cluster 1: 195 patients (Mean progression: 106.59)
  - Cluster 2: 140 patients (Mean progression: 200.84)

## Requirements

See `requirements.txt` for the complete list of dependencies.

Main libraries:
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Installation

1. Clone or download this repository
2. Install required packages:

```bash
pip install -r requirements.txt
```

## Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook notebook18.ipynb
```

2. Run all cells sequentially to reproduce the analysis

The notebook is self-contained and loads the diabetes dataset directly from scikit-learn (no external data files required).

## Project Structure

```
.
├── notebook18.ipynb      # Main analysis notebook
├── requirements.txt      # Python dependencies
└── README.md            # This file
```

## Methodology

1. **Data Loading**: Load and inspect the diabetes dataset from scikit-learn
2. **Exploratory Data Analysis (EDA)**:
   - Distribution analysis of target variable
   - Correlation analysis via heatmap
3. **Polynomial Regression**:
   - Feature selection (BMI chosen based on correlation)
   - Model fitting with degrees 1, 2, and 3
   - Performance evaluation using Mean Squared Error (MSE)
4. **K-Means Clustering**:
   - Feature standardization (critical for K-means)
   - Elbow method for optimal K selection
   - Final clustering with K=3
   - PCA visualization for 2D cluster representation
   - Cluster interpretation via summary statistics

## Author

**Faizan Ahsraf**

## Course Information

Machine Learning Neural Networks - Individual Assignment (40%)
University of Hull, Semester 2, Jan 2025

## License

This project is for educational purposes as part of academic coursework.

