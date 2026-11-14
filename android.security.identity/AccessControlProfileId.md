Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessControlProfileId

```
open class AccessControlProfileId
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.identity.AccessControlProfileId](https://developer.android.com/reference/kotlin/android/security/identity/AccessControlProfileId#) |

> [!CAUTION]
> **This class was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

A class used to wrap an access control profile identifiers.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/identity/AccessControlProfileId#AccessControlProfileId(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a new object holding a numerical identifier. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/identity/AccessControlProfileId#getId()()` Gets the numerical identifier wrapped by this object. |

## Public constructors

### AccessControlProfileId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AccessControlProfileId(id: Int)
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Constructs a new object holding a numerical identifier.

The identifier must be a non-negative number and less than 32.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the identifier. |

## Public methods

### getId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getId(): Int
```

**Deprecated:** *Use `java.security.KeyStore` with the Android hardware-backed keystore instead.*

Gets the numerical identifier wrapped by this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the identifier. |
