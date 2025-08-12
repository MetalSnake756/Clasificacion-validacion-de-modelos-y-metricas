
# Classification, Model Validation, and Evaluation Metrics
This project uses machine learning to classify clients for an auto financing company. The goal is to improve the identification of clients who are likely to default on their loans (referred to as "delinquent" or "moroso" in the original notebook). The manual, client-by-client analysis currently used is time-consuming and inaccurate.

## Project Description
The project addresses a challenge faced by an auto financing company with high demand for a small fleet of vehicles and a large number of delinquent clients, which is causing significant losses. My task is to use data provided by the company to build a classification model that identifies these delinquent clients.

## Methodology
The approach uses a Decision Tree Classifier to build a predictive model. The key steps are:

Initial Model: An initial model is trained on the entire dataset, which is shown to have an accuracy of 1.0, highlighting the need for proper validation to avoid overfitting.

Data Splitting: The dataset is split into three parts to ensure the model's ability to generalize to new data is properly assessed:

Training Set: Used to train the model and identify patterns.

Validation Set: Used to evaluate the performance of different models on new, unseen data.

Test Set: Kept separate from the beginning to simulate real-world data and provide a final, unbiased estimate of the chosen model's performance.

Model Validation: A new Decision Tree model with a maximum depth of 10 is trained on the training set and then evaluated on both the training and validation sets. This results in training accuracy of ~92% and validation accuracy of ~91%.

Model Evaluation: The final model is evaluated using a confusion matrix to understand its performance in classifying clients.

## Dataset
The notebook uses a CSV file named prestacar.csv. The dataset contains 54,025 entries and 11 columns. The columns include:

ingresos_cliente (client income)

anualidad_prestamo (loan annuity)

años_casa_propia (years of home ownership)

telefono_trab (work phone)

evaluacion_ciudad (city rating)

score_1, score_2, score_3, score_social (various scores)

cambio_telefono (phone change)

moroso (delinquent), which is the target variable (0 for non-delinquent, 1 for delinquent)

## Requirements
The following Python libraries are imported and used in the notebook:
Pandas → Data manipulation & analysis

Seaborn & Matplotlib → Data visualization

Warnings → Suppress execution warnings

scikit-learn → Machine Learning

sklearn.model_selection.train_test_split

sklearn.metrics.confusion_matrix

sklearn.metrics.ConfusionMatrixDisplay
