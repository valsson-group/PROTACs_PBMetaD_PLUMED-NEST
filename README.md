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
  - This file should be located in the same folder as the MD files. 
- The last bias reweighting post-processing was run using the `plumed driver` using the following PLUMED input files in the `Reweighting-Example/LastBiasReweighting_8microsec/` folder: 
  - `plumed_lastbias.dat`: Reads in the deposited Gaussians and calculates the biasing weights for each configuration. 
  - `plumed_read.dat`: used to read from the colvar files the relevant CVs for the reweighting.
  - These input files will read in the colvar files from the parent folder (`../`)and create new colvar files with the appropriate biasing weights that can be used to obtain reweighted free energy surfaces and densities. These files should be located in a sub-folder of the runs. 

## License
Copyright (c) 2025 Shikshya Bhusal and Omar Valsson

Creative Commons Attribution 4.0 International Public License (CC BY 4.0). See `LICENSE` for more details.
