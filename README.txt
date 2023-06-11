House prices in Iowa, USA - Find good deals and avoid scams

Objectives
1. Try to determine the best deals and worst scams from our database - people will get good investment ideas and have a sense of what to dodge.
2. Aplly new algorithms that I have not previously worked with (random forests, support vector machine)

Structure:
On short, we took and cleaned the data and then used the same x and y for all the 3 models. Then, we compared their performance and took into account the most accurate in order to talk about our business case - which houses are deals and which ones are scams.

Step-by-step:
1. Explain the data: get the dataset, see what features it has, what kind (how many numerical, how many non-numerical)
2. Plot some relevant information (distribution of target variable by an relevant independet variable or others)
3. Split the data in x (80 features) and y (Sale Price) - y is the target variable, x is the independent variable
4. Clean x (find out how many outliers we have according to IQR, eliminate a big part of them - we only kep 798/1460 rows -, fill the empty values with the median, eliminate 19 features with the help of correlation matrix)
5. Normalize x (MinMaxScaler)
6.1. Train the linear model
7.1. Make predictions 
8.1. Evaluate predictions with the help of statistical metrics (RMSE, MSE, normalized RMSE etc)
6.2. Train random forests model
7.2. Make predictions
8.2. Evaluate predictions with the help of statistical metrics (RMSE, MSE, normalized RMSE etc)
6.3. Train svm model
7.3. Make predictions
8.3. Evaluate predictions with the help of statistical metrics (RMSE, MSE, R^2)
9. Compare predictions with actual values to see which ones are priced fairly, which are overpriced and which are underpriced - create a new dataframe and sort it by largest to smallest.
10. Retrieve the first 10 and last 10 (meaning the top 10 best underpriced properties that we should buy and top 10 biggest scams - houses worth a little but are priced much higher).
* Clustering is part of another project