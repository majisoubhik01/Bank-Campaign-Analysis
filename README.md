## About Project:

The project was on Bank Campaign analysis. So there is a bank who wants to find out who are the customers which are most likely to respond to their marketing campaign for a Term Policy.

The bank provided us with the historical data of similar campaigns organized by the bank.
The data had customer demographics such as age, job, etc, account information such as balance, loan defaults; previous campaign methods and outcomes such as by what methods they were communicated about the campaign and did they buy the term policy or not.
Our goal was to propose such a solution which will enable our client to target their customers better, and thus save money and improve customer satisfaction by calling the right customer for the right product.
It was a classification problem, so we proceeded with Exploratory data analysis of the data.
We did it in Excel. Plotted histograms and bar graphs so as to check for outliers.
There wasn't any missing data.
Now after the EDA was complete, we imported the data in jupyter notebook and proceeded with our findings from EDA.

The machine only understands numbers, so we had to convert the categorical values into numerical so as to use those in our models.
Here, we transformed the categorical variables into numerical variables using label encoding. There were many job profiles so it was difficult to deal with them using label encoding, instead we put them in categories so as to reduce the number of categories.
For example retired and student were kept in one category, blue collar and management posts were kept in one category. Then after categorising those, we converted those to numerical values.

We then standardised the columns balance and duration so that the algorithms used for the models won't be biased and would also train and converge faster.

After we were done with the pre processing steps, it was time to run some models on this data and get accuracies for training and testing data.
So here we split the data into training and testing datasets using the train test split methods available in scikit learn library.
We ran 6 models here, namely Logistic Regression, Decision Trees, Random Forest, k-Nearest Neighbour, Support Vector Machines and Naive Bayes and got the accuracies for training and testing datasets.
We proceeded with Random Forest model as it gave us the highest training accuracy as well as testing accuracy and performed hyperparameter tuning to improve the accuracy on testing dataset.
After we were satisfied with the accuracies, we used the method "probability predictor" available in Random Forest model to predict the probabilities of each customer buying the term policy and merged it with our final dataset and exported it.
With this, our work in python was finished.

Now we open this exported file in Excel and we can see there is a column in the end which has probabilities for y=1 which is the probability that the customer will buy the term policy.
So we will sort this column from largest value to smallest value and the result will be list of highly probable customers.

We present this list to our client and explain what we have done.
So the first 500 customers from this list have high chances of buying the term policy.
Our client will send this list of customers to their call centres and we believe 200 customers will buy the term policy.
If they had chosen random 500 customers, let's say 50 of them would have bought the term policy.
So if our client makes 10$ per customer then he would make 500$ from those customers.
But if they use our list then there will ~150 more customers, that means 1500$ profit and will also save their time.
