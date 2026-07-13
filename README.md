# Customer Segmentation at Spotify

## 📖 Overview
Understanding users is key to delivering a successful and personalized platform experience. By segmenting a vast customer base, this project enables more personalized experiences—ranging from targeted music recommendations to curated playlists—which ultimately increases user engagement and retention.

## 🎯 Project Objectives & Scope
*   **Objective:** Develop a robust Machine Learning model for dynamic customer segmentation.
*   **Scope:** Focus specifically on user behavior data to identify distinct listening patterns.
*   **Business Impact:** Enable targeted marketing, tailored content curation, and data-driven product feature development.

---

## 🏗️ Architecture Flow: From Data to Insights

The project follows a structured five-step machine learning pipeline:

1.  **Exploratory Data Analysis (EDA):** Includes missing value treatment, distribution analysis, and outlier detection.
2.  **Feature Engineering:** Deriving key metrics such as average listening time, skip rate, session length, genre diversity index, and an overall engagement score.
3.  **Data Preprocessing:** Applying scaling and transformation techniques, evaluating Standard, Min-Max, Robust, and Power transforms.
4.  **Model Selection:** Implementing and comparing clustering algorithms, specifically K-Means and Gaussian Mixture Models (GMM).
5.  **Automation & Optimization:** Streamlining the segmentation process to allow for continuous improvement.

### 💻 Implementation Stack
*   **Environment:** Windows (PowerShell) / VS Code
*   **Data Manipulation:** Python, Pandas, NumPy
*   **Exploratory Data Analysis (EDA):** Matplotlib, Seaborn
*   **Machine Learning Modeling:** Scikit-Learn

---

## 📊 Behavioral Dimensions for Segmentation
The segmentation model is built upon five core behavioral metrics:

*   **Frequency:** Daily listening minutes
*   **Intensity:** Sessions per day
*   **Depth:** Average session minutes
*   **Consistency:** Days active over the last 30 days
*   **Friction:** Song skip rate and the percentage of ads skipped

---

## 🏆 Model Evaluation & Best Model
Identifying the optimal clustering solution required rigorous testing using the following metrics:
*   Silhouette Score
*   Elbow Method
*   AIC/BIC (specifically evaluated for the GMM model)

**Final Model Selection:** The K-Means model utilizing Min-Max scaling yielded a Silhouette Score of **0.18**, indicating similarly shaped, distinct user clusters.

---

## 👥 Customer Clusters Profiling
Based on the selected model, the customer base was segmented into four distinct groups:

*   **Cluster 1: Casual Listeners**
    *   Low session depth, medium frequency, and medium consistency.
    *   Medium ads skipped and a high song skip rate.
    *   Low-medium overall listening minutes.
*   **Cluster 2: Intermittent Engagers**
    *   Medium session depth and medium-high frequency.
    *   Low days active, high ads skipped, medium skip song rate, and medium intensity.
*   **Cluster 3: Engaged Loyalists**
    *   High session depth, medium frequency, and high consistency.
    *   High ads skipped, medium-high intensity, and a low song skip rate.
*   **Cluster 4: Power Users**
    *   Highest session depth, low frequency, and high consistency.
    *   Low ads skipped, high intensity, and a low song skip rate.
