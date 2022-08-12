# 3. Customizing Keyboard Layout for Windows and Mac

{% hint style="warning" %}
QMK Toolbox currently does not support Linux. See [Section 4](customizing-keyboard-layout-for-linux.md) instead.
{% endhint %}

{% hint style="info" %}
For troubleshooting, see [Section 8.1](troubleshooting/qmk-toolbox.md).
{% endhint %}



3.1 Navigate to  [QMK Configurator](https://config.qmk.fm/#/handwired/dactyl\_manuform/5x6/LAYOUT\_5x6) to begin creating a custom key map for your keyboard.

![Figure 3.1. QMK Configurator](.gitbook/assets/qmkconfigurator\_0.png)

A. Keyboard: Selects pre-configured key mappings. Typing in dactyl will bring up a list of different variations of the dactyl\_manuform keymapping. Select handwired/dactyl\_manuform/5x6 here.

B. Keymap Name: Enter a name for your custom keymap. Eventually, QMK will generate a hex file with the name `handwired_dactyl_manuform_5x6_your_keymap_name.hex`

C. Download keymap.json: Downloads a keymap.json file with your current keymapping. This file saves your progress as you create a new keymap. You can return to your save point by uploading the keymap.json file on the QMK Configurator website. Note that downloading the keymap.json file is optional and the file is not what you use to flash your keyboard.

D. Upload keymap.json: As described in _C_, this gives you the option to upload the keymap.json file to return to your save point.

E. Layers: Layers are a QMK specific functionality. The concept is similar to a Fn or FnLock key that is seen on some keyboards. In _Figure 3.1_, layer 0 is selected. Clicking on 1 or 2 in the layer section will bring up a different keymap.&#x20;

A layer key is what you actually press on your keyboard to switch to a different layer. On the keymap in _Figure 3.1_, the layer keys look like "MO(1)" or "MO(2)". The MO(layer) stands for Momentarily activating the layer, similar to a Fn or Shift key on a regular keyboard. For example in the keymap in _Figure 3.1_, you must hold both "MO(2)" and "P" to get "Scroll Lock" on layer 2. As soon as you release the "MO(2)" key, it goes back to the original layer. Layers range from 0 to 15.&#x20;

A more useful layer key is the DF(layer) key. The DF stands for Default. Tapping this key switches your keymapping to the new layer until you decide to switch to a different layer by pressing another DF key. This is similar to the FnLock key seen on some keyboards.

F. Keycodes: Drag the keycode onto the keymap to replace the key. As per QMK, North America primarily uses ANSI, Europe and Africa primarily use ISO, and Japan uses JIS. You'll find the MO(layer) and DF(layer) keys by navigating to _Quantum > Layer_ _and Layer Tap functions._

G. When you are finished customizing your keymap, click compile. You should see a nice rotating potato baking in outerspace. Once QMK has finished compiling, the Download Firmware button should become clickable.

H. Download Firmware: Download the `handwired_dactyl_manuform_5x6_your_keymap_name.hex` file. You will use this to flash your keyboard.



3.2 Open the website to [QMK Toolbox](https://github.com/qmk/qmk\_toolbox/releases), which is used to flash the hex file onto your keyboard.

![Figure 3.2. QMK Toolbox website navigation](.gitbook/assets/qmktoolbox\_0.png)

A. Check that you are looking at the latest release. In the photo above, the latest version was 0.0.21. The latest release as of this writing is 0.1.1, but this could be different from what you see.

B. Download QMK.Toolbox.pkg if you use a Mac.

C. Download qmk\_toolbox.exe if you use Windows.



3.3 Open QMK.Toolbox.pkg or qmk\_toolbox.exe. If you are opening QMK Toolbox for the first time on Windows, you might see a dialogue box asking "Would you like to install drivers for your devices?". Select "Yes".

![Figure 3.3. QMK Toolbox Navigation](.gitbook/assets/qmktoolbox\_open.png)

A.  Install Drivers: If this is your first time using QMK Toolbox on your Windows PC and you did not see the install drivers dialogue box, right click the bottom bar of the QMK Toolbox and select Install Drivers.

B. Open Local File: Open the `handwired_dactyl_manuform_5x6_your_keymap_name.hex` file you previously downloaded.

C. Make sure it says Atmega32U4. If it doesn't, it select from the drop down.

D. Select Auto-Flash. **Do not click Flash yet!** First ensure your keyboard is unplugged from your computer. Disconnect the TRRS cord from each piece of the keyboard. Then connect only one piece of the keyboard to your computer via USB. Note that the TRRS cord looks like an audio cord and connects to the socket indicated by the blue arrow in Figure 3.4 below.

E. After ensuring only one piece of the keyboard is connected to your computer and the TRRS cord is disconnected from both sides, click Flash. The toolbox will wait for you as you perform the following step.



3.4 Next, click the reset button indicated by the green arrow in Figure 3.4. You will need to use a stick or a pen to click it.

![Figure 3.4 The green arrow indicates the reset switch. The blue arrow indicates the TRRS socket.](.gitbook/assets/taikorobotics\_ergonomic\_split\_mechanical\_curvilinear\_keyboard\_with\_audio\_socket.jpg)

If it flashes correctly, you should see the following

> Attempting to flash, please don't remove device
>
> avrdude.exe -p atmega32u4 -c avr109 -U flash:w:"C:\Users\username\Desktop\firmware\qmk\windows\five\handwired\_dactyl\_manuform\_5x6.hex":i -P COM6
>
> Connecting to programmer: . Found programmer: Id = "CATERIN"; type = S Software Version = 1.0; No Hardware Version given. Programmer supports auto addr increment. Programmer supports buffered memory access with buffersize=128 bytes.
>
> Programmer supports the following devices: Device code: 0x44
>
> avrdude.exe: AVR device initialized and ready to accept instructions
>
> Reading | ################################################## | 100% 0.00s
>
> avrdude.exe: Device signature = 0x1e9587 (probably m32u4) avrdude.exe: NOTE: "flash" memory has been specified, an erase cycle will be performed To disable this feature, specify the -D option. avrdude.exe: erasing chip avrdude.exe: reading input file "C:\Users\username\Desktop\firmware\qmk\windows\five\handwired\_dactyl\_manuform\_5x6.hex" avrdude.exe: writing flash (19424 bytes):
>
> Writing | ################################################## | 100% 1.47s
>
> avrdude.exe: 19424 bytes of flash written avrdude.exe: verifying flash memory against C:\Users\username\Desktop\firmware\qmk\windows\five\handwired\_dactyl\_manuform\_5x6\_five.hex: avrdude.exe: load data flash data from input file C:\Users\username\Desktop\firmware\qmk\windows\five\handwired\_dactyl\_manuform\_5x6\_five.hex: avrdude.exe: input file C:\Users\username\Desktop\firmware\qmk\windows\five\handwired\_dactyl\_manuform\_5x6\_five.hex contains 19424 bytes avrdude.exe: reading on-chip flash data:
>
> Reading | ################################################## | 100% 0.16s
>
> avrdude.exe: verifying ... avrdude.exe: 19424 bytes of flash verified
>
> avrdude.exe: safemode: Fuses OK (E:CB, H:D8, L:FF)
>
> avrdude.exe done. Thank you.
>
> Flash complete



3.5 Repeat sections 2.4 and 2.5 for the other piece of your keyboard.

3.6 Connect the TRRS cord to the two pieces. The sockets for each piece are shown by the blue arrow in Figure 3.4. Then connect the USB cord from the **left** keyboard to the computer.

