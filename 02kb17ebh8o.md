```
%matplotlib inline

% from numpy import loadtxt, savetxt, array  #omit if already entered earlier
from matplotlib import pyplot as plt         #this is the traditional method

from matplotlib import rc                    #this allows you to change overall settings
rc('xtick', labelsize = 18)                  #use 18 point font for numbering 
rc('ytick', labelsize = 18) #18 point font

plt.figure()
plt.xlabel(r"$\theta$ [degrees]", fontsize = 18)
plt.ylabel(r"$V_{pd}$ [volts]", fontsize = 18)


```