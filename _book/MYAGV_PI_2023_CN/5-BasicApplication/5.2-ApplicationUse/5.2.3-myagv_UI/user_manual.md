# myAgv 软件用户手册

## 运行程序

1. 克隆 github 的版本库：  
   `https://github.com/elephantrobotics/AGV_UI.git`
2. 切换到分支 **Visualize_OP** :  
   `git checkout Visualize_OP`
3. 安装所有依赖项：  
   `pip install -r requirements.txt`
4. 在终端中执行命令：  
   `python operations.py`

![Softeware Page](../../../resources/5-BasicApplication/5.2/5.2.3/software_page_en.png "Software Page")

## 1. 切换语言

选择中文和英文，切换相应语言。

![Language Choose](../../../resources/5-BasicApplication/5.2/5.2.3/language_choices_en.png "Choose Language")

## 2. 激光雷达

![Radar Open](../../../resources/5-BasicApplication/5.2/5.2.3/radar_open_en.png "Open Radar")

![Radar Close](../../../resources/5-BasicApplication/5.2/5.2.3/radar_close_en.png "Close Radar")

- 点击按钮打开雷达。按钮变为红色，文字显示 "off"。
- myAgv 的雷达开始旋转。
- 桌面上会出现一个新终端，表明雷达已成功打开。  
   ![Radar Open](../../../resources/5-BasicApplication/5.2/5.2.3/radar_open_terminal.png "Open Radar")

**限制：**

- 雷达开启：可使用基本控制、制图、导航和地图保存功能。
- 雷达关闭：
  - 可使用 LED 灯光控制和测试功能
  - 在关闭雷达之前，您需要确保已关闭基本控制、映射和导航功能。

## 3. 基本控制

> 通过键盘和手柄控制机器移动有两种方法。

![Basic Control](../../../resources/5-BasicApplication/5.2/5.2.3/basic_control_en.png "Basic Control")

**准备：** 在开启基本控制功能之前，必须先开启雷达。如果雷达未打开，则会弹出提示框，显示 "Radar is not turned on"。

单击下拉框选择所需的控制方法，然后单击左侧的按钮打开。此时，桌面上会打开一个新的终端。

### 3.1 键盘控制

![Keyboard terminal](../../../resources/5-BasicApplication/5.2/5.2.3/keyboard_terminal.png "Keyboard terminal")

**方向键**

| 按键 | 路线指引   |
| :--- | :--------- |
| i    | 转发       |
| ，   | 后退       |
| j    | 向左移动   |
| l    | 向右移动   |
| u    | 逆时针旋转 |
| o    | 顺时针旋转 |
| k    | 停止       |

### 3.2 手柄控制

#### 2.1 手柄-字母型

![JoyStick Alphabet](../../../resources/5-BasicApplication/5.2/5.2.3/joystick_terminal.jpg "JoyStick Alphabet")

> There are 7 buttons on the handle to control the car movement, as shown in the picture, 1~4 control the car forward and backward and left and right movement, 5 control the car counterclockwise rotation, 6 control the car clockwise rotation, 7 is the stop button.

![JoyStick Alphabet](../../../resources/5-BasicApplication/5.2/5.2.3/joystick_alphabet.jpg)

---

#### 2.2 Handle-Digital type

![JoyStick Number](../../../resources/5-BasicApplication/5.2/5.2.3/joystick_terminal.jpg "JoyStick Number")

> There are 7 buttons on the handle to control the car movement, as shown in the picture, 1~4 control the car forward and backward and left and right movement, 5 control the car counterclockwise rotation, 6 control the car clockwise rotation, 7 is the stop button.

![JoyStick Number](../../../resources/5-BasicApplication/5.2/5.2.3/joystick_number.png "JoyStick Number")

## 4. Map and Navigation

![Map Navigation](../../../resources/5-BasicApplication/5.2/5.2.3/map_navi_en.png "Map and navigation")

**Preconditions：**

- Open radar
- Open keyboard control

If it is not opened, a prompt box will pop up to prompt for the items that need to be opened.

### 4.1 Build Map

