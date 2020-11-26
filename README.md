# PCA2 
> Point Cloud Alignment with PCA


## Install

### Create conda environment *(Recommended)*

`git pull https://github.com/lukemshepherd/PCA_2.git`

`conda env create -f environment.yml`

`conda activate PCA2`

## With pip


`pip install PCA2`

## Editable install

`git pull https://github.com/lukemshepherd/PCA_2.git`

`pip install -e .`

## How to use

```
from PCA2.core import *
from mayavi import mlab # for calling the plots
```

#### *Set custom filter level (optional)*

```
bone.filter_level = 0.3
```

## Load the data that you want to use

```
tibia_f2 = bone.from_matlab_path(matlab_file='data/tibia_f2.mat')
tibia_f1 = bone.from_matlab_path(matlab_file='data/phantom_tibia_f1.mat')
```

#### *Set custom colour for bone (optional)*

```
tibia_f1.default_color = (0.8, 0.3, 0)
```

## Rotate the bone

```
rotate(tibia_f1, tibia_f2)
```

    0.17471680699860007 no invert
    0.5819453559235347 no invert
    3.906788298496456e-16 no invert


## Plotting the rotation

Plotting with mayavi is very similar to matplotplib where you build a scene and call it with show()

You can plot bones by calling the `.plot()` method and then `mlab.show()`

```
# tibia_f1.plot()
# tibia_f2.plot()
# mlab.show()
```

<div> 
    <img src="docs/images/aligned.png" width="100%"> 
</div>

## Table of angles

```
df_angles(tibia_f1, tibia_f2, name='tibia')
```

    1.7785780651003298e-16 no invert
    1.2719202621569003e-16 no invert
    3.906788298496456e-16 no invert





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
      <td>1.778578e-16</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>tibia f1: pc2</th>
      <td>NaN</td>
      <td>1.271920e-16</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>tibia f1: pc3</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>3.906788e-16</td>
    </tr>
  </tbody>
</table>
</div>


