```
from scipy.stats import chi2          # 'chi-square' goodness of fit calculation

data_uncertainty = V_pd_delta         # this is an assumption

chisq = sum((residual/ data_uncertainty))**2
degrees_of_freedom = len(residual) - len()
reduced_chisq = chisq / degrees_of_freedom  # this should be close to one
CDF = chi2.cdf(chisq, degrees_of_freedom)  

print('chi-square         = ',chisq)
print('degrees of freedom = ',degrees_of_freedom)
print('reduced chi-square = ',reduced_chisq)
print('fractional probability of chisq ≤', chisq, 'for ', degrees_of_freedom, 'dof is', CDF)
```