```
from scipy.signal import savgol_filter  

window_width = 25                              # number of points over which data is fit and smoothed
polynomial_order = 2                     # order of polynominal used to fit data (must be less than window_width)

data_spacing = 0.1  # data_spacing = x_

smoothed_data   = savgol_filter(noisy_data, window_width, polynomial_order)                             #smooth data
data_derivative = savgol_filter(noisy_data, window_width, polynomial_order, deriv = 1, delta = 0.1) #take 1st derivative, declare spacing delta_x = 0.1 between data points y(x_i)  

```