# MODFLOW-NWT

[![mfnwt checks](https://github.com/MODFLOW-ORG/mfnwt/actions/workflows/ci.yml/badge.svg)](https://github.com/MODFLOW-ORG/mfnwt/actions/workflows/ci.yml)

## Overview of MODFLOW-NWT

The USGS MODFLOW-NWT is a Newton-Raphson formulation for MODFLOW-2005 to improve solution of unconfined groundwater-flow problems. MODFLOW-NWT is a standalone program that is intended for solving problems involving drying and rewetting nonlinearities of the unconfined groundwater-flow equation.

MODFLOW-NWT must be used with the Upstream-Weighting (UPW) Package for calculating intercell conductances in a different manner than is done in the Block-Centered Flow (BCF), Layer Property Flow (LPF), or Hydrogeologic-Unit Flow (HUF) Packages. Flow-property input for the UPW Package is designed based on the LPF Package and material-property input is identical to that for the LPF Package except that the rewetting and vertical-conductance correction options of the LPF Package are not available with the UPW Package. Input files constructed for the LPF Package can be used with slight modification as input for the UPW Package.

The NWT linearization approach generates an asymmetric matrix, which is different from the standard MODFLOW formulation that generates a symmetric matrix. Because all linear solvers presently available for use with MODFLOW-2005 solve only symmetric matrices, MODFLOW-NWT includes two previously developed asymmetric matrix-solver options. The matrix-solver options include a generalized-minimum-residual (GMRES) Solver and an Orthomin / stabilized conjugate-gradient (CGSTAB) Solver.

MODFLOW-NWT is described in the documentation report by Niswonger and others (2011). The Surface-Water Routing (SWR1) and Seawater Intrusion (SWI2) Packages, which are included with MODFLOW-NWT are documented in Hughes and others (2012) and Bakker and others (2013), respectively.

## How to Cite MODFLOW-NWT

### Report Citation

Niswonger, R.G., Panday, Sorab, and Ibaraki, Motomu, 2011, MODFLOW-NWT, A Newton formulation for MODFLOW-2005: U.S. Geological Survey Techniques and Methods 6-A37, 44 p., https://doi.org/10.3133/tm6A37
