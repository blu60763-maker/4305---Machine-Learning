## Overview
This repository contains coursework and project deliverables for **ITEC 4305: Web Mining**. The project establishes an end-to-end data science and machine learning pipeline that builds a fair-value rental pricing framework using the UCI *Apartment for Rent Classified* dataset. Beyond standard price regression, the framework acts as a practical decision-support tool by standardizing rents and classifying listings into actionable market valuation bands ("Deal", "Fair", and "Premium") based on model residuals.

The goal of this project is to build a fair-value rental pricing framework using the Apartment
for Rent Classified dataset. The project first standardizes listing prices to a monthly basis,
then uses cleaned and transformed listing information to estimate the expected monthly rent
of each unit. Based on the difference between the actual listed price and model-predicted
price, the system further classifies listings into practical pricing bands such as Deal, Fair, and
Premium. This allows the output to be interpreted not only as a prediction task, but also as a
decision-support tool.

---

## Core Project Work & Deliverables

* **`Amenity.ipynb`**  
  Primary source notebook containing the full implementation of the NLP keyword extraction, text preprocessing, feature engineering pipelines, model training workflows, and evaluation analysis.

* **`Interim Report.pdf` & `Final Report`**  
  Comprehensive project documentation detailing business context, data cleaning, exploratory data analysis, and ablation experiments across multiple regression models.

* **NLP Amenity Mining & Categorical Market Engineering**  
  * Implemented regular expressions and synonym mapping across unstructured listing descriptions, recovering over 56,000 missing amenity tags and significantly reducing feature sparsity.
  * Engineered a two-tier hybrid market aggregation strategy that consolidated thousands of sparse raw cities into stable market categories, preventing tree overfitting on rare geographic keys.
  * Tuned an **XGBoost Regressor** that significantly outperformed the baseline model, increasing R^2 from 0.5223 to 0.7875 and reducing MAPE from 22.12\% down to 13.75\% by effectively capturing non-linear interactions between granular amenities and localized markets.

* **Geospatial Intelligence & Clustering**  
  * Combined continuous coordinates (latitude and longitude) with state-level administrative markers using spatial K-Means clustering (k=30) to act as localized neighborhood market proxies.
  * Evaluated non-linear spatial effects using **Random Forest** and **Ridge Regression**, achieving peak performance when combining regional boundaries with localized spatial cluster features.

* **Decision-Support Valuation Framework**  
  * Converted residual error margins into transparent pricing bands: **Good Deal** (underpriced/high value for renters), **Fair Market Price**, and **Overpriced** (above market/vacancy risk for landlords).

---

Overall, this project is designed as an end-to-end data science pipeline that connects data
understanding, preprocessing, exploratory analysis, modeling, and interpretation. Rather than
focusing only on model accuracy, the project emphasizes decision value: whether the
resulting system can provide stakeholders with a more consistent and evidence-based way to
evaluate rental prices.

## Data

This project uses the *Apartment for Rent Classified* dataset from the UCI Machine Learning Repository.

- `apartments_for_rent_classified_10K.csv`  
  A smaller subset used for development, debugging, and demonstration purposes.  
  This file is included in the repository.

- `apartments_for_rent_classified_100K.csv`  
  The full dataset (~100,000 listings) used for final analysis.  
  Due to file size limitations, this file is **not included** in the repository.

### How to obtain the full dataset

Download the full dataset from:
https://archive.ics.uci.edu/dataset/555/apartment+for+rent+classified

After downloading, place the file in folder: data
