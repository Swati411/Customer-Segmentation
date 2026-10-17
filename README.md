# Customer-Segmentation
An unsupervised machine learning project designed to segment customers into distinct behavioral groups. This repository covers data exploration, feature scaling, optimal cluster evaluation using the Elbow Method, and K-Means clustering to uncover high-value and low-value customer tiers.   


🚀 Project Overview
In competitive markets, understanding customer behavior is vital for personalizing experiences and driving revenue. Because customers vary across demographics and purchasing habits, this project uses clustering techniques to group them based on similarities, helping businesses optimize marketing strategies and improve customer retention.   


📂 Dataset & Features
The synthetic dataset contains 238 rows and 7 columns capturing customer purchasing patterns:   

Demographics & Geography: user_id, age, region

Financial & Behavior Metrics: annual_income, purchase_amount, purchase_frequency, loyalty_score

   
🛠️ Methodology & Workflow
Data Cleaning & Exploration:

Checked for missing values and duplicate rows (none found).   

Performed univariate and bivariate exploratory data analysis (EDA) to visualize distributions and correlations.   

Key Patterns Discovered: Higher annual income correlates with larger purchase amounts, and higher purchase frequency strongly correlates with a higher loyalty score.   

Preprocessing & Feature Engineering:

One-Hot Encoding: Encoded categorical features like region using pd.get_dummies (dropping the first column).   

Feature Scaling: Standardized numerical and encoded variables using StandardScaler to ensure balanced feature weighting during clustering.   

Feature Selection: Selected core metrics (annual_income, purchase_amount, purchase_frequency, and loyalty_score) to build the clustering feature matrix 
X.   

🤖 Model Training & Cluster Evaluation
Elbow Method (WCSS): Calculated the Within-Cluster-Sum-of-Squares (WCSS) for values of 
k ranging from 2 to 10 to identify the optimal number of clusters.   

K-Means Clustering: Tested multiple configurations (including 
k=5 and 
k=4).   


Silhouette Score Evaluation:

Clustering with 
k=5 yielded a strong silhouette score of 0.602.   

Clustering with 
k=4 yielded a silhouette score of 0.536.   

Cluster Visualization: Generated comparative scatter plots mapping relationships like annual_income vs. purchase_amount, age vs. purchase_amount, and annual_income vs. age across assigned cluster labels.   

💡 Key Business Insights
Customer Tiers: The segmentation successfully isolates distinct tiers (such as high-value vs. low-value groups) based on income and spending habits.   

Loyalty Link: Frequency of purchase maps directly to customer loyalty, showing clear behavioral clusters that can be targeted with customized retention campaigns.   
