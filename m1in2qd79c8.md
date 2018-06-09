```

theta = angle * pi / 180  # convert to radians

# make initial estimates from data

V0   = 33.0    #peak value - offset voltage, in mV
phi0 = 0.0   #offset angle, in radians
V1   = 0.2 #offset voltage, in mV

V0_error = 0.014 # data implies zero, but let's assume same as V1_error
phi0_error = 1 * pi / 180 # assume 1 degree error
V1_error = 0.014 # in mV estimate from data 

initial_guess=array([V0, phi0, V1])



V_pd_estimated_error = sigma(theta, V0_error, phi0_error, V1_error, V0)

fit, covariance = curve_fit(polarization_model_1, theta, V_pd, 
                       p0 = initial_guess, 
                       sigma = V_pd_estimated_error, absolute_sigma = True)
                       
I_0 = fit[0]
phi_0 = fit[1]
offset = fit[2]

error = sqrt(diag(covariance))

```