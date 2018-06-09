```

V0   = 33.0    #peak value - offset voltage, in mV
phi0 = 0.0   #offset angle, in radians
V1   = 0.2 #offset voltage, in mV

initial_guess=array([V0, phi0, V1])

theta = angle * pi / 180  # convert to radians

V_pd_estimated_error = sigma(theta, V0, phi0, )

fit, covariance = curve_fit(polarization_model_1, theta, V_pd, 
                       p0 = initial_guess, 
                       sigma = V_pd_delta, absolute_sigma = True)
                       
I_0 = fit[0]
phi_0 = fit[1]
offset = fit[2]

error = sqrt(diag(covariance))

```