```
# example: direct import method of data file

from numpy import loadtxt   #only need to use this once per program

filename = 'Calibration_650nm.csv'                                   # replace with the name of your csv data file
#filefolder = 'Python_Workspace/'                                    # replace with relative address of your csv data file 


data_file = filefolder + filename

angle, V_pd, V_pd_error  = loadtxt(data_file, delimiter = ',', skiprows = 1, unpack = True)
```