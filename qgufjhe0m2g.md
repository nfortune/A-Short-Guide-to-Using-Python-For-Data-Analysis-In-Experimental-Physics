```
# import numpy as np

def polarization_model( phi_array, V_0, phi_0, V_1): # Malus's law 
    return V_0 * (1 + np.cos(2 * (phi_array - phi_0)))/2 + V_1
```