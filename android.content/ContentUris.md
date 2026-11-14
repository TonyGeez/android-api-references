# ContentUris

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentUris

Kotlin| [Java](ContentUris.md) 
| --- | --- |

```
open class ContentUris
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.ContentUris](ContentUris.md) |

Utility methods useful for working with [android.net.Uri](../android.net/Uri.md) objects that use the "content" (content://) scheme.

Content URIs have the syntax

`content://`*authority* `/`*path* `/`*id*

`content:`
: The scheme portion of the URI. This is always set to [ContentResolver.SCHEME_CONTENT](ContentResolver.md)(value`content://`).

*authority*
: A string that identifies the entire content provider. All the content URIs for the provider start with this string. To guarantee a unique authority, providers should consider using an authority that is the same as the provider class' package identifier.

*path*
: Zero or more segments, separated by a forward slash (`/`), that identify some subset of the provider's data. Most providers use the path part to identify individual tables. Individual segments in the path are often called "directories" although they do not refer to file directories. The right-most segment in a path is often called a "twig"

*id*
: A unique numeric identifier for a single row in the subset of data identified by the preceding path part. Most providers recognize content URIs that contain an id part and give them special handling. A table that contains a column named`_ID`often expects the id part to be a particular value for that column.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------|---|
| [ContentUris](ContentUris.md))`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Uri.Builder](../android/net/Uri.Builder.md) | [appendId](ContentUris.md))`(`builder:` ` [Uri.Builder](../android/net/Uri.Builder.md)`, `id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Appends the given ID to the end of the path. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [parseId](ContentUris.md))`(`contentUri:` ` [Uri](../android.net/Uri.md)`)` Converts the last path segment to a long. |
| openstatic [Uri](../android.net/Uri.md) | [removeId](ContentUris.md))`(`contentUri:` ` [Uri](../android.net/Uri.md)`)` Removes any ID from the end of the path. |
| --- | --- |
| openstatic [Uri](../android.net/Uri.md) | [withAppendedId](ContentUris.md))`(`contentUri:` ` [Uri](../android.net/Uri.md)`, `id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Appends the given ID to the end of the path. |

## Public constructors

### ContentUris

```
ContentUris()
```

## Public methods

### appendId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun appendId(
    builder: Uri.Builder, 
    id: Long
): Uri.Builder
```

Appends the given ID to the end of the path.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `builder` | [Uri.Builder](../android/net/Uri.Builder.md):to append the ID to This value cannot be`null`. |
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):to append |

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [Uri.Builder](../android/net/Uri.Builder.md) | the given builder This value cannot be`null`. |

### parseId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parseId(contentUri: Uri): Long
```

Converts the last path segment to a long.

This supports a common convention for content URIs where an ID is stored in the last segment.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------|
| `contentUri` | [Uri](../android.net/Uri.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the long conversion of the last segment or -1 if the path is empty |

| Exceptions ||
|-------------------------------------------|------------------------------------|
| `java.lang.UnsupportedOperationException` | if this isn't a hierarchical URI |
| `java.lang.NumberFormatException` | if the last segment isn't a number |

### removeId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun removeId(contentUri: Uri): Uri
```

Removes any ID from the end of the path.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------|
| `contentUri` | [Uri](../android.net/Uri.md):that ends with an ID This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Uri](../android.net/Uri.md) | a new URI with the ID removed from the end of the path This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when the given URI has no ID to remove from the end of the path |

### withAppendedId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun withAppendedId(
    contentUri: Uri, 
    id: Long
): Uri
```

Appends the given ID to the end of the path.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| `contentUri` | [Uri](../android.net/Uri.md):to start with This value cannot be`null`. |
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):to append |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Uri](../android.net/Uri.md) | a new URI with the given ID appended to the end of the path This value cannot be`null`. |
