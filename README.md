## create_2d_collision_maps

A simple package to create ROS collision objects from a black/white image or a txt file.

From image:

<p float="left">
  <img src="/.doc/maze.png" width="25%" />
  <img src="/.doc/rviz_bitmap.png" width="35%" /> 
</p>

From text:
<p float="left">
  <img src="/.doc/maze_10.png" width="20%" />
  <img src="/.doc/maze_txt.png" width="35%" /> 
</p>

### Usage

To create the map from an image, e.g. ```input/images/maze.png```:
```
cd scripts
python3 create_2d_map_from_image.py
```
To create the map from a txt file , e.g. ```input/text/test.txt```:
```
cd scripts
python3 create_2d_map_from_txt.py
```

### How to upload the objects to _MoveIt!_

The scripts output two YAML files, one contains the description of the collision boxes and one contains the position of the boxes in the Cartesian space.
These two files are used by the package [object_loader](https://github.com/CNR-STIIMA-IRAS/object_loader) to load the boxes in the MoveIt! planning scene.
An example can be found [here](https://github.com/JRL-CARI-CNR-UNIBS/planar_cartesian_robot/tree/master/planar_cartesian_robot_benchmark).

### Options

Options on the size of the scenarios (in meters) and resolution of the collision boxes can be given directly in the scripts, along with the input and output filenames.

### Contacts

Marco Faroni (marco.faroni \[at\] polimit)
