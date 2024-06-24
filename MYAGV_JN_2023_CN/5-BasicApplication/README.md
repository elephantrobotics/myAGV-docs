# 基本应用

| <img src="../resources/5-BasicApplication/README/danger.png" alt="img-1" width="600" height=“auto” /> | 本章主要解释产品的基本功能用法和基本软件的使用。本章至关重要，应仔细阅读。在实际应用机器人之前，请确保正确理解所述操作。 |
| ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |

## 章节摘要

### **5.1-系统说明**

在使用系统之前，你需要掌握基本的 Linux 知识，如文件管理和命令行操作。在网络配置方面，要了解访问系统的远程连接方法（如 SSH）。闪存镜像时，选择正确的文件和工具，正确设置参数，确保系统正常运行。

- [定制的机器人操作系统](5.1-SystemInstructionManual.md)<br>
  myAGV 2023 系统不仅内置了 ROS 和 Python 等环境，还配备了 VSCode、VNC 和 SSH 等机器人开发软件。
  无需复杂的配置。它还提供自动更新软件，并支持一键更新相应的开发环境。

### **5.2-应用用途**

针对 myAGV 系列产品，我们推出了专为机器人应用和维护设计的软件，供用户使用。其中，myBlockly 和 myStudio 是用户使用机器人的必备工具。本章将详细介绍这三款软件的使用方法。

- [myBlockly](5.2-ApplicationUse/5.2.1-myblockly/jetsonnano/README.md)<br>
  myBlockly 是一款完全可视化的模块化编程软件，是一种图形化编程语言。myBlockly 界面简洁，编程功能全面。它的可视化编程方法适合初次接触机器人产品的用户。

- [myStudio](5.2-ApplicationUse/5.2.2-mystudio/jetsonnano/README.md)<br>
  myStudio 是使用 myAGV 等机器人的一站式平台。用户可以根据自己的使用场景选择不同的固件并下载，同时还可以在线学习相关教材和浏览教学视频，非常方便。

- [myagv_UI](5.2-ApplicationUse/5.2.3-myagv_UI/user_manual.md)<br>
  MyAGV_UI 软件专为与 MyAGV 产品配套使用而设计。它通过图形界面降低了用户的使用门槛，只需单击按钮即可快速了解 MyAGV。
  它可以一键启动 MyAGV 传感器通信和 SLAM，一键更换后部 LED 灯，还包括测试电机和摄像头的功能。

### **5.3-固件使用**

为了确保您的 myagv 始终处于最佳状态，我们不断改进和更新固件。固件更新是确保设备功能、性能和安全性的关键步骤之一。通过及时更新固件，我们可以修复已知问题、改进功能、提高性能，并确保 myagv 的稳定性和安全性。

- [固件更新信息](5.3-FirmwareUse/5.3.1-FirmwareUpdateInfo.md)<br>
  固件表信息，描述固件更改后的性能改进或优势。

- [刻录固件操作](5.3-FirmwareUse/5.3.2-HowToBurnFirmware.md)<br>
  本章介绍如何使用 mystudio 软件为 myagv 刻录固件代码。

---

[← 上一章](../4-FirstInstallAndUse/README.md) | [下一章 →](../6-SDKDevelopment/README.md)
