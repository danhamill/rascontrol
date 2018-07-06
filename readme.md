### Readme

This repo was originally forked from [Mike Bannis](https://github.com/mikebannis/rascontrol). Thanks Mike!

This repository is a work in progress.

##### Setup

``` python
conda create --name rascontrol
conda activate rascontrol
pip install numpy scipy psutil ipykernel

``

Install pywin32 from conda-forge

```python
conda config --add channels conda-forge
conda install pywin32
conda config --remove channels conda-forge
```
