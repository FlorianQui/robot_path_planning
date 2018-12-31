# ROBOT PATH PLANNING

### Requirements

- Python installed
- Matplotlib module installed (pip install matplotlib)

---

## Path planner

In order to move in a space, a robot needs planner that control movements and path. This is called Navigation. We can split this definition in two parts, the global planner and the local planner.
This navigation handles the dynamic map, and also control both motors (differential drive robot).

### Global planner

This parts handles the map server and also some algorithms that search for best path from point A to point B.
It contains, for example, an A* algorithm.
A* is the most popular algorithm used for this application. It takes the begin and end point, and find the shortest path using a costmap calculation. Then it returns a list of point that the robot should go. These points are send to the local planner which will drive the robot.

### Local planner

This part can control robot with velocity vector (linear and angular). First of all, the local planner receives a point to go by the global planner. It calculates the trajectory that the robot should take, and return the volicty command to the base controller. We could refer to differential drive kinematic for more details.

## Run an example algorithm

``` python path_planning.py ```

Then, you should see the results.

A video that explained the path planner is [available](https://www.youtube.com/watch?v=Py5hc2e-1P4&feature=youtu.be&fbclid=IwAR1rhgxYFMu62zpzVrZ7MOx7avrtlYMkAouFs4nl09Y_n_gcna1DN7q2B2g)
