# **深度相机**

==============================================

##环境依赖

###硬件

- IntelRealSense-D435i相机

###软件

- ROS Melodic

- RealSense

- C++

- Python

#####我们在Ubuntu18.04系统上完成了对深度相机的调试运行，把深度图和rgb图匹配起来，进而可以从一张图像上面读取更多的信息。

##部署步骤

###1. 安装ROS Melodic

```

http://wiki.ros.org/melodic/Installation/Ubuntu

```

###2. 配置RealSense环境

```

https://github.com/IntelRealSense/librealsense

```

###3. 创建工作空间

```

mkdir -p ~/RoboRTS_wsc

cd ~/RoboRTS_wsc

catkin_init_workspace

cd ~/RoboRTS_ws/

catkin_make

source develtup.bash

```

###4. 将功能包放入工作空间的src文件夹并编译

```

cd ~/RoboRTS_wsc

git clone https://github.com/IntelRealSense/realsense-ros

git clone https://github.com/pal-robotics/ddynamic_reconfigure/tree/kinetic-devel

cd ~/RoboRTS_ws

catkin_make

```

##启动相机

```
roalaunch realsense_camera rs_camera.launch

```

##在ROS中运行
```
roslaunch roborts_bringup ws.launch
```
可以在ROS中看到深度相机检测到的
