# 开发环境配置

## 1 使用环境

myAGV Jetson Nano 2023具有内置的开发环境，因此本章中描述的内容环境是基于 myAGV Jetson Nano 2023 上的操作系统环境。

## 2 开发环境

为了满足机器人在不同场景下的多样化应用需求，我们对机器人进行了多种编程语言的适配。到目前为止，我们已经适配了以下主流编程语言。如果您觉得以下语言具有挑战性，可以返回到 [myBlockly](../5-BasicApplication/5.2-ApplicationUse/5.2.1-myblockly/jetsonnano/README.md) 部分，并使用可视化编程语言进行开发。不过，我们认为您可以使用以下任何一种语言进行开发。请务必严格按照说明进行操作。任何遗漏的步骤都可能导致相应语言无法成功运行。祝您顺利使用机器人。

**跳转到各部分：**

- [Python](../6-SDKDevelopment/6.1-ApplicationBasePython/README.md)<br>
  我们的机器人支持 Python，Python API 库的开发也日趋完善。MyAGV 的基本运动控制，包括前进、后退、转弯和控制彩色光条效果，都可以通过 Python 中的相关库函数来实现。

- [Robot Operating System 1 (ROS1)](../6-SDKDevelopment/6.2-ApplicationBaseROS1/6.2.1-ROS_Introduction.md)<br>
  ROS 是开放源码的，是用于机器人控制的后置操作系统或辅助操作系统。ROS 提供强大的导航堆栈，包括 SLAM（同步定位和映射）技术和路径规划算法。这使开发人员能够为移动机器人实现自主导航、避障和路径规划，使机器人能够在未知环境中安全高效地移动。

---

[← 上一章](../5-BasicApplication/README.md) | [下一章 →](../7-ExamplesRobotsUsing/README.md)
