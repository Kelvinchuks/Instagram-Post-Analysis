# 📊 Instagram Post Analysis – Instafocus Project

## 🔍 Overview
This project presents a secondary data analysis of Instagram posts, focusing on **geographic targeting** and **sentiment analysis** to understand engagement patterns. The dataset was initially cleaned using **PowerQuery and Excel**, and further processed and analyzed in Python.

## 🧹 Data Cleaning
- Handled missing values in `comment` and `description` fields.
- Renamed the `description` column to `post_description` for clarity.
- Filtered dataset to focus on posts from:
  - **United States**
  - Select **European countries** (e.g., Italy, France, Ireland, etc.)

## 📈 Top Performing Posts by Engagement
- Engagement score was derived from likes and comments.
- Top 10 posts were analyzed based on `engagement_score_view`.

**🔑 Insight:**  
Posts with emotional tone, hashtags, user mentions, and calls-to-action had higher engagement.

## 🌍 Geo-Targeted Engagement

Average engagement by country (Top 5):
1. 🇮🇹 Italy – 8681.5  
2. 🇫🇷 France – 6706.0  
3. 🇮🇪 Ireland – 5949.0  
4. 🇺🇸 United States – 4989.5  
5. 🇵🇱 Poland – moderate  

**📌 Insight:**  
Geo-targeted strategies can be refined based on country-wise engagement. Italy, France, and Ireland show particularly strong response.

## 🧠 Sentiment Analysis

**Tool Used**: `VADER` (Valence Aware Dictionary and sEntiment Reasoner)

### Scoring Breakdown
| Sentiment Type | VADER Compound Score     |
|----------------|--------------------------|
| Negative       | `< -0.1`                 |
| Neutral        | `-0.1 ≤ score ≤ 0.1`     |
| Positive       | `> 0.1`                  |

Sentiment was calculated for:
- `post_description`
- `comment`

### Sample Categorization:
| Text Example                                | Compound Score | Sentiment |
|--------------------------------------------|----------------|-----------|
| "Absolutely loved the experience, thank you!" | 0.85           | Positive  |
| "The event was okay, nothing too special."   | 0.05           | Neutral   |
| "This is the worst day ever!"                | -0.75          | Negative  |

## 📊 Sentiment vs Engagement

| Sentiment        | Avg. Engagement Score |
|------------------|-----------------------|
| Positive         | Highest               |
| Neutral          | Moderate              |
| Negative         | Lowest                |

**📌 Insight:**  
Positive sentiment in post descriptions is correlated with better audience engagement.

## 📉 Visualizations
- **Bar Chart**: Average engagement by country

## 🧾 Conclusion
This analysis provides strategic insights into how **geographic focus** and **emotional tone** influence Instagram engagement. These findings can inform content strategies, scheduling, and targeted advertising.

## 🛠 Tools & Libraries
- Python (Pandas, Seaborn, NLTK)
- Excel / PowerQuery
- VADER Sentiment Analysis
