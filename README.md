# Credit_Risk_Analysis

## Overview

Credit Risk Analysis is a very large and very important data analytics specialty. Banks and credit card companies need to be able to evaluate potential prospects in order to decide if they pose any sort of risk of defaulting on payments. If the credit issued is substantial, then the risk of default could be extremely costly to a bank or credit card. There are many different ways to build models in order to be able predict whether or not to approve an application. Using machine learning types of analysis are increasingly popular as they can adapt to changes in consumer behavior and make accurate predictions without having to start building the model from scratch. 

No one algorithm or model is perfect, so in this analysis, we compare a couple of different types of supervised machine learning in order to train a model that fits these needs in the best manner. This involves oversampling, undersampling, bagging, boosting, etc in order to find a way to minimize approving applicants that are indeed risky. 

## Results
* **Naive Random Oversampling**
![Naive Random Oversampling](https://user-images.githubusercontent.com/109319148/202930286-6fd30152-ad39-4144-ac43-13e07652280f.png)
    * Balanced accuracy score is 64%. The precision is quite low at 1% with recall at 69%. In our analysis, recall is important as false negatives are harmful and costly
    
* **Smote Oversampling**
![SMOTE](https://user-images.githubusercontent.com/109319148/202931028-d75cabb3-96ed-4496-8460-6f7190407d52.png)
    * In our Smote analysis, our balanced accuracy score goes up slightly to 66%, while our precision score stays at 1% and our recally is at 63%.
    
* **UnderSampling**
![UnderSampling](https://user-images.githubusercontent.com/109319148/202931298-9c641454-6133-443c-a045-2e040cda077f.png)
    * UnderSampling brought our accuracy score down to 54%. Our precision score is still at 1% and our recall went back up to 69%
    
* **Combination Sampling**
![Combination](https://user-images.githubusercontent.com/109319148/202931426-79b518c7-e89b-4267-911e-3a735f120bc2.png)
     * Combination of Over Sampling and Under Sampling brought our accuracy score up to 67%, our precision stayed at 1% and the recall went up to 76%, which was a good           improvement.

* **Balanced Random Forest Classifier**
![Random Forest](https://user-images.githubusercontent.com/109319148/202931936-407782eb-7191-4635-8af9-aef035e062f7.png)
      * These models are performing very differently with an accuracy score of almost 68%. The Precision score has gone up to 88%, but the recall score is down to only 36%. We want recall to be higher, since false negatives are very indeed credit risks and detrimental to our goal.
      
* **Ensemble Classifier**
 ![ensemble](https://user-images.githubusercontent.com/109319148/202932080-5c55aee3-f5cc-4683-a963-f141d50834ec.png)
      * The ensemble classifier did quite well with an accuracy score of 93%, a precision score of 9%, and most importantly, a recall score of 92%.
      
      
## Summary 
When looking at the accuracy score, this is just telling us how often our model is telling us if we got the prediction right. This is very important, as accuracy is never not important. It just isn't always the MOST important factor. In this case, accuracy in flagging all applicants that do pose risk is more important than accidentally flagging non risky applicants as risky. With further scrutiny, these could be appealed and granted. The danger really lies in approving a risky applicant and later having them default. So, if we fail to flag or have false negatives, these are what we want to avoid. The metric that tells us this is our Recall score. 

The Ensemble Classifier had the higherst accuracy and the highest recall score. However, if I were an institution looking for a credit risk model, I would want a model that identifies closer to 95-98% of risky applicants. This is also not great since you are missing approving some applicants and money making opportunities by flagging them as potentailly faudulent. We probably need to re look at the factors involved in the model and other data possibly available. 
