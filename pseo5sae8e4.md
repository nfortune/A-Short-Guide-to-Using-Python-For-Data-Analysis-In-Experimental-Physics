```
# example: direct numpy import style 

from numpy import loadtxt
#from numpy import *        #an alternative method that imports everything

filename = '650 nm calibration.csv'
angle, V_pd = loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True)
```