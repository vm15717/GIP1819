---
layout: page
---
## Reduced Order Modelling 
Steps:
1. Apply forces to the finite element model
2. Get displacement outputs from the finite element model
3. Convert forces and displacements to modal forces and modal displacements
4. Repeat steps from 1 till 3 for different forces
5. Perform a curvefit to find the coefficients of nonlinear terms using the modal forces and modal displacements
## Theory 
There two methods currently used in deriving reduced order models. They are:
..1. AMF - Applied Modal Force and 
..2. EMD- Enforced Modal Displacement  
In the AMF method, a set of forces are applied to the finite element model. A static analysis is done and the displacements are used in finding the Reduced Order Model which is described below.  
Consider a 2 DOF system with the following equations describing the dynamics
$$
f_{q1}=\omega_{1}^2q_{1}+\alpha_{1}q_{1}^{2}+\alpha_{2}q_{1}q_{2}+\alpha_{3}q_{2}^2+\alpha_{4}q_{1}^3+\alpha_{5}q_{1}^2q_{2}+\alpha_{6}q_{1}q_{2}^2+\alpha_{7}q_{2}^3 \\f_{q2}=\omega_{2}^2q_{2}+\beta_{1}q_{1}^{2}+\beta_{2}q_{1}q_{2}+\beta_{3}q_{2}^2+\beta_{4}q_{1}^3+\beta_{5}q_{1}^2q_{2}+\beta_{6}q_{1}q_{2}^2+\beta_{7}q_{2}^3
$$
where $$q_{1}$$ and $$q_{2}$$ are the modal displacements. $$\omega_{1}$$ and $$\omega_{2}$$ are the natural frequencies of the system.
$$\alpha_{i}$$s and $$\gamma_{i}$$s are the coefficients of the higher order terms.  
Regression analysis was done using the data collected to estimate the coefficients $$\alpha_{1}$$ and $$\alpha_{2}$$.  
$$
\begin{bmatrix}
\hat{F_{1}}^{(1)}-k_{1}\hat{q_{1}}^{(1)} \\ \hat{F_{1}}^{(2)}-k_{1}\hat{q_{1}}^{(2)} \\ \hat{F_{1}}^{(3)}-k_{1}\hat{q_{1}}^{(3)} \\...\\\hat{F_{1}^{(i)}}-k_{1}\hat{q_{1}}^{(i)}\\...\\...
\end{bmatrix}
=
\begin{bmatrix}
\hat{q_{1}^{(1)}}^{2}& \hat{q_{1}^{(1)}}^{3} \\ \hat{q_{1}^{(2)}}^{2} & \hat{q_{1}^{(2)}}^{3} \\
\hat{q_{1}^{(3)}}^{2} & \hat{q_{1}^{(3)}}^{3} \\...&...\\\hat{q_{1}^{(i)}}^{2} & \hat{q_{1}^{(i)}}^{3} \\... &...\\...&...
\end{bmatrix}
$$
$$
\begin{bmatrix}
\alpha_{1} \\ \alpha_{2} 
\end{bmatrix}
$$
The above equation is represented in a simple form as follows
$$
\mathbf{F}=\mathbf{Q}\mathbf{\alpha} \\ \mathbf{\alpha}=\mathbf{Q^{-1}}\mathbf{F}
$$
In the EMD method, a set of displacements are inputted into the Finite element model and the forces are found out. A curve fit is done between the displacements and the 
