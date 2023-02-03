# Maximising Sales
Identifying connections between item characteristics and sales

Ammon Snell

# Data
https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/
https://drive.google.com/file/d/1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw/view

The above links lead to a data set for Big Mart. This includes features such as item weight, fat content and location that the item is sold at. It also includes item sales which will be the focus of our project

# Methods
The first step to prepare the data is cleaning the fat content manually. Since the column has 3 different strings that essentially mean low fat, any encoder we use will split items with low fat into three different categories

Once that has been done, the rest of the cleaning was handled using preprocessing. Two pipelines were made for the categorical and numerical columns respectively. Once that was done, both pipelines were put in a comumn transformer to clean the data to satisfactory levels.

# Results
![download](https://user-images.githubusercontent.com/120761360/216644048-a82c91ff-854c-486d-a001-3a62f906e4a2.png)
This chart shows the number of items that had a certain number of sales. The x axis shows the sales for individual items and the y axis shows how many items had those sales. For example, over 3000 items had around 1000 sales, approximately 2500 items had around 2000 sales etc.
The data shows that most items have fewer sales. What causes this?
![download](https://user-images.githubusercontent.com/120761360/216645771-59e8933c-e518-4695-ba59-f8e5ed13eaa6.png)
This data shows positive correlation between MRP and item sales.

# Model
a simple linear regression model was used to find how each data column impacts the Item_Outlet_Sales column. Once the evaluations were finished a decision tree model was instantiated and evaluated.
in the end, the decision tree turned out to be better at explaining the outputs of future predictions.

# Recommendations
Since the heatmap demonstrates the highest positive correlation between MRP and sales. Big Mart should focus on products that have high MRP in order to increase sales.

For any additional information, see ammonsnell95@gmail.com
