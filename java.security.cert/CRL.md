# CRL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CRL

```
abstract class CRL
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.CRL](../java/security/cert/CRL.md) |

| Known Direct Subclasses [X509CRL](../java/security/cert/X509CRL.md) |--------------------------------------------------------------------------------------|--------------------------| | [X509CRL](../java/security/cert/X509CRL.md) | Abstract class for an X. | |
| --- | --- | --- | --- | --- | --- | --- |

This class is an abstraction of certificate revocation lists (CRLs) that have different formats but important common uses. For example, all CRLs share the functionality of listing revoked certificates, and can be queried on whether or not they list a given certificate.

Specialized CRL types can be defined by subclassing off of this abstract class.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CRL](../java/security/cert/CRL.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a CRL of the specified type. |

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](../java/security/cert/CRL.md))`()` Returns the type of this CRL. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRevoked](../java/security/cert/CRL.md))`(`cert:` ` [Certificate](../java/security/cert/Certificate.md)!`)` Checks whether the given certificate is on this CRL. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/security/cert/CRL.md))`()` Returns a string representation of this CRL. |
| --- | --- |

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
| `cert` | [Certificate](../java/security/cert/Certificate.md)!:the certificate to check for. |

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
