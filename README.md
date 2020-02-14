# Tweet Classifier: Detecting Disasters

The beauty of Twitter is that it offers real-time communication of users. And when a disaster happens, being able to analyze tweets can better assist in responding to the situation. That’s why it’s important for media outlets and disaster relief organizations, like FEMA, to monitor social media. Programming a machine learning model to do this can be difficult. There’s certain words that can mean different things that humans can decipher quicker than a machine. For example, “on fire” can refer to an actual fire, as in “that building is on fire”, or a term used when you eat something spicy, as in “my mouth is on fire”. I believe that there are certain elements in a tweet that a model can recognize to predict whether a tweet is referring to a real disaster, like unique keywords and the length of tweets. The goal of this project is to build a model that can recognize the difference and predict what’s referring to a disaster and what is not.

## Data
Data is coming from Data for Everyone (https://www.figure-eight.com/data-for-everyone/) where there’s a data set for about 10,000 tweets that include the tweet and whether it’s relevant or not relevant to the topic of a real disaster. 

## Process

1. Text data had to be cleaned before being used by any machine learning model.
      a. Removing common characters that are seen in tweets such as hashtags, mentions, and urls
      b. Lowercasing words
      c. Lemmatize words
      d. Remove stopwords

2. Feature Engineering was done to create numerical features such as hashtag count, length of tweet and number of words.

3. Exploratory Data Analysis was done to get a sense of what kind of story the data is providing. Disaster tweets tend to be longer and have more words, and usually include words such as 'Suicide', 'Bomb', and 'Wildfire'. 

4. Converting cleaned text to vectors using CountVectorizer and TfidfVectorizer

5. Logistic Regression, SVC, KNN, Decision Tree Classifier, Random Forest Classifier, AdaBoost Classifier, and Gradient Boost Classifier were tested against each other to see which algorithm performed the best when measuring against f1-score.

6. Logistic Regression, SVC, and Random Forest Classifier were further refined to produce optimal results.

## Results

Logistic Regression model performed the best along with TfidfVectorizer. I was able to produce a model that has an accuracy score of about 80% and a f1 score of 0.76


## Files

Tweet Classifier: Detecting Disasters.ipynb : This contains the code for this project. From importing the data, to cleaning, to machine learning. All of this projects code is in this file.

Tweet Classifier_ Detecting Disasters Slide Deck Final.pdf: These are report slides with basic information about the project. If you want more detail into the thinking behind the process, please read Tweet Classifer_ Detecting Disasters Final.pdf

Tweet Classifer_ Detecting Disasters Final.pdf: Detailed approach and analysis to this problem.

Tweet Classifer_ Detecting Disasters Milestone1.pdf: A midpoint report before machine learning was used. Everything in this file is also included in Tweet Classifer_ Detecting Disasters Final.pdf file.
