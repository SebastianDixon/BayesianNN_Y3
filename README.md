# BayesianNN_Y3
Bayesian Neural Network regression on California Housing Dataset using MCMC and Variational Approximation

# Introduction

This is an investigation of Bayesian neural networks (BNNs) to manage uncertainty in comparison of
two approximation methods; variation approximation (VA), and Markov Chain Monte Carlo (MCMC).
The comparison of effectiveness will be quantified through the following scores: accuracy,
computational efficiency, and real-world data applicability. 

# Dataset

https://www.kaggle.com/datasets/camnugent/california-housing-prices

I have chosen to use the California Housing prices dataset, designed for regression analysis of the
median house price for California districts from the 1990 census. The housing market is a
relatively volatile industry, and is quite dependent on demand and supply fluctuations, not to mention
economic factors such as interest rates & inflation, so it’s a challenge to predict the price variation
over time. It's also a challenge to predict housing prices due to the limited data available, most datasets
contain a limited number of features related to each property, prioritising feature engineering in this use
case.

By investigating the position of these houses, I found that producing a feature representing a
combination of the longitude and latitude to have significant positive correlation to the median value of
the housing, which I will refer to as the “value” feature. The haversine distance is the angular distance
between two points on the surface of a sphere and is often used as a representation for both longitude
and latitude. This feature showed weak positive correlation with the value, and therefore through feature
engineering I developed a stronger representation of the position. This feature accounts for a greater
percentage of the variance in the data and therefore represents more information. 
The Position feature has 0.56 pairwise correlation against the target variable Value.
