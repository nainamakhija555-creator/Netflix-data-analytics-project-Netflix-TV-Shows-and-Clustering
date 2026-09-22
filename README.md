# Netflix Movies and TV Shows Clustering

An unsupervised machine learning project focused on analyzing, visualising, and clustering Netflix's dataset of movies and TV shows. The dataset originates from Flixable (a third-party Netflix search engine) and reflects titles available on the platform as of 2019.

---

## Project Overview

The goal of this project is to perform Exploratory Data Analysis (EDA) on Netflix's library and build text-based clustering models using unsupervised learning. By engineering features from metadata such as descriptions, cast, directors, and genres, the model groups similar movies and TV shows together to derive actionable content insights.

### Key Objectives
* Conduct exploratory data analysis to discover trends across release years, durations, and ratings.
* Examine content distribution across different geographical regions.
* Evaluate historical trends to answer whether Netflix has shifted focus toward TV shows over movies.
* Preprocess textual attributes and apply clustering algorithms to group similar content together.

---

## Dataset Summary

* **Total Records:** 7,787
* **Total Features:** 12
* **Data Types:** 1 Numerical, 11 Text/Categorical

### Attributes
| Column | Description |
| :--- | :--- |
| `show_id` | Unique identifier for each title |
| `type` | Content category (`Movie` or `TV Show`) |
| `title` | Title of the movie or TV show |
| `director` | Director(s) involved |
| `cast` | Primary actors involved |
| `country` | Country/countries of production |
| `date_added` | Date the content was added to Netflix |
| `release_year` | Original release year |
| `rating` | TV/Film age rating |
| `duration` | Runtime in minutes or number of seasons |
| `listed_in` | Associated genres |
| `description` | Short plot summary |

---

## Project Workflow

1. **Data Cleaning & Feature Engineering**
   * Handled missing values across `director`, `cast`, `country`, `date_added`, and `rating`.
   * Converted `date_added` to datetime format and extracted `year_added`.
   * Standardized string values (e.g., stripping whitespace from country names).

2. **Exploratory Data Analysis (EDA)**
   * Visualized top actors and directors with the highest content count (e.g., Anupam Kher, Takahiro Sakurai, Shah Rukh Khan).
   * Tracked content expansion trends over time to analyze changes in streaming catalog composition.
   * Explored country-specific preferences and genre distributions using Plotly and Seaborn.

3. **Text Preprocessing & NLP**
   * Tokenized, cleaned, and removed stopwords from text fields.
   * Applied stemming/lemmatization using NLTK.
   * Converted processed text into numerical feature vectors using `TfidfVectorizer`.

4. **Dimensionality Reduction & Clustering**
   * Applied Principal Component Analysis (PCA) to reduce feature space dimensionality.
   * Implemented **K-Means Clustering** and evaluated performance using the Silhouette Score.
   * Built **Agglomerative Hierarchical Clustering** and generated dendrograms for cluster hierarchy inspection.

---

## Technologies Used

* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn, Plotly, Missingno, WordCloud
* **NLP:** NLTK, Scikit-learn (TF-IDF Vectorizer)
* **Machine Learning:** Scikit-learn (KMeans, PCA, Silhouette Score, Agglomerative Clustering), SciPy

---
