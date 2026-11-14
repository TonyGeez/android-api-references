# Authenticator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Authenticator

```
abstract class Authenticator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.Authenticator](../java/net/Authenticator.md) |

The class Authenticator represents an object that knows how to obtain authentication for a network connection. Usually, it will do this by prompting the user for information.

Applications use this class by overriding [getPasswordAuthentication()](../java/net/Authenticator.md)) in a sub-class. This method will typically use the various getXXX() accessor methods to get information about the entity requesting authentication. It must then acquire a username and password either by interacting with the user or through some other non-interactive means. The credentials are then returned as a [PasswordAuthentication](../java/net/PasswordAuthentication.md) return value.

An instance of this concrete sub-class is then registered with the system by calling [setDefault(java.net.Authenticator)](../java/net/Authenticator.md)). When authentication is required, the system will invoke one of the requestPasswordAuthentication() methods which in turn will call the getPasswordAuthentication() method of the registered object.

All methods that request authentication have a default implementation that fails.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [RequestorType](../java/net/Authenticator.RequestorType.md) The type of the entity requesting authentication. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [Authenticator](../java/net/Authenticator.md))`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open static [PasswordAuthentication](../java/net/PasswordAuthentication.md)! | [requestPasswordAuthentication](../java/net/Authenticator.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `addr:` ` [InetAddress](../java/net/InetAddress.md)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `prompt:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `scheme:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Ask the authenticator that has been registered with the system for a password. |
| open static [PasswordAuthentication](../java/net/PasswordAuthentication.md)! | [requestPasswordAuthentication](../java/net/Authenticator.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `addr:` ` [InetAddress](../java/net/InetAddress.md)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `prompt:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `scheme:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `url:` ` [URL](../java/net/URL.md)!`, `reqType:` ` [Authenticator.RequestorType](../java/net/Authenticator.RequestorType.md)!`)` Ask the authenticator that has been registered with the system for a password. |
| open static [PasswordAuthentication](../java/net/PasswordAuthentication.md)! | [requestPasswordAuthentication](../java/net/Authenticator.md))`(`addr:` ` [InetAddress](../java/net/InetAddress.md)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `prompt:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `scheme:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Ask the authenticator that has been registered with the system for a password. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefault](../java/net/Authenticator.md))`(`a:` ` [Authenticator](../java/net/Authenticator.md)!`)` Sets the authenticator that will be used by the networking code when a proxy or an HTTP server asks for authentication. |

| Protected methods ||
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [PasswordAuthentication](../java/net/PasswordAuthentication.md)! | [getPasswordAuthentication](../java/net/Authenticator.md))`()` Called when password authorization is needed. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRequestingHost](../java/net/Authenticator.md))`()` Gets the `hostname` of the site or proxy requesting authentication, or `null` if not available. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestingPort](../java/net/Authenticator.md))`()` Gets the port number for the requested connection. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRequestingPrompt](../java/net/Authenticator.md))`()` Gets the prompt string given by the requestor. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRequestingProtocol](../java/net/Authenticator.md))`()` Give the protocol that's requesting the connection. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRequestingScheme](../java/net/Authenticator.md))`()` Gets the scheme of the requestor (the HTTP scheme for an HTTP firewall, for example). |
| --- | --- |
| [InetAddress](../java/net/InetAddress.md)! | [getRequestingSite](../java/net/Authenticator.md))`()` Gets the `InetAddress` of the site requesting authorization, or `null` if not available. |
| open [URL](../java/net/URL.md)! | [getRequestingURL](../java/net/Authenticator.md))`()` Returns the URL that resulted in this request for authentication. |
| open [Authenticator.RequestorType](../java/net/Authenticator.RequestorType.md)! | [getRequestorType](../java/net/Authenticator.md))`()` Returns whether the requestor is a Proxy or a Server. |
| --- | --- |

## Public constructors

### Authenticator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Authenticator()
```

## Public methods

### requestPasswordAuthentication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun requestPasswordAuthentication(
    host: String!, 
    addr: InetAddress!, 
    port: Int, 
    protocol: String!, 
    prompt: String!, 
    scheme: String!
): PasswordAuthentication!
```

Ask the authenticator that has been registered with the system for a password. This is the preferred method for requesting a password because the hostname can be provided in cases where the InetAddress is not available.

First, if there is a security manager, its `checkPermission` method is called with a `NetPermission("requestPasswordAuthentication")` permission. This may result in a java.lang.SecurityException.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The hostname of the site requesting authentication. |
| `addr` | [InetAddress](../java/net/InetAddress.md)!: The InetAddress of the site requesting authentication, or null if not known. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the port for the requested connection. |
| --- | --- |
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The protocol that's requesting the connection ([java.net.Authenticator#getRequestingProtocol()](../java/net/Authenticator.md))) |
| `prompt` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A prompt string for the user which identifies the authentication realm. |
| `scheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The authentication scheme |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [PasswordAuthentication](../java/net/PasswordAuthentication.md)! | The username/password, or null if one can't be gotten. |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method doesn't allow the password authentication request. |

**See Also**

- [java.net.NetPermission](../java/net/NetPermission.md) 

