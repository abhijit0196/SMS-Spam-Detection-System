# SMS Spam Detection System
1. Project Overview

This project builds a Natural Language Processing (NLP) pipeline to detect spam SMS messages.
The implementation includes Data Cleaning, Exploratory Data Analysis (EDA), and advanced Text Preprocessing, preparing the dataset for machine learning model training.
The goal is to analyze text patterns to distinguish between legitimate (Ham) and spam messages.

2. Dataset

Dataset: SMS Spam Collection
Total Messages: 5,574
Labels: ham (legitimate), spam
Input File: spam1.csv
Encoding: Latin-1

3. Tech Stack

Language: Python
Data Manipulation: Pandas, NumPy
Visualization: Matplotlib, Seaborn
NLP: NLTK
Preprocessing: Scikit-Learn LabelEncoder
4. Project Workflow
4.1 Data Cleaning
Dropped unnecessary columns: Unnamed: 2, Unnamed: 3, Unnamed: 4
Renamed columns:
v1 → target
v2 → text
Encoded labels: ham = 0, spam = 1
Removed duplicate entries

4.2 Feature Engineering
Created three new features:
num_of_char: number of characters in the SMS
num_of_word: number of words (via NLTK tokenization)
num_of_sen: number of sentences

4.3 Exploratory Data Analysis (EDA)
Analyzed relationships between engineered features and the target
Found that spam messages tend to be longer
Generated correlation matrix

4.4 Text Preprocessing (NLP Pipeline)
The function transform_text() performs:
Lowercasing
Tokenization
Removing special characters
Removing stopwords
Stemming using PorterStemmer


