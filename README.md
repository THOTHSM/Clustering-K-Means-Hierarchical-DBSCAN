# Scaler - Clustering

### Goal
The goal of this project is to cluster Scaler's learner profiles based on their job position, company, CTC, and other relevant features. The clustering will help identify distinct groups of learners with similar characteristics, which can assist in profiling the best companies and job positions for talent acquisition and management strategies.

### Problem Statement
Scaler is an online tech-versity offering intensive computer science and data science courses through live classes led by industry experts. As a data scientist working with the analytics team, you are tasked with clustering learners based on their job profile, company, and other features to identify groups with similar characteristics from the Scaler database.

### Data Dictionary:
- **Unnamed 0**: Index of the dataset.
- **Email_hash**: Anonymized Personal Identifiable Information (PII).
- **Company_hash**: Anonymized identifier for the current employer of the learner.
- **orgyear**: Employment start date.
- **CTC**: Current CTC.
- **Job_position**: Job profile in the company.
- **CTC_updated_year**: Year in which CTC got updated (Yearly increments, Promotions).

### Summary of Clustering Process:

#### 1. Data Loading and Initial Exploration:
- The dataset was loaded from a CSV file.
- An initial examination was conducted to understand its structure and the types of information it contains.

#### 2. Data Cleaning:
- Cleaned the **job_position** column by removing special characters to ensure consistency in the data.
- Removed duplicate entries based on **email_hash**, **job_position**, and **company_hash** to refine the dataset.

#### 3. Feature Engineering:
- Created a new column, **years_of_experience**, by calculating the difference between the current year and the learner's entry year (orgyear).

#### 4. Data Scaling:
- Applied **StandardScaler** to standardize the dataset, ensuring all features contributed equally to clustering algorithms.

#### 5. Handling Missing Values:
- Used the **KNN Imputer** to fill in missing values, improving the dataset’s completeness and reliability for analysis.

#### 6. Outlier Detection:
- Employed the **Local Outlier Factor** (LOF) method to detect and remove outliers that could distort the clustering results.

#### 7. Clustering Techniques:
- **K-Means Clustering**: Applied the K-Means algorithm, using the **Elbow Method** to determine that four clusters were optimal.
- **Hierarchical Clustering**: Performed on a sample of the data due to computational limitations and plotted a dendrogram to visualize the relationships between clusters.
- **DBSCAN Clustering**: Implemented to identify density-based clusters, with some data points labeled as noise.

#### 8. Dimensionality Reduction and Visualization:
- Employed **t-SNE** and **PCA** techniques to reduce dimensionality and visualize clustering results in two dimensions, providing insights into the clusters’ characteristics.

#### 9. Final Analysis and Conclusion:
- The analysis identified distinct categories of job positions within the dataset, highlighting specific job trends and CTC distributions.
- These findings can be leveraged for decision-making and strategies in talent acquisition and management.

