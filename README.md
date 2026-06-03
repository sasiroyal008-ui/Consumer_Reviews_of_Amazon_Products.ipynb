# Consumer_Reviews_of_Amazon_Products.ipynbREADME.md
Sentiment Analysis on Amazon Product Reviews using NLP
Project Overview
This project performs Sentiment Analysis on Amazon product reviews using Natural Language Processing (NLP) and Machine Learning techniques.
The model classifies reviews into:
Positive Sentiment (1)
Negative Sentiment (0)
The workflow includes:
Data collection from Kaggle
Data preprocessing
Text cleaning and stemming
Feature extraction using TF-IDF
Model training using Logistic Regression
Performance evaluation
Prediction on new reviews
Dataset
Dataset Name: Amazon Product Reviews
Source: kaggle.com⁠�
The dataset contains:
Product reviews
Review ratings
Product information
Used Columns:
Column
Description
reviews.text
Review text
reviews.rating
Rating given by customer
Technologies Used
Python
Pandas
NumPy
NLTK
Scikit-learn
Matplotlib
Seaborn
KaggleHub
Machine Learning Pipeline
1. Data Collection
The dataset is automatically downloaded using KaggleHub.
Python
path = kagglehub.dataset_download(
    "datafiniti/consumer-reviews-of-amazon-products"
)
2. Data Preprocessing
Steps performed:
Convert text to lowercase
Remove HTML tags
Remove special characters
Remove stopwords
Apply Porter Stemming
Example:
Input:
Plain text
This product is AMAZING!!!
Output:
Plain text
product amaz
3. Sentiment Label Creation
Ratings are converted into sentiment labels.
Rating
Sentiment
4, 5
Positive (1)
1, 2
Negative (0)
3
Removed (Neutral)
4. Feature Extraction
TF-IDF Vectorization converts text into numerical features.
Python
vectorizer = TfidfVectorizer(max_features=5000)
5. Model Training
Logistic Regression is used for sentiment classification.
Python
model = LogisticRegression(max_iter=1000)
6. Evaluation Metrics
The model is evaluated using:
Accuracy Score
Classification Report
Confusion Matrix
Project Structure
Plain text
Sentiment-Analysis/
│
├── sentiment_analysis.py
├── README.md
├── requirements.txt
└── outputs/
    ├── sentiment_distribution.png
    └── confusion_matrix.png
Installation
Clone Repository
Bash
git clone <repository-url>
cd Sentiment-Analysis
Install Dependencies
Bash
pip install pandas numpy matplotlib seaborn nltk scikit-learn kagglehub
Run the Project
Bash
python sentiment_analysis.py
Expected Output
Dataset Information
Plain text
Dataset Shape: (xxxxx, x)
Missing Values: 0
Accuracy
Plain text
Accuracy: 92.5 %
(Actual accuracy may vary depending on dataset version and train-test split.)
Classification Report
Plain text
precision    recall    f1-score
Confusion Matrix
A heatmap visualization showing prediction performance.
Sample Predictions
Example:
Plain text
Review:
This product is amazing and works perfectly.

Sentiment:
Positive
Plain text
Review:
Worst purchase ever. Totally disappointed.

Sentiment:
Negative
Key Insights
Positive reviews generally dominate Amazon product review datasets.
TF-IDF effectively captures important textual features.
Logistic Regression provides strong baseline performance for sentiment classification.
Text preprocessing significantly improves prediction accuracy.
Future Improvements
Use advanced NLP models such as:
LSTM
GRU
BERT
RoBERTa
Hyperparameter tuning
Multi-class sentiment classification
Positive
Neutral
Negative
Deployment using:
Streamlit
Flask
Gradio
Author
NLP Sentiment Analysis Project
Developed using Python, NLP, and Machine Learning techniques for sentiment classification of Amazon product reviews.
