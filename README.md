# Movie_Correlation_Project
# 🎬 Movie Correlation Analysis

Exploratory data analysis project that uncovers hidden correlations between movie attributes — budget, gross revenue, ratings, votes, and more — using the Kaggle Movies Dataset.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?style=flat-square&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-1.24-013243?style=flat-square&logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7-11557c?style=flat-square)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12-4c72b0?style=flat-square)

---

## 📌 Project Overview

This project analyzes a dataset of thousands of movies to answer questions like:

- Does a higher budget lead to higher gross revenue?
- Which numeric features correlate most strongly with a movie's success?
- Are there patterns across genres, companies, or release years?

The analysis relies on **correlation matrices**, **regression plots**, and **heatmaps** to make relationships visually interpretable.

---

## 📁 Project Structure

```
movie-correlation/
│
├── data/
│   └── movies.csv               # Kaggle Movies Dataset
│
├── notebooks/
│   └── movie_correlation.ipynb  # Main analysis notebook
│
├── plots/
│   ├── correlation_heatmap.png
│   ├── budget_vs_gross.png
│   └── top_correlations.png
│
├── movie_correlation.py         # Standalone Python script
├── requirements.txt
└── README.md
```

---

## 📊 Dataset

**Source:** [Kaggle — Movies Dataset](https://www.kaggle.com/datasets/danielgrijalvas/movies)

**Key columns used:**

| Column      | Description                          |
|-------------|--------------------------------------|
| `name`      | Movie title                          |
| `rating`    | MPAA rating (G, PG, R, etc.)         |
| `genre`     | Primary genre                        |
| `year`      | Release year                         |
| `released`  | Full release date                    |
| `score`     | IMDb user score                      |
| `votes`     | Number of IMDb votes                 |
| `director`  | Director name                        |
| `writer`    | Writer name                          |
| `star`      | Lead actor/actress                   |
| `country`   | Country of production                |
| `budget`    | Production budget (USD)              |
| `gross`     | Worldwide gross revenue (USD)        |
| `company`   | Production company                   |
| `runtime`   | Runtime in minutes                   |

---

## 🔍 Key Findings

- **Budget vs. Gross** has one of the strongest positive correlations (~0.74), confirming that higher-budget films tend to earn more.
- **Votes vs. Gross** is also strongly correlated — popular films generate more box-office revenue.
- **IMDb Score** shows only a moderate correlation with gross, suggesting critical acclaim alone doesn't drive revenue.
- **Runtime** has a weak but positive relationship with both score and votes.

---

## 📈 Visualizations

### Correlation Heatmap
A full numeric correlation matrix across all quantitative features — rendered with Seaborn's `heatmap()` with annotations.

### Budget vs. Gross (Regression Plot)
A scatter plot with a linear regression line showing the relationship between production budget and worldwide gross revenue.

### Top Correlations Bar Chart
Ranked bar chart of the features most correlated with gross revenue.

---

## 🛠️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/movie-correlation.git
cd movie-correlation
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the dataset

Download `movies.csv` from [Kaggle](https://www.kaggle.com/datasets/danielgrijalvas/movies) and place it in the `data/` folder.

---

## ▶️ Usage

### Run as a Python script

```bash
python movie_correlation.py
```

### Or open the Jupyter notebook

```bash
jupyter notebook notebooks/movie_correlation.ipynb
```

---

## 📦 Requirements

```
pandas>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
seaborn>=0.12.0
jupyter>=1.0.0
```

Install all at once:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

---

## 🧠 Analysis Workflow

```
1. Load & inspect the dataset (shape, dtypes, head)
        ↓
2. Handle missing values (drop or impute)
        ↓
3. Feature engineering (extract year from release date)
        ↓
4. Encode categorical columns numerically for correlation
        ↓
5. Compute Pearson correlation matrix
        ↓
6. Visualize: heatmap, scatter plots, bar charts
        ↓
7. Interpret and summarize findings
```

