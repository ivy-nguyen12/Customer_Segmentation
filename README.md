# Sun-Country_Customer-Segmentation
Objective: This project processed Sun Country Airlines’ customer data using K-means clustering in Python to identify 5 distinct segments. For each segment, targeted marketing strategies were developed based on unique insights derived from Python and Tableau visualizations.

Project prepared by: Vy Nguyen, Becky Wang, Dennis Wu, Kenjee Koh, Hsiang-Han Huang.

## Clustering Approach
First, we tested an optimum number of clusters in range 1 to 21 and designed an elbow curve plot to find the suitable number (cluster =5). Then we applied the cluster to fit data columns, running 30 times with different centroids. Last, we assigned the cluster column back to the original clustering data by merging on UID number.

## Data Preparation
For continuous variables, we scaled the influence of each variable and replaced it with the transformed data (0 to 1); For categorical variables, we chose more influential columns and converted them to dummy variables (=1); For Boolean variables, we converted them to numerical codes (True=1, False=0).

## Key Findings 
By analyzing the Mean and Mode for each cluster, along with visualizing the differences in characteristics, we were able to describe each cluster using tiles:    
* Cluster 0 - Spontaneous Direct Flyers in Summer
* Cluster 1 - Non-Member Seasonal Group Travelers
* Cluster 2 - Non-Member Middle-Aged Leisure Travelers
* Cluster 3 - Ufly Early-Bird Direct Flyers
* Cluster 4 - Non-Member Business Travelers

## Recommendations
Based on the segmentation analysis, we recommend Sun Country Airlines implement the below strategies to better serve distinct customer groups and maximize revenue potential:
* Business Travelers (Cluster 4): To attract solo business travelers with last-minute bookings, offer specialized packages that include flight deals, single-person hotel options, and ride-hailing credits. Incentives like tier upgrades and first-booking discounts, combined with personalized emails focusing on time-saving benefits, would further enhance appeal. Expanding "Stay-and-Fly" partnerships with MSP hotels and lounges, and establishing co-branded deals with Fortune 500 companies, would provide exclusive perks and strengthen loyalty.
* Older and Group Travelers (Clusters 1 & 2): Customers in these clusters prefer non-digital booking channels. Sun Country Airlines should invest in non-digital marketing efforts, such as mailbox fliers, vouchers, and airport booths, to engage with these segments. Promoting family and group-oriented packages, with kid-friendly resorts and activities, would appeal to group travelers, especially in Clusters 1 and 2.
* Seasonal Travelers (Clusters 0, 1, 2, 3 & 4): Tailor marketing campaigns to target seasonal preferences. Promote summer destinations like Fort Myers, Las Vegas, and Costa Rica to travelers in Clusters 0 and 4. For winter/spring travelers in Clusters 1, 2, and 3, focus on destinations like Seattle and Miami, offering exclusive flight and hotel packages to align with travel trends.
* Ufly Members (Cluster 3): Leverage the strong loyalty of Ufly members by expanding Referral and Appreciation programs. Offer exclusive referral bonuses like lounge access, free baggage, and seat upgrades. Additionally, capitalize on the higher spending patterns and early booking tendencies in this cluster by introducing tier-based loyalty perks and discounts on premium add-ons to incentivize long-term commitment
