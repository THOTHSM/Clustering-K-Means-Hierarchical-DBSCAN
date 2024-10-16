Business Case: Scaler - Clustering

Problem Statement

Scaler is an online tech-versity offering intensive computer science & Data Science courses through live classes delivered by tech leaders and subject matter experts. The meticulously structured program enhances the skills of software professionals by offering a modern curriculum with exposure to the latest technologies. It is a product by InterviewBit.

You are working as a data scientist with the analytics vertical of Scaler, focused on profiling the best companies and job positions to work for from the Scaler database. You are provided with the information for a segment of learners and tasked to cluster them on the basis of their job profile, company, and other features. Ideally, these clusters should have similar characteristics.

Data Dictionary:

    ‘Unnamed 0’ - Index of the dataset
    Email_hash - Anonymised Personal Identifiable Information (PII)
    Company_hash - This represents an anonymized identifier for the company, which is the current employer of the learner.
    orgyear - Employment start date
    CTC - Current CTC
    Job_position - Job profile in the company
    CTC_updated_year - Year in which CTC got updated (Yearly increments, Promotions)

Summary :
This analysis involved a comprehensive exploration of a job position dataset, applying various data preprocessing and clustering techniques. Below is a summary of the key steps and findings from the analysis:

    Data Loading and Initial Exploration:
        The dataset was loaded from a CSV file, and an initial examination was conducted to understand its structure and contents.

    Data Cleaning:
        The job_position column was cleaned by removing special characters to ensure consistency in the data.
        Duplicate entries were removed based on email_hash, job_position, and company_hash, resulting in a more refined dataset.

    Feature Engineering:
        A new column, years_of_experience, was created by calculating the difference between the current year and the year of organization entry (orgyear).

    Data Scaling:
        The dataset was standardized using StandardScaler to ensure that all features contributed equally to the clustering algorithms.

    Handling Missing Values:
        The KNN Imputer was applied to address any missing values in the dataset, enhancing the overall data quality for analysis.

    Outlier Detection:
        The Local Outlier Factor method was used to identify and remove outliers from the dataset, which may skew clustering results.

    Clustering Techniques:
        K-Means clustering was applied, using the Elbow Method to determine the optimal number of clusters, which was found to be four.
        Hierarchical clustering was performed on a sample of the data due to computational constraints, and a dendrogram was plotted to visualize cluster relationships.
        DBSCAN clustering was implemented to identify clusters based on density, with some data points categorized as noise.

    Dimensionality Reduction and Visualization:
        t-SNE and PCA techniques were employed to visualize the clustering results in two dimensions, providing insights into the distribution of clusters and their characteristics.

    Final Analysis and Conclusion:
        The analysis revealed distinct categories of job positions within the dataset, highlighting their unique attributes.
        The findings offer valuable insights into job trends and salary distributions, which can inform decision-making and strategies in talent acquisition and management.
