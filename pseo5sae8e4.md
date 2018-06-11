```
# example: direct numpy import style 

from numpy import loadtxt   #import just the numpy command loadtxt
#from numpy import *        #an alternative method that imports all numpy commands

filename = '650 nm calibration.csv'
angle, V_pd = loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True)
```