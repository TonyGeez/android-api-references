# X509KeyManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509KeyManager

```
interface X509KeyManager : KeyManager
```

| [javax.net.ssl.X509KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#) |

| Known Direct Subclasses [X509ExtendedKeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedKeyManager) |---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [X509ExtendedKeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedKeyManager) | Abstract class that provides for extension of the X509KeyManager interface. | |
| --- | --- | --- | --- | --- | --- | --- |

Instances of this interface manage which X509 certificate-based key pairs are used to authenticate the local side of a secure socket.

During secure socket negotiations, implentations call methods in this interface to:

- determine the set of aliases that are available for negotiations based on the criteria presented,
- select the*best alias*based on the criteria presented, and
- obtain the corresponding key material for given aliases.

Note: the X509ExtendedKeyManager should be used in favor of this class.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [chooseClientAlias](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#chooseClientAlias(kotlin.Array,%20kotlin.Array,%20java.net.Socket))`(`keyType:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!>!`, `socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`)` Choose an alias to authenticate the client side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [chooseServerAlias](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#chooseServerAlias(kotlin.String,%20kotlin.Array,%20java.net.Socket))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!>!`, `socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`)` Choose an alias to authenticate the server side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>! | [getCertificateChain](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#getCertificateChain(kotlin.String))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the certificate chain associated with the given alias. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getClientAliases](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#getClientAliases(kotlin.String,%20kotlin.Array))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!>!`)` Get the matching aliases for authenticating the client side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). |
| abstract [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)! | [getPrivateKey](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#getPrivateKey(kotlin.String))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the key associated with the given alias. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getServerAliases](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#getServerAliases(kotlin.String,%20kotlin.Array))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!>!`)` Get the matching aliases for authenticating the server side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). |
| --- | --- |

## Public methods

### chooseClientAlias

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun chooseClientAlias(
    keyType: Array<String!>!, 
    issuers: Array<Principal!>!, 
    socket: Socket!
): String!
```

Choose an alias to authenticate the client side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyType` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the key algorithm type name(s), ordered with the most-preferred key type first. |
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!\>!:the list of acceptable CA issuer subject names or null if it does not matter which issuers are used. |
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:the socket to be used for this connection. This parameter can be null, which indicates that implementations are free to select an alias applicable to any socket. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the alias name for the desired key, or null if there are no matches. |

### chooseServerAlias

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun chooseServerAlias(
    keyType: String!, 
    issuers: Array<Principal!>!, 
    socket: Socket!
): String!
```

Choose an alias to authenticate the server side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key algorithm type name. |
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!\>!:the list of acceptable CA issuer subject names or null if it does not matter which issuers are used. |
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:the socket to be used for this connection. This parameter can be null, which indicates that implementations are free to select an alias applicable to any socket. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the alias name for the desired key, or null if there are no matches. |

### getCertificateChain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCertificateChain(alias: String!): Array<X509Certificate!>!
```

Returns the certificate chain associated with the given alias.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias name |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>! | the certificate chain (ordered with the user's certificate first and the root certificate authority last), or null if the alias can't be found. |

### getClientAliases

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getClientAliases(
    keyType: String!, 
    issuers: Array<Principal!>!
): Array<String!>!
```

Get the matching aliases for authenticating the client side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key algorithm type name |
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!\>!:the list of acceptable CA issuer subject names, or null if it does not matter which issuers are used. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of the matching alias names, or null if there were no matches. |

### getPrivateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrivateKey(alias: String!): PrivateKey!
```

Returns the key associated with the given alias.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias name |

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)! | the requested key, or null if the alias can't be found. |

### getServerAliases

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getServerAliases(
    keyType: String!, 
    issuers: Array<Principal!>!
): Array<String!>!
```

Get the matching aliases for authenticating the server side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key algorithm type name |
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!\>!:the list of acceptable CA issuer subject names or null if it does not matter which issuers are used. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of the matching alias names, or null if there were no matches. |
