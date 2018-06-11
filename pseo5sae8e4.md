```
# example: direct numpy import style 

from numpy import loadtxt

filename = '650 nm calibration.csv'
angle, V_pd, V_pd_delta = loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True)
```