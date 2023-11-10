# QMUL_HPC_note_w_MDAnalysis
This is a QMUL HPC usage note and project template.
MDAnalysis tutorial is derived from the official page of the [MDAnalysis User Guide](https://userguide.mdanalysis.org/stable/index.html). The used version of the package is ***2.6.1***.

## Research template w/ MDAnalysis 2.6.1

### Install MDAnalysis using conda (recommended, because pip is not install all functions)
#### quick install 
```bash
# previously test on Linux 3.10.0-1160.83.1.el7.x86_64 x86_64
# but may conflict on other system or due to its version
conda env create --name mdanalysis --file environment.yml -y
conda activate mdanalysis
```

#### one by one
```bash
conda create --name mdanalysis python=3.9
conda activate mdanalysis
conda config --add channels conda-forge
conda install mdanalysis=2.6.1 -y   # install mdanalysis
conda update mdanalysis             # (optional) update mdanalysis 
conda install MDAnalysisTests -y    # install test_resource
conda install mdanalysisdata -y     # install package for getting additional dataset

## other python packages
conda install ipywidgets -y         # install ipynb for VScode
conda install ipykernel -y          # install ipynb for VScode
conda install openmm -y
conda install parmed -y
conda install nglview=2.7.7 -y            # Optionally, use NGLView to interactively view your trajectory
conda install moviepy -y            # Optionally, create the movie
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

[Tutorial06 - Distances and contacts](./Tutorial_notebook/Tutorial06_dist_contacts.ipynb): learn how to   
(1) Atom-wise distances between matching AtomGroups.  
(2) All distances between two selections
All distances within a selection.  
(3) Fraction of native contacts over a trajectory.  
(4) Q1 vs Q2 contact analysis.  
(5) Contact analysis: number of contacts within a cutoff.  
(6) Write your own native contacts analysis method.  

[Tutorial07 - Trajectory similarity](./Tutorial_notebook/Tutorial07_TrajSimilar.ipynb): learn how to  
(1) Comparing the geometric similarity of trajectories.  
(2) Calculating the Harmonic Ensemble Similarity between ensembles.  
(3) Calculating the Clustering Ensemble Similarity between ensembles.  
(4) Calculating the Dimension Reduction Ensemble Similarity between ensembles.  
(5) Evaluating convergence.  

[Tutorial08 - Structure analysis](./Tutorial_notebook/Tutorial08_StructureAnaly.ipynb): learn how to  
(1) Elastic network analysis.  
(2) Average radial distribution functions.  
(3) Calculating the RDF atom-to-atom.  
(4) Protein dihedral angle analysis.  
(5) Helix analysis.  

[Tutorial09 - Dimenstion reduction](./Tutorial_notebook/Tutorial09_dimReduce.ipynb): learn how to  
(1) Perform principal component analysis for a trajectory.  
(2) Perform non-linear dimension reduction to diffusion maps.  

[Tutorial10 - Polymers and membranes](./Tutorial_notebook/Tutorial10_polymer_member.ipynb): learn how to  
(1) Determining the persistence length of a polymer.  
(2) Analysing pore dimensions with HOLE2.  

[Tutorial11 - Volumetric analyses](./Tutorial_notebook/Tutorial10_polymer_member.ipynb): learn how to   
(1) Compute mass and charge density on each axis.  
(2) Calculate the solvent density around a protein.  

[Tutorial12 - transform views to images and videos](./Tutorial_notebook/Tutorial12_nglview_video.ipynb): learn to create a images and videos from NGL view.

[Tutorial13 - automatically transforming trajectory to videos](./Tutorial_notebook/Tutorial13_nglview_video_func.ipynb): try to develop a function to generate the trajectory video. (but there are some bugs that `the video is fixed` and `have to waiting for the image generations with unpredictable time`)





## Trouble shooting
```bash
touch rapid_testing.ipynb
```
