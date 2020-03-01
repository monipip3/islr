## Q1.
Describe the null hypotheses to which the p-values given in Table 3.4 correspond.
Explain what conclusions you can draw based on these p-values.
Your explanation should be phrased in terms of sales, TV, radio, and newspaper, rather than in terms of the coefficients of the linear model.

*We can conclude that TV, while holding everything else constant affects sales and so does radio. Newspaper has no affect on sales*

## Q2.
Carefully explain the differences between the KNN classifier and KNN regression methods.

*KNN tries to estimate a conditional probability of X belonging to a certain class depending on the fraction of the points nearest the test observation, the KNN classifier will classify a class whereas the KNN regression method will take the average of the K amount of points nearest the test observation.*

## Q3.
Suppose we have a data set with five predictors, X1 = GPA, X2 = IQ, X3 = Gender (1 for Female and 0 for Male), X4 = Interaction between GPA and IQ, and X5 = Interaction between GPA and Gender. The response is starting salary after graduation (in thousands of dollars).
Y = 50 + 20GPA + .07IQ + 35Gender + .01GPAIQ - .10GPAGender.

#### (a) Which answer is correct, and why?

*For a fixed value of IQ and GPA, males earn more on average than females provided that the GPA is high enough. Because if Female = 0 and Male = 1.*
*M: Y = 50 + 20GPA + 35 -.10GPAGender + .07IQ + .01GPAIQ 
*F = Y = 50 + 20GPA + .07IQ + .01GPAIQ

85 + 10GPA <= 50 + 20GPA ; solve for GPA which is 3.5 so unless GPA is greater than 3.5 males will earn more on a fixed value of IQ and GPA.

#### (b)Predict the salary of a female with IQ of 110 and a GPA of 4.0.
* 50 + 80 + 0 + 0 + 7.7 + 4.4 = $142,100

#### (c)True or false: Since the coefficient for the GPA/IQ interaction term is very small, there is very little evidence of an interaction effect. Justify your answer.
* False because we have to do hypothesis testing and look at the p value, not the coefficient.

## Q4.
I collect a set of data (n = 100 observations) containing a single predictor and a quantitative response. I then fit a linear regression model to the data, as well as a separate cubic regression,

#### Suppose that the true relationship between X and Y is linear. Consider the training residual sum of squares (RSS) for the linear regression, and also the training RSS for the cubic regression. Would we expect one to be lower than the other, would we expect them to be the same, or is there not enough information to tell? Justify your answer
What about testing as well.
* The more flexible models will always fit the training data more despite the relationship it will do just worse in the testing unless the relationship was not truly linear.

## Q6.
Argue that in the case of simple linear regression, the least squares line always passes through the (average of x , average of y)

*The solution for the normal equations to estimate the intercept is the average of y * least squares estimate for b1 * the average of x.
If you substitute that into the regression line of Y = bo - b1X and the average of X into b1X you get :
Y = average of Y - b1(mean X) + b1(meanx) = 0 . With Y = mean(Y). 


