# Credit-Card-Fraud-Detection-System
This Project is made up of html , and python and python librarie. It takes inputs in html page and the model predicts whether the credit card is fraud or not , Since I was un-aware of features in datasets , My Aim was to just build a model which operates on GUI Interface , This is the my First Project which includes Machine learning technique

GUI Looks like ... : 

![Screenshot_20230111_031649](https://user-images.githubusercontent.com/99462259/211774648-38580d0d-6ec7-4818-abc7-e033bfef0528.png)

After Giving Inputs : 

![Screenshot_20230111_032040](https://user-images.githubusercontent.com/99462259/211775026-69bd8bfd-c10a-4f86-a5e0-6f658bfe657d.png)
 
Results Looks like ... :  

![Screenshot_20230111_032048](https://user-images.githubusercontent.com/99462259/211775247-2806360e-d357-4d3f-bc77-8e876907195e.png)

The provided code consists of two parts: data preprocessing and model deployment using Flask
<br>
# Credit Card Fraud Detection System
<br>
This project aims to develop a credit card fraud detection system using machine learning techniques. The system utilizes a dataset containing credit card transactions and employs a Decision Tree Classifier to predict whether a transaction is fraudulent or not. The project is divided into two parts: data preprocessing and model deployment.
<br>

# Data Preprocessing <br>
The data preprocessing part involves loading the credit card dataset from a CSV file and performing exploratory data analysis (EDA) to gain insights into the data. The following steps are performed:<br>

    -> The dataset is loaded using the pandas library.
    -> Initial data exploration is conducted by displaying the first few rows of the dataset using the head() function.
    -> Missing values in the dataset are identified using the isnull().sum() function.
    -> The distribution of the 'Time' column is analyzed by counting the occurrences of each unique value using value_counts().sum().
    -> The 'Time' column is dropped from the dataset as it is not relevant for the fraud detection task.
    -> The display option is set to show all columns of the DataFrame using pd.pandas.set_option('display.max_columns', None).

After data preprocessing, the dataset is split into training and testing sets using the train_test_split function from sklearn. The input features are stored in X, and the target variable ('Class') is stored in y.<br><br>
# Model Deployment <br>

The model deployment part involves training a Decision Tree Classifier on the preprocessed data and creating a Flask web application for fraud prediction. The following steps are performed:<br><br>

    -> A Decision Tree Classifier is initialized with the entropy criterion and a random state of 0.
    -> The classifier is trained on the training data using fit(X_train, y_train).
    -> Predictions are made on the testing data using predict(X_test).
    -> The confusion matrix and accuracy score are computed using confusion_matrix(y_test, y_pred) and accuracy_score(y_test, y_pred), respectively.
    -> The trained classifier is serialized using the pickle library and saved as a file named "classifier.pkl".
    -> In the Flask web application, the "classifier.pkl" file is loaded using pickle.load(pickle_in).
    -> The Flask app is created, and a root page is defined to render the main GUI template.
    -> A POST request handler is defined to receive input values from the GUI form.
    -> The input values are used to make predictions using the loaded classifier.
    -> The predicted result is displayed in the output GUI template.

To run the web application, execute the script and access the provided URL. The web application allows users to enter credit card transaction details and predicts whether the transaction is fraudulent or not.<br>
