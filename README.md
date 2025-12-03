📅 Customer Segmentation & Clustering Analysis Using Python (K-Means)

Using Python-based analytics and clustering, we identified five distinct customer groups to support data-driven marketing decisions. 🎯📊

<h2>📌 Table of Contents</h2> <ul> <li><a href="#project-overview">Project Overview</a></li> <li><a href="#business-problem">Business Problem</a></li> <li><a href="#dataset">Dataset</a></li> <li><a href="#tools-and-technologies">Tools & Technologies</a></li> <li><a href="#folder-structure">Folder Structure</a></li> <li><a href="#data-cleaning-preparation">Data Cleaning & Preparation</a></li> <li><a href="#libraries-used">Libraries Used</a></li> <li><a href="#eda-clustering">Exploratory Data Analysis (EDA) & Clustering</a></li> <li><a href="#key-insights">Key Insights & Recommendations</a></li> <li><a href="#references">References</a></li> <li><a href="#author-contact">Author & Contact</a></li> </ul>
<h2 id="project-overview">📘 Project Overview</h2>

This project analyzes mall customer data using Python to uncover hidden shopping patterns.
Through EDA and K-Means clustering, we segmented customers based on age, income, and spending behaviour.
The Elbow Method helped determine the optimal number of clusters for accurate grouping.
These insights support targeted marketing by identifying high-value and strategic customer segments.

<h2 id="business-problem">❗ Business Problem</h2>

The mall currently lacks data-driven insights to distinguish between different customer types and their purchasing behaviours.
As a result, marketing efforts are broad, resource-intensive, and not optimized for customer value.
The key challenge is to segment customers based on demographic and spending patterns to identify meaningful groups.
A clear segmentation model will enable precise targeting, improved campaign efficiency, and better allocation of marketing resources.

<h2 id="dataset">📂 Dataset</h2>

The dataset contains information about mall customers, including the following columns:

CustomerID – Unique identifier for each customer

Gender – Male or Female

Age – Customer’s age in years

Annual Income (k$) – Yearly income in thousands of dollars

Spending Score (1–100) – A score representing customer spending behaviour

This dataset serves as the basis for exploratory analysis and K-Means clustering to identify customer segments.

<h2 id="tools-and-technologies">🛠️ Tools & Technologies</h2>

Python – Programming language for data analysis

Jupyter Notebook – Development environment for interactive coding

Pandas – Data manipulation and preprocessing

Matplotlib & Seaborn – Data visualization

Scikit-learn – K-Means clustering, StandardScaler, One-Hot Encoding

NumPy – Numerical computations

These tools enabled end-to-end analysis, from data exploration to cluster modeling and visualization.

<h2 id="folder-structure">📁 Folder Structure</h2>

Customer_Segmentation_Project/
│
├── data/                      
│   ├── raw_customer_data.csv          # Original dataset
│   └── clustered_customer_data.csv    # Processed/clustered dataset
│
├── images/                            # All images used in the project
│
├── customer_data_visualization_python_notebook.ipynb   # Jupyter Notebook for analysis
├── report_customer_needs.pdf                             # Detailed analysis report
├── README.md                                            # Project documentation
└── .gitignore                                           # Git ignore file


<h2 id="data-cleaning-preparation">🧹 Data Cleaning & Preparation</h2>

- Missing Values: Checked for nulls and ensured the dataset was complete with no missing entries.

- Data Types: Verified and corrected data types for accurate analysis (numerical vs categorical).

- Duplicate Records: Identified and removed duplicates.

- Feature Selection: Selected Age, Income, Spending Score, Gender for clustering.

- Preprocessing: Applied StandardScaler and One-Hot Encoding for advanced multivariate clustering.

These steps ensured the dataset was clean, consistent, and ready for EDA and K-Means clustering.

<h2 id="libraries-used">📚 Libraries Used & Their Purpose</h2>

1.Pandas :	Data loading, manipulation, preprocessing

2.Matplotlib :	Plotting distributions, scatter plots, clusters

3.Seaborn :	Statistical visualizations (histograms, KDE, pairplots, heatmaps)

