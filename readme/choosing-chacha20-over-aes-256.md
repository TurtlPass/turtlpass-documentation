---
description: >-
  In the realm of cryptography, selecting the right algorithm is crucial for
  ensuring security, performance, and ease of implementation. This page explores
  why ChaCha20 is preferred over AES-256.
---

# 🔐 Choosing ChaCha20 over AES-256

### Simplicity and Security

#### Simplicity

ChaCha20 is simpler to implement correctly compared to AES-256. AES requires complex and careful implementation to avoid side-channel attacks, especially on devices without dedicated hardware support for AES. ChaCha20, on the other hand, is designed to be secure even when implemented in software without needing specialized hardware.

#### Security

ChaCha20 offers a high level of security comparable to AES-256. Both algorithms provide robust encryption, but ChaCha20 has the added advantage of being resistant to certain types of cryptographic attacks that AES is vulnerable to when implemented poorly.

### Performance

#### Speed

ChaCha20 is designed to be fast and efficient on a wide range of hardware, including low-powered devices like those used in TurtlPass. It performs exceptionally well on CPUs without hardware acceleration for AES. Specifically, the RP2040 chip used in TurtlPass, with its Dual-core Arm Cortex-M0+ processor, benefits significantly from ChaCha20’s design, ensuring responsive performance even on resource-constrained devices.

#### Consistent Performance Across Platforms

ChaCha20 delivers consistent performance across different platforms, from high-end servers to embedded systems. This makes it a versatile choice for TurtlPass, ensuring that users experience fast encryption and decryption regardless of the device they are using.

### Resistance to Timing Attacks

ChaCha20 is specifically designed to be resistant to timing attacks. Timing attacks exploit variations in the time it takes to perform cryptographic operations to leak information about the keys or plaintext. ChaCha20's operations are constant-time, meaning they take the same amount of time regardless of the input, which significantly reduces the risk of timing attacks.

### Flexibility

ChaCha20 is highly flexible and is used in TurtlPass for various security functions, including:

* Encrypting shared keys for one-time passwords (OTPs)
* File encryption

This versatility allows TurtlPass to use ChaCha20 for multiple security functions, ensuring robust protection for all types of sensitive data.

### Proven and Trusted

ChaCha20 is a well-studied and trusted algorithm, standardized as RFC 8439. It is recommended by security experts and used by major organizations for various applications:

* **Google**: Implements ChaCha20 in its HTTPS connections for secure web traffic.
* **Cloudflare**: Uses ChaCha20 to provide fast and secure internet services.
* **OpenSSH**: Utilizes ChaCha20 for encrypting data in transit.
* **Linux Kernel**: Supports ChaCha20 for disk encryption and network security.

The widespread adoption and rigorous examination of ChaCha20 by the cryptographic community underscore its reliability and security.

### Conclusion

TurtlPass uses the ChaCha20 algorithm because it provides a perfect balance of simplicity, security, performance, and resistance to side-channel attacks. While AES-256 is also a strong encryption algorithm, ChaCha20's advantages make it the superior choice for ensuring that TurtlPass delivers the highest level of security and efficiency to its users.
