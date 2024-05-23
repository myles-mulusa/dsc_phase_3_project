# SyriaTel Company Customer Churn Prediction


## Overview

![image](https://github.com/myles-mulusa/dsc_phase_3_project/assets/151248454/75b7f4d7-b17c-42af-af17-6251a80d9f81)


Customer churn refers to the process where customers stop using a company’s services, either due to dissatisfaction or the availability of better alternatives from competitors at lower prices. This can lead to substantial revenue and profit losses.

Accurately predicting customer churn can enhance retention rates, boost market share, and improve overall business performance.


## Business/Data Understanding

This data was obtained from kaggle , [https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset).

We began by individually examining each predictor variable, focusing on their characteristics and distributions. During the data preparation phase, we meticulously cleaned the data as documented step-by-step in the notebook. We conducted univariate analysis to understand the distribution of each individual variable, followed by bivariate analysis to compare these variables against our target variable, churn. This helped us understand how the target variable is distributed across the predictor variables.

We also examined the relationships between variables. Categorical variables were converted to numerical format for modeling purposes. The data was then split into training and testing sets, allowing us to train the model on the training set and evaluate it using the testing set. Various classification algorithms were applied to the data, and since many of these algorithms require data scaling, we standardized the predictor variables in both the training and testing sets.

The stakeholder audience for this project involving SyriaTel's customer churn includes Senior Management who are responsible for the overall strategy and performance of the company, Marketing Team who are responsible for customer acquisition, retention, and engagement, Customer Service Department who interact directly with customers and can use churn insights to proactively address customer issues, Product Development Team who are responsible for meeting customer needs better, and Board of Directors: They oversee the company’s strategic direction and performance, needing high-level insights to ensure the company is on track to meet its goals.


## Modeling

Our goal in this section is to develop a predictive model capable of accurately identifying customer churn based on the features available in our dataset. Our primary evaluation metric will be the recall score, with a target of achieving 80% or higher to meet project requirements.

To achieve our objectives, we will employ the following algorithms:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. XG Boost

Additionally, we will evaluate the performance of our models using the ROC_AUC metric.

Given the class imbalance in our dataset, we will address this issue by utilizing SMOTE (Synthetic Minority Over-sampling Technique) to generate synthetic examples of the minority class, thereby balancing the dataset and improving the model's ability to capture patterns associated with churn.

The XGBoost classifier model showcases a remarkable recall score of 0.77, surpassing the performance of all prior models. This implies that the model adeptly identifies approximately 77% of the actual positive instances.


## Evaluation

Our primary evaluation metrics will be the recall score and ROC_AUC. We shall assess multiple models using these metrics and select the top two performers for further tuning to enhance their performance.

The XGBoostClassifier achieved the highest recall score, followed by the RandomForestClassifier and LogisticRegression. The DecisionTreeClassifier, on the other hand, attained the lowest recall score of 0.73.

The analysis of the ROC curves reveals that the XGBClassifier exhibits the most favorable performance, followed by the RandomForestClassifier, DecisionTreeClassifier, and LogisticRegression respectively. Specifically, the XGBClassifier achieves the highest AUC score of 0.884, while the LogisticRegression attains the lowest AUC score of 0.79.


## Conclusion

It's commendable that despite achieving a respectable recall score of 79% with our XGB classifier, there's acknowledgment of the potential for further improvement through additional feature engineering. This recognition underscores a commitment to refining the predictive model and maximizing its effectiveness in identifying customers at risk of churn. 

Despite not achieving an ideal recall score, meeting the primary objective of predicting customer churn while maintaining an acceptable level of performance demonstrates the efficacy of the methodologies employed. With more time and continued iteration, there's optimism for even greater refinement and enhancement of the model, ultimately contributing to more proactive churn management strategies and sustained business success.

## Next Steps

Employee Training and Engagement: Invest in employee training and engagement programs to ensure that frontline staff are equipped to address customer concerns and deliver exceptional service. Empowered and motivated employees play a crucial role in retaining customers and fostering long-term relationships.

Market Research and Competitor Analysis: Stay informed about market trends, competitor offerings, and evolving customer preferences through ongoing market research and competitor analysis. This insight can help SyriaTel stay ahead of the competition and adapt its strategies to meet changing customer needs.

Continuous Monitoring and Evaluation: Continuously monitor and evaluate the effectiveness of retention strategies and predictive models. Regularly review key performance indicators such as churn rate, customer lifetime value, and customer satisfaction scores to assess the impact of implemented initiatives and adjust strategies as needed.

By implementing these recommendations and next steps, SyriaTel can improve its customer retention efforts, reduce churn, and ultimately enhance its competitiveness and long-term sustainability in the telecommunications industry.


Repository Structure

├── LICENSE.md                           <- The license for the project 

|
├── README.md                            <- README for reviewers of this project

|
├── notebook.ipynb                       <- Analysis in Jupyter Notebook

|
├── presentation.pdf                     <- PDF version of the presentation

|
├── SyriaTelCustomerChurn.csv            <- Dataset used in the analysis 

|
└── notebook.pdf                         <- PDF version of project write up
