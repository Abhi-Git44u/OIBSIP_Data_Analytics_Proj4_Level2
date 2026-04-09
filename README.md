# 📊 Unveiling the Android App Market: Analyzing Google Play Store Data

> **Data Analytics | Project 4 Proposal | Level-2**  
> A comprehensive analysis of the Google Play Store ecosystem using data cleaning, visualization, and sentiment analysis techniques.

---

## 📁 Dataset

| File | Description |
|---|---|
| `Cleand_Data1.csv` | Cleaned app-level data (ratings, installs, category, pricing, etc.) |
| `Cleaned_Data2.csv` | Cleaned user reviews data used for sentiment analysis |

---

## 📌 Project Overview

This project dives deep into the Android app market by leveraging data analytics, visualization, and NLP-based sentiment analysis on Google Play Store data.

### Goals
1. **Data Preparation** — Clean and correct data types for accuracy
2. **Category Exploration** — Investigate app distribution across categories
3. **Metrics Analysis** — Examine app ratings, size, popularity, and pricing trends
4. **Sentiment Analysis** — Assess user sentiments through reviews
5. **Interactive Visualization** — Utilize code for compelling visualizations
6. **Skill Enhancement** — Integrate insights from the "Understanding Data Visualization" course

---

## 📊 Dashboard & Visual Analysis

### 1️⃣ Market Overview — High-Level KPIs

