```
# example: traditional numpy import style 

import numpy as np # this allows you to type the abbreviation 'np' instead of 'numpy' when needed

filename = '650 nm calibration with erro.csv'
angle, V_pd, V_pd_delta = np.loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True) #notice the np. prefix! 
```