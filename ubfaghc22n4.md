```
# import numpy as np

def photodiode_error(phi_array, delta_V_0, delta_phi, delta_V_1, V_0, phi_0):  
    V_0_error= (delta_V_0 / V_0) * (np.cos(phi_array - phi_0))**2
    phi_error = (delta_phi) * (2 * np.cos(phi_array- phi_0) * np.sin(phi_array - phi_0))
    V_1_error= (delta_V_1 / V_0) 
    fractional_error = np.sqrt(V_0_error **2 + phi_error **2 + V_1_error **2)
    return fractional_error * V_0
```