# 7. Swapping Microcontrollers

7.1 Microcontrollers

A microcontroller is a small device that controls your keyboard. Each piece of your keyboard comes with a Pro Micro microcontroller. You may come across it abbreviated as MCU, which stands for MicroController Unit.



7.2 Why swap microcontrollers?

The main reason to swap microcontrollers is to add new features. For example, you may want to use a nice!nano microcontroller to add Bluetooth functionality. Or you may want to use a Adafruit KB2040, which uses a more powerful RP2040 chip, to add very complex macros.&#x20;

{% hint style="danger" %}
Unplug any cords or batteries before swapping your microcontrollers.
{% endhint %}



7.3 Necessary tools and components

* 3mm Allen key
* Two new microcontrollers
  * These need to have a similar footprint to the Arduino Pro Micro.&#x20;
  * Compatible microcontrollers includes Adafruit KB2040, nice!nano, among many others.&#x20;

{% hint style="warning" %}
Not compatible with BlueMicro840 V1.0.
{% endhint %}



7.4. Swapping microcontrollers

a. Remove all power source from your keyboard. Unplug any cords or batteries.

b. Take off the plastic cover on the base plate of the keyboard, indicated by the yellow arrow in Figure 7.2. You can use a pen or an Allen key to **gently** wedge it out from the sides, as indicated by the blue arrows in Figure 7.2. You should take turns wedging from each side.

![Figure 7.2. Take off the cover for the microcontroller indicated by the yellow arrow. You may need to use a pen to gently wedge on either side of the cover, indicated by the blue arrows.](.gitbook/assets/taikorobotics\_ergonomic\_split\_mechanical\_keyboard\_sized\_medium\_base\_plate.jpg)

c. Remove the microcontroller that came with the keyboard. Hold the microcontrollers by the top and bottom as indicated by the yellow arrows on Figure 7.3. Then gently wiggle it out.&#x20;

![Figure 7.3. Put your fingers on each side of the microcontroller indicated by the yellow arrows, then gently wiggle it out.](.gitbook/assets/taikorobotics\_ergonomic\_split\_mechanical\_keyboard\_sized\_medium\_pro\_micro\_removal.jpg)

d. **Gently** plug in your own microcontroller. Note that some microcontrollers will require you to solder pin headers onto them.

![Figure 7.4. Insert the new microcontroller. Adafruit KB2040 is shown here.](.gitbook/assets/taikorobotics\_ergonomic\_split\_mechanical\_keyboard\_sized\_medium\_swap\_microcontroller\_to\_adafruit\_kb2040.jpg)

e. Some microcontrollers, such as the KB2040, are slightly smaller than the microcontroller that came with your keyboard. If you want the USB-C port closer to the front of the keyboard, you need to open up the baseplate to slide the microcontroller forward. Put the cover back on and you're finished 🎉!



7.5 Bluetooth: Support

Although Bluetooth works, it's not officially supported. If this is something you're considering, please contact david@taikohub.com. Please note this is **highly recommended**. It'll be safer for you and you're not wasting my time, really!

{% hint style="warning" %}
Bluetooth functionality is not officially supported. Only do it if you know what you're doing. Add it at your own risk.
{% endhint %}

{% hint style="info" %}
QMK does not work well with Bluetooth. It's recommended to use ZMK instead.
{% endhint %}



7.6 Bluetooth: Necessary tools and components

* 3mm Allen key
* Two new microcontrollers
  * These need to have a similar footprint to the Arduino Pro Micro.&#x20;
  * Compatible microcontrollers includes nice!nano, among others.

{% hint style="warning" %}
Not compatible with BlueMicro840 V1.0.
{% endhint %}

* To add Bluetooth, you will also need:
  * Two LiPo batteries with 2 Pin JST-PH. It's safest to get them from Adafruit or Sparkfun.
  * Two On-Off Switches. Not all on-off switches will work here. Compatible switches may include toggle switch, latching switch or slide switch. Momentary switches will not work. The on-off switch can't be too large, because of limited room.&#x20;
  * Two 2x1 female pin headers with 2.54mm pitch. 2x1 is also known as single row, two pins.
  * Crimping tool. To attach the pin headers onto the wires.

{% hint style="danger" %}
Double check what LiPo battery you need for your microcontroller on the manufacturer's website! Different microcontrollers may require different batteries. <mark style="color:red;">**Using the wrong battery can lead to**</mark> <mark style="color:red;">**explosions**</mark>!

Make sure that your JST-PH is correctly wired! As in, make sure that the black wire and red wire are in the correct orientation on the JST-PH connector, shown in Figure 7.5. Adafruit and Sparkfun are generally reliable, but some vendors sell LiPo batteries with their wires reversed. See video on this issue by Adafruit [here](https://www.youtube.com/watch?v=ILArrTIMFyM).
{% endhint %}

![Figure 7.5 LiPo Battery. Ensure the orientation of the red and black wires connecting to the JST-PH header is correct. The JST-PH header has two different sides.](.gitbook/assets/lipo\_battery\_caution.png) ![Figure 7.6. This 3.7V 110mAh LiPo battery worked with nice!nano's during testing.](.gitbook/assets/lipo\_battery.jpg)



7.7. Adding Bluetooth

a. Swap in your Bluetooth enabled microcontroller.

b. Flash your new microcontroller with ZMK. See ZMK documentation [here](https://zmk.dev/docs/user-setup).

c. Attach the LiPo battery to the JST-PH socket indicated by the green arrow in Figure 7.7.

![Figure 7.7. Keyboard with nice!nano microcontroller. Green arrow indicates the JST-PH socket for the Lipo battery. Purple arrow indicates pin headers for the on-off switch.](.gitbook/assets/taikorobotics\_ergonomic\_split\_mechanical\_keyboard\_sized\_medium\_swap\_microcontroller\_to\_nice\_nano\_assembly.jpg)

d. Use your crimping tool to attach female pin headers to the wires on your on-off switch.

e. Attach the female pin headers indicated by the purple arrow in Figure 7.7. It should attach to the two male pin headers on the top right as indicated by the red arrows in Figure 7.8. The orientation doesn't matter. Technically you could even use a wire with two female pin headers. Although the keyboard would remain 'ON' until you disconnect the wire or the battery runs out.

![Figure 7.8. Attach the on-off switch to the two male pin headers on the top right as indicated by the red arrows.](.gitbook/assets/male\_pin\_headers\_for\_on\_off\_switch.jpg)

f. Put the cover back on, then turn on your keyboard. You did it 🎉!
