# Development Environment Construction

## 1 Use Environment

myAGV pi 2023 is developed and used based on the Raspberry Pi system, so the content environment described in this chapter is based on the operating system environment on the Raspberry Pi.

## 2 Development Environment

In order to meet the diverse application needs of robots in different scenarios, we have adapted the robot for multiple programming languages. So far, we have adapted the following mainstream programming languages. If you find any of the following languages challenging, you can return to the [myBlockly](../5-BasicApplication/5.2-ApplicationUse/5.2.1-myblockly/README.md) section and use a visual programming language for development. However, we believe that you can use any of the following languages for development. Please make sure to strictly follow the instructions during the operation. Any missed steps may result in the corresponding language not running successfully. We wish you smooth and successful robot usage.

- [6.1 Python](../6-SDKDevelopment/6.1-ApplicationBasePython/README.md)<br>
Our robots support Python and the development of the Python API library has become increasingly complete.The basic motion control of MyAGV, including forward, backward, turning, and controlling the colorful light bar effects, can be achieved through relevant library functions in Python.

- [6.2 Robot Operating System 1 (ROS1)](../6-SDKDevelopment/6.2-ApplicationBaseROS1/6.2.1-ROS_Introduction.md)<br>
ROS is open-source and is a post operating system, or secondary operating system, used for robot control.ROS provides a powerful navigation stack, including SLAM (Simultaneous Localization and Mapping) technology and path planning algorithms. This enables developers to implement autonomous navigation, obstacle avoidance and path planning for mobile robots, enabling robots to move safely and efficiently in unknown environments.

----
[← Previous Chapter](../5-BasicApplication/README.md) | [Next Chapter →](../7-ExamplesRobotsUsing/README.md)