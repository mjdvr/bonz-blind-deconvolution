# bonz-blind-deconvolution

[placeholder]

## Topic
This code, contained in its entirety in the `main.ipynb` Jupyter notebook, is a presentation of different blind deconvolution techniques, consisting of both analytical solutions, as well as some machine learning algorithms. The user may feel free to modify the code to their liking, and experimentation (especially in the case of the machine learning algorithms) is encouraged.

Image deconvolution is a general term for different methods of removing noise, but mainly blur artifacts from images. This can be done in a variety of different ways, some of which are described and implemented in this repository's Jupyter notebook file. An effort has been made to make the code and its proper usage as accesible as possible.

Some rudimentary comments have been added to the code, both in the form of some markdown blocks, as well as some more involved explanations in the code blocks themselves as well, in the form of comments.

## Guide
Both markdown and codeblocks can be collapsed or expanded to the users liking, which is especially advised when focused on the machine learning section, where frequent kernel restarts may be useful. Collapsing the 'Analytical Methods' section allows for an easier overview of the required library imports, custom function definitions and base data loading cells.

Running the code cells in sequence results in a code cell output with some information printouts as well as some visual output, hopefully comprehensibly displaying the results of the corresponding deconvolution methods.

Tip: when investigating or experimenting with the machine learning methods, it is advised to restart the kernel when changing datasets or models. This allows the users machine to unload the memory allocated to previous datasets and models, which in some cases may prove exceedingly taxing on the users system.

Tip: when, in some cases, the users machine runs into issues as related to available memory (RAM or VRAM), smaller datasets or smaller batches in training may be used to alleviate some of the strain placed on the users system. This may then allow the user to perform training and predictions which otherwise would be too resource demanding, especially in the case of high-resolution images in the trainig and testing dataset.

Tip: as stated in the `main.ipynb` code file, the `opentensorboard.bat` simply contains some code to open the TensorBoard dashboard using the correct log-file directory. If the user feels wary of running this file even after inspection, the following code may be run from the terminal after logging some machine learning training sessions:
```
python -m tensorboard.main --logdir=logs/
```
In the code example above `--logdir=logs/` may be changed to the desired log-file directory as: `--logdir={directory}`, replacing `{directory}` with the directory of choice. In case the instructions are unclear, the user may resort to the official documentation of the TensorBoard at [tensorflow.org/tensorboard](https://www.tensorflow.org/tensorboard).

## Installation
To copy this repository for easy installation, the user is encouraged to install and use `git`, which may be acquired at [git-scm.com/downloads](https://git-scm.com/downloads). After installing this software, the user may then run the following command from their terminal in the desired location in their file structure:
```
git clone https://github.com/mjdvr/bonz-blind-deconvolution.git
```
For ease of use, and congruency with the rest of this README file, the user is furthermore encouraged to install and make use of the `conda` package manager for python, which may be installed following the instructions at [docs.conda.io](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html).

After succesfully installing both git, cloning this repository and installing conda, the user may then proceed to cloning the environment used in the development of the code. Note: to run this program in exactly the same manner as the original version, the user must install python version 3.9.15 with all required packages.

Assuming that the user has succesfully installed, and is familiar with the usage of, `conda`, the following command may be run to create an exact copy of the development environment required to run the code as supplied.

```
conda env create -f environment.yml
```

Note that the name of the environment is defined in the `environment.yml` as "`tf`". If another environment of the same name already exists, one may feel free to modify the name as states in the `.yml` file to any name of the users choosing.