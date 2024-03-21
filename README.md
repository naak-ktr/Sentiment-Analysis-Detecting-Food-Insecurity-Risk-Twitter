# Sentiment Analysis in Detecting Food Insecurity Risk Among Twitter Users

![Thumbnail](https://github.com/naak-ktr/Sentiment-Analysis-Detecting-Food-Insecurity-Risk-Twitter/assets/89067111/6acae4b6-7d19-4cf0-9253-c982530705c4)


## Tackling Food Insecurity with Twitter Sentiment Analysis: A Machine Learning Approach 

Food insecurity remains a critical global issue, exacerbated by the recent pandemic and inflation. Social media platforms like Twitter offer valuable insights into individual struggles, but identifying those at risk requires advanced analytics. This project demonstrates the power of data-driven approaches in tackling food insecurity. By analyzing online sentiments, we can gain valuable insights to guide effective interventions and ultimately alleviate this critical issue. 

## Method

### 1) Data Collection & Preprocessing
I used Python's Snscrape module and RapidMiner to retrieve tweets containing keywords associated with food insecurity in Malaysia. Then, the tweets data were cleaned and preprocessed.


### 2) Lexicon-Based Sentiment Analysis
Employed three lexicon-based approaches to capture sentiment patterns within tweets:

1. TextBlob
2. VADER
3. Harmonized Lexicon 
   (A novel lexicon created by combining TextBlob and VADER scores with domain-specific food insecurity terms)

From here, the tweets dataset was categorized as positive or negative based on the overall sentiment score extracted from each lexicon.

### 3) Multi-Level Risk Classification:
Developed a machine learning pipeline using traditional supervised learning algorithms like Support Vector Machine (SVM), Naive Bayes, and Logistic Regression on the sentiment-annotated dataset.

Tweets with positive sentiment - Food Secure
Tweets with negative sentiment - Food Insecure

Negative tweets were further categorized into risk levels (mild, moderate, severe) based on their sentiment score thresholds 
(Refer the figure below)

![Labelling Sentiment for Severity-Page-3 drawio](https://github.com/naak-ktr/Sentiment-Analysis-Detecting-Food-Insecurity-Twitter/assets/89067111/e4fb6020-8214-4fbd-9079-76f2a441b79f)


### 4) Model Evaluation and Selection:
I used 70:30 and 80:20 train-test splits for robust model evaluation. Then, I compared the performance of various lexicon-algorithm combinations through accuracy testing with 70:30 and 80:20 train-test splits.





To amplify the project's significance, I translated the key insights into an interactive dashboard, enabling intuitive exploration of food insecurity risk patterns and empowering data-driven decision making.

[Tracking Food Insecurity on Twitter Interactive Dashboard](https://app.powerbi.com/view?r=eyJrIjoiM2E5YWZjMWUtNTIzMy00OGU5LWFkMDAtNDdiMzY2OWUwNTYyIiwidCI6ImNkY2JiMGUyLTlmZWEtNGY1NC04NjcwLTY3MjcwNzc5N2FkYSIsImMiOjEwfQ%3D%3D&pageName=ReportSection)
