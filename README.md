# Pediatric_Brain_Cancer_Classification
## Introduction

This repository integrates cutting-edge generative AI capabilities, leveraging OpenAI's GPT-3.5 model, with bioinformatics analyses focused on pediatric brain cancer research. The analyses are based on the Pediatric Brain Cancer study published in Cell in 2020.

## Data Description

The data used in this analysis is sourced from cBioportal and is derived from the Pediatric Brain Cancer study. Here are the details:

- Source: cBioportal
- Sample size: 218
- Classes: medulloblastoma, ganglioglioma, low grade glioma, ependymoma, high grade glioma, craniopharyngioma, and atypical teratoid rhabdoid tumor.
- Purpose: Samples are selected from the MBL and GNG classes, focusing on 2000 genes for demonstration purposes.

Notes:
- Medulloblastoma (MBL): The most common malignant brain tumor in pediatric patients, comprising 15% of all pediatric CNS tumors. It arises from the cerebellum.
- Gangliogliomas (GBL): Benign tumors of the CNS that can occur anywhere in the CNS, most commonly found in the temporal lobe.

## Objectives

The primary objective of this analysis is to identify genes with the potential to discriminate between MBL and GNG classes.

## Analyses

1. Differential Expression Analysis:
   - Utilize generative AI functions to identify differentially expressed genes using t-tests between the MBL and GNG classes, assuming normalized data.
   - Implement functions to conduct t-tests and calculate log fold changes for each gene, returning results as dataframes.

2. Principal Component Analysis (PCA):
   - Conduct PCA with differentially expressed genes.
   - Visualize PC1 and PC2, coloring samples based on the categorical variable using Seaborn.

3. Enrichment Analysis:
   - Perform enrichment analysis to identify pathways enriched by differentially expressed genes.
   - Implement enrichment analysis using the gseapy package.

4. Machine Learning Classifier:
   - Build a machine learning-based classifier using genes obtained from differential expression.
   - Utilize logistic regression for binary classification of MBL and GNG.
   - Split data into 70% training and 30% test sets.
   - Evaluate classifier performance metrics including accuracy, AUROC, precision, recall, and plot the ROC curve.
