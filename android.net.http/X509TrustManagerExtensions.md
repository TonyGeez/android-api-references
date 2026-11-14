Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509TrustManagerExtensions

```
open class X509TrustManagerExtensions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.http.X509TrustManagerExtensions](https://developer.android.com/reference/kotlin/android/net/http/X509TrustManagerExtensions#) |

X509TrustManager wrapper exposing Android-added features.

The checkServerTrusted methods allow callers to provide some additional context for the verification. This is particularly useful when an SSLEngine or SSLSocket is not available.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/http/X509TrustManagerExtensions#X509TrustManagerExtensions(javax.net.ssl.X509TrustManager)(tm: https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager.html#!)` Constructs a new X509TrustManagerExtensions wrapper. |

| Public methods ||
|---|---|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\> | `https://developer.android.com/reference/kotlin/android/net/http/X509TrustManagerExtensions#checkServerTrusted(kotlin.Array,%20kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.String)(chain: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!>, ocspData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?, tlsSctData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?, authType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Verifies the given certificate chain. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>! | `https://developer.android.com/reference/kotlin/android/net/http/X509TrustManagerExtensions#checkServerTrusted(kotlin.Array,%20kotlin.String,%20kotlin.String)(chain: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!>!, authType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Verifies the given certificate chain. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/X509TrustManagerExtensions#isSameTrustConfiguration(kotlin.String,%20kotlin.String)(hostname1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, hostname2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns `true` if the TrustManager uses the same trust configuration for the provided hostnames. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/X509TrustManagerExtensions#isUserAddedCertificate(java.security.cert.X509Certificate)(cert: https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!)` Checks whether a CA certificate is added by an user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/X509TrustManagerExtensions#setNetworkSecurityPolicy(android.security.NetworkSecurityPolicy)(policy: https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#)` Sets the `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#` to be used by this TrustManager. |

## Public constructors

### X509TrustManagerExtensions

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
X509TrustManagerExtensions(tm: X509TrustManager!)
```

Constructs a new X509TrustManagerExtensions wrapper.

| Parameters ||
|---|---|
| `tm` | [X509TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager.html#)!: A `https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager.html#` as returned by TrustManagerFactory.getInstance(); |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If tm is an unsupported TrustManager type. |

## Public methods

### checkServerTrusted

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkServerTrusted(
    chain: Array<X509Certificate!>, 
    ocspData: ByteArray?, 
    tlsSctData: ByteArray?, 
    authType: String, 
    host: String
): MutableList<X509Certificate!>
```

Verifies the given certificate chain.

See `https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager.html#checkServerTrusted(kotlin.Array,%20kotlin.String)` for a description of the chain and authType parameters. The final parameter, host, should be the hostname of the server.

ocspData and tlsSctData may be provided to verify any Signed Certificate Timestamp (SCT) attached to the connection. These are ASN.1 octet strings (SignedCertificateTimestampList) as described in RFC 6962, Section 3.3. Note that SCTs embedded in the certificate chain will automatically be processed.

| Parameters ||
|---|---|
| `chain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>: This value cannot be `null`. |
| `ocspData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: This value may be `null`. |
| `tlsSctData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: This value may be `null`. |
| `authType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!>` | the properly ordered chain used for verification as a list of X509Certificates. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the TrustManager is not compatible. |
| `java.security.cert.CertificateException` | if the chain does not verify correctly. |

### checkServerTrusted

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkServerTrusted(
    chain: Array<X509Certificate!>!, 
    authType: String!, 
    host: String!
): MutableList<X509Certificate!>!
```

Verifies the given certificate chain.

See `https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager.html#checkServerTrusted(kotlin.Array,%20kotlin.String)` for a description of the chain and authType parameters. The final parameter, host, should be the hostname of the server.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!>!` | the properly ordered chain used for verification as a list of X509Certificates. |

| Exceptions ||
|---|---|
| `java.security.cert.CertificateException` | if the chain does not verify correctly. |

### isSameTrustConfiguration

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSameTrustConfiguration(
    hostname1: String!, 
    hostname2: String!
): Boolean
```

Returns `true` if the TrustManager uses the same trust configuration for the provided hostnames.

### isUserAddedCertificate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isUserAddedCertificate(cert: X509Certificate!): Boolean
```

Checks whether a CA certificate is added by an user.

Since `https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager.html#checkServerTrusted(kotlin.Array,%20kotlin.String)` may allow its parameter `chain` to chain up to user-added CA certificates, this method can be used to perform additional policies for user-added CA certificates.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` to indicate that the certificate authority exists in the user added certificate store, `false` otherwise. |

### setNetworkSecurityPolicy

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNetworkSecurityPolicy(policy: NetworkSecurityPolicy): Unit
```

Sets the `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#` to be used by this TrustManager.

This method allows an application to associate a specific security policy with this `https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager.html#` instance. When a policy is set, it overrides the default process-wide policy returned by `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#getInstance()` for all certificate verifications performed by this TrustManager.

The TrustManager will query the provided policy for security decisions, including:

- Whether cleartext traffic is permitted for a specific hostname.
- Whether Certificate Transparency (CT) verification is required for a hostname.
- The domain encryption mode (e.g., Encrypted Client Hello) to be used.

By using a custom `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#`, applications can programmatically define granular security constraints that differ from the global application configuration. This is useful for specialized network stacks or for enforcing stricter security on specific sensitive connections.

| Parameters ||
|---|---|
| `policy` | [NetworkSecurityPolicy](https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#): the `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#` to associate with this TrustManager. Must not be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#`
- `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#getInstance()`
