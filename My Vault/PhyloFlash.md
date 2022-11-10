# PhyloFlash 
These are some notes that can help with the installation of the program PhyloFlash. Along with this troubleshooting notes along the way. 

## Downloading Package  

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

The dependency Sortmerna is optiional (an alternative to BBmap dependency), if decide to download use (Note: If Conda cannot solve the environment mamba can be used, replacing conda with mamba in the code below)

```
conda create -n pf phyloflash sortmerna=2.1b
```

Installing Phyloflash

```
conda install phyloflash 
```

### Note: If using the Hydra computer via the Smithsonian using the Hydra tool: Qsub generation via telework.si.edu, no need to download as the program is alsready downloaded. Can move to "Setting up Refrence Database" step. 

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

## Prerequisites

Check all dependicies have been downloaded (Note: If not installed through conda these dependencies will need to be installed manually)

```
phyloFlash.pl -check_env
```

Phyloflash dependencies: 
1. [Perl >= 5.13.2](http://www.perl.org/get.html)
2. [EMIRGE](https://github.com/csmiller/EMIRGE)  (and dependencies for EMIRGE)
3. [BBmap](http://sourceforge.net/projects/bbmap/)
4. [Vsearch](https://github.com/torognes/vsearch)
5.  [SPAdes](http://bioinf.spbau.ru/spades)
6. [Bedtools](https://github.com/arq5x/bedtools2)
7. [Mafft](http://mafft.cbrc.jp/alignment/software/)
8. [Barrnap](https://github.com/tseemann/barrnap)
9. Optional: [SortMeRNA](https://github.com/biocore/sortmerna) v2.1b (can be used as an alternative to BBmap)

## Setting up Refrence Database

#### Hydra computer
PhyloFlash is already in installed as a module. In installing the refrence database the QSub Generation Utility on the telework site works best. 
- Memory = 8
- Multi-thread = 8
- Job shell = sh
Can decide to do less memory and or multi-thread, if so set to 6 for both. 


Resrources: [phyloFlash | phyloFlash is a pipeline to rapidly reconstruct the SSU rRNAs and explore the phylogenetic composition of an Illumina (meta)genomic dataset. (hrgv.github.io)](http://hrgv.github.io/phyloFlash/)


