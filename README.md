# Sentiment-Analysis-on-Tweets
Problem statement

Analyzing sentiment in social media, particularly Twitter, presents a complex challenge due to the diverse nature of user-generated content and the nuances of language. Traditional methods often struggle with the variability and noise inherent in Twitter data, which includes slang, sarcasm, and varying sentence structures. These factors can complicate sentiment classification, affecting the accuracy of predictive models.

This project aims to develop an advanced sentiment analysis model using Twitter data, focusing on classifying tweets as positive or negative based on their content. We aim to employ Natural Language Processing (NLP) techniques for robust text preprocessing, including tokenization, stopwords removal, and lemmatization. The model will utilize Logistic Regression, a well-established classification algorithm, to accurately predict sentiment labels. The insights gained from this analysis will provide a valuable understanding of public sentiment trends on Twitter, facilitating applications in market research, brand management, and social listening.

Dataset description
The dataset we are using for this project is Kaggle's Sentiment140 dataset with 1.6 million tweets, which can be downloaded from the provided link(https://www.kaggle.com/datasets/kazanova/sentiment140).The sentiment140 dataset contains 1,600,000 tweets extracted using the twitter api . The tweets have been annotated (0 = negative, 4 = positive) and they can be used to detect sentiment . It contains the following 6 fields:

1.target: the polarity of the tweet (0 = negative, 2 = neutral, 4 = positive)

2.ids: The id of the tweet ( 2087)

3.date: the date of the tweet (Sat May 16 23:58:44 UTC 2009)

4.flag: The query (lyx). If there is no query, then this value is NO_QUERY.

5.user: the user that tweeted (robotickilldozr)

6.text: the text of the tweet (Lyx is cool)

Data Collection

Given the size of our dataset, we utilize the Kaggle API to seamlessly transfer data from Kaggle's environment to Google Colab. Begin by generating a new API token in your Kaggle account, which will download a kaggle.json file. Upload this file to your Colab environment:
