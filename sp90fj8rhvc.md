```
# example: traditional numpy import style 

# import numpy     # if you use this, replace 'np' with 'numpy' in the loadtxt command
import numpy as np # if you use this, 'numpy' is replaced with the abbreviation 'np'

filename = 'Calibration_650.csv'

angle, V_pd, delta_V_pd = np.loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True) 
#notice the required np. prefix because of the use of import numpy as np 
```