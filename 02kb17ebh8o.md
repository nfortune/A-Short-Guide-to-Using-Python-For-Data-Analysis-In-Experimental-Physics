```
%matplotlib inline

import matplotlib as mpl
from matplotlib import pyplot as plt #this is the traditional method

mpl.rc('xtick', labelsize = 18)      #use 18 point font for numbering on x axis
mpl.rc('ytick', labelsize = 18)      #use 18 point font for numbering on y axis

plt.figure(figsize = (7,5))          #specify figure size as 7 x 5 inches
                                     #for default size, type plt.figure() 
                                             
plt.xlabel(r"$\theta$ [degrees]", fontsize = 18) #label axis (using LaTeX commands)
plt.ylabel(r"$V_{pd}$ [volts]", fontsize = 18)   #use 18 point font for label text

plt.errorbar(angle, V_pd,  
    xerr=None, yerr=V_pd_error, 
    linestyle = 'none', 
    color = 'blue',  
    capsize = 3, capthick = 1)
    
plt.show()    
```