```
from numpy import savetxt
output_filename = 'output.csv'                   #provide a name for the new file
header_row_text = 'angle, V_pd, V_pd_delta'      #this is optional


data = array([angle, V_pd, V_pd_delta]).T        #create a 2D matrix and transpose rows and columns 
savetxt(output_filename, data, delimiter = ',')  #save the data to the file in csv format
```