# UnivariateDensityEstimate.jl

Package for univariate density estimation with combinatorial constraints, based on Bernstein polynomials. 

<h2> Installing the package </h2>

Run the following code to install the package.


```julia
import Pkg
Pkg.clone("https://github.com/visuddhi/UnivariateDensityEstimate.jl")
```

<h2> The mirror-descent (MD) algorithm </h2>

It is recommended to use `BernsteinEstimate_MD(Y,m,a,b,k,e,T,MaxIter,obj,flag,Reg)` when combinatorial constraints are not imposed.

* Y: data
* m: number of Bernstein basis
* [a,b]: range of the estimator
* k: number of modes (only k=0,1 is supported for <code> BernsteinEstimate_MD </code>, k=0 means vanilla density estimation, k=1 means unimodal density estimation)
* e: tolerance of error, 1e-4 by default
* T: maximum computational time (in sceonds), 10e10 by default
* MaxIter: maximum number of iterations
* obj: "Log" or "Quad", "Log" -> maximum log likelihood estimator; "Quad" -> Anderson-Darling estimator
* flag: "Acc" or "NonAcc", only application for k=0, "Acc" -> accelerated mirror descent, "NonAcc" -> nonaccelerated mirror descent
* Reg: coefficient of the L2 regularizer

<h2> The mixed-integer-qudratic-optimization (MIQO) algorithm </h2>

It is recommended to use `BernsteinEstimate_MIQO(Y,m,a,b,k,e,T)` when there are combinatorial constraints.

* Y: data
* m: number of Bernstein basis
* [a,b]: range of the estimator
* k: number of modes, k can be arbitrary positive integer
* e: MIP gap
* T: maximum computational time (in sceonds)

<h2> An example </h2>


