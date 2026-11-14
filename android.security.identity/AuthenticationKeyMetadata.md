Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AuthenticationKeyMetadata

```
class AuthenticationKeyMetadata
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.identity.AuthenticationKeyMetadata](AuthenticationKeyMetadata.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

Data about authentication keys.

## Summary

| Public methods ||
|---|---|
| [Instant](../java.time/Instant.md) | getExpirationDate Gets expiration date for the authentication key. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getUsageCount Gets usage count for the authentication key. |

## Public methods

### getExpirationDate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExpirationDate(): Instant
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets expiration date for the authentication key.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | the expiration date of the authentication key. This value cannot be `null`. |

### getUsageCount

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUsageCount(): Int
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets usage count for the authentication key.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the usage count. Value is 0 or greater |
