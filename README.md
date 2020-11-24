# PCA2 
> Point Cloud Alignment with PCA


## Install

### Create conda environment (Recommended)

`git pull https://github.com/lukemshepherd/PCA_2.git`

`cd PCA2`

`conda env create -f environment.yml`

`conda activate PCA2`

### Install from PyPi

`pip install PCA2`

### Or: Install from GitHub

`cd PCA2`

`pip install -e .`

## How to use

Fill me in please! Don't forget code examples:

#### Set custom filter level (optional)

```
bone.filter_level = 0.2
```

## Load the data that you want to use

```
tibia_f2 = bone.from_matlab_path(matlab_file='data/tibia_f2.mat')
tibia_f1 = bone.from_matlab_path(matlab_file='data/phantom_tibia_f1.mat')
```

#### Set custom colour for bone (optional)

```
tibia_f1.default_color = (0.8, 0.3, 0)
```

## Rotate the bone

```
rotate(tibia_f1, tibia_f2)
```

    0.17458532149354633 no invert
    0.5815521223920518 no invert
    1.9141791241147516e-16 no invert


## Plotting the rotation

Plotting with mayavi is very similar to matplotplib where you build a scene and call it with show()

You can plot bones by calling the .plot() method and then mlab.show()

```
tibia_f1.plot()
tibia_f2.plot()
mlab.show()
```

<div> 
    <img src="docs/images/aligned.png" width="100%"> 
</div>

## Table of angles

```
df_angles(tibia_f1, tibia_f2, name='tibia')
```

    0.6019718433476905 no invert
    2.6184557666721346e-16 no invert
    0.6019718433476903 no invert





<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>tibia f2: pc1</th>
      <th>tibia f2: pc2</th>
      <th>tibia f2: pc3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>tibia f1: pc1</th>
      <td>0.601972</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>tibia f1: pc2</th>
      <td>NaN</td>
      <td>2.618456e-16</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>tibia f1: pc3</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.601972</td>
    </tr>
  </tbody>
</table>
</div>


