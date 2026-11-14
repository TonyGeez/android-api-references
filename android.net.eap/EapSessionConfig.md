Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EapSessionConfig

```
class EapSessionConfig
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.eap.EapSessionConfig](../android/net/eap/EapSessionConfig.md) |

EapSessionConfig represents a container for EAP method configuration.

The EAP authentication server decides which EAP method is used, so clients are encouraged to provide configs for several EAP methods.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.Builder` This class can be used to incrementally construct an `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig#`. |
| | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapAkaConfig` EapAkaConfig represents the configs needed for an EAP AKA session. |
| | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapAkaOption` EapAkaOption represents optional configurations for EAP AKA authentication. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapAkaPrimeConfig` EapAkaPrimeConfig represents the configs needed for an EAP-AKA' session. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapMethodConfig` EapMethodConfig represents a generic EAP method configuration. |
| | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapMsChapV2Config` EapMsChapV2Config represents the configs needed for an EAP MSCHAPv2 session. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapSimConfig` EapSimConfig represents the configs needed for an EAP SIM session. |
| | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapTtlsConfig` EapTtlsConfig represents the configs needed for an EAP-TTLS session. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [EapSessionConfig.EapAkaConfig](../android/net/eap/EapSessionConfig.EapAkaConfig.md)? | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig#getEapAkaConfig()()` Retrieves configuration for EAP AKA |
| [EapSessionConfig.EapAkaPrimeConfig](../android/net/eap/EapSessionConfig.EapAkaPrimeConfig.md)? | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig#getEapAkaPrimeConfig()()` Retrieves configuration for EAP AKA' |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig#getEapIdentity()()` Retrieves client's EAP Identity |
| [EapSessionConfig.EapMsChapV2Config](../android/net/eap/EapSessionConfig.EapMsChapV2Config.md)? | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig#getEapMsChapV2Config()()` Retrieves configuration for EAP MSCHAPV2 |
| [EapSessionConfig.EapSimConfig](../android/net/eap/EapSessionConfig.EapSimConfig.md)? | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig#getEapSimConfig()()` Retrieves configuration for EAP SIM |
| --- | --- |
| [EapSessionConfig.EapTtlsConfig](../android/net/eap/EapSessionConfig.EapTtlsConfig.md)? | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig#getEapTtlsConfig()()` Retrieves configuration for EAP-TTLS |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig#hashCode()()` Returns a hash code value for the object. |

## Public methods

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getEapAkaConfig

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEapAkaConfig(): EapSessionConfig.EapAkaConfig?
```

Retrieves configuration for EAP AKA

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapAkaConfig?` | the configuration for EAP AKA, or null if it was not set |

### getEapAkaPrimeConfig

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEapAkaPrimeConfig(): EapSessionConfig.EapAkaPrimeConfig?
```

Retrieves configuration for EAP AKA'

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapAkaPrimeConfig?` | the configuration for EAP AKA', or null if it was not set |

### getEapIdentity

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEapIdentity(): ByteArray
```

Retrieves client's EAP Identity

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | This value cannot be `null`. |

### getEapMsChapV2Config

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEapMsChapV2Config(): EapSessionConfig.EapMsChapV2Config?
```

Retrieves configuration for EAP MSCHAPV2

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapMsChapV2Config?` | the configuration for EAP MSCHAPV2, or null if it was not set |

### getEapSimConfig

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEapSimConfig(): EapSessionConfig.EapSimConfig?
```

Retrieves configuration for EAP SIM

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapSimConfig?` | the configuration for EAP SIM, or null if it was not set |

### getEapTtlsConfig

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEapTtlsConfig(): EapSessionConfig.EapTtlsConfig?
```

Retrieves configuration for EAP-TTLS

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapTtlsConfig?` | the configuration for EAP-TTLS, or null if it was not set |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
