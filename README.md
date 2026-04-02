# cm1v19.6-newif

## Overview

This repository contains modifications to CM1 v19.6 used in Ross and Lasher-Trapp (2025) and subsequent studies. These modifications include changes to the NSSL 2-moment microphysics scheme associated with the NewIF immersion-freezing routine, as well as Carpenter-style convective forcing used in the experiments. Files not included here are assumed to be unchanged from the official CM1 v19.6 distribution.

## Repository layout

- `src/`: CM1 source files modified relative to the official CM1 v19.6 release
- `papers/`: paper-specific run inputs and notes

## How to use

1. Start from a clean CM1 v19.6 source tree.
2. Copy the files in `src/` into the CM1 source directory, overwriting the corresponding originals.
3. Build CM1.
4. Copy the desired files from `papers/<paper_id>/<storm>/` into your run directory.
5. Run CM1.

## Citation and versioning

If you use these modifications, please cite the relevant paper describing the model development as well as the archived release of this repository corresponding to the version used in your study.

- Ross, T., & Lasher-Trapp, S. (2025). *Investigating the Relative Roles of INPs and CCN in a Simulated Thunderstorm Using a New Immersion Freezing Algorithm*. *Journal of Geophysical Research: Atmospheres*.
- Ross, T., & Lasher-Trapp, S. (2026). *[current manuscript title]*. *Journal of Geophysical Research: Atmospheres*, submitted.

For reproducibility, please cite the specific release, tag, or archived version used for a given study.

## What is modified?

The modified files are located in `src/`. Broadly, these changes:

- implement a temperature-dependent IF-INP immersion-freezing routine in the NSSL 2-moment microphysics scheme
- enable Carpenter-style forcing initialization and associated outputs used in the experiments

For NewIF parameters, search within the microphysics file for `!<IFINP_USER_SETTINGS>`.




