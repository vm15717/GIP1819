## Reduced Order Modelling 
Steps:
1. Apply forces to the finite element model
2. Get displacement outputs from the finite element model
3. Convert forces and displacements to modal forces and modal displacements
4. Repeat 1 till 3 for different forces
5. Perform a curvefit to find the coefficients of nonlinear terms using the modal forces and modal displacements
