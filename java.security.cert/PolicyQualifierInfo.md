# PolicyQualifierInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PolicyQualifierInfo

```
open class PolicyQualifierInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.PolicyQualifierInfo](https://developer.android.com/reference/kotlin/java/security/cert/PolicyQualifierInfo#) |

An immutable policy qualifier represented by the ASN.1 PolicyQualifierInfo structure.

The ASN.1 definition is as follows: 

```kotlin
PolicyQualifierInfo ::= SEQUENCE {
         policyQualifierId       PolicyQualifierId,
         qualifier               ANY DEFINED BY policyQualifierId }
  
```

A certificate policies extension, if present in an X.509 version 3 certificate, contains a sequence of one or more policy information terms, each of which consists of an object identifier (OID) and optional qualifiers. In an end-entity certificate, these policy information terms indicate the policy under which the certificate has been issued and the purposes for which the certificate may be used. In a CA certificate, these policy information terms limit the set of policies for certification paths which include this certificate.

A`Set`of`PolicyQualifierInfo`objects are returned by the [PolicyNode.getPolicyQualifiers](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode#getPolicyQualifiers())method. This allows applications with specific policy requirements to process and validate each policy qualifier. Applications that need to process policy qualifiers should explicitly set the`policyQualifiersRejected`flag to false (by calling the [PKIXParameters.setPolicyQualifiersRejected](https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setPolicyQualifiersRejected(kotlin.Boolean))method) before validating a certification path.

Note that the PKIX certification path validation algorithm specifies that any policy qualifier in a certificate policies extension that is marked critical must be processed and validated. Otherwise the certification path must be rejected. If the`policyQualifiersRejected`flag is set to false, it is up to the application to validate all policy qualifiers in this manner in order to be PKIX compliant.

**Concurrent Access**

All`PolicyQualifierInfo`objects must be immutable and thread-safe. That is, multiple threads may concurrently invoke the methods defined in this class on a single`PolicyQualifierInfo`object (or more than one) with no ill effects. Requiring`PolicyQualifierInfo`objects to be immutable and thread-safe allows them to be passed around to various pieces of code without worrying about coordinating access.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PolicyQualifierInfo](https://developer.android.com/reference/kotlin/java/security/cert/PolicyQualifierInfo#PolicyQualifierInfo(kotlin.ByteArray))`(`encoded:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates an instance of`PolicyQualifierInfo`from the encoded bytes. |

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](https://developer.android.com/reference/kotlin/java/security/cert/PolicyQualifierInfo#getEncoded())`()` Returns the ASN. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getPolicyQualifier](https://developer.android.com/reference/kotlin/java/security/cert/PolicyQualifierInfo#getPolicyQualifier())`()` Returns the ASN. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPolicyQualifierId](https://developer.android.com/reference/kotlin/java/security/cert/PolicyQualifierInfo#getPolicyQualifierId())`()` Returns the`policyQualifierId`field of this`PolicyQualifierInfo`. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/cert/PolicyQualifierInfo#toString())`()` Return a printable representation of this`PolicyQualifierInfo`. |

## Public constructors

### PolicyQualifierInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PolicyQualifierInfo(encoded: ByteArray!)
```

Creates an instance of`PolicyQualifierInfo`from the encoded bytes. The encoded byte array is copied on construction.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `encoded` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array containing the qualifier in DER encoding |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------|
| `java.io.IOException` | thrown if the byte array does not represent a valid and parsable policy qualifier |

## Public methods

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEncoded(): ByteArray!
```

Returns the ASN.1 DER encoded form of this`PolicyQualifierInfo`.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the ASN.1 DER encoded bytes (never`null`). Note that a copy is returned, so the data is cloned each time this method is called. |

### getPolicyQualifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPolicyQualifier(): ByteArray!
```

Returns the ASN.1 DER encoded form of the`qualifier`field of this`PolicyQualifierInfo`.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the ASN.1 DER encoded bytes of the`qualifier`field. Note that a copy is returned, so the data is cloned each time this method is called. |

### getPolicyQualifierId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPolicyQualifierId(): String!
```

Returns the`policyQualifierId`field of this`PolicyQualifierInfo`. The`policyQualifierId`is an Object Identifier (OID) represented by a set of nonnegative integers separated by periods.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the OID (never`null`) |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Return a printable representation of this`PolicyQualifierInfo`.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a`String`describing the contents of this`PolicyQualifierInfo` |
