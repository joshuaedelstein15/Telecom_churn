#### 05/01/2023
#### Joshua Edelstein



# Telecom Churn Analysis
## Overview

Most telecom companies suffer from churn(loss of customers to competition). Churn rate has strong impact on the life time value of the customer because it affects the length of service and the future revenue of the company. For example if a company has 25% churn rate then the average customer lifetime is 4 years; similarly a company with a churn rate of 50%, has an average customer lifetime of 2 years. It is estimated that 75 percent of the 17 to 20 million subscribers signing up with a new wireless carrier every year are coming from another wireless provider. Telecom companies spend hundreds of dollars to acquire a new customer and when that customer leaves, the company not only loses the future revenue from that customer but also the resources spent to acquire that customer.

Telecom companies have used two approaches to address churn - (a) Untargeted approach and (b) Targeted approach. The untargeted approach relies on creating brand loyalty in hopes of retaining customers. The targeted approach relies on identifying customers who are likely to churn, and then providing intervention to encourage them to stay.<a name="cite_ref-1"></a>[<sup>[1]</sup>](#cite_note-1)

<a name="cite_note-1"></a>1. [^](#cite_ref-1) Data from CrowdAnalytix, https://www.crowdanalytix.com/contests/why-customer-churn

## Business Understanding

SyriaTel is a smaller end wireless provider, they don't have such the budget to invest in a large scale advertising campaign. However, they also can't afford to keep losing customers. Therefore they have turned to us to create a model for predicting which customers will churn. When a customers has been determined as likely to churn they will reach out to them in hopes of keeping the customer.

In this scenario we will break the data into 2 categories: 1) the columns used to predict churn(predictors) 2) the target column of whether the customers churned or not. If churn is "True" that means the customer churned, and "False" if the customer didn't churn. 

In general it is important to consider beforehand whether a false positive or false negative is worse. In each specific case one should tune their model based on what is more important. In our case a false positive means that we predicted the customer would churn when they didn't. The outcome of this is that we will send them some promotional deals, and perhaps give them a discount. This will in turn cause a slight loss of profit, as these clients were already happy paying full price. On the other hand, a false negative is when we predict that a customer won't churn when really they will. This means that we will lose a customer without ever sending them promotional deals to try to get them to stay. The loss from this mistake is far greater then the loss from a false positive. As such when we are creating models we will attempt to minimize false negatives(maximize recall) as much as possible.

<div>
<img src="Images/telephone_poles.jpg", width = 800, height = 400/>
</div>

Photo by <a href="https://unsplash.com/@giggiulena?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Mario Caruso</a> on <a href="https://unsplash.com/photos/0C9VmZUqcT8?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
  
