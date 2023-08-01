# Project 1

## Project Proposal

## Data Analysis Results

### Question 1: Do people with Cardiovascular Disease tend to have more additional health issues than people without CVD?


### Question 2: Is there a relationship between an increase in age and a prevalence of heart disease?
After completing the data analysis it is clear there is a strong, positive correlation between the survey respondent's age and the prevalence of heart disease. The data analysis supports the hypothesis, "As a respondent's age increases, there is a higher likelihood they will positive for heart disease." (r-square = 0.90101; p-value = 0)

Of the approximately 309k respondents surveyed in the cleaned dataset, 24971 (or 8.1%) responded as being positvely identified as having heart disease.

The data was first parsed down to only positive cases. This new dataset was plotted as a count of the 'Age Category' column, and it clearly shows a sharp increase in the number of positive heart disease cases starting at the '55-59' category. A brief check of the median showed 50% of the postive cases could be found somewhere above the 70-year-old age group. Additionally, 88% of the positive cases occured at the 55-year-old age group and above.

The full cleaned dataset was also plotted as a count of the 'Age Category' column to see if the age categories were evenly distributed across. The total respondent age categories are also slightly skewed towards the older age categories. Although, nowhere near extreme as the positive heart disease cases.

Chi square testing was done using 12 degrees of freedom and a 95% confidence. The expected values were caluclated using the actual numbers for each category * the 8.1% of positive cases in the dataset as a whole.
The statistical value = 21.03, and the observed statistical value = 16574.54. The calculated p-value was so low it was returned as 0.0. This supports our Alternative Hypothesis that age correlates to heart disease prevalence, and allows us to reject the null hypothesis of a similar percentage of positive cases across all age groups.

After converting the categorical 'Age Category' data to ordinal data. The values were plotted and a linear regression and correlation analysis performed. Both showed a stron, positive correlation between an increase in age and an increase in the prevalence of heart disease, (r-squared = 0.90101).

To conclude, the analysis shows there is a strong, positive correlation between increased age and numebr of positive cases of heart disease. The dataset includes additional categories such as diet, exercise, and other comorbidities. Data analysis should be done to see whether any of these other lifestyle and other health issues may also correlate to the 'Age Category' and number of positive cases. It is possible a lifestyle or health issue associated with age may also be part of the pattern leading to the increased number of positive cases with age.


### Question 3:

### Question 4: 

## Collaborators and Sources
**RESOURCES**
* Web App Survey for Dataset: https://cvd-risk-prediction.streamlit.app/page_2
* Kaggle Dataset used for Data Analysis: https://www.kaggle.com/datasets/alphiree/cardiovascular-diseases-risk-prediction-dataset 
* Turning categorical data into Ordinal Data: https://stackoverflow.com/questions/34007308/linear-regression-analysis-with-string-categorical-features-variables

