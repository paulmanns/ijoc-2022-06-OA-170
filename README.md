# ijoc-2022-06-OA-170

This repository contains setup and results data for the computational experiments in the article _Efficient Solution of Discrete Subproblems Arising in Integer Optimal Control with Total Variation Regularization_ by Marvin Severitt and Paul Manns. The data for the benchmark problems _SH_ and _SR_ from said article can be found in the respectively named subdirectories. The data is structured as follows.

## Subdirectory _SH_

For each of the algorithms _top_, _astar_, and _scip_ and the initializations _1_, _2_, and _3_ analyzed the article, the file results_ALGORITHM_INITIALIZATION.csv contains the information of one instance (= subproblem solve) in each row. The columns of each row provide the following information:

* the regularization parameter &alpha;,
* the number of (control) discretization intervals N,
* the trust-region radius &Delta;, and
* the time the algorithm required to solve the instance to optimality.

## Subdirectory _SR_

For each of the 10 sampled kernels, the 200 sampled values _b\_1,...,b\_200_ are provided in the file b_KERNEL.csv, the 200 sampled values _&mu;\_1,...,&mu;\_200_ are provided in the file mu_KERNEL.csv, and the 200 sampled values _&sigma;\_1,...,&sigma;\_200_ are provided in the file sigma_KERNEL.csv. 
