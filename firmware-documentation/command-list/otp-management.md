---
description: One-time passwords (aka One-time passcodes)
---

# 🔢 OTP Management

## ⏳ Get OTP Code

<pre class="language-plaintext"><code class="lang-plaintext"><strong>@[HASH]:[TIMESTAMP]
</strong></code></pre>

Retrieves the OTP code for the specified hash and current timestamp from the virtual EEPROM.

#### Command Example:

```plaintext
@4dff4ea340f0a823f15d3f4f01ab62eae0e5da579ccb851f8db9dfe84c58b2b37b89903a740e1ee172da793a6e79d560e5f7f9bd058a12a280433ed6fa46510a:1676821524
```

#### Success Response:

```
<OTP-READY>
```

Now touch the sensor on the device and it will automatically type the OTP code on the host machine, wherever the cursor/focus is on.

#### Error Response:

```
<OTP-ERROR>
```

Something went wrong. Double-check the input specification and try again.

## ➕ Add OTP Shared Secret

```plaintext
+[HASH]:[SECRET]
```

Adds a new OTP shared secret to the virtual EEPROM for the specified hash.

#### Example:

```plaintext
+4dff4ea340f0a823f15d3f4f01ab62eae0e5da579ccb851f8db9dfe84c58b2b37b89903a740e1ee172da793a6e79d560e5f7f9bd058a12a280433ed6fa46510a:ABCDEF0123456789ABCDEF0123456789
```

#### Success Response:

```
<OTP-ADDED>
```

#### Error Response:

```
<OTP-ERROR>
```

Something went wrong. Double-check the input specification and try again.

## 🖨️ Print All Encrypted OTP Secrets

```plaintext
?
```

Prints all encrypted OTP secrets stored in the virtual EEPROM.

#### Example Response:

```
Total Used Bytes: 40/4096
0:A8C02BC1:CD32D8B0D6625FF8B891DD1DD3C970F4FF421936FD73FAB1BAB86DAEB3345B3
```
