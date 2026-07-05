# FUTURE_ML_02
Support Ticket Classification - Future Interns ML Task 2
# 🎫 Support Ticket Classification & Prioritization

**Future Interns – Machine Learning Internship (Task 2)**

## 📌 Overview
This project builds an NLP-based Machine Learning system to automatically classify customer support tickets into categories (Billing, Technical Issue, Refund, etc.) and predict their priority level (Low, Medium, High, Critical), using TF-IDF text vectorization and Logistic Regression.

## 🔍 Dataset
Customer Support Ticket Dataset (Kaggle) — structured ticket data including subject, description, category, and priority labels.

## 🛠️ Approach
1. Cleaned raw ticket text (lowercasing, punctuation removal)
2. Converted text into numerical features using TF-IDF vectorization (with built-in stopword removal)
3. Trained a Logistic Regression model to classify ticket category
4. Trained a second Logistic Regression model to predict ticket priority
5. Evaluated both models using accuracy, precision, recall, and F1-score
6. Built a confusion matrix to visualize classification performance

## 📈 Results
- Category classification accuracy: approx. 19.78%
- Priority classification accuracy: approx. 27.51%
- Both results are close to random-chance baseline, indicating the text alone carries limited distinguishing signal

## 🔬 Key Insight
On inspection, this dataset's ticket descriptions are largely templated (e.g., "I'm having an issue with the {product_purchased}. Please assist.") rather than authentic free-form customer writing. This means the wording is nearly identical across tickets regardless of true category or priority — limiting what any text-based model can learn.

This is a valuable, realistic ML lesson: **model performance is only as good as the signal present in the data.**

## 💡 Business Value
- Highlights the importance of using authentic, varied ticket text for production systems
- Recommends combining text classification with structured metadata (product type, customer tier, order value) for stronger real-world performance
- Even an imperfect model can add value by flagging tickets for manual review rather than fully automating triage

## 🧰 Tools Used
Python, Pandas, Scikit-learn, TF-IDF, Logistic Regression, Matplotlib, Seaborn, Google Colab

## 📂 Files
- `Support_Ticket_Classification_Task2.ipynb` — Full notebook with code, evaluation, confusion matrix, and analysis
