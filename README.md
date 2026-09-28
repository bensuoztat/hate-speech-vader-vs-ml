# Classifying Hate Speech: VADER vs. Naive Bayes vs. Logistic Regression

A comparison of a rule-based sentiment tool (VADER) against two supervised
models (Naive Bayes, Logistic Regression) on an imbalanced tweet dataset,
where label 1 marks racist/sexist tweets (7% of the data).

## Dataset
[Twitter Sentiment Analysis - Analytics Vidhya](https://www.kaggle.com/datasets/dv1453/twitter-sentiment-analysis-analytics-vidya)
(31,962 tweets, label 1 = hate-speech)

## Results
| Model | Precision | Recall | F1 |
|---|---|---|---|
| VADER | 0.14 | 0.39 | 0.21 |
| Naive Bayes | 0.90 | 0.37 | 0.53 |
| Logistic Regression | 0.46 | 0.78 | 0.58 |

## Summary
VADER measures sentiment, not whether a tweet is racist/sexist, so it performs
poorly on this task. Between the two supervised models, Naive Bayes is
more precise but misses more hateful tweets, while Logistic Regression
catches more of them at the cost of more false alarms. Which model is
"better" depends on whether missing a hateful tweet or raising a false
alarm is more costly.

