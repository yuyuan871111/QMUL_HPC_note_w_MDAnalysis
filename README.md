# QMUL_HPC_note_w_MDAnalysis
This is a QMUL HPC usage note and project template.
MDAnalysis tutorial is derived from the official page of the [MDAnalysis User Guide](https://userguide.mdanalysis.org/stable/index.html). The used version of the package is ***2.6.1***.

## Research template w/ MDAnalysis 2.6.1

### Install MDAnalysis using conda (recommended, because pip is not install all functions)
#### quick install 
```bash
# previously test on Linux 3.10.0-1160.83.1.el7.x86_64 x86_64
# but may conflict on other system or due to its version
conda create --name mdanalysis --file environment.yml
conda activate mdanalysis
```

#### one by one
```bash
conda create --name mdanalysis python=3.10
conda activate mdanalysis
conda install -c conda-forge mamba              # install mamba

mamba install -c conda-forge mdanalysis         # install mdanalysis
mamba update mdanalysis                         # (optional) update mdanalysis 
mamba install -c conda-forge MDAnalysisTests    # install test_resource
conda install -c conda-forge mdanalysisdata     # install package for getting additional dataset

conda install -c conda-forge ipywidgets         # install ipynb for VScode
conda install -c conda-forge openmm
```
#### other python modules needed
```bash
pip install parmed
pip install nglview         # Optionally, use NGLView to interactively view your trajectory
pip install moviepy         # Optionally, create the movie
```

### Get started with the tutorials
[Tutorial01 - quick start](./Tutorial_notebook/Tutorial01_quickstart.ipynb): learn how to  
(1) load a structure or trajectory.  
(2) select atoms, chains, residues, and universe.  
(3) work with trajectory.  
(4) write out coordinates.  
(5) use methods to analyse the trajectory.  

[Tutorial02 - modify universe](./Tutorial_notebook/Tutorial02_modifyuniverse.ipynb): learn how to  
(1) create a Universe consisting of water molecules.  
(2) merge this with a protein Universe loaded from a file.  
(3) create custom segments labeling protein domains.  


[Tutorial03 - center the trajectory](./Tutorial_notebook/Tutorial03_centeringTraj.ipynb): learn how to  
(1) use MDAnalysis transformations to make a protein whole.  
(2) center it in the box.  
(3) wrap the water back into the box.

[Tutorial04 - using ParmEd with MDAnalysis and OpenMM](./Tutorial_notebook/Tutorial04_ParmEdsimu.ipynb): learn how to   
(1) use MDAnalysis to convert a ParmEd structure to an MDAnalysis Universe.  
(2) select a subset of atoms.   
(3) convert it back to ParmEd to simulate with OpenMM.  

[Tutorial05 - alignments and RMS fitting](./Tutorial_notebook/Tutorial05_alignRMSfit.ipynb): learn how to   
(1) align a structure to another.  
(2) align a trajectory to a reference.  
(3) align a trajectory to itself.  
(4) calculate the root mean square deviation (RMSD) of atomic structures.  
(5) calculate the pairwise RMSD of a trajectory.  
(6) calculate the root mean square fluctuation (RMSF) over a trajectory.  

## Trouble shooting
```bash
touch rapid_testing.ipynb
```
