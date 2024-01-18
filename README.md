# Linear Regression Model for Marketing Data Analysis and Prediction

## Objective:
1. Analyze and comprehend the key factors and variables influencing lead generation;
2. Develop a prediction model to estimate sales returns and revenue based on marketing investment.

## Descriptive Analysis
The data is composed of 4 columns:
1. youtube: investment in marketing on youtube per month
2. facebook: investiment in marketing on facebook per month
3. newspaper: investment in marketing on newspaper per month
4. sales: sales revenue per month

The database has 171 rows, and all the data are of float type. No data preparation techniques were needed.

No information regarding the units and scale of the variables was provided. Therefore, considering that the database represents monthly values of a Brazilian company, for analysis purposes, it will be assumed that the unit of measurement is "Rs" for the investments collumns and "parts per Rs 1.000,00" for the sales column.

##Exploratory Analysis

To conduct this analysis, a new exploration dataframe was created, to which two new attributes were added:

1. social_media: Marketing investments in social media (facebook + youTube) per month;
2. total: Total marketing investment per month.

The following conclusions were drawn:

1. The "newspaper" attribute shows a weak relationship with the target, with a coefficient of determination (r²) of 0.065;
2. "social_media" reveals a high relationship with the target, with an r² of 0.742;
3. The "youtube" attribute is the variable with the highest correlation with the target, presenting an r² of 0.612.

## Modeling

In the model construction phase, the implementation of a simple linear regression model was demanded. The model yielded an RMSE of R$ 1781.42, representing an error of 10.1134% from the mean. Due to the model's straightforward simplicity and transparent parameter approach, hyperparameter optimization did not have a noticeable impact on the outcomes.

## Evaluation

###Results Evaluation

Initially, the model presented a coefficient of determination (R²) of 92.47%, indicating an extremely satisfactory fit to the utilized data and excellent predictive capability within the sample space.

Therefore, we can assume that the results presented in the analysis of parameters have a high probability of representing analytically useful data. Thus, the following conclusions were drawn from the results and model development:

1. It is noted that Facebook is the marketing platform with the highest sales-generating capacity. At the same time, it is observed that investment in newspapers is extremely inefficient.

2. Despite the model's excellent fit to the data, as evidenced in the modeling section, it exhibits a high error. This suggests the need for improved model training, possibly with a larger database or the exploration of other modeling techniques.

###Next Steps

Based on the results, it would be beneficial to conduct a detailed analysis of the YouTube and newspapers platforms.

1. **YouTube:** It would be necessary to examine whether the target audience for marketing on the platform aligns with the company's consumer base.
2. **Newspapers:** Due to the very low performance and limited correlation with sales, it would be interesting to explore reallocating the investment to other marketing platforms.
