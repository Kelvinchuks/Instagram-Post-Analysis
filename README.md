# Instagram Post Analysis – Instafocus Project

## Overview
This project presents a secondary data analysis of Instagram posts, focusing on **geographic targeting** and **sentiment analysis** to understand the social well-being of individuals based on engagement patterns. The dataset was initially cleaned using **PowerQuery and Excel**, and further processed and analyzed in Python.

## Data Cleaning
- Handled missing values in `comment` and `description` fields.
- Renamed the `description` column to `post_description` for clarity.
- Filtered dataset to focus on posts from:
  - **United States**
  - Select **European countries** (e.g., Italy, France, Ireland, etc.)

## Top Performing Posts by Engagement
- Engagement score was derived from likes and comments.
- Top 10 posts were analyzed based on `engagement_score_view`.

** Insight:**  
Posts with emotional tone, hashtags, user mentions, and calls-to-action had higher engagement.

## Geo-Targeted Engagement

Average engagement by country (Top 5):
1. Italy – 8681.5  
2. France – 6706.0  
3. Ireland – 5949.0  
4. United States – 4989.5  
5. Poland – moderate  

** Insight:**  
Geo-targeted strategies can be refined based on country-wise engagement. Italy, France, and Ireland show particularly strong response.

## Sentiment Analysis

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

## Sentiment vs Engagement

| Sentiment        | Avg. Engagement Score |
|------------------|-----------------------|
| Negative          | Highest               |
| Neutral          | Moderate              |
| Positive         | Lowest                |

** Insight:**  
Instagram users tend to engage more with posts reflecting negative sentiment than neutral or positive ones. This tendency could have implications for social well-being and mental health, as frequent exposure to or engagement with negative content may reinforce negative emotions, create a skewed perception of reality, and contribute to stress or anxiety. Conversely, depending on the context of the engagement, it may also provide a platform for expressing and addressing difficult emotions.

## Visualizations
- **Bar Chart**: Average engagement by country

## Conclusion
This analysis provides strategic insights into how **geographic focus** and **emotional tone** influence Instagram engagement. These findings can inform content strategies, scheduling, and targeted advertising.

## Tools & Libraries
- Python (Pandas, Seaborn, NLTK)
- Excel / PowerQuery
- VADER Sentiment Analysis
