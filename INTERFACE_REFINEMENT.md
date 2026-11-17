# Interface-only refinement

The numerical demonstration selects the fine-grid region using `0.2 < φ < 0.8` on the evolving phase field, with a four-coarse-cell buffer and periodic wrapping. Fine spacing and time step are half the coarse values. The liquid core is not part of the tagged interface and remains coarse unless included by the buffer. The original underlying solver formulation is not disclosed here.

## Data provenance

All field plots and histories in this public repository come from a fresh 400-coarse-step interface-only run at finest time 800. The earlier liquid-region-refined long-run statistics are not used as evidence for this changed refinement criterion.

The phase-volume error and uniform-grid comparison are numerical diagnostics, not a claim that coarse–fine momentum flux is exactly conservative.
