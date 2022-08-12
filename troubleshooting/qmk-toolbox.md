---
description: >-
  QMK Toolbox is the graphical interface for Windows and Mac. It is not
  compatible with Linux.
---

# 8.1 Troubleshooting: QMK Toolbox

<details>

<summary>8.1.1 <code>read error: The I/O operation has been aborted because of either a thread exit or an application request.</code></summary>

Problem: You tried to flash with QMK Toolbox. It completed the flash, but the keyboard didn't get flashed with your new keymapping at all. You see an output similar to the following in QMK Toolbox.



```
Caterina device connected (usbser): Arduino LLC (www.arduino.cc) Arduino Leonardo bootloader (COM6) (2341:0036:0001) [COM6] Attempting to flash, please don't remove device
avrdude.exe -p atmega32u4 -c avr109 -U flash:w:"C:\Users\username\Desktop\firmware\qmk\windows\five\handwired_dactyl_manuform_5x6.hex":i -P COM6 avrdude.exe: ser_drain(): read error: The I/O operation has been aborted because of either a thread exit or an application request.

Connecting to programmer: .avrdude.exe: ser_send(): write error: sorry no info avail avrdude.exe: ser_drain(): read error: The device does not recognize the command.

avrdude.exe: ser_send(): write error: sorry no info avail avrdude.exe: ser_recv(): read error: The device does not recognize the command.

avrdude.exe: butterfly_recv(): programmer is not responding

avrdude.exe: ser_recv(): read error: The device does not recognize the command.

avrdude.exe: butterfly_recv(): programmer is not responding avrdude.exe: ser_drain(): read error: The device does not recognize the command.

avrdude.exe: ser_send(): write error: sorry no info avail avrdude.exe: ser_recv(): read error: The device does not recognize the command.

avrdude.exe: butterfly_recv(): programmer is not responding avrdude.exe: ser_send(): write error: sorry no info avail avrdude.exe: ser_recv(): read error: The device does not recognize the command.

avrdude.exe: butterfly_recv(): programmer is not responding avrdude.exe: ser_recv(): read error: The device does not recognize the command.

avrdude.exe: butterfly_recv(): programmer is not responding avrdude.exe: ser_send(): write error: sorry no info avail avrdude.exe: ser_recv(): read error: The device does not recognize the command.

avrdude.exe: butterfly_recv(): programmer is not responding Found programmer: Id = "‹"; type = > Software Version = â.·; Hardware Version = ö. avrdude.exe: ser_send(): write error: sorry no info avail avrdude.exe: ser_recv(): read error: The device does not recognize the command.

avrdude.exe: butterfly_recv(): programmer is not responding avrdude.exe: ser_send(): write error: sorry no info avail avrdude.exe: ser_recv(): read error: The device does not recognize the command.

avrdude.exe: butterfly_recv(): programmer is not responding avrdude.exe: error: buffered memory access not supported. Maybe it isn't a butterfly/AVR109 but a AVR910 device? avrdude.exe: initialization failed, rc=-1 Double check connections and try again, or use -F to override this check.

avrdude.exe: ser_send(): write error: sorry no info avail avrdude.exe: ser_recv(): read error: The device does not recognize the command.

avrdude.exe: butterfly_recv(): programmer is not responding avrdude.exe: error: programmer did not respond to command: leave prog mode avrdude.exe: ser_send(): write error: sorry no info avail avrdude.exe: ser_recv(): read error: The device does not recognize the command.

avrdude.exe: butterfly_recv(): programmer is not responding avrdude.exe: error: programmer did not respond to command: exit bootloader
avrdude.exe done. Thank you.
```



Possible Causes:

a. Another computer peripheral is interfering with QMK Toolbox. Try disconnecting anything connected to the computer except the keyboard. A computer peripheral is anything that physically connects to your computer, and includes: mouse, phone, cables, monitors, another keyboard, among others.

b. If the above doesn't work, please contact david@taikohub.com

</details>



