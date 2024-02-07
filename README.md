<h1>Predicting Heart Disease with Machine Learning</h1>

<h2>Description</h2>

This project is a pivotal venture into medical data science, aiming to discern and predict heart disease presence through comprehensive data analysis. 

This project dives into the complexity of cardiovascular health, employing advanced machine learning techniques to sift through clinical and physiological data. By meticulously preprocessing data, engineering relevant features, and deploying sophisticated models such as Decision Trees and Random Forests, this endeavor offers invaluable insights for healthcare professionals. 
It stands as a beacon for leveraging technology in medical diagnostics, promising enhanced predictive accuracy and operational strategies in heart health management.n

<h2>Project Overview</h2>

In this project, we analyzed heart disease data to predict its onset in individuals. Key steps included:

- Data preprocessing and exploration to understand the dataset's characteristics.
- Feature engineering and selection with pandas and numpy to identify relevant predictors.
- Application of machine learning algorithms like Decision Tree, Logistic Regression, Random Forest, and K-Nearest Neighbors for prediction.
- Visualization of analytical results using tools like Seaborn and Matplotlib to interpret data and model outcomes effectively.

<h2>Data Dictonary</h2>

- age: The age of the patient in years.
- sex: The sex of the patient (1 = male; 0 = female).
- cp: The type of chest pain experienced by the patient (values range from 1 to 4).
- trestbps: The resting blood pressure of the patient upon hospital admission.
- fbs: Indicates if the fasting blood sugar is greater than 120 mg/dl (1 = true; 0 = false).
- restecg: Resting electrocardiographic results (values are 0, 1, or 2).
- thalach: The maximum heart rate achieved by the patient.
- exang: Exercise induced angina (1 = yes; 0 = no).
- oldpeak: ST depression induced by exercise relative to rest.
- slope: The slope of the peak exercise ST segment.
- ca: Number of major vessels colored by fluoroscopy (0-3).
- thal: Thallium stress test result (3 = normal; 6 = fixed defect; 7 = reversible defect).
- target: The diagnosis of heart disease (angiographic disease status) with value 1 for > 50% diameter narrowing, and 0 for < 50% diameter narrowing.


<h2>Project Walkthrough</h2>
 <br />

<p align="center">
<strong>First, we will see how variables are correlated to each other</strong> <br />
<img width="780" alt="image" src="https://github.com/lokhandeishan/Predicting-Heart_disease/assets/157990694/297b427e-30e2-424b-ad1b-b2ab3c237e5c">
<br />
<br />

<p align="center">
<strong>We then produce a histogram to see the distribution of our variables</strong> <br />
<img width="529" alt="image" src="https://github.com/lokhandeishan/Predicting-Heart_disease/assets/157990694/8b38ea13-4859-48a7-b7f9-ec243939378f">
<br />
<br />

<p align="center">
<strong>Now, let's see the number of patients in our Target 0 or 1 bucket.</strong> <br />
<img width="532" alt="image" src="https://github.com/lokhandeishan/Predicting-Heart_disease/assets/157990694/70fcf2b1-63c1-422c-b0ba-1b52b843d54f">

<br />
<br />


<p align="center">
<strong>We now scaled our data to run our models</strong> <br />
<img width="666" alt="image" src="https://github.com/lokhandeishan/Predicting-Heart_disease/assets/157990694/7e76dacf-1a23-4e3c-8f0d-6887a0d4a01e">
<br />
<br />

<p align="center">
<strong>Let's check cross val score to choose best K-value</strong><br />
<img width="590" alt="image" src="https://github.com/lokhandeishan/Predicting-Heart_disease/assets/157990694/5bb44d0b-3dda-41b8-8559-fa94573ad66b">
<br />
<br />

<p align="center">
<strong>The rsult of our 1st model - KNN is out</strong> <br />
<img width="605" alt="image" src="https://github.com/lokhandeishan/Predicting-Heart_disease/assets/157990694/4636ac7c-df36-4e27-b5c4-a28ed0244918">
<br />
<br />

<p align="center">
<strong>Similarly, running our 2nd Model - Random forest, we get.</strong> <br />
<img width="605" alt="image" src="https://github.com/lokhandeishan/Predicting-Heart_disease/assets/157990694/26416dea-dbc2-47b6-840b-fea23cedfb64">
<br />
<br />

<p align="center">
<strong>Splitting the data into Train:Test ration of 30:70</strong> <br />
<img width="606" alt="image" src="https://github.com/lokhandeishan/Predicting-Heart_disease/assets/157990694/78a86971-6e4e-4bb2-93ba-a74e53b3efef">
<br />
<br />

