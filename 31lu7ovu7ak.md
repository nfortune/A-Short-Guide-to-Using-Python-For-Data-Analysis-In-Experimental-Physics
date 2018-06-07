```
fit, covariance = curve_fit(polarization_model_1, theta, V_pd, 
                       p0 = initial_guess, 
                       sigma = V_pd_delta, absolute_sigma = True)
                       
I_0 = fit[0]
phi_0 = fit[1]
offset = fit[2]
```