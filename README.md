# crypto-forecast

# Topic
Predict cryptocurrency trend based on sentiment analysis of discussions on forums and other data.

### Table of contents

1. [Data sources](#data)
2. [APIs](#api)
3. [Data science steps](#steps)
4. [Resources](#resources)
5. [Ethical guidelines](#ethics)

### Data sources <a name="data"></a>
### APIs<a name="apis"></a>
### Data science<a name="steps"></a>
Below are only examples of how to address each step
1. Define objective and response/output to model  

What to predict: we can have more models:
* model to predict sentiment from conversation (classifier: positive/negative)
* model to predict if the currency value will increase or decrease (classifier: yes/no)
* optional: model to say how much the currency will increase (regression model or time series forecast)

2. Collect data sources  
Datasets used to predict: currency evolution, conversations, etc.

3. Model sentiment prediction: apply all the text data preprocessing and modelling steps e.g. like [here](https://towardsdatascience.com/sentiment-analysis-with-python-part-1-5ce197074184) or [here](https://scikit-learn.org/stable/tutorial/text_analytics/working_with_text_data.html)  

a. Clean and prepare data: label (if you don't have the label already) conversations for several  days/time points as positive/negative 

b. Define features and extract features from data for sentiment prediction as in the above article  

c. Train and validate model for sentiment prediction  

d. Predict for more conversations  

4. Model currency evolution  

a. Clean and prepare data  
* turn the currency data in a [date, trend] signal (smoothen/filter the signal, differentiate to get trend) 
* merge currency data with sentiment predictions based on date
* to use only past conversations to predict the currency, one must add columns in the dataset, for each past point in time to be used, and introduce a delay by shifting the rows - for each column by the delta to the present time  

b. Define features and extract features from data, e.g. column(s) with positive/negative label of past conversations, if specific keywords are mentioned, other market signals 

c. Train and validate model TBD

### Resources<a name="resources"></a>  
[Bitcoin prediction project 1](https://hackernoon.com/how-i-created-a-bitcoin-trading-algorithm-with-a-29-return-rate-using-sentiment-analysis-b0db0e777f4)  
[Bitcoin prediction project 2](https://hackernoon.com/forecasting-bitcoin-price-with-crowdsourced-algorithms-part-ii-753f9ac99d07)  
[Arbitrage](https://towardsdatascience.com/cryptocurrency-arbitrage-how-to-profit-from-it-e2d7bf805fde)  
[Social impact](https://hackernoon.com/blockchain-for-social-good-reviewing-top-use-cases-in-2018-85b6b36f4c3d)

### Ethical guidelines <a name="ethics"></a>

TBD
