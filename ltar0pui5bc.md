```
import numpy as np
from pint import UnitRegistry
unit = UnitRegistry()
width = (10. * unit.centimeter).plus_minus(.1, relative=True) # 10 percent uncertainty
length = (20. * unit.centimeter).plus_minus(2.) # 2 cm uncertainty
area = length * width

print(width)
print(length)
print('{:~P}'.format(area))

(10.0 +/- 1.0) centimeter
(20.0 +/- 2.0) centimeter
(200 ± 28) cm²
```