# installing-python
How to install, run and manage Python

# Installing Miniconda

[Video Guide](https://ual.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=216db530-2583-4017-88aa-b07b00ec438f)

You will be installing Python using a package called Miniconda. 

This will give you Python, as well as some useful packages that you’ll need, as well as a way for you to manage and switch between different python environments (more on that later), and install new packages and libraries.

This is a lightweight version of a larger package you may have heard of called Anaconda. If you already have Anaconda installed, you can ignore the rest of this set up for now!

## How do I know if I have conda installed?

### Mac OSX

Open up a Terminal and type ``which conda``

### Windows

Open up a Terminal and type ``where conda``

If its says something to the effect of ``conda not found``, then you are good to go!

## Installing Miniconda 

Go to the [Downloads page](https://docs.conda.io/en/latest/miniconda.html) and get the installer for **your machine**

### Mac OSX

Is your Mac an M1, M2 or M3? If so, get the correct installer (Miniconda3 macOS Apple M1 64-bit pkg)! 

Older intel Macs should use (Miniconda3 macOS Intel x86 64-bit pkg)

### Windows

You probably have a 64 bit machine (Miniconda3 Windows 64-bit)

Follow the instructions on the installer that runs 

## Check Installation 

Close any open Terminals or Command Prompts, then **reopen** a new one 

### Mac OSX

* ``which conda`` should return a message 
* ``which python`` should return a file path to a miniconda installation 

### Windows

* ``where conda`` should return a message 
* ``where python`` should return a file path to a miniconda installation 

## What if Miniconda installation fails?

### Windows or Intel Mac

#### Install Anaconda Naviagator 

There is an alternative way to get ``conda`` and ``Python`` on your computer, along with some software to view and manage packages and environments. Its called Anaconda Navigator and you can [follow these download instructions](https://www.anaconda.com/download)

## Setting up a conda environment 

### Create the environment
We are going to create a new conda environment (a specific collection of packages) for this unit (recommended if you are doing other Python/ML work on the same machine, or if you're on a shared machine)

You can use the terminal/console and type 

``conda create --name stem python=3.10`` 

This will create a Python 3.10 environment named "stem" (you can choose some other memorable name if you'd like)

Once you've created an environment, install jupyter and pandas in this environment using the terminal console:

``conda activate stem``

``conda install -c conda-forge -y pandas jupyter``

You will know you have been successful because the environment name will appear at the front of the terminal line in brackets 

For example

``(stem) louisbusby@Louiss-MBP-3 STEM-4-Creatives-22-23``

If you do create an environment for this unit, just make sure you're always using that environment when you work on lab/project activities!

# Running Code

First we need to get the code for this unit onto our local machines.

## GitHub App

All the code for this unit lives in something called a “repository”. The largest
commercial version of this is [GitHub](https://github.com)

We have our own version at (https://git.arts.ac.uk). The easiest way to get code, and weekly updates, is to use the Github App.

### Getting Code

#### Option 1: Using GitHub Desktop

To download (clone) the contents of a repository for the first time:

  * First, download and install GitHub Desktop
  
  * Then, navigate to the URL of the repository you want to clone (this will be a http://git.arts..... address and will be provided for each different unit)
  
  * Look for the green button near the top of the page that says "Code." Hit this button then select "Open with GitHub Desktop."
  
  * In GitHub Desktop, set the "local path" directory in the pop-up so that you're happy with it - this is where your local copy of the repository will live.
  
  * Hit "Clone" and you're done!

To get updates to a repository you've previously cloned:

  * In GitHub Desktop, ensure you've selected the correct repository (name will be shown on top left of the window)
  
  * Then hit "fetch origin."

The video below illustrates these steps:


https://git.arts.ac.uk/lmccallum/installing-python/assets/23/041880eb-8cf4-4441-b3a6-695d95ab6327


#### Option 2: Using the command line and ssh:

To download (clone) the contents of a repository for the first time:

  * First, set up an ssh key for yourself [using these instructions](https://docs.github.com/en/enterprise-server@2.22/authentication/connecting-to-github-with-ssh)
  * Then, navigate to the URL of the repository you want to clone (this will be a http://git.arts..... address and will be provided for each different unit)
  * Look for the green button near the top of the page that says "Code." Hit this button then select "SSH" then copy the URL just below (e.g., git@git.arts.ac.uk:rfiebrink/ExploringMachineIntelligence_Spring2022.git)
  * Then, in a terminal/console window, navigate to the directory on your machine where you want to download the repository. Then type "git clone" followed by the URL you just copied (e.g., "git clone git@git.arts.ac.uk:rfiebrink/ExploringMachineIntelligence_Spring2022.git"). This will download the full repository into that directory.

To get updates to a repository you've previously cloned:

  * In a terminal/console window, navigate to the directory on your machine where your repository lives.
  * Type "git pull" to grab any new files or changes and put them in your local copy of the repository.
  
  The video below illustrates these steps:

https://git.arts.ac.uk/lmccallum/installing-python/assets/23/8910d880-fc81-4ccc-aad6-db1d11ef6d36


## VSCode
[Video guide](https://ual.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=d7ebfac4-3802-45da-a4ae-b07d00e44517)(install VSCode and create conda enviroment)

[Download Visual Studio Code](https://code.visualstudio.com/)
Essential plugins to install:
- [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
- [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
- [pip manager](https://marketplace.visualstudio.com/items?itemName=slightc.pip-manager)

Additional reccomended plugins:
- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
- [Edit csv](https://marketplace.visualstudio.com/items?itemName=janisdd.vscode-edit-csv)
- [JSON tools](https://marketplace.visualstudio.com/items?itemName=eriklynd.json-tools)

## Troubleshooting Python

- Which install of Python are you using? `which python` (unix) `where python` (windows)
- Which version of Python are you using? `python —-version`
- Which install of pip are you using? `which pip` (unix) `where pip` (windows)
- Which version of package is installed using pip? `pip show [package name]`
- Which install of Anaconda are you using? `which conda` (unix) `where conda` (windows)
- Which version of package is installed using Anaconda? `conda list [package name]`






