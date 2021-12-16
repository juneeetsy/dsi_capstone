<img src="http://imgur.com/1ZcRyrc.png" style="float: left; margin: 20px; height: 55px">

# Capstone: Shopee Sales Analysis

## Executive Summary
In this analysis, we will be using the pycaret library to get the best models to predict sales performance in terms of quantity on Shopee. This project be focused on the Beauty and Personal Care category. This will not only allow us to forecast future sales performances in terms of categories, and will help sellers remain competitive on the platform. This in turn, increases sellers' efficiency on the platform.

We will be scraping data using Selenium from shops mainly on Shopee Mall, as it is an area on Shopee that lists verified sellers - mainly authorised distributors, retailers and flagship stores. These sellers are all regulated and are required to sell authentic products, following the guidelines of the brands they are selling. We will focus mainly on Watsons Official Store as it has a huge variety of 3000 product listings from different brands and categories within the health and beauty category, which provides us with a substantial sample size.

The provided data dictionary is reflected below, along with an additional column describing the corresponding data type.

**The main metric we will be using to assess the models is RMSE (root mean squared error) as it allows us to accurately assess how a model performs both on train and test data. Although we are optimizing for RMSE, we will also be looking at R2 to compare between models.

This analysis will benefit retailers in the Health and Beauty industry to make better business decisions and pick more popular products to increase sales. On Shopee, we can see that there is a limit of 3000 product listings, and larger distributors and retailers will have more than 3000 products. Listing products online, apart from their brick and mortar stores requires additional costs (creation of listings, allocating stocks to e-commerce, online stock inventory system etc.). Hence this will help Health and Beauty retailers have a better selection of products from popular categories, meeting the needs of shoppers.

In this analysis, we will be looking to answer the following questions:
* What features are most relevant for sellers to increase sale quantity?
* In what ways do categories or sub categories impact sales quantity?
* What mechanics are ideal for their range of products?
* What other insights can we get from the analysis?


## Problem Statement
This project aims to help retailers in the Health and Beauty industry by finding out key features or criterias that affect sale quantity on e-commerce platform. This allows sellers to have better selections of products that better suit the needs of shoppers on Shopee.

The model can also be used to forecast future sales, and hence allow brands to restock sufficient quantities to meet the volume on the platform. This prevents sellers and brands from missing out on sales.

The model will be trained using products from Watsons' official store on Shopee Mall, using the PyCaret which will determine the suitable models.

### 1. Data Scraping

In this section we will scrape the information for each product listing on the Watsons Official store ([source](https://shopee.sg/shop/195238920/search)). The data is scraped 4 December 2021.
The following features will be scraped from the individual product listings:

**Product information**
- Product Link
- Product Name
- Original Price
- Sale Price
- Discount
- Free Shpping
- Vouchers
- Product Category
- Product Description

**Ratings**
- Ratings
- Number Of Ratings
- Number of 5 star ratings
- Number of 4 star ratings
- Number of 3 star ratings
- Number of 2 star ratings
- Number of 1 star ratings
- Number of Ratings with Comments
- Number of Ratings with Media

**Stocks**
- Brand
- Quantity Sold
- Stocks available
- Number of users who Favourited the product

**Shop Description**
- Shop
- Total Ratings
- Total Products
- Total Followers

## Conclusion
In this analysis, we will be looking to answer the following questions:
* What features are most relevant for sellers to increase sale quantity?
> In terms of model prediction, the best features for Gradient Boost Regressor are mostly Shopper interaction generations such as comments, favourites, and reviews. These features are indeed related to the QtySold, however they are not as controllable by retailers. More information should be scraped, such as social media advertisements, increase in traffic from the traffic sources, impact of mechanics on the sales quantity.

  > It would also be more beneficial to get backend data such as basket size, basket value etc. this can help us understand mechanics that were implemented as well as the effectiveness of them. We can learn from consumer shopping behaviour patterns and implement better shopping mechanics to boost sales. (Not only Qty but $ value as well)

* In what ways do categories or sub categories impact sales quantity?
> Home Appliances > Cooling & Heating are extremely popular in terms of Sales Quantity. The main products in this category are Dehumidifiers. This can be due to flashsales that were created on this product in the past which boosted the sales quantity even more than usual.  It can also mean that Watsons is more competitive in terms of pricing for products in this category but we can only find out if we do a category wide research.

* What mechanics are ideal for their range of products?
> More information required as stated in point 1.

* What other insights can we get from the analysis?
> We definitely need more information that will be available on the back end. In order to help Watsons' specifically. However, applying this research on a larger scale on the Health and Beauty category can help us understand what Shopee's Shoppers look out for on the platform. It can also help us do competitors analysis - finding out similar products in different stores, as well as the performance of the similar products. We can then move on to analyse the drivers of the better performing listings.
