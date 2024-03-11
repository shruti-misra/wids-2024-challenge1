# Problem Statement
Based on the provided dataset which consists of patients information (age, race, BMI, zip code, breast cancer diagnosis code, metastatic cancer diagnosis code, metastatic cancer treatments, etc.), their geo-demographic data (income, education, rent, race, poverty, …etc), as well as toxic air quality data (Ozone, PM25 and NO2), predict the likelihood of the patient’s Diagnosis Period being less than 90 days. The data for this datathon was provided by Gilead Sciences.

# Features
## Target

The variable that needs to be predicted is the probability that the diagnosis period is less than 90.

## Patient Level Features

Patient level features included:
* Race
* Payer type
* Location (Zipcode, State, Region)
* Gender
* Age
* Breast cancer diagnosis code
* Metastatic cancer diagnosis code

## Patient Level Features

Demographic features included the following features as they pertain to the patients' region:
* Population of the patient's region
* Population density of the patient's region
* Gender distribution (male vs. female)
* Age distribution
* Relationship status distribution (single, married, widowed etc.)
* Income distribution
* Education Distribution
* Racial distribution
* Air quality (ozone, NO2, PM25)
* Employment rate
* Home ownership
* Commute time
* Health insurance (uninsured vs. not uninsured)

# Exploratory Data Analysis (file WiDS_Datathon_EDA.ipynb)

EDA for this dataset consisted of 
* Plotting the distribution of each variable
* Conducting a bivariate analysis by looking at the correlations between different variables
* Conducting a bivariate analysis by looking at the distribution of the features with respect to different values of the target (diagnosed on time vs. not)

## Key observations



