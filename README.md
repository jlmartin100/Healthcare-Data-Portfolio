# 30-Day Readmission Risk Analysis 
## HealthGuard Synthetic Dataset

### The Business Problem
The [Hospital Readmissions Reduction Program](https://www.cms.gov/medicare/quality/value-based-programs/hospital-readmissions) of the Centers for Medicare and Medicaid Services (CMS) incentivizes hospitals to reduce their 30-day readmission rates. In order to reduce readmission rates, analysis of patient risk factors is needed to identify areas of improvement.

### The Dataset
As patient data is heavily regulated by HIPAA due to privacy concerns, real observational datasets for modeling this type of analysis are not publicly available. To demonstrate the methods used in conducting this analysis, I have utilized the [HealthGuard Readmission Dataset](https://www.kaggle.com/datasets/epictetusmgr/healthguard-readmission-dataset/data) from Kaggle, a synthetic dataset constructed explicitly for the purpose of training machine learning models.


### The Skills
This preliminary portfolio includes
- SQL data cleaning and exploratory data analysis
- R code for training, fitting, and evaluating an XGBoost model
- A Tableau Public [set of dashboards](https://public.tableau.com/views/30DayReadmissionRiskHealthGuardDataset/TitlePage?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link) for data visualization

### Coming Soon
- An update using the UCI Diabetes dataset, which has more granular patient information
- Updated SQL and Tableau presentations
- A Python machine learning pipeline
- Statistical and survival analysis in R

### SQL: Exploratory Data Analysis
**What diagnoses do we have in the dataset? How many patients fall in each?**

  There are ten diagnoses included in this dataset, with the three largest cohorts being Type 2 diabetes, hypertension, and lipidemias.

**What is the baseline readmission rate?**

  The entire patient sample has a readmission rate of 27%.

**What is the breakdown by gender in the dataset?**

  The distribution is relatively even, with 49% female, 48% male, and 1% other.

  <img width="700" height="432" alt="gender labeled" src="https://github.com/user-attachments/assets/af254877-f831-4772-81d7-08deabdaefdd" />


**What is the age distribution?**

  The distribution has a right skew toward older age, with the largest number of patients in the 70-79 age group at 3345 individuals.

**What is the breakdown by admission type?**

  50% of patients were admitted via emergency, 30% as elective, and 19% as urgent.

  <img width="700" height="432" alt="admission type labeled" src="https://github.com/user-attachments/assets/80bfab5d-836b-46de-b990-c88b0ba1343a" />


**What about data on prior admissions?**

  Roughly half of the patients in the sample have no prior admissions. The average number of prior admissions is 1.02.

**What do we know about length of stay?**

  The weighted average length of stay for this sample is 4.98 days.

**How about insurance type?**

  Private insurance covers 50% of the patients in this sample, and Medicare covers another 30%. The remaining patients are covered by Medicaid or are self-pay.

  <img width="700" height="432" alt="insurance type labeled" src="https://github.com/user-attachments/assets/4d2fa5b5-5b74-4222-9a54-42320c7e0c75" />


**What else does the dataset tell us?**

  The average number of medications for these patients is 25.09. The average number of lab procedures is 49.74.

### R: XGBoost Modeling for 30-Day Readmission Risk Factors
XGBoost is a powerful machine-learning algorithm frequently used to predict patient hospital readmission risk with high accuracy. Read more about similar uses of this package on actual clinical data [here](https://pmc.ncbi.nlm.nih.gov/articles/PMC11311788/), [here](https://ieeexplore.ieee.org/document/11041492), or [here](https://pubmed.ncbi.nlm.nih.gov/40945246/).

The result of the model predicts readmission within 30 days with a 72.7% accuracy. The risk factors it calculates with are presented in the graphic below.

<img width="700" height="432" alt="Feature Importance" src="https://github.com/user-attachments/assets/56849524-8437-45b5-ad42-c545a6102238" />


### Tableau: Dashboards and Data Visualization
Visit Tableau Public for [dashboards and data visualizations](https://public.tableau.com/views/30DayReadmissionRiskHealthGuardDataset/TitlePage?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).
