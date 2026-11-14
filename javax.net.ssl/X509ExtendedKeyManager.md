# X509ExtendedKeyManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509ExtendedKeyManager

```
abstract class X509ExtendedKeyManager : X509KeyManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.X509ExtendedKeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedKeyManager#) |

Abstract class that provides for extension of the X509KeyManager interface.

Methods in this class should be overriden to provide actual implementations.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [X509ExtendedKeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedKeyManager#X509ExtendedKeyManager())`()` Constructor used by subclasses only. |

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [chooseEngineClientAlias](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedKeyManager#chooseEngineClientAlias(kotlin.Array,%20kotlin.Array,%20javax.net.ssl.SSLEngine))`(`keyType:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!>!`, `engine:` ` [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)!`)` Choose an alias to authenticate the client side of an`SSLEngine`connection given the public key type and the list of certificate issuer authorities recognized by the peer (if any). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [chooseEngineServerAlias](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedKeyManager#chooseEngineServerAlias(kotlin.String,%20kotlin.Array,%20javax.net.ssl.SSLEngine))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!>!`, `engine:` ` [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)!`)` Choose an alias to authenticate the server side of an`SSLEngine`connection given the public key type and the list of certificate issuer authorities recognized by the peer (if any). |

| Inherited functions ||
|---|---|
| From class [X509KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [chooseClientAlias](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#chooseClientAlias(kotlin.Array,%20kotlin.Array,%20java.net.Socket))`(`keyType:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!>!`, `socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`)` <br /> Choose an alias to authenticate the client side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [chooseServerAlias](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#chooseServerAlias(kotlin.String,%20kotlin.Array,%20java.net.Socket))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!>!`, `socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`)` <br /> Choose an alias to authenticate the server side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>! | [getCertificateChain](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#getCertificateChain(kotlin.String))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Returns the certificate chain associated with the given alias. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getClientAliases](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#getClientAliases(kotlin.String,%20kotlin.Array))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!>!`)` <br /> Get the matching aliases for authenticating the client side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). <br /> | | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)! | [getPrivateKey](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#getPrivateKey(kotlin.String))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Returns the key associated with the given alias. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getServerAliases](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager#getServerAliases(kotlin.String,%20kotlin.Array))`(`keyType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!>!`)` <br /> Get the matching aliases for authenticating the server side of a secure socket given the public key type and the list of certificate issuer authorities recognized by the peer (if any). <br /> | ||

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
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!\>!:the list of acceptable CA issuer subject names or null if it does not matter which issuers are used. |
| `engine` | [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)!:the`SSLEngine`to be used for this connection. This parameter can be null, which indicates that implementations of this interface are free to select an alias applicable to any engine. |
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
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!\>!:the list of acceptable CA issuer subject names or null if it does not matter which issuers are used. |
| `engine` | [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)!:the`SSLEngine`to be used for this connection. This parameter can be null, which indicates that implementations of this interface are free to select an alias applicable to any engine. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the alias name for the desired key, or null if there are no matches. |
