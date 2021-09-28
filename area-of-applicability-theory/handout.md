Author: [@GitLiliana](https://github.com/GitLiliana)

Issue: [#5](https://github.com/Geosoft2/geosoft2-2021/issues/5)

# Area of Applicability - Theory

This handout aims to summarise the preprint paper 'Predicting into unkown space? Estimating the area of applicability of spatial prediction models' by Meyer and Pebesma (2020) with focus on motivation/problemstatement and methodology.

## Motivation

Spatial mapping of environmental variables is important to reveal spatial patterns and changes of the environment. A common method in this context is the predictive modelling using machine learning algorithms as the relationships between environmental variables are complex. On the basis of field data statistical models are trained to make predictions for the entire area of interest which is quite often on a global scale. The field data normally is not evenly distributed and does not cover the entire study area. Nevertheless predictions are often made for areas which lack training data. This is especially problematic for heterogenous landscapes which might differ considerably in its properties from what has been observed in the training data. It might lead to areas for which the model does not give reliable predictions because it has no knowledge about them. This arises the following questions:
1. What is the model's area of applicability (AOA)?
2. How can the area of applicability be estimated?
 

## Methodology

### Basic Idea

1. **Calculate dissimilarity index (DI):** As differences between areas play an important role in the applicability of a model, an index which describes the dissimilarity between data points is calculated. This is the so called 'dissimilarity index'. It is based on the minimum distance to the training data within the multdimensional predictor space using weighed predictor variables.
2. **Estimating the AOA by applying threshold of the DI:** The threshold of the DI is derived from comparison between the prediction error within the AOA and the cross-validation error of the model.

### Calculating the Dissimilarity Index (DI)

1. **Standardization of predictor variables:** To ensure that all variables are treated equally they are scaled by the following formula.
![scaledVar](/images/scaledVar.png)
3. **Weighing of variables:** To reflect the variable importance the scaled variables are multiplied with an impotance estimate w<sub>j</sub> which is provided by most machine learning models.
4. **Distance calculation:** The distance between two point a and b in the predictor variable space is calculated using the euclidean distance.
5. **Minimum distance for a prediction point:** For a new prediction point k, the distance to the nearest training data point is determined by the following formula.
6. **Obtain dissimilarity index:** Standardize the minimum distances by deviding d<sub>k</sub> by the average of pairwise distances in the training data.

### Estimating the Area of Applicability

## Results from Case Study

## References

[Meyer, H. and Pebesma, E. (2020): Predicting into unkown space? Estimating the area of applicability of spatial prediction models. Preprint](https://arxiv.org/abs/2005.07939)
