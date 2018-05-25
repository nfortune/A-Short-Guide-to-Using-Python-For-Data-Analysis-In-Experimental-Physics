```
>>> mass_magnitudes = np.array([0.1, 0.2, 0.5, 1.0, 2.0, 5.0, 10.0])
>>> masses = mass_magnitudes * unit.kg
>>> print('{:~P}'.format(masses))

[  0.1   0.2   0.5   1.    2.    5.   10. ] kg

masses.magnitude

array([  0.1,   0.2,   0.5,   1. ,   2. ,   5. ,  10. ])

print('{:~P}'.format(masses * g))
[  0.98   1.96   4.9    9.8   19.6   49.    98.  ] N
```