# CodeSigner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CodeSigner

```
class CodeSigner : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.CodeSigner](CodeSigner.md) |

This class encapsulates information about a code signer. It is immutable.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CodeSigner](CodeSigner.md))`(`signerCertPath:` ` [CertPath](../java.security.cert/CertPath.md)!`, `timestamp:` ` [Timestamp](Timestamp.md)!`)` Constructs a CodeSigner object. |

| Public methods ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](CodeSigner.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Tests for equality between the specified object and this code signer. |
| [CertPath](../java.security.cert/CertPath.md)! | [getSignerCertPath](CodeSigner.md))`()` Returns the signer's certificate path. |
| [Timestamp](Timestamp.md)! | [getTimestamp](CodeSigner.md))`()` Returns the signature timestamp. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](CodeSigner.md))`()` Returns the hash code value for this code signer. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](CodeSigner.md))`()` Returns a string describing this code signer. |

## Public constructors

### CodeSigner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CodeSigner(
    signerCertPath: CertPath!, 
    timestamp: Timestamp!)
```

Constructs a CodeSigner object.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `signerCertPath` | [CertPath](../java.security.cert/CertPath.md)!:The signer's certificate path. It must not be`null`. |
| `timestamp` | [Timestamp](Timestamp.md)!:A signature timestamp. If`null`then no timestamp was generated for the signature. |

| Exceptions ||
|----------------------------------|-----------------------------|
| `java.lang.NullPointerException` | if`signerCertPath`is`null`. |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Tests for equality between the specified object and this code signer. Two code signers are considered equal if their signer certificate paths are equal and if their timestamps are equal, if present in both.

| Parameters ||
|-------|---------------------------------------------------|
| `obj` | the object to test for equality with this object. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the objects are considered equal, false otherwise. |

### getSignerCertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSignerCertPath(): CertPath!
```

Returns the signer's certificate path.

| Return ||
|-----------------------------------------------------------------------------------------|---------------------|
| [CertPath](../java.security.cert/CertPath.md)! | A certificate path. |

### getTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimestamp(): Timestamp!
```

Returns the signature timestamp.

| Return ||
|--------------------------------------------------------------------------------------|-------------------------------------------|
| [Timestamp](Timestamp.md)! | The timestamp or`null`if none is present. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns the hash code value for this code signer. The hash code is generated using the signer's certificate path and the timestamp, if present.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this code signer. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string describing this code signer.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A string comprising the signer's certificate and a timestamp, if present. |
