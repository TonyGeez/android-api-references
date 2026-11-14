# Timestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Timestamp

```
class Timestamp : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.Timestamp](Timestamp.md) |

This class encapsulates information about a signed timestamp. It is immutable. It includes the timestamp's date and time as well as information about the Timestamping Authority (TSA) which generated and signed the timestamp.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Timestamp](Timestamp.md))`(`timestamp:` ` [Date](../java.util/Date.md)!`, `signerCertPath:` ` [CertPath](../java.security.cert/CertPath.md)!`)` Constructs a Timestamp. |

| Public methods ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Timestamp.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Tests for equality between the specified object and this timestamp. |
| [CertPath](../java.security.cert/CertPath.md)! | [getSignerCertPath](Timestamp.md))`()` Returns the certificate path for the Timestamping Authority. |
| [Date](../java.util/Date.md)! | [getTimestamp](Timestamp.md))`()` Returns the date and time when the timestamp was generated. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Timestamp.md))`()` Returns the hash code value for this timestamp. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Timestamp.md))`()` Returns a string describing this timestamp. |

## Public constructors

### Timestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Timestamp(
    timestamp: Date!, 
    signerCertPath: CertPath!)
```

Constructs a Timestamp.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `timestamp` | [Date](../java.util/Date.md)!:is the timestamp's date and time. It must not be null. |
| `signerCertPath` | [CertPath](../java.security.cert/CertPath.md)!:is the TSA's certificate path. It must not be null. |

| Exceptions ||
|----------------------------------|-----------------------------------------|
| `java.lang.NullPointerException` | if timestamp or signerCertPath is null. |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Tests for equality between the specified object and this timestamp. Two timestamps are considered equal if the date and time of their timestamp's and their signer's certificate paths are equal.

| Parameters ||
|-------|------------------------------------------------------|
| `obj` | the object to test for equality with this timestamp. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the timestamp are considered equal, false otherwise. |

### getSignerCertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSignerCertPath(): CertPath!
```

Returns the certificate path for the Timestamping Authority.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [CertPath](../java.security.cert/CertPath.md)! | The TSA's certificate path. |

### getTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimestamp(): Date!
```

Returns the date and time when the timestamp was generated.

| Return ||
|------------------------------------------------------------------------------|--------------------------------|
| [Date](../java.util/Date.md)! | The timestamp's date and time. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns the hash code value for this timestamp. The hash code is generated using the date and time of the timestamp and the TSA's certificate path.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this timestamp. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string describing this timestamp.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A string comprising the date and time of the timestamp and its signer's certificate. |
