# 10. Terminology

**Keycode:** The output after you press a keyswitch. For example, "Q" or "F11".

**Keymap:** Also called keyboard layout. Examples of keymaps include QWERTY, DVORAK, Colemak.

**Layers:**  Layers are a QMK specific functionality. The concept is similar to a Fn or FnLock key that is seen on some keyboards.

**Layer Key:** The keycode you use to switch to a different layer. If you are using QMK Configurator, you'll see M(0) or M(1). If you are following [customizing-keyboard-layout-for-linux-with-qmk.md](customizing-keyboard-layout-for-linux-with-qmk.md "mention"), you'll see the RAISE and LOWER layer keys in the default dactyl\_manuform/5x6 layout.

**QMK Toolbox:** A software tool used to flash a new layout onto your keyboard. It is available on Mac and Windows.

**Flashing:** Refers to when you install software onto your keyboard.

**QMK Configurator:** A website that allows you to create a custom keyboard layout and export the layout as a `.hex` file. This file is then used in QMK Toolbox.

**QMK CLI:** QMK's official command line interface tool.

**Microcontroller:** A microcontroller is a small device that controls your keyboard. Each piece of your keyboard comes with a Pro Micro microcontroller. You may come across it abbreviated as MCU, which stands for MicroController Unit.

**Firmware:** The software installed on microcontrollers to make your keyboard work. QMK firmware and ZMK firmware are examples.
