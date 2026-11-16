# Validation and provenance

Two datasets are referenced in this repository.

## A. Archived fields and time series: t = 2,000

The phase fields, mesh mask, reference phase field, and time history were available from the completed periodic-crossing calculation. Figures 01–04 use these results.

End-of-run diagnostics:

| Quantity | Value |
|---|---:|
| Fine-grid time | 2,000 |
| Unwrapped centroid | 205.928332 |
| Wrapped centroid | 5.928332 |
| Maximum lattice speed | 0.0159551 |
| Relative volume error | −1.1239 × 10⁻¹³ |
| Refinement updates | 137 |
| Mean absolute phase-field difference vs uniform | 7.589 × 10⁻⁶ |
| Momentum residual divided by forcing impulse | 0.1812% |

The summarized, non-sensitive time history is included as `data/validation_history_t2000.csv`; dense simulation fields are deliberately excluded.

## B. Extended run: t = 5,000

Values come from the completed Spyder/IPython console output supplied by the simulation author. The final field arrays for that longer run were not supplied. Figure 05 and `data/long_run_summary.json` therefore report **only the logged aggregate metrics**, not fabricated t=5,000 contours.

| Quantity | Value |
|---|---:|
| Fine-grid time | 5,000 |
| Unwrapped centroid | 289.568947 |
| Wrapped centroid | 89.568947 |
| Maximum lattice speed | 0.0399026 |
| Relative volume error | −2.7883 × 10⁻¹³ |
| Refinement updates | 437 |
| Mean absolute phase-field difference vs uniform | 5.2787 × 10⁻⁵ |
| Momentum-budget discrepancy | 0.3006% |

## Interpretation and limits

- The periodic boundary crossing and dynamic refinement are demonstrated.
- Reported relative phase-volume errors are very small, and the uniform-grid phase-field discrepancy remains small in the tested interval.
- A 0.3006% momentum-budget discrepancy persists at t=5,000; additional conservative interlevel hydrodynamic validation remains open.
- Active-cell reduction is not equal to compute-time acceleration for the current validation prototype.

No source code, internal solver notes, or unpublished derivations are part of the public artifact.
