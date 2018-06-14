```
# example: direct import method of data file

from numpy import loadtxt   #import just the numpy command loadtxt

filename = 'Calibration_650nm.csv'  #this assumes the data file is in the same folder as your python program
angle, V_pd, V_  = loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True)

```