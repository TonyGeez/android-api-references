# CRL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CRL

```
abstract class CRL
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.cert.CRL](https://developer.android.com/reference/kotlin/java/security/cert/CRL#) |

| Known Direct Subclasses [X509CRL](https://developer.android.com/reference/kotlin/java/security/cert/X509CRL) |--------------------------------------------------------------------------------------|--------------------------| | [X509CRL](https://developer.android.com/reference/kotlin/java/security/cert/X509CRL) | Abstract class for an X. | |

This class is an abstraction of certificate revocation lists (CRLs) that have different formats but important common uses. For example, all CRLs share the functionality of listing revoked certificates, and can be queried on whether or not they list a given certificate.

Specialized CRL types can be defined by subclassing off of this abstract class.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CRL](https://developer.android.com/reference/kotlin/java/security/cert/CRL#CRL(kotlin.String))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a CRL of the specified type. |

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/java/security/cert/CRL#getType())`()` Returns the type of this CRL. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRevoked](https://developer.android.com/reference/kotlin/java/security/cert/CRL#isRevoked(java.security.cert.Certificate))`(`cert:` ` [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!`)` Checks whether the given certificate is on this CRL. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/cert/CRL#toString())`()` Returns a string representation of this CRL. |

## Protected constructors

### CRL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CRL(type: String!)
```

Creates a CRL of the specified type.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the CRL type. See the [Java Security Standard Algorithm Names](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html) document for information about standard CRL types. |

## Public methods

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): String!
```

Returns the type of this CRL.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the type of this CRL. |

### isRevoked

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isRevoked(cert: Certificate!): Boolean
```

Checks whether the given certificate is on this CRL.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `cert` | [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!:the certificate to check for. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the given certificate is on this CRL, false otherwise. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toString(): String
```

Returns a string representation of this CRL.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this CRL. |
