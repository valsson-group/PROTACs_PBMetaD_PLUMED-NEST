# Input files for "Characterizing the conformational ensemble of PROTAC degraders in solutions via atomistic simulations"

Supporting Information for:
- S. Bhusal and O. Valsson    
*Characterizing the conformational ensemble of PROTAC degraders in solutions via atomistic simulations*    
ChemRxiv Preprint, submitted to Phys. Chem. Chem. Phys. (2025)    
ChemRxiv: [10.26434/chemrxiv-2025-bxf47](https://doi.org/10.26434/chemrxiv-2025-bxf47)

This archive contains input files used to generate the data.

## Authors
Shikshya Bhusal - shikshyabhusal@my.unt.edu   
*Department of Chemistry*    
*University of North Texas*    
*Denton, Texas, USA*     
ORCID: [0000-0001-5668-645X](https://orcid.org/0000-0001-5668-645X)

Omar Valsson - omar.valsson@unt.edu    
*Department of Chemistry*     
*University of North Texas*    
*Denton, Texas, USA*    
ORCID: [0000-0001-7971-4767](https://orcid.org/0000-0001-7971-4767)     
Website: www.valsson.info

## Software
Files were run with the following codes:
- GROMACS 2022.5 MD code
- PLUMED 2.8.2 enhanced sampling plug-in code 
- VMD 1.9.3 for trajectory analysis

## File Overview:

- All the .gro, .itp and .top files for each solvent are located in their respective folders under `Input_Files`
  - Water: `Input_Files/Water`
  - Chloroform: `Input_Files/Chloroform`
  - DMSO: `Input_Files/DMSO`
- The GROMACS molecular dynamics parameters can be found in the `md-npt.mdp` file.
- The DMSO and chloroform simulations were run with the `-tunepme no` flag to disable the PME parameter tuning at run time. 
- The Parallel Bias Metadynamics simulations are run using the following PLUMED input files:
  - `plumed_pbmetad.dat`: include all CVs defined in the simulations and the PBMetaD bias.
- The last bias reweighting post-processing was run using the `plumed driver` using the following PLUMED input files: 
  - `plumed_lastbias.dat`
  - `plumed_read.dat`: used to read from files the relevant CVs for the reweighting

## License
Copyright (c) 2025 Shikshya Bhusal and Omar Valsson

Creative Commons Attribution 4.0 International Public License (CC BY 4.0). See `LICENSE` for more details.
