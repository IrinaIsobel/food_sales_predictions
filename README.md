# Food Sales Predicitons
## Learning to analyze and predict sales with python and machine learning
<b>Author:</b> Irina Isobel Lukban Diaz
### Business Problem:
How well can we predict future item sales, and what data is relevant?

### Data:
[Source](https://docs.google.com/spreadsheets/d/e/2PACX-1vSneA58lbwC6aQ6kDKUMgY7t3V_fVQkMF6n-wXIBWpvzHH20Rx0UDQYufcWhZ7TTdVUjrPwabuKua-C/pub?output=csv)

# Methods
- Identifying duplicates and imputing null values using pandas
- Visual analysis - using graphs to visually understand numerical data
- Exploring correlations between data, and exploring sales within certain variables 
- Using machine learning regression models to predict future sales

# Results
<b>Correlation</b>
![image](https://user-images.githubusercontent.com/123199534/225164727-bd90971c-e244-4bc3-8114-b6da7e27e55c.png)
- There is a moderate correlation between Item Outlet Sales and Item MRP.
- There is a slight correlation between Item Visibility and Outlet Sales.
- All other correlations are negligible.

<b>Average Outlet Sales by Type</b>
![image](https://user-images.githubusercontent.com/123199534/225164869-297d4471-8045-40b7-a9e8-de415cf4d8f9.png)
- The most, average outlet sales per type were Type 3 Supermarkets at \$3694.04
- The least were Grocery Stores at $339.83

<b>Average Outlet Sales by Type</b>
![image](https://user-images.githubusercontent.com/123199534/225164963-0b0e9ee3-8a9c-431b-ab24-d8e22e8ce6b9.png)
- Though data is skewed by missing outlet size, the highest average outlet item sales comes from medium sized outlets at \$2681.60.
- The lowest sales come from small outlets at $1912.15

<b>Average Outlet Sales per Item Type</b>
![image](https://user-images.githubusercontent.com/123199534/225165119-f765a39a-3863-4453-8745-1b6ca385156e.png)
- Starchy foods have the highest average sales ($2374.33)
- All item types range within $400 in sales

<b>Item MRP vs. Sales</b>
![image](https://user-images.githubusercontent.com/123199534/225165253-b77014a2-e5b6-41b2-957e-cc500ecb4760.png)
- There is a moderate correlation between MRP and item sales.
- As the MRP rises, so do sales.

### Model:
- Final prediciton model is a Random Forest Model
- Metrics:
>Train RMSE:	1074.4923
>Test RMSE:	1047.1732
>Train R2: 0.609883
>Test R2: 0.602544
- The R2 score shows that that about 60% of the testing data fits within the model, wh ile the RMSE shows it can predict sales within $1,047.
- The model may not be ideal for a number of reasons, including being too simple of a model, not having enough data, or features that do not correlate well with the target.
- Note that during the machine learning process, the missing object type data (outlet size) was imputed with the most frequently used value, instead of creating a new value: missing. Since the amount of null data was large, I opted to impute frequently used data rather than drop null values. This was to avoid skewing the process with new and unnecessary data.

### Recommendations:
- Gathering more data
- Finding data more relavent to sales predictions

<b>For further information</b>
For any additional questions, please contact IrinaLukban@gmail.com
