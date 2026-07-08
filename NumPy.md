Vectorization & Broadcasting used to increase speed.
multidimensional indexing is faster than chain indexing.

Vectorization Code Example- { for a array of daily stock prices you want to calculate a simple daily price change.
a. Python Loop: 
  prices = [100.0, 102.5, 101.2, 103.0, 104.5]
  gains = []
  for i in range (1, len(prices))
      gains.append((prices[i] - prices[i - 1] / prices[i - 1])
b. NumPy Vectorization:
  import numpy as np
  prices = np.array([100.0, 102.5, 101.2, 103.0, 104.5]
  gains = (prices[1:] - prices[:-1] / prices[:-1]

Broadcasting Code Example-
a. 1D x 0D
  returns = np.array([0.01, -0.02, 0.05, 0.00])
  scaled_returns = returns * 2
b. 2D x 1D
  matrix = np.ones((4, 3)) * 0.02
  rf_rates = np.array([0.005, 0.006, 0.004])
  excess_returns = matrix - rf_rates
c. 2D x 2D
  benchmark = np.array([0.001, 0.002, 0.001, 0.003])
  benchmark_col = benchmark[:, np.newaxis]
  adjusted_matrix = matrix - benchmark_col

np.where(condition, x, y) - acts as a vectorized ternary operator.
np.dot / @ - for calculating portfolio variance.
np.linalg.inv / np.lingalg.eig - used for mean variance optimization and principal component analysis for yield curve modeling.

