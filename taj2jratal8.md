```
from numpy import savetxt

output_filename = 'output.csv'                   #provide a name for the new file
header_row_text = 'angle, V_pd, V_pd_delta'      #make first row of file be a list of column names. Optional. 
comment_text = ''                                #do not start header row with a '#'. Optional. 
#comment_text = '#'                              #starting the header row with a '#'

data = array([angle, V_pd, V_pd_delta]).T        #create a 2D matrix and transpose rows and columns 
savetxt(output_filename, data, delimiter = ',', header = header_row_text, comments = comment_text) 
```