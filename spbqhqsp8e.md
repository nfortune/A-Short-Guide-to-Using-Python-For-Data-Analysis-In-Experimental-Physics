```
#to calculate values while also automatically taking into account uncertainties, use unumpy instead of numpy
V_pd_theory = (1/2)*V_0 * (1 + unumpy.cos(2*(theta_array - theta_0 ))) + V_1 #notice use of unumpy.cos

values = unumpy.nominal_values(V_pd_array)  #creates an array with best estimates of V_pd
uncertainties = unumpy.std_devs(V_pd_array) #creates an array with uncertainties for V_pd
```