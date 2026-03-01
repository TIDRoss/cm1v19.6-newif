# cm1v19.6-newif

## Overview
This repository provides a small set of CM1 v19.6 source-file modifications used in experiments involving an IF-INP (“NewIF”) immersion-freezing routine and Carpenter-style convective forcing. All other CM1 source files are assumed to be identical to the official CM1 v19.6 distribution.

The intent is:
- **`src/`**: general implementation (code changes)
- **`papers/`**: paper-specific runtime inputs (namelists + forcing files) and brief run notes

## Repository layout
- `src/`
  - CM1 source files that differ from the vanilla CM1 v19.6 release (copy these into a CM1 source tree and rebuild).
  - Includes `base.F` (sounding/wind options, including paper-used constants) and `init3d.F` (Carpenter forcing; reads `carp_force`).
- `papers/`
  - Paper-specific run packages and documentation.
  - Each storm folder is designed to contain only what is needed to run that case once CM1 is built (typically `namelist.input` + `carp_force`).

## How to use (minimal)
1. Start from a clean CM1 v19.6 source tree.
2. Copy the contents of `src/` into the CM1 source directory (overwriting the corresponding files).
3. Build CM1 (note: any provided Makefile may be cluster-specific).
4. Choose a run package in `papers/<paper_id>/<storm>/` and copy into a run directory:
   - `namelist.input` → `./namelist.input`
   - `carp_force` → `./carp_force`
5. Run CM1.

## Notes on reproducibility / releases
This repo is designed to be cited via **GitHub Releases** (and, if connected, archived by Zenodo).
For a specific paper, cite the **release/tag (or commit hash)** used for that paper’s simulations.

## Citation
If you use these modifications, please cite the relevant paper and the corresponding archived release of this repository.

- Ross, T., & Lasher-Trapp, S. (2025): *Investigating the Relative Roles of INPs and CCN in a Simulated Thunderstorm Using a New Immersion Freezing Algorithm*. Journal of Geophysical Research: Atmospheres. (Add DOI here if desired.)
- Ross, T., & Lasher-Trapp, S. (2026): submitted to  Journal of Geophysical Research: Atmospheres.
## What is modified?
The modified files live in `src/`. In broad terms these changes:
- implement a temperature-dependent IF-INP immersion-freezing routine in the NSSL 2-moment microphysics, and/or
- enable Carpenter-style forcing initialization and associated outputs used in the experiments.

(For NewIF parameters, search within the microphysics file for: `!<IFINP_USER_SETTINGS>`.)




