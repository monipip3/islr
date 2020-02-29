# Q1.
For each of parts (a) through (d), indicate whether we would generally expect the performance of a flexible statistical 
learning method to be better or worse than an inflexible method. Justify your answer.

### a) The sample size n is extremely large, and the number of predictors p is small.
*A flexible learning method would be better because when your sample size is extremely large you minimize the testing error due to training on large amount of data. Also since number of predictors is small along with large sample size there is no risk of curse of dimensionality*

### b) The number of predictors p is extremely large, and the number of observations n is small.
*Here we can run into curse of dimensionality, there is not enough observations for each feature, with that an inflexible method like lasso regression can reduce the number of predictors*

### c) The relationship between the predictors and response is highly non-linear.
*We would need a more flexible model than an inflexible model to adapt to a highly non linear relationship. For example, KNN or SVM do not need linear relationships whereas linear regression analysis does. If we were to test with linear regression on a highly non linear data set we would get a worse testing error than something like KNN.*

### d) The variance of the error terms are extremely high
*We would need an inflexible model to reduce variance however we would have higher bias, so we have to be careful to pick a model that would reduce the variance but not highly increase bias like linear regression.*

# Q2.
Explain whether each scenario is a classification or regression problem, and indicate whether we are most interested in inference or prediction. Finally, provide n and p.

### a) We collect a set of data on the top 500 firms in the US. For each firm we record profit, number of employees, industry and the CEO salary. We are interested in understanding which factors affect CEO salary.
*Since we care to understand, this is inference so the model needs to be highly interpretable like linear regression. Since the CEO salary, Y is quantitative and continous, this is a regression problem. We wish to understand the relationship between this Y and the following Xs : profit (quantitative), number of employees (quantitative) , industry (categorical).*

### b) We are considering launching a new product and wish to know whether it will be a success or a failure. We collect data on 20 similar products that were previously launched. For each product we have recorded whether it was a success or failure, price charged for the product, marketing budget, competition price, and ten other variables.
*This is a classification problem, a binomial classification not multiclass because there is just 2 scenarios. N = 20, and we wish to predict this class using price charged for the product, marketing budget, competition price, and ten other variables.*

### c) We are interest in predicting the % change in the USD/Euro 3. We now revisit the bias-variance decomposition. 
Hence we collect weekly data for all of 2012. For each week we record the % change in the USD/Euro, the % change in the US market, the % change in the British market, and the % change in the German market.




(a) Provide a sketch of typical (squared) bias, variance, training error, test error, and Bayes (or irreducible) error curves, on a single plot, as we go from less flexible statistical learning methods towards more flexible approaches. The x-axis should represent ed exchange rate in relation to the weekly changes in the world stock markets. Hence we collect weekly data for all of 2012. For each week we record the % change in the USD/Euro, the % change in the US market, the % change in the British market, and the % change in the German market.

