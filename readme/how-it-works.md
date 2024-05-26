# 🚀 How it Works

Using our client app (available on [Android](https://github.com/TurtlPass/turtlpass-android), as a [Chrome Extension](https://github.com/TurtlPass/turtlpass-chrome-extension), or the [Python CLI](https://github.com/TurtlPass/turtlpass-python)), you simply select the **App** or **Domain n**ame, enter your **Account** ID (typically your email), and choose a **PIN** code. Every time you want to change the password, just use a different PIN. The PIN is never stored anywhere and is the only thing you need to memorize.

A hash of your inputs is sent via USB serial to the TurtlPass device, which uses a deterministic key derivation function (KDF) to generate a 100-character password combining lowercase and uppercase letters, along with numbers.

Once you touch the sensor on the TurtlPass device, the generated password is automatically typed using a virtual keyboard.
