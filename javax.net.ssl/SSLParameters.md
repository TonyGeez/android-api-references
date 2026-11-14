Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLParameters

```
open class SSLParameters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#) |

Encapsulates parameters for an SSL/TLS connection. The parameters are the list of ciphersuites to be accepted in an SSL/TLS handshake, the list of protocols to be allowed, the endpoint identification algorithm during SSL/TLS handshaking, the Server Name Indication (SNI), the algorithm constraints and whether SSL/TLS servers should request or require client authentication, etc.

SSLParameters can be created via the constructors in this class. Objects can also be obtained using the `getSSLParameters()` methods in `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getSSLParameters()` and `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#getSSLParameters()` and `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getSSLParameters()` or the `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getDefaultSSLParameters()` and `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#getSupportedSSLParameters()` methods in `SSLContext`.

SSLParameters can be applied to a connection via the methods `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setSSLParameters(javax.net.ssl.SSLParameters)` and `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket#setSSLParameters(javax.net.ssl.SSLParameters)` and `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setSSLParameters(javax.net.ssl.SSLParameters)`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#SSLParameters()()` Constructs SSLParameters. |
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#SSLParameters(kotlin.Array)(cipherSuites: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Constructs SSLParameters from the specified array of ciphersuites. |
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#SSLParameters(kotlin.Array,%20kotlin.Array)(cipherSuites: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, protocols: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Constructs SSLParameters from the specified array of ciphersuites and protocols. |

| Public methods ||
|---|---|
| open [AlgorithmConstraints](https://developer.android.com/reference/kotlin/java/security/AlgorithmConstraints.html#)! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getAlgorithmConstraints()()` Returns the cryptographic algorithm constraints. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getApplicationProtocols()()` Returns a prioritized array of application-layer protocol names that can be negotiated over the SSL/TLS protocols. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getCipherSuites()()` Returns a copy of the array of ciphersuites or null if none have been set. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getEndpointIdentificationAlgorithm()()` Gets the endpoint identification algorithm. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getNamedGroups()()` Returns a prioritized array of key exchange named groups names that can be used over the SSL/TLS/DTLS protocols. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getNeedClientAuth()()` Returns whether client authentication should be required. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getProtocols()()` Returns a copy of the array of protocols or null if none have been set. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [SNIMatcher](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher)!\>! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getSNIMatchers()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Collection.html#` containing all `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher`s of the Server Name Indication (SNI) parameter, or null if none has been set. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName)!\>! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getServerNames()()` Returns a `https://developer.android.com/reference/kotlin/java/util/List.html#` containing all `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName`s of the Server Name Indication (SNI) parameter, or null if none has been set. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getUseCipherSuitesOrder()()` Returns whether the local cipher suites preference should be honored. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getWantClientAuth()()` Returns whether client authentication should be requested. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setAlgorithmConstraints(java.security.AlgorithmConstraints)(constraints: https://developer.android.com/reference/kotlin/java/security/AlgorithmConstraints.html#!)` Sets the cryptographic algorithm constraints, which will be used in addition to any configured by the runtime environment. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setApplicationProtocols(kotlin.Array)(protocols: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Sets the prioritized array of application-layer protocol names that can be negotiated over the SSL/TLS protocols. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setCipherSuites(kotlin.Array)(cipherSuites: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Sets the array of ciphersuites. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setEndpointIdentificationAlgorithm(kotlin.String)(algorithm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the endpoint identification algorithm. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setNamedGroups(kotlin.Array)(namedGroups: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Sets the prioritized array of key exchange named groups names that can be used over the SSL/TLS/DTLS protocols. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setNeedClientAuth(kotlin.Boolean)(needClientAuth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether client authentication should be required. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setProtocols(kotlin.Array)(protocols: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Sets the array of protocols. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setSNIMatchers(kotlin.collections.MutableCollection)(matchers: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher!>!)` Sets the `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher`s of the Server Name Indication (SNI) parameter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setServerNames(kotlin.collections.MutableList)(serverNames: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName!>!)` Sets the desired `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName`s of the Server Name Indication (SNI) parameter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setUseCipherSuitesOrder(kotlin.Boolean)(honorOrder: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the local cipher suites preference should be honored. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setWantClientAuth(kotlin.Boolean)(wantClientAuth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether client authentication should be requested. |

## Public constructors

### SSLParameters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SSLParameters()
```

Constructs SSLParameters.

The values of cipherSuites, protocols, cryptographic algorithm constraints, endpoint identification algorithm, server names and server name matchers are set to `null`, useCipherSuitesOrder, wantClientAuth and needClientAuth are set to `false`.

### SSLParameters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SSLParameters(cipherSuites: Array<String!>!)
```

Constructs SSLParameters from the specified array of ciphersuites.

Calling this constructor is equivalent to calling the no-args constructor followed by `setCipherSuites(cipherSuites);`.

| Parameters ||
|---|---|
| `cipherSuites` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: the array of ciphersuites (or null) |

### SSLParameters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SSLParameters(
    cipherSuites: Array<String!>!, 
    protocols: Array<String!>!)
