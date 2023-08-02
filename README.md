# Project 1

# Table of Contents:
1. [Data Analysis Results](#data-analysis-results)
2. [Project Proposal](#project-proposal)
3. [Collaborators and Resources](#collaborators-and-sources)

## Data Analysis Results

[Our Presentation Slides Can Be Found Here](https://docs.google.com/presentation/d/1Zt4UjkYOpoyy6h1VcesQ5X5-cXRsllS0v4aGlSOe0Ug/edit#slide=id.g25dd646f00b_5_0)

### Question 1: What eating and exercise habits relate to frequent instances of CVD?
[Analysis File 1 (Exercise)](Data%20Analysis/data_analysis_Porretta/sophia_data_analysis.ipynb)

[Analysis File 2 (Eating Habits)](Data%20Analysis/data_analysis_Bowman/data2.ipynb)

**Exercise:** When looking at the population of people from the survey that exercise, there is a clear relationship drawn between exercise and heart disease. There are many ways to look at this data but when viewing it from the population of people that excercise, it is safe to say that the number of people that have heart disease is much smaller than the number of people that do not have heart disease. In this sample specifically, we conclude that 6.67% of those that exercise have heart disease. 
Please Note: This does not draw any concusions about the relationship or potential impact that exercise has on developing heart disease. It is simply an observation on the comparison of two variables.

**Eating:** This dataset studies the links between different food items and the risks of heart disease. from what we can find, there are statistically significant results, but the correlation between the two is very weak. It seems that people that have heart disease eat a little under two fewer servings of fruit per month, as well as 1.3 servings fewer of vegetables. But again these correlation coefficients are near zero, so take those individual relationships with a grain of salt. There are some other interesting data, though. For example, the median serving count of alcohol drank per month among those with heart disease is zero, while the median for fruit consumption among heart disease patients and those without is also the same. The only median increase in consumption is for fried potatoes. 

### Question 2: How does biological sex relate to heart disease?
[Analysis File](Data%20Analysis/data_analysis_Porretta/sophia_data_analysis.ipynb)

To help us answer the question: Do a higher percentage of men or women have heart disease?, the initial dataset was looked at to compare the percentage of men and women that were tested to understand if the groups being considered are of similar size. The pie graph titled "Percentage of Each Gender in the Survey" gives a visual representation of the similar sample sizes we have for men and women. The results from the analysis show us that given the similar sized sample groups we can conclude that there is a slightly higher percentage of men that have heart disease than women. If this study were to be done again, a larger sample size would help us to make a more realistic assumption on the entire population. 

### Question 3: Is there a relationship between an increase in age and a prevalence of heart disease?
[Analysis File](Data%20Analysis/data_analysis_Bourgeois/data_analysis.ipynb)

After completing the data analysis it is clear there is a strong, positive correlation between the survey respondent's age and the prevalence of heart disease. The data analysis supports the hypothesis, "As a respondent's age increases, there is a higher likelihood they will positive for heart disease." (r-square = 0.90101; p-value = 0)

Of the approximately 309k respondents surveyed in the cleaned dataset, 24971 (or 8.1%) responded as being positvely identified as having heart disease.

The data was first parsed down to only positive cases. This new dataset was plotted as a count of the 'Age Category' column, and it clearly shows a sharp increase in the number of positive heart disease cases starting at the '55-59' category. A brief check of the median showed 50% of the postive cases could be found somewhere above the 70-year-old age group. Additionally, 88% of the positive cases occured at the 55-year-old age group and above.

The full cleaned dataset was also plotted as a count of the 'Age Category' column to see if the age categories were evenly distributed across. The total respondent age categories are also slightly skewed towards the older age categories. Although, nowhere near extreme as the positive heart disease cases.

Chi square testing was done using 12 degrees of freedom and a 95% confidence. The expected values were caluclated using the actual numbers for each category * the 8.1% of positive cases in the dataset as a whole.
The statistical value = 21.03, and the observed statistical value = 16574.54. The calculated p-value was so low it was returned as 0.0. This supports our Alternative Hypothesis that age correlates to heart disease prevalence, and allows us to reject the null hypothesis of a similar percentage of positive cases across all age groups.

After converting the categorical 'Age Category' data to ordinal data. The values were plotted and a linear regression and correlation analysis performed. Both showed a stron, positive correlation between an increase in age and an increase in the prevalence of heart disease, (r-squared = 0.90101).

To conclude, the analysis shows there is a strong, positive correlation between increased age and numebr of positive cases of heart disease. The dataset includes additional categories such as diet, exercise, and other comorbidities. Data analysis should be done to see whether any of these other lifestyle and other health issues may also correlate to the 'Age Category' and number of positive cases. It is possible a lifestyle or health issue associated with age may also be part of the pattern leading to the increased number of positive cases with age.


### Question 4: Do people with Cardiovascular Disease tend to have more additional health issues than people without CVD?
[Analysis File](Data%20Analysis/data_analysis_Leary/laxleary.ipynb)

![Figure 1](Data%20Analysis/data_analysis_Leary/Result%20Images/Diabetes.png)

**Diabetes:** From our pie chart we see that there is a very clear difference between the percentage of people with CVD who have diabetes and the percentage of people who do not have CVD and have diabetes. With 33% of the people with CVD having diabetes and only 11% of people without CVD having diabetes, the studied sample is three times more likely to have Diabetes if they have CVD  than if they do not. We are able to apply a simple chi-squared independence test to see that this difference  is statistically significant. With a chi-squared value of 10418.55, and degree of freedom 3, we are able to reject the null hypothesis with more than 99% certainty. This chi-squared test was carried out manually through the code to practice the test and to demonstrate the underlying methods for the test, but later tests use the built-in scipy stats function. 

Future studies on this topic might explore whether eating habits could be an underlying variable that could experimentally be shown to influence both conditions. Eating habits in relation to CVD are explored in Question 1, but a future examination could try to combine the results of both questions in order to determine any relation between all three. Similarly, it would also be of interest to split the "Yes" data in the Diabetes questionnaire by type, since the known causes for Type 1 and Type 2 diabetes do not have much overlap.

![Figure 2](Data%20Analysis/data_analysis_Leary/Result%20Images/Arthritis.png)

**Arthritis:** In this comparison we again see a large difference between the percentage of people with CVD who have Arthritis and the percentage of people without CVD who have Arthritis. While we know that a p-value of 0.0 in our code merely means that the p-value was so small that it could not be stored as a 64-bit decimal (absolute 0 p-values do not exist), we find once again a clearly statistically significant result in our chi-squared independence test. Formally, our null hypothesis here would be that "Arthritis occurs in patients with CVD with the same frequency that it appears in those without CVD", but we have significant evidence to reject this hypothesis, implying that there very well could be a relationship between having CVD and having Arthritis. 

As both conditions are related to excessive inflammation in the body, this could provide an interesting area of study. Future studies might focus on causes of inflammation and whether there is a relationship between the specific causes of imflammation and each of arthritis and CVD. 

![Figure 3](Data%20Analysis/data_analysis_Leary/Result%20Images/Other_Cancer.png)
![Figure 4](Data%20Analysis/data_analysis_Leary/Result%20Images/Skin_Cancer.png)

**Cancer:** As in the previously mentioned studies, our chi-squared tests for independence on both Skin Cancer and Other Cancer yield extremely small p-values due to extremely large chi-squared values. We again are able to reject our null hypotheses in favor of the hypothesis that there is a relationship between having Cardiovascular Disease and having cancer.  However, we were also able to analyze further whether there is a statistically significant difference between the frequency of Skin Cancer and the frequency of other cancers as a whole in those with CVD. The chi-squared test to differentiate between skin cancer and other cancers output a p-value of 0.91, meaning that there is not sufficient evidence in this case to reject the null hypothesis: "The quantitative relationship between having skin cancer and CVD is the same as the relationship between other cancers and CVD". This makes more interesting the fact that the data gatherers in this study opted to single-out skin cancer as a unique point of study, while grouping all the others.

Future exploration of this topic might further separate the category of "Other Cancer" in order to determine whether the relationship between skin cancer and CVD is unique to that type of cancer, as well as looking into whether any other specific types of cancer are uniquely common (or uncommon) in those with CVD. 

![Figure 5](Data%20Analysis/data_analysis_Leary/Result%20Images/Depression.png)

**Depression:** Unlike most of our previous results, our chi-squared test for the relationship bewteen Depression and CVD did not return a 0.0 value when run through our code, but the resulting p-value is still and *extremely* small number. Yet again, we have sufficient evidence to reject our null hypothesis in favor of the hypothesis "Depression occurs in patients with CVD more frequently than it occurs in those without CVD", since our data shows 4.7% more people with Depression amongst our CVD-positive population than amongst our CVD-negative population. 

Future studies on this specific topic might focus on potential causation by asking questions such as "Do patients tend to experience symptoms of depression first before or after their CVD diagnosis?" This question could be altered to incorporate time of appearance of CVD symptoms rather than diagnosis as well. Ultimately, the goal of future studies might be to discover whether a CVD diagnosis leads to increased rates of Depression, or whether the lifestyles lived by those with Depression could lead to increased risk of CVD.

![Figure 6](Data%20Analysis/data_analysis_Leary/Result%20Images/Comorbidities_With.png)
![Figure 7](Data%20Analysis/data_analysis_Leary/Result%20Images/Comorbidities_Without.png)

**Overlapping Conditions:**  We note that the relative sizes of our Venn-Diagram circles are very similar between the two plots. This leads to the question: Are the relative frequencies of Arthritis, Diabetes, and Cancer in those with CVD the same as in those without CVD?

 Despite the appearance of the pie charts as very similar, we find through our chi-squared test that we should reject the null hypothesis of "Patients with CVD experience Arthritis, Diabetes, and Cancer in equal proportion to those without CVD". The conflict between this result and our visual impression could be due to the fact that patients experiencing none of these comorbidities are not depicted in the Venn Diagram circles, but we can see in the annotation that these numbers are vastly different. In particular, the number of people in our data set with none of these health issues, including CVD, is by far the largest set when examining which health concerns people have. 

## Project Proposal
Project 1: CardioVascular Diseases Risk Prediction

**Team Members**

- Andrew Bourgeois
- Spencer Bowman
- Aubrey Leary
- Sophia Porretta

**Project Description**

This project will analyze a collection of data that was taken through a telephone survey about a person's health based on their response to a series of 304 questions. We will draw conclusions about the correlation between different lifestyle factors and the instances of CardioVascular Disease.

**Research Questions to Answer**

[Q1:](#question-1) What eating and exercise habits relate to frequent instances CVD?

[Q2:](#question-2) How does biological sex relate to heart disease?

[Q3:](#question-3-is-there-a-relationship-between-an-increase-in-age-and-a-prevalence-of-heart-disease)  Is CVD more prominent in Males or Females?

[Q4:](#question-4-do-people-with-cardiovascular-disease-tend-to-have-more-additional-health-issues-than-people-without-cvd) Is there a relation between CVD and other health concerns?


**Datasets to Be Used**

[Kaggle Data](https://www.kaggle.com/datasets/alphiree/cardiovascular-diseases-risk-prediction-dataset)

[Cleaned Data File](Resources/Cleaned_CVD.csv)


**Breakdown of Tasks**

- Find Dataset: Aubrey Leary


- Data Analysis: 
    - Q1: Sophia Porretta and Spencer Bowman
    - Q2: Sophia Porretta
    - Q3: Andrew Bourgeois
    - Q4: Aubrey Leary
<br/><br/>

- Final Writeup: Each person will summarize their own topic and then combine together


- Slide Deck: Each person will contribute the slides relevant to their topic to the Google Slides




## Collaborators and Sources

**RESOURCES**
* Web App Survey for Dataset: https://cvd-risk-prediction.streamlit.app/page_2
* Kaggle Dataset used for Data Analysis: https://www.kaggle.com/datasets/alphiree/cardiovascular-diseases-risk-prediction-dataset 
* Turning categorical data into Ordinal Data: https://stackoverflow.com/questions/34007308/linear-regression-analysis-with-string-categorical-features-variables
* Matplotlib Venn Documentation: https://stackoverflow.com/questions/19841535/python-matplotlib-venn-diagram

