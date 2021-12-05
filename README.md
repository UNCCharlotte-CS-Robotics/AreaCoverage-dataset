# AreaCoverage-dataset
The repository contains a collection of datasets for the Area Coverage problem (also known as the Coverage Path Planning problem).

It also contains the results using our algorithm for the Area Coverage problem. The paper describing the algorithm has been submitted to IEEE RA-L and is currently under final review.

> Saurav Agarwal and Srinivas Akella,
> “Area Coverage Problem with Multiple Capacity-Constrained Robots,”
> IEEE Robotics and Automation Letters, 2021 (under review).

### Description of common files:

- `outer_polygon`: Points for the outer polygon.
- `holes`: Points for the hole (obstacle) polygons.
- `robot_polygon`: Points describing the robot.
- `graph.png:` Environment and service tracks.
- `mem_<description>_route.png`: Routes generated using our algorithm.
- `mem_<description>_route_data<route_nuumber>`: File containing route using our algorithm. The first two columns are the coordinates, and the last column states whether the travel to the point is servicing or deadheading.

# Description of the Datasets

### `VM25` dataset

A dataset of 25 indoor environments for coverage using ground robots. The dataset was provided by Isaac Vandermeulen. The dataset is part of the following paper:

> I. Vandermeulen, R. Groß, and A. Kolling,
> “Turn-minimizing multirobot coverage,”
> IEEE International Conference on Robotics and Automation (ICRA), 2019, pp. 1014–1020.

> Vandermeulen, Isaac   (2020) 
> [Coverage & cooperation: Completing complex tasks as quickly as possible using teams of robots.](https://etheses.whiterose.ac.uk/27452/)
> PhD thesis, University of Sheffield.  

Scale: 1 unit = .1 m

- `env_<num>.wkt`: The original environment data in WKT format as given by Isaac Vandermeulen.

- `mem_r<num>`: Folder containing our results for `<num`> robots.

  

### `AC300` dataset

A dataset of 300 outdoor environments using aerial robots. The dataset is part of the installation from the source code available at https://github.com/ethz-asl/polygon_coverage_planning. The environments have been converted to our format. The original dataset can be obtained from https://polybox.ethz.ch/index.php/s/7J5HPRR6lM22TnK/download. The dataset is part of the following paper:

> Bähnemann, Rik, et al.,
> "Revisiting boustrophedon coverage path planning as a generalized traveling salesman problem,"
> Field and Service Robotics. Springer, Singapore, 2021.

The dataset contains 300 environments with 1--15 holes (obstacles) derived from buildings. The environments are named `AC<#holes>_<#num>`. 

Scale: 1 unit = 1 m

- `mem_inf`: Our solution with a single robot.

- `mem_1200`: Our solution with robots with 1200 s as capacity.

  

# License

The datasets are owned by the respective authors. However, the results were generated using our algorithms. The results should be used only for the purpose of benchmarking.
