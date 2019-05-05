# PDE-Constrained-Optimization
Numerical Methods for PDE Constrained Optimization (Preconditioning Iterative Methods)

# Solver Process
Step 1 Pre-process step: information of the nodal element and indices

Step 2 Process step: 
1-Compute the stiffness matrix and load vector of the elements 
2- Assemble the global stiffness matrix and global load vector 
3-Deal with the boundary condition 
4-Solve the linear system AU = F
 
Step 3 post-process step: visualization of results
