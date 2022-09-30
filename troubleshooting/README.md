# 9. Troubleshooting

9.1 Keyswitch is not working

Remove the keyswitch from the socket with a keyswitch puller. Check if the metal pins on the bottom of the keyswitch are straight. If any of them are bent, gently bend it straight with pliers. If you don’t have pliers, you can use the pads of your fingers to gently pinch it straight.

If the keyswitch pins are straight, open up the base plate and check if any wires have come off of the microcontroller.



9.2 Keymapping is flipped

Check whether the USB cord is connecting the **left** piece of the keyboard to the computer. The USB socket on the right keyboard should only be used to flash keymapping. Conceptually, your computer assumes the keyboard connected to it is the left side. It assumes the right side is other piece.

If you had not disconnected the TRRS cord from each piece of the keyboard while flashing a new keymapping, you will need to re-flash each piece of the keyboard.



9.3 Thumb cluster not working after flashing right side of the keyboard

If the right side of the keyboard is directly connected to the computer, some keys on the thumb cluster will not register. This is normal. Simply make sure USB cable is connected to the left side of the keyboard and the TRRS cable is connected to the right side of the keyboard. The keyboard should start working as normal.



9.4 Keyboard doesn't register any keys

If you are using a different USB cord from the one that came with your keyboard, it may be a USB cord issue. Check to see if the keyboard works with the default USB cord. Certain USB cords do not play well with the microcontroller. If you are using a USB-C to USB-C cord, try switching which side of the cord you plug into the computer and which side you plug into the keyboard. This can sometimes resolve the problem.&#x20;



9.5 My problem isn't mentioned in the documentation

Please share it in the GitHub discussion section seen below.

{% embed url="https://github.com/taikohub/dactyl-manuform-documentation/discussions/categories/general" %}
