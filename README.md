# test_tm_driver
tm_driver test without using ROS

## Installation
1. create a folder ```test_rm_dreiver``` for this test code
2. copy the *CMakeLists.txt* and *test_tm_driver.cpp* to ```test_rm_dreiver/```
3. copy the ```src``` folder in ```techman_robot/tm_driver/``` to ```test_rm_dreiver/```
4. copy the ```tm_driver``` folder in ```techman_robot/tm_driver/include/``` to ```test_rm_dreiver/src/```
5. ```$ cmake .``` and ```$ make``` to build this test code

## Usage
To start this test program:
```
$ ./test_tm_driver 192.168.0.10
```
**During the execution**
* input ```start``` to connect to techman robot
* input ```halt``` to disconnect to techman robot
* input ```quit``` to exit the program

**If the connection is success**
* input ```datart``` to print all robot_state_rt once
* input ```show``` to print robot_state cyclic, type ```1, 2, ..., 9, 0``` to change data type, type ```q``` to leave the loop
* input ```clear``` to clear terminal.
* input ```stop``` to stop immediately. **(NOTE: this command need ```run``` to restart robot)**

## Motion Commands

### Absolute Joint position 
- The input joint position argument is **radius**
```
movjabs j1 j2 j3 j4 j5 j6
```

### Reference Joint position
- The input joint position argument is **radius**
- This command will set joint psition based on last position.
```
movjrel j1 j2 j3 j4 j5 j6
```



### Absolute TCP Cartesian position
- The input cartesian position argument is **meter**
```
movlabs x y z a b c
```

TODO: the usage of all robot commands...
