# Predicting US Visa availability

## Background
* The solution is based on the F1 Visa slot availability dataset provided by Checkvisaslots. 
* Checkvisaslots is a Chrome extension that aspiring students use to check for visa slots availability without having to log into the visa portal. This is useful because users who exceed the daily login limit will be locked out for 72 hours. 
* The tool shows visa slot availability based on whether other users found a slot or not while they logged in. This helps users avoid excessive login attempts which can lock them out.
* When a user logs in, the extension collects data from the slot availability page such as consulates where the slots are available and dates when they are available.

## Problem
* Many aspiring students were facing issues with finding visa interview slots to attend their university.
* Students had to rely on Telegram groups which had hundreds of thousands of students competing for limited visa slots.
* It is very common to see wait times for appointment go later than the class start date and many students have had to defer their admission due to this issue.
* Students have also been locked out of their appointment portal due to logging in too many times, which is a limitation set by USCIS to curb agent and bot intervention. As a result, many have agonizingly missed booking visa slots even though they knew slots were available.
* Many have missed their sleep trying to check for slots at odd hours in an attempt to book the rare slot or two that become available.

## Solution
* Applied the **decision tree classifier model** after comparing the accuracy with logistic regression model to predict visa slot availability.
* Checkvisaslots can add slot prediction as a premium feature which can help users plan in advance instead of checking every moment.
* Users can reduce their reliance on agents and consultancies and save money to book their visa slot.

## Results
* Improved accuracy from 77.75% to **84.43%** with the decision tree classifier while achieving a high ROC-AUC value of **0.90** indicating the model's effectiveness.

## Considerations
* Testing only Logistic Regression and Decision Trees offers simplicity, interpretability, and computational efficiency. They provide strong baseline performance, help control overfitting, and are often sufficient for specific domains or regulated industries. In our case, performance is adequate, so more complex models may be unnecessary.
* While the model can be great at predicting slot availability for the month of May, June, July, and August due to the data available, it can be improved by collecting data throughout the year and adjusting the model based on the patterns observed.
* A high ROC-AUC score indicates that the model is effective at distinguishing between positive and negative classes. However, caution should be exercised to avoid overfitting by monitoring performance on the test set using various metrics, such as accuracy, precision, recall, and F1-score. Additionally, ensuring the interpretability of results is crucial for understanding the model's decisions.