![Market Overview](https://github.com/Abhi-Git44u/OIBSIP_Data_Analytics_Proj4_Level2/blob/56a1662196552fc987cb2553182ed6d7e3c9f3ce/Visuals/dashboard_overview.png)

**Dataset:** 9,659 apps · 64,295 user reviews · 33 categories

| Metric | Value |
|---|---|
| Total Apps | 9,659 (across 33 categories) |
| Average Rating | 4.17 ★ out of 5.0 |
| Free Apps | 92.2% (756 paid) |
| Total Installs | 75.1 Billion |

**Insights:**
- The Play Store is overwhelmingly dominated by free apps at **92.2%**, confirming the freemium model as the industry standard.
- An average rating of **4.17★** suggests that developers generally maintain decent quality, or that the platform's review system skews positive.
- With **75.1 billion total installs**, the Android ecosystem represents a massive, active user base.
- **FAMILY**, **GAME**, and **TOOLS** are the top 3 categories by number of apps — indicating highly competitive spaces with thousands of listings.

---

### 2️⃣ App Distribution by Category (Top 12)

![App Distribution](assets/dashboard_overview.png)

**Insights:**
- **FAMILY** leads with ~1,850 apps — the largest single category, likely because many utility/educational apps get labeled under it.
- **GAME** (~950) and **TOOLS** (~800) follow, showing strong developer interest in entertainment and utility.
- Categories like **FINANCE**, **SPORTS**, and **HEALTH_AND_FITNESS** have fewer apps (~300 each), but may represent high-value niches with monetization potential.
- The steep drop-off after the top 3 categories suggests a **long-tail distribution** in the app market.

---

### 3️⃣ Installs by Category vs. Avg Rating by Category

![Category Analysis](assets/category_analysis.png)

#### 📦 Installs by Category (Top 8)

| Rank | Category | Total Installs |
|---|---|---|
| 1 | GAME | ~14B |
| 2 | COMMUNICATION | ~11B |
| 3 | TOOLS | ~8B |
| 4 | PRODUCTIVITY | ~5B |
| 5 | SOCIAL | ~5B |
| 6 | PHOTOGRAPHY | ~4B |
| 7 | FAMILY | ~4B |
| 8 | VIDEO_PLAYERS | ~3.5B |

**Insights:**
- **GAME** dominates installs at ~14 billion, far outpacing other categories — confirming gaming as the single biggest driver of Play Store traffic.
- **COMMUNICATION** at ~11B reflects the global dependency on messaging apps (WhatsApp, Messenger, etc.).
- Despite **FAMILY** having the most apps, it ranks lower in total installs — indicating high supply but fragmented demand.

#### ⭐ Avg Rating by Category (Top 8)

| Rank | Category | Avg Rating |
|---|---|---|
| 1 | EVENTS | ~4.44 |
| 2 | EDUCATION | ~4.37 |
| 3 | ART_AND_DESIGN | ~4.35 |
| 4 | BOOKS_AND_REF | ~4.33 |
| 5 | PERSONALIZATION | ~4.33 |
| 6 | PARENTING | ~4.30 |
| 7 | BEAUTY | ~4.28 |
| 8 | GAME | ~4.25 |

**Insights:**
- **EVENTS** and **EDUCATION** apps receive the highest average ratings — users tend to give high ratings when an app serves a clear, specific purpose.
- **GAME** appears in both top installs AND top ratings, making it the most dominant and well-received category overall.
- Categories like **TOOLS** and **COMMUNICATION** rank high on installs but don't appear here — suggesting they have high usage but more mixed reviews.

---

### 4️⃣ Free vs. Paid Apps & Rating Distribution

![Free vs Paid](https://github.com/Abhi-Git44u/OIBSIP_Data_Analytics_Proj4_Level2/blob/c91ab523852aef68489c41cbe407936df1011ae9/Visuals/free_vs_paid.png)

#### 💰 Free vs. Paid

| Type | Share | Avg Rating |
|---|---|---|
| Free | 92.2% | 4.17 ★ |
| Paid | 7.8% | 4.26 ★ |

**Insights:**
- Paid apps have a marginally higher average rating (**4.26★** vs **4.17★**) — likely because paid users have higher intent and are more selective before purchasing.
- The **7.8% paid** share still represents 756 apps, a small but potentially high-revenue segment.
- The freemium model clearly dominates — developers monetize through ads and in-app purchases rather than upfront pricing.

#### 📈 Rating Distribution

| Rating | Volume |
|---|---|
| 1★ | Very low |
| 2★ | Low |
| 3★ | Moderate (~700) |
| 4★ | Highest (~5,700) |
| 5★ | High (~1,600) |

**Insights:**
- The distribution is heavily **right-skewed**, with 4★ being the most common rating by far.
- This pattern is typical of app store data — users who bother to rate usually have a positive experience, while dissatisfied users often just uninstall without reviewing.
- Very few apps receive 1★ or 2★ ratings in aggregate, suggesting that poorly received apps likely get removed or abandoned early.

---

### 5️⃣ Top 10 Apps by Review Count

![Top 10 Apps](https://github.com/Abhi-Git44u/OIBSIP_Data_Analytics_Proj4_Level2/blob/44c76692e3797a3739cb35f839b91427a72b8682/Visuals/top10_apps.png)

**Insights:**
- **Facebook** leads review count at 78.2M but has the lowest rating (4.1★) among the top 10 — showing that massive user bases produce more critical feedback.
- **Instagram** achieves a strong balance of high installs (1B+) and solid ratings (4.5★), reflecting strong product-market fit.
- **SOCIAL** and **COMMUNICATION** apps dominate by review volume, while **GAME** apps dominate by rating quality.
- **Clean Master** and **Security Master** (TOOLS) both sport 4.7★ with hundreds of millions of installs — outliers in the tools space.
- The presence of 4 games in the top 10 reinforces gaming's outsized engagement on the platform.

---

### 6️⃣ Sentiment Analysis — 37,432 Classified Reviews

![Sentiment Analysis](https://github.com/Abhi-Git44u/OIBSIP_Data_Analytics_Proj4_Level2/blob/fde3936b4f326423826fe788c460add859b69e42/Visuals/sentiment_analysis.png)

| Sentiment | Count | Percentage | Avg Polarity |
|---|---|---|---|
| Positive | 23,998 | 64.1% | +0.37 |
| Neutral | 5,163 | 13.8% | 0.00 |
| Negative | 8,271 | 22.1% | -0.26 |

**Insights:**
- Nearly **2 in 3 reviews** are positive, reinforcing the overall satisfaction trend seen in high average ratings across the store.
- **22.1% negative** reviews (8,271) is a significant segment — these are critical for developers to monitor as they often surface bugs, UX issues, and unmet expectations.
- The average positive polarity of **+0.37** is moderate, meaning most positive reviews are genuinely enthusiastic rather than mildly pleased.
- The negative polarity of **-0.26** is relatively mild — users are unhappy but not extremely hostile on average.
- The **13.8% neutral** reviews likely come from factual or transactional feedback ("Works as expected", "Does the job").
- For developers, the **1:3 negative-to-positive ratio** is a healthy benchmark — anything worse would signal serious product issues.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core analysis and scripting |
| Pandas | Data cleaning and manipulation |
| Matplotlib / Seaborn | Static visualizations |
| TextBlob / VADER | Sentiment analysis on reviews |
| Plotly / Power BI | Interactive dashboard visualizations |
| Jupyter Notebook | Exploratory data analysis |

---

## 📂 Project Structure

```
google-playstore-analysis/
│
├── data/
│   ├── Cleand_Data1.csv            # App-level cleaned dataset
│   └── Cleaned_Data2.csv           # Reviews cleaned dataset
│
├── assets/                         # Dashboard screenshots for README
│   ├── dashboard_overview.png
│   ├── category_analysis.png
│   ├── free_vs_paid.png
│   ├── top10_apps.png
│   └── sentiment_analysis.png
│
├── notebooks/
│   └── playstore_analysis.ipynb    # Main analysis notebook
│
├── visuals/                         # Exported charts
│
└── README.md
```

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/your-username/google-playstore-analysis.git
cd google-playstore-analysis

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook notebooks/playstore_analysis.ipynb
```

### Requirements
```
pandas
numpy
matplotlib
seaborn
plotly
textblob
nltk
jupyter
```

---

## 🔍 Key Takeaways

1. **Free apps rule** — 92.2% of all apps are free; the freemium model is the dominant monetization strategy.
2. **Gaming is king** — GAME category leads in both total installs (~14B) and engagement (multiple entries in top 10 by reviews).
3. **User sentiment is mostly positive** — 64.1% of reviews are positive with a polarity of +0.37; developers should closely track the 22.1% negative feedback.
4. **High install count ≠ high rating** — Facebook has the most reviews but one of the lower ratings; niche/paid apps tend to score higher.
5. **EVENTS and EDUCATION score highest** in average ratings — users value purpose-built, well-designed apps.
6. **Rating distribution skews right** — 4★ is by far the most common rating, a characteristic bias of app store review systems.

---

## 📜 License

This project is part of a Data Analytics course assignment.  
Dataset sourced from [Kaggle — Google Play Store Apps](https://www.kaggle.com/datasets/lava18/google-play-store-apps).
