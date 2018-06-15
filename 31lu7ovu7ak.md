```
estimated_error = photodiode_error(theta, delta_V0, delta_theta, delta_V1, 
    V0, theta0)    #start with initial values

fit, covariance = curve_fit(polarization_model, theta, V_pd, 
                            p0 = initial_guess, 
                            sigma = estimated_error, absolute_sigma = True)

error = np.sqrt(np.diag(covariance))

print(old_fit)
print(fit)

old_fit = np.copy(fit)

data_uncertainty = photodiode_error(theta, delta_V0, delta_theta, delta_V1, 
    fit[0], fit[1])  # updated values for V0, V1

print()
print('V_0    = ','{:.3f}'.format(fit[0]), '±', '{:.3f}'.format(error[0]), ' mV')
print('V_1 = ','{:.4f}'.format(fit[2]), '±', '{:.3f}'.format(error[2]), ' mV')
print('theta_0  = ','{:.4f}'.format(fit[1]), '±', '{:.4f}'.format(error[1]), 'radian')
print('       = ','{:.4f}'.format(fit[1]*180/pi), '±', '{:.4f}'.format(error[1]*180/pi), 'degrees')

```