# Machine_Learning_Final
my Final Project for my Machine Learning class 


##Explanation

Link to Dataset used: https://www.kaggle.com/datasets/rashikrahmanpritom/heart-attack-analysis-prediction-dataset/discussion?select=heart.csv
I got the dataset off of Kaggle.

The data contains the follwoing columns: age, sex, cp, trtbps, chol, fbs, restecg, thalachh, exng, oldpeak, slp, caa, thall, and output. 

the Problem I will be trying to solve is to find the best algorithm to classify whether or not a person is at a high risk of heart attacks. The target variable for this experiment is going to be output, which states whether or not a person is at a high or low risk of a heart attack, where 1 = high risk and 0 = low risk.


##Findings
I Discovered That the best algorithm for this dataset was a Random Forest agorithm, however I would not have known that if I just ran the basic function for each of these and then tuned the best algorithm. The best RF I came up with had a random_state of 3 and the # of estimators set to 8. I was surprised by this because my gut intuition with this dataset was that it would be easily seperable and would work best with somethign like an SVC, but that was not the case.

The worst algorithm was the SVC, which I thought would be the best, I'm assuming that the reason SVC performed so poorly is that the data isn't easily seperated. This was also a problem I remembered SVMs having in assignment 05 as well. I also noticed that changing C and the Gamma of the algorithm had no influence on the accuracy.

I was able to increase the accuracy of my SGD, but not enough to out perform my tuned random forest algorithm. I found that by using the following parameters I was able to increase the accuracy: random_state = 0, penalty = "l1", loss = "log", learning_rate = "constant", eta0 = .5, max_iter = 7 .

Both the Perceptron and the MLP worked ok, but changing parameters also only lowered their accuracy, like the SVC.
