# BioPython & Python Bioinformatics Workshop
This repository contains all necessary files for an **Introductory Python Bioinformatics Workshop**, using **BioPython** and other related tools.
To download, click on the large "**Code**" button on the top right, or [click here](https://github.com/vsojo/Python_Bioinformatics_Workshop/archive/refs/heads/main.zip).

## Contents
The workshop introduces multiple basic bioinformatics topics, chiefly using BioPython, including:
1. Accessing NCBI databases (e.g., for nucleotide sequences or taxonomy).
1. Reading and writing sequence files with BioPython.
1. Aligning sequences (e.g., with MAFFT or Clustal-Omega).
1. Building phylogenetic trees (with FastTree or IQ-Tree).
1. Parsing those trees and creating publication quality tree images with ETE-3.

---
## Requirements
:warning: This workshop assumes familiarity with both basic Python and Jupyter Notebooks.<br/>
If you have never used Python, I have a separate Introductory Python Workshop [here](https://github.com/vsojo/Python_Workshop).<br/>
If you need a Python refresher and/or an introduction to Jupyter, I recommend using the Jupyter & Python refresher that I produced [here](https://github.com/vsojo/Python_Workshop/blob/master/JupyIntro_PythonRefresher.zip).

### Setting up `conda`
This workshop assumes that you are at least somewhat familiar with `conda` and Jupyter. If you are not, please take a look at the Jupyter intro linked above, which covers conda.
1. Make sure you have [`conda`](https://www.anaconda.com/products/individual) (through either Anaconda or Miniconda) and are using a `conda` environment that has all the required packages. For example, in case you haven't already, I would recommend doing the following in a terminal(Mac/Linux) or the Anaconda prompt (Windows) after installing conda:
```bash
   conda update --all -y
   conda config --add channels bioconda
   conda config --add channels conda-forge
   conda create -n bioinfo jupyter jupyterlab biopython
```
This will create an environment named `bioinfo`, containing all the necessary packages to get started with the workshop.

2. If you already have such an environment, update it regularly (every couple of weeks):
```
   conda update -y -n bioinfo
```
3. Activate the environment (unless you're using the base/root environment):
```
   conda activate bioinfo
```

3. Start Jupter Notebook:
```
   jupyter notebook
```
or Jupyter Lab:
Lab:
```
   jupyter lab
```
A browser window with Jupyter will open. Lab and Notebook are roughly equivalent. Lab is formally the future, but I would still recommend Notebook because it presently runs better with some tools (most significantly Plotly, which we won't use here). For the purposes of this workshop, both will work equally well.

---
## How to follow this workshop
I recommend that you:
1. Open the file called .BEG.ipynb for the lesson that you want to follow.
2. Open the corresponding .html file.
3. Use the HTML file as reference to write the code in the .BEG.ipynb file.

Once you're done, your Notebook should look like the .END.ipynb file.
Alternatively, you could just use the .END.ipynb file, which has all the code in it, but you would miss out on learning by writing the code yourself. 

---
## :warning: Warnings for Windows users :warning:
### 1. Activating Linux inside Windows
You need to activate the Windows Subsystem for Linux (WSL) and have a valid Linux installation inside your Windows machine.
This is a little involved but much easier than in previous times. You don't need a virtual machine or dual-boot system. Linux just works like an app inside your Windows machine, but since Linux is so powerful, you need to allow some special permissions.
Take a look here:
https://docs.microsoft.com/en-us/windows/wsl/install-win10

### 2. Some unavailable `conda` packages
A number of packages are not available for Windows via `conda`. At the time of writing, this includes:
+ [MAFFT](https://mafft.cbrc.jp/alignment/software/).
+ [Clustal-Omega](http://www.clustal.org/omega/).
+ [FastTree](http://meta.microbesonline.org/fasttree/).
+ [IQ-Tree](http://www.iqtree.org/).

In the workshop documents, I will be installing these packages from inside the Jupyter notebooks using `conda`. However, at the time of writing you cannot do that on Windows for these packages. I recommend that you first check whether they are available when you read this, but assuming they are not, then please download and install at least MAFFT and FastTree\*, since we will be using both of them in the workshop. Then, whenever we run one of those programs inside the Jupyter cells in the workshop, you just run them outside Jupyter following the software instructions as you would any other software.<br/>
\*For your real-world research, I strongly recommend that you look into IQ-Tree over FastTree.

-----------
:copyright:**Copyright:** Everything in this repository (i.e. all of this workshop) is released under a [CC-NC-BY-SA v4.0 license](https://creativecommons.org/licenses/by-nc-sa/4.0/). That stands for _Creative-Commons, non-commercial, attribution-required, share-alike_ license. Please do read the specifications of the license but, in brief, this means that I am happy for you to use any of these documents or code in your own research or teaching. If you do redistribute it, however -- whether you change it a little or a lot or leave it exactly as is -- you must credit the original, and you must _never ever_ make any money off of the documents themselves, even if you make a lot of changes to them. You can of course get paid for teaching or for the work you create using what you learn here, but it must be clear to students that the documents themselves are all free (in both cost and access). Again, this applies both to my originals and to anything you make from them.

:pencil: I am always very happy to receive comments and suggestions for improvement at vsojo@amnh.org
