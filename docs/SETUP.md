# Numerical setup (public summary)

This note describes the benchmark at an application-level overview; it does not document the unpublished fluid solver or refinement implementation.

| Configuration | Value |
|---|---|
| Governing numerical framework | Simplified Multiphase Lattice Boltzmann Method |
| Fine-equivalent domain | 200 × 200 |
| Coarse level | 100 × 100 |
| Hierarchy | Two levels; 2:1 balanced |
| Fine grid spacing | Δx = Δy = 1 lattice unit |
| Coarse grid spacing | Δx = Δy = 2 lattice units |
| Fine time step | Δt = 1 lattice time unit |
| Coarse time step | Δt = 2 lattice time units |
| Applied acceleration | x direction, 8 × 10⁻⁶ in fine-lattice units |
| Initial droplet radius | 30 lattice units |
| Initial centre | (190, 100) |
| Domain boundary conditions | Periodic x and y |
| Refinement tracking | Liquid/interface region, updated every 5 coarse steps |
| Hierarchy buffer | 4 coarse cells |
| 5,000-time-unit test | 2,500 coarse steps, 437 nontrivial refinement updates |

## Numerical reporting conventions

- All lengths, times, and velocities are reported in **lattice units**; no physical dimensional calibration is claimed.
- Wrapped centroids are displayed modulo the domain width; unwrapped centroids track accumulated motion.
- Reported mass conservation concerns the simulated phase-volume integral; it does not establish exact global momentum-flux conservation.
- ``active composite cells`` counts the owned active cells on both mesh levels. The numerical prototype still computes arrays on both levels, so the active-cell savings are not wall-clock savings.
- The detailed numerical formulation is not part of the public research portfolio.
