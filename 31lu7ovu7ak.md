```
theta_array = angle * pi/180 


estimated_error = sigma(theta_array, dV0, dtheta, dV1, V0, theta0 )

fit, covariance = curve_fit(polarization_model, theta_array, V_pd, 
                       p0 = initial_guess, 
                       sigma = estimated_error, absolute_sigma = True)
                       
                       
                       
I_0 = fit[0]
phi_0 = fit[1]
offset = fit[2]

error = sqrt(diag(covariance))

print()
print('I_0    = ','{:.3f}'.format(fit[0]), '±', '{:.3f}'.format(error[0]), ' mV')
print('offset = ','{:.4f}'.format(fit[2]), '±', '{:.3f}'.format(error[2]), ' mV')
print('phi_0  = ','{:.4f}'.format(fit[1]), '±', '{:.4f}'.format(error[1]), 'radian')
print('       = ','{:.4f}'.format(fit[1]*180/pi), '±', '{:.4f}'.format(error[1]*180/pi), 'degrees')

```