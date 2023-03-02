# E-Commerce Customer Segmentation 

## Project Description:
The project is about customer segmentation in an e-commerce website. Customer segmentation is the process of breaking a
customer base into groups of people that are similar in areas that matter in marketing, such as age, gender, interests, 
and purchasing habits. Companies that use customer segmentation believe that each customer is unique and that their 
marketing efforts would be better served if they targeted, smaller groups with messaging that would be relevant to those
customers and lead to a purchase. Companies also want to obtain a better understanding of their consumers' tastes and 
demands, with the goal of determining what each category values the most so that marketing materials can be more precisely 
tailored to that segment

## Data Source
The dataset is provided by The UCI Machine Learning Repository and contains actual e-commerce transactions occurring
between 01/12/2010 and 09/12/2011 for a UK-based online retailer. The company mainly sells unique all-occasion gifts. 
Many customers of the company are wholesalers.

## Data Info

Dataset has the following columns:
- **InvoiceNo**:   Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation.
- **StockCode**:   Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.
- **Description**: Product (item) name. Nominal.
- **Quantity**:    The quantities of each product (item) per transaction. Numeric.
- **InvoiceDate**: Invoice Date and time. Numeric, the day and time when each transaction was generated.
- **UnitPrice**:   Unit price. Numeric, Product price per unit in sterling.
- **CustomerID**:  Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.
- **Country**:     Country name. Nominal, the name of the country where each customer resides.

Here is a snapshot of the data

| InvoiceNo | StockCode |             Description             |          Quantity           |   InvoiceDate   | UnitPrice | CustomerID |    Country     |
|:---------:|:---------:|:-----------------------------------:|:---------------------------:|:---------------:|:---------:|:----------:|:--------------:|
|  536365   |  85123A   | WHITE HANGING HEART T-LIGHT HOLDER  |              6              | 12/1/2010 8:26  |   2.55    |  17850.0   | United Kingdom |
|  536365   |   71053   |         WHITE METAL LANTERN         |              6              | 12/1/2010 8:26  |   3.39    |  17850.0   | United Kingdom |
|  536365   |  84406B   |   CREAM CUPID HEARTS COAT HANGER    |              8              | 12/1/2010 8:26  |   2.75    |  17850.0   | United Kingdom |
|  536365   |  84029G   | KNITTED UNION FLAG HOT WATER BOTTLE |              6              | 12/1/2010 8:26  |   3.39    |  17850.0   | United Kingdom |
|  536365   |  84029E   |   RED WOOLLY HOTTIE WHITE HEART.    |              6              | 12/1/2010 8:26  |   3.39    |  17850.0   | United Kingdom |


The data is **incorrect** format, so it needs some modification to process easily. Here is a snapshot after modifications: 

| CustomerID |  Revenue   | Purchases | Quantity | RevenuePercentage |
|:----------:|:----------:|:---------:|:--------:|:-----------------:|
|  14646.0   | 279489.02  |   2085    |  196719  |     0.028672      |
|  18102.0   | 256438.49  |    433    |  64122   |     0.026307      |
|  17450.0   | 187482.17  |    351    |  69029   |     0.019233      |
|  14911.0   | 132572.62  |   5903    |  77180   |     0.013600      |
|  12415.0   | 123725.45  |    778    |  77242   |     0.012693      |

## Data Exploration
To explore more about data, the following questions need to be answered:
  - What was the total revenue?
  - Which months had the higher sales?
  - What products are in the top 10 in sales and revenue?
  - Which products were returned more frequently?
  - What are the top 10 countries that purchased the most?
  - How much is the share of the revenue for each cluster?

## Data Preprocessing
  - Set up the data with required columns
  - Removing the outliers
  - Correlation between the selected features
  - Split data into train set & test set
  - Scaling using minmax scaler

## Applying ML Methods  
### KMeans Clustering
   1. Determine optimal cluster number with Elbow method
   2. Fitting KMeans Model
   3. Plotting the Result
### Agglomerative Clustering
   1. Determine optimal cluster number with Elbow method
   2. Fitting Agglomerative Model
   3. Plotting the result
### Evaluating Models
   - The Completeness Score
   - Random Score  
   - The Normalized Mutual Info Score 
   - Heatmap

## References
  - [link 1](https://scikit-learn.org/stable/modules/model_evaluation.html)
  - [link 2](https://scikit-learn.org/stable/modules/clustering.html#clustering-performance-evaluation)
  - [link 3](https://www.datacamp.com/cheat-sheet/scikit-learn-cheat-sheet-python-machine-learning)
  - [link 4](https://towardsdatascience.com/cheat-sheet-to-implementing-7-methods-for-selecting-optimal-number-of-clusters-in-python-898241e1d6ad)
  - [link 5](https://github.com/microsoft/ML-For-Beginners/blob/main/5-Clustering/2-K-Means/README.md)
  - [link 6](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2099486/)

