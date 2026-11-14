Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EphemeralPublicKeyNotFoundException

```
open class EphemeralPublicKeyNotFoundException : IdentityCredentialException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [android.security.identity.IdentityCredentialException](IdentityCredentialException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.security.identity.EphemeralPublicKeyNotFoundException](EphemeralPublicKeyNotFoundException.md) |

> [!CAUTION]
> **This exception was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

Thrown if the ephemeral public key was not found in the session transcript passed to getEntries.

## Summary

| Public constructors ||
|---|---|
| EphemeralPublicKeyNotFoundException Constructs a new EphemeralPublicKeyNotFoundException exception. |
| EphemeralPublicKeyNotFoundException Constructs a new EphemeralPublicKeyNotFoundException exception. |

## Public constructors

### EphemeralPublicKeyNotFoundException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
EphemeralPublicKeyNotFoundException(message: String)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new EphemeralPublicKeyNotFoundException exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |

### EphemeralPublicKeyNotFoundException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
EphemeralPublicKeyNotFoundException(
    message: String, 
    cause: Throwable)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new EphemeralPublicKeyNotFoundException exception.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the detail message. This value cannot be `null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html): the cause. This value cannot be `null`. |
