# Restaurant-Clustering (Zomato)
**Objective:**
The goal of this project was to perform clustering analysis on Zomato restaurant data to identify distinct groups or clusters of restaurants based on various features such as ratings, sentiment scores from reviews, cost, and cuisine types. This analysis aimed to uncover hidden patterns and insights that could be valuable for restaurant recommendations and strategic decision-making.

**Dataset:**
The dataset comprises two primary CSV files:
1. **Zomato Restaurant names and Metadata.csv:** Contains 105 rows and 6 columns with information about restaurants, including names and metadata.
2. **Zomato Restaurant reviews.csv:** Contains 10,000 rows and 7 columns with detailed reviews of restaurants, including ratings, review text, and metadata.

**Specific Tasks:**

- **Data Collection and Initial Look:** The project began with collecting two CSV files from Zomato: one with restaurant names and metadata, and the other with detailed reviews. Initial exploration involved inspecting the data's structure, identifying key variables, and assessing the quality and completeness of the information to prepare for subsequent analysis and preprocessing.

- **Data Wrangling, Visualization and Storytelling:** Data cleaning and transformation were performed to handle missing values, inconsistencies, and data type conversions. This step ensured the data was suitable for further analysis. Further visualization techniques were employed to understand the distribution and relationships between variables. Charts and graphs were created to illustrate patterns in ratings, costs, and review sentiments.

- **Text Preprocessing & Sentiment Analysis:** Reviews were preprocessed by removing stopwords, handling abbreviations, and normalizing text. Sentiment analysis was conducted using DistilBERT, which provided sentiment scores along with labels (Positive, Negative, Neutral) for each review. Visualized the resulting data.

- **Hypothesis Testing:** Hypotheses were formulated and tested regarding the relationships between review length, ratings, and sentiment to validate assumptions and gain deeper insights.

- **Feature Engineering & Data Preprocessing:** Features were engineered, encoded and scaled to prepare the dataset for machine learning models. This included using one-hot encoder on Sentiment and multilabel encoder on Cuisine columns. MultiLabel Encoder were used after categorizing 42 unique cuisines into 12. Review text was vectorized  using DistilBERT embeddings, which resulted in 768-dimensional vectors.  Dimensionality reduction (UMAP) was then applied to reduce these 768 dimensions to 90, which resulted in 108 columns in total. To further refine the feature set, UMAP was again used to reduce these 108 dimensions to 25 before proceeding with modeling.

- **ML Model Implementation:** Several clustering algorithms were applied, including K-Means, DBSCAN, and Mean Shift. Each model was evaluated based on Silhouette Score, Davies-Bouldin Index, and Calinski-Harabasz Index to determine the best fit for the data. The clustering results were analyzed to interpret and label clusters based on the features and insights derived from the models. This involved examining the characteristics of each cluster and understanding how different restaurants grouped together.

**Results:**
The clustering models (K-Means, and Mean Shift) achieved similar metrics:
- **Silhouette Score:** 0.80
- **Davies-Bouldin Index:** 0.31
- **Calinski-Harabasz Index:** 416.77

The clustering analysis of the Zomato restaurant data effectively identified distinct groups, revealing insights into different market segments. K-Means and MeanShift models demonstrated superior performance with a Silhouette Score of 0.79, a Davies-Bouldin Index of 0.31, and a Calinski-Harabasz Index of 416.77. These models produced well-defined clusters characterized by diverse features such as ratings, costs, and cuisine types. The clusters identified various restaurant categories, from high-end establishments with excellent reviews to budget-friendly options specializing in fast food. These insights can be used for targeted marketing, personalized recommendations, and strategic planning within the restaurant industry.
![image](https://github.com/user-attachments/assets/3a7211b6-a7d9-40db-8c4c-9956e579c53f)

**Conclusion:**
The clustering analysis revealed distinct groups of restaurants based on various features such as ratings, cost, sentiment, and cuisine types. These insights can be leveraged for personalized recommendations, market segmentation, and strategic planning. The project demonstrated the effectiveness of combining data preprocessing, sentiment analysis, and clustering techniques to extract valuable insights from complex datasets.
