These are some notes that can help with the installation of the program PhyloFlash. Along with this troubleshooting notes along the way. 


```
```Downloading Package

Dowload via Conda
	PhyloFlash is available through the Bioconda channel on Conda (Note: Conda can, at times, fail to solve the environemnt, to which Mamba usually helps resolve this. If still using Conda try: conda config --set channel_prioroty strict)
	Setting up Bioconda
		conda config --add channels defaults
		conda config --add channels bioconda
		conda config --add channels conda-forge
	Create new environment named "phyloflash"
			Sortmerna is an optional dependency, if using do
				conda create -n "phyloflash" sortmerna 2.1b (If conda cannot solve the environemnt mamba is required in the base environment, can replace conda with mamba with)

Dowload via Github
	Downloading latest version 
		wget https://github.com/HRGV/phyloFlash/archive/pf3.4.tar.gz tar -xzf pf3.4.tar.g 
		




