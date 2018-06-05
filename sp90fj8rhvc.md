```
import numpy as np # this allows you to type the abbreviation 'np' instead of 'numpy' when needed

filename = '650 nm calibration with error.csv'
angle, V_pd, V_pd_delta = nloadtxt(filename, delimiter = ',', skiprows = 1, unpack = True)
```