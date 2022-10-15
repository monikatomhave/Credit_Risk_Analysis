CREDIT RISK ANALYSIS

OVERVIEW:  
The purpose of this analysis is to run different classifier algorithms on the same data set and to then determine, if any of the classifier algorithms give us a better accuracy measure of the data being analyised over the other algorithms. So comparing undersampling with ClusterCentroid, oversampling with RandomOVerSampler and SMOTE, combination of over and undersampling  with SMOTEEEN, and then also two other machine learning models, BalancedRandomForestClassifier and EasyEnsembleClassifier, to reduce and bias about predicting credit risk.  Should any of these models be used to predict credit risk?

RESULTS:
The Balanced Accuracy Score tells us the percentage of predictions that are correct.
        BA% for RandomOversampling:     64.6%
        BA% for SMOTE Oversampling:     65.86%
        BA% for Cluster Undersampling:  65.86%
        BA% for Combingation SMOTEEN:   54.4%
        BA% for Random Forest:          68.3%
        BA% for Easy Ensemble:          68.8%
The best model is Easy Ensemble with the highest percentage of 68.8%. For the sake of not losing money, I think the percentage of predictions that are correct needs to be higher.  

         
Precision tells us how reliable a positive classification is. All the models give us a precision of 100% for the low-risk applicants. There is a 1% for the high-risk applicants in all but the Random Forest and Easy Ensemble classifiers, they held an 88% precision. The first four models are not good at predicting the high-risk applicants and that is not good for business because if you give credit to people with a high risk of not paying their bill the company will lose money.

Recall (Sensitivity) indicates the ability of the classifier to find all positive samples. 

        recall % for RandomOversampling:     high: 71%     low: 58%
        recall % for SMOTE Oversampling:     high: 63%     low: 68%
        recall % for Cluster Undersampling:  high: 69%     low: 40%
        recall % for Combingation SMOTEEN:   high: 73%     low: 60%
        recall % for Random Forest:          high: 37%     low: 100%
        recall % for Easy Ensemble:          high: 38%     low: 100%

Looking at the recall numbers, all the models did better at finding the high-risk applications with the SMOTEEN model generating the best results at 73% for high-risk. Random Forest and Easy Ensemble both at 100% for low-risk.

SUMMARY:
Overall, Recall seems to be the most important because it is better even if it means a certain number of false positives, than to miss those with a high-risk. Essentially, highly sensitive test and algorithms tend to be aggressive as they do a good job of detecting the intended target, even if that means they result in a number of false positives. In this case, I think it is better to have false positives than not because you really want to target the high-risk applications. The false positives in a highly sensitive test are accepted as a cost of doing business.
