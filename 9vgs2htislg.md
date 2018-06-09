```
from numpy import cos, sin  # (or import *) if not done already 

def sigma(phi_array, delta_V0, delta_V1, delta_phi, V_0 ): 
    V_0_error = (delta_V0 / V_0)**2 * (cos(phi_array))**4
    V_1_error = (delta_V0 / V_0)**2 
    phi_error = (delta_phi)**2 * (2 * cos(phi_array) * sin(phi_array))**2
    fractional_error = V_0_error + V_1_error + phi_error
    
```