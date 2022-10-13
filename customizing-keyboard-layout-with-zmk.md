---
description: (10 min read)
---

# 5. Customizing Keyboard Layout with ZMK

### 5.1 🌀ZMK Firmware

**Firmware:** Firmware is software installed on microcontrollers to make your keyboard work.

**ZMK Firmware:** ZMK firmware is also known as just ZMK. It is a keyboard firmware similar to QMK, which is what your keyboard initially came with. ZMK and QMK are nearly identical for most users. The main difference being: If you want Bluetooth, use ZMK. If you want wired, use QMK.



{% hint style="warning" %}
Swap in nice!nanos before following this section. See [bluetooth.md](swapping-microcontrollers/bluetooth.md "mention") before continuing below.
{% endhint %}



### 5.2 📶Adding Bluetooth Functionality

**Step 1.A** Add Bluetooth the Fast Way Using Default Configuration Files (5 minutes)

If you want your keyboard to have the same QWERTY layout as it initially came with, continue with this step. If you want to customize your keyboard layout, see Step 1.B instead.&#x20;

Download the configuration file for the left and right piece of your keyboard. Then skip Step 1.B and continue to Step 2.

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



**Step 1.B** Add Bluetooth the Slow Way By Customizing Your Own Configuration Files (10+ minutes)

Navigate to [https://github.com/taikohub/zmk-config](https://github.com/taikohub/zmk-config). See the `Getting Started` section in the README. The steps can be summarized as:&#x20;

1. Fork the repo.
2. Clone it to your local machine.
3. Edit `config/dactyl_manuform_5x6.keymap`.
4. Push the edits to your remote repo.
5. Navigate to GitHub Actions.
6. Click `firmware` to download the firmware.zip file.&#x20;
7. Unzip the firmware.zip. Then continue to Step 2.



**Step 2.** Make sure the two sides of the keyboard are **not** connected to each other. Connect only the left piece of your keyboard to the computer.



**Step 3.** Click the reset switch twice. You should see `NICE!NANO` show up as a USB device. If you opened up the directory, you would see 3 files. Ignore them. Do not edit or delete them. Even after you flash the keyboard, there will only be these 3 files.

<figure><img src=".gitbook/assets/NICENANO should show up on as a USB device.png" alt=""><figcaption><p>Figure 5.1 You should see <code>NICE!NANO</code> show up as a USB device.</p></figcaption></figure>



**Step 4.** Drag the  `dactyl_manuform_5x6_left-nice_nano_v2-zmk.uf` file into the USB device directory. You may see the following prompt: `Error while copying "dactyl_manuform_5x6_left-nice_nano_v2-zmk.uf2"`. This is not an actual error. The nice!nano uses the file you dragged to flash itself, then automatically ejects itself as a USB device.

<figure><img src=".gitbook/assets/Error while copying.png" alt=""><figcaption><p>Figure 5.2 This prompt is not an error: <code>Error while copying "dactyl_manuform_5x6_left-nice_nano_v2-zmk.uf2"</code> .</p></figcaption></figure>



### 5.3 🖥️Repeat for the Other Piece of the Keyboard

* Repeat Section 5.2 Steps 2 to 4 for the right piece of the keyboard.

### 5.4 🎊Woot you're done!

* Turn on the keyboard by clicking the on-off switch indicated by the green arrow in the figure below, then snap in the transparent plastic cover.
* If the switch button height lowers, it means it's now turned on. If the switch button height rises, it means it's now turned off.
* Since it's wireless, you no longer need to connect the USB cord or the audio cord. Turn on Bluetooth on your computer then pair with your keyboard.
* Charge the keyboard battery by connecting a piece of the keyboard to your computer via USB.

<figure><img src=".gitbook/assets/taikohub-dactyl-manuform-keyboard-legend-2 (1).jpg" alt=""><figcaption><p>Figure 5.3 The green arrow points to the on/off switch.</p></figcaption></figure>
