# Spam Classification using Random Forest

This project implements a spam email classifier using the Random Forest algorithm and compares its performance with Logistic Regression. The implementation is based on the Spambase dataset from UCI Machine Learning Repository.

## Project Overview

The project demonstrates the application of machine learning techniques for email spam classification. It uses two different models:
- Random Forest Classifier
- Logistic Regression

The implementation achieves high accuracy in distinguishing between spam and non-spam emails.

## Dataset

The project uses the Spambase dataset from UCI, which contains 4,601 emails with 57 features. The features include:
- Word frequencies (e.g., 'make', 'address', 'all', etc.)
- Character frequencies (e.g., ';', '(', '[', '!', '$', '#')
- Capital letter statistics (average length, longest length, total length)

## Implementation Details

### Data Preprocessing
- Removed duplicate entries
- Applied domain-specific rules (e.g., emails containing 'george' or '650' are marked as non-spam)
- Split the dataset into training (70%) and testing (30%) sets

### Models
1. **Random Forest Classifier**
   - Number of trees: 100
   - Random state: 42
   - Achieved accuracy: 94.22%

2. **Logistic Regression**
   - Solver: liblinear
   - Random state: 42
   - Achieved accuracy: 92.40%

## Results

### Random Forest Performance
- Overall accuracy: 94.22%
- Precision (spam): 0.94
- Recall (spam): 0.92
- F1-score (spam): 0.93

### Logistic Regression Performance
- Overall accuracy: 92.40%
- Precision (spam): 0.92
- Recall (spam): 0.89
- F1-score (spam): 0.90

### Feature Importance
The most important features for classification were:
1. Character frequency of '!'
2. Character frequency of '$'
3. Word frequency of 'remove'
4. Capital run length average
5. Word frequency of 'free'

## Requirements

The project requires the following Python packages:
- pandas
- scipy
- scikit-learn

## Usage

The implementation is provided in a Jupyter notebook (`SpamClassification.ipynb`). To run the project:

1. Ensure you have all required packages installed
2. Download the Spambase dataset
3. Run the Jupyter notebook

## Conclusion

The Random Forest model outperformed the Logistic Regression model in terms of accuracy and classification metrics. This is attributed to:
- Random Forest's ability to capture non-linear relationships
- Better handling of complex feature interactions
- More robust decision boundaries

The high accuracy achieved (94.22%) demonstrates the effectiveness of Random Forest for spam classification tasks.
