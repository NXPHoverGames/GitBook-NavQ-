# Table of contents

* [NavQPlus](README.md)
  * [Kit Contents](readme/kit-contents.md)
  * [Block Diagram](readme/block-diagram.md)
  * [Unofficial Specifications](readme/unofficial-specifications.md)
  * [How to order - Part Numbers](readme/ordering-info.md)
  * [Caution and Disclaimers](disclaimers.md)
    * [FCC / IC information](readme/disclaimers/fcc-ic-information.md)
    * [Note about the source code provided here in this document](readme/disclaimers/note-about-the-source-code-provided-here-in-this-document.md)
* [Prerequisites](prerequisites/README.md)
  * [Supported Hardware](prerequisites/supported-hardware/README.md)
    * [NavQPlus add on modules](prerequisites/supported-hardware/navqplus-add-on-modules.md)
  * [Supported Software](prerequisites/supported-software/README.md)
    * [Build from Source (Docker Image)](prerequisites/supported-software/build-from-source-docker-image.md)
  * [Experimental Nature](prerequisites/experimental-nature.md)
  * [Ubuntu Proof of Concept (Ubuntu POC)](prerequisites/ubuntu-proof-of-concept-ubuntu-poc.md)

## NavQPlus User Guide

* [Quick start guide](navqplus-user-guide/setup-guide-emmc.md)
* [Typical NavQPlus Interface usage](navqplus-user-guide/quickstart/README.md)
  * [Power supply options](navqplus-user-guide/quickstart/power.md)
  * [Serial Console](navqplus-user-guide/quickstart/serial-console/README.md)
    * [Additional Boot Details](navqplus-user-guide/quickstart/serial-console/boot.md)
  * [Wired Network connections](navqplus-user-guide/quickstart/ethernet-over-usbc-gadget-mode.md)
  * [Wireless Networking](navqplus-user-guide/quickstart/wireless-networking/README.md)
    * [WiFi - nmtui](navqplus-user-guide/quickstart/wireless-networking/wifi-nmtui.md)
  * [Camera Usage](navqplus-user-guide/quickstart/taking-an-image-from-the-camera.md)
  * [Flashing new firmware](navqplus-user-guide/quickstart/flashing-with-new-firmware/README.md)
    * [Boot DIP Switches](navqplus-user-guide/quickstart/flashing-with-new-firmware/flashing-with-new-firmware.md)
* [Application Software](navqplus-user-guide/software/README.md)
  * [OpenCV](navqplus-user-guide/software/opencv.md)
  * [GStreamer](navqplus-user-guide/software/gstreamer.md)
  * [I2C](navqplus-user-guide/software/i2c.md)
  * [WebServer](navqplus-user-guide/software/webserver.md)
* [TurtleBot4 - iRobot Create3](navqplus-user-guide/turtlebot4-irobot-create3.md)
* [MR-B3RB](navqplus-user-guide/mr-b3rb.md)
* [Simulation](navqplus-user-guide/simulation.md)

## NavQPlus HW Reference <a href="#hardware" id="hardware"></a>

* [Schematics](hardware/schematics.md)
* [Hardware interfaces usage](hardware/hardware-interfaces/README.md)
  * [CAN Bus](hardware/hardware-interfaces/can-bus.md)
  * [Network Management](hardware/hardware-interfaces/network-management.md)
  * [IX Industrial Ethernet](hardware/hardware-interfaces/ix-industrial-ethernet.md)
  * [MIPI CSI (Camera)](hardware/hardware-interfaces/mipi-csi/README.md)
    * [MIPI-CSI interface RevA vs RevB rework](hardware/hardware-interfaces/mipi-csi/mipi-csi-interface-reva-vs-revb-rework.md)
  * [100BaseT1 "2-Wire" Ethernet](hardware/hardware-interfaces/t1-2-wire-automotive-ethernet/README.md)
    * [Available 100BaseT1 hardware](hardware/hardware-interfaces/t1-2-wire-automotive-ethernet/t1-2-wire-automotive-ethernet.md)
  * [I2C](hardware/hardware-interfaces/i2c.md)
  * [UARTS](hardware/hardware-interfaces/uart/README.md)
    * [UART1 (Bluetooth)](hardware/hardware-interfaces/uart/uart1-bluetooth.md)
    * [UART2 (A53 Debug)](hardware/hardware-interfaces/uart/uart2-a53-debug.md)
    * [UART3 (SPI)](hardware/hardware-interfaces/uart/uart3.md)
    * [UART4 (M7 MCU Core)](hardware/hardware-interfaces/uart/uart4-m7-core.md)
  * [USB-C](hardware/hardware-interfaces/usb-c.md)
  * [PCIe](hardware/hardware-interfaces/pcie.md)
  * [GPIO](hardware/hardware-interfaces/gpio/README.md)
    * [AUX - GPIO](hardware/hardware-interfaces/gpio/aux-gpio.md)
    * [Miscellaneous GPIO pins](hardware/hardware-interfaces/gpio/miscellaneous-gpio-pins.md)
  * [External RTC - Timestamp inputs](hardware/hardware-interfaces/external-rtc-timestamp-inputs.md)
  * [Micro-HDMI](hardware/hardware-interfaces/micro-hdmi.md)
  * [LVDS](hardware/hardware-interfaces/lvds.md)
  * [MIPI DSI](hardware/hardware-interfaces/mipi-dsi.md)

## tips and tricks

* [Extra - HowTo Linux notes](tips-and-tricks/extra-howto-linux-notes.md)
* [Remote control setup](tips-and-tricks/remote-control-setup.md)
* [Introduction to Tips-and-Tricks](tips-and-tricks/introduction-to-tips-and-tricks.md)
* [Linux Host Computer Tips](tips-and-tricks/linux-host-computer-tips.md)
* [YouTube Links](tips-and-tricks/youtube-links.md)
* [3D Printer Files](tips-and-tricks/3d-printer-files.md)
  * [NavQPlus Drone Mounting Plate](tips-and-tricks/3d-printer-files/navqplus-drone-mounting-plate.md)
  * [Google Coral Camera Mounts](tips-and-tricks/3d-printer-files/google-coral-camera-mounts.md)
* [AI/ML Links](tips-and-tricks/ai-ml-links.md)
* [Lightweight GUI](tips-and-tricks/lightweight-gui.md)
* [Ethernet](tips-and-tricks/ethernet.md)
* [Run a script on startup](tips-and-tricks/run-script-on-startup.md)

## 👥 User Contributed Content

* [WiFi](user-contributed-content/wifi.md)
* [AI/ML](user-contributed-content/ai.md)
* [ROS2](user-contributed-content/ros2/README.md)
  * [MicroDDS Agent/MicroROS](user-contributed-content/ros2/microdds.md)
  * [ROS2 example](user-contributed-content/ros2/ros2-example.md)

## MR-Buggy3 Demo

* [MR-B3RB Demo](mr-buggy3-demo/mr-b3rb-demo.md)
* [NavQPlus\_MR-Buggy3 Tradeshow Demo Guide (2022)](mr-buggy3-demo/mr-buggy3-demo-guide.md)
* [Operate MR-Buggy 3 using NavQPlus and FMURT6](mr-buggy3-demo/operate-mr-buggy-3-using-navqplus-and-fmurt6.md)

## LED & OLED Demo

* [Operate APA102 LED Board via ROS2 on NavQPlus over UCANS32K1 Board](led-and-oled-demo/mr-buggy3-demo-guide.md)
* [Operate SSD1306 OLED via NavQPlus](led-and-oled-demo/operate-ssd1306-oled-via-navqplus.md)
