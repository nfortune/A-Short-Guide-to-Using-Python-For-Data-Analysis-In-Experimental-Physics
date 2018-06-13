```
%matplotlib inline
from matplotlib import pyplot as plt  

from numpy import *
from uncertainties import ufloat, unumpy

filename = 'Calibration_650nm.csv'
angle, V_pd, delta_V_pd = loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True) 
angel, vapid = loadtxt(filename, delimiter = ',', skiprows = 1, usecols = (1, 2), unpack = True)
```