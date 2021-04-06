This is Victor Sojo's introductory Bioinformatics with Python Workshop.
Please contact me at <vsojo@amnh.org> if you have any comments or suggestions.

###############################
#  WARNING FOR WINDOWS USERS  #
###############################
You need to activate the Windows Subsystem for Linux (WSL) and have a valid Linux installation inside your Windows machine.
This is a little involved but much easier than in previous times. You don't need a virtual machine or dual-boot system. Linux just works like an app inside your Windows machine, but since Linux is so powerful, you need to allow some special permissions.
Take a look here:
https://docs.microsoft.com/en-us/windows/wsl/install-win10


###################
#   CONDA SETUP   #
###################
1. Make sure you have conda (either Anaconda or Miniconda) and are using a conda environment that has all the required packages. For example, in case you haven't already, I would recommend doing the following in a terminal(Mac/Linux) or the Anaconda prompt (Windows):
   conda update --all -y
   conda config --add channels bioconda
   conda config --add channels conda-forge
   conda create -n bioinfo jupyter jupyterlab biopython
   
2. Activate the environment (unless you're using the base/root environment):
   conda activate bioinfo

3. Start Jupter Lab:
   jupyter lab

A browser window with Jupyter Lab will open.


#################################
#  HOW TO FOLLOW THIS WORKSHOP  #
#################################
I recommend that you:
1. Open the file called .BEG.ipynb for the lesson that you want to follow.
2. Open the corresponding .html file.
3. Use the HTML file as reference to write the code in the .BEG.ipynb file.

Once you're done, your Notebook should look like the .END.ipynb file.
Alternatively, you could just use the .END.ipynb file, which has all the code in it. 
