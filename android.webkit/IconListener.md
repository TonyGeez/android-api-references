# WebIconDatabase.IconListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IconListener

Kotlin| [Java](https://developer.android.com/reference/android/webkit/WebIconDatabase.IconListener "View this page in Java") 
| --- | --- |

```
interface IconListener
```

| [android.webkit.WebIconDatabase.IconListener](https://developer.android.com/reference/kotlin/android/webkit/WebIconDatabase.IconListener#) |

| **This interface was deprecated in API level 18.**
|
| This interface is obsolete.

Interface for receiving icons from the database.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedIcon](https://developer.android.com/reference/kotlin/android/webkit/WebIconDatabase.IconListener#onReceivedIcon(kotlin.String,%20android.graphics.Bitmap))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `icon:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!`)` Called when the icon has been retrieved from the database and the result is non-null. |

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
| `icon` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!:The favicon for the given url. |
