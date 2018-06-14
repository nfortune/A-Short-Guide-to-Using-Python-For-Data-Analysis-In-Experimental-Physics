```
# example: direct import method 

from numpy import loadtxt   #import just the numpy command loadtxt
#from numpy import *        #an alternative method that imports _all_ numpy commands. Be 

filename = 'Calibration_650nm.csv'  #this assumes the data file is in the same folder as your python program
angle, V_pd, delta_V_pd  = loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True)
```