# ContentHandlerFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentHandlerFactory

```
interface ContentHandlerFactory
```

| [java.net.ContentHandlerFactory](../java/net/ContentHandlerFactory.md) |

This interface defines a factory for content handlers. An implementation of this interface should map a MIME type into an instance of`ContentHandler`.

This interface is used by the`URLStreamHandler`class to create a`ContentHandler`for a MIME type.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ContentHandler](../java/net/ContentHandler.md)! | [createContentHandler](../java/net/ContentHandlerFactory.md))`(`mimetype:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new`ContentHandler`to read an object from a`URLStreamHandler`. |

## Public methods

### createContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createContentHandler(mimetype: String!): ContentHandler!
```

Creates a new`ContentHandler`to read an object from a`URLStreamHandler`.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `mimetype` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the MIME type for which a content handler is desired. |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [ContentHandler](../java/net/ContentHandler.md)! | a new`ContentHandler`to read an object from a`URLStreamHandler`. |

**See Also**

- [java.net.ContentHandler](../java/net/ContentHandler.md)
- [java.net.URLStreamHandler](../java/net/URLStreamHandler.md)
