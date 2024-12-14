# E-Commerce-Sales
The dataset contains a collection of fictional e-commerce transaction data created for the purpose of data analysis, machine learning, and predictive modeling. It includes various e-commerce transaction attributes such as product categories, prices, discounts, payment methods, and purchase dates.

## Define the Problem Statement
We aim to:
* Analyze sales trends over time to identify patterns.
* Determine the top-performing categories and products.
* Understand customer payment preferences.
* Evaluate the impact of discounts on final sales.

## Exploratory Data Analysis (EDA)
* Analyze overall sales trends (Final_Price) by time.
* Identify top categories and products by sales.
* Understand payment method distribution.
* Evaluate the impact of discounts.

### Analyze overall sales trends (Final_Price) by time
![image](https://github.com/user-attachments/assets/e0facf1e-73a8-4380-bbf8-d83d892c6949)
* Sales start strong in the early months (February to April), peaking in April.
* A noticeable decline in sales is observed in May and June.
* Another peak occurs in October, followed by a sharp decline in November.
* April and October might coincide with specific events, holidays, or shopping festivals, boosting sales.
* Months like June and November could indicate off-season periods or reduced consumer spending.

### Identify top categories and products by sales
![image](https://github.com/user-attachments/assets/c3f3ec2c-13de-43cc-aaa2-520b32d350a2)
* Clothing leads the sales, followed closely by Books, Home & Kitchen, and Sports categories.
* The other categories like Toys, Beauty, and Electronics have similar sales numbers.

### Understand payment method distribution
![image](https://github.com/user-attachments/assets/09294dd0-944d-448e-8bde-0aad8269e597)
* Credit Card and UPI dominate as the most used payment methods, followed closely by Debit Card.
* Cash on Delivery remains a significant portion, showing that a considerable number of customers prefer this option.

### Evaluate the impact of discounts
![image](https://github.com/user-attachments/assets/fbf9cb62-1cf8-434f-b0cc-a490f11dd7e3)
* The data points show a clear downward trend as the Discount (%) increases.
* At 0% discount, the Final Price is at its maximum (around 500 Rs).
* As the discount increases (e.g., 10%, 20%, 30%, and so on), the Final Price decreases in a nearly linear manner.
* This suggests that the Final Price is directly dependent on the Discount applied.
* Each discount level (0%, 10%, 20%, 30%, 50%) forms a vertical cluster of points. This indicates that multiple products have the same discount level, but their corresponding final prices vary. The variation in final prices is likely due to the differences in the original prices of the products.
* At 50% discount, the Final Price drops significantly compared to other discount levels.
* The cluster at 50% shows a tighter range of Final Prices (between 0 Rs. to ~200 Rs.), implying that products receiving a 50% discount were priced lower compared to those at smaller discounts.
* Products with higher discounts tend to have a lower final price, possibly indicating that lower-priced products are given larger discounts.

### Statistical analysis
![image](https://github.com/user-attachments/assets/19998cb8-d2e6-48c1-b085-8b6ec91ce1d4)
1. **Mean**
* Price (Rs.): ₹254.80 (average original price of the products).
* Discount (%): 18.83% (average discount offered).
* Final_Price (Rs.): ₹206.91 (average price customers paid after applying the discount).

2. **std (Standard Deviation)**
* Price (Rs.): ₹141.68 (product prices vary significantly, indicating a mix of low- and high-priced items).
* Discount (%): 14.73% (discounts vary from low to high).
* Final_Price (Rs.): ₹122.69 (final prices also vary significantly, influenced by both price and discount).

3. **Quartiles (25%, 50%, 75%)**
* Price (Rs.):
    * 25%: ₹134.01 (most cheaper products fall below this price).
    * 50% (Median): ₹253.85 (half of the products cost less than this).
    * 75%: ₹377.60 (most higher-priced products are above this).
* Discount (%):
    * 25%: 5% (a quarter of products have discounts ≤ 5%).
    * 50% (Median): 15% (typical discount offered is 15%).
    * 75%: 25% (a quarter of products have discounts ≥ 25%).
* Final_Price (Rs.):
    * 25%: ₹104.51 (most products are purchased below this price).
    * 50% (Median): ₹199.19 (half of the purchases cost less than this).
    * 75%: ₹304.12 (higher-priced purchases are above this).

### Correlation Analysis
![image](https://github.com/user-attachments/assets/99a17530-01c8-4f85-aeef-0a5a12d7ad4a)
1. **Price (Rs.) and Final Price (Rs.)**:
* Correlation = 0.94 (strong positive correlation).
* This indicates that the Final Price is highly dependent on the Original Price.
* As the Price increases, the Final Price also increases, which is expected because the Final Price is derived from the Price after applying the discount.
2. **Discount (%) and Final Price (Rs.)**:
* Correlation = -0.31 (moderate negative correlation).
* This shows that as the Discount (%) increases, the Final Price decreases.
* The negative correlation aligns with the expected behavior since higher discounts lower the Final Price.
3. **Price (Rs.) and Discount (%):**
* Correlation = -0.00 (no correlation).
* This indicates there is virtually no linear relationship between the Price and the Discount (%).
* This suggests that discounts are applied independently of the product's price.

### Impact of Discounts on Categories
![image](https://github.com/user-attachments/assets/d2d574d1-7abf-45a7-aa6e-e788f557bf1e)
* Overall, the average discount percentages across all categories appear quite close, ranging from approximately 18% to 19.5%.
There is no drastic difference in discounting trends.
* The higher average discount for Home & Kitchen category suggests it may be a focus area for promotions to attract customers.
* Clothing, Toys, and Beauty categories might not receive as aggressive discounts, possibly due to consistent demand or other pricing strategies.

##  Forecasted sales values for the upcoming months (from December 2024 to November 2025)

### ARIMA model
An Autoregressive Integrated Moving Average (ARIMA) model is a forecasting tool that uses past data to predict how something will perform in the future. It's a popular model for time series forecasting because it's flexible and effective at capturing both autoregressive (AR) and moving average (MA) components

![image](https://github.com/user-attachments/assets/571afc79-1401-4aeb-b0e2-cd536861d421)

![image](https://github.com/user-attachments/assets/571b33ec-f616-4351-9154-b05e2c55d616)
* For December 2024, the forecasted sales are ₹89,491.29.
* Sales fluctuate significantly in the following months, with the lowest forecasted value being ₹53,877.83 in January 2025, followed by increases, then a dip, and then further fluctuations.
* There's a significant increase in the predicted sales for December 2024 (₹89,491.29) compared to November 2024 (₹51,915.08). This might indicate a seasonal boost in sales, possibly due to holiday shopping or other factors specific to that period.
* The forecast shows volatility in the upcoming months, with periods of high and low sales, suggesting that the model predicts erratic or seasonal fluctuations.
* For instance, January 2025 shows a dip (₹53,877.83), followed by a rise in February 2025 (₹86,235.82).
* The pattern of alternating high and low sales might indicate that external factors such as holidays, promotions, or market conditions are influencing the sales cycle.

## SARIMA (Seasonal ARIMA)
SARIMA extends ARIMA by considering seasonality in the data.

![image](https://github.com/user-attachments/assets/8fef2cc9-31a3-4c50-8ee7-e17291472019)

Same prediction as ARIMA

## Prophet (by Facebook)
Prophet is an open-source time series forecasting model that's used to decompose time series into trends, seasons, and holidays

![image](https://github.com/user-attachments/assets/518dce05-b1a1-49f1-9dfa-7b829b35baf8)

## Recommendations
* Plan promotions around April and October to maximize sales during peak periods. Stock up on popular products.
* Use discounts or flash sales to increase sales in May and November, especially if there's a seasonal dip.
* Allocate more marketing resources to Clothing, Books, and Home & Kitchen, which drive the most sales.
* Consider bundling products from popular categories with those from lesser-performing ones (e.g., combining Clothing with Toys or Beauty) to boost sales across all categories.
* For categories like Sports, Beauty, and Electronics, consider focusing promotions around specific seasons (e.g., sports equipment during seasonal games or beauty products around holiday seasons)
* Since Credit Card and UPI make up the majority of the payments, incentivize more customers to use these methods by offering exclusive digital discounts or offers.
* Given that a good portion of customers still prefer Cash on Delivery, ensure smooth and quick handling of COD orders to improve customer satisfaction.
* Consider integrating other modern payment options (e.g., mobile wallets or cryptocurrencies) to appeal to a wider customer base.
