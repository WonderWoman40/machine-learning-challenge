Machine Learning - Exoplanet Exploration


Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, i have created machine learning models capable of classifying candidate exoplanets from the raw dataset.

The following steps were taken as follows;

1. Preprocess the raw data
2. Tune the models
3. Compare the two models used. 

A detailed approach of the above steps:

1. Preprocess the Data

* Preprocess the dataset prior to fitting the model.
* Perform feature selection and remove unnecessary features.
* Use `MinMaxScaler` to scale the numerical data.
* Separate the data into training and testing data.

2. Tune Model Parameters

* Use `GridSearch` to tune model parameters.
* Tune and compare the two different classifiers selected(Support Vector Machine(SVM) and Random Forest Classifier).

Reporting the Final Result

For both models we did a train/test and this was to measure the accuracy of the our models. The train the model creates the model and the Test the model test the accuracy of the model. After this we tuned both models with `GridSearch`. For the SVM the tuning made the model more accurate with the values of the test and train score almost equal to 1, while for the Random Forest the models did not need any tuning as values dropped slightly below after tuning.

SVC | Before Tuning | After Tuning
--- | --- | ---
*Training score* | `0.845` | **0.887**
Testing Score | 0.841 | 0.879

RFC | Before Tuning | After Tuning
--- | --- | ---
*Training score* | `1.0` | **0.963**
Testing Score | 0.902 | 0.8883


I also did some visualizations for the RFC model :
The first visualization is for the Classification report and the second visualization is for the Features Importance. 
[Alt text](relative//Users/adesolafakiyesi/Desktop/machine-learning-challenge/Images/RandomForestClassifier Classification Report.png/to/img.jpg?raw=true "RandomForestClassifier Classificiation Report")

In conclusion the Random Forest Classifier Model is the most accurate based on my data. It had the highest scores close to 1 and had 1.0 for the training data even before tuning. I would say the RFC model is good at predicting the new exponents. However there is no harm in trying other models to test their accuracy if we could get any better than the RFC model. 















