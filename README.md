# sentiment-analysis-model-comparison
This code analyzes the performance of logistic regression, linear SVC, LSTM, and TinyBERT on the Yelp reviews dataset. It loads and preprocesses the dataset, trains the models, and analyzes performance using accuracy, precision, recall, F1- score, ROC-AUC, and training time.

Instructions:

To run the code, you must download the dataset from Yelp using the following link:

https://business.yelp.com/data/resources/open-dataset/

Upload the Yelp_academic_dataset_reviews.json dataset into your Google drive, and then you must allow the notebook to mount to your drive. Change the %cd section in the first code block to your directory:

%cd /content/drive/MyDrive/ <- change here!

Required Libraries:

json
pandas as pd
random
from sklearn.model_selection import train_test_split
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score, roc_auc_score
from sklearn.svm import LinearSVC
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Embedding, LSTM, Dense, Dropout
from tensorflow.keras.preprocessing.text import Tokenizer
from tensorflow.keras.preprocessing.sequence import pad_sequences
time
!pip install -q transformers torch accelerate
from transformers import AutoTokenizer, AutoModelForSequenceClassification
torch
from torch.utils.data import Dataset, DataLoader
matplotlib as plt


