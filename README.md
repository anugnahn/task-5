Task 5: Exploratory Data Analysis (EDA) - Titanic Dataset 🚢
Project Overview
This project completes Task 5 of the Data Analyst Internship, focusing on Exploratory Data Analysis (EDA) using the classic Titanic Survival Dataset.

The objective was to extract meaningful insights, patterns, and anomalies from the data using Python libraries (Pandas, Matplotlib, Seaborn) and to prepare a summary report of the findings.

Files in this Repository
File Name	Description
titanic_eda_notebook.ipynb	The complete analysis script (Jupyter Notebook) containing all code, plots, and detailed written observations for each visualization.
EDA_Findings_Report.pdf	The required PDF Report providing a high-level summary of all key findings and data quality notes.
titanic.csv	The raw dataset used for the analysis.
README.md (This file)	Project summary and key insights.

Export to Sheets
Key Findings & Insights from the EDA
The analysis focused on identifying which factors were most correlated with a passenger's survival (survived variable).

1. Primary Survival Drivers (Bivariate Analysis)
Gender (sex): This was the single most dominant factor. Females had a significantly higher survival rate (approximately 74%) compared to males (approximately 19%). This confirms the "women and children first" policy in action.

Passenger Class (pclass): Survival was strongly correlated with socio-economic status. First-class passengers had a much higher survival rate than Third-class passengers, regardless of gender.

Fare (fare): Passengers who paid higher fares were more likely to survive, which directly ties into the pclass correlation.

2. Data Distribution & Quality (Univariate Analysis)
Skewness and Outliers: The fare column is heavily right-skewed, meaning most passengers paid low fares, but a few paid extremely high fares (outliers).

Missing Data: The age column contains a substantial number of missing values (NaNs), which will require imputation (e.g., replacing with the mean or median) before any machine learning modeling can occur.

Age and Survival: While the median age for survivors and non-survivors was similar, boxplots showed that the distribution of ages for survivors was skewed towards younger passengers (children), suggesting they were prioritized.

3. Correlation Structure (Multivariate Analysis)
The Heatmap confirmed that sex and pclass have the strongest correlation with the target variable survived.

A strong negative correlation exists between pclass and fare (wealthy passengers pay higher fares), confirming that these two features capture similar socio-economic information.

Conclusion
The Exploratory Data Analysis successfully identified clear, strong patterns that heavily influence survival on the Titanic, most notably gender and passenger class. The findings provide a solid foundation for subsequent data preprocessing and model building.



interpretation & Summary
This phase is where you transition from a Data Analyst to a Data Storyteller.

A. Written Observations
Your first step must be to revisit your Jupyter Notebook and write down observations for every plot.

Analysis Phase	Example Observation (Markdown Cell)
Univariate (Histogram of Fare)	The 'fare' distribution is highly right-skewed, indicating that the majority of tickets were priced low. This suggests mean will be greater than the median, and a log transformation may be beneficial later.
Bivariate (Countplot of Pclass vs. Survived)	Survival rate is strongly dependent on class. First-class passengers had the highest survival proportion, while Third-class passengers had the highest death toll, reflecting the "women and children first" and socio-economic rules of the disaster.
Multivariate (Correlation Heatmap)	The variable with the highest correlation to 'survived' is 'sex' (approximately -0.54) followed by 'pclass' (approximately -0.34). This confirms that gender and socio-economic status were the strongest predictors of survival.

Export to Sheets
B. Summary of Findings (The Report Content)
After writing all individual observations, draft a high-level summary. This summary is the core content of your PDF Report.

Data Quality: Note that the dataset requires cleaning, primarily due to missing values in the 'age' column.

Key Survival Drivers: Survival was a matter of "class, then gender." Women and children had priority, and within those groups, higher-class passengers survived at a significantly greater rate.

Distribution Insights: Numerical features like 'fare' and 'age' have skewed distributions and contain outliers, suggesting they will need preprocessing (e.g., imputation, standardization) before building a machine learning model.

