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
  This patient sample has a readmission rate of 27%.

**What is the breakdown by gender in the dataset?**
The distribution is relatively even, with 49% female, 48% male, and 1% other.

**What is the age distribution?**
The distribution has a right skew toward older age, with the largest number of patients in the 70-79 age group at 3345 individuals.

**What is the breakdown by admission type?**
50% of patients were admitted via emergency, 30% as elective, and 19% as urgent.

**What about data on prior admissions?**
Roughly half of the patients in the sample have no prior admissions. The next largest group had 1 prior admission.

**What do we know about length of stay?**
The weighted average length of stay for this sample is 4.98 days.

**How about insurance type?**
Private insurance covers 50% of the patients in this sample, and Medicare covers another 30%. The remaining patients are covered by Medicaid or are self-pay.


