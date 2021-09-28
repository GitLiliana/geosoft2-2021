Author: [@GitLiliana](https://github.com/GitLiliana)

Issue: [#5](https://github.com/Geosoft2/geosoft2-2021/issues/5)

# Area of Applicability - Theory

This handout aims to summarise the preprint paper 'Predicting into unkown space? Estimating the area of applicability of spatial prediction models' by Meyer and Pebesma (2020) with focus on motivation/problemstatement and methodology.

## Motivation

Spatial mapping of environmental variables is important to reveal spatial patterns and changes of the environment. A common method in this context is the predictive modelling using machine learning algorithms as the relationships between environmental variables are complex. On the basis of field data statistical models are trained to make predictions for the entire area of interest which is quite often on a global scale. The field data normally is not evenly distributed and does not cover the entire study area. Nevertheless predictions are often made for areas which lack training data. This is especially problematic for heterogenous landscapes which might differ considerably in its properties from what has been observed in the training data. This might lead to areas for which the model does not give reliable predictions. This arises the following questions:
1. What is the model's area of applicability (AOA)?
2. How can the area of applicability be estimated?
 

## Methodology

### Basic Idea

As differences between areas play an important role in the applicability of a model, an index which describes the dissimilarity between data points is calculated. This is the so called 'dissimilarity index' (DI) which is based on the minimum distance to the training data within the multdimensional predictor space. Due to varying importance of the environmental variables within the model the predictors are weighed before calculating distances.
As cross-validation is common for machine learning models, the AOA is defined as the area for which, on average, the cross-validation error applies. This area is estimated by using a threshold of the DI. This threshold is derived from comparison between the prediction error within the AOA and the cross-validation error of the model.
Finally, the approach is illustrated in a simulated case study.

Summarized this leads to:
1. Calculate DI for expressing differences between data points.
2. Define AOA by applying threshold of DI.

### Calculating the Dissimilarity Index

### Defining the Area of Applicability

## Results from Case Study

## References

[Meyer, H. and Pebesma, E. (2020): Predicting into unkown space? Estimating the area of applicability of spatial prediction models. Preprint](https://arxiv.org/abs/2005.07939)
