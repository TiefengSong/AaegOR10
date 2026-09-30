# From Ligand Binding to Pore Opening in the Mosquito Odorant Receptor AaegOR10

This repository contains the analysis workflows and supporting data for the study **“From Ligand Binding to Pore Opening in the Mosquito Odorant Receptor AaegOR10.”**

## Contents

### `features/`
- `filter_features.ipynb`: Compare open and closed structures and identify significant distance/dihedral changes.
- `feature2plumed.ipynb`: Convert selected structural changes into PLUMED collective variables.
- `cal_distribution.ipynb`: Calculate and compare reweighted CV distributions and free-energy profiles.

### `MSM/`
- `build_msm_apo.ipynb`: Build and analyze the apo tICA/MSM model.
- `build_msm_holo.ipynb`: Build and analyze the holo/bound tICA/MSM model.
- `macrostate.ipynb`: Analyze macrostate free-energy landscapes and structural coordinates.
- `plumed_from_2trajs.dat`: PLUMED definitions for calculating trajectory collective variables.
- `apo_md.tpr`, `holo_md.tpr`: GROMACS system/run input files for the MSM trajectories.

The MSM notebooks include microstate clustering, PCCA macrostates, implied timescales, CK tests, MFPT, reactive flux, and free-energy analysis.

### `PCCA_COLVAR/`
Contains reweighted COLVAR files generated for individual PCCA macrostates and representative pathways. Each subdirectory contains `closed`, `intermediate`, `open`, `super_open`, and off-pathway states.

- `Helix/`: AlphaRMSD coordinates.
- `Dporelowest/`: Lowest pore diameter(`d1.lowest`).
- `Dis_293294_356/`: Distances involving residues 293, 294, and 356.
- `Dis_S3-S6/`: S3–S6 distance and membrane/lipid-related coordinates.

These files can be used to reproduce macrostate-specific distributions and free-energy plots.

### `unbiased/`
- `unbiased_analysis.ipynb`: Analyze unbiased trajectories, contacts, tICA projections, RMSD, ligand/lipid distances, and mutation-related comparisons.
- `apo_closed.tpr`, `apo_open.tpr`, `holo_closed.tpr`, `holo_open.tpr`: GROMACS system/run input files for the four unbiased systems.
