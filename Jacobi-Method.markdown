The Jacobi method is easily derived by examining each of the $n$ equations in the linear system $Ax=b$ in isolation. If in the $i$-th equation
$$
\sum_{j=1}^n{a_{i,j}x_j}=b_i
$$

we solve for the value of $x_i$ while assuming the other entries of $x$ remain fixed, we obtain
$$
x_i=(b_i-sum_{j\neq i}{a_{i,j}x_j}/a_{i,i})
$$

This suggests an iterative method defined by
$$
x^k_i=(b_i-sum_{j\neq i}{a_{i,j}x^{k-1}_j}/a_{i,i})
$$
which is the **Jacobi method**. Note that the order in which the equations are examined is irrelevant, since the Jacobi method treats them independently. For this reason, the Jacobi method is also known as the *method of simultaneous displacements*, since the updates could in principle be done simultaneously.

Simultaneous displacements, method of: Jacobi method.

In matrix terms, the definition of the Jacobi method in (gif) can be expressed as
$$
x^k=D^{-1}(L+U)x^{k-1}+D^{-1}b
$$
where the matrices $D, -L$  and $-U$ represent the diagonal, the strictly lower-triangular, and the strictly upper-triangular parts of $A$, respectively.

The pseudocode for the Jacobi method is given in Figure . Note that an auxiliary storage vector,  is used in the algorithm. It is not possible to update the vector  in place, since values from  are needed throughout the computation of .
