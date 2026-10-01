# Project Methodology

## 1. Data Preparation

The supplied CSV contains three input features (`R`, `IR`, and `G`) and one target column (`RES`). The target contains five distinct class labels.

The dataset is loaded using pandas and separated into input features and target labels.

## 2. Train-Test Split

The current implementation uses scikit-learn's `train_test_split` with a test size of 33% and `random_state=0`.

Future experiments should consider stratified splitting where the class counts permit it.

## 3. Machine-Learning Models

### K-Nearest Neighbors

The KNN classifier uses four neighbors and predicts the class based on nearby training examples.

### Support Vector Classifier

The SVC model uses scikit-learn's default settings, including `gamma='scale'`.

### Logistic Regression

The Logistic Regression model uses the `liblinear` solver.

## 4. Evaluation

The original implementation calculates classification accuracy for each model and plots a comparison chart.

Further evaluation should include precision, recall, F1-score, and confusion matrices, particularly because the class distribution is imbalanced.

## 5. Raspberry Pi Integration

The application reads incoming serial data, interprets the comma-separated values as model inputs, applies the trained KNN classifier, and displays messages on an LCD. It also contains GSM modem commands for sending SMS notifications.

## 6. Reproducibility

Document the dataset source, Python environment, feature definitions, train-test split, model settings, and evaluation results when reporting experiments.

## 7. Scope

The supplied implementation performs classification. Its demonstration code generates random glucose values based on the predicted class; these values are simulated and are not be interpreted as measured or validated glucose concentrations.
<img width="656" height="514" alt="ai glucose" src="https://github.com/user-attachments/assets/27ea86ef-5e41-4813-8045-f645cf08a712" />
<img width="927" height="1575" alt="architecture-diagram" src="https://github.com/user-attachments/assets/cf6c5499-d6d6-4e5b-8fcc-5b84e6cf4fe6" />

