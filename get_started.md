# Get started on Neptune project


## Download the dataset

Aqualoc dataset can be downloaded from here: https://seafile.lirmm.fr/d/79b03788f29148ca84e5/?p=%2F&mode=list


## Set up the environment

Since the dataset is in ros format, one would need to set up a python environment that is ros-compatible. 

A guidance can be found here: https://github.com/RoboStack/ros-noetic

But these are the only necessary steps:


```bash

conda create -n robostackenv python=3.8
conda activate robostackenv
# this adds the conda-forge channel to your persistent configuration in ~/.condarc
conda config --add channels conda-forge
# and the robostack channel
conda config --add channels robostack
# it's very much advised to use strict channel priority
conda config --set channel_priority strict

conda install ros-noetic-desktop

# optionally, install some compiler packages if you want to e.g. build packages in a catkin_ws - with conda:
conda install compilers cmake pkg-config make ninja catkin_tools

# reload environment to activate required scripts before running anything
# on Windows, please restart the Anaconda Prompt / Command Prompt!
conda deactivate
conda activate robostackenv

```

Also install jupyter notebook

```bash

conda activate robostackenv

pip install jupyter

python -m ipykernel install --user --name ros --display-name "Python (ros)"

```



## Visualize data

You can use `notebook/visualize_data.ipynb` to visualize Aqualoc data.