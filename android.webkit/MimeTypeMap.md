# MimeTypeMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MimeTypeMap

Kotlin| [Java](../android/webkit/MimeTypeMap.md) 
| --- | --- |

```
open class MimeTypeMap
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.MimeTypeMap](../android/webkit/MimeTypeMap.md) |

Two-way map that maps MIME-types to file extensions and vice versa.

See also [java.net.URLConnection#guessContentTypeFromName](../java/net/URLConnection.md))and [java.net.URLConnection#guessContentTypeFromStream](../java/net/URLConnection.md)). This class and`URLConnection`share the same MIME-type database.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getExtensionFromMimeType](../android/webkit/MimeTypeMap.md))`(`mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return the registered extension for the given MIME type. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFileExtensionFromUrl](../android/webkit/MimeTypeMap.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the file extension or an empty string if there is no extension. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMimeTypeFromExtension](../android/webkit/MimeTypeMap.md))`(`extension:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return the MIME type for the given extension. |
| --- | --- |
| openstatic [MimeTypeMap](../android/webkit/MimeTypeMap.md)! | [getSingleton](../android/webkit/MimeTypeMap.md))`()` Get the singleton instance of MimeTypeMap. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasExtension](../android/webkit/MimeTypeMap.md))`(`extension:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return`true`if the given extension has a registered MIME type. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMimeType](../android/webkit/MimeTypeMap.md))`(`mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return`true`if the given MIME type has an entry in the map. |
| --- | --- |

## Public methods

### getExtensionFromMimeType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtensionFromMimeType(mimeType: String!): String?
```

Return the registered extension for the given MIME type. Note that some MIME types map to multiple extensions. This call will return the most common extension for the given MIME type.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A MIME type (i.e. text/plain) |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The extension for the given MIME type or`null`if there is none. |

### getFileExtensionFromUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getFileExtensionFromUrl(url: String!): String!
```

Returns the file extension or an empty string if there is no extension. This method is a convenience method for obtaining the extension of a url and has undefined results for other Strings.

| Parameters ||
|-------|------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The file extension of the given url. |

### getMimeTypeFromExtension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMimeTypeFromExtension(extension: String!): String?
```

Return the MIME type for the given extension.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `extension` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A file extension without the leading '.' |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The MIME type for the given extension or`null`if there is none. |

### getSingleton

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSingleton(): MimeTypeMap!
```

Get the singleton instance of MimeTypeMap.

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| [MimeTypeMap](../android/webkit/MimeTypeMap.md)! | The singleton instance of the MIME-type map. |

### hasExtension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasExtension(extension: String!): Boolean
```

Return`true`if the given extension has a registered MIME type.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `extension` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A file extension without the leading '.' |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if there is an extension entry in the map. |

### hasMimeType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasMimeType(mimeType: String!): Boolean
```

Return`true`if the given MIME type has an entry in the map.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A MIME type (i.e. text/plain) |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if there is a mimeType entry in the map. |
