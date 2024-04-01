# 💿 Flashing RP2040

## 1. INSTALL and setup `arduino-cli`

**Run the script** `1-click-setup.sh` to install automatically the `arduino-cli`, RP2040 boards, and all the libraries required.

## 2. SEED generation

**Run the script** `generate-seed.sh` to generate your unique seed on your local machine. The output file `Seed.cpp` will be added to your codebase.

**IMPORTANT**: Make sure you delete `turtlpass-firmware/Seed.cpp` file once you're done!

## 3. BUILD your custom TurtlPass Firmware

**Run the following command to compile the firmware to your RP2040 board:**

_Option A:_ If you have a touch sensor TTP-223 wired to the PIN `2`

```bash
$ arduino-cli compile --clean \
--fqbn "rp2040:rp2040:generic" \
--output-dir ../turtlpass-firmware/build/ \
--build-property "build.extra_flags=\"-D__TURTLPASS_VERSION__=\"2.0.0\"\"" \
--build-property "build.extra_flags=\"-D__TURTLPASS_PIN_TTP223__=2\"" \
../turtlpass-firmware/turtlpass-firmware.ino
```

_Option B:_ If you don't have a touch sensor TTP-223, fallback to built-in `BOOTSEL` button

```bash
$ arduino-cli compile --clean \
--fqbn "rp2040:rp2040:generic" \
--output-dir ../turtlpass-firmware/build/ \
--build-property "build.extra_flags=\"-D__TURTLPASS_VERSION__=\"2.0.0\"\"" \
../turtlpass-firmware/turtlpass-firmware.ino
```

## 4. UPLOAD TurtlPass Firmware to your RP2040 Board

**Run the following command to upload the firmware to your RP2040 board:**

`$ arduino-cli upload --fqbn "rp2040:rp2040:generic" -i ../turtlpass-firmware/build/turtlpass-firmware.ino.bin -p <PORT>`

_Example:_

```bash
$ arduino-cli upload \
--fqbn "rp2040:rp2040:generic" \
-i ../turtlpass-firmware/build/turtlpass-firmware.ino.bin \
-p /dev/cu.usbmodem14101
```

**IMPORTANT**: Make sure you delete `turtlpass-firmware/build/` directory once you're done!