<p align="center">
<strong>Let' see the F1 score for our 3rd Model : Decision Tree</strong> <br />
<img width="595" alt="image" src="https://github.com/lokhandeishan/Predicting-Heart_disease/assets/157990694/c5ce78aa-b5d9-4db2-8e6c-5a89802b3bd9">
<br />
<br />

<p align="center">
<strong>Lastly, let's plot our ROC Curve </strong><br />
<img width="546" alt="image" src="https://github.com/lokhandeishan/Predicting-Heart_disease/assets/157990694/d50a4197-68f0-4c80-aefc-6f3a714b851a">
<br />
<br />


<h2>Model Performance</h2>

We assessed several machine learning models and evaluated their performance using confusion matrices and accuracy scores:


- **Random Forest**:
   - Accuracy: 78.82%

- **Decision Tree**:
   - Accuracy: 77.89%

- **K-Nearest Neighbors (KNN)**:
   - Accuracy: 84.49%

The K-Nearest Neighbour model achieved the highest accuracy of approximately 84.49% among the models.


<h2>Findings</h2>

<strong>Based on the Correlation Matrix, we see:</strong>

- age shows a slight positive correlation with trestbps (resting blood pressure) and ca (number of major vessels).
- sex has a moderate negative correlation with thal (thalassemia), indicating different patterns in thalassemia between males and females.
- cp (chest pain type) has a noticeable positive correlation with the target, suggesting chest pain type is a good indicator of heart disease presence.
- thalach (maximum heart rate achieved) and slope of the peak exercise ST segment have moderate positive correlations with the target, indicating higher heart rates and certain ST segment slopes are associated with the presence of heart disease.
- exang (exercise-induced angina), oldpeak (ST depression induced by exercise), and ca show moderate to strong negative correlations with the target, implying these are indicative of the absence of heart disease.
- oldpeak and slope are also negatively correlated, which is consistent with the understanding of exercise-induced cardiac stress response.


<strong>Based on the Histogram, we see:</strong>

- Most participants are in their mid-50s to 60s, indicating a middle-aged cohort which is a common demographic for heart disease studies.
- The dataset includes more males than females, which should be considered when analyzing sex-specific trends
- The majority of participants do not experience typical angina (chest pain), suggesting that asymptomatic cases are prevalent in the dataset.
- Cholestrol was found to be present in a normal distribution pattern suggesting presence as age goes up.
- Resting Blood Pressure (trestbps) Shows a normal distribution with a slight right skew, indicating most individuals have normal to moderately high blood pressure
- The majority of participants have fasting blood sugar below 120 mg/dl- oldpeak and slope are also negatively correlated, which is consistent with the understanding of exercise-induced cardiac stress response.
- Most participants have a normal resting electrocardiographic reading
- Maximum Heart Rate (thalach): The distribution is left-skewed, with most participants achieving a high maximum heart rate during testing.
- More participants did not experience angina during exercise
- Many participants have a minimal depression, which is a good sign in the context of heart disease
- Slope of the Peak Exercise ST Segment (slope): A flat slope is the most common, which can be an indicator of heart disease.
- Most participants have 0 visible vessels on fluoroscopy.
- The majority of participants do not have typical findings associated with thalassemia.
- we see more individuals with heart disease than without in the dataset.


<strong>Based on the Target Bar-Chart, we see that more individuals have a heart condition than the one's who don't.</strong>


<strong>Based on the ROC-Curve, we see:</strong>

- The curve climbs quickly towards the top-left corner, indicating a good true positive rate when the false positive rate is low
- The AUC of 0.77 implies that there's a 77% chance the model will distinguish between a patient with heart disease and one without if chosen at random.
- While not perfect, the curve suggests the model has a reasonable predictive power and could be useful in a clinical setting for preliminary assessments.

<h2>Recommendation and Predictions</h2>

- Older age and higher resting blood pressure could indicate a higher risk for heart disease.
- Male patients may have different thalassemia patterns and potentially higher risk.
- Certain chest pain types may strongly suggest the presence of heart disease.
- Higher maximum heart rates and specific ST segment slopes during exercise might correlate with heart disease
- Absence of exercise-induced angina and minimal ST depression may suggest a lower risk of heart disease.
- A count of zero visible vessels on fluoroscopy could be associated with a lower risk, whereas a higher count may indicate a higher risk

<h2>Libraries Used</h2>

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

<h2>Data Source</h2>

The data was sourced from the UC Irvine Machine Learning Repository (https://archive.ics.uci.edu/dataset/45/heart+disease)
