### Readme

This repo was originally forked from [Mike Bannis](https://github.com/mikebannis/rascontrol). Thanks Mike!

This repository is a work in progress. The overall goal is to develop a toolbox to assist a modeler with the calibration and verification of models built in HEC-RAS.  

##### My Development environment

- conda 4.4.10
- python 3.5
- Windows 10

##### Setup
Here are some packages I think Ill need in myu virtual environment
```
conda create --name rascontrol
conda activate rascontrol
pip install numpy scipy psutil ipykernel
```

Install pywin32 from conda-forge

```
conda config --add channels conda-forge
conda install pywin32
conda config --remove channels conda-forge
```

Create virtual environment kernel for testing in atom

```
python -m ipykernel install --user --name rascontrol
```

#### Git workflow
I will do all feature development on a local develop branch.  I rarely will push to `master`, but will routinely push to the development branch `dev`. A typical workflow is:

```
1. git checkout dev-dan
    - Develop and commit as many features as I like
3. git checkout dev
4. git pull dev
    - A bit excessive since I am working by myself,
      but none the less I want to resolve any differences
5. git checkout dev-dan
6. git rebase dev
    - rebase with dev to make the commits appear linear
7. git checkout dev
8. git merge dev-dan
    - Merge the development branch with the main dev branch
9. git push origin dev
```
