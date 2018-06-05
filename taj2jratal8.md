```
from numpy import savetxt

output_filename = 'output.csv'                   #provide a name for the new file
header_row_text = 'angle, V_pd, V_pd_delta'      #make first row of file be a li column names as text in first row. this is optional
comment_text = ''                                #do not start header row with a '#' this is optional. 
                                                 #the default is start the header row with a '#' 

data = array([angle, V_pd, V_pd_delta]).T        #create a 2D matrix and transpose rows and columns 
savetxt(output_filename, data, delimiter = ',', header = header_row_text, comments = '') # 
```