## End-to-end Bulldozer Price Prediction Project

The goal of this project was to predict the sales price of a particular piece of heavy equipment at an auction based on its usage, type, and configuarations. The data is sourced from an expired Kaggle competiton ("Blue Book for Bulldozers"), which was subsequently sources from posted historical auction results. This competition was launched under the Kaggle Startup Program.

https://www.kaggle.com/c/bluebook-for-bulldozers/overview

### The Environment
- Python3
- Pandas, Numpy, Matplotlib, Scikit-Learn, Seaborn
- Jupyter Notebook

### 1. Problem Definition
How accurately can we predict the future sales price of a bulldozer given its characteristics and the previous sales prices of similar bulldozers?

### 2. Data
The data used in this project is available on Kaggle's 'Blue Book for Bulldozers' competition. In this case, it's historical sales data of bulldozers, including things like, model type, size, sale date and more: https://www.kaggle.com/c/bluebook-for-bulldozers/data

### 3. Evaluation
The evaluation metric for this competition is the RMSLE (root mean squared log error), calcluated between the actual and predicted auction prices.

**Note:** The goal for most regression evaluation metrics is to minimize the error. In this case, the goal was to build a machine learning model that minimises the RMSLE.

### 4. Features 
The Kaggle competition provides a data dictionary detailing all of the features and attributes of the dataset. The data dictionary can also be viewed on Google Sheets: https://docs.google.com/spreadsheets/d/18ly-bLR8sbDJLITkWG7ozKm8l3RyieQ2Fpgix-beSYI/edit?usp=sharing

In this section most of the exploratory data analysis (EDA) and data preprocessing is performed.

### 5. Modeling
Using the Scikit-Learn machine learning map as a guide, I opted to use a `RandomForestRegressor()` as the model for this project, in conjunction with `RandomizedSearchCV` for hyperparamter tuning. 

### The Conclusion
We can, with fair accuracy, predict the future sales price of a bulldozer, using the historical data provided.

- The final model achieved a RMSLE score of **0.24524163989538328** on the validation set
- The top 5 most important feature variables were `Year Made`, `Product Size`, `Sale Year`, `FI`, `Enclosure`
- A submission to Kaggle would have resulted in **30th place**, out of a total of 475 submission.
