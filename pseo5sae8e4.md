```
# example: direct numpy import style 

from numpy import loadtxt
#from numpy 

filename = '650 nm calibration.csv'
angle, V_pd = loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True)
```