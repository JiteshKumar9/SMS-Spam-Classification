# SMS Spam Classification

This project focuses on classifying SMS messages as either spam or ham (normal) using machine learning models. The dataset used for this project contains SMS messages labeled as spam or ham. The goal is to build a classification model that can predict whether a given SMS message is spam or not.

## Dataset

The dataset used in this project is `SMSSpamCollection.csv`, which contains two columns:
- `label`: The label indicating whether the message is spam (1) or ham (0).
- `message`: The actual text of the SMS message.

## Libraries Used

The following libraries are used in this project:
- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations.
- `matplotlib`: For data visualization.
- `seaborn`: For enhanced data visualization.
- `nltk`: For natural language processing tasks such as stopwords removal and lemmatization.
- `sklearn`: For machine learning algorithms and tools such as TF-IDF vectorization, Naive Bayes, and Decision Tree models.

## Steps Involved

1. **Data Preprocessing**:
   - The dataset is loaded, and missing values are checked.
   - The labels are mapped from 'ham' and 'spam' to 0 and 1, respectively.
   - Imbalanced dataset is handled by oversampling the spam messages.
   - A word count feature is added to the dataset.
   - A new feature is created to check if the message contains currency symbols.

2. **Text Cleaning and Lemmatization**:
   - Special characters and numbers are filtered out.
   - Text is tokenized, and stopwords are removed.
   - Lemmatization is applied to reduce words to their base form.

3. **Feature Extraction**:
   - The text data is transformed into numerical features using the TF-IDF vectorizer.

4. **Model Building**:
   - Two classification models are used: Naive Bayes and Decision Tree.
   - The models are trained using the training data, and predictions are made on the test data.
   - Cross-validation is used to evaluate the performance of both models.
   - The classification reports and confusion matrices for both models are displayed.

5. **Prediction**:
   - A function `predict_spam` is created to classify new SMS messages as spam or ham.

## How to Run the Code

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/sms-spam-classification.git

2. Install the required libraries:

```bash

   pip install -r requirements.txt

3.  Place the SMSSpamCollection.csv dataset in the project directory.

4. Run the Python script:

   bash
   python sms_spam_classification.py

5. You can also use the predict_spam function to classify new SMS messages:

   ``python
`sample_message = 'Your sample message here'
`result = predict_spam(sample_message)
`print(result)

6. Results
The classification models' performance is evaluated using F1 score, classification reports, and confusion matrices. The Naive Bayes model and Decision Tree model are compared for their performance on the dataset.

Example Output
For a sample spam message:

Gotcha! This is a SPAM message.
