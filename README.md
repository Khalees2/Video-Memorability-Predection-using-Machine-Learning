# Video-Memorability-Predection-for-MediaEval-2018-using-Machine-Learning

MediaEval 2018 is a competition which took place at France, Sophia Antipolis and EURECOM in October 2018. This competition had various tasks and predicting media memorability is one among those. Memorability can be defined as how good or bad a person can remember any video after a specified period of time. This is a part of MediaEval 2018 Benchmarking Initiative for Multimedia Evaluation. I will be predicting the probability of video getting remembered based on the given set of pre-computed features.

# Assignment Problem Statement
Predict short-term and long-term memorability scores using either the video features like C3D, HMP or semantic feature like the captions (text explaining the video content).

# Dataset
In this work, we were given a development dataset having 6000 rows where each row corresponds to a video along with the Short-term Memorability scores, Long-term memorability scores and number of annotations which represents the number of people participated in the experiment. 80% of the dev-set was divided to train our model and rest was used for testing. Later a Test dataset features was released on which we have to predict both Short-term and Long-term memorability scores.

# Features and Classifiers
We have used the following features: Captions, C3D and HMP for this work. Random Forest (RF) and Support Vector Regressor (SVR) Machine Learning models from Scikit-learn were used to predict the memorability scores. In the first approach, only Captions were used in which each caption was converted into Bag of words using CountVectorizer from Scikitlearn. In the second approach only C3D features were used. In the third approach Captions and C3D features were flattened into one single vector similarly Captions, C3D and HMP features were also combined and used.

# Results
Please see the report for the results acheived by classifiers

# Conclusion
Our results show that, Captions alone yield the best results compared to other features especially for Short-term memorability
score prediction. It is also notable that short term predictions are always better than Long-term because, number of annotations which represents the people participated in the Long-term experiments when collecting data is less because the data was collected after two days and people hardly came to participate. From this observation we can say, less the number of people, bad the results. For example, if the experiment is conducted on ten people who have incredible memory power then obviously, they tend to remember everything, and memorability score would increase. It is also notable from the results that SVR achieved better results for Long-term predictions than others. However, the difference is very small when compared to RF. Overall, we can say that using only Captions when predicting the memorability scores would yield better results than any other features.
