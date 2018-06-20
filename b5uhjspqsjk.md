```
#construct an interpolating function from the data
interpolating_function = interp1d(angle, V_pd, kind = 'cubic') # create interpolation function

#create array of new angle values for interpolation
new_angle_values = np.linspace(0, 360, 180)   # in degrees

#evaluate at new angle values
interpolated_data = interpolating_function(new_angle_values) 
```