# ACCESS-NRI 2025 -- CMWG Workshop
September 12, 2025

**Welcome to the ACCESS-NRI Cryosphere Modelling Working Group (CMWG) 2025 Science Day!**

This session provides an introduction to ISSM and, specifically, [pyISSM](https://github.com/ACCESS-NRI/pyISSM), the Python API for [ISSM](https://github.com/ISSMteam/ISSM) under development by ACCESS-NRI. This is intended to be an interactive session for users to work through a series of tutorials at their own pace. There are a few necessary steps to get up-and-running, detailed below.

# 0. Pre-workshop preparation

❗*To get the most from the workshop, please complete these "pre-workshop preparation" steps before the workshop*❗

- **NCI Account** - This workshop has been designed to operatre on the Australian Research Environment (ARE), a web-based graphical interface for performing computational research on the National Computational Infrastructure (NCI) *Gadi* supercomputer. In order to access ARE, you will require an NCI account. If you do not have an NCI account, you can sign up [here](https://my.nci.org.au/mancini/signup/0).

- **NCI Project Membership** - To run the exercises you will require access to two specific projects on *Gadi*:
    - [`nf33` - ACCESS-NRI Training](https://my.nci.org.au/mancini/project/nf33) - This project hosts sample ISSM model files used throughout this workshop.
    - [`xp65` - ACCESS Analysis Environments](https://my.nci.org.au/mancini/project/xp65) - This project hosts the shared `analysis3` conda environment that contains all the Python packages used throughout the workshop.
 
  *Please request to join these projects at least 1-2 days before the workshop to allow for your request to be approved.*

# 1. Activate an ARE JupyterLab Session

The Australian Research Environment (ARE) is a web-based graphical interface for performing computational research on National Computational Infrastructure (NCI) *Gadi* supercomputer. It allows users to run JupyerLab, an interactive development environment for notebooks, code, and data. We will use JupyterLab to run a series of tutorials developed using notebooks.

> ⚠️ **NCI account & project access:** To use ARE, you must have an NCI account and be a member of a project with available computing resources.
>For this workshop, you will require access to NCI projects `nf33` and `xp65`. If you have not requested to join these projects, you can do so by logging into your [NCI account](https://my.nci.org.au/) (See Step 0 above).

Detailed instructions on how to start an ARE JupyterLab session for this workshop are included [here](LINKTOWALKTHROUGH) and summarised below:

1. Navigate to the [ARE Dashboard](https://are.nci.org.au/pun/sys/dashboard) and Login with your NCI username and password.
2. Select **JupyterLab** from the "Featured Apps" list
3. Configure the session with the following options:
    - Walltime (hours): `4`
    - Queue: `normalbw`
    - Compute Size: `medium`
    - Project: `nf33`
    - Storage: `gdata/nf33+gdata/xp65`
4. Click "Show advanced settings" and populate the following fields:
   - Module directories: `/g/data/xp65/public/modules`
   - Modules: `conda/analysis3`
5. Click `Launch` to launch the ARE JupyterLab session.

Once you have clicked `Launch`, the browser will redirect to the "My Interactive Sessions" page of your ARE dashboard. Here, you'll see your JupyterLab instance. It might take a few minutes for the instance to launch, but once it's ready, simply click `Open JupyterLab` to access the session.

Further detailed instructions on launching an ARE JupyterLab session can be found on the [ACCESS-Hive Docs](https://docs.access-hive.org.au/getting_started/are/).

# 2. `git clone` Workshop notebooks

To access the resources required for this workshop, you need to `git clone` this repository to a directory on Gadi. To do this, follow these steps:

1. Open a new terminal window in your JupyterLab session. To do this, click on the `+` in the tab ribbon and select "Terminal".
2. Navigate to a location on Gadi where you have write permission and wish to save these resources. **We recommend simply placing them in your home directory.** You can get here by running `cd ~` in the terminal.
3. Run the following command to create a new directory called "CMWG_workshop_2025" in your current directory:
   
       git clone https://github.com/ACCESS-NRI/CMWG_workshop_2025.git
   
    > ⚠️ **Github Username and Password:** This repository is public and you *do not* need to write to the repository for this workshop. Therefore, a Github username and password is not required. If you have already configured `git` on *Gadi* you *may* be prompted to enter your Github Username and Password in order for this process to complete. Note that if you use a "Personal Access Token (PAT)" with Github, the Password you enter here should be your PAT.

4. Confirm that these workshop resources are now available in the following directory: `~/CMWG_workshop_2025/`

# 3. Self-paced tutorials in JupyterLab

This workshop comprises 5 self-paced tutorials that are accessible in the `CMWG_workshop_2025` directory that you just cloned. Using the File Browser on the left of your JupyterLab window, navigate to the `CMWG_workshop_2025` directory. Here, you will find one sub-directory:

1. `notebooks/` - This directory contains the following Jupyter Notebooks that form the basis of this workshop:
    - `01_pyISSM_intro.ipynb`: Initial overview of the ISSM model class and sub-classes.
    - `02_pyISSM_vis1.ipynb`: Visualisation of the ISSM model mesh and element/node types.
    - `03_pyISSM_vis2.ipynb`: Visualisation of ISSM model fields and results.
    - `04_pyISSM_grid.ipynb`: Gridding and exporting ISSM models.
    - `05_cryoDatastore_example.ipynb`: A bonus notebook that provides an example usage of the Cryosphere Datapool!
  
Access to another directory (`/g/data/nf33/access-nri/CMWG_workshop_2025/`) is required to access two example ISSM models (and the Cryosphere datapool). Access to this directory should be granted by joining the `nf33` project and by specifying the `gdata/nf33` storage location when activating the ARE JupyterLab Session (Step 1 above). The default options in the workshop notebooks are designed to interact with a model of Antarctica (`antarctica_sample_model.nc`). We also provide a second model, of Greenland (`greenland_sample_model.nc`) for those of you who would like to explore a different ice sheet!

To open a notebook, simply double click the notebook. You can execute cells in the notebook using the arrow button in the control panel along the top of the notebook, or simply using `<shift>+<enter>`.

> ⚠️ **Data Sharing:** Please do not copy or share the ISSM models provided in `/g/data/nf33/access-nri/CMWG_workshop_2025/sample_models/`. They are provided for use within this workshop only. Direct access to this directory is not necessary -- models are loaded via the workshop notebooks.

```text
© 2022 ACCESS-NRI and contributors. See the top-level COPYRIGHT file for details. 
SPDX-License-Identifier: Apache-2.0
```
