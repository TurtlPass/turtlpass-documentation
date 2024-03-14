---
description: >-
  This page explains how to utilize Argon2 for generating secure hashes on the
  client side.
---

# 🔐 Generating Secure Hash with Argon2

By following these steps, you can generate secure hashes using the Argon2 hashing algorithm on the client side, specifically tailored for use with the TurtlPass Firmware:

1.  **Install Required Libraries**: Ensure that you have the necessary libraries or packages installed in your development environment to utilize the Argon2 hashing algorithm. Depending on your programming language, you may need to install specific packages or modules. In Python, you can install the `argon2-cffi` library using pip:

    ```bash
    pip install argon2-cffi
    ```
2. **Define Input Data**: Determine the input data required for generating the secure hash. For TurtlPass Firmware, this typically includes the `Personal Identification Number (PIN)`, `DomainName`, and `AccountID`. These values are used to generate the secure hash and should be kept confidential.
3.  **Configure Argon2 Parameters**: Set up the Argon2 parameters according to the specifications used by the TurtlPass Firmware. These parameters include the number of iterations (`t_cost`), memory cost (`m_cost`), parallelism (`parallelism`), hash length (`hash_length`), and Argon2 version (`argon2_version`). The parameters used by TurtlPass Firmware are:

    | Parameter       | Value | Description                       |
    | --------------- | ----- | --------------------------------- |
    | T\_COST         | 32    | Number of iterations              |
    | PARALLELISM     | 4     | Number of threads in parallel     |
    | M\_COST         | 65536 | Memory cost in kibibytes (64 MiB) |
    | HASH\_LENGTH    | 64    | Hash length in bytes              |
    | ARGON2\_VERSION | ID    | Argon2 version (ID for Argon2i)   |
4. **Generate Salt**: Generate a salt value to increase the security of the hash. For TurtlPass Firmware, the salt is derived from the combination of `DomainName` and `AccountID` using the `SHA-512` hashing algorithm.
5. **Compute Hash Value**: Use the configured `Argon2` parameters and the input data to compute the hash value. Combine the input data and salt, then pass them to the Argon2 hashing function along with the parameters set in step 3.
6. **Use the Secure Hash**: The generated hash can now be used for various security-sensitive purposes within the TurtlPass Firmware, such as password generation or data encryption. Ensure that you handle the hash securely and do not expose it to unauthorized parties.