**There are two way for building map by Gmapping and Cartographer.**

![Build Map](../../../resources/5-BasicApplication/5.2/5.2.3/build_map_en.png "Build Map")

#### Gmapping

Click the drop-down box to select the Gmapping mapping method, and click the "Open Mapping" button to start mapping.

- Desktop display rviz interface.
- Select the opened keyboard terminal and use the keyboard to control the car. The rviz space will build the map as the car moves. The trajectory is shown in the figure: ![Gmapping Map](../../../resources/5-BasicApplication/5.2/5.2.3/gmapping_rviz.png "Gmapping Map")

#### Cartographer

Click the drop-down box to select the Gmapping mapping method, and click the "Open Mapping" button to start mapping.

- Click the button and it will open a new terminal. If the terminal keeps scrolling the output data, the cartographer build file is successfully opened, and the terminal displays the following status: ![Cartographer Map](../../../resources/5-BasicApplication/5.2/5.2.3/cartographer_terminal.png)
- When the code runs successfully, rviz will be opened, and the map and lidar information will be displayed in rviz, and the red arrow is the direction of the car. The interface is shown in the figure. ![Cartographer Map](../../../resources/5-BasicApplication/5.2/5.2.3/cartograph_rviz.jpg)
- Select the opened keyboard terminal and use the keyboard to control the car. The rviz space will build the map as the car moves. The trajectory is shown in the figure: ![Cartographer Track](../../../resources/5-BasicApplication/5.2/5.2.3/catograph_rviz2.jpg)

**Limit:** Navigation cannot be used after mapping is turned on; if you need to use the navigation function, please turn off mapping first.

#### 4.1.1 Save Map

![Save Map](../../../resources/5-BasicApplication/5.2/5.2.3/save_map_en.png "Save Map")

Click the "Save Map" button, and a new terminal will appear on the desktop to display the saved map information, as shown in the figure. The red circled part in the picture is the saved map file:

![Save map terminal](../../../resources/5-BasicApplication/5.2/5.2.3/save_map.png)

**The default save path is in the software running directory.**

### 4.2 Navigation

![Map Navigation](../../../resources/5-BasicApplication/5.2/5.2.3/navagation_en.png "Map Navigation")

### Preconditions

#### 1、Copy and paste the saved map file into this path

> /home/ubuntu/myagv_ros/src/myagv_navigation/map/

![File Manager](../../../resources/5-BasicApplication/5.2/5.2.3/file_2.png)

#### 2、modify the launch file

1. Click to open Visual Studio Code in the top left corner to open the code editor.  
   ![vscode Icon](../../../resources/5-BasicApplication/5.2/5.2.3/vscode_icon.png)

2. Open the navigation_active.launch file in /home/ubuntu/myagv_ros/src/myagv_navigation/launch/ path.  
   ![modify launchfile1](../../../resources/5-BasicApplication/5.2/5.2.3/modify_launch1.png)

3、Replace the myroom2.yaml in line 5 with our own map file name map.yaml.  
![modify launch file2](../../../resources/5-BasicApplication/5.2/5.2.3/modify_launch2.png)

4、Save the modified file and exit (VScode is more memory intensive when running, it is recommended to close VScode after modifying the code, otherwise the running carsystem will be very laggy, you can also use vim and other lightweight editors.)

**After following the above steps, click the corresponding button according to the desired navigation method.**  
**A Rviz simulation window will open. Note: It is best to place the initial position of the car at the starting position of the car when we build the map.**

### Adjust

If the car on the Rviz interface does not correspond to the actual car, click "2D Pose Estimate" on the top toolbar to adjust, so that the car on the Rviz interface and the realized car can correspond, and navigate after adjustment.

![Run launch File1](../../../resources/5-BasicApplication/5.2/5.2.3/run_launch1.jpg)

1、Click on "2D Nav Goal" in the top toolbar.

![Run launch File3](../../../resources/5-BasicApplication/5.2/5.2.3/run_launch3.png)

2、Click on the point we want to reach on the map, the carwill start towards the target point, and you can also see in the rviz a planned path of the carbetween the starting point and the target point, the carwill move along the route to the target point.

