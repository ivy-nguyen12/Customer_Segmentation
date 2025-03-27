# Airline Customer Segmentation

## Overview
This project applies unsupervised machine learning to segment Sun Country Airlines customers into distinct groups based on their booking and travel behavior. Using K-Means clustering and Python preprocessing, we uncovered five customer segments and identified their key characteristics. These insights help the airline tailor targeted marketing strategies, enhance loyalty, and improve the customer experience.

Prepared by: Vy Nguyen, Becky Wang, Dennis Wu, Kenjee Koh, Hsiang-Han Huang

Key business takeaways:
- Customers differ significantly by booking habits, loyalty status, and seasonal preferences
- Targeted strategies for each segment can drive revenue growth and loyalty
- Clusters 1 & 2 represent the majority of customers and prefer non-digital channels
- Cluster 4 travelers are likely business flyers booking last-minute trips
- Cluster 3 (Ufly members) show strong early-booking loyalty and higher spending

## Dataset
- **Source:** Internal reservation and booking data from Sun Country Airlines
- **Scope:** Passenger-level records including demographics, booking details, loyalty status, and trip specifics
- **Size:** ~48,000 customers (exact varies by filtering steps)
- **Goal:** Identify behavioral patterns and group customers using unsupervised learning

### 📋 Data Dictionary
| Feature Type          | Examples                                                                                  |
|-----------------------|-------------------------------------------------------------------------------------------|
| **Continuous Variables** | `BaseFareAmt`, `Days_Prebooked`, `Age`                                                   |
| **Categorical Variables** | `Gender`, `BkdClassOfService`, `BookingChannel`, `UflyMemberStatus`, `Seasonality`       |
| **Boolean Variables** | `CardHolder`, `StopoverCode`, `RoundTrip`, `Group`                                        |

All categorical variables were encoded using one-hot encoding. Continuous variables were scaled to standardize influence.

## Tools & Methodology Overview
**Languages and Libraries:** Python (pandas, sklearn, matplotlib, seaborn), Tableau

### Data Preprocessing:
- Scaled continuous features to [0,1] range
- Encoded categorical variables using dummy variables
- Converted boolean features to numerical format (True = 1, False = 0)
- Filtered for verified bookings and cleaned anomalies

### Clustering Approach:
- Used K-Means clustering (k=5) based on Elbow Method
- Fitted clustering model with 30 initialization runs (n_init=30)
- Assigned cluster labels back to original data using unique customer ID
- Analyzed clusters using grouped summary statistics (mean/mode) and visualizations

## Cluster Summaries & Titles
| Cluster | Segment Name                            | Description                                                                 |
|---------|------------------------------------------|-----------------------------------------------------------------------------|
| 0       | Spontaneous Direct Flyers in Summer      | Book late, fly direct in Q3, not Ufly members                              |
| 1       | Non-Member Seasonal Group Travelers      | Prefer group travel, seasonal, use mixed booking channels                  |
| 2       | Non-Member Middle-Aged Leisure Travelers | 35+, leisure flyers, prefer outside booking, seasonal                      |
| 3       | Ufly Early-Bird Direct Flyers            | Loyal Ufly members, book far in advance, prefer non-stop flights           |
| 4       | Non-Member Business Travelers            | Solo flyers, stopovers, last-minute bookings, higher spenders in summer    |

## Results & Key Insights
- **Clusters 1 & 2** make up the majority of the customer base and prefer offline booking. Target them with non-digital promotions, mail campaigns, and group deals.
- **Cluster 4** aligns with business travelers: solo flyers, higher base fare, stopovers, and Q3 travel. Promote premium packages and last-minute travel deals.
- **Cluster 3 (Ufly members)** show strong loyalty and pre-booking behavior. Encourage continued engagement through tiered perks, referrals, and premium upgrades.
- **Seasonal preferences** vary by cluster. For example, Cluster 0 & 4 travel mostly in summer, while Cluster 1, 2, and 3 are winter/spring travelers.

## Recommendations
- **Cluster 4 - Business Travelers:** Offer flight-hotel-ride packages, tier upgrades, and time-saving perks. Partner with MSP hotels and corporate programs.
- **Clusters 1 & 2 - Group and Older Travelers:** Promote family packages, print-based promotions, and airport engagement booths.
- **All Clusters - Seasonality-Based Promotions:** Market Fort Myers, Las Vegas, Costa Rica for Q3 flyers; promote Seattle and Miami for winter/spring travelers.
- **Cluster 3 - Ufly Loyalty Flyers:** Introduce referral bonuses (e.g., lounge access, free baggage), and discounts on premium add-ons for early bookings.

## Key Deliverables
- Jupyter Notebook
- Final Report PDF

## What I Learned
- Unsupervised clustering is a powerful tool for customer segmentation even without a target variable
- Feature scaling and encoding have a major impact on clustering performance
- Visualizations and grouped statistics enhance the interpretation of abstract clusters
- Aligning marketing strategy with data-driven segmentation improves personalization and efficiency

## What I Plan to Improve
- Apply alternative clustering techniques (e.g., DBSCAN, Hierarchical) to compare cluster stability
- Re-run the segmentation regularly with new data to adapt to shifting customer behavior

## About Me
Hi, I’m Vy Nguyen and I’m currently pursuing my MS in Business Analytics at UC Irvine. I’m passionate about data analytics in Finance, Investment, and Customer Strategy. Connect with me on [LinkedIn](https://www.linkedin.com/in/vy-ngoc-lan-nguyen).
