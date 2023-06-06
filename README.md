# er_upper_controller
1.
sudo udevadm control --reload-rules
Failed to send reload request: No such file or directory
A：sudo service udev restart

2. change kernel
https://github.com/microsoft/WSL/issues/7747

3.usbipd: error: Failed to attach device with busid '1-1'.
A:usbipd bind --busid 1-3 --force

4.Error: libusb_open() failed with LIBUSB_ERROR_ACCESS
Error: open failed
A:sudo chmod 666 /dev/ttyACM0
sudo udevadm control --reload-rules


rosrun rosserial_python serial_node.py _port:=/dev/ttyACM0 _baud:=9600
SerialClient.py 330

https://medium.com/swlh/7-simple-steps-to-create-and-build-our-first-ros-package-7e3080d36faa

http://wiki.ros.org/joy/Tutorials/ConfiguringALinuxJoystick
