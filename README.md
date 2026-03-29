# 📊 YouTube Channel Growth Analysis — [HealthieRecipes24](https://www.youtube.com/@HealthieRecipies24)


## Project Overview
This project analyzes my own YouTube channel **HealthieRecipes24** using real data exported from YouTube Studio API. The goal was to identify what was stopping the channel from growing and use data to make smarter content decisions.

**Tools Used:** Python, Pandas, Matplotlib, Seaborn, WordCloud, Tableau  
**Dataset:** 460 videos | 16 metrics | Lifetime data (Dec 2023 – Jan 2026)

---

## Business Problem
Despite accumulating **6.3 million total views**, the channel had only **4,789 subscribers** — a conversion rate of 0.06%, which is 20x below the industry benchmark of 1-3%. The question was: **why are people watching but not subscribing?**

---

## What I Did

### 1. Data Collection
- Exported analytics data directly from YouTube Studio Advanced Mode
- Selected 16 key metrics including views, CTR, watch time, subscribers gained/lost, likes, comments, and impressions

### 2. Data Cleaning (Python + Pandas)
- Removed the aggregated "Total" row that would have skewed analysis
- Renamed 16 columns to clean, Python-friendly names
- Converted `publish_date` from string to datetime format
- Converted `avg_view_duration` from "hh:mm:ss" text to numeric seconds
- Dropped `unique_viewers` column (460/460 values missing)
- Created derived metrics: `conversion_rate`, `engagement_rate`

### 3. Analysis & Insights

#### 📌 Insight 1 — The Conversion Problem
The Appam video drove **2,876,998 views** but converted only **0.06%** to subscribers.
Out of every 1,000 viewers, only 1 person subscribed. Industry standard is 1–3%.

#### 📌 Insight 2 — CTR is Strong, But Distribution is Weak
Top 10 videos by CTR averaged **9%+** — nearly double the industry benchmark of 2–5%.
However, CTR showed only **0.14 correlation** with views, meaning YouTube wasn't distributing impressions to high-CTR videos.

#### 📌 Insight 3 — One Viral Moment, No Consistent Growth
**96% of total views came from just 2 months** (Sep–Oct 2024), driven by one viral Short.
Before and after this period, the channel flatlined — indicating no sustainable content strategy.

#### 📌 Insight 4 — Mixed Content Identity
Word frequency analysis of all 460 video titles revealed a mix of food recipes, celebrity content, and random topics. This unclear brand identity reduced subscriber loyalty — viewers didn't know what to consistently expect from the channel.

#### 📌 Insight 5 — Small Videos, Hidden Engagement
Gym Coach Nitesh video (12,512 views) achieved **6.11% engagement rate** — 3x higher than the viral Appam video (1.75%). Niche, focused content drives stronger audience connection.

#### 📌 Insight 6 — Correlation Analysis (The Most Important Finding)
A full correlation heatmap revealed:
- Views, likes, watch time, and subscribers gained correlate strongly (**0.93–1.0**) — they all move together
- CTR has near-zero correlation with views (**0.14**) — high CTR alone doesn't drive growth
- Engagement rate shows **negative correlation (-0.04)** with subscribers gained — people engage with small videos but don't convert
- Conversion rate has **zero correlation (-0.025)** with views — more views does not mean more subscribers

---

## Changes I Made to the Channel
Based on these findings, I made the following strategic changes:

✅ **Shifted to food-focused content** — eliminated celebrity focused content and random videos that diluted the channel identity  
✅ **Improved titles and thumbnails** — focused on searchable, benefit-driven titles like "Benefits of eating certain heathy food"  
✅ **Reduced Shorts dependency** — began planning longer-form recipe content to improve subscriber conversion  

---

## Visualizations
| Chart | Insight |
|---|---|
| Horizontal Bar — Top 10 by Views | Appam dominates at 2.8M |
| Line Chart — Views Over Time | Spike in Sep-Oct 2024, flat otherwise |
| Bar Chart — Top 10 by CTR | Strong CTR averaging 9% |
| Word Cloud — Title Analysis | Shorts + food dominant, mixed identity |
| Bar Chart — Engagement Rate | Small videos outperform viral ones |
| Correlation Heatmap | Views ≠ Subscribers |

---

## Key Takeaway
> High views without a clear content strategy does not build a sustainable YouTube channel.<br> Data showed that the channel needed a focused food identity, consistent posting,<br> and content designed to convert viewers into subscribers — not just attract clicks.

---

## Files in This Repository
- `youtube_channel_analysis.ipynb` — Full Python analysis notebook
- `healthie_recipes_clean.csv` — Cleaned dataset
- `healthie_recipes_final.csv` — Final export for Tableau
- `/charts` — All saved visualizations

---

*This project was built as part of my data analytics portfolio to demonstrate real-world analysis using personal data.*
