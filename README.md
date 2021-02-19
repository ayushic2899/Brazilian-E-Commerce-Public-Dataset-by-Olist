# Brazilian-E-Commerce-Public-Dataset-by-Olist

Dataset Link: https://www.kaggle.com/olistbr/brazilian-ecommerce

Welcome! This is a Brazilian ecommerce public dataset of orders made at Olist Store. The dataset has information of 100k orders from 2016 to 2018 made at multiple marketplaces in Brazil. Its features allows viewing an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes and finally reviews written by customers. We also released a geolocation dataset that relates Brazilian zip codes to lat/lng coordinates.

This is real commercial data, it has been anonymised, and references to the companies and partners in the review text have been replaced with the names of Game of Thrones great houses.
 
# Problem Statement

We need to understand how important this problem is to real world scenarios.
Trying to Build an automated Module for Recommender/recommendation system is a subclass of information filtering system that seeks to predict the rating/ preference a user would give to an item.
They are primarily used in applications where a person/ entity is involved with a product/ service to further improve their experience with this product, we try to personalize it to their needs. For this we have to look up at their past interactions with this product.
The purpose of the document is to explain the High architecture that would be used for developing the Recommendation/Recommender System for Market Basket Analysis acceptance system. The architecture diagram will provide an overview of an entire system, identifying the main components that would be developed for the product and their interfaces.

# Objective

The objective of this document is to present the brief overview of the technical architecture of the Market Basket Recommendation System. It describes the complete journey -> Data Collection to the Best Model Selection to the Deployment of the ML model for end user’s usage.

## The high-level objectives and outcomes are:
This dataset offers a supreme environment to parse out the reviews text through its multiple dimensions.

Clustering		:Some customers didn't write a review. But why are they happy or mad?
Sales Prediction		:With purchase date information you'll be able to predict future sales.
Delivery Performance	:You will also be able to work through delivery performance and find ways to 				  optimize delivery times.
Product Quality		:Enjoy yourself discovering the products categories that are more prone to 				  customer insatisfaction.
Feature Engineering	:Create features from this rich dataset or attach some external public 					  information to it.
Customer Lifetime Value:How much a customer will bring in future revenue?
SR/SDR Optimization	:Which SR or SDR should talk with each kind of lead?
Closing Prediction	:Which deals will be closed?

## Identifying Top line fast selling items
Calculate the Rate of Sale for each SKU.
This helps in ensuring that there is availability for right size / quantity rather than over stocking / under stocking. 
This will also help in reducing stock-outs at the SKU level. 
Improving the supplier delivery performance by reducing the freight costs and ensuring quicker response time from suppliers.

## Recommendations System:
### Collaborative Based
They are primarily used in applications where a person/ entity is involved with a product/ service. To further improve their experience with this product, we try to personalize it to their needs. For this we have to look up at their past interactions with this product.

# Data Collection Strategy

## There 9 csv files are available at Kaggle viz .

1. Customers Dataset - olist_customers_dataset.csv
This dataset has information about the customer and its location. Use it to identify unique customers in the orders dataset and to find the orders delivery location.
Each order is assigned to a unique customer id. This means that the same customer will get different ids for different orders. The purpose of having a customerunique_id on the dataset is to allow you to identify customers that made repurchases at the store. Otherwise we have to find that each order had a different customer associated with it.

2. Geolocation Dataset - olist_geolocation_dataset.csv
This dataset has information Brazilian zip codes and its lat/lng coordinates. Use it to plot maps and find distances between sellers and customers.

3. Order Items Dataset - olist_order_items_dataset.csv
This dataset includes data about the items purchased within each order.
Example:
The order_id = 00143d0f86d6fbd9f9b38ab440ac16f5 has 3 items (same product). Each item has the freight calculated according to its measures and weight. To get the total freight value for each order you just have to sum.
The total order_item value is: 21.33 * 3 = 63.99
The total freight value is: 15.10 * 3 = 45.30
The total order value (product + freight) is: 45.30 + 63.99 = 109.29

4. Payments Dataset - olist_order_payments_dataset.csv
This dataset includes data about the orders payment options.

5. Order Reviews Dataset - olist_order_reviews_dataset.csv
This dataset includes data about the reviews made by the customers.
After a customer purchases the product from Olist Store a seller gets notified to fulfill that order. Once the customer receives the product, or the estimated delivery date is due, the customer gets a satisfaction survey by email where he can give a note for the purchase experience and write down some comments.

6. Order Dataset - olist_orders_dataset.csv
This is the core dataset. From each order you might find all other information.

7. Products Dataset - olist_products_dataset.csv
This dataset includes data about the products sold by Olist.

8. Sellers Dataset - olist_sellers_dataset.csv
This dataset includes data about the sellers that fulfilled orders made at Olist. Use it to find the seller location and to identify which seller fulfilled each product.

9. Category Name Translation - product_category_name_translation.csv
Translates the product category name to english.
This is a real commercial data published by Olist

# Architecture of Data Schema

![alt text](https://i.imgur.com/HRhd2Y0.png)

# Flow Diagram - Explanation


1. Data wrangling - The process of cleaning and unifying messy and complex data sets for easy access and analysis.

2. EDA - Exploratory Data Analysis (EDA) is an approach/philosophy for data analysis that employs a variety of techniques (mostly graphical) to.

3. Modeling - The process of modeling means training a machine learning algorithm to predict the labels from the features, tuning it for the business need, and validating it on holdout data. The output from modeling is a trained model that can be used for inference, making predictions on new data points.

4. Model Evaluation - After data splits into Train & Test and predicts the result.

5. Dockerizing - An application is the process of converting an application to run within a Docker container.

6. Deployment - Deployment of an ML/DL-models simply means the integration of the models into an existing production environment which can take in an input and return an output that can be used in making practical business decisions.


# Conclusion

An automated Recommendation/Predictions system called the Market Basket Analysis recommendation/prediction system that will help the organization in making the decision to enhance their sales process and can optimize their business in a better form.


