# URLStreamHandlerFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# URLStreamHandlerFactory

```
interface URLStreamHandlerFactory
```

| [java.net.URLStreamHandlerFactory](https://developer.android.com/reference/kotlin/java/net/URLStreamHandlerFactory#) |

This interface defines a factory for`URL`stream protocol handlers.

A URL stream handler factory is used as specified in the [URL constructor](https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String)).

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [URLStreamHandler](https://developer.android.com/reference/kotlin/java/net/URLStreamHandler)! | [createURLStreamHandler](https://developer.android.com/reference/kotlin/java/net/URLStreamHandlerFactory#createURLStreamHandler(kotlin.String))`(`protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new`URLStreamHandler`instance with the specified protocol. |

## Public methods

### createURLStreamHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createURLStreamHandler(protocol: String!): URLStreamHandler!
```

Creates a new`URLStreamHandler`instance with the specified protocol.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the protocol ("`ftp`", "`http`", "`nntp`", etc.). |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [URLStreamHandler](https://developer.android.com/reference/kotlin/java/net/URLStreamHandler)! | a`URLStreamHandler`for the specific protocol, or`null`if this factory cannot create a handler for the specific protocol |

**See Also**

- [java.net.URLStreamHandler](https://developer.android.com/reference/kotlin/java/net/URLStreamHandler)
