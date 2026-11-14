# URICertStoreParameters

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# URICertStoreParameters

```
class URICertStoreParameters : CertStoreParameters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.URICertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/URICertStoreParameters#) |

Parameters used as input for`CertStore`algorithms which use information contained in a URI to retrieve certificates and CRLs.

This class is used to provide necessary configuration parameters through a URI as defined in RFC 5280 to implementations of`CertStore`algorithms.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [URICertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/URICertStoreParameters#URICertStoreParameters(java.net.URI))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!`)` Creates an instance of`URICertStoreParameters`with the specified URI. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [URICertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/URICertStoreParameters#) | [clone](https://developer.android.com/reference/kotlin/java/security/cert/URICertStoreParameters#clone())`()` Returns a copy of this object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/security/cert/URICertStoreParameters#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified object with this parameters object for equality. |
| [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)! | [getURI](https://developer.android.com/reference/kotlin/java/security/cert/URICertStoreParameters#getURI())`()` Returns the URI used to construct this`URICertStoreParameters`object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/security/cert/URICertStoreParameters#hashCode())`()` Returns a hash code value for this parameters object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/cert/URICertStoreParameters#toString())`()` Returns a formatted string describing the parameters including the URI used to construct this object. |

## Public constructors

### URICertStoreParameters

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
URICertStoreParameters(uri: URI!)
```

Creates an instance of`URICertStoreParameters`with the specified URI.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!:the URI which contains configuration information. |

| Exceptions ||
|----------------------------------|----------------|
| `java.lang.NullPointerException` | if`uri`is null |

## Public methods

### clone

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clone(): URICertStoreParameters
```

Returns a copy of this object. Changes to the copy will not affect the original and vice versa.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|----------|
| [URICertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/URICertStoreParameters#) | the copy |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares the specified object with this parameters object for equality. Two URICertStoreParameters are considered equal if the URIs used to construct them are equal.

| Parameters ||
|-------|-------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `p` | the object to test for equality with this parameters. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified object is equal to this parameters object. |

### getURI

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getURI(): URI!
```

Returns the URI used to construct this`URICertStoreParameters`object.

| Return ||
|---------------------------------------------------------------------------|----------|
| [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)! | the URI. |

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for this parameters object. The hash code is generated using the URI supplied at construction.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this parameters. |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a formatted string describing the parameters including the URI used to construct this object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a formatted string describing the parameters |
