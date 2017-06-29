Regression Case Study
======================

The goal of the contest is to predict the sale price of a particular piece of
heavy equipment at auction based on it's usage, equipment type, and configuration.
The data is sourced from auction result postings and includes information on usage
and equipment configurations.

Evaluation
======================
The evaluation of the model is based on Root Mean Squared Log Error. Which
is computed as follows:

![](images/rmsle.png)

where *p<sub>i</sub>* are the predicted values and *a<sub>i</sub>* are the target
values.

Data
======================
The data for this case study are in `./data`. There are both training and testing data sets,
the testing data set will only be utilized to evaluate your final model performance.

Model
======================
I ran XGBoost and lightGBM on this data and got RMSLE scores of `0.346` and `0.449` respectively. Although lightGBM performed worse, it took a tenth of the time, so I could have run more rounds and perhaps gotten the same score as XGBoost. Both of these algorithms are state-of-the-art and outperformed the benchmark, which had a score of `0.0`. The iPython Notebook `workflow.ipynb` contains all the work done for this project with step-by-step instructions to how the results were obtained.
