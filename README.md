# Image_classify_using_Machine Learning 
## 1. Introduction
An image classifier using machine learning is a tool that looks at a picture and decides what category it belongs to — for example, identifying whether an image shows a flower, a car, or a butterfly. The motivation behind building image classifiers is to make image sorting and recognition faster and easier. This has real-world applications in many fields, such as helping doctors detect diseases from medical images, recognizing products in retail stores, and helping self-driving cars understand their surroundings on the road.

## 2. Aims and Objectives
Aims:
Create an accurate classification model
Improve the model's accuracy over time
Make the model usable in real-life applications

Objectives:
Prepare and preprocess the image dataset
Identify and extract important features from images
Train and test the model
Make adjustments to improve performance
Compare results with other approaches

## 3. Literature Review / Problem Breakdown
The dataset for this project was built using Bing Image Search to collect images. The system is an image classification model trained on three categories of images. It uses the SVM (Support Vector Machine) algorithm for classification, and a user-friendly interface was built using Streamlit to let users interact with the model.

## 4. Proposed Solution / Methodology
The system design follows a standard machine learning pipeline:
Data → Training the Machine → Building a Model → Predicting Outcome
## System design 

<img width="695" height="219" alt="Picture1" src="https://github.com/user-attachments/assets/aeaa84ea-650e-4677-aa26-1701adb4a36d" />

Image data is collected and prepared
The machine is trained on this data
A classification model is built using SVM
The trained model predicts outcomes for new, unseen images

<img width="1409" height="761" alt="image" src="https://github.com/user-attachments/assets/e25509ee-ab1d-42fb-bc95-85b177debd2b" />

##5. Coding Section
Dataset Preparation: Images for the three categories (butterfly, cars, sunflowers) were collected, resized, and converted into flattened arrays suitable for training an SVM model.
Data Visualization: A bar graph was plotted to show the number of images available per category, confirming a balanced dataset across butterfly, cars, and pretty sunflowers classes.

<img width="810" height="702" alt="image" src="https://github.com/user-attachments/assets/51817b14-56af-4fa4-8d00-7e2735437a08" />

Splitting the Data: The dataset was split into training and testing sets using train_test_split from scikit-learn, ensuring the model could be evaluated on unseen data.

<img width="1120" height="249" alt="image" src="https://github.com/user-attachments/assets/5a56e308-d40b-4ba9-97f8-8792602b10da" />

Defining the Model: An SVM classifier was defined using sklearn.svm, with GridSearchCV used to tune hyperparameters (such as kernel type and regularization parameter C) for the best performance.

<img width="1068" height="444" alt="image" src="https://github.com/user-attachments/assets/63e17803-996e-4448-b936-c76d0828b523" />

Checking Accuracy: The model's accuracy was evaluated using accuracy_score, and a confusion matrix was generated to analyze prediction performance across the three classes.

<img width="1343" height="571" alt="image" src="https://github.com/user-attachments/assets/34ac072e-2f9d-442b-9e88-f033189abb3d" />

Testing with a New Image: A function was written to accept an image URL, download and preprocess the image (resize, flatten), and pass it through the trained model to predict its category — printing the predicted output (e.g., "cars").

<img width="1534" height="652" alt="image" src="https://github.com/user-attachments/assets/d7607dc1-ceab-4d30-ae48-833fb42c5438" />

<img width="1281" height="978" alt="image" src="https://github.com/user-attachments/assets/b1caa995-ee62-48d6-8d67-ab28a47078d1" />

<img width="679" height="962" alt="image" src="https://github.com/user-attachments/assets/458109d3-69c4-4b9e-ad7a-33bd45eb3858" />

## 6. Results
The model achieved a classification accuracy of over 90%
The trained model was saved using the pickle library for reuse without retraining
A Streamlit web app was built, allowing users to upload an image and get a live prediction
Example test results included correctly predicting categories such as "cars" and "butterfly" from new, user-provided images
ngrok was used to generate a public URL, making the Streamlit app accessible outside the local machine

## 7. Conclusion
This project successfully developed a machine learning model capable of classifying images into three categories: butterfly, cars, and sunflowers. The model was trained on a custom image dataset and tested, achieving an accuracy score of over 90%. The trained model was saved using the pickle library, and a Streamlit web application was created to allow users to upload images and receive real-time classification results. The app was deployed publicly using ngrok. The primary goal of this project was to provide users with an interactive, easy-to-use interface for image classification, demonstrating a complete end-to-end machine learning workflow — from data collection to model deployment.
