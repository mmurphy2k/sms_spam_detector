# sms_spam_detector
## Module 21 Challenge
### Table of Contents
1. **Program Description**
2. **File Structure**
3. **Prerequisites**
4. **How to run the notebook**
5. **README.md**
6. **sms_text_classification_solution.ipynb**
7. **gradio_sms_text_classification.ipynb**
8. **Interface**
9. **Prediction Results**


## 1. **Program Description**

You'll be refactoring code from an SMS text classification solution into a function that constructs a linear Support Vector Classification (SVC) model. Once the model is created and trained, you will create a Gradio app to host the application, enabling users to test text messages. The application will provide feedback to users, indicating whether the text is classified as spam or not, based on the model's performance.

## 2. **File Structure**

![File Structure](<Screenshot 2025-03-23 at 10.24.26 PM.png>)


## 3. **Prerequisites**
```bash
pip install pandas sklearn gradio
``` 


## 4. **How to run the notebook**


Within VS Code, select the **"gradio_sms_text_classification.ipynbb"** file and execute each of the code cells within the notebook from top to bottom in order.

Select the public URL and enter your SMS text message to be tested, press the "submit" button and view the results.


## 5. **README.md**

This file. 


## 6. **sms_text_classification_solution.ipynb**

This notebook contains the original code that will be refactored in the `gradio_sms_text_classification` code. The file is made up of the following steps:

1. Load the dataset into a DataFrame.
2. Split the data into train and test sets.
3. Build a Pipeline with the vectorizer and SVM model.
4. Test the classifier and display results 

## 7. **gradio_sms_text_classification.ipynb**

This notebook contains the refactored code from the `sms_text_classification_solution` code. The file is made up of the following steps:

1. Define the `sms_classification` function that will perform SMS classification using a pipeline with TF-IDF vectorization and Linear Support Vector Classification.
2. Load the dataset into a DataFrame.
3. Define the `sms_prediction` function that takes in the SMS text and predicts whether the text is "not spam" or "spam".
4. Create a sms_app that takes a textbox for the inputs and has a textbox for the output.


## 8. **Interface**

![sms_app](<Screenshot 2025-03-23 at 10.23.20 PM.png>)


## 9. **Prediction Results**

Test the following text messages. 

---
1. You are a lucky winner of $5000!
2. You won 2 free tickets to the Super Bowl.
3. You won 2 free tickets to the Super Bowl text us to claim your prize.
4. Thanks for registering. Text 4343 to receive free updates on medicare.
---
Results for the above text messages

---
1. The text message: "You are a lucky winner of $5000!", is not spam.
2. The text message: "You won 2 free tickets to the Super Bowl.", is not spam.
3. The text message: "You won 2 free tickets to the Super Bowl text us to claim your prize.", is spam.
4. The text message: "Thanks for registering. Text 4343 to receive free updates on medicare.", is spam.

---------------------------------------------

Mark Murphy mmurphy2k@gmail.com