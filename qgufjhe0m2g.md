```
def polarization_model_1(phi, I_0, phi_0, offset): # variation of light intensity with  relative polarizer angle 
    return I_0 * (1 + cos(2 * (phi - phi_0)))/2 + offset
```