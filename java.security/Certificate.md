Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Certificate

```
interface Certificate
```

| [java.security.Certificate](https://developer.android.com/reference/kotlin/java/security/Certificate#) |

| **This interface was deprecated in API level 3.**
|
| This class is deprecated and subject to removal in a future version of Java SE. It has been replaced by `java.security.cert.Certificate` and related classes.

This is an interface of abstract methods for managing a variety of identity certificates. An identity certificate is a guarantee by a principal that a public key is that of another principal. (A principal represents an entity such as an individual user, a group, or a corporation.)

In particular, this interface is intended to be a common abstraction for constructs that have different formats but important common uses. For example, different types of certificates, such as X.509 certificates and PGP certificates, share general certificate functionality (the need to encode and decode certificates) and some types of information, such as a public key, the principal whose key it is, and the guarantor guaranteeing that the public key is that of the specified principal. So an implementation of X.509 certificates and an implementation of PGP certificates can both utilize the Certificate interface, even though their formats and additional types and amounts of information stored are different.

**Important** : This interface is useful for cataloging and grouping objects sharing certain common uses. It does not have any semantics of its own. In particular, a Certificate object does not make any statement as to the *validity* of the binding. It is the duty of the application implementing this interface to verify the certificate and satisfy itself of its validity.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/Certificate#decode(java.io.InputStream)(stream: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)` Decodes a certificate from an input stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/Certificate#encode(java.io.OutputStream)(stream: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!)` Encodes the certificate to an output stream in a format that can be decoded by the `decode` method. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/Certificate#getFormat()()` Returns the name of the coding format. |
| --- | --- |
| abstract [Principal](https://developer.android.com/reference/kotlin/java/security/Principal)! | `https://developer.android.com/reference/kotlin/java/security/Certificate#getGuarantor()()` Returns the guarantor of the certificate, that is, the principal guaranteeing that the public key associated with this certificate is that of the principal associated with this certificate. |
| abstract [Principal](https://developer.android.com/reference/kotlin/java/security/Principal)! | `https://developer.android.com/reference/kotlin/java/security/Certificate#getPrincipal()()` Returns the principal of the principal-key pair being guaranteed by the guarantor. |
| abstract [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)! | `https://developer.android.com/reference/kotlin/java/security/Certificate#getPublicKey()()` Returns the key of the principal-key pair being guaranteed by the guarantor. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/Certificate#toString(kotlin.Boolean)(detailed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns a string that represents the contents of the certificate. |

## Public methods

### decode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun decode(stream: InputStream!): Unit
```

**Deprecated:** *Deprecated in Java.*

Decodes a certificate from an input stream. The format should be that returned by `getFormat` and produced by `encode`.

| Parameters ||
|---|---|
| `stream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!: the input stream from which to fetch the data being decoded. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an exception occurs while trying to input the encoded certificate from the input stream. |
| `java.security.KeyException` | if the certificate is not properly initialized, or data is missing, etc. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/Certificate#encode(java.io.OutputStream)`
- `https://developer.android.com/reference/kotlin/java/security/Certificate#getFormat()`

### encode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun encode(stream: OutputStream!): Unit
```

**Deprecated:** *Deprecated in Java.*

Encodes the certificate to an output stream in a format that can be decoded by the `decode` method.

| Parameters ||
|---|---|
| `stream` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!: the output stream to which to encode the certificate. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if a stream exception occurs while trying to output the encoded certificate to the output stream. |
| `java.security.KeyException` | if the certificate is not properly initialized, or data is missing, etc. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/Certificate#decode(java.io.InputStream)`
- `https://developer.android.com/reference/kotlin/java/security/Certificate#getFormat()`

### getFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFormat(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the name of the coding format. This is used as a hint to find an appropriate parser. It could be "X.509", "PGP", etc. This is the format produced and understood by the `encode` and `decode` methods.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the name of the coding format. |

### getGuarantor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getGuarantor(): Principal!
```

**Deprecated:** *Deprecated in Java.*

Returns the guarantor of the certificate, that is, the principal guaranteeing that the public key associated with this certificate is that of the principal associated with this certificate. For X.509 certificates, the guarantor will typically be a Certificate Authority (such as the United States Postal Service or Verisign, Inc.).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Principal!` | the guarantor which guaranteed the principal-key binding. |

### getPrincipal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPrincipal(): Principal!
```

**Deprecated:** *Deprecated in Java.*

Returns the principal of the principal-key pair being guaranteed by the guarantor.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Principal!` | the principal to which this certificate is bound. |

### getPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPublicKey(): PublicKey!
```

**Deprecated:** *Deprecated in Java.*

Returns the key of the principal-key pair being guaranteed by the guarantor.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/PublicKey!` | the public key that this certificate certifies belongs to a particular principal. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun toString(detailed: Boolean): String!
```

**Deprecated:** *Deprecated in Java.*

Returns a string that represents the contents of the certificate.

| Parameters ||
|---|---|
| `detailed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether or not to give detailed information about the certificate |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a string representing the contents of the certificate |
