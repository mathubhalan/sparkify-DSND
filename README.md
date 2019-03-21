## Predictive Analytics - Customer Churn using pyspark

### Introduction
This purpose of the project is to predict the customer chrun for company named sparkify with pyspark. Sparkify is an imaginary music app service provided, who provides service in both free and paid mode for their customers.
The dataset is 128 MB, subset of the full 12 GB dataset. It has around 2,86,500 records pertaining to two months of event data for 226 users.
More context on this analysis and interpretation of the results can be found in this blog post on [Medium](https://medium.com/@mathubhalang/predictive-analytics-customer-churn-d9443a03752a)

### File Structure
. **Sparkify.ipynb:** this is the Spark notebook which contains all the code for this analysis. In order to run it, `pyspark`, `pandas`, `matplotlib`, `seaborn` and `datetime` have to be installed.
. **Sparkify.html:** an HTML version of the notebook.

### Analysis
Loading and cleaning the dataset, created new features. Loaded the crafted dataset into machine learning algorithm like `Random forest`, `Logistic Regression` and `GBT Classifier` using the spark `pipeline` and compared their accuracy and F1 score. `Random Forest` classifier performed well compared to other two with `73% accuracy` and `0.72 as F1 score`. 
We did hyperparameter turing using `Cross Validation` and `Grid Search` to improve the performance of model, but it doen't provide a good perfromance might be due to very minimal amount of data. 

### Possible Improvements
This analysis would gain from leveraging a larger dataset and being deployed on a cluster. Grid search is a particularly computationally expensive operation, but with larger resources and more time a more extensive search over a larger dataset and hyperparameter space could be conducted to further tune the model and likely improve overall accuracy.