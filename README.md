# Python-course

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/jboulanger/Python-course/HEAD)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://mybinder.org/v2/gh/jboulanger/)

This course introduces the essential steps of setting up an image analysis workflow for your research. It covers the topics of microscopy data loading, processing and quantification. It illustrates how to extract relevant information from an image using common Python packages. 

To run the notebook on the server, use either the badges above or copy and paste the following link into the browser: 

http://10.91.193.124/hub/user-redirect/git-pull?repo=https://github.com/jboulanger/Python-course&branch=main&app=lab


## Installation

### Using miniconda
Install first [miniconda](https://docs.anaconda.com/free/miniconda/miniconda-install/).

On Windows with cuda support:
```bash
conda create -f envs/environment-win.yml
conda activate imaging-python-course
```

On Linux with cuda support:
```bash
conda create -f envs/environment-linux.yml
conda activate imaging-python-course
```

On MacOS:
```bash
conda create -f envs/environment-macos.yml
conda activate imaging-python-course
```

### Using micromamba

```bash
# install micromamba
"${SHELL}" <(curl -L micro.mamba.pm/install.sh)
# reload the shell
${SHELL}
# create an environment
micromamba -qy create -f environment.yml
# activate the environment 
micromamba activate imaging-python-course
# start the notebook
jupyter lab 
```