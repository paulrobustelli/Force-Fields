# Force-Fields
Thank your interest in the TIP4P-D, a99SB-disp, DES-amber, and DES-amberSF1.0 force fields.

#######Please Cite: ###########

Water dispersion interactions strongly influence simulated structural properties of disordered protein states
S Piana, AG Donchev, P Robustelli, DE Shaw
The journal of physical chemistry B 119 (16), 5113-5123

Developing a molecular dynamics force field for both folded and disordered protein states
P Robustelli, S Piana, DE Shaw
Proceedings of the National Academy of Sciences 115 (21), E4758-E4766

Piana, S., Robustelli, P., Tan, D., Chen, S. and Shaw, D.E., 2020. Development of a force field for the simulation of single-chain proteins and protein–protein complexes. Journal of chemical theory and computation, 16(4), pp.2494-2507.

###############################

#### Experimental Data For Force Field Validation ####

Experimental data used to validate the a99SB-disp force field described in (Robustelli et al, PNAS, 2018) is available for download:

https://www.dropbox.com/s/vl6yrpl0el5uabc/a99SBdisp_PNAS_2018.experimental_data.tar?dl=0


##############################


a99SB-disp is intended for use with the a99SBdisp water model and c22 ions.

DES-amber and DES-amberSF1.10 parameres are intended for use with the TIP4P-D water model, and contain their own ion parameters

The Gromacs versions were adopted from DESMOND viparr parameters.

Please note that all published simulations were performed using a DESMOND version of the force-fields.   

GROMACS versions were created for the convenience of external researchers.  

Basic tests have indicated that the GROMACS versions should provide accurate parameters that correctly reproduce the DESMOND force-field, but we cannot cannot guarantee that they are free from any bug.  

To ensure accuracy for your system, you should compare FF energies to energies obtained from DESMOND using official viparr-ff releease.

##############################

######  a99SB-disp Notes #####
The gromacs implementation of a99SBdisp.ff contians parameters for c22ions and a99SBdisp water

These parameters can be compared against

Robutselli_Lab_ForceFields/Desmond/a99SBdisp_viparr-ff/

aa.amber.ff99SB-disp  ions.charmm22  water.tip4pd-1.6

These a99SBdisp parameters were taken from the public viparr-ff repository  
https://github.com/DEShawResearch/viparr-ffpublic

##### DES-amber Notes   ######
The gromacs implementations of des-amber.ff and des-amber-SF1.0.ff contain their own ion parameters and TIP4P-D water parameters and can be compared to:

Robustelli_Lab_ForceFields/Desmond/

des-amber  des-amber-SF1.0  water.tip4pd

These viparr implementations are *not* official D.E. Shaw Research releases, and should be considered personal implementations.  D.E. Shaw Research should be contacted about official DES-amber viparr force field releases.

##### Note on DES-amber Charge Scaling ######

DES-amber has charges and charged ions that are scaled by a factor of 0.9       

This means if you are combining this force fields with lipids, ligands, or nucleic acids
with net charges, the total charge of the system will not be neutral  

You can either scale the charges of the other molecules (not recommended )
or use DES-amber_SF1.0 (scale factor 1.0) which does not contain scaled charges        

