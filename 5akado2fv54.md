```
from scipy.stats import chi2          # 'chi-square' goodness of fit calculation

chisq = sum((residual/ data_uncertainty))**2
degrees_of_freedom = len(residual) - len(initial_guess)
reduced_chisq = chisq / degrees_of_freedom  # this should be close to one
CDF = chi2.cdf(chisq, degrees_of_freedom)   # this should be close to 50 percent

print('chi-square         = ',chisq)
print('degrees of freedom = ',degrees_of_freedom)
print('reduced chi-square = ',reduced_chisq)
print('fractional probability of chisq ≤', chisq, 'for ', degrees_of_freedom, 'dof is', CDF)
```