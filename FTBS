import numpy as np

#parameter
nx = 1000
nt = 2500
dx = 1/nx
dt = dx*0.8
#int
u = np.zeros(nx)
for i in range(nx):
    if((i>=299 and i<=699)):
        u[i] = 1

un = u.copy()
#calculate
for n in range(nt):
    u = un.copy()
    for i in range(nx):
        un[i] = u[i]-(u[i]-u[i-1])*dt/dx
    un[0] = un[999]

np.savetxt('ftbs_u',un)
