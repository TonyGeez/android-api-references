# X509ExtendedKeyManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509ExtendedKeyManager

```
abstract class X509ExtendedKeyManager : X509KeyManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.X509ExtendedKeyManager](../javax/net/ssl/X509ExtendedKeyManager.md) |

Abstract class that provides for extension of the X509KeyManager interface.

Methods in this class should be overriden to provide actual implementations.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [X509ExtendedKeyManager](../javax/net/ssl/X509ExtendedKeyManager.md))`()` Constructor used by subclasses only. |

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [chooseEngineClientAlias](../javax/net/ssl/X509ExtendedKeyManager.md))`(`keyType:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](../java/security/Principal.md)!>!`, `engine:` ` [SSLEngine](../javax/net/ssl/SSLEngine.md)!`)` Choose an alias to authenticate the client side of an`SSLEngine`connection given the public key type and the list of certificate issuer authorities recognized by the peer (if any). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [chooseEngineServerAlias](../javax/net/ssl/X509ExtendedKeyManager.md))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](../java/security/Principal.md)!>!`, `engine:` ` [SSLEngine](../javax/net/ssl/SSLEngine.md)!`)` Choose an alias to authenticate the server side of an`SSLEngine`connection given the public key type and the list of certificate issuer authorities recognized by the peer (if any). |

| Inherited functions ||
|---|---|
| From class [X509KeyManager](../javax/net/ssl/X509KeyManager.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [chooseClientAlias](../javax/net/ssl/X509KeyManager.md))`(`keyType:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](../java/security/Principal.md)!>!`, `socket:` ` [Socket](../java/net/Socket.md)!`)` <br /> Choose an alias to authenticate the client side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [chooseServerAlias](../javax/net/ssl/X509KeyManager.md))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](../java/security/Principal.md)!>!`, `socket:` ` [Socket](../java/net/Socket.md)!`)` <br /> Choose an alias to authenticate the server side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](../java/security/cert/X509Certificate.md)!>! | [getCertificateChain](../javax/net/ssl/X509KeyManager.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Returns the certificate chain associated with the given alias. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getClientAliases](../javax/net/ssl/X509KeyManager.md))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](../java/security/Principal.md)!>!`)` <br /> Get the matching aliases for authenticating the client side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). <br /> | | [PrivateKey](../java/security/PrivateKey.md)! | [getPrivateKey](../javax/net/ssl/X509KeyManager.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Returns the key associated with the given alias. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getServerAliases](../javax/net/ssl/X509KeyManager.md))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](../java/security/Principal.md)!>!`)` <br /> Get the matching aliases for authenticating the server side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). <br /> | ||

## Protected constructors

### X509ExtendedKeyManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected X509ExtendedKeyManager()
```

Constructor used by subclasses only.

## Public methods

### chooseEngineClientAlias

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun chooseEngineClientAlias(
    keyType: Array<String!>!, 
    issuers: Array<Principal!>!, 
    engine: SSLEngine!
): String!
```

Choose an alias to authenticate the client side of an`SSLEngine`connection given the public key type and the list of certificate issuer authorities recognized by the peer (if any).

The default implementation returns null.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyType` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the key algorithm type name(s), ordered with the most-preferred key type first. |
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](../java/security/Principal.md)!\>!:the list of acceptable CA issuer subject names or null if it does not matter which issuers are used. |
| `engine` | [SSLEngine](../javax/net/ssl/SSLEngine.md)!:the`SSLEngine`to be used for this connection. This parameter can be null, which indicates that implementations of this interface are free to select an alias applicable to any engine. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the alias name for the desired key, or null if there are no matches. |

### chooseEngineServerAlias

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun chooseEngineServerAlias(
    keyType: String!, 
    issuers: Array<Principal!>!, 
    engine: SSLEngine!
): String!
```

Choose an alias to authenticate the server side of an`SSLEngine`connection given the public key type and the list of certificate issuer authorities recognized by the peer (if any).

The default implementation returns null.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key algorithm type name. |
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](../java/security/Principal.md)!\>!:the list of acceptable CA issuer subject names or null if it does not matter which issuers are used. |
| `engine` | [SSLEngine](../javax/net/ssl/SSLEngine.md)!:the`SSLEngine`to be used for this connection. This parameter can be null, which indicates that implementations of this interface are free to select an alias applicable to any engine. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the alias name for the desired key, or null if there are no matches. |
