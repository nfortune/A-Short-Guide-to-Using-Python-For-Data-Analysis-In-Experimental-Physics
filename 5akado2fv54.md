```
chisq = sum((residual/ V_pd_delta))**2
degrees_of_freedom = len(residual) - 3
reduced_chisq = chisq / degrees_of_freedom
CDF = chi2.cdf(chisq, degrees_of_freedom)
print('chi-square         = ',chisq)
print('degrees of freedom = ',degrees_of_freedom)
print('reduced chi-square = ',reduced_chisq)
print()
print('fractional probability of chisq ≤', chisq, 'for ', degrees_of_freedom, 'dof is', CDF)
```