# ECCOv5-Configurations

**Content:**

This repository contains documentation (doc/) and model configuration files (code/, namelist/) for official releases of the ECCO Version 5 ocean and sea-ice state estimates.  Model configuration files allow users to reproduce the state estimate or  conduct new simulation experiments. 

## ECCO Version 5

ECCO Version 5 increases the horizontal resolution and employs a new optimization methodology compared to its predecessors. It moves from the 1-degree latitude-longitude-cap (LLC) 90 grid used in Version 4 to a nominal 1/3-degree horizontal resolution (llc270). Most notably, this version introduces the first multigrid optimization approach for ECCO: the forward model runs on the high-resolution llc270 grid, while control parameters are optimized on the lower-resolution llc90 grid for computational efficiency.

### Latest: Release 1: 1992-2025

ECCO Version 5 Relase 1 starts from an earlier ECCO Version 5 Alpha solution (1992–2017) and utilizes seasonal cycle-adjusted MERRA-2 atmospheric forcing for the 2018–2025 period. The optimization strategy was two-phased:
Initial Optimization (2018–2024): Focused on rapidly improving less well optimized control variables during the post-Alpha period
Full-Period Optimization (1992–2024): A full optimization covering the long-duration record prior to the 2025 extension

The final solution is further extended through 2025 in a simulation mode using seasonal cycle-adjusted MERRA-2 forcing. This release leverages the high-resolution llc270 grid to provide more detailed ocean state estimates while maintaining the physical consistency and closed-budget requirements of previous versions.

Technical outputs include monthly mean model state variables, atmospheric state variables and fluxes at the ocean surface, and three-dimensional budget terms for heat, salt, and momentum, optimized to bridge the gap between the V5 Alpha period and more recent satellite and in situ observations.

## Other Directories

### devel: 

The devel directory contains ECCO configurations that are in development and other useful code that is not checked into the main MITgcm repository. 

## Support

For support questions about ECCO please contact ecco-support@mit.edu.
For support questions about MITgcm please contact  mitgcm-support@mit.edu.

We also encourage you to create a new 'ISSUE' here in the "ECCO-v5-Configurations" github repository to report a problem: https://github.com/ECCO-GROUP/ECCO-v5-Configurations/issue 

Your feedback is key to helping us improve! 

## References

**References:**

ECCO Consortium, I. Fukumori, O. Wang, I. Fenty, G. Forget, P. Heimbach, and R. M. Ponte, 2020: Synopsis of the ECCO Central Production Global Ocean and Sea-Ice State Estimate (Version 4 Release 4). doi:10.5281/ZENODO.3765929.

Forget, G., J.-M. Campin, P. Heimbach, C. N. Hill, R. M. Ponte, and C. Wunsch, 2015: ECCO version 4: an integrated framework for non-linear inverse modeling and global ocean state estimation. Geoscientific Model Development, 8, 3071-3104, <http://dx.doi.org/10.5194/gmd-8-3071-2015>, <http://www.geosci-model-dev.net/8/3071/2015/>

Forget, G., J.-M. Campin, P. Heimbach, C. N. Hill, R. M. Ponte, and C. Wunsch, 2016: ECCO Version 4: Second Release, <http://hdl.handle.net/1721.1/102062>, [direct download](https://dspace.mit.edu/bitstream/handle/1721.1/102062/standardAnalysis.pdf?sequence=1&isAllowed=y)

Fukumori, Ichiro; Wang, Ou; Fenty, Ian; Forget, Gael; Heimbach, Patrick; Ponte, Rui M., 2017. ECCO Version 4 Release 3, 10, 1721.1/110380.
