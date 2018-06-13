```
%matplotlib inline
from matplotlib import pyplot as plt  

from numpy import *
from uncertainties import ufloat, unumpy

filename = 'Calibration_650nm.csv'
angle_array, V_pd_array = loadtxt(filename, delimiter = ',', skiprows = 1, usecols = (1, 2), unpack = True) 

#define measured values V_0 ± delta_V_0, V_1 ± delta_V_1, etc  
V_0 = ufloat(32.631, 0.024) # mV
V_1 = ufloat(0.023, 0.016) # mV

```