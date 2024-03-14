# 🖥️ Client Documentation

To interact with the TurtlPass Firmware securely, clients need to send commands along with a secure hash of the relevant inputs. Argon2 is a highly recommended hashing algorithm due to its resistance against various types of attacks, including brute-force and dictionary attacks. By leveraging Argon2, clients can ensure the highest level of security for their hashed inputs during transmission over USB serial communication.\
