# Run/install/debug Android applications over Wi-Fi
1. Connect the device via USB and make sure USB Debugging is working. 
2. In Terminal, type ```adb tcpip 5555 ```. This makes the device to start listening for connections on port 5555.
3. Look up the device IP address with ```adb shell netcfg``` or ```console adb shell ifconfig``` with Android 6.0 or higher. Else just
   check your device settings to find your device's IP Address.
4. You can disconnect the USB now.
5. ```adb connect <DEVICE_IP_ADDRESS>:5555```. This connects to the server we set up on the device in step 2.
6. Now you have a device over the network with which you can debug as usual.

To switch the server back to the USB mode, run ```adb usb```, which will put the server on your phone back to the USB mode.

If you have more than one device, you can specify the device with the -s option: ```adb -s <DEVICE_IP_ADDRESS>:5555 usb```.

### Note: If you are on a different network and same PC continue from Step 5 where your DEVICE_IP_ADDRESS will be different this time.
