# Hyderabad_rent_predction
predicts the rent for top 15 cities in hyderabad
Here is a brief project report on the Hyderabad real estate price prediction based on the Jupyter notebook file:

Introduction
The goal of this project was to build a model to predict residential rental prices in Hyderabad based on location, property size, number of bedrooms etc. Predicting real estate prices can help property owners price their properties appropriately and help renters find affordable options.

Data
The data used in this project was sourced from a Hyderabad real estate dataset with 19110 rows and 36 columns. It contained details on property location, size, bedrooms, amenities, rental price etc. 

Data Cleaning and Preprocessing
The following data cleaning and preprocessing steps were taken:

- Dropped unnecessary columns like id, url etc. retaining only relevant features like locality, property size, bedrooms etc.

- Handled missing values by dropping rows with NA values.

- Converted categorical features like locality to dummy variables. 

- Removed outliers in property size and rental price using standard deviation from mean.

- Filtered top 10 localities for model building.

This resulted in a clean dataframe with 19046 rows and 10 columns ready for modelling.

Model Building
The data was split into 70% train and 30% test sets. A linear regression model was built and evaluated using R2 score and cross-validation. GridsearchCV was used to tune hyperparameters of linear regression, lasso regression and decision tree models. Linear regression performed best with an average cross-val score of 0.7. 

The final model was able to predict prices on test data with 71% accuracy. It was converted to a function to provide rental price predictions on new data based on inputs for locality, property size and bedrooms.

Conclusion
The model provides decent accuracy in predicting Hyderabad rental prices. The locality feature being converted to dummy variables improved model performance significantly. Going forward, adding more relevant features like amenities, furnishing, floors etc. can help further improve accuracy. Overall, this model provides a good starting point for price prediction.