![Run launch File4](../../../resources/5-BasicApplication/5.2/5.2.3/run_launch4.jpg)

**Limit:**

- You can only choose one of the two methods: navigation and 3D navigation. If you need to use another one, please close the current one.
- Mapping cannot be opened after the navigation is turned on. If you need to build a map, please close the navigation.

## 5、 LED light Control

![LED Light](../../../resources/5-BasicApplication/5.2/5.2.3/led_light_en.png "LED Light")

**Preconditions：** Close radar
Use the disc to select the light color, and drag the slider to change the brightness of the light color. The right side of the picture shows the corresponding HEX and RGB values.

## 6、 Testing FUnction

![Testing Function](../../../resources/5-BasicApplication/5.2/5.2.3/testing_en.png "Testing Function")
**Limit：During the test, the radar, basic control, and map navigation modules cannot be used.**

### 6.1 Motor

**Functions：** Check whether the motor can operate normally  
**Running：**

- Select the 'Motor' from the drop-down box and click to start testing
- In this process, it is recommended to place myAgv on the ground for testing; during the process, it will go forward and backward for 4 seconds each, translate left and right for 4 seconds each, and rotate left and right for 8 seconds each.
- After all the above steps are executed, the detection is completed.

### 6.2 LED light

**Functions：** Check whether the Led light can operate normally  
**Running：**

- Select the 'LED' from the drop-down box and click to start testing
- Switch the red, orange, yellow, green, blue, and purple colors in sequence. If the color switching can be observed normally, the LED light is used normally.
- The display time of each color is 1s. After all colors are displayed normally, the detection is completed.

### 6.3 3D Camera

**Functions：** Check whether the 3D camera can operate normally  
**Running：**

- Select the '3D Camera' from the drop-down box and click to start testing
- A new window pops up to display the image captured by the camera; if the image can be displayed, the camera is operating normally.
- The screen is displayed for about 5 seconds, and then the window screen is automatically closed. Testing completed.

### 6.4 2D Camera

**Functions：** Check whether the 2D camera can operate normally  
**Running：**

- Select the '2D Camera' from the drop-down box and click to start testing
- A new window pops up to display the image captured by the camera; if the image can be displayed, the camera is operating normally.
- The screen is displayed for about 5 seconds, and then the window screen is automatically closed. Testing completed.

### 6.5 Pump

**Functions：** Check whether the pump can operate normally  
**Running：**

- Select the 'Pump' from the drop-down box and click to start testing
- The suction pump is turned on and turns off automatically after running for 4 seconds; at this time the detection is completed

### 6.6 Restore

![Restore Function](../../../resources/5-BasicApplication/5.2/5.2.3/restore_en.png "Restore FUnction")  
**Functions：** Return the stalled motor to normal operation.
**Running：** Clicked the button as the picture shows above.

- Select the 'Pump' from the drop-down box and click to start testing
- The suction pump is turned on and turns off automatically after running for 4 seconds; at this time the detection is completed

## 7. Log Area

![Log Area](../../../resources/5-BasicApplication/5.2/5.2.3/log_area_en.png "Log Area")

All the above operations will be displayed in the log area. Click the "Clear Button" on the right side of the icon to clear the current content.

## 8. Status Detection

![Status Detecting](../../../resources/5-BasicApplication/5.2/5.2.3/status_add_en.png "Status Information")

**1、 IP Address:** Show current IP address  
**2、 Battery Information:** Display the currently connected battery information

- When connected, the green light and the corresponding power and voltage are displayed; when not connected, the display is gray and the value is 0.

**3、 Motor Current:** Shows whether there is current flowing through and the electricity value

- When the motor is in motion and there is current flowing through it, the motor will light up green and the page will display the current value; otherwise it will be gray.

**4、 Radar Detection:** Shows whether radar is on

- When the radar button is turned on, the green light turns on; when the radar button is turned off, the light turns off and turns gray.

---

[← Previous Page](../../README.md) | [Next Chapter →](../../5.3-FirmwareUse/5.3.1-FirmwareUpdateInfo.md)
