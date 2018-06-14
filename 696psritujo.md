```
# example: direct import method of data file

from numpy import loadtxt   #only need to use this once per program

filename = 'Calibration_650nm.csv'    # replace with the name of your csv data file
filefolder = ''                       # use this if your data file is in the same folder as your python program
#filefolder = 'Python_Workspace/'     # use this if data file is in a subfolder called  with relative address of your csv data file 


data_file = filefolder + filename

angle, V_pd, V_pd_error  = loadtxt(data_file, delimiter = ',', skiprows = 1, unpack = True)
```