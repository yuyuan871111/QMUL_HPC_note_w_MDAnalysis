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
```


### Get started with the tutorials
[Tutorial01-quickstart](./Tutorial_notebook/Tutorial01_quickstart.ipynb): learn how to 
(1) load a structure or trajectory, 
(2) select atoms, chains, residues, and universe
(3) work with trajectory
(4) write out coordinates
(5) use methods to analyse the trajectory


## Trouble shooting
```bash
touch rapid_testing.ipynb
```
