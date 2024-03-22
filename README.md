# UW HYAK FSL container

FMRIB Software Library container recipe and SLURM job submission script examples. 

Created at the request of UW HYAK users in March 2024. 

### About FMRIB Software Library (FSL)

 [FSL Wiki](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FSL)

 ### Versions

 OS = Centos7 
 
 `fslinstaller.py` version number 3.2.0 - The version in this repo contains one change to fix a ca.certificates error. There are lines in the apptainer recipe file to download `fslinstaller.py` from the [FSL Wiki](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FSL). Un-comment lines to use that install, and `#comment lines to install from this GitHub repo.` 

 Installs `FSL` version 6.0.6 .

 Includes the [fsl-sub-plugin-slurm](https://git.fmrib.ox.ac.uk/fsl/fsl_sub_plugin_slurm) for integration with `SLURM`. 

 ### Apptainer recipe file

The apptainer recipe file `fsl-centos7.def` was from a template originally created by Tashrif Billah found in this [repo](https://github.com/pnlbwh/fsl-containers/tree/master) and the file named [Singularity.centos7](https://github.com/pnlbwh/fsl-containers/blob/master/Singularity.centos7).

### SLURM script

`SLURM` scripts provided for sending array and single jobs to HYAK.

Send job/s to SLURM job scheduler with `sbatch`. 

```shell terminal=true
$ sbatch fsl-centos7-array.slurm
```

Monitor job/s with `squeue` and your `UWNetID`.

```shell terminal=true
$ squeue -u <UWNetID>
```

Cancel job/s with `scancel` and the `JOBID`.

```shell terminal=true
$ scancel <JOBID>
```