4.Scikit-learn :	K-Means clustering, StandardScaler, One-Hot Encoding

These libraries provided all tools required for analysis, visualization, preprocessing, and clustering.

<h2 id="eda-clustering">📊 Exploratory Data Analysis (EDA) & Clustering</h2>

It involves understanding the dataset, visualizing patterns, and applying K-Means clustering to segment customers for actionable insights.

# Univariate Analysis :

- Descriptive statistics (mean, median, quartiles)

- Histograms + KDE plots for Age, Income, Spending Score

- Observed:

     - Spending Score mostly between 40–60

     - Age & income normally distributed

- Gender-based comparison via boxplots:

     - Females → higher mean spending

     - Males → slightly higher income


![customer Analysis python DashBoard](images/Screenshot(5).png)

![customer Analysis python DashBoard](images/Screenshot(7).png)

![customer Analysis python DashBoard](images/Screenshot(8).png)

![customer Analysis python DashBoard](images/Screenshot(9).png)

![customer Analysis python DashBoard](images/Screenshot(10).png)


# Bivariate Analysis :

- Scatter plots for relationships between variables

- Annual Income vs Spending Score suggested natural clustering

- Pairplots for multivariate visualization

- Heatmap correlations:

     Age ↘ Spending Score

     Age ↘ Income

     Income ↗ Spending = weak

- Gender grouping for comparative metrics


![customer-Analysis-python-DashBoard](Screenshot(11).png)

![customer Analysis python DashBoard](Screenshot(12).png)

![customer Analysis python DashBoard](Screenshot(13).png)

# Determining Optimal Clusters (Elbow Method) :

- Calculated inertia for k = 1 to 10

- Elbow at k = 5 → optimal number of clusters

- Used for bivariate clustering (Income + Spending Score)

# K-Means Clustering Implementation :

- Univariate Clustering

    - Applied only on Annual Income

    - Elbow → 3 clusters (low, medium, high income)

- Bivariate Clustering (Main Model)

     - Applied on Annual Income + Spending Score

     - k = 5

     - Resulting clusters:

       - High Income – High Spending

       - Low Income – High Spending

       - High Income – Low Spending

       - Low Income – Low Spending

       - Medium Income – Medium Spending

- Multivariate Clustering

     - Added Age + Gender features

     - Applied StandardScaler + One-Hot Encoding

     - Prepared dataset for advanced clustering possibilities


![customer Analysis python DashBoard2](Screenshot(14).png)

![customer Analysis python DashBoard2](Screenshot(15).png)

![customer Analysis python DashBoard2](Screenshot(16).png)

<h2 id="key-insights">💡 Key Insights & Recommendations</h2>
Cluster Summary & Marketing Recommendations


1) High-Value Customers (Cluster 4) :
     - High income, high spending, age ~32
     - Focus: Premium campaigns, loyalty programs
       

2) Strategic Opportunity Customers (Cluster 2) :
     - Low income, high spending, age ~25
     - Focus: Promotional campaigns, aspirational products

3) Low-Engagement Customers (Cluster 3) :
    - High income, low spending, age ~41
    - Focus: Personalized discounts, loyalty incentives

4) Low-Value Customers (Cluster 1) :
    - Low income, low spending, age ~45
    - Focus: Minimal marketing allocation

5) Average Customers (Cluster 0) :
    - Medium income, medium spending, age ~43
    - Focus: General promotions, occasional upselling

Overall Takeaways:
K-Means successfully segmented customers into five actionable groups Enables targeted marketing and resource optimization

<h2 id="references">📚 References</h2>

Dataset Source: Mall Customer Segmentation Dataset obtained from AbsentData
🔗 https://absentdata.com/data-analysis/where-to-find-data

<h2 id="author-contact">👤 Author & Contact</h2>

Shreeganesh Bhat

Data Analyst

Email: shriganeshbhat0@gmail.com

LinkedIn: https://www.linkedin.com/in/shreeganesh-bhat-8a8184398

GitHub: https://github.com/shriganeshbhat0-git





