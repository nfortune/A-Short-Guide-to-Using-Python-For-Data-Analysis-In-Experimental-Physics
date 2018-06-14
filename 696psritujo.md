```
# example: direct import method of data file

from numpy import loadtxt   #only need to use this once per program

filename = 'Calibration_650nm.csv'                # replace with the name of your csv data file
filefolder = ''                                   # use this if your data file is in the same folder as your python program
#filefolder = 'data/'                             # use this if data file is in a subfolder called data ('relative' address)
#filefolder = '/Users/nfortune/Python_Workspace'  # use this if data file is in a different folder called 

data_file = filefolder + filename

angle, V_pd, V_pd_error  = loadtxt(data_file, delimiter = ',', skiprows = 1, unpack = True)
```