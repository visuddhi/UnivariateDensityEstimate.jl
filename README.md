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


