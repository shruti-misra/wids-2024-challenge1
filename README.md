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

# Exploratory Data Analysis (WiDS_Datathon_EDA.ipynb)

EDA for this dataset consisted of 
* Plotting the distribution of each variable
* Conducting a bivariate analysis by looking at the correlations between different variables
* Conducting a bivariate analysis by looking at the distribution of the features with respect to different values of the target (diagnosed on time vs. not)

## Key observations

* The dataset is unbalanced with more cases being diagnosed on time than not
* All patients are female, therefore the patient_gender column can be dropped as it doesn't add new information
* Only one treatment type is represented for the Metastatic_first_novel_treatment_type variable, so this column can be dropped
* Multiple significant correlations were observed between different variables indicating that there are many redundant features in the data. Therefore, some features will have to be dropped to build a predictive model (see section on feature selection).
* Feature distributions for both types of diagnosis periods (above and below 90 days) are similar. There seem to be no outliers.

# Null Values and encoding

The null and missing values were dealt with as follows:

1. Remove columns where over half the values are null
2. Remove rows with more than 2 null values
3. Drop patient_gender (all female) and patient_race (mostly white, a lot of imbalance)
4. The rest of the missing values for numerical were filled in using the median as many of the distributions were skewed.
5. The missing values for the categorical variables were filled using the mode.

Three encoding schemes were explore for this project

1. One hot encoding was used to begin with as none of the categorical categories had any natural order
2. OrdinalEncoder
3. LabelEncoder (performed the best)

# Feature Selection (WiDS_Datathon_FeatureSelection.ipynb)

Given the many correlations and redundant variables in the dataset, three strategies were explored to select the appropriate features. 

### Remove high correlations

Features that are highly correlated often have redundant information in them, so I tried to remove them





