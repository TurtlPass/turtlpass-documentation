---
description: ChaCha20 algorithm
---

# 🗃️ Hardware Encryption

## 🔒 Encrypt

```plaintext
>[HASH]

<byte> <byte> ...
```

Encrypts the bytes sent. The encryption process stops after `300`ms of inactivity.

#### Response:

```
<encrypted-byte> <encrypted-byte> ...
```

#### Example:

```plaintext
>4dff4ea340f0a823f15d3f4f01ab62eae0e5da579ccb851f8db9dfe84c58b2b37b89903a740e1ee172da793a6e79d560e5f7f9bd058a12a280433ed6fa46510a
```

## 🔓 Decrypt

```plaintext
<[HASH]

<encrypted-byte> <encrypted-byte> ...
```

Decrypts the bytes sent. The decryption process stops after `300`ms of inactivity.

#### Response:

```
<decrypted-byte> <decrypted-byte> ...
```

#### Example:

```plaintext
<4dff4ea340f0a823f15d3f4f01ab62eae0e5da579ccb851f8db9dfe84c58b2b37b89903a740e1ee172da793a6e79d560e5f7f9bd058a12a280433ed6fa46510a
```
