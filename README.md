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

Given the size of our dataset, we utilize the Kaggle API to seamlessly transfer data from Kaggle's environment to Google Colab. Begin by generating a new API token in your Kaggle account, which will download a kaggle.json file.

Results

In this project, we developed a logistic regression model to classify tweets as either positive or negative. After thorough data preprocessing and model tuning, we achieved the following results:

The accuracy score on the training data: 81.73% The accuracy score on the test data: 78.28% These results indicate that our logistic regression model performs well in classifying the sentiment of tweets, achieving a high level of accuracy. The slight drop in accuracy from the training data to the test data suggests a good generalization capability of the model, although there might still be room for improvement.

Overall, logistic regression has proven to be an effective method for this binary classification task, providing a solid foundation for further enhancements or integration into larger systems for sentiment analysis.

Implications for Stakeholders
The logistic regression model provides a reliable method for sentiment analysis, offering valuable insights into public opinion as expressed on Twitter. This can be particularly useful for monitoring brand sentiment, customer feedback, and market trends. While the current model performs well, ongoing refinements and the integration of additional data sources could further enhance its accuracy and reliability.

By leveraging this model, stakeholders can make more informed decisions based on real-time sentiment analysis, ultimately driving better strategies and outcomes.

Challanges and solution

When initially importing data from Kaggle, the column headers did not import correctly. To resolve this issue, I referenced the dataset description where all the column names were specified. I created a variable named column_names and set the dataframe's column parameter to this variable, ensuring accurate data import.

The stemming function stemming_func requires significant processing time due to the dataset's large size. In my case, it took up to 10 minutes to complete.

Due to the dataset's size, hyperparameter tuning is computationally intensive. To mitigate this, I created a subset of the dataset for tuning. Surprisingly, the best parameters identified on this subset closely resembled the default parameters of the logistic regression model.
