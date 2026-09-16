# SPREAD_LOCATOR_ANALYSIS_PR3
Project 3 – Transaction Data Distribution Analysis

Project Overview
This project analyses transaction data using probability distributions,
statistical techniques, transformations, and visualization methods in Python.

The main purpose is to understand transaction occurrence, transaction counts,
and transaction amounts through different statistical models.
Dataset
Dataset file: spread_locator_dataset.xlsx

The analysis uses transaction-related fields such as:

transaction_amount – amount of each transaction

transaction_date – date of the transaction

transaction_count – transaction count

transaction_status – Success or Fail

Tools and Libraries Used

Python
Pandas
NumPy
SciPy
Statsmodels
Matplotlib
Seaborn
Google Colab
Analysis Performed
1. Bernoulli and Binomial Distribution
The transaction status was converted into a binary outcome:
Success = 1
Fail = 0
The success probability was calculated from the dataset.

Weekly transaction counts were also approximately modelled using a Binomial
distribution. Since weekly counts do not naturally have a fixed number of
trials, this was treated as an approximate model.

2. Poisson Distribution
The number of transactions per day was analysed using a Poisson distribution.
The average number of transactions per day was approximately 7.10.
3. Log-Normal and Power Law Distribution
Transaction amounts were modelled using:
Log-Normal distribution
Power Law distribution
The models were compared using AIC. The calculated results showed a lower AIC
for the Log-Normal model, so it provided the better relative fit among the two
models tested.

4. Q-Q Plot and Normality
A Q-Q plot was generated to check whether transaction amounts followed a
normal distribution.
The transaction amounts showed noticeable deviation from the normal reference
line and a right-skewed pattern.

5. Box-Cox Transformation
A Box-Cox transformation was applied to transaction amounts to reduce skewness
and improve the shape of the distribution.
The estimated Box-Cox lambda was approximately -0.18.

6. Z-Score and Probability Above ₹5000
The Z-score of ₹5000 was calculated using:
Z = (X - Mean) / Standard Deviation
Results:
Mean transaction amount: ₹3365.19
Standard deviation: ₹1985.71
Z-score for ₹5000: 0.82
Estimated normal upper-tail probability: 20.52%
The Z-score indicates that ₹5000 is approximately 0.82 standard deviations
above the mean.

7. PDF and CDF
Probability Density Function (PDF) and Cumulative Distribution Function (CDF)
were plotted for transaction amounts using the fitted Log-Normal model.
The PDF shows the density of transaction amounts, while the CDF shows the
cumulative probability up to a given transaction amount.
8. Final Conclusion
The analysis shows that transaction amounts are not normally distributed and
have a right-skewed pattern.

Among the Log-Normal and simple Power Law models tested, the Log-Normal model
gave the lower AIC and therefore the better relative fit for this dataset.

The Poisson distribution was useful for daily transaction counts, while the
Bernoulli distribution represented transaction success and failure.

Overall, the analysis demonstrates how probability distributions,
transformations, and statistical plots can be used to understand transaction
data and support data-driven interpretation.

Project Files

A_Statistical_Distribution_Analysis_model_ipynb.ipynb – Google Colab/Jupyter
analysis notebook

spread_locator_dataset.xlsx – transaction dataset

README.md – project documentation

How to Run

Open the .ipynb file in Google Colab.

Upload spread_locator_dataset.xlsx.

Run the notebook cells from top to bottom.

Review the calculated values, plots, and conclusions.

Key Learning Outcomes

Through this project, the following concepts were practised:

Bernoulli Distribution

Binomial Distribution

Poisson Distribution

Log-Normal Distribution

Power Law Distribution

Q-Q Plot

Normality checking

Box-Cox Transformation

Z-Scores

Probability estimation

PDF and CDF

Statistical interpretation

Distribution comparison
AUTHOR 
PATHAN SAHIL
