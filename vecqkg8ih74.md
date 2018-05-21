```
import numpy as np 
# numpy (NUmerical PYthon) is a ubiquitous numerical analysis package for python 
# 'as np' allows us to use the standard abbreviation 'np' in place of 'numpy' 

import pint # a useful package for calculations using units

unit = pint.UnitRegistry()  # here we use 'unit' instead of the more standard 'ureg' for clarity
Q_ = unit.Quantity 

gravitational_field_strength  = 9.8  * unit.newton / unit.kg
g = gravitational_field_strength.to_base_units()

print(gravitational_field_strength)
print('{:~P}'.format(gravitational_field_strength))
print('')


```