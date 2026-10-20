---
title: Consumer Complaint Analytics
summary: An NLP pipeline over the 8+ GB CFPB Consumer Complaint Database that classifies complaints and separates templated filing volume from genuine consumer harm.
date: 2026-07-10
featured: true
links:
  - type: code
    url: https://github.com/porushy/Consumer-Complaint-Analytics
    label: Code
    icon: brands/github
tags:
  - NLP
  - Machine Learning
  - Text Classification
  - Statistical Analysis
---

Jul 2026

Python · pandas · Dask · scikit-learn · Parquet · Streamlit

- Engineered a memory-safe data pipeline using Dask and Parquet to stream and process the 8.8 GB (15.2M+ rows) CFPB database without exceeding RAM limits.
- Trained an NLP text classifier using TF-IDF and Logistic Regression on 3.3M narratives, achieving 87.0% accuracy on a de-duplicated test set against a 60.6% naive baseline.
- Applied chi-square tests and Cramér's V effect-size statistics to uncover a surge in templated "dispute-mill" filings (rising to 77%); deployed insights via an interactive Streamlit dashboard.

<!--more-->
