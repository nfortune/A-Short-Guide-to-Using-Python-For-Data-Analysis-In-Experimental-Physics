```
plt.figure(figsize = (11,8))                  #specify figure size as 7 x 5 inches
                                             #for default size, type plt.figure() 
                                             
plt.xlabel(r"$\theta$ [degrees]", fontsize = 18) #label axis (using LaTeX commands)
plt.ylabel(r"$V_{pd}$ [mV]", fontsize = 18)   #use 18 point font for label text

#plt.errorbar(angle_fit, V_pd_fit, xerr = None, yerr = None, 
color = 'red', label = 'fit to physical model' )
plt.errorbar(angle, V_pd,  
    xerr=None, yerr=data_uncertainty, 
    linestyle = 'none', 
    color = 'blue',  
    capsize = 3, capthick = 2, label = "original data points")

plt.errorbar(angle_fit, interpolated_data, xerr = None, yerr = None, color = 'black', label = 'cubic spline interpolation')


plt.xlim(-15, 375)
plt.ylim(-2.5, 40)
plt.xticks([0,   30, 60, 90, 120, 150, 180, 210, 240, 270, 300, 330, 360], 
           ('0', '', '', 90,  '',  '', 180,  '',  '', 270,  '',  '', 360))
plt.legend(loc = 'best')
    
plt.show() 
```