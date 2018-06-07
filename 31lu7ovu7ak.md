```
fit, covariance = curve_fit(polarization_model_1, theta, V_pd, 
                       p0 = initial_guess, 
                       sigma = V_pd_delta, absolute_sigma = True)
                       
error = sqrt(diag(covariance))

```