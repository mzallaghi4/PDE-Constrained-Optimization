# PDE-Constrained-Optimization
Numerical Methods for PDE Constrained Optimization (Preconditioning Iterative Methods with Domain Decomposition)

Domain Decomposition Preconditioning (DDP) is a technique used to solve large-scale linear systems that arise in the numerical solution of PDE such as the Navier-Stokes equations. 

#### Domain Decomposition methods:
- Overlapping 
- Non overlapping

## DDP for Optimal Control Constrained with PDE

Here are the step-by-step instructions on how to use DDP for Optimal Control Constrained with PDE:

- Discretize the Navier-Stokes equations using a finite element method. This should result in a large system of linear equations.

- Set up the optimal control problem by defining the objective function and the constraints.

- Use a Lagrange multiplier approach to express the optimal control problem as a saddle-point problem.

- Apply the DDP method by decomposing the computational domain into subdomains, each of which is solved separately using a suitable preconditioner.

- Choose a suitable preconditioner for each subdomain.
 -- The preconditioner should be chosen such that it effectively reduces the condition number of the matrix associated with the subdomain problem.
* Here we use overlapping Schwarz-type preconditioner.

- Solve the subdomain problems using an iterative solver such as GMRES.

- Combine the solutions from the subdomain problems to obtain the solution of the original problem.

- Check the convergence of the iterative solver and adjust the preconditioners if necessary.

- Finally, use the computed solution to evaluate the objective function and check whether the constraints are satisfied.

## Recommandation 
It is important to note that the effectiveness of DDP depends on the choice of subdomain decomposition and preconditioners. 
A good choice can result in significant speedup and reduced memory requirements, while a poor choice can lead to slow convergence and increased computational cost. Therefore, it is crucial to test different decomposition strategies and preconditioners to find the best one for your specific problem.
