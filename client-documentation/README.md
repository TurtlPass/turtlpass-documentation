# 🖥️ Client Documentation

To interact with the TurtlPass Firmware securely, clients need to send commands along with a secure hash of the relevant inputs. Argon2 is a highly recommended hashing algorithm due to its resistance against various types of attacks, including brute-force and dictionary attacks. By leveraging Argon2, clients can ensure the highest level of security for their hashed inputs during transmission over USB serial communication.\


## Client app Available on

<details>

<summary>Android</summary>

Source code: [https://github.com/TurtlPass/turtlpass-android](https://github.com/TurtlPass/turtlpass-android)

Preview:

![](<../.gitbook/assets/TurtlPass Android how-to.gif>)

</details>

<details>

<summary>Chrome Extension</summary>

Source code: [https://github.com/TurtlPass/turtlpass-chrome-extension](https://github.com/TurtlPass/turtlpass-chrome-extension)

Preview:

![](<../.gitbook/assets/TurtlPass Chrome Extension.gif>)

</details>

<details>

<summary>Python (Command-Line Interface)</summary>

Source code: [https://github.com/TurtlPass/turtlpass-python](https://github.com/TurtlPass/turtlpass-python)

Preview:

```
                               ___-------___
                           _-~~             ~~-_
                        _-~                    /~-_
     /^\__/^\         /~  \                   /    \
   /|  O|| O|        /      \_______________/        \
  | |___||__|      /       /                \          \
  |          \    /      /                    \          \
  |   (_______) /______/                        \_________ \
  |         / /         \                      /            \
   \         \^\\         \                  /               \     /
     \         ||           \______________/      _-_       //\__//
       \       ||------_-~~-_ ------------- \ --/~   ~\    || __/
         ~-----||====/~     |==================|       |/~~~~~
          (_(__/  ./     /                    \_\      \.
                 (_(___/                         \_____)_)   [art by jurcy]

████████╗██╗░░░██╗██████╗░████████╗██╗░░░░░██████╗░░█████╗░░██████╗░██████╗
╚══██╔══╝██║░░░██║██╔══██╗╚══██╔══╝██║░░░░░██╔══██╗██╔══██╗██╔════╝██╔════╝
░░░██║░░░██║░░░██║██████╔╝░░░██║░░░██║░░░░░██████╔╝███████║╚█████╗░╚█████╗░
░░░██║░░░██║░░░██║██╔══██╗░░░██║░░░██║░░░░░██╔═══╝░██╔══██║░╚═══██╗░╚═══██╗
░░░██║░░░╚██████╔╝██║░░██║░░░██║░░░███████╗██║░░░░░██║░░██║██████╔╝██████╔╝
░░░╚═╝░░░░╚═════╝░╚═╝░░╚═╝░░░╚═╝░░░╚══════╝╚═╝░░░░░╚═╝░░╚═╝╚═════╝░╚═════╝░
Welcome to TurtlPass!
Device detected: /dev/cu.usbmodem14101
Options:
0. Exit
1. Get Device Information
2. Generate Password
3. Generate OTP Code
4. Add OTP Shared Secret
5. Get Encrypted OTP Secrets
6. Encrypt File
7. Decrypt File
8. Encrypt Image (experimental)
9. Decrypt Image (experimental)
Select an option:
```

</details>
