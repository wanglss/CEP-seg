# CEP-seg: Automatic Segmentation of Cartilage Endplate (CEP)

## About
This code performs automatic segmentation of L4-L5 and L5-S1 CEPs from **sagittal UTE** (**U**l**t**ra-short **E**cho Time) **spine MR images**<br /> 

Segmentation is performed via a U-net ([Ronneberger et al., 2015](https://arxiv.org/abs/1505.04597)) that was trained on UTE images and manual segmentations.

## Setup
### Installing a virtual environment
Set up a conda environment if you do not have all the packages/compatible versions (the list of dependencies is listed in `environment.yml`).<br />

**Create and activate virtual environment using conda**<br />
Set-up environment using conda (make sure you are in the `CEP-seg` code repository):
`conda env create -f environment.yml`<br />
The default name of the environment is `CEPseg`. Activate the environment with `source activate CEPseg`, and deactivate with `source deactivate`.<br />
Use `conda info CEPseg` to see more information about the environment and ensure that it was installed properly.

## Usage
### Open Jupyter Notebook
Make sure you are in the `CEP-seg` directory. 
```
source activate CEPseg
jupyter notebook
```
Open `prediction.ipynb`.

### Change User Inputs
Under  `User inputs`, change `level` ('l4l5inf', 'l4l5sup', 'l5s1inf', 'l5s1sup'), `img_path` (where MR images are stored) and `pred_path` (where masks will be created) as desired. 

### Create Masks
Run  `prediction.ipynb`. Masks will be created in the directory specified as  `pred_path`.
