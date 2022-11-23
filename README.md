# starbucks-experimental-design

## Project Description
A randomized experiment was conducted by Starbucks. An advertising promotion was tested to see if it would bring more customers to purchase a specific product priced at $10. Since it costs the company $0.15 to send out each promotion, it would be best to limit that promotion only to those that are most receptive to it. 

The Take Home Assignment is available in the Repository.

The goal of this exercise is to build a model to select the best customers to target, maximizing the two following metrics:

* Incremental Response Rate (IRR) - depicting how many more customers purchased the product with the promotion, as compared to if they didn't receive the promotion.

* Net Incremental Revenue (NIR) - depicting how much is made (or lost) by sending out the promotion.

Different approaches are described in Jupyter Notebook to solve this problem.

1. Two Models Approach
1. Single Model with additionnal "Receptive" feature

## Files
1. training.csv: contains the training data, to train our models.
1. Test.csv: contains test data, to test our models and promotion strategy.
1. Starbucks.ipynb: contains the Starbucks Promotion Strategies.
1. test_results.py: contains functions to evaluate the IRR and NIR values. File is provided by Starbucks.

## Evaluation and Result
The invariant metric shows minimal statistical significant with z-score=-0.66 and p-value=.507 that is under the range of hypothesis null and since the null cannot be ignored then, we proceed with evaluation metrics.
 The evaluation metrics; Incremental Response Rate(IRR) and Net Incremental Revenue(NIR). The IRR shows little effect of customers in promotion group compare to non-promotion group that make a purchase with just 1% increase . And the NIR indicates negative value of -2330 that might have been from promotion offer being sent to less receptive customers.
  On the first approach to promotion stratehy, we assume promotion is sent to all customers and how does this affect the IRR and NIR, there isn't much changes on the IRR but there is a signficant reduction in the NIR that show improvement, however the company cannot send all customers promotion since it's going to cost the company 0.15$ to send each promotion offer. The goal is to target customers who are likely to purchase the product.
   The challenge with imbalance data was contained with the use of SMOTE to overcome this issue and two classifier models(LinearRegression and LinearSVC) were used to predict if a customer with particular features will purchase the product or not. In addition, the gridsearch provides access to tuning the hyperparameters to improve the performance of the model.
    The single model after creating a categorical feature(Receptive) to classify the customers that receive promotion offer and bought the product as 1 and others as 0. This implementation show improvement in both IRR AND NIR even better than starbucks model with NIR= 290 and IRR= 2% increase

