```
# example: traditional import method 

import numpy as np # only need this once per program

filename = 'Calibration_650nm.csv' #this assumes the data file is in the same folder as your python program
angle, V_pd, V_pd_error = np.loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True) # load the data
```