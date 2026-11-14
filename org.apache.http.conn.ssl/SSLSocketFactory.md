# SSLSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLSocketFactory

```
open class SSLSocketFactory : LayeredSocketFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.apache.http.conn.ssl.SSLSocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#) |

| **This class was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

Layered socket factory for TLS/SSL connections, based on JSSE. .

SSLSocketFactory can be used to validate the identity of the HTTPS server against a list of trusted certificates and to authenticate to the HTTPS server using a private key.

SSLSocketFactory will enable server authentication when supplied with a [truststore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#) file containg one or several trusted certificates. The client secure socket will reject the connection during the SSL session handshake if the target HTTPS server attempts to authenticate itself with a non-trusted certificate.

Use JDK keytool utility to import a trusted certificate and generate a truststore file: 

```kotlin
keytool -import -alias "my server cert" -file server.crt -keystore my.truststore
     
```

<br />

SSLSocketFactory will enable client authentication when supplied with a [keystore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#) file containg a private key/public certificate pair. The client secure socket will use the private key to authenticate itself to the target HTTPS server during the SSL session handshake if requested to do so by the server. The target HTTPS server will in its turn verify the certificate presented by the client in order to establish client's authenticity

Use the following sequence of actions to generate a keystore file

- Use JDK keytool utility to generate a new key

  ```kotlin
  keytool -genkey -v -alias "my client key" -validity 365 -keystore my.keystore
  ```
 For simplicity use the same password for the key as that of the keystore

 <br />

- Issue a certificate signing request (CSR)

  ```kotlin
  keytool -certreq -alias "my client key" -file mycertreq.csr -keystore my.keystore
  ```

 <br />

- Send the certificate request to the trusted Certificate Authority for signature. One may choose to act as their own CA and sign the certificate request using a PKI tool, such as OpenSSL.

- Import the trusted CA root certificate

  ```kotlin
  keytool -import -alias "my trusted ca" -file caroot.crt -keystore my.keystore
  ```

 <br />

- Import the PKCS#7 file containg the complete certificate chain

  ```kotlin
  keytool -import -alias "my client key" -file mycert.p7 -keystore my.keystore
  ```

 <br />

- Verify the content the resultant keystore file

  ```kotlin
  keytool -list -v -keystore my.keystore
  ```

 <br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SSL](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#SSL:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SSLV2](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#SSLV2:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TLS](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#TLS:kotlin.String) <br /> |
| --- | --- |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#SSLSocketFactory(kotlin.String,%20java.security.KeyStore,%20kotlin.String,%20java.security.KeyStore,%20java.security.SecureRandom,%20org.apache.http.conn.scheme.HostNameResolver))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `keystore:` ` [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#)!`, `keystorePassword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `truststore:` ` [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#)!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`, `nameResolver:` ` [HostNameResolver](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/HostNameResolver.html#)!`)` <br /> |
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#SSLSocketFactory(java.security.KeyStore))`(`truststore:` ` [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#)!`)` <br /> |
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#SSLSocketFactory(java.security.KeyStore,%20kotlin.String))`(`keystore:` ` [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#)!`, `keystorePassword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#SSLSocketFactory(java.security.KeyStore,%20kotlin.String,%20java.security.KeyStore))`(`keystore:` ` [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#)!`, `keystorePassword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `truststore:` ` [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore.html#)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [connectSocket](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#connectSocket(java.net.Socket,%20kotlin.String,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int,%20org.apache.http.params.HttpParams))`(`sock:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `localAddress:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `localPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams.html#)!`)` <br /> |
| open [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#createSocket())`()` <br /> |
| open [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | [createSocket](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#createSocket(java.net.Socket,%20kotlin.String,%20kotlin.Int,%20kotlin.Boolean))`(`socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `autoClose:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| open [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier)! | [getHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#getHostnameVerifier())`()` <br /> |
| openstatic [SSLSocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#)! | [getSocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#getSocketFactory())`()` Gets an singleton instance of the SSLProtocolSocketFactory. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSecure](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#isSecure(java.net.Socket))`(`sock:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`)` Checks whether a socket connection is secure. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#setHostnameVerifier(org.apache.http.conn.ssl.X509HostnameVerifier))`(`hostnameVerifier:` ` [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier)!`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier)! | [ALLOW_ALL_HOSTNAME_VERIFIER](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#ALLOW_ALL_HOSTNAME_VERIFIER:org.apache.http.conn.ssl.X509HostnameVerifier) <br /> |
| static [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier)! | [BROWSER_COMPATIBLE_HOSTNAME_VERIFIER](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#BROWSER_COMPATIBLE_HOSTNAME_VERIFIER:org.apache.http.conn.ssl.X509HostnameVerifier) <br /> |
| static [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier)! | [STRICT_HOSTNAME_VERIFIER](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#STRICT_HOSTNAME_VERIFIER:org.apache.http.conn.ssl.X509HostnameVerifier) <br /> |
| --- | --- |

## Constants

### SSL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SSL: String
```

**Deprecated:** *Deprecated in Java.* 

 Value: "SSL"

### SSLV2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SSLV2: String
```

**Deprecated:** *Deprecated in Java.* 

 Value: "SSLv2"

### TLS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TLS: String
```

**Deprecated:** *Deprecated in Java.* 

 Value: "TLS"

## Public constructors

### SSLSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLSocketFactory(
    algorithm: String!, 
    keystore: KeyStore!, 
    keystorePassword: String!, 
    truststore: KeyStore!, 
    random: SecureRandom!, 
    nameResolver: HostNameResolver!)
```  

### SSLSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLSocketFactory(truststore: KeyStore!)
```  

### SSLSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLSocketFactory(
    keystore: KeyStore!, 
    keystorePassword: String!)
```  

### SSLSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLSocketFactory(
    keystore: KeyStore!, 
    keystorePassword: String!, 
    truststore: KeyStore!)
```

## Public methods

### connectSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun connectSocket(
    sock: Socket!, 
    host: String!, 
    port: Int, 
    localAddress: InetAddress!, 
    localPort: Int, 
    params: HttpParams!
): Socket!
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sock` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:the socket to connect, as obtained from [createSocket](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/SocketFactory.html#createSocket()).`null`indicates that a new socket should be created and connected. |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host to connect to |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port to connect to on the host |
| --- | --- |
| `localAddress` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:the local address to bind the socket to, or`null`for any |
| `localPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port on the local machine, 0 or a negative number for any |
| `params` | [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams.html#)!:additional [parameters](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams.html#) for connecting |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | the connected socket. The returned object may be different from the`sock`argument if this factory supports a layered protocol. |

| Exceptions ||
|------------------------------------------------|--------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.net.UnknownHostException` | if the IP address of the target host can not be determined |
| `org.apache.http.conn.ConnectTimeoutException` | if the socket cannot be connected within the time limit defined in the`params` |
| --- | --- |

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSocket(): Socket!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---------------------------------------------------------------------------------|--------------|
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | a new socket |

| Exceptions ||
|-----------------------|--------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while creating the socket |

### createSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSocket(
    socket: Socket!, 
    host: String!, 
    port: Int, 
    autoClose: Boolean
): Socket!
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:the existing socket |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host name/IP |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port on the host |
| --- | --- |
| `autoClose` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):a flag for closing the underling socket when the created socket is closed |

| Return ||
|---------------------------------------------------------------------------------|---------------------|
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)! | Socket a new socket |

| Exceptions ||
|---------------------------------|----------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while creating the socket |
| `java.net.UnknownHostException` | if the IP address of the host cannot be determined |

### getHostnameVerifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHostnameVerifier(): X509HostnameVerifier!
```

**Deprecated:** *Deprecated in Java.* 

### getSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSocketFactory(): SSLSocketFactory!
```

**Deprecated:** *Deprecated in Java.*

Gets an singleton instance of the SSLProtocolSocketFactory.

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------|
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory#)! | a SSLProtocolSocketFactory |

### isSecure

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSecure(sock: Socket!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether a socket connection is secure. This factory creates TLS/SSL socket connections which, by default, are considered secure. 
Derived classes may override this method to perform runtime checks, for example based on the cypher suite.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `sock` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:the connected socket |

| Return ||
|------------------------------------------------------------------------------------|--------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if the argument is invalid |

### setHostnameVerifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHostnameVerifier(hostnameVerifier: X509HostnameVerifier!): Unit
```

**Deprecated:** *Deprecated in Java.*

## Properties

### ALLOW_ALL_HOSTNAME_VERIFIER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALLOW_ALL_HOSTNAME_VERIFIER: X509HostnameVerifier!
```

**Deprecated:** *Deprecated in Java.* 

### BROWSER_COMPATIBLE_HOSTNAME_VERIFIER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BROWSER_COMPATIBLE_HOSTNAME_VERIFIER: X509HostnameVerifier!
```

**Deprecated:** *Deprecated in Java.* 

### STRICT_HOSTNAME_VERIFIER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STRICT_HOSTNAME_VERIFIER: X509HostnameVerifier!
```

**Deprecated:** *Deprecated in Java.*
