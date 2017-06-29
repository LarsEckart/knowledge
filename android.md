# Android

## How to connect via wifi to your device

1) connect the device via usb
2) Figure out the device's ip address

```bash
adb shell ip -f inet addr show wlan0
```

3) run these commands to connect to the device

```bash
adb tcpip 5555
adb connect 192.168.xxx.xxx:5555
```
