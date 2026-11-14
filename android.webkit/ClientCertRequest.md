# ClientCertRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClientCertRequest

Kotlin | [Java](ClientCertRequest.md) 
| --- | --- |

```
abstract class ClientCertRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.ClientCertRequest](ClientCertRequest.md) |

ClientCertRequest: The user receives an instance of this class as a parameter of [WebViewClient.onReceivedClientCertRequest](WebViewClient.md)). The request includes the parameters to choose the client certificate, such as the host name and the port number requesting the cert, the acceptable key types and the principals. The user should call one of the class methods to indicate how to deal with the client certificate request. All methods should be called on UI thread. WebView caches the [proceed](ClientCertRequest.md)) and [cancel](ClientCertRequest.md)) responses in memory and uses them to handle future client certificate requests for the same host/port pair. The user can clear the cached data using [WebView.clearClientCertPreferences](WebView.md)).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClientCertRequest](ClientCertRequest.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](ClientCertRequest.md))`()` Cancel this request. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHost](ClientCertRequest.md))`()` Returns the host name of the server requesting the certificate. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getKeyTypes](ClientCertRequest.md))`()` Returns the acceptable types of asymmetric keys. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](ClientCertRequest.md))`()` Returns the port number of the server requesting the certificate. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](../java.security/Principal.md)!\>? | [getPrincipals](ClientCertRequest.md))`()` Returns the acceptable certificate issuers for the certificate matching the private key. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ignore](ClientCertRequest.md))`()` Ignore the request for now. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [proceed](ClientCertRequest.md))`(`privateKey:` ` [PrivateKey](../java.security/PrivateKey.md)!`, `chain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](../java.security.cert/X509Certificate.md)!>!`)` Proceed with the specified private key and client certificate chain. |

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
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](../java.security/Principal.md)!>? | This value may be `null`. |

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
