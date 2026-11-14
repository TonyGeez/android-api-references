# X509KeyManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509KeyManager

```
interface X509KeyManager : KeyManager
```

| [javax.net.ssl.X509KeyManager](X509KeyManager.md) |

| Known Direct Subclasses [X509ExtendedKeyManager](X509ExtendedKeyManager.md) |---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [X509ExtendedKeyManager](X509ExtendedKeyManager.md) | Abstract class that provides for extension of the X509KeyManager interface. | |
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
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [chooseClientAlias](X509KeyManager.md))`(`keyType:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](../java.security/Principal.md)!>!`, `socket:` ` [Socket](../java.net/Socket.md)!`)` Choose an alias to authenticate the client side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [chooseServerAlias](X509KeyManager.md))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](../java.security/Principal.md)!>!`, `socket:` ` [Socket](../java.net/Socket.md)!`)` Choose an alias to authenticate the server side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](../java.security.cert/X509Certificate.md)!\>! | [getCertificateChain](X509KeyManager.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the certificate chain associated with the given alias. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getClientAliases](X509KeyManager.md))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](../java.security/Principal.md)!>!`)` Get the matching aliases for authenticating the client side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). |
| abstract [PrivateKey](../java.security/PrivateKey.md)! | [getPrivateKey](X509KeyManager.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the key associated with the given alias. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getServerAliases](X509KeyManager.md))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](../java.security/Principal.md)!>!`)` Get the matching aliases for authenticating the server side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). |
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
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](../java.security/Principal.md)!\>!:the list of acceptable CA issuer subject names or null if it does not matter which issuers are used. |
| `socket` | [Socket](../java.net/Socket.md)!:the socket to be used for this connection. This parameter can be null, which indicates that implementations are free to select an alias applicable to any socket. |
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
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](../java.security/Principal.md)!\>!:the list of acceptable CA issuer subject names or null if it does not matter which issuers are used. |
| `socket` | [Socket](../java.net/Socket.md)!:the socket to be used for this connection. This parameter can be null, which indicates that implementations are free to select an alias applicable to any socket. |
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
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](../java.security.cert/X509Certificate.md)!>! | the certificate chain (ordered with the user's certificate first and the root certificate authority last), or null if the alias can't be found. |

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
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](../java.security/Principal.md)!\>!:the list of acceptable CA issuer subject names, or null if it does not matter which issuers are used. |

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
| [PrivateKey](../java.security/PrivateKey.md)! | the requested key, or null if the alias can't be found. |

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
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](../java.security/Principal.md)!\>!:the list of acceptable CA issuer subject names or null if it does not matter which issuers are used. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of the matching alias names, or null if there were no matches. |
