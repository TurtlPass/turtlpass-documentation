# 🛣️ Roadmap

## ✅ Released / Done

#### \[HARDWARE]

* Support for **RP2040-**_**based**_** hardware**
  * Raspberry Pi Pico (RP2040)
  * Adafruit Trinkey QT2040
  * Waveshare RP2040-Zero
  * Generic RP2040
* Touch Sensor (TTP-223)

#### \[FIRMWARE]

* Features
  * **Password Generation**
  * **2FA Management**
  * **File Encryption**

#### \[CLIENTS]

* **Android** (Kotlin & Jetpack Compose)
* **Chrome Extension** (JavaScript)
* **Command-line interface** (Python)

***

## 🚀 Future / Analysing:

#### \[HARDWARE]

* **Touch Display**
  * Design and implement UI/UX for rounded screen
* **Work standalone** (w/o client app)
  * Most common services logo vectors built-in (Facebook, Amazon, etc.)
* **Persist in EEPROM a log**/history of the last `N` operations
  * Example: Password for Facebook with user Alice; OTP code for Amazon with user Bob;

#### \[FIRMWARE]

* Refactor serial communication to transmit structured data serialized with [Protocol Buffers](https://protobuf.dev)
* Post-Quantum Key Encapsulation Mechanism (KEM) for encrypted comms with client apps
  * [Post-Quantum Key Encapsulation](https://blog.cloudflare.com/post-quantum-key-encapsulation)
  * [Post-Quantum for All](https://blog.cloudflare.com/post-quantum-for-all)

#### \[CLIENTS]

* **Migrate** TurtlPass Android project **to** **Kotlin & Compose Multiplatform**
* **Migrate** to **libraries** with Kotlin Multiplatform support
* **TurtlPass Client monorepo** (Android, Browser-extension & more later)
* **Add support to Web & Desktop**
  * Needs a different UI/UX since Chrome or Android APIs aren't available here
* **Add support to iOS**
  * Write custom iOS logic to fetch installed apps
