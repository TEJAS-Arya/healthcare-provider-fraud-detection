# healthcare-provider-fraud-detection

Introduction:
What is Healthcare Fraud?
Fraud is defined as any deliberate and dishonest act committed with the knowledge that it could result in an unauthorized benefit to the person committing the act or someone else who is similarly not entitled to the benefit. Healthcare fraud is one of the types of fraud. Here we will analyze and detect “Healthcare Provider Fraud” where the provider fills all the details and makes a claim on behalf of the beneficiary. Provider Fraud is one of the biggest problems that Medicare is facing currently. Healthcare fraud is an organized crime which involves peers of providers, physicians, beneficiaries acting together to make fraud claims. As per the U.S. legislation, an insurance company should pay a legitimate healthcare claim within 30 days. So, there is very less time to properly investigate this. Insurance companies are the most vulnerable institutions impacted due to these bad practices. As per the Government, the total Medicare spending increased exponentially due to frauds in Medicare claims.

Healthcare fraud and abuse take many forms. Some of the most common types of frauds by providers are: a) Billing for services that were not provided. b) Duplicate submission of a claim for the same service. c) Misrepresenting the service provided. d) Charging for a more complex or expensive service than was actually provided. e) Billing for a covered service when the service actually provided was not covered.

Business Problem:
Statistics shows that 15% of the total medicare expense are caused due to fraud claims. Insurance companies are the most vulnerable institutions impacted due to these bad practices. Insuarance premium is also increasing day by day due to this bad practice.

Our objective is to predict whether a provider is potentially fraudulent or probability score of that provider's fradulent activity and also find the reasons behind it as well to prevent the financial loss.

Depending on the probability score and fradulent reasons insurance company can accept or deny the claim or set up an investigation on that provider.

Find out the important features which are the reasons behind the potentially fraudlent providers. Such as if claim amount is high for a patient whose risk score is low, then it is suspicious.

Not only the financial loss is a great concern but also to protect the healthcare system so that they can provide quality and safe care to legitimate patients.

ML Formulation:
Build a binary classification model based on the claims filled by the provider along with Inpatient data, Outpatient data, Beneficiary details to predict whether the provider is potentially fraudulent or not.

Business Constraints:
Cost of misclassification is very high. False Negative and False Positive should be as low as possible.If fraudulent providers are predicted as non-fraudulent (False Negative) it is a huge financial loss to the insurer and if legitimate providers are predicted as fraudulent (False Positive) it will cost for investigation and also it's a matter of reputation of the agency.
Model interpretability is very important because the agency or insurer should justify that fraudulent activity and may need to setup a manual investigation. It should not be a black box type prediction.
Insurer should pay the claim amount to the provider for legitimate claims within 30 days. So, there is no such strict latency constraints but it should not take more than a day because depending on the output of the model the agency may need to setup an investigation.


Objective
Identify fraudulent claims:

To protect the insurance providers from great loss due to this bad practice.
To protect the healthcare systen so that they can provide quality and safe care to legitimate patients.
To reduce the cost of healthcare services.



Performance Metric:
1. AUC score 2. F1 Score 3. Confusion Matrix 4. Check FPR and FNR separately
Train-Test Split and Oversampling:
As our dataset is imbalanced Legitimate:Fraudulent = 90:10, I need to do oversampling. First I will split the data into Train and Test (Because if oversampling is done first, crossvalidation may contain train data) then I will do oversampling to make 4 sets of data with ratio 80:20, 75:25, 65:35 and 50:50.

Model Selection and Approach to be followed:
I will use Logistic Regression, Decision Trees, Naive Bayes and SVM for this classification task. For each model, I will do 5 fold cross validation for 10 times then I will take the average. I will compare the scores and pick the best model.

I will do further hyperparameter tuning to get better score.

For further improvement I will use ensemble models.
