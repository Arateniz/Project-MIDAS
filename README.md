# Project-MIDAS

MIAD (Metody Inteligentnej Analizy Danych) is a class taken by second year students of Technical Physics (second cycle). It revolves around basic machine learning methods such as linear regression, PCA, decision trees and simple neural networks.

__Project-MIDAS__ (Project for the Methods of Intelligent Data Analysis clasS) is supposed to be a (partial) reconstruction of this publication: [Phys. Rev. D 112, 052012 (2025)](https://journals.aps.org/prd/abstract/10.1103/sllb-p3j8)

## Data
The data that are used in this project have been provided to us by our professor. You have to put it inside `data/` directory for the code to run properly. Unfortunately I haven't been able to find the data on the internet yet.

## Instructions for editing `.ipynb` files in this repository

My assumption is that you know how to open and use jupyter notebooks. In order to run Julia code cells in a notebook follow these steps:

### 1. Install Julia

Obviously you need to have Julia installed on your system to run Julia code. You can find instructions for how to install Julia on your OS here: https://julialang.org/downloads/.

### 2. Install IJulia

IJulia is to Julia what IPython is to Python. Essentially, for our use cases in this project, it serves as a backend for Jupyter. In order to install it open the Julia REPL. You can do it by typing
```console
$ julia
```
in your terminal or by launching the Julia REPL app (Windows only, _probably_).

Once you have the REPL launched type in
```console
julia> ]
```
to open the package manager. You should see something like
```console
(@v1.12) pkg>
```
now, or whatever Julia version you're using atm. All you have to do is execute the following command
```console
(@v1.12) pkg> add IJulia
```
and that should install IJulia globally for you.

### 3. Run the notebook

After opening your notebook inside JupyterLab or vscode (make sure to install the Julia extension here) or whatever else you're using, select the Julia kernel. You should now be able to run and edit the notebook. Make sure that you have the `Project.toml` downloaded since it lists all your dependencies. The first time you run the code the first cell will activate a new Julia environment inside the project's directory and will download your dependencies based on `Project.toml`. If you see a `Manifest.toml` inside your directory afterwards, then that's the expected result. Subsequent runs of the first cell should be much faster, since it won't have to download all the dependencies again.