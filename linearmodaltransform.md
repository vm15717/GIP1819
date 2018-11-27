---
layout: page
---
# Linear Modal Transform
Consider the following second order differential equation  
$$
\mathbf{M}\ddot{x}+\mathbf{C}\dot{x}+\mathbf{K}x+\mathbf{Nu_{x}(x)}=\mathbf{f_{x}}  
$$  
where $$\mathbf{M}$$ is the Mass matrix, $$\mathbf{C}$$ is the Damping Matrix and $$\mathbf{K}$$ is the Stiffness matrix.  
$$\mathbf{Nu_{x}(x)}$$ is the Nonlinear part and $$\mathbf{f_{x}}$$ is a vector of forces.
the matrix equation is transformed using $$x=\mathbf{\Phi} q$$.
$$
\mathbf{M}\mathbf{\Phi}\ddot{q}+\mathbf{C}\mathbf{\Phi}\dot{q}+\mathbf{K}\mathbf{\Phi}q+\mathbf{Nu_{x}(\Phi \mathit{q})}=\mathbf{f_{x}}\\
\mathbf{\Phi}^{\mathrm{T}}\mathbf{M}\mathbf{\Phi}\ddot{q}+\mathbf{\Phi}^{\mathrm{T}}\mathbf{C}\mathbf{\Phi}\dot{q}+\mathbf{\Phi}^{\mathrm{T}}\mathbf{K}\mathbf{\Phi}q+\mathbf{\Phi}^{\mathrm{T}}\mathbf{Nu_{x}(\Phi \mathit{q})}=\mathbf{\Phi}^{\mathrm{T}}\mathbf{f_{x}}\\
\ddot{q}+\mathbf{\zeta}\dot{q}+\mathbf{\Lambda}{q}+\mathbf{Nu_{q}(\Phi \mathit{q})}=\mathbf{f_{q}}
$$
So if 
$$
x=\mathbf{\Phi} q
$$
then 
$$
f_{x}={(\mathbf{\Phi}^{\mathrm{T}})}^{-1}f_{q}
$$
