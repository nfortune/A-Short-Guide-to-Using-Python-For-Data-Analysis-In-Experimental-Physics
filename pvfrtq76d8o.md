```
```
import numpy as np                       # import a few needed functions from the numpy package

angle_in_degrees = array([0, 30, 60, 90]) # create an array with elements corresponding to 0, 30, 60, and 90 degrees 
angle_in_radians = degrees * pi / 180     # convert to radians
x = cos(angle_in_radians)                 # calculate cosine for each element in array, assign values to an array called 'x'
y = sin(angle_in_radians)                 # calculate sine for each element in array, assign values to an array called 'y'

print(y)
```
```