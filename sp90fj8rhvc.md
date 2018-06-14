```
# example: traditional numpy import style 

import numpy as np # if you use this, 'numpy' is replaced with the abbreviation 'np'

filename = 'Calibration_650nm.csv'
angle, V_pd, delta_V_pd = np.loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True) # load the data
```