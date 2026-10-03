## Credit Card Fraud Detection using SVM 💳

A machine learning web application that detects fraudulent credit card transactions using a Support Vector Machine (SVM) classifier. Built as my undergrad final year project, combining a Python backend with a web interface for submitting transactions and viewing predictions.

**Overview**
Credit card fraud is typically detected by analyzing a cardholder's spending patterns and flagging transactions that deviate from their "usual" behavior. This project implements that idea end-to-end: a user submits transaction data through a simple web page, a trained SVM model classifies it as genuine or fraudulent, and the result is rendered back with supporting accuracy metrics and visualizations.

## Objectives:
- Study and compare data mining approaches to credit card fraud detection
- Build a working fraud detection model using SVM
- Evaluate the model on classification accuracy, false positive rate, and false negative rate
  
## Architecture

![Credit Card Fraud Detection](images/fraud-detection.png)

The architecture consists of:
- A web frontend (index.html) for submitting transaction data
- A Python backend (app.py) that handles requests and runs predictions
- A trained SVM classifier (sklearn) performing the fraud/genuine classification
- A results page (result.html) rendering the prediction, accuracy, and scatter-plot visualizations
  
## Key Components

- 🌐 **Frontend** — `index.html` / `result.html`  
  Simple HTML pages for submitting transaction data and displaying prediction results, styled with `indexstyle.css/.scss` and `resultstyle.css`.

- 🖥️ **Backend** — `app.py`  
  Loads the dataset, preprocesses features and labels, and routes requests between the frontend and the model.

- 🧠 **Model** — SVM Classifier  
  Trained on labeled transaction data (`V1–V60`, label `0/1`) using `train_test_split`, `fit`, and `predict` from `scikit-learn`.

- 📊 **Evaluation**  
  Accuracy measured using `accuracy_score`, supported by scatter-plot visualizations comparing genuine and fraudulent transactions.

## Results

| Metric | Value |
|---|---:|
| Overall Accuracy | ~94.3% |
| True Fraud Correctly Flagged | ~93.3% |
| Genuine Transactions Misclassified as Fraud | ~13.3% |

## Project Structure

```text
Credit-Card-Fraud-Detection/

├── app.py                          # Backend — loads model and handles requests
├── index.html                      # Input page — submit transaction data
├── result.html                     # Output page — prediction results & charts
├── indexstyle.css                  # Styling for the input page
├── indexstyle.scss                 # SCSS styling for the input page
├── resultstyle.css                 # Styling for the results page
├── Credit Card Fraud Abstract.docx # Project abstract
├── Credit card fraud doc.docx      # Full project report
└── Credit Card Fraud PPT.pptx      # Presentation slides
```

## Conclusion

The Credit Card Fraud Detection project demonstrates the use of machine learning to identify potentially fraudulent transactions. An SVM classifier was trained on transaction data and achieved approximately **94.3% overall accuracy**, with around **93.3% of fraudulent transactions correctly identified**.

The project also integrates a **Flask backend with a simple HTML/CSS frontend**, allowing users to submit transaction data and receive a fraud prediction. Overall, the project provides a practical implementation of machine learning for transaction classification and demonstrates the complete workflow from data preprocessing and model training to prediction and visualization.
