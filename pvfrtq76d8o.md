```
#traditional import 
import numpy as np                            # you only need to type this once in each program

angle_in_degrees = np. array([0, 30, 60, 90]) # create an array with elements corresponding to 0, 30, 60, and 90 degrees 
angle_in_radians = degrees * np.pi / 180      # convert to radians
x = np.cos(angle_in_radians)                  # calculate cosine for each element in array, assign values to an array called 'x'
y = np.sin(angle_in_radians)                 # calculate sine for each element in array, assign values to an array called 'y'

print(y)
```