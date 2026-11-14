# FileNameMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileNameMap

```
interface FileNameMap
```

| [java.net.FileNameMap](../java/net/FileNameMap.md) |

A simple interface which provides a mechanism to map between a file name and a MIME type string.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getContentTypeFor](../java/net/FileNameMap.md))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the MIME type for the specified file name. |

## Public methods

### getContentTypeFor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getContentTypeFor(fileName: String!): String!
```

Gets the MIME type for the specified file name.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the specified file name |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a`String`indicating the MIME type for the specified file name. |
