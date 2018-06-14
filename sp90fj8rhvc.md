```
# example: traditional numpy import style 

import numpy as np # if you use this, 'numpy' is replaced with the abbreviation 'np'

filename = 'Calibration_650nm.csv'
angle, V_pd, V_pd_error = np.loadtxt(filename, delimiter = ',', skiprows = 1, usecols = (1unpack = True) # load the data
```