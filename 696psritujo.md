```
# example: direct import method of data file

from numpy import loadtxt   #only need to use this once per program

filename = 'Calibration_650nm.csv'                                   # replace with the name of your csv data file! 
#filefolder = 'jove.smith.edu/user/nfortune/tree/Python_Workspace/'  # address of your c
filefolder = ''                     #this assumes the data file is in the same folder as your python program

angle, V_pd, V_pd_error  = loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True)
```