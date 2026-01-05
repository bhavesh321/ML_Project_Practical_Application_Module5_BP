# Coffee Coupon Acceptance Analysis

## Problem Statement
This project analyzes coupon acceptance behavior using survey data from Amazon Mechanical Turk. 

The problem is to identify factors influencing acceptance of Coffee House coupons, distinguishing between acceptors and non-acceptors using visualizations and statistical analysis.

## Key Project Structure
- `prompt.ipynb`: Main analysis notebook with guided questions and exploratory tasks
- `data/coupons.csv`: Survey dataset with 12,686 records and 26 features (user attributes, contextual factors, coupon attributes)
- `images/`: Contains reference images for Git workflow and project setup
- [practical-application.ipynb](practical-application.ipynb) Main analysis notebook for the Coffee Cupons acceptance analysis and findings. Divided in 5 sections.
    1. Important Libraries and Load Data
    2. Explore Features and Complete Feature Engineering
    3. Outlier Detections
    4. Analysis- Coffee Cupons
    5. Findings

## Data Source
Data from UCI Machine Learning Repository (coupons.csv).

## Dataset Characteristics
- **Target Variable**: `Y` (1=accepted coupon, 0=rejected), renamed to 'coupon_accepted' for better readabiliy
- **Coupon Types**: Bar, Coffee House, Restaurant(<$20), Restaurant($20-50), Carry out & Take away
- **Key Features**: Demographics (age, income, education), behavioral patterns (bar/restaurant frequency), contextual factors (weather, time, passenger type)
- **Data Issues**: `car` column has excessive missing values and should be dropped early in analysis


### Key Insights:
- **Overall Acceptance**: Coffee House coupons show varying acceptance rates across different demographic groups.
- **Demographic Trends**: Acceptance rates differ by age (e.g., higher in certain age groups like 50+) and income levels. For example, acceptance peaks in mid-to-high income ranges ($30K-$62.5K). Specific groups like young low-income individuals (<21 and <$25K) have very low acceptance (0%).
- **Driving Direction**: Higher acceptance when the driving direction matches the coupon location.
- **Outliers**: Numerical features like `bar_num`, `toCoupon_GEQ5min`, etc., have outliers detected via IQR method, but they are minimal and don't skew distributions significantly at least for the Coffee House Cupon
- **Marketing Implications**: Target marketing campaigns to users with income $30K-$62.5K and those already heading toward the coupon location. Avoid targeting young low-income groups as acceptance is negligible.

### Visualizations Demonstrating Exploration of Differences
- Bar plot of acceptance rates by age shows variations across age groups.
- Line plot of acceptance rates by income indicates trends, with peaks in mid-to-high income ranges.
- Box plot of income by acceptance status highlights distribution differences.
- Histogram of age distribution provides context on demographics.
- Box plots for outliers in numerical features ensure data quality.


