# Overview of the analysis
The purpose of this analysis is to evaluate the effectiveness of different supervised machine learning algorithms to predict risk. Identifying an effective algorithm can help create a quicker and more reliable lending experience. It can also assist with more accurately identifying ideal loan candidates, which in turn will reduce default rates. 

To accomplish this, we used a common set of data and selected six different machine learning models. Each model was trained on the data, and the results from each one was compared. Based on the balanced accuracy precision, and recall scores of each model, we will make a recommendation on which (if any) is best suited for the task. 

# Results
Below is a list of each algorithm that was used, along with a screenshot of the results. 

* RandomOverSampler
[RandomOverSampler](Resources/RandomOversampler.PNG)
	* RandomOverSampler received an accuracy score of 64.9%. 
	* The precision for high-risk applicants was 1%, and for low-risk applicants was 100%.  
	* The recall score of 73% for high-risk applicants and 57% for low-risk applicants.

* SMOTE
[SMOTE](Resources/SMOTE.PNG)
	* SMOTE received an accuracy score of 65.8%.
	* The precision for high-risk applicants was 1%, and for low-risk applicants was 100%. 
	* The recall scores for both categories were similar, at 63% for high-risk applicants and 68% for low-risk applicants.

* ClusterCentroids
[ClusterCentroids](Resources/ClusterCentroids.PNG)
	* ClusterCentroids received an accuracy score of 65.8%. 
	* The precision for high-risk applicants was 1%, and for low-risk applicants was 100%. 
	* The recall score for high-risk applicants was 69%, and for low-risk applicants was 40%. 

* SMOTEENN
[SMOTEENN](Resources/SMOTEENN.PNG)
	* SMOTEENN received an accuracy score of 54.4%. 
	* The precision for high-risk applicants was 1%, and for low-risk applicants was 100%. 
	* The recall score for high-risk applicants was 57%, and for low-risk applicants was 72%. 

* BalancedRandomForests
[BalancedRandomForests](Resources/BalancedRandomForests.PNG)
	* BalancedRandomForests received an accuracy score of 77.3%.
	* The precision for high-risk applicants was 3%, and for low-risk applicants was 100%. 
	* The recall score for high-risk applicants was 66%, and for low-risk applicants was 88%. 

* EasyEnsembleClassifier
[EasyEnsembleClassifier](Resources/EasyEnsembleClassifier.PNG)
	* EasyEnsembleClassifier received an accuracy score of 93.2%. 
	* The precision for high-risk applicants was 9% and for low-risk applicants was 100%. 
	* The recall score for high-risk applicants was 92% and for low-risk applicants was 94%. 

# Summary
## Final Results
The first four algorithms either employed oversampling, under sampling, or a combination of the two. The last two algorithms utilized ensemble classifiers. None of the models were able to achieve a high degree of precision when it came to correctly classifying high risk applicants. The only two models that correctly identified more than 1% of the high-risk applicants were the two ensemble classifiers. 

In terms of accuracy scores, the ensemble classifiers also fared better than the ones using sampling techniques. Overall, SMOTEENN performed the worst and EasyEnsembleClassifier performed the best. 

## Recommendations
Based on the results, EasyEnsembleClassifier was the most accurate. However, I would stop short of recommending this model. It still had a lot of trouble accurately identifying high risk applicants. It could be possible that this is lower than the current accuracy rate (assuming the applications are reviewed and approved/denied by humans). If so, then this would not be a good model to use. If this is a more accurate predictions than each application being reviewed individually, then it might be a good start. I would still advise testing other models to find one that is able to more accurately identify high risk candidates.
