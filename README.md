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

## Installation
Note: to run this program in exactly the same manner as the original version, the user must install python version 3.9.15 with all required packages.

Assuming an at least slightly experienced target audience, the environment used can easily be installed using the following command:

```
conda env create -f environment.yml
```

Note that the name of the environment is defined in the `environment.yml` as "`tf`". If another environment of the same name already exists, one may feel free to modify the name as states in the `.yml` file to any name of the users choosing.