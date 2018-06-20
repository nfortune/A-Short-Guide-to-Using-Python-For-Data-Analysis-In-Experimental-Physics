```
from scipy.interpolate import InterpolatedUnivariateSpline


InterpolatingUnivariateSpline_function = InterpolatedUnivariateSpline( angle, V_pd, k = 4) # k = 4 means 4th order

#create array of new angle values for interpolation
new_angle_values = np.linspace(0, 360, 180)   # in degrees

# generate new data values
IUS_interpolated_data = InterpolatingUnivariateSpline_function(angle_fit)
```