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
$$
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
$$

$$ 5 + 5 $$
