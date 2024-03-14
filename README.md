# 🐢 TurtlPass

<div align="center">

<img src="https://raw.githubusercontent.com/TurtlPass/turtlpass-firmware-arduino/main/assets/icon.png" alt="" width="128">

</div>

## TurtlPass: Where Passwords Swim Securely! Unleash Peace of Mind with Turtle-Approved Wisdom. Protecting You, Saving Turtles. 🐢💻

[![Firmware Repo](https://img.shields.io/github/v/release/TurtlPass/turtlpass-firmware-arduino?color=blue\&label=Arduino%20Firmware\&logo=arduino)](https://github.com/TurtlPass/turtlpass-firmware-arduino) [![Android Repo](https://img.shields.io/github/v/release/TurtlPass/turtlpass-android?color=blue\&label=Android%20App\&logo=android)](https://github.com/TurtlPass/turtlpass-android) [![Chrome Extension Repo](https://img.shields.io/github/v/release/TurtlPass/turtlpass-chrome-extension?color=blue\&label=Chrome%20Extension\&logo=googlechrome)](https://github.com/TurtlPass/turtlpass-chrome-extension)

## ⚡ TurtlPass Features

* **Hardware Password Generator**
  * Unlimited passwords are generated on the device
  * Passwords are 100 characters long, including a combination of lowercase and uppercase letters, as well as numbers
  * Automatically types the password for you, so you don't have to
* **Hardware 2FA Manager**
  * One-time passwords (OTP) are generated on the device&#x20;
  * Automatically types the OTP code whenever you're ready
  * Shared secrets are encrypted with `AES-256` in the virtual `EEPROM`
* **Hardware Encryption**
  * Files encrypted on the device using the `ChaCha20` algorithm

### 🔑 TurtlPass ≠ FIDO

TurtlPass is **not** a **FIDO** Security Key and does **not** intend to be one. If you're looking for that, check [pico-fido](https://github.com/polhenarejos/pico-fido) project. **TurtlPass** is intended for **all the other websites/apps** that don't support hardware security keys, the ones with a `password` field :)
