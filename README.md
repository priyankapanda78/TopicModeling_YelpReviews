# TopicModeling_YelpReviews

Goal: To find topics in positive and negative restaurant reviews in Yelp.

Data Source: Yelp Dataset

Tools used:
* Data Visulization: matplotlib,seaborn
* Tools used: Pandas, sklearn, gensim, NLTK

Datasets brief description:
Yelp_academic_dataset_business: Details of all business including the location.
Yelp_academic_dataset_reviews: All the reviews with reviewIds, business Ids, ratings.

Preprocessing:
* Neutral reviews with ratings 3/3.5 are removed from the data as that is not much useful in identifying topics for 
  Positive / Negative.
* Ratings with 4 or above are categorized as Positive Reviews.
* Ratings with 2 or below are categorized as Negative Reviews.
* Included Stopwords, Stemming and bigrams for CountVectorizer.

Algorithms:
* TFIDF with LDA
* CountVectorizer with LDA (bigrams)
* TFIDF with NMF

Results:
* TFIDF with LDA: This model is not able to detect negative context of the document, also not able to detect sarcasm in the     reviews.
* CountVectorizer with LDA (bigrams): This model performs better after including bigrams, as it gives negative topics for the   reviews. But the topics for both Positive and Negative reviews are mostly over lapping with each other.
* TFIDF with NMF: The topics for both positive and negative reviews are more distributed. This model gives better insights on   different business and could be helpful for Future work in the project.
