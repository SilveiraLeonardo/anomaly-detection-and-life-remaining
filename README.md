# Paper Studied

## Long Short Term Memory Networks for Anomaly Detection in Time Series
Pankaj Malhotra, Lovekesh Vig, Gautam Shroff, Puneet Agarwal


In this paper, we demonstrate that by modelling the normal behaviour of a time series via stacked LSTM networks, 
we can accurately detect deviations from normal behaviour without any pre-specified context window or preprocessing.


 We use a predictor to model normal behaviour, and subsequently use the prediction errors to identify abnormal behaviour. 
 (This is particularly helpful in real-world anomaly detection scenarios where instances of normal behaviour may be available in 
 abundance but instances of anomalous behaviour are rare.) In order to ensure that the networks capture the temporal structure of the sequence, 
 we predict several time steps into the future.
 
 
 The probability distribution of the errors made while predicting on normal data is then used to obtain the likelihood of normal 
 behaviour on the test data. When control variables (such as vehicle accelerator or brake) are also present, the network is made to predict the control variable 
 in addition to the dependent variables. This forces the network to learn the normal usage patterns via the joint distribution of the prediction errors for the control and dependent sensor variables.'
 
We compute an error vector e(t) for point x(t) as
e(t) = [e(t),...,e(t),...,e(t),...,e(t)], where e(t) is the difference between x(t) and 
its value as predicted at time t − j.


The error vectors are modelled to fit a multivariate Gaussian distribution N = N(μ,Σ). The likelihood p(t) of observing an error vector e(t) 
is given by the value of N at e(t)


An observation x(t) is classified as ‘anomalous’ if p(t) < τ, else the observation is classified as ‘normal’.
The sets vN2 and vA are used to learn τ by maximizing Fβ-score (where anomalous points belong to positive class and normal points 
belong to negative class).
