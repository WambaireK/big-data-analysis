

## 📊 Case Study Overview

### 1. Amazon Case Study (Task 1) 🚚

**Objective:** Analyse delivery patterns to identify operational inefficiencies and provide evidence-based recommendations.

**Dataset:** Amazon Delivery Dataset (43,739 records, 16 features)

**Key Analyses:**
- ⏰ **Time-Based Analysis:** Peak order hours and delivery time distribution
- 🗺️ **Geographic Analysis:** Delivery distances and area type impact
- 🌦️ **Factor Analysis:** Traffic and weather conditions
- 👤 **Agent Performance:** Age and rating correlations
- 🚗 **Operational Factors:** Vehicle type and product category

**Key Findings:**
- Peak order hours: 17:00-23:00 (4,200-4,700 orders/hour)
- Metropolitan areas show highest delivery time variability
- Traffic congestion and stormy weather significantly increase delivery times
- No correlation between agent age/rating and delivery time

**Recommendation:** Hybrid Lambda architecture combining batch processing (historical analysis) with stream processing (real-time route optimisation).

**📁 Folder:** [`amazon_analysis/`](amazon_analysis/README.md)

---

### 2. Google Case Study (Task 2) 🔎

**Objective:** Demonstrate search trend analysis using Google Trends data, handling search engine logs and clickstream data.

**Method:**
- Fetches live data from Google Trends API
- Falls back to synthetic data if API is unavailable
- Generates 4 visualisations

**Keywords Analysed:**
- `python` - Programming language
- `data science` - Field of study
- `machine learning` - AI subfield

**Key Findings:**
- Machine learning shows the strongest long-term growth
- Python has stable interest with seasonal peaks
- Data science maintains consistent search volume

**📁 Folder:** [`google_analysis/`](google_analysis/README.md)

---

### 3. Netflix Case Study (Task 3) 🎬

**Objective:** Build a content-based recommendation system using the MovieLens 100k dataset.

**Dataset:** MovieLens 100k (100,000 ratings, 943 users, 1,682 movies)

**Method:**
- Content-based filtering using TF-IDF and cosine similarity
- Memory-optimised to run in Google Colab free tier
- Generates 2 visualisations

**Key Findings:**
- Rating distribution shows right-skew pattern
- Top 10 movies concentrate user attention
- Content-based filtering can address cold-start problem

**📁 Folder:** [`netflix_analysis/`](netflix_analysis/README.md)

---

## 🔍 Key Insights Across Case Studies

| Theme | Amazon | Google | Netflix |
|-------|--------|--------|---------|
| **Big Data Problem** | Big P + Big N | Volume + Velocity | Big P + Big N |
| **Key Challenge** | Too many features & observations | Real-time data processing | Data sparsity & cold-start |
| **Solution Approach** | Lambda Architecture | API integration + visualisation | Content-based filtering |
| **Visualisations** | 5 pair charts | 4 trend charts | 2 analysis charts |
| **Key Finding** | Peak hours 17:00-23:00 | ML has strongest growth | Rating distribution skewed right |

### Common Themes

1. **Real-Time vs Batch Processing**: Across all cases, the trade-off between real-time and batch processing emerges as a central concern. Amazon needs both (peak hours vs off-peak), Google needs real-time search trends, and Netflix needs batch training with real-time inference.

2. **Data Sparsity**: Both Amazon (category-specific deliveries) and Netflix (user-item matrix) face the challenge of sparse data, requiring different strategies to generate meaningful insights.

3. **Feature Selection**: The Big P problem (too many features) appears in both Amazon and Netflix, requiring regularization techniques like Lasso to identify the most predictive features.

---

## 🚀 Quick Start

### Prerequisites

