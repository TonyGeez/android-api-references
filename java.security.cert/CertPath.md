# CertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPath

```
abstract class CertPath : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath#) |

An immutable sequence of certificates (a certification path).

This is an abstract class that defines the methods common to all`CertPath`s. Subclasses can handle different kinds of certificates (X.509, PGP, etc.).

All`CertPath`objects have a type, a list of`Certificate`s, and one or more supported encodings. Because the`CertPath`class is immutable, a`CertPath`cannot change in any externally visible way after being constructed. This stipulation applies to all public fields and methods of this class and any added or overridden by subclasses.

The type is a`String`that identifies the type of`Certificate`s in the certification path. For each certificate`cert`in a certification path`certPath`,`cert.getType().equals(certPath.getType())`must be`true`.

The list of`Certificate`s is an ordered`List`of zero or more`Certificate`s. This`List`and all of the`Certificate`s contained in it must be immutable.

Each`CertPath`object must support one or more encodings so that the object can be translated into a byte array for storage or transmission to other parties. Preferably, these encodings should be well-documented standards (such as PKCS#7). One of the encodings supported by a`CertPath`is considered the default encoding. This encoding is used if no encoding is explicitly requested (for the [getEncoded()](https://developer.android.com/reference/kotlin/java/security/cert/CertPath#getEncoded())method, for instance).

All`CertPath`objects are also`Serializable`.`CertPath`objects are resolved into an alternate [CertPathRep](https://developer.android.com/reference/kotlin/java/security/cert/CertPath.CertPathRep) object during serialization. This allows a`CertPath`object to be serialized into an equivalent representation regardless of its underlying implementation.

`CertPath`objects can be created with a`CertificateFactory`or they can be returned by other classes, such as a`CertPathBuilder`.

By convention, X.509`CertPath`s (consisting of`X509Certificate`s), are ordered starting with the target certificate and ending with a certificate issued by the trust anchor. That is, the issuer of one certificate is the subject of the following one. The certificate representing the [TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor) should not be included in the certification path. Unvalidated X.509`CertPath`s may not follow these conventions. PKIX`CertPathValidator`s will detect any departure from these conventions that cause the certification path to be invalid and throw a`CertPathValidatorException`.

Every implementation of the Java platform is required to support the following standard`CertPath`encodings:

- `PKCS7`
- `PkiPath`

These encodings are described in the [CertPath Encodings section](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certpath-encodings) of the Java Security Standard Algorithm Names Specification. Consult the release documentation for your implementation to see if any other encodings are supported.

**Concurrent Access**

All`CertPath`objects must be thread-safe. That is, multiple threads may concurrently invoke the methods defined in this class on a single`CertPath`object (or more than one) with no ill effects. This is also true for the`List`returned by`CertPath.getCertificates`.

Requiring`CertPath`objects to be immutable and thread-safe allows them to be passed around to various pieces of code without worrying about coordinating access. Providing this thread-safety is generally not difficult, since the`CertPath`and`List`objects in question are immutable.

## Summary

| Nested classes ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [CertPathRep](https://developer.android.com/reference/kotlin/java/security/cert/CertPath.CertPathRep) Alternate`CertPath`class for serialization. |

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath#CertPath(kotlin.String))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`CertPath`of the specified type. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/security/cert/CertPath#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this certification path for equality with the specified object. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!\>! | [getCertificates](https://developer.android.com/reference/kotlin/java/security/cert/CertPath#getCertificates())`()` Returns the list of certificates in this certification path. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](https://developer.android.com/reference/kotlin/java/security/cert/CertPath#getEncoded())`()` Returns the encoded form of this certification path, using the default encoding. |
| --- | --- |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](https://developer.android.com/reference/kotlin/java/security/cert/CertPath#getEncoded(kotlin.String))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the encoded form of this certification path, using the specified encoding. |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getEncodings](https://developer.android.com/reference/kotlin/java/security/cert/CertPath#getEncodings())`()` Returns an iteration of the encodings supported by this certification path, with the default encoding first. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/java/security/cert/CertPath#getType())`()` Returns the type of`Certificate`s in this certification path. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/security/cert/CertPath#hashCode())`()` Returns the hashcode for this certification path. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/cert/CertPath#toString())`()` Returns a string representation of this certification path. |

| Protected methods ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [writeReplace](https://developer.android.com/reference/kotlin/java/security/cert/CertPath#writeReplace())`()` Replaces the`CertPath`to be serialized with a`CertPathRep`object. |

## Protected constructors

### CertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CertPath(type: String!)
```

Creates a`CertPath`of the specified type.

This constructor is protected because most users should use a`CertificateFactory`to create`CertPath`s.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the type of`Certificate`s in this path |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this certification path for equality with the specified object. Two`CertPath`s are equal if and only if their types are equal and their certificate`List`s (and by implication the`Certificate`s in those`List`s) are equal. A`CertPath`is never equal to an object that is not a`CertPath`.

This algorithm is implemented by this method. If it is overridden, the behavior specified here must be maintained.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object to test for equality with this certification path |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified object is equal to this certification path, false otherwise |

### getCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCertificates(): MutableList<out Certificate!>!
```

Returns the list of certificates in this certification path. The`List`returned must be immutable and thread-safe.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!>! | an immutable`List`of`Certificate`s (may be empty, but not null) |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncoded(): ByteArray!
```

Returns the encoded form of this certification path, using the default encoding.

| Return ||
|------------------------------------------------------------------------------------------|-------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the encoded bytes |

| Exceptions ||
|---------------------------------------------------|-----------------------------|
| `java.security.cert.CertificateEncodingException` | if an encoding error occurs |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncoded(encoding: String!): ByteArray!
```

Returns the encoded form of this certification path, using the specified encoding.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------|
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the encoding to use |

| Return ||
|------------------------------------------------------------------------------------------|-------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the encoded bytes |

| Exceptions ||
|---------------------------------------------------|------------------------------------------------------------------------|
| `java.security.cert.CertificateEncodingException` | if an encoding error occurs or the encoding requested is not supported |

### getEncodings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncodings(): MutableIterator<String!>!
```

Returns an iteration of the encodings supported by this certification path, with the default encoding first. Attempts to modify the returned`Iterator`via its`remove`method result in an`UnsupportedOperationException`.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an`Iterator`over the names of the supported encodings (as Strings) |

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): String!
```

Returns the type of`Certificate`s in this certification path. This is the same string that would be returned by [cert.getType()](https://developer.android.com/reference/kotlin/java/security/cert/Certificate#getType())for all`Certificate`s in the certification path.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the type of`Certificate`s in this certification path (never null) |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hashcode for this certification path. The hash code of a certification path is defined to be the result of the following calculation: 

```kotlin
<code>hashCode = path.getType().hashCode();
   hashCode = 31*hashCode + path.getCertificates().hashCode();
  </code>
```
This ensures that`path1.equals(path2)`implies that`path1.hashCode()==path2.hashCode()`for any two certification paths,`path1`and`path2`, as required by the general contract of`Object.hashCode`.

<br />

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hashcode value for this certification path |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this certification path. This calls the`toString`method on each of the`Certificate`s in the path.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this certification path |

## Protected methods

### writeReplace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun writeReplace(): Any!
```

Replaces the`CertPath`to be serialized with a`CertPathRep`object.

| Return ||
|-----------------------------------------------------------------------------|----------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the`CertPathRep`to be serialized |

| Exceptions ||
|---------------------------------|-----------------------------------------------------------------------------------|
| `java.io.ObjectStreamException` | if a`CertPathRep`object representing this certification path could not be created |
