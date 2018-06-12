```
plt.figure(figsize = (11,8))                  #specify figure size as 7 x 5 inches
                                             #for default size, type plt.figure() 
                                             
plt.xlabel(r"$\theta$ [degrees]", fontsize = 18) #label axis (using LaTeX commands)
plt.ylabel(r"$V_{pd}$ [volts]", fontsize = 18)   #use 18 point font for label text

# plot the data as before
plt.errorbar(angle, V_pd,  
    xerr=None, yerr=V_pd_delta, 
    linestyle = 'none', 
    color = 'blue',  
    capsize = 3, capthick = 1, label = "data")

#create curve showing fit to data 
angle_fit = linspace(0, 360, 180)
theta_fit = angle_fit * pi / 180
V_pd_fit = polarization_model(theta_fit, fit[0], fit[1], fit[2])

#plot the curve fit 
plt.errorbar(angle_fit, V_pd_fit, xerr = None, yerr = None, color = 'red', label = 'fit' )
plt.xlim(-15, 375)
plt.ylim(-2.5, 40)
plt.xticks([0,   30, 60, 90, 120, 150, 180, 210, 240, 270, 300, 330, 360], 
           ('0', '', '', 90,  '',  '', 180,  '',  '', 270,  '',  '', 360))
plt.legend(loc = 'best')
    
plt.show()  
```