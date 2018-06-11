```
from numpy import savetxt, array                 #assumes you haven't already imported these commands

output_filename = 'output.csv'                   #provide a name for the new file
header_row_text = 'angle, V_pd'      #make first row of file be a list of column names. Optional. 
comment_text = ''                                #do not start header row with a '#'. Optional. 
#comment_text = '#'                              #start the header row with a '#' . Default setting. 

data = array([angle, V_pd, delta]).T        #create a 2D matrix and transpose rows and columns (clever trick) 
savetxt(output_filename, data, delimiter = ',', header = header_row_text, comments = comment_text) 
```