# ijoc-2022-06-OA-170

This repository contains setup and results data for the computational experiments in the article _Efficient Solution of Discrete Subproblems Arising in Integer Optimal Control with Total Variation Regularization_ by Marvin Severitt and Paul Manns. A brief description of the data is given below.

## Subdirectory _SH_

For each of the algorithms _top_, _astar_, and _scip_ from the article, the file results_ALGORITHM_2.csv contains the information of one instance (= subproblem solve) in each row. The columns of each row provide the following information:

* the regularization parameter &alpha;,
* the number of (control) discretization intervals N,
* the trust-region radius &Delta;, and
* the time the algorithm required to solve the instance to optimality.

## Subdirectory _SR_

