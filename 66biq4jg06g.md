```
import numpy as np
import pint

unit = pint.UnitRegistry()  # for clarity, we use 'unit' instead of the default 'ureg'
Q_ = unit.Quantity 

g  = 9.8  * unit.newton / unit.kg # define quantities with units
m = Q_(1.0, 'kg')  # an alternative method

force = m * g  #define calculated quantity

print(force) 
9.8 newton  # sample output
```