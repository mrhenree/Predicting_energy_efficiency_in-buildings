### Note: Details to project are contained in the jupyter notebook bears the project code ("Predicting energy efficiency/consumption in buildings, using multi-output models").

## Project brief

In a building, thermal energy involves two measures of cooling load (CL), and heating load (HL) and these measures are regulated by heating, ventilation, and air conditioning (HVAC) system. The HVAC system is designed to compute the HL and CL of the space and thereby, provide a desirable indoor air condition. 

Predicting heating and cooling needs of a building in the initial design phase to find out optimal solutions amongst different designs is very important, as well as in the operating phase of the building for efficient energy usage. In this project, different multi-output regression models were applied in predicting heating and cooling needs of buildings based on parameters such as building height, surface area, glazing area, wall area, and so on. 

The models used include Linear Regression, Ridge Regression, Lasso Regression, SVR, K-Nearest Neighbors, Decision Tree, Random Forest, Gradient Boosting, and Neural Network. These models were used as Multi-output models in this project because the aim was to simultaneously predict two target variables from the dataset; but since some models do not natively support direct multi-output predictions, all the six (6) models were individually fed into the MultiOutputRegressor Wrapper to aid multi-output predictions.  

Lastly, this dataset was taken from https://cml.ics.uci.edu/, based on research by Tsanas and Xifara, and consists of 768 observations and 10 variables (which are listed below). Eight (8) of these variables were used as features (input variables), while two (2) were used as predictors (output variables).

Input variables are: 
+ relative compactness 
+ roof area (in m²) 
+ overall height (in m) 
+ surface area (in m²) 
+ glazing area - 0%, 10%, 25%, 40% of floor area
+ wall area (in m²)
+ glazing area distribution of a building (already encoded) - 1:Uniform, 2:North, 3:East, 4:South, 5:West
+ orientation (already encoded) - 2:North, 3:East, 4:South, 5:West

Output variables: 
+ heating loads (in kWh)
+ cooling loads of the building (in kWh)
