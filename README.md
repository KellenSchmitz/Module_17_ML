# Module_17_ML
### Overview: Supervised Machine Learning for Credit Card Risk


Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Employ different techniques with unbalanced classes using imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. And finally, we compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.


ML Models Used:
1) RandomOverSampler
2) SMOTE
3) ClusterCentroids
4) SMOTEENN
5) BalancedRandomForestClassifier
6) EasyEnsembleClassifier


## Results

1) RandomOverSampler
![image](https://user-images.githubusercontent.com/86166117/143131189-54345940-2044-4525-b70a-0f4ac00d80f9.png)
   * Balanced Accuracy Score: 0.62155
   * Precision: 
     * High Risk:  1.00
     * Low Risk:  0.01
   * Recall (sensitivity):  
     * High Risk:  0.54
     * Low Risk: 0.70
     


2) SMOTE
![image](https://user-images.githubusercontent.com/86166117/143131395-68768e36-ecf9-407b-b95b-5bb19a082298.png)
   * Balanced Accuracy Score: 0.6324840559040494
   * Precision: 
     * High Risk:  1.00
     * Low Risk:  0.01
   * Recall (sensitivity):  
     * High Risk: 0.63
     * Low Risk: 0.63

3) ClusterCentroids (undersampling)
![image](https://user-images.githubusercontent.com/86166117/143131451-4a63ca1c-a510-4e71-b313-e18cac36973f.png)
   * Balanced Accuracy Score: 0.5118790061681392
   * Precision: 
     * High Risk:  1.00
     * Low Risk:  0.01
   * Recall (sensitivity):  
     * High Risk: 0.59
     * Low Risk: 0.44

4) SMOTEENN (Combination (Over and Under) Sampling)
![image](https://user-images.githubusercontent.com/86166117/143131503-d96daafc-081d-4c0a-bfbe-0ee02e623c33.png)
   * Balanced Accuracy Score: 0.6561312754068112
   * Precision: 
     * High Risk:  1.00
     * Low Risk:  0.01
   * Recall (sensitivity):  
     * High Risk: 0.75
     * Low Risk: 0.57

5) BalancedRandomForestClassifier
![image](https://user-images.githubusercontent.com/86166117/143131801-702bb0c9-d960-45d8-b4d1-a02656fa964e.png)
   * Balanced Accuracy Score: 0.8020001128072487
   * Precision: 
     * High Risk:  1.00
     * Low Risk:  0.01
   * Recall (sensitivity):  
     * High Risk: 0.70
     * Low Risk: 0.90


6) EasyEnsembleClassifier
![image](https://user-images.githubusercontent.com/86166117/143135221-c4b3b227-5e4b-4c07-bc02-fb443e13caab.png)

   * Balanced Accuracy Score: 0.7416600714093861
   * Precision: 
     * High Risk:  0.02
     * Low Risk:  1.00
   * Recall (sensitivity):  
     * High Risk: 0.71
     * Low Risk: 0.79


## Summary
The imbalanced nature of the data (with only 347 high risk loans out of 68,817) is a challenge for simpler RandomOverSampler, SMOTE, ClusterCentroids, and SMOTEENN algorythms. The prediction outcomes of the BalancedRandomForestClassifier and EasyEnsembleClassifier improves, but there are still a significant number of false positives from both models. 

*Recommendation* Becuase of the high number of false positives, even with the best improved outcomes of models 5 and 6, we do not recomend their use as a primary credit risk screening tool. It may be that with a larger data set, the models could be improved, but at this point it would be better to use the best model, EasyEnsembleClassifier (based on true positive), as a secondary tool to identify loans that may need further review.  




