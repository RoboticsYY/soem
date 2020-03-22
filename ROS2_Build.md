# ROS2_Build

## Install Dependencies

Follow the steps in the link to install [ROS2 Eloquent](https://index.ros.org/doc/ros2/Installation/Eloquent/) on Ubuntu 18.04.

## Build

```bash
mkdir -p ws_ros2/src && cd ws_ros2/src
git clone https://github.com/RoboticsYY/soem.git
cd ..
colcon build --symlink-install
```

## Usage

To use `soem` in your ROS package add the following to your `package.xml`and `CMakeLists.txt`, respectively.

In your `package.xml` add:

```xml
  <build_depend>soem</build_depend>
  <exec_depend>soem</exec_depend>
```

and in your `CMakeLists.txt`, add it to `find_package` as shown:

```CMake
find_package(soem REQUIRED)
```
