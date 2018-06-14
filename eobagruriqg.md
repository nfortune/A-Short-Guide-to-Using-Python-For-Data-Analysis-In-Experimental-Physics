```
# example: traditional import method 

import numpy as np # only need this once per program

file_name = 'Calibration_650nm.csv'               # replace with the name of your csv data file

file_folder = ''                                  # use this if your data file is in the same folder as your python program

#file_folder = 'data/'                            # use this if data file is in a _subfolder_ called data 
                                                  # this is called 'relative addressing'
                                                  
#file_folder = '/Users/nfortune/data'            # use this if data file is in a folder called 'Python_Workspace' 
                                                  # inside the folder 'nfortune' within the 'Users' directory 
                                                  # such as when using the Jupyter webserver jove.smith.edu
                                                  # this is called 'absolute addressing'

data_file = file_folder + file_name

angle, V_pd, V_pd_error  = np.loadtxt(data_file, delimiter = ',', skiprows = 1, unpack = True)
```