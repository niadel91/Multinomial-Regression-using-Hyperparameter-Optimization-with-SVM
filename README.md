# Multinomial-Regression-using-Hyperparameter-Optimization-with-SVM
Gauging how Support Vector Machine Algorithm behaves with Hyperparameter Tuning

## Data Description

The “juice.csv” data contains purchase information for Citrus Hill or Minute Maid orange juice.  A description of the variables follows. 

1. Purchase: A factor with levels CH and MM indicating whether the customer purchased Citrus Hill or Minute Maid Orange Juice 
2. WeekofPurchase: Week of purchase 
3. StoreID: Store ID 
4. PriceCH: Price charged for CH 
5. PriceMM: Price charged for MM 
6. DiscCH: Discount offered for CH 
7. DiscMM: Discount offered for MM 
8. SpecialCH: Indicator of special on CH 
9. SpecialMM: Indicator of special on MM 
10. LoyalCH: Customer brand loyalty for CH 
11. SalePriceMM: Sale price for MM 
12. SalePriceCH: Sale price for CH 
13. PriceDiff: Sale price of MM less sale price of CH 
14. Store7: A factor with levels No and Yes indicating whether the sale is at Store 7 
15. PctDiscMM: Percentage discount for MM 
16. PctDiscCH: Percentage discount for CH 
17. ListPriceDiff: List price of MM less list price of CH 
18. STORE: Which of 5 possible stores the sale occured at

 More crucial attribute than the prices of both these brands is the price difference between both these brands.
We already have the Store ID in the dataset so STORE and Store7 need not be included in the dataset.
List Price difference is a redundant attribute as we already have the Sales Price Difference in the data.

## Conclusion

After comparing the Train and Test Scores for all the models:


<u>Basic Models</u>

SVM with Linear Kernel is the best in case of Basic Models with the least Error scores for both Train and Test datasets.




<u>Tuned Models</u>

For both RBF and Linear Kernels, the cost parameter for the best model is 0.31 and the scores are almost equal.
For Polynomial, the cost parameter is 9.61 but the model isn't as good.  

Taking the Accuracy rate and Error Rate into Consideration, both tuned models - SVM with Kernel RBF and Kernel Linear are good but RBF is slighlty better as there are lower chances of Overfitting.

Removing such redundant variables in the dataset and keeping more relevant attributes will help us avoid the overfitting of the model.
