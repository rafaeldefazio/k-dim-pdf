# Editing Multivariate normal distribution PDF


From [Wikipedia](https://en.wikipedia.org/wiki/Multivariate_normal_distribution):

<img src="https://render.githubusercontent.com/render/math?math=PDF=(2\pi)^{-\frac{k}{2}}\det(\boldsymbol\Sigma)^{-\frac{1}{2}} \, e^{ -\frac{1}{2}(\mathbf{x} - \boldsymbol\mu)^{{{\!\mathsf{T}}}} \boldsymbol\Sigma^{-1}(\mathbf{x} - \boldsymbol\mu)}">

# `nth_dimension_pdf()` function

## Parameters
- xyzk_vector: numpy array with k 'x' values `np.array([1, 3, 5])`
- mi_vector: numpy array with mu values, same length as xyzk_vector `np.array([1, 1, 5])`
- sigma_matrix: k x k matrix

## Inside the code
- f1 is <img src="https://render.githubusercontent.com/render/math?math=(2\pi)^{-\frac{k}{2}}">
- f2 is <img src="https://render.githubusercontent.com/render/math?math=\det(\boldsymbol\Sigma)^{-\frac{1}{2}}">
- f3 is <img src="https://render.githubusercontent.com/render/math?math=e^{ -\frac{1}{2}(\mathbf{x} - \boldsymbol\mu)^{{{\!\mathsf{T}}}} \boldsymbol\Sigma^{-1}(\mathbf{x} - \boldsymbol\mu)}">

## Tests
Tests were performed using R with the library [mvtnorm](https://cran.r-project.org/web/packages/mvtnorm/index.html), using the functions `rmvnorm` to generate numbers and and `dmvnorm` to test them.

### rmvnorm: Generate data with the multivariate normal (i.e., Gaussian) distribution

Function generates data from the multivariate normal distribution given some mean vector and/or covariance matrix.

### dmvnorm: Multivariate normal distribution density function

These functions provide the density function and a random number generator for the multivariate normal distribution with mean equal to ‘mean’ and covariance matrix ‘sigma’.
