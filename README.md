# MovieLens 1M Data Mining & Recommendation System

[![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0+-green.svg)](https://pandas.pydata.org/)
[![Plotly](https://img.shields.io/badge/Plotly-Interactive-red.svg)](https://plotly.com/)
[![mlxtend](https://img.shields.io/badge/mlxtend-FP--Growth-purple.svg)](https://rasbt.github.io/mlxtend/)
[![License](https://img.shields.io/badge/License-MovieLens-yellow.svg)](https://grouplens.org/)

> Data mining course assignment analyzing the MovieLens 1M dataset with EDA, Association Rule Mining (Apriori/FP-Growth), and future implementations of Collaborative Filtering & Content-Based Filtering.

## 📊 Dataset Overview

| Metric | Value |
|--------|-------|
| Total Ratings | 1,000,209 |
| Unique Users | 6,040 |
| Unique Movies | 3,883 |
| Genres | 18 |
| Time Range | Apr 2000 - Feb 2003 |

**Source:** [MovieLens 1M Dataset](https://grouplens.org/datasets/movielens/1m/) by GroupLens Research

---

## 🗂️ Project Structure

```
.
├── README.md                    # This file
├── requirements.txt             # Python dependencies
├── movielens_analysis.ipynb     # Main analysis notebook
├── ml-1m/                      # Dataset directory
│   ├── ratings.dat
│   ├── users.dat
│   ├── movies.dat
│   └── README
└── .venv/                      # Virtual environment
```

---

## 🚀 Quick Start

### 1. Setup

```bash
# Navigate to project directory
cd /path/to/project

# Create virtual environment
python3 -m venv .venv

# Activate virtual environment
source .venv/bin/activate  # macOS/Linux
# .venv\Scripts\activate   # Windows

# Install dependencies
pip install -r requirements.txt
```

### 2. Run the Notebook

```bash
# Start Jupyter Lab
jupyter lab movielens_analysis.ipynb

# Or use Jupyter Notebook
jupyter notebook movielens_analysis.ipynb
```

---

## 📈 Features Implemented

### ✅ Completed

| Feature | Description |
|---------|-------------|
| **Data Preprocessing** | Load, clean, and merge MovieLens 1M datasets |
| **EDA** | Rating distribution, user demographics, genre analysis |
| **Apriori/FP-Growth** | Association rule mining for genre patterns |
| **Movie-Based Rules** | Genre co-occurrence in movies (lift ~4.5) |
| **User-Based Rules** | User preference patterns (for comparison) |
| **Genre Recommender** | Simple content-based genre recommendation |

### 🔄 In Progress / Planned

| Feature | Status |
|---------|--------|
| **Collaborative Filtering** | User-based & Item-based CF |
| **Content-Based Filtering** | Genre & metadata-based recommendations |
| **Hybrid Recommender** | Combine CF + Content-Based |
| **Model Evaluation** | RMSE, Precision@K, Recall@K |

---

## 📊 Key Findings

### Association Rules Results

| Approach | Avg Lift | Interpretation |
|----------|----------|----------------|
| User-Based | ~1.0 | Trivial rules (base rates) |
| **Movie-Based** | **~4.5** | **Strong genre associations** |

### Top Genre Association Rules

```
Animation          → Children's      (lift: 6.2)
Adventure + Fantasy → Action         (lift: 4.1)  
Romance            → Drama            (lift: 3.8)
Crime + Drama      → Thriller         (lift: 3.2)
Action + Adventure → Thriller        (lift: 2.9)
```

### EDA Insights

- **Rating Distribution:** 52% are 4-5 stars (positive skew)
- **User Demographics:** 71% male, 25-34 largest age group
- **Top Genres:** Drama (55%), Comedy (35%), Action (24%)
- **Highest Rated:** Film-Noir, Documentary (niche appeal)

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python 3.11+ |
| Data Processing | pandas, numpy |
| Visualization | Plotly, Seaborn |
| Mining | mlxtend (FP-Growth, Apriori) |
| Development | Jupyter Notebook |

---

## 📖 Documentation

- **[movielens_analysis.ipynb](movielens_analysis.ipynb)** - Main analysis notebook with:
  - Data loading & preprocessing
  - Exploratory Data Analysis
  - User-Based vs Movie-Based Apriori comparison
  - Genre recommendation system

---

## 📝 Assignment Requirements

This project fulfills the following course requirements:

- [x] Data preprocessing & cleaning
- [x] Exploratory Data Analysis (EDA)
- [x] Data mining algorithm implementation
- [ ] Collaborative Filtering *(planned)*
- [ ] Content-Based Filtering *(planned)*
- [x] Visualization of results
- [x] Decision making & conclusions

---

## 📜 License

This dataset is provided by [GroupLens Research](https://grouplens.org/) under their usage terms. See `ml-1m/README` for details.

This project is for educational purposes as part of the Data Mining course assignment.

---

## 👥 Contributors

| Role | Description |
|------|-------------|
| Data Mining Course | Assignment |
| Dataset | MovieLens 1M by GroupLens |

---

## 🔗 References

1. [MovieLens Dataset](https://grouplens.org/datasets/movielens/1m)
2. [Harper, F. M., & Konstan, J. A. (2015)](https://dl.acm.org/doi/10.1145/2827872) - The MovieLens Datasets: History and Context
3. [FP-Growth Algorithm](https://rasbt.github.io/mlxtend/api_reference/frequent_patterns/mlxtend.frequent_patterns.fpgrowth/)
4. [Association Rules](https://rasbt.github.io/mlxtend/api_reference/frequent_patterns/mlxtend.frequent_patterns.association_rules/)

---

*Last Updated: March 2026*
