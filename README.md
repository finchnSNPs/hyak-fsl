# UW HYAK FSL container

FMRIB Software Library container recipe and SLURM job submission script examples. 

Created at the request of UW HYAK users in March 2024. 

### About FMRIB Software Library (FSL)

 [FSL Wiki](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FSL)

 ### Versions

 OS - Centos 7 
 
 fslinstaller.py version number 3.2.0 - The version in this repo contains one change to fix a ca.certificates error. 

 Installs FSL version 6.0.6 .

 Includes the [fsl-sub-plugin-slurm](https://git.fmrib.ox.ac.uk/fsl/fsl_sub_plugin_slurm) for integration with SLURM. 

 ### Apptainer recipe file

The apptainer recipe file (fsl-centos7.def) was from a template originally created by Tashrif Billah found in this [repo](https://github.com/pnlbwh/fsl-containers/tree/master) and the file named [Singularity.centos7](https://github.com/pnlbwh/fsl-containers/blob/master/Singularity.centos7).

### SLURM script

