```
# load curve_fit routine from scipy
from scipy.optimize import curve_fit # import method used here

# alternative method (as recommended in hdocs.scipy.org/doc/scipy/reference.api.html)
#from scipy import optimize
#fit, covariance = optimize.curve_fit(...)

#run curve_fit for polarization_model
fit, covariance = curve_fit(polarization_model, theta, V_pd, 
                            p0 = initial_guess, 
                            sigma = estimated_error, absolute_sigma = True)

error = np.sqrt(np.diag(covariance))

print(old_fit)
print(fit)

old_fit = np.copy(fit)

print()
print('V_0    = ','{:.3f}'.format(fit[0]), '±', '{:.3f}'.format(error[0]), ' mV')
print('V_1 = ','{:.4f}'.format(fit[2]), '±', '{:.3f}'.format(error[2]), ' mV')
print('theta_0  = ','{:.4f}'.format(fit[1]), '±', '{:.4f}'.format(error[1]), 'radian')
print('       = ','{:.4f}'.format(fit[1]*180/pi), '±', '{:.4f}'.format(error[1]*180/pi), 'degrees')

```