```

Constructs SSLParameters from the specified array of ciphersuites and protocols.

Calling this constructor is equivalent to calling the no-args constructor followed by `setCipherSuites(cipherSuites); setProtocols(protocols);`.

| Parameters ||
|---|---|
| `cipherSuites` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: the array of ciphersuites (or null) |
| `protocols` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: the array of protocols (or null) |

## Public methods

### getAlgorithmConstraints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAlgorithmConstraints(): AlgorithmConstraints!
```

Returns the cryptographic algorithm constraints.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/AlgorithmConstraints.html#!` | the cryptographic algorithm constraints, or null if the constraints have not been set |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setAlgorithmConstraints(java.security.AlgorithmConstraints)`

### getApplicationProtocols

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationProtocols(): Array<String!>!
```

Returns a prioritized array of application-layer protocol names that can be negotiated over the SSL/TLS protocols.

The array could be empty (zero-length), in which case protocol indications will not be used.

This method will return a new array each time it is invoked.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | a non-null, possibly zero-length array of application protocol `String`s. The array is ordered based on protocol preference, with `protocols[0]` being the most preferred. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setApplicationProtocols(kotlin.Array)`

### getCipherSuites

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCipherSuites(): Array<String!>!
```

Returns a copy of the array of ciphersuites or null if none have been set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | a copy of the array of ciphersuites or null if none have been set. |

### getEndpointIdentificationAlgorithm

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEndpointIdentificationAlgorithm(): String!
```

Gets the endpoint identification algorithm.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the endpoint identification algorithm, or null if none has been set. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setEndpointIdentificationAlgorithm(kotlin.String)`

### getNamedGroups

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNamedGroups(): Array<String!>!
```

Returns a prioritized array of key exchange named groups names that can be used over the SSL/TLS/DTLS protocols.

