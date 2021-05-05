# Classification-based Sentiment Analysis (NLP)

## ***Goal:*** 
Classify sentiment as positive or negative for a mixed dataset of customer reviews. Natural language processing exercise.

## ***Initial subject matter understanding:***
Language is extremely complex to break down for natural language processing exercises. That is why transformers are becoming extremely popular in the deep learning space since transformers are able to identify context. For the purposes of this classification exercise, there will likely be challenges with irony, sarcasm, ambiguity, errors in spelling or grammar, slang, and more.

## ***Initial thoughts on dataset before preprocessing:***
It will be important to normalize the character case. Since the dataset is relatively small, it may be possible to run a simple spell check - however, spell checks aren't viable with big data since it is too slow to process. I also plan to apply removal of stop words, apply lemmatization, and TF-IDF vectorization.

## ***Approach:***
I applied stratified k-fold cross validation and the respective grid searches for hyper parameter tuning on Random Forest, KNN, Decision Trees, and SVM.

## ***Results:***
A tuned random forest model nets an accuracy of 0.77 and F1 Score of 0.76. 

Please note: at the bottom of the notebook file, I analyze five (5) examples of where the classification went wrong. 

Example 1: "See it.", Predicted=0, Actual=1, (index=93)

Example 1 demonstrates a one-off error and how tricky language is due to meaning and quality. 'See it' is ambiguously describing a command to watch a film with a subtle inference that it worth watching. This is extremely challenging to capture in sentiment analysis and is also a rare example of a review.

## ***Technology used:***
Google Colab, Pandas, Numpy, Sklearn, nltk, beautifulsoup, autocorrect
