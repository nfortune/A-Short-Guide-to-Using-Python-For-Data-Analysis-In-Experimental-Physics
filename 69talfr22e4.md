```
#setup Jupyter notebook 
%matplotlib inline

#import packages and functions
import matplotlib as mpl
import matplotlib.pyplot as plt
import numpy as np
from scipy.interpolate import interp1d  # this is the 1d iterpolation 

file_name = 'Calibration_650nm_result.csv' 
file_folder = '/Users/nfortune/data/' 

angle, V_pd, data_uncertainty  = np.loadtxt(file_folder + file_name, delimiter = ',', skiprows = 1, usecols = (0, 1, 2), unpack = True)
```