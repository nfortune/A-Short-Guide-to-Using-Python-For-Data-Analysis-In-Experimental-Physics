```
def polarization_model_( phi_array, V_0, phi_0, V_1): # variation of light intensity with  relative polarizer angle
    return V_0 * (1 + cos(2 * (phi_array - phi_0)))/2 + V_1
```