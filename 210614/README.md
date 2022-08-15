# Assignment 1

The package `math` has been created which contains some nodes, a service node and a client node. Python is used to write the nodes using the `rospy` package.

The following scripts are there:
- `random_num.py`: Creates the node `random_num_generator`. Generates two random numbers and publishes them to two topics, `random_num_1` and `random_num_2`.
- `input_node.py`: Creates the node `input_node` which is subscribed to `random_num_1` and `random_num_2`. It publishes sum of the received numbers to `sum`.
- `output_node.py`: Creates the node `output_node` which is subscribed to `sum` and publishes the sum to `another_sum`.
- `add_two_numbers_service.py`: Creates a service named `add_two_numbers` through a node `add_two_numbers_server`.
- `add_two_numbers_client.py`: This script is called using `rosrun` to take the numbers being published by `random_num_1` and `random_num_2`, and calls the service to get their sum.

## Implentation

1. Source the setup file of ROS:
```source /opt/ros/noetic/setup.bash```
2. Run `catkin_make` to build the required files. This automatically initialises the directory as a catkin workspace.
3. Source the setup file for the workspace by `source devel/setup.bash`.
4. Run the package by `roslaunch math_package math_package.launch`.
