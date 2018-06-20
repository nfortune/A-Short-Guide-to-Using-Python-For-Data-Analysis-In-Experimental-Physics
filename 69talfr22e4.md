```
%matplotlib inline
import matplotlib as mpl
import matplotlib.pyplot as plt

import numpy as np
from scipy.interpolate import interp1d

file_name = 'Calibration_650nm_result.csv' 
file_folder = '/Users/nfortune/data/' 

angle, V_pd, data_uncertainty  = np.loadtxt(file, delimiter = ',', skiprows = 1, usecols = (0, 1, 2), unpack = True)
```