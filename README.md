# Portfolio-Strategy-Risk-Pairity - (Still Work In Progress)

This project used MLFinLab to optimise portfolio using Hierarchical Risk Pairity (HRP) and Hierarchical Equal Risk Contribution (HERC) models.
Both models used agglomerative clustering algorithm to cluster different shares based on their price or returns. The main difference between HERC and HRP is that
HERC allocate assets equally in each cluster based on the cluster risk contribution, while HRP is more like a vanilla risk pairity model.

Two techniques were used as our benchmark. Risk pairity built using both Numpy and Pandas and equally weighted strategies.

Three different covariance measures were tested as part of this project:

1. Minimum Covariance Determinant
    "The basic idea of the algorithm is to find a set of observations that are not outliers and compute their empirical covariance matrix, 
     which is then rescaled to compensate for the performed selection of observations"
     
2. Maximum Likelihood Covariance Estimator
   "Maximum Likelihood Estimator of a sample is an unbiased estimator of the corresponding population’s covariance matrix”
   
3. Exponentially-Weighted Covariance Matrix
   Use exponential smoothing technique to create an accurate representation of our stocks covariance. Hence, more recent price/returns information carry more
   weight compared to older information

From my experiments, I found no significant differences between these covariance estimators. Hence, for this project I chose Exponentially-Weighted Covariance Matrix
since I personally quite love the idea of exponential smoothing to create better estimation of the stock covariance matrix.

Lastly, I backtested the all portfolio models. Overall, for the selected set of shares, I found that equally weighted is just as good or even better compared to other
techniques. This seems to confirm that basic risk pairity models do not work for Australian stock. You can find the article here: https://www.schroders.com/en/au/advisers/insights/white-papers/risk-parity---no-free-lunch1/

Please note that I'm in no way an expert in finance.
Hence, this result should be taken with a grain of salt.
</br><b>USE THIS MODEL AT YOUR OWN RISK</b>