### requestPasswordAuthentication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun requestPasswordAuthentication(
    host: String!, 
    addr: InetAddress!, 
    port: Int, 
    protocol: String!, 
    prompt: String!, 
    scheme: String!, 
    url: URL!, 
    reqType: Authenticator.RequestorType!
): PasswordAuthentication!
```

Ask the authenticator that has been registered with the system for a password.

First, if there is a security manager, its `checkPermission` method is called with a `NetPermission("requestPasswordAuthentication")` permission. This may result in a java.lang.SecurityException.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The hostname of the site requesting authentication. |
| `addr` | [InetAddress](../java/net/InetAddress.md)!: The InetAddress of the site requesting authorization, or null if not known. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the port for the requested connection |
| --- | --- |
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The protocol that's requesting the connection ([java.net.Authenticator#getRequestingProtocol()](../java/net/Authenticator.md))) |
| `prompt` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A prompt string for the user |
| `scheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The authentication scheme |
| --- | --- |
| `url` | [URL](../java/net/URL.md)!: The requesting URL that caused the authentication |
| `reqType` | [Authenticator.RequestorType](../java/net/Authenticator.RequestorType.md)!: The type (server or proxy) of the entity requesting authentication. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [PasswordAuthentication](../java/net/PasswordAuthentication.md)! | The username/password, or null if one can't be gotten. |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method doesn't allow the password authentication request. |

**See Also**

- [java.net.NetPermission](../java/net/NetPermission.md) 

### requestPasswordAuthentication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun requestPasswordAuthentication(
    addr: InetAddress!, 
    port: Int, 
    protocol: String!, 
    prompt: String!, 
    scheme: String!
): PasswordAuthentication!
```

Ask the authenticator that has been registered with the system for a password.

First, if there is a security manager, its `checkPermission` method is called with a `NetPermission("requestPasswordAuthentication")` permission. This may result in a java.lang.SecurityException.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `addr` | [InetAddress](../java/net/InetAddress.md)!: The InetAddress of the site requesting authorization, or null if not known. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the port for the requested connection |
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The protocol that's requesting the connection ([java.net.Authenticator#getRequestingProtocol()](../java/net/Authenticator.md))) |
| --- | --- |
| `prompt` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A prompt string for the user |
| `scheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The authentication scheme |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [PasswordAuthentication](../java/net/PasswordAuthentication.md)! | The username/password, or null if one can't be gotten. |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method doesn't allow the password authentication request. |

**See Also**

- [java.net.NetPermission](../java/net/NetPermission.md) 

### setDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDefault(a: Authenticator!): Unit
```

Sets the authenticator that will be used by the networking code when a proxy or an HTTP server asks for authentication.

First, if there is a security manager, its `checkPermission` method is called with a `NetPermission("setDefaultAuthenticator")` permission. This may result in a java.lang.SecurityException.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `a` | [Authenticator](../java/net/Authenticator.md)!: The authenticator to be set. If a is `null` then any previously set authenticator is removed. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method doesn't allow setting the default authenticator. |

**See Also**

- [java.net.NetPermission](../java/net/NetPermission.md)

## Protected methods

### getPasswordAuthentication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getPasswordAuthentication(): PasswordAuthentication!
```

Called when password authorization is needed. Subclasses should override the default implementation, which returns null.

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [PasswordAuthentication](../java/net/PasswordAuthentication.md)! | The PasswordAuthentication collected from the user, or null if none is provided. |

### getRequestingHost

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun getRequestingHost(): String!
```

Gets the `hostname` of the site or proxy requesting authentication, or `null` if not available.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the hostname of the connection requiring authentication, or null if it's not available. |

### getRequestingPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun getRequestingPort(): Int
```

Gets the port number for the requested connection.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an `int` indicating the port for the requested connection. |

### getRequestingPrompt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun getRequestingPrompt(): String!
```

Gets the prompt string given by the requestor.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the prompt string given by the requestor (realm for http requests) |

### getRequestingProtocol

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun getRequestingProtocol(): String!
```

Give the protocol that's requesting the connection. Often this will be based on a URL, but in a future JDK it could be, for example, "SOCKS" for a password-protected SOCKS5 firewall.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the protocol, optionally followed by "/version", where version is a version number. |

**See Also**

- [java.net.URL#getProtocol()](../java/net/URL.md)) 

### getRequestingScheme

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun getRequestingScheme(): String!
```

Gets the scheme of the requestor (the HTTP scheme for an HTTP firewall, for example).

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the scheme of the requestor |

### getRequestingSite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun getRequestingSite(): InetAddress!
```

Gets the `InetAddress` of the site requesting authorization, or `null` if not available.

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [InetAddress](../java/net/InetAddress.md)! | the InetAddress of the site requesting authorization, or null if it's not available. |

### getRequestingURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getRequestingURL(): URL!
```

Returns the URL that resulted in this request for authentication.

| Return ||
|---------------------------------------------------------------------|--------------------|
| [URL](../java/net/URL.md)! | the requesting URL |

### getRequestorType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getRequestorType(): Authenticator.RequestorType!
```

Returns whether the requestor is a Proxy or a Server.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [Authenticator.RequestorType](../java/net/Authenticator.RequestorType.md)! | the authentication type of the requestor |
