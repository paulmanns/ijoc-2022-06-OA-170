# ijoc-2022-06-OA-170

This repository contains setup and results data for the computational experiments in the article _Efficient Solution of Discrete Subproblems Arising in Integer Optimal Control with Total Variation Regularization_ by Marvin Severitt and Paul Manns. The data for the benchmark problems _SH_ and _SR_ from said article can be found in the respectively named subdirectories. The data is structured as follows.

## Subdirectory _SH_

For each of the algorithms _top_, _astar_, and the three data subsets generated with _scip_, _scip\_random_ and _scip\_highest_ analyzed the article, the file results\_ALGORITHM.csv contains the information of one instance (= subproblem solve) in each row. The columns of each row provide the following information:

* ID of the instance,
* initialization of SLIP (_1_, _2_, or  _3_),
* the regularization parameter &alpha;,
* the number of (control) discretization intervals N,
* the trust-region radius &Delta;, and
* the time the algorithm required to solve the instance to optimality.

For the runs of the overall algorithms _SLIP_, _BFGS_ (+ roundings), and their hybridizations, the running times are reported in the file
results\_slip\_times.csv and the objective values are reported in the file results\_slip\_objective\_values.csv. Each row corresponds to one run and the columns
contain the following information:

* the number of (control) discretization intervals N,
* the regularization parameter &alpha;,
* the resulting value (running time or objective) for _SLIP_ initialized with initialization _1_,
* the resulting value (running time or objective) for _SLIP_ initialized with initialization _2_,
* the resulting value (running time or objective) for _SLIP_ initialized with initialization _3_,
* the resulting value (running time or objective) for _SLIP_ initialized with the result of _BFGS_ followed by an execution of _SUR_,
* the resulting value (running time or objective) for _SUR_,
* the resulting value (running time or objective) for _BFGS_.

## Subdirectory _SR_

For each of the 10 sampled kernels, the 200 sampled values _b\_1,...,b\_200_ are provided in the file b\_KERNEL.csv, the 200 sampled values _&mu;\_1,...,&mu;\_200_ are provided in the file mu\_KERNEL.csv, and the 200 sampled values _&sigma;\_1,...,&sigma;\_200_ are provided in the file sigma\_KERNEL.csv. 

For each of the algorithms _top_, _astar_, and the three data subsets generated with _scip_, _scip\_random_ and _scip\_highest_, the file results\_ALGORITHM.csv contains the information of one instance (= subproblem solve) in each row. The columns of each row provide the following information:

* ID of the instance,
* the ID of the used kernel (in 1,...,10),
* the regularization parameter &alpha;,
* the number of (control) discretization intervals N,
* the trust-region radius &Delta;, and
* the time the algorithm required to solve the instance to optimality.

For the runs of the overall algorithms _SLIP_, _BFGS_ (+ roundings), and their hybridizations, the running times are reported in the file
results\_slip\_times.csv and the objective values are reported in the file results\_slip\_objective\_values.csv. Each row corresponds to one run and the columns
contain the following information:


* the number of (control) discretization intervals N,
* the regularization parameter &alpha;,
* the ID of the used kernel (in 1,...,10),
* the resulting value (running time or objective) for _SLIP_ initialized with the zero vector,
* the resulting value (running time or objective) for _SLIP_ initialized with the result of _BFGS_ followed by nearest integer rounding,
* the resulting value (running time or objective) for _SLIP_ initialized with the result of _BFGS_ followed by an execution of _SCARP_,
* the resulting value (running time or objective) for _SLIP_ initialized with the result of _BFGS_ followed by an execution of _SUR_,
* the resulting value (running time or objective) for _SCARP_,
* the resulting value (running time or objective) for _SUR_,
* the resulting value (running time or objective) for _BFGS_.
