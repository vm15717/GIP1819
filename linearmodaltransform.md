---
layout: page
---
# Linear Modal Transform
Consider the following second order differential equation  
$$
M\ddot{x}+C\dot{x}+Kx=f_{x}
$$
the matrix equation is transformed using $$x=\Phi \mathit{q}$$  
$$
x=\mathbf{\Phi} q\\
\mathbf{\Phi}\ddot{q}+\mathbf{M^{-1}K}\mathbf{\Phi}q+\mathbf{Nu(\Phi \mathit{q})}=0\\
\mathbf{\Phi}^{\mathrm{T}}\mathbf{\Phi}\ddot{q}+\mathbf{\Phi}^{\mathrm{T}}\mathbf{M^{-1}K}\mathbf{\Phi}q+\mathbf{\Phi}^{\mathrm{T}}\mathbf{Nu(\Phi \mathit{q})}=0\\
\ddot{q}+\mathbf{\Lambda}{q}+\mathbf{Nu_{q}(\Phi \mathit{q})}=0
$$
