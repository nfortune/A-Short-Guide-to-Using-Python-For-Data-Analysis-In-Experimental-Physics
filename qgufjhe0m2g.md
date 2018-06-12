```
def polarization_model_1( phi, V_0, phi_0, V_1): # variation of light intensity with  relative polarizer angle
    return V_0 * (1 + cos(2 * (phi - phi_0)))/2 + V_1
```