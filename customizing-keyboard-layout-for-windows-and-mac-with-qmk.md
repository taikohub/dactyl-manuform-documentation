# 3. Customizing Keyboard Layout for Windows and Mac with QMK

3.1 Instructions

This section uses QMK Toolbox, a GUI (graphical user interface) compatible with Mac and Windows. The QMK CLI (command line interface) is also compatible with Mac and Windows. But if you are not familiar with programming, you should follow section instead.

{% hint style="warning" %}
QMK Toolbox currently does not support Linux. See [Section 4](customizing-keyboard-layout-for-linux-with-qmk.md) instead.
{% endhint %}

{% hint style="info" %}
For troubleshooting with QMK Toolbox, see [Section 8.1](troubleshooting/qmk-toolbox.md).
{% endhint %}

<mark style="color:yellow;">`Text in this format and color refers to something you can click on.`</mark>

> Text in block quotes refers to text output from QMK Toolbox.



3.2 Navigate to  [QMK Configurator](https://config.qmk.fm/#/handwired/dactyl\_manuform/5x6/LAYOUT\_5x6).

![Figure 3.1. QMK Configurator. Letters A to H refer to each step in this section.](.gitbook/assets/qmkconfigurator\_0.png)

Letters A to H in Figure 3.1 refer to each step in this section.

&#x20;

A. Click the <mark style="color:yellow;">`Keyboard`</mark> <mark style="color:yellow;"></mark><mark style="color:yellow;"></mark> dropdown. Select <mark style="color:yellow;">`handwired/dactyl_manuform/5x6`</mark>.&#x20;

B. Enter the name you want to give your layout. For example, you put <mark style="color:yellow;">my\_keymap</mark>, QMK will later generate a file with the name <mark style="color:yellow;">`handwired_dactyl_manuform_5x6_my_keymap.hex`</mark>

<details>

<summary>C. keymap.json - Save your progress (Optional)</summary>

If you're not fully done customizing your keymap, the keymap.json file is a way to save your progress. You can return to your save point by uploading the keymap.json file to QMK Configurator. Note that downloading the keymap.json file is optional and the file is not what you use to flash your keyboard.

</details>

<details>

<summary>D. keymap.json - Load previous save point (Optional)</summary>

As described in the previous step, this gives you the option to upload the keymap.json file to return to your save point.

</details>

E. This section in Figure 3.1 highlights the keyboard layout.

F. Try dragging the <mark style="color:yellow;">`F1`</mark> keycode onto <mark style="color:yellow;">`End`</mark> on the keyboard layout. This changes that switch on the layout from <mark style="color:yellow;">`End`</mark> to <mark style="color:yellow;">`F1`</mark>. You likely won't want that button to be <mark style="color:yellow;">`F1`</mark>. Change it back by finding <mark style="color:yellow;">`End`</mark> in the keycode section and drag it to replace <mark style="color:yellow;">`F1`</mark>. Now that you're familiar with this, feel free to customize your keyboard layout.&#x20;

The sections below refer to a specific QMK functionality called layers that is not seen in a traditional keyboard. If this is not important to you, feel free to skip to part G.

<details>

<summary>Layers - What are they?</summary>

Layers are a QMK specific functionality. The concept is similar to the Fn or FnLock key that is seen on some keyboards.

If you are coming from a traditional keyboard, the easiest way to understand layers is to interact with it. In Figure 3.1, Layer 0 is selected. Try clicking on layer 1, 2, or others. Clicking on a different layer will bring up a different layout.

</details>

<details>

<summary>Layer keys - What are they?</summary>

Pressing a layer key switches the layout a different layer.&#x20;

1\. MO(layer)

In Figure 3.1, the layer keys look like <mark style="color:yellow;">`MO(1)`</mark> or <mark style="color:yellow;">`MO(2)`</mark>. This <mark style="color:yellow;">`MO(layer)`</mark> stands for momentarily activating the layer. This works similar to the Fn or Shift key on a regular keyboard.&#x20;

If you used a keyboard flashed with the keymap seen in Figure 3.1, you must hold both "MO(2)" and "P" to get "Scroll Lock" on layer 2. As soon as you release the "MO(2)" key, it goes back to the original layer. Layers range from 0 to 15.



2\. DF(layer)

`DF(layer)` stands for default layer. It is similar to the FnLock key seen on some keyboards.

Tapping this key switches your keymapping to the new layer until you decide to switch to a different layer by pressing another DF key.

</details>

G. When you are finished customizing your layout, click <mark style="color:yellow;">`Compile`</mark>. You should see a nice rotating potato baking in outerspace. Once this is done, the <mark style="color:yellow;">`Download Firmware`</mark> button should no longer be gray.

H. Click <mark style="color:yellow;">`Download Firmware`</mark>. It will download a file with a name similar to `handwired_dactyl_manuform_5x6_your_keymap.hex`. You will use this to flash your keyboard. You are ready to go to part 3.3.&#x20;



3.3 Open the website to [QMK Toolbox](https://github.com/qmk/qmk\_toolbox/releases), which is used to flash the hex file onto your keyboard.

![Figure 3.2. QMK Toolbox website navigation. The photo was taken when the latest version was 0.0.21. The latest version is now 0.2.2.](.gitbook/assets/qmktoolbox\_0.png)

A. Check that you are looking at the latest release. In the photo above, the latest version was 0.0.21. The latest release as of this writing is 0.2.2. If the latest version has the name "Latest Beta", scroll down to the next latest version.

B. Click to download <mark style="color:yellow;">`qmk_toolbox.pkg`</mark> if you use Mac.

C. Click to download <mark style="color:yellow;">`qmk_toolbox.exe`</mark> if you use Windows.



3.4 Open <mark style="color:yellow;">`qmk_toolbox.pkg`</mark>  or <mark style="color:yellow;">`qmk_toolbox.exe`</mark>. If you are opening QMK Toolbox for the first time, you might see a dialogue box asking "Would you like to install drivers for your devices?". Select <mark style="color:yellow;">`Yes`</mark>.

![Figure 3.3. QMK Toolbox Navigation](.gitbook/assets/qmktoolbox\_open.png)

A. If this is your first time using QMK Toolbox on your computer and you did not see the install drivers dialogue box, go to <mark style="color:yellow;">`Tool`</mark> then <mark style="color:yellow;">`Install Drivers`</mark>.

B. Click <mark style="color:yellow;">`Open`</mark> then select the <mark style="color:yellow;">`handwired_dactyl_manuform_5x6_your_keymap_name.hex`</mark> file that was downloaded earlier.

C. Make sure the dropdown menu shows <mark style="color:yellow;">`Atmega32U4`</mark>.

D. Check off <mark style="color:yellow;">`Auto-Flash`</mark>. **DO NOT click Flash just yet!**&#x20;

Before you flash the firmware, ensure you have:

* [ ] Disconnect the audio cord from each piece of the keyboard. This cord normally connects to the socket indicated by the blue arrow in Figure 4.2 below.
* [ ] Connected one piece of the keyboard to your computer via USB cord.

E. After ensuring only one piece of the keyboard is connected to your computer and the audio cord is disconnected from both sides, click <mark style="color:yellow;">`Flash`</mark>. The toolbox will wait for you as you perform the following step.



3.4 Next, click the reset button indicated by the green arrow in Figure 3.4.

![Figure 3.4 The green arrow indicates the reset switch. The blue arrow indicates the socket connecting the two pieces of the keyboard.](.gitbook/assets/taikorobotics\_ergonomic\_split\_mechanical\_curvilinear\_keyboard\_with\_audio\_socket.jpg)

If it flashes correctly, you should see the following.

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



3.5 Repeat sections 3.3.E and 3.5 for the other piece of your keyboard.



3.6 Reconnect the two pieces with the audio cord. The sockets for each piece are shown by the blue arrow in Figure 3.4. Then connect the USB cord from the **left** keyboard to the computer. Good work, you did it 🥳!

