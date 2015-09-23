# RandomQuantum

This package provides functions to sample from various random matrix ensebles
associated with quantum information applications.

Here is a table of currently support ensembles:

Type    | Ensemble
--------|----------
`GinibreEnsemble` | Ginibre unitarily invariant matrix ensemble
`FubiniStudyPureState` | Fubini-Study pure ensemble
`FubiniStudyMixedState` | Mixed-state ensemble induced by tracing out elements of Fubini-Study ensenble on a larger space
`HilbertSchmidtMixedState` | Mixed-state ensemble given by the "flat" Hilbert-Schmidt 
`BuresMixedState` | Mixed-state ensemble given by the Bures metric.
`ClosedHaarEnsemble` | Circular Unitary Ensemble (CUE), unitaries distributed according to the Haar measure.
`OpenHaarEnsemble` | Quantum channel ensemble induced by Haar-distributed unitaries (CUE) on a larger space.
`RandomClosedEvolution` | Unitary matrix ensemble obtained by evolving under a Hamiltonian sampled from a Gaussian unitary ensemble
`RandomOpenEvolution` | Quantum channel ensemble induced by integrated GUE evolution on a larger space.

The interface is emulates the interface of `Distributions.jl`,
although there is a lot missing at the moment.

# Examples

```julia
julia> using RandomQuantum

julia> rand(BuresMixedState(2))
2x2 Array{Complex{Float64},2}:
   0.771511+0.0im       -0.0632581+0.116198im
 -0.0632581-0.116198im    0.228489+0.0im    
```

# References

Francesco Mezzadri, **How to Generate Random Matrices from the
Classical Compact Groups** [Notices Amer Math Soc 54 4 592
(2007)](http://www.ams.org/notices/200705/fea-mezzadri-web.pdf)
[arXiv:math-ph/0609050](http://arxiv.org/abs/math-ph/0609050)

Wojciech Bruzda, Valerio Cappellini, Hans-Jürgen Sommers, Karol
Życzkowski, **Random quantum operations**, [Physics Letters A, Volume 373,
Issue 3, 12 January 2009, Pages
320-324](http://www.sciencedirect.com/science/article/pii/S0375960108016885)
[arXiv:0804.2361](http://arxiv.org/abs/0804.2361)

Karol Życzkowski, Karol A. Penson, Ion Nechita, and Benoît Collins,
**Generating random density matrices**, [Journal of Mathematical
Physics, 52, 062201 (2011)](http://dx.doi.org/10.1063/1.3595693)
[arXiv:1010.3570](http://arxiv.org/abs/1010.3570)

# License

MIT License

# Copyright

(c) Raytheon BBN Technologies, 2015

# Contributors

Marcus P S (@marcusps)