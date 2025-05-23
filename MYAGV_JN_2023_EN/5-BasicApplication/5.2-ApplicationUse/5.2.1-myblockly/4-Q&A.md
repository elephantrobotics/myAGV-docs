# 10 Q&A

This chapter lists common problems with using myBlockly to control robotic arms for reference.

**Q1: When running myBlockly, an error message `ModuleNotFoundError: No module named 'pymycobot'`**

A: This is caused by not installing the pymycobot library when setting up the Python environment. To install the pymycobot library, you need to open the terminal (Win key + R key), enter: `pip install pymycobot --upgrade --user`, and click the Enter key to see Successfully installed pymycobot.

<img src="../../../resources/5-BasicApplication/5.2/5.2.1/img/Q&A/pymycobotinstallation.jpg" style="zoom: 50%;" />



**Q2: The robot arm is unresponsive because the `sleep` method module is not added**

A: The program to operate the robot arm takes time to complete, so after an action, a `sleep' module needs to be connected to give the robot arm time to move before proceeding with the next movement (the time required depends on the situation, the machine The default setting of the arm is to run myBlockly with a minimum sleep time of no less than 0.5s), otherwise the robotic arm will not be able to achieve the ideal movement.



**Q3: The `Run` button in the upper right corner cannot be clicked and is gray-green. **

A: The new version of myBlockly adds the function of detecting the serial communication of the robot arm. If the robot arm is currently connected to the computer, you need to check:

(1) Whether there is a background program occupying the serial port of the robotic arm;

(2) Whether the toolbar under the red arrow on the right is closed. If it is open, it needs to be closed manually.



**Q4: Why do I get a bunch of errors after running the program? **

A: You need to confirm some information before running the program:

(1) Please confirm that your robot serial port number and baud rate are correct.

 How to check the serial port number:

* On Windows systems, find the device manager and check the port.
   If the port (COM and LPT) displays USB-Enhanced-SERIAL CH9102, it is a CP34X chip.
   If the port (COM and LPT) shows Silicon Labs CP210x USB to UART Bridge, it is the CP210X chip. The port corresponding to these two names is the serial port of your robot arm.
* Open the terminal on Linux system, enter ls/dev/tty* and press Enter. What is displayed is the serial number of the robot arm. Among them AMA0 or USB0
   etc. is the serial number of your robotic arm.
* Open the terminal on Mac system, enter cd/dev/ and press Enter, then run ls -al tty to find it, such as /dev/tty.usbserial-10.

(2) Please confirm that the baud rate is correct. `myAGV Jetson Nano 2023 ` baud rate is `115200`.

(3) Please confirm that the model, serial port number and baud rate in the blue box are consistent with those in the small toolbar on the right, and match the robotic arm.



**Q5: Error MyCobot._int_() takes 2 positional arguments but 3 were given.**

A: This error will appear in the old version of myBlockly because the versions of myBlockly and pymycobot are not compatible. Just update the versions of myBlockly and pymycobot driver libraries.



**Q6: The result of running the program shows child process exited with code 1**
A: This is not an error. All programs return the binary number 1 after running. It means everything has been successfully run.

---

 [← Previous Page](./3-interface_description.md) | [Next Page →](./5-api.md)
