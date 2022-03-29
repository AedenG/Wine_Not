# Wine_Not

## Project Overview
The topic that we have selected is to detect a difference between red and white wine based off their chemical makeup. There's a myth that red wines have more sulfates than white wines. There's also a myth that white wines have more sugar than red wines. By combining two datasets, that were created from red and white wine variants from the Vinho Verde region of Portugal, we can see the properties of the wine. Using machine learning models, we will attempt to answer the following question: Can it be determined if the wine is red or white based off of the properties of the wine (ex. sulfates and sugar content)?

## Resources
P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis. Modeling wine preferences by data mining from physicochemical properties. In Decision Support Systems, Elsevier, 47(4):547-553, 2009.

## Communication
- Slack
- Zoom 

## Team Roles
- Square: Aeden
- Triangle: Hallie and Lara
- Circle: Marcus
- X: Daryl
<p align="center">
   <img src="https://github.com/AedenG/Wine_Not/blob/main/Images/ps5_group_label.png" width="520" height="380">
</p>

## Presentation of the Data
- [Google Slides](https://docs.google.com/presentation/d/1JBao1ZdLgtQ-TbDuoW-FYv36dGSUo3bWlBLuH3_NfpA/edit?usp=sharing)
- [Tableau](https://public.tableau.com/views/Wine_Not/ResidualSugarvs_Alcohol?:language=en-US&:display_count=n&:origin=viz_share_link)

## Discussion

### Description of the Data
Two separate red and white wine datasets with identical columns were joined into one CSV dataset. Since data regarding wine is difficult to scrape due to scraping legal restrictions, and wine information is typically restricted by wine companies, the datasets were chosen from Kaggle. These specific datasets were chosen due to the amount of quantitative data that was available for red and white wines. A column was added to identify each wine as a red or white wine. The combined dataset contains 6,497 rows and 13 columns; however, the dataset has more examples of white wines than red wines. This makes sense, as the wines are all from the Vinho Verde region of Portugal where more white wines are produced. A database was created using SQL and postgres for the joined dataset. Red wines were labeled as 1. White wines were labeled as 0. The database was read into Jupyter Notebook using Pandas and SQLAlchemy.

<p align="center">
   <img src="https://user-images.githubusercontent.com/91852495/159169651-ab071710-ac70-47d5-b363-68b76afbcfb4.png" width="520" height="400">
</p>

### Feature Selection 
Our independent variable includes the following: fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol content, and quality. Our dependent variable is wine type: red or white wine.

## Results

### Machine Learning Model
Scikit-learn train_test_split was used to split the data into training and testing sets. It also served to stratify the data. 

Since logistic regression is used for the prediction of binary outcomes, we felt this was the best machine learning model for our dependent variables- red or white wine. Scikit-learn was used to create a logistic regression model and train the data with the training set. Predictions were made. The logistic regression model was evaluated with an accuracy score of 98.65%.

<p align="center">
   <img src="https://user-images.githubusercontent.com/91852495/159141345-ea5845bf-542c-4213-8f89-ce61067ee273.png" width="520" height="400">
</p>

### Correlation
To assist in determining the relationship between our identified independent variables, we created a correlation matrix. We found that there is a negative correlation between wine type and alcohol content, as well as wine type and residual sugar, with a statistically significant p-value. This means that the red wines have a lower level of alcohol and lower level of residual sugar than the white wines. This finding is interesting because typically, red wines have higher alcohol content and higher sugar levels; however, in the Vinho Verde region of Portugal, the opposite is found to be the case. In addition to these two findings, we found that there is a positive correlation between wine type and sulphates with a statistically significant p-value. This means that the red wines had higher sulfate levels than the white wines. We created a heatmap based off of this data which illustrates the relationship between variables. The darker the square, the higher the positive correlation is between the two variables, whereas the lighter the square, the higher the negative correlation is between the two variables.

<p align="center">
   <img src="https://user-images.githubusercontent.com/91852495/159138472-0dd7d32c-0c97-430f-96b7-27c4a1bb4ee0.png" width="520" height="400">
</p>

