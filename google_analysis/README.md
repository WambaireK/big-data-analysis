 Google Trends Analysis (Task 2)

 📋 Overview

This analysis demonstrates search trend analysis using the Google Trends API, with a synthetic data fallback. The goal is to show how large-scale search data can be processed and visualised to reveal patterns in user behaviour, addressing key big data challenges such as Volume, Velocity, and Variety.

 🎯 Objectives

- Demonstrate handling of search engine logs and clickstream data
- Analyse keyword popularity over time
- Generate visualisations of search trends
- Compare different search terms and their popularity patterns

 📊 Data Sources

| Source | Description |
|--------|-------------|
| **Google Trends API** | Live search interest data (fetched via `pytrends`) |
| **Synthetic Data (Fallback)** | Realistic generated data if API is unavailable |

 Keywords Analysed
- **python** - Programming language interest
- **data science** - Field of study popularity
- **machine learning** - AI subfield interest

🚀 Running the Analysis

 Prerequisites

```bash
# Install required libraries
pip install pandas numpy matplotlib seaborn pytrends
