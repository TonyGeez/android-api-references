# SNIMatcher

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SNIMatcher

```
abstract class SNIMatcher
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.net.ssl.SNIMatcher](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher#) |

Instances of this class represent a matcher that performs match operations on an [SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName) instance.

Servers can use Server Name Indication (SNI) information to decide if specific [SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket) or [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine) instances should accept a connection. For example, when multiple "virtual" or "name-based" servers are hosted on a single underlying network address, the server application can use SNI information to determine whether this server is the exact server that the client wants to access. Instances of this class can be used by a server to verify the acceptable server names of a particular type, such as host names.

`SNIMatcher` objects are immutable. Subclasses should not provide methods that can change the state of an instance once it has been created.

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SNIMatcher](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher#SNIMatcher(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an `SNIMatcher` using the specified server name type. |

| Public methods ||
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher#getType())`()` Returns the server name type of this `SNIMatcher` object. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matches](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher#matches(javax.net.ssl.SNIServerName))`(`serverName:` ` [SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName)!`)` Attempts to match the given [SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName). |

## Protected constructors

### SNIMatcher

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SNIMatcher(type: Int)
```

Creates an `SNIMatcher` using the specified server name type.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the type of the server name that this matcher performs on |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if `type` is not in the range of 0 to 255, inclusive. |

## Public methods

### getType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Returns the server name type of this `SNIMatcher` object.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the server name type of this `SNIMatcher` object. |

**See Also**

- [javax.net.ssl.SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName) 

### matches

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun matches(serverName: SNIServerName!): Boolean
```

Attempts to match the given [SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `serverName` | [SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName)!: the [SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName) instance on which this matcher performs match operations |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if, and only if, the matcher matches the given `serverName` |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------|
| `java.lang.NullPointerException` | if `serverName` is `null` |
| `java.lang.IllegalArgumentException` | if `serverName` is not of the given server name type of this matcher |

**See Also**

- [javax.net.ssl.SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName)
