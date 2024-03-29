---
description: >-
  Where Passwords Swim Securely! Unleash Peace of Mind with Turtle-Approved
  Wisdom. Protecting You, Saving Turtles. 🐢💻
---

# 🐢 TurtlPass

<div align="center">

<img src=".gitbook/assets/turtlpass-header.jpg" alt="">

</div>

[![Firmware Repo](https://img.shields.io/github/v/release/TurtlPass/turtlpass-firmware-arduino?color=blue\&label=Arduino%20Firmware\&logo=arduino)](https://github.com/TurtlPass/turtlpass-firmware-arduino) [![Android Repo](https://img.shields.io/github/v/release/TurtlPass/turtlpass-android?color=blue\&label=Android%20App\&logo=android)](https://github.com/TurtlPass/turtlpass-android) [![Chrome Extension Repo](https://img.shields.io/github/v/release/TurtlPass/turtlpass-chrome-extension?color=blue\&label=Chrome%20Extension\&logo=googlechrome)](https://github.com/TurtlPass/turtlpass-chrome-extension)

## ⚡ Features

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
  * Speed: \~80 kB/s @ 133 Mhz

## 🚀 How it Works

Using the client app ([Android](https://github.com/TurtlPass/turtlpass-android), [Chrome Extension](https://github.com/TurtlPass/turtlpass-chrome-extension), or the [Python CLI](https://github.com/TurtlPass/turtlpass-python)) select the **App** or **Domain Name** you want to generate a password for, enter your **Account ID** (typically your email), and **choose a PIN** code. Every time you want to change the password, you just need to use a different PIN. The PIN is never stored anywhere and is the only thing you need to memorize in the entire process.

A **hash of the inputs** is **sent via USB serial** to the TurtlPass device that then uses a deterministic key derivation function (**KDF**) to generate a **100-character password** that includes a combination of lowercase and uppercase letters, as well as numbers.

Once you **touch the sensor** on the TurtlPass device, the generated **password is typed automatically** using a virtual keyboard.

### 🔑 TurtlPass ≠ FIDO

TurtlPass is **not** a **FIDO** Security Key and does **not** intend to be one. If you're looking for that, check [pico-fido](https://github.com/polhenarejos/pico-fido) project. **TurtlPass** is intended for **all the other websites/apps** that don't support hardware security keys, the ones with a `password` field :)
