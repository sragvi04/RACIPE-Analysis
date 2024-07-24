# RACIPE-Analysis

This analysis was a part of a study that explores the inhibitory effects of fasting on Epithelial to Mesenchymal Transition (EMT) using RACIPE and Genome Scale Metabolic Modeling during my summer internship programme at IISC, Bangalore.

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Data Analysis](#data-analysis)
- [Results](#results)

## Introduction

The built Gene Regulatory Network (GRN) from literature survey was the basis to create a topology file, which served as input for RACIPE. RACIPE processed this topology input to generate gene expressions for each stable state of 10,000 models. The gene expression data for six genes—mTOR, AMPK, SNAIL, ZEB, miR-200, and miR-34—was subsequently z-normalized.

We then determined a score called the metabolic score, calculated as AMPK-mTOR, to capture the fasting state based on gene expressions. A higher expression of AMPK and a
lower expression of mTOR indicated a fasting state, represented by a positive value in the metabolic score.
Similarly, the EMT score was determined by subtracting mesenchymal markers from epithelial markers
(SNAIL + ZEB - miR-200 - miR-34) to predict the direction of the transition epithelial or mesenchymal.
Plots were then generated from this data and were analyzed using the Seaborn library in Python.


## Installation

To run the notebook and reproduce the results, you need to install the required dependencies. You can install them using the following commands:

```bash
pip install pandas numpy matplotlib seaborn scipy
```
## Data Analysis
The racipe 2 analysis.ipynb notebook performs the following steps:

- Libraries and Dependencies: Imports necessary libraries such as pandas, numpy, seaborn, matplotlib, and scipy.
- Data Loading: Reads gene expression data obtained from RACIPE.
- Data Normalization: Standardizes the data by subtracting the mean and dividing by the standard deviation(z-score normalization).
- Data Visualization: Creates scatter and regression plots to visualize relationships between various gene expression levels.
- Feature Engineering: Creates a new feature called "metabolic score" and " EMT score" based on existing gene expression levels.
- Further Visualization: Plots the distribution of the metabolic and EMT score and its relationship with other variables.
  
## Results
The generated plots provide insights into the relationship between the metabolic score and gene expressions, as well as the EMT score and the direction of the transition. RACIPE simulations show upregulation of AMPK and inhibition of mTOR can end up in giving more epithelial phenotype.
