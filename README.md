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
3. Click "Show advanced settings" and populate the following fields:
   - Module directories: `/g/data/xp65/public/modules`
   - Modules: `conda/analysis3 openmpi`
5. Click `Launch` to launch the ARE JupyterLab session.

Once the ARE session is active, it will appear in the `My Interactive Sessions` section of your ARE dashboard. Simply click `Open JupyterLab` to access the session.

Further detailed instructions on launching an ARE JupyterLab session can be found on the [ACCESS-Hive Docs](https://docs.access-hive.org.au/getting_started/are/).

# 2. `git clone` Workshop notebooks

To access the resources required for this workshop, you need to `git clone` this repository to a directory on Gadi. To do this, follow these steps:

1. Open a new terminal window in your JupyterLab session. To do this, click on the `+` in the tab ribbon and select "Terminal".
2. Navigate to a location on Gadi where you have write permission and wish to save these resources. **We recommend simply placing them in your home directory.** You can get here by running `cd ~` in the terminal.
3. Run the following command to create a new directory called "CMWG_workshop_2025" in your current directory:
   
       git clone https://github.com/ACCESS-NRI/CMWG_workshop_2025.git
   
    > ⚠️ **Github Username and Password:** Depending on if/how you have configured git on Gadi, you may be prompted to enter your Github Username and Password in order for this process to complete. Note that if you use a "Personal Access Token (PAT)" with Github, the Password you enter here should be your PAT.

4. Confirm that these workshop resources are now available in the following directory: `~/CMWG_workshop_2025/`

# 3. In JupyterLab

Using the File Browser on the left of your JupyterLab window, navigate to the `CMWG_workshop_2025` directory that you just cloned. Here, you will find one sub-directory:

1. `notebooks/` - This directory contains the following Jupyter Notebooks that form the basis of this workshop:
    - `01_pyISSM_intro.ipynb`: Initial overview of the ISSM model class and sub-classes.
    - `02_pyISSM_vis1.ipynb`: Visualisation of the ISSM model mesh and element/node types.
    - `03_pyISSM_vis2.ipynb`: Visualisation of ISSM model fields and results.
    - `04_pyISSM_grid.ipynb`: Gridding and exporting ISSM models.
    - `05_cryoDatastore_example.ipynb`: A bonus notebook that provides an example usage of the Cryosphere Datapool!
  
Access to another directory (`/g/data/nf33/access-nri/CMWG_workshop_2025/`) is required to access two example ISSM models (and the Cryosphere datapool). Access to this directory should be granted by joining the `nf33` project and by specifying the `gdata/nf33` storage location when activating the ARE JupyterLab Session (Step 1 above). The default options in the workshop notebooks are designed to interact with a model of Antarctica (`antarctica_sample_model.nc`). We also provide a second model, of Greenland (`greenland_sample_model.nc`) for those of you who would like to explore a different ice sheet!

> ⚠️ **Data Sharing:** Please do not copy or share the ISSM models provided in `/g/data/nf33/access-nri/CMWG_workshop_2025/sample_models/`. They are provided for use within this workshop only. Direct access to this directory is not necessary -- models are loaded via the workshop notebooks.

```text
© 2022 ACCESS-NRI and contributors. See the top-level COPYRIGHT file for details. 
SPDX-License-Identifier: Apache-2.0
```
