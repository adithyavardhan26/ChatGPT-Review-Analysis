# 📊 ChatGPT Review Analysis

## 📌 Project Overview
This project focuses on analyzing real user reviews of ChatGPT to uncover insights into **user satisfaction**, **pain points**, and **sentiment trends over time**.
The goal is to identify what users love, what frustrates them, and what improvements can enhance their experience.

The analysis involves:
- **Sentiment Analysis:** Classifying reviews into Positive, Neutral, and Negative categories.
- **Issue Identification:** Extracting common words from negative reviews to understand recurring issues.
- **Time-Series Analysis:** Tracking sentiment and rating patterns over time.
- **Visual Insights:** Creating clear and actionable visualizations for storytelling and decision-making.

---

## 📂 Dataset Details
The dataset contains reviews with the following fields:

| Column        | Description |
|--------------|-------------|
| **Review Id** | Unique identifier for each review |
| **Review**    | User comment text |
| **Ratings**   | Integer rating (0–5 scale) |
| **Review Date** | Date and time when the review was posted |

---

## 🛠 Project Workflow

### 1️⃣ Data Preparation
- Loaded the dataset using **pandas**
- Handled missing values (filled empty reviews with blank strings)
- Converted `Review Date` to datetime format
- Ensured ratings were numeric

### 2️⃣ Sentiment Analysis
- Used **TextBlob** to compute **polarity** for each review
- Classified reviews into:
  - **Positive** (polarity > 0.1)
  - **Negative** (polarity < -0.1)
  - **Neutral** (otherwise)

### 3️⃣ Issue Identification
- Filtered negative reviews and extracted keywords
- Cleaned text (removed special characters, stopwords)
- Counted word frequencies to identify most common complaints

### 4️⃣ Time-Series Analysis
- Grouped data by `Review Date` and analyzed:
  - **Average Rating Trend**
  - **Positive/Neutral/Negative Sentiment Trends**

### 5️⃣ Visualization
- **Sentiment Distribution Bar Chart** → Shows proportion of Positive, Neutral, Negative reviews
- **Average Rating Over Time (Line Plot)** → Displays user satisfaction trend
- **Sentiment Over Time (Line Plot)** → Tracks sentiment fluctuations daily
- **Top Words in Negative Reviews** → Reveals recurring problems

---

## 💡 Key Insights
✅ **Majority of reviews are positive** → Strong user satisfaction  
✅ **Most common issues:** Speed, login errors, accuracy problems  
✅ **Ratings are stable over time** → Indicates consistent product quality  
✅ **Negative sentiment spikes** on specific dates → Likely due to outages or product changes

---

## 🚀 Tech Stack
- **Python** (pandas, textblob, matplotlib, seaborn, re, collections)
- **Google Colab** for analysis & visualization
