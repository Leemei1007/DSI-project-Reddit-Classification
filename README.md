# Project 3 - Reddit classification challenge


### Problem statement and objectives

**Problem statement**

- In recent years there has been a surge of forums/discussion/comments among netizens in various social media channels, where a wide range of topics are being discussed.
- As the variety of discussion topics rose substantially, the data science team realise that when compiling information from these netizens, discussion/comments which can be broken down into sub-topics will be more meaningful. For example topics relating to dietary, instead of categorising it broadly as "diet", further breakdowns such as 'plant-based', 'kosher' or 'paleo' will be useful.

**Objectives**

- To develop a classification model which is able to classify/categorise subtopics based on consolidated netizens' comments / discussion. 

- The model should be able to distinguish / classify discussion / comments on topics which are closely related. That's why for a start, the data science team chose streaming services namely, Netflix and AmazonPrimeVideo to train the model. Data is extracted from sub-reddits due to active users on the platform. 

- The model to be shortlisted will be based on various consideration such as accuracy score, strengths and limitations and the selected model will be trained further to include more subtopics

- The model when deployed, may be useful to any user, be it data scientist, marketing team to get insights on which discussion / comment belong which subtopic


### Overall workflow
- The process of developing the model entails the following:
1. Scrape the dataset from Reddit using API pushshifts to train the model
2. Prepping the data, i.e. data processing, inpute the missing values, tokenize, lemmatise and stem the words where required
3. Some preliminary EDA conducted to gauge relationship / insights 
4. Data modelling - 3 models were compared, namely, Logistic Regression, Random Forest and Multinomial Naive Bayes model. Overall, Logistic Regression produces the most accurate results among other models with the worse off being the Naive Bayes model (since its known for its bad estimation anyway). However, after some consideration and judgement, the team has decided to opt for **Random Forest** because: <br><br>- it is more dynamic, i.e. it can classify more categories, <br><br>- can map non-linear relationships - A major limitation of Logistic Regression is the assumption of linearity between the dependent variable and the independent variables. This model is trained based on netizen's statements. As people's behaviour and preference varies, the independent variable (in this case, words used by netizens) and dependent variable (in this case, category) may not necessarily be linear

### Conclusion

#### Observations

- Overall, both Netflix and AmazonPrimeVideo are popular for movies and tv shows
- From this exercise, it is interesting to note that Netflix's personal brand relates to its original tv shows. "Netflix Original" means they either produce or own exclusive streaming rights in a given country
- In my preliminary data exploration, top Netflix words relate to its original tv shows.

#### Limitations

- The model has to be trained frequently (and hence, costly to maintain) on latest trends or hot topics. As we can observe in the r/Netflix, there are words which appear to be latest tv shows. As time goes by, such tv shows may not be mentioned much. 

#### Recommendation
- The Random Forest model may be deployed to classify consolidated comments/discussions from various social media into subtopics because it is able to classify various categories

- Despite the limitations, the model is still useful to give users, namely data scientist, marketing team some guide

#### Future steps

Train the model with more data so that it can classify more subtopics other than the current Netflix and AmazonPrimeVideo
