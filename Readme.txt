
# PyCh

PyCh is a Python package based on SimPy for discrete-event simulation.
It is a tool developed for the course "Analysis of production systems" (4DC10).
PyCh is a port of [Chi3](https://cstweb.wtb.tue.nl/chi/trunk-r9682/).

## Contents
- Tutorials chapter 1 - 10 contain the tutorial on how to use PyCh
- Offline_PyCh_tutorial2022 contains the tutorial in PDF format (for reference)
- Assignment.ipynb contains the jupyter notebook for the course assignment.
- LectureNotesExamples.ipynb - contains the jupyter notebook of all models used in the lecture notes
- LectureSlidesExamples.ipynb - contains the jupyter notebook of all models used in the lecture slides

## How to install
1.	Download and install the latest version of anaconda
    -	https://www.anaconda.com/products/individual 
2.	Open an `Anaconda prompt (Anaconda3)` (you can type it in the windows bar below), and enter the following commands:
    - `conda create --name pychEnv`
        - Enter `y` (for yes)
    -	`conda activate pychEnv`
    -	`conda install git pip ipykernel`
        - Enter `y` (for yes)
    -	`python -m ipykernel install --user --name pychEnv --display-name "Python (pychEnv)"`
    -	`pip install git+https://github.com/Nickp1993/Pych/`
    -	Close this window (do not continue with the "how to use" without closing!)
3.	You have finished installation, continue with the "How to use" below to start a notebook

## How to use
1. Download the notebook files
    -   Click the green button above, and click download ZIP (or [click here](https://github.com/Nickp1993/4DC10-student/archive/refs/heads/main.zip))
    -   Extract the ZIP-file.
        - E.g. to `C:\4DC10\notebooks`
2. Every time you want to start jupyter notebook: 
    -   Open the anaconda prompt (found in windows menu)
    -   In anaconda, set the path to that of your notebooks folder by entering `cd <path>` with `<path>` the path of your notebooks folder. If you are not using your default drive (`C:\`), use `cd /D <path>`.
        - E.g. `cd C:\4DC10\notebooks`, or `cd /D F:\4DC10\notebooks`
    -   Enter `jupyter notebook`
    -	Wait till a local server has started, your browser should open it automatically, if not, [try clicking this links](http://127.0.0.1:8888/)
    -   Open one of the notebooks (files with an `.ipynb` extension)
    -	In the menubar, click kernel > change kernel >  Python (pychEnv)
3. You can now use this notebook!
    -   You can now click run to execute the cells of the notebook one-by-one (jupyter notebooks work top-down)
    -   [Click this link for information on how jupyter notebook works](https://realpython.com/jupyter-notebook-introduction/)

## Troubleshooting
- Most errors are caused by not following the *How to install* instruction carefully enough.
- If you get the error `No module named 'PyCh'` when you try to run the command `from PyCh import *`, then PyCh has likely not been installed correctly.
- The same goes if you get a `Numpy importerror`.
- Make sure you open ``Anaconda Prompt (Anaconda3)`` and not another version (such as `Anaconda Prompt` **without Anaconda3**)!
- If you get a `EnvironmentNotWritableError` or `Error [WinError 2]` during installation, try running the anaconda prompt as administrator, and then try installing again.
- If you get a `CondaSSLError`, the solution is as follows:
    1. Find your anaconda installation directory (e.g. `C:\ProgramData\Anaconda3` or `C:\Users\<username>\Anaconda3`)
    2.  Go to the subdirectory`\Anaconda3\Library\bin\` and copy the files `libcrypto-1_1-x64.dll` and `libssl-1_1-x64.dll`.
    3. Paste these files in the following subdirectory: `\Anaconda3\DLLs\`.
- If you get an error code 128 while executing `pip install git+https://github.com/Nickp1993/Pych/`, you can instead try the following command: `pip install https://github.com/Nickp1993/PyCh/archive/master.tar.gz`.
- If you had a previous installation of Anaconda, this could cause issues. If so, contact a TA for help. The easiest solution generally is a clean install of Anaconda.
