```
%matplotlib inline

% from numpy import loadtxt, savetxt, array  #omit if already entered earlier
from matplotlib import pyplot as plt         #this is the traditional method

from matplotlib import rc                    #this allows you to change overall settings
rc('xtick', labelsize = 18)                  #use 18 point font for numbering on x axis
rc('ytick', labelsize = 18)                  #use 18 point font for numbering on y axis

plt.figure(figsize = (7,5))                  #specify figure size as 7 x 5 inches
                                             #for default size, type plt.figure() 
plt.xlabel(r"$\theta$ [degrees]", fontsize = 18)
plt.ylabel(r"$V_{pd}$ [volts]", fontsize = 18)


```