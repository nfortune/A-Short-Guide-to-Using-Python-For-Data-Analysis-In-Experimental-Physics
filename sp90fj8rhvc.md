```
# example: traditional numpy import style 

# import numpy 
import numpy as np # this allows you to type the abbreviation 'np' instead of 'numpy' when needed

filename = '650 nm calibration.csv'

angle, V_pd, delta_V_pd = np.loadtxt(filename, delimiter = ',', skiprows = 1, unpack = True) 
#notice the required np. prefix because of the use of import numpy as np 
```