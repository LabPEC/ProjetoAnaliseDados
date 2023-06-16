# Installation

We will show the installation steps using a bash shell on a Linux system. You may need to adapt these commands to your own system. 

## Download this repository
To install this repository and run the Jupyter notebooks on your machine, you will first need git, which you may already have. Open a terminal and type `git` to check. If you do not have git, you can download it from [git-scm.com](https://git-scm.com/).

Next, clone this repository by opening a terminal and typing the following commands (do not type the first `$` on each line, it's just a convention to show that this is a terminal prompt, not something else like Python code):

    $ cd $HOME  # or any other development directory you prefer
    $ git clone https://<GITHUB_ACCESS_TOKEN>@github.com/LabPEC/ProjetoADERES
    $ cd ProjetoADERES

## Install Anaconda
Next, you will need Python 3 and a bunch of Python libraries. The simplest way to install these is to [download and install Anaconda](https://www.anaconda.com/distribution/), which is a great cross-platform Python distribution for scientific computing. It comes bundled with many scientific libraries, including NumPy, Pandas, Matplotlib, Scikit-Learn and much more, so it's quite a large installation. If you prefer a lighter weight Anaconda distribution, you can [install Miniconda](https://docs.conda.io/en/latest/miniconda.html), which contains the bare minimum to run the `conda` packaging tool. You should install the latest version of Anaconda (or Miniconda) available.

In Linux, after download the Anaconda atual version (.sh file), execute in your downloads directory the [comand](https://mas-dse.github.io/startup/anaconda-ubuntu-install/)
    
    $ bash Anaconda3-<ATUAL VERSION>-Linux-x86_64.sh

During the installation on MacOSX and Linux, you will be asked whether to initialize Anaconda by running `conda init`: you should accept, as it will update your shell script to ensure that `conda` is available whenever you open a terminal. After the installation, you must close your terminal and open a new one for the changes to take effect.

During the installation on Windows, you will be asked whether you want the installer to update the `PATH` environment variable. This is not recommended as it may interfere with other software. Instead, after the installation you should open the Start Menu and launch an Anaconda Shell whenever you want to use Anaconda.

Once Anaconda (or Miniconda) is installed, run the following command to update the `conda` packaging tool to the latest version:

    $ conda update -n base -c defaults conda

## Create the `PjAd` Environment

If you would like to work in an isolated environment (which is strongly recommended so you can work on different projects without having conflicting library versions). With Anaconda, you can create, export, list, remove, and update environments that have different versions of Python and/or packages installed in them [managing environments in Anaconda](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#activating-an-environment).

You can create a isolated enviroment from scratch (see next [section](https://github.com/LabPEC/ProjetoADERES/blob/main/INSTALL.md#creating-an-isolated-environment)) or create an environment from an environment.yml file (see Section [Creating an environment from an environment.yml file](https://github.com/LabPEC/ProjetoADERES/blob/main/INSTALL.md#creating-an-environment-from-an-environmentyml-file))

#### Creating an Isolated Environment

Make sure you're in the `ProjetoADERES` directory and run the following commands. It will create a new `conda` environment containing every library you will need to run all the notebooks (by default, the environment will be named `PjAd`, but you can choose another name using the `-n` option):

Create an environment PjAd:

    $ conda create -n PjAd

Next, activate the new environment:

    $ conda activate PjAd

Now you can install all the required modules and their dependencies using this simple command:

    $ conda install jupyter matplotlib numpy pandas scipy scikit-learn ipykernel openpyxl

You can also create an environment from an environment.yml file (see next section). The `environment.yml` given in this project was created from the active environment `PjAd` using command:

    $ conda env export > environment.yml

#### Creating an environment from an environment.yml file

Make sure you're in the `ProjetoADERES` directory and run the following command. It will create a new `conda` environment containing every library you will need to run all the notebooks (by default, the environment will be named `PjAd`, but you can choose another name using the `-n` option):

    $ conda env create -f environment.yml

Next, activate the new environment:

    $ conda activate PjAd


## Start Jupyter
You're almost there! You just need to register the `PjAd` conda environment to Jupyter. The notebooks in this project will default to the environment named `python3`, so it's best to register this environment using the name `python3` (if you prefer to use another name, you will have to select it in the "Kernel > Change kernel..." menu in Jupyter every time you open a notebook):

    $ python3 -m ipykernel install --user --name=python3

You can now start Jupyter like this:

    $ jupyter notebook

This should open up your browser, and you should see Jupyter's tree view, with the contents of the current directory. If your browser does not open automatically, visit [localhost:8888](http://localhost:8888/tree). Click on `index.ipynb` to get started.

Congrats! You are ready to learn Machine Learning, hands on!

When you're done with Jupyter, you can close it by typing Ctrl-C in the Terminal window where you started it. Every time you want to work on this project, you will need to open a Terminal, and run:

    $ cd $HOME # or whatever development directory you chose earlier
    $ cd ProjetoADERES
    $ jupyter notebook

## Update This Project and its Libraries
I regularly update the notebooks to fix issues and add support for new libraries. So make sure you update this project regularly.

For this, open a terminal, and run:

    $ cd $HOME # or whatever development directory you chose earlier
    $ cd ProjetoADERES # go to this project's directory
    $ git pull

If you get an error, it's probably because you modified a notebook. In this case, before running `git pull` you will first need to commit your changes. I recommend doing this in your own branch, or else you may get conflicts:

    $ git checkout -b my_branch # you can use another branch name if you want
    $ git add -u
    $ git commit -m "describe your changes here"
    $ git checkout master
    $ git pull

Next, let's update the libraries. First, let's update `conda` itself:

    $ conda update -c defaults -n base conda

Next, activate the `PjAd` environment:

    $ conda activate PjAd

Lastly, we start Jupyter:

    $ jupyter notebook
    
After you change files and directories and if you are not working in colaboration, you must save your changes and update your repository commiting directly to the `main` branch to avoid future conflicts:

    $ git status
    $ git add -A
    $ git status
    $ git commit -a -m "your message here"
    $ git push
