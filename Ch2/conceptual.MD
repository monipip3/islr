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

### c) We are interest in predicting the % change in the USD/Euro 3 exchange rate in relation to the weekly changes in the world stock markets. Hence we collect weekly data for all of 2012. For each week we record the % change in the USD/Euro, the % change in the US market, the % change in the British market, and the % change in the German market.
*This is a prediction problem using regression because we we care to pick a continous variable, the exechange rate. N = 52 weeks and our predictors are the % change in the US market, the % change in the British market, and the % change in the German market.*

# Q3.

### (a) Provide a sketch of typical (squared) bias, variance, training error, test error, and Bayes (or irreducible) error curves, on a single plot, as we go from less flexible statistical learning methods towards more flexible approaches.
![Bias Variance])(/img/bias_variance.jpeg)

### (b) Explain why each of the five curves has the shape displayed in part (a).
* As flexibility in the model increases, so does variance because of instability. One change can throw off the estimation more than inflexible model like linear regression which fits a straight line through the obs ervations. Bias also decreases as a model because more flexible because you can mirror almost every point, for example when K = 1 in KNN. Inflexible models like lasso regression are highly biased but more interepretable. The testing error can never be below Bayes error because Bayes error is irreducible. The testing error is curve linear because as a model becomes more flexible, the testing error goes down but once you run out of data the testing error increases. The training error goes down as flexibility increases, for example training error is below the Bayes error because in KNN K = 1 , your training error is 0. The sweet spot is where variance and bias meet. 

# Q4. You will now think of some real-life applications for statistical learning.

### a) Describe three real-life applications in which classification might be useful. Describe the response, as well as the predictors. Is the goal of each application inference or prediction? Explain your answer.
+ *Detecting a fraudulent transaction (order utilizing stolen credit card) versus a real transaction (order created by actual owner of credit card). The response is a 1 for fraud and 0 for no fraud. Predictors can be IP address, age of email address, linked to another fraud account by device, amount purchased, spammy email, billing address, full name, etc. The goal would be to predict from previously labeled data*
+ *Classifying a house as undervalued vs overvalued to make a better decision in buying a house. The predictors could be number of bedrooms, bath, zipcode, square foot of house, age of house, profit from last time it was sold, property tax, distance to nearest grocery store, walkability score, etc. The goal would be predicting if the house you want to buy is undervalued or overvalued*
+ *Trying to understand who is at risk for developing lung cancer. You can do a logistic regression problem to try to see what factors such as years smoking, age, gender, and many more variables if there is a correlation between observations of people who have developed lung cancer and people who have not. The goal is inference.

### (b) Describe three real-life applications in which regression might be useful. Describe the response, as well as the predictors. Is the goal of each application inference or prediction? Explain your answer.
+ *Similar to 4b but instead of predicting housing price
+ *Trying to understand fatality rates for a certain disease using demographics, this is for inference. 
+ *Trying to predict someone's salary based on age, experience, job title, years of experience, education level, and gender. This can be both inference and prediction.
 
 ### (c) Describe three real-life applications in which cluster analysis might be useful.
 + *Creating personas, trying to divide your customers in different groups utilizing spending habits, demographics, etc.*
 + *Clustering similar cities together for urban policy making, so mayors can network from similar cities and learn from each other*
 + *Clustering different movies or songs to see which are similar to each other**
 
 # Q5. What are the advantages and disadvantages of a very flexible (versus a less flexible) approach for regression or classification? Under what circumstances might a more flexible approach be preferred to a less flexible approach? When might a less flexible approach be preferred?
* Advantages of a less flexible approach would be: (1) when you have a lot of predictors and a small sample size, (2) you understand or assume the relationship between Y and your predictors, for example if you know it is a linear relationship you might want to use lasso or ridge ression and (3) if you want something more interepretable. A more flexible approach would be preffered if you have an extremely large sample size and you want to optimize the testing error, because you care about prediction. 

# Q6. Describe the differences between a parametric and a non-parametric statistical learning approach. What are the advantages of a parametric approach to regression or classification (as opposed to a nonparametric approach)? What are its disadvantages?
*If you don't know the relationship between Y and the predictors, a non parametric approach would be best at first. If however you know for example the relationship is linear, a parametric approach like linear regression will always beat out something like KNN unless the sample size was extremely large and the KNN boundary line behaved like a straight line. A parametric approach is more interepretable than a flexible (non parametric) model. If you care more about prediction than inference a non parametric approach would be preferred.*

# Q7.
### a) Compute the Euclidean distance between each observation and the test point, X1 = X2 = X3 = 0. 
*Take the square root of (x -y) ^2 for every point. For example Obs 1 sqrt((0 - 0) ^2 + (0-3) ^2 + (0 - 0)) yields 3.
+ 3 - Red
+ 2 - Red
+ 3.16 - Red
+ 2.23 - Green
+1.41 - Green
+ 1.73 - Red

 ### b) What is our prediction with K = 1? Why?
*Green because the first Green is at 1.41 which is the closest

### c)What is our prediction with K = 3? Why?
*Red because 3 out of 3 of the closest points are Red

### d) If the Bayes decision boundary in this problem is highly nonlinear, then would we expect the best value for K to be large or small? Why?
* We expect the best value for K to be SMALL because the bigger K is the more linear the bounary is. For example if K = 100, 1/100 = .001 versus K being 3 , 1/3 is .333. The smaller K is the more flexible the boundary.



 
