
# Writing a simple publisher and subscriber (C++)

In this project, I follow the tutorial to create a simple publisher and subscriber node in ROS (Robot Operating System). 

The ROS tutorial is the following:
[Writing a simple publisher and subscriber (C++)](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Writing-A-Simple-Cpp-Publisher-And-Subscriber.html)


## Prerequisites

Having ROS working directory installed and setup. You can follow the installation instructions [here](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html).

### Details
I used the following software versions:
 - ROS Humble
 - Ubuntu 22.04 (in a VM environment)

## Steps for reproducing the tutorial

1. From the ROS working directory, create the package with the name "cpp_pubsub"
```
ros2 pkg create --build-type ament_cmake cpp_pubsub
```
2. Download the files "publisher_member_function.cpp" and "subscriber_member_function.cpp" specified in the [tutorial](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Writing-A-Simple-Cpp-Publisher-And-Subscriber.html).
3. Update the "package.xml" for the description, maintainer and license.
4. Update the "CMakeLists.txt" for packages, executables, target dependencies and install targets.
5. Build the ROS working directory (to be able to find the package for the first time).
```
colcon build
```
6. Source the setup files
```
source install/setup.bash
```
7. Run the package node "talker".
```
ros2 run cpp_pubsub talker
```
8. In a different terminal, in the ROS working directory, source the setup files and run the package node "subscriber".
```
source install/setup.bash
ros2 run cpp_pubsub talker
```

## Output

When you run the two nodes "talker" and "listener", you will see the following outputs in the two different terminals.

### Node "talker" terminal output

```
[INFO] [1695923045.041721691] [minimal_publisher]: Publishing: 'Hello, world! 42'
[INFO] [1695923045.542948080] [minimal_publisher]: Publishing: 'Hello, world! 43'
[INFO] [1695923046.042858630] [minimal_publisher]: Publishing: 'Hello, world! 44'
[INFO] [1695923046.552194040] [minimal_publisher]: Publishing: 'Hello, world! 45'
[INFO] [1695923047.042264277] [minimal_publisher]: Publishing: 'Hello, world! 46'
[INFO] [1695923047.543484309] [minimal_publisher]: Publishing: 'Hello, world! 47'
[INFO] [1695923048.042480557] [minimal_publisher]: Publishing: 'Hello, world! 48'
[INFO] [1695923048.541982527] [minimal_publisher]: Publishing: 'Hello, world! 49'
```

### Node "listener" terminal output

```
[INFO] [1695923045.189962365] [minimal_subscriber]: I heard: 'Hello, world! 42'
[INFO] [1695923045.543275748] [minimal_subscriber]: I heard: 'Hello, world! 43'
[INFO] [1695923046.043285533] [minimal_subscriber]: I heard: 'Hello, world! 44'
[INFO] [1695923046.552648223] [minimal_subscriber]: I heard: 'Hello, world! 45'
[INFO] [1695923047.042770792] [minimal_subscriber]: I heard: 'Hello, world! 46'
[INFO] [1695923047.544103068] [minimal_subscriber]: I heard: 'Hello, world! 47'
[INFO] [1695923048.042873401] [minimal_subscriber]: I heard: 'Hello, world! 48'
[INFO] [1695923048.542611794] [minimal_subscriber]: I heard: 'Hello, world! 49'
```

## Source Material

I followed the tutorials from the ROS (Humble) documentation: 

[Writing a simple publisher and subscriber (C++)](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Writing-A-Simple-Cpp-Publisher-And-Subscriber.html)

## About Me

My name is Marissa Campa and I'm a Software Engineer. This is my [GitHub page](https://github.com/MarissaCampa).

You can reach me on &nbsp; [![Linkedin Badge](https://img.shields.io/badge/-marissa-blue?style=flat&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/marissa-campa/) &nbsp; or &nbsp; [![Gmail Badge](https://img.shields.io/badge/-marissag.campa@gmail.com-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:marissag.campa@gmail.com)](mailto:marissag.campa@gmail.com)
