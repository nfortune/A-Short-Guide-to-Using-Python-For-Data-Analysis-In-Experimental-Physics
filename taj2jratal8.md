```
from numpy import savetxt

data = array([angle, V_pd, V_pd_delta]).T        #crea
output_filename = 'output.csv'
savetxt(output_filename, data, delimiter = ',')


```