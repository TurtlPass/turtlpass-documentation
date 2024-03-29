# 🔑 Password Generation

### Input Specification

* Command syntax:
  * Hash length must be between 1 and 128 characters.
  * Hash must consist only of hexadecimal digits (0-9, A-F, a-f).
* Commands must be newline-terminated.

## 🔑 Generate a Password based on the provided Hash input

<pre class="language-plaintext"><code class="lang-plaintext"><strong>/[HASH]
</strong></code></pre>

#### Command Example:

```plaintext
/4dff4ea340f0a823f15d3f4f01ab62eae0e5da579ccb851f8db9dfe84c58b2b37b89903a740e1ee172da793a6e79d560e5f7f9bd058a12a280433ed6fa46510a
```

#### Success Response:

```
<PASSWORD-READY>
```

Now touch the sensor on the device and it will automatically type the generated password on the host machine, wherever the cursor/focus is on.

#### Error Response:

```
<PASSWORD-ERROR>
```

Something went wrong. Double-check the input specification and try again.