Note that the standard list of key exchange named groups are defined in the [Named Groups](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#named-groups) section of the Java Security Standard Algorithm Names Specification. Providers may support named groups not defined in this list or may not use the recommended name for a certain named group.

The set of named groups that will be used over the SSL/TLS/DTLS connections is determined by the returned array of this method and the underlying provider-specific default named groups.

If the returned array is `null`, then the underlying provider-specific default named groups will be used over the SSL/TLS/DTLS connections.

If the returned array is empty (zero-length), then the named group negotiation mechanism is turned off for SSL/TLS/DTLS protocols, and the connections may not be able to be established if the negotiation mechanism is required by a certain SSL/TLS/DTLS protocol. This parameter will override the underlying provider-specific default name groups.

If the returned array is not `null` or empty (zero-length), then the named groups in the returned array will be used over the SSL/TLS/DTLS connections. This parameter will override the underlying provider-specific default named groups.

This method returns the most recent value passed to `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setNamedGroups(kotlin.Array)` if that method has been called and otherwise returns the default named groups for connection populated objects, or `null` for pre-populated objects.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of key exchange named group names `Strings` or `null` if none have been set. For non-null returns, this method will return a new array each time it is invoked. The array is ordered based on named group preference, with the first entry being the most preferred. Providers should ignore unknown named group names while establishing the SSL/TLS/DTLS connections. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setNamedGroups(kotlin.Array)`

### getNeedClientAuth

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNeedClientAuth(): Boolean
```

Returns whether client authentication should be required.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether client authentication should be required. |

### getProtocols

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProtocols(): Array<String!>!
```

Returns a copy of the array of protocols or null if none have been set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | a copy of the array of protocols or null if none have been set. |

### getSNIMatchers

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSNIMatchers(): MutableCollection<SNIMatcher!>!
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Collection.html#` containing all `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher`s of the Server Name Indication (SNI) parameter, or null if none has been set.

This method is only useful to `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket`s or `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine`s operating in server mode.

For better interoperability, providers generally will not define default matchers so that by default servers will ignore the SNI extension and continue the handshake.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher!>!` | null or an immutable collection of non-null `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher`s |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setSNIMatchers(kotlin.collections.MutableCollection)`

### getServerNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServerNames(): MutableList<SNIServerName!>!
```

Returns a `https://developer.android.com/reference/kotlin/java/util/List.html#` containing all `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName`s of the Server Name Indication (SNI) parameter, or null if none has been set.

This method is only useful to `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket`s or `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine`s operating in client mode.

For SSL/TLS connections, the underlying SSL/TLS provider may specify a default value for a certain server name type. In client mode, it is recommended that, by default, providers should include the server name indication whenever the server can be located by a supported server name type.

It is recommended that providers initialize default Server Name Indications when creating `SSLSocket`/`SSLEngine`s. In the following examples, the server name could be represented by an instance of `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIHostName` which has been initialized with the hostname "www.example.com" and type `https://developer.android.com/reference/kotlin/javax/net/ssl/StandardConstants#SNI_HOST_NAME:kotlin.Int`.

```kotlin
Socket socket =
          sslSocketFactory.createSocket("www.example.com", 443);
  
```
or

```kotlin
SSLEngine engine =
          sslContext.createSSLEngine("www.example.com", 443);
  
```

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName!>!` | null or an immutable list of non-null `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName`s |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/List.html#`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setServerNames(kotlin.collections.MutableList)`

### getUseCipherSuitesOrder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUseCipherSuitesOrder(): Boolean
```

Returns whether the local cipher suites preference should be honored.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether local cipher suites order in `getCipherSuites` should be honored during SSL/TLS handshaking. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setUseCipherSuitesOrder(kotlin.Boolean)`

### getWantClientAuth

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWantClientAuth(): Boolean
```

Returns whether client authentication should be requested.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether client authentication should be requested. |

### setAlgorithmConstraints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAlgorithmConstraints(constraints: AlgorithmConstraints!): Unit
```

Sets the cryptographic algorithm constraints, which will be used in addition to any configured by the runtime environment.

If the `constraints` parameter is non-null, every cryptographic algorithm, key and algorithm parameters used in the SSL/TLS handshake must be permitted by the constraints.

| Parameters ||
|---|---|
| `constraints` | [AlgorithmConstraints](https://developer.android.com/reference/kotlin/java/security/AlgorithmConstraints.html#)!: the algorithm constraints (or null) |

### setApplicationProtocols

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setApplicationProtocols(protocols: Array<String!>!): Unit
```

Sets the prioritized array of application-layer protocol names that can be negotiated over the SSL/TLS protocols.

If application-layer protocols are supported by the underlying SSL/TLS implementation, this method configures which values can be negotiated by protocols such as [RFC 7301](http://www.ietf.org/rfc/rfc7301.txt), the Application Layer Protocol Negotiation (ALPN).

If this end of the connection is expected to offer application protocol values, all protocols configured by this method will be sent to the peer.

If this end of the connection is expected to select the application protocol value, the `protocols` configured by this method are compared with those sent by the peer. The first matched value becomes the negotiated value. If none of the `protocols` were actually requested by the peer, the underlying protocol will determine what action to take. (For example, ALPN will send a `"no_application_protocol"` alert and terminate the connection.)

<br />

| Parameters ||
|---|---|
| `protocols` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: an ordered array of application protocols, with `protocols[0]` being the most preferred. If the array is empty (zero-length), protocol indications will not be used. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if protocols is null, or if any element in a non-empty array is null or an empty (zero-length) string |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getApplicationProtocols()`

### setCipherSuites

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCipherSuites(cipherSuites: Array<String!>!): Unit
```

Sets the array of ciphersuites.

| Parameters ||
|---|---|
| `cipherSuites` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: the array of ciphersuites (or null) |

### setEndpointIdentificationAlgorithm

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setEndpointIdentificationAlgorithm(algorithm: String!): Unit
```

Sets the endpoint identification algorithm.

If the `algorithm` parameter is non-null or non-empty, the endpoint identification/verification procedures must be handled during SSL/TLS handshaking. This is to prevent on-path attacks.

| Parameters ||
|---|---|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The standard string name of the endpoint identification algorithm (or null). See Appendix A in the [Java Cryptography Architecture API Specification \& Reference](https://docs.oracle.com/javase/8/docs/technotes/guides/security/crypto/CryptoSpec.html#AppA) for information about standard algorithm names. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager`

### setNamedGroups

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNamedGroups(namedGroups: Array<String!>!): Unit
```

Sets the prioritized array of key exchange named groups names that can be used over the SSL/TLS/DTLS protocols.

Note that the standard list of key exchange named groups are defined in the [Named Groups](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#named-groups) section of the Java Security Standard Algorithm Names Specification. Providers may support named groups not defined in this list or may not use the recommended name for a certain named group.

The set of named groups that will be used over the SSL/TLS/DTLS connections is determined by the input parameter `namedGroups` array and the underlying provider-specific default named groups. See `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getNamedGroups()` for specific details on how the parameters are used in SSL/TLS/DTLS connections.

| Parameters ||
|---|---|
| `namedGroups` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: an ordered array of key exchange named group names with the first entry being the most preferred, or `null`. This method will make a copy of this array. Providers should ignore unknown named group scheme names while establishing the SSL/TLS/DTLS connections. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if any element in the `namedGroups` array is a duplicate, `null` or [blank](https://developer.android.com/reference/kotlin/java/lang/String.html#isBlank()). |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getNamedGroups()`

### setNeedClientAuth

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNeedClientAuth(needClientAuth: Boolean): Unit
```

Sets whether client authentication should be required. Calling this method clears the `wantClientAuth` flag.

| Parameters ||
|---|---|
| `needClientAuth` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether client authentication should be required |

### setProtocols

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setProtocols(protocols: Array<String!>!): Unit
```

Sets the array of protocols.

| Parameters ||
|---|---|
| `protocols` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: the array of protocols (or null) |

### setSNIMatchers

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setSNIMatchers(matchers: MutableCollection<SNIMatcher!>!): Unit
```

Sets the `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher`s of the Server Name Indication (SNI) parameter.

This method is only useful to `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket`s or `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine`s operating in server mode.

Note that the `matchers` collection is cloned to protect against subsequent modification.

| Parameters ||
|---|---|
| `matchers` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [SNIMatcher](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher)!\>!: the collection of `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher`s (or null) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `matchers` contains more than one name of the same name type |
| `java.lang.NullPointerException` | if the `matchers` contains `null` element |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Collection.html#`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getSNIMatchers()`

### setServerNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setServerNames(serverNames: MutableList<SNIServerName!>!): Unit
```

Sets the desired `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName`s of the Server Name Indication (SNI) parameter.

This method is only useful to `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket`s or `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine`s operating in client mode.

Note that the `serverNames` list is cloned to protect against subsequent modification.

| Parameters ||
|---|---|
| `serverNames` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName)!\>!: the list of desired `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName`s (or null) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `serverNames` contains more than one name of the same name type |
| `java.lang.NullPointerException` | if the `serverNames` contains `null` element |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getServerNames()`

### setUseCipherSuitesOrder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setUseCipherSuitesOrder(honorOrder: Boolean): Unit
```

Sets whether the local cipher suites preference should be honored.

| Parameters ||
|---|---|
| `honorOrder` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether local cipher suites order in `getCipherSuites` should be honored during SSL/TLS handshaking. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getUseCipherSuitesOrder()`

### setWantClientAuth

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWantClientAuth(wantClientAuth: Boolean): Unit
```

Sets whether client authentication should be requested. Calling this method clears the `needClientAuth` flag.

| Parameters ||
|---|---|
| `wantClientAuth` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether client authentication should be requested |
