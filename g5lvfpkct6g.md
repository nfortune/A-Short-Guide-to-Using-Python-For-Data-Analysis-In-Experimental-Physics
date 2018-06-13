```
%matplotlib inline
from matplotlib import pyplot as plt  

from numpy import *
from uncertainties import ufloat, unumpy

filename = 'Calibration_650nm.csv'
angle, V_pd, delta_V= loadtxt(filename, delimiter = ',', skiprows = 1, usecols = (1, 2), unpack = True) 

#define measured values V_0, 
```