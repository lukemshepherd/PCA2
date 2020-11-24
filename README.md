# PCA2 
> Point Cloud Alignment with PCA


## Install

### Create conda environment (Recommended)

`git pull https://github.com/lukemshepherd/PCA_2.git`

`cd PCA_2`

`conda env create -f environment.yml`

`conda activate PCA_2`

### Install from PyPi

`pip install PCA_2`

### Or: Install from GitHub

`cd PCA_2`

`pip install -e .`

## How to use

Fill me in please! Don't forget code examples:

#### Set custom filter level (optional)

```
bone.filter_level = 0.1
```

#### Set custom colour for bone (optional)

```
tibia_f1.default_color = (0.8, 0.3, 0)
```

## Load the data that you want to use

```
tibia_f2 = bone.from_matlab_path(matlab_file='data/tibia_f2.mat')

tibia_f1 = bone.from_matlab_path(matlab_file='data/phantom_tibia_f1.mat')
```

## Rotate the bone

```
voxel_rotate(tibia_f1, tibia_f2)
```

## Plotting the rotation

Plotting with mayavi is very similar to matplotplib where you build a scene and call it with show()

You can plot bones by calling the .plot() method and then mlab.show()

```
tibia_f1.plot()
tibia_f2.plot()
mlab.show()
```

<img src="docs/images/aligned.png" width="80%">

## Table of angles

```
df_angles(tibia_f1, tibia_f2, name='tibia')
```
