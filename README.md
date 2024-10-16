Codes used to compile CM1v19.6 that were modified from the original model source code and initialize model experiments in Ross and Lasher-Trapp (in submission). All other model source files were unedited. 

module_mp_nssl_2mom_cpbudg2_NewIF_prcsrates.F is the NSSL microphysics scheme with the new immersion freezing algorithm (NewIF) embedded. 

init3d.F includes code for the guassian plume used to initiate convection (Carpenter et al. 1998)  

All other files are to compile and initialize the model with NewIF and output microphysical process rate terms. 



