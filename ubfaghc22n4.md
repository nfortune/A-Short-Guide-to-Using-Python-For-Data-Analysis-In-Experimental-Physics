from numpy import cos, sin, sqrt, pi  # (or import *) if not done already 

def sigma(phi_array, delta_V0, delta_phi, delta_V1, V_0 ):  #calculate delta_V_pd
    V_0_error_sq= (delta_V0 / V_0)**2 * (cos(phi_array))**4
    phi_error_sq = (delta_phi)**2 * (2 * cos(phi_array) * sin(phi_array))**2
    V_1_error_sq = (delta_V0 / V_0)**2 
    fractional_error = sqrt(V_0_error_sq + V_1_error_sq + phi_error_sq)
    return fractional_error * V_0