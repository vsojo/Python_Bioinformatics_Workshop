# Python Biopython & Bioinformatics Workshop
This repository contains all necessary data for my introductory Bioinformatics workshop.

This is **not** an introductory _Python_ workshop. There's one of those [here](https://github.com/vsojo/Python_Workshop).

The contents of the `.ZIP` and `.TAR.GZ` files are identical. Just pick whichever you prefer.

The workshop introduces multiple basic bioinformatics topics, chiefly using BioPython, including:
1. Accessing NCBI databases.
1. Readaing and writing sequences with BioPython.
1. Aligning sequences (with MAFFT or Clustal-Omega).
1. Building phylogenetic trees (with FastTree or IQ-Tree).
1. Parsing those trees and creating images with ETE-3.

:pencil: I am always very happy to receive comments and suggestions for improvement at vsojo@amnh.org

---
## `conda` setup
This workshop assumes that you're at least somewhat familiar with `conda` and Jupyter. If you are not, please take a look at the Jupyter intro [here](https://github.com/vsojo/Python_Workshop).
1. Make sure you have [`conda`](https://www.anaconda.com/products/individual) (either Anaconda or Miniconda) and are using a `conda` environment that has all the required packages. For example, in case you haven't already, I would recommend doing the following in a terminal(Mac/Linux) or the Anaconda prompt (Windows):
   conda update --all -y
   conda config --add channels bioconda
   conda config --add channels conda-forge
   conda create -n bioinfo jupyter jupyterlab biopython
   
2. Activate the environment (unless you're using the base/root environment):
   conda activate bioinfo

3. Start Jupter Lab:
   jupyter lab

A browser window with Jupyter Lab will open.

---
## How to follow this workshop
I recommend that you:
1. Open the file called .BEG.ipynb for the lesson that you want to follow.
2. Open the corresponding .html file.
3. Use the HTML file as reference to write the code in the .BEG.ipynb file.

Once you're done, your Notebook should look like the .END.ipynb file.
Alternatively, you could just use the .END.ipynb file, which has all the code in it. 

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
+ [Clusta-Omega](http://www.clustal.org/omega/).
+ [FastTree](http://meta.microbesonline.org/fasttree/).
+ [IQ-Tree](http://www.iqtree.org/).

I will be installing them inside my Jupyter notebooks using `conda`, but at the time of writing, you can't do that on Windows. I recommend that you first check if they now work, but assuming they don't, then please download and install at least MAFFT and FastTree\*, since we will be using both of them in the workshop. Then, whenever you see me run one of those programs inside the Jupyter cells in the workshop, you just run them outside Jupyter following the software instructions as you would any other software.<br/>
\*For your real-world research, I strongly recommend that you look into IQ-Tree.

-----------
:copyright:**Copyright:** Everything in this repository (i.e. all of this workshop) is released under a [CC-NC-BY-SA v4.0 license](https://creativecommons.org/licenses/by-nc-sa/4.0/). That stands for _Creative-Commons, non-commercial, attribution-required, share-alike_ license. Please do read the specifications of the license but, in brief, this means that I'm happy for you to use any of this stuff in your own work or teaching. If you do redistribute it, though -- whether you change it a little or a lot or leave it exactly as is -- you must credit the original, and you must _never ever_ make any money off of the document itself, even if you make a lot of changes to it. You can of course get paid for teaching, but it must be clear to students that the documents themselves are all free (in both cost and access). Again, this applies both to my originals and to anything you make from them.
