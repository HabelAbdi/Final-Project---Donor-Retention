# Final-Project-Charity Donor Churn Prediction

## Overview

This project aims to address challenges faced by charities regarding donor churn. Donor churn is the phenomenon where individuals cease their contributions to a charity. By leveraging data science techniques, I aim to help predict and understand donor behavior to aid charities in tailoring engagement strategies.


Charities encounter difficulties in: 

## 1. Accessing clean and usable data for analysis.
   
Background:
Charities accumulate a vast amount of data, including donor information, contributions, engagement metrics, and other relevant details. However, the quality of this data is crucial for meaningful analysis and decision-making

Data Quality Issues: 
The data collected by charities may have various issues such as missing values, inaccuracies, inconsistencies, or duplications. These issues can arise due to manual errors, system glitches, or gaps in data collection processes.

Unstructured Formats: 
Data might be stored in unstructured formats, making it challenging to extract valuable insights. For example, donor addresses might be entered in various formats, or donation amounts may be recorded inconsistently.



Why is Clean Data so Important?
Effective Analysis: Clean and well-structured data is essential for accurate and effective analysis. Analysts need reliable data to draw meaningful conclusions and insights.

Robust Models: Data quality directly impacts the performance of machine learning models. Models trained on clean data are more likely to generalize well to new, unseen data.

Trustworthy Insights: Clean data instills confidence in the insights derived from analysis. Decision-makers can trust the information presented, leading to more informed and confident decisions.

What's the need for Regular Data Upkeep?

Regular Maintenance: Charities need to engage in regular data maintenance activities to ensure data cleanliness. This involves identifying and rectifying errors, handling missing values, and standardizing formats.

Data Preprocessing: Before analysis, data preprocessing steps may include normalization, scaling, or transforming variables to make them suitable for modeling. This ensures that the data is in a form that algorithms can effectively process.

What does all this get a Charity?
Efficiency: Analysts can work more efficiently with clean data, focusing on analysis and interpretation rather than spending time addressing data quality issues.

Reliable Results: Clean data produces reliable and reproducible results, reinforcing the credibility of the analyses and insights generated.

Summary: 
The process of accessing clean data involves addressing data quality issues and ensuring that the data is structured and prepared for analysis. This is a foundational step for charities seeking to derive meaningful insights from their donor data.







## 2. Analyzing non-linear relationships in donor data.
   
Background:
Large charities often accumulate a vast amount of data regarding their donors, capturing various attributes or features related to donor behavior, contributions, engagement, and other relevant factors. Traditional data analysis methods might focus on simple or linear relationships between these variables. For instance, one might examine how an increase in one variable, like the frequency of donations, linearly correlates with another variable, such as total donation amounts.

Examples of Non-Linear Relationships:
Diminishing Returns: As the frequency of donations increases, the impact on total donation amounts might exhibit diminishing returns. Initially, more frequent donations could lead to a substantial increase in total contributions, but there may be a point where additional donations result in smaller incremental gains.

Threshold Effects: There could be a specific threshold for certain donor characteristics, beyond which the impact on engagement or contribution levels sharply changes. For instance, the effect of donor age on engagement might significantly differ for donors below and above a certain age threshold.

Importance of Exploring Non-Linear Relationships:
Improved Predictions: Analyzing non-linear relationships allows for more accurate predictive models. Linear models might overlook patterns that significantly influence donor behavior.

Tailored Engagement Strategies: 
Understanding non-linear relationships helps in crafting more targeted and effective engagement strategies. For instance, recognizing a point of diminishing returns might influence decisions on how often to reach out to donors.

Enhanced Decision-Making: 
Insights from non-linear relationships empower charities to make informed decisions about resource allocation, communication strategies, and donor retention efforts.

Summary
Exploring non-linear relationships in donor data enables charities to unearth hidden patterns and nuances, leading to more precise predictions and tailored strategies for donor engagement and retention.



## 3. Retaining and engaging donors effectively.
   
Background:
Charities encounter challenges in retaining and engaging donors effectively. This involves understanding and addressing the factors that influence donor loyalty and participation. Traditionally, strategies have often been linear and straightforward, focusing on general outreach rather than delving into the nuanced, non-linear aspects of donor relationships.

The Challenge:
Donor retention is a multifaceted task that goes beyond simple, linear approaches. The complex and non-linear nature of donor behavior requires a more nuanced understanding to tailor engagement strategies effectively.

Examples of Non-Linear Considerations:

Diminishing Engagement Returns:

Scenario: Frequent outreach may not continually increase donor engagement.
Implication: Identifying a point of diminishing returns can guide decisions on the optimal frequency of communication to maintain engagement.
Thresholds for Personalization:

Scenario: There could be specific thresholds in donor characteristics that trigger changes in engagement levels.
Implication: Personalization efforts need to consider these thresholds to ensure impactful and relevant interactions.

Importance of Exploring Non-Linear Aspects:

Precision in Engagement:

Advantage: Understanding non-linear relationships allows for more precise tailoring of engagement efforts, ensuring activities are aligned with donor preferences.
Anticipating Changing Engagement Dynamics:

Advantage: Recognizing thresholds and non-linear patterns enables charities to anticipate shifts in donor engagement, adjusting strategies accordingly.
Strategic Resource Allocation:

Advantage: Non-linear insights empower charities to allocate resources strategically, focusing efforts where they are most likely to yield positive donor responses.

