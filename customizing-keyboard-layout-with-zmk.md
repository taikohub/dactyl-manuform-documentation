---
description: (10 min read)
---

# 5. Customizing Keyboard Layout with ZMK

5.1 ZMK Firmware

**Firmware:** Firmware is software installed on microcontrollers to make your keyboard work.

**ZMK Firmware:** ZMK firmware is also known as just ZMK. It is a keyboard firmware similar to QMK, which is what your keyboard initially came with. ZMK and QMK are nearly identical for most users. The main difference being: If you want Bluetooth, use ZMK. If you want wired, use QMK.



{% hint style="info" %}
The first step to adding Bluetooth is to swap in nice!nanos. Follow steps from[bluetooth.md](swapping-microcontrollers/bluetooth.md "mention") before continuing below.
{% endhint %}



5.2 Adding Bluetooth Functionality - The Fast Way (5 minutes)

If you want your keyboard to have the same QWERTY layout as it initially came with, continue following this section. Otherwise, skip to Section 5.3.



Step 1. Download the configuration file for the left and right piece of your keyboard.

{% tabs %}
{% tab title="Size Large (6 Key Thumb Cluster)" %}


{% file src=".gitbook/assets/dactyl_manuform_5x6_left-nice_nano_v2-zmk.uf20-4233576" %}
ZMK Configuration File for the **Left** side of the TaikoHub Dactyl Manuform Keyboard in Size Large (Six Keyed Thumb Cluster)
{% endfile %}

{% file src=".gitbook/assets/dactyl_manuform_5x6_right-nice_nano_v2-zmk.uf203633576" %}
ZMK Configuration File for the **Right** side of the TaikoHub Dactyl Manuform Keyboard in Size Large (Six Keyed Thumb Cluster)
{% endfile %}
{% endtab %}

{% tab title="Size Medium (5 Key Thumb Cluster)" %}


{% file src=".gitbook/assets/dactyl_manuform_5x6_left-nice_nano_v2-zmk.uf20-3433576" %}
ZMK Configuration File for the **Left** side of the TaikoHub Dactyl Manuform Keyboard in Size Medium (Five Keyed Thumb Cluster)
{% endfile %}

{% file src=".gitbook/assets/dactyl_manuform_5x6_right-nice_nano_v2-zmk (2).uf2" %}
ZMK Configuration File for the **Right** side of the TaikoHub Dactyl Manuform Keyboard in Size Medium (Five Keyed Thumb Cluster)
{% endfile %}
{% endtab %}

{% tab title="Size Small (3 Key Thumb Cluster)" %}


{% file src=".gitbook/assets/dactyl_manuform_5x6_left-nice_nano_v2-zmk.uf2" %}
ZMK Configuration File for the **Left** side of the TaikoHub Dactyl Manuform Keyboard in Size Small (Three Keyed Thumb Cluster)
{% endfile %}

{% file src=".gitbook/assets/dactyl_manuform_5x6_right-nice_nano_v2-zmk (1).uf2" %}
ZMK Configuration File for the **Left** side of the TaikoHub Dactyl Manuform Keyboard in Size Small (Three Keyed Thumb Cluster)
{% endfile %}
{% endtab %}
{% endtabs %}



Step 2. Make sure the two sides of the keyboard are **not** connected to each other. Connect only the left piece of your keyboard to the computer.

Step 3. Click the reset switch twice. You should see `NICE!NANO` show up as a USB device. If you opened up the directory, you would see 3 files. Ignore them. Do not edit or delete them. Even after you flash the keyboard, there will only be these 3 files.

<figure><img src=".gitbook/assets/NICENANO should show up on as a USB device.png" alt=""><figcaption><p>Figure 5.2.1 You should see <code>NICE!NANO</code> show up as a USB device.</p></figcaption></figure>

Step 4. Drag the  `dactyl_manuform_5x6_left-nice_nano_v2-zmk.uf` file into the USB device directory. You may see the following prompt: `Error while copying "dactyl_manuform_5x6_left-nice_nano_v2-zmk.uf2"`. This is not an actual error. The nice!nano uses the file you dragged to flash itself, then automatically ejects itself as a USB device.

<figure><img src=".gitbook/assets/Error while copying.png" alt=""><figcaption><p>Figure 5.2.2 This prompt is not an error: <code>Error while copying "dactyl_manuform_5x6_left-nice_nano_v2-zmk.uf2"</code> .</p></figcaption></figure>

Step 5. Repeat the same thing with the right side of the keyboard. Woot you're done! 🙌



5.2 Adding Bluetooth Functionality - The Slow Way (10+ minutes)

Coming soon.

