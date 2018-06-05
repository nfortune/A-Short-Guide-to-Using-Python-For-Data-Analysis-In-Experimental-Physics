```
from numpy import savetxt

data = array([angle, V_pd, V_pd_delta]).T        #create a 2D matrix and transpose rows and columns 
output_filename = 'output.csv'                   
savetxt(output_filename, data, delimiter = ',')


```