```
#create array of new angle values for interpolation
new_angle_values = np.linspace(0, 360, 180)   # in degrees

#evaluate at new anglevalues
interpolated_data = interpolating_function(new_angle_values) 
```