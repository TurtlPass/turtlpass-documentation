---
description: Flashing RP2040 with TurtlPass Firmware
---

# 💿 Installation Guide

## 1. INSTALL and setup `arduino-cli`

**Run the script** `1-click-setup.sh` to install automatically the `arduino-cli`, RP2040 boards, and all the libraries required.

{% hint style="info" %}
`$ ./1-click-setup.sh`
{% endhint %}

## 2. SEED generation

**Run the script** `generate-seed.sh` to generate your unique seed on your local machine. The output file `Seed.cpp` will be added to your codebase.

{% hint style="info" %}
`$ ./generate-seed.sh`
{% endhint %}

{% hint style="danger" %}
Make sure you delete `turtlpass-firmware/Seed.cpp` file once you're done with all the steps!
{% endhint %}

## 3. BUILD your custom TurtlPass Firmware

**Run one of the following commands to compile the firmware to your RP2040 board:**

<details>

<summary><em>Option A:</em> If you have a touch sensor TTP-223 wired to the PIN <code>2</code></summary>

```bash
arduino-cli compile --clean \
--fqbn "rp2040:rp2040:generic" \
--output-dir ../turtlpass-firmware/build/ \
--build-property "build.extra_flags=\"-D__TURTLPASS_VERSION__=\"2.1.0\"\"" \
--build-property "build.extra_flags=\"-D__TURTLPASS_PIN_TTP223__=2\"" \
../turtlpass-firmware/turtlpass-firmware.ino
```

</details>

<details>

<summary><em>Option B:</em> If you don't have a touch sensor TTP-223, fallback to built-in <code>BOOTSEL</code> button</summary>

```bash
arduino-cli compile --clean \
--fqbn "rp2040:rp2040:generic" \
--output-dir ../turtlpass-firmware/build/ \
--build-property "build.extra_flags=\"-D__TURTLPASS_VERSION__=\"2.1.0\"\"" \
../turtlpass-firmware/turtlpass-firmware.ino
```

</details>

## 4. UPLOAD TurtlPass Firmware to your RP2040 Board

**Run the following command to upload the firmware to your RP2040 board:**

{% hint style="info" %}
`$ arduino-cli upload --fqbn "rp2040:rp2040:generic" -i ../turtlpass-firmware/build/turtlpass-firmware.ino.bin -p <PORT>`
{% endhint %}

<details>

<summary>Example</summary>

```bash
arduino-cli upload \
--fqbn "rp2040:rp2040:generic" \
-i ../turtlpass-firmware/build/turtlpass-firmware.ino.bin \
-p /dev/cu.usbmodem14101
```

</details>

{% hint style="danger" %}
Make sure you delete `turtlpass-firmware/build/` directory once you're done!
{% endhint %}
