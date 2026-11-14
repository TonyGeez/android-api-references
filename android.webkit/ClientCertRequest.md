# ClientCertRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClientCertRequest

Kotlin | [Java](https://developer.android.com/reference/android/webkit/ClientCertRequest "View this page in Java") 
| --- | --- |

```
abstract class ClientCertRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.ClientCertRequest](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#) |

ClientCertRequest: The user receives an instance of this class as a parameter of [WebViewClient.onReceivedClientCertRequest](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onReceivedClientCertRequest(android.webkit.WebView,%20android.webkit.ClientCertRequest)). The request includes the parameters to choose the client certificate, such as the host name and the port number requesting the cert, the acceptable key types and the principals. The user should call one of the class methods to indicate how to deal with the client certificate request. All methods should be called on UI thread. WebView caches the [proceed](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#proceed(java.security.PrivateKey,%20kotlin.Array)) and [cancel](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#cancel()) responses in memory and uses them to handle future client certificate requests for the same host/port pair. The user can clear the cached data using [WebView.clearClientCertPreferences](https://developer.android.com/reference/kotlin/android/webkit/WebView#clearClientCertPreferences(java.lang.Runnable)).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClientCertRequest](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#ClientCertRequest())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#cancel())`()` Cancel this request. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHost](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#getHost())`()` Returns the host name of the server requesting the certificate. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getKeyTypes](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#getKeyTypes())`()` Returns the acceptable types of asymmetric keys. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#getPort())`()` Returns the port number of the server requesting the certificate. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!\>? | [getPrincipals](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#getPrincipals())`()` Returns the acceptable certificate issuers for the certificate matching the private key. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignore](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#ignore())`()` Ignore the request for now. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [proceed](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#proceed(java.security.PrivateKey,%20kotlin.Array))`(`privateKey:` ` [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)!`, `chain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>!`)` Proceed with the specified private key and client certificate chain. |

## Public constructors

### ClientCertRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClientCertRequest()
```

## Public methods

### cancel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cancel(): Unit
```

Cancel this request. Remember the user's choice and use it for future requests. 

### getHost

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getHost(): String!
```

Returns the host name of the server requesting the certificate. 

### getKeyTypes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getKeyTypes(): Array<String!>?
```

Returns the acceptable types of asymmetric keys.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | This value may be `null`. |

### getPort

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPort(): Int
```

Returns the port number of the server requesting the certificate. 

### getPrincipals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrincipals(): Array<Principal!>?
```

Returns the acceptable certificate issuers for the certificate matching the private key.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!>? | This value may be `null`. |

### ignore

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun ignore(): Unit
```

Ignore the request for now. Do not remember user's choice. 

### proceed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun proceed(
    privateKey: PrivateKey!, 
    chain: Array<X509Certificate!>!
): Unit
```

Proceed with the specified private key and client certificate chain. Remember the user's positive choice and use it for future requests.