```bash
# Python 3.7+
pip install -r requirements.txt
Running All Analyses
bash
# Clone the repository
git clone https://github.com/WambaireK/big-data-analysis.git
cd big-data-analysis

# Amazon Analysis
cd amazon_analysis
jupyter notebook notebooks/01_analysis.ipynb

# Google Analysis
cd ../google_analysis
python google_trends_complete.py

# Netflix Analysis
cd ../netflix_analysis
python netflix_recommender_stable.py
📦 Dependencies
text
pandas>=1.5.0
numpy>=1.24.0
matplotlib>=3.7.0
seaborn>=0.12.0
scikit-learn>=1.2.0
scipy>=1.10.0
pytrends>=4.9.0      # Google Trends (optional)
datasets>=2.0.0      # For dataset loading
📚 References
Big Data Fundamentals
Chen, M., Mao, S. and Liu, Y. (2014) 'Big data: A survey', Mobile Networks and Applications, 19(2), pp. 171-209.

Gandomi, A. and Haider, M. (2015) 'Beyond the hype: Big data concepts, methods, and analytics', International Journal of Information Management, 35(2), pp. 137-144.

Distributed Computing
Dean, J. and Ghemawat, S. (2008) 'MapReduce: Simplified data processing on large clusters', Communications of the ACM, 51(1), pp. 107-113.

Chang, F. et al. (2008) 'Bigtable: A distributed storage system for structured data', ACM Transactions on Computer Systems, 26(2), pp. 1-26.

Melnik, S. et al. (2010) 'Dremel: Interactive analysis of web-scale datasets', Proceedings of the VLDB Endowment, 3(1-2), pp. 330-339.

Kreps, J. (2014) 'Questioning the Lambda Architecture', O'Reilly Radar, 2 July.

Zaharia, M. et al. (2012) 'Resilient distributed datasets: A fault-tolerant abstraction for in-memory cluster computing', in Proceedings of the 9th USENIX Conference on Networked Systems Design and Implementation. San Jose, CA: USENIX Association, pp. 15-28.

Machine Learning & Regularization
Tibshirani, R. (1996) 'Regression shrinkage and selection via the lasso', Journal of the Royal Statistical Society: Series B (Methodological), 58(1), pp. 267-288.

Hoerl, A.E. and Kennard, R.W. (1970) 'Ridge regression: Biased estimation for nonorthogonal problems', Technometrics, 12(1), pp. 55-67.

Zou, H. and Hastie, T. (2005) 'Regularization and variable selection via the elastic net', Journal of the Royal Statistical Society: Series B (Statistical Methodology), 67(2), pp. 301-320.

Recommendation Systems
Gomez-Uribe, C.A. and Hunt, N. (2016) 'The Netflix recommender system: Algorithms, business value, and innovation', ACM Transactions on Management Information Systems, 6(4), pp. 1-19.

Bennett, J. and Lanning, S. (2007) 'The Netflix Prize', in Proceedings of KDD Cup and Workshop. San Jose, CA: ACM, pp. 3-6.

Ethics & Fairness
Barocas, S., Hardt, M. and Narayanan, A. (2019) Fairness and Machine Learning: Limitations and Opportunities. Cambridge, MA: fairmlbook.org.

Mitchell, M. et al. (2019) 'Model cards for model reporting', in Proceedings of the Conference on Fairness, Accountability, and Transparency. Atlanta, GA: ACM, pp. 220-229.

Zuboff, S. (2019) The Age of Surveillance Capitalism: The Fight for a Human Future at the New Frontier of Power. New York: PublicAffairs.

Cross-Validation
Stone, M. (1974) 'Cross-validatory choice and assessment of statistical predictions', Journal of the Royal Statistical Society: Series B (Methodological), 36(2), pp. 111-147.

Kohavi, R. (1995) 'A study of cross-validation and bootstrap for accuracy estimation and model selection', in Proceedings of the 14th International Joint Conference on Artificial Intelligence. Montreal: Morgan Kaufmann, pp. 1137-1143.

📄 License
This repository is for educational purposes as part of the Master of Science in Data Science program at [Institution Name].

 ✅ Summary

| Section | Include in Main README? |
|---------|------------------------|
| **Key Insights Across Case Studies** | ✅ Yes - shows synthesis and critical thinking |
| **References** | ✅ Yes - demonstrates academic integrity |
| **Repository Structure** | ✅ Yes - helps navigation |
| **Case Study Overviews** | ✅ Yes - provides context |
| **Quick Start** | ✅ Yes - helps reproducibility |
