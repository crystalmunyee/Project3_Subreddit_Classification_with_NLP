# Project 3: Subreddit Classification with NLP

**Introduction**

The goal of this project is to classify posts from two different subreddits based on their title and selftext, or text within the body of the post. For this project, the two subreddits that were selected are similar on the surface which are r/Yoga and r/Meditation but we are interested in uncovering what are the characteristic of both subreddits that brings users to join yoga or meditation.

**Problem Statement**

We are Data Scientists that are hired by a studio providing yoga lessons and tasked to identify potential yoga students from a meditation subreddit group to maximize profit.
- Our focus subreddit group will be r/yoga and r/Meditation.
- Deep dive into common topics and those lacked of by yoga subreddit to bring in new users/students.
- Identify the classification model with higher accuracy/recall score to get the key differences that a yoga studio needs to improve attraction from the meditation community.
- Communicate out the improvement criterias to bring in better subscription rates to maximize profit from marketing expenses.

**Executive Summary**

The final model we choosed used Count Vectorization with no max feature limit and Naive Bayes with Ridge regularization (alpha = 0.8). The model we choosed has the highest test score, recall and f1-score.
![image](https://media.git.generalassemb.ly/user/38908/files/94b84300-809c-11ec-9854-ab20855afbd3)

Some interesting insights that we obtained after finding the predictors for each subreddit post were as follow:
![image](https://media.git.generalassemb.ly/user/38908/files/794d3800-809c-11ec-9a74-ca4b81ba217a)
![image](https://media.git.generalassemb.ly/user/38908/files/7fdbaf80-809c-11ec-86fe-2cae12765270)

These keywords can help marketing build a more attractive package for future yoga enthusiast whether they are already into yoga or transitioning from meditation to yoga.

**Data Collection**

- In this stage, we scraped 1500 posts each from r/yoga and r/meditation and this was optimized using a function.
- Sufficient sleep time was implemented to not overload the server.

**Data Cleaning and EDA**

- Missing values were dropped and so as for duplicate posts.
- The distributions for both yoga and meditation were analyzed by looking into the title/post length etc.
- Summary statistic provided an insight whereby there are high spread in the length of posts but expected.
- Sentiment Analysis was ran to identify overall mood for user on both yoga and meditation.

**Preprocessing and Modeling**

- After preprocessing the combined post and title with stop words, stemming, and lemmatization. We decided to apply lemmatization and stopwords removal as the words are more comprehensible.
- Train test split was applied with stratification on the dataset to minimize the effect of the unbalanced dataset post cleaning.
- For the modelling test, we decided to test logistic regression, naive bayes, random forest, extra trees, adaboost, and svm.
- After running the models with both count vectorizer and tfidf vectorizer respectively, we ranked the models based on the business requirement which is to better classify posts from yoga and meditation via the test score, recall, roc score and f1-score.
- Even with hyperparameter tuning, we have concluded that naive bayes has the best f1-score and recall score which reduced false negative cases even on default params.

**Conclusion and Recommendations**

In conclusion, we have decided that the best model for these 2 subreddit classifications is naive bayes with count vectorizer as it give overall the best test score, recall score and f1-score. This allows us to reduce the potential loss of clients that are already a yoga enthusiast.

Besides maximizing the funds and manpower to classify posts from two different subreddits based on their title and selftext, there are a number of other possible applications for this model.

By looking at the probabilities associated with each post, marketing teams can better appeal to the potential clients when they are promoting to the yoga or meditation users. In fact, this can also be useful as words can be trending with time but withi this model we can accurately ride the trend with words that have high probability of being classified as yoga.

The sentiment analysis we implemented can also determine the mood of the potential clients which either is a positive attraction to yoga or vice versa.

The recommendation we would propose at this point of time for the marketing team is that we can focus on are as follows:

Provide free mat or foam rollers to entice the clients to join yoga especially for those that are already interested in yoga.
Promote body fitness and wellness for those who are both yoga and meditation enthusiast.
Transition the business in a way that also appeal to meditation enthusiast whereby yoga also focuses on breathing regulation and helps to reduce anxiety. The community and people from yoga can also help newcomers settle in easier.


