---
description: >-
  This page guides how client applications can communicate with the TurtlPass
  Firmware via USB serial. It also includes an example using the `arduino-cli`
  command-line tool.
---

# 🔁 USB Serial Communication

### Overview

Client applications, like our [Android app](https://github.com/TurtlPass/turtlpass-android) or [Chrome Extension](https://github.com/TurtlPass/turtlpass-chrome-extension), can communicate with the TurtlPass Firmware over USB serial to access its functionalities, including password generation, OTP management, and hardware encryption. By establishing a serial connection, client apps can send commands to the firmware and receive responses accordingly.

### Prerequisites

Before initiating USB serial communication with the TurtlPass Firmware from a client app, ensure the following:

* **TurtlPass Firmware:** Have the TurtlPass Firmware uploaded to an RP2040 microcontroller.
* **USB Connection:** Connect the RP2040 microcontroller to the host computer via USB.
* **Terminal Emulator:** Use a terminal emulator capable of establishing a serial connection (e.g., `arduino-cli`, Arduino IDE Serial Monitor, PuTTY, or minicom).

### Steps to Communicate

Follow these steps to establish USB serial communication between a client app and the TurtlPass Firmware:

1.  **Find Port of Connected Device**: Use the following command to find the port of the connected microcontroller device on the host machine:

    ```bash
    $ ls /dev/cu.* | grep usbmodem
    ```
2. **Open Serial Port**: The client app should open the serial port corresponding to the microcontroller device connected via USB.
3. **Set Baud Rate**: Configure the serial port to use a baud rate of `115200`, as this is the baud rate supported by the TurtlPass Firmware.
4. **Send Commands**: The client app sends commands to the serial port, following the syntax specified in the TurtlPass Firmware documentation. These commands can include requests for password generation, OTP management, or encryption operations.
5. **Receive Responses**: The TurtlPass Firmware processes the commands received over the serial port and provides responses accordingly. The client app reads these responses from the serial port to retrieve the requested information or perform the desired action.
6. **Close Connection**: Once communication is complete, the client app closes the serial port to release the resources and terminate the connection with the TurtlPass Firmware.

### Example using arduino-cli

Here's an example of how to communicate with the TurtlPass Firmware using the `arduino-cli` command-line tool:

```bash
$ arduino-cli monitor \
--config baudrate=115200 \
-p <PORT>
```

Replace `<PORT>` with the appropriate port identifier for your microcontroller device.

### Conclusion

Client applications can communicate with the TurtlPass Firmware over USB serial by following the steps outlined above. By establishing a serial connection and sending commands, client apps can leverage the features provided by the TurtlPass Firmware to enhance password management and encryption capabilities.
