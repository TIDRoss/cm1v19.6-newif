Overview

This repository contains the codes used to compile CM1v19.6 with specific modifications made for the experiments presented in Ross and Lasher-Trapp (in submission).
All other CM1 source files remain unmodified from the original release.
Modified Files

    module_mp_nssl_2mom_cpbudg2_NewIF_prcsrates.F
    Modified version of the NSSL double-moment microphysics scheme, incorporating the New Immersion Freezing (NewIF) algorithm for improved representation of drop freezing.

    init3d.F
    Modified to include code for initializing convection using a Gaussian plume, following the method of Carpenter et al. (1998).

Purpose

The modifications allow CM1 to:

    Embed a new temperature-dependent immersion freezing parameterization within the NSSL microphysics scheme.

    Initialize deep convection using a Gaussian plume.

    Output microphysical process rate terms for detailed budget analyses.

All other model source files are identical to the official CM1v19.6 distribution.
Citation

If you use these modifications or find them helpful, please cite:

    Ross, T. and Lasher-Trapp, S. (in submission): Investigating the Relative Roles of INPs and CCN in a Simulated Thunderstorm Using a New Immersion Freezing Algorithm. [JGR Atmospheres].




