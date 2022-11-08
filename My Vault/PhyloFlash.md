# PhyloFlash 
These are some notes that can help with the installation of the program PhyloFlash. Along with this troubleshooting notes along the way. 

# Downloading Package 

#### Download via Conda

PhyloFlash is avialable through the Bioconda channel on Conda -Note: Conda can, at times, fail to solve the environement, to whcih Mamba usually helps resolve this. If still using Conda can change priority of channel by trying:
	
```
conda config --set channel_priority strict 
```

Setting up Bioconda 

```
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge
```

Create a new environemnt for Phyloflash 

```
conda create --name pf
```

The dependency Sortmerna is optiional, if decide to download use (Note: If Conda cannot solve the environment mamba can be used, replacing conda with mamba in the code below)

```
conda create -n pf phyloflash sortmerna=2.1b
```

Installing Phyloflash

```
conda install phyloflash 
```

## Note: If using the Hydra computer via the Smithsonian using the Hydra tool: Qsub generation via telework.si.edu, no need to download as the program is alsready downloaded. Can move to "Setting up Database" step. 

#### Download via Github

Downloading from Github is also another option

	Download latest release:
```
wget https://github.com/HRGV/phyloFlash/archive/pf3.4.tar.gz tar -xzf pf3.4.tar.gz
```

	Clone latest development version via Git:
```
git clone https://github.com/HrGV/phyloFlash.git
ls phyloFlash
```

