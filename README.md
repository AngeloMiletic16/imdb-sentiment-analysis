# IMDb Sentiment Analysis

This project performs **sentiment analysis** on IMDb movie reviews using **machine learning** and **TF-IDF vectorization**.

## Project Overview

The goal of this project is to classify movie reviews as either **positive** or **negative**.  
It presents a complete **binary text classification** workflow, including:

- loading and exploring the dataset
- handling class imbalance
- splitting data into training and testing sets
- converting text into numerical features using TF-IDF
- training and comparing multiple machine learning models
- tuning the best model with GridSearchCV
- evaluating final model performance

## Dataset

The dataset contains two columns:

- `review` — the text of the movie review  
- `sentiment` — the review label (`positive` or `negative`)

This makes the task a **binary classification problem** in the field of **Natural Language Processing (NLP)**.

The dataset file is not included in this repository because of its size.

To run the notebook, download the IMDb dataset manually and place it in the project folder as:

```text
IMDB Dataset.csv
```

## Workflow

### 1. Data Loading and Exploration
The dataset is loaded with pandas and inspected to understand its structure and class distribution.

### 2. Handling Imbalanced Classes
Since the selected data initially contained a class imbalance, balancing techniques were applied to create a more suitable dataset for training.

### 3. Train-Test Split
The balanced dataset was split into training and testing subsets.

### 4. TF-IDF Vectorization
The review text was transformed into numerical features using **TF-IDF (Term Frequency–Inverse Document Frequency)** so that machine learning models could process the text data.

### 5. Model Training
Several machine learning models were trained and compared, including:

- Support Vector Classifier (`SVC`)
- Decision Tree Classifier
- Multinomial Naive Bayes
- Logistic Regression

### 6. Hyperparameter Tuning
The SVM model was further optimized using **GridSearchCV** to find the best hyperparameters.

### 7. Final Evaluation
The best-performing model was evaluated on the test set using:

- accuracy
- classification report
- confusion matrix
- sample predictions

## Technologies Used

- Python
- pandas
- NumPy
- scikit-learn
- imbalanced-learn
- matplotlib
- Jupyter Notebook

## Project Structure

```text
IMDb_Sentiment_Analysis.ipynb   # Main notebook with full workflow
README.md                       # Project documentation
requirements.txt                # Required Python libraries
```

## How to Run

1.  Clone this repository.
2.  Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Open Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
4.  Run the notebook: `IMDb_Sentiment_Analysis.ipynb`

## Project Goal

The main objective of this project is to explore how well different machine learning models perform on sentiment classification tasks and to build a clear end-to-end NLP pipeline for classifying movie reviews.

## Conclusion

This project demonstrates a full machine learning workflow for sentiment analysis, from raw text data to a tuned classification model. It highlights the importance of preprocessing, class balancing, feature extraction, model comparison, and evaluation in NLP tasks.
