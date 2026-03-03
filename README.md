# Wine Segmentation Using Unsupervised Learning  
## Discovering Structure in Chemical Composition Data

---

# Overview

In many real-world business environments, data exists without labels.

There is no predefined “segment,” no category column, and no ground truth — yet decisions must still be made.

This project explores how **unsupervised machine learning** can reveal natural structure in wine data using only chemical composition features.

Using **K-Means clustering**, validation via the **Elbow Method**, and dimensionality reduction with **t-SNE**, the analysis identifies **three distinct clusters** — demonstrating how structure can emerge from unlabeled data.

While this dataset focuses on wine chemistry, the methodology directly applies to:

- Customer segmentation  
- Risk grouping  
- Product differentiation  
- Behavioral clustering  
- Operational anomaly detection  

The objective was not prediction — but discovery.

---

# Business Framing

Imagine this scenario:

A wine producer has hundreds of product variants and lab measurements but no defined product segments.

They need to:

- Identify natural product groupings  
- Support differentiated pricing strategies  
- Optimize marketing positioning  
- Detect unusual production batches  

Without predefined categories, clustering becomes a powerful tool for insight generation.

This project mirrors that workflow.

---

# Dataset Description

Each wine sample contains numerical chemical measurements, including:

- Alcohol  
- Flavonoids  
- Total Phenols  
- Proanthocyanidins  
- Color Intensity  
- Hue  
- Proline  
- Ash  
- Ash Alkalinity  
- OD280  

All features are continuous and numeric.

No label or target variable was used during clustering.

---

# Analytical Approach

## Feature Selection

From the full dataset, 10 chemically relevant features were selected for clustering.

The focus was on attributes most likely to contribute to meaningful differentiation.

---

## Determining the Number of Clusters

Rather than arbitrarily choosing the number of clusters, the **Elbow Method** was used.

K-Means was trained across cluster sizes from 1 to 21, tracking:

- Within-Cluster Sum of Squares (WCSS)

A clear inflection point appeared at:

> **k = 3**

This indicates diminishing returns in variance reduction beyond three clusters.

---

## Model Implementation

**Algorithm used:**

- K-Means clustering  
- Initialization: `k-means++`  
- Cluster count: 3  

Each wine sample was assigned a cluster label based on chemical similarity.

This step reveals structure without supervision.

---

## Visualization via Dimensionality Reduction

Clustering operates in high-dimensional space (10 features).

To interpret results visually, **t-SNE** was applied using:

- 1D projection  
- 2D projection  
- 3D projection  

The 2D and 3D projections show clear separation between clusters, reinforcing that the segmentation reflects meaningful structure rather than noise.

---

## Cluster Interpretation - Technical

After clustering, feature distributions were analyzed per cluster.

Distinct patterns emerged:

- One cluster exhibited higher alcohol and flavonoid concentration.  
- Another showed stronger color intensity characteristics.  
- A third reflected lower phenolic content overall.  

This confirms that clusters align with chemical differentiation, not random assignment.

---

## Cluster Interpretation - Non Technical

### Cluster 1 — Rich & Intense Profile

Wines in this group show stronger structural characteristics.

They tend to have:

- Higher alcohol concentration  
- More pronounced flavor compounds  
- Fuller overall composition  

From a business perspective, these wines may represent:

- Premium-tier products  
- Bold flavor profiles  
- Stronger market positioning  

---

### Cluster 2 — Balanced & Vibrant Profile

This group is characterized by higher visual intensity and distinctive balance across features.

These wines may represent:

- Visually appealing products  
- Distinct but not overpowering profiles  
- Potential mid-range positioning  

They stand out without being extreme.

---

### Cluster 3 — Lighter & Subtle Profile

This cluster reflects wines with generally lower intensity across several characteristics.

They may correspond to:

- Lighter-bodied products  
- More subtle flavor experiences  
- Entry-level or easy-drinking options  

---

# What This Means

Even without labels, the algorithm identified three clearly differentiated wine profiles:

- Strong & bold  
- Balanced & vibrant  
- Light & subtle  

This demonstrates how unsupervised learning can uncover natural product segmentation without prior classification.

In a real business setting, this insight could support:

- Pricing strategy  
- Inventory grouping  
- Marketing campaigns  
- Product positioning  
- Portfolio rationalization  

---

### Key Takeaway

The data already contained structure — clustering simply revealed it.

# Key Results

- **Optimal cluster count:** 3  
- **Method:** K-Means  
- **Validation:** Elbow Method  
- **Visualization:** t-SNE projections  
- **Outcome:** Clear, interpretable segmentation  

---

# Technical Considerations

## Why K-Means?

- Efficient and scalable  
- Interpretable centroids  
- Industry-standard baseline for segmentation  

## Why Elbow Method?

- Prevents arbitrary model selection  
- Provides data-driven justification  

## Why t-SNE?

- Enables visualization of nonlinear high-dimensional structure  
- Helps validate cluster separation visually  

---

# Industry Relevance

This project demonstrates the ability to:

- Extract insight from unlabeled datasets  
- Apply validation methodology appropriately  
- Translate technical output into business meaning  
- Structure an end-to-end unsupervised workflow  

The same framework can scale to:

- Retail customer segmentation  
- Banking fraud grouping  
- Healthcare patient clustering  
- Manufacturing quality control  

---
