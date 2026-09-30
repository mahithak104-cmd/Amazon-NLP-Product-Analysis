# Amazon NLP Product Analysis
This project uses Natural Language Processing and machine learning to analyze Amazon product data. The main goal was to see how product titles, features, and descriptions can be used to automatically categorize products, find patterns between products, and build a simple product search system.

## What I Worked With

The dataset contains **25,000 Amazon products** across five categories:

- Electronics
- Books
- Toys & Games
- Automotive
- Beauty & Personal Care

For each product, I combined the title, features, and description into a single text field and used that information for the NLP and machine learning tasks.

## What I Built

The project has three main parts:

1. **Product Classification** – Predicting the product category using Multinomial Naive Bayes.
2. **Product Clustering** – Using KMeans to explore whether products naturally form groups based on their descriptions.
3. **Product Search** – Using TF-IDF and cosine similarity to find products that are similar to a user's search query.

## Tools & Technologies

- Python
- Pandas
- NumPy
- NLTK
- Scikit-learn
- Matplotlib
- Jupyter Notebook

## NLP Preprocessing

Before training the models, I cleaned and prepared the product text using:

- Text normalization
- Tokenization
- Stopword removal
- Stemming with Porter Stemmer
- TF-IDF vectorization
- Unigrams and bigrams

The title, features, and description were combined so that the model could use more information about each product.

## Product Classification

I used a **Multinomial Naive Bayes** classifier with TF-IDF features to predict the category of each product.

The model achieved:

**94.3% accuracy**

The overall macro F1-score was approximately **0.94**.

The model performed particularly well on the **Beauty & Personal Care** category, which had an F1-score of **0.98**.

The **Toys & Games** category was more difficult for the model, with a recall of **0.89**. Some products were classified as Automotive or Electronics, which makes sense for products that share terms such as "car," "battery," "electronic," or "set."

## Product Clustering

I also used **KMeans clustering** to see whether products would naturally group together based only on their text.

I looked at:

- The products in each cluster
- The most common terms in each cluster
- The relationship between clusters and the known product categories
- A 2D TruncatedSVD visualization
- Silhouette scores for different values of K

With five clusters, the silhouette score was approximately **0.010**. I also tested values of K from 2 to 10, but the scores remained very low.

This showed that there is a lot of overlap between products in the TF-IDF feature space. In other words, products from different categories often use similar words in their descriptions.

## Classification Performance

The Multinomial Naive Bayes model achieved **94.3% accuracy**.

![Confusion Matrix](./confusion-matrix.jpg)

## KMeans Clustering

![KMeans Clusters](KMeans%20Product%20Clusters.jpg)

## Silhouette Analysis

![Silhouette Scores](Silhouette%20Score%20for%20Different%20K%20Values.jpg)

## Product Search

The final part of the project was a simple text-based product search system.

I used:

- TF-IDF
- Cosine similarity

A user can enter a query, and the system returns the most similar products based on their text.

## Conclusion
This project gave me hands-on experience applying NLP and machine learning to a real-world e-commerce dataset. It also helped me understand the difference between supervised learning, where the model can learn from known product categories, and unsupervised learning, where the underlying product groupings are much less clearly separated.
The final system combines classification, clustering, and text-based search into one project and provides a good starting point for experimenting with more advanced NLP and multimodal approaches.

##  Author

**Mahitha Kalinathabotla**

Master of Science in Business Analytics  
University at Albany, SUNY

- GitHub: https://github.com/mahithak104-cmd
- LinkedIn: [www.linkedin.com/in/mahitha-kalinathabotla]
