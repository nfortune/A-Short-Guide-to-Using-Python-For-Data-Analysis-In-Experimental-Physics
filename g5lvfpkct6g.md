```
%matplotlib inline
from matplotlib import pyplot as plt  

from numpy import *
from uncertainties import ufloat, unumpy

filename = 'Calibration_650nm.csv'
angle_data, V_pd_data = loadtxt(filename, delimiter = ',', skiprows = 1, usecols = (1, 2), unpack = True) 

#define measured values V_0 ± delta_V_0, V_1 ± delta_V_1, etc  
V_0 = ufloat(32.631, 0.024) # first element is the nominal value, the second is the standard dev, both in mV
V_1 = ufloat(0.023, 0.016) # first element is the nominal value, the second is the standard dev, both in mV
theta_0 = ufloat(-1.16, 0.11) * pi / 180  # convert from degrees to radians 

theta_data = angle_data * pi / 180
delta_theta = 0.5 * pi / 180

theta_array = unumpy.uarray(theta)
```