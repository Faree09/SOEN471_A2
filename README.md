# SmartCart Starter Notebook

## Overview

This notebook provides an end-to-end example for building a recommendation system. It consists of four parts:
1. **Data Preprocessing**
2. **User-Based Collaborative Filtering**
3. **Association Rule Mining (Apriori)**
4. **Visualization**

The goal is to preprocess the e-commerce user and product data, generate recommendations based on user similarity, perform association rule mining to uncover product relationships, and visualize key insights.

---

## Table of Contents
- [Prerequisites](#prerequisites)
- [File Structure](#file-structure)
- [Instructions to Run](#instructions-to-run)
- [Dependencies](#dependencies)
- [Part 1: Data Preprocessing](#part-1-data-preprocessing)
- [Part 2: User-Based Collaborative Filtering](#part-2-user-based-collaborative-filtering)
- [Part 3: Association Rule Mining (Apriori)](#part-3-association-rule-mining-apriori)
- [Part 4: Visualization](#part-4-visualization)
- [Outputs](#outputs)

---

## Prerequisites

Before running the notebook, ensure you have the following:

- Python 3.x
- Jupyter Notebook or JupyterLab for running the notebook

### Files Required

- `ecommerce_user_data.csv` - Contains user interaction data with products.
- `product_details.csv` - Contains product details for each item.
- Notebook file (typically named `smartcart_starter_detailed.ipynb`).

---

## File Structure
SmartCart/
│
│── ecommerce_user_data.csv       # User interaction data
│── product_details.csv           # Product details data
│── Report_Part_5.pdf              # Answer to part 5
├── smartcart_starter_detailed.ipynb  # The Jupyter notebook with the steps outlined below
└── README.md                        # This file

## Instructions to Run

pandas
numpy
scikit-learn
mlxtend
matplotlib
seaborn
jupyter

## Part 1: Data Preprocessing

In this section, we load the datasets and preprocess them:

1. **Load** `ecommerce_user_data.csv` and `product_details.csv`.
2. **Merge** the data if necessary (based on common identifiers).
3. **Create** a user-item matrix based on the user-product interactions.
4. **Fill missing ratings** with 0 to account for items the user hasn't rated.
5. **Group user behavior by category** to organize the data into meaningful segments.

---

## Part 2: User-Based Collaborative Filtering

1. **Cosine Similarity** is used to compute the similarity between users based on their interactions with products.
2. **Top-N product recommendations** are generated based on users who are most similar to the target user.
3. The model is evaluated using:
   - **Precision@K**: Measures the relevance of the top-N recommendations.
   - **Coverage**: Measures the proportion of products covered in the recommendations.

---

## Part 3: Association Rule Mining (Apriori)

1. Convert the **user-product interactions** into a transaction format suitable for association rule mining.
2. Apply the **Apriori algorithm** to find frequent itemsets from the transaction data.
3. **Generate association rules** with metrics:
   - **Support**: Frequency of the itemset in the data.
   - **Confidence**: Likelihood of purchasing a product given the presence of another product.
   - **Lift**: Indicates the strength of a rule over random chance.

---

## Part 4: Visualization

In this section, we create various visualizations to help interpret the results:

1. **User similarity heatmap** - Visualize the similarity between users based on cosine similarity.
2. **Top frequent itemsets** - Visualize the most frequently bought-together products.
3. **Top recommendations** - Visualize the most recommended products for the target user.


## Outputs

After running the notebook, the following outputs will be generated:

### Data Preprocessing Output:
- Merged user-product dataset.
- Preprocessed user-item matrix.

### Collaborative Filtering:
- A list of top-N recommended products for a sample user.
- Precision@K and coverage values to evaluate recommendation quality.

### Association Rule Mining:
- A list of frequent itemsets.
- Association rules with their support, confidence, and lift values.

### Visualizations:
- Heatmap of user similarity.
- Plots of frequent itemsets and top product recommendations.
