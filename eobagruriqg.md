```
# example: traditional import method 

import numpy as np # only need this once per program

filename = 'Calibration_650nm.csv'
angle, V_pd, V_pd_error = np.loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True) # load the data
```