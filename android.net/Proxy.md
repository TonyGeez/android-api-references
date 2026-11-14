# Proxy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Proxy

Kotlin| [Java](Proxy.md) 
| --- | --- |

```
class Proxy
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.Proxy](Proxy.md) |

A convenience class for accessing the user and default proxy settings.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROXY_CHANGE_ACTION](Proxy.md) Used to notify an app that's caching the proxy that either the default connection has changed or any connection's proxy has changed. |

| Public constructors ||
|----------------------------------------------------------------------------------------------|---|
| [Proxy](Proxy.md))`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultHost](Proxy.md))`()` Return the default proxy host specified by the carrier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultPort](Proxy.md))`()` Return the default proxy port specified by the carrier. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHost](Proxy.md))`(`ctx:` ` [Context](../android.content/Context.md)!`)` Return the proxy host set by the user. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](Proxy.md))`(`ctx:` ` [Context](../android.content/Context.md)!`)` Return the proxy port set by the user. |

## Constants

### PROXY_CHANGE_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROXY_CHANGE_ACTION: String
```

Used to notify an app that's caching the proxy that either the default connection has changed or any connection's proxy has changed. The new proxy should be queried using [ConnectivityManager.getDefaultProxy()](ConnectivityManager.md)).

This is a protected intent that can only be sent by the system 

 Value: "android.intent.action.PROXY_CHANGE"

## Public constructors

### Proxy

```
Proxy()
```

## Public methods

### getDefaultHost

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefaultHost(): String!
```

**Deprecated:** *Use standard java vm proxy values to find the host, port and exclusion list. This call ignores the exclusion list and no longer reports only mobile-data apn-based proxy values.*

Return the default proxy host specified by the carrier.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | String containing the host name or null if there is no proxy for this carrier. |

### getDefaultPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefaultPort(): Int
```

**Deprecated:** *Use standard java vm proxy values to find the host, port and exclusion list. This call ignores the exclusion list and no longer reports only mobile-data apn-based proxy values.*

Return the default proxy port specified by the carrier.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The port number to be used with the proxy host or -1 if there is no proxy for this carrier. |

### getHost

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getHost(ctx: Context!): String!
```

**Deprecated:** *Use standard java vm proxy values to find the host, port and exclusion list. This call ignores the exclusion list.*

Return the proxy host set by the user.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `ctx` | [Context](../android.content/Context.md)!:A Context used to get the settings for the proxy host. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | String containing the host name. If the user did not set a host name it returns the default host. A null value means that no host is to be used. |

### getPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getPort(ctx: Context!): Int
```

**Deprecated:** *Use standard java vm proxy values to find the host, port and exclusion list. This call ignores the exclusion list.*

Return the proxy port set by the user.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `ctx` | [Context](../android.content/Context.md)!:A Context used to get the settings for the proxy port. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The port number to use or -1 if no proxy is to be used. |
