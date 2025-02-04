# Input files for "Characterizing the conformational ensemble of PROTAC degraders in solutions via atomistic simulations"

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
Group Website : www.valsson.info

## Software
Files were run with the following codes:
- GROMACS 2022.5 MD code
- PLUMED 2.8.2 enhanced sampling plug-in code 
- VMD 1.9.3 for trajectory analysis

##File Overview:

- All the .gro, .itp and .top files for each solvent (Water, Chloroform, and DMSO) are located in their respective folders.
- The molecular dynamics parameters can be found in the md-npt.mdp file.
- The collective variables (CVs) are clearly listed in the plumed_pbmetad.dat file.
- For DMSO and chloroform, we did not use gmx tune_pme tool for the simulation. gmx tune_pme tool is disabled by setting -tunepme no in the simulation command.
- plumed_pbmetad.dat file defines all the collective variables illustrated in the paper for parallel bias metadynamics.
- plumed_lastbias.dat file is used for the reweighting to remove the effect of bias.
- plumed_read.dat file includes the arrangement of collective variables in specific folder.

## License
Copyright (c) 2025 Shikshya Bhusal and Omar Valsson

Creative Commons Attribution 4.0 International Public License (CC BY 4.0). See `LICENSE` for more details.
