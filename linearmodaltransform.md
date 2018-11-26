---
layout: page
---
# Linear Modal Transform
Consider the following second order differential equation  
$$
\mathbf{M}\ddot{x}+\mathbf{C}\dot{x}+\mathbf{K}x+\mathbf{Nu(x)}=f_{x}  
$$  
the matrix equation is transformed using $$x=\mathbf{\Phi} q\\$$  and the mass matrix is inverted and multiplied through the equation.
$$
\mathbf{\Phi}\ddot{q}+\mathbf{M^{-1}C}\mathbf{\Phi}\dot{q}+\mathbf{M^{-1}K}\mathbf{\Phi}q+\mathbf{Nu(\Phi \mathit{q})}=f_{x}\\
\mathbf{\Phi}^{\mathrm{T}}\mathbf{\Phi}\ddot{q}+\mathbf{\Phi}^{\mathrm{T}}\mathbf{M^{-1}C}\mathbf{\Phi}\dot{q}+\mathbf{\Phi}^{\mathrm{T}}\mathbf{M^{-1}K}\mathbf{\Phi}q+\mathbf{\Phi}^{\mathrm{T}}\mathbf{Nu(\Phi \mathit{q})}=\mathbf{\Phi}^{\mathrm{T}}f_{x}\\
\ddot{q}+\mathbf{\zeta}\dot{q}+\mathbf{\Lambda}{q}+\mathbf{Nu_{q}(\Phi \mathit{q})}=f_{q}
$$
