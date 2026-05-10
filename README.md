# Geometric-Analysis-of-Point-Processes-with-Applications-in-Machine-Learning.

RAUC (Relative Area Under the Curve) is a novel geometric metric designed to analyze the structure of two-dimensional point processes. This measure quantifies the degree of spatial randomness or clustering in a point cloud, facilitating the interpretation of complex relationships in Machine Learning workflows.

Unlike classical correlation measures (such as Pearson) which are limited to linear associations, RAUC captures non-linear dependencies through the geometry of the data. It utilizes concepts of alpha-shapes and empty-space functions to compare an observed point distribution against a Complete Spatial Randomness (CSR) model.

**Key Features:** 
- Scalar Interpretation: Provides a numerical value where values close to 0 indicate strong clustering patterns, and higher values reflect a transition toward spatial randomness.
- Scale Independence: Input data is normalized via a min-max transformation to the unit square $^2$ before calculation.
- Versatility: Applicable to feature selection in regression and evaluating dimensionality reduction techniques (e.g., PCA, UMAP).

**Methodology:**

The RAUC calculation follows these fundamental steps:
- Normalization: Transformation of input variables to the $$ interval to ensure comparability.
- Geometric Construction: Generation of alpha-shapes for the point cloud over a discrete grid of radii $\alpha$.
- Empty-Space Loss Function ($f^j(\alpha)$): Defines the proportion of empty space within the unit square as the radius $\alpha$ increases.
- CSR Reference: A homogeneous Poisson process is used as a null model to compare the empirical curve.
- Ratio Calculation: RAUC is defined as the ratio between the area under the curve of the CSR process and the area under the curve of the empirical loss function.- 

 **Use Cases:**
 - Feature Selection in Regression.
RAUC allows for ranking predictors based on their geometric relevance to the target variable. For instance, in datasets like the Boston Housing data, variables with lower RAUC values indicate persistent geometric structures and stronger relationships with the dependent variable.
 - Dimensionality Reduction Evaluation.
It is used to objectively compare hyperparameter configurations in algorithms like UMAP or PCA, identifying which settings produce the most defined clusters and the least amount of spatial noise.

📝 Academic Reference: This project is based on the research by: 
Dylan Benavides, National High Technology Center (CeNAT), Costa Rica.