Summary:
Effectively retaining and engaging donors requires acknowledging and navigating the non-linear dynamics inherent in donor relationships. By doing so, charities can move beyond conventional strategies, providing a more personalized and responsive donor experience, and ultimately fostering long-term donor loyalty.



## Project Phases

### 1. Exploratory Data Analysis (EDA)

Conducted in-depth EDA to unveil patterns and crucial features. Analyzed for outliers, and nulls, and described the data distribution.

### 2. Feature Engineering

Searched for any need for new features based on data analysis to enhance model performance.

### 3. Model Development

Chose three models, selected the best-performing, and performed hyperparameter tuning for optimization.

### 4. Model Interpretation

Interpreted the model's predictions and related insights to actionable strategies for reducing churn.

### 5. Results Comparison

I Compared the results of the original model with tuned versions, highlighting trade-offs made during hyperparameter tuning.

## Model Metrics

+-------------------+----------+--------+---------+---------+
| Metric            | Original | Tuned 1| Tuned 2 |  Model  |
+-------------------+----------+--------+---------+---------+
| Accuracy          | 0.900    | 0.883  | 0.889   |   GB    |
| Precision         | 0.769    | 0.739  | 0.773   |   GB    |
| Recall            | 0.625    | 0.531  | 0.531   |   GB    |
| F1 Score          | 0.690    | 0.618  | 0.630   |   GB    |
| ROC AUC Score     | 0.792    | 0.745  | 0.749   |   GB    |
+-------------------+----------+--------+---------+---------+

## Key Metric Explanations & Interpretations

Accuracy:

Explanation: Accuracy represents the overall correctness of the model's predictions.
Charity Context: A high accuracy indicates the percentage of correct predictions among all instances. However, in the context of donor churn, it may not be the sole metric to rely on. For example, a high accuracy could result from a model that predominantly predicts non-churning donors, potentially missing critical instances of churn.
Precision:

Explanation: Precision measures the accuracy of positive predictions made by the model.
Charity Context: Precision is crucial for the charity to minimize false positives. In the context of donor churn, high precision means that when the model predicts a donor is likely to churn, it is likely correct. This is important for resource allocation, as reaching out to donors requires time and effort.
Recall:

Explanation: Recall measures the ability of the model to capture all positive instances.
Charity Context: Recall is vital for the charity to minimize false negatives. In the context of donor churn, high recall indicates that the model is effective at identifying most actual churning donors. Missing a donor who is likely to churn could result in a loss of contributions, making recall crucial for proactive engagement.
F1 Score:

Explanation: The F1 score is the harmonic mean of precision and recall.
Charity Context: The F1 score provides a balanced measure that considers both false positives and false negatives. It's particularly relevant for the charity to strike a balance between identifying actual churning donors (recall) and ensuring the predictions are accurate (precision).
ROC AUC Score:

Explanation: ROC AUC (Receiver Operating Characteristic Area Under the Curve) evaluates the model's ability to distinguish between classes.
Charity Context: ROC AUC score is significant for the charity as it assesses the model's capability to differentiate between donors likely to churn and those likely to stay. A higher ROC AUC score indicates better discrimination and, consequently, a more effective model.

Understanding these metrics in the charity context helps align the model evaluation with the organization's goals and priorities in managing donor churn effectively.


## Overall
The original model showed strong performance across various metrics. However, hyperparameter tuning introduced trade-offs, affecting precision, recall, and F1 score. The charity needs to carefully assess these results based on its specific goals and preferences regarding donor engagement and retention strategies.

For instance, some charities might prioritize limiting false positives, ensuring that when the model predicts a donor is likely to churn, it is highly accurate. This approach is crucial when reaching out to donors demands significant resources or when the charity wants to be confident about the accuracy of its predictions. Also, it would look bad on the charity if they reached out to a donor who had no intentions of churning,  but due to this miscalculation, they are considering it and now have a sour taste of being categorized as a churner. On the other hand, some charities might focus on minimizing false negatives, ensuring that most actual churning cases are identified. This strategy is important when missing a donor who is likely to churn has significant consequences. The decision between these two approaches depends on the charity's unique context and objectives in managing donor relationships. This addition emphasizes the importance of tailoring the model evaluation based on the specific goals and operational considerations of the charity.



## Areas for Improvement and Future Work:

Hyperparameter Tuning: Further exploration of hyperparameter tuning strategies could be beneficial to identify an optimal configuration for improved model performance.

Data Quality: Continuous efforts to ensure data cleanliness and relevance are crucial. Implementing regular data cleaning processes and addressing any anomalies could enhance model robustness. Also, this dataset was not only an incomplete dataset, but it was also not a typical dataset presented by charities. Most charities would have far more features along with those features having greater significance over the variability and feature importance.

Feature Importance: Regularly reassessing feature importance is essential, as donor behavior might evolve. Incorporating new relevant features and reevaluating existing ones can contribute to model accuracy. There weren't many opportunities to combine or create special or unique features by combining original ones. The creation or combination of features plays a significant role in the path that the metrics of each model takes along with the type of problem it solves. 

Model Evaluation Metrics: Depending on the charity's evolving goals, reassessing the importance of metrics like precision, recall, and ROC AUC score should be an ongoing process. Adjusting the evaluation criteria can align the model with the charity's changing priorities.

## Contributions

Feel free to contribute to this project! Whether it's fixing bugs, improving documentation, or adding new features, your help is appreciated.


