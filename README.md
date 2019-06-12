Chirag J Patel


A coding exercise to welcome folks to the group.


INTRODUCTION
============
Every day, doctors administer clinical lab tests, such as cholesterol and fasting glucose, to diagnose health of their patients for heart disease and diabetes.

After seeing many patients, one doctor realizes that some of his patients who have higher levels of a diagnostic for diabetes, glycohemoglobin, also have higher levels of other clinical markers. Specifically, she hypothesizes that certain lab tests are predictive of others and would like to build evidence for (or against) her hypothesis.

ABOUT THE DATA
==============
In this short exercise, we will use a real clinical dataset to look for correlations between a diagnostic marker of diabetes, glycohemoglobin (http://www.webmd.com/diabetes/glycohemoglobin-ghb), and other serum biomarker diagnostics, including LDL-Cholesterol, HDL-Cholesterol, and triglycerides (used to test for heart disease), and cotinine, an indicator of current smoking status. 

The data originates from the National Health and Nutrition Examination Survey, a annual survey of the health of the nation. Optionally, you can learn more about the dataset here:
http://wwwn.cdc.gov/nchs/nhanes/search/datapage.aspx?Component=Laboratory&CycleBeginYear=2011
http://wwwn.cdc.gov/nchs/nhanes/search/datapage.aspx?Component=Demographics&CycleBeginYear=2011

Data files are in the ./nhanes simple csv 2011-2012/ directory.

EXERCISE
===============
We wish to search for what variables are correlated with Glycohemoglobin (%) and rank them in terms of their strength of their correlation. Using a coding language of your choice, do the following and record the time you started and ended:

0.) Read in the data files, formatted as .csv. Each file contains a different set of individual variables (columns) for each patient (rows). Each row identifies a patient whose ID is denoted in the column "ID". Being a real (read: "dirty") dataset, there are missing values and these are coded as "NA" in the datafiles.

1.) Next, after reading in all datasets, join/merge them together by patient ID.

2.) Describe the data set briefly: what is the mean age of the population? The median age? How many females and how many males? Ignore the observations that are missing (coded as NA)

3.) Implement your correlation search engine to test whether a.) LDL-Cholesterol, b.) Triglycerides, c.) HDL-Cholesterol, and d.) Cotinine (a marker of nicotene found in smoking) is associated with Glycohemoglobin (%). Specifically, build a linear regression model for Glycohemoglobin (%) as a function of  each variable a.)-d.) separately. For example, for a.):

Glycohemoglobin (%) = intercept + LDL-Cholesterol(mg/dL) * beta

For simplicity, ignore observations that are missing.

Answer the following questions (be very brief):
What is the model testing?
What are the assumptions of a linear regression model?

4.) Rank the four models in order of p-value. What is the clinical variable that is has the lowest p-value?

Optional: 
We just conducted multiple tests of hypotheses comparing Glycohemoglobin to 4 others. What is one issue to be cautious of when conducting multiple tests?

5.) Optional: build a multivariable linear regression model predicting Glycohemoglobin (%) as a function of other variables in the dataset. 

6.) Write a brief statement to the doctor regarding your findings (200 words or less). Keep it simple, telling her what you did, how you did it, and how you interpret the results (e.g., what do the beta mean?).



Feel free to use RStudio with RMarkdown (and export as .html) or Jupyter notebook.
