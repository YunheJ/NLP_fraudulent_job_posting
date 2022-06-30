# Fake Job Posting Classification

## Goal
Job search is a hard and struggling process for each graduate. It's too upset that sometimes the job posting is fake and even plan to steal money from students without income.:smiling_face_with_tear:

This project aims to automatically help job seeker detect if the posting is fake based on NLP models.

## Data
Data Source: https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction. Total ~18k rows and 19 columns.</br>
The raw data consists basic info of postings such as description, job location, company profile, benifits and label that if the posting is fraudulent.

## Approach
Model Input: combined job description, requirements and benifits.</br>
Train-Valid-Test split: 70%-15%-15%. Use test data to evaluate performance across different models.</br>
* CNN
* RNN
* BERT
Performance Comparison</br>
<img width="540" alt="Screen Shot 2022-06-30 at 11 04 40 AM" src="https://user-images.githubusercontent.com/102109674/176746874-6651b8d7-2e07-42ef-bed6-090dd8ba3aeb.png">

## Result
We'll forcus more on recall score since we try to detect fake postings as much as possible.</br>
Model results are aligned with our expectation.</br>
* CNN model is the most efficient one and recall rate is acceptable.
* RNN model got the highest recall score amoung the three models.
* BERT model performed not well compare to above two and is time consuming. We may need choose BERT when the data is not enough. But for current problem, CNN, RNN is more suitable.

## Improvement In the Future

* Fake postings data is imbalanced, further improvement can be done on resample to balance the target rate.
* Try to integrate the model in email/googl extension to automatically detect the fake postings.

## Resource
Notebook: WIP
