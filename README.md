# ACCESS-NRI 2025 -- CMWG Workshop
September 12, 2025

**Welcome to the ACCESS-NRI Cryosphere Modelling Working Group (CMWG) 2025 Science Day!**

This session provides an introduction to ISSM and, specifically, [pyISSM](https://github.com/ACCESS-NRI/pyISSM), the Python API for [ISSM](https://github.com/ISSMteam/ISSM) under development by ACCESS-NRI. This is intended to be an interactive session. There are a few necessary steps to get up-and-running, detailed below.

# 1. Activate an ARE JupyterLab Session

The Australian Research Environment (ARE) is a web-based graphical interface for performing computational research on National Computational Infrastructure (NCI) *Gadi* supercomputer. It allows users to interactively run Python

> ⚠️ **NCI account & project access:** To use ARE, you must have an NCI account and be a member of a project with available computing resources.
>For this workshop, you will require access to NCI project `nf33` and `xp65`. If you have not requested to join these projects, you can do so by logging into your [NCI account](https://my.nci.org.au/).

To start an ARE JupyterLab session, go to the [ARE JupyterLab](https://are.nci.org.au/pun/sys/dashboard/batch_connect/sys/jupyter/ncigadi/session_contexts/new) page and follow these steps:

1. Log in with your NCI username and password.
2. Configure the following PBS directives:
    - Walltime (hours): `4`
    - Queue: `normalbw`
    - Compute Size: `medium`
    - Project: `nf33`
    - Storage: `gdata/nf33`
3. Click `Launch` to launch the ARE JupyterLab session.

One the ARE session is active, it will appear in the `My Interactive Sessions` section of your ARE dashboard. Simply click `Open JupyterLab` to access the session.

Further detailed instructions on launching an ARE JupyterLab session can be found on the [ACCESS-Hive Docs](https://docs.access-hive.org.au/getting_started/are/).

# 2. In JupyterLab

Once in JupyterLab, navigate to the workshop directory here: `/g/data/nf33/access-nri/CMWG_workshop_2025/`. Here, you'll find two directories:

1. `notebooks/` - This directory contains the following Jupyter Notebooks that form the basis of this workshop:
    - `01_pyISSM_intro.ipynb`: Initial overview of the ISSM model class and sub-classes.
    - `02_pyISSM_vis1.ipynb`: Visualisation of the ISSM model mesh and element/node types.
    - `03_pyISSM_vis2.ipynb`: Visualisation of ISSM model fields and results.
    - `04_pyISSM_grid.ipynb`: Gridding and exporting ISSM models.
2. `sample_models/` - This directory contains two example ISSM models. The default options in the notebooks are designed to interact with a model of Antarctica (`zrun_yearly_aSMB_HadGEM2_ctrl_2300_again.nc`). We also provide a second model, of Greenland (`Greenland.HistoricTransient_200yr.nc`) for those of you who would like to explore a different ice sheet!

> ⚠️ **Data Sharing:** Please do not copy or share the ISSM models provided in `sample_models/`. They are provided for use within this workshop only.

```text
© 2022 ACCESS-NRI and contributors. See the top-level COPYRIGHT file for details. 
SPDX-License-Identifier: Apache-2.0
```
