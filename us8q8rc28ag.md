```
estimated_error = photodiode_error(theta, delta_V0, delta_theta, delta_V1, fit[0], fit[1]) # propagate error using new values for V0, et

fit, covariance = curve_fit(polarization_model, theta, V_pd, 
                            p0 = initial_guess, 
                            sigma = estimated_error, absolute_sigma = True)

error = np.sqrt(np.diag(covariance))

print(old_fit)
print(fit)

old_fit = np.copy(fit)

V_pd_model = polarization_model(theta, fit[0], fit[1], fit[2])
residual = V_pd - V_pd_model

data_uncertainty = photodiode_error(theta, delta_V0, delta_theta, delta_V1, fit[0], fit[1])

chisq = sum((residual/ data_uncertainty))**2
degrees_of_freedom = len(residual) - len(initial_guess)
reduced_chisq = chisq / degrees_of_freedom  # this should be close to one
CDF = chi2.cdf(chisq, degrees_of_freedom)   # this should be close to 50 percent

print('chi-square         = ',chisq)
print('degrees of freedom = ',degrees_of_freedom)
print('reduced chi-square = ',reduced_chisq)
print('fractional probability of chisq ≤', chisq, 'for ', degrees_of_freedom, 'dof is', CDF)
```