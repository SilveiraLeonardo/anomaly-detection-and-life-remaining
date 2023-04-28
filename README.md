# Papers Studied

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


## Predicting Remaining Useful Life using Time Series Embeddings based on Recurrent Neural Networks
Narendhar Gugulothu, Vishnu TV, Pankaj Malhotra, Lovekesh Vig, Puneet Agarwal, Gautam Shroff


An RNN is used as an encoder to obtain a fixed- dimensional representation that serves as an embedding for multi- sensor time series data. The health of a machine at any point of time can be estimated by comparing an embedding computed using recent sensor history with representative embeddings computed for periods of normal behavior. 


Our approach for RUL estimation does not rely on degradation trend assumptions, can handle noise and missing values, and can capture complex temporal dependencies among the sensors.


Our proposed approach handles noise in sensor readings by learning robust representations from sensor data via RNN Encoder- Decoder (RNN-ED) models.


## Graph Neural Networks for Leveraging Industrial Equipment Structure: An application to Remaining Useful Life Estimation


In this work, we explore the applicability of GGNNs to explicitly model the underlying graph-structured mechanism of IoT-enabled complex equipment. We represent the struc- ture of a particular complex equipment as a directed graph where each node corresponds to a subset of sensors (e.g. those from the same module), and an edge models the re- lationship or dependency between two nodes or subsets of sensors (e.g. the dependence of a module on another mod- ule).
