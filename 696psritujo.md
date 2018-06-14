```
# example: direct import method of data file

from numpy import loadtxt   #only need to use this once per program

file_name = 'Calibration_650nm.csv'                # replace with the name of your csv data file

file_folder = ''                                  # use this if your data file is in the same folder as your python program

#file_folder = 'data/'                            # use this if data file is in a _subfolder_ called data 
                                                  # this is called 'relative addressing'
                                                  
#file_folder = '/Users/nfortune/Python_Workspace' # use this if data file is in a folder called 'Python_Workspace' 
                                                  # inside the folder 'nfortune' within the 'Users' directory 
                                                  # such as when using the Jupyter webserver jove.smith.edu
                                                  # this is called 'absolute addressing'

data_file = filefolder + filename

angle, V_pd, V_pd_error  = loadtxt(data_file, delimiter = ',', skiprows = 1, unpack = True)
```