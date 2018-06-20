```
#create array of angle values for interpolation
new_angle_values = np.linspace(0, 360, 180)   # in degrees

#interpolate data
interpolating_function = interp1d(angle, V_pd, kind = 'cubic') # create interpolation function

interpolated_data = interpolating_function(new_angle_values) #interpolate at new_angle_values
```