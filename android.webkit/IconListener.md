# WebIconDatabase.IconListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IconListener

Kotlin| [Java](../android/webkit/WebIconDatabase.IconListener.md) 
| --- | --- |

```
interface IconListener
```

| [android.webkit.WebIconDatabase.IconListener](../android/webkit/WebIconDatabase.IconListener.md) |

| **This interface was deprecated in API level 18.**
|
| This interface is obsolete.

Interface for receiving icons from the database.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedIcon](../android/webkit/WebIconDatabase.IconListener.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `icon:` ` [Bitmap](../android.graphics/Bitmap.md)!`)` Called when the icon has been retrieved from the database and the result is non-null. |

## Public methods

### onReceivedIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onReceivedIcon(
    url: String!, 
    icon: Bitmap!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the icon has been retrieved from the database and the result is non-null.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The url passed in the request. |
| `icon` | [Bitmap](../android.graphics/Bitmap.md)!:The favicon for the given url. |
