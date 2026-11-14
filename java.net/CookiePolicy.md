# CookiePolicy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CookiePolicy

```
interface CookiePolicy
```

| [java.net.CookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookiePolicy#) |

CookiePolicy implementations decide which cookies should be accepted and which should be rejected. Three pre-defined policy implementations are provided, namely ACCEPT_ALL, ACCEPT_NONE and ACCEPT_ORIGINAL_SERVER.

See RFC 2965 sec. 3.3 and 7 for more detail.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldAccept](https://developer.android.com/reference/kotlin/java/net/CookiePolicy#shouldAccept(java.net.URI,%20java.net.HttpCookie))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI)!`, `cookie:` ` [HttpCookie](https://developer.android.com/reference/kotlin/java/net/HttpCookie)!`)` Will be called to see whether or not this cookie should be accepted. |

| Properties ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [CookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookiePolicy#)! | [ACCEPT_ALL](https://developer.android.com/reference/kotlin/java/net/CookiePolicy#ACCEPT_ALL:java.net.CookiePolicy) One pre-defined policy which accepts all cookies. |
| static [CookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookiePolicy#)! | [ACCEPT_NONE](https://developer.android.com/reference/kotlin/java/net/CookiePolicy#ACCEPT_NONE:java.net.CookiePolicy) One pre-defined policy which accepts no cookies. |
| static [CookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookiePolicy#)! | [ACCEPT_ORIGINAL_SERVER](https://developer.android.com/reference/kotlin/java/net/CookiePolicy#ACCEPT_ORIGINAL_SERVER:java.net.CookiePolicy) One pre-defined policy which only accepts cookies from original server. |

## Public methods

### shouldAccept

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun shouldAccept(
    uri: URI!, 
    cookie: HttpCookie!
): Boolean
```

Will be called to see whether or not this cookie should be accepted.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI)!: the URI to consult accept policy with |
| `cookie` | [HttpCookie](https://developer.android.com/reference/kotlin/java/net/HttpCookie)!: the HttpCookie object in question |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this cookie should be accepted; otherwise, `false` |

## Properties

### ACCEPT_ALL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCEPT_ALL: CookiePolicy!
```

One pre-defined policy which accepts all cookies. 

### ACCEPT_NONE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCEPT_NONE: CookiePolicy!
```

One pre-defined policy which accepts no cookies. 

### ACCEPT_ORIGINAL_SERVER

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCEPT_ORIGINAL_SERVER: CookiePolicy!
```

One pre-defined policy which only accepts cookies from original server